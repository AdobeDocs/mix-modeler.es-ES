---
title: Administración
description: Aprenda a administrar Mix Modeler.
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
source-git-commit: 4d84c93121fc476cc6610ad572bab161bbacfc23
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---

# Administración

Use [Adobe Admin Console](https://helpx.adobe.com/es/enterprise/using/admin-console.html) para administrar los productos y usuarios de Mix Modeler.

Para que Mix Modeler funcione correctamente, debe establecer los permisos correctos.

En la IU de Adobe Experience Cloud:

1. Seleccione **[!UICONTROL Permissions]** del carril izquierdo, debajo de **[!UICONTROL ADMINISTRATION]**.

1. Seleccione ![Usuario](/help/assets/icons/User.svg) **[!UICONTROL Roles]** del panel izquierdo.

1. Seleccione una función existente o cree una función con **[!UICONTROL Create role]** (por ejemplo, **Mix Modeler**). Si selecciona una función existente, seleccione ![Editar](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** para editar los permisos de la función. Consulte [Administrar funciones](https://helpx.adobe.com/es/enterprise/using/admin-console.html) para obtener más información.

1. Asegúrese de haber seleccionado una o más zonas protegidas para la función.

1. Agregue el recurso **Adobe Mix Modeler** a la lista de recursos para el rol.

1. Asegúrese de seleccionar los permisos de **[!UICONTROL Adobe Mix Modeler]** correctos para la función que está configurando. Puede seleccionar una o varias de las siguientes funciones:

   - **[!UICONTROL View Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL Manage Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL View Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL View Adobe Mix Modeler Plans Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Plans Configuration]**

     ![Mix Modeler RBAC](/help/assets/mix-modeler-rbac.png)


1. Asegúrese de seleccionar permisos adicionales para la función. Por ejemplo, para ver o administrar conjuntos de datos y esquemas, seleccionaría:

   - **[!UICONTROL Data Management]**: seleccione las opciones relevantes: **[!UICONTROL View Datasets]** o **[!UICONTROL Manage Datasets]**.

   - **[!UICONTROL Data Modeling]**: seleccione las opciones relevantes: **[!UICONTROL Manage Schemas]** o **[!UICONTROL View Schemas]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   Seleccione **[!UICONTROL Save]** para guardar los permisos.

1. En **[!UICONTROL Details]** dentro de **[!UICONTROL Role]**, agregue **[!UICONTROL Users]** o **[!UICONTROL User groups]** adecuados para proporcionar a los usuarios acceso al Mix Modeler.
