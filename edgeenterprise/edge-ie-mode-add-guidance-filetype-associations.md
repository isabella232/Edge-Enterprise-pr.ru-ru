---
title: Сопоставление расширений файлов с режимом Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Сопоставление расширений файлов с режимом Internet Explorer
ms.openlocfilehash: 7efa30a6ec3013cf5b1595471f1fb91dca8bdfda
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641495"
---
# <a name="associate-file-extensions-with-internet-explorer-mode"></a><span data-ttu-id="a3a9b-103">Сопоставление расширений файлов с режимом Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="a3a9b-103">Associate file extensions with Internet Explorer mode</span></span>

>[!Note]
> <span data-ttu-id="a3a9b-104">Поддержка классического приложения Internet Explorer 11 будет прекращена 15 июня 2022 г. (список области применения см. в [вопросах и ответах](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span><span class="sxs-lookup"><span data-stu-id="a3a9b-104">The Internet Explorer 11 desktop application will be retired and go out of support on June 15, 2022 (for a list of what’s in scope, [see the FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span></span> <span data-ttu-id="a3a9b-105">Те же приложения и сайты IE11, которые вы используете сегодня, можно открывать в Microsoft Edge в режиме Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a3a9b-105">The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode.</span></span> <span data-ttu-id="a3a9b-106">Дополнительные сведения см. [здесь](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span><span class="sxs-lookup"><span data-stu-id="a3a9b-106">[Learn more here](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span></span>

<span data-ttu-id="a3a9b-107">В этой статье объясняется, как сопоставить Microsoft Edge в режиме Internet Explorer с расширениями файлов для классических приложений.</span><span class="sxs-lookup"><span data-stu-id="a3a9b-107">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="a3a9b-108">Эта статья относится к Microsoft Edge версии 86 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a3a9b-108">This article applies to Microsoft Edge version 86 or later.</span></span>

## <a name="guidance-for-file-extension-association-with-internet-explorer-mode"></a><span data-ttu-id="a3a9b-109">Руководство по сопоставлению расширений файлов с режимом Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="a3a9b-109">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="a3a9b-110">В приведенных ниже инструкциях показано, как сопоставить Microsoft Edge в режиме IE с типом файла MHT.</span><span class="sxs-lookup"><span data-stu-id="a3a9b-110">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="a3a9b-111">Используйте приведенные ниже инструкции, чтобы настроить сопоставление файлов.</span><span class="sxs-lookup"><span data-stu-id="a3a9b-111">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="a3a9b-112">Вы можете задать конкретные расширения файлов, которые будут открываться в режиме Internet Explorer по умолчанию, с помощью политики **Задать файл конфигурации сопоставлений по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="a3a9b-112">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="a3a9b-113">Дополнительные сведения см. в разделе [Политика CSP — ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span><span class="sxs-lookup"><span data-stu-id="a3a9b-113">For more information, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="a3a9b-114">Определите новый идентификатор ProgID в канале Microsoft Edge, который будет открываться в режиме Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a3a9b-114">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="a3a9b-115">Идентификатор ProgID содержит имя и значок приложения, а также полный путь к msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="a3a9b-115">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

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

2. <span data-ttu-id="a3a9b-116">Настройте обновления оболочки, чтобы передать командную строку, которая будет открываться в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="a3a9b-116">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="a3a9b-117">Наконец, сопоставьте расширение файла MHT с новым идентификатором ProgID.</span><span class="sxs-lookup"><span data-stu-id="a3a9b-117">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="a3a9b-118">Добавьте идентификатор ProgID в качестве имени значения с типом значения REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="a3a9b-118">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="a3a9b-119">После назначения ключей, описанных в предыдущем примере, в меню **Открыть с помощью** отобразится дополнительный параметр, позволяющий открывать файлы MHT с помощью Microsoft Edge \<channel\> в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="a3a9b-119">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <a name="registry-example"></a><span data-ttu-id="a3a9b-120">Пример реестра</span><span class="sxs-lookup"><span data-stu-id="a3a9b-120">Registry Example</span></span>

<span data-ttu-id="a3a9b-121">Следующий фрагмент кода можно сохранить в формате REG и импортировать в реестр.</span><span class="sxs-lookup"><span data-stu-id="a3a9b-121">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

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

## <a name="configuring-file-types-to-open-in-internet-explorer-mode"></a><span data-ttu-id="a3a9b-122">Настройка типов файлов для открытия в режиме Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="a3a9b-122">Configuring file types to open in Internet Explorer mode</span></span>

<span data-ttu-id="a3a9b-123">С Microsoft Edge 88 вы можете настроить для ссылок на определенные типы файлов открытие в режиме Internet Explorer с помощью политики [Показывать контекстное меню для открытия ссылок в режиме Internet Explorer](./microsoft-edge-policies.md#internetexplorerintegrationreloadiniemodeallowed).</span><span class="sxs-lookup"><span data-stu-id="a3a9b-123">Starting Edge 88, you can configure specific file type links to open in Internet Explorer mode using the policy [Show context menu to open links in Internet Explorer mode](./microsoft-edge-policies.md#internetexplorerintegrationreloadiniemodeallowed).</span></span>

<span data-ttu-id="a3a9b-124">Вы можете определить типы файлов, к которым должен применяться этот параметр, указав расширения файлов в политике [Открывать локальные файлы из списка разрешенных расширений файлов в режиме Internet Explorer](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist).</span><span class="sxs-lookup"><span data-stu-id="a3a9b-124">You can define file types this option should apply to, by specifying file extensions in this policy [Open local files in Internet Explorer mode file extension allow list](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist).</span></span> 

## <a name="see-also"></a><span data-ttu-id="a3a9b-125">См. также</span><span class="sxs-lookup"><span data-stu-id="a3a9b-125">See also</span></span>

- [<span data-ttu-id="a3a9b-126">Сведения о режиме IE</span><span class="sxs-lookup"><span data-stu-id="a3a9b-126">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="a3a9b-127">Сведения о настраиваемых сайтах</span><span class="sxs-lookup"><span data-stu-id="a3a9b-127">Configurable sites information</span></span>](./edge-learnmore-configurable-sites-ie-mode.md)
- [<span data-ttu-id="a3a9b-128">Дополнительные сведения о режиме предприятия</span><span class="sxs-lookup"><span data-stu-id="a3a9b-128">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="a3a9b-129">Настройка сопоставлений типов файлов</span><span class="sxs-lookup"><span data-stu-id="a3a9b-129">Setting file type associations</span></span>](/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="a3a9b-130">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="a3a9b-130">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)