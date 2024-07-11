---
title: Creación de un plan
description: Obtenga información sobre cómo crear un plan en Mix Modeler.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---


# Creación de un plan

En Mix Modeler, se crea un plan utilizando el lienzo de plan. En el lienzo del plan, puede configurar los detalles y presupuestos del plan y el modelo subyacente que se utilizará para el plan. Una vez que haya especificado los detalles, el presupuesto y el modelo, puede seguir adelante con un plan recomendado por IA o editar el gasto por canal.

Para crear un plan, en la ![PLan](/help/assets//icons/FileChart.svg) **[!UICONTROL Plans]** interfaz en Mix Modeler, seleccione **[!UICONTROL Open plan canvas]**.

1. En la pantalla de creación del Plan:

   1. En el **[!UICONTROL Setup]** sección

      1. Introduzca una **[!UICONTROL Plan name]**, por ejemplo `Demo plan`. Introduzca una **[!UICONTROL Description]**, por ejemplo `Demo plan for Luma company`.
      1. Seleccione una **[!UICONTROL Model]** de **[!UICONTROL _Seleccione una opción.._.]**.
      1. Puede seleccionar ![LinkOut](/help/assets//icons/LinkOut.svg) **[!UICONTROL Create model]** para crear un modelo directamente desde la creación del plan. Se abrirá una nueva pestaña en el navegador y se mostrará la [Modelos](../models/overview.md) interfaz.

         ![Configuración del plan](/help/assets//plan-setup.png)

   1. En el **[!UICONTROL Budget]** sección:

      1. Especifique un intervalo de fechas, ya sea escribiendo fechas o seleccionando un intervalo de fechas utilizando ![Calendario](/help/assets//icons/Calendar.svg).
      1. Introduzca un presupuesto.

      Para añadir intervalos de fechas adicionales, cada uno con su presupuesto, seleccione ![CalendarAdd](/help/assets//icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

      Para eliminar un intervalo de fechas y un presupuesto asociado, seleccione ![Cerrar](/help/assets//icons/Close.svg).

      Para definir un presupuesto máximo especificado:

      1. Cambiar **[!UICONTROL Maximize budget]** en.
      1. Especifique la cantidad de presupuesto máximo. La cantidad debe ser igual o superior a la cantidad total de presupuestos especificados para los intervalos de fechas.

         ![Presupuesto del plan](/help/assets//plan-budget.png)

   1. Seleccione **[!UICONTROL Next]**.

1. En el **[!UICONTROL Done with all required fields]** diálogo:

   ![Plan finalizado](/help/assets//plan-done-required-fields.png)

   * Seleccionar <img src="/help/assets//icons/NewPlan.svg" width="25" /> **[!UICONTROL Create plan now]** si desea generar un plan recomendado por IA con ROI previsto.

     Seleccionar **[!UICONTROL OK]**. Se ha creado su plan.


   * Seleccionar ![TableEdit](/help/assets//icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** si desea editar el presupuesto del canal antes de crear un plan con el ROI previsto.

     Seleccionar **[!UICONTROL OK]**, para que pueda definir el gasto del canal en **[!UICONTROL Spend selection]** en el paso siguiente.



1. En el **[!UICONTROL Spend selection]** , para cada intervalo de fechas del presupuesto, utilice el ![cheurón](/help/assets//icons/ChevronRight.svg) arriba, abra la vista distribución de canales para ese rango de datos.

   1. Para definir presupuestos para cada canal, introduzca un valor para **[!UICONTROL Min]** y **[!UICONTROL Max]** o utilice los controles deslizantes.

   1. Para alternar entre la entrada de moneda o porcentaje, seleccione **[!UICONTROL $]** o **[!UICONTROL %]** para **[!UICONTROL View spend by]**.

      ![Selección de gasto](/help/assets//plan-spend-selection.png)

   1. Cuando termine, seleccione **[!UICONTROL Create]**.

   1. En el **[!UICONTROL Create plan]** diálogo, seleccione **[!UICONTROL Create plan]** para crear su plan. Seleccionar **[!UICONTROL Cancel]** para cancelar la creación de su plan. A **[!UICONTROL No work is saved]** El cuadro de diálogo se muestra para confirmar.
