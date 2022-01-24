---
title: Заметки о выпуске Microsoft Edge для канала Beta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 01/07/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для канала Beta
ms.openlocfilehash: ddb745c206dc392dc1dbb46a0522db9648ba624e
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2022
ms.locfileid: "12297717"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Заметки о выпуске для Microsoft Edge из канала Beta

Эти заметки о выпуске содержат сведения о новых возможностях и обновлениях, не связанных с безопасностью, которые включены Microsoft Edge канала Beta Архивные версии этих записей выпуска доступны в [архивных](./microsoft-edge-relnote-archive-beta-channel.md)записях выпуска для Microsoft Edge Beta Channel .

> [!NOTE]
> Веб-платформа Microsoft Edge постоянно развивается для улучшения взаимодействия с пользователями, безопасности и конфиденциальности. Дополнительные сведения см. в статье [Изменения в Microsoft Edge, затрагивающие совместимость сайтов](/microsoft-edge/web-platform/site-impacting-changes).

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

- **Используйте текущий профиль для входов на веб-сайты при входе нескольких учетных записей на устройстве.** Когда на устройстве будет подписано несколько учетных записей о работе или школе, пользователям будет предложено выбрать учетную запись из выбора учетной записи для продолжения посещения веб-сайтов. В этом выпуске пользователям будет предложено разрешить Microsoft Edge автоматически войти на веб-сайты с учетной записью работы и школы, которая была подписана в текущем профиле. Пользователи могут включить и отключить эту функцию в **Параметры/Profile.**

- **Добавьте поддержку для microsoft Endpoint Data Loss Prevention (DLP) на macOS.** Правоприменители политики DLP конечной точки Майкрософт доступны на macOS.

- **Откройте цифрово подписанные PDF-файлы.**  Цифровые подписи широко используются для проверки подлинности документа и его изменений. Пользователи могут проверять подписи для PDF-файлов непосредственно из браузера без необходимости в надстройки.

- **Цитации в Microsoft Edge.** Ссылки на источники для исследований являются распространенным требованием для учащихся. Они должны управлять многими ссылками на исследования и источниками, которые не являются простыми задачами. Они также должны перевести эти цитаты в правильные форматы цитирования, такие как APA, MLA и Чикаго. Эта новая функция "Citations" в Microsoft Edge (в настоящее время в Preview) позволяет учащимся лучше управлять и создавать цитации по мере их исследования в Интернете. С помощью цитирования, включенного в коллекциях или Параметры и более **(Alt-F),** Microsoft Edge автоматически генерирует цитации, которые студенты могут использовать позже, чтобы они могли сосредоточиться на своих исследованиях. Когда они будут завершены, они могут легко компилировать эти цитаты в окончательный результат. Дополнительные сведения см. [в Microsoft Edge.](https://blogs.windows.com/msedgedev/2021/11/04/preview-citations-feature-edge/)

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

- [AccessibilityImageLabelsEnabled](/DeployEdge/microsoft-edge-policies#accessibilityimagelabelsenabled) — получите описания изображений от Microsoft Enabled
- [CORSNonWildcardRequestHeadersSupport](/DeployEdge/microsoft-edge-policies#corsnonwildcardrequestheaderssupport) — поддержка заголовок запроса без поддиагреда CORS
- [EdgeDiscoverEnabled](/DeployEdge/microsoft-edge-policies#edgediscoverenabled) — функция Обнаружения в Microsoft Edge
- [EdgeEnhanceImagesEnabled](/DeployEdge/microsoft-edge-policies#edgeenhanceimagesenabled) - Расширение изображений включено
- [InternetExplorerModeTabInEdgeModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorermodetabinedgemodeallowed) — разрешить открывать сайты, настроенные для режима Internet Explorer, в Microsoft Edge
- [SameOriginTabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#sameorigintabcaptureallowedbyorigins) - Allow Same Origin Tab capture by these origins
- [ScreenCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#screencaptureallowedbyorigins) — разрешить захват настольных компьютеров, окон и вкладок в этих источниках
- [SerialAllowAllPortsForUrls](/DeployEdge/microsoft-edge-policies#serialallowallportsforurls) — автоматически предоставляет сайтам разрешение на подключение всех серийных портов
- [SerialAllowUsbDevicesForUrls](/DeployEdge/microsoft-edge-policies#serialallowusbdevicesforurls) — автоматически предоставляет сайтам разрешение на подключение к серийным устройствам USB
- [SmartScreenDnsRequestsEnabled](/DeployEdge/microsoft-edge-policies#smartscreendnsrequestsenabled) — включить фильтр SmartScreen в Microsoft Defender запросы DNS
- [TabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#tabcaptureallowedbyorigins) — разрешить захват вкладок этими истоками
- [WebSQLInThirdPartyContextEnabled](/DeployEdge/microsoft-edge-policies#websqlinthirdpartycontextenabled) - Force WebSQL в сторонних контекстах для повторного включения
- [WindowCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#windowcaptureallowedbyorigins) — разрешить захват окон и вкладок этими истоками

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

- **Запуск прогрессивного веб-приложения (PWA) непосредственно по протокольным ссылкам.** Позвольте установленным PWAs обрабатывать ссылки, которые используют определенный протокол для более интегрированного использования.

- **Узнайте, как решить математические проблемы с помощью математического решения.** Мы рады сообщить, что вы можете использовать math Solver в Microsoft Edge, чтобы получить помощь с широким спектром математических понятий. Эти понятия варьируются от элементарных арифметических и четырехугольных уравнений до тригонометрии и исчисляемости. Math Solver позволяет сфотографировать рукописную или напечатанную математическую проблему, а затем предоставляет мгновенное решение с пошаговой инструкцией, которая поможет вам узнать, как достичь решения без поручений. Math Solver также поставляется с математической клавиатурой, с помощью которую можно легко ввести математические проблемы. Эта клавиатура устраняет необходимость поиска по традиционной клавиатуре, чтобы найти нужные символы математики. После решения проблемы math Solver предоставляет варианты для продолжения обучения с помощью викторин, таблиц и видеоуроков.

- **Freeform highlighting on PDFs.** С добавлением выделенок freeform улучшается режим просмотра PDF и разметки. В PDF можно выделить разделы, к которые не имеется доступа, и отсканировать документы.

- **Защита стеков с аппаратным обеспечением.**  Microsoft Edge приступить к поддержке еще более безопасного режима просмотра, который использует аппаратный поток управления для процессов браузера на поддерживаемом оборудовании (Intel 11th Gen). или AMD Zen 3). Примечание. Поскольку это управляемый выкат функции, вы можете не заметить, что эта функция включена на всех устройствах. Вы можете включить или отключить аппаратную защиту стека, манипулируя вариантами выполнения файлов изображений (IFEO) с помощью групповой политики.

- **Новый диалоговое окно предупреждения для сайтов typosquatting.** Теперь браузер будет показывать предупреждение на некоторых сайтах с URL-адресами, похожими на другие сайты. Этот пользовательский интерфейс использует клиентскую юристику, чтобы предупредить пользователей о сайтах, которые могут подменять популярные веб-сайты. Дополнительные сведения см. в дополнительных сведениях о том, что такое [typosquatting?.](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0)

- **Улучшенная раздатка между режимом IE и современным браузером.**  Начиная с этой версии Microsoft Edge, навигация между режимом Microsoft Edge и Internet Explorer будет включать данные форм и дополнительные http-заготки. Ссылки, почтовые данные, формы данных и методы запроса будут правильно перенаправляться через два опыта. Можно указать, какие типы данных следует включить с помощью политики [InternetExplorerIntegrationComplexNavDataTypes.](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) Дополнительные сведения см. в этом faQ. Мое приложение требует передачи данных POST между [режимом IE и Microsoft Edge.](./edge-ie-mode-faq.md#my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported)

- **Управление списками облачных сайтов для режима IE в общедоступных предварительных просмотрах.**  Управление списками облачных сайтов позволяет управлять списками сайтов для режима IE в облаке, не нуждаясь в локальной инфраструктуре для хозяйского списка сайтов организации. Вы можете получить доступ к функции управления списками облачных сайтов с помощью Microsoft Edge списков сайтов в центре Microsoft 365 Admin. Дополнительные дополнительные статьи см. в статье Управление списками облачных сайтов [для режима IE (Public Preview).](./edge-ie-mode-cloud-site-list-mgmt.md)

- **Обновление Microsoft Edge WebWiew2 с помощью WSUS.** ИТ-администраторы, использующие WSUS для обновления Microsoft Edge, также смогут обновлять Microsoft Edge WebView2 с помощью WSUS. Эта возможность упрощает администрирование для автономных устройств.

- **Обновления WSUS для Сервера.** Обновления WSUS и Каталога для Microsoft Edge каналов (Stable, Beta, Dev) теперь будут применяться к Windows серверных СКА, которые Microsoft Edge установлены, в том числе Windows Server 2022. Дополнительные сведения о настройке обновлений WSUS для Microsoft Edge см. в [Microsoft Edge.](https://docs.microsoft.com/mem/configmgr/apps/deploy-use/deploy-edge?bc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Ftoc.json#update-microsoft-edge)

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

- [ApplicationGuardUploadBlockingEnabled](/DeployEdge/microsoft-edge-policies#applicationguarduploadblockingenabled) — предотвращает отправку файлов во время службы Application Guard.
- [AudioProcessHighPriorityEnabled](/DeployEdge/microsoft-edge-policies#audioprocesshighpriorityenabled) — разрешить звуковой процесс работать с приоритетом выше обычного на Windows.
- [Компонент AutoLaunchProtocolsComponentEnabled](/DeployEdge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) — включен компонент протоколов autoLaunch.
- [EfficiencyMode](/DeployEdge/microsoft-edge-policies#efficiencymode) — настройка, когда режим эффективности должен стать активным.
- [ForceSyncTypes](/DeployEdge/microsoft-edge-policies#forcesynctypes) — настройка списка типов, включенных для синхронизации.
- [InternetExplorerIntegrationComplexNavDataTypes](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) — настройте, будут ли отправлены данные форм и http-загонщики при вводе или выходе из режима Internet Explorer.
- [InternetExplorerModeToolbarButtonEnabled](/DeployEdge/microsoft-edge-policies#internetexplorermodetoolbarbuttonenabled) — покажите кнопку Перезагрузка в режиме Internet Explorer на панели инструментов.
- [PrintPostScriptMode](/DeployEdge/microsoft-edge-policies#printpostscriptmode) — печать в PostScript режиме.
- [PrintRasterizePdfDpi](/DeployEdge/microsoft-edge-policies#printrasterizepdfdpi) - Печать в Rasterize PDF DPI.
- [RendererAppContainerEnabled](/DeployEdge/microsoft-edge-policies#rendererappcontainerenabled) — включить рендер в контейнере приложений.
- [SharedLinksEnabled](/DeployEdge/microsoft-edge-policies#sharedlinksenabled) — показать ссылки, общие для Microsoft 365 приложений в истории.
- [TyposquattingCheckerEnabled](/DeployEdge/microsoft-edge-policies#typosquattingcheckerenabled) — Настройка edge TyposquattingChecker.

<!-- end major 96 --->

## <a name="version-950102038-october-28"></a>Версия 95.0.1020.38: 28 октября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-950102020-october-11"></a>Версия 95.0.1020.20: 11 октября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-950102014-october-5"></a>Версия 95.0.1020.14: 5 октября

Исправлены ошибки и проблемы с производительностью.

<!-- archive from version 95.0.1020.9: September 28 to version 94.0.992.14: September 7 ---->
<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive on Oct 27 From Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
