---
title: Registros de auditoría
description: Obtenga información sobre cómo acceder a los registros de auditoría desde Mix Modeler.
feature: Administration
exl-id: aa65aac5-bea4-43ff-b0d0-9e8a6a97d3ca
source-git-commit: 1a9df9f9819d9e0031e58443ec6a9e755a151ba0
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 5%

---

# Registros de auditoría

Para aumentar la transparencia y la visibilidad de las actividades realizadas en el sistema, la actividad del usuario dentro del flujo de trabajo de Mix Modeler se captura en los registros de auditoría de Experience Platform para comprender cualquier cambio impulsado por el usuario en las categorías de Mix Modeler. Estos registros forman una pista de auditoría que puede ayudar con la resolución de problemas y pueden ayudar a su empresa a cumplir de forma eficaz con las políticas de administración de datos corporativos y los requisitos regulatorios.

<!-- DO WE HAVE TO ADD THIS
If you are subject to the Health Insurance Portability and Accountability Act (HIPAA) and create, receive, maintain, or transmit permitted sensitive personal data through Mix Modeler, you are responsible for executing a BAA with Adobe and licensing Healthcare Shield.
-->

Un registro de auditoría informa de quién realizó qué acción y cuándo lo hizo. Cada acción registrada contiene metadatos que indican el tipo de acción, la fecha y la hora, el ID de correo electrónico del usuario que realizó la acción y los atributos adicionales relevantes de ese tipo de acción. Rastrea las acciones de creación, actualización y eliminación realizadas por los usuarios en Mix Modeler.

Para inspeccionar el registro de auditoría, en la interfaz de Mix Modeler:

1. Seleccione ![Lista de tareas](/help/assets/icons/TaskList.svg) **[!UICONTROL Audits]** de **[!UICONTROL PRIVACY]**.

1. En **[!UICONTROL Audits]**, puede encontrar **[!UICONTROL Activity log]**. El registro de actividad muestra las entradas de las siguientes categorías, acciones y estados de Mix Modeler.

   | Categoría | Acción | Estado |
   |---|---|---|
   | Regla de conjunto de datos Mix Modeler | Crear | Permitir o denegar |
   | Regla de conjunto de datos Mix Modeler | Actualización | Permitir o denegar |
   | Regla de conjunto de datos Mix Modeler | Eliminar | Permitir o denegar |
   | Campo de Mix Modeler | Crear | Permitir o denegar |
   | Campo de Mix Modeler | Actualización | Permitir o denegar |
   | Campo de Mix Modeler | Eliminar | Permitir o denegar |
   | Mix Modeler Marketing Touchpoint | Crear | Permitir o denegar |
   | Mix Modeler Marketing Touchpoint | Actualización | Permitir o denegar |
   | Mix Modeler Marketing Touchpoint | Eliminar | Permitir o denegar |
   | Conversión de Mix Modeler | Crear | Permitir o denegar |
   | Conversión de Mix Modeler | Actualización | Permitir o denegar |
   | Conversión de Mix Modeler | Eliminar | Permitir o denegar |
   | Modelo Mix Modeler | Crear | Permitir o denegar |
   | Modelo Mix Modeler | Actualización | Permitir o denegar |
   | Modelo Mix Modeler | Eliminar | Permitir o denegar |
   | Modelo Mix Modeler | Rescore | Permitir o denegar |
   | Modelo Mix Modeler | Clonar | Permitir o denegar |
   | Modelo Mix Modeler | Tren/reciclaje | Permitir o denegar |
   | Modelo Mix Modeler | Descargar o guardar metadatos | Permitir o denegar |
   | Plan de Mix Modeler | Crear | Permitir o denegar |
   | Plan de Mix Modeler | Actualización | Permitir o denegar |
   | Plan de Mix Modeler | Cambiar modelo asociado | Permitir o denegar |
   | Armonización de datos de Mix Modeler | Sincronización de déclencheur | Permitir o denegar |


1. Seleccione una entrada en el registro de actividad para abrir un panel y obtener más información.

   ![Auditoría de Mix Modeler](/help/assets/mix-modeler-audit.png)

1. Para filtrar por el rango **[!UICONTROL Category]**, **[!UICONTROL Action]**, **[!UICONTROL Request ID]**, **[!UICONTROL User]**, **[!UICONTROL Status]** o **[!UICONTROL Date]**, seleccione ![Filtro](/help/assets/icons/Filter.svg).

1. Para modificar las columnas mostradas en el registro de actividad, seleccione ![Columnas](/help/assets/icons/ColumnSetting.svg) y, en el cuadro de diálogo **[!UICONTROL Customize table]**, seleccione las columnas que desea mostrar. Seleccione **[!UICONTROL Apply]** para aplicar la selección, **[!UICONTROL Cancel]** para cancelar la selección.

1. Para descargar el registro de auditoría, seleccione ![Descargar](/help/assets/icons/Download.svg) **[!UICONTROL Download log]**. En el cuadro de diálogo **[!UICONTROL Download log]**, seleccione **[!UICONTROL CSV]** o **[!UICONTROL JSON]** como formato y seleccione **[!UICONTROL Download]**.

## Acceso a los registros de auditoría

Cuando la función está habilitada para su organización, los registros de auditoría se recopilan automáticamente a medida que se produce la actividad. No es necesario habilitar manualmente la recopilación de registros de auditoría.

Para ver y exportar los registros de auditoría, se debe contar con el permiso de control Acceso a registros de auditoría. Para obtener información sobre cómo administrar los permisos individuales para las características de Mix Modeler, consulte la [documentación de control de acceso](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home).
