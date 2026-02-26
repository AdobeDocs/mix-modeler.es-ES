---
title: Información general sobre armonizar conjuntos de datos
description: Aprenda a armonizar los datos en Mix Modeler.
feature: Harmonized Data
exl-id: 6cb70762-e3b2-46a0-b028-1d6daf3edae5
source-git-commit: 23cb7cefe3d1dabfdb8484ad150c38d785841e3b
workflow-type: tm+mt
source-wordcount: '1369'
ht-degree: 7%

---

# Información general sobre armonizar conjuntos de datos

Los datos de Mix Modeler son de diferente naturaleza según la fuente de los datos. Los datos pueden ser:

* datos agregados o resumidos, por ejemplo, recopilados a partir de fuentes de datos de walled garden o datos de publicidad sin conexión recopilados (como el gasto) al ejecutar una campaña de cartelera, un evento o una campaña de publicidad física,
* datos de evento, por ejemplo, de fuentes de datos de origen. Estos datos de evento pueden ser datos recopilados a través del conector de origen de Adobe Analytics desde Adobe Analytics, o a través de la API de Experience Platform Web, Mobile SDK o Edge Network, o datos introducidos mediante conectores de origen.

El servicio de armonización de Mix Modeler asimila los datos acumulados y de evento en una vista de datos coherente. Esta vista de datos es la fuente de los modelos de Mix Modeler. El servicio utiliza la granularidad más alta en los diferentes conjuntos de datos. Por ejemplo, si un conjunto de datos tiene una granularidad mensual y los demás conjuntos de datos tienen granularidad semanal y diaria, el servicio de armonización crea una vista de datos con granularidad mensual.

## Factores

Los factores son clave para modelar la creación y usted desea comprender qué impacto tiene el negocio de manera integral. Es posible que los factores no estén relacionados con los datos de marketing.

* Los factores internos son específicos de su organización y pueden afectar a las conversiones. Por ejemplo, la temporada de ventas, las promociones y mucho más.

* Los factores externos son factores que escapan al control de su organización, pero que aún pueden afectar a las conversiones que logre. Algunos ejemplos son CPI, S&amp;P 500 y más.

La funcionalidad Factores de Mix Modeler utiliza un flujo de trabajo de factores armonizado. Este flujo de trabajo simplifica la administración de los factores, ofrece coherencia en todos los modelos y proporciona una experiencia intuitiva.

Como parte del flujo de trabajo de factores armonizados:

1. Defina campos armonizados para factores de un conjunto de datos de factores en [reglas de conjuntos de datos](/help/harmonize-data/dataset-rules.md#create-a-dataset-rule).
1. [Sincroniza](/help/harmonize-data/dataset-rules.md#sync-data) tus datos armonizados.
1. [Use los factores](/help/models/build.md#configure) en la configuración del modelo.

### Migración

Es posible que tenga modelos que aún no hayan adoptado el flujo de trabajo de factores armonizados y que utilicen el flujo de trabajo de factores basados en conjuntos de datos de Experience Platform. Estos modelos siguen mostrando sus factores basados en conjuntos de datos originales hasta que se actualizan con nuevos factores basados en el flujo de trabajo de factores armonizados.

Al duplicar un modelo que utiliza el flujo de trabajo de factores basados en conjuntos de datos:

* Si el modelo no se ha armonizado, la configuración de factor antigua no se transferirá al modelo duplicado. Tiene que añadir factores mediante el nuevo flujo de trabajo de factores armonizados.
* Si el modelo se ha armonizado, los factores se transfieren y se conservan o actualizan.

## Ejemplo de datos armonizados

Imagine que tiene los siguientes conjuntos de datos disponibles para Mix Modeler.

**Conjunto de datos 1**

Contiene el conjunto de datos de esfuerzo de marketing de YouTube, con una granularidad de los datos agregados establecidos en diarios.

| Fecha | Tipo de fecha | Canal | Campaign | Marca | Geografía | Clics | Gasto |
|---|:--:|---|---|---|---|---:|---:|
| 31-12-2021 | día | YouTube | Y_Otoño_02 | BrandX | EE. UU. | 10000 | 100 |
| 01-01-2022 | día | YouTube | Y_Otoño_02 | BrandX | EE. UU. | 1000 | 10 |
| 03-01-2022 | día | YouTube | Y_Otoño_01 | MarcaY | CA | 10000 | 100 |
| 04-01-2022 | día | YouTube | Y_Summer_01 | Nulo | CA | 9000 | 80 |

{style="table-layout:auto"}


**Conjunto de datos 2**

Contiene el conjunto de datos de esfuerzo de marketing de Facebook, con una granularidad de los datos agregados establecidos en semanal.

| Fecha | Tipo de fecha | Canal | Campaign | Geografía | Clics | Gasto |
|--- |:---:|--- |---|---|---:|---:|
| 01-01-2022 | semana | Facebook | FB_Fall_01 | EE. UU. | 8000 | 100 |
| 08-01-2022 | semana | Facebook | FB_Fall_02 | EE. UU. | 1000 | 10 |
| 08-01-2022 | semana | Facebook | FB_Fall_01 | EE. UU. | 7000 | 100 |
| 16-01-2022 | semana | Facebook | FB_Summer_01 | CA | 10000 | 80 |

{style="table-layout:auto"}


**Conjunto de datos 3**

Un conjunto de datos de conversión, con una granularidad de los datos agregados establecidos en diarios.

| Fecha | Tipo de fecha | Geografía | Objetivo | Ingresos |
|--- |:---: |---|---|---:|
| 01-01-2022 | día | EE. UU. | Moda | 200 |
| 08-01-2022 | día | EE. UU. | Moda | 10 |
| 08-01-2022 | día | EE. UU. | Joyería | 1100 |
| 16-01-2022 | día | CA | Joyería | 80 |

{style="table-layout:auto"}


**Conjunto de datos 4**

Un conjunto de datos de evento de experiencia de ejemplo (eventos de SDK web) del cliente.

| Marca de tiempo | Espacio de nombres de identidad | Id De Identidad | Canal | Clics |
|--- |--- |--- |--- |---:|
| 01-01-2022 00:01:01,000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-01-2022 00:01:01,000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-08-2022 00:01:01,000 | ECID | 2ca2a16e-caf0-4fa9-9a8b-9774b39547c4 | CSE | 1 |
| 01-08-2022 00:01:01,000 | ECID | 5ce99bfb-e44a-40d9-b8cd-c5408bda7cdc | CSE | 1 |

{style="table-layout:auto"}


Desea crear un conjunto de datos armonizado con una granularidad establecida en semanal. Los datos del evento se añaden a la granularidad de la semana y al conjunto de datos armonizado. El resultado es:

**Conjunto de datos armonizado**

| Fecha | Tipo de fecha | Canal | Campaign | Marca | Geografía | Objetivo | Clics | Gasto | Ingresos |
|--- |:---:|--- |--- |--- |---|---|---:|---:|---:|
| 27-12-2021 | semana | YouTube | Y_Otoño_02 | BrandX | EE. UU. | Nulo | 11000 | 110 | Nulo |
| 03-01-2022 | semana | YouTube | Y_Otoño_01 | MarcaY | CA | Nulo | 10000 | 100 | Nulo |
| 03-01-2022 | semana | YouTube | Y_Summer_01 | Nulo | CA | Nulo | 9000 | 80 | Nulo |
| 01-01-2022 | semana | Facebook | FB_Fall_01 | Nulo | EE. UU. | Nulo | 8000 | 100 | Nulo |
| 08-01-2022 | semana | Facebook | FB_Fall_02 | Nulo | EE. UU. | Nulo | 1000 | 10 | Nulo |
| 08-01-2022 | semana | Facebook | FB_Fall_01 | Nulo | EE. UU. | Nulo | 7000 | 100 | Nulo |
| 16-01-2022 | semana | Facebook | FB_Summer_01 | Nulo | CA | Nulo | 10000 | 80 | Nulo |
| 27-12-2021 | semana | Nulo | Nulo | Nulo | EE. UU. | Moda | Nulo | Nulo | 200 |
| 03-01-2022 | semana | Nulo | Nulo | Nulo | EE. UU. | Moda | Nulo | Nulo | 10 |
| 03-01-2022 | semana | Nulo | Nulo | Nulo | EE. UU. | Joyería | Nulo | Nulo | 1100 |
| 10-01-2022 | semana | Nulo | Nulo | Nulo | CA | Joyería | Nulo | Nulo | 80 |
| 01-01-2022 | semana | CSE | Nulo | Nulo | Nulo | Nulo | 2 | Nulo | Nulo |
| 08-01-2022 | semana | CSE | Nulo | Nulo | Nulo | Nulo | 2 | Nulo | Nulo |

{style="table-layout:auto"}


## Configuración de datos armonizados

Para generar un conjunto de datos armonizado, como en el [ejemplo](#an-example-of-harmonized-data) simplificado, debe seguir estos pasos:

1. Defina [campos armonizados](fields.md) adicionales que desee usar más allá de los campos armonizados globales ya disponibles.
1. Configure [reglas de conjuntos de datos](dataset-rules.md) para asignar campos de su agregado (factor o resumen) o conjuntos de datos de eventos de experiencia a campos armonizados.
1. Defina [puntos de contacto de marketing](marketing-touchpoints.md) utilizando los campos armonizados estándar y adicionales que definió.
1. Defina [conversiones](conversions.md) utilizando los campos armonizados estándar y adicionales que definió.


## Ver datos armonizados

Para ver los datos armonizados, en la interfaz de Mix Modeler:

1. Seleccione ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized datasets]** en el carril izquierdo.

1. Seleccione **[!UICONTROL Harmonized data]** de la barra superior. Se muestra un resumen de los datos armonizados en función de los campos, las reglas del conjunto de datos, los puntos de contacto de marketing y las conversiones que haya definido.

   1. Para redefinir el período en el que se basa la recapitulación de datos armonizados, escriba un intervalo de fechas para **[!UICONTROL Date range]** o use ![Calendario](/help/assets/icons/Calendar.svg) para seleccionar un intervalo de datos.

   1. Para modificar las columnas de campos armonizados mostradas para la tabla de datos armonizados, use ![Configuración](/help/assets/icons/Setting.svg) para abrir el cuadro de diálogo **[!UICONTROL Column settings]**.

      1. Seleccione ![SelectBox](/help/assets/icons/SelectBox.svg) una o más columnas de **[!UICONTROL AVAILABLE COLUMNS]** y use ![Chevron right](/help/assets/icons/ChevronRight.svg) para agregar estas columnas a **[!UICONTROL SELECTED COLUMNS]**. Están disponibles todos los campos armonizados estándar que ha definido (incluidos los campos relacionados con conjuntos de datos de factores, como **[!UICONTROL Factor Name]**, **[!UICONTROL Factor Value]**, **[!UICONTROL Factor Type]** y **[!UICONTROL Factor Value Type]**).

      1. Seleccione ![SelectBox](/help/assets/icons/SelectBox.svg) una o más columnas de **[!UICONTROL SELECTED COLUMNS]** y use ![Chevron left](/help/assets/icons/ChevronLeft.svg) para quitar las columnas seleccionadas y devolver estas columnas a **[!UICONTROL AVAILABLE COLUMNS]**.

      1. Seleccione una columna de **[!UICONTROL DEFAULT SORT]** y cambie entre **[!UICONTROL Ascending]** o **[!UICONTROL Descending]**.

      1. Para cambiar el orden de las columnas mostradas, puede mover una columna de **[!UICONTROL SELECTED COLUMNS]** hacia arriba y hacia abajo arrastrando y soltando

   1. Seleccione **[!UICONTROL Submit]** para enviar los cambios de configuración de columna. Seleccione **[!UICONTROL Close]** para cancelar los cambios que haya hecho.

1. Si hay más páginas disponibles, usa ![Flecha izquierda](/help/assets/icons/ChevronLeft.svg) o ![Flecha derecha](/help/assets/icons/ChevronRight.svg) en **[!UICONTROL Page _x _de_x_]** para moverte de una página a otra.

1. Si lo desea, puede descargar los datos armonizados.

   1. Seleccione ![Descargar](/help/assets/icons/Download.svg) [!BADGE beta].
   1. En la ventana emergente, seleccione ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Create]**.
   1. Escriba un **[!UICONTROL Report name]**, por ejemplo `Test Report`.
   1. Seleccione ![ArchivoCSV](/help/assets/icons/FileCSV.svg) **[!UICONTROL Report]**.

   Se descargará un informe CSV con un título basado en el nombre del informe proporcionado y en la fecha y hora actuales (por ejemplo, `Test Report_2025_04_23_9-5-18.csv`) en la carpeta de descarga predeterminada.


## Prácticas recomendadas

Cuando cree su conjunto de datos armonizado, aplique las siguientes prácticas recomendadas.

### Esquema

* Evite las discrepancias de tipos de datos. Las discrepancias se producen cuando el tipo de datos de un campo en los registros de los conjuntos de datos introducidos no se ajusta al tipo de datos configurado para ese campo en el esquema subyacente.
* Evite tipos de esquema incorrectos. Se producen tipos de esquema incorrectos cuando intenta introducir un tipo de datos específico mediante un conjunto de datos que no coincide con el esquema de esos datos. Por ejemplo, intenta introducir datos de resumen mediante un conjunto de datos de factor externo.

### Asignación de datos

* Asegúrese de haber configurado las identidades correctamente para cada uno de los conjuntos de datos de evento.

### Calidad de datos

* Asegúrese de utilizar el formato de fecha y hora de forma coherente para todos los registros de conjuntos de datos que requieran datos con marca de hora.
* Asegúrese de utilizar la misma granularidad (día o semana) para los registros de conjuntos de datos agregados o de resumen.

### Cálculo de datos

* Evite filas duplicadas en un conjunto de datos.
* Asegúrese de que cada conjunto de datos que cargue sea específico para un canal y tipo de conversión únicos. Los puntos de contacto o las conversiones duplicados en varios conjuntos de datos afectan a la salida y la calidad del modelo.

