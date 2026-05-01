---
title: Administración
description: Obtenga información sobre cómo administrar Mix Modeler.
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
TQID: https://experienceleague.adobe.com/0MxMv6Due-i9-8JxKTb3vk2NDZ5mc6Pj4yEe-liCszg
autotag-review: '2026-05-01T09:07:55.299Z'
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: fe2edbb1-46f9-4347-a27c-577cab3640cb
subfeature_v2: id: abe9e290-7d2f-4131-b71e-ef9900865044id: a6da0571-746e-4d59-89a4-7b691b1c3b9a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12bid: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 7%

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

1. En **[!UICONTROL Details]** dentro de **[!UICONTROL Role]**, agregue **[!UICONTROL Users]** o **[!UICONTROL User groups]** adecuados para proporcionar a los usuarios acceso a Mix Modeler.
