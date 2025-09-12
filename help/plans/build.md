---
title: Planes de compilación
description: Obtenga información sobre cómo crear planes en Mix Modeler.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 20985d0f9e9d2990b881ab448f6475e4bb8244d1
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 0%

---


# Planes de compilación

En Mix Modeler, puede crear un plan mediante el asistente de planes. En el asistente de plan, puede configurar los detalles y los presupuestos o las métricas de destino del plan y el modelo subyacente que se utilizará para el plan. Una vez que haya especificado los detalles, el presupuesto, las métricas de objetivo y el modelo, puede seguir adelante con un plan recomendado por IA o editar el gasto por canal. Tiene la opción de definir configuraciones avanzadas en ingresos promedio por conversión y costes de canal.

Debe definir el objetivo con el que desea maximizar el plan. Este objetivo puede ser un presupuesto que se pueda gastar o un objetivo que se quiera lograr. Si el objetivo es un objetivo, además debe especificar valores para que los utilice la métrica de objetivo: conversión, ingresos, CPA o ROI.

Para crear un plan, en la interfaz ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** de Mix Modeler, seleccione **[!UICONTROL Create plan]**.


1. En la pantalla **[!UICONTROL Plan creation]**:

   1. En la sección **[!UICONTROL Setup]**:

      1. Escriba un **[!UICONTROL Plan name]**, por ejemplo `Goal based plan`. Escriba un **[!UICONTROL Description]**, por ejemplo `A goal based plan`.
      1. Seleccionar un(a) **[!UICONTROL Model]** de **[!UICONTROL _Seleccionar una opción.._.]**

         ![Configuración del plan](/help/assets/plan-setup.png)

   1. En la sección **[!UICONTROL Goal]**, seleccione el objetivo hacia el cual desea optimizar su plan. Puede seleccionar entre

      * **[!UICONTROL I have a budget to spend]**

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


      * **[!UICONTROL I have a target to achieve]** [!BADGE Beta]

        ![Destino del plan](../assets/plan-target.png)

         1. En el contenedor **[!UICONTROL Optimize]**
            1. Seleccione una conversión en el menú desplegable **[!UICONTROL Select conversion]**.
            1. Seleccione una métrica de destino en el menú desplegable **[!UICONTROL Select target metric]**. Puede seleccionar entre **[!UICONTROL Conversion]**, **[!UICONTROL CPA]**, **[!UICONTROL Revenue]** o **[!UICONTROL ROI]**.
            1. Seleccione un modelo del menú desplegable **[!UICONTROL Select model]**.
         1. Especifique un Intervalo de fechas, ya sea escribiendo fechas o seleccionando un intervalo de fechas utilizando ![Calendario](/help/assets/icons/Calendar.svg).
         1. Introduzca un valor para la métrica de destino seleccionada. Por ejemplo, un número para **[!UICONTROL Total Conversions]**, un porcentaje para **[!UICONTROL Paid Marketing ROI]** o valores de moneda para **[!UICONTROL Paid Marketing CPA]** y **[!UICONTROL Total Revenue]**.
Para agregar intervalos de fechas adicionales, cada uno con su métrica de destino, seleccione ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.
Para eliminar un intervalo de fechas y la métrica de destino asociada, seleccione ![Cerrar](/help/assets/icons/Close.svg).
         1. Para definir un presupuesto máximo opcional en el que desea restringir el plan:
            1. Activar **[!UICONTROL Maximize budget]**.
            1. Especifique la cantidad del presupuesto máximo.


   1. Seleccione **[!UICONTROL Next]**.

1. En el diálogo **[!UICONTROL Done with all required fields]**:

   ![Plan Finalizado](/help/assets/plan-done-required-fields.png)

   * Seleccione ![NuevoPlan](/help/assets/icons/NewPlan.svg) **[!UICONTROL Create plan now]** si desea generar un plan recomendado por IA con ROI previsto. Seleccione **[!UICONTROL OK]**. Se ha creado su plan.





   * Seleccione ![TableEdit](/help/assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** si desea editar el presupuesto del canal y definir las configuraciones avanzadas antes de crear un plan con el ROI previsto.  Seleccione **[!UICONTROL OK]** para que pueda definir el gasto del canal en **[!UICONTROL Spend selection]** en el paso siguiente.


     >[!IMPORTANT]
     >
     >La siguiente información solo es relevante si ha seleccionado ![TableEdit](/help/assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]**


1. En la sección **[!UICONTROL Spend selection]**, para cada intervalo de fechas del presupuesto, use ![cheurón](/help/assets/icons/ChevronRight.svg) para abrir la vista de distribución de canal para ese intervalo de datos.

   Puede utilizar datos de referencia históricos si desea utilizar datos y perspectivas de gasto de marketing anteriores. Considere los datos de referencia históricos en:

   * Mejore la asignación del presupuesto resaltando los canales de alto rendimiento y los canales con mal rendimiento.
   * Análisis de tendencias de soporte.
   * Identificar estrategias eficaces y evitar errores al configurar los planes.

   Si selecciona un período de referencia histórico, se alineará con las preferencias del patrón de gasto anterior y la funcionalidad de planificación de Mix Modeler podrá generar planes que se ajusten a sus expectativas. Estos planes deberían, en última instancia, mejorar la confianza de las partes interesadas, garantizar que los planes de marketing sean estratégicos y eficientes y que se basen en datos de rendimiento comprobados y en las necesidades empresariales.

   ![Selección de gastos](/help/assets/plan-spend-selection.png)

   1. Seleccione el **[!UICONTROL Spend pattern]**.

      * La opción predeterminada es **[!UICONTROL Automatic]**.
      * Seleccione **[!UICONTROL Historical reference]** e introduzca un **[!UICONTROL Start date]** para hacer referencia a los datos de gastos de marketing anteriores que ya están disponibles para Mix Modeler. El **[!UICONTROL End date]** se determina automáticamente en función del intervalo de fechas para el cual define el patrón de gasto. La fecha de inicio propuesta es la primera fecha de gasto de marketing pasada disponible. Para indicar que ha seleccionado un período de referencia histórico no existente o no válido, verá un ![AlertRed](/help/assets/icons/AlertRed.svg).

   1. Para definir presupuestos para cada canal, escriba un valor para **[!UICONTROL Min]** y **[!UICONTROL Max]** o use los controles deslizantes.

   1. Para alternar entre la entrada de moneda o porcentaje, seleccione **[!UICONTROL $]** o **[!UICONTROL %]** para **[!UICONTROL View spend by]**. Esta opción está desactivada si ha seleccionado métricas de destino que no están basadas en monedas.

   1. Cuando termine, seleccione **[!UICONTROL Create]**.
      ![Selección de gastos](/help/assets/plan-spend-selection.png)

   1. Seleccione **[!UICONTROL Next]**.



1. En la sección **[!UICONTROL Advanced configurations]**, puede especificar configuraciones avanzadas opcionales.

   ![Resumen del plan](../assets/plan-advanced-configurations.png)

   * Se resumen el nombre del plan, el modelo, el intervalo de fechas y el presupuesto total.

   * De forma predeterminada, Mix Modeler calcula automáticamente el promedio de ingresos por conversión utilizando los datos de temporada más recientes. En **[!UICONTROL Average Revenue per conversion]** puede definir un promedio de ingresos por conversión específico.

      1. Para cada intervalo de fechas del presupuesto:

         1. Seleccione un intervalo de fecha en el menú desplegable **[!UICONTROL Date range]**.
         1. Escriba un valor **[!UICONTROL Average revenue]**.

      1. Seleccione ![Agregar círculo](/help/assets/icons/AddCircle.svg) Agregar ingresos promedio personalizados por unidad de conversión para agregar un intervalo de fechas.
      1. Seleccione ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) para quitar un intervalo de fecha.

     >[!NOTE]
     >
     >Si el modelo no incluye datos de ingresos históricos, debe definir un promedio de ingresos por conversión para cada intervalo de fechas especificado para el presupuesto.
     >

   * De forma predeterminada, Mix Modeler calcula automáticamente los costes de canal mediante los datos estacionales históricos más recientes. En **[!UICONTROL Channel costs]** puede definir los costos de canal personalizados.

      1. Para cada canal del modelo, defina un coste de canal personalizado.

         1. Seleccione un canal del menú desplegable **[!UICONTROL Channel]**.
         1. Para cada intervalo de fechas del presupuesto:
            1. Seleccione un intervalo de fecha en el menú desplegable **[!UICONTROL Date range]**.
            1. Escriba un valor **[!UICONTROL Average revenue]**.
         1. Seleccione ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom average revenue per conversion unit]** para agregar un intervalo de fechas.
         1. Seleccione ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) para quitar un intervalo de fecha.

      1. Seleccione ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom channel cost]** para agregar un canal.
      1. Seleccione ![CrossSize400](/help/assets/icons/CrossSize400.svg) para quitar un canal personalizado.


1. Cuando termine, seleccione **[!UICONTROL Create]**.

1. En el cuadro de diálogo **[!UICONTROL Create plan]**, seleccione **[!UICONTROL Create plan]** para crear su plan. Seleccione **[!UICONTROL Cancel]** para cancelar la creación de su plan. Se muestra un cuadro de diálogo **[!UICONTROL No work is saved]** para confirmar.

