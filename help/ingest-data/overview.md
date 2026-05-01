---
title: Resumen de ingesta de datos
description: Obtenga información sobre cómo introducir datos en Mix Modeler.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
TQID: https://experienceleague.adobe.com/XPr8Av7skzHBYoU6WtNw8PtHFrPH-MokICrLwoB2-J0
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: e0abf868-dae2-4c1c-83e9-b21799232845
  - id: fbd94e4b-f9b8-42a4-8df5-3f917aabae24
subfeature_v2:
  - id: ad7101f7-ae92-401b-a25a-d3060d42989d
  - id: d1167c89-f64a-42ca-ac95-1d91b7790df2
  - id: ee1bf083-e090-4def-936b-c111d29f42d0
  - id: a4dc3e7d-bd07-4ac8-8e49-ff2e8fecf1e7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
autotag-review: '2026-05-01T09:11:34.506Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 584
ht-degree: 14%

---

# Resumen de ingesta de datos

Mix Modeler funciona con datos de nivel de evento, datos de esfuerzo de marketing acumulados o resumidos de varios jardines amurallados. Y con datos agregados o resumidos de cualquier otra fuente, como publicidad fuera de línea, factores internos o externos.

Los clientes pueden utilizar cualquier tipo de datos que se incorporen a Experience Platform como conjuntos de datos y que se basen en esquemas que utilicen el ExperienceEvent de XDM o las métricas de resumen de XDM como clase base.

Por ejemplo:

* Datos recopilados mediante el conector de origen de Adobe Analytics. Y se transforman en conjuntos de datos que se ajustan a la versión predeterminada o personalizada del esquema de Adobe Analytics.
* Datos recopilados mediante la API de Experience Platform Web SDK, Mobile SDK o Edge Network Server para recopilar interacciones de clientes en la web, dispositivos móviles o cualquier otro tipo de dispositivo.
* Datos agregados o resumidos de jardines amurallados (como Facebook, YouTube), fuentes de tráfico o datos de publicidad sin conexión.
* Datos acumulados o resumidos no relacionados con el marketing que contienen factores internos o externos que son útiles para la creación de modelos.

Puede utilizar cualquier tipo de mecanismo, compatible con Experience Platform, para introducir datos de esfuerzo de marketing agregado, nivel de evento de experiencia y datos de otras fuentes. Como los SDK de Experience Platform, las API, los conectores de origen y la transmisión y la ingesta por lotes. Para obtener más información sobre cómo ingerir los datos en Experience Platform para usarlos en Adobe Mix Modeler, consulte la [descripción general de la ingesta de datos](https://experienceleague.adobe.com/es/docs/experience-platform/ingestion/home).

## Directrices

Para introducir datos en Experience Platform para utilizarlos con Mix Modeler, siga estas directrices:

* No debe haber ninguna superposición en los datos incrementales que se añaden a los conjuntos de datos.
* Todos los datos de un solo origen deben tener la misma granularidad.
* La fecha y la granularidad son campos obligatorios en el esquema subyacente para todos los datos agregados introducidos como conjuntos de datos
* El canal es un campo obligatorio en el esquema subyacente para todos los datos de esfuerzo/gasto de marketing introducidos como conjuntos de datos.


## Ejemplos

A continuación, se muestran algunos ejemplos de datos que generalmente se utilizan en Mix Modeler, aparte de los datos de evento de experiencia más estándar.

+++ Datos del esfuerzo de marketing agregado

| Geografía | Fecha | Tipo de fecha | Canal | Campaign | Click | Obtenido | Participación | Impresión | Abrir | Propio | Enviado | Gasto |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|--:|
| AMER | 2021-10-31 | día | EMAIL | | 12752 | | | | | | 1132945 | |
| AMER | 2021-10-31 | día | FB | | 148844 | | | | | | | 42111 |
| AMER | 2021-10-31 | día | YT | | | | 2314452 | | | | | 10540 |
| JPN | 2021-10-21 | día | EMAIL | | 21089 | | | | | | 3283626 | |
| JPN | 2021-10-21 | día | SOCIAL | | | | 621 | | | | | 74512 |

{style="table-layout:auto"}

+++

+++ Datos de conversión agregados

| Geografía | Fecha | Tipo de fecha | Producto | Unidades vendidas | Ingresos |
|---|:---|:---:|---|--:|--:|
| EMEA | 2021-09-13 | día | Economía creadora | 603 | 36537.68 |
| EMEA | 2021-09-13 | día | Metaverso | 55 | 21704.37 |
| JPN | 2022-05-30 | día | Pro Imaging | 487 | 64469.60 |
| JPN | 2022-05-30 | día | Document Cloud | 642 | 100509.07 |

{style="table-layout:auto"}

+++

+++ Datos de factores externos

| Datos | Tipo de fecha | Factor | Valor |
|---|:---:|:---:|:---|
| 2020-08-02 | semana | SPX | 3325.866 |
| 2020-08-09 | semana | SPX | 3364.158 |
| 2020-08-16 | semana | SPX | 3385.858 |
| 2020-08-23 | semana | SPX | 3497.965 |

{style="table-layout:auto"}

+++

Para trabajar con datos en Mix Modeler, necesita datos recopilados en conjuntos de datos y modelados según esquemas en Experience Platform. La interfaz de Mix Modeler proporciona fácil acceso a la interfaz de usuario de esquemas y conjuntos de datos de Experience Platform.


## Validación

Para validar si los datos están disponibles correctamente en Mix Modeler, puede hacer lo siguiente:

* Use visualizaciones en [Información general](/help/overview.md).
* Descargue e inspeccione datos de [datos armonizados](/help/harmonize-data/overview.md) en conjuntos de datos armonizados.

Para comprobar si los datos se han introducido correctamente en Experience Platform, puede [escribir y ejecutar consultas SQL mediante el servicio de consultas de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/query/home).


>[!MORELIKETHIS]
>
>Consulte para obtener más información sobre cómo administrar esquemas y conjuntos de datos:
>
>* [Esquemas](schemas.md)
>* [Conjuntos de datos](datasets.md)
