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
# <a name="associate-file-extensions-with-internet-explorer-mode"></a><span data-ttu-id="4624e-103">Сопоставление расширений файлов с режимом Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="4624e-103">Associate file extensions with Internet Explorer mode</span></span>

<span data-ttu-id="4624e-104">В этой статье объясняется, как сопоставить Microsoft Edge в режиме Internet Explorer с расширениями файлов для классических приложений.</span><span class="sxs-lookup"><span data-stu-id="4624e-104">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="4624e-105">Эта статья относится к Microsoft Edge версии 86 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="4624e-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <a name="guidance-for-file-extension-association-with-internet-explorer-mode"></a><span data-ttu-id="4624e-106">Руководство по сопоставлению расширений файлов с режимом Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="4624e-106">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="4624e-107">В приведенных ниже инструкциях показано, как сопоставить Microsoft Edge в режиме IE с типом файла MHT.</span><span class="sxs-lookup"><span data-stu-id="4624e-107">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="4624e-108">Используйте приведенные ниже инструкции, чтобы настроить сопоставление файлов.</span><span class="sxs-lookup"><span data-stu-id="4624e-108">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="4624e-109">Вы можете задать конкретные расширения файлов, которые будут открываться в режиме Internet Explorer по умолчанию, с помощью политики **Задать файл конфигурации сопоставлений по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="4624e-109">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="4624e-110">Дополнительные сведения см. в разделе [Политика CSP — ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span><span class="sxs-lookup"><span data-stu-id="4624e-110">For more information, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="4624e-111">Определите новый идентификатор ProgID в канале Microsoft Edge, который будет открываться в режиме Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4624e-111">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="4624e-112">Идентификатор ProgID содержит имя и значок приложения, а также полный путь к msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="4624e-112">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

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

2. <span data-ttu-id="4624e-113">Настройте обновления оболочки, чтобы передать командную строку, которая будет открываться в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="4624e-113">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="4624e-114">Наконец, сопоставьте расширение файла MHT с новым идентификатором ProgID.</span><span class="sxs-lookup"><span data-stu-id="4624e-114">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="4624e-115">Добавьте идентификатор ProgID в качестве имени значения с типом значения REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="4624e-115">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="4624e-116">После назначения ключей, описанных в предыдущем примере, в меню **Открыть с помощью** отобразится дополнительный параметр, позволяющий открывать файлы MHT с помощью Microsoft Edge \<channel\> в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="4624e-116">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <a name="registry-example"></a><span data-ttu-id="4624e-117">Пример реестра</span><span class="sxs-lookup"><span data-stu-id="4624e-117">Registry Example</span></span>

<span data-ttu-id="4624e-118">Следующий фрагмент кода можно сохранить в формате REG и импортировать в реестр.</span><span class="sxs-lookup"><span data-stu-id="4624e-118">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

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
## <a name="configuring-file-types-to-open-in-internet-explorer-mode"></a><span data-ttu-id="4624e-119">Настройка типов файлов для открытия в режиме Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="4624e-119">Configuring file types to open in Internet Explorer mode</span></span>

<span data-ttu-id="4624e-120">С Microsoft Edge 88 вы можете настроить для ссылок на определенные типы файлов открытие в режиме Internet Explorer с помощью политики [Показывать контекстное меню для открытия ссылок в режиме Internet Explorer](./microsoft-edge-policies.md#show-context-menu-to-open-a-link-in-internet-explorer-mode).</span><span class="sxs-lookup"><span data-stu-id="4624e-120">Starting Edge 88, you can configure specific file type links to open in Internet Explorer mode using the policy [Show context menu to open links in Internet Explorer mode](./microsoft-edge-policies.md#show-context-menu-to-open-a-link-in-internet-explorer-mode).</span></span> 

<span data-ttu-id="4624e-121">Вы можете определить типы файлов, к которым должен применяться этот параметр, указав расширения файлов в политике [Открывать локальные файлы из списка разрешенных расширений файлов в режиме Internet Explorer](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist).</span><span class="sxs-lookup"><span data-stu-id="4624e-121">You can define file types this option should apply to, by specifying file extensions in this policy [Open local files in Internet Explorer mode file extension allow list](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist).</span></span> 

## <a name="see-also"></a><span data-ttu-id="4624e-122">См. также</span><span class="sxs-lookup"><span data-stu-id="4624e-122">See also</span></span>

- [<span data-ttu-id="4624e-123">Сведения о режиме IE</span><span class="sxs-lookup"><span data-stu-id="4624e-123">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="4624e-124">Сведения о настраиваемых сайтах</span><span class="sxs-lookup"><span data-stu-id="4624e-124">Configurable sites information</span></span>](./edge-learnmore-configurable-sites-ie-mode.md)
- [<span data-ttu-id="4624e-125">Дополнительные сведения о режиме предприятия</span><span class="sxs-lookup"><span data-stu-id="4624e-125">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="4624e-126">Настройка сопоставлений типов файлов</span><span class="sxs-lookup"><span data-stu-id="4624e-126">Setting file type associations</span></span>](/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="4624e-127">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="4624e-127">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)