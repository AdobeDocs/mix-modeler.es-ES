---
title: Controles de acceso
description: Obtenga información sobre cómo configurar los controles de acceso en Mix Modeler.
feature: Administration
exl-id: c9ec97d9-b9a2-41f5-8626-1cf967d5d7fe
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 1%

---

# Controles de acceso

El control de acceso para el Mix Modeler se proporciona a través del Experience Platform en [Adobe Admin Console](https://adminconsole.adobe.com/) y de [Permisos](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#platform-permissions) en el Experience Platform. Esta funcionalidad aprovecha los perfiles de producto en el Admin Console, que vinculan a los usuarios con permisos y entornos limitados.

Para obtener más información sobre el control de acceso, vea [Información general sobre el control de acceso](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home).

## Control de acceso basado en roles

Consulte [Administración](../main-guide/administration.md) sobre cómo configurar permisos de acceso basados en roles para usuarios Mix Modeler y grupos de usuarios en Experience Platform.

## Control de acceso basado en atributos

[El control de acceso basado en atributos](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) es una capacidad de Experience Platform que permite a los administradores controlar el acceso a objetos específicos o a funcionalidades basadas en atributos. Los atributos pueden ser metadatos añadidos a un objeto, como una etiqueta añadida a un campo o segmento de esquema. Un administrador define directivas de acceso que incluyen atributos para administrar permisos de acceso de usuarios.

Esta funcionalidad le permite etiquetar campos de esquema del Modelo de datos de experiencia (XDM) con etiquetas que definen ámbitos organizativos o de uso de datos. En paralelo, los administradores pueden utilizar la interfaz de administración de usuarios y funciones para definir directivas de acceso en los campos de esquema XDM. Y administrar mejor el acceso dado a usuarios o grupos de usuarios (usuarios internos, externos o de terceros). Además, el control de acceso basado en atributos permite a los administradores gestionar el acceso a segmentos específicos.

Mediante el control de acceso basado en atributos, los administradores pueden controlar el acceso de los usuarios a los datos personales confidenciales (SPD) y a la información de identificación personal (PII) en todos los flujos de trabajo y recursos de la plataforma. Los administradores pueden definir funciones de usuario que solo tengan acceso a campos y datos específicos que correspondan a esos campos.

Al configurar reglas de conjuntos de datos para conjuntos de datos armonizados, el control de acceso [basado en atributos](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) de Experience Platform se aplica en el nivel de campo. Un campo está restringido cuando se adjunta una etiqueta a un campo de esquema. Y se habilita una directiva activa que deniega el acceso al campo. Como resultado:

* no ve los campos de esquema que están restringidos al crear una regla de conjunto de datos,
* no puede ver ni editar la asignación de uno o varios campos de esquema que están restringidos. Cuando edita o ve una regla del conjunto de datos que contiene estos campos restringidos, verá la siguiente pantalla.
  ![Acción no permitida](/help/assets/action-not-permitted.png)
