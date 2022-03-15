---
title: Заметки о выпуске Microsoft Edge для канала Beta
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 03/14/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для канала Beta
ms.openlocfilehash: 8633a5f15fe737a64a0160de714c1c4e53541482
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445713"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Заметки о выпуске для Microsoft Edge из канала Beta

Эти заметки о выпуске содержат сведения о новых возможностях и обновлениях, не связанных с безопасностью, которые включены Microsoft Edge канала Beta Архивные версии этих записей выпуска доступны в архивных заметках для [Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> Веб-платформа Microsoft Edge постоянно развивается для улучшения взаимодействия с пользователями, безопасности и конфиденциальности. Дополнительные сведения см. в статье [Изменения в Microsoft Edge, затрагивающие совместимость сайтов](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-990115039-march-10"></a>Версия 99.0.1150.39: 10 марта

### <a name="feature-updates"></a>Обновления компонентов

- **Улучшения в области управления списками облачных сайтов для режима IE.** Определите пробелы в списке корпоративных сайтов, настроив отчеты о отзывах на сайте с помощью политик [InternetExplorerIntegrationCloudUserSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) и [InternetExplorerIntegrationCloudNeutralSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) . Вы можете просматривать локальные URL-адреса списков сайтов от пользователей и потенциально неправильно сконфигурировали нейтральные URL-адреса сайтов в Microsoft Edge списков сайтов в центре Microsoft 365 Admin. Дополнительные дополнительные комментарии см. в обзоре отзывов на [сайте центра Microsoft 365 Admin.](/deployedge/edge-ie-mode-cloud-site-list-mgmt#view-site-feedback-on-the-microsoft-365-admin-center-1)  **Примечание:** Это управляемый выкат функции. Если вы не видите эту функцию, проверьте, как мы продолжаем нашу выкатку.

## <a name="version-990115030-march-2"></a>Версия 99.0.1150.30: 2 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-990115025-february-25"></a>Версия 99.0.1150.25: 25 февраля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-990115021-february-22"></a>Версия 99.0.1150.21: 22 февраля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-990115016-february-14"></a>Версия 99.0.1150.16: 14 февраля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-990115011-february-9"></a>Версия 99.0.1150.11: 9 февраля

### <a name="feature-updates"></a>Обновления компонентов

- **Предстоящий трехзначный номер версии в строке агента пользователя.** Начиная с версии 100, Microsoft Edge отправит трехзначный номер версии в User-Agent, например "Edg/100". Начиная с Microsoft Edge 97, владельцы сайтов могут протестировать эту строку предстоящих агентов, включив флаг эксперимента **#force-major-version-to-100** в edge://flags, чтобы убедиться, что их логика User-Agent разметки надежна и работает, как и *ожидалось*.

- **Персонализация многопрофиальных опытом с предпочтениями профилей для сайтов.** Пользователи могут настроить свой многопрофиальный опыт с возможностью создания настраиваемого списка сайтов для автоматического переключения профилей в Microsoft Edge.

- **Bidirectional Cookie Sharing for IE mode.** Эта функция расширяет возможности обмена файлами cookie, которые уже доступны, и позволяет пользователям синхронизировать определенные файлы cookie сеанса из режима Internet Explorer/IE в Microsoft Edge. Дополнительные сведения см. в разделе [Cookie sharing between Microsoft Edge и Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

- **Перейдите по pdf-документам с помощью эскизов страниц.** Теперь вы сможете перемещаться по документу PDF с помощью эскизов, которые представляют страницы. Эти эскизы будут отображаться в области слева от читателя PDF.

- **Настройте список доменов, для которых будет отключен пользовательский интерфейс диспетчера паролей для сохранения и заполнения.** Используйте политику [PasswordManagerBlocklist](/deployedge/microsoft-edge-policies#passwordmanagerblocklist) для настройки списка доменов (только схемы HTTP/HTTPS и имена хостов), в которых Microsoft Edge отключить диспетчер паролей. Это означает, что процессы сохранения и заполнения будут отключены, что гарантирует, что пароли для этих веб-сайтов не могут быть сохранены или автоматически заполнены в веб-формы.

- **Обновление расширений для Microsoft Edge магазина надстройок с помощью API (в публичном предварительном просмотре).** Эти API можно интегрировать непосредственно в конвейер сборки и опубликовать обновления пакетов на веб-сайте Microsoft Edge надстройки. Дополнительные новости см. в [Microsoft Edge API надстройки (в закрытом предварительном просмотре)](/microsoft-edge/extensions-chromium/publish/api/using-addons-api)

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

- [AllowGamesMenu](/DeployEdge/microsoft-edge-policies#allowgamesmenu) — разрешить пользователям доступ к меню игр
- [DoNotSilentlyBlockProtocolsFromOrigins](/DeployEdge/microsoft-edge-policies#donotsilentlyblockprotocolsfromorigins) — определите список протоколов, которые не могут быть молча заблокированы защитой от наводнения
- [HubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#hubssidebarenabled) — боковая панель show Hubs
- [InternetExplorerIntegrationCloudNeutralSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) — настройка отчетов о потенциально неправильно настроенных URL-адресах нейтрального сайта в приложение Списки сайтов центра администрирования M365
- [InternetExplorerIntegrationCloudUserSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) — настройка записей списков пользователей IE Mode в приложение Списки сайтов центра администрирования M365
- [PasswordManagerBlocklist](/DeployEdge/microsoft-edge-policies#passwordmanagerblocklist) — настройка списка доменов, для которых будет отключен пользовательский интерфейс диспетчера паролей (Сохранение и заполнение).
- [RelatedMatchesCloudServiceEnabled](/DeployEdge/microsoft-edge-policies#relatedmatchescloudserviceenabled) — настройка связанных совпадений в поиске на странице
- [SignInCtaOnNtpEnabled](/DeployEdge/microsoft-edge-policies#signinctaonntpenabled) . Включить вход в диалоговое окно действия
- [UserAgentReduction](/DeployEdge/microsoft-edge-policies#useragentreduction) — включить или отключить User-Agent уменьшение

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

- **Повышение безопасности в Интернете.** Режим просмотра в Microsoft Edge, где безопасность браузера имеет приоритет, что дает дополнительный уровень защиты при просмотре веб-страниц. Администраторы могут применять следующие групповые политики к настольным компьютерам конечных пользователей (Windows, macOS и Linux), чтобы защитить от нулевых дней. Эти политики также делают так, чтобы важные сайты и линейка бизнес-приложений работали как и ожидалось. Эта функция является огромным шагом вперед, так как позволяет нам смягчать непредвиденные активные нулевые дни (на основе исторических тенденций). Flow При включенном включите эту функцию в качестве поддержки мер по смягчению последствий безопасности для повышения безопасности пользователей в Интернете.
Групповые политики:
  - [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode)
  - [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains)
  - [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains)

- **Настраиваемый основной пароль.** Браузер уже имеет возможность добавить шаг проверки подлинности до автоматического заполнения сохраненных паролей в веб-формах. Это добавляет еще один уровень конфиденциальности и помогает предотвратить использование сохраненных паролей для входа на веб-сайты. Настраиваемый основной пароль — это эволюция той же функции, в которой пользователи теперь смогут использовать настраиваемую строку выбора в качестве основного пароля. После его включения пользователи введите этот пароль для проверки подлинности и автоматического заполнения сохраненных паролей в веб-формах.

- **Перекладывка прокрутки, добавленная в Microsoft Edge.** Мы обновили наши прокрутки с помощью дизайна на основе наложения. Пользователи могут включить эту функцию в *edge://flags*.

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

- [AddressBarEditingEnabled](/DeployEdge/microsoft-edge-policies#addressbareditingenabled) — настройка редактирования панели адресов.
- [EdgeFollowEnabled](/DeployEdge/microsoft-edge-policies#edgefollowenabled) — включить службу Follow в Microsoft Edge.
- [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode) — повышение состояния безопасности в Microsoft Edge.
- [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains) — настройка списка доменов, для которых не будет применяться усиленный режим безопасности.
- [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains) — настройте список доменов, для которых всегда будет применяться усиленный режим безопасности.
- [InAppSupportEnabled](/DeployEdge/microsoft-edge-policies#inappsupportenabled) — включена поддержка в приложении.
- [MicrosoftEdgeInsiderPromotionEnabled](/DeployEdge/microsoft-edge-policies#microsoftedgeinsiderpromotionenabled) — Microsoft Edge включено продвижение по инсайдерской службе.
- [PrintStickySettings](/DeployEdge/microsoft-edge-policies#printstickysettings) - Печать липких параметров предварительного просмотра.
- [SandboxExternalProtocolBlocked](/DeployEdge/microsoft-edge-policies#sandboxexternalprotocolblocked) — разрешить Microsoft Edge для блокировки навигации по внешним протоколам в песочнице iframe.
- [U2fSecurityKeyApiEnabled](/DeployEdge/microsoft-edge-policies#u2fsecuritykeyapienabled) — разрешить использование API ключа безопасности U2F.

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

<!--- Version 97.0.1072.21: December 1 to Version 96.0.1054.13: November 5  --->
<!--- archive from Version 96.0.1054.8: November 1 to Version 95.0.1020.14: October 5  --->
<!-- archive from version 95.0.1020.9: September 28 to version 94.0.992.14: September 7 ---->
<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive on Oct 27 From Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)

