---
title: Ingesta de datos
description: Aprenda a ingerir datos en el Modelador de mezcla de Adobe.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
source-git-commit: ae1c74ed2edf1e69e7ab77d16aba797921c14ad9
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 14%

---


# Ingesta de datos

El Modelador de mezcla de Adobe funciona tanto con datos de nivel de evento como con datos de esfuerzo de marketing acumulados de varios jardines amurallados. Los clientes pueden utilizar todo tipo de datos que se incorporan en Adobe Experience Platform como conjuntos de datos y que se basan en esquemas basados en eventos de experiencia XDM.

Por ejemplo:

* datos recopilados mediante el conector de origen de Adobe Analytics y transformados en conjuntos de datos que se ajustan a la versión predeterminada o personalizada del esquema de Adobe Analytics o, alternativamente,
* datos recopilados mediante el SDK web de Adobe Experience Platform, el SDK móvil o la API del servidor de red perimetral para recopilar interacciones de clientes en la web, dispositivos móviles o cualquier otro tipo de dispositivo,
* datos de resumen de diferentes fuentes de tráfico/jardín amurallado, basados en un esquema que incluye la clase Métricas de resumen de XDM con el grupo de campos Resumen de tráfico y conversión,
* datos no relacionados con la comercialización (indicadores macroeconómicos, por ejemplo) que sean útiles para la creación de modelos,

Puede utilizar cualquier tipo de mecanismo admitido por Adobe Experience Platform para introducir los datos del nivel de evento de experiencia y el esfuerzo de marketing acumulado. Como los SDK de Adobe Experience Platform, las API, los conectores de origen y la transmisión y la ingesta por lotes.


## Directrices

Para introducir datos en Adobe Experience Platform para utilizarlos con el Modelador de mezcla de Adobe, siga estas directrices:

* No debe haber ninguna superposición en los datos incrementales que se añaden a los conjuntos de datos.
* Todos los datos de un solo origen deben tener la misma granularidad.
* La fecha y la granularidad son campos obligatorios en el esquema subyacente para todos los datos agregados introducidos como conjuntos de datos
* El canal es un campo obligatorio en el esquema subyacente para todos los datos de esfuerzo/gasto de marketing introducidos como conjuntos de datos.


## Ejemplos

A continuación, encontrará algunos ejemplos de datos que normalmente se utilizan en el Modelador de mezcla de Adobe, aparte de datos de eventos de experiencia más estándar.

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

Para trabajar con datos en el Modelador de mezcla de Adobe, necesita datos recopilados en conjuntos de datos y modelados según esquemas en Adobe Experience Platform. La interfaz del Modelador de mezcla de Adobe proporciona fácil acceso a la interfaz de usuario de esquemas y conjuntos de datos.

>[!MORELIKETHIS]
>
>Consulte para obtener más información sobre cómo administrar esquemas y conjuntos de datos:
>
>* [Esquemas](schemas.md)
>* [Conjuntos de datos](datasets.md)
