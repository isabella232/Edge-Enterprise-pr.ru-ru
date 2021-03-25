---
title: Сопоставление расширений файлов с режимом Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 12/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Сопоставление расширений файлов с режимом Internet Explorer
ms.openlocfilehash: 6c651499401757d9a58e697d1d019a7294bb5fa7
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447373"
---
# <a name="associate-file-extensions-with-internet-explorer-mode"></a>Сопоставление расширений файлов с режимом Internet Explorer

В этой статье объясняется, как сопоставить Microsoft Edge в режиме Internet Explorer с расширениями файлов для классических приложений.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 86 или более поздней версии.

## <a name="guidance-for-file-extension-association-with-internet-explorer-mode"></a>Руководство по сопоставлению расширений файлов с режимом Internet Explorer

В приведенных ниже инструкциях показано, как сопоставить Microsoft Edge в режиме IE с типом файла MHT. Используйте приведенные ниже инструкции, чтобы настроить сопоставление файлов.

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

3. Наконец, сопоставьте расширение файла MHT с новым идентификатором ProgID. Добавьте идентификатор ProgID в качестве имени значения с типом значения REG_SZ.

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

После назначения ключей, описанных в предыдущем примере, в меню **Открыть с помощью** отобразится дополнительный параметр, позволяющий открывать файлы MHT с помощью Microsoft Edge \<channel\> в режиме IE.

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

С Microsoft Edge 88 вы можете настроить для ссылок на определенные типы файлов открытие в режиме Internet Explorer с помощью политики [Показывать контекстное меню для открытия ссылок в режиме Internet Explorer](./microsoft-edge-policies.md#show-context-menu-to-open-a-link-in-internet-explorer-mode). 

Вы можете определить типы файлов, к которым должен применяться этот параметр, указав расширения файлов в политике [Открывать локальные файлы из списка разрешенных расширений файлов в режиме Internet Explorer](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist). 

## <a name="see-also"></a>См. также

- [Сведения о режиме IE](./edge-ie-mode.md)
- [Сведения о настраиваемых сайтах](./edge-learnmore-configurable-sites-ie-mode.md)
- [Дополнительные сведения о режиме предприятия](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Настройка сопоставлений типов файлов](/windows/win32/shell/fa-file-types)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)