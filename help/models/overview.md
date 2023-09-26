---
title: Modelos
description: Aprenda a configurar y utilizar modelos en el Modelador de mezcla de Adobe.
feature: Models
source-git-commit: ac17f5a9fcf036c8e689879578e4b745b789cea3
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---


# Modelos

La funcionalidad de modelo del Modelador de combinación de Adobe le permite configurar, entrenar y puntuar modelos de IA/ML específicos para sus objetivos comerciales y compatibles con el aprendizaje de transferencia impulsado por IA entre la atribución multitáctil y el modelado de combinación de marketing.

Los modelos se basan en los datos armonizados que crea como parte del flujo de trabajo de la aplicación Modelador de mezcla de Adobe.

Para crear un modelo, utilice el flujo de configuración del modelo guiado paso a paso de Mix Modeler, disponible al seleccionar **[!UICONTROL Guide me]**. Consulte [Creación de un modelo](create.md) para obtener más información.

## Administrar modelos

Para ver una tabla de los modelos actuales, en la interfaz del Modelador de mezcla de Adobe:

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
>Esta selección solo está disponible en modelos formados correctamente (modelos con el estado Última ejecución de Correcto).
>

Para ver las perspectivas de un modelo, en la interfaz del Modelador de mezcla de Adobe:

1. Seleccionar ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** desde el carril izquierdo.

1. Seleccione el nombre de un modelo con una **[!UICONTROL Last run status]** de <span style="color:green">●</span> **[!UICONTROL Success]** desde el **[!UICONTROL Models]** tabla

1. En el menú contextual, seleccione **[!UICONTROL Model Insights]**. Se le redirigirá a [Datos del modelo](insights.md).


