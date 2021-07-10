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
# <a name="allow-list-for-microsoft-edge-endpoints"></a>Список разрешений для конечных точек Microsoft Edge

Для работы этих функций в Microsoft Edge требуется подключение к Интернету. В этой статье указаны URL-адреса доменов, которые необходимо добавить в список разрешений для обеспечения взаимодействия через брандмауэры и другие механизмы защиты.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## <a name="domain-urls-to-allow"></a>URL-адреса доменов, которые необходимо добавить в список разрешений

Разрешите следующие URL-адреса доменов для Microsoft Edge.

### <a name="update-service"></a>Служба обновления

Служба, которую Microsoft Edge использует для проверки наличия новых обновлений.

- `https://msedge.api.cdp.microsoft.com`

### <a name="experimentation-and-configuration-service"></a>Служба экспериментов и конфигураций

- `https://config.edge.skype.com`

### <a name="download-locations-for-microsoft-edge"></a>Расположения загрузки для Microsoft Edge

Расположения Microsoft Edge можно скачать во время начальной установки или при появлении обновления. Расположение для загрузки определяется службой обновления.

#### <a name="http"></a>HTTP

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### <a name="https"></a>HTTPS

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Чтобы упростить список разрешений для расположений загрузки, можно использовать подстановочный знак. `*.dl.delivery.mp.microsoft.com`

### <a name="download-locations-for-microsoft-edge-extensions"></a>Расположения загрузки для расширений Microsoft Edge

Расположения для расширений Microsoft Edge можно скачать во время начальной установки или при появлении обновления. Расположение для загрузки определяется службой обновления.

#### <a name="http"></a>HTTP

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### <a name="https"></a>HTTPS

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Чтобы упростить список разрешений для расположений загрузки, можно использовать подстановочный знак. `*.dl.delivery.mp.microsoft.com`

### <a name="optionally-for-download-delivery-optimization"></a>Дополнительно для оптимизации доставки загрузки

Сведения об оптимизации доставки см. в разделе [Оптимизация доставки обновлений Windows 10](/windows/deployment/update/waas-delivery-optimization).

- Обмен данными между клиентом и службой: `*.do.dsp.mp.microsoft.com` (HTTP-порт 80, HTTPS-порт 443)
- Обмен данными между клиентами: TCP-порт 7680 должен быть открыт для входящего трафика

### <a name="sync"></a>Sync

Эти конечные точки управляют чтением и записью синхронизированных данных, управлением правами для безопасных данных, а также уведомлением браузера о доступности новых синхронизированных данных.

- Конечные точки службы синхронизации Microsoft Edge:

  - `https://edge-enterprise.activity.windows.com`
  - `https://edge.activity.windows.com`

- Конечные точки Azure Information Protection:

  - `https://api.aadrm.com` (для большинства клиентов)
  - `https://api.aadrm.de` (для клиентов в Германии)
  - `https://api.aadrm.cn` (для клиентов в Китае)

- [Конечные точки службы уведомлений Windows](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

## <a name="other-browser-support-services"></a>Другие службы для обеспечения поддержи работы браузера

Предоставьте метаданные для компонентов браузера, таких как защита от слежения, списки отзыва сертификатов и других обновлений компонентов браузера. Предоставьте загружаемые словари для проверки правописания и списки блокировки рекламы. Предоставьте службы для поддержки работы функций браузера, таких как коллекции, автозаполнение и хранилище расширений.

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## <a name="see-also"></a>Статьи по теме

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Целевая страница с документацией по Microsoft Edge Enterprise](./index.yml)
- [Управление конечными точками подключений для Windows 10 Корпоративная, версия 1903](/windows/privacy/manage-windows-1903-endpoints)