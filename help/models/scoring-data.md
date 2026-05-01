---
title: Usar datos de puntuación
description: Descubra cómo se mantienen los datos de puntuación de un modelo en Mix Modeler.
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
TQID: https://experienceleague.adobe.com/6eMg5Azsb-rdyG5g-hIkiyJrVbgOOul5V-0TvxzCTyo
autotag-review: '2026-05-01T08:58:54.964Z'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: f40f1683-8300-4054-aab8-77da06ad63ff
subfeature_v2:
  - id: cb40363e-1205-4921-971c-9ee6bdb18329
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 684
ht-degree: 11%

---

# Usar datos de puntuación

Como parte de la puntuación de un modelo, los datos de puntuación se conservan dentro de un conjunto de datos en Experience Platform. Cuando se ha habilitado la atribución de múltiples contactos durante la creación del modelo, se conservan datos de puntuación de evento adicionales dentro de un conjunto de datos en Experience Platform.

Cada uno de estos conjuntos de datos se ajusta a un esquema. Este artículo documenta estos esquemas.


## Esquema de datos de puntuación agregada

El esquema para los datos de puntuación se denomina como `AMM AI Schema - <name of model> <id>`. Por ejemplo: `AMM AI Schema - Model for Online Conversion 10120`.

El conjunto de datos, que mantiene los datos de puntuación de un modelo, tiene el nombre `AMM AI Aggregrate Scores - <id>`, por ejemplo `AMM AI Aggregrate Scores - 10120`.

El esquema incluye un grupo de campos con un objeto que contiene detalles sobre las puntuaciones. El objeto consta de los siguientes campos.

| Nombre del campo | Tipo | Definición |
|---|---|---|
| `campaignGroup` | Cadena | Nombre del grupo de campañas. |
| `campaignName` | Cadena | Nombre de la campaña. |
| `contribution` | Duplicada | Contribución atribuida a esta conversión para el punto de contacto determinado. |
| `conversionEndDate` | Fecha | Fecha de finalización de la ventana de conversión. |
| `conversionName` | Cadena | Nombre de la conversión que se creó durante el paso de configuración de la definición de conversión. |
| `conversionStartDate` | Fecha | Fecha de inicio de la ventana de conversión. |
| `geo` | Cadena | La ubicación geográfica donde se produjo la conversión. |
| `mediaChannel` | Cadena | Nombre del canal que se utilizó durante el paso de configuración del punto de contacto. |
| `mediaSubChannel` | Cadena | Nombre del subcanal. |
| `revenue` | Duplicada | Ingresos atribuidos a esta conversión para el punto de contacto determinado. |
| `scoreCreatedTime` | Fecha/Hora | Marca de tiempo del momento en el que se crea este registro de puntuación. |
| `touchpointEndDate` | Fecha | Fecha de finalización de la ventana de punto de contacto. |
| `touchpointName` | Cadena | Nombre del punto de contacto que se creó durante el paso de configuración de la definición del punto de contacto. Actualmente, el punto de contacto se define en el canal de medios. |
| `touchpointStartDate` | Fecha | Fecha de inicio de la ventana de punto de contacto. |


## Esquema de datos de puntuación de eventos

El esquema para los datos de puntuación se denomina como `Attribution AI Scores - <name of model> <id> - Schema`. Por ejemplo: `Attribution AI Scores - Model for Online Conversion 10120 - Schema`.

El conjunto de datos, que mantiene los datos de puntuación de un modelo, tiene el nombre `Attribution AI Scores - <name of model> <id>`, por ejemplo `Attribution AI Scores - Model for Online Conversion 10120 `.

El esquema incluye un grupo de campos que contiene un objeto con detalles sobre los núcleos. El nombre del objeto es `attibution_AI_scores__<name of model> id`.

El grupo de campos contiene los campos siguientes.

| Nombre del campo | Tipo | Descripción |
|---|---|---|
| `conversion` | Objeto | Columnas de metadatos de conversión. |
|     `passThrough` | Objeto |  |
|         `eventType` | Cadena | |
|         `channel_typeAtSource` | Cadena | |
|      `dataSource` | Cadena | Identificación global única de una fuente de datos. <br> **Ejemplo:** `Adobe Analytics` |
|      `eventSource` | Cadena | Origen cuando se produjo el evento real. <br> **Ejemplo:** `Adobe.com` |
|      `eventType` | Cadena | El tipo de evento principal para este registro de serie temporal. <br> **Ejemplo:** `Order` |
|      `geo` | Cadena | Ubicación geográfica donde se entregó la conversión `placeContext.geo.countryCode`. <br> **Ejemplo:** `US` |
|      `path` | Cadena | |
|      `priceTotal` | Duplicada | Ingresos obtenidos mediante la conversión <br> **Ejemplo:** `99.9` |
|      `product` | Cadena | El identificador de XDM del producto en sí. <br> **Ejemplo:** `RX 1080 ti` |
|      `productType` | Cadena | El nombre para mostrar del producto tal como se presenta al usuario en esta vista de producto. <br> **Ejemplo:** `Gpus` |
|      `quantity` | Número entero | Cantidad comprada durante la conversión. <br> **Ejemplo:** `1` |
|      `receivedTimeStamp` | Fecha/Hora | Marca de tiempo recibida de la conversión. <br> **Ejemplo:** `2020-06-09T00:01:51.000Z` |
|      `skuId` | Cadena | SKU (código de referencia), el identificador único de un producto definido por el proveedor. <br> **Ejemplo:** `MJ-03-XS-Black` |
|      `timestamp` | Fecha/Hora | Marca de tiempo de la conversión. <br> **Ejemplo:** `2020-06-09T00:01:51.000Z` |
|      `totalDaysToConversion` | Número entero |  |
|      `totalTouchpointCount` | Número entero | |
| `customerProfile` | Objeto | Detalles de identidad del usuario utilizado para crear el modelo. |
|      `identity` | Objeto | |
|           `id` | Cadena | |
|           `namespace` | Cadena | Contiene los detalles del usuario utilizado para generar el modelo como `id` y `namespace`. |
| `touchpointsDetail` | Objeto[] | La lista de detalles de punto de contacto que llevan a la conversión, ordenados por ocurrencia de punto de contacto o marca de tiempo. |
|      `scores` | Objeto | Contribución de punto de contacto a esta conversión como puntuación. |
|           `algorithmicInfluenced` | Duplicada | La puntuación influenciada es la fracción de la conversión de la que es responsable cada punto de contacto de marketing. |
|           `algorithmicSourced` | Duplicada | La puntuación incremental es la cantidad de impacto marginal causado directamente por un punto de contacto de marketing. |
|           `decayUnits` | Duplicada | Puntuación de atribución basada en reglas en la que los puntos de contacto más cercanos a la conversión reciben más crédito que los puntos de contacto que están más lejos en el tiempo de la conversión. |
|           `firstTouch` | Duplicada | Puntuación de atribución basada en reglas que asigna todos los créditos al punto de contacto inicial de una ruta de conversión. |
|           `lastTouch` | Duplicada | Puntuación de atribución basada en reglas que asigna todo el crédito al punto de contacto más cercano a la conversión. |
|           `linear` | Duplicada | Puntuación de atribución basada en reglas que asigna crédito igual a cada punto de contacto en una ruta de conversión. |
|           `uShape` | Duplicada | Puntuación de atribución basada en reglas que asigna el 40 % del crédito al primer punto de contacto y el 40 % del crédito al último punto de contacto. Los demás puntos de contacto dividen el 20 % restante de forma equitativa. |
|      `touchPoint` | Objeto | Metadatos de Touchpoint. |
|           `passThrough` | Objeto | |
|                `eventType` | Cadena | |
|           `campaignGroup` | Cadena |  |
|           `campaignName` | Cadena | |
|           `campaignTag` | Cadena | |
|           `eventId` | Cadena | |
|           `geo` | Cadena | |
|           `mediaAction` | Cadena | |
|           `mediaChannel` | Cadena | |
|           `receivedTimeStamp` | Fecha/Hora | |
|           `timestamp` | Fecha/Hora | |
|      `isFirstInThePosition` | Número entero | |
|      `lag` | Número entero | |
|      `position` | Cadena | |
|      `touchpointCountToConversion` | Número entero | |
|      `touchpointName` | Cadena | Nombre del punto de contacto que se configuró durante la configuración. <br> **Ejemplo:** `PAID_SEARCH_CLICK` |
| `conversionName` | Cadena | Nombre de la conversión que se configuró durante la configuración. <br> **Ejemplo:** `Order`, `Lead`, `Visit` |
| `scoreCreatedTime` | Fecha/Hora | |
| `segmentation` | Cadena | Segmento de conversión, como la segmentación geográfica, con el que se crea el modelo. Cuando los segmentos están ausentes, `segmentation` es igual que `conversionName`. <br> **Ejemplo:** `ORDER_US` |





Consulte [Esquemas](../ingest-data/schemas.md) para obtener más información.
