---
title: Modelos de compilación
description: Aprenda a crear modelos en Mix Modeler.
feature: Models
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: f12eea7454d1c81b347dc4960f5c491d81725f7d
workflow-type: tm+mt
source-wordcount: '893'
ht-degree: 0%

---

# Modelos de compilación

Para crear sus modelos personalizados con tecnología de IA, la interfaz proporciona un flujo de configuración de modelo guiado paso a paso.

En la interfaz de ![Modelos](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** del Mix Modeler, seleccione **[!UICONTROL Open model canvas]**.

## Configurar

El nombre y la descripción se definen en el paso **[!UICONTROL Setup]**:

1. Escriba el modelo **[!UICONTROL Name]**, por ejemplo `Demo model`. Escriba un **[!UICONTROL Description]**, por ejemplo `Demo model to explore AI featues of Mix Modeler`.

   ![Nombre y descripción del modelo](/help/assets/model-name-description.png)

1. Seleccione **[!UICONTROL Next]** para continuar con el paso siguiente. Seleccione **[!UICONTROL Cancel]** para cancelar la configuración del modelo.

## Configurar

El modelo se configura en el paso **[!UICONTROL Configure]**. La configuración implica la definición de los objetivos de conversión, los puntos de contacto de marketing, la población de datos apta, los factores externos e internos, etc.

1. En la sección **[!UICONTROL Conversion goal]**:

   ![Modelo: paso de conversión](/help/assets/model-conversion-step.png)

   1. Seleccione una conversión en el menú desplegable **[!UICONTROL Conversion]**. Las conversiones disponibles son las conversiones que definió como parte de [Conversiones](../harmonize-data/conversions.md) en [!UICONTROL Harmonized datasets]. Por ejemplo, **[!UICONTROL Online Conversion]**.

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

   * Para quitar un contenedor de población de datos apto, dentro del contenedor, seleccione ![Más](/help/assets/icons/More.svg) y **[!UICONTROL Remove marketing touchpoint]** en el menú contextual.

   * Seleccione **And** y **Or** entre contenedores para generar definiciones más complejas para la población de datos elegible.


1. Para agregar conjuntos de datos que contengan factores externos al modelo, utilice uno o más contenedores en la sección **[!UICONTROL External factors dataset]**. Un ejemplo de factores externos son los índices S&amp;P.

   ![Modelo: conjunto de datos de factores externos](/help/assets/model-external-factors-dataset-step.png)

   * Para cada contenedor:

      1. Escriba un **[!UICONTROL External factor name]**, por ejemplo `External Factors`.

      1. Seleccione un conjunto de datos del menú desplegable **[!UICONTROL Dataset]**. Puede seleccionar ![Datos](/help/assets/icons/Data.svg) para administrar conjuntos de datos. Consulte [Conjuntos de datos](../ingest-data/datasets.md) para obtener más información.

      1. Seleccione una opción del menú desplegable **[!UICONTROL Impact on conversion]**: **[!UICONTROL Auto select]**, **[!UICONTROL Positive]** o **[!UICONTROL Negative]**.

   * Para agregar un contenedor de conjunto de datos de factores externos adicional, seleccione ![Agregar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

   * Para quitar un contenedor de conjunto de datos de factores externos, seleccione ![RemoveCircle](/help/assets/icons/RemoveCircle.svg).




1. Para agregar conjuntos de datos que contengan factores internos al modelo, utilice uno o más contenedores en la sección **[!UICONTROL Internal factors dataset]**. Un ejemplo de factores internos son los datos de marketing por correo electrónico.

   ![Modelo: conjunto de datos de factores internos](/help/assets/model-internal-factors-dataset-step.png)

   * Para cada contenedor:

      1. Escriba un **[!UICONTROL Internal factor name]**, por ejemplo `Email Marketing Data`.

      1. Seleccione un conjunto de datos de **[!UICONTROL _Seleccione un conjunto de datos_]**. Puede seleccionar ![Datos](/help/assets/icons/Data.svg) para administrar conjuntos de datos. Consulte [Conjuntos de datos](../ingest-data/datasets.md) para obtener más información.

      1. Seleccione una opción del menú desplegable **[!UICONTROL Impact on conversion]**: **[!UICONTROL Auto select]**, **[!UICONTROL Positive]** o **[!UICONTROL Negative]**.

   * Para agregar un contenedor de conjunto de datos de factores internos adicional, seleccione ![Agregar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add internal factor]**.

   * Para quitar un contenedor de conjunto de datos de factores internos, seleccione ![RemoveCircle](/help/assets/icons/RemoveCircle.svg).



1. Para definir la ventana retrospectiva del modelo, escriba un valor entre `1` y `52` en **[!UICONTROL Give contribution credit to touchpoints occurring within]**... **[!UICONTROL weeks prior to the conversion]**.

1. Seleccione **[!UICONTROL Next]** para continuar con el paso siguiente. Si se necesita más configuración, un contorno rojo y texto explican qué configuración adicional se requiere. <br/>Seleccione **[!UICONTROL Back]** para regresar al paso anterior. <br/>Seleccione **[!UICONTROL Cancel]** para cancelar la configuración del modelo.


## Avanzadas

Puede especificar la configuración avanzada en el paso **[!UICONTROL Advanced]**. En este paso puede habilitar el modelo para atribución multitáctil (MTA).

1. En la sección **[!UICONTROL Spend share]**:

   * Para usar las relaciones de inversión de marketing históricas para informar al modelo cuando los datos de marketing son dispersos, active **[!UICONTROL Allow spend share]**.

1. En la sección **[!UICONTROL MTA enabled]**:

   * Para habilitar las características de MTA para el modelo, active **[!UICONTROL MTA enabled]**. Si ha habilitado el MTA, las perspectivas de atribución multitáctil están disponibles después de haber entrenado y puntuado al modelo. Consulte la pestaña [Atribución](insights.md#attribution) en [Información del modelo](insights.md).

1. En la sección **[!UICONTROL Prior knowledge]**:

   ![Modelo - Conocimientos previos](/help/assets/model-prior-knowledge-step.png)

   1. Seleccione **[!UICONTROL Rule type]**, que es de forma predeterminada **[!UICONTROL Absolute values]**.

   1. Especifique los porcentajes de contribución para cualquiera de los canales enumerados en **[!UICONTROL Name]**, utilizando la columna **[!UICONTROL Contribution proportion]**.

   1. Si corresponde, puede agregar para cada canal un porcentaje de **[!UICONTROL Level of confidence]**.

   1. Si es necesario, use **[!UICONTROL Clear all]** para borrar todos los valores de entrada de las columnas **[!UICONTROL Contribution proportion]** y **[!UICONTROL Level of confidence]**.


## Programación

Puede programar la formación y la puntuación del modelo en el paso **[!UICONTROL Schedule]**.

1. En la sección **[!UICONTROL Schedule]** puede programar la formación y la puntuación del modelo.

   ![Modelo de horario](../assets/model-schedule.png)

   Para programar la puntuación y la formación del modelo:

   1. Activar **[!UICONTROL Enable scheduled model scoring and training]**.
   1. Seleccionar un **[!UICONTROL Scoring frequency]**:

      * **[!UICONTROL Daily]**: escriba una hora válida (por ejemplo, `05:22 pm`) o use ![Reloj](/help/assets/icons/Clock.svg).
      * **[!UICONTROL Weekly]**: seleccione un día de la semana e introduzca una hora válida (por ejemplo, `05:22 pm`) o use ![Reloj](/help/assets/icons/Clock.svg).
      * **[!UICONTROL Monthly]**: selecciona un día del mes en el menú desplegable Ejecutar en cada e introduce una hora válida (por ejemplo, `05:22 pm`) o usa ![Reloj](/help/assets/icons/Clock.svg).

   1. Seleccione un(a) **[!UICONTROL Training frequency]** del menú desplegable: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** o **[!UICONTROL None]**.

1. En la sección **[!UICONTROL Define training window]**, seleccione entre:

   ![Modelo - Definir ventana de formación](/help/assets/model-define-training-window.png)

   * **[!UICONTROL Have Mix Modeler select a helpful training window]** y

   * **[!UICONTROL Manually input a training window]**. Cuando esté seleccionado, defina el número de años en **[!UICONTROL Include events the following years prior to a conversion]**.


1. Seleccione **[!UICONTROL Finish]** para finalizar la configuración del modelo.

   * En el cuadro de diálogo **[!UICONTROL Create instance?]**, seleccione **[!UICONTROL Ok]** para almacenar en déclencheur el primer conjunto de entrenamientos y ejecuciones de puntuación inmediatamente. Su modelo aparece con el estado ![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Awaiting training]**.

     Seleccione **[!UICONTROL Cancel]** para cancelar.

   * Si se necesita más configuración, un contorno rojo y texto explican qué configuración adicional se requiere.

   Seleccione **[!UICONTROL Back]** para volver al paso anterior.

   Seleccione **[!UICONTROL Cancel]** para cancelar la configuración del modelo.
