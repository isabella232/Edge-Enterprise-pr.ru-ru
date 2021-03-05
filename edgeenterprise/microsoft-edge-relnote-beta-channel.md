---
title: Заметки о выпуске Microsoft Edge для канала Beta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 03/04/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для канала Beta
ms.openlocfilehash: e5096d437f8b70ed94add8341db1cdb1d4b69b84
ms.sourcegitcommit: f63a30c3e64e9e57fd76b6675ddff1fc2bbbeac8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "11393628"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Заметки о выпуске для Microsoft Edge из канала Beta

Эти заметки о выпуске содержат сведения о новых возможностях и обновлениях, не связанных с безопасностью, которые включены Microsoft Edge канала Beta Архивные версии этих заметок о выпуске доступны [здесь](microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> Мы обновили заметку о выпуске [версии 89.0.774.18 от 3 февраля](#version-89077418-february-3) канала Microsoft Edge Beta, чтобы указать выпущенные функции.

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
<!-- begin major 89 -->
## <a name="version-89077418-february-3"></a>Версия 89.0.774.18: 3 февраля

### <a name="feature-updates"></a>Обновления компонентов

- **Режим терминала включает дополнительные возможности блокировки.** Начиная с Microsoft Edge версии 89, мы добавили дополнительные возможности блокировки в режиме терминала, чтобы пользователи могли работать эффективно и безопасно. [Подробнее](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **Средство Enterprise Mode Site List Manager будет доступно в браузере на странице *edge://compat***. Это средство можно использовать для создания, изменения и экспорта XML списка сайтов для режима Internet Explorer в Microsoft Edge. Доступ к этому средству можно получить при необходимости с помощью групповой политики. [Подробнее](https://docs.microsoft.com/deployedge/edge-ie-mode-site-list-manager).

- **Повышение производительности браузера с помощью спящих вкладок**. Функция спящих вкладок повышает производительность браузера, переводя неактивные вкладки в спящий режим, чтобы освободить системные ресурсы, такие как память и процессор, и использовать их для активных вкладок или других приложений. Пользователи могут предотвратить переход сайтов в спящий режим и настроить время, по истечении которого неактивная вкладка перейдет в спящий режим. Чтобы пользователи могли оставаться в потоке, существуют также [эвристические методы](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434), которые предотвращают переход определенных сайтов, например сайтов интрасети, в спящий режим. Управлять этой возможностью можно с помощью групповых политик.

  > [!NOTE]
  > "Повышение производительности браузера с помощью спящих вкладок" — это обновление заметок о выпуске от 3 февраля для основной версии 89.0.774.18.

- **Сброс данных синхронизации Microsoft Edge в облаке вручную**. Мы представляем способ сброса данных синхронизации Microsoft Edge из продукта. Это гарантирует очистку данных из служб Майкрософт, а также устранение определенных проблем с продуктом, которые ранее требовали передачи в службу поддержки.

- **Усовершенствования в области выделения текста в документах PDF**. Пользователи начнут более плавный и согласованный выбор текста в документах PDF, открытых в Microsoft Edge, начиная с версии 89.

- **Поле даты рождения теперь поддерживается автозаполнением**. В настоящее время Microsoft Edge позволяет сэкономить время и усилия при заполнении форм и создании учетных записей в Интернете путем автоматического заполнения таких данных, как адреса, имена, номера телефонов и т. д. Начиная с Microsoft Edge версии 89, мы добавляем поддержку для другого поля, которое можно сохранить и заполнить автоматически — дата рождения. Вы можете просматривать, изменять и удалять эти сведения в любое время в параметрах профиля.

- **Поддержка поиска на естественном языке в адресной строке, на странице поиска журнала и в центре журнала**. Начиная с Microsoft Edge версии 89, поиск статьи или веб-сайта будет проще при поиске на естественном языке в адресной панели, на странице журнала и в центре журнала. Пользователи могут искать ранее просматриваемое содержимое страницы, описание и время (например, "рецепт торта за последнюю неделю"), а также совпадения по ключевым словам заголовков и URL-адресов. Эта возможность доступна только случайно выбранной группе пользователей, участвующих в эксперименте. Эти пользователи предоставляют отзывы службе поддержки.

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

- [BrowsingDataLifetime](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsingdatalifetime) — параметры времени существования данных браузера
- [MAMEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#mamenabled) — управление мобильными приложениями включено
- [DefinePreferredLanguages](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#definepreferredlanguages) — определение упорядоченного списка предпочитаемых языков, на которых должны отображаться веб-сайты, если сайт поддерживает этот язык
- [ShowRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showrecommendationsenabled) — разрешение рекомендаций и рекламных уведомлений из Microsoft Edge
- [PrintingAllowedBackgroundGraphicsModes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingallowedbackgroundgraphicsmodes) — ограничение режима печати фона
- [PrintingBackgroundGraphicsDefault](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingbackgroundgraphicsdefault)— режим печати фона по умолчанию
- [SmartActionsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartactionsblocklist) — блокировка интеллектуальных действий для списка служб

#### <a name="obsoleted-policies"></a>Устаревшие политики

- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy) — использование политики ссылок по умолчанию для no-referrer-when-downgrade
- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) — включение отчетов с данными об использовании и сбоях
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices)| — отправка сведений о сайтах для улучшения служб Майкрософт
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

- **Возможность завершения сеанса в режиме терминала**. Кнопка "Завершить сеанс" теперь доступна при открытом просмотре в режиме терминала. Эта возможность обеспечивает удаление данных и параметров браузера при закрытии Microsoft Edge. Подробнее о возможностях и дорожной карте режима терминала см. в статье [Настройка режима терминала Microsoft Edge.](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)

- **Безопасность и конфиденциальность:**

  - Оповещения создаются в том случае, если пароль пользователя обнаружен среди украденных данных в Интернете. Пароли пользователей сверяются с репозиторием известных украденных учетных данных, а пользователю отправляется оповещение при обнаружении совпадения. Для обеспечения безопасности и конфиденциальности пароли пользователей хэшируются и шифруются, когда они сверяются с базой данных, содержащей украденные учетные данные.
  - Автоматическое обновление смешанного содержимого. Защищенные страницы, доставляемые по протоколу HTTPS, могут содержать ссылки на изображения, которые обслуживаются по незащищенному протоколу HTTP. Чтобы повысить конфиденциальность и безопасность в Microsoft Edge версии 88, эти изображения будут извлекаться по протоколу HTTPS. Если изображение недоступно по протоколу HTTPS, оно не будет загружено.
  - Просмотр разрешений сайта по сайту и по недавним действиям. Начиная с Microsoft Edge версии 88, пользователям будет легче управлять разрешениями сайта. Они смогут просматривать разрешения по веб-сайту, а не только по типу разрешения. Кроме того, мы добавили раздел недавних действий, в котором пользователь сможет просмотреть все последние изменения, внесенные в разрешения сайта.
  - Улучшение контроля над файлами cookie браузера. Начиная с Microsoft Edge версии 88, пользователи могут удалять сторонние файлы cookie, не затрагивая основные файлы cookie. Пользователи также смогут фильтровать файлы cookie по отправителю (основные и сторонние) и сортировать их по имени, количеству и объему данных, которые были сохранены или изменены в последний раз.

- **Производительность:**

  - Повышение производительности браузера с помощью спящих вкладок. Функция спящих вкладок повышает производительность браузера, переводя неактивные вкладки в спящий режим, чтобы освободить системные ресурсы, такие как память и процессор, и использовать их для активных вкладок или других приложений. Пользователи могут предотвратить переход сайтов в спящий режим и настроить время, по истечении которого неактивная вкладка перейдет в спящий режим. Чтобы пользователи могли оставаться в потоке, существуют также эвристические методы, которые предотвращают переход определенных сайтов, например сайтов интрасети, в спящий режим. Эта возможность доступна только случайно выбранной группе пользователей, участвующих в эксперименте. Мы планируем активировать функцию спящих вкладок в Microsoft Edge версии 89 по умолчанию. Управлять этой возможностью можно с помощью групповых политик.
  - Увеличение скорости запуска Microsoft Edge с помощью ускорения запуска. Чтобы повысить скорость запуска Microsoft Edge, мы разработали возможность ускорения запуска. Запуск Microsoft Edge ускоряется за счет работы браузера в фоновом режиме. Примечание. Эта возможность доступна только случайно выбранной группе пользователей, участвующих в эксперименте. Эти пользователи предоставляют отзывы службе поддержки.

- **Эффективная работа:**

  - Улучшение эффективности работы и многозадачности с помощью вертикальных вкладок. По мере роста числа горизонтальных вкладок названия сайтов обрезаются, а элементы управления вкладками теряются в уменьшенных вкладках. Это прерывает рабочий процесс пользователей, так как они тратят больше времени на поиск, переключение и управление вкладками и меньше времени на текущую задачу. Функция вертикальных вкладок позволяет пользователям перемещать вкладки в сторону, а вертикально выровненные значки и более длинные заголовки сайтов упрощают быстрое сканирование, идентификацию и переключение на нужную вкладку.
  - Автоматическое заполнение поля даты рождения. Microsoft Edge позволяет экономить время и усилия при заполнении форм и создании учетных записей в Интернете, автоматически заполняя данные пользователя, такие как адрес, имя, номер телефона и т.д. Теперь Microsoft Edge предоставляет поддержку и для поля даты рождения, данные в котором пользователи могут сохранить и автоматически заполнять. Пользователь может просматривать, изменять и удалять эти сведения в любое время в параметрах своего профиля.
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

- [BlockExternalExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#blockexternalextensions) — блокирует установку внешних расширений.
- [InternetExplorerIntegrationLocalFileAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileallowed) — разрешает запуск локальных файлов в режиме Internet Explorer.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist) — открывает локальные файлы в списке разрешенных расширений файлов в режиме Internet Explorer.
- [InternetExplorerIntegrationLocalFileShowContextMenu](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileshowcontextmenu) — показывает контекстное меню, чтобы открыть ссылку в режиме Internet Explorer.
- [IntranetRedirectBehavior](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#intranetredirectbehavior) — поведение при перенаправлении в интрасети.
- [PrinterTypeDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printertypedenylist) — отключает типы принтеров в списке запрещенных.
- [ShowMicrosoftRewards](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showmicrosoftrewards)— показывает возможности Microsoft Rewards.
- [SleepingTabsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabsenabled) — настраивает спящие вкладки.
- [SleepingTabsTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabstimeout) — устанавливает время ожидания активности фоновой вкладки для функции спящих вкладок.
- [SleepingTabsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabsblockedforurls) — блокирует спящие вкладки на определенных сайтах.
- [StartupBoostEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#startupboostenabled) — включает ускорение запуска.
- [UpdatePolicyOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#updatepolicyoverride) — определяет, как Центр обновления Microsoft Edge обрабатывает доступные обновления из Microsoft Edge.
- [VerticalTabsAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#verticaltabsallowed) — настраивает доступность вертикального макета для вкладок в боковой части окна браузера.
- [WebRtcAllowLegacyTLSProtocols](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtcallowlegacytlsprotocols) — разрешает переход на устаревшую версию TLS/DTLS в WebRTC.

#### <a name="deprecated-policies"></a>Нерекомендуемые политики

Ниже приводятся нерекомендуемые политики.

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled) — включает упреждающую проверку подлинности.
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist) — настраивает правила обхода прокси-сервера.
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode) — настраивает параметры прокси-сервера.
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl) — устанавливает URL-адрес PAC-файла прокси-сервера.
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver) — настраивает адрес или URL-адрес прокси-сервера.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) — разрешает WebDriver переопределять несовместимые политики.

#### <a name="obsoleted-policies"></a>Устаревшие политики

Ниже приводятся устаревшие политики.

- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting)— настраивает Adobe Flash по умолчанию.
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls) — разрешает подключаемый модуль Adobe Flash на определенных сайтах.
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls)— блокирует подключаемый модуль Adobe Flash на определенных сайтах.
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode) — расширяет настройку содержимого Adobe Flash на все содержимое.

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

- **Включение средств конфиденциальности режима терминала**. В версии 87 и в дальнейших версиях Microsoft Edge в режиме терминала появляются средства, которые помогут компаниям обеспечивать конфиденциальность пользовательских данных. Благодаря этим функциям включаются такие возможности, как удаление пользовательских данных при выходе, удаление загруженных файлов и сброс настроенной начальной даты возможности после указанного периода бездействия. Подробнее о [Настройке режима терминала Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).
- **Включение развертывания ClickOnce по умолчанию**. ClickOnce в Microsoft Edge 87 включен по умолчанию, что позволяет снизить количество барьеров для развертывания организациями программного обеспечения и более эффективного согласования поведения устаревшей версии браузера Microsoft Edge. Начиная с Microsoft Edge 87 состояние "Не настроено" политики ClickOnceEnabled отражает новое состояние ClickOnce по умолчанию "Включено" (по сравнению с предыдущим состоянием по умолчанию "Отключено").
- **Интегрирование продуктивности с настраиваемым, связанным с работой содержимым веб-канала на странице новой вкладки (NTP) организации**. На странице новой вкладки (NTP) организации страница производительности Office 365, предлагаемая пользователям, вошедшим в систему с помощью своей рабочей или учебной учетной записи, объединяется с персонализированными, связанными с работой корпоративными и отраслевыми каналами, организованными на одной странице. Пользователи смогут распознавать знакомое содержимое Office 365 и Поиска (Майкрософт) для бизнеса на платформе Bing. Кроме того, они смогут с легкостью переходить к настраиваемому каналу "My Feed" с содержимым и модулями, которые относятся к пользователю, компании или отрасли пользователя, а также подборке других каналов, к которым организация предоставила доступ. [Подробнее](https://docs.microsoft.com/microsoft-365/admin/manage/manage-industry-news?view=o365-worldwide&preserve-view=true).

- **Конфиденциальность и безопасность.**

  - Поддержка привязки маркеров TLS для сайтов с настроенной политикой. Привязка маркеров TLS предотвращает атаки, направленные на кражу маркеров, для того, чтобы файлы cookie нельзя было повторно использовать на устройстве, которое не является устройством, на котором они изначально были установлены. При использовании привязки маркеров TLS необходимо задать политику [AllowTokenBindingForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowtokenbindingforurls) и обеспечить поддержку перечисленными сайтами этой возможности.

- **Поддержка пера в качестве маркера в PDF-файлах.** Пользователи смогут выделять маркером текст в PDF-файле с помощью клавиатуры.

- **Вывод на печать:**

  - При печати на обеих сторонах выберите сторону, на которую вам необходимо перевернуть. При печати на обеих сторонах пользователь может перевернуть лист длинной стороной или короткой стороной.
  - Выбор режима растеризации печати для предприятия. Управление печатью Microsoft Edge на принтере без поддержки PostScript в Windows. Иногда для правильной печати на принтерах без поддержки PostScript необходимо правильно растеризовать задания для печати. Параметры печати — "Полная" и "Быстрая".

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено десять новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Добавлены следующие новые политики.

- [ConfigureFriendlyURLFormat](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configurefriendlyurlformat) — Настройка формата по умолчанию для URL-адресов, скопированных из Microsoft Edge, и определение доступности пользователям дополнительных форматов.
- [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled) — Включены покупки в Microsoft Edge.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hideinternetexplorerredirectuxforincompatiblesitesenabled) — Скрыты диалоговое окно однократного перенаправления и баннер в Microsoft Edge.
- [KioskAddressBarEditingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) — Настройка редактирования в адресной строке для общедоступного просмотра в режиме терминала.
- [KioskDeleteDownloadsOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) — Удаление файлов, загруженных в ходе сеанса терминала, при закрытии Microsoft Edge.
- [PasswordRevealEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordrevealenabled) — Включение кнопки "Показать пароль.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerpreventbhoinstall) — Запрет установки объекта BHO для перенаправления несовместимых сайтов из Internet Explorer в Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerredirectmode) — Перенаправление несовместимых сайтов из Internet Explorer в Microsoft Edge.
- [SpeechRecognitionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#speechrecognitionenabled) — Настройка распознавания речи.
- [WebCaptureEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcaptureenabled) - Включение функции захвата веб-страниц в Microsoft Edge.

#### <a name="deprecated-policy"></a>Политика устарела

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) — Настройка взаимодействия с новой вкладкой Microsoft Edge.

#### <a name="obsoleted-policy"></a>Устаревшая политика

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) — Повторное включение устаревших функций веб-платформы на ограниченное время (устарело).

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

<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
