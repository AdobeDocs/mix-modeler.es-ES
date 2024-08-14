---
title: Políticas
description: Obtenga información sobre cómo acceder a las directivas desde Mix Modeler.
feature: Administration
exl-id: 4dba7c30-ad1e-4213-a2b0-afc55f2448a3
source-git-commit: 132dc18b84723358a7d65e2aaadd49cf1deb2dd8
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 1%

---

# Políticas

Una vez que revise el flujo de trabajo para crear un modelo y enviar su configuración, [aplicación de políticas](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/enforcement/overview#automatic-enforcement) comprueba si hay alguna infracción. Si se produce una infracción de directiva, aparece una ventana emergente que indica que se han infringido una o más directivas. Esta comprobación sirve para garantizar que las operaciones de datos y las acciones de marketing de Experience Platform cumplan con las políticas de uso de datos.

De forma predeterminada, el Mix Modeler comprueba las infracciones de las directivas definidas de Adobe asociadas a las siguientes etiquetas y acciones de marketing:

| Nombre de política | Etiqueta asociada | Acción de marketing asociada |
|---|---|---|
| Restringir el análisis de uso y la medición basada en usuarios | C8 | Analytics |
| Restringir la ciencia de datos | C9 | Ciencia de datos |
| Restringir la exportación de datos | C12 | Exportación de datos |

Las infracciones también se comprueban en busca de las directivas que ha definido usted mismo y que no contienen ninguna acción de marketing enumerada en la tabla anterior.

Cuando infringe una directiva al crear una regla de conjunto de datos, ve una ventana emergente que muestra información sobre la infracción de directiva.

Por ejemplo:

- ha habilitado la directiva [!UICONTROL Restrict data science] con la etiqueta asociada [!UICONTROL C9] y la acción de marketing asociada [!UICONTROL Data Science],
- ha aplicado la etiqueta [!UICONTROL C9] - [!UICONTROL No data science] al campo `totalCost` en el esquema de datos de conversión,
- desea configurar una regla del conjunto de datos que, entre otras cosas, asigne el campo `totalCost` del esquema de datos de conversión al campo armonizado con el nombre `spend` (y el nombre para mostrar `Spend`).

Cuando desee guardar la regla del conjunto de datos, verá una ventana emergente de **[!UICONTROL Data governance policy violation detected]** que muestra una lista de directivas infringidas. Cuando selecciona el nombre de la directiva, en [!UICONTROL Violation summary], ve una lista de [!UICONTROL Active data governance labels], que contiene [!UICONTROL Entity], [!UICONTROL Type], [!UICONTROL Field] y [!UICONTROL Government labels] aplicados.

<!-- pending screenshot -->

Al aplicar una etiqueta de uso de datos a un campo de esquema que ya se utiliza en datos armonizados, aparece una ventana emergente que muestra información sobre la infracción de directiva.

Por ejemplo:

- ha configurado una regla del conjunto de datos que, entre otras cosas, asigna el campo `totalCost` del esquema de datos de conversión al campo armonizado con el nombre `spend` (y el nombre para mostrar `Spend`).
- ha sincronizado los datos armonizados correctamente al menos una vez (consulte [Reglas del conjunto de datos: sincronizar datos](/help/harmonize-data/dataset-rules.md#sync-data)).
- habilita la directiva [!UICONTROL Restrict data science] con la etiqueta asociada [!UICONTROL C9] y la acción de marketing asociada [!UICONTROL Data Science],
- desea aplicar la etiqueta [!UICONTROL C9] - [!UICONTROL No data science] al campo `totalCost` en el esquema de datos de conversión.

Cuando quiera guardar la actualización del esquema, verá una ventana emergente de **[!UICONTROL Data governance policy violation detected]** que muestra una lista de directivas infringidas. Seleccione el nombre de la directiva en [!UICONTROL Violation summary] para obtener más detalles en la lista [!UICONTROL Data Lineage].

<!-- pending screenshot -->

## Infracción detectada en fuentes

La infracción de directiva de gobernanza de datos detectada proporciona información específica sobre la infracción. Puede resolver estas infracciones mediante la configuración de directivas y otras medidas que no estén directamente relacionadas con el flujo de trabajo de configuración. Por ejemplo, puede cambiar las etiquetas para que determinados campos puedan utilizarse con fines de ciencia de datos. Como alternativa, también puede modificar la configuración del modelo en sí, de modo que el modelo no utilice un objeto con una etiqueta de uso de datos.

La selección de ![Privacidad](/help/assets/icons/Privacy.svg) **[!UICONTROL Policies]** en el carril izquierdo proporciona acceso a la interfaz de [!UICONTROL Policies] del Experience Platform, lo que permite administrar sus directivas, etiquetas y acciones de marketing.

<!--
Currently,  Mix Modeler does not support all of the data governance functionality offered by Experience Platform. Field level access control is supported. See [Field level access control](../harmonize-data/dataset-rules.md#field-level-access-control)
-->

>[!MORELIKETHIS]
>
>[Información general sobre políticas de uso de datos](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/policies/overview)
>
>

