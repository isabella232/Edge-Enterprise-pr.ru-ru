---
title: Заметки о выпуске Microsoft Edge для канала Beta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 11/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для канала Beta
ms.openlocfilehash: bcc2ecf91c6d90443de26b5bff1c744d7582aa18
ms.sourcegitcommit: 4ec03873a85f065d9bfa6203cfe6c3e938f79bc5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2021
ms.locfileid: "12155106"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Заметки о выпуске для Microsoft Edge из канала Beta

Эти заметки о выпуске содержат сведения о новых возможностях и обновлениях, не связанных с безопасностью, которые включены Microsoft Edge канала Beta Архивные версии этих заметок о выпуске доступны [здесь](microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> Веб-платформа Microsoft Edge постоянно развивается для улучшения взаимодействия с пользователями, безопасности и конфиденциальности. Дополнительные сведения см. в статье [Изменения в Microsoft Edge, затрагивающие совместимость сайтов](/microsoft-edge/web-platform/site-impacting-changes).

## <a name="version-96010548-november-1"></a>Версия 96.0.1054.8: 1 ноября

### <a name="feature-updates"></a>Обновления компонентов

- **Запуск прогрессивного веб-приложения (PWA) непосредственно по протокольным ссылкам.** Позвольте установленным PWAs обрабатывать ссылки, которые используют определенный протокол для более интегрированного использования.

- **Узнайте, как решить математические проблемы с помощью математического решения.** Мы рады сообщить, что вы можете использовать math Solver в Microsoft Edge, чтобы получить помощь с широким спектром математических понятий. Эти понятия варьируются от элементарных арифметических и четырехугольных уравнений до тригонометрии и исчисляемости. Math Solver позволяет сфотографировать рукописную или напечатанную математическую проблему, а затем предоставляет мгновенное решение с пошаговой инструкцией, которая поможет вам узнать, как достичь решения без поручений. Math Solver также поставляется с математической клавиатурой, с помощью которую можно легко ввести математические проблемы. Эта клавиатура устраняет необходимость поиска по традиционной клавиатуре, чтобы найти нужные символы математики. После решения проблемы math Solver предоставляет варианты для продолжения обучения с помощью викторин, таблиц и видеоуроков.

- **Прокрутка улучшений для документов PDF.** Мы улучшаем производительность прокрутки, чтобы обеспечить более плавное выполнение прокрутки в документах PDF. Во время прокрутки не отображаются белые полосы.

- **Freeform highlighting on PDFs.** С добавлением выделенок freeform улучшается режим просмотра PDF и разметки. В PDF можно выделить разделы, к которые не имеется доступа, и отсканировать документы.

- **Технология управления потоком исполнения (CET).**  Microsoft Edge начнет поддерживать еще более безопасный режим просмотра, использующий аппаратный поток управления для процессов браузера. Поток управления обеспечивается на поддерживаемом оборудовании: Intel 11th Gen. или AMD Zen 3. Можно отключить CET, настроив параметры выполнения файлов изображений (IFEO) с помощью групповой политики.

- **Новый диалоговое окно предупреждения для сайтов typosquatting.** Теперь браузер будет показывать предупреждение на некоторых сайтах с URL-адресами, которые очень похожи на другие сайты. Этот пользовательский интерфейс использует клиентскую юристику, чтобы предупредить пользователей о сайтах, которые могут подменять популярные веб-сайты. Дополнительные сведения см. в дополнительных сведениях о том, что такое [typosquatting?.](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0)

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

## <a name="version-95010209-september-28"></a>Версия 95.0.1020.9: 28 сентября

### <a name="feature-updates"></a>Обновления компонентов

- **Поддержка функции "Просмотр в проводнике" для библиотек SharePoint Online в Microsoft Edge**  Теперь вы можете включить функцию View in File Explorer для SharePoint современных библиотек документов в Интернете. Чтобы этот опыт был виден и работал для пользователей, необходимо включить Microsoft Edge "Настройка функции View in File Explorer для SharePoint страниц в политике [Microsoft Edge"](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) и обновить конфигурацию клиента SharePoint Online. Дополнительные данные. Просмотр SharePoint файлов с [помощью обозревателя файлов в Microsoft Edge - SharePoint в Microsoft 365 | Microsoft Docs](/SharePoint/sharepoint-view-in-edge).

- **URL-адреса файлов зоны интрасети будут открываться в проводнике Windows.**  Можно разрешить URL-адресам файлов с веб-сайтов из зоны интрасети, доступных по протоколу HTTPS, открывать проводник Windows для этих файлов и каталогов. Эту возможность можно включить с помощью политики [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled).

- **Улучшения возможностей скачивания.**  Поддержка загрузки пользователей распространяется на прогрессивные веб-приложения PWAs и WebView. Кроме того, мы будет реализована поддержка перетаскивания в проводнике и на рабочем столе.

- **Возобновите работу с PDF-файлами с того места, на котором вы остановились.**  Вы можете возобновить чтение с места, где последний раз закрывали pdf-документ.

- **Режим эффективности продлевает время работы батареи, когда ноутбук переключается в режим экономии заряда.**  Когда ноутбук перейдет в режим экономии заряда, включится режим эффективности, чтобы разрешить браузеру управлять ресурсами для увеличения времени работы батареи вашего устройства. У вас будет четыре варианта, когда режим эффективности активен, отключен и не работает отключаемой батареи, отключен, всегда и никогда. Примечание. Это управляемый выкат функции. Устройства с аккумулятором должны иметь включенную функцию.

***Новые политики***

- [BrowserLegacyExtensionPointsBlockingEnabled](/DeployEdge/microsoft-edge-policies#browserlegacyextensionpointsblockingenabled) — включить блокировку устаревших точек расширения браузера.
- [CrossOriginWebAssemblyModuleSharingEnabled](/DeployEdge/microsoft-edge-policies#crossoriginwebassemblymodulesharingenabled) — указывает, можно ли перенаправлять модули WebAssembly.
- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) — указывает, проверяется или пропускается политика разрешений отображения.
- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) — настройка настройки пикселей между высотами window.open, источником для страниц режима IE и Microsoft Edge страниц режима.
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) — настройка настройки пикселей между ширинами window.open, источником из страниц режима IE и Microsoft Edge страниц режима.
- [IntranetFileLinksEnabled](/DeployEdge/microsoft-edge-policies#intranetfilelinksenabled) — разрешить ссылки url-адресов url-адресов файлов Microsoft Edge для Windows File Explorer.
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) — настройка поведения отката аварийного сбоя ShadowStack.
- [VisualSearchEnabled](/DeployEdge/microsoft-edge-policies#visualsearchenabled) — включить визуальный поиск.

***Устаревшие политики***

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) — разрешить тестирование режима Internet Explorer.
- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) — поддержка стандартного устаревшего параметра поведения SameSite для cookie-файлов.

## <a name="version-94099223-september-17"></a>Версия 94.0.992.23: 17 сентября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-94099219-september-13"></a>Версия 94.0.992.19: 13 сентября

Исправлены ошибки и проблемы с производительностью.

## <a name="version-94099214-september-7"></a>Версия 94.0.992.14: 7 сентября

Исправлены ошибки и проблемы с производительностью.

<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive on Oct 27 From Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
