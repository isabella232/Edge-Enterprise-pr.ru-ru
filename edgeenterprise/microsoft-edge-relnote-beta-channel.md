---
title: Заметки о выпуске Microsoft Edge для канала Beta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 12/04/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для канала Beta
ms.openlocfilehash: 39e6062d8cf7ce0e5f03ecf26daaae4cc06bd4cf
ms.sourcegitcommit: 46d42a284e54574811a7c934a36d85a3526fc8ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "11196540"
---
# Заметки о выпуске для Microsoft Edge из канала Beta

Эти заметки о выпуске содержат сведения о новых возможностях и обновлениях, не связанных с безопасностью, которые включены Microsoft Edge канала Beta

> [!IMPORTANT]
> Смотрите эти [обновления в каналах Microsoft Edge](https://blogs.windows.com/msedgedev/2020/03/20/update-stable-channel-releases/).

## Версия 87.0.664.55: 3 декабря

Исправлены ошибки и проблемы с производительностью. В этом выпуске поддерживается следующая новая функция.

- **Оповещения создаются в том случае, если пароль пользователя обнаружен среди украденных данных в Интернете**. Пароли пользователей сверяются с репозиторием известных украденных учетных данных, а пользователю отправляется оповещение при обнаружении совпадения. Для обеспечения безопасности и конфиденциальности пароли пользователей хэшируются и шифруются, когда они сверяются с базой данных украденных учетных данных.

## Версия 87.0.664.52: 30 ноября

Исправлены ошибки и проблемы с производительностью.

## Версия 87.0.664.40: 18 ноября

Исправлены ошибки и проблемы с производительностью.

## Версия 87.0.664.36: 16 ноября

Исправлены ошибки и проблемы с производительностью.

## Версия 87.0.664.30: 9 ноября

Исправлены ошибки и проблемы с производительностью.

## Версия 87.0.664.24: 2 ноября

Исправлены ошибки и проблемы с производительностью.

## Версия 87.0.664.18: 26 октября

Исправлены ошибки и проблемы с производительностью.

<!-- begin major 87 -->
## Версия 87.0.664.12: 20 октября

### Обновления компонентов

- **Включение средств конфиденциальности режима терминала**. В версии 87 и в дальнейших версиях Microsoft Edge в режиме терминала появляются средства, которые помогут компаниям обеспечивать конфиденциальность пользовательских данных. Благодаря этим функциям включаются такие возможности, как удаление пользовательских данных при выходе, удаление загруженных файлов и сброс настроенной начальной даты возможности после указанного периода бездействия. Подробнее о [Настройке режима терминала Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).
- **Включение развертывания ClickOnce по умолчанию**. ClickOnce в Microsoft Edge 87 включен по умолчанию, что позволяет снизить количество барьеров для развертывания организациями программного обеспечения и более эффективного согласования поведения устаревшей версии браузера Microsoft Edge. Начиная с Microsoft Edge 87 состояние "Не настроено" политики ClickOnceEnabled отражает новое состояние ClickOnce по умолчанию "Включено" (по сравнению с предыдущим состоянием по умолчанию "Отключено").
- **Интегрирование продуктивности с настраиваемым, связанным с работой содержимым веб-канала на странице новой вкладки (NTP) организации**. На странице новой вкладки (NTP) организации страница производительности Office 365, предлагаемая пользователям, вошедшим в систему с помощью своей рабочей или учебной учетной записи, объединяется с персонализированными, связанными с работой корпоративными и отраслевыми каналами, организованными на одной странице. Пользователи смогут распознавать знакомое содержимое Office 365 и Поиска (Майкрософт) для бизнеса на платформе Bing. Кроме того, они смогут с легкостью переходить к настраиваемому каналу "My Feed" с содержимым и модулями, которые относятся к пользователю, компании или отрасли пользователя, а также подборке других каналов, к которым организация предоставила доступ. [Подробнее](https://docs.microsoft.com/microsoft-365/admin/manage/manage-industry-news?view=o365-worldwide&preserve-view=true).

- **Конфиденциальность и безопасность.**

  - Поддержка привязки маркеров TLS для сайтов с настроенной политикой. Привязка маркеров TLS предотвращает атаки, направленные на кражу маркеров, для того, чтобы файлы cookie нельзя было повторно использовать на устройстве, которое не является устройством, на котором они изначально были установлены. При использовании привязки маркеров TLS необходимо задать политику [AllowTokenBindingForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowtokenbindingforurls) и обеспечить поддержку перечисленными сайтами этой возможности.

- **Поддержка пера в качестве маркера в PDF-файлах.** Пользователи смогут выделять маркером текст в PDF-файле с помощью клавиатуры.

- **Вывод на печать:**

  - При печати на обеих сторонах выберите сторону, на которую вам необходимо перевернуть. При печати на обеих сторонах пользователь может перевернуть лист длинной стороной или короткой стороной.
  - Выбор режима растеризации печати для предприятия. Управление печатью Microsoft Edge на принтере без поддержки PostScript в Windows. Иногда для правильной печати на принтерах без поддержки PostScript необходимо правильно растеризовать задания для печати. Параметры печати — "Полная" и "Быстрая".

### Обновления политик

#### Новые политики

Добавлено десять новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Добавлены следующие новые политики.

- [ConfigureFriendlyURLFormat](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configurefriendlyurlformat) — Настройка формата по умолчанию для URL-адресов, скопированных из Microsoft Edge, и определение доступности пользователям дополнительных форматов.
- [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled) — Включены покупки в Microsoft Edge.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hideinternetexplorerredirectuxforincompatiblesitesenabled) — Скрыты диалоговое окно однократного перенаправления и баннер в Microsoft Edge.
- [KioskAddressBarEditingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) — Настройка редактирования в адресной строке для общедоступного просмотра в режиме терминала.
- [KioskDeleteDownloadsOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) — Удаление файлов, загруженных в ходе сеанса терминала, при закрытии Microsoft Edge.
- [PasswordRevealEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordrevealenabled) — Включение кнопки "Показать пароль.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerpreventbhoinstall) — Запрет установки объекта BHO для перенаправления несовместимых сайтов из Internet Explorer в Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerredirectmode) — Перенаправление несовместимых сайтов из Internet Explorer в Microsoft Edge.
- [SpeechRecognitionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#speechrecognitionenabled) — Настройка распознавания речи.
- [WebCaptureEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcaptureenabled) - Включение функции захвата веб-страниц в Microsoft Edge.

#### Политика устарела

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) — Настройка взаимодействия с новой вкладкой Microsoft Edge.

#### Устаревшая политика

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) — Повторное включение устаревших функций веб-платформы на ограниченное время (устарело).

<!-- end major 87 -->

## Версия 86.0.622.43: 16 октября

Исправлены ошибки и проблемы с производительностью.

## Версия 86.0.622.36: 7 октября

Исправлены ошибки и проблемы с производительностью.

## Версия 86.0.622.31: 1 октября

Исправлены ошибки и проблемы с производительностью.

## Версия 86.0.622.28: 28 сентября

Исправлены ошибки и проблемы с производительностью.

## Версия 86.0.622.15: 14 сентября

Исправлены ошибки и проблемы с производительностью.

## Версия 86.0.622.11: 9 сентября

### Обновления компонентов

* **Режим Internet Explorer:**

   * Позвольте пользователям применять пользовательский интерфейс (UI) Microsoft Edge для проверки сайтов в режиме Internet Explorer. С Microsoft Edge версии 86 администраторы могут включить параметр пользовательского интерфейса, чтобы пользователи могли загружать вкладки в режиме Internet Explorer для тестирования или в качестве временной меры до того, как сайты будут добавлены в XML-файл списка сайтов.

* **Удаление загрузки с диска с помощью диспетчера загрузок.** Пользователи теперь могут удалять загруженные файлы с диска, не выходя из браузера. Новая функция удаления загрузок находится в контекстном меню панели загрузок или на странице загрузок.

* **Откат к предыдущей версии Microsoft Edge.** Функция отката позволяет администраторам вернуть известную хорошую версию Microsoft Edge, если у вас возникла проблема с последней версией Microsoft Edge.
[Подробнее](edge-learnmore-rollback.md).

* **Принудительное включение синхронизации по умолчанию в организации.**  Администраторы могут включить синхронизацию учетных записей Azure Active Directory (Azure AD) по умолчанию с помощью политики [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync).

* **Обновления PDF:**

  * Оглавление для PDF-документов. С версии 86 в Microsoft Edge добавлена поддержка оглавления, которое позволяет пользователям легко перемещаться по PDF-документам.
  * Доступ ко всем возможностям PDF на экранах небольшого форм-фактора. Получите доступ ко всем возможностям средства чтения PDF-файлов Microsoft Edge на устройствах с небольшим размером экрана.
  * Поддержка пера в качестве маркера в PDF-файлах. Благодаря этому обновлению пользователи могут использовать собственное цифровое перо для прямого выделения текста в PDF-файлах по аналогии с обычным маркером на листе бумаги.
  * Улучшена прокрутка PDF-документов. Теперь вы сможете наслаждаться прокруткой без запинок при просмотре длинных PDF-документов.

* **Автоматическое переключение профилей в Windows 7, 8 и 8.1.** Автоматическое переключение профилей, в настоящее время доступное в Microsoft Edge в Windows 10, теперь расширено и на более ранние версии Windows (Windows 7, 8 и 8.1). Дополнительные сведения см. в записи блога об [автоматическом переключении профилей](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **Пользователям предлагаются варианты автозаполнения при вводе поискового запроса на веб-сайте надстроек Microsoft Edge.** Автозаполнение помогает пользователям быстро завершать поисковые запросы без необходимости ввода всей строки. Это удобно, так как пользователям не нужно запоминать правильное написание и они могут выбирать из доступных демонстрируемых вариантов.

* **Удаление API кэша приложений HTML5.**  С Microsoft Edge версии 86 устаревший API кэша приложений, позволяющий использовать веб-страницы в автономном режиме, удаляется из Microsoft Edge. Сведения для веб-разработчиков о замене API кэша приложений на служебные сценарии доступны в [документации для веб-разработчиков](https://web.dev/appcache-removal/).  Важно! Вы можете запросить [маркер AppCache OriginTrial](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673), позволяющий сайтам продолжать использовать устаревший API кэша приложений до Microsoft Edge версии 90.

* **Безопасность:**

  * Поддержка безопасной службы DNS (DNS поверх HTTPS).  С Microsoft Edge версии 86 доступны параметры для управления безопасной службой DNS на неуправляемых устройствах. Эти параметры недоступны пользователям управляемых устройств, но ИТ-администраторы могут включать и отключать безопасную службу DNS с помощью групповой политики [dnsoverhttpsmode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#dnsoverhttpsmode).


* **Добавление настраиваемого изображения на страницу новой вкладки (NTP) с помощью групповой политики.** С Microsoft Edge версии 86 на странице новой вкладки доступна возможность для замены стандартного изображения на настраиваемое изображение, предоставляемое пользователем. Возможность управления свойствами этого изображения также поддерживается групповой политикой.

* **Сопоставление настроенных сочетаний клавиш с VS Code.** Средства разработчика Microsoft Edge теперь поддерживают настройку сочетаний клавиш в средствах разработчика для обеспечения соответствия вашему редактору/IDE. (В Microsoft Edge 84 мы добавили возможность сопоставлять сочетания клавиш средств разработчика с VS Code.)

* **Замена политик [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) и [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) для более ранних версий Windows и macOS.** Эти политики не рекомендуются в Microsoft Edge версии 86 и станут устаревшими в Microsoft Edge версии 89.<br>
Эти политики заменяются политикой [Разрешить телеметрию](https://go.microsoft.com/fwlink/?linkid=2099569) в Windows 10 и новой политикой [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) для всех остальных платформ. Это позволит пользователям управлять диагностическими данными, отправляемыми в корпорацию Майкрософт, для Windows 7, 8, 8.1 и macOS.

* **Параметр файлов cookie, используемый по умолчанию: SameSite=Lax**. Чтобы повысить безопасность и конфиденциальность в Интернете, по умолчанию файлы cookie будут обрабатываться с использованием параметра [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite). Это означает, что файлы cookie будут отправляться только в основном контексте и будут пропущены в запросах, отправляемых третьим сторонам. Это изменение может повлиять на совместимость для веб-сайтов, которым требуются файлы cookie для правильной работы сторонних ресурсов. Чтобы разрешить такие файлы cookie, веб-разработчики могут помечать файлы cookie, которые должны настраиваться и отправляться в сторонних контекстах, добавив явные атрибуты `SameSite=none` и `Secure` при настройке файлов cookie. Организации, которые хотят исключить определенные сайты из этого изменения, могут сделать это с помощью политики [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) или отказаться от изменения на всех сайтах с помощью политики [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled).

### Обновления политик

#### Новые политики

Добавлено 19 политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [CollectionsServicesAndExportsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#collectionsservicesandexportsblocklist) — блокировка доступа к указанному списку служб и целевым объектам экспорта в Коллекциях.
- [DefaultSensorsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsensorssetting) — стандартный параметр для датчиков.
- [DefaultSerialGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultserialguardsetting) — управлять использованием API Serial.
- [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) — отправлять обязательные и необязательные диагностические данных об использовании браузера.
- [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed) — разрешить доступ к средству Enterprise Mode Site List Manager.
- [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync) — принудительно синхронизировать данные браузера и не показывать запрос на разрешение синхронизации.
- [InsecureFormsWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecureformswarningsenabled) — включить предупреждения для небезопасных форм.
- [InternetExplorerIntegrationTestingAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) — разрешить тестирование режима Internet Explorer.
- [SpotlightExperiencesAndRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#spotlightexperiencesandrecommendationsenabled) — выберите, могут ли пользователи получать настроенные фоновые изображения и текст, предложения, уведомления и советы для служб Майкрософт.
- [NewTabPageAllowedBackgroundTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageallowedbackgroundtypes) — настройка типов фона, разрешенных для макета страницы новой вкладки.
- [SaveCookiesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#savecookiesonexit) — сохранять файлы cookie при закрытии Microsoft Edge.
- [SensorsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsallowedforurls) — разрешить доступ к датчиками на определенных сайтах.
- [SensorsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsblockedforurls) — блокировать доступ к датчиками на определенных сайтах.
- [SerialAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialaskforurls) — разрешить API Serial на определенных сайтах.
- [SerialBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialblockedforurls) — блокировать API Serial на определенных сайтах.
- [URLBlocklist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlblocklist) — заблокировать доступ к списку URL-адресов.
- [URLAllowlist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlallowlist) — определить список разрешенных URL-адресов.
- [UserAgentClientHintsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) — включение функции клиентских подсказок User-Agent.
- [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#userdatasnapshotretentionlimit) — ограничение количества снимков пользовательских данных, сохраняемых для применения в случае аварийного отката.

#### Устаревшие политики

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) — включить отчеты с данными об использовании и сбоях.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) — отправка сведений о сайтах для улучшения служб Майкрософт.

#### Устаревшая политика

[TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled) — включение функции безопасности TLS 1.3 для местных якорей доверия.

#### Изменен заголовок политики

[NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled)— включение загораживания собственного окна

#### Изменено описание политики

- [AdsSettingForIntrusiveAdsSites](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#adssettingforintrusiveadssites)
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls)
- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled)
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy)
- [AutoImportAtFirstRun](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoimportatfirstrun)
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes)
- [BrowserSignin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsersignin)
- [ClearBrowsingDataOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearbrowsingdataonexit) 
- [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled)
- [CommandLineFlagSecurityWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#commandlineflagsecuritywarningsenabled)
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin)
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare)
- [CookiesAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#cookiesallowedforurls)
- [CustomHelpLink](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#customhelplink)
- [DefaultCookiesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultcookiessetting)
- [DefaultGeolocationSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultgeolocationsetting)
- [DefaultImagesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultimagessetting)
- [DefaultInsecureContentSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultinsecurecontentsetting)
- [DefaultJavaScriptSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultjavascriptsetting)
- [DefaultNotificationsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultnotificationssetting)
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting)
- [DefaultPopupsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpopupssetting)
- [DefaultSearchProviderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchproviderenabled)
- [DefaultWebBluetoothGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebbluetoothguardsetting)
- [DefaultWebUsbGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebusbguardsetting)
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload)
- [DeveloperToolsAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#developertoolsavailability)
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors)
- [DownloadRestrictions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#downloadrestrictions)
- [EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures)
- [WinHttpProxyResolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#winhttpproxyresolverenabled)
- [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol)
- [ExternalProtocolDialogShowAlwaysOpenCheckbox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox)
- [ExtensionInstallForcelist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ForceBingSafeSearch](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcebingsafesearch)
- [ForceYouTubeRestrict](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forceyoutuberestrict)
- [HomepageIsNewTabPage](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepageisnewtabpage)
- [HomepageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepagelocation)
- [InPrivateModeAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#inprivatemodeavailability)
- [InternetExplorerIntegrationEnhancedHangDetection](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationenhancedhangdetection)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect)
- [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled)
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled)
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout)
- [NetworkPredictionOptions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#networkpredictionoptions)
- [NewTabPageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation)
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox)
- [NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype)
- [NonRemovableProfileEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nonremovableprofileenabled)
- [PasswordProtectionWarningTrigger](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionwarningtrigger)
- [PasswordProtectionLoginURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionloginurls)
- [PasswordProtectionChangePasswordURL](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionchangepasswordurl)
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls)
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls)
- [PreventSmartScreenPromptOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverride)
- [PreventSmartScreenPromptOverrideForFiles](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverrideforfiles)
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode)
- [RegisteredProtocolHandlers](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#registeredprotocolhandlers)
- [RelaunchNotification](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#relaunchnotification)
- [RestoreOnStartup](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartup)
- [RestoreOnStartupURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartupurls)
- [RestrictSigninToPattern](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restrictsignintopattern)
- [SSLVersionMin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslversionmin)
- [SmartScreenAllowListDomains](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenallowlistdomains)
- [SmartScreenEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenenabled)
- [SmartScreenForTrustedDownloadsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenfortrusteddownloadsenabled)
- [SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled)
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled)
- [TrackingPrevention](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#trackingprevention)
- [WebRtcLocalhostIpHandling](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtclocalhostiphandling)

<!-- end 86 -->

## Версия 85.0.564.41: 25 августа

Исправлены ошибки и проблемы с производительностью.

## Версия 85.0.564.40: 21 августа

Исправлены ошибки и проблемы с производительностью.

## Версия 85.0.564.36: 17 августа

Исправлены ошибки и проблемы с производительностью.

## Версия 85.0.564.30: 10 августа

Исправлены ошибки и проблемы с производительностью.

## Версия 85.0.564.23: 3 августа

Исправлены ошибки и проблемы с производительностью.

<!--- BEGIN 85 ---->
## Версия 85.0.564.18: 28 июля

### Обновления компонентов

- **Локальная синхронизация элементов "Избранное" и "Параметры"**. Теперь вы можете синхронизировать избранные элементы браузера и параметры между профилями Active Directory в собственной среде без необходимости синхронизации с облаком.

- **Поддержка групповой политики Microsoft Edge для комбинаций "доверенный веб-сайт + приложение" для запуска без запроса подтверждения.** Добавлена поддержка групповой политики, которая позволяет администраторам добавлять комбинации "доверенный веб-сайт + приложение", которые можно запускать без запроса подтверждения. Это позволяет администраторам настраивать комбинации доверенных протоколов и источников данных (например, Microsoft 365), чтобы конечные пользователи могли подавить запрос на подтверждение при переходе по URL-адресу, содержащему протокол приложения.

- **Инструмент "Маркер PDF"**. Это средство можно добавить на панель инструментов для PDF-файлов, чтобы легко выделять важный текст.

- **Доступен API доступа к хранилищу**. Этот API доступа к хранилищу позволяет получить доступ к основному хранилищу в стороннем контексте, когда пользователь продемонстрировал явное намерение разрешить хранилище, которое в противном случае блокируется текущей конфигурацией браузера. Дополнительные сведения см. в разделе [API доступа к хранилищу](https://www.chromestatus.com/feature/5612590694662144).

- **Для коллекций Microsoft Edge доступна опция "Отправить в OneNote"**. Все рады возможности отправлять информацию, собранную в Коллекциях, в OneNote, где можно добавить ее в более крупный проект и сотрудничать с другими! А еще важнее то, что в Microsoft Edge 85 вы можете отправлять контент в продукты *Office для Mac* (Word, Excel и OneNote) для учетной записи Майкрософт и Azure Active Directory.

- **обновления Средств разработчика**. Дополнительные сведения о перечисленных ниже обновлениях см. в статье [Новые возможности в Средствах разработчика (Microsoft Edge 85)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools).

   - Средства разработчика Microsoft Edge поддерживают эмуляцию Surface Duo. Средства разработчика Microsoft Edge могут эмулировать Surface Duo, что позволяет вам проверить, как будет выглядеть веб-контент на устройствах с двумя экранами. Для включения этого эксперимента в Средствах разработчика перейдите в "Режим устройства", нажав клавиши CTRL + SHIFT + M в Windows или Command + Shift + M в macOS, а затем в раскрывающемся списке устройства выберите Surface Duo.
   - Средства разработчика Microsoft Edge позволяют сопоставлять сочетания клавиш с VS Code. Средства разработчика Microsoft Edge поддерживают настройку сочетаний клавиш в Средствах разработчика для обеспечения соответствия вашему редактору/IDE. В Microsoft Edge 85 мы добавляем возможность сопоставлять сочетания клавиш Средств разработчика с VS Code. Это изменение позволит повысить эффективность работы между VS Code и Средствами разработчика.

### Обновления политик

#### Новые политики

Добавлено 13 политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [AutoLaunchProtocolsFromOrigins](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autolaunchprotocolsfromorigins) - Определение списка протоколов, с помощью которых можно запустить внешнее приложение из списка источников без обращения к пользователю.
- [AutoOpenAllowedForURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenallowedforurls) - URL-адреса, с которыми можно применять параметр AutoOpenFileTypes.
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes) - Список типов файлов, которые должны автоматически открываться после скачивания.
- [DefaultSearchProviderContextMenuAccessAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchprovidercontextmenuaccessallowed) - Разрешение доступа по умолчанию к поиску контекстного меню службы поиска.
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) — Разрешение сертификатов, подписанных с помощью SHA-1 при выдаче локальными якорями доверия.
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Отключение предупреждений о расширениях загружаемых файлов для определенных типов файлов в доменах.
- [IntensiveWakeUpThrottlingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#intensivewakeupthrottlingenabled) - Управление функцией IntensiveWakeUpThrottling.
- [NewTabPagePrerenderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageprerenderenabled) - Включение предварительной загрузки страницы новой вкладки для ускорения отрисовки.
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox) - Настройка интерфейса поля поиска на странице новой вкладки.
- [PasswordMonitorAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordmonitorallowed) - Разрешение отправки оповещений пользователям, если их пароли окажутся небезопасными.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled) - Разрешение использования перемещаемых копий для данных профиля Microsoft Edge.
- [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation) - Настройка каталога перемещаемого профиля.
- [TLSCipherSuiteDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tlsciphersuitedenylist) - Выбор наборов шифров TLS для отключения.

#### Устаревшие политики

- [EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload) - Разрешение загрузки действий домена из Microsoft.
- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) — повторное включение API веб-компонентов v0 до M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies)- Разрешение WebDriver переопределять несовместимые политики.

<!--- END ---->

## Версия 84.0.522.35: 9 июля

Исправлены ошибки и проблемы с производительностью.

## Версия 84.0.522.28: 26 июня

Исправлены ошибки и проблемы с производительностью.

## Версия 84.0.522.26: 24 июня

Исправлены ошибки и проблемы с производительностью.

## Версия 84.0.522.20: 15 июня

Исправлены ошибки и проблемы с производительностью.

## Версия 84.0.522.15: 8 июня

Исправлены ошибки и проблемы с производительностью.

## Версия 84.0.522.11: 2 июня

### Обновления компонентов

- Эта версия Microsoft Edge обеспечивает оптимизированное время скачивания списка сайтов для режима Internet Explorer.  Мы сократили задержку скачивания для списка сайтов в режиме Internet Explorer до 0 секунд (с 60-секундного ожидания) при отсутствии кэшированного списка сайтов. Мы также добавили поддержку групповой политики для случаев, когда требуется задержка перехода на домашнюю страницу режима Internet Explorer, пока скачивается список сайтов. Дополнительные сведения см. в политике [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload).

- Microsoft Edge теперь позволяет пользователям входить в браузер, если он "запущен от имени администратора" в Windows 10. Это помогает пользователям, использующим Microsoft Edge в Windows Server или в сценариях удаленного рабочего стола и песочницы.

- Microsoft Edge теперь обеспечивает полную поддержку мыши в полноэкранном режиме. Теперь с помощью мыши вы можете получить доступ к вкладкам, адресной строке и другим элементам, не выходя из полноэкранного режима.

- Улучшение покупок в Интернете. Добавляйте собственные псевдонимы для сохраненных дебетовых и кредитных карт. Теперь вы можете отличать свои кредитные карты при совершении покупок в Интернете. Присвоение псевдонима для дебетовой или кредитной карты позволяет выбрать правильную карту при использовании автозаполнения для выбора способа оплаты.

- Протоколы TLS/1.0 и TLS/1.1 отключены по умолчанию. Для обнаружения затронутых сайтов можно установить флаг *edge://flags/#display-legacy-tls-warnings*, чтобы Microsoft Edge выводил неблокирующее уведомление "Небезопасно" при загрузке страниц, требующих устаревшие протоколы TLS. Политика [SSLVersionMin](https://docs.microsoft.com/deployedge/microsoft-edge-policies#sslversionmin) позволяет повторно включить протокол TLS/1.0 и TLS/1.1. Эта политика будет доступна как минимум до Microsoft Edge версии 88. Дополнительные сведения см. в статье [Изменения, вносимые в Microsoft Edge, которые влияю на совместимость сайтов](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

- Улучшения коллекций:

  - Добавлена функция заметок, позволяющая добавлять заметку или комментарий к элементу коллекции. Заметки группируются вместе и остаются прикрепленными к элементу, даже если вы сортируете элементы в коллекции. Чтобы попробовать эту новую функцию, щелкните элемент правой кнопкой мыши и выберите "Добавить заметку".
  - Вы можете изменить цвет фона заметок в коллекциях. Цветовую кодировку можно использовать для упорядочения информации и повышения производительности.
  - Имеются заметные улучшения производительности, позволяющие экспортировать коллекции в Excel быстрее, чем в предыдущих версиях Microsoft Edge.

- Дополнительная поддержка API Microsoft Edge:

  - API доступа к хранилищу. Этот API позволяет получить доступ к основному хранилищу в стороннем контексте, когда пользователь демонстрирует явное намерение разрешить хранилище, которое в противном случае блокируется текущей конфигурацией браузера.

    По мере роста значимости конфиденциальности для пользователей все чаще возникают запросы на более строгие параметры браузера, используемые по умолчанию, и параметры согласия пользователей на использование, такие как блокировка доступа ко всем сторонним хранилищам. Хотя эти параметры улучшают конфиденциальность и блокируют нежелательный доступ неизвестными или недоверенными сторонами, они могут привести к нежелательным побочным эффектам, например к блокировке доступа к содержимому, которое хочет просмотреть пользователь (например, социальные сети и внедренный мультимедийный контент).

  - API собственной файловой системы, означающий, что вы можете предоставлять сайтам разрешения на изменение файлов или папок с помощью API собственной файловой системы.

- Улучшения PDF-файлов:

  - Чтение вслух для PDF-файлов позволяет пользователям прослушивать содержимое PDF при выполнении других важных задач. Это также помогает обучающимся, использующим аудиовизуальные материалы, сосредоточиться на чтении содержимого, облегчая процесс обучения.
  - Улучшено редактирование PDF-файлов. Теперь вы можете сохранить в файле изменения, внесенные в PDF, вместо сохранения копии при каждом изменении PDF-файла.

- Microsoft Edge теперь поддерживает перевод в иммерсивном средстве чтения. Когда пользователь открывает представление иммерсивного средства чтения, появляется возможность перевести страницу на нужный язык.

- Средства разработчика поддерживают настройку сочетаний клавиш для обеспечения соответствия вашему редактору/IDE, включая VS Code.

### Обновления политик

#### Новые политики

Добавлено пять новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [AppCacheForceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#appcacheforceenabled) — разрешает повторное включение компонента AppCache, даже если он отключен по умолчанию.
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy) — прокси-сервер контейнера Application Guard.
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload) — требование наличия списка сайтов в режиме предприятия перед навигацией по вкладкам.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled)— включить скрытие родной Windows.
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout) — установка времени ожидания для навигации по вкладкам списка сайтов в режиме предприятия.

#### Устаревшие политики

- [AllowSyncXHRInPageDismissal](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal) — разрешение страницам отправлять синхронные запросы XHR при удалении страницы.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) — определяет, используется ли встроенное средство проверки сертификатов для проверки сертификатов серверов.
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled) — включение более строгой обработки для смешанного контента.

#### Устаревшая политика

[ForceNetworkInProcess](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcenetworkinprocess) — принудительный запуск сетевого кода в процессе браузера.

<!-- end 84 -->

## Версия 83.0.478.44: 1 июня

Исправлены ошибки и проблемы с производительностью.

## Версия 83.0.478.37: 20 мая

Исправлены ошибки и проблемы с производительностью.

## Версия 83.0.478.33: 15 мая

Исправлены ошибки и проблемы с производительностью.

## Версия 83.0.478.28: 7 мая

Исправлены ошибки и проблемы с производительностью.

## Версия 83.0.478.25: 4 мая

Исправлены ошибки и проблемы с производительностью.

## Версия 83.0.478.18: 27 апреля

Исправлены ошибки и проблемы с производительностью.

## Версия 83.0.478.13: 22 апреля

### Обновления компонентов

- Усовершенствования фильтра SmartScreen в Microsoft Defender: реализован ряд улучшений службы фильтра SmartScreen в Microsoft Defender, включая улучшенную защиту от вредоносных сайтов с перенаправлением при загрузке и блокирование фреймов верхнего уровня, полностью заменяющее вредоносные сайты страницей безопасности фильтра SmartScreen в Microsoft Defender. Функция блокирования фрейма верхнего уровня запрещает воспроизведение звука и других данных мультимедиа с вредоносного сайта, за счет чего повышается удобство и снижается путаница.

- Пользователи теперь могут исключить некоторые файлы cookie из автоматического удаления при закрытии браузера. Эта возможность добавлена на основе отзывов пользователей. Этот вариант пригодится, если пользователи не хотят выходить с определенного сайта, но при этом хотят удалить все остальные файлы cookie при закрытии браузера. Чтобы использовать эту функцию, перейдите по адресу *edge://settings/clearBrowsingDataOnClose* и включите переключатель "Файлы cookie и другие данные сайтов".

- Теперь доступна функция автоматического переключения профилей для более удобного доступа к рабочему содержимому. Если на работе вы используете несколько профилей, можно проверить работу этой функции: достаточно зайти с личным профилем на сайт, на котором требуется проверка подлинности с рабочей или учебной учетной записью. Когда мы обнаружим изменение, вы получите предложение переключиться на рабочий профиль, чтобы получить доступ к сайту, не проходя проверку подлинности. Когда вы выберете рабочий профиль, на который нужно переключиться, веб-сайт откроется в вашем рабочем профиле. Надеемся, что такой подход поможет вам отделить рабочие данные от личных и удобнее получать доступ к рабочему содержимому. Если вы не хотите, чтобы эта функция предлагала вам переключить профиль, можно выбрать "Больше не спрашивать", тогда эти запросы не будут отображаться.

- Улучшения функции коллекций:
  - Можно перетаскивать элементы в коллекцию, не открывая ее. При перетаскивании можно выбрать место в списке коллекции, в которое нужно поместить элемент.
  - Можно добавлять сразу несколько элементов в коллекцию, а не только по одному. Чтобы добавить несколько элементов, выделите их и перетащите в коллекцию. Также можно выделить элементы, щелкнуть их правой кнопкой мыши и выбрать коллекцию, в которую нужно их поместить.

- Можно добавить все вкладки в окне Edge в коллекцию без необходимости добавлять их по отдельности. Чтобы добавить все вкладки, щелкните любую вкладку правой кнопкой мыши и выберите "Добавить все вкладки в новую коллекцию".

- Теперь доступна синхронизация расширений. Можно синхронизировать расширения на всех устройствах. С Microsoft Edge синхронизируются расширения из Microsoft Store и Chrome Store. Чтобы использовать эту функцию, щелкните многоточие (**…**) в строке меню и выберите **Параметры**. Щелкните **Синхронизация** в вашем профиле, чтобы открыть варианты синхронизации. Используйте переключатель в разделе **Профили/Синхронизация**, чтобы включить расширения. Можно отключить синхронизацию расширений с помощью групповой политики [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled).

- Улучшено сообщение на странице управления загрузкой для заблокированных небезопасных загруженных файлов.

- Усовершенствования иммерсивного средства чтения:
  - добавлена поддержка наречий в инструменте иммерсивного средства чтения "Части речи". При чтении статьи с помощью иммерсивного средства чтения откройте средства проверки правописания и выберите наречия в разделе "Части речи", чтобы выделить все наречия на странице.
  - Добавлена возможность выбрать любое содержимое на веб-странице и открыть его в иммерсивном средстве чтения. Эта возможность позволяет пользователям использовать иммерсивное средство чтения, а также все средства обучения, такие как "Выделение строк" и "Прочесть вслух", на всех веб-сайтах.

- Неправильно введенный пользователями URL-адрес поможет исправить средство для исправления ссылок, которое корректирует узел и поисковый запрос. Например: <br>
Пользователь по ошибке вводит "powerbi" как "powerbbi".com. Средство для исправления ссылок предложит вариант "powerbi".com в качестве откорректированного варианта и создаст ссылку на поиск "powerbbi" на случай, если пользователь ищет что-то другое.

- Разрешите пользователям сохранять свое решение о запуске внешний протокол для определенного сайта. Чтобы включить или отключить эту функцию, пользователи могут настроить политику [ExternalProtocolDialogShowAlwaysOpenCheckbox]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox).

- Microsoft Edge можно задать в качестве браузера по умолчанию непосредственно в **параметрах** Microsoft Edge. Эта возможность упрощает для пользователей изменение браузера, используемого по умолчанию,— можно сделать это из самого браузера вместо того, чтобы искать эту возможность в параметрах операционной системы. Чтобы использовать эту функцию, перейдите на *edge://settings/defaultBrowser* и нажмите **Сделать браузером по умолчанию**.

- Несколько обновлений средств разработчика, в том числе новая удаленная поддержка отладки, улучшения пользовательского интерфейса и многое другое. Дополнительные сведения см. в статье [Новые возможности средств разработчика (Microsoft Edge 83)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

### Обновления политик

#### Новые политики

Добавлено 15 новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [AllowSurfGame](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsurfgame) — разрешить игру "Серфинг".
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls) — настроить список сайтов, для которых Microsoft Edge попытается установить привязку токена.
- [BingAdsSuppression](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#bingadssuppression) — блокировать всю рекламу в результатах поиска Bing.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) — определяет, используется ли встроенное средство проверки сертификатов для проверки сертификатов серверов.
- [ClearCachedImagesAndFilesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearcachedimagesandfilesonexit) — очистка кэшированных изображений и файлов при закрытии Microsoft Edge.
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare) — настройка возможностей общего доступа.
- [DeleteDataOnMigration](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#deletedataonmigration) — удаление данных старого браузера при миграции.
- [DnsOverHttpsMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsoverhttpsmode) — управление режимом DNS по протоколу HTTPS.
- [DnsOverHttpsTemplates](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsoverhttpstemplates) — настройка шаблона URI нужного сопоставителя DNS по протоколу HTTPS.
- [FamilySafetySettingsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#familysafetysettingsenabled) — разрешить пользователям настраивать семейную безопасность.
- [LocalProvidersEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#localprovidersenabled) — разрешить варианты поиска локальных поставщиков.
- [ScrollToTextFragmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#scrolltotextfragmentenabled) — разрешить прокрутку до текста, указанного во фрагментах URL-адресов.
- [ScreenCaptureAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#screencaptureallowed) — разрешить или запретить создание снимков экрана.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) — настройка списка типов, исключенных из синхронизации.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled)— включить скрытие родной Windows.

#### Политика устарела

Следующая политика продолжит работать в этом выпуске. Она станет устаревшей в будущем выпуске.

[EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload) — включение скачивания действий с доменами в Майкрософт

<!--  end 83 -->

## Версия 81.0.416.60: 20 апреля

Исправлены ошибки и проблемы с производительностью.

## Версия 81.0.416.58: 17 апреля

Обновления для системы безопасности

## Версия 81.0.416.50: 10 апреля

Исправлены ошибки и проблемы с производительностью.

## Версия 81.0.416.45: 3 апреля

Исправлены ошибки и проблемы с производительностью.

## Версия 81.0.416.41: 30 марта

Исправлены ошибки и проблемы с производительностью.

## Версия 81.0.416.34: 17 марта

Исправлены ошибки и проблемы с производительностью.

## Версия 81.0.416.31: 12 марта

Исправлены ошибки и проблемы с производительностью.

## Версия 81.0.416.28: 9 марта

Исправлены ошибки и проблемы с производительностью.

## Версия 81.0.416.20: 28 февраля

Исправлены ошибки и проблемы с производительностью.

## Версия 81.0.416.12: 20 февраля

### Обновления компонентов

- Стали доступны коллекции. Чтобы начать работу, щелкните значок "Коллекции" рядом с адресной строкой. Откроется область "Коллекции", где можно создавать, редактировать и просматривать коллекции. Мы создали Коллекции на основе ваших действий в Интернете. Если вы покупатель, путешественник, преподаватель или учащийся, Коллекции помогут вам. [Подробнее](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Разрешение удаления (скрытие с панели инструментов) кнопки "Коллекции" с панели инструментов Microsoft Edge для согласованности.

- Автоматический вход локальной учетной записи Active Directory будет использоваться только для организаций, включивших его. Если пользователи уже выполнили вход с помощью локальной учетной записи AD, им будет доступна возможность выхода из нее. Теперь пользователи будут автоматически входить только с помощью основной учетной записи своей операционной системы, если это учетная запись Майкрософт или Azure Active Directory. Администраторы могут включить автоматический вход с использованием локальной учетной записи AD с помощью политики ConfigureOnPremisesAccountAutoSignIn.

- Application Guard. Поддержка расширений теперь доступна в контейнере.

- Добавлено сообщение для пользователей о том, что Internet Explorer не установлен, когда они переходят на страницу, настроенную для открытия в режиме Internet Explorer.

- В средствах разработчика Microsoft Edge обновлен инструмент трехмерного представления с добавлением новой функции для отладки контекста стопки z-index. Трехмерное представление демонстрирует глубину модели DOM с помощью цвета и стопки, а представление z-Index помогает изолировать разные контексты стопки страницы. [Подробнее](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/).

- Локализованы средства разработчика F12 на 10 новых языках, и теперь они будут соответствовать языку, используемому в браузере. [Подробнее](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/).

- Добавлена поддержка воспроизведения Dolby Vision. В Windows 10 сборки 17134 (обновление за апрель 2018 г.) с поддержкой Dolby Vision веб-сайты могут отображать контент Dolby Vision. Узнайте, как включить контент Dolby Vision в [Netflix](https://help.netflix.com/en/node/42384).

- Microsoft Edge теперь может определять и удалять дубликаты избранного, а также объединять папки с одинаковыми именами. Чтобы получить доступ к инструменту, щелкните звезду на панели инструментов браузера и выберите "Удалить дубликаты избранного".  Вы сможете подтвердить изменения, и все обновления в папке "Избранное" будут синхронизированы на других устройствах.

- Пользователи сообщили нам, что сложно отличить обычное окно браузера в темном режиме от окна InPrivate, так как для обоих окон используется темное обрамление. Новый сплошной синий значок InPrivate в правом верхнем углу помогает пользователям убедиться в использовании режима InPrivate.

- Открытие внешних ссылок в правильном профиле браузера. Выберите профиль по умолчанию для ссылок, открываемых во внешних приложениях, на странице *edge://settings/multiProfileSettings*.

- Добавлено предупреждение для пользователей, входящих в профиль браузера с учетной записью после ранее выполненного входа с помощью другой учетной записи. Это помогает предотвратить непреднамеренное объединение данных.

- Если вы сохранили карты оплаты в своей учетной записи Майкрософт, их можно использовать в Microsoft Edge при заполнении форм платежей. Карты из вашей учетной записи Майкрософт будут синхронизированы на других компьютерах, а все сведения будут предоставляться веб-сайту после двухфакторной проверки подлинности (код CVC и ваше удостоверение Майкрософт). Для дополнительного удобства вы можете безопасно сохранить копию карты на устройстве во время проверки подлинности.

- Выделение строк предназначено для пользователей, которые хотят сосредоточиться на ограниченной части содержимого при чтении. Эта функция позволяет пользователям сосредоточиться на 1, 3 или 5 строках и затемняет остальную страницу, чтобы не отвлекать пользователей при чтении.  Пользователи могут прокручивать страницы с помощью касания или клавиш со стрелками, и фокус смещается соответствующим образом.

- Браузер Microsoft Edge теперь интегрирован с Windows Speller на платформах Windows 8.1 и более поздних версий. Эта интеграция обеспечивает дополнительную языковую поддержку с доступом к словарям дополнительных языков и возможностью использования настраиваемых словарей Windows. От пользователей не требуются дополнительные действия при добавлении языка в языковых параметрах ОС, а переключатель проверки правописания включен в параметрах Microsoft Edge.

- Когда PDF-документы открываются в Microsoft Edge, пользователи могут создавать выделение, изменять цвет и удалять выделение. Это помогает в дальнейшем ссылаться на важные части документа при совместной работе.

- При загрузке длинных PDF-документов, оптимизированных для Интернета, просматриваемые пользователем страницы загружаются быстрее, одновременно с загрузкой остального документа.

- Стало проще запустить средство иммерсивного чтения для веб-сайта с помощью клавиши F9.

- Стало проще запустить функцию "Прочесть вслух" с помощью сочетания клавиш (CTRL+SHIFT+U).

### Обновления политик

#### Новые политики

Добавлено 12 новых политик Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled) — включение внешней проверки подлинности для InPrivate и гостевых профилей. 
- [AudioSandboxEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#audiosandboxenabled) — разрешение запускать Audio Sandbox.
- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy) — использование политики источника ссылки no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#globallyscopehttpauthcacheenabled) — включение глобального кэша HTTP-авторизации.
- [ImportExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importextensions) — разрешение импорта расширений.
- [ImportCookies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importcookies) — разрешение импорта файлов cookie.
- [ImportShortcuts](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importshortcuts) — разрешение импорта ярлыков.
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect) — указание, как будут действовать переходы в пределах страницы на ненастроенные сайты, начинаемые со страниц в режиме Internet Explorer.
- [OmniboxMSBProviderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#omniboxmsbproviderenabled) — включение поставщика Поиска (Майкрософт) для бизнеса в омнибоксе. 
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled) — включение более строгой обработки для смешанного контента.
- [TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled) — включение функции безопасности TLS 1.3 для местных якорей доверия.
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin) — настройка автоматического входа с помощью учетной записи домена Active Directory при отсутствии учетной записи домена Azure AD.

#### Устаревшие политики

В этом выпуске продолжают действовать следующие политики. Они станут устаревшими в будущем выпуске.

- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) — повторное включение API веб-компонентов v0 до M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) — разрешение WebDriver переопределять несовместимые политики.

## См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
