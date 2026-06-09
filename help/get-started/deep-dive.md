---
title: Mix Modeler Deep Dive
description: Explore la metodología técnica subyacente a Adobe Mix Modeler, incluida la atribución multitáctil, el modelado de la combinación de marketing, el aprendizaje de transferencia y la optimización del presupuesto.
feature: Administration
hide: true
feature_v2:
  - id: a234aebd-3855-4376-a64d-29b38411e0c5
  - id: fe1c9ae8-a908-4ae1-a0b6-fcf35177b134
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
source-git-commit: 4f4fe68694c81ddb258656eb05d62ef057f200cb
workflow-type: tm+mt
source-wordcount: 2747
ht-degree: 0%

---


# Inmersión profunda


Adobe Mix Modeler es una plataforma de medición unificada con tecnología AI/ML que combina atribución multitáctil (MTA) y modelado de combinación de marketing (MMM) para ofrecer perspectivas de marketing precisas, escalables y preparadas para el futuro. Este artículo presenta un desglose detallado de la metodología, las opciones de diseño y las innovaciones técnicas que subyacen a Mix Modeler. Y se basa en [esta sesión de Summit de 2025](https://business.adobe.com/summit/2025/sessions/marketing-mix-modeling-at-adobe-learn-to-predict-s602.html){target="_blank"}, que presenta un desglose detallado de la metodología, las opciones de diseño y las innovaciones técnicas detrás de Mix Modeler.

A medida que aumenta la complejidad del marketing, los enfoques de medición tradicionales se quedan cortos. Los datos fragmentados, las cambiantes restricciones de privacidad y la necesidad de velocidad y rigor hacen necesario reconsiderar cómo se evalúa el rendimiento de marketing. La respuesta de Adobe es Mix Modeler: un sistema integrado que utiliza el aprendizaje automático para sintetizar varias fuentes de datos y paradigmas de modelado en una estrategia coherente.


>[!TIP]
>
>Una de las ventajas clave de Mix Modeler es la accesibilidad de la solución para los especialistas en marketing. La aplicación simplifica las complejidades de la ciencia de datos a través de una interfaz fácil de usar que no requiere conocimientos de ciencia de datos. Si le interesa profundizar, este artículo explora las opciones técnicas realizadas al desarrollar Mix Modeler. El artículo asume cierta familiaridad con conceptos (avanzados) de ciencia de datos.

Este artículo explica los componentes básicos con más detalle. Estos componentes básicos son:

* [atribución multitáctil](#multi-touch-attribution-mta)
* [modelado de combinación de marketing](#marketing-mix-modeling-mmm)
* [transferir aprendizaje](#transfer-learning) (el intercambio inteligente de resultados entre la atribución de múltiples contactos y el modelado de la combinación de marketing)



## Atribución multitáctil (MTA)


### Información general

El modelo de atribución multitáctil (MTA) que alimenta Mix Modeler se basa en un modelo de supervivencia de tiempo discreto entrenado en datos de nivel de evento. Los datos incluyen búsquedas, clics, vistas de productos, adición a carros de compras y cierres de compra. Utilizando el aprendizaje supervisado, el modelo estima la probabilidad condicional de conversión en cada paso del recorrido del cliente. El modelo considera las rutas de recorrido del cliente de conversión y no conversión para medir cómo los distintos puntos de contacto de marketing influyen en el comportamiento del cliente a lo largo del tiempo. La ruta de no conversión es tan importante como la ruta de conversión. El contraste entre las dos rutas ayuda a comprender si un tipo particular de punto de contacto de marketing impulsa la conversión de forma eficaz. Por ejemplo, si un tipo de punto de contacto aparece como probable en una ruta que no es de conversión o en una ruta de conversión, ese punto de contacto no tiene impacto en la conversión. Este comportamiento es contrario a un punto de contacto que aparece a menudo en una ruta de conversión y no en una ruta que no sea de conversión.

![Datos de nivel de evento](/help/assets/event-level-data.png)

### Conceptos clave

Los conceptos clave detrás de la atribución de múltiples contactos son:

* **Modelado de intereses**: la conversión del cliente se modela como una acumulación de interés a lo largo del tiempo.

  ![Interés por aumento de exposición](/help/assets/exposure-increases-interest.jpg)

  En este enfoque, una serie de señales de interés aumentan la probabilidad de conversión, cada una de ellas influida por

   * exposiciones a medios anteriores,
   * impacto de los medios de comunicación (un modelo de cómo las respuestas a la publicidad se acumulan y decaen en los mercados de consumo), y
   * otros factores basales.



  Estas señales se representan como *ϴ<sub>BL</sub>* + *ϴ<sub>E,tc-t1</sub>* + *ϴ<sub>E,tc-t2</sub>* y *ϴ<sub>S, tc-t3</sub>*, donde:

   * *ϴ*: ilustra los parámetros del modelo (lo que se ha aprendido del modelo).
   * *tc*: hora de la conversión.
   * *tc-tx: el tiempo entre la exposición y la conversión, que es relevante para el modelo.
   * *BL*: línea de base.
   * *E*: correo electrónico.
   * *S*: búsqueda.

  En el marco de modelado, el objetivo es tener en cuenta explícitamente el tiempo entre cada exposición a los medios y el momento de la conversión (*tc-tx*), reconociendo que las interacciones más recientes tienen más peso que las anteriores.

* **Asignación de probabilidad**: la probabilidad de conversión se deriva del nivel de interés mediante una función logística en forma de S.

  ![Probabilidad de conversión](/help/assets/probability-of-conversion.jpg)

  A través del aprendizaje automático supervisado que utiliza un modelo de supervivencia en tiempo discreto, la ilustración anterior visualiza el recorrido del cliente A con la conversión. El nivel de interés se muestra en el eje X y la probabilidad de conversión en el eje Y. Esta asignación muestra que la exposición del segundo correo electrónico (*ϴE, tc-t2*) tiene el mayor impacto en la conversión. Como indica un aumento significativo de la probabilidad de conversión en el momento de ese paso.

* **Menor rendimiento**: Los puntos de contacto adicionales tienen menos impacto incremental a medida que aumenta el interés.

  La curva en forma de S, de la ilustración anterior, también muestra que exponer al cliente a puntos de contacto adicionales tiene menos impacto incremental con niveles de interés crecientes.

* **Modelo de supervivencia en tiempo discreto**: El uso de un modelo de supervivencia en tiempo discreto introduce más flexibilidad en el modelo, lo que le permite capturar matices temporales en el comportamiento de los clientes. El modelo de supervivencia en tiempo discreto también relaja algunos de los supuestos más restrictivos requeridos por los modelos de supervivencia en tiempo continuo.

  ![Modelo de supervivencia de tiempo discreto](/help/assets/discrete-time-survival-model.jpg)

  Una función de tiempo continuo modela el impacto del correo electrónico y el stock en el nivel de interés, en cualquier momento desde el momento de la exposición: *ϴ<sub>E</sub>(t;⋋)*
Una función de tiempo discreto modela el impacto del material publicitario de correo electrónico en el nivel de interés como períodos de tiempo discretos mediante parámetros escalares: *ϴ<sub>E,i</sub> ≥ 0<sub>E,i+1</sub>*


### Ventajas

El enfoque de atribución multitáctil seleccionado para Mix Modeler tiene varias ventajas clave.

* Tenga en cuenta las rutas de conversión y no conversión, lo que garantiza una estimación más precisa del impacto real de los medios.
* Incorpore un inventario y retornos menguantes que modelen el comportamiento real del cliente y eviten suposiciones excesivamente simplificadas que a menudo se encuentran en los modelos basados en reglas.
* Escalar de forma eficaz a grandes conjuntos de datos gracias a la optimización de la informática distribuida y el procesamiento paralelo.
* Apoyar la atribución intuitiva de puntos de contacto que permite una interpretación clara al contrario de otros métodos como los modelos de Markov ocultos.
* Ofrezca un rendimiento sólido y una alta precisión predictiva cuando se compara con otros algoritmos de clasificación.

Mix Modeler proporciona una [interfaz fácil de usar para expertos en marketing](/help/models/insights.md#attribution) a las perspectivas resultantes de la atribución multitáctil.

![Datos de atribución de modelo](/help/assets/model-insights-attribution.png)


Aunque la atribución multitáctil proporciona todas estas ventajas, Mix Modeler no depende completamente de las perspectivas de conversión de los datos de nivel de evento. El modelado de combinaciones de marketing es otro componente fundamental para tener en cuenta los datos de nivel agregado.

## Modelado de combinación de marketing (MMM)

El modelado de la combinación de marketing (MMM) se basa en datos de nivel agregado y utiliza una estructura de modelo multiplicativo, en lugar de uno aditivo, para reflejar las interacciones de marketing en el mundo real.

![Datos de nivel agregado](/help/assets/mmm-aggregate-data.jpg)

La ilustración muestra datos de nivel agregado en formato tabular. Cada fila corresponde a un período de tiempo (normalmente una semana, a veces un día) y cada columna representa una variable. La tabla incluye:

* la columna conversion (la variable de resultado del modelo),
* columnas de medios (por ejemplo: búsqueda, visualización) y
* columnas de factor (por ejemplo, estacionalidad, promociones) para capturar influencias internas o externas fuera del gasto en medios que aún afectan el rendimiento de los medios.

El modelo predice las conversiones de la semana 4 usando los datos resaltados en verde claro, incluidos los factores de esa semana y las entradas históricas de los canales de medios.

### Conceptos clave

Los conceptos clave detrás del modelado de combinaciones de marketing son:

* **Modelo multiplicativo**: las ventas o las conversiones son el producto de una línea de base y de multiplicadores de medios.

  Por lo tanto, en lugar de utilizar un modelo aditivo:
  *Conversiones semanales = Demanda de línea de base **+**&#x200B;Multiplicador de búsqueda **+**&#x200B;Multiplicador de pantalla **+**....*
utilizar un modelo multiplicativo:
  *Conversiones semanales = Demanda de línea de base **x**&#x200B;Multiplicador de búsqueda **x**&#x200B;Multiplicador de pantalla **x**....*

  O en una fórmula: ** Y = ⨍<sub>BL</sub>(X<sub>factores</sub>;<sub>factores</sub>) x ⨍<sub>S</sub>(X<sub>S</sub>;<sub>S</sub>) x ⨍<sub>D</sub>(X<sub>D</sub>;<sub>D</sub>)*

  Por ejemplo:

   * Conversiones reales por semana: 1730.
   * Conversiones previstas por semana: 1787,5 = 1100 x 1,25 x 1,3, donde:
      * 1100: demanda basal prevista en la semana 4, una función para los datos de factor 1 y 2 de la semana 4.
      * 1,25: multiplicador de búsqueda predicha de la semana 4, una función de los datos de búsqueda de la semana 1 a la semana 4.
      * 1.3: multiplicador de visualización previsto de la semana 4, una función para los datos de visualización de la semana 1 a la semana 4.

  La diferencia anticipada entre lo que el modelo predice (1787.5) y las conversiones reales (1730) es el residual, que a menudo es pequeño en tamaño y no es algo de lo que preocuparse.


* **Capturar Adstock y disminuir el retorno**: Adstock se captura usando declive exponencial y funciones de potencia.

  ![Capturando devoluciones decrecientes de stock de anuncios](/help/assets/capturing-adstock-diminishing-return.jpg)


  El deterioro exponencial de un material puede ser de una o dos colas, dependiendo de dónde se produzca el impacto máximo después de la inversión en medios.

  Para evitar que disminuyan los retornos, se aplica la función de alimentación: *x<sup>∈</sup>* para *(0,1*). Esta función de potencia da como resultado un gráfico cóncavo para capturar el retorno decreciente. El retorno decreciente se captura en la función del multiplicador dentro del modelo MMM.


### Ventajas

Los beneficios del enfoque de modelado de combinación de marketing se basan en el hecho de que el modelo multiplicativo apoya mejor los comportamientos de marketing esperados en el mundo real. Por ejemplo:

* Sinergia de medios donde los canales de medios a menudo funcionan mejor juntos que aislados.
* Impacto variable en el tiempo en el que un mismo nivel de inversión en marketing puede generar diferentes rendimientos en diferentes momentos debido a factores externos.
* Recomendaciones presupuestarias a lo largo del tiempo en las que las condiciones de mercado previstas o las fluctuaciones de línea de base ayudan a informar la asignación presupuestaria a lo largo del tiempo.

Mix Modeler proporciona una [interfaz fácil de usar para expertos en marketing](/help/models/insights.md#attribution) a las distintas perspectivas que resultan del modelado de combinaciones de marketing. Por ejemplo, un desglose de contribución de factores para mostrar la proporción de las conversiones de base que puede atribuirse a varios factores incluidos en el modelo.


![Desglose de contribución de factores](/help/assets/factors-example.png)


#### Ejemplo

Este ejemplo simplificado ilustra cómo un enfoque de modelado multiplicativo para una tienda en línea ficticia de zapatillas permite una mejor asignación de presupuesto que el modelo aditivo.

![Enfoque de modelo multiplicativo](/help/assets/benefits-mmm.jpg)

##### Suposiciones

* La demanda de zapatillas es mayor en verano y menor en invierno, como ilustran las contribuciones de referencia totales.

* La estrategia predeterminada para la planificación del marketing es gastar una cantidad fija del presupuesto de marketing (840 dólares) durante todo el año, cuando cada mes obtiene el mismo presupuesto.

* Adstock se ignora y los medios de pago se tratan como una unidad. Estas suposiciones son independientes del modelo elegido y no influyen en la comparación.

* Un presupuesto constante en el modelo aditivo significa una contribución constante durante cada mes, lo que se refleja para el modelo aditivo en el gráfico superior de la columna central.

* En el modelo multiplicativo, un presupuesto constante significa multiplicadores constantes cada mes. Para proporcionar un impacto variable en el tiempo para el mismo gasto mensual, el multiplicador funciona con la demanda de línea de base. Ese efecto multiplicador se muestra en el gráfico inferior de la columna central.

##### Mover presupuestos

¿Existe alguna capacidad para alejarse de un presupuesto fijo, cambiando el presupuesto, pero manteniendo el presupuesto total en $840?

* En el modelo aditivo, no hay ningún incentivo desde la perspectiva del modelo para realizar un cambio, ya que no hay interacción con la línea de base. Tener un gasto fijo es óptimo. Si mueve 1 dólar de noviembre a mayo, la ganancia en mayo es menor que la caída en noviembre debido a la disminución de los retornos.
* En un modelo multiplicativo, hay espacio para moverse. En función de la línea de base, puede cambiar los presupuestos de los meses de invierno a los de verano. La ganancia en el mes de verano es mayor que la pérdida en el mes de invierno debido al efecto de multiplicación. La extensión del cambio y la ubicación a la que se realizará se explican en los [algoritmos de optimización de presupuesto](#budget-optimization) utilizados en el modelado de combinaciones de marketing.



## Transferir aprendizaje

Junto con la atribución de múltiples contactos y el modelado de mezclas de marketing, la experimentación es otro pilar importante en la resolución de problemas de medición de marketing. Aunque la experimentación no se implementa en Mix Modeler, puede utilizarla, como desactivar el marketing en determinados mercados, para comprender el impacto causal del marketing en las ventas.

Adobe recomienda y emplea el aprendizaje de transferencia para combinar las perspectivas de atribución multitáctil, modelado de combinación de marketing, experimentación y otras fuentes de conocimiento anteriores.  Esta fusión se puede describir como un enfoque por capas. Cada capa tiene huecos para ilustrar las limitaciones en la producción de un modelo cohesivo. Pero si apilamos las capas de la manera correcta, podemos compensar los huecos en el modelo combinado.
Aplique esta analogía cuando utilice la combinación de atribución multitáctil, modelado de combinación de marketing, experimentación y fuentes de conocimiento anteriores. Mezcle estos componentes de forma que la combinación sufra menos defectos en cada uno de los componentes.

En esencia, el aprendizaje de transferencia son algoritmos de optimización numérica en funcionamiento. Como parte del entrenamiento del modelo, se configura una función de pérdida (para cuantificar la diferencia entre la salida predicha de un modelo y el valor real (verdad del suelo)). Y se determina una métrica de bondad de ajuste (para evaluar cómo se alinean las predicciones de un modelo con los datos observados). A continuación, transfiera el aprendizaje y resuelva la optimización numérica para obtener los thetas (parámetros del modelo). Si hay una o más fuentes de información, esa función del objetivo de optimización original se aumenta con otro término. Ese término mide la distancia entre lo que suministró como conocimiento previo y lo que el modelo produce para comparar.


### Aprendizaje de transferencia bidireccional

Cuando se tienen datos de nivel de evento y datos de nivel agregado, el aprendizaje de transferencia bidireccional implica el siguiente flujo de trabajo.

![Aprendizaje de transferencia bidireccional](/help/assets/bi-directional-transfer-learning.jpg)

| Paso | Descripción |
|:---:|---|
| 1a | El modelo de MTA predeterminado recibe formación sobre los datos de. Normalmente, un modelo de MTA se entrena en un período de tiempo más corto que el modelo de MMM. Los datos abarcan los datos de evento de los canales en línea. |
| 1b | El modelo de MTA está entrenado. Normalmente, un modelo MMM se entrena en ventanas de tiempo de al menos dos años. Los datos cubren factores y canales en línea y sin conexión. |
| 2 | El modelo de MTA tiene una puntuación. |
| 3 | Los resultados del modelo de MTA puntuado se introducen en MMM como aprendizaje de transferencia. |
| 4 | El modelo MMM se actualiza con los datos de aprendizaje de transferencia. Esta actualización significa que se utiliza un nuevo conjunto de estimaciones de parámetros para obtener perspectivas adicionales y optimizar el presupuesto. Los canales y la cobertura de tiempo no cambian. |
| 5 | El modelo MMM se puntúa usando los datos agregados semanales de los canales. |
| 6 | El resultado del modelo MMM puntuado se introduce en el MTA como aprendizaje de transferencia. |
| 7 | Las puntuaciones de MTA para los datos de nivel de evento se actualizan mediante los resultados de aprendizaje de transferencia y se utilizan para obtener perspectivas adicionales. |

Tenga en cuenta lo siguiente:

* El MTA está limitado con respecto a la cobertura de canal (solo datos de nivel de evento de datos web y móviles por ejemplo), pero es ventajoso debido a la gran cantidad de datos. El aspecto clave del MTA es el rendimiento relativo.
* MMM entiende la imagen más holística con factores, canales en línea y sin conexión.
* El aprendizaje de transferencia de MTA a MMM actualiza el modelo MMM. Los resultados de aprendizaje de transferencia influyen en los parámetros que impulsan el *modelo* multiplicativo. El aprendizaje de transferencia de MMM a MTA actualiza el MTA *puntuaciones*. No es necesario influir en el modelo de MTA, ya que las puntuaciones iniciales ya son estadísticamente suficientes.

## Conocimientos previos

Por lo tanto, más allá del MTA, el MMM y la experimentación, existen muchas otras fuentes diferentes de conocimiento previo que puede aprovechar de forma opcional para la planificación de la medición de marketing. Diferentes empresas tienen diferentes fuentes de conocimiento previo. Algunos ejemplos son participación en el gasto, modelos internos anteriores o experiencia en el sector.

![Conocimientos previos](/help/assets/prior-knowledge.jpg)

El proceso de creación de modelos puede aprovechar todas estas fuentes de información a través del mismo proceso de aprendizaje de transferencia. Estas fuentes de conocimientos previos son opcionales. No es necesario tener fuentes de conocimientos anteriores para que funcione el modelado de combinaciones de marketing. Si no tiene conocimientos previos, el modelo predeterminado se utiliza para generar perspectivas de puntuación y, a continuación, optimizar el presupuesto. Si dispone de datos de conocimientos previos, puede utilizar el aprendizaje de transferencia para actualizar el modelo MMM.


## Optimización del presupuesto

La optimización del presupuesto se basa en el modelo MMM multiplicativo explicado anteriormente,

En un ejemplo sencillo, hay dos canales: búsqueda y visualización. Y usted tiene un presupuesto total. El objetivo es dividir el presupuesto entre los dos canales para maximizar la conversión. La optimización numérica se utiliza para encontrar la combinación de presupuesto óptima que maximiza la conversión bajo la restricción de presupuesto total. Por ejemplo, imaginemos que la restricción presupuestaria total es de 130 000 $.

La fórmula de optimización del presupuesto es: *⨍ máximo(X<sub>S</sub>, X<sub>D</sub>) = ⨍<sub>BL</sub>(X<sub>factores</sub>) x ⨍<sub>S</sub>(X<sub>S</sub>) x ⨍<sub>D</sub>(X<sub>D</sub>)*, donde *X<sub>S</sub>* y *X<sub>D</sub>* son parámetros y *X<sub>factores</sub>* está previsto.

![Restricciones de presupuesto](/help/assets/budget-constraints.png)


### Restricciones de nivel de canal

Imagine que tiene restricciones de nivel de canal adicionales:

* $10K - $80K para la búsqueda.
* $5.000 - $70.000 para visualización.
* 130.000 dólares en total.

Como resultado, la combinación de presupuestos elegibles provoca que la superficie de optimización esté restringida. A continuación, el algoritmo de optimización numérica ayuda a determinar la asignación de presupuesto óptima.

### En varias conversiones

Además de las restricciones de nivel de canal, planifique una asignación presupuestaria óptima en varias conversiones.

![Optimización del presupuesto entre conversiones](/help/assets/planning-across-multiple-conversions.jpg)

Para dar cabida a una asignación presupuestaria óptima entre conversiones, se utiliza una media ponderada de la función anterior para cada una de las conversiones. La fórmula se convierte en *⨍<sub>nuevo</sub>(X) = con<sub>1</sub>f<sub>1</sub>(X) + con<sub>2</sub>f<sub>2</sub>(X)*

Algunos ejemplos de optimización del presupuesto en varias conversiones son:

* Desea maximizar los ingresos totales de las ventas en línea y las conversiones de ventas en tienda.
* Desea optimizar el éxito a largo plazo mediante los KPI de reconocimiento de marca y las conversiones de ventas.

En el segundo ejemplo, las unidades de las dos conversiones no son similares (KPI de conocimiento de marca frente a conversiones), pero eso no importa. Las conversiones o modelos no tienen que hacer referencia a los mismos canales y también pueden superponerse. La optimización numérica encuentra la mejor solución al problema dentro de las restricciones dadas.


## Resumen

Adobe Mix Modeler es más que una herramienta de medición; Mix Modeler es un motor de apoyo a la toma de decisiones y sus puntos fuertes son:

* La capacidad de modelar la complejidad real con rigor estadístico
* Una integración unificada de diversos paradigmas de modelado y datos
* Una arquitectura preparada para el futuro que se adapta a las tendencias de obsolescencia de los datos

La combinación de interpretabilidad y rendimiento ha hecho que Mix Modeler sea fundamental para la transformación de marketing basada en datos de Adobe. Mix Modeler permite a los equipos de marketing tomar decisiones de inversión más rápidas, inteligentes y alineadas.
