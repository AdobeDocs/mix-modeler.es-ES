---
title: Esquemas
description: Aprenda a administrar los esquemas necesarios para la ingesta de datos en el Modelador de mezcla de Adobe.
feature: Schemas
source-git-commit: 4a6cbda1ff0a779ebf8a38a4de3f797ed9e54b00
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# Esquemas

Para administrar esquemas compatibles con los datos que desea introducir en Adobe Experience Platform y utilizar en el Modelador de mezcla de Adobe:

1. Vaya a la interfaz del Modelador de mezcla de Adobe.

1. Seleccionar ![Esquemas](../assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, debajo **[!UICONTROL DATA MANAGEMENT]**.

Consulte la [Resumen de IU de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en) para obtener más información.

## Datos agregados o resumidos

Se recomienda encarecidamente utilizar la clase Métricas de resumen de XDM como base del esquema subyacente a cualquier dato agregado o de resumen que desee introducir en Experience Platform y utilizarlo en el Modelador de mezcla de Adobe.

Consulte a continuación un ejemplo de **[!DNL LumaPaidMarketingSchema]** uso de las métricas de resumen de XDM como clase base y grupos de campos dedicados (anotados con colores) para la métrica (**[!DNL AMMMetrics]**), dimensiones (**[!DNL AMMDimensions]**) y otra información específica del cliente (**[!DNL CustomerSpecific]**).

![Esquema de resumen](../assets/summary-schema.png)

Para definir un conjunto de propiedades de auditoría, se recomienda encarecidamente utilizar el grupo de campos Detalles de auditoría del sistema de origen externo, como parte de un esquema utilizado para recopilar datos agregados o de resumen de fuentes externas.
