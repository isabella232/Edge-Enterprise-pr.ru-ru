---
title: Добавление режима Internet Explorer в контекстное меню "Открыть с помощью"
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/13/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Добавление режима Internet Explorer в контекстное меню "Открыть с помощью"
ms.openlocfilehash: 6453cd2587e3bec10404d2491914debb999fcf3f
ms.sourcegitcommit: e3c80274a9b8ef15761c968214b3cba593476132
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/13/2020
ms.locfileid: "11168493"
---
# <span data-ttu-id="c94a4-103">Добавление режима Internet Explorer в контекстное меню "Открыть с помощью"</span><span class="sxs-lookup"><span data-stu-id="c94a4-103">Add Internet Explorer mode to the "Open with" context menu</span></span>

<span data-ttu-id="c94a4-104">В этой статье объясняется, как сопоставить Microsoft Edge в режиме Internet Explorer с расширениями файлов для классических приложений.</span><span class="sxs-lookup"><span data-stu-id="c94a4-104">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="c94a4-105">Эта статья относится к Microsoft Edge версии 86 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="c94a4-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <span data-ttu-id="c94a4-106">Руководство по сопоставлению расширений файлов с режимом Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="c94a4-106">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="c94a4-107">В приведенных ниже инструкциях показано, как сопоставить Microsoft Edge в режиме IE с типом файла MHT.</span><span class="sxs-lookup"><span data-stu-id="c94a4-107">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="c94a4-108">Используйте приведенные ниже инструкции, чтобы настроить сопоставление файлов.</span><span class="sxs-lookup"><span data-stu-id="c94a4-108">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="c94a4-109">Вы можете задать конкретные расширения файлов, которые будут открываться в режиме Internet Explorer по умолчанию, с помощью политики **Задать файл конфигурации сопоставлений по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="c94a4-109">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="c94a4-110">Дополнительные сведения см. в разделе [Политика CSP — ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span><span class="sxs-lookup"><span data-stu-id="c94a4-110">For more information, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="c94a4-111">Определите новый идентификатор ProgID в канале Microsoft Edge, который будет открываться в режиме Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c94a4-111">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="c94a4-112">Идентификатор ProgID содержит имя и значок приложения, а также полный путь к msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="c94a4-112">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

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

2. <span data-ttu-id="c94a4-113">Настройте обновления оболочки, чтобы передать командную строку, которая будет открываться в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="c94a4-113">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="c94a4-114">Наконец, сопоставьте расширение файла MHT с новым идентификатором ProgID.</span><span class="sxs-lookup"><span data-stu-id="c94a4-114">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="c94a4-115">Добавьте идентификатор ProgID в качестве имени значения с типом значения REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="c94a4-115">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="c94a4-116">После назначения ключей, описанных в предыдущем примере, в меню **Открыть с помощью** отобразится дополнительный параметр, позволяющий открывать файлы MHT с помощью Microsoft Edge \<channel\> в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="c94a4-116">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <span data-ttu-id="c94a4-117">Пример реестра</span><span class="sxs-lookup"><span data-stu-id="c94a4-117">Registry Example</span></span>

<span data-ttu-id="c94a4-118">Следующий фрагмент кода можно сохранить в формате REG и импортировать в реестр.</span><span class="sxs-lookup"><span data-stu-id="c94a4-118">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

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

## <span data-ttu-id="c94a4-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c94a4-119">See also</span></span>

- [<span data-ttu-id="c94a4-120">Сведения о режиме IE</span><span class="sxs-lookup"><span data-stu-id="c94a4-120">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="c94a4-121">Сведения о настраиваемых сайтах</span><span class="sxs-lookup"><span data-stu-id="c94a4-121">Configurable sites information</span></span>](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [<span data-ttu-id="c94a4-122">Дополнительные сведения о режиме предприятия</span><span class="sxs-lookup"><span data-stu-id="c94a4-122">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="c94a4-123">Настройка сопоставлений типов файлов</span><span class="sxs-lookup"><span data-stu-id="c94a4-123">Setting file type associations</span></span>](https://docs.microsoft.com/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="c94a4-124">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="c94a4-124">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
