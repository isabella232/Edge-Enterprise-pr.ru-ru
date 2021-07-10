---
title: Заметки о выпуске Microsoft Edge для стабильного канала
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Заметки о выпуске Microsoft Edge для стабильного канала
ms.openlocfilehash: ab599e3995641290ed806acc241b00e808f7fc1b
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642535"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Заметки о выпуске для стабильного канала Microsoft Edge

Эти заметки о выпуске содержат сведения о новых компонентах и обновлениях, не связанных с безопасностью, которые включены в стабильный канал Microsoft Edge.

- Список обновлений системы безопасности находится [здесь](microsoft-edge-relnotes-security.md).
- Архивные заметки о выпуске для канала Microsoft Edge Stable находятся [здесь](microsoft-edge-relnote-archive-stable-channel.md).

 Чтобы ознакомиться с каналами Microsoft Edge, см. статью [Обзор каналов Microsoft Edge](microsoft-edge-channels.md).

> [!NOTE]
> Для канала Stable обновления последовательно разворачиваются в течение одного или нескольких дней. Дополнительные сведения см. в статье [Последовательные развертывания обновлений Microsoft Edge](microsoft-edge-update-progressive-rollout.md).
>
> Веб-платформа Microsoft Edge постоянно развивается для улучшения взаимодействия с пользователями, безопасности и конфиденциальности. Дополнительные сведения см. в статье [Изменения, вносимые в Microsoft Edge, которые влияют на совместимость сайтов](/microsoft-edge/web-platform/site-impacting-changes).


## <a name="version-91086464-july-2"></a>Версия 91.0.864.64: 2 июля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-91086459-june-24"></a>Версия 91.0.864.59: 24 июня

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#june-24-2021).

## <a name="version-91086454-june-18"></a>Версия 91.0.864.54: 18 июня

> [!Important]
> Это обновление содержит исправление для уязвимости [CVE-2021-30554](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30554), которая, по сообщениям группы разработчиков Chromium, имеет действующий эксплойт. Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#june-18-2021).

## <a name="version-91086448-june-11"></a>Версия 91.0.864.48: 11 июня

> [!Important]
>Это обновление содержит исправление для уязвимости [CVE-2021-30551](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30551), которая, по сообщениям группы разработчиков Chromium, имеет действующий эксплойт. Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#june-11-2021).

## <a name="version-91086441-june-3"></a>Версия 91.0.864.41: 3 июня

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#june-3-2021).

## <a name="version-91086437-may-27"></a>Версия 91.0.864.37: 27 мая

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#may-27-2021).

### <a name="feature-updates"></a>Обновления компонентов

- **Определение сетевого трафика, исходя из контейнеров Application Guard в Microsoft Defender на уровне прокси-сервера**. Начиная с Microsoft Edge версии 91, для добавления тегов сетевого трафика, исходящего из контейнеров Application Guard, встраивается поддержка, что позволяет предприятиям идентифицировать их и применять определенные политики.

- **Параметр поддержки, позволяющий синхронизировать избранное из хоста в контейнер Edge Application Guard.** Начиная с Microsoft Edge версии 91, пользователи могут настроить Application Guard для синхронизации избранного из хоста в контейнер. Это также гарантирует появление нового избранного в контейнере.

- **Начиная с Microsoft Edge версии 91 браузер автоматически прерывает загрузки типов, которые могут нанести вред вашему компьютеру, если они начинаются без взаимодействия с пользователем и не поддерживаются проверкой репутации приложений по данным SmartScreen.** Пользователи могут переопределять и продолжать загрузку, щелкнув правой кнопкой мыши и выбрав параметр "Keep" ("Сохранить") на элементе загрузки. Администраторы предприятия могут отказаться от этого, настроив следующую политику:
  - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings.md) – Отключение предупреждений о расширениях загружаемых файлов для определенных типов файлов в доменах

    Дополнительные сведения см. в [Перебои загрузок Microsoft Edge Security](microsoft-edge-security-downloads-interruptions.md).

- **Поддержка API распознавания речи.** Начиная с Microsoft Edge версии 91, добавляется поддержка API команд распознавания речи на Google.com и аналогичных сайтах. Эта возможность доступна только случайно выбранной группе пользователей, участвующих в эксперименте. Эти пользователи предоставляют отзывы службе поддержки.

- **Персонализация браузера с помощью новых цветовых тем.** Персонализируйте Microsoft Edge с помощью одной из четырнадцати новых цветовых тем на странице "Параметры - > Внешний вид". Вы также можете установить настраиваемые темы с сайта надстроек Microsoft Edge. [Подробнее](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено шесть новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Добавлены следующие новые политики:

- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) — идентификация трафика Application Guard
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) — явно разрешенные сетевые порты
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) — разрешение импорта параметров страниц запуска
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) — позволяет пользователям вставлять фрагменты математических задач и получать решение с пошаговым объяснением в Microsoft Edge
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) — разрешает содержимое Microsoft News на новой странице вкладки
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) — разрешает быстрые ссылки на новой странице вкладки

#### <a name="obsoleted-policy"></a>Устаревшая политика

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) — включает упреждающую проверку подлинности
<!-- end major 91 -->

## <a name="version-90081866-may-20"></a>Версия 90.0.818.66: 20 мая

Исправлены ошибки и проблемы с производительностью.

## <a name="version-90081862-may-13"></a>Версия 90.0.818.62: 13 мая

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#may-13-2021).

## <a name="version-90081856-may-6"></a>Версия 90.0.818.56: 6 мая

Исправлены ошибки и проблемы с производительностью.

## <a name="version-90081851-april-29"></a>Версия 90.0.818.51: 29 апреля

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#april-29-2021).

## <a name="version-90081849-april-26"></a>Версия 90.0.818.49: 26 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-90081846-april-22"></a>Версия 90.0.818.46: 22 апреля ##

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#april-22-2021).

## <a name="version-90081842-april-19"></a>Версия 90.0.818.42: 19 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-90081841-april-16"></a>Версия 90.0.818.41: 16 апреля ##

> [!Important]
>Это обновление содержит исправление для уязвимости [CVE-2021-21224](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21224), которая, по сообщениям группы разработчиков Chromium, имеет действующий эксплойт. Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide).

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#april-16-2021).

## <a name="version-90081839-april-15"></a>Версия 90.0.818.39: 15 апреля ##

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#april-15-2021).

## <a name="feature-updates"></a>Обновления компонентов ##

-    **Единый вход (SSO) теперь доступен для учетных записей Azure Active Directory (Azure AD) и Microsoft Account (MSA) на macOS.** Пользователь, вошедший в систему в Microsoft Edge на macOS, автоматически получает вход на веб-сайты, настроенные на единый вход с помощью рабочей учетной записи и учетной записи Майкрософт (например, bing.com, office.com, msn.com и outlook.com).

- **Режим терминала** Начиная с Microsoft Edge версии 90, мы заблокировали параметры печати пользовательского интерфейса, чтобы разрешить только настроенные принтеры и параметры "Печать в PDF". Кроме того, мы усовершенствовали режим терминала с одним приложением, чтобы ограничить запуск других приложений из браузера. Дополнительные сведения о функциях режима терминала см. [здесь.](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features)

- **Прерывание загрузки** Начиная с Microsoft Edge версии 91 браузер автоматически прерывает загрузки типов, которые могут нанести вред вашему компьютеру, если они начинаются без взаимодействия с пользователем и не поддерживаются проверкой репутации приложений SmartScreen. Пользователи могут переопределять и продолжать загрузку, щелкнув правой кнопкой мыши и выбрав параметр "Keep" ("Сохранить") на элементе загрузки.
Администраторы предприятия могут отказаться от этого с помощью одной из этих двух политик:
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) – Отключение предупреждений о расширениях загружаемых файлов для определенных типов файлов в доменах. Дополнительные сведения см. в статье [Перебои загрузок в Microsoft Edge Security](/deployedge/microsoft-edge-security-downloads-interruptions)

- **Печать**:

    - **Новый режим растеризации печати для принтеров без PostScript.** Начиная с Microsoft Edge версии 90, администраторы могут использовать новую политику для определения режима растеризации печати для своих пользователей. Эта политика управляет печатью из Microsoft Edge на принтерах в Windows без PostScript. Иногда для правильной печати на принтерах без поддержки PostScript необходимо правильно растеризовать задания для печати. Возможные настройки - Полная и Быстрая.
    
  - **Дополнительные параметры масштабирования страниц для печати.** Теперь пользователи могут настраивать масштабирование при печати веб-страниц и документов PDF с помощью дополнительных параметров. Параметр "Вписать на страницу" гарантирует, что веб-страница или документ вписываются в пространство, доступное в выбранном для печати "Размере бумаги". Значение "Фактический размер" гарантирует, что размер печатаемого контента не изменится независимо от выбранного "Размера бумаги".

-   **Производительность:**

    -   **Предложения по автозаполнению стали более разнообразными – теперь они включают в себя содержимое адресных полей из буфера обмена.** При нажатии на поле профиля или адреса (такое как телефон, электронная почта, почтовый индекс, город, область и т.д.) происходит разбор содержимого буфера обмена и результаты выводятся в качестве предложений автозаполнения.

    -   **Пользователи могут искать предложения автозаполнения, даже если форма или поле не обнаружены.** Теперь, если у вас есть сведения, сохраненные в Microsoft Edge, предложения по автозаполнению всплывают автоматически, помогая сэкономить время при заполнении форм. Если автозаполнение не работает для формы или если вы хотите получить данные в формах, обычно не имеющих автозаполнения (например, временные формы), вы можете искать информацию с помощью автозаполнения.

-   **Доступ к загрузкам из раскрывающегося меню в панели меню.** Загрузки будут показаны в правом верхнем углу, причем все загрузки, активные в данный момент, будут располагаться рядом. Это меню легко закрыть, чтобы продолжать просматривать веб-страницу и при этом отслеживать общий ход скачивания прямо на панели инструментов. [Подробнее](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).

-   **Улучшения визуализации шрифтов.** Начиная с Microsoft Edge версии 90, мы улучшили визуализацию текста для повышения четкости и уменьшения размытости. Часть улучшений отрисовки шрифтов появится уже в бета-версии 90, но будет отключена по умолчанию.

- **Детский режим.** Мы обновили политику, чтобы при ее включении она отключала функцию детского режима в дополнение к семейной безопасности. Дополнительные сведения о детском режиме см. [здесь](https://go.microsoft.com/fwlink/?linkid=2146910)

## <a name="policy-updates"></a>Обновления политик

## <a name="new-policies"></a>Новые политики

Добавлено восемь новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Добавлены следующие новые политики:
-   [ApplicationGuardFavoritesSyncEnabled](/DeployEdge/microsoft-edge-policies#applicationguardfavoritessyncenabled) — включена синхронизация избранного Application Guard
- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) Идентификация трафика Application Guard
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) Явно разрешенные сетевые порты
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) Разрешение импорта параметров страниц запуска
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) Позволяет пользователям вставлять фрагменты математических задач и получать решение с пошаговым объяснением в Microsoft Edge
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) Разрешает содержимое Microsoft News на новой странице вкладки
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) Разрешает быстрые ссылки на новой странице вкладки
-   [FetchKeepaliveDurationSecondsOnShutdown](/DeployEdge/microsoft-edge-policies#fetchkeepalivedurationsecondsonshutdown) Получение сведений о продолжительности активности при завершении работы
-   [ManagedConfigurationPerOrigin](/DeployEdge/microsoft-edge-policies#managedconfigurationperorigin) — задает управляемые значения конфигурации для веб-сайтов в определенных источниках
-   [PrintRasterizationMode](/DeployEdge/microsoft-edge-policies#printrasterizationmode) — режим растеризации печати
-   [QuickViewOfficeFilesEnabled](/DeployEdge/microsoft-edge-policies#quickviewofficefilesenabled) — управление возможностями быстрого просмотра файлов Office в Microsoft Edge
-   [SSLErrorOverrideAllowedForOrigins](/DeployEdge/microsoft-edge-policies#sslerroroverrideallowedfororigins) — разрешить пользователям переходить дальше со страницы предупреждения HTTPS для определенных источников
-   [WindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#windowocclusionenabled) — включить загораживание окна
-   [WindowsHelloForHTTPAuthEnabled](/DeployEdge/microsoft-edge-policies#windowshelloforhttpauthenabled) — включена Windows Hello для HTTP Auth

## <a name="deprecated-policies"></a>Нерекомендуемые политики

- [ProactiveAuthEnabled](/DeployEdge/microsoft-edge-policies#proactiveauthenabled) Включает упреждающую проверку подлинности.
-   [NativeWindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) — включить встроенное загораживание окна
-   [SSLVersionMin](/DeployEdge/microsoft-edge-policies#sslversionmin)— включена минимальная версия TLS

## <a name="version-89077477-april-14"></a>Версия 89.0.774.77: 14 апреля

> [!Important]
>Это обновление содержит исправление для уязвимостей [CVE-2021-21206](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21206) и [CVE-2021-21220](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21220), которые, по сообщениям группы разработчиков Chromium, имеют действующий эксплойт.  Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide).

Стабильные обновления безопасности канала перечислены [здесь](/deployedge/microsoft-edge-relnotes-security#april-14-2021).

## <a name="version-89077476-april-12"></a>Версия 89.0.774.76: 12 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-89077475-april-8"></a>Версия 89.0.774.75: 8 апреля

Исправлены ошибки и проблемы с производительностью.

## <a name="version-89077468-april-1"></a>Версия 89.0.774.68: 1 апреля

Стабильные обновления безопасности канала перечислены [здесь](./microsoft-edge-relnotes-security.md#april-1-2021).

## <a name="version-89077463-march-25"></a>Версия 89.0.774.63: 25 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-89077457-march-18"></a>Версия 89.0.774.57: 18 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-89077454-march-13"></a>Версия 89.0.774.54: 13 марта

> [!IMPORTANT]
> В этом обновлении [содержится CVE-2021-21193,](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21193) который, по сообщениям группы Chromium, имеет действующий эксплойт. Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide).

Стабильные обновления безопасности канала перечислены [здесь](./microsoft-edge-relnotes-security.md#march-13-2021).

## <a name="version-89077450-march-10"></a>Версия 89.0.774.50: 10 марта

Исправлены ошибки и проблемы с производительностью.

## <a name="version-89077448-march-8"></a>Версия 89.0.774.48: 8 марта

Исправлены ошибки и проблемы с производительностью.

<!-- begin major 89 -->
## <a name="version-89077445-march-4"></a>Версия 89.0.774.45: 4 марта

> [!IMPORTANT]
> Это обновление содержит уязвимость [CVE-2021-21166](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21166), которая согласно отчету команды Chromium имеет эксплойты на практике. Дополнительные сведения см. в [руководстве по обновлению для системы безопасности](https://msrc.microsoft.com/update-guide).

Стабильные обновления безопасности канала перечислены [здесь](./microsoft-edge-relnotes-security.md#march-4-2021).

### <a name="resolved-issues"></a>Устраненные проблемы

- **Обновления и исправления ярлыков панели задач и меню Пуск:**
  - Щелкнув правой кнопкой мыши ярлык Microsoft Edge в меню "Пуск", вы увидите функцию открепления Microsoft Edge от панели задач при его закреплении.
  - Начальные макеты, включающие [конфигурацию панели задач](/windows/configuration/configure-windows-10-taskbar) для закрепления Microsoft Edge на панели задач, больше не приведут к тому, что второй ярлык Microsoft Edge будет закреплен на панели задач.
  - Организации, использующие профили роуминга Windows, больше не будут видеть пустой белый значок на месте значка Microsoft Edge на панели задач при входе пользователей в Windows.

### <a name="feature-updates"></a>Обновления компонентов

- **Режим терминала включает дополнительные возможности блокировки.** Начиная с Microsoft Edge версии 89, мы добавили дополнительные возможности блокировки в режиме терминала, чтобы пользователи могли работать эффективно и безопасно. [Подробнее](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **Средство Enterprise Mode Site List Manager будет доступно в браузере на странице *edge://compat***. Это средство можно использовать для создания, изменения и экспорта XML списка сайтов для режима Internet Explorer в Microsoft Edge. Доступ к этому средству можно получить при необходимости с помощью групповой политики. [Подробнее](./edge-ie-mode-site-list-manager.md).

- **Повышение производительности браузера с помощью спящих вкладок**. Функция спящих вкладок повышает производительность браузера, переводя неактивные вкладки в спящий режим, чтобы освободить системные ресурсы, такие как память и процессор, и использовать их для активных вкладок или других приложений. Пользователи могут предотвратить переход сайтов в спящий режим и настроить время, по истечении которого неактивная вкладка перейдет в спящий режим. Чтобы пользователи могли оставаться в потоке, существуют также [эвристические методы](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434), которые предотвращают переход определенных сайтов, например сайтов интрасети, в спящий режим. Управлять этой возможностью можно с помощью групповых политик.

- **Сброс данных синхронизации Microsoft Edge в облаке вручную**. Мы представляем способ сброса данных синхронизации Microsoft Edge из продукта. Это гарантирует очистку данных из служб Майкрософт, а также устранение определенных проблем с продуктом, которые ранее требовали передачи заявки в службу поддержки.

- **Интеллектуальный единый вход (SSO Windows Azure) для всех учетных записей Active Directory (Azure AD) Windows Azure для пользователей с одним профилем Microsoft Edge, не входящим в Azure AD**.  Автоматически включите этот параметр для пользователей, которые могут извлечь больше всего пользы из этой функции. Если у пользователя есть только один профиль Microsoft Edge (и это не Azure AD и не Kids Mode), параметр будет автоматически включен при запуске Microsoft Edge. Этот автоматический переключатель также автоматически отключится, если пользователь позже решит войти в другой профиль Microsoft Edge с учетной записью Azure AD. Из этого профиля пользователи могут вручную обновлять свои настройки этой функции на странице **Параметры > Профили >Профили > Разрешить один вход** для работы или школьных сайтов.

- **Усовершенствования в области выделения текста в документах PDF**. Пользователи начнут более плавный и согласованный выбор текста в документах PDF, открытых в Microsoft Edge, начиная с версии 89.

- **Поле даты рождения теперь поддерживается автозаполнением**. В настоящее время Microsoft Edge позволяет сэкономить время и усилия при заполнении форм и создании учетных записей в Интернете путем автоматического заполнения таких данных, как адреса, имена, номера телефонов и т. д. Начиная с Microsoft Edge версии 89, мы добавляем поддержку для другого поля, которое можно сохранить и заполнить автоматически — дата рождения. Вы можете просматривать, изменять и удалять эти сведения в любое время в параметрах профиля.

### <a name="policy-updates"></a>Обновления политик

#### <a name="new-policies"></a>Новые политики

Добавлено семь новых политик. Скачайте обновленные административные шаблоны на [целевой странице Microsoft Edge Enterprise](https://www.microsoft.com/edge/business/download). Добавлены следующие новые политики.

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) — параметры времени существования данных браузера
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled) — управление мобильными приложениями включено
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) — определение упорядоченного списка предпочитаемых языков, на которых должны отображаться веб-сайты, если сайт поддерживает этот язык
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) — разрешение рекомендаций и рекламных уведомлений от Microsoft Edge
- [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) — ограничение режима печати фона
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault) — режим печати фоновой графики по умолчанию
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist) — блокировка интеллектуальных действий для списка служб

#### <a name="obsoleted-policies"></a>Устаревшие политики

Ниже приводятся устаревшие политики.

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) — использование политики ссылок по умолчанию для no-referrer-when-downgrade
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) — включение отчетов с данными об использовании и сбоях
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) — отправка сведений о сайте для улучшения служб Майкрософт
<!-- end major 89 -->

<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
