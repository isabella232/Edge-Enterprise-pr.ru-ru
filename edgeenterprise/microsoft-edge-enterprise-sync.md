---
title: Синхронизация Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 09/15/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Синхронизация Microsoft Edge Enterprise
ms.openlocfilehash: d9cd643142d0f6744664a5071c5000b820583e41
ms.sourcegitcommit: 06c365faeea6070f103fe867cc2da13539ae4680
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2020
ms.locfileid: "11016348"
---
# <span data-ttu-id="fd1db-103">Синхронизация Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="fd1db-103">Microsoft Edge Enterprise Sync</span></span>

<span data-ttu-id="fd1db-104">В этой статье объясняется, как использовать Microsoft Edge для синхронизации избранного, паролей и других данных браузера на всех устройствах, на которых выполнен вход пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="fd1db-104">This article explains how to use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="fd1db-105">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="fd1db-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="fd1db-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="fd1db-106">Overview</span></span>

<span data-ttu-id="fd1db-107">Функция синхронизации Microsoft Edge позволяет пользователям получать доступ к данным браузера на всех своих устройствах, на которых они выполняют вход в систему.</span><span class="sxs-lookup"><span data-stu-id="fd1db-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="fd1db-108">К данным, поддерживаемым функцией синхронизации, относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="fd1db-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="fd1db-109">Избранное</span><span class="sxs-lookup"><span data-stu-id="fd1db-109">Favorites</span></span>
- <span data-ttu-id="fd1db-110">Пароли</span><span class="sxs-lookup"><span data-stu-id="fd1db-110">Passwords</span></span>
- <span data-ttu-id="fd1db-111">Адреса и прочее (заполнения форм)</span><span class="sxs-lookup"><span data-stu-id="fd1db-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="fd1db-112">Коллекции</span><span class="sxs-lookup"><span data-stu-id="fd1db-112">Collections</span></span>
- <span data-ttu-id="fd1db-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd1db-113">Settings</span></span>
- <span data-ttu-id="fd1db-114">История просмотров</span><span class="sxs-lookup"><span data-stu-id="fd1db-114">Browsing history</span></span>
- <span data-ttu-id="fd1db-115">Открытые вкладки</span><span class="sxs-lookup"><span data-stu-id="fd1db-115">Open tabs</span></span>

<span data-ttu-id="fd1db-116">Функция синхронизации включается путем предоставления пользователем согласия с этим действием. Пользователи могут включать или отключать синхронизацию для всех перечисленных выше типов данных.</span><span class="sxs-lookup"><span data-stu-id="fd1db-116">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="fd1db-117">Для обеспечения поддержки функции синхронизации передаются дополнительные данные о подключении устройства и данные конфигурации (например, имя устройства, изготовитель и модель).</span><span class="sxs-lookup"><span data-stu-id="fd1db-117">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="fd1db-118">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="fd1db-118">Prerequisites</span></span>

<span data-ttu-id="fd1db-119">Функция синхронизации Microsoft Edge для учетных записей Azure Active Directory (Azure AD) доступна в рамках любой из этих подписок:</span><span class="sxs-lookup"><span data-stu-id="fd1db-119">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="fd1db-120">Azure AD Premium (P1 или P2)</span><span class="sxs-lookup"><span data-stu-id="fd1db-120">Azure AD Premium (P1 and P2)</span></span>
- <span data-ttu-id="fd1db-121">M365 бизнес премиум</span><span class="sxs-lookup"><span data-stu-id="fd1db-121">M365 Business Premium</span></span>
- <span data-ttu-id="fd1db-122">Office 365 E3 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="fd1db-122">Office 365 E3 and above</span></span>
- <span data-ttu-id="fd1db-123">Azure Information Protection (AIP) (P1 и P2)</span><span class="sxs-lookup"><span data-stu-id="fd1db-123">Azure Information Protection (AIP) (P1& P2)</span></span>
- <span data-ttu-id="fd1db-124">Все подписки EDU (приложения Майкрософт для учащихся или преподавателей, Exchange Online для учащихся или преподавателей, O365 A1 или выше, M365 A1 или выше, Azure Information Protection P1 или P2 для учащихся или преподавателей)</span><span class="sxs-lookup"><span data-stu-id="fd1db-124">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <span data-ttu-id="fd1db-125">Настройка синхронизации Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fd1db-125">Configuring Microsoft Edge sync</span></span>

<span data-ttu-id="fd1db-126">Параметры конфигурации для функции синхронизации Microsoft Edge доступны в службе Azure Information Protection (AIP).</span><span class="sxs-lookup"><span data-stu-id="fd1db-126">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="fd1db-127">Если служба AIP включена для клиента, все пользователи могут синхронизировать данные в Microsoft Edge независимо от типа лицензии.</span><span class="sxs-lookup"><span data-stu-id="fd1db-127">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="fd1db-128">Инструкции по включению службы AIP см. [здесь](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="fd1db-128">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="fd1db-129">Чтобы ограничить синхронизацию для определенной группы пользователей, вы можете включить для них [политику управления регистрацией в AIP](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) .</span><span class="sxs-lookup"><span data-stu-id="fd1db-129">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) for those users.</span></span> <span data-ttu-id="fd1db-130">Если после регистрации всех необходимых пользователей синхронизация все еще недоступна, убедитесь в том, что служба IPCv3Service включена, используя командлет PowerShell [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps).</span><span class="sxs-lookup"><span data-stu-id="fd1db-130">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="fd1db-131">При включении службы Azure Information Protection другие приложения, такие как Microsoft Word и Microsoft Outlook, также смогут защищать контент с помощью AIP.</span><span class="sxs-lookup"><span data-stu-id="fd1db-131">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="fd1db-132">Кроме того, любая политика управления регистрацией, используемая для ограничения синхронизации Microsoft Edge, также ограничит защиту контента с помощью AIP в других приложениях.</span><span class="sxs-lookup"><span data-stu-id="fd1db-132">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <span data-ttu-id="fd1db-133">Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="fd1db-133">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="fd1db-134">Новая версия Microsoft Edge— это межплатформенное приложение для расширенной синхронизации пользовательских данных на всех используемых устройствах. Приложение больше не входит состав службы Enterprise State Roaming в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="fd1db-134">The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="fd1db-135">Однако в новой версии Microsoft Edge будут реализованы средства защиты данных, аналогичные ESR, такие как возможность использования собственного ключа.</span><span class="sxs-lookup"><span data-stu-id="fd1db-135">However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="fd1db-136">Дополнительные сведения см. в разделе [Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="fd1db-136">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="fd1db-137">Синхронизация групповых политик</span><span class="sxs-lookup"><span data-stu-id="fd1db-137">Sync group policies</span></span>

<span data-ttu-id="fd1db-138">На функцию синхронизации Microsoft Edge влияют следующие групповые политики:</span><span class="sxs-lookup"><span data-stu-id="fd1db-138">The following group policies impact Microsoft Edge sync:</span></span>

- <span data-ttu-id="fd1db-139">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): полное отключение синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fd1db-139">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="fd1db-140">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): отключает сохранение журнала браузера и синхронизацию. Эта политика также отключает синхронизацию открытых вкладок.</span><span class="sxs-lookup"><span data-stu-id="fd1db-140">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="fd1db-141">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Настройка списка типов, которые исключены из синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fd1db-141">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="fd1db-142">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): разрешает профилям Active Directory (AD) использовать локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="fd1db-142">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="fd1db-143">Дополнительные сведения см. в статье [Локальная синхронизация для пользователей Active Directory (AD)](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span><span class="sxs-lookup"><span data-stu-id="fd1db-143">For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span></span>
- <span data-ttu-id="fd1db-144">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): включает синхронизацию по умолчанию и не требует согласия пользователя для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fd1db-144">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn sync on by default and do not require user consent to sync.</span></span>  

## <span data-ttu-id="fd1db-145">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="fd1db-145">Frequently Asked Questions</span></span>

### <span data-ttu-id="fd1db-146">БЕЗОПАСНОСТЬ И СООТВЕТСТВИЕ СЕРВЕРА/ДАННЫХ</span><span class="sxs-lookup"><span data-stu-id="fd1db-146">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="fd1db-147">Шифруются ли синхронизированные данные?</span><span class="sxs-lookup"><span data-stu-id="fd1db-147">Is the synced data encrypted?</span></span> 

<span data-ttu-id="fd1db-148">Данные шифруются в процессе транспортировки с использованием TLS 1.2 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="fd1db-148">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="fd1db-149">Большинство типов данных дополнительно шифруются в неактивном состоянии в службе Microsoft с использованием AES256, за исключением журнала браузера и открытых вкладок.</span><span class="sxs-lookup"><span data-stu-id="fd1db-149">Most data types are additionally encrypted at rest in Microsoft's service using AES256, with the exception of the browser history and open tabs datatypes.</span></span> <span data-ttu-id="fd1db-150">Чтобы запретить синхронизацию этих типов данных, можно применить политику [SavingBrowserHistoryDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#savingbrowserhistorydisabled).</span><span class="sxs-lookup"><span data-stu-id="fd1db-150">To prevent these data types from syncing, you can apply the [SavingBrowserHistoryDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#savingbrowserhistorydisabled) policy.</span></span>

#### <span data-ttu-id="fd1db-151">Где хранятся данные синхронизации Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="fd1db-151">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="fd1db-152">Синхронизированные данные учетных записей Azure AD хранятся на защищенных серверах в соответствии с идентификатором клиента.</span><span class="sxs-lookup"><span data-stu-id="fd1db-152">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="fd1db-153">Например, данные клиента, зарегистрированного в США, хранятся на серверах, расположенных в этом географическом регионе, и к ним применяется то же самое решение для хранения, что и к приложениям Office.</span><span class="sxs-lookup"><span data-stu-id="fd1db-153">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="fd1db-154">Выходят ли данные за пределы облака Майкрософт помимо синхронизации с Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="fd1db-154">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="fd1db-155">Нет.</span><span class="sxs-lookup"><span data-stu-id="fd1db-155">No.</span></span>

#### <span data-ttu-id="fd1db-156">Могут ли администраторы клиента использовать свой ключ?</span><span class="sxs-lookup"><span data-stu-id="fd1db-156">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="fd1db-157">Да, с помощью[ Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="fd1db-157">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="fd1db-158">Каковы условия использования синхронизации в корпоративной среде?</span><span class="sxs-lookup"><span data-stu-id="fd1db-158">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="fd1db-159">Условия предоставления услуг те же, что и для вашей подписки на Azure AD.</span><span class="sxs-lookup"><span data-stu-id="fd1db-159">The terms of service are the same terms as your Azure AD subscription.</span></span> <span data-ttu-id="fd1db-160">Все условия предоставления услуг в Azure AD регулируются [условиями использования веб-служб](https://www.microsoft.com/licensing/product-licensing/products) Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="fd1db-160">All the Azure AD terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="fd1db-161">Поддерживает ли Microsoft Edge стандарты соответствия требованиям облака сообщества для государственных организаций (GCC High)?</span><span class="sxs-lookup"><span data-stu-id="fd1db-161">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="fd1db-162">Еще нет.</span><span class="sxs-lookup"><span data-stu-id="fd1db-162">Not today.</span></span> <span data-ttu-id="fd1db-163">GCC High использует уровень D, тогда как Microsoft Edge поддерживает стандарты соответствия требованиям до уровня C.</span><span class="sxs-lookup"><span data-stu-id="fd1db-163">GCC High is Tier D, while Microsoft Edge supports up to Tier C.</span></span>

### <span data-ttu-id="fd1db-164">ПРИМЕНЕНИЕ СИНХРОНИЗАЦИИ</span><span class="sxs-lookup"><span data-stu-id="fd1db-164">APPLYING SYNC</span></span>

#### <span data-ttu-id="fd1db-165">Что произойдет с корпоративными клиентами и клиентами из сферы образования, которые решат продолжить использовать устаревшую версию Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="fd1db-165">What happens with enterprise and educational customers who decide to stay with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="fd1db-166">Текущая версия браузера Microsoft Edge продолжит входить в состав предложения ESR.</span><span class="sxs-lookup"><span data-stu-id="fd1db-166">The current version of Microsoft Edge browser will continue to participate in the ESR offering.</span></span>

#### <span data-ttu-id="fd1db-167">Почему для синхронизации нужна подписка Azure AD Premium?</span><span class="sxs-lookup"><span data-stu-id="fd1db-167">Why do I need a premium Azure AD subscription to sync?</span></span>

<span data-ttu-id="fd1db-168">Синхронизация в корпоративной среде зависит от службы Azure Information Protection, которая доступна не для всех уровней Azure AD.</span><span class="sxs-lookup"><span data-stu-id="fd1db-168">Enterprise sync depends on Azure Information Protection, which is not available in all Azure AD tiers.</span></span>

#### <span data-ttu-id="fd1db-169">Основана ли функция синхронизации Microsoft Edge на Enterprise State Roaming?</span><span class="sxs-lookup"><span data-stu-id="fd1db-169">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="fd1db-170">Нет.</span><span class="sxs-lookup"><span data-stu-id="fd1db-170">No.</span></span> <span data-ttu-id="fd1db-171">ESR может использоваться для включения синхронизации, но функция синхронизации Microsoft Edge не входит в состав ESR.</span><span class="sxs-lookup"><span data-stu-id="fd1db-171">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="fd1db-172">Дополнительные сведения см. в разделах [Функция синхронизации Microsoft Edge](microsoft-edge-enterprise-sync.md) и [Microsoft Edge и Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="fd1db-172">For more information, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) and [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

#### <span data-ttu-id="fd1db-173">Будет ли Microsoft Edge поддерживать синхронизацию между Microsoft Edge и IE?</span><span class="sxs-lookup"><span data-stu-id="fd1db-173">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="fd1db-174">Поддержка такой синхронизации не планируется.</span><span class="sxs-lookup"><span data-stu-id="fd1db-174">There are no plans to support this syncing.</span></span> <span data-ttu-id="fd1db-175">Если для поддержки устаревших приложений вам нужен IE, подумайте об использовании [нового режима IE](https://docs.microsoft.com/deployedge/edge-ie-mode).</span><span class="sxs-lookup"><span data-stu-id="fd1db-175">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="fd1db-176">Будет ли синхронизироваться новый браузер Microsoft Edge с устаревшей версией Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="fd1db-176">Will the new Microsoft Edge browser sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="fd1db-177">Нет, не будет.</span><span class="sxs-lookup"><span data-stu-id="fd1db-177">No, it won't.</span></span> <span data-ttu-id="fd1db-178">Мы считаем, что объединение этих двух экосистем может привести к нарушению надежности синхронизации в новой версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fd1db-178">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the new Microsoft Edge.</span></span> <span data-ttu-id="fd1db-179">Мы обеспечим перенос имеющихся данных в новую версию Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fd1db-179">We will ensure that existing data is migrated to the new Microsoft Edge.</span></span> <span data-ttu-id="fd1db-180">Кроме того, пользователи смогут импортировать данные из браузера, которым они пользуются.</span><span class="sxs-lookup"><span data-stu-id="fd1db-180">Users will also be able to import data from browser of their choice.</span></span> <span data-ttu-id="fd1db-181">Это также означает, что синхронизация между новым браузером Microsoft Edge и браузером Internet Explorer выполняться не будет.</span><span class="sxs-lookup"><span data-stu-id="fd1db-181">This also means that new Microsoft Edge browser won't have a way to sync with IE.</span></span>

### <span data-ttu-id="fd1db-182">УПРАВЛЕНИЕ СИНХРОНИЗАЦИЕЙ</span><span class="sxs-lookup"><span data-stu-id="fd1db-182">MANAGING SYNC</span></span>

#### <span data-ttu-id="fd1db-183">Можно ли запретить пользователям синхронизацию с личным клиентом?</span><span class="sxs-lookup"><span data-stu-id="fd1db-183">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="fd1db-184">Прямо нет, но вы можете определить, с каким профилем можно входить в Microsoft Edge, с помощью политики [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="fd1db-184">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="fd1db-185">См. также</span><span class="sxs-lookup"><span data-stu-id="fd1db-185">See also</span></span>

- [<span data-ttu-id="fd1db-186">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="fd1db-186">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="fd1db-187">Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="fd1db-187">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
