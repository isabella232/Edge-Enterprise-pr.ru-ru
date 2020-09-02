---
title: Поддержка Windows Information Protection в Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 04/24/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Поддержка Windows Information Protection в Microsoft Edge
ms.openlocfilehash: 4ec48d258deb1cf6d4436716f14aa2561cee2a50
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980997"
---
# <span data-ttu-id="f5095-103">Поддержка Windows Information Protection (WIP) в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f5095-103">Microsoft Edge support for Windows Information Protection (WIP)</span></span>

<span data-ttu-id="f5095-104">В этой статье объясняется, как Microsoft Edge поддерживает Windows Information Protection (WIP).</span><span class="sxs-lookup"><span data-stu-id="f5095-104">This article describes how Microsoft Edge supports Windows Information Protection (WIP).</span></span>

> [!NOTE]
> <span data-ttu-id="f5095-105">Эта статья относится к Microsoft Edge версии 81 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="f5095-105">This applies to Microsoft Edge version 81 or later.</span></span>

## <span data-ttu-id="f5095-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="f5095-106">Overview</span></span>

<span data-ttu-id="f5095-107">Windows Information Protection (WIP) — это функция Windows 10, которая помогает защитить корпоративные данные от несанкционированного или случайного раскрытия.</span><span class="sxs-lookup"><span data-stu-id="f5095-107">Windows Information Protection (WIP) is a Windows 10 feature that helps protect enterprise data from unauthorized or accidental disclosure.</span></span> <span data-ttu-id="f5095-108">С ростом популярности удаленной работы увеличивается риск общего доступа к корпоративным данным за пределами рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f5095-108">With the rise of remote work, there's an increased risk of sharing corporate data outside the workplace.</span></span> <span data-ttu-id="f5095-109">Этот риск возрастает, если личные действия и рабочие действия выполняются на корпоративных устройствах.</span><span class="sxs-lookup"><span data-stu-id="f5095-109">This risk increases when personal activities and work activities occur on corporate devices.</span></span>

<span data-ttu-id="f5095-110">Microsoft Edge поддерживает WIP, чтобы защитить содержимое в веб-среде, где пользователи часто делятся содержимым и распространяют его.</span><span class="sxs-lookup"><span data-stu-id="f5095-110">Microsoft Edge supports WIP to help protect content in a web environment where users often share and distribute content.</span></span>

### <span data-ttu-id="f5095-111">Требования к системе</span><span class="sxs-lookup"><span data-stu-id="f5095-111">System requirements</span></span>

<span data-ttu-id="f5095-112">К мобильным устройствам, использующим WIP в корпоративной среде, применяются следующие требования:</span><span class="sxs-lookup"><span data-stu-id="f5095-112">The follow requirements apply to devices using WIP in the enterprise:</span></span>

- <span data-ttu-id="f5095-113">Windows10 версии1607 или более поздней</span><span class="sxs-lookup"><span data-stu-id="f5095-113">Windows 10, version 1607 or later</span></span>
- <span data-ttu-id="f5095-114">Только номера SKU клиентов Windows</span><span class="sxs-lookup"><span data-stu-id="f5095-114">Only Windows client SKUs</span></span>
- <span data-ttu-id="f5095-115">Одно из решений для управления, описанных в статье [Необходимые компоненты WIP](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#prerequisites)</span><span class="sxs-lookup"><span data-stu-id="f5095-115">One of the management solutions described in [WIP prerequisites](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#prerequisites)</span></span>

### <span data-ttu-id="f5095-116">Преимущества Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="f5095-116">Windows Information Protection benefits</span></span>

<span data-ttu-id="f5095-117">WIP обеспечивает следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="f5095-117">WIP provides the following benefits:</span></span>

- <span data-ttu-id="f5095-118">Очевидное разделение между персональными и корпоративными данными без необходимости переключения сотрудниками сред или приложений.</span><span class="sxs-lookup"><span data-stu-id="f5095-118">Obvious separation between personal and corporate data, without requiring employees to switch environments or apps.</span></span>
- <span data-ttu-id="f5095-119">Дополнительная защита данных в существующих бизнес-приложениях без необходимости обновления приложений.</span><span class="sxs-lookup"><span data-stu-id="f5095-119">Additional data protection for existing line-of-business apps without a need to update the apps.</span></span>
- <span data-ttu-id="f5095-120">Возможность удаленной очистки корпоративных данных, не затрагивающей персональные данные, на зарегистрированных в MDM устройствах Intune.</span><span class="sxs-lookup"><span data-stu-id="f5095-120">The ability to remote wipes corporate data from Intune Mobile Device Management (MDM) enrolled devices while leaving personal data unaffected.</span></span> 
- <span data-ttu-id="f5095-121">Отчеты аудита для отслеживания проблем и действий по устранению неполадок, таких как обучение пользователей соответствию требованиям.</span><span class="sxs-lookup"><span data-stu-id="f5095-121">Audit reports for tracking issues and for remedial actions such as compliance training for users.</span></span>
- <span data-ttu-id="f5095-122">Интеграция с существующей системой управления для настройки, развертывания и управления WIP.</span><span class="sxs-lookup"><span data-stu-id="f5095-122">Integration with your existing management system to configure, deploy, and manage WIP.</span></span> <span data-ttu-id="f5095-123">В качестве примера можно привести Microsoft Intune, Microsoft Endpoint Configuration Manager или текущую систему управления мобильными устройствами (MDM).</span><span class="sxs-lookup"><span data-stu-id="f5095-123">Some examples are Microsoft Intune, Microsoft Endpoint Configuration Manager, or your current mobile device management (MDM) system.</span></span>

## <span data-ttu-id="f5095-124">Политика WIP и режимы защиты</span><span class="sxs-lookup"><span data-stu-id="f5095-124">WIP policy and protection modes</span></span>

<span data-ttu-id="f5095-125">С помощью политик можно настроить четыре режима защиты, описанные в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="f5095-125">Using policies, you can configure the four protection modes described in the following table.</span></span> <span data-ttu-id="f5095-126">Дополнительные сведения см. в статье [Режимы защиты WIP](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#wip-protection-modes).</span><span class="sxs-lookup"><span data-stu-id="f5095-126">For more information, see [WIP-protection modes](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#wip-protection-modes).</span></span>

| <span data-ttu-id="f5095-127">Режим</span><span class="sxs-lookup"><span data-stu-id="f5095-127">Mode</span></span> | <span data-ttu-id="f5095-128">Описание</span><span class="sxs-lookup"><span data-stu-id="f5095-128">Description</span></span> |
|------|-------------|
| <span data-ttu-id="f5095-129">Блокирование</span><span class="sxs-lookup"><span data-stu-id="f5095-129">Block</span></span> | <span data-ttu-id="f5095-130">WIP обнаруживает случаи недопустимого предоставления доступа к данным и запрещает сотруднику выполнить действие.</span><span class="sxs-lookup"><span data-stu-id="f5095-130">WIP looks for inappropriate data sharing practices and stops the employee from completing the action.</span></span> <span data-ttu-id="f5095-131">К таким обнаруженным случаям может относиться предоставление общего доступа к корпоративным данным в приложениях, которые не защищены на корпоративном уровне (в дополнение к совместному использованию корпоративных данных в различных приложениях), а также попытки предоставить доступ к данным вне сети вашей организации.</span><span class="sxs-lookup"><span data-stu-id="f5095-131">This search can include sharing enterprise data to non-enterprise-protected apps in addition to sharing enterprise data between apps or attempting to share outside of your organization's network.</span></span> |
| <span data-ttu-id="f5095-132">Разрешить переопределения</span><span class="sxs-lookup"><span data-stu-id="f5095-132">Allow Overrides</span></span> | <span data-ttu-id="f5095-133">WIP обнаруживает случаи недопустимого предоставления доступа к данным и предупреждает сотрудника о том, что он собирается выполнить потенциально небезопасное действие.</span><span class="sxs-lookup"><span data-stu-id="f5095-133">WIP looks for inappropriate data sharing, warning employees if they do something deemed potentially unsafe.</span></span> <span data-ttu-id="f5095-134">Тем не менее в этом режиме управления сотрудник может переопределить политику и предоставить доступ к данным. При этом сведения о его действии будут внесены в журнал аудита.</span><span class="sxs-lookup"><span data-stu-id="f5095-134">However, this management mode lets the employee override the policy and share the data, logging the action to your audit log.</span></span> |
| <span data-ttu-id="f5095-135">Автоматически</span><span class="sxs-lookup"><span data-stu-id="f5095-135">Silent</span></span> | <span data-ttu-id="f5095-136">WIP работает в автоматическом режиме, занося в журнал сведения о недопустимом предоставлении доступа к данным, но не останавливает действия, предупреждения о которых пользователь увидел бы в режиме "Разрешить переопределения".</span><span class="sxs-lookup"><span data-stu-id="f5095-136">WIP runs silently, logging inappropriate data sharing, without stopping anything that would have been prompted for employee interaction while in Allow Overrides mode.</span></span> <span data-ttu-id="f5095-137">Неразрешенные действия, например несанкционированные попытки приложений получить доступ к сетевым ресурсам или данным, защищенным с помощью WIP, останавливаются.</span><span class="sxs-lookup"><span data-stu-id="f5095-137">Unallowed actions, like apps inappropriately trying to access a network resource or WIP-protected data, are still stopped.</span></span> |
| <span data-ttu-id="f5095-138">Отключено</span><span class="sxs-lookup"><span data-stu-id="f5095-138">Off</span></span> | <span data-ttu-id="f5095-139">Средство WIP отключено. Оно не защищает данные и не производит их аудит.</span><span class="sxs-lookup"><span data-stu-id="f5095-139">WIP is turned off and doesn't help to protect or audit your data.</span></span> <span data-ttu-id="f5095-140">После отключения WIP будет выполнена попытка расшифровать все файлы с тегами WIP на локально подключенных дисках.</span><span class="sxs-lookup"><span data-stu-id="f5095-140">After you turn off WIP, an attempt is made to decrypt any WIP-tagged files on the locally attached drives.</span></span> <span data-ttu-id="f5095-141">Необходимо отметить, что введенные ранее сведения о расшифровке и политике не применяются повторно автоматически, если снова включить защиту WIP.</span><span class="sxs-lookup"><span data-stu-id="f5095-141">Your previous decryption and policy info isn't automatically reapplied if you turn WIP protection back on.</span></span>
 |

## <span data-ttu-id="f5095-142">Возможности WIP, поддерживаемые в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f5095-142">WIP features supported in Microsoft Edge</span></span>

<span data-ttu-id="f5095-143">С Microsoft Edge версии 81 поддерживаются следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="f5095-143">Starting with Microsoft Edge version 81, the following features are supported:</span></span>

- <span data-ttu-id="f5095-144">Рабочие сайты определяются значком портфеля в адресной строке.</span><span class="sxs-lookup"><span data-stu-id="f5095-144">Work sites will be indicated by a briefcase icon on the address bar.</span></span>  
- <span data-ttu-id="f5095-145">Файлы, загруженные из рабочего расположения, шифруются автоматически.</span><span class="sxs-lookup"><span data-stu-id="f5095-145">Files downloaded from a work location are automatically encrypted.</span></span>
- <span data-ttu-id="f5095-146">Использование режимов "Автоматически", "Блокирование" и "Переопределение" для отправки рабочих файлов в нерабочие расположения.</span><span class="sxs-lookup"><span data-stu-id="f5095-146">Silent/Block/Override enforcement for work file uploads to non-work locations.</span></span>  
- <span data-ttu-id="f5095-147">Использование режимов "Автоматически", "Блокирование" и "Переопределение" для операций перетаскивания файлов.</span><span class="sxs-lookup"><span data-stu-id="f5095-147">Silent/Block/Override enforcement for file Drag & Drop actions.</span></span>
- <span data-ttu-id="f5095-148">Использование режимов "Автоматически", "Блокирование" и "Переопределение" для действий в буфере обмена.</span><span class="sxs-lookup"><span data-stu-id="f5095-148">Silent/Block/Override enforcement for Clipboard actions.</span></span>
- <span data-ttu-id="f5095-149">Автоматическое перенаправление на рабочий профиль (связанный с удостоверением Azure AD) при переходе к рабочим расположениям из нерабочих профилей.</span><span class="sxs-lookup"><span data-stu-id="f5095-149">Browsing to work locations from non-work profiles automatically redirects to the Work Profile (associated with the Azure AD Identity.)</span></span>
- <span data-ttu-id="f5095-150">В режиме IE поддерживаются все возможности WIP.</span><span class="sxs-lookup"><span data-stu-id="f5095-150">IE Mode supports full WIP functionality.</span></span>

## <span data-ttu-id="f5095-151">Работа с WIP в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f5095-151">Working with WIP in Microsoft Edge</span></span>

<span data-ttu-id="f5095-152">После включения поддержки WIP в Microsoft Edge пользователи будут видеть, когда осуществляется доступ к информации, связанной с работой.</span><span class="sxs-lookup"><span data-stu-id="f5095-152">After WIP support is enabled for Microsoft Edge, users will see when work-related information is accessed.</span></span> <span data-ttu-id="f5095-153">На следующем снимке экрана отображается значок портфеля в адресной строке, который указывает на то, что доступ к информации, связанной с работой, осуществляется через браузер.</span><span class="sxs-lookup"><span data-stu-id="f5095-153">The next screenshot shows the briefcase icon in the address bar, indicating that work-related information is accessed via the browser.</span></span>

 ![Индикатор адресной строки для сайтов, помеченных как "рабочие"](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-notify.png)

<span data-ttu-id="f5095-155">Microsoft Edge предоставляет пользователям возможность делиться защищенным содержимым на неутвержденном веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="f5095-155">Microsoft Edge gives users the ability to share protected content in an unapproved website.</span></span> <span data-ttu-id="f5095-156">На следующем снимке экрана показан запрос в Microsoft Edge, позволяющий пользователю использовать защищенное содержимое на неутвержденном веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="f5095-156">The next screenshot shows the Microsoft Edge prompt that allows a user to use protected content in an unapproved website.</span></span>

 ![Запрос на переопределение защищенного содержимого](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-override.png)

## <span data-ttu-id="f5095-158">Настройка политик для поддержки WIP</span><span class="sxs-lookup"><span data-stu-id="f5095-158">Configure policies to support WIP</span></span>

<span data-ttu-id="f5095-159">Для использования WIP в Microsoft Edge требуется рабочий профиль.</span><span class="sxs-lookup"><span data-stu-id="f5095-159">Using WIP with Microsoft Edge requires the presence of a work profile.</span></span>

### <span data-ttu-id="f5095-160">Убедитесь в наличии рабочего профиля</span><span class="sxs-lookup"><span data-stu-id="f5095-160">Ensure the presence of a work profile</span></span>

<span data-ttu-id="f5095-161">На компьютерах с гибридным присоединением вход в Microsoft Edge автоматически выполняется с помощью учетной записи Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="f5095-161">On hybrid joined machines, Microsoft Edge is automatically signed in with the Azure Active Directory (Azure AD) account.</span></span> <span data-ttu-id="f5095-162">Чтобы убедиться, что пользователи не смогут удалить профиль, необходимый для WIP, настройте следующую политику:</span><span class="sxs-lookup"><span data-stu-id="f5095-162">To make sure that users don't remove this profile, which is needed for WIP, configure the following policy:</span></span>

- [<span data-ttu-id="f5095-163">NonRemovableProfileEnabled</span><span class="sxs-lookup"><span data-stu-id="f5095-163">NonRemovableProfileEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#nonremovableprofileenabled)

> [!NOTE]
> <span data-ttu-id="f5095-164">Если в вашей среде отсутствует гибридное присоединение, вы можете реализовать его с помощью инструкций, приведенных в статье [Планирование реализации гибридного присоединения к Azure Active Directory](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-plan).</span><span class="sxs-lookup"><span data-stu-id="f5095-164">If your environment isn't hybrid joined, you can hybrid join using these instructions: [Plan your hybrid Azure Active Directory join implementation](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-plan).</span></span>

<span data-ttu-id="f5095-165">Если гибридное присоединение невозможно, можно использовать локальные учетные записи Active Directory, чтобы разрешить Microsoft Edge автоматически создавать специальный рабочий профиль с помощью учетных записей доменов пользователей.</span><span class="sxs-lookup"><span data-stu-id="f5095-165">If hybrid joining isn't an option, you can use on-prem Active Directory accounts to allow Microsoft Edge to auto create a special work profile with the users' domain accounts.</span></span> <span data-ttu-id="f5095-166">Обратите внимание, что локальным учетным записям могут присваиваться не все функции Azure AD, такие как облачная синхронизация, Office NTP и т. д.</span><span class="sxs-lookup"><span data-stu-id="f5095-166">Note that on-premises accounts may not receive all of Azure AD's features, such as cloud sync, Office NTP, and so on.)</span></span>

#### <span data-ttu-id="f5095-167">Учетные записи Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="f5095-167">Active Directory (AD) accounts</span></span>

<span data-ttu-id="f5095-168">Чтобы в Microsoft Edge автоматически создавался специальный рабочий профиль, необходимо настроить следующую политику для учетных записей AD:</span><span class="sxs-lookup"><span data-stu-id="f5095-168">For AD accounts, you must configure the following policy to have the Microsoft Edge auto create a special work profile.</span></span>

- [<span data-ttu-id="f5095-169">ConfigureOnPremisesAccountAutoSignIn</span><span class="sxs-lookup"><span data-stu-id="f5095-169">ConfigureOnPremisesAccountAutoSignIn</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin)

### <span data-ttu-id="f5095-170">Политики Windows для WIP</span><span class="sxs-lookup"><span data-stu-id="f5095-170">Windows policies for WIP</span></span>

<span data-ttu-id="f5095-171">WIP можно настроить с помощью политик Windows.</span><span class="sxs-lookup"><span data-stu-id="f5095-171">You can configure WIP using Windows policies.</span></span> <span data-ttu-id="f5095-172">Дополнительные сведения см. в статье [Создание и развертывание политик WIP с помощью Microsoft Intune](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/overview-create-wip-policy)</span><span class="sxs-lookup"><span data-stu-id="f5095-172">For more information, see [Create and deploy WIP policies using Microsoft Intune](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/overview-create-wip-policy)</span></span>

## <span data-ttu-id="f5095-173">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="f5095-173">Frequently Asked Questions</span></span>

### <span data-ttu-id="f5095-174">Как устранить ошибку с кодом 2147024540?</span><span class="sxs-lookup"><span data-stu-id="f5095-174">How do I resolve Error Code -2147024540?</span></span>

<span data-ttu-id="f5095-175">Этот код ошибки соответствует следующей ошибке Windows Information Protection: *ERROR_EDP_POLICY_DENIES_OPERATION: запрошенная операция была заблокирована политикой Windows Information Protection. Для получения дополнительных сведений обратитесь к системному администратору*.</span><span class="sxs-lookup"><span data-stu-id="f5095-175">This error code corresponds to the following Windows Information Protection error: *ERROR_EDP_POLICY_DENIES_OPERATION: The requested operation was blocked by Windows Information Protection policy. For more information, contact your system administrator.*</span></span>

<span data-ttu-id="f5095-176">Эта ошибка возникает в Microsoft Edge в том случае, если в организации включена система Windows Information Protection (WIP) с целью разрешить доступ к корпоративным ресурсам только пользователям с утвержденными приложениями.</span><span class="sxs-lookup"><span data-stu-id="f5095-176">Microsoft Edge shows this error when the organization has enabled Windows Information Protection (WIP) to only allow users with approved applications to access corporate resources.</span></span> <span data-ttu-id="f5095-177">В этом случае, поскольку Microsoft Edge нет в списке утвержденных приложений, администратору необходимо обновить политики WIP, чтобы предоставить доступ к Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f5095-177">In this case because Microsoft Edge isn't on the approved applications list, the admin will have to update the WIP policies to grant access to Microsoft Edge.</span></span>

<span data-ttu-id="f5095-178">На приведенном ниже снимке экрана отображено, как использовать Microsoft Intune, чтобы добавить Microsoft Edge в качестве разрешенного приложения для WIP.</span><span class="sxs-lookup"><span data-stu-id="f5095-178">The following screenshot shows how the Microsoft Intune is used to add Microsoft Edge as an allowed app for WIP.</span></span>

 ![Диалоговое окно Intune при добавлении Microsoft Edge в качестве приложения для WIP.](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-exemption.png)

<span data-ttu-id="f5095-180">Если вы не используете Microsoft Intune, скачайте и примените обновление политики в файле [WIP Enterprise AppLocker Policy](https://download.microsoft.com/download/8/9/9/8995d820-065c-4ab1-aa2a-9d6dc0cd7ffa/MsEdge%20-%20WIP%20Enterprise%20AppLocker%20Policy%20Files.zip).</span><span class="sxs-lookup"><span data-stu-id="f5095-180">If you're not using Microsoft Intune, download and apply the policy update in the [WIP Enterprise AppLocker Policy](https://download.microsoft.com/download/8/9/9/8995d820-065c-4ab1-aa2a-9d6dc0cd7ffa/MsEdge%20-%20WIP%20Enterprise%20AppLocker%20Policy%20Files.zip) file.</span></span>

## <span data-ttu-id="f5095-181">См. также</span><span class="sxs-lookup"><span data-stu-id="f5095-181">See also</span></span>

- [<span data-ttu-id="f5095-182">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="f5095-182">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise) 
- [<span data-ttu-id="f5095-183">Защита корпоративных данных с помощью Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="f5095-183">Protect enterprise data using Windows Information Protection</span></span>](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)
