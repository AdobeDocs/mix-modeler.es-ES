---
title: Ver las notas de la versión actuales de Mix Modeler
description: Últimas notas de la versión de Mix Modeler
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
source-git-commit: f4755b5b83c50c1a0c63839854954154d0b141c1
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 4%

---

# Notas de la versión actuales de Mix Modeler

**Última actualización**: 13 de enero de 2026.

Estas notas de la versión se refieren a la última versión de Mix Modeler. Las versiones de Mix Modeler funcionan con un modelo de entrega continua, que permite una cadencia de versión mensual aproximada. Por lo tanto, estas notas de la versión se actualizan, por lo que debe comprobarlas regularmente.



## Enero de 2026

| Función | Descripción | [Inicio del despliegue](#release-strategy) | [Disponibilidad general](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Dataset rules]** | Se ha actualizado la tabla de reglas del conjunto de datos. Puede buscar una o más reglas de conjuntos de datos y ver, editar o eliminar una regla de conjuntos de datos directamente desde la tabla. | 13 de enero de 2026 | 13 de enero de 2026 |
| **[!UICONTROL Current spend]** | Agregue un punto de gasto actual en la [visualización de la curva de respuesta marginal](/help/models/insights.md#marginal-response-curves) en Información del modelo. | 13 de enero de 2026 | 13 de enero de 2026 |
| **[!UICONTROL Sort and resize columns]** | Se ha agregado la ordenación y el cambio de tamaño de las columnas en las tablas [Modelos](/help/models/overview.md) y [Planes](/help/plans/overview.md). | 13 de enero de 2026 | 13 de enero de 2026 |
| **Correcciones** | Correcciones para los siguientes tickets: <ul><li>AMM-3328: entrada de campo deshabilitada para los nuevos operadores por factores</li><li>AMM-3359: Bloqueo del selector de fechas y del cuadro combinado.</li><li>AMM-3441: La duplicación de un plan no rellena automáticamente el intervalo de fechas y el presupuesto.</li></ul> | 13 de enero de 2026 | 13 de enero de 2026 |


## Estrategia de lanzamiento

[!UICONTROL Mix Modeler] usa indicadores de características (también conocidos como &quot;alternadores&quot;) para controlar la visibilidad de las nuevas características, lo que permite realizar pruebas de escala controladas antes del lanzamiento final. Esta estrategia de versión incluye las siguientes fases:

* **Pruebas limitadas**: Una versión por fases comienza con las pruebas realizadas por los usuarios internos de Adobe. A continuación, se pone a disposición de un pequeño grupo de cuentas de cliente para garantizar que la función satisfaga las necesidades y expectativas de los clientes.

* **Inicio del despliegue**: El despliegue de una versión por fases comienza con la fase de prueba limitada. La versión se escalará de 0% a 100% de disponibilidad para los clientes en un par de meses. La implementación por fases se produce en el nivel de organización de Experience Cloud, por lo que todos los usuarios con derecho de una organización reciben la misma experiencia.
