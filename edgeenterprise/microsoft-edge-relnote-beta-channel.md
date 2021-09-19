---
title: Заметки о выпуске Microsoft Edge для канала Beta
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 09/17/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для канала Beta
ms.openlocfilehash: 95f3f02401d00e59eed1df20688d0069db1e8b06
ms.sourcegitcommit: 93e141b725a08727b030332ea82f983d35c2a745
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/19/2021
ms.locfileid: "12019178"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Заметки о выпуске для Microsoft Edge из канала Beta

Эти заметки о выпуске содержат сведения о новых возможностях и обновлениях, не связанных с безопасностью, которые включены Microsoft Edge канала Beta Архивные версии этих заметок о выпуске доступны [здесь](microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> Веб-платформа Microsoft Edge постоянно развивается для улучшения взаимодействия с пользователями, безопасности и конфиденциальности. Дополнительные сведения см. в статье [Изменения в Microsoft Edge, затрагивающие совместимость сайтов](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-94099223-september-17"></a>Версия 94.0.992.23: 17 сентября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-94099219-september-13"></a>Версия 94.0.992.19: 13 сентября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-94099214-september-7"></a>Версия 94.0.992.14: 7 сентября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-9409929-september-2"></a>Версия 94.0.992.9: 2 сентября

### <a name="feature-updates"></a>Обновления компонентов

- **Microsoft Edge 4-недельную каденцию обновлений в бета-версии и стабильных каналах.**  Для основных версий будет принят новый четырехнедельный цикл выпуска. Подробнее о решении можно узнать здесь: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **Предлагается новый расширенный стабильный вариант.**  Мы предлагаем новый расширенный стабильный вариант для наших управляемых Enterprise клиентов. Параметр Extended Stable будет обновляться каждые 8 недель. Будет раз в две недели обновляться безопасность.  Дополнительные сведения здесь: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Улучшения поведения по умолчанию при открытии MHTML-файлов.**  Файлы MHTML будут продолжать открываться в режиме IE, если режим IE включен, если файл MHTML не был сохранен из Microsoft Edge (с помощью параметров Сохранить как или сохранить страницу Как в Microsoft Edge). Если файл был сохранен из Microsoft Edge, он будет открыт в Microsoft Edge.  Это изменение устраняет проблему отрисовки, которая наблюдалась при открытии MHTML-файла в режиме IE при Microsoft Edge.

- **Ограничить частные сетевые запросы безопасными контекстами.** Доступ к ресурсам локальных (интрасетей) сетей со страниц в Интернете требует, чтобы эти страницы доставлялись через HTTPS. Это изменение осуществляется в проекте Chromium, на котором основан Microsoft Edge. Дополнительные сведения см. в записи о [состоянии платформы Chrome](https://chromestatus.com/feature/5436853517811712). Для поддержки сценариев, необходимых для сохранения совместимости с незащищенными страницами, доступны две политики совместимости: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) и [InsecurePrivateNetworkRequestAllowedForUrls.](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls)

- **Блокируют смешанные загрузки контента.** Безопасные страницы будут загружать файлы, которые будут скачать только на других защищенных страницах, а загрузки, которые будут загружаться на небезопасных (не-HTTPS) страницах, будут заблокированы, если они инициируют с безопасной страницы. Это изменение осуществляется в проекте Chromium, на котором основан Microsoft Edge. Дополнительные сведения можно найти в записи [блога безопасности Google.](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html)

- **Включить неявный вход для учетных записей на локальной основе.**   Включив политику OnlyOnPremisesImplicitSigninEnabled, для неявного входа будут включены только учетные записи на месте.  Браузер Microsoft Edge не будет пытаться выполнять неявный вход в учетные записи MSA и AAD. Переход с локальных учетных записей на учетные записи AAD также будет остановлен.

- **Бесплатные текстовые поля формы, добавленные в документы PDF.**  Теперь мы поддерживаем добавление текстовых полей свободной формы в документы PDF, которые можно использовать для заполнения форм и добавления видимых заметок.

- **Обновление паролей с легкостью.**  Браузер теперь будет принимать вас непосредственно на страницу Изменить пароль для данного веб-сайта, экономя время и клики, избегая необходимости переходить на страницу вручную. После того, как вы на этой странице браузер также автозаполнеет существующий пароль и предложит надежный, уникальный новый пароль.  Обратите внимание: в настоящее время эта функция доступна на ограниченном количестве сайтов.  

- **Страница Новые параметры доступности.** Мы собрали параметры, связанные с доступностью, на одной странице. Вы можете найти новую страницу edge://settings/accessibility в списке основных параметров. Здесь вы можете найти параметры, чтобы сделать веб-страницу больше, показать контур высокой видимости вокруг области фокуса и другие параметры, которые могут помочь улучшить ваш опыт просмотра веб-страниц. Мы продолжим добавлять новые параметры здесь в будущих версиях Microsoft Edge.

***Новые политики***

- [ApplicationGuardPassiveModeEnabled](/DeployEdge/microsoft-edge-policies#applicationguardpassivemodeenabled) Игнорировать конфигурацию списка сайтов Application Guard и просматривать edge обычно
- [OnlyOnPremisesImplicitSigninEnabled](/DeployEdge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) Только учетная запись локальной учетной записи включена для неявного входа
- [WebRtcRespectOsRoutingTableEnabled](/DeployEdge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) Включить поддержку Windows правил маршрутивки ОС при создании одноранговых подключений через WebRTC

***Устаревшая политика***

- [UserAgentClientHintsEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) Включить функцию User-Agent клиентские подсказки

## <a name="version-93096133-august-27"></a>Версия 93.0.961.33: 27 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-93096127-august-20"></a>Версия 93.0.961.27: 20 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-93096124-august-18"></a>Версия 93.0.961.24: 18 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-93096111-august-3"></a>Версия 93.0.961.11: 3 августа

### <a name="feature-updates"></a>Обновления компонентов

- **Начальные предпочтения в Microsoft Edge.**  Начиная с Microsoft Edge версии 93, развертывание Microsoft Edge на предприятии станет проще с добавлением [начальных предпочтений.](/deployedge/initial-preferences-support-on-microsoft-edge-browser)

- **Режим IE в Microsoft Edge поддерживает поведение "без слияния".**  Начиная с Microsoft Edge версии 93, режим IE на Microsoft Edge будет поддерживать "без слияния". Для конечных пользователей при запуске нового окна браузера из приложения режима IE оно будет в отдельном сеансе, аналогичном поведению в IE11. Вам потребуется настроить список сайтов, чтобы настроить сайты, необходимые для предотвращения совместного доступа к сеансам. Для каждого окна Microsoft Edge при первом посещении вкладки режима IE в этом окне, если это один из назначенных сайтов "без слияния", это окно блокируется в другом сеансе IE "без слияния" от всех остальных окон Microsoft Edge по крайней мере до закрытия последней вкладки режима IE в этом окне. [Здесь](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--no-merge--option-that-was-supported-in-internet-explorer-11-) вы найдете дополнительные сведения.

- **Группы вкладок.**  Возможность классификации вкладок в группы, определяемую пользователем, позволяет эффективнее находить, переключать и управлять вкладками в нескольких workstreams. Для этого мы включаем группировку вкладок, начиная с Microsoft Edge версии 93.

- **Скрытие заголовка окна при использовании вертикальных вкладок.**  Получите дополнительные несколько пикселей обратно, скрыв заголовок окна браузера при использовании вертикальных вкладок. Начиная с Microsoft Edge версии 93, вы можете перейти к edge://settings/appearance и в разделе Настройка панели инструментов выберите параметр, чтобы скрыть панель заголовка в режиме Вертикальная вкладка.

- **Видео "картинка в картинке" (PiP) в панели инструментов, вызываемой при наведении курсора.**  Начиная с Microsoft Edge версии 93, будет еще проще вводить изображение в режиме Picture (PiP). При наведении курсора на поддерживаемое видео появляется панель инструментов, которая позволяет просматривать это видео в окне PiP.  Примечание. В настоящее время это доступно для Microsoft Edge на macOS.  Проверьте в ближайшее время, как мы продолжаем нашу выкатку для Windows пользователей.

- **Удаление 3DES в TLS.**  Начиная с Microsoft Edge версии 93 поддержка TLS_RSA_WITH_3DES_EDE_CBC_SHA шифра будет удалена. Это изменение осуществляется в проекте Chromium, на котором основан Microsoft Edge. Дополнительные сведения см. в записи о [состоянии платформы Chrome](https://chromestatus.com/feature/6678134168485888). Кроме того, в Microsoft Edge версии 93 будет доступна политика [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) для поддержки сценариев, которым необходимо сохранение совместимости с устаревшими серверами. Эта политика совместимости устареет и перестанет работать в Microsoft Edge версии 95. Обновите затронутые серверы заранее.

- **Политики для обхода запросов ClickOnce и DirectInvoke.**  Мы обновили наши политики, чтобы включить обход запросов ClickOnce и приложения DirectInvoke для указанных типов файлов из указанных доменов. Для этого необходимо:

  - Включить [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) или [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Включить политику [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) и настроить список определенных типов файлов, для которых следует отключить ClickOnce и DirectInvoke.
  - Включим политику [AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls) и установите список определенных доменов, которые ClickOnce и DirectInvoke будут отключены для

  Примечание. AutoOpenAllowedForURLs — это вспомогательная политика для AutoOpenFileTypes. Если политика AutoOpenAllowedForURLs не настроена, но настроена политика AutoOpenFileTypes, указанные типы файлов будут автоматически открываться из всех URL-адресов.

### <a name="new-policies"></a>Новые политики

- [AutoplayAllowlist](/DeployEdge/microsoft-edge-policies#autoplayallowlist) Разрешить автоматическое воспроизведение мультимедиа на определенных сайтах
- [CECPQ2Enabled](/DeployEdge/microsoft-edge-policies#cecpq2enabled) Согласование постквантовых ключей CeCPQ2 включено для TLS
- [ConfigureViewInFileExplorer](/DeployEdge/microsoft-edge-policies#configureviewinfileexplorer) Настройка функции "Просмотреть в проводнике" для страниц SharePoint в Microsoft Edge
- [DefaultJavaScriptJitSetting](/DeployEdge/microsoft-edge-policies#defaultjavascriptjitsetting) Управление использованием JIT JavaScript
- [ShowPDFDefaultRecommendationsEnabled](/DeployEdge/microsoft-edge-policies#showpdfdefaultrecommendationsenabled) Разрешить уведомлениям устанавливать Microsoft Edge в качестве программы чтения PDF-файлов по умолчанию
- [FeatureFlagOverridesControl](/DeployEdge/microsoft-edge-policies#featureflagoverridescontrol) Настройка возможности пользователей переопределять флаги функций
- [ImplicitSignInEnabled](/DeployEdge/microsoft-edge-policies#implicitsigninenabled) Включить неявный вход
- [InternetExplorerIntegrationCloudSiteList](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) Настройка списка облачных сайтов в режиме предприятия
- [InternetExplorerIntegrationSiteListRefreshInterval](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsitelistrefreshinterval) Настройка частоты обновления списка сайтов в режиме предприятия
- [JavaScriptJitAllowedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitallowedforsites) Разрешить JavaScript использовать JIT на этих сайтах
- [JavaScriptJitBlockedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitblockedforsites) Запретить JavaScript использовать JIT на этих сайтах
- [LocalBrowserDataShareEnabled](/DeployEdge/microsoft-edge-policies#localbrowserdatashareenabled) Включить Windows для поиска в локальных данных просмотра веб-страниц через Microsoft Edge
- [MAUEnabled](/DeployEdge/microsoft-edge-policies#mauenabled) Всегда использовать службу автоматического обновления Майкрософт в качестве средства обновления для Microsoft Edge
- [MSAWebSiteSSOUsingThisProfileAllowed](/DeployEdge/microsoft-edge-policies#msawebsitessousingthisprofileallowed) Разрешить единый вход для сайтов Майкрософт с использованием этого профиля
- [OneAuthAuthenticationEnforced](/DeployEdge/microsoft-edge-policies#oneauthauthenticationenforced) Проверка подлинности OneAuth Flow для signin
- [PasswordGeneratorEnabled](/DeployEdge/microsoft-edge-policies#passwordgeneratorenabled) Разрешить пользователям получать подсказку надежного пароля при каждом создании учетной записи в Интернете
- [PrimaryPasswordSetting](/DeployEdge/microsoft-edge-policies#primarypasswordsetting) Настраивает параметр, предлагающий пользователям ввести пароль устройства при использовании автозаполнения паролей
- [PrintingWebpageLayout](/DeployEdge/microsoft-edge-policies#printingwebpagelayout) Задает макет для печати
- [RemoteDebuggingAllowed](/DeployEdge/microsoft-edge-policies#remotedebuggingallowed) Разрешить удаленную отладку
- [RelaunchWindow](/DeployEdge/microsoft-edge-policies#relaunchwindow) Установка интервала времени для повторного запуска
- [TravelAssistanceEnabled](/DeployEdge/microsoft-edge-policies#travelassistanceenabled) Включить помощь в поездках
- [TripleDESEnabled](/DeployEdge/microsoft-edge-policies#tripledesenabled) Включить шифры 3DES в TLS

#### <a name="deprecated-policy"></a>Устаревшая политика

- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Поддержка стандартного устаревшего параметра поведения SameSite для cookie-файлов.

#### <a name="obsoleted-policy"></a>Устаревшая политика

- [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) Настройка взаимодействия с новой вкладкой Microsoft Edge

#### <a name="additional-change"></a>Дополнительные изменения

- [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) Добавление поддержки платформы Mac

## <a name="version-93096118-august-10"></a>Версия 93.0.961.18: 10 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-92090262-july-29"></a>Версия 92.0.902.62: 29 июля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-92090255-july-21"></a>Версия 92.0.902.55: 21 июля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-92090245-july-12"></a>Версия 92.0.902.45: 12 июля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-92090240-july-6"></a>Версия 92.0.902.40: 6 июля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-92090222-june-21"></a>Версия 92.0.902.22: 21 июня

### <a name="feature-updates"></a>Обновления компонентов

- **Поиск естественного языка для истории браузера в панели адресов.** Поиск статьи или веб-сайта, который вы ищете, теперь проще благодаря поиску естественного языка прямо из панели адресов. Результаты поиска можно найти на основе содержимого страницы/описания/времени (например, "рецепт торта с прошлой недели"), а также только для названий и ключевых слов URL-адресов.
Обратите внимание: это контролируемый выпуск компонентов. Если вы не видите эту возможность, вернитесь сюда позже, так как выпуск продолжается.

- **Пользователи могут легко перейти в режим Internet Explorer в Microsoft Edge**. Начиная с Microsoft Edge версии 92, пользователи могут перезагрузить сайт в режиме Internet Explorer в Microsoft Edge, а не в отдельном приложении IE 11 в ожидании настройки сайта в списке сайтов в режиме предприятия. Пользователям будет предложено добавить сайт в список локальных сайтов, чтобы переход на ту же страницу в Microsoft Edge автоматически происходил в режиме IE в течение следующих 30 дней. Вы можете использовать политику *[InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)*, чтобы настроить это взаимодействие и разрешить доступ к точкам входа в режиме IE, а также настроить возможность добавления сайтов в список локальных сайтов. Вы можете использовать политику *[InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)*, чтобы настроить количество дней хранения сайтов в списке локальных сайтов.
Обратите внимание, что комплексной работы для Windows 10 версии 1909 требуется KB5003698 или более поздняя версия, для Windows 10 версии 2004, Windows 10 версии 20H2 или Windows 10 версии 21H1 требуется KB5003690 или более поздняя версия.

- **MHTML-файлы по умолчанию открываются в режиме Internet Explorer**. Начиная с Microsoft Edge версии 92 Stable, MHTML-файлы автоматически открываются в режиме Internet Explorer в Microsoft Edge, а не в приложении Internet Explorer (IE11). Это чаще всего наблюдается при попытке просмотра электронной почты Outlook в браузере. Это изменение будет происходить только в том случае, если IE11 является обработчиком по умолчанию для этого типа файлов. Если вы хотите изменить это, это можно сделать перед установкой обновления Stable версии 92 с помощью [этого руководства](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

- **Платежные инструменты теперь синхронизируются между устройствами**. Начиная с Microsoft Edge версии 92, вы можете синхронизировать платежную информацию между устройствами, на которых вы выполнили вход.
Обратите внимание: это контролируемый выпуск компонентов. Если вы не видите эту функцию, проверьте в ближайшее время, как мы продолжим нашу выкатку.

- **Предупреждение "Отключить расширения режима разработчика" можно закрыть окончательно**. Начиная с Microsoft Edge версии 92, вы можете отключить предупреждение "Отключить расширения режима разработчика", нажав параметр "Не показывать это снова".
Обратите внимание: это контролируемый выпуск компонентов. Если вы не видите эту функцию, проверьте в ближайшее время, как мы продолжим нашу выкатку.

- **Управляйте расширениями непосредственно с панели инструментов**. Совершенно новое меню расширений на панели инструментов позволит легко скрыть расширения или закрепить их. Быстрые ссылки на управление расширениями и поиск новых расширений упростят поиск новых расширений и управление существующими.
Обратите внимание: это контролируемый выпуск компонентов. Если вы не видите эту функцию, проверьте в ближайшее время, как мы продолжим нашу выкатку.

- **Автоматическое использование HTTPS**. Пользователи смогут обновить навигацию с HTTP до HTTPS для доменов, которые, скорее всего, поддерживают этот более безопасный протокол. Эту поддержку также можно настроить так, чтобы попытка доставки по протоколу HTTPS осуществлялась для всех доменов.
Обратите внимание: мы экспериментируем с этой функцией, и это поведение не будет проявляться, если вы решили отказаться от экспериментов.

- **Улучшения визуализации шрифтов.** Улучшена четкость и снижена размытость при передаче текста.
Обратите внимание: это контролируемый выпуск компонентов. Если вы не видите эту функцию, проверьте в ближайшее время, как мы продолжим нашу выкатку.

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено восемь новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Добавлены следующие новые политики:

- [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) Единый вход для рабочих и учебных сайтов с помощью этого профиля включен
- [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) Настройка автоматического использования HTTPS
- [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) Управление использованием режима без монитора
- [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed)Указывает, следует ли разрешить небезопасным веб-сайтам делать запросы к более закрытым конечным точкам сети
- [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) Разрешает перечисленным веб-сайтам делать запросы к более частным конечным точкам сети из небезопасных контекстов
- [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) Указать количество дней, в течение которых сайт остается в локальном списке сайтов режима IE
- [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) Разрешить перезагрузку ненастроенных сайтов в режиме Internet Explorer
- [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) Указывает, разрешено ли использовать SharedArrayBuffers в контексте без изоляции ссылок перекрестного происхождения

#### <a name="obsoleted-policy"></a>Устаревшая политика

- [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) Разрешение сертификатов, подписанных с помощью SHA-1 при выдаче локальными якорями доверия.

## <a name="version-9209029-june-8"></a>Версия 92.0.902.9: 8 июня

Исправлены ошибки и проблемы с производительностью.

## <a name="version-91086441-june-3"></a>Версия 91.0.864.41: 3 июня

Исправлены ошибки и проблемы с производительностью.

## <a name="version-91086437-may-27"></a>Версия 91.0.864.37: 27 мая

Исправлены ошибки и проблемы с производительностью.

## <a name="version-91086436-may-26"></a>Версия 91.0.864.36: 26 мая

Исправлены ошибки и проблемы с производительностью.

## <a name="version-91086433-may-21"></a>Версия 91.0.864.33: 21 мая

Исправлены ошибки и проблемы с производительностью.

## <a name="version-91086427-may-14"></a>Версия 91.0.864.27: 14 мая

Исправлены ошибки и проблемы с производительностью.

## <a name="version-91086419-may-7"></a>Версия 91.0.864.19: 7 мая

Исправлены ошибки и проблемы с производительностью.

## <a name="version-91086415-may-3"></a>Версия 91.0.864.15: 3 мая

Исправлены ошибки и проблемы с производительностью.

## <a name="version-91086411-april-30"></a>Версия 91.0.864.11: 30 апреля

### <a name="feature-updates"></a>Обновления компонентов

- **Определение сетевого трафика, исходя из контейнеров Application Guard в Microsoft Defender на уровне прокси-сервера**. Начиная с Microsoft Edge версии 91, для добавления тегов сетевого трафика, исходящего из контейнеров Application Guard, встраивается поддержка, что позволяет предприятиям идентифицировать их и применять определенные политики.

- **Параметр поддержки, позволяющий синхронизировать избранное из хоста в контейнер Edge Application Guard.** Начиная с Microsoft Edge версии 91, пользователи могут настроить Application Guard для синхронизации избранного из хоста в контейнер. Это гарантирует появление нового избранного в контейнере.

- **Поддержка API распознавания речи.** Начиная с Microsoft Edge версии 91, добавляется поддержка API команд распознавания речи на Google.com и аналогичных сайтах. Эта возможность доступна только случайно выбранной группе пользователей, участвующих в эксперименте. Эти пользователи предоставляют отзывы службе поддержки.

- **Персонализация браузера с помощью новых цветовых тем.** Персонализируйте Microsoft Edge с помощью одной из четырнадцати новых цветовых тем на странице "Параметры - > Внешний вид". Вы также можете установить настраиваемые темы с сайта надстроек Microsoft Edge. [Подробнее](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

- **Прерывание загрузки** Начиная с Microsoft Edge версии 91 браузер автоматически прерывает загрузки типов, которые могут нанести вред вашему компьютеру, если они начинаются без взаимодействия с пользователем и не поддерживаются проверкой репутации приложений SmartScreen. Пользователи могут переопределять и продолжать загрузку, щелкнув правой кнопкой мыши и выбрав параметр "Keep" ("Сохранить") на элементе загрузки.
Администраторы предприятия могут отказаться от этого с помощью одной из этих двух политик:
    - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) – Отключение предупреждений о расширениях загружаемых файлов для определенных типов файлов в доменах. Дополнительные сведения см. в статье [Перебои загрузок в Microsoft Edge Security](/deployedge/microsoft-edge-security-downloads-interruptions)

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено шесть новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Добавлены следующие новые политики:

- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) — идентификация трафика Application Guard
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) — явно разрешенные сетевые порты
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) — разрешение импорта параметров страниц запуска
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) — позволяет пользователям вставлять фрагменты математических задач и получать решение с пошаговым объяснением в Microsoft Edge
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) — разрешает содержимое Microsoft News на новой странице вкладки
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) — разрешает быстрые ссылки на новой странице вкладки

#### <a name="obsoleted-policy"></a>Устаревшая политика

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) — включает упреждающую проверку подлинности
<!-- end major 91 -->

## <a name="version-90081846-april-22"></a>Версия 90.0.818.46: 22 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-90081842-april-20"></a>Версия 90.0.818.42: 20 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-90081841-april-16"></a>Версия 90.0.818.41: 16 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-90081838-april-14"></a>Версия 90.0.818.38: 14 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-90081836-april-12"></a>Версия 90.0.818.36: 12 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-90081827-april-2"></a>Версия 90.0.818.27: 2 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-90081822-march-29"></a>Версия 90.0.818.22: 29 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-90081814-march-22"></a>Версия 90.0.818.14: 22 марта

Исправлены ошибки и проблемы с производительностью.
<!-- begin major 90 -->
## <a name="version-9008188-march-16"></a>Версия 90.0.818.8: 16 марта

### <a name="feature-updates"></a>Обновления компонентов

- Единый вход (SSO) теперь доступен для учетных записей **Azure Active Directory (Azure AD) и Microsoft Account (MSA) на macOS.** Пользователь, вошедший в систему в Microsoft Edge на macOS, автоматически получает вход на веб-сайты, настроенные на единый вход с помощью рабочей учетной записи и учетной записи Майкрософт (например, bing.com, office.com, msn.com и outlook.com).

- **Режим терминала** Начиная с Microsoft Edge версии 90, мы заблокировали параметры печати пользовательского интерфейса, чтобы разрешить только настроенные принтеры и параметры "Печать в PDF". Кроме того, мы усовершенствовали режим терминала с одним приложением, чтобы ограничить запуск других приложений из браузера. Дополнительные сведения о функциях режима терминала см. [здесь.](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features)

- **Вывод на печать:**

  - **Новый режим растеризации печати**для принтеров без PostScript. Начиная с Microsoft Edge версии 90, администраторы могут использовать новую политику для определения режима растеризации печати для своих пользователей. Эта политика управляет печатью из Microsoft Edge на принтерах в Windows без PostScript.  Иногда для правильной печати на принтерах без поддержки PostScript необходимо правильно растеризовать задания для печати. Возможные настройки - Полная и Быстрая.

  - **Дополнительные параметры масштабирования страниц для печати.** Теперь пользователи могут настраивать масштабирование при печати веб-страниц и документов PDF с помощью дополнительных параметров. Параметр "Вписать на страницу" гарантирует, что веб-страница или документ вписываются в пространство, доступное в выбранном для печати "Размере бумаги". Значение "Фактический размер" гарантирует, что размер печатаемого контента не изменится независимо от выбранного "Размера бумаги".

- **Эффективная работа:**

  - **Предложения по автозаполнению стали более разнообразными**- теперь они включают в себя содержимое адресных полей из буфера обмена. При нажатии на поле профиля или адреса (такое как телефон, электронная почта, почтовый индекс, город, область и т.д.) происходит разбор содержимого буфера обмена и результаты выводятся в качестве предложений автозаполнения.

  - **Пользователи могут искать предложения автозаполнения, даже если форма или поле не обнаружены**. Теперь, если у вас есть сведения, сохраненные в Microsoft Edge, предложения по автозаполнению всплывают автоматически, помогая сэкономить время при заполнении форм. Если автозаполнение не работает для формы или если вы хотите получить данные в формах, обычно не имеющих автозаполнения (например, временные формы), вы можете искать информацию с помощью автозаполнения.

- **Доступ к загрузкам из раскрывающегося меню в панели меню**. Загрузки будут показаны в правом верхнем углу, причем все загрузки, активные в данный момент, будут располагаться рядом. Это меню легко закрыть, чтобы продолжать просматривать веб-страницу и при этом отслеживать общий ход скачивания прямо на панели инструментов. [Подробнее](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).


### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено семь новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Добавлены следующие новые политики:

- [ApplicationGuardFavoritesSyncEnabled](./microsoft-edge-policies.md#applicationguardfavoritessyncenabled) — включена синхронизация избранного Application Guard
- [ManagedConfigurationPerOrigin](./microsoft-edge-policies.md#managedconfigurationperorigin) — задает управляемые значения конфигурации для веб-сайтов в определенных источниках
- [PrintRasterizationMode](./microsoft-edge-policies.md#printrasterizationmode) — режим растеризации печати
- [QuickViewOfficeFilesEnabled](./microsoft-edge-policies.md#quickviewofficefilesenabled) — управление возможностями быстрого просмотра файлов Office в Microsoft Edge
- [SSLErrorOverrideAllowedForOrigins](./microsoft-edge-policies.md#sslerroroverrideallowedfororigins) — разрешить пользователям переходить дальше со страницы предупреждения HTTPS для определенных источников
- [WindowOcclusionEnabled](./microsoft-edge-policies.md#windowocclusionenabled) — включить загораживание окна
- [WindowsHelloForHTTPAuthEnabled](./microsoft-edge-policies.md#windowshelloforhttpauthenabled) — включена Windows Hello для HTTP Auth

#### <a name="deprecated-policies"></a>Устаревшие политики

- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) — включить встроенное загораживание окна
- [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin)— включена минимальная версия TLS
<!-- end major 90 -->

## <a name="version-89077454-march-13"></a>Версия 89.0.774.54: 13 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-89077450-march-10"></a>Версия 89.0.774.50: 10 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-89077448-march-8"></a>Версия 89.0.774.48: 8 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-89077445-march-3"></a>Версия 89.0.774.45: 3 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-89077439-february-26"></a>Версия 89.0.774.39: 26 февраля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-89077434-february-22"></a>Версия 89.0.774.34: 22 февраля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-89077427-february-12"></a>Версия 89.0.774.27: 12 февраля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-89077423-february-8"></a>Версия 89.0.774.23: 8 февраля

Исправлены ошибки и проблемы с производительностью.

<!-- begin major 89 -->

<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
