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
# Список разрешений для конечных точек Microsoft Edge

Для работы этих функций в Microsoft Edge требуется подключение к Интернету. В этой статье указаны URL-адреса доменов, которые необходимо добавить в список разрешений для обеспечения взаимодействия через брандмауэры и другие механизмы защиты.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## URL-адреса доменов, которые необходимо добавить в список разрешений

Разрешите следующие URL-адреса доменов для Microsoft Edge.

### Служба обновления

Служба, которую Microsoft Edge использует для проверки наличия новых обновлений.

- `https://msedge.api.cdp.microsoft.com`

### Служба экспериментов и конфигураций

- `https://config.edge.skype.com`

### Расположения загрузки для Microsoft Edge

Расположения Microsoft Edge можно скачать во время начальной установки или при появлении обновления. Расположение для загрузки определяется службой обновления.

#### HTTP

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### HTTPS

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Чтобы упростить список разрешений для расположений загрузки, можно использовать подстановочный знак. `*.dl.delivery.mp.microsoft.com`

### Расположения загрузки для расширений Microsoft Edge

Расположения для расширений Microsoft Edge можно скачать во время начальной установки или при появлении обновления. Расположение для загрузки определяется службой обновления.

#### HTTP

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### HTTPS

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > Чтобы упростить список разрешений для расположений загрузки, можно использовать подстановочный знак. `*.dl.delivery.mp.microsoft.com`

### Дополнительно для оптимизации доставки загрузки

Сведения об оптимизации доставки см. в разделе [Оптимизация доставки обновлений Windows 10](https://aka.ms/waas-do).

- Обмен данными между клиентом и службой: `*.do.dsp.mp.microsoft.com` (HTTP-порт 80, HTTPS-порт 443)
- Обмен данными между клиентами: TCP-порт 7680 должен быть открыт для входящего трафика

### Sync

Эти конечные точки управляют чтением и записью синхронизированных данных, управлением правами для безопасных данных, а также уведомлением браузера о доступности новых синхронизированных данных.

- Конечные точки службы синхронизации Microsoft Edge:

  - `https://edge-enterprise.activity.windows.com`
  - `https://edge.activity.windows.com`

- Конечные точки Azure Information Protection:

  - `https://api.aadrm.com` (для большинства клиентов)
  - `https://api.aadrm.de` (для клиентов в Германии)
  - `https://api.aadrm.cn` (для клиентов в Китае)

- [Конечные точки службы уведомлений Windows](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

## Другие службы для обеспечения поддержи работы браузера

Предоставьте метаданные для компонентов браузера, таких как защита от слежения, списки отзыва сертификатов и других обновлений компонентов браузера. Предоставьте загружаемые словари для проверки правописания и списки блокировки рекламы. Предоставьте службы для поддержки работы функций браузера, таких как коллекции, автозаполнение и хранилище расширений.

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## Статьи по теме

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Целевая страница с документацией по Microsoft Edge Enterprise](https://docs.microsoft.com/DeployEdge/)
- [Управление конечными точками подключений для Windows 10 Корпоративная, версия 1903](https://docs.microsoft.com/windows/privacy/manage-windows-1903-endpoints)
