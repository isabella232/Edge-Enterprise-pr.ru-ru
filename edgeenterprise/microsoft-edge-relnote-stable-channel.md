---
title: Заметки о выпуске Microsoft Edge для стабильного канала
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 01/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для стабильного канала
ms.openlocfilehash: b7a875c7a3688d1839be9c3fdc835f77e14f3bae
ms.sourcegitcommit: f0f250190fc09964175778338a177f1240946b98
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297193"
---
# Заметки о выпуске для стабильного канала Microsoft Edge

Эти заметки о выпуске содержат сведения о новых компонентах и обновлениях, не связанных с безопасностью, которые включены в стабильный канал Microsoft Edge.

- Список обновлений системы безопасности находится [здесь](microsoft-edge-relnotes-security.md).
- Архивные заметки о выпуске для канала Microsoft Edge Stable находятся [здесь](microsoft-edge-relnote-archive-stable-channel.md).

 Чтобы ознакомиться с каналами Microsoft Edge, см. статью [Обзор каналов Microsoft Edge](microsoft-edge-channels.md).

> [!NOTE]
> Для канала Stable обновления последовательно разворачиваются в течение одного или нескольких дней. Дополнительные сведения см. в статье [Последовательные развертывания обновлений Microsoft Edge](microsoft-edge-update-progressive-rollout.md).

## Версия 88.0.705.50: 21 января

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#january-21-2021).

<!--- begin major 88  --->
### Обновления компонентов

- **Нерекомендуемые компоненты:**

  - Не рекомендуется поддержка протокола FTP. Поддержка устаревшего протокола FTP удалена из Microsoft Edge. При попытке перейти по ссылке FTP браузер направит операционную систему на открытие внешнего приложения для обработки ссылки FTP. Кроме того, ИТ-администраторы могут настроить Microsoft Edge на использование режима IE для сайтов, которые используют протокол FTP.
  - Поддержка Adobe Flash будет удалена. Начиная с бета-версии Microsoft Edge 88, возможности и поддержка Adobe Flash будут удалены. Подробнее: [Новости об окончании поддержки Adobe Flash Player — блог Microsoft Edge (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Проверка подлинности:**

  - Единый вход теперь доступен для учетных записей Azure Active Directory (Azure AD) и учетной записи Майкрософт (MSA) в Windows нижнего уровня. Пользователь, выполнивший вход в Microsoft Edge в Microsoft Windows нижнего уровня (7, 8.1), теперь автоматически входит в веб-сайты, настроенные на единый вход с помощью рабочей учетной записи или учетной записи Майкрософт (например, Bing.com, Office.com, msn.com, Outlook.com).<br>Примечание. Чтобы использовать эту функцию, пользователю может потребоваться выйти, а затем снова войти в систему, если вход был выполнен в версии Microsoft Edge ниже 88.

- **Возможность завершения сеанса в режиме терминала**. Кнопка "Завершить сеанс" теперь доступна при открытом просмотре в режиме терминала. Эта возможность обеспечивает удаление данных и параметров браузера при закрытии Microsoft Edge. Подробнее о возможностях и дорожной карте режима терминала см. в статье [Настройка режима терминала Microsoft Edge.](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)

- **Безопасность и конфиденциальность:**

  - Оповещения создаются в том случае, если пароль пользователя обнаружен среди украденных данных в Интернете. Пароли пользователей сверяются с репозиторием известных украденных учетных данных, а пользователю отправляется оповещение при обнаружении совпадения. Для обеспечения безопасности и конфиденциальности пароли пользователей хэшируются и шифруются, когда они сверяются с базой данных, содержащей украденные учетные данные.
  - Автоматическое обновление смешанного содержимого. Защищенные страницы, доставляемые по протоколу HTTPS, могут содержать ссылки на изображения, которые обслуживаются по незащищенному протоколу HTTP. Чтобы повысить конфиденциальность и безопасность в Microsoft Edge версии 88, эти изображения будут извлекаться по протоколу HTTPS. Если изображение недоступно по протоколу HTTPS, оно не будет загружено.
  - Просмотр разрешений сайта по сайту и по недавним действиям. Начиная с Microsoft Edge версии 88, пользователям будет легче управлять разрешениями сайта. Они смогут просматривать разрешения по веб-сайту, а не только по типу разрешения. Кроме того, мы добавили раздел недавних действий, в котором пользователь сможет просмотреть все последние изменения, внесенные в разрешения сайта.
  - Улучшение контроля над файлами cookie браузера. Начиная с Microsoft Edge версии 88, пользователи могут удалять сторонние файлы cookie, не затрагивая основные файлы cookie. Пользователи также смогут фильтровать файлы cookie по отправителю (основные и сторонние) и сортировать их по имени, количеству и объему данных, которые были сохранены или изменены в последний раз.

- **Пароли:**

  - Генератор паролей. Microsoft Edge предлагает встроенный генератор надежных паролей, который можно использовать при регистрации новой учетной записи или при изменении существующего пароля. Просто найдите в поле пароля раскрывающийся список паролей, рекомендуемых браузером, и при его выборе он автоматически сохранится в браузере и синхронизируется на разных устройствах для простого использования в будущем.
  - Мониторинг паролей. Если любой из ваших паролей, сохраненных в браузере, совпадает со списком утечек учетных данных, Microsoft Edge уведомит вас и запросит обновление пароля. Мониторинг паролей проверяет совпадения от вашего имени и включен по умолчанию.
  - Изменение пароля. Теперь сохраненные пароли можно изменять непосредственно в параметрах Microsoft Edge. Каждый раз, когда пароль обновляется за пределами Microsoft Edge, можно легко заменить старый сохраненный пароль новым, изменив сохраненную запись в параметрах. 

- **Производительность:**

  - Повышение производительности браузера с помощью спящих вкладок. Функция спящих вкладок повышает производительность браузера, переводя неактивные вкладки в спящий режим, чтобы освободить системные ресурсы, такие как память и процессор, и использовать их для активных вкладок или других приложений. Пользователи могут предотвратить переход сайтов в спящий режим и настроить время, по истечении которого неактивная вкладка перейдет в спящий режим. Чтобы пользователи могли оставаться в потоке, существуют также эвристические методы, которые предотвращают переход определенных сайтов, например сайтов интрасети, в спящий режим. Эта возможность доступна только случайно выбранной группе пользователей, участвующих в эксперименте. Мы планируем активировать функцию спящих вкладок в Microsoft Edge версии 89 по умолчанию. Управлять этой возможностью можно с помощью групповых политик.
  - Увеличение скорости запуска Microsoft Edge с помощью ускорения запуска. Чтобы повысить скорость запуска Microsoft Edge, мы разработали возможность ускорения запуска. Запуск Microsoft Edge ускоряется за счет работы браузера в фоновом режиме. Примечание. Эта возможность доступна только случайно выбранной группе пользователей, участвующих в эксперименте. Эти пользователи предоставляют отзывы службе поддержки.

- **Эффективная работа:**

  - Улучшение эффективности работы и многозадачности с помощью вертикальных вкладок. По мере роста числа горизонтальных вкладок названия сайтов обрезаются, а элементы управления вкладками теряются в уменьшенных вкладках. Это прерывает рабочий процесс пользователей, так как они тратят больше времени на поиск, переключение и управление вкладками и меньше времени на текущую задачу. Функция вертикальных вкладок позволяет пользователям перемещать вкладки в сторону, а вертикально выровненные значки и более длинные заголовки сайтов упрощают быстрое сканирование, идентификацию и переключение на нужную вкладку.
  - Автоматическое заполнение поля даты рождения. Microsoft Edge позволяет экономить время и усилия при заполнении форм и создании учетных записей в Интернете, автоматически заполняя данные пользователя, такие как адрес, имя, номер телефона и т.д. Теперь Microsoft Edge предоставляет поддержку и для поля даты рождения, данные в котором пользователи могут сохранить и автоматически заполнять. Пользователь может просматривать, изменять и удалять эти сведения в любое время в параметрах своего профиля.
  - Улучшения для раздела "Недавно закрытые" в журнале. Теперь раздел "Недавно закрытые" включает последние 25 вкладок и окон из любых сеансов просмотра, а не только из предыдущего сеанса. Пользователи могут выбрать раздел "Недавно закрытые" в новом интерфейсе журнала, чтобы просмотреть все открытые вкладки.
  - Функция "Ваш день в двух словах" включена по умолчанию. С Microsoft Edge версии 88 информационные работники могут воспользоваться интеллектуальными функциями повышения производительности на странице "Новая вкладка" (NTP). Пользователи Microsoft Edge 87 также смогут использовать эти функции в течение 2 недель после выпуска Microsoft Edge 88. Мы предлагаем пользователям, которые вошли в рабочую или учебную учетную запись, персонализированный и актуальный контент на основе Microsoft 365 Graph. Пользователи могут быстро просмотреть модули "Ваш день в двух словах", чтобы легко отслеживать встречи и недавние задачи, а также быстро запускать приложения, которые они хотят использовать.

- **Синхронизация журнала и открытых вкладок**. Теперь пользователям доступна синхронизация журнала и открытых вкладок. Включение этих функций поможет пользователям продолжить работу с того места, где они остановились, сделав журнал браузера и открытые вкладки доступными на всех синхронизируемых устройствах. Мы обновили политики синхронизации и журнала браузера, поэтому теперь пользователи не теряют связь и поддерживают производительность при применении Microsoft Edge на любых устройствах. [Подробнее](https://blogs.windows.com/windowsexperience/2021/01/21/this-year-lets-resolve-to-make-the-most-of-our-time-online-and-better-protect-ourselves-from-online-threats/).

- **PDF:**

  - Отображение PDF-документа в виде книги (две страницы). Начиная с Microsoft Edge версии 88, пользователи могут просматривать PDF-документы в одностраничном или двухстраничном представлении книги. Чтобы изменить представление, нажмите кнопку **Просмотр страницы** на панели инструментов.
  - Поддержка привязанных текстовых заметок для PDF-файлов. С Microsoft Edge версии 87 пользователи могут добавлять набранные текстовые заметки к любому фрагменту текста в PDF-файлах.

- **Шрифты:**

  - Значки браузера обновляются в соответствии со системой проектирования Fluent Design. В рамках продолжающейся работы над Fluent Design в браузере мы внесли изменения, позволяющие точнее согласовать значки с новой системой значков Майкрософт. Эти изменения затронут многие из пользовательских интерфейсов с действиями, выполняемыми вручную, в том числе вкладки, адресную строку, а также значки навигации и поиска, которые можно найти в различных меню.
  - Улучшенное отображение шрифтов. Отрисовка текста улучшена для достижения большей четкости и уменьшения размытости.

### Обновления политик

#### Новые политики

Добавлено 18 новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Добавлены следующие новые политики.

- [BasicAuthOverHttpEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#basicauthoverhttpenabled) — разрешить базовую проверку подлинности для HTTP.
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
- [TargetBlankImpliesNoOpener](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#targetblankimpliesnoopener) — не устанавливать window.opener для ссылок, нацеленных на _blank.
- [UpdatePolicyOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#updatepolicyoverride) — определяет, как Центр обновления Microsoft Edge обрабатывает доступные обновления из Microsoft Edge.
- [VerticalTabsAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#verticaltabsallowed) — настраивает доступность вертикального макета для вкладок в боковой части окна браузера.
- [WebRtcAllowLegacyTLSProtocols](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtcallowlegacytlsprotocols) — разрешает переход на устаревшую версию TLS/DTLS в WebRTC.
- [WebWidgetAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webwidgetallowed)— включает мини веб-приложение.
- [WebWidgetIsEnabledOnStartup](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webwidgetisenabledonstartup) — разрешает запускать мини веб-приложение при начальной загрузке Windows.

#### Нерекомендуемые политики

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled) — включает упреждающую проверку подлинности.
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist) — настраивает правила обхода прокси-сервера.
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode) — настраивает параметры прокси-сервера.
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl) — устанавливает URL-адрес PAC-файла прокси-сервера.
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver) — настраивает адрес или URL-адрес прокси-сервера.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) — разрешает WebDriver переопределять несовместимые политики.

### Устаревшие политики

- [AllowPopupsDuringPageUnload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowpopupsduringpageunload) — позволяет странице показывать всплывающие окне во время ее выгрузки.
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting)— настраивает Adobe Flash по умолчанию.
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls) — разрешает подключаемый модуль Adobe Flash на определенных сайтах.
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls)— блокирует подключаемый модуль Adobe Flash на определенных сайтах.
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode) — расширяет настройку содержимого Adobe Flash на все содержимое.
<!--- end major 88  --->
## Версия 87.0.664.75: 7 января

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#january-7-2021).

## Версия 87.0.664.66: 17 декабря

Исправлены ошибки и проблемы с производительностью.

## Версия 87.0.664.60: 10 декабря

Исправлены ошибки и проблемы с производительностью.

## Версия 87.0.664.57: 7 декабря

Исправлены ошибки и проблемы с производительностью. Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#december-7-2020).

## Версия 87.0.664.55: 3 декабря

Исправлены ошибки и проблемы с производительностью. Для этого выпуска был обновлен следующий компонент.

- **Компонент "Покупки" включен по умолчанию**. Начиная с Microsoft Edge версии 87, корпоративные пользователи могут пользоваться функциями для покупок в Microsoft Edge. Функции для покупок позволяют пользователям Microsoft Edge при совершении покупок в сети находить купоны и выгодные цены. (Использование купонов появилось в версии 87.0.664.41 канала Stable). В этом обновлении доступна функция сравнения цен. Эту функцию можно настроить с помощью политики [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgeshoppingassistantenabled). Ознакомьтесь с нашим [блогом](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) и [узнайте больше](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#shopping) о компоненте "Покупки" (Майкрософт).

## Версия 87.0.664.52: 30 ноября

Исправлены ошибки и проблемы с производительностью.

## Версия 87.0.664.47: 23 ноября

Исправлены ошибки и проблемы с производительностью.

<!-- begin major 87 --->
## Версия 87.0.664.41: 19 ноября

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-19-2020).

### Обновления компонентов

- **Автоматическое перенаправление несовместимых сайтов из Internet Explorer в Microsoft Edge**. С обновления Microsoft Edge 87 стабильного канала общедоступные веб-сайты, на которых отображается сообщение о несовместимости с Internet Explorer, будут автоматически перенаправляться в Microsoft Edge. Дополнительные сведения и инструкции по настройке этой возможности см. в статье [Перенаправление несовместимых сайтов](https://docs.microsoft.com/deployedge/edge-learnmore-neededge).

- **Включение средств конфиденциальности режима терминала**. С Microsoft Edge версии 87 в режиме терминала доступны средства, помогающие компаниям обеспечивать конфиденциальность пользовательских данных. Благодаря этим функциям включаются такие возможности, как удаление пользовательских данных при выходе, удаление загруженных файлов и сброс настроенной начальной даты возможности после указанного периода бездействия. Дополнительные сведения см. в статье [Настройка режима терминала в Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).

- **Функции для покупок, доступные по умолчанию**. C Microsoft Edge версии 87 корпоративные пользователи также могут воспользоваться возможностями покупок в Microsoft Edge. С помощью функций покупок Microsoft Edge помогает пользователям находить купоны и лучшие цены при покупках в Интернете. В этом обновлении доступен интерфейс купонов, а в предстоящих обновлениях для Microsoft Edge 87 будет выпущена функция сравнения цен. Эту возможность можно настроить с помощью политики [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled). Ознакомьтесь с нашим [блогом](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) и [узнайте больше](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#shopping) о Microsoft Shopping.

- **Включение развертывания ClickOnce по умолчанию**. ClickOnce в Microsoft Edge 87 включен по умолчанию, что позволяет снизить количество барьеров для развертывания организациями программного обеспечения и более эффективного согласования поведения устаревшей версии браузера Microsoft Edge. Начиная с Microsoft Edge 87 состояние "Не настроено" политики ClickOnceEnabled отражает новое состояние ClickOnce по умолчанию "Включено" (по сравнению с предыдущим состоянием по умолчанию "Отключено").

- **Интегрирование продуктивности с настраиваемым, связанным с работой содержимым веб-канала на странице новой вкладки (NTP) организации**. На странице новой вкладки (NTP) организации страница производительности Office 365, предлагаемая пользователям, вошедшим в систему с помощью своей рабочей или учебной учетной записи, объединяется с персонализированными, связанными с работой корпоративными и отраслевыми каналами, организованными на одной странице. Пользователи смогут распознавать знакомое содержимое Office 365 и Поиска (Майкрософт) для бизнеса на платформе Bing. Кроме того, они могут легко настроить возможность "Моя лента", выбрав важное для себя содержимое из доступного контента и модулей для своей организации. ИТ-администраторы могут управлять параметрами веб-канала новостей для своей организации, включая выбранную отрасль на странице новой вкладки Microsoft Edge, перейдя в Центр администрирования Microsoft 365. [Подробнее](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/)

- **Конфиденциальность и безопасность:**

  - Поддержка привязки маркеров TLS для сайтов с настроенной политикой. Привязка маркеров TLS предотвращает атаки, направленные на кражу маркеров, для того, чтобы файлы cookie нельзя было повторно использовать на устройстве, которое не является устройством, на котором они изначально были установлены. При использовании привязки маркеров TLS необходимо задать политику [AllowTokenBindingForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowtokenbindingforurls) и обеспечить поддержку перечисленными сайтами этой возможности.

- **Поддержка пера в качестве маркера в PDF-файлах.** Пользователи смогут выделять маркером текст в PDF-файле с помощью клавиатуры.

- **Вывод на печать:**

  - При печати на обеих сторонах выберите сторону, на которую вам необходимо перевернуть. При печати на обеих сторонах пользователь может перевернуть лист длинной стороной или короткой стороной.
  - Выбор режима растеризации печати для предприятия. Управление печатью Microsoft Edge на принтере без поддержки PostScript в Windows. Иногда для правильной печати на принтерах без поддержки PostScript необходимо правильно растеризовать задания для печати. Параметры печати — "Полная" и "Быстрая".

### Обновления политик

#### Новые политики

Добавлено десять новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Добавлены следующие новые политики.

- [ConfigureFriendlyURLFormat](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configurefriendlyurlformat) — настройка стандартного формата вставки для URL-адресов, скопированных из Microsoft Edge, и определение доступности дополнительных форматов для пользователей.
- [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled) — покупки в Microsoft Edge включены.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hideinternetexplorerredirectuxforincompatiblesitesenabled) — скрытие диалогового окна однократного перенаправления и баннера в Microsoft Edge.
- [KioskAddressBarEditingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) — Настройка редактирования в адресной строке для общедоступного просмотра в режиме терминала.
- [KioskDeleteDownloadsOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) — удаление файлов, скачанных в сеансе терминала, при закрытии Microsoft Edge.
- [PasswordRevealEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordrevealenabled) — включение кнопки отображения пароля.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerpreventbhoinstall) — запрет установки вспомогательного объекта браузера (BHO) для перенаправления несовместимых сайтов из Internet Explorer в Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerredirectmode) — перенаправление несовместимых сайтов из Internet Explorer в Microsoft Edge.
- [SpeechRecognitionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#speechrecognitionenabled) — настройка распознавания речи.
- [WebCaptureEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcaptureenabled) — включение функции захвата веб-страниц в Microsoft Edge.

#### Политика устарела

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) — Настройка взаимодействия с новой вкладкой Microsoft Edge.

#### Устаревшая политика

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) — повторное включение устаревших функций веб-платформы на ограниченное время.

<!-- end major 87 -->

## Версия 86.0.622.69: 13 ноября

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-13-2020). Это обновление содержит [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) и [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017), указанные командой Chromium как имеющие эксплойты на практике.

## Версия 86.0.622.68: 11 ноября

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-11-2020)

## Версия 86.0.622.63: 4 ноября

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-4-2020). Это обновление содержит [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009), указанное командой Chromium как имеющее эксплойт на практике.

## Версия 86.0.622.61: 2 ноября

Исправлены ошибки и проблемы с производительностью.

## Версия 86.0.622.58: 29 октября

Исправлены ошибки и проблемы с производительностью.

## Версия 86.0.622.56: 27 октября

Исправлены ошибки и проблемы с производительностью.

## Версия 86.0.622.51: 22 октября

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#october-22-2020)

## Версия 86.0.622.48: 20 октября

Исправлены ошибки и проблемы с производительностью.

## Версия 86.0.622.43: 15 октября

Исправлены ошибки и проблемы с производительностью.

<!-- begin major 86 -->
## Версия 86.0.622.38: 9 октября

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#october-9-2020)

### Обновления компонентов

* **Откат к предыдущей версии Microsoft Edge.** Функция отката позволяет администраторам вернуть известную хорошую версию Microsoft Edge, если у вас возникла проблема с последней версией Microsoft Edge. **Примечание.** Стабильная версия 86.0.622.38 — это первая версия, к которой можно выполнить откат. Это означает, что стабильная версия 87 — это первая версия, с которой можно выполнить откат. [Подробнее](edge-learnmore-rollback.md).

* **Принудительное включение синхронизации по умолчанию в организации.**  Администраторы могут включить синхронизацию учетных записей Azure Active Directory (Azure AD) по умолчанию с помощью политики [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync).

* **Автоматическое переключение профилей в Windows 7 и 8.1.** Автоматическое переключение профилей, в настоящее время доступное в Microsoft Edge в Windows 10, теперь расширено и на более ранние версии Windows (Windows 7 и 8.1). Дополнительные сведения см. в записи блога об [автоматическом переключении профилей](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/).

* **Параметр файлов cookie, используемый по умолчанию: SameSite=Lax**. Чтобы повысить безопасность и конфиденциальность в Интернете, по умолчанию файлы cookie будут обрабатываться с использованием параметра [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite). Это означает, что файлы cookie будут отправляться только в основном контексте и будут пропущены в запросах, отправляемых третьим сторонам. Это изменение может повлиять на совместимость для веб-сайтов, которым требуются файлы cookie для правильной работы сторонних ресурсов. Чтобы разрешить такие файлы cookie, веб-разработчики могут помечать файлы cookie, которые должны настраиваться и отправляться в сторонних контекстах, добавив явные атрибуты `SameSite=none` и `Secure` при настройке файлов cookie. Организации, которые хотят исключить определенные сайты из этого изменения, могут сделать это с помощью политики [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) или отказаться от изменения на всех сайтах с помощью политики [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled).

* **Удаление API кэша приложений HTML5.**  С Microsoft Edge версии 86 устаревший API кэша приложений, позволяющий использовать веб-страницы в автономном режиме, удаляется из Microsoft Edge. Сведения для веб-разработчиков о замене API кэша приложений на служебные сценарии доступны в [документации для веб-разработчиков](https://web.dev/appcache-removal/).  Важно! Вы можете запросить [маркер AppCache OriginTrial](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673), позволяющий сайтам продолжать использовать устаревший API кэша приложений до Microsoft Edge версии 90.

* **Конфиденциальность и безопасность.**

  * **Замена политик [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) и [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) для более ранних версий Windows и macOS.** Эти политики не рекомендуются в Microsoft Edge версии 86 и станут устаревшими в Microsoft Edge версии 89.<br>
Эти политики заменяются политикой [Разрешить телеметрию](https://go.microsoft.com/fwlink/?linkid=2099569) в Windows 10 и новой политикой [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) для всех остальных платформ. Это позволит пользователям управлять диагностическими данными, отправляемыми в корпорацию Майкрософт, для Windows 7, 8, 8.1 и macOS.
  * Поддержка безопасной службы DNS (DNS поверх HTTPS).  С Microsoft Edge версии 86 доступны параметры для управления безопасной службой DNS на неуправляемых устройствах. Эти параметры недоступны пользователям управляемых устройств, но ИТ-администраторы могут включать и отключать безопасную службу DNS с помощью групповой политики [dnsoverhttpsmode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#dnsoverhttpsmode).

* **Режим Internet Explorer:** Позвольте пользователям применять пользовательский интерфейс Microsoft Edge для проверки сайтов в режиме Internet Explorer. С Microsoft Edge версии 86 администраторы могут включить параметр пользовательского интерфейса, чтобы пользователи могли загружать вкладки в режиме Internet Explorer для тестирования или в качестве временной меры до того, как сайты будут добавлены в XML-файл списка сайтов.

* **Обновления PDF:**

  * Оглавление для PDF-документов. С версии 86 в Microsoft Edge добавлена поддержка оглавления, которое позволяет пользователям легко перемещаться по PDF-документам.
  * Доступ ко всем возможностям PDF на экранах небольшого форм-фактора. Получите доступ ко всем возможностям средства чтения PDF-файлов Microsoft Edge на устройствах с небольшим размером экрана.
  * Поддержка пера в качестве маркера в PDF-файлах. Благодаря этому обновлению пользователи могут использовать собственное цифровое перо для прямого выделения текста в PDF-файлах по аналогии с обычным маркером на листе бумаги.
  * Улучшена прокрутка PDF-документов. Теперь вы сможете наслаждаться прокруткой без запинок при просмотре длинных PDF-документов.

* **Пользователям предлагаются варианты автозаполнения при вводе поискового запроса на веб-сайте надстроек Microsoft Edge.** Автозаполнение помогает пользователям быстро завершать поисковые запросы без необходимости ввода всей строки. Это удобно, так как пользователям не нужно запоминать правильное написание и они могут выбирать из доступных демонстрируемых вариантов.

* **Добавление настраиваемого изображения на страницу новой вкладки (NTP) с помощью групповой политики.** С Microsoft Edge версии 86 на странице новой вкладки доступна возможность для замены стандартного изображения на настраиваемое изображение, предоставляемое пользователем. Возможность управления свойствами этого изображения также поддерживается групповой политикой.

* **Сопоставление настроенных сочетаний клавиш с VS Code.** Средства разработчика Microsoft Edge теперь поддерживают настройку сочетаний клавиш в средствах разработчика для обеспечения соответствия вашему редактору/IDE. (В Microsoft Edge 84 мы добавили возможность сопоставлять сочетания клавиш средств разработчика с VS Code.)

* **Удаление загрузки с диска с помощью диспетчера загрузок.** Пользователи теперь могут удалять загруженные файлы с диска, не выходя из браузера. Новая функция удаления загрузок находится в контекстном меню панели загрузок или на странице загрузок.

### Обновления политик

#### Новые политики

Добавлены двадцать три новые политики. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise). Добавлены следующие новые политики.

- [CollectionsServicesAndExportsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#collectionsservicesandexportsblocklist) — блокировка доступа к указанному списку служб и целевым объектам экспорта в Коллекциях.
- [DefaultFileSystemReadGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultfilesystemreadguardsetting) — управлять использованием API файловой системы для чтения.
- [DefaultFileSystemWriteGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultfilesystemwriteguardsetting) — управлять использованием API файловой системы для записи.
- [DefaultSensorsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsensorssetting) — стандартный параметр для датчиков.
- [DefaultSerialGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultserialguardsetting) — управлять использованием API Serial.
- [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) — отправлять обязательные и необязательные диагностические данных об использовании браузера.
- [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed) — разрешить доступ к средству Enterprise Mode Site List Manager.
- [FileSystemReadAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemreadaskforurls) — разрешить доступ на чтение через API файловой системы на этих сайтах.
- [FileSystemReadBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemreadblockedforurls) — заблокировать доступ на чтение через API файловой системы на этих сайтах.
- [FileSystemWriteAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemwriteaskforurls) — Разрешить доступ на запись к файлам и каталогам на этих сайтах.
- [FileSystemWriteBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemwriteblockedforurls) — Заблокировать доступ на запись к файлам и каталогам на этих сайтах.
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
- [UserAgentClientHintsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) — включение функции клиентских подсказок User-Agent.
- [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#userdatasnapshotretentionlimit) — ограничение количества снимков пользовательских данных, сохраняемых для применения в случае аварийного отката.

#### Устаревшие политики

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) — включить отчеты с данными об использовании и сбоях.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) — отправка сведений о сайтах для улучшения служб Майкрософт.

#### Устаревшая политика

[TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled) — включение функции безопасности TLS 1.3 для местных якорей доверия.

## Версия 85.0.564.70: 6 октября

Исправлены ошибки и проблемы с производительностью.

## Версия 85.0.564.68: 1 октября

Исправлены ошибки и проблемы с производительностью.

## Версия 85.0.564.63: 23 сентября

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#september-23-2020)

## Версия 85.0.564.51: 9 сентября

Список обновлений системы безопасности находится [здесь](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#september-9-2020)

## Версия 85.0.564.44: 31 августа

Исправлены ошибки и проблемы с производительностью.

<!-- 85.0.564.41: August 27 -->
<!-- Archived to version 84.0.522.40: July 16 -->

## См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
