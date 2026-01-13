---
title: Esquemas
description: Aprenda a administrar los esquemas necesarios para la ingesta de datos en Mix Modeler.
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
source-git-commit: 7524c2ffc0408b04e6bef5bd5deedc1feea0b682
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 4%

---

# Esquemas

Para administrar esquemas compatibles con los datos que desea introducir en Experience Platform y utilizar en Mix Modeler:

1. Vaya a la interfaz de Mix Modeler.

1. Seleccione ![Esquemas](/help/assets/icons/Schemas.svg) **[!UICONTROL Schemas]**, debajo de **[!UICONTROL SETUP]**.

Consulte la [descripción general de la interfaz de usuario de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=es) para obtener más información.

## Datos agregados o resumidos

Se recomienda encarecidamente utilizar la clase Métricas de resumen de XDM como base del esquema subyacente a cualquier dato agregado o de resumen que desee introducir en Experience Platform y utilizar en Mix Modeler.

Utilice la clase Métricas de resumen de XDM para:

- datos del huerto amurallado, por ejemplo, datos de Facebook o YouTube.

- datos de factores externos, como datos de SPX (índices bursátiles S&amp;P 500), datos meteorológicos,

- datos de factores internos como, por ejemplo, cambios de precios o un calendario festivo.

>[!IMPORTANT]
>
>La definición del esquema debe contener al menos un campo numérico (con tipo entero, doble, booleano u otro tipo numérico) para admitir las métricas necesarias para los datos introducidos.

Un esquema que use la clase base **[!DNL XDM Summary Metrics]** puede ser sencillo, como se muestra en el **[!DNL ExternalFactorSummarySchema]** siguiente.

![Esquema de factores externos](/help/assets/external-factors-schema.png)

Este esquema simple se puede utilizar para introducir conjuntos de datos que contengan datos para, por ejemplo:

- Datos del índice del competidor

  | timestamp | date_type | factor | valor |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | semana | competitor_index | 289,8 |
  | 2020-12-05T00:00:00.000Z | semana | competitor_index | 291,2 |
  | 2020-12-12T00:00:00.000Z | semana | competitor_index | 280,07 |
  | ... | ... | ... | ... |

- Datos de festivos públicos

  | timestamp | date_type | factor | valor |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | semana | all_holiday_flag | 0,0 |
  | 2020-12-05T00:00:00.000Z | semana | all_holiday_flag | 0,0 |
  | 2020-12-12T00:00:00.000Z | semana | all_holiday_flag | 0,0 |
  | 2020-12-19T00:00:00.000Z | semana | all_holiday_flag | 0,0 |
  | 2020-12-26T00:00:00.000Z | semana | all_holiday_flag | 1,0 |
  | ... | ... | ... | ... |


Vea a continuación un ejemplo más completo de un(a) **[!DNL LumaPaidMarketingSchema]** que usa el(la) **[!DNL XDM Summary Metrics]** como clase base. El esquema utiliza grupos de campos dedicados (anotados con colores) para métricas (**[!DNL AMMMetrics]**), dimensiones (**[!DNL AMMDimensions]**) y otra información específica del cliente (**[!DNL CustomerSpecific]**).

![Esquema de resumen](/help/assets/summary-schema.png)

Dada la naturaleza asíncrona de la ingesta de perfiles, al recopilar datos acumulados o resumidos de fuentes externas, se recomienda utilizar el grupo de campos Detalles de auditoría del sistema de Source externo como parte de un esquema. Este grupo de campos define un conjunto de propiedades de auditoría para orígenes externos.

## Grupo de campos Campos estándar de factor

Para su comodidad, Experience Platform admite un grupo de campos Campos de estándar de factores específico para datos de factores internos y externos que a menudo forman parte de datos de factores resumidos, internos o externos. Este grupo de campos define los campos siguientes:

| Nombre para mostrar del campo | Nombre de campo | Tipo de campo | Tipo de datos | Requerido | Descripción |
|---|---|---|---|:-:|---|
| Nombre de factor | factorName | Dimensión | Cadena | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | El nombre del factor |
| Valor de factor | factorValue | Métrica | Doble | ![Marca de verificación](/help/assets/icons/Checkmark.svg) | El valor del factor |
| Tipo de factor | factorType | Dimensión | Cadena (Enumeración) | | El tipo de factor.<br/>Los valores posibles son: <ul><li>Interno (factor interno)</li><li>Externo (factor externo)</li></ul> |
| Tipo de valor | valueType | Dimensión | Cadena (Enumeración) | | Los valores posibles son:<ul><li>Real (valor real)</li><li>Previsto (valor previsto)</li></ul>Si no hay ningún valor, Real es el valor predeterminado. |
| Granularidad | granularidad | Dimensión | Cadena (Enumeración) | | Los valores posibles son:<ul><li>Diario</li><li>Semanalmente</li><li>Mensual</li></ul> |

Un resumen, un factor interno o un conjunto de datos de factor externo puede basarse en:

- Esquema que **utiliza** el grupo Campos estándar de factor. Este conjunto de datos se muestra como un conjunto de datos **[!UICONTROL Factors]** al configurar las reglas del conjunto de datos. Y los campos armonizados que defina, como parte de las reglas del conjunto de datos para el conjunto de datos, están disponibles como factores al crear un modelo.
- Esquema que **no usa** el grupo Campos estándar de factor. Este conjunto de datos se muestra como un conjunto de datos **[!UICONTROL Summary]** al configurar las reglas del conjunto de datos. El conjunto de datos está configurado como datos de resumen y no influye en los datos armonizados.

## Tipos de datos admitidos

Actualmente, Mix Modeler no admite un subconjunto de tipos de datos de Experience Platform. Se admiten los siguientes tipos de datos básicos (campos), mencionados en [Conceptos básicos de composición de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=es#data-type):

- Cadena
- Entero
- Doble
- Booleano
- Largo
- Corto
- Byte
- Fecha
- Fecha-hora


>[!MORELIKETHIS]
>
>- [Esquemas](schemas.md)
