---
title: Campos armonizados
description: Aprenda a definir campos que se utilizarán como parte de la armonización de los datos en Mix Modeler.
feature: Harmonized Data, Harmonized Fields
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 10%

---


# Campos armonizados

Los campos armonizados permiten definir campos para datos conceptualmente iguales, procedentes de diferentes fuentes, cada uno con su propia definición de esos datos. Por ejemplo, una métrica de clics puede definirse y denominarse de forma diferente en función del origen de los datos. Un campo armonizado de clics le permite definir una nomenclatura común para una métrica de clics basada en esas diferentes fuentes de datos de clics.

Los campos armonizados permiten definir los campos que desea utilizar como parte del flujo de trabajo de armonización de datos. Los campos que defina se pueden utilizar para definir reglas de conjuntos de datos, puntos de contacto de marketing y conversiones.

## Campos de armonización global

Los campos de armonización global predeterminados disponibles en Mix Modeler son los siguientes:


| Nombre del campo | Nombre para mostrar | Categoría | Tipo de datos | Comentario |
| ---------------------- | ---------------------- | --------- | --------- | --------- |
| marca | Marca | Dimensión | Cadena |           |
| campaña | Campaign | Dimensión | Cadena |           |
| canal | Canal | Dimensión | Cadena |           |
| channel_id | ID de canal | Dimensión | Cadena |           |
| channel_type_at_source | Tipo De Canal En Origen | Dimensión | Cadena |           |
| canal | Canal | Dimensión | Cadena |           |
| clics | Clics | Métrica | Número |           |
| conversiontype | Tipo de conversión | Dimensión | Cadena |           |
| coste | Coste | Métrica | Moneda |           |
| conjunto de datos | Conjunto de datos | Dimensión | Cadena |           |
| date_type | Tipo de fecha | Dimensión | Cadena | día, semana |
| correos electrónicos enviados | Correos electrónicos enviados | Métrica | Número |           |
| event_date | Fecha | Dimensión | DateTime |           |
| demanda_bruta | Demanda bruta | Métrica | Moneda |           |
| impresiones | Impresiones | Métrica | Número |           |
| last_updated_date | Fecha de última actualización | Dimensión | DateTime |           |
| linkvisit | Visitas de vínculo | Métrica | Número |           |
| mediatype | Tipo de medio | Dimensión | Cadena |           |
| net_sales | Ventas netas | Métrica | Moneda |           |
| pedidos | Pedidos | Métrica | Número |           |
| sourcetype | Tipo de origen | Dimensión | Cadena |           |
| gastar | Gasto | Métrica | Moneda |           |
| fuente de tráfico | Traffic Source | Dimensión | Cadena |           |

{style="table-layout:auto"}

Puede añadir, editar o eliminar sus propios campos armonizados sobre estos campos armonizados globales.

## Administrar campos armonizados

Para ver una tabla de los campos armonizados disponibles, en la interfaz del Mix Modeler:

1. Seleccionar ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** desde el carril izquierdo.

1. Seleccionar **[!UICONTROL Fields]** desde la barra superior. Verá una tabla de los campos armonizados.

   Las columnas de la tabla especifican detalles sobre los campos armonizados

   | Nombre de columna | Detalles |
   | ---------------------- | ----------|
   | Nombre del campo | El nombre del campo armonizado. |
   | Nombre para mostrar | El nombre para mostrar del campo armonizado. Este nombre para mostrar se utiliza al definir reglas de conjuntos de datos, puntos de contacto de marketing y definiciones de conversión. |
   | Categoría | Especifica si un campo de datos armonizado es una [!UICONTROL Dimension], a [!UICONTROL Metric] o [!UICONTROL Derived]. Una categoría derivada es un campo armonizado que utiliza una definición de fórmula basada en métricas. |
   | Propietario | Indica si un campo armonizado es predeterminado ([!UICONTROL Global]), o se ha definido por usted ([!UICONTROL Client]). |
   | Tipo de datos | Especifica el tipo de datos ([!UICONTROL Number], [!UICONTROL String], [!UICONTROL Currency], [!UICONTROL DateTime]). |
   | Fecha y hora de creación | Fecha y hora de creación del campo armonizado. |
   | Fecha y hora de la última modificación | Datos y hora de la última modificación del campo armonizado. |
   | Fórmula | Especifica la fórmula de un campo armonizado basado en una categoría derivada. |

   {style="table-layout:auto"}

1. Para buscar un campo armonizado específico, utilice ![Buscar](../assets/icons/Search.svg) **[!UICONTROL *Buscar campo armonizado *]**.




### Añadir un campo armonizado

Para añadir un campo armonizado, en la ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** en el Mix Modeler:

1. Seleccionar ![Añadir](../assets/icons/AddCircle.svg)Agregue el campo.

1. En el **[!UICONTROL Create]** diálogo:

   1. Introduzca una **[!UICONTROL Field name]**, por ejemplo `region`.
   1. Introduzca una **[!UICONTROL Display name]**, por ejemplo `Region`.
   1. Seleccione una **[!UICONTROL Category]**: **[!UICONTROL Dimension]**, **[!UICONTROL Metric]** o **[!UICONTROL Derived]**.

      Al seleccionar **[!UICONTROL Derived]**, especifique un **[!UICONTROL Formula]**. Para crear una expresión aritmética válida, combine una o más métricas de **[!UICONTROL Insert Metric]** con uno o más operadores **[!UICONTROL + - * / ( )]** . Por ejemplo, `[orders]/[impressions]`

   1. Seleccione una **[!UICONTROL Data type]**.

      - **[!UICONTROL String]** o **[!UICONTROL DateTime]**, cuando la categoría seleccionada sea Dimension.
      - **[!UICONTROL Number]** o **[!UICONTROL Currency]** cuando la categoría seleccionada es Métrica o Derivada.

   1. Seleccionar **[!UICONTROL Submit]** para añadir el campo armonizado. Seleccionar **[!UICONTROL Close]** para cerrar el cuadro de diálogo sin añadir el campo armonizado.

      ![Creación de un campo](../assets/create-field.png)


### Editar un campo armonizado

Solo puede editar los campos armonizados que haya creado anteriormente. No se puede editar un campo armonizado global.

Para editar un campo armonizado, en la ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** en el Mix Modeler:

1. Seleccione el campo armonizado que desea editar. Por ejemplo, **[!UICONTROL Region]**.

1. En el **[!UICONTROL Edit harmonization values]** panel, modificar valores para **[!UICONTROL Display name]**, **[!UICONTROL Category]**, y **[!UICONTROL Data type]**.

1. Seleccionar **[!UICONTROL Submit]** para aplicar los cambios en el campo armonizado.

   ![Editar un campo](../assets/edit-field.png)

### Eliminar un campo armonizado

Solo puede eliminar los campos armonizados que haya creado anteriormente. No se puede eliminar un campo armonizado global.

Para eliminar un campo armonizado, en la ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** en el Mix Modeler:

1. Seleccione el campo armonizado que desee eliminar, por ejemplo **[!UICONTROL Region]**.

1. Seleccionar ![Eliminar](../assets/icons/Delete.svg) **[!UICONTROL Delete]** desde el **[!UICONTROL Edit harmonization values]** panel izquierdo.


