---
title: Корпоративные параметры конфиденциальности Microsoft Edge
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 09/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Настройка корпоративных параметров конфиденциальности Microsoft Edge
ms.openlocfilehash: 9af3ce14b9ee717d4c64fa3b920e8c63224613e6
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617779"
---
# <a name="configure-microsoft-edge-policies-to-support-enterprise-privacy"></a>Настройка политик Microsoft Edge для поддержки корпоративной конфиденциальности

Корпорация Майкрософт стремится предоставлять организациям сведения и средства управления, необходимые для принятия решений о сборе данных в Microsoft Edge.

## <a name="overview"></a>Обзор

При развертывании Microsoft Edge в Windows 10 диагностические данные по умолчанию отправляются на основании пользовательского [параметра диагностических данных Windows](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

При развертывании Microsoft Edge на платформах, отличных от Windows, диагностические данные собираются в соответствии с параметрами следующих групповых политик.

- (НЕ РЕКОМЕНДУЕТСЯ) [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) — включить отчеты с данными об использовании и сбоях. Эта политика станет устаревшей в Microsoft Edge версии 89.
- (НЕ РЕКОМЕНДУЕТСЯ) [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) — отправка сведений о сайтах для улучшения служб Майкрософт. Эта политика станет устаревшей в Microsoft Edge версии 89.

Предыдущие нерекомендуемые политики заменяются политикой [Разрешить телеметрию](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) в Windows 10 и политикой [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) для всех остальных платформ.  

## <a name="configure-policy-settings"></a>Настройка параметров политик.

Прежде чем приступить к работе, скачайте и используйте последний шаблон политик Microsoft Edge (дополнительные сведения см. в разделе [Настройка Microsoft Edge](configure-microsoft-edge.md)).

### <a name="send-required-and-optional-diagnostic-data-about-browser-usage"></a>Отправлять обязательные и необязательные диагностические данных об использовании браузера

Если политика [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) настроена, она имеет приоритет перед политиками [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) и [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices).

#### <a name="required-and-optional-diagnostic-data"></a>Обязательные и необязательные диагностические данные

Обязательные диагностические данные собираются для защиты, обеспечения актуальности и правильной работы Microsoft Edge.

Необязательные диагностические данные включают данные об использовании браузера, посещаемых веб-сайтах, а также отчеты о сбоях с целью защиты, обеспечения актуальности и правильной работы Microsoft Edge. Они используются для улучшения Microsoft Edge, а также других продуктов и служб Майкрософт для всех пользователей.

> [!NOTE]
> Эта политика не поддерживается на устройствах с Windows 10. Чтобы управлять сбором данных в Windows 10, ИТ-администраторы должны использовать групповую политику диагностических данных Windows. Эта политика называется **Разрешить телеметрию** или **Разрешить диагностические данные** в зависимости от версии Windows. Узнайте больше о [сборе диагностических данных Windows 10](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

Используйте один из следующих параметров для настройки политики **DiagnosticData**:

- "Выкл" (не рекомендуется) (0) — отключает сбор обязательных и необязательных диагностических данных. 
- "Обязательные данные" (1) — отправляет обязательные диагностические данные, но отключает сбор необязательных диагностических данных. Microsoft Edge отправляет обязательные диагностические данные, необходимые для защиты, обеспечения актуальности и правильной работы Microsoft Edge. 
- "Необязательные данные" (2) — отправляет необязательные диагностические данные, включающие данные об использовании браузера, посещенных веб-сайтах и отчеты о сбоях в корпорацию Майкрософт с целью защиты, обеспечения актуальности и правильной работы Microsoft Edge. Они используются для улучшения Microsoft Edge, а также других продуктов и служб Майкрософт для всех пользователей.

В Windows 7, Windows 8/8.1 и macOS эта политика управляет отправкой обязательных и необязательных данных в Майкрософт.

Если эта политика не настроена или отключена, Microsoft Edge будет по умолчанию использовать параметры пользователя.

### <a name="deprecated-enable-usage-and-crash-related-data-reporting"></a>(НЕ РЕКОМЕНДУЕТСЯ) Включение отчетов с данными об использовании и сбоях

Политика **MetricsReportingEnabled** позволяет отправлять отчеты с данными об использовании и сбоях Microsoft Edge в корпорацию Майкрософт.

Microsoft Edge собирает ряд обязательных данных, необходимых для обеспечения безопасности, актуальности и надлежащей работы продукта. К этим данным относятся базовые сведения о подключении и конфигурации устройства из Microsoft Edge (текущее состояние согласия на сбор данных, версия приложения и состояние установки Microsoft Edge). Сбор этих данных можно отключить, отключив политику.

Включите эту политику, чтобы отправлять отчеты с данными об использовании и сбоях в корпорацию Майкрософт. Отключите эту политику, чтобы не отправлять эти данные в корпорацию Майкрософт. В обоих случаях пользователи не смогут изменить или переопределить его.

При запуске Microsoft Edge в Windows 10:

- Если эта политика не настроена, Microsoft Edge по умолчанию использует параметр диагностических данных Windows.
- Если эта политика включена, Microsoft Edge будет отправлять данные об использовании, только если для параметра диагностических данных Windows задано значение **Расширенный** или **Полный**.
  - Если эта политика включена, Microsoft Edge будет отправлять данные об использовании только в том случае, если также включена политика [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices).
- Если эта политика отключена, Microsoft Edge не будет отправлять данные об использовании. Данные о сбоях отправляются в зависимости от параметра диагностических данных Windows. [Дополнительные сведения о параметрах диагностических данных Windows](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

При запуске Microsoft Edge в Windows 7, 8 и macOS:

- Если эта политика не настроена, Microsoft Edge по умолчанию применяет настройки пользователя.
-  Если эта политика включена, Microsoft Edge будет отправлять данные об использовании только в том случае, если также включена политика [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices).

### <a name="deprecated-send-site-information-to-improve-microsoft-services"></a>(НЕ РЕКОМЕНДУЕТСЯ) Отправка сведений о сайтах для улучшения служб Майкрософт

Политика **SendSiteInformationToImproveServices** позволяет отправлять сведения о веб-сайтах, посещенных в Microsoft Edge, в корпорацию Майкрософт для улучшения продуктов и служб, таких как поиск.

Включите эту политику, чтобы отправлять сведения о посещаемых вами веб-сайтах с помощью Microsoft Edge в Майкрософт. Отключите эту политику, чтобы не отправлять сведения о посещаемых вами веб-сайтах с помощью Microsoft Edge в Майкрософт. В обоих случаях пользователи не смогут изменить или переопределить его.

При запуске Microsoft Edge в Windows 10:

- Если эта политика не настроена, Microsoft Edge по умолчанию использует параметр диагностических данных Windows.
- Если эта политика включена, Microsoft Edge будет отправлять данные о посещаемых веб-сайтах, только если для параметра диагностических данных Windows задано значение **Полный**.
  - Если эта политика включена, Microsoft Edge будет отправлять данные об использовании только в том случае, если также включена политика [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled). 
- Если эта политика отключена, Microsoft Edge не будет отправлять данные о посещаемых веб-сайтах. [Дополнительные сведения о параметрах диагностических данных Windows](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

При запуске Microsoft Edge в Windows 7, 8 и macOS:

- Если эта политика включена, Microsoft Edge будет отправлять данные об использовании только в том случае, если также включена политика [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled).
- Если эта политика не настроена, Microsoft Edge по умолчанию применяет настройки пользователя.

## <a name="implementation-details"></a>Сведения о реализации

Для устройств, отличных от Windows 10: 
- Если политика [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) настроена, она имеет приоритет перед политиками [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) и [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices). 
- Если политика [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) не настроена, Microsoft Edge обращается к политикам [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) и [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices).  

Чтобы разъяснить нашу реализацию для Windows 10 с зависимостью от параметра диагностических данных Windows, в таблице ниже указано, отправляются ли  **обязательные** и **необязательные** диагностические данные в Майкрософт.

| Параметр диагностических данных Windows | Необходимые диагностические данные  | Дополнительные диагностические данные |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| Безопасность                        | Не отправляются                                      | Не отправляются                                            |
| Базовый                           | Отправляются                                      | Не отправляются                                            |
| Расширенный                        | Отправляются                                          | Не отправляются                                            |
| Полный                            | Отправляются                                          | Отправляются                                                |

> [!IMPORTANT]
> Microsoft Edge поддерживает **MetricsReportingEnabled** и **SendSiteInfoToImproveServices** в версиях 86—88 включительно. В Microsoft Edge версии 89 **MetricsReportingEnabled** и **SendSiteInfoToImproveServices** больше не будут поддерживаться, и по умолчанию будет использоваться политика **DiagnosticData** на платформах, отличных от Windows 10, или политика **Разрешить телеметрию** для Windows 10.

## <a name="additional-privacy-policy-options"></a>Дополнительные параметры политики конфиденциальности

Возможно, вам потребуется использовать следующие групповые политики, связанные с конфиденциальностью данных.

- Блокировка cookie-файлов на определенных сайтах
- Блокировка сторонних cookie-файлов
- Настройка запрета на отслеживание
- Отключение режима InPrivate

## <a name="see-also"></a>Статьи по теме

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Политики Microsoft Edge](microsoft-edge-policies.md)
- [Техническая документация по конфиденциальности Microsoft Edge](/microsoft-edge/privacy-whitepaper)