---
title: Конфигурации и эксперименты Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Конфигурации и эксперименты Microsoft Edge
ms.openlocfilehash: 1ebfe5fc1da107aa7e9e20b629f14aff468bdd6d
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641565"
---
# <a name="microsoft-edge-configurations-and-experimentation"></a><span data-ttu-id="971cf-103">Конфигурации и эксперименты Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="971cf-103">Microsoft Edge configurations and experimentation</span></span>

<span data-ttu-id="971cf-104">В этой статье описывается взаимодействие между Microsoft Edge и службой экспериментирования и настройки (ECS).</span><span class="sxs-lookup"><span data-stu-id="971cf-104">This article describes the interaction between Microsoft Edge and the Experimentation and Configuration Service (ECS).</span></span> <span data-ttu-id="971cf-105">Microsoft Edge обменивается данными с этой службой, чтобы запрашивать и получать различные типы полезных данных.</span><span class="sxs-lookup"><span data-stu-id="971cf-105">Microsoft Edge communicates with this service to request and receive different kinds of payloads.</span></span> <span data-ttu-id="971cf-106">Эти полезные данные включают в себя конфигурации, развертывания компонентов и эксперименты.</span><span class="sxs-lookup"><span data-stu-id="971cf-106">These payloads include configurations, feature rollouts, and experiments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="971cf-107">Убедитесь, что клиенты могут получить доступ к `https://config.edge.skype.com`, чтобы получать полезные данные.</span><span class="sxs-lookup"><span data-stu-id="971cf-107">Make sure clients are able to access `https://config.edge.skype.com` so payloads can be received.</span></span>

> [!NOTE]
> <span data-ttu-id="971cf-108">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="971cf-108">This applies to Microsoft Edge version 77 or later.</span></span>

## <a name="configurations"></a><span data-ttu-id="971cf-109">Конфигурации</span><span class="sxs-lookup"><span data-stu-id="971cf-109">Configurations</span></span>

<span data-ttu-id="971cf-110">Конфигурации — это полезная нагрузка, используемая для обеспечения работоспособности, безопасности, соответствия требованиям конфиденциальности и предоставления одинаковых значений всем пользователям (на основе платформ и каналов). Ее можно использовать для включения флага компонента для действия домена, а также для отключения флага компонента в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="971cf-110">Configurations are the payload meant to ensure product health, security, and privacy compliance, and are intended to have the same value for all the users (based on platforms and channels.) This could be to enable a feature flag for a domain action, and can also be used to disable a feature flag in the event of a bug.</span></span>

## <a name="controlled-feature-rollout"></a><span data-ttu-id="971cf-111">Контролируемый выпуск компонентов</span><span class="sxs-lookup"><span data-stu-id="971cf-111">Controlled Feature Rollout</span></span>

<span data-ttu-id="971cf-112">Контролируемый выпуск компонентов (CFR) — это процедура медленного увеличения размера группы пользователей, получающей компонент.</span><span class="sxs-lookup"><span data-stu-id="971cf-112">Controlled Feature Rollout (CFR) is a procedure for slowly increasing the size of the user group that receives a feature.</span></span> <span data-ttu-id="971cf-113">Распространение нового компонента среди выбранной случайным образом части пользователей позволяет сравнить отзывы пользователей с контрольной группой такого же размера без этого компонента, чтобы оценить влияние компонента.</span><span class="sxs-lookup"><span data-stu-id="971cf-113">By distributing a new feature to a randomly selected subset of the user population, it’s possible to compare user feedback to an equally sized control group without the feature to measure the impact of the feature.</span></span>

## <a name="experiments"></a><span data-ttu-id="971cf-114">Эксперименты</span><span class="sxs-lookup"><span data-stu-id="971cf-114">Experiments</span></span>

<span data-ttu-id="971cf-115">В сборах Microsoft Edge есть компоненты и функции, которые все еще находятся в разработке или являются экспериментальными.</span><span class="sxs-lookup"><span data-stu-id="971cf-115">Microsoft Edge builds have features and functionality that are still in development or are experimental.</span></span> <span data-ttu-id="971cf-116">Эксперименты похожи на CFR, но для тестирования новой концепции используется группа пользователей гораздо меньшего размера.</span><span class="sxs-lookup"><span data-stu-id="971cf-116">Experiments are like CFR, but the size of the user group is much smaller for testing the new concept.</span></span> <span data-ttu-id="971cf-117">Эти компоненты по умолчанию скрыты до их выпуска или завершения эксперимента.</span><span class="sxs-lookup"><span data-stu-id="971cf-117">These features are hidden by default until the feature's rolled out or the experiment's finished.</span></span> <span data-ttu-id="971cf-118">Для включения и отключения этих компонентов используются флаги эксперимента.</span><span class="sxs-lookup"><span data-stu-id="971cf-118">Experiment flags are used to enable and disable these features.</span></span>

## <a name="about-the-ecs"></a><span data-ttu-id="971cf-119">Сведения о службе ECS</span><span class="sxs-lookup"><span data-stu-id="971cf-119">About the ECS</span></span>

<span data-ttu-id="971cf-120">Во всех указанных выше сценариях служба предоставляет значения флагов компонентов клиенту браузера, чтобы их можно было применить.</span><span class="sxs-lookup"><span data-stu-id="971cf-120">In all the preceding scenarios, the service delivers the feature flag values to the browser client so they can be applied.</span></span> <span data-ttu-id="971cf-121">В зависимости от обновления конфигурации применяются сразу или при перезапуске браузера пользователем.</span><span class="sxs-lookup"><span data-stu-id="971cf-121">Depending on the update, configurations are applied immediately or when the user restarts the browser.</span></span>

<span data-ttu-id="971cf-122">Взаимодействие Microsoft Edge с этой службой управляется параметрами в политике [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol).</span><span class="sxs-lookup"><span data-stu-id="971cf-122">Microsoft Edge's interaction with this service is controlled by settings in the [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol) policy.</span></span> <span data-ttu-id="971cf-123">Параметры политики можно настраивать, чтобы:</span><span class="sxs-lookup"><span data-stu-id="971cf-123">You can configure policy settings to:</span></span>

- <span data-ttu-id="971cf-124">Получать только конфигурации</span><span class="sxs-lookup"><span data-stu-id="971cf-124">Retrieve configurations only</span></span>
- <span data-ttu-id="971cf-125">Получать конфигурации и эксперименты</span><span class="sxs-lookup"><span data-stu-id="971cf-125">Retrieve configurations and experiments</span></span>
- <span data-ttu-id="971cf-126">Отключение связи со службой</span><span class="sxs-lookup"><span data-stu-id="971cf-126">Disable communication with the service</span></span>

  > [!CAUTION]
  > <span data-ttu-id="971cf-127">Если вы отключите связь со службой, это повлияет на возможность корпорации Майкрософт своевременно реагировать на серьезные ошибки.</span><span class="sxs-lookup"><span data-stu-id="971cf-127">If you disable communications with the service, this will affect Microsoft’s ability to respond to a severe bug in a timely manner.</span></span>

## <a name="see-also"></a><span data-ttu-id="971cf-128">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="971cf-128">See also</span></span>

- [<span data-ttu-id="971cf-129">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="971cf-129">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="971cf-130">Целевая страница с документацией по Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="971cf-130">Microsoft Edge documentation landing page</span></span>](./index.yml)