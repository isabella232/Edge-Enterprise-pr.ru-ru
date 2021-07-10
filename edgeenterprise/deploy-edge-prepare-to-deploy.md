---
title: Microsoft Edge в вашей среде
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge в вашей среде
ms.openlocfilehash: 2381380cb399f6a1fbb5efa9378ffeba20fa774f
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641605"
---
# <a name="microsoft-edge-in-your-environment"></a><span data-ttu-id="f983d-103">Microsoft Edge в вашей среде</span><span class="sxs-lookup"><span data-stu-id="f983d-103">Microsoft Edge in your environment</span></span>

<span data-ttu-id="f983d-104">В этой статье описывается, как подготовиться к развертыванию Microsoft Edge, когда устаревшая версия Microsoft Edge завершит службу.</span><span class="sxs-lookup"><span data-stu-id="f983d-104">This article describes how to prepare to deploy Microsoft Edge when Microsoft Edge Legacy reaches its end of service.</span></span>

<span data-ttu-id="f983d-105">Как было объявлено в [записи блога](https://aka.ms/EdgeLegacyEOS) группы по продуктам Microsoft Edge, поддержка устаревшей версии Microsoft Edge для настольных компьютеров завершится 9 марта 2021 г.</span><span class="sxs-lookup"><span data-stu-id="f983d-105">As per the Microsoft Edge Product Team’s [blog post](https://aka.ms/EdgeLegacyEOS), support for the Microsoft Edge Legacy desktop application will end on March 9, 2021.</span></span> <span data-ttu-id="f983d-106">Апрельский выпуск вторничного обновления (или "B") удалит устаревшую версию Microsoft Edge с устройств под управлением Windows 10 (версий начиная с RS4 и по 20H1) и заменит ее на Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f983d-106">When you apply the Update Tuesday (or "B") release in April, it will remove Microsoft Edge Legacy from devices running Windows 10 RS4 through 20H1 and replace it with Microsoft Edge.</span></span>

## <a name="how-to-prepare"></a><span data-ttu-id="f983d-107">Подготовка</span><span class="sxs-lookup"><span data-stu-id="f983d-107">How to Prepare</span></span>

<span data-ttu-id="f983d-108">Чтобы подготовиться к установке Microsoft Edge на устройствах с Windows 10 RS4-20H1 вторничным обновлением в апреле, рекомендуем прочитать статью [Планирование развертывания Microsoft Edge](deploy-edge-plan-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="f983d-108">To prepare for Microsoft Edge being installed on Windows 10 RS4 through 20H1 devices with the Update Tuesday release in April, we recommend reading [Plan your deployment of Microsoft Edge](deploy-edge-plan-deployment.md).</span></span>

<span data-ttu-id="f983d-109">Составив план развертывания, используйте один из следующих подходов для подготовки к развертыванию Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f983d-109">After you plan your deployment, use one of the following approaches to prepare to deploy Microsoft Edge.</span></span>

- <span data-ttu-id="f983d-110">**Установите групповые политики для настройки подхода к обновлению Microsoft Edge.**</span><span class="sxs-lookup"><span data-stu-id="f983d-110">**Install group policies to customize your Microsoft Edge update approach**.</span></span> <span data-ttu-id="f983d-111">Дополнительные сведения см. в [справке по настройке параметров политики Microsoft Edge в Windows](configure-microsoft-edge.md). Обратите особое внимание на [справочные материалы по политике обновления](microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="f983d-111">For more information, see [Configure Microsoft Edge policy settings on Windows](configure-microsoft-edge.md), and pay special attention to the [Update Policy reference](microsoft-edge-update-policies.md) material.</span></span> <span data-ttu-id="f983d-112">Если установить групповые политики для управления обновлениями до установки апрельского вторничного обновления, Microsoft Edge сразу же начнет соблюдать вашу политику.</span><span class="sxs-lookup"><span data-stu-id="f983d-112">If you install group policies to manage your updates before installing April’s Update Tuesday release, Microsoft Edge will immediately start respecting your policy.</span></span> <span data-ttu-id="f983d-113">Если никакая групповая политика не установлена, Microsoft Edge автоматически обновится.</span><span class="sxs-lookup"><span data-stu-id="f983d-113">If there isn't any installed group policy, Microsoft Edge will automatically update itself.</span></span>

- <span data-ttu-id="f983d-114">**Удалите настольное приложение устаревшей версии Microsoft Edge до даты окончания ее службы 9 марта 2021г. и разверните Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="f983d-114">**Remove the Microsoft Edge Legacy desktop application before its end of service date of March 9, 2021 and deploy Microsoft Edge**.</span></span> <span data-ttu-id="f983d-115">Для Windows 10 RS4-20H1 это можно сделать с помощью Обновлений Windows.</span><span class="sxs-lookup"><span data-stu-id="f983d-115">For Windows 10 RS4 through 20H1, you can do this by using Windows Updates.</span></span> <span data-ttu-id="f983d-116">Дополнительные сведения см. в статье [Развертывание Microsoft Edge с обновлениями Windows 10](deploy-edge-with-windows-10-updates.md).</span><span class="sxs-lookup"><span data-stu-id="f983d-116">For more information, see [Deploy Microsoft Edge with Windows 10 updates](deploy-edge-with-windows-10-updates.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f983d-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f983d-117">See also</span></span>

- [<span data-ttu-id="f983d-118">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="f983d-118">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="f983d-119">Планирование развертывания Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f983d-119">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)