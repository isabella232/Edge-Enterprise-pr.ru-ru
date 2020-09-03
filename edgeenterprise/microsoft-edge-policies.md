---
title: Документация по политикам браузера Microsoft Edge
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 09/01/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Документация Windows и Mac для всех политик, поддерживаемых браузером Microsoft Edge
ms.openlocfilehash: 9320d7e7b161e6d92421b05262391642b0fe1c2d
ms.sourcegitcommit: 827a47d641c7ddc1d89be5d5fc0615373dec18b0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993729"
---
# Microsoft Edge - Политики
Последняя версия Microsoft Edge включает в себя следующие политики. Эти политики можно использовать для настройки работы Microsoft Edge в вашей организации.

Информацию о дополнительном наборе политик, используемых для управления тем, как и когда обновляется Microsoft Edge, можно найти в [справочнике по политике обновления Microsoft Edge](microsoft-edge-update-policies.md).

Вы можете скачать [Microsoft Security Compliance Toolkit](https://www.microsoft.com/download/details.aspx?id=55319) для рекомендуемых базовых параметров конфигурации безопасности для Microsoft Edge. Дополнительные сведения см. в [блоге Microsoft Security Baselines](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines).

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## Доступные политики
В этих таблицах перечислены все связанные с браузером групповые политики, доступные в этом выпуске Microsoft Edge. Для получения дополнительных сведений о конкретных политиках см. ссылки в таблице.

|||
|-|-|
|[Параметры Application Guard](#application-guard-settings)|[Передавать](#cast)|
|[Настройки контента](#content-settings)|[Поставщик поиска по умолчанию](#default-search-provider)|
|[Расширения](#extensions)|[Проверка подлинности HTTP](#http-authentication)|
|[Встроенные сообщения](#native-messaging)|[Менеджер паролей и защита](#password-manager-and-protection)|
|[Вывод на печать](#printing)|[Прокси-сервер](#proxy-server)|
|[Параметры SmartScreen](#smartscreen-settings)|[Автозагрузка, домашняя страница и новая вкладка](#startup-home-page-and-new-tab-page)|
|[Дополнительно](#additional)|

### [*Параметры Application Guard*](#application-guard-settings-policies)
|Имя политики|Заголовок|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|Прокси-сервер контейнера Application Guard|
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
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|Настройка геолокации по умолчанию|
|[DefaultImagesSetting](#defaultimagessetting)|Настройка изображений по умолчанию|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|Контроль использования небезопасных исключений содержимого|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|Настройка JavaScript по умолчанию|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|Настройка уведомлений по умолчанию|
|[DefaultPluginsSetting](#defaultpluginssetting)|Настройка Adobe Flash по умолчанию|
|[DefaultPopupsSetting](#defaultpopupssetting)|Параметр всплывающего окна по умолчанию|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|Контроль использования веб-API Bluetooth|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|Контроль использования API WebUSB|
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
|[PluginsAllowedForUrls](#pluginsallowedforurls)|Разрешить плагин Adobe Flash на определенных сайтах|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|Блокировать плагин Adobe Flash на определенных сайтах|
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
|[ExtensionAllowedTypes](#extensionallowedtypes)|Настройте разрешенные типы расширений|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|Разрешить установку определенных расширений|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|Определить, какие расширения нельзя установить|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|Определить, какие расширения устанавливаются в автоматическом режиме|
|[ExtensionInstallSources](#extensioninstallsources)|Настроить расширение и исходные тексты для установки пользовательских скриптов|
|[ExtensionSettings](#extensionsettings)|Настройка параметров управления расширениями|
### [*Проверка подлинности HTTP*](#http-authentication-policies)
|Имя политики|Заголовок|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|Разрешить перекрестные исходные запросы HTTP Basic Auth|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|Указывает список серверов, которым Microsoft Edge может делегировать учетные данные пользователя|
|[AuthSchemes](#authschemes)|Поддерживаемые схемы аутентификации|
|[AuthServerAllowlist](#authserverallowlist)|Настроить список разрешенных серверов аутентификации|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|Отключить поиск CNAME при согласовании проверки подлинности Kerberos|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Включить нестандартный порт в Kerberos SPN|
|[NtlmV2Enabled](#ntlmv2enabled)|Проверьте, включена ли аутентификация NTLMv2|
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
### [*Вывод на печать*](#printing-policies)
|Имя политики|Заголовок|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|Правила выбора принтера по умолчанию|
|[PrintHeaderFooter](#printheaderfooter)|Верхние и нижние колонтитулы печати|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|Установите системный принтер по умолчанию в качестве принтера по умолчанию|
|[PrintingEnabled](#printingenabled)|Включить печать|
|[UseSystemPrintDialog](#usesystemprintdialog)|Печать с использованием системного диалога печати|
### [*Прокси-сервер*](#proxy-server-policies)
|Имя политики|Заголовок|
|-|-|
|[ProxyBypassList](#proxybypasslist)|Настроить правила обхода прокси|
|[ProxyMode](#proxymode)|Настройте параметры прокси-сервера|
|[ProxyPacUrl](#proxypacurl)|Задайте URL-адрес прокси-файла .pac|
|[ProxyServer](#proxyserver)|Настройте адрес или URL прокси-сервера|
|[ProxySettings](#proxysettings)|Параметры прокси-сервера|
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
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|Задать новую страницу вкладки логотип компании (устарело)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|Скрыть стандартные сайты по умолчанию на новой вкладке|
|[NewTabPageLocation](#newtabpagelocation)|Настроить URL-адрес страницы "Новая вкладка"|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|Установить быстрые ссылки на новую вкладку|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|Включение предварительной загрузки новой вкладки для ускорения отрисовки|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|Настройка Microsoft Edge для новой вкладки|
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
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|Позволяет странице показывать всплывающие окна во время ее выгрузки|
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
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|Настройте автоматический вход с учетной записью домена Active Directory, если учетная запись домена Azure AD отсутствует|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|Настроить онлайн текст в речь|
|[ConfigureShare](#configureshare)|Настройте обмен опытом|
|[CustomHelpLink](#customhelplink)|Укажите пользовательскую ссылку справки|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|Проверка перехвата DNS включена|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|Установите Microsoft Edge в качестве браузера по умолчанию|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|Разрешить доступ к службе поиска по умолчанию в контекстном меню|
|[DefaultSensorsSetting](#defaultsensorssetting)|Стандартный параметр для датчиков|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|Управлять использованием API Serial|
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
|[EditFavoritesEnabled](#editfavoritesenabled)|Позволяет пользователям редактировать избранное|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|Повторно включить устаревшие функции веб-платформы на ограниченное время|
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
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|Использование политики ссылки по умолчанию no-referrer-when-downgrade (не рекомендуется)|
|[ForceNetworkInProcess](#forcenetworkinprocess)|Принудительный запуск сетевого кода в процессе браузера (устарело)|
|[ForceSync](#forcesync)|Принудительно синхронизировать данные браузера и не показывать запрос на разрешение синхронизации|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|Принудительный минимальный ограниченный режим YouTube|
|[FullscreenAllowed](#fullscreenallowed)|Разрешить полноэкранный режим|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|Включить глобальный кэш проверки подлинности HTTP|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|Принудительная прямая навигация по сайту в интрасети вместо поиска по отдельным словам в адресной строке|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|Настройте список имен, которые будут обходить проверку политики HSTS|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|Используйте аппаратное ускорение, когда доступно|
|[HideFirstRunExperience](#hidefirstrunexperience)|Скрыть первый запуск опыта и заставки|
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
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|Настройка списка сайтов для режима Enterprise|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|Укажите, как ведут себя внутренние переходы на ненастроенные сайты при запуске со страниц режима Internet Explorer.|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|Разрешить тестирование режима Internet Explorer|
|[IsolateOrigins](#isolateorigins)|Включить изоляцию сайта для определенных источников|
|[LocalProvidersEnabled](#localprovidersenabled)|Разрешить предложения от местных поставщиков|
|[ManagedFavorites](#managedfavorites)|Настроить избранное|
|[ManagedSearchEngines](#managedsearchengines)|Управление поисковыми движками|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|Максимальное количество одновременных подключений к прокси-серверу|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|Разрешить Google Cast подключаться к устройствам Cast на всех IP-адресах|
|[MetricsReportingEnabled](#metricsreportingenabled)|Включение отчетов с данными об использовании и сбоях (устарело)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|Включение загораживание собственного окна|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|Установка времени ожидания перехода между вкладками списка сайтов для режима предприятия|
|[NetworkPredictionOptions](#networkpredictionoptions)|Включить прогнозирование сети|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|Настройте, всегда ли у пользователя профиль по умолчанию автоматически входит в свою учетную запись на работе или в школе|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|Контроль, где применяются ограничения безопасности для небезопасных источников|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|Разрешить веб-сайтам запрашивать доступные способы оплаты|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|Разрешить персонализацию рекламы, поиска и новостей, отправляя историю просмотров в Microsoft|
|[PinningWizardAllowed](#pinningwizardallowed)|Мастер «Разрешить закрепление на панели задач»|
|[ProactiveAuthEnabled](#proactiveauthenabled)|Включить проактивную аутентификацию|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|Включить рекламный контент на всей вкладке|
|[PromptForDownloadLocation](#promptfordownloadlocation)|Спросите, где сохранить загруженные файлы|
|[QuicAllowed](#quicallowed)|Разрешить протокол QUIC|
|[RelaunchNotification](#relaunchnotification)|Уведомить пользователя, что перезагрузка браузера рекомендуется или требуется для ожидающих обновлений|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|Установите период времени для уведомлений об обновлениях|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|Включить целостность кода рендерера|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|Укажите, требуются ли онлайн-проверки OCSP / CRL для локальных якорей доверия|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|Включить разрешение ошибок навигации с помощью веб-службы|
|[RestrictSigninToPattern](#restrictsignintopattern)|Ограничить, какие учетные записи могут быть использованы в качестве основных учетных записей Microsoft Edge|
|[RoamingProfileLocation](#roamingprofilelocation)|Настройка каталога перемещаемого профиля|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|Разрешение использования перемещаемых копий для данных профиля Microsoft Edge|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|Расширение настроек содержимого Adobe Flash на все содержимое|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|Разрешить пользователям переходить со страницы предупреждения HTTPS|
|[SSLVersionMin](#sslversionmin)|Минимальная версия TLS включена|
|[SaveCookiesOnExit](#savecookiesonexit)|Сохранять файлы cookie при закрытии Microsoft Edge|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|Отключить сохранение истории браузера|
|[ScreenCaptureAllowed](#screencaptureallowed)|Разрешить или запретить захват экрана|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|Включить прокрутку до текста, указанного в фрагментах URL|
|[SearchSuggestEnabled](#searchsuggestenabled)|Включить варианты поиска|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|Веб-сайты или домены, которым не требуется разрешение на прямую аттестацию ключа безопасности|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|Отправлять все сайты интрасети в Internet Explorer|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|Отправка сведений о сайтах для улучшения служб Майкрософт (устарело)|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|Разрешить доступ к датчиками на определенных сайтах|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|Блокировать доступ к датчиками на определенных сайтах|
|[SerialAskForUrls](#serialaskforurls)|Разрешить API Serial на определенных сайтах|
|[SerialBlockedForUrls](#serialblockedforurls)|Блокировать API Serial на определенных сайтах|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|Показать ярлык Microsoft Office на панели избранного|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|Включить поддержку подписанного HTTP Exchange (SXG)|
|[SitePerProcess](#siteperprocess)|Включить изоляцию сайта для каждого сайта|
|[SpellcheckEnabled](#spellcheckenabled)|Включить проверку орфографии|
|[SpellcheckLanguage](#spellchecklanguage)|Включить определенные языки проверки орфографии|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|Принудительное отключение языков проверки орфографии|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|Включение более строгой обработки смешанного контента (не рекомендуется)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|Подавить предупреждение о неподдерживаемой ОС|
|[SyncDisabled](#syncdisabled)|Отключить синхронизацию данных с помощью служб Microsoft Sync Services|
|[SyncTypesListDisabled](#synctypeslistdisabled)|Настройте список типов, которые исключены из синхронизации|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|Включение функции безопасности TLS 1.3 для локальных якорей доверия (устарело)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|Выбор наборов шифров TLS для отключения|
|[TabFreezingEnabled](#tabfreezingenabled)|Разрешить замораживание фоновых вкладок|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|Включить завершающие процессы в диспетчере задач браузера|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|Установка ограничения на размер памяти (в мегабайтах), который может использовать один экземпляр Microsoft Edge.|
|[TrackingPrevention](#trackingprevention)|Блокировка отслеживания активности пользователей в Интернете|
|[TranslateEnabled](#translateenabled)|Включить перевод|
|[URLAllowlist](#urlallowlist)|Определите список разрешенных URL|
|[URLBlocklist](#urlblocklist)|Блокировать доступ к списку URL-адресов|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|Включение функции клиентских подсказок User-Agent (устарело)|
|[UserDataDir](#userdatadir)|Установить каталог пользовательских данных|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|Ограничение количества снимков пользовательских данных, сохраняемых для применения в случае аварийного отката|
|[UserFeedbackAllowed](#userfeedbackallowed)|Разрешить обратную связь с пользователем|
|[VideoCaptureAllowed](#videocaptureallowed)|Разрешить или заблокировать захват видео|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|Сайты, которые могут получить доступ к устройствам захвата видео без запроса разрешения|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|Установить оптимизацию WPAD|
|[WebAppInstallForceList](#webappinstallforcelist)|Настроить список принудительно установленных веб-приложений|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|Повторно включить API веб-компонентов v0 до M84 (устарело).|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|Разрешить интерфейсу WebDriver переопределять несовместимые политики (устарело)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|Управление выставлением локальных IP-адресов с помощью WebRTC|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|Ограничить доступность локального IP-адреса в WebRTC|
|[WebRtcUdpPortRange](#webrtcudpportrange)|Ограничить диапазон локальных портов UDP, используемых WebRTC|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|Использовать сопоставитель прокси-серверов Windows (не рекомендуется)|




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
  - Имя ключа предпочтения: ShowCastIconInToolbar
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
  Укажите список сайтов на основе шаблонов URL, для которых Microsoft Edge должен автоматически выбирать сертификат клиента, если сайт запрашивает его.

Значение должно быть массивом строковых словарей JSON. Каждый словарь должен иметь форму { "pattern": "$URL_PATTERN", "filter" : $FILTER }, где $URL_PATTERN - это шаблон настройки контента. $FILTER ограничивает, из каких клиентских сертификатов браузер будет автоматически выбирать. Независимо от фильтра будут выбраны только сертификаты, соответствующие запросу сертификата сервера. Например, если $FILTER имеет форму {"ISSUER": {"CN": "$ ISSUER_CN"}}, дополнительно выбираются только клиентские сертификаты, выданные сертификатом с общим именем $ ISSUER_CN. Если $FILTER содержит раздел «ISSUER» и «SUBJECT», сертификат клиента должен удовлетворять обоим условиям для выбора. Если $FILTER указывает организацию («O»), сертификат должен иметь хотя бы одну организацию, которая соответствует указанному значению, которое будет выбрано. Если $FILTER указывает организационную единицу («OU»), сертификат должен иметь хотя бы одну организационную единицу, которая соответствует указанному значению, которое будет выбрано. Если $FILTER является пустым словарем {}, выбор клиентских сертификатов дополнительно не ограничен.

Если вы не настроите эту политику, автоматический выбор не будет сделан ни для одного сайта.

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
  - Имя ключа предпочтения: AutoSelectCertificateForUrls
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
  - Имя ключа предпочтения: CookiesAllowedForUrls
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
  - Имя ключа предпочтения: CookiesBlockedForUrls
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
  #### Настройка Adobe Flash по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Сначала проверяются [PluginsAllowedForUrls](#pluginsallowedforurls) и [PluginsBlockedForUrls](#pluginsblockedforurls), а затем эта политика. Варианты: "ClickToPlay" и "BlockPlugins". Если этой политике присвоено значение "BlockPlugins", этот подключаемый модуль запрещается на всех веб-сайтах. "ClickToPlay" позволяет запустить подключаемый модуль Flash, но пользователям нужно щелкнуть заполнитель, чтобы запустить его.

                                                                                                                                                                                                                                            

Если не настроить эту политику, она использует параметр BlockPlugins и пользователи смогут изменить его.

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
  - Название GP: настройка Adobe Flash по умолчанию
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
  - Имя ключа предпочтения: DefaultWebUsbGuardSetting
  - Пример значения:
``` xml
<integer>2</integer>
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
  - Имя ключа предпочтения: JavaScriptBlockedForUrls
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
  Позволяет вам вернуть все файлы cookie в прежнее поведение SameSite. Возврат к унаследованному поведению приводит к тому, что файлы cookie, для которых не указан атрибут SameSite, обрабатываются так, как если бы они были «SameSite = None», и устраняет необходимость в файлах cookie «SameSite = None» для переноса атрибута «Secure».

Если вы не установите эту политику, поведение по умолчанию для файлов cookie, в которых не указан атрибут SameSite, будет зависеть от других источников конфигурации для функции SameSite-по-умолчанию. Эта функция может быть установлена в полевых условиях или путем включения того же флага site-by-default-cookies в edge://flags.

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

Возврат к унаследованному поведению приводит к тому, что файлы cookie, для которых не указан атрибут SameSite, обрабатываются так, как если бы они были «SameSite = None», и устраняет необходимость в файлах cookie «SameSite = None» для переноса атрибута «Secure».

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
  - Имя ключа предпочтения: LegacySameSiteCookieBehaviorEnabledForDomainList
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
  #### Разрешить плагин Adobe Flash на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Определите список сайтов на основе шаблонов URL, которые могут запускать плагин Adobe Flash.

Если вы не настроите эту политику, глобальное значение по умолчанию из политики [DefaultPluginsSetting](#defaultpluginssetting) (если установлено) или личная конфигурация пользователя используется для всех сайтов.

Подробные сведения о шаблонах допустимых URL-адресов см. в[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Начиная с M85, шаблоны с подстановочными знаками "*" и "[*.]" в URL-адресах узла больше не поддерживаются для этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:
  - Список строк

  #### Сведения и параметры Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя GP: PluginsAllowedForUrls
  - Имя GP: разрешить плагин Adobe Flash на определенных сайтах
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
  #### Блокировать плагин Adobe Flash на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Определите список сайтов, основанных на шаблонах URL, которые заблокированы для запуска Adobe Flash.

Если вы не настроите эту политику, глобальное значение по умолчанию из политики [DefaultPluginsSetting](#defaultpluginssetting) (если установлено) или личная конфигурация пользователя используется для всех сайтов.

Подробные сведения о шаблонах допустимых URL-адресов см. в[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Начиная с M85, шаблоны с подстановочными знаками "*" и "[*.]" в URL-адресах узла больше не поддерживаются для этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:
  - Список строк

  #### Сведения и параметры Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя GP: PluginsBlockedForUrls
  - Имя GP: заблокировать плагин Adobe Flash на определенных сайтах
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
  Определите список сайтов на основе шаблонов URL, которые могут открывать всплывающие окна.

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
  Определите список сайтов, основанный на шаблонах URL, которым запрещено открывать всплывающие окна.

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
  - Имя ключа предпочтения: PopupsBlockedForUrls
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


  #### Информация о Mac и настройки
  - Имя ключа предпочтения: WebUsbAllowDevicesForUrls
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
  - Имя ключа предпочтения: WebUsbAskForUrls
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
  - Имя ключа предпочтения: WebUsbBlockedForUrls
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

  ### ExtensionAllowedTypes
  #### Настройте разрешенные типы расширений
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Контролирует, какие типы расширений могут быть установлены, и ограничивает доступ во время выполнения.

Этот параметр определяет разрешенные типы расширений и хосты, с которыми они могут взаимодействовать. Значение представляет собой список строк, каждая из которых должна иметь одно из следующих значений: "extension", "theme", "user_script", и "hosted_app". См. Документацию по расширениям Microsoft Edge для получения дополнительной информации об этих типах.

Обратите внимание, что эта политика также влияет на принудительно устанавливаемые расширения с помощью политики [ExtensionInstallForcelist](#extensioninstallforcelist).

Если вы включите эту политику, будут установлены только расширения, соответствующие типу в списке.

Если вы не настроите эту политику, ограничения на допустимые типы расширений не применяются.

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
  - Имя ключа предпочтения: ExtensionAllowedTypes
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
  По умолчанию все расширения разрешены. Однако если вы заблокируете все расширения, установив для политики 'ExtensionInstallBlockList' значение "*", пользователи смогут устанавливать только расширения, определенные в этой политике.

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
  Перечислите конкретные расширения, которые пользователи НЕ МОГУТ установить в Microsoft Edge. При развертывании этой политики все ранее установленные в этом списке расширения будут отключены, и пользователь не сможет их включить. Если вы удаляете элемент из списка заблокированных расширений, это расширение автоматически включается везде, где оно было установлено ранее.

Используйте "*", чтобы заблокировать все расширения, которые явно не указаны в списке разрешений.

Если вы не настроите эту политику, пользователи могут установить любое расширение в Microsoft Edge.

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
  - Имя ключа предпочтения: ExtensionInstallBlocklist
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
  Указывает расширения, которые устанавливаются без вывода сообщений, без вмешательства пользователя, и которые пользователи не могут удалить или отключить («принудительно установлен»). Все разрешения, запрашиваемые расширениями, предоставляются неявно, без взаимодействия с пользователем, включая любые дополнительные разрешения, запрашиваемые будущими версиями расширения. Кроме того, разрешения предоставляются для API расширений enterprise.deviceAttributes и enterprise.platformKeys. (Эти два API доступны только для расширений, которые установлены принудительно.)

Эта политика имеет приоритет над потенциально конфликтующей политикой [ExtensionInstallBlocklist](#extensioninstallblocklist). Когда вы удаляете расширение из списка принудительной установки, оно автоматически удаляется Microsoft Edge.

Принудительная установка ограничена только приложениями и расширениями, перечисленными на веб-сайте надстроек Microsoft Edge, для экземпляров, не являющихся следующими: экземпляры Windows, присоединенные к домену Microsoft Active Directory, либо экземпляры Windows 10 Pro и Windows Корпоративная, зарегистрированные для управления устройствами, а также экземпляры macOS, управляемые посредством MDM или присоединенные к домену через MCX.

Обратите внимание, что пользователи могут изменять исходный код любого расширения с помощью Инструментов разработчика, что потенциально делает его неработоспособным. Если это проблема, установите политику [DeveloperToolsAvailability](#developertoolsavailability).

Используйте следующий формат, чтобы добавить расширение в список:

[extensionID];[updateURL]

- extensionID - 32-буквенная строка, найденная на edge://extensions в режиме разработчика.

- updateURL (необязательно) - это адрес XML-документа манифеста обновления для приложения или расширения, как описано в разделе [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043). Если вы хотите установить расширение из интернет-магазина Chrome, укажите URL-адрес обновления интернет-магазина Chrome. https://clients2.google.com/service/update2/crx. Обратите внимание, что URL-адрес обновления, установленный в этой политике, используется только для начальной установки; последующие обновления расширения используют URL-адрес обновления, указанный в манифесте расширения. Если элемент updateURL не задан, то предполагается, что расширение размещено в Microsoft Store, и используется следующий URL-адрес обновления (https://edge.microsoft.com/extensionwebstorebase/v1/crx).

Например, gggmmkjegpiggikcnhidnjjhmicpibll; https://edge.microsoft.com/extensionwebstorebase/v1/crx устанавливает приложение Microsoft Online с URL-адреса «обновления» в Microsoft Store. Для получения дополнительной информации о расширениях хостинга см: [https://go.microsoft.com/fwlink/?linkid=2095044](https://go.microsoft.com/fwlink/?linkid=2095044).

Если вы не настроите эту политику, расширения не будут установлены автоматически, и пользователи могут удалить любое расширение в Microsoft Edge.

Обратите внимание, что эта политика не распространяется на режим InPrivate.

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
  - Имя ключа предпочтения: ExtensionInstallForcelist
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

По умолчанию пользователи должны загрузить файл *.crx для каждого расширения или сценария, который они хотят установить, а затем перетащить его на страницу настроек Microsoft Edge. Эта политика позволяет определенным URL-адресам использовать расширение или скрипт для пользователя.

Каждый элемент в этом списке является шаблоном соответствия стилю расширения (см. [https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039)). Пользователи могут легко устанавливать элементы с любого URL-адреса, соответствующего элементу в этом списке. Этим шаблонам должно быть разрешено как местоположение файла *.crx, так и страница, с которой начинается загрузка (другими словами, реферер).

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
  Настраивает параметры управления расширениями для Microsoft Edge.

Эта политика управляет несколькими параметрами, включая параметры, контролируемые любыми существующими политиками, относящимися к расширениям. Эта политика переопределяет любые устаревшие политики, если установлены оба.

Эта политика сопоставляет идентификатор расширения или URL-адрес обновления с его конфигурацией. При использовании идентификатора расширения конфигурация применяется только к указанному добавочному номеру. Задайте конфигурацию по умолчанию для специального идентификатора "*", чтобы применить его ко всем расширениям, которые конкретно не перечислены в этой политике. С помощью URL-адреса обновления конфигурация применяется ко всем расширениям с точным URL-адресом обновления, указанным в манифесте этого расширения, как описано в разделе [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043).

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


  #### Информация о Mac и настройки
  - Имя ключа предпочтения: ExtensionSettings
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
  #### Разрешить перекрестные исходные запросы HTTP Basic Auth
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Определяет, может ли стороннее содержимое на странице открывать диалоговое окно HTTP Basic Auth.

Как правило, это отключено в качестве защиты от фишинга. Если вы не настроите эту политику, она отключена, и стороннее вспомогательное содержимое не сможет открыть диалоговое окно HTTP Basic Auth.

  #### Поддерживаемые функции:
  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:
  - Boolean (Логическое)

  #### Сведения и параметры Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя GP: AllowCrossOriginAuthPrompt
  - Имя GP: Разрешить запросы HTTP Basic Auth для разных источников
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

  ## Собственные политики обмена сообщениями

  [В начало](#microsoft-edge---policies)

  ### NativeMessagingAllowlist
  #### Контроль, какие нативные хосты обмена сообщениями могут использовать пользователи
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Перечислите конкретные собственные узлы обмена сообщениями, которые пользователи могут использовать в Microsoft Edge.

По умолчанию все собственные узлы обмена сообщениями разрешены. Если для политики [NativeMessagingBlocklist](#nativemessagingblocklist) задано значение *, все собственные узлы обмена сообщениями блокируются, и загружаются только перечисленные здесь собственные узлы обмена сообщениями.

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
  Указывает, какие собственные узлы обмена сообщениями не следует использовать.

Используйте '*', чтобы заблокировать все собственные узлы обмена сообщениями, если они явно не указаны в списке разрешений.

Если вы не настроите эту политику, Microsoft Edge загрузит все установленные собственные узлы обмена сообщениями.

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
  Включает установку на уровне пользователя собственных узлов обмена сообщениями.

Если вы отключите эту политику, Microsoft Edge будет использовать только собственные хосты обмена сообщениями, установленные на системном уровне.

По умолчанию, если вы не настроите эту политику, Microsoft Edge разрешит использование собственных узлов обмена сообщениями на уровне пользователя.

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
  - Имя ключа предпочтения: PrintHeaderFooter
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
  - Имя ключа предпочтения: PrintPreviewUseSystemDefaultPrinter
  - Пример значения:
``` xml
<false/>
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
  #### Настроить правила обхода прокси
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Определяет список хостов, для которых Microsoft Edge обходит любой прокси.

Эта политика применяется, только если вы выбрали «Использовать фиксированные прокси-серверы» в политике [ProxyMode](#proxymode). Если вы выбрали любой другой режим для настройки политик прокси, не включайте и не настраивайте эту политику.

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
  - Имя GP: Настройка правил обхода прокси
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
  #### Настройте параметры прокси-сервера
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Укажите настройки прокси-сервера, используемые Microsoft Edge. Если вы включите эту политику, пользователи не смогут изменять параметры прокси.

Если вы решите никогда не использовать прокси-сервер и всегда подключаться напрямую, все остальные параметры игнорируются.

Если вы решите использовать настройки прокси-сервера системы, все остальные параметры будут игнорироваться.

Если вы выбираете автоопределение прокси-сервера, все остальные параметры игнорируются.

Если вы выбираете фиксированный режим прокси-сервера, вы можете указать дополнительные параметры в [ProxyServer](#proxyserver) и «Список разделенных запятыми правил обхода прокси».

Если вы решите использовать прокси-скрипт .pac, вы должны указать URL-адрес скрипта в «URL-адресе файла .pac прокси».

Для подробных примеров, перейдите к [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

Если вы включите эту политику, Microsoft Edge будет игнорировать все параметры, связанные с прокси, указанные в командной строке.

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
  - Имя GP: Настройка параметров прокси-сервера
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
  #### Задайте URL-адрес прокси-файла .pac
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Указывает URL-адрес для файла автоматической настройки прокси (PAC).

Эта политика применяется, только если вы выбрали «Использовать сценарий прокси .pac» в политике [ProxyMode](#proxymode). Если вы выбрали любой другой режим для настройки политик прокси, не включайте и не настраивайте эту политику.

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
  - Имя GP: установите URL-адрес прокси-файла .pac
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
  #### Настройте адрес или URL прокси-сервера
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Определяет URL прокси-сервера.

Эта политика применяется, только если вы выбрали «Использовать фиксированные прокси-серверы» в политике [ProxyMode](#proxymode). Если вы выбрали любой другой режим для настройки политик прокси, не включайте и не настраивайте эту политику.

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
  - Имя GP: настроить адрес или URL прокси-сервера
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
  - Имя ключа предпочтения: ProxyServer
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

Поле ProxyMode позволяет указать прокси-сервер, используемый Microsoft Edge, и запрещает пользователям изменять настройки прокси.

Поле ProxyPacUrl - это URL-адрес прокси-файла .pac.

Поле ProxyServer является URL-адресом прокси-сервера.

Поле ProxyBypassList представляет собой список прокси-хостов, которые Microsoft Edge обходит.

Если вы выберете значение 'direct' как 'ProxyMode', прокси никогда не будет использоваться, а все остальные поля будут игнорироваться.

Если в качестве значения «system» выбрано «ProxyMode», используется системный прокси-сервер, а все остальные поля игнорируются.

Если вы выберете значение «auto_detect» как «ProxyMode», все остальные поля будут игнорироваться.

Если вы выбрали значение «fixed_server» в качестве «ProxyMode», используются поля «ProxyServer» и «ProxyBypassList».

Если вы выбираете значение «pac_script» как «ProxyMode», то используются поля «ProxyPacUrl» и «ProxyBypassList».

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
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
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
  <string>direct</string>
  <key>ProxyPacUrl</key>
  <string>https://internal.site/example.pac</string>
  <key>ProxyServer</key>
  <string>123.123.123.123:8080</string>
</dict>
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
  - Имя ключа предпочтения: SmartScreenAllowListDomains
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
  - Имя ключа предпочтения: SmartScreenEnabled
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
  - Имя ключа предпочтения: SmartScreenPuaEnabled
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
  - Имя ключа предпочтения: NewTabPageAllowedBackgroundTypes
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### NewTabPageCompanyLogo
  #### Задать новую страницу вкладки логотип компании (устарело)
  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 79 или позже

  #### Описание
  Мы не рекомендуем использовать эту политику, поскольку она не работает должным образом. Она не будет работать в Microsoft Edge версии 86.

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
  - Название GP: Установка логотипа компании на новой вкладке (не рекомендуется)
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

Эта политика определяет страницу, которая открывается при создании новых вкладок (в том числе при открытии новых окон). Это также влияет на начальную страницу, если она настроена на открытие новой вкладки.

Эта политика не определяет, какая страница открывается при запуске; это контролируется политикой [RestoreOnStartup](#restoreonstartup). Она также не влияет на домашнюю страницу, если настроено ее открытие в новой вкладке.

Если вы не настроите эту политику, используется новая вкладка по умолчанию.

Если вы настраиваете эту политику *и* политику [NewTabPageSetFeedType](#newtabpagesetfeedtype), эта политика имеет приоритет.

Если указан неверный URL, откроются новые вкладки о: // blank.

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
  #### Настройка Microsoft Edge для новой вкладки
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 79 или позже

  #### Описание
  Позволяет выбрать режим новостей Microsoft News или Office 365 для новой вкладки.

Если для этой политики задано значение «News», пользователи увидят новостную ленту Microsoft на странице новой вкладки.

Если для этой политики задано значение «Office», после входа в браузер Azure Active Directory пользователи увидят работу ленты Office 365 на новой вкладке.

Если вы отключите или не настроите эту политику:

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
  - Имя GP: Настройка взаимодействия с новой вкладкой Microsoft Edge
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
Если вы отключите эту политику, пользователи не смогут видеть внутренние результаты в списке предложений адресной строки Microsoft Edge.
Если вы включили набор политик, который заставляет поставщика поиска по умолчанию ([DefaultSearchProviderEnabled](#defaultsearchproviderenabled), [DefaultSearchProviderName](#defaultsearchprovidername) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)), и указанный поставщик поиска не является Bing, то эта политика не применима, и в предложении Bing не будет предложений Microsoft для поиска в Bing. Список предложений бара.

  #### Поддерживаемые функции:
  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

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
  - Имя ключа предпочтения: AdsSettingForIntrusiveAdsSites
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

Если вы отключите эту политику, пользователи не смогут удалить историю просмотров и загрузок.

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
  #### Позволяет странице показывать всплывающие окна во время ее выгрузки
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 78 и более поздних версий

  #### Описание
  Эта политика позволяет администратору указать, что страница может отображать всплывающие окна во время ее выгрузки.Эта политика позволяет администратору показывать всплывающие окна во время выгрузки страницы.

Когда политика включена, на страницах разрешается показывать всплывающие окна во время их выгрузки.

Когда для политики установлено значение «отключено» или «не установлено», на страницах не разрешается показывать всплывающие окна во время их выгрузки. Это согласно спецификации: (https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name).

Эта политика будет удалена в будущем.

  #### Поддерживаемые функции:
  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:
  - Boolean (Логическое)

  #### Сведения и параметры Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя GP: AllowPopupsDuringPageUnload
  - Имя GP: Позволяет странице показывать всплывающие окна во время ее выгрузки
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
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
  - Имя ключа предпочтения: AllowTrackingForUrls
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

Если вы включите эту политику, Microsoft Edge будет обрабатывать файлы PDF как загружаемые файлы и разрешать пользователям открывать их с помощью приложения по умолчанию.

Если вы не настроите эту политику или не отключите ее, Microsoft Edge откроет файлы PDF (если пользователь не отключит ее).

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
  - Имя ключа предпочтения: AutoImportAtFirstRun
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

* У вас есть арендатор EDU, но политика не работает.

* Ваш IP-адрес занесен в белый список за то, что у вас был бесплатный поиск без рекламы.

* Вы испытывали возможность поиска без рекламы в устаревшей версии Microsoft Edge и хотите обновить ее до новой версии Microsoft Edge.

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
  - Имя ключа предпочтения: BlockThirdPartyCookies
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
  - Имя ключа предпочтения: BrowserGuestModeEnabled
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
  - Имя ключа предпочтения: BrowserNetworkTimeQueriesEnabled
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
  - Имя ключа предпочтения: BrowserSignin
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge---policies)

  ### BuiltInDnsClientEnabled
  #### Используйте встроенный DNS-клиент
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Определяет, использовать ли встроенный DNS-клиент.

Это не влияет на то, какие DNS-серверы используются; просто программный стек, который используется для связи с ними. Например, если операционная система настроена на использование корпоративного DNS-сервера, этот же сервер будет использоваться встроенным DNS-клиентом. Однако возможно, что встроенный клиент DNS будет обращаться к серверам по-разному, используя более современные протоколы, связанные с DNS, такие как DNS-через-TLS.

Если вы включите эту политику, будет использоваться встроенный клиент DNS, если он доступен.

Если вы отключите эту политику, клиент никогда не будет использоваться.

Если вы не настроите эту политику, встроенный DNS-клиент по умолчанию включен в MacOS, и пользователи могут изменить, использовать ли встроенный DNS-клиент, отредактировав edge://flags или указав флаг командной строки.

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

```


  #### Информация о Mac и настройки
  - Имя ключа предпочтения: CollectionsServicesAndExportsBlockList
  - Пример значения:
``` xml
<array>
  <string>pinterest_suggestions</string>
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
  - Имя ключа предпочтения: ConfigureDoNotTrack
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ConfigureOnPremisesAccountAutoSignIn
  #### Настройте автоматический вход с учетной записью домена Active Directory, если учетная запись домена Azure AD отсутствует
  
  
  #### Поддерживаемые версии:
  - В Windows с 81 и более поздних версий

  #### Описание
  Включите использование учетных записей Active Directory для автоматического входа, если компьютеры ваших пользователей подключены к домену, а ваша среда не является гибридной. Если вы хотите, чтобы пользователи автоматически входили в свои учетные записи Azure Active Directory, присоединитесь к Azure AD (Дополнительные сведения см. в статье [https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197)) или гибридному (Дополнительные сведения см. в статье [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365).) свою среду.

Если вы отключили политику [BrowserSignin](#browsersignin), эта политика не будет действовать.

Если вы включите эту политику и зададите для нее значение «SignInAndMakeDomainAccountNonRemovable», Microsoft Edge автоматически выполнит вход в систему пользователей, которые находятся на компьютерах, подключенных к домену, с использованием их учетных записей Active Directory.

Если для этой политики установлено значение «Disabled» или она не настроена, Microsoft Edge не будет автоматически входить в систему пользователей, которые находятся на компьютерах, подключенных к домену с помощью учетных записей Active Directory.

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
  - Имя ключа предпочтения: DefaultSearchProviderContextMenuAccessAllowed
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
  - Имя ключа предпочтения: DiskCacheDir
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
  - Имя ключа предпочтения: DiskCacheSize
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
  - Имя ключа предпочтения: DnsOverHttpsMode
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
  - Имя ключа предпочтения: DownloadDirectory
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
  #### Повторно включить устаревшие функции веб-платформы на ограниченное время
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
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
  - Имя GP: Повторно включить устаревшие функции веб-платформы на ограниченное время
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
  - Имя ключа предпочтения: EnableDomainActionsDownload
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
  - Имя ключа предпочтения: EnableSha1ForLocalAnchors
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
  - Имя ключа предпочтения: FamilySafetySettingsEnabled
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
  - Имя ключа предпочтения: ForceBingSafeSearch
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
  - Имя ключа предпочтения: ForceGoogleSafeSearch
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge---policies)

  ### ForceLegacyDefaultReferrerPolicy
  #### Использование политики ссылки по умолчанию no-referrer-when-downgrade (не рекомендуется)
  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:
  - В Windows и macOS с 81 и более поздних версий

  #### Описание
  Эта политика не рекомендуется, так как она предусмотрена только в качестве краткосрочного механизма, предоставляющего организациям больше времени на обновление веб-содержимого, если и при условии, что оно не совместимо с текущей политикой источника ссылки по умолчанию Она не будет работать в Microsoft Edge версии 86.

По умолчанию в Microsoft Edge политика источника ссылки по умолчанию укрепляется с текущего значения no-referrer-when-downgrade на более безопасное strict-origin-when-cross-origin через постепенный выпуск.

До развертывания эта корпоративная политика не будет иметь никакого эффекта. После выпуска, когда эта корпоративная политика включена, для политики источника ссылки Microsoft Edge по умолчанию будет установлено прежнее значение no-referrer-when-downgrade.

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
  - Имя GP: Использование политики ссылки по умолчанию no-referrer-when-downgrade (не рекомендуется)
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

Для правильной работы этой политики, политика [BrowserSignin](#browsersignin) не должна быть настроена или должна быть включена. Если политика [ForceSync](#forcesync) отключена, то политика [BrowserSignin](#browsersignin) не будет применяться.

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
  - Имя ключа предпочтения: HSTSPolicyBypassList
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
  Укажите использование аппаратного ускорения, если оно доступно. Если вы включите эту политику или не настроите ее, аппаратное ускорение будет включено, если только функция GPU явно не заблокирована.

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

-Синхронизация не будет включена по умолчанию, и пользователи смогут включить синхронизацию из настроек синхронизации.

Если вы отключите или не настроите эту политику, отобразятся «Первый запуск» и экран заставки.

Примечание. Конкретные параметры конфигурации, отображаемые пользователю в режиме первого запуска, также могут управляться с помощью других специальных политик. Вы можете использовать политику HideFirstRunExperience в сочетании с этими политиками, чтобы настроить конкретную работу браузера на управляемых устройствах. Некоторые из этих других политик:

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

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
  Эта политика заменяет политику флага ie-mode-test. Она позволяет пользователям открыть вкладку режима IE из параметра меню пользовательского интерфейса.

       Этот параметр работает совместно с политикой [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) с установленным значением "IEMode" и политикой [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist), список которой содержит минимум одну запись.

       Если эта политика включена, пользователи могут открыть вкладку режима IE из параметра пользовательского интерфейса и перевести текущий сайт в режим IE.

       Если эта политика отключена, пользователи не увидят параметр пользовательского интерфейса непосредственно в меню.

       Если не настроить эту политику, вы сможете настроить флаг ie-mode-test вручную.

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


  #### Информация о Mac и настройки
  - Имя ключа предпочтения: ManagedSearchEngines
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
  #### Включение отчетов с данными об использовании и сбоях (устарело)
  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
   
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Этот параметр политики является устаревшим. В настоящее время она поддерживается, но устареет в Microsoft Edge 89. Эта политика заменяется новой политикой: [DiagnosticData](#diagnosticdata) для Windows 7, Windows 8 и macOS. Эта политика заменяется политикой "Разрешить телеметрию" в Windows 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

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
  - Имя групповой политики: Включение отчетов с данными об использовании и сбоях (устарело)
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
  #### Включение загораживание собственного окна
  
  
  #### Поддерживаемые версии:
  - В Windows с 84 и более поздних версий

  #### Описание
  Включает загораживание собственного окна в Microsoft Edge.

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
  - Уникальное имя GP: NativeWindowOcclusionEnabled
  - Имя GP: Включение загораживания собственного окна
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
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
  - Имя ключа предпочтения: NetworkPredictionOptions
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

Если вы включите эту политику, в Windows будет создан несъемный профиль с учетной записью пользователя или учебой. Этот профиль нельзя выписать или удалить.

Если вы отключите или не настроите эту политику, профиль, автоматически входящий в учетную запись пользователя для работы или учебы в Windows, может быть подписан или удален пользователем.

Если вы хотите настроить вход в браузер, используйте политику [BrowserSignin](#browsersignin).

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft Active Directory, а также экземпляров Windows 10 Pro или Корпоративная, зарегистрированных для управления устройством.

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
  #### Включить проактивную аутентификацию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Позволяет настроить, следует ли включать проактивную аутентификацию.

Если вы включите эту политику, Microsoft Edge попытается проактивно аутентифицировать зарегистрированного пользователя с помощью служб Microsoft. Microsoft Edge регулярно проверяет наличие у веб-службы обновленного манифеста, содержащего конфигурацию, определяющую, как это сделать.

Если вы отключите эту политику, Microsoft Edge не будет пытаться проактивно аутентифицировать зарегистрированного пользователя с помощью служб Microsoft. Microsoft Edge больше не проверяет с помощью веб-службы обновленный манифест, содержащий конфигурацию для этого.

Если вы не настроите эту политику, проактивная аутентификация будет включена.

  #### Поддерживаемые функции:
  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Нет - требуется перезапуск браузера

  #### Тип данных:
  - Boolean (Логическое)

  #### Сведения и параметры Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя GP: ProactiveAuthEnabled
  - Имя GP: Включить проактивную аутентификацию
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
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
  Если эта политика включена или не задана, тогда включена целостность кода Renderer. Эту политику следует отключать только в случае возникновения проблем совместимости со сторонним программным обеспечением, которое должно запускаться в процессах рендеринга Microsoft Edge.

Отключение этой политики отрицательно сказывается на безопасности и стабильности Microsoft Edge, поскольку неизвестный и потенциально враждебный код может загружаться в процессах рендеринга Microsoft Edge.

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

Если эта политика отключена или не настроена, то будут использоваться только обычные локальные профили.

Политика [SyncDisabled](#syncdisabled) отключает синхронизацию всех данных, переопределяя политику.

Дополнительные сведения об использовании перемещаемых профилей пользователей см. в https://docs.microsoft.com/windows-server/storage/folder-redirection/deploy-roaming-user-profiles.

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
  #### Расширение настроек содержимого Adobe Flash на все содержимое
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
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
  - Имя GP: Расширение настроек содержимого Adobe Flash на все содержимое
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
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
  #### Разрешить пользователям переходить со страницы предупреждения HTTPS
  
  
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
  - Имя GP: Разрешить пользователям переходить со страницы предупреждений HTTPS
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

  ### SSLVersionMin
  #### Минимальная версия TLS включена
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Устанавливает минимальную поддерживаемую версию SSL. Если вы не настроите эту политику, Microsoft Edge использует минимальную версию по умолчанию, TLS 1.0.

Если вы включите эту политику, вы можете установить минимальную версию на одно из следующих значений: «TLSv1», «TLSv1.1» или «TLSv1.2». Если установлено, Microsoft Edge не будет использовать любую версию SSL/TLS ниже указанной версии. Любое нераспознанное значение игнорируется.

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
  - Имя ключа предпочтения: SecurityKeyPermitAttestation
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
  #### Отправка сведений о сайтах для улучшения служб Майкрософт (устарело)
  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
   
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Этот параметр политики является устаревшим. В настоящее время она поддерживается, но устареет в Microsoft Edge 89. Эта политика заменяется новой политикой: [DiagnosticData](#diagnosticdata) для Windows 7, Windows 8 и macOS. Эта политика заменяется политикой "Разрешить телеметрию" в Windows 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

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
  - Имя групповой политики: Отправка сведений о сайтах для улучшения служб Майкрософт (устарело)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
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
  - Имя ключа предпочтения: SendSiteInfoToImproveServices
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

  ### ShowOfficeShortcutInFavoritesBar
  #### Показать ярлык Microsoft Office на панели избранного
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS начиная с 77 или позже

  #### Описание
  Указывает, следует ли включать ярлык Office.com в панели избранного. Для пользователей, вошедших в Microsoft Edge, ярлык переносит пользователей в их приложения и документы Microsoft Office.

Если эта политика включена или не настроена, пользователи могут выбрать, следует ли видеть ярлык, изменив переключатель в контекстном меню панели избранного.

Если политика отключена, ярлык не будет отображаться.

  #### Поддерживаемые функции:
  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:
  - Boolean (Логическое)

  #### Сведения и параметры Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя GP: ShowOfficeShortcutInFavoritesBar
  - Имя GP: Показать ярлык Microsoft Office на панели избранного
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
  - Имя ключа предпочтения: SitePerProcess
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
  #### Включение более строгой обработки смешанного контента (не рекомендуется)
  >УСТАРЕЛО: Эта политика устарела. В настоящее время он поддерживается, но устареет в следующем выпуске.
  
  #### Поддерживаемые версии:
  - В Windows и macOS с 81 и более поздних версий

  #### Описание
  Эта политика не рекомендуется, так как она предусмотрена только в качестве краткосрочного механизма, предоставляющего организациям больше времени на обновление веб-содержимого, если и при условии, что оно не совместимо с более строгой обработкой смешанного содержимого. Она не будет работать в Microsoft Edge версии 85.

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
  - Имя групповой политики: включение более строгой обработки смешанного содержимого (не рекомендуется)
  - Путь к GP (Обязательный): Административные шаблоны/Microsoft Edge/
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
  - Имя ключа предпочтения: SuppressUnsupportedOSWarning
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


 
Если вы не установите эту политику или не примете ее в соответствии с рекомендациями, пользователи смогут включить или отключить синхронизацию. Если вы примените эту политику как обязательную, пользователи не смогут включить синхронизацию.

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
  - Имя ключа предпочтения: SyncDisabled
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
  - Имя ключа предпочтения: SyncTypesListDisabled
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
  - Имя ключа предпочтения: TrackingPrevention
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
  Разрешить доступ к указанным URL-адресам, как к исключениям из списка заблокированных URL-адресов.

Отформатируйте шаблон URL в соответствии с [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Вы можете использовать эту политику, чтобы открывать исключения в ограничительных списках блокировки. Например, вы можете включить '*' в список блокировки, чтобы заблокировать все запросы, а затем использовать эту политику, чтобы разрешить доступ к ограниченному списку URL-адресов. Вы можете использовать эту политику, чтобы открывать исключения для определенных схем, поддоменов других доменов, портов или определенных путей.

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
  - Имя ключа предпочтения: UserAgentClientHintsEnabled
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
  - Имя ключа предпочтения: VideoCaptureAllowedUrls
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
  Определяет список веб-сайтов, которые устанавливаются автоматически, без участия пользователя, и которые не могут быть удалены или отключены пользователем.

Каждый элемент списка политики является объектом со следующими членами:
  - "url", который является обязательным. "url" должен быть URL-адрес веб-приложения для установки.

Значения для необязательных членов:
  - "launch_container" должен быть либо «окном», либо «вкладкой», чтобы указать, как будет открываться веб-приложение после его установки.
  - "create_desktop_shortcut" должно быть истинным, если ярлык на рабочем столе должен быть создан в Windows.

Если значение "default_launch_container" отсутствует, приложение по умолчанию открывается на вкладке. Независимо от значения "default_launch_container", пользователи могут изменять, в каком контейнере будет открываться приложение. Если "create_desktop_shortcuts" опущено, ярлыки на рабочем столе не будут созданы.

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
  }
]
```


  #### Информация о Mac и настройки
  - Имя ключа предпочтения: WebAppInstallForceList
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
</array>
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
  #### Разрешить интерфейсу WebDriver переопределять несовместимые политики (устарело)
        
  
  
  
  >УСТАРЕЛО: эта политика устарела и не работает в Microsoft Edge версии 84 и более поздних.
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
  - Имя GP: Разрешение интерфейсу WebDriver переопределять несовместимые политики (устарело)
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
  - Имя ключа предпочтения: WebRtcLocalhostIpHandling
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
  - Имя ключа предпочтения: WebRtcUdpPortRange
  - Пример значения:
``` xml
<string>10000-11999</string>
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


## См. также
- [Настройка Microsoft Edge](configure-microsoft-edge.md)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Блог базовых параметров безопасности Майкрософт](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)
