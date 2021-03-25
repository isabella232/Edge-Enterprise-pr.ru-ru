---
title: Архивные заметки о выпуске для канала Microsoft Edge Stable
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 03/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Архивные заметки о выпуске для канала Microsoft Edge Stable
ms.openlocfilehash: b12d8c34e2936b7f1c8dbc0573672273a74beabc
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448013"
---
# <a name="archived-release-notes-for-microsoft-edge-stable-channel"></a>Архивные заметки о выпуске для канала Microsoft Edge Stable

Эти заметки о выпуске содержат сведения о новых компонентах и не связанных с безопасностью обновлениях, которые включены в канал Microsoft Edge Stable. Список обновлений системы безопасности находится [здесь](microsoft-edge-relnotes-security.md).

## <a name="version-86062238-october-9"></a>Версия 86.0.622.38: 9 октября

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#october-9-2020)

### <a name="feature-updates"></a>Обновления компонентов

* **Откат к предыдущей версии Microsoft Edge.** Функция отката позволяет администраторам вернуть известную хорошую версию Microsoft Edge, если у вас возникла проблема с последней версией Microsoft Edge. **Примечание.** Стабильная версия 86.0.622.38 — это первая версия, к которой можно выполнить откат. Это означает, что стабильная версия 87 — это первая версия, с которой можно выполнить откат. [Подробнее](edge-learnmore-rollback.md).

* **Принудительное включение синхронизации по умолчанию в организации.**  Администраторы могут включить синхронизацию учетных записей Azure Active Directory (Azure AD) по умолчанию с помощью политики [ForceSync](./microsoft-edge-policies.md#forcesync).

* **Автоматическое переключение профилей в Windows 7 и 8.1.** Автоматическое переключение профилей, в настоящее время доступное в Microsoft Edge в Windows 10, теперь расширено и на более ранние версии Windows (Windows 7 и 8.1). Дополнительные сведения см. в записи блога об [автоматическом переключении профилей](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **Параметр файлов cookie, используемый по умолчанию: SameSite=Lax**. Чтобы повысить безопасность и конфиденциальность в Интернете, по умолчанию файлы cookie будут обрабатываться с использованием параметра [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite). Это означает, что файлы cookie будут отправляться только в основном контексте и будут пропущены в запросах, отправляемых третьим сторонам. Это изменение может повлиять на совместимость для веб-сайтов, которым требуются файлы cookie для правильной работы сторонних ресурсов. Чтобы разрешить такие файлы cookie, веб-разработчики могут помечать файлы cookie, которые должны настраиваться и отправляться в сторонних контекстах, добавив явные атрибуты `SameSite=none` и `Secure` при настройке файлов cookie. Организации, которые хотят исключить определенные сайты из этого изменения, могут сделать это с помощью политики [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) или отказаться от изменения на всех сайтах с помощью политики [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled).

* **Удаление API кэша приложений HTML5.**  С Microsoft Edge версии 86 устаревший API кэша приложений, позволяющий использовать веб-страницы в автономном режиме, удаляется из Microsoft Edge. Сведения для веб-разработчиков о замене API кэша приложений на служебные сценарии доступны в [документации для веб-разработчиков](https://web.dev/appcache-removal/).  Важно! Вы можете запросить [маркер AppCache OriginTrial](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673), позволяющий сайтам продолжать использовать устаревший API кэша приложений до Microsoft Edge версии 90.

* **Конфиденциальность и безопасность.**

  * Замена политик [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) и [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) для более ранних версий Windows и macOS. Эти политики не рекомендуются в Microsoft Edge версии 86 и станут устаревшими в Microsoft Edge версии 89.<br>
Эти политики заменяются политикой [Разрешить телеметрию](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) в Windows 10 и новой политикой [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) для всех остальных платформ. Это позволит пользователям управлять диагностическими данными, отправляемыми в корпорацию Майкрософт, для Windows 7, 8, 8.1 и macOS.
  * Поддержка безопасной службы DNS (DNS поверх HTTPS).  С Microsoft Edge версии 86 доступны параметры для управления безопасной службой DNS на неуправляемых устройствах. Эти параметры недоступны пользователям управляемых устройств, но ИТ-администраторы могут включать и отключать безопасную службу DNS с помощью групповой политики [dnsoverhttpsmode](./microsoft-edge-policies.md#dnsoverhttpsmode).

* **Режим Internet Explorer:** Позвольте пользователям применять пользовательский интерфейс Microsoft Edge для проверки сайтов в режиме Internet Explorer. С Microsoft Edge версии 86 администраторы могут включить параметр пользовательского интерфейса, чтобы пользователи могли загружать вкладки в режиме Internet Explorer для тестирования или в качестве временной меры до того, как сайты будут добавлены в XML-файл списка сайтов.

* **Обновления PDF:**

  * Оглавление для PDF-документов. С версии 86 в Microsoft Edge добавлена поддержка оглавления, которое позволяет пользователям легко перемещаться по PDF-документам.
  * Доступ ко всем возможностям PDF на экранах небольшого форм-фактора. Получите доступ ко всем возможностям средства чтения PDF-файлов Microsoft Edge на устройствах с небольшим размером экрана.
  * Поддержка пера в качестве маркера в PDF-файлах. Благодаря этому обновлению пользователи могут использовать собственное цифровое перо для прямого выделения текста в PDF-файлах по аналогии с обычным маркером на листе бумаги.
  * Улучшена прокрутка PDF-документов. Теперь вы сможете наслаждаться прокруткой без запинок при просмотре длинных PDF-документов.

* **Пользователям предлагаются варианты автозаполнения при вводе поискового запроса на веб-сайте надстроек Microsoft Edge.** Автозаполнение помогает пользователям быстро завершать поисковые запросы без необходимости ввода всей строки. Это удобно, так как пользователям не нужно запоминать правильное написание и они могут выбирать из доступных демонстрируемых вариантов.

* **Добавление настраиваемого изображения на страницу новой вкладки (NTP) с помощью групповой политики.** С Microsoft Edge версии 86 на странице новой вкладки доступна возможность для замены стандартного изображения на настраиваемое изображение, предоставляемое пользователем. Возможность управления свойствами этого изображения также поддерживается групповой политикой.

* **Сопоставление настроенных сочетаний клавиш с VS Code.** Средства разработчика Microsoft Edge теперь поддерживают настройку сочетаний клавиш в средствах разработчика для обеспечения соответствия вашему редактору/IDE. (В Microsoft Edge 84 мы добавили возможность сопоставлять сочетания клавиш средств разработчика с VS Code.)

* **Удаление загрузки с диска с помощью диспетчера загрузок.** Пользователи теперь могут удалять загруженные файлы с диска, не выходя из браузера. Новая функция удаления загрузок находится в контекстном меню панели загрузок или на странице загрузок.

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлены двадцать три новые политики. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [CollectionsServicesAndExportsBlockList](./microsoft-edge-policies.md#collectionsservicesandexportsblocklist) — блокировка доступа к указанному списку служб и целевым объектам экспорта в Коллекциях.
- [DefaultFileSystemReadGuardSetting](./microsoft-edge-policies.md#defaultfilesystemreadguardsetting) — управлять использованием API файловой системы для чтения.
- [DefaultFileSystemWriteGuardSetting](./microsoft-edge-policies.md#defaultfilesystemwriteguardsetting) — управлять использованием API файловой системы для записи.
- [DefaultSensorsSetting](./microsoft-edge-policies.md#defaultsensorssetting) — стандартный параметр для датчиков.
- [DefaultSerialGuardSetting](./microsoft-edge-policies.md#defaultserialguardsetting) — управлять использованием API Serial.
- [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) — отправлять обязательные и необязательные диагностические данных об использовании браузера.
- [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) — разрешить доступ к средству Enterprise Mode Site List Manager.
- [FileSystemReadAskForUrls](./microsoft-edge-policies.md#filesystemreadaskforurls) — разрешить доступ на чтение через API файловой системы на этих сайтах.
- [FileSystemReadBlockedForUrls](./microsoft-edge-policies.md#filesystemreadblockedforurls) — заблокировать доступ на чтение через API файловой системы на этих сайтах.
- [FileSystemWriteAskForUrls](./microsoft-edge-policies.md#filesystemwriteaskforurls) — Разрешить доступ на запись к файлам и каталогам на этих сайтах.
- [FileSystemWriteBlockedForUrls](./microsoft-edge-policies.md#filesystemwriteblockedforurls) — Заблокировать доступ на запись к файлам и каталогам на этих сайтах.
- [ForceSync](./microsoft-edge-policies.md#forcesync) — принудительно синхронизировать данные браузера и не показывать запрос на разрешение синхронизации.
- [InsecureFormsWarningsEnabled](./microsoft-edge-policies.md#insecureformswarningsenabled) — включить предупреждения для небезопасных форм.
- [InternetExplorerIntegrationTestingAllowed](./microsoft-edge-policies.md#internetexplorerintegrationtestingallowed) — разрешить тестирование режима Internet Explorer.
- [SpotlightExperiencesAndRecommendationsEnabled](./microsoft-edge-policies.md#spotlightexperiencesandrecommendationsenabled) — выберите, могут ли пользователи получать настроенные фоновые изображения и текст, предложения, уведомления и советы для служб Майкрософт.
- [NewTabPageAllowedBackgroundTypes](./microsoft-edge-policies.md#newtabpageallowedbackgroundtypes) — настройка типов фона, разрешенных для макета страницы новой вкладки.
- [SaveCookiesOnExit](./microsoft-edge-policies.md#savecookiesonexit) — сохранять файлы cookie при закрытии Microsoft Edge.
- [SensorsAllowedForUrls](./microsoft-edge-policies.md#sensorsallowedforurls) — разрешить доступ к датчиками на определенных сайтах.
- [SensorsBlockedForUrls](./microsoft-edge-policies.md#sensorsblockedforurls) — блокировать доступ к датчиками на определенных сайтах.
- [SerialAskForUrls](./microsoft-edge-policies.md#serialaskforurls) — разрешить API Serial на определенных сайтах.
- [SerialBlockedForUrls](./microsoft-edge-policies.md#serialblockedforurls) — блокировать API Serial на определенных сайтах.
- [UserAgentClientHintsEnabled](./microsoft-edge-policies.md#useragentclienthintsenabled) — включение функции клиентских подсказок User-Agent.
- [UserDataSnapshotRetentionLimit](./microsoft-edge-policies.md#userdatasnapshotretentionlimit) — ограничение количества снимков пользовательских данных, сохраняемых для применения в случае аварийного отката.

#### <a name="deprecated-policies"></a>Устаревшие политики

- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) — включить отчеты с данными об использовании и сбоях.
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) — отправка сведений о сайтах для улучшения служб Майкрософт.

#### <a name="obsoleted-policy"></a>Устаревшая политика

[TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) — включение функции безопасности TLS 1.3 для местных якорей доверия.

## <a name="version-85056470-october-6"></a>Версия 85.0.564.70: 6 октября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-85056468-october-1"></a>Версия 85.0.564.68: 1 октября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-85056463-september-23"></a>Версия 85.0.564.63: 23 сентября

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#september-23-2020)

## <a name="version-85056451-september-9"></a>Версия 85.0.564.51: 9 сентября

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#september-9-2020)

## <a name="version-85056444-august-31"></a>Версия 85.0.564.44: 31 августа

Исправлены ошибки и проблемы с производительностью.

<!-- 85.0.564.41: August 27 -->

## <a name="version-85056441-august-27"></a>Версия 85.0.564.41: 27 августа

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#august-27-2020)

### <a name="feature-updates"></a>Обновления компонентов

- **Локальная синхронизация элементов "Избранное" и "Параметры"**. Теперь вы можете синхронизировать избранные элементы браузера и параметры между профилями Active Directory в собственной среде без необходимости синхронизации с облаком.

- **Поддержка групповой политики Microsoft Edge для комбинаций "доверенный веб-сайт + приложение" для запуска без запроса подтверждения**. Добавлена поддержка групповой политики, которая позволяет администраторам добавлять комбинации "доверенный веб-сайт + приложение", которые можно запускать без запроса подтверждения. Это позволяет администраторам настраивать комбинации доверенных протоколов и источников данных (например, Microsoft 365), чтобы конечные пользователи могли подавить запрос на подтверждение при переходе по URL-адресу, содержащему протокол приложения.

- **Инструмент "Маркер PDF"**. Это средство можно добавить на панель инструментов для PDF-файлов, чтобы легко выделять важный текст.

- **Доступен API доступа к хранилищу**. Этот API доступа к хранилищу позволяет получить доступ к основному хранилищу в стороннем контексте, когда пользователь продемонстрировал явное намерение разрешить хранилище, которое в противном случае блокируется текущей конфигурацией браузера. Дополнительные сведения см. в разделе [API доступа к хранилищу](https://www.chromestatus.com/feature/5612590694662144).

- **Для коллекций Microsoft Edge доступна опция "Отправить в OneNote"**. Все рады возможности отправлять информацию, собранную в Коллекциях, в OneNote, где можно добавить ее в более крупный проект и сотрудничать с другими! А еще важнее то, что в Microsoft Edge 85 вы можете отправлять контент в продукты *Office для Mac* (Word, Excel и OneNote) для учетной записи Майкрософт и Azure Active Directory.

- **обновления Средств разработчика**. Дополнительные сведения о перечисленных ниже обновлениях см. в статье [Новые возможности в Средствах разработчика (Microsoft Edge 85)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools).

   - Средства разработчика Microsoft Edge поддерживают эмуляцию Surface Duo. Средства разработчика Microsoft Edge могут эмулировать Surface Duo, что позволяет вам проверить, как будет выглядеть веб-контент на устройствах с двумя экранами. Для включения этого эксперимента в Средствах разработчика перейдите в "Режим устройства", нажав клавиши CTRL + SHIFT + M в Windows или Command + Shift + M в macOS, а затем в раскрывающемся списке устройства выберите Surface Duo.
   - Средства разработчика Microsoft Edge позволяют сопоставлять сочетания клавиш с VS Code. Средства разработчика Microsoft Edge поддерживают настройку сочетаний клавиш в Средствах разработчика для обеспечения соответствия вашему редактору/IDE. В Microsoft Edge 85 мы добавляем возможность сопоставлять сочетания клавиш Средств разработчика с VS Code. Это изменение позволит повысить эффективность работы между VS Code и Средствами разработчика.

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено 13 политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [AutoLaunchProtocolsFromOrigins](./microsoft-edge-policies.md#autolaunchprotocolsfromorigins) - Определение списка протоколов, с помощью которых можно запустить внешнее приложение из списка источников без обращения к пользователю.
- [AutoOpenAllowedForURLs](./microsoft-edge-policies.md#autoopenallowedforurls) - URL-адреса, с которыми можно применять параметр AutoOpenFileTypes.
- [AutoOpenFileTypes](./microsoft-edge-policies.md#autoopenfiletypes) - Список типов файлов, которые должны автоматически открываться после скачивания.
- [DefaultSearchProviderContextMenuAccessAllowed](./microsoft-edge-policies.md#defaultsearchprovidercontextmenuaccessallowed) - Разрешение доступа по умолчанию к поиску контекстного меню службы поиска.
- [EnableSha1ForLocalAnchors](./microsoft-edge-policies.md#enablesha1forlocalanchors) — Разрешение сертификатов, подписанных с помощью SHA-1 при выдаче локальными якорями доверия.
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](./microsoft-edge-policies.md#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Отключение предупреждений о расширениях загружаемых файлов для определенных типов файлов в доменах.
- [IntensiveWakeUpThrottlingEnabled](./microsoft-edge-policies.md#intensivewakeupthrottlingenabled) - Управление функцией IntensiveWakeUpThrottling.
- [NewTabPagePrerenderEnabled](./microsoft-edge-policies.md#newtabpageprerenderenabled) - Включение предварительной загрузки страницы новой вкладки для ускорения отрисовки.
- [NewTabPageSearchBox](./microsoft-edge-policies.md#newtabpagesearchbox) - Настройка интерфейса поля поиска на странице новой вкладки.
- [PasswordMonitorAllowed](./microsoft-edge-policies.md#passwordmonitorallowed) - Разрешение отправки оповещений пользователям, если их пароли окажутся небезопасными.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled) - Разрешение использования перемещаемых копий для данных профиля Microsoft Edge.
- [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation) - Настройка каталога перемещаемого профиля.
- [TLSCsipherSuiteDenyList](./microsoft-edge-policies.md#tlsciphersuitedenylist) — выбор наборов шифров TLS для отключения.

#### <a name="obsoleted-policies"></a>Устаревшие политики

- [EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) - Разрешение загрузки действий домена из Microsoft.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) — повторное включение API веб-компонентов v0 до M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies)- Разрешение WebDriver переопределять несовместимые политики.

## <a name="version-84052263-august-20"></a>Версия 84.0.522.63: 20 августа

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#august-20-2020).

## <a name="version-84052261-august-17"></a>Версия 84.0.522.61: 17 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-84052259-august-11"></a>Версия 84.0.522.59: 11 августа

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#august-11-2020)

## <a name="version-84052258-august-10"></a>Версия 84.0.522.58: 10 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-84052252-august-1"></a>Версия 84.0.522.52: 1 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-84052250-july-31"></a>Версия 84.0.522.50: 31 июля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-84052249-july-29"></a>Версия 84.0.522.49: 29 июля

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#july-29-2020)

## <a name="version-84052248-july-28"></a>Версия 84.0.522.48: 28 июля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-84052244-july-23"></a>Версия 84.0.522.44: 23 июля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-84052240-july-16"></a>Версия 84.0.522.40: 16 июля

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#july-16-2020)

### <a name="feature-updates"></a>Обновления компонентов

- Эта версия Microsoft Edge обеспечивает оптимизированное время скачивания списка сайтов для режима Internet Explorer. Мы сократили задержку скачивания для списка сайтов в режиме Internet Explorer до 0 секунд (с 60-секундного ожидания) при отсутствии кэшированного списка сайтов. Мы также добавили поддержку групповой политики для случаев, когда требуется задержка перехода на домашнюю страницу режима Internet Explorer, пока скачивается список сайтов. Дополнительные сведения см. в политике [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload).

- Microsoft Edge теперь позволяет пользователям входить в браузер, если он "запущен от имени администратора" в Windows 10. Это помогает пользователям, использующим Microsoft Edge в Windows Server или в сценариях удаленного рабочего стола и песочницы.

- Microsoft Edge теперь обеспечивает полную поддержку мыши в полноэкранном режиме. Теперь с помощью мыши вы можете получить доступ к вкладкам, адресной строке и другим элементам, не выходя из полноэкранного режима.

- Улучшение покупок в Интернете. Добавляйте собственные псевдонимы для сохраненных дебетовых и кредитных карт. Теперь вы можете отличать свои кредитные карты при совершении покупок в Интернете. Присвоение псевдонима для дебетовой или кредитной карты позволяет выбрать правильную карту при использовании автозаполнения для выбора способа оплаты.

- Протоколы TLS/1.0 и TLS/1.1 отключены по умолчанию.  Политика [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin) позволяет повторно включить протокол TLS/1.0 и TLS/1.1. Эта политика будет доступна как минимум до Microsoft Edge версии 88. Дополнительные сведения см. в статье [Изменения, вносимые в Microsoft Edge, которые влияю на совместимость сайтов](/microsoft-edge/web-platform/site-impacting-changes).

- Улучшения коллекций:

  - Добавлена функция заметок, позволяющая добавлять заметку или комментарий к элементу коллекции. Заметки группируются вместе и остаются прикрепленными к элементу, даже если вы сортируете элементы в коллекции. Чтобы попробовать эту новую функцию, щелкните элемент правой кнопкой мыши и выберите "Добавить заметку".
  - Вы можете изменить цвет фона заметок в коллекциях. Цветовую кодировку можно использовать для упорядочения информации и повышения производительности.
  - Имеются заметные улучшения производительности, позволяющие экспортировать коллекции в Excel быстрее, чем в предыдущих версиях Microsoft Edge.

- Дополнительная поддержка API Microsoft Edge:

  - Для экспериментов включен API доступа к хранилищу. Эта функция включена для домашних и корпоративных пользователей путем присвоения политике [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol) значения "Full". Эта функция будет включена по умолчанию для всех пользователей стабильного канала Microsoft Edge версии 85.
  
    По мере роста значимости конфиденциальности для пользователей все чаще возникают запросы на более строгие параметры браузера, используемые по умолчанию, и параметры согласия пользователей на использование, такие как блокировка доступа ко всем сторонним хранилищам. Хотя эти параметры улучшают конфиденциальность и блокируют нежелательный доступ неизвестными или недоверенными сторонами, они могут привести к нежелательным побочным эффектам, например к блокировке доступа к содержимому, которое хочет просмотреть пользователь (например, социальные сети и внедренный мультимедийный контент).

    API доступа к хранилищу позволяет получить доступ к основному хранилищу в стороннем контексте, когда пользователь демонстрирует явное намерение разрешить хранилище, которое в противном случае блокируется текущей конфигурацией браузера. Дополнительные сведения см. в разделе [API доступа к хранилищу](https://www.chromestatus.com/feature/5612590694662144).

  - API собственной файловой системы, означающий, что вы можете предоставлять сайтам разрешения на изменение файлов или папок с помощью API собственной файловой системы.

- Улучшения PDF-файлов:

  - Чтение вслух для PDF-файлов позволяет пользователям прослушивать содержимое PDF при выполнении других важных задач. Это также помогает обучающимся, использующим аудиовизуальные материалы, сосредоточиться на чтении содержимого, облегчая процесс обучения.
  - Улучшено редактирование PDF-файлов. Теперь вы можете сохранить в файле изменения, внесенные в PDF, вместо сохранения копии при каждом изменении PDF-файла.

- Microsoft Edge теперь поддерживает перевод в иммерсивном средстве чтения. Когда пользователь открывает представление иммерсивного средства чтения, появляется возможность перевести страницу на нужный язык.

- Несколько обновлений средств разработчика, включая поддержку настройки сочетаний клавиш в соответствии с VS Code и просмотр средств разработчика в высокой контрастности.  Дополнительные сведения см. в статье [Новые возможности средств разработчика (Microsoft Edge 84)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/05/devtools).

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено семь новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [AppCacheForceEnabled](./microsoft-edge-policies.md#appcacheforceenabled) — разрешает повторное включение компонента AppCache, даже если он отключен по умолчанию.
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy) — настройка параметров прокси-сервера контейнера Application Guard.
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) — требование наличия списка сайтов в режиме предприятия перед навигацией по вкладкам.
- [WinHttpProxyResolverEnabled](./microsoft-edge-policies.md#winhttpproxyresolverenabled) — использование сопоставителя прокси-сервера Windows.
- [InternetExplorerIntegrationEnhancedHangDetection](./microsoft-edge-policies.md#internetexplorerintegrationenhancedhangdetection) — настройка расширенного обнаружения зависаний в режиме Internet Explorer.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled)— чтобы снизить энергопотребление и нагрузку на процессор, Microsoft Edge определяет, когда окно закрыто другими окнами, и приостанавливает работу рисования пикселей.
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout) — установка времени ожидания для навигации по вкладкам списка сайтов в режиме предприятия.

#### <a name="deprecated-policies"></a>Устаревшие политики

- [AllowSyncXHRInPageDismissal](./microsoft-edge-policies.md#allowsyncxhrinpagedismissal) — разрешение страницам отправлять синхронные запросы XHR при удалении страницы.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) — определяет, используется ли встроенное средство проверки сертификатов для проверки сертификатов серверов.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) — включение более строгой обработки для смешанного контента.

#### <a name="obsoleted-policy"></a>Устаревшая политика

[ForceNetworkInProcess](./microsoft-edge-policies.md#forcenetworkinprocess) — принудительный запуск сетевого кода в процессе браузера.

<!-- End 84 -->
## <a name="version-83047864-july-13"></a>Версия 83.0.478.64: 13 июля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-83047861-july-7"></a>Версия 83.0.478.61: 7 июля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-83047858-june-30"></a>Версия 83.0.478.58: 30 июня

Исправлены ошибки и проблемы с производительностью.

## <a name="version-83047856-june-24"></a>Версия 83.0.478.56: 24 июня

Исправлены ошибки и проблемы с производительностью.

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#june-24-2020)

## <a name="version-83047854-june-17"></a>Версия 83.0.478.54: 17 июня

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#june-17-2020)

## <a name="version-83047850-june-15"></a>Версия 83.0.478.50: 15 июня

Исправлены ошибки и проблемы с производительностью.

## <a name="version-83047845-june-4"></a>Версия 83.0.478.45: 4 июня

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#june-4-2020)

## <a name="version-83047844-june-1"></a>Версия 83.0.478.44: 1 июня

Исправлены ошибки и проблемы с производительностью.

## <a name="version-83047837-may-21"></a>Версия 83.0.478.37: 21 мая

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#may-21-2020)

### <a name="feature-updates"></a>Обновления компонентов

- Обновления Microsoft Edge теперь будут разворачиваться постепенно. В дальнейшем обновления для Microsoft Edge будут разворачиваться для пользователей в течение нескольких дней. Это позволяет обеспечить для вас дополнительную защиту от обновлений со случайными ошибками, что улучшает взаимодействие с обновлениями. В качестве пользователя вы продолжите без проблем получать автоматические обновления. Если ваша организация не зарегистрирована для получения автоматических обновлений, это изменение вас не затронет. Дополнительные сведения см. в [статье о постепенном развертывании](microsoft-edge-update-progressive-rollout.md).
- Усовершенствования фильтра SmartScreen в Microsoft Defender: реализован ряд улучшений службы фильтра SmartScreen в Microsoft Defender, включая улучшенную защиту от вредоносных сайтов с перенаправлением при загрузке и блокирование фреймов верхнего уровня, полностью заменяющее вредоносные сайты страницей безопасности фильтра SmartScreen в Microsoft Defender. Функция блокирования фрейма верхнего уровня запрещает воспроизведение звука и других данных мультимедиа с вредоносного сайта, за счет чего повышается удобство и снижается путаница.

- Пользователи теперь могут исключить некоторые файлы cookie из автоматического удаления при закрытии браузера. Эта возможность добавлена на основе отзывов пользователей. Этот вариант пригодится, если пользователи не хотят выходить с определенного сайта, но при этом хотят удалить все остальные файлы cookie при закрытии браузера. Чтобы использовать эту функцию, перейдите по адресу *edge://settings/clearBrowsingDataOnClose* и включите переключатель "Файлы cookie и другие данные сайтов".

- Теперь доступна функция автоматического переключения профилей для более удобного доступа к рабочему содержимому. Если на работе вы используете несколько профилей, можно проверить работу этой функции: достаточно зайти с личным профилем на сайт, на котором требуется проверка подлинности с рабочей или учебной учетной записью. Когда мы это обнаружим, вы получите предложение переключиться на рабочий профиль, чтобы получить доступ к сайту, не проходя проверку подлинности. Когда вы выберете рабочий профиль, на который нужно переключиться, веб-сайт просто откроется в вашем рабочем профиле. Надеемся, что такой подход поможет вам отделить рабочие данные от личных и удобнее получать доступ к рабочему содержимому. Если вы не хотите, чтобы эта функция предлагала вам переключить профиль, можно выбрать "Больше не спрашивать", тогда эти запросы не будут отображаться.

- Улучшения функции коллекций:
  - Можно перетаскивать элементы в коллекцию, не открывая ее. При перетаскивании можно выбрать место в списке коллекции, в которое нужно поместить элемент.
  - Можно добавлять сразу несколько элементов в коллекцию, а не только по одному. Чтобы добавить несколько элементов, выделите их и перетащите в коллекцию. Также можно выделить элементы, щелкнуть их правой кнопкой мыши и выбрать коллекцию, в которую нужно их поместить.

- Можно добавить все вкладки в окне Edge в коллекцию без необходимости добавлять их по отдельности. Для этого щелкните любую вкладку правой кнопкой мыши и выберите "Добавить все вкладки в новую коллекцию".

- Теперь доступна синхронизация расширений. Можно синхронизировать расширения на всех устройствах. С Microsoft Edge синхронизируются расширения из Microsoft Store и Chrome Store. Чтобы использовать эту функцию, щелкните многоточие (**…**) в строке меню и выберите **Параметры**. Щелкните **Синхронизация** в вашем профиле, чтобы открыть варианты синхронизации. Используйте переключатель в разделе **Профили/Синхронизация**, чтобы включить расширения. Можно отключить синхронизацию расширений с помощью групповой политики [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled).

- Улучшено сообщение на странице управления загрузкой для заблокированных небезопасных загруженных файлов.

- Усовершенствования иммерсивного средства чтения:
  - добавлена поддержка наречий в инструменте иммерсивного средства чтения "Части речи". При чтении статьи с помощью иммерсивного средства чтения откройте средства проверки правописания и выберите наречия в разделе "Части речи", чтобы выделить все наречия на странице.
  - Добавлена возможность выбрать любое содержимое на веб-странице и открыть его в иммерсивном средстве чтения. Эта возможность позволяет пользователям использовать иммерсивное средство чтения, а также все средства обучения, такие как "Выделение строк" и "Прочесть вслух", на всех веб-сайтах.

- Неправильно введенный пользователями URL-адрес поможет исправить средство для исправления ссылок, которое корректирует узел и поисковый запрос. Например: <br>
Пользователь по ошибке вводит "powerbi" как "powerbbi".com. Средство для исправления ссылок предложит вариант "powerbi".com в качестве откорректированного варианта и создаст ссылку на поиск "powerbbi" на случай, если пользователь ищет что-то другое.

- Разрешите пользователям сохранять свое решение о запуске внешний протокол для определенного сайта. Чтобы включить или отключить эту функцию, пользователи могут настроить политику [ExternalProtocolDialogShowAlwaysOpenCheckbox]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox).

- Microsoft Edge можно задать в качестве браузера по умолчанию непосредственно в **параметрах** Microsoft Edge. Таким образом пользователям легче переназначить браузер по умолчанию— можно сделать это из самого браузера вместо того, чтобы искать эту возможность параметрах операционной системы. Чтобы использовать эту функцию, перейдите на *edge://settings/defaultBrowser* и нажмите **Сделать браузером по умолчанию**.

- Несколько обновлений средств разработчика, в том числе новая удаленная поддержка отладки, улучшения пользовательского интерфейса и многое другое. Дополнительные сведения см. в статье [Что нового в средствах разработчика (Microsoft Edge 83)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

- Теперь доступен сценарий предупреждения MCAS (Microsoft Cloud Access Security). Это позволяет администраторам настраивать предупреждение — новую категорию блокировок MCAS, в которой пользователь может переопределить страницу блокировки MCAS. Блокировки MDATP E5 изначально интегрированы в блокировки SmartScreen в Microsoft Edge для удобства работы. Это позволяет использовать красную блокировку на всю страницу с сообщением "Этот веб-сайт заблокирован вашей организацией", а не только всплывающее уведомление.

- Запрет синхронного объекта XmlHttpRequest при закрытии страницы. Отправка синхронных объектов XmlHttpRequest во время выгрузки веб-страницы будет устранена. Это изменение улучшает производительность и надежность браузера, но может повлиять на веб-приложения, которые еще не были обновлены для использования более современных веб-API, включая sendBeacon и fetch. Групповая политика для отключения этого изменения и разрешения синхронного XHR при закрытии страницы будет доступна до Microsoft Edge 88. Дополнительные сведения см. в статье [Изменения, вносимые в Microsoft Edge, которые влияю на совместимость сайтов](/microsoft-edge/web-platform/site-impacting-changes).

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено 15 новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [AllowSurfGame](./microsoft-edge-policies.md#allowsurfgame) — разрешить игру "Серфинг".
- [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) — настроить список сайтов, для которых Microsoft Edge попытается установить привязку токена.
- [BingAdsSuppression](./microsoft-edge-policies.md#bingadssuppression) — блокировать всю рекламу в результатах поиска Bing.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) — определяет, используется ли встроенное средство проверки сертификатов для проверки сертификатов серверов.
- [ClearCachedImagesAndFilesOnExit](./microsoft-edge-policies.md#clearcachedimagesandfilesonexit) — очистка кэшированных изображений и файлов при закрытии Microsoft Edge.
- [ConfigureShare](./microsoft-edge-policies.md#configureshare) — настройка возможностей общего доступа.
- [DeleteDataOnMigration](./microsoft-edge-policies.md#deletedataonmigration) — удаление данных старого браузера при миграции.
- [DnsOverHttpsMode](./microsoft-edge-policies.md#dnsoverhttpsmode) — управление режимом DNS по протоколу HTTPS.
- [DnsOverHttpsTemplates](./microsoft-edge-policies.md#dnsoverhttpstemplates) — настройка шаблона URI нужного сопоставителя DNS по протоколу HTTPS.
- [FamilySafetySettingsEnabled](./microsoft-edge-policies.md#familysafetysettingsenabled) — разрешить пользователям настраивать семейную безопасность.
- [LocalProvidersEnabled](./microsoft-edge-policies.md#localprovidersenabled) — разрешить варианты поиска локальных поставщиков.
- [ScrollToTextFragmentEnabled](./microsoft-edge-policies.md#scrolltotextfragmentenabled) — разрешить прокрутку до текста, указанного во фрагментах URL-адресов.
- [ScreenCaptureAllowed](./microsoft-edge-policies.md#screencaptureallowed) — разрешить или запретить создание снимков экрана.
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) — настройка списка типов, исключенных из синхронизации.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled)— включить скрытие родной Windows.

#### <a name="deprecated-policy"></a>Политика устарела

Следующая политика продолжит работать в этом выпуске. Она станет устаревшей в будущем выпуске.

[EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) — включение скачивания действий с доменами в Майкрософт

<!-- end 83 -->

## <a name="version-81041677-may-18"></a>Версия 81.0.416.77: 18 мая

Исправлены ошибки и проблемы с производительностью.

## <a name="version-81041672-may-7"></a>Версия 81.0.416.72: 7 мая

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#may-7-2020)

## <a name="version-81041668-april-29"></a>Версия 81.0.416.68: 29 апреля

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#april-29-2020)

## <a name="version-81041664-april-23"></a>Версия 81.0.416.64: 23 апреля

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#april-23-2020)

## <a name="version-81041658-april-17"></a>Версия 81.0.416.58: 17 апреля

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#april-17-2020)

## <a name="version-81041653-april-13"></a>Версия 81.0.416.53: 13 апреля

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#april-13-2020)

### <a name="feature-updates"></a>Обновления компонентов

- Добавлена поддержка для Windows Information Protection (WIP), чтобы помочь предприятиям защитить конфиденциальные данные от несанкционированного раскрытия. [Подробнее](./microsoft-edge-security-windows-information-protection.md).

- Стали доступны коллекции. Чтобы начать работу, щелкните значок "Коллекции" рядом с адресной строкой. Откроется область "Коллекции", где можно создавать, редактировать и просматривать коллекции. Мы создали Коллекции на основе ваших действий в Интернете. Если вы покупатель, путешественник, преподаватель или учащийся, Коллекции помогут вам. [Подробнее](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Разрешение удаления (скрытие с панели инструментов) кнопки "Коллекции" с панели инструментов Microsoft Edge для согласованности.

- Автоматический вход локальной учетной записи Active Directory будет использоваться только для организаций, включивших его.  Если пользователи уже выполнили вход с помощью локальной учетной записи AD, им будет доступна возможность выхода из нее. Для пользователей автоматический вход в систему с основной учетной записью будет выполняться лишь в случае, если это учетная запись Майкрософт или учетная запись Azure Active Directory. Администраторы могут включить автоматический вход с использованием локальной учетной записи AD с помощью политики ConfigureOnPremisesAccountAutoSignIn.

- Application Guard. Поддержка расширений теперь доступна в контейнере.

- Добавлено сообщение для пользователей о том, что Internet Explorer не установлен, при переходе на страницу, настроенную для открытия в режиме Internet Explorer.

- В средствах разработчика Microsoft Edge обновлен инструмент трехмерного представления с добавлением новой функции для отладки контекста стопки z-index. Трехмерное представление демонстрирует глубину модели DOM с помощью цвета и стопки, а представление z-Index помогает изолировать разные контексты стопки страницы. [Подробнее](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/).

- Средства разработчика F12 локализованы на 10 новых языках, и теперь они будут соответствовать языку, используемому в браузере. [Подробнее](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/).

- Добавлена поддержка воспроизведения Dolby Vision. В Windows 10 сборки 17134 (обновление за апрель 2018 г.) с поддержкой Dolby Vision веб-сайты могут отображать контент Dolby Vision. Узнайте, как включить контент Dolby Vision в [Netflix](https://help.netflix.com/en/node/42384).

- Microsoft Edge теперь может определять и удалять дубликаты избранного, а также объединять папки с одинаковыми именами. Чтобы получить доступ к инструменту, щелкните звезду на панели инструментов браузера и выберите "Удалить дубликаты избранного".  Вы можете подтвердить изменения, и все обновления в папке "Избранное" будут синхронизированы на других устройствах.

- Пользователи сообщили нам, что сложно отличить обычное окно браузера в темном режиме от окна InPrivate, так как для обоих окон используется темное обрамление. Новый сплошной синий значок InPrivate в правом верхнем углу помогает пользователям убедиться в использовании режима InPrivate.

- Открытие внешних ссылок в правильном профиле браузера. Выберите профиль по умолчанию для ссылок, открываемых во внешних приложениях, на странице *edge://settings/multiProfileSettings*.

- Добавлено предупреждение для пользователей, входящих в профиль браузера с помощью учетной записи после ранее выполненного входа с помощью другой учетной записи. Это предупреждение поможет предотвратить непреднамеренное объединение данных.

- Если вы сохранили карты оплаты в своей учетной записи Майкрософт, их можно использовать в Microsoft Edge при заполнении форм платежей. Карты из вашей учетной записи Майкрософт будут синхронизированы на других компьютерах, а все сведения будут предоставляться веб-сайту после двухфакторной проверки подлинности (код CVC и ваше удостоверение Майкрософт). Для дополнительного удобства вы можете безопасно сохранить копию карты на устройстве во время проверки подлинности.

- Выделение строк предназначено для пользователей, которые хотят сосредоточиться на ограниченной части содержимого при чтении. Эта функция позволяет пользователям сосредоточиться на одной, трех или пяти строках и затемняет остальную страницу, чтобы не отвлекать пользователей при чтении.  Пользователи могут прокручивать страницы с помощью касания или клавиш со стрелками, и фокус смещается соответствующим образом.

- Браузер Microsoft Edge теперь интегрирован с Windows Speller на платформах Windows 8.1 и более поздних версий. Эта интеграция обеспечивает дополнительную языковую поддержку с доступом к словарям дополнительных языков и возможностью использования настраиваемых словарей Windows. После добавления языка в языковые параметры операционной системы дальнейших действий от пользователей не требуется. Кроме того, в параметрах Microsoft Edge активирован переключатель проверки орфографии.

- Когда PDF-документы открываются в Microsoft Edge, пользователи могут создавать выделение, изменять цвет и удалять выделение. Эта функция помогает в дальнейшем ссылаться на важные части документа при совместной работе.

- При загрузке длинных PDF-документов, оптимизированных для Интернета, просматриваемые пользователем страницы загружаются быстрее, одновременно с загрузкой остального документа.

- Стало проще запустить средство иммерсивного чтения для веб-сайта с помощью клавиши F9.

- Стало проще запустить функцию "Прочесть вслух" с помощью сочетания клавиш (CTRL+SHIFT+U).

- Добавлен параметр командной строки MSI, позволяющий отключить создание значков на рабочем столе при установке Microsoft Edge. В следующем примере показано, как использовать этот новый параметр: <br>
`MicrosoftEdgeEnterpriseX64.msi DONOTCREATEDESKTOPSHORTCUT=true`<br>
Предстоящий выпуск будет содержать групповую политику для поддержки этой возможности.

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено 11 новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled) — включение внешней проверки подлинности для InPrivate и гостевых профилей. 
- [AudioSandboxEnabled](./microsoft-edge-policies.md#audiosandboxenabled) — разрешение запускать Audio Sandbox.
- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) — использование политики источника ссылки no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](./microsoft-edge-policies.md#globallyscopehttpauthcacheenabled) — включение глобального кэша HTTP-авторизации.
- [ImportExtensions](./microsoft-edge-policies.md#importextensions) — разрешение импорта расширений.
- [ImportCookies](./microsoft-edge-policies.md#importcookies) — разрешение импорта файлов cookie.
- [ImportShortcuts](./microsoft-edge-policies.md#importshortcuts) — разрешение импорта ярлыков.
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect) — указание, как будут действовать переходы в пределах страницы на ненастроенные сайты, начинаемые со страниц в режиме Internet Explorer.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) — включение более строгой обработки для смешанного контента.
- [TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) — включение функции безопасности TLS 1.3 для местных якорей доверия.
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin) — настройка автоматического входа с помощью учетной записи домена Active Directory при отсутствии учетной записи домена Azure AD.

#### <a name="policy-name-and-caption-changes"></a>Изменение имени и описания политики

`OmniboxMSBProviderEnabled` политики изменен на [AddressBarMicrosoftSearchInBingProviderEnabled](//DeployEdge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled). Описание политики– "Включение предложений Поиска (Майкрософт) в Bing в адресной строке".

#### <a name="deprecated-policies"></a>Устаревшие политики

В этом выпуске продолжают действовать следующие политики. Они станут устаревшими в будущем выпуске.

- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) — повторное включение API веб-компонентов v0 до M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) — разрешение WebDriver переопределять несовместимые политики.

#### <a name="resolved-issues"></a>Устраненные проблемы

- Исправлена проблема, из-за которой в Microsoft Edge в режиме IE диалоговое окно загрузки выводилось даже после загрузки файла.
- Исправлена проблема, из-за которой Microsoft Edge удалял файлы cookie сеанса, когда страница, уже находящаяся в режиме IE, инициировала открытие новой вкладки в режиме IE.

## <a name="version-800361111-april-7"></a>Версия 80.0.361.111: 7 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-800361109-april-1"></a>Версия 80.0.361.109: 1 апреля

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#april-1-2020)

## <a name="version-80036169-march-19"></a>Версия 80.0.361.69: 19 марта

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#march-19-2020)

## <a name="version-80036166-march-4"></a>Версия 80.0.361.66: 4 марта

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#march-4-2020)

## <a name="version-80036162-february-25"></a>Версия 80.0.361.62: 25 февраля

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#february-25-2020)

## <a name="version-80036157-february-20"></a>Версия 80.0.361.57: 20 февраля

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#february-20-2020)

## <a name="version-80036156-february-19"></a>Версия 80.0.361.56: 19 февраля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-80036154-february-14"></a>Версия 80.0.361.54: 14 февраля

### <a name="resolved-issues"></a>Устраненные проблемы

- Исправлена проблема, из-за который пароль, оплата и файлы cookie не импортировались в Microsoft Edge.

## <a name="version-80036150-february-11"></a>Версия 80.0.361.50: 11 февраля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-80036148-february-7"></a>Версия 80.0.361.48: 7 февраля

Список обновлений системы безопасности находится [здесь](./microsoft-edge-relnotes-security.md#february-7-2020)

### <a name="feature-updates"></a>Обновления компонентов

- Добавлена защита SmartScreen от скачивания нежелательных приложений. [Подробнее](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus)
- Добавлена поддержка воспроизведения Dolby Vision.
- Поддерживается возможность для пользователей Windows Mixed Reality просматривать видео 360° на гарнитурах виртуальной реальности.
- В режим чтения добавлен параметр для увеличения интервалов.
- Добавлена поддержка удаления ссылок с помощью ластика ручки Surface.
- Добавлена поддержка клавиш со стрелками и клавиши пробела для рисования на снимках экрана для отзывов в режиме редактора.
- Улучшена надежность отображения снимков экрана. Теперь они не отображаются полностью черными при отправке отзыва.
- Добавлена поддержка темной темы на локальной новой вкладке, которая отображается, если устройство не подключено к Интернету.
- Добавлена возможность восстановления веб-сайтов, установленных как приложения, при восстановлении сеанса браузера после обновления, сбоя и т. д.
- Добавлена поддержка темной темы в пользовательском интерфейсе PDF, если браузер управляется групповой политикой.
- Обновлено приложение Adobe Flash до версии 32.0.0.321. [Подробнее](https://helpx.adobe.com/flash-player/release-note/fp_32_air_32_release_notes.html)

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено 16 новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [AlternateErrorPagesEnabled](./microsoft-edge-policies.md#alternateerrorpagesenabled) — предлагает похожие страницы, если веб-страница не найдена.
- [DefaultInsecureContentSetting](./microsoft-edge-policies.md#defaultinsecurecontentsetting) — управляемое использование небезопасных исключений содержимого.
- [DNSInterceptionChecksEnabled](./microsoft-edge-policies.md#dnsinterceptionchecksenabled) — включены проверки перехвата DNS.
- [HideFirstRunExperience](./microsoft-edge-policies.md#hidefirstrunexperience) — скрытие экрана первого запуска и экрана-заставки.
- [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) — разрешение небезопасного содержимого на указанных сайтах.
- [InsecureContentBlockedForUrls](./microsoft-edge-policies.md#insecurecontentblockedforurls) — блокирование небезопасного содержимого на указанных сайтах.
- [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) — поддержка стандартного устаревшего параметра поведения SameSite для cookie-файлов.
- [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) — возврат к устаревшему поведению SameSite для cookie-файлов на указанных сайтах.
- [PaymentMethodQueryEnabled](./microsoft-edge-policies.md#paymentmethodqueryenabled) — разрешение веб-сайтам запрашивать доступные способы оплаты.
- [PersonalizationReportingEnabled](./microsoft-edge-policies.md#personalizationreportingenabled) — разрешение персонализации рекламы, поиска и новостей путем отправки журнала браузера в корпорацию Майкрософт.
- [PinningWizardAllowed](./microsoft-edge-policies.md#pinningwizardallowed) — разрешает использование мастера закрепления на панели задач.
- [SmartScreenPuaEnabled](./microsoft-edge-policies.md#smartscreenpuaenabled) — настройка Microsoft Defender SmartScreen для блокирования нежелательных приложений.
- [TotalMemoryLimitMb](./microsoft-edge-policies.md#totalmemorylimitmb) — настройка ограничения в мегабайтах памяти, которое может использовать один экземпляр Microsoft Edge.
- [WebAppInstallForceList](./microsoft-edge-policies.md#webappinstallforcelist) — настройка списка принудительно устанавливаемых веб-приложений.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) — повторное включение API веб-компонентов v0 до M84.
- [WebRtcLocalIpsAllowedUrls](./microsoft-edge-policies.md#webrtclocalipsallowedurls) — управление отображением локальных IP-адресов с помощью WebRTC.

#### <a name="deprecated-policies"></a>Устаревшие политики

Следующая политика устарела.

- [NewTabPageCompanyLogo](./microsoft-edge-policies.md#newtabpagecompanylogo) — настройка логотипа компании для новой вкладки.

### <a name="resolved-issues"></a>Устраненные проблемы

- Исправлена проблема, из-за которой звук не работает в среде Citrix.
- Исправлена проблема, из-за которой параллельная работа Microsoft Edge и устаревшей версии Microsoft Edge приводит к повреждению устаревших ссылок и сбоям.

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)