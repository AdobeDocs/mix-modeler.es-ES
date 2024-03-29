---
title: Puntos de contacto de marketing
description: Aprenda a crear puntos de contacto de marketing para utilizarlos en la armonización de los datos en Mix Modeler.
feature: Harmonized Data, Marketing Touch Points
exl-id: 42851107-7568-4bc9-92ca-3cba713a522e
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# Puntos de contacto de marketing

Los puntos de contacto de marketing son eventos de marketing a nivel de destinatario, individual o de cookie que se utilizan para evaluar el impacto de las inversiones de marketing en las conversiones numéricas o basadas en ingresos.

Puede definir puntos de contacto de marketing para ayudarle en el análisis de atribución.

## Administrar puntos de contacto de marketing

Para ver una tabla de los puntos de contacto de marketing disponibles en la interfaz de Mix Modeler:

1. Seleccionar ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** desde el carril izquierdo.

1. Seleccionar **[!UICONTROL Marketing touchpoint]** desde la barra superior. Verá una tabla de los puntos de contacto de marketing. Si hay más páginas disponibles, utilice ![Flecha izquierda](../assets/icons/ChevronLeft.svg) o ![Flecha derecha](../assets/icons/ChevronRight.svg) en **[!UICONTROL Page _x _de_x_]** para desplazarse entre las páginas de la tabla.

Las columnas de la tabla especifican detalles sobre el punto de contacto de marketing:

| Nombre de columna | Detalles |
| --- | ---|
| Nombre | Nombre del punto de contacto de marketing. |
| Métrica de gasto | La métrica de datos armonizados que se utilizará para calcular el gasto en puntos de contacto. |
| Métrica de volumen | La métrica de datos armonizada que se utilizará para calcular el volumen del punto de contacto. |
| Regla | Regla de punto de contacto que se va a utilizar. |
| Creado | Fecha y hora de creación del punto de contacto de marketing. |
| Última modificación | Fecha y hora de la última modificación del punto de contacto de marketing. |

{style="table-layout:auto"}

## Añadir un punto de contacto de marketing

Para añadir un punto de contacto de marketing, en ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Marketing touchpoint]** interfaz en el Mix Modeler:

1. Seleccionar ![Añadir](../assets/icons/AddCircle.svg) Añadir punto de contacto de marketing.

1. En el **[!UICONTROL Marketing touchpoint]** diálogo.

   1. Introduzca un nombre para **[!UICONTROL Touchpoint Name]**, por ejemplo `Luma Touchpoint`.

   1. Defina un **[!UICONTROL Touchpoint rule]**.

      1. Seleccione un valor de **[!UICONTROL *Seleccionar armonizado *]**, por ejemplo **[!UICONTROL Brand]**.

      1. Seleccione un valor para el operador ![cheurón](../assets/icons/ChevronDown.svg), por ejemplo **[!UICONTROL is]**.

      1. Seleccione un valor de **[!UICONTROL *Seleccionar valor *]**o introduzca un valor, por ejemplo **[!DNL Luma]**.

   1. Seleccione un campo armonizado de **[!UICONTROL Touchpoint volume]**, por ejemplo **[!UICONTROL Impressions]**.

   1. Seleccione un campo armonizado de **[!UICONTROL Touchpoint spend]**, por ejemplo **[!UICONTROL Cost]**.

      ![Punto de contacto de marketing](../assets/create-touchpoint.png)

   1. Para crear el punto de contacto de marketing, seleccione **[!UICONTROL Create]**. Para cancelar la creación de un punto de contacto de marketing, seleccione **[!UICONTROL Cancel]** .

1. Cuando se crea, el punto de contacto se añade a la tabla de puntos de contacto de marketing.


## Ver un punto de contacto de marketing

Para ver un punto de contacto de marketing:

1. Seleccionar ![Más](../assets/icons/More.svg) al pasar el ratón por encima de un nombre de punto de contacto de marketing en la tabla.

1. Seleccionar ![Ver](../assets/icons/ViewDetail.svg) **Ver**. Un cuadro de diálogo muestra detalles del punto de contacto de marketing. Consulte [Añadir un punto de contacto de marketing](#add-a-marketing-touchpoint) para obtener más información. Seleccionar **[!UICONTROL Cancel]** para cerrar el cuadro de diálogo.


## Eliminación de un punto de contacto de marketing

Para eliminar un punto de contacto de marketing:

1. Seleccionar ![Eliminar](../assets/icons/Delete.svg) **Eliminar** al pasar el ratón por encima de un nombre de punto de contacto de marketing en la tabla.
1. En el **[!UICONTROL Delete touchpoint]** cuadro de diálogo de confirmación seleccionar **[!UICONTROL Delete]** para eliminar permanentemente el punto de contacto de marketing.

