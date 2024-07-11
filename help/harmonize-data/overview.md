---
title: Armonizar datos
description: Aprenda a armonizar los datos en Mix Modeler.
feature: Harmonized Data
exl-id: 6cb70762-e3b2-46a0-b028-1d6daf3edae5
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '893'
ht-degree: 7%

---

# Armonizar datos

Los datos de Mix Modeler son de diferente naturaleza según la fuente de los datos. Los datos pueden ser:

* datos agregados o resumidos, por ejemplo, recopilados a partir de fuentes de datos de walled garden o datos de publicidad sin conexión recopilados (como el gasto) al ejecutar una campaña de cartelera, un evento o una campaña de publicidad física,
* datos de evento, por ejemplo, de fuentes de datos de origen. Estos datos de evento pueden ser datos recopilados a través del conector de origen de Adobe Analytics desde Adobe Analytics o a través de la web de Experience Platform, el SDK móvil o la API de Edge Network, o datos introducidos mediante conectores de origen.

El servicio de armonización de Mix Modeler asimila los datos acumulados y de evento en una vista de datos coherente. Esta vista de datos, combinada con datos de factores internos y externos, es la fuente de los modelos de Mix Modeler. El servicio utiliza la granularidad más alta en los diferentes conjuntos de datos. Por ejemplo, si un conjunto de datos tiene una granularidad mensual y los demás conjuntos de datos tienen granularidad semanal y diaria, el servicio de armonización crea una vista de datos con granularidad mensual.

## Ejemplo de datos armonizados

Imagine que tiene los siguientes conjuntos de datos disponibles para el Mix Modeler.

**Conjunto de datos 1**

Contiene el conjunto de datos de esfuerzo de marketing de YouTube, con una granularidad de los datos agregados establecidos en diarios.

| Fecha | Tipo de fecha | Canal | Campaign | Marca | Geo | Clics | Gasto |
|---|:--:|---|---|---|---|---:|---:|
| 31-12-2021 | día | YouTube | Y_Otoño_02 | BrandX | US | 10000 | 100 |
| 01-01-2022 | día | YouTube | Y_Otoño_02 | BrandX | US | 1000 | 10 |
| 03-01-2022 | día | YouTube | Y_Otoño_01 | MarcaY | CA | 10000 | 100 |
| 04-01-2022 | día | YouTube | Y_Summer_01 | Nulo | CA | 9000 | 80 |

{style="table-layout:auto"}


**Conjunto de datos 2**

Contiene el conjunto de datos de esfuerzo de marketing de Facebook, con una granularidad del conjunto de datos agregado establecido en semanal.

| Fecha | Tipo de fecha | Canal | Campaign | Geo | Clics | Gasto |
|--- |:---:|--- |---|---|---:|---:|
| 01-01-2022 | semana | Facebook | FB_Fall_01 | US | 8000 | 100 |
| 08-01-2022 | semana | Facebook | FB_Fall_02 | US | 1000 | 10 |
| 08-01-2022 | semana | Facebook | FB_Fall_01 | US | 7000 | 100 |
| 16-01-2022 | semana | Facebook | FB_Summer_01 | CA | 10000 | 80 |

{style="table-layout:auto"}


**Conjunto de datos 3**

Un conjunto de datos de conversión, con una granularidad de los datos agregados establecidos en diarios.

| Fecha | Tipo de fecha | Geo | Meta | Ingresos |
|--- |:---: |---|---|---:|
| 01-01-2022 | día | US | Moda | 200 |
| 08-01-2022 | día | US | Moda | 10 |
| 08-01-2022 | día | US | Joyería | 1100 |
| 16-01-2022 | día | CA | Joyería | 80 |

{style="table-layout:auto"}


**Conjunto de datos 4**

Un conjunto de datos de evento de experiencia de ejemplo (eventos de SDK web) del cliente.

| Marca de tiempo | Área de nombres de identidad | Id De Identidad | Canal | Clics |
|--- |--- |--- |--- |---:|
| 01-01-2022 00:01:01,000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-01-2022 00:01:01,000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-08-2022 00:01:01,000 | ECID | 2ca2a16e-caf0-4fa9-9a8b-9774b39547c4 | CSE | 1 |
| 01-08-2022 00:01:01,000 | ECID | 5ce99bfb-e44a-40d9-b8cd-c5408bda7cdc | CSE | 1 |

{style="table-layout:auto"}


Desea crear un conjunto de datos armonizado con una granularidad establecida en semanal. Los datos del evento se añaden a la granularidad de la semana y al conjunto de datos armonizado. El resultado es:

**Conjunto de datos armonizado**

| Fecha | Tipo de fecha | Canal | Campaign | Marca | Geo | Meta | Clics | Gasto | Ingresos |
|--- |:---:|--- |--- |--- |---|---|---:|---:|---:|
| 27-12-2021 | semana | YouTube | Y_Otoño_02 | BrandX | US | Nulo | 11000 | 110 | Nulo |
| 03-01-2022 | semana | YouTube | Y_Otoño_01 | MarcaY | CA | Nulo | 10000 | 100 | Nulo |
| 03-01-2022 | semana | YouTube | Y_Summer_01 | Nulo | CA | Nulo | 9000 | 80 | Nulo |
| 01-01-2022 | semana | Facebook | FB_Fall_01 | Nulo | US | Nulo | 8000 | 100 | Nulo |
| 08-01-2022 | semana | Facebook | FB_Fall_02 | Nulo | US | Nulo | 1000 | 10 | Nulo |
| 08-01-2022 | semana | Facebook | FB_Fall_01 | Nulo | US | Nulo | 7000 | 100 | Nulo |
| 16-01-2022 | semana | Facebook | FB_Summer_01 | Nulo | CA | Nulo | 10000 | 80 | Nulo |
| 27-12-2021 | semana | Nulo | Nulo | Nulo | US | Moda | Nulo | Nulo | 200 |
| 03-01-2022 | semana | Nulo | Nulo | Nulo | US | Moda | Nulo | Nulo | 10 |
| 03-01-2022 | semana | Nulo | Nulo | Nulo | US | Joyería | Nulo | Nulo | 1100 |
| 10-01-2022 | semana | Nulo | Nulo | Nulo | CA | Joyería | Nulo | Nulo | 80 |
| 01-01-2022 | semana | CSE | Nulo | Nulo | Nulo | Nulo | 2 | Nulo | Nulo |
| 08-01-2022 | semana | CSE | Nulo | Nulo | Nulo | Nulo | 2 | Nulo | Nulo |

{style="table-layout:auto"}


## Configuración de datos armonizados

Para crear un conjunto de datos armonizado, como en el [ejemplo](#an-example-of-harmonized-data), debe seguir estos pasos:

1. Definir más [campos armonizados](fields.md) que desee utilizar más allá de los campos globales armonizados ya disponibles.
1. Configuración de [reglas de conjuntos de datos](dataset-rules.md) para asignar campos de los conjuntos de datos de evento de experiencias o agregados a campos armonizados.
1. Definir [puntos de contacto de marketing](marketing-touchpoints.md) utilizando los campos armonizados estándar y adicionales que haya definido.
1. Definir [conversiones](conversions.md) utilizando los campos armonizados estándar y adicionales que haya definido.


## Ver datos armonizados

Para ver los datos armonizados, en la interfaz de Mix Modeler:

1. Seleccionar ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized datasets]** desde el carril izquierdo.

1. Seleccionar **[!UICONTROL Harmonized Data]** desde la barra superior. Se muestra un resumen de los datos armonizados en función de los campos, las reglas del conjunto de datos, los puntos de contacto de marketing y las conversiones que haya definido.

   1. Para redefinir el periodo en el que se basa el resumen de datos armonizados, introduzca un intervalo de fechas para **[!UICONTROL Date range]** o use ![Calendario](/help/assets//icons/Calendar.svg) para seleccionar un rango de datos.

   1. Para modificar las columnas de campo armonizadas mostradas para la tabla de datos armonizados, utilice ![Configuración](/help/assets//icons/Setting.svg) para abrir **[!UICONTROL Column settings]** diálogo.

      1. Seleccionar ![SelectBox](/help/assets//icons/SelectBox.svg) una o más columnas de **[!UICONTROL AVAILABLE COLUMNS]** y utilice ![cheurón derecho](/help/assets//icons/ChevronRight.svg) para agregar estas columnas a **[!UICONTROL SELECTED COLUMNS]**.

      1. Seleccionar ![SelectBox](/help/assets//icons/SelectBox.svg) una o más columnas de **[!UICONTROL SELECTED COLUMNS]** y utilice ![Corchete izquierdo](/help/assets//icons/ChevronLeft.svg) para quitar las columnas seleccionadas y devolver estas columnas a **[!UICONTROL AVAILABLE COLUMNS]**.

      1. Seleccionar una columna de **[!UICONTROL DEFAULT SORT]** y alternar entre **[!UICONTROL Ascending]** o **[!UICONTROL Descending]**.

      1. Para cambiar el orden de las columnas mostradas, puede mover una columna a **[!UICONTROL SELECTED COLUMNS]** arriba y abajo mediante arrastrar y soltar

   1. Seleccionar **[!UICONTROL Submit]** para enviar los cambios de configuración de columna. Seleccionar **[!UICONTROL Close]** para cancelar los cambios realizados.

1. Si hay más páginas disponibles, utilice ![Flecha izquierda](/help/assets//icons/ChevronLeft.svg) o ![Flecha derecha](/help/assets//icons/ChevronRight.svg) en **[!UICONTROL Page _x _de_x_]** para desplazarse entre páginas.
