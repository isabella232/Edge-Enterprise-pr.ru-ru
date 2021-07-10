---
title: Edge для инфраструктуры виртуальных рабочих столов
ms.author: anlake
author: AndreaLBarr
manager: collw
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge для инфраструктуры виртуальных рабочих столов.
ms.openlocfilehash: 5dc234b0e6fbba4778f8236399a0ff438f704578
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641855"
---
# <a name="microsoft-edge-for-virtualized-desktop-infrastructure"></a><span data-ttu-id="bf795-103">Microsoft Edge для инфраструктуры виртуальных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="bf795-103">Microsoft Edge for Virtualized Desktop Infrastructure</span></span>

<span data-ttu-id="bf795-104">В этой статье описываются требования и ограничения, относящиеся к использованию Microsoft Edge в виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="bf795-104">This article describes the requirements and limitations for using Microsoft Edge in a virtualized environment.</span></span>

## <a name="what-is-vdi"></a><span data-ttu-id="bf795-105">Что такое VDI?</span><span class="sxs-lookup"><span data-stu-id="bf795-105">What is VDI?</span></span>

<span data-ttu-id="bf795-106">Инфраструктура виртуальных рабочих столов (VDI) — это технология виртуализации, размещающая операционную систему и приложения компьютера на централизованном сервере в центре обработки данных.</span><span class="sxs-lookup"><span data-stu-id="bf795-106">Virtual Desktop Infrastructure (VDI) is virtualization technology that hosts a desktop operating system and applications on a centralized server in a data center.</span></span> <span data-ttu-id="bf795-107">Это позволяет обеспечить пользователям полностью персонализированный интерфейс рабочего стола с полностью защищенным и соответствующим требованиям централизованным источником.</span><span class="sxs-lookup"><span data-stu-id="bf795-107">This enables a fully personalized desktop experience for users with a fully secured and compliant centralized source.</span></span>

<span data-ttu-id="bf795-108">Microsoft Edge можно использовать в такой виртуальной среде практически так же, как и на локальном устройстве, при этом он будет работать в безопасной и управляемой серверной среде.</span><span class="sxs-lookup"><span data-stu-id="bf795-108">Microsoft Edge can be used in such a virtualized environment in much the same ways as it can be used on the local device, all the while running from secure and controlled server environment.</span></span> <span data-ttu-id="bf795-109">В зависимости от выбранного вами решения VDI можно также предоставить вашим пользователям беспрепятственный доступ к приложениям и сайтам интрасети.</span><span class="sxs-lookup"><span data-stu-id="bf795-109">Depending on your chosen VDI solution it may also be possible to give your users seamless access to intranet Applications and Sites.</span></span>

<span data-ttu-id="bf795-110">Большинство функций Edge поддерживаются в средах VDI без какой-либо особой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bf795-110">Most features of Edge are supported on VDI environments without any special configuration.</span></span> <span data-ttu-id="bf795-111">Однако для обеспечения оптимальной работы рекомендуется следовать приведенной ниже инструкции.</span><span class="sxs-lookup"><span data-stu-id="bf795-111">However, to ensure an optimal experience it’s recommended to follow the guidance below.</span></span>

## <a name="platforms-certified-for-edge"></a><span data-ttu-id="bf795-112">Платформы, сертифицированные для Edge</span><span class="sxs-lookup"><span data-stu-id="bf795-112">Platforms certified for Edge</span></span>

- <span data-ttu-id="bf795-113">Виртуальный рабочий стол Azure</span><span class="sxs-lookup"><span data-stu-id="bf795-113">Azure Virtual Desktop</span></span>
- <span data-ttu-id="bf795-114">Виртуальные приложения и рабочие столы Citrix (ранее известные как XenApp и XenDesktop)</span><span class="sxs-lookup"><span data-stu-id="bf795-114">Citrix Virtual Apps and Desktops (formerly known as XenApp and XenDesktop)</span></span>

<span data-ttu-id="bf795-115">Хотя другие решения VDI еще не проверены командой Edge, ожидается, что наиболее распространенные рабочие процессы в Edge должны поддерживаться.</span><span class="sxs-lookup"><span data-stu-id="bf795-115">While other VDI solutions have not yet been verified by the Edge team, it is expected that the most common workflows in Edge should be supported.</span></span> <span data-ttu-id="bf795-116">Руководство, приведенное ниже, может как соответствовать, так и не соответствовать выбранному вами решению.</span><span class="sxs-lookup"><span data-stu-id="bf795-116">Guidance provided below may or may not be applicable to your chosen solution.</span></span>

## <a name="edge-on-vdi-performance-considerations"></a><span data-ttu-id="bf795-117">Вопросы производительности Edge в VDI</span><span class="sxs-lookup"><span data-stu-id="bf795-117">Edge on VDI performance considerations</span></span>

<span data-ttu-id="bf795-118">При создании среды VDI для достижения оптимальной производительности вам необходимо внимательно учитывать рабочие процессы и потребности своих пользователей, а также ограничения, связанные с конфигурацией сервера.</span><span class="sxs-lookup"><span data-stu-id="bf795-118">When designing your VDI environment you should carefully consider the workflows and needs of your users to achieve optimal performance, as well as the limits of your server configuration.</span></span>

<span data-ttu-id="bf795-119">Edge рекомендует следующие минимальные требования к развертыванию Edge в средах VDI:</span><span class="sxs-lookup"><span data-stu-id="bf795-119">Edge recommends the following minimal requirements for deploying Edge to VDI environments:</span></span>

- <span data-ttu-id="bf795-120">vCPU — 2–4 ядра на пользователя</span><span class="sxs-lookup"><span data-stu-id="bf795-120">vCPU – 2-4 Cores per User</span></span>
- <span data-ttu-id="bf795-121">ОЗУ — 1 ГБ на пользователя</span><span class="sxs-lookup"><span data-stu-id="bf795-121">RAM – 1 GB per User</span></span>

<span data-ttu-id="bf795-122">Обратите внимание: для больших сложных веб-приложений и расширений потребуется больше памяти, и это необходимо учитывать в конфигурации среды.</span><span class="sxs-lookup"><span data-stu-id="bf795-122">Please note that large complex web applications and extensions will require more memory and will have to be accounted for when configuring your environment.</span></span>

## <a name="edge-on-non-persisted-vdi-environments"></a><span data-ttu-id="bf795-123">Edge для несохраняемой среды VDI</span><span class="sxs-lookup"><span data-stu-id="bf795-123">Edge on non-persisted VDI environments</span></span>

<span data-ttu-id="bf795-124">Многие решения VDI позволяют получать доступ к сохраняемой среде, где пользователям назначается виртуальная среда, которая сохраняется между сеансами, и к несохраняемой среде, где пользователям назначается одна из нескольких доступных машин (возможно, новая машина каждый новый сеанс), при этом пользовательские данные могут синхронизироваться или не синхронизироваться между сеансами.</span><span class="sxs-lookup"><span data-stu-id="bf795-124">Many VDI solutions allow access to persisted environments, where users are assigned a virtual environment that persists between sessions, and non-persisted environments, where users are assigned to one of several available machines, possibly a different machine each session, user data may or may not sync between sessions.</span></span>

<span data-ttu-id="bf795-125">При использовании несохраняемой среды обычно создается "золотой образ", который используется для каждого устройства и включает необходимые приложения и конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bf795-125">When using a non-persisted environment, one usually creates a “golden image” which is used for each device that includes the needed apps and configurations.</span></span> <span data-ttu-id="bf795-126">Ниже приведены наши рекомендации по подготовке Edge для такого образа.</span><span class="sxs-lookup"><span data-stu-id="bf795-126">Below are our recommendations for preparing Edge for such an image.</span></span>

### <a name="deploy-edge"></a><span data-ttu-id="bf795-127">Развертывание Edge</span><span class="sxs-lookup"><span data-stu-id="bf795-127">Deploy Edge</span></span>

<span data-ttu-id="bf795-128">Если вы используете Windows 10 версии 1803 или более поздней, Microsoft Edge уже должен быть установлен в вашей системе.</span><span class="sxs-lookup"><span data-stu-id="bf795-128">If you are on Windows 10, version 1803 and above, you should have Microsoft Edge installed on your system.</span></span> <span data-ttu-id="bf795-129">Однако, если вы используете старую версию Windows или хотите развернуть другой канал Edge, рекомендуется выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bf795-129">However, if you are on an older version of Windows or wish to deploy a different channel of Edge, the following steps are recommended.</span></span>

1. <span data-ttu-id="bf795-130">Скачайте пакет Edge MSI, соответствующий операционной системе вашей виртуальной машины VDI, перейдя по следующей ссылке:</span><span class="sxs-lookup"><span data-stu-id="bf795-130">Download the Edge MSI package matching your VDI VM operating system from:</span></span>

    - [<span data-ttu-id="bf795-131">Загрузка Microsoft Edge для бизнеса — Microsoft</span><span class="sxs-lookup"><span data-stu-id="bf795-131">Download Microsoft Edge for Business - Microsoft</span></span>](https://www.microsoft.com/edge/business/download)

2. <span data-ttu-id="bf795-132">Установите MSI на виртуальную машину VDI, запустив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bf795-132">Install the MSI to the VDI VM by running the following command:</span></span>

    - `msiexec /i <path_to_msi> /qn /norestart /l*v <install_logfile_name>`

### <a name="disable-automatic-updates"></a><span data-ttu-id="bf795-133">Отключение автоматических обновлений</span><span class="sxs-lookup"><span data-stu-id="bf795-133">Disable automatic updates</span></span>

<span data-ttu-id="bf795-134">Для несохраняемых машин лучше отключить автоматические обновления, вместо этого обновляя Edge путем обновления "золотого образа", чтобы исключить несоответствие версий в пуле машин.</span><span class="sxs-lookup"><span data-stu-id="bf795-134">For non-persisted machines it is best practice to disable automatic updates and instead update Edge by updating the “golden image” to ensure that there are no version mismatches among the pool of machines.</span></span>

<span data-ttu-id="bf795-135">См. следующие политики отключения автоматических обновлений.</span><span class="sxs-lookup"><span data-stu-id="bf795-135">See the following policies for disabling automatic updates:</span></span>

- [<span data-ttu-id="bf795-136">Переопределение политики обновления по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bf795-136">Update policy override default</span></span>](/deployedge/microsoft-edge-update-policies#updatedefault)

- [<span data-ttu-id="bf795-137">Переопределение политики обновления</span><span class="sxs-lookup"><span data-stu-id="bf795-137">Update policy override</span></span>](/deployedge/microsoft-edge-update-policies#update)

### <a name="profile-management"></a><span data-ttu-id="bf795-138">Управление профилем</span><span class="sxs-lookup"><span data-stu-id="bf795-138">Profile management</span></span>

<span data-ttu-id="bf795-139">При настройке несохраняемых машин важно учитывать, что виртуальные машины могут не сохранять данные пользователя между сеансами и что пользователю может быть назначена виртуальная машина, которую они никогда не использовали раньше и на которой поэтому нет их пользовательских данных.</span><span class="sxs-lookup"><span data-stu-id="bf795-139">On non-persisted setups it is important to consider that VMs may not maintain user state between sessions or users may be assigned a VM they have never used before and as such has none of their user data.</span></span>

<span data-ttu-id="bf795-140">Edge поддерживает несколько методов синхронизации пользовательских данных, с тем чтобы обеспечить их доступность независимо от того, как осуществляется доступ к Edge.</span><span class="sxs-lookup"><span data-stu-id="bf795-140">Edge supports several methods for syncing user data such that it is available regardless of how they are accessing Edge.</span></span>

### <a name="azure-ad-sync"></a><span data-ttu-id="bf795-141">Синхронизация Azure AD</span><span class="sxs-lookup"><span data-stu-id="bf795-141">Azure AD Sync</span></span>

<span data-ttu-id="bf795-142">Если ваш план Azure AD поддерживает этот вариант, корпоративная синхронизация является самым быстрым и простым методом синхронизации пользовательских данных Edge со всеми устройствами пользователей.</span><span class="sxs-lookup"><span data-stu-id="bf795-142">If your Azure AD plan supports it, Enterprise sync is the fastest and easiest method to ensure that Edge user data is synced to all user devices.</span></span>  

<span data-ttu-id="bf795-143">Ниже приведена более подробная информация о требованиях и конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bf795-143">See the following for more information on requirements and configuration.</span></span>  

- [<span data-ttu-id="bf795-144">Настройка корпоративной синхронизации Microsoft Edge | Документация Майкрософт</span><span class="sxs-lookup"><span data-stu-id="bf795-144">Configure Microsoft Edge enterprise sync | Microsoft Docs</span></span>](/deployedge/microsoft-edge-enterprise-sync)

### <a name="on-premise-sync-for-active-directory-users"></a><span data-ttu-id="bf795-145">Локальная синхронизация для пользователей Active Directory</span><span class="sxs-lookup"><span data-stu-id="bf795-145">On-premise Sync for Active Directory Users</span></span>

<span data-ttu-id="bf795-146">При локальной синхронизации Microsoft Edge сохраняет избранное и параметры пользователя Active Directory в файл, который можно легко перемещать между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="bf795-146">With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can easily be moved between different computers.</span></span>  

<span data-ttu-id="bf795-147">Ниже приведена более подробная информация о требованиях и конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bf795-147">See the following for more information on requirements and configuration.</span></span>  

- [<span data-ttu-id="bf795-148">Локальная синхронизация для пользователей Active Directory (AD) | Документация Майкрософт</span><span class="sxs-lookup"><span data-stu-id="bf795-148">On-premises sync for Active Directory (AD) users | Microsoft Docs</span></span>](/deployedge/microsoft-edge-on-premises-sync)

### <a name="user-profile-redirection"></a><span data-ttu-id="bf795-149">Перенаправление профилей пользователей</span><span class="sxs-lookup"><span data-stu-id="bf795-149">User Profile Redirection</span></span>  

<span data-ttu-id="bf795-150">Существует несколько решений по переносу и перенаправлению всей папки пользователя для сохранения пользовательского контекста в таких несохраняемых средах.</span><span class="sxs-lookup"><span data-stu-id="bf795-150">There are several solutions for migrating and redirecting the entire user folder to ensure that user context is maintained in such non-persisted environments.</span></span> <span data-ttu-id="bf795-151">Обратитесь к поставщику VDI, который порекомендует вам подходящее решение.</span><span class="sxs-lookup"><span data-stu-id="bf795-151">Check with your VDI provider to determine the recommended solution.</span></span>

<span data-ttu-id="bf795-152">Среди популярных решений следующие.</span><span class="sxs-lookup"><span data-stu-id="bf795-152">Some popular solutions include:</span></span>

- [<span data-ttu-id="bf795-153">FSLogix Overview - FSLogix | Документация Майкрософт</span><span class="sxs-lookup"><span data-stu-id="bf795-153">FSLogix Overview - FSLogix | Microsoft Docs</span></span>](/fslogix/overview)
- [<span data-ttu-id="bf795-154">Настройка управления профилем Citrix</span><span class="sxs-lookup"><span data-stu-id="bf795-154">How to Configure Citrix Profile Management</span></span>](https://support.citrix.com/article/CTX222893)

<span data-ttu-id="bf795-155">Кроме того, можно порекомендовать, чтобы при использовании этого метода ненужные папки были исключены из подлежащей резервному копированию папки пользователя, чтобы сократить время начальной загрузки при входе пользователей в машину и миграции профиля.</span><span class="sxs-lookup"><span data-stu-id="bf795-155">It is also may be recommended that when using this method unnecessary folders be excluded from the backed-up user folder to reduce initial loading times when users are logging on to a machine and the profile is being migrated.</span></span> <span data-ttu-id="bf795-156">В этом случае мы рекомендуем исключить следующие папки из резервного копирования, чтобы уменьшить размер.</span><span class="sxs-lookup"><span data-stu-id="bf795-156">If so, we recommend the following folders be excluded from your backup to reduce size.</span></span>

- <span data-ttu-id="bf795-157">%LocalAppData%\Microsoft\Edge\User Data\Default\Cache</span><span class="sxs-lookup"><span data-stu-id="bf795-157">%LocalAppData%\Microsoft\Edge\User Data\Default\Cache</span></span>
- <span data-ttu-id="bf795-158">%LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache</span><span class="sxs-lookup"><span data-stu-id="bf795-158">%LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache</span></span>
- <span data-ttu-id="bf795-159">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites</span><span class="sxs-lookup"><span data-stu-id="bf795-159">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites</span></span>
- <span data-ttu-id="bf795-160">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed</span><span class="sxs-lookup"><span data-stu-id="bf795-160">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed</span></span>

## <a name="known-issues"></a><span data-ttu-id="bf795-161">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="bf795-161">Known issues</span></span>

### <a name="microsoft-edge-crashes-in-older-versions-of-xenapp-and-xendesktop"></a><span data-ttu-id="bf795-162">Сбой Microsoft Edge в старых версиях XenApp и XenDesktop</span><span class="sxs-lookup"><span data-stu-id="bf795-162">Microsoft Edge crashes in older versions of XenApp and XenDesktop</span></span>

<span data-ttu-id="bf795-163">Эта проблема должна быть устранена в более новых версиях, однако если вы столкнулись с ней в вашей среде, в качестве временного решения можно отключить Citrix API Hooks для Edge — см. статью [Как отключить Citrix API Hooks на основе конкретных приложений](https://support.citrix.com/article/CTX107825).</span><span class="sxs-lookup"><span data-stu-id="bf795-163">This issue should be mitigated in newer versions however if you are encountering this issue in your environment, you can work around the issue by disabling Citrix API Hooks for Edge, see [How to Disable Citrix API Hooks on a Per-application Basis.](https://support.citrix.com/article/CTX107825)</span></span>

### <a name="degraded-performance-when-rendering-pages-with-exceptionally-large-html-tables"></a><span data-ttu-id="bf795-164">Ухудшение производительности при отрисовки страниц с очень большими таблицами HTML</span><span class="sxs-lookup"><span data-stu-id="bf795-164">Degraded performance when rendering pages with exceptionally large HTML tables</span></span>

<span data-ttu-id="bf795-165">Известно, что следующие политики Citrix замедляют отрисовку HTML-страниц с очень большими таблицами (более 30 000 строк).</span><span class="sxs-lookup"><span data-stu-id="bf795-165">The following Citrix policies are known to slow rendering of html pages with very large (30,000+ row) tables.</span></span>

- <span data-ttu-id="bf795-166">Автоматическое отображение клавиатуры</span><span class="sxs-lookup"><span data-stu-id="bf795-166">Automatic keyboard display</span></span>
- <span data-ttu-id="bf795-167">Удаленное поле со списком</span><span class="sxs-lookup"><span data-stu-id="bf795-167">Remote the combo box</span></span>

<span data-ttu-id="bf795-168">Подробнее см. раздел [Настройки политик для мобильного интерфейса (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html).</span><span class="sxs-lookup"><span data-stu-id="bf795-168">See [Mobile experience policy settings (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) for more information.</span></span> <span data-ttu-id="bf795-169">Отключение этих политик должно устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="bf795-169">Disabling these policies should mitigate the issue.</span></span>

### <a name="windows-account-manager-authorization-scenarios-ie--azure-sync-fail-in-edge-when-run-as-a-citrix-seamless-application"></a><span data-ttu-id="bf795-170">Сбой сценариев авторизации диспетчера учетных записей Windows (например, синхронизации Azure) в Edge при запуске в качестве удаленного приложения Citrix</span><span class="sxs-lookup"><span data-stu-id="bf795-170">Windows Account Manager authorization scenarios (i.e.  Azure sync) fail in Edge when run as a Citrix seamless application</span></span>

<span data-ttu-id="bf795-171">Это известная проблема в Edge и других приложениях, использующих WAM (например, Office), возникающая из-за отсутствия инициализации компонентов Windows, необходимых для таких сценариев, при работе в удаленном режиме.</span><span class="sxs-lookup"><span data-stu-id="bf795-171">This is a known issue in Edge and other applications that use WAM (i.e. Office) due to Windows components necessary for such scenarios not being initialized when running in the “seamless” mode.</span></span> <span data-ttu-id="bf795-172">Ниже приведены действия для временного решения этой проблемы.</span><span class="sxs-lookup"><span data-stu-id="bf795-172">To work around this issue:</span></span>

- <span data-ttu-id="bf795-173">Использование Edge в режиме удаленного рабочего стола в Citrix Host вместо режима удаленного приложения.</span><span class="sxs-lookup"><span data-stu-id="bf795-173">Use Edge via a Remote Desktop to the Citrix Host instead of as a seamless remote application.</span></span>
- <span data-ttu-id="bf795-174">Используйте удаленные приложения для виртуального рабочего стола Azure, в которых предусмотрены меры для решения этой проблемы.</span><span class="sxs-lookup"><span data-stu-id="bf795-174">Use Azure Virtual Desktop remote apps instead, which has mitigation's for this issue.</span></span>
