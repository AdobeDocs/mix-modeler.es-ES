---
title: Conversiones
description: Aprenda a crear conversiones para utilizarlas en la armonización de los datos en Mix Modeler.
feature: Harmonized Data, Conversions
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 3%

---


# Conversiones

Los eventos de conversión son objetivos empresariales que identifican el impacto de las actividades de marketing. Ejemplos: pedidos de comercio electrónico, compras en tienda, visitas a sitios web, etc.

Las conversiones de marketing se definen para el análisis de atribución.

## Administración de conversiones

Para ver una tabla de las conversiones disponibles, en la interfaz del Mix Modeler:

1. Seleccionar ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** desde el carril izquierdo.

1. Seleccionar **[!UICONTROL Conversions]** desde la barra superior. Verá una tabla de conversiones.

Las columnas de la tabla especifican detalles sobre la conversión:

| Nombre de columna | Detalles |
| --- | ---|
| Nombre | Nombre de la conversión. |
| Ingresos | La métrica de datos armonizados que se utilizará para calcular los ingresos procedentes de una conversión. |
| Métrica de conversión | La métrica de datos armonizada que se utilizará como métrica de conversión para el análisis. |
| Creado | Fecha y hora de creación de la conversión. |
| Última modificación | Fecha y hora de la última modificación de la conversión. |

{style="table-layout:auto"}

## Añadir una conversión

Para añadir una conversión, en ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** interfaz en el Mix Modeler:

1. Seleccionar ![Añadir](../assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion]**.

1. En el **[!UICONTROL Create Conversion]** diálogo:

   1. Introduzca un nombre para **[!UICONTROL Conversion]**, por ejemplo `Store Conversions`.

   1. Defina el **[!UICONTROL Conversion category]**.

      1. Seleccione un valor de **[!UICONTROL *Seleccionar armonizar...*]**, por ejemplo `Conversion Type`.

      1. Seleccione un valor para el operador ![cheurón](../assets/icons/ChevronDown.svg), por ejemplo **[!UICONTROL is]**.

      1. Seleccione un valor de **[!UICONTROL *Seleccionar valor *]**o introduzca un valor, por ejemplo **[!UICONTROL Store]**.

   1. Seleccione un campo armonizado de **[!UICONTROL Conversion metric for analysis]**, por ejemplo **[!UICONTROL Orders]**.

   1. Seleccione un campo armonizado de **[!UICONTROL Revenue field]**, por ejemplo **[!UICONTROL Gross Demand]**.

   1. Para crear la conversión, seleccione **[!UICONTROL Create]**. Para cancelar la creación de una conversión, seleccione **[!UICONTROL Cancel]**.

      ![Texto alternativo](../assets/create-conversion.png)

1. Cuando se crea, la conversión se añade a la tabla de conversiones.
