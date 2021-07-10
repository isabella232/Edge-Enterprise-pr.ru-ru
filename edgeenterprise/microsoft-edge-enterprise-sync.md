---
title: Настройка синхронизации Microsoft Edge Enterprise
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Параметры пользователя и администратора для настройки синхронизации избранного, паролей и других данных браузера в Microsoft Edge.
ms.openlocfilehash: 5e3813664d3942e84d38e4ae1b4fd17e41049cda
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642825"
---
# <a name="configure-microsoft-edge-enterprise-sync"></a><span data-ttu-id="f54d5-103">Настройка синхронизации Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="f54d5-103">Configure Microsoft Edge enterprise sync</span></span>

<span data-ttu-id="f54d5-104">В этой статье рассказывается о том, как администраторы могут настроить для пользователя синхронизацию избранного, паролей и других данных браузера в Microsoft Edge на всех устройствах, на которых выполнен вход. Если вы не являетесь администратором, ознакомьтесь со статьей о том, как выполнять вход и синхронизацию Microsoft Edge на разных устройствах.</span><span class="sxs-lookup"><span data-stu-id="f54d5-104">This article explains how admins can configure Microsoft Edge to sync user favorites, passwords, and other browser data across all signed-in devices.If you are not an admin, please visit this article for how to sign-in and sync Microsoft Edge across devices.</span></span> <span data-ttu-id="f54d5-105">[Войдите, чтобы синхронизировать Microsoft Edge на разных устройствах](https://support.microsoft.com/microsoft-edge/sign-in-to-sync-microsoft-edge-across-devices-e6ffa79b-ed52-aa32-47e2-5d5597fe4674).</span><span class="sxs-lookup"><span data-stu-id="f54d5-105">[Sign in to sync Microsoft Edge across devices](https://support.microsoft.com/microsoft-edge/sign-in-to-sync-microsoft-edge-across-devices-e6ffa79b-ed52-aa32-47e2-5d5597fe4674).</span></span>

> [!NOTE]
> <span data-ttu-id="f54d5-106">Применяется к Microsoft Edge версии 77 или более поздней, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="f54d5-106">Applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <a name="overview"></a><span data-ttu-id="f54d5-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="f54d5-107">Overview</span></span>

<span data-ttu-id="f54d5-108">Функция синхронизации Microsoft Edge позволяет пользователям получать доступ к данным браузера на всех своих устройствах, на которых они выполняют вход в систему.</span><span class="sxs-lookup"><span data-stu-id="f54d5-108">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="f54d5-109">К данным, поддерживаемым функцией синхронизации, относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="f54d5-109">The data supported by sync includes:</span></span>

- <span data-ttu-id="f54d5-110">Избранное</span><span class="sxs-lookup"><span data-stu-id="f54d5-110">Favorites</span></span>
- <span data-ttu-id="f54d5-111">Пароли</span><span class="sxs-lookup"><span data-stu-id="f54d5-111">Passwords</span></span>
- <span data-ttu-id="f54d5-112">Адреса и прочее (заполнения форм)</span><span class="sxs-lookup"><span data-stu-id="f54d5-112">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="f54d5-113">Коллекции</span><span class="sxs-lookup"><span data-stu-id="f54d5-113">Collections</span></span>
- <span data-ttu-id="f54d5-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="f54d5-114">Settings</span></span>
- <span data-ttu-id="f54d5-115">Расширение</span><span class="sxs-lookup"><span data-stu-id="f54d5-115">Extension</span></span>
- <span data-ttu-id="f54d5-116">Открытые вкладки (доступно в Microsoft Edge версии 88)</span><span class="sxs-lookup"><span data-stu-id="f54d5-116">Open tabs (available in Microsoft Edge version 88)</span></span>
- <span data-ttu-id="f54d5-117">Журнал (доступно в Microsoft Edge версии 88)</span><span class="sxs-lookup"><span data-stu-id="f54d5-117">History (available in Microsoft Edge version 88)</span></span>

<span data-ttu-id="f54d5-118">Функциональность синхронизации включается путем предоставления согласия пользователя. Пользователи могут включать или отключать синхронизацию для каждого из перечисленных выше типов данных.</span><span class="sxs-lookup"><span data-stu-id="f54d5-118">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span> <span data-ttu-id="f54d5-119">Если у пользователя возникли проблемы с синхронизацией, может потребоваться сброс синхронизации в разделе **Параметры** > **Профили** > **Сбросить синхронизацию**.</span><span class="sxs-lookup"><span data-stu-id="f54d5-119">If a user is experiencing a sync issue they might need to reset sync in **Settings** > **Profiles** > **Reset sync**.</span></span>

> [!NOTE]
> <span data-ttu-id="f54d5-120">Для поддержки функциональности синхронизации передаются дополнительные данные о подключении устройства и конфигурации (например, имя устройства, изготовитель и модель).</span><span class="sxs-lookup"><span data-stu-id="f54d5-120">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f54d5-121">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="f54d5-121">Prerequisites</span></span>

<span data-ttu-id="f54d5-122">Функция синхронизации Microsoft Edge для учетных записей Azure Active Directory (Azure AD) доступна в рамках любой из этих подписок:</span><span class="sxs-lookup"><span data-stu-id="f54d5-122">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="f54d5-123">Azure AD Premium (P1 или P2)</span><span class="sxs-lookup"><span data-stu-id="f54d5-123">Azure AD Premium (P1 or P2)</span></span>
- <span data-ttu-id="f54d5-124">M365 бизнес премиум</span><span class="sxs-lookup"><span data-stu-id="f54d5-124">M365 Business Premium</span></span>
- <span data-ttu-id="f54d5-125">Office 365 E1 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="f54d5-125">Office 365 E1 and above</span></span>
- <span data-ttu-id="f54d5-126">Azure Information Protection (AIP) (P1 или P2)</span><span class="sxs-lookup"><span data-stu-id="f54d5-126">Azure Information Protection (AIP) (P1 or P2)</span></span>
- <span data-ttu-id="f54d5-127">Все подписки EDU (приложения Майкрософт для учащихся или преподавателей, Exchange Online для учащихся или преподавателей, O365 A1 или выше, M365 A1 или выше, Azure Information Protection P1 или P2 для учащихся или преподавателей)</span><span class="sxs-lookup"><span data-stu-id="f54d5-127">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <a name="sync-group-policies"></a><span data-ttu-id="f54d5-128">Синхронизация групповых политик</span><span class="sxs-lookup"><span data-stu-id="f54d5-128">Sync group policies</span></span>

<span data-ttu-id="f54d5-129">Администраторы могут использовать следующие групповые политики для настройки и управления синхронизацией Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="f54d5-129">Admins can use the following group policies to configure and manage Microsoft Edge sync:</span></span>

- <span data-ttu-id="f54d5-130">[SyncDisabled](./microsoft-edge-policies.md#syncdisabled): полное отключение синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f54d5-130">[SyncDisabled](./microsoft-edge-policies.md#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="f54d5-131">[SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): отключает сохранение журнала браузера и синхронизацию. Эта политика также отключает синхронизацию открытых вкладок.</span><span class="sxs-lookup"><span data-stu-id="f54d5-131">[SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="f54d5-132">[AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): если эта политика отключена, синхронизация журнала также будет отключена.</span><span class="sxs-lookup"><span data-stu-id="f54d5-132">[AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.</span></span>
- <span data-ttu-id="f54d5-133">[SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): настройка списка типов, исключенных из синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f54d5-133">[SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="f54d5-134">[RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): разрешает профилям Active Directory (AD) использовать локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="f54d5-134">[RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="f54d5-135">Дополнительные сведения см. в статье [Локальная синхронизация для пользователей Active Directory (AD)](./microsoft-edge-on-premises-sync.md).</span><span class="sxs-lookup"><span data-stu-id="f54d5-135">For more information, see [On-premises sync for Active Directory (AD) users](./microsoft-edge-on-premises-sync.md).</span></span>
- <span data-ttu-id="f54d5-136">[ForceSync:](/deployedge/microsoft-edge-policies#forcesync) включает синхронизацию по умолчанию и не требует согласия пользователя.</span><span class="sxs-lookup"><span data-stu-id="f54d5-136">[ForceSync](/deployedge/microsoft-edge-policies#forcesync): Turn on sync by default and do not require user consent to sync.</span></span>  

## <a name="configure-microsoft-edge-sync"></a><span data-ttu-id="f54d5-137">Настройка синхронизации Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f54d5-137">Configure Microsoft Edge sync</span></span>

<span data-ttu-id="f54d5-138">Параметры конфигурации для функции синхронизации Microsoft Edge доступны в службе Azure Information Protection (AIP).</span><span class="sxs-lookup"><span data-stu-id="f54d5-138">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="f54d5-139">Если служба AIP включена для клиента, все пользователи могут синхронизировать данные в Microsoft Edge независимо от типа лицензии.</span><span class="sxs-lookup"><span data-stu-id="f54d5-139">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="f54d5-140">Инструкции по включению службы AIP см. [здесь](/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="f54d5-140">Instructions on how to enable AIP can be found [here](/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="f54d5-141">Чтобы ограничить синхронизацию для определенной группы пользователей, вы можете включить для них [политику управления регистрацией в AIP](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) .</span><span class="sxs-lookup"><span data-stu-id="f54d5-141">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) for those users.</span></span> <span data-ttu-id="f54d5-142">Если после регистрации всех необходимых пользователей синхронизация все еще недоступна, убедитесь в том, что служба IPCv3Service включена, используя командлет PowerShell [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps).</span><span class="sxs-lookup"><span data-stu-id="f54d5-142">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="f54d5-143">При включении службы Azure Information Protection другие приложения, такие как Microsoft Word и Microsoft Outlook, также смогут защищать контент с помощью AIP.</span><span class="sxs-lookup"><span data-stu-id="f54d5-143">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="f54d5-144">Кроме того, любая политика управления регистрацией, используемая для ограничения синхронизации Microsoft Edge, также ограничит защиту контента с помощью AIP в других приложениях.</span><span class="sxs-lookup"><span data-stu-id="f54d5-144">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <a name="microsoft-edge-and-enterprise-state-roaming-esr"></a><span data-ttu-id="f54d5-145">Microsoft Edge и Enterprise State Roaming (ESR)</span><span class="sxs-lookup"><span data-stu-id="f54d5-145">Microsoft Edge and Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="f54d5-146">Microsoft Edge — это межплатформенное приложение с широкими возможностями синхронизации пользовательских данных на всех используемых устройствах. Приложение больше не входит состав службы Enterprise State Roaming в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f54d5-146">Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="f54d5-147">Однако в Microsoft Edge будут реализованы средства защиты данных, аналогичные ESR, такие как возможность использования собственного ключа.</span><span class="sxs-lookup"><span data-stu-id="f54d5-147">However, the Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="f54d5-148">Дополнительные сведения см. в разделе [Microsoft Edge и Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span><span class="sxs-lookup"><span data-stu-id="f54d5-148">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f54d5-149">См. также</span><span class="sxs-lookup"><span data-stu-id="f54d5-149">See also</span></span>

- [<span data-ttu-id="f54d5-150">Синхронизация Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="f54d5-150">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="f54d5-151">Диагностика и устранение проблем синхронизации Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f54d5-151">Diagnose and fix Microsoft Edge sync issues</span></span>](microsoft-edge-troubleshoot-enterprise-sync.md)
- [<span data-ttu-id="f54d5-152">Microsoft Edge и Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="f54d5-152">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="f54d5-153">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="f54d5-153">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)