---
title: Сопоставление расширений файлов с режимом Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Сопоставление расширений файлов с режимом Internet Explorer
ms.openlocfilehash: c80732239b911f7cd3d615e9ce1e480db2749f17
ms.sourcegitcommit: fc0ac6bb6655d1f6e2de7c838f275779cd7a5de6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "11175182"
---
# Сопоставление расширений файлов с режимом Internet Explorer

В этой статье объясняется, как сопоставить Microsoft Edge в режиме Internet Explorer с расширениями файлов для классических приложений.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 86 или более поздней версии.

## Руководство по сопоставлению расширений файлов с режимом Internet Explorer

В приведенных ниже инструкциях показано, как сопоставить Microsoft Edge в режиме IE с типом файла MHT. Используйте приведенные ниже инструкции, чтобы настроить сопоставление файлов.

> [!NOTE]
> Вы можете задать конкретные расширения файлов, которые будут открываться в режиме Internet Explorer по умолчанию, с помощью политики **Задать файл конфигурации сопоставлений по умолчанию**. Дополнительные сведения см. в разделе [Политика CSP — ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

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

3. Наконец, сопоставьте расширение файла MHT с новым идентификатором ProgID. Добавьте идентификатор ProgID в качестве имени значения с типом значения REG_SZ.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

После назначения ключей, описанных в предыдущем примере, в меню **Открыть с помощью** отобразится дополнительный параметр, позволяющий открывать файлы MHT с помощью Microsoft Edge \<channel\> в режиме IE.

## Пример реестра

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

## См. также

- [Сведения о режиме IE](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Сведения о настраиваемых сайтах](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [Дополнительные сведения о режиме предприятия](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Настройка сопоставлений типов файлов](https://docs.microsoft.com/windows/win32/shell/fa-file-types)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
