---
title: Reglas de conjuntos de datos
description: Obtenga información sobre cómo definir reglas de conjuntos de datos para utilizarlas como parte de la armonización de los datos en Mix Modeler.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: b631cf8d06fe71d9f5ca547923eb3237c677a915
workflow-type: tm+mt
source-wordcount: '1696'
ht-degree: 0%

---

# Reglas de conjuntos de datos

Las reglas del conjunto de datos le ayudan a asignar los campos armonizados con los campos de los datos introducidos en Mix Modeler.

* Para los datos agregados que ha introducido en Adobe Experience Platform, asigne uno o más de los campos de conjunto de datos disponibles a los campos armonizados correspondientes.
* Para los datos de evento, puede asignar individualmente uno o más campos armonizados a campos del conjunto de datos, directamente o mediante condiciones.


## Administrar reglas de conjuntos de datos

Para ver una tabla de las reglas de conjuntos de datos disponibles, en la interfaz de Mix Modeler:

1. Seleccione ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** en el carril izquierdo.

1. Seleccione **[!UICONTROL Dataset rules]** de la barra superior. Verá una tabla de las reglas del conjunto de datos.

Puede buscar un conjunto de datos rápidamente usando ![Buscar](/help/assets/icons/Search.svg) **[!UICONTROL _Escriba un nombre de conjunto de datos_]**.

Las columnas de la tabla especifican detalles sobre las reglas del conjunto de datos:

| Nombre de columna | Detalles |
| ---------------------- | ----------|
| Conjunto de datos | Nombre del conjunto de datos.  Use ![Más](/help/assets/icons/More.svg) para seleccionar acciones para un conjunto de datos. Puede hacer lo siguiente:<ul><li>![Vista previa](/help/assets/icons/Preview.svg) **[!UICONTROL View]** para ver la configuración de reglas del conjunto de datos. Todos los campos están desactivados.</li><li>![Editar](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** para editar la configuración de reglas del conjunto de datos.</li><li>![Eliminar](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** para eliminar la configuración de reglas del conjunto de datos. Se le pedirá que confirme la eliminación en el cuadro de diálogo Eliminar conjunto de datos. Seleccione **[!UICONTROL Delete]** para eliminar de forma permanente la configuración de reglas del conjunto de datos.</li><ul> |
| Fuente | El origen del conjunto de datos: Adobe Analytics, Eventos de experiencia, Resumen (agregado) o Eventos de experiencia del consumidor. |
| Esquema | Esquema al que se ajusta el conjunto de datos. Puede seleccionar rápidamente el nombre del esquema para abrir el esquema en una nueva pestaña del editor de esquemas en ![Esquema](/help/assets/icons/Schemas.svg) [Esquemas](../ingest-data/schemas.md). |
| Granularidad | La granularidad de los datos del conjunto de datos. Los valores posibles son Diario, Semanal, Mensual o Anual. |
| Inicio de semana | Especifica qué día de la semana se considera el inicio de una nueva semana para el conjunto de datos específico. |
| Estado | El estado del campo: <p><span style="color:gray">●</span> borrador o <p><span style="color:green">●</span> activo |
| Última modificación | Datos y hora de la última modificación de la regla del conjunto de datos. |

{style="table-layout:auto"}

### Crear una regla de conjunto de datos

Para crear una regla de conjunto de datos, en la interfaz ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** de Mix Modeler, seleccione **[!UICONTROL Create a dataset rule]** en el asistente **[!UICONTROL Dataset rules configuration]**.

En la pantalla **[!UICONTROL Create]**,

1. En **[!UICONTROL Dataset details]**, seleccione un conjunto de datos de **[!UICONTROL Select dataset]** para comenzar la configuración. En la lista, los conjuntos de datos se clasifican en **[!UICONTROL Consumer Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]** y **[!UICONTROL Summary]**.

1. Seleccione un día para **[!UICONTROL Start of the week]**.

1. Seleccione **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** o **[!UICONTROL Yearly]** para **[!UICONTROL Granularity]**.

1. Cuando haya seleccionado un conjunto de datos de la categoría **[!UICONTROL Summary]**, seleccione **[!UICONTROL Aggregation]** o **[!UICONTROL Replacement]** para **[!UICONTROL Data restatement is by]**.

   Los datos de informes de los editores son muy importantes para los analistas de marketing, ya que trabajar con editores suele implicar un gasto significativo y los cambios en los datos de informes pueden dar como resultado perspectivas y planes de inversión muy diferentes. Además, los analistas de marketing necesitan datos precisos para obtener las perspectivas correctas y presentar propuestas convincentes para ganar la confianza de los interesados. Sin embargo, estos editores, como Google y Facebook, suelen reiterar o eliminar los datos de los informes a medida que concilian sus datos. El lapso de tiempo para la mayoría de los cambios es de 7 días desde el rendimiento de los medios informado. Es posible realizar cambios adicionales en los datos en un plazo de 30 días. En general, después de 30 días, los libros se consideran cerrados y los datos completos.

   Mix Modeler admite la reafirmación de datos. Garantizar que los datos utilizados para la creación de informes, el modelado y la planificación sean precisos. Y que los datos puedan satisfacer las expectativas y necesidades de los analistas de marketing y de marca.

   Puede enviar filas restauradas de datos de resumen como filas incrementales en un conjunto de datos de Experience Platform y el servicio de armonización actualiza el conjunto de datos armonizado con esos datos restaurados. Del mismo modo, también puede eliminar filas de datos de resumen que deban reflejarse en el servicio de armonización.

1. En la sección **[!UICONTROL Map to harmonized fields]**:

   1. Seleccionar un campo armonizado de **[!UICONTROL Standard harmonized field]**.

   1. Cuando el campo armonizado seleccionado es del tipo métrica:

      1. Seleccione **[!UICONTROL Count]** o **[!UICONTROL Sum]** de **[!UICONTROL Mapping type]**.

      1. Seleccione un **[!UICONTROL *campo del conjunto de datos de AEP *]**&#x200B;al que desee que se asigne el campo armonizado de forma predeterminada.

   1. Cuando el campo seleccionado es de tipo dimensión:

      1. Seleccione **[!UICONTROL Map Into]** o **[!UICONTROL Case]** de **[!UICONTROL Mapping type]**.

      1. Cuando haya seleccionado **[!UICONTROL Map Into]**, seleccione **[!UICONTROL Field]** y **[!UICONTROL *campo del conjunto de datos de AEP *]**&#x200B;o **[!UICONTROL Value]**&#x200B;y un valor predeterminado para asignar el campo armonizado de forma predeterminada al campo del conjunto de datos o al valor introducido.

      1. Cuando seleccione **[!UICONTROL Case]**, seleccione **[!UICONTROL Field]** y **[!UICONTROL *campo del conjunto de datos de AEP *]**&#x200B;o **[!UICONTROL Value]**&#x200B;y un valor predeterminado para asignar el campo armonizado de forma predeterminada al campo del conjunto de datos o al valor introducido.

         1. Para establecer valores de forma explícita, defina uno o más casos, que consten de una o más condiciones. Cada condición puede comprobar si hay un campo específico del **[!UICONTROL *conjunto de datos de AEP *]**&#x200B;que sea **[!UICONTROL Exists]**&#x200B;o **[!UICONTROL Not Exists]**, o si es **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**&#x200B;o **[!UICONTROL Ends With]**&#x200B;un valor introducido en&#x200B;**[!UICONTROL * Introducir valor de entrada *]**.

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

      Al asignar un campo armonizado estándar desde un conjunto de datos de resumen, Mix Modeler intenta deducir el campo del conjunto de datos de Experience Platform correspondiente. Si se realiza correctamente:

      * Si el campo es de tipo dimensión, **[!UICONTROL Map into]** está seleccionado como **[!UICONTROL Mapping type]**.
      * Si el campo es del tipo métrica, **[!UICONTROL Sum]** está seleccionado como **[!UICONTROL Mapping type]**.
      * **[!UICONTROL Field]** está seleccionado como tipo de asignación **[!UICONTROL Default]**.
      * El campo del conjunto de datos de Experience Platform correspondiente se inserta automáticamente para *Campo del conjunto de datos de AEP*.

      Puede cambiar cualquiera de los valores propuestos si estos son incorrectos o no admiten su caso de uso específico.

1. Seleccione ![Agregar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]** para definir campos adicionales.

Cuando termine, seleccione **[!UICONTROL Save as draft]** para guardar una versión de borrador de la regla o **[!UICONTROL Save]** para guardar y activar la regla. Seleccione **[!UICONTROL Cancel]** para cancelar la configuración de regla.

>[!NOTE]
>
>La experiencia **[!UICONTROL Map to harmonized fields]** dedicada para las reglas de conjuntos de datos de resumen está en desuso. Todas las reglas del conjunto de datos ahora utilizan una experiencia **[!UICONTROL Map to harmonized fields]** similar, independientemente del tipo de conjunto de datos. Para los conjuntos de datos de resumen para los que ha definido reglas utilizando la experiencia **[!UICONTROL Map to harmonized fields]** obsoleta, es posible que desee comprobar estas reglas con la experiencia **[!UICONTROL Map to harmonized field]** genérica.
>



### Editar una regla de conjunto de datos

Para editar una regla del conjunto de datos, en la interfaz ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** de Mix Modeler:

1. Seleccione ![Más](/help/assets/icons/More.svg) en la columna **[!UICONTROL Dataset]** para la regla del conjunto de datos que desee editar.
1. En el menú contextual, seleccione ![Editar](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** para comenzar a editar la regla del conjunto de datos. Consulte [Crear una regla de conjunto de datos](#create-a-dataset-rule) para obtener más información.


### Eliminar una regla del conjunto de datos

Para eliminar una regla del conjunto de datos, en la interfaz ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** de Mix Modeler:

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
>[!BADGE beta]{type=Informative} Las preferencias de combinación de datos son una característica beta y su funcionalidad está sujeta a cambios.

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

1. En el diálogo **[!UICONTROL Data merge preferences]** [!BADGE beta]{type=Informative}:

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
