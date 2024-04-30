---
title: Auditoría
description: Obtenga información sobre cómo auditar al Mix Modeler.
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
source-git-commit: b8435c46276be9d0755049a502ba029b0983cb72
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 6%

---

# Auditoría

>[!AVAILABILITY]
>
>La funcionalidad descrita en este artículo se encuentra en la fase de prueba limitada de la versión y es posible que aún no esté disponible en su entorno. Esta nota se eliminará cuando la funcionalidad esté disponible de forma general. Para obtener información sobre las últimas versiones de Mix Modeler, consulte [Versiones del Mix Modeler](/help/releases/latest.md).

Puede auditar lo que los usuarios están haciendo en Mix Modeler, utilizando la parte Interfaz de auditoría del Experience Platform e incrustada en la interfaz de usuario del Mix Modeler.

Para inspeccionar el registro de auditoría, en la interfaz del Mix Modeler:

1. Seleccionar ![Lista de tareas](../assets/icons/TaskList.svg) **[!UICONTROL Audits]** de **[!UICONTROL PRIVACY]**.

1. Entrada **[!UICONTROL Audits]** puede encontrar la **[!UICONTROL Activity log]**. El registro de actividad mostrará entradas para las siguientes categorías de Mix Modeler, acciones y estados.

   | Categoría | Acción | Estado |
   |---|---|---|
   | Regla de conjunto de datos de Mix Modeler | Crear | Permitir o denegado |
   | Regla de conjunto de datos de Mix Modeler | Actualización | Permitir o denegado |
   | Regla de conjunto de datos de Mix Modeler | Eliminar | Permitir o denegado |
   | Campo de Mix Modeler | Crear | Permitir o denegado |
   | Campo de Mix Modeler | Actualización | Permitir o denegado |
   | Campo de Mix Modeler | Eliminar | Permitir o denegado |
   | Mix Modeler Marketing Touchpoint | Crear | Permitir o denegado |
   | Mix Modeler Marketing Touchpoint | Actualización | Permitir o denegado |
   | Mix Modeler Marketing Touchpoint | Eliminar | Permitir o denegado |
   | Conversión de Mix Modeler | Crear | Permitir o denegado |
   | Conversión de Mix Modeler | Actualización | Permitir o denegado |
   | Conversión de Mix Modeler | Eliminar | Permitir o denegado |
   | Modelo de Mix Modeler | Crear | Permitir o denegado |
   | Modelo de Mix Modeler | Actualización | Permitir o denegado |
   | Modelo de Mix Modeler | Eliminar | Permitir o denegado |

1. Seleccione una entrada en el registro de actividad para abrir un panel y obtener más información.

   ![Auditoría de Mix Modeler](../assets/mix-modeler-audit.png)

1. Para filtrar por **[!UICONTROL Category]**, **[!UICONTROL Action]**, **[!UICONTROL Request ID]**, **[!UICONTROL User]**, **[!UICONTROL Status]** o **[!UICONTROL Date]** rango, seleccione ![Filtrar](../assets/icons/Filter.svg).

1. Para modificar las columnas mostradas en el registro de actividad, seleccione ![Columnas](../assets/icons/ColumnSetting.svg) y en el **[!UICONTROL Customize table]** diálogo seleccione las columnas que desea mostrar. Seleccionar **[!UICONTROL Apply]** para aplicar la selección, **[!UICONTROL Cancel]** para cancelar la selección.

1. Para descargar el registro de auditoría, seleccione ![Descargar](../assets/icons/Download.svg) **[!UICONTROL Download log]**. En el **[!UICONTROL Download log]** diálogo seleccionar **[!UICONTROL CSV]** o **[!UICONTROL JSON]** Seleccione como formato y seleccione **[!UICONTROL Download]**.
