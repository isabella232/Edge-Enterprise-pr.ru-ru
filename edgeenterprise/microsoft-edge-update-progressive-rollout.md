---
title: Постепенное развертывание обновлений стабильного канала Microsoft Edge
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 05/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Постепенное развертывание обновлений стабильного канала Microsoft Edge
ms.openlocfilehash: 5b0d2f58318b10538d0470b644d346b5b9b9489b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980930"
---
# <span data-ttu-id="b15d5-103">Постепенное развертывание обновлений стабильного канала Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b15d5-103">Progressive rollouts for Microsoft Edge Stable channel updates</span></span>

<span data-ttu-id="b15d5-104">С выпуска Microsoft Edge 83 мы будем постепенно разворачивать основные обновления для стабильного канала Microsoft Edge в течение нескольких дней.</span><span class="sxs-lookup"><span data-stu-id="b15d5-104">Starting with Microsoft Edge 83 release, we will perform gradual rollouts of major updates to Microsoft Edge Stable channel over the span of a few days.</span></span> <span data-ttu-id="b15d5-105">Это постепенное развертывание позволяет нам отслеживать обновления и безопасно обновлять браузер в организации.</span><span class="sxs-lookup"><span data-stu-id="b15d5-105">This progressive rollout allows us to monitor upgrades and safely update the browser across the organization.</span></span>

> [!NOTE]
> <span data-ttu-id="b15d5-106">Эта статья относится к Microsoft Edge версии 83 или более поздней из стабильного канала.</span><span class="sxs-lookup"><span data-stu-id="b15d5-106">This applies to Microsoft Edge Stable channel version 83 or later.</span></span>

## <span data-ttu-id="b15d5-107">Зачем нужно постепенное развертывание?</span><span class="sxs-lookup"><span data-stu-id="b15d5-107">Why do we need progressive rollout?</span></span>

<span data-ttu-id="b15d5-108">Внимательно отслеживая работоспособность наших обновлений и развертывая обновления в течение нескольких дней, мы можем сократить влияние проблем, которые могут возникать в новых обновлениях.</span><span class="sxs-lookup"><span data-stu-id="b15d5-108">By monitoring the health of our updates closely and rolling out the updates over the course of several days, we can limit the impact of issues that might occur with the new update.</span></span> <span data-ttu-id="b15d5-109">В выпуске Microsoft Edge 83 постепенные развертывания будут включены для всех версий Microsoft Edge, предназначенных для Windows 7, Windows 8 и 8.1, а также Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b15d5-109">With Microsoft Edge release 83, Progressive Rollouts will be enabled for all Windows 7, Windows 8 & 8.1, and Windows 10 versions of Microsoft Edge.</span></span> <span data-ttu-id="b15d5-110">Microsoft Edge станет поддерживаться на Mac сразу по мере готовности.</span><span class="sxs-lookup"><span data-stu-id="b15d5-110">We will support Microsoft Edge on Mac as soon as it is ready.</span></span>

## <span data-ttu-id="b15d5-111">Как будут работать обновления?</span><span class="sxs-lookup"><span data-stu-id="b15d5-111">How will the updates work?</span></span>

<span data-ttu-id="b15d5-112">Каждой установке Microsoft Edge присваивается значение обновления.</span><span class="sxs-lookup"><span data-stu-id="b15d5-112">Each installation of Microsoft Edge is assigned an upgrade value.</span></span> <span data-ttu-id="b15d5-113">Когда мы начнем постепенное развертывание, вы получите обновление после того, как значение вашего устройства попадет в диапазон значений обновления.</span><span class="sxs-lookup"><span data-stu-id="b15d5-113">When we start rolling out incrementally, you'll see the update when the value on your device falls within the upgrade value range.</span></span> <span data-ttu-id="b15d5-114">По мере развертывания (в течение нескольких дней) все пользователи получат обновление.</span><span class="sxs-lookup"><span data-stu-id="b15d5-114">As the rollout progresses (within a few days), all users will eventually get the update.</span></span> <span data-ttu-id="b15d5-115">Обновления браузера с важными исправлениями системы безопасности будут разворачиваться чаще, чем обновления без важных исправлений системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="b15d5-115">Browser updates with critical security fixes will have a faster rollout cadence than updates that don't have critical security fixes.</span></span> <span data-ttu-id="b15d5-116">Это сделано для быстрого обеспечения защиты от уязвимостей.</span><span class="sxs-lookup"><span data-stu-id="b15d5-116">This is done to ensure prompt protection from vulnerabilities.</span></span>

## <span data-ttu-id="b15d5-117">Как это повлияет на предприятия?</span><span class="sxs-lookup"><span data-stu-id="b15d5-117">How does this affect enterprises?</span></span>

<span data-ttu-id="b15d5-118">Артефакты Microsoft Edge распространяются для предприятий с помощью нескольких механизмов, таких как Microsoft Intune, Windows Server Update Service (WSUS) и диспетчер конфигураций.</span><span class="sxs-lookup"><span data-stu-id="b15d5-118">Microsoft Edge artifacts are distributed to enterprises using multiple mechanisms such as Microsoft Intune, Windows Server Update Service (WSUS), and Configuration Manager.</span></span> <span data-ttu-id="b15d5-119">Эти средства развертывания работают по-разному в отношении постепенного развертывания:</span><span class="sxs-lookup"><span data-stu-id="b15d5-119">These deployment tools behave differently with respect to Progressive Rollout:</span></span>

- <span data-ttu-id="b15d5-120">Предприятия, управляющие распространением через Microsoft Intune, зарегистрированы для получения автоматических обновлений.</span><span class="sxs-lookup"><span data-stu-id="b15d5-120">Enterprises that manage distribution via Microsoft Intune are registered for auto-updates.</span></span> <span data-ttu-id="b15d5-121">При применении постепенного развертывания все пользователи увидят обновление через несколько дней.</span><span class="sxs-lookup"><span data-stu-id="b15d5-121">Progressive Rollout is used, and all the users will see an update in a few days.</span></span>
- <span data-ttu-id="b15d5-122">Предприятия, управляющие распространением с помощью WSUS (Windows Server Update Services) или диспетчера конфигураций, не зарегистрированы для получения автоматических обновлений.</span><span class="sxs-lookup"><span data-stu-id="b15d5-122">Enterprises that manage distribution through WSUS (Windows Server Update Services) or Configuration Manager are not registered for auto-updates.</span></span> <span data-ttu-id="b15d5-123">Управление обновлениями, которые будут доступны с самого начала, а также их применение осуществляют администраторы.</span><span class="sxs-lookup"><span data-stu-id="b15d5-123">Administrators manage and apply the updates that will be available from the start.</span></span> <span data-ttu-id="b15d5-124">Постепенное развертывание не влияет на этот процесс.</span><span class="sxs-lookup"><span data-stu-id="b15d5-124">Progressive Rollout does not affect this process.</span></span>

<span data-ttu-id="b15d5-125">Поделитесь своим ценным мнением с помощью сайта User Voice, кнопки отзыва в приложении или ниже в комментариях, если у вас возникли проблемы или вопросы.</span><span class="sxs-lookup"><span data-stu-id="b15d5-125">Please share your valuable feedback through user voice, the in-application feedback button, or below in the comments if you have any concerns or questions.</span></span>

## <span data-ttu-id="b15d5-126">См. также</span><span class="sxs-lookup"><span data-stu-id="b15d5-126">See also</span></span>

- [<span data-ttu-id="b15d5-127">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="b15d5-127">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
