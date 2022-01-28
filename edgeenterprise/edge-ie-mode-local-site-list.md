---
title: Локальный список сайтов для режима Internet Explorer (IE)
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/15/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Узнайте, как включить локальные списки сайтов и легкий доступ к режиму IE
ms.openlocfilehash: 8113b3baa613a0c19c80a738b3bbddfc330ec3ba
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2022
ms.locfileid: "12297975"
---
# <a name="configure-local-site-list-for-internet-explorer-ie-mode"></a>Настройка локального списка сайтов для режима Internet Explorer (IE)

>[!Note]
> 15 июня 2022 г. настольное приложение Internet Explorer 11 будет отправлено в отставку и не будет поддерживаться (список того, что имеется в области, см. в faq для настольных приложений [Internet Explorer 11).](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549) Те же приложения и сайты IE11, которые вы используете сегодня, можно открывать в Microsoft Edge в режиме Internet Explorer. Дополнительные дополнительные информации см. в Windows 10 Обозреватель интернета [в Microsoft Edge.](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)

В этой статье рассказывается, как настроить простой доступ к режиму Internet Explorer (режим IE) и разрешить использование локальных списков сайтов в организации.

> [!NOTE]
> Эта статья применима к Microsoft Edge версии 92 или более поздней версии.

## <a name="prerequisites"></a>Предварительные условия

1. Обновления Windows

   - Windows 10 версии 1909 — [KB5003698 или](https://support.microsoft.com/topic/june-15-2021-kb5003698-os-build-18363-1645-preview-1ecf117e-1f89-40f9-a0a5-ed5766737620) более поздней версии  

   - Windows 10 версии 2004; Windows 10 версии 20H2 и Windows 10 версии 21H1 — [KB5003690](https://support.microsoft.com/topic/june-21-2021-kb5003690-os-builds-19041-1081-19042-1081-and-19043-1081-preview-11a7581f-2a01-47d5-ba12-431709ee2248) или более поздней версии

2. Microsoft Edge версии 92 (92.0.902.55 или более поздней версии)

> [!IMPORTANT]
> В настоящее время эта функция локального списка сайтов Windows Server 2016 не поддерживается.

## <a name="overview"></a>Обзор

Режим IE питание от конфигурации списка Enterprise режима. При определении и настройке сайтов в списке сайтов для использования режима IE пользователям больше не нужно ждать или возвращаться к автономным приложениям IE11.

Начиная с Microsoft Edge версии 92, повторный доступ к *неконфигурованным* сайтам режима IE проще. Пользователи могут перезагрузить сайты в режиме IE. Они могут добавлять эти сайты в локальный список сайтов, чтобы автоматически отрисовки в режиме IE в течение 30 дней, в то время как список сайтов организации обновляется. При [отключении IE11](/deployedge/edge-ie-disable-ie11) в среде пользователи больше не зависят только от списка сайтов организации.

Этот опыт можно настроить с помощью групповых политик для организации.

> [!NOTE]
> *Неконфигурируемый* сайт — это сайт, который требует режима IE, но не настроен для открытия в режиме IE в списке Enterprise режима сайта.

## <a name="enable-the-local-site-list-experience"></a>Включить локальный список сайтов

Чтобы включить локальный список сайтов, пользователи ** могут перейти на URL-адрес edge://settings/defaultBrowser и установить разрешить перезагрузку сайтов в режиме **Internet Explorer,** чтобы **разрешить**.

:::image type="content" source="media/Edge-hybrid-IE-mode/internet-explorer-compatibilitiy.png" alt-text="Совместимость Internet Explorer":::

>[!Note]  
>
>1. Если вы включили тестирование режима IE с помощью политики *InternetExplorerIntegrationTestingAllowed,* вы увидите этот параметр, но он будет серым, если не будет явно включена политика *InternetExplorerIntegrationReloadInIEModeAllowed.*
>
>2. Если разрешить перезагрузку сайтов в режиме Internet Explorer по **умолчанию,** пользователи могут перезагрузить сайты в режиме IE, если у них есть существующее использование Internet **Explorer** 11.  

Когда этот параметр включен, пользователи могут перезагрузить сайт в режиме IE, выбрав Параметры и больше (значок эллипсов ...) > перезагрузки в режиме **Internet Explorer**. Пользователи также могут выбрать вкладку Перезагрузка в режиме **Internet Explorer,** когда они правой кнопкой мыши на вкладке или выбрать открытую ссылку в новой вкладке режим **Internet Explorer,** когда они правой кнопкой мыши по ссылке.

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-screenshot.png" alt-text="Перезагрузка в режиме internet Explorer":::

Значок режима Перезагрузка в **режиме Internet Explorer** можно прикрепить к панели инструментов. Кнопка панели инструментов позволяет пользователям легко входить и выходить из режима IE и может управляться edge://settings/appearance *URL-адресом.*

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-icon-screenshot.png" alt-text="Перезагрузка в значке режима internet Explorer":::

>[!Note]
>Если пользователь находится на сайте, который уже находится в списке сайтов Enterprise режима организации, параметры перезагрузки в режиме Internet Explorer (или Exit) будут видны, но отойдите в серый цвет.

При выборе параметра сайт перезагружается в режиме IE. Значок индикатора режима IE виден слева от панели адресов, а на вылете отображается параметр, который пользователи могут переметать, чтобы открыть страницу в режиме Internet Explorer в следующий раз. Это добавляет определенную страницу пользователя в локальный список сайтов и автоматически откроется в режиме IE в течение следующих 30 дней.

:::image type="content" source="media/Edge-hybrid-IE-mode/site-has-been-reloaded-in-ie-mode-screenshot.png" alt-text="Эта страница открыта в режиме internet Explorer":::

После перезагрузки сайта в режиме IE навигация "на странице" будет оставаться в режиме IE (например, ссылка, скрипт, форма на странице или перенаправление на стороне сервера из другой навигации на странице).  

В режиме IE пользователи увидят баннер, указывающий, что они находятся в режиме IE, возможность оставить режим IE и прикрепить значок режима IE к панели инструментов (если она еще не закреплена).

:::image type="content" source="media/Edge-hybrid-IE-mode/ie-mode-banner-screenshot.png" alt-text="Баннер режима IE":::

Пользователи могут выбрать выход из режима IE с помощью кнопки Leave на баннере, закрепленного значка режима IE или Параметры и более (значок эллипсов ...) > Режим Выхода internet **Explorer,** в противном случае Microsoft Edge автоматически выйдет из режима IE, когда происходит навигация, которая не является "на странице" (например, с помощью панели адресов, задней кнопки или любимой ссылки).

Записи остаются в локальном списке сайтов в течение 30 дней по умолчанию. Рекомендуется настроить устаревшие сайты для организации в списке Enterprise режима. Локальный список сайтов гарантирует, что пользователи смогут продолжать рабочий процесс, не прерываясь при обновлении списка сайтов организации. На 31-й день, когда пользователи переходят на сайт, они увидят баннер, объясняющий, что сайт больше не будет загружаться в режиме IE. Пользователи могут добавить его обратно в локальный список сайтов, если они этого хотят.

:::image type="content" source="media/Edge-hybrid-IE-mode/page-will-no-longer-load-in-ie-mode-screenshot.png" alt-text="Страница больше не будет загружаться в режиме IE":::

## <a name="policies-to-configure-the-use-of-local-site-lists-for-ie-mode"></a>Политики настройки использования локальных списков сайтов для режима IE

Для настройки локального списка сайтов в Microsoft Edge доступны две групповые политики. Вот эти политики:

### <a name="policy-internetexplorerintegrationreloadiniemodeallowed"></a>Политика: InternetExplorerIntegrationReloadInIEModeAllowed

Эта политика соответствует параметру Microsoft Edge "Разрешить перезагрузку сайтов в режиме Internet Explorer". Чтобы получить доступ к этому параметру, перейдите по URL-адресу *edge://settings/defaultbrowser*.

- Если включить эту политику, пользователи могут перезагрузить сайт в режиме IE, выбрав Параметры и больше (значок эллипсов ... > перезагрузки в режиме **Internet Explorer**. Пользователи также могут выбрать вкладку Перезагрузка в режиме **Internet Explorer,** когда они правой кнопкой мыши на вкладке, или выбрать открытую ссылку в новой вкладке режим **Internet Explorer,** когда они правой кнопкой мыши по ссылке.
Пользователи могут дополнительно Microsoft Edge использовать режим IE для сайта в будущем. Этот выбор запомнится по умолчанию в течение 30 дней и может управляться с помощью политики *InternetExplorerIntegrationLocalSiteListExpirationDays*.

- Если вы отключаете эту политику, пользователям не будет разрешено перезагрузить неконфигурованный сайт в режиме IE.

- Если эта политика не настроена, мы покажем пользователям варианты перезагрузки неконфигурируемых сайтов в режиме IE в зависимости от недавнего использования Internet Explorer 11.

Обратите внимание, что эта политика имеет приоритет над настройкой политики [InternetExplorerIntegrationTestingAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) и эта политика будет отключена.

### <a name="policy-internetexplorerintegrationlocalsitelistexpirationdays"></a>Политика: InternetExplorerIntegrationLocalSiteListExpirationDays

Эта политика может использоваться для настройки количества дней, которые сайт остается в локальном списке сайтов для пользователей.  

- Если вы отключать или не настраивать эту политику, используется значение по умолчанию в 30 дней.

- Если вы включаете политику, необходимо ввести значение от 0 до 90 дней, чтобы сохранить сайт в локальном списке веб-сайтов пользователя.

Эта политика не влияет на отключение политики *InternetExplorerIntegrationReloadInIEModeAllowed.*

> [!NOTE]
> В настоящее время локальный список сайтов не синхронизируется между устройствами. Это улучшение в настоящее время находится в нашем отставание, и мы обновим эту функцию, когда она будет доступна.

## <a name="see-also"></a>См. также

- Отключение Internet Explorer 11 — [отключение Internet Explorer 11](/deployedge/edge-ie-disable-ie11)
- Настройка политик режима IE — [Настройка политик режима IE](/deployedge/edge-ie-mode-policies)
