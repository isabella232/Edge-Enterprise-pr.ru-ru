---
title: Локальная синхронизация для пользователей Active Directory (AD)
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 02/12/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Локальная синхронизация для пользователей Active Directory (AD)
ms.openlocfilehash: adf0adc8370aa1e18d07d0d2e91727d1ac607bf1
ms.sourcegitcommit: 90b8eab62edbed0e0a84780abd7d3854bf95c130
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "11328051"
---
# <span data-ttu-id="8227e-103">Локальная синхронизация для пользователей Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="8227e-103">On-premises sync for Active Directory (AD) users</span></span>

<span data-ttu-id="8227e-104">В этой статье объясняется, как пользователи Active Directory (AD) могут перемещать избранное и параметры Microsoft Edge между компьютерами, не подключаясь к облачным службам (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="8227e-104">This article explains how Active Directory (AD) users can roam Microsoft Edge favorites and settings between computers without connecting to Microsoft cloud services.</span></span>

> [!NOTE]
> <span data-ttu-id="8227e-105">Эта статья относится к Microsoft Edge версии 85 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="8227e-105">This article applies to Microsoft Edge version 85 or later.</span></span>

## <span data-ttu-id="8227e-106">Введение</span><span class="sxs-lookup"><span data-stu-id="8227e-106">Introduction</span></span>

<span data-ttu-id="8227e-107">Для синхронизации данных пользователя в Microsoft Edge обычно требуется учетная запись Майкрософт или учетная запись Azure Active Directory (Azure AD), а также подключение к облачным службам (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="8227e-107">Syncing user data in Microsoft Edge normally requires either a Microsoft Account or an Azure Active Directory (Azure AD) account, and a connection to Microsoft cloud services.</span></span> <span data-ttu-id="8227e-108">При использовании локальной синхронизации Microsoft Edge сохраняет избранное и параметры пользователя Active Directory в файле, который можно перемещать между различными компьютерами.</span><span class="sxs-lookup"><span data-stu-id="8227e-108">With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can be moved between different computers.</span></span> <span data-ttu-id="8227e-109">Локальная синхронизация не влияет на облачную синхронизацию профилей, для которых она разрешена.</span><span class="sxs-lookup"><span data-stu-id="8227e-109">On-premises sync doesn't interfere with cloud syncing for those profiles that allow it.</span></span>

## <span data-ttu-id="8227e-110">Принцип работы</span><span class="sxs-lookup"><span data-stu-id="8227e-110">How it works</span></span>

<span data-ttu-id="8227e-111">Microsoft Edge позволяет связать профили с учетными записями Active Directory (AD), которые невозможно использовать с облачной синхронизацией. При включении локальной синхронизации данные из профиля AD сохраняются в файле profile.pb.</span><span class="sxs-lookup"><span data-stu-id="8227e-111">Microsoft Edge allows profiles to be associated with Active Directory (AD) accounts, which can't be used with cloud sync. When on-premises sync is enabled, the data from the AD profile is saved to a file named profile.pb.</span></span> <span data-ttu-id="8227e-112">По умолчанию этот файл хранится в *%APPDATA%/Microsoft/Edge*.</span><span class="sxs-lookup"><span data-stu-id="8227e-112">By default, this file is stored in *%APPDATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="8227e-113">Записанный файл можно перемещать между несколькими компьютерами, и на каждом из них будет выполняться чтение и запись данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="8227e-113">After this file is written, it can be moved between different computers, and user data will be read and written on each computer.</span></span> <span data-ttu-id="8227e-114">Microsoft Edge только считывает и записывает из этого файла; ответственность за перемещение файла по мере необходимости лежит на администраторе.</span><span class="sxs-lookup"><span data-stu-id="8227e-114">Microsoft Edge only reads and writes from this file; it is the admin's responsibility to ensure that the file is moved as needed.</span></span>

## <span data-ttu-id="8227e-115">Использование локальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="8227e-115">Use on-premises sync</span></span>

<span data-ttu-id="8227e-116">Чтобы использовать локальную синхронизацию, необходимо включить ее, связать профиль с учетной записью AD и при необходимости изменить расположение данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="8227e-116">To use on-premises sync, you have to enable it, associate a profile with an AD account, and optionally, change the location of the user data.</span></span>

### <span data-ttu-id="8227e-117">Включение локальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="8227e-117">Enable on-premises sync</span></span>

<span data-ttu-id="8227e-118">Чтобы включить локальную синхронизацию в Microsoft Edge, настройте политику [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled).</span><span class="sxs-lookup"><span data-stu-id="8227e-118">To enable on-premises sync in Microsoft Edge, configure the [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled) policy.</span></span>

### <span data-ttu-id="8227e-119">Убедитесь, что профиль связан с учетной записью Active Directory</span><span class="sxs-lookup"><span data-stu-id="8227e-119">Ensure that a profile is associated with an Active Directory account</span></span>

<span data-ttu-id="8227e-120">Для выполнения локальной синхронизации необходим профиль, связанный с учетной записью Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="8227e-120">On-premises sync only works with the profile associated with an Active Directory (AD) account.</span></span> <span data-ttu-id="8227e-121">При отсутствии такого профиля локальная синхронизация не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8227e-121">If no such profile exists, on-premises sync will not function.</span></span> <span data-ttu-id="8227e-122">Чтобы убедиться, что пользователи входят в систему с помощью учетной записи AD, настройте политику [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin).</span><span class="sxs-lookup"><span data-stu-id="8227e-122">To ensure that users sign on with an AD account, configure the [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin) policy.</span></span> <span data-ttu-id="8227e-123">Для локальной синхронизации Microsoft Edge использует только AD для установления удостоверения для данных пользователя, и нет прямой связи между тем, как Microsoft Edge считывает и записывает локальные данные, и тем, как администратор настроил роуминг для пользователя AD.</span><span class="sxs-lookup"><span data-stu-id="8227e-123">For on-premises sync, Microsoft Edge only relies on AD to establish an identity for the user data, and there's no direct relationship between how Microsoft Edge reads and writes on-premises data to how the admin has configured roaming for an AD user.</span></span>

### <span data-ttu-id="8227e-124">Изменение расположения данных пользователя (необязательно)</span><span class="sxs-lookup"><span data-stu-id="8227e-124">Change the location of the user data (optional)</span></span>

<span data-ttu-id="8227e-125">По умолчанию данные пользователя хранятся в файле **profile.pb** в *%APPDATA%/Microsoft/Edge*.</span><span class="sxs-lookup"><span data-stu-id="8227e-125">By default, the user data is stored in a filed named **profile.pb** in *%APPDATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="8227e-126">Чтобы изменить расположение этого файла, настройте политику [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation).</span><span class="sxs-lookup"><span data-stu-id="8227e-126">To change the location of this file, configure the [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation) policy.</span></span>

## <span data-ttu-id="8227e-127">Изменения во взаимодействии с пользователем при включении локальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="8227e-127">Changes in the user experience when on-premises sync is enabled</span></span>

<span data-ttu-id="8227e-128">Если включена локальная синхронизация, пользователям не будет предложено включить синхронизацию. Кроме того, пользователи не могут отключить синхронизацию в параметрах синхронизации или включить типы синхронизации, которые не поддерживаются локальной синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="8227e-128">When on-premises sync is enabled, users won't be asked to enable sync. In addition, users can't turn off sync in Sync settings, and they can't turn on sync types that aren't supported by on-premises sync.</span></span>

## <span data-ttu-id="8227e-129">Заметки об использовании локальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="8227e-129">On-premises sync usage notes</span></span>

### <span data-ttu-id="8227e-130">Выполнение облачной синхронизации и локальной синхронизации на одном компьютере</span><span class="sxs-lookup"><span data-stu-id="8227e-130">Running cloud sync and on-premises sync on the same computer</span></span>

<span data-ttu-id="8227e-131">Локальная синхронизация не влияет на облачную синхронизацию. Если в Microsoft Edge есть несколько учетных записей Майкрософт или профилей Azure Active Directory, которые синхронизируются с облаком, эти профили продолжат синхронизироваться при включении локальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8227e-131">On-premises sync doesn't interfere with cloud sync. If Microsoft Edge has multiple Microsoft Account or Azure Active Directory profiles that sync to the cloud, these profiles will continue to sync while on-premises sync is enabled.</span></span>

### <span data-ttu-id="8227e-132">Не рекомендуется запуск Microsoft Edge на нескольких компьютерах одновременно</span><span class="sxs-lookup"><span data-stu-id="8227e-132">Running Microsoft Edge on more than one computer at a time isn't recommended</span></span>

<span data-ttu-id="8227e-133">Так как при локальной синхронизации выполняется перемещение файла данных пользователя между компьютерами, изменения между одновременными сеансами не синхронизируются.</span><span class="sxs-lookup"><span data-stu-id="8227e-133">Because on-premises sync works by moving a user data file between computers, on-premises sync doesn't sync changes between simultaneous sessions.</span></span> <span data-ttu-id="8227e-134">Поэтому локальную синхронизацию лучше всего использовать на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="8227e-134">For this reason, on-premises sync works best when used on one computer at a time.</span></span> <span data-ttu-id="8227e-135">Если выполняются одновременные локальные сеансы, данные на любом из компьютеров могут неожиданно переопределяться данными с другого компьютера при следующем запуске сеанса браузера.</span><span class="sxs-lookup"><span data-stu-id="8227e-135">If there are simultaneous on-premises sessions running, data on any of the computers may be unexpectedly overwritten by data from another computer the next time you start a browser session.</span></span>

> [!NOTE]
> <span data-ttu-id="8227e-136">Microsoft Edge блокирует файл **profile.pb** при включении локальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8227e-136">Microsoft Edge locks the **profile.pb** file when on-premises sync is enabled.</span></span> <span data-ttu-id="8227e-137">Если один файл **profile.pb** совместно используется на нескольких компьютерах с помощью перенаправления папок, тогда можно запускать только один экземпляр Microsoft Edge, использующий этот файл.</span><span class="sxs-lookup"><span data-stu-id="8227e-137">If folder redirection is used to share a single **profile.pb** file between different computers, then only one instance of Microsoft Edge using that file can be started.</span></span>

### <span data-ttu-id="8227e-138">Использование других политик синхронизации при локальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="8227e-138">Using other sync policies with on-premises sync</span></span>

<span data-ttu-id="8227e-139">Политику [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) можно использовать для выборочного отключения избранного или параметров синхронизации при необходимости.</span><span class="sxs-lookup"><span data-stu-id="8227e-139">The [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) policy can be used to selectively disable either favorites or settings sync if desired.</span></span> <span data-ttu-id="8227e-140">Политика [SyncDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled) не влияет на локальное синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="8227e-140">The [SyncDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled) policy has no impact on on-premises sync.</span></span>

## <span data-ttu-id="8227e-141">См. также</span><span class="sxs-lookup"><span data-stu-id="8227e-141">See also</span></span>

- [<span data-ttu-id="8227e-142">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="8227e-142">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="8227e-143">Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="8227e-143">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="8227e-144">Синхронизация Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="8227e-144">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
