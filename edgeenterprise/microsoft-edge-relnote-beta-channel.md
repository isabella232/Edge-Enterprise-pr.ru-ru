---
title: Заметки о выпуске Microsoft Edge для канала Beta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 11/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для канала Beta
ms.openlocfilehash: 57ea92fde42d4ad4c63f238c3b30fa218ee5b360
ms.sourcegitcommit: 42f01cad0bf15224222b2aeadb48f03d46c35723
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2021
ms.locfileid: "12154521"
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

- **Улучшенная раздатка между режимом IE и современным браузером.**  Начиная с этой версии Microsoft Edge, навигация между режимом Microsoft Edge и Internet Explorer будет включать данные форм и дополнительные http-заготки. Ссылки, почтовые данные, формы данных и методы запроса будут правильно перенаправляться через два опыта. Можно указать, какие типы данных следует включить с помощью политики [InternetExplorerIntegrationComplexNavDataTypes.](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes)

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

## <a name="version-9409929-september-2"></a>Версия 94.0.992.9: 2 сентября

### <a name="feature-updates"></a>Обновления компонентов

- **Microsoft Edge 4-недельную каденцию обновлений в бета-версии и стабильных каналах.**  Для основных версий будет принят новый четырехнедельный цикл выпуска. Подробнее о решении можно узнать здесь: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **Доступен новый вариант выпуска "Расширенный стабильный".**  Мы предлагаем новый вариант выпуска "Расширенный стабильный" для управляемых корпоративных клиентов. Вариант выпуска "Расширенный стабильный" будет сохраняться в четных версиях и обновляться каждые 8 недель. Система безопасности будет обновляться каждые две недели.  Дополнительные сведения см. здесь: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Улучшение поведения по умолчанию при открытии MHTML-файлов.**  MHTML-файлы будут по-прежнему открываться в режиме IE (если он включен), если только они не были сохранены в Microsoft Edge (с помощью параметров "Сохранить как" или "Сохранить страницу как"). Если файл сохранен в Microsoft Edge, он будет открываться только в Microsoft Edge.  Это изменение устраняет проблему отрисовки, которая наблюдалась при открытии MHTML-файлов, сохраненных в Microsoft Edge, в режиме IE.

- **Ограничение запросов частной сети безопасными контекстами.** При доступе к ресурсам в локальных (частных) сетях со страниц в Интернете требуется, чтобы эти страницы доставлялись по протоколу HTTPS. Это изменение осуществляется в проекте Chromium, на котором основан Microsoft Edge. Дополнительные сведения см. в [записи о состоянии платформы Chrome](https://chromestatus.com/feature/5436853517811712). Для поддержки сценариев, необходимых для сохранения совместимости с незащищенными страницами, доступны две политики совместимости: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) и [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls).

- **Блокировка скачивания смешанного контента.** На защищенных страницах разрешено скачивание только файлов, размещенных на других защищенных страницах, а загрузки, размещенные на незащищенных (отличных от HTTPS) страницах, блокируются, если они инициируются с защищенной страницы. Это изменение осуществляется в проекте Chromium, на котором основан Microsoft Edge. Дополнительные сведения см. в [записи блога безопасности Google](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html).

- **Включение неявного входа для локальных учетных записей.**   Если включить политику OnlyOnPremisesImplicitSigninEnabled, неявный вход будет включен только для локальных учетных записей.  Браузер Microsoft Edge не будет пытаться выполнять неявный вход в учетные записи MSA и AAD. Переход с локальных учетных записей на учетные записи AAD также будет остановлен.

- **К документам PDF добавлены поля для произвольного текста.**  Теперь мы поддерживаем добавление текстовых полей свободной формы в документы PDF, которые можно использовать для заполнения форм и добавления видимых заметок.

- **Обновление паролей с легкостью.**  Браузер теперь будет принимать вас непосредственно на страницу Изменить пароль для данного веб-сайта, экономя время и клики, избегая необходимости переходить на страницу вручную. После того, как вы на этой странице браузер также автозаполнеет существующий пароль и предложит надежный, уникальный новый пароль.  Обратите внимание: в настоящее время эта функция доступна на ограниченном количестве сайтов.  

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

- **Начальные предпочтения в Microsoft Edge.**  Начиная с Microsoft Edge версии 93, развертывание Microsoft Edge на предприятии станет проще с добавлением [начальных предпочтений.](/deployedge/initial-preferences-support-on-microsoft-edge-browser)

- **Режим IE в Microsoft Edge поддерживает поведение "без слияния".**  Начиная с Microsoft Edge версии 93, режим IE на Microsoft Edge будет поддерживать "без слияния". Для конечных пользователей при запуске нового окна браузера из приложения режима IE оно будет в отдельном сеансе, аналогичном поведению в IE11. Вам потребуется настроить список сайтов, чтобы настроить сайты, необходимые для предотвращения совместного доступа к сеансам. Для каждого окна Microsoft Edge при первом посещении вкладки режима IE в этом окне, если это один из назначенных сайтов "без слияния", это окно блокируется в другом сеансе IE "без слияния" от всех остальных окон Microsoft Edge по крайней мере до закрытия последней вкладки режима IE в этом окне. [Здесь](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--no-merge--option-that-was-supported-in-internet-explorer-11-) вы найдете дополнительные сведения.

- **Группы вкладок.**  Возможность классификации вкладок в группы, определяемую пользователем, позволяет эффективнее находить, переключать и управлять вкладками в нескольких workstreams. Для этого мы включаем группировку вкладок, начиная с Microsoft Edge версии 93.

- **Скрытие заголовка окна при использовании вертикальных вкладок.**  Получите дополнительные несколько пикселей обратно, скрыв заголовок окна браузера при использовании вертикальных вкладок. Начиная с Microsoft Edge версии 93, вы можете перейти к edge://settings/appearance и в разделе Настройка панели инструментов выберите параметр, чтобы скрыть панель заголовка в режиме Вертикальная вкладка.

- **Видео "картинка в картинке" (PiP) в панели инструментов, вызываемой при наведении курсора.**  Начиная с Microsoft Edge версии 93, будет еще проще вводить изображение в режиме Picture (PiP). При наведении курсора на поддерживаемое видео появляется панель инструментов, которая позволяет просматривать это видео в окне PiP.  Примечание. В настоящее время это доступно для Microsoft Edge на macOS.  Проверьте в ближайшее время, как мы продолжаем нашу выкатку для Windows пользователей.

- **Удаление 3DES в TLS.**  Начиная с Microsoft Edge версии 93 поддержка TLS_RSA_WITH_3DES_EDE_CBC_SHA шифра будет удалена. Это изменение осуществляется в проекте Chromium, на котором основан Microsoft Edge. Дополнительные сведения см. в записи о [состоянии платформы Chrome](https://chromestatus.com/feature/6678134168485888). Кроме того, в Microsoft Edge версии 93 будет доступна политика [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) для поддержки сценариев, которым необходимо сохранение совместимости с устаревшими серверами. Эта политика совместимости устареет и перестанет работать в Microsoft Edge версии 95. Обновите затронутые серверы заранее.

- **Политики для обхода запросов ClickOnce и DirectInvoke.**  Мы обновили наши политики, чтобы включить обход запросов ClickOnce и приложения DirectInvoke для указанных типов файлов из указанных доменов. Для этого необходимо:

  - Включить [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) или [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Включить политику [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) и настроить список определенных типов файлов, для которых следует отключить ClickOnce и DirectInvoke.
  - Включим политику [AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls) и установите список определенных доменов, которые ClickOnce и DirectInvoke будут отключены для

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

<!--Archive on Oct 27 From Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
