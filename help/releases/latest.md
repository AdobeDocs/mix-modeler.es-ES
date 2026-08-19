---
title: Ver las notas de la versión actuales de Mix Modeler
description: Últimas notas de la versión de Mix Modeler
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
TQID: https://experienceleague.adobe.com/8o2hpkneIUMbBNEZfw9TsQLaGuPOxqF-XA2TV9cJnqc
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: ca6bcd6f-f5ca-4e5f-a5ae-7dce7177bde9
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
autotag-review: '2026-05-01T09:06:55.437Z'
source-git-commit: 1e6444e672e85d9f3f666bc865d020fb67c45b09
workflow-type: tm+mt
source-wordcount: 524
ht-degree: 6%

---

# Notas de la versión actuales de Mix Modeler

**Última actualización**: 19 de agosto de 2026.

Estas notas de la versión se refieren a la última versión de Mix Modeler. Las versiones de Mix Modeler funcionan con un modelo de entrega continua, que permite una cadencia de versión mensual aproximada. Por lo tanto, estas notas de la versión se actualizan, por lo que debe comprobarlas regularmente.

## Agosto de 2026

| Función | Descripción | [Inicio del despliegue](#release-strategy) | [Disponibilidad general](#release-strategy) |
|---|---|---|---|
| **Filtrar por reglas de conjuntos de datos** | En la configuración de conjuntos de datos armonizados, puede [filtrar reglas de conjuntos de datos en origen, granularidad e inicio de semana](/help/harmonize-data/dataset-rules.md#manage-dataset-rules). | 19 de agosto de 2026 | 19 de agosto de 2026 |
| **Enfoque de canal de medios de pago** | Puede seleccionar [centrarse en la contribución de canal de medios pagados](/help/models/insights.md#contribution-by-channel) en Información del modelo. | 19 de agosto de 2026 | 19 de agosto de 2026 |
| **Configuración del resumen de rendimiento de marketing** | Puede [seleccionar la métrica y cómo se muestra](/help/models/insights.md#marketing-performance-summary) para el resumen de rendimiento de marketing de modelos basados en ingresos en perspectivas de modelos. | 19 de agosto de 2026 | 19 de agosto de 2026 |


## Marzo de 2026

| Función | Descripción | [Inicio del despliegue](#release-strategy) | [Disponibilidad general](#release-strategy) |
|---|---|---|---|
| **Adstock de canal** | Puede incorporar experiencia de dominio, resultados de experimentación o análisis de canal anteriores directamente en la configuración avanzada del modelo a través de [Canal adstock](/help/models/build.md#channel-adstock). Y mostrar [datos de stock de anuncios de canal](/help/models/insights.md#channel-adstock) dentro del análisis de canal de un modelo. | 30 de marzo de 2026 | 30 de marzo de 2026 |

## Febrero de 2026

| Función | Descripción | [Inicio del despliegue](#release-strategy) | [Disponibilidad general](#release-strategy) |
|---|---|---|---|
| **Flujo de trabajo de factores armonizados** | Los factores ahora se administran como parte de un [flujo de trabajo de factores armonizados](/help/harmonize-data/overview.md#factors). Esto simplifica cómo [definir datos de factor](/help/ingest-data/schemas.md#factor-standard-fields-field-group), cómo [administrar factores internos y externos como parte de las reglas del conjunto de datos](/help/harmonize-data/dataset-rules.md#factor-datasets) y cómo usar datos de factor en [modelos](/help/models/build.md#configure). | 25 de febrero de 2026 | 25 de febrero de 2026 |
| **[!UICONTROL Granular incrementality reporting]** | Defina campos armonizados para que pueda explorar en profundidad los informes de su modelo usando [campos de informes de perspectivas granulares](/help/models/build.md#granular-insights-reporting-fields), en lugar de tener que crear modelos separados. | 18 de febrero de 2026 | 18 de febrero de 2026 |

## Enero de 2026

| Función | Descripción | [Inicio del despliegue](#release-strategy) | [Disponibilidad general](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Dataset rules]** | [Se actualizó la tabla de reglas del conjunto de datos](/help/harmonize-data/dataset-rules.md). Puede buscar una o más reglas de conjuntos de datos y ver, editar o eliminar una regla de conjuntos de datos directamente desde la tabla. | 13 de enero de 2026 | 13 de enero de 2026 |
| **[!UICONTROL Current spend]** | Agregue un punto de gasto actual en la [visualización de la curva de respuesta marginal](/help/models/insights.md#marginal-response-curves) en Información del modelo. | 13 de enero de 2026 | 13 de enero de 2026 |
| **[!UICONTROL Sort and resize columns]** | Se ha agregado la ordenación y el cambio de tamaño de las columnas en las tablas [Modelos](/help/models/overview.md) y [Planes](/help/plans/overview.md). | 13 de enero de 2026 | 13 de enero de 2026 |
| **Correcciones** | Correcciones para los siguientes tickets: <ul><li>AMM-3328: entrada de campo deshabilitada para los nuevos operadores por factores</li><li>AMM-3359: Bloqueo del selector de fechas y del cuadro combinado.</li><li>AMM-3441: La duplicación de un plan no rellena automáticamente el intervalo de fechas y el presupuesto.</li></ul> | 13 de enero de 2026 | 13 de enero de 2026 |


## Estrategia de lanzamiento

[!UICONTROL Mix Modeler] usa indicadores de características (también conocidos como &quot;alternadores&quot;) para controlar la visibilidad de las nuevas características, lo que permite realizar pruebas de escala controladas antes del lanzamiento final. Esta estrategia de versión incluye las siguientes fases:

* **Pruebas limitadas**: Una versión por fases comienza con las pruebas realizadas por los usuarios internos de Adobe. A continuación, se pone a disposición de un pequeño grupo de cuentas de cliente para garantizar que la función satisfaga las necesidades y expectativas de los clientes.

* **Inicio del despliegue**: El despliegue de una versión por fases comienza con la fase de prueba limitada. La versión se escalará de 0% a 100% de disponibilidad para los clientes en un par de meses. La implementación por fases se produce en el nivel de organización de Experience Cloud, por lo que todos los usuarios con derecho de una organización reciben la misma experiencia.

