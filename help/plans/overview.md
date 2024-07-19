---
title: Planes
description: Obtenga información sobre cómo ver, seleccionar y actuar sobre planes en Mix Modeler.
feature: Plans
exl-id: 45a8dc30-3259-493d-8ea5-1899903733a6
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# Planes

Los planes de Mix Modeler le permiten asignar presupuestos por unidad de negocio y canal. La funcionalidad de planificación está integrada con los resultados de los modelos formados en función de los datos armonizados.

Un plan describe las inversiones discrecionales (por ejemplo, presupuestos) que una empresa tiene la intención de gastar en proyectos relacionados con el marketing a lo largo de un periodo de tiempo determinado en servicio de un KPI común (por ejemplo, pedidos, ingresos). Los planes pueden incluir gastos de canales como publicidad de pago, contenido web patrocinado, eventos.

Un plan requiere:

- un modelo,
- un intervalo de datos,
- un presupuesto.

Un plan puede incluir de forma opcional:

- una ventana de reconocimiento configurada,
- varias fechas de vuelo, cada una con un presupuesto objetivo,
- restricciones de presupuesto mínimas y máximas por canal y fecha de vuelo.


## Administrar planes

Para ver una tabla de sus planes actuales, en la interfaz del Mix Modeler:

1. Seleccione ![](/help/assets//icons/FileChart.svg) **[!UICONTROL Plans]** en el carril izquierdo.

1. Verá una tabla de los planes actuales y su estado.

   Las columnas de la tabla especifican detalles sobre los planes.

   | Nombre de columna | Detalles |
   |---|---|
   | Nombre | Nombre del plan |
   | Modelo | El modelo utilizado como base para el plan. |
   | Intervalo de fechas | Intervalo de fechas completo de un plan. |
   | Presupuesto | Presupuesto total de un plan. |
   | Retorno previsto | El rendimiento previsto de un plan |
   | ROI previsto | El ROI previsto de un plan. |
   | Estado | El estado de un plan: <p>Error de <span style="color:red">●</span>, <p><span style="color:blue">●</span> Procesando o <p><span style="color:green">●</span> completado. |

   {style="table-layout:auto"}

1. Use ![Buscar](/help/assets//icons/Search.svg) para buscar y filtrar la tabla de uno o más planes específicos.

## Creación de un plan

Para crear un plan, utilice el asistente de creación de planes de Mix Modeler. Consulte [Crear un plan](create.md) para obtener más información.


## Edición de un plan

Para editar un plan, seleccione su nombre en la tabla. Consulte [Editar un plan](edit.md) para obtener más información.


## Selección y acción de planes

Puede seleccionar uno o varios planes, lo que muestra la barra de acciones Planes. La barra de acciones permite eliminar, comparar o duplicar planes.

Para quitar todas las selecciones de la tabla Planes, seleccione ![Cerrar](/help/assets//icons/Close.svg) en la barra de acciones

![Planes de barra de acciones](/help/assets//plans-action-bar.png)

### Duplicación de un plan

Para duplicar un plan:

1. Seleccione un solo plan de la tabla.
1. Seleccione ![Copiar](/help/assets//icons/Copy.svg) **[!UICONTROL Duplicate]** de la barra de acciones. Un nuevo plan, con un nombre compuesto por el nombre del plan original anexado con **[!UICONTROL (Copy)]**, se agrega en la parte superior de la tabla.

Alternativamente:

1. Seleccione ![Más](/help/assets//icons/More.svg) para un plan de la tabla.
1. Seleccione **[!UICONTROL Duplicate]** del menú contextual. Un nuevo plan, con un nombre compuesto por el nombre del plan original anexado con **[!UICONTROL (Copy)]**, se agrega en la parte superior de la tabla.

### Comparar planes

Para comparar planes:

1. Seleccione dos planes de la tabla.
1. Seleccione ![Comparar](/help/assets//icons/Compare.svg) **[!UICONTROL Compare]** de la barra de acciones. Verá la interfaz de usuario de **[!UICONTROL Compare plans]**.


### Eliminar planes

Para suprimir planes:

1. Seleccione uno o más planes de la tabla.
1. Seleccione ![Eliminar](/help/assets//icons/Delete.svg) **[!UICONTROL Delete]** de la barra de acciones.

Alternativamente:

1. Seleccione ![Más](/help/assets//icons/More.svg) para un plan de la tabla.
1. Seleccione **[!UICONTROL Delete]** del menú contextual. Un nuevo plan, con un nombre compuesto por el nombre del plan original anexado con **[!UICONTROL (Copy)]**, se agrega en la parte superior de la tabla.

   >[!WARNING]
   >
   >   Los planes seleccionados se eliminan inmediatamente.
