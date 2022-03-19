---
title: Заметки о выпуске Microsoft Edge для стабильного канала
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 03/10/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для стабильного канала
ms.openlocfilehash: a7e11586c77b600253f25c2819a26e72e18f4b28
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445643"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Заметки о выпуске для стабильного канала Microsoft Edge

Эти заметки о выпуске содержат сведения о новых компонентах и обновлениях, не связанных с безопасностью, которые включены в стабильный канал Microsoft Edge.

- Все обновления для системы безопасности см. в разделе [Заметки о выпуске обновлений для системы безопасности Microsoft Edge](./microsoft-edge-relnotes-security.md).
- Архивные заметки о выпуске для стабильного канала Microsoft Edge см. в разделе [Архивные заметки о выпуске для канала Microsoft Edge Stable](./microsoft-edge-relnote-archive-stable-channel.md).

 Чтобы ознакомиться с каналами Microsoft Edge, см. статью [Обзор каналов Microsoft Edge](./microsoft-edge-channels.md).

> [!NOTE]
> Для канала Stable обновления последовательно разворачиваются в течение одного или нескольких дней. Дополнительные сведения см. в статье [Последовательные развертывания обновлений Microsoft Edge](./microsoft-edge-update-progressive-rollout.md).
>
> Веб-платформа Microsoft Edge постоянно развивается для улучшения взаимодействия с пользователями, безопасности и конфиденциальности. Дополнительные сведения см. в статье [Изменения в Microsoft Edge, затрагивающие совместимость сайтов](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-990115039-march-10"></a>Версия 99.0.1150.39: 10 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-980110876-march-9"></a>Версия 98.0.1108.76: 9 марта

Исправлены различные ошибки и проблемы с производительностью для выпуска "Расширенный стабильный".

## <a name="version-990115036-march-7"></a>Версия 99.0.1150.36: 7 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-990115030-march-3"></a>Версия 99.0.1150.30: 3 марта

Обновления безопасности стабильного канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#march-3-2022).

### <a name="feature-updates"></a>Обновления компонентов

- **Предстоящий трехзначный номер версии в строке агента пользователя.** Начиная с версии 100, Microsoft Edge будет отправлять трехзначный номер версии в заголовке User-Agent, например, "Edg/100". Начиная с Microsoft Edge 97, владельцы сайтов могут протестировать эту строку будущего агента, включив флаг эксперимента **#force-major-version-to-100** в *edge://flags* для обеспечения надежности и работы логики синтаксического анализа User-Agent.

- **Персонализация многопрофильного опыта с помощью предпочтений профиля для сайтов.** Пользователи могут персонализировать работу с несколькими профилями, создав настраиваемый список сайтов для автоматического переключения профилей в Microsoft Edge.

- **Навигация по PDF-документам с помощью эскизов страниц.** Теперь вы сможете перемещаться по PDF-документу с помощью эскизов, которые представляют страницы. Эти эскизы будут отображаться в области в левой части экрана средства чтения PDF-файлов.

- **Настройка списка доменов, для которых пользовательский интерфейс диспетчера паролей для функций "Сохранение" и "Заполнение" будет отключен.** Используйте политику [PasswordManagerBlocklist](/deployedge/microsoft-edge-policies#passwordmanagerblocklist) для настройки списка доменов (только схемы и имена узлов HTTP/HTTPS), в которых Microsoft Edge должен отключить диспетчер паролей. Это означает, что рабочие процессы "Сохранить" и "Заполнить" будут отключены, что позволит не сохранять пароли для этих веб-сайтов или не заполнять их в веб-формы автоматически.

- **Пользовательский основной пароль.** В браузере уже есть возможность, с помощью которой пользователи могут добавить шаг проверки подлинности перед автоматическим заполнением сохраненных паролей в веб-формах. Это добавляет еще один уровень конфиденциальности и помогает предотвратить использование неавторизованными пользователями сохраненных паролей для входа на веб-сайты. Пользовательский основной пароль— это развитие той же функции, где пользователи теперь смогут использовать настраиваемую строку по своему выбору в качестве основного пароля. После включения пользователи будут вводить этот пароль для проверки подлинности и автоматического заполнения сохраненных паролей в веб-формах.

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

- [DoNotSilentlyBlockProtocolsFromOrigins](/DeployEdge/microsoft-edge-policies#donotsilentlyblockprotocolsfromorigins) - Определить список протоколов, которые не могут быть автоматически заблокированы защитой от переполнения
- [ForceMajorVersionToMinorPositionInUserAgent](/DeployEdge/microsoft-edge-policies#forcemajorversiontominorpositioninuseragent) - Включить или отключить заморозку строки User-Agent в основной версии 99
- [HubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#hubssidebarenabled) - Показать боковую панель центров
- [InternetExplorerIntegrationCloudNeutralSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) - Настройка отправки отчетов о потенциально неправильно настроенных URL-адресах нейтральных сайтов в приложение "Списки сайтов" Центра администрирования M365
- [InternetExplorerIntegrationCloudUserSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) - Настройка отправки отчетов о записях списка пользователей в режиме IE в приложение "Списки сайтов" Центра администрирования M365
- [PasswordManagerBlocklist](/DeployEdge/microsoft-edge-policies#passwordmanagerblocklist) - Настройка списка доменов, для которых пользовательский интерфейс диспетчера паролей (сохранение и заполнение) будет отключен
- [RelatedMatchesCloudServiceEnabled](/DeployEdge/microsoft-edge-policies#relatedmatchescloudserviceenabled) - Настройка связанных соответствий в разделе "Найти на странице"
- [SignInCtaOnNtpEnabled](/DeployEdge/microsoft-edge-policies#signinctaonntpenabled) - Включить диалоговое окно входа в систему по щелчку для принятия действий
- [UserAgentReduction](/DeployEdge/microsoft-edge-policies#useragentreduction) - Включение или отключение уменьшения числа агентов пользователей


## <a name="version-980110862-february-24"></a>Версия 98.0.1108.62: 24 февраля

Исправлены различные ошибки и проблемы с производительностью для выпуска "Стабильный" и "Расширенный стабильный".

## <a name="version-980110856-february-17"></a>Версия 98.0.1108.56: 17 февраля

Исправлены различные ошибки и проблемы с производительностью для выпуска "Стабильный" и "Расширенный стабильный".

## <a name="version-980110855-february-16"></a>Версия 98.0.1108.55: 16 февраля

> [!Important]
> В этом обновлении содержится исправление уязвимости [CVE-2022-0609](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-0609), которая, как сообщают разработчики Chromium, используется на практике. Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide).

Обновления безопасности канала Stable перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#february-16-2022).

## <a name="version-980110850-february-10"></a>Версия 98.0.1108.50: 10 февраля

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#february-10-2022).

## <a name="version-980110843-february-3"></a>Версия 98.0.1108.43: 3 февраля

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#february-3-2022).

### <a name="feature-updates"></a>Обновления компонентов

- **Усильте безопасность в Интернете.** Это режим просмотра в Microsoft Edge с приоритетной защитой браузера для более безопасного и надежного просмотра веб-страниц. Администраторы могут применять групповые политики к рабочим столам конечных пользователей (Windows, macOS и Linux), чтобы защититься от эксплойтов, которые также называются эксплойтами 0-го дня. Этот режим просмотра поддерживается следующими групповыми политиками:

  - [EnhanceSecurityMode](/deployedge/microsoft-edge-policies#enhancesecuritymode)
  - [EnhanceSecurityModeBypassListDomains](/deployedge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains)
  - [EnhanceSecurityModeEnforceListDomains](/deployedge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains)

- **Предстоящий трехзначный номер версии в строке агента пользователя.** Начиная с версии 100, Microsoft Edge будет отправлять трехзначный номер версии в заголовке User-Agent, например, "Edg/**100**". Начиная с Microsoft Edge 97, владельцы сайтов могут протестировать эту строку будущего агента пользователя, включив флаг эксперимента **#force-major-version-to-100** в *edge://flags* для обеспечения надежности и работы логики синтаксического анализа User-Agent.

- **Прекратите поддержку семантики SDP плана B WebRTC.** Это изменение делает устаревшим диалект протокола SDP под названием "План B". Этот формат SDP заменяется единым планом, который соответствует спецификациям и совместим с форматом SDP в разных браузерах. Дополнительные сведения см. в записи состояния платформы Chrome [PSA: план B должен запускаться в бета-версии M96 и стабильной версии](https://chromestatus.com/feature/5823036655665152) и [PSA: запуск плана B в конце срока действия пробной версии прекращения поддержки стабильного и расширенного выпуска](https://groups.google.com/g/discuss-webrtc/c/gEHrZyYKsfU). Запрос [Испытания для семантики SDP плана B RTCPeerConnection](https://developer.chrome.com/origintrials/#/view_trial/3892235977954951169) позволяет сайтам продолжать использовать неподдерживаемый API до версии 101.

- **Прокрутки наложения добавлены в Microsoft Edge.** Мы обновили панели прокрутки с помощью дизайна на основе наложения. Пользователи могут включить эту функцию в *edge://flags*.

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

- [AddressBarEditingEnabled](/DeployEdge/microsoft-edge-policies#addressbareditingenabled) - Настройка редактирования адресной строки
- [AllowGamesMenu](/DeployEdge/microsoft-edge-policies#allowgamesmenu) - Разрешить пользователям доступ к меню игр
- [EdgeFollowEnabled](/DeployEdge/microsoft-edge-policies#edgefollowenabled) - Включить службу "Подписаться" в Microsoft Edge
- [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode) - Повышение состояния безопасности в Microsoft Edge
- [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains) - Настройка списка доменов, для которых режим усиленной безопасности не применяется
- [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains) - Настройка списка доменов, для которых режим усиленной безопасности применяется всегда
- [InAppSupportEnabled](/DeployEdge/microsoft-edge-policies#inappsupportenabled) - Поддержка в приложении включена
- [MicrosoftEdgeInsiderPromotionEnabled](/DeployEdge/microsoft-edge-policies#microsoftedgeinsiderpromotionenabled) - Включено продвижение программы предварительной оценки Microsoft Edge
- [PrintStickySettings](/DeployEdge/microsoft-edge-policies#printstickysettings) - Сохраняющиеся параметры предварительного просмотра
- [SandboxExternalProtocolBlocked](/DeployEdge/microsoft-edge-policies#sandboxexternalprotocolblocked) - Разрешить Microsoft Edge блокировать переходы по внешним протоколам в изолированном iframe
- [U2fSecurityKeyApiEnabled](/DeployEdge/microsoft-edge-policies#u2fsecuritykeyapienabled) - Разрешить использование нерекомендуемого API ключа безопасности U2fSecurityKeyApiEnabled

## <a name="version-970107276-january-27"></a>Версия 97.0.1072.76: 27 января

Исправлены ошибки и проблемы с производительностью.

### <a name="feature-updates"></a>Обновления компонентов

- **Предстоящий трехзначный номер версии в строке агента пользователя.** Начиная с версии 100, Microsoft Edge будет отправлять трехзначный номер версии в заголовке User-Agent, например, "Edg/**100**". Начиная с Microsoft Edge 97, владельцы сайтов могут протестировать эту строку будущего агента пользователя, включив флаг эксперимента **#force-major-version-to-100** в *edge://flags* для обеспечения надежности и работы логики синтаксического анализа User-Agent.

## <a name="version-960105475-january-21"></a>Версия 96.0.1054.75: 21 января

Исправлены различные ошибки и проблемы с производительностью для выпуска "Расширенный стабильный".

## <a name="version-970107269-january-20"></a>Версия 97.0.1072.69: 20 января

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#january-20-2022).

## <a name="version-970107262-january-13"></a>Версия 97.0.1072.62: 13 января

Исправлены ошибки и проблемы с производительностью.

## <a name="version-960105472-january-6"></a>Версия 96.0.1054.72: 6 января

Исправлены различные ошибки и проблемы с производительностью для выпуска "Расширенный стабильный".

## <a name="version-970107255-january-6"></a>Версия 97.0.1072.55: 6 января

Обновления безопасности стабильного канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#january-6-2022).

### <a name="feature-updates"></a>Обновления компонентов

- **Используйте текущий профиль для входа на веб-сайты, если на устройстве вошли в систему несколько рабочих и учебных учетных записей.** Если на устройстве осуществлен вход в несколько учетных записей организации или учебного заведения, пользователям будет предложено выбрать учетную запись из средства выбора учетной записи, чтобы продолжить посещения веб-сайтов. В этом выпуске пользователям будет предложено позволить Microsoft Edge автоматически входить на веб-сайты с помощью учетной записи организации или учебного заведения, которая вошла в текущий профиль. Пользователи могут включить и отключить эту функцию в разделе **Параметры** > **Профильные настройки**.

- **Добавьте поддержку защиты от потери данных (DLP) в конечной точке Майкрософт в macOS.** Политика Защиты от потери данных в конечной точке Майкрософт будет доступна непосредственно в macOS.

- **Автоматическое использование HTTPS.** Пользователи могут обновить навигацию с HTTP до HTTPS для доменов, которые, скорее всего, поддерживают этот более безопасный протокол. Эту поддержку также можно настроить так, чтобы попытка доставки по протоколу HTTPS осуществлялась для всех доменов. Примечание. Эта функция входит в состав контролируемого выпуска функций. Если эта функция отсутствует, вернитесь сюда, поскольку выпуск продолжается.

- **Блокировка WebSQL в сторонних контекстах.** Использование устаревшей функции WebSQL будет заблокировано в сторонних фреймах. Политика [WebSQLInThirdPartyContextEnabled](/deployedge/microsoft-edge-policies#websqlinthirdpartycontextenabled) доступна для отказа до Microsoft Edge версии 101. Это изменение осуществляется в проекте Chromium, на котором основан Microsoft Edge. Дополнительные сведения см. в [записи о состоянии платформы Chrome](https://chromestatus.com/feature/5684870116278272).

- **Цитаты в Microsoft Edge.** Учащимся часто необходимо цитировать источники для исследования. Им необходимо управлять множеством справочных материалов и источников, а это непростая задача. Кроме того, им необходимо перевести эти цитаты в соответствующие форматы, такие как APA, MLA и Chicago. Это новая функция "Ссылки", предварительная версия которой доступна в Microsoft Edge, позволяет учащимся лучше управлять цитатами и создавать цитаты по мере исследования в Интернете. Если ссылки включены в коллекциях или из раздела **Параметры и другое (ALT-F)**, Microsoft Edge автоматически создает цитаты, которые учащиеся смогут использовать позже, чтобы они могли сосредоточиться на своих исследованиях. Когда все будет готово, можно будет легко скомпилировать эти цитаты в окончательный результат. Дополнительные сведения см. в статье [Предварительный просмотр цитат в Microsoft Edge](https://blogs.windows.com/msedgedev/2021/11/04/preview-citations-feature-edge/).

- **Защита потока управления (CFG).** Microsoft Edge начнет поддерживать более тонкую защиту, борясь с уязвимостями повреждения памяти и защищая непрямые вызовы. CFG поддерживается только в Windows 8 и более поздних версиях. Дополнительные сведения см. в статье [Защита потока управления](/windows/win32/secbp/control-flow-guard).
  
  > [!NOTE]
  > Это развивающаяся технология. Поделитесь своими отзывами, чтобы помочь нам усилить ее поддержку.

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

## <a name="version-960105462-december-17"></a>Версия 96.0.1054.62: 17 декабря

Исправлены ошибки и проблемы с производительностью.

## <a name="version-960105457-december-14"></a>Версия 96.0.1054.57: 14 декабря

> [!Important]
> В этом обновлении содержится исправление уязвимости [CVE-2021-4102](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-4102), которая, как сообщают разработчики Chromium, используется на практике. Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide).

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#december-14-2021).

## <a name="version-960105453-december-10"></a>Версия 96.0.1054.53: 10 декабря

Обновления безопасности канала Stable перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#december-10-2021).

## <a name="version-960105443-december-2"></a>Версия 96.0.1054.43: 2 декабря

Исправлены ошибки и проблемы с производительностью.

## <a name="version-960105441-november-30"></a>Версия 96.0.1054.41: 30 ноября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-960105434-november-23"></a>Версия 96.0.1054.34: 23 ноября

Исправлены ошибки и проблемы с производительностью.

<!---archive from Version 96.0.1054.29: November 19 to Version 94.0.992.57: October 27 --->
<!-- archive from Version 95.0.1020.30: October 21 to Version 94.0.992.37: September 30 -->
<!-- archive from Version 94.0.992.31: September 24 to Version 93.0.961.44: September 9  -->
<!--- Archive from Version 93.0.961.38: September 2 to Version 92.0.902.62: July 29 --->
<!-- Archive from Version 92.0.902.55: July 22 to Version 91.0.864.37: May 27 -->
<!-- Archive from 89.0.774.45: March 4 to 90.0.818.66: May 20 ->
<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
