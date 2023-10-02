---
title: Datos del modelo
description: Obtenga información sobre cómo obtener detalles acerca del modelo, como información general histórica, perspectivas del modelo y calidad del modelo en Mix Modeler.
feature: Models
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '280'
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

* Conversión y gasto por trimestre fiscal y producto

* Gasto por canal

* Gasto de Touchpoint

  Puede seleccionar un canal alternativo basado en gastos para mostrar para este widget. Seleccionar un canal de **[!UICONTROL Channels]**.

* Volumen de Touchpoint

  Puede seleccionar un canal alternativo basado en volumen para mostrar para este widget. Seleccionar un canal de **[!UICONTROL Channels]**.



![Modelo: información general histórica](../assets/model-historical-overview.png)


## Datos del modelo

La pestaña Información del modelo muestra los widgets de:

* Contribución por fecha y medios base

* Contribución por canal

* Resumen de rendimiento de marketing

Puede situarse sobre elementos de gráfico individuales en cada widget para ver una ventana emergente con más detalles.

![Modelo: perspectivas del modelo](../assets/model-model-insights.png)


## Calidad de modelo

La pestaña Calidad del modelo muestra widgets para medir:

* R2 (R cuadrado), que indica cómo se ajustan los datos al modelo de regresión (la bondad de ajuste).

* MAPE (Error de porcentaje absoluto medio), que es uno de los KPI más utilizados para medir la precisión de la previsión y expresa el error de la previsión como un porcentaje del valor real.

* RMSE (Error Cuadrado Medio Raíz): que muestra el &quot;error&quot; promedio, ponderado según el cuadrado del error.

![Calidad de modelo](../assets/model-quality.png)


