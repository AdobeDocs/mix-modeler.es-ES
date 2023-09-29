---
title: Comparar planes
description: Aprenda a comparar planes en el Modelador de mezcla de Adobe.
source-git-commit: 1eaebc6f6178270a9e8aebb6b250e0b0a6289f52
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 7%

---


# Administración

Utilice el [Adobe Admin Console](https://helpx.adobe.com/es/enterprise/using/admin-console.html) para administrar productos y usuarios de Adobe Mix Modeler.

Para que Adobe Mix Modeler funcione correctamente, debe establecer los permisos correctos.

En la interfaz de usuario de Adobe Experience Cloud,

1. Seleccionar **[!UICONTROL Permissions]** desde el carril izquierdo debajo **[!UICONTROL ADMINISTRATION]**.

1. Seleccionar ![Persona](assets/icons/User.svg) **[!UICONTROL Roles]** en el panel izquierdo.

1. Seleccione una función existente o cree una función con **[!UICONTROL Create role]**. Si seleccionó una función existente, seleccione ![Editar](assets/icons/Edit.svg) **[!UICONTROL Edit]** para editar los permisos de la función. Consulte [Administrar funciones](https://helpx.adobe.com/es/enterprise/using/admin-console.html) para obtener más información.

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
