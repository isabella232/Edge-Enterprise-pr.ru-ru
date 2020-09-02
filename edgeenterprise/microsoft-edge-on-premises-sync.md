---
title: Локальная синхронизация для пользователей Active Directory (AD)
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 08/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Локальная синхронизация для пользователей Active Directory (AD)
ms.openlocfilehash: 89f061072fdaa748d317ca8dc0c290893cfdfd6c
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980982"
---
# <span data-ttu-id="11d2a-103">Локальная синхронизация для пользователей Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="11d2a-103">On-premises sync for Active Directory (AD) users</span></span>

<span data-ttu-id="11d2a-104">В этой статье объясняется, как пользователи Active Directory (AD) могут перемещать избранное и параметры Microsoft Edge между компьютерами, не подключаясь к облачным службам (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="11d2a-104">This article explains how Active Directory (AD) users can roam Microsoft Edge favorites and settings between computers without connecting to Microsoft cloud services.</span></span>

> [!NOTE]
> <span data-ttu-id="11d2a-105">Эта статья относится к Microsoft Edge версии 85 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="11d2a-105">This article applies to Microsoft Edge version 85 or later.</span></span>

## <span data-ttu-id="11d2a-106">Введение</span><span class="sxs-lookup"><span data-stu-id="11d2a-106">Introduction</span></span>

<span data-ttu-id="11d2a-107">Для синхронизации данных пользователя в Microsoft Edge обычно требуется учетная запись Майкрософт или учетная запись Azure Active Directory (Azure AD), а также подключение к облачным службам (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="11d2a-107">Syncing user data in Microsoft Edge normally requires either a Microsoft Account or an Azure Active Directory (Azure AD) account, and a connection to Microsoft cloud services.</span></span> <span data-ttu-id="11d2a-108">При использовании локальной синхронизации Microsoft Edge сохраняет избранное и параметры пользователя Active Directory в файле, который можно перемещать между различными компьютерами.</span><span class="sxs-lookup"><span data-stu-id="11d2a-108">With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can be moved between different computers.</span></span> <span data-ttu-id="11d2a-109">Локальная синхронизация не влияет на облачную синхронизацию профилей, для которых она разрешена.</span><span class="sxs-lookup"><span data-stu-id="11d2a-109">On-premises sync doesn't interfere with cloud syncing for those profiles that allow it.</span></span>

## <span data-ttu-id="11d2a-110">Принцип работы</span><span class="sxs-lookup"><span data-stu-id="11d2a-110">How it works</span></span>

<span data-ttu-id="11d2a-111">Microsoft Edge позволяет связать профили с учетными записями Active Directory (AD), которые невозможно использовать с облачной синхронизацией. При включении локальной синхронизации данные из профиля AD сохраняются в файле profile.pb.</span><span class="sxs-lookup"><span data-stu-id="11d2a-111">Microsoft Edge allows profiles to be associated with Active Directory (AD) accounts, which can't be used with cloud sync. When on-premises sync is enabled, the data from the AD profile is saved to a file named profile.pb.</span></span> <span data-ttu-id="11d2a-112">По умолчанию этот файл хранится в *%APP_DATA%/Microsoft/Edge*.</span><span class="sxs-lookup"><span data-stu-id="11d2a-112">By default, this file is stored in *%APP_DATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="11d2a-113">Записанный файл можно перемещать между несколькими компьютерами, и на каждом из них будет выполняться чтение и запись данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="11d2a-113">After this file is written, it can be moved between different computers, and user data will be read and written on each computer.</span></span>

## <span data-ttu-id="11d2a-114">Использование локальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="11d2a-114">Use on-premises sync</span></span>

<span data-ttu-id="11d2a-115">Чтобы использовать локальную синхронизацию, необходимо включить ее, связать профиль с учетной записью AD и при необходимости изменить расположение данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="11d2a-115">To use on-premises sync, you have to enable it, associate a profile with an AD account, and optionally, change the location of the user data.</span></span>

### <span data-ttu-id="11d2a-116">Включение локальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="11d2a-116">Enable on-premises sync</span></span>

<span data-ttu-id="11d2a-117">Чтобы включить локальную синхронизацию в Microsoft Edge, настройте политику [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled).</span><span class="sxs-lookup"><span data-stu-id="11d2a-117">To enable on-premises sync in Microsoft Edge, configure the [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled) policy.</span></span>

### <span data-ttu-id="11d2a-118">Убедитесь, что профиль связан с учетной записью Active Directory</span><span class="sxs-lookup"><span data-stu-id="11d2a-118">Ensure that a profile is associated with an Active Directory account</span></span>

<span data-ttu-id="11d2a-119">Для выполнения локальной синхронизации необходим профиль, связанный с учетной записью Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="11d2a-119">On-premises sync only works with the profile associated with an Active Directory (AD) account.</span></span> <span data-ttu-id="11d2a-120">При отсутствии такого профиля локальная синхронизация не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11d2a-120">If no such profile exists, on-premises sync will not function.</span></span> <span data-ttu-id="11d2a-121">Чтобы убедиться, что пользователи входят в систему с помощью учетной записи AD, настройте политику [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin).</span><span class="sxs-lookup"><span data-stu-id="11d2a-121">To ensure that users sign on with an AD account, configure the [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin) policy.</span></span>

### <span data-ttu-id="11d2a-122">Изменение расположения данных пользователя (необязательно)</span><span class="sxs-lookup"><span data-stu-id="11d2a-122">Change the location of the user data (optional)</span></span>

<span data-ttu-id="11d2a-123">По умолчанию данные пользователя хранятся в файле **profile.pb** в *%APP_DATA%/Microsoft/Edge*.</span><span class="sxs-lookup"><span data-stu-id="11d2a-123">By default, the user data is stored in a filed named **profile.pb** in *%APP_DATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="11d2a-124">Чтобы изменить расположение этого файла, настройте политику [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation).</span><span class="sxs-lookup"><span data-stu-id="11d2a-124">To change the location of this file, configure the [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation) policy.</span></span>

## <span data-ttu-id="11d2a-125">Изменения во взаимодействии с пользователем при включении локальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="11d2a-125">Changes in the user experience when on-premises sync is enabled</span></span>

<span data-ttu-id="11d2a-126">Если включена локальная синхронизация, пользователям не будет предложено включить синхронизацию. Кроме того, пользователи не могут отключить синхронизацию в параметрах синхронизации или включить типы синхронизации, которые не поддерживаются локальной синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="11d2a-126">When on-premises sync is enabled, users won't be asked to enable sync. In addition, users can't turn off sync in Sync settings, and they can't turn on sync types that aren't supported by on-premises sync.</span></span>

## <span data-ttu-id="11d2a-127">Заметки об использовании локальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="11d2a-127">On-premises sync usage notes</span></span>

### <span data-ttu-id="11d2a-128">Выполнение облачной синхронизации и локальной синхронизации на одном компьютере</span><span class="sxs-lookup"><span data-stu-id="11d2a-128">Running cloud sync and on-premises sync on the same computer</span></span>

<span data-ttu-id="11d2a-129">Локальная синхронизация не влияет на облачную синхронизацию. Если в Microsoft Edge есть несколько учетных записей Майкрософт или профилей Azure Active Directory, которые синхронизируются с облаком, эти профили продолжат синхронизироваться при включении локальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="11d2a-129">On-premises sync doesn't interfere with cloud sync. If Microsoft Edge has multiple Microsoft Account or Azure Active Directory profiles that sync to the cloud, these profiles will continue to sync while on-premises sync is enabled.</span></span>

### <span data-ttu-id="11d2a-130">Не рекомендуется запуск Microsoft Edge на нескольких компьютерах одновременно</span><span class="sxs-lookup"><span data-stu-id="11d2a-130">Running Microsoft Edge on more than one computer at a time isn't recommended</span></span>

<span data-ttu-id="11d2a-131">Так как при локальной синхронизации выполняется перемещение файла данных пользователя между компьютерами, изменения между одновременными сеансами не синхронизируются.</span><span class="sxs-lookup"><span data-stu-id="11d2a-131">Because on-premises sync works by moving a user data file between computers, on-premises sync doesn't sync changes between simultaneous sessions.</span></span> <span data-ttu-id="11d2a-132">Поэтому локальную синхронизацию лучше всего использовать на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="11d2a-132">For this reason, on-premises sync works best when used on one computer at a time.</span></span> <span data-ttu-id="11d2a-133">Если выполняются одновременные локальные сеансы, данные на любом из компьютеров могут неожиданно переопределяться данными с другого компьютера при следующем запуске сеанса браузера.</span><span class="sxs-lookup"><span data-stu-id="11d2a-133">If there are simultaneous on-premises sessions running, data on any of the computers may be unexpectedly overwritten by data from another computer the next time you start a browser session.</span></span>

> [!NOTE]
> <span data-ttu-id="11d2a-134">Microsoft Edge блокирует файл **profile.pb** при включении локальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="11d2a-134">Microsoft Edge locks the **profile.pb** file when on-premises sync is enabled.</span></span> <span data-ttu-id="11d2a-135">Если один файл **profile.pb** совместно используется на нескольких компьютерах с помощью перенаправления папок, тогда можно запускать только один экземпляр Microsoft Edge, использующий этот файл.</span><span class="sxs-lookup"><span data-stu-id="11d2a-135">If folder redirection is used to share a single **profile.pb** file between different computers, then only one instance of Microsoft Edge using that file can be started.</span></span>

### <span data-ttu-id="11d2a-136">Использование других политик синхронизации при локальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="11d2a-136">Using other sync policies with on-premises sync</span></span>

<span data-ttu-id="11d2a-137">Политику [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) можно использовать для выборочного отключения избранного или параметров синхронизации при необходимости.</span><span class="sxs-lookup"><span data-stu-id="11d2a-137">The [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) policy can be used to selectively disable either favorites or settings sync if desired.</span></span> <span data-ttu-id="11d2a-138">Если включена политика [SyncDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled), локальная синхронизация также будет отключена.</span><span class="sxs-lookup"><span data-stu-id="11d2a-138">If the [SyncDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled) policy is active, then on-premises sync is disabled as well.</span></span>  

## <span data-ttu-id="11d2a-139">См. также</span><span class="sxs-lookup"><span data-stu-id="11d2a-139">See also</span></span>

- [<span data-ttu-id="11d2a-140">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="11d2a-140">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="11d2a-141">Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="11d2a-141">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="11d2a-142">Синхронизация Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="11d2a-142">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
