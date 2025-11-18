---
title: Datos del modelo
description: Obtenga información sobre cómo obtener detalles acerca del modelo, como información general histórica, perspectivas del modelo y calidad del modelo en Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 1a9df9f9819d9e0031e58443ec6a9e755a151ba0
workflow-type: tm+mt
source-wordcount: '2332'
ht-degree: 2%

---

# Datos del modelo

Cada visualización de las perspectivas del modelo está diseñada para ayudarle a lo siguiente:

* Visualice y cuantifique el impacto de las actividades de marketing de su organización.
* Identifique qué canales tienen un alto rendimiento.
* Identifique qué canales pueden necesitar optimización.

A continuación, estas perspectivas le ayudan a admitir la priorización y asignación de recursos.

Para ver la información del modelo, en la interfaz de ![Modelos](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** en Mix Modeler:

1. En la tabla **[!UICONTROL Models]**, seleccione el nombre de un modelo que tenga **[!UICONTROL Last run status]** de <span style="color:green">●</span> **[!UICONTROL Success]**.

1. En el menú contextual, seleccione **[!UICONTROL Model Insights]**.



Las pestañas disponibles son las siguientes:

* [Datos del modelo](#model-insights)
* [Factores](#factors-beta) [!BADGE beta]
* [Atribución](#attribution) (solo para modelos con MTA habilitado)
* [Diagnósticos](#diagnostics)
* [Información general histórica](#historical-overview).

Puede cambiar el periodo de fecha en el que se basan las visualizaciones de cada una de las pestañas. Escriba un período de fecha o seleccione ![Calendario](/help/assets/icons/Calendar.svg) para elegir un período de fecha.

## Deriva de modelo

{{release-limited-testing-section}}

Si se detecta una deriva del modelo en el modelo, verá un cuadro de diálogo **[!UICONTROL Model drift detected]** con opciones que se le recordarán más adelante o que se [**[!UICONTROL Retrain]**](overview.md#retrain) inmediatamente el modelo. Si selecciona **[!UICONTROL Remind me later]**, se le avisará al día siguiente o al iniciar sesión más tarde.

![Cuadro de diálogo detectado de deriva de modelo](/help/assets/model-drift-dialog.png)

## [!UICONTROL Model insights]

La pestaña Información del modelo muestra visualizaciones para [Contribución por fecha y medios base](#contribution-by-date-and-base-media), [Contribución por canal](#contribution-by-channel), [Resumen de rendimiento de marketing](#marketing-performance-summary) y [Curvas de respuesta marginales](#marginal-response-curves). La pestaña también proporciona una tabla [Desglose de puntos de contacto](#touchppint-breakdown).

![Modelo - Datos del modelo](/help/assets/model-insights-insights.png)

* Puede situarse sobre elementos de gráfico individuales en cada visualización para mostrar una ventana emergente con más detalles.

* Para descargar un archivo CSV que contenga los datos de la visualización, seleccione ![Descargar](/help/assets/icons/Download.svg).

* Para descargar datos completos de información del modelo en formato Microsoft® Excel, seleccione ![Descargar](/help/assets/icons/Download.svg) **[!UICONTROL Download data]**.


### Contribución por fecha y medios base.

Esta visualización de gráficos apilados se ordena de la siguiente manera:

* La base se muestra en la parte inferior.
* Los canales que no son de gasto se muestran en el centro.
* Los canales de gasto se muestran arriba.

Esta visualización representa la proporción de contribución conseguida por base, por canales de gasto y por canales que no son de gasto, en un intervalo de fechas. Esta visualización es útil para mostrar la incrementalidad. La base representa lo que habría sucedido sin ningún tipo de marketing, y los canales que no son de gasto, además de los canales de gasto (además de la base) atribuyen el impacto de su marketing. En resumen, no gastar más gastar es igual al impacto incremental de sus esfuerzos de marketing y la visualización proporciona una insight sencilla en el valor que genera el marketing.

### Contribución por canal

Una visualización de anillo que muestra una distribución de la contribución por varios canales. Esta visualización muestra la incrementalidad a través del lente de los tres canales con mejor rendimiento (excluyendo las categorías base y *All other*). La visualización ayuda a admitir la priorización y la asignación de presupuesto.

### Resumen de rendimiento de marketing.

Una visualización de gráfico de barras horizontales que muestra el rendimiento de la inversión o de la CPA de cada uno de los canales. Esta visualización resalta el ROI/CPA de sus inversiones de marketing. Los canales se clasifican en orden descendente según el ROI/CPA. La visualización ayuda a identificar qué canales son los más efectivos y cuáles podrían necesitar optimización.

### Curvas de respuesta marginales.

El gráfico de líneas visualiza y compara los retornos marginales generados por la inversión en sus canales de marketing.  E identifica el punto de equilibrio en el que el retorno incremental es menor que el gasto incremental. Como resultado, esta visualización le ayuda a comprender cuándo la inversión en marketing empieza a tener menos impacto.

La curva, el punto de equilibrio y los valores correspondientes se calculan en función del rango de datos seleccionado y del canal seleccionado.

Para cambiar el canal:

* Seleccione un canal del menú desplegable **[!UICONTROL Channel]** para actualizar la visualización de un canal específico.


### Desglose por punto de contacto

La tabla de desglose de puntos de contacto muestra los desgloses semanales de puntos de contacto para todos los canales o los seleccionados, de forma semanal, y muestra las métricas clave asociadas a cada uno. La tabla permite realizar comparaciones, identificaciones de tendencias y seguimientos del rendimiento de forma sencilla a un nivel de canal más granular. Esta tabla complementa explícitamente la visualización [Contribución por fecha y medios base](#contribution-by-date-and-base-media) y la visualización [Contribución por canal](#contribution-by-channel).

![Desglose de punto de contacto](../assets/touchpoint-breakdown.png)

Las columnas disponibles son las siguientes:

| Columna | Descripción |
|---|---|
| **[!UICONTROL Date range]** | La semana sobre la que se debe informar. |
| **[!UICONTROL Touchpoint]** | El canal de punto de contacto específico. |
| **[!UICONTROL ROI]** | El porcentaje de (**[!UICONTROL Revenue]** - **[!UICONTROL Spend]**) / **[!UICONTROL Spend]**. |
| **[!UICONTROL Revenue]** | Ingresos para el intervalo de fechas. |
| **[!UICONTROL CPA]** | **[!UICONTROL Spend]** / **[!UICONTROL Conversions]**. |
| **[!UICONTROL Conversions]** | Las conversiones del intervalo de fechas. |
| **[!UICONTROL Spend]** | Gasto para el rango de datos. |

Para seleccionar un canal específico para todos los canales, seleccione en el menú desplegable **[!UICONTROL View]**.

Para descargar el contenido de la tabla de desglose de puntos de contacto, seleccione ![Descargar](/help/assets/icons/Download.svg) **[!UICONTROL Download CSV]**.

## **[!UICONTROL Factors]** [!BADGE beta]

La pestaña Factores [!BADGE beta] muestra información relacionada con factores externos.

![Factores](/help/assets/factors.png)

Esta visualización le ayuda a comprender el efecto incremental que varios factores internos y externos tienen en la línea de base de las conversiones. Por ejemplo, condiciones económicas o actividades promocionales.

Utilice el menú desplegable **[!UICONTROL Factors]** para seleccionar qué factores desea mostrar.

<!-- need to update the image when we do have a proper example -->

Para descargar un archivo CSV que contenga los datos de la tabla, seleccione ![Descargar](/help/assets/icons/Download.svg).

Si no hay datos disponibles, verá un mensaje ![TableAndChart](/help/assets/icons/TableAndChart.svg) **[!UICONTROL No data is available, you may need to retrain your model, or change the date range to view insights]**.

## [!UICONTROL Attribution]

>[!NOTE]
>
>La pestaña Atribución solo está disponible para modelos con MTA habilitado.


Con la ficha [!UICONTROL Attribution], puede comprender la eficacia de los puntos de contacto y las campañas de marketing que tienen datos de nivel de evento.  Consulte [Modelo de compilación](build.md).

Se admiten los siguientes modelos de atribución:

* En función del modelo seleccionado en Mix Modeler:
   * Algorítmico: influenciado
   * Algorítmico: incremental
* Basado en reglas:
   * Unidades de deterioro
   * Primer contacto
   * Último contacto
   * Lineal
   * Ushape

Consulte [Atribución multitáctil](../get-started/about.md#multi-touch-attribution) para obtener una introducción sobre la capacidad de atribución multitáctil en Mix Modeler.

Seleccione uno o varios modelos de atribución en el menú desplegable **[!UICONTROL Attribution Model]**. Los modelos de atribución seleccionados se aplican a todas las visualizaciones de la pestaña Atribución.

![Atribución](/help/assets/model-insights-attribution.png)

Las puntuaciones de evento granulares de atribución de múltiples contactos de Mix Modeler se alinean con las puntuaciones generales de Mix Modeler y los ROI. Estas puntuaciones también están disponibles como conjuntos de datos en Experience Platform.

La pestaña Atribución consta de las siguientes visualizaciones:

### [!UICONTROL Overview]

La visualización [!UICONTROL Overview] muestra, para los modelos de atribución seleccionados, las conversiones totales y porcentajes. Al seleccionar más modelos, se añaden círculos adicionales a la visualización, cada uno con su propio color correspondiente a la leyenda.

Para ver una ventana emergente con detalles para un modelo de atribución, pase el ratón sobre cualquiera de los círculos de la visualización.

### [!UICONTROL Trends]

La visualización [!UICONTROL Daily trends], [!UICONTROL Weekly trends] o [!UICONTROL Monthly trends] muestra, para los modelos de atribución seleccionados, las tendencias de conversión diarias, semanales o mensuales.

Para elegir el período, seleccione **[!UICONTROL Daily trends]**, **[!UICONTROL Weekly trends]** o **[!UICONTROL Monthly trends]** de entre ![Más](/help/assets/icons/More.svg).

Para ver los detalles, pase el ratón sobre la línea de datos de un modelo de atribución específico para mostrar una ventana emergente que muestre el número total de conversiones para esos datos.

### [!UICONTROL Breakdown]

La visualización [!UICONTROL Breakdown] es un desglose por canal o punto de contacto de las conversiones de cada uno de los modelos de atribución seleccionados. Esta visualización puede resultar útil para tomar decisiones sobre la eficacia de cada canal o punto de contacto.

Para elegir el tipo de desglose, seleccione **[!UICONTROL Breakdown by channel]** o **[!UICONTROL Breakdown by touchpoint]** de ![Más](/help/assets/icons/More.svg).

Para ver los detalles, pase el ratón sobre cualquiera de los elementos del gráfico.

### [!UICONTROL Top campaigns]

La visualización Campañas principales muestra una tabla de las campañas principales con columnas para Nombre de campaña, Canal, Tipo de medio y Conversiones incrementales. Esta visualización puede ayudar a informar a su equipo de la eficacia de una campaña específica para un canal determinado y proporcionar perspectivas sobre las campañas en las que debe invertir más.

Para ordenar la tabla en orden ascendente ↑ o descendente ↓ para el canal, el tipo de medio o las conversiones incrementales, seleccione el encabezado de la columna y cambie la ordenación.

Para expandir la tabla en un cuadro de diálogo independiente, seleccione **[!UICONTROL Expand]** de ![Más](/help/assets/icons/More.svg).

El cuadro de diálogo Campañas principales expandido muestra la misma tabla con columnas adicionales para

* Conversiones incrementales
* Conversiones influenciadas
* Conversiones de primer contacto
* Conversiones de último contacto

  Puede seleccionar cada uno de los encabezados de columna adicionales para ordenar la tabla en orden ascendente o descendente.

Para cerrar el cuadro de diálogo Campañas principales expandido, seleccione **[!UICONTROL Close]**.


### [!UICONTROL Breakdown by touchpoint position]

La visualización [!UICONTROL Breakdown by touchpoint position] es un desglose de conversiones atribuidas por posición del punto de contacto y del punto de contacto en todas las rutas de conversión. Este gráfico le ayuda a comparar si un punto de contacto contribuye mejor en una posición que las posiciones restantes y otros puntos de contacto en cualquier posición.

>[!NOTE]
>
>La suma de la contribución porcentual para un modelo de atribución en todos los puntos de contacto y posiciones debe ser igual a 100.


Las posiciones [!UICONTROL Starter], [!UICONTROL Player] y [!UICONTROL Closer] se definen de la siguiente manera:

| Posición | Descripción |
|---|---|
| [!UICONTROL Starter] | Esta posición indica si el punto de contacto es el primer contacto en una ruta de conversión. |
| [!UICONTROL Player] | Esta posición indica si el punto de contacto no es el primer ni el último contacto que provocó la conversión. |
| [!UICONTROL Closer] | Esta posición indica si el punto de contacto es el último contacto antes de la conversión. |


### [!UICONTROL Top conversion paths]

La visualización [!UICONTROL Top conversion paths] muestra las 5 rutas de conversión principales en función de los modelos de atribución seleccionados.

Para cada ruta de conversión, verá lo siguiente:

* la cantidad de canales que sí tienen impacto,
* el total de rutas atribuidas,
* el porcentaje de rutas atribuidas para esta ruta de conversión frente al total de rutas atribuidas,
* para cada canal, el porcentaje de contribución del modelo de atribución y
* la suma de estos porcentajes de contribución del modelo de atribución de canal.


## [!UICONTROL Diagnostics] {#diagnostics}


>[!CONTEXTUALHELP]
>id="models_diagnostics_modelassessment"
>title="Gráficos de evaluación de modelos"
>abstract="Las visualizaciones de evaluación de modelos desglosan las conversiones reales frente a las previstas o residuales."
>additional-url=" https://experienceleague.adobe.com/es/docs/mix-modeler/using/overview" text="Información general sobre Mix Modeler"
>additional-url="https://video.tv.adobe.com/v/3440794/?learn=on&enablevpops" text="Demostración de Mix Modeler"


>[!CONTEXTUALHELP]
>id="models_diagnostics_pathstouched"
>title="Rutas contactadas"
>abstract="Rutas contactadas es el porcentaje de rutas que consiguen la conversión y el porcentaje de rutas que no consiguen la conversión para cada punto de contacto."


>[!CONTEXTUALHELP]
>id="models_diagnostics_modeldateinfo"
>title="Fecha del modelo a partir de"
>abstract="Los datos de esta tabla solo se generan para periodos de tiempo específicos.  La fecha **[!UICONTROL As of]** indica cuándo se generaron los datos y se basa en los datos de startDate a endDate."


La ficha **[!UICONTROL Diagnostics]** muestra visualizaciones para:

* **[!UICONTROL Model Assessment]** visualizaciones, que constan de:

  ![Evaluación de modelo](../assets/model-assessment.png)

   * Gráfico que puede desglosar las conversiones reales frente a las previstas o residuales.
Para desglosar la visualización, seleccione una de las siguientes opciones en la lista **[!UICONTROL Breakdown]**.

      * **[!UICONTROL Actual vs Predicted]**: esta opción compara valores reales con predicciones de modelos. Lo ideal es que los valores predichos se alineen estrechamente con los valores reales, aunque se espera alguna desviación. Las desviaciones o patrones grandes o sistemáticos pueden indicar la falta de relaciones y datos o sesgos potenciales.

      * **[!UICONTROL Residuals]**: esta opción muestra la diferencia entre los valores reales y los predichos. Un modelo de buen rendimiento tiene residuos que se distribuyen aleatoriamente, sin patrones claros o con una propagación creciente. Las tendencias estructuradas o los residuales de ampliación pueden indicar relaciones faltantes y problemas de datos o varianza.

   * Una tabla que muestra las siguientes columnas para cada métrica de conversión:

      * **[!UICONTROL Actual Conversion]**
      * **[!UICONTROL Predicted Conversion]**
      * **[!UICONTROL Residual Conversion]**
      * **[!UICONTROL R<sup>2</sup>]**, una puntuación que indica cómo se ajustan los datos al modelo de regresión (la bondad de ajuste).
      * **[!UICONTROL MAPE]** (Error de porcentaje absoluto medio), que es uno de los KPI más utilizados para medir la precisión de la previsión y expresa el error de la previsión como un porcentaje del valor real.
      * **[!UICONTROL RMSE]** (Error cuadrático medio raíz): que muestra el error promedio, ponderado según el cuadrado del error.

  Para descargar un archivo CSV que contenga los datos de la tabla, seleccione ![Descargar](/help/assets/icons/Download.svg).

* **[!UICONTROL Model training fit metrics]** tabla, que se muestra para cada métrica de conversión:

  ![Tabla de métricas de ajuste de formación del modelo](../assets/model-training-fit-metrics.png)

   * **[!UICONTROL Training R<sup>2</sup>]**: indica la proporción de varianza en los valores reales explicados por las predicciones del modelo, que van de 0 a 1.
   * **[!UICONTROL Training sMAPE]** (error de porcentaje absoluto medio simétrico): mide el porcentaje de error promedio en los datos de formación. Los valores más bajos indican una mejor precisión.
   * **[!UICONTROL Training RMSE]** (error al cuadrado medio raíz): mide el porcentaje medio de error en los datos de formación. Penaliza los errores más grandes más que MAPE. Un menor RMSE sugiere una mejor precisión predictiva, pero es sensible a periféricos.
   * **[!UICONTROL Out-of-sample sMAPE]**: evalúa el porcentaje de error en datos no vistos, equilibrando las predicciones de exceso y de defecto. Ayuda a evaluar la generalización. Actualmente, Mix Modeler evalúa el porcentaje de error utilizando los datos del último trimestre de formación como un conjunto de no participación.
   * **[!UICONTROL Out-of-sample RMSE]**: evalúa el porcentaje de error en datos no vistos, equilibrando las predicciones de exceso y de defecto. Ayuda a evaluar la generalización. Actualmente, Mix Modeler evalúa el porcentaje de error utilizando los datos del último trimestre de formación como un conjunto de no participación. RMSE penaliza los errores más grandes más que MAPE.


* **[!UICONTROL Touchpoint effectiveness]**, que representa el resultado del modelo algorítmico de inteligencia artificial aplicada a la atribución.

  ![Tabla de efectividad del punto de contacto](../assets/touchpoint-effectiveness.png)

  Los datos de esta tabla solo se generan para periodos de tiempo específicos. Seleccione **[!UICONTROL As of *xx/xx/xx, xx:xx TZ *]**![Info](/help/assets/icons/InfoOutline.svg) para obtener más información.

  La visualización muestra, en orden descendente de [!UICONTROL Efficiency measure] ![Orden descendente](/help/assets/icons/SortOrderDown.svg), para cada punto de contacto:

   * **[!UICONTROL Paths touched]**: visualiza el porcentaje de rutas que consiguen conversión y el porcentaje de rutas que no logran conversión. Para un punto de contacto, verá conversiones atribuidas más cuando la proporción de conversión de atribución sea alta. Esta proporción compara el porcentaje de rutas que llevan a la conversión frente al porcentaje de rutas que llevan a la conversión *no*.
   * **[!UICONTROL Efficiency measure]**: generado por el modelo de atribución algorítmica, la medida de eficiencia indica la importancia relativa de un punto de contacto hacia la conversión, independientemente del volumen del punto de contacto. La eficiencia se mide en una escala de 1 a 5. Tenga en cuenta que un volumen de punto de contacto más alto no garantiza una medida de eficiencia más alta.
   * **[!UICONTROL Total volume]**: el número agregado de veces que un usuario toca un punto de contacto. El número incluye los puntos de contacto que aparecen en una ruta que logra la conversión, así como las rutas *no* que resultan en conversión.


### Detección de deriva del modelo

>[!AVAILABILITY]
>
>La funcionalidad descrita en esta sección se encuentra en la fase de prueba limitada de la versión y es posible que aún no esté disponible en su entorno. Esta nota se eliminará cuando la funcionalidad esté disponible de forma general. Para obtener información sobre el proceso de lanzamiento de Mix Modeler, consulte [lanzamientos de características de Mix Modeler](/help/releases/latest.md).
>

Si se detecta una desviación de modelo, verá una notificación **[!UICONTROL Model drift detected]** en la parte superior.

![Notificación de deriva del modelo](/help/assets/model-drift-notification.png)

Seleccione **[!UICONTROL Hide]** para ocultar la notificación. La notificación volverá a aparecer al día siguiente o al inicio de sesión siguiente.


## [!UICONTROL Historical overview]

La pestaña Información general histórica muestra visualizaciones para:

![Modelo: información general histórica](/help/assets/model-insights-historical-overview.png)


### Conversión y gasto por trimestre fiscal y producto

Esta visualización representa la conversión y la distribución del gasto en varios trimestres dentro del intervalo de fechas determinado. La visualización ayuda a identificar trimestres de alto rendimiento en los que el gasto genera conversiones.


### Gasto por canal

Esta visualización representa la distribución del gasto en varios canales dentro del intervalo de fechas determinado. La visualización admite la identificación rápida de los canales que reciben la mayor cantidad de gasto.


### Gasto de Touchpoint

Esta visualización representa la distribución del gasto en puntos de contacto de pago para cada trimestre dentro del intervalo de fechas determinado. La visualización permite comprender qué puntos de contacto se priorizan dentro de canales y trimestres específicos. La visualización ayuda a identificar los patrones y tendencias de gasto de los canales, especialmente los canales con gasto bajo y poco frecuente a lo largo del tiempo.

Para seleccionar un canal alternativo basado en gastos para mostrar en esta visualización:

* Seleccionar un canal de **[!UICONTROL Channels]**.


### Volumen de Touchpoint

Esta visualización representa la distribución del volumen en todos los puntos de contacto para cada trimestre dentro del intervalo de fechas determinado.

Para seleccionar un canal alternativo basado en volumen para mostrar en esta visualización:

* Seleccionar un canal de **[!UICONTROL Channels]**.


## **[!UICONTROL Edit]**

Puede editar el nombre, la descripción y la programación de la formación y la puntuación del modelo.

1. Seleccionar ![Editar](/help/assets/icons/Edit.svg) Editar

1. En el diálogo **[!UICONTROL Edit model]**:

   * Escriba un nuevo(a) **[!UICONTROL Name]** y **[!UICONTROL Description]**.

   * Para habilitar la programación, habilite **[!UICONTROL Status]**. Solo se puede activar la programación de modelos que se hayan entrenado y clasificado.

      1. Seleccionar un **[!UICONTROL Scoring frequency]**:

         * **[!UICONTROL Daily]**: escriba una hora válida (por ejemplo, `05:22 pm`) o use ![Reloj](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Weekly]**: seleccione un día de la semana e introduzca una hora válida (por ejemplo, `05:22 pm`) o use ![Reloj](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Monthly]**: selecciona un día del mes en el menú desplegable Ejecutar en cada e introduce una hora válida (por ejemplo, `05:22 pm`) o usa ![Reloj](/help/assets/icons/Clock.svg).

      1. Seleccione un(a) **[!UICONTROL Training frequency]** del menú desplegable: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** o **[!UICONTROL None]**.

     ![Editar un modelo](../assets/model-edit.png)

1. Seleccione **[!UICONTROL Save]**.
