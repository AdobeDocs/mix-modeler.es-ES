---
title: Reglas de conjuntos de datos
description: Obtenga información sobre cómo definir reglas de conjuntos de datos para utilizarlas como parte de la armonización de los datos en el Modelador de mezcla de Adobe.
feature: Harmonized Data, Dataset Rules
source-git-commit: ac17f5a9fcf036c8e689879578e4b745b789cea3
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---


# Reglas de conjuntos de datos

Las reglas de conjuntos de datos le ayudan a asignar los campos armonizados con campos de los datos introducidos en el Modelador de mezcla de Adobe.

* Para los datos agregados que ha introducido en Adobe Experience Platform, asigne uno o más de los campos de conjunto de datos disponibles a los campos armonizados correspondientes.
* Para los datos de evento, puede asignar individualmente uno o más campos armonizados a campos del conjunto de datos, directamente o mediante condiciones.


## Administrar reglas y asignaciones de conjuntos de datos

Para ver una tabla de las asignaciones de conjuntos de datos disponibles, en la interfaz del Modelador de mezcla de Adobe:

1. Seleccionar ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** desde el carril izquierdo.

1. Seleccionar **[!UICONTROL Dataset rules]** desde la barra superior. Verá una tabla de asignaciones de conjuntos de datos.

Las columnas de la tabla especifican detalles sobre las asignaciones de conjuntos de datos:

| Nombre de columna | Detalles |
| ---------------------- | ----------|
| Conjunto de datos | Nombre del conjunto de datos. |
| Fuente | El origen del conjunto de datos, que puede ser Adobe Analytics, Eventos de experiencia, Resumen (acumulado) o Eventos de experiencia del consumidor. |
| Esquema | Esquema al que se ajusta el conjunto de datos. Puede seleccionar rápidamente el nombre del esquema para abrirlo en una nueva pestaña del editor de esquemas en el Modelador de mezcla de Adobes: Esquemas. |
| Granularidad | La granularidad de los datos del conjunto de datos. Los valores posibles son Diario, Semanal, Mensual o Anual. |
| Inicio de semana | Especifica qué día de la semana se considera el inicio de una nueva semana para el conjunto de datos específico. |
| Última modificación | Datos y hora de la última modificación de la asignación del conjunto de datos. |

{style="table-layout:auto"}

### Creación de una asignación de conjunto de datos

Para crear una asignación de conjunto de datos, en la variable ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** interfaz en el Modelador de mezcla de Adobe, seleccione **[!UICONTROL Create Dataset Mapping]**.

En el **[!UICONTROL Create]** pantalla,

1. Entrada **[!UICONTROL Dataset Details]**, seleccione un conjunto de datos de **[!UICONTROL Select dataset]** para comenzar la configuración.

1. Seleccione un día para la **[!UICONTROL Start of the week]**.

1. Seleccionar **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** o **[!UICONTROL Yearly]** para **[!UICONTROL Granularity]**.

1. Cuando haya seleccionado una **[!UICONTROL Summary]** tipo de conjunto de datos:

   1. Asigne cada uno de los **[!UICONTROL Available dataset fields]** a correspondiente **[!UICONTROL Standard harmonized fields]**. Si no desea asignar un campo de conjunto de datos a un campo armonizado, seleccione explícitamente **[!UICONTROL -- None --]**.

   1. Si necesita un nuevo campo armonizado, no disponible en la lista, seleccione **[!UICONTROL Create New]** para crear un nuevo campo armonizado. Verá el cuadro de diálogo como se describe en [Añadir un nuevo campo armonizado](fields.md#add-a-harmonized-field) para permitirle añadir rápidamente un nuevo campo armonizado.

   1. Cuando finalice la asignación para todos los campos, seleccione **[!UICONTROL Save]**. Seleccionar **[!UICONTROL Cancel]** para cancelar la asignación.

      ![Crear reglas de conjuntos de datos](../assets/dataset-create-summary.png)

1. Cuando haya seleccionado un tipo de evento de conjunto de datos, en el cuadro sombreado situado debajo de **[!UICONTROL Map to harmonized fields]**:

   1. Seleccione un campo armonizado de **[!UICONTROL Standard harmonized field]**.

   1. Cuando el campo armonizado seleccionado es del tipo métrica:

      1. Seleccionar **[!UICONTROL Count]** o **[!UICONTROL Sum]** de **[!UICONTROL Mapping type]**.

      1. Seleccione un **[!UICONTROL *Campo del conjunto de datos AEP *]**que desea que el campo armonizado se asigne a de forma predeterminada.

   1. Cuando el campo seleccionado es de tipo dimensión:

      1. Seleccionar **[!UICONTROL Map Into]** o **[!UICONTROL Case]** de **[!UICONTROL Mapping type]**.

      1. Cuando haya seleccionado **[!UICONTROL Map Into]**, seleccione **[!UICONTROL Field]** y **[!UICONTROL *Campo del conjunto de datos AEP *]**o **[!UICONTROL Value]**y un valor predeterminado para asignar el campo armonizado de forma predeterminada al campo del conjunto de datos o al valor introducido.

      1. Cuando haya seleccionado **[!UICONTROL Case]**, seleccione **[!UICONTROL Field]** y **[!UICONTROL *Campo del conjunto de datos AEP *]**o **[!UICONTROL Value]**y un valor predeterminado para asignar el campo armonizado de forma predeterminada al campo del conjunto de datos o al valor introducido.

         1. Además, puede definir uno o más casos, que consisten en una o más condiciones para establecer explícitamente valores. Cada condición puede comprobar una condición específica **[!UICONTROL *Campo del conjunto de datos AEP *]**ya sea **[!UICONTROL Exists]**o **[!UICONTROL Not Exists]**o si **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**, o **[!UICONTROL Ends With]**un valor introducido en**[!UICONTROL * Introducir valor de entrada *]**.

         1. Para añadir otro caso, seleccione ![Añadir](../assets/icons/AddCircle.svg) **[!UICONTROL Add case]**, para añadir otra condición, seleccione ![Añadir](../assets/icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. Para eliminar un caso o condición, seleccione ![Cerrar](../assets/icons/Close.svg) en el contenedor correspondiente.

         1. Para seleccionar si alguna o todas las condiciones deben aplicarse a un caso, seleccione **[!UICONTROL Any of]** o **[!UICONTROL All of]**.

         1. Para establecer el valor de resultado de un caso, introduzca el valor en **[!UICONTROL Then]**.

      El ejemplo siguiente

      * utiliza un **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** para asignar el **[!UICONTROL Channel Type At Source]** campo armonizado para el **[!UICONTROL channel_type]** del campo **[!DNL Luma Transactions]** conjunto de datos.

      * utiliza un **[!UICONTROL Case]** **[!UICONTROL Mapping]** escriba para asignar de forma condicional el valor de **[!UICONTROL marketing.campaignName]** en el campo **[!DNL Luma Transactions]** conjunto de datos a **[!UICONTROL Campaign]** campo armonizado. El campo Campaña armonizada se establece en:

         * `Black Friday` cuando la variable **[!UICONTROL marketing.campaignName]** es `_black_friday` o `BlackFriday`.
         * al valor del **[!UICONTROL marketing.campaignName]** en todos los demás casos.

        ![Evento de regla del conjunto de datos](../assets/dataset-create-event.png)

1. Seleccionar ![Añadir](../assets/icons/AddCircle.svg) **[!UICONTROL Add field]** para definir campos adicionales.

Cuando termine, seleccione **[!UICONTROL Save]** para guardar la asignación, o seleccione **[!UICONTROL Cancel]** para cancelar la asignación.


### Edición de una asignación de conjunto de datos

Para editar una asignación de conjunto de datos, en la variable ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** Interfaz en el Modelador de mezcla de Adobe:

1. Seleccionar ![Más](../assets/icons/More.svg) en el **[!UICONTROL Dataset]** para la asignación de conjuntos de datos que desea editar.
1. En el menú contextual, seleccione ![Editar](../assets/icons/Edit.svg) **[!UICONTROL Edit]** para empezar a editar la asignación del conjunto de datos. Consulte [Creación de una asignación de conjunto de datos](#create-a-dataset-mapping) para obtener más información.


### Eliminar una asignación de conjunto de datos

Para eliminar una asignación de conjunto de datos, en la variable ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** Interfaz en el Modelador de mezcla de Adobe:

1. Seleccionar ![Más](../assets/icons/More.svg) en el **[!UICONTROL Dataset]** para la asignación de conjuntos de datos que desea eliminar.
1. En el menú contextual, seleccione ![Eliminar](../assets/icons/Delete.svg) **[!UICONTROL Delete]** para eliminar la asignación del conjunto de datos.


## Sincronizar datos

Para sincronizar datos entre los datos armonizados y los conjuntos de datos de resumen o evento, siga toda la lógica de las reglas del conjunto de datos:

1. Seleccione **[!UICONTROL Sync data]**.

1. Desde el **[!UICONTROL Sync data for dataset rules]** , seleccione una de las siguientes opciones **[!UICONTROL Refresh harmonized data for summary datasets]**, **[!UICONTROL Refresh harmonized data for event datasets]**, o **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Seleccionar **[!UICONTROL Sync]** para iniciar la sincronización basada en las reglas del conjunto de datos definidas entre los datos armonizados y los datos de conjuntos de datos. Para cancelar la sincronización, seleccione **[!UICONTROL Cancel]**.

   ![Sincronizar datos](../assets/sync-data.png)

