---
title: Заметки о выпуске Microsoft Edge для стабильного канала
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 04/07/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для стабильного канала
ms.openlocfilehash: 0cf9c2d0ac7a60c03ad6c80d4186629d296a73c6
ms.sourcegitcommit: dd8cdbd35726c795ddce917e549ddf17ee7f5290
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/11/2022
ms.locfileid: "12473669"
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

## <a name="version-1000118536-april-7"></a>Версия 100.0.1185.36: 7 апреля

Обновления безопасности канала Stable перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#april-7-2022).

## <a name="version-1000118529-april-1"></a>Версия 100.0.1185.29: 1 апреля

Обновления безопасности канала Stable перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#april-1-2022).

### <a name="feature-updates"></a>Обновления компонентов

- **Трехзначный номер версии в строке агента пользователя.** Microsoft Edge теперь будет отправлять трехзначный номер версии, например Edg/100, в заголовке User-Agent. Это может привести к путанице в сценариях или аналитике на стороне сервера, которые используют синтаксический анализатор с ошибками для определения номера версии строки User-Agent. Вы можете использовать политику [ForceMajorVersionToMinorPositionInUserAgent](/deployedge/microsoft-edge-policies#forcemajorversiontominorpositioninuseragent), чтобы определить, должна ли основная версия строки user-Agent быть заморожена на 99. Кроме того, флаг **#force-major-version-to-minor**доступен в *edge://flags*, чтобы заморозить основную версию в строке User-Agent до 99.

- **Оптимизация активаций протокола приложений Microsoft 365.** Активация протокола приложений Microsoft 365 в доверенных службах облачного хранилища Microsoft теперь будет запускать определенные приложения Microsoft 365 напрямую, включая поддомены SharePoint и URL-адреса Microsoft OneDrive. С помощью политик [AutoLaunchProtocolsComponentEnabled](/deployedge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) и [AutoLaunchProtocolsFromOrigins](/deployedge/microsoft-edge-policies#autolaunchprotocolsfromorigins) можно включить запросы активации протокола приложения, а также определить другие приложения и службы, для которых включены или отключены предупреждения.

- **Принудительная аппаратная защита стека.** Microsoft Edge продолжает поддерживать более тонкую защиту, борясь с уязвимостями повреждения памяти и защищая непрямые вызовы. Аппаратная защита стека поддерживается только в Windows 8 и более поздних версиях. Дополнительные сведения см. в разделе [Аппаратная защита стека](https://techcommunity.microsoft.com/t5/windows-kernel-internals-blog/developer-guidance-for-hardware-enforced-stack-protection/ba-p/2163340). Поведением этой функции можно управлять с помощью политики [ShadowStackCrashRollbackBehavior](/deployedge/microsoft-edge-policies#shadowstackcrashrollbackbehavior).

- **Предварительный просмотр PDF-файлов в Microsoft Outlook и проводнике.** Пользователи могут просматривать PDF-файлы в облегченной и полной предварительной версии, доступной только для чтения. Эта функция доступна для вложений PDF-файлов в классической версии Outlook или для локальных файлов PDF с помощью проводника.

- **Открытие PDF-файлов с цифровой подписью.** Цифровые подписи широко используются для проверки подлинности документа и внесенных в него изменений. Вы можете использовать политику [PDFSecureMode](/deployedge/microsoft-edge-policies#pdfsecuremode), чтобы включить проверку цифровой подписи для PDF-файлов непосредственно из браузера без необходимости в надстройках.

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

- [AdsTransparencyEnabled](/DeployEdge/microsoft-edge-policies#adstransparencyenabled) — указывает, включена ли функция прозрачности рекламы
- [DefaultWebHidGuardSetting](/DeployEdge/microsoft-edge-policies#defaultwebhidguardsetting) — управляет использованием API WebHID
- [HideRestoreDialogEnabled](/DeployEdge/microsoft-edge-policies#hiderestoredialogenabled) — скрывает диалоговое окно "Восстановление страниц" после сбоя браузера
- [PDFSecureMode](/DeployEdge/microsoft-edge-policies#pdfsecuremode) — безопасный режим и проверка цифровых подписей на основе сертификатов в собственном средстве чтения файлов PDF
- [PromptOnMultipleMatchingCertificates](/DeployEdge/microsoft-edge-policies#promptonmultiplematchingcertificates) — предлагает пользователю выбрать сертификат при совпадении нескольких сертификатов
- [WebHidAskForUrls](/DeployEdge/microsoft-edge-policies#webhidaskforurls) — разрешает API WebHID на этих сайтах
- [WebHidBlockedForUrls](/DeployEdge/microsoft-edge-policies#webhidblockedforurls) — блокирует API WebHID на этих сайтах

#### <a name="deprecated-policy"></a>Политика устарела

- [BackgroundTemplateListUpdatesEnabled](/DeployEdge/microsoft-edge-policies#backgroundtemplatelistupdatesenabled) — включение фоновых обновлений в списке доступных шаблонов для коллекций и других функций, которые используют шаблоны

#### <a name="obsoleted-policy"></a>Устаревшая политика

- [AllowSyncXHRInPageDismissal](/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal) — разрешение страницам отправлять синхронные запросы XHR при удалении страницы

## <a name="version-980110892-march-26"></a>Версия 98.0.1108.92: 26 марта

Исправлены различные ошибки и проблемы с производительностью для выпуска "Расширенный стабильный".

## <a name="version-990115055-march-26"></a>Версия 99.0.1150.55: 26 марта

> [!Important]
> В этом обновлении содержится исправление уязвимости [CVE-2022-1096](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-1096), которая, как сообщают разработчики Chromium, используется на практике. Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide).

Обновления безопасности канала Stable перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#march-26-2022).

## <a name="version-990115052-march-24"></a>Версия 99.0.1150.52: 24 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-980110884-march-17"></a>Версия 98.0.1108.84: 17 марта

Исправлены различные ошибки и проблемы с производительностью для выпуска "Расширенный стабильный".

## <a name="version-990115046-march-17"></a>Версия 99.0.1150.46: 17 марта

Обновления безопасности канала Stable перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#march-17-2022).

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

<!---- From Version 97.0.1072.55: January 6 to Version 96.0.1054.34: November 23 ---->
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
