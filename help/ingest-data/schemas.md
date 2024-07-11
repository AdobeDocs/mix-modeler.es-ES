---
title: Esquemas
description: Aprenda a administrar los esquemas necesarios para introducir datos en Mix Modeler.
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 3%

---

# Esquemas

Para administrar esquemas compatibles con los datos que desea introducir en Experience Platform y utilizar en Mix Modeler:

1. Vaya a la interfaz del Mix Modeler.

1. Seleccionar ![Esquemas](/help/assets//icons/Schemas.svg) **[!UICONTROL Schemas]**, debajo **[!UICONTROL SETUP]**.

Consulte la [Resumen de IU de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en) para obtener más información.

## Datos agregados o resumidos

Se recomienda encarecidamente utilizar la clase Métricas de resumen de XDM como base del esquema subyacente a cualquier dato agregado o de resumen que desee introducir en Experience Platform y utilizar en Mix Modeler.

Utilice la clase Métricas de resumen de XDM para:

- datos del huerto amurallado, por ejemplo, datos de Facebook o YouTube.

- datos de factores externos, como datos de SPX (índices bursátiles S&amp;P 500), datos meteorológicos,

- datos de factores internos como, por ejemplo, cambios de precios o un calendario festivo.

>[!IMPORTANT]
>
>La definición del esquema debe contener al menos un campo numérico (con tipo entero, doble, booleano u otro tipo numérico) para admitir las métricas necesarias para los datos introducidos.

Un esquema con la variable **[!DNL XDM Summary Metrics]** la clase base puede ser simple, como se muestra en la **[!DNL ExternalFactorSummarySchema]** más abajo.

![Esquema de factores externos](/help/assets//external-factors-schema.png)

Este esquema simple se puede utilizar para introducir conjuntos de datos que contengan datos para, por ejemplo:

- Datos del índice del competidor

  | timestamp | date_type | factor | valor |
  |---|---|---|--:|
  | 28T00-11-2020:00:00,000Z | semana | competitor_index | 289,8 |
  | 05T00-12-2020:00:00,000Z | semana | competitor_index | 291,2 |
  | 12T00-12-2020:00:00,000Z | semana | competitor_index | 280,07 |
  | ... | ... | ... | ... |

- Datos de festivos públicos

  | timestamp | date_type | factor | valor |
  |---|---|---|--:|
  | 28T00-11-2020:00:00,000Z | semana | all_holiday_flag | 0,0 |
  | 05T00-12-2020:00:00,000Z | semana | all_holiday_flag | 0,0 |
  | 12T00-12-2020:00:00,000Z | semana | all_holiday_flag | 0,0 |
  | 19-12-2020:00:00,000Z | semana | all_holiday_flag | 0,0 |
  | 26-12-2020:00:00,000Z | semana | all_holiday_flag | 1,0 |
  | ... | ... | ... | ... |


Consulte a continuación un ejemplo más completo de una **[!DNL LumaPaidMarketingSchema]** uso del **[!DNL XDM Summary Metrics]** como clase base. El esquema utiliza grupos de campos dedicados (anotados con colores) para las métricas (**[!DNL AMMMetrics]**), dimensiones (**[!DNL AMMDimensions]**) y otra información específica del cliente (**[!DNL CustomerSpecific]**).

![Esquema de resumen](/help/assets//summary-schema.png)

Dada la naturaleza asíncrona de la ingesta de perfiles, al recopilar datos acumulados o resumidos de fuentes externas, se recomienda utilizar el grupo de campos Detalles de auditoría del sistema de Source externo como parte de un esquema. Este grupo de campos define un conjunto de propiedades de auditoría para orígenes externos.


## Tipos de datos admitidos

Actualmente, Mix Modeler no admite un subconjunto de tipos de datos de Experience Platform. Los siguientes tipos de datos básicos (campos), mencionados en [Conceptos básicos de composición de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#data-type), son compatibles:

- Cadena
- Entero
- Doble
- Booleano
- Largo
- Corto
- Byte
- Fecha
- Fecha-hora
