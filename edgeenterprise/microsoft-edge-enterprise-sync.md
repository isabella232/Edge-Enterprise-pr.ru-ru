---
title: Синхронизация Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 12/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Синхронизация Microsoft Edge Enterprise
ms.openlocfilehash: 791188b5d28c867d6409a4d5373ea6c1ec7e49c7
ms.sourcegitcommit: 482b2e440a62cbf974dc45ac817f9d9d187ba1b9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "11205468"
---
# <span data-ttu-id="b5419-103">Синхронизация Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="b5419-103">Microsoft Edge Enterprise Sync</span></span>

<span data-ttu-id="b5419-104">В этой статье объясняется, как использовать Microsoft Edge для синхронизации избранного, паролей и других данных браузера на всех устройствах, на которых выполнен вход пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="b5419-104">This article explains how to use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="b5419-105">Эта статья относится к Microsoft Edge версии 77 или более поздней, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="b5419-105">This article applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <span data-ttu-id="b5419-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="b5419-106">Overview</span></span>

<span data-ttu-id="b5419-107">Функция синхронизации Microsoft Edge позволяет пользователям получать доступ к данным браузера на всех своих устройствах, на которых они выполняют вход в систему.</span><span class="sxs-lookup"><span data-stu-id="b5419-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="b5419-108">К данным, поддерживаемым функцией синхронизации, относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="b5419-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="b5419-109">Избранное</span><span class="sxs-lookup"><span data-stu-id="b5419-109">Favorites</span></span>
- <span data-ttu-id="b5419-110">Пароли</span><span class="sxs-lookup"><span data-stu-id="b5419-110">Passwords</span></span>
- <span data-ttu-id="b5419-111">Адреса и прочее (заполнения форм)</span><span class="sxs-lookup"><span data-stu-id="b5419-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="b5419-112">Коллекции</span><span class="sxs-lookup"><span data-stu-id="b5419-112">Collections</span></span>
- <span data-ttu-id="b5419-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5419-113">Settings</span></span>
- <span data-ttu-id="b5419-114">Расширение</span><span class="sxs-lookup"><span data-stu-id="b5419-114">Extension</span></span>
- <span data-ttu-id="b5419-115">Открытые вкладки (доступно в Microsoft Edge версии 88)</span><span class="sxs-lookup"><span data-stu-id="b5419-115">Open tabs (available in Microsoft Edge version 88)</span></span>
- <span data-ttu-id="b5419-116">Журнал (доступно в Microsoft Edge версии 88)</span><span class="sxs-lookup"><span data-stu-id="b5419-116">History (available in Microsoft Edge version 88)</span></span>

<span data-ttu-id="b5419-117">Функция синхронизации включается путем предоставления пользователем согласия с этим действием. Пользователи могут включать или отключать синхронизацию для всех перечисленных выше типов данных.</span><span class="sxs-lookup"><span data-stu-id="b5419-117">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="b5419-118">Для обеспечения поддержки функции синхронизации передаются дополнительные данные о подключении устройства и данные конфигурации (например, имя устройства, изготовитель и модель).</span><span class="sxs-lookup"><span data-stu-id="b5419-118">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="b5419-119">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="b5419-119">Prerequisites</span></span>

<span data-ttu-id="b5419-120">Функция синхронизации Microsoft Edge для учетных записей Azure Active Directory (Azure AD) доступна в рамках любой из этих подписок:</span><span class="sxs-lookup"><span data-stu-id="b5419-120">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="b5419-121">Azure AD Premium (P1 или P2)</span><span class="sxs-lookup"><span data-stu-id="b5419-121">Azure AD Premium (P1 or P2)</span></span>
- <span data-ttu-id="b5419-122">M365 бизнес премиум</span><span class="sxs-lookup"><span data-stu-id="b5419-122">M365 Business Premium</span></span>
- <span data-ttu-id="b5419-123">Office 365 E1 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="b5419-123">Office 365 E1 and above</span></span>
- <span data-ttu-id="b5419-124">Azure Information Protection (AIP) (P1 или P2)</span><span class="sxs-lookup"><span data-stu-id="b5419-124">Azure Information Protection (AIP) (P1 or P2)</span></span>
- <span data-ttu-id="b5419-125">Все подписки EDU (приложения Майкрософт для учащихся или преподавателей, Exchange Online для учащихся или преподавателей, O365 A1 или выше, M365 A1 или выше, Azure Information Protection P1 или P2 для учащихся или преподавателей)</span><span class="sxs-lookup"><span data-stu-id="b5419-125">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <span data-ttu-id="b5419-126">Настройка синхронизации Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b5419-126">Configuring Microsoft Edge sync</span></span>

<span data-ttu-id="b5419-127">Параметры конфигурации для функции синхронизации Microsoft Edge доступны в службе Azure Information Protection (AIP).</span><span class="sxs-lookup"><span data-stu-id="b5419-127">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="b5419-128">Если служба AIP включена для клиента, все пользователи могут синхронизировать данные в Microsoft Edge независимо от типа лицензии.</span><span class="sxs-lookup"><span data-stu-id="b5419-128">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="b5419-129">Инструкции по включению службы AIP см. [здесь](https://docs.microsoft.com/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="b5419-129">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="b5419-130">Чтобы ограничить синхронизацию для определенной группы пользователей, вы можете включить для них [политику управления регистрацией в AIP](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="b5419-130">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) for those users.</span></span> <span data-ttu-id="b5419-131">Если после регистрации всех необходимых пользователей синхронизация все еще недоступна, убедитесь в том, что служба IPCv3Service включена, используя командлет PowerShell [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="b5419-131">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="b5419-132">При включении службы Azure Information Protection другие приложения, такие как Microsoft Word и Microsoft Outlook, также смогут защищать контент с помощью AIP.</span><span class="sxs-lookup"><span data-stu-id="b5419-132">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="b5419-133">Кроме того, любая политика управления регистрацией, используемая для ограничения синхронизации Microsoft Edge, также ограничит защиту контента с помощью AIP в других приложениях.</span><span class="sxs-lookup"><span data-stu-id="b5419-133">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <span data-ttu-id="b5419-134">Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="b5419-134">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="b5419-135">Новая версия Microsoft Edge— это межплатформенное приложение для расширенной синхронизации пользовательских данных на всех используемых устройствах. Приложение больше не входит состав службы Enterprise State Roaming в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="b5419-135">The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="b5419-136">Однако в новой версии Microsoft Edge будут реализованы средства защиты данных, аналогичные ESR, такие как возможность использования собственного ключа.</span><span class="sxs-lookup"><span data-stu-id="b5419-136">However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="b5419-137">Дополнительные сведения см. в разделе [Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="b5419-137">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="b5419-138">Синхронизация групповых политик</span><span class="sxs-lookup"><span data-stu-id="b5419-138">Sync group policies</span></span>

<span data-ttu-id="b5419-139">На функцию синхронизации Microsoft Edge влияют следующие групповые политики:</span><span class="sxs-lookup"><span data-stu-id="b5419-139">The following group policies impact Microsoft Edge sync:</span></span>

- <span data-ttu-id="b5419-140">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): полное отключение синхронизации.</span><span class="sxs-lookup"><span data-stu-id="b5419-140">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="b5419-141">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): отключает сохранение журнала браузера и синхронизацию. Эта политика также отключает синхронизацию открытых вкладок.</span><span class="sxs-lookup"><span data-stu-id="b5419-141">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="b5419-142">[AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): если эта политика отключена, синхронизация журнала также будет отключена.</span><span class="sxs-lookup"><span data-stu-id="b5419-142">[AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.</span></span>
- <span data-ttu-id="b5419-143">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): настройка списка типов, исключенных из синхронизации.</span><span class="sxs-lookup"><span data-stu-id="b5419-143">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="b5419-144">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): разрешает профилям Active Directory (AD) использовать локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="b5419-144">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="b5419-145">Дополнительные сведения см. в статье [Локальная синхронизация для пользователей Active Directory (AD)](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span><span class="sxs-lookup"><span data-stu-id="b5419-145">For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span></span>
- <span data-ttu-id="b5419-146">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): включает синхронизацию по умолчанию и не требует согласия пользователя для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="b5419-146">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn sync on by default and do not require user consent to sync.</span></span>  

## <span data-ttu-id="b5419-147">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="b5419-147">Frequently Asked Questions</span></span>

### <span data-ttu-id="b5419-148">БЕЗОПАСНОСТЬ И СООТВЕТСТВИЕ СЕРВЕРА/ДАННЫХ</span><span class="sxs-lookup"><span data-stu-id="b5419-148">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="b5419-149">Шифруются ли синхронизированные данные?</span><span class="sxs-lookup"><span data-stu-id="b5419-149">Is the synced data encrypted?</span></span>

<span data-ttu-id="b5419-150">Данные шифруются в процессе транспортировки с использованием протокола TLS 1.2 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b5419-150">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="b5419-151">Все типы данных дополнительно шифруются в службе Майкрософт с помощью AES128.</span><span class="sxs-lookup"><span data-stu-id="b5419-151">All data types are additionally encrypted at rest in Microsoft's service using AES128.</span></span> <span data-ttu-id="b5419-152">Все типы данных, кроме используемых для синхронизации открытой вкладки и журнала, дополнительно шифруются перед покиданием устройства пользователя с использованием ключей, управляемых с помощью [Azure Information Protection](https://docs.microsoft.com/azure/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="b5419-152">All data types except those used for open tab and history sync are additionally encrypted before leaving the user’s device with keys managed via [Azure Information Protection](https://docs.microsoft.com/azure/information-protection/).</span></span>

#### <span data-ttu-id="b5419-153">Почему данные открытой вкладки и журнала не используют дополнительное шифрование на стороне клиента?</span><span class="sxs-lookup"><span data-stu-id="b5419-153">Why don’t open tab and history data have additional client-side encryption?</span></span>  

<span data-ttu-id="b5419-154">Чтобы сократить использование ресурсов на устройствах конечных пользователей, данные журнала создаются на стороне сервера на основе перемещаемых данных открытой вкладки.</span><span class="sxs-lookup"><span data-stu-id="b5419-154">In order to reduce resource utilization on end user devices, history data is generated server-side based on open tab roaming data.</span></span> <span data-ttu-id="b5419-155">Этот процесс невозможен при шифровании этих данных на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="b5419-155">This process would not be possible with client-side encryption of this data.</span></span> <span data-ttu-id="b5419-156">Чтобы отключить синхронизацию открытой вкладки и журнала, примените политику [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) или [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled).</span><span class="sxs-lookup"><span data-stu-id="b5419-156">To disable open tab and history sync, apply the [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) or [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) policies.</span></span>

#### <span data-ttu-id="b5419-157">Могут ли администраторы клиента использовать свой ключ?</span><span class="sxs-lookup"><span data-stu-id="b5419-157">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="b5419-158">Да, с помощью  [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="b5419-158">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="b5419-159">Где хранятся данные синхронизации Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="b5419-159">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="b5419-160">Синхронизированные данные учетных записей Azure AD хранятся на защищенных серверах в соответствии с идентификатором клиента.</span><span class="sxs-lookup"><span data-stu-id="b5419-160">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="b5419-161">Например, данные клиента, зарегистрированного в США, хранятся на серверах, расположенных в этом географическом регионе, и к ним применяется то же самое решение для хранения, что и к приложениям Office.</span><span class="sxs-lookup"><span data-stu-id="b5419-161">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="b5419-162">Выходят ли данные за пределы облака Майкрософт помимо синхронизации с Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="b5419-162">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="b5419-163">Нет.</span><span class="sxs-lookup"><span data-stu-id="b5419-163">No.</span></span>

#### <span data-ttu-id="b5419-164">Каковы условия использования синхронизации в корпоративной среде?</span><span class="sxs-lookup"><span data-stu-id="b5419-164">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="b5419-165">Условия использования функции синхронизации Microsoft Edge регулируются лицензией на программное обеспечение корпорации Майкрософт, с которой можно ознакомиться в Microsoft Edge по адресу  *edge://terms*.</span><span class="sxs-lookup"><span data-stu-id="b5419-165">Terms of service for Microsoft Edge sync falls under the Microsoft software license viewable in Microsoft Edge at *edge://terms*.</span></span> <span data-ttu-id="b5419-166">Ваша подписка на Azure AD и условия обслуживания в конечном итоге регулируются [условиями использования веб-служб](https://www.microsoft.com/licensing/product-licensing/products) Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="b5419-166">Your Azure AD subscription and terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="b5419-167">Поддерживает ли Microsoft Edge стандарты соответствия требованиям облака сообщества для государственных организаций (GCC High)?</span><span class="sxs-lookup"><span data-stu-id="b5419-167">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="b5419-168">Еще нет.</span><span class="sxs-lookup"><span data-stu-id="b5419-168">Not today.</span></span> <span data-ttu-id="b5419-169">Для клиентов в облаке GCC High синхронизация Microsoft Edge отключена.</span><span class="sxs-lookup"><span data-stu-id="b5419-169">For customers in the GCC High cloud, Microsoft Edge sync is disabled.</span></span>

### <span data-ttu-id="b5419-170">ПРИМЕНЕНИЕ СИНХРОНИЗАЦИИ</span><span class="sxs-lookup"><span data-stu-id="b5419-170">APPLYING SYNC</span></span>

#### <span data-ttu-id="b5419-171">Почему синхронизация Microsoft Edge не поддерживается во всех подписках M365?</span><span class="sxs-lookup"><span data-stu-id="b5419-171">Why isn’t Microsoft Edge sync supported in all M365 subscriptions?</span></span>

<span data-ttu-id="b5419-172">Синхронизация в корпоративной среде зависит от службы Azure Information Protection, которая доступна не во всех подписках M365.</span><span class="sxs-lookup"><span data-stu-id="b5419-172">Enterprise sync depends on Azure Information Protection, which is not available in all M365 subscriptions.</span></span>

#### <span data-ttu-id="b5419-173">Основана ли функция синхронизации Microsoft Edge на Enterprise State Roaming?</span><span class="sxs-lookup"><span data-stu-id="b5419-173">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="b5419-174">Нет.</span><span class="sxs-lookup"><span data-stu-id="b5419-174">No.</span></span> <span data-ttu-id="b5419-175">ESR может использоваться для включения синхронизации, но функция синхронизации Microsoft Edge не входит в состав ESR.</span><span class="sxs-lookup"><span data-stu-id="b5419-175">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="b5419-176">Дополнительные сведения см. в разделах [Функция синхронизации Microsoft Edge](microsoft-edge-enterprise-sync.md) и [Microsoft Edge и Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="b5419-176">For more information, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) and [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

#### <span data-ttu-id="b5419-177">Будет ли Microsoft Edge поддерживать синхронизацию между Microsoft Edge и IE?</span><span class="sxs-lookup"><span data-stu-id="b5419-177">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="b5419-178">Поддержка такой синхронизации не планируется.</span><span class="sxs-lookup"><span data-stu-id="b5419-178">There are no plans to support this syncing.</span></span> <span data-ttu-id="b5419-179">Если для поддержки устаревших приложений вам нужен IE, подумайте об использовании [нового режима IE](https://docs.microsoft.com/deployedge/edge-ie-mode).</span><span class="sxs-lookup"><span data-stu-id="b5419-179">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="b5419-180">Будет ли Microsoft Edge синхронизироваться с устаревшей версией Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="b5419-180">Will Microsoft Edge sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="b5419-181">Нет, не будет.</span><span class="sxs-lookup"><span data-stu-id="b5419-181">No, it won't.</span></span> <span data-ttu-id="b5419-182">Мы считаем, что объединение этих двух экосистем может привести к нарушению надежности синхронизации в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b5419-182">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the Microsoft Edge.</span></span> <span data-ttu-id="b5419-183">Мы обеспечим перенос имеющихся данных в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b5419-183">We will ensure that existing data is migrated to the Microsoft Edge.</span></span> <span data-ttu-id="b5419-184">Кроме того, пользователи смогут импортировать данные из браузера, которым они пользуются.</span><span class="sxs-lookup"><span data-stu-id="b5419-184">Users will also be able to import data from browser of their choice.</span></span> <span data-ttu-id="b5419-185">Это также означает, что синхронизация между новым браузером Microsoft Edge и браузером Internet Explorer выполняться не будет.</span><span class="sxs-lookup"><span data-stu-id="b5419-185">This also means that new Microsoft Edge browser won't have a way to sync with IE.</span></span>

### <span data-ttu-id="b5419-186">УПРАВЛЕНИЕ СИНХРОНИЗАЦИЕЙ</span><span class="sxs-lookup"><span data-stu-id="b5419-186">MANAGING SYNC</span></span>

#### <span data-ttu-id="b5419-187">Можно ли запретить пользователям синхронизацию с личным клиентом?</span><span class="sxs-lookup"><span data-stu-id="b5419-187">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="b5419-188">Прямо нет, но вы можете определить, с каким профилем можно входить в Microsoft Edge, с помощью политики [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).</span><span class="sxs-lookup"><span data-stu-id="b5419-188">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="b5419-189">См. также</span><span class="sxs-lookup"><span data-stu-id="b5419-189">See also</span></span>

- [<span data-ttu-id="b5419-190">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="b5419-190">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="b5419-191">Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="b5419-191">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
