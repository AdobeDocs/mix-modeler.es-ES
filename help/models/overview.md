---
title: Modelos
description: Aprenda a configurar y utilizar modelos en Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: f445cb2b1ec04ffe9247e858c048587802bffe9c
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Modelos

La funcionalidad de modelo de Mix Modeler le permite configurar, entrenar y puntuar modelos de IA/ML específicos para sus objetivos comerciales y compatibles con el aprendizaje de transferencia impulsado por IA entre la atribución multitáctil y el modelado de combinación de marketing.

Los modelos se basan en los datos armonizados que crea como parte del flujo de trabajo de la solicitud de Mix Modeler.

Un modelo en Mix Modeler es un modelo de aprendizaje automático empleado para medir y/o predecir un resultado específico basado en las inversiones de un experto en marketing. Se pueden utilizar puntos de contacto de marketing y datos de nivel de resumen como entrada. Mix Modeler le permite crear variantes de modelos basadas en diferentes conjuntos de variables, dimensiones y resultados, como ingresos, unidades vendidas o posibles clientes.

Un modelo requiere:

* una conversión,
* uno o más puntos de contacto de marketing (canales) compuestos de datos de nivel de resumen, datos de punto de contacto de marketing (datos de evento) o ambos,
* una ventana retrospectiva configurable para
* una ventana de formación configurable.

Un modelo puede incluir de forma opcional:

* factores externos,
* factores internos,
* los denominados &quot;precedentes&quot; (distribución de probabilidad que representa el conocimiento o la incertidumbre de los datos antes o antes de observarlos), que indexan las conversiones anteriores por canal,
* porcentaje de gasto, que utiliza el porcentaje de gasto relativo como proxy cuando los datos de marketing son escasos.


## Creación de un modelo

Para crear un modelo, utilice el flujo de configuración del modelo guiado paso a paso del Mix Modeler disponible al seleccionar **[!UICONTROL Guide me]**. Consulte [Creación de un modelo](create.md) para obtener más información.

## Administrar modelos

Para ver una tabla de los modelos actuales, en la interfaz del Mix Modeler:

1. Seleccionar ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** desde el carril izquierdo.

1. Verá una tabla de los modelos actuales.

   Las columnas de la tabla especifican detalles sobre el modelo.

   | Nombre de columna | Detalles |
   |---|---|
   | Nombre | Nombre del modelo |
   | Descripción | Descripción del modelo |
   | Eventos de conversión | La conversión que ha seleccionado para el modelo. |
   | Conjunto de datos | El conjunto de datos que el modelo utiliza para entrenar y puntuar. Este es de forma predeterminada el conjunto de datos armonizado. |
   | Frecuencia de ejecución | Frecuencia de ejecución del aprendizaje del modelo. |
   | Última ejecución | La fecha y hora de la última formación del modelo. |
   | Último estado de ejecución | El estado de la última ejecución de la formación del modelo. <br/><span style="color:green">●</span> Correcto<br/><span style="color:orange">●</span> Problema de formación<br/> <span style="color:orange">●</span> Esperando formación <br/><span style="color:red">●</span> Error |

   {style="table-layout:auto"}

1. Para cambiar las columnas mostradas en la lista, seleccione ![Configuración de columna](../assets/icons/ColumnSetting.svg) y activar las columnas ![Marque](../assets/icons/Checkmark.svg) o apagada.

### Eliminación de un modelo

Para eliminar un modelo:

1. Seleccione el nombre del modelo que desea eliminar.

1. En el menú contextual, seleccione **[!UICONTROL Delete]** para eliminar el modelo.

### Ver detalles de un modelo

Para ver más detalles de un modelo:

1. Seleccione el nombre del modelo del que desea ver más detalles.

1. En el menú contextual, seleccione **[!UICONTROL More]**. Verá los detalles del modelo seleccionado en el panel derecho.



### Datos del modelo

>[!NOTE]
>
>Esta selección solo está disponible en modelos formados correctamente.
>

Para ver las perspectivas de un modelo, en la interfaz del Mix Modeler:

1. Seleccionar ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** desde el carril izquierdo.

1. Seleccione el nombre de un modelo con una **[!UICONTROL Last run status]** de <span style="color:green">●</span> **[!UICONTROL Success]** desde el **[!UICONTROL Models]** tabla.

1. En el menú contextual, seleccione **[!UICONTROL Model Insights]**. Se le redirigirá a [Datos del modelo](insights.md).
