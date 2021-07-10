---
title: Использование Microsoft Edge для защиты от потенциально нежелательных приложений
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Использование Microsoft Edge для защиты от потенциально нежелательных приложений
ms.openlocfilehash: 68cd87e85408933212c4b25baa01a9ff8d994089
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643105"
---
# <a name="protect-against-potentially-unwanted-applications-puas"></a><span data-ttu-id="96f22-103">Защита от потенциально нежелательных приложений (ПНП)</span><span class="sxs-lookup"><span data-stu-id="96f22-103">Protect against potentially unwanted applications (PUAs)</span></span>

<span data-ttu-id="96f22-104">В этой статье объясняется, как защититься от потенциально нежелательных приложений (ПНП) с помощью Microsoft Edge или с помощью антивирусной программы в Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="96f22-104">This article explains how you can protect against potentially unwanted applications (PUAs) using Microsoft Edge or by using Windows Defender Antivirus.</span></span>

> [!NOTE]
> <span data-ttu-id="96f22-105">Эта статья относится к Microsoft Edge версии 80 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="96f22-105">This article applies to Microsoft Edge version 80 or later.</span></span>

## <a name="overview"></a><span data-ttu-id="96f22-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="96f22-106">Overview</span></span>

<span data-ttu-id="96f22-107">Потенциально нежелательные приложения не считаются вирусами или вредоносными программами, но могут выполнять действия, которые негативно влияют на использование и производительность конечных точек.</span><span class="sxs-lookup"><span data-stu-id="96f22-107">Potentially unwanted applications aren't considered to be viruses or malware, but these apps might perform actions on endpoints that adversely affect endpoint performance or use.</span></span> <span data-ttu-id="96f22-108">Например, *программное обеспечение Evasion* пытается скрыться от обнаружения в продуктах обеспечения безопасности.</span><span class="sxs-lookup"><span data-stu-id="96f22-108">For example, *Evasion software* actively tries to evade detection by security products.</span></span> <span data-ttu-id="96f22-109">Такое программное обеспечение повышает риск заражения вашей сети реальными вредоносными программами.</span><span class="sxs-lookup"><span data-stu-id="96f22-109">This kind of software can increase the risk of your network being infected with actual malware.</span></span> <span data-ttu-id="96f22-110">К потенциально нежелательным приложениям также относятся приложения с плохой репутацией.</span><span class="sxs-lookup"><span data-stu-id="96f22-110">PUA can also refer to applications that are considered to have poor reputation.</span></span>

<span data-ttu-id="96f22-111">Описание условий, применяемых для классификации программного обеспечения в качестве ПНП, см. в статье [Потенциально нежелательные приложения](/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua).</span><span class="sxs-lookup"><span data-stu-id="96f22-111">For a description of the criteria used to classify software as a PUA, see [Potentially unwanted application](/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua).</span></span>

## <a name="protect-against-pua-with-microsoft-edge"></a><span data-ttu-id="96f22-112">Защита от ПНП с Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="96f22-112">Protect against PUA with Microsoft Edge</span></span>

<span data-ttu-id="96f22-113">В Microsoft Edge (версии 80.0.361.50 или более поздней) загрузки ПНП и связанные с ними URL-адреса ресурсов блокируются.</span><span class="sxs-lookup"><span data-stu-id="96f22-113">Microsoft Edge (version 80.0.361.50 or later) blocks PUA downloads and associated resource URLs.</span></span>

<span data-ttu-id="96f22-114">Вы можете настроить защиту, включив функцию **Блокировка потенциально опасных приложений** в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="96f22-114">You can set up protection by enabling the **Block potentially unwanted apps** feature in Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="96f22-115">В [своем блоге группа Microsoft Edge](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/) описывает эту функцию, и объясняет, как обрабатывать приложения с ошибками и сообщать о нежелательной программе.</span><span class="sxs-lookup"><span data-stu-id="96f22-115">The [Microsoft Edge Team blog post](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/) describes this new feature and explains how to handle a mislabeled app or report an app as unwanted.</span></span>

### <a name="to-enable-pua-protection"></a><span data-ttu-id="96f22-116">Включение защиты от ПНП:</span><span class="sxs-lookup"><span data-stu-id="96f22-116">To enable PUA protection:</span></span>

1. <span data-ttu-id="96f22-117">Откройте **Параметры** в браузере.</span><span class="sxs-lookup"><span data-stu-id="96f22-117">Open **Settings** in the browser.</span></span>
2. <span data-ttu-id="96f22-118">Выберите **Конфиденциальность и службы**.</span><span class="sxs-lookup"><span data-stu-id="96f22-118">Select **Privacy and services**.</span></span>
3. <span data-ttu-id="96f22-119">Убедитесь, что в разделе **Службы** включен **фильтр SmartScreen в Microsoft Defender**.</span><span class="sxs-lookup"><span data-stu-id="96f22-119">In the **Services** section, check to see that **Microsoft Defender SmartScreen** is turned on.</span></span> <span data-ttu-id="96f22-120">Включите фильтр SmartScreen в Microsoft Defender, если это не так.</span><span class="sxs-lookup"><span data-stu-id="96f22-120">If not, then turn on Microsoft Defender SmartScreen.</span></span> <span data-ttu-id="96f22-121">На снимке экрана ниже показано, что браузер управляется организацией, а фильтр SmartScreen в Microsoft Defender включен.</span><span class="sxs-lookup"><span data-stu-id="96f22-121">The example in the following screenshot shows the browser is managed by the organization and that Microsoft Defender SmartScreen is turned on.</span></span>

   ![Включение ПНП Microsoft Edge в параметрах](./media/microsoft-edge-potentially-unwanted-apps/security-pua-setup.png)

4. <span data-ttu-id="96f22-123">В разделе **Службы** используйте переключатель, показанный на предыдущем снимке экрана, чтобы включить **Блокировку потенциально опасных приложений**.</span><span class="sxs-lookup"><span data-stu-id="96f22-123">In the **Services** section, use the toggle shown in the preceding screenshot to turn on **Block potentially unwanted apps**.</span></span>

   > [!TIP]
   > <span data-ttu-id="96f22-124">Функцию блокировки URL-адресов защиты от ПНП можно использовать, проверив ее на одной из [демонстрационных страниц](https://demo.smartscreen.msft.net/) SmartScreen в Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="96f22-124">You can safely explore the URL-blocking feature of PUA protection by testing it out on one of our Windows Defender SmartScreen [demo pages](https://demo.smartscreen.msft.net/).</span></span>

<span data-ttu-id="96f22-125">Когда Microsoft Edge обнаружит ПНП, появится сообщение со снимка экрана ниже.</span><span class="sxs-lookup"><span data-stu-id="96f22-125">When Microsoft Edge detects a PUA, you will see a message like the one in the next screenshot.</span></span>

   ![Предупреждающее сообщение ПНП Microsoft Edge](./media/microsoft-edge-potentially-unwanted-apps/security-pua-msg.png)

### <a name="to-block-against-pua-associated-urls"></a><span data-ttu-id="96f22-127">Блокировка URL-адресов, связанных с ПНП</span><span class="sxs-lookup"><span data-stu-id="96f22-127">To block against PUA-associated URLs</span></span>

<span data-ttu-id="96f22-128">После включения ПНП защиты в Microsoft Edge, SmartScreen в Microsoft Defender защитит вас от связанных с ПНП URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="96f22-128">After you turn on PUA protection in Microsoft Edge, Windows Defender SmartScreen will protect you from PUA-associated URLs.</span></span>

<span data-ttu-id="96f22-129">Администраторы могут настроить способы совместной работы Microsoft Edge и SmartScreen защитника Windows несколькими способами, чтобы защитить пользователей от связанных с ПНП URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="96f22-129">There are several ways admins can configure how Microsoft Edge and Windows Defender SmartScreen work together to protect users from PUA-associated URLs.</span></span> <span data-ttu-id="96f22-130">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="96f22-130">For more information, see:</span></span>

- [<span data-ttu-id="96f22-131">Настройка параметров политик Microsoft Edge в Windows</span><span class="sxs-lookup"><span data-stu-id="96f22-131">Configure Microsoft Edge policy settings on Windows</span></span>](./configure-microsoft-edge.md)
- [<span data-ttu-id="96f22-132">Параметры SmartScreen</span><span class="sxs-lookup"><span data-stu-id="96f22-132">SmartScreen settings</span></span>](./microsoft-edge-policies.md#smartscreen-settings)
- [<span data-ttu-id="96f22-133">Политика SmartScreenPuaEnabled</span><span class="sxs-lookup"><span data-stu-id="96f22-133">SmartScreenPuaEnabled policy</span></span>](./microsoft-edge-policies.md#smartscreenpuaenabled)
- [<span data-ttu-id="96f22-134">Настройка фильтра SmartScreen Защитника Windows</span><span class="sxs-lookup"><span data-stu-id="96f22-134">Configure Windows Defender SmartScreen</span></span>](/microsoft-edge/deploy/available-policies?source=docs#configure-windows-defender-smartscreen)

<span data-ttu-id="96f22-135">Администраторы могут настраивать список блокировок Advanced Threat Protection в Microsoft Defender (ATP в Microsoft Defender).</span><span class="sxs-lookup"><span data-stu-id="96f22-135">Admins can also customize the Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP) block list.</span></span> <span data-ttu-id="96f22-136">С помощью портала ATP в Microsoft Defender можно [создавать индикаторы для IP и URL-адресов, а также управлять ими](/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview).</span><span class="sxs-lookup"><span data-stu-id="96f22-136">They can use the Microsoft Defender ATP portal to [create and manage indicators for IPs and URLs](/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview).</span></span>

## <a name="protect-against-pua-with-windows-defender-antivirus"></a><span data-ttu-id="96f22-137">Защита от ПНП с помощью антивирусной программы в Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="96f22-137">Protect against PUA with Windows Defender Antivirus</span></span>

<span data-ttu-id="96f22-138">Статья [Обнаружение и блокировка потенциально нежелательных приложений](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus) содержит сведения о том, как настроить антивирусную программу "Защитник Windows" для включения защиты от ПНП.</span><span class="sxs-lookup"><span data-stu-id="96f22-138">The [Detect and block potentially unwanted applications](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus) article also describes how you can configure Windows Defender Antivirus to enable PUA protection.</span></span> <span data-ttu-id="96f22-139">Настроить защиту можно с помощью следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="96f22-139">You can configure protection using any of the following options:</span></span>

- [<span data-ttu-id="96f22-140">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="96f22-140">Microsoft Intune</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-intune-to-configure-pua-protection)
- [<span data-ttu-id="96f22-141">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="96f22-141">Microsoft Endpoint Configuration Manager</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-configuration-manager-to-configure-pua-protection)
- [<span data-ttu-id="96f22-142">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="96f22-142">Group Policy</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-group-policy-to-configure-pua-protection)
- [<span data-ttu-id="96f22-143">Командлеты PowerShell</span><span class="sxs-lookup"><span data-stu-id="96f22-143">PowerShell cmdlets</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection)

<span data-ttu-id="96f22-144">Когда защитник Windows обнаруживает файл ПНП на конечной точке, он помещает его в карантин и уведомляет пользователя ([если уведомления не отключены](/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus)), как при обычном обнаружение угроз (с приставкой "ПНП:"). Обнаруженные угрозы также появляются в [списке карантина в приложении "Безопасность Windows"](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history).</span><span class="sxs-lookup"><span data-stu-id="96f22-144">When Windows Defender detects a PUA file on an endpoint it quarantines the file and notifies the user ([unless notifications are disabled](/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus)) in the same format as a normal threat detection (prefaced with "PUA:".) Detected threats also appear in the [quarantine list in the Windows Security app](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history).</span></span>

### <a name="pua-notifications-and-events"></a><span data-ttu-id="96f22-145">Уведомления и события ПНП</span><span class="sxs-lookup"><span data-stu-id="96f22-145">PUA notifications and events</span></span>

<span data-ttu-id="96f22-146">Администратор может просматривать события ПНП несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="96f22-146">There are several ways an admin can see PUA events:</span></span>

- <span data-ttu-id="96f22-147">В средстве просмотра событий Windows, но не в Microsoft Endpoint Configuration Manager или Intune.</span><span class="sxs-lookup"><span data-stu-id="96f22-147">In the Windows Event Viewer, but not in Microsoft Endpoint Configuration Manager or Intune.</span></span>
- <span data-ttu-id="96f22-148">В сообщении электронной почты, если включены уведомления об обнаружении ПНП.</span><span class="sxs-lookup"><span data-stu-id="96f22-148">In an email if email notifications for PUA detections is turned on.</span></span>
- <span data-ttu-id="96f22-149">В журнале событий [антивирусной программы в Microsoft Defender](/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus), где события ПНП записываются с идентификатором событий 1116, с сообщением: "Платформа защиты от вредоносных программ обнаружила вредоносную или другую потенциально нежелательную программу."</span><span class="sxs-lookup"><span data-stu-id="96f22-149">In [Windows Defender Antivirus](/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus) event logs, where a PUA event is recorded under event ID 1116 with the message: "The antimalware platform detected malware or other potentially unwanted software."</span></span>

> [!NOTE]
> <span data-ttu-id="96f22-150">Пользователи увидят, что приложение "\*.exe заблокировано фильтром SmartScreen в Microsoft Defender, как нежелательное.</span><span class="sxs-lookup"><span data-stu-id="96f22-150">Users will see "\*.exe has been blocked as a potentially unwanted app by Microsoft Defender SmartScreen".</span></span>

### <a name="allow-list-an-app"></a><span data-ttu-id="96f22-151">Список разрешенных приложений</span><span class="sxs-lookup"><span data-stu-id="96f22-151">Allow-list an app</span></span>

<span data-ttu-id="96f22-152">Как и в Microsoft Edge, антивирусная программа "Защитник Windows" обеспечивает возможность разрешения ошибочно заблокированных или необходимых для выполнения задачи файлов.</span><span class="sxs-lookup"><span data-stu-id="96f22-152">Like Microsoft Edge, Windows Defender Antivirus provides a way to allow files that are blocked by mistake or needed to complete a task.</span></span> <span data-ttu-id="96f22-153">В этом случае можно внести приложение в список разрешенных.</span><span class="sxs-lookup"><span data-stu-id="96f22-153">If this happens you can allow-list a file.</span></span> <span data-ttu-id="96f22-154">Чтобы узнать, как исключить определенные файлы или папки, см. статью [Настройка Endpoint Protection в Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders).</span><span class="sxs-lookup"><span data-stu-id="96f22-154">For more information, see [How to Configure Endpoint Protection in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders) to learn how to exclude specific files or folders.</span></span>

## <a name="see-also"></a><span data-ttu-id="96f22-155">См. также</span><span class="sxs-lookup"><span data-stu-id="96f22-155">See also</span></span>

- [<span data-ttu-id="96f22-156">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="96f22-156">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="96f22-157">Защита от угроз</span><span class="sxs-lookup"><span data-stu-id="96f22-157">Threat protection</span></span>](/windows/security/threat-protection/index)
- [<span data-ttu-id="96f22-158">Настройка поведенческой и эвристической защиты, а также защиты в режиме реального времени</span><span class="sxs-lookup"><span data-stu-id="96f22-158">Configure behavioral, heuristic, and real-time protection</span></span>](/windows/security/threat-protection/windows-defender-antivirus/configure-protection-features-windows-defender-antivirus)
- [<span data-ttu-id="96f22-159">Защита нового поколения</span><span class="sxs-lookup"><span data-stu-id="96f22-159">Next-generation protection</span></span>](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-antivirus-in-windows-10)
- [<span data-ttu-id="96f22-160">Базовый план безопасности для Microsoft Edge на основе Chromium (версия 79).</span><span class="sxs-lookup"><span data-stu-id="96f22-160">Security baseline for Chromium-based Microsoft Edge, version 79</span></span>](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/security-baseline-final-for-chromium-based-microsoft-edge/ba-p/1111863)