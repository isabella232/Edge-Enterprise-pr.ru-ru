---
title: Создание переменных каталога с данными пользователя в Microsoft Edge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Инструкции по созданию переменных каталога с данными пользователя в Microsoft Edge
ms.openlocfilehash: 284bef9156dc3dff1413f349eebe4e7dac854a98
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980957"
---
# Создание переменных каталога с данными пользователя в Microsoft Edge

В этой статье объясняется, как можно использовать переменные каталога с данными вместо использования жестко заданных путей при изменении Microsoft Edge.

>[!NOTE]
>Эта статья относится к Microsoft Edge версии 77 или более поздней.

## Переменные пути

Политики для изменения путей к каталогам данных (например, для настройки переменных поддержки [UserDataDir](microsoft-edge-policies.md#userdatadir) или [DownloadDirectory](microsoft-edge-policies.md#downloaddirectory).) При настройке этих политик можно использовать переменные вместо жестко заданных путей. Например, для хранения данных профиля в разделе "Локальные данные приложения пользователя" в Windows вместо расположения по умолчанию. Задайте политике [UserDataDir](microsoft-edge-policies.md#userdatadir) значение **${local_app_data}\Edge\Profile**. В большинстве установок Windows 10 этот путь соответствует *C:\Users\\&lt;Current-user&gt;\AppData\Local\Microsoft\Edge\Profile*.

>[!NOTE]
>Если значение не задано, Microsoft Edge использует пути к каталогам по умолчанию. Пользователь может использовать флаг командной строки `--user-data-dir` для переопределения значения по умолчанию.

Чтобы просмотреть текущий **путь к профилю**, откройте страницу **О версии** (введите "edge://version"). **Путь профиля** следует этому формату: *C:\Users\\&lt;Current-user&gt;\AppData\Local\Microsoft\Edge\User Data\Default*.

### Руководство по использованию переменных пути

Перед использованием переменных для путей ознакомьтесь со следующими рекомендациями.

- Все политики, включающие пути к расположениям, в которых Microsoft Edge хранит разные данные, зависят от платформы. Некоторые из этих политик доступны только на определенных платформах, тогда как другие можно использовать на всех платформах.
- Во избежание ошибок, вызываемых приложениями, которые запускаются из разных расположений в различных условиях, проверьте, что пути являются абсолютными.
- Каждая переменная может быть использована в пути только один раз. Для большинства из них это единственный эффективный способ использовать переменные, так как они разрешаются в абсолютные пути.
- Почти все политики будут создавать путь, если его нет (по возможности в существующих обстоятельствах).
- Использование сетевых расположений для некоторых политик может привести к непредвиденным результатам из-за различий в том, как разные версии и каналы Microsoft Edge обрабатывают структуру папок.

### Поддерживаемые переменные пути

Microsoft Edge поддерживает следующие переменные пути.

#### Все платформы

| Переменная | Описание |
| --- | --- |
| **${user_name}** | Пользователь, использующий Microsoft Edge. Microsoft Edge учитывает идентификаторы SUID (установка ИД пользователя-владельца при выполнении). Пример: *audreysmall* |
| **${machine_name}** | Имя компьютера, возможно, содержащее доменное имя. Пример: *audreysmall* или *audrey.ex.contoso.com* |

#### Только Windows

| Переменная | Описание |
| --- | --- |
| **${documents}** | Папка "Документы" для текущего пользователя. Пример: *C:\Users\Administrator\Documents* |
|**${local_app_data}** | Папка "Данные приложения" для текущего пользователя. Пример: *C:\Users\Administrator\AppData\Local* |
|**${roaming_app_data}** | Папка "Перемещенные данные приложения" для текущего пользователя. Пример: *C:\Users\Administrator\AppData\Roaming* |
| **${profile}** | Домашняя папка для текущего пользователя. Пример: *C:\Users\Administrator* |
| **${global_app_data}** | Системная папка "Данные приложения". Пример: *C:\AppData* |
| **${program_files}** | Папка Program Files для текущего процесса. Эта папка зависит от того, используется 32-битный или 64-битный процесс. Пример разрешения: *C:\Program Files (x86)* |
| **${windows}** | Папка Windows. Пример: *C:\Windows* |
| **${client_name)** | Имя клиентского компьютера, подключенного к сеансу удаленного рабочего стола или Citrix. Эта переменная пуста, если она используется из локального сеанса. Если он используется в пути, добавьте к нему префикс, который гарантированно не будет пустым. Пример: *C:\edge_profiles\session_${client_name}* разрешается в *C:\edge_profiles\session_&lt;ForlocalSessions&gt;* и *C:\edge_profiles\session_&lt;SomePCname&gt;* для удаленных сеансов. |
| **${session_name}** | Имя активного сеанса. Используйте это имя для различения между несколькими одновременно подключенными удаленными сеансами, использующими один и тот же профиль пользователя. Пример: *WinSta0 for local desktop sessions* (WinSta0 для сеансов локального компьютера) |

#### Только macOS

| Переменная | Описание |
| --- | --- |
| **${users}** | Папка, в которой хранятся профили пользователей. Пример: */Users* |
| **${documents}** | Папка "Документы" для текущего пользователя. Пример: */Users/audreysmall/Documents* |

## Лицензия на содержимое

>[!NOTE]
>Некоторые части этой страницы представляют собой измененные материалы, созданные и предоставленные на сайте Chromium.org. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). Исходная страница Chromium находится [здесь](https://www.chromium.org/administrators/policy-list-3/user-data-directory-variables).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br/>Эта работа предоставляется в рамках международной лицензии <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)