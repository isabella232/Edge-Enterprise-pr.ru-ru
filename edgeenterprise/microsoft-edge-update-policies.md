---
title: Документация по политикам Центра обновления Microsoft Edge
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 11/12/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Документация по всем политикам, поддерживаемым средством обновления Microsoft Edge
ms.openlocfilehash: 921a95c0a5e80ba08fa745748ffa8b0da714ea7d
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617889"
---
# <a name="microsoft-edge---update-policies"></a><span data-ttu-id="ff3db-103">Microsoft Edge — политики обновления</span><span class="sxs-lookup"><span data-stu-id="ff3db-103">Microsoft Edge - Update policies</span></span>

<span data-ttu-id="ff3db-104">Последняя версия Microsoft Edge включает в себя следующие политики, которые можно использовать для управления процессом и временем обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff3db-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

<span data-ttu-id="ff3db-105">Сведения о других политиках, доступных в Microsoft Edge, см. в [Справочнике по политикам браузера Microsoft Edge](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="ff3db-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="ff3db-106">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ff3db-106">This article applies to Microsoft Edge version 77 or later.</span></span>
## <a name="available-policies"></a><span data-ttu-id="ff3db-107">Доступные политики</span><span class="sxs-lookup"><span data-stu-id="ff3db-107">Available policies</span></span>
<span data-ttu-id="ff3db-108">В этих таблицах указаны все групповые политики, связанные с обновлением, доступные в данном выпуске Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff3db-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="ff3db-109">Для получения дополнительных сведений о конкретных политиках см. ссылки в таблице.</span><span class="sxs-lookup"><span data-stu-id="ff3db-109">Use the links in the table to get more details about specific policies.</span></span>

<span data-ttu-id="ff3db-110">|&nbsp;|&nbsp;| |**-**|-| |**[Приложения](#applications)**|[Параметры](#preferences)| |**[Прокси-сервер](#proxy-server)**|[Microsoft Edge WebView](#microsoft-edge-webview)|</span><span class="sxs-lookup"><span data-stu-id="ff3db-110">|&nbsp;|&nbsp;| |**-**|-| |**[Applications](#applications)**|[Preferences](#preferences)| |**[Proxy Server](#proxy-server)**|[Microsoft Edge WebView](#microsoft-edge-webview)|</span></span>
### [<a name="applications"></a><span data-ttu-id="ff3db-111">Приложения</span><span class="sxs-lookup"><span data-stu-id="ff3db-111">Applications</span></span>](#applications-policies)
|<span data-ttu-id="ff3db-112">Имя политики</span><span class="sxs-lookup"><span data-stu-id="ff3db-112">Policy Name</span></span>|<span data-ttu-id="ff3db-113">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ff3db-113">Caption</span></span>|
|-|-|
|[<span data-ttu-id="ff3db-114">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="ff3db-114">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="ff3db-115">Разрешить установку по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ff3db-115">Allow installation default</span></span>|
|[<span data-ttu-id="ff3db-116">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="ff3db-116">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="ff3db-117">Переопределение политики обновления по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ff3db-117">Update policy override default</span></span>|
|[<span data-ttu-id="ff3db-118">Install</span><span class="sxs-lookup"><span data-stu-id="ff3db-118">Install</span></span>](#install)|<span data-ttu-id="ff3db-119">Разрешить установку (для канала)</span><span class="sxs-lookup"><span data-stu-id="ff3db-119">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="ff3db-120">Update</span><span class="sxs-lookup"><span data-stu-id="ff3db-120">Update</span></span>](#update)|<span data-ttu-id="ff3db-121">Переопределение политики обновления (для канала)</span><span class="sxs-lookup"><span data-stu-id="ff3db-121">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="ff3db-122">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="ff3db-122">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="ff3db-123">Разрешить параллельный запуск разных типов браузеров Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff3db-123">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="ff3db-124">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="ff3db-124">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="ff3db-125">Запрет создания ярлыка на рабочем столе при установке по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ff3db-125">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="ff3db-126">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="ff3db-126">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="ff3db-127">Запрет создания ярлыка на рабочем столе при установке (для каналов)</span><span class="sxs-lookup"><span data-stu-id="ff3db-127">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="ff3db-128">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="ff3db-128">RollbackToTargetVersion</span></span>](#rollbacktotargetversion)|<span data-ttu-id="ff3db-129">Откат к целевой версии (для каналов)</span><span class="sxs-lookup"><span data-stu-id="ff3db-129">Rollback to Target version (per channel)</span></span>|
|[<span data-ttu-id="ff3db-130">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="ff3db-130">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="ff3db-131">Переопределение целевой версии (для каналов)</span><span class="sxs-lookup"><span data-stu-id="ff3db-131">Target version override (per channel)</span></span>|

### [<a name="preferences"></a><span data-ttu-id="ff3db-132">Предпочтения</span><span class="sxs-lookup"><span data-stu-id="ff3db-132">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="ff3db-133">Имя политики</span><span class="sxs-lookup"><span data-stu-id="ff3db-133">Policy Name</span></span>|<span data-ttu-id="ff3db-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ff3db-134">Caption</span></span>|
|-|-|
|[<span data-ttu-id="ff3db-135">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="ff3db-135">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="ff3db-136">Переопределение периода автоматической проверки обновления</span><span class="sxs-lookup"><span data-stu-id="ff3db-136">Auto-update check period override</span></span>|
|[<span data-ttu-id="ff3db-137">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="ff3db-137">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="ff3db-138">Период времени в течение дня, когда будет блокироваться автоматическая проверка обновлений</span><span class="sxs-lookup"><span data-stu-id="ff3db-138">Time period in each day to suppress auto-update check</span></span>|

### [<a name="proxy-server"></a><span data-ttu-id="ff3db-139">Прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="ff3db-139">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="ff3db-140">Имя политики</span><span class="sxs-lookup"><span data-stu-id="ff3db-140">Policy Name</span></span>|<span data-ttu-id="ff3db-141">Действие</span><span class="sxs-lookup"><span data-stu-id="ff3db-141">Caption</span></span>|
|-|-|
|[<span data-ttu-id="ff3db-142">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="ff3db-142">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="ff3db-143">Выбор способа задания параметров прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="ff3db-143">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="ff3db-144">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="ff3db-144">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="ff3db-145">URL-адрес файла PAC прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="ff3db-145">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="ff3db-146">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="ff3db-146">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="ff3db-147">Адрес или URL-адрес прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="ff3db-147">Address or URL of proxy server</span></span>|

### [<a name="microsoft-edge-webview"></a><span data-ttu-id="ff3db-148">Веб-представление Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff3db-148">Microsoft Edge WebView</span></span>](#microsoft-edge-webview-policies)
|<span data-ttu-id="ff3db-149">Имя политики</span><span class="sxs-lookup"><span data-stu-id="ff3db-149">Policy Name</span></span>|<span data-ttu-id="ff3db-150">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ff3db-150">Caption</span></span>|
|-|-|
|[<span data-ttu-id="ff3db-151">Установка</span><span class="sxs-lookup"><span data-stu-id="ff3db-151">Install</span></span>](#install-webview)|<span data-ttu-id="ff3db-152">Разрешить установку</span><span class="sxs-lookup"><span data-stu-id="ff3db-152">Allow installation</span></span>|
|[<span data-ttu-id="ff3db-153">Обновление</span><span class="sxs-lookup"><span data-stu-id="ff3db-153">Update</span></span>](#update-webview)|<span data-ttu-id="ff3db-154">Переопределение политики обновления</span><span class="sxs-lookup"><span data-stu-id="ff3db-154">Update policy override</span></span>|

## <a name="applications-policies"></a><span data-ttu-id="ff3db-155">Политики приложений</span><span class="sxs-lookup"><span data-stu-id="ff3db-155">Applications policies</span></span>

[<span data-ttu-id="ff3db-156">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-156">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="installdefault"></a><span data-ttu-id="ff3db-157">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="ff3db-157">InstallDefault</span></span>
#### <a name="allow-installation-default"></a><span data-ttu-id="ff3db-158">Разрешить установку по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ff3db-158">Allow installation default</span></span>
><span data-ttu-id="ff3db-159">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-159">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-160">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-160">Description</span></span>
<span data-ttu-id="ff3db-161">Вы можете указать поведение по умолчанию для всех каналов: разрешить или заблокировать Microsoft Edge на присоединенных к домену устройствах.</span><span class="sxs-lookup"><span data-stu-id="ff3db-161">You can specify the default behavior of all channels to allow or block Microsoft Edge on domain-joined devices.</span></span>

<span data-ttu-id="ff3db-162">Вы можете переопределить эту политику для отдельных каналов, включив политику "[Разрешить установку](#install)" для конкретных каналов.</span><span class="sxs-lookup"><span data-stu-id="ff3db-162">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="ff3db-163">Если эта политика отключена, установка Microsoft Edge будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="ff3db-163">If you disable this policy, the installation of Microsoft Edge is blocked.</span></span> <span data-ttu-id="ff3db-164">Эта политика влияет на установку программного обеспечения Microsoft Edge, только если для политики "[Разрешить установку](#install)" задано значение "Не настроено".</span><span class="sxs-lookup"><span data-stu-id="ff3db-164">This only affects the installation of Microsoft Edge software when the '[Allow installation](#install)' policy is set to Not Configured.</span></span>

<span data-ttu-id="ff3db-165">Эта политика не запрещает запуск Центра обновления Microsoft Edge и не запрещает пользователям устанавливать программное обеспечение Microsoft Edge другим способом.</span><span class="sxs-lookup"><span data-stu-id="ff3db-165">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>

<span data-ttu-id="ff3db-166">Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="ff3db-166">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-167">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-167">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-168">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-168">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-169">Уникальное имя групповой политики: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="ff3db-169">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="ff3db-170">Имя групповой политики: Разрешить установку по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ff3db-170">GP name: Allow installation default</span></span>
- <span data-ttu-id="ff3db-171">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="ff3db-171">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="ff3db-172">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-172">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-173">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-173">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-174">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-174">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-175">Имя значения: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="ff3db-175">Value Name: InstallDefault</span></span>
- <span data-ttu-id="ff3db-176">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ff3db-176">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-177">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-177">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="ff3db-178">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-178">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="updatedefault"></a><span data-ttu-id="ff3db-179">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="ff3db-179">UpdateDefault</span></span>
#### <a name="update-policy-override-default"></a><span data-ttu-id="ff3db-180">Переопределение политики обновления по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ff3db-180">Update policy override default</span></span>
><span data-ttu-id="ff3db-181">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-181">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-182">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-182">Description</span></span>
<span data-ttu-id="ff3db-183">Позволяет задать поведение по умолчанию для всех каналов в отношении обработки Центром обновления Microsoft Edge доступных обновлений для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff3db-183">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="ff3db-184">Можно переопределить для отдельных каналов, задав политику "[Переопределение политики обновления](#update)" для этих конкретных каналов.</span><span class="sxs-lookup"><span data-stu-id="ff3db-184">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="ff3db-185">Если эта политика включена, Центр обновления Microsoft Edge обрабатывает обновления Microsoft Edge в соответствии со значениями следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="ff3db-185">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="ff3db-186">Всегда разрешать обновления: обновления всегда применяются при их обнаружении путем периодической автоматической или ручной проверки наличия обновлений.</span><span class="sxs-lookup"><span data-stu-id="ff3db-186">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="ff3db-187">Только обновления, найденные автоматически: обновления применяются только в том случае, если они были найдены при периодической автоматической проверке наличия обновлений.</span><span class="sxs-lookup"><span data-stu-id="ff3db-187">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="ff3db-188">Только обновления, найденные вручную: обновления применяются только в том случае, если пользователь запускает проверку наличия обновлений вручную.</span><span class="sxs-lookup"><span data-stu-id="ff3db-188">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="ff3db-189">Обновления отключены: обновления никогда не применяются.</span><span class="sxs-lookup"><span data-stu-id="ff3db-189">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="ff3db-190">При выборе параметра "Обновления, найденные вручную" периодически проверяйте наличие обновлений с помощью механизма приложения для поиска обновлений вручную, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="ff3db-190">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="ff3db-191">При отключении обновлений разрешите периодическую автоматическую проверку наличия обновлений и их распространение для пользователей.</span><span class="sxs-lookup"><span data-stu-id="ff3db-191">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="ff3db-192">Если вы не включите и не настроите эту политику, Центр обновления Microsoft Edge будет обрабатывать доступные обновления в соответствии с политикой "[Переопределение политики обновления](#update)".</span><span class="sxs-lookup"><span data-stu-id="ff3db-192">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>

  <span data-ttu-id="ff3db-193">Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="ff3db-193">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-194">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-194">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-195">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-195">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-196">Уникальное имя групповой политики: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="ff3db-196">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="ff3db-197">Имя групповой политики: Переопределение политики обновления по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ff3db-197">GP name: Update policy override default</span></span>
- <span data-ttu-id="ff3db-198">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="ff3db-198">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="ff3db-199">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-199">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-200">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-200">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-201">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-201">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-202">Имя значения: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="ff3db-202">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="ff3db-203">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ff3db-203">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-204">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-204">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="ff3db-205">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-205">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="install"></a><span data-ttu-id="ff3db-206">Install</span><span class="sxs-lookup"><span data-stu-id="ff3db-206">Install</span></span>
#### <a name="allow-installation"></a><span data-ttu-id="ff3db-207">Разрешить установку</span><span class="sxs-lookup"><span data-stu-id="ff3db-207">Allow installation</span></span>
><span data-ttu-id="ff3db-208">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-208">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-209">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-209">Description</span></span>
<span data-ttu-id="ff3db-210">Указывает, можно ли установить канал Microsoft Edge на присоединенные к домену устройства.</span><span class="sxs-lookup"><span data-stu-id="ff3db-210">Specifies whether a Microsoft Edge channel can be installed on domain-joined devices.</span></span>

  <span data-ttu-id="ff3db-211">Если эта политика включена для канала, установка Microsoft Edge не будет блокироваться.</span><span class="sxs-lookup"><span data-stu-id="ff3db-211">If you enable this policy for a channel, Microsoft Edge will not be blocked from installation.</span></span>

  <span data-ttu-id="ff3db-212">Если эта политика отключена для канала, установка Microsoft Edge будет блокироваться.</span><span class="sxs-lookup"><span data-stu-id="ff3db-212">If you disable this policy for a channel, Microsoft Edge will be blocked from installation.</span></span>

  <span data-ttu-id="ff3db-213">Если эта политика не настроена для канала, конфигурация политики "[Разрешить установку по умолчанию](#installdefault)" будет определять, смогут ли пользователи устанавливать этот канал Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff3db-213">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge.</span></span>

  <span data-ttu-id="ff3db-214">Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="ff3db-214">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-215">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-215">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-216">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-216">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-217">Уникальное имя групповой политики: Install</span><span class="sxs-lookup"><span data-stu-id="ff3db-217">GP unique name: Install</span></span>
- <span data-ttu-id="ff3db-218">Имя групповой политики: Разрешить установку по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ff3db-218">GP name: Allow installation</span></span>
- <span data-ttu-id="ff3db-219">Путь к групповой политике:</span><span class="sxs-lookup"><span data-stu-id="ff3db-219">GP path:</span></span> 
  - <span data-ttu-id="ff3db-220">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff3db-220">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="ff3db-221">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="ff3db-221">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="ff3db-222">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="ff3db-222">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="ff3db-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="ff3db-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="ff3db-224">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-224">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-225">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-225">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-226">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-226">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-227">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-227">Value Name:</span></span> 
  - <span data-ttu-id="ff3db-228">(Канал Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="ff3db-228">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="ff3db-229">(Канал Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="ff3db-229">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="ff3db-230">(Канал Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="ff3db-230">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="ff3db-231">Канал (Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="ff3db-231">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="ff3db-232">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ff3db-232">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-233">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-233">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="ff3db-234">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-234">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="update"></a><span data-ttu-id="ff3db-235">Update</span><span class="sxs-lookup"><span data-stu-id="ff3db-235">Update</span></span>
#### <a name="update-policy-override"></a><span data-ttu-id="ff3db-236">Переопределение политики обновления</span><span class="sxs-lookup"><span data-stu-id="ff3db-236">Update policy override</span></span>
><span data-ttu-id="ff3db-237">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-237">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-238">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-238">Description</span></span>
<span data-ttu-id="ff3db-239">Указывает, как Центр обновления Microsoft Edge обрабатывает доступные обновления для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff3db-239">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

<span data-ttu-id="ff3db-240">Если эта политика включена, Центр обновления Microsoft Edge обрабатывает обновления Microsoft Edge в соответствии со значениями следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="ff3db-240">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="ff3db-241">Всегда разрешать обновления: обновления всегда применяются при их обнаружении путем периодической автоматической или ручной проверки наличия обновлений.</span><span class="sxs-lookup"><span data-stu-id="ff3db-241">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
  - <span data-ttu-id="ff3db-242">Только обновления, найденные автоматически: обновления применяются только в том случае, если они были найдены при периодической автоматической проверке наличия обновлений.</span><span class="sxs-lookup"><span data-stu-id="ff3db-242">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
  - <span data-ttu-id="ff3db-243">Только обновления, найденные вручную: обновления применяются только в том случае, если пользователь запускает проверку наличия обновлений вручную.</span><span class="sxs-lookup"><span data-stu-id="ff3db-243">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="ff3db-244">(Не все приложения предоставляют интерфейс для этого варианта.)</span><span class="sxs-lookup"><span data-stu-id="ff3db-244">(Not all apps provide an interface for this option.)</span></span>
  - <span data-ttu-id="ff3db-245">Обновления отключены: обновления никогда не применяются.</span><span class="sxs-lookup"><span data-stu-id="ff3db-245">Updates disabled: Updates are never applied.</span></span>

<span data-ttu-id="ff3db-246">При выборе параметра "Обновления, найденные вручную" периодически проверяйте наличие обновлений с помощью механизма приложения для поиска обновлений вручную, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="ff3db-246">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="ff3db-247">При отключении обновлений разрешите периодическую автоматическую проверку наличия обновлений и их распространение для пользователей.</span><span class="sxs-lookup"><span data-stu-id="ff3db-247">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

<span data-ttu-id="ff3db-248">Если вы не включите и не настроите эту политику, Центр обновления Microsoft Edge будет обрабатывать доступные обновления в соответствии с политикой "[Переопределение политики обновления по умолчанию](#updatedefault)".</span><span class="sxs-lookup"><span data-stu-id="ff3db-248">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>

<span data-ttu-id="ff3db-249">Дополнительные сведения см. в статье [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406).</span><span class="sxs-lookup"><span data-stu-id="ff3db-249">See [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) for more information.</span></span>

<span data-ttu-id="ff3db-250">Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="ff3db-250">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-251">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-251">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-252">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-252">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-253">Уникальное имя групповой политики: Update</span><span class="sxs-lookup"><span data-stu-id="ff3db-253">GP unique name: Update</span></span>
- <span data-ttu-id="ff3db-254">Имя групповой политики: Переопределение политики обновления</span><span class="sxs-lookup"><span data-stu-id="ff3db-254">GP name: Update policy override</span></span>
- <span data-ttu-id="ff3db-255">Путь к групповой политике:</span><span class="sxs-lookup"><span data-stu-id="ff3db-255">GP path:</span></span> 
  - <span data-ttu-id="ff3db-256">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff3db-256">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="ff3db-257">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="ff3db-257">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="ff3db-258">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="ff3db-258">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="ff3db-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="ff3db-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="ff3db-260">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-260">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-261">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-261">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-262">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-262">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-263">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-263">Value Name:</span></span> 
  - <span data-ttu-id="ff3db-264">(Канал Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="ff3db-264">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="ff3db-265">(Канал Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="ff3db-265">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="ff3db-266">(Канал Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="ff3db-266">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="ff3db-267">Канал (Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="ff3db-267">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="ff3db-268">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ff3db-268">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-269">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-269">Example value:</span></span>
```
always allow updates 0x00000001
Automatic silent updates only 0x00000003
manual updates only 0x00000002
updates disabled 0x00000000
```
[<span data-ttu-id="ff3db-270">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-270">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="allowsxs"></a><span data-ttu-id="ff3db-271">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="ff3db-271">Allowsxs</span></span>
#### <a name="allow-microsoft-edge-side-by-side-browser-experience"></a><span data-ttu-id="ff3db-272">Разрешить параллельный запуск разных типов браузеров Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff3db-272">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="ff3db-273">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-273">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-274">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-274">Description</span></span>
<span data-ttu-id="ff3db-275">Эта политика позволяет пользователю параллельно запускать Microsoft Edge (Edge HTML) и Microsoft Edge (на основе Chromium).</span><span class="sxs-lookup"><span data-stu-id="ff3db-275">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="ff3db-276">Если для этой политики задано значение "Не настроено", браузер Microsoft Edge (на основе Chromium) заменит Microsoft Edge (Edge HTML) после установки Microsoft Edge (на основе Chromium) в рамках канала Stable, а также обновлений для системы безопасности за ноябрь 2019 года.</span><span class="sxs-lookup"><span data-stu-id="ff3db-276">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="ff3db-277">Поведение параметра "Отключено" такое же.</span><span class="sxs-lookup"><span data-stu-id="ff3db-277">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="ff3db-278">Если параметр "Отключено" блокирует параллельный запуск, браузер Microsoft Edge (на основе Chromium) заменит Microsoft Edge (Edge HTML) после установки Microsoft Edge (на основе Chromium) в рамках канала Stable, а также обновлений для системы безопасности за ноябрь 2019 года.</span><span class="sxs-lookup"><span data-stu-id="ff3db-278">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="ff3db-279">Поведение параметра "Не настроено" такое же.</span><span class="sxs-lookup"><span data-stu-id="ff3db-279">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="ff3db-280">Если эта политика "Включена", браузер Microsoft Edge (на основе Chromium) и браузер Microsoft Edge (HTML Edge) смогут выполняться параллельно после установки Microsoft Edge (на основе Chromium).</span><span class="sxs-lookup"><span data-stu-id="ff3db-280">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="ff3db-281">Чтобы эта групповая политика вступила в силу, ее необходимо настроить до выполнения автоматической установки Microsoft Edge (на основе Chromium) с помощью Центра обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="ff3db-281">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="ff3db-282">Примечание. Пользователь может заблокировать автоматическое обновление Microsoft Edge (на основе Chromium) с помощью набора средств блокировки Microsoft Edge (на основе Chromium).</span><span class="sxs-lookup"><span data-stu-id="ff3db-282">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-283">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-283">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-284">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-284">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-285">Уникальное имя групповой политики: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="ff3db-285">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="ff3db-286">Имя групповой политики: Разрешить параллельный запуск разных типов браузеров Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff3db-286">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="ff3db-287">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="ff3db-287">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="ff3db-288">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-288">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-289">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-289">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-290">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-290">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-291">Имя значения: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="ff3db-291">Value Name: Allowsxs</span></span>
- <span data-ttu-id="ff3db-292">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ff3db-292">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-293">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-293">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="ff3db-294">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-294">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="createdesktopshortcutdefault"></a><span data-ttu-id="ff3db-295">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="ff3db-295">CreateDesktopShortcutDefault</span></span>
#### <a name="prevent-desktop-shortcut-creation-upon-install-default"></a><span data-ttu-id="ff3db-296">Запрет создания ярлыка на рабочем столе при установке по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ff3db-296">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="ff3db-297">Центр обновления Microsoft Edge 1.3.128.0 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-297">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-298">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-298">Description</span></span>
<span data-ttu-id="ff3db-299">Позволяет указать поведение по умолчанию для всех каналов в отношении создания ярлыка на рабочем столе при установке Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff3db-299">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="ff3db-300">Если эта политика включена, при установке Microsoft Edge создается ярлык на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="ff3db-300">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="ff3db-301">Если эта политика отключена, при установке Microsoft Edge ярлык на рабочем столе не создается.</span><span class="sxs-lookup"><span data-stu-id="ff3db-301">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="ff3db-302">Если вы не настроите эту политику, при установке будет создан ярлык Microsoft Edge на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="ff3db-302">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="ff3db-303">Если Microsoft Edge уже установлен, эта политика не действует.</span><span class="sxs-lookup"><span data-stu-id="ff3db-303">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-304">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-304">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-305">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-305">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-306">Уникальное имя групповой политики: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="ff3db-306">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="ff3db-307">Имя групповой политики: Запрет создания ярлыка на рабочем столе при установке по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ff3db-307">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="ff3db-308">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="ff3db-308">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="ff3db-309">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-309">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-310">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-310">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-311">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-311">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-312">Имя значения: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="ff3db-312">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="ff3db-313">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ff3db-313">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-314">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-314">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="ff3db-315">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-315">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="createdesktopshortcut"></a><span data-ttu-id="ff3db-316">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="ff3db-316">CreateDesktopShortcut</span></span>
#### <a name="prevent-desktop-shortcut-creation-upon-install"></a><span data-ttu-id="ff3db-317">Запрет создания ярлыка на рабочем столе при установке</span><span class="sxs-lookup"><span data-stu-id="ff3db-317">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="ff3db-318">Центр обновления Microsoft Edge 1.3.128.0 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-318">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-319">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-319">Description</span></span>
<span data-ttu-id="ff3db-320">Если эта политика включена, при установке Microsoft Edge создается ярлык на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="ff3db-320">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="ff3db-321">Если эта политика отключена, при установке Microsoft Edge ярлык на рабочем столе не создается.</span><span class="sxs-lookup"><span data-stu-id="ff3db-321">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="ff3db-322">Если вы не настроите эту политику, при установке будет создан ярлык Microsoft Edge на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="ff3db-322">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="ff3db-323">Если Microsoft Edge уже установлен, эта политика не действует.</span><span class="sxs-lookup"><span data-stu-id="ff3db-323">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="ff3db-324">Если не настроить эту политику для канала, создание ярлыка при установке Microsoft Edge определяется конфигурацией политики "[Запрет создания ярлыка на рабочем столе при установке по умолчанию](#createdesktopshortcutdefault)".</span><span class="sxs-lookup"><span data-stu-id="ff3db-324">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-325">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-325">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-326">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-326">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-327">Уникальное имя групповой политики: CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="ff3db-327">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="ff3db-328">Имя групповой политики: Запрет создания ярлыка на рабочем столе при установке</span><span class="sxs-lookup"><span data-stu-id="ff3db-328">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="ff3db-329">Путь к групповой политике:</span><span class="sxs-lookup"><span data-stu-id="ff3db-329">GP path:</span></span> 
  - <span data-ttu-id="ff3db-330">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff3db-330">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="ff3db-331">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="ff3db-331">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="ff3db-332">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="ff3db-332">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="ff3db-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="ff3db-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="ff3db-334">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-334">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-335">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-335">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-336">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-336">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-337">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-337">Value Name:</span></span> 
  - <span data-ttu-id="ff3db-338">(Канал Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="ff3db-338">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="ff3db-339">(Канал Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="ff3db-339">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="ff3db-340">(Канал Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="ff3db-340">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="ff3db-341">(Канал Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="ff3db-341">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="ff3db-342">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ff3db-342">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-343">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-343">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="ff3db-344">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-344">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="rollbacktotargetversion"></a><span data-ttu-id="ff3db-345">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="ff3db-345">RollbackToTargetVersion</span></span>
#### <a name="rollback-to-target-version"></a><span data-ttu-id="ff3db-346">Откат к целевой версии</span><span class="sxs-lookup"><span data-stu-id="ff3db-346">Rollback to Target version</span></span>
><span data-ttu-id="ff3db-347">Центр обновления Microsoft Edge 1.3.133.3 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-347">Microsoft Edge Update 1.3.133.3 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-348">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-348">Description</span></span>
<span data-ttu-id="ff3db-349">Указывает, что Центр обновления Microsoft Edge должен откатить установки Microsoft Edge к версии, указанной в политике "'[Переопределение целевой версии](#targetversionprefix)".</span><span class="sxs-lookup"><span data-stu-id="ff3db-349">Specifies that Microsoft Edge Update should rollback installations of Microsoft Edge to the version indicated in '[Target version override](#targetversionprefix)'.</span></span>

<span data-ttu-id="ff3db-350">Эта политика действует, только если для политики "[Переопределение целевой версии](#targetversionprefix)" задано значение и политика "[Переопределение политики обновления](#update)" имеет одно из состояний "ВКЛ." ("Всегда разрешать обновление", "Только автоматическое обновление", "Только обновление вручную").</span><span class="sxs-lookup"><span data-stu-id="ff3db-350">This policy has no effect unless '[Target version override](#targetversionprefix)' is set and '[Update policy override](#update)' is set to one of the ON states (Always allow updates, Automatic silent updates only, Manual updates only).</span></span>

<span data-ttu-id="ff3db-351">Если эта политика отключена или не настроена, установки, имеющие более позднюю версию, чем версия, указанная в политике "[Переопределение целевой версии](#targetversionprefix)", останутся без изменений.</span><span class="sxs-lookup"><span data-stu-id="ff3db-351">If you disable this policy or don't configure it, installs that have a version higher than that specified by '[Target version override](#targetversionprefix)' will be left as-is.</span></span>

<span data-ttu-id="ff3db-352">Если эта политика включена, установки, имеющие более позднюю текущую версию, чем версия, указанная в политике "[Переопределение целевой версии](#targetversionprefix)", будут понижены до целевой версии.</span><span class="sxs-lookup"><span data-stu-id="ff3db-352">If you enable this policy, installs that have a current version higher than specified by the '[Target version override](#targetversionprefix)' will be downgraded to the target version.</span></span>

<span data-ttu-id="ff3db-353">Пользователям рекомендуется устанавливать последнюю версию браузера Microsoft Edge, чтобы обеспечить защиту, предоставляемую новейшими обновлениями для системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="ff3db-353">We recommend that users install the latest version of the Microsoft Edge browser to ensure protection by the latest security updates.</span></span> <span data-ttu-id="ff3db-354">Откат к более ранней версии сопровождается риском возникновения известных проблем безопасности.</span><span class="sxs-lookup"><span data-stu-id="ff3db-354">Rollback to an earlier version risks exposure to known security issues.</span></span> <span data-ttu-id="ff3db-355">Эта политика предназначена для временного решения проблем, связанных с обновлением браузера Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff3db-355">This policy is meant to be used as a temporary fix to address issues in a Microsoft Edge browser update.</span></span>

<span data-ttu-id="ff3db-356">Перед временным откатом версии браузера мы рекомендуем включить синхронизацию ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) для всех пользователей в организации.</span><span class="sxs-lookup"><span data-stu-id="ff3db-356">Before temporarily rolling back your browser version, we recommend that you turn on Sync ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) for all users in your organization.</span></span> <span data-ttu-id="ff3db-357">Если не включить синхронизацию, возникает риск необратимой потери данных браузера.</span><span class="sxs-lookup"><span data-stu-id="ff3db-357">If you don't turn on Sync, there is a risk of permanent browsing data loss.</span></span> <span data-ttu-id="ff3db-358">Вся ответственность за использование этой политики ложится на пользователя.</span><span class="sxs-lookup"><span data-stu-id="ff3db-358">Use this policy at your own risk.</span></span>

<span data-ttu-id="ff3db-359">Примечание. Все версии, доступные для отката, можно посмотреть здесь [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="ff3db-359">Note: All versions available for rollback can be viewed here [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="ff3db-360">Эта политика применяется к Microsoft Edge версии 86 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ff3db-360">This policy applies to Microsoft Edge version 86 or later.</span></span>

<span data-ttu-id="ff3db-361">Дополнительные сведения см. в статье [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918).</span><span class="sxs-lookup"><span data-stu-id="ff3db-361">See [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) for more information.</span></span>

<span data-ttu-id="ff3db-362">Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="ff3db-362">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-363">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-363">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-364">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-364">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-365">Уникальное имя групповой политики: RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="ff3db-365">GP unique name: RollbackToTargetVersion</span></span>
- <span data-ttu-id="ff3db-366">Имя групповой политики: Откат к целевой версии</span><span class="sxs-lookup"><span data-stu-id="ff3db-366">GP name: Rollback to Target version</span></span>
- <span data-ttu-id="ff3db-367">Путь к групповой политике:</span><span class="sxs-lookup"><span data-stu-id="ff3db-367">GP path:</span></span> 
  - <span data-ttu-id="ff3db-368">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff3db-368">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="ff3db-369">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="ff3db-369">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="ff3db-370">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="ff3db-370">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="ff3db-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="ff3db-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="ff3db-372">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-372">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-373">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-373">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-374">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-374">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-375">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-375">Value Name:</span></span> 
  - <span data-ttu-id="ff3db-376">(Канал Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="ff3db-376">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="ff3db-377">(Канал Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="ff3db-377">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="ff3db-378">(Канал Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="ff3db-378">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="ff3db-379">(Канал Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="ff3db-379">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="ff3db-380">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ff3db-380">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-381">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-381">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="ff3db-382">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-382">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="targetversionprefix"></a><span data-ttu-id="ff3db-383">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="ff3db-383">TargetVersionPrefix</span></span>
#### <a name="target-version-override"></a><span data-ttu-id="ff3db-384">Переопределение целевой версии</span><span class="sxs-lookup"><span data-stu-id="ff3db-384">Target version override</span></span>
><span data-ttu-id="ff3db-385">Центр обновления Microsoft Edge 1.3.119.43 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-385">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-386">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-386">Description</span></span>
<span data-ttu-id="ff3db-387">Если эта политика включена и включено автоматическое обновление, Microsoft Edge обновляется до версии, указанной значением этой политики.</span><span class="sxs-lookup"><span data-stu-id="ff3db-387">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="ff3db-388">В качестве значения политики требуется использовать определенную версию Microsoft Edge, например 83.0.499.12.</span><span class="sxs-lookup"><span data-stu-id="ff3db-388">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="ff3db-389">Если на устройстве установлена более поздняя версия Microsoft Edge, чем указано в значении, Microsoft Edge сохранит новую версию и не будет понижен до указанной версии.</span><span class="sxs-lookup"><span data-stu-id="ff3db-389">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="ff3db-390">Если указанная версия не существует или имеет неправильный формат, Microsoft Edge сохранит текущую версию и не будет автоматически обновляться до будущих версий.</span><span class="sxs-lookup"><span data-stu-id="ff3db-390">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>

<span data-ttu-id="ff3db-391">Дополнительные сведения см. в статье [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707).</span><span class="sxs-lookup"><span data-stu-id="ff3db-391">See [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) for more information.</span></span>

<span data-ttu-id="ff3db-392">Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="ff3db-392">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-393">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-393">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-394">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-394">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-395">Уникальное имя групповой политики: TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="ff3db-395">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="ff3db-396">Имя групповой политики: Переопределение целевой версии</span><span class="sxs-lookup"><span data-stu-id="ff3db-396">GP name: Target version override</span></span>
- <span data-ttu-id="ff3db-397">Путь к групповой политике:</span><span class="sxs-lookup"><span data-stu-id="ff3db-397">GP path:</span></span> 
  - <span data-ttu-id="ff3db-398">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff3db-398">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="ff3db-399">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="ff3db-399">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="ff3db-400">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="ff3db-400">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="ff3db-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="ff3db-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="ff3db-402">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-402">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-403">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-403">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-404">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-404">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-405">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-405">Value Name:</span></span> 
  - <span data-ttu-id="ff3db-406">(Канал Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="ff3db-406">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="ff3db-407">(Канал Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="ff3db-407">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="ff3db-408">(Канал Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="ff3db-408">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="ff3db-409">(Канал Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="ff3db-409">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="ff3db-410">Тип значения: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ff3db-410">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-411">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-411">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="ff3db-412">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-412">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="preferences-policies"></a><span data-ttu-id="ff3db-413">Предпочтительные политики</span><span class="sxs-lookup"><span data-stu-id="ff3db-413">Preferences policies</span></span>

[<span data-ttu-id="ff3db-414">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-414">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="autoupdatecheckperiodminutes"></a><span data-ttu-id="ff3db-415">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="ff3db-415">AutoUpdateCheckPeriodMinutes</span></span>
#### <a name="auto-update-check-period-override"></a><span data-ttu-id="ff3db-416">Переопределение периода автоматической проверки обновлений</span><span class="sxs-lookup"><span data-stu-id="ff3db-416">Auto-update check period override</span></span>
><span data-ttu-id="ff3db-417">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-417">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-418">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-418">Description</span></span>
<span data-ttu-id="ff3db-419">Если политика включена, вы можете задать минимальное количество минут между автоматическими проверками обновлений.</span><span class="sxs-lookup"><span data-stu-id="ff3db-419">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="ff3db-420">В противном случае по умолчанию автоматическая проверка наличия обновлений будет выполняться каждые 10 часов.</span><span class="sxs-lookup"><span data-stu-id="ff3db-420">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="ff3db-421">Если необходимо отключить все автоматические проверки обновлений, задайте значение равным 0 (не рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="ff3db-421">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-422">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-422">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-423">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-423">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-424">Уникальное имя групповой политики: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="ff3db-424">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="ff3db-425">Имя групповой политики: Переопределение периода автоматической проверки обновления</span><span class="sxs-lookup"><span data-stu-id="ff3db-425">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="ff3db-426">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Preferences</span><span class="sxs-lookup"><span data-stu-id="ff3db-426">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="ff3db-427">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-427">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-428">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-428">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-429">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-429">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-430">Имя значения: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="ff3db-430">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="ff3db-431">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ff3db-431">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-432">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-432">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="ff3db-433">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-433">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="updatessuppressed"></a><span data-ttu-id="ff3db-434">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="ff3db-434">UpdatesSuppressed</span></span>
#### <a name="time-period-in-each-day-to-suppress-auto-update-check"></a><span data-ttu-id="ff3db-435">Период времени в течение дня, когда будет блокироваться автоматическая проверка обновлений</span><span class="sxs-lookup"><span data-stu-id="ff3db-435">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="ff3db-436">Центр обновления Microsoft Edge 1.3.33.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-436">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-437">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-437">Description</span></span>
<span data-ttu-id="ff3db-438">Если эта политика включена, проверки обновлений блокируются каждый день, начиная с Hour:Minute в течение заданного периода времени (в минутах).</span><span class="sxs-lookup"><span data-stu-id="ff3db-438">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="ff3db-439">На этот период не влияет переход на летнее время.</span><span class="sxs-lookup"><span data-stu-id="ff3db-439">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="ff3db-440">Например, если время начала равно 22:00, а длительность составляет 480 минут, обновления будут блокироваться в течение 8 часов, независимо от этапа перехода на летнее время, то есть его начала или завершения.</span><span class="sxs-lookup"><span data-stu-id="ff3db-440">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="ff3db-441">Если эта политика отключена или не настроена, проверки обновлений не блокируются в течение заданного периода.</span><span class="sxs-lookup"><span data-stu-id="ff3db-441">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-442">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-442">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-443">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-443">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-444">Уникальное имя групповой политики: UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="ff3db-444">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="ff3db-445">Имя групповой политики: Период времени в течение дня, когда будет блокироваться автоматическая проверка обновлений</span><span class="sxs-lookup"><span data-stu-id="ff3db-445">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="ff3db-446">Параметры {Hour, Minute, Duration} (Час, Минута, Длительность)</span><span class="sxs-lookup"><span data-stu-id="ff3db-446">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="ff3db-447">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Preferences</span><span class="sxs-lookup"><span data-stu-id="ff3db-447">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="ff3db-448">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-448">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-449">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-449">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-450">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-450">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-451">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-451">Value Name:</span></span> 
  - <span data-ttu-id="ff3db-452">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="ff3db-452">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="ff3db-453">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="ff3db-453">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="ff3db-454">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="ff3db-454">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="ff3db-455">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ff3db-455">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-456">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-456">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="ff3db-457">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-457">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="proxy-server-policies"></a><span data-ttu-id="ff3db-458">Политики прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="ff3db-458">Proxy Server policies</span></span>

[<span data-ttu-id="ff3db-459">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-459">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="proxymode"></a><span data-ttu-id="ff3db-460">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="ff3db-460">ProxyMode</span></span>
#### <a name="choose-how-to-specify-proxy-server-settings"></a><span data-ttu-id="ff3db-461">Выбор способа задания параметров прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="ff3db-461">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="ff3db-462">Центр обновления Microsoft Edge 1.3.21.81 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-462">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-463">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-463">Description</span></span>
<span data-ttu-id="ff3db-464">Позволяет указать параметры прокси-сервера, используемые Центром обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff3db-464">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="ff3db-465">Если эта политика включена, можно выбрать один из следующих параметров прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="ff3db-465">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="ff3db-466">Если вы решите никогда не использовать прокси-сервер и всегда подключаться напрямую, все остальные параметры будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="ff3db-466">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="ff3db-467">Если вы решите использовать системные параметры прокси-сервера или включите автоматическое определение прокси-сервера, все остальные параметры будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="ff3db-467">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="ff3db-468">При выборе режима фиксированного прокси-сервера можно указать дополнительные параметры в политике "[Адрес или URL-адрес прокси-сервера](#proxyserver)".</span><span class="sxs-lookup"><span data-stu-id="ff3db-468">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="ff3db-469">Если вы решите использовать сценарий прокси-сервера PAC, необходимо указать URL-адрес сценария в политике "[URL-адрес файла PAC прокси-сервера](#proxypacurl)".</span><span class="sxs-lookup"><span data-stu-id="ff3db-469">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="ff3db-470">Если эта политика включена, пользователи в вашей организации не смогут изменять параметры прокси-сервера в Центре обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff3db-470">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="ff3db-471">Если эта политика отключена или не настроена, параметры прокси-сервера не будут заданы, но пользователи в вашей организации смогут задать собственные параметры прокси-сервера для Центра обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff3db-471">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-472">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-472">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-473">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-473">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-474">Уникальное имя групповой политики: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="ff3db-474">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="ff3db-475">Имя групповой политики: Выбор способа задания параметров прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="ff3db-475">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="ff3db-476">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="ff3db-476">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="ff3db-477">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-477">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-478">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-478">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-479">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-479">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-480">Имя значения: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="ff3db-480">Value Name: ProxyMode</span></span>
- <span data-ttu-id="ff3db-481">Тип значения: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ff3db-481">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-482">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-482">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="ff3db-483">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-483">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="proxypacurl"></a><span data-ttu-id="ff3db-484">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="ff3db-484">ProxyPacUrl</span></span>
#### <a name="url-to-a-proxy-pac-file"></a><span data-ttu-id="ff3db-485">URL-адрес файла PAC прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="ff3db-485">URL to a proxy .pac file</span></span>
><span data-ttu-id="ff3db-486">Центр обновления Microsoft Edge 1.3.21.81 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-486">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-487">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-487">Description</span></span>
<span data-ttu-id="ff3db-488">Позволяет указать URL-адрес к файлу автоматической настройки прокси-сервера (PAC).</span><span class="sxs-lookup"><span data-stu-id="ff3db-488">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="ff3db-489">Если эта политика включена, вы можете указать URL-адрес для файла PAC, чтобы автоматизировать процесс выбора подходящего прокси-сервера Центром обновления Microsoft Edge для загрузки конкретного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="ff3db-489">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="ff3db-490">Эта политика применяется только в том случае, если параметры прокси-сервера были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".</span><span class="sxs-lookup"><span data-stu-id="ff3db-490">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="ff3db-491">Не настраивайте эту политику, если параметры прокси-сервера не были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".</span><span class="sxs-lookup"><span data-stu-id="ff3db-491">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-492">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-492">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-493">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-493">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-494">Уникальное имя групповой политики: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="ff3db-494">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="ff3db-495">Имя групповой политики: URL-адрес файла PAC прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="ff3db-495">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="ff3db-496">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="ff3db-496">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="ff3db-497">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-497">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-498">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-498">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-499">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-499">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-500">Имя значения: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="ff3db-500">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="ff3db-501">Тип значения: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ff3db-501">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-502">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-502">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="ff3db-503">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-503">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="proxyserver"></a><span data-ttu-id="ff3db-504">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="ff3db-504">ProxyServer</span></span>
#### <a name="address-or-url-of-proxy-server"></a><span data-ttu-id="ff3db-505">Адрес или URL-адрес прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="ff3db-505">Address or URL of proxy server</span></span>
><span data-ttu-id="ff3db-506">Центр обновления Microsoft Edge 1.3.21.81 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-506">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-507">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-507">Description</span></span>
<span data-ttu-id="ff3db-508">Позволяет указать URL-адрес прокси-сервера, который будет использовать Центр обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff3db-508">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="ff3db-509">Если эта политика включена, вы можете задать URL-адрес прокси сервера, который будет использовать Центр обновления Microsoft Edge в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="ff3db-509">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="ff3db-510">Эта политика применяется только в том случае, если параметры прокси-сервера были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".</span><span class="sxs-lookup"><span data-stu-id="ff3db-510">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="ff3db-511">Не настраивайте эту политику, если параметры прокси-сервера не были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".</span><span class="sxs-lookup"><span data-stu-id="ff3db-511">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-512">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-512">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-513">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-513">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-514">Уникальное имя групповой политики: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="ff3db-514">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="ff3db-515">Имя групповой политики: Адрес или URL-адрес прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="ff3db-515">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="ff3db-516">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="ff3db-516">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="ff3db-517">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-517">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-518">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-518">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-519">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-519">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-520">Имя значения: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="ff3db-520">Value Name: ProxyServer</span></span>
- <span data-ttu-id="ff3db-521">Тип значения: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ff3db-521">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-522">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-522">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="ff3db-523">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-523">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="microsoft-edge-webview-policies"></a><span data-ttu-id="ff3db-524">Политики веб-представления Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff3db-524">Microsoft Edge WebView policies</span></span>

[<span data-ttu-id="ff3db-525">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-525">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="install-webview"></a><span data-ttu-id="ff3db-526">Установка (веб-представление)</span><span class="sxs-lookup"><span data-stu-id="ff3db-526">Install (WebView)</span></span>
#### <a name="allow-installation"></a><span data-ttu-id="ff3db-527">Разрешить установку</span><span class="sxs-lookup"><span data-stu-id="ff3db-527">Allow installation</span></span>
><span data-ttu-id="ff3db-528">Центр обновления Microsoft Edge 1.3.127.1 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-528">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-529">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-529">Description</span></span>
<span data-ttu-id="ff3db-530">Позволяет указать, можно ли установить веб-представление Microsoft Edge с помощью Центра обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff3db-530">Lets you specify whether Microsoft Edge WebView can be installed using Microsoft Edge Update.</span></span>

  - <span data-ttu-id="ff3db-531">Если эта политика включена, пользователи смогут установить веб-представление Microsoft Edge с помощью Центра обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff3db-531">If you enable this policy, users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="ff3db-532">Если эта политика отключена, пользователи не смогут установить веб-представление Microsoft Edge с помощью Центра обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff3db-532">If you disable this policy, users cannot install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="ff3db-533">Если эта политика не настроена, возможность установки пользователями веб-представления Microsoft Edge через Центр обновления Microsoft Edge будет определяться конфигурацией политики "[Разрешить установку по умолчанию](#installdefault)".</span><span class="sxs-lookup"><span data-stu-id="ff3db-533">If you don't configure this policy, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-534">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-534">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-535">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-535">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-536">Уникальное имя групповой политики: Install</span><span class="sxs-lookup"><span data-stu-id="ff3db-536">GP unique name: Install</span></span>
- <span data-ttu-id="ff3db-537">Имя групповой политики: Разрешить установку по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ff3db-537">GP name: Allow installation</span></span>
- <span data-ttu-id="ff3db-538">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="ff3db-538">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="ff3db-539">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-539">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-540">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-540">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-541">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-541">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-542">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-542">Value Name:</span></span> 
  - <span data-ttu-id="ff3db-543">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="ff3db-543">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="ff3db-544">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ff3db-544">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-545">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-545">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="ff3db-546">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-546">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="update-webview"></a><span data-ttu-id="ff3db-547">Обновление (веб-представление)</span><span class="sxs-lookup"><span data-stu-id="ff3db-547">Update (WebView)</span></span>
#### <a name="update-policy-override"></a><span data-ttu-id="ff3db-548">Переопределение политики обновления</span><span class="sxs-lookup"><span data-stu-id="ff3db-548">Update policy override</span></span>
><span data-ttu-id="ff3db-549">Центр обновления Microsoft Edge 1.3.127.1 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ff3db-549">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <a name="description"></a><span data-ttu-id="ff3db-550">Описание</span><span class="sxs-lookup"><span data-stu-id="ff3db-550">Description</span></span>
<span data-ttu-id="ff3db-551">Позволяет указать, включено ли автоматическое обновление для веб-представления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ff3db-551">Lets you specify whether or not automatic updates are enabled for Microsoft Edge WebView.</span></span> <span data-ttu-id="ff3db-552">Веб-представление Microsoft Edge — это компонент, используемый приложениями для отображения веб-содержимого.</span><span class="sxs-lookup"><span data-stu-id="ff3db-552">Microsoft Edge WebView is a component used by applications to display web content.</span></span>
<span data-ttu-id="ff3db-553">Автоматическое обновление включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff3db-553">Automatic updates are enabled by default.</span></span> <span data-ttu-id="ff3db-554">Отключение автоматического обновления веб-представления Microsoft Edge может привести к проблемам совместимости с приложениями, зависящими от этого компонента.</span><span class="sxs-lookup"><span data-stu-id="ff3db-554">Disabling automatic updates for Microsoft Edge WebView might cause compatibility issues with applications that depend on this component.</span></span>

  <span data-ttu-id="ff3db-555">Если эта политика включена, Центр обновления Microsoft Edge обрабатывает обновления веб-представления Microsoft Edge в соответствии со значениями следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="ff3db-555">If you enable this policy, Microsoft Edge Update handles Microsoft Edge WebView updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="ff3db-556">Всегда разрешать обновления. Обновления скачиваются и применяются автоматически</span><span class="sxs-lookup"><span data-stu-id="ff3db-556">Always allow updates: Updates are automatically downloaded and applied</span></span>
  - <span data-ttu-id="ff3db-557">Обновления отключены. Обновления никогда не скачиваются и не применяются</span><span class="sxs-lookup"><span data-stu-id="ff3db-557">Updates disabled: Updates are never downloaded or applied</span></span>

  <span data-ttu-id="ff3db-558">Если эта политика не включена, обновления скачиваются и применяются автоматически.</span><span class="sxs-lookup"><span data-stu-id="ff3db-558">If you don't enable this policy, updates are automatically downloaded and applied.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="ff3db-559">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-559">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="ff3db-560">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="ff3db-560">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="ff3db-561">Уникальное имя групповой политики: Update</span><span class="sxs-lookup"><span data-stu-id="ff3db-561">GP unique name: Update</span></span>
- <span data-ttu-id="ff3db-562">Имя групповой политики: Переопределение политики обновления</span><span class="sxs-lookup"><span data-stu-id="ff3db-562">GP name: Update policy override</span></span>
- <span data-ttu-id="ff3db-563">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="ff3db-563">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="ff3db-564">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="ff3db-564">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="ff3db-565">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="ff3db-565">Windows Registry Settings</span></span>
- <span data-ttu-id="ff3db-566">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="ff3db-566">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="ff3db-567">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-567">Value Name:</span></span> 
  - <span data-ttu-id="ff3db-568">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="ff3db-568">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="ff3db-569">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ff3db-569">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="ff3db-570">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="ff3db-570">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="ff3db-571">В начало</span><span class="sxs-lookup"><span data-stu-id="ff3db-571">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="see-also"></a><span data-ttu-id="ff3db-572">См. также</span><span class="sxs-lookup"><span data-stu-id="ff3db-572">See also</span></span>
  - [<span data-ttu-id="ff3db-573">Настройка Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff3db-573">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="ff3db-574">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="ff3db-574">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
