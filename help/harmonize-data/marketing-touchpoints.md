---
title: Puntos de contacto de marketing
description: Aprenda a crear puntos de contacto de marketing para utilizarlos en la armonización de los datos en Mix Modeler.
feature: Harmonized Data, Marketing Touch Points
exl-id: 42851107-7568-4bc9-92ca-3cba713a522e
source-git-commit: b3e52a34f26574961823c08859f17e2e6f1fdcd3
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# Puntos de contacto de marketing {#marketing-touchpoints}

>[!CONTEXTUALHELP]
>id="harmonizeddata_marketingtouchpoint"
>title="Punto de contacto de marketing"
>abstract="Los puntos de contacto de marketing son eventos de marketing a nivel de destinatario, individual o de cookie que se utilizan para evaluar el impacto de las inversiones de marketing en las conversiones numéricas o basadas en ingresos."


Los puntos de contacto de marketing son eventos de marketing a nivel de destinatario, individual o de cookie que se utilizan para evaluar el impacto de las inversiones de marketing en las conversiones numéricas o basadas en ingresos.

Puede definir puntos de contacto de marketing para ayudarle en el análisis de atribución.

## Administrar puntos de contacto de marketing

Para ver una tabla de los puntos de contacto de marketing disponibles en la interfaz de Mix Modeler:

1. Seleccione ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** en el carril izquierdo.

1. Seleccione **[!UICONTROL Marketing touchpoint]** de la barra superior. Verá una tabla de los puntos de contacto de marketing. Si hay más páginas disponibles, usa ![Flecha izquierda](/help/assets/icons/ChevronLeft.svg) o ![Flecha derecha](/help/assets/icons/ChevronRight.svg) en **[!UICONTROL Page _x _de_x_]** para moverte entre las páginas de la tabla.

Las columnas de la tabla especifican detalles sobre el punto de contacto de marketing:

| Nombre de columna | Detalles |
| --- | ---|
| Nombre | Nombre del punto de contacto de marketing. |
| Métrica de gasto | La métrica de datos armonizados que se utilizará para calcular el gasto en puntos de contacto. |
| Métrica de volumen | La métrica de datos armonizada que se utilizará para calcular el volumen del punto de contacto. |
| Regla | Regla de punto de contacto que se va a utilizar. |
| Creado | Fecha y hora de creación del punto de contacto de marketing. |
| Última modificación | Fecha y hora de la última modificación del punto de contacto de marketing. |


## Añadir un punto de contacto de marketing

Para agregar un punto de contacto de marketing, en la interfaz ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Marketing touchpoint]** de Mix Modeler:

1. Seleccione ![Agregar](/help/assets/icons/AddCircle.svg) Agregar punto de contacto de marketing.

1. En el diálogo **[!UICONTROL Marketing touchpoint]**.

   1. Escriba un nombre para **[!UICONTROL Touchpoint Name]**, por ejemplo `Luma Touchpoint`.

   1. Definir un **[!UICONTROL Touchpoint rule]**.

      1. Seleccione un valor de **[!UICONTROL *Seleccionar armonizado *]**, por ejemplo **[!UICONTROL Brand]**.

      1. Seleccione un valor para el operador ![Chevron](/help/assets/icons/ChevronDown.svg), por ejemplo **[!UICONTROL is]**.

      1. Seleccione un valor de **[!UICONTROL *Seleccionar valor *]**&#x200B;o escriba un valor, por ejemplo **[!DNL Luma]**.

   1. Seleccione un campo armonizado de **[!UICONTROL Touchpoint volume]**, por ejemplo **[!UICONTROL Impressions]**.

   1. Seleccione un campo armonizado de **[!UICONTROL Touchpoint spend]**, por ejemplo **[!UICONTROL Cost]**.

      ![Punto de contacto de marketing](/help/assets/create-touchpoint.png)

   1. Para crear el punto de contacto de marketing, seleccione **[!UICONTROL Create]**. Para cancelar la creación de un punto de contacto de marketing, seleccione **[!UICONTROL Cancel]**

1. Cuando se crea, el punto de contacto se añade a la tabla de puntos de contacto de marketing.


## Ver detalles

Para ver los detalles de un punto de contacto de marketing:

1. Seleccione ![Más](/help/assets/icons/More.svg) al pasar el ratón sobre un nombre de punto de contacto de marketing de la tabla.

1. Seleccionar ![Vista](/help/assets/icons/ViewDetail.svg) **Vista**. Un cuadro de diálogo muestra detalles del punto de contacto de marketing. Consulte [Agregar un punto de contacto de marketing](#add-a-marketing-touchpoint) para obtener más información. Seleccione **[!UICONTROL Cancel]** para cerrar el cuadro de diálogo.


## Ver informe

Para ver un informe de un punto de contacto de marketing:

1. Seleccione ![Más](/help/assets/icons/More.svg) al pasar el ratón sobre un nombre de punto de contacto de marketing de la tabla.

1. Seleccione ![GraphTrend](/help/assets/icons/GraphTrend.svg) **Ver informe**. Un cuadro de diálogo muestra un informe del punto de contacto de marketing.

   ![Informe de vista de punto de contacto de marketing](../assets/marketingtouchpoint-view-report.png)

   * Para cambiar la granularidad sobre la que generar el informe, seleccione un valor del menú desplegable **[!UICONTROL Weekly]**.
   * Para cambiar el período del que se va a realizar el informe, escriba una fecha de inicio y otra de finalización o use ![Calendario](/help/assets/icons/Calendar.svg) para definir un período en la ventana emergente del calendario.

1. Seleccione **[!UICONTROL Close]** para cerrar el cuadro de diálogo.

## Eliminación de un punto de contacto de marketing

Para eliminar un punto de contacto de marketing:

1. Seleccione ![Delete](/help/assets/icons/Delete.svg) **Delete** al pasar el ratón por encima del nombre de un punto de contacto de marketing en la tabla.
1. En el cuadro de diálogo de confirmación de **[!UICONTROL Delete touchpoint]**, seleccione **[!UICONTROL Delete]** para eliminar permanentemente el punto de contacto de marketing.

