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
# <span data-ttu-id="a8c0c-103">Сопоставление расширений файлов с режимом Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="a8c0c-103">Associate file extensions with Internet Explorer mode</span></span>

<span data-ttu-id="a8c0c-104">В этой статье объясняется, как сопоставить Microsoft Edge в режиме Internet Explorer с расширениями файлов для классических приложений.</span><span class="sxs-lookup"><span data-stu-id="a8c0c-104">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="a8c0c-105">Эта статья относится к Microsoft Edge версии 86 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a8c0c-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <span data-ttu-id="a8c0c-106">Руководство по сопоставлению расширений файлов с режимом Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="a8c0c-106">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="a8c0c-107">В приведенных ниже инструкциях показано, как сопоставить Microsoft Edge в режиме IE с типом файла MHT.</span><span class="sxs-lookup"><span data-stu-id="a8c0c-107">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="a8c0c-108">Используйте приведенные ниже инструкции, чтобы настроить сопоставление файлов.</span><span class="sxs-lookup"><span data-stu-id="a8c0c-108">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="a8c0c-109">Вы можете задать конкретные расширения файлов, которые будут открываться в режиме Internet Explorer по умолчанию, с помощью политики **Задать файл конфигурации сопоставлений по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="a8c0c-109">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="a8c0c-110">Дополнительные сведения см. в разделе [Политика CSP — ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span><span class="sxs-lookup"><span data-stu-id="a8c0c-110">For more information, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="a8c0c-111">Определите новый идентификатор ProgID в канале Microsoft Edge, который будет открываться в режиме Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a8c0c-111">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="a8c0c-112">Идентификатор ProgID содержит имя и значок приложения, а также полный путь к msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="a8c0c-112">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

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

2. <span data-ttu-id="a8c0c-113">Настройте обновления оболочки, чтобы передать командную строку, которая будет открываться в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="a8c0c-113">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="a8c0c-114">Наконец, сопоставьте расширение файла MHT с новым идентификатором ProgID.</span><span class="sxs-lookup"><span data-stu-id="a8c0c-114">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="a8c0c-115">Добавьте идентификатор ProgID в качестве имени значения с типом значения REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="a8c0c-115">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="a8c0c-116">После назначения ключей, описанных в предыдущем примере, в меню **Открыть с помощью** отобразится дополнительный параметр, позволяющий открывать файлы MHT с помощью Microsoft Edge \<channel\> в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="a8c0c-116">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <span data-ttu-id="a8c0c-117">Пример реестра</span><span class="sxs-lookup"><span data-stu-id="a8c0c-117">Registry Example</span></span>

<span data-ttu-id="a8c0c-118">Следующий фрагмент кода можно сохранить в формате REG и импортировать в реестр.</span><span class="sxs-lookup"><span data-stu-id="a8c0c-118">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

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

## <span data-ttu-id="a8c0c-119">См. также</span><span class="sxs-lookup"><span data-stu-id="a8c0c-119">See also</span></span>

- [<span data-ttu-id="a8c0c-120">Сведения о режиме IE</span><span class="sxs-lookup"><span data-stu-id="a8c0c-120">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="a8c0c-121">Сведения о настраиваемых сайтах</span><span class="sxs-lookup"><span data-stu-id="a8c0c-121">Configurable sites information</span></span>](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [<span data-ttu-id="a8c0c-122">Дополнительные сведения о режиме предприятия</span><span class="sxs-lookup"><span data-stu-id="a8c0c-122">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="a8c0c-123">Настройка сопоставлений типов файлов</span><span class="sxs-lookup"><span data-stu-id="a8c0c-123">Setting file type associations</span></span>](https://docs.microsoft.com/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="a8c0c-124">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="a8c0c-124">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
