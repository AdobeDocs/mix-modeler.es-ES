---
title: Datos de puntuación
description: Descubra cómo se mantienen los datos de puntuación de un modelo en Mix Modeler.
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 5%

---

# Datos de puntuación

Como parte de la puntuación de un modelo, los datos de puntuación se conservan dentro de un conjunto de datos en Experience Platform. Este conjunto de datos se ajusta a un esquema creado para cada modelo en la instancia de Mix Modeler.

El esquema para los datos de puntuación se denomina como `AMM AI Schema - <name of model> <id>`. Por ejemplo: `AMM AI Schema - Model for Online Conversion 10120`.

El conjunto de datos, que mantiene los datos de puntuación de un modelo, tiene el nombre `AMM AI Aggregrate Scores - <id>`, por ejemplo `AMM AI Aggregrate Scores - 10120`.


## Esquema

El esquema incluye un grupo de campos con un objeto que contiene detalles sobre las puntuaciones. El objeto consta de los siguientes campos.

| Nombre de campo | Tipo | Definición |
|---|---|---|
| **campaignGroup** | Cadena | Nombre del grupo de campañas. |
| **campaignName** | Cadena | Nombre de la campaña. |
| **contribución** | Doble | Contribución atribuida a esta conversión para el punto de contacto determinado. |
| **conversionEndDate** | Fecha | Fecha de finalización de la ventana de conversión. |
| **conversionName** | Cadena | Nombre de la conversión que se creó durante el paso de configuración de la definición de conversión. |
| **conversionStartDate** | Fecha | Fecha de inicio de la ventana de conversión. |
| **geo** | Cadena | La ubicación geográfica donde se produjo la conversión. |
| **mediaChannel** | Cadena | Nombre del canal que se utilizó durante el paso de configuración del punto de contacto. |
| **mediaSubChannel** | Cadena | Nombre del subcanal. |
| **ingresos** | Doble | Ingresos atribuidos a esta conversión para el punto de contacto determinado. |
| **scoreCreatedTime** | DateTime | Hora a la que se crea este registro de puntuación. |
| **touchpointEndDate** | Fecha | Fecha de finalización de la ventana de punto de contacto. |
| **touchpointName** | Cadena | Nombre del punto de contacto que se creó durante el paso de configuración de la definición del punto de contacto. Actualmente, el punto de contacto se define en el canal de medios. |
| **touchpointStartDate** | Fecha | Fecha de inicio de la ventana de punto de contacto. |

Consulte [Esquemas](../ingest-data/schemas.md) para obtener más información.
