---
title: Заметки о выпуске Microsoft Edge для канала Beta
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 04/27/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для канала Beta
ms.openlocfilehash: 41f9efd48fa9afef215c2fd8e6499b2840ec256c
ms.sourcegitcommit: 592f6e40b13e28af588473b2a75c3ae697e5db2d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2022
ms.locfileid: "12505372"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Заметки о выпуске для Microsoft Edge из канала Beta

Эти заметки о выпуске содержат сведения о новых возможностях и обновлениях, не связанных с безопасностью, которые включены Microsoft Edge канала Beta Архивные версии этих заметок о выпуске доступны в архивных заметках о выпуске [Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> Веб-платформа Microsoft Edge постоянно развивается для улучшения взаимодействия с пользователями, безопасности и конфиденциальности. Дополнительные сведения см. в статье [Изменения в Microsoft Edge, затрагивающие совместимость сайтов](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-1010121031-april-27"></a>Версия 101.0.1210.31: 27 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-1010121026-april-22"></a>Версия 101.0.1210.26: 22 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-1010121019-april-18"></a>Версия 101.0.1210.19: 18 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-1010121014-april-12"></a>Версия 101.0.1210.14: 12 апреля

Исправлены ошибки и проблемы с производительностью.

### <a name="feature-updates"></a>Обновления компонентов

- **Усовершенствования в Enterprise Site List Manager.** Теперь вы можете настроить общие файлы cookie между Microsoft Edge и Internet Explorer в списке корпоративных сайтов. Вы можете получить доступ [к Enterprise site List Manager](/deployedge/edge-ie-mode-site-list-manager) по *адресу edge://compat/SiteListManager*.

## <a name="version-1010121010-april-8"></a>Версия 101.0.1210.10: 8 апреля

### <a name="feature-updates"></a>Обновления компонентов

- **Возможность задать профиль по умолчанию.** Политика [EdgeDefaultProfileEnabled](/DeployEdge/microsoft-edge-policies#edgedefaultprofileenabled) позволяет задать профиль по умолчанию, используемый при открытии браузера, а не последний используемый профиль. Эта политика не будет применяться, если `--profile-directory` указан параметр.

- **Коммутатор сертификатов клиента.** Эта функция позволяет пользователям очистить сохраненный сертификат и повторно открыть средство выбора сертификатов при посещении сайта, для которого требуется проверка подлинности http-сертификата. Это можно сделать, не выходя из Microsoft Edge.

- **Запустите прогрессивные веб-приложения (PWA) из панели избранного.** Улучшения в PWA запуска начнут отображаться, начиная со значка "Приложения", который можно добавить на панель инструментов.

- **Управление параметром "Разрешить расширения из других магазинов".** Используйте политику [ControlDefaultStateOfAllowExtensionFromOtherStoresSettingEnabled](/DeployEdge/microsoft-edge-policies#controldefaultstateofallowextensionfromotherstoressettingenabled) , чтобы управлять состоянием по умолчанию параметра "Разрешить расширения из других хранилищ".

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

- [ConfigureKeyboardShortcuts](/DeployEdge/microsoft-edge-policies#configurekeyboardshortcuts) — настройка списка команд, для которых нужно отключить сочетания клавиш
- [ControlDefaultStateOfAllowExtensionFromOtherStoresSettingEnabled](/DeployEdge/microsoft-edge-policies#controldefaultstateofallowextensionfromotherstoressettingenabled) — настройка состояния по умолчанию для разрешения расширений из других хранилищ
- [EdgeAssetDeliveryServiceEnabled](/DeployEdge/microsoft-edge-policies#edgeassetdeliveryserviceenabled) — разрешить функциям скачивать ресурсы из службы доставки ресурсов
- [EdgeDefaultProfileEnabled](/DeployEdge/microsoft-edge-policies#edgedefaultprofileenabled) — включен параметр профиля по умолчанию
- [InternetExplorerModeEnableSavePageAs](/DeployEdge/microsoft-edge-policies#internetexplorermodeenablesavepageas) — разрешить сохранение страницы, как в режиме Internet Explorer
- [KioskSwipeGesturesEnabled](/DeployEdge/microsoft-edge-policies#kioskswipegesturesenabled) — жесты прокрутки в Microsoft Edge режиме киоска
- [MicrosoftOfficeMenuEnabled](/DeployEdge/microsoft-edge-policies#microsoftofficemenuenabled) — разрешить пользователям доступ к Microsoft Office меню
- [SiteSafetyServicesEnabled](/DeployEdge/microsoft-edge-policies#sitesafetyservicesenabled) — разрешить пользователям настраивать службы безопасности сайта

#### <a name="deprecated-policy"></a>Политика устарела

- [ForceCertificatePromptsOnMultipleMatches](/DeployEdge/microsoft-edge-policies#forcecertificatepromptsonmultiplematches) — настройте, следует ли Microsoft Edge автоматически выбирать сертификат при наличии нескольких совпадений сертификатов для сайта, настроенного с помощью AutoSelectCertificateForUrls.

#### <a name="obsoleted-policy"></a>Устаревшая политика

- [WebSQLInThirdPartyContextEnabled](/DeployEdge/microsoft-edge-policies#websqlinthirdpartycontextenabled) - Принудительное повторное включение WebSQL в сторонних контекстах


## <a name="version-1000118527-march-31"></a>Версия 100.0.1185.27: 31 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-1000118523-march-28"></a>Версия 100.0.1185.23: 28 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-1000118517-march-23"></a>Версия 100.0.1185.17: 23 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-1000118512-march-18"></a>Версия 100.0.1185.12: 18 марта

Исправлены ошибки и проблемы с производительностью.

### <a name="feature-updates"></a>Обновления компонентов

- **Оптимизация активаций протокола приложений Microsoft 365.** Активация протокола приложений Microsoft 365 в доверенных службах облачного хранилища Microsoft теперь будет запускать определенные приложения Microsoft 365 напрямую, включая поддомены SharePoint и URL-адреса Microsoft OneDrive. С помощью политик [AutoLaunchProtocolsComponentEnabled](/deployedge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) и [AutoLaunchProtocolsFromOrigins](/deployedge/microsoft-edge-policies#autolaunchprotocolsfromorigins) можно включить запросы активации протокола приложения, а также определить другие приложения и службы, для которых включены или отключены предупреждения.

## <a name="version-1000118510-march-17"></a>Версия 100.0.1185.10: 17 марта

### <a name="feature-updates"></a>Обновления компонентов

- **Усовершенствования в управлении списками облачных сайтов для режима IE.** Вы можете настроить общий доступ к файлам cookie сеансов между Microsoft Edge и Internet Explorer для режима IE в списке сайтов в Microsoft 365 Admin Center. **Примечание:** Это управляемое развертывание компонентов. Если вы не видите эту функцию, вернитесь, пока мы продолжим развертывание.

- **Предварительный просмотр PDF-файлов в Microsoft Outlook и проводнике.** Пользователи могут просматривать PDF-файлы в облегченной и полной предварительной версии, доступной только для чтения.  Доступно для Outlook PDF-файлов рабочего стола или для локальных PDF-файлов с проводник.  

- **Установленная синхронизация веб-приложений на всех настольных устройствах.** Веб-сайты или веб-приложения (PWA), установленные в качестве приложений, будут синхронизироваться на всех настольных устройствах, на которых вы вошли и включили синхронизацию. Они будут отображаться как доступные приложения для установки. Приложение, удаленное с одного устройства, синхронизирует удаление на всех устройствах.

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

## <a name="version-990115039-march-10"></a>Версия 99.0.1150.39: 10 марта

### <a name="feature-updates"></a>Обновления компонентов

- **Усовершенствования в управлении списками облачных сайтов для режима IE.** Определите пробелы в списке корпоративных сайтов, настроив отчеты о отзывах сайтов с помощью политик [InternetExplorerIntegrationCloudUserSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) и [InternetExplorerIntegrationCloudNeutralSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) . ВЫ можете просматривать URL-адреса локальных списков сайтов от пользователей и потенциально неправильно настроенные URL-адреса нейтральных сайтов в интерфейсе Microsoft Edge сайта в Microsoft 365 Admin Center. Дополнительные сведения см[. в разделе "Просмотр отзывов о сайте" Microsoft 365 Admin Центре](/deployedge/edge-ie-mode-cloud-site-list-mgmt#view-site-feedback-on-the-microsoft-365-admin-center-1).  **Примечание:** Это управляемое развертывание компонентов. Если вы не видите эту функцию, вернитесь, когда мы продолжим развертывание.

## <a name="version-990115030-march-2"></a>Версия 99.0.1150.30: 2 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-990115025-february-25"></a>Версия 99.0.1150.25: 25 февраля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-990115021-february-22"></a>Версия 99.0.1150.21: 22 февраля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-990115016-february-14"></a>Версия 99.0.1150.16: 14 февраля

Исправлены ошибки и проблемы с производительностью.

<!--- From Version 99.0.1150.11: February 9 to Version 98.0.1108.27: January 19 --->
<!-- archive from Version 98.0.1108.23: January 14 to Version 97.0.1072.28: December 8 -->
<!--- Version 97.0.1072.21: December 1 to Version 96.0.1054.13: November 5  --->
<!--- archive from Version 96.0.1054.8: November 1 to Version 95.0.1020.14: October 5  --->
<!-- archive from version 95.0.1020.9: September 28 to version 94.0.992.14: September 7 -->
<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive from Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!-- Archive from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 --->
<!-- Archive from Version 87.0.664.12: October 20 to version 86.0.622.15: September 14 -->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)

