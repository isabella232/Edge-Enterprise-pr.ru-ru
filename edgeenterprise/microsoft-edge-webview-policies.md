---
title: Документация по политикам Microsoft Edge WebView2
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 04/08/2022
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Документация Windows и Mac для всех политик, поддерживаемых браузером Microsoft Edge
ms.openlocfilehash: d785ab4a06a6972dcc8d85b560bbae5049c9d314
ms.sourcegitcommit: dd8cdbd35726c795ddce917e549ddf17ee7f5290
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/11/2022
ms.locfileid: "12473600"
---
# <a name="microsoft-edge-webview2---policies"></a>Политики Microsoft Edge WebView2

Последняя версия Microsoft Edge WebView2 включает в себя следующие политики. Эти политики можно использовать для настройки работы Microsoft Edge WebView2 в вашей организации.

Информацию о дополнительном наборе политик, используемых для управления тем, как и когда обновляется Microsoft Edge WebView2, можно найти в [справочнике по политике обновления Microsoft Edge](microsoft-edge-update-policies.md).


> [!NOTE]
> Эта статья относится к Microsoft Edge версии 87 или более поздней.

## <a name="available-policies"></a>Доступные политики

В этих таблицах перечислены все групповые политики, доступные в этом выпуске Microsoft Edge WebView2. Для получения дополнительных сведений о конкретных политиках см. ссылки в таблице.

- [Параметры переопределения загрузчика](#loader-override-settings)
- [Дополнительно](#additional)


### [*<a name="loader-override-settings"></a>Параметры переопределения загрузчика*](#loader-override-settings-policies)

|Имя политики|Заголовок|
|-|-|
|[BrowserExecutableFolder](#browserexecutablefolder)|Настройка расположения папки исполняемого файла браузера|
|[ReleaseChannelPreference](#releasechannelpreference)|Настройка предпочитаемого порядка поиска каналов выпуска|
### [*<a name="additional"></a>Дополнительно*](#additional-policies)

|Имя политики|Заголовок|
|-|-|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Управлять связью со Службой экспериментов и конфигурации|




  ## <a name="loader-override-settings-policies"></a>Политики "Параметры переопределения загрузчика"

  [В начало](#microsoft-edge-webview2---policies)

  ### <a name="browserexecutablefolder"></a>BrowserExecutableFolder

  #### <a name="configure-the-location-of-the-browser-executable-folder"></a>Настройка расположения папки исполняемого файла браузера

  
  
  #### <a name="supported-versions"></a>Поддерживаемые версии:

  - В Windows 87 и более поздних версий

  #### <a name="description"></a>Описание

  Эта политика настраивает приложения WebView2, чтобы использовать среду выполнения WebView2 по указанному пути. Папка должна содержать следующие файлы: msedgewebview2.exe, msedge.dll и т. д.

Чтобы задать значение для пути к папке, предоставьте имя и пару значения. Задайте имя значения для идентификатора пользовательской модели приложения или имя исполняемого файла. Вы можете использовать подстановочный знак "*" в качестве имени значения для применения ко всем приложениям.

  #### <a name="supported-features"></a>Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### <a name="data-type"></a>Тип данных:

  - Список строк

  #### <a name="windows-information-and-settings"></a>Сведения и параметры Windows

  ##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: BrowserExecutableFolder
  - Имя групповой политики: Настройка расположения папки исполняемого файла браузера
  - Путь к групповой политике (обязательно): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings
  - Путь GP (рекомендуется): N/A
  - Имя ADMX-файла групповой политики: MSEdgeWebView2.admx

  ##### <a name="windows-registry-settings"></a>Параметры реестра Windows

  - Путь (обязательно): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder
  - Путь (рекомендуется): N/A
  - Имя значения: список REG_SZ
  - Тип значения: список REG_SZ

  ##### <a name="example-value"></a>Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [В начало](#microsoft-edge-webview2---policies)

  ### <a name="releasechannelpreference"></a>ReleaseChannelPreference

  #### <a name="set-the-release-channel-search-order-preference"></a>Настройка предпочитаемого порядка поиска каналов выпуска

  
  
  #### <a name="supported-versions"></a>Поддерживаемые версии:

  - В Windows 87 и более поздних версий

  #### <a name="description"></a>Описание

  Порядок поиска каналов по умолчанию — среда выполнения WebView2, Beta, Dev и Canary.

Чтобы установить обратный порядок поиска по умолчанию, задайте для этой политики значение 1.

Чтобы задать значение для предпочитаемого канала выпуска, предоставьте имя и пару значения. Задайте имя значения для идентификатора пользовательской модели приложения или имя исполняемого файла. Вы можете использовать подстановочный знак "*" в качестве имени значения для применения ко всем приложениям.

  #### <a name="supported-features"></a>Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### <a name="data-type"></a>Тип данных:

  - Список строк

  #### <a name="windows-information-and-settings"></a>Сведения и параметры Windows

  ##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)

  - Уникальное имя групповой политики: ReleaseChannelPreference
  - Имя групповой политики: Настройка предпочитаемого порядка поиска каналов выпуска
  - Путь к групповой политике (обязательно): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings
  - Путь GP (рекомендуется): N/A
  - Имя ADMX-файла групповой политики: MSEdgeWebView2.admx

  ##### <a name="windows-registry-settings"></a>Параметры реестра Windows

  - Путь (обязательно): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference
  - Путь (рекомендуется): N/A
  - Имя значения: список REG_SZ
  - Тип значения: список REG_SZ

  ##### <a name="example-value"></a>Пример значения:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference = "Name: *, Value: 1"

```

  

  [В начало](#microsoft-edge-webview2---policies)

  ## <a name="additional-policies"></a>Дополнительные политики

  [В начало](#microsoft-edge-webview2---policies)

  ### <a name="experimentationandconfigurationservicecontrol"></a>ExperimentationAndConfigurationServiceControl

  #### <a name="control-communication-with-the-experimentation-and-configuration-service"></a>Управлять связью со Службой экспериментов и конфигурации

  
  
  #### <a name="supported-versions"></a>Поддерживаемые версии:

  - На Windows 97 или более поздней

  #### <a name="description"></a>Описание

  Служба эксперимента и конфигурации используется для развертывания полезной нагрузки эксперимента и конфигурации в клиенте.

Полезная нагрузка для экспериментов состоит из списка ранних функций разработки, которые Microsoft предоставляет для тестирования и обратной связи.

Полезная нагрузка конфигурации состоит из списка рекомендуемых параметров, которые Microsoft хочет развернуть для оптимизации взаимодействия с пользователем.

Полезная нагрузка конфигурации может также содержать список действий, которые необходимо выполнить для определенных доменов по причинам совместимости. Например, браузер может переопределить строку пользовательского агента на веб-сайте, если этот веб-сайт поврежден. Каждое из этих действий должно быть временным, пока Microsoft пытается решить проблему с владельцем сайта.

Если вы зададите для этой политики режим «FullMode», полная полезная нагрузка будет загружена из Службы экспериментов и конфигурации. Это включает в себя как экспериментальные, так и конфигурационные данные.

Если вы установите эту политику в режим "ConfigurationsOnlyMode", будет скачана только полезная нагрузка конфигурации.

Если для этой политики задано значение "RestrictedMode", взаимодействие со Службой экспериментов и конфигурации останавливается. Корпорация Майкрософт не рекомендует этот параметр.

Если вы не настроите эту политику, на управляемом устройстве в стабильных и бета-каналах поведение будет таким же, как в режиме "ConfigurationsOnlyMode". В каналах Canary и Dev поведение такое же, как и в "FullMode".

Если вы не настроите эту политику, на неуправляемом устройстве поведение будет таким же, как в режиме "FullMode".

Сопоставление параметров политики:

* FullMode (2) = Получить конфигурации и эксперименты

* ConfigurationsOnlyMode (1) = Получить только конфигурации

* RestrictedMode (0) = Отключить связь со Службой экспериментов и конфигурации

Используйте изложенные выше сведения при настройке этой политики.

  #### <a name="supported-features"></a>Поддерживаемые функции:

  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### <a name="data-type"></a>Тип данных:

  - целое число

  #### <a name="windows-information-and-settings"></a>Сведения и параметры Windows

  ##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)

  - Уникальное имя GP: ExperimentationAndConfigurationServiceControl
  - Имя GP: Управление связью со Службой Экспериментов и Конфигурации.
  - Путь к групповой политике (обязательно): Административные шаблоны/Microsoft Edge WebView2/
  - Путь GP (рекомендуется): N/A
  - Имя ADMX-файла групповой политики: MSEdgeWebView2.admx

  ##### <a name="windows-registry-settings"></a>Параметры реестра Windows

  - Путь (обязательно): SOFTWARE\Policies\Microsoft\Edge\WebView2
  - Путь (рекомендуется): N/A
  - Имя значения: ExperimentationAndConfigurationServiceControl
  - Тип значения: REG_DWORD

  ##### <a name="example-value"></a>Пример значения:

```
0x00000002
```

  

  [В начало](#microsoft-edge-webview2---policies)


## <a name="see-also"></a>См. также

- [Настройка Microsoft Edge](configure-microsoft-edge.md)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Блог базовых параметров безопасности Майкрософт](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)