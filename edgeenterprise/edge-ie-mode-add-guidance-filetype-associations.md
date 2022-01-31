---
title: Сопоставление расширений файлов с режимом Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/24/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Сопоставление расширений файлов с режимом Internet Explorer
ms.openlocfilehash: c7d72e94079ff35d8ffe49c068585b0c97d208cc
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2022
ms.locfileid: "12298257"
---
# <a name="associate-file-extensions-with-internet-explorer-mode"></a>Сопоставление расширений файлов с режимом Internet Explorer

>[!Note]
> 15 июня 2022 г. настольное приложение Internet Explorer 11 будет снято с службы поддержки. Чтобы увидеть список того, что имеется в области, [ознакомьтесь с этой задаваемой проблемой).](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549) Те же приложения и сайты IE11, которые вы используете сегодня, можно открывать в Microsoft Edge в режиме Internet Explorer. Дополнительные сведения см. [здесь](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

В этой статье объясняется, как сопоставить Microsoft Edge в режиме Internet Explorer с расширениями файлов для классических приложений.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 86 или более поздней версии.

## <a name="guidance-for-file-extension-association-with-internet-explorer-mode"></a>Руководство по сопоставлению расширений файлов с режимом Internet Explorer

В следующих инструкциях покажите запись, Microsoft Edge с режимом IE с типом файла \.mht. Используйте приведенные ниже инструкции, чтобы настроить сопоставление файлов.

> [!NOTE]
> Вы можете задать конкретные расширения файлов, которые будут открываться в режиме Internet Explorer по умолчанию, с помощью политики **Задать файл конфигурации сопоставлений по умолчанию**. Дополнительные сведения см. в разделе [Политика CSP — ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

1. Определите новый идентификатор ProgID в канале Microsoft Edge, который будет открываться в режиме Internet Explorer. Идентификатор ProgID содержит имя и значок приложения, а также полный путь к msedge.exe.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,4"
"AppUserModelId"=""
```

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\DefaultIcon]
@="C:\\<edge_installation_dir>\\msedge.exe,4"
```

2. Настройте обновления оболочки, чтобы передать командную строку, которая будет открываться в режиме IE.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. Наконец, связать расширение файла \.mht с новым ProgID. Добавьте идентификатор ProgID в качестве имени значения с типом значения REG_SZ.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

После настройки ключей, описанных в предыдущем примере, пользователи увидят другой вариант в open **с** меню, чтобы открыть файл \.mht с помощью Microsoft Edge с режимом \<channel\> IE.

## <a name="registry-example"></a>Пример реестра

Следующий фрагмент кода можно сохранить в формате REG и импортировать в реестр.

```markdown
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,4"
"AppUserModelId"=""

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\DefaultIcon]
@="C:\\<edge_installation_dir>\\msedge.exe,4"

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""

```

## <a name="configuring-file-types-to-open-in-internet-explorer-mode"></a>Настройка типов файлов для открытия в режиме Internet Explorer

Начиная с Microsoft Edge 88, вы можете настроить определенные ссылки типа файлов для открытия в режиме Internet Explorer с помощью контекстного меню показать политику, чтобы открыть ссылки в [режиме Internet Explorer.](./microsoft-edge-policies.md#internetexplorerintegrationreloadiniemodeallowed)

Вы можете определить типы файлов, к которым должен применяться этот параметр, указав расширения файлов в политике [Открывать локальные файлы из списка разрешенных расширений файлов в режиме Internet Explorer](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist). 

## <a name="see-also"></a>См. также

- [Сведения о режиме IE](./edge-ie-mode.md)
- [Сведения о настраиваемых сайтах](./edge-learnmore-configurable-sites-ie-mode.md)
- [Дополнительные сведения о режиме предприятия](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Настройка сопоставлений типов файлов](/windows/win32/shell/fa-file-types)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)