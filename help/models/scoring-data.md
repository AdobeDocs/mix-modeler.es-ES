---
title: Datos de puntuación
description: Descubra cómo se mantienen los datos de puntuación de un modelo en Mix Modeler.
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
source-git-commit: b6045176e82b97f848113f4e0ffbbb995c48b3d4
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 6%

---

# Datos de puntuación

Como parte de la puntuación de un modelo, los datos de puntuación se conservan dentro de un conjunto de datos en Experience Platform. Cuando se ha habilitado la atribución de múltiples contactos durante la creación del modelo, se conservan datos de puntuación de evento adicionales dentro de un conjunto de datos en Experience Platform.

Cada uno de estos conjuntos de datos se ajusta a un esquema. Este artículo documenta estos esquemas.


## Esquema de datos de puntuación agregada

El esquema para los datos de puntuación se denomina como `AMM AI Schema - <name of model> <id>`. Por ejemplo: `AMM AI Schema - Model for Online Conversion 10120`.

El conjunto de datos, que mantiene los datos de puntuación de un modelo, tiene el nombre `AMM AI Aggregrate Scores - <id>`, por ejemplo `AMM AI Aggregrate Scores - 10120`.

El esquema incluye un grupo de campos con un objeto que contiene detalles sobre las puntuaciones. El objeto consta de los siguientes campos.

| Nombre de campo | Tipo | Definición |
|---|---|---|
| `campaignGroup` | Cadena | Nombre del grupo de campañas. |
| `campaignName` | Cadena | Nombre de la campaña. |
| `contribution` | Doble | Contribución atribuida a esta conversión para el punto de contacto determinado. |
| `conversionEndDate` | Fecha | Fecha de finalización de la ventana de conversión. |
| `conversionName` | Cadena | Nombre de la conversión que se creó durante el paso de configuración de la definición de conversión. |
| `conversionStartDate` | Fecha | Fecha de inicio de la ventana de conversión. |
| `geo` | Cadena | La ubicación geográfica donde se produjo la conversión. |
| `mediaChannel` | Cadena | Nombre del canal que se utilizó durante el paso de configuración del punto de contacto. |
| `mediaSubChannel` | Cadena | Nombre del subcanal. |
| `revenue` | Doble | Ingresos atribuidos a esta conversión para el punto de contacto determinado. |
| `scoreCreatedTime` | DateTime | Marca de tiempo del momento en el que se crea este registro de puntuación. |
| `touchpointEndDate` | Fecha | Fecha de finalización de la ventana de punto de contacto. |
| `touchpointName` | Cadena | Nombre del punto de contacto que se creó durante el paso de configuración de la definición del punto de contacto. Actualmente, el punto de contacto se define en el canal de medios. |
| `touchpointStartDate` | Fecha | Fecha de inicio de la ventana de punto de contacto. |


## Esquema de datos de puntuación de eventos

El esquema para los datos de puntuación se denomina como `Attribution AI Scores - <name of model> <id> - Schema`. Por ejemplo: `Attribution AI Scores - Model for Online Conversion 10120 - Schema`.

El conjunto de datos, que mantiene los datos de puntuación de un modelo, tiene el nombre `Attribution AI Scores - <name of model> <id>`, por ejemplo `Attribution AI Scores - Model for Online Conversion 10120 `.

El esquema incluye un grupo de campos que contiene un objeto con detalles sobre los núcleos. El nombre del objeto es `attibution_AI_scores__<name of model> id`.

El grupo de campos contiene los campos siguientes.

| Nombre de campo | Tipo | Descripción |
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
|      `priceTotal` | Doble | Ingresos obtenidos mediante la conversión <br> **Ejemplo:** `99.9` |
|      `product` | Cadena | El identificador de XDM del producto en sí. <br> **Ejemplo:** `RX 1080 ti` |
|      `productType` | Cadena | El nombre para mostrar del producto tal como se presenta al usuario en esta vista de producto. <br> **Ejemplo:** `Gpus` |
|      `quantity` | Entero | Cantidad comprada durante la conversión. <br> **Ejemplo:** `1` |
|      `receivedTimeStamp` | DateTime | Marca de tiempo recibida de la conversión. <br> **Ejemplo:** `2020-06-09T00:01:51.000Z` |
|      `skuId` | Cadena | SKU (código de referencia), el identificador único de un producto definido por el proveedor. <br> **Ejemplo:** `MJ-03-XS-Black` |
|      `timestamp` | DateTime | Marca de tiempo de la conversión. <br> **Ejemplo:** `2020-06-09T00:01:51.000Z` |
|      `totalDaysToConversion` | Entero |  |
|      `totalTouchpointCount` | Entero | |
| `customerProfile` | Objeto | Detalles de identidad del usuario utilizado para crear el modelo. |
|      `identity` | Objeto | |
|           `id` | Cadena | |
|           `namespace` | Cadena | Contiene los detalles del usuario utilizado para generar el modelo como `id` y `namespace`. |
| `touchpointsDetail` | Objeto[] | La lista de detalles de punto de contacto que llevan a la conversión, ordenados por ocurrencia de punto de contacto o marca de tiempo. |
|      `scores` | Objeto | Contribución de punto de contacto a esta conversión como puntuación. |
|           `algorithmicInfluenced` | Doble | La puntuación influenciada es la fracción de la conversión de la que es responsable cada punto de contacto de marketing. |
|           `algorithmicSourced` | Doble | La puntuación incremental es la cantidad de impacto marginal causado directamente por un punto de contacto de marketing. |
|           `decayUnits` | Doble | Puntuación de atribución basada en reglas en la que los puntos de contacto más cercanos a la conversión reciben más crédito que los puntos de contacto que están más lejos en el tiempo de la conversión. |
|           `firstTouch` | Doble | Puntuación de atribución basada en reglas que asigna todos los créditos al punto de contacto inicial de una ruta de conversión. |
|           `lastTouch` | Doble | Puntuación de atribución basada en reglas que asigna todo el crédito al punto de contacto más cercano a la conversión. |
|           `linear` | Doble | Puntuación de atribución basada en reglas que asigna crédito igual a cada punto de contacto en una ruta de conversión. |
|           `uShape` | Doble | Puntuación de atribución basada en reglas que asigna el 40 % del crédito al primer punto de contacto y el 40 % del crédito al último punto de contacto. Los demás puntos de contacto dividen el 20 % restante de forma equitativa. |
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
|           `receivedTimeStamp` | DateTime | |
|           `timestamp` | DateTime | |
|      `isFirstInThePosition` | Entero | |
|      `lag` | Entero | |
|      `position` | Cadena | |
|      `touchpointCountToConversion` | Entero | |
|      `touchpointName` | Cadena | Nombre del punto de contacto que se configuró durante la configuración. <br> **Ejemplo:** `PAID_SEARCH_CLICK` |
| `conversionName` | Cadena | Nombre de la conversión que se configuró durante la configuración. <br> **Ejemplo:** `Order`, `Lead`, `Visit` |
| `scoreCreatedTime` | DateTime | |
| `segmentation` | Cadena | Segmento de conversión, como la segmentación geográfica, con el que se crea el modelo. Cuando los segmentos están ausentes, `segmentation` es igual que `conversionName`. <br> **Ejemplo:** `ORDER_US` |





Consulte [Esquemas](../ingest-data/schemas.md) para obtener más información.
