---
title: Узнайте, как настроить начальные предпочтения в Microsoft Edge.
ms.author: collw
author: AndreaLBarr
manager: srugh
ms.date: 07/27/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Узнайте, как настроить начальные предпочтения в Microsoft Edge.
ms.openlocfilehash: 06452996be4e2f1e2c40bfc5ba1753b9d2b7b222
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445664"
---
# <a name="configure-microsoft-edge-using-initial-preferences-settings-for-the-first-run"></a>Настройка Microsoft Edge с помощью параметров начальных предпочтений для первого запуска

Используйте сведения в этой статье для настройки Microsoft Edge параметров начальных предпочтений на Windows устройствах.

> [!Note]
> Эта статья применима к Microsoft Edge версии 93 или более поздней версии.

## <a name="configure-policy-settings-on-windows"></a>Настройка параметров политики в Windows

Начиная Microsoft Edge выпуска 93, Корпорация Майкрософт поддерживает ограниченное число начальных предпочтений, ранее именуемых "Master Preferences", чтобы помочь администраторам настроить браузеры для первого запуска. Дополнительные сведения см. в таблице поддерживаемых параметров в следующей таблице [Параметры предпочтений](#preference-settings) .

При развертывании начальные предпочтения выступают в качестве параметров браузера по умолчанию на управляемых устройствах. Эти параметры — это параметры, которые администраторы предпочитают использовать в качестве параметров браузера по умолчанию для первого запуска.

> [!NOTE]
> Начальные предпочтения могут быть изменены пользователями и недоступны для некоторых устройств, так как они не присоединились к домену Active Directory®.

Некоторые примеры параметров начальных предпочтений включают начальную конфигурацию домашней страницы по умолчанию или вкладок с определенными URL-адресами.

Предпочтения копируется только один *раз* из initial_preferences, изменения, внесенные в этот файл после того, как конфигурация не будет соблюдаться. Если параметр управляется политикой Microsoft Edge [и](/deployedge/microsoft-edge-policies) настроен в файле *initial_preferences, политика* всегда имеет приоритет.

### <a name="preference-settings"></a>Параметры предпочтений

В следующей таблице показаны параметры, поддерживаемые Microsoft Edge.

| Категория "Предпочтения" | Параметр |
| - | - |
| Bookmark_bar | show_apps_shortcut<br>show_managed_bookmarks<br>show_on_all_tabs |
| Bookmarks | editing_enabled |
| Браузер / clear_data | browsing_history<br>browsing_history_basic"<br>кэш<br>cache_basic<br>cookies<br>download_history<br>form_data<br>пароли |
| Журнал | browsing_history<br>кэш<br>cookies<br>download_history<br>form_data<br>hosted_apps_data<br>пароли<br>site_settings |
| Browser | first_run_tabs<br>dark_theme<br>show_toolbar_bookmarks_button<br>show_toolbar_collections_butto<br>show_toolbar_downloads_button<br>show_home_button<br>show_prompt_before_closing_tabs<br>show_toolbar_history_button |
| default_search_provider | Включено [default_search_provider] |
| Полноэкранный режим | Разрешено |
| домашнюю страницу | Homepage_url |
| homepage_is_newtabpage | homepage_is_newtabpage |
| Сеанс | restore_on_startup<br>startup_urls |
| Расширения | Расширения: параметры |

## <a name="1-download-an-example-initial_preferences-file"></a>1. Скачайте пример initial_preferences файла

Чтобы начать работу, скачайте файл "Политика" с [Microsoft Edge Enterprise страницы](/edge/business/download). Извлеките файлы в скачивке, а затем *откройте initial_preferences* файл в *папке примеры* . На следующем скриншоте показаны доступные для скачивания параметры файлов политики

:::image type="content" source="media/initial-preferences-support-on-microsoft-edge-browser/edge-policy-files.png" alt-text="Microsoft Edge файлы политик, доступные для скачивания.":::

## <a name="2-customize-and-validate-the-initial_preferences-file"></a>2. Настройка и проверка initial_preferences файла

Настройка параметров предпочтений в загруженных файлах initial_preferences проверку изменений, чтобы убедиться, что в коде JSON нет ошибок.** Если вы нашли ошибки, проверьте синтаксис и структуру файла ** initial_preferences, внести исправления и снова проверить его. Несколько примеров инструментов для проверки JSON, Online [JSON Tools](https://jsonformatter.org/) или [редактирования JSON в Visual Studio Code](https://code.visualstudio.com/docs/languages/json).

## <a name="3-deploy-preferences-to-users-computer"></a>3. Развертывание предпочтений на компьютере пользователей

Развертывание *initial_preferences* на устройствах пользователей одновременно с развертыванием Microsoft Edge и размещение файла в следующем расположении на устройстве.

### <a name="windows-amd64-and-arm64"></a>Windows (AMD64 и ARM64)

| Канал | Местонахождение |
| - | - |
| Stable | `"C:\Program Files (x86)\Microsoft\Edge\Application"` |
| Beta | `"C:\Program Files (x86)\Microsoft\Edge Beta\Application"` |
|Canary | `"%LOCALAPPDATA%\Microsoft\Edge SxS\Application"` |
| Dev | `"C:\Program Files (x86)\Microsoft\Edge Dev\Application"` |

> [!NOTE]
> Файл *initial_preferences* должен быть развернут в той же папке, что * иmsedge.exe* на компьютерах Windows пользователей.  

### <a name="macos"></a>macOS

| Канал | Местонахождение |
| - | - |
| Stable | `"~/Library/Application Support/Microsoft Edge/Microsoft Edge Initial Preferences"` |
| Beta | `“~/Library/Application Support/Microsoft Edge Beta/Microsoft Edge Initial Preferences"` |
| Canary | `“~/Library/Application Support/Microsoft Edge Canary/Microsoft Edge Initial Preferences"` |
| Dev | `"~/Library/Application Support/Microsoft Edge Dev/Microsoft Edge Initial Preferences"` |

## <a name="important-notes-msi--pkg-deployment-and-initial_preferences-interaction"></a>Важные заметки: MSI / Pkg Deployment и *initial_preferences* взаимодействия

Первоначальные предпочтения вступает в силу только после развертывания *initial_preferences* перед первым запуском браузера конечными пользователями.  

## <a name="see-also"></a>См. также

- [Файл *шаблона initial_prefrences* пример](/edge/business/download)
