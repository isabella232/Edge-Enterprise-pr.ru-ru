---
title: Развертывание Microsoft Edge с обновлениями Windows 10
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Развертывание Microsoft Edge с обновлениями Windows 10
ms.openlocfilehash: 8ef5bd79059f31eb368a415ccca456fcea43788aed5738ed626a476b71a7d1ad
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "11726182"
---
# <a name="deploy-microsoft-edge-with-windows-10-updates"></a>Развертывание Microsoft Edge с обновлениями Windows 10

В этой статье содержатся сведения для пользователей, развертывающих Microsoft Edge с помощью обновлений Windows 10.

## <a name="for-windows-10-release-20h2"></a>Для выпуска Windows 10 20H2

В Windows 10 версии 20H2 в качестве браузера по умолчанию уже установлен Microsoft Edge.

## <a name="for-windows-10-releases-rs4-through-20h1"></a>Для выпусков Windows 10 RS4-20H1

Службы Windows Server Update Services (WSUS) имеют обновления для каждой версии Windows 10 с RS4 по 20H1. Эти обновления удалят классическое приложение Microsoft Edge Legacy и заменит его на Microsoft Edge. Дополнительные сведения, которые позволят определить, какое обновление WSUS подойдет для вашей версии Windows, см. [в этой статье](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c).

## <a name="for-windows-10-releases-prior-to-rs4-and-windows-7-81-and-earlier"></a>Для выпусков Windows 10 до RS4 (а также Windows 7, 8.1 и более ранних версий)

Обновления Windows для установки Microsoft Edge недоступны для этих версий. Рассмотрите другие варианты развертывания Microsoft Edge на этих устройствах, такие как [диспетчер конфигураций](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) или [Intune.](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Планирование развертывания Microsoft Edge](deploy-edge-plan-deployment.md)