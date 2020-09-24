---
title: Заметки о выпуске Microsoft Edge для стабильного канала
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 09/23/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для стабильного канала
ms.openlocfilehash: 91bb0ee198b22a25e61470962d4f192a5adf737d
ms.sourcegitcommit: 4d250c0c48634ecb1ea7ca03307809c80bb21db8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2020
ms.locfileid: "11077636"
---
# Заметки о выпуске для стабильного канала Microsoft Edge

Эти заметки о выпуске содержат сведения о новых компонентах и обновлениях, не связанных с безопасностью, которые включены в стабильный канал Microsoft Edge. Чтобы ознакомиться с каналами Microsoft Edge, см. статью [Обзор каналов в Microsoft Edge](microsoft-edge-channels.md). Список обновлений системы безопасности находится [здесь](microsoft-edge-relnotes-security.md).

> [!NOTE]
> Для стабильного канала обновления последовательно разворачиваются в течение одного или нескольких дней. Дополнительные сведения см. в статье [Последовательные развертывания обновлений Microsoft Edge](microsoft-edge-update-progressive-rollout.md).

## Версия 85.0.564.63: 23 сентября

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#september-23-2020)

## Версия 85.0.564.51: 9 сентября

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#september-9-2020)

## Версия 85.0.564.44: 31 августа

Исправлены ошибки и проблемы с производительностью.
<!-- begin 85 -->
## Версия 85.0.564.41: 27 августа

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#august-27-2020)

### Обновления компонентов

- **Локальная синхронизация элементов "Избранное" и "Параметры"**. Теперь вы синхронизируете избранные элементы браузера и параметры между профилями Active Directory в собственной среде без необходимости синхронизации с облаком.

- **Поддержка групповой политики Microsoft Edge для комбинаций "доверенный веб-сайт + приложение" для запуска без запроса подтверждения**. Добавлена поддержка групповой политики, которая позволяет администраторам добавлять комбинации "доверенный веб-сайт + приложение", которые можно запускать без запроса подтверждения. Это позволяет администраторам настраивать комбинации доверенных протоколов и источников данных (например, Microsoft 365), чтобы конечные пользователи могли подавить запрос на подтверждение при переходе по URL-адресу, содержащему протокол приложения.

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
- [TLSCsipherSuiteDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tlsciphersuitedenylist) — выбор наборов шифров TLS для отключения.

#### Устаревшие политики

- [EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload) - Разрешение загрузки действий домена из Microsoft.
- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) — повторное включение API веб-компонентов v0 до M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies)- Разрешение WebDriver переопределять несовместимые политики.

<!--- END 85 ---->

## Версия 84.0.522.63: 20 августа

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#august-20-2020).

## Версия 84.0.522.61: 17 августа

Исправлены ошибки и проблемы с производительностью.

## Версия 84.0.522.59: 11 августа

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#august-11-2020)

## Версия 84.0.522.58: 10 августа

Исправлены ошибки и проблемы с производительностью.

## Версия 84.0.522.52: 1 августа

Исправлены ошибки и проблемы с производительностью.

## Версия 84.0.522.50: 31 июля

Исправлены ошибки и проблемы с производительностью.

## Версия 84.0.522.49: 29 июля

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#july-29-2020)

## Версия 84.0.522.48: 28 июля

Исправлены ошибки и проблемы с производительностью.

## Версия 84.0.522.44: 23 июля

Исправлены ошибки и проблемы с производительностью.

<!-- begin 84 -->
## Версия 84.0.522.40: 16 июля

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#july-16-2020)

### Обновления компонентов

- Эта версия Microsoft Edge обеспечивает оптимизированное время скачивания списка сайтов для режима Internet Explorer. Мы сократили задержку скачивания для списка сайтов в режиме Internet Explorer до 0 секунд (с 60-секундного ожидания) при отсутствии кэшированного списка сайтов. Мы также добавили поддержку групповой политики для случаев, когда требуется задержка перехода на домашнюю страницу режима Internet Explorer, пока скачивается список сайтов. Дополнительные сведения см. в политике [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload).

- Microsoft Edge теперь позволяет пользователям входить в браузер, если он "запущен от имени администратора" в Windows 10. Это помогает пользователям, использующим Microsoft Edge в Windows Server или в сценариях удаленного рабочего стола и песочницы.

- Microsoft Edge теперь обеспечивает полную поддержку мыши в полноэкранном режиме. Теперь с помощью мыши вы можете получить доступ к вкладкам, адресной строке и другим элементам, не выходя из полноэкранного режима.

- Улучшение покупок в Интернете. Добавляйте собственные псевдонимы для сохраненных дебетовых и кредитных карт. Теперь вы можете отличать свои кредитные карты при совершении покупок в Интернете. Присвоение псевдонима для дебетовой или кредитной карты позволяет выбрать правильную карту при использовании автозаполнения для выбора способа оплаты.

- Протоколы TLS/1.0 и TLS/1.1 отключены по умолчанию.  Политика [SSLVersionMin](https://docs.microsoft.com/deployedge/microsoft-edge-policies#sslversionmin) позволяет повторно включить протокол TLS/1.0 и TLS/1.1. Эта политика будет доступна как минимум до Microsoft Edge версии 88. Дополнительные сведения см. в статье [Изменения, вносимые в Microsoft Edge, которые влияю на совместимость сайтов](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

- Улучшения коллекций:

  - Добавлена функция заметок, позволяющая добавлять заметку или комментарий к элементу коллекции. Заметки группируются вместе и остаются прикрепленными к элементу, даже если вы сортируете элементы в коллекции. Чтобы попробовать эту новую функцию, щелкните элемент правой кнопкой мыши и выберите "Добавить заметку".
  - Вы можете изменить цвет фона заметок в коллекциях. Цветовую кодировку можно использовать для упорядочения информации и повышения производительности.
  - Имеются заметные улучшения производительности, позволяющие экспортировать коллекции в Excel быстрее, чем в предыдущих версиях Microsoft Edge.

- Дополнительная поддержка API Microsoft Edge:

  - Для экспериментов включен API доступа к хранилищу. Эта функция включена для домашних и корпоративных пользователей путем присвоения политике [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/deployedge/microsoft-edge-policies#experimentationandconfigurationservicecontrol) значения "Full". Эта функция будет включена по умолчанию для всех пользователей стабильного канала Microsoft Edge версии 85.
  
    По мере роста значимости конфиденциальности для пользователей все чаще возникают запросы на более строгие параметры браузера, используемые по умолчанию, и параметры согласия пользователей на использование, такие как блокировка доступа ко всем сторонним хранилищам. Хотя эти параметры улучшают конфиденциальность и блокируют нежелательный доступ неизвестными или недоверенными сторонами, они могут привести к нежелательным побочным эффектам, например к блокировке доступа к содержимому, которое хочет просмотреть пользователь (например, социальные сети и внедренный мультимедийный контент).

    API доступа к хранилищу позволяет получить доступ к основному хранилищу в стороннем контексте, когда пользователь демонстрирует явное намерение разрешить хранилище, которое в противном случае блокируется текущей конфигурацией браузера. Дополнительные сведения см. в разделе [API доступа к хранилищу](https://www.chromestatus.com/feature/5612590694662144).

  - API собственной файловой системы, означающий, что вы можете предоставлять сайтам разрешения на изменение файлов или папок с помощью API собственной файловой системы.

- Улучшения PDF-файлов:

  - Чтение вслух для PDF-файлов позволяет пользователям прослушивать содержимое PDF при выполнении других важных задач. Это также помогает обучающимся, использующим аудиовизуальные материалы, сосредоточиться на чтении содержимого, облегчая процесс обучения.
  - Улучшено редактирование PDF-файлов. Теперь вы можете сохранить в файле изменения, внесенные в PDF, вместо сохранения копии при каждом изменении PDF-файла.

- Microsoft Edge теперь поддерживает перевод в иммерсивном средстве чтения. Когда пользователь открывает представление иммерсивного средства чтения, появляется возможность перевести страницу на нужный язык.

- Несколько обновлений средств разработчика, включая поддержку настройки сочетаний клавиш в соответствии с VS Code и просмотр средств разработчика в высокой контрастности.  Дополнительные сведения см. в статье [Новые возможности средств разработчика (Microsoft Edge 84)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/05/devtools).

### Обновления политик

#### Новые политики

Добавлено семь новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [AppCacheForceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#appcacheforceenabled) — разрешает повторное включение компонента AppCache, даже если он отключен по умолчанию.
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy) — настройка параметров прокси-сервера контейнера Application Guard.
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload) — требование наличия списка сайтов в режиме предприятия перед навигацией по вкладкам.
- [WinHttpProxyResolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#winhttpproxyresolverenabled) — использование сопоставителя прокси-сервера Windows.
- [InternetExplorerIntegrationEnhancedHangDetection](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationenhancedhangdetection) — настройка расширенного обнаружения зависаний в режиме Internet Explorer.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled)— чтобы снизить энергопотребление и нагрузку на процессор, Microsoft Edge определяет, когда окно закрыто другими окнами, и приостанавливает работу рисования пикселей.
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout) — установка времени ожидания для навигации по вкладкам списка сайтов в режиме предприятия.

#### Устаревшие политики

- [AllowSyncXHRInPageDismissal](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal) — разрешение страницам отправлять синхронные запросы XHR при удалении страницы.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) — определяет, используется ли встроенное средство проверки сертификатов для проверки сертификатов серверов.
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled) — включение более строгой обработки для смешанного контента.

#### Устаревшая политика

[ForceNetworkInProcess](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcenetworkinprocess) — принудительный запуск сетевого кода в процессе браузера.

<!-- End 84 -->
## Версия 83.0.478.64: 13 июля

Исправлены ошибки и проблемы с производительностью.

## Версия 83.0.478.61: 7 июля

Исправлены ошибки и проблемы с производительностью.

## Версия 83.0.478.58: 30 июня

Исправлены ошибки и проблемы с производительностью.

## Версия 83.0.478.56: 24 июня

Исправлены ошибки и проблемы с производительностью.

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#june-24-2020)

## Версия 83.0.478.54: 17 июня

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#june-17-2020)

## Версия 83.0.478.50: 15 июня

Исправлены ошибки и проблемы с производительностью.

## Версия 83.0.478.45: 4 июня

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#june-4-2020)

## Версия 83.0.478.44: 1 июня

Исправлены ошибки и проблемы с производительностью.

## Версия 83.0.478.37: 21 мая

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#may-21-2020)

### Обновления компонентов

- Обновления Microsoft Edge теперь будут разворачиваться постепенно. В дальнейшем обновления для Microsoft Edge будут разворачиваться для пользователей в течение нескольких дней. Это позволяет обеспечить для вас дополнительную защиту от обновлений со случайными ошибками, что улучшает взаимодействие с обновлениями. В качестве пользователя вы продолжите без проблем получать автоматические обновления. Если ваша организация не зарегистрирована для получения автоматических обновлений, это изменение вас не затронет. Дополнительные сведения см. в [статье о постепенном развертывании](microsoft-edge-update-progressive-rollout.md).
- Усовершенствования фильтра SmartScreen в Microsoft Defender: реализован ряд улучшений службы фильтра SmartScreen в Microsoft Defender, включая улучшенную защиту от вредоносных сайтов с перенаправлением при загрузке и блокирование фреймов верхнего уровня, полностью заменяющее вредоносные сайты страницей безопасности фильтра SmartScreen в Microsoft Defender. Функция блокирования фрейма верхнего уровня запрещает воспроизведение звука и других данных мультимедиа с вредоносного сайта, за счет чего повышается удобство и снижается путаница.

- Пользователи теперь могут исключить некоторые файлы cookie из автоматического удаления при закрытии браузера. Эта возможность добавлена на основе отзывов пользователей. Этот вариант пригодится, если пользователи не хотят выходить с определенного сайта, но при этом хотят удалить все остальные файлы cookie при закрытии браузера. Чтобы использовать эту функцию, перейдите по адресу *edge://settings/clearBrowsingDataOnClose* и включите переключатель "Файлы cookie и другие данные сайтов".

- Теперь доступна функция автоматического переключения профилей для более удобного доступа к рабочему содержимому. Если на работе вы используете несколько профилей, можно проверить работу этой функции: достаточно зайти с личным профилем на сайт, на котором требуется проверка подлинности с рабочей или учебной учетной записью. Когда мы это обнаружим, вы получите предложение переключиться на рабочий профиль, чтобы получить доступ к сайту, не проходя проверку подлинности. Когда вы выберете рабочий профиль, на который нужно переключиться, веб-сайт просто откроется в вашем рабочем профиле. Надеемся, что такой подход поможет вам отделить рабочие данные от личных и удобнее получать доступ к рабочему содержимому. Если вы не хотите, чтобы эта функция предлагала вам переключить профиль, можно выбрать "Больше не спрашивать", тогда эти запросы не будут отображаться.

- Улучшения функции коллекций:
  - Можно перетаскивать элементы в коллекцию, не открывая ее. При перетаскивании можно выбрать место в списке коллекции, в которое нужно поместить элемент.
  - Можно добавлять сразу несколько элементов в коллекцию, а не только по одному. Чтобы добавить несколько элементов, выделите их и перетащите в коллекцию. Также можно выделить элементы, щелкнуть их правой кнопкой мыши и выбрать коллекцию, в которую нужно их поместить.

- Можно добавить все вкладки в окне Edge в коллекцию без необходимости добавлять их по отдельности. Для этого щелкните любую вкладку правой кнопкой мыши и выберите "Добавить все вкладки в новую коллекцию".

- Теперь доступна синхронизация расширений. Можно синхронизировать расширения на всех устройствах. С Microsoft Edge синхронизируются расширения из Microsoft Store и Chrome Store. Чтобы использовать эту функцию, щелкните многоточие (**…**) в строке меню и выберите **Параметры**. Щелкните **Синхронизация** в вашем профиле, чтобы открыть варианты синхронизации. Используйте переключатель в разделе **Профили/Синхронизация**, чтобы включить расширения. Можно отключить синхронизацию расширений с помощью групповой политики [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled).

- Улучшено сообщение на странице управления загрузкой для заблокированных небезопасных загруженных файлов.

- Усовершенствования иммерсивного средства чтения:
  - добавлена поддержка наречий в инструменте иммерсивного средства чтения "Части речи". При чтении статьи с помощью иммерсивного средства чтения откройте средства проверки правописания и выберите наречия в разделе "Части речи", чтобы выделить все наречия на странице.
  - Добавлена возможность выбрать любое содержимое на веб-странице и открыть его в иммерсивном средстве чтения. Эта возможность позволяет пользователям использовать иммерсивное средство чтения, а также все средства обучения, такие как "Выделение строк" и "Прочесть вслух", на всех веб-сайтах.

- Неправильно введенный пользователями URL-адрес поможет исправить средство для исправления ссылок, которое корректирует узел и поисковый запрос. Например: <br>
Пользователь по ошибке вводит "powerbi" как "powerbbi".com. Средство для исправления ссылок предложит вариант "powerbi".com в качестве откорректированного варианта и создаст ссылку на поиск "powerbbi" на случай, если пользователь ищет что-то другое.

- Разрешите пользователям сохранять свое решение о запуске внешний протокол для определенного сайта. Чтобы включить или отключить эту функцию, пользователи могут настроить политику [ExternalProtocolDialogShowAlwaysOpenCheckbox]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox).

- Microsoft Edge можно задать в качестве браузера по умолчанию непосредственно в **параметрах** Microsoft Edge. Таким образом пользователям легче переназначить браузер по умолчанию— можно сделать это из самого браузера вместо того, чтобы искать эту возможность параметрах операционной системы. Чтобы использовать эту функцию, перейдите на *edge://settings/defaultBrowser* и нажмите **Сделать браузером по умолчанию**.

- Несколько обновлений средств разработчика, в том числе новая удаленная поддержка отладки, улучшения пользовательского интерфейса и многое другое. Дополнительные сведения см. в статье [Что нового в средствах разработчика (Microsoft Edge 83)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

- Теперь доступен сценарий предупреждения MCAS (Microsoft Cloud Access Security). Это позволяет администраторам настраивать предупреждение — новую категорию блокировок MCAS, в которой пользователь может переопределить страницу блокировки MCAS. Блокировки MDATP E5 изначально интегрированы в блокировки SmartScreen в Microsoft Edge для удобства работы. Это позволяет использовать красную блокировку на всю страницу с сообщением "Этот веб-сайт заблокирован вашей организацией", а не только всплывающее уведомление.

- Запрет синхронного объекта XmlHttpRequest при закрытии страницы. Отправка синхронных объектов XmlHttpRequest во время выгрузки веб-страницы будет устранена. Это изменение улучшает производительность и надежность браузера, но может повлиять на веб-приложения, которые еще не были обновлены для использования более современных веб-API, включая sendBeacon и fetch. Групповая политика для отключения этого изменения и разрешения синхронного XHR при закрытии страницы будет доступна до Microsoft Edge 88. Дополнительные сведения см. в статье [Изменения, вносимые в Microsoft Edge, которые влияю на совместимость сайтов](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

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

<!-- end 83 -->

## Версия 81.0.416.77: 18 мая

Исправлены ошибки и проблемы с производительностью.

## Версия 81.0.416.72: 7 мая

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#may-7-2020)

## Версия 81.0.416.68: 29 апреля

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-29-2020)

## Версия 81.0.416.64: 23 апреля

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-23-2020)

## Версия 81.0.416.58: 17 апреля

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-17-2020)

## Версия 81.0.416.53: 13 апреля

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-13-2020)

### Обновления компонентов

- Добавлена поддержка для Windows Information Protection (WIP), чтобы помочь предприятиям защитить конфиденциальные данные от несанкционированного раскрытия. [Подробнее](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection).

- Стали доступны коллекции. Чтобы начать работу, щелкните значок "Коллекции" рядом с адресной строкой. Откроется область "Коллекции", где можно создавать, редактировать и просматривать коллекции. Мы создали Коллекции на основе ваших действий в Интернете. Если вы покупатель, путешественник, преподаватель или учащийся, Коллекции помогут вам. [Подробнее](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Разрешение удаления (скрытие с панели инструментов) кнопки "Коллекции" с панели инструментов Microsoft Edge для согласованности.

- Автоматический вход локальной учетной записи Active Directory будет использоваться только для организаций, включивших его.  Если пользователи уже выполнили вход с помощью локальной учетной записи AD, им будет доступна возможность выхода из нее. Пользователи будут автоматически входить только с помощью основной учетной записи в своей операционной системе, если это учетная запись MSA или Azure AD. Администраторы могут включить автоматический вход с использованием локальной учетной записи AD с помощью политики ConfigureOnPremisesAccountAutoSignIn.

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

### Обновления политик

#### Новые политики

Добавлено 11 новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled) — включение внешней проверки подлинности для InPrivate и гостевых профилей. 
- [AudioSandboxEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#audiosandboxenabled) — разрешение запускать Audio Sandbox.
- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy) — использование политики источника ссылки no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#globallyscopehttpauthcacheenabled) — включение глобального кэша HTTP-авторизации.
- [ImportExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importextensions) — разрешение импорта расширений.
- [ImportCookies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importcookies) — разрешение импорта файлов cookie.
- [ImportShortcuts](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importshortcuts) — разрешение импорта ярлыков.
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect) — указание, как будут действовать переходы в пределах страницы на ненастроенные сайты, начинаемые со страниц в режиме Internet Explorer.
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled) — включение более строгой обработки для смешанного контента.
- [TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled) — включение функции безопасности TLS 1.3 для местных якорей доверия.
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin) — настройка автоматического входа с помощью учетной записи домена Active Directory при отсутствии учетной записи домена Azure AD.

#### Изменение имени и описания политики

`OmniboxMSBProviderEnabled` политики изменен на [AddressBarMicrosoftSearchInBingProviderEnabled](https://docs.microsoft.com//DeployEdge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled). Описание политики– "Включение предложений Поиска (Майкрософт) в Bing в адресной строке".

#### Устаревшие политики

В этом выпуске продолжают действовать следующие политики. Они станут устаревшими в будущем выпуске.

- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) — повторное включение API веб-компонентов v0 до M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) — разрешение WebDriver переопределять несовместимые политики.

#### Устраненные проблемы

- Исправлена проблема, из-за которой в Microsoft Edge в режиме IE диалоговое окно загрузки выводилось даже после загрузки файла.
- Исправлена проблема, из-за которой Microsoft Edge удалял файлы cookie сеанса, когда страница, уже находящаяся в режиме IE, инициировала открытие новой вкладки в режиме IE.

## Версия 80.0.361.111: 7 апреля

Исправлены ошибки и проблемы с производительностью.

## Версия 80.0.361.109: 1 апреля

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-1-2020)

## Версия 80.0.361.69: 19 марта

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#march-19-2020)

## Версия 80.0.361.66: 4 марта

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#march-4-2020)

## Версия 80.0.361.62: 25 февраля

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#february-25-2020)

## Версия 80.0.361.57: 20 февраля

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#february-20-2020)

## Версия 80.0.361.56: 19 февраля

Исправлены ошибки и проблемы с производительностью.

## Версия 80.0.361.54: 14 февраля

### Устраненные проблемы

- Исправлена проблема, из-за который пароль, оплата и файлы cookie не импортировались в Microsoft Edge.

## Версия 80.0.361.50: 11 февраля

Исправлены ошибки и проблемы с производительностью.

## Версия 80.0.361.48: 7 февраля

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#february-7-2020)

### Обновления компонентов

- Добавлена защита SmartScreen от скачивания нежелательных приложений. [Подробнее](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus)
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

### Обновления политик

#### Новые политики

Добавлено 16 новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [AlternateErrorPagesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#alternateerrorpagesenabled) — предлагает похожие страницы, если веб-страница не найдена.
- [DefaultInsecureContentSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultinsecurecontentsetting) — управляемое использование небезопасных исключений содержимого.
- [DNSInterceptionChecksEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsinterceptionchecksenabled) — включены проверки перехвата DNS.
- [HideFirstRunExperience](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hidefirstrunexperience) — скрытие экрана первого запуска и экрана-заставки.
- [InsecureContentAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecurecontentallowedforurls) — разрешение небезопасного содержимого на указанных сайтах.
- [InsecureContentBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecurecontentblockedforurls) — блокирование небезопасного содержимого на указанных сайтах.
- [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) — поддержка стандартного устаревшего параметра поведения SameSite для cookie-файлов.
- [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) — возврат к устаревшему поведению SameSite для cookie-файлов на указанных сайтах.
- [PaymentMethodQueryEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#paymentmethodqueryenabled) — разрешение веб-сайтам запрашивать доступные способы оплаты.
- [PersonalizationReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#personalizationreportingenabled) — разрешение персонализации рекламы, поиска и новостей путем отправки журнала браузера в корпорацию Майкрософт.
- [PinningWizardAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pinningwizardallowed) — разрешает использование мастера закрепления на панели задач.
- [SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled) — настройка Microsoft Defender SmartScreen для блокирования нежелательных приложений.
- [TotalMemoryLimitMb](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#totalmemorylimitmb) — настройка ограничения в мегабайтах памяти, которое может использовать один экземпляр Microsoft Edge.
- [WebAppInstallForceList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webappinstallforcelist) — настройка списка принудительно устанавливаемых веб-приложений.
- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) — повторное включение API веб-компонентов v0 до M84.
- [WebRtcLocalIpsAllowedUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtclocalipsallowedurls) — управление отображением локальных IP-адресов с помощью WebRTC.

#### Устаревшие политики

Следующая политика устарела.

- [NewTabPageCompanyLogo](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagecompanylogo) — настройка логотипа компании для новой вкладки.

### Устраненные проблемы

- Исправлена проблема, из-за которой звук не работает в среде Citrix.
- Исправлена проблема, из-за которой параллельная работа Microsoft Edge и устаревшей версии Microsoft Edge приводит к повреждению устаревших ссылок и сбоям.

## См. также

- [Использование целевой страницы Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
