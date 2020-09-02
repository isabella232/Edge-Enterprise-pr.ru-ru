---
title: Набор средств блокировки Blocker Toolkit для отключения автоматической доставки Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Набор средств блокировки Blocker Toolkit для отключения автоматической доставки Microsoft Edge
ms.openlocfilehash: 7563d2c94cf91a8434328699e46c75dbcfb77561
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980975"
---
# <span data-ttu-id="e3877-103">Набор средств блокировки Blocker Toolkit для отключения автоматической доставки Microsoft Edge (на основе Chromium)</span><span class="sxs-lookup"><span data-stu-id="e3877-103">Blocker Toolkit to disable automatic delivery of Microsoft Edge (Chromium-based)</span></span>

<span data-ttu-id="e3877-104">В этой статье приведены инструкции по использованию набора средств блокировки для отключения автоматической доставки и установки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e3877-104">This article describes the Blocker Toolkit for disabling automatic delivery and installation of Microsoft Edge.</span></span> <span data-ttu-id="e3877-105">Эта статья была обновлена **09.01.2020** с добавлением сведений об устройствах, для которых может потребоваться использовать набор средств блокировки Blocker Toolkit, **28.02.2020** с удалением фразы об управлении с помощью MDM из условий для устройств, исключаемых из автоматического обновления, и **30.06.2020** для указания того, что все устройства, подключенные к Центру обновления Windows, получают это обновление (вступает в силу не ранее 30.07.2020).</span><span class="sxs-lookup"><span data-stu-id="e3877-105">This article was updated on **01/09/2020** with more information about devices that might require you to use the Blocker Toolkit, on **2/28/2020** to remove "MDM managed" from the criteria of devices to be excluded from this automatic update, and on **6/30/2020** to reflect that all Windows Update connected devices are in scope to receive this update (effective no sooner than 7/30/2020).</span></span>

> [!NOTE]
> <span data-ttu-id="e3877-106">Эта статья относится к Microsoft Edge из канала Stable.</span><span class="sxs-lookup"><span data-stu-id="e3877-106">This applies to Microsoft Edge Stable channel.</span></span>

## <span data-ttu-id="e3877-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="e3877-107">Overview</span></span>

<span data-ttu-id="e3877-108">Чтобы помочь нашим клиентам обеспечить безопасность и актуальное состояние устройств, корпорация Майкрософт будет распространять Microsoft Edge (на основе Chromium) для всех устройств, подключенных к Центру обновления Windows и использующих Windows 10 версии 1803 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="e3877-108">To help our customers become more secure and up-to-date, Microsoft will distribute Microsoft Edge (Chromium-based) to all Windows Update-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="e3877-109">Этот процесс начнется после 15 января 2020г. с предоставлением дополнительных сведений в эту дату.</span><span class="sxs-lookup"><span data-stu-id="e3877-109">This process will start after January 15, 2020 and more information will be available on that date.</span></span>

<span data-ttu-id="e3877-110">Набор средств блокировки Blocker Toolkit предназначен для организаций, которым необходимо заблокировать автоматическую доставку Microsoft Edge (на основе Chromium) для устройств, подключенных к Центру обновления Windows и использующих Windows 10 версии 1803 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="e3877-110">The Blocker Toolkit is intended for organizations that would like to block automatic delivery of Microsoft Edge (Chromium-based) to Windows Updated-connected devices running Windows 10 version 1803 and newer.</span></span>
<span data-ttu-id="e3877-111">Устройства под управлением Windows Server Update Services (WSUS) или Центра обновления Windows для бизнеса (WUfB) будут исключены из этого автоматического обновления.</span><span class="sxs-lookup"><span data-stu-id="e3877-111">Devices that are Windows Server Update Services (WSUS) or Windows Update for Business (WUfB) managed will be excluded from this automatic update.</span></span>

**<span data-ttu-id="e3877-112">Важно обратить внимание на следующее.</span><span class="sxs-lookup"><span data-stu-id="e3877-112">It's important to note that:</span></span>**

- <span data-ttu-id="e3877-113">Набор средств блокировки Blocker Toolkit не запрещает пользователям вручную устанавливать Microsoft Edge (на основе Chromium) при скачивании браузера в Интернете или с внешнего носителя.</span><span class="sxs-lookup"><span data-stu-id="e3877-113">The Blocker Toolkit will not prevent users from manually installing Microsoft Edge (Chromium-based) from Internet download, or from external media.</span></span>
- <span data-ttu-id="e3877-114">Организации, обновления которых управляются с помощью Центра обновления Windows для бизнеса (WUfB), не будут получать это обновление автоматически, и им не требуется развертывать набор средств блокировки Blocker Toolkit.</span><span class="sxs-lookup"><span data-stu-id="e3877-114">Organizations with updates managed through Windows Update for Business (WUfB) will not automatically receive this update and do not need to deploy the blocker toolkit.</span></span>
- <span data-ttu-id="e3877-115">Организациям со средами, управляемыми с помощью решения для управления обновлениями, такого как службы Windows Server Update Services (WSUS) или System Center Configuration Manager (SCCM), не требуется развертывать набор средств блокировки Blocker Toolkit.</span><span class="sxs-lookup"><span data-stu-id="e3877-115">Organizations with environments managed with an update management solution such as Windows Server Update Services (WSUS) or System Center Configuration Manager (SCCM) do not have to deploy the Blocker Toolkit.</span></span> <span data-ttu-id="e3877-116">Они могут использовать эти продукты для комплексного управления развертыванием обновлений, выпущенных Центром обновления Windows и Центром обновления Майкрософт, включая Microsoft Edge (на основе Chromium), в своей среде.</span><span class="sxs-lookup"><span data-stu-id="e3877-116">They can use those products to fully manage deployment of updates released through Windows Update and Microsoft Update, including Microsoft Edge (Chromium-based), within their environment.</span></span>
- <span data-ttu-id="e3877-117">Это автономное обновление (не входит в ежемесячное накопительное обновление), которое предоставляет корпоративным клиентам гибкость и максимальный контроль над развертыванием.</span><span class="sxs-lookup"><span data-stu-id="e3877-117">This update is a stand-alone update (not part of the monthly cumulative update) to give Enterprise customers flexibility and maximum control over deploying this update.</span></span>
- <span data-ttu-id="e3877-118">Новая версия Microsoft Edge (на основе Chromium) будет включена в состав обновления компонентов Windows 10 версии 20H2 во второй половине 2020 г.</span><span class="sxs-lookup"><span data-stu-id="e3877-118">The new Microsoft Edge (Chromium-based) will be included as part of the Windows 10, version 20H2 feature update in the second half of 2020.</span></span> <span data-ttu-id="e3877-119">Набор средств Blocker не влияет на поведение и развертывание версии 20H2.</span><span class="sxs-lookup"><span data-stu-id="e3877-119">The Blocker toolkit does not impact 20H2 behaviors or deployment.</span></span> <span data-ttu-id="e3877-120">Дополнительные сведения о Windows 10 версии 20H2 см. [здесь](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span><span class="sxs-lookup"><span data-stu-id="e3877-120">See more information about Windows 10, version 20H2 [here](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span></span>

<span data-ttu-id="e3877-121">Вы можете скачать исполняемый файл набора средств блокировки Blocker Toolkit здесь: [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span><span class="sxs-lookup"><span data-stu-id="e3877-121">You can download the Blocker Toolkit executable file from [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span></span>

### <span data-ttu-id="e3877-122">Компоненты набора средств</span><span class="sxs-lookup"><span data-stu-id="e3877-122">Toolkit components</span></span>

<span data-ttu-id="e3877-123">В этом наборе средств содержатся следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="e3877-123">This toolkit contains the following components:</span></span>

- <span data-ttu-id="e3877-124">Исполняемый сценарий блокировщика (.CMD)</span><span class="sxs-lookup"><span data-stu-id="e3877-124">Executable blocker script (.CMD)</span></span>
- <span data-ttu-id="e3877-125">Административный шаблон групповой политики (.ADMX и .ADML)</span><span class="sxs-lookup"><span data-stu-id="e3877-125">Group Policy Administrative Template (.ADMX and .ADML)</span></span>

### <span data-ttu-id="e3877-126">Поддерживаемые операционные системы</span><span class="sxs-lookup"><span data-stu-id="e3877-126">Supported Operating Systems</span></span>

<span data-ttu-id="e3877-127">Windows10 версии1803 и выше.</span><span class="sxs-lookup"><span data-stu-id="e3877-127">Windows 10 version 1803 and newer.</span></span>

## <span data-ttu-id="e3877-128">Сценарий блокировщика</span><span class="sxs-lookup"><span data-stu-id="e3877-128">Blocker script</span></span>

<span data-ttu-id="e3877-129">Сценарий создает раздел реестра и настраивает связанное значение на блокировку или разблокировку (в зависимости от используемого параметра командной строки) автоматической доставки Microsoft Edge (на основе Chromium) на локальном компьютере или на удаленном целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="e3877-129">The script creates a registry key and sets the associated value to block or unblock (depending on the command-line option used) automatic delivery of Microsoft Edge (Chromium-based) on either the local machine or a remote target machine.</span></span>

**<span data-ttu-id="e3877-130">Раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="e3877-130">Registry key:</span></span>** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**<span data-ttu-id="e3877-131">Имя значения реестра:</span><span class="sxs-lookup"><span data-stu-id="e3877-131">Key value name:</span></span>** `DoNotUpdateToEdgeWithChromium`

| <span data-ttu-id="e3877-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e3877-132">Value</span></span>                | <span data-ttu-id="e3877-133">Результат</span><span class="sxs-lookup"><span data-stu-id="e3877-133">Result</span></span>                         |
|----------------------|--------------------------------|
| *<span data-ttu-id="e3877-134">Раздел не определен</span><span class="sxs-lookup"><span data-stu-id="e3877-134">Key is not defined</span></span>* | <span data-ttu-id="e3877-135">Распространение *не* блокируется.</span><span class="sxs-lookup"><span data-stu-id="e3877-135">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="e3877-136">0</span><span class="sxs-lookup"><span data-stu-id="e3877-136">0</span></span>                    | <span data-ttu-id="e3877-137">Распространение *не* блокируется.</span><span class="sxs-lookup"><span data-stu-id="e3877-137">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="e3877-138">1</span><span class="sxs-lookup"><span data-stu-id="e3877-138">1</span></span>                    | <span data-ttu-id="e3877-139">Распространение блокируется.</span><span class="sxs-lookup"><span data-stu-id="e3877-139">Distribution is blocked.</span></span>       |

<span data-ttu-id="e3877-140">Сценарий имеет следующий синтаксис командной строки:</span><span class="sxs-lookup"><span data-stu-id="e3877-140">The script has the following command-line syntax:</span></span><br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### <span data-ttu-id="e3877-141">Имя компьютера</span><span class="sxs-lookup"><span data-stu-id="e3877-141">Machine name</span></span>

<span data-ttu-id="e3877-142">Параметр `<machine name>` является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e3877-142">The `<machine name>` parameter is optional.</span></span> <span data-ttu-id="e3877-143">Если этот параметр не указан, действие выполняется на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e3877-143">If not specified, the action is performed on the local machine.</span></span> <span data-ttu-id="e3877-144">В противном случае доступ к удаленному компьютеру осуществляется с помощью возможностей удаленного реестра команды `REG`.</span><span class="sxs-lookup"><span data-stu-id="e3877-144">Otherwise, the remote machine is accessed through the remote registry capabilities of the `REG` command.</span></span> <span data-ttu-id="e3877-145">Если не удается получить доступ к удаленному реестру из-за разрешений безопасности или не удается найти удаленный компьютер, команда `REG` возвращает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e3877-145">If the remote registry can't be accessed due to security permissions or the remote machine can't be found, an error message is returned from the `REG` command.</span></span>

### <span data-ttu-id="e3877-146">Переключатели</span><span class="sxs-lookup"><span data-stu-id="e3877-146">Switches</span></span>

<span data-ttu-id="e3877-147">Переключатели, используемые сценарием, являются взаимоисключающими и действие применяется только к первому допустимому переключателю из конкретной команды.</span><span class="sxs-lookup"><span data-stu-id="e3877-147">Switches used by the script are mutually exclusive and only the first valid switch from a given command is acted on.</span></span> <span data-ttu-id="e3877-148">Сценарий может выполняться несколько раз на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e3877-148">The script can be run multiple times on the same machine.</span></span>

| <span data-ttu-id="e3877-149">Переключатель</span><span class="sxs-lookup"><span data-stu-id="e3877-149">Switch</span></span>       | <span data-ttu-id="e3877-150">Описание</span><span class="sxs-lookup"><span data-stu-id="e3877-150">Description</span></span>                              |
|--------------|------------------------------------------|
| `/B`         | <span data-ttu-id="e3877-151">Блокирует распространение</span><span class="sxs-lookup"><span data-stu-id="e3877-151">Blocks distribution</span></span>                      |
| `/U`         | <span data-ttu-id="e3877-152">Разблокирует распространение</span><span class="sxs-lookup"><span data-stu-id="e3877-152">Unblocks distribution</span></span>                    |
| `/H` <span data-ttu-id="e3877-153">или</span><span class="sxs-lookup"><span data-stu-id="e3877-153">or</span></span> `/?` | <span data-ttu-id="e3877-154">Отображает следующую сводную справку.</span><span class="sxs-lookup"><span data-stu-id="e3877-154">Displays the following summary help:</span></span><br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## <span data-ttu-id="e3877-155">Административный шаблон групповой политики (файлы .ADMX и .ADML)</span><span class="sxs-lookup"><span data-stu-id="e3877-155">Group Policy Administrative Template (.ADMX and .ADML files)</span></span>

<span data-ttu-id="e3877-156">Административный шаблон групповой политики (файлы .ADMX и .ADML) позволяют администраторам импортировать новые параметры групповой политики, чтобы блокировать или разблокировать автоматическую доставку Microsoft Edge (на основе Chromium) в свою среду групповых политик, а также использовать групповую политику для централизованного выполнения действия на разных системах в их среде.</span><span class="sxs-lookup"><span data-stu-id="e3877-156">The Group Policy Administrative Template (.ADMX  and .ADML files) allows administrators to import the new Group Policy settings to block or unblock automatic delivery of Microsoft Edge (Chromium-based) into their Group Policy environment, and use Group Policy to centrally execute the action across systems in their environment.</span></span>

<span data-ttu-id="e3877-157">Пользователи, использующие Windows 10 RS3 Enterprise/EDU, RS4 и более новых версий, будут видеть по следующему пути:</span><span class="sxs-lookup"><span data-stu-id="e3877-157">Users running Windows 10 RS3 Enterprise/EDU and RS4 and newer, will see the policy under the following path:</span></span>

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

<span data-ttu-id="e3877-158">Этот параметр доступен только в качестве параметра для компьютера. Параметры для пользователей отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="e3877-158">This setting is available only as a Computer setting; there is no Per-User setting.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3877-159">Этот параметр реестра не хранится в разделе политик и считается *предпочтением.*</span><span class="sxs-lookup"><span data-stu-id="e3877-159">This registry setting isn't stored in a policies key and is considered a *preference*.</span></span> <span data-ttu-id="e3877-160">Таким образом, если объект групповой политики, реализующий параметр, удаляется или политике задается значение **Не настроено**, параметр остается.</span><span class="sxs-lookup"><span data-stu-id="e3877-160">Therefore, if the Group Policy Object that implements the setting is ever removed or the policy is set to **Not Configured**, the setting will remain.</span></span> <span data-ttu-id="e3877-161">Чтобы разблокировать распространение Microsoft Edge (на основе Chromium) с помощью групповой политики, установите для политики значение **Отключено**.</span><span class="sxs-lookup"><span data-stu-id="e3877-161">To unblock distribution of Microsoft Edge (Chromium-based) by using Group Policy, set the policy to **Disabled**.</span></span>

## <span data-ttu-id="e3877-162">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e3877-162">See also</span></span>

- [<span data-ttu-id="e3877-163">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="e3877-163">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="e3877-164">Обновления Windows для поддержки Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e3877-164">Windows updates to support Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [<span data-ttu-id="e3877-165">Как получить доступ к старой версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e3877-165">How to access the old version of Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
