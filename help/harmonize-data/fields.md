---
title: Campos armonizados
description: Aprenda a definir campos que se utilizarán como parte de la armonización de los datos en Mix Modeler.
feature: Harmonized Data, Harmonized Fields
exl-id: f051279a-1ae9-49bd-a946-abfc34c90413
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 8%

---

# Campos armonizados

Los campos armonizados permiten definir campos para datos conceptualmente iguales, procedentes de diferentes fuentes, cada uno con su propia definición de esos datos. Por ejemplo, una métrica de clics puede definirse y denominarse de forma diferente en función del origen de los datos. Un campo armonizado de clics le permite definir una nomenclatura común para una métrica de clics basada en esas diferentes fuentes de datos de clics.

Los campos armonizados permiten definir los campos que desea utilizar como parte del flujo de trabajo de armonización de datos. Los campos que defina se pueden utilizar para definir reglas de conjuntos de datos, puntos de contacto de marketing y conversiones.

## Campos de armonización global

Los campos de armonización global predeterminados disponibles en Mix Modeler son los siguientes:


| Nombre de campo | Nombre para mostrar | Categoría | Tipo de datos | Comentario |
| ---------------------- | ---------------------- | --------- | --------- | --------- |
| marca | Marca | Dimensión | Cadena |           |
| campaña | Campaign | Dimensión | Cadena |           |
| canal | Canal | Dimensión | Cadena |           |
| channel_id | ID de canal | Dimensión | Cadena |           |
| channel_type_at_source | Tipo De Canal En Source | Dimensión | Cadena |           |
| canal | Canal | Dimensión | Cadena |           |
| clics | Clics | Métrica | Número |           |
| conversiontype | Tipo de conversión | Dimensión | Cadena |           |
| coste | Coste | Métrica | Moneda |           |
| conjunto de datos | Conjunto de datos | Dimensión | Cadena |           |
| date_type | Tipo de fecha | Dimensión | Cadena | día, semana |
| correos electrónicos enviados | Correos electrónicos enviados | Métrica | Número |           |
| event_date | Fecha | Dimensión | Fecha y hora |           |
| demanda_bruta | Demanda bruta | Métrica | Moneda |           |
| impresiones | Impresiones | Métrica | Número |           |
| last_updated_date | Fecha de última actualización | Dimensión | Fecha y hora |           |
| linkvisit | Visitas de vínculo | Métrica | Número |           |
| mediatype | Tipo de medio | Dimensión | Cadena |           |
| net_sales | Ventas netas | Métrica | Moneda |           |
| pedidos | Pedidos | Métrica | Número |           |
| sourcetype | Tipo de Source | Dimensión | Cadena |           |
| gastar | Gasto | Métrica | Moneda |           |
| fuente de tráfico | Traffic Source | Dimensión | Cadena |           |

{style="table-layout:auto"}

Puede añadir, editar o eliminar sus propios campos armonizados sobre estos campos armonizados globales.

## Administrar campos armonizados

Para ver una tabla de los campos armonizados disponibles, en la interfaz del Mix Modeler:

1. Seleccione ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** en el carril izquierdo.

1. Seleccione **[!UICONTROL Fields]** de la barra superior. Verá una tabla de los campos armonizados. Si hay más páginas disponibles, usa ![Flecha izquierda](/help/assets/icons/ChevronLeft.svg) o ![Flecha derecha](/help/assets/icons/ChevronRight.svg) en **[!UICONTROL Page _x _de_x_]** para moverte entre las páginas de la tabla.

   Las columnas de la tabla especifican detalles sobre los campos armonizados

   | Nombre de columna | Detalles |
   | ---------------------- | ----------|
   | Nombre de campo | El nombre del campo armonizado. |
   | Nombre para mostrar | El nombre para mostrar del campo armonizado. Este nombre para mostrar se utiliza al definir reglas de conjuntos de datos, puntos de contacto de marketing y definiciones de conversión. |
   | Categoría | Especifica si un campo de datos armonizado es [!UICONTROL Dimension], [!UICONTROL Metric] o [!UICONTROL Derived]. Una categoría derivada es un campo armonizado que utiliza una definición de fórmula basada en métricas. |
   | Tipo de datos | Especifica el tipo de datos ([!UICONTROL Number], [!UICONTROL String], [!UICONTROL Currency], [!UICONTROL Date time]). |
   | Fecha de creación | Fecha y hora de creación del campo armonizado. |
   | Propietario | Indica si un campo armonizado es uno predeterminado ([!UICONTROL Global]) o si lo ha definido usted ([!UICONTROL Client]). |
   | Fecha de la última modificación | Datos y hora de la última modificación del campo armonizado. |
   | Fórmula | Especifica la fórmula de un campo armonizado basado en una categoría derivada. |

   {style="table-layout:auto"}

1. Para buscar un campo armonizado específico, use ![Buscar](/help/assets/icons/Search.svg) **[!UICONTROL *Buscar campo armonizado *]**.


### Añadir un campo armonizado

Para agregar un campo armonizado, en la interfaz ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** del Mix Modeler:

1. Seleccione ![Agregar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]**.

1. En el diálogo **[!UICONTROL Create]**:

   1. Escriba un **[!UICONTROL Field name]**, por ejemplo `region`.
   1. Escriba un **[!UICONTROL Display name]**, por ejemplo `Region`.
   1. Seleccione un(a) **[!UICONTROL Category]**: **[!UICONTROL Dimension]**, **[!UICONTROL Metric]** o **[!UICONTROL Derived]**.

      Cuando seleccione **[!UICONTROL Derived]**, especifique un **[!UICONTROL Formula]**. Para generar una expresión aritmética válida, combine una o más métricas de **[!UICONTROL Insert Metric]** con uno o más operadores **[!UICONTROL + - * / ( )]** Por ejemplo, `[orders]/[impressions]`

   1. Seleccione un(a) **[!UICONTROL Data type]**.

      - **[!UICONTROL String]** o **[!UICONTROL Date time]**, cuando la categoría seleccionada es Dimension.
      - **[!UICONTROL Number]** o **[!UICONTROL Currency]** cuando la categoría seleccionada es Métrica o Derivada.

   1. Seleccione **[!UICONTROL Submit]** para agregar el campo armonizado. Seleccione **[!UICONTROL Close]** para cerrar el cuadro de diálogo sin agregar el campo armonizado.

      ![Crear un campo](/help/assets/create-field.png)


### Editar un campo armonizado

Solo puede editar campos armonizados creados anteriormente (el propietario es el cliente). No se puede editar un campo armonizado global.

Para editar un campo armonizado, en la interfaz ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** del Mix Modeler:

1. Seleccione el campo armonizado que desea editar. Por ejemplo, **[!UICONTROL Region]**.

1. En el panel **[!UICONTROL Edit harmonization values]**, modifique los valores de **[!UICONTROL Display name]**, **[!UICONTROL Category]** y **[!UICONTROL Data type]**. Consulte [Agregar un campo armonizado](#add-a-harmonized-field) para obtener más información.

1. Seleccione **[!UICONTROL Submit]** para aplicar los cambios al campo armonizado.

   ![Editar un campo](/help/assets/edit-field.png)

### Eliminar un campo armonizado

Solo puede eliminar los campos armonizados que haya creado anteriormente (el propietario es el cliente). No se puede eliminar un campo armonizado global.

Para eliminar un campo armonizado, en la interfaz ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** del Mix Modeler:

1. Seleccione el campo armonizado que desea eliminar, por ejemplo **[!UICONTROL Region]**.

1. Seleccione ![Eliminar](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** del panel izquierdo **[!UICONTROL Edit harmonization values]**.

   >[!WARNING]
   >
   >   El campo se eliminará inmediatamente.

