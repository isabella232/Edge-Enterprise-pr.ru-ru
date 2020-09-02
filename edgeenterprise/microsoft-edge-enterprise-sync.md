---
title: Синхронизация Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 08/03/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Синхронизация Microsoft Edge Enterprise
ms.openlocfilehash: a6d01356db478871a7c6b386bbb731b32dc4739a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980967"
---
# <span data-ttu-id="043ef-103">Синхронизация Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="043ef-103">Microsoft Edge Enterprise Sync</span></span>

<span data-ttu-id="043ef-104">В этой статье объясняется, как использовать Microsoft Edge для синхронизации избранного, паролей и других данных браузера на всех устройствах, на которых выполнен вход пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="043ef-104">This article explains how to use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="043ef-105">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="043ef-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="043ef-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="043ef-106">Overview</span></span>

<span data-ttu-id="043ef-107">Функция синхронизации Microsoft Edge позволяет пользователям получать доступ к данным браузера на всех своих устройствах, на которых они выполняют вход в систему.</span><span class="sxs-lookup"><span data-stu-id="043ef-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="043ef-108">К данным, поддерживаемым функцией синхронизации, относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="043ef-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="043ef-109">Избранное</span><span class="sxs-lookup"><span data-stu-id="043ef-109">Favorites</span></span>
- <span data-ttu-id="043ef-110">Пароли</span><span class="sxs-lookup"><span data-stu-id="043ef-110">Passwords</span></span>
- <span data-ttu-id="043ef-111">Адреса и прочее (заполнения форм)</span><span class="sxs-lookup"><span data-stu-id="043ef-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="043ef-112">Коллекции</span><span class="sxs-lookup"><span data-stu-id="043ef-112">Collections</span></span>
- <span data-ttu-id="043ef-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="043ef-113">Settings</span></span>

<span data-ttu-id="043ef-114">Функция синхронизации включается путем предоставления пользователем согласия с этим действием. Пользователи могут включать или отключать синхронизацию для всех перечисленных выше типов данных.</span><span class="sxs-lookup"><span data-stu-id="043ef-114">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="043ef-115">Для обеспечения поддержки функции синхронизации передаются дополнительные данные о подключении устройства и данные конфигурации (например, имя устройства, изготовитель и модель).</span><span class="sxs-lookup"><span data-stu-id="043ef-115">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="043ef-116">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="043ef-116">Prerequisites</span></span>

<span data-ttu-id="043ef-117">Функция синхронизации Microsoft Edge для учетных записей Azure Active Directory (Azure AD) сейчас доступна в рамках следующих подписок:</span><span class="sxs-lookup"><span data-stu-id="043ef-117">Currently Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for the following subscriptions:</span></span>

- <span data-ttu-id="043ef-118">Azure AD Premium (P1 или P2)</span><span class="sxs-lookup"><span data-stu-id="043ef-118">Azure AD Premium (P1 and P2)</span></span>
- <span data-ttu-id="043ef-119">M365 бизнес премиум</span><span class="sxs-lookup"><span data-stu-id="043ef-119">M365 Business Premium</span></span>
- <span data-ttu-id="043ef-120">Office 365 E3 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="043ef-120">Office 365 E3 and above</span></span>
- <span data-ttu-id="043ef-121">Azure Information Protection (AIP) (P1 и P2)</span><span class="sxs-lookup"><span data-stu-id="043ef-121">Azure Information Protection (AIP) (P1& P2)</span></span>
- <span data-ttu-id="043ef-122">Все подписки EDU для образовательной сферы (O365 A1 или выше, M365 A1 или выше, либо Azure Information Protection P1 или P2 для учащихся и преподавателей)</span><span class="sxs-lookup"><span data-stu-id="043ef-122">All EDU subscriptions (O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

> [!NOTE]
> <span data-ttu-id="043ef-123">Синхронизация зависит от службы защиты, предлагаемой Azure Information Protection (AIP) для защиты данных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="043ef-123">Sync has a dependency on the protection service offered by Azure Information Protection (AIP) to protect sync data.</span></span> <span data-ttu-id="043ef-124">В настоящее время эта служба доступна для указанных выше подписок.</span><span class="sxs-lookup"><span data-stu-id="043ef-124">This service is currently available to the preceding subscriptions.</span></span> <span data-ttu-id="043ef-125">Полный список номеров SKU с AIP см. в разделе [Ценообразование на службы защиты информации](https://azure.microsoft.com/pricing/details/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="043ef-125">To see the full list of SKUs with AIP, see [Information Protection Pricing](https://azure.microsoft.com/pricing/details/information-protection/).</span></span>

## <span data-ttu-id="043ef-126">Параметры конфигурации для функции синхронизации Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="043ef-126">Configuration options for Microsoft Edge sync</span></span>

<span data-ttu-id="043ef-127">Для включения функции синхронизации Microsoft Edge доступны следующие параметры конфигурации:</span><span class="sxs-lookup"><span data-stu-id="043ef-127">The following configuration options are available for enabling Microsoft Edge sync:</span></span>

- <span data-ttu-id="043ef-128">Azure Information Protection (AIP)</span><span class="sxs-lookup"><span data-stu-id="043ef-128">Azure Information Protection (AIP)</span></span>
- <span data-ttu-id="043ef-129">Azure AD Enterprise State Roaming (ESR)</span><span class="sxs-lookup"><span data-stu-id="043ef-129">Azure AD Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="043ef-130">Если обе службы AIP и ESR отключены, то пользователи увидят сообщение об ошибке, указывающее на то, что синхронизация для их учетной записи недоступна.</span><span class="sxs-lookup"><span data-stu-id="043ef-130">If both AIP and ESR are disabled, users will see an error message indicating that sync is not available for their account.</span></span>

### <span data-ttu-id="043ef-131">Azure Information Protection (AIP)</span><span class="sxs-lookup"><span data-stu-id="043ef-131">Azure Information Protection (AIP)</span></span>

<span data-ttu-id="043ef-132">Если служба Azure Information Protection (AIP) для клиента включена, все пользователи могут синхронизировать данные Microsoft Edge независимо от типа лицензии.</span><span class="sxs-lookup"><span data-stu-id="043ef-132">If the Azure Information Protection (AIP) service is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="043ef-133">Инструкции по включению службы AIP см. [здесь](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="043ef-133">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="043ef-134">Чтобы ограничить синхронизацию для определенных пользователей, вы можете включить для них [Политику управления регистрацией в AADRM](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps).</span><span class="sxs-lookup"><span data-stu-id="043ef-134">To restrict sync to certain set of users, you can enable the [AADRM onboarding control policy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) for those users.</span></span> <span data-ttu-id="043ef-135">Если после регистрации всех необходимых пользователей синхронизация все еще недоступна, убедитесь в том, что служба IPCv3Service включена, используя командлет PowerShell [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/Get-AipServiceIPCv3?view=azureipps).</span><span class="sxs-lookup"><span data-stu-id="043ef-135">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/Get-AipServiceIPCv3?view=azureipps) PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="043ef-136">Включение службы Azure Information Protection также ограничит доступ с помощью AIP для других приложений, таких как Microsoft Word или Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="043ef-136">Activating Azure Information Protection will also restrict access for other applications using AIP, such as Microsoft Word or Microsoft Outlook.</span></span>

### <span data-ttu-id="043ef-137">Azure AD Enterprise State Roaming (ESR)</span><span class="sxs-lookup"><span data-stu-id="043ef-137">Azure AD Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="043ef-138">Если функция [Enterprise State Roaming](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) (ESR) в Azure Active Directory включена для любого пользователя или клиента, они смогут использовать функцию синхронизации Microsoft Edge независимо от значения параметра политики управления регистрацией.</span><span class="sxs-lookup"><span data-stu-id="043ef-138">If the Azure Active Directory [Enterprise State Roaming](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) (ESR) feature is enabled for any user or tenant, they can use the Microsoft Edge sync feature regardless of the onboarding control policy setting.</span></span>

## <span data-ttu-id="043ef-139">Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="043ef-139">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="043ef-140">Новая версия Microsoft Edge— это межплатформенное приложение для расширенной синхронизации пользовательских данных на всех используемых устройствах. Приложение больше не входит состав службы Enterprise State Roaming в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="043ef-140">The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="043ef-141">Однако в новой версии Microsoft Edge будут реализованы средства защиты данных, аналогичные ESR, такие как возможность использования собственного ключа.</span><span class="sxs-lookup"><span data-stu-id="043ef-141">However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="043ef-142">Дополнительные сведения см. в разделе [Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="043ef-142">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="043ef-143">Синхронизация групповых политик</span><span class="sxs-lookup"><span data-stu-id="043ef-143">Sync group policies</span></span>

<span data-ttu-id="043ef-144">На функцию синхронизации Microsoft Edge влияют следующие групповые политики:</span><span class="sxs-lookup"><span data-stu-id="043ef-144">The following group policies impact Microsoft Edge sync:</span></span>

- <span data-ttu-id="043ef-145">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): полное отключение синхронизации.</span><span class="sxs-lookup"><span data-stu-id="043ef-145">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="043ef-146">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): отключает сохранение журнала браузера и синхронизацию. Эта политика также отключает синхронизацию открытых вкладок.</span><span class="sxs-lookup"><span data-stu-id="043ef-146">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="043ef-147">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Настройка списка типов, которые исключены из синхронизации.</span><span class="sxs-lookup"><span data-stu-id="043ef-147">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>

## <span data-ttu-id="043ef-148">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="043ef-148">Frequently Asked Questions</span></span>

### <span data-ttu-id="043ef-149">БЕЗОПАСНОСТЬ И СООТВЕТСТВИЕ СЕРВЕРА/ДАННЫХ</span><span class="sxs-lookup"><span data-stu-id="043ef-149">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="043ef-150">Шифруются ли синхронизированные данные?</span><span class="sxs-lookup"><span data-stu-id="043ef-150">Is the synced data encrypted?</span></span> 

<span data-ttu-id="043ef-151">Данные шифруются при передаче с использованием протокола TLS 1.2 или более поздней версии, а также дополнительно в других службах Майкрософт с использованием AES256.</span><span class="sxs-lookup"><span data-stu-id="043ef-151">The data is encrypted in transport using TLS 1.2 or greater, and additionally at rest in Microsoft's service using AES256.</span></span>

#### <span data-ttu-id="043ef-152">Где хранятся данные синхронизации Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="043ef-152">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="043ef-153">Синхронизированные данные учетных записей Azure AD хранятся на защищенных серверах в соответствии с идентификатором клиента.</span><span class="sxs-lookup"><span data-stu-id="043ef-153">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="043ef-154">Например, данные клиента, зарегистрированного в США, хранятся на серверах, расположенных в этом географическом регионе, и к ним применяется то же самое решение для хранения, что и к приложениям Office.</span><span class="sxs-lookup"><span data-stu-id="043ef-154">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="043ef-155">Выходят ли данные за пределы облака Майкрософт помимо синхронизации с Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="043ef-155">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="043ef-156">Нет.</span><span class="sxs-lookup"><span data-stu-id="043ef-156">No.</span></span>

#### <span data-ttu-id="043ef-157">Могут ли администраторы клиента использовать свой ключ?</span><span class="sxs-lookup"><span data-stu-id="043ef-157">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="043ef-158">Да, с помощью[ Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="043ef-158">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="043ef-159">Каковы условия использования синхронизации в корпоративной среде?</span><span class="sxs-lookup"><span data-stu-id="043ef-159">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="043ef-160">Условия предоставления услуг те же, что и для вашей подписки на Azure AD.</span><span class="sxs-lookup"><span data-stu-id="043ef-160">The terms of service are the same terms as your Azure AD subscription.</span></span> <span data-ttu-id="043ef-161">Все условия предоставления услуг в Azure AD регулируются [условиями использования веб-служб](https://www.microsoft.com/licensing/product-licensing/products) Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="043ef-161">All the Azure AD terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="043ef-162">Поддерживает ли Microsoft Edge стандарты соответствия требованиям облака сообщества для государственных организаций (GCC High)?</span><span class="sxs-lookup"><span data-stu-id="043ef-162">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="043ef-163">Еще нет.</span><span class="sxs-lookup"><span data-stu-id="043ef-163">Not today.</span></span> <span data-ttu-id="043ef-164">GCC High использует уровень D, тогда как Microsoft Edge поддерживает стандарты соответствия требованиям до уровня C.</span><span class="sxs-lookup"><span data-stu-id="043ef-164">GCC High is Tier D, while Microsoft Edge supports up to Tier C.</span></span>

### <span data-ttu-id="043ef-165">ПРИМЕНЕНИЕ СИНХРОНИЗАЦИИ</span><span class="sxs-lookup"><span data-stu-id="043ef-165">APPLYING SYNC</span></span>

#### <span data-ttu-id="043ef-166">Что произойдет с корпоративными клиентами и клиентами из сферы образования, которые решат продолжить использовать устаревшую версию Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="043ef-166">What happens with enterprise and educational customers who decide to stay with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="043ef-167">Текущая версия браузера Microsoft Edge продолжит входить в состав предложения ESR.</span><span class="sxs-lookup"><span data-stu-id="043ef-167">The current version of Microsoft Edge browser will continue to participate in the ESR offering.</span></span>

#### <span data-ttu-id="043ef-168">Почему для синхронизации нужна подписка Azure AD Premium?</span><span class="sxs-lookup"><span data-stu-id="043ef-168">Why do I need a premium Azure AD subscription to sync?</span></span>

<span data-ttu-id="043ef-169">Синхронизация в корпоративной среде зависит от службы Azure Information Protection, которая доступна не для всех уровней Azure AD.</span><span class="sxs-lookup"><span data-stu-id="043ef-169">Enterprise sync depends on Azure Information Protection, which is not available in all Azure AD tiers.</span></span>

#### <span data-ttu-id="043ef-170">Основана ли функция синхронизации Microsoft Edge на Enterprise State Roaming?</span><span class="sxs-lookup"><span data-stu-id="043ef-170">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="043ef-171">Нет.</span><span class="sxs-lookup"><span data-stu-id="043ef-171">No.</span></span> <span data-ttu-id="043ef-172">ESR может использоваться для включения синхронизации, но функция синхронизации Microsoft Edge не входит в состав ESR.</span><span class="sxs-lookup"><span data-stu-id="043ef-172">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="043ef-173">Дополнительные сведения см. в разделах [Функция синхронизации Microsoft Edge](microsoft-edge-enterprise-sync.md) и [Microsoft Edge и Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="043ef-173">For more information, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) and [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

#### <span data-ttu-id="043ef-174">Будет ли Microsoft Edge поддерживать синхронизацию между Microsoft Edge и IE?</span><span class="sxs-lookup"><span data-stu-id="043ef-174">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="043ef-175">Поддержка такой синхронизации не планируется.</span><span class="sxs-lookup"><span data-stu-id="043ef-175">There are no plans to support this syncing.</span></span> <span data-ttu-id="043ef-176">Если для поддержки устаревших приложений вам нужен IE, подумайте об использовании [нового режима IE](https://docs.microsoft.com/deployedge/edge-ie-mode).</span><span class="sxs-lookup"><span data-stu-id="043ef-176">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="043ef-177">Будет ли синхронизироваться новый браузер Microsoft Edge с устаревшей версией Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="043ef-177">Will the new Microsoft Edge browser sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="043ef-178">Нет, не будет.</span><span class="sxs-lookup"><span data-stu-id="043ef-178">No, it won't.</span></span> <span data-ttu-id="043ef-179">Мы считаем, что объединение этих двух экосистем может привести к нарушению надежности синхронизации в новой версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="043ef-179">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the new Microsoft Edge.</span></span> <span data-ttu-id="043ef-180">Мы обеспечим перенос имеющихся данных в новую версию Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="043ef-180">We will ensure that existing data is migrated to the new Microsoft Edge.</span></span> <span data-ttu-id="043ef-181">Кроме того, пользователи смогут импортировать данные из браузера, которым они пользуются.</span><span class="sxs-lookup"><span data-stu-id="043ef-181">Users will also be able to import data from browser of their choice.</span></span> <span data-ttu-id="043ef-182">Это также означает, что синхронизация между новым браузером Microsoft Edge и браузером Internet Explorer выполняться не будет.</span><span class="sxs-lookup"><span data-stu-id="043ef-182">This also means that new Microsoft Edge browser won't have a way to sync with IE.</span></span>

### <span data-ttu-id="043ef-183">УПРАВЛЕНИЕ СИНХРОНИЗАЦИЕЙ</span><span class="sxs-lookup"><span data-stu-id="043ef-183">MANAGING SYNC</span></span>

#### <span data-ttu-id="043ef-184">Можно ли запретить пользователям синхронизацию с личным клиентом?</span><span class="sxs-lookup"><span data-stu-id="043ef-184">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="043ef-185">Прямо нет, но вы можете определить, с каким профилем можно входить в Microsoft Edge, с помощью политики [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="043ef-185">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="043ef-186">См. также</span><span class="sxs-lookup"><span data-stu-id="043ef-186">See also</span></span>

- [<span data-ttu-id="043ef-187">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="043ef-187">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="043ef-188">Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="043ef-188">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
