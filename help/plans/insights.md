---
title: Perspectivas del plan
description: Obtenga información sobre cómo ver información sobre su plan y editar un plan en Mix Modeler.
feature: Plans
exl-id: 91385595-284f-4fcb-b54b-9539905e552b
source-git-commit: 86b58717c3c8be183c70d1ceccf6f7c757303518
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 0%

---

# Perspectivas del plan


En [!UICONTROL Plan insights], se crean las perspectivas del plan, que muestran [!UICONTROL Model], [!UICONTROL Data range] y [!UICONTROL Plan target] en los que se basa el plan.


Cuando se crean las perspectivas, verá una descripción general de su plan, que consta de:

- Encabezado que muestra [!UICONTROL Model], [!UICONTROL Data range] y [!UICONTROL Plan target] en los que se basa el plan.
   - Si ha definido un plan basado en objetivos, un distintivo indica el estado del objetivo. Las opciones posibles son:

      - [!BADGE Objetivo alcanzable]{type=Positive}
      - [!BADGE Destino inalcanzable]{type=Negative}

   - Seleccione ![ChevronDown](/help/assets/icons/ChevronDown.svg) **[!UICONTROL Show more]** para mostrar más detalles.

- [Visualización [!UICONTROL Forecasted paid channel ROI]](#forecasted-paid-channel-spend-and-roi)
- [Visualización [!UICONTROL Forecasted revenue]](#forecasted-revenue)
- [Visualización [!UICONTROL Forecasted conversion]](#forecasted-conversions)
- [Visualización [!UICONTROL Marginal channel return]](#marginal-channel-return)
- [[!UICONTROL Data range breakdown] tabla del plan](#date-range-breakdown), mostrando columnas para

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

Esta visualización de gráfico de líneas muestra una curva de retorno marginal para el canal seleccionado con indicadores para **[!UICONTROL Marginal break-even]** y **[!UICONTROL Return point]**. Esta visualización le ayuda a comprender cómo se gasta un canal al alcanzar un punto de equilibrio marginal. Y si tiene espacio para aumentar el gasto en un canal o si debe gastar menos en un canal para mejorar la eficiencia del gasto en el canal.

![Visualización de retorno de canal marginal](../assets/overview-plan-marginal-channel-return.png)

Para seleccionar un canal específico para la visualización, seleccione un canal del menú desplegable **[!UICONTROL View]**.

## Sinergias de canal

La matriz de sinergias de canal le ayuda a identificar cómo interactúan los canales de marketing para crear efectos multiplicativos, más allá de sus contribuciones individuales.

![Planificar sinergias de canales](/help/assets/plan-channel-synergies.png)

Para descargar un archivo CSV que represente la matriz, seleccione ![Descargar](/help/assets/icons/Download.svg) **[!UICONTROL Download]**.

## Desglose del intervalo de fechas

La tabla [!UICONTROL Date range breakdown] muestra datos granulares detallados por canal para [!UICONTROL ROI], [!UICONTROL Revenue], [!UICONTROL CPA], [!UICONTROL Conversions] y [!UICONTROL Spend].

![Tabla de desglose de intervalos de fechas](../assets/overview-plan-date-range-breakdown.png)

1. Para descargar un archivo CSV que contenga los datos del desglose Intervalo de fechas, seleccione ![Descargar](/help/assets/icons/Download.svg) **[!UICONTROL Download CSV]**. En el menú contextual:

   - Seleccione ![Descargar](/help/assets/icons/Download.svg) **[!UICONTROL Detailed CSV]** para obtener datos detallados en formato CSV.
   - Seleccione ![Descargar](/help/assets/icons/Download.svg) **[!UICONTROL Summary CSV]** para ver los datos de resumen en formato CSV.

   Los datos detallados son datos granulares tecleados por semana. Los datos de resumen son datos introducidos por el intervalo de fechas proporcionado por el modelo.

1. Para ver el desglose Intervalo de fecha por categoría de canales, seleccione **[!UICONTROL All channels]**, **[!UICONTROL Paid channels]** o **[!UICONTROL Non-paid channels]** de la selección **[!UICONTROL View]**.


## Editar plan

Para editar tu plan, selecciona ![Editar](/help/assets/icons/Edit.svg) **[!UICONTROL Edit plan]**.

1. En la sección **[!UICONTROL Spend selection]**, para cada intervalo de fechas del presupuesto, use ![cheurón](/help/assets/icons/ChevronRight.svg) para abrir la vista de distribución de canal para ese intervalo de datos.

   Puede utilizar datos de referencia históricos si desea utilizar datos y perspectivas de gasto de marketing anteriores. Considere los datos de referencia históricos en:

   - Mejore la asignación del presupuesto resaltando los canales de alto rendimiento y los canales con mal rendimiento.
   - Análisis de tendencias de soporte.
   - Identificar estrategias eficaces y evitar errores al configurar los planes.

   Si selecciona un período de referencia histórico, se alineará con las preferencias del patrón de gasto anterior y la funcionalidad de planificación de Mix Modeler podrá generar planes que se ajusten a sus expectativas. Estos planes deberían, en última instancia, mejorar la confianza de las partes interesadas, garantizar que los planes de marketing sean estratégicos y eficientes y que se basen en datos de rendimiento comprobados y en las necesidades empresariales.

   ![Selección de gastos](/help/assets/plan-spend-selection.png)

   1. Seleccione el **[!UICONTROL Spend pattern]**.

      - La opción predeterminada es **[!UICONTROL Automatic]**.
      - Seleccione **[!UICONTROL Historical reference]** e introduzca un **[!UICONTROL Start date]** para hacer referencia a los datos de gastos de marketing anteriores que ya están disponibles para Mix Modeler. **[!UICONTROL End date]** se determina automáticamente en función del intervalo de datos seleccionado. La fecha de inicio propuesta es la primera vez que hay datos disponibles sobre el gasto en marketing anterior. Para indicar que ha seleccionado un período de referencia histórico no existente, verá ![AlertRed](/help/assets/icons/AlertRed.svg).


   1. Para modificar los presupuestos de cada canal, modifique los valores de **[!UICONTROL Min]** y **[!UICONTROL Max]** o use los controles deslizantes.

   1. Para alternar entre la entrada de moneda o porcentaje, seleccione **[!UICONTROL $]** o **[!UICONTROL %]** para **[!UICONTROL View spend by]**.

   1. Para editar los detalles de su plan, seleccione **[!UICONTROL Edit details]**:

      1. En la sección **[!UICONTROL Setup]**:

         1. Escriba un **[!UICONTROL Plan name]**, por ejemplo `Demo plan`. Escriba un **[!UICONTROL Description]**, por ejemplo `Demo plan for Luma company`.
         1. Seleccionar un(a) **[!UICONTROL Model]** de **[!UICONTROL _Seleccionar una opción.._.]**

            ![Configuración del plan](/help/assets/plan-setup.png)

      1. En la sección **[!UICONTROL Goal]**, seleccione el objetivo hacia el cual desea optimizar su plan. Puede seleccionar entre
         - **[!UICONTROL I have a budget to spend]**

           ![Presupuesto del plan](../assets/plan-budget.png)

           Esta opción le permite introducir presupuestos para uno o más intervalos de fechas.

            1. En el contenedor **[!UICONTROL Optimize]**:
               1. Seleccione una conversión en el menú desplegable **[!UICONTROL Select conversion]**.
               1. Seleccione un modelo del menú desplegable **[!UICONTROL Select model]**.
            1. Especifique un **[!UICONTROL Date range]**, ya sea escribiendo fechas o seleccionando un intervalo de fechas utilizando ![Calendario](/help/assets/icons/Calendar.svg).
            1. Escriba un **[!UICONTROL Budget]**.
Para agregar intervalos de fechas adicionales, cada uno con su presupuesto, seleccione ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.
Para eliminar un intervalo de fechas y un presupuesto asociado, seleccione ![Cerrar](/help/assets/icons/Close.svg).
            1. Para definir un presupuesto máximo opcional en el que desea restringir el plan:
               1. Activar **[!UICONTROL Maximize budget]**.
               1. Especifique la cantidad del presupuesto máximo. El importe debe ser igual o superior al importe total de los presupuestos especificados para los intervalos de fechas.


         - **[!UICONTROL I have a target to achieve]** [!BADGE Beta]

           ![Destino del plan](../assets/plan-target.png)

            1. En el contenedor **[!UICONTROL Optimize]**
               1. Seleccione una conversión en el menú desplegable **[!UICONTROL Select conversion]**.
               1. Seleccione una métrica de destino en el menú desplegable **[!UICONTROL Select target metric]**. Puede seleccionar entre **[!UICONTROL Conversion]**, **[!UICONTROL CPA]**, **[!UICONTROL Revenue]** o **[!UICONTROL ROI]**.
               1. Seleccione un modelo del menú desplegable **[!UICONTROL Select model]**.
            1. Especifique un Intervalo de fechas, ya sea escribiendo fechas o seleccionando un intervalo de fechas utilizando ![Calendario](/help/assets/icons/Calendar.svg).
            1. Introduzca un valor para la métrica de destino seleccionada. Por ejemplo, un número para **[!UICONTROL Conversion]**, un porcentaje para **[!UICONTROL ROI]** o valores de moneda para **[!UICONTROL CPA]** y **[!UICONTROL Revenue]**.
Para agregar intervalos de fechas adicionales, cada uno con su métrica de destino, seleccione ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.
Para eliminar un intervalo de fechas y la métrica de destino asociada, seleccione ![Cerrar](/help/assets/icons/Close.svg).
            1. Para definir un presupuesto máximo opcional en el que desea restringir el plan:
               1. Activar **[!UICONTROL Maximize budget]**.
               1. Especifique la cantidad del presupuesto máximo.

         1. Seleccione **[!UICONTROL Next]** para volver a la sección **[!UICONTROL Spend selection]**.

1. En la sección **[!UICONTROL Advanced configuration]**:

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


1. Cuando haya terminado de editar su plan, seleccione **[!UICONTROL Edit]**.

   En el cuadro de diálogo **[!UICONTROL All changes are final]**, seleccione **[!UICONTROL OK]** para actualizar la asignación de gasto y las previsiones de retorno de la inversión e ingresos actuales del plan. Seleccione **[!UICONTROL Cancel]** para cancelar la actualización de su plan.


- Para cancelar las actualizaciones de tu plan en cualquier momento, selecciona **[!UICONTROL Cancel]**. En el cuadro de diálogo **[!UICONTROL No work will be saved]**, seleccione **[!UICONTROL Cancel]** para continuar trabajando en su plan o seleccione **[!UICONTROL OK]** para regresar a la interfaz de Planes.
- Para volver al asistente, seleccione **[!UICONTROL Back]**.
