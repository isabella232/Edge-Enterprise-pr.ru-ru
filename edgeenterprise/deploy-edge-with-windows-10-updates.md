---
title: Развертывание Microsoft Edge с обновлениями Windows 10
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Развертывание Microsoft Edge с обновлениями Windows 10
ms.openlocfilehash: c8ea65f6c452b52b01c00d8fca418fe59db801b1
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447383"
---
# <a name="deploy-microsoft-edge-with-windows-10-updates"></a><span data-ttu-id="fefe6-103">Развертывание Microsoft Edge с обновлениями Windows 10</span><span class="sxs-lookup"><span data-stu-id="fefe6-103">Deploy Microsoft Edge with Windows 10 updates</span></span>

<span data-ttu-id="fefe6-104">В этой статье содержатся сведения для пользователей, развертывающих Microsoft Edge с помощью обновлений Windows 10.</span><span class="sxs-lookup"><span data-stu-id="fefe6-104">The article provides information for users who are deploying Microsoft Edge by using Windows 10 updates.</span></span>

## <a name="for-windows-10-release-20h2"></a><span data-ttu-id="fefe6-105">Для выпуска Windows 10 20H2</span><span class="sxs-lookup"><span data-stu-id="fefe6-105">For Windows 10 release 20H2</span></span>

<span data-ttu-id="fefe6-106">В Windows 10 версии 20H2 в качестве браузера по умолчанию уже установлен Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fefe6-106">Windows 10 version 20H2 already has Microsoft Edge installed as its default browser.</span></span>

## <a name="for-windows-10-releases-rs4-through-20h1"></a><span data-ttu-id="fefe6-107">Для выпусков Windows 10 RS4-20H1</span><span class="sxs-lookup"><span data-stu-id="fefe6-107">For Windows 10 releases RS4 through 20H1</span></span>

<span data-ttu-id="fefe6-108">Службы Windows Server Update Services (WSUS) имеют обновления для каждой версии Windows 10 с RS4 по 20H1. Эти обновления удалят классическое приложение Microsoft Edge Legacy и заменит его на Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fefe6-108">Windows Server Update Services (WSUS) has updates for each version of Windows 10 from RS4 through 20H1 that will remove the Microsoft Edge Legacy desktop app and replace it with Microsoft Edge.</span></span> <span data-ttu-id="fefe6-109">Дополнительные сведения, которые позволят определить, какое обновление WSUS подойдет для вашей версии Windows, см. [в этой статье](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c).</span><span class="sxs-lookup"><span data-stu-id="fefe6-109">For more information, see [this support article](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c) to find out which WSUS update is right for your Windows version.</span></span>

## <a name="for-windows-10-releases-prior-to-rs4-and-windows-7-81-and-earlier"></a><span data-ttu-id="fefe6-110">Для выпусков Windows 10 до RS4 (а также Windows 7, 8.1 и более ранних версий)</span><span class="sxs-lookup"><span data-stu-id="fefe6-110">For Windows 10 releases prior to RS4 (and Windows 7, 8.1, and earlier)</span></span>

<span data-ttu-id="fefe6-111">Обновления Windows для установки Microsoft Edge недоступны для этих версий.</span><span class="sxs-lookup"><span data-stu-id="fefe6-111">Windows updates to install Microsoft Edge aren't available for these versions.</span></span> <span data-ttu-id="fefe6-112">Рассмотрите другие варианты развертывания Microsoft Edge на этих устройствах, такие как [диспетчер конфигураций](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) или [Intune.](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="fefe6-112">Consider other options for deploying Microsoft Edge to these devices such as [Configuration Manager](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) or [Intune](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json).</span></span>

## <a name="see-also"></a><span data-ttu-id="fefe6-113">См. также</span><span class="sxs-lookup"><span data-stu-id="fefe6-113">See also</span></span>

- [<span data-ttu-id="fefe6-114">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="fefe6-114">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="fefe6-115">Планирование развертывания Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fefe6-115">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)