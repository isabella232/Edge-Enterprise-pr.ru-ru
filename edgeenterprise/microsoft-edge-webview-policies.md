---
title: Документация по политикам Microsoft Edge WebView2
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 10/27/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Документация Windows и Mac для всех политик, поддерживаемых браузером Microsoft Edge
ms.openlocfilehash: 3ca9adb18ef41581bb016451015cf0aca0aa63c9
ms.sourcegitcommit: 91abbcdd4918065d4ec1151587fc1fa92486dbf3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "11136218"
---
# <span data-ttu-id="0427b-103">Политики Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="0427b-103">Microsoft Edge WebView2 - Policies</span></span>

<span data-ttu-id="0427b-104">Последняя версия Microsoft Edge WebView2 включает в себя следующие политики.</span><span class="sxs-lookup"><span data-stu-id="0427b-104">The latest version of Microsoft Edge WebView2 includes the following policies.</span></span> <span data-ttu-id="0427b-105">Эти политики можно использовать для настройки работы Microsoft Edge WebView2 в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="0427b-105">You can use these policies to configure how Microsoft Edge WebView2 runs in your organization.</span></span>

<span data-ttu-id="0427b-106">Информацию о дополнительном наборе политик, используемых для управления тем, как и когда обновляется Microsoft Edge WebView2, можно найти в [справочнике по политике обновления Microsoft Edge](microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="0427b-106">For information about an additional set of policies used to control how and when Microsoft Edge WebView2 is updated, check out [Microsoft Edge update policy reference](microsoft-edge-update-policies.md).</span></span>


> [!NOTE]
> <span data-ttu-id="0427b-107">Эта статья относится к Microsoft Edge версии 87 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="0427b-107">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="0427b-108">Доступные политики</span><span class="sxs-lookup"><span data-stu-id="0427b-108">Available policies</span></span>

<span data-ttu-id="0427b-109">В этих таблицах перечислены все групповые политики, доступные в этом выпуске Microsoft Edge WebView2.</span><span class="sxs-lookup"><span data-stu-id="0427b-109">These tables list all of the group policies available in this release of Microsoft Edge WebView2.</span></span> <span data-ttu-id="0427b-110">Для получения дополнительных сведений о конкретных политиках см. ссылки в таблице.</span><span class="sxs-lookup"><span data-stu-id="0427b-110">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="0427b-111">Параметры переопределения загрузчика</span><span class="sxs-lookup"><span data-stu-id="0427b-111">Loader Override Settings</span></span>](#loader-override-settings)|

### [*<span data-ttu-id="0427b-112">Параметры переопределения загрузчика</span><span class="sxs-lookup"><span data-stu-id="0427b-112">Loader Override Settings</span></span>*](#loader-override-settings-policies)

|<span data-ttu-id="0427b-113">Имя политики</span><span class="sxs-lookup"><span data-stu-id="0427b-113">Policy Name</span></span>|<span data-ttu-id="0427b-114">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0427b-114">Caption</span></span>|
|-|-|
|[<span data-ttu-id="0427b-115">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="0427b-115">BrowserExecutableFolder</span></span>](#browserexecutablefolder)|<span data-ttu-id="0427b-116">Настройка расположения папки исполняемого файла браузера</span><span class="sxs-lookup"><span data-stu-id="0427b-116">Configure the location of the browser executable folder</span></span>|
|[<span data-ttu-id="0427b-117">ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="0427b-117">ReleaseChannelPreference</span></span>](#releasechannelpreference)|<span data-ttu-id="0427b-118">Настройка предпочитаемого порядка поиска каналов выпуска</span><span class="sxs-lookup"><span data-stu-id="0427b-118">Set the release channel search order preference</span></span>|




  ## <span data-ttu-id="0427b-119">Политики "Параметры переопределения загрузчика"</span><span class="sxs-lookup"><span data-stu-id="0427b-119">Loader Override Settings policies</span></span>

  [<span data-ttu-id="0427b-120">В начало</span><span class="sxs-lookup"><span data-stu-id="0427b-120">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <span data-ttu-id="0427b-121">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="0427b-121">BrowserExecutableFolder</span></span>

  #### <span data-ttu-id="0427b-122">Настройка расположения папки исполняемого файла браузера</span><span class="sxs-lookup"><span data-stu-id="0427b-122">Configure the location of the browser executable folder</span></span>

  
  
  #### <span data-ttu-id="0427b-123">Поддерживаемые версии:</span><span class="sxs-lookup"><span data-stu-id="0427b-123">Supported versions:</span></span>

  - <span data-ttu-id="0427b-124">В Windows 87 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="0427b-124">On Windows since 87 or later</span></span>

  #### <span data-ttu-id="0427b-125">Описание</span><span class="sxs-lookup"><span data-stu-id="0427b-125">Description</span></span>

  <span data-ttu-id="0427b-126">Эта политика настраивает приложения WebView2, чтобы использовать среду выполнения WebView2 по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="0427b-126">This policy configures WebView2 applications to use the WebView2 Runtime in the specified path.</span></span> <span data-ttu-id="0427b-127">Папка должна содержать следующие файлы: msedgewebview2.exe, msedge.dll и т. д.</span><span class="sxs-lookup"><span data-stu-id="0427b-127">The folder should contain the following files: msedgewebview2.exe, msedge.dll, and so on.</span></span>

<span data-ttu-id="0427b-128">Чтобы задать значение для пути к папке, предоставьте имя и пару значения.</span><span class="sxs-lookup"><span data-stu-id="0427b-128">To set the value for the folder path, provide a Value name and Value pair.</span></span> <span data-ttu-id="0427b-129">Задайте имя значения для идентификатора пользовательской модели приложения или имя исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="0427b-129">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="0427b-130">Вы можете использовать подстановочный знак "\*" в качестве имени значения для применения ко всем приложениям.</span><span class="sxs-lookup"><span data-stu-id="0427b-130">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <span data-ttu-id="0427b-131">Поддерживаемые функции:</span><span class="sxs-lookup"><span data-stu-id="0427b-131">Supported features:</span></span>

  - <span data-ttu-id="0427b-132">Может быть обязательным: Да</span><span class="sxs-lookup"><span data-stu-id="0427b-132">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="0427b-133">Может быть рекомендовано: Нет</span><span class="sxs-lookup"><span data-stu-id="0427b-133">Can be recommended: No</span></span>
  - <span data-ttu-id="0427b-134">Обновление динамической политики: Да</span><span class="sxs-lookup"><span data-stu-id="0427b-134">Dynamic Policy Refresh: Yes</span></span>

  #### <span data-ttu-id="0427b-135">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0427b-135">Data Type:</span></span>

  - <span data-ttu-id="0427b-136">Список строк</span><span class="sxs-lookup"><span data-stu-id="0427b-136">List of strings</span></span>

  #### <span data-ttu-id="0427b-137">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="0427b-137">Windows information and settings</span></span>

  ##### <span data-ttu-id="0427b-138">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="0427b-138">Group Policy (ADMX) info</span></span>

  - <span data-ttu-id="0427b-139">Уникальное имя групповой политики: BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="0427b-139">GP unique name: BrowserExecutableFolder</span></span>
  - <span data-ttu-id="0427b-140">Имя групповой политики: Настройка расположения папки исполняемого файла браузера</span><span class="sxs-lookup"><span data-stu-id="0427b-140">GP name: Configure the location of the browser executable folder</span></span>
  - <span data-ttu-id="0427b-141">Путь к групповой политике (обязательно): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span><span class="sxs-lookup"><span data-stu-id="0427b-141">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="0427b-142">Путь GP (рекомендуется): N/A</span><span class="sxs-lookup"><span data-stu-id="0427b-142">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="0427b-143">Имя ADMX-файла групповой политики: MSEdgeWebView2.admx</span><span class="sxs-lookup"><span data-stu-id="0427b-143">GP ADMX file name: MSEdgeWebView2.admx</span></span>

  ##### <span data-ttu-id="0427b-144">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="0427b-144">Windows Registry Settings</span></span>

  - <span data-ttu-id="0427b-145">Путь (обязательно): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="0427b-145">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder</span></span>
  - <span data-ttu-id="0427b-146">Путь (рекомендуется): N/A</span><span class="sxs-lookup"><span data-stu-id="0427b-146">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="0427b-147">Имя значения: список REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0427b-147">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="0427b-148">Тип значения: список REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0427b-148">Value Type: list of REG_SZ</span></span>

  ##### <span data-ttu-id="0427b-149">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="0427b-149">Example value:</span></span>

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [<span data-ttu-id="0427b-150">В начало</span><span class="sxs-lookup"><span data-stu-id="0427b-150">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <span data-ttu-id="0427b-151">ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="0427b-151">ReleaseChannelPreference</span></span>

  #### <span data-ttu-id="0427b-152">Настройка предпочитаемого порядка поиска каналов выпуска</span><span class="sxs-lookup"><span data-stu-id="0427b-152">Set the release channel search order preference</span></span>

  
  
  #### <span data-ttu-id="0427b-153">Поддерживаемые версии:</span><span class="sxs-lookup"><span data-stu-id="0427b-153">Supported versions:</span></span>

  - <span data-ttu-id="0427b-154">В Windows 87 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="0427b-154">On Windows since 87 or later</span></span>

  #### <span data-ttu-id="0427b-155">Описание</span><span class="sxs-lookup"><span data-stu-id="0427b-155">Description</span></span>

  <span data-ttu-id="0427b-156">Порядок поиска каналов по умолчанию — среда выполнения WebView2, Beta, Dev и Canary.</span><span class="sxs-lookup"><span data-stu-id="0427b-156">The default channel search order is WebView2 Runtime, Beta, Dev, and Canary.</span></span>

<span data-ttu-id="0427b-157">Чтобы установить обратный порядок поиска по умолчанию, задайте для этой политики значение 1.</span><span class="sxs-lookup"><span data-stu-id="0427b-157">To reverse the default search order, set this policy to 1.</span></span>

<span data-ttu-id="0427b-158">Чтобы задать значение для предпочитаемого канала выпуска, предоставьте имя и пару значения.</span><span class="sxs-lookup"><span data-stu-id="0427b-158">To set the value for the release channel preference, provide a Value name and Value pair.</span></span> <span data-ttu-id="0427b-159">Задайте имя значения для идентификатора пользовательской модели приложения или имя исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="0427b-159">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="0427b-160">Вы можете использовать подстановочный знак "\*" в качестве имени значения для применения ко всем приложениям.</span><span class="sxs-lookup"><span data-stu-id="0427b-160">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <span data-ttu-id="0427b-161">Поддерживаемые функции:</span><span class="sxs-lookup"><span data-stu-id="0427b-161">Supported features:</span></span>

  - <span data-ttu-id="0427b-162">Может быть обязательным: Да</span><span class="sxs-lookup"><span data-stu-id="0427b-162">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="0427b-163">Может быть рекомендовано: Нет</span><span class="sxs-lookup"><span data-stu-id="0427b-163">Can be recommended: No</span></span>
  - <span data-ttu-id="0427b-164">Обновление динамической политики: Да</span><span class="sxs-lookup"><span data-stu-id="0427b-164">Dynamic Policy Refresh: Yes</span></span>

  #### <span data-ttu-id="0427b-165">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0427b-165">Data Type:</span></span>

  - <span data-ttu-id="0427b-166">Список строк</span><span class="sxs-lookup"><span data-stu-id="0427b-166">List of strings</span></span>

  #### <span data-ttu-id="0427b-167">Сведения и параметры Windows</span><span class="sxs-lookup"><span data-stu-id="0427b-167">Windows information and settings</span></span>

  ##### <span data-ttu-id="0427b-168">Сведения о групповой политике (ADMX)</span><span class="sxs-lookup"><span data-stu-id="0427b-168">Group Policy (ADMX) info</span></span>

  - <span data-ttu-id="0427b-169">Уникальное имя групповой политики: ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="0427b-169">GP unique name: ReleaseChannelPreference</span></span>
  - <span data-ttu-id="0427b-170">Имя групповой политики: Настройка предпочитаемого порядка поиска каналов выпуска</span><span class="sxs-lookup"><span data-stu-id="0427b-170">GP name: Set the release channel search order preference</span></span>
  - <span data-ttu-id="0427b-171">Путь к групповой политике (обязательно): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span><span class="sxs-lookup"><span data-stu-id="0427b-171">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="0427b-172">Путь GP (рекомендуется): N/A</span><span class="sxs-lookup"><span data-stu-id="0427b-172">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="0427b-173">Имя ADMX-файла групповой политики: MSEdgeWebView2.admx</span><span class="sxs-lookup"><span data-stu-id="0427b-173">GP ADMX file name: MSEdgeWebView2.admx</span></span>

  ##### <span data-ttu-id="0427b-174">Параметры реестра Windows</span><span class="sxs-lookup"><span data-stu-id="0427b-174">Windows Registry Settings</span></span>

  - <span data-ttu-id="0427b-175">Путь (обязательно): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="0427b-175">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference</span></span>
  - <span data-ttu-id="0427b-176">Путь (рекомендуется): N/A</span><span class="sxs-lookup"><span data-stu-id="0427b-176">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="0427b-177">Имя значения: список REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0427b-177">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="0427b-178">Тип значения: список REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0427b-178">Value Type: list of REG_SZ</span></span>

  ##### <span data-ttu-id="0427b-179">Пример значения:</span><span class="sxs-lookup"><span data-stu-id="0427b-179">Example value:</span></span>

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference = "Name: *, Value: 1"

```

  

  [<span data-ttu-id="0427b-180">В начало</span><span class="sxs-lookup"><span data-stu-id="0427b-180">Back to top</span></span>](#microsoft-edge-webview2---policies)


## <span data-ttu-id="0427b-181">См. также</span><span class="sxs-lookup"><span data-stu-id="0427b-181">See also</span></span>

- [<span data-ttu-id="0427b-182">Настройка Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0427b-182">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="0427b-183">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="0427b-183">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="0427b-184">Блог базовых параметров безопасности Майкрософт</span><span class="sxs-lookup"><span data-stu-id="0427b-184">Microsoft Security Baselines Blog</span></span>](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)