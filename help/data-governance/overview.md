---
title: Gobernanza de datos
description: Aprenda a utilizar los servicios y las herramientas de Experience Platform que le permiten controlar los datos de experiencia recopilados. Por lo tanto, usted cumple con sus prácticas comerciales, obligaciones legales y proceso de desarrollo.
feature: Administration
source-git-commit: 6776a91563f120db1341adef923aab4b0f582c9d
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 2%

---

# Gobernanza de datos

La integración entre Mix Modeler y Experience Platform ofrece al Mix Modeler las funciones para aprovechar las funciones intrínsecas de control de datos de Experience Platform. Esta sección de la documentación detalla los detalles específicos de las funciones de control de datos disponibles en Mix Modeler.

Administración de datos de Experience Platform le permite controlar y comprender los datos a través del recorrido que los datos utilizan para Experience Platform. Este recorrido implica mantener la calidad de los datos, el linaje, la catalogación y mucho más.

Las etiquetas y políticas de uso de datos que se crean en conjuntos de datos consumidos por el Experience Platform aparecen en el Mix Modeler cuando corresponde. Por ejemplo, estas etiquetas detienen o advierten a los usuarios cuando eliminan conjuntos de datos que forman parte de una regla de conjunto de datos en los datos armonizados. También puede ocultar los campos de esquema restringidos para los usuarios al crear una regla de conjunto de datos.

La integración de la gobernanza de datos le permite administrar el cumplimiento de normas de forma más eficiente. Los administradores de datos de su organización pueden establecer políticas para restringir el uso. Como resultado, puede utilizar datos que cumplan con las directivas definidas por los administradores de datos. Lea la documentación de [Etiquetas y directivas](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-governance) para obtener más información.

Las siguientes funciones de control de datos están disponibles:

| Función | Detalles |
|---|---|
| Controles de acceso | Se admiten el control de acceso basado en roles y el control de acceso basado en atributos (nivel de campo). Consulte [Controles de acceso](access-controls.md) para obtener más información. |
| Registros de auditoría | Cuando los usuarios crean, actualizan o eliminan categorías de Mix Modeler específicas, la funcionalidad Auditoría de Experience Platform registra la actividad en los registros de auditoría. Consulte [Registros de auditoría](audit-logs.md) para obtener más información. |
| Políticas | Como parte del flujo de trabajo de datos armonizado, se aplican las políticas definidas por el Experience Platform. Cualquier infracción de las etiquetas de uso de datos se informa y se muestra al usuario. Consulte [Directivas](policies.md) para obtener más información. |
| Cifrado | Todos los conjuntos de datos utilizados para la entrada y salida de modelos siguen las directrices del Experience Platform. El cifrado de datos Experience Platform se aplica a los datos en reposo y en tránsito. |
| Higiene de datos | Todos los conjuntos de datos utilizados para los modelos de entrada y salida siguen las directrices del Experience Platform. Experience Platform proporciona un conjunto de herramientas para administrar el ciclo vital de los datos del cliente, incluida la compatibilidad con diferentes tipos de caducidad de los datos. Cuando se elimina un conjunto de datos de origen de Experience Platform, que se utiliza como parte de los datos armonizados, se le notifica. Consulte [Reglas de conjunto de datos](/help/harmonize-data/dataset-rules.md) para obtener más información. |
| Claves gestionadas por el cliente | Cuando tenga un Mix Modeler con licencia con el complemento Escudo de seguridad de privacidad o Escudo de atención sanitaria, puede utilizar la capacidad Claves gestionadas por el cliente para aprovechar Azure Key Vault y traer sus propias claves a través de las API. Tiene una administración completa de los datos que se procesan dentro de los modelos en Mix Modeler. |
