---
title: Resumen de ingesta de datos
description: Obtenga información sobre cómo introducir datos en Mix Modeler.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
source-git-commit: 857641f6c1db749f79056ce2a2ea35fc4d3e3a3c
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 7%

---

# Resumen de ingesta de datos

Mix Modeler funciona con datos de nivel de evento, datos de esfuerzo de marketing acumulados o resumidos de varios jardines amurallados y datos acumulados o resumidos de cualquier otra fuente, como publicidad sin conexión, factores internos o externos.

Los clientes pueden utilizar cualquier tipo de datos que se incorporen a Experience Platform como conjuntos de datos y que se basen en esquemas que utilicen el ExperienceEvent de XDM o las métricas de resumen de XDM como clase base.

Por ejemplo:

* datos recopilados mediante el conector de origen de Adobe Analytics y transformados en conjuntos de datos que se ajustan a la versión predeterminada o personalizada del esquema de Adobe Analytics o, alternativamente,
* datos recopilados mediante la API de Experience Platform Web SDK, Mobile SDK o Edge Network Server para recopilar interacciones de clientes en la web, dispositivos móviles o cualquier otro tipo de dispositivo,
* datos agregados o resumidos de jardines amurallados (como Facebook, YouTube), fuentes de tráfico o datos de publicidad fuera de línea,
* datos acumulados o resumidos que no sean de marketing y que contengan factores internos o externos que sean útiles para la creación de modelos.

Puede utilizar cualquier tipo de mecanismo, compatible con Experience Platform, para introducir datos de esfuerzo de marketing agregado, nivel de evento de experiencia y datos de otras fuentes. Como los SDK de Experience Platform, las API, los conectores de origen y la transmisión y la ingesta por lotes.


## Directrices

Para introducir datos en Experience Platform para utilizarlos con Mix Modeler, siga estas directrices:

* No debe haber ninguna superposición en los datos incrementales que se añaden a los conjuntos de datos.
* Todos los datos de un solo origen deben tener la misma granularidad.
* La fecha y la granularidad son campos obligatorios en el esquema subyacente para todos los datos agregados introducidos como conjuntos de datos
* El canal es un campo obligatorio en el esquema subyacente para todos los datos de esfuerzo/gasto de marketing introducidos como conjuntos de datos.


## Ejemplos

A continuación, se muestran algunos ejemplos de datos que generalmente se utilizan en Mix Modeler, aparte de los datos de evento de experiencia más estándar.

+++ Datos del esfuerzo de marketing agregado

| Geo | Fecha | Tipo de fecha | Canal | Campaign | Haga clic | Obtenido | Participación | Impresión | Open | Propio | Enviado | Gasto |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|--:|
| AMER | 31-10-2021 | día | CORREO ELECTRÓNICO | | 12752 | | | | | | 1132945 | |
| AMER | 31-10-2021 | día | FB | | 148844 | | | | | | | 42111 |
| AMER | 31-10-2021 | día | YT | | | | 2314452 | | | | | 10540 |
| JPN | 21-10-2021 | día | CORREO ELECTRÓNICO | | 21089 | | | | | | 3283626 | |
| JPN | 21-10-2021 | día | SOCIAL | | | | 621 | | | | | 74512 |

{style="table-layout:auto"}

+++

+++ Datos de conversión agregados

| Geo | Fecha | Tipo de fecha | Producto | Unidades vendidas | Ingresos |
|---|:---|:---:|---|--:|--:|
| EMEA | 13-09-2021 | día | Economía creadora | 603 | 36537,68 |
| EMEA | 13-09-2021 | día | Metaverso | 55 | 21704,37 |
| JPN | 30-05-2022 | día | Pro Imaging | 487 | 64469,60 |
| JPN | 30-05-2022 | día | Document Cloud | 642 | 100509,07 |

{style="table-layout:auto"}

+++

+++ Datos de factores externos

| Datos | Tipo de fecha | Factor | Valor |
|---|:---:|:---:|:---|
| 02-08-2020 | semana | SPX | 3325,866 |
| 09-08-2020 | semana | SPX | 3364,158 |
| 16-08-2020 | semana | SPX | 3385,858 |
| 23-08-2020 | semana | SPX | 3497,965 |

{style="table-layout:auto"}

+++

Para trabajar con datos en Mix Modeler, necesita datos recopilados en conjuntos de datos y modelados según esquemas en Experience Platform. La interfaz de Mix Modeler proporciona fácil acceso a la interfaz de usuario de esquemas y conjuntos de datos de Experience Platform.


## Validate

Para validar si los datos están disponibles correctamente en Mix Modeler, puede hacer lo siguiente:

* Usar visualizaciones en [Información general](/help/overview.md).
* Descargue e inspeccione datos de [datos armonizados](/help/harmonize-data/overview.md) en conjuntos de datos armonizados.

Para comprobar si los datos se han introducido correctamente en Experience Platform, puede [escribir y ejecutar consultas SQL mediante el servicio de consultas de Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/query/home).


>[!MORELIKETHIS]
>
>Consulte para obtener más información sobre cómo administrar esquemas y conjuntos de datos:
>
>* [Esquemas](schemas.md)
>* [Conjuntos de datos](datasets.md)
