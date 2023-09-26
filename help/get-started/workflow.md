---
title: Flujo de trabajo del Modelador Adobe Mix
description: Comprenda el flujo de trabajo típico del Modelador de mezcla de Adobe.
feature: Datasets, Event Datasets, Plans, Harmonized Data, Models
source-git-commit: ac17f5a9fcf036c8e689879578e4b745b789cea3
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Flujo de trabajo del Modelador Adobe Mix

Un flujo de trabajo típico en el Modelador de mezcla de Adobe tiene este aspecto:

![Texto alternativo](../assets/ApplicationWorkflow.svg)

|  | Actividad | Descripción |
|---|---|---|
| ![Datos](../assets/icons/Data.svg){width="100"} | [**Ingesta de datos**](../ingest-data/overview.md) | Ingesta de datos de evento de Adobe Experience Platform (por ejemplo, Adobe Analytics, SDK web, otras fuentes), datos agregados de canales de marketing (por ejemplo, TV, jardines empotrados, correo electrónico, actividades propias y operadas) y datos de factores externos de clientes (por ejemplo, cambios de precio en el servicio de suscripción). |
| ![DataCheck](../assets/icons/DataCheck.svg){width="100"} | [**Armonizar datos**](../harmonize-data/overview.md) | Configure las reglas de asignación y las reglas de resolución de conflictos para combinar los distintos conjuntos de datos de marketing necesarios para medir y planificar el rendimiento de la campaña en el Modelador de mezcla de Adobes. |
| ![FileConfig](../assets/icons/FileGear.svg){width="100"} | [**Configuración de modelos**](../models/create.md) | Configure instancias de modelo con puntos de contacto de marketing (por ejemplo, canales) y definiciones de conversión. |
| ![FileData](../assets/icons/FileData.svg){width="100"} | [**Modelos de entrenamiento y puntuación**](../models/overview.md) | Cree puntuaciones agregadas y de nivel de evento mediante la formación y la puntuación de aprendizaje automático. |
| ![GráficoDeArchivos](../assets/icons/FileChart.svg){width="100"} | [**Crear planes**](../plans/overview.md) | Determine la mejor asignación de fondos de marketing para lograr un objetivo comercial utilizando la salida de los modelos de Adobe Mix Modeler. |
| ![Panel](../assets/icons/Dashboard.svg){width="100"} | [**Panel de información general**](../dashboard/overview.md) | Obtenga información sobre datos, modelos y planes armonizados mediante varios widgets configurables. |

{style="table-layout:auto"}

