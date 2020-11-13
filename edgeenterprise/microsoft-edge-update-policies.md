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
ms.openlocfilehash: 0cdcda984efff8d10a84431e44c49ffbf28ddf07
ms.sourcegitcommit: c2ac4f889b625210b9365a60a447482fb5b4c9d4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/12/2020
ms.locfileid: "11167311"
---
# <span data-ttu-id="2601c-103">Microsoft Edge — политики обновления</span><span class="sxs-lookup"><span data-stu-id="2601c-103">Microsoft Edge - Update policies</span></span>

<span data-ttu-id="2601c-104">Последняя версия Microsoft Edge включает в себя следующие политики, которые можно использовать для управления процессом и временем обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2601c-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

<span data-ttu-id="2601c-105">Сведения о других политиках, доступных в Microsoft Edge, см. в [Справочнике по политикам браузера Microsoft Edge](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="2601c-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="2601c-106">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="2601c-106">This article applies to Microsoft Edge version 77 or later.</span></span>
## <span data-ttu-id="2601c-107">Доступные политики</span><span class="sxs-lookup"><span data-stu-id="2601c-107">Available policies</span></span>
<span data-ttu-id="2601c-108">В этих таблицах указаны все групповые политики, связанные с обновлением, доступные в данном выпуске Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2601c-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="2601c-109">Для получения дополнительных сведений о конкретных политиках см. ссылки в таблице.</span><span class="sxs-lookup"><span data-stu-id="2601c-109">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="2601c-110">Приложения</span><span class="sxs-lookup"><span data-stu-id="2601c-110">Applications</span></span>](#applications)|[<span data-ttu-id="2601c-111">Предпочтения</span><span class="sxs-lookup"><span data-stu-id="2601c-111">Preferences</span></span>](#preferences)|
|[<span data-ttu-id="2601c-112">Прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="2601c-112">Proxy Server</span></span>](#proxy-server)|[<span data-ttu-id="2601c-113">Веб-представление Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2601c-113">Microsoft Edge WebView</span></span>](#microsoft-edge-webview)|

### [<span data-ttu-id="2601c-114">Приложения</span><span class="sxs-lookup"><span data-stu-id="2601c-114">Applications</span></span>](#applications-policies)
|<span data-ttu-id="2601c-115">Имя политики</span><span class="sxs-lookup"><span data-stu-id="2601c-115">Policy Name</span></span>|<span data-ttu-id="2601c-116">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2601c-116">Caption</span></span>|
|-|-|
|[<span data-ttu-id="2601c-117">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="2601c-117">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="2601c-118">Разрешить установку по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2601c-118">Allow installation default</span></span>|
|[<span data-ttu-id="2601c-119">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="2601c-119">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="2601c-120">Переопределение политики обновления по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2601c-120">Update policy override default</span></span>|
|[<span data-ttu-id="2601c-121">Install</span><span class="sxs-lookup"><span data-stu-id="2601c-121">Install</span></span>](#install)|<span data-ttu-id="2601c-122">Разрешить установку (для канала)</span><span class="sxs-lookup"><span data-stu-id="2601c-122">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="2601c-123">Update</span><span class="sxs-lookup"><span data-stu-id="2601c-123">Update</span></span>](#update)|<span data-ttu-id="2601c-124">Переопределение политики обновления (для канала)</span><span class="sxs-lookup"><span data-stu-id="2601c-124">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="2601c-125">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="2601c-125">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="2601c-126">Разрешить параллельный запуск разных типов браузеров Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2601c-126">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="2601c-127">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="2601c-127">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="2601c-128">Запрет создания ярлыка на рабочем столе при установке по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2601c-128">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="2601c-129">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="2601c-129">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="2601c-130">Запрет создания ярлыка на рабочем столе при установке (для каналов)</span><span class="sxs-lookup"><span data-stu-id="2601c-130">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="2601c-131">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="2601c-131">RollbackToTargetVersion</span></span>](#rollbacktotargetversion)|<span data-ttu-id="2601c-132">Откат к целевой версии (для каналов)</span><span class="sxs-lookup"><span data-stu-id="2601c-132">Rollback to Target version (per channel)</span></span>|
|[<span data-ttu-id="2601c-133">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="2601c-133">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="2601c-134">Переопределение целевой версии (для каналов)</span><span class="sxs-lookup"><span data-stu-id="2601c-134">Target version override (per channel)</span></span>|

### [<span data-ttu-id="2601c-135">Предпочтения</span><span class="sxs-lookup"><span data-stu-id="2601c-135">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="2601c-136">Имя политики</span><span class="sxs-lookup"><span data-stu-id="2601c-136">Policy Name</span></span>|<span data-ttu-id="2601c-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2601c-137">Caption</span></span>|
|-|-|
|[<span data-ttu-id="2601c-138">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="2601c-138">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="2601c-139">Переопределение периода автоматической проверки обновления</span><span class="sxs-lookup"><span data-stu-id="2601c-139">Auto-update check period override</span></span>|
|[<span data-ttu-id="2601c-140">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="2601c-140">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="2601c-141">Период времени в течение дня, когда будет блокироваться автоматическая проверка обновлений</span><span class="sxs-lookup"><span data-stu-id="2601c-141">Time period in each day to suppress auto-update check</span></span>|

### [<span data-ttu-id="2601c-142">Прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="2601c-142">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="2601c-143">Имя политики</span><span class="sxs-lookup"><span data-stu-id="2601c-143">Policy Name</span></span>|<span data-ttu-id="2601c-144">Действие</span><span class="sxs-lookup"><span data-stu-id="2601c-144">Caption</span></span>|
|-|-|
|[<span data-ttu-id="2601c-145">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="2601c-145">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="2601c-146">Выбор способа задания параметров прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="2601c-146">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="2601c-147">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="2601c-147">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="2601c-148">URL-адрес файла PAC прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="2601c-148">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="2601c-149">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="2601c-149">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="2601c-150">Адрес или URL-адрес прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="2601c-150">Address or URL of proxy server</span></span>|

### [<span data-ttu-id="2601c-151">Веб-представление Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2601c-151">Microsoft Edge WebView</span></span>](#microsoft-edge-webview-policies)
|<span data-ttu-id="2601c-152">Имя политики</span><span class="sxs-lookup"><span data-stu-id="2601c-152">Policy Name</span></span>|<span data-ttu-id="2601c-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2601c-153">Caption</span></span>|
|-|-|
|[<span data-ttu-id="2601c-154">Установка</span><span class="sxs-lookup"><span data-stu-id="2601c-154">Install</span></span>](#install-webview)|<span data-ttu-id="2601c-155">Разрешить установку</span><span class="sxs-lookup"><span data-stu-id="2601c-155">Allow installation</span></span>|
|[<span data-ttu-id="2601c-156">Обновление</span><span class="sxs-lookup"><span data-stu-id="2601c-156">Update</span></span>](#update-webview)|<span data-ttu-id="2601c-157">Переопределение политики обновления</span><span class="sxs-lookup"><span data-stu-id="2601c-157">Update policy override</span></span>|

## <span data-ttu-id="2601c-158">Политики приложений</span><span class="sxs-lookup"><span data-stu-id="2601c-158">Applications policies</span></span>

[<span data-ttu-id="2601c-159">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-159">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="2601c-160">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="2601c-160">InstallDefault</span></span>
#### <span data-ttu-id="2601c-161">Разрешить установку по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2601c-161">Allow installation default</span></span>
><span data-ttu-id="2601c-162">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-162">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="2601c-163">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-163">Description</span></span>
<span data-ttu-id="2601c-164">Вы можете указать поведение по умолчанию для всех каналов: разрешить или заблокировать Microsoft Edge на присоединенных к домену устройствах.</span><span class="sxs-lookup"><span data-stu-id="2601c-164">You can specify the default behavior of all channels to allow or block Microsoft Edge on domain-joined devices.</span></span>

<span data-ttu-id="2601c-165">Вы можете переопределить эту политику для отдельных каналов, включив политику "[Разрешить установку](#install)" для конкретных каналов.</span><span class="sxs-lookup"><span data-stu-id="2601c-165">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="2601c-166">Если эта политика отключена, установка Microsoft Edge будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="2601c-166">If you disable this policy, the installation of Microsoft Edge is blocked.</span></span> <span data-ttu-id="2601c-167">Эта политика влияет на установку программного обеспечения Microsoft Edge, только если для политики "[Разрешить установку](#install)" задано значение "Не настроено".</span><span class="sxs-lookup"><span data-stu-id="2601c-167">This only affects the installation of Microsoft Edge software when the '[Allow installation](#install)' policy is set to Not Configured.</span></span>

<span data-ttu-id="2601c-168">Эта политика не запрещает запуск Центра обновления Microsoft Edge и не запрещает пользователям устанавливать программное обеспечение Microsoft Edge другим способом.</span><span class="sxs-lookup"><span data-stu-id="2601c-168">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>

<span data-ttu-id="2601c-169">Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="2601c-169">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="2601c-170">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-170">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-171">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-171">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-172">Уникальное имя групповой политики: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="2601c-172">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="2601c-173">Имя групповой политики: Разрешить установку по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2601c-173">GP name: Allow installation default</span></span>
- <span data-ttu-id="2601c-174">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="2601c-174">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="2601c-175">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-175">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-176">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-176">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-177">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-177">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-178">Имя значения: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="2601c-178">Value Name: InstallDefault</span></span>
- <span data-ttu-id="2601c-179">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2601c-179">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2601c-180">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-180">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="2601c-181">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-181">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2601c-182">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="2601c-182">UpdateDefault</span></span>
#### <span data-ttu-id="2601c-183">Переопределение политики обновления по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2601c-183">Update policy override default</span></span>
><span data-ttu-id="2601c-184">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-184">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="2601c-185">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-185">Description</span></span>
<span data-ttu-id="2601c-186">Позволяет задать поведение по умолчанию для всех каналов в отношении обработки Центром обновления Microsoft Edge доступных обновлений для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2601c-186">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="2601c-187">Можно переопределить для отдельных каналов, задав политику "[Переопределение политики обновления](#update)" для этих конкретных каналов.</span><span class="sxs-lookup"><span data-stu-id="2601c-187">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="2601c-188">Если эта политика включена, Центр обновления Microsoft Edge обрабатывает обновления Microsoft Edge в соответствии со значениями следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="2601c-188">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="2601c-189">Всегда разрешать обновления: обновления всегда применяются при их обнаружении путем периодической автоматической или ручной проверки наличия обновлений.</span><span class="sxs-lookup"><span data-stu-id="2601c-189">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="2601c-190">Только обновления, найденные автоматически: обновления применяются только в том случае, если они были найдены при периодической автоматической проверке наличия обновлений.</span><span class="sxs-lookup"><span data-stu-id="2601c-190">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="2601c-191">Только обновления, найденные вручную: обновления применяются только в том случае, если пользователь запускает проверку наличия обновлений вручную.</span><span class="sxs-lookup"><span data-stu-id="2601c-191">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="2601c-192">Обновления отключены: обновления никогда не применяются.</span><span class="sxs-lookup"><span data-stu-id="2601c-192">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="2601c-193">При выборе параметра "Обновления, найденные вручную" периодически проверяйте наличие обновлений с помощью механизма приложения для поиска обновлений вручную, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="2601c-193">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="2601c-194">При отключении обновлений разрешите периодическую автоматическую проверку наличия обновлений и их распространение для пользователей.</span><span class="sxs-lookup"><span data-stu-id="2601c-194">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="2601c-195">Если вы не включите и не настроите эту политику, Центр обновления Microsoft Edge будет обрабатывать доступные обновления в соответствии с политикой "[Переопределение политики обновления](#update)".</span><span class="sxs-lookup"><span data-stu-id="2601c-195">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>

  <span data-ttu-id="2601c-196">Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="2601c-196">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="2601c-197">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-197">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-198">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-198">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-199">Уникальное имя групповой политики: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="2601c-199">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="2601c-200">Имя групповой политики: Переопределение политики обновления по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2601c-200">GP name: Update policy override default</span></span>
- <span data-ttu-id="2601c-201">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="2601c-201">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="2601c-202">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-202">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-203">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-203">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-204">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-204">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-205">Имя значения: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="2601c-205">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="2601c-206">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2601c-206">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2601c-207">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-207">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="2601c-208">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-208">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2601c-209">Install</span><span class="sxs-lookup"><span data-stu-id="2601c-209">Install</span></span>
#### <span data-ttu-id="2601c-210">Разрешить установку</span><span class="sxs-lookup"><span data-stu-id="2601c-210">Allow installation</span></span>
><span data-ttu-id="2601c-211">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-211">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="2601c-212">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-212">Description</span></span>
<span data-ttu-id="2601c-213">Указывает, можно ли установить канал Microsoft Edge на присоединенные к домену устройства.</span><span class="sxs-lookup"><span data-stu-id="2601c-213">Specifies whether a Microsoft Edge channel can be installed on domain-joined devices.</span></span>

  <span data-ttu-id="2601c-214">Если эта политика включена для канала, установка Microsoft Edge не будет блокироваться.</span><span class="sxs-lookup"><span data-stu-id="2601c-214">If you enable this policy for a channel, Microsoft Edge will not be blocked from installation.</span></span>

  <span data-ttu-id="2601c-215">Если эта политика отключена для канала, установка Microsoft Edge будет блокироваться.</span><span class="sxs-lookup"><span data-stu-id="2601c-215">If you disable this policy for a channel, Microsoft Edge will be blocked from installation.</span></span>

  <span data-ttu-id="2601c-216">Если эта политика не настроена для канала, конфигурация политики "[Разрешить установку по умолчанию](#installdefault)" будет определять, смогут ли пользователи устанавливать этот канал Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2601c-216">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge.</span></span>

  <span data-ttu-id="2601c-217">Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="2601c-217">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="2601c-218">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-218">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-219">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-219">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-220">Уникальное имя групповой политики: Install</span><span class="sxs-lookup"><span data-stu-id="2601c-220">GP unique name: Install</span></span>
- <span data-ttu-id="2601c-221">Имя групповой политики: Разрешить установку по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2601c-221">GP name: Allow installation</span></span>
- <span data-ttu-id="2601c-222">Путь к групповой политике:</span><span class="sxs-lookup"><span data-stu-id="2601c-222">GP path:</span></span> 
  - <span data-ttu-id="2601c-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2601c-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="2601c-224">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="2601c-224">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="2601c-225">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="2601c-225">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="2601c-226">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="2601c-226">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="2601c-227">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-227">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-228">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-228">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-229">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-229">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-230">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-230">Value Name:</span></span> 
  - <span data-ttu-id="2601c-231">(Канал Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="2601c-231">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="2601c-232">(Канал Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="2601c-232">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="2601c-233">(Канал Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="2601c-233">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="2601c-234">Канал (Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="2601c-234">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="2601c-235">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2601c-235">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2601c-236">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-236">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="2601c-237">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-237">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2601c-238">Update</span><span class="sxs-lookup"><span data-stu-id="2601c-238">Update</span></span>
#### <span data-ttu-id="2601c-239">Переопределение политики обновления</span><span class="sxs-lookup"><span data-stu-id="2601c-239">Update policy override</span></span>
><span data-ttu-id="2601c-240">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-240">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="2601c-241">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-241">Description</span></span>
<span data-ttu-id="2601c-242">Указывает, как Центр обновления Microsoft Edge обрабатывает доступные обновления для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2601c-242">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

<span data-ttu-id="2601c-243">Если эта политика включена, Центр обновления Microsoft Edge обрабатывает обновления Microsoft Edge в соответствии со значениями следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="2601c-243">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="2601c-244">Всегда разрешать обновления: обновления всегда применяются при их обнаружении путем периодической автоматической или ручной проверки наличия обновлений.</span><span class="sxs-lookup"><span data-stu-id="2601c-244">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
  - <span data-ttu-id="2601c-245">Только обновления, найденные автоматически: обновления применяются только в том случае, если они были найдены при периодической автоматической проверке наличия обновлений.</span><span class="sxs-lookup"><span data-stu-id="2601c-245">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
  - <span data-ttu-id="2601c-246">Только обновления, найденные вручную: обновления применяются только в том случае, если пользователь запускает проверку наличия обновлений вручную.</span><span class="sxs-lookup"><span data-stu-id="2601c-246">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="2601c-247">(Не все приложения предоставляют интерфейс для этого варианта.)</span><span class="sxs-lookup"><span data-stu-id="2601c-247">(Not all apps provide an interface for this option.)</span></span>
  - <span data-ttu-id="2601c-248">Обновления отключены: обновления никогда не применяются.</span><span class="sxs-lookup"><span data-stu-id="2601c-248">Updates disabled: Updates are never applied.</span></span>

<span data-ttu-id="2601c-249">При выборе параметра "Обновления, найденные вручную" периодически проверяйте наличие обновлений с помощью механизма приложения для поиска обновлений вручную, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="2601c-249">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="2601c-250">При отключении обновлений разрешите периодическую автоматическую проверку наличия обновлений и их распространение для пользователей.</span><span class="sxs-lookup"><span data-stu-id="2601c-250">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

<span data-ttu-id="2601c-251">Если вы не включите и не настроите эту политику, Центр обновления Microsoft Edge будет обрабатывать доступные обновления в соответствии с политикой "[Переопределение политики обновления по умолчанию](#updatedefault)".</span><span class="sxs-lookup"><span data-stu-id="2601c-251">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>

<span data-ttu-id="2601c-252">Дополнительные сведения см. в статье [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406).</span><span class="sxs-lookup"><span data-stu-id="2601c-252">See [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) for more information.</span></span>

<span data-ttu-id="2601c-253">Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="2601c-253">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="2601c-254">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-254">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-255">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-255">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-256">Уникальное имя групповой политики: Update</span><span class="sxs-lookup"><span data-stu-id="2601c-256">GP unique name: Update</span></span>
- <span data-ttu-id="2601c-257">Имя групповой политики: Переопределение политики обновления</span><span class="sxs-lookup"><span data-stu-id="2601c-257">GP name: Update policy override</span></span>
- <span data-ttu-id="2601c-258">Путь к групповой политике:</span><span class="sxs-lookup"><span data-stu-id="2601c-258">GP path:</span></span> 
  - <span data-ttu-id="2601c-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2601c-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="2601c-260">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="2601c-260">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="2601c-261">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="2601c-261">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="2601c-262">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="2601c-262">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="2601c-263">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-263">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-264">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-264">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-265">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-265">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-266">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-266">Value Name:</span></span> 
  - <span data-ttu-id="2601c-267">(Канал Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="2601c-267">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="2601c-268">(Канал Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="2601c-268">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="2601c-269">(Канал Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="2601c-269">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="2601c-270">Канал (Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="2601c-270">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="2601c-271">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2601c-271">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2601c-272">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-272">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="2601c-273">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-273">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2601c-274">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="2601c-274">Allowsxs</span></span>
#### <span data-ttu-id="2601c-275">Разрешить параллельный запуск разных типов браузеров Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2601c-275">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="2601c-276">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-276">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="2601c-277">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-277">Description</span></span>
<span data-ttu-id="2601c-278">Эта политика позволяет пользователю параллельно запускать Microsoft Edge (Edge HTML) и Microsoft Edge (на основе Chromium).</span><span class="sxs-lookup"><span data-stu-id="2601c-278">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="2601c-279">Если для этой политики задано значение "Не настроено", браузер Microsoft Edge (на основе Chromium) заменит Microsoft Edge (Edge HTML) после установки Microsoft Edge (на основе Chromium) в рамках канала Stable, а также обновлений для системы безопасности за ноябрь 2019 года.</span><span class="sxs-lookup"><span data-stu-id="2601c-279">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="2601c-280">Поведение параметра "Отключено" такое же.</span><span class="sxs-lookup"><span data-stu-id="2601c-280">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="2601c-281">Если параметр "Отключено" блокирует параллельный запуск, браузер Microsoft Edge (на основе Chromium) заменит Microsoft Edge (Edge HTML) после установки Microsoft Edge (на основе Chromium) в рамках канала Stable, а также обновлений для системы безопасности за ноябрь 2019 года.</span><span class="sxs-lookup"><span data-stu-id="2601c-281">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="2601c-282">Поведение параметра "Не настроено" такое же.</span><span class="sxs-lookup"><span data-stu-id="2601c-282">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="2601c-283">Если эта политика "Включена", браузер Microsoft Edge (на основе Chromium) и браузер Microsoft Edge (HTML Edge) смогут выполняться параллельно после установки Microsoft Edge (на основе Chromium).</span><span class="sxs-lookup"><span data-stu-id="2601c-283">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="2601c-284">Чтобы эта групповая политика вступила в силу, ее необходимо настроить до выполнения автоматической установки Microsoft Edge (на основе Chromium) с помощью Центра обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="2601c-284">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="2601c-285">Примечание. Пользователь может заблокировать автоматическое обновление Microsoft Edge (на основе Chromium) с помощью набора средств блокировки Microsoft Edge (на основе Chromium).</span><span class="sxs-lookup"><span data-stu-id="2601c-285">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <span data-ttu-id="2601c-286">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-286">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-287">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-287">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-288">Уникальное имя групповой политики: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="2601c-288">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="2601c-289">Имя групповой политики: Разрешить параллельный запуск разных типов браузеров Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2601c-289">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="2601c-290">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="2601c-290">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="2601c-291">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-291">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-292">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-292">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-293">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-293">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-294">Имя значения: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="2601c-294">Value Name: Allowsxs</span></span>
- <span data-ttu-id="2601c-295">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2601c-295">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2601c-296">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-296">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="2601c-297">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-297">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2601c-298">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="2601c-298">CreateDesktopShortcutDefault</span></span>
#### <span data-ttu-id="2601c-299">Запрет создания ярлыка на рабочем столе при установке по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2601c-299">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="2601c-300">Центр обновления Microsoft Edge 1.3.128.0 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-300">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="2601c-301">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-301">Description</span></span>
<span data-ttu-id="2601c-302">Позволяет указать поведение по умолчанию для всех каналов в отношении создания ярлыка на рабочем столе при установке Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2601c-302">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="2601c-303">Если эта политика включена, при установке Microsoft Edge создается ярлык на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="2601c-303">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="2601c-304">Если эта политика отключена, при установке Microsoft Edge ярлык на рабочем столе не создается.</span><span class="sxs-lookup"><span data-stu-id="2601c-304">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="2601c-305">Если вы не настроите эту политику, при установке будет создан ярлык Microsoft Edge на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="2601c-305">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="2601c-306">Если Microsoft Edge уже установлен, эта политика не действует.</span><span class="sxs-lookup"><span data-stu-id="2601c-306">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <span data-ttu-id="2601c-307">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-307">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-308">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-308">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-309">Уникальное имя групповой политики: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="2601c-309">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="2601c-310">Имя групповой политики: Запрет создания ярлыка на рабочем столе при установке по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2601c-310">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="2601c-311">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="2601c-311">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="2601c-312">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-312">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-313">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-313">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-314">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-314">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-315">Имя значения: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="2601c-315">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="2601c-316">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2601c-316">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2601c-317">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-317">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="2601c-318">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-318">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2601c-319">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="2601c-319">CreateDesktopShortcut</span></span>
#### <span data-ttu-id="2601c-320">Запрет создания ярлыка на рабочем столе при установке</span><span class="sxs-lookup"><span data-stu-id="2601c-320">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="2601c-321">Центр обновления Microsoft Edge 1.3.128.0 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-321">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="2601c-322">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-322">Description</span></span>
<span data-ttu-id="2601c-323">Если эта политика включена, при установке Microsoft Edge создается ярлык на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="2601c-323">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="2601c-324">Если эта политика отключена, при установке Microsoft Edge ярлык на рабочем столе не создается.</span><span class="sxs-lookup"><span data-stu-id="2601c-324">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="2601c-325">Если вы не настроите эту политику, при установке будет создан ярлык Microsoft Edge на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="2601c-325">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="2601c-326">Если Microsoft Edge уже установлен, эта политика не действует.</span><span class="sxs-lookup"><span data-stu-id="2601c-326">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="2601c-327">Если не настроить эту политику для канала, создание ярлыка при установке Microsoft Edge определяется конфигурацией политики "[Запрет создания ярлыка на рабочем столе при установке по умолчанию](#createdesktopshortcutdefault)".</span><span class="sxs-lookup"><span data-stu-id="2601c-327">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <span data-ttu-id="2601c-328">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-328">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-329">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-329">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-330">Уникальное имя групповой политики: CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="2601c-330">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="2601c-331">Имя групповой политики: Запрет создания ярлыка на рабочем столе при установке</span><span class="sxs-lookup"><span data-stu-id="2601c-331">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="2601c-332">Путь к групповой политике:</span><span class="sxs-lookup"><span data-stu-id="2601c-332">GP path:</span></span> 
  - <span data-ttu-id="2601c-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2601c-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="2601c-334">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="2601c-334">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="2601c-335">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="2601c-335">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="2601c-336">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="2601c-336">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="2601c-337">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-337">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-338">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-338">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-339">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-339">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-340">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-340">Value Name:</span></span> 
  - <span data-ttu-id="2601c-341">(Канал Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="2601c-341">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="2601c-342">(Канал Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="2601c-342">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="2601c-343">(Канал Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="2601c-343">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="2601c-344">(Канал Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="2601c-344">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="2601c-345">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2601c-345">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2601c-346">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-346">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="2601c-347">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-347">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2601c-348">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="2601c-348">RollbackToTargetVersion</span></span>
#### <span data-ttu-id="2601c-349">Откат к целевой версии</span><span class="sxs-lookup"><span data-stu-id="2601c-349">Rollback to Target version</span></span>
><span data-ttu-id="2601c-350">Центр обновления Microsoft Edge 1.3.133.3 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-350">Microsoft Edge Update 1.3.133.3 and later</span></span>

#### <span data-ttu-id="2601c-351">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-351">Description</span></span>
<span data-ttu-id="2601c-352">Указывает, что Центр обновления Microsoft Edge должен откатить установки Microsoft Edge к версии, указанной в политике "'[Переопределение целевой версии](#targetversionprefix)".</span><span class="sxs-lookup"><span data-stu-id="2601c-352">Specifies that Microsoft Edge Update should rollback installations of Microsoft Edge to the version indicated in '[Target version override](#targetversionprefix)'.</span></span>

<span data-ttu-id="2601c-353">Эта политика действует, только если для политики "[Переопределение целевой версии](#targetversionprefix)" задано значение и политика "[Переопределение политики обновления](#update)" имеет одно из состояний "ВКЛ." ("Всегда разрешать обновление", "Только автоматическое обновление", "Только обновление вручную").</span><span class="sxs-lookup"><span data-stu-id="2601c-353">This policy has no effect unless '[Target version override](#targetversionprefix)' is set and '[Update policy override](#update)' is set to one of the ON states (Always allow updates, Automatic silent updates only, Manual updates only).</span></span>

<span data-ttu-id="2601c-354">Если эта политика отключена или не настроена, установки, имеющие более позднюю версию, чем версия, указанная в политике "[Переопределение целевой версии](#targetversionprefix)", останутся без изменений.</span><span class="sxs-lookup"><span data-stu-id="2601c-354">If you disable this policy or don't configure it, installs that have a version higher than that specified by '[Target version override](#targetversionprefix)' will be left as-is.</span></span>

<span data-ttu-id="2601c-355">Если эта политика включена, установки, имеющие более позднюю текущую версию, чем версия, указанная в политике "[Переопределение целевой версии](#targetversionprefix)", будут понижены до целевой версии.</span><span class="sxs-lookup"><span data-stu-id="2601c-355">If you enable this policy, installs that have a current version higher than specified by the '[Target version override](#targetversionprefix)' will be downgraded to the target version.</span></span>

<span data-ttu-id="2601c-356">Пользователям рекомендуется устанавливать последнюю версию браузера Microsoft Edge, чтобы обеспечить защиту, предоставляемую новейшими обновлениями для системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="2601c-356">We recommend that users install the latest version of the Microsoft Edge browser to ensure protection by the latest security updates.</span></span> <span data-ttu-id="2601c-357">Откат к более ранней версии сопровождается риском возникновения известных проблем безопасности.</span><span class="sxs-lookup"><span data-stu-id="2601c-357">Rollback to an earlier version risks exposure to known security issues.</span></span> <span data-ttu-id="2601c-358">Эта политика предназначена для временного решения проблем, связанных с обновлением браузера Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2601c-358">This policy is meant to be used as a temporary fix to address issues in a Microsoft Edge browser update.</span></span>

<span data-ttu-id="2601c-359">Перед временным откатом версии браузера мы рекомендуем включить синхронизацию ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) для всех пользователей в организации.</span><span class="sxs-lookup"><span data-stu-id="2601c-359">Before temporarily rolling back your browser version, we recommend that you turn on Sync ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) for all users in your organization.</span></span> <span data-ttu-id="2601c-360">Если не включить синхронизацию, возникает риск необратимой потери данных браузера.</span><span class="sxs-lookup"><span data-stu-id="2601c-360">If you don't turn on Sync, there is a risk of permanent browsing data loss.</span></span> <span data-ttu-id="2601c-361">Вся ответственность за использование этой политики ложится на пользователя.</span><span class="sxs-lookup"><span data-stu-id="2601c-361">Use this policy at your own risk.</span></span>

<span data-ttu-id="2601c-362">Примечание. Все версии, доступные для отката, можно посмотреть здесь [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="2601c-362">Note: All versions available for rollback can be viewed here [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="2601c-363">Эта политика применяется к Microsoft Edge версии 86 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="2601c-363">This policy applies to Microsoft Edge version 86 or later.</span></span>

<span data-ttu-id="2601c-364">Дополнительные сведения см. в статье [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918).</span><span class="sxs-lookup"><span data-stu-id="2601c-364">See [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) for more information.</span></span>

<span data-ttu-id="2601c-365">Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="2601c-365">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="2601c-366">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-366">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-367">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-367">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-368">Уникальное имя групповой политики: RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="2601c-368">GP unique name: RollbackToTargetVersion</span></span>
- <span data-ttu-id="2601c-369">Имя групповой политики: Откат к целевой версии</span><span class="sxs-lookup"><span data-stu-id="2601c-369">GP name: Rollback to Target version</span></span>
- <span data-ttu-id="2601c-370">Путь к групповой политике:</span><span class="sxs-lookup"><span data-stu-id="2601c-370">GP path:</span></span> 
  - <span data-ttu-id="2601c-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2601c-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="2601c-372">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="2601c-372">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="2601c-373">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="2601c-373">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="2601c-374">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="2601c-374">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="2601c-375">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-375">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-376">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-376">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-377">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-377">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-378">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-378">Value Name:</span></span> 
  - <span data-ttu-id="2601c-379">(Канал Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="2601c-379">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="2601c-380">(Канал Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="2601c-380">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="2601c-381">(Канал Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="2601c-381">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="2601c-382">(Канал Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="2601c-382">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="2601c-383">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2601c-383">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2601c-384">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-384">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="2601c-385">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-385">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2601c-386">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="2601c-386">TargetVersionPrefix</span></span>
#### <span data-ttu-id="2601c-387">Переопределение целевой версии</span><span class="sxs-lookup"><span data-stu-id="2601c-387">Target version override</span></span>
><span data-ttu-id="2601c-388">Центр обновления Microsoft Edge 1.3.119.43 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-388">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <span data-ttu-id="2601c-389">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-389">Description</span></span>
<span data-ttu-id="2601c-390">Если эта политика включена и включено автоматическое обновление, Microsoft Edge обновляется до версии, указанной значением этой политики.</span><span class="sxs-lookup"><span data-stu-id="2601c-390">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="2601c-391">В качестве значения политики требуется использовать определенную версию Microsoft Edge, например 83.0.499.12.</span><span class="sxs-lookup"><span data-stu-id="2601c-391">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="2601c-392">Если на устройстве установлена более поздняя версия Microsoft Edge, чем указано в значении, Microsoft Edge сохранит новую версию и не будет понижен до указанной версии.</span><span class="sxs-lookup"><span data-stu-id="2601c-392">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="2601c-393">Если указанная версия не существует или имеет неправильный формат, Microsoft Edge сохранит текущую версию и не будет автоматически обновляться до будущих версий.</span><span class="sxs-lookup"><span data-stu-id="2601c-393">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>

<span data-ttu-id="2601c-394">Дополнительные сведения см. в статье [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707).</span><span class="sxs-lookup"><span data-stu-id="2601c-394">See [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) for more information.</span></span>

<span data-ttu-id="2601c-395">Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="2601c-395">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="2601c-396">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-396">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-397">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-397">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-398">Уникальное имя групповой политики: TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="2601c-398">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="2601c-399">Имя групповой политики: Переопределение целевой версии</span><span class="sxs-lookup"><span data-stu-id="2601c-399">GP name: Target version override</span></span>
- <span data-ttu-id="2601c-400">Путь к групповой политике:</span><span class="sxs-lookup"><span data-stu-id="2601c-400">GP path:</span></span> 
  - <span data-ttu-id="2601c-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2601c-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="2601c-402">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="2601c-402">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="2601c-403">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="2601c-403">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="2601c-404">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="2601c-404">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="2601c-405">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-405">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-406">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-406">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-407">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-407">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-408">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-408">Value Name:</span></span> 
  - <span data-ttu-id="2601c-409">(Канал Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="2601c-409">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="2601c-410">(Канал Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="2601c-410">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="2601c-411">(Канал Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="2601c-411">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="2601c-412">(Канал Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="2601c-412">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="2601c-413">Тип значения: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2601c-413">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="2601c-414">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-414">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="2601c-415">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-415">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="2601c-416">Предпочтительные политики</span><span class="sxs-lookup"><span data-stu-id="2601c-416">Preferences policies</span></span>

[<span data-ttu-id="2601c-417">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-417">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="2601c-418">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="2601c-418">AutoUpdateCheckPeriodMinutes</span></span>
#### <span data-ttu-id="2601c-419">Переопределение периода автоматической проверки обновлений</span><span class="sxs-lookup"><span data-stu-id="2601c-419">Auto-update check period override</span></span>
><span data-ttu-id="2601c-420">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-420">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="2601c-421">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-421">Description</span></span>
<span data-ttu-id="2601c-422">Если политика включена, вы можете задать минимальное количество минут между автоматическими проверками обновлений.</span><span class="sxs-lookup"><span data-stu-id="2601c-422">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="2601c-423">В противном случае по умолчанию автоматическая проверка наличия обновлений будет выполняться каждые 10 часов.</span><span class="sxs-lookup"><span data-stu-id="2601c-423">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="2601c-424">Если необходимо отключить все автоматические проверки обновлений, задайте значение равным 0 (не рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="2601c-424">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <span data-ttu-id="2601c-425">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-425">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-426">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-426">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-427">Уникальное имя групповой политики: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="2601c-427">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="2601c-428">Имя групповой политики: Переопределение периода автоматической проверки обновления</span><span class="sxs-lookup"><span data-stu-id="2601c-428">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="2601c-429">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Preferences</span><span class="sxs-lookup"><span data-stu-id="2601c-429">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="2601c-430">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-430">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-431">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-431">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-432">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-432">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-433">Имя значения: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="2601c-433">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="2601c-434">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2601c-434">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2601c-435">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-435">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="2601c-436">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-436">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2601c-437">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="2601c-437">UpdatesSuppressed</span></span>
#### <span data-ttu-id="2601c-438">Период времени в течение дня, когда будет блокироваться автоматическая проверка обновлений</span><span class="sxs-lookup"><span data-stu-id="2601c-438">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="2601c-439">Центр обновления Microsoft Edge 1.3.33.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-439">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <span data-ttu-id="2601c-440">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-440">Description</span></span>
<span data-ttu-id="2601c-441">Если эта политика включена, проверки обновлений блокируются каждый день, начиная с Hour:Minute в течение заданного периода времени (в минутах).</span><span class="sxs-lookup"><span data-stu-id="2601c-441">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="2601c-442">На этот период не влияет переход на летнее время.</span><span class="sxs-lookup"><span data-stu-id="2601c-442">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="2601c-443">Например, если время начала равно 22:00, а длительность составляет 480минут, обновления будут блокироваться в течение 8 часов, независимо от этапа перехода на летнее время, то есть его начала или завершения.</span><span class="sxs-lookup"><span data-stu-id="2601c-443">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="2601c-444">Если эта политика отключена или не настроена, проверки обновлений не блокируются в течение заданного периода.</span><span class="sxs-lookup"><span data-stu-id="2601c-444">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <span data-ttu-id="2601c-445">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-445">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-446">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-446">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-447">Уникальное имя групповой политики: UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="2601c-447">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="2601c-448">Имя групповой политики: Период времени в течение дня, когда будет блокироваться автоматическая проверка обновлений</span><span class="sxs-lookup"><span data-stu-id="2601c-448">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="2601c-449">Параметры {Hour, Minute, Duration} (Час, Минута, Длительность)</span><span class="sxs-lookup"><span data-stu-id="2601c-449">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="2601c-450">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Preferences</span><span class="sxs-lookup"><span data-stu-id="2601c-450">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="2601c-451">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-451">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-452">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-452">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-453">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-453">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-454">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-454">Value Name:</span></span> 
  - <span data-ttu-id="2601c-455">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="2601c-455">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="2601c-456">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="2601c-456">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="2601c-457">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="2601c-457">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="2601c-458">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2601c-458">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2601c-459">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-459">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="2601c-460">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-460">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="2601c-461">Политики прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="2601c-461">Proxy Server policies</span></span>

[<span data-ttu-id="2601c-462">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-462">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="2601c-463">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="2601c-463">ProxyMode</span></span>
#### <span data-ttu-id="2601c-464">Выбор способа задания параметров прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="2601c-464">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="2601c-465">Центр обновления Microsoft Edge 1.3.21.81 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-465">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="2601c-466">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-466">Description</span></span>
<span data-ttu-id="2601c-467">Позволяет указать параметры прокси-сервера, используемые Центром обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2601c-467">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="2601c-468">Если эта политика включена, можно выбрать один из следующих параметров прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="2601c-468">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="2601c-469">Если вы решите никогда не использовать прокси-сервер и всегда подключаться напрямую, все остальные параметры будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="2601c-469">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="2601c-470">Если вы решите использовать системные параметры прокси-сервера или включите автоматическое определение прокси-сервера, все остальные параметры будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="2601c-470">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="2601c-471">При выборе режима фиксированного прокси-сервера можно указать дополнительные параметры в политике "[Адрес или URL-адрес прокси-сервера](#proxyserver)".</span><span class="sxs-lookup"><span data-stu-id="2601c-471">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="2601c-472">Если вы решите использовать сценарий прокси-сервера PAC, необходимо указать URL-адрес сценария в политике "[URL-адрес файла PAC прокси-сервера](#proxypacurl)".</span><span class="sxs-lookup"><span data-stu-id="2601c-472">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="2601c-473">Если эта политика включена, пользователи в вашей организации не смогут изменять параметры прокси-сервера в Центре обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2601c-473">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="2601c-474">Если эта политика отключена или не настроена, параметры прокси-сервера не будут заданы, но пользователи в вашей организации смогут задать собственные параметры прокси-сервера для Центра обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2601c-474">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <span data-ttu-id="2601c-475">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-475">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-476">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-476">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-477">Уникальное имя групповой политики: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="2601c-477">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="2601c-478">Имя групповой политики: Выбор способа задания параметров прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="2601c-478">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="2601c-479">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="2601c-479">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="2601c-480">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-480">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-481">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-481">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-482">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-482">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-483">Имя значения: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="2601c-483">Value Name: ProxyMode</span></span>
- <span data-ttu-id="2601c-484">Тип значения: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2601c-484">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="2601c-485">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-485">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="2601c-486">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-486">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2601c-487">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="2601c-487">ProxyPacUrl</span></span>
#### <span data-ttu-id="2601c-488">URL-адрес файла PAC прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="2601c-488">URL to a proxy .pac file</span></span>
><span data-ttu-id="2601c-489">Центр обновления Microsoft Edge 1.3.21.81 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-489">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="2601c-490">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-490">Description</span></span>
<span data-ttu-id="2601c-491">Позволяет указать URL-адрес к файлу автоматической настройки прокси-сервера (PAC).</span><span class="sxs-lookup"><span data-stu-id="2601c-491">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="2601c-492">Если эта политика включена, вы можете указать URL-адрес для файла PAC, чтобы автоматизировать процесс выбора подходящего прокси-сервера Центром обновления Microsoft Edge для загрузки конкретного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="2601c-492">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="2601c-493">Эта политика применяется только в том случае, если параметры прокси-сервера были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".</span><span class="sxs-lookup"><span data-stu-id="2601c-493">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="2601c-494">Не настраивайте эту политику, если параметры прокси-сервера не были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".</span><span class="sxs-lookup"><span data-stu-id="2601c-494">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="2601c-495">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-495">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-496">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-496">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-497">Уникальное имя групповой политики: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="2601c-497">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="2601c-498">Имя групповой политики: URL-адрес файла PAC прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="2601c-498">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="2601c-499">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="2601c-499">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="2601c-500">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-500">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-501">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-501">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-502">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-502">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-503">Имя значения: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="2601c-503">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="2601c-504">Тип значения: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2601c-504">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="2601c-505">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-505">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="2601c-506">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-506">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2601c-507">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="2601c-507">ProxyServer</span></span>
#### <span data-ttu-id="2601c-508">Адрес или URL-адрес прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="2601c-508">Address or URL of proxy server</span></span>
><span data-ttu-id="2601c-509">Центр обновления Microsoft Edge 1.3.21.81 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-509">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="2601c-510">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-510">Description</span></span>
<span data-ttu-id="2601c-511">Позволяет указать URL-адрес прокси-сервера, который будет использовать Центр обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2601c-511">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="2601c-512">Если эта политика включена, вы можете задать URL-адрес прокси сервера, который будет использовать Центр обновления Microsoft Edge в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="2601c-512">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="2601c-513">Эта политика применяется только в том случае, если параметры прокси-сервера были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".</span><span class="sxs-lookup"><span data-stu-id="2601c-513">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="2601c-514">Не настраивайте эту политику, если параметры прокси-сервера не были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".</span><span class="sxs-lookup"><span data-stu-id="2601c-514">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="2601c-515">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-515">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-516">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-516">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-517">Уникальное имя групповой политики: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="2601c-517">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="2601c-518">Имя групповой политики: Адрес или URL-адрес прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="2601c-518">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="2601c-519">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="2601c-519">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="2601c-520">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-520">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-521">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-521">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-522">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-522">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-523">Имя значения: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="2601c-523">Value Name: ProxyServer</span></span>
- <span data-ttu-id="2601c-524">Тип значения: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2601c-524">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="2601c-525">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-525">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="2601c-526">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-526">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="2601c-527">Политики веб-представления Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2601c-527">Microsoft Edge WebView policies</span></span>

[<span data-ttu-id="2601c-528">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-528">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="2601c-529">Установка (веб-представление)</span><span class="sxs-lookup"><span data-stu-id="2601c-529">Install (WebView)</span></span>
#### <span data-ttu-id="2601c-530">Разрешить установку</span><span class="sxs-lookup"><span data-stu-id="2601c-530">Allow installation</span></span>
><span data-ttu-id="2601c-531">Центр обновления Microsoft Edge 1.3.127.1 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-531">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <span data-ttu-id="2601c-532">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-532">Description</span></span>
<span data-ttu-id="2601c-533">Позволяет указать, можно ли установить веб-представление Microsoft Edge с помощью Центра обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2601c-533">Lets you specify whether Microsoft Edge WebView can be installed using Microsoft Edge Update.</span></span>

  - <span data-ttu-id="2601c-534">Если эта политика включена, пользователи смогут установить веб-представление Microsoft Edge с помощью Центра обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2601c-534">If you enable this policy, users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="2601c-535">Если эта политика отключена, пользователи не смогут установить веб-представление Microsoft Edge с помощью Центра обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2601c-535">If you disable this policy, users cannot install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="2601c-536">Если эта политика не настроена, возможность установки пользователями веб-представления Microsoft Edge через Центр обновления Microsoft Edge будет определяться конфигурацией политики "[Разрешить установку по умолчанию](#installdefault)".</span><span class="sxs-lookup"><span data-stu-id="2601c-536">If you don't configure this policy, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
#### <span data-ttu-id="2601c-537">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-537">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-538">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-538">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-539">Уникальное имя групповой политики: Install</span><span class="sxs-lookup"><span data-stu-id="2601c-539">GP unique name: Install</span></span>
- <span data-ttu-id="2601c-540">Имя групповой политики: Разрешить установку по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2601c-540">GP name: Allow installation</span></span>
- <span data-ttu-id="2601c-541">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="2601c-541">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="2601c-542">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-542">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-543">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-543">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-544">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-544">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-545">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-545">Value Name:</span></span> 
  - <span data-ttu-id="2601c-546">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="2601c-546">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="2601c-547">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2601c-547">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2601c-548">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-548">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="2601c-549">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-549">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="2601c-550">Обновление (веб-представление)</span><span class="sxs-lookup"><span data-stu-id="2601c-550">Update (WebView)</span></span>
#### <span data-ttu-id="2601c-551">Переопределение политики обновления</span><span class="sxs-lookup"><span data-stu-id="2601c-551">Update policy override</span></span>
><span data-ttu-id="2601c-552">Центр обновления Microsoft Edge 1.3.127.1 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="2601c-552">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <span data-ttu-id="2601c-553">Описание</span><span class="sxs-lookup"><span data-stu-id="2601c-553">Description</span></span>
<span data-ttu-id="2601c-554">Позволяет указать, включено ли автоматическое обновление для веб-представления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2601c-554">Lets you specify whether or not automatic updates are enabled for Microsoft Edge WebView.</span></span> <span data-ttu-id="2601c-555">Веб-представление Microsoft Edge — это компонент, используемый приложениями для отображения веб-содержимого.</span><span class="sxs-lookup"><span data-stu-id="2601c-555">Microsoft Edge WebView is a component used by applications to display web content.</span></span>
<span data-ttu-id="2601c-556">Автоматическое обновление включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2601c-556">Automatic updates are enabled by default.</span></span> <span data-ttu-id="2601c-557">Отключение автоматического обновления веб-представления Microsoft Edge может привести к проблемам совместимости с приложениями, зависящими от этого компонента.</span><span class="sxs-lookup"><span data-stu-id="2601c-557">Disabling automatic updates for Microsoft Edge WebView might cause compatibility issues with applications that depend on this component.</span></span>

  <span data-ttu-id="2601c-558">Если эта политика включена, Центр обновления Microsoft Edge обрабатывает обновления веб-представления Microsoft Edge в соответствии со значениями следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="2601c-558">If you enable this policy, Microsoft Edge Update handles Microsoft Edge WebView updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="2601c-559">Всегда разрешать обновления. Обновления скачиваются и применяются автоматически</span><span class="sxs-lookup"><span data-stu-id="2601c-559">Always allow updates: Updates are automatically downloaded and applied</span></span>
  - <span data-ttu-id="2601c-560">Обновления отключены. Обновления никогда не скачиваются и не применяются</span><span class="sxs-lookup"><span data-stu-id="2601c-560">Updates disabled: Updates are never downloaded or applied</span></span>

  <span data-ttu-id="2601c-561">Если эта политика не включена, обновления скачиваются и применяются автоматически.</span><span class="sxs-lookup"><span data-stu-id="2601c-561">If you don't enable this policy, updates are automatically downloaded and applied.</span></span>
#### <span data-ttu-id="2601c-562">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-562">Windows information and settings</span></span>
##### <span data-ttu-id="2601c-563">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="2601c-563">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="2601c-564">Уникальное имя групповой политики: Update</span><span class="sxs-lookup"><span data-stu-id="2601c-564">GP unique name: Update</span></span>
- <span data-ttu-id="2601c-565">Имя групповой политики: Переопределение политики обновления</span><span class="sxs-lookup"><span data-stu-id="2601c-565">GP name: Update policy override</span></span>
- <span data-ttu-id="2601c-566">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="2601c-566">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="2601c-567">Имя ADMX-файла групповой политики: msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="2601c-567">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="2601c-568">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="2601c-568">Windows Registry Settings</span></span>
- <span data-ttu-id="2601c-569">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="2601c-569">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="2601c-570">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-570">Value Name:</span></span> 
  - <span data-ttu-id="2601c-571">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="2601c-571">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="2601c-572">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2601c-572">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="2601c-573">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="2601c-573">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="2601c-574">В начало</span><span class="sxs-lookup"><span data-stu-id="2601c-574">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="2601c-575">См. также</span><span class="sxs-lookup"><span data-stu-id="2601c-575">See also</span></span>
  - [<span data-ttu-id="2601c-576">Настройка Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2601c-576">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="2601c-577">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="2601c-577">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)