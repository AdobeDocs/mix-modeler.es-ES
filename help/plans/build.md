---
title: Planes de compilación
description: Obtenga información sobre cómo crear planes en Mix Modeler.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: f12eea7454d1c81b347dc4960f5c491d81725f7d
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---


# Planes de compilación

En Mix Modeler, se crea un plan utilizando el lienzo de plan. En el lienzo del plan, puede configurar los detalles y presupuestos del plan y el modelo subyacente que se utilizará para el plan. Una vez que haya especificado los detalles, el presupuesto y el modelo, puede seguir adelante con un plan recomendado por IA o editar el gasto por canal.

Para crear un plan, en la interfaz ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** del Mix Modeler, seleccione **[!UICONTROL Create plan]**.

1. En la pantalla de creación del Plan:

   1. En la sección **[!UICONTROL Setup]**

      1. Escriba un **[!UICONTROL Plan name]**, por ejemplo `Demo plan`. Escriba un **[!UICONTROL Description]**, por ejemplo `Demo plan for Luma company`.
      1. Seleccionar un(a) **[!UICONTROL Model]** de **[!UICONTROL _Seleccionar una opción.._.]**.
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

   * Seleccionar <img src="/help/assets/icons/NewPlan.svg" width="25" /> **[!UICONTROL Create plan now]** si desea generar un plan recomendado por IA con ROI pronosticado.

     Seleccione **[!UICONTROL OK]**. Se ha creado su plan.


   * Seleccione ![TableEdit](/help/assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** si desea editar el presupuesto del canal antes de crear un plan con el retorno de la inversión previsto.

     Seleccione **[!UICONTROL OK]** para que pueda definir el gasto del canal en **[!UICONTROL Spend selection]** en el paso siguiente.



1. En la sección **[!UICONTROL Spend selection]**, para cada intervalo de fechas del presupuesto, use las ![comillas angulares](/help/assets/icons/ChevronRight.svg) para abrir la vista de distribución de canal para ese intervalo de datos.

   1. Para definir presupuestos para cada canal, escriba un valor para **[!UICONTROL Min]** y **[!UICONTROL Max]** o use los controles deslizantes.

   1. Para alternar entre la entrada de moneda o porcentaje, seleccione **[!UICONTROL $]** o **[!UICONTROL %]** para **[!UICONTROL View spend by]**.

      ![Selección de gastos](/help/assets/plan-spend-selection.png)

   1. Cuando termine, seleccione **[!UICONTROL Create]**.

   1. En el cuadro de diálogo **[!UICONTROL Create plan]**, seleccione **[!UICONTROL Create plan]** para crear su plan. Seleccione **[!UICONTROL Cancel]** para cancelar la creación de su plan. Se muestra un cuadro de diálogo **[!UICONTROL No work is saved]** para confirmar.
