---
title: Resumen de planes
description: Obtenga información sobre cómo ver, seleccionar y actuar sobre planes en Mix Modeler.
feature: Plans
exl-id: 45a8dc30-3259-493d-8ea5-1899903733a6
source-git-commit: f0871834ec665c907caf0af3edeeed4fb2549a58
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Resumen de planes

Los planes de Mix Modeler le permiten asignar presupuestos por unidad de negocio y canal. La funcionalidad de planificación está integrada con los resultados de los modelos formados en función de los datos armonizados.

Un plan describe las inversiones discrecionales (por ejemplo, presupuestos) que una empresa tiene la intención de gastar en proyectos relacionados con el marketing durante un periodo de tiempo determinado. Estas inversiones están al servicio de KPI comunes (por ejemplo, pedidos, ingresos). Los planes pueden incluir gastos de canales como publicidad de pago, contenido web patrocinado, eventos.

Un plan requiere:

- un modelo,
- un intervalo de datos,
- un presupuesto.

Un plan puede incluir de forma opcional:

- una ventana de reconocimiento configurada,
- varias fechas de vuelo, cada una con un presupuesto objetivo,
- restricciones de presupuesto mínimas y máximas por canal y fecha de vuelo.

Si un modelo que ha utilizado para su plan recibe una puntuación con los nuevos datos, debe crear un nuevo plan para tener en cuenta los datos que se han vuelto a puntuar.


## Planes de compilación

Para crear un plan, utilice el asistente de creación de planes de Mix Modeler. Consulte [Planes de compilación](build.md) para obtener más información.


## Administrar planes

Para ver una tabla de sus planes actuales, en la interfaz de Mix Modeler:

1. Seleccione ![](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** en el carril izquierdo.

1. Verá una tabla de los planes actuales y su estado.

   Las columnas de la tabla especifican detalles sobre los planes.

   | Nombre de columna | Detalles |
   |---|---|
   | Nombre | Nombre del plan |
   | Modelo | El modelo utilizado como base para el plan. |
   | Intervalo de fechas | Intervalo de fechas completo de un plan. |
   | Presupuesto | Presupuesto total de un plan. |
   | Destino del plan | La métrica de destino definida para un plan basado en destino. |
   | Retorno previsto | [regreso previsto](/help/main-guide/glossary.md) para un plan |
   | ROI previsto | El [ROI previsto](/help/main-guide/glossary.md) para un plan. |
   | Conversión prevista | [conversión prevista](/help/main-guide/glossary.md) para un plan |
   | CPA previsto | El [CPA previsto](/help/main-guide/glossary.md) para un plan |
   | Estado | El estado de un plan: <p><span style="color:red">●</span> con error, <p><span style="color:blue">●</span> Procesando, o <p><span style="color:green">●</span> completado. |

   {style="table-layout:auto"}

   Puede usar ![ColumnSetting](/help/assets/icons/ColumnSetting.svg) para seleccionar ![Marca de verificación](/help/assets/icons/Checkmark.svg) las columnas que se mostrarán en la tabla.

1. Use ![Buscar](/help/assets/icons/Search.svg) para buscar y filtrar la tabla de uno o más planes específicos.

### Perspectivas del plan

Para ver las perspectivas de un plan y editar un plan:

1. Seleccione ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** del carril izquierdo.

1. Seleccione el nombre del plan.

Se le redirigirá a [Información sobre el plan](insights.md).


### Duplicación de un plan

Para duplicar un plan:

- Seleccione ![Más](/help/assets/icons/More.svg) para un plan. En el menú contextual, seleccione **[!UICONTROL Duplicate]**.
- También puede seleccionar un plan en la tabla ![SelectBox](/help/assets/icons/SelectBox.svg) y seleccionar ![Copiar](/help/assets/icons/Copy.svg) **[!UICONTROL Duplicate]** en la barra de acciones azul.

Se crea un nuevo plan, con un nombre compuesto por el nombre del plan original anexado con **[!UICONTROL (Copy)] (_n_)**. Se le redirigirá automáticamente a [Creación de plan](build.md) para proporcionar detalles actualizados para el plan copiado.

- Los detalles (como la descripción, el presupuesto, etc.) del plan original se copian.
- Las restricciones presupuestarias del plan original se copian en el plan recién creado.
- Tiene la opción de seleccionar otro modelo como base para el plan copiado.
   - En el caso de los puntos de contacto o canales que no existen en el plan copiado, pero que no existen en el modelo recién seleccionado, cualquier restricción para estos puntos de contacto o canales se elimina del plan.
   - Para los puntos de contacto o canales que no existen en el plan copiado, pero sí en el modelo recién seleccionado, las restricciones se definen como:
      - un valor mínimo de `0`,
      - un valor máximo en línea con el presupuesto del intervalo de vuelo del plan.



### Comparar planes

Para comparar planes:

1. Seleccione dos planes de la tabla.
1. Seleccione ![Comparar](/help/assets/icons/Compare.svg) **[!UICONTROL Compare]** de la barra de acciones azul. Verá la interfaz de usuario de **[!UICONTROL Compare plans]**.


### Eliminar planes

Para suprimir un plan:

1. Seleccione ![Más](/help/assets/icons/More.svg) para un plan. En el menú contextual, seleccione **[!UICONTROL Delete]**. <br/>También puede seleccionar un plan en la tabla ![SelectBox](/help/assets/icons/SelectBox.svg) y seleccionar ![Delete](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** de la barra de acciones azul.
1. Seleccione **[!UICONTROL Delete]** en el cuadro de diálogo de confirmación **[!UICONTROL Delete plan]** para eliminar el plan. Seleccione **[!UICONTROL Cancel]** para cancelar.

Para eliminar varios planes:

1. Seleccione varios planes.
1. En la barra de acciones azul, seleccione ![Eliminar](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** para eliminar los planes.
1. Seleccione **[!UICONTROL Delete]** en el cuadro de diálogo de confirmación de **[!UICONTROL Delete *x *planes]**&#x200B;para eliminar los planes. Seleccione **[!UICONTROL Cancel]**&#x200B;para cancelar.


