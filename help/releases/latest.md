---
title: Ver las notas de la versión actuales de Mix Modeler
description: Últimas notas de la versión de Mix Modeler
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
source-git-commit: 0a5fdbe90c4a32de45f4f2756f080dc265f5fbb7
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 8%

---

# Notas de la versión actuales de Mix Modeler

**Última actualización**: 26 de febrero de 2026.

Estas notas de la versión se refieren a la última versión de Mix Modeler. Las versiones de Mix Modeler funcionan con un modelo de entrega continua, que permite una cadencia de versión mensual aproximada. Por lo tanto, estas notas de la versión se actualizan, por lo que debe comprobarlas regularmente.


## Febrero de 2026

| Función | Descripción | [Inicio del despliegue](#release-strategy) | [Disponibilidad general](#release-strategy) |
|---|---|---|---|
| **Flujo de trabajo de factores armonizados** | Los factores ahora se administran como parte de un [flujo de trabajo de factores armonizados](/help/harmonize-data/overview.md#factors). Esto simplifica cómo [definir datos de factor](/help/ingest-data/schemas.md#factor-standard-fields-field-group), cómo [administrar factores internos y externos como parte de las reglas del conjunto de datos](/help/harmonize-data/dataset-rules.md#factor-datasets) y cómo usar datos de factor en [modelos](/help/models/build.md#configure). | jueves, 25 de febrero de 2026 | jueves, 25 de febrero de 2026 |
| **[!UICONTROL Granular incrementality reporting]** | Defina campos armonizados para que pueda explorar en profundidad los informes de su modelo usando [campos de informes de perspectivas granulares](/help/models/build.md#granular-insights-reporting-fields), en lugar de tener que crear modelos separados. | jueves, 18 de febrero de 2026 | jueves, 18 de febrero de 2026 |

## Enero de 2026

| Función | Descripción | [Inicio del despliegue](#release-strategy) | [Disponibilidad general](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Dataset rules]** | [Se actualizó la tabla de reglas del conjunto de datos](/help/harmonize-data/dataset-rules.md). Puede buscar una o más reglas de conjuntos de datos y ver, editar o eliminar una regla de conjuntos de datos directamente desde la tabla. | miércoles, 13 de enero de 2026 | miércoles, 13 de enero de 2026 |
| **[!UICONTROL Current spend]** | Agregue un punto de gasto actual en la [visualización de la curva de respuesta marginal](/help/models/insights.md#marginal-response-curves) en Información del modelo. | miércoles, 13 de enero de 2026 | miércoles, 13 de enero de 2026 |
| **[!UICONTROL Sort and resize columns]** | Se ha agregado la ordenación y el cambio de tamaño de las columnas en las tablas [Modelos](/help/models/overview.md) y [Planes](/help/plans/overview.md). | miércoles, 13 de enero de 2026 | miércoles, 13 de enero de 2026 |
| **Correcciones** | Correcciones para los siguientes tickets: <ul><li>AMM-3328: entrada de campo deshabilitada para los nuevos operadores por factores</li><li>AMM-3359: Bloqueo del selector de fechas y del cuadro combinado.</li><li>AMM-3441: La duplicación de un plan no rellena automáticamente el intervalo de fechas y el presupuesto.</li></ul> | miércoles, 13 de enero de 2026 | miércoles, 13 de enero de 2026 |


## Estrategia de lanzamiento

[!UICONTROL Mix Modeler] usa indicadores de características (también conocidos como &quot;alternadores&quot;) para controlar la visibilidad de las nuevas características, lo que permite realizar pruebas de escala controladas antes del lanzamiento final. Esta estrategia de versión incluye las siguientes fases:

* **Pruebas limitadas**: Una versión por fases comienza con las pruebas realizadas por los usuarios internos de Adobe. A continuación, se pone a disposición de un pequeño grupo de cuentas de cliente para garantizar que la función satisfaga las necesidades y expectativas de los clientes.

* **Inicio del despliegue**: El despliegue de una versión por fases comienza con la fase de prueba limitada. La versión se escalará de 0% a 100% de disponibilidad para los clientes en un par de meses. La implementación por fases se produce en el nivel de organización de Experience Cloud, por lo que todos los usuarios con derecho de una organización reciben la misma experiencia.
