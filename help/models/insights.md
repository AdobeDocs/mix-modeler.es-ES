---
title: Datos del modelo
description: Obtenga información sobre cómo obtener detalles acerca del modelo, como información general histórica, perspectivas del modelo y calidad del modelo en Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 4f4c7f05e90d73a0ab4865150b1ec4c2af88fc12
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# Datos del modelo

Para ver la información del modelo, en ![Modelos](../assets/icons/FileData.svg) **[!UICONTROL Models]** interfaz en el Mix Modeler:

1. Seleccione el nombre de un modelo con una **[!UICONTROL Last run status]** de <span style="color:green">●</span> **[!UICONTROL Success]** desde el **[!UICONTROL Models]** tabla.

1. En el menú contextual, seleccione **[!UICONTROL Model Insights]**.

Verá cuándo se actualizó por última vez el modelo especificado y se mostrarán los widgets mediante tres pestañas: Información general histórica, Perspectivas del modelo y Calidad del modelo.

Puede cambiar el periodo de fecha en el que se basan los widgets de cada una de las pestañas. Introduzca un periodo de fecha o seleccione ![Calendario](../assets/icons/Calendar.svg) para seleccionar un periodo de fecha.


## Resumen histórico

La pestaña Información general histórica muestra los widgets de:

* Conversión y gasto por trimestre fiscal y producto.

* Gasto por canal.

* Gasto en Touchpoint.

  Puede seleccionar un canal alternativo basado en gastos para mostrar para este widget. Seleccionar un canal de **[!UICONTROL Channels]**.

* Volumen de Touchpoint.

  Puede seleccionar un canal alternativo basado en volumen para mostrar para este widget. Seleccionar un canal de **[!UICONTROL Channels]**.

![Modelo: información general histórica](../assets/model-historical-overview.png)

## Datos del modelo

La pestaña Información del modelo muestra los widgets de:

* Contribución por fecha y medios base. El gráfico apilado está ordenado: canales base en la parte inferior, canales de no gasto en el centro y canales de gasto en la parte superior.

* Contribución por canal.

* Resumen de rendimiento de marketing.

* Curvas de respuesta marginales.

![Modelo: perspectivas del modelo](../assets/model-model-insights.png)

Puede situarse sobre elementos de gráfico individuales en cada widget para mostrar una ventana emergente con más detalles.

Para descargar un archivo CSV que contenga los datos del widget, seleccione ![Descargar](../assets/icons/Download.svg).

Para descargar datos de perspectivas de modelo completos en formato Microsoft® Excel, seleccione ![Descargar](../assets/icons/Download.svg) **[!UICONTROL Download data]**.


## Calidad de modelo

![Evaluación de la calidad del modelo](/help/assets/model-quality-assessment.png)
La pestaña de calidad del modelo muestra un

* [!UICONTROL Model Assessment] , que puede desglosar según las conversiones reales frente a las previstas o residuales.

  Para desglosar la visualización, seleccione **[!UICONTROL Actual vs. Predicted]** o **[!UICONTROL Residuals]** desde el **[!UICONTROL Breakdown]** lista.

* [!UICONTROL Model fitting metrics] , mostrando las siguientes columnas para cada métrica de conversión:

   * Conversión real

   * Conversión modelada

   * Conversión residual (diferencia entre conversión real y modelada)

   * Valores de puntuación de calidad del modelo:

      * R2 (R cuadrado), que indica cómo se ajustan los datos al modelo de regresión (la bondad de ajuste).

      * MAPE (Error de porcentaje absoluto medio), que es uno de los KPI más utilizados para medir la precisión de la previsión y expresa el error de la previsión como un porcentaje del valor real.

      * RMSE (Error Cuadrado Medio Raíz): que muestra el &quot;error&quot; promedio, ponderado según el cuadrado del error.

  Para descargar un archivo CSV que contenga los datos de la tabla, seleccione ![Descargar](../assets/icons/Download.svg).
