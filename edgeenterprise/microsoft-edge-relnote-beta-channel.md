---
title: Заметки о выпуске Microsoft Edge для канала Beta
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 01/20/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для канала Beta
ms.openlocfilehash: c1d0b7091655d5ca0893ea11cc0c2fc44bb516dd
ms.sourcegitcommit: a6c58b19976c194299be217c58b9a99b48756fd0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "11281008"
---
# Заметки о выпуске для Microsoft Edge из канала Beta

Эти заметки о выпуске содержат сведения о новых возможностях и обновлениях, не связанных с безопасностью, которые включены Microsoft Edge канала Beta Архивные версии этих заметок о выпуске доступны [здесь](microsoft-edge-relnote-archive-beta-channel.md).

## Версия 88.0.705.49: 20 января

Исправлены ошибки и проблемы с производительностью.

## Версия 88.0.705.45: 15 января

Исправлены ошибки и проблемы с производительностью.

## Версия 88.0.705.41: 11 января

Исправлены ошибки и проблемы с производительностью.

## Версия 88.0.705.29: 21 декабря

Исправлены ошибки и проблемы с производительностью.

<!-- begin major 88 -->
## Версия 88.0.705.18: 9 декабря

### Обновления компонентов

- **Нерекомендуемые компоненты:**

  - Не рекомендуется поддержка протокола FTP. Поддержка устаревшего протокола FTP удалена из Microsoft Edge. При попытке перейти по ссылке FTP браузер направит операционную систему на открытие внешнего приложения для обработки ссылки FTP. Кроме того, ИТ-администраторы могут настроить Microsoft Edge на использование режима IE для сайтов, которые используют протокол FTP.
  - Поддержка Adobe Flash будет удалена. Начиная с бета-версии Microsoft Edge 88, возможности и поддержка Adobe Flash будут удалены. Подробнее: [Новости об окончании поддержки Adobe Flash Player — блог Microsoft Edge (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Проверка подлинности:**

  - Единый вход теперь доступен для учетных записей Azure Active Directory (Azure AD) и учетной записи Майкрософт (MSA) в macOS и Windows нижнего уровня. Пользователь, выполнивший вход в Microsoft Edge в macOS или Microsoft Windows нижнего уровня (версии 7 и 8.1), теперь автоматически подключается к веб-сайтам, для которых настроено разрешение единого входа с помощью рабочей учетной записи или учетной записи Майкрософт (например, bing.com, office.com, msn.com, outlook.com).<br>Примечание. Чтобы использовать эту функцию, пользователю может потребоваться выйти, а затем снова войти в систему, если вход был выполнен в версии Microsoft Edge ниже 88.
  - Автоматическое переключение пользователей macOS на рабочий профиль для сайтов, на которых проверка подлинности выполняется с помощью рабочей учетной записи. Начиная с Microsoft Edge версии 88, мы предоставляем возможность переключения между сайтами, на которых проверка подлинности выполняется с помощью рабочего профиля пользователя в macOS.<br>Примечание. Чтобы использовать эту функцию, пользователю может потребоваться выйти, а затем снова войти в систему, если вход был выполнен в версии Microsoft Edge ниже 88.

- Возможность завершения сеанса в режиме терминала. Кнопка "Завершить сеанс" теперь доступна в режиме терминала при открытом просмотре в режиме терминала. Эта возможность обеспечивает удаление данных и параметров браузера при закрытии Microsoft Edge. Подробнее о возможностях и дорожной карте режима терминала см. в статье [Настройка режима терминала Microsoft Edge.](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)

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

### Обновления политик

#### Новые политики

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

#### Нерекомендуемые политики

Ниже приводятся нерекомендуемые политики.

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled) — включает упреждающую проверку подлинности.
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist) — настраивает правила обхода прокси-сервера.
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode) — настраивает параметры прокси-сервера.
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl) — устанавливает URL-адрес PAC-файла прокси-сервера.
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver) — настраивает адрес или URL-адрес прокси-сервера.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) — разрешает WebDriver переопределять несовместимые политики.

#### Устаревшие политики

Ниже приводятся устаревшие политики.

- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting)— настраивает Adobe Flash по умолчанию.
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls) — разрешает подключаемый модуль Adobe Flash на определенных сайтах.
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls)— блокирует подключаемый модуль Adobe Flash на определенных сайтах.
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode) — расширяет настройку содержимого Adobe Flash на все содержимое.

<!-- end major 88 -->

## Версия 87.0.664.55: 3 декабря

Исправлены ошибки и проблемы с производительностью. В этом выпуске поддерживается следующая новая функция.

- **Оповещения создаются в том случае, если пароль пользователя обнаружен среди украденных данных в Интернете**. Пароли пользователей сверяются с репозиторием известных украденных учетных данных, а пользователю отправляется оповещение при обнаружении совпадения. Для обеспечения безопасности и конфиденциальности пароли пользователей хэшируются и шифруются, когда они сверяются с базой данных украденных учетных данных.

## Версия 87.0.664.52: 30 ноября

Исправлены ошибки и проблемы с производительностью.

## Версия 87.0.664.40: 18 ноября

Исправлены ошибки и проблемы с производительностью.

## Версия 87.0.664.36: 16 ноября

Исправлены ошибки и проблемы с производительностью.

## Версия 87.0.664.30: 9 ноября

Исправлены ошибки и проблемы с производительностью.

## Версия 87.0.664.24: 2 ноября

Исправлены ошибки и проблемы с производительностью.

## Версия 87.0.664.18: 26 октября

Исправлены ошибки и проблемы с производительностью.

<!-- begin major 87 -->
## Версия 87.0.664.12: 20 октября

### Обновления компонентов

- **Включение средств конфиденциальности режима терминала**. В версии 87 и в дальнейших версиях Microsoft Edge в режиме терминала появляются средства, которые помогут компаниям обеспечивать конфиденциальность пользовательских данных. Благодаря этим функциям включаются такие возможности, как удаление пользовательских данных при выходе, удаление загруженных файлов и сброс настроенной начальной даты возможности после указанного периода бездействия. Подробнее о [Настройке режима терминала Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).
- **Включение развертывания ClickOnce по умолчанию**. ClickOnce в Microsoft Edge 87 включен по умолчанию, что позволяет снизить количество барьеров для развертывания организациями программного обеспечения и более эффективного согласования поведения устаревшей версии браузера Microsoft Edge. Начиная с Microsoft Edge 87 состояние "Не настроено" политики ClickOnceEnabled отражает новое состояние ClickOnce по умолчанию "Включено" (по сравнению с предыдущим состоянием по умолчанию "Отключено").
- **Интегрирование продуктивности с настраиваемым, связанным с работой содержимым веб-канала на странице новой вкладки (NTP) организации**. На странице новой вкладки (NTP) организации страница производительности Office 365, предлагаемая пользователям, вошедшим в систему с помощью своей рабочей или учебной учетной записи, объединяется с персонализированными, связанными с работой корпоративными и отраслевыми каналами, организованными на одной странице. Пользователи смогут распознавать знакомое содержимое Office 365 и Поиска (Майкрософт) для бизнеса на платформе Bing. Кроме того, они смогут с легкостью переходить к настраиваемому каналу "My Feed" с содержимым и модулями, которые относятся к пользователю, компании или отрасли пользователя, а также подборке других каналов, к которым организация предоставила доступ. [Подробнее](https://docs.microsoft.com/microsoft-365/admin/manage/manage-industry-news?view=o365-worldwide&preserve-view=true).

- **Конфиденциальность и безопасность.**

  - Поддержка привязки маркеров TLS для сайтов с настроенной политикой. Привязка маркеров TLS предотвращает атаки, направленные на кражу маркеров, для того, чтобы файлы cookie нельзя было повторно использовать на устройстве, которое не является устройством, на котором они изначально были установлены. При использовании привязки маркеров TLS необходимо задать политику [AllowTokenBindingForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowtokenbindingforurls) и обеспечить поддержку перечисленными сайтами этой возможности.

- **Поддержка пера в качестве маркера в PDF-файлах.** Пользователи смогут выделять маркером текст в PDF-файле с помощью клавиатуры.

- **Вывод на печать:**

  - При печати на обеих сторонах выберите сторону, на которую вам необходимо перевернуть. При печати на обеих сторонах пользователь может перевернуть лист длинной стороной или короткой стороной.
  - Выбор режима растеризации печати для предприятия. Управление печатью Microsoft Edge на принтере без поддержки PostScript в Windows. Иногда для правильной печати на принтерах без поддержки PostScript необходимо правильно растеризовать задания для печати. Параметры печати — "Полная" и "Быстрая".

### Обновления политик

#### Новые политики

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

#### Политика устарела

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) — Настройка взаимодействия с новой вкладкой Microsoft Edge.

#### Устаревшая политика

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) — Повторное включение устаревших функций веб-платформы на ограниченное время (устарело).

<!-- end major 87 -->

## Версия 86.0.622.43: 16 октября

Исправлены ошибки и проблемы с производительностью.

## Версия 86.0.622.36: 7 октября

Исправлены ошибки и проблемы с производительностью.

## Версия 86.0.622.31: 1 октября

Исправлены ошибки и проблемы с производительностью.

## Версия 86.0.622.28: 28 сентября

Исправлены ошибки и проблемы с производительностью.

## Версия 86.0.622.15: 14 сентября

Исправлены ошибки и проблемы с производительностью.

## Версия 86.0.622.11: 9 сентября

### Обновления компонентов

* **Режим Internet Explorer:**

   * Позвольте пользователям применять пользовательский интерфейс (UI) Microsoft Edge для проверки сайтов в режиме Internet Explorer. С Microsoft Edge версии 86 администраторы могут включить параметр пользовательского интерфейса, чтобы пользователи могли загружать вкладки в режиме Internet Explorer для тестирования или в качестве временной меры до того, как сайты будут добавлены в XML-файл списка сайтов.

* **Удаление загрузки с диска с помощью диспетчера загрузок.** Пользователи теперь могут удалять загруженные файлы с диска, не выходя из браузера. Новая функция удаления загрузок находится в контекстном меню панели загрузок или на странице загрузок.

* **Откат к предыдущей версии Microsoft Edge.** Функция отката позволяет администраторам вернуть известную хорошую версию Microsoft Edge, если у вас возникла проблема с последней версией Microsoft Edge.
[Подробнее](edge-learnmore-rollback.md).

* **Принудительное включение синхронизации по умолчанию в организации.**  Администраторы могут включить синхронизацию учетных записей Azure Active Directory (Azure AD) по умолчанию с помощью политики [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync).

* **Обновления PDF:**

  * Оглавление для PDF-документов. С версии 86 в Microsoft Edge добавлена поддержка оглавления, которое позволяет пользователям легко перемещаться по PDF-документам.
  * Доступ ко всем возможностям PDF на экранах небольшого форм-фактора. Получите доступ ко всем возможностям средства чтения PDF-файлов Microsoft Edge на устройствах с небольшим размером экрана.
  * Поддержка пера в качестве маркера в PDF-файлах. Благодаря этому обновлению пользователи могут использовать собственное цифровое перо для прямого выделения текста в PDF-файлах по аналогии с обычным маркером на листе бумаги.
  * Улучшена прокрутка PDF-документов. Теперь вы сможете наслаждаться прокруткой без запинок при просмотре длинных PDF-документов.

* **Автоматическое переключение профилей в Windows 7, 8 и 8.1.** Автоматическое переключение профилей, в настоящее время доступное в Microsoft Edge в Windows 10, теперь расширено и на более ранние версии Windows (Windows 7, 8 и 8.1). Дополнительные сведения см. в записи блога об [автоматическом переключении профилей](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **Пользователям предлагаются варианты автозаполнения при вводе поискового запроса на веб-сайте надстроек Microsoft Edge.** Автозаполнение помогает пользователям быстро завершать поисковые запросы без необходимости ввода всей строки. Это удобно, так как пользователям не нужно запоминать правильное написание и они могут выбирать из доступных демонстрируемых вариантов.

* **Удаление API кэша приложений HTML5.**  С Microsoft Edge версии 86 устаревший API кэша приложений, позволяющий использовать веб-страницы в автономном режиме, удаляется из Microsoft Edge. Сведения для веб-разработчиков о замене API кэша приложений на служебные сценарии доступны в [документации для веб-разработчиков](https://web.dev/appcache-removal/).  Важно! Вы можете запросить [маркер AppCache OriginTrial](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673), позволяющий сайтам продолжать использовать устаревший API кэша приложений до Microsoft Edge версии 90.

* **Безопасность:**

  * Поддержка безопасной службы DNS (DNS поверх HTTPS).  С Microsoft Edge версии 86 доступны параметры для управления безопасной службой DNS на неуправляемых устройствах. Эти параметры недоступны пользователям управляемых устройств, но ИТ-администраторы могут включать и отключать безопасную службу DNS с помощью групповой политики [dnsoverhttpsmode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#dnsoverhttpsmode).


* **Добавление настраиваемого изображения на страницу новой вкладки (NTP) с помощью групповой политики.** С Microsoft Edge версии 86 на странице новой вкладки доступна возможность для замены стандартного изображения на настраиваемое изображение, предоставляемое пользователем. Возможность управления свойствами этого изображения также поддерживается групповой политикой.

* **Сопоставление настроенных сочетаний клавиш с VS Code.** Средства разработчика Microsoft Edge теперь поддерживают настройку сочетаний клавиш в средствах разработчика для обеспечения соответствия вашему редактору/IDE. (В Microsoft Edge 84 мы добавили возможность сопоставлять сочетания клавиш средств разработчика с VS Code.)

* **Замена политик [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) и [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) для более ранних версий Windows и macOS.** Эти политики не рекомендуются в Microsoft Edge версии 86 и станут устаревшими в Microsoft Edge версии 89.<br>
Эти политики заменяются политикой [Разрешить телеметрию](https://go.microsoft.com/fwlink/?linkid=2099569) в Windows 10 и новой политикой [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) для всех остальных платформ. Это позволит пользователям управлять диагностическими данными, отправляемыми в корпорацию Майкрософт, для Windows 7, 8, 8.1 и macOS.

* **Параметр файлов cookie, используемый по умолчанию: SameSite=Lax**. Чтобы повысить безопасность и конфиденциальность в Интернете, по умолчанию файлы cookie будут обрабатываться с использованием параметра [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite). Это означает, что файлы cookie будут отправляться только в основном контексте и будут пропущены в запросах, отправляемых третьим сторонам. Это изменение может повлиять на совместимость для веб-сайтов, которым требуются файлы cookie для правильной работы сторонних ресурсов. Чтобы разрешить такие файлы cookie, веб-разработчики могут помечать файлы cookie, которые должны настраиваться и отправляться в сторонних контекстах, добавив явные атрибуты `SameSite=none` и `Secure` при настройке файлов cookie. Организации, которые хотят исключить определенные сайты из этого изменения, могут сделать это с помощью политики [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) или отказаться от изменения на всех сайтах с помощью политики [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled).

### Обновления политик

#### Новые политики

Добавлено 19 политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [CollectionsServicesAndExportsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#collectionsservicesandexportsblocklist) — блокировка доступа к указанному списку служб и целевым объектам экспорта в Коллекциях.
- [DefaultSensorsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsensorssetting) — стандартный параметр для датчиков.
- [DefaultSerialGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultserialguardsetting) — управлять использованием API Serial.
- [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) — отправлять обязательные и необязательные диагностические данных об использовании браузера.
- [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed) — разрешить доступ к средству Enterprise Mode Site List Manager.
- [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync) — принудительно синхронизировать данные браузера и не показывать запрос на разрешение синхронизации.
- [InsecureFormsWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecureformswarningsenabled) — включить предупреждения для небезопасных форм.
- [InternetExplorerIntegrationTestingAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) — разрешить тестирование режима Internet Explorer.
- [SpotlightExperiencesAndRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#spotlightexperiencesandrecommendationsenabled) — выберите, могут ли пользователи получать настроенные фоновые изображения и текст, предложения, уведомления и советы для служб Майкрософт.
- [NewTabPageAllowedBackgroundTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageallowedbackgroundtypes) — настройка типов фона, разрешенных для макета страницы новой вкладки.
- [SaveCookiesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#savecookiesonexit) — сохранять файлы cookie при закрытии Microsoft Edge.
- [SensorsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsallowedforurls) — разрешить доступ к датчиками на определенных сайтах.
- [SensorsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsblockedforurls) — блокировать доступ к датчиками на определенных сайтах.
- [SerialAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialaskforurls) — разрешить API Serial на определенных сайтах.
- [SerialBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialblockedforurls) — блокировать API Serial на определенных сайтах.
- [URLBlocklist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlblocklist) — заблокировать доступ к списку URL-адресов.
- [URLAllowlist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlallowlist) — определить список разрешенных URL-адресов.
- [UserAgentClientHintsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) — включение функции клиентских подсказок User-Agent.
- [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#userdatasnapshotretentionlimit) — ограничение количества снимков пользовательских данных, сохраняемых для применения в случае аварийного отката.

#### Устаревшие политики

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) — включить отчеты с данными об использовании и сбоях.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) — отправка сведений о сайтах для улучшения служб Майкрософт.

#### Устаревшая политика

[TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled) — включение функции безопасности TLS 1.3 для местных якорей доверия.

#### Изменен заголовок политики

[NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled)— включение загораживания собственного окна

#### Изменено описание политики

- [AdsSettingForIntrusiveAdsSites](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#adssettingforintrusiveadssites)
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls)
- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled)
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy)
- [AutoImportAtFirstRun](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoimportatfirstrun)
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes)
- [BrowserSignin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsersignin)
- [ClearBrowsingDataOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearbrowsingdataonexit) 
- [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled)
- [CommandLineFlagSecurityWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#commandlineflagsecuritywarningsenabled)
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin)
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare)
- [CookiesAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#cookiesallowedforurls)
- [CustomHelpLink](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#customhelplink)
- [DefaultCookiesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultcookiessetting)
- [DefaultGeolocationSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultgeolocationsetting)
- [DefaultImagesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultimagessetting)
- [DefaultInsecureContentSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultinsecurecontentsetting)
- [DefaultJavaScriptSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultjavascriptsetting)
- [DefaultNotificationsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultnotificationssetting)
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting)
- [DefaultPopupsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpopupssetting)
- [DefaultSearchProviderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchproviderenabled)
- [DefaultWebBluetoothGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebbluetoothguardsetting)
- [DefaultWebUsbGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebusbguardsetting)
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload)
- [DeveloperToolsAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#developertoolsavailability)
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors)
- [DownloadRestrictions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#downloadrestrictions)
- [EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures)
- [WinHttpProxyResolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#winhttpproxyresolverenabled)
- [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol)
- [ExternalProtocolDialogShowAlwaysOpenCheckbox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox)
- [ExtensionInstallForcelist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ForceBingSafeSearch](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcebingsafesearch)
- [ForceYouTubeRestrict](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forceyoutuberestrict)
- [HomepageIsNewTabPage](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepageisnewtabpage)
- [HomepageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepagelocation)
- [InPrivateModeAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#inprivatemodeavailability)
- [InternetExplorerIntegrationEnhancedHangDetection](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationenhancedhangdetection)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect)
- [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled)
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled)
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout)
- [NetworkPredictionOptions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#networkpredictionoptions)
- [NewTabPageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation)
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox)
- [NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype)
- [NonRemovableProfileEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nonremovableprofileenabled)
- [PasswordProtectionWarningTrigger](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionwarningtrigger)
- [PasswordProtectionLoginURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionloginurls)
- [PasswordProtectionChangePasswordURL](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionchangepasswordurl)
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls)
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls)
- [PreventSmartScreenPromptOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverride)
- [PreventSmartScreenPromptOverrideForFiles](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverrideforfiles)
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode)
- [RegisteredProtocolHandlers](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#registeredprotocolhandlers)
- [RelaunchNotification](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#relaunchnotification)
- [RestoreOnStartup](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartup)
- [RestoreOnStartupURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartupurls)
- [RestrictSigninToPattern](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restrictsignintopattern)
- [SSLVersionMin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslversionmin)
- [SmartScreenAllowListDomains](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenallowlistdomains)
- [SmartScreenEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenenabled)
- [SmartScreenForTrustedDownloadsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenfortrusteddownloadsenabled)
- [SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled)
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled)
- [TrackingPrevention](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#trackingprevention)
- [WebRtcLocalhostIpHandling](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtclocalhostiphandling)

<!-- end 86 -->

## Версия 85.0.564.41: 25 августа

Исправлены ошибки и проблемы с производительностью.

## Версия 85.0.564.40: 21 августа

Исправлены ошибки и проблемы с производительностью.

## Версия 85.0.564.36: 17 августа

Исправлены ошибки и проблемы с производительностью.

## Версия 85.0.564.30: 10 августа

Исправлены ошибки и проблемы с производительностью.

## Версия 85.0.564.23: 3 августа

Исправлены ошибки и проблемы с производительностью.

<!--- Archived to version 85.0.564.18: July 28 ---->

## См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
