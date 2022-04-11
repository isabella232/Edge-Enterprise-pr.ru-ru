---
title: Узнайте, как настроить начальные параметры в Microsoft Edge.
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 03/23/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Узнайте, как настроить начальные параметры в Microsoft Edge.
ms.openlocfilehash: 751097853e02589fe1b900f6af0d290feb5fbe67
ms.sourcegitcommit: dd8cdbd35726c795ddce917e549ddf17ee7f5290
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/11/2022
ms.locfileid: "12473408"
---
# <a name="configure-microsoft-edge-using-initial-preferences-settings-for-the-first-run"></a>Настройка Microsoft Edge с помощью параметров начальных предпочтений для первого запуска

Сведения, указанные в этой статье, помогут Microsoft Edge параметры начальных параметров на Windows устройствах.

> [!Note]
> Эта статья относится к Microsoft Edge версии 93 или более поздней.

## <a name="configure-policy-settings-on-windows"></a>Настройка параметров политики в Windows

Начиная Microsoft Edge версии 93, корпорация Майкрософт поддерживает ограниченное количество начальных параметров( прежнее название — "Главные настройки"), чтобы помочь администраторам настроить браузеры для первого запуска. Дополнительные сведения см. в поддерживаемых параметрах в следующей таблице [параметров предпочтений](#preference-settings) .

При развертывании начальные настройки выступают в качестве параметров браузера по умолчанию на управляемых устройствах. Эти параметры являются предпочтительными администраторами для использования в качестве параметров браузера по умолчанию для первого запуска.

> [!NOTE]
> Начальные настройки могут быть изменены пользователями и недоступны для некоторых устройств, так как они не присоединены к домену Active Directory®.

Некоторые примеры параметров начальных параметров включают начальную конфигурацию домашней страницы по умолчанию или вкладок с определенными URL-адресами.

Параметры копируются только один *раз* из initial_preferences файла, изменения, внесенные в этот файл после настройки, не учитываются. Если параметр управляется политикой Microsoft Edge [и](/deployedge/microsoft-edge-policies) настраивается в файле *initial_preferences, политика* всегда имеет приоритет.

### <a name="preference-settings"></a>Параметры предпочтений

В следующей таблице показаны параметры, которые в настоящее время поддерживаются Microsoft Edge.

| Категория "Параметры" | Параметр |
| - | - |
| Bookmark_bar | show_apps_shortcut<br>show_managed_bookmarks<br>show_on_all_tabs |
| Bookmarks | editing_enabled |
| Браузер или clear_data | browsing_history<br>browsing_history_basic"<br>Кэша<br>cache_basic<br>Печенье<br>download_history<br>form_data<br>Пароли |
| Журнал | browsing_history<br>Кэша<br>Печенье<br>download_history<br>form_data<br>hosted_apps_data<br>Пароли<br>site_settings |
| Browser | first_run_tabs<br>dark_theme<br>show_toolbar_bookmarks_button<br>show_toolbar_collections_butto<br>show_toolbar_downloads_button<br>show_home_button<br>show_prompt_before_closing_tabs<br>show_toolbar_history_button |
| default_search_provider | [default_search_provider] включено |
| Полноэкранный режим | Разрешено |
| домашнюю страницу | Homepage_url |
| homepage_is_newtabpage | homepage_is_newtabpage |
| Сессии | restore_on_startup<br>startup_urls |
| Расширения | Расширения: параметры |

## <a name="1-download-an-example-initial_preferences-file"></a>1. Скачивание примера initial_preferences файла

Чтобы приступить к работе, скачайте файл Policy с целевой [Microsoft Edge Enterprise страницы](https://www.microsoft.com/edge/business/download). Извлеките файлы в скачанный файл, а затем откройте *initial_preferences в* *папке примеров* . На следующем снимке экрана показаны параметры файла политики, доступные для скачивания

:::image type="content" source="media/initial-preferences-support-on-microsoft-edge-browser/edge-policy-files.png" alt-text="Microsoft Edge файлов политики, доступных для скачивания.":::

## <a name="2-customize-and-validate-the-initial_preferences-file"></a>2. Настройка и проверка initial_preferences файла

Настройте параметры параметров в загруженном *initial_preferences и проверьте* изменения, чтобы убедиться, что в коде JSON нет ошибок. Если вы обнаружите ошибки, проверьте синтаксис и структуру ** файла initial_preferences, внесите исправления и проверьте его еще раз. Несколько примеров инструментов для проверки JSON, [онлайн-инструментов JSON](https://jsonformatter.org/) или редактирования [JSON в Visual Studio Code](https://code.visualstudio.com/docs/languages/json).

## <a name="3-deploy-preferences-to-users-computer"></a>3. Развертывание параметров на компьютере пользователей

Разверните *initial_preferences* на устройствах пользователей одновременно с развертыванием Microsoft Edge и поместите файл в следующее расположение на устройстве.

### <a name="windows-amd64-and-arm64"></a>Windows (AMD64 и ARM64)

| Канал | Местоположение |
| - | - |
| Stable | `"C:\Program Files (x86)\Microsoft\Edge\Application"` |
| Beta | `"C:\Program Files (x86)\Microsoft\Edge Beta\Application"` |
|Canary | `"%LOCALAPPDATA%\Microsoft\Edge SxS\Application"` |
| Dev | `"C:\Program Files (x86)\Microsoft\Edge Dev\Application"` |

> [!NOTE]
> Файл *initial_preferences* должен быть развернут в той же папке, что * и *msedge.exeна компьютерах Windows пользователей.  

### <a name="macos"></a>macOS

| Канал | Местоположение |
| - | - |
| Stable | `"~/Library/Application Support/Microsoft Edge/Microsoft Edge Initial Preferences"` |
| Beta | `“~/Library/Application Support/Microsoft Edge Beta/Microsoft Edge Initial Preferences"` |
| Canary | `“~/Library/Application Support/Microsoft Edge Canary/Microsoft Edge Initial Preferences"` |
| Dev | `"~/Library/Application Support/Microsoft Edge Dev/Microsoft Edge Initial Preferences"` |

## <a name="important-notes-msi--pkg-deployment-and-initial_preferences-interaction"></a>Важные примечания: MSI/ Pkg Deployment и *initial_preferences* взаимодействия

Начальные настройки вступает в силу только после *initial_preferences* развертывания файла перед первым запуском браузера конечными пользователями.  

## <a name="see-also"></a>См. также

- [Пример *initial_prefrences* шаблона](/edge/business/download)
