---
title: Перенаправление из Internet Explorer в Microsoft Edge для обеспечения совместимости с современными веб-сайтами
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 11/03/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Перенаправление из Internet Explorer в Microsoft Edge для обеспечения совместимости с современными веб-сайтами
ms.openlocfilehash: d822bf4cef76fe4c0298133b47ed80f5d1242b3d
ms.sourcegitcommit: 73fec3998f26d110252ace621be01f1c1142cf57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2020
ms.locfileid: "11151099"
---
# <span data-ttu-id="200aa-103">Перенаправление из Internet Explorer в Microsoft Edge для обеспечения совместимости с современными веб-сайтами</span><span class="sxs-lookup"><span data-stu-id="200aa-103">Redirection from Internet Explorer to Microsoft Edge for compatibility with modern web sites</span></span>

> [!NOTE]
> <span data-ttu-id="200aa-104">Эта статья относится к Microsoft Edge из стабильного канала версии 87 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="200aa-104">This article applies to Microsoft Edge Stable version 87 or later.</span></span>

## <span data-ttu-id="200aa-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="200aa-105">Overview</span></span>

<span data-ttu-id="200aa-106">Дизайн многих современных веб-сайтов несовместим с Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="200aa-106">Many modern websites have designs that are incompatible with Internet Explorer.</span></span> <span data-ttu-id="200aa-107">Когда пользователь Internet Explorer посещает несовместимый общедоступный сайт, для него отображается сообщение о том, что сайт несовместим с браузером и требуется вручную переключиться на другой браузер.</span><span class="sxs-lookup"><span data-stu-id="200aa-107">Whenever an Internet Explorer user visits an incompatible public site, they get a message that tells them the site is incompatible with their browser, and they need to manually switch to a different browser.</span></span>

<span data-ttu-id="200aa-108">Необходимость ручного переключения на другой браузер изменяется с Microsoft Edge стабильного канала версии 87.</span><span class="sxs-lookup"><span data-stu-id="200aa-108">The need to  manually switch to a different browser changes starting with Microsoft Edge Stable version 87.</span></span>

<span data-ttu-id="200aa-109">Когда пользователь переходит на сайт, несовместимый с Internet Explorer, он автоматически перенаправляется в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="200aa-109">When a user goes to a site that is incompatible with Internet Explorer, they will be automatically redirected to Microsoft Edge.</span></span> <span data-ttu-id="200aa-110">В этой статье описан пользовательский интерфейс перенаправления и групповые политики, которые используются для настройки или отключения автоматического перенаправления.</span><span class="sxs-lookup"><span data-stu-id="200aa-110">This article describes the user experience for redirection and the group policies that are used to configure or disable automatic redirection.</span></span>

> [!NOTE]
> <span data-ttu-id="200aa-111">Корпорация Майкрософт поддерживает список всех сайтов, о которых известно, что они несовместимы с Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="200aa-111">Microsoft maintains a list of all sites that are known to be incompatible with Internet Explorer.</span></span>

## <span data-ttu-id="200aa-112">Интерфейс перенаправления</span><span class="sxs-lookup"><span data-stu-id="200aa-112">Redirection experience</span></span>

<span data-ttu-id="200aa-113">При перенаправлении в Microsoft Edge пользователям однократно демонстрируется диалоговое окно, как на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="200aa-113">On redirection to Microsoft Edge, users are shown the one-time dialog in the next screenshot.</span></span> <span data-ttu-id="200aa-114">В этом диалоговом окне объясняется, почему выполняется перенаправление, и запрашивается согласие на копирование данных браузера и параметров из Internet Explorer в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="200aa-114">This dialog explains why they're getting redirected and prompts for consent to copy their browsing data and preferences from Internet Explorer to Microsoft Edge.</span></span> <span data-ttu-id="200aa-115">Будут импортированы следующие данные браузера: избранное, пароли, поисковые системы, открытые вкладки, журнал, параметры, файлы cookie и домашняя страница.</span><span class="sxs-lookup"><span data-stu-id="200aa-115">The following browsing data will be imported: Favorites, Passwords, Search engines, open tabs, History, settings, cookies, and the Home Page.</span></span>

![Уведомление браузера и запрос на импорт данных и настроек.](media/edge-learnmore-neededge/neededge-dialog1.png)

<span data-ttu-id="200aa-117">Даже если пользователь не предоставит согласие путем установки флажка "Всегда извлекать данные и параметры браузера из Internet Explorer", он может нажать  **Продолжить просмотр**  для продолжения сеанса.</span><span class="sxs-lookup"><span data-stu-id="200aa-117">Even if they don't give their consent by checking "Always bring over my browsing data and preferences from Internet Explorer", they can click **Continue browsing** to continue their session.</span></span>

<span data-ttu-id="200aa-118">В конце отображается баннер о несовместимости веб-сайта (показанный на следующем снимке экрана) под адресной строкой для каждого перенаправления.</span><span class="sxs-lookup"><span data-stu-id="200aa-118">Finally, a website incompatibility banner, shown in the next screenshot, appears below the address bar for every redirection.</span></span>

![Уведомление о современных сайтах и предложение установить Microsoft Edge в качестве браузера, используемого по умолчанию, или ознакомиться с Microsoft Edge.](media/edge-learnmore-neededge/neededge-banner.png)

<span data-ttu-id="200aa-120">Баннер о несовместимости веб-сайта:</span><span class="sxs-lookup"><span data-stu-id="200aa-120">The website incompatibility banner:</span></span>

- <span data-ttu-id="200aa-121">рекомендует пользователю переключиться на Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="200aa-121">encourages the user to switch to Microsoft Edge</span></span>
- <span data-ttu-id="200aa-122">предлагает сделать Microsoft Edge браузером, используемым по умолчанию</span><span class="sxs-lookup"><span data-stu-id="200aa-122">offers to make Microsoft Edge as the default browser</span></span>
- <span data-ttu-id="200aa-123">дает пользователю возможность исследовать Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="200aa-123">gives the user the option to explore Microsoft Edge</span></span>

<span data-ttu-id="200aa-124">При перенаправлении сайта из Internet Explorer в Microsoft Edge вкладка Internet Explorer, на которой началась загрузка сайта, закрывается, если для нее не предоставлено предварительное согласие.</span><span class="sxs-lookup"><span data-stu-id="200aa-124">When a site is redirected from Internet Explorer to Microsoft Edge, the Internet Explorer tab that started loading the site is closed if it had no prior content.</span></span> <span data-ttu-id="200aa-125">В противном случае представление активной вкладки переходит на страницу  [поддержки](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) Майкрософт, на которой объясняется, почему сайт перенаправлен в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="200aa-125">Otherwise, the active tab view goes to a  Microsoft [support](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) page that explains why the site was redirected to Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="200aa-126">После перенаправления пользователи могут вернуться к использованию Internet Explorer для сайтов, которых нет в списке несовместимых с Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="200aa-126">After a redirection users can go back to using Internet Explorer for sites that are not on the Internet Explorer incompatibility list.</span></span>  

## <span data-ttu-id="200aa-127">Политики для настройки перенаправления в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="200aa-127">Policies to configure redirection to Microsoft Edge</span></span>

> [!NOTE]
> <span data-ttu-id="200aa-128">Эти политики будут доступны в виде обновлений ADMX-файла к 26 октября 2020 г. и будут доступны в Intune к 9 ноября 2020 г.</span><span class="sxs-lookup"><span data-stu-id="200aa-128">These policies will be available as ADMX file updates by October 26, 2020 and will be available in Intune by November 9, 2020.</span></span>

<span data-ttu-id="200aa-129">Чтобы включить автоматическое перенаправление в Microsoft Edge, требуется настроить три групповых политики.</span><span class="sxs-lookup"><span data-stu-id="200aa-129">Three group policies must be configured to enable automatic redirection to Microsoft Edge.</span></span> <span data-ttu-id="200aa-130">Вот эти политики:</span><span class="sxs-lookup"><span data-stu-id="200aa-130">These policies are:</span></span>

- <span data-ttu-id="200aa-131">RedirectSitesFromInternetExplorerPreventBHOInstall</span><span class="sxs-lookup"><span data-stu-id="200aa-131">RedirectSitesFromInternetExplorerPreventBHOInstall</span></span>
- <span data-ttu-id="200aa-132">RedirectSitesFromInternetExplorerRedirectMode</span><span class="sxs-lookup"><span data-stu-id="200aa-132">RedirectSitesFromInternetExplorerRedirectMode</span></span>
- <span data-ttu-id="200aa-133">HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span><span class="sxs-lookup"><span data-stu-id="200aa-133">HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span></span>

### <span data-ttu-id="200aa-134">Политика: RedirectSitesFromInternetExplorerPreventBHOInstall</span><span class="sxs-lookup"><span data-stu-id="200aa-134">Policy: RedirectSitesFromInternetExplorerPreventBHOInstall</span></span>

<span data-ttu-id="200aa-135">Для перенаправления из Internet Explorer в Microsoft Edge требуется вспомогательный объект браузера (BHO) Internet Explorer с именем "IEtoEdge BHO".</span><span class="sxs-lookup"><span data-stu-id="200aa-135">Redirection from Internet Explorer to Microsoft Edge requires an Internet Explorer Browser Helper Object (BHO) named "IEtoEdge BHO".</span></span> <span data-ttu-id="200aa-136">Политика **RedirectSitesFromInternetExplorerPreventBHOInstall** определяет, устанавливается ли этот вспомогательный объект браузера.</span><span class="sxs-lookup"><span data-stu-id="200aa-136">The **RedirectSitesFromInternetExplorerPreventBHOInstall** policy controls whether or not this BHO is installed.</span></span>  

- <span data-ttu-id="200aa-137">Если эта политика включена, вспомогательный объект браузера, необходимый для перенаправления, не будет установлен, а для ваших пользователей по-прежнему будут отображаться сообщения о несовместимости для определенных веб-сайтов в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="200aa-137">If you enable this policy, the BHO required for redirection will not be installed and your users will continue to see incompatibility messages for certain websites on Internet Explorer.</span></span> <span data-ttu-id="200aa-138">Если вспомогательный объект браузера уже установлен, он будет удален при следующем обновлении стабильного канала Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="200aa-138">If the BHO is already installed, it will be uninstalled the next time the Microsoft Edge Stable channel is updated.</span></span>
- <span data-ttu-id="200aa-139">Если отключить или не настроить эту политику, вспомогательный объект браузера будет установлен.</span><span class="sxs-lookup"><span data-stu-id="200aa-139">If you disable or don't configure this policy, the BHO will be installed.</span></span> <span data-ttu-id="200aa-140">Такая реакция на события используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="200aa-140">This is the default behavior.</span></span>

<span data-ttu-id="200aa-141">Помимо необходимости во вспомогательном объекте браузера существует зависимость от параметра **RedirectSitesFromInternetExplorerRedirectMode**, которому требуется присвоить значение "Перенаправлять сайты на основе списка несовместимых сайтов" или "Не настроено".</span><span class="sxs-lookup"><span data-stu-id="200aa-141">In addition to needing the BHO, there is a dependency on the **RedirectSitesFromInternetExplorerRedirectMode**, which needs to be set to "Redirect sites based on the incompatible sites sitelist" or "Not Configured".</span></span>

### <span data-ttu-id="200aa-142">Политика: RedirectSitesFromInternetExplorerRedirectMode</span><span class="sxs-lookup"><span data-stu-id="200aa-142">Policy: RedirectSitesFromInternetExplorerRedirectMode</span></span>

 <span data-ttu-id="200aa-143">Эта политика соответствует параметру раздела **Браузер по умолчанию** в Microsoft Edge "Разрешить Internet Explorer открывать сайты в Microsoft Edge".</span><span class="sxs-lookup"><span data-stu-id="200aa-143">This policy corresponds to the Microsoft Edge **Default browser** setting "Let Internet Explorer open sites in Microsoft Edge".</span></span> <span data-ttu-id="200aa-144">Чтобы получить доступ к этому параметру, перейдите по URL-адресу *edge://settings/defaultbrowser*.</span><span class="sxs-lookup"><span data-stu-id="200aa-144">You can access this setting by going to the *edge://settings/defaultbrowser* URL.</span></span>  

- <span data-ttu-id="200aa-145">Если не настроить эту политику или присвоить ей значение Sitelist (Список сайтов), Internet Explorer будет перенаправлять несовместимые сайты в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="200aa-145">If you don't configure this policy or set it to "Sitelist", Internet Explorer will redirect incompatible sites to Microsoft Edge.</span></span> <span data-ttu-id="200aa-146">Такая реакция на события используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="200aa-146">This is the default behavior.</span></span>
- <span data-ttu-id="200aa-147">Чтобы отключить эту политику, выберите **Включено**, затем в раскрывающемся меню "Настройки: Перенаправление несовместимых сайтов из Internet Explorer в Microsoft Edge" выберите **Отключить**.</span><span class="sxs-lookup"><span data-stu-id="200aa-147">To disable this policy, select **Enabled** AND then in the dropdown under Options: Redirect incompatible sites from Internet Explorer to Microsoft Edge, select **Disable**.</span></span> <span data-ttu-id="200aa-148">В этом случае несовместимые сайты не перенаправляются в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="200aa-148">In this state, incompatible sites aren't redirected to Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="200aa-149">Если вы используете персональное устройство, не управляемое вашей организацией, в разделе **Обеспечение совместимости с Internet Explorer** вы увидите другой параметр с именем "Разрешить сайтам загрузку в режиме Internet Explorer".</span><span class="sxs-lookup"><span data-stu-id="200aa-149">If you're on a personal device that isn't  managed by your organization, you'll see another setting named "Allow sites to be loaded in Internet Explorer mode" under **Internet Explorer compatibility**.</span></span>
>
><span data-ttu-id="200aa-150">Если вы используете устройство, присоединенное к домену или зарегистрированное в службе управления мобильными устройствами (MDM), этот параметр не отображается.</span><span class="sxs-lookup"><span data-stu-id="200aa-150">If you're on a domain joined or Mobile Device Management (MDM) enrolled device, you won't see this option.</span></span>
>
> <span data-ttu-id="200aa-151">Если вместо этого вы хотите разрешить своим пользователям загружать сайты в режиме Internet Explorer, вы можете это сделать, настроив политику [Разрешить тестирование режима Internet Explorer](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing).</span><span class="sxs-lookup"><span data-stu-id="200aa-151">Instead, if you want to let your users load sites in Internet Explorer mode, you can do so by configuring the policy [Allow Internet Explorer mode testing](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing).</span></span>

### <span data-ttu-id="200aa-152">Политика: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span><span class="sxs-lookup"><span data-stu-id="200aa-152">Policy: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span></span>

<span data-ttu-id="200aa-153">Эта политика настраивает пользовательский интерфейс для перенаправления несовместимых сайтов в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="200aa-153">This policy configures the user experience for incompatible site redirection to Microsoft Edge.</span></span>  

- <span data-ttu-id="200aa-154">Если эта политика включена, пользователям никогда не демонстрируется диалоговое окно однократного перенаправления и баннер перенаправления.</span><span class="sxs-lookup"><span data-stu-id="200aa-154">If you enable this policy, users never see the one-time redirection dialog and the redirection banner.</span></span> <span data-ttu-id="200aa-155">Данные браузера и пользовательские параметры не импортируются.</span><span class="sxs-lookup"><span data-stu-id="200aa-155">No browser data or user preferences are imported.</span></span>
- <span data-ttu-id="200aa-156">Если отключить или не настроить эту политику, диалоговое окно перенаправления будет отображаться при первом перенаправлении, а сохраненный баннер перенаправления будет отображаться для сеансов, начинающихся с перенаправления.</span><span class="sxs-lookup"><span data-stu-id="200aa-156">If you disable or don't configure this policy, the redirection dialog will be shown on the first redirection and the persistent redirection banner will be shown for sessions that start with a redirection.</span></span>

  > [!NOTE]
  > <span data-ttu-id="200aa-157">Данные браузера пользователя будут импортироваться при каждом выполнении перенаправления для пользователя.</span><span class="sxs-lookup"><span data-stu-id="200aa-157">User browsing data will be imported every time a user encounters a new redirection.</span></span> <span data-ttu-id="200aa-158">Однако это происходит только в том случае, если пользователь согласился на импорт в диалоговом окне однократного перенаправления.</span><span class="sxs-lookup"><span data-stu-id="200aa-158">However, this only happens if the user consented to the import on the one-time redirection dialog.</span></span>

## <span data-ttu-id="200aa-159">Отключение перенаправления в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="200aa-159">Disable redirection to Microsoft Edge</span></span>

<span data-ttu-id="200aa-160">Если вы хотите отключить перенаправление ДО обновления до Microsoft Edge версии 87 из стабильного канала, выполните следующее действие.</span><span class="sxs-lookup"><span data-stu-id="200aa-160">If you want to disable redirection BEFORE updating to Microsoft Edge Stable version 87, use the following step:</span></span>

1. <span data-ttu-id="200aa-161">Присвойте политике **RedirectSitesFromInternetExplorerPreventBHOInstall** значение **Включено**.</span><span class="sxs-lookup"><span data-stu-id="200aa-161">Set the **RedirectSitesFromInternetExplorerPreventBHOInstall** policy to **Enabled**.</span></span>

<span data-ttu-id="200aa-162">Если вы хотите отключить перенаправление ПОСЛЕ обновления до Microsoft Edge версии 87 из стабильного канала, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="200aa-162">If you want to disable redirection AFTER updating to Microsoft Edge Stable version 87, use the following steps:</span></span>

1. <span data-ttu-id="200aa-163">Установите для политики **RedirectSitesFromInternetExplorerRedirectMode** значение **Включено**, затем в раскрывающемся меню "Настройки: Перенаправление несовместимых сайтов из Internet Explorer в Microsoft Edge" выберите **Отключить**.</span><span class="sxs-lookup"><span data-stu-id="200aa-163">Set the **RedirectSitesFromInternetExplorerRedirectMode** policy to **Enabled** AND then in the dropdown under Options: Redirect incompatible sites from Internet Explorer to Microsoft Edge, select **Disable**.</span></span> <span data-ttu-id="200aa-164">Этот параметр прекратит перенаправление, как только политика вступит в силу.</span><span class="sxs-lookup"><span data-stu-id="200aa-164">This setting will stop redirecting as soon as the policy takes effect.</span></span>
2. <span data-ttu-id="200aa-165">Присвойте политике **RedirectSitesFromInternetExplorerPreventBHOInstall** значение **Включено**.</span><span class="sxs-lookup"><span data-stu-id="200aa-165">Set the **RedirectSitesFromInternetExplorerPreventBHOInstall** policy to **Enabled**.</span></span> <span data-ttu-id="200aa-166">Это приведет к удалению вспомогательного объекта браузера после следующего обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="200aa-166">This will uninstall the BHO after the next Microsoft Edge update.</span></span>

## <span data-ttu-id="200aa-167">См. также</span><span class="sxs-lookup"><span data-stu-id="200aa-167">See also</span></span>

- [<span data-ttu-id="200aa-168">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="200aa-168">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="200aa-169">Политики Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="200aa-169">Microsoft Edge Policies</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies)
