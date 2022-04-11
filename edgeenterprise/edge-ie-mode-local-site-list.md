---
title: Список локальных сайтов для режима Internet Explorer (IE)
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/24/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Узнайте, как включить локальные списки сайтов и упростить доступ к режиму IE
ms.openlocfilehash: 85aa6baa1abaa1a59f4e9cf9f2414f54ccf70cbb
ms.sourcegitcommit: dd8cdbd35726c795ddce917e549ddf17ee7f5290
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/11/2022
ms.locfileid: "12473636"
---
# <a name="configure-local-site-list-for-internet-explorer-ie-mode"></a>Настройка локального списка сайтов для режима Internet Explorer (IE)

>[!Note]
> Поддержка классических приложений Internet Explorer 11 будет прекращена и прекращена 15 июня 2022 г. (список областей применения см. в статье "Часто задаваемые вопросы о прекращении поддержки для классических приложений [Internet Explorer 11"](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Те же приложения и сайты IE11, которые вы используете сегодня, можно открывать в Microsoft Edge в режиме Internet Explorer. Дополнительные сведения см. [в статье о будущем Internet Explorer Windows 10 в Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

В этой статье объясняется, как настроить простой доступ к режиму Internet Explorer (режим IE) и разрешить использование локальных списков сайтов в организации.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 92 или более поздней.

## <a name="prerequisites"></a>Предварительные условия

1. Обновления Windows

   - Windows 11

   - Windows 10 версии 1909 — [KB5003974](https://support.microsoft.com/topic/kb5003974-servicing-stack-update-for-windows-10-version-1909-june-15-2021-0e65680e-2d21-4a31-b97a-e24c022aeccf) и [KB5003698](https://support.microsoft.com/topic/june-15-2021-kb5003698-os-build-18363-1645-preview-1ecf117e-1f89-40f9-a0a5-ed5766737620) или более поздней

   - Windows 10 версии 2004; Windows 10 версии 20H2 и Windows 10 версии 21H — [KB5005260](https://support.microsoft.com/topic/kb5005260-servicing-stack-update-for-windows-10-version-2004-20h2-and-21h1-august-10-2021-ec4c5daa-2cec-4b06-be93-037f150fe3ba) и [KB5005101](https://support.microsoft.com/topic/september-1-2021-kb5005101-os-builds-19041-1202-19042-1202-and-19043-1202-preview-82a50f27-a56f-4212-96ce-1554e8058dc1) или более поздней

2. Microsoft Edge версии 92 (92.0.902.55 или более поздней)

> [!IMPORTANT]
> В настоящее время эта функция локального списка сайтов Windows Server 2016 не поддерживается.

## <a name="overview"></a>Обзор

Режим IE определяется конфигурацией списка сайтов Enterprise режима. Пока вы определяете и настраиваете сайты в списке сайтов для использования режима IE, пользователям больше не нужно ждать или вернуться к автономному приложению IE11.

Начиная с Microsoft Edge версии 92, повторный доступ к ненастройным сайтам *режима IE* проще. Пользователи могут перезагружать сайты в режиме IE. Они могут добавлять эти сайты в свой локальный список сайтов, чтобы автоматически отображать их в режиме IE в течение 30 дней, пока список сайтов организации обновляется. Если [IE11 отключен](/deployedge/edge-ie-disable-ie11) в вашей среде, пользователи больше не зависят только от списка сайтов организации.

Этот интерфейс можно настроить с помощью групповых политик для организации.

> [!NOTE]
> *Ненастройный* сайт — это сайт, для которого требуется режим IE, но он не настроен для открытия в режиме IE в Enterprise режиме сайта.

## <a name="enable-the-local-site-list-experience"></a>Включение интерфейса локального списка сайтов

Чтобы включить работу со списком локальных сайтов, пользователи могут перейти *по URL-адресу* edge://settings/defaultBrowser и задать разрешение перезагрузки сайтов в режиме **Internet Explorer** как **"Разрешить"**.

:::image type="content" source="media/Edge-hybrid-IE-mode/internet-explorer-compatibilitiy.png" alt-text="Совместимость Internet Explorer":::

>[!Note]  
>
>1. Если вы включили тестирование режима IE с помощью политики *InternetExplorerIntegrationTestingAllowed* , вы увидите этот параметр, но он будет неактивен, если вы явно не включите политику *InternetExplorerIntegrationReloadInIEModeAllowed* .
>
>2. Если для параметра "Разрешить перезагрузку сайтов в режиме **Internet Explorer** " задано значение **"** По умолчанию", пользователи могут перезагрузить сайты в режиме IE, если у них уже есть internet Explorer 11.  

Если этот параметр включен, пользователи могут перезагрузить сайт в режиме IE, нажав кнопку Параметры (значок многоточия...) > перезагрузку в режиме **Internet Explorer**. Пользователи также могут выбрать вкладку "Перезагрузка" в режиме **Internet Explorer** , щелкнув правой кнопкой мыши вкладку или выбрав команду "Открыть ссылку" на новой вкладке режима **Internet Explorer** , щелкнув ссылку правой кнопкой мыши.

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-screenshot.png" alt-text="Перезагрузка в режиме Internet Explorer":::

**Значок перезагрузки в режиме Internet Explorer** можно закрепить на панели инструментов. Кнопка панели инструментов позволяет пользователям легко перейти в режим IE и выйти из него, а управлять ими можно с *помощью EDGE://SETTINGS/APPEARANCE URL-адреса* .

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-icon-screenshot.png" alt-text="Значок перезагрузки в режиме Internet Explorer":::

>[!Note]
>Если пользователь находится на сайте, который уже находится в списке сайтов Enterprise в режиме Enterprise организации, параметры перезагрузки в режиме Internet Explorer (или выхода) будут видны, но неактивен.

Если этот параметр выбран, сайт перезагружается в режиме IE. Значок индикатора режима IE отображается слева от адресной строки, а во всплывающем окне отображается параметр, который пользователи могут переключать, чтобы открыть страницу в режиме Internet Explorer в следующий раз. В результате пользователь добавит определенную страницу в список локальных сайтов и автоматически откроется в режиме IE в течение следующих 30 дней.

:::image type="content" source="media/Edge-hybrid-IE-mode/site-has-been-reloaded-in-ie-mode-screenshot.png" alt-text="Эта страница открыта в режиме Internet Explorer":::

После перезагрузки сайта в режиме IE навигация "на странице" останется в режиме IE (например, ссылка, скрипт, форма на странице или перенаправление на стороне сервера из другой навигации на странице).  

В режиме IE пользователи будут видеть баннер, указывающий, что они находятся в режиме IE, возможность выйти из режима IE и закрепить значок режима IE на панели инструментов (если он еще не закреплен).

:::image type="content" source="media/Edge-hybrid-IE-mode/ie-mode-banner-screenshot.png" alt-text="Баннер режима IE":::

Пользователи могут выйти из режима IE с помощью кнопки "Выйти" на баннере, закрепленного значка режима IE или Параметры и т. д. (значок многоточия **...) > Выйти из режима Internet Explorer**. В противном случае Microsoft Edge автоматически выйдет из режима IE при переходе, который не является "на странице" (например, с помощью адресной строки, кнопки "Назад" или избранной ссылки).

Записи остаются в локальном списке сайтов в течение 30 дней по умолчанию. Рекомендуется настроить устаревшие сайты для организации в списке Enterprise режиме. Локальный список сайтов гарантирует, что пользователи смогут продолжить рабочий процесс без прерывания при обновлении списка сайтов организации. На 31-й день при переходе на сайт пользователи видят баннер с сообщением о том, что сайт больше не будет загружаться в режиме IE. Пользователи могут добавить его обратно в локальный список сайтов при необходимости.

:::image type="content" source="media/Edge-hybrid-IE-mode/page-will-no-longer-load-in-ie-mode-screenshot.png" alt-text="Страница больше не будет загружаться в режиме IE":::

## <a name="policies-to-configure-the-use-of-local-site-lists-for-ie-mode"></a>Политики для настройки использования локальных списков сайтов для режима IE

Для настройки локального интерфейса списка сайтов в Microsoft Edge доступны две групповые политики. Вот эти политики:

### <a name="policy-internetexplorerintegrationreloadiniemodeallowed"></a>Политика: InternetExplorerIntegrationReloadInIEModeAllowed

Эта политика соответствует параметру Microsoft Edge "Разрешить перезагрузку сайтов в режиме Internet Explorer". Чтобы получить доступ к этому параметру, перейдите по URL-адресу *edge://settings/defaultbrowser*.

- Если эта политика включена, пользователи могут перезагрузить сайт в режиме IE, щелкнув Параметры и т. д. (значок многоточия... > перезагрузить в режиме **Internet Explorer**. Пользователи также могут выбрать вкладку "Перезагрузка" в режиме **Internet Explorer** , щелкнув ее правой кнопкой мыши, или открыть ссылку на новой вкладке режима **Internet Explorer** , щелкнув ссылку правой кнопкой мыши.
При необходимости пользователи могут Microsoft Edge использовать режим IE для сайта в будущем. Этот выбор будет запоминаться в течение 30 дней по умолчанию и может управляться с помощью политики *InternetExplorerIntegrationLocalSiteListExpirationDays*.

- Если отключить эту политику, пользователям не будет разрешено перезагружать ненастройный сайт в режиме IE.

- Если вы не настроите эту политику, мы отобразим параметры перезагрузки ненастрояемых сайтов в режиме IE в зависимости от последнего использования Internet Explorer 11.

Обратите внимание, что эта политика имеет приоритет над настройкой политики [InternetExplorerIntegrationTestingAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) , и эта политика будет отключена.

### <a name="policy-internetexplorerintegrationlocalsitelistexpirationdays"></a>Политика: InternetExplorerIntegrationLocalSiteListExpirationDays

Эту политику можно использовать для настройки количества дней, в течение которых сайт остается в локальном списке сайтов для пользователей.  

- Если эта политика отключена или не настроена, используется значение по умолчанию 30 дней.

- Если вы включите политику, необходимо ввести значение от 0 до 90 дней, чтобы сохранить сайт в локальном списке сайтов пользователя.

Эта политика не действует, если вы отключите политику *InternetExplorerIntegrationReloadInIEModeAllowed* .

> [!NOTE]
> Список локальных сайтов в настоящее время не синхронизируется между устройствами. В настоящее время это улучшение находится в невыполненной работе, и мы обновим эту функцию, когда она будет доступна.

## <a name="see-also"></a>См. также

- Отключение Internet Explorer 11 — [отключение Internet Explorer 11](/deployedge/edge-ie-disable-ie11)
- Настройка политик режима IE . Настройка политик [режима IE](/deployedge/edge-ie-mode-policies)
