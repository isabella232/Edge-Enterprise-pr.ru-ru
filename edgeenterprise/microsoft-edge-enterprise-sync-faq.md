---
title: Вопросы и ответы о синхронизации Microsoft Edge для предприятий
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Вопросы и ответы о синхронизации Microsoft Edge для предприятий.
ms.openlocfilehash: 4bb41c8d7ded64fcc0b4fd4843ef2b7ec0adec23
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617769"
---
# <a name="microsoft-edge-enterprise-sync-faq"></a><span data-ttu-id="52304-103">Вопросы и ответы о синхронизации Microsoft Edge для предприятий</span><span class="sxs-lookup"><span data-stu-id="52304-103">Microsoft Edge enterprise sync FAQ</span></span>

<span data-ttu-id="52304-104">В этой статье содержатся ответы на самые популярные вопросы о синхронизации Microsoft Edge версии 77 или более поздней для предприятий.</span><span class="sxs-lookup"><span data-stu-id="52304-104">This article answers frequently asked questions about enterprise sync for Microsoft Edge version 77 or later.</span></span>

## <a name="security-and-serverdata-compliance"></a><span data-ttu-id="52304-105">Безопасность и соответствие сервера/данных</span><span class="sxs-lookup"><span data-stu-id="52304-105">Security and Server/Data Compliance</span></span>

### <a name="is-the-synced-data-encrypted"></a><span data-ttu-id="52304-106">Шифруются ли синхронизированные данные?</span><span class="sxs-lookup"><span data-stu-id="52304-106">Is the synced data encrypted?</span></span>

<span data-ttu-id="52304-107">Данные шифруются в процессе транспортировки с использованием протокола TLS 1.2 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="52304-107">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="52304-108">Все типы данных дополнительно шифруются в службе Майкрософт с помощью AES128.</span><span class="sxs-lookup"><span data-stu-id="52304-108">All data types are additionally encrypted at rest in Microsoft's service using AES128.</span></span> <span data-ttu-id="52304-109">Все типы данных, кроме используемых для синхронизации открытой вкладки и журнала, дополнительно шифруются перед покиданием устройства пользователя с использованием ключей, управляемых с помощью политики [Azure Information Protection](./microsoft-edge-policies.md#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="52304-109">All data types except those used for open tab and history sync are additionally encrypted before leaving the user’s device with keys managed via the [Azure Information Protection](./microsoft-edge-policies.md#restrictsignintopattern) policy.</span></span>

### <a name="why-dont-open-tab-and-history-data-have-more-client-side-encryption"></a><span data-ttu-id="52304-110">Почему данные открытой вкладки и журнала не используют дополнительное шифрование на стороне клиента?</span><span class="sxs-lookup"><span data-stu-id="52304-110">Why don’t open tab and history data have more client-side encryption?</span></span>

<span data-ttu-id="52304-111">Чтобы сократить использование ресурсов на устройствах конечных пользователей, данные журнала создаются на стороне сервера на основе перемещаемых данных открытой вкладки.</span><span class="sxs-lookup"><span data-stu-id="52304-111">To reduce resource utilization on end-user devices, history data is generated server-side based on open tab roaming data.</span></span> <span data-ttu-id="52304-112">Этот процесс невозможен при шифровании этих данных на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="52304-112">This process would not be possible with client-side encryption of this data.</span></span> <span data-ttu-id="52304-113">Чтобы отключить синхронизацию открытой вкладки и журнала, примените политику [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) или [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled).</span><span class="sxs-lookup"><span data-stu-id="52304-113">To disable open tab and history sync, apply the [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) or [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) policies.</span></span>

### <a name="can-tenant-admins-bring-their-own-key"></a><span data-ttu-id="52304-114">Могут ли администраторы клиента использовать свой ключ?</span><span class="sxs-lookup"><span data-stu-id="52304-114">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="52304-115">Да, с помощью  [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="52304-115">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

### <a name="where-is-microsoft-edge-sync-data-stored"></a><span data-ttu-id="52304-116">Где хранятся данные синхронизации Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="52304-116">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="52304-117">Синхронизированные данные учетных записей Azure AD хранятся на защищенных серверах в соответствии с идентификатором клиента.</span><span class="sxs-lookup"><span data-stu-id="52304-117">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="52304-118">Например, данные клиента, зарегистрированного в США, хранятся на серверах, расположенных в этом географическом регионе, и к ним применяется то же самое решение для хранения, что и к приложениям Office.</span><span class="sxs-lookup"><span data-stu-id="52304-118">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

### <a name="does-the-data-ever-leave-microsofts-cloud-aside-from-syncing-to-microsoft-edge"></a><span data-ttu-id="52304-119">Выходят ли данные за пределы облака Майкрософт помимо синхронизации с Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="52304-119">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="52304-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="52304-120">No.</span></span>

### <a name="what-terms-of-service-does-enterprise-sync-fall-under"></a><span data-ttu-id="52304-121">Каковы условия использования синхронизации в корпоративной среде?</span><span class="sxs-lookup"><span data-stu-id="52304-121">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="52304-122">Условия использования функции синхронизации Microsoft Edge регулируются лицензией на программное обеспечение корпорации Майкрософт, с которой можно ознакомиться в Microsoft Edge по адресу  *edge://terms*.</span><span class="sxs-lookup"><span data-stu-id="52304-122">Terms of service for Microsoft Edge sync falls under the Microsoft software license viewable in Microsoft Edge at *edge://terms*.</span></span> <span data-ttu-id="52304-123">Ваша подписка на Azure AD и условия обслуживания в конечном итоге регулируются [условиями использования веб-служб](https://www.microsoft.com/licensing/product-licensing/products) Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="52304-123">Your Azure AD subscription and terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

### <a name="does-microsoft-edge-support-government-community-cloud-gcc-high-compliance"></a><span data-ttu-id="52304-124">Поддерживает ли Microsoft Edge стандарты соответствия требованиям облака сообщества для государственных организаций (GCC High)?</span><span class="sxs-lookup"><span data-stu-id="52304-124">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="52304-125">Еще нет.</span><span class="sxs-lookup"><span data-stu-id="52304-125">Not today.</span></span> <span data-ttu-id="52304-126">Для клиентов в облаке GCC High синхронизация Microsoft Edge отключена.</span><span class="sxs-lookup"><span data-stu-id="52304-126">For customers in the GCC High cloud, Microsoft Edge sync is disabled.</span></span>

## <a name="applying-sync"></a><span data-ttu-id="52304-127">Применение синхронизации</span><span class="sxs-lookup"><span data-stu-id="52304-127">Applying Sync</span></span>

### <a name="why-isnt-microsoft-edge-sync-supported-in-all-m365-subscriptions"></a><span data-ttu-id="52304-128">Почему синхронизация Microsoft Edge не поддерживается во всех подписках M365?</span><span class="sxs-lookup"><span data-stu-id="52304-128">Why isn’t Microsoft Edge sync supported in all M365 subscriptions?</span></span>

<span data-ttu-id="52304-129">Синхронизация в корпоративной среде зависит от службы [Azure Information Protection](https://azure.microsoft.com/services/information-protection/), которая доступна не во всех подписках M365.</span><span class="sxs-lookup"><span data-stu-id="52304-129">Enterprise sync depends on [Azure Information Protection](https://azure.microsoft.com/services/information-protection/), which is not available in all M365 subscriptions.</span></span>

### <a name="is-microsoft-edge-sync-based-on-enterprise-state-roaming"></a><span data-ttu-id="52304-130">Основана ли функция синхронизации Microsoft Edge на Enterprise State Roaming?</span><span class="sxs-lookup"><span data-stu-id="52304-130">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="52304-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="52304-131">No.</span></span> <span data-ttu-id="52304-132">ESR может использоваться для включения синхронизации, но функция синхронизации Microsoft Edge не входит в состав ESR.</span><span class="sxs-lookup"><span data-stu-id="52304-132">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="52304-133">Дополнительные сведения см. в разделах [Функция синхронизации Microsoft Edge](/DeployEdge/microsoft-edge-enterprise-sync) и [Microsoft Edge и Enterprise State Roaming](/DeployEdge/microsoft-edge-enterprise-state-roaming).</span><span class="sxs-lookup"><span data-stu-id="52304-133">For more information, see [Microsoft Edge Sync](/DeployEdge/microsoft-edge-enterprise-sync) and [Microsoft Edge and Enterprise State Roaming](/DeployEdge/microsoft-edge-enterprise-state-roaming).</span></span>

### <a name="will-microsoft-edge-ever-support-syncing-between-microsoft-edge-and-ie"></a><span data-ttu-id="52304-134">Будет ли Microsoft Edge поддерживать синхронизацию между Microsoft Edge и IE?</span><span class="sxs-lookup"><span data-stu-id="52304-134">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="52304-135">Поддержка такой синхронизации не планируется.</span><span class="sxs-lookup"><span data-stu-id="52304-135">There are no plans to support this syncing.</span></span> <span data-ttu-id="52304-136">Если для поддержки устаревших приложений вам нужен IE, подумайте об использовании [нового режима IE](./edge-ie-mode.md).</span><span class="sxs-lookup"><span data-stu-id="52304-136">If you still need IE in your environment to support legacy apps, consider our [new IE mode](./edge-ie-mode.md).</span></span>

### <a name="will-microsoft-edge-sync-with-microsoft-edge-legacy"></a><span data-ttu-id="52304-137">Будет ли Microsoft Edge синхронизироваться с устаревшей версией Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="52304-137">Will Microsoft Edge sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="52304-138">Нет, не будет.</span><span class="sxs-lookup"><span data-stu-id="52304-138">No, it won't.</span></span> <span data-ttu-id="52304-139">Мы считаем, что объединение этих двух экосистем может привести к нарушению надежности синхронизации в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="52304-139">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the Microsoft Edge.</span></span> <span data-ttu-id="52304-140">Мы обеспечим перенос имеющихся данных в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="52304-140">We will ensure that existing data is migrated to the Microsoft Edge.</span></span> <span data-ttu-id="52304-141">Пользователи также смогут импортировать данные из браузера по своему выбору, что также означает, что Microsoft Edge не сможет синхронизироваться с Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="52304-141">Users will also be able to import data from browser of their choice, which also means that Microsoft Edge won't have a way to sync with IE.</span></span>

## <a name="managing-sync"></a><span data-ttu-id="52304-142">Управление синхронизацией</span><span class="sxs-lookup"><span data-stu-id="52304-142">Managing Sync</span></span>

### <a name="is-it-possible-to-stop-my-users-from-syncing-with-a-personal-tenant"></a><span data-ttu-id="52304-143">Можно ли запретить пользователям синхронизацию с личным клиентом?</span><span class="sxs-lookup"><span data-stu-id="52304-143">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="52304-144">Прямо нет, но вы можете определить, с каким профилем можно входить в Microsoft Edge, с помощью политики [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="52304-144">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern) policy.</span></span>

## <a name="see-also"></a><span data-ttu-id="52304-145">См. также</span><span class="sxs-lookup"><span data-stu-id="52304-145">See also</span></span>

- [<span data-ttu-id="52304-146">Синхронизация Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="52304-146">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="52304-147">Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="52304-147">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="52304-148">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="52304-148">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)