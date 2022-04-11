---
title: Архивные заметки о выпуске для канала Microsoft Edge Beta
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 04/08/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Архивные заметки о выпуске для канала Microsoft Edge Beta
ms.openlocfilehash: 71db889e373c09832ead59547b08b0a285ed0b78
ms.sourcegitcommit: dd8cdbd35726c795ddce917e549ddf17ee7f5290
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/11/2022
ms.locfileid: "12473646"
---
# <a name="archived-release-notes-for-microsoft-edge-beta-channel"></a>Архивные заметки о выпуске для канала Microsoft Edge Beta

Эти заметки о выпуске содержат сведения о новых компонентах и не связанных с безопасностью обновлениях, которые включены в канал Microsoft Edge Beta. Чтобы ознакомиться с каналами Microsoft Edge, см. статью [Обзор каналов Microsoft Edge](microsoft-edge-channels.md). Список всех обновлений системы безопасности находится [здесь](microsoft-edge-relnotes-security.md).

## <a name="version-990115011-february-9"></a>Версия 99.0.1150.11: 9 февраля

### <a name="feature-updates"></a>Обновления компонентов

- **Предстоящий трехзначный номер версии в строке агента пользователя.** Начиная с версии 100, Microsoft Edge будет отправлять трехзначный номер версии в заголовке User-Agent, например, "Edg/100". Начиная с Microsoft Edge 97, владельцы сайтов могут протестировать эту строку будущего агента, включив флаг эксперимента **#force-major-version-to-100** в *edge://flags* для обеспечения надежности и работы логики синтаксического анализа User-Agent.

- **Персонализация многопрофильного опыта с помощью предпочтений профиля для сайтов.** Пользователи могут персонализировать работу с несколькими профилями, создав настраиваемый список сайтов для автоматического переключения профилей в Microsoft Edge.

- **Двунаправленный общий доступ к файлам cookie для режима IE.** Эта функция расширяет возможности общего доступа к файлам cookie и позволяет пользователям синхронизировать определенные файлы cookie сеанса из режима Internet Explorer или IE в Microsoft Edge. Дополнительные сведения см. в статье о [совместном использовании файлов cookie между Microsoft Edge и Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

- **Навигация по PDF-документам с помощью эскизов страниц.** Теперь вы сможете перемещаться по PDF-документу с помощью эскизов, представляющих страницы. Эти эскизы будут отображаться в области в левой части экрана средства чтения PDF-файлов.

- **Настройка списка доменов, для которых пользовательский интерфейс диспетчера паролей для функций "Сохранение" и "Заполнение" будет отключен.** Используйте политику [PasswordManagerBlocklist](/deployedge/microsoft-edge-policies#passwordmanagerblocklist) для настройки списка доменов (только схемы и имена узлов HTTP/HTTPS), в которых Microsoft Edge должен отключить диспетчер паролей. Это означает, что рабочие процессы "Сохранить" и "Заполнить" будут отключены, что позволит не сохранять пароли для этих веб-сайтов или не заполнять их в веб-формы автоматически.

- **Обновите расширения для Microsoft Edge надстроек с помощью API (в общедоступной предварительной версии).** Вы можете интегрировать эти API непосредственно в конвейер сборки и опубликовать обновления пакетов на веб-сайте Microsoft Edge надстройки. Дополнительные сведения см. в Microsoft Edge [API надстроек (в закрытой предварительной версии)](/microsoft-edge/extensions-chromium/publish/api/using-addons-api)

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

- [AllowGamesMenu](/DeployEdge/microsoft-edge-policies#allowgamesmenu) - Разрешить пользователям доступ к меню игр
- [DoNotSilentlyBlockProtocolsFromOrigins](/DeployEdge/microsoft-edge-policies#donotsilentlyblockprotocolsfromorigins) - Определить список протоколов, которые не могут быть автоматически заблокированы защитой от переполнения
- [HubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#hubssidebarenabled) - Показать боковую панель центров
- [InternetExplorerIntegrationCloudNeutralSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) - Настройка отправки отчетов о потенциально неправильно настроенных URL-адресах нейтральных сайтов в приложение "Списки сайтов" Центра администрирования M365
- [InternetExplorerIntegrationCloudUserSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) - Настройка отправки отчетов о записях списка пользователей в режиме IE в приложение "Списки сайтов" Центра администрирования M365
- [PasswordManagerBlocklist](/DeployEdge/microsoft-edge-policies#passwordmanagerblocklist) - Настройка списка доменов, для которых пользовательский интерфейс диспетчера паролей (сохранение и заполнение) будет отключен
- [RelatedMatchesCloudServiceEnabled](/DeployEdge/microsoft-edge-policies#relatedmatchescloudserviceenabled) - Настройка связанных соответствий в разделе "Найти на странице"
- [SignInCtaOnNtpEnabled](/DeployEdge/microsoft-edge-policies#signinctaonntpenabled) - Включить диалоговое окно входа в систему по щелчку для принятия действий
- [UserAgentReduction](/DeployEdge/microsoft-edge-policies#useragentreduction) - Включение или отключение уменьшения числа агентов пользователей

## <a name="version-980110848-february-8"></a>Версия 98.0.1108.48: 8 февраля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-980110843-february-3"></a>Версия 98.0.1108.43: 3 февраля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-980110842-february-2"></a>Версия 98.0.1108.42: 2 февраля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-980110839-january-31"></a>Версия 98.0.1108.39: 31 января

Исправлены ошибки и проблемы с производительностью.

## <a name="version-980110833-january-24"></a>Версия 98.0.1108.33: 24 января

Исправлены ошибки и проблемы с производительностью.

## <a name="version-980110827-january-19"></a>Версия 98.0.1108.27: 19 января

Исправлены ошибки и проблемы с производительностью.

## <a name="version-980110823-january-14"></a>Версия 98.0.1108.23: 14 января

### <a name="feature-updates"></a>Обновления компонентов

- **Усильте безопасность в Интернете.** Режим просмотра в Microsoft Edge, где безопасность браузера имеет приоритет, что обеспечивает дополнительный уровень защиты при просмотре в Интернете. Администраторы могут применять следующие групповые политики к рабочим столам конечных пользователей (Windows, macOS и Linux), чтобы защититься от нуля дней. Эти политики также позволяют важным сайтам и бизнес-приложениям продолжать работать должным образом. Эта функция является очень большим шагом вперед, так как позволяет нам устранять непредвиденные активные нулевые дни (на основе исторических тенденций). Если эта функция включена, она обеспечивает аппаратную защиту стека, Произвольный code Guard (ACG) и Content Flow Guard (CFG) в качестве поддержки мер по устранению рисков безопасности для повышения безопасности пользователей в Интернете.
Групповые политики:
  - [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode)
  - [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains)
  - [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains)

- **Пользовательский основной пароль.** В браузере уже есть возможность, в которой пользователи могут добавить шаг проверки подлинности перед автоматическим заполнением сохраненных паролей в веб-формах. Это добавляет еще один уровень конфиденциальности и помогает предотвратить использование неавторизованными пользователями сохраненных паролей для входа на веб-сайты. Пользовательский основной пароль— это развитие той же функции, где пользователи теперь смогут использовать настраиваемую строку по своему выбору в качестве основного пароля. После включения пользователи будут вводить этот пароль для проверки подлинности и автоматического заполнения сохраненных паролей в веб-формах.

- **Прокрутки наложения добавлены в Microsoft Edge.** Мы обновили панели прокрутки с помощью дизайна на основе наложения. Пользователи могут включить эту функцию в *edge://flags*.

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

- [AddressBarEditingEnabled](/DeployEdge/microsoft-edge-policies#addressbareditingenabled) — настройка редактирования адресной строки.
- [EdgeFollowEnabled](/DeployEdge/microsoft-edge-policies#edgefollowenabled) — включение службы "Подписка" в Microsoft Edge.
- [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode) — улучшение состояния безопасности в Microsoft Edge.
- [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains) — настройка списка доменов, для которых режим повышенной безопасности не будет применяться.
- [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains) — настройте список доменов, для которых всегда будет применяться расширенный режим безопасности.
- [InAppSupportEnabled](/DeployEdge/microsoft-edge-policies#inappsupportenabled) — включена поддержка в приложении.
- [MicrosoftEdgeInsiderPromotionEnabled](/DeployEdge/microsoft-edge-policies#microsoftedgeinsiderpromotionenabled) — Microsoft Edge insider Promotion Enabled.
- [PrintStickySettings](/DeployEdge/microsoft-edge-policies#printstickysettings) — печать параметров предварительного просмотра с закреплением.
- [SandboxExternalProtocolBlocked](/DeployEdge/microsoft-edge-policies#sandboxexternalprotocolblocked) — Microsoft Edge блокировать навигацию по внешним протоколам в изолированном iframe.
- [U2fSecurityKeyApiEnabled](/DeployEdge/microsoft-edge-policies#u2fsecuritykeyapienabled) — разрешить использование устаревшего API ключа безопасности U2F.

## <a name="version-970107254-january-5"></a>Версия 97.0.1072.54: 5 января

Исправлены ошибки и проблемы с производительностью.

## <a name="version-970107252-january-3"></a>Версия 97.0.1072.52: 3 января

Исправлены ошибки и проблемы с производительностью.

## <a name="version-970107241-december-20"></a>Версия 97.0.1072.41: 20 декабря

Исправлены ошибки и проблемы с производительностью.

## <a name="version-970107234-december-13"></a>Версия 97.0.1072.34: 13 декабря

Исправлены ошибки и проблемы с производительностью.

## <a name="version-970107228-december-8"></a>Версия 97.0.1072.28: 8 декабря

Исправлены ошибки и проблемы с производительностью.

## <a name="version-970107221-december-1"></a>Версия 97.0.1072.21: 1 декабря

### <a name="feature-updates"></a>Обновления компонентов

- **Используйте текущий профиль для входа на веб-сайты при входе нескольких рабочих или учебных учетных записей на устройстве.** Если на устройстве осуществлен вход в несколько учетных записей организации или учебного заведения, пользователям будет предложено выбрать учетную запись из средства выбора учетной записи, чтобы продолжить посещения веб-сайтов. В этом выпуске пользователям будет предложено разрешить Microsoft Edge автоматический вход на веб-сайты с помощью рабочей и учебной учетной записи, которые вошли в текущий профиль. Пользователи могут включать и отключать эту функцию в **параметрах Параметры профиля.**

- **Добавьте поддержку защиты от потери данных (DLP) в конечной точке Майкрософт в macOS.** Принудительное применение политики защиты от потери данных в конечной точке Майкрософт доступно в macOS.

- **Откройте PDF-файлы с цифровой подписью.**  Цифровые подписи широко используются для проверки подлинности документа и изменений в документе. Пользователи могут проверять подписи для PDF-файлов непосредственно из браузера, не требуя надстроек.

- **Цитаты в Microsoft Edge.** Учащимся часто необходимо цитировать источники для исследования. Им необходимо управлять множеством справочных материалов и источников, а это непростая задача. Кроме того, им необходимо перевести эти цитаты в соответствующие форматы, такие как APA, MLA и Chicago. Эта новая функция "Ссылки" в Microsoft Edge (теперь в предварительной версии) позволяет учащимся лучше управлять ссылками и создавать их по мере исследования в Интернете. Если ссылки включены в коллекциях или из раздела **Параметры и другое (ALT-F)**, Microsoft Edge автоматически создает цитаты, которые учащиеся смогут использовать позже, чтобы они могли сосредоточиться на своих исследованиях. Когда все будет готово, можно будет легко скомпилировать эти цитаты в окончательный результат. Дополнительные сведения см. в статье [Предварительный просмотр цитат в Microsoft Edge](https://blogs.windows.com/msedgedev/2021/11/04/preview-citations-feature-edge/).

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

- [AccessibilityImageLabelsEnabled](/DeployEdge/microsoft-edge-policies#accessibilityimagelabelsenabled) - Получение описаний изображений от Майкрософт включено
- [CORSNonWildcardRequestHeadersSupport](/DeployEdge/microsoft-edge-policies#corsnonwildcardrequestheaderssupport) - Включена поддержка заголовка запроса CORS без подстановочных знаков
- [EdgeDiscoverEnabled](/DeployEdge/microsoft-edge-policies#edgediscoverenabled) - Функция обнаружения в Microsoft Edge
- [EdgeEnhanceImagesEnabled](/DeployEdge/microsoft-edge-policies#edgeenhanceimagesenabled) - Улучшение изображений включено
- [InternetExplorerModeTabInEdgeModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorermodetabinedgemodeallowed) - Разрешить открывать в Microsoft Edge сайты, настроенные для режима Internet Explorer
- [SameOriginTabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#sameorigintabcaptureallowedbyorigins) - Разрешить этим источникам запись вкладок из этих же источников
- [ScreenCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#screencaptureallowedbyorigins) - Разрешить этим источникам запись рабочего стола, окон и вкладок
- [SerialAllowAllPortsForUrls](/DeployEdge/microsoft-edge-policies#serialallowallportsforurls) - Автоматически предоставлять сайтам разрешение на подключение всех последовательных портов
- [SerialAllowUsbDevicesForUrls](/DeployEdge/microsoft-edge-policies#serialallowusbdevicesforurls) - Автоматическое предоставление сайтам разрешений на подключение к последовательным USB-устройствам
- [SerialAllowUsbDevicesForUrls](/DeployEdge/microsoft-edge-policies#smartscreendnsrequestsenabled) - Включить DNS-запросы фильтра SmartScreen в Microsoft Defender
- [TabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#tabcaptureallowedbyorigins) - Разрешить этим источникам запись вкладок
- [WebSQLInThirdPartyContextEnabled](/DeployEdge/microsoft-edge-policies#websqlinthirdpartycontextenabled) - Принудительное повторное включение WebSQL в сторонних контекстах
- [WindowCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#windowcaptureallowedbyorigins) - Разрешить этим источникам запись окон и вкладок

#### <a name="obsoleted-policies"></a>Устаревшие политики

- [AppCacheForceEnabled](/deployedge/microsoft-edge-policies#appcacheforceenabled) — разрешает повторное включение компонента AppCache, даже если он отключен по умолчанию.

## <a name="version-960105434-november-23"></a>Версия 96.0.1054.34: 23 ноября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-960105426-november-17"></a>Версия 96.0.1054.26: 17 ноября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-960105424-november-16"></a>Версия 96.0.1054.24: 16 ноября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-960105413-november-5"></a>Версия 96.0.1054.13: 5 ноября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-96010548-november-1"></a>Версия 96.0.1054.8: 1 ноября

### <a name="feature-updates"></a>Обновления компонентов

- **Запустите прогрессивное веб-приложение (PWA) непосредственно по ссылкам протокола.** Разрешим установленным PWA обрабатывать ссылки, использующие определенный протокол для более интегрированного взаимодействия.

- **Узнайте, как решать математические задачи с помощью математического решателя.** Мы рады сообщить, что вы можете использовать математический решатель в Microsoft Edge для получения справки по широкому спектру математических понятий. Эти понятия могут варьироваться от простейших арифметических и квадратических уравнений до тригонометрии и вычислений. Математический решатель позволяет сделать снимок рукописной или печатной математической задачи, а затем предоставляет мгновенное решение с пошаговые инструкции, которые помогут вам узнать, как получить решение без помощи. Математический решатель также поставляется с математической клавиатурой, с помощью которую можно легко ввести математические задачи. Эта клавиатура устраняет необходимость поиска по традиционной клавиатуре, чтобы найти нужные математические символы. После решения проблемы математическое решение предоставляет возможности для продолжения обучения с помощью тестов, листов и видеоучений.

- **Выделение свободной формы в PDF.** Возможности просмотра PDF-файлов и разметки улучшены благодаря добавлению выделенных элементов свободной формы. Вы можете выделить разделы в файлах PDF, к которым у вас нет доступа, и просмотреть документы.

- **Аппаратная защита стека.**  Microsoft Edge начнет поддерживать еще более безопасный режим просмотра, использующий аппаратный поток управления для процессов браузера на поддерживаемом оборудовании (Intel 11-го поколения. или AMD Zen 3). Примечание. Так как это управляемый выпуск компонентов, вы можете не заметить, что эта функция включена на всех устройствах. Вы можете включить или отключить аппаратную защиту стека, используя параметры выполнения файлов изображений (IFEO) с помощью групповой политики.

- **Новое диалоговое окно предупреждения для сайтов опечаток.** Теперь браузер отображает предупреждение на некоторых сайтах с URL-адресами, которые выглядят аналогично другим сайтам. В этом пользовательском интерфейсе используется эвристика на стороне клиента, чтобы предупреждать пользователей о сайтах, которые могут подделывать популярные веб-сайты. Дополнительные сведения см. в разделе "Что такое [опечатка"?](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0)

- **Улучшена передача данных между режимом IE и современным браузером.**  Начиная с этой версии Microsoft Edge навигация между Microsoft Edge и режимом Internet Explorer будет включать данные формы и дополнительные заголовки HTTP. Заголовки ссылок, данные публикации, данные форм и методы запроса будут правильно перенаправлены между двумя интерфейсами. Вы можете указать, какие типы данных следует включить, с помощью политики [InternetExplorerIntegrationComplexNavDataTypes](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) . Дополнительные сведения см. в разделе "Часто задаваемые вопросы". Мое приложение требует передачи данных POST между режимом [IE и Microsoft Edge](./edge-ie-mode-faq.md#my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported).

- **Управление списками облачных сайтов для режима IE в общедоступной предварительной версии.**  Cloud Site List Management позволяет управлять списками сайтов для режима IE в облаке, не требуя локальной инфраструктуры для размещения списка сайтов организации. Вы можете получить доступ к функции управления списками облачных сайтов с помощью Microsoft Edge списков сайтов в Microsoft 365 Admin Центре. Дополнительные сведения см. в статье об управлении списками облачных сайтов для [режима IE (общедоступная предварительная](./edge-ie-mode-cloud-site-list-mgmt.md) версия).

- **Обновите Microsoft Edge WebWiew2 с помощью WSUS.** ИТ-администраторы, использующие WSUS для обновления Microsoft Edge также смогут обновлять Microsoft Edge WebView2 с помощью служб WSUS. Эта возможность упрощает администрирование автономных устройств.

- **Обновления WSUS для Сервера.** Обновления WSUS и каталога для каналов Microsoft Edge (Stable, Beta, Dev) теперь будут применяться к SKU Windows Server, которые Microsoft Edge установлены, включая Windows Server 2022. Дополнительные сведения о настройке обновлений WSUS для Microsoft Edge см. [в Microsoft Edge.](https://docs.microsoft.com/mem/configmgr/apps/deploy-use/deploy-edge?bc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Ftoc.json#update-microsoft-edge)

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

- [ApplicationGuardUploadBlockingEnabled —](/DeployEdge/microsoft-edge-policies#applicationguarduploadblockingenabled) предотвращает отправку файлов в Application Guard.
- [AudioProcessHighPriorityEnabled](/DeployEdge/microsoft-edge-policies#audioprocesshighpriorityenabled) — позволяет аудиопроцессу выполняться с приоритетом выше обычного на Windows.
- [AutoLaunchProtocolsComponentEnabled](/DeployEdge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) — компонент протоколов AutoLaunch включен.
- [EfficiencyMode](/DeployEdge/microsoft-edge-policies#efficiencymode) — настройка того, когда должен активироваться режим эффективности.
- [ForceSyncTypes](/DeployEdge/microsoft-edge-policies#forcesynctypes) — настройка списка типов, включенных для синхронизации.
- [InternetExplorerIntegrationComplexNavDataTypes](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) — настройка отправки данных формы и заголовков HTTP при переходе в режим Internet Explorer или выходе из него.
- [InternetExplorerModeToolbarButtonEnabled](/DeployEdge/microsoft-edge-policies#internetexplorermodetoolbarbuttonenabled) — кнопка "Перезагрузить" в режиме Internet Explorer на панели инструментов.
- [PrintPostScriptMode](/DeployEdge/microsoft-edge-policies#printpostscriptmode) — печать в PostScript режиме.
- [PrintRasterizePdfDpi](/DeployEdge/microsoft-edge-policies#printrasterizepdfdpi) — печать в растеризации PDF DPI.
- [RendererAppContainerEnabled](/DeployEdge/microsoft-edge-policies#rendererappcontainerenabled) — включение отрисовщика в контейнере приложения.
- [SharedLinksEnabled](/DeployEdge/microsoft-edge-policies#sharedlinksenabled) — отображение ссылок, Microsoft 365 приложений в журнале.
- [TyposquattingCheckerEnabled](/DeployEdge/microsoft-edge-policies#typosquattingcheckerenabled) — настройка Edge TyposquattingChecker.

<!-- end major 96 --->

## <a name="version-950102038-october-28"></a>Версия 95.0.1020.38: 28 октября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-950102020-october-11"></a>Версия 95.0.1020.20: 11 октября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-950102014-october-5"></a>Версия 95.0.1020.14: 5 октября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-95010209-september-28"></a>Версия 95.0.1020.9: 28 сентября

### <a name="feature-updates"></a>Обновления компонентов

- **Поддержка функции "Просмотр в проводнике" для библиотек SharePoint Online в Microsoft Edge**  Теперь вы можете включить представление в проводник для SharePoint современных библиотек документов в Интернете. Чтобы этот интерфейс был видимым и рабочим для пользователей, необходимо включить политику Microsoft Edge "Настройка функции просмотра в [проводник для страниц SharePoint в Microsoft Edge"](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) и обновить конфигурацию клиента SharePoint Online. Дополнительные сведения: [просмотр SharePoint с помощью проводник в Microsoft Edge — SharePoint в Microsoft 365 | Документация Майкрософт](/SharePoint/sharepoint-view-in-edge).

- **URL-адреса файлов зоны интрасети будут открываться в проводнике Windows.**  Можно разрешить URL-адресам файлов с веб-сайтов из зоны интрасети, доступных по протоколу HTTPS, открывать проводник Windows для этих файлов и каталогов. Эту возможность можно включить с помощью политики [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled).

- **Улучшения возможностей скачивания.**  Поддержка скачивания пользовательского интерфейса распространяется на прогрессивные веб-приложения PWA и WebView. Кроме того, мы будет реализована поддержка перетаскивания в проводнике и на рабочем столе.

- **Возобновите работу с PDF-файлами с того места, на котором вы остановились.**  Вы можете возобновить чтение из места последнего закрытия PDF-документа.

- **Режим эффективности продлевает время работы батареи, когда ноутбук переключается в режим экономии заряда.**  Когда ноутбук перейдет в режим экономии заряда, включится режим эффективности, чтобы разрешить браузеру управлять ресурсами для увеличения времени работы батареи вашего устройства. У вас будет четыре варианта, когда режим эффективности становится активным, отключенным и низким зарядом батареи, отключенным, всегда и никогда. Примечание. Это управляемое развертывание компонентов. На устройствах с аккумулятором должна быть включена функция.

***Новые политики***

- [BrowserLegacyExtensionPointsBlockingEnabled](/DeployEdge/microsoft-edge-policies#browserlegacyextensionpointsblockingenabled) — включение блокировки устаревшей точки расширения браузера.
- [CrossOriginWebAssemblyModuleSharingEnabled](/DeployEdge/microsoft-edge-policies#crossoriginwebassemblymodulesharingenabled) — указывает, могут ли модули WebAssembly отправляться независимо от источника.
- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) — указывает, установлена или пропущена политика разрешений для записи экрана.
- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) — настройка корректировки пикселей между высотами window.open, источником которых являются страницы режима IE, и Microsoft Edge страниц в режиме интеграции.
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) — настройка корректировки пикселей между ширинами window.open, источником которых являются страницы режима IE, и Microsoft Edge страниц режима.
- [IntranetFileLinksEnabled](/DeployEdge/microsoft-edge-policies#intranetfilelinksenabled) — разрешить открывать url-адреса файлов зоны интрасети из Microsoft Edge в Windows проводник.
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) — настройка поведения отката сбоев ShadowStack.
- [VisualSearchEnabled](/DeployEdge/microsoft-edge-policies#visualsearchenabled) — включение визуального поиска.

***Устаревшие политики***

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) — разрешить тестирование режима Internet Explorer.
- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) — поддержка стандартного устаревшего параметра поведения SameSite для cookie-файлов.

## <a name="version-94099223-september-17"></a>Версия 94.0.992.23: 17 сентября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-94099219-september-13"></a>Версия 94.0.992.19: 13 сентября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-94099214-september-7"></a>Версия 94.0.992.14: 7 сентября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-9409929-september-2"></a>Версия 94.0.992.9: 2 сентября

### <a name="feature-updates"></a>Обновления компонентов

- **Microsoft Edge переход на периодичность обновления в каналах Beta и Stable в течение 4 недель.**  Мы внедрим новый 4-недельный цикл выпуска для основных версий. Дополнительные сведения о решении см. здесь: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **Доступен новый вариант выпуска "Расширенный стабильный".**  Мы предлагаем новый вариант выпуска "Расширенный стабильный" для управляемых корпоративных клиентов. Вариант выпуска "Расширенный стабильный" будет сохраняться в четных версиях и обновляться каждые 8 недель. Система безопасности будет обновляться каждые две недели.  Дополнительные сведения см. здесь: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Улучшение поведения по умолчанию при открытии MHTML-файлов.**  MHTML-файлы будут по-прежнему открываться в режиме IE (если он включен), если только они не были сохранены в Microsoft Edge (с помощью параметров "Сохранить как" или "Сохранить страницу как"). Если файл сохранен в Microsoft Edge, он будет открываться только в Microsoft Edge.  Это изменение устраняет проблему отрисовки, которая наблюдалась при открытии MHTML-файлов, сохраненных в Microsoft Edge, в режиме IE.

- **Ограничение запросов частной сети безопасными контекстами.** При доступе к ресурсам в локальных (частных) сетях со страниц в Интернете требуется, чтобы эти страницы доставлялись по протоколу HTTPS. Это изменение осуществляется в проекте Chromium, на котором основан Microsoft Edge. Дополнительные сведения см. в [записи о состоянии платформы Chrome](https://chromestatus.com/feature/5436853517811712). Для поддержки сценариев, необходимых для сохранения совместимости с незащищенными страницами, доступны две политики совместимости: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) и [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls).

- **Блокировка скачивания смешанного контента.** На защищенных страницах разрешено скачивание только файлов, размещенных на других защищенных страницах, а загрузки, размещенные на незащищенных (отличных от HTTPS) страницах, блокируются, если они инициируются с защищенной страницы. Это изменение осуществляется в проекте Chromium, на котором основан Microsoft Edge. Дополнительные сведения см. в [записи блога безопасности Google](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html).

- **Включение неявного входа для локальных учетных записей.**   Если включить политику OnlyOnPremisesImplicitSigninEnabled, неявный вход будет включен только для локальных учетных записей.  Браузер Microsoft Edge не будет пытаться выполнять неявный вход в учетные записи MSA и AAD. Переход с локальных учетных записей на учетные записи AAD также будет остановлен.

- **К документам PDF добавлены поля для произвольного текста.**  Теперь мы поддерживаем добавление бесплатных текстовых полей в PDF-документы, которые можно использовать для заполнения форм и добавления видимых заметок.

- **С легкостью обновите пароли.**  Теперь браузер перейдет непосредственно на страницу изменения пароля для заданного веб-сайта, экономя время, и щелкает, избегая необходимости переходить на страницу вручную. Когда вы откроете эту страницу, браузер автоматически заполнит существующий пароль и предложит надежный уникальный новый пароль.  Обратите внимание: в настоящее время эта функция доступна на ограниченном количестве сайтов.  

- **Новая страница сведений о специальных возможностях.** Сведения о специальных возможностях теперь доступны на отдельной странице. Новую страницу можно найти в списке основных параметров edge://settings/accessibility. Здесь находятся параметры для увеличения масштаба веб-страницы и отображения хорошо заметного контура вокруг области фокусировки, а также другие параметры, позволяющие улучшить просмотр веб-страниц. Мы продолжим добавлять здесь новые параметры для будущих версий Microsoft Edge.

***Новые политики***

- [ApplicationGuardPassiveModeEnabled](/DeployEdge/microsoft-edge-policies#applicationguardpassivemodeenabled) — позволяет игнорировать конфигурацию списка сайтов Application Guard и просматривать сайты в Edge обычным образом.
- [OnlyOnPremisesImplicitSigninEnabled](/DeployEdge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) — включает неявный вход только для локальных учетных записей.
- [WebRtcRespectOsRoutingTableEnabled](/DeployEdge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) — включает поддержку правил таблицы маршрутизации Windows при создании одноранговых подключений через WebRTC.

***Устаревшая политика***

- [UserAgentClientHintsEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) — включает функцию клиентских подсказок User-Agent.

## <a name="version-93096133-august-27"></a>Версия 93.0.961.33: 27 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-93096127-august-20"></a>Версия 93.0.961.27: 20 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-93096124-august-18"></a>Версия 93.0.961.24: 18 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-93096111-august-3"></a>Версия 93.0.961.11: 3 августа

### <a name="feature-updates"></a>Обновления компонентов

- **Начальные предпочтения в Microsoft Edge.**  Начиная с Microsoft Edge версии 93, развертывание Microsoft Edge на предприятии станет проще с добавлением начальных [настроек](/deployedge/initial-preferences-support-on-microsoft-edge-browser).

- **Режим IE в Microsoft Edge поддерживает поведение "без слияния".**  Начиная с Microsoft Edge версии 93 режим IE на Microsoft Edge будет поддерживать "без слияния". Для конечного пользователя при запуске нового окна браузера из приложения в режиме IE оно будет в отдельном сеансе, аналогичном поведению в IE11. Вам потребуется настроить список сайтов, чтобы настроить сайты, которые должны запретить общий доступ к сеансам. Для каждого окна Microsoft Edge при первом посещении вкладки режима IE в этом окне, если это один из назначенных сайтов "без слияния", это окно блокируется в другом сеансе IE "без слияния" от всех остальных окон Microsoft Edge по крайней мере до закрытия последней вкладки режима IE в этом окне. [Здесь](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--no-merge--option-that-was-supported-in-internet-explorer-11-) вы найдете дополнительные сведения.

- **Группы вкладок.**  Возможность классифицировать вкладки по определяемой пользователем группам помогает эффективнее находить вкладки, переключаться и управлять ими в нескольких рабочих потоках. Для этого мы включаем группирование вкладок, начиная с Microsoft Edge версии 93.

- **Скрытие заголовка окна при использовании вертикальных вкладок.**  Получите дополнительные несколько пикселей обратно, скрыв заголовок окна браузера при использовании вертикальных вкладок. Начиная с Microsoft Edge версии 93, вы можете перейти к edge://settings/appearance и в разделе "Настройка панели инструментов" выберите параметр, чтобы скрыть заголовок строки в режиме вертикальной вкладки.

- **Видео "картинка в картинке" (PiP) в панели инструментов, вызываемой при наведении курсора.**  Начиная с Microsoft Edge версии 93, станет еще проще перейти в режим рисунка (PiP). При наведении курсора на поддерживаемое видео появляется панель инструментов, которая позволяет просматривать это видео в окне PiP.  Примечание. В настоящее время эта возможность доступна Microsoft Edge в macOS.  Вернитесь в ближайшее время, когда мы продолжим развертывание для Windows пользователей.

- **Удаление 3DES в TLS.**  Начиная с Microsoft Edge версии 93 поддержка TLS_RSA_WITH_3DES_EDE_CBC_SHA шифров будет удалена. Это изменение осуществляется в проекте Chromium, на котором основан Microsoft Edge. Дополнительные сведения см. в записи о [состоянии платформы Chrome](https://chromestatus.com/feature/6678134168485888). Кроме того, в Microsoft Edge версии 93 будет доступна политика [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) для поддержки сценариев, которым необходимо сохранение совместимости с устаревшими серверами. Эта политика совместимости устареет и перестанет работать в Microsoft Edge версии 95. Обновите затронутые серверы заранее.

- **Политики для обхода запросов ClickOnce и DirectInvoke.**  Мы обновили наши политики, чтобы включить обход запросов ClickOnce и приложения DirectInvoke для указанных типов файлов из указанных доменов. Для этого необходимо:

  - Включить [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) или [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Включить политику [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) и настроить список определенных типов файлов, для которых следует отключить ClickOnce и DirectInvoke.
  - [Включите политику AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls) и задайте список определенных доменов, ClickOnce и DirectInvoke будут отключены для

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

#### <a name="deprecated-policy"></a>Нерекомендуемая политика

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

- **Поиск журнала браузера на естественном языке в адресной строке**. Поиск нужной статьи или веб-сайта теперь проще благодаря поиску на естественном языке прямо из адресной строки. Результаты поиска можно найти по содержимому страницы, описанию и времени (например, "рецепту на прошлой неделе"), а также только по совпадениям ключевых слов заголовков и URL-адресов.
Обратите внимание: это контролируемый выпуск компонентов. Если вы не видите эту возможность, вернитесь сюда позже, так как выпуск продолжается.

- **Пользователи могут легко перейти в режим Internet Explorer в Microsoft Edge**. Начиная с Microsoft Edge версии 92, пользователи могут перезагрузить сайт в режиме Internet Explorer в Microsoft Edge, а не в отдельном приложении IE 11 в ожидании настройки сайта в списке сайтов в режиме предприятия. Пользователям будет предложено добавить сайт в список локальных сайтов, чтобы переход на ту же страницу в Microsoft Edge автоматически происходил в режиме IE в течение следующих 30 дней. Вы можете использовать политику *[InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)*, чтобы настроить это взаимодействие и разрешить доступ к точкам входа в режиме IE, а также настроить возможность добавления сайтов в список локальных сайтов. Вы можете использовать политику *[InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)*, чтобы настроить количество дней хранения сайтов в списке локальных сайтов.
Обратите внимание, что комплексной работы для Windows 10 версии 1909 требуется KB5003698 или более поздняя версия, для Windows 10 версии 2004, Windows 10 версии 20H2 или Windows 10 версии 21H1 требуется KB5003690 или более поздняя версия.

- **MHTML-файлы по умолчанию открываются в режиме Internet Explorer**. Начиная с Microsoft Edge версии 92 Stable, MHTML-файлы автоматически открываются в режиме Internet Explorer в Microsoft Edge, а не в приложении Internet Explorer (IE11). Это чаще всего наблюдается при попытке просмотра электронной почты Outlook в браузере. Это изменение будет происходить только в том случае, если IE11 является обработчиком по умолчанию для этого типа файлов. Если вы хотите изменить это, это можно сделать перед установкой обновления Stable версии 92 с помощью [этого руководства](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

- **Платежные инструменты теперь синхронизируются между устройствами**. Начиная с Microsoft Edge версии 92, вы можете синхронизировать платежную информацию между устройствами, на которых вы выполнили вход.
Обратите внимание: это контролируемый выпуск компонентов. Если эта функция отсутствует, вернитесь сюда позже, поскольку выпуск продолжается.

- **Предупреждение "Отключить расширения режима разработчика" можно закрыть окончательно**. Начиная с Microsoft Edge версии 92, вы можете отключить предупреждение "Отключить расширения режима разработчика", нажав параметр "Не показывать это снова".
Обратите внимание: это контролируемый выпуск компонентов. Если эта функция отсутствует, вернитесь сюда позже, поскольку выпуск продолжается.

- **Управляйте расширениями непосредственно с панели инструментов**. Совершенно новое меню расширений на панели инструментов позволит легко скрыть расширения или закрепить их. Быстрые ссылки на управление расширениями и поиск новых расширений упростят поиск новых расширений и управление существующими.
Обратите внимание: это контролируемый выпуск компонентов. Если эта функция отсутствует, вернитесь сюда позже, поскольку выпуск продолжается.

- **Автоматическое использование HTTPS**. Пользователи смогут обновить навигацию с HTTP до HTTPS для доменов, которые, скорее всего, поддерживают этот более безопасный протокол. Эту поддержку также можно настроить так, чтобы попытка доставки по протоколу HTTPS осуществлялась для всех доменов.
Обратите внимание: мы экспериментируем с этой функцией, и это поведение не будет проявляться, если вы решили отказаться от экспериментов.

- **Улучшения визуализации шрифтов.** Улучшена четкость и снижена размытость при передаче текста.
Обратите внимание: это контролируемый выпуск компонентов. Если эта функция отсутствует, вернитесь сюда позже, поскольку выпуск продолжается.

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
<!---
Enterprise administrators may opt out of this behavior one of these two policies: 

    - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](./deployedge/microsoft-edge-policies.md#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains --->
Дополнительные сведения см[. в Microsoft Edge security downloads interruptions](/deployedge/microsoft-edge-security-downloads-interruptions)

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

## <a name="version-89077418-february-3"></a>Версия 89.0.774.18: 3 февраля

### <a name="feature-updates"></a>Обновления компонентов

- **Режим терминала включает дополнительные возможности блокировки.** Начиная с Microsoft Edge версии 89, мы добавили дополнительные возможности блокировки в режиме терминала, чтобы пользователи могли работать эффективно и безопасно. [Подробнее](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **Средство Enterprise Mode Site List Manager будет доступно в браузере на странице *edge://compat***. Это средство можно использовать для создания, изменения и экспорта XML списка сайтов для режима Internet Explorer в Microsoft Edge. Доступ к этому средству можно получить при необходимости с помощью групповой политики. [Подробнее](./edge-ie-mode-site-list-manager.md).

- **Повышение производительности браузера с помощью спящих вкладок**. Функция спящих вкладок повышает производительность браузера, переводя неактивные вкладки в спящий режим, чтобы освободить системные ресурсы, такие как память и процессор, и использовать их для активных вкладок или других приложений. Пользователи могут предотвратить переход сайтов в спящий режим и настроить время, по истечении которого неактивная вкладка перейдет в спящий режим. Чтобы пользователи могли оставаться в потоке, существуют также [эвристические методы](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434), которые предотвращают переход определенных сайтов, например сайтов интрасети, в спящий режим. Управлять этой возможностью можно с помощью групповых политик.

  > [!NOTE]
  > "Повышение производительности браузера с помощью спящих вкладок" — это обновление заметок о выпуске от 3 февраля для основной версии 89.0.774.18.

- **Сброс данных синхронизации Microsoft Edge в облаке вручную**. Мы представляем способ сброса данных синхронизации Microsoft Edge из продукта. Это гарантирует очистку данных из служб Майкрософт, а также устранение определенных проблем с продуктом, которые ранее требовали передачи в службу поддержки.

- **Усовершенствования в области выделения текста в документах PDF**. Пользователи начнут более плавный и согласованный выбор текста в документах PDF, открытых в Microsoft Edge, начиная с версии 89.

- **Поле даты рождения теперь поддерживается автозаполнением**. В настоящее время Microsoft Edge позволяет сэкономить время и усилия при заполнении форм и создании учетных записей в Интернете путем автоматического заполнения таких данных, как адреса, имена, номера телефонов и т. д. Начиная с Microsoft Edge версии 89, мы добавляем поддержку для другого поля, которое можно сохранить и заполнить автоматически — дата рождения. Вы можете просматривать, изменять и удалять эти сведения в любое время в параметрах профиля.

- **Поддержка поиска на естественном языке в адресной строке, на странице поиска журнала и в центре журнала**. Начиная с Microsoft Edge версии 89, поиск статьи или веб-сайта будет проще при поиске на естественном языке в адресной панели, на странице журнала и в центре журнала. Пользователи могут искать ранее просматриваемое содержимое страницы, описание и время (например, "рецепт торта за последнюю неделю"), а также совпадения по ключевым словам заголовков и URL-адресов. Эта возможность доступна только случайно выбранной группе пользователей, участвующих в эксперименте. Эти пользователи предоставляют отзывы службе поддержки.

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) — параметры времени существования данных браузера
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled) — управление мобильными приложениями включено
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) — определение упорядоченного списка предпочитаемых языков, на которых должны отображаться веб-сайты, если сайт поддерживает этот язык
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) — разрешение рекомендаций и рекламных уведомлений из Microsoft Edge
- [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) — ограничение режима печати фона
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault)— режим печати фона по умолчанию
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist) — блокировка интеллектуальных действий для списка служб

#### <a name="obsoleted-policies"></a>Устаревшие политики

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) — использование политики ссылок по умолчанию для no-referrer-when-downgrade
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) — включение отчетов с данными об использовании и сбоях
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices)| — отправка сведений о сайтах для улучшения служб Майкрософт
<!-- end major 89 -->

## <a name="version-88070556-january-29"></a>Версия 88.0.705.56: 29 января

Исправлены ошибки и проблемы с производительностью.

## <a name="version-88070549-january-20"></a>Версия 88.0.705.49: 20 января

Исправлены ошибки и проблемы с производительностью.

## <a name="version-88070545-january-15"></a>Версия 88.0.705.45: 15 января

Исправлены ошибки и проблемы с производительностью.

## <a name="version-88070541-january-11"></a>Версия 88.0.705.41: 11 января

Исправлены ошибки и проблемы с производительностью.

## <a name="version-88070529-december-21"></a>Версия 88.0.705.29: 21 декабря

Исправлены ошибки и проблемы с производительностью.

<!-- begin major 88 -->
## <a name="version-88070518-december-9"></a>Версия 88.0.705.18: 9 декабря

### <a name="feature-updates"></a>Обновления компонентов

- **Нерекомендуемые компоненты:**

  - Не рекомендуется поддержка протокола FTP. Поддержка устаревшего протокола FTP удалена из Microsoft Edge. При попытке перейти по ссылке FTP браузер направит операционную систему на открытие внешнего приложения для обработки ссылки FTP. Кроме того, ИТ-администраторы могут настроить Microsoft Edge на использование режима IE для сайтов, которые используют протокол FTP.
  - Поддержка Adobe Flash будет удалена. Начиная с бета-версии Microsoft Edge 88, возможности и поддержка Adobe Flash будут удалены. Подробнее: [Новости об окончании поддержки Adobe Flash Player — блог Microsoft Edge (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Проверка подлинности:**

  - Единый вход теперь доступен для учетных записей Azure Active Directory (Azure AD) и учетной записи Майкрософт (MSA) в macOS и Windows нижнего уровня. Пользователь, выполнивший вход в Microsoft Edge в macOS или Microsoft Windows нижнего уровня (версии 7 и 8.1), теперь автоматически подключается к веб-сайтам, для которых настроено разрешение единого входа с помощью рабочей учетной записи или учетной записи Майкрософт (например, bing.com, office.com, msn.com, outlook.com).<br>Примечание. Чтобы использовать эту функцию, пользователю может потребоваться выйти, а затем снова войти в систему, если вход был выполнен в версии Microsoft Edge ниже 88.
  - Автоматическое переключение пользователей macOS на рабочий профиль для сайтов, на которых проверка подлинности выполняется с помощью рабочей учетной записи. Начиная с Microsoft Edge версии 88, мы предоставляем возможность переключения между сайтами, на которых проверка подлинности выполняется с помощью рабочего профиля пользователя в macOS.<br>Примечание. Чтобы использовать эту функцию, пользователю может потребоваться выйти, а затем снова войти в систему, если вход был выполнен в версии Microsoft Edge ниже 88.

- **Возможность завершения сеанса в режиме терминала**. Кнопка "Завершить сеанс" теперь доступна при открытом просмотре в режиме терминала. Эта возможность обеспечивает удаление данных и параметров браузера при закрытии Microsoft Edge. Подробнее о возможностях и дорожной карте режима терминала см. в статье [Настройка режима терминала Microsoft Edge.](./microsoft-edge-configure-kiosk-mode.md)

- **Безопасность и конфиденциальность:**

  - Оповещения создаются в том случае, если пароль пользователя обнаружен среди украденных данных в Интернете. Пароли пользователей сверяются с репозиторием известных украденных учетных данных, а пользователю отправляется оповещение при обнаружении совпадения. Для обеспечения безопасности и конфиденциальности пароли пользователей хэшируются и шифруются, когда они сверяются с базой данных, содержащей украденные учетные данные.
  - Автоматическое обновление смешанного содержимого. Защищенные страницы, доставляемые по протоколу HTTPS, могут содержать ссылки на изображения, которые обслуживаются по незащищенному протоколу HTTP. Чтобы повысить конфиденциальность и безопасность в Microsoft Edge версии 88, эти изображения будут извлекаться по протоколу HTTPS. Если изображение недоступно по протоколу HTTPS, оно не будет загружено.
  - Просмотр разрешений сайта по сайту и по недавним действиям. Начиная с Microsoft Edge версии 88, пользователям будет легче управлять разрешениями сайта. Они смогут просматривать разрешения по веб-сайту, а не только по типу разрешения. Кроме того, мы добавили раздел недавних действий, в котором пользователь сможет просмотреть все последние изменения, внесенные в разрешения сайта.
  - Улучшение контроля над файлами cookie браузера. Начиная с Microsoft Edge версии 88, пользователи могут удалять сторонние файлы cookie, не затрагивая основные файлы cookie. Пользователи также смогут фильтровать файлы cookie по отправителю (основные и сторонние) и сортировать их по имени, количеству и объему данных, которые были сохранены или изменены в последний раз.

- **Производительность:**

  - Повышение производительности браузера с помощью спящих вкладок. Функция спящих вкладок повышает производительность браузера, переводя неактивные вкладки в спящий режим, чтобы освободить системные ресурсы, такие как память и процессор, и использовать их для активных вкладок или других приложений. Пользователи могут предотвратить переход сайтов в спящий режим и настроить время, по истечении которого неактивная вкладка перейдет в спящий режим. Чтобы пользователи могли оставаться в потоке, существуют также эвристические методы, которые предотвращают переход определенных сайтов, например сайтов интрасети, в спящий режим. Эта возможность доступна только случайно выбранной группе пользователей, участвующих в эксперименте. Мы планируем активировать функцию спящих вкладок в Microsoft Edge версии 89 по умолчанию. Управлять этой возможностью можно с помощью групповых политик.
  - Увеличение скорости запуска Microsoft Edge с помощью функции ускорения запуска. Чтобы повысить скорость запуска Microsoft Edge, мы разработали функцию ускорения запуска. Ускорение запуска Microsoft Edge возможно благодаря работе браузера в фоновом режиме. Примечание. Эта возможность доступна только случайно выбранной группе пользователей, участвующих в эксперименте. Эти пользователи предоставляют отзывы службе поддержки.

- **Эффективная работа:**

  - Улучшение эффективности работы и многозадачности с помощью вертикальных вкладок. По мере роста числа горизонтальных вкладок названия сайтов обрезаются, а элементы управления вкладками теряются в уменьшенных вкладках. Это прерывает рабочий процесс пользователей, так как они тратят больше времени на поиск, переключение и управление вкладками и меньше времени на текущую задачу. Функция вертикальных вкладок позволяет пользователям перемещать вкладки в сторону, а вертикально выровненные значки и более длинные заголовки сайтов упрощают быстрое сканирование, идентификацию и переключение на нужную вкладку.
  - Автоматическое заполнение поля даты рождения. Microsoft Edge позволяет экономить время и усилия при заполнении форм и создании учетных записей в Интернете, автоматически заполняя данные пользователя, такие как адрес, имя, номер телефона и т. д. Теперь Microsoft Edge предоставляет поддержку и для поля даты рождения, данные в котором пользователи могут сохранить и автоматически заполнять. Пользователь может просматривать, изменять и удалять эти сведения в любое время в параметрах своего профиля.
  - Улучшения для раздела "Недавно закрытые" в журнале. Теперь раздел "Недавно закрытые" включает последние 25 вкладок и окон из любых сеансов просмотра, а не только из предыдущего сеанса. Пользователи могут выбрать раздел "Недавно закрытые" в новом интерфейсе журнала, чтобы просмотреть все открытые вкладки.
  - Функция "Ваш день в двух словах" включена по умолчанию. Начиная с Microsoft Edge версии 88, информационные работники могут воспользоваться интеллектуальными функциями повышения производительности на странице "Новая вкладка" (NTP). Мы предлагаем пользователям, которые вошли в рабочую или учебную учетную запись, персонализированный и актуальный контент на основе Microsoft 365 Graph. Пользователи могут быстро просмотреть модули "Ваш день в двух словах", чтобы легко отслеживать встречи и недавние задачи, а также быстро запускать приложения, которые они хотят использовать.

- **PDF:**

  - Отображение PDF-документа в виде книги (две страницы). Начиная с Microsoft Edge версии 88, пользователи могут просматривать PDF-документы в одностраничном или двухстраничном представлении книги. Чтобы изменить представление, нажмите кнопку **Просмотр страницы** на панели инструментов.
  - Поддержка привязанных текстовых заметок для PDF-файлов. Начиная с Microsoft Edge версии 87, пользователи могут добавлять набранные текстовые заметки к любому фрагменту текста в PDF-файлах.
  - Более плавное выделение текста в PDF-документах. Пользователи получат возможность более плавного и последовательного выделения текста в PDF-документах, открытых в Microsoft Edge.
  - Просмотр веб-страниц, сохраненных в виде PDF-файлов, на панели загрузок. Теперь пользователи могут просматривать PDF-файлы, созданные с использованием параметра "Сохранить как PDF" в качестве назначения принтера для веб-страниц, на панели загрузок.

- **Шрифты:**

  - Значки браузера обновляются в соответствии со системой проектирования Fluent Design. В рамках продолжающейся работы над Fluent Design в браузере мы внесли изменения, позволяющие точнее согласовать значки с новой системой значков Майкрософт. Эти изменения затронут многие из пользовательских интерфейсов с действиями, выполняемыми вручную, в том числе вкладки, адресную строку, а также значки навигации и поиска, которые можно найти в различных меню.
  - Улучшенное отображение шрифтов. Отрисовка текста улучшена для достижения большей четкости и уменьшения размытости.

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено шестнадцать новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Добавлены следующие новые политики.

- [BlockExternalExtensions](./microsoft-edge-policies.md#blockexternalextensions) — блокирует установку внешних расширений.
- [InternetExplorerIntegrationLocalFileAllowed](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileallowed) — разрешает запуск локальных файлов в режиме Internet Explorer.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist) — открывает локальные файлы в списке разрешенных расширений файлов в режиме Internet Explorer.
- [InternetExplorerIntegrationLocalFileShowContextMenu](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileshowcontextmenu) — показывает контекстное меню, чтобы открыть ссылку в режиме Internet Explorer.
- [IntranetRedirectBehavior](./microsoft-edge-policies.md#intranetredirectbehavior) — поведение при перенаправлении в интрасети.
- [PrinterTypeDenyList](./microsoft-edge-policies.md#printertypedenylist) — отключает типы принтеров в списке запрещенных.
- [ShowMicrosoftRewards](./microsoft-edge-policies.md#showmicrosoftrewards) — показывает возможности Microsoft Rewards.
- [SleepingTabsEnabled](./microsoft-edge-policies.md#sleepingtabsenabled) — настраивает спящие вкладки.
- [SleepingTabsTimeout](./microsoft-edge-policies.md#sleepingtabstimeout) — устанавливает время ожидания активности фоновой вкладки для функции спящих вкладок.
- [SleepingTabsBlockedForUrls](./microsoft-edge-policies.md#sleepingtabsblockedforurls) — блокирует спящие вкладки на определенных сайтах.
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled) включает ускорение запуска.
- [UpdatePolicyOverride](./microsoft-edge-policies.md#updatepolicyoverride) — определяет, как Центр обновления Microsoft Edge обрабатывает доступные обновления из Microsoft Edge.
- [VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) — настраивает доступность вертикального макета для вкладок в боковой части окна браузера.
- [WebRtcAllowLegacyTLSProtocols](./microsoft-edge-policies.md#webrtcallowlegacytlsprotocols) — разрешает переход на устаревшую версию TLS/DTLS в WebRTC.

#### <a name="deprecated-policies"></a>Нерекомендуемые политики

Ниже приводятся нерекомендуемые политики.

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) — включает упреждающую проверку подлинности.
- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist) — настраивает правила обхода прокси-сервера.
- [ProxyMode](./microsoft-edge-policies.md#proxymode) — настраивает параметры прокси-сервера.
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl) — устанавливает URL-адрес PAC-файла прокси-сервера.
- [ProxyServer](./microsoft-edge-policies.md#proxyserver) — настраивает адрес или URL-адрес прокси-сервера.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) — разрешает WebDriver переопределять несовместимые политики.

#### <a name="obsoleted-policies"></a>Устаревшие политики

Ниже приводятся устаревшие политики.

- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting) — настраивает Adobe Flash по умолчанию.
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls) — разрешает подключаемый модуль Adobe Flash на определенных сайтах.
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls) — блокирует подключаемый модуль Adobe Flash на определенных сайтах.
- [RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode) — расширяет настройку содержимого Adobe Flash на все содержимое.

<!-- end major 88 -->

## <a name="version-87066455-december-3"></a>Версия 87.0.664.55: 3 декабря

Исправлены ошибки и проблемы с производительностью. В этом выпуске поддерживается следующая новая функция.

- **Оповещения создаются в том случае, если пароль пользователя обнаружен среди украденных данных в Интернете**. Пароли пользователей сверяются с репозиторием известных украденных учетных данных, а пользователю отправляется оповещение при обнаружении совпадения. Для обеспечения безопасности и конфиденциальности пароли пользователей хэшируются и шифруются, когда они сверяются с базой данных украденных учетных данных.

## <a name="version-87066452-november-30"></a>Версия 87.0.664.52: 30 ноября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-87066440-november-18"></a>Версия 87.0.664.40: 18 ноября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-87066436-november-16"></a>Версия 87.0.664.36: 16 ноября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-87066430-november-9"></a>Версия 87.0.664.30: 9 ноября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-87066424-november-2"></a>Версия 87.0.664.24: 2 ноября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-87066418-october-26"></a>Версия 87.0.664.18: 26 октября

Исправлены ошибки и проблемы с производительностью.

<!-- begin major 87 -->
## <a name="version-87066412-october-20"></a>Версия 87.0.664.12: 20 октября

### <a name="feature-updates"></a>Обновления компонентов

- **Включение средств конфиденциальности режима терминала**. В версии 87 и в дальнейших версиях Microsoft Edge в режиме терминала появляются средства, которые помогут компаниям обеспечивать конфиденциальность пользовательских данных. Благодаря этим функциям включаются такие возможности, как удаление пользовательских данных при выходе, удаление загруженных файлов и сброс настроенной начальной даты возможности после указанного периода бездействия. Подробнее о [Настройке режима терминала Microsoft Edge](./microsoft-edge-configure-kiosk-mode.md).
- **Включение развертывания ClickOnce по умолчанию**. ClickOnce в Microsoft Edge 87 включен по умолчанию, что позволяет снизить количество барьеров для развертывания организациями программного обеспечения и более эффективного согласования поведения устаревшей версии браузера Microsoft Edge. Начиная с Microsoft Edge 87 состояние "Не настроено" политики ClickOnceEnabled отражает новое состояние ClickOnce по умолчанию "Включено" (по сравнению с предыдущим состоянием по умолчанию "Отключено").
- **Интегрирование продуктивности с настраиваемым, связанным с работой содержимым веб-канала на странице новой вкладки (NTP) организации**. На странице новой вкладки (NTP) организации страница производительности Office 365, предлагаемая пользователям, вошедшим в систему с помощью своей рабочей или учебной учетной записи, объединяется с персонализированными, связанными с работой корпоративными и отраслевыми каналами, организованными на одной странице. Пользователи смогут распознавать знакомое содержимое Office 365 и Поиска (Майкрософт) для бизнеса на платформе Bing. Кроме того, они смогут с легкостью переходить к настраиваемому каналу "My Feed" с содержимым и модулями, которые относятся к пользователю, компании или отрасли пользователя, а также подборке других каналов, к которым организация предоставила доступ. [Подробнее](/microsoft-365/admin/manage/manage-industry-news?preserve-view=true&view=o365-worldwide).

- **Конфиденциальность и безопасность.**

  - Поддержка привязки маркеров TLS для сайтов с настроенной политикой. Привязка маркеров TLS предотвращает атаки, направленные на кражу маркеров, для того, чтобы файлы cookie нельзя было повторно использовать на устройстве, которое не является устройством, на котором они изначально были установлены. При использовании привязки маркеров TLS необходимо задать политику [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) и обеспечить поддержку перечисленными сайтами этой возможности.

- **Поддержка пера в качестве маркера в PDF-файлах.** Пользователи смогут выделять маркером текст в PDF-файле с помощью клавиатуры.

- **Вывод на печать:**

  - При печати на обеих сторонах выберите сторону, на которую вам необходимо перевернуть. При печати на обеих сторонах пользователь может перевернуть лист длинной стороной или короткой стороной.
  - Выбор режима растеризации печати для предприятия. Управление печатью Microsoft Edge на принтере без поддержки PostScript в Windows. Иногда для правильной печати на принтерах без поддержки PostScript необходимо правильно растеризовать задания для печати. Параметры печати — "Полная" и "Быстрая".

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено десять новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Добавлены следующие новые политики.

- [ConfigureFriendlyURLFormat](./microsoft-edge-policies.md#configurefriendlyurlformat) — Настройка формата по умолчанию для URL-адресов, скопированных из Microsoft Edge, и определение доступности пользователям дополнительных форматов.
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) — Включены покупки в Microsoft Edge.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](./microsoft-edge-policies.md#hideinternetexplorerredirectuxforincompatiblesitesenabled) — Скрыты диалоговое окно однократного перенаправления и баннер в Microsoft Edge.
- [KioskAddressBarEditingEnabled](./microsoft-edge-policies.md#kioskaddressbareditingenabled) — Настройка редактирования в адресной строке для общедоступного просмотра в режиме терминала.
- [KioskDeleteDownloadsOnExit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) — Удаление файлов, загруженных в ходе сеанса терминала, при закрытии Microsoft Edge.
- [PasswordRevealEnabled](./microsoft-edge-policies.md#passwordrevealenabled) — Включение кнопки "Показать пароль.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerpreventbhoinstall) — Запрет установки объекта BHO для перенаправления несовместимых сайтов из Internet Explorer в Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerredirectmode) — Перенаправление несовместимых сайтов из Internet Explorer в Microsoft Edge.
- [SpeechRecognitionEnabled](./microsoft-edge-policies.md#speechrecognitionenabled) — Настройка распознавания речи.
- [WebCaptureEnabled](./microsoft-edge-policies.md#webcaptureenabled) - Включение функции захвата веб-страниц в Microsoft Edge.

#### <a name="deprecated-policy"></a>Политика устарела

[NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype) — Настройка взаимодействия с новой вкладкой Microsoft Edge.

#### <a name="obsoleted-policy"></a>Устаревшая политика

[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures) — Повторное включение устаревших функций веб-платформы на ограниченное время (устарело).

<!-- end major 87 -->

## <a name="version-86062243-october-16"></a>Версия 86.0.622.43: 16 октября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-86062236-october-7"></a>Версия 86.0.622.36: 7 октября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-86062231-october-1"></a>Версия 86.0.622.31: 1 октября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-86062228-september-28"></a>Версия 86.0.622.28: 28 сентября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-86062215-september-14"></a>Версия 86.0.622.15: 14 сентября

Исправлены ошибки и проблемы с производительностью.
<!-- major 86 -->
## <a name="version-86062211-september-9"></a>Версия 86.0.622.11: 9 сентября

### <a name="feature-updates"></a>Обновления компонентов

* **Режим Internet Explorer:**

   * Позвольте пользователям применять пользовательский интерфейс (UI) Microsoft Edge для проверки сайтов в режиме Internet Explorer. С Microsoft Edge версии 86 администраторы могут включить параметр пользовательского интерфейса, чтобы пользователи могли загружать вкладки в режиме Internet Explorer для тестирования или в качестве временной меры до того, как сайты будут добавлены в XML-файл списка сайтов.

* **Удаление загрузки с диска с помощью диспетчера загрузок.** Пользователи теперь могут удалять загруженные файлы с диска, не выходя из браузера. Новая функция удаления загрузок находится в контекстном меню панели загрузок или на странице загрузок.

* **Откат к предыдущей версии Microsoft Edge.** Функция отката позволяет администраторам вернуть известную хорошую версию Microsoft Edge, если у вас возникла проблема с последней версией Microsoft Edge.
[Подробнее](edge-learnmore-rollback.md).

* **Принудительное включение синхронизации по умолчанию в организации.**  Администраторы могут включить синхронизацию учетных записей Azure Active Directory (Azure AD) по умолчанию с помощью политики [ForceSync](./microsoft-edge-policies.md#forcesync).

* **Обновления PDF:**

  * Оглавление для PDF-документов. С версии 86 в Microsoft Edge добавлена поддержка оглавления, которое позволяет пользователям легко перемещаться по PDF-документам.
  * Доступ ко всем возможностям PDF на экранах небольшого форм-фактора. Получите доступ ко всем возможностям средства чтения PDF-файлов Microsoft Edge на устройствах с небольшим размером экрана.
  * Поддержка пера в качестве маркера в PDF-файлах. Благодаря этому обновлению пользователи могут использовать собственное цифровое перо для прямого выделения текста в PDF-файлах по аналогии с обычным маркером на листе бумаги.
  * Улучшена прокрутка PDF-документов. Теперь вы сможете наслаждаться прокруткой без запинок при просмотре длинных PDF-документов.

* **Автоматическое переключение профилей в Windows 7, 8 и 8.1.** Автоматическое переключение профилей, в настоящее время доступное в Microsoft Edge в Windows 10, теперь расширено и на более ранние версии Windows (Windows 7, 8 и 8.1). Дополнительные сведения см. в записи блога об [автоматическом переключении профилей](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **Пользователям предлагаются варианты автозаполнения при вводе поискового запроса на веб-сайте надстроек Microsoft Edge.** Автозаполнение помогает пользователям быстро завершать поисковые запросы без необходимости ввода всей строки. Это удобно, так как пользователям не нужно запоминать правильное написание и они могут выбирать из доступных демонстрируемых вариантов.

* **Удаление API кэша приложений HTML5.**  С Microsoft Edge версии 86 устаревший API кэша приложений, позволяющий использовать веб-страницы в автономном режиме, удаляется из Microsoft Edge. Сведения для веб-разработчиков о замене API кэша приложений на служебные сценарии доступны в [документации для веб-разработчиков](https://web.dev/appcache-removal/).  Важно! Вы можете запросить [маркер AppCache OriginTrial](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673), позволяющий сайтам продолжать использовать устаревший API кэша приложений до Microsoft Edge версии 90.

* **Безопасность:**

  * Поддержка безопасной службы DNS (DNS поверх HTTPS).  С Microsoft Edge версии 86 доступны параметры для управления безопасной службой DNS на неуправляемых устройствах. Эти параметры недоступны пользователям управляемых устройств, но ИТ-администраторы могут включать и отключать безопасную службу DNS с помощью групповой политики [dnsoverhttpsmode](./microsoft-edge-policies.md#dnsoverhttpsmode).


* **Добавление настраиваемого изображения на страницу новой вкладки (NTP) с помощью групповой политики.** С Microsoft Edge версии 86 на странице новой вкладки доступна возможность для замены стандартного изображения на настраиваемое изображение, предоставляемое пользователем. Возможность управления свойствами этого изображения также поддерживается групповой политикой.

* **Сопоставление настроенных сочетаний клавиш с VS Code.** Средства разработчика Microsoft Edge теперь поддерживают настройку сочетаний клавиш в средствах разработчика для обеспечения соответствия вашему редактору/IDE. (В Microsoft Edge 84 мы добавили возможность сопоставлять сочетания клавиш средств разработчика с VS Code.)

* **Замена политик [MetricsReportingEnabled]( /DeployEdge/microsoft-edge-policies#metricsreportingenabled) и [SendSiteInformationToImproveServices]( /DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) для более ранних версий Windows и macOS.** Эти политики не рекомендуются в Microsoft Edge версии 86 и станут устаревшими в Microsoft Edge версии 89.<br>
Эти политики заменяются политикой [Разрешить телеметрию](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) в Windows 10 и новой политикой [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) для всех остальных платформ. Это позволит пользователям управлять диагностическими данными, отправляемыми в корпорацию Майкрософт, для Windows 7, 8, 8.1 и macOS.

* **Параметр файлов cookie, используемый по умолчанию: SameSite=Lax**. Чтобы повысить безопасность и конфиденциальность в Интернете, по умолчанию файлы cookie будут обрабатываться с использованием параметра [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite). Это означает, что файлы cookie будут отправляться только в основном контексте и будут пропущены в запросах, отправляемых третьим сторонам. Это изменение может повлиять на совместимость для веб-сайтов, которым требуются файлы cookie для правильной работы сторонних ресурсов. Чтобы разрешить такие файлы cookie, веб-разработчики могут помечать файлы cookie, которые должны настраиваться и отправляться в сторонних контекстах, добавив явные атрибуты `SameSite=none` и `Secure` при настройке файлов cookie. Организации, которые хотят исключить определенные сайты из этого изменения, могут сделать это с помощью политики [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) или отказаться от изменения на всех сайтах с помощью политики [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled).

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено 19 политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [CollectionsServicesAndExportsBlockList](./microsoft-edge-policies.md#collectionsservicesandexportsblocklist) — блокировка доступа к указанному списку служб и целевым объектам экспорта в Коллекциях.
- [DefaultSensorsSetting](./microsoft-edge-policies.md#defaultsensorssetting) — стандартный параметр для датчиков.
- [DefaultSerialGuardSetting](./microsoft-edge-policies.md#defaultserialguardsetting) — управлять использованием API Serial.
- [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) — отправлять обязательные и необязательные диагностические данных об использовании браузера.
- [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) — разрешить доступ к средству Enterprise Mode Site List Manager.
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
- [URLBlocklist](./microsoft-edge-policies.md#urlblocklist) — заблокировать доступ к списку URL-адресов.
- [URLAllowlist](./microsoft-edge-policies.md#urlallowlist) — определить список разрешенных URL-адресов.
- [UserAgentClientHintsEnabled](./microsoft-edge-policies.md#useragentclienthintsenabled) — включение функции клиентских подсказок User-Agent.
- [UserDataSnapshotRetentionLimit](./microsoft-edge-policies.md#userdatasnapshotretentionlimit) — ограничение количества снимков пользовательских данных, сохраняемых для применения в случае аварийного отката.

#### <a name="deprecated-policies"></a>Устаревшие политики

- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) — включить отчеты с данными об использовании и сбоях.
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) — отправка сведений о сайтах для улучшения служб Майкрософт.

#### <a name="obsoleted-policy"></a>Устаревшая политика

[TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) — включение функции безопасности TLS 1.3 для местных якорей доверия.

#### <a name="policy-caption-changed"></a>Изменен заголовок политики

[NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) — включение загораживания собственного окна

#### <a name="policy-description-changed"></a>Изменено описание политики

- [AdsSettingForIntrusiveAdsSites](./microsoft-edge-policies.md#adssettingforintrusiveadssites)
- [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls)
- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled)
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy)
- [AutoImportAtFirstRun](./microsoft-edge-policies.md#autoimportatfirstrun)
- [AutoOpenFileTypes](./microsoft-edge-policies.md#autoopenfiletypes)
- [BrowserSignin](./microsoft-edge-policies.md#browsersignin)
- [ClearBrowsingDataOnExit](./microsoft-edge-policies.md#clearbrowsingdataonexit) 
- [ClickOnceEnabled](./microsoft-edge-policies.md#clickonceenabled)
- [CommandLineFlagSecurityWarningsEnabled](./microsoft-edge-policies.md#commandlineflagsecuritywarningsenabled)
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin)
- [ConfigureShare](./microsoft-edge-policies.md#configureshare)
- [CookiesAllowedForUrls](./microsoft-edge-policies.md#cookiesallowedforurls)
- [CustomHelpLink](./microsoft-edge-policies.md#customhelplink)
- [DefaultCookiesSetting](./microsoft-edge-policies.md#defaultcookiessetting)
- [DefaultGeolocationSetting](./microsoft-edge-policies.md#defaultgeolocationsetting)
- [DefaultImagesSetting](./microsoft-edge-policies.md#defaultimagessetting)
- [DefaultInsecureContentSetting](./microsoft-edge-policies.md#defaultinsecurecontentsetting)
- [DefaultJavaScriptSetting](./microsoft-edge-policies.md#defaultjavascriptsetting)
- [DefaultNotificationsSetting](./microsoft-edge-policies.md#defaultnotificationssetting)
- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting)
- [DefaultPopupsSetting](./microsoft-edge-policies.md#defaultpopupssetting)
- [DefaultSearchProviderEnabled](./microsoft-edge-policies.md#defaultsearchproviderenabled)
- [DefaultWebBluetoothGuardSetting](./microsoft-edge-policies.md#defaultwebbluetoothguardsetting)
- [DefaultWebUsbGuardSetting](./microsoft-edge-policies.md#defaultwebusbguardsetting)
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload)
- [DeveloperToolsAvailability](./microsoft-edge-policies.md#developertoolsavailability)
- [EnableSha1ForLocalAnchors](./microsoft-edge-policies.md#enablesha1forlocalanchors)
- [DownloadRestrictions](./microsoft-edge-policies.md#downloadrestrictions)
- [EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures)
- [WinHttpProxyResolverEnabled](./microsoft-edge-policies.md#winhttpproxyresolverenabled)
- [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol)
- [ExternalProtocolDialogShowAlwaysOpenCheckbox](./microsoft-edge-policies.md#externalprotocoldialogshowalwaysopencheckbox)
- [ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist)
- [ForceBingSafeSearch](./microsoft-edge-policies.md#forcebingsafesearch)
- [ForceYouTubeRestrict](./microsoft-edge-policies.md#forceyoutuberestrict)
- [HomepageIsNewTabPage](./microsoft-edge-policies.md#homepageisnewtabpage)
- [HomepageLocation](./microsoft-edge-policies.md#homepagelocation)
- [InPrivateModeAvailability](./microsoft-edge-policies.md#inprivatemodeavailability)
- [InternetExplorerIntegrationEnhancedHangDetection](./microsoft-edge-policies.md#internetexplorerintegrationenhancedhangdetection)
- [InternetExplorerIntegrationLevel](./microsoft-edge-policies.md#internetexplorerintegrationlevel)
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect)
- [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled)
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled)
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout)
- [NetworkPredictionOptions](./microsoft-edge-policies.md#networkpredictionoptions)
- [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation)
- [NewTabPageSearchBox](./microsoft-edge-policies.md#newtabpagesearchbox)
- [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype)
- [NonRemovableProfileEnabled](./microsoft-edge-policies.md#nonremovableprofileenabled)
- [PasswordProtectionWarningTrigger](./microsoft-edge-policies.md#passwordprotectionwarningtrigger)
- [PasswordProtectionLoginURLs](./microsoft-edge-policies.md#passwordprotectionloginurls)
- [PasswordProtectionChangePasswordURL](./microsoft-edge-policies.md#passwordprotectionchangepasswordurl)
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls)
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls)
- [PreventSmartScreenPromptOverride](./microsoft-edge-policies.md#preventsmartscreenpromptoverride)
- [PreventSmartScreenPromptOverrideForFiles](./microsoft-edge-policies.md#preventsmartscreenpromptoverrideforfiles)
- [ProxyMode](./microsoft-edge-policies.md#proxymode)
- [RegisteredProtocolHandlers](./microsoft-edge-policies.md#registeredprotocolhandlers)
- [RelaunchNotification](./microsoft-edge-policies.md#relaunchnotification)
- [RestoreOnStartup](./microsoft-edge-policies.md#restoreonstartup)
- [RestoreOnStartupURLs](./microsoft-edge-policies.md#restoreonstartupurls)
- [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern)
- [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin)
- [SmartScreenAllowListDomains](./microsoft-edge-policies.md#smartscreenallowlistdomains)
- [SmartScreenEnabled](./microsoft-edge-policies.md#smartscreenenabled)
- [SmartScreenForTrustedDownloadsEnabled](./microsoft-edge-policies.md#smartscreenfortrusteddownloadsenabled)
- [SmartScreenPuaEnabled](./microsoft-edge-policies.md#smartscreenpuaenabled)
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled)
- [TrackingPrevention](./microsoft-edge-policies.md#trackingprevention)
- [WebRtcLocalhostIpHandling](./microsoft-edge-policies.md#webrtclocalhostiphandling)

<!-- end 86 -->

## <a name="version-85056441-august-25"></a>Версия 85.0.564.41: 25 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-85056440-august-21"></a>Версия 85.0.564.40: 21 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-85056436-august-17"></a>Версия 85.0.564.36: 17 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-85056430-august-10"></a>Версия 85.0.564.30: 10 августа

Исправлены ошибки и проблемы с производительностью.

## <a name="version-85056423-august-3"></a>Версия 85.0.564.23: 3 августа

Исправлены ошибки и проблемы с производительностью.
<!-- major 85 -->
## <a name="version-85056418-july-28"></a>Версия 85.0.564.18: 28 июля

### <a name="feature-updates"></a>Обновления компонентов

- **Локальная синхронизация элементов "Избранное" и "Параметры"**. Теперь вы можете синхронизировать избранные элементы браузера и параметры между профилями Active Directory в собственной среде без необходимости синхронизации с облаком.

- **Поддержка групповой политики Microsoft Edge для комбинаций "доверенный веб-сайт + приложение" для запуска без запроса подтверждения.** Добавлена поддержка групповой политики, которая позволяет администраторам добавлять комбинации "доверенный веб-сайт + приложение", которые можно запускать без запроса подтверждения. Это позволяет администраторам настраивать комбинации доверенных протоколов и источников данных (например, Microsoft 365), чтобы конечные пользователи могли подавить запрос на подтверждение при переходе по URL-адресу, содержащему протокол приложения.

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
- [EnableSha1ForLocalAnchors](./microsoft-edge-policies.md#enablesha1forlocalanchors) — Разрешение сертификатов, подписанных с помощью SHA-1 при выдаче локальными якорями доверия. <!--- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](./microsoft-edge-policies.md#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains. -->
- [IntensiveWakeUpThrottlingEnabled](./microsoft-edge-policies.md#intensivewakeupthrottlingenabled) - Управление функцией IntensiveWakeUpThrottling.
- [NewTabPagePrerenderEnabled](./microsoft-edge-policies.md#newtabpageprerenderenabled) - Включение предварительной загрузки страницы новой вкладки для ускорения отрисовки.
- [NewTabPageSearchBox](./microsoft-edge-policies.md#newtabpagesearchbox) - Настройка интерфейса поля поиска на странице новой вкладки.
- [PasswordMonitorAllowed](./microsoft-edge-policies.md#passwordmonitorallowed) - Разрешение отправки оповещений пользователям, если их пароли окажутся небезопасными.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled) - Разрешение использования перемещаемых копий для данных профиля Microsoft Edge.
- [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation) - Настройка каталога перемещаемого профиля.
- [TLSCipherSuiteDenyList](./microsoft-edge-policies.md#tlsciphersuitedenylist) - Выбор наборов шифров TLS для отключения.

#### <a name="obsoleted-policies"></a>Устаревшие политики

- [EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) - Разрешение загрузки действий домена из Microsoft.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) — повторное включение API веб-компонентов v0 до M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies)- Разрешение WebDriver переопределять несовместимые политики.

<!--- END ---->

## <a name="version-84052235-july-9"></a>Версия 84.0.522.35: 9 июля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-84052228-june-26"></a>Версия 84.0.522.28: 26 июня

Исправлены ошибки и проблемы с производительностью.

## <a name="version-84052226-june-24"></a>Версия 84.0.522.26: 24 июня

Исправлены ошибки и проблемы с производительностью.

## <a name="version-84052220-june-15"></a>Версия 84.0.522.20: 15 июня

Исправлены ошибки и проблемы с производительностью.

## <a name="version-84052215-june-8"></a>Версия 84.0.522.15: 8 июня

Исправлены ошибки и проблемы с производительностью.

## <a name="version-84052211-june-2"></a>Версия 84.0.522.11: 2 июня

### <a name="feature-updates"></a>Обновления компонентов

- Эта версия Microsoft Edge обеспечивает оптимизированное время скачивания списка сайтов для режима Internet Explorer.  Мы сократили задержку скачивания для списка сайтов в режиме Internet Explorer до 0 секунд (с 60-секундного ожидания) при отсутствии кэшированного списка сайтов. Мы также добавили поддержку групповой политики для случаев, когда требуется задержка перехода на домашнюю страницу режима Internet Explorer, пока скачивается список сайтов. Дополнительные сведения см. в политике [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload).

- Microsoft Edge теперь позволяет пользователям входить в браузер, если он "запущен от имени администратора" в Windows 10. Это помогает пользователям, использующим Microsoft Edge в Windows Server или в сценариях удаленного рабочего стола и песочницы.

- Microsoft Edge теперь обеспечивает полную поддержку мыши в полноэкранном режиме. Теперь с помощью мыши вы можете получить доступ к вкладкам, адресной строке и другим элементам, не выходя из полноэкранного режима.

- Улучшение покупок в Интернете. Добавляйте собственные псевдонимы для сохраненных дебетовых и кредитных карт. Теперь вы можете отличать свои кредитные карты при совершении покупок в Интернете. Присвоение псевдонима для дебетовой или кредитной карты позволяет выбрать правильную карту при использовании автозаполнения для выбора способа оплаты.

- Протоколы TLS/1.0 и TLS/1.1 отключены по умолчанию. Для обнаружения затронутых сайтов можно установить флаг *edge://flags/#display-legacy-tls-warnings*, чтобы Microsoft Edge выводил неблокирующее уведомление "Небезопасно" при загрузке страниц, требующих устаревшие протоколы TLS. Политика [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin) позволяет повторно включить протокол TLS/1.0 и TLS/1.1. Эта политика будет доступна как минимум до Microsoft Edge версии 88. Дополнительные сведения см. в статье [Изменения, вносимые в Microsoft Edge, которые влияю на совместимость сайтов](/microsoft-edge/web-platform/site-impacting-changes).

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

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено пять новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [AppCacheForceEnabled](./microsoft-edge-policies.md#appcacheforceenabled) — разрешает повторное включение компонента AppCache, даже если он отключен по умолчанию.
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy) — прокси-сервер контейнера Application Guard.
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) — требование наличия списка сайтов в режиме предприятия перед навигацией по вкладкам.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) — включить скрытие родной Windows.
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout) — установка времени ожидания для навигации по вкладкам списка сайтов в режиме предприятия.

#### <a name="deprecated-policies"></a>Устаревшие политики

- [AllowSyncXHRInPageDismissal](./microsoft-edge-policies.md#allowsyncxhrinpagedismissal) — разрешение страницам отправлять синхронные запросы XHR при удалении страницы.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) — определяет, используется ли встроенное средство проверки сертификатов для проверки сертификатов серверов.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) — включение более строгой обработки для смешанного контента.

#### <a name="obsoleted-policy"></a>Устаревшая политика

[ForceNetworkInProcess](./microsoft-edge-policies.md#forcenetworkinprocess) — принудительный запуск сетевого кода в процессе браузера.

<!-- end 84 -->

## <a name="version-83047844-june-1"></a>Версия 83.0.478.44: 1 июня

Исправлены ошибки и проблемы с производительностью.

## <a name="version-83047837-may-20"></a>Версия 83.0.478.37: 20 мая

Исправлены ошибки и проблемы с производительностью.

## <a name="version-83047833-may-15"></a>Версия 83.0.478.33: 15 мая

Исправлены ошибки и проблемы с производительностью.

## <a name="version-83047828-may-7"></a>Версия 83.0.478.28: 7 мая

Исправлены ошибки и проблемы с производительностью.

## <a name="version-83047825-may-4"></a>Версия 83.0.478.25: 4 мая

Исправлены ошибки и проблемы с производительностью.

## <a name="version-83047818-april-27"></a>Версия 83.0.478.18: 27 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-83047813-april-22"></a>Версия 83.0.478.13: 22 апреля

### <a name="feature-updates"></a>Обновления компонентов

- Усовершенствования фильтра SmartScreen в Microsoft Defender: реализован ряд улучшений службы фильтра SmartScreen в Microsoft Defender, включая улучшенную защиту от вредоносных сайтов с перенаправлением при загрузке и блокирование фреймов верхнего уровня, полностью заменяющее вредоносные сайты страницей безопасности фильтра SmartScreen в Microsoft Defender. Функция блокирования фрейма верхнего уровня запрещает воспроизведение звука и других данных мультимедиа с вредоносного сайта, за счет чего повышается удобство и снижается путаница.

- Пользователи теперь могут исключить некоторые файлы cookie из автоматического удаления при закрытии браузера. Эта возможность добавлена на основе отзывов пользователей. Этот вариант пригодится, если пользователи не хотят выходить с определенного сайта, но при этом хотят удалить все остальные файлы cookie при закрытии браузера. Чтобы использовать эту функцию, перейдите по адресу *edge://settings/clearBrowsingDataOnClose* и включите переключатель "Файлы cookie и другие данные сайтов".

- Теперь доступна функция автоматического переключения профилей для более удобного доступа к рабочему содержимому. Если на работе вы используете несколько профилей, можно проверить работу этой функции: достаточно зайти с личным профилем на сайт, на котором требуется проверка подлинности с рабочей или учебной учетной записью. Когда мы обнаружим изменение, вы получите предложение переключиться на рабочий профиль, чтобы получить доступ к сайту, не проходя проверку подлинности. Когда вы выберете рабочий профиль, на который нужно переключиться, веб-сайт откроется в вашем рабочем профиле. Надеемся, что такой подход поможет вам отделить рабочие данные от личных и удобнее получать доступ к рабочему содержимому. Если вы не хотите, чтобы эта функция предлагала вам переключить профиль, можно выбрать "Больше не спрашивать", тогда эти запросы не будут отображаться.

- Улучшения функции коллекций:
  - Можно перетаскивать элементы в коллекцию, не открывая ее. При перетаскивании можно выбрать место в списке коллекции, в которое нужно поместить элемент.
  - Можно добавлять сразу несколько элементов в коллекцию, а не только по одному. Чтобы добавить несколько элементов, выделите их и перетащите в коллекцию. Также можно выделить элементы, щелкнуть их правой кнопкой мыши и выбрать коллекцию, в которую нужно их поместить.

- Можно добавить все вкладки в окне Edge в коллекцию без необходимости добавлять их по отдельности. Чтобы добавить все вкладки, щелкните любую вкладку правой кнопкой мыши и выберите "Добавить все вкладки в новую коллекцию".

- Теперь доступна синхронизация расширений. Можно синхронизировать расширения на всех устройствах. С Microsoft Edge синхронизируются расширения из Microsoft Store и Chrome Store. Чтобы использовать эту функцию, щелкните многоточие (**…**) в строке меню и выберите **Параметры**. Щелкните **Синхронизация** в вашем профиле, чтобы открыть варианты синхронизации. Используйте переключатель в разделе **Профили/Синхронизация**, чтобы включить расширения. Можно отключить синхронизацию расширений с помощью групповой политики [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled).

- Улучшено сообщение на странице управления загрузкой для заблокированных небезопасных загруженных файлов.

- Усовершенствования иммерсивного средства чтения:
  - добавлена поддержка наречий в инструменте иммерсивного средства чтения "Части речи". При чтении статьи с помощью иммерсивного средства чтения откройте средства проверки правописания и выберите наречия в разделе "Части речи", чтобы выделить все наречия на странице.
  - Добавлена возможность выбрать любое содержимое на веб-странице и открыть его в иммерсивном средстве чтения. Эта возможность позволяет пользователям использовать иммерсивное средство чтения, а также все средства обучения, такие как "Выделение строк" и "Прочесть вслух", на всех веб-сайтах.

- Неправильно введенный пользователями URL-адрес поможет исправить средство для исправления ссылок, которое корректирует узел и поисковый запрос. Например: <br>
Пользователь по ошибке вводит "powerbi" как "powerbbi".com. Средство для исправления ссылок предложит вариант "powerbi".com в качестве откорректированного варианта и создаст ссылку на поиск "powerbbi" на случай, если пользователь ищет что-то другое.

- Разрешите пользователям сохранять свое решение о запуске внешний протокол для определенного сайта. Чтобы включить или отключить эту функцию, пользователи могут настроить политику [ExternalProtocolDialogShowAlwaysOpenCheckbox](/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox).

- Microsoft Edge можно задать в качестве браузера по умолчанию непосредственно в **параметрах** Microsoft Edge. Эта возможность упрощает для пользователей изменение браузера, используемого по умолчанию, — можно сделать это из самого браузера вместо того, чтобы искать эту возможность в параметрах операционной системы. Чтобы использовать эту функцию, перейдите на *edge://settings/defaultBrowser* и нажмите **Сделать браузером по умолчанию**.

- Несколько обновлений средств разработчика, в том числе новая удаленная поддержка отладки, улучшения пользовательского интерфейса и многое другое. Дополнительные сведения см. в статье [Новые возможности средств разработчика (Microsoft Edge 83)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

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
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) — включить скрытие родной Windows.

#### <a name="deprecated-policy"></a>Политика устарела

Следующая политика продолжит работать в этом выпуске. Она станет устаревшей в будущем выпуске.

[EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) — включение скачивания действий с доменами в Майкрософт

<!--  end 83 -->

## <a name="version-81041660-april-20"></a>Версия 81.0.416.60: 20 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-81041658-april-17"></a>Версия 81.0.416.58: 17 апреля

Обновления для системы безопасности

## <a name="version-81041650-april-10"></a>Версия 81.0.416.50: 10 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-81041645-april-3"></a>Версия 81.0.416.45: 3 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-81041641-march-30"></a>Версия 81.0.416.41: 30 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-81041634-march-17"></a>Версия 81.0.416.34: 17 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-81041631-march-12"></a>Версия 81.0.416.31: 12 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-81041628-march-9"></a>Версия 81.0.416.28: 9 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-81041620-february-28"></a>Версия 81.0.416.20: 28 февраля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-81041612-february-20"></a>Версия 81.0.416.12: 20 февраля

### <a name="feature-updates"></a>Обновления компонентов

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

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено 12 новых политик Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled) — включение внешней проверки подлинности для InPrivate и гостевых профилей. 
- [AudioSandboxEnabled](./microsoft-edge-policies.md#audiosandboxenabled) — разрешение запускать Audio Sandbox.
- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) — использование политики источника ссылки no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](./microsoft-edge-policies.md#globallyscopehttpauthcacheenabled) — включение глобального кэша HTTP-авторизации.
- [ImportExtensions](./microsoft-edge-policies.md#importextensions) — разрешение импорта расширений.
- [ImportCookies](./microsoft-edge-policies.md#importcookies) — разрешение импорта файлов cookie.
- [ImportShortcuts](./microsoft-edge-policies.md#importshortcuts) — разрешение импорта ярлыков.
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect) — указание, как будут действовать переходы в пределах страницы на ненастроенные сайты, начинаемые со страниц в режиме Internet Explorer.
- [OmniboxMSBProviderEnabled](./microsoft-edge-policies.md) — включение поставщика Поиска (Майкрософт) для бизнеса в омнибоксе.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) — включение более строгой обработки для смешанного контента.
- [TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) — включение функции безопасности TLS 1.3 для местных якорей доверия.
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin) — настройка автоматического входа с помощью учетной записи домена Active Directory при отсутствии учетной записи домена Azure AD.

#### <a name="deprecated-policies"></a>Устаревшие политики

В этом выпуске продолжают действовать следующие политики. Они станут устаревшими в будущем выпуске.

- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) — повторное включение API веб-компонентов v0 до M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) — разрешение WebDriver переопределять несовместимые политики.

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)