---
title: Datos del modelo
description: Obtenga información sobre cómo obtener detalles acerca del modelo, como información general histórica, perspectivas del modelo y calidad del modelo en Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: af315f4566c34c1961130d61ce2804b98d859b24
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Datos del modelo

Para ver la información del modelo, en la interfaz de ![Modelos](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** del Mix Modeler:

1. En la tabla **[!UICONTROL Models]**, seleccione el nombre de un modelo que tenga **[!UICONTROL Last run status]** de <span style="color:green">●</span> **[!UICONTROL Success]**.

1. En el menú contextual, seleccione **[!UICONTROL Model Insights]**.

![Barra de fichas de información del modelo](/help/assets/model-insights-tabbar.png)

Verá cuándo se actualizó por última vez el modelo especificado y cuándo se muestran las visualizaciones mediante cuatro fichas: [Información del modelo](#model-insights), [Atribución](#attribution), [Factores](#factors), [Diagnósticos](#diagnostics) y [Información general histórica](#historical-overview).

Puede cambiar el periodo de fecha en el que se basan las visualizaciones de cada una de las pestañas. Escriba un período de fecha o seleccione ![Calendario](/help/assets/icons/Calendar.svg) para elegir un período de fecha.

## [!UICONTROL Model insights]

La pestaña Información del modelo muestra visualizaciones para [Contribución por fecha y medios base](#contribution-by-date-and-base-media), [Contribución por canal](#contribution-by-channel), [Resumen de rendimiento de marketing](#marketing-performance-summary) y [Curvas de respuesta marginales](#marginal-response-curves). La pestaña también proporciona una tabla [Desglose de puntos de contacto](#touchppint-breakdown).

![Modelo - Datos del modelo](/help/assets/model-insights-insights.png)

* Puede situarse sobre elementos de gráfico individuales en cada visualización para mostrar una ventana emergente con más detalles.

* Para descargar un archivo CSV que contenga los datos de la visualización, seleccione ![Descargar](/help/assets/icons/Download.svg).

* Para descargar datos completos de información del modelo en formato Microsoft® Excel, seleccione ![Descargar](/help/assets/icons/Download.svg) **[!UICONTROL Download data]**.


### Contribución por fecha y medios base.

El gráfico apilado está ordenado: canales base en la parte inferior, canales de no gasto en el centro y canales de gasto en la parte superior.

### Contribución por canal

La visualización de anillo muestra una distribución de la contribución por canal.

### Resumen de rendimiento de marketing.

Gráfico de barras horizontales que muestra el rendimiento de la inversión por canal.

### Curvas de respuesta marginales.

El gráfico de líneas visualiza y compara los retornos marginales generados por la inversión en sus canales de marketing.  E identifica el punto de equilibrio en el que el retorno incremental es menor que el gasto incremental. Como resultado, esta visualización le ayuda a comprender cuándo la inversión en marketing empieza a tener menos impacto.

La curva, el punto de equilibrio y los valores correspondientes se calculan en función del rango de datos seleccionado y del canal seleccionado.

Para cambiar el canal:

* Seleccione un canal del menú desplegable **[!UICONTROL Channel]** para actualizar la visualización de un canal específico.



## [!UICONTROL Attribution]

>[!NOTE]
>
>La pestaña Atribución solo está disponible para modelos con MTA habilitado.


Con la ficha [!UICONTROL Attribution], puede comprender la eficacia de los puntos de contacto y las campañas de marketing que tienen datos de nivel de evento.  Consulte [Crear un modelo](create.md).

Se admiten los siguientes modelos de atribución:

* En función del modelo seleccionado en Mix Modeler:
   * Algorítmico: influenciado
   * Algorítmico: incremental
* Basado en reglas:
   * Unidades de deterioro
   * Primer contacto
   * Último contacto
   * Lineal
   * Ushape

Consulte [Atribución multitáctil](../get-started/about.md#multi-touch-attribution) para obtener una introducción sobre la capacidad de atribución multitáctil en Mix Modeler.

Seleccione uno o varios modelos de atribución en el menú desplegable **[!UICONTROL Attribution Model]**. Los modelos de atribución seleccionados se aplican a todas las visualizaciones de la pestaña Atribución.

![Atribución](/help/assets/model-insights-attribution.png)

Las puntuaciones de evento granulares de atribución de múltiples contactos del Mix Modeler se alinean con las puntuaciones de Mix Modeler generales y los ROI. Estas puntuaciones también están disponibles como conjuntos de datos en Experience Platform.

La pestaña Atribución consta de las siguientes visualizaciones:

### [!UICONTROL Overview]

La visualización [!UICONTROL Overview] muestra, para los modelos de atribución seleccionados, las conversiones totales y porcentajes. Al seleccionar más modelos, se añaden círculos adicionales a la visualización, cada uno con su propio color correspondiente a la leyenda.

Para ver una ventana emergente con detalles para un modelo de atribución, pase el ratón sobre cualquiera de los círculos de la visualización.

### [!UICONTROL Trends]

La visualización [!UICONTROL Daily trends], [!UICONTROL Weekly trends] o [!UICONTROL Monthly trends] muestra, para los modelos de atribución seleccionados, las tendencias de conversión diarias, semanales o mensuales.

Para elegir el período, seleccione **[!UICONTROL Daily trends]**, **[!UICONTROL Weekly trends]** o **[!UICONTROL Monthly trends]** de entre ![Más](/help/assets/icons/More.svg).

Para ver los detalles, pase el ratón sobre la línea de datos de un modelo de atribución específico para mostrar una ventana emergente que muestre el número total de conversiones para esos datos.

### [!UICONTROL Breakdown]

La visualización [!UICONTROL Breakdown] es un desglose por canal o punto de contacto de las conversiones de cada uno de los modelos de atribución seleccionados. Esta visualización puede resultar útil para tomar decisiones sobre la eficacia de cada canal o punto de contacto.

Para elegir el tipo de desglose, seleccione **[!UICONTROL Breakdown by channel]** o **[!UICONTROL Breakdown by touchpoint]** de ![Más](/help/assets/icons/More.svg).

Para ver los detalles, pase el ratón sobre cualquiera de los elementos del gráfico.

### [!UICONTROL Top campaigns]

La visualización Campañas principales muestra una tabla de las campañas principales con columnas para Nombre de campaña, Canal, Tipo de medio y Conversiones incrementales. Esta visualización puede ayudar a informar a su equipo de la eficacia de una campaña específica para un canal determinado y proporcionar perspectivas sobre las campañas en las que debe invertir más.

Para ordenar la tabla en orden ascendente ↑ o descendente ↓ para el canal, el tipo de medio o las conversiones incrementales, seleccione el encabezado de la columna y cambie la ordenación.

Para expandir la tabla en un cuadro de diálogo independiente, seleccione **[!UICONTROL Expand]** de ![Más](/help/assets/icons/More.svg).

El cuadro de diálogo Campañas principales expandido muestra la misma tabla con columnas adicionales para

* Conversiones incrementales
* Conversiones influenciadas
* Conversiones de primer contacto
* Conversiones de último contacto

  Puede seleccionar cada uno de los encabezados de columna adicionales para ordenar la tabla en orden ascendente o descendente.

Para cerrar el cuadro de diálogo Campañas principales expandido, seleccione **[!UICONTROL Close]**.


### [!UICONTROL Breakdown by touchpoint position]

La visualización [!UICONTROL Breakdown by touchpoint position] es un desglose de conversiones atribuidas por posición del punto de contacto y del punto de contacto en todas las rutas de conversión. Este gráfico le ayuda a comparar si un punto de contacto contribuye mejor en una posición que las posiciones restantes y otros puntos de contacto en cualquier posición.

>[!NOTE]
>
>La suma de la contribución porcentual para un modelo de atribución en todos los puntos de contacto y posiciones debe ser igual a 100.


Las posiciones [!UICONTROL Starter], [!UICONTROL Player] y [!UICONTROL Closer] se definen de la siguiente manera:

| Posición | Descripción |
|---|---|
| [!UICONTROL Starter] | Esta posición indica si el punto de contacto es el primer contacto en una ruta de conversión. |
| [!UICONTROL Player] | Esta posición indica si el punto de contacto no es el primer ni el último contacto que provocó la conversión. |
| [!UICONTROL Closer] | Esta posición indica si el punto de contacto es el último contacto antes de la conversión. |


### [!UICONTROL Top conversion paths]

La visualización [!UICONTROL Top conversion paths] muestra las 5 rutas de conversión principales en función de los modelos de atribución seleccionados.

Para cada ruta de conversión, verá lo siguiente:

* la cantidad de canales que sí tienen impacto,
* el total de rutas atribuidas,
* el porcentaje de rutas atribuidas para esta ruta de conversión frente al total de rutas atribuidas,
* para cada canal, el porcentaje de contribución del modelo de atribución y
* la suma de estos porcentajes de contribución del modelo de atribución de canal.

## **[!UICONTROL Factors]**

La pestaña Factores muestra perspectivas relacionadas con factores externos.

![Factores](/help/assets/factors.png)

Esta visualización le ayuda a comprender el efecto incremental que varios factores internos y externos tienen en la línea de base de las conversiones. Por ejemplo, condiciones económicas o actividades promocionales.


Para descargar un archivo CSV que contenga los datos de la tabla, seleccione ![Descargar](/help/assets/icons/Download.svg).

Si no hay datos disponibles, verá un mensaje ![TableAndChart](/help/assets/icons/TableAndChart.svg) **[!UICONTROL No data is available, you may need to retrain your model, or change the date range to view insights]**.

## [!UICONTROL Diagnostics]

La pestaña Diagnóstico muestra visualizaciones para:

* Visualización [!UICONTROL Model Assessment], que puede desglosar en conversiones reales frente a previstas o residuales.

  Para desglosar la visualización, seleccione **[!UICONTROL Actual vs. Predicted]** o **[!UICONTROL Residuals]** de la lista **[!UICONTROL Breakdown]**.

* [!UICONTROL Model fitting metrics] tabla, que muestra las siguientes columnas para cada métrica de conversión:

   * Conversión real

   * Conversión modelada

   * Conversión residual (diferencia entre conversión real y modelada)

   * Valores de puntuación de calidad del modelo:

      * R2 (R cuadrado), que indica cómo se ajustan los datos al modelo de regresión (la bondad de ajuste).

      * MAPE (Error de porcentaje absoluto medio), que es uno de los KPI más utilizados para medir la precisión de la previsión y expresa el error de la previsión como un porcentaje del valor real.

      * RMSE (Error Cuadrado Medio Raíz): que muestra el error medio, ponderado según el cuadrado del error.

  Para descargar un archivo CSV que contenga los datos de la tabla, seleccione ![Descargar](/help/assets/icons/Download.svg).

* [!UICONTROL Touchpoint effectiveness], que representa el resultado del modelo algorítmico de Attribution AI. Los datos de esta tabla solo se generan para periodos de tiempo específicos. Seleccione **[!UICONTROL As of *xx/xx/xx, xx:xx TZ *]**![Información](/help/assets/icons/InfoOutline.svg) para obtener más información.

  La visualización muestra, en orden descendente de [!UICONTROL Efficiency measure] ![Orden descendente](/help/assets/icons/SortOrderDown.svg), para cada punto de contacto:

   * [!UICONTROL Paths touched]: visualiza el porcentaje de rutas que consiguen conversión y el porcentaje de rutas que no logran conversión. Para un punto de contacto, verá conversiones atribuidas más cuando la proporción de conversión de atribución sea alta. Esta proporción compara el porcentaje de rutas que llevan a la conversión frente al porcentaje de rutas que llevan a la conversión *no*.
   * [!UICONTROL Efficiency measure]: generado por el modelo de atribución algorítmica, la medida de eficiencia indica la importancia relativa de un punto de contacto hacia la conversión, independientemente del volumen del punto de contacto. La eficiencia se mide en una escala de 1 a 5. Tenga en cuenta que un volumen de punto de contacto más alto no garantiza una medida de eficiencia más alta.
   * [!UICONTROL Total volume]: el número agregado de veces que un usuario toca un punto de contacto. El número incluye los puntos de contacto que aparecen en una ruta que logra la conversión, así como las rutas *no* que resultan en conversión.

![Diagnóstico](/help/assets/model-insights-diagnostics.png)


## [!UICONTROL Historical overview]

La pestaña Información general histórica muestra visualizaciones para:

* Conversión y gasto por trimestre fiscal y producto.

* Gasto por canal.

* Gasto en Touchpoint.

  Puede seleccionar un canal alternativo basado en el gasto para mostrar en esta visualización. Seleccionar un canal de **[!UICONTROL Channels]**.

* Volumen de Touchpoint.

  Puede seleccionar un canal alternativo basado en volumen para mostrar en esta visualización. Seleccionar un canal de **[!UICONTROL Channels]**.

![Modelo: información general histórica](/help/assets/model-insights-historical-overview.png)
