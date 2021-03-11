---
title: Отключение Internet Explorer 11
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Узнайте, как отключить Internet Explorer 11 и использовать режим Internet Explorer в Microsoft Edge.
ms.openlocfilehash: a0486c2965b1868db67b6de1423f279905074410
ms.sourcegitcommit: f34ff11499a2b96941e704103bdd959d19e3d7e7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "11400609"
---
# <a name="disable-internet-explorer-11"></a><span data-ttu-id="4da29-103">Отключение Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="4da29-103">Disable Internet Explorer 11</span></span>

<span data-ttu-id="4da29-104">В этой статье описано, как отключить Internet Explorer 11 в качестве автономного браузера в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="4da29-104">This article describes how to disable Internet Explorer 11 as a standalone browser in your environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4da29-105">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="4da29-105">Prerequisites</span></span>

<span data-ttu-id="4da29-106">Требуются следующие обновления Windows и программное обеспечение Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="4da29-106">The following Windows updates and Microsoft Edge software are required:</span></span>

- <span data-ttu-id="4da29-107">Обновления Windows</span><span class="sxs-lookup"><span data-stu-id="4da29-107">Windows updates</span></span>

  - <span data-ttu-id="4da29-108">Windows 10 версии 2004, Windows Server версии 2004, Windows 10 версии 20H2: обновление [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) или более позднее</span><span class="sxs-lookup"><span data-stu-id="4da29-108">Windows 10, version 2004, Windows Server version 2004, Windows 10, version 20H2: [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) or later</span></span>
  - <span data-ttu-id="4da29-109">Windows 10 версии 1909, Windows Server версии 1909: обновление [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) или более позднее</span><span class="sxs-lookup"><span data-stu-id="4da29-109">Windows 10 version 1909, Windows Server version 1909: [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) or later</span></span>
  - <span data-ttu-id="4da29-110">Windows 10 версии 1809, Windows Server версии 1809 и Windows Server 2019: обновление [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) или более позднее</span><span class="sxs-lookup"><span data-stu-id="4da29-110">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019: [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) or later</span></span>
  - <span data-ttu-id="4da29-111">Windows 10 версии 1607, Windows Server 2016: обновление [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) или более позднее</span><span class="sxs-lookup"><span data-stu-id="4da29-111">Windows 10, version 1607, Windows Server 2016: [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) or later</span></span>
   - <span data-ttu-id="4da29-112">Начальная версия Windows 10 (июль 2015 г.): обновление [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) или более позднее</span><span class="sxs-lookup"><span data-stu-id="4da29-112">Windows 10 initial version (July 2015): [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) or later</span></span>
  - <span data-ttu-id="4da29-113">Windows 8.1: обновление [KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) или более позднее</span><span class="sxs-lookup"><span data-stu-id="4da29-113">Windows 8.1: [KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) or later</span></span>
  - <span data-ttu-id="4da29-114">Windows Server 2012: обновление [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) или более позднее</span><span class="sxs-lookup"><span data-stu-id="4da29-114">Windows Server 2012: [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) or later</span></span>
  
- <span data-ttu-id="4da29-115">Стабильный канал Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4da29-115">Microsoft Edge Stable Channel</span></span>


## <a name="overview"></a><span data-ttu-id="4da29-116">Обзор</span><span class="sxs-lookup"><span data-stu-id="4da29-116">Overview</span></span>

<span data-ttu-id="4da29-117">Организациям, которым требуется Internet Explorer 11 (IE11) для обеспечения совместимости с устаревшими программами, режим Internet Explorer (режим IE) в Microsoft Edge обеспечивает удобный интерфейс в одном браузере.</span><span class="sxs-lookup"><span data-stu-id="4da29-117">For organizations that require Internet Explorer 11 (IE11) for legacy compatibility, Internet Explorer mode (IE mode) on Microsoft Edge provides a seamless, single browser experience.</span></span> <span data-ttu-id="4da29-118">Пользователи могут получать доступ к устаревшим приложениям из Microsoft Edge, не возвращаясь к IE11.</span><span class="sxs-lookup"><span data-stu-id="4da29-118">Users can access legacy applications from within Microsoft Edge without having to switch back to IE11.</span></span>

<span data-ttu-id="4da29-119">После настройки режима IE вы можете отключить IE11 в качестве автономного браузера, **не затрагивая функции режима IE** в организации, с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="4da29-119">After you configure IE mode, you can disable IE11 as a standalone browser **without affecting IE mode functionality** across your organization using group policy.</span></span>

> [!NOTE]
> <span data-ttu-id="4da29-120">Если вам нужно отдельное приложение IE11 для определенных сайтов и вы хотите перенаправлять весь трафик браузера в Microsoft Edge, вы можете настроить политику [Отправлять все сайты, которые не включены в список сайтов, в Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge), чтобы перенаправлять сайты из IE в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4da29-120">If you need the standalone IE11 app for specific sites, and want to redirect all other browser traffic to Microsoft Edge, you can configure the [Send all sites not included in the site list to Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge) policy to redirect sites from IE to Microsoft Edge.</span></span>

## <a name="user-experience-after-redirecting-traffic-to-microsoft-edge"></a><span data-ttu-id="4da29-121">Взаимодействие с пользователем после перенаправления трафика в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4da29-121">User experience after redirecting traffic to Microsoft Edge</span></span>

<span data-ttu-id="4da29-122">Если включить политику **Отключить Internet Explorer 11 в качестве автономного браузера**, действия IE11 перенаправляются в Microsoft Edge и пользователям предлагается следующее взаимодействие:</span><span class="sxs-lookup"><span data-stu-id="4da29-122">When you enable the **Disable Internet Explorer 11 as a standalone browser** policy, all IE11 activity is redirected to Microsoft Edge and users have the following experience:</span></span>

- <span data-ttu-id="4da29-123">Значок IE11 в меню "Пуск" будет удален, но останется значок на панели задач.</span><span class="sxs-lookup"><span data-stu-id="4da29-123">The IE11 icon on the Start Menu will be removed, but the one on the taskbar will remain.</span></span>
- <span data-ttu-id="4da29-124">При попытке запуска ярлыков или сопоставлений файлов, применяющих IE11, пользователи будут перенаправлены в Microsoft Edge для открытия этого файла или URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="4da29-124">When users try to launch shortcuts or file associations that use IE11, they will be redirected to open the same file/URL in Microsoft Edge.</span></span>
- <span data-ttu-id="4da29-125">Если пользователи попытаются запустить IE11, непосредственно вызвав двоичный файл iexplore.exe, вместо этого запустится Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4da29-125">When users try to launch IE11 by directly invoking the iexplore.exe binary, Microsoft Edge will launch instead.</span></span>

<span data-ttu-id="4da29-126">В рамках настройки политики для этого интерфейса вы можете дополнительно отображать сообщение о перенаправлении для каждого пользователя, который пытается запустить IE11.</span><span class="sxs-lookup"><span data-stu-id="4da29-126">As part of setting the policy for this experience, you can optionally show a redirect message for each user who tries to launch IE11.</span></span> <span data-ttu-id="4da29-127">Для этого сообщения можно настроить следующие варианты отображения: "Всегда" или "Однократно для пользователя".</span><span class="sxs-lookup"><span data-stu-id="4da29-127">This message can be set to display "Always" or "Once per user".</span></span> <span data-ttu-id="4da29-128">По умолчанию сообщение о перенаправлении, показанное на следующем снимке экрана, никогда не отображается.</span><span class="sxs-lookup"><span data-stu-id="4da29-128">By default, the redirect message shown in the next screenshot is never shown.</span></span>

:::image type="content" source="media/edge-ie-disable-ie11/disable-ie-redirect-msg.png" alt-text="Оповещение при попытке открыть IE после активации перенаправления в Microsoft Edge.":::

<span data-ttu-id="4da29-130">Если список сайтов в режиме предприятия содержит приложения, настроенные для открытия в приложении IE11, и вы отключили IE11 с помощью этой политики, они будут открываться в режиме IE в браузере Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4da29-130">If your Enterprise Mode Site List contains applications that are configured to open in the IE11 app and you disable IE11 with this policy, they will open in IE mode on Microsoft Edge.</span></span>
> [!NOTE]
> <span data-ttu-id="4da29-131">Существует известная проблема с пользовательским потоком, если сайт настроен на открытие в IE11 и задана политика отключения IE11.</span><span class="sxs-lookup"><span data-stu-id="4da29-131">There is a known issue with the user flow when a site is configured to open in IE11 and the disable IE11 policy is set.</span></span> <span data-ttu-id="4da29-132">Эта проблема активно исследуется.</span><span class="sxs-lookup"><span data-stu-id="4da29-132">The issue being actively investigated.</span></span>

## <a name="disable-internet-explorer-11-as-a-standalone-browser"></a><span data-ttu-id="4da29-133">Отключение Internet Explorer 11 в качестве автономного браузера</span><span class="sxs-lookup"><span data-stu-id="4da29-133">Disable Internet Explorer 11 as a standalone browser</span></span>

<span data-ttu-id="4da29-134">Чтобы отключить Internet Explorer 11 с помощью групповой политики, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4da29-134">To disable Internet Explorer 11 using group policy, follow these steps:</span></span>

1. <span data-ttu-id="4da29-135">Убедитесь, что у вас есть необходимые обновления операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4da29-135">Ensure you have the pre-requisite operating system updates.</span></span> <span data-ttu-id="4da29-136">На этом шаге будут обновляться файлы ADMX непосредственно на компьютере (в частности inetres.adml и inetres.admx).</span><span class="sxs-lookup"><span data-stu-id="4da29-136">This step will update the ADMX files on your machine directly (specifically inetres.adml and inetres.admx).</span></span> <span data-ttu-id="4da29-137">Обратите внимание, что для обновления центрального хранилища нужно скопировать файлы ADML и ADMX на компьютере с необходимыми обновлениями.</span><span class="sxs-lookup"><span data-stu-id="4da29-137">Please note that if you want to update your Central Store, you will need to copy over the .adml and .admx files from a machine that has the pre-requisite updates.</span></span> <span data-ttu-id="4da29-138">Дополнительные сведения см. в статье [Создание центрального хранилища и управление им](https://docs.microsoft.com/troubleshoot/windows-client/group-policy/create-and-manage-central-store)</span><span class="sxs-lookup"><span data-stu-id="4da29-138">For more information, see [Create and manage Central Store](https://docs.microsoft.com/troubleshoot/windows-client/group-policy/create-and-manage-central-store)</span></span>
2. <span data-ttu-id="4da29-139">Откройте редактор групповых политик.</span><span class="sxs-lookup"><span data-stu-id="4da29-139">Open the Group Policy Editor.</span></span>
3. <span data-ttu-id="4da29-140">Выберите ***Конфигурация компьютера/Административные шаблоны/Компоненты Windows/Internet Explorer***.</span><span class="sxs-lookup"><span data-stu-id="4da29-140">Go to ***Computer Configuration/Administrative Templates/Windows Components/Internet Explorer***.</span></span> 
4. <span data-ttu-id="4da29-141">Дважды щелкните  **Отключить Internet Explorer 11 в качестве автономного браузера**.</span><span class="sxs-lookup"><span data-stu-id="4da29-141">Double-click **Disable Internet Explorer 11 as a standalone browser**.</span></span>
5. <span data-ttu-id="4da29-142">Выберите  **Включено**.</span><span class="sxs-lookup"><span data-stu-id="4da29-142">Select **Enabled**.</span></span>
6. <span data-ttu-id="4da29-143">В разделе  **Параметры** выберите одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4da29-143">Under **Options**, pick one of the following values:</span></span>

   - <span data-ttu-id="4da29-144">**Никогда**,  если вы не хотите уведомлять пользователей об отключении IE11.</span><span class="sxs-lookup"><span data-stu-id="4da29-144">**Never** if you don’t want to notify users that IE11 is disabled.</span></span>
   - <span data-ttu-id="4da29-145">**Всегда**,  если вы хотите уведомлять пользователей при каждом перенаправлении из IE11.</span><span class="sxs-lookup"><span data-stu-id="4da29-145">**Always** if you want to notify users every time they're redirected from IE11.</span></span>
   - <span data-ttu-id="4da29-146">**Однократно для пользователя**,  если вы хотите уведомлять пользователей только при первом перенаправлении.</span><span class="sxs-lookup"><span data-stu-id="4da29-146">**Once per user** if you want to notify users only the first time they are redirected.</span></span>

7. <span data-ttu-id="4da29-147">Нажмите  **ОК**  или  **Применить**  для сохранения этого параметра политики.</span><span class="sxs-lookup"><span data-stu-id="4da29-147">Click **OK** or **Apply** to save this policy setting.</span></span>

## <a name="see-also"></a><span data-ttu-id="4da29-148">См. также</span><span class="sxs-lookup"><span data-stu-id="4da29-148">See also</span></span>

- [<span data-ttu-id="4da29-149">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="4da29-149">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="4da29-150">Сведения о режиме IE</span><span class="sxs-lookup"><span data-stu-id="4da29-150">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="4da29-151">Дополнительные сведения о режиме предприятия</span><span class="sxs-lookup"><span data-stu-id="4da29-151">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
