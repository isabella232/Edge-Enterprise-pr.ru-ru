---
title: Набор средств блокировки Blocker Toolkit для отключения автоматической доставки Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 12/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Набор средств блокировки Blocker Toolkit для отключения автоматической доставки Microsoft Edge
ms.openlocfilehash: 9fb97d2dfec4822f8ce76dc3e37b85118c6572ad
ms.sourcegitcommit: 606282995b466a968bab40c16005a6653323c763
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/16/2020
ms.locfileid: "11229620"
---
# <span data-ttu-id="62240-103">Набор средств блокировки Blocker Toolkit для отключения автоматической доставки Microsoft Edge (на основе Chromium)</span><span class="sxs-lookup"><span data-stu-id="62240-103">Blocker Toolkit to disable automatic delivery of Microsoft Edge (Chromium-based)</span></span>

<span data-ttu-id="62240-104">В этой статье приведены инструкции по использованию набора средств блокировки для отключения автоматической доставки и установки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="62240-104">This article describes the Blocker Toolkit for disabling automatic delivery and installation of Microsoft Edge.</span></span>

<span data-ttu-id="62240-105">В эту статью добавлены сведения о следующих обновлениях:</span><span class="sxs-lookup"><span data-stu-id="62240-105">The following updates have been made to this article:</span></span>

- <span data-ttu-id="62240-106">**09.01.2020** — добавлены сведения об устройствах для которых может потребоваться использовать Blocker Toolkit.</span><span class="sxs-lookup"><span data-stu-id="62240-106">**01/09/2020** with more information about devices that might require you to use the Blocker Toolkit</span></span>
- <span data-ttu-id="62240-107">**28.02.2020** — удаление критерия "находится под управлением MDM" из списка критериев устройств, исключенных из этого автоматического обновления.</span><span class="sxs-lookup"><span data-stu-id="62240-107">**2/28/2020** to remove "MDM managed" from the criteria of devices to be excluded from this automatic update</span></span>
- <span data-ttu-id="62240-108">**30.06.2020** — разъяснение, что все устройства, подключенные к Центру обновления Windows, входят в область устройств, получающих это обновление (действует не ранее 30.07.2020).</span><span class="sxs-lookup"><span data-stu-id="62240-108">**6/30/2020** to reflect that all Windows Update connected devices are in scope to receive this update (effective no sooner than 7/30/2020)</span></span>
- <span data-ttu-id="62240-109">**10.12.2020** — разъяснение ситуаций с версиями до 20H2, в которых параметры Blocker Toolkit будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="62240-109">**12/10/2020** to explain pre 20H2 situations in which the Blocker Toolkit settings will be ignored</span></span>

> [!NOTE]
> <span data-ttu-id="62240-110">Эта статья относится к каналу Microsoft Edge Stable.</span><span class="sxs-lookup"><span data-stu-id="62240-110">This applies to Microsoft Edge Stable channel.</span></span>

## <span data-ttu-id="62240-111">Обзор</span><span class="sxs-lookup"><span data-stu-id="62240-111">Overview</span></span>

<span data-ttu-id="62240-112">Чтобы помочь нашим клиентам обеспечить безопасность и актуальное состояние устройств, корпорация Майкрософт будет распространять Microsoft Edge (на основе Chromium) для всех устройств, подключенных к Центру обновления Windows и использующих Windows 10 версии 1803 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="62240-112">To help our customers become more secure and up-to-date, Microsoft will distribute Microsoft Edge (Chromium-based) to all Windows Update-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="62240-113">Этот процесс начнется после 15 января 2020г. с предоставлением дополнительных сведений в эту дату.</span><span class="sxs-lookup"><span data-stu-id="62240-113">This process will start after January 15, 2020 and more information will be available on that date.</span></span>

<span data-ttu-id="62240-114">Набор средств блокировки Blocker Toolkit предназначен для организаций, которым необходимо заблокировать автоматическую доставку Microsoft Edge (на основе Chromium) для устройств, подключенных к Центру обновления Windows и использующих Windows 10 версии 1803 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="62240-114">The Blocker Toolkit is intended for organizations that would like to block automatic delivery of Microsoft Edge (Chromium-based) to Windows Updated-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="62240-115">Устройства, находящиеся под управлением служб Windows Server Update Services (WSUS) или Центра обновления Windows для бизнеса (WUfB), будут исключены из этого автоматического обновления Центра обновления Windows, но могут получить новую версию Microsoft Edge (на базе Chromium) через организацию, в которой находятся эти устройства.</span><span class="sxs-lookup"><span data-stu-id="62240-115">Devices that are Windows Server Update Services (WSUS) or Windows Update for Business (WUfB) managed will be excluded from this automatic Windows Update, but may receive the new Microsoft Edge (Chromium-based) through their organization.</span></span>

**<span data-ttu-id="62240-116">Важно отметить следующее:</span><span class="sxs-lookup"><span data-stu-id="62240-116">It's important to note that:</span></span>**

- <span data-ttu-id="62240-117">Набор средств блокировки Blocker Toolkit не запрещает пользователям вручную устанавливать Microsoft Edge (на основе Chromium) при скачивании браузера в Интернете или с внешнего носителя.</span><span class="sxs-lookup"><span data-stu-id="62240-117">The Blocker Toolkit will not prevent users from manually installing Microsoft Edge (Chromium-based) from Internet download, or from external media.</span></span>
- <span data-ttu-id="62240-118">Организации, обновления которых управляются с помощью Центра обновления Windows для бизнеса (WUfB), не будут получать это обновление автоматически, и им не требуется развертывать набор средств блокировки Blocker Toolkit.</span><span class="sxs-lookup"><span data-stu-id="62240-118">Organizations with updates managed through Windows Update for Business (WUfB) will not automatically receive this update and do not need to deploy the blocker toolkit.</span></span>
- <span data-ttu-id="62240-119">Организациям со средами, управляемыми с помощью решения для управления обновлениями, такого как службы Windows Server Update Services (WSUS) или System Center Configuration Manager (SCCM), не требуется развертывать набор средств блокировки Blocker Toolkit.</span><span class="sxs-lookup"><span data-stu-id="62240-119">Organizations with environments managed with an update management solution such as Windows Server Update Services (WSUS) or System Center Configuration Manager (SCCM) do not have to deploy the Blocker Toolkit.</span></span> <span data-ttu-id="62240-120">Они могут использовать эти продукты, чтобы полностью управлять развертыванием обновлений, выпущенных через Центр обновления Windows и Центр обновления Майкрософт, включая [обновление в WSUS для новой версии Microsoft Edge](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge), в своей среде.</span><span class="sxs-lookup"><span data-stu-id="62240-120">They can use those products to fully manage deployment of updates released through Windows Update and Microsoft Update, including the [Update in WSUS for the new Microsoft Edge](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge), within their environment.</span></span>
- <span data-ttu-id="62240-121">Это автономное обновление (не входит в ежемесячное накопительное обновление), которое предоставляет корпоративным клиентам гибкость и максимальный контроль над развертыванием.</span><span class="sxs-lookup"><span data-stu-id="62240-121">This update is a stand-alone update (not part of the monthly cumulative update) to give Enterprise customers flexibility and maximum control over deploying this update.</span></span>
- <span data-ttu-id="62240-122">Новая версия Microsoft Edge (на базе Chromium) входит в состав обновления компонентов Windows 10 версии 20H2 во второй половине 2020 г.</span><span class="sxs-lookup"><span data-stu-id="62240-122">The new Microsoft Edge (Chromium-based) is included as part of the Windows 10, version 20H2 feature update in the second half of 2020.</span></span> <span data-ttu-id="62240-123">Набор средств Blocker не влияет на поведение и развертывание версии 20H2.</span><span class="sxs-lookup"><span data-stu-id="62240-123">The Blocker toolkit does not impact 20H2 behaviors or deployment.</span></span> <span data-ttu-id="62240-124">Дополнительные сведения о Windows 10 версии 20H2 см. [здесь](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span><span class="sxs-lookup"><span data-stu-id="62240-124">See more information about Windows 10, version 20H2 [here](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span></span>

<span data-ttu-id="62240-125">Вы можете скачать исполняемый файл набора средств блокировки Blocker Toolkit здесь: [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span><span class="sxs-lookup"><span data-stu-id="62240-125">You can download the Blocker Toolkit executable file from [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span></span>

### <span data-ttu-id="62240-126">Компоненты набора средств</span><span class="sxs-lookup"><span data-stu-id="62240-126">Toolkit components</span></span>

<span data-ttu-id="62240-127">В этом наборе средств содержатся следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="62240-127">This toolkit contains the following components:</span></span>

- <span data-ttu-id="62240-128">Исполняемый сценарий блокировщика (.CMD)</span><span class="sxs-lookup"><span data-stu-id="62240-128">Executable blocker script (.CMD)</span></span>
- <span data-ttu-id="62240-129">Административный шаблон групповой политики (.ADMX и .ADML)</span><span class="sxs-lookup"><span data-stu-id="62240-129">Group Policy Administrative Template (.ADMX and .ADML)</span></span>

### <span data-ttu-id="62240-130">Поддерживаемые операционные системы</span><span class="sxs-lookup"><span data-stu-id="62240-130">Supported Operating Systems</span></span>

<span data-ttu-id="62240-131">Windows10 версии1803 и выше.</span><span class="sxs-lookup"><span data-stu-id="62240-131">Windows 10 version 1803 and newer.</span></span>

## <span data-ttu-id="62240-132">Сценарий блокировщика</span><span class="sxs-lookup"><span data-stu-id="62240-132">Blocker script</span></span>

<span data-ttu-id="62240-133">Сценарий создает раздел реестра и настраивает связанное значение на блокировку или разблокировку (в зависимости от используемого параметра командной строки) автоматической доставки Microsoft Edge (на основе Chromium) на локальном компьютере или на удаленном целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="62240-133">The script creates a registry key and sets the associated value to block or unblock (depending on the command-line option used) automatic delivery of Microsoft Edge (Chromium-based) on either the local machine or a remote target machine.</span></span>

**<span data-ttu-id="62240-134">Раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="62240-134">Registry key:</span></span>** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**<span data-ttu-id="62240-135">Имя значения реестра:</span><span class="sxs-lookup"><span data-stu-id="62240-135">Key value name:</span></span>** `DoNotUpdateToEdgeWithChromium`

| <span data-ttu-id="62240-136">Значение</span><span class="sxs-lookup"><span data-stu-id="62240-136">Value</span></span>                | <span data-ttu-id="62240-137">Результат</span><span class="sxs-lookup"><span data-stu-id="62240-137">Result</span></span>                         |
|----------------------|--------------------------------|
| *<span data-ttu-id="62240-138">Раздел не определен</span><span class="sxs-lookup"><span data-stu-id="62240-138">Key is not defined</span></span>* | <span data-ttu-id="62240-139">Распространение *не* блокируется.</span><span class="sxs-lookup"><span data-stu-id="62240-139">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="62240-140">0</span><span class="sxs-lookup"><span data-stu-id="62240-140">0</span></span>                    | <span data-ttu-id="62240-141">Распространение *не* блокируется.</span><span class="sxs-lookup"><span data-stu-id="62240-141">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="62240-142">1</span><span class="sxs-lookup"><span data-stu-id="62240-142">1</span></span>                    | <span data-ttu-id="62240-143">Распространение блокируется.</span><span class="sxs-lookup"><span data-stu-id="62240-143">Distribution is blocked.</span></span>       |

<span data-ttu-id="62240-144">Сценарий имеет следующий синтаксис командной строки:</span><span class="sxs-lookup"><span data-stu-id="62240-144">The script has the following command-line syntax:</span></span><br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### <span data-ttu-id="62240-145">Имя компьютера</span><span class="sxs-lookup"><span data-stu-id="62240-145">Machine name</span></span>

<span data-ttu-id="62240-146">Параметр `<machine name>` является необязательным.</span><span class="sxs-lookup"><span data-stu-id="62240-146">The `<machine name>` parameter is optional.</span></span> <span data-ttu-id="62240-147">Если этот параметр не указан, действие выполняется на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="62240-147">If not specified, the action is performed on the local machine.</span></span> <span data-ttu-id="62240-148">В противном случае доступ к удаленному компьютеру осуществляется с помощью возможностей удаленного реестра команды `REG`.</span><span class="sxs-lookup"><span data-stu-id="62240-148">Otherwise, the remote machine is accessed through the remote registry capabilities of the `REG` command.</span></span> <span data-ttu-id="62240-149">Если не удается получить доступ к удаленному реестру из-за разрешений безопасности или не удается найти удаленный компьютер, команда `REG` возвращает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="62240-149">If the remote registry can't be accessed due to security permissions or the remote machine can't be found, an error message is returned from the `REG` command.</span></span>

### <span data-ttu-id="62240-150">Переключатели</span><span class="sxs-lookup"><span data-stu-id="62240-150">Switches</span></span>

<span data-ttu-id="62240-151">Переключатели, используемые сценарием, являются взаимоисключающими и действие применяется только к первому допустимому переключателю из конкретной команды.</span><span class="sxs-lookup"><span data-stu-id="62240-151">Switches used by the script are mutually exclusive and only the first valid switch from a given command is acted on.</span></span> <span data-ttu-id="62240-152">Сценарий может выполняться несколько раз на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="62240-152">The script can be run multiple times on the same machine.</span></span>

| <span data-ttu-id="62240-153">Переключатель</span><span class="sxs-lookup"><span data-stu-id="62240-153">Switch</span></span>       | <span data-ttu-id="62240-154">Описание</span><span class="sxs-lookup"><span data-stu-id="62240-154">Description</span></span>                              |
|--------------|------------------------------------------|
| `/B`         | <span data-ttu-id="62240-155">Блокирует распространение</span><span class="sxs-lookup"><span data-stu-id="62240-155">Blocks distribution</span></span>                      |
| `/U`         | <span data-ttu-id="62240-156">Разблокирует распространение</span><span class="sxs-lookup"><span data-stu-id="62240-156">Unblocks distribution</span></span>                    |
| `/H` <span data-ttu-id="62240-157">или</span><span class="sxs-lookup"><span data-stu-id="62240-157">or</span></span> `/?` | <span data-ttu-id="62240-158">Отображает следующую сводную справку.</span><span class="sxs-lookup"><span data-stu-id="62240-158">Displays the following summary help:</span></span><br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## <span data-ttu-id="62240-159">Административный шаблон групповой политики (файлы .ADMX и .ADML)</span><span class="sxs-lookup"><span data-stu-id="62240-159">Group Policy Administrative Template (.ADMX and .ADML files)</span></span>

<span data-ttu-id="62240-160">Административный шаблон групповой политики (файлы .ADMX и .ADML) позволяют администраторам импортировать новые параметры групповой политики, чтобы блокировать или разблокировать автоматическую доставку Microsoft Edge (на основе Chromium) в свою среду групповых политик, а также использовать групповую политику для централизованного выполнения действия на разных системах в их среде.</span><span class="sxs-lookup"><span data-stu-id="62240-160">The Group Policy Administrative Template (.ADMX  and .ADML files) allows administrators to import the new Group Policy settings to block or unblock automatic delivery of Microsoft Edge (Chromium-based) into their Group Policy environment, and use Group Policy to centrally execute the action across systems in their environment.</span></span>

<span data-ttu-id="62240-161">Пользователи, использующие Windows 10 RS3 Enterprise/EDU, RS4 и более новых версий, будут видеть по следующему пути:</span><span class="sxs-lookup"><span data-stu-id="62240-161">Users running Windows 10 RS3 Enterprise/EDU and RS4 and newer, will see the policy under the following path:</span></span>

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

<span data-ttu-id="62240-162">Этот параметр доступен только в качестве параметра для компьютера. Параметры для пользователей отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="62240-162">This setting is available only as a Computer setting; there is no Per-User setting.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62240-163">Этот параметр реестра не хранится в разделе политик и считается *предпочтением.*</span><span class="sxs-lookup"><span data-stu-id="62240-163">This registry setting isn't stored in a policies key and is considered a *preference*.</span></span> <span data-ttu-id="62240-164">Таким образом, если объект групповой политики, реализующий параметр, удаляется или политике задается значение **Не настроено**, параметр остается.</span><span class="sxs-lookup"><span data-stu-id="62240-164">Therefore, if the Group Policy Object that implements the setting is ever removed or the policy is set to **Not Configured**, the setting will remain.</span></span> <span data-ttu-id="62240-165">Чтобы разблокировать распространение Microsoft Edge (на основе Chromium) с помощью групповой политики, установите для политики значение **Отключено**.</span><span class="sxs-lookup"><span data-stu-id="62240-165">To unblock distribution of Microsoft Edge (Chromium-based) by using Group Policy, set the policy to **Disabled**.</span></span>

## <span data-ttu-id="62240-166">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="62240-166">See also</span></span>

- [<span data-ttu-id="62240-167">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="62240-167">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="62240-168">Обновления Windows для поддержки Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="62240-168">Windows updates to support Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [<span data-ttu-id="62240-169">Как получить доступ к старой версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="62240-169">How to access the old version of Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
