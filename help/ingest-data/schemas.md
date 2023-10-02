---
title: Esquemas
description: Aprenda a administrar los esquemas necesarios para la ingesta de datos en el Modelador de mezcla de Adobe.
feature: Schemas
source-git-commit: b5b277e3476bdf6c0c0da85425bba19bea00c594
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 6%

---


# Esquemas

Para administrar esquemas compatibles con los datos que desea introducir en Adobe Experience Platform y utilizar en el Modelador de mezcla de Adobe:

1. Vaya a la interfaz del Modelador de mezcla de Adobe.

1. Seleccionar ![Esquemas](../assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, debajo **[!UICONTROL DATA MANAGEMENT]**.

Consulte la [Resumen de IU de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en) para obtener más información.

## Datos agregados o resumidos

Se recomienda encarecidamente utilizar la clase Métricas de resumen de XDM como base del esquema subyacente a cualquier dato agregado o de resumen que desee introducir en Experience Platform y utilizarlo en el Modelador de mezcla de Adobe.

Utilice la clase Métricas de resumen de XDM para:

- datos del huerto amurallado, por ejemplo, datos de Facebook o YouTube.

- datos de factores externos, como datos de SPX (índices bursátiles S&amp;P 500), datos meteorológicos,

- datos de factores internos como, por ejemplo, cambios de precios o un calendario festivo.

>[!IMPORTANT]
>
>La definición del esquema debe contener al menos un campo numérico (con tipo entero, doble, booleano u otro tipo numérico) para admitir las métricas necesarias para los datos introducidos.

Un esquema con la variable **[!DNL XDM Summary Metrics]** la clase base puede ser simple, como se muestra en la **[!DNL ExternalFactorSummarySchema]** más abajo.

![Esquema de factores externos](../assets/external-factors-schema.png)

Este esquema sencillo se puede utilizar para introducir conjuntos de datos que contengan datos para:

- Datos del índice del competidor

  | timestamp | date_type | factor | valor |
  |---|---|---|--:|
  | 28T00-11-2020:00:00,000Z | semana | competitor_index | 289.8 |
  | 05T00-12-2020:00:00,000Z | semana | competitor_index | 291.2 |
  | 12T00-12-2020:00:00,000Z | semana | competitor_index | 280.07 |
  | ... | ... | ... | ... |

- Datos de festivos públicos

  | timestamp | date_type | factor | valor |
  |---|---|---|--:|
  | 28T00-11-2020:00:00,000Z | semana | all_holiday_flag | 0.0 |
  | 05T00-12-2020:00:00,000Z | semana | all_holiday_flag | 0.0 |
  | 12T00-12-2020:00:00,000Z | semana | all_holiday_flag | 0.0 |
  | 19-12-2020:00:00,000Z | semana | all_holiday_flag | 0.0 |
  | 26-12-2020:00:00,000Z | semana | all_holiday_flag | 1.0 |
  | ... | ... | ... | ... |


Consulte a continuación un ejemplo más completo de una **[!DNL LumaPaidMarketingSchema]** uso del **[!DNL XDM Summary Metrics]** como clase base. El esquema utiliza grupos de campos dedicados (anotados con colores) para las métricas (**[!DNL AMMMetrics]**), dimensiones (**[!DNL AMMDimensions]**) y otra información específica del cliente (**[!DNL CustomerSpecific]**).

![Esquema de resumen](../assets/summary-schema.png)

Dada la naturaleza asíncrona de la ingesta de perfiles, al recopilar datos acumulados o de resumen de fuentes externas, se recomienda utilizar el grupo de campos Detalles de auditoría del sistema de fuentes externas como parte de un esquema. Este grupo de campos define un conjunto de propiedades de auditoría para orígenes externos.
