---
title: Диагностика и устранение проблем синхронизации Microsoft Edge
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Инструкции и средства, доступные администратору Microsoft Edge для устранения неполадок и решения распространенных проблем синхронизации для предприятий
ms.openlocfilehash: 0aca8c98492aead0673b5738aa5dba85c3a34314
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642235"
---
# <a name="diagnose-and-fix-microsoft-edge-sync-issues"></a><span data-ttu-id="1aa14-103">Диагностика и устранение проблем синхронизации Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1aa14-103">Diagnose and fix Microsoft Edge sync issues</span></span>

<span data-ttu-id="1aa14-104">В этой статье содержится руководство по устранению наиболее распространенных проблем синхронизации в среде Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="1aa14-104">This article provides troubleshooting guidance for the most commonly encountered sync issues in an Azure Active Directory (Azure AD) environment.</span></span> <span data-ttu-id="1aa14-105">Эта статья также содержит сведения о рекомендуемых средствах для сбора журналов, необходимых для устранения проблем синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1aa14-105">It also includes the recommended tools for gathering the logs needed for troubleshooting a sync issue.</span></span>

<span data-ttu-id="1aa14-106">Если у пользователя возникла проблема с синхронизацией данных браузера на устройствах, он может попытаться [сбросить синхронизацию](edge-learnmore-reset-data-in-cloud.md). Если это не поможет, администраторы или сотрудники службы поддержки могут использовать следующие инструкции для устранения проблемы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1aa14-106">If a user is experiencing an issue syncing browser data across their devices they can try [resetting sync](edge-learnmore-reset-data-in-cloud.md). If this doesn't work, admins or support staff can use the following guidance to fix a sync issue.</span></span>

> [!NOTE]
> <span data-ttu-id="1aa14-107">Применяется к Microsoft Edge версии 77 или более поздней, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="1aa14-107">Applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <a name="identity-issues-versus-sync-issues"></a><span data-ttu-id="1aa14-108">Проблемы с удостоверениями и проблемы синхронизации</span><span class="sxs-lookup"><span data-stu-id="1aa14-108">Identity issues versus sync issues</span></span>

<span data-ttu-id="1aa14-109">Перед началом работы важно понять разницу между проблемами с удостоверениями и проблемами синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1aa14-109">Before you begin it's important to understand the difference between identity issues and sync issues.</span></span> <span data-ttu-id="1aa14-110">Наиболее популярный способ сохранения удостоверений пользователей в браузере — поддержка синхронизации. Поэтому проблемы с удостоверениями часто путают с проблемами синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1aa14-110">A popular use case for maintaining user identity in the browser is to support sync. For this reason, identity issues are frequently confused with sync issues.</span></span> <span data-ttu-id="1aa14-111">Прежде чем приступить к устранению неполадок синхронизации, необходимо понять разницу между проблемами с удостоверениями и проблемами синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1aa14-111">Understand the difference between identity and sync issue before you start troubleshooting sync.</span></span>

<span data-ttu-id="1aa14-112">Прежде чем решать проблему синхронизации, проверьте, вошел ли пользователь в браузер с помощью действительной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1aa14-112">Before you treat an issue as a sync issue, check to see if the user is signed into the browser with a valid account.</span></span>

<span data-ttu-id="1aa14-113">На следующем снимке экрана показан пример ошибки удостоверения.</span><span class="sxs-lookup"><span data-stu-id="1aa14-113">The next screenshot shows an example of an identity error.</span></span> <span data-ttu-id="1aa14-114">Сообщение об ошибке: "**Последняя ошибка токена, EDGE_AUTH_ERROR: 3, 54, 3ea**", которая находится в *edge://sync-internals* в разделе **Учетные данные**:</span><span class="sxs-lookup"><span data-stu-id="1aa14-114">The error is "**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**", which is found in *edge://sync-internals* under **Credentials**:</span></span>

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Последняя ошибка токена EDGE_AUTH_ERROR: 3,54, 3ea":::

## <a name="common-sync-issues"></a><span data-ttu-id="1aa14-116">Распространенные проблемы синхронизации</span><span class="sxs-lookup"><span data-stu-id="1aa14-116">Common sync issues</span></span>

### <a name="issue-cant-access-m365-or-azure-information-protection-subscription"></a><span data-ttu-id="1aa14-117">Проблема: Нет доступа к подписке M365 или Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="1aa14-117">Issue: Can't access M365 or Azure Information Protection subscription</span></span>

<span data-ttu-id="1aa14-118">У вас есть предыдущая подписка M365 или Azure Information Protection (AIP), срок действия которой истек, и которая затем была заменена новой подпиской?</span><span class="sxs-lookup"><span data-stu-id="1aa14-118">Do you have a previous M365 or Azure Information Protection (AIP) subscription that expired and then replaced with a new subscription?</span></span> <span data-ttu-id="1aa14-119">Если да, то ИД клиента изменился и данные службы нужно сбросить.</span><span class="sxs-lookup"><span data-stu-id="1aa14-119">If so, then the tenant ID has changed and the service data needs to be reset.</span></span> <span data-ttu-id="1aa14-120">Инструкции по сбросу данных см. в разделе **Ошибка кодировщика**.</span><span class="sxs-lookup"><span data-stu-id="1aa14-120">See the instructions for resetting data in the **Cryptographer error encountered** issue.</span></span>

### <a name="issue-sync-is-not-available-for-this-account"></a><span data-ttu-id="1aa14-121">Проблема: "Синхронизация для этой учетной записи недоступна".</span><span class="sxs-lookup"><span data-stu-id="1aa14-121">Issue: “Sync is not available for this account.”</span></span>

<span data-ttu-id="1aa14-122">Если эта ошибка обнаружена для учетной записи Azure Active Directory или если в *edge://sync-internals* отображается DISABLED_BY_ADMIN, последовательно выполните инструкции, описанные в следующей процедуре, пока проблема не будет устранена.</span><span class="sxs-lookup"><span data-stu-id="1aa14-122">If this error is encountered for an Azure Active Directory account, or if DISABLED_BY_ADMIN appears in *edge://sync-internals*, follow the steps in the next procedure sequentially until the problem is fixed.</span></span>

> [!NOTE]
> <span data-ttu-id="1aa14-123">Поскольку источник этой ошибки обычно требует изменения конфигурации в клиенте Azure Active Directory, эти действия по устранению неполадок может выполнить только администратор клиента, а не пользователь.</span><span class="sxs-lookup"><span data-stu-id="1aa14-123">Because the source of this error is usually requires a configuration change in an Azure Active Directory tenant, these troubleshooting steps can only performed by a tenant admin and not by end users.</span></span>

1. <span data-ttu-id="1aa14-124">Убедитесь, что у корпоративного клиента есть поддерживаемая подписка M365.</span><span class="sxs-lookup"><span data-stu-id="1aa14-124">Verify that the enterprise tenant has a supported M365 subscription.</span></span> <span data-ttu-id="1aa14-125">Текущий список доступных типов подписки [представлен здесь](/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="1aa14-125">The current list of available subscription types is [provided here](/azure/information-protection/activate-office365).</span></span> <span data-ttu-id="1aa14-126">Если у клиента нет поддерживаемой подписки, он можно приобрести Azure Information Protection отдельно или обновиться до одной из поддерживаемых подписок.</span><span class="sxs-lookup"><span data-stu-id="1aa14-126">If the tenant doesn't have a supported subscription, they can either purchase Azure Information Protection separately, or upgrade to one of the supported subscriptions.</span></span>
2. <span data-ttu-id="1aa14-127">Если поддерживаемая подписка доступна, убедитесь, что у клиента есть служба Azure Information Protection (AIP).</span><span class="sxs-lookup"><span data-stu-id="1aa14-127">If a supported subscription is available, verify that the tenant has Azure Information Protection (AIP) available.</span></span> <span data-ttu-id="1aa14-128">Инструкции по проверке состояния службы AIP и, если требуется, по ее активации см. [здесь](/azure/information-protection/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="1aa14-128">The instructions for checking the AIP status and, if necessary, activating AIP are [here](/azure/information-protection/activate-office365).</span></span>
3. <span data-ttu-id="1aa14-129">Если на шаге 2 видно, что AIP активен, но синхронизация по-прежнему не работает, включите Enterprise State Roaming (ESR).</span><span class="sxs-lookup"><span data-stu-id="1aa14-129">If step 2 shows that AIP is active but sync still doesn't work, turn on Enterprise State Roaming (ESR).</span></span> <span data-ttu-id="1aa14-130">Инструкции по включению ESR см. [здесь](/azure/active-directory/devices/enterprise-state-roaming-enable).</span><span class="sxs-lookup"><span data-stu-id="1aa14-130">The instructions for enabling ESR are [here](/azure/active-directory/devices/enterprise-state-roaming-enable).</span></span> <span data-ttu-id="1aa14-131">Обратите внимание, что служба ESR не должна оставаться включенной.</span><span class="sxs-lookup"><span data-stu-id="1aa14-131">Note that ESR does not need to stay on.</span></span> <span data-ttu-id="1aa14-132">Если на этом шаге проблема исправлена, службу ESR можно отключить.</span><span class="sxs-lookup"><span data-stu-id="1aa14-132">You can turn off ESR if this step fixes the issue.</span></span>
4. <span data-ttu-id="1aa14-133">Убедитесь, что служба Azure Information Protection не ограничена с помощью политики регистрации.</span><span class="sxs-lookup"><span data-stu-id="1aa14-133">Confirm that Azure Information Protection is not scoped via an onboarding policy.</span></span> <span data-ttu-id="1aa14-134">Вы можете использовать приложение PowerShell [Get-AadrmOnboardingControlPolicy](/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps), чтобы узнать, включено ли ограничение.</span><span class="sxs-lookup"><span data-stu-id="1aa14-134">You can use the [Get-AadrmOnboardingControlPolicy](/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell applet to see if scoping is enabled.</span></span> <span data-ttu-id="1aa14-135">В следующих двух примерах показана неограниченная конфигурация и конфигурация, ограниченная определенной группой безопасности.</span><span class="sxs-lookup"><span data-stu-id="1aa14-135">The next two examples show an unscoped configuration and a configuration scoped to a specific security group.</span></span>

   ```powershell
    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False 
   ```

   ```powershell

    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False f1488a05-8196-40a6-9483-524948b90282   All
   ```

   <span data-ttu-id="1aa14-136">Если ограничение включено, затронутый пользователь должен быть либо добавлен в группу безопасности для ограничения, либо ограничение должно быть удалено.</span><span class="sxs-lookup"><span data-stu-id="1aa14-136">If scoping is enabled, the affected user should either be added to the security group for the scope, or the scope should be removed.</span></span> <span data-ttu-id="1aa14-137">В приведенном ниже примере регистрация ограничила AIP указанной группой безопасности и ограничение должно быть удалено с помощью приложения PowerShell [Set-AadrmOnboardingControlPolicy](/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps).</span><span class="sxs-lookup"><span data-stu-id="1aa14-137">In the example below, onboarding has scoped AIP to the indicated security group and the scoping should be removed with the [Set-AadrmOnboardingControlPolicy](/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell applet.</span></span>

5. <span data-ttu-id="1aa14-138">Убедитесь, что в клиенте включена служба IPCv3Service.</span><span class="sxs-lookup"><span data-stu-id="1aa14-138">Confirm that the IPCv3Service is turned on in the tenant.</span></span> <span data-ttu-id="1aa14-139">Приложение PowerShell [Get-AadrmConfiguration](/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps) показывает состояние службы.</span><span class="sxs-lookup"><span data-stu-id="1aa14-139">The [Get-AadrmConfiguration](/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps)  PowerShell applet shows the status of the service.</span></span>

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Проверьте, включена ли служба IPCv3Service.":::

6. <span data-ttu-id="1aa14-141">Если проблема не исчезла, обратитесь в [службу поддержки Microsoft Edge](https://www.microsoftedgeinsider.com/support).</span><span class="sxs-lookup"><span data-stu-id="1aa14-141">If the issue isn't fixed, contact [Microsoft Edge support](https://www.microsoftedgeinsider.com/support).</span></span>

### <a name="issue-stuck-at-setting-up-sync-or-couldnt-connect-to-the-sync-server-retrying"></a><span data-ttu-id="1aa14-142">Проблема: Зависание с состоянием "Настройка синхронизации..." или "Не удалось подключиться к серверу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1aa14-142">Issue: Stuck at "Setting up sync..." or “Couldn’t connect to the sync server.</span></span> <span data-ttu-id="1aa14-143">Выполняется повторная попытка..."</span><span class="sxs-lookup"><span data-stu-id="1aa14-143">Retrying…”</span></span>

1. <span data-ttu-id="1aa14-144">Попробуйте выйти из системы и снова в нее войти.</span><span class="sxs-lookup"><span data-stu-id="1aa14-144">Try to sign out and then sign in.</span></span>
2. <span data-ttu-id="1aa14-145">Перейдите в *edge://sync-internals*.</span><span class="sxs-lookup"><span data-stu-id="1aa14-145">Go to *edge://sync-internals*.</span></span> <span data-ttu-id="1aa14-146">Если в разделе "**Сведения о типе**" присутствует следующая ошибка, переходите к следующей проблеме, **Ошибка кодировщика**.</span><span class="sxs-lookup"><span data-stu-id="1aa14-146">If under the "**Type info**" section the following error is present, then  skip to the following issue, **Cryptographer error encountered**.</span></span>

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. <span data-ttu-id="1aa14-147">Попробуйте проверить связь с конечной точкой сервера.</span><span class="sxs-lookup"><span data-stu-id="1aa14-147">Try pinging the server endpoint.</span></span> <span data-ttu-id="1aa14-148">Конечная точка сервера для клиента доступна в *edge://sync-internals*.</span><span class="sxs-lookup"><span data-stu-id="1aa14-148">The server endpoint for a client is available in *edge://sync-internals*.</span></span> <span data-ttu-id="1aa14-149">На следующем снимке экрана показаны сведения о конечной точке в разделе **Сведения об окружении**.</span><span class="sxs-lookup"><span data-stu-id="1aa14-149">The next screenshot shows endpoint information under **Environment Info**.</span></span>

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info.png" alt-text="Сведения о конечной точке":::

4. <span data-ttu-id="1aa14-151">Если конечная точка сервера пуста или связь с сервером не может быть проверена и в среде присутствует брандмауэр, убедитесь, что для клиентского компьютера доступны необходимые конечные точки службы.</span><span class="sxs-lookup"><span data-stu-id="1aa14-151">If the server endpoint is empty, or if server cannot be pinged and a firewall is present in the environment, confirm that the necessary service endpoints are available to the client computer.</span></span>

   - <span data-ttu-id="1aa14-152">Конечные точки службы синхронизации Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="1aa14-152">Microsoft Edge sync service endpoints:</span></span>
     - [https://edge-enterprise.activity.windows.com](https://edge-enterprise.activity.windows.com)
     - [https://edge.activity.windows.com](https://edge.activity.windows.com)
    - <span data-ttu-id="1aa14-153">Конечные точки Azure Information Protection:</span><span class="sxs-lookup"><span data-stu-id="1aa14-153">Azure Information Protection endpoints:</span></span>
      - <span data-ttu-id="1aa14-154">[https://api.aadrm.com](https://api.aadrm.com) (для большинства клиентов)</span><span class="sxs-lookup"><span data-stu-id="1aa14-154">[https://api.aadrm.com](https://api.aadrm.com) (for most tenants)</span></span>
      - <span data-ttu-id="1aa14-155">[https://api.aadrm.de](https://api.aadrm.de) (для клиентов в Германии)</span><span class="sxs-lookup"><span data-stu-id="1aa14-155">[https://api.aadrm.de](https://api.aadrm.de) (for tenants in Germany)</span></span>
      - <span data-ttu-id="1aa14-156">[https://api.aadrm.cn](https://api.aadrm.cn) (для клиентов в Китае)</span><span class="sxs-lookup"><span data-stu-id="1aa14-156">[https://api.aadrm.cn](https://api.aadrm.cn) (for tenants in China)</span></span>
   - <span data-ttu-id="1aa14-157">[Конечные точки службы уведомлений Windows.](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)</span><span class="sxs-lookup"><span data-stu-id="1aa14-157">[Windows Notification Service endpoints](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).</span></span>

5. <span data-ttu-id="1aa14-158">Если проблема не устранена, обратитесь в [службу поддержки Microsoft Edge](https://www.microsoftedgeinsider.com/support).</span><span class="sxs-lookup"><span data-stu-id="1aa14-158">If the issue still isn't fixed, contact [Microsoft Edge support](https://www.microsoftedgeinsider.com/support).</span></span>

### <a name="issue-cryptographer-error-encountered"></a><span data-ttu-id="1aa14-159">Проблема: Ошибка кодировщика</span><span class="sxs-lookup"><span data-stu-id="1aa14-159">Issue: Cryptographer error encountered</span></span>

<span data-ttu-id="1aa14-160">Эта ошибка отображается в разделе **Сведения о типе** в *edge://sync-internals* и может означать, что требуется сбросить данные на стороне службы пользователя.</span><span class="sxs-lookup"><span data-stu-id="1aa14-160">This error is visible under **Type info** in *edge://sync-internals* and may mean that the user's service side data needs to be reset.</span></span> <span data-ttu-id="1aa14-161">В следующем примере показано сообщение об ошибке шифрования:</span><span class="sxs-lookup"><span data-stu-id="1aa14-161">The following example shows a cryptography error message:</span></span>
<br><span data-ttu-id="1aa14-162">"Error:GenerateCryptoErrorsForTypes@.. /.. /components/sync/driver/data_type_manager_impl.cc:42, произошла ошибка кодировщика".</span><span class="sxs-lookup"><span data-stu-id="1aa14-162">"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered".</span></span>

1. <span data-ttu-id="1aa14-163">Перезапустите Microsoft Edge, перейдите в *edge://sync-internals* и проверьте раздел "**Состояние ключа учетной записи AAD**"</span><span class="sxs-lookup"><span data-stu-id="1aa14-163">Restart Microsoft Edge and navigate to *edge://sync-internals* and check the “**AAD Account Key Status**” section</span></span>
   - <span data-ttu-id="1aa14-164">Пункт "Последний результат MIP" имеет значение "Успешно": ошибка кодировщика означает, что данные сервера могут быть зашифрованы с помощью потерянного ключа.</span><span class="sxs-lookup"><span data-stu-id="1aa14-164">"Success" in "Last MIP Result": the cryptographer error means server data might be encrypted with a lost key.</span></span> <span data-ttu-id="1aa14-165">Для возобновления синхронизации требуется сброс данных.</span><span class="sxs-lookup"><span data-stu-id="1aa14-165">Data reset is needed to resume sync.</span></span>
   - <span data-ttu-id="1aa14-166">Пункт "Последний результат MIP" имеет значение "Нет разрешений": возможно, это вызвано изменением Azure AD или изменением подписки клиента.</span><span class="sxs-lookup"><span data-stu-id="1aa14-166">"No permissions" in "Last MIP Result": It is possibly caused by an Azure AD change or tenant subscription changes.</span></span> <span data-ttu-id="1aa14-167">Для возобновления синхронизации требуется сброс данных.</span><span class="sxs-lookup"><span data-stu-id="1aa14-167">Data reset is needed to resume sync.</span></span>
   - <span data-ttu-id="1aa14-168">Другие ошибки могут означать проблемы с конфигурацией сервера.</span><span class="sxs-lookup"><span data-stu-id="1aa14-168">Other errors may mean server configuration issues.</span></span>
2. <span data-ttu-id="1aa14-169">Если требуется сброс данных, см. статью [Сброс данных Microsoft Edge в облаке](edge-learnmore-reset-data-in-cloud.md).</span><span class="sxs-lookup"><span data-stu-id="1aa14-169">If data reset is needed, see [Reset Microsoft Edge data in the cloud](edge-learnmore-reset-data-in-cloud.md).</span></span>

### <a name="issue-sync-has-been-turned-off-by-your-administrator"></a><span data-ttu-id="1aa14-170">Проблема: "Синхронизация отключена администратором".</span><span class="sxs-lookup"><span data-stu-id="1aa14-170">Issue: “Sync has been turned off by your administrator.”</span></span>

<span data-ttu-id="1aa14-171">Убедитесь, что [политика SyncDisabled](./microsoft-edge-policies.md#syncdisabled) не установлена.</span><span class="sxs-lookup"><span data-stu-id="1aa14-171">Make sure that the [SyncDisabled policy](./microsoft-edge-policies.md#syncdisabled)  is not set.</span></span>

## <a name="see-also"></a><span data-ttu-id="1aa14-172">См. также</span><span class="sxs-lookup"><span data-stu-id="1aa14-172">See also</span></span>

- [<span data-ttu-id="1aa14-173">Синхронизация Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="1aa14-173">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="1aa14-174">Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming</span><span class="sxs-lookup"><span data-stu-id="1aa14-174">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="1aa14-175">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="1aa14-175">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)