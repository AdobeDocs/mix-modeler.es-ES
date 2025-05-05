---
title: Conversiones
description: Aprenda a crear conversiones para utilizarlas en la armonización de los datos en Mix Modeler.
feature: Harmonized Data, Conversions
exl-id: a8559426-452a-43e8-9a60-0c0bc97d863c
source-git-commit: 935b179e31d1b677a8c83b1566c02b7aaa617e8d
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---

# Conversiones

Los eventos de conversión son objetivos empresariales que identifican el impacto de las actividades de marketing. Ejemplos: pedidos de comercio electrónico, compras en tienda, visitas a sitios web, etc.

Las conversiones de marketing se definen para el análisis de atribución.

## Administración de conversiones

Para ver una tabla de las conversiones disponibles, en la interfaz del Mix Modeler:

1. Seleccione ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** en el carril izquierdo.

1. Seleccione **[!UICONTROL Conversions]** de la barra superior. Verá una tabla de conversiones.

Las columnas de la tabla especifican detalles sobre la conversión:

| Nombre de columna | Detalles |
| --- | ---|
| Nombre | Nombre de la conversión. |
| Ingresos | La métrica de datos armonizados que se utilizará para calcular los ingresos procedentes de una conversión. |
| Métrica de conversión | La métrica de datos armonizada que se utilizará como métrica de conversión para el análisis. |
| Categoría | La categoría de conversión de la conversión. |
| Creado | Fecha y hora de creación de la conversión. |
| Última modificación | Fecha y hora de la última modificación de la conversión. |


## Añadir una conversión

Para agregar una conversión, en la interfaz de ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** del Mix Modeler:

1. Seleccione ![Agregar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion]**.

1. En el diálogo **[!UICONTROL Create conversion]**:

   1. Escriba un nombre para **[!UICONTROL Conversion]**, por ejemplo `Store Conversions`.

   1. Defina **[!UICONTROL Conversion category]**.

      1. Seleccione un valor de **[!UICONTROL *Seleccionar armonizar...*]**, por ejemplo `Conversion types`.

      1. Seleccione un valor para el operador ![Chevron](/help/assets/icons/ChevronDown.svg), por ejemplo **[!UICONTROL is]**.

      1. Seleccione un valor de **[!UICONTROL *Seleccionar valor *]**&#x200B;o escriba un valor, por ejemplo **[!UICONTROL Store]**.

   1. Seleccione un campo armonizado de **[!UICONTROL Conversion metric for analysis]**, por ejemplo **[!UICONTROL Orders]**.

   1. Seleccione un campo armonizado de **[!UICONTROL Revenue field]**, por ejemplo **[!UICONTROL Gross Demand]**.

   1. Para crear la conversión, seleccione **[!UICONTROL Create]**. Para cancelar la creación de una conversión, seleccione **[!UICONTROL Cancel]**.

      ![Texto alternativo](/help/assets/create-conversion.png)

1. Cuando se crea, la conversión se añade a la tabla de conversiones.


## Ver detalles

Para ver los detalles de una conversión:

1. Seleccione ![Más](/help/assets/icons/More.svg) al pasar el ratón sobre un nombre de conversión de la tabla.

1. Seleccione ![Ver](/help/assets/icons/ViewDetail.svg) **Ver detalles**. Un cuadro de diálogo muestra los detalles de la conversión. Consulte [Agregar una conversión](#add-a-conversion) para obtener más información. Seleccione **[!UICONTROL Cancel]** para cerrar el cuadro de diálogo.

## Ver informe

Para ver un informe de una conversión:

1. Seleccione ![Más](/help/assets/icons/More.svg) al pasar el ratón sobre un nombre de conversión de la tabla.

1. Seleccione ![GraphTrend](/help/assets/icons/GraphTrend.svg) **Ver informe**. Un cuadro de diálogo muestra un informe de la conversión.

   ![Informe de vista de conversión](../assets/conversion-view-report.png)

   * Para cambiar la granularidad sobre la que generar el informe, seleccione un valor del menú desplegable **[!UICONTROL Weekly]**.
   * Para cambiar el período del que se va a realizar el informe, escriba una fecha de inicio y otra de finalización o use ![Calendario](/help/assets/icons/Calendar.svg) para definir un período en la ventana emergente del calendario.

1. Seleccione **[!UICONTROL Close]** para cerrar el cuadro de diálogo.

## Eliminar una conversión

Para eliminar una conversión:

1. Seleccione ![Delete](/help/assets/icons/Delete.svg) **Delete** al pasar el ratón por encima de un nombre de conversión en la tabla.
1. En el cuadro de diálogo de confirmación **[!UICONTROL Delete conversion]**, seleccione **[!UICONTROL Delete]** para eliminar permanentemente la conversión.
