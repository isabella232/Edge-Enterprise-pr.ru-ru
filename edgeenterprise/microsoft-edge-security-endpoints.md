---
title: Список разрешений для конечных точек Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 11/25/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Список разрешений для конечных точек Microsoft Edge
ms.openlocfilehash: 3d46e2e8c85eadc39cf9788df44b45592ea4fb1b
ms.sourcegitcommit: ed6a5afabf909df87bec48671c4c47bcdfaeb7bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/02/2020
ms.locfileid: "11194696"
---
# <span data-ttu-id="dd96d-103">Список разрешений для конечных точек Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="dd96d-103">Allow list for Microsoft Edge endpoints</span></span>

<span data-ttu-id="dd96d-104">Для работы этих функций в Microsoft Edge требуется подключение к Интернету.</span><span class="sxs-lookup"><span data-stu-id="dd96d-104">Microsoft Edge requires connectivity to the Internet to support its features.</span></span> <span data-ttu-id="dd96d-105">В этой статье указаны URL-адреса доменов, которые необходимо добавить в список разрешений для обеспечения взаимодействия через брандмауэры и другие механизмы защиты.</span><span class="sxs-lookup"><span data-stu-id="dd96d-105">This article identifies the domain URLs that you need to add to the Allow list to ensure communications through firewalls and other security mechanisms.</span></span>

> [!NOTE]
> <span data-ttu-id="dd96d-106">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="dd96d-106">This applies  to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="dd96d-107">URL-адреса доменов, которые необходимо добавить в список разрешений</span><span class="sxs-lookup"><span data-stu-id="dd96d-107">Domain URLs to allow</span></span>

<span data-ttu-id="dd96d-108">Разрешите следующие URL-адреса доменов для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dd96d-108">Allow the following domain URLs for Microsoft Edge.</span></span>

### <span data-ttu-id="dd96d-109">Служба обновления</span><span class="sxs-lookup"><span data-stu-id="dd96d-109">Update Service</span></span>

<span data-ttu-id="dd96d-110">Служба, которую Microsoft Edge использует для проверки наличия новых обновлений.</span><span class="sxs-lookup"><span data-stu-id="dd96d-110">The service that Microsoft Edge uses to check for new updates.</span></span>

- `https://msedge.api.cdp.microsoft.com`

### <span data-ttu-id="dd96d-111">Служба экспериментов и конфигураций</span><span class="sxs-lookup"><span data-stu-id="dd96d-111">Experimentation and Configuration service</span></span>

- `https://config.edge.skype.com`

### <span data-ttu-id="dd96d-112">Расположения загрузки для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="dd96d-112">Download locations for Microsoft Edge</span></span>

<span data-ttu-id="dd96d-113">Расположения Microsoft Edge можно скачать во время начальной установки или при появлении обновления.</span><span class="sxs-lookup"><span data-stu-id="dd96d-113">Locations Microsoft Edge can be downloaded from during an initial install or when an update is available.</span></span> <span data-ttu-id="dd96d-114">Расположение для загрузки определяется службой обновления.</span><span class="sxs-lookup"><span data-stu-id="dd96d-114">The download location is determined by the Update Service.</span></span>

#### <span data-ttu-id="dd96d-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="dd96d-115">HTTP</span></span>

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### <span data-ttu-id="dd96d-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="dd96d-116">HTTPS</span></span>

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > <span data-ttu-id="dd96d-117">Чтобы упростить список разрешений для расположений загрузки, можно использовать подстановочный знак.</span><span class="sxs-lookup"><span data-stu-id="dd96d-117">To simplify the allow list for download locations a wild card can be used:</span></span> `*.dl.delivery.mp.microsoft.com`

### <span data-ttu-id="dd96d-118">Расположения загрузки для расширений Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="dd96d-118">Download locations for Microsoft Edge Extensions</span></span>

<span data-ttu-id="dd96d-119">Расположения для расширений Microsoft Edge можно скачать во время начальной установки или при появлении обновления.</span><span class="sxs-lookup"><span data-stu-id="dd96d-119">Locations Microsoft Edge Extensions can be downloaded from during an initial install or when an update is available.</span></span> <span data-ttu-id="dd96d-120">Расположение для загрузки определяется службой обновления.</span><span class="sxs-lookup"><span data-stu-id="dd96d-120">The download location is determined by the Update Service.</span></span>

#### <span data-ttu-id="dd96d-121">HTTP</span><span class="sxs-lookup"><span data-stu-id="dd96d-121">HTTP</span></span>

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### <span data-ttu-id="dd96d-122">HTTPS</span><span class="sxs-lookup"><span data-stu-id="dd96d-122">HTTPS</span></span>

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > <span data-ttu-id="dd96d-123">Чтобы упростить список разрешений для расположений загрузки, можно использовать подстановочный знак.</span><span class="sxs-lookup"><span data-stu-id="dd96d-123">To simplify the allow list for download locations a wild card can be used:</span></span> `*.dl.delivery.mp.microsoft.com`

### <span data-ttu-id="dd96d-124">Дополнительно для оптимизации доставки загрузки</span><span class="sxs-lookup"><span data-stu-id="dd96d-124">Optionally for Download Delivery Optimization</span></span>

<span data-ttu-id="dd96d-125">Сведения об оптимизации доставки см. в разделе [Оптимизация доставки обновлений Windows 10](https://aka.ms/waas-do).</span><span class="sxs-lookup"><span data-stu-id="dd96d-125">For information about delivery optimization, see [Delivery Optimization for Windows 10 updates](https://aka.ms/waas-do).</span></span>

- <span data-ttu-id="dd96d-126">Обмен данными между клиентом и службой: `*.do.dsp.mp.microsoft.com` (HTTP-порт 80, HTTPS-порт 443)</span><span class="sxs-lookup"><span data-stu-id="dd96d-126">Client to Service communication: `*.do.dsp.mp.microsoft.com` (HTTP Port 80, HTTPS Port 443)</span></span>
- <span data-ttu-id="dd96d-127">Обмен данными между клиентами: TCP-порт 7680 должен быть открыт для входящего трафика</span><span class="sxs-lookup"><span data-stu-id="dd96d-127">Client to Client communication: TCP port 7680 should be open for inbound traffic</span></span>

### <span data-ttu-id="dd96d-128">Sync</span><span class="sxs-lookup"><span data-stu-id="dd96d-128">Sync</span></span>

<span data-ttu-id="dd96d-129">Эти конечные точки управляют чтением и записью синхронизированных данных, управлением правами для безопасных данных, а также уведомлением браузера о доступности новых синхронизированных данных.</span><span class="sxs-lookup"><span data-stu-id="dd96d-129">These endpoints manage the reading and writing of synced data, rights management for secure data, and notifying the browser when new sync data is available.</span></span>

- <span data-ttu-id="dd96d-130">Конечные точки службы синхронизации Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="dd96d-130">Edge sync service endpoints:</span></span>

  - `https://edge-enterprise.activity.windows.com`
  - `https://edge.activity.windows.com`

- <span data-ttu-id="dd96d-131">Конечные точки Azure Information Protection:</span><span class="sxs-lookup"><span data-stu-id="dd96d-131">Azure Information Protection endpoints:</span></span>

  - `https://api.aadrm.com` <span data-ttu-id="dd96d-132">(для большинства клиентов)</span><span class="sxs-lookup"><span data-stu-id="dd96d-132">(for most tenants)</span></span>
  - `https://api.aadrm.de` <span data-ttu-id="dd96d-133">(для клиентов в Германии)</span><span class="sxs-lookup"><span data-stu-id="dd96d-133">(for tenants in Germany)</span></span>
  - `https://api.aadrm.cn` <span data-ttu-id="dd96d-134">(для клиентов в Китае)</span><span class="sxs-lookup"><span data-stu-id="dd96d-134">(for tenants in China)</span></span>

- [<span data-ttu-id="dd96d-135">Конечные точки службы уведомлений Windows</span><span class="sxs-lookup"><span data-stu-id="dd96d-135">Windows Notification Service endpoints</span></span>](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

## <span data-ttu-id="dd96d-136">Другие службы для обеспечения поддержи работы браузера</span><span class="sxs-lookup"><span data-stu-id="dd96d-136">Other browser support services</span></span>

<span data-ttu-id="dd96d-137">Предоставьте метаданные для компонентов браузера, таких как защита от слежения, списки отзыва сертификатов и других обновлений компонентов браузера.</span><span class="sxs-lookup"><span data-stu-id="dd96d-137">Provide metadata for browser features such as tracking protection, certificate revocation lists, and other browser component updates.</span></span> <span data-ttu-id="dd96d-138">Предоставьте загружаемые словари для проверки правописания и списки блокировки рекламы.</span><span class="sxs-lookup"><span data-stu-id="dd96d-138">Provide downloadable spellcheck dictionaries and ad-blocking block lists.</span></span> <span data-ttu-id="dd96d-139">Предоставьте службы для поддержки работы функций браузера, таких как коллекции, автозаполнение и хранилище расширений.</span><span class="sxs-lookup"><span data-stu-id="dd96d-139">Provide services to support browser features such as collections, autofill, and extension store.</span></span>

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## <span data-ttu-id="dd96d-140">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="dd96d-140">See also</span></span>

- [<span data-ttu-id="dd96d-141">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="dd96d-141">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="dd96d-142">Целевая страница с документацией по Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="dd96d-142">Microsoft Edge documentation landing page</span></span>](https://docs.microsoft.com/DeployEdge/)
- [<span data-ttu-id="dd96d-143">Управление конечными точками подключений для Windows 10 Корпоративная, версия 1903</span><span class="sxs-lookup"><span data-stu-id="dd96d-143">Manage connection endpoints for Windows 10 Enterprise, version 1903</span></span>](https://docs.microsoft.com/windows/privacy/manage-windows-1903-endpoints)
