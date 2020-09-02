---
title: Настройка политик для режима IE
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 03/25/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Настройка политик для режима IE
ms.openlocfilehash: 2d2ded3a3fb338bdf2d815d681b52249007945ac
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980860"
---
# <span data-ttu-id="0ff7a-103">Настройка политик для режима IE</span><span class="sxs-lookup"><span data-stu-id="0ff7a-103">Configure IE mode policies</span></span>

<span data-ttu-id="0ff7a-104">В этой статье объясняется, как настроить политики для режима IE.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-104">This article explains how to configure IE mode policies.</span></span>

> [!NOTE]
> <span data-ttu-id="0ff7a-105">Эта статья относится к Microsoft Edge версии 77 или более поздней; каналы **Stable**, **Beta** и **Dev**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-105">This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.</span></span>

<span data-ttu-id="0ff7a-106">При настройке режима IE необходимо выполнить три действия:</span><span class="sxs-lookup"><span data-stu-id="0ff7a-106">Configuring IE mode requires three steps:</span></span>

1. [<span data-ttu-id="0ff7a-107">Настройка интеграции с Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="0ff7a-107">Configure Internet Explorer integration</span></span>](#configure-internet-explorer-integration)
2. [<span data-ttu-id="0ff7a-108">Перенаправление сайтов с Microsoft Edge в режим IE</span><span class="sxs-lookup"><span data-stu-id="0ff7a-108">Redirect sites from Microsoft Edge to IE mode</span></span>](#redirect-sites-from-microsoft-edge-to-ie-mode)
3. <span data-ttu-id="0ff7a-109">(Необязательно) [Перенаправление сайтов с IE в Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)</span><span class="sxs-lookup"><span data-stu-id="0ff7a-109">(Optional) [Redirect sites from IE to Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)</span></span>

> [!NOTE]
> <span data-ttu-id="0ff7a-110">Политики для включения режима IE можно настроить с помощью Intune.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-110">Policies to enable IE mode can be configured through Intune.</span></span> <span data-ttu-id="0ff7a-111">Дополнительные сведения см. в статьях [Добавление Microsoft Edge в Microsoft Intune](https://docs.microsoft.com/intune/apps/apps-windows-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json) и [Настройка политик Microsoft Edge с помощью Microsoft Intune](https://docs.microsoft.com/DeployEdge/configure-edge-with-intune).</span><span class="sxs-lookup"><span data-stu-id="0ff7a-111">For more information, see [Add Microsoft Edge to Microsoft Intune](https://docs.microsoft.com/intune/apps/apps-windows-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json) and [Configure Microsoft Edge policies with Microsoft Intune](https://docs.microsoft.com/DeployEdge/configure-edge-with-intune).</span></span>

## <span data-ttu-id="0ff7a-112">Настройка интеграции с Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="0ff7a-112">Configure Internet Explorer integration</span></span>

<span data-ttu-id="0ff7a-113">Вы можете настроить Internet Explorer для открытия сайтов непосредственно в Microsoft Edge (режим IE).</span><span class="sxs-lookup"><span data-stu-id="0ff7a-113">You can configure Internet Explorer to open directly within Microsoft Edge (IE mode).</span></span> <span data-ttu-id="0ff7a-114">Кроме того, можно настроить Internet Explorer для открытия сайтов в отдельном окне Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-114">You can also configure Internet Explorer to open with a standalone Internet Explorer 11 window.</span></span> <span data-ttu-id="0ff7a-115">Большинство пользователей предпочитает, чтобы сайты открывались непосредственно в Microsoft Edge в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-115">Most users prefer when sites open directly within Microsoft Edge in IE mode.</span></span>

### <span data-ttu-id="0ff7a-116">Включение интеграции с Internet Explorer с помощью групповой политики</span><span class="sxs-lookup"><span data-stu-id="0ff7a-116">Enable Internet Explorer integration using Group Policy</span></span>

1. <span data-ttu-id="0ff7a-117">Скачайте и используйте последний [шаблон политик Microsoft Edge](https://www.microsoft.com/en-us/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="0ff7a-117">Download and use the latest [Microsoft Edge Policy Template](https://www.microsoft.com/en-us/edge/business/download).</span></span>
2. <span data-ttu-id="0ff7a-118">Откройте редактор групповых политик.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-118">Open Group Policy Editor.</span></span>
3. <span data-ttu-id="0ff7a-119">Щелкните **Конфигурация компьютера** > **Административные шаблоны** > **Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-119">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
4. <span data-ttu-id="0ff7a-120">Дважды щелкните пункт **Настройка интеграции с Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-120">Double-click **Configure Internet Explorer integration**.</span></span>
5. <span data-ttu-id="0ff7a-121">Выберите **Включено**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-121">Select **Enabled**.</span></span>
6. <span data-ttu-id="0ff7a-122">В разделе **Параметры** выберите из раскрывающегося списка значение</span><span class="sxs-lookup"><span data-stu-id="0ff7a-122">Under **Options**, set the dropdown value to</span></span> 
   -  <span data-ttu-id="0ff7a-123">**Режим Internet Explorer**, если вы хотите, чтобы сайты открывались в браузере Microsoft Edge в режиме IE</span><span class="sxs-lookup"><span data-stu-id="0ff7a-123">**Internet Explorer mode** if you want sites to open in IE mode on Microsoft Edge</span></span>
   -  <span data-ttu-id="0ff7a-124">**Internet Explorer 11**, если вы хотите, чтобы сайты открывались в отдельном окне Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="0ff7a-124">**Internet Explorer 11** if you want sites to open in a standalone Internet Explorer 11 window</span></span>
   -  <span data-ttu-id="0ff7a-125">**Нет**, если вы хотите запретить пользователям настройку режима Internet Explorer с помощью edge://flags или параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-125">**None** if you want to stop users from configuring Internet Explorer mode via edge://flags or through the command line</span></span>

   > [!NOTE]
   > <span data-ttu-id="0ff7a-126">Установка для политики значения **Отключено** предполагает, что режим IE отключен политикой, но его можно настроить с помощью edge://flags или параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-126">Setting the policy to **Disabled** implies IE mode is disabled by policy, but can be set through edge://flags or command line options.</span></span>
7. <span data-ttu-id="0ff7a-127">Нажмите **ОК** или **Применить**, чтобы сохранить этот параметр политики.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-127">Click **OK** or **Apply** to save this policy setting.</span></span>

## <span data-ttu-id="0ff7a-128">Перенаправление сайтов с Microsoft Edge в режим IE</span><span class="sxs-lookup"><span data-stu-id="0ff7a-128">Redirect sites from Microsoft Edge to IE mode</span></span>

<span data-ttu-id="0ff7a-129">Существует два варианта определения сайтов, которые должны открываться в режиме IE:</span><span class="sxs-lookup"><span data-stu-id="0ff7a-129">There are two options for identifying which sites should open in IE mode:</span></span>

- <span data-ttu-id="0ff7a-130">(Рекомендуется) [Настройка сайтов в списке сайтов предприятия](#configure-sites-on-the-enterprise-site-list)</span><span class="sxs-lookup"><span data-stu-id="0ff7a-130">(Recommended) [Configure sites on the Enterprise Site list](#configure-sites-on-the-enterprise-site-list)</span></span>
- [<span data-ttu-id="0ff7a-131">Настройка всех сайтов интрасети</span><span class="sxs-lookup"><span data-stu-id="0ff7a-131">Configure all Intranet sites</span></span>](#configure-all-intranet-sites)

### <span data-ttu-id="0ff7a-132">Настройка сайтов в списке сайтов предприятия</span><span class="sxs-lookup"><span data-stu-id="0ff7a-132">Configure sites on the Enterprise Site list</span></span>

<span data-ttu-id="0ff7a-133">Вы можете использовать следующие групповые политики для настройки отдельных сайтов, которые нужно открыть в режиме IE:</span><span class="sxs-lookup"><span data-stu-id="0ff7a-133">You can use the following group policies to configure specific sites to open in IE mode:</span></span>

- <span data-ttu-id="0ff7a-134">[Использовать список веб-сайтов IE в режиме предприятия](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)</span><span class="sxs-lookup"><span data-stu-id="0ff7a-134">[Use the Enterprise Mode IE website list](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)</span></span>
- <span data-ttu-id="0ff7a-135">[Настройка списка сайтов в режиме предприятия](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge версии 78 или более поздней)</span><span class="sxs-lookup"><span data-stu-id="0ff7a-135">[Configure the Enterprise Mode Site List](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge, version 78 or later)</span></span><br/><span data-ttu-id="0ff7a-136">Эта политика позволяет создать отдельный список сайтов в режиме предприятия для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-136">This policy lets you create a separate Enterprise Mode Site list for Microsoft Edge.</span></span> <span data-ttu-id="0ff7a-137">Включение этой политики переопределяет параметры в политике "Использовать список веб-сайтов IE в режиме предприятия", если включен параметр "Настройка интеграции с Internet Explorer".</span><span class="sxs-lookup"><span data-stu-id="0ff7a-137">Enabling this policy overrides the settings in the "Use the Enterprise Mode IE website list" policy, if "Configure Internet Explorer integration" is enabled.</span></span> <span data-ttu-id="0ff7a-138">Отключение или отмена настройки политики не влияет на поведение по умолчанию политики "Настройка интеграции с Internet Explorer".</span><span class="sxs-lookup"><span data-stu-id="0ff7a-138">Disabling or not configuring this policy doesn't affect the default behavior of the "Configure Internet Explorer integration" policy.</span></span>
    > [!NOTE]
    > <span data-ttu-id="0ff7a-139">Настраивать политику Microsoft Edge не обязательно.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-139">It is not mandatory to configure the Microsoft Edge policy.</span></span> <span data-ttu-id="0ff7a-140">Во многих организациях используется переопределение. Это позволяет сделать текущий список сайтов доступным для всех пользователей с помощью политики IE, а также упрощает пилотное использование обновленной версии с помощью политики Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-140">Many organizations use this as an override, allowing them to target the current Site List at all users with the IE policy, and more easily target an updated version to pilot uses with the Microsoft Edge policy.</span></span>

<span data-ttu-id="0ff7a-141">Дополнительные сведения о списках сайтов в режиме предприятия можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="0ff7a-141">For more information about Enterprise Mode Site lists, see:</span></span>

- [<span data-ttu-id="0ff7a-142">Использование средства Enterprise Mode Site List Manager</span><span class="sxs-lookup"><span data-stu-id="0ff7a-142">Use the Enterprise Mode Site List Manager</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/use-the-enterprise-mode-site-list-manager)
- <span data-ttu-id="0ff7a-143">[Добавление нескольких сайтов в список сайтов в режиме предприятия в средстве Enterprise Mode Site List Manager с помощью файла (схема версии2)](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool).</span><span class="sxs-lookup"><span data-stu-id="0ff7a-143">[Add multiple sites to the Enterprise Mode site list using a file and the Enterprise Mode Site List Manager (schema v.2)](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool).</span></span>

### <span data-ttu-id="0ff7a-144">Настройка с помощью политики "Использовать список веб-сайтов IE в режиме предприятия"</span><span class="sxs-lookup"><span data-stu-id="0ff7a-144">Configure using the Use the Enterprise Mode IE website list policy</span></span>

<span data-ttu-id="0ff7a-145">В режиме Internet Explorer можно использовать существующую политику для настройки списка сайтов предприятия для Internet Explorer, что позволяет создавать и вести один список.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-145">IE mode can use the existing policy configuring the Enterprise Site List for Internet Explorer, allowing you to create and maintain a single list.</span></span>

1. <span data-ttu-id="0ff7a-146">Создание или повторное использование XML-файла списка сайтов</span><span class="sxs-lookup"><span data-stu-id="0ff7a-146">Create or reuse a Site List XML</span></span>
    1. <span data-ttu-id="0ff7a-147">Все сайты, в которых есть элемент _\<open-in\>IE11\</open-in\>_, теперь будут открываться в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-147">All sites that have the element _\<open-in\>IE11\</open-in\>_ will now open in IE mode.</span></span>
2. <span data-ttu-id="0ff7a-148">Откройте редактор групповых политик.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-148">Open Group Policy Editor.</span></span>
3. <span data-ttu-id="0ff7a-149">Выберите **Конфигурация компьютера** > **Административные шаблоны** > **Компоненты Windows** > **Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-149">Click **Computer Configuration** > **Administrative Templates** > **Windows Components** > **Internet Explorer**.</span></span>
4. <span data-ttu-id="0ff7a-150">Дважды щелкните пункт **Использовать список веб-сайтов IE в режиме предприятия**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-150">Double-click **Use the Enterprise Mode IE website list**.</span></span>
5. <span data-ttu-id="0ff7a-151">Выберите **Включено**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-151">Select **Enabled**.</span></span>
6. <span data-ttu-id="0ff7a-152">В разделе **Параметры** введите расположение списка веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-152">Under **Options**, type the location of website list.</span></span> <span data-ttu-id="0ff7a-153">Можно использовать одно из указанных ниже местоположений.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-153">You can use one of the following locations:</span></span>
    - <span data-ttu-id="0ff7a-154">(Рекомендуется) Расположение HTTPS: **https**:**//iemode/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="0ff7a-154">(Recommended) HTTPS location: **https**:**//iemode/sites.xml**</span></span>
    - <span data-ttu-id="0ff7a-155">Файл в локальной сети: **\\\network\shares\sites.xml**</span><span class="sxs-lookup"><span data-stu-id="0ff7a-155">Local network file: **\\\network\shares\sites.xml**</span></span>
    - <span data-ttu-id="0ff7a-156">Локальный файл: **file:///c:/Users/\<user\>/Documents/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="0ff7a-156">Local file: **file:///c:/Users/\<user\>/Documents/sites.xml**</span></span>
7. <span data-ttu-id="0ff7a-157">Нажмите **ОК** или **Применить**, чтобы сохранить эти параметры.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-157">Click **OK** or **Apply** to save these settings.</span></span>

### <span data-ttu-id="0ff7a-158">Настройка с помощью политики "Настроить список сайтов для режима предприятия"</span><span class="sxs-lookup"><span data-stu-id="0ff7a-158">Configure using the Configure the Enterprise Mode Site List policy</span></span>

<span data-ttu-id="0ff7a-159">Кроме того, в режиме IE можно задать отдельную политику для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-159">You can also configure IE mode with a separate policy for Microsoft Edge.</span></span> <span data-ttu-id="0ff7a-160">Эта дополнительная политика позволяет переопределять список сайтов IE.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-160">This additional policy allows you to override the IE site list.</span></span> <span data-ttu-id="0ff7a-161">Например, в некоторых организациях список рабочих сайтов будет доступен для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-161">For example, some organizations will target the production site list to all users.</span></span> <span data-ttu-id="0ff7a-162">Тогда вы сможете развернуть пилотный список сайтов для небольшой группы пользователей, используя эту политику.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-162">You can then deploy the pilot site list to a small group of users using this policy.</span></span>

1. <span data-ttu-id="0ff7a-163">Создание или повторное использование XML-файла списка сайтов</span><span class="sxs-lookup"><span data-stu-id="0ff7a-163">Create or reuse a Site List XML</span></span>
    1. <span data-ttu-id="0ff7a-164">Все сайты, в которых есть элемент _\<open-in\>IE11\</open-in\>_, теперь будут открываться в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-164">All sites that have the element _\<open-in\>IE11\</open-in\>_ will now open in IE mode.</span></span>
2. <span data-ttu-id="0ff7a-165">Откройте редактор групповых политик.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-165">Open Group Policy Editor.</span></span>
3. <span data-ttu-id="0ff7a-166">Щелкните **Конфигурация компьютера** > **Административные шаблоны** > **Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-166">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
4. <span data-ttu-id="0ff7a-167">Дважды щелкните **Настроить список сайтов для режима предприятия**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-167">Double-click **Configure the Enterprise Mode Site List**.</span></span>
5. <span data-ttu-id="0ff7a-168">Выберите **Включено**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-168">Select **Enabled**.</span></span>
6. <span data-ttu-id="0ff7a-169">В разделе **Параметры** введите расположение списка веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-169">Under **Options**, type the location of website list.</span></span> <span data-ttu-id="0ff7a-170">Можно использовать одно из указанных ниже местоположений.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-170">You can use one of the following locations:</span></span>
    - <span data-ttu-id="0ff7a-171">(Рекомендуется) Расположение HTTPS: **https**:**//iemode/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="0ff7a-171">(Recommended) HTTPS location: **https**:**//iemode/sites.xml**</span></span> <!--Trying to keep this from being an active link in MD -->
    - <span data-ttu-id="0ff7a-172">Файл в локальной сети: **\\\network\shares\sites.xml**</span><span class="sxs-lookup"><span data-stu-id="0ff7a-172">Local network file: **\\\network\shares\sites.xml**</span></span>
    - <span data-ttu-id="0ff7a-173">Локальный файл: **file:///c:/Users/\<user\>/Documents/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="0ff7a-173">Local file: **file:///c:/Users/\<user\>/Documents/sites.xml**</span></span>
7. <span data-ttu-id="0ff7a-174">Нажмите **ОК** или **Применить**, чтобы сохранить эти параметры.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-174">Click **OK** or **Apply** to save these settings.</span></span>

### <span data-ttu-id="0ff7a-175">Настройка всех сайтов интрасети</span><span class="sxs-lookup"><span data-stu-id="0ff7a-175">Configure all intranet sites</span></span>

<span data-ttu-id="0ff7a-176">Режим IE можно настроить для всех сайтов в зоне местной интрасети.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-176">IE mode can be configured as for all sites in the Local Intranet zone.</span></span> <span data-ttu-id="0ff7a-177">Вы можете исключить отдельные сайты из режима IE с помощью списка сайтов в режиме предприятия.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-177">You can remove individual sites from IE mode using an Enterprise Mode Site List.</span></span>

>[!NOTE]
>
> <span data-ttu-id="0ff7a-178">Зона местной интрасети содержит явно добавленные сайты, а также сайты, назначенные для этой зоны с помощью эвристики.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-178">The Local Intranet zone contains explicitly added sites, but also assigns sites to this zone using heuristics.</span></span> <span data-ttu-id="0ff7a-179">Сюда могут входить имена узлов без точки (например, **https**:**//payroll**) и сайты, подключаемые в обход прокси-сервера по сценарию настройки прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-179">This can include dotless host names (e.g. **https**:**//payroll**) and sites that the proxy configuration script configures to bypass the proxy.</span></span> <span data-ttu-id="0ff7a-180">Если управление DNS или прокси-сервером осуществляется внешней стороной, она потенциально может добавить веб-сайты в режим IE.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-180">If an external party controls DNS or proxy, they could potentially force websites into IE mode.</span></span>

1. <span data-ttu-id="0ff7a-181">Откройте редактор локальных групповых политик.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-181">Open Local Group Policy Editor.</span></span>
2. <span data-ttu-id="0ff7a-182">Щелкните **Конфигурация компьютера** > **Административные шаблоны** > **Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-182">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
3. <span data-ttu-id="0ff7a-183">Дважды щелкните **Отправлять все сайты интрасети в Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-183">Double-click **Send all intranet sites to Internet Explorer**.</span></span>
4. <span data-ttu-id="0ff7a-184">Выберите **Включено**, а затем нажмите кнопку **ОК** или **Применить**, чтобы сохранить параметры политики.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-184">Select **Enabled**, and then click **OK** or **Apply** to save the policy settings.</span></span>

## <span data-ttu-id="0ff7a-185">Перенаправление сайтов с IE в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0ff7a-185">Redirect sites from IE to Microsoft Edge</span></span>

<span data-ttu-id="0ff7a-186">Вы можете запретить пользователям использовать Internet Explorer для сайтов, для которых он не нужен.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-186">You can prevent your users from using Internet Explorer for sites that don't need it.</span></span> <span data-ttu-id="0ff7a-187">Internet Explorer может автоматически перенаправлять сайты в Microsoft Edge, если они не находятся в вашем списке сайтов.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-187">Internet Explorer can automatically redirect sites to Microsoft Edge if they aren't on your site list.</span></span>

1. <span data-ttu-id="0ff7a-188">Откройте редактор групповых политик.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-188">Open Group Policy Editor.</span></span>
2. <span data-ttu-id="0ff7a-189">Щелкните **Конфигурация компьютера** > **Средства администрирования** > **Компоненты Windows** > **Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-189">Click **Computer Configuration** > **Administrative Tools** > **Windows Components** > **Internet Explorer**.</span></span>
3. <span data-ttu-id="0ff7a-190">Дважды щелкните **Отправлять все сайты, которые не включены в список сайтов в режиме предприятия, в Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-190">Double-click **Send all sites not included in the Enterprise Mode Site List to Microsoft Edge.**</span></span>
4. <span data-ttu-id="0ff7a-191">Выберите **Включено**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-191">Select **Enabled**</span></span>
5. <span data-ttu-id="0ff7a-192">Нажмите **ОК** или **Применить**, чтобы сохранить эти параметры.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-192">Click **OK** or **Apply** to save these settings.</span></span>
6. <span data-ttu-id="0ff7a-193">Дважды щелкните **Настроить канал Microsoft Edge, который будет использоваться для открытия перенаправленных сайтов**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-193">Double-click **Configure which channel of Microsoft Edge to use for opening redirected sites**.</span></span>
7. <span data-ttu-id="0ff7a-194">Выберите **Включено**.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-194">Select **Enabled**.</span></span>
8. <span data-ttu-id="0ff7a-195">В разделе **Параметры** выберите три основных варианта канала, который будет использоваться. Internet Explorer будет перенаправлять сайты на канал с наивысшим рейтингом, который пользователь установил на устройстве.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-195">Under **Options**, select your top three choices for the channel to use - Internet Explorer will redirect to the highest ranked choice that the user has installed on that device:</span></span>
   - <span data-ttu-id="0ff7a-196">Канал Microsoft Edge Stable</span><span class="sxs-lookup"><span data-stu-id="0ff7a-196">Microsoft Edge Stable</span></span>
   - <span data-ttu-id="0ff7a-197">Канал Microsoft Edge Beta версии 77 или более поздней</span><span class="sxs-lookup"><span data-stu-id="0ff7a-197">Microsoft Edge Beta version 77 or later</span></span>
   - <span data-ttu-id="0ff7a-198">Канал Microsoft Edge Dev версии 77 или более поздней</span><span class="sxs-lookup"><span data-stu-id="0ff7a-198">Microsoft Edge Dev version 77 or later</span></span>
   - <span data-ttu-id="0ff7a-199">Канал Microsoft Edge Canary версии 77 или более поздней</span><span class="sxs-lookup"><span data-stu-id="0ff7a-199">Microsoft Edge Canary version 77 or later</span></span>
   - <span data-ttu-id="0ff7a-200">Microsoft Edge версии 45 или более ранней</span><span class="sxs-lookup"><span data-stu-id="0ff7a-200">Microsoft Edge version 45 or earlier</span></span>
9. <span data-ttu-id="0ff7a-201">Нажмите **ОК** или **Применить**, чтобы сохранить эти параметры.</span><span class="sxs-lookup"><span data-stu-id="0ff7a-201">Click **OK** or **Apply** to save these settings.</span></span>

## <span data-ttu-id="0ff7a-202">См. также</span><span class="sxs-lookup"><span data-stu-id="0ff7a-202">See also</span></span>

- [<span data-ttu-id="0ff7a-203">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="0ff7a-203">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="0ff7a-204">Сведения о режиме IE</span><span class="sxs-lookup"><span data-stu-id="0ff7a-204">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="0ff7a-205">Дополнительные сведения о режиме предприятия</span><span class="sxs-lookup"><span data-stu-id="0ff7a-205">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)