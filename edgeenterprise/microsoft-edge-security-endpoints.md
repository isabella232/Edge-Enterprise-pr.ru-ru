---
title: Список разрешений для конечных точек Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Список разрешений для конечных точек Microsoft Edge
ms.openlocfilehash: 735e18e63095405dad4fdd51d51654956b564ca7
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641335"
---
# <a name="allow-list-for-microsoft-edge-endpoints"></a><span data-ttu-id="46ab7-103">Список разрешений для конечных точек Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="46ab7-103">Allow list for Microsoft Edge endpoints</span></span>

<span data-ttu-id="46ab7-104">Для работы этих функций в Microsoft Edge требуется подключение к Интернету.</span><span class="sxs-lookup"><span data-stu-id="46ab7-104">Microsoft Edge requires connectivity to the Internet to support its features.</span></span> <span data-ttu-id="46ab7-105">В этой статье указаны URL-адреса доменов, которые необходимо добавить в список разрешений для обеспечения взаимодействия через брандмауэры и другие механизмы защиты.</span><span class="sxs-lookup"><span data-stu-id="46ab7-105">This article identifies the domain URLs that you need to add to the Allow list to ensure communications through firewalls and other security mechanisms.</span></span>

> [!NOTE]
> <span data-ttu-id="46ab7-106">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="46ab7-106">This applies  to Microsoft Edge version 77 or later.</span></span>

## <a name="domain-urls-to-allow"></a><span data-ttu-id="46ab7-107">URL-адреса доменов, которые необходимо добавить в список разрешений</span><span class="sxs-lookup"><span data-stu-id="46ab7-107">Domain URLs to allow</span></span>

<span data-ttu-id="46ab7-108">Разрешите следующие URL-адреса доменов для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="46ab7-108">Allow the following domain URLs for Microsoft Edge.</span></span>

### <a name="update-service"></a><span data-ttu-id="46ab7-109">Служба обновления</span><span class="sxs-lookup"><span data-stu-id="46ab7-109">Update Service</span></span>

<span data-ttu-id="46ab7-110">Служба, которую Microsoft Edge использует для проверки наличия новых обновлений.</span><span class="sxs-lookup"><span data-stu-id="46ab7-110">The service that Microsoft Edge uses to check for new updates.</span></span>

- `https://msedge.api.cdp.microsoft.com`

### <a name="experimentation-and-configuration-service"></a><span data-ttu-id="46ab7-111">Служба экспериментов и конфигураций</span><span class="sxs-lookup"><span data-stu-id="46ab7-111">Experimentation and Configuration service</span></span>

- `https://config.edge.skype.com`

### <a name="download-locations-for-microsoft-edge"></a><span data-ttu-id="46ab7-112">Расположения загрузки для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="46ab7-112">Download locations for Microsoft Edge</span></span>

<span data-ttu-id="46ab7-113">Расположения Microsoft Edge можно скачать во время начальной установки или при появлении обновления.</span><span class="sxs-lookup"><span data-stu-id="46ab7-113">Locations Microsoft Edge can be downloaded from during an initial install or when an update is available.</span></span> <span data-ttu-id="46ab7-114">Расположение для загрузки определяется службой обновления.</span><span class="sxs-lookup"><span data-stu-id="46ab7-114">The download location is determined by the Update Service.</span></span>

#### <a name="http"></a><span data-ttu-id="46ab7-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="46ab7-115">HTTP</span></span>

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### <a name="https"></a><span data-ttu-id="46ab7-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="46ab7-116">HTTPS</span></span>

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > <span data-ttu-id="46ab7-117">Чтобы упростить список разрешений для расположений загрузки, можно использовать подстановочный знак.</span><span class="sxs-lookup"><span data-stu-id="46ab7-117">To simplify the allow list for download locations a wild card can be used:</span></span> `*.dl.delivery.mp.microsoft.com`

### <a name="download-locations-for-microsoft-edge-extensions"></a><span data-ttu-id="46ab7-118">Расположения загрузки для расширений Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="46ab7-118">Download locations for Microsoft Edge Extensions</span></span>

<span data-ttu-id="46ab7-119">Расположения для расширений Microsoft Edge можно скачать во время начальной установки или при появлении обновления.</span><span class="sxs-lookup"><span data-stu-id="46ab7-119">Locations Microsoft Edge Extensions can be downloaded from during an initial install or when an update is available.</span></span> <span data-ttu-id="46ab7-120">Расположение для загрузки определяется службой обновления.</span><span class="sxs-lookup"><span data-stu-id="46ab7-120">The download location is determined by the Update Service.</span></span>

#### <a name="http"></a><span data-ttu-id="46ab7-121">HTTP</span><span class="sxs-lookup"><span data-stu-id="46ab7-121">HTTP</span></span>

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### <a name="https"></a><span data-ttu-id="46ab7-122">HTTPS</span><span class="sxs-lookup"><span data-stu-id="46ab7-122">HTTPS</span></span>

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > <span data-ttu-id="46ab7-123">Чтобы упростить список разрешений для расположений загрузки, можно использовать подстановочный знак.</span><span class="sxs-lookup"><span data-stu-id="46ab7-123">To simplify the allow list for download locations a wild card can be used:</span></span> `*.dl.delivery.mp.microsoft.com`

### <a name="optionally-for-download-delivery-optimization"></a><span data-ttu-id="46ab7-124">Дополнительно для оптимизации доставки загрузки</span><span class="sxs-lookup"><span data-stu-id="46ab7-124">Optionally for Download Delivery Optimization</span></span>

<span data-ttu-id="46ab7-125">Сведения об оптимизации доставки см. в разделе [Оптимизация доставки обновлений Windows 10](/windows/deployment/update/waas-delivery-optimization).</span><span class="sxs-lookup"><span data-stu-id="46ab7-125">For information about delivery optimization, see [Delivery Optimization for Windows 10 updates](/windows/deployment/update/waas-delivery-optimization).</span></span>

- <span data-ttu-id="46ab7-126">Обмен данными между клиентом и службой: `*.do.dsp.mp.microsoft.com` (HTTP-порт 80, HTTPS-порт 443)</span><span class="sxs-lookup"><span data-stu-id="46ab7-126">Client to Service communication: `*.do.dsp.mp.microsoft.com` (HTTP Port 80, HTTPS Port 443)</span></span>
- <span data-ttu-id="46ab7-127">Обмен данными между клиентами: TCP-порт 7680 должен быть открыт для входящего трафика</span><span class="sxs-lookup"><span data-stu-id="46ab7-127">Client to Client communication: TCP port 7680 should be open for inbound traffic</span></span>

### <a name="sync"></a><span data-ttu-id="46ab7-128">Sync</span><span class="sxs-lookup"><span data-stu-id="46ab7-128">Sync</span></span>

<span data-ttu-id="46ab7-129">Эти конечные точки управляют чтением и записью синхронизированных данных, управлением правами для безопасных данных, а также уведомлением браузера о доступности новых синхронизированных данных.</span><span class="sxs-lookup"><span data-stu-id="46ab7-129">These endpoints manage the reading and writing of synced data, rights management for secure data, and notifying the browser when new sync data is available.</span></span>

- <span data-ttu-id="46ab7-130">Конечные точки службы синхронизации Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="46ab7-130">Edge sync service endpoints:</span></span>

  - `https://edge-enterprise.activity.windows.com`
  - `https://edge.activity.windows.com`

- <span data-ttu-id="46ab7-131">Конечные точки Azure Information Protection:</span><span class="sxs-lookup"><span data-stu-id="46ab7-131">Azure Information Protection endpoints:</span></span>

  - `https://api.aadrm.com` <span data-ttu-id="46ab7-132">(для большинства клиентов)</span><span class="sxs-lookup"><span data-stu-id="46ab7-132">(for most tenants)</span></span>
  - `https://api.aadrm.de` <span data-ttu-id="46ab7-133">(для клиентов в Германии)</span><span class="sxs-lookup"><span data-stu-id="46ab7-133">(for tenants in Germany)</span></span>
  - `https://api.aadrm.cn` <span data-ttu-id="46ab7-134">(для клиентов в Китае)</span><span class="sxs-lookup"><span data-stu-id="46ab7-134">(for tenants in China)</span></span>

- [<span data-ttu-id="46ab7-135">Конечные точки службы уведомлений Windows</span><span class="sxs-lookup"><span data-stu-id="46ab7-135">Windows Notification Service endpoints</span></span>](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

## <a name="other-browser-support-services"></a><span data-ttu-id="46ab7-136">Другие службы для обеспечения поддержи работы браузера</span><span class="sxs-lookup"><span data-stu-id="46ab7-136">Other browser support services</span></span>

<span data-ttu-id="46ab7-137">Предоставьте метаданные для компонентов браузера, таких как защита от слежения, списки отзыва сертификатов и других обновлений компонентов браузера.</span><span class="sxs-lookup"><span data-stu-id="46ab7-137">Provide metadata for browser features such as tracking protection, certificate revocation lists, and other browser component updates.</span></span> <span data-ttu-id="46ab7-138">Предоставьте загружаемые словари для проверки правописания и списки блокировки рекламы.</span><span class="sxs-lookup"><span data-stu-id="46ab7-138">Provide downloadable spellcheck dictionaries and ad-blocking block lists.</span></span> <span data-ttu-id="46ab7-139">Предоставьте службы для поддержки работы функций браузера, таких как коллекции, автозаполнение и хранилище расширений.</span><span class="sxs-lookup"><span data-stu-id="46ab7-139">Provide services to support browser features such as collections, autofill, and extension store.</span></span>

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## <a name="see-also"></a><span data-ttu-id="46ab7-140">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="46ab7-140">See also</span></span>

- [<span data-ttu-id="46ab7-141">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="46ab7-141">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="46ab7-142">Целевая страница с документацией по Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="46ab7-142">Microsoft Edge documentation landing page</span></span>](./index.yml)
- [<span data-ttu-id="46ab7-143">Управление конечными точками подключений для Windows 10 Корпоративная, версия 1903</span><span class="sxs-lookup"><span data-stu-id="46ab7-143">Manage connection endpoints for Windows 10 Enterprise, version 1903</span></span>](/windows/privacy/manage-windows-1903-endpoints)