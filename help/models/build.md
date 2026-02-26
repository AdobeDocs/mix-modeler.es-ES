---
title: Crear modelos en Mix Modeler
description: Aprenda a crear modelos en Mix Modeler, incluyendo cómo configurar y especificar opciones avanzadas para el modelo.
feature: Models
solution: Mix Modeler
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: 56682fb57d6ca99fbf5d355ae487af2b31a72319
workflow-type: tm+mt
source-wordcount: '1194'
ht-degree: 2%

---

# Crear modelos

Para crear modelos personalizados con tecnología de IA, la interfaz proporciona un flujo de configuración de modelos guiado paso a paso.

En la interfaz ![Modelos](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** del Mix Modeler, seleccione **[!UICONTROL Open model canvas]**.

## Configuración

Usted define un nombre y una descripción en el paso **[!UICONTROL Setup]**:

1. Escriba el modelo **[!UICONTROL Name]**, por ejemplo `Demo model`. Escriba un **[!UICONTROL Description]**, por ejemplo `Demo model to explore AI features of Mix Modeler`.

   ![Nombre y descripción del modelo](/help/assets/model-name-description.png)

1. Seleccione **[!UICONTROL Next]** para continuar con el paso siguiente. Seleccione **[!UICONTROL Cancel]** para cancelar la configuración del modelo.

## Configurar{#configure}

>[!CONTEXTUALHELP]
>id="model_marketingtouchpoints_select"
>title="Puntos de contacto de marketing"
>abstract="Los puntos de contacto de marketing son eventos de marketing a nivel de destinatario, individuales o de cookie que se utilizan para evaluar el impacto de las inversiones de marketing en las conversiones numéricas o basadas en ingresos.<br/><br/>No puede configurar el modelo con puntos de contacto que tengan datos superpuestos y debe haber al menos un punto de contacto con el gasto."

Puede configurar su modelo en el paso **[!UICONTROL Configure]**. La configuración implica la definición de objetivos de conversión, puntos de contacto de marketing, la población de datos elegible, factores externos e internos, y más.

1. En la sección **[!UICONTROL Conversion goal]**:

   ![Modelo: paso de conversión](/help/assets/model-conversion-step.png)

   1. Seleccione una conversión en el menú desplegable **[!UICONTROL Conversion]**. Las conversiones disponibles son la conversión que definió como parte de [Conversiones](../harmonize-data/conversions.md) en [!UICONTROL Harmonized datasets]. Por ejemplo, **[!UICONTROL Online Conversion]**.

   1. Puede seleccionar ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) **[!UICONTROL Create a conversion]** para crear una conversión directamente desde la configuración del modelo.



1. En la sección **[!UICONTROL Marketing touchpoints]**, puede seleccionar uno o más puntos de contacto de marketing, correspondientes a los puntos de contacto de marketing que definió como parte de [puntos de contacto de marketing](../harmonize-data/marketing-touchpoints.md) en [!UICONTROL Harmonized datasets].


   ![Modelo: paso de punto de contacto de marketing](/help/assets/model-marketing-touchpoint-step.png)

   1. Seleccione uno o más puntos de contacto de marketing en el menú desplegable **[!UICONTROL Touchpoint include]**.

      * Puede usar ![CrossSize75](/help/assets/icons/CrossSize75.svg) para quitar un punto de contacto.
      * Puede usar **[!UICONTROL Clear all]** para eliminar todos los puntos de contacto.

   1. Puede seleccionar ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) **[!UICONTROL Create a touchpoint]** para crear un punto de contacto de marketing directamente desde la configuración del modelo.

   >[!NOTE]
   >
   >No puede configurar el modelo con puntos de contacto que tengan datos superpuestos y debe haber al menos un punto de contacto con gasto.

1. De forma predeterminada, se genera una puntuación para todos los datos de la vista armonizada. Para puntuar solo un subconjunto de la población, defina uno o más filtros usando contenedores en la sección **[!UICONTROL Eligible data population]**.

   ![Modelo: población de datos elegible](/help/assets/model-eligible-data-population-step.png)

   * Para cada contenedor, defina uno o más eventos.

      1. Para cada evento:

         1. Seleccione una métrica o dimensión de **[!UICONTROL _Seleccionar campo armonizado_]**.

         1. Seleccione el operador apropiado: **[!UICONTROL equals]**, **[!UICONTROL not equals]**, **[!UICONTROL less than]**, **[!UICONTROL greater than]**, **[!UICONTROL starts with]**, **[!UICONTROL doesn't start with]**, **[!UICONTROL ends with]**, **[!UICONTROL doesn't end with]**, **[!UICONTROL contains]**, **[!UICONTROL doesn't contain]**, **[!UICONTROL is in]** o **[!UICONTROL is not in]**.

         1. Escriba o seleccione un valor en **[!UICONTROL _Escriba o seleccione el valor_]**.

      1. Para agregar un evento adicional en el contenedor, seleccione ![Agregar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add event]**.

      1. Para quitar un evento del contenedor, seleccione ![Cerrar](/help/assets/icons/CrossSize75.svg).

      1. Para filtrar usando todos o cualquiera de los múltiples eventos definidos en el contenedor, seleccione **[!UICONTROL Any of]** o **[!UICONTROL All of]**. La etiqueta cambia de **[!UICONTROL Include ... Or ...]** a **[!UICONTROL Include ... And ...]**.

   * Para agregar un contenedor de población de datos apto, seleccione ![Agregar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add eligible population]**.

   * Para quitar un contenedor de población de datos apto, dentro del contenedor, seleccione ![Más](/help/assets/icons/More.svg) y **[!UICONTROL Remove container]** en el menú contextual.

   * Seleccione **And** y **Or** entre contenedores para generar definiciones más complejas para la población de datos elegible.

1. Puede administrar conjuntos de datos que contengan factores internos o externos en la sección **[!UICONTROL Factor dataset]**.

   ![Modelo: paso de conjunto de datos de factor](../assets/model-factors-dataset-step.png)

   * Para agregar un conjunto de datos de factor, seleccione **[!UICONTROL Add Factor]**. Puede añadir un máximo de 30 factores a un modelo.

      1. Seleccione un **[!UICONTROL Factor dataset]** en el menú desplegable. Los factores disponibles son los factores para los que ha definido un campo armonizado en [reglas del conjunto de datos](/help/harmonize-data/dataset-rules.md#create-a-dataset-rule).
Según el conjunto de datos seleccionado, el **[!UICONTROL Factor type**] es **[!UICONTROL Internal]** o **[!UICONTROL External]**.

      1. Seleccione **[!UICONTROL Impact on conversion]** en el menú desplegable. Las opciones disponibles son: **[!UICONTROL Auto]**, **[!UICONTROL Positive]** o **[!UICONTROL Negative]**. La opción predeterminada es **[!UICONTROL Auto]**, que permite al modelo determinar el impacto del conjunto de datos de factor.

   * Para eliminar un conjunto de datos de factor, seleccione ![CrossSize200](/help/assets/icons/CrossSize400.svg).




1. Para definir la ventana retrospectiva del modelo, escriba un valor entre `1` y `52` en **[!UICONTROL Give contribution credit to touchpoints occurring within]**... **[!UICONTROL weeks prior to the conversion]** en la sección **[!UICONTROL Define lookback window]**.

1. Seleccione **[!UICONTROL Next]** para continuar con el paso siguiente. Si se necesita más configuración, un contorno rojo y texto explican qué configuración adicional se requiere. <br/>Seleccione **[!UICONTROL Back]** para regresar al paso anterior. <br/>Seleccione **[!UICONTROL Cancel]** para cancelar la configuración del modelo.


## Avanzadas

Puede especificar la configuración avanzada en el paso **[!UICONTROL Advanced]**. En este paso, puede habilitar el modelo para atribución multitáctil (MTA).

1. En la sección **[!UICONTROL Spend share]**:

   * Para usar las relaciones de inversión de marketing históricas para informar al modelo cuando los datos de marketing son dispersos, active **[!UICONTROL Allow spend share]**. Se recomienda esta configuración, especialmente en los siguientes casos:
      * Un canal no tiene suficientes observaciones (por ejemplo, baja frecuencia de gasto, impresiones o clics).
      * Estás modelando medios llamativos pero regulares y potencialmente muy gastados (como la televisión para algunas marcas), donde los datos pueden ser escasos.

     >[!NOTE]
     >
     >En el caso de inversiones puntuales (por ejemplo, un anuncio de la Super Bowl), considere la posibilidad de incorporar esos datos como un factor, en lugar de depender de la participación en el gasto.
     >


1. En la sección **[!UICONTROL MTA enabled]**:

   * Para habilitar las características de MTA para el modelo, active **[!UICONTROL MTA enabled]**. Si ha habilitado el MTA, los conocimientos de atribución multitáctil estarán disponibles una vez que haya formado y marcado a su modelo. Consulte la pestaña [Atribución](insights.md#attribution) en [Información del modelo](insights.md).

1. En la sección **[!UICONTROL Prior knowledge]**:

   ![Modelo - Conocimientos previos](/help/assets/model-prior-knowledge-step.png)

   1. Seleccione **[!UICONTROL Rule type]**, que es de forma predeterminada **[!UICONTROL Absolute values]**.

   1. Especifique los porcentajes de contribución para cualquiera de los canales enumerados en **[!UICONTROL Name]**, utilizando la columna **[!UICONTROL Contribution proportion]**.

   1. Si corresponde, puede agregar para cada canal un porcentaje de **[!UICONTROL Level of confidence]**.

   1. Cuando sea necesario, use **[!UICONTROL Clear all]** para borrar todos los valores de entrada de las columnas **[!UICONTROL Contribution proportion]** y **[!UICONTROL Level of confidence]**.


## Establecer opciones

Puede [programar entrenamiento y puntuación](#schedule), [definir ventana de entrenamiento](#training-window) y especificar [campos de informes de conocimientos detallados](#granular-insights-reporting-fields) para su modelo en el paso **[!UICONTROL Set options]**.


### Programación

En la sección **[!UICONTROL Schedule]**, puede programar entrenamiento y puntuación de modelos.

![Modelo de programación](../assets/model-schedule.png)

Para programar la puntuación y el entrenamiento del modelo:

1. Activar **[!UICONTROL Enable scheduled model scoring and training]**.
1. Seleccione un **[!UICONTROL Scoring frequency]**:

   * **[!UICONTROL Daily]**: Introduzca una hora válida (por ejemplo, `05:22 pm`) o utilice ![Reloj](/help/assets/icons/Clock.svg).
   * **[!UICONTROL Weekly]**: Seleccione un día de la semana y escriba una hora válida (por ejemplo, `05:22 pm`) o utilice ![Reloj](/help/assets/icons/Clock.svg).
   * **[!UICONTROL Monthly]**: Seleccione un día del mes en el menú desplegable Ejecutar y escriba una hora válida (por ejemplo, `05:22 pm`) o utilice ![Reloj](/help/assets/icons/Clock.svg).

1. Seleccione un(a) **[!UICONTROL Training frequency]** del menú desplegable: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** o **[!UICONTROL None]**.


### Ventana de formación

En la sección **[!UICONTROL Define training window]**, seleccione entre:

![Modelo - Definir ventana de formación](/help/assets/model-define-training-window.png)

* **[!UICONTROL Have Mix Modeler select a helpful training window]** y

* **[!UICONTROL Manually input a training window]**. Cuando esté seleccionado, defina el número de años en **[!UICONTROL Include events the following years prior to a conversion]**.


### Campos de informes de perspectivas granulares

La sección **[!UICONTROL Granular insights reporting fields]** utiliza la funcionalidad de informes de incrementalidad granular. Esta funcionalidad le permite seleccionar campos armonizados para desglosar las puntuaciones de conversión e incrementalidad de punto de contacto.

![Definir campos granulares de informes de perspectivas](/help/assets/granular-insights-reporting-fields.png)

Estos campos armonizados se definen de modo que se pueda explorar en profundidad el sistema de informes del modelo mediante columnas de informes granulares en lugar de tener que crear modelos separados.

Por ejemplo, crea un modelo centrado en los ingresos, pero también le interesa el rendimiento de las campañas, los tipos de medios, las regiones y las fuentes de tráfico. Sin la funcionalidad de creación de informes de incrementalidad granular, tendría que crear cuatro modelos independientes. Con la funcionalidad de creación de informes de incrementalidad granular, puede desglosar el modelo de ingresos en campañas, tipos de medios, regiones y fuentes de tráfico.

1. Seleccione uno o más campos armonizados de **[!UICONTROL _Seleccionar campos armonizados_]** debajo de **[!UICONTROL Includes]**. Los campos armonizados seleccionados se añaden al panel.
1. Seleccione **[!UICONTROL *Campo armonizado *]**![CrossSize100](/help/assets/icons/CrossSize100.svg) para quitar un campo armonizado del contenedor con los campos armonizados seleccionados.
1. Seleccione **[!UICONTROL Clear all]** para eliminar todos los campos armonizados seleccionados.

Los campos armonizados seleccionados para los informes de incrementalidad granular están disponibles como parte de los conjuntos de datos [schema](/help/ingest-data/schemas.md) y [dataset](/help/ingest-data/datasets.md) de Experience Platform que resultan de la puntuación del modelo. Los campos de informes de datos detallados se pueden encontrar dentro de los objetos **[!UICONTROL conversionPassthrough]** y **[!UICONTROL touchpointPassthrough]**.

![Captura de pantalla de los objetos conversionPassthrough y touchpointPassthrough en un esquema para un modelo habilitado para la creación de informes de incrementalidad granular](/help/assets/schema-granular-insights-reporting.png)


## Finalizar

* Seleccione **[!UICONTROL Finish]** para finalizar la configuración del modelo.

   * En el cuadro de diálogo **[!UICONTROL Create instance?]**, seleccione **[!UICONTROL Ok]** para almacenar en déclencheur el primer conjunto de entrenamientos y ejecuciones de puntuación inmediatamente. Su modelo aparece con el estado ![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Awaiting training]**.

     Seleccione **[!UICONTROL Cancel]** para cancelar.

   * Si se necesita más configuración, un contorno rojo y texto explican qué configuración adicional se requiere.

* Seleccione **[!UICONTROL Back]** para volver al paso anterior.

* Seleccione **[!UICONTROL Cancel]** para cancelar la configuración del modelo.

