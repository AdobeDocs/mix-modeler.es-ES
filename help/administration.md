---
title: Administración
description: Aprenda a administrar Adobe Mix Modeler.
source-git-commit: 4a6cbda1ff0a779ebf8a38a4de3f797ed9e54b00
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 8%

---


# Administración

Utilice el [Adobe Admin Console](https://helpx.adobe.com/es/enterprise/using/admin-console.html) para administrar productos y usuarios de Adobe Mix Modeler.

Para que Adobe Mix Modeler funcione correctamente, debe establecer los permisos correctos.

En la interfaz de usuario de Adobe Experience Cloud,

1. Seleccionar **[!UICONTROL Permissions]** desde el carril izquierdo, debajo de **[!UICONTROL ADMINISTRATION]**.

1. Seleccionar ![Persona](assets/icons/User.svg) **[!UICONTROL Roles]** en el panel izquierdo.

1. Seleccione una función existente o cree una función con **[!UICONTROL Create role]**. Si selecciona una función existente, seleccione ![Editar](assets/icons/Edit.svg) **[!UICONTROL Edit]** para editar los permisos de la función. Consulte [Administrar funciones](https://helpx.adobe.com/es/enterprise/using/admin-console.html) para obtener más información.

1. Asegúrese de seleccionar los siguientes permisos para la función:

   * **[!UICONTROL Sandboxes]**: seleccione al menos una zona protegida.

   * **[!UICONTROL Data Management]**: asegúrese de seleccionar las opciones **[!UICONTROL View Datasets]** y **[!UICONTROL Manage Datasets]**.

   * **[!UICONTROL Data Modeling]**: asegúrese de seleccionar las opciones **[!UICONTROL Manage Schemas]** y **[!UICONTROL View Schemas]**.

   * **[!UICONTROL Destinations]**: asegúrese de seleccionar **[!UICONTROL Manage and Activate Dataset Destination]**, **[!UICONTROL Destination Authoring]**, **[!UICONTROL Activate Destinations]** y **[!UICONTROL View Destinations]**.

   * **[!UICONTROL Data Ingestion]**: asegúrese de seleccionar **[!UICONTROL View Sources]** y **[!UICONTROL Manage Sources]**.

   Los permisos configurados para la función deben tener el siguiente aspecto:

   ![Permisos](assets/permissions.png)

   Seleccionar **[!UICONTROL Save]** para guardar los permisos.

1. Entrada **[!UICONTROL Details]** dentro **[!UICONTROL Role]**, añada el adecuado **[!UICONTROL Users]** y/o **[!UICONTROL User groups]** para proporcionar a los usuarios acceso a Adobe Mix Modeler.
