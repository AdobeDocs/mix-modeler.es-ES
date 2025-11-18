---
title: Información general de modelos
description: Aprenda a crear y utilizar modelos en Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 1a9df9f9819d9e0031e58443ec6a9e755a151ba0
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 0%

---

# Información general de modelos

La funcionalidad de modelo de Mix Modeler le permite configurar, entrenar y puntuar modelos específicos para sus objetivos comerciales. La formación y la puntuación admiten el aprendizaje de transferencia impulsado por IA entre la atribución multitáctil y el modelado de combinación de marketing.

Los modelos se basan en los datos armonizados que crea como parte del flujo de trabajo de la aplicación Mix Modeler.

Un modelo en Mix Modeler es un modelo de aprendizaje automático empleado para medir y predecir un resultado especificado en función de las inversiones de un experto en marketing. Se pueden utilizar puntos de contacto de marketing y datos de nivel de resumen como entrada. Mix Modeler le permite crear variantes de modelos basadas en diferentes conjuntos de variables, dimensiones y resultados, como ingresos, unidades vendidas o posibles clientes.

Un modelo requiere:

* Una conversión.
* Uno o más puntos de contacto de marketing (canales) compuestos de datos de nivel de resumen, datos de punto de contacto de marketing (datos de evento) o ambos.
* Una ventana retrospectiva configurable.
* Una ventana de formación configurable.

Un modelo puede incluir de forma opcional:

* Factores externos.
* Factores internos.
* Conocimiento previo de las contribuciones de marketing de otras fuentes, como la experiencia previa de las partes interesadas, las pruebas graduales y otros modelos.
* Porcentaje de gasto, que utiliza el porcentaje de gasto relativo como proxy cuando los datos de marketing son escasos.

Cuando se crea un modelo por primera vez, la creación inicia inmediatamente el proceso de formación y puntuación. Una vez finalizada la formación inicial y la ejecución de puntuación, las perspectivas del modelo están disponibles para su revisión. Un modelo puede ser entrenado posteriormente. Además, se pueden añadir datos al modelo, lo que requiere que vuelva a puntuar el modelo manualmente. Volver a entrenar y a puntuar son un proceso iterativo a medida que surgen nuevos hallazgos e información, y se necesitan ajustes para obtener un modelo de ajuste que sea más apropiado para sus objetivos comerciales.


## Modelos de compilación

Para generar un modelo, use el flujo de configuración del modelo guiado paso a paso de Mix Modeler disponible al seleccionar **[!UICONTROL Open model canvas]**. Consulte [Modelos de compilación](build.md) para obtener más información.

## Administrar modelos

Para ver una tabla de los modelos actuales, en la interfaz de Mix Modeler:

1. Seleccione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** en el carril izquierdo.

1. Verá una tabla de los modelos actuales.

   Las columnas de la tabla especifican detalles sobre el modelo.

   | Nombre de columna | Detalles |
   |---|---|
   | Nombre | Nombre del modelo |
   | Descripción | Descripción del modelo |
   | Evento de conversión | La conversión que ha seleccionado para el modelo. |
   | Frecuencia de ejecución | Frecuencia de ejecución del aprendizaje del modelo. |
   | Última ejecución | La fecha y hora de la última formación del modelo. |
   | Estado | El estado del modelo. |

   {style="table-layout:auto"}

   El estado del modelo del que se informa depende de dónde se encuentre un modelo dentro de su ciclo de vida. Por ejemplo, si un modelo se ha creado, si se ha vuelto a entrenar correctamente o no, o si se ha marcado o no correctamente.

   En la tabla siguiente:

   * ![Marca de verificación](/help/assets/icons/Checkmark.svg): indica una ejecución correcta de un paso en el ciclo de vida del modelo.
   * ![Reloj](/help/assets/icons/Clock.svg): indica una ejecución en curso actual de un paso en el ciclo de vida del modelo.
   * ![Cerrar](/help/assets/icons/Close.svg) - indica una ejecución fallida de un paso en el ciclo de vida del modelo.

   | Estado | [Compilación](/help/models/build.md) | [Entrenar](/help/models/train-score.md#train) | [Puntuación](/help/models/train-score.md#score) | [Volver A Entrenar](/help/models/train-score.md#train) | [Puntuación adicional](/help/models/train-score.md#score) |
   |---|:---:|:---:|:---:|:---:|:---:|
   | En curso | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | | | | |
   | En curso | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Reloj](/help/assets/icons/Clock.svg) | | | |
   | En curso | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Reloj](/help/assets/icons/Clock.svg) | | |
   | En curso | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Reloj](/help/assets/icons/Clock.svg) | |
   | En curso | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Reloj](/help/assets/icons/Clock.svg) |
   | Error de formación | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Cerrar](/help/assets/icons/Close.svg) | | | |
   | Error de formación | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Cerrar](/help/assets/icons/Close.svg) | |
   | Formación completada correctamente | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | | | |
   | Formación completada correctamente | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | |
   | Error de puntuación | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Cerrar](/help/assets/icons/Close.svg) | | |
   | Error de puntuación | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Cerrar](/help/assets/icons/Close.svg) |
   | Puntuación correcta | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | | |
   | Puntuación correcta | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | ![Marca de verificación](/help/assets/icons/Checkmark.svg) |

   {style="table-layout:fixed"}

1. Para cambiar las columnas mostradas en la lista, seleccione ![Configuración de columna](/help/assets/icons/ColumnSetting.svg) y active o desactive las columnas ![Comprobar](/help/assets/icons/Checkmark.svg).

Puede realizar las siguientes acciones en un modelo específico.

### Datos del modelo

La funcionalidad de perspectivas del modelo solo está disponible en modelos entrenados y puntuados correctamente.

Para ver las perspectivas de un modelo:

1. Seleccione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** en el carril izquierdo.

1. Seleccione el nombre del modelo.

Se le redirigirá a [Información del modelo](insights.md).


### Ver detalles

Para ver más detalles de un modelo:

1. Seleccione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** en el carril izquierdo.

1. Seleccione ![Información](/help/assets/icons/Info.svg) para que un modelo muestre una ventana emergente con detalles.


### Duplicar

Puede duplicar rápidamente un modelo.

1. Seleccione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** en el carril izquierdo.

1. Seleccione ![Más](/help/assets/icons/More.svg) para un modelo y, en el menú contextual, seleccione **[!UICONTROL Duplicate]**.

Se le redirigirá a los pasos para crear un nuevo modelo, con un nombre propuesto compuesto por el nombre del modelo original anexado con **[!UICONTROL (Copy)] (_n_)**.

### Editar

Puede editar el nombre, la descripción y la programación de la formación y la puntuación de un modelo.

1. Seleccione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** en el carril izquierdo.

1. Seleccione ![Más](/help/assets/icons/More.svg) para un modelo y, en el menú contextual, seleccione **[!UICONTROL Edit]**.

   En el diálogo **[!UICONTROL Edit model]**:

   * Escriba un nuevo(a) **[!UICONTROL Name]** y **[!UICONTROL Description]**.

   * Para habilitar la programación, habilite **[!UICONTROL Status]**. Solo se puede activar la programación de modelos que se hayan entrenado y clasificado.

      1. Seleccionar un **[!UICONTROL Scoring frequency]**:

         * **[!UICONTROL Daily]**: escriba una hora válida (por ejemplo, `05:22 pm`) o use ![Reloj](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Weekly]**: seleccione un día de la semana e introduzca una hora válida (por ejemplo, `05:22 pm`) o use ![Reloj](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Monthly]**: selecciona un día del mes en el menú desplegable Ejecutar en cada e introduce una hora válida (por ejemplo, `05:22 pm`) o usa ![Reloj](/help/assets/icons/Clock.svg).

      1. Seleccione un(a) **[!UICONTROL Training frequency]** del menú desplegable: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** o **[!UICONTROL None]**.

     ![Editar un modelo](../assets/model-edit.png)

1. Seleccione **[!UICONTROL Save]**.



### Entrenar

Considere la posibilidad de volver a entrenar un modelo cuando desee incluir nuevos datos de factor y marketing incremental. Consulte [Modelos de entrenamiento y puntuación](train-score.md#train) para obtener más información.


### Puntuación

Puede puntuar gradualmente un modelo basado en nuevos datos de marketing o volver a puntuar un modelo para un intervalo de fechas específico. Consulte [Modelos de entrenamiento y puntuación](train-score.md#score) para obtener más información.


### Eliminar modelos

Para eliminar un modelo:

1. Seleccione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** en el carril izquierdo.
1. Seleccione ![Más](/help/assets/icons/More.svg) para un modelo y, en el menú contextual, seleccione **[!UICONTROL Delete]**. También puede seleccionar ![Eliminar](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** de la barra de acciones azul.
1. Seleccione **[!UICONTROL Delete]** en el cuadro de diálogo de confirmación **[!UICONTROL Delete model]** para eliminar el modelo. Seleccione **[!UICONTROL Cancel]** para cancelar.

Para eliminar varios modelos:

1. Seleccione varios modelos.
1. En la barra de acciones azul, seleccione ![Eliminar](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** para eliminar los modelos.
1. Seleccione **[!UICONTROL Delete]** en el cuadro de diálogo de confirmación de **[!UICONTROL Delete *x *modelos]**&#x200B;para eliminar los modelos. Seleccione **[!UICONTROL Cancel]**&#x200B;para cancelar.

