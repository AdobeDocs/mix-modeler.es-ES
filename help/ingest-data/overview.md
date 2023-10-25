---
title: Ingesta de datos
description: Obtenga información sobre cómo introducir datos en Mix Modeler.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
source-git-commit: 1dbdee00f518d98241fc042e2aabc0e40d5a9153
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 14%

---

# Ingesta de datos

El Mix Modeler trabaja con datos de nivel de evento, agrega un resumen de datos de esfuerzo de marketing de varios jardines amurallados y agrega o resume datos de cualquier otra fuente, como publicidad sin conexión, factores internos o factores externos.

Los clientes pueden utilizar cualquier tipo de datos que se incorporen en Experience Platform como conjuntos de datos y que se basen en esquemas que utilicen las métricas de resumen de XDM ExperienceEvent o XDM como clase base.

Por ejemplo:

* datos recopilados mediante el conector de origen de Adobe Analytics y transformados en conjuntos de datos que se ajustan a la versión predeterminada o personalizada del esquema de Adobe Analytics o, alternativamente,
* datos recopilados mediante el SDK web de Experience Platform, el SDK móvil o la API del servidor de red perimetral para recopilar interacciones de clientes en la web, dispositivos móviles o cualquier otro tipo de dispositivo,
* datos agregados o resumidos de los jardines amurallados (como Facebook, YouTube), fuentes de tráfico o datos de publicidad sin conexión,
* datos acumulados o resumidos que no sean de marketing y que contengan factores internos o externos que sean útiles para la creación de modelos.

Puede utilizar cualquier tipo de mecanismo, admitido por Experience Platform, para introducir datos de esfuerzo de marketing acumulado, nivel de evento de experiencia y datos de otras fuentes. Como los SDK de Experience Platform, las API, los conectores de origen y la transmisión y la ingesta por lotes.


## Directrices

Para introducir datos en Experience Platform para su uso con Mix Modeler, siga estas directrices:

* No debe haber ninguna superposición en los datos incrementales que se añaden a los conjuntos de datos.
* Todos los datos de un solo origen deben tener la misma granularidad.
* La fecha y la granularidad son campos obligatorios en el esquema subyacente para todos los datos agregados introducidos como conjuntos de datos
* El canal es un campo obligatorio en el esquema subyacente para todos los datos de esfuerzo/gasto de marketing introducidos como conjuntos de datos.


## Ejemplos

A continuación, se muestran algunos ejemplos de datos que generalmente se utilizan en Mix Modeler aparte de los datos de evento de experiencia más estándar.

+++ Datos del esfuerzo de marketing agregado

| Geo | Fecha | Tipo de fecha | Canal | Campaign | Haga clic | Obtenido | Participación | Impresión | Open | Propio | Enviados |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|
| AMER | 2021-10-31 | día | CORREO ELECTRÓNICO | | 12752 | | | | | | 1132945 |
| AMER | 2021-10-31 | día | FB | | 148844 | | | | | | |
| AMER | 2021-10-31 | día | YT | | | | 2314452 | | | | |
| JPN | 2021-10-21 | día | CORREO ELECTRÓNICO | | 21089 | | | | | | 3283626 |
| JPN | 2021-10-21 | día | SOCIAL | | | | 621 | | | | |

{style="table-layout:auto"}

+++

+++ Datos de conversión agregados

| Geo | Fecha | Tipo de fecha | Producto | Unidades vendidas | Ingresos |
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

Para trabajar con datos en Mix Modeler, necesita datos recopilados en conjuntos de datos y modelados según esquemas en Experience Platform. La interfaz de Mix Modeler proporciona fácil acceso a la interfaz de usuario de esquemas y conjuntos de datos.


>[!MORELIKETHIS]
>
>Consulte para obtener más información sobre cómo administrar esquemas y conjuntos de datos:
>
>* [Esquemas](schemas.md)
>* [Conjuntos de datos](datasets.md)
