---
title: Reglas de conjuntos de datos
description: Obtenga información sobre cómo definir reglas de conjuntos de datos para utilizarlas como parte de la armonización de los datos en Mix Modeler.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: a8590d604f79268bc8d1f012f2c19271a3b38668
workflow-type: tm+mt
source-wordcount: '1407'
ht-degree: 0%

---

# Reglas de conjuntos de datos

Las reglas de conjuntos de datos le ayudan a asignar los campos armonizados con campos de los datos introducidos en Mix Modeler.

* Para los datos agregados que ha introducido en Adobe Experience Platform, asigne uno o más de los campos de conjunto de datos disponibles a los campos armonizados correspondientes.
* Para los datos de evento, puede asignar individualmente uno o más campos armonizados a campos del conjunto de datos, directamente o mediante condiciones.


## Administrar reglas de conjuntos de datos

Para ver una tabla de las reglas de conjuntos de datos disponibles, en la interfaz del Mix Modeler:

1. Seleccione ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** en el carril izquierdo.

1. Seleccione **[!UICONTROL Dataset rules]** de la barra superior. Verá una tabla de las reglas del conjunto de datos.

Las columnas de la tabla especifican detalles sobre las reglas del conjunto de datos:

| Nombre de columna | Detalles |
| ---------------------- | ----------|
| Conjunto de datos | Nombre del conjunto de datos. |
| Fuente | El origen del conjunto de datos: Adobe Analytics, Eventos de experiencia, Resumen (agregado) o Eventos de experiencia del consumidor. |
| Esquema | Esquema al que se ajusta el conjunto de datos. Puede seleccionar rápidamente el nombre del esquema para abrir el esquema en una nueva pestaña del editor de esquemas en ![Esquema](/help/assets/icons/Schemas.svg) [Esquemas](../ingest-data/schemas.md). |
| Granularidad | La granularidad de los datos del conjunto de datos. Los valores posibles son Diario, Semanal, Mensual o Anual. |
| Inicio de semana | Especifica qué día de la semana se considera el inicio de una nueva semana para el conjunto de datos específico. |
| Estado | El estado del campo: <p><span style="color:gray">●</span> borrador o <p><span style="color:green">●</span> activo |
| Última modificación | Datos y hora de la última modificación de la regla del conjunto de datos. |

{style="table-layout:auto"}

### Crear una regla de conjunto de datos

Para crear una regla de conjunto de datos, en la interfaz ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** del Mix Modeler, seleccione **[!UICONTROL Create a dataset rule]** en el asistente **[!UICONTROL Dataset rules configuration]**.

En la pantalla **[!UICONTROL Create]**,

1. En **[!UICONTROL Dataset details]**, seleccione un conjunto de datos de **[!UICONTROL Select dataset]** para comenzar la configuración. En la lista, los conjuntos de datos se clasifican en **[!UICONTROL Consumer Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]** y **[!UICONTROL Summary]**.

1. Seleccione un día para **[!UICONTROL Start of the week]**.

1. Seleccione **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** o **[!UICONTROL Yearly]** para **[!UICONTROL Granularity]**.

1. Cuando haya seleccionado un conjunto de datos de la categoría **[!UICONTROL Summary]**:

   1. Para definir si los datos del conjunto de datos agregan o reemplazan datos existentes, seleccione **[!UICONTROL Aggregation]** o **[!UICONTROL Replacement]** para **[!UICONTROL Data restatement is by]**.

   1. Asigne cada uno de los(as) **[!UICONTROL Available dataset fields]** a los(as) **[!UICONTROL Standard harmonized fields]** correspondientes en **[!UICONTROL Map to harmonized fields]**. Si no desea asignar un campo de conjunto de datos a un campo armonizado, seleccione explícitamente **[!UICONTROL -- None --]**.

   1. Si necesita un nuevo campo armonizado, no disponible en la lista, seleccione **[!UICONTROL Create New]** para crear un nuevo campo armonizado. Verá el cuadro de diálogo como se describe en [Agregar un nuevo campo armonizado](fields.md#add-a-harmonized-field).

   1. Cuando finalice la asignación de todos los campos de la regla, seleccione **[!UICONTROL Save as draft]** para guardar una versión de borrador de la regla o **[!UICONTROL Save]** para guardar y activar la regla. Seleccione **[!UICONTROL Cancel]** para cancelar la configuración de regla.

      ![Crear reglas de conjuntos de datos](/help/assets/dataset-create-summary.png)

1. Cuando haya seleccionado un conjunto de datos de categoría de evento (**[!UICONTROL Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Consumer Experience Events]**), en el cuadro debajo de **[!UICONTROL Map to harmonized fields]**:

   1. Seleccionar un campo armonizado de **[!UICONTROL Standard harmonized field]**.

   1. Cuando el campo armonizado seleccionado es del tipo métrica:

      1. Seleccione **[!UICONTROL Count]** o **[!UICONTROL Sum]** de **[!UICONTROL Mapping type]**.

      1. Seleccione un **[!UICONTROL *campo del conjunto de datos de AEP *]**&#x200B;al que desee asignar el campo armonizado de forma predeterminada.

   1. Cuando el campo seleccionado es de tipo dimensión:

      1. Seleccione **[!UICONTROL Map Into]** o **[!UICONTROL Case]** de **[!UICONTROL Mapping type]**.

      1. Cuando haya seleccionado **[!UICONTROL Map Into]**, seleccione **[!UICONTROL Field]** y **[!UICONTROL *campo del conjunto de datos de AEP *]**&#x200B;o **[!UICONTROL Value]**&#x200B;y un valor predeterminado para asignar el campo armonizado de forma predeterminada al campo del conjunto de datos o al valor introducido.

      1. Cuando seleccione **[!UICONTROL Case]**, seleccione **[!UICONTROL Field]** y **[!UICONTROL *campo del conjunto de datos de AEP *]**&#x200B;o **[!UICONTROL Value]**, y un valor predeterminado para asignar el campo armonizado de forma predeterminada al campo del conjunto de datos o al valor introducido.

         1. Para establecer valores de forma explícita, defina uno o más casos, que consten de una o más condiciones. Cada condición puede comprobar si hay un campo específico de **[!UICONTROL *conjunto de datos de AEP *]**&#x200B;que sea **[!UICONTROL Exists]**&#x200B;o **[!UICONTROL Not Exists]**, o si es **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**&#x200B;o **[!UICONTROL Ends With]**&#x200B;un valor introducido en&#x200B;**[!UICONTROL * Introducir valor de entrada *]**.

         1. Para agregar otro caso, seleccione ![Agregar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add case]**, para agregar otra condición, seleccione ![Agregar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. Para eliminar un caso o condición, seleccione ![Cerrar](/help/assets/icons/Close.svg) en el contenedor correspondiente.

         1. Para seleccionar si alguna o todas las condiciones deben aplicarse a un caso, seleccione **[!UICONTROL Any of]** o **[!UICONTROL All of]**.

         1. Para establecer el valor de resultado de un caso, escriba el valor en **[!UICONTROL Then]**.

      El ejemplo siguiente

      * usa un **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** para asignar el campo armonizado **[!UICONTROL Channel Type At Source]** al campo **[!UICONTROL channel_type]** desde el conjunto de datos **[!DNL Luma Transactions]**.

      * usa un **[!UICONTROL Case]** **[!UICONTROL Mapping type]** para asignar de forma condicional el valor del campo **[!UICONTROL marketing.campaignName]** del conjunto de datos **[!DNL Luma Transactions]** al campo armonizado **[!UICONTROL Campaign]**. El campo Campaña armonizada se establece en:

         * `Black Friday` cuando **[!UICONTROL marketing.campaignName]** es `_black_friday` o `BlackFriday`.
         * al valor de **[!UICONTROL marketing.campaignName]** en todos los demás casos.

        ![Evento de regla de conjunto de datos](/help/assets/dataset-create-event.png)

1. Seleccione ![Agregar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]** para definir campos adicionales.

Cuando termine, seleccione **[!UICONTROL Save as draft]** para guardar una versión de borrador de la regla o **[!UICONTROL Save]** para guardar y activar la regla. Seleccione **[!UICONTROL Cancel]** para cancelar la configuración de regla.


### Editar una regla de conjunto de datos

Para editar una regla del conjunto de datos, en la interfaz ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** del Mix Modeler:

1. Seleccione ![Más](/help/assets/icons/More.svg) en la columna **[!UICONTROL Dataset]** para la regla del conjunto de datos que desee editar.
1. En el menú contextual, seleccione ![Editar](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** para comenzar a editar la regla del conjunto de datos. Consulte [Crear una regla de conjunto de datos](#create-a-dataset-rule) para obtener más información.


### Eliminar una regla del conjunto de datos

Para eliminar una regla del conjunto de datos, en la interfaz ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** del Mix Modeler:

1. Seleccione ![Más](/help/assets/icons/More.svg) en la columna **[!UICONTROL Dataset]** para la regla del conjunto de datos que desee eliminar.
1. En el menú contextual, seleccione ![Eliminar](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** para eliminar la regla del conjunto de datos. Se le pedirá confirmación. Seleccione **[!UICONTROL Delete]** para eliminar de forma permanente la regla del conjunto de datos seleccionado.


## Sincronizar datos

Para sincronizar datos entre los datos armonizados y los conjuntos de datos de resumen o evento al aplicar la lógica en las reglas del conjunto de datos:

1. Seleccione **[!UICONTROL Sync data]**.

1. En el cuadro de diálogo **[!UICONTROL Sync data for dataset rules]**, seleccione
   * **[!UICONTROL Refresh harmonized data for summary datasets]**,
   * **[!UICONTROL Refresh harmonized data for event datasets]**, o
   * **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Para iniciar la sincronización basada en las reglas del conjunto de datos definidas entre los datos armonizados y los datos de los conjuntos de datos, seleccione **[!UICONTROL Sync]**. Para cancelar la sincronización, seleccione **[!UICONTROL Cancel]**.

   ![Sincronizar datos](/help/assets/sync-data.png)


## Preferencias de combinación de datos

>[!NOTE]
>
>[!BADGE beta]{type=Informative}

Para garantizar predicciones de modelos precisas, puede definir las preferencias de combinación de datos. Esta funcionalidad permite a los usuarios resolver cualquier conflicto después de combinar los datos de nivel de resumen y de nivel de evento.

Puede configurar una preferencia de métrica predeterminada para que se aplique en casos de actualizaciones en conflicto. Esta métrica predeterminada puede ser una de las tres opciones:

* **[!UICONTROL Summary data]**
* **[!UICONTROL Sum of summary and event data]**
* **[!UICONTROL Event data]**

Cuando, durante la armonización, varias fuentes de datos intentan actualizar un campo de métrica para un canal determinado, se aplica la preferencia predeterminada configurada por el usuario. Esta preferencia se aplica en el nivel de zona protegida a menos que se anule para determinadas preferencias basadas en métricas que se han configurado adicionalmente.

En **[!UICONTROL Metric based preferences]**, el usuario puede configurar el origen específico (**[!UICONTROL Summary]** o **[!UICONTROL Event]**) para una métrica determinada y el tipo de conversión correspondiente para esa métrica.

Los casos de uso habituales son:

* la misma métrica publicitaria se mide y se comunica en varios conjuntos de datos, o
* la medición de métricas puede estar incompleta en algunos conjuntos de datos, mientras que otro conjunto de datos puede ser un superconjunto de una métrica en particular, lo que resulta en un recuento doble.

### Configurar

Para configurar las preferencias de combinación:


1. Seleccionar ![preferencias de combinación de datos](/help/assets/icons/Merge.svg) [!BADGE beta].

1. En la **[!UICONTROL Data merge preferences]** [!BADGE versión beta]{type=Informative}

   ![Preferencias de combinación de datos](/help/assets/data-merge-preferences.png)

   * Seleccione un(a) **[!UICONTROL Default metric preference]**. La preferencia de métrica predeterminada seleccionada se aplica cuando, durante la armonización, varias fuentes de datos actualizan un campo de métrica para un canal determinado. La preferencia se aplica en el nivel de zona protegida, a menos que se anule para las preferencias específicas basadas en métricas. Puede seleccionar entre **[!UICONTROL Summary data]**, **[!UICONTROL Event data]** y **[!UICONTROL Sum of summary and event data]**.

   * Para agregar preferencias basadas en métricas específicas:

      1. Seleccione ![Más](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a metric]**.
         1. Seleccione una métrica de la lista **[!UICONTROL *Selección de métrica *]**.
         1. Seleccione **[!UICONTROL CHANNELS]** o **[!UICONTROL CONVERSION TYPES]**. En la lista, seleccione **[!UICONTROL All]** o un canal o tipo de conversión específico.
         1. Seleccione **[!UICONTROL Summary]** o **[!UICONTROL Event]** para especificar si se prefieren los datos de resumen o los datos de evento para la métrica (y todo o el canal seleccionado) al combinar datos.

         Para agregar uno o más canales adicionales o tipos de conversión:

         1. Seleccione ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a channel]** o ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion type]**.
         1. Seleccione **[!UICONTROL Summary]** o **[!UICONTROL Event]**.

         Para eliminar un canal o tipo de conversión, selecciona ![Cruzar](/help/assets/icons/Close.svg).

      1. Para agregar preferencias basadas en métricas más específicas, repita el paso anterior.

   * Para eliminar una preferencia basada en una métrica específica existente, seleccione ![Eliminar](/help/assets/icons/Delete.svg).

1. Seleccione **[!UICONTROL Save]** para guardar las preferencias de combinación de datos. Se inicia una resincronización de los datos. <br/>Seleccione **[!UICONTROL Cancel]** para cancelar.

## Eliminar un conjunto de datos de origen

Al eliminar un conjunto de datos de origen que se utiliza en los datos armonizados, las entradas subyacentes de ese conjunto de datos de origen se eliminan de [[!UICONTROL Harmonized data]](/help/harmonize-data/overview.md). Sin embargo, la regla del conjunto de datos con el conjunto de datos de origen eliminado permanece en la lista de configuración de reglas del conjunto de datos con un icono ![DataRemove](/help/assets/icons/DataRemove.svg) que indica que el conjunto de datos de origen se ha eliminado. Para obtener más información:

* Seleccione ![Más](/help/assets/icons/More.svg) y ![Vista previa](/help/assets/icons/Preview.svg) **[!UICONTROL View]** del menú contextual.
El cuadro de diálogo **[!UICONTROL Dataset rule mapping - Fields]** muestra información sobre el conjunto de datos de origen eliminado y los campos utilizados en la configuración de reglas del conjunto de datos.

Cuando vuelva a la configuración de **[!UICONTROL Dataset rules]**, verá un cuadro de diálogo que explica que se han eliminado uno o más conjuntos de datos de origen. Los datos armonizados se ven afectados en una próxima sincronización ad hoc o programada. Revise la configuración de reglas del conjunto de datos.

Los datos armonizados se actualizan sin los datos de origen eliminados en la siguiente sincronización ad hoc o programada. Sin embargo, sigue viendo cuadros de diálogo de alerta que le piden que elimine la regla del conjunto de datos basada en el conjunto de datos de origen eliminado. Esta alerta permite a los usuarios ver y evaluar los campos afectados en el conjunto de datos eliminado. Y para determinar el impacto en los puntos de contacto de marketing o en las conversiones que se pueden utilizar en cualquier modelo. Una vez revisado y mitigado este impacto, debe eliminar la regla del conjunto de datos de la lista de configuración de reglas del conjunto de datos.
