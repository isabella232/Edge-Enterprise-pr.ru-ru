---
title: Документация по политикам браузера Microsoft Edge
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 02/17/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Документация Windows и Mac для всех политик, поддерживаемых браузером Microsoft Edge
ms.openlocfilehash: e293fc948625f2a36a94184f1e0502bb5e73f65a
ms.sourcegitcommit: b85a216c616e055448028754971cd6dc4c308e81
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "11340609"
---
# Microsoft Edge - Политики

Последняя версия Microsoft Edge включает в себя следующие политики. Эти политики можно использовать для настройки работы Microsoft Edge в вашей организации.

Информацию о дополнительном наборе политик, используемых для управления тем, как и когда обновляется Microsoft Edge, можно найти в [справочнике по политике обновления Microsoft Edge](microsoft-edge-update-policies.md).

Вы можете скачать [Microsoft Security Compliance Toolkit](https://www.microsoft.com/download/details.aspx?id=55319) для рекомендуемых базовых параметров конфигурации безопасности для Microsoft Edge. Дополнительные сведения см. в [блоге Microsoft Security Baselines](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines).

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## Новые и устаревшие политики

В таблице ниже перечислены новые и устаревшие политики для этого обновления.

| Имя | Заголовок |
|--|--|
|[SSLErrorOverrideAllowedForOrigins](#sslerroroverrideallowedfororigins)|Разрешить пользователям продолжать работу со страницы предупреждения HTTPS для определенных источников|
|[WindowOcclusionEnabled](#windowocclusionenabled)|Включить загораживание окна|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|Включить загораживание собственного окна (устарело)|

## Доступные политики

В этих таблицах перечислены все связанные с браузером групповые политики, доступные в этом выпуске Microsoft Edge. Для получения дополнительных сведений о конкретных политиках см. ссылки в таблице.

|||
|-|-|
|[Параметры Application Guard](#application-guard-settings)|[Передавать](#cast)|
|[Настройки контента](#content-settings)|[Поставщик поиска по умолчанию](#default-search-provider)|
|[Расширения](#extensions)|[Проверка подлинности HTTP](#http-authentication)|
|[Параметры режима полного экрана](#kiosk-mode-settings)|[Управляемость](#manageability)|
|[Встроенные сообщения](#native-messaging)|[Менеджер паролей и защита](#password-manager-and-protection)|
|[Производительность](#performance)|[Вывод на печать](#printing)|
|[Прокси-сервер](#proxy-server)|[Параметры вкладки для сна](#sleeping-tabs-settings)|
|[Параметры SmartScreen](#smartscreen-settings)|[Автозагрузка, домашняя страница и новая вкладка](#startup-home-page-and-new-tab-page)|
|[Дополнительно](#additional)|

### [*Параметры Application Guard*](#application-guard-settings-policies)

|Имя политики|Заголовок|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|Прокси-сервер контейнера Application Guard|
|[ApplicationGuardFavoritesSyncEnabled](#applicationguardfavoritessyncenabled)|Включена синхронизация избранного в Application Guard|
### [*Передавать*](#cast-policies)

|Имя политики|Заголовок|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|Включить Google Cast|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|Показать иконку передачи на панели инструментов|
### [*Настройки контента*](#content-settings-policies)

|Имя политики|Заголовок|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|Автоматически выбирать клиентские сертификаты для этих сайтов|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|Разрешить куки на определенных сайтах|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|Блокировка cookie-файлов на определенных сайтах|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|Ограничить использование файлов cookie с определенных веб-сайтов текущим сеансом|
|[DefaultCookiesSetting](#defaultcookiessetting)|Настройка файлов cookie|
|[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)|Управление использованием API файловой системы для чтения|
|[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)|Управление использованием API файловой системы для записи|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|Настройка геолокации по умолчанию|
|[DefaultImagesSetting](#defaultimagessetting)|Настройка изображений по умолчанию|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|Контроль использования небезопасных исключений содержимого|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|Настройка JavaScript по умолчанию|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|Настройка уведомлений по умолчанию|
|[DefaultPluginsSetting](#defaultpluginssetting)|Параметр Adobe Flash по умолчанию (устарело)|
|[DefaultPopupsSetting](#defaultpopupssetting)|Параметр всплывающего окна по умолчанию|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|Контроль использования веб-API Bluetooth|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|Контроль использования API WebUSB|
|[FileSystemReadAskForUrls](#filesystemreadaskforurls)|Разрешить доступ на чтение через API файловой системы на этих сайтах|
|[FileSystemReadBlockedForUrls](#filesystemreadblockedforurls)|Блокировать доступ на чтение через API файловой системы на этих сайтах|
|[FileSystemWriteAskForUrls](#filesystemwriteaskforurls)|Разрешить доступ на запись к файлам и каталогам на этих сайтах|
|[FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls)|Блокировать доступ на запись к файлам и каталогам на этих сайтах|
|[ImagesAllowedForUrls](#imagesallowedforurls)|Разрешить изображения на этих сайтах|
|[ImagesBlockedForUrls](#imagesblockedforurls)|Блокировать изображения на определенных сайтах|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|Разрешить небезопасный контент на указанных сайтах|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|Блокировать небезопасный контент на указанных сайтах|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|Разрешить JavaScript на определенных сайтах|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|Блокировать JavaScript на определенных сайтах|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|Включить стандартную настройку поведения файлов cookie SameSite по умолчанию|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|Возврат к устаревшему поведению SameSite для файлов cookie на указанных сайтах|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|Разрешить уведомления на определенных сайтах|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|Блокировать уведомления на определенных сайтах|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|Разрешить подключаемый модуль Adobe Flash на определенных сайтах (устарело)|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|Блокировать подключаемый модуль Adobe Flash на определенных сайтах (устарело)|
|[PopupsAllowedForUrls](#popupsallowedforurls)|Разрешить всплывающие окна на определенных сайтах|
|[PopupsBlockedForUrls](#popupsblockedforurls)|Блокировать всплывающие окна на определенных сайтах|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|Регистрация обработчиков протокола|
|[SpotlightExperiencesAndRecommendationsEnabled](#spotlightexperiencesandrecommendationsenabled)|Выберите, могут ли пользователи получать настроенные фоновые изображения и текст, предложения, уведомления
и советы для служб Майкрософт|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|Предоставить доступ к определенным сайтам для подключения к определенным USB-устройствам|
|[WebUsbAskForUrls](#webusbaskforurls)|Разрешить WebUSB на определенных сайтах|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|Блокировка WebUSB на определенных сайтах|
### [*Поставщик поиска по умолчанию*](#default-search-provider-policies)

|Имя политики|Заголовок|
|-|-|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|Включить поисковую систему по умолчанию|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|Кодировки поставщика поиска по умолчанию|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|Определяет функцию поиска по изображению для поставщика поиска по умолчанию|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|Параметры для изображения URL, который использует POST|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|Ключевое слово поставщика поиска по умолчанию|
|[DefaultSearchProviderName](#defaultsearchprovidername)|Имя поставщика поиска по умолчанию|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|URL поиска по умолчанию для поисковой системы|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|URL поставщика поиска по умолчанию для предложений|
|[NewTabPageSearchBox](#newtabpagesearchbox)|Настройка интерфейса поля поиска на новой вкладке|
### [*Расширения*](#extensions-policies)

|Имя политики|Заголовок|
|-|-|
|[BlockExternalExtensions](#blockexternalextensions)|Блокировка установки внешних расширений|
|[ExtensionAllowedTypes](#extensionallowedtypes)|Настройте разрешенные типы расширений|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|Разрешить установку определенных расширений|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|Определить, какие расширения нельзя установить|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|Определить, какие расширения устанавливаются в автоматическом режиме|
|[ExtensionInstallSources](#extensioninstallsources)|Настроить расширение и исходные тексты для установки пользовательских скриптов|
|[ExtensionSettings](#extensionsettings)|Настройка параметров управления расширениями|
### [*Проверка подлинности HTTP*](#http-authentication-policies)

|Имя политики|Заголовок|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|Разрешение запросов на проверку подлинности в нескольких источниках|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|Указывает список серверов, которым Microsoft Edge может делегировать учетные данные пользователя|
|[AuthSchemes](#authschemes)|Поддерживаемые схемы аутентификации|
|[AuthServerAllowlist](#authserverallowlist)|Настроить список разрешенных серверов аутентификации|
|[BasicAuthOverHttpEnabled](#basicauthoverhttpenabled)|Разрешить базовую проверку подлинности для HTTP|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|Отключить поиск CNAME при согласовании проверки подлинности Kerberos|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Включить нестандартный порт в Kerberos SPN|
|[NtlmV2Enabled](#ntlmv2enabled)|Проверьте, включена ли проверка подлинности NTLMv2|
|[WindowsHelloForHTTPAuthEnabled](#windowshelloforhttpauthenabled)|Функция Windows Hello для проверки подлинности HTTP включена|
### [*Параметры режима полного экрана*](#kiosk-mode-settings-policies)

|Имя политики|Заголовок|
|-|-|
|[KioskAddressBarEditingEnabled](#kioskaddressbareditingenabled)|Настройка редактирования в адресной строке для общедоступного просмотра в режиме терминала|
|[KioskDeleteDownloadsOnExit](#kioskdeletedownloadsonexit)|Удалять файлы, загруженные в сеансе терминала, при закрытии Microsoft Edge|
### [*Управляемость*](#manageability-policies)

|Имя политики|Заголовок|
|-|-|
|[MAMEnabled](#mamenabled)|Управление мобильными приложениями включено|
### [*Встроенные сообщения*](#native-messaging-policies)

|Имя политики|Заголовок|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|Контроль, какие нативные хосты обмена сообщениями могут использовать пользователи|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|Настроить собственный черный список сообщений|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|Разрешить собственные узлы обмена сообщениями на уровне пользователя (установлены без прав администратора)|
### [*Менеджер паролей и защита*](#password-manager-and-protection-policies)

|Имя политики|Заголовок|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|Включить сохранение паролей в диспетчере паролей|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|Разрешение отправки оповещений пользователям, если их пароли окажутся небезопасными.|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|Настройте URL смены пароля|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|Настройка списка корпоративных URL-адресов входа, где служба защиты пароля должна фиксировать соленые хэши пароля|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|Настройте триггер предупреждения о защите паролем|
|[PasswordRevealEnabled](#passwordrevealenabled)|Включить кнопку отображения пароля|
### [*Производительность*](#performance-policies)

|Имя политики|Заголовок|
|-|-|
|[StartupBoostEnabled](#startupboostenabled)|Включить усиление начальной загрузки|
### [*Вывод на печать*](#printing-policies)

|Имя политики|Заголовок|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|Правила выбора принтера по умолчанию|
|[PrintHeaderFooter](#printheaderfooter)|Верхние и нижние колонтитулы печати|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|Установить системный принтер по умолчанию в качестве принтера по умолчанию|
|[PrinterTypeDenyList](#printertypedenylist)|Отключить типы принтеров из списка запрещенных|
|[PrintingAllowedBackgroundGraphicsModes](#printingallowedbackgroundgraphicsmodes)|Ограничение режима печати фона|
|[PrintingBackgroundGraphicsDefault](#printingbackgroundgraphicsdefault)|Режим печати фона по умолчанию|
|[PrintingEnabled](#printingenabled)|Включить печать|
|[PrintingPaperSizeDefault](#printingpapersizedefault)|Размер страницы печати по умолчанию|
|[UseSystemPrintDialog](#usesystemprintdialog)|Печать с использованием системного диалога печати|
### [*Прокси-сервер*](#proxy-server-policies)

|Имя политики|Заголовок|
|-|-|
|[ProxyBypassList](#proxybypasslist)|Настроить правила обхода прокси-сервера (устарело)|
|[ProxyMode](#proxymode)|Настроить параметры прокси-сервера (устарело)|
|[ProxyPacUrl](#proxypacurl)|Установить URL-адрес файла .pac прокси-сервера (устарело)|
|[ProxyServer](#proxyserver)|Настроить адрес или URL прокси-сервера (устарело)|
|[ProxySettings](#proxysettings)|Параметры прокси-сервера|
### [*Параметры вкладки для сна*](#sleeping-tabs-settings-policies)

|Имя политики|Заголовок|
|-|-|
|[SleepingTabsBlockedForUrls](#sleepingtabsblockedforurls)|Блокировка вкладок для сна на определенных сайтах|
|[SleepingTabsEnabled](#sleepingtabsenabled)|Настройка вкладок для сна|
|[SleepingTabsTimeout](#sleepingtabstimeout)|Настройка времени бездействия фоновой вкладки для вкладки в режиме сна|
### [*Параметры SmartScreen*](#smartscreen-settings-policies)

|Имя политики|Заголовок|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|Запретить обходить запросы фильтра SmartScreen в Microsoft Defender для сайтов|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|Запретить обходить предупреждения фильтра SmartScreen в Microsoft Defender о загрузках|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|Настройте список доменов, для которых фильтр SmartScreen в Microsoft Defender не будет вызывать предупреждения|
|[SmartScreenEnabled](#smartscreenenabled)|Настроить фильтр SmartScreen в Microsoft Defender|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|Принудительно проверяет фильтр SmartScreen в Microsoft Defender на загрузку из надежных источников|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|Настройте фильтр SmartScreen в Microsoft Defender для блокировки потенциально нежелательных приложений|
### [*Автозагрузка&comma;, домашняя страница и новая вкладка*](#startup-home-page-and-new-tab-page-policies)

|Имя политики|Заголовок|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|Установить новую вкладку в качестве домашней страницы|
|[HomepageLocation](#homepagelocation)|Настроить URL-адрес домашней страницы|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|Настройка типов фона, разрешенных для макета страницы новой вкладки|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|Установить логотип организации на странице новой вкладки (устарело)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|Скрыть стандартные сайты по умолчанию на новой вкладке|
|[NewTabPageLocation](#newtabpagelocation)|Настроить URL-адрес страницы "Новая вкладка"|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|Установить быстрые ссылки на новую вкладку|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|Включение предварительной загрузки новой вкладки для ускорения отрисовки|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|Настройка Microsoft Edge для новой вкладки (не рекомендуется)|
|[RestoreOnStartup](#restoreonstartup)|Действие при запуске|
|[RestoreOnStartupURLs](#restoreonstartupurls)|Сайты открываются при запуске браузера|
|[ShowHomeButton](#showhomebutton)|Показать кнопку Home на панели инструментов|
### [*Дополнительно*](#additional-policies)

|Имя политики|Заголовок|
|-|-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|Включить поиск Microsoft в предложениях Bing в адресной строке|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|Настройка рекламы для сайтов с навязчивой рекламой|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|Включить удаление браузера и историю загрузок|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|Разрешить диалог выбора файла|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|Позволяет странице показывать всплывающие окна во время ее выгрузки (устаревший)|
|[AllowSurfGame](#allowsurfgame)|Разрешить серфинг|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|Разрешить страницам отправлять синхронные запросы XHR при удалении страницы (не рекомендуется)|
|[AllowTokenBindingForUrls](#allowtokenbindingforurls)|Настроить список сайтов, для которых Microsoft Edge будет пытаться установить привязку токена.|
|[AllowTrackingForUrls](#allowtrackingforurls)|Настроить исключения для предотвращения отслеживания для определенных сайтов|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|Если не удается найти веб-страницу, предлагать похожие страницы|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|Всегда открывайте PDF-файлы извне|
|[AmbientAuthenticationInPrivateModesEnabled](#ambientauthenticationinprivatemodesenabled)|Включить внешнюю аутентификацию для профилей InPrivate и Guest|
|[AppCacheForceEnabled](#appcacheforceenabled)|Разрешение повторного включения компонента AppCache, даже если он отключен по умолчанию.|
|[ApplicationLocaleValue](#applicationlocalevalue)|Настройка языкового стандарта приложения|
|[AudioCaptureAllowed](#audiocaptureallowed)|Разрешить или заблокировать захват звука|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|Сайты, которые могут получить доступ к устройствам захвата звука без запроса разрешения|
|[AudioSandboxEnabled](#audiosandboxenabled)|Разрешить запуск аудио-песочницы|
|[AutoImportAtFirstRun](#autoimportatfirstrun)|Автоматический импорт данных и настроек другого браузера при первом запуске|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|Определять список протоколов, с помощью которых можно запустить внешнее приложение из списка источников без обращения к пользователю|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|URL-адреса, с которыми можно применять параметр AutoOpenFileTypes|
|[AutoOpenFileTypes](#autoopenfiletypes)|Список типов файлов, которые должны автоматически открываться после скачивания|
|[AutofillAddressEnabled](#autofilladdressenabled)|Включить автозаполнение для адресов|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|Включить автозаполнение для кредитных карт|
|[AutoplayAllowed](#autoplayallowed)|Разрешить автозапуск мультимедиа для веб-сайтов|
|[BackgroundModeEnabled](#backgroundmodeenabled)|Продолжить запуск фоновых приложений после закрытия Microsoft Edge|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|Включает фоновые обновления в списке доступных шаблонов для коллекций и других функций, которые используют шаблоны|
|[BingAdsSuppression](#bingadssuppression)|Блокировать все объявления в результатах поиска Bing|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|Блокировка сторонних cookie-файлов|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|Включите создание профиля из всплывающего меню Identity или страницы настроек.|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|Включить гостевой режим|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|Разрешить запросы к службе сетевого времени браузера|
|[BrowserSignin](#browsersignin)|Настройки входа в браузер|
|[BrowsingDataLifetime](#browsingdatalifetime)|Параметры времени существования данных браузера|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|Используйте встроенный DNS-клиент|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|Определяет, будет ли встроенный верификатор сертификатов использоваться для проверки сертификатов сервера (не рекомендуется)|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|Отключите принудительное использование прозрачности сертификата для списка хэшей subjectPublicKeyInfo|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|Отключите принудительное использование прозрачности сертификатов для списка устаревших центров сертификации|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|Отключить принудительное использование прозрачности сертификатов для определенных URL-адресов|
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|Очистить данные браузера при закрытии Microsoft Edge|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|Очистить кэшированные изображения и файлы при закрытии Microsoft Edge|
|[ClickOnceEnabled](#clickonceenabled)|Разрешить пользователям открывать файлы с использованием протокола ClickOnce|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|Блокировка доступа к указанному списку служб и целевым объектам экспорта в Коллекциях|
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|Включить предупреждения безопасности для флагов командной строки|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|Включить обновления компонентов в Microsoft Edge|
|[ConfigureDoNotTrack](#configuredonottrack)|Настройка запрета на отслеживание|
|[ConfigureFriendlyURLFormat](#configurefriendlyurlformat)|Настройка формата по умолчанию для URL-адресов, скопированных из Microsoft Edge, и определение доступности пользователям дополнительных форматов|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|Настройте автоматический вход с учетной записью домена Active Directory, если учетная запись домена Azure AD отсутствует|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|Настроить онлайн текст в речь|
|[ConfigureShare](#configureshare)|Настройте обмен опытом|
|[CustomHelpLink](#customhelplink)|Укажите пользовательскую ссылку справки|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|Проверка перехвата DNS включена|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|Установите Microsoft Edge в качестве браузера по умолчанию|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|Разрешить доступ к службе поиска по умолчанию в контекстном меню|
|[DefaultSensorsSetting](#defaultsensorssetting)|Стандартный параметр для датчиков|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|Управление использованием API Serial|
|[DefinePreferredLanguages](#definepreferredlanguages)|Определение упорядоченного списка предпочитаемых языков, на которых должны отображаться веб-сайты, если сайт поддерживает этот язык|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|Требование наличия списка сайтов для режима предприятия перед переходом между вкладками|
|[DeleteDataOnMigration](#deletedataonmigration)|Удалить старые данные браузера при миграции|
|[DeveloperToolsAvailability](#developertoolsavailability)|Контроль, где инструменты разработчика могут использоваться|
|[DiagnosticData](#diagnosticdata)|Отправлять обязательные и необязательные диагностические данных об использовании браузера|
|[DirectInvokeEnabled](#directinvokeenabled)|Разрешить пользователям открывать файлы с использованием протокола DirectInvoke|
|[Disable3DAPIs](#disable3dapis)|Отключить поддержку API для трехмерной графики|
|[DisableScreenshots](#disablescreenshots)|Отключить создание скриншотов|
|[DiskCacheDir](#diskcachedir)|Установить каталог дискового кэша|
|[DiskCacheSize](#diskcachesize)|Установить размер дискового кэша в байтах|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|Управление режимом DNS через HTTPS|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|Укажите шаблон URI нужного преобразователя DNS-over-HTTPS.|
|[DownloadDirectory](#downloaddirectory)|Установить каталог загрузки|
|[DownloadRestrictions](#downloadrestrictions)|Разрешить ограничения загрузки|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|Включить функцию коллекций|
|[EdgeShoppingAssistantEnabled](#edgeshoppingassistantenabled)|Покупки в Microsoft Edge включены|
|[EditFavoritesEnabled](#editfavoritesenabled)|Позволяет пользователям редактировать избранное|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|Повторно включить устаревшие функции веб-платформы на ограниченное время (устарело)|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|Разрешение загрузки действий, связанных с доменом, из Microsoft (устарело)|
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|Включить онлайн проверки OCSP/CRL|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|Разрешение сертификатов, подписанных с помощью SHA-1 при выдаче локальными якорями доверия (не рекомендуется)|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|Разрешить управляемым расширениям использовать API-интерфейс Enterprise Hardware Platform|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|Разрешение доступа к средству Enterprise Mode Site List Manager|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|Отключение предупреждений о расширениях загружаемых файлов для определенных типов файлов в доменах|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Управлять связью со Службой экспериментов и конфигурации|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|Показать флажок «Всегда открывать» в диалоговом окне внешнего протокола|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|Разрешить пользователям настраивать семейную безопасность|
|[FavoritesBarEnabled](#favoritesbarenabled)|Включить панель избранного|
|[ForceBingSafeSearch](#forcebingsafesearch)|Обеспечивать соблюдение Bing SafeSearch|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|Настройте, должен ли Microsoft Edge автоматически выбирать сертификат при наличии нескольких совпадений сертификатов для сайта, настроенного с помощью «AutoSelectCertificateForUrls»|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|Включить использование эфемерных профилей|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|Принудительный поиск Google SafeSearch|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|Использование политики ссылок по умолчанию no-referrer-when-downgrade (устаревшее)|
|[ForceNetworkInProcess](#forcenetworkinprocess)|Принудительный запуск сетевого кода в процессе браузера (устарело)|
|[ForceSync](#forcesync)|Принудительно синхронизировать данные браузера и не показывать запрос на разрешение синхронизации|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|Принудительный минимальный ограниченный режим YouTube|
|[FullscreenAllowed](#fullscreenallowed)|Разрешить полноэкранный режим|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|Включить глобальный кэш проверки подлинности HTTP|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|Принудительная прямая навигация по сайту в интрасети вместо поиска по отдельным словам в адресной строке|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|Настройте список имен, которые будут обходить проверку политики HSTS|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|Используйте аппаратное ускорение, когда доступно|
|[HideFirstRunExperience](#hidefirstrunexperience)|Скрыть первый запуск опыта и заставки|
|[HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](#hideinternetexplorerredirectuxforincompatiblesitesenabled)|Скрытие диалогового окна однократного перенаправления и объявления в Microsoft Edge|
|[ImportAutofillFormData](#importautofillformdata)|Разрешить импорт данных формы автозаполнения|
|[ImportBrowserSettings](#importbrowsersettings)|Разрешить импорт настроек браузера|
|[ImportCookies](#importcookies)|Разрешить импорт файлов cookie|
|[ImportExtensions](#importextensions)|Разрешить импорт расширений|
|[ImportFavorites](#importfavorites)|Разрешить импорт избранного|
|[ImportHistory](#importhistory)|Разрешить импорт истории просмотров|
|[ImportHomepage](#importhomepage)|Разрешить импорт настроек домашней страницы|
|[ImportOpenTabs](#importopentabs)|Разрешить импорт открытых вкладок|
|[ImportPaymentInfo](#importpaymentinfo)|Разрешить импорт информации об оплате|
|[ImportSavedPasswords](#importsavedpasswords)|Разрешить импорт сохраненных паролей|
|[ImportSearchEngine](#importsearchengine)|Разрешить импорт настроек поисковой системы|
|[ImportShortcuts](#importshortcuts)|Разрешить импорт ярлыков|
|[InPrivateModeAvailability](#inprivatemodeavailability)|Настройка доступности режима InPrivate|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|Включить предупреждения для небезопасных форм|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|Управление параметром IntensiveWakeUpThrottling|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|Настройка улучшенной функции обнаружения зависаний в режиме Internet Explorer|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|Настройка интеграции с Internet Explorer|
|[InternetExplorerIntegrationLocalFileAllowed](#internetexplorerintegrationlocalfileallowed)|Разрешить запуск локальных файлов в режиме Internet Explorer|
|[InternetExplorerIntegrationLocalFileExtensionAllowList](#internetexplorerintegrationlocalfileextensionallowlist)|Открыть локальные файлы из списка разрешенных расширений файлов в режиме  Internet Explorer|
|[InternetExplorerIntegrationLocalFileShowContextMenu](#internetexplorerintegrationlocalfileshowcontextmenu)|Показать контекстное меню для открытия ссылки в режиме Internet Explorer|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|Настройка списка сайтов для режима Enterprise|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|Укажите, как ведут себя внутренние переходы на ненастроенные сайты при запуске со страниц режима Internet Explorer.|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|Разрешить тестирование режима Internet Explorer|
|[IntranetRedirectBehavior](#intranetredirectbehavior)|Поведение перенаправления в интрасети|
|[IsolateOrigins](#isolateorigins)|Включить изоляцию сайта для определенных источников|
|[LocalProvidersEnabled](#localprovidersenabled)|Разрешить предложения от местных поставщиков|
|[ManagedConfigurationPerOrigin](#managedconfigurationperorigin)|Задает определенные значения управляемой конфигурации для веб-сайтов|
|[ManagedFavorites](#managedfavorites)|Настроить избранное|
|[ManagedSearchEngines](#managedsearchengines)|Управление поисковыми движками|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|Максимальное количество одновременных подключений к прокси-серверу|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|Разрешить Google Cast подключаться к устройствам Cast на всех IP-адресах|
|[MetricsReportingEnabled](#metricsreportingenabled)|Включить отчеты с данными об использовании и сбоях данных (устаревшие)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|Включить загораживание собственного окна (устарело)|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|Установка времени ожидания перехода между вкладками списка сайтов для режима предприятия|
|[NetworkPredictionOptions](#networkpredictionoptions)|Включить прогнозирование сети|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|Настройте, всегда ли у пользователя профиль по умолчанию автоматически входит в свою учетную запись на работе или в школе|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|Контроль, где применяются ограничения безопасности для небезопасных источников|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|Разрешить веб-сайтам запрашивать доступные способы оплаты|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|Разрешить персонализацию рекламы, поиска и новостей, отправляя историю просмотров в Microsoft|
|[PinningWizardAllowed](#pinningwizardallowed)|Мастер «Разрешить закрепление на панели задач»|
|[ProactiveAuthEnabled](#proactiveauthenabled)|Включение проактивной проверки подлинности (не рекомендуется)|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|Включить рекламный контент на всей вкладке|
|[PromptForDownloadLocation](#promptfordownloadlocation)|Спросите, где сохранить загруженные файлы|
|[QuicAllowed](#quicallowed)|Разрешить протокол QUIC|
|[QuickViewOfficeFilesEnabled](#quickviewofficefilesenabled)|Управление возможностью быстрого просмотра файлов Office в Microsoft Edge|
|[RedirectSitesFromInternetExplorerPreventBHOInstall](#redirectsitesfrominternetexplorerpreventbhoinstall)|Запрет установки объекта BHO для перенаправления несовместимых сайтов из Internet Explorer в Microsoft Edge|
|[RedirectSitesFromInternetExplorerRedirectMode](#redirectsitesfrominternetexplorerredirectmode)|Перенаправление несовместимых сайтов из Internet Explorer в Microsoft Edge|
|[RelaunchNotification](#relaunchnotification)|Уведомить пользователя, что перезагрузка браузера рекомендуется или требуется для ожидающих обновлений|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|Установите период времени для уведомлений об обновлениях|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|Включить целостность кода рендерера|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|Укажите, требуются ли онлайн-проверки OCSP / CRL для локальных якорей доверия|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|Включить разрешение ошибок навигации с помощью веб-службы|
|[RestrictSigninToPattern](#restrictsignintopattern)|Ограничить, какие учетные записи могут быть использованы в качестве основных учетных записей Microsoft Edge|
|[RoamingProfileLocation](#roamingprofilelocation)|Настройка каталога перемещаемого профиля|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|Разрешение использования перемещаемых копий для данных профиля Microsoft Edge|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|Применить параметр содержимого Adobe Flash ко всему содержимому (устарело)|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|Разрешить пользователям продолжать работу со страницы предупреждения HTTPS|
|[SSLErrorOverrideAllowedForOrigins](#sslerroroverrideallowedfororigins)|Разрешить пользователям продолжать работу со страницы предупреждения HTTPS для определенных источников|
|[SSLVersionMin](#sslversionmin)|Минимальная версия TLS включена|
|[SaveCookiesOnExit](#savecookiesonexit)|Сохранять файлы cookie при закрытии Microsoft Edge|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|Отключить сохранение истории браузера|
|[ScreenCaptureAllowed](#screencaptureallowed)|Разрешить или запретить захват экрана|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|Включить прокрутку до текста, указанного в фрагментах URL|
|[SearchSuggestEnabled](#searchsuggestenabled)|Включить варианты поиска|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|Веб-сайты или домены, которым не требуется разрешение на прямую аттестацию ключа безопасности|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|Отправлять все сайты интрасети в Internet Explorer|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|Отправка сведений о сайте для улучшения служб Майкрософт (устаревший)|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|Разрешить доступ к датчиками на определенных сайтах|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|Блокировать доступ к датчиками на определенных сайтах|
|[SerialAskForUrls](#serialaskforurls)|Разрешить API Serial на определенных сайтах|
|[SerialBlockedForUrls](#serialblockedforurls)|Блокировать API Serial на определенных сайтах|
|[ShowMicrosoftRewards](#showmicrosoftrewards)|Показать возможности Microsoft Rewards|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|Показать ярлык Microsoft Office на панели избранного (не рекомендуется)|
|[ShowRecommendationsEnabled](#showrecommendationsenabled)|Разрешить рекомендации и рекламные уведомления от Microsoft Edge|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|Включить поддержку подписанного HTTP Exchange (SXG)|
|[SitePerProcess](#siteperprocess)|Включить изоляцию сайта для каждого сайта|
|[SmartActionsBlockList](#smartactionsblocklist)|Блокировка интеллектуальных действий для списка служб|
|[SpeechRecognitionEnabled](#speechrecognitionenabled)|Configure Speech Recognition|
|[SpellcheckEnabled](#spellcheckenabled)|Включить проверку орфографии|
|[SpellcheckLanguage](#spellchecklanguage)|Включить определенные языки проверки орфографии|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|Принудительное отключение языков проверки орфографии|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|Включить более строгую обработку смешанного контента (устарело)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|Подавить предупреждение о неподдерживаемой ОС|
|[SyncDisabled](#syncdisabled)|Отключить синхронизацию данных с помощью служб Microsoft Sync Services|
|[SyncTypesListDisabled](#synctypeslistdisabled)|Настройте список типов, которые исключены из синхронизации|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|Включение функции безопасности TLS 1.3 для локальных якорей доверия (устарело)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|Выбор наборов шифров TLS для отключения|
|[TabFreezingEnabled](#tabfreezingenabled)|Разрешить замораживание фоновых вкладок|
|[TargetBlankImpliesNoOpener](#targetblankimpliesnoopener)|Не устанавливать window.opener для ссылок, нацеленных на _blank|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|Включить завершающие процессы в диспетчере задач браузера|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|Установка ограничения на размер памяти (в мегабайтах), который может использовать один экземпляр Microsoft Edge.|
|[TrackingPrevention](#trackingprevention)|Блокировка отслеживания активности пользователей в Интернете|
|[TranslateEnabled](#translateenabled)|Включить перевод|
|[URLAllowlist](#urlallowlist)|Определите список разрешенных URL|
|[URLBlocklist](#urlblocklist)|Блокировать доступ к списку URL-адресов|
|[UpdatePolicyOverride](#updatepolicyoverride)|Указывает, как Центр обновления Microsoft Edge обрабатывает доступные обновления из Microsoft Edge|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|Включение функции клиентских подсказок User-Agent (устарело)|
|[UserDataDir](#userdatadir)|Установить каталог пользовательских данных|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|Ограничение количества снимков пользовательских данных, сохраняемых для применения в случае аварийного отката|
|[UserFeedbackAllowed](#userfeedbackallowed)|Разрешить обратную связь с пользователем|
|[VerticalTabsAllowed](#verticaltabsallowed)|Настройка доступности вертикального макета для вкладок на боковой панели браузера|
|[VideoCaptureAllowed](#videocaptureallowed)|Разрешить или заблокировать захват видео|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|Сайты, которые могут получить доступ к устройствам захвата видео без запроса разрешения|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|Установить оптимизацию WPAD|
|[WebAppInstallForceList](#webappinstallforcelist)|Настроить список принудительно установленных веб-приложений|
|[WebCaptureEnabled](#webcaptureenabled)|Включение функции захвата веб-страниц в Microsoft Edge|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|Повторно включить API веб-компонентов v0 до M84 (устарело).|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|Разрешить WebDriver переопределять несовместимые политики (устарело)|
|[WebRtcAllowLegacyTLSProtocols](#webrtcallowlegacytlsprotocols)|Разрешить устаревшую версию TLS/DTLS в WebRTC (устарело)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|Управление выставлением локальных IP-адресов с помощью WebRTC|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|Ограничить доступность локального IP-адреса в WebRTC|
|[WebRtcUdpPortRange](#webrtcudpportrange)|Ограничить диапазон локальных портов UDP, используемых WebRTC|
|[WebWidgetAllowed](#webwidgetallowed)|Включить мини веб-приложение|
|[WebWidgetIsEnabledOnStartup](#webwidgetisenabledonstartup)|Разрешить запускать мини веб-приложение при начальной загрузке Windows|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|Использовать сопоставитель прокси-серверов Windows (устарело)|
|[WindowOcclusionEnabled](#windowocclusionenabled)|Включить загораживание окна|




  ## Политики параметров Application Guard

  [В начало](#microsoft-edge---policies)

  ### ApplicationGuardContainerProxy

  #### Прокси-сервер контейнера Application Guard

  
  
  #### Поддерживаемые версии:

  - В Windows с 84 и более поздних версий

  #### Описание

  Настраивает параметры прокси-сервера для Microsoft Edge Application Guard.
Если эта политика включена, Microsoft Edge Application Guard игнорирует другие источники конфигураций прокси-сервера.

Если эта политика не настроена, Microsoft Edge Application Guard использует конфигурацию прокси-сервера узла.

Эта политика не влияет на конфигурацию прокси-сервера Microsoft Edge за пределами Application Guard (на узле).

Поле ProxyMode позволяет указать прокси-сервер, используемый Microsoft Edge Application Guard.

Поле ProxyPacUrl - это URL-адрес прокси-файла .pac.

Поле ProxyServer является URL-адресом прокси-сервера.

Если вы выберете значение "direct" для поля "ProxyMode", все остальные поля будут игнорироваться.

Если вы выберете значение «auto_detect» как «ProxyMode», все остальные поля будут игнорироваться.

Если вы выберите значение "fixed_servers" для "ProxyMode", будет использоваться поле "ProxyServer".

Если вы выберите значение "pac_script" для "ProxyMode", будет использоваться поле "ProxyPacUrl".

Дополнительные сведения о том, как идентифицировать трафик Application Guard с использованием двойного прокси-сервера, можно найти в статье [https://go.microsoft.com/fwlink/?linkid=2134653](https://go.microsoft.com/fwlink/?linkid=2134653).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Dictionary

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: ApplicationGuardContainerProxy
  - Имя групповой политики: Прокси-сервер контейнера Application Guard
  - Путь к групповой политике (обязательно): Административные шаблоны/Microsoft Edge/Настройки Application Guard
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ApplicationGuardContainerProxy
  - Тип значения: REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```

  ##### Компактный пример значения:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {"ProxyMode": "direct", "ProxyPacUrl": "https://internal.site/example.pac", "ProxyServer": "123.123.123.123:8080"}
  ```
  

  

  [В начало](#microsoft-edge---policies)

  ### ApplicationGuardFavoritesSyncEnabled

  #### Включена синхронизация избранного в Application Guard

  
  
  #### Поддерживаемые версии:

  - В Windows 90 и более поздних версий

  #### Описание

  Эта политика позволяет компьютерам и устройствам с Microsoft Edge, на которых включено расширение Application Guard, синхронизировать избранное с главного компьютера с контейнером, чтобы оно совпадало.

Если настроено свойство [ManagedFavorites](#managedfavorites), управляемое избранное также синхронизируется с контейнером.

Если вы включите эту политику, изменение избранного в контейнере будет отключено. В этом случае кнопки "Добавить избранное" и "Добавить папку "Избранное"" будут размыты в пользовательском интерфейсе браузера контейнера.

Если вы отключите или не настроите эту политику, избранное на главном компьютере не будет отправлено в контейнер.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ApplicationGuardFavoritesSyncEnabled
  - Имя GP: Включена синхронизация избранного в Application Guard
  - Путь к GP (обязательный): Administrative Templates/Microsoft Edge/Application Guard settings
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ApplicationGuardFavoritesSyncEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ## Политики передачи

  [В начало](#microsoft-edge---policies)

  ### EnableMediaRouter

  #### Включить Google Cast

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Включите эту политику, чтобы включить Google Cast. Пользователи смогут запускать его из меню приложения, контекстных меню страницы, элементов управления мультимедиа на веб-сайтах с поддержкой Cast и (если отображается) значка панели инструментов Cast.

Отключите эту политику, чтобы отключить Google Cast.

По умолчанию Google Cast включен.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: EnableMediaRouter
  - Название GP: Включить Google Cast
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Cast
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: EnableMediaRouter
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: EnableMediaRouter
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ShowCastIconInToolbar

  #### Показать иконку передачи на панели инструментов

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Установите для этой политики значение true, чтобы отображать значок панели инструментов Cast на панели инструментов или в меню переполнения. Пользователи не смогут удалить это.

Если вы не настроите эту политику или отключите ее, пользователи смогут закрепить или удалить значок, используя его контекстное меню.

Если вы также установили для политики [EnableMediaRouter](#enablemediarouter) значение false, эта политика игнорируется и значок панели инструментов не отображается.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ShowCastIconInToolbar
  - Имя GP: Показать иконку на панели инструментов
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Cast
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ShowCastIconInToolbar
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа настройки: ShowCastIconInToolbar
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ## Политики настроек контента

  [В начало](#microsoft-edge---policies)

  ### AutoSelectCertificateForUrls

  #### Автоматически выбирать клиентские сертификаты для этих сайтов

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  При настройке политики вы можете создать список шаблонов URL-адресов, которые определяют сайты, для которых Microsoft Edge может автоматически выбрать сертификат клиента. Значение — это массив стрингифиедных словарей JSON, каждый из которых имеет форму {"Pattern": "$URL _PATTERN", "Filter": $FILTER}, где $URL _PATTERN является шаблоном настройки содержимого. $FILTER ограничивает сертификаты клиентов, которые автоматически выбираются в браузере. Независимо от фильтра, выделяются только сертификаты, совпадающие с запросом сертификата сервера.

Примеры использования раздела $FILTER:

* Если для параметра $FILTER задано значение {"издатель": {"CN": "$ISSUER _CN"}}, выделяются только те сертификаты, которые были созданы сертификатом с _CN Коммоннаме $ISSUER.

* Если $FILTER содержит оба раздела "издатель" и "Тема", то выбираются только сертификаты клиента, удовлетворяющие обоим условиям.

* Если $FILTER содержит раздел "Тема" со значением "O", сертификату необходимо по крайней мере одна организация, соответствующая выбранному значению.

* Если $FILTER содержит раздел "Тема" со значением "OU", сертификату требуется по крайней мере одно подразделение, в котором выбрано указанное значение.

* Если для $FILTER задано значение {}, выбор сертификатов клиента также не ограничивается. Обратите внимание на то, что фильтры, предоставляемые веб-сервером, по-своему применяются.

Если политика не задана, Автовыбор для любого сайта отсутствует.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AutoSelectCertificateForUrls
  - Имя GP: автоматически выбирать клиентские сертификаты для этих сайтов
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\AutoSelectCertificateForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = "{\"pattern\":\"https://www.contoso.com\",\"filter\":{\"ISSUER\":{\"CN\":\"certificate issuer name\", \"L\": \"certificate issuer location\", \"O\": \"certificate issuer org\", \"OU\": \"certificate issuer org unit\"}, \"SUBJECT\":{\"CN\":\"certificate subject name\", \"L\": \"certificate subject location\", \"O\": \"certificate subject org\", \"OU\": \"certificate subject org unit\"}}}"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: AutoSelectCertificateForUrls
  - Пример значения:
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### CookiesAllowedForUrls

  #### Разрешить куки на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определите список сайтов на основе шаблонов URL, которым разрешено устанавливать файлы cookie.

Если вы не настроите эту политику, глобальное значение по умолчанию из политики [DefaultCookiesSetting](#defaultcookiessetting) (если установлено) или личная конфигурация пользователя используется для всех сайтов.

См. Политики [CookiesBlockedForUrls](#cookiesblockedforurls) и [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) для получения дополнительной информации.

Обратите внимание, что между этими тремя политиками не может быть конфликтующих шаблонов URL:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

Подробные сведения о шаблонах допустимых URL-адресов см. на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). * не является допустимым значением для этой политики.

Чтобы исключить удаление файлов cookie при выходе, настройте политику [SaveCookiesOnExit](#savecookiesonexit).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: CookiesAllowedForUrls
  - Название GP: Разрешить куки на определенных сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\CookiesAllowedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: CookiesAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### CookiesBlockedForUrls

  #### Блокировка cookie-файлов на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определите список сайтов на основе шаблонов URL, которые не могут устанавливать файлы cookie.

Если вы не настроите эту политику, глобальное значение по умолчанию из политики [DefaultCookiesSetting](#defaultcookiessetting) (если установлено) или личная конфигурация пользователя используется для всех сайтов.

Посмотрите политики [CookiesAllowedForUrls](#cookiesallowedforurls) и [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) для получения дополнительной информации.

Обратите внимание, что между этими тремя политиками не может быть конфликтующих шаблонов URL:

- CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

Подробные сведения о допустимом шаблоне URL-адресов см. в [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). * не является принятым значением для этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: CookiesBlockedForUrls
  - Название GP: блокировать куки на определенных сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\CookiesBlockedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: CookiesBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### CookiesSessionOnlyForUrls

  #### Ограничить использование файлов cookie с определенных веб-сайтов текущим сеансом

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Файлы cookie, созданные веб-сайтами, которые соответствуют заданному вами шаблону URL, удаляются по окончании сеанса (когда окно закрывается).

Файлы cookie, создаваемые веб-сайтами, которые не соответствуют шаблону, контролируются политикой [DefaultCookiesSetting](#defaultcookiessetting) (если установлена) или личной конфигурацией пользователя. Это также поведение по умолчанию, если вы не настроили эту политику.

Если Microsoft Edge работает в фоновом режиме, сеанс может не закрыться при закрытии последнего окна, что означает, что куки не будут удалены при закрытии окна. См. Политику [BackgroundModeEnabled](#backgroundmodeenabled) для получения информации о настройке того, что происходит, когда Microsoft Edge работает в фоновом режиме.

Вы также можете использовать политики [CookiesAllowedForUrls](#cookiesallowedforurls) и [CookiesBlockedForUrls](#cookiesblockedforurls), чтобы контролировать, какие веб-сайты могут создавать куки.

Обратите внимание, что между этими тремя политиками не может быть конфликтующих шаблонов URL:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

Подробные сведения о допустимом шаблоне URL-адресов см. в [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). * не является принятым значением для этой политики.

Если вы устанавливаете политику [RestoreOnStartup](#restoreonstartup) для восстановления URL-адресов из предыдущих сеансов, эта политика игнорируется, и файлы cookie постоянно сохраняются для этих сайтов.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: CookiesSessionOnlyForUrls
  - Имя GP: ограничение файлов cookie с определенных веб-сайтов на текущий сеанс
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: CookiesSessionOnlyForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultCookiesSetting

  #### Настройка файлов cookie

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Проверьте, могут ли веб-сайты создавать файлы cookie на устройстве пользователя. Это правило «все или ничего» - вы можете разрешить всем веб-сайтам создавать файлы cookie, или никакие веб-сайты не создают файлы cookie. Вы не можете использовать эту политику для включения файлов cookie с определенных веб-сайтов.

Установите политику в 'SessionOnly', чтобы очистить куки при закрытии сессии. Если Microsoft Edge работает в фоновом режиме, сеанс может не закрыться при закрытии последнего окна, что означает, что куки не будут удалены при закрытии окна. Посмотрите политику [BackgroundModeEnabled](#backgroundmodeenabled) для получения информации о настройке того, что происходит, когда Microsoft Edge работает в фоновом режиме.

Если вы не настроите эту политику, будет использоваться значение по умолчанию «AllowCookies», и пользователи могут изменить этот параметр в настройках Microsoft Edge. (Если вы не хотите, чтобы пользователи могли изменять этот параметр, установите политику.)

Сопоставление параметров политики:

* AllowCookies (1) = Разрешить всем сайтам создавать cookies

* BlockCookies (2) = Не разрешать сайтам создавать cookies

* SessionOnly (4) = Сохранять файлы cookie в течение сеанса, кроме перечисленных в [SaveCookiesOnExit](#savecookiesonexit)

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultCookiesSetting
  - Название GP: настроить cookies
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultCookiesSetting
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultCookiesSetting
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultFileSystemReadGuardSetting

  #### Управление использованием API файловой системы для чтения

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  Если присвоить этой политике значение "3", веб-сайты смогут запрашивать доступ на чтение к файловой системе главной ОС с помощью API файловой системы. Если присвоить этой политике значение "2", доступ будет запрещен.

Если не настроить эту политику, веб-сайты смогут запрашивать доступ. Пользователи могут изменить этот параметр.

Сопоставление параметров политики:

* BlockFileSystemRead (2) = запретить всем сайтам запрашивать доступ на чтение файлов и каталогов через API файловой системы

* AskFileSystemRead (3) = разрешить сайтам запрашивать у пользователя доступ на чтение файлов и каталогов через API файловой системы

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: DefaultFileSystemReadGuardSetting
  - Имя групповой политики: Управление использованием API файловой системы для чтения
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultFileSystemReadGuardSetting
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultFileSystemReadGuardSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultFileSystemWriteGuardSetting

  #### Управление использованием API файловой системы для записи

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  Если присвоить этой политике значение "3", веб-сайты смогут запрашивать доступ на запись к файловой системе главной ОС с помощью API файловой системы. Если присвоить этой политике значение "2", доступ будет запрещен.

Если не настроить эту политику, веб-сайты смогут запрашивать доступ. Пользователи могут изменить этот параметр.

Сопоставление параметров политики:

* BlockFileSystemWrite (2) = запретить всем сайтам запрашивать доступ на запись к файлам и каталогам

* AskFileSystemWrite (3) = разрешить сайтам запрашивать у пользователя доступ на запись к файлам и каталогам

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: DefaultFileSystemWriteGuardSetting
  - Имя групповой политики: Управление использованием API файловой системы для записи
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultFileSystemWriteGuardSetting
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultFileSystemWriteGuardSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultGeolocationSetting

  #### Настройка геолокации по умолчанию

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Установите, могут ли веб-сайты отслеживать физическое местоположение пользователей. Вы можете разрешить отслеживание по умолчанию ('AllowGeolocation'), отклонить его по умолчанию ('BlockGeolocation') или запрашивать пользователя каждый раз, когда веб-сайт запрашивает их местоположение ('AskGeolocation').

Если вы не настроите эту политику, используется политика AskGeolocation, которую пользователь может изменить.

Сопоставление параметров политики:

* AllowGeolocation (1) = разрешить сайтам отслеживать физическое местоположение пользователей

* BlockGeolocation (2) = не разрешать сайтам отслеживать местонахождение пользователей

* AskGeolocation (3) = спрашивать, когда сайт хочет отслеживать физическое местоположение пользователей

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultGeolocationSetting
  - Имя GP: настройка геолокации по умолчанию
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultGeolocationSetting
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultGeolocationSetting
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultImagesSetting

  #### Настройка изображений по умолчанию

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Установите, могут ли веб-сайты отображать изображения. Вы можете разрешить изображения на всех сайтах ('AllowImages') или заблокировать их на всех сайтах ('BlockImages').

Если вы не настроите эту политику, изображения будут разрешены по умолчанию, и пользователь может изменить этот параметр.

Сопоставление параметров политики:

* AllowImages (1) = разрешить всем сайтам показывать все изображения

* BlockImages (2) = Не разрешать сайтам показывать изображения

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultImagesSetting
  - Название GP: настройка изображений по умолчанию
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultImagesSetting
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultImagesSetting
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultInsecureContentSetting

  #### Контроль использования небезопасных исключений содержимого

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 80 или позже

  #### Описание

  Позволяет указать, могут ли пользователи добавлять исключения, разрешающие смешанный контент для определенных сайтов.

Эта политика может быть переопределена для определенных шаблонов URL с помощью политик [InsecureContentAllowedForUrls](#insecurecontentallowedforurls) и [InsecureContentBlockedForUrls](#insecurecontentblockedforurls).

Если эта политика не установлена, пользователям будет разрешено добавлять исключения, чтобы разрешить блокируемое смешанное содержимое и отключить автообновления для необязательно блокируемого смешанного содержимого.

Сопоставление параметров политики:

* BlockInsecureContent (2) = Не разрешать любому сайту загружать блокируемый смешанный контент

* AllowExceptionsInsecureContent (3) = разрешить пользователям добавлять исключения для загрузки блокируемого смешанного контента.

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultInsecureContentSetting
  - Имя GP: контроль использования небезопасных исключений содержимого
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultInsecureContentSetting
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultInsecureContentSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultJavaScriptSetting

  #### Настройка JavaScript по умолчанию

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Установите, могут ли веб-сайты запускать JavaScript. Можно разрешить эту возможность для всех сайтов («AllowJavaScript») или заблокировать для всех сайтов («BlockJavaScript»).

Если вы не настроите эту политику, все сайты могут по умолчанию запускать JavaScript, и пользователь может изменить этот параметр.

Сопоставление параметров политики:

* AllowJavaScript (1) = Разрешить всем сайтам запускать JavaScript

* BlockJavaScript (2) = Не разрешать JavaScript на любом сайте

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultJavaScriptSetting
  - Имя GP: настройка JavaScript по умолчанию
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultJavaScriptSetting
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultJavaScriptSetting
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultNotificationsSetting

  #### Настройка уведомлений по умолчанию

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Установите, могут ли веб-сайты отображать уведомления на рабочем столе. Вы можете разрешить их по умолчанию ('AllowNotifications'), запретить их по умолчанию ('BlockNotifications') или попросить пользователя каждый раз, когда веб-сайт хочет показать уведомление ('AskNotifications').

Если вы не настроите эту политику, уведомления будут разрешены по умолчанию, и пользователь может изменить этот параметр.

Сопоставление параметров политики:

* AllowNotifications (1) = Разрешить сайтам показывать уведомления на рабочем столе

* BlockNotifications (2) = Не разрешать сайтам показывать уведомления на рабочем столе

* AskNotifications (3) = Спрашивать каждый раз, когда сайт хочет показывать уведомления на рабочем столе

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultNotificationsSetting
  - Имя GP: настройка уведомления по умолчанию
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultNotificationsSetting
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultNotificationsSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultPluginsSetting

  #### Параметр Adobe Flash по умолчанию (устарело)

  
  >УСТАРЕЛО: эта политика устарела и не работает в версиях Microsoft Edge после 87.
  #### Поддерживаемые версии:

  - В Windows и macOS — версии c 77 по 87

  #### Описание

  Эта политика не работает, так как Flash больше не поддерживается Microsoft Edge.

Сначала проверяются [PluginsAllowedForUrls](#pluginsallowedforurls) и [PluginsBlockedForUrls](#pluginsblockedforurls), а затем эта политика. Варианты: "ClickToPlay" и "BlockPlugins". Если этой политике присвоено значение "BlockPlugins", этот подключаемый модуль запрещается на всех веб-сайтах. "ClickToPlay" позволяет запустить подключаемый модуль Flash, но пользователям нужно щелкнуть заполнитель, чтобы запустить его.

Если вы не настроите эту политику, пользователь может изменить этот параметр вручную.

Примечание. Автоматическое воспроизведение предназначено только для доменов, явно указанных в политике [PluginsAllowedForUrls](#pluginsallowedforurls). Чтобы включить автоматическое воспроизведение для всех сайтов, добавьте http://* и https://* в список разрешенных URL-адресов.

Сопоставление параметров политики:

* BlockPlugins (2) = Заблокировать плагин Adobe Flash

* ClickToPlay (3) = Щелкнуть для воспроизведения

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultPluginsSetting
  - Имя GP: параметр Adobe Flash по умолчанию (устарело)
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultPluginsSetting
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultPluginsSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultPopupsSetting

  #### Параметр всплывающего окна по умолчанию

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Установите, могут ли веб-сайты отображать всплывающие окна. Вы можете разрешить их на всех сайтах («AllowPopups») или заблокировать их на всех сайтах («BlockPopups»).

Если вы не настроите эту политику, всплывающие окна по умолчанию блокируются, и пользователи могут изменить этот параметр.

Сопоставление параметров политики:

* AllowPopups (1) = Разрешить показывать всплывающие окна на всех сайтах

* BlockPopups (2) = Не разрешать сайтам показывать всплывающие окна

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultPopupsSetting
  - Имя GP: настройка всплывающего окна по умолчанию
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultPopupsSetting
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultPopupsSetting
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultWebBluetoothGuardSetting

  #### Контроль использования веб-API Bluetooth

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Управление доступом веб-сайтов к близлежащим устройствам Bluetooth. Вы можете полностью заблокировать доступ или потребовать, чтобы сайт запрашивал пользователя каждый раз, когда он хочет получить доступ к устройству Bluetooth.

Если вы не настроите эту политику, будет использоваться значение по умолчанию («AskWebBluetooth», что означает, что пользователи спрашиваются каждый раз), и пользователи могут изменить его.

Сопоставление параметров политики:

* BlockWebBluetooth (2) = Не разрешать сайтам запрашивать доступ к Bluetooth-устройствам с помощью веб-API Bluetooth

* AskWebBluetooth (3) = Разрешить сайтам запрашивать у пользователя доступ к ближайшему устройству Bluetooth

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultWebBluetoothGuardSetting
  - Название GP: Контроль использования веб-API Bluetooth
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultWebBluetoothGuardSetting
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultWebBluetoothGuardSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultWebUsbGuardSetting

  #### Контроль использования API WebUSB

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настройте, могут ли веб-сайты получать доступ к подключенным USB-устройствам. Вы можете полностью блокировать доступ или запрашивать пользователя каждый раз, когда веб-сайт хочет получить доступ к подключенным USB-устройствам.

Вы можете переопределить эту политику для определенных шаблонов URL, используя политики [WebUsbAskForUrls](#webusbaskforurls) и [WebUsbBlockedForUrls](#webusbblockedforurls).

Если вы не настроите эту политику, сайты могут спросить пользователей, могут ли они получить доступ к подключенным USB-устройствам («AskWebUsb») по умолчанию, и пользователи могут изменить этот параметр.

Сопоставление параметров политики:

* BlockWebUsb (2) = Не разрешать сайтам запрашивать доступ к USB-устройствам через API WebUSB

* AskWebUsb (3) = разрешить сайтам запрашивать у пользователя доступ к подключенному USB-устройству

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultWebUsbGuardSetting
  - Имя GP: Контроль использования API WebUSB
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultWebUsbGuardSetting
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: DefaultWebUsbGuardSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### FileSystemReadAskForUrls

  #### Разрешить доступ на чтение через API файловой системы на этих сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  Настройка этой политики позволяет вам перечислять шаблоны URL-адресов, указывающие, какие сайты могут запрашивать у пользователей доступ на чтение файлов или каталогов в файловой системе главной ОС посредством API файловой системы.

В случае отсутствия настройки этой политики ко всем сайтам применяется политика [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting), если она задана. В противном случае применяются личные параметры пользователей.

Шаблоны URL-адресов не могут конфликтовать с [FileSystemReadBlockedForUrls](#filesystemreadblockedforurls). Никакая политика не получает приоритет, если URL-адрес соответствует обеим политикам.

Подробные сведения о шаблонах допустимых URL-адресов см. на странице https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: FileSystemReadAskForUrls
  - Имя групповой политики: Разрешить доступ на чтение через API файловой системы на этих сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Политики\Microsoft\Edge\FileSystemReadAskForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\2 = "[*.]example.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: FileSystemReadAskForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### FileSystemReadBlockedForUrls

  #### Блокировать доступ на чтение через API файловой системы на этих сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  Если настроить эту политику, вы сможете перечислять шаблоны URL-адресов, указывающие, какие сайты не могут запрашивать у пользователей доступ на чтение файлов или каталогов в файловой системе главной ОС посредством API файловой системы.

Если не настроить эту политику, ко всем сайтам применяется политика [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) (если она задана). В противном случае применяются личные параметры пользователей.

Шаблоны URL-адресов не могут конфликтовать с [FileSystemReadAskForUrls](#filesystemreadaskforurls). Никакая политика не получает приоритет, если URL-адрес соответствует обеим политикам.

Подробные сведения о шаблонах допустимых URL-адресов см. на странице https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: FileSystemReadBlockedForUrls
  - Имя групповой политики: Блокировать доступ на чтение через API файловой системы на этих сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Политики\Microsoft\Edge\FileSystemReadBlockedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\2 = "[*.]example.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: FileSystemReadBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### FileSystemWriteAskForUrls

  #### Разрешить доступ на запись к файлам и каталогам на этих сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  Если настроить эту политику, вы сможете перечислять шаблоны URL-адресов, указывающие, какие сайты могут запрашивать у пользователей доступ на запись к файлам или каталогам в файловой системе главной ОС.

Если не настроить эту политику, ко всем сайтам применяется политика [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) (если она задана). В противном случае применяются личные параметры пользователей.

Шаблоны URL-адресов не могут конфликтовать с [FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls). Никакая политика не получает приоритет, если URL-адрес соответствует обеим политикам.

Подробные сведения о шаблонах допустимых URL-адресов см. на странице https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: FileSystemWriteAskForUrls
  - Имя групповой политики: Разрешить доступ на запись к файлам и каталогам на этих сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Политики\Microsoft\Edge\FileSystemWriteAskForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\2 = "[*.]example.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: FileSystemWriteAskForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### FileSystemWriteBlockedForUrls

  #### Блокировать доступ на запись к файлам и каталогам на этих сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  Если настроить эту политику, вы сможете перечислять шаблоны URL-адресов, указывающие, какие сайты не могут запрашивать у пользователей доступ на запись к файлам или каталогам в файловой системе главной ОС.

Если не настроить эту политику, ко всем сайтам применяется политика [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) (если она задана). В противном случае применяются личные параметры пользователей.

Шаблоны URL-адресов не могут конфликтовать с [FileSystemWriteAskForUrls](#filesystemwriteaskforurls). Никакая политика не получает приоритет, если URL-адрес соответствует обеим политикам.

Подробные сведения о шаблонах допустимых URL-адресов см. на странице https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: FileSystemWriteBlockedForUrls
  - Имя групповой политики: Блокировать доступ на запись к файлам и каталогам на этих сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Политики\Microsoft\Edge\FileSystemWriteBlockedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\2 = "[*.]example.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: FileSystemWriteBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### ImagesAllowedForUrls

  #### Разрешить изображения на этих сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определите список сайтов на основе шаблонов URL, которые могут отображать изображения.

Если вы не настроите эту политику, глобальное значение по умолчанию будет использоваться для всех сайтов либо из политики [DefaultImagesSetting](#defaultimagessetting) (если установлена), либо из личной конфигурации пользователя.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ImagesAllowedForUrls
  - Название GP: Разрешить изображения на этих сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\ImagesAllowedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ImagesAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### ImagesBlockedForUrls

  #### Блокировать изображения на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определите список сайтов на основе шаблонов URL, которым не разрешено отображать изображения.

Если вы не настроите эту политику, глобальное значение по умолчанию из политики [DefaultImagesSetting](#defaultimagessetting) (если установлено) или личная конфигурация пользователя используется для всех сайтов.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ImagesBlockedForUrls
  - Название GP: Блокировка изображений на определенных сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\ImagesBlockedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ImagesBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### InsecureContentAllowedForUrls

  #### Разрешить небезопасный контент на указанных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 80 или позже

  #### Описание

  Создайте список шаблонов URL-адресов, чтобы указать сайты, которые могут отображать небезопасное смешанное содержимое (то есть содержимое HTTP на сайтах HTTPS).

Если вы не настроите эту политику, блокируемый смешанный контент будет заблокирован, а необязательно блокируемый смешанный контент будет обновлен. Однако пользователям будет разрешено устанавливать исключения, чтобы разрешить небезопасный смешанный контент для определенных сайтов.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: InsecureContentAllowedForUrls
  - Имя GP: разрешить небезопасный контент на указанных сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\InsecureContentAllowedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = "[*.]example.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: InsecureContentAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### InsecureContentBlockedForUrls

  #### Блокировать небезопасный контент на указанных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 80 или позже

  #### Описание

  Создайте список шаблонов URL-адресов, чтобы указать сайты, которым не разрешено отображать блокируемое (то есть активное) смешанное содержимое (то есть содержимое HTTP на сайтах HTTPS) и для которых необязательно блокируемые обновления смешанного содержимого будут отключены.

Если вы не настроите эту политику, блокируемый смешанный контент будет заблокирован, а необязательно блокируемый смешанный контент будет обновлен. Однако пользователям будет разрешено устанавливать исключения, чтобы разрешить небезопасный смешанный контент для определенных сайтов.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: InsecureContentBlockedForUrls
  - Имя GP: блокировать небезопасный контент на указанных сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\InsecureContentBlockedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = "[*.]example.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: InsecureContentBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### JavaScriptAllowedForUrls

  #### Разрешить JavaScript на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определите список сайтов на основе шаблонов URL, которым разрешено запускать JavaScript.

Если вы не настроите эту политику, глобальное значение по умолчанию из политики [DefaultJavaScriptSetting](#defaultjavascriptsetting) (если установлено) или личная конфигурация пользователя используется для всех сайтов.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: JavaScriptAllowedForUrls
  - Название GP: разрешить JavaScript на определенных сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\JavaScriptAllowedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: JavaScriptAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### JavaScriptBlockedForUrls

  #### Блокировать JavaScript на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определите список сайтов на основе шаблонов URL, для которых не разрешен запуск JavaScript.

Если вы не настроите эту политику, глобальное значение по умолчанию из политики [DefaultJavaScriptSetting](#defaultjavascriptsetting) (если установлено) или личная конфигурация пользователя используется для всех сайтов.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: JavaScriptBlockedForUrls
  - Название GP: блокировать JavaScript на определенных сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: JavaScriptBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### LegacySameSiteCookieBehaviorEnabled

  #### Включить стандартную настройку поведения файлов cookie SameSite по умолчанию

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 80 или позже

  #### Описание

  Позволяет вам вернуть все файлы cookie в прежнее поведение SameSite. При восстановлении до устаревшего поведения файлы cookie, не задающие атрибут Самесите, будут рассматриваться так, как если бы они были "Самесите = None", и при этом пропускают сравнение схем при оценке того, что два сайта являются одним и тем же.

Если не задать эту политику, поведение Самесите, используемое по умолчанию для файлов cookie, будет зависеть от других источников конфигурации по умолчанию для Самесите, а также файлов Сookie, не-Самесите-обязательно-быть по умолчанию и функции схемы на одном сайте. Эти возможности также можно настроить с помощью флажка "пробная версия" или "один и тот же". флаги для одного и того же сайта, а также для файлов cookie без параметров "один-к-одному" или "схема одного сайта" в edge://flags.

Сопоставление параметров политики:

* DefaultToLegacySameSiteCookieBehavior (1) = возврат к устаревшему поведению SameSite для cookie-файлов на всех сайтах.

* DefaultToSameSiteByDefaultCookieBehavior (2) = Использовать поведение SameSite по умолчанию для cookie-файлов на всех сайтах

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: LegacySameSiteCookieBehaviorEnabled
  - Имя GP: включить стандартную настройку поведения файлов cookie SameSite по умолчанию
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: LegacySameSiteCookieBehaviorEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: LegacySameSiteCookieBehaviorEnabled
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### LegacySameSiteCookieBehaviorEnabledForDomainList

  #### Возврат к устаревшему поведению SameSite для файлов cookie на указанных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 80 или позже

  #### Описание

  Файлы cookie, установленные для доменов, соответствующих указанным шаблонам, вернутся к устаревшему поведению SameSite.

При восстановлении до устаревшего поведения файлы cookie, не задающие атрибут Самесите, будут рассматриваться так, как если бы они были "Самесите = None", и при этом пропускают сравнение схем при оценке того, что два сайта являются одним и тем же.

Если вы не установите эту политику, будет использоваться глобальное значение по умолчанию. Глобальное значение по умолчанию также будет использоваться для файлов cookie в доменах, на которые не распространяются указанные вами шаблоны.

Глобальное значение по умолчанию можно настроить с помощью политики [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled). Если [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) не установлено, глобальное значение по умолчанию возвращается к другим источникам конфигурации.

Обратите внимание, что шаблоны, перечисленные в этой политике, рассматриваются как домены, а не как URL-адреса, поэтому не следует указывать схему или порт.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Имя GP: возврат к устаревшему поведению SameSite для файлов cookie на указанных сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = "www.example.com"
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = "[*.]example.edu"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Пример значения:
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### NotificationsAllowedForUrls

  #### Разрешить уведомления на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет создать список шаблонов URL-адресов, чтобы указать сайты, которым разрешено отображать уведомления.

Если вы не настроите эту политику, для всех сайтов будет использоваться глобальное значение по умолчанию. Это значение по умолчанию берется из политики [DefaultNotificationsSetting](#defaultnotificationssetting) (если она настроена) или из персональной конфигурации пользователя. Подробные сведения о шаблонах допустимых URL-адресов см. [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NotificationsAllowedForUrls
  - Имя GP: разрешить уведомления на определенных сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательно): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\NotificationsAllowedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: NotificationsAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### NotificationsBlockedForUrls

  #### Блокировать уведомления на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет создать список шаблонов URL-адресов, чтобы указать сайты, которым запрещено отображать уведомления.

Если вы не настроите эту политику, для всех сайтов будет использоваться глобальное значение по умолчанию. Это значение по умолчанию берется из политики [DefaultNotificationsSetting](#defaultnotificationssetting) (если она настроена) или из персональной конфигурации пользователя. Подробные сведения о шаблонах допустимых URL-адресов см. [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NotificationsBlockedForUrls
  - Название GP: блокировать уведомления на определенных сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательно): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\NotificationsBlockedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: NotificationsBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### PluginsAllowedForUrls

  #### Разрешить подключаемый модуль Adobe Flash на определенных сайтах (устарело)

  
  >УСТАРЕЛО: эта политика устарела и не работает в версиях Microsoft Edge после 87.
  #### Поддерживаемые версии:

  - В Windows и macOS — версии c 77 по 87

  #### Описание

  Эта политика не работает, так как Flash больше не поддерживается Microsoft Edge.

Определите список сайтов на основе шаблонов URL-адресов, которые могут запускать подключаемый модуль Adobe Flash.

Если вы не настроите эту политику, глобальное значение по умолчанию из политики [DefaultPluginsSetting](#defaultpluginssetting) (если установлено) или личная конфигурация пользователя используется для всех сайтов.

Подробные сведения о допустимых шаблонах URL-адресов см. в статье [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Тем не менее, начиная с M85, шаблоны с подстановочными знаками "\*" и "[\*.]" в узле больше не поддерживаются для этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PluginsAllowedForUrls
  - Имя GP: разрешить подключаемый модуль Adobe Flash на определенных сайтах (устарело)
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\PluginsAllowedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = "http://contoso.edu:8080"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PluginsAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### PluginsBlockedForUrls

  #### Блокировать подключаемый модуль Adobe Flash на определенных сайтах (устарело)

  
  >УСТАРЕЛО: эта политика устарела и не работает в версиях Microsoft Edge после 87.
  #### Поддерживаемые версии:

  - В Windows и macOS — версии c 77 по 87

  #### Описание

  Эта политика не работает, так как Flash больше не поддерживается Microsoft Edge.

Определите список сайтов на основе шаблонов URL-адресов, которым запрещено запускать Adobe Flash.

Если вы не настроите эту политику, глобальное значение по умолчанию из политики [DefaultPluginsSetting](#defaultpluginssetting) (если установлено) или личная конфигурация пользователя используется для всех сайтов.

Подробные сведения о допустимых шаблонах URL-адресов см. в статье [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Тем не менее, начиная с M85, шаблоны с подстановочными знаками "\*" и "[\*.]" в узле больше не поддерживаются для этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PluginsBlockedForUrls
  - Имя GP: блокировать подключаемый модуль Adobe Flash на определенных сайтах (устарело)
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\PluginsBlockedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = "http://contoso.edu:8080"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PluginsBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### PopupsAllowedForUrls

  #### Разрешить всплывающие окна на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определите список сайтов на основе шаблонов URL, которые могут открывать всплывающие окна. * не является принятым значением для этой политики.

Если вы не настроите эту политику, глобальное значение по умолчанию из политики [DefaultPopupsSetting](#defaultpopupssetting) (если установлено) или личная конфигурация пользователя используется для всех сайтов.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PopupsAllowedForUrls
  - Имя GP: разрешить всплывающие окна на определенных сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\PopupsAllowedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PopupsAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### PopupsBlockedForUrls

  #### Блокировать всплывающие окна на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определите список сайтов, основанный на шаблонах URL, которым запрещено открывать всплывающие окна. * не является принятым значением для этой политики.

Если вы не настроите эту политику, глобальное значение по умолчанию из политики [DefaultPopupsSetting](#defaultpopupssetting) (если установлено) или личная конфигурация пользователя используется для всех сайтов.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PopupsBlockedForUrls
  - Имя GP: блокировать всплывающие окна на определенных сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\PopupsBlockedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: PopupsBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### RegisteredProtocolHandlers

  #### Регистрация обработчиков протокола

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настройте эту политику (recommended only) для регистрации списка обработчиков протоколов. Этот список будет объединен с теми, которые зарегистрированы пользователем, и они будут доступны для использования.

Регистрация обработчиков протокола

- Установите свойство протокола для схемы (например, «mailto»)
- Установите свойство URL для свойства URL-адреса приложения, которое обрабатывает схему, указанную в поле «протокол». Шаблон может содержать заполнитель «% s», который будет заменен на обработанный URL.

Пользователи не могут удалить обработчик протоколов, зарегистрированный в этой политике. Тем не менее они могут установить новый обработчик протокола по умолчанию для переопределения существующих обработчиков протоколов.

  #### Поддерживаемые функции:

  - Может быть обязательным: Нет
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Dictionary

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: RegisteredProtocolHandlers
  - Имя GP: Регистрация обработчиков протокола
  - Путь GP (обязательно): N / A
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Настройки контента
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательно): N/A
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: RegisteredProtocolHandlers
  - Тип значения: REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true, 
    "protocol": "mailto", 
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```

  ##### Компактный пример значения:

  ```
  SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [{"default": true, "protocol": "mailto", "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"}]
  ```
  

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: RegisteredProtocolHandlers
  - Пример значения:
``` xml
<key>RegisteredProtocolHandlers</key>
<array>
  <dict>
    <key>default</key>
    <true/>
    <key>protocol</key>
    <string>mailto</string>
    <key>url</key>
    <string>https://mail.contoso.com/mail/?extsrc=mailto&url=%s</string>
  </dict>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### SpotlightExperiencesAndRecommendationsEnabled

  #### Выберите, могут ли пользователи получать настроенные фоновые изображения и текст, предложения, уведомления
и советы для служб Майкрософт

  
  
  #### Поддерживаемые версии:

  - В Windows — версия 86 или более поздние

  #### Описание

  Выберите, могут ли пользователи получать настроенные фоновые изображения и текст, предложения, уведомления и советы для служб Майкрософт.

Если включить или не настроить этот параметр, функции выделения важного и рекомендации будут включены.

Если этот параметр отключен, функции выделения важного и рекомендации будут отключены.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: SpotlightExperiencesAndRecommendationsEnabled
  - Имя групповой политики: Выберите, могут ли пользователи получать настроенные фоновые изображения и текст, предложения, уведомления и советы для служб Майкрософт.
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: SpotlightExperiencesAndRecommendationsEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### WebUsbAllowDevicesForUrls

  #### Предоставить доступ к определенным сайтам для подключения к определенным USB-устройствам

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет установить список URL-адресов, в которых указывается, каким сайтам автоматически будет предоставлено разрешение на доступ к USB-устройству с указанным поставщиком и идентификаторами продуктов. Каждый элемент в списке должен содержать как устройства, так и URL-адреса, чтобы политика была действительной. Каждый элемент в устройствах может содержать идентификатор поставщика и поле идентификатора продукта. Любой опущенный идентификатор обрабатывается как подстановочный знак с одним исключением, и это исключение состоит в том, что идентификатор продукта не может быть указан без указания идентификатора поставщика. В противном случае политика не будет действительной и будет игнорироваться.

Модель разрешений USB использует URL запрашивающего сайта («запрашивающий URL») и URL сайта верхнего уровня («встраиваемый URL») для предоставления разрешения запрашивающему URL для доступа к устройству USB. Запрашивающий URL-адрес может отличаться от встраиваемого URL-адреса, когда запрашивающий сайт загружается в iframe. Следовательно, поле «urls» может содержать до двух строк URL, разделенных запятой, чтобы указать запрашивающий и внедряемый URL соответственно. Если указан только один URL-адрес, то доступ к соответствующим USB-устройствам будет предоставлен, когда URL-адрес запрашивающего сайта совпадает с этим URL-адресом, независимо от статуса встраивания. URL-адреса в «URL-адресах» должны быть действительными, в противном случае политика будет игнорироваться.

Если эта политика не задана, глобальное значение по умолчанию будет использоваться для всех сайтов либо из политики [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting), если она задана, либо из личной конфигурации пользователя в противном случае.

Шаблоны URL в этой политике не должны конфликтовать с шаблонами, настроенными через [WebUsbBlockedForUrls](#webusbblockedforurls). В случае конфликта эта политика будет иметь приоритет над [WebUsbBlockedForUrls](#webusbblockedforurls) и [WebUsbAskForUrls](#webusbaskforurls).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Dictionary

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WebUsbAllowDevicesForUrls
  - Имя GP: Предоставить доступ к определенным сайтам для подключения к определенным USB-устройствам.
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: WebUsbAllowDevicesForUrls
  - Тип значения: REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAllowDevicesForUrls = [
  {
    "devices": [
      {
        "product_id": 5678, 
        "vendor_id": 1234
      }
    ], 
    "urls": [
      "https://contoso.com", 
      "https://fabrikam.com"
    ]
  }
]
```

  ##### Компактный пример значения:

  ```
  SOFTWARE\Policies\Microsoft\Edge\WebUsbAllowDevicesForUrls = [{"devices": [{"product_id": 5678, "vendor_id": 1234}], "urls": ["https://contoso.com", "https://fabrikam.com"]}]
  ```
  

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: WebUsbAllowDevicesForUrls
  - Пример значения:
``` xml
<key>WebUsbAllowDevicesForUrls</key>
<array>
  <dict>
    <key>devices</key>
    <array>
      <dict>
        <key>product_id</key>
        <integer>5678</integer>
        <key>vendor_id</key>
        <integer>1234</integer>
      </dict>
    </array>
    <key>urls</key>
    <array>
      <string>https://contoso.com</string>
      <string>https://fabrikam.com</string>
    </array>
  </dict>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### WebUsbAskForUrls

  #### Разрешить WebUSB на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определите список сайтов на основе шаблонов URL, которые могут запрашивать у пользователя доступ к USB-устройству.

Если вы не настроите эту политику, глобальное значение по умолчанию из политики [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (если установлено) или личная конфигурация пользователя используется для всех сайтов.

Шаблоны URL, определенные в этой политике, не могут конфликтовать с шаблонами, настроенными в политике [WebUsbBlockedForUrls](#webusbblockedforurls) - вы не можете разрешить и заблокировать URL. Подробные сведения о шаблонах допустимых URL-адресов см. [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WebUsbAskForUrls
  - Имя GP: Разрешить WebUSB на определенных сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\WebUsbAskForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: WebUsbAskForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### WebUsbBlockedForUrls

  #### Блокировка WebUSB на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определите список сайтов на основе шаблонов URL, которые не могут попросить пользователя предоставить им доступ к USB-устройству.

Если вы не настроите эту политику, глобальное значение по умолчанию из политики [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (если установлено) или личная конфигурация пользователя используется для всех сайтов.

Шаблоны URL в этой политике не могут конфликтовать с шаблонами, настроенными в политике [WebUsbAskForUrls](#webusbaskforurls). Вы не можете одновременно разрешить и заблокировать URL.  Подробные сведения о шаблонах допустимых URL-адресов см. в[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WebUsbBlockedForUrls
  - Название GP: блокировать WebUSB на определенных сайтах
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\WebUsbBlockedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: WebUsbBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ## Политики поставщика поиска по умолчанию

  [В начало](#microsoft-edge---policies)

  ### DefaultSearchProviderEnabled

  #### Включить поисковую систему по умолчанию

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Включает возможность использовать поисковый сервис по умолчанию.

Если вы включите эту политику, пользователь сможет искать термин, вводя его в адресной строке (если он вводит не URL-адрес).

Вы можете указать поставщика поиска по умолчанию для использования, включив остальные политики поиска по умолчанию. Если они оставлены пустыми (не настроены) или настроены неправильно, пользователь может выбрать поставщика по умолчанию.

Если вы отключите эту политику, пользователь не сможет выполнять поиск из адресной строки.

Если вы включите или отключите эту политику, пользователи не смогут изменить или переопределить ее.

Если вы не настроите эту политику, включается поставщик поиска по умолчанию, и пользователь может выбрать поставщика поиска по умолчанию и задать список поставщиков поиска.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

Начиная с Microsoft Edge 84, эту политику можно установить в качестве рекомендуемой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultSearchProviderEnabled
  - Имя GP: включить поисковую систему по умолчанию
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Поставщик поиска по умолчанию
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge — Настройки по умолчанию (пользователи могут переопределить)/Поставщик поиска по умолчанию
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: DefaultSearchProviderEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultSearchProviderEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultSearchProviderEncodings

  #### Кодировки поставщика поиска по умолчанию

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Укажите кодировки символов, поддерживаемые поставщиком поиска. Кодировки - это имена кодовых страниц, такие как UTF-8, GB2312 и ISO-8859-1. Они судят в указанном порядке.

Эта политика не является обязательной. Если не настроено, используется значение по умолчанию, UTF-8.

Эта политика применяется только в том случае, если включены политики [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

Начиная с Microsoft Edge 84, эту политику можно установить в качестве рекомендуемой политики. Если пользователь уже установил используемую по умолчанию службу поиска, то настроенная этой рекомендованной политикой служба поиска по умолчанию не будет добавлена в предлагаемый пользователю список служб поиска. Если нужны именно такие действия, используйте политику [ManagedSearchEngines](#managedsearchengines).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultSearchProviderEncodings
  - Имя GP: кодировки поставщика поиска по умолчанию
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Поставщик поиска по умолчанию
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge — Настройки по умолчанию (пользователи могут переопределить)/Поставщик поиска по умолчанию
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\DefaultSearchProviderEncodings
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Политики\Microsoft\Edge\Рекомендованное\RestoreOnStartupURLs
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = "UTF-8"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = "UTF-16"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = "GB2312"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = "ISO-8859-1"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultSearchProviderEncodings
  - Пример значения:
``` xml
<array>
  <string>UTF-8</string>
  <string>UTF-16</string>
  <string>GB2312</string>
  <string>ISO-8859-1</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultSearchProviderImageURL

  #### Определяет функцию поиска по изображению для поставщика поиска по умолчанию

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Указывает URL-адрес поисковой системы, используемой для поиска изображений. Поисковые запросы отправляются методом GET.

Эта политика не является обязательной. Если вы не настроите его, поиск изображений будет недоступен.

Укажите URL-адрес поиска изображений Bing как: '{bing:baseURL}images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights'.

Укажите URL-адрес поиска изображений Google как: '{google:baseURL}searchbyimage/upload'.

См. Политику [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams) для завершения настройки поиска изображений.

Эта политика применяется только в том случае, если включены политики [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

Начиная с Microsoft Edge 84, эту политику можно установить в качестве рекомендуемой политики. Если пользователь уже установил используемую по умолчанию службу поиска, то настроенная этой рекомендованной политикой служба поиска по умолчанию не будет добавлена в предлагаемый пользователю список служб поиска. Если нужны именно такие действия, используйте политику [ManagedSearchEngines](#managedsearchengines).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultSearchProviderImageURL
  - Имя GP: Определяет функцию поиска по картинке для поисковой системы по умолчанию.
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Поставщик поиска по умолчанию
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge — Настройки по умолчанию (пользователи могут переопределить)/Поставщик поиска по умолчанию
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: DefaultSearchProviderImageURL
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"https://search.contoso.com/searchbyimage/upload"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultSearchProviderImageURL
  - Пример значения:
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultSearchProviderImageURLPostParams

  #### Параметры для изображения URL, который использует POST

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Если вы включите эту политику, в ней будут указаны параметры, используемые при поиске изображения с использованием POST. Политика состоит из разделенных запятыми пар имя / значение. Если значение является параметром шаблона, как {imageThumbnail} в предыдущем примере, оно заменяется данными эскиза реального изображения. Эта политика применяется только в том случае, если включены политики [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

Укажите параметры публикации URL для поиска изображений в Bing как: 'imageBin={google:imageThumbnailBase64}'.

Укажите параметры публикации URL для поиска картинок Google как: 'encoded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}'.

Если эта политика не задана, запросы поиска изображения отправляются с использованием метода GET.

Начиная с Microsoft Edge 84, эту политику можно установить в качестве рекомендуемой политики. Если пользователь уже установил используемую по умолчанию службу поиска, то настроенная этой рекомендованной политикой служба поиска по умолчанию не будет добавлена в предлагаемый пользователю список служб поиска. Если нужны именно такие действия, используйте политику [ManagedSearchEngines](#managedsearchengines).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultSearchProviderImageURLPostParams
  - Имя GP: параметры для URL изображения, который использует POST
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Поставщик поиска по умолчанию
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge — Настройки по умолчанию (пользователи могут переопределить)/Поставщик поиска по умолчанию
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: DefaultSearchProviderImageURLPostParams
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"content={imageThumbnail},url={imageURL},sbisrc={SearchSource}"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultSearchProviderImageURLPostParams
  - Пример значения:
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultSearchProviderKeyword

  #### Ключевое слово поставщика поиска по умолчанию

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определяет ключевое слово, которое является ярлыком, используемым в адресной строке для запуска поиска этого провайдера.

Эта политика не является обязательной. Если вы не настроите его, ни одно ключевое слово не активирует поисковую систему.

Эта политика применяется только в том случае, если включены политики [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

Начиная с Microsoft Edge 84, эту политику можно установить в качестве рекомендуемой политики. Если пользователь уже установил используемую по умолчанию службу поиска, то настроенная этой рекомендованной политикой служба поиска по умолчанию не будет добавлена в предлагаемый пользователю список служб поиска. Если нужны именно такие действия, используйте политику [ManagedSearchEngines](#managedsearchengines).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultSearchProviderKeyword
  - Название GP: ключевое слово поставщика поиска по умолчанию
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Поставщик поиска по умолчанию
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge — Настройки по умолчанию (пользователи могут переопределить)/Поставщик поиска по умолчанию
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: DefaultSearchProviderKeyword
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"mis"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultSearchProviderKeyword
  - Пример значения:
``` xml
<string>mis</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultSearchProviderName

  #### Имя поставщика поиска по умолчанию

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Указывает имя поискового поставщика по умолчанию.

Если вы включите эту политику, вы зададите имя поставщика поиска по умолчанию.

Если вы не включите эту политику или оставите ее пустой, используется имя хоста, указанное в URL-адресе поиска.

«DefaultSearchProviderName» должно быть установлено в утвержденный организацией зашифрованный поставщик поиска, который соответствует зашифрованному поставщику поиска, установленному в DTBC-0008. Эта политика применяется только в том случае, если включены политики [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

Начиная с Microsoft Edge 84, эту политику можно установить в качестве рекомендуемой политики. Если пользователь уже установил используемую по умолчанию службу поиска, то настроенная этой рекомендованной политикой служба поиска по умолчанию не будет добавлена в предлагаемый пользователю список служб поиска. Если нужны именно такие действия, используйте политику [ManagedSearchEngines](#managedsearchengines).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultSearchProviderName
  - Имя GP: имя поискового поставщика по умолчанию
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Поставщик поиска по умолчанию
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge — Настройки по умолчанию (пользователи могут переопределить)/Поставщик поиска по умолчанию
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: DefaultSearchProviderName
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"My Intranet Search"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultSearchProviderName
  - Пример значения:
``` xml
<string>My Intranet Search</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultSearchProviderSearchURL

  #### URL поиска по умолчанию для поисковой системы

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Указывает URL-адрес поисковой системы, используемой для поиска по умолчанию. URL содержит строку '{searchTerms}', которая заменяется во время запроса терминами, которые ищет пользователь.

Укажите поисковый URL Bing как:

'{bing:baseURL}search?q={searchTerms}'.

Укажите поисковый URL Google как: '{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}'.

Эта политика требуется при включении политики [DefaultSearchProviderEnabled](#defaultsearchproviderenabled); если вы не включите последнюю политику, эта политика игнорируется.

Начиная с Microsoft Edge 84, эту политику можно установить в качестве рекомендуемой политики. Если пользователь уже установил используемую по умолчанию службу поиска, то настроенная этой рекомендованной политикой служба поиска по умолчанию не будет добавлена в предлагаемый пользователю список служб поиска. Если нужны именно такие действия, используйте политику [ManagedSearchEngines](#managedsearchengines).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultSearchProviderSearchURL
  - Название GP: поисковый URL по умолчанию
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Поставщик поиска по умолчанию
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge — Настройки по умолчанию (пользователи могут переопределить)/Поставщик поиска по умолчанию
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: DefaultSearchProviderSearchURL
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"https://search.contoso.com/search?q={searchTerms}"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultSearchProviderSearchURL
  - Пример значения:
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultSearchProviderSuggestURL

  #### URL поставщика поиска по умолчанию для предложений

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определяет URL для поисковой системы, используемой для предоставления поисковых предложений. URL содержит строку '{searchTerms}', которая во время запроса заменяется текстом, введенным пользователем до сих пор.

Эта политика не является обязательной. Если вы не настроите его, пользователи не будут видеть предложения поиска; они будут видеть предложения из своей истории просмотров и избранного.

Предлагаемый Bing URL может быть указан как:

'{bing:baseURL}qbox?query={searchTerms}'.

Предлагаемый Google URL может быть указан как: '{google:baseURL}complete/search?output=chrome&q={searchTerms}'.

Эта политика применяется только в том случае, если включены политики [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

Начиная с Microsoft Edge 84, эту политику можно установить в качестве рекомендуемой политики. Если пользователь уже установил используемую по умолчанию службу поиска, то настроенная этой рекомендованной политикой служба поиска по умолчанию не будет добавлена в предлагаемый пользователю список служб поиска. Если нужны именно такие действия, используйте политику [ManagedSearchEngines](#managedsearchengines).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultSearchProviderSuggestURL
  - Имя GP: URL поставщика поиска по умолчанию для предложений
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Поставщик поиска по умолчанию
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge — Настройки по умолчанию (пользователи могут переопределить)/Поставщик поиска по умолчанию
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: DefaultSearchProviderSuggestURL
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"https://search.contoso.com/suggest?q={searchTerms}"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultSearchProviderSuggestURL
  - Пример значения:
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### NewTabPageSearchBox

  #### Настройка интерфейса поля поиска на новой вкладке

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS — версия 85 или более поздние

  #### Описание

  Вы можете настроить поле поиска на новой вкладке так, чтобы использовался вариант "Поле поиска (рекомендуется)" или "Адресная строка". Эта политика работает только в том случае, если вы зададите отличную от Bing поисковую систему путем использования следующих двух политик: [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

 Если вы отключите или не настроите эту политику и:

- если поисковой системой, по умолчанию заданной для адресной строки, является Bing, то на новой вкладке будет использоваться поле поиска.
- если поисковой системой, по умолчанию заданной для адресной строки, является не Bing, то пользователям будет предоставляться дополнительный вариант для поиска на новой вкладке ("Адресная строка").


Если вы включите эту политику и настроите ее следующим образом:

- "Поле поиска (рекомендуется)" ('bing'), то на новой вкладке будет использоваться поле поиска.
- "Адресная строка" ('redirect'), то на новой вкладке будет использоваться для поиска адресная строка.

Сопоставление параметров политики:

* bing (bing) = поле поиска (рекомендуется)

* redirect (redirect) = Адресная строка

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NewTabPageSearchBox
  - Имя GP: Настройка интерфейса поля поиска на новой вкладке
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Поставщик поиска по умолчанию
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge — Настройки по умолчанию (пользователи могут переопределить)/Поставщик поиска по умолчанию
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: NewTabPageSearchBox
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"bing"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: NewTabPageSearchBox
  - Пример значения:
``` xml
<string>bing</string>
```
  

  [В начало](#microsoft-edge---policies)

  ## Политики расширений

  [В начало](#microsoft-edge---policies)

  ### BlockExternalExtensions

  #### Блокировка установки внешних расширений

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 88 или позже

  #### Описание

  Управление установкой внешних расширений.

Если этот параметр включен, внешние расширения будут заблокированы для установки.

Если этот параметр отключен или не задан, внешние расширения разрешено устанавливать.

Внешние расширения и их установка описаны на странице https://docs.microsoft.com/microsoft-edge/extensions-chromium/developer-guide/alternate-distribution-options.


  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: BlockExternalExtensions
  - Имя GP: Блокировка установки внешних расширений
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Расширения
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: BlockExternalExtensions
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: BlockExternalExtensions
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ExtensionAllowedTypes

  #### Настройте разрешенные типы расширений

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настройка политики определяет, какие приложения и расширения можно установить в Microsoft Edge, с какими узлами они могут взаимодействовать, а также ограничивает доступ к среде выполнения.

Если вы не настроите эту политику, для доступных типов расширений и приложений будут отсутствовать какие-либо ограничения.

Расширения и приложения, тип которых не указан в списке, не будут установлены. В качестве каждого значения должна применяться одна из следующих строк:

* "extension"

* "theme"

* "user_script"

* "hosted_app"

Дополнительные сведения об этих типах см. в документации по расширениям Microsoft Edge.

Примечание. Эта политика также влияет на расширения и приложения, принудительно устанавливаемые с помощью политики [ExtensionInstallForcelist](#extensioninstallforcelist).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ExtensionAllowedTypes
  - Имя GP: настройка разрешенных типов расширений
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Расширения
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\ExtensionAllowedTypes
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = "hosted_app"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: ExtensionAllowedTypes
  - Пример значения:
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### ExtensionInstallAllowlist

  #### Разрешить установку определенных расширений

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  При настройке этой политики указываются расширения, которые не регулируются списком блокировки.

Значение "*" в списке блокировки означает, что все расширения блокируются и пользователи могут устанавливать только расширения, указанные в списке разрешений.

По умолчанию все расширения разрешены. Но если вы запретили расширения в политике, вы можете использовать список разрешенных расширений для изменения этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ExtensionInstallAllowlist
  - Имя GP: разрешить установку определенных расширений
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Расширения
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\ExtensionInstallAllowlist
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = "extension_id2"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ExtensionInstallAllowlist
  - Пример значения:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### ExtensionInstallBlocklist

  #### Определить, какие расширения нельзя установить

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет указать, какие расширения пользователи НЕ МОГУТ установить. Установленные расширения будут отключены, если они заблокированы, без возможности их включить. После удаления отключенного расширения из списка блокировки оно автоматически будет включено повторно.

Значение списка заблокированных расширений "\*" означает, что все расширения блокируются, если они явно не указаны в списке.

Если эта политика не настроена, пользователь может установить любое расширение в Microsoft Edge.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ExtensionInstallBlocklist
  - Имя GP: укажите, какие расширения не могут быть установлены
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Расширения
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\ExtensionInstallBlocklist
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = "extension_id2"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: ExtensionInstallBlocklist
  - Пример значения:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### ExtensionInstallForcelist

  #### Определить, какие расширения устанавливаются в автоматическом режиме

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настройте эту политику, чтобы указать список приложений и расширений, которые устанавливаются без вмешательства пользователя. Пользователи не могут удалить или отключить этот параметр. Разрешения предоставляются неявно, в том числе для API расширений enterprise.deviceAttributes и enterprise.platformKeys. Примечание. Эти 2 API недоступны для приложений и расширений, которые не установлены принудительно.

Если вы не настроите эту политику, никакие приложения и расширения не будут устанавливаться автоматически, а пользователи смогут удалить приложение в Microsoft Edge.

Эта политика заменяет политику [ExtensionInstallBlocklist](#extensioninstallblocklist). Если принудительно установленное приложение или расширение удаляется из этого списка, Microsoft Edge автоматически удалит его.

В экземплярах Microsoft Windows приложения и расширения, полученные не с веб-сайта надстроек Microsoft Edge, можно принудительно устанавливать только в том случае, если экземпляр присоединен к домену Microsoft Active Directory и используется ОС Windows 10 Pro.

В экземплярах macOS приложения и расширения, полученные не с веб-сайта надстроек Microsoft Edge, можно принудительно устанавливать только в том случае, если экземпляр управляется с помощью MDM или присоединен к домену посредством MCX.

Исходный код любого расширения может изменяться пользователями с помощью средств разработчика, что может сделать расширение неработоспособным. Если вы опасаетесь этой проблемы, настройте политику DeveloperToolsDisabled.

Каждый элемент списка политики является строкой, содержащей идентификатор расширения и (необязательно) URL-адрес "обновления", отделенный точкой с запятой (;). Идентификатор расширения — это 32-буквенная строка, доступная, к примеру, на странице edge://extensions в режиме разработчика. URL-адрес "обновления" (если он задан) должен указывать на XML-документ манифеста обновления ( [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043) ). По умолчанию используется URL-адрес обновления веб-сайта надстроек Microsoft Edge. URL-адрес "обновления", заданный в этой политике, используется только для начальной установки; последующие обновления расширения используют URL-адрес обновления из манифеста расширения.

Примечание. Эта политика не применяется к режиму InPrivate. Ознакомьтесь с размещением расширений (https://docs.microsoft.com/microsoft-edge/extensions-chromium/enterprise/hosting-and-updating).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ExtensionInstallForcelist
  - Имя GP: Контроль над тем, какие расширения устанавливаются без вывода сообщений
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Расширения
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\ExtensionInstallForcelist
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = "gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = "abcdefghijklmnopabcdefghijklmnop"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: ExtensionInstallForcelist
  - Пример значения:
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### ExtensionInstallSources

  #### Настроить расширение и исходные тексты для установки пользовательских скриптов

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определите URL-адреса, которые могут устанавливать расширения и темы.

Определите URL-адреса, которые могут устанавливать расширения и темы непосредственно без перетаскивания пакетов на страницу edge://extensions.

Каждый элемент в этом списке является шаблоном соответствия стилю расширения (см. [https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039)). Пользователи могут легко устанавливать элементы с любого URL-адреса, соответствующего элементу в этом списке. Этим шаблонам должно быть разрешено как местоположение файла *.crx, так и страница, с которой начинается загрузка (другими словами, реферер). Не размещайте файлы в расположениях, требующих проверки подлинности.

Политика [ExtensionInstallBlocklist](#extensioninstallblocklist) имеет приоритет над этой политикой. Любые расширения, которые есть в списке заблокированных, не будут установлены, даже если они получены с сайта в этом списке.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ExtensionInstallSources
  - Имя GP: настройка расширения и источников установки пользовательских скриптов
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Расширения
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\ExtensionInstallSources
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = "https://corp.contoso.com/*"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ExtensionInstallSources
  - Пример значения:
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### ExtensionSettings

  #### Настройка параметров управления расширениями

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Путем настройки этой политики контролируются параметры управления расширениями для Microsoft Edge, включая любые расширения, управляемые существующими соответствующими политиками. Эта политика заменяет все устаревшие политики, которые могли быть настроены.

Эта политика сопоставляет идентификатор расширения или URL-адрес обновления только с определенным параметром. Для специального ИД "*" можно настроить конфигурацию по умолчанию, применяемую ко всем расширениям без настраиваемой конфигурации в этой политике. С помощью URL-адреса обновления конфигурация применяется к расширениям с точным URL-адресом обновления, указанным в манифесте расширения ( [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043) ).

Чтобы заблокировать расширения из определенного магазина стороннего производителя, необходимо заблокировать только update_url для этого магазина. Например, если вы хотите заблокировать расширения из веб-магазина Chrome, можно использовать следующий JSON.

{"update_url: https://clients2.google.com/service/update2/crx ":{"installation_mode":"blocked"}}

Обратите внимание, что вы по-прежнему можете использовать [ExtensionInstallForcelist](#extensioninstallforcelist) и [ExtensionInstallAllowlist,](#extensioninstallallowlist) чтобы разрешить или принудительно установить определенные расширения, даже если хранилище заблокировано с помощью JSON в предыдущем примере.

Примечание. Для экземпляров Windows, не присоединенных к домену Microsoft Active Directory, принудительная установка ограничена приложениями и расширениями, перечисленными на веб-сайте надстроек Microsoft Edge.


  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Dictionary

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ExtensionSettings
  - Имя GP: Настройка параметров управления расширениями
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Расширения
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ExtensionSettings
  - Тип значения: REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings = {
  "*": {
    "allowed_types": [
      "hosted_app"
    ], 
    "blocked_install_message": "Custom error message.", 
    "blocked_permissions": [
      "downloads", 
      "bookmarks"
    ], 
    "install_sources": [
      "https://company-intranet/apps"
    ], 
    "installation_mode": "blocked", 
    "runtime_allowed_hosts": [
      "*://good.contoso.com"
    ], 
    "runtime_blocked_hosts": [
      "*://*.contoso.com"
    ]
  }, 
  "abcdefghijklmnopabcdefghijklmnop": {
    "blocked_permissions": [
      "history"
    ], 
    "installation_mode": "allowed", 
    "minimum_version_required": "1.0.1"
  }, 
  "bcdefghijklmnopabcdefghijklmnopa": {
    "allowed_permissions": [
      "downloads"
    ], 
    "installation_mode": "force_installed", 
    "runtime_allowed_hosts": [
      "*://good.contoso.com"
    ], 
    "runtime_blocked_hosts": [
      "*://*.contoso.com"
    ], 
    "update_url": "https://contoso.com/update_url"
  }, 
  "cdefghijklmnopabcdefghijklmnopab": {
    "blocked_install_message": "Custom error message.", 
    "installation_mode": "blocked"
  }, 
  "defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd": {
    "blocked_install_message": "Custom error message.", 
    "installation_mode": "blocked"
  }, 
  "fghijklmnopabcdefghijklmnopabcde": {
    "blocked_install_message": "Custom removal message.", 
    "installation_mode": "removed"
  }, 
  "update_url:https://www.contoso.com/update.xml": {
    "allowed_permissions": [
      "downloads"
    ], 
    "blocked_permissions": [
      "wallpaper"
    ], 
    "installation_mode": "allowed"
  }
}
```

  ##### Компактный пример значения:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings = {"*": {"allowed_types": ["hosted_app"], "blocked_install_message": "Custom error message.", "blocked_permissions": ["downloads", "bookmarks"], "install_sources": ["https://company-intranet/apps"], "installation_mode": "blocked", "runtime_allowed_hosts": ["*://good.contoso.com"], "runtime_blocked_hosts": ["*://*.contoso.com"]}, "abcdefghijklmnopabcdefghijklmnop": {"blocked_permissions": ["history"], "installation_mode": "allowed", "minimum_version_required": "1.0.1"}, "bcdefghijklmnopabcdefghijklmnopa": {"allowed_permissions": ["downloads"], "installation_mode": "force_installed", "runtime_allowed_hosts": ["*://good.contoso.com"], "runtime_blocked_hosts": ["*://*.contoso.com"], "update_url": "https://contoso.com/update_url"}, "cdefghijklmnopabcdefghijklmnopab": {"blocked_install_message": "Custom error message.", "installation_mode": "blocked"}, "defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd": {"blocked_install_message": "Custom error message.", "installation_mode": "blocked"}, "fghijklmnopabcdefghijklmnopabcde": {"blocked_install_message": "Custom removal message.", "installation_mode": "removed"}, "update_url:https://www.contoso.com/update.xml": {"allowed_permissions": ["downloads"], "blocked_permissions": ["wallpaper"], "installation_mode": "allowed"}}
  ```
  

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: ExtensionSettings
  - Пример значения:
``` xml
<key>ExtensionSettings</key>
<dict>
  <key>*</key>
  <dict>
    <key>allowed_types</key>
    <array>
      <string>hosted_app</string>
    </array>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>blocked_permissions</key>
    <array>
      <string>downloads</string>
      <string>bookmarks</string>
    </array>
    <key>install_sources</key>
    <array>
      <string>https://company-intranet/apps</string>
    </array>
    <key>installation_mode</key>
    <string>blocked</string>
    <key>runtime_allowed_hosts</key>
    <array>
      <string>*://good.contoso.com</string>
    </array>
    <key>runtime_blocked_hosts</key>
    <array>
      <string>*://*.contoso.com</string>
    </array>
  </dict>
  <key>abcdefghijklmnopabcdefghijklmnop</key>
  <dict>
    <key>blocked_permissions</key>
    <array>
      <string>history</string>
    </array>
    <key>installation_mode</key>
    <string>allowed</string>
    <key>minimum_version_required</key>
    <string>1.0.1</string>
  </dict>
  <key>bcdefghijklmnopabcdefghijklmnopa</key>
  <dict>
    <key>allowed_permissions</key>
    <array>
      <string>downloads</string>
    </array>
    <key>installation_mode</key>
    <string>force_installed</string>
    <key>runtime_allowed_hosts</key>
    <array>
      <string>*://good.contoso.com</string>
    </array>
    <key>runtime_blocked_hosts</key>
    <array>
      <string>*://*.contoso.com</string>
    </array>
    <key>update_url</key>
    <string>https://contoso.com/update_url</string>
  </dict>
  <key>cdefghijklmnopabcdefghijklmnopab</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>installation_mode</key>
    <string>blocked</string>
  </dict>
  <key>defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>installation_mode</key>
    <string>blocked</string>
  </dict>
  <key>fghijklmnopabcdefghijklmnopabcde</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom removal message.</string>
    <key>installation_mode</key>
    <string>removed</string>
  </dict>
  <key>update_url:https://www.contoso.com/update.xml</key>
  <dict>
    <key>allowed_permissions</key>
    <array>
      <string>downloads</string>
    </array>
    <key>blocked_permissions</key>
    <array>
      <string>wallpaper</string>
    </array>
    <key>installation_mode</key>
    <string>allowed</string>
  </dict>
</dict>
```
  

  [В начало](#microsoft-edge---policies)

  ## Политики проверки подлинности HTTP

  [В начало](#microsoft-edge---policies)

  ### AllowCrossOriginAuthPrompt

  #### Разрешение запросов на проверку подлинности в нескольких источниках

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определяет, могут ли на странице выводится запрос на проверку подлинности сторонних изображений.

Как правило, это отключено в качестве защиты от фишинга. Если эта политика не настроена, это означает, что она отключена, а сторонние изображения не могут выводить запрос на проверку подлинности.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AllowCrossOriginAuthPrompt
  - Имя GP: Разрешение запросов на проверку подлинности в нескольких источниках
  - Путь к GP (обязательно): административные шаблоны / Microsoft Edge / HTTP-аутентификация
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AllowCrossOriginAuthPrompt
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AllowCrossOriginAuthPrompt
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### AuthNegotiateDelegateAllowlist

  #### Указывает список серверов, которым Microsoft Edge может делегировать учетные данные пользователя

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настройте список серверов, которым Microsoft Edge может делегировать.

Разделите несколько имен серверов запятыми. Подстановочные знаки (*) разрешены.

Если вы не настроите эту политику, Microsoft Edge не будет делегировать учетные данные пользователя, даже если сервер обнаружен как интрасеть.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AuthNegotiateDelegateAllowlist
  - Имя GP: указывает список серверов, которым Microsoft Edge может делегировать учетные данные пользователя.
  - Путь к GP (обязательно): административные шаблоны / Microsoft Edge / HTTP-аутентификация
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AuthNegotiateDelegateAllowlist
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"contoso.com"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AuthNegotiateDelegateAllowlist
  - Пример значения:
``` xml
<string>contoso.com</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### AuthSchemes

  #### Поддерживаемые схемы аутентификации

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Указывает, какие схемы аутентификации HTTP поддерживаются.

Вы можете настроить политику, используя следующие значения: 'basic', 'digest', 'ntlm', и 'negotiate'. Разделите несколько значений запятыми.

Если вы не настроите эту политику, будут использованы все четыре схемы.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AuthSchemes
  - Имя GP: Поддерживаемые схемы аутентификации
  - Путь к GP (обязательно): административные шаблоны / Microsoft Edge / HTTP-аутентификация
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AuthSchemes
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"basic,digest,ntlm,negotiate"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AuthSchemes
  - Пример значения:
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### AuthServerAllowlist

  #### Настроить список разрешенных серверов аутентификации

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Указывает, какие серверы включить для встроенной аутентификации. Интегрированная аутентификация включается только тогда, когда Microsoft Edge получает запрос аутентификации от прокси-сервера или с сервера в этом списке.

Разделите несколько имен серверов запятыми. Подстановочные знаки (*) разрешены.

Если вы не настроите эту политику, Microsoft Edge попытается определить, находится ли сервер в интрасети - только тогда он будет отвечать на запросы IWA. Если сервер находится в Интернете, запросы IWA от него игнорируются Microsoft Edge.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AuthServerAllowlist
  - Имя GP: Настройка списка разрешенных серверов аутентификации.
  - Путь к GP (обязательно): административные шаблоны / Microsoft Edge / HTTP-аутентификация
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AuthServerAllowlist
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"*contoso.com,contoso.com"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AuthServerAllowlist
  - Пример значения:
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### BasicAuthOverHttpEnabled

  #### Разрешить базовую проверку подлинности для HTTP

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 88 или позже

  #### Описание

  Если включить эту политику или оставить ее неустановленной, будут разрешены основные задачи проверки подлинности, полученные посредством небезопасной проверке подлинности HTTP.

Если вы отключили эту политику, небезопасные HTTP-запросы из схемы базовой проверки подлинности будут блокироваться, и будет разрешен только безопасный протокол HTTPS.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: BasicAuthOverHttpEnabled
  - Имя GP: Разрешить базовую проверку подлинности для HTTP
  - Путь к GP (обязательно): административные шаблоны / Microsoft Edge / HTTP-аутентификация
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): Н/Д
  - Имя значения: BasicAuthOverHttpEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: BasicAuthOverHttpEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### DisableAuthNegotiateCnameLookup

  #### Отключить поиск CNAME при согласовании проверки подлинности Kerberos

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определяет, основано ли созданное имя участника службы Kerberos на каноническом имени DNS (CNAME) или на введенном исходном имени.

Если вы включите эту политику, поиск CNAME будет пропущен, а имя сервера (в том виде, в котором оно введено) используется.

Если вы отключите эту политику или не настроите ее, используется каноническое имя сервера.  Это определяется с помощью поиска CNAME.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DisableAuthNegotiateCnameLookup
  - Имя GP: отключить поиск CNAME при согласовании аутентификации Kerberos
  - Путь к GP (обязательно): административные шаблоны / Microsoft Edge / HTTP-аутентификация
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DisableAuthNegotiateCnameLookup
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DisableAuthNegotiateCnameLookup
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### EnableAuthNegotiatePort

  #### Включить нестандартный порт в Kerberos SPN

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Указывает, должен ли созданный SPN Kerberos включать нестандартный порт.

Если вы включите эту политику, и пользователь включит в URL нестандартный порт (порт, отличный от 80 или 443), этот порт будет включен в созданное имя участника службы Kerberos.

Если вы не настроите или не отключите эту политику, сгенерированное имя Kerberos SPN не будет включать порт в любом случае.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: EnableAuthNegotiatePort
  - Имя GP: Включить нестандартный порт в Kerberos SPN.
  - Путь к GP (обязательно): административные шаблоны / Microsoft Edge / HTTP-аутентификация
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: EnableAuthNegotiatePort
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: EnableAuthNegotiatePort
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### NtlmV2Enabled

  #### Проверьте, включена ли аутентификация NTLMv2

  
  
  #### Поддерживаемые версии:

  - MacOS с 77 и более поздних версий

  #### Описание

  Управляет включением NTLMv2.

Все последние версии серверов Samba и Windows поддерживают NTLMv2. Вы должны отключить NTLMv2 только для решения проблем с обратной совместимостью, поскольку это снижает безопасность аутентификации.

Если вы не настроите эту политику, NTLMv2 включен по умолчанию.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: NtlmV2Enabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### WindowsHelloForHTTPAuthEnabled

  #### Функция Windows Hello для проверки подлинности HTTP включена

  
  
  #### Поддерживаемые версии:

  - В Windows 90 и более поздних версий

  #### Описание

  Указывает, следует ли использовать пользовательский интерфейс учетных данных Windows для ответа на запросы проверки подлинности NTLM и Negotiate.

Если вы отключите эту политику, для ответа на запросы NTLM и Negotiate будут использоваться основное имя пользователя и пароль. Если включить или не настраивать эту политику, будет использоваться пользовательский интерфейс учетных данных Windows.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WindowsHelloForHTTPAuthEnabled
  - Название GP: Функция Windows Hello для проверки подлинности HTTP включена
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Проверка подлинности HTTP
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Проверка подлинности HTTP
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Имя значения: WindowsHelloForHTTPAuthEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ## Политики режима полного экрана

  [В начало](#microsoft-edge---policies)

  ### KioskAddressBarEditingEnabled

  #### Настройка редактирования в адресной строке для общедоступного просмотра в режиме терминала

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 87 или позже

  #### Описание

  Эта политика применима только к режиму терминала в Microsoft Edge при использовании общедоступного просмотра.

Если вы включите или не настроите эту политику, пользователи смогут изменить URL-адрес в адресной строке.

Если вы отключите эту политику, пользователи не смогут изменить URL-адрес в адресной строке.

Подробнее о настройке режима терминала см. в статье [https://go.microsoft.com/fwlink/?linkid=2137578](https://go.microsoft.com/fwlink/?linkid=2137578).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: KioskAddressBarEditingEnabled
  - Имя групповой политики: Настройка редактирования в адресной строке для общедоступного просмотра в режиме терминала
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки режима полного экрана
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: KioskAddressBarEditingEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа настройки: KioskAddressBarEditingEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### KioskDeleteDownloadsOnExit

  #### Удалять файлы, загруженные в сеансе полного экрана, при закрытии Microsoft Edge

  
  
  #### Поддерживаемые версии:

  - В Windows 87 и более поздних версий

  #### Описание

  Эта политика применяется только к Microsoft Edge в режиме полного экрана.

Если включить эту политику, файлы, загруженные в сеансе полного экрана, будут удаляться каждый раз при закрытии Microsoft Edge.

Если выключить эту политику или не настроить ее, файлы, загруженные в сеансе полного экрана, не будут удаляться при закрытии Microsoft Edge.

Дополнительно о настройке режима полного экрана см. [https://go.microsoft.com/fwlink/?linkid=2137578](https://go.microsoft.com/fwlink/?linkid=2137578).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: KioskDeleteDownloadsOnExit
  - Имя GP: Удалять файлы, загруженные в сеансе полного экрана, при закрытии Microsoft Edge
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки режима полного экрана
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: KioskDeleteDownloadsOnExit
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ## Политики управляемости

  [В начало](#microsoft-edge---policies)

  ### MAMEnabled

  #### Управление мобильными приложениями включено

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с версии 89 или более поздней

  #### Описание

  Позволяет браузеру Microsoft Edge получать политики из служб управления приложениями Intune и применять их к профилям пользователей.

Если включить эту политику или не настроить ее, можно применять политики управления мобильными приложениями (MAM).

Если отключить эту политику, Microsoft Edge не будет связываться с Intune для запроса политик MAM.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: MAMEnabled
  - Имя групповой политики: управление мобильными приложениями включено
  - Путь к групповой политике (обязательно): Административные шаблоны/Microsoft Edge/Управляемость
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: MAMEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: MAMEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ## Собственные политики обмена сообщениями

  [В начало](#microsoft-edge---policies)

  ### NativeMessagingAllowlist

  #### Контроль, какие нативные хосты обмена сообщениями могут использовать пользователи

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Путем настройки политики указывается, какие узлы собственного обмена сообщениями не регулируются списком запрещений. Значение "*" в списке запрещений означает, что все узлы собственного обмена сообщениями запрещены, если они не разрешены явным образом.

По умолчанию разрешены все узлы собственного обмена сообщениями. Но если политика запрещает узел собственного обмена сообщениями, администратор может использовать список разрешений для изменения этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NativeMessagingAllowlist
  - Имя GP: управляйте тем, какие собственные узлы обмена сообщениями могут использовать пользователи
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Native Messaging
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\NativeMessagingAllowlist
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = "com.native.messaging.host.name2"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: NativeMessagingAllowlist
  - Пример значения:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### NativeMessagingBlocklist

  #### Настроить собственный черный список сообщений

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Путем настройки этой политики указывается, какие узлы собственного обмена сообщениями не должны загружаться. Значение "*" в списке запрещений означает, что все узлы собственного обмена сообщениями запрещены, если они не разрешены явным образом.

Если не настроить эту политику, Microsoft Edge будет загружать все установленные узлы собственного обмена сообщениями.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NativeMessagingBlocklist
  - Имя GP: Настройка собственного списка заблокированных сообщений
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Native Messaging
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\NativeMessagingBlocklist
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = "com.native.messaging.host.name2"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: NativeMessagingBlocklist
  - Пример значения:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### NativeMessagingUserLevelHosts

  #### Разрешить собственные узлы обмена сообщениями на уровне пользователя (установлены без прав администратора)

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Если эта политика включена или не настроена, Microsoft Edge может использовать узлы собственного обмена сообщениями, установленные на уровне пользователя.

Если эта политика отключена, Microsoft Edge может использовать эти узлы, только если они установлены на уровне системы.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NativeMessagingUserLevelHosts
  - Имя GP: Разрешить собственные узлы обмена сообщениями на уровне пользователя (устанавливается без прав администратора)
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Native Messaging
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: NativeMessagingUserLevelHosts
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: NativeMessagingUserLevelHosts
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ## Менеджер паролей и политики защиты

  [В начало](#microsoft-edge---policies)

  ### PasswordManagerEnabled

  #### Включить сохранение паролей в диспетчере паролей

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Включите Microsoft Edge для сохранения пользовательских паролей.

Если вы включите эту политику, пользователи смогут сохранять свои пароли в Microsoft Edge. При следующем посещении сайта Microsoft Edge автоматически введет пароль.

Если вы отключите эту политику, пользователи не смогут сохранять новые пароли, но они могут использовать ранее сохраненные пароли.

Если вы включите или отключите эту политику, пользователи не смогут изменить или переопределить ее в Microsoft Edge. Если вы не настроите его, пользователи смогут сохранять пароли, а также отключать эту функцию.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PasswordManagerEnabled
  - Имя GP: Включить сохранение паролей в диспетчере паролей
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Менеджер паролей и защита
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Менеджер паролей и защита
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: PasswordManagerEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PasswordManagerEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### PasswordMonitorAllowed

  #### Разрешение отправки оповещений пользователям, если их пароли окажутся небезопасными.

  
  
  #### Поддерживаемые версии:

  - В Windows — версия 85 или более поздние

  #### Описание

  Предоставление Microsoft Edge разрешения вести мониторинг пользовательских паролей.

Если вы включили эту политику и пользователь дал согласие на ее включение, он будет получать оповещение в тех случаях, если какой-либо из его паролей, хранящихся в Microsoft Edge, будет признан небезопасным. Оповещение будет отображаться в Microsoft Edge; кроме того, эта информация будет доступна в разделе Настройки > Пароли > Мониторинг паролей.

Если отключить эту политику, пользователям не будет предложено разрешить эту функцию. Их пароли не будут сканироваться и, соответственно, они не будут получать оповещений.

Если вы включите или не настроите эту политику, пользователи смогут включать и отключать эту функцию.

Подробнее о том, как Microsoft Edge находит небезопасные пароли, см. в статье [https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833)

Дополнительные рекомендации

Эту политику можно задать и как рекомендуемую, и как обязательную, однако необходимо сделать важное замечание.

Обязательное применение: учитывая, что согласие конкретного пользователя является необходимым условием включения для него этой политики, параметр "Обязательное применение" для этой политики отсутствует. Если установить для этой политики параметр "Обязательное применение", то пользовательский интерфейс в разделе "Настройки" не изменится, и на странице edge://policy будет отображаться следующее сообщение об ошибке

Пример сообщения об ошибке: "Этот параметр политики проигнорирован, поскольку для включения мониторинга паролей требуется разрешение пользователя. Вы можете попросить пользователей в вашей организации перейти в раздел "Настройки" > "Профиль" > "Пароль" и включить эту функцию ".

Рекомендуемое применение: если для политики включен параметр "Рекомендуемое применение", то в пользовательском интерфейсе в разделе "Настройки" этот параметр останется в состоянии "Выкл.", но рядом с ним будет отображаться значок портфеля, при наведении на который появится следующий текст: "Ваша организация рекомендует конкретное значение для этого параметра. Вы выбрали другое значение".

Параметры обязательного и рекомендуемого применения отключены: в обоих состояниях система будет работать обычным образом, и для пользователей будут отображаться обычные подписи.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PasswordMonitorAllowed
  - Имя GP: Разрешение отправки оповещений пользователям, если их пароли окажутся небезопасными.
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Менеджер паролей и защита
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Менеджер паролей и защита
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: PasswordMonitorAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### PasswordProtectionChangePasswordURL

  #### Настройте URL смены пароля

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настраивает URL смены пароля (только схемы HTTP и HTTPS).

Служба защиты паролем отправит пользователей по этому URL для изменения их пароля после просмотра предупреждения в браузере.

Если вы включите эту политику, то служба защиты паролем отправит пользователей по этому URL-адресу для изменения их пароля.

Если вы отключите эту политику или не настроите ее, служба защиты паролем не будет перенаправлять пользователей на URL-адрес смены пароля.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PasswordProtectionChangePasswordURL
  - Имя GP: Настройка URL смены пароля
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Менеджер паролей и защита
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: PasswordProtectionChangePasswordURL
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"https://contoso.com/change_password.html"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PasswordProtectionChangePasswordURL
  - Пример значения:
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### PasswordProtectionLoginURLs

  #### Настройка списка корпоративных URL-адресов входа, где служба защиты пароля должна фиксировать соленые хэши пароля

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настройка списка корпоративных URL-адресов для входа (только для схем HTTP и HTTPS), где Microsoft Edge должен фиксировать соленые хэши паролей и использовать их для обнаружения повторного использования паролей.

Если вы включите эту политику, служба защиты паролем захватывает отпечатки пальцев паролей на определенных URL-адресах.

Если вы отключите эту политику или не настроите ее, отпечатки паролей не будут записаны.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PasswordProtectionLoginURLs
  - Имя групповой политики: Настройка списка корпоративных URL-адресов входа, где служба защиты пароля должна фиксировать соленые хэши пароля
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Менеджер паролей и защита
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\PasswordProtectionLoginURLs
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = "https://contoso.com/login.html"
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = "https://login.contoso.com"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PasswordProtectionLoginURLs
  - Пример значения:
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### PasswordProtectionWarningTrigger

  #### Настройте триггер предупреждения о защите паролем

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет контролировать, когда вызывать предупреждение о защите паролем. Защита паролем предупреждает пользователей, когда они повторно используют свой защищенный пароль на потенциально подозрительных сайтах.

Вы можете использовать политики [PasswordProtectionLoginURLs](#passwordprotectionloginurls) и [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) для настройки паролей для защиты.

Исключения: пароли для сайтов, перечисленных в [PasswordProtectionLoginURLs](#passwordprotectionloginurls) и [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl), а также для сайтов, перечисленных в [SmartScreenAllowListDomains](#smartscreenallowlistdomains), не будут вызывать предупреждение о защите паролем.

Установите «PasswordProtectionWarningOff», чтобы не показывать предупреждения о защите паролем.

Установите «PasswordProtectionWarningOnPasswordReuse», чтобы отображать предупреждения о защите паролем, когда пользователь повторно использует свой защищенный пароль на сайте, который не включен в список.

Если вы отключите или не настроите эту политику, то триггер предупреждения не отображается.

Сопоставление параметров политики:

* PasswordProtectionWarningOff (0) = Предупреждение о защите паролем отключено

* PasswordProtectionWarningOnPasswordReuse (1) = Предупреждение о защите паролем инициируется повторным использованием пароля

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PasswordProtectionWarningTrigger
  - Имя GP: Настройка предупреждения о срабатывании защиты паролем
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Менеджер паролей и защита
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: PasswordProtectionWarningTrigger
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PasswordProtectionWarningTrigger
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### PasswordRevealEnabled

  #### Включить кнопку отображения пароля

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 87 или позже

  #### Описание

  Позволяет настроить стандартное отображение кнопки отображения пароля браузера для полей ввода паролей на веб-сайтах.

Если включить или не настроить эту политику, в пользовательских настройках браузера по умолчанию будет отображаться кнопка отображения пароля.

Если эта политика отключена, в пользовательских настройках браузера не будет отображаться кнопка отображения пароля.

Чтобы воспользоваться специальными возможностями, пользователь может изменить настройки браузера, используя политику по умолчанию.

Эта политика влияет только на кнопку отображения паролей в браузере, но не влияет на настраиваемые кнопки отображения веб-сайтов.

  #### Поддерживаемые функции:

  - Может быть обязательным: Нет
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PasswordRevealEnabled
  - Имя GP: Включить кнопку отображения пароля
  - Путь GP (обязательно): N / A
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Менеджер паролей и защита
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательно): N/A
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: PasswordRevealEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PasswordRevealEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ## Политики производительности

  [В начало](#microsoft-edge---policies)

  ### StartupBoostEnabled

  #### Включить усиление начальной загрузки

  
  
  #### Поддерживаемые версии:

  - В Windows 88 и более поздних версий

  #### Описание

  Позволяет запускать процессы Microsoft Edge при входе в ОС и выполнять перезапуск в фоновом режиме после закрытия последнего окна браузера.

Если Microsoft Edge работает в фоновом режиме, браузер может не закрываться и не выполнять перезапуск в фоновом режиме после закрытия последнего окна. См. политику [BackgroundModeEnabled](#backgroundmodeenabled) для получения информации о том, что произойдет после настройки поведения Microsoft Edge в фоновом режиме.

Если эта политика включена, включается усиление начальной загрузки.

Если эта политика отключена, усиление начальной загрузки выключается.

Если не настроить эту политику, усиление начальной загрузки может быть изначально выключено или включено.. Пользователь может настроить ее поведение на странице edge://settings/system.

Дополнительные сведения об усилении начальной загрузки: [https://go.microsoft.com/fwlink/?linkid=2147018](https://go.microsoft.com/fwlink/?linkid=2147018)

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: StartupBoostEnabled
  - Имя GP: Включение усиления начальной загрузки
  - Путь GP (обязательно): Административные шаблоны/Microsoft Edge/Производительность
  - Путь GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Производительность
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: StartupBoostEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ## Политика печати

  [В начало](#microsoft-edge---policies)

  ### DefaultPrinterSelection

  #### Правила выбора принтера по умолчанию

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Переопределяет стандартные правила выбора принтера Microsoft Edge. Эта политика определяет правила выбора принтера по умолчанию в Microsoft Edge, что происходит при первой попытке пользователя напечатать страницу.

Когда эта политика установлена, Microsoft Edge пытается найти принтер, который соответствует всем указанным атрибутам, и использует его в качестве принтера по умолчанию. Если существует несколько принтеров, которые соответствуют критериям, используется первый соответствующий принтер.

Если вы не настроите эту политику или не найдены подходящие принтеры в течение тайм-аута, принтер по умолчанию будет использовать встроенный принтер PDF или принтер не будет работать, если принтер PDF недоступен.

Значение анализируется как объект JSON в соответствии со следующей схемой: { "type": "object", "properties": { "idPattern": { "description": "Регулярное выражение для соответствия идентификатору принтера.", "Type ":" string "}," namePattern ": { " description ":" Регулярное выражение, соответствующее отображаемому имени принтера. "," type ":" string "} } }

Пропуск поля означает, что все значения совпадают; например, если вы не укажете возможность подключения, предварительный просмотр печати начнет обнаруживать все виды локальных принтеров. Шаблоны регулярных выражений должны соответствовать синтаксису JavaScript RegExp, а совпадения чувствительны к регистру.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultPrinterSelection
  - Имя GP: Правила выбора принтера по умолчанию
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Печать
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultPrinterSelection
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"{ \"idPattern\": \".*public\", \"namePattern\": \".*Color\" }"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultPrinterSelection
  - Пример значения:
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### PrintHeaderFooter

  #### Верхние и нижние колонтитулы печати

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Принудительно включить или отключить «верхние и нижние колонтитулы» в диалоговом окне печати.

Если вы не настроите эту политику, пользователи могут решить, печатать ли верхние и нижние колонтитулы.

Если вы отключите эту политику, пользователи не смогут печатать верхние и нижние колонтитулы.

Если вы включите эту политику, пользователи всегда будут печатать верхние и нижние колонтитулы.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PrintHeaderFooter
  - Название GP: Верхние и нижние колонтитулы печати
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Печать
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Печать
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: PrintHeaderFooter
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: PrintHeaderFooter
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### PrintPreviewUseSystemDefaultPrinter

  #### Установите системный принтер по умолчанию в качестве принтера по умолчанию

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Указывает Microsoft Edge использовать системный принтер по умолчанию в качестве выбора по умолчанию в режиме предварительного просмотра вместо последнего использованного принтера.

Если вы отключите эту политику или не настроите ее, в режиме предварительного просмотра в качестве пункта назначения по умолчанию будет использоваться последний использованный принтер.

Если вы включите эту политику, в окне предварительного просмотра будет использоваться принтер по умолчанию для операционной системы.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PrintPreviewUseSystemDefaultPrinter
  - Имя GP: Установите системный принтер по умолчанию в качестве принтера по умолчанию
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Печать
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Печать
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: PrintPreviewUseSystemDefaultPrinter
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: PrintPreviewUseSystemDefaultPrinter
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### PrinterTypeDenyList

  #### Отключить типы принтеров из списка запрещенных

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 88 или позже

  #### Описание

  Типы принтеров из списка запрещенных не будут обнаружены, и их возможности не будут получены.

Если вы помещаете все типы принтеров в список запрещенных, печать будет отключена, так как для документов не указано назначение печати.

Если эта политика не настроена или список принтеров пуст, все типы принтеров доступны для обнаружения.

Назначения принтеров включают принтеры расширения и локальные принтеры. Принтеры расширения также называются назначениями поставщика печати и включают любое назначение, относящееся к расширению Microsoft Edge.
Локальные принтеры также называются собственными назначениями печати и включают назначения, доступные для локального компьютера и общих сетевых принтеров.

Сопоставление параметров политики:

* privet (privet) = назначения протокола на основе Zeroconf (mDNS + DNS-SD)

* extension (extension) = назначения на основе расширения

* pdf (pdf) = назначение "Сохранить как PDF"

* local (local) = назначения локальных принтеров

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PrinterTypeDenyList
  - Имя GP: отключить типы принтеров из списка запрещенных
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Печать
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge\PrinterTypeDenyList
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\PrinterTypeDenyList\1 = "local"
SOFTWARE\Policies\Microsoft\Edge\PrinterTypeDenyList\2 = "privet"

```

  #### Сведения о Mac и параметры
  
  - Имя ключа настройки: PrinterTypeDenyList
  - Пример значения:
``` xml
<array>
  <string>local</string>
  <string>privet</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### PrintingAllowedBackgroundGraphicsModes

  #### Ограничение режима печати фона

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с версии 89 или более поздней

  #### Описание

  Ограничивает режим печати фона. Если эта политика не настроена, ограничения на печать фона отсутствуют.

Сопоставление параметров политики:

* любой (любой) = разрешить печать с фоном и без него

* включено (включено) = разрешить печать только с фоном

* отключено (отключено) = разрешить печать только без фона

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: PrintingAllowedBackgroundGraphicsModes
  - Имя групповой политики: ограничение режима печати фона
  - Путь к групповой политике (обязательно): Административные шаблоны/Microsoft Edge/Печать
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): Н/Д
  - Имя значения: PrintingAllowedBackgroundGraphicsModes
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"enabled"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PrintingAllowedBackgroundGraphicsModes
  - Пример значения:
``` xml
<string>enabled</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### PrintingBackgroundGraphicsDefault

  #### Режим печати фона по умолчанию

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с версии 89 или более поздней

  #### Описание

  Переопределяет последний использованный параметр для печати фоновой графики.
Если включить этот параметр, будет включена печать фоновой графики.
Если отключить этот параметр, печать фоновой графики будет отключена.

Сопоставление параметров политики:

* включено (включено) = включить режим печати фона по умолчанию

* отключено (отключено ) = отключить режим печати фона по умолчанию

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: PrintingBackgroundGraphicsDefault
  - Имя групповой политики: режим печати фона по умолчанию
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Печать
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: PrintingBackgroundGraphicsDefault
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"enabled"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PrintingBackgroundGraphicsDefault
  - Пример значения:
``` xml
<string>enabled</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### PrintingEnabled

  #### Включить печать

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Включает печать в Microsoft Edge и запрещает пользователям изменять этот параметр.

Если вы включите эту политику или не настроите ее, пользователи смогут печатать.

Если вы отключите эту политику, пользователи не смогут печатать из Microsoft Edge. Печать отключена в меню гаечного ключа, расширениях, приложениях JavaScript и т. д. Пользователи по-прежнему могут печатать из подключаемых модулей, которые обходят Microsoft Edge во время печати. Например, некоторые приложения Adobe Flash имеют параметр печати в контекстном меню, которое не распространяется на эту политику.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PrintingEnabled
  - Название GP: Включить печать
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Печать
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: PrintingEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PrintingEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### PrintingPaperSizeDefault

  #### Размер страницы печати по умолчанию

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  Переопределяет размер страницы печати, используемый по умолчанию.

Параметр name должен содержать один из указанных форматов или значение "custom", если нужный размер бумаги отсутствует в списке. Если присвоено значение "custom", следует указать свойство custom_size. Оно описывает нужную высоту и ширину в микрометрах. В противном случае свойство custom_size указывать не следует. Политика, нарушающая эти правила, игнорируется.

Если соответствующий размер страницы недоступен на принтере, выбранном пользователем, эта политика игнорируется.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Dictionary

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: PrintingPaperSizeDefault
  - Имя групповой политики: Размер страницы печати по умолчанию
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Печать
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: PrintingPaperSizeDefault
  - Тип значения: REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {
  "custom_size": {
    "height": 297000, 
    "width": 210000
  }, 
  "name": "custom"
}
```

  ##### Компактный пример значения:

  ```
  SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {"custom_size": {"height": 297000, "width": 210000}, "name": "custom"}
  ```
  

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PrintingPaperSizeDefault
  - Пример значения:
``` xml
<key>PrintingPaperSizeDefault</key>
<dict>
  <key>custom_size</key>
  <dict>
    <key>height</key>
    <integer>297000</integer>
    <key>width</key>
    <integer>210000</integer>
  </dict>
  <key>name</key>
  <string>custom</string>
</dict>
```
  

  [В начало](#microsoft-edge---policies)

  ### UseSystemPrintDialog

  #### Печать с использованием системного диалога печати

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Показывает системный диалог печати вместо предварительного просмотра.

Если вы включите эту политику, Microsoft Edge откроет системный диалог печати вместо встроенного предварительного просмотра, когда пользователь печатает страницу.

Если вы не настроите или не отключите эту политику, команды печати вызовут экран предварительного просмотра печати Microsoft Edge.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: UseSystemPrintDialog
  - Имя GP: Печать с использованием системного диалога печати
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Печать
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: UseSystemPrintDialog
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: UseSystemPrintDialog
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ## Политики прокси-сервера

  [В начало](#microsoft-edge---policies)

  ### ProxyBypassList

  #### Настроить правила обхода прокси-сервера (устарело)

  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Эта политика устарела, используйте [ProxySettings](#proxysettings). Она не будет работать в Microsoft Edge версии 91.

Определяет список хостов, для которых Microsoft Edge обходит любой прокси.

Эта политика применяется, если политика [ProxySettings](#proxysettings) не указана, и в политике [ProxyMode](#proxymode) выбрано fixed_servers. Если вы выбрали любой другой режим для настройки политик прокси, не включайте и не настраивайте эту политику.

Если вы включите эту политику, вы сможете создать список хостов, для которых Microsoft Edge не использует прокси.

Если вы не настроите эту политику, не будет создан список хостов, для которых Microsoft Edge обходит прокси. Оставьте эту политику ненастроенной, если вы указали любой другой метод для настройки прокси-политик.

Для более подробных примеров перейдите по ссылке [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ProxyBypassList
  - Имя GP: Настройка правил обхода прокси-сервера (устарело)
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Прокси-сервер
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ProxyBypassList
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"https://www.contoso.com, https://www.fabrikam.com"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ProxyBypassList
  - Пример значения:
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### ProxyMode

  #### Настроить параметры прокси-сервера (устарело)

  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Эта политика устарела, используйте [ProxySettings](#proxysettings). Она не будет работать в Microsoft Edge версии 91.

Если включить эту политику, можно указать прокси-сервер, который использует Microsoft Edge, и запрещает пользователям менять параметры прокси. Microsoft Edge игнорирует все параметры, связанные с прокси-сервером, которые указаны в командной строке. Политика применяется только в том случае, если не указана политика [ProxySettings](#proxysettings).

Другие параметры игнорируются, если выбрать один из следующих вариантов:
  * direct = никогда не использовать прокси-сервер и всегда подключаться напрямую
  * system = использовать системные настройки прокси
  * auto_detect = автоматически определять прокси-сервер

При использовании:
  * fixed_servers = использовать фиксированные прокси-серверы. Дополнительные параметры можно задать с помощью [ProxyServer](#proxyserver) и[ProxyBypassList](#proxybypasslist).
  * pac_script = использовать прокси-скрипт .pac. Чтобы задать URL-адрес для .pac файла прокс-сервера, используйте [ProxyPacUrl](#proxypacurl) .

Для подробных примеров, перейдите к [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

Если вы не настроите эту политику, пользователи могут выбрать свои собственные настройки прокси.

Сопоставление параметров политики:

* ProxyDisabled (direct) = никогда не использовать прокси

* ProxyAutoDetect (auto_detect) = Автоматическое определение настроек прокси

* ProxyPacScript (pac_script) = Использовать прокси-скрипт .pac

* ProxyFixedServers (fixed_servers) = использовать фиксированные прокси-серверы

* ProxyUseSystem (system) = использовать системные настройки прокси

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: ProxyMode
  - Имя GP: Настройка параметров прокси-сервера (устарело)
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Прокси-сервер
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ProxyMode
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"direct"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ProxyMode
  - Пример значения:
``` xml
<string>direct</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### ProxyPacUrl

  #### Установить URL-адрес файла .pac прокси-сервера (устарело)

  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Эта политика устарела, используйте [ProxySettings](#proxysettings). Она не будет работать в Microsoft Edge версии 91.

Указывает URL-адрес для файла автоматической настройки прокси (PAC).

Эта политика применяется, если политика [ProxySettings](#proxysettings) не указана, и в политике [ProxyMode](#proxymode) выбрано pac_script. Если вы выбрали любой другой режим для настройки политик прокси, не включайте и не настраивайте эту политику.

Если вы включите эту политику, вы можете указать URL-адрес для PAC файла, который определяет, как браузер автоматически выбирает соответствующий прокси-сервер для загрузки определенного веб-сайта.

Если вы отключите или не настроите эту политику, PAC файл не будет указан. Оставьте эту политику ненастроенной, если вы указали любой другой метод для настройки прокси-политик.

Подробные примеры см [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: ProxyPacUrl
  - Имя GP: Установка URL-адреса файла .pac прокси-сервера (устарело)
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Прокси-сервер
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ProxyPacUrl
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"https://internal.contoso.com/example.pac"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ProxyPacUrl
  - Пример значения:
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### ProxyServer

  #### Настроить адрес или URL прокси-сервера (устарело)

  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Эта политика устарела, используйте [ProxySettings](#proxysettings). Она не будет работать в Microsoft Edge версии 91.

Определяет URL прокси-сервера.

Эта политика применяется, если политика [ProxySettings](#proxysettings) не указана, и в политике [ProxyMode](#proxymode) выбрано fixed_servers. Если вы выбрали любой другой режим для настройки политик прокси, не включайте и не настраивайте эту политику.

Если вы включите эту политику, прокси-сервер, настроенный этой политикой, будет использоваться для всех URL-адресов.

Если вы отключите или не настроите эту политику, пользователи смогут выбирать свои собственные параметры прокси-сервера в этом режиме. Оставьте эту политику ненастроенной, если вы указали любой другой метод для настройки прокси-политик.

Дополнительные параметры и подробные примеры см [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: ProxyServer
  - Имя GP: Настройка адреса или URL прокси-сервера (устарело)
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Прокси-сервер
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ProxyServer
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"123.123.123.123:8080"
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: ProxyServer
  - Пример значения:
``` xml
<string>123.123.123.123:8080</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### ProxySettings

  #### Параметры прокси-сервера

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настраивает параметры прокси для Microsoft Edge.

Если вы включите эту политику, Microsoft Edge будет игнорировать все параметры, связанные с прокси, указанные в командной строке.

Если вы не настроите эту политику, пользователи могут выбрать свои собственные настройки прокси.

Эта политика переопределяет следующие отдельные политики:

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

Настройка политики [ProxySettings](#proxysettings) допускает указанные ниже поля.
  * ProxyMode, который позволяет указать прокси-сервер, используемый Microsoft Edge, и запрещает пользователям менять параметры прокси
  * ProxyPacUrl – URL-адрес файла .pac прокси-сервера
  * ProxyServer – URL-адрес прокси-сервера
  * ProxyBypassList – список прокси-хостов, которые обходит Microsoft Edge

Для ProxyMode, выбрано значение:
  * direct – прокси-сервер никогда не используется, а все остальные поля игнорируются.
  * system – используется системный прокси-сервер, а все остальные поля игнорируются.
  * auto_detect — все остальные поля игнорируются.
  * fixed_servers — используются поля ProxyServer и ProxyBypassList.
  * pac_script — используются поля ProxyPacUrl и ProxyBypassList.

Для более подробных примеров перейдите по ссылке [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Dictionary

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ProxySettings
  - Название GP: Настройки прокси
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Прокси-сервер
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ProxySettings
  - Тип значения: REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", 
  "ProxyMode": "pac_script", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```

  ##### Компактный пример значения:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {"ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", "ProxyMode": "pac_script", "ProxyPacUrl": "https://internal.site/example.pac", "ProxyServer": "123.123.123.123:8080"}
  ```
  

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ProxySettings
  - Пример значения:
``` xml
<key>ProxySettings</key>
<dict>
  <key>ProxyBypassList</key>
  <string>https://www.example1.com,https://www.example2.com,https://internalsite/</string>
  <key>ProxyMode</key>
  <string>pac_script</string>
  <key>ProxyPacUrl</key>
  <string>https://internal.site/example.pac</string>
  <key>ProxyServer</key>
  <string>123.123.123.123:8080</string>
</dict>
```
  

  [В начало](#microsoft-edge---policies)

  ## Политики параметров настройки вкладок для сна

  [В начало](#microsoft-edge---policies)

  ### SleepingTabsBlockedForUrls

  #### Блокировка вкладок для сна на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 88 или позже

  #### Описание

  Определите список сайтов в соответствии с шаблонами URL-адресов, которым не разрешено переходить в спящий режим с помощью спящих вкладок.

Если политика [SleepingTabsEnabled](#sleepingtabsenabled) отключена, этот список не используется, и сайты не будут автоматически переведены в спящий режим.

Если не настроить эту политику, все сайты будут иметь право на переход в спящий режим, если они не заблокированы в личной конфигурации пользователя.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SleepingTabsBlockedForUrls
  - Имя GP: Блокировка спящих вкладок на определенных сайтах
  - Путь к GP (обязательно): Параметры административных шаблонов/Microsoft Edge/спящих вкладок
  - Путь GP (рекомендуется): Параметры административных шаблонов/Microsoft Edge — параметры по умолчанию (пользователи могут переопределять)/спящих вкладок
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательно): SOFTWARE\Policies\Microsoft\Edge\SleepingTabsBlockedForUrls
  - Путь (рекомендуется): SOFTWARE\Policies\Microsoft\Edge\Recommended\SleepingTabsBlockedForUrls
  - Имя значения: 1, 2, 3,...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\SleepingTabsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SleepingTabsBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: SleepingTabsBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### SleepingTabsEnabled

  #### Настройка вкладок для сна

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 88 или позже

  #### Описание

  Этот параметр политики позволяет указать, следует ли включить спящие вкладки. Вкладки в спящем режиме сокращают использование ЦП, батареи и памяти путем перевода вкладок заднего плана бездействия в спящий режим. Microsoft Edge использует эвристику, чтобы избежать перевода в спящий режим вкладок, которые выполняют полезную работу в фоновом режиме, например, отображают уведомления, воспроизводят звук и транслируют видео. По умолчанию спящие вкладки включены.

Некоторые сайты могут быть заблокированы от перевода в режим сна с помощью настройки политики [SleepingTabsBlockedForUrls](#sleepingtabsblockedforurls).

Если этот параметр включен, спящие вкладки включены.

Если этот параметр отключен, спящие вкладки отключены.

Если не настроить этот параметр, пользователи смогут выбирать, следует ли использовать спящие вкладки.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SleepingTabsEnabled
  - Имя GP: Настройка спящих вкладок
  - Путь к GP (обязательно): Параметры административных шаблонов/Microsoft Edge/спящих вкладок
  - Путь GP (рекомендуется): Параметры административных шаблонов/Microsoft Edge — параметры по умолчанию (пользователи могут переопределять)/спящих вкладок
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Имя значения: SleepingTabsEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: SleepingTabsEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SleepingTabsTimeout

  #### Настройка времени бездействия фоновой вкладки для вкладки в режиме сна

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 88 или позже

  #### Описание

  Этот параметр политики позволяет настроить время ожидания в секундах, после чего неактивные вкладки фона будут автоматически переведены в спящий режим при включенной функции спящих вкладок. По умолчанию это время ожидания составляет 7 200 секунд (2 часа).

Вкладки переводятся в спящий режим автоматически, если политика [SleepingTabsEnabled](#sleepingtabsenabled) включена или не настроена, а пользователь включил параметр спящих вкладок.

Если не настроить эту политику, пользователи смогут выбрать значение времени ожидания.

Сопоставление параметров политики:

* 5Minutes (300) = 5 минут бездействия

* 15Minutes (900) = 15 минут бездействия

* 30Minutes (1800) = 30 минут бездействия

* 1Hour (3600) = 1 час бездействия

* 2Hours (7200) = 2 часа бездействия

* 3Hours (10800) = 3 часа бездействия

* 6Hours (21600) = 6 часов бездействия

* 12Hours (43200) = 12 часов бездействия

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SleepingTabsTimeout
  - Имя GP: Настройка время ожидания активности для фоновых вкладок на спящих вкладках
  - Путь к GP (обязательно): Параметры административных шаблонов/Microsoft Edge/спящих вкладок
  - Путь GP (рекомендуется): Параметры административных шаблонов/Microsoft Edge — параметры по умолчанию (пользователи могут переопределять)/спящих вкладок
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Имя значения: SleepingTabsTimeout
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000384
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: SleepingTabsTimeout
  - Пример значения:
``` xml
<integer>900</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ## Политики настроек SmartScreen

  [В начало](#microsoft-edge---policies)

  ### PreventSmartScreenPromptOverride

  #### Запретить обходить запросы фильтра SmartScreen в Microsoft Defender для сайтов

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Этот параметр политики позволяет вам решить, могут ли пользователи переопределять предупреждения фильтра SmartScreen в Microsoft Defender о потенциально вредоносных веб-сайтах.

Если вы включите этот параметр, пользователи не смогут игнорировать предупреждения фильтра SmartScreen в Microsoft Defender, и им будет запрещено посещать сайт.

Если этот параметр отключен или не настроен, пользователи могут игнорировать предупреждения фильтра SmartScreen в Microsoft Defender и переходить на сайт.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PreventSmartScreenPromptOverride
  - Имя GP: Предотвращение обхода запросов фильтра SmartScreen в Microsoft Defender для сайтов
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки SmartScreen
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: PreventSmartScreenPromptOverride
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PreventSmartScreenPromptOverride
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### PreventSmartScreenPromptOverrideForFiles

  #### Запретить обходить предупреждения фильтра SmartScreen в Microsoft Defender о загрузках

  
  
  #### Поддерживаемые версии:

  - В Windows с 77 и более поздних версий
  - MacOS с 79 и более поздних версий

  #### Описание

  Эта политика позволяет определить, могут ли пользователи переопределять предупреждения фильтра SmartScreen в Microsoft Defender о непроверенных загрузках.

Если вы включите эту политику, пользователи в вашей организации не смогут игнорировать предупреждения фильтра SmartScreen в Microsoft Defender, и они не смогут завершить непроверенные загрузки.

Если вы отключите или не настроите эту политику, пользователи могут игнорировать предупреждения фильтра SmartScreen в Microsoft Defender и завершать непроверенные загрузки.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PreventSmartScreenPromptOverrideForFiles
  - Имя GP: Предотвращение обхода предупреждений фильтра SmartScreen в Microsoft Defender о загрузках
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки SmartScreen
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: PreventSmartScreenPromptOverrideForFiles
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PreventSmartScreenPromptOverrideForFiles
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SmartScreenAllowListDomains

  #### Настройте список доменов, для которых фильтр SmartScreen в Microsoft Defender не будет вызывать предупреждения

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настройте список доверенных доменов фильтра SmartScreen в Microsoft Defender. Это означает, что фильтр SmartScreen в Microsoft Defender не будет проверять наличие потенциально вредоносных ресурсов, таких как фишинговое программное обеспечение и другие вредоносные программы, если исходные URL-адреса соответствуют этим доменам.
Служба защиты загрузок фильтра SmartScreen в Microsoft Defender не будет проверять загрузки, размещенные на этих доменах.

Если вы включите эту политику, фильтр SmartScreen в Microsoft Defender доверяет этим доменам.
Если вы отключите или не установите эту политику, защита фильтра SmartScreen в Microsoft Defender по умолчанию будет применена ко всем ресурсам.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.
Также обратите внимание, что эта политика не применяется, если в вашей организации включена Advanced Threat Protection в Microsoft Defender. Вместо этого вы должны настроить списки разрешенных и заблокированных сообщений в центре безопасности в Microsoft Defender.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SmartScreenAllowListDomains
  - Имя GP: Настройка списка доменов, для которых фильтр SmartScreen в Microsoft Defender не будет вызывать предупреждения
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки SmartScreen
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\SmartScreenAllowListDomains
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = "myuniversity.edu"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: SmartScreenAllowListDomains
  - Пример значения:
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### SmartScreenEnabled

  #### Настроить фильтр SmartScreen в Microsoft Defender

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Этот параметр политики позволяет настроить, включать ли фильтр SmartScreen в Microsoft Defender. Фильтр SmartScreen в Microsoft Defender предоставляет предупреждающие сообщения, чтобы помочь защитить ваших пользователей от потенциальных фишинговых и вредоносных программ. По умолчанию фильтр SmartScreen в Microsoft Defender включен.

Если этот параметр включен, фильтр SmartScreen в Microsoft Defender включен.

Если вы отключите этот параметр, фильтр SmartScreen в Microsoft Defender будет отключен.

Если вы не настроите этот параметр, пользователи смогут выбирать, использовать ли фильтр SmartScreen в Microsoft Defender.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SmartScreenEnabled
  - Название GP: Настройка фильтра SmartScreen в Microsoft Defender
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки SmartScreen
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Настройки SmartScreen
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: SmartScreenEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: SmartScreenEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SmartScreenForTrustedDownloadsEnabled

  #### Принудительно проверяет фильтр SmartScreen в Microsoft Defender на загрузку из надежных источников

  
  
  #### Поддерживаемые версии:

  - В Windows с 78 и более поздних версий

  #### Описание

  Этот параметр политики позволяет указать, будет ли фильтр SmartScreen в Microsoft Defender проверять репутацию загрузки из надежного источника.

Если этот параметр включен или не настроен, фильтр SmartScreen в Microsoft Defender проверяет репутацию загрузки независимо от источника.

Если этот параметр отключен, фильтр SmartScreen в Microsoft Defender не проверяет репутацию загрузки при загрузке из надежного источника.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, а также экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SmartScreenForTrustedDownloadsEnabled
  - Имя GP: Принудительная проверка скачивания из надежных источников с применением фильтра SmartScreen Microsoft Defender
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки SmartScreen
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Настройки SmartScreen
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: SmartScreenForTrustedDownloadsEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  

  [В начало](#microsoft-edge---policies)

  ### SmartScreenPuaEnabled

  #### Настройте фильтр SmartScreen в Microsoft Defender для блокировки потенциально нежелательных приложений

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 80 или позже

  #### Описание

  Этот параметр политики позволяет настроить, следует ли включать блокировку для потенциально нежелательных приложений с помощью фильтра SmartScreen Microsoft Defender. Потенциально нежелательная блокировка приложений с помощью фильтра SmartScreen Microsoft Defender предоставляет предупреждающие сообщения, которые помогают защитить пользователей от рекламного ПО, монетоприемников, пакетных программ и других приложений с низкой репутацией, которые размещаются на веб-сайтах. Потенциально нежелательная блокировка приложений с помощью фильтра SmartScreen Microsoft Defender по умолчанию отключена.

Если этот параметр включен, потенциально нежелательная блокировка приложений с помощью фильтра SmartScreen Microsoft Defender включена.

Если вы отключите этот параметр, потенциально нежелательная блокировка приложений с помощью фильтра SmartScreen Microsoft Defender будет отключена.

Если вы не настроите этот параметр, пользователи смогут выбирать, использовать ли потенциально нежелательную блокировку приложений с фильтром SmartScreen Microsoft Defender.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SmartScreenPuaEnabled
  - Имя GP: Настройте фильтр SmartScreen Microsoft Defender для блокировки потенциально нежелательных приложений.
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/Настройки SmartScreen
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Настройки SmartScreen
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: SmartScreenPuaEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: SmartScreenPuaEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ## Политики автозагрузки&comma;, домашней страницы и новых вкладок

  [В начало](#microsoft-edge---policies)

  ### HomepageIsNewTabPage

  #### Установить новую вкладку в качестве домашней страницы

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настраивает домашнюю страницу по умолчанию в Microsoft Edge. Вы можете установить домашнюю страницу на указанный вами URL-адрес или на новую вкладку.

Если вы включите эту политику, страница новой вкладки всегда будет использоваться для домашней страницы, а расположение URL домашней страницы игнорируется.

Если вы отключите эту политику, домашняя страница пользователя не может быть новой вкладкой, если для URL не задано значение 'edge://newtab'.

Если не настроено, пользователи могут выбрать, является ли новая вкладка их домашней страницей.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: HomepageIsNewTabPage
  - Имя GP: Установка новой вкладки в качестве домашней страницы
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/автозагрузка, домашняя страница и страница новой вкладки
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Автозагрузка, домашняя страница и страница новой вкладки
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: HomepageIsNewTabPage
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: HomepageIsNewTabPage
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### HomepageLocation

  #### Настроить URL-адрес домашней страницы

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настраивает URL-адрес домашней страницы по умолчанию в Microsoft Edge.

Домашняя страница - это страница, открываемая кнопкой Домой. Страницы, которые открываются при запуске, управляются политиками [RestoreOnStartup](#restoreonstartup).

Вы можете установить здесь URL-адрес или настроить домашнюю страницу, чтобы открыть страницу новой вкладки. Если вы решите открыть новую вкладку, эта политика не вступит в силу.

Если вы включите эту политику, пользователи не смогут изменить URL-адрес своей домашней страницы, но они могут использовать новую вкладку в качестве своей домашней страницы.

Если вы отключите или не настроите эту политику, пользователи смогут выбирать свою собственную домашнюю страницу, если не включена политика [HomepageIsNewTabPage](#homepageisnewtabpage).

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: HomepageLocation
  - Имя GP: Настройка URL домашней страницы
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/автозагрузка, домашняя страница и страница новой вкладки
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Автозагрузка, домашняя страница и страница новой вкладки
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: HomepageLocation
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"https://www.contoso.com"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: HomepageLocation
  - Пример значения:
``` xml
<string>https://www.contoso.com</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### NewTabPageAllowedBackgroundTypes

  #### Настройка типов фона, разрешенных для макета страницы новой вкладки

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  Вы можете настроить типы фоновых изображений, разрешенных для макета страницы новой вкладки в Microsoft Edge.

Если эта политика не настроена, на странице новой вкладки будут включены все типы фоновых изображений.

Сопоставление параметров политики:

* DisableImageOfTheDay (1) = Отключить ежедневный тип фонового изображения

* DisableCustomImage (2) = Отключить настраиваемый тип фонового изображения

* DisableAll (3) = Отключить все типы фоновых изображений

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NewTabPageAllowedBackgroundTypes
  - Имя GP: Настройка типов фона, разрешенных для макета страницы новой вкладки
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/автозагрузка, домашняя страница и страница новой вкладки
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: NewTabPageAllowedBackgroundTypes
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: NewTabPageAllowedBackgroundTypes
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### NewTabPageCompanyLogo

  #### Установить логотип организации на странице новой вкладки (устарело)

  
  >УСТАРЕЛО: эта политика устарела и не работает в Microsoft Edge версии 85 и более поздних.
  #### Поддерживаемые версии:

  - В Windows и macOS — версии c 79 по 85

  #### Описание

  Эта политика работала неправильно из-за изменений операционных требований. Поэтому она является устаревшей, и ее не следует использовать.

Указывает логотип компании для использования на новой вкладке в Microsoft Edge.

Политика должна быть настроена как строка, которая выражает логотип (ы) в формате JSON. Например: { "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo": { "url": "https://www.contoso.com/light_logo.png", "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" } }

Вы настраиваете эту политику, указав URL-адрес, с которого Microsoft Edge может загрузить логотип и его криптографический хеш (SHA-256), который используется для проверки целостности загрузки. Логотип должен быть в формате PNG или SVG, а его размер не должен превышать 16 МБ. Логотип загружается и кэшируется, и он будет перезагружен всякий раз, когда изменяется URL-адрес или хэш. URL должен быть доступен без какой-либо аутентификации.

'Default_logo' является обязательным и будет использоваться, когда нет фонового изображения. Если указано «light_logo», оно будет использоваться, когда на странице новой вкладки пользователя будет фоновое изображение. Мы рекомендуем горизонтальный логотип с прозрачным фоном по левому краю и по центру. Логотип должен иметь минимальную высоту 32 пикселя и соотношение сторон от 1:1 до 4:1. 'Default_logo' должен иметь надлежащий контраст с белым/черным фоном, в то время как 'light_logo' должен иметь надлежащий контраст с фоновым изображением.

Если вы включите эту политику, Microsoft Edge загрузит и покажет указанные логотипы на новой вкладке. Пользователи не могут переопределить или скрыть логотип (ы).

Если вы отключите или не настроите эту политику, Microsoft Edge не будет отображать логотип компании или логотип Microsoft на странице новой вкладки.

Для получения справки по определению хэша SHA-256 см. https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-filehash.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Dictionary

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NewTabPageCompanyLogo
  - Имя групповой политики: Установить логотип организации на странице новой вкладки (устарело)
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/автозагрузка, домашняя страница и страница новой вкладки
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: NewTabPageCompanyLogo
  - Тип значения: REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\NewTabPageCompanyLogo = {
  "default_logo": {
    "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29", 
    "url": "https://www.contoso.com/logo.png"
  }, 
  "light_logo": {
    "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737", 
    "url": "https://www.contoso.com/light_logo.png"
  }
}
```

  ##### Компактный пример значения:

  ```
  SOFTWARE\Policies\Microsoft\Edge\NewTabPageCompanyLogo = {"default_logo": {"hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29", "url": "https://www.contoso.com/logo.png"}, "light_logo": {"hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737", "url": "https://www.contoso.com/light_logo.png"}}
  ```
  

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: NewTabPageCompanyLogo
  - Пример значения:
``` xml
<key>NewTabPageCompanyLogo</key>
<dict>
  <key>default_logo</key>
  <dict>
    <key>hash</key>
    <string>cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29</string>
    <key>url</key>
    <string>https://www.contoso.com/logo.png</string>
  </dict>
  <key>light_logo</key>
  <dict>
    <key>hash</key>
    <string>517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737</string>
    <key>url</key>
    <string>https://www.contoso.com/light_logo.png</string>
  </dict>
</dict>
```
  

  [В начало](#microsoft-edge---policies)

  ### NewTabPageHideDefaultTopSites

  #### Скрыть стандартные сайты по умолчанию на новой вкладке

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Скрывает стандартные сайты по умолчанию на новой вкладке в Microsoft Edge.

Если для этой политики задано значение true, верхние плитки сайта по умолчанию скрыты.

Если для этой политики задано значение false или она не настроена, верхние плитки сайта по умолчанию остаются видимыми.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NewTabPageHideDefaultTopSites
  - Название GP: Скрытие топовых сайтов по умолчанию со страницы новой вкладки
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/автозагрузка, домашняя страница и страница новой вкладки
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: NewTabPageHideDefaultTopSites
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: NewTabPageHideDefaultTopSites
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### NewTabPageLocation

  #### Настроить URL-адрес страницы "Новая вкладка"

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настраивает URL-адрес по умолчанию для новой вкладки.

Рекомендуемая версия этой политики в настоящее время не работает и функционирует точно так же, как обязательная версия.

Эта политика определяет страницу, которая открывается при создании новых вкладок (в том числе при открытии новых окон). Это также влияет на начальную страницу, если она настроена на открытие новой вкладки.

Эта политика не определяет, какая страница открывается при запуске; это контролируется политикой [RestoreOnStartup](#restoreonstartup). Она также не влияет на домашнюю страницу, если настроено ее открытие в новой вкладке.

Если вы не настроите эту политику, используется новая вкладка по умолчанию.

Если вы настроите эту политику *и* политику [NewTabPageSetFeedType](#newtabpagesetfeedtype), эта политика будет иметь приоритет.

Если вы предпочитаете использовать пустую вкладку, правильный URL-адрес— "about:blank", а не "about://blank".

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NewTabPageLocation
  - Имя GP: Настройка URL новой вкладки
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/автозагрузка, домашняя страница и страница новой вкладки
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Автозагрузка, домашняя страница и страница новой вкладки
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: NewTabPageLocation
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"https://www.fabrikam.com"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: NewTabPageLocation
  - Пример значения:
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### NewTabPageManagedQuickLinks

  #### Установить быстрые ссылки на новую вкладку

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 79 или позже

  #### Описание

  По умолчанию Microsoft Edge отображает быстрые ссылки на странице новой вкладки из добавленных пользователем ярлыков и популярных сайтов на основе истории просмотров. С помощью этой политики вы можете настроить до трех плиток быстрых ссылок на новой вкладке, выраженных в виде объекта JSON:

[ { "url": "https://www.contoso.com", "title": "Contoso Portal", "pinned": true/false }, ... ]

Поле 'url' обязательно для заполнения; 'title' и 'pinned' являются необязательными. Если заголовок не указан, в качестве заголовка по умолчанию используется URL. Если «закреплено» не предусмотрено, значением по умолчанию является false.

Microsoft Edge представляет их в указанном порядке слева направо, причем все закрепленные листы отображаются перед не прикрепленными листами.

Если политика установлена как обязательная, поле «закреплено» будет игнорироваться и все ячейки будут закреплены. Плитка не может быть удалена пользователем и всегда будет отображаться в начале списка быстрых ссылок.

Если политика установлена в соответствии с рекомендациями, закрепленные листы останутся в списке, но пользователь сможет их редактировать и удалять. Плитки быстрых ссылок, которые не закреплены, ведут себя как популярные сайты по умолчанию и удаляются из списка, если другие сайты посещаются чаще. При применении не закрепленных ссылок с помощью этой политики к существующему профилю браузера ссылки могут не отображаться вообще, в зависимости от их ранжирования по сравнению с историей просмотра пользователя.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Dictionary

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NewTabPageManagedQuickLinks
  - Название GP: Установить быстрые ссылки на новую вкладку
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/автозагрузка, домашняя страница и страница новой вкладки
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Автозагрузка, домашняя страница и страница новой вкладки
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: NewTabPageManagedQuickLinks
  - Тип значения: REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\NewTabPageManagedQuickLinks = [
  {
    "pinned": true, 
    "title": "Contoso Portal", 
    "url": "https://contoso.com"
  }, 
  {
    "title": "Fabrikam", 
    "url": "https://fabrikam.com"
  }
]
```

  ##### Компактный пример значения:

  ```
  SOFTWARE\Policies\Microsoft\Edge\NewTabPageManagedQuickLinks = [{"pinned": true, "title": "Contoso Portal", "url": "https://contoso.com"}, {"title": "Fabrikam", "url": "https://fabrikam.com"}]
  ```
  

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: NewTabPageManagedQuickLinks
  - Пример значения:
``` xml
<key>NewTabPageManagedQuickLinks</key>
<array>
  <dict>
    <key>pinned</key>
    <true/>
    <key>title</key>
    <string>Contoso Portal</string>
    <key>url</key>
    <string>https://contoso.com</string>
  </dict>
  <dict>
    <key>title</key>
    <string>Fabrikam</string>
    <key>url</key>
    <string>https://fabrikam.com</string>
  </dict>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### NewTabPagePrerenderEnabled

  #### Включение предварительной загрузки новой вкладки для ускорения отрисовки

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS — версия 85 или более поздние

  #### Описание

  Если настроить эту политику, предварительная загрузка вкладки будет включена, и у пользователей не будет возможности изменить этот параметр. Если не настроить эту политику, предварительная загрузка вкладки будет включена, и у пользователей будет возможность изменить этот параметр.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NewTabPagePrerenderEnabled
  - Имя GP: Включение предварительной загрузки новой вкладки для ускорения отрисовки
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/автозагрузка, домашняя страница и страница новой вкладки
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Автозагрузка, домашняя страница и страница новой вкладки
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: NewTabPagePrerenderEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: NewTabPagePrerenderEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### NewTabPageSetFeedType

  #### Настройка Microsoft Edge для новой вкладки (не рекомендуется)

  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 79 или позже

  #### Описание

  Мы не рекомендуем эту политику, так как новая версия корпоративной страницы новой вкладки больше не требует выбора между различными типами контента. Вместо этого контент, предоставляемый пользователю, можно контролировать с помощью Центра администрирования Microsoft 365. Чтобы получить доступ к Центру администрирования Microsoft 365, выполните вход https://admin.microsoft.com с помощью учетной записи администратора. Политика станет устаревшей в Microsoft Edge версии 90.

Позволяет выбрать режим новостей Microsoft News или Office 365 для новой вкладки.

Если для этой политики задано значение «News», пользователи увидят новостную ленту Microsoft на странице новой вкладки.

Если для этой политики задано значение «Office», после входа в браузер Azure Active Directory пользователи увидят работу ленты Office 365 на новой вкладке.

Если отключить или не настроить эту политику:

- Пользователям, имеющим вход в браузер Azure Active Directory, предлагается новый веб-канал Office 365 для просмотра вкладок, а также стандартная новая страница-вкладка.

- Пользователи без входа в Azure Active Directory через браузер увидят стандартную новую вкладку.

Если вы настраиваете эту политику *и* политику [NewTabPageLocation](#newtabpagelocation), [NewTabPageLocation](#newtabpagelocation)имеет приоритет.

Настройка по умолчанию: отключено или не настроено.

Сопоставление параметров политики:

* News (0) = Взаимодействие новостной ленты Microsoft

* Office (1) = Взаимодействие ленты Office 365

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NewTabPageSetFeedType
  - Имя GP: Настройка Microsoft Edge для новой вкладки (не рекомендуется)
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/автозагрузка, домашняя страница и страница новой вкладки
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Автозагрузка, домашняя страница и страница новой вкладки
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: NewTabPageSetFeedType
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: NewTabPageSetFeedType
  - Пример значения:
``` xml
<integer>0</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### RestoreOnStartup

  #### Действие при запуске

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определите, как Microsoft Edge будет работать при запуске.

Если вы хотите, чтобы новая вкладка всегда открывалась при запуске, выберите «RestoreOnStartupIsNewTabPage».

Если вы хотите снова открыть URL-адреса, которые были открыты в последний раз, когда Microsoft Edge закрывался, выберите «RestoreOnStartupIsLastSession». Сеанс просмотра будет восстановлен, как это было. Обратите внимание, что этот параметр отключает некоторые параметры, которые зависят от сеансов или которые выполняют действия при выходе (например, Очистить данные просмотра при выходе или файлы cookie только для сеанса).

Если вы хотите открыть определенный набор URL-адресов, выберите «RestoreOnStartupIsURLs».

Отключение этого параметра равносильно тому, что он не настроен. Пользователи смогут изменить его в Microsoft Edge.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

Сопоставление параметров политики:

* RestoreOnStartupIsNewTabPage (5) = открыть новую вкладку

* RestoreOnStartupIsLastSession (1) = восстановить последний сеанс

* RestoreOnStartupIsURLs (4) = Открыть список URL-адресов

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: RestoreOnStartup
  - Имя GP: Действие при запуске
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/автозагрузка, домашняя страница и страница новой вкладки
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Автозагрузка, домашняя страница и страница новой вкладки
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: RestoreOnStartup
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000004
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: RestoreOnStartup
  - Пример значения:
``` xml
<integer>4</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### RestoreOnStartupURLs

  #### Сайты открываются при запуске браузера

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Укажите список сайтов, которые будут открываться автоматически при запуске браузера. Если вы не настроите эту политику, ни один сайт не будет открыт при запуске.

Эта политика работает только в том случае, если для политики [RestoreOnStartup](#restoreonstartup) также установлено значение «Открыть список URL-адресов» (4).

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: RestoreOnStartupURLs
  - Имя GP: Сайты, которые открываются при запуске браузера.
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/автозагрузка, домашняя страница и страница новой вкладки
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Автозагрузка, домашняя страница и страница новой вкладки
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\RestoreOnStartupURLs
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended\RestoreOnStartupURLs
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = "https://contoso.com"
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = "https://www.fabrikam.com"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: RestoreOnStartupURLs
  - Пример значения:
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### ShowHomeButton

  #### Показать кнопку Home на панели инструментов

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Показывает кнопку «Домой» на панели инструментов Microsoft Edge.

Включите эту политику, чтобы всегда отображать кнопку «Домой». Отключите его, чтобы никогда не показывать кнопку.

Если вы не настроите политику, пользователи могут выбрать, показывать ли кнопку «Домой».

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ShowHomeButton
  - Название GP: Показать кнопку Home на панели инструментов
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/автозагрузка, домашняя страница и страница новой вкладки
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/Автозагрузка, домашняя страница и страница новой вкладки
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ShowHomeButton
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ShowHomeButton
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ## Дополнительные политики

  [В начало](#microsoft-edge---policies)

  ### AddressBarMicrosoftSearchInBingProviderEnabled

  #### Включить поиск Microsoft в предложениях Bing в адресной строке

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с 81 и более поздних версий

  #### Описание

  Позволяет отображать соответствующие предложения Microsoft Search в Bing в списке предложений адресной строки, когда пользователь вводит строку поиска в адресной строке. Если вы включите или не настроите эту политику, пользователи смогут видеть внутренние результаты, основанные на поиске Microsoft в Bing, в списке предложений адресной строки Microsoft Edge. Чтобы просмотреть результаты поиска Microsoft в Bing, пользователь должен войти в Microsoft Edge со своей учетной записью Azure AD для этой организации.
Если отключить эту политику, пользователи не смогут просматривать внутренние результаты в списке предложений адресной строки Microsoft Edge.
С Microsoft Edge версии 89 предложения Поиска (Майкрософт) в Bing будут доступны, даже если Bing не является службой поиска по умолчанию для пользователя.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AddressBarMicrosoftSearchInBingProviderEnabled
  - Имя GP: Включить поиск Microsoft в предложениях Bing в адресной строке
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AddressBarMicrosoftSearchInBingProviderEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AddressBarMicrosoftSearchInBingProviderEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### AdsSettingForIntrusiveAdsSites

  #### Настройка рекламы для сайтов с навязчивой рекламой

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 78 и более поздних версий

  #### Описание

  Управляет блокировкой рекламы на сайтах с навязчивой рекламой.

Сопоставление параметров политики:

* AllowAds (1) = Разрешить рекламу на всех сайтах

* BlockAds (2) = Блокировать рекламу на сайтах с навязчивой рекламой. (Значение по умолчанию)

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AdsSettingForIntrusiveAdsSites
  - Название GP: Настройка рекламы для сайтов с навязчивой рекламой
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AdsSettingForIntrusiveAdsSites
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: AdsSettingForIntrusiveAdsSites
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### AllowDeletingBrowserHistory

  #### Включить удаление браузера и историю загрузок

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет удалять историю браузера и историю загрузок и запрещает пользователям изменять этот параметр.

Обратите внимание, что даже если эта политика отключена, история просмотра и загрузки не гарантируется: пользователи могут редактировать или удалять файлы базы данных истории напрямую, а сам браузер может удалять (в зависимости от срока действия) или архивировать любой или все предметы истории в любое время.

Если вы включите эту политику или не настроите ее, пользователи смогут удалить историю просмотров и загрузок.

Если отключить эту политику, пользователи не смогут удалять журнал просмотра и загрузок, а синхронизация журнала будет отключена.

Если вы включите эту политику, не включайте политику ClearBrowsingDataOnExit, потому что они оба имеют дело с удалением данных[ClearBrowsingDataOnExit](#clearbrowsingdataonexit) Если вы включите оба, политика [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) имеет приоритет и удаляет все данные при закрытии Microsoft Edge независимо от того, как настроена эта политика.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AllowDeletingBrowserHistory
  - Имя GP: включить удаление браузера и историю загрузок
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AllowDeletingBrowserHistory
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AllowDeletingBrowserHistory
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### AllowFileSelectionDialogs

  #### Разрешить диалог выбора файла

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Разрешите доступ к локальным файлам, позволяя Microsoft Edge отображать диалоговые окна выбора файлов.

Если вы включите или не настроите эту политику, пользователи смогут открывать диалоги выбора файлов как обычно.

Если вы отключите эту политику, всякий раз, когда пользователь выполняет действие, которое вызывает диалоговое окно выбора файлов (например, импорт избранных файлов, выгрузка файлов или сохранение ссылок), вместо этого отображается сообщение, и предполагается, что пользователь нажал кнопку «Отмена» при выборе файла. диалог.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AllowFileSelectionDialogs
  - Имя GP: Разрешить диалог выбора файла
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AllowFileSelectionDialogs
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AllowFileSelectionDialogs
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### AllowPopupsDuringPageUnload

  #### Позволяет странице показывать всплывающие окна во время ее выгрузки (устаревший)

  
  >УСТАРЕЛО: эта политика устарела и не работает в версиях Microsoft Edge после 87.
  #### Поддерживаемые версии:

  - В Windows и macOS — версии c 78 по 87

  #### Описание

  Эта политика позволяет администратору указать, что страница может отображать всплывающие окна во время ее выгрузки.Эта политика позволяет администратору показывать всплывающие окна во время выгрузки страницы.

Когда политика включена, на страницах разрешается показывать всплывающие окна во время их выгрузки.

Когда для политики установлено значение «отключено» или «не установлено», на страницах не разрешается показывать всплывающие окна во время их выгрузки. Это согласно спецификации: (https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name).

Эта политика была удалена в Microsoft Edge 88 и игнорируется, если она установлена.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AllowPopupsDuringPageUnload
  - Имя GP: позволяет странице показывать всплывающие окна во время ее выгрузки (устаревший)
  - Путь к GP (обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AllowPopupsDuringPageUnload
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AllowPopupsDuringPageUnload
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### AllowSurfGame

  #### Разрешить серфинг

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 83 и более поздних версий

  #### Описание

  Если вы отключите эту политику, пользователи не смогут играть в игру для серфинга, когда устройство находится в автономном режиме или если пользователь переходит к edge://surf.

Если вы включите или не настроите эту политику, пользователи смогут играть в игру для серфинга.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AllowSurfGame
  - Имя GP: разрешить путешествовать по играм
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AllowSurfGame
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AllowSurfGame
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### AllowSyncXHRInPageDismissal

  #### Разрешить страницам отправлять синхронные запросы XHR при удалении страницы (не рекомендуется)

  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 79 или позже

  #### Описание

  Эта политика не рекомендуется, так как она предусмотрена только в качестве краткосрочного механизма, предоставляющего организациям больше времени на обновление веб-содержимого, если и при условии, что оно не совместимо с изменением, чтобы предотвратить отправку синхронных запросов XHR при удалении страницы. Она не будет работать в Microsoft Edge версии 88.

Эта политика позволяет указать, что страница может отправлять синхронные XHR-запросы во время удаления страницы.

Если вы включите эту политику, страницы могут отправлять синхронные запросы XHR во время удаления страницы.

Если вы отключите эту политику или не настроите ее, страницам не разрешается отправлять синхронные запросы XHR во время удаления страницы.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AllowSyncXHRInPageDismissal
  - Имя групповой политики: разрешить страницам отправлять синхронные запросы XHR при удаления страницы (не рекомендуется)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AllowSyncXHRInPageDismissal
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AllowSyncXHRInPageDismissal
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### AllowTokenBindingForUrls

  #### Настроить список сайтов, для которых Microsoft Edge будет пытаться установить привязку токена.

  
  
  #### Поддерживаемые версии:

  - На Windows с 83 и более поздних версий

  #### Описание

  Настройте список шаблонов URL для сайтов, с которыми браузер будет пытаться выполнить протокол привязки токенов.
Для доменов из этого списка браузер отправит Token Binding ClientHello в рукопожатии TLS (см. https://tools.ietf.org/html/rfc8472).
Если сервер отвечает допустимым ответом ServerHello, браузер будет создавать и отправлять сообщения о привязке токенов при последующих https запросах. Дополнительные сведения см. в статье https://tools.ietf.org/html/rfc8471.

Если этот список пуст, привязка токена будет отключена.

Эта политика доступна только на устройствах с Windows 10 с возможностью виртуального безопасного режима.

С Microsoft Edge 86 эта политика больше не поддерживает динамическое обновление.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AllowTokenBindingForUrls
  - Имя GP: Настройка списка сайтов, для которых Microsoft Edge попытается установить привязку токена.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\AllowTokenBindingForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = "[*.]mydomain2.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = "[*.].mydomain2.com"

```

  

  [В начало](#microsoft-edge---policies)

  ### AllowTrackingForUrls

  #### Настроить исключения для предотвращения отслеживания для определенных сайтов

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 78 и более поздних версий

  #### Описание

  Настройте список шаблонов URL, которые исключены из предотвращения отслеживания.

Если вы настроите эту политику, список настроенных шаблонов URL будет исключен из функции предотвращения отслеживания.

Если вы не настроите эту политику, для всех сайтов будет использоваться глобальное значение по умолчанию из политики «Блокировать отслеживание активности пользователей в Интернете» (если установлено) или личная конфигурация пользователя.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AllowTrackingForUrls
  - Имя GP: Настройка исключений отслеживания для определенных сайтов
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\AllowTrackingForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: AllowTrackingForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### AlternateErrorPagesEnabled

  #### Если не удается найти веб-страницу, предлагать похожие страницы

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 80 или позже

  #### Описание

  Разрешить Microsoft Edge выдавать соединение с веб-службой для создания URL-адреса и поиска предложений для устранения проблем с подключением, таких как ошибки DNS.

Если вы включите эту политику, веб-служба будет использоваться для создания URL-адресов и поиска предложений для сетевых ошибок.

Если вы отключите эту политику, вызовы веб-службы не будут выполняться, и отобразится стандартная страница ошибок.

Если вы не настроите эту политику, Microsoft Edge учитывает пользовательские настройки, установленные в разделе «Сервисы на edge://settings/privacy.
А именно, есть переключатель **Если не удается найти веб-страницу, предлагать похожие страницы**, который пользователь может устанавливать в положение "Вкл." или "Выкл.". Обратите внимание: если вы включили эту политику (AlternateErrorPagesEnabled), параметр "Если не удается найти веб-страницу, предлагать похожие страницы" будет включен, но у пользователя не будет возможности изменить его с помощью этого переключателя. Если вы отключите эту политику, параметр "Если не удается найти веб-страницу, предлагать похожие страницы" будет выключен, и у пользователя не будет возможности изменить его с помощью этого переключателя.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AlternateErrorPagesEnabled
  - Имя GP: Если не удается найти веб-страницу, предлагать похожие страницы
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: AlternateErrorPagesEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AlternateErrorPagesEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### AlwaysOpenPdfExternally

  #### Всегда открывайте PDF-файлы извне

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Отключает внутреннее средство просмотра PDF-файлов в Microsoft Edge.

Если вы включите эту политику, Microsoft Edge будет обрабатывать файлы PDF как загружаемые файлы и разрешит пользователям открывать их с помощью приложения по умолчанию.

Если Microsoft Edge является средством чтения PDF по умолчанию, PDF-файлы не загружаются и продолжат открываться в Microsoft Edge.

Если эта политика не настроена или отключена, PDF-файлы будут открываться в Microsoft Edge (если пользователь не отключит эту функцию).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AlwaysOpenPdfExternally
  - Имя GP: Всегда открывать PDF-файлы извне
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AlwaysOpenPdfExternally
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AlwaysOpenPdfExternally
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### AmbientAuthenticationInPrivateModesEnabled

  #### Включить внешнюю аутентификацию для профилей InPrivate и Guest

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с 81 и более поздних версий

  #### Описание

  Настройте эту политику, чтобы разрешить / запретить внешнюю аутентификацию для профилей InPrivate и Guest в Microsoft Edge.

Ambient Authentication - это HTTP-аутентификация с учетными данными по умолчанию, когда явные учетные данные не предоставляются через NTLM / Kerberos / Negotiate схемы запроса / ответа.

Если для этой политики задано значение «RegularOnly», внешняя аутентификация будет разрешена только для регулярных сеансов. Сессиям InPrivate и Guest не разрешается выполнять внешнюю аутентификацию.

Если для политики задано значение «InPrivateAndRegular», внешняя аутентификация будет разрешена для сеансов InPrivate и Regular. Гостевые сеансы не будут разрешены для внешней аутентификации.

Если для политики задано значение «GuestAndRegular», она разрешает внешнюю аутентификацию для гостевых и обычных сеансов. Сеансам InPrivate не разрешается внешняя аутентификация

Если для политики задано значение «All», она разрешает внешнюю аутентификацию для всех сеансов.

Обратите внимание, что внешняя аутентификация всегда разрешена в обычных профилях

В Microsoft Edge версии 81 и новее, если политика не задана, внешняя аутентификация будет включена только в обычных сеансах.

Сопоставление параметров политики:

* RegularOnly (0) = Включить внешнюю аутентификацию только в обычных сеансах

* InPrivateAndRegular (1) = Включить внешнюю аутентификацию в InPrivate и обычных сеансах

* GuestAndRegular (2) = Включить внешнюю аутентификацию в гостевых и обычных сеансах

* All (3) = Включить внешнюю аутентификацию в обычных, InPrivate и гостевых сессиях

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AmbientAuthenticationInPrivateModesEnabled
  - Имя GP: Включить Ambient Authentication для профилей InPrivate и Guest
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AmbientAuthenticationInPrivateModesEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AmbientAuthenticationInPrivateModesEnabled
  - Пример значения:
``` xml
<integer>0</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### AppCacheForceEnabled

  #### Разрешение повторного включения компонента AppCache, даже если он отключен по умолчанию.

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS — версия 84 или более поздние

  #### Описание

  Если для этой политики задано значение "истина", AppCache будет включен, даже когда по умолчанию AppCache в Microsoft Edge недоступен.

Если установить для этой политики значение "ложь" или не настраивать ее, для компонента AppCache будут действовать настройки, по умолчанию заданные в Microsoft Edge.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP:AppCacheForceEnabled
  - Имя GP: Разрешить повторное включение компонента AppCache, даже если он отключен по умолчанию.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AppCacheForceEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AppCacheForceEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ApplicationLocaleValue

  #### Настройка языкового стандарта приложения

  
  
  #### Поддерживаемые версии:

  - В Windows с 77 и более поздних версий

  #### Описание

  Настраивает языковой стандарт приложения в Microsoft Edge и запрещает пользователям изменять языковой стандарт.

Если вы включите эту политику, Microsoft Edge будет использовать указанный языковой стандарт. Если настроенный языковой стандарт не поддерживается, вместо него используется en-US.

Если этот параметр отключен или не настроен, Microsoft Edge использует либо указанный пользователем предпочтительный языковой стандарт (если он настроен), либо резервный языковой стандарт «en-US».

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ApplicationLocaleValue
  - Имя GP: Настройка языкового стандарта приложения
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ApplicationLocaleValue
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"en"
```

  

  [В начало](#microsoft-edge---policies)

  ### AudioCaptureAllowed

  #### Разрешить или заблокировать захват звука

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет указать, будет ли пользователю предлагаться предоставить веб-сайту доступ к своему устройству захвата звука. Эта политика применяется ко всем URL-адресам, кроме тех, которые настроены в списке [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Если вы включите эту политику или не настроите ее (настройка по умолчанию), пользователю будет предложен доступ к захвату звука, за исключением URL-адресов в списке [AudioCaptureAllowedUrls](#audiocaptureallowedurls). Эти перечисленные URL-адреса получают доступ без запроса.

Если вы отключите эту политику, пользователю не будет предложено, и захват аудио доступен только для URL-адресов, настроенных в [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Эта политика затрагивает все типы аудиовходов, а не только встроенный микрофон.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AudioCaptureAllowed
  - Имя GP: Разрешить или заблокировать захват аудио
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AudioCaptureAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AudioCaptureAllowed
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### AudioCaptureAllowedUrls

  #### Сайты, которые могут получить доступ к устройствам захвата звука без запроса разрешения

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Укажите веб-сайты, основанные на шаблонах URL, которые могут использовать устройства захвата звука, не запрашивая у пользователя разрешения. Шаблоны в этом списке сопоставляются с источником безопасности запрашивающего URL. Если они совпадают, сайту автоматически предоставляется доступ к устройствам захвата звука.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AudioCaptureAllowedUrls
  - Имя GP: Сайты, которые могут получить доступ к устройствам захвата звука без запроса разрешения
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\AudioCaptureAllowedUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AudioCaptureAllowedUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### AudioSandboxEnabled

  #### Разрешить запуск аудио-песочницы

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с 81 и более поздних версий

  #### Описание

  Эта политика управляет песочницей аудио процесса.

Если вы включите эту политику, аудио процесс будет выполняться в песочнице.

Если вы отключите эту политику, аудио процесс будет запущен без коробки, а модуль обработки звука WebRTC будет запущен в процессе рендеринга.
Это оставляет пользователей открытыми для угроз безопасности, связанных с запуском звуковой подсистемы.

Если вы не настроите эту политику, будет использована конфигурация по умолчанию для звуковой песочницы, которая может отличаться в зависимости от платформы.

Эта политика предназначена для предоставления предприятиям гибкости, чтобы отключить звуковую изолированную программную среду, если они используют настройки программного обеспечения безопасности, которые мешают в изолированной программной среде.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AudioSandboxEnabled
  - Имя GP: Разрешить запуск аудио-песочницы
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AudioSandboxEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AudioSandboxEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### AutoImportAtFirstRun

  #### Автоматический импорт данных и настроек другого браузера при первом запуске

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Если вы включите эту политику, все поддерживаемые типы данных и параметры из указанного браузера будут автоматически и автоматически импортироваться при первом запуске. Во время первого запуска раздел импорта также будет пропущен.

Данные браузера из устаревшей версии Microsoft Edge всегда будут автоматически перенесены при первом запуске, независимо от значения этой политики.

Если для этой политики установлено значение «FromDefaultBrowser», будут импортированы типы данных, соответствующие браузеру по умолчанию на управляемом устройстве.

Если браузер, указанный в качестве значения этой политики, отсутствует на управляемом устройстве, Microsoft Edge просто пропустит импорт без какого-либо уведомления пользователя.

Если для этой политики установлено значение «DisabledAutoImport», раздел импорта при первом запуске полностью пропускается, и Microsoft Edge не импортирует данные и настройки браузера автоматически.

Если для этой политики задано значение «FromInternetExplorer», из Internet Explorer будут импортированы следующие типы данных:
1. Избранные или закладки
2. Сохраненные пароли
3. Поисковые системы
4. История просмотров
5. Домашняя страница

Если для этого правила установлено значение «FromGoogleChrome», из Google Chrome будут импортированы следующие типы данных:
1. Избранное
2. Сохраненные пароли
3. Адреса и другие сведения
4. Платежная информация
5. История просмотров
6. Параметры
7. Закрепленные и открытые вкладки
8. Расширения
9. Файлы cookie

Примечание. Для получения дополнительной информации о том, что импортируется из Google Chrome, см. [https://go.microsoft.com/fwlink/?linkid=2120835](https://go.microsoft.com/fwlink/?linkid=2120835)

Если для этой политики задано значение «FromSafari», пользовательские данные больше не импортируются в Microsoft Edge. Это связано с тем, как работает полный доступ к диску на компьютере Mac.
На macOS версии Mojave и выше больше нет возможности выполнять автоматизированный импорт данных Safari в Microsoft Edge без участия пользователя.

Начиная с Microsoft Edge версии 83, если для этой политики задано значение «FromMozillaFirefox», из Mozilla Firefox будут импортированы следующие типы данных:
1. Избранные или закладки
2. Сохраненные пароли
3. Адреса и другие сведения
4. История просмотров

Если вы хотите ограничить импорт определенных типов данных на управляемые устройства, вы можете использовать эту политику с другими политиками, такими как [ImportAutofillFormData](#importautofillformdata), [ImportBrowserSettings](#importbrowsersettings), [ImportFavorites](#importfavorites) и т. д.

Сопоставление параметров политики:

* FromDefaultBrowser (0) = Автоматически импортирует все поддерживаемые типы данных и настройки из браузера по умолчанию

* FromInternetExplorer (1) = Автоматически импортирует все поддерживаемые типы данных и настройки из Internet Explorer

* FromGoogleChrome (2) = Автоматически импортирует все поддерживаемые типы данных и настройки из Google Chrome

* FromSafari (3) = Автоматически импортирует все поддерживаемые типы данных и настройки из Safari

* DisabledAutoImport (4) = Отключает автоматический импорт, и раздел импорта при первом запуске пропускается

* FromMozillaFirefox (5) = Автоматически импортирует все поддерживаемые типы данных и настройки из Mozilla Firefox

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AutoImportAtFirstRun
  - Имя GP: Автоматически импортировать данные и настройки другого браузера при первом запуске
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AutoImportAtFirstRun
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: AutoImportAtFirstRun
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### AutoLaunchProtocolsFromOrigins

  #### Определять список протоколов, с помощью которых можно запустить внешнее приложение из списка источников без обращения к пользователю

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS — версия 85 или более поздние

  #### Описание

  Позволяет задать список протоколов (и для каждого протокола — связанный список разрешенных шаблонов происхождения), которые могут запускать внешнее приложение без обращения к пользователю. Протоколы должны включаться в список без конечных разделительных знаков. Например, должно быть указано "skype", а не "skype:" или "skype://".

Если эта политика настроена, протоколу будет разрешено запускать внешнее приложение без обращения к пользователю, только если:

- протокол указан в списке;

- происхождение сайта, запускающего протокол, соответствует шаблонам происхождения в списке allowed_origins этого протокола.

Если хотя бы одно из этих утверждений ложно, обращение к пользователю за разрешением запустить внешнее приложение не будет пропущено политикой.

Если не настроить эту политику, никакие протоколы не смогут запускать приложения без запроса. Пользователи могут отказаться от запросов для каждого протокола или каждого сайта, если политика [ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) не отключена. Эта политика не влияет на исключения, установленные пользователями в отношении отдельных протоколов или сайтов.

В шаблонах сопоставления источников используется тот же формат, что и для политики [URLBlocklist](#urlblocklist), задокументированный в [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Однако шаблоны сопоставления источников для этой политики не могут содержать элементы "/path" или "@query". Любой шаблон, содержащий элемент "/path" или "@query", будет проигнорирован.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Dictionary

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AutoLaunchProtocolsFromOrigins
  - Имя GP: Определять список протоколов, с помощью которых можно запустить внешнее приложение из списка источников без обращения к пользователю
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AutoLaunchProtocolsFromOrigins
  - Тип значения: REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\AutoLaunchProtocolsFromOrigins = [
  {
    "allowed_origins": [
      "example.com", 
      "http://www.example.com:8080"
    ], 
    "protocol": "spotify"
  }, 
  {
    "allowed_origins": [
      "https://example.com", 
      "https://.mail.example.com"
    ], 
    "protocol": "teams"
  }, 
  {
    "allowed_origins": [
      "*"
    ], 
    "protocol": "outlook"
  }
]
```

  ##### Компактный пример значения:

  ```
  SOFTWARE\Policies\Microsoft\Edge\AutoLaunchProtocolsFromOrigins = [{"allowed_origins": ["example.com", "http://www.example.com:8080"], "protocol": "spotify"}, {"allowed_origins": ["https://example.com", "https://.mail.example.com"], "protocol": "teams"}, {"allowed_origins": ["*"], "protocol": "outlook"}]
  ```
  

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AutoLaunchProtocolsFromOrigins
  - Пример значения:
``` xml
<key>AutoLaunchProtocolsFromOrigins</key>
<array>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>example.com</string>
      <string>http://www.example.com:8080</string>
    </array>
    <key>protocol</key>
    <string>spotify</string>
  </dict>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>https://example.com</string>
      <string>https://.mail.example.com</string>
    </array>
    <key>protocol</key>
    <string>teams</string>
  </dict>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>*</string>
    </array>
    <key>protocol</key>
    <string>outlook</string>
  </dict>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### AutoOpenAllowedForURLs

  #### URL-адреса, с которыми можно применять параметр AutoOpenFileTypes

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS — версия 85 или более поздние

  #### Описание

  Список URL-адресов, к которым будет применяться [AutoOpenFileTypes](#autoopenfiletypes). Эта политика не влияет на значения параметров автоматического открытия, установленные пользователями в пункте меню области загрузки... > "Всегда открывать файлы этого типа".

Если задать URL-адреса в этой политике, файлы будут автоматически открываться в соответствии с политикой только в том случае, если URL-адрес входит в указанный набор, а тип файла содержится в списке [AutoOpenFileTypes](#autoopenfiletypes). Если хотя бы одно из этих условий не выполнено, загруженный файл не будет автоматически открыт в соответствии с политикой.

Если не задать эту политику, все загружаемые файлы, тип которых содержится в [AutoOpenFileTypes](#autoopenfiletypes), будут автоматически открываться.

Шаблон URL-адреса должен быть иметь формат, соответствующий [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AutoOpenAllowedForURLs
  - Имя GP: URL-адреса, с которыми можно применять параметр AutoOpenFileTypes
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательно): SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = "example.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = ".exact.hostname.com"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AutoOpenAllowedForURLs
  - Пример значения:
``` xml
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### AutoOpenFileTypes

  #### Список типов файлов, которые должны автоматически открываться после скачивания

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS — версия 85 или более поздние

  #### Описание

  Эта политика задает список типов файлов, должны автоматически открываться после скачивания. Примечание. Типы файлов должны указываться без начальных разделителей, т.е. "txt", а не ".txt".

По умолчанию файлы этих типов будут открываться автоматически для всех URL-адресов. С помощью политики [AutoOpenAllowedForURLs](#autoopenallowedforurls) можно ограничить множество URL-адресов, для которых будут автоматически открываться файлы этих типов.

Файлы, которые должны открываться автоматически, все же будут проверяться фильтром SmartScreen в Microsoft Defender и при отрицательном результате проверки открываться не будут.

Файлы тех типов, которые пользователь указал для автоматического открытия, будут по-прежнему автоматически открываться после скачивания. Пользователь по-прежнему сможет указывать другие типы файлов, которые будут автоматически открываться.

Если эта политика не настроена, автоматически открываться будут только файлы тех типов, которые указал пользователь.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AutoOpenFileTypes
  - Имя GP: Список типов файлов, которые должны автоматически открываться после скачивания
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательно): SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = "exe"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = "txt"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AutoOpenFileTypes
  - Пример значения:
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### AutofillAddressEnabled

  #### Включить автозаполнение для адресов

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Включает функцию автозаполнения и позволяет пользователям автоматически заполнять адресную информацию в веб-формах, используя ранее сохраненную информацию.

Если вы отключите эту политику, автозаполнение никогда не предлагает и не вводит информацию об адресе, а также не сохраняет дополнительную информацию об адресе, которую пользователь может предоставить при просмотре веб-страниц.

Если вы включите эту политику или не настроите ее, пользователи смогут управлять автозаполнением для адресов в пользовательском интерфейсе.

Обратите внимание, что если вы отключите эту политику, вы также прекратите все действия для всех веб-форм, кроме форм оплаты и пароля. Дальнейшие записи не сохраняются, и Microsoft Edge не будет предлагать или автоматический заполнять любые предыдущие записи.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AutofillAddressEnabled
  - Имя GP: Включить автозаполнение для адресов
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: AutofillAddressEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AutofillAddressEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### AutofillCreditCardEnabled

  #### Включить автозаполнение для кредитных карт

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Включите функцию автозаполнения Microsoft Edge и позволяет пользователям автоматически заполнять данные кредитной карты в веб-формах, используя ранее сохраненную информацию.

Если вы отключите эту политику, автозаполнение никогда не будет предлагать или заполнять информацию о кредитной карте, а также не будет сохранять дополнительную информацию о кредитной карте, которую пользователи могут отправлять при просмотре веб-страниц.

Если вы включите эту политику или не настроите ее, пользователи смогут управлять автозаполнением для кредитных карт.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: AutofillCreditCardEnabled
  - Название GP: Включить автозаполнение для кредитных карт
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: AutofillCreditCardEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AutofillCreditCardEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### AutoplayAllowed

  #### Разрешить автозапуск мультимедиа для веб-сайтов

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 78 и более поздних версий

  #### Описание

  Эта политика устанавливает политику автозапуска мультимедиа для веб-сайтов.

Параметр по умолчанию «Не настроена» учитывает текущие параметры автозапуска мультимедиа и позволяет пользователям настраивать свои параметры автозапуска.

Установка на «Включен» устанавливает автозапуск медиа на «Разрешить».  Все веб-сайты могут автоматически воспроизводить мультимедиа. Пользователи не могут переопределить эту политику.

Установка на «Отключено» устанавливает автозапуск медиа на «Блокировать».  Никакие веб-сайты не могут автоматически воспроизводить мультимедиа. Пользователи не могут переопределить эту политику.

Чтобы эта политика вступила в силу, необходимо закрыть и открыть заново вкладку.


  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - GP уникальное имя: AutoplayAllowed
  - Название GP: Разрешить автозапуск мультимедиа для сайтов
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: AutoplayAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: AutoplayAllowed
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### BackgroundModeEnabled

  #### Продолжить запуск фоновых приложений после закрытия Microsoft Edge

  
  
  #### Поддерживаемые версии:

  - В Windows с 77 и более поздних версий

  #### Описание

  Позволяет запускать процессы Microsoft Edge при входе в ОС и продолжать работу после закрытия последнего окна браузера. В этом случае фоновые приложения и текущий сеанс просмотра остаются активными, включая любые сеансовые файлы cookie. Открытый фоновый процесс отображает значок в системной панели и всегда может быть закрыт оттуда.

Если вы включите эту политику, фоновый режим включен.

Если вы отключите эту политику, фоновый режим отключится.

Если вы не настроите эту политику, фоновый режим первоначально отключен, и пользователь может настроить его поведение в edge://settings/system.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: BackgroundModeEnabled
  - Имя GP: Продолжить запуск фоновых приложений после закрытия Microsoft Edge
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: BackgroundModeEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### BackgroundTemplateListUpdatesEnabled

  #### Включает фоновые обновления в списке доступных шаблонов для коллекций и других функций, которые используют шаблоны

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 79 или позже

  #### Описание

  Позволяет включать или отключать фоновые обновления в списке доступных шаблонов для коллекций и других функций, которые используют шаблоны.  Шаблоны используются для извлечения расширенных метаданных с веб-страницы, когда страница сохраняется в коллекции.

Если этот параметр включен или параметр не настроен, список доступных шаблонов будет загружаться в фоновом режиме из службы Microsoft каждые 24 часа.

Если этот параметр отключен, список доступных шаблонов будет загружаться по запросу. Этот тип загрузки может привести к небольшим потерям производительности для коллекций и других функций.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: BackgroundTemplateListUpdatesEnabled
  - Имя GP: Включение фоновых обновлений в списке доступных шаблонов для коллекций и других функций, которые используют шаблоны
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: BackgroundTemplateListUpdatesEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: BackgroundTemplateListUpdatesEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### BingAdsSuppression

  #### Блокировать все объявления в результатах поиска Bing

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 83 и более поздних версий

  #### Описание

  Включает поиск без рекламы на Bing.com

Если вы включите эту политику, то пользователь сможет выполнять поиск на bing.com и пользоваться поиском без рекламы. В то же время для параметра безопасного поиска будет установлено значение «Строгий», и пользователь не сможет его изменить.

Если вы не настроите эту политику, в результатах поиска по умолчанию на bing.com появятся объявления. По умолчанию SafeSearch будет установлен на «Умеренный» и может быть изменен пользователем.

Эта политика доступна только для SKU K-12, которые определены Microsoft как арендаторы EDU.

Пожалуйста, обратитесь к [https://go.microsoft.com/fwlink/?linkid=2119711](https://go.microsoft.com/fwlink/?linkid=2119711), чтобы узнать больше об этой политике или если к вам применимы следующие сценарии:

* У вас есть клиент EDU, но политика не работает.

* Ваш IP-адрес внесен в список разрешенных в связи с наличием возможностей поиска без рекламы.

* Вы пользовались возможностями поиска без рекламы в устаревшей версии Microsoft Edge и хотите обновить браузер до новой версии.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: BingAdsSuppression
  - Название GP: Заблокировать все объявления в результатах поиска Bing
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: BingAdsSuppression
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: BingAdsSuppression
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### BlockThirdPartyCookies

  #### Блокировка сторонних cookie-файлов

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Блокировать элементы веб-страницы, которые не принадлежат домену, который находится в адресной строке, от настройки файлов cookie.

Если вы включите эту политику, элементы веб-страницы, которые не принадлежат домену, который находится в адресной строке, не могут устанавливать файлы cookie

Если вы отключите эту политику, элементы веб-страниц из доменов, отличных от адресной строки, могут устанавливать файлы cookie.

Если вы не настроите эту политику, сторонние файлы cookie будут включены, но пользователи могут изменить этот параметр.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: BlockThirdPartyCookies
  - Название GP: Блокировать сторонние куки
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: BlockThirdPartyCookies
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: BlockThirdPartyCookies
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### BrowserAddProfileEnabled

  #### Включите создание профиля из всплывающего меню Identity или страницы настроек.

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет пользователям создавать новые профили, используя опцию **Добавить профиль**.
Если вы включите эту политику или не настроите ее, Microsoft Edge позволит пользователям использовать **Добавить профиль** во всплывающем меню «Идентичность» или на странице «Настройки» для создания новых профилей.

Если вы отключите эту политику, пользователи не смогут добавлять новые профили из всплывающего меню Identity или страницы настроек.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: BrowserAddProfileEnabled
  - Имя GP: Включить создание профиля из всплывающего меню Удостоверение или страницы настроек.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: BrowserAddProfileEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: BrowserAddProfileEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### BrowserGuestModeEnabled

  #### Включить гостевой режим

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Включите эту опцию, чтобы разрешить использование гостевых профилей в Microsoft Edge. В гостевом профиле браузер не импортирует данные просмотра из существующих профилей и удаляет данные просмотра, когда все гостевые профили закрыты.

Если вы включите эту политику или не настроите ее, Microsoft Edge позволит пользователям просматривать гостевые профили.

Если вы отключите эту политику, Microsoft Edge не позволит пользователям просматривать гостевые профили.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: BrowserGuestModeEnabled
  - Имя GP: Включить гостевой режим
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: BrowserGuestModeEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: BrowserGuestModeEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### BrowserNetworkTimeQueriesEnabled

  #### Разрешить запросы к службе сетевого времени браузера

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Запрещает Microsoft Edge периодически отправлять запросы в службу сетевого времени браузера для получения точной метки времени.

Если вы отключите эту политику, Microsoft Edge прекратит отправку запросов в службу сетевого времени браузера.

Если вы включите эту политику или не настроите ее, Microsoft Edge будет время от времени отправлять запросы в службу сетевого времени браузера.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: BrowserNetworkTimeQueriesEnabled
  - Имя GP: Разрешить запросы к службе сетевого времени браузера.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: BrowserNetworkTimeQueriesEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: BrowserNetworkTimeQueriesEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### BrowserSignin

  #### Настройки входа в браузер

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Укажите, может ли пользователь войти в Microsoft Edge со своей учетной записью и использовать связанные с учетной записью службы, такие как синхронизация и единый вход. Чтобы контролировать доступность синхронизации, используйте вместо этого политику [SyncDisabled](#syncdisabled).

Если для этой политики установлено значение «Отключить», убедитесь, что вы также отключили политику [NonRemovableProfileEnabled](#nonremovableprofileenabled), поскольку [NonRemovableProfileEnabled](#nonremovableprofileenabled)отключает создание автоматически подписанного в профиле браузера. Если установлены обе политики, Microsoft Edge будет использовать политику «Отключить вход в браузер» и будет вести себя так, как будто для [NonRemovableProfileEnabled](#nonremovableprofileenabled) установлено значение «отключено».

Если для этой политики установлено значение «Enable», пользователи могут войти в профиль, чтобы использовать браузер. Вход в браузер не означает, что синхронизация включена по умолчанию; пользователь должен отдельно подписаться на использование этой функции.

Если для этой политики установлено значение «Force», пользователи должны войти в профиль, чтобы использовать браузер. По умолчанию это позволит пользователю выбирать, хотят ли они синхронизировать свою учетную запись, если только синхронизация не отключена администратором домена или с помощью политики [SyncDisabled](#syncdisabled). Значение по умолчанию политики [BrowserGuestModeEnabled](#browserguestmodeenabled)установлено как false.

Если вы не настроите эту политику, пользователи могут решить, хотят ли они включить опцию входа в браузер, и использовать ее по своему усмотрению.

Сопоставление параметров политики:

* Disable (0)= Отключить вход в браузер

* Enable (1) = Включить вход в браузер

* Force (2) = Пользователи должны войти в систему, чтобы использовать браузер

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - GP уникальное имя: BrowserSignin
  - Имя GP: Настройки входа в браузер
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: BrowserSignin
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: BrowserSignin
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### BrowsingDataLifetime

  #### Параметры времени существования данных браузера

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с версии 89 или более поздней

  #### Описание

  Настраивает параметры времени существования данных браузера для Microsoft Edge.
Эта политика управляет временем существования выбранных данных браузера. Эта политика не действует, если включена синхронизация.
Доступные типы данных: browsing_history, download_history, cookies_and_other_site_data, cached_images_and_files, password_signin, autofill, site_settings и hosted_app_data.
Microsoft Edge регулярно удаляет данные выбранных типов, которые старше time_to_live_in_hours. Так как удаление данных происходит только через определенные интервалы, некоторые данные могут храниться немного дольше, при этом никогда не превышая time_to_live_in_hours более чем в два раза.


  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Dictionary

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: BrowsingDataLifetime
  - Имя групповой политики: параметры времени существования данных браузера
  - Путь к групповой политике (обязательно): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): Н/Д
  - Имя значения: BrowsingDataLifetime
  - Тип значения: REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\BrowsingDataLifetime = [
  {
    "data_types": [
      "browsing_history"
    ], 
    "time_to_live_in_hours": 24
  }, 
  {
    "data_types": [
      "password_signin", 
      "autofill"
    ], 
    "time_to_live_in_hours": 12
  }
]
```

  ##### Компактный пример значения:

  ```
  SOFTWARE\Policies\Microsoft\Edge\BrowsingDataLifetime = [{"data_types": ["browsing_history"], "time_to_live_in_hours": 24}, {"data_types": ["password_signin", "autofill"], "time_to_live_in_hours": 12}]
  ```
  

  #### Сведения о Mac и параметры
  
  - Имя ключа предпочтения: BrowsingDataLifetime
  - Пример значения:
``` xml
<key>BrowsingDataLifetime</key>
<array>
  <dict>
    <key>data_types</key>
    <array>
      <string>browsing_history</string>
    </array>
    <key>time_to_live_in_hours</key>
    <integer>24</integer>
  </dict>
  <dict>
    <key>data_types</key>
    <array>
      <string>password_signin</string>
      <string>autofill</string>
    </array>
    <key>time_to_live_in_hours</key>
    <integer>12</integer>
  </dict>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### BuiltInDnsClientEnabled

  #### Используйте встроенный DNS-клиент

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определяет, использовать ли встроенный DNS-клиент.

Эта политика управляет программным стеком, используемым для связи с DNS-сервером: DNS-клиентом операционной системы или встроенным DNS-клиентом Microsoft Edge. Эта политика не влияет на то, какие DNS-серверы используются: например, если операционная система настроена на использование корпоративного DNS-сервера, этот же сервер будет использоваться встроенным DNS-клиентом. Она также не управляет тем, используется ли DNS поверх HTTPS; Microsoft Edge всегда использует встроенный сопоставитель для запросов DNS поверх HTTPS. Сведения об управлении DNS поверх HTTPS см. в политике [DnsOverHttpsMode](#dnsoverhttpsmode).

При включении этой политики будет использоваться встроенный DNS-клиент, если он доступен.

Если отключить эту политику, встроенный DNS-клиент будет использоваться только при применении DNS поверх HTTPS.

Если вы не настроили эту политику, встроенный DNS-клиент включен по умолчанию.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: BuiltInDnsClientEnabled
  - Имя GP: Использовать встроенный DNS-клиент
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: BuiltInDnsClientEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: BuiltInDnsClientEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### BuiltinCertificateVerifierEnabled

  #### Определяет, будет ли встроенный верификатор сертификатов использоваться для проверки сертификатов сервера (не рекомендуется)

  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:

  - MacOS с 83 и более поздних версий

  #### Описание

  Эта политика устарела, так как она предназначена для использования только в качестве краткосрочного механизма, чтобы предоставить предприятиям больше времени для обновления своих сред и сообщения о проблемах, если они окажутся несовместимы со встроенным средством проверки сертификатов.

Она не будет работать в Microsoft Edge версии 87 при планируемом удалении устаревшего средства проверки сертификатов в Mac OS X.


  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: BuiltinCertificateVerifierEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForCas

  #### Отключите принудительное использование прозрачности сертификата для списка хэшей subjectPublicKeyInfo

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Отключает применение требований прозрачности сертификата для списка хэшей subjectPublicKeyInfo.

Эта политика позволяет отключить требования раскрытия информации о прозрачности сертификатов для цепочек сертификатов, которые содержат сертификаты с одним из указанных хэшей subjectPublicKeyInfo. Это позволяет сертификатам, которые в противном случае были бы ненадежными, поскольку они не были должным образом обнародованы, по-прежнему использоваться для узлов Enterprise.

Чтобы отключить принудительное использование прозрачности сертификатов, когда установлена эта политика, должен быть выполнен один из следующих наборов условий:
1. Хеш имеет имя субъекта сертификата сервера PublicKeyInfo.
2. Хэш имеет значение subjectPublicKeyInfo, которое появляется в сертификате CA в цепочке сертификатов, этот сертификат CA ограничен расширением nameConstraints X.509v3, одно или несколько directoryName nameConstraints присутствуют в allowSubtrees, а directoryName содержит атрибут organizationName.
3. Хэш имеет значение subjectPublicKeyInfo, которое отображается в сертификате CA в цепочке сертификатов, сертификат CA имеет один или несколько атрибутов organizationName в теме сертификата, а сертификат сервера содержит такое же количество атрибутов organizationName, в том же порядке и с байтовые идентичные значения.

Хэш subjectPublicKeyInfo указывается путем объединения имени алгоритма хеширования, символа "/" и кодирования Base64 этого алгоритма хеширования, применяемого к DER-кодированному subjectPublicKeyInfo указанного сертификата. Эта кодировка Base64 имеет тот же формат, что и отпечаток SPKI, как определено в RFC 7469, раздел 2.4. Нераспознанные алгоритмы хеширования игнорируются. Единственный поддерживаемый алгоритм хеширования на данный момент это "sha256".

Если вы отключите эту политику или не настроите ее, любой сертификат, который требуется раскрыть через прозрачность сертификата, будет считаться ненадежным, если он не раскрыт в соответствии с политикой прозрачности сертификата.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: CertificateTransparencyEnforcementDisabledForCas
  - Имя GP: Отключить применение прозрачности сертификата для списка хэшей subjectPublicKeyInfo
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = "sha256//////////////////////w=="

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: CertificateTransparencyEnforcementDisabledForCas
  - Пример значения:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForLegacyCas

  #### Отключите принудительное использование прозрачности сертификатов для списка устаревших центров сертификации

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Отключает применение требований прозрачности сертификатов для списка устаревших центров сертификации (Cas).

Эта политика позволяет отключить требования раскрытия информации о прозрачности сертификатов для цепочек сертификатов, которые содержат сертификаты с одним из указанных хэшей subjectPublicKeyInfo. Это позволяет сертификатам, которые в противном случае были бы ненадежными, поскольку они не были должным образом обнародованы, продолжают использоваться для корпоративных хостов.

Чтобы отключить принудительное использование прозрачности сертификатов, необходимо установить для хэша значение subjectPublicKeyInfo, отображаемое в сертификате CA, который распознается как устаревший центр сертификации (CA). Устаревший ЦС - это ЦС, который по умолчанию является публично доверенным в одной или нескольких операционных системах, поддерживаемых Microsoft Edge.

Вы указываете хэш subjectPublicKeyInfo, объединяя имя алгоритма хеширования, символ "/" и кодировку Base64 этого алгоритма хэширования, примененного к DER-кодированному subjectPublicKeyInfo указанного сертификата. Эта кодировка Base64 имеет тот же формат, что и отпечаток SPKI, как определено в RFC 7469, раздел 2.4. Нераспознанные алгоритмы хеширования игнорируются. Единственный поддерживаемый алгоритм хеширования на данный момент это "sha256".

Если вы не настроите эту политику, любой сертификат, который требуется раскрыть через прозрачность сертификата, будет считаться ненадежным, если он не раскрыт в соответствии с политикой прозрачности сертификата.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Имя GP: Отключите принудительное использование прозрачности сертификата для списка устаревших центров сертификации.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = "sha256//////////////////////w=="

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Пример значения:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForUrls

  #### Отключить принудительное использование прозрачности сертификатов для определенных URL-адресов

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Отключает применение требований прозрачности сертификатов для указанных URL-адресов.

Эта политика позволяет не раскрывать сертификаты для имен хостов в указанных URL-адресах через прозрачность сертификатов. Это позволяет вам использовать сертификаты, которые в противном случае были бы ненадежными, поскольку они не были должным образом обнародованы, но затрудняло обнаружение неправильно выданных сертификатов для этих хостов.

Сформируйте ваш шаблон URL в соответствии с [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Поскольку сертификаты действительны для данного имени хоста, независимо от схемы, порта или пути, рассматривается только часть имени хоста в URL. Подстановочные хосты не поддерживаются.

Если вы не настроите эту политику, любой сертификат, который должен быть раскрыт через прозрачность сертификата, считается ненадежным, если он не раскрыт.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: CertificateTransparencyEnforcementDisabledForUrls
  - Имя GP: Отключить принудительное использование прозрачности сертификата для определенных URL
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = ".contoso.com"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: CertificateTransparencyEnforcementDisabledForUrls
  - Пример значения:
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### ClearBrowsingDataOnExit

  #### Очистить данные браузера при закрытии Microsoft Edge

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 78 и более поздних версий

  #### Описание

  Microsoft Edge не очищает данные просмотра по умолчанию при закрытии. Данные для просмотра включают информацию, введенную в формах, паролях и даже посещенных веб-сайтах.

Если вы включите эту политику, все данные о просмотре будут удаляться при каждом закрытии Microsoft Edge. Обратите внимание, что если вы включите эту политику, она будет иметь приоритет над тем, как вы настроили [DefaultCookiesSetting](#defaultcookiessetting)

Если вы отключите или не настроите эту политику, пользователи могут настроить параметр Очистить данные просмотра в Настройках.

Если вы включите эту политику, не настраивайте политику [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) или [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit), поскольку все они имеют дело с удалением данных просмотра. Если вы настраиваете предыдущие политики и эту политику, все данные просмотра удаляются при закрытии Microsoft Edge независимо от того, как вы настроили [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) или [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

Чтобы исключить удаление файлов cookie при выходе, настройте политику [SaveCookiesOnExit](#savecookiesonexit).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ClearBrowsingDataOnExit
  - Имя GP: Очистить данные просмотра при закрытии Microsoft Edge
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ClearBrowsingDataOnExit
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ClearBrowsingDataOnExit
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ClearCachedImagesAndFilesOnExit

  #### Очистить кэшированные изображения и файлы при закрытии Microsoft Edge

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 83 и более поздних версий

  #### Описание

  Microsoft Edge не очищает кэшированные изображения и файлы по умолчанию при закрытии.

Если вы включите эту политику, кэшированные изображения и файлы будут удаляться при каждом закрытии Microsoft Edge.

Если вы отключите эту политику, пользователи не смогут настроить параметр кэшированных изображений и файлов в edge://settings/clearBrowsingDataOnClose.

Если вы не настроите эту политику, пользователи могут выбрать, будут ли очищенные кэшированные изображения и файлы очищаться при выходе.

Если вы отключите эту политику, не включайте политику [ClearBrowsingDataOnExit](#clearbrowsingdataonexit), потому что они обе имеют дело с удалением данных. Если вы настраиваете оба, политика [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) имеет приоритет и удаляет все данные, когда Microsoft Edge закрывается, независимо от того, как вы настроили [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ClearCachedImagesAndFilesOnExit
  - Имя GP: Очистить кэшированные изображения и файлы при закрытии Microsoft Edge
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ClearCachedImagesAndFilesOnExit
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ClearCachedImagesAndFilesOnExit
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ClickOnceEnabled

  #### Разрешить пользователям открывать файлы с использованием протокола ClickOnce

  
  
  #### Поддерживаемые версии:

  - В Windows с 78 и более поздних версий

  #### Описание

  Разрешить пользователям открывать файлы с использованием протокола ClickOnce. Протокол ClickOnce позволяет веб-сайтам запрашивать, чтобы браузер открывал файлы с определенного URL-адреса, используя обработчик файлов ClickOnce на компьютере или устройстве пользователя.

Если вы включите эту политику, пользователи смогут открывать файлы, используя протокол ClickOnce. Эта политика переопределяет параметр ClickOnce пользователя на странице edge://flags/.

Если вы отключите эту политику, пользователи не смогут открывать файлы, используя протокол ClickOnce. Вместо этого файл будет сохранен в файловой системе с помощью браузера. Эта политика переопределяет параметр ClickOnce пользователя на странице edge://flags/.

Если эта политика не настроена, пользователи, которые используют Microsoft Edge до версии 87, не смогут по умолчанию открывать файлы с помощью протокола ClickOnce. Тем не менее пользователям доступен параметр, позволяющий разрешить использование протокола ClickOnce на странице edge://flags/. Начиная с Microsoft Edge версии 87, пользователи, могут открывать файлы по умолчанию с помощью протокола ClickOnce, но также могут отключить протокол ClickOnce на странице edge://flags/.

Отключение ClickOnce может помешать правильному запуску приложений ClickOnce (файлов приложений).

Для получения дополнительной информации о ClickOnce, см. [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) и [https://go.microsoft.com/fwlink/?linkid=2099880](https://go.microsoft.com/fwlink/?linkid=2099880).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ClickOnceEnabled
  - Имя GP: Разрешить пользователям открывать файлы по протоколу ClickOnce.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ClickOnceEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  

  [В начало](#microsoft-edge---policies)

  ### CollectionsServicesAndExportsBlockList

  #### Блокировка доступа к указанному списку служб и целевым объектам экспорта в Коллекциях

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  Перечислите конкретные службы и целевые объекты экспорта, которые будут недоступны пользователям при использовании функции Коллекций в Microsoft Edge. Это включает отображение дополнительных данных из Bing и экспорт коллекций в продукты Майкрософт или внешних партнеров.

Если включить эту политику, блокируются службы и целевые объекты экспорта, соответствующие указанному списку.

Если вы не настроите эту политику, ограничения на допустимые службы и целевые объекты экспорта не применяются.

Сопоставление параметров политики:

* pinterest_suggestions (pinterest_suggestions) = предложения Pinterest

* collections_share (collections_share) = предоставление общего доступа к коллекциям

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: CollectionsServicesAndExportsBlockList
  - Имя GP: Блокировка доступа к указанному списку служб и целевым объектам экспорта в Коллекциях
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = "pinterest_suggestions"
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\2 = "collections_share"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: CollectionsServicesAndExportsBlockList
  - Пример значения:
``` xml
<array>
  <string>pinterest_suggestions</string>
  <string>collections_share</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### CommandLineFlagSecurityWarningsEnabled

  #### Включить предупреждения безопасности для флагов командной строки

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 78 и более поздних версий

  #### Описание

  Если этот параметр отключен, эта политика предотвращает появление предупреждений безопасности при запуске Microsoft Edge с потенциально опасными флагами командной строки.

Если включено или не установлено, предупреждения безопасности отображаются, когда эти флаги командной строки используются для запуска Microsoft Edge.

Например, флаг --disable-gpu-sandbox генерирует это предупреждение: вы используете неподдерживаемый флаг командной строки: --disable-gpu-sandbox. Это создает угрозу стабильности и безопасности.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: CommandLineFlagSecurityWarningsEnabled
  - Имя GP: Включить предупреждения безопасности для флагов командной строки
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: CommandLineFlagSecurityWarningsEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: CommandLineFlagSecurityWarningsEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ComponentUpdatesEnabled

  #### Включить обновления компонентов в Microsoft Edge

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Если вы включите или не настроите эту политику, обновления компонентов будут включены в Microsoft Edge.

Если вы отключите эту политику или зададите значение false, обновления компонентов будут отключены для всех компонентов в Microsoft Edge.

Однако некоторые компоненты освобождаются от этой политики. Это включает в себя любой компонент, который не содержит исполняемого кода, который существенно не изменяет поведение браузера или является критически важным для безопасности. То есть обновления, которые считаются «критическими для безопасности», все еще применяются, даже если вы отключите эту политику.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ComponentUpdatesEnabled
  - Имя GP: Включить обновления компонентов в Microsoft Edge
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ComponentUpdatesEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ComponentUpdatesEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ConfigureDoNotTrack

  #### Настройка запрета на отслеживание

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Укажите, следует ли отправлять запросы «Не отслеживать» на веб-сайты, которые запрашивают информацию для отслеживания. Запросы «Не отслеживать» позволяют веб-сайтам, которые вы посещаете, знать, что вы не хотите, чтобы ваши действия по просмотру отслеживались. По умолчанию Microsoft Edge не отправляет запросы «Не отслеживать», но пользователи могут включить эту функцию для их отправки.

Если вы включите эту политику, запросы «Не отслеживать» всегда отправляются на веб-сайты, запрашивающие информацию для отслеживания.

Если вы отключите эту политику, запросы никогда не будут отправлены.

Если вы не настроите эту политику, пользователи могут выбрать, следует ли отправлять эти запросы.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ConfigureDoNotTrack
  - Имя GP: Настройка "не отслеживать"
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ConfigureDoNotTrack
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: ConfigureDoNotTrack
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ConfigureFriendlyURLFormat

  #### Настройка формата по умолчанию для URL-адресов, скопированных из Microsoft Edge, и определение доступности пользователям дополнительных форматов

  
  
  #### Поддерживаемые версии:

  - В Windows 87 и более поздних версий
  - MacOS с 88 и более поздних версий

  #### Описание

  При включенной функции FriendlyURLs, Microsoft Edge вычисляет дополнительные представления URL-адреса и размещает их в буфере обмена.

Эта политика определяет, какой формат будет вставлен при вставке пользователя во внешние приложения или в Microsoft Edge без элемента контекстного меню "Вставить как".

Если параметр настроен, политика позволяет выбрать от лица пользователя. Параметры в edge://settings/shareCopyPaste будут неактивны, а параметры в контекстном меню "Вставить как" – недоступны.

* Не настроено = Пользователь может выбирать предпочитаемый формат вставки. По умолчанию используется удобный формат URL-адреса. Меню "Вставить как" будет доступно в Microsoft Edge.

* 1 = Дополнительные форматы в буфере обмена не сохраняются. В Microsoft Edge не будет элемента контекстного меню "Вставить как", а для вставки будет использоваться формат обычного текста URL-адреса. В результате функция удобного URL-адреса будет отключена.

* 3 = Пользователь получает удобный URL-адрес при вставке в поверхности, принимающие форматируемый текст. Обычный URL-адрес будет доступен для поверхностей без возможности форматирования. Меню "Вставить как" будет недоступно в Microsoft Edge.

* 4 = (На данный момент не используется)

Расширенные форматы могут не поддерживаться в некоторых местах вставки и (или) на веб-сайтах. Таким образом, чтобы настроить эту политику, рекомендуется использовать параметр "Обычный URL-адрес".

Сопоставление параметров политики:

* PlainText (1) = Обычный URL-адрес без дополнительных сведений, например заголовок страницы. Рекомендуется, если этот параметр настроен. Дополнительные сведения см. в описании.

* TitledHyperlink (3) = Гиперссылка с именем: Гиперссылка, указывающая на скопированный URL-адрес, видимый текст которого — это заголовок конечной страницы. Это удобный формат URL-адреса.

* WebPreview (4) = Ожидается в ближайшее время. Если настроено, функционирует как "Обычный URL-адрес".

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ConfigureFriendlyURLFormat
  - Имя GP: Настройка формата по умолчанию для URL-адресов, скопированных из Microsoft Edge, и определение доступности пользователям дополнительных форматов
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ConfigureFriendlyURLFormat
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000003
```

  #### Информация о Mac и настройки
  
  - Имя ключа настройки: ConfigureFriendlyURLFormat
  - Пример значения:
``` xml
<integer>3</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### ConfigureOnPremisesAccountAutoSignIn

  #### Настройте автоматический вход с учетной записью домена Active Directory, если учетная запись домена Azure AD отсутствует

  
  
  #### Поддерживаемые версии:

  - В Windows с 81 и более поздних версий

  #### Описание

  Включите использование учетных записей Active Directory для автоматического входа, если компьютеры ваших пользователей подключены к домену, а ваша среда не является гибридной. Если вы хотите, чтобы пользователи автоматически входили в свои учетные записи Azure Active Directory, присоединитесь к Azure AD (Дополнительные сведения см. в статье [https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197)) или гибридному (Дополнительные сведения см. в статье [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365).) свою среду.

При каждом запуске Microsoft Edge будет пытаться выполнить вход, используя эту политику, если первый профиль не вошел в систему или не вошел в систему автоматически ранее.

Если вы отключили политику [BrowserSignin](#browsersignin), эта политика не будет действовать.

Если вы включите эту политику и зададите для нее значение «SignInAndMakeDomainAccountNonRemovable», Microsoft Edge автоматически выполнит вход в систему пользователей, которые находятся на компьютерах, подключенных к домену, с использованием их учетных записей Active Directory.

Если для этой политики установлено значение «Disabled» или она не настроена, Microsoft Edge не будет автоматически входить в систему пользователей, которые находятся на компьютерах, подключенных к домену с помощью учетных записей Active Directory.

Начиная с Microsoft Edge 89 и далее, если существует  локальный профиль пользователя с отключенной синхронизацией, а компьютер гибриден, то у него есть учетная запись Azure AD; она автоматически обновит локальный профиль до профиля Azure AD, чтобы получить полный набор функций синхронизации Azure AD.

Сопоставление параметров политики:

* Disabled (0) = отключено

* SignInAndMakeDomainAccountNonRemovable (1) = Войти и сделать учетную запись домена неудаляемой

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ConfigureOnPremisesAccountAutoSignIn
  - Имя GP: Настроить автоматический вход с учетной записью домена Active Directory, если учетная запись домена Azure AD отсутствует
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ConfigureOnPremisesAccountAutoSignIn
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  

  [В начало](#microsoft-edge---policies)

  ### ConfigureOnlineTextToSpeech

  #### Настроить онлайн текст в речь

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Укажите, можно ли использовать в браузере текст из Интернета для голосовых шрифтов, входящих в состав служб Azure. Эти голосовые шрифты более высокого качества, чем предустановленные системные голосовые шрифты.

Если вы включите или не настроите эту политику, в веб-приложениях, использующих API SpeechSynthesis, можно использовать текст из Интернета в голосовые шрифты.

Если вы отключите эту политику, голосовые шрифты будут недоступны.

Подробнее об этой функции читайте здесь: SpeechSynthesis API: [https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038) Cognitive Services: [https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ConfigureOnlineTextToSpeech
  - Название GP: Настройка онлайн-текста в речь
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ConfigureOnlineTextToSpeech
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ConfigureOnlineTextToSpeech
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ConfigureShare

  #### Настройте обмен опытом

  
  
  #### Поддерживаемые версии:

  - На Windows с 83 и более поздних версий

  #### Описание

  Если вы установите для этой политики значение «ShareAllowed» (по умолчанию), пользователи смогут получить доступ к интерфейсу «Общий доступ Windows 10» из меню «Параметры» и «Больше» в Microsoft Edge, чтобы поделиться им с другими приложениями в системе.

Если вы установите эту политику в «ShareDisallowed», пользователи не смогут получить доступ к Windows 10 Share. Если кнопка «Поделиться» находится на панели инструментов, она также будет скрыта.

Сопоставление параметров политики:

* ShareAllowed (0) = Разрешить использование обмена опытом

* ShareDisallowed (1) = Не разрешать использовать обмена опытом

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ConfigureShare
  - Имя участника: Настройте обмен опытом
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ConfigureShare
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### CustomHelpLink

  #### Укажите пользовательскую ссылку справки

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 79 или позже

  #### Описание

  Укажите ссылку для меню «Справка» или клавишу F1.

Если вы включите эту политику, администратор может указать ссылку для меню Справка или клавишу F1.

Если вы отключите или не настроите эту политику, будет использоваться ссылка по умолчанию для меню справки или клавиши F1.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: CustomHelpLink
  - Имя GP: Укажите пользовательскую ссылку справки
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: CustomHelpLink
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"https://go.microsoft.com/fwlink/?linkid=2080734"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: CustomHelpLink
  - Пример значения:
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### DNSInterceptionChecksEnabled

  #### Проверка перехвата DNS включена

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 80 или позже

  #### Описание

  Эта политика настраивает локальный коммутатор, который можно использовать для отключения проверки перехвата DNS. Эти проверки пытаются определить, находится ли браузер за прокси-сервером, который перенаправляет неизвестные имена хостов.

Это обнаружение может не потребоваться в корпоративной среде, где известна конфигурация сети. Его можно отключить, чтобы избежать дополнительного трафика DNS и HTTP при запуске и при каждом изменении конфигурации DNS.

Если вы включили эту политику или не настроили ее, то выполняется проверка перехвата DNS.

Если вы отключили эту политику, то проверка перехвата DNS не выполняется.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DNSInterceptionChecksEnabled
  - Имя GP: Включена проверка перехвата DNS
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DNSInterceptionChecksEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DNSInterceptionChecksEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultBrowserSettingEnabled

  #### Установите Microsoft Edge в качестве браузера по умолчанию

  
  
  #### Поддерживаемые версии:

  - В Windows 7 и macOS с 77 и более поздних версий

  #### Описание

  Если для этой политики задано значение "истина", Microsoft Edge всегда будет проверять при запуске, является ли он браузером по умолчанию, и, если это возможно, автоматически регистрироваться.

Если для этой политики задано значение "ложь", Microsoft Edge никогда не будет проверять, является ли он браузером по умолчанию, и пользовательские элементы управления этим параметром будут отключены.

Если эта политика не задана, пользователи смогут разрешить Microsoft Edge проверять, является ли он браузером по умолчанию, и включить отправку пользователю уведомления при отрицательном результате этой проверки.

Примечание для администраторов Windows: эта политика работает только на ПК под управлением Windows 7. Для более поздних версий Windows необходимо развернуть файл «ассоциации приложений по умолчанию», который делает Microsoft Edge обработчиком протоколов https и http (и, необязательно, протокол ftp и форматы файлов, такие как .html, .htm, .pdf, .svg, .webp). Дополнительные сведения см. в статье [https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultBrowserSettingEnabled
  - Имя GP: Установить Microsoft Edge в качестве браузера по умолчанию
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultBrowserSettingEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultBrowserSettingEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultSearchProviderContextMenuAccessAllowed

  #### Разрешить доступ к службе поиска по умолчанию в контекстном меню

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS — версия 85 или более поздние

  #### Описание

  Включает использование службы поиска по умолчанию в контекстном меню.

Если для этой политики выбрано значение отключено, элемент контекстного меню поиска, который использует поиск по умолчанию, а также боковая панель поиска доступны не будут.

Если для этой политики выбрано значение включено или оно не задано, элемент контекстного меню для поиска по умолчанию, а также боковая панель поиска будут доступны.

Значение политики используется, только если политика [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) включена, в других случаях оно не применяется.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DefaultSearchProviderContextMenuAccessAllowed
  - Имя GP: Разрешить доступ к службе поиска по умолчанию в контекстном меню
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultSearchProviderContextMenuAccessAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: DefaultSearchProviderContextMenuAccessAllowed
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultSensorsSetting

  #### Стандартный параметр для датчиков

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  Укажите, могут ли веб-сайты получать доступ к датчикам, например к датчикам движения и света. Вы можете полностью заблокировать или разрешить веб-сайтам доступ к датчикам.

Присвоение политике значения "1" разрешает веб-сайтам доступ и использование датчиков. Присвоение политике значения "2" запрещает доступ к датчикам.

Вы можете переопределить эту политику для определенных шаблонов URL-адресов с помощью политик [SensorsAllowedForUrls](#sensorsallowedforurls) и [SensorsBlockedForUrls](#sensorsblockedforurls).

Если эта политика не настроена, веб-сайты смогут получать доступ к датчикам и использовать их, а пользователи смогут изменять этот параметр. Это глобальное значение по умолчанию для [SensorsAllowedForUrls](#sensorsallowedforurls) и [SensorsBlockedForUrls](#sensorsblockedforurls).

Сопоставление параметров политики:

* AllowSensors (1) = разрешить сайтам доступ к датчикам

* BlockSensors (2) = запретить доступ к датчикам для всех сайтов

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: DefaultSensorsSetting
  - Имя групповой политики: Параметр датчиков по умолчанию
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultSensorsSetting
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultSensorsSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefaultSerialGuardSetting

  #### Управлять использованием API Serial

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  Укажите, могут ли сайты получать доступ к последовательным портам. Вы можете либо полностью заблокировать доступ, либо каждый раз запрашивать у пользователя разрешение, когда веб-сайт пытается получить доступ к последовательному порту.

Присвоение этой политике значения "3" позволяет веб-сайтам запрашивать доступ к последовательным портам. Присвоение этой политике значения "2" запрещает доступ к последовательным портам.

Вы можете переопределить эту политику для конкретных шаблонов URL-адресов с помощью политик [SerialAskForUrls](#serialaskforurls) и [SerialBlockedForUrls](#serialblockedforurls).

Если эта политика не настроена, по умолчанию сайты могут запрашивать у пользователя доступ к последовательному порту, при этом пользователи могут изменить эту настройку.

Сопоставление параметров политики:

* BlockSerial (2) = запретить всем сайтам запрашивать доступ к последовательным портам через API Serial

* AskSerial (3) = разрешить сайтам запрашивать разрешение пользователя на доступ к последовательному порту

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: DefaultSerialGuardSetting
  - Имя групповой политики: Управлять использованием API Serial
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefaultSerialGuardSetting
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DefaultSerialGuardSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DefinePreferredLanguages

  #### Определение упорядоченного списка предпочитаемых языков, на которых должны отображаться веб-сайты, если сайт поддерживает этот язык

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с версии 89 или более поздней

  #### Описание

  Настраивает языковые варианты, отправляемые Microsoft Edge на веб-сайты в рамках запроса Accept-Language заголовком HTTP, и не позволяет пользователям добавлять, удалять или изменять порядок предпочитаемых языков в параметрах Microsoft Edge. Пользователи, желающие изменить языки, на которых Microsoft Edge отображает интерфейс или на которые предлагает переводить страницы, будут ограничены языками, настроенными в этой политике.

Если включить эту политику, веб-сайты будут отображаться на первом языке в списке, который они поддерживают, если для определения языка интерфейса не используется другая логика сайта. Языковые варианты, определенные в этой политике, переопределяют языки, настроенные в рамках политики [SpellcheckLanguage](#spellchecklanguage).

Если не настроить или отключить эту политику, Microsoft Edge будет отправлять веб-сайтам указанные пользователем предпочитаемые языки в рамках запроса Accept-Language заголовка HTTP.

Подробные сведения о допустимых языковых вариантах см. на странице [https://go.microsoft.com/fwlink/?linkid=2148854](https://go.microsoft.com/fwlink/?linkid=2148854).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: DefinePreferredLanguages
  - Имя групповой политики: определение упорядоченного списка предпочитаемых языков, на которых должны отображаться веб-сайты, если сайт поддерживает этот язык
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DefinePreferredLanguages
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"en-US,fr,es"
```

  #### Сведения о Mac и параметры
  
  - Имя ключа предпочтения: DefinePreferredLanguages
  - Пример значения:
``` xml
<string>en-US,fr,es</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### DelayNavigationsForInitialSiteListDownload

  #### Требование наличия списка сайтов для режима предприятия перед переходом между вкладками

  
  
  #### Поддерживаемые версии:

  - В Windows с 84 и более поздних версий

  #### Описание

  Позволяет указать, должны ли вкладки Microsoft Edge ждать перед переходом, пока браузер не загрузит исходный список сайтов для режима предприятия. Этот параметр предназначен для сценария, при котором домашняя страница браузера должна загружаться в режиме Internet Explorer, и это должно происходить при первом запуске браузера после включения режима IE. Если такого сценария нет, мы рекомендуем не включать этот параметр, поскольку он может отрицательно сказаться на производительности при загрузке домашней страницы. Этот параметр применим только в том случае, если в Microsoft Edge нет кэшированного списка сайтов для режима предприятия, например при первом запуске браузера после включения режима IE.

Этот параметр работает в сочетании с [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) со значением «IEMode» и политикой [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist), где список содержит хотя бы одну запись.

Время ожидания и соответствующее поведение для этой политики можно настроить с помощью политики [NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout).

Если для политики задано значение «All» и в Microsoft Edge нет кэшированной версии списка сайтов для режима предприятия, вкладки будут ожидать перехода, пока браузер не загрузит список сайтов. Сайты, содержащиеся в списке для открытия в режиме Internet Explorer, будут загружаться в режиме Internet Explorer даже при начале навигации в браузере. Сайты, для которых нельзя настроить открытие в Internet Explorer, например любые сайты со схемой, отличающейся от "http:", "https:", "file:" или "ftp:", не ожидают перехода и сразу загружаются в режиме Edge.

Если для политики задано значение «None» или она не настроена, а в Microsoft Edge нет кэшированной версии списка сайтов для режима предприятия, вкладки будут открываться сразу, не дожидаясь, пока браузер загрузит список сайтов для режима предприятия. Сайты, содержащиеся в списке сайтов для открытия в режиме Internet Explorer, будут открываться в режиме Microsoft Edge, пока браузер не завершит загрузку списка сайтов для режима предприятия.

Сопоставление параметров политики:

* None (0) = Нет

* All (1) = Все соответствующие условиям переходы

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DelayNavigationsForInitialSiteListDownload
  - Имя GP: Требование наличия списка сайтов для режима предприятия перед переходом между вкладками
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DelayNavigationsForInitialSiteListDownload
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### DeleteDataOnMigration

  #### Удалить старые данные браузера при миграции

  
  
  #### Поддерживаемые версии:

  - На Windows с 83 и более поздних версий

  #### Описание

  Эта политика определяет, будут ли данные о просмотре пользователями устаревшей версии Microsoft Edge удаляться после перехода на Microsoft Edge версии 81 или новее.

Если для этой политики установлено значение «Включено», все данные о просмотре из устаревшей версии Microsoft Edge после миграции на Microsoft Edge версии 81 или более поздней будут удалены. Эта политика должна быть установлена до перехода на Microsoft Edge версии 81 или новее, чтобы иметь какое-либо влияние на существующие данные просмотра.

Если для этой политики установлено значение «Отключено» или она не настроена, данные о просмотре пользователями не удаляются после перехода на Microsoft Edge версии 83 или более поздней версии.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DeleteDataOnMigration
  - Имя GP: Удалить старые данные браузера при миграции
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DeleteDataOnMigration
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  

  [В начало](#microsoft-edge---policies)

  ### DeveloperToolsAvailability

  #### Контроль, где инструменты разработчика могут использоваться

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Контроль, где инструменты разработчика могут быть использованы.

Если для этой политики задано значение «DeveloperToolsDisallowedForForceInstalledExtensions» (по умолчанию), пользователи могут получить доступ к инструментам разработчика и консоли JavaScript в целом, но не в контексте расширений, установленных корпоративной политикой.

Если вы установите для этой политики значение «DeveloperToolsAllowed», пользователи смогут получить доступ к инструментам разработчика и консоли JavaScript во всех контекстах, включая расширения, установленные корпоративной политикой.

Если вы установите для этой политики значение «DeveloperToolsDisallowed», пользователи не смогут получить доступ к инструментам разработчика или проверить элементы веб-сайта. Сочетания клавиш и пункты меню или контекстного меню, которые открывают инструменты разработчика или консоль JavaScript, отключены.

Сопоставление параметров политики:

* DeveloperToolsDisallowedForForceInstalledExtensions (0) = Заблокировать инструменты разработчика на расширениях, установленных корпоративной политикой, разрешить в других контекстах

* DeveloperToolsAllowed (1) = разрешить использовать инструменты разработчика

* DeveloperToolsDisallowed (2) = не разрешать использовать инструменты разработчика

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DeveloperToolsAvailability
  - Имя GP: Контроль, где могут использоваться инструменты разработчика
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DeveloperToolsAvailability
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DeveloperToolsAvailability
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DiagnosticData

  #### Отправлять обязательные и необязательные диагностические данных об использовании браузера

  
  
  #### Поддерживаемые версии:

  - В Windows 7 и macOS — с версии 86 и более поздних версий

  #### Описание

  Эта политика управляет отправкой обязательных и необязательных диагностических данных об использовании браузера в корпорацию Майкрософт.

Обязательные диагностические данные собираются для защиты, обеспечения актуальности и правильной работы Microsoft Edge.

Необязательные диагностические данные включают данные об использовании браузера, посещаемых веб-сайтах, а также отчеты о сбоях, чтобы помочь в улучшении продуктов и служб Майкрософт.

Эта политика не поддерживается на устройствах с Windows 10. Чтобы управлять сбором этих данных в Windows 10, ИТ-администраторы должны использовать групповую политику диагностических данных Windows. Эта политика называется "Разрешить телеметрию" или "Разрешить диагностические данные" в зависимости от версии Windows. Подробнее о сборе диагностических данных Windows 10: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Используйте один из следующих параметров для настройки этой политики:

"Off" — отключает сбор обязательных и необязательных диагностических данных. Не рекомендуется использовать этот параметр.

"RequiredData" — отправляет обязательные диагностические данные, но отключает сбор необязательных диагностических данных. Microsoft Edge отправляет обязательные диагностические данные для защиты, обеспечения актуальности и правильной работы Microsoft Edge.

"OptionalData" — отправляет необязательные диагностические данные, включающие данные об использовании браузера, посещенных веб-сайтах, отчеты о сбоях, для улучшения продуктов и служб Майкрософт.

В Windows 7/macOS эта политика управляет отправкой обязательных и необязательных данных в Майкрософт.

Если эта политика не настроена или отключена, Microsoft Edge будет по умолчанию использовать параметры пользователя.

Сопоставление параметров политики:

* Off (0) = Отключено (не рекомендуется)

* RequiredData (1) = Обязательные данные

* OptionalData (2) = Необязательные данные

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: DiagnosticData
  - Имя групповой политики: Отправлять обязательные и необязательные диагностические данных об использовании браузера
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DiagnosticData
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DiagnosticData
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DirectInvokeEnabled

  #### Разрешить пользователям открывать файлы с использованием протокола DirectInvoke

  
  
  #### Поддерживаемые версии:

  - В Windows с 78 и более поздних версий

  #### Описание

  Разрешить пользователям открывать файлы с использованием протокола DirectInvoke. Протокол DirectInvoke позволяет веб-сайтам запрашивать, чтобы браузер открывал файлы с определенного URL-адреса, используя определенный обработчик файлов на компьютере или устройстве пользователя.

Если вы включите или не настроите эту политику, пользователи смогут открывать файлы, используя протокол DirectInvoke.

Если вы отключите эту политику, пользователи не смогут открывать файлы, используя протокол DirectInvoke. Вместо этого файл будет сохранен в файловой системе.

Примечание. Отключение DirectInvoke может помешать работе некоторых функций Microsoft SharePoint Online должным образом.

Дополнительные сведения о DirectInvoke см. в статьях [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) и [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DirectInvokeEnabled
  - Имя GP: Разрешить пользователям открывать файлы, используя протокол DirectInvoke.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DirectInvokeEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  

  [В начало](#microsoft-edge---policies)

  ### Disable3DAPIs

  #### Отключить поддержку API для трехмерной графики

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Запретить веб-страницам доступ к графическому процессору (GPU). В частности, веб-страницы не могут получить доступ к API WebGL, а подключаемые модули не могут использовать Pepper 3D API.

Если вы не настроите или не отключите эту политику, она потенциально позволяет веб-страницам использовать API WebGL, а подключаемые модули - API Pepper 3D. Microsoft Edge может по умолчанию по-прежнему требовать передачи аргументов командной строки для использования этих API.

Если для политики [HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled) задано значение false, параметр политики Disable3DAPIs игнорируется - это эквивалентно установке политики Disable3DAPIs в значение true.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: Disable3DAPIs
  - Имя GP: Отключить поддержку API для трехмерной графики
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: Disable3DAPIs
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: Disable3DAPIs
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### DisableScreenshots

  #### Отключить создание скриншотов

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определяет, могут ли пользователи делать скриншоты страницы браузера.

Если этот параметр включен, пользователь не может делать снимки экрана с помощью сочетаний клавиш или расширенных API.

Если эта политика отключена или не настроена, пользователи могут делать снимки экрана.

Обратите внимание, что эта политика контролирует снимки экрана, сделанные из самого браузера. Даже если вы включите эту политику, пользователи все равно смогут делать снимки экрана, используя какой-либо метод вне браузера (например, с помощью функции операционной системы или другого приложения).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DisableScreenshots
  - Название GP: Отключить создание скриншотов
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DisableScreenshots
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DisableScreenshots
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### DiskCacheDir

  #### Установить каталог дискового кэша

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настраивает каталог для хранения кэшированных файлов.

Если вы включите эту политику, Microsoft Edge будет использовать предоставленный каталог независимо от того, указал ли пользователь флаг --disk-cache-dir. Чтобы избежать потери данных или других непредвиденных ошибок, не настраивайте эту политику на корневой каталог тома или на каталог, используемый для других целей, поскольку Microsoft Edge управляет его содержимым.

Список переменных, которые можно использовать при указании каталогов и путей, см. в статье [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

Если вы не настроите эту политику, используется каталог кэша по умолчанию, и пользователи могут переопределить это значение по умолчанию с помощью флага командной строки --disk-cache-dir.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DiskCacheDir
  - Имя GP: Установить каталог дискового кэша
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DiskCacheDir
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"${user_home}/Edge_cache"
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: DiskCacheDir
  - Пример значения:
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### DiskCacheSize

  #### Установить размер дискового кэша в байтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настраивает размер кэша в байтах, используемого для хранения файлов на диске.

Если вы включите эту политику, Microsoft Edge использует предоставленный размер кэша независимо от того, указал ли пользователь флаг --disk-cache-size. Значение, указанное в этой политике, не является жесткой границей, а скорее предложением для системы кэширования; любое значение ниже нескольких мегабайт слишком мало и будет округлено до разумного минимума.

Если вы установите значение этой политики равным 0, будет использоваться размер кэша по умолчанию, и пользователи не смогут его изменить.

Если вы не настроите эту политику, используется размер по умолчанию, но пользователи могут переопределить его с помощью флага --disk-cache-size.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DiskCacheSize
  - Имя GP: Установить размер дискового кэша в байтах.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DiskCacheSize
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x06400000
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: DiskCacheSize
  - Пример значения:
``` xml
<integer>104857600</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### DnsOverHttpsMode

  #### Управление режимом DNS через HTTPS

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 83 и более поздних версий

  #### Описание

  Управлять режимом распознавателя DNS-через-HTTPS. Обратите внимание, что эта политика будет устанавливать режим по умолчанию только для каждого запроса. Режим может быть переопределен для особых типов запросов, таких как запросы на разрешение имени хоста сервера DNS-через-HTTPS.

Выключенный режим отключит DNS-через-HTTPS.

В «автоматическом» режиме сначала будут отправляться запросы DNS-через-HTTPS, если сервер DNS-через-HTTPS доступен, и в случае ошибки может произойти отправка небезопасных запросов.

В «безопасном» режиме будут отправляться только запросы DNS-через-HTTPS, и он не будет разрешен в случае ошибки.

Если вы не настроите эту политику, браузер может отправлять запросы DNS-через-HTTPS на распознаватель, связанный с настроенным обработчиком системы пользователя.

Сопоставление параметров политики:

* off (off) = Отключить DNS-через-HTTPS

* automatic (automatic) = Включить DNS-через-HTTPS с небезопасным резервом

* secure (secure) = Включить DNS-через-HTTPS без небезопасного резерва

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DnsOverHttpsMode
  - Имя GP: Управление режимом DNS-over-HTTPS
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DnsOverHttpsMode
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"off"
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: DnsOverHttpsMode
  - Пример значения:
``` xml
<string>off</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### DnsOverHttpsTemplates

  #### Укажите шаблон URI нужного преобразователя DNS-over-HTTPS.

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 83 и более поздних версий

  #### Описание

  Шаблон URI нужного преобразователя DNS-over-HTTPS. Чтобы указать несколько распознавателей DNS-over-HTTPS, разделите соответствующие шаблоны URI пробелами.

Если для [DnsOverHttpsMode](#dnsoverhttpsmode) установлено значение «secure», эта политика должна быть установлена и не может быть пустой.

Если вы установите [DnsOverHttpsMode](#dnsoverhttpsmode) в «автоматический», и эта политика установлена, то будут использоваться указанные шаблоны URI. Если вы не установите эту политику, то жестко закодированные сопоставления будут использоваться для попытки обновить текущий распознаватель DNS пользователя до распознавателя DoH, управляемого тем же поставщиком.

Если шаблон URI содержит переменную dns, запросы к распознавателю будут использовать GET; в противном случае запросы будут использовать POST.

Неправильно отформатированные шаблоны будут игнорироваться.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DnsOverHttpsTemplates
  - Имя GP: Укажите шаблон URI нужного преобразователя DNS-over-HTTPS.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: DnsOverHttpsTemplates
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"https://dns.example.net/dns-query{?dns}"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DnsOverHttpsTemplates
  - Пример значения:
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### DownloadDirectory

  #### Установить каталог загрузки

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настраивает каталог для использования при загрузке файлов.

Если вы включите эту политику, Microsoft Edge будет использовать предоставленный каталог независимо от того, указал ли пользователь один или выбрал, чтобы каждый раз запрашивать местоположение загрузки. Список переменных, которые можно использовать, см. в статье [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

Если вы отключите или не настроите эту политику, используется каталог загрузки по умолчанию, и пользователь может изменить его.

Если вы указали неверный путь, Microsoft Edge по умолчанию будет использовать каталог по умолчанию для загрузки пользователя.

Если папка, указанная в этом пути, не существует, при загрузке будет выведено приглашение, в котором пользователю будет предложено сохранить свою загрузку.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DownloadDirectory
  - Имя GP: Установить каталог загрузки
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: DownloadDirectory
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"\n      Linux-based OSes (including Mac): /home/${user_name}/Downloads\n      Windows: C:\\Users\\${user_name}\\Downloads"
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: DownloadDirectory
  - Пример значения:
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### DownloadRestrictions

  #### Разрешить ограничения загрузки

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настраивает тип загрузок, которые Microsoft Edge полностью блокирует, не позволяя пользователям отменять решение о безопасности.

Установите опцию «BlockDangerousDownloads», чтобы разрешить все загрузки, кроме тех, которые содержат предупреждения фильтра SmartScreen в Microsoft Defender.

Установите опцию «BlockPotentiallyDangerousDownloads», чтобы разрешить все загрузки, кроме тех, которые содержат предупреждения фильтра SmartScreen в Microsoft Defender о потенциально опасных и нежелательных загрузках.

Установите значение «BlockAllDownloads», чтобы заблокировать все загрузки.

Если вы не настроили эту политику или не установили опцию «DefaultDownloadSecurity», загрузки проходят обычные ограничения безопасности, основанные на результатах анализа фильтра SmartScreen в Microsoft Defender.

Обратите внимание, что эти ограничения применяются к загрузкам из содержимого веб-страницы, а также к параметру контекстного меню «ссылка для загрузки...». Эти ограничения не распространяются на сохранение или загрузку отображаемой в данный момент страницы, а также на параметр «Сохранить как PDF» из параметров печати.

См. [https://go.microsoft.com/fwlink/?linkid=2094934](https://go.microsoft.com/fwlink/?linkid=2094934) для дополнительной информации о фильтре SmartScreen в Microsoft Defender.

Сопоставление параметров политики:

* DefaultDownloadSecurity (0) = Без особых ограничений

* BlockDangerousDownloads (1) = Блокировать опасные загрузки

* BlockPotentiallyDangerousDownloads (2) = Блокировать потенциально опасные и нежелательные загрузки

* BlockAllDownloads (3) = Заблокировать все загрузки.

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: DownloadRestrictions
  - Имя GP: Разрешить ограничения загрузки
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: DownloadRestrictions
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: DownloadRestrictions
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### EdgeCollectionsEnabled

  #### Включить функцию коллекций

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 78 и более поздних версий

  #### Описание

  Позволяет пользователям получать доступ к функции «Коллекции», где они могут более эффективно собирать, организовывать, обмениваться и экспортировать контент с помощью интеграции с Office.

Если вы включите или не настроите эту политику, пользователи смогут получать доступ и использовать функцию «Коллекции» в Microsoft Edge.

Если вы отключите эту политику, пользователи не смогут получать доступ к коллекциям в Microsoft Edge и использовать их.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: EdgeCollectionsEnabled
  - Имя GP: Включить функцию коллекций
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: EdgeCollectionsEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: EdgeCollectionsEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### EdgeShoppingAssistantEnabled

  #### Покупки в Microsoft Edge включены

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 87 или позже

  #### Описание

  Эта политика позволяет пользователям сравнивать цены на продукт, который они просматривают, получать купоны или скидки с веб-сайтов, а также автоматически применять купоны во время оформления заказа.

Если включить или не настроить эту политику, возможности покупок, такие как сравнение цен, купоны и скидки, будут автоматически применяться для доменов розничной торговли. Купоны текущего продавца и цены других продавцов будут получены с сервера.

Если отключить эту политику, возможности покупок, такие как сравнение цен, купоны и скидки, не будут автоматически обнаруживаться для доменов розничной торговли.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: EdgeShoppingAssistantEnabled
  - Имя GP: Покупки в Microsoft Edge включены
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: EdgeShoppingAssistantEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа настройки: EdgeShoppingAssistantEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### EditFavoritesEnabled

  #### Позволяет пользователям редактировать избранное

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Включите эту политику, чтобы пользователи могли добавлять, удалять и изменять избранное. Это поведение по умолчанию, если вы не настроили политику.

Отключите эту политику, чтобы пользователи не могли добавлять, удалять или изменять избранное. Они все еще могут использовать существующие избранное.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: EditFavoritesEnabled
  - Имя GP: Позволять пользователям редактировать избранное
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: EditFavoritesEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: EditFavoritesEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### EnableDeprecatedWebPlatformFeatures

  #### Повторно включить устаревшие функции веб-платформы на ограниченное время (устарело)

  
  >УСТАРЕЛО: эта политика устарела и не работает в версиях Microsoft Edge после 86.
  #### Поддерживаемые версии:

  - В Windows и macOS — версии c 77 по 86

  #### Описание

  Эта политика устарела, так как для управления индивидуальными функциями веб-платформ используются специальные политики веб-платформы.

Укажите список устаревших функций веб-платформы для временного повторного включения.

Эта политика позволяет повторно активировать устаревшие функции веб-платформы в течение ограниченного времени. Особенности идентифицируются строковым тегом.

Если вы не настроите эту политику, если список пуст, или если функция не соответствует одному из поддерживаемых строковых тегов, все устаревшие функции веб-платформы останутся отключенными.

Хотя сама политика поддерживается на вышеперечисленных платформах, ее функция может быть недоступна на всех этих платформах. Не все устаревшие функции веб-платформы могут быть повторно включены. Только те, которые явно перечислены ниже, могут быть повторно включены, и только в течение ограниченного периода времени, который отличается для каждой функции. Вы можете ознакомиться с намерениями изменений функции веб-платформы на https://bit.ly/blinkintents.

Общий формат строкового тега: [DeprecatedFeatureName]_EffectiveUntil[yyyymmdd].

Сопоставление параметров политики:

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = Включить API ExampleDeprecatedFeature до 2008/09/02

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: EnableDeprecatedWebPlatformFeatures
  - Имя GP: Повторно включить устаревшие функции веб-платформы на ограниченное время (устарело)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = "ExampleDeprecatedFeature_EffectiveUntil20080902"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: EnableDeprecatedWebPlatformFeatures
  - Пример значения:
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### EnableDomainActionsDownload

  #### Разрешение загрузки действий, связанных с доменом, из Microsoft (устарело)

  
  >УСТАРЕЛО: эта политика устарела и не работает в Microsoft Edge версии 84 и более поздних.
  #### Поддерживаемые версии:

  - На Windows и macOS с 77, до 84 версии

  #### Описание

  Эта политика не работает, поскольку конфликтующих состояний следует избегать. Она использовалась для включения и выключения загрузки списка действий, связанных с доменом, но не всегда приводила к желаемому состоянию. У службы экспериментов и конфигураций, обрабатывающая загрузку, есть собственная политика, определяющая, что должно загружаться из службы. Вместо нее используйте политику [ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol).

В Microsoft Edge действия над доменом представляют собой ряд функций совместимости, которые помогают браузеру корректно работать в Интернете.

Microsoft ведет список действий, предпринимаемых на определенных доменах по причинам совместимости. Например, браузер может переопределить строку пользовательского агента на веб-сайте, если этот веб-сайт поврежден из-за новой строки пользовательского агента в Microsoft Edge. Каждое из этих действий должно быть временным, пока Microsoft пытается решить проблему с владельцем сайта.

Когда браузер запускается, а затем периодически после этого, браузер связывается со Службой экспериментов и настройки, которая содержит самый последний список совместимых действий, которые необходимо выполнить. Этот список сохраняется локально после первого извлечения, поэтому последующие запросы будут обновлять список только в том случае, если копия сервера изменилась.

Если вы включите эту политику, список действий домена будет по-прежнему загружаться из службы экспериментов и настройки.

Если вы отключите эту политику, список действий домена больше не будет загружаться из службы экспериментов и настройки.

Если вы не настроите эту политику, список действий домена будет по-прежнему загружаться из службы экспериментов и настройки.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: EnableDomainActionsDownload
  - Имя GP: Разрешение загрузки действий, связанных с доменом, из Microsoft (устарело)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: EnableDomainActionsDownload
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: EnableDomainActionsDownload
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### EnableOnlineRevocationChecks

  #### Включить онлайн проверки OCSP/CRL

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Проверка отзыва в режиме онлайн не дает существенного преимущества безопасности и по умолчанию отключена.

Если вы активируете эту политику, Microsoft Edge будет выполнять оперативные проверки OCSP/CRL со сбоем. «Мягкий сбой» означает, что если сервер отзыва не может быть достигнут, сертификат будет считаться действительным.

Если вы отключите политику или не настроите ее, Microsoft Edge не будет выполнять онлайн-проверки отзыва.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: EnableOnlineRevocationChecks
  - Имя GP: включить онлайн проверки OCSP / CRL
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: EnableOnlineRevocationChecks
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: EnableOnlineRevocationChecks
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### EnableSha1ForLocalAnchors

  #### Разрешение сертификатов, подписанных с помощью SHA-1 при выдаче локальными якорями доверия (не рекомендуется)

  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:

  - В Windows и macOS — версия 85 или более поздние

  #### Описание

  Если этот параметр включен, Microsoft Edge позволяет использовать соединения, которые защищены с помощью сертификатов SHA-1, до тех пор, пока цепочка сертификатов завершается установленным локально корневым сертификатом, который действителен в других отношениях.

Обратите внимание на то, что эта политика зависит от стека проверки сертификатов операционной системы (ОС), разрешающего использование подписей SHA-1. Если при обновлении ОС изменяется метод обработки сертификатов SHA-1, эта политика может перестать работать.  Кроме того, эта политика является временным решением, которое дает компаниям больше времени на отказ от SHA-1. Эта политика будет удалена в Microsoft Edge версии 92, которая будет выпущена в середине 2021 г.

Если не задать эту политику или задать для нее значение false, а также если цепочка сертификатов SHA-1 будет завершаться публично доверенным корневым сертификатом, Microsoft Edge не сможет использовать сертификаты, подписанные с применением алгоритма SHA-1.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: EnableSha1ForLocalAnchors
  - Имя GP: Разрешение сертификатов, подписанных с помощью SHA-1 при выдаче локальными якорями доверия (не рекомендуется)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: EnableSha1ForLocalAnchors
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: EnableSha1ForLocalAnchors
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### EnterpriseHardwarePlatformAPIEnabled

  #### Разрешить управляемым расширениям использовать API-интерфейс Enterprise Hardware Platform

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 78 и более поздних версий

  #### Описание

  Когда эта политика включена, расширения, установленные корпоративной политикой, могут использовать API-интерфейс Enterprise Hardware Platform.
Если эта политика отключена или не установлена, никакие расширения не могут использовать API-интерфейс Enterprise Hardware Platform.
Эта политика также применяется к расширениям компонентов.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: EnterpriseHardwarePlatformAPIEnabled
  - Имя GP: Разрешить управляемым расширениям использовать API-интерфейс Enterprise Hardware Platform.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: EnterpriseHardwarePlatformAPIEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: EnterpriseHardwarePlatformAPIEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### EnterpriseModeSiteListManagerAllowed

  #### Разрешение доступа к средству Enterprise Mode Site List Manager

  
  
  #### Поддерживаемые версии:

  - В Windows — версия 86 или более поздние

  #### Описание

  Позволяет задать доступность для пользователей средства Enterprise Mode Site List Manager.

Если эта политика включена, пользователям будет доступна кнопка навигации средства Enterprise Mode Site List Manager на странице edge://compat, они смогут переходить к этому средству и использовать его.

Если вы отключите или не настроите эту политику, кнопка навигации средства Enterprise Mode Site List Manager будет недоступна пользователями и они не смогут использовать ее.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: EnterpriseModeSiteListManagerAllowed
  - Имя GP: Разрешение доступа к средству Enterprise Mode Site List Manager
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: EnterpriseModeSiteListManagerAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  

  [В начало](#microsoft-edge---policies)

  ### ExemptDomainFileTypePairsFromFileTypeDownloadWarnings

  #### Отключение предупреждений о расширениях загружаемых файлов для определенных типов файлов в доменах

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS — версия 85 или более поздние

  #### Описание

  Вы можете включить эту политику, чтобы создать словарь расширений типов файлов с соответствующим списком доменов, относительно которых не будут поступать предупреждения о расширениях загружаемых файлов. Это позволяет администраторам предприятий блокировать предупреждения о расширениях загружаемых файлов, если файлы связаны с доменом из списка. Например, если расширение "jnlp" связано с "website1.com", пользователи не будут получать предупреждений при загрузке файлов "jnlp" с "website1.com", но при загрузке файлов "jnlp" с "website2.com" предупреждения будут поступать.

Относительно файлов с расширениями тех типов, которые связаны с упомянутыми в данной политике доменами, по-прежнему будут поступать предупреждения службы безопасности, не относящиеся к расширениям и типам файлов, например предупреждения о загрузке смешанного контента и предупреждения фильтра SmartScreen в Microsoft Defender.

Если эта политика отключена или не настроена, пользователям будут поступать предупреждения о расширениях загружаемых файлов.

Если политика включена, то должны выполняться следующие условия:

* шаблон URL-адреса должен быть иметь формат, соответствующий [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322);
* расширение файла должно вводиться в символах ASCII нижнего регистра. Расширения файлов должны указываться без начального разделителя, например "jnlp", а не ".jnlp".

Пример.

Значение, приведенное в этом примере, отключает предупреждения о загрузке файлов с расширениями swf, exe и jnlp для доменов *.contoso.com. При этом пользователь будет получать предупреждения о загрузке файлов с расширениями exe и jnlp для любых других доменов, но о файлах с расширением swf предупреждений не будет.

[ { "file_extension": "jnlp", "domains": ["contoso.com"] }, { "file_extension": "exe", "domains": ["contoso.com"] }, { "file_extension": "swf", "domains": ["*"] } ]

Обратите внимание: в предыдущем примере запрещены предупреждения о загрузке файлов с расширением "swf" для всех доменов. Применение подобного отключения предупреждений для всех доменов в отношении какого-либо опасного расширения файлов не рекомендуется по соображениям безопасности. Пример приведен только для того, чтобы продемонстрировать такую возможность.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Имя GP: Отключение предупреждений о расширениях загружаемых файлов для определенных типов файлов в доменах
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {"domains": ["https://contoso.com", "contoso2.com"], "file_extension": "jnlp"}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {"domains": ["*"], "file_extension": "swf"}

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Пример значения:
``` xml
<array>
  <string>{'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}</string>
  <string>{'domains': ['*'], 'file_extension': 'swf'}</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### ExperimentationAndConfigurationServiceControl

  #### Управлять связью со Службой экспериментов и конфигурации

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  В Microsoft Edge служба эксперимента и конфигурации используется для развертывания полезной нагрузки эксперимента и конфигурации.

Полезная нагрузка для экспериментов состоит из списка ранних функций разработки, которые Microsoft предоставляет для тестирования и обратной связи.

Полезная нагрузка конфигурации состоит из списка параметров, которые Microsoft хочет развернуть в Microsoft Edge для оптимизации взаимодействия с пользователем. Например, полезная нагрузка конфигурации может указывать, как часто Microsoft Edge отправляет запросы в Службу экспериментов и настройки для получения новейшей полезной нагрузки.

Кроме того, полезная нагрузка конфигурации может также содержать список действий, которые необходимо выполнить для определенных доменов по причинам совместимости. Например, браузер может переопределить строку пользовательского агента на веб-сайте, если этот веб-сайт поврежден из-за новой строки пользовательского агента в Microsoft Edge. Каждое из этих действий должно быть временным, пока Microsoft пытается решить проблему с владельцем сайта.

Если вы зададите для этой политики режим «FullMode», полная полезная нагрузка будет загружена из Службы экспериментов и конфигурации. Это включает в себя как экспериментальные, так и конфигурационные данные.

Если вы установите эту политику в режим «ConfigurationsOnlyMode», будет доставлена только полезная нагрузка конфигурации.

Если для этой политики задано значение "RestrictedMode", взаимодействие со Службой экспериментов и конфигурации останавливается.

Если вы не настроите эту политику, на управляемом устройстве в стабильных и бета-каналах поведение будет таким же, как в режиме «ConfigurationsOnlyMode».

Если вы не настроите эту политику, на неуправляемом устройстве поведение будет таким же, как в режиме «FullMode».

Сопоставление параметров политики:

* FullMode (2) = Получить конфигурации и эксперименты

* ConfigurationsOnlyMode (1) = Получить только конфигурации

* RestrictedMode (0) = Отключить связь со Службой экспериментов и конфигурации

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ExperimentationAndConfigurationServiceControl
  - Имя GP: Управление связью со Службой Экспериментов и Конфигурации.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ExperimentationAndConfigurationServiceControl
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ExperimentationAndConfigurationServiceControl
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### ExternalProtocolDialogShowAlwaysOpenCheckbox

  #### Показать флажок «Всегда открывать» в диалоговом окне внешнего протокола

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 79 или позже

  #### Описание

  Эта политика контролирует, отображается ли флажок «Всегда разрешать этому сайту открывать ссылки этого типа» в запросах подтверждения запуска внешнего протокола. Эта политика применяется только к ссылкам https://.

Если эта политика включена, при отображении запроса подтверждения внешнего протокола пользователь может выбрать "Всегда разрешать", чтобы пропускать все последующие запросы подтверждения для протокола на этом сайте.

Если эта политика отключена, флажок "Всегда разрешать" не отображается. Пользователь будет запрашивать подтверждение каждый раз, когда вызывается внешний протокол.

Если эта политика не настроена, до Microsoft Edge 83 флажок "Всегда разрешать" не отображается. Пользователь будет запрашивать подтверждение каждый раз, когда вызывается внешний протокол.

В Microsoft Edge 83, если эта политика не настроена, отображение флажка контролируется флагом "Включить запоминание настроек запросов при запуске протокола" в edge://flags

Что касается Microsoft Edge 84, если эта политика не настроена включена, при отображении запроса подтверждения протокола пользователь может выбрать "Всегда разрешать", чтобы пропускать все последующие запросы подтверждения для протокола на этом сайте.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Имя GP: Показать флажок «Всегда открывать» в диалоге внешнего протокола.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### FamilySafetySettingsEnabled

  #### Разрешить пользователям настраивать семейную безопасность

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 83 и более поздних версий

  #### Описание

  Эта политика отключает и полностью скрывает страницу «Безопасность семьи» в настройках. Навигация до edge://settings/familysafety также будет заблокирована. Страница «Семейная безопасность» описывает, какие функции доступны для семейных групп и как вступить в семейную группу. Узнайте больше о семейной безопасности здесь: ([https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432)).

Если вы включите эту политику или не настроите ее, отобразится страница «Семейная безопасность».

Если вы отключите эту политику, страница семейной безопасности не будет отображаться.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: FamilySafetySettingsEnabled
  - Имя GP: Разрешить пользователям настраивать семейную безопасность
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: FamilySafetySettingsEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: FamilySafetySettingsEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### FavoritesBarEnabled

  #### Включить панель избранного

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Включает или отключает панель избранного.

Если вы включите эту политику, пользователи увидят панель избранного.

Если вы отключите эту политику, пользователи не увидят панель избранного.

Если эта политика не настроена, то пользователь может решить использовать панель избранного или нет.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: FavoritesBarEnabled
  - Имя GP: Включить панель избранного
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: FavoritesBarEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: FavoritesBarEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ForceBingSafeSearch

  #### Обеспечивать соблюдение Bing SafeSearch

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Убедитесь, что запросы в веб-поиске Bing выполняются с SafeSearch, для которого установлено указанное значение. Пользователи не могут изменить этот параметр.

Если для этой политики задано значение «BingSafeSearchNoRestrictionsMode», Безопасный поиск в поиске Bing возвращается к значению bing.com.

Если для этой политики задано значение «BingSafeSearchModerateMode», в SafeSearch используется умеренный параметр фильтрации. Умеренная настройка фильтрует видео и изображения для взрослых, но не текст из результатов поиска.

Если вы настроили эту политику в "BingSafeSearchStrictMode", в SafeSearch используется строгий параметр фильтрации. Строгая настройка фильтрует текст, изображения и видео для взрослых.

Если вы отключите эту политику или не настроите ее, безопасный поиск в поиске Bing не будет применен, и пользователи смогут установить желаемое значение на bing.com.

Сопоставление параметров политики:

* BingSafeSearchNoRestrictionsMode (0) = Не настраивать ограничения поиска в Bing

* BingSafeSearchModerateMode (1) = Настроить умеренные ограничения поиска в Bing

* BingSafeSearchStrictMode (2) = Настроить строгие ограничения поиска в Bing

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ForceBingSafeSearch
  - Название GP: Enforce Bing SafeSearch
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ForceBingSafeSearch
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: ForceBingSafeSearch
  - Пример значения:
``` xml
<integer>0</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### ForceCertificatePromptsOnMultipleMatches

  #### Настройте, должен ли Microsoft Edge автоматически выбирать сертификат при наличии нескольких совпадений сертификатов для сайта, настроенного с помощью «AutoSelectCertificateForUrls»

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с 81 и более поздних версий

  #### Описание

  Переключает, предлагается ли пользователям выбирать сертификат, если доступно несколько сертификатов, а сайт настроен с помощью [AutoSelectCertificateForUrls](#autoselectcertificateforurls). Если вы не настроите [AutoSelectCertificateForUrls](#autoselectcertificateforurls) для сайта, пользователю всегда будет предложено выбрать сертификат.

Если для этой политики задано значение True, Microsoft Edge предложит пользователю выбрать сертификат для сайтов в списке, определенном в [AutoSelectCertificateForUrls](#autoselectcertificateforurls), если и только если существует более одного сертификата.

Если для этой политики задано значение «Ложь» или она не настроена, Microsoft Edge автоматически выберет сертификат, даже если для сертификата существует несколько совпадений. Пользователю не будет предложено выбрать сертификат для сайтов в списке, определенном в [AutoSelectCertificateForUrls](#autoselectcertificateforurls).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ForceCertificatePromptsOnMultipleMatches
  - Имя GP: Укажите, должен ли Microsoft Edge автоматически выбирать сертификат при наличии нескольких совпадений сертификатов для сайта, настроенного с помощью «AutoSelectCertificateForUrls».
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ForceCertificatePromptsOnMultipleMatches
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ForceCertificatePromptsOnMultipleMatches
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ForceEphemeralProfiles

  #### Включить использование эфемерных профилей

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Управляет переключением профилей пользователей в эфемерный режим. Эфемерный профиль создается при начале сеанса, удаляется по окончании сеанса и связывается с исходным профилем пользователя.

Если вы включите эту политику, профили будут работать в эфемерном режиме. Это позволяет пользователям работать со своих собственных устройств без сохранения данных просмотра на этих устройствах. Если вы включите эту политику как политику ОС (например, с помощью объекта групповой политики в Windows), она будет применяться ко всем профилям в системе.

Если вы отключите эту политику или не настроите ее, пользователи получат свои обычные профили при входе в браузер.

В эфемерном режиме данные профиля сохраняются на диске только на время сеанса пользователя. Такие функции, как история браузера, расширения и их данные, веб-данные, такие как файлы cookie, и веб-базы данных не сохраняются после закрытия браузера. Это не мешает пользователю вручную загружать любые данные на диск, сохранять страницы или распечатывать их. Если пользователь включил синхронизацию, все данные сохраняются в его учетных записях синхронизации, как и в обычных профилях. Пользователи также могут использовать просмотр InPrivate в эфемерном режиме, если вы явно не отключите это.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ForceEphemeralProfiles
  - Название GP: Включить использование эфемерных профилей
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ForceEphemeralProfiles
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ForceEphemeralProfiles
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ForceGoogleSafeSearch

  #### Принудительный поиск Google SafeSearch

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Вызывает выполнение запросов в веб-поиске Google с активным SafeSearch и запрещает пользователям изменять этот параметр.

Если вы включите эту политику, Безопасный поиск в Поиске Google всегда активен.

Если вы отключите эту политику или не настроите ее, безопасный поиск в Поиске Google не будет применен.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ForceGoogleSafeSearch
  - Имя GP: Принудительный поиск Google SafeSearch
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ForceGoogleSafeSearch
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: ForceGoogleSafeSearch
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ForceLegacyDefaultReferrerPolicy

  #### Использование политики ссылок по умолчанию no-referrer-when-downgrade (устаревшее)

  
  >УСТАРЕЛО: эта политика устарела и не работает в версиях Microsoft Edge после 88.
  #### Поддерживаемые версии:

  - В Windows и macOS — версии c 81 по 88

  #### Описание

  Эта политика не работает, так как она была предназначена только для краткосрочного механизма, чтобы дать предприятиям больше времени на обновление веб-содержимого, если оно оказалось несовместимо с новой политикой ссылок по умолчанию.

Политика ссылок по умолчанию в Microsoft Edge была усилена со значения no-referrer-when-downgrade до более безопасного strict-origin-when-cross-origin.

Если эта корпоративная политика включена, для политики ссылок Microsoft Edge по умолчанию будет установлено старое значение no-referrer-when-downgrade.

Эта корпоративная политика по умолчанию отключена.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ForceLegacyDefaultReferrerPolicy
  - Имя GP: Использование политики ссылок по умолчанию no-referrer-when-downgrade (устаревшее)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ForceLegacyDefaultReferrerPolicy
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ForceLegacyDefaultReferrerPolicy
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ForceNetworkInProcess

  #### Принудительный запуск сетевого кода в процессе браузера (устарело)

  
  >УСТАРЕЛО: эта политика устарела и не работает в Microsoft Edge версии 83 и более поздних.
  #### Поддерживаемые версии:

  - В Windows — версии с 78 по 83

  #### Описание

  Эта политика не работает, так как она была предусмотрена только в качестве краткосрочного механизма, предоставляющего организациям больше времени для перехода на стороннее программное обеспечение, которое не зависит от использования сетевых API. Прокси-серверы рекомендуется использовать для исправлений LSP и Win32 API.

Эта политика заставляет сетевой код запускаться в процессе браузера.

Эта политика по умолчанию отключена. Если включено, пользователи открыты для проблем безопасности, когда сетевой процесс изолирован.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ForceNetworkInProcess
  - Имя GP: Принудительный запуск сетевого кода в процессе браузера (устарело)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ForceNetworkInProcess
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  

  [В начало](#microsoft-edge---policies)

  ### ForceSync

  #### Принудительно синхронизировать данные браузера и не показывать запрос на разрешение синхронизации

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  Принудительно синхронизирует данные в Microsoft Edge. Эта политика также запрещает пользователям отключать синхронизацию.

Если эта политика не настроена, пользователи смогут включать и отключать синхронизацию. Если включить эту политику, пользователи не смогут отключить синхронизацию.

Для правильной работы этой политики, политика [BrowserSignin](#browsersignin) не должна быть настроена или должна быть включена. Если политика [BrowserSignin](#browsersignin) отключена, то политика [ForceSync](#forcesync) не будет применяться.

Политика [SyncDisabled](#syncdisabled) не должна быть настроена или ей должно быть присвоено значение False. Если ей присвоено значение True, то политика [ForceSync](#forcesync) не будет применяться.

0 = не запускать синхронизацию автоматически и отображать запрос разрешения на синхронизацию (по умолчанию) 1 = принудительная синхронизация будет включена для профиля пользователя Azure AD/устаревшей службы Azure AD и не будет отображаться запрос на разрешение синхронизации

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: ForceSync
  - Имя групповой политики: Принудительно синхронизировать данные браузера и не показывать запрос на разрешение синхронизации
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ForceSync
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ForceSync
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ForceYouTubeRestrict

  #### Принудительный минимальный ограниченный режим YouTube

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Обеспечивает минимальный ограниченный режим на YouTube и запрещает пользователям выбирать менее ограниченный режим.

Установите значение «Strict», чтобы включить строгий ограниченный режим на YouTube.

Установите «Moderate», чтобы пользователи могли использовать только умеренный ограниченный режим и строгий ограниченный режим на YouTube. Они не могут отключить ограниченный режим.

Установите значение «Off» или не настраивайте эту политику, чтобы не применять ограниченный режим на YouTube. Внешние политики, такие как политики YouTube, могут по-прежнему использовать ограниченный режим.

Сопоставление параметров политики:

* Off (0) = Не применять ограниченный режим на YouTube

* Moderate (1) = Применять на YouTube как минимум умеренный ограниченный режим

* Strict (2) = Применять принудительный строгий режим для YouTube

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ForceYouTubeRestrict
  - Название GP: Принудительное ограничение YouTube в ограниченном режиме.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ForceYouTubeRestrict
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ForceYouTubeRestrict
  - Пример значения:
``` xml
<integer>0</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### FullscreenAllowed

  #### Разрешить полноэкранный режим

  
  
  #### Поддерживаемые версии:

  - В Windows с 77 и более поздних версий

  #### Описание

  Установите доступность полноэкранного режима - весь пользовательский интерфейс Microsoft Edge скрыт и виден только веб-контент.

Если вы включите эту политику или не настроите ее, пользователь, приложения и расширения с соответствующими разрешениями смогут перейти в полноэкранный режим.

Если вы отключите эту политику, пользователи, приложения и расширения не смогут перейти в полноэкранный режим.

Открытие Microsoft Edge в режиме киоска с помощью командной строки недоступно, если полноэкранный режим отключен.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: FullscreenAllowed
  - Имя GP: Разрешить полноэкранный режим
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: FullscreenAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### GloballyScopeHTTPAuthCacheEnabled

  #### Включить глобальный кэш проверки подлинности HTTP

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с 81 и более поздних версий

  #### Описание

  Эта политика настраивает один глобальный кэш для каждого профиля с учетными данными аутентификации HTTP-сервера.

Если политика отключена или не настроена, браузер будет применять заданное по умолчанию поведение межсайтовой проверки подлинности, которое, начиная с версии 80, будет заключаться в том, чтобы данные проверки подлинности HTTP-сервера ограничивались сайтом верхнего уровня. Таким образом, если два сайта используют ресурсы из одного и того же домена проверки подлинности, учетные данные должны быть предоставлены независимо в контексте обоих сайтов. Кэшированные учетные данные прокси будут повторно использоваться на разных сайтах.

Если вы включите эту политику, учетные данные HTTP-аутентификации, введенные в контексте одного сайта, будут автоматически использоваться в контексте другого сайта.

Включение этой политики оставляет сайты открытыми для некоторых типов межсайтовых атак и позволяет отслеживать пользователей по сайтам даже без файлов cookie, добавляя записи в кэш проверки подлинности HTTP с использованием учетных данных, встроенных в URL-адреса.

Эта политика предназначена для предоставления предприятиям, в зависимости от унаследованного поведения, возможности обновить свои процедуры входа в систему и будет удалена в будущем.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: GloballyScopeHTTPAuthCacheEnabled
  - Имя GP: Включить глобальный кэш проверки подлинности HTTP
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: GloballyScopeHTTPAuthCacheEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: GloballyScopeHTTPAuthCacheEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### GoToIntranetSiteForSingleWordEntryInAddressBar

  #### Принудительная прямая навигация по сайту в интрасети вместо поиска по отдельным словам в адресной строке

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 78 и более поздних версий

  #### Описание

  Если вы включите эту политику, верхний результат автоматического предложения в списке предложений адресной строки будет перемещаться на сайты интрасети, если текст, введенный в адресной строке, представляет собой одно слово без пунктуации.

Навигация по умолчанию при вводе одного слова без пунктуации приведет к переходу на сайт интрасети, соответствующий введенному тексту.

Если вы включите эту политику, второй результат автоматического предложения в списке предложений в адресной строке будет выполнять веб-поиск в точности так, как он был введен, при условии, что этот текст представляет собой одно слово без знаков препинания. Поставщик поиска по умолчанию будет использоваться, если не включена политика предотвращения веб-поиска.

Два эффекта включения этой политики:

Переход на сайты в ответ на запросы с одним словом, которые обычно разрешаются в элементе истории, больше не будет выполняться. Вместо этого браузер будет пытаться перейти на внутренние сайты, которые могут отсутствовать в интрасети организации. Это приведет к ошибке 404.

Популярные поисковые запросы, состоящие из одного слова, потребуют ручного выбора поисковых предложений для правильного проведения поиска.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Имя GP: Принудительная прямая навигация по сайту в интрасети вместо поиска по отдельным словам в адресной строке.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### HSTSPolicyBypassList

  #### Настройте список имен, которые будут обходить проверку политики HSTS

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 79 или позже

  #### Описание

  Имена хостов, указанные в этом списке, будут освобождены от проверки политики HSTS, которая потенциально может обновить запросы с «http://» до «https://». В этой политике разрешены только имена хостов с одной меткой. Имена хостов должны быть канонизированы. Любые IDN должны быть преобразованы в формат их метки A, а все буквы ASCII должны быть строчными. Эта политика применяется только к указанным именам хостов; это не относится к поддоменам имен в списке.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: HSTSPolicyBypassList
  - Имя GP: Настроить список имен, которые будут пропускать проверку политики HSTS
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательно): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\HSTSPolicyBypassList
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = "meet"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: HSTSPolicyBypassList
  - Пример значения:
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### HardwareAccelerationModeEnabled

  #### Используйте аппаратное ускорение, когда доступно

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Указывает, следует ли использовать аппаратное ускорение, если оно доступно. Если вы включите эту политику или не настроите ее, аппаратное ускорение будет включено при условии, что функция GPU явно не заблокирована.

Если вы отключите эту политику, аппаратное ускорение будет отключено.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: HardwareAccelerationModeEnabled
  - Имя GP: Использование аппаратного ускорения, если доступно
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: HardwareAccelerationModeEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: HardwareAccelerationModeEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### HideFirstRunExperience

  #### Скрыть первый запуск опыта и заставки

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 80 или позже

  #### Описание

  Если вы включите эту политику, при первом запуске Microsoft Edge пользователи не будут отображаться при первом запуске и заставке.

Для параметров конфигурации, показанных в режиме первого запуска, браузер по умолчанию настроен на следующее:

- На странице новой вкладки тип канала будет установлен на MSN News, а макет - на Inspirational.

-Пользователь все равно будет автоматически входить в Microsoft Edge, если учетная запись Windows имеет тип Azure AD или MSA.

-Синхронизация не будет включена по умолчанию, и пользователям будет предложено выбрать, нужно ли выполнять синхронизацию при запуске браузера. Для настройки синхронизации и запроса на выполнение синхронизации можно использовать политику [ForceSync](#forcesync) или [SyncDisabled](#syncdisabled).

Если вы отключите или не настроите эту политику, отобразятся «Первый запуск» и экран заставки.

Примечание. Конкретные параметры конфигурации, отображаемые пользователю в режиме первого запуска, также могут управляться с помощью других специальных политик. Вы можете использовать политику HideFirstRunExperience в сочетании с этими политиками, чтобы настроить конкретную работу браузера на управляемых устройствах. Некоторые из этих других политик:

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

-[ForceSync](#forcesync)

-[SyncDisabled](#syncdisabled)

-[BrowserSignin](#browsersignin)

-[NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: HideFirstRunExperience
  - Название GP: Скрыть первый опыт и заставку
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: HideFirstRunExperience
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: HideFirstRunExperience
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

  #### Скрытие диалогового окна однократного перенаправления и объявления в Microsoft Edge

  
  
  #### Поддерживаемые версии:

  - В Windows 87 и более поздних версий

  #### Описание

  Эта политика позволяет отключить диалоговое окно однократного перенаправления и баннер. Если эта политика включена, пользователи не увидят однократное диалоговое окно и заголовок одновременно.
При обнаружении несовместимого веб-сайта в Internet Explorer пользователи будут перенаправлены в Microsoft Edge, но их данные просмотра не будут импортированы.

- Если эта политика включена, пользователям никогда не демонстрируется диалоговое окно однократного перенаправления и баннер перенаправления. При перенаправлении данные просмотра пользователей не будут импортированы.

- Если отключить или не установить эту политику, диалоговое окно перенаправления будет отображаться при первом перенаправлении, а сохраненный баннер перенаправления будет отображаться для пользователей сеансов, начинающихся с перенаправления. Данные просмотра пользователей, импортируются каждый раз, когда для пользователя выполняется такое перенаправление (только в том случае, если пользователь дал согласие в однократном диалоговом окне).


  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled
  - Имя GP: Скрытие диалогового окна однократного перенаправления и объявления в Microsoft Edge
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### ImportAutofillFormData

  #### Разрешить импорт данных формы автозаполнения

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет пользователям импортировать данные автозаполнения формы из другого браузера в Microsoft Edge.

Если вы включите эту политику, опция автоматического импорта данных автозаполнения будет выбрана автоматически.

Если вы отключите эту политику, данные автозаполнения формы не будут импортированы при первом запуске, и пользователи не смогут импортировать их вручную.

Если вы не настроите эту политику, данные автозаполнения импортируются при первом запуске, и пользователи могут выбрать, следует ли импортировать эти данные вручную во время последующих сеансов просмотра.

Вы можете установить эту политику в качестве рекомендации. Это означает, что Microsoft Edge будет импортировать данные автозаполнения при первом запуске, но пользователи могут выбрать или очистить параметр **данных автозаполнения** во время импорта вручную.

**Примечание**: В настоящее время эта политика управляет импортом из браузеров Google Chrome (в Windows 7, 8 и 10 и в macOS) и Mozilla Firefox (в Windows 7, 8 и 10 и в macOS).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ImportAutofillFormData
  - Имя GP: Разрешить импорт данных формы автозаполнения
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ImportAutofillFormData
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ImportAutofillFormData
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ImportBrowserSettings

  #### Разрешить импорт настроек браузера

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 78 и более поздних версий

  #### Описание

  Позволяет пользователям импортировать настройки браузера из другого браузера в Microsoft Edge.

Если вы включите эту политику, флажок **Параметры браузера** будет автоматически установлен в диалоговом окне **Импорт данных браузера**.

Если эта политика отключена, параметры браузера не будут импортированы при первом запуске, и у пользователей не будет возможности импортировать их вручную.

Если эта политика не настроена, параметры браузера будут импортированы при первом запуске, а у пользователей будет возможность выбрать, импортировать ли их вручную во время последующих сеансов работы в браузере.

Вы также можете установить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует настройки при первом запуске, но пользователи могут выбрать или очистить параметр **настроек браузера** во время импорта вручную.

**Примечание**: В настоящее время эта политика управляет импортом Google Chrome (в Windows 7, 8 и 10 и в macOS).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ImportBrowserSettings
  - Имя GP: Разрешить импорт настроек браузера
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ImportBrowserSettings
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ImportBrowserSettings
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ImportCookies

  #### Разрешить импорт файлов cookie

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с 81 и более поздних версий

  #### Описание

  Позволяет пользователям импортировать файлы cookie из другого браузера в Microsoft Edge.

Если вы отключите эту политику, файлы cookie не будут импортированы при первом запуске.

Если вы не настроите эту политику, файлы cookie будут импортированы при первом запуске.

Вы также можете установить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует файлы cookie при первом запуске.

**Примечание**: В настоящее время эта политика управляет импортом Google Chrome (в Windows 7, 8 и 10 и в macOS).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ImportCookies
  - Имя GP: Разрешить импорт файлов cookie
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ImportCookies
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ImportCookies
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ImportExtensions

  #### Разрешить импорт расширений

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с 81 и более поздних версий

  #### Описание

  Позволяет пользователям импортировать расширения из другого браузера в Microsoft Edge.

Если вы включите эту политику, флажок **Расширения** будет автоматически установлен в диалоговом окне **Импорт данных браузера**.

Если вы отключите эту политику, расширения не будут импортированы при первом запуске, и пользователи не смогут импортировать их вручную.

Если вы не настроите эту политику, расширения импортируются при первом запуске, и пользователи могут выбирать, импортировать ли их вручную во время последующих сеансов просмотра.

Вы также можете установить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует расширения при первом запуске, но пользователи могут выбрать или очистить параметр **Избранное** во время импорта вручную.

**Примечание**: В настоящее время эта политика поддерживает импорт только из Google Chrome (в Windows 7, 8 и 10 и в macOS).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ImportExtensions
  - Имя GP: Разрешить импорт расширений
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ImportExtensions
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ImportExtensions
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ImportFavorites

  #### Разрешить импорт избранного

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет пользователям импортировать избранное из другого браузера в Microsoft Edge.

Если вы включите эту политику, флажок **Избранное** будет автоматически установлен в диалоговом окне **Импорт данных браузера**.

Если вы отключите эту политику, избранное не будет импортировано при первом запуске, и пользователи не смогут импортировать его вручную.

Если вы не настроите эту политику, избранное импортируется при первом запуске, а пользователи могут выбрать, импортировать ли его вручную во время последующих сеансов работы в браузере.

Вы также можете установить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует избранное при первом запуске, но пользователи могут выбрать или очистить параметр **Избранное** во время импорта вручную.

**Примечание**: Эта политика в настоящее время управляет импортом из Internet Explorer (в Windows 7, 8 и 10), Google Chrome (в Windows 7, 8 и 10 и в macOS), Mozilla Firefox (в Windows 7, 8 и 10 и в macOS) и браузеры Apple Safari (на macOS).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ImportFavorites
  - Имя GP: Разрешить импорт избранного
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ImportFavorites
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ImportFavorites
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ImportHistory

  #### Разрешить импорт истории просмотров

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет пользователям импортировать свою историю просмотров из другого браузера в Microsoft Edge.

Если вы включите эту политику, флажок **История просмотра** автоматически будет установлен в диалоговом окне **Импорт данных браузера**.

Если вы отключите эту политику, данные журнала браузера не будут импортированы при первом запуске, и пользователи не смогут импортировать эти данные вручную.

Если вы не настроите эту политику, данные журнала браузера импортируются при первом запуске, а пользователи смогут выбрать, импортировать ли их вручную во время последующих сеансов работы в браузере.

Вы также можете установить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует историю просмотров при первом запуске, но пользователи могут выбрать или очистить параметр **истории** при импорте вручную.

**Примечание**: Эта политика в настоящее время управляет импортом из Internet Explorer (в Windows 7, 8 и 10), Google Chrome (в Windows 7, 8 и 10 и в macOS), Mozilla Firefox (в Windows 7, 8 и 10 и в macOS) и браузеры Apple Safari (macOS).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ImportHistory
  - Имя GP: Разрешить импорт истории просмотра
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ImportHistory
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ImportHistory
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ImportHomepage

  #### Разрешить импорт настроек домашней страницы

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет пользователям импортировать настройки своей домашней страницы из другого браузера в Microsoft Edge.

Если вы включите эту политику, автоматически будет выбран параметр импорта параметров домашней страницы вручную.

Если эта политика отключена, параметр домашней страницы не будет импортирован при первом запуске, и у пользователей не будет возможности импортировать его вручную.

Если вы не настроите эту политику, параметр домашней страницы импортируется при первом запуске, а пользователи могут выбрать, импортировать ли его вручную во время последующих сеансов работы в браузере.

Вы можете установить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует настройки домашней страницы при первом запуске, но пользователи могут выбрать или очистить параметр **домашней страницы** во время импорта вручную.

**Примечание**: В настоящее время эта политика управляет импортом из Internet Explorer (в Windows 7, 8 и 10).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ImportHomepage
  - Имя GP: Разрешить импорт настроек домашней страницы
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ImportHomepage
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ImportHomepage
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ImportOpenTabs

  #### Разрешить импорт открытых вкладок

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 79 или позже

  #### Описание

  Позволяет пользователям импортировать открытые и закрепленные вкладки из другого браузера в Microsoft Edge.

Если вы включите эту политику, флажок **Открыть вкладки** будет автоматически установлен в диалоговом окне **Импорт данных браузера**.

Если вы отключите эту политику, открытые вкладки не будут импортированы при первом запуске, и пользователи не смогут импортировать их вручную.

Если вы не настроите эту политику, открытые вкладки импортируются при первом запуске, и пользователи могут выбирать, импортировать ли их вручную во время последующих сеансов просмотра.

Вы также можете установить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует открытые вкладки при первом запуске, но пользователи могут выбрать или очистить параметр **Открыть вкладки** во время импорта вручную.

**Примечание**: В настоящее время эта политика поддерживает импорт только из Google Chrome (в Windows 7, 8 и 10 и в macOS).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ImportOpenTabs
  - Имя GP: Разрешить импорт открытых вкладок
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ImportOpenTabs
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ImportOpenTabs
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ImportPaymentInfo

  #### Разрешить импорт информации об оплате

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет пользователям импортировать платежную информацию из другого браузера в Microsoft Edge.

Если вы включите эту политику, флажок **информации о платеже** будет автоматически установлен в диалоговом окне **Импорт данных браузера**.

Если вы отключите эту политику, платежная информация не будет импортирована при первом запуске, и пользователи не смогут импортировать ее вручную.

Если вы не настроите эту политику, платежная информация импортируется при первом запуске, а пользователи смогут выбрать, импортировать ли ее вручную во время последующих сеансов работы в браузере.

Вы также можете установить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует платежную информацию при первом запуске, но пользователи могут выбрать или очистить параметр **платежной информации** при импорте вручную.

**Примечание:** В настоящее время эта политика управляет импортом из Google Chrome (в Windows 7, 8 и 10 и в macOS).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ImportPaymentInfo
  - Имя GP: Разрешить импорт информации о платеже
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ImportPaymentInfo
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ImportPaymentInfo
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ImportSavedPasswords

  #### Разрешить импорт сохраненных паролей

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет пользователям импортировать сохраненные пароли из другого браузера в Microsoft Edge.

Если вы включите эту политику, автоматически будет выбран вариант импорта сохраненных паролей вручную.

Если вы отключите эту политику, сохраненные пароли не будут импортированы при первом запуске, и пользователи не смогут импортировать их вручную.

Если вы не настроите эту политику, пароли импортируются при первом запуске, и пользователи могут выбирать, импортировать ли их вручную во время последующих сеансов просмотра.

Вы можете установить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует пароли при первом запуске, но пользователи могут выбрать или очистить параметр **паролей** во время импорта вручную.

**Примечание**: В настоящее время эта политика управляет импортом из Internet Explorer (в Windows 7, 8 и 10), Google Chrome (в Windows 7, 8 и 10 и в macOS) и Mozilla Firefox (в Windows 7, 8 и 10 и на macOS) браузеры.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ImportSavedPasswords
  - Имя GP: Разрешить импорт сохраненных паролей
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ImportSavedPasswords
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ImportSavedPasswords
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ImportSearchEngine

  #### Разрешить импорт настроек поисковой системы

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет пользователям импортировать настройки поисковой системы из другого браузера в Microsoft Edge.

Если вы включите эту политику, опция импорта настроек поисковой системы будет выбрана автоматически.

Если эта политика отключена, параметры поисковой системы не будут импортированы при первом запуске, и у пользователей не будет возможности импортировать их вручную.

Если вы не настроите эту политику, параметры поисковой системы импортируются при первом запуске, а пользователи могут выбрать, импортировать ли их вручную во время последующих сеансов работы в браузере.

Вы можете установить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует настройки поисковой системы при первом запуске, но пользователи могут выбрать или очистить параметр **поисковой системы** во время импорта вручную.

**Примечание**: В настоящее время эта политика управляет импортом из Internet Explorer (в Windows 7, 8 и 10).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ImportSearchEngine
  - Имя GP: Разрешить импорт настроек поисковой системы
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ImportSearchEngine
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ImportSearchEngine
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ImportShortcuts

  #### Разрешить импорт ярлыков

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с 81 и более поздних версий

  #### Описание

  Позволяет пользователям импортировать ярлыки из другого браузера в Microsoft Edge.

Если вы отключите эту политику, ярлыки не будут импортированы при первом запуске.

Если вы не настроите эту политику, ярлыки импортируются при первом запуске.

Вы также можете установить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует ярлыки при первом запуске.

**Примечание**: В настоящее время эта политика управляет импортом из Google Chrome (в Windows 7, 8 и 10 и в macOS).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ImportShortcuts
  - Имя GP: Разрешить импорт ярлыков
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ImportShortcuts
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ImportShortcuts
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### InPrivateModeAvailability

  #### Настройка доступности режима InPrivate

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Указывает, может ли пользователь открывать страницы в режиме InPrivate в Microsoft Edge.

Если вы не настроите эту политику или не установите ее в значение «Enabled», пользователи смогут открывать страницы в режиме InPrivate.

Установите для этой политики значение «Disabled», чтобы запретить пользователям использовать режим InPrivate.

Установите для этой политики значение «Forced», чтобы всегда использовать режим InPrivate.

Сопоставление параметров политики:

* Enabled (0) = Режим InPrivate доступен

* Disabled (1) = Режим InPrivate отключен

* Forced (2) = Принудительный режим InPrivate

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: InPrivateModeAvailability
  - Имя GP: Настройка доступности режима InPrivate
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: InPrivateModeAvailability
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: InPrivateModeAvailability
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### InsecureFormsWarningsEnabled

  #### Включить предупреждения для небезопасных форм

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  Эта политика управляет обработкой небезопасных форм (форм, отправляемых по протоколу HTTP), внедренных в безопасные (HTTPS) сайты в браузере.
Если включить или не настроить эту политику, при отправке небезопасной формы будет отображаться предупреждение на всю страницу. Кроме того, будет отображаться пузырек предупреждения рядом с полями формы при наведении на них фокуса, и для этих форм будет отключено автозаполнение.
Если отключить эту политику, предупреждения не будут отображаться для небезопасных форм, а автозаполнение будет работать нормально.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: InsecureFormsWarningsEnabled
  - Имя групповой политики: Включить предупреждения для небезопасных форм
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: InsecureFormsWarningsEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: InsecureFormsWarningsEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### IntensiveWakeUpThrottlingEnabled

  #### Управление параметром IntensiveWakeUpThrottling

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS — версия 85 или более поздние

  #### Описание

  Когда функция IntensiveWakeUpThrottling включена, таймеры Javascript в фоновых вкладках принудительно затормаживаются и объединяются, включаясь не чаще одного раза в минуту после того, как страница находилась в фоновом режиме не менее 5 мин.

Эта функция соответствует веб-стандартам, но может вызвать нарушение функциональности некоторых веб-сайтов, отложив выполнение определенных действий на срок до минуты. Тем не менее, ее включение позволяет существенно снизить нагрузку на ЦП и сэкономить заряд батареи. Дополнительные сведения см. в разделе https://bit.ly/30b1XR4.

Если эта политика включена, функция будет действовать принудительно, и пользователи не смогут переопределить этот параметр.
Если эта политика выключена, функция будет принудительно отключена, и пользователи не смогут переопределить этот параметр.
Если не настроить эту политику, функция будет управляться собственной внутренней логикой. Пользователи смогут настраивать этот параметр вручную.

Обратите внимание на то, что политика применяется для каждого процесса отрисовки, и при запуске процесса отрисовки применяется последнее заданное значение параметра политики. Чтобы обеспечить использование одного и того же параметра для всех загруженных вкладок, необходимо выполнить полный перезапуск. Выполнение процессов с разными значениями этой политики безопасно.


  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: IntensiveWakeUpThrottlingEnabled
  - Имя GP: Управление параметром IntensiveWakeUpThrottling
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: IntensiveWakeUpThrottlingEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: IntensiveWakeUpThrottlingEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### InternetExplorerIntegrationEnhancedHangDetection

  #### Настройка улучшенной функции обнаружения зависаний в режиме Internet Explorer

  
  
  #### Поддерживаемые версии:

  - В Windows с 84 и более поздних версий

  #### Описание

  Улучшенная функция обнаружения зависаний представляет собой реализацию более тщательного подхода к обнаружению зависших страниц в режиме Internet Explorer, чем тот, что используется в самостоятельном браузере Internet Explorer. При обнаружении зависшей веб-страницы браузер предпримет действия для предотвращения своего полного зависания.

Этот параметр позволяет настраивать использование улучшенной функции обнаружения зависаний на случай возникновения проблем несовместимости с любыми из ваших веб-сайтов. Мы рекомендуем отключать эту политику только в том случае, если вы получаете такие уведомления, как "(веб-сайт) не отвечает" в режиме Internet Explorer, но не в самостоятельном браузере Internet Explorer.

Этот параметр работает в сочетании с [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) со значением «IEMode» и политикой [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist), где список содержит хотя бы одну запись.

Если для этой политики задано значение «Enabled» или она не настроена, то к веб-сайтам, открытым в режиме Internet Explorer, будет применяться улучшенная функция обнаружения зависаний.

Если для этой политики задано значение «Disabled», то улучшенная функция обнаружения зависаний будет отключена, и для пользователей будет работать обычная функция обнаружения зависаний Internet Explorer.

Чтобы узнать больше о режиме Internet Explorer, см. [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Сопоставление параметров политики:

* Disabled (0) = Улучшенная функция обнаружения зависаний отключена

* Enabled (1) = Улучшенная функция обнаружения зависаний включена

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: InternetExplorerIntegrationEnhancedHangDetection
  - Имя GP: Настройка улучшенной функции обнаружения зависаний в режиме Internet Explorer
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: InternetExplorerIntegrationEnhancedHangDetection
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### InternetExplorerIntegrationLevel

  #### Настройка интеграции с Internet Explorer

  
  
  #### Поддерживаемые версии:

  - В Windows с 77 и более поздних версий

  #### Описание

  Инструкции по настройке оптимального режима для режима Internet Explorer см. [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Сопоставление параметров политики:

* None (0) = Нет

* IEMode (1) = Режим Internet Explorer

* NeedIE (2) = Internet Explorer 11

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: InternetExplorerIntegrationLevel
  - Имя GP: Настройка интеграции с Internet Explorer
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: InternetExplorerIntegrationLevel
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### InternetExplorerIntegrationLocalFileAllowed

  #### Разрешить запуск локальных файлов в режиме Internet Explorer

  
  
  #### Поддерживаемые версии:

  - В Windows 88 и более поздних версий

  #### Описание

  Эта политика определяет доступность аргумента командной строки --ie-mode-file-url, который используется для запуска Microsoft Edge с локальным файлом, указанным в командной строке, в режиме Internet Explorer.

Этот параметр используется вместе с [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel), для которого задано значение "IEMode".

Если для этой политики задано значение true или она не настроена, пользователю разрешается использовать аргумент командной строки --ie-mode-file-url для запуска локальных файлов в режиме Internet Explorer.

Если для этой политики задано значение false, пользователю не разрешается использовать аргумент командной строки --ie-mode-file-url для запуска локальных файлов в режиме Internet Explorer.

Чтобы узнать больше о режиме Internet Explorer, см. [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: InternetExplorerIntegrationLocalFileAllowed
  - Имя GP: разрешить запуск локальных файлов в режиме Internet Explorer
  - Путь к GP (обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: InternetExplorerIntegrationLocalFileAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### InternetExplorerIntegrationLocalFileExtensionAllowList

  #### Открыть локальные файлы из списка разрешенных расширений файлов в режиме  Internet Explorer

  
  
  #### Поддерживаемые версии:

  - В Windows 88 и более поздних версий

  #### Описание

  Эта политика ограничивает перечень файлов URL file://, которые можно запускать в режиме Internet Explorer, с учетом расширения файла.

Этот параметр используется вместе с [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel), для которого задано значение "IEMode".

Когда отправляется запрос на запуск файла URL file:// в режиме Internet Explorer, расширение файла URL должно быть указано в этом списке, чтобы запуск был разрешен. Файл URL, для которого запрещено открытие в режиме Internet Explorer, будет открыт в режиме Microsoft Edge.

Если для этой политики задано специальное значение "*" или она не настроена, все расширения файлов будут разрешены.

Чтобы узнать больше о режиме Internet Explorer, см. [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: InternetExplorerIntegrationLocalFileExtensionAllowList
  - Имя GP: открыть локальные файлы из списка разрешенных расширений файлов в режиме Internet Explorer
  - Путь к GP (обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge\InternetExplorerIntegrationLocalFileExtensionAllowList
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\InternetExplorerIntegrationLocalFileExtensionAllowList\1 = ".mht"
SOFTWARE\Policies\Microsoft\Edge\InternetExplorerIntegrationLocalFileExtensionAllowList\2 = ".pdf"
SOFTWARE\Policies\Microsoft\Edge\InternetExplorerIntegrationLocalFileExtensionAllowList\3 = ".vsdx"

```

  

  [В начало](#microsoft-edge---policies)

  ### InternetExplorerIntegrationLocalFileShowContextMenu

  #### Показать контекстное меню для открытия ссылки в режиме Internet Explorer

  
  
  #### Поддерживаемые версии:

  - В Windows 88 и более поздних версий

  #### Описание

  Эта политика управляет видимостью параметра "Открыть ссылку на новой вкладке в режиме Internet Explorer" в контекстном меню для ссылок file://.

Этот параметр используется вместе с [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel), для которого задано значение "IEMode".

Если для этой политики задано значение true, элемент контекстного меню "Открыть ссылку на новой вкладке в режиме Internet Explorer" будет доступен для ссылок file://.

Если для этой политики задано значение false или она не настроена, данный элемент контекстного меню не будет добавлен.

Чтобы узнать больше о режиме Internet Explorer, см. [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: InternetExplorerIntegrationLocalFileShowContextMenu
  - Имя GP: показать контекстное меню для открытия ссылки в режиме Internet Explorer
  - Путь к GP (обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: InternetExplorerIntegrationLocalFileShowContextMenu
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### InternetExplorerIntegrationSiteList

  #### Настройка списка сайтов для режима Enterprise

  
  
  #### Поддерживаемые версии:

  - В Windows с 78 и более поздних версий

  #### Описание

  Инструкции по настройке оптимального режима для режима Internet Explorer см. [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: InternetExplorerIntegrationSiteList
  - Имя GP: Настройка списка сайтов в режиме предприятия
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: InternetExplorerIntegrationSiteList
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"https://internal.contoso.com/sitelist.xml"
```

  

  [В начало](#microsoft-edge---policies)

  ### InternetExplorerIntegrationSiteRedirect

  #### Укажите, как ведут себя внутренние переходы на ненастроенные сайты при запуске со страниц режима Internet Explorer.

  
  
  #### Поддерживаемые версии:

  - В Windows с 81 и более поздних версий

  #### Описание

  Навигация «внутри страницы» запускается из ссылки, скрипта или формы на текущей странице. Это также может быть перенаправление на стороне сервера предыдущей попытки навигации внутри страницы. И наоборот, пользователь может запустить навигацию, которая не является «внутри страницы» и которая не зависит от текущей страницы, несколькими способами, используя элементы управления браузера. Например, используя адресную строку, кнопку «Назад» или избранную ссылку.

Этот параметр позволяет указать, будут ли переходы от страниц, загруженных в режиме Internet Explorer, к ненастроенным сайтам (которые не настроены в списке сайтов в режиме Enterprise) переключаться обратно на Microsoft Edge или оставаться в режиме Internet Explorer.

Этот параметр работает в сочетании с [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) со значением «IEMode» и политикой [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist), где список содержит хотя бы одну запись.

Если вы отключите или не настроите эту политику, в этом режиме будут открываться только сайты, настроенные на открытие в режиме Internet Explorer. Все сайты, не настроенные для открытия в режиме Internet Explorer, будут перенаправляться обратно в Microsoft Edge.

Если для этой политики задано значение «Default», в этом режиме будут открываться только сайты, настроенные для открытия в режиме Internet Explorer. Все сайты, не настроенные для открытия в режиме Internet Explorer, будут перенаправляться обратно в Microsoft Edge.

Если вы установите для этой политики значение «AutomaticNavigationsOnly», вы получите опыт по умолчанию, за исключением того, что все автоматические переходы (например, перенаправления 302) на ненастроенные сайты будут сохраняться в режиме Internet Explorer.

Если для этой политики задано значение «AllInPageNavigations», все переходы от страниц, загруженных в режиме IE, к ненастроенным сайтам, сохраняются в режиме Internet Explorer (как минимум, рекомендуется).

Чтобы узнать больше о режиме Internet Explorer, см. [https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106)

Сопоставление параметров политики:

* Default (0) = По умолчанию

* AutomaticNavigationsOnly (1) = Сохранить только автоматическую навигацию в режиме Internet Explorer

* AllInPageNavigations (2) = Сохранить все переходы по страницам в режиме Internet Explorer

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: InternetExplorerIntegrationSiteRedirect
  - Имя GP: укажите, как ведут себя переходы «внутри страницы» к ненастроенным сайтам при запуске со страниц режима Internet Explorer.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: InternetExplorerIntegrationSiteRedirect
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  

  [В начало](#microsoft-edge---policies)

  ### InternetExplorerIntegrationTestingAllowed

  #### Разрешить тестирование режима Internet Explorer

  
  
  #### Поддерживаемые версии:

  - В Windows — версия 86 или более поздние

  #### Описание

  Эта политика позволяет пользователям проверять приложения в режиме Internet Explorer, открыв вкладку режима Internet Explorer в Microsoft Edge.

Это можно сделать с помощью меню "Другие инструменты", выбрав пункт "Открыть сайты в режиме Internet Explorer".

Кроме того, пользователи могут проверить приложения в современном браузере, не удаляя их из списка сайтов с помощью команды "Открыть сайты в режиме Microsoft Edge".

Этот параметр работает в сочетании с [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) со значением «IEMode» и политикой [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist), где список содержит хотя бы одну запись.

Если эта политика включена, команда "Открыть сайты в режиме Internet Explorer" будет отображаться в разделе "Другие инструменты". На этой вкладке пользователи могут просматривать свои сайты в режиме Internet Explorer. Другой вариант функции "Открыть сайты в режиме Microsoft Edge" также будет отображаться в разделе "Другие инструменты", чтобы проверить сайты в современном браузере, не удаляя их из списка сайтов.

Если отключить или не настроить эту политику, пользователи не смогут увидеть параметры "Открыть в режиме Internet Explorer" и "Открыть в режиме Microsoft Edge" в меню "Другие инструменты". Тем не менее, пользователи могут настраивать эти параметры с помощью флага --ie-mode-test.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: InternetExplorerIntegrationTestingAllowed
  - Имя групповой политики: Разрешить тестирование режима Internet Explorer
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: InternetExplorerIntegrationTestingAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  

  [В начало](#microsoft-edge---policies)

  ### IntranetRedirectBehavior

  #### Поведение перенаправления в интрасети

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 88 или позже

  #### Описание

  Эта политика настраивает поведение перенаправления интрасети с помощью проверок перехвата DNS. Проверки пытаются определить наличие браузера за прокси-сервером, который перенаправляет неизвестные имена хостов.

Если эта политика не настроена, браузер будет использовать поведение по умолчанию для проверок перехвата DNS и вариантов перенаправления в интрасети. В M88 они включены по умолчанию, но будут отключены по умолчанию в будущем выпуске.

[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled) — это связанная политика, которая также может отключить проверки перехвата DNS. Однако эта политика является более гибкой версией, которая может отдельно управлять информационными панелями перенаправления в интрасети. Возможно, она будет развернута в будущем.
Если [DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled) или эта политика запросит отключение проверок перехвата, проверки будут отключены.
Если проверки перехвата DNS отключены с помощью этой политики, но политика [GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar) включена, однословные запросы по-прежнему можно будет использовать для переходов в интрасети.

Сопоставление параметров политики:

* Default (0) = использовать поведение браузера по умолчанию.

* DisableInterceptionChecksDisableInfobar (1) = отключить проверки перехвата DNS и информационные панели "http://intranetsite/" ("имелось в виду").

* DisableInterceptionChecksEnableInfobar (2) = отключить проверки перехвата DNS; разрешить информационные панели "http://intranetsite/" ("имелось в виду").

* EnableInterceptionChecksEnableInfobar (3) = разрешить проверки перехвата DNS и информационные панели "http://intranetsite/" ("имелось в виду").

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: IntranetRedirectBehavior
  - Имя GP: поведение перенаправления в интрасети
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: IntranetRedirectBehavior
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа настройки: IntranetRedirectBehavior
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### IsolateOrigins

  #### Включить изоляцию сайта для определенных источников

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Укажите источники для запуска в отдельности, в своем собственном процессе.

Эта политика также изолирует источники, названные под-доменами - например, указание https://contoso.com/ приведет к изоляции https://foo.contoso.com/ как части сайта https://contoso.com/.

Если политика включена, каждый из названных источников в списке через запятую будет выполняться в своем собственном процессе.

Если вы отключите эту политику, то функции IsolateOrigins и SitePerProcess будут отключены. Пользователи по-прежнему могут включить политику IsolateOrigins вручную с помощью флагов командной строки.

Если вы не настроите политику, пользователь может изменить этот параметр.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: IsolateOrigins
  - Имя GP: Включить изоляцию сайта для определенных источников
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: IsolateOrigins
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"https://contoso.com/,https://fabrikam.com/"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: IsolateOrigins
  - Пример значения:
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### LocalProvidersEnabled

  #### Разрешить предложения от местных поставщиков

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 83 и более поздних версий

  #### Описание

  Разрешить предложения от поставщиков предложений на устройстве (локальные поставщики), например «Избранное» и «История просмотров», в адресной строке Microsoft Edge и в списке автоматических советов.

Если вы включите эту политику, будут использоваться предложения от местных поставщиков.

Если вы отключите эту политику, предложения от местных поставщиков никогда не будут использоваться. Местная история и местные избранные предложения не появятся.

Если вы не настроите эту политику, предложения от местных поставщиков будут разрешены, но пользователь может изменить это с помощью переключателя настроек.

Обратите внимание, что некоторые функции могут быть недоступны, если была применена политика отключения этой функции. Например, предложения журнала посещений будут недоступны, если вы включите политику [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled).

Эта политика требует перезагрузки браузера для завершения применения.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: LocalProvidersEnabled
  - Имя врача: Разрешить предложения от местных провайдеров
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: LocalProvidersEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: LocalProvidersEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ManagedConfigurationPerOrigin

  #### Задает определенные значения управляемой конфигурации для веб-сайтов

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с версии 90 или более поздней

  #### Описание

  При установке этой политики определяется возвращаемое значение API управляемой конфигурации для данного источника.

 API управляемой конфигурации — это конфигурация "ключ-значение", доступ к которой можно получить с помощью вызова javascript navigator.device.getManagedConfiguration(). Этот API доступен только тем источникам, которые соответствуют принудительно установленным веб-приложениям через [WebAppInstallForceList.](#webappinstallforcelist)


  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Dictionary

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ManagedConfigurationPerOrigin
  - Название GP: Задает значения управляемой конфигурации для веб-сайтов в определенных источниках
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): Н/Д
  - Имя значения: ManagedConfigurationPerOrigin
  - Тип значения: REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\ManagedConfigurationPerOrigin = [
  {
    "managed_configuration_hash": "asd891jedasd12ue9h", 
    "managed_configuration_url": "https://static.contoso.com/configuration.json", 
    "origin": "https://www.contoso.com"
  }, 
  {
    "managed_configuration_hash": "djio12easd89u12aws", 
    "managed_configuration_url": "https://static.contoso.com/configuration2.json", 
    "origin": "https://www.example.com"
  }
]
```

  ##### Компактный пример значения:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ManagedConfigurationPerOrigin = [{"managed_configuration_hash": "asd891jedasd12ue9h", "managed_configuration_url": "https://static.contoso.com/configuration.json", "origin": "https://www.contoso.com"}, {"managed_configuration_hash": "djio12easd89u12aws", "managed_configuration_url": "https://static.contoso.com/configuration2.json", "origin": "https://www.example.com"}]
  ```
  

  #### Сведения о Mac и параметры
  
  - Имя ключа предпочтения: ManagedConfigurationPerOrigin
  - Пример значения:
``` xml
<key>ManagedConfigurationPerOrigin</key>
<array>
  <dict>
    <key>managed_configuration_hash</key>
    <string>asd891jedasd12ue9h</string>
    <key>managed_configuration_url</key>
    <string>https://static.contoso.com/configuration.json</string>
    <key>origin</key>
    <string>https://www.contoso.com</string>
  </dict>
  <dict>
    <key>managed_configuration_hash</key>
    <string>djio12easd89u12aws</string>
    <key>managed_configuration_url</key>
    <string>https://static.contoso.com/configuration2.json</string>
    <key>origin</key>
    <string>https://www.example.com</string>
  </dict>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### ManagedFavorites

  #### Настроить избранное

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настраивает список управляемых избранных.

Политика создает список избранного. Каждый фаворит содержит ключи «имя» и «URL», которые содержат имя фаворита и его цель. Вы можете настроить подпапку, определив избранное без ключа "url", но с дополнительным ключом «дети», который содержит список избранного, как определено выше (некоторые из которых могут снова быть папками). Microsoft Edge исправляет неполные URL-адреса, как если бы они были отправлены через адресную строку, например, «microsoft.com» становится "https://microsoft.com/".

Эти избранное помещаются в папку, которую пользователь не может изменить (но пользователь может скрыть ее из панели избранного). По умолчанию имя папки - «Управляемые избранные», но вы можете изменить его, добавив в список избранных словарь, содержащий ключ «toplevel_name» с нужным именем папки в качестве значения.

Управляемые избранное не синхронизируются с учетной записью пользователя и не могут быть изменены расширениями.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Dictionary

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ManagedFavorites
  - Имя GP: Настройка избранного
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ManagedFavorites
  - Тип значения: REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\ManagedFavorites = [
  {
    "toplevel_name": "My managed favorites folder"
  }, 
  {
    "name": "Microsoft", 
    "url": "microsoft.com"
  }, 
  {
    "name": "Bing", 
    "url": "bing.com"
  }, 
  {
    "children": [
      {
        "name": "Microsoft Edge Insiders", 
        "url": "www.microsoftedgeinsider.com"
      }, 
      {
        "name": "Microsoft Edge", 
        "url": "www.microsoft.com/windows/microsoft-edge"
      }
    ], 
    "name": "Microsoft Edge links"
  }
]
```

  ##### Компактный пример значения:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ManagedFavorites = [{"toplevel_name": "My managed favorites folder"}, {"name": "Microsoft", "url": "microsoft.com"}, {"name": "Bing", "url": "bing.com"}, {"children": [{"name": "Microsoft Edge Insiders", "url": "www.microsoftedgeinsider.com"}, {"name": "Microsoft Edge", "url": "www.microsoft.com/windows/microsoft-edge"}], "name": "Microsoft Edge links"}]
  ```
  

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ManagedFavorites
  - Пример значения:
``` xml
<key>ManagedFavorites</key>
<array>
  <dict>
    <key>toplevel_name</key>
    <string>My managed favorites folder</string>
  </dict>
  <dict>
    <key>name</key>
    <string>Microsoft</string>
    <key>url</key>
    <string>microsoft.com</string>
  </dict>
  <dict>
    <key>name</key>
    <string>Bing</string>
    <key>url</key>
    <string>bing.com</string>
  </dict>
  <dict>
    <key>children</key>
    <array>
      <dict>
        <key>name</key>
        <string>Microsoft Edge Insiders</string>
        <key>url</key>
        <string>www.microsoftedgeinsider.com</string>
      </dict>
      <dict>
        <key>name</key>
        <string>Microsoft Edge</string>
        <key>url</key>
        <string>www.microsoft.com/windows/microsoft-edge</string>
      </dict>
    </array>
    <key>name</key>
    <string>Microsoft Edge links</string>
  </dict>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### ManagedSearchEngines

  #### Управление поисковыми движками

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет настроить список из 10 поисковых систем, одна из которых должна быть помечена как поисковая система по умолчанию.
Вам не нужно указывать кодировку. Начиная с Microsoft Edge 80, параметры offer_url и image_search_url являются необязательными. Необязательный параметр image_search_post_params (состоит из разделенных запятыми пар имя / значение) доступен начиная с Microsoft Edge 80.

Начиная с Microsoft Edge 83, вы можете включить поиск в поисковой системе с помощью необязательного параметра allow_search_engine_discovery. Этот параметр должен быть первым элементом в списке. Если параметр allow_search_engine_discovery не указан, по умолчанию поиск в поисковых системах будет отключен. Начиная с Microsoft Edge 84, эту политику можно установить в качестве рекомендуемой политики, которая позволяет обнаруживать службу поиска. Добавлять необязательный параметр allow_search_engine_discovery не требуется.

Если вы включите эту политику, пользователи не смогут добавлять, удалять или изменять любые поисковые системы в списке. Пользователи могут установить свою поисковую систему по умолчанию на любую поисковую систему в списке.

Если вы отключите или не настроите эту политику, пользователи могут изменять список поисковых систем по своему усмотрению.

Если установлена политика [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl), эта политика (ManagedSearchEngines) игнорируется. Пользователь должен перезапустить свой браузер, чтобы завершить применение этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Dictionary

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ManagedSearchEngines
  - Название GP: Управление поисковыми системами
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ManagedSearchEngines
  - Тип значения: REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\ManagedSearchEngines = [
  {
    "allow_search_engine_discovery": true
  }, 
  {
    "is_default": true, 
    "keyword": "example1.com", 
    "name": "Example1", 
    "search_url": "https://www.example1.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example1.com/qbox?query={searchTerms}"
  }, 
  {
    "image_search_post_params": "content={imageThumbnail},url={imageURL},sbisrc={SearchSource}", 
    "image_search_url": "https://www.example2.com/images/detail/search?iss=sbiupload", 
    "keyword": "example2.com", 
    "name": "Example2", 
    "search_url": "https://www.example2.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example2.com/qbox?query={searchTerms}"
  }, 
  {
    "encoding": "UTF-8", 
    "image_search_url": "https://www.example3.com/images/detail/search?iss=sbiupload", 
    "keyword": "example3.com", 
    "name": "Example3", 
    "search_url": "https://www.example3.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example3.com/qbox?query={searchTerms}"
  }, 
  {
    "keyword": "example4.com", 
    "name": "Example4", 
    "search_url": "https://www.example4.com/search?q={searchTerms}"
  }
]
```

  ##### Компактный пример значения:

  ```
  SOFTWARE\Policies\Microsoft\Edge\ManagedSearchEngines = [{"allow_search_engine_discovery": true}, {"is_default": true, "keyword": "example1.com", "name": "Example1", "search_url": "https://www.example1.com/search?q={searchTerms}", "suggest_url": "https://www.example1.com/qbox?query={searchTerms}"}, {"image_search_post_params": "content={imageThumbnail},url={imageURL},sbisrc={SearchSource}", "image_search_url": "https://www.example2.com/images/detail/search?iss=sbiupload", "keyword": "example2.com", "name": "Example2", "search_url": "https://www.example2.com/search?q={searchTerms}", "suggest_url": "https://www.example2.com/qbox?query={searchTerms}"}, {"encoding": "UTF-8", "image_search_url": "https://www.example3.com/images/detail/search?iss=sbiupload", "keyword": "example3.com", "name": "Example3", "search_url": "https://www.example3.com/search?q={searchTerms}", "suggest_url": "https://www.example3.com/qbox?query={searchTerms}"}, {"keyword": "example4.com", "name": "Example4", "search_url": "https://www.example4.com/search?q={searchTerms}"}]
  ```
  

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: ManagedSearchEngines
  - Пример значения:
``` xml
<key>ManagedSearchEngines</key>
<array>
  <dict>
    <key>allow_search_engine_discovery</key>
    <true/>
  </dict>
  <dict>
    <key>is_default</key>
    <true/>
    <key>keyword</key>
    <string>example1.com</string>
    <key>name</key>
    <string>Example1</string>
    <key>search_url</key>
    <string>https://www.example1.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example1.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>image_search_post_params</key>
    <string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
    <key>image_search_url</key>
    <string>https://www.example2.com/images/detail/search?iss=sbiupload</string>
    <key>keyword</key>
    <string>example2.com</string>
    <key>name</key>
    <string>Example2</string>
    <key>search_url</key>
    <string>https://www.example2.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example2.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>encoding</key>
    <string>UTF-8</string>
    <key>image_search_url</key>
    <string>https://www.example3.com/images/detail/search?iss=sbiupload</string>
    <key>keyword</key>
    <string>example3.com</string>
    <key>name</key>
    <string>Example3</string>
    <key>search_url</key>
    <string>https://www.example3.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example3.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>keyword</key>
    <string>example4.com</string>
    <key>name</key>
    <string>Example4</string>
    <key>search_url</key>
    <string>https://www.example4.com/search?q={searchTerms}</string>
  </dict>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### MaxConnectionsPerProxy

  #### Максимальное количество одновременных подключений к прокси-серверу

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Задает максимальное количество одновременных подключений к прокси-серверу.

Некоторые прокси-серверы не могут обрабатывать большое количество одновременных подключений на клиента - вы можете решить эту проблему, установив для этой политики более низкое значение.

Значение этой политики должно быть ниже 100 и выше 6. Значение по умолчанию: 32.

Известно, что некоторые веб-приложения используют много соединений с зависшими GET - снижение максимального числа соединений ниже 32 может привести к зависанию браузера в сети, если открыто слишком много таких веб-приложений.

Если вы не настроите эту политику, используется значение по умолчанию (32).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: MaxConnectionsPerProxy
  - Имя GP: Максимальное количество одновременных подключений к прокси-серверу.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: MaxConnectionsPerProxy
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000020
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: MaxConnectionsPerProxy
  - Пример значения:
``` xml
<integer>32</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### MediaRouterCastAllowAllIPs

  #### Разрешить Google Cast подключаться к устройствам Cast на всех IP-адресах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Включите эту политику, чтобы разрешить Google Cast подключаться к устройствам Cast по всем IP-адресам, а не только по частным адресам RFC1918/RFC4193.

Отключите эту политику, чтобы ограничить использование устройств Google Cast to Cast частными адресами RFC1918/RFC4193.

Если вы не настроите эту политику, Google Cast подключится к устройствам Cast только по частным адресам RFC1918/RFC4193, если вы не включите функцию CastAllowAllIPs.

Если политика [EnableMediaRouter](#enablemediarouter) отключена, эта политика не действует.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: MediaRouterCastAllowAllIPs
  - Имя GP: Разрешить Google Cast подключаться к устройствам Cast на всех IP-адресах.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: MediaRouterCastAllowAllIPs
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: MediaRouterCastAllowAllIPs
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### MetricsReportingEnabled

  #### Включить отчеты с данными об использовании и сбоях данных (устаревшие)

  
  >УСТАРЕЛО: эта политика устарела и не работает в версиях Microsoft Edge после 88.
  #### Поддерживаемые версии:

  - В Windows и macOS — версии c 77 по 88

  #### Описание

  Эта политика больше не поддерживается. Она заменяется на [DiagnosticData](#diagnosticdata) (для Windows 7, Windows 8 и macOS) и Allow Telemetry on Win 10 ( [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569) ).

Эта политика позволяет отправлять отчеты с данными об использовании и сбоях Microsoft Edge в корпорацию Майкрософт.

Включите эту политику, чтобы отправлять отчеты с данными об использовании и сбоях в корпорацию Майкрософт. Отключите эту политику, чтобы не отправлять эти данные в корпорацию Майкрософт. В обоих случаях пользователи не смогут изменить или переопределить его.

В Windows 10, если вы не настроите эту политику, Microsoft Edge по умолчанию будет использовать параметр диагностических данных Windows. Если вы включите эту политику, Microsoft Edge будет отправлять данные об использовании только в том случае, если для параметра данных диагностики Windows установлено значение «Расширенный» или «Полный». Если вы отключите эту политику, Microsoft Edge не будет отправлять данные об использовании. Данные о сбоях отправляются в зависимости от параметра диагностических данных Windows. Подробнее о настройках данных диагностики Windows можно узнать на [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

В Windows 7, Windows 8 и macOS эта политика управляет отправкой данных об использовании и сбоях. Если вы не настроите эту политику, Microsoft Edge по умолчанию будет использовать настройки пользователя.

Чтобы включить эту политику, параметру [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) требуется присвоить значение "Включено". Если параметру [MetricsReportingEnabled](#metricsreportingenabled) или [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) присвоено значение "Не настроено" или "Отключено", эти данные не отправляются в корпорацию Майкрософт.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством, или экземпляров macOS, управляемых с помощью MDM или присоединенных к домену посредством MCX.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: MetricsReportingEnabled
  - Имя GP: Включить отчеты с данными об использовании и сбоях данных (устаревший)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: MetricsReportingEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: MetricsReportingEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### NativeWindowOcclusionEnabled

  #### Включить загораживание собственного окна (устарело)

  >УСТАРЕЛО: эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:

  - В Windows с 84 и более поздних версий

  #### Описание

  Эта политика устарела, используйте вместо нее политику [WindowOcclusionEnabled](#windowocclusionenabled). Она не будет работать в Microsoft Edge версии 92.

Включает загораживание собственного окна в Microsoft Edge.

Если вы включите этот параметр, чтобы снизить нагрузку на процессор и энергопотребление, Microsoft Edge будет определять, когда окно закрыто другими окнами, и приостанавливать работу рисования пикселей.

Если вы отключите этот параметр, Microsoft Edge не будет определять, когда окно закрыто другими окнами.

Если эта политика не настроена, обнаружение загораживания будет включено.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: NativeWindowOcclusionEnabled
  - Имя групповой политики: включить загораживание собственного окна (устарело)
  - Путь к групповой политике (обязательно): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: NativeWindowOcclusionEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### NavigationDelayForInitialSiteListDownloadTimeout

  #### Установка времени ожидания перехода между вкладками списка сайтов для режима предприятия

  
  
  #### Поддерживаемые версии:

  - В Windows с 84 и более поздних версий

  #### Описание

  Позволяет установить время ожидания в секундах при переходе между вкладками Microsoft Edge, требуемое для загрузки браузером исходного списка сайтов для режима предприятия.

Этот параметр работает при выполнении следующих условий: параметр [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) имеет значение «IEMode», в политике [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) имеется хотя бы одна запись, а параметр [DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload) имеет значение «Все соответствующие переходы» (1).

Вкладки будут ожидать загрузки списка сайтов для режима предприятия не дольше этого времени. Если до истечения этого времени браузер не завершил загрузку списка сайтов для режима предприятия, переход между вкладками Microsoft Edge все равно будет выполнен. Значение времени ожидания должно быть не больше 20 секунд и не меньше 1 секунды.

Если для времени ожидания задано значение, больше используемого по умолчанию значения в 2 секунды, то по прошествии 2 секунд для пользователя отобразится информационная панель. На информационной панели есть кнопка, с помощью которой пользователь может завершить ожидание загрузки списка сайтов для режима предприятия.

Если эта политика не настроена, то используется установленное по умолчанию время ожидания в 2секунды. Это значение по умолчанию в будущем может быть изменено.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NavigationDelayForInitialSiteListDownloadTimeout
  - Имя GP: Установка времени ожидания перехода между вкладками списка сайтов для режима предприятия
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: NavigationDelayForInitialSiteListDownloadTimeout
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x0000000a
```

  

  [В начало](#microsoft-edge---policies)

  ### NetworkPredictionOptions

  #### Включить прогнозирование сети

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Включает прогнозирование сети и запрещает пользователям изменять этот параметр.

Он контролирует предварительную выборку DNS, предварительное подключение TCP и SSL и предварительную визуализацию веб-страниц.

Если вы не настроите эту политику, предсказание сети будет включено, но пользователь может изменить его.

Сопоставление параметров политики:

* NetworkPredictionAlways (0) = Прогнозировать сетевые действия при любом сетевом соединении

* NetworkPredictionWifiOnly (1) = Не поддерживается. При использовании этого значения оно будет восприниматься так же, как установка параметра "Прогнозировать сетевые действия при любом сетевом соединении" (0)

* NetworkPredictionNever (2) = Не прогнозировать сетевые действия при любом сетевом соединении

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NetworkPredictionOptions
  - Имя GP: Включить прогнозирование сети
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: NetworkPredictionOptions
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: NetworkPredictionOptions
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### NonRemovableProfileEnabled

  #### Настройте, всегда ли у пользователя профиль по умолчанию автоматически входит в свою учетную запись на работе или в школе

  
  
  #### Поддерживаемые версии:

  - В Windows с 78 и более поздних версий

  #### Описание

  Эта политика определяет, может ли пользователь удалить профиль Microsoft Edge, автоматически вошедший в учетную запись пользователя для работы или школы.

Если вы включите эту политику, в Windows будет создан несъемный профиль с учетной записью пользователя или учебой. Этот профиль нельзя выписать или удалить. Профиль будет недоступен для удаления только в том случае, если профиль подключился к локальной учетной записи или учетной записи Azure AD, которая соответствует учетной записи ОС.

Если вы отключите или не настроите эту политику, профиль, автоматически входящий в учетную запись пользователя для работы или учебы в Windows, может быть подписан или удален пользователем.

Если вы хотите настроить вход в браузер, используйте политику [BrowserSignin](#browsersignin).

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, а также экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством.

Если в Microsoft Edge 89 и далее существует локальный профиль с отключенной синхронизацией и компьютер гибриден, он автоматически обновит его до профиля Azure AD и сделает его недоступным для удаления вместо создания нового недоступного для удаления профиля Azure AD.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: NonRemovableProfileEnabled
  - Имя GP: Укажите, всегда ли у пользователя профиль по умолчанию автоматически входит в свою учетную запись на работе или в школе.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: NonRemovableProfileEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### OverrideSecurityRestrictionsOnInsecureOrigin

  #### Контроль, где применяются ограничения безопасности для небезопасных источников

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Указывает список источников (URL) или шаблонов имен хостов (например, "*.contoso.com"), для которых не применяются ограничения безопасности для незащищенных источников.

Эта политика позволяет указать разрешенные источники для устаревших приложений, которые не могут развернуть TLS, или настроить промежуточный сервер для внутренней веб-разработки, чтобы разработчики могли тестировать функции, требующие безопасного контекста, без необходимости развертывания TLS на промежуточном сервере. Эта политика также не допускает, чтобы источник был помечен как «Незащищенный» в омнибоксе.

Установка списка URL-адресов в этой политике имеет тот же эффект, что и установка флага командной строки '--unsafely-Treat-insecure-origin-as-secure' в список разделенных запятыми тех же URL-адресов. Если вы включите эту политику, она переопределит флаг командной строки.

Для получения дополнительной информации о безопасных контекстах см. https://www.w3.org/TR/secure-contexts/

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: OverrideSecurityRestrictionsOnInsecureOrigin
  - Имя GP: Контроль, где применяются ограничения безопасности для небезопасных источников
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательно): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = "http://testserver.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = "*.contoso.com"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: OverrideSecurityRestrictionsOnInsecureOrigin
  - Пример значения:
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### PaymentMethodQueryEnabled

  #### Разрешить веб-сайтам запрашивать доступные способы оплаты

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 80 или позже

  #### Описание

  Позволяет указать, могут ли веб-сайты проверять, сохранены ли у пользователя методы оплаты.

Если вы отключите эту политику, веб-сайты, использующие API PaymentRequest.canMakePayment или PaymentRequest.hasEnrolledInstrument, будут проинформированы о том, что способы оплаты недоступны.

Если вы активируете эту политику или не устанавливаете ее, веб-сайты могут проверить, сохранены ли у пользователя способы оплаты.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PaymentMethodQueryEnabled
  - Название GP: Разрешить веб-сайтам запрашивать доступные способы оплаты
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: PaymentMethodQueryEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PaymentMethodQueryEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### PersonalizationReportingEnabled

  #### Разрешить персонализацию рекламы, поиска и новостей, отправляя историю просмотров в Microsoft

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 80 или позже

  #### Описание

  Эта политика запрещает Microsoft собирать пользовательскую историю посещений Microsoft Edge для персонализации рекламы, поиска, новостей и других служб Microsoft.

Этот параметр доступен только для пользователей с учетной записью Microsoft. Этот параметр недоступен для дочерних или корпоративных учетных записей.

Если вы отключите эту политику, пользователи не смогут изменить или переопределить настройку. Если эта политика включена или не настроена, Microsoft Edge будет использоваться по умолчанию 

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PersonalizationReportingEnabled
  - Имя GP: Разрешить персонализацию рекламы, поиска и новостей, отправляя историю просмотров в Microsoft
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: PersonalizationReportingEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PersonalizationReportingEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### PinningWizardAllowed

  #### Мастер «Разрешить закрепление на панели задач»

  
  
  #### Поддерживаемые версии:

  - В Windows с 80 и более поздних версий

  #### Описание

  Microsoft Edge использует мастер закрепления на панели задач, чтобы помочь пользователям закрепить предлагаемые сайты на панели задач. Функция мастера «Прикрепить к панели задач» включена по умолчанию и доступна пользователю через меню «Настройки» и другие параметры.

Если вы включите эту политику или не настроите ее, пользователи смогут вызывать мастера «Прикрепить к панели задач» из меню «Параметры» и «Еще». Мастер также может быть вызван через запуск протокола.

Если вы отключите эту политику, мастер «Прикрепить к панели задач» будет отключен в меню и не может быть вызван при запуске протокола.

Пользовательские настройки для включения или отключения мастера прикрепления к панели задач недоступны.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PinningWizardAllowed
  - Имя GP: Разрешить привязку к мастеру панели задач
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: PinningWizardAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  

  [В начало](#microsoft-edge---policies)

  ### ProactiveAuthEnabled

  #### Включение проактивной проверки подлинности (не рекомендуется)

  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Эта политика устарела, так как она не работает независимо от входных данных браузера. Она не будет работать в Microsoft Edge версии 91. Если вы хотите настроить вход в браузер, используйте политику [BrowserSignin](#browsersignin).

Позволяет настроить включение упреждающего способа проверки подлинности в Microsoft Edge.

Если эта политика включена, Microsoft Edge будет выполнять проверку подлинности на веб-сайтах и в службах с учетной записью, с помощью которой выполнен вход в браузер.

Если этот параметр отключен, Microsoft Edge не будет выполнять проверку подлинности на веб-сайтах и в службах с помощью единого входа (SSO). Возможности проверки подлинности, такие как корпоративная новая вкладка, не будут работать (например, последние и рекомендуемые документы Office не будут доступны).

Если эта политика не настроена, функция упреждающего способа проверки подлинности включена.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ProactiveAuthEnabled
  - Имя GP: Включение проактивной проверки подлинности (не рекомендуется)
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ProactiveAuthEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ProactiveAuthEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### PromotionalTabsEnabled

  #### Включить рекламный контент на всей вкладке

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Контролируйте презентацию рекламного или образовательного контента с полной вкладкой. Этот параметр управляет отображением страниц приветствия, которые помогают пользователям войти в Microsoft Edge, выбрать браузер по умолчанию или узнать о функциях продукта.

Если вы включите эту политику (установите ее значение true) или не настроите ее, Microsoft Edge может показывать пользователям содержимое полной вкладки, чтобы предоставить информацию о продукте.

Если вы отключите (установите как false) эту политику, Microsoft Edge не сможет показывать пользователям содержимое полной вкладки.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PromotionalTabsEnabled
  - Название GP: Включить рекламный контент на полной вкладке
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: PromotionalTabsEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PromotionalTabsEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### PromptForDownloadLocation

  #### Спросите, где сохранить загруженные файлы

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Укажите, нужно ли спрашивать, где сохранить файл перед его загрузкой.

Если вы включите эту политику, пользователю будет предложено сохранить каждый файл перед загрузкой; если вы не настроите его, файлы будут автоматически сохранены в папку по умолчанию, без запроса пользователя.

Если вы не настроите эту политику, пользователь сможет изменить этот параметр.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: PromptForDownloadLocation
  - Имя GP: Спросите, где сохранить загруженные файлы
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: PromptForDownloadLocation
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: PromptForDownloadLocation
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### QuicAllowed

  #### Разрешить протокол QUIC

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет использовать протокол QUIC в Microsoft Edge.

Если вы включите эту политику или не настроите ее, протокол QUIC будет разрешен.

Если вы отключите эту политику, протокол QUIC будет заблокирован.

QUIC - это сетевой протокол транспортного уровня, который может улучшить производительность веб-приложений, которые в настоящее время используют TCP.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: QuicAllowed
  - Имя GP: Разрешить протокол QUIC
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: QuicAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: QuicAllowed
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### QuickViewOfficeFilesEnabled

  #### Управление возможностью быстрого просмотра файлов Office в Microsoft Edge

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с версии 90 или более поздней

  #### Описание

  Позволяет указать, могут ли пользователи просматривать в Интернете файлы Office, не находящиеся в OneDrive или SharePoint (например, документы Word, презентации PowerPoint и электронные таблицы Excel).

Если вы включите или не настроите эту политику, файлы можно будет просматривать в Microsoft Edge с помощью средства просмотра Office, не скачивая их.

Если вы отключите эту политику, файлы потребуется скачать для просмотра.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: QuickViewOfficeFilesEnabled
  - Имя GP: Управление возможностью быстрого просмотра файлов Office в Microsoft Edge
  - Путь к GP (обязательный): Administrative Templates/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: QuickViewOfficeFilesEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и параметры
  
  - Предпочитаемое имя ключа: QuickViewOfficeFilesEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### RedirectSitesFromInternetExplorerPreventBHOInstall

  #### Запрет установки объекта BHO для перенаправления несовместимых сайтов из Internet Explorer в Microsoft Edge

  
  
  #### Поддерживаемые версии:

  - В Windows 87 и более поздних версий

  #### Описание

  Этот параметр позволяет указать, следует ли блокировать установку вспомогательного объекта браузера (BHO), который поддерживает перенаправление несовместимых сайтов из Internet Explorer в Microsoft Edge для сайтов, требующих современный браузер.

Если включить эту политику, вспомогательный объект браузера не будет установлен. Если приложение уже установлено, оно будет удалено при следующем обновлении Microsoft Edge.

Если эта политика не настроена или отключена, вспомогательный объект браузера будет установлен.

Вспомогательный объект браузера необходим для перенаправления несовместимого сайта, но даже если перенаправление не выполняется,он управляется [RedirectSitesFromInternetExplorerRedirectMode](#redirectsitesfrominternetexplorerredirectmode).

Дополнительные сведения об этой политике см. в статье [https://go.microsoft.com/fwlink/?linkid=2141715](https://go.microsoft.com/fwlink/?linkid=2141715)

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: RedirectSitesFromInternetExplorerPreventBHOInstall
  - Имя GP: Запрет установки объекта BHO для перенаправления несовместимых сайтов из Internet Explorer в Microsoft Edge
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: RedirectSitesFromInternetExplorerPreventBHOInstall
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### RedirectSitesFromInternetExplorerRedirectMode

  #### Перенаправление несовместимых сайтов из Internet Explorer в Microsoft Edge

  
  
  #### Поддерживаемые версии:

  - В Windows 87 и более поздних версий

  #### Описание

  Этот параметр позволяет указать, будет ли Internet Explorer перенаправлять навигацию на сайты, требующие современный браузер в Microsoft Edge.

Если не настроить эту политику или присвоить ей значение "Sitelist" (Список сайтов), начиная с M87, Internet Explorer будет перенаправлять сайты, требующие современный браузер в Microsoft Edge.

При перенаправлении сайта из Internet Explorer в Microsoft Edge вкладка Internet Explorer, на которой началась загрузка сайта, закрывается, если для нее не предоставлено предварительное согласие. В противном случае выполняется переход на страницу справки от Майкрософт, объясняющую причину перенаправления сайта в Microsoft Edge.

При запуске Microsoft Edge для загрузки сайта из Internet Explorer пользователю будет доступна информационная панель, объясняющая, что сайт лучше всего подходит для современного браузера.

Если для этой политики задано значение "Отключить", Internet Explorer не будет перенаправлять трафик в Microsoft Edge.

Дополнительные сведения об этой политике см. в статье  [https://go.microsoft.com/fwlink/?linkid=2141715](https://go.microsoft.com/fwlink/?linkid=2141715)

Сопоставление параметров политики:

* Disable (0) = Отключить

* Sitelist (1) = Перенаправление сайтов на основе списка несовместимых сайтов

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: RedirectSitesFromInternetExplorerRedirectMode
  - Имя GP: Перенаправление несовместимых сайтов из Internet Explorer в Microsoft Edge
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: RedirectSitesFromInternetExplorerRedirectMode
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### RelaunchNotification

  #### Уведомить пользователя, что перезагрузка браузера рекомендуется или требуется для ожидающих обновлений

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Сообщите пользователям, что им нужно перезапустить Microsoft Edge, чтобы применить ожидающее обновление.

Если вы не настроите эту политику, Microsoft Edge добавит значок корзины в дальнем правом углу верхней строки меню, чтобы предложить пользователям перезапустить браузер, чтобы применить обновление.

Если вы включите эту политику и установите для нее значение «Recommended», повторяющееся предупреждение предлагает пользователям рекомендовать перезагрузку. Пользователи могут отклонить это предупреждение и отложить перезапуск.

Если для политики задано значение «Required», повторяющееся предупреждение запрашивает пользователей о том, что браузер будет перезапущен автоматически, как только пройдет период уведомления. Период по умолчанию составляет семь дней. Вы можете настроить этот период с помощью политики [RelaunchNotificationPeriod](#relaunchnotificationperiod).

Сеанс пользователя восстанавливается при перезапуске браузера.

Сопоставление параметров политики:

* Recommended (1) = Рекомендуется - показать пользователю повторяющееся приглашение, указывающее, что рекомендуется перезагрузка

* Required (2) = Обязательно - показать пользователю повторяющееся приглашение, указывающее, что требуется перезагрузка

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: RelaunchNotification
  - Имя GP: Уведомить пользователя о том, что перезагрузка браузера рекомендуется или требуется для ожидающих обновлений
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: RelaunchNotification
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: RelaunchNotification
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### RelaunchNotificationPeriod

  #### Установите период времени для уведомлений об обновлениях

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет вам установить период времени в миллисекундах, в течение которого пользователи будут уведомлены о том, что Microsoft Edge должен быть перезапущен для применения ожидающего обновления.

В течение этого периода времени пользователь будет неоднократно уведомляться о необходимости обновления. В Microsoft Edge меню приложения изменяется, чтобы указать, что перезапуск необходим, когда прошла одна треть периода уведомления. Это уведомление меняет цвет по истечении двух третей периода уведомления и снова по истечении полного периода уведомления. Дополнительные уведомления, включенные политикой [RelaunchNotification](#relaunchnotification), следуют этому же графику.

Если не установлено, используется период по умолчанию 604800000 миллисекунд (одна неделя).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: RelaunchNotificationPeriod
  - Имя GP: Установите период времени для уведомлений об обновлениях.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: RelaunchNotificationPeriod
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x240c8400
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: RelaunchNotificationPeriod
  - Пример значения:
``` xml
<integer>604800000</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### RendererCodeIntegrityEnabled

  #### Включить целостность кода рендерера

  
  
  #### Поддерживаемые версии:

  - В Windows с 78 и более поздних версий

  #### Описание

  Если политика включена или не настроена, параметр целостности кода рендерера будет включен.
Отключение этой политики отрицательно сказывается на безопасности и стабильности Microsoft Edge, так как неизвестный и потенциально опасный код может загружаться в процессах рендерера Microsoft Edge. Отключайте эту политику, только если существуют проблемы совместимости со сторонним программным обеспечением, которое должно запускаться в процессах рендерера Microsoft Edge.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: RendererCodeIntegrityEnabled
  - Имя GP: Включить целостность кода рендерера
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: RendererCodeIntegrityEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  

  [В начало](#microsoft-edge---policies)

  ### RequireOnlineRevocationChecksForLocalAnchors

  #### Укажите, требуются ли онлайн-проверки OCSP / CRL для локальных якорей доверия

  
  
  #### Поддерживаемые версии:

  - В Windows с 77 и более поздних версий

  #### Описание

  Проверьте, требуются ли онлайн-проверки отзыва (проверки OCSP/CRL). Если Microsoft Edge не может получить информацию о состоянии отзыва, эти сертификаты считаются отозванными («сбои»).

Если вы включите эту политику, Microsoft Edge всегда выполняет проверку отзыва сертификатов сервера, которые успешно проходят проверку и подписаны локально установленными сертификатами CA.

Если вы не настроите или не отключите эту политику, Microsoft Edge использует существующие параметры проверки отзыва в Интернете.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: RequireOnlineRevocationChecksForLocalAnchors
  - Имя GP: Укажите, требуются ли онлайн-проверки OCSP/CRL для локальных якорей доверия.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: RequireOnlineRevocationChecksForLocalAnchors
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  

  [В начало](#microsoft-edge---policies)

  ### ResolveNavigationErrorsUseWebService

  #### Включить разрешение ошибок навигации с помощью веб-службы

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Разрешить Microsoft Edge выдавать соединение без данных с веб-службой для проверки сетей на предмет подключения в таких случаях, как Wi-Fi в отелях и аэропортах.

Если вы включите эту политику, веб-служба будет использоваться для тестов сетевого подключения.

Если вы отключите эту политику, Microsoft Edge будет использовать собственные API-интерфейсы для решения проблем сетевого подключения и навигации.

**Примечание**: За исключением Windows 8 и более поздних версий Windows, Microsoft Edge *всегда* использует собственные API-интерфейсы для решения проблем с подключением.

Если вы не настроите эту политику, Microsoft Edge учитывает пользовательские настройки, установленные в разделе «Сервисы на edge://settings/privacy.
В частности, есть переключатель **Использовать веб-сервис для устранения ошибок навигации**, который пользователь может включать или отключать. Помните, что если вы включили эту политику (ResolveNavigationErrorsUseWebService), параметр **Использовать веб-службу для устранения ошибок навигации** включен, но пользователь не может изменить параметр с помощью переключателя. Если вы отключили эту политику, параметр **Использовать веб-службу для устранения ошибок навигации** отключен, и пользователь не может изменить параметр с помощью переключателя.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ResolveNavigationErrorsUseWebService
  - Имя GP: Включить разрешение ошибок навигации с помощью веб-службы.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: ResolveNavigationErrorsUseWebService
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ResolveNavigationErrorsUseWebService
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### RestrictSigninToPattern

  #### Ограничить, какие учетные записи могут быть использованы в качестве основных учетных записей Microsoft Edge

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определяет, какие учетные записи могут быть установлены в качестве основных учетных записей обозревателя в Microsoft Edge (учетная запись, выбранная в ходе процесса синхронизации).

Если пользователь пытается настроить основную учетную запись браузера с именем пользователя, которое не соответствует этому шаблону, он блокируется и получает соответствующее сообщение об ошибке. Эту политику можно настроить для нескольких учетных записей, используя регулярное выражение в стиле Perl для шаблона. Обратите внимание, что при выявлении соответствия шаблонов учитывается регистр. Дополнительные сведения о используемых правилах для регулярных выражений см. в статье https://go.microsoft.com/fwlink/p/?linkid=2133903.

Если вы не настроите эту политику или оставите ее пустой, пользователи могут установить любую учетную запись в качестве основной учетной записи браузера в Microsoft Edge.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: RestrictSigninToPattern
  - Имя GP: Ограничение, какие учетные записи могут использоваться в качестве основных учетных записей Microsoft Edge.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: RestrictSigninToPattern
  - Тип значения: REG_SZ

  ##### Пример значения:

```
".*@contoso.com"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: RestrictSigninToPattern
  - Пример значения:
``` xml
<string>.*@contoso.com</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### RoamingProfileLocation

  #### Настройка каталога перемещаемого профиля

  
  
  #### Поддерживаемые версии:

  - В Windows — версия 85 или более поздние

  #### Описание

  Выполняет настройку каталога для хранения перемещаемой копии профиля.

Если эта политика включена, Microsoft Edge использует указанный каталог для хранения перемещаемой копии профиля (при условии, что политика [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) также включена). Если отключить политику [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) или не настраивать ее, то значение, хранящееся в этой политике, не будет использоваться.

Список переменных для использования см. в разделе [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

Если эта политика не настроена, то используется установленный по умолчанию путь к перемещаемому профилю.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: RoamingProfileLocation
  - Имя GP: Настройка каталога перемещаемого профиля
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: RoamingProfileLocation
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"${roaming_app_data}\\edge-profile"
```

  

  [В начало](#microsoft-edge---policies)

  ### RoamingProfileSupportEnabled

  #### Разрешение использования перемещаемых копий для данных профиля Microsoft Edge

  
  
  #### Поддерживаемые версии:

  - В Windows — версия 85 или более поздние

  #### Описание

  Включите эту политику, чтобы использовать перемещаемые профили в Windows. Параметры, сохраненные в профилях Microsoft Edge ("Избранное" и "Параметры"), также записываются в файл, хранящийся в папке перемещаемого профиля пользователя (или в расположении, заданном администратором с помощью политики [RoamingProfileLocation](#roamingprofilelocation)).

Если эта политика отключена или не настроена, будут использоваться только обычные локальные профили.

[SyncDisabled](#syncdisabled) отключает только облачную синхронизацию и не влияет на эту политику.

Дополнительные сведения об использовании перемещаемых профилей пользователей см. на странице [https://go.microsoft.com/fwlink/?linkid=2150058](https://go.microsoft.com/fwlink/?linkid=2150058).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: RoamingProfileSupportEnabled
  - Имя GP: Разрешение использования перемещаемых копий для данных профиля Microsoft Edge
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: RoamingProfileSupportEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### RunAllFlashInAllowMode

  #### Применить параметр содержимого Adobe Flash ко всему содержимому (устарело)

  
  >УСТАРЕЛО: эта политика устарела и не работает в версиях Microsoft Edge после 87.
  #### Поддерживаемые версии:

  - В Windows и macOS — версии c 77 по 87

  #### Описание

  Эта политика не работает, так как Flash больше не поддерживается Microsoft Edge.

Если вы включите эту политику, будет запущен весь контент Adobe Flash, встроенный в веб-сайты, для которых в настройках контента разрешено использование Adobe Flash - либо пользователем, либо политикой предприятия. Это включает в себя контент из других источников и/или небольшой контент.

Чтобы указать, каким веб-сайтам разрешено запускать Adobe Flash, см. Спецификации в политиках [DefaultPluginsSetting](#defaultpluginssetting), [PluginsAllowedForUrls](#pluginsallowedforurls), и [PluginsBlockedForUrls](#pluginsblockedforurls).

Если вы отключите эту политику или не настроите ее, содержимое Adobe Flash из других источников (с сайтов, которые не указаны в трех упомянутых выше политиках) или небольшое содержимое может быть заблокировано.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: RunAllFlashInAllowMode
  - Имя GP: применить параметр содержимого Adobe Flash ко всему содержимому (устарело)
  - Путь к GP (обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: RunAllFlashInAllowMode
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: RunAllFlashInAllowMode
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SSLErrorOverrideAllowed

  #### Разрешить пользователям продолжать работу со страницы предупреждения HTTPS

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Microsoft Edge показывает страницу с предупреждением, когда пользователи посещают сайты с ошибками SSL.

Если вы включите или не настроите (по умолчанию) эту политику, пользователи смогут переходить по этим страницам предупреждений.

Если вы отключите эту политику, пользователи не смогут нажимать на любую страницу с предупреждением.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SSLErrorOverrideAllowed
  - Имя групповой политики: разрешить пользователям продолжать работу со страницы предупреждения HTTPS
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: SSLErrorOverrideAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: SSLErrorOverrideAllowed
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SSLErrorOverrideAllowedForOrigins

  #### Разрешить пользователям продолжать работу со страницы предупреждения HTTPS для определенных источников

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с версии 90 или более поздней

  #### Описание

  Microsoft Edge показывает страницу с предупреждением, когда пользователи посещают сайты с ошибками SSL.

Если включить или не настроить политику [SSLErrorOverrideAllowed](#sslerroroverrideallowed), эта политика ничего не делает.

Если отключить политику [SSLErrorOverrideAllowed](#sslerroroverrideallowed), настройка этой политики позволит настроить список шаблонов источников для сайтов, на которых пользователи могут переходить по страницам ошибок SSL. Пользователи не могут переходить по страницам ошибок SSL в источниках, отсутствующих в этом списке.

Если не настроить эту политику, политика [SSLErrorOverrideAllowed](#sslerroroverrideallowed) применяется ко всем сайтам.

Подробные сведения о шаблонах допустимых источников см. на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). * не является допустимым значением для этой политики. Соответствие этой политики определяется только на основе источника, поэтому любой путь или запрос в шаблоне URL-адреса игнорируется.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: SSLErrorOverrideAllowedForOrigins
  - Имя групповой политики: разрешить пользователям продолжать работу со страницы предупреждения HTTPS для определенных источников
  - Путь к групповой политике (обязательно): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Политики\Microsoft\Edge\SSLErrorOverrideAllowedForOrigins
  - Путь (рекомендуется): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\SSLErrorOverrideAllowedForOrigins\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\SSLErrorOverrideAllowedForOrigins\2 = "[*.]example.edu"

```

  #### Информация о Mac и параметры
  
  - Имя ключа предпочтения: SSLErrorOverrideAllowedForOrigins
  - Пример значения:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### SSLVersionMin

  #### Минимальная версия TLS включена

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Устанавливает минимальную поддерживаемую версию TLS. Если не настроить эту политику, в Microsoft Edge будет отображаться сообщение об ошибке TLS 1.0 и TLS 1.1, но пользователь сможет пропустить его.

Если установлено, Microsoft Edge не будет использовать любую версию SSL/TLS ниже указанной версии. Любое нераспознанное значение игнорируется.

Сопоставление параметров политики:

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SSLVersionMin
  - Имя GP: Включена минимальная версия TLS
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: SSLVersionMin
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"tls1"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: SSLVersionMin
  - Пример значения:
``` xml
<string>tls1</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### SaveCookiesOnExit

  #### Сохранять файлы cookie при закрытии Microsoft Edge

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  Если эта политика включена, указанный набор файлов cookie исключается из удаления при закрытии браузера. Эта политика действует только в следующих случаях:
- Настроен переключатель "Файлы cookie и другие данные сайтов" в разделе "Настройки/Конфиденциальность и службы/Удалять данные браузера при выходе" или
- Включена политика [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) или
- Политике [DefaultCookiesSetting](#defaultcookiessetting) присвоено значение "Сохранять файлы cookie в течение сеанса".

Вы можете определить список сайтов на основе шаблонов URL-адресов, которые будут сохранять свои файлы cookie в сеансах.

Примечание. Пользователи по-прежнему могут изменять список сайтов с файлами cookie, чтобы добавлять или удалять URL-адреса. Но они не могут удалять URL-адреса, добавленные администратором.

Если включить эту политику, список файлов cookie не будет очищаться при закрытии браузера.

Если эта политика отключена или не настроена, применяется личная настройка пользователя.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: SaveCookiesOnExit
  - Имя групповой политики: Сохранять файлы cookie при закрытии Microsoft Edge
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): Программное обеспечение\Политики\Microsoft\Edge\SaveCookiesOnExit
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: SaveCookiesOnExit
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### SavingBrowserHistoryDisabled

  #### Отключить сохранение истории браузера

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Отключить сохранение истории браузера и запретить пользователям изменять этот параметр.

Если вы включите эту политику, история просмотра не будет сохранена. Это также отключает синхронизацию вкладок.

Если вы отключите эту политику или не настроите ее, история посещений будет сохранена.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SavingBrowserHistoryDisabled
  - Имя GP: Отключить сохранение истории браузера
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: SavingBrowserHistoryDisabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: SavingBrowserHistoryDisabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ScreenCaptureAllowed

  #### Разрешить или запретить захват экрана

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 83 и более поздних версий

  #### Описание

  Если вы включите эту политику или не настроите ее, веб-страница может использовать API общего доступа к экрану (например, getDisplayMedia() или API расширения Desktop Capture) для захвата экрана.
Если вы отключите эту политику, вызовы к API общего доступа к экрану не будут выполнены. Например, если вы используете веб-конференцию в Интернете, общий доступ к видео или экрану не будет работать.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ScreenCaptureAllowed
  - Имя GP: Разрешить или запретить захват экрана
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ScreenCaptureAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ScreenCaptureAllowed
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ScrollToTextFragmentEnabled

  #### Включить прокрутку до текста, указанного в фрагментах URL

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 83 и более поздних версий

  #### Описание

  Эта функция позволяет гиперссылкам и URL-адресам в адресной строке ориентироваться на определенный текст на веб-странице, который будет прокручиваться после завершения загрузки веб-страницы.

Если вы включите или не настроите эту политику, будет включена прокрутка веб-страницы до определенных фрагментов текста через URL.

Если вы отключите эту политику, прокрутка веб-страницы до определенных фрагментов текста через URL будет отключена.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ScrollToTextFragmentEnabled
  - Имя GP: Включить прокрутку к тексту, указанному во фрагментах URL
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ScrollToTextFragmentEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ScrollToTextFragmentEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SearchSuggestEnabled

  #### Включить варианты поиска

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Включает предложения веб-поиска в адресной строке Microsoft Edge и в списке автоматических советов и запрещает пользователям изменять эту политику.

Если вы включите эту политику, будут использоваться предложения веб-поиска.

Если вы отключите эту политику, предложения веб-поиска никогда не будут использоваться, однако по-прежнему будут отображаться предложения по локальной истории и локальным избранным. Если вы отключите эту политику, ни введенные символы, ни посещенные URL-адреса не будут включены в телеметрию для Microsoft.

Если это правило не задано, поисковые подсказки включены, но пользователь может это изменить.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SearchSuggestEnabled
  - Имя GP: Включение вариантов поиска
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: SearchSuggestEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: SearchSuggestEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SecurityKeyPermitAttestation

  #### Веб-сайты или домены, которым не требуется разрешение на прямую аттестацию ключа безопасности

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Указывает веб-сайты и домены, которым не требуется явное разрешение пользователя при запросе сертификатов аттестации из ключей безопасности. Кроме того, на ключ безопасности отправляется сигнал, указывающий, что он может использовать индивидуальную аттестацию. Без этого пользователям предлагается каждый раз, когда сайт запрашивает аттестацию ключей безопасности.

Сайты (например, https://contoso.com/some/path) совпадают с U2F appID. Домены (например, contoso.com) совпадают только как идентификаторы RP веб-сайтов. Чтобы охватить как API-интерфейсы U2F, так и API-интерфейсы webauthn для данного сайта, необходимо указать URL-адрес appID и домен.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SecurityKeyPermitAttestation
  - Имя GP: Веб-сайты или домены, которым не требуется разрешение на прямую аттестацию ключа безопасности
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательно): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\SecurityKeyPermitAttestation
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = "https://contoso.com"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: SecurityKeyPermitAttestation
  - Пример значения:
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### SendIntranetToInternetExplorer

  #### Отправлять все сайты интрасети в Internet Explorer

  
  
  #### Поддерживаемые версии:

  - В Windows с 77 и более поздних версий

  #### Описание

  Инструкции по настройке оптимального режима для режима Internet Explorer см. [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SendIntranetToInternetExplorer
  - Имя GP: Отправить все сайты интрасети в Internet Explorer
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: SendIntranetToInternetExplorer
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### SendSiteInfoToImproveServices

  #### Отправка сведений о сайте для улучшения служб Майкрософт (устаревший)

  
  >УСТАРЕЛО: эта политика устарела и не работает в версиях Microsoft Edge после 88.
  #### Поддерживаемые версии:

  - В Windows и macOS — версии c 77 по 88

  #### Описание

  Эта политика больше не поддерживается. Она заменяется на [DiagnosticData](#diagnosticdata) (для Windows 7, Windows 8 и macOS) и Allow Telemetry on Win 10 ( [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569) ).

Эта политика позволяет отправлять информацию о веб-сайтах, посещенных в Microsoft Edge, в Microsoft для улучшения таких услуг, как поиск.

Включите эту политику для отправки информации о веб-сайтах, посещенных в Microsoft Edge, в Microsoft. Отключите эту политику, чтобы не отправлять информацию о веб-сайтах, посещенных в Microsoft Edge, в Microsoft. В обоих случаях пользователи не смогут изменить или переопределить его.

В Windows 10, если вы не настроите эту политику, Microsoft Edge по умолчанию будет использовать параметр диагностических данных Windows. Если эта политика включена, Microsoft Edge будет отправлять информацию о веб-сайтах, посещенных в Microsoft Edge, только если для параметра данных диагностики Windows установлено значение «Полный». Если эта политика отключена, Microsoft Edge не будет отправлять данные о посещенных веб-сайтах. Подробнее о настройках данных диагностики Windows: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

В Windows 7, Windows 8 и Mac эта политика управляет отправкой информации о посещенных веб-сайтах. Если вы не настроите эту политику, Microsoft Edge по умолчанию будет использовать настройки пользователя.

Чтобы включить эту политику, параметру [MetricsReportingEnabled](#metricsreportingenabled) требуется присвоить значение "Включено". Если параметру [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) или [MetricsReportingEnabled](#metricsreportingenabled) присвоено значение "Не настроено" или "Отключено", эти данные не отправляются в корпорацию Майкрософт.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SendSiteInfoToImproveServices
  - Имя GP: Отправка сведений о сайте для улучшения служб Майкрософт (устаревший)
  - Путь к GP (обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: SendSiteInfoToImproveServices
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: SendSiteInfoToImproveServices
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SensorsAllowedForUrls

  #### Разрешить доступ к датчиками на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  На основании шаблонов URL-адресов определите список сайтов, которые могут получать доступ к датчикам и использовать их, например датчики движения и света.

Если не настроить эту политику, для всех сайтов будет использоваться стандартное глобальное значение из политики [DefaultSensorsSetting](#defaultsensorssetting) (если настроена) или личная конфигурация пользователя.

Для шаблонов URL-адресов, не соответствующих этой политике, используется следующий порядок приоритета: политика [SensorsBlockedForUrls](#sensorsblockedforurls) (если существует совпадение), политика [DefaultSensorsSetting](#defaultsensorssetting) (если настроена) или личные параметры пользователя.

Шаблоны URL-адресов, определенные в этой политике, не могут конфликтовать с настроенными в политике [SensorsBlockedForUrls](#sensorsblockedforurls). Вы не можете разрешить и заблокировать URL-адрес.

Подробные сведения о шаблонах допустимых URL-адресов см. на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: SensorsAllowedForUrls
  - Имя групповой политики: Разрешить доступ к датчиками на определенных сайтах
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Политики\Microsoft\Edge\SensorsAllowedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: SensorsAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### SensorsBlockedForUrls

  #### Блокировать доступ к датчиками на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  На основании шаблонов URL-адресов определите список сайтов, которые не могут получать доступ к датчикам, например к датчикам движения и света.

Если не настроить эту политику, для всех сайтов будет использоваться стандартное глобальное значение из политики [DefaultSensorsSetting](#defaultsensorssetting) (если настроена) или личная конфигурация пользователя.

Для шаблонов URL-адресов, не соответствующих этой политике, используется следующий порядок приоритета: политика [SensorsAllowedForUrls](#sensorsallowedforurls) (если существует совпадение), политика [DefaultSensorsSetting](#defaultsensorssetting) (если настроена) или личные параметры пользователя.

Шаблоны URL-адресов, определенные в этой политике, не могут конфликтовать с настроенными в политике [SensorsAllowedForUrls](#sensorsallowedforurls). Вы не можете разрешить и заблокировать URL-адрес.

Подробные сведения о шаблонах допустимых URL-адресов см. на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: SensorsBlockedForUrls
  - Имя групповой политики: Блокировать доступ к датчиками на определенных сайтах
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Политики\Microsoft\Edge\SensorsBlockedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: SensorsBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### SerialAskForUrls

  #### Разрешить API Serial на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  На основании шаблонов URL-адресов определите список сайтов, которые могут запрашивать у пользователя доступ к последовательному порту.

Если не настроить эту политику, для всех сайтов будет использоваться стандартное глобальное значение из политики [DefaultSerialGuardSetting](#defaultserialguardsetting) (если настроена) или личная конфигурация пользователя.  

Для шаблонов URL-адресов, не соответствующих этой политике, используется следующий порядок приоритета: политика [SerialBlockedForUrls](#serialblockedforurls) (если существует совпадение), политика [DefaultSerialGuardSetting](#defaultserialguardsetting) (если настроена) или личные параметры пользователя.

Шаблоны URL-адресов, определенные в этой политике, не могут конфликтовать с настроенными в политике [SerialBlockedForUrls](#serialblockedforurls). Вы не можете разрешить и заблокировать URL-адрес.

Подробные сведения о шаблонах допустимых URL-адресов см. на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: SerialAskForUrls
  - Имя групповой политики: Разрешить API Serial на определенных сайтах
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Политики\Microsoft\Edge\SerialAskForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: SerialAskForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### SerialBlockedForUrls

  #### Блокировать API Serial на определенных сайтах

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  На основании шаблонов URL-адресов определите список сайтов, которые не могут запрашивать у пользователя предоставление доступа к последовательному порту.

Если не настроить эту политику, для всех сайтов будет использоваться стандартное глобальное значение из политики [DefaultSerialGuardSetting](#defaultserialguardsetting) (если настроена) или личная конфигурация пользователя.  

Для шаблонов URL-адресов, не соответствующих этой политике, используется следующий порядок приоритета: политика [SerialAskForUrls](#serialaskforurls) (если существует совпадение), политика [DefaultSerialGuardSetting](#defaultserialguardsetting) (если настроена) или личные параметры пользователя.

Шаблоны URL-адресов в этой политике не могут конфликтовать с настроенными в политике [SerialAskForUrls](#serialaskforurls). Вы не можете разрешить и заблокировать URL-адрес.

Подробные сведения о шаблонах допустимых URL-адресов см. на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: SerialBlockedForUrls
  - Имя групповой политики: Блокировать API Serial на определенных сайтах
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Политики\Microsoft\Edge\SerialBlockedForUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: SerialBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### ShowMicrosoftRewards

  #### Показать возможности Microsoft Rewards

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 88 или позже

  #### Описание

  Отображение возможностей и уведомлений Microsoft Rewards.
Если эта политика включена:
   - Пользователи учетной записи Майкрософт (исключая учетные записи Azure AD) в службах поиска и получения будут видеть возможности Microsoft Rewards в пользовательском профиле Microsoft Edge.
   - Параметр для включения и выключения Microsoft Rewards в параметрах Microsoft Edge будет включен.

Если этот параметр отключен:
   - Пользователи учетной записи Майкрософт (исключая учетные записи Azure AD) в службах поиска и получения не будут видеть возможности Microsoft Rewards в пользовательском профиле Microsoft Edge.
   - Параметр для включения и выключения Microsoft Rewards в параметрах Microsoft Edge будет отключен.

Если политика не будет настроена:
   - Пользователи учетной записи Майкрософт (исключая учетные записи Azure AD) в службах поиска и получения будут видеть возможности Microsoft Rewards в пользовательском профиле Microsoft Edge.
   - Параметр для включения и выключения Microsoft Rewards в параметрах Microsoft Edge будет включен.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ShowMicrosoftRewards
  - Имя GP: Показать возможности Microsoft Rewards
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): SOFTWARE\Policies\Microsoft\Edge\Recommended
  - Имя значения: ShowMicrosoftRewards
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ShowMicrosoftRewards
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ShowOfficeShortcutInFavoritesBar

  #### Показать ярлык Microsoft Office на панели избранного (не рекомендуется)

  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Эта политика работала неправильно из-за изменений операционных требований. Поэтому она устарела, и ее не следует использовать.

Указывает, следует ли включать ярлык Office.com в панели избранного. Пользователей, вошедших в Microsoft Edge, ярлык направит в приложения и документы Microsoft Office. Если эта политика включена или не настроена, пользователи могут выбрать, следует ли отображать ярлык, переключив кнопку в контекстном меню панели избранного.
Если отключить эту политику, ярлык не будет отображаться.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ShowOfficeShortcutInFavoritesBar
  - Имя GP: Показать ярлык Microsoft Office на панели избранного (не рекомендуется)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: ShowOfficeShortcutInFavoritesBar
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: ShowOfficeShortcutInFavoritesBar
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ShowRecommendationsEnabled

  #### Разрешить рекомендации и рекламные уведомления от Microsoft Edge

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с версии 89 или более поздней

  #### Описание

  С помощью этого параметра политики вы можете решить, следует ли сотрудникам получать рекомендации и уведомления о помощи в продуктах от Microsoft Edge.

Если этот параметр включен или не настроен, сотрудники будут получать рекомендации или уведомления от Microsoft Edge.

Если этот параметр отключен, сотрудники не будут получать никаких рекомендаций или уведомлений от Microsoft Edge.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ShowRecommendationsEnabled
  - Имя GP: Разрешить рекомендации и рекламные уведомления из Microsoft Edge
  - Путь к GP (обязательный): Administrative Templates/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): Н/Д
  - Имя значения: ShowRecommendationsEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Сведения о Mac и параметры
  
  - Имя ключа предпочтения: ShowRecommendationsEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SignedHTTPExchangeEnabled

  #### Включить поддержку подписанного HTTP Exchange (SXG)

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 78 и более поздних версий

  #### Описание

  Включите поддержку подписанного обмена HTTP (SXG).

Если эта политика не установлена или не включена, Microsoft Edge будет принимать веб-содержимое, которое используется как подписанный обмен HTTP.

Если эта политика отключена, подписанные обмены HTTP не могут быть загружены.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SignedHTTPExchangeEnabled
  - Имя GP: Включить поддержку Signed HTTP Exchange (SXG)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: SignedHTTPExchangeEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: SignedHTTPExchangeEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SitePerProcess

  #### Включить изоляцию сайта для каждого сайта

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Политика «SitePerProcess» может использоваться, чтобы запретить пользователям отказаться от поведения по умолчанию изоляции всех сайтов. Обратите внимание, что вы также можете использовать политику [IsolateOrigins](#isolateorigins) для изоляции дополнительных, более мелких источников.

Если вы включите эту политику, пользователи не смогут отказаться от поведения по умолчанию, при котором каждый сайт работает в своем собственном процессе.

Если эта политика отключена или не настроена, пользователь может отказаться от изоляции сайта.  (Например, с помощью записи «Отключить изоляцию сайта» в edge://flags.) Отключение политики или ее отсутствие не отключает изоляцию сайта.


  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SitePerProcess
  - Имя GP: Включить изоляцию сайта для каждого сайта
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: SitePerProcess
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: SitePerProcess
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SmartActionsBlockList

  #### Блокировка интеллектуальных действий для списка служб

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS с версии 89 или более поздней

  #### Описание

  Перечисление определенных служб, например PDF, не отображающих интеллектуальные действия. (К интеллектуальным действиям относятся такие действия, как "определить", доступные в полных и уменьшенных контекстных меню Microsoft Edge.)

Если вы включите политику:
   - Интеллектуальное действие в уменьшенном и полном контекстном меню будет отключено во всех профилях для служб, соответствующих указанному списку.
   - При выборе текста для служб, соответствующих указанному списку, пользователи не увидят интеллектуальное действие в уменьшенном и полном контекстном меню.
   - В параметрах Microsoft Edge интеллектуальное действие в уменьшенном и полном контекстном меню будет отключено для служб, соответствующих указанному списку.

Если отключить или не настроить эту политику:
   - Интеллектуальное действие в уменьшенном и полном контекстном меню будет включено для всех профилей.
   - При выборе текста пользователи увидят интеллектуальное действие в уменьшенном и полном контекстном меню.
   - В параметрах Microsoft Edge интеллектуальное действие в уменьшенном и полном контекстном меню будет включено.

Сопоставление параметров политики:

* smart_actions_pdf (smart_actions_pdf) = интеллектуальные действия в PDF

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SmartActionsBlockList
  - Название GP: блокировка интеллектуальных действий для списка служб
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge\SmartActionsBlockList
  - Путь (рекомендуется): SOFTWARE\Policies\Microsoft\Edge\Recommended\SmartActionsBlockList
  - Имя значения: 1, 2, 3,...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\SmartActionsBlockList\1 = "smart_actions_pdf"

```

  #### Сведения о Mac и параметры
  
  - Имя ключа предпочтения: SmartActionsBlockList
  - Пример значения:
``` xml
<array>
  <string>smart_actions_pdf</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### SpeechRecognitionEnabled

  #### Configure Speech Recognition

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 87 или позже

  #### Описание

  Укажите, смогут ли веб-сайты использовать веб-интерфейс API речи консорциума W3C для распознавания речи от пользователя. В Microsoft Edge API веб-интерфейса голосовых функций используется служба самообслуживания Azure, поэтому голосовые данные будут выходить из компьютера.

Если вы включите или не настроите эту политику, то в веб-приложениях, использующих веб-интерфейс речи, можно использовать функцию распознавания речи.

Если этот параметр отключен, распознавание речи не будет доступно через API-интерфейс голосового веб-интерфейса.

Подробнее об этой функции читайте здесь: SpeechRecognition API: [https://go.microsoft.com/fwlink/?linkid=2143388](https://go.microsoft.com/fwlink/?linkid=2143388) Cognitive Services: [https://go.microsoft.com/fwlink/?linkid=2143680](https://go.microsoft.com/fwlink/?linkid=2143680)

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - GP unique name: SpeechRecognitionEnabled
  - GP name: Configure Speech Recognition
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Value Name: SpeechRecognitionEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Preference Key Name: SpeechRecognitionEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SpellcheckEnabled

  #### Включить проверку орфографии

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Если вы включите или не настроите эту политику, пользователь может использовать проверку орфографии.

Если вы отключите эту политику, пользователь не сможет использовать проверку правописания, а политики [SpellcheckLanguage](#spellchecklanguage) и [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) также будут отключены.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SpellcheckEnabled
  - Название GP: Включить проверку орфографии
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: SpellcheckEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: SpellcheckEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SpellcheckLanguage

  #### Включить определенные языки проверки орфографии

  
  
  #### Поддерживаемые версии:

  - В Windows с 77 и более поздних версий

  #### Описание

  Включает разные языки для проверки орфографии. Любой указанный вами язык, который не распознается, игнорируется.

Если вы включите эту политику, проверка орфографии будет включена для указанных языков, а также для всех языков, включенных пользователем.

Если вы не настроите или не отключите эту политику, настройки проверки правописания пользователя не изменятся.

Если политика [SpellcheckEnabled](#spellcheckenabled) отключена, эта политика не будет действовать.

Если язык включен в политику «SpellcheckLanguage» и [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist), язык проверки орфографии включен.

Поддерживаются следующие языки: af, bg, ca, cs, cy, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SpellcheckLanguage
  - Имя GP: Включить определенные языки проверки орфографии
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\SpellcheckLanguage
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = "es"

```

  

  [В начало](#microsoft-edge---policies)

  ### SpellcheckLanguageBlocklist

  #### Принудительное отключение языков проверки орфографии

  
  
  #### Поддерживаемые версии:

  - В Windows с 78 и более поздних версий

  #### Описание

  Принудительно отключить проверку правописания языков. Нераспознанные языки в этом списке будут игнорироваться.

Если вы включите эту политику, проверка орфографии будет отключена для указанных языков. Пользователь по-прежнему может включать или отключать проверку орфографии для языков, которых нет в списке.

Если вы не установите эту политику или не отключите ее, настройки проверки правописания пользователя не изменятся.

Если политика [SpellcheckEnabled](#spellcheckenabled) отключена, эта политика не будет действовать.

Если язык включен в политику [SpellcheckLanguage](#spellchecklanguage) и SpellcheckLanguageBlocklist, язык проверки орфографии включен.

В настоящее время поддерживаются следующие языки: af, bg, ca, cs, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SpellcheckLanguageBlocklist
  - Имя GP: Принудительное отключение языков проверки орфографии
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательно): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = "es"

```

  

  [В начало](#microsoft-edge---policies)

  ### StricterMixedContentTreatmentEnabled

  #### Включить более строгую обработку смешанного контента (устарело)

  
  >УСТАРЕЛО: эта политика устарела и не работает в Microsoft Edge версии 84 и более поздних.
  #### Поддерживаемые версии:

  - В Windows и macOS — версии c 81 по 84

  #### Описание

  Эта политика не работает, так как она была предусмотрена только в качестве краткосрочного механизма, чтобы дать организациям больше времени на обновление веб-содержимого, если оно оказалось несовместимым с более строгой обработкой смешанного содержимого.

Эта политика контролирует обработку смешанного содержимого (содержимого HTTP на сайтах HTTPS) в браузере.

Если для этой политики задано значение "истина" или она не настроена, то смешанный аудио- и видеоконтент будет автоматически обновлен до HTTPS (то есть URL-адрес будет перезаписан как HTTPS без учета того, что ресурс может быть недоступен через HTTPS), а для контента с изображениями смешанного типа в адресной строке появится предупреждение "Небезопасно".

Если для политики задано значение false, автоматическое обновление будет отключено для аудио и видео, и для изображений не будет отображаться предупреждение.

Эта политика не влияет на другие типы смешанного контента, кроме аудио, видео и изображений.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: StricterMixedContentTreatmentEnabled
  - Название GP: включение более строгой обработки смешанного содержимого (устарело)
  - Путь к GP (обязательно): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: StricterMixedContentTreatmentEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: StricterMixedContentTreatmentEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SuppressUnsupportedOSWarning

  #### Подавить предупреждение о неподдерживаемой ОС

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Подавляет предупреждение, которое появляется, когда Microsoft Edge работает на компьютере или в операционной системе, которая больше не поддерживается.

Если эта политика ложна или не установлена, предупреждения будут появляться на таких неподдерживаемых компьютерах или операционных системах.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SuppressUnsupportedOSWarning
  - Имя GP: Подавить предупреждение о неподдерживаемой ОС
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: SuppressUnsupportedOSWarning
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: SuppressUnsupportedOSWarning
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SyncDisabled

  #### Отключить синхронизацию данных с помощью служб Microsoft Sync Services

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Отключает синхронизацию данных в Microsoft Edge. Эта политика также предотвращает появление запроса на согласие синхронизации.

Эта политика отключает только облачную синхронизацию и не влияет на политику [RoamingProfileSupportEnabled](#roamingprofilesupportenabled).

Если эта политика не настроена или не применена в соответствии с рекомендациями, пользователи смогут включить или отключить синхронизацию. Если вы примените эту политику как обязательную, пользователи не смогут включить синхронизацию.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SyncDisabled
  - Имя GP: Отключить синхронизацию данных с помощью служб синхронизации Microsoft
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: SyncDisabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: SyncDisabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### SyncTypesListDisabled

  #### Настройте список типов, которые исключены из синхронизации

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 83 и более поздних версий

  #### Описание

  Если вы включите эту политику, все указанные типы данных будут исключены из синхронизации. Эту политику можно использовать для ограничения типа данных, загружаемых в службу синхронизации Microsoft Edge.

Для этой политики может использоваться один из следующих типов данных: "favorites", "settings", "passwords", "addressesAndMore", "extensions", "history", "openTabs" и "collections". Обратите внимание, что эти имена типов данных чувствительны к регистру.

Пользователи не смогут переопределять отключенные типы данных.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: SyncTypesListDisabled
  - Имя GP: Настроить список типов, которые исключены из синхронизации
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\SyncTypesListDisabled
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = "favorites"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: SyncTypesListDisabled
  - Пример значения:
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### TLS13HardeningForLocalAnchorsEnabled

  #### Включение функции безопасности TLS 1.3 для локальных якорей доверия (устарело)

  
  >УСТАРЕЛО: эта политика устарела и не работает в Microsoft Edge версии 85 и более поздних.
  #### Поддерживаемые версии:

  - В Windows и macOS — версии c 81 по 85

  #### Описание

  Эта политика не работает, так как она была предусмотрена только в качестве краткосрочного механизма, чтобы дать предприятиям больше времени для обновления затронутых прокси-серверов.

Эта политика управляет функцией безопасности в TLS 1.3, которая защищает соединения от атак понижения. Он обратно совместим и не влияет на соединения с совместимыми серверами TLS 1.2 или прокси серверами. Однако более старые версии некоторых TLS-перехватывающих прокси имеют недостаток реализации, что делает их несовместимыми.

Если вы включите эту политику или не установите ее, Microsoft Edge включит эти средства защиты для всех соединений.

Если вы отключите эту политику, Microsoft Edge отключит эти средства защиты для соединений, аутентифицированных с помощью локально установленных сертификатов CA. Эти средства защиты всегда включены для соединений, аутентифицированных с помощью общедоступных сертификатов CA.

Эту политику можно использовать для тестирования всех затронутых прокси-серверов и их обновления. Ожидается, что затронутые прокси-серверы потерпят неудачу в соединениях с кодом ошибки ERR_TLS13_DOWNGRADE_DETECTED.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: TLS13HardeningForLocalAnchorsEnabled
  - Имя групповой политики: Включение функции безопасности TLS 1.3 для локальных якорей доверия (устарело)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: TLS13HardeningForLocalAnchorsEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: TLS13HardeningForLocalAnchorsEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### TLSCipherSuiteDenyList

  #### Выбор наборов шифров TLS для отключения

  
  
  #### Поддерживаемые версии:

  - В Windows и macOS — версия 85 или более поздние

  #### Описание

  Настройка списка наборов шифров, отключенных для соединений TLS

Если вы настроили эту политику, то при установлении подключения TLS наборы шифров из настроенного списка использоваться не будут.

Если эта политика не настроена, то будут использоваться выбранные браузером наборы шифров TLS.

Значения наборов шифров для отключения задаются в 16-битовом шестнадцатеричном формате. Значения назначаются реестром Internet Assigned Numbers Authority (IANA).

Набор шифров TLS 1.3 TLS_AES_128_GCM_SHA256 (0x1301) является обязательным для TLS 1.3 и не может быть отключен с помощью этой политики.

Эта политика не влияет на подключения по протоколу QUIC. Протокол QUIC можно отключить с помощью политики [QuicAllowed](#quicallowed).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: TLSCipherSuiteDenyList
  - Имя GP: Выбор наборов шифров TLS для отключения
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = "0x1303"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = "0xcca8"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = "0xcca9"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: TLSCipherSuiteDenyList
  - Пример значения:
``` xml
<array>
  <string>0x1303</string>
  <string>0xcca8</string>
  <string>0xcca9</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### TabFreezingEnabled

  #### Разрешить замораживание фоновых вкладок

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 79 или позже

  #### Описание

  Определяет, может ли Microsoft Edge заморозить вкладки, которые находятся в фоновом режиме, как минимум на 5 минут.

Замораживание вкладок уменьшает использование процессора, батареи и памяти. Microsoft Edge использует эвристику, чтобы избежать зависания вкладок, которые выполняют полезную работу в фоновом режиме, например, отображают уведомления, воспроизводят звук и транслируют видео.

Если вы включите или не настроите эту политику, вкладки, которые были в фоновом режиме не менее 5 минут, могут быть заморожены.

Если вы отключите эту политику, никакие вкладки не будут заморожены.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: TabFreezingEnabled
  - Имя GP: Разрешить замораживание вкладок фона
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: TabFreezingEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: TabFreezingEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### TargetBlankImpliesNoOpener

  #### Не устанавливать window.opener для ссылок, нацеленных на _blank

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 88 или позже

  #### Описание

  Если включить эту политику или оставить ее неопределенной, window.opener будет задано значение null, если только в привязке не указано rel="opener".

Если вы отключили эту политику, всплывающие окна, для которых разрешено _blank, будут иметь доступ (через JavaScript) к странице, которая запросила открытие всплывающего окна.

Эта политика будет устаревшей в Microsoft Edge версии 95.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: TargetBlankImpliesNoOpener
  - Имя GP: Не устанавливать window.opener для ссылок, нацеленных на _blank
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: TargetBlankImpliesNoOpener
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: TargetBlankImpliesNoOpener
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### TaskManagerEndProcessEnabled

  #### Включить завершающие процессы в диспетчере задач браузера

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Если вы включите или не настроите эту политику, пользователи могут завершать процессы в диспетчере задач браузера. Если вы отключите его, пользователи не смогут завершить процессы, а кнопка «Завершить процесс» будет отключена в диспетчере задач браузера.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: TaskManagerEndProcessEnabled
  - Имя GP: Включить конечные процессы в диспетчере задач браузера.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: TaskManagerEndProcessEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: TaskManagerEndProcessEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### TotalMemoryLimitMb

  #### Установка ограничения на размер памяти (в мегабайтах), который может использовать один экземпляр Microsoft Edge.

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 80 или позже

  #### Описание

  Настраивает объем памяти, который может использовать один экземпляр Microsoft Edge, прежде чем вкладки начнут сбрасываться для экономии памяти. Память, используемая вкладкой, будет освобождена, и вкладка должна быть перезагружена при переключении на.

Если вы включите эту политику, браузер начнет сбрасывать вкладки для экономии памяти после превышения ограничения. Тем не менее, нет никаких гарантий, что браузер всегда работает под лимитом. Любое значение меньше 1024 будет округлено до 1024.

Если вы не установите эту политику, браузер будет пытаться сохранить память только тогда, когда обнаружит, что объем физической памяти на его компьютере невелик.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: TotalMemoryLimitMb
  - Имя GP: Установка ограничения на размер памяти (в мегабайтах), который может использовать один экземпляр Microsoft Edge.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: TotalMemoryLimitMb
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000800
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: TotalMemoryLimitMb
  - Пример значения:
``` xml
<integer>2048</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### TrackingPrevention

  #### Блокировка отслеживания активности пользователей в Интернете

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 78 и более поздних версий

  #### Описание

  Позволяет решить, следует ли блокировать веб-сайты от отслеживания активности пользователей в Интернете.

Если вы отключите эту политику или не настроите ее, пользователи могут установить собственный уровень предотвращения отслеживания.

Сопоставление параметров политики:

* TrackingPreventionOff (0) = Выкл. (без блокировки отслеживания)

* TrackingPreventionBasic (1) = Базовый (блокирует вредоносные отслеживания, контент и реклама будут персонализированы)

* TrackingPreventionBalanced (2) = Сбалансированный (блокирует вредоносные отслеживания и отслеживания с сайтов, которые пользователь не посещал; контент и реклама будут менее персонализированы)

* TrackingPreventionStrict (3) = Строгий (блокирует вредоносные отслеживания и большинство трекеров со всех сайтов; контент и реклама будут иметь минимальную персонализацию. Некоторые части сайтов могут не работать)

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: TrackingPrevention
  - Имя GP: Блокировка отслеживания активности пользователей в Интернете
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: TrackingPrevention
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000002
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: TrackingPrevention
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### TranslateEnabled

  #### Включить перевод

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Включает встроенную службу перевода Microsoft в Microsoft Edge.

Если вы включите эту политику, Microsoft Edge предложит пользователю функциональность перевода, показывая при необходимости встроенную всплывающую подсказку перевода и опцию перевода в контекстном меню, вызываемом правой кнопкой мыши.

Отключите эту политику, чтобы отключить все встроенные функции перевода.

Если вы не настроите политику, пользователи могут выбирать, использовать функцию перевода или нет.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - GP уникальное имя: TranslateEnabled
  - Имя GP: Включение перевода
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь к GP (рекомендуется): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределить)/
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\Recommended
  - Имя значения: TranslateEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: TranslateEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### URLAllowlist

  #### Определите список разрешенных URL

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Настройка политики предоставляет доступ к указанным URL-адресам, как исключения к [URLBlocklist](#urlblocklist).

Отформатируйте шаблон URL в соответствии с [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Вы можете использовать эту политику, чтобы открывать исключения в ограничительных списках блокировки. Например, можно включить "\*" в список блокировки, чтобы заблокировать все запросы, а затем использовать эту политику, чтобы разрешить доступ к ограниченному списку URL-адресов. Вы можете использовать эту политику, чтобы открывать исключения для определенных схем, поддоменов других доменов, портов или определенных путей.

Самый специфический фильтр определяет, заблокирован или разрешен URL. Разрешенный список имеет приоритет над черным списком.

Эта политика ограничена 1000 записей; последующие записи игнорируются.

Эта политика также позволяет браузеру автоматически вызывать внешние приложения, зарегистрированные как обработчики таких протоколов, как "tel:" или "ssh:".

Если вы не сконфигурируете эту политику, не будет никаких исключений из списка заблокированных в политике [URLBlocklist](#urlblocklist).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: URLAllowlist
  - Имя GP: Определение списка разрешенных URL
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\URLAllowlist
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = ".exact.hostname.com"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: URLAllowlist
  - Пример значения:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### URLBlocklist

  #### Блокировать доступ к списку URL-адресов

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Определите список сайтов, основанных на шаблонах URL, которые заблокированы (ваши пользователи не могут их загрузить).

Отформатируйте шаблон URL в соответствии с [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Вы можете определить исключения в политике [URLAllowlist](#urlallowlist). Эти политики ограничены 1000 записей; последующие записи игнорируются.

Обратите внимание, что блокировка внутренних URL-адресов 'edge://*' не рекомендуется - это может привести к непредвиденным ошибкам.

Эта политика не запрещает динамическое обновление страницы через JavaScript. Например, если вы заблокируете «contoso.com/abc», пользователи все равно смогут посетить «contoso.com» и щелкнуть ссылку, чтобы перейти на «contoso.com/abc», если страница не обновляется.

Если вы не настроите эту политику, никакие URL не будут заблокированы.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: URLBlocklist
  - Имя GP: Заблокировать доступ к списку URL
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\URLBlocklist
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\3 = "hosting.com/bad_path"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\5 = ".exact.hostname.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\6 = "file://*"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\7 = "custom_scheme:*"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\8 = "*"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: URLBlocklist
  - Пример значения:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/bad_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
  <string>file://*</string>
  <string>custom_scheme:*</string>
  <string>*</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### UpdatePolicyOverride

  #### Указывает, как Центр обновления Microsoft Edge обрабатывает доступные обновления из Microsoft Edge

  
  
  #### Поддерживаемые версии:

  - macOS версии 89 или более поздней

  #### Описание

  Если эта политика включена, Центр обновления Microsoft Edge обрабатывает обновления Microsoft Edge в соответствии со значениями следующих параметров.

- Только обновления, найденные автоматически: обновления применяются только в том случае, если они были найдены при периодической автоматической проверке наличия обновлений.

- Только обновления, найденные вручную: обновления применяются только в том случае, если пользователь запускает проверку наличия обновлений вручную. (Не все приложения предоставляют интерфейс для этого варианта.)

При выборе параметра "Обновления, найденные вручную" периодически проверяйте наличие обновлений с помощью функции автоматического обновления (Майкрософт).

Если вы не включите и не настроите эту политику, Центр обновления Microsoft Edge будет автоматически проверять наличие обновлений.


Сопоставление параметров политики:

* automatic-silent-only (automatic-silent-only) = обновления применяются только в том случае, если они были найдены при периодической автоматической проверке наличия обновлений.

* manual-only (manual-only) = обновления применяются только в том случае, если пользователь запускает проверку наличия обновлений вручную. (Не все приложения предоставляют интерфейс для этого варианта.)

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Да
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Строка

  

  #### Сведения о Mac и параметры
  
  - Имя ключа настройки: UpdatePolicyOverride
  - Пример значения:
``` xml
<string>automatic-silent-only</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### UserAgentClientHintsEnabled

  #### Включение функции клиентских подсказок User-Agent (устарело)

  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:

  - На Windows и macOS — версия 86 или более поздние

  #### Описание

  Поддержка этой политики прекращена, так как она предусматривалась только в качестве краткосрочного механизма, чтобы дать предприятиям больше времени для обновления своего веб-содержимого, несовместимого с функцией клиентских подсказок User-Agent. Она не будет работать в Microsoft Edge версии 89.

При включении функции клиентских подсказок User-Agent она отправляет подробные заголовки запросов, которые содержат сведения о пользовательском браузере (например, версия браузера) и среде (например, архитектура системы).

Это аддитивная функция, но новые заголовки могут быть несовместимы с некоторыми веб-сайтами, которые ограничивают количество символов в запросах.

Если вы включите или не настроите эту политику, функции клиентских подсказок User-Agent будет включена. Если вы выключите эту политику, данная функция будет недоступна.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: UserAgentClientHintsEnabled
  - Имя групповой политики: Включение функции клиентских подсказок User-Agent (устарело)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: UserAgentClientHintsEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: UserAgentClientHintsEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### UserDataDir

  #### Установить каталог пользовательских данных

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Установите каталог для хранения пользовательских данных.

Если вы включите эту политику, Microsoft Edge использует указанный каталог независимо от того, установил ли пользователь флаг командной строки “--user-data-dir”.

Если вы не включите эту политику, будет использован путь к профилю по умолчанию, но пользователь может переопределить его, используя флаг “--user-data-dir”. Пользователи могут найти каталог для профиля на edge://version/ под путем к профилю.

Чтобы избежать потери данных или других ошибок, не настраивайте эту политику для корневого каталога тома или каталога, который используется для других целей, поскольку Microsoft Edge управляет его содержимым.

Список переменных, которые можно использовать, см. в статье [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: UserDataDir
  - Имя GP: Установить каталог пользовательских данных
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: UserDataDir
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"${users}/${user_name}/Edge"
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: UserDataDir
  - Пример значения:
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### UserDataSnapshotRetentionLimit

  #### Ограничение количества снимков пользовательских данных, сохраняемых для применения в случае аварийного отката

  
  
  #### Поддерживаемые версии:

  - В Windows — версия 86 или более поздние

  #### Описание

  После каждого обновления основного номера версии Microsoft Edge создает снимок компонентов данных браузера пользователя для использования в дальнейшем в случае экстренного реагирования, которое требует временного отката версии. При выполнении временного отката к версии, для которой у пользователя есть соответствующий снимок, восстанавливаются данные из снимка. Это позволяет пользователям сохранять такие параметры, как закладки и данные автозаполнения.

Если не настроить эту политику, будет использоваться значение по умолчанию (3 снимка).

Если настроить эту политику, старые снимки будут удалены в соответствии с заданным вами ограничением. Если этой политике присвоено значение 0, снимки не делаются.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - целое число

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: UserDataSnapshotRetentionLimit
  - Имя групповой политики: Ограничение количества снимков пользовательских данных, сохраняемых для применения в случае аварийного отката
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: UserDataSnapshotRetentionLimit
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000003
```

  

  [В начало](#microsoft-edge---policies)

  ### UserFeedbackAllowed

  #### Разрешить обратную связь с пользователем

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Microsoft Edge использует функцию обратной связи Edge (включена по умолчанию), чтобы позволить пользователям отправлять отзывы, предложения или опросы клиентов и сообщать о любых проблемах с браузером. Также по умолчанию пользователи не могут отключить (отключить) функцию обратной связи Edge.

Если вы включите эту политику или не настроите ее, пользователи могут вызывать обратную связь Edge.

Если вы отключите эту политику, пользователи не смогут вызывать обратную связь Edge.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: UserFeedbackAllowed
  - Имя GP: Разрешить обратную связь с пользователем
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: UserFeedbackAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: UserFeedbackAllowed
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### VerticalTabsAllowed

  #### Настройка доступности вертикального макета для вкладок на боковой панели браузера

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 88 или позже

  #### Описание

  Указывает, может ли пользователь получить доступ к альтернативному макету, в котором вкладки вертикально выровнены по боковой стороне окна браузера, а не вверху.
Если открыто несколько вкладок, этот макет обеспечивает лучший просмотр и управление. Лучше видны названия сайтов, легче проверять выровненные значки, а также больше места для управления вкладками и их закрытия.

Если эта политика отключена, вертикальный макет вкладок не будет доступен для пользователей.

Если эта политика включена или не настроена, вкладки будут по-прежнему расположены вверху, но пользователь сможет включить вертикальные вкладки сбоку.


  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: VerticalTabsAllowed
  - Имя GP: настройка доступности вертикального макета для вкладок на боковой панели браузера
  - Путь к GP (обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: VerticalTabsAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Сведения о Mac и параметры
  
  - Имя ключа настройки: VerticalTabsAllowed
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### VideoCaptureAllowed

  #### Разрешить или заблокировать захват видео

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Контроль, могут ли сайты захватывать видео.

Если этот параметр включен или не настроен (по умолчанию), пользователю будет задан вопрос о доступе к захвату видео для всех сайтов, за исключением сайтов с URL-адресами, настроенными в списке политик [VideoCaptureAllowedUrls](#videocaptureallowedurls), которым будет предоставлен доступ без запроса.

Если вы отключите эту политику, пользователю не будет предложено, и захват видео доступен только для URL-адресов, настроенных в политике [VideoCaptureAllowedUrls](#videocaptureallowedurls).

Эта политика распространяется на все типы видеовходов, а не только на встроенную камеру.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: VideoCaptureAllowed
  - Имя GP: Разрешить или заблокировать захват видео
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: VideoCaptureAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: VideoCaptureAllowed
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### VideoCaptureAllowedUrls

  #### Сайты, которые могут получить доступ к устройствам захвата видео без запроса разрешения

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Укажите веб-сайты, основанные на шаблонах URL, которые могут использовать устройства захвата видео, не запрашивая у пользователя разрешения. Шаблоны в этом списке сопоставляются с источником безопасности запрашивающего URL. Если они совпадают, сайту автоматически предоставляется доступ к устройствам захвата видео.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: VideoCaptureAllowedUrls
  - Имя GP: Сайты, которые могут получить доступ к устройствам захвата видео без запроса разрешения.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\VideoCaptureAllowedUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: VideoCaptureAllowedUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### WPADQuickCheckEnabled

  #### Установить оптимизацию WPAD

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет отключить оптимизацию WPAD (автоматическое обнаружение веб-прокси) в Microsoft Edge.

Если вы отключите эту политику, оптимизация WPAD отключится, что заставит браузер дольше ждать DNS-серверы WPAD.

Если вы включаете или не настраиваете политику, включается оптимизация WPAD.

Независимо от того, включена ли или как эта политика, параметр оптимизации WPAD не может быть изменен пользователями.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WPADQuickCheckEnabled
  - Название GP: Установить оптимизацию WPAD
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: WPADQuickCheckEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: WPADQuickCheckEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### WebAppInstallForceList

  #### Настроить список принудительно установленных веб-приложений

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 80 или позже

  #### Описание

  При настройке этой политики укажите список веб-приложений, которые устанавливаются без вмешательства пользователя и которые пользователи не могут удалять или отключать.

Каждый элемент списка политики является объектом с обязательным элементом: URL-адрес (URL-адрес веб-приложения для установки)

и 3 необязательных элемента:
- default_launch_container (по умолчанию указывается режим окна, в котором открывается веб-приложение. Новая вкладка используется по умолчанию.)

- create_desktop_shortcut (true, если вы хотите создать ярлыки для рабочего стола Linux и Microsoft Windows.)

- fallback_app_name (начиная с Microsoft Edge 90 вы можете переопределять имя приложения, если оно не является прогрессивным веб-приложением (PWA) или временно устанавливается (если это PWA), но для завершения установки требуется проверка подлинности.)

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Dictionary

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WebAppInstallForceList
  - Имя GP: Настройка списка принудительно установленных веб-приложений.
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: WebAppInstallForceList
  - Тип значения: REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\WebAppInstallForceList = [
  {
    "create_desktop_shortcut": true, 
    "default_launch_container": "window", 
    "url": "https://www.contoso.com/maps"
  }, 
  {
    "default_launch_container": "tab", 
    "url": "https://app.contoso.edu"
  }, 
  {
    "default_launch_container": "window", 
    "fallback_app_name": "Editor", 
    "url": "https://app.contoso.com/editor"
  }
]
```

  ##### Компактный пример значения:

  ```
  SOFTWARE\Policies\Microsoft\Edge\WebAppInstallForceList = [{"create_desktop_shortcut": true, "default_launch_container": "window", "url": "https://www.contoso.com/maps"}, {"default_launch_container": "tab", "url": "https://app.contoso.edu"}, {"default_launch_container": "window", "fallback_app_name": "Editor", "url": "https://app.contoso.com/editor"}]
  ```
  

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: WebAppInstallForceList
  - Пример значения:
``` xml
<key>WebAppInstallForceList</key>
<array>
  <dict>
    <key>create_desktop_shortcut</key>
    <true/>
    <key>default_launch_container</key>
    <string>window</string>
    <key>url</key>
    <string>https://www.contoso.com/maps</string>
  </dict>
  <dict>
    <key>default_launch_container</key>
    <string>tab</string>
    <key>url</key>
    <string>https://app.contoso.edu</string>
  </dict>
  <dict>
    <key>default_launch_container</key>
    <string>window</string>
    <key>fallback_app_name</key>
    <string>Editor</string>
    <key>url</key>
    <string>https://app.contoso.com/editor</string>
  </dict>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### WebCaptureEnabled

  #### Включение функции захвата веб-страниц в Microsoft Edge

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 87 или позже

  #### Описание

  Включение функции захвата веб-содержимого в Microsoft Edge, с помощью которой пользователи могут записывать веб-содержимое и добавлять к нему примечания с помощью инструментов рукописного ввода.
Если эта политика включена или не настроена, команда "Захват веб-содержимого" отображается в контекстном меню, в параметрах и дополнительных меню, а также с помощью сочетаний клавиш CTRL + SHIFT + S.
Если политика отключена, пользователи не смогут получать доступ к функциям захвата веб-страниц в Microsoft Edge.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WebCaptureEnabled
  - Имя GP: Включение функции захвата веб-страниц в Microsoft Edge
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: WebCaptureEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа настройки: WebCaptureEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### WebComponentsV0Enabled

  #### Повторно включить API веб-компонентов v0 до M84 (устарело).

  
  >УСТАРЕЛО: эта политика устарела и не работает в Microsoft Edge версии 84 и более поздних.
  #### Поддерживаемые версии:

  - В Windows и macOS — версии c 80 по 84

  #### Описание

  Эта политика не работает потому, что она позволяет выборочно повторно включать эти функции в Microsoft Edge до версии 85. API веб-компонентов v0 (Shadow DOM v0, настраиваемые элементы v0 и импорт HTML) в 2018 году были признаны нерекомендуемыми и их использование по умолчанию было отключено, начиная с Microsoft Edge версии 80.

Если для этой политики задано значение True, функции веб-компонентов v0 будут включены для всех сайтов.

Если для этой политики установлено значение "ложь" или она не настроена, функции веб-компонентов v0 по умолчанию будут отключены, начиная с Microsoft Edge версии 80.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WebComponentsV0Enabled
  - Имя GP: Повторное включение API веб-компонентов v0 до M84 (устарело)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: WebComponentsV0Enabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: WebComponentsV0Enabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### WebDriverOverridesIncompatiblePolicies

  #### Разрешить WebDriver переопределять несовместимые политики (устарело)

  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:

  - На Windows и macOS с 77, до 84 версии

  #### Описание

  Эта политика не работает, поскольку WebDriver теперь совместим со всеми существующими политиками.

Эта политика позволяет пользователям функции WebDriver переопределять политики, которые могут мешать его работе.

В настоящее время эта политика отключает политики [SitePerProcess](#siteperprocess) и [IsolateOrigins](#isolateorigins).

Если политика включена, WebDriver сможет переопределять несовместимые политики.
Если политика отключена или не настроена, WebDriver не будет разрешено переопределять несовместимые политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WebDriverOverridesIncompatiblePolicies
  - Имя GP: Разрешить WebDriver переопределять несовместимые политики (устарело)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: WebDriverOverridesIncompatiblePolicies
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: WebDriverOverridesIncompatiblePolicies
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge---policies)

  ### WebRtcAllowLegacyTLSProtocols

  #### Разрешить устаревшую версию TLS/DTLS в WebRTC (устарело)

  >НЕ РЕКОМЕНДУЕТСЯ: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 88 или позже

  #### Описание

  Если вы включите эту политику, для одноранговых соединений WebRTC будут использоваться устаревшие версии протоколов TLS/DTLS (DTLS 1.0, TLS 1.0 и TLS 1.1).
Если вы отключите или не настроите эту политику, данные версии TLS/DTLS будут отключены.

Эта политика является временной и будет удалена в будущей версии Microsoft Edge.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WebRtcAllowLegacyTLSProtocols
  - Имя GP: разрешить устаревшую версию TLS/DTLS в WebRTC (устарело)
  - Путь к GP (обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: WebRtcAllowLegacyTLSProtocols
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000000
```

  #### Сведения о Mac и параметры
  
  - Имя ключа настройки: WebRtcAllowLegacyTLSProtocols
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### WebRtcLocalIpsAllowedUrls

  #### Управление выставлением локальных IP-адресов с помощью WebRTC

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 80 или позже

  #### Описание

  Указывает список источников (URL) или шаблонов имен хостов (например, "*contoso.com*"), для которых WebRTC должен предоставлять локальный IP-адрес.

Если вы включите эту политику и зададите список исходных (URL) или шаблонов имен хостов, когда параметр edge://flags/#enable-webrtc-hide-local-ips-with-mdns включен, WebRTC предоставит локальный IP-адрес для случаи, которые соответствуют шаблонам в списке.

Если вы отключите или не настроите эту политику, а параметр edge://flags/#enable-webrtc-hide-local-ips-with-mdns включен, WebRTC не будет предоставлять локальные IP-адреса. Локальный IP-адрес скрывается за именем хоста mDNS.

Если вы включите, отключите или не настроите эту политику, а параметр edge://flags/#enable-webrtc-hide-local-ips-with-mdns будет отключен, WebRTC предоставит локальные IP-адреса.

Обратите внимание, что эта политика ослабляет защиту локальных IP-адресов, которые могут понадобиться администраторам.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Список строк

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WebRtcLocalIpsAllowedUrls
  - Имя GP: Управление экспозицией локальных IP-адресов с помощью WebRTC
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - Путь (рекомендуется): N/A
  - Имя значения: 1, 2, 3, ...
  - Тип значения: список REG_SZ

  ##### Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = "*contoso.com*"

```

  #### Информация о Mac и настройки
  
  - Имя ключа предпочтения: WebRtcLocalIpsAllowedUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [В начало](#microsoft-edge---policies)

  ### WebRtcLocalhostIpHandling

  #### Ограничить доступность локального IP-адреса в WebRTC

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Позволяет вам указать, будет ли WebRTC предоставлять локальный IP-адрес пользователя.

Если для этой политики задано «AllowAllInterfaces» или «AllowPublicAndPrivateInterfaces», WebRTC предоставляет локальный IP-адрес.

Если для этой политики задано значение «AllowPublicInterfaceOnly» или «DisableNonProxiedUdp», WebRTC не предоставляет локальный IP-адрес.

Если вы не устанавливаете эту политику или отключаете ее, WebRTC предоставляет локальный IP-адрес.

Сопоставление параметров политики:

* AllowAllInterfaces (по умолчанию) = Разрешить все интерфейсы. Это раскрывает локальный IP-адрес

* AllowPublicAndPrivateInterfaces (default_public_and_private_interfaces) = Разрешить публичный и приватный интерфейсы по http-маршруту по умолчанию. Это раскрывает локальный IP-адрес

* AllowPublicInterfaceOnly (default_public_interface_only) = Разрешить общедоступный интерфейс по http-маршруту по умолчанию. Это не раскрывает локальный IP-адрес

* DisableNonProxiedUdp (disable_non_proxied_udp) = Использовать TCP, если прокси-сервер не поддерживает UDP. Это не раскрывает локальный IP-адрес

Используйте изложенные выше сведения при настройке этой политики.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WebRtcLocalhostIpHandling
  - Имя GP: Ограничение доступа локального IP-адреса с помощью WebRTC
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: WebRtcLocalhostIpHandling
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"default"
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: WebRtcLocalhostIpHandling
  - Пример значения:
``` xml
<string>default</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### WebRtcUdpPortRange

  #### Ограничить диапазон локальных портов UDP, используемых WebRTC

  
  
  #### Поддерживаемые версии:

  - На Windows и macOS начиная с 77 или позже

  #### Описание

  Ограничивает диапазон портов UDP, используемый WebRTC, указанным интервалом порта (включая конечные точки).

Настраивая эту политику, вы указываете диапазон локальных портов UDP, которые может использовать WebRTC.

Если вы не настроите эту политику, или если вы установите пустую строку или неверный диапазон портов, WebRTC может использовать любой доступный локальный порт UDP.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Строка

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WebRtcUdpPortRange
  - Имя GP: Ограничение диапазона локальных портов UDP, используемых WebRTC
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: WebRtcUdpPortRange
  - Тип значения: REG_SZ

  ##### Пример значения:

```
"10000-11999"
```

  #### Информация о Mac и настройки
  
  - Имя предпочтительного ключа: WebRtcUdpPortRange
  - Пример значения:
``` xml
<string>10000-11999</string>
```
  

  [В начало](#microsoft-edge---policies)

  ### WebWidgetAllowed

  #### Включить мини веб-приложение

  
  
  #### Поддерживаемые версии:

  - В Windows 88 и более поздних версий

  #### Описание

  Включает мини веб-приложение. Если включено, пользователи могут использовать это мини-приложение для поиска в Интернете на рабочем столе или в приложении. Мини-приложение содержит поле поиска, которое отображает предложения и открывает все поисковые запросы в Microsoft Edge. Поле поиска предоставляет поиск (на платформе Bing) и предложения URL-адреса. Мини-приложение также включает в себя плитки веб-канала, на которые пользователи могут щелкнуть, чтобы получить дополнительные сведения о msn.com в новой вкладке или окне браузера Microsoft Edge. Плитки веб-каналов могут содержать рекламные материалы. Мини-приложение можно запустить в параметрах Microsoft Edge или в меню "Другие инструменты".

Если включить или не настроить эту политику: мини веб-приложение будет автоматически включено для всех профилей.
В параметрах Microsoft Edge пользователи увидят возможность запуска мини-приложения.
В параметрах Microsoft Edge пользователи увидят элемент меню для запуска мини-приложение при начальной загрузке Windows (автозапуске).
Параметр включения мини-приложения при запуске будет включен, если включена политика [WebWidgetIsEnabledOnStartup](#webwidgetisenabledonstartup).
Если [WebWidgetIsEnabledOnStartup](#webwidgetisenabledonstartup) отключена или не настроена, параметр включения мини-приложения при запуске будет отключен.
Пользователь увидит элемент для запуска мини-приложения из меню "Другие инструменты" в Microsoft Edge. Пользователи могут запустить мини-приложение из меню "Другие инструменты".
Мини-приложение можно отключить с помощью параметра "Выход" в области уведомлений или закрыв мини-приложение на панели задач. Мини-приложение перезапускается при перезагрузке системы, если включен автозапуск.

Если эта политика отключена, мини веб-приложение будет отключено для всех профилей.
Параметр запуска мини-приложения из параметров Microsoft Edge будет отключен.
Параметр запуска мини-приложения при начальной загрузке Windows (автозапуск) будет отключен.
Параметр запуска мини-приложения из меню "Другие инструменты" в Microsoft Edge будет отключен.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WebWidgetAllowed
  - Имя GP: Включение мини-приложения
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: WebWidgetAllowed
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### WebWidgetIsEnabledOnStartup

  #### Разрешить запускать мини веб-приложение при начальной загрузке Windows

  
  
  #### Поддерживаемые версии:

  - В Windows 88 и более поздних версий

  #### Описание

  Позволяет запустить мини веб-приложения при начальной загрузке Windows.

Если включено: мини веб-приложение запускается при начальной загрузке Windows по умолчанию.
Если мини-приложение отключено с помощью политики [WebWidgetAllowed](#webwidgetallowed), эта политика не запустит мини-приложение при начальной загрузке Windows.

Если эта политика отключена: мини веб-приложение не будет запущено при начальной загрузке Windows для всех профилей.
Параметр запуска мини-приложения при начальной загрузке Windows будет отключен в параметрах Microsoft Edge.

Если эта политика не настроена: мини веб-приложение не будет запущено при начальной загрузке Windows для всех профилей.
Параметр запуска мини-приложения при начальной загрузке Windows будет выключен в параметрах Microsoft Edge.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WebWidgetIsEnabledOnStartup
  - Имя GP: Разрешение запуска мини веб-приложения при начальной загрузке Windows
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: WebWidgetIsEnabledOnStartup
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### WinHttpProxyResolverEnabled

  #### Использовать сопоставитель прокси-серверов Windows (не рекомендуется)

  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:

  - В Windows с 84 и более поздних версий

  #### Описание

  Использование этой политики не рекомендуется, так как она будет заменена аналогичной функцией в будущем выпуске, см. https://crbug.com/1032820.

Для сопоставления прокси-серверов при всех сетевых подключениях браузера используйте средства Windows, а не встроенный в Microsoft Edge сопоставитель прокси-серверов. В сопоставителе прокси-серверов Windows используются такие функции прокси-серверов Windows, как DirectAccess/NRPT.

В этой политике имеются проблемы, описанные в https://crbug.com/644030. Она приводит к получению PAC-файлов и их выполнению кодом Windows, включая PAC-файлы, установленные с помощью политики [ProxyPacUrl](#proxypacurl). Поскольку при получении PAC-файлов из сети это происходит с помощью кода Windows, а не Microsoft Edge, то такие политики сети, как [DnsOverHttpsMode](#dnsoverhttpsmode), не будут применяться к получению из сети PAC-файлов.

Если эта политика включена, будет использоваться сопоставитель прокси-серверов Windows.

Если вы отключите или не настроите эту политику, будет использоваться сопоставитель прокси-серверов Microsoft Edge.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя GP: WinHttpProxyResolverEnabled
  - Имя GP: Использование сопоставителя прокси-серверов Windows (не рекомендуется)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): N/A
  - Имя значения: WinHttpProxyResolverEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)

  ### WindowOcclusionEnabled

  #### Включить загораживание окна

  
  
  #### Поддерживаемые версии:

  - В Windows — версия 89 или более поздние

  #### Описание

  Включает загораживание окна в Microsoft Edge.

Если вы включите этот параметр, чтобы снизить нагрузку на процессор и энергопотребление, Microsoft Edge будет определять, когда окно закрыто другими окнами, и приостанавливать работу рисования пикселей.

Если вы отключите этот параметр, Microsoft Edge не будет определять, когда окно закрыто другими окнами.

Если это правило не задано, обнаружение скрытия окна будет включено.

  #### Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:

  - Boolean (Логическое)

  #### Сведения и параметры Windows

  ##### Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: WindowOcclusionEnabled
  - Имя групповой политики: включить загораживание окна
  - Путь к групповой политике (обязательно): Административные шаблоны/Microsoft Edge/
  - Путь GP (рекомендуется): N/A
  - Имя файла GP ADMX: MSEdge.admx

  ##### Параметры реестра Windows

  - Путь (обязательный): SOFTWARE\Policies\Microsoft\Edge
  - Путь (рекомендуется): Н/Д
  - Имя значения: WindowOcclusionEnabled
  - Тип значения: REG_DWORD

  ##### Пример значения:

```
0x00000001
```

  

  [В начало](#microsoft-edge---policies)


## Статьи по теме

- [Настройка Microsoft Edge](configure-microsoft-edge.md)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Блог базовых параметров безопасности Майкрософт](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)