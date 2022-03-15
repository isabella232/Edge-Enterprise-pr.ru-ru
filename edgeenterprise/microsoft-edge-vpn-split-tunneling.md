---
title: Microsoft Edge и поддержка VPN для раздельного туннеля для WebRTC
ms.author: juso
author: dan-wesley
manager: harneets
ms.date: 01/24/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Включить Microsoft Edge и разделять VPN-поддержку для WebRTC (веб-Real-Time связи)
ms.openlocfilehash: 73bd6494ebb95db23d2701cc9dab4023af28eb70
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445958"
---
# <a name="split-tunnel-vpn-support-for-webrtc-web-real-time-communication"></a>Поддержка VPN для раздельного туннеля для WebRTC (веб-Real-Time связи)
  
В этой статье описывается Microsoft Edge и поддержка VPN для раздельного туннеля для WebRTC. Эта поддержка позволяет корпоративным клиентам получать преимущества vpn-раздельного туннелинга для одноранговых трафика на Microsoft Edge. Разделение VPN-туннелей улучшает качество потоковой передачи мультимедиа между однорангами для пользователей и снижает нагрузку на vpn-сервер.

> [!NOTE]
> Эта статья применима к Microsoft Edge версии 96 или более поздней версии.

## <a name="what-is-vpn-split-tunneling-and-why-should-i-use-it"></a>Что такое раздельный vpn-туннель и зачем его использовать?

VPN split tunneling is a feature that enables users to use two different networks for traffic instead of having all the traffic routed through a VPN. Windows поддерживает эту функцию для отечественных приложений, а для приложений Microsoft 365 для сплит-туннеля VPN Windows. Дополнительные сведения см. в [раздел Обзоре: разделяемая туннельная сеть VPN с Office 365 - Microsoft 365 корпоративный](/microsoft-365/enterprise/microsoft-365-vpn-split-tunnel?view=o365-worldwide&preserve-view=true). Microsoft Edge также удостоилась конфигурации vpn-раздельного туннеля, но поддержка одноранговых трафика отсутствовала.

Мы слышали о потребностях клиентов в маршрутике одноранговых пользовательских трафика через корпоративную сеть или облачную инфраструктуру через VPN.Они были разочарованы качеством видеоконференции пользователей в браузерах по сравнению с родными приложениями.Как показано на основе родного опыта, разделение VPN-тоннелей для одноранговых трафика может повысить качество видеозвонков пользователей, маршрутив его по обычным подключениям к Интернету вместо VPN. Это также может уменьшить общую загрузку VPN-сервера путем маршрутинга назначенного трафика от VPN. Microsoft Edge теперь это одноранговая улучшения трафика для корпоративных клиентов.

## <a name="how-to-configure-vpn-split-tunneling-on-microsoft-edge"></a>Настройка vpn-раздельного туннеля на Microsoft Edge

Чтобы включить vpn-раздельный туннель и настроить сети для пользователей, рекомендуем начать с руководства по внедрению [vpn-раздельного туннелинга для Office 365 - Microsoft 365 корпоративный](/microsoft-365/enterprise/microsoft-365-vpn-implement-split-tunnel?view=o365-worldwide&preserve-view=true). С правильной таблицей маршрутов, настроенной на основе сведений, описанных в предыдущей статье, необходимо сделать дополнительный шаг, чтобы включить политику [WebRtcRespectOsRoutingTableEnabled](/deployedge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) . Эта политика позволяет поддерживать правила Windows маршрутивки ОС при создании одноранговых подключений через WebRTC. Теперь вы готовы предоставить улучшенный опыт одноранговой потоковой передачи мультимедиа на Microsoft Edge!

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
