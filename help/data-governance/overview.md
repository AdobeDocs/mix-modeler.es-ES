---
title: Información general de gobernanza de datos
description: Aprenda a utilizar los servicios y las herramientas de Experience Platform que le permiten controlar los datos de experiencia que recopila. Por lo tanto, usted cumple con sus prácticas comerciales, obligaciones legales y proceso de desarrollo.
feature: Administration
exl-id: 87407c29-e158-48bf-bde9-b3c16a16107e
source-git-commit: 0ee212a626986e4c721d0e58f2528d0ca1a9fdbf
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 1%

---

# Información general de gobernanza de datos

La integración entre Mix Modeler y Experience Platform proporciona a Mix Modeler las funciones para aprovechar las funciones intrínsecas de control de datos de Experience Platform. Esta sección de la documentación detalla los detalles específicos de las funciones de control de datos disponibles en Mix Modeler.

Administración de datos de Experience Platform le permite controlar y comprender los datos a través del recorrido que los datos utilizan en Experience Platform. Este recorrido implica mantener la calidad de los datos, el linaje, la catalogación y mucho más.

Las etiquetas y políticas de uso de datos que se crean en conjuntos de datos consumidos por Experience Platform aparecen en Mix Modeler donde corresponde. Por ejemplo, estas etiquetas detienen o advierten a los usuarios cuando eliminan conjuntos de datos que forman parte de una regla de conjunto de datos en los datos armonizados. También puede ocultar los campos de esquema restringidos para los usuarios al crear una regla de conjunto de datos.

La integración de la gobernanza de datos le permite administrar el cumplimiento de normas de forma más eficiente. Los administradores de datos de su organización pueden establecer políticas para restringir el uso. Como resultado, puede utilizar datos que cumplan con las directivas definidas por los administradores de datos. Lea la documentación de [Etiquetas y directivas](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-dataviews/data-governance) para obtener más información.

Las siguientes funciones de control de datos están disponibles:

| Función | Detalles |
|---|---|
| Controles de acceso | Se admiten el control de acceso basado en roles y el control de acceso basado en atributos (nivel de campo). Consulte [Controles de acceso](access-controls.md) para obtener más información. |
| Registros de auditoría | Cuando los usuarios crean, actualizan o eliminan categorías específicas de Mix Modeler, la funcionalidad Auditoría de Experience Platform registra la actividad en los registros de auditoría. Consulte [Registros de auditoría](audit-logs.md) para obtener más información. |
| Políticas | Como parte del flujo de trabajo de datos armonizado, se aplican las políticas definidas por Experience Platform. Cualquier infracción de las etiquetas de uso de datos se informa y se muestra al usuario. Consulte [Directivas](policies.md) para obtener más información. |
| Cifrado | Todos los conjuntos de datos utilizados para la entrada y salida de modelos siguen las directrices de Experience Platform. El cifrado de datos de Experience Platform se aplica a los datos en reposo y en tránsito. |
| Higiene de datos | Todos los conjuntos de datos utilizados para los modelos de entrada y salida siguen las directrices de Experience Platform. Experience Platform proporciona un conjunto de herramientas para administrar el ciclo vital de los datos del cliente, incluida la compatibilidad con diferentes tipos de caducidad de los datos. Se le notifica cuando elimina un conjunto de datos de origen de Experience Platform, que se utiliza como parte de los datos armonizados. Consulte [Reglas de conjunto de datos](/help/harmonize-data/dataset-rules.md) para obtener más información. |
| Claves gestionadas por el cliente | Cuando tenga licencia de Mix Modeler con el complemento Escudo de seguridad de privacidad o Escudo de atención sanitaria, puede utilizar la capacidad Claves gestionadas por el cliente para aprovechar Azure Key Vault y traer sus propias claves a través de las API. Tiene la administración completa de los datos que se procesan dentro de los modelos en Mix Modeler. |
