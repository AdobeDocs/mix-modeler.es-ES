---
title: Ver las notas de la versión actuales de Mix Modeler
description: Últimas notas de la versión de Mix Modeler
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
source-git-commit: 1bd08eb1f5e803c7405d11d371127d3db8f309c4
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 5%

---

# Notas de la versión actuales de Mix Modeler

**Última actualización**: 20 de agosto de 2025.

Estas notas de la versión se refieren a la última versión de Mix Modeler. Las versiones de Mix Modeler funcionan con un modelo de entrega continua, que permite una cadencia de versión mensual aproximada. Por lo tanto, estas notas de la versión se actualizan, por lo que debe comprobarlas regularmente.



## De julio a agosto de 2025

| Función | Descripción | [Inicio del despliegue](#release-strategy) | [Disponibilidad general](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Compare plans update]** | La interfaz de usuario de [Comparar planes](/help/plans/compare.md) ahora muestra detalles adicionales para el marketing de pago: ROI o CPA, e ingresos. | 20 de agosto de 2025 | 20 de agosto de 2025 |
| **Actualizaciones de armonización** | Todas las reglas de conjuntos de datos ahora usan un mapa [genérico similar a la experiencia de campos armonizados](/help/harmonize-data/dataset-rules.md), independientemente del tipo de conjunto de datos. Al asignar un campo armonizado estándar desde un conjunto de datos de resumen, Mix Modeler intenta deducir automáticamente el campo del conjunto de datos de Experience Platform correspondiente. | miércoles, 29 de julio de 2025 | miércoles, 29 de julio de 2025 |


## Mayo a junio de 2025

| Función | Descripción | [Inicio del despliegue](#release-strategy) | [Disponibilidad general](#release-strategy) |
|---|---|---|---|
| **Planes basados en objetivos** | Junto a los presupuestos, puedes definir un objetivo (objetivo) al [crear](/help/plans/build.md) o [editar](/help/plans/insights.md#edit-plan) un plan. Algunos ejemplos de métricas de destino son ingresos, conversión, CPA o ROI. | 18 de junio de 2025 | miércoles, 08 de julio de 2025 |
| **Configuración del patrón de gasto** | Cuando crea un plan, ahora tiene la opción de usar los datos de [referencia histórica](/help/plans/build.md) (como datos y perspectivas de gasto de marketing anteriores) al definir el patrón de gasto para cada intervalo de fechas del presupuesto. | 14 de mayo de 2025 | 14 de mayo de 2025 |
| **Configuraciones de plan avanzadas** | Puede definir [configuraciones avanzadas](/help/plans/build.md) para su plan, como el promedio de ingresos por conversión y los costos de canal. | 14 de mayo de 2025 | 14 de mayo de 2025 |

## De marzo a abril de 2025

| Función | Descripción | [Inicio del despliegue](#release-strategy) | [Disponibilidad general](#release-strategy) |
|---|---|---|---|
| **Detección de deriva del modelo** | Cuando abra un modelo, se le pedirá [que vuelva a entrenar el modelo cuando se detecte la deriva del modelo](/help/models/insights.md#model-drift). | 3 de abril de 2025 | 7 de mayo de 2025 |
| **Retorno de canal marginal en las perspectivas del plan** | Se ha agregado una visualización de [retorno de canal marginal](/help/plans/insights.md#marginal-channel-return) a las perspectivas del plan, la cual muestra el evento de salto marginal y el retorno del plan para todos los canales o los seleccionados. | 3 de abril de 2025 | 24 de abril de 2025 |


## Enero-febrero de 2025

| Función | Descripción | [Inicio del despliegue](#release-strategy) | [Disponibilidad general](#release-strategy) |
|---|---|---|---|
| **Condiciones anidadas** | Puede crear condiciones anidadas mediante AND y OR cuando defina una población de datos elegible como parte de la [configuración de un modelo](/help/models/build.md#configure). | 15 de enero de 2025 | 18 de febrero de 2025 |
| **Ver informes** | Puede ver un informe sobre una [conversión](/help/harmonize-data/conversions.md#view-report) o un [punto de contacto de marketing](/help/harmonize-data/marketing-touchpoints.md#view-report) que haya definido como parte de la armonización de datos. | 15 de enero de 2025 | 18 de febrero de 2025 |
| **Eliminar confirmaciones** | Se le pedirá que confirme la eliminación de un [plan](/help/plans/overview.md#delete-plans) o un [modelo](/help/models/overview.md#delete-models). | 15 de enero de 2025 | 18 de febrero de 2025 |
| **Mejora de la interfaz de usuario de factores** | Puede seleccionar los [factores](/help/models/insights.md#factors-beta) que desea mostrar en Información del modelo. | 15 de enero de 2025 | 18 de febrero de 2025 |
| **Tratamiento de errores** | Mensajes de error fáciles de usar y experiencia del usuario mejorada para escenarios de error en la armonización y los planes de datos. | 18 de febrero de 2025 | 18 de febrero de 2025 |
| **Estado del modelo** | Redefinición de [estados de modelo](/help/models/overview.md#manage-models) en el ciclo de vida del modelo. | 18 de febrero de 2025 | 18 de febrero de 2025 |


## Estrategia de lanzamiento

[!UICONTROL Mix Modeler] usa indicadores de características (también conocidos como &quot;alternadores&quot;) para controlar la visibilidad de las nuevas características, lo que permite realizar pruebas de escala controladas antes del lanzamiento final. Esta estrategia de versión incluye las siguientes fases:

* **Pruebas limitadas**: Una versión por fases comienza con las pruebas realizadas por los usuarios internos de Adobe. A continuación, se pone a disposición de un pequeño grupo de cuentas de cliente para garantizar que la función satisfaga las necesidades y expectativas de los clientes.

* **Inicio del despliegue**: El despliegue de una versión por fases comienza con la fase de prueba limitada. La versión se escalará de 0% a 100% de disponibilidad para los clientes en un par de meses. La implementación por fases se produce en el nivel de organización de Experience Cloud, por lo que todos los usuarios con derecho de una organización reciben la misma experiencia.
