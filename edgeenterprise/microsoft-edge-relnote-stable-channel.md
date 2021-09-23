---
title: Заметки о выпуске Microsoft Edge для стабильного канала
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 09/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для стабильного канала
ms.openlocfilehash: ffd0beb7533edf88fdab9402cb2486e71b1773e6
ms.sourcegitcommit: 85818deae134b48d7f2766e53b4400a1b4d4277d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2021
ms.locfileid: "12034448"
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

- 
            [AutoplayAllowlist](/DeployEdge/microsoft-edge-policies#autoplayallowlist) Разрешить автоматическое воспроизведение мультимедиа на определенных сайтах
- 
            [CECPQ2Enabled](/DeployEdge/microsoft-edge-policies#cecpq2enabled) Согласование постквантовых ключей CeCPQ2 включено для TLS
- 
            [ConfigureViewInFileExplorer](/DeployEdge/microsoft-edge-policies#configureviewinfileexplorer) Настройка функции "Просмотреть в проводнике" для страниц SharePoint в Microsoft Edge
- 
            [DefaultJavaScriptJitSetting](/DeployEdge/microsoft-edge-policies#defaultjavascriptjitsetting) Управление использованием JIT JavaScript
- 
            [ShowPDFDefaultRecommendationsEnabled](/DeployEdge/microsoft-edge-policies#showpdfdefaultrecommendationsenabled) Разрешить уведомлениям устанавливать Microsoft Edge в качестве программы чтения PDF-файлов по умолчанию
- 
            [FeatureFlagOverridesControl](/DeployEdge/microsoft-edge-policies#featureflagoverridescontrol) Настройка возможности пользователей переопределять флаги функций
- 
            [ImplicitSignInEnabled](/DeployEdge/microsoft-edge-policies#implicitsigninenabled) Включить неявный вход
- 
            [InternetExplorerIntegrationCloudSiteList](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) Настройка списка облачных сайтов в режиме предприятия
- 
            [InternetExplorerIntegrationSiteListRefreshInterval](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsitelistrefreshinterval) Настройка частоты обновления списка сайтов в режиме предприятия
- 
            [JavaScriptJitAllowedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitallowedforsites) Разрешить JavaScript использовать JIT на этих сайтах
- 
            [JavaScriptJitBlockedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitblockedforsites) Запретить JavaScript использовать JIT на этих сайтах
- 
            [LocalBrowserDataShareEnabled](/DeployEdge/microsoft-edge-policies#localbrowserdatashareenabled) Включить Windows для поиска в локальных данных просмотра веб-страниц через Microsoft Edge
- 
            [MAUEnabled](/DeployEdge/microsoft-edge-policies#mauenabled) Всегда использовать службу автоматического обновления Майкрософт в качестве средства обновления для Microsoft Edge
- 
            [MSAWebSiteSSOUsingThisProfileAllowed](/DeployEdge/microsoft-edge-policies#msawebsitessousingthisprofileallowed) Разрешить единый вход для сайтов Майкрософт с использованием этого профиля
- 
            [OneAuthAuthenticationEnforced](/DeployEdge/microsoft-edge-policies#oneauthauthenticationenforced) Проверка подлинности OneAuth Flow для signin
- 
            [PasswordGeneratorEnabled](/DeployEdge/microsoft-edge-policies#passwordgeneratorenabled) Разрешить пользователям получать подсказку надежного пароля при каждом создании учетной записи в Интернете
- 
            [PrimaryPasswordSetting](/DeployEdge/microsoft-edge-policies#primarypasswordsetting) Настраивает параметр, предлагающий пользователям ввести пароль устройства при использовании автозаполнения паролей
- 
            [PrintingWebpageLayout](/DeployEdge/microsoft-edge-policies#printingwebpagelayout) Задает макет для печати
- 
            [RemoteDebuggingAllowed](/DeployEdge/microsoft-edge-policies#remotedebuggingallowed) Разрешить удаленную отладку
- 
            [RelaunchWindow](/DeployEdge/microsoft-edge-policies#relaunchwindow) Установка интервала времени для повторного запуска
- 
            [TravelAssistanceEnabled](/DeployEdge/microsoft-edge-policies#travelassistanceenabled) Включить помощь в поездках
- 
            [TripleDESEnabled](/DeployEdge/microsoft-edge-policies#tripledesenabled) Включить шифры 3DES в TLS
- 
            [WAMAuthBelowWin10RS3Enabled](/DeployEdge/microsoft-edge-policies#wamauthbelowwin10rs3enabled) Диспетчер учетных записей Windows включен для проверки подлинности в Windows 10 версий до WAMAuthBelowWin10RS3Enabled

***Устаревшая политика***

- 
            [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Поддержка стандартного устаревшего параметра поведения SameSite для cookie-файлов.

***Устаревшая политика***

- 
            [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) Настройка взаимодействия с новой вкладкой Microsoft Edge

***Дополнительные изменения***

- 
            [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) Добавление поддержки платформы Mac
- 
            [PasswordMonitorAllowed](/DeployEdge/microsoft-edge-policies#passwordmonitorallowed) Добавление поддержки платформы Mac

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

## <a name="version-92090255-july-22"></a>Версия 92.0.902.55: 22 июля

Обновления безопасности канала Stable перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#july-22-2021).

### <a name="feature-updates"></a>Обновления компонентов


            **Пользователи могут легко перейти в режим Internet Explorer в Microsoft Edge**. Начиная с Microsoft Edge версии 92, пользователи могут перезагрузить сайт в режиме Internet Explorer в Microsoft Edge, а не в отдельном приложении IE 11 в ожидании настройки сайта в списке сайтов в режиме предприятия. Пользователям будет предложено добавить сайт в список локальных сайтов, чтобы переход на ту же страницу в Microsoft Edge автоматически происходил в режиме IE в течение следующих 30 дней. Вы можете использовать политику [InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed), чтобы настроить это взаимодействие и разрешить доступ к точкам входа в режиме IE, а также настроить возможность добавления сайтов в список локальных сайтов. Вы можете использовать политику [InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) для настройки количества дней, в течение которых сайты остаются в списке локальных сайтов. Обратите внимание, что комплексной работы для Windows 10 версии 1909 требуется KB5003698 или более поздняя версия, для Windows 10 версии 2004, Windows 10 версии 20H2 или Windows 10 версии 21H1 требуется KB5003690 или более поздняя версия. Дополнительные сведения см. в статье [локальный список сайтов в режиме IE](/deployedge/edge-ie-mode-local-site-list).


            **MHTML-файлы по умолчанию открываются в режиме Internet Explorer**. Начиная с Microsoft Edge версии 92 Stable, MHTML-файлы автоматически открываются в режиме Internet Explorer в Microsoft Edge, а не в приложении Internet Explorer (IE11). Это чаще всего наблюдается при попытке просмотра электронной почты Outlook в браузере. Это изменение будет происходить только в том случае, если IE11 является обработчиком по умолчанию для этого типа файлов. Изменить этот параметр при желании можно перед установкой обновления стабильной версии 92 с помощью [этого руководства](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).


            **Предупреждение "Отключить расширения режима разработчика" можно отключить на 2 недели**. Начиная с Microsoft Edge версии 92, можно на 2 недели отложить предупреждение "Отключить расширения режима разработчика", выбрав этот вариант в раскрывающемся списке в диалоговом окне предупреждения.


            **Управляйте расширениями непосредственно с панели инструментов**. Совершенно новое меню расширений на панели инструментов позволит легко скрыть расширения или закрепить их. Быстрые ссылки на управление расширениями и поиск новых расширений упростят поиск новых расширений и управление существующими.


            **По умолчанию для автоматического воспроизведения будет установлено ограничение**.  Чтобы помочь вам сосредоточиться на главном в Интернете, мы изменили значение по умолчанию для автоматического воспроизведения мультимедиа с "Разрешить" на "Ограничено", начиная с Microsoft Edge версии 92.


            **Платежные средства теперь синхронизируются между устройствами**. Начиная с Microsoft Edge версии 92, вы можете синхронизировать платежную информацию между устройствами, на которых вы выполнили вход. Обратите внимание: это контролируемый выпуск компонентов. Если вы не видите эту возможность, вернитесь сюда позже, так как выпуск продолжается.
В настоящее время эта возможность доступна только в США и только для пользователей MSA (не AAD)


            **Улучшение передачи шрифтов**. Улучшена четкость и снижена размытость при передаче текста. Обратите внимание: это контролируемый выпуск компонентов. Если вы не видите эту возможность, вернитесь сюда позже, так как выпуск продолжается.


            **Функции кнопки панели инструментов, например "Избранное" и "Коллекции", запомнят выбор пользователя и закрепят соответствующие файлы в боковой части окна**. Теперь эта возможность включается по умолчанию, если пользователь закрепит кнопку панели инструментов. Она всегда будет открываться в состоянии закрепления, пока пользователь не открепит ее.


            **Теперь пользователи могут использовать групповую политику для управления параметром "Разрешить единый вход для рабочих и учебных сайтов с помощью этого профиля"**.  Параметр "Разрешить единый вход для рабочих и учебных сайтов с помощью этого профиля" позволяет профилям, не принадлежащим к AAD, использовать единый вход для рабочих и учебных сайтов с помощью учетных данных компании или учебного заведения, имеющихся на компьютере. Этот параметр отображается для пользователей как переключатель в разделе "Параметры" -> "Профили" -> "Параметры профиля только для профилей, не принадлежащих к AAD".  Для настройки поведения можно использовать политику [AADWebSiteSOUsingThisProfileEnabled.](/deployedge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled)  


            **Работоспособность пароля** Важно использовать надежные и уникальные пароли для различных учетных записей, чтобы защитить себя в Интернете. Однако это проще сказать, чем сделать. У большинства пользователей выработались плохие привычки в отношении паролей, например использовать слабые пароли, которые легко угадать, или повторно использовать один надежный пароль для всех учетных записей.

Эта последняя версия Microsoft Edge позволяет несколько упростить задачу использования надежных и уникальных паролей. Теперь Microsoft Edge будет сообщать вам, достаточно ли надежны сохраненные пароли, а также указывать, использовались ли они на нескольких сайтах, что поможет вам защитить себя в Интернете. Сведения о работоспособности пароля можно найти в списке сохраненных паролей на странице edge://settings/passwords.
  

            **Дополнительная конфиденциальность сохраненных паролей** Если вы используете устройство вместе с другими пользователями или по какой-либо причине оставили компьютер незаблокированным, вы можете выбрать вторую проверку с использованием пароля устройства, чтобы другие пользователи не получили доступ к вашим паролям веб-сайтов. Просто!


            **Расширение Outlook**.  Эффективно управляйте папкой "Входящие", календарем, задачами и т. д. в Microsoft Outlook, не открывая новое окно браузера.  Новое расширение Outlook можно получить здесь: [Microsoft Outlook. Надстройки Microsoft Edge](https://microsoftedge.microsoft.com/addons/detail/microsoft-outlook/kkpalkknhlklpbflpcpkepmmbnmfailf?hl=en-US)


            **Microsoft Edge, соответствуя проекту с открытым кодом Chromium, обновляет способ отрисовки таблиц на веб-страницах**. С помощью этого изменения устраняются известные проблемы, и Microsoft Edge приближается к тому определенному способу отрисовки таблиц, который предполагается в других веб-браузерах. Рекомендуем протестировать важные рабочие процессы в вашей среде и убедиться в отсутствии непредвиденных проблем. Полное разъяснение см. [здесь](https://docs.google.com/document/d/16PFD1GtMI9Zgwu0jtPaKZJ75Q2wyZ9EZnVbBacOfiNA/edit).

### <a name="new-policies"></a>Новые политики

- 
            [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) Включение единого входа для рабочих и учебных сайтов с помощью этого профиля
- 
            [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) Настройка автоматического использования HTTPS
- 
            [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) Управление использованием режима без монитора
- 
            [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) Указывает, следует ли разрешать небезопасным веб-сайтам делать запросы к более закрытым конечным точкам сети.
- 
            [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) Разрешает перечисленным сайтам делать запросы к более закрытым конечным точкам сети из небезопасных контекстов
- 
            [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) Указать количество дней, в течение которых сайт остается в локальном списке сайтов режима IE
- 
            [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) Разрешить перезагрузку ненастроенных сайтов в режиме Internet Explorer
- 
            [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) Указывает, разрешено ли использовать SharedArrayBuffers в контексте без изоляции от других источников

### <a name="deprecated-policy"></a>Нерекомендуемая политика

- 
            [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) Разрешить тестирование режима Internet Explorer

### <a name="obsoleted-policy"></a>Устаревшая политика

- 
            [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) Разрешить сертификаты, подписанные с помощью SHA-1 при выдаче локальными якорями доверия

## <a name="version-91086471-july-19"></a>Версия 91.0.864.71: 19 июля

> [!Important]
>В этом обновлении содержится исправление уязвимости [CVE-2021-30563](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30563), которая, как сообщают разработчики Chromium, используется на практике. Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Обновления безопасности канала Stable перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#july-19-2021).

## <a name="version-91086467-july-8"></a>Версия 91.0.864.67: 8 июля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-91086464-july-2"></a>Версия 91.0.864.64: 2 июля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-91086459-june-24"></a>Версия 91.0.864.59: 24 июня

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#june-24-2021).

## <a name="version-91086454-june-18"></a>Версия 91.0.864.54: 18 июня

> [!Important]
> В этом обновлении содержится исправление уязвимости [CVE-2021-30554](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30554), которая, как сообщают разработчики Chromium, используется на практике. Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#june-18-2021).

## <a name="version-91086448-june-11"></a>Версия 91.0.864.48: 11 июня

> [!Important]
>В этом обновлении содержится исправление уязвимости [CVE-2021-30551](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30551), которая, как сообщают разработчики Chromium, используется на практике. Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#june-11-2021).

## <a name="version-91086441-june-3"></a>Версия 91.0.864.41: 3 июня

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#june-3-2021).

## <a name="version-91086437-may-27"></a>Версия 91.0.864.37: 27 мая

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#may-27-2021).

### <a name="feature-updates"></a>Обновления компонентов

- 
            **Определение сетевого трафика, исходя из контейнеров Application Guard в Microsoft Defender на уровне прокси-сервера**. Начиная с Microsoft Edge версии 91, для добавления тегов сетевого трафика, исходящего из контейнеров Application Guard, встраивается поддержка, что позволяет предприятиям идентифицировать их и применять определенные политики.

- 
            **Параметр поддержки, позволяющий синхронизировать избранное из хоста в контейнер Edge Application Guard.** 
           Начиная с Microsoft Edge версии 91, пользователи могут настроить Application Guard для синхронизации избранного из хоста в контейнер. Это также гарантирует появление нового избранного в контейнере.

- 
            **Начиная с Microsoft Edge версии 91 браузер автоматически прерывает загрузки типов, которые могут нанести вред вашему компьютеру, если они начинаются без взаимодействия с пользователем и не поддерживаются проверкой репутации приложений по данным SmartScreen.** 
           Пользователи могут переопределять и продолжать загрузку, щелкнув правой кнопкой мыши и выбрав параметр "Keep" ("Сохранить") на элементе загрузки. Администраторы предприятия могут отказаться от этого, настроив следующую политику:
  - 
            [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings.md) – Отключение предупреждений о расширениях загружаемых файлов для определенных типов файлов в доменах

    Дополнительные сведения см. в [Перебои загрузок Microsoft Edge Security](microsoft-edge-security-downloads-interruptions.md).

- 
            **Поддержка API распознавания речи.** 
           Начиная с Microsoft Edge версии 91, добавляется поддержка API команд распознавания речи на Google.com и аналогичных сайтах. Эта возможность доступна только случайно выбранной группе пользователей, участвующих в эксперименте. Эти пользователи предоставляют отзывы службе поддержки.

- 
            **Персонализация браузера с помощью новых цветовых тем.** 
           Персонализируйте Microsoft Edge с помощью одной из четырнадцати новых цветовых тем на странице "Параметры - > Внешний вид". Вы также можете установить настраиваемые темы с сайта надстроек Microsoft Edge. [Подробнее](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено шесть новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Добавлены следующие новые политики:

- 
            [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) — идентификация трафика Application Guard
- 
            [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) — явно разрешенные сетевые порты
- 
            [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) — разрешение импорта параметров страниц запуска
- 
            [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) — позволяет пользователям вставлять фрагменты математических задач и получать решение с пошаговым объяснением в Microsoft Edge
- 
            [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) — разрешает содержимое Microsoft News на новой странице вкладки
- 
            [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) — разрешает быстрые ссылки на новой странице вкладки

#### <a name="obsoleted-policy"></a>Устаревшая политика

- 
            [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) — включает упреждающую проверку подлинности
<!-- end major 91 -->

<!-- Archive from 89.0.774.45: March 4 to 90.0.818.66: May 20 ->
<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
