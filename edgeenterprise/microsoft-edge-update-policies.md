---
title: Документация по политикам Центра обновления Microsoft Edge
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 06/10/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Документация по всем политикам, поддерживаемым средством обновления Microsoft Edge
ms.openlocfilehash: d772d8dd6f60b89e9bd12a77b740e5fad699756a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980932"
---
# <span data-ttu-id="7d1b5-103">Microsoft Edge — политики обновления</span><span class="sxs-lookup"><span data-stu-id="7d1b5-103">Microsoft Edge - Update policies</span></span>
<span data-ttu-id="7d1b5-104">Последняя версия Microsoft Edge включает в себя следующие политики, которые можно использовать для управления процессом и временем обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

           
<span data-ttu-id="7d1b5-105">Сведения о других политиках, доступных в Microsoft Edge, см. в [Справочнике по политикам браузера Microsoft Edge](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="7d1b5-106">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-106">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="7d1b5-107">Доступные политики</span><span class="sxs-lookup"><span data-stu-id="7d1b5-107">Available policies</span></span>
<span data-ttu-id="7d1b5-108">В этих таблицах указаны все групповые политики, связанные с обновлением, доступные в данном выпуске Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="7d1b5-109">Для получения дополнительных сведений о конкретных политиках см. ссылки в таблице.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-109">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="7d1b5-110">Приложения</span><span class="sxs-lookup"><span data-stu-id="7d1b5-110">Applications</span></span>](#applications)|[<span data-ttu-id="7d1b5-111">Предпочтения</span><span class="sxs-lookup"><span data-stu-id="7d1b5-111">Preferences</span></span>](#preferences)|
|[<span data-ttu-id="7d1b5-112">Прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="7d1b5-112">Proxy Server</span></span>](#proxy-server)||

### [<span data-ttu-id="7d1b5-113">Приложения</span><span class="sxs-lookup"><span data-stu-id="7d1b5-113">Applications</span></span>](#applications-policies)
|<span data-ttu-id="7d1b5-114">Имя политики</span><span class="sxs-lookup"><span data-stu-id="7d1b5-114">Policy Name</span></span>|<span data-ttu-id="7d1b5-115">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7d1b5-115">Caption</span></span>|
|-|-|
|[<span data-ttu-id="7d1b5-116">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="7d1b5-116">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="7d1b5-117">Разрешить установку по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7d1b5-117">Allow installation default</span></span>|
|[<span data-ttu-id="7d1b5-118">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="7d1b5-118">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="7d1b5-119">Переопределение политики обновления по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7d1b5-119">Update policy override default</span></span>|
|[<span data-ttu-id="7d1b5-120">Установка</span><span class="sxs-lookup"><span data-stu-id="7d1b5-120">Install</span></span>](#install)|<span data-ttu-id="7d1b5-121">Разрешить установку (для канала)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-121">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="7d1b5-122">Update</span><span class="sxs-lookup"><span data-stu-id="7d1b5-122">Update</span></span>](#update)|<span data-ttu-id="7d1b5-123">Переопределение политики обновления (для канала)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-123">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="7d1b5-124">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="7d1b5-124">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="7d1b5-125">Разрешить параллельный запуск разных типов браузеров Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7d1b5-125">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="7d1b5-126">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="7d1b5-126">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="7d1b5-127">Запрет создания ярлыка на рабочем столе при установке по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7d1b5-127">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="7d1b5-128">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="7d1b5-128">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="7d1b5-129">Запрет создания ярлыка на рабочем столе при установке (для каналов)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-129">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="7d1b5-130">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="7d1b5-130">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="7d1b5-131">Переопределение целевой версии (для каналов)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-131">Target version override (per channel)</span></span>|

### [<span data-ttu-id="7d1b5-132">Предпочтения</span><span class="sxs-lookup"><span data-stu-id="7d1b5-132">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="7d1b5-133">Имя политики</span><span class="sxs-lookup"><span data-stu-id="7d1b5-133">Policy Name</span></span>|<span data-ttu-id="7d1b5-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7d1b5-134">Caption</span></span>|
|-|-|
|[<span data-ttu-id="7d1b5-135">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="7d1b5-135">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="7d1b5-136">Переопределение периода автоматической проверки обновления</span><span class="sxs-lookup"><span data-stu-id="7d1b5-136">Auto-update check period override</span></span>|
|[<span data-ttu-id="7d1b5-137">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="7d1b5-137">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="7d1b5-138">Период времени в течение дня, когда будет блокироваться автоматическая проверка обновлений</span><span class="sxs-lookup"><span data-stu-id="7d1b5-138">Time period in each day to suppress auto-update check</span></span>|

### [<span data-ttu-id="7d1b5-139">Прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="7d1b5-139">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="7d1b5-140">Имя политики</span><span class="sxs-lookup"><span data-stu-id="7d1b5-140">Policy Name</span></span>|<span data-ttu-id="7d1b5-141">Действие</span><span class="sxs-lookup"><span data-stu-id="7d1b5-141">Caption</span></span>|
|-|-|
|[<span data-ttu-id="7d1b5-142">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="7d1b5-142">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="7d1b5-143">Выбор способа задания параметров прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="7d1b5-143">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="7d1b5-144">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="7d1b5-144">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="7d1b5-145">URL-адрес файла PAC прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="7d1b5-145">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="7d1b5-146">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="7d1b5-146">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="7d1b5-147">Адрес или URL-адрес прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="7d1b5-147">Address or URL of proxy server</span></span>|

                 
      
  
             
            
                  

## <span data-ttu-id="7d1b5-148">Политики приложений</span><span class="sxs-lookup"><span data-stu-id="7d1b5-148">Applications policies</span></span>

[<span data-ttu-id="7d1b5-149">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-149">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="7d1b5-150">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="7d1b5-150">InstallDefault</span></span>
#### <span data-ttu-id="7d1b5-151">Разрешить установку по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7d1b5-151">Allow installation default</span></span>
><span data-ttu-id="7d1b5-152">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="7d1b5-152">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="7d1b5-153">Описание</span><span class="sxs-lookup"><span data-stu-id="7d1b5-153">Description</span></span>
<span data-ttu-id="7d1b5-154">Вы можете указать поведение по умолчанию для всех каналов: разрешить или заблокировать обновления Microsoft Edge при использовании Центра обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-154">You can specify the default behavior of all channels to allow or block Microsoft Edge updates when Microsoft Edge Update is used.</span></span>

<span data-ttu-id="7d1b5-155">Вы можете переопределить эту политику для отдельных каналов, включив политику "[Разрешить установку](#install)" для конкретных каналов.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-155">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="7d1b5-156">Если эта политика отключена, установка Microsoft Edge через Центр обновления Microsoft Edge будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-156">If you disable this policy, the installation of Microsoft Edge through Microsoft Edge Update is blocked.</span></span> <span data-ttu-id="7d1b5-157">Это влияет на установку программного обеспечения Microsoft Edge только в том случае, если пользователи используют Центр обновления Microsoft Edge и политика "[Разрешить установку](#install)" не настроена.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-157">This only affects the installation of Microsoft Edge software only when users are running Microsoft Edge Update and when they haven't configured the '[Allow installation](#install)' policy.</span></span>

<span data-ttu-id="7d1b5-158">Эта политика не запрещает запуск Центра обновления Microsoft Edge и не запрещает пользователям устанавливать программное обеспечение Microsoft Edge другим способом.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-158">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>
#### <span data-ttu-id="7d1b5-159">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-159">Windows information and settings</span></span>
##### <span data-ttu-id="7d1b5-160">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-160">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="7d1b5-161">Уникальное имя групповой политики: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="7d1b5-161">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="7d1b5-162">Имя групповой политики: Разрешить установку по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7d1b5-162">GP name: Allow installation default</span></span>
- <span data-ttu-id="7d1b5-163">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="7d1b5-163">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="7d1b5-164">Имя ADMX-файла групповой политики: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="7d1b5-164">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="7d1b5-165">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-165">Windows Registry Settings</span></span>
- <span data-ttu-id="7d1b5-166">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="7d1b5-166">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="7d1b5-167">Имя значения: InstallDefault</span><span class="sxs-lookup"><span data-stu-id="7d1b5-167">Value Name: InstallDefault</span></span>
- <span data-ttu-id="7d1b5-168">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7d1b5-168">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="7d1b5-169">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-169">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="7d1b5-170">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-170">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="7d1b5-171">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="7d1b5-171">UpdateDefault</span></span>
#### <span data-ttu-id="7d1b5-172">Переопределение политики обновления по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7d1b5-172">Update policy override default</span></span>
><span data-ttu-id="7d1b5-173">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="7d1b5-173">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="7d1b5-174">Описание</span><span class="sxs-lookup"><span data-stu-id="7d1b5-174">Description</span></span>
<span data-ttu-id="7d1b5-175">Позволяет задать поведение по умолчанию для всех каналов в отношении обработки Центром обновления Microsoft Edge доступных обновлений для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-175">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="7d1b5-176">Можно переопределить для отдельных каналов, задав политику "[Переопределение политики обновления](#update)" для этих конкретных каналов.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-176">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="7d1b5-177">Если эта политика включена, Центр обновления Microsoft Edge обрабатывает обновления Microsoft Edge в соответствии со значениями следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-177">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="7d1b5-178">Всегда разрешать обновления: обновления всегда применяются при их обнаружении путем периодической автоматической или ручной проверки наличия обновлений.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-178">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="7d1b5-179">Только обновления, найденные автоматически: обновления применяются только в том случае, если они были найдены при периодической автоматической проверке наличия обновлений.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-179">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="7d1b5-180">Только обновления, найденные вручную: обновления применяются только в том случае, если пользователь запускает проверку наличия обновлений вручную.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-180">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="7d1b5-181">Обновления отключены: обновления никогда не применяются.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-181">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="7d1b5-182">При выборе параметра "Обновления, найденные вручную" периодически проверяйте наличие обновлений с помощью механизма приложения для поиска обновлений вручную, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-182">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="7d1b5-183">При отключении обновлений разрешите периодическую автоматическую проверку наличия обновлений и их распространение для пользователей.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-183">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="7d1b5-184">Если вы не включите и не настроите эту политику, Центр обновления Microsoft Edge будет обрабатывать доступные обновления в соответствии с политикой "[Переопределение политики обновления](#update)".</span><span class="sxs-lookup"><span data-stu-id="7d1b5-184">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>
#### <span data-ttu-id="7d1b5-185">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-185">Windows information and settings</span></span>
##### <span data-ttu-id="7d1b5-186">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-186">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="7d1b5-187">Уникальное имя групповой политики: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="7d1b5-187">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="7d1b5-188">Имя групповой политики: Переопределение политики обновления по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7d1b5-188">GP name: Update policy override default</span></span>
- <span data-ttu-id="7d1b5-189">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="7d1b5-189">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="7d1b5-190">Имя ADMX-файла групповой политики: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="7d1b5-190">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="7d1b5-191">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-191">Windows Registry Settings</span></span>
- <span data-ttu-id="7d1b5-192">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="7d1b5-192">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="7d1b5-193">Имя значения: UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="7d1b5-193">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="7d1b5-194">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7d1b5-194">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="7d1b5-195">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-195">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="7d1b5-196">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-196">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="7d1b5-197">Install</span><span class="sxs-lookup"><span data-stu-id="7d1b5-197">Install</span></span>
#### <span data-ttu-id="7d1b5-198">Разрешить установку</span><span class="sxs-lookup"><span data-stu-id="7d1b5-198">Allow installation</span></span>
><span data-ttu-id="7d1b5-199">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="7d1b5-199">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="7d1b5-200">Описание</span><span class="sxs-lookup"><span data-stu-id="7d1b5-200">Description</span></span>
<span data-ttu-id="7d1b5-201">Указывает, можно ли установить канал Microsoft Edge с помощью Центра обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-201">Specifies whether a Microsoft Edge channel can be installed using Microsoft Edge Update.</span></span>

  <span data-ttu-id="7d1b5-202">Если эта политика включена для канала, пользователи смогут установить этот канал Microsoft Edge с помощью Центра обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-202">If you enable this policy for a channel, users can install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>

  <span data-ttu-id="7d1b5-203">Если эта политика отключена для канала, пользователи не смогут установить этот канал Microsoft Edge с помощью Центра обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-203">If you disable this policy for a channel, users cannot install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>

  <span data-ttu-id="7d1b5-204">Если вы не настроите эту политику для канала, конфигурация политики "[Разрешить установку по умолчанию](#installdefault)" будет определять, смогут ли пользователи устанавливать этот канал Microsoft Edge через Центр обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-204">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>
#### <span data-ttu-id="7d1b5-205">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-205">Windows information and settings</span></span>
##### <span data-ttu-id="7d1b5-206">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-206">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="7d1b5-207">Уникальное имя групповой политики: Install</span><span class="sxs-lookup"><span data-stu-id="7d1b5-207">GP unique name: Install</span></span>
- <span data-ttu-id="7d1b5-208">Имя групповой политики: Разрешить установку по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7d1b5-208">GP name: Allow installation</span></span>
- <span data-ttu-id="7d1b5-209">Путь к групповой политике:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-209">GP path:</span></span> 
  - <span data-ttu-id="7d1b5-210">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7d1b5-210">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="7d1b5-211">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="7d1b5-211">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="7d1b5-212">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="7d1b5-212">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="7d1b5-213">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="7d1b5-213">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="7d1b5-214">Имя ADMX-файла групповой политики: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="7d1b5-214">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="7d1b5-215">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-215">Windows Registry Settings</span></span>
- <span data-ttu-id="7d1b5-216">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="7d1b5-216">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="7d1b5-217">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-217">Value Name:</span></span> 
  - <span data-ttu-id="7d1b5-218">(Канал Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-218">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="7d1b5-219">(Канал Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-219">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="7d1b5-220">(Канал Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-220">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="7d1b5-221">Канал (Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-221">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="7d1b5-222">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7d1b5-222">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="7d1b5-223">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-223">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="7d1b5-224">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-224">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="7d1b5-225">Update</span><span class="sxs-lookup"><span data-stu-id="7d1b5-225">Update</span></span>
#### <span data-ttu-id="7d1b5-226">Переопределение политики обновления</span><span class="sxs-lookup"><span data-stu-id="7d1b5-226">Update policy override</span></span>
><span data-ttu-id="7d1b5-227">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="7d1b5-227">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="7d1b5-228">Описание</span><span class="sxs-lookup"><span data-stu-id="7d1b5-228">Description</span></span>
<span data-ttu-id="7d1b5-229">Указывает, как Центр обновления Microsoft Edge обрабатывает доступные обновления для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-229">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

  <span data-ttu-id="7d1b5-230">Если эта политика включена, Центр обновления Microsoft Edge обрабатывает обновления Microsoft Edge в соответствии со значениями следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-230">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="7d1b5-231">Всегда разрешать обновления: обновления всегда применяются при их обнаружении путем периодической автоматической или ручной проверки наличия обновлений.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-231">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="7d1b5-232">Только обновления, найденные автоматически: обновления применяются только в том случае, если они были найдены при периодической автоматической проверке наличия обновлений.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-232">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="7d1b5-233">Только обновления, найденные вручную: обновления применяются только в том случае, если пользователь запускает проверку наличия обновлений вручную.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-233">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="7d1b5-234">(Не все приложения предоставляют интерфейс для этого варианта.)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-234">(Not all apps provide an interface for this option.)</span></span>
   - <span data-ttu-id="7d1b5-235">Обновления отключены: обновления никогда не применяются.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-235">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="7d1b5-236">При выборе параметра "Обновления, найденные вручную" периодически проверяйте наличие обновлений с помощью механизма приложения для поиска обновлений вручную, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-236">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="7d1b5-237">При отключении обновлений разрешите периодическую автоматическую проверку наличия обновлений и их распространение для пользователей.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-237">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="7d1b5-238">Если вы не включите и не настроите эту политику, Центр обновления Microsoft Edge будет обрабатывать доступные обновления в соответствии с политикой "[Переопределение политики обновления по умолчанию](#updatedefault)".</span><span class="sxs-lookup"><span data-stu-id="7d1b5-238">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>
#### <span data-ttu-id="7d1b5-239">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-239">Windows information and settings</span></span>
##### <span data-ttu-id="7d1b5-240">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-240">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="7d1b5-241">Уникальное имя групповой политики: Update</span><span class="sxs-lookup"><span data-stu-id="7d1b5-241">GP unique name: Update</span></span>
- <span data-ttu-id="7d1b5-242">Имя групповой политики: Переопределение политики обновления</span><span class="sxs-lookup"><span data-stu-id="7d1b5-242">GP name: Update policy override</span></span>
- <span data-ttu-id="7d1b5-243">Путь к групповой политике:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-243">GP path:</span></span> 
  - <span data-ttu-id="7d1b5-244">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7d1b5-244">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="7d1b5-245">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="7d1b5-245">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="7d1b5-246">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="7d1b5-246">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="7d1b5-247">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="7d1b5-247">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="7d1b5-248">Имя ADMX-файла групповой политики: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="7d1b5-248">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="7d1b5-249">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-249">Windows Registry Settings</span></span>
- <span data-ttu-id="7d1b5-250">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="7d1b5-250">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="7d1b5-251">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-251">Value Name:</span></span> 
  - <span data-ttu-id="7d1b5-252">(Канал Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-252">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="7d1b5-253">(Канал Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-253">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="7d1b5-254">(Канал Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-254">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="7d1b5-255">Канал (Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-255">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="7d1b5-256">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7d1b5-256">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="7d1b5-257">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-257">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="7d1b5-258">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-258">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="7d1b5-259">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="7d1b5-259">Allowsxs</span></span>
#### <span data-ttu-id="7d1b5-260">Разрешить параллельный запуск разных типов браузеров Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7d1b5-260">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="7d1b5-261">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="7d1b5-261">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="7d1b5-262">Описание</span><span class="sxs-lookup"><span data-stu-id="7d1b5-262">Description</span></span>
<span data-ttu-id="7d1b5-263">Эта политика позволяет пользователю параллельно запускать Microsoft Edge (Edge HTML) и Microsoft Edge (на основе Chromium).</span><span class="sxs-lookup"><span data-stu-id="7d1b5-263">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="7d1b5-264">Если для этой политики задано значение "Не настроено", браузер Microsoft Edge (на основе Chromium) заменит Microsoft Edge (Edge HTML) после установки Microsoft Edge (на основе Chromium) в рамках канала Stable, а также обновлений для системы безопасности за ноябрь 2019 года.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-264">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="7d1b5-265">Поведение параметра "Отключено" такое же.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-265">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="7d1b5-266">Если параметр "Отключено" блокирует параллельный запуск, браузер Microsoft Edge (на основе Chromium) заменит Microsoft Edge (Edge HTML) после установки Microsoft Edge (на основе Chromium) в рамках канала Stable, а также обновлений для системы безопасности за ноябрь 2019 года.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-266">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="7d1b5-267">Поведение параметра "Не настроено" такое же.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-267">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="7d1b5-268">Если эта политика "Включена", браузер Microsoft Edge (на основе Chromium) и браузер Microsoft Edge (HTML Edge) смогут выполняться параллельно после установки Microsoft Edge (на основе Chromium).</span><span class="sxs-lookup"><span data-stu-id="7d1b5-268">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="7d1b5-269">Чтобы эта групповая политика вступила в силу, ее необходимо настроить до выполнения автоматической установки Microsoft Edge (на основе Chromium) с помощью Центра обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-269">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="7d1b5-270">Примечание. Пользователь может заблокировать автоматическое обновление Microsoft Edge (на основе Chromium) с помощью набора средств блокировки Microsoft Edge (на основе Chromium).</span><span class="sxs-lookup"><span data-stu-id="7d1b5-270">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <span data-ttu-id="7d1b5-271">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-271">Windows information and settings</span></span>
##### <span data-ttu-id="7d1b5-272">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-272">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="7d1b5-273">Уникальное имя групповой политики: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="7d1b5-273">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="7d1b5-274">Имя групповой политики: Разрешить параллельный запуск разных типов браузеров Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7d1b5-274">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="7d1b5-275">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="7d1b5-275">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="7d1b5-276">Имя ADMX-файла групповой политики: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="7d1b5-276">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="7d1b5-277">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-277">Windows Registry Settings</span></span>
- <span data-ttu-id="7d1b5-278">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="7d1b5-278">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="7d1b5-279">Имя значения: Allowsxs</span><span class="sxs-lookup"><span data-stu-id="7d1b5-279">Value Name: Allowsxs</span></span>
- <span data-ttu-id="7d1b5-280">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7d1b5-280">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="7d1b5-281">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-281">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="7d1b5-282">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-282">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="7d1b5-283">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="7d1b5-283">CreateDesktopShortcutDefault</span></span>
#### <span data-ttu-id="7d1b5-284">Запрет создания ярлыка на рабочем столе при установке по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7d1b5-284">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="7d1b5-285">Центр обновления Microsoft Edge 1.3.128.0 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="7d1b5-285">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="7d1b5-286">Описание</span><span class="sxs-lookup"><span data-stu-id="7d1b5-286">Description</span></span>
<span data-ttu-id="7d1b5-287">Позволяет указать поведение по умолчанию для всех каналов в отношении создания ярлыка на рабочем столе при установке Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-287">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="7d1b5-288">Если эта политика включена, при установке Microsoft Edge создается ярлык на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-288">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="7d1b5-289">Если эта политика отключена, при установке Microsoft Edge ярлык на рабочем столе не создается.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-289">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="7d1b5-290">Если вы не настроите эту политику, при установке будет создан ярлык Microsoft Edge на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-290">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="7d1b5-291">Если Microsoft Edge уже установлен, эта политика не действует.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-291">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <span data-ttu-id="7d1b5-292">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-292">Windows information and settings</span></span>
##### <span data-ttu-id="7d1b5-293">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-293">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="7d1b5-294">Уникальное имя групповой политики: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="7d1b5-294">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="7d1b5-295">Имя групповой политики: Запрет создания ярлыка на рабочем столе при установке по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7d1b5-295">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="7d1b5-296">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications</span><span class="sxs-lookup"><span data-stu-id="7d1b5-296">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="7d1b5-297">Имя ADMX-файла групповой политики: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="7d1b5-297">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="7d1b5-298">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-298">Windows Registry Settings</span></span>
- <span data-ttu-id="7d1b5-299">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="7d1b5-299">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="7d1b5-300">Имя значения: CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="7d1b5-300">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="7d1b5-301">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7d1b5-301">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="7d1b5-302">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-302">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="7d1b5-303">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-303">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="7d1b5-304">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="7d1b5-304">CreateDesktopShortcut</span></span>
#### <span data-ttu-id="7d1b5-305">Запрет создания ярлыка на рабочем столе при установке</span><span class="sxs-lookup"><span data-stu-id="7d1b5-305">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="7d1b5-306">Центр обновления Microsoft Edge 1.3.128.0 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="7d1b5-306">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="7d1b5-307">Описание</span><span class="sxs-lookup"><span data-stu-id="7d1b5-307">Description</span></span>
<span data-ttu-id="7d1b5-308">Если эта политика включена, при установке Microsoft Edge создается ярлык на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-308">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="7d1b5-309">Если эта политика отключена, при установке Microsoft Edge ярлык на рабочем столе не создается.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-309">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="7d1b5-310">Если вы не настроите эту политику, при установке будет создан ярлык Microsoft Edge на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-310">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="7d1b5-311">Если Microsoft Edge уже установлен, эта политика не действует.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-311">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="7d1b5-312">Если не настроить эту политику для канала, создание ярлыка при установке Microsoft Edge определяется конфигурацией политики "[Запрет создания ярлыка на рабочем столе при установке по умолчанию](#createdesktopshortcutdefault)".</span><span class="sxs-lookup"><span data-stu-id="7d1b5-312">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <span data-ttu-id="7d1b5-313">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-313">Windows information and settings</span></span>
##### <span data-ttu-id="7d1b5-314">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-314">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="7d1b5-315">Уникальное имя групповой политики: CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="7d1b5-315">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="7d1b5-316">Имя групповой политики: Запрет создания ярлыка на рабочем столе при установке</span><span class="sxs-lookup"><span data-stu-id="7d1b5-316">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="7d1b5-317">Путь к групповой политике:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-317">GP path:</span></span> 
  - <span data-ttu-id="7d1b5-318">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7d1b5-318">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="7d1b5-319">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="7d1b5-319">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="7d1b5-320">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="7d1b5-320">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="7d1b5-321">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="7d1b5-321">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="7d1b5-322">Имя ADMX-файла групповой политики: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="7d1b5-322">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="7d1b5-323">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-323">Windows Registry Settings</span></span>
- <span data-ttu-id="7d1b5-324">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="7d1b5-324">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="7d1b5-325">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-325">Value Name:</span></span> 
  - <span data-ttu-id="7d1b5-326">(Канал Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-326">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="7d1b5-327">(Канал Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-327">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="7d1b5-328">(Канал Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-328">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="7d1b5-329">(Канал Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-329">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="7d1b5-330">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7d1b5-330">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="7d1b5-331">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-331">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="7d1b5-332">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-332">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="7d1b5-333">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="7d1b5-333">TargetVersionPrefix</span></span>
#### <span data-ttu-id="7d1b5-334">Переопределение целевой версии</span><span class="sxs-lookup"><span data-stu-id="7d1b5-334">Target version override</span></span>
><span data-ttu-id="7d1b5-335">Центр обновления Microsoft Edge 1.3.119.43 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="7d1b5-335">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <span data-ttu-id="7d1b5-336">Описание</span><span class="sxs-lookup"><span data-stu-id="7d1b5-336">Description</span></span>
<span data-ttu-id="7d1b5-337">Если эта политика включена и включено автоматическое обновление, Microsoft Edge обновляется до версии, указанной значением этой политики.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-337">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="7d1b5-338">В качестве значения политики требуется использовать определенную версию Microsoft Edge, например 83.0.499.12.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-338">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="7d1b5-339">Если на устройстве установлена более поздняя версия Microsoft Edge, чем указано в значении, Microsoft Edge сохранит новую версию и не будет понижен до указанной версии.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-339">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="7d1b5-340">Если указанная версия не существует или имеет неправильный формат, Microsoft Edge сохранит текущую версию и не будет автоматически обновляться до будущих версий.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-340">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>
#### <span data-ttu-id="7d1b5-341">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-341">Windows information and settings</span></span>
##### <span data-ttu-id="7d1b5-342">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-342">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="7d1b5-343">Уникальное имя групповой политики: TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="7d1b5-343">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="7d1b5-344">Имя групповой политики: Переопределение целевой версии</span><span class="sxs-lookup"><span data-stu-id="7d1b5-344">GP name: Target version override</span></span>
- <span data-ttu-id="7d1b5-345">Путь к групповой политике:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-345">GP path:</span></span> 
  - <span data-ttu-id="7d1b5-346">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7d1b5-346">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="7d1b5-347">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="7d1b5-347">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="7d1b5-348">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="7d1b5-348">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="7d1b5-349">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="7d1b5-349">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="7d1b5-350">Имя ADMX-файла групповой политики: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="7d1b5-350">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="7d1b5-351">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-351">Windows Registry Settings</span></span>
- <span data-ttu-id="7d1b5-352">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="7d1b5-352">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="7d1b5-353">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-353">Value Name:</span></span> 
  - <span data-ttu-id="7d1b5-354">(Канал Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-354">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="7d1b5-355">(Канал Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-355">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="7d1b5-356">(Канал Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-356">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="7d1b5-357">(Канал Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="7d1b5-357">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="7d1b5-358">Тип значения: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="7d1b5-358">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="7d1b5-359">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-359">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="7d1b5-360">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-360">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="7d1b5-361">Предпочтительные политики</span><span class="sxs-lookup"><span data-stu-id="7d1b5-361">Preferences policies</span></span>

[<span data-ttu-id="7d1b5-362">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-362">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="7d1b5-363">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="7d1b5-363">AutoUpdateCheckPeriodMinutes</span></span>
#### <span data-ttu-id="7d1b5-364">Переопределение периода автоматической проверки обновлений</span><span class="sxs-lookup"><span data-stu-id="7d1b5-364">Auto-update check period override</span></span>
><span data-ttu-id="7d1b5-365">Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="7d1b5-365">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="7d1b5-366">Описание</span><span class="sxs-lookup"><span data-stu-id="7d1b5-366">Description</span></span>
<span data-ttu-id="7d1b5-367">Если политика включена, вы можете задать минимальное количество минут между автоматическими проверками обновлений.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-367">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="7d1b5-368">В противном случае по умолчанию автоматическая проверка наличия обновлений будет выполняться каждые 10 часов.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-368">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="7d1b5-369">Если необходимо отключить все автоматические проверки обновлений, задайте значение равным 0 (не рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="7d1b5-369">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <span data-ttu-id="7d1b5-370">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-370">Windows information and settings</span></span>
##### <span data-ttu-id="7d1b5-371">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-371">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="7d1b5-372">Уникальное имя групповой политики: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="7d1b5-372">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="7d1b5-373">Имя групповой политики: Переопределение периода автоматической проверки обновления</span><span class="sxs-lookup"><span data-stu-id="7d1b5-373">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="7d1b5-374">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Preferences</span><span class="sxs-lookup"><span data-stu-id="7d1b5-374">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="7d1b5-375">Имя ADMX-файла групповой политики: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="7d1b5-375">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="7d1b5-376">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-376">Windows Registry Settings</span></span>
- <span data-ttu-id="7d1b5-377">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="7d1b5-377">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="7d1b5-378">Имя значения: AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="7d1b5-378">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="7d1b5-379">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7d1b5-379">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="7d1b5-380">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-380">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="7d1b5-381">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-381">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="7d1b5-382">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="7d1b5-382">UpdatesSuppressed</span></span>
#### <span data-ttu-id="7d1b5-383">Период времени в течение дня, когда будет блокироваться автоматическая проверка обновлений</span><span class="sxs-lookup"><span data-stu-id="7d1b5-383">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="7d1b5-384">Центр обновления Microsoft Edge 1.3.33.5 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="7d1b5-384">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <span data-ttu-id="7d1b5-385">Описание</span><span class="sxs-lookup"><span data-stu-id="7d1b5-385">Description</span></span>
<span data-ttu-id="7d1b5-386">Если эта политика включена, проверки обновлений блокируются каждый день, начиная с Hour:Minute в течение заданного периода времени (в минутах).</span><span class="sxs-lookup"><span data-stu-id="7d1b5-386">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="7d1b5-387">На этот период не влияет переход на летнее время.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-387">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="7d1b5-388">Например, если время начала равно 22:00, а длительность составляет 480минут, обновления будут блокироваться в течение 8 часов, независимо от этапа перехода на летнее время, то есть его начала или завершения.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-388">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="7d1b5-389">Если эта политика отключена или не настроена, проверки обновлений не блокируются в течение заданного периода.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-389">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <span data-ttu-id="7d1b5-390">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-390">Windows information and settings</span></span>
##### <span data-ttu-id="7d1b5-391">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-391">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="7d1b5-392">Уникальное имя групповой политики: UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="7d1b5-392">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="7d1b5-393">Имя групповой политики: Период времени в течение дня, когда будет блокироваться автоматическая проверка обновлений</span><span class="sxs-lookup"><span data-stu-id="7d1b5-393">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="7d1b5-394">Параметры {Hour, Minute, Duration} (Час, Минута, Длительность)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-394">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="7d1b5-395">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Preferences</span><span class="sxs-lookup"><span data-stu-id="7d1b5-395">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="7d1b5-396">Имя ADMX-файла групповой политики: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="7d1b5-396">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="7d1b5-397">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-397">Windows Registry Settings</span></span>
- <span data-ttu-id="7d1b5-398">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="7d1b5-398">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="7d1b5-399">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-399">Value Name:</span></span> 
  - <span data-ttu-id="7d1b5-400">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="7d1b5-400">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="7d1b5-401">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="7d1b5-401">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="7d1b5-402">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="7d1b5-402">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="7d1b5-403">Тип значения: REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7d1b5-403">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="7d1b5-404">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-404">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="7d1b5-405">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-405">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="7d1b5-406">Политики прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="7d1b5-406">Proxy Server policies</span></span>
  
  

[<span data-ttu-id="7d1b5-407">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-407">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="7d1b5-408">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="7d1b5-408">ProxyMode</span></span>
#### <span data-ttu-id="7d1b5-409">Выбор способа задания параметров прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="7d1b5-409">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="7d1b5-410">Центр обновления Microsoft Edge 1.3.21.81 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="7d1b5-410">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="7d1b5-411">Описание</span><span class="sxs-lookup"><span data-stu-id="7d1b5-411">Description</span></span>
<span data-ttu-id="7d1b5-412">Позволяет указать параметры прокси-сервера, используемые Центром обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-412">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="7d1b5-413">Если эта политика включена, можно выбрать один из следующих параметров прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-413">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="7d1b5-414">Если вы решите никогда не использовать прокси-сервер и всегда подключаться напрямую, все остальные параметры будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-414">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="7d1b5-415">Если вы решите использовать системные параметры прокси-сервера или включите автоматическое определение прокси-сервера, все остальные параметры будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-415">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="7d1b5-416">При выборе режима фиксированного прокси-сервера можно указать дополнительные параметры в политике "[Адрес или URL-адрес прокси-сервера](#proxyserver)".</span><span class="sxs-lookup"><span data-stu-id="7d1b5-416">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="7d1b5-417">Если вы решите использовать сценарий прокси-сервера PAC, необходимо указать URL-адрес сценария в политике "[URL-адрес файла PAC прокси-сервера](#proxypacurl)".</span><span class="sxs-lookup"><span data-stu-id="7d1b5-417">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="7d1b5-418">Если эта политика включена, пользователи в вашей организации не смогут изменять параметры прокси-сервера в Центре обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-418">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="7d1b5-419">Если эта политика отключена или не настроена, параметры прокси-сервера не будут заданы, но пользователи в вашей организации смогут задать собственные параметры прокси-сервера для Центра обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-419">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <span data-ttu-id="7d1b5-420">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-420">Windows information and settings</span></span>
##### <span data-ttu-id="7d1b5-421">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-421">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="7d1b5-422">Уникальное имя групповой политики: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="7d1b5-422">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="7d1b5-423">Имя групповой политики: Выбор способа задания параметров прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="7d1b5-423">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="7d1b5-424">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="7d1b5-424">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="7d1b5-425">Имя ADMX-файла групповой политики: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="7d1b5-425">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="7d1b5-426">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-426">Windows Registry Settings</span></span>
- <span data-ttu-id="7d1b5-427">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="7d1b5-427">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="7d1b5-428">Имя значения: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="7d1b5-428">Value Name: ProxyMode</span></span>
- <span data-ttu-id="7d1b5-429">Тип значения: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="7d1b5-429">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="7d1b5-430">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-430">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="7d1b5-431">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-431">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="7d1b5-432">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="7d1b5-432">ProxyPacUrl</span></span>
#### <span data-ttu-id="7d1b5-433">URL-адрес файла PAC прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="7d1b5-433">URL to a proxy .pac file</span></span>
><span data-ttu-id="7d1b5-434">Центр обновления Microsoft Edge 1.3.21.81 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="7d1b5-434">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="7d1b5-435">Описание</span><span class="sxs-lookup"><span data-stu-id="7d1b5-435">Description</span></span>
<span data-ttu-id="7d1b5-436">Позволяет указать URL-адрес к файлу автоматической настройки прокси-сервера (PAC).</span><span class="sxs-lookup"><span data-stu-id="7d1b5-436">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="7d1b5-437">Если эта политика включена, вы можете указать URL-адрес для файла PAC, чтобы автоматизировать процесс выбора подходящего прокси-сервера Центром обновления Microsoft Edge для загрузки конкретного веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-437">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="7d1b5-438">Эта политика применяется только в том случае, если параметры прокси-сервера были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".</span><span class="sxs-lookup"><span data-stu-id="7d1b5-438">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="7d1b5-439">Не настраивайте эту политику, если параметры прокси-сервера не были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".</span><span class="sxs-lookup"><span data-stu-id="7d1b5-439">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="7d1b5-440">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-440">Windows information and settings</span></span>
##### <span data-ttu-id="7d1b5-441">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-441">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="7d1b5-442">Уникальное имя групповой политики: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="7d1b5-442">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="7d1b5-443">Имя групповой политики: URL-адрес файла PAC прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="7d1b5-443">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="7d1b5-444">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="7d1b5-444">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="7d1b5-445">Имя ADMX-файла групповой политики: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="7d1b5-445">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="7d1b5-446">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-446">Windows Registry Settings</span></span>
- <span data-ttu-id="7d1b5-447">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="7d1b5-447">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="7d1b5-448">Имя значения: ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="7d1b5-448">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="7d1b5-449">Тип значения: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="7d1b5-449">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="7d1b5-450">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-450">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="7d1b5-451">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-451">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="7d1b5-452">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="7d1b5-452">ProxyServer</span></span>
#### <span data-ttu-id="7d1b5-453">Адрес или URL-адрес прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="7d1b5-453">Address or URL of proxy server</span></span>
><span data-ttu-id="7d1b5-454">Центр обновления Microsoft Edge 1.3.21.81 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="7d1b5-454">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="7d1b5-455">Описание</span><span class="sxs-lookup"><span data-stu-id="7d1b5-455">Description</span></span>
<span data-ttu-id="7d1b5-456">Позволяет указать URL-адрес прокси-сервера, который будет использовать Центр обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-456">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="7d1b5-457">Если эта политика включена, вы можете задать URL-адрес прокси сервера, который будет использовать Центр обновления Microsoft Edge в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="7d1b5-457">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="7d1b5-458">Эта политика применяется только в том случае, если параметры прокси-сервера были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".</span><span class="sxs-lookup"><span data-stu-id="7d1b5-458">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="7d1b5-459">Не настраивайте эту политику, если параметры прокси-сервера не были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".</span><span class="sxs-lookup"><span data-stu-id="7d1b5-459">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="7d1b5-460">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-460">Windows information and settings</span></span>
##### <span data-ttu-id="7d1b5-461">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="7d1b5-461">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="7d1b5-462">Уникальное имя групповой политики: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="7d1b5-462">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="7d1b5-463">Имя групповой политики: Адрес или URL-адрес прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="7d1b5-463">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="7d1b5-464">Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Proxy Server</span><span class="sxs-lookup"><span data-stu-id="7d1b5-464">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="7d1b5-465">Имя ADMX-файла групповой политики: edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="7d1b5-465">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="7d1b5-466">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="7d1b5-466">Windows Registry Settings</span></span>
- <span data-ttu-id="7d1b5-467">Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="7d1b5-467">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="7d1b5-468">Имя значения: ProxyServer</span><span class="sxs-lookup"><span data-stu-id="7d1b5-468">Value Name: ProxyServer</span></span>
- <span data-ttu-id="7d1b5-469">Тип значения: REG_SZ</span><span class="sxs-lookup"><span data-stu-id="7d1b5-469">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="7d1b5-470">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="7d1b5-470">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="7d1b5-471">В начало</span><span class="sxs-lookup"><span data-stu-id="7d1b5-471">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="7d1b5-472">См. также</span><span class="sxs-lookup"><span data-stu-id="7d1b5-472">See also</span></span>
  - [<span data-ttu-id="7d1b5-473">Настройка Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7d1b5-473">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="7d1b5-474">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="7d1b5-474">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
