---
title: Документация по политикам Microsoft Edge WebView2
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 08/27/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Документация Windows и Mac для всех политик, поддерживаемых браузером Microsoft Edge
ms.openlocfilehash: e1cef7c960dd9ac51916499281f6247e09078fee
ms.sourcegitcommit: 5aeaeb85eba7572d1871ad55568a8bea4d4a4e5f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2021
ms.locfileid: "11934588"
---
# <a name="microsoft-edge-webview2---policies"></a>Политики Microsoft Edge WebView2

Последняя версия Microsoft Edge WebView2 включает в себя следующие политики. Эти политики можно использовать для настройки работы Microsoft Edge WebView2 в вашей организации.

Информацию о дополнительном наборе политик, используемых для управления тем, как и когда обновляется Microsoft Edge WebView2, можно найти в [справочнике по политике обновления Microsoft Edge](microsoft-edge-update-policies.md).


> [!NOTE]
> Эта статья относится к Microsoft Edge версии 87 или более поздней.

## <a name="available-policies"></a>Доступные политики

В этих таблицах перечислены все групповые политики, доступные в этом выпуске Microsoft Edge WebView2. Для получения дополнительных сведений о конкретных политиках см. ссылки в таблице.

- [Параметры переопределения загрузчика](#loader-override-settings)


### [*<a name="loader-override-settings"></a>Параметры переопределения загрузчика*](#loader-override-settings-policies)

|Имя политики|Заголовок|
|-|-|
|[BrowserExecutableFolder](#browserexecutablefolder)|Настройка расположения папки исполняемого файла браузера|
|[ReleaseChannelPreference](#releasechannelpreference)|Настройка предпочитаемого порядка поиска каналов выпуска|




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


## <a name="see-also"></a>См. также

- [Настройка Microsoft Edge](configure-microsoft-edge.md)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Блог базовых параметров безопасности Майкрософт](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)