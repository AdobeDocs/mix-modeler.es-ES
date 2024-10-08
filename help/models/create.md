---
title: Creación de un modelo
description: Obtenga información sobre cómo crear un modelo en Mix Modeler.
feature: Models
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---

# Creación de un modelo

Para crear un modelo, en la interfaz de ![Modelos](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** del Mix Modeler, seleccione **[!UICONTROL Open model canvas]**.

Para crear sus modelos personalizados con tecnología de IA, la interfaz proporciona un flujo de configuración de modelo guiado paso a paso.

1. En el paso **[!UICONTROL Setup]**:

   1. Escriba el modelo **[!UICONTROL Name]**, por ejemplo `Demo model`. Escriba un **[!UICONTROL Description]**, por ejemplo `Demo model to explore AI featues of Mix Modeler`.

      ![Nombre y descripción del modelo](/help/assets/model-name-description.png)

   1. Seleccione **[!UICONTROL Next]** para continuar con el paso siguiente. Seleccione **[!UICONTROL Cancel]** para cancelar la configuración del modelo.

1. En el paso **[!UICONTROL Configure]**:

   1. En la sección **[!UICONTROL Conversion goal]**, dentro del contenedor:

      1. Escriba **[!UICONTROL Conversion name]** para la conversión, por ejemplo `Conversion`

      1. Seleccione una conversión de **[!UICONTROL *Seleccionar campo armonizado *]**que contenga las conversiones disponibles que definió como parte de [Conversiones](../harmonize-data/conversions.md) en [!UICONTROL Harmonized datasets]. Por ejemplo,**[!UICONTROL Online Conversion]**.

      1. Puede seleccionar ![Responder](/help/assets/icons/Reply.svg) **[!UICONTROL Create new conversion]** para crear una conversión directamente desde la configuración del modelo.

         ![Modelo: paso de conversión](/help/assets/model-conversion-step.png)

   1. En la sección **[!UICONTROL Marketing touchpoints]**, verá una serie de contenedores de puntos de contacto de marketing, correspondientes a los puntos de contacto de marketing que definió como parte de [puntos de contacto de marketing](../harmonize-data/marketing-touchpoints.md) en [!UICONTROL Harmonized datasets].

      * Para cada contenedor:

         1. Puede modificar **[!UICONTROL Marketing touchpoint name]**.

         1. Seleccione un punto de contacto de marketing de **[!UICONTROL _Seleccione un punto de contacto de marketing_]**.

         1. Puede seleccionar ![Responder](/help/assets/icons/Reply.svg) **[!UICONTROL Create new marketing touchpoint]** para crear un punto de contacto de marketing directamente desde la configuración del modelo.

      * Para agregar un contenedor de punto de contacto de marketing, seleccione ![Agregar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add marketing touchpoint]**.

      * Para quitar un contenedor de punto de contacto de marketing, dentro del contenedor, seleccione ![Más](/help/assets/icons/More.svg) y **[!UICONTROL Remove container]** en el menú contextual.

        ![Modelo: puntos de contacto de marketing-step](/help/assets/model-marketing-touchpoint-step.png)

   1. De forma predeterminada, se genera una puntuación para todos los datos de la vista armonizada. Para puntuar solo un subconjunto de la población, defina uno o más filtros usando contenedores en la sección **[!UICONTROL Eligible data population]**.

      * Para cada contenedor, defina uno o más eventos.

         1. Para cada evento:

            1. Seleccione una métrica o dimensión de **[!UICONTROL _Seleccionar campo armonizado_]**.

            1. Seleccione el operador apropiado: **[!UICONTROL equals]**, **[!UICONTROL not equals]**, **[!UICONTROL less than]**, **[!UICONTROL greater than]**, **[!UICONTROL starts with]**, **[!UICONTROL doesn't start with]**, **[!UICONTROL ends with]**, **[!UICONTROL doesn't end with]**, **[!UICONTROL contains]**, **[!UICONTROL doesn't contain]**, **[!UICONTROL is in]** o **[!UICONTROL is not in]**.

            1. Escriba o seleccione un valor en **[!UICONTROL _Escriba o seleccione el valor_]**.

         1. Para agregar un evento adicional en el contenedor, seleccione ![Agregar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add event]**.

         1. Para quitar un evento del contenedor, seleccione ![Cerrar](/help/assets/icons/Close.svg).

         1. Para filtrar usando todos o cualquiera de los múltiples eventos definidos en el contenedor, seleccione **[!UICONTROL Any of]** o **[!UICONTROL All of]**. La etiqueta cambia de **[!UICONTROL Include ... Or ...]** a **[!UICONTROL Include ... And ...]**.

      * Para agregar un contenedor de población de datos apto, seleccione ![Agregar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add eligible population]**.

      * Para quitar un contenedor de población de datos apto, dentro del contenedor, seleccione ![Más](/help/assets/icons/More.svg) y **[!UICONTROL Remove marketing touchpoint]** en el menú contextual.

        ![Modelo: población de datos elegible](/help/assets/model-eligible-data-population-step.png)

   1. Para agregar conjuntos de datos que contengan factores externos al modelo, utilice uno o más contenedores en la sección **[!UICONTROL External factors dataset]**.

      * Para cada contenedor:

         1. Escriba un **[!UICONTROL Factor name]** en **[!UICONTROL _Introducir factor_]**.

         1. Seleccione un conjunto de datos de **[!UICONTROL _Seleccione un conjunto de datos_]**. Puede seleccionar ![Datos](/help/assets/icons/Data.svg) para administrar conjuntos de datos. Consulte [Conjuntos de datos](../ingest-data/datasets.md) para obtener más información.

      * Para agregar un contenedor de conjunto de datos de factores externos adicional, seleccione ![Agregar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

      * Para quitar un contenedor de conjunto de datos de factores externos, dentro del contenedor, seleccione ![Más](/help/assets/icons/More.svg) y seleccione **[!UICONTROL Remove external factor]** en el menú contextual.

        ![Modelo: conjunto de datos de factores externos](/help/assets/model-external-factors-dataset-step.png)


   1. Para agregar conjuntos de datos que contengan factores internos al modelo, utilice uno o más contenedores en la sección **[!UICONTROL Internal factors dataset]**.

      * Para cada contenedor:

         1. Escriba un **[!UICONTROL Factor name]** en **[!UICONTROL _Introducir factor_]**.

         1. Seleccione un conjunto de datos de **[!UICONTROL _Seleccione un conjunto de datos_]**. Puede seleccionar ![Datos](/help/assets/icons/Data.svg) para administrar conjuntos de datos. Consulte [Conjuntos de datos](../ingest-data/datasets.md) para obtener más información.

      * Para agregar un contenedor de conjunto de datos de factores internos adicional, seleccione ![Agregar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add internal factor]**.

      * Para quitar un contenedor de conjunto de datos de factores internos adicional, dentro del contenedor, seleccione ![Más](/help/assets/icons/More.svg) y **[!UICONTROL Remove internal factor]** del menú contextual.

        ![Modelo: conjunto de datos de factores internos](/help/assets/model-internal-factors-dataset-step.png)

   1. Para definir la ventana retrospectiva del modelo, escriba un valor entre `1` y `52` en **[!UICONTROL Give contribution credit to touchpoints occurring within]**... **[!UICONTROL weeks prior to the conversion]**.

   1. Seleccione **[!UICONTROL Next]** para continuar con el paso siguiente. Si se necesita más configuración, un contorno rojo y texto explican qué configuración adicional se requiere. <br/>Seleccione **[!UICONTROL Back]** para regresar al paso anterior. <br/>Seleccione **[!UICONTROL Cancel]** para cancelar la configuración del modelo.

1. En el paso **[!UICONTROL Advanced]**:

   1. En la sección **[!UICONTROL Define training window]**, seleccione entre

      * **[!UICONTROL Have Mix Modeler select a helpful training window]** y

      * **[!UICONTROL Manually input a training window]**. Cuando esté seleccionado, defina el número de años en **[!UICONTROL Include events the following years prior to a conversion]**.

        ![Modelo - Definir ventana de formación](/help/assets/model-define-training-window.png)

   1. En la sección **[!UICONTROL Spend share]**:

      * Para usar las relaciones de inversión de marketing históricas para informar al modelo cuando los datos de marketing son dispersos, active **[!UICONTROL Allow spend share]**.

   1. En la sección **[!UICONTROL Prior knowledge]**:

      1. Seleccione el **[!UICONTROL Rule type]**.

      1. Especifique los porcentajes de contribución para cualquiera de los canales enumerados en **[!UICONTROL Name]**, utilizando la columna **[!UICONTROL Contribution proportion]**.

      1. Si corresponde, puede agregar para cada canal un porcentaje de **[!UICONTROL Level of confidence]**.

      1. Si es necesario, use **[!UICONTROL Clear all]** para borrar todos los valores de entrada de las columnas **[!UICONTROL Contribution proportion]** y **[!UICONTROL Level of confidence]**.

         ![Modelo - Conocimientos previos](/help/assets/model-prior-knowledge-step.png)

1. Seleccione **[!UICONTROL Finish]** para finalizar la configuración del modelo.

   * En el cuadro de diálogo **[!UICONTROL Create instance?]**, seleccione **[!UICONTROL Ok]** para almacenar en déclencheur el primer conjunto de entrenamientos y ejecuciones de puntuación inmediatamente. Su modelo aparece con el estado <span style="color:orange">●</span> **[!UICONTROL Awaiting training]**.

     Seleccione **[!UICONTROL Cancel]** para cancelar.

   * Si se necesita más configuración, un contorno rojo y texto explican qué configuración adicional se requiere.

   Seleccione **[!UICONTROL Back]** para volver al paso anterior.

   Seleccione **[!UICONTROL Cancel]** para cancelar la configuración del modelo.
