---
title: Perspectivas del plan
description: Obtenga información sobre cómo ver información sobre su plan y editar un plan en Mix Modeler.
feature: Plans
exl-id: 91385595-284f-4fcb-b54b-9539905e552b
source-git-commit: 3545a7045478108db4d9f6bb87df679bfede5a45
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Perspectivas del plan


En [!UICONTROL Plan insights], se crean las perspectivas del plan, que muestran [!UICONTROL Model], [!UICONTROL Data range] y [!UICONTROL Total budget] en los que se basa el plan.

Cuando termine de recuperar, verá una descripción general del plan, que consta de:

- Visualización [!UICONTROL Forecasted paid channel ROI]
- Visualización [!UICONTROL Forecasted revenue]
- Visualización [!UICONTROL Forecasted conversion]
- Visualización [!UICONTROL Marginal channel return]
- [!UICONTROL Data range breakdown] tabla del plan, mostrando columnas para

   - Canal
   - ROI
   - CPA
   - Ingresos
   - Meta de conversión
   - Gasto

Para cerrar la interfaz, seleccione **[!UICONTROL Close]**.

Para cambiar la forma de ver el ROI de su plan, seleccione **[!UICONTROL X]** o **[!UICONTROL  %]** en **[!UICONTROL View ROI]**.

## Gasto previsto en el canal de pago y ROI

Esta visualización muestra un diagrama de dispersión para el gasto previsto y el retorno de la inversión en los canales de pago, en función del modelo, el intervalo de fechas y el presupuesto.

![Visualización del gasto y el retorno de la inversión del canal de pago previsto](../assets/overview-plan-forecasted-paid-channel-send-roi.png)


## Ingresos previstos

Esta visualización de gráfico de barras muestra los ingresos previstos para sus canales en función del modelo, el intervalo de fechas y el presupuesto.

![Visualización de ingresos previstos](../assets/overview-plan-forecasted-revenue.png)


## Conversiones previstas

Esta visualización de gráfico de barras muestra las conversiones previstas para los canales en función del modelo, el intervalo de fechas y el presupuesto.

![Visualización de conversiones previstas](../assets/overview-plan-forecasted-conversions.png)


## Retorno de canal marginal

Esta visualización de gráfico de líneas muestra una curva de retorno marginal para el canal seleccionado con indicadores para **[!UICONTROL Marginal break-even]** y **[!UICONTROL Return point]**. Esta visualización le ayuda a comprender cómo se gasta un canal al alcanzar un punto de equilibrio marginal y si tiene espacio para aumentar el gasto en un canal o si debe gastar menos en un canal para mejorar la eficiencia de gasto del canal.

![Visualización de retorno de canal marginal](../assets/overview-plan-marginal-channel-return.png)

Para seleccionar un canal específico para la visualización, seleccione un canal del menú desplegable **[!UICONTROL View]**.


## Desglose del intervalo de fechas

La tabla [!UICONTROL Date range breakdown] muestra datos granulares detallados por canal para [!UICONTROL ROI], [!UICONTROL Revenue], [!UICONTROL CPA], [!UICONTROL Conversions] y [!UICONTROL Spend].

![Tabla de desglose de intervalos de fechas](../assets/overview-plan-date-range-breakdown.png)

1. Para descargar un archivo CSV que contenga los datos del desglose Intervalo de fechas, seleccione ![Descargar](/help/assets/icons/Download.svg) **[!UICONTROL Download CSV]**. En el menú contextual:

   - Seleccione ![Descargar](/help/assets/icons/Download.svg) **[!UICONTROL Detailed CSV]** para obtener datos detallados en formato CSV.
   - Seleccione ![Descargar](/help/assets/icons/Download.svg) **[!UICONTROL Summary CSV]** para ver los datos de resumen en formato CSV.

   Los datos detallados son datos granulares tecleados por semana. Los datos de resumen son datos introducidos por el intervalo de fechas proporcionado por el modelo.

1. Para ver el desglose Intervalo de fecha por categoría de canales, seleccione **[!UICONTROL All channels]**, **[!UICONTROL Paid channels]** o **[!UICONTROL Non-paid channels]** de la selección **[!UICONTROL View]**.


## Editar plan

1. Para editar tu plan, selecciona ![Editar](/help/assets/icons/Edit.svg) **[!UICONTROL Edit plan]**:

   1. En la sección **[!UICONTROL Spend selection]**, para cada intervalo de fechas del presupuesto, use ![cheurón](/help/assets/icons/ChevronRight.svg) para abrir la vista de distribución de canal para ese intervalo de datos.

   1. Para modificar los presupuestos de cada canal, modifique los valores de **[!UICONTROL Min]** y **[!UICONTROL Max]** o use los controles deslizantes.

   1. Para alternar entre la entrada de moneda o porcentaje, seleccione **[!UICONTROL $]** o **[!UICONTROL %]** para **[!UICONTROL View spend by]**.

      ![Selección de gastos](/help/assets/spend-selection.png)

   1. Para editar los detalles de su plan, seleccione **[!UICONTROL Edit details]**:

      1. En la sección **[!UICONTROL Setup]**, si corresponde, modifique **[!UICONTROL Plan name]** y **[!UICONTROL Description]**.

      1. En la sección **[!UICONTROL Budget]**:

         1. Modifique **[!UICONTROL Date range]** para uno o más intervalos de fechas del plan, ya sea escribiendo fechas o seleccionando un intervalo de fechas utilizando ![Calendario](/help/assets/icons/Calendar.svg).

         1. Modifique **[!UICONTROL Budget]** para uno o más de los intervalos de fechas de su plan.

         Para agregar intervalos de fechas adicionales, cada uno con su presupuesto, seleccione ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

         Para eliminar un intervalo de fechas y un presupuesto asociado, seleccione ![Cerrar](/help/assets/icons/Close.svg).

         Para definir un presupuesto máximo:

         1. Activar **[!UICONTROL Maximize budget]**.
         1. Especifique la cantidad de presupuesto máximo. La cantidad debe ser igual o superior a la cantidad total de presupuestos especificados para los intervalos de fechas.

      1. Seleccione **[!UICONTROL Next]** para volver a la sección **[!UICONTROL Spend]**. Seleccione **[!UICONTROL Cancel]** para regresar a la descripción general de sus planes.

         ![Detalles del plan](/help/assets/plan-details.png)

   1. Si ha definido configuraciones avanzadas para su plan, seleccione **[!UICONTROL Next]**.

      ![Editar configuración avanzada](../assets/edit-plan-advanced-configuration.png)

      - Se resumen el nombre del plan, el modelo, el intervalo de fechas y el presupuesto total.

      - De forma predeterminada, Mix Modeler calcula automáticamente el promedio de ingresos por conversión utilizando los datos de temporada más recientes. En **[!UICONTROL Average Revenue per conversion]** puede definir un promedio de ingresos por conversión específico.

         1. Para cada intervalo de fechas del presupuesto:
            1. Seleccione un intervalo de fecha en el menú desplegable **[!UICONTROL Date range]**.
            1. Escriba un valor **[!UICONTROL Average revenue]**.

         1. Seleccione ![Agregar círculo](/help/assets/icons/AddCircle.svg) Agregar ingresos promedio personalizados por unidad de conversión para agregar un intervalo de fechas.
         1. Seleccione ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) para quitar un intervalo de fecha.

        >[!NOTE]
        >
        >Si el modelo no incluye datos de ingresos históricos, debe definir un promedio de ingresos por conversión para cada intervalo de fechas especificado para el presupuesto.
        >

      - De forma predeterminada, Mix Modeler calcula automáticamente los costes de canal mediante los datos estacionales históricos más recientes. En **[!UICONTROL Channel costs]** puede definir los costos de canal personalizados.

         1. Para cada canal del modelo, defina el coste de canal personalizado.
            1. Seleccione un canal del menú desplegable **[!UICONTROL Channel]**.
            1. Para cada intervalo de fechas del presupuesto:
               1. Seleccione un intervalo de fecha en el menú desplegable **[!UICONTROL Date range]**.
               1. Escriba un valor **[!UICONTROL Average revenue]**.
            1. Seleccione ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom average revenue per conversion unit]** para agregar un intervalo de fechas.
            1. Seleccione ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) para quitar un intervalo de fecha.

         1. Seleccione ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom channel cost]** para agregar un canal.
         1. Seleccione ![CrossSize400](/help/assets/icons/CrossSize400.svg) para quitar un canal personalizado.


1. Cuando termine de editar su plan, seleccione **[!UICONTROL Edit]**.

   En el cuadro de diálogo **[!UICONTROL All changes are final]**, seleccione **[!UICONTROL OK]** para actualizar la asignación de gasto y las previsiones de retorno de la inversión e ingresos actuales del plan. Seleccione **[!UICONTROL Cancel]** para cancelar la actualización de su plan.

1. Para cancelar las actualizaciones de su plan, seleccione **[!UICONTROL Cancel]**.

   En el cuadro de diálogo **[!UICONTROL No work will be saved]**, seleccione **[!UICONTROL Cancel]** para continuar trabajando en su plan o seleccione **[!UICONTROL OK]** para regresar a la interfaz de Planes.
