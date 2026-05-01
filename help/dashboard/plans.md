---
title: Rendimiento para planificar
description: Aprenda a utilizar la información general Rendimiento para planificar en Mix Modeler.
feature: Dashboard, Plans, Models
exl-id: 930fc1d5-8e28-4610-af7b-c4ec91f86a8a
TQID: https://experienceleague.adobe.com/iRFbGXoCx5jzg6ATId2tNLTfyigoTzD4JQIqlPU5isU
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: d822825b-9821-40d5-9b0d-42a9e3f317c5
subfeature_v2: id: d7b067e6-4f39-41e9-a081-7650346a84cdid: b2520ae7-8f6c-4952-935e-aacc2c10256fid: e6c284e0-b6e6-4f82-bf96-e96bb5157b90
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
autotag-review: '2026-05-01T09:20:18.412Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 537
ht-degree: 0%

---

# Rendimiento para planificar

>[!NOTE]
>
>La ficha **[!UICONTROL Performance to plan]** [!BADGE Beta]{type=Informative} de la página de inicio ![Mix Modeler](/help/assets/icons/Home.svg) **[!UICONTROL Overview]** es una característica beta y su funcionalidad está sujeta a cambios. La función está disponible para un número limitado de clientes.

La ficha **[!UICONTROL Plans]** [!BADGE Beta]{type=Informative} de la página de inicio ![Mix Modeler](/help/assets/icons/Home.svg) **[!UICONTROL Overview]** proporciona un panel de seguimiento para supervisar el rendimiento de su marketing con respecto al plan. Puede realizar un seguimiento del rendimiento real en comparación con el rendimiento planificado mediante tarjetas de estado y visualizaciones.

El tablero le ayuda a identificar brechas, detectar riesgos u oportunidades y realizar ajustes oportunos en sus planes y presupuestos.

Para seleccionar qué datos se muestran para las visualizaciones y las tarjetas de estado de KPI:

* Seleccione un plan en el menú desplegable **[!UICONTROL Plan name]**, usando **[!UICONTROL _Seleccionar una opción..._]**.

* Especifique un periodo de fecha. Para cambiar el período de fecha, escriba una fecha de inicio y una fecha de finalización manualmente o seleccione un período de fecha con ![Calendario](/help/assets/icons/Calendar.svg).

La ficha **[!UICONTROL Plans]** [!BADGE Beta]{type=Informative} muestra:

* [Tarjetas de estado de KPI](#kpi-status-cards):

   * [Presupuesto](#budget)
   * [Ingresos](#revenue)
   * [ROI](#roi)
   * [KPI](#kpi)

* [Visualizaciones](#visualizations):
   * [*Métrica*: real frente a planificada](#metric-actual-vs-planned)
   * [*Métrica*: real frente a planeada por *granularidad*](#metric-actual-vs-planned-by-granularity)
   * [Canal *métrica* por *granularidad*](#channel-metric-by-granularity)
   * [*Métrica* frente a *Métrica* por canal](#metric-vs-metric-by-channel)
   * [*Métrica* por *granularidad*](#metric-by-granularity)
   * [*Métrica* por canal](#metric-by-channel)

## Tarjetas de estado de KPI

![Tarjetas de estado de KPI](../assets/performance-to-plan-kpi-cards.png)


### Presupuesto

Una visualización de progreso circular que muestra cómo se compara el gasto de marketing con el presupuesto del plan para el periodo de fecha.

### Ingresos

Una visualización de progreso circular que muestra cómo se comparan los ingresos reales con los ingresos objetivo planificados para el período de fecha.


### ROI

Una visualización de líneas que muestra el ROI del periodo de fecha.


### KPI

Una visualización de líneas que muestra el KPI para el periodo de fecha.

Para seleccionar otro KPI:

1. Seleccione ![Editar](/help/assets/icons/Edit.svg).
1. En el cuadro de diálogo **[!UICONTROL KPI status card]**, seleccione un KPI en el menú desplegable **[!UICONTROL KPI]**. Las opciones disponibles son: [!UICONTROL Conversions], [!UICONTROL CPA], [!UICONTROL Revenue], [!UICONTROL ROI] y [!UICONTROL Spend].


## Visualizaciones

Hay seis visualizaciones disponibles y puede editar cada una de ellas.

Para cambiar el tamaño de una visualización, utilice el controlador ┛ en la esquina inferior derecha. Para mover una visualización, solo tiene que arrastrar y soltar la visualización en la posición preferida.

Puede situarse sobre cualquier línea, barra o elemento de dispersión de una visualización para mostrar una ventana emergente con información adicional.

![Visualización](../assets/performance-to-plan-visualizations.png)

### *Métrica*: real frente a planificada

Una visualización de barras apiladas que compara los valores de métricas seleccionadas para acumulado, acumulado planificado y totales.


### *Métrica*: real frente a planeada por *granularidad*

Una visualización de líneas que muestra los valores reales y planificados de la métrica seleccionada y la granularidad seleccionada.


### Canal *métrica* por *granularidad*

Una visualización de barras apiladas que muestra las barras apiladas que muestran los canales de la métrica seleccionada y la granularidad seleccionada.


### *Métrica* frente a *Métrica* por canal

Una visualización de puntos que muestra un diagrama de puntos para los canales en las métricas seleccionadas.


### *Métrica* por *granularidad*

Una visualización de barras que muestra los valores reales y planificados de la métrica seleccionada.


### *Métrica* por canal

Una visualización de varias líneas que muestra la métrica seleccionada sobre la granularidad seleccionada.


### Edición de una visualización

Para editar una visualización:

1. Seleccione ![Editar](/help/assets/icons/Edit.svg) para abrir el diálogo **[!UICONTROL Edit data]**.
1. Según la visualización, puede cambiar lo siguiente:

   * Una o dos métricas: Seleccione una métrica en el menú desplegable **[!UICONTROL Select metric]**.

      * Para los planes basados en ROI, las opciones son: [!UICONTROL Conversions], [!UICONTROL CPA], [!UICONTROL Revenue], [!UICONTROL ROI], [!UICONTROL Spend] y [!UICONTROL Volume].
      * Para planes basados en CPA, las opciones son: [!UICONTROL Conversions], [!UICONTROL CPA], [!UICONTROL Spend] y [!UICONTROL Volume].
   * **[!UICONTROL Granularity]**: seleccione **[!UICONTROL date ranges]** o **[!UICONTROL week]** en el menú desplegable **[!UICONTROL Granularity]**.

   Verá en **[!UICONTROL Preview]** que los cambios son diferentes de la visualización **[!UICONTROL Current]**.

1. Seleccione **[!UICONTROL Apply]** para aplicar los cambios. Seleccione **[!UICONTROL Cancel]** para cancelar cualquier cambio en la visualización.
