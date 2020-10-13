---
title: Документация по политикам браузера Microsoft Edge
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 10/08/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Документация Windows и Mac для всех политик, поддерживаемых браузером Microsoft Edge
ms.openlocfilehash: 56abadf907dfffec733af2456cc20db36510880b
ms.sourcegitcommit: 4e6188ade942ca6fd599a4ce1c8e0d90d3d03399
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "11105769"
---
# Политики Microsoft Edge WebView2

Последняя версия Microsoft Edge WebView2 включает в себя следующие политики. Эти политики можно использовать для настройки работы Microsoft Edge WebView2 в вашей организации.

Информацию о дополнительном наборе политик, используемых для управления тем, как и когда обновляется Microsoft Edge WebView2, можно найти в [справочнике по политике обновления Microsoft Edge](microsoft-edge-update-policies.md).

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 87 или более поздней.

## Доступные политики
В этих таблицах перечислены все групповые политики, доступные в этом выпуске Microsoft Edge WebView2. Для получения дополнительных сведений о конкретных политиках см. ссылки в таблице.

|||
|-|-|
|[Параметры переопределения загрузчика](#loader-override-settings)|

### [*Параметры переопределения загрузчика*](#loader-override-settings-policies)
|Имя политики|Заголовок|
|-|-|
|[browserExecutableFolder](#browserexecutablefolder)|Настройка расположения папки исполняемого файла браузера|
|[releaseChannelPreference](#releasechannelpreference)|Настройка предпочитаемого порядка поиска каналов выпуска|




  ## Политики "Параметры переопределения загрузчика"

  [В начало](#microsoft-edge-webview2---policies)

  ### browserExecutableFolder
  #### Настройка расположения папки исполняемого файла браузера
  
  
  #### Поддерживаемые версии:
  - В Windows 87 и более поздних версий

  #### Описание
  Эта политика настраивает приложения WebView2, чтобы использовать среду выполнения WebView2 по указанному пути. Папка должна содержать следующие файлы: msedgewebview2.exe, msedge.dll и т. д.

Чтобы задать значение для пути к папке, предоставьте имя и пару значения. Задайте имя значения для идентификатора пользовательской модели приложения или имя исполняемого файла. Вы можете использовать подстановочный знак "*" в качестве имени значения для применения ко всем приложениям.

  #### Поддерживаемые функции:
  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:
  - Список строк

  #### Сведения и параметры Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: browserExecutableFolder
  - Имя групповой политики: Настройка расположения папки исполняемого файла браузера
  - Путь к групповой политике (обязательно): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings
  - Путь GP (рекомендуется): N/A
  - Имя ADMX-файла групповой политики: MSEdgeWebView2.admx
  ##### Параметры реестра Windows
  - Путь (обязательно): SOFTWARE\Policies\Microsoft\Edge\WebView2\browserExecutableFolder
  - Путь (рекомендуется): N/A
  - Имя значения: список REG_SZ
  - Тип значения: список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\WebView2\browserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```


  

  [В начало](#microsoft-edge-webview2---policies)

  ### releaseChannelPreference
  #### Настройка предпочитаемого порядка поиска каналов выпуска
  
  
  #### Поддерживаемые версии:
  - В Windows 87 и более поздних версий

  #### Описание
  Порядок поиска каналов по умолчанию — среда выполнения WebView2, Beta, Dev и Canary.

Чтобы установить обратный порядок поиска по умолчанию, задайте для этой политики значение 1.

Чтобы задать значение для предпочитаемого канала выпуска, предоставьте имя и пару значения. Задайте имя значения для идентификатора пользовательской модели приложения или имя исполняемого файла. Вы можете использовать подстановочный знак "*" в качестве имени значения для применения ко всем приложениям.

  #### Поддерживаемые функции:
  - Может быть обязательным: Да
  - Может быть рекомендовано: Нет
  - Обновление динамической политики: Да

  #### Тип данных:
  - Список строк

  #### Сведения и параметры Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: releaseChannelPreference
  - Имя групповой политики: Настройка предпочитаемого порядка поиска каналов выпуска
  - Путь к групповой политике (обязательно): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings
  - Путь GP (рекомендуется): N/A
  - Имя ADMX-файла групповой политики: MSEdgeWebView2.admx
  ##### Параметры реестра Windows
  - Путь (обязательно): SOFTWARE\Policies\Microsoft\Edge\WebView2\releaseChannelPreference
  - Путь (рекомендуется): N/A
  - Имя значения: список REG_SZ
  - Тип значения: список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\WebView2\releaseChannelPreference = "Name: *, Value: 1"

```


  

  [В начало](#microsoft-edge-webview2---policies)


## См. также
- [Настройка Microsoft Edge](configure-microsoft-edge.md)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Блог базовых параметров безопасности Майкрософт](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)