---
title: Planes de compilación
description: Obtenga información sobre cómo crear planes en Mix Modeler.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 3545a7045478108db4d9f6bb87df679bfede5a45
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 0%

---


# Planes de compilación

En Mix Modeler, se crea un plan utilizando el lienzo de plan. En el lienzo del plan, puede configurar los detalles y presupuestos del plan y el modelo subyacente que se utilizará para el plan. Una vez que haya especificado los detalles, el presupuesto y el modelo, puede seguir adelante con un plan recomendado por IA o editar el gasto por canal.

Para crear un plan, en la interfaz ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** de Mix Modeler, seleccione **[!UICONTROL Create plan]**.


1. En la pantalla **[!UICONTROL Plan creation]**:

   1. En la sección **[!UICONTROL Setup]**:

      1. Escriba un **[!UICONTROL Plan name]**, por ejemplo `Demo plan`. Escriba un **[!UICONTROL Description]**, por ejemplo `Demo plan for Luma company`.
      1. Seleccionar un(a) **[!UICONTROL Model]** de **[!UICONTROL _Seleccionar una opción.._.]**
      1. Puede seleccionar ![LinkOut](/help/assets/icons/LinkOut.svg) **[!UICONTROL Create model]** para crear un modelo directamente desde la creación del plan. Se abrirá una nueva ficha en el explorador y se mostrará la interfaz de [Modelos](../models/overview.md).

         ![Configuración del plan](/help/assets/plan-setup.png)

   1. En la sección **[!UICONTROL Budget]**:

      1. Especifique un intervalo de fechas, ya sea escribiendo fechas o seleccionando un intervalo de fechas utilizando ![Calendario](/help/assets/icons/Calendar.svg).
      1. Introduzca un presupuesto.

      Para agregar intervalos de fechas adicionales, cada uno con su presupuesto, seleccione ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

      Para eliminar un intervalo de fechas y un presupuesto asociado, seleccione ![Cerrar](/help/assets/icons/Close.svg).

      Para definir un presupuesto máximo especificado:

      1. Activar **[!UICONTROL Maximize budget]**.
      1. Especifique la cantidad de presupuesto máximo. La cantidad debe ser igual o superior a la cantidad total de presupuestos especificados para los intervalos de fechas.

         ![Presupuesto del plan](/help/assets/plan-budget.png)

   1. Seleccione **[!UICONTROL Next]**.

1. En el diálogo **[!UICONTROL Done with all required fields]**:

   ![Plan Finalizado](/help/assets/plan-done-required-fields.png)

   * Seleccione ![NuevoPlan](../assets/icons/NewPlan.svg) **[!UICONTROL Create plan now]** si desea generar un plan recomendado por IA con ROI previsto.

     Seleccione **[!UICONTROL OK]**. Se ha creado su plan.


   * Seleccione ![TableEdit](/help/assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** si desea editar el presupuesto del canal y definir las configuraciones avanzadas antes de crear un plan con el ROI previsto.

     Seleccione **[!UICONTROL OK]** para que pueda definir el gasto del canal en **[!UICONTROL Spend selection]** en el paso siguiente.



1. En la sección **[!UICONTROL Spend selection]**, para cada intervalo de fechas del presupuesto, use las ![comillas angulares](/help/assets/icons/ChevronRight.svg) para abrir la vista de distribución de canal para ese intervalo de datos.

   1. Para definir presupuestos para cada canal, escriba un valor para **[!UICONTROL Min]** y **[!UICONTROL Max]** o use los controles deslizantes.

   1. Para alternar entre la entrada de moneda o porcentaje, seleccione **[!UICONTROL $]** o **[!UICONTROL %]** para **[!UICONTROL View spend by]**.

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

      1. Para cada canal del modelo, defina el coste de canal personalizado.

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

