---
title: flujo de trabajo del Mix Modeler
description: Comprender el flujo de trabajo típico de Mix Modeler.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: 512cc28a9fab81438d54e30bb6e20f05da5265d1
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# flujo de trabajo del Mix Modeler

Consulte este vídeo para ver una introducción al flujo de trabajo del usuario en Mix Modeler.

>[!VIDEO](https://video.tv.adobe.com/v/3424854/?learn=on)


Desde un punto de vista funcional, un flujo de trabajo típico en Mix Modeler consta de las siguientes actividades:

![Texto alternativo](../assets/ApplicationWorkflow.svg)

|  | Actividad | Descripción |
|---|---|---|
| ![Datos](../assets/icons/Data.svg){width="100"} | [**Ingesta de datos**](../ingest-data/overview.md) | Ingesta de datos de evento del Experience Platform (por ejemplo, Adobe Analytics, SDK web, otras fuentes), datos agregados de canales de marketing (por ejemplo, TV, jardines empotrados, correo electrónico, actividades propias y operadas), datos de factores externos de clientes (por ejemplo, cambios de precios en el servicio de suscripción) y datos de factores internos (por ejemplo, planes de vacaciones). |
| ![DataCheck](../assets/icons/DataCheck.svg){width="100"} | [**Armonizar datos**](../harmonize-data/overview.md) | Configure reglas de asignación y reglas de resolución de conflictos para combinar los distintos conjuntos de datos de marketing necesarios para medir y planificar el rendimiento de la campaña en Mix Modeler. |
| ![FileConfig](../assets/icons/FileGear.svg){width="100"} | [**Configuración de modelos**](../models/create.md) | Configure instancias de modelo con puntos de contacto de marketing (por ejemplo, canales) y definiciones de conversión. |
| ![FileData](../assets/icons/FileData.svg){width="100"} | [**Modelos de entrenamiento y puntuación**](../models/overview.md) | Cree puntuaciones agregadas y de nivel de evento mediante la formación y la puntuación de aprendizaje automático. |
| ![GráficoDeArchivos](../assets/icons/FileChart.svg){width="100"} | [**Crear planes**](../plans/overview.md) | Determine la mejor asignación de fondos de marketing para lograr un objetivo comercial utilizando los resultados de los modelos de Mix Modeler. |
| ![Panel](../assets/icons/Dashboard.svg){width="100"} | [**Panel de información general**](../dashboard/overview.md) | Obtenga información sobre datos, modelos y planes armonizados mediante varios widgets configurables. |

{style="table-layout:auto"}
