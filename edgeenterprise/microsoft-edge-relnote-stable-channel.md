---
title: Заметки о выпуске Microsoft Edge для стабильного канала
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 11/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для стабильного канала
ms.openlocfilehash: 5c8a893254d9c9be0ccf22c76a3f873f31a58756
ms.sourcegitcommit: 42f01cad0bf15224222b2aeadb48f03d46c35723
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2021
ms.locfileid: "12154500"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Заметки о выпуске для стабильного канала Microsoft Edge

Эти заметки о выпуске содержат сведения о новых компонентах и обновлениях, не связанных с безопасностью, которые включены в стабильный канал Microsoft Edge.

- Список всех обновлений системы безопасности находится [здесь](microsoft-edge-relnotes-security.md).
- Архивные заметки о выпуске для канала Microsoft Edge Stable находятся [здесь](microsoft-edge-relnote-archive-stable-channel.md).

 Чтобы ознакомиться с каналами Microsoft Edge, см. статью [Обзор каналов Microsoft Edge](microsoft-edge-channels.md).

> [!NOTE]
> Для канала Stable обновления последовательно разворачиваются в течение одного или нескольких дней. Дополнительные сведения см. в статье [Последовательные развертывания обновлений Microsoft Edge](microsoft-edge-update-progressive-rollout.md).
>
> Веб-платформа Microsoft Edge постоянно развивается для улучшения взаимодействия с пользователями, безопасности и конфиденциальности. Дополнительные сведения см. в статье [Изменения в Microsoft Edge, затрагивающие совместимость сайтов](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-94099258-october-30"></a>Версия 94.0.992.58: 30 октября

Исправлены различные ошибки и проблемы с производительностью для выпуска "Расширенный стабильный".

## <a name="version-950102040-october-29"></a>Версия 95.0.1020.40: 29 октября

> [!IMPORTANT]
> Это обновление содержит исправление уязвимостей [CVE-2021-38000](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-38000) и [CVE-2021-38003](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-38003), которые, как сообщают разработчики Chromium, используются на практике. Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide)

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#october-29-2021).

## <a name="version-950102038-october-28"></a>Версия 95.0.1020.38: 28 октября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-94099257-october-27"></a>Версия 94.0.992.57: 27 октября

Исправлены различные ошибки и проблемы с производительностью для выпуска "Расширенный стабильный".

## <a name="version-950102030-october-21"></a>Версия 95.0.1020.30: 21 октября

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#october-21-2021).

### <a name="feature-updates"></a>Обновления компонентов

- **Поддержка функции "Просмотр в проводнике" для библиотек SharePoint Online в Microsoft Edge**  Теперь можно включить функцию "Просмотр в проводнике" для современных библиотек документов в SharePoint Online. Чтобы пользователи могли видеть и использовать эту функцию, необходимо включить политику Microsoft Edge [Настройка функции "Просмотр в проводнике" для страниц SharePoint в Microsoft Edge](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) и обновить конфигурацию клиента SharePoint Online. Подробнее: [просмотр файлов SharePoint в проводнике в Microsoft Edge](/SharePoint/sharepoint-view-in-edge). 

- **URL-адреса файлов зоны интрасети будут открываться в проводнике Windows.**  Можно разрешить URL-адресам файлов с веб-сайтов из зоны интрасети, доступных по протоколу HTTPS, открывать проводник Windows для этих файлов и каталогов. Эту возможность можно включить с помощью политики [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled).

- **Улучшения возможностей скачивания.** Поддержка пользовательского интерфейса скачивания расширена и теперь распространяется на прогрессивные веб-приложения PWA и WebView. Кроме того, мы будет реализована поддержка перетаскивания в проводнике и на рабочем столе.

- **Возобновите работу с PDF-файлами с того места, на котором вы остановились.**  Теперь вы сможете возобновить чтение PDF-документов с того места, на котором вы остановились в прошлый раз.

- **Режим эффективности продлевает время работы батареи, когда ноутбук переключается в режим экономии заряда.**  Когда ноутбук перейдет в режим экономии заряда, включится режим эффективности, чтобы разрешить браузеру управлять ресурсами для увеличения времени работы батареи вашего устройства. При включенном режиме эффективности можно выбрать четыре варианта: "Отключено от электросети и низкий уровень заряда батареи", "Отключено от сети", "Всегда" и "Никогда". Примечание. Эта функция входит в состав контролируемого выпуска функций. Если эта функция отсутствует, вернитесь сюда позже, поскольку выпуск продолжается.

- **К документам PDF добавлены поля для произвольного текста.** Теперь поддерживается добавление полей для произвольного текста в документы в формате PDF. С помощью этих полей можно заполнять формы и добавлять видимые заметки.

- **В Коллекции добавлена поддержка цитирования.**  Улучшены возможности Коллекций, особенно для учащихся и исследователей. Коллекции будут поддерживать цитаты и списки для чтения.

- **Более быстрое и удобное обновление паролей.** Теперь в браузере сразу будет открываться страница изменения пароля для заданного веб-сайта. За счет этого пользователю уже не нужно тратить время и переходить на эту страницу вручную. После открытия этой страницы браузер автоматически заполнит ваш существующий пароль, а также предложит новый уникальный и надежный пароль.  Примечание. В настоящее время эта функция доступна на ограниченном количестве сайтов.

- **Автоматическое создание учетных записей.** Теперь предоставляется дополнительная поддержка страниц регистрации: можно одним щелчком создать ученую запись интернет-служб. Для этого нужно выбрать предложение в раскрывающемся списке при щелчке любого поля в форме регистрации. При том будут показаны сведения, необходимые для формы регистрации, а также будет предложен новый надежный пароль. После выбора все применимые сведения будут введены в соответствующие поля, а предложенный пароль будет автоматически сохранен при отправке на этот веб-сайт. Примечание. В настоящее время эта функция доступна на ограниченном количестве сайтов.

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

- [BrowserLegacyExtensionPointsBlockingEnabled](/DeployEdge/microsoft-edge-policies#browserlegacyextensionpointsblockingenabled) — включение блокировки устаревших точек расширения браузера
- [CrossOriginWebAssemblyModuleSharingEnabled](/DeployEdge/microsoft-edge-policies#crossoriginwebassemblymodulesharingenabled) — указывает, могут ли модули WebAssembly отправляться из разных источников
- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) — указывает, установлена или пропущена политика разрешений записи экрана
- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) — настройка корректировки пикселей между значениями высоты window.open со страниц в режиме IE и со страниц в режиме Edge
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenwidthadjustment) — настройка корректировки пикселей между значениями ширины window.open со страниц в режиме IE и со страниц в режиме Edge
- [IntranetFileLinksEnabled](/DeployEdge/microsoft-edge-policies#intranetfilelinksenabled) — разрешить открывать URL-адреса файлов зоны интрасети Microsoft Edge в проводнике Windows
- [NewSmartScreenLibraryEnabled](/DeployEdge/microsoft-edge-policies#newsmartscreenlibraryenabled) — включить новую библиотеку SmartScreen
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) — настроить поведение отката ShadowStack в случае сбоев
- [VisualSearchEnabled](/DeployEdge/microsoft-edge-policies#visualsearchenabled) — визуальный поиск включен

#### <a name="obsoleted-policies"></a>Устаревшие политики

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) Разрешить тестирование режима Internet Explorer
- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Поддержка стандартного устаревшего параметра поведения SameSite для cookie-файлов.

## <a name="version-94099250-october-14"></a>Версия 94.0.992.50: 14 октября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-94099247-october-11"></a>Версия 94.0.992.47: 11 октября

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#october-11-2021).

## <a name="version-94099238-october-1"></a>Версия 94.0.992.38: 1 октября

> [!Important]
> Это обновление содержит исправление уязвимостей [CVE-2021-37975](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37975) и [CVE-2021-37976](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37976), для которых, как сообщают разработчики Chromium, имеются действующие эксплойты. Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide)

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#october-01-2021).

## <a name="version-94099237-september-30"></a>Версия 94.0.992.37: 30 сентября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-94099231-september-24"></a>Версия 94.0.992.31: 24 сентября

> [!Important]
> В этом обновлении содержится исправление уязвимости [CVE-2021-37973](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37973), которая, как сообщают разработчики Chromium, используется на практике. Дополнительные сведения см. в [Руководстве по обновлению системы безопасности](https://msrc.microsoft.com/update-guide).

Обновления безопасности канала Stable перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#september-24-2021).

### <a name="feature-updates"></a>Обновления компонентов

- **Microsoft Edge завершил переход на 4-недельный цикл обновлений.**  Мы перешли на новый 4-недельный цикл выпуска основных версий. Дополнительные сведения см. здесь: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **Доступен новый вариант выпуска "Расширенный стабильный".**  Мы предлагаем новый вариант выпуска "Расширенный стабильный" для управляемых корпоративных клиентов. Вариант выпуска "Расширенный стабильный" будет сохраняться в четных версиях и обновляться каждые 8 недель. Система безопасности будет обновляться каждые две недели.  Дополнительные сведения см. здесь: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Улучшение поведения по умолчанию при открытии MHTML-файлов.**  MHTML-файлы будут по-прежнему открываться в режиме IE (если он включен), если только они не были сохранены в Microsoft Edge (с помощью параметров "Сохранить как" или "Сохранить страницу как"). Если файл сохранен в Microsoft Edge, он будет открываться только в Microsoft Edge.  Это изменение устраняет проблему отрисовки, которая наблюдалась при открытии MHTML-файлов, сохраненных в Microsoft Edge, в режиме IE.

- **Ограничение запросов частной сети безопасными контекстами.** При доступе к ресурсам в локальных (частных) сетях со страниц в Интернете требуется, чтобы эти страницы доставлялись по протоколу HTTPS. Это изменение осуществляется в проекте Chromium, на котором основан Microsoft Edge. Дополнительные сведения см. в [записи о состоянии платформы Chrome](https://chromestatus.com/feature/5436853517811712). Для поддержки сценариев, необходимых для сохранения совместимости с незащищенными страницами, доступны две политики совместимости: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) и [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls).

- **Блокировка скачивания смешанного контента.** На защищенных страницах разрешено скачивание только файлов, размещенных на других защищенных страницах, а загрузки, размещенные на незащищенных (отличных от HTTPS) страницах, блокируются, если они инициируются с защищенной страницы. Это изменение осуществляется в проекте Chromium, на котором основан Microsoft Edge. Дополнительные сведения см. в [записи блога безопасности Google](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html).

- **Включение неявного входа для локальных учетных записей.** Если включить политику [OnlyOnPremisesImplicitSigninEnabled](/deployedge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled), неявный вход будет включен только для локальных учетных записей.  Браузер Microsoft Edge не будет пытаться выполнять неявный вход в учетные записи MSA и AAD. Переход с локальных учетных записей на учетные записи AAD также будет остановлен.

- **Новая страница сведений о специальных возможностях.**  Сведения о специальных возможностях теперь доступны на отдельной странице. Новую страницу можно найти в списке основных параметров edge://settings/accessibility. Здесь находятся параметры для увеличения масштаба веб-страницы и отображения хорошо заметного контура вокруг области фокусировки, а также другие параметры, позволяющие улучшить просмотр веб-страниц. Мы продолжим добавлять здесь новые параметры для будущих версий Microsoft Edge.

***Новые политики***

- [ApplicationGuardPassiveModeEnabled](/DeployEdge/microsoft-edge-policies#applicationguardpassivemodeenabled) — позволяет игнорировать конфигурацию списка сайтов Application Guard и просматривать сайты в Edge обычным образом.
- [OnlyOnPremisesImplicitSigninEnabled](/DeployEdge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) — включает неявный вход только для локальных учетных записей.
- [WebRtcRespectOsRoutingTableEnabled](/DeployEdge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) — включает поддержку правил таблицы маршрутизации Windows при создании одноранговых подключений через WebRTC.

***Устаревшая политика***

- [UserAgentClientHintsEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) — включает функцию клиентских подсказок User-Agent.

## <a name="version-93096152-september-16"></a>Версия 93.0.961.52: 16 сентября

>[!Important]
>В этом обновлении содержится исправление уязвимости [CVE-2021-30633](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30632), которая, как сообщают разработчики Chromium, используется на практике. Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide).

Обновления для системы безопасности в стабильном канале перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#september-16-2021).

## <a name="version-93096147-september-11"></a>Версия93.0.961.47: 11сентября

> [!Important]
> В этом обновлении содержится исправление уязвимости [CVE-2021-30632](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30632), которая, как сообщают разработчики Chromium, используется на практике. Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide).

Обновления безопасности стабильного канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#september-11-2021).

## <a name="version-93096144-september-9"></a>Версия 93.0.961.44: 9 сентября

Обновления безопасности стабильного канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#september-09-2021).

## <a name="version-93096138-september-2"></a>Версия 93.0.961.38: 2 сентября

Обновления безопасности стабильного канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#september-02-2021).

### <a name="feature-updates"></a>Обновления компонентов

- **Начальные предпочтения в Microsoft Edge.**  Microsoft Edge теперь поддерживает ограниченное количество начальных предпочтений (прежнее название — главные предпочтения). ИТ-администраторы могут развернуть эти параметры по умолчанию до первого запуска браузера пользователями. Дополнительные сведения: [Настройка Microsoft Edge с помощью параметров начальных предпочтений для первого запуска](/deployedge/initial-preferences-support-on-microsoft-edge-browser).

- **Режим IE в Microsoft Edge поддерживает поведение "без слияния".**  Для конечных пользователей при запуске нового окна браузера из приложения в режиме IE будет запускаться отдельный сеанс аналогично поведению "без слияния" в IE11. Вам потребуется изменить список сайтов, чтобы настроить сайты, которые должны запрещать общий доступ к сеансу в режиме "без слияния". Для каждого окна Microsoft Edge при первом посещении вкладки режима IE в этом окне, если это один из назначенных сайтов "без слияния", это окно блокируется в другом сеансе IE "без слияния" от всех остальных окон Microsoft Edge по крайней мере до закрытия последней вкладки режима IE в этом окне. Это соответствует предыдущему поведению, когда пользователи могли запускать IE с использованием режима "без слияния", а также запускать Microsoft Edge без режима "без слияния" с помощью других механизмов.  Дополнительные сведения: [Устранение неполадок режима IE и вопросы с ответами | Документация Майкрософт](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--nomerge--option-that-was-supported-in-internet-explorer-11-)

- **Новая политика для остановки неявного входа.**  Политика [ImplicitSignInEnabled](/deployedge/microsoft-edge-policies#implicitsigninenabled) позволяет системным администраторам отключить неявный вход в браузерах Microsoft Edge.

- **Политики для обхода запросов ClickOnce и DirectInvoke.** Мы обновили наши политики, чтобы включить обход запросов ClickOnce и приложения DirectInvoke для указанных типов файлов из указанных доменов. Для этого необходимо:

  - Включить [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) или [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Включить политику [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) и настроить список определенных типов файлов, для которых следует отключить ClickOnce и DirectInvoke.
  - Включить политику [AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls) и настроить список определенных доменов, для которых будут отключены ClickOnce и DirectInvoke.

  Примечание. AutoOpenAllowedForURLs — это вспомогательная политика для AutoOpenFileTypes. Если политика AutoOpenAllowedForURLs не настроена, но настроена политика AutoOpenFileTypes, указанные типы файлов будут автоматически открываться из всех URL-адресов.

- **Группы вкладок.**  Мы включаем группирование вкладок, что позволяет классифицировать вкладки по группам, определяемым пользователями, и помогает эффективнее находить и переключать вкладки, а также управлять ими в нескольких рабочих потоках.  

- **Скрытие заголовка окна при использовании вертикальных вкладок.**  Получите дополнительные несколько пикселей обратно, скрыв заголовок окна браузера при использовании вертикальных вкладок. Теперь вы можете перейти на страницу edge://settings/appearance и в разделе "Настройка панели инструментов" выбрать параметр, чтобы скрыть заголовок окна в режиме вертикальных вкладок.

- **Видео "картинка в картинке" (PiP) в панели инструментов, вызываемой при наведении курсора.**  При наведении курсора на поддерживаемое видео появляется панель инструментов, которая позволяет просматривать это видео в окне PiP.  Примечание. В настоящее время эта функция доступна для пользователей Microsoft Edge на macOS.  

- **Удаление 3DES в TLS. Поддержка комплекта шифров TLS_RSA_WITH_3DES_EDE_CBC_SHA будет удалена.** Это изменение осуществляется в проекте Chromium, на котором основан Microsoft Edge. Дополнительные сведения см. в записи о [состоянии платформы Chrome](https://chromestatus.com/feature/6678134168485888). Кроме того, в Microsoft Edge версии 93 будет доступна политика [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) для поддержки сценариев, которым необходимо сохранение совместимости с устаревшими серверами. Эта политика совместимости устареет и перестанет работать в Microsoft Edge версии 95. Обновите затронутые серверы заранее.

***Новые политики***

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
- [WAMAuthBelowWin10RS3Enabled](/DeployEdge/microsoft-edge-policies#wamauthbelowwin10rs3enabled) Диспетчер учетных записей Windows включен для проверки подлинности в Windows 10 версий до WAMAuthBelowWin10RS3Enabled

***Нерекомендуемая политика***

- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Поддержка стандартного устаревшего параметра поведения SameSite для cookie-файлов.

***Устаревшая политика***

- [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) Настройка взаимодействия с новой вкладкой Microsoft Edge

***Дополнительные изменения***

- [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) Добавление поддержки платформы Mac
- [PasswordMonitorAllowed](/DeployEdge/microsoft-edge-policies#passwordmonitorallowed) Добавление поддержки платформы Mac

## <a name="version-92090284-august-26"></a>Версия 92.0.902.84: 26 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-92090278-august-19"></a>Версия 92.0.902.78: 19 августа

Обновления безопасности стабильного канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#august-19-2021).

## <a name="version-92090273-august-12"></a>Версия 92.0.902.73: 12 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-92090267-august-5"></a>Версия 92.0.902.67: 5 августа

Обновления безопасности стабильного канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#august-05-2021).

## <a name="version-92090262-july-29"></a>Версия 92.0.902.62: 29 июля

Исправлены ошибки и проблемы с производительностью.

### <a name="modified-policy"></a>Измененная политика

- AutoplayAllowed — Отключение теперь устанавливает для автовоспроизведения мультимедиа значение "Limit".
<!-- end major 92 -->
<!-- Archive from Version 92.0.902.55: July 22 to Version 91.0.864.37: May 27 -->
<!-- Archive from 89.0.774.45: March 4 to 90.0.818.66: May 20 ->
<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
