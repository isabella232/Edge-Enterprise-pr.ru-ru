---
title: Поддержка платформ для функций Microsoft Edge
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Общие сведения о поддержке платформ для функций Microsoft Edge
ms.openlocfilehash: 1ac512d4e9e6279ce2d6fcff5aebede0974eb5cdcf9211c957ace9f015b95010
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "11727472"
---
# <a name="platform-support-for-microsoft-edge-features"></a>Поддержка платформ для функций Microsoft Edge

В этой статье обобщены сведения о поддержке платформ для функций Microsoft Edge.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## <a name="feature-matrix-for-platforms"></a>Матрица функций для платформ

В следующих таблицах обобщены сведения о поддержке функций для платформ Windows и macOS.

> [!NOTE]
> В настоящее время Android и iOS не представлены в таблицах поддержки, однако мы продолжаем работать в этом направлении и будем обновлять сведения соответствующим образом.

| Функции безопасности |Win 10|Win 8.1|Win 7|macOS|URL-адрес|
|--------|-------|--------|-----|-------|---|
|Условный доступ Azure Active Directory (Azure AD)|Да|Да|Да|Да|[Условный доступ Azure AD](/deployedge/ms-edge-security-conditional-access#accessing-conditional-access-protected-resources-in-microsoft-edge)|
|Application Guard в Microsoft Defender|Да (1890 и более поздние версии)|Нет|Нет|Нет|[Application Guard в Microsoft Defender](/deployedge/microsoft-edge-security-windows-defender-application-guard) |
|Фильтр SmartScreen в Microsoft Defender|Да|Да|Да|Да|[Фильтр SmartScreen в Microsoft Defender](/deployedge/microsoft-edge-security-smartscreen) |
|Защита от потери данных в конечной точке Майкрософт|Да|Нет|Нет|Нет|[Защита от потери данных в конечной точке Майкрософт](/deployedge/microsoft-edge-security-dlp#microsoft-endpoint-data-loss-prevention-endpoint-dlp)|
|Мониторинг паролей|Да|Да|Да|Да|[Мониторинг паролей](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|Генератор паролей|Да|Да|Да|Да|[Генератор паролей](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|Windows Information Protection (WIP)|Да (1607 и более поздние версии)|Нет|Нет|Нет|[WIP](/deployedge/microsoft-edge-security-windows-information-protection#system-requirements)|

|Функции удостоверений| Win 10 | Win 8.1 | Win 7 | macOS | URL-адрес |
|--|--|--|--|--|--|
|Автоматический вход (гибридная среда/AAD-J)|Да|Да|Да|Нет|[Гибридная среда/AAD-J](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Автоматический вход (присоединение к домену)|Да|Да|Да|Нет|[присоединение к домену](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Автоматический вход (стандартная учетная запись ОС — MSA)|Да (1709 и более поздние версии)|Нет|Нет|Нет|[Учетная запись Майкрософт](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Браузер для единого входа через веб-интерфейс (SSO)|Да|Да|Да|Да|[Единый вход в браузере](https://www.microsoft.com/microsoft-365/roadmap?featureid=66332)|
|Управляемое переключение/"Автоматическое переключение профилей"|Да|Да|Да|Да|[Использование нескольких профилей на работе и дома](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|Несколько профилей|Да|Да|Да|Да|[Использование нескольких профилей на работе и дома](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|Локальная синхронизация для Active Directory (AD)|Да|Да|Да|Нет|[Локальная синхронизация для пользователей Active Directory (AD)](/deployedge/microsoft-edge-on-premises-sync) |
|Простой единый вход|Да (1709 и более поздние версии)|Да|Да|Да|[Простой единый вход](/deployedge/microsoft-edge-security-identity#seamless-sso)|
|Единый вход с основным маркером обновления (PRT)|Да (1709 и более поздние версии)|Да|Да|Нет|[Единый вход с PRT](/deployedge/microsoft-edge-security-identity#sso-with-primary-refresh-token-prt)|
|Встроенная проверка подлинности Windows (WIA)|Да|Да|Да|Да* (требуется политика)|[WIA](/deployedge/microsoft-edge-security-identity#windows-integrated-authentication-wia)|

|Дополнительные возможности|Win 10|Win 8.1|Win 7|macOS|URL-адрес|
|--------|-------|--------|-----|-------|---|
|Коллекции|Да|Да|Да|Да|[Коллекции](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/) |
|Корпоративная страница новой вкладки|Да|Да|Да|Да|[Страница "Новая вкладка"](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/) |
|Режим IE|Да|Да|Да|Нет|[Режим IE](/deployedge/edge-ie-mode#prerequisites)|
|Режим терминала|Да|Нет|Нет|Нет|[Режим терминала](/deployedge/microsoft-edge-configure-kiosk-mode)|
|Поиск (Майкрософт) в Bing|Да|Да|Да|Да|[Интеллектуальный поиск в Bing](https://www.microsoft.com/edge/business/intelligent-search-with-bing) |
|Средство чтения PDF|Да|Да|Да|Да|[Средство чтения PDF](/deployedge/microsoft-edge-pdf) |
|Покупки|Да|Да|Да|Да|[Покупки](https://techcommunity.microsoft.com/t5/articles/introducing-shopping-with-microsoft-edge/m-p/1870080) |
|Спящие вкладки|Да|Да|Да|Да|[Обзор функций](/deployedge/microsoft-edge-relnote-stable-channel)<br>[Последняя запись блога](https://blogs.windows.com/msedgedev/2021/03/04/edge-89-performance/)<br>[Групповые политики](/deployedge/microsoft-edge-policies#sleeping-tabs-settings)|
|Синхронизация|Да|Да|Да|Да| [Корпоративная синхронизация](/deployedge/microsoft-edge-enterprise-sync) |
|Откат версии|Да|Да|Да|Нет|[Откат версии](/deployedge/edge-learnmore-rollback) |
|Вертикальные вкладки|Да|Да|Да|Да| |

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)