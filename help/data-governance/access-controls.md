---
title: Controles de acceso
description: Obtenga información sobre cómo configurar los controles de acceso en Mix Modeler.
feature: Administration
exl-id: c9ec97d9-b9a2-41f5-8626-1cf967d5d7fe
TQID: https://experienceleague.adobe.com/EoiF5ui2Bqq0Oxuv-s5E5pQclj9gnjoKgZ1bOzRK-vY
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: fe2edbb1-46f9-4347-a27c-577cab3640cb
subfeature_v2:
  - id: abe9e290-7d2f-4131-b71e-ef9900865044
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
autotag-review: '2026-05-01T09:20:37.287Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 1%

---

# Controles de acceso

El control de acceso para Mix Modeler se proporciona a través de Experience Platform en [Adobe Admin Console](https://adminconsole.adobe.com/) y de [Permisos](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#platform-permissions) en Experience Platform. Esta funcionalidad aprovecha los perfiles de producto en Admin Console, que vinculan a los usuarios con permisos y entornos limitados.

Para obtener más información sobre el control de acceso, vea [Información general sobre el control de acceso](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home).

## Control de acceso basado en roles

Consulte [Administración](../main-guide/administration.md) sobre cómo configurar permisos de acceso basados en roles para usuarios y grupos de usuarios de Mix Modeler en Experience Platform.

## Control de acceso basado en atributos

[El control de acceso basado en atributos](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) es una funcionalidad de Experience Platform que permite a los administradores controlar el acceso a objetos específicos o a funcionalidades basadas en atributos. Los atributos pueden ser metadatos añadidos a un objeto, como una etiqueta añadida a un campo o segmento de esquema. Un administrador define directivas de acceso que incluyen atributos para administrar permisos de acceso de usuarios.

Esta funcionalidad le permite etiquetar campos de esquema del Modelo de datos de experiencia (XDM) con etiquetas que definen ámbitos organizativos o de uso de datos. En paralelo, los administradores pueden utilizar la interfaz de administración de usuarios y funciones para definir directivas de acceso en los campos de esquema XDM. Y administrar mejor el acceso dado a usuarios o grupos de usuarios (usuarios internos, externos o de terceros). Además, el control de acceso basado en atributos permite a los administradores gestionar el acceso a segmentos específicos.

Mediante el control de acceso basado en atributos, los administradores pueden controlar el acceso de los usuarios a los datos personales confidenciales (SPD) y a la información de identificación personal (PII) en todos los flujos de trabajo y recursos de la plataforma. Los administradores pueden definir funciones de usuario que solo tengan acceso a campos y datos específicos que correspondan a esos campos.

Al configurar reglas de conjuntos de datos para conjuntos de datos armonizados, el control de acceso [basado en atributos](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) de Experience Platform se aplica en el nivel de campo. Un campo está restringido cuando se adjunta una etiqueta a un campo de esquema. Y se habilita una directiva activa que deniega el acceso al campo. Como resultado:

* no ve los campos de esquema que están restringidos al crear una regla de conjunto de datos,
* no puede ver ni editar la asignación de uno o varios campos de esquema que están restringidos. Cuando edita o ve una regla del conjunto de datos que contiene estos campos restringidos, verá la siguiente pantalla.
  ![Acción no permitida](/help/assets/action-not-permitted.png)
