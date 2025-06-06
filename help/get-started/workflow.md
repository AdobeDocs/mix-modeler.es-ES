---
title: Flujo de trabajo de Mix Modeler
description: Descubra el flujo de trabajo típico de Mix Modeler.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: bdb5992ba1e6a4e5aa546b6ffb8e9673ed69be22
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Flujo de trabajo de Mix Modeler

Consulte este vídeo para ver una introducción al flujo de trabajo del usuario en Mix Modeler.

>[!VIDEO](https://video.tv.adobe.com/v/3440206/?learn=on&captions=spa)


Un flujo de trabajo típico de Mix Modeler consta de las siguientes actividades:

![Texto alternativo](/help/assets/ApplicationWorkflow.svg)

|  | Actividad | Descripción |
|---|---|---|
| ![Datos](/help/assets/icons/Data.svg){width="100"} | [**Ingesta de datos**](../ingest-data/overview.md) | Ingesta de datos de evento de Experience Platform (por ejemplo, Adobe Analytics, Web SDK, otras fuentes), datos agregados de canales de marketing (por ejemplo, TV, jardines empotrados, correo electrónico, actividades de propiedad y operadas), datos de factores externos de clientes (por ejemplo, cambios de precios en el servicio de suscripción) y datos de factores internos (por ejemplo, planes de vacaciones). |
| ![Comprobación de datos](/help/assets/icons/DataCheck.svg){width="100"} | [**Armonizar datos**](../harmonize-data/overview.md) | Configure reglas de asignación y reglas de resolución de conflictos para combinar los distintos conjuntos de datos de marketing necesarios para medir y planificar el rendimiento de la campaña en Mix Modeler. |
| ![ArchivoDeConfiguración](/help/assets/icons/FileGear.svg){width="100"} | [**Modelos de compilación**](../models/overview.md) | Cree instancias de modelo con puntos de contacto de marketing (por ejemplo, canales), definiciones de conversión y factores internos y externos. |
| ![DatosDeArchivo](/help/assets/icons/FileData.svg){width="100"} | [**Modelos de entrenamiento y puntuación**](../models/overview.md) | Cree puntuaciones agregadas y de nivel de evento mediante la formación y la puntuación de aprendizaje automático. |
| ![GráficoDeArchivos](/help/assets/icons/FileChart.svg){width="100"} | [**Planes de compilación**](../plans/overview.md) | Crear y generar planes. Determine la mejor asignación de fondos de marketing para lograr un objetivo comercial utilizando los resultados de los modelos de Mix Modeler. |
| ![Tablero](/help/assets/icons/Dashboard.svg){width="100"} | [**Panel de información general**](../dashboard/overview.md) | Obtenga información sobre datos, modelos y planes armonizados mediante varias visualizaciones configurables. |

{style="table-layout:auto"}

A continuación se muestra una descripción general de cómo los datos de entrada pueden fluir a Mix Modeler y cómo Mix Modeler puede producir datos de salida para su propia interfaz, pero también para otras soluciones, como Customer Journey Analytics.

![Flujo de datos de salida de entrada de Mix Modeler](../assets/mm-input-output.png)
<!---
The detailed data-oriented flowchart below illustrates how:

* harmonized data is based on:

  * experience event data (originating from Analytics source connector, collected through Experience Platform SDKs and APIs, ingested through source connectors, or using streaming ingestion),
  * aggregate or summary data from walled gardens (like Facebook, YouTube), traffic sources, or offline advertising data, and 
  * definitions of harmonized fields and dataset rules.

* a model is based on:

  * the conversion and marketing touchpoint definitions resulting from the harmonized data and 
  * non-marketing aggregate or summary data containing internal or external factors.

* mult-touch attribution event scores can potentially be fed back into Experience Platform data lake for use in subsequent model configuration, training and scoring.

![Comprehensive workflow](/help/assets/comprehensive-workflow.svg)

-->
