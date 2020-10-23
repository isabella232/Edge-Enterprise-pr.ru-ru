---
title: Синхронизация Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 10/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Синхронизация Microsoft Edge Enterprise
ms.openlocfilehash: e51346d9bab83228c42a84a7a14ee45dc9b463a7
ms.sourcegitcommit: b32d8d64ae65dc5a46e47b7c34b0211097a0cc65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2020
ms.locfileid: "11133134"
---
# <span data-ttu-id="db481-103">Синхронизация Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="db481-103">Microsoft Edge Enterprise Sync</span></span>

<span data-ttu-id="db481-104">В этой статье объясняется, как использовать Microsoft Edge для синхронизации избранного, паролей и других данных браузера на всех устройствах, на которых выполнен вход пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="db481-104">This article explains how to use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="db481-105">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="db481-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="db481-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="db481-106">Overview</span></span>

<span data-ttu-id="db481-107">Функция синхронизации Microsoft Edge позволяет пользователям получать доступ к данным браузера на всех своих устройствах, на которых они выполняют вход в систему.</span><span class="sxs-lookup"><span data-stu-id="db481-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="db481-108">К данным, поддерживаемым функцией синхронизации, относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="db481-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="db481-109">Избранное</span><span class="sxs-lookup"><span data-stu-id="db481-109">Favorites</span></span>
- <span data-ttu-id="db481-110">Пароли</span><span class="sxs-lookup"><span data-stu-id="db481-110">Passwords</span></span>
- <span data-ttu-id="db481-111">Адреса и прочее (заполнения форм)</span><span class="sxs-lookup"><span data-stu-id="db481-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="db481-112">Коллекции</span><span class="sxs-lookup"><span data-stu-id="db481-112">Collections</span></span>
- <span data-ttu-id="db481-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="db481-113">Settings</span></span>

<span data-ttu-id="db481-114">Функция синхронизации включается путем предоставления пользователем согласия с этим действием. Пользователи могут включать или отключать синхронизацию для всех перечисленных выше типов данных.</span><span class="sxs-lookup"><span data-stu-id="db481-114">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="db481-115">Для обеспечения поддержки функции синхронизации передаются дополнительные данные о подключении устройства и данные конфигурации (например, имя устройства, изготовитель и модель).</span><span class="sxs-lookup"><span data-stu-id="db481-115">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="db481-116">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="db481-116">Prerequisites</span></span>

<span data-ttu-id="db481-117">Функция синхронизации Microsoft Edge для учетных записей Azure Active Directory (Azure AD) доступна в рамках любой из этих подписок:</span><span class="sxs-lookup"><span data-stu-id="db481-117">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="db481-118">Azure AD Premium (P1 или P2)</span><span class="sxs-lookup"><span data-stu-id="db481-118">Azure AD Premium (P1 and P2)</span></span>
- <span data-ttu-id="db481-119">M365 бизнес премиум</span><span class="sxs-lookup"><span data-stu-id="db481-119">M365 Business Premium</span></span>
- <span data-ttu-id="db481-120">Office 365 E1 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="db481-120">Office 365 E1 and above</span></span>
- <span data-ttu-id="db481-121">Azure Information Protection (AIP) (P1 и P2)</span><span class="sxs-lookup"><span data-stu-id="db481-121">Azure Information Protection (AIP) (P1& P2)</span></span>
- <span data-ttu-id="db481-122">Все подписки EDU (приложения Майкрософт для учащихся или преподавателей, Exchange Online для учащихся или преподавателей, O365 A1 или выше, M365 A1 или выше, Azure Information Protection P1 или P2 для учащихся или преподавателей)</span><span class="sxs-lookup"><span data-stu-id="db481-122">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <span data-ttu-id="db481-123">Настройка синхронизации Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="db481-123">Configuring Microsoft Edge sync</span></span>

<span data-ttu-id="db481-124">Параметры конфигурации для функции синхронизации Microsoft Edge доступны в службе Azure Information Protection (AIP).</span><span class="sxs-lookup"><span data-stu-id="db481-124">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="db481-125">Если служба AIP включена для клиента, все пользователи могут синхронизировать данные в Microsoft Edge независимо от типа лицензии.</span><span class="sxs-lookup"><span data-stu-id="db481-125">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="db481-126">Инструкции по включению службы AIP см. [здесь](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="db481-126">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="db481-127">Чтобы ограничить синхронизацию для определенной группы пользователей, вы можете включить для них [политику управления регистрацией в AIP](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) .</span><span class="sxs-lookup"><span data-stu-id="db481-127">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) for those users.</span></span> <span data-ttu-id="db481-128">Если после регистрации всех необходимых пользователей синхронизация все еще недоступна, убедитесь в том, что служба IPCv3Service включена, используя командлет PowerShell [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps).</span><span class="sxs-lookup"><span data-stu-id="db481-128">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="db481-129">При включении службы Azure Information Protection другие приложения, такие как Microsoft Word и Microsoft Outlook, также смогут защищать контент с помощью AIP.</span><span class="sxs-lookup"><span data-stu-id="db481-129">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="db481-130">Кроме того, любая политика управления регистрацией, используемая для ограничения синхронизации Microsoft Edge, также ограничит защиту контента с помощью AIP в других приложениях.</span><span class="sxs-lookup"><span data-stu-id="db481-130">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <span data-ttu-id="db481-131">Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="db481-131">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="db481-132">Новая версия Microsoft Edge— это межплатформенное приложение для расширенной синхронизации пользовательских данных на всех используемых устройствах. Приложение больше не входит состав службы Enterprise State Roaming в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="db481-132">The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="db481-133">Однако в новой версии Microsoft Edge будут реализованы средства защиты данных, аналогичные ESR, такие как возможность использования собственного ключа.</span><span class="sxs-lookup"><span data-stu-id="db481-133">However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="db481-134">Дополнительные сведения см. в разделе [Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="db481-134">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="db481-135">Синхронизация групповых политик</span><span class="sxs-lookup"><span data-stu-id="db481-135">Sync group policies</span></span>

<span data-ttu-id="db481-136">На функцию синхронизации Microsoft Edge влияют следующие групповые политики:</span><span class="sxs-lookup"><span data-stu-id="db481-136">The following group policies impact Microsoft Edge sync:</span></span>

- <span data-ttu-id="db481-137">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): полное отключение синхронизации.</span><span class="sxs-lookup"><span data-stu-id="db481-137">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="db481-138">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): отключает сохранение журнала браузера и синхронизацию. Эта политика также отключает синхронизацию открытых вкладок.</span><span class="sxs-lookup"><span data-stu-id="db481-138">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="db481-139">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Настройка списка типов, которые исключены из синхронизации.</span><span class="sxs-lookup"><span data-stu-id="db481-139">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="db481-140">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): разрешает профилям Active Directory (AD) использовать локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="db481-140">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="db481-141">Дополнительные сведения см. в статье [Локальная синхронизация для пользователей Active Directory (AD)](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span><span class="sxs-lookup"><span data-stu-id="db481-141">For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span></span>
- <span data-ttu-id="db481-142">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): включает синхронизацию по умолчанию и не требует согласия пользователя для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="db481-142">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn sync on by default and do not require user consent to sync.</span></span>  

## <span data-ttu-id="db481-143">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="db481-143">Frequently Asked Questions</span></span>

### <span data-ttu-id="db481-144">БЕЗОПАСНОСТЬ И СООТВЕТСТВИЕ СЕРВЕРА/ДАННЫХ</span><span class="sxs-lookup"><span data-stu-id="db481-144">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="db481-145">Шифруются ли синхронизированные данные?</span><span class="sxs-lookup"><span data-stu-id="db481-145">Is the synced data encrypted?</span></span> 

<span data-ttu-id="db481-146">Данные шифруются в процессе транспортировки с использованием TLS 1.2 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="db481-146">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="db481-147">Большинство типов данных дополнительно шифруются в службе Майкрософт с помощью AES256.</span><span class="sxs-lookup"><span data-stu-id="db481-147">Most data types are additionally encrypted at rest in Microsoft's service using AES256.</span></span> 

#### <span data-ttu-id="db481-148">Где хранятся данные синхронизации Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="db481-148">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="db481-149">Синхронизированные данные учетных записей Azure AD хранятся на защищенных серверах в соответствии с идентификатором клиента.</span><span class="sxs-lookup"><span data-stu-id="db481-149">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="db481-150">Например, данные клиента, зарегистрированного в США, хранятся на серверах, расположенных в этом географическом регионе, и к ним применяется то же самое решение для хранения, что и к приложениям Office.</span><span class="sxs-lookup"><span data-stu-id="db481-150">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="db481-151">Выходят ли данные за пределы облака Майкрософт помимо синхронизации с Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="db481-151">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="db481-152">Нет.</span><span class="sxs-lookup"><span data-stu-id="db481-152">No.</span></span>

#### <span data-ttu-id="db481-153">Могут ли администраторы клиента использовать свой ключ?</span><span class="sxs-lookup"><span data-stu-id="db481-153">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="db481-154">Да, с помощью[ Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="db481-154">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="db481-155">Каковы условия использования синхронизации в корпоративной среде?</span><span class="sxs-lookup"><span data-stu-id="db481-155">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="db481-156">Условия предоставления услуг те же, что и для вашей подписки на Azure AD.</span><span class="sxs-lookup"><span data-stu-id="db481-156">The terms of service are the same terms as your Azure AD subscription.</span></span> <span data-ttu-id="db481-157">Все условия предоставления услуг в Azure AD регулируются [условиями использования веб-служб](https://www.microsoft.com/licensing/product-licensing/products) Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="db481-157">All the Azure AD terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="db481-158">Поддерживает ли Microsoft Edge стандарты соответствия требованиям облака сообщества для государственных организаций (GCC High)?</span><span class="sxs-lookup"><span data-stu-id="db481-158">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="db481-159">Еще нет.</span><span class="sxs-lookup"><span data-stu-id="db481-159">Not today.</span></span> <span data-ttu-id="db481-160">GCC High использует уровень D, тогда как Microsoft Edge поддерживает стандарты соответствия требованиям до уровня C.</span><span class="sxs-lookup"><span data-stu-id="db481-160">GCC High is Tier D, while Microsoft Edge supports up to Tier C.</span></span>

### <span data-ttu-id="db481-161">ПРИМЕНЕНИЕ СИНХРОНИЗАЦИИ</span><span class="sxs-lookup"><span data-stu-id="db481-161">APPLYING SYNC</span></span>

#### <span data-ttu-id="db481-162">Что произойдет с корпоративными клиентами и клиентами из сферы образования, которые решат продолжить использовать устаревшую версию Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="db481-162">What happens with enterprise and educational customers who decide to stay with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="db481-163">Текущая версия браузера Microsoft Edge продолжит входить в состав предложения ESR.</span><span class="sxs-lookup"><span data-stu-id="db481-163">The current version of Microsoft Edge browser will continue to participate in the ESR offering.</span></span>

#### <span data-ttu-id="db481-164">Почему для синхронизации нужна подписка Azure AD Premium?</span><span class="sxs-lookup"><span data-stu-id="db481-164">Why do I need a premium Azure AD subscription to sync?</span></span>

<span data-ttu-id="db481-165">Синхронизация в корпоративной среде зависит от службы Azure Information Protection, которая доступна не для всех уровней Azure AD.</span><span class="sxs-lookup"><span data-stu-id="db481-165">Enterprise sync depends on Azure Information Protection, which is not available in all Azure AD tiers.</span></span>

#### <span data-ttu-id="db481-166">Основана ли функция синхронизации Microsoft Edge на Enterprise State Roaming?</span><span class="sxs-lookup"><span data-stu-id="db481-166">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="db481-167">Нет.</span><span class="sxs-lookup"><span data-stu-id="db481-167">No.</span></span> <span data-ttu-id="db481-168">ESR может использоваться для включения синхронизации, но функция синхронизации Microsoft Edge не входит в состав ESR.</span><span class="sxs-lookup"><span data-stu-id="db481-168">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="db481-169">Дополнительные сведения см. в разделах [Функция синхронизации Microsoft Edge](microsoft-edge-enterprise-sync.md) и [Microsoft Edge и Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="db481-169">For more information, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) and [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

#### <span data-ttu-id="db481-170">Будет ли Microsoft Edge поддерживать синхронизацию между Microsoft Edge и IE?</span><span class="sxs-lookup"><span data-stu-id="db481-170">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="db481-171">Поддержка такой синхронизации не планируется.</span><span class="sxs-lookup"><span data-stu-id="db481-171">There are no plans to support this syncing.</span></span> <span data-ttu-id="db481-172">Если для поддержки устаревших приложений вам нужен IE, подумайте об использовании [нового режима IE](https://docs.microsoft.com/deployedge/edge-ie-mode).</span><span class="sxs-lookup"><span data-stu-id="db481-172">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="db481-173">Будет ли синхронизироваться новый браузер Microsoft Edge с устаревшей версией Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="db481-173">Will the new Microsoft Edge browser sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="db481-174">Нет, не будет.</span><span class="sxs-lookup"><span data-stu-id="db481-174">No, it won't.</span></span> <span data-ttu-id="db481-175">Мы считаем, что объединение этих двух экосистем может привести к нарушению надежности синхронизации в новой версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="db481-175">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the new Microsoft Edge.</span></span> <span data-ttu-id="db481-176">Мы обеспечим перенос имеющихся данных в новую версию Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="db481-176">We will ensure that existing data is migrated to the new Microsoft Edge.</span></span> <span data-ttu-id="db481-177">Кроме того, пользователи смогут импортировать данные из браузера, которым они пользуются.</span><span class="sxs-lookup"><span data-stu-id="db481-177">Users will also be able to import data from browser of their choice.</span></span> <span data-ttu-id="db481-178">Это также означает, что синхронизация между новым браузером Microsoft Edge и браузером Internet Explorer выполняться не будет.</span><span class="sxs-lookup"><span data-stu-id="db481-178">This also means that new Microsoft Edge browser won't have a way to sync with IE.</span></span>

### <span data-ttu-id="db481-179">УПРАВЛЕНИЕ СИНХРОНИЗАЦИЕЙ</span><span class="sxs-lookup"><span data-stu-id="db481-179">MANAGING SYNC</span></span>

#### <span data-ttu-id="db481-180">Можно ли запретить пользователям синхронизацию с личным клиентом?</span><span class="sxs-lookup"><span data-stu-id="db481-180">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="db481-181">Прямо нет, но вы можете определить, с каким профилем можно входить в Microsoft Edge, с помощью политики [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="db481-181">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="db481-182">См. также</span><span class="sxs-lookup"><span data-stu-id="db481-182">See also</span></span>

- [<span data-ttu-id="db481-183">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="db481-183">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="db481-184">Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="db481-184">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
