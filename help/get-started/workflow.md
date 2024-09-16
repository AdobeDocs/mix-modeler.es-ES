---
title: flujo de trabajo del Mix Modeler
description: Comprender el flujo de trabajo típico de Mix Modeler.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# flujo de trabajo del Mix Modeler

Consulte este vídeo para ver una introducción al flujo de trabajo del usuario en Mix Modeler.

>[!VIDEO](https://video.tv.adobe.com/v/3424854/?learn=on)


Un flujo de trabajo típico de Mix Modeler consta de las siguientes actividades:

![Texto alternativo](/help/assets/ApplicationWorkflow.svg)

|  | Actividad | Descripción |
|---|---|---|
| ![Datos](/help/assets/icons/Data.svg){width="100"} | [**Ingesta de datos**](../ingest-data/overview.md) | Ingesta de datos de evento del Experience Platform (por ejemplo, Adobe Analytics, SDK web, otras fuentes), datos agregados de canales de marketing (por ejemplo, TV, jardines empotrados, correo electrónico, actividades propias y operadas), datos de factores externos de clientes (por ejemplo, cambios de precios en el servicio de suscripción) y datos de factores internos (por ejemplo, planes de vacaciones). |
| ![Comprobación de datos](/help/assets/icons/DataCheck.svg){width="100"} | [**Armonizar datos**](../harmonize-data/overview.md) | Configure reglas de asignación y reglas de resolución de conflictos para combinar los distintos conjuntos de datos de marketing necesarios para medir y planificar el rendimiento de la campaña en Mix Modeler. |
| ![ArchivoDeConfiguración](/help/assets/icons/FileGear.svg){width="100"} | [**Configurar modelos**](../models/create.md) | Configure instancias de modelo con puntos de contacto de marketing (por ejemplo, canales), definiciones de conversión y factores internos y externos. |
| ![DatosDeArchivo](/help/assets/icons/FileData.svg){width="100"} | [**Modelos de entrenamiento y puntuación**](../models/overview.md) | Cree puntuaciones agregadas y de nivel de evento mediante la formación y la puntuación de aprendizaje automático. |
| ![GráficoDeArchivos](/help/assets/icons/FileChart.svg){width="100"} | [**Crear planes**](../plans/overview.md) | Determine la mejor asignación de fondos de marketing para lograr un objetivo comercial utilizando los resultados de los modelos de Mix Modeler. |
| ![Tablero](/help/assets/icons/Dashboard.svg){width="100"} | [**Panel de información general**](../dashboard/overview.md) | Obtenga información sobre datos, modelos y planes armonizados mediante varias visualizaciones configurables. |

{style="table-layout:auto"}

El diagrama de flujo detallado orientado a los datos que aparece a continuación ilustra cómo:

* los datos armonizados se basan en:

   * datos de evento de experiencia (procedentes del conector de origen de Analytics, recopilados mediante SDK y API de Experience Platform, introducidos mediante conectores de origen o utilizando la introducción de flujo continuo),
   * datos agregados o resumidos de los jardines amurallados (como Facebook, YouTube), fuentes de tráfico o datos de publicidad sin conexión, y
   * definiciones de campos armonizados y reglas de conjuntos de datos.

* un modelo se basa en:

   * las definiciones de los puntos de contacto de conversión y marketing resultantes de los datos armonizados y
   * datos acumulados o resumidos no relacionados con la comercialización que contengan factores internos o externos.

* las puntuaciones de eventos de atribución de contacto múltiple se pueden devolver al lago de datos del Experience Platform para su uso en la configuración, el aprendizaje y la puntuación de modelos posteriores.

![Flujo de trabajo completo](/help/assets/comprehensive-workflow.svg)
