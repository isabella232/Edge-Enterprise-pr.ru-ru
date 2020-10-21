---
title: Доступ к старой версии Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 08/17/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Узнайте, как получить доступ к устаревшей версии Microsoft Edge.
ms.openlocfilehash: e4733d020f3a681ded50e5a087fe086d39362201
ms.sourcegitcommit: f7f7eb69d2298b0f9779a9fd28e3c4e297ef2e05
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125521"
---
# <span data-ttu-id="aa501-103">Получение доступа к устаревшей версии Microsoft Edge после установки новой версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="aa501-103">Access Microsoft Edge Legacy after installing the new version of Microsoft Edge</span></span>

<span data-ttu-id="aa501-104">Узнайте, как получить доступ к устаревшей версии Microsoft Edge после установки новой версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa501-104">Learn how to access Microsoft Edge Legacy after installing the new version of Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="aa501-105">Эта статья относится к Microsoft Edge из [стабильного канала](microsoft-edge-channels.md).</span><span class="sxs-lookup"><span data-stu-id="aa501-105">This article applies to the Microsoft Edge [Stable channel](microsoft-edge-channels.md).</span></span>

<span data-ttu-id="aa501-106">Хотя в большинстве организаций рекомендуется заменить устаревшую версию Microsoft Edge новой версией, есть несколько ситуаций, в которых пользователям потребуется доступ к обеим версиям.</span><span class="sxs-lookup"><span data-stu-id="aa501-106">While most organizations will want to replace Microsoft Edge Legacy with the new version, there are some situations where users will need access to both versions.</span></span> <span data-ttu-id="aa501-107">Например:</span><span class="sxs-lookup"><span data-stu-id="aa501-107">For example:</span></span>

- <span data-ttu-id="aa501-108">Служба поддержки и техническая поддержка, взаимодействующие с пользователями, применяющими любую или обе версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa501-108">Helpdesk and support staff who interact with users who are using either or both versions of Microsoft Edge.</span></span>
- <span data-ttu-id="aa501-109">Разработчики, поддерживающие пользователей, которые применяют любую или обе версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa501-109">Developers who support customers who are using either or both versions of Microsoft Edge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa501-110">Использование устаревшей версии Microsoft Edge параллельно с новой версией Microsoft Edge не рекомендуется для рабочей среды.</span><span class="sxs-lookup"><span data-stu-id="aa501-110">Running Microsoft Edge Legacy side-by-side with the new version of Microsoft Edge is not recommended for use in production.</span></span> <span data-ttu-id="aa501-111">Эту конфигурацию следует использовать только в определенных случаях, когда требуется тестирование с обеими версиями браузера.</span><span class="sxs-lookup"><span data-stu-id="aa501-111">This configuration should only be used in specific cases where testing with both browser versions is required.</span></span>
>
> <span data-ttu-id="aa501-112">Поддержка классического приложения устаревшей версии Microsoft Edge будет прекращена 9 марта 2021 г. Вместо него будет использоваться новая версия Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa501-112">The Microsoft Edge Legacy desktop app will reach end of support on March 9, 2021 in favor of the new Microsoft Edge.</span></span> <span data-ttu-id="aa501-113">Это означает, что устаревшая версия Microsoft Edge не будет получать обновления для системы безопасности после этой даты.</span><span class="sxs-lookup"><span data-stu-id="aa501-113">This means that Microsoft Edge Legacy will not receive security updates after that date.</span></span> <span data-ttu-id="aa501-114">Это изменение применяется ко всем интерфейсам, работающим в классическом приложении устаревшей версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa501-114">This change is applicable to all experiences that run in the Microsoft Edge Legacy desktop app.</span></span> <span data-ttu-id="aa501-115">[Подробнее](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span><span class="sxs-lookup"><span data-stu-id="aa501-115">[Learn more](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span></span>

## <span data-ttu-id="aa501-116">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="aa501-116">Before you begin</span></span>
> [!NOTE]
> <span data-ttu-id="aa501-117">С Windows 10 версии 20H2 устаревшая версия Microsoft Edge отсутствует.</span><span class="sxs-lookup"><span data-stu-id="aa501-117">Starting with Windows 10 version 20H2 Microsoft Edge Legacy is no longer included.</span></span> <span data-ttu-id="aa501-118">Начиная с этой версии Windows 10 параллельная работа не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="aa501-118">Starting with this version of Windows 10 the side-by-side experience is not supported.</span></span>

<span data-ttu-id="aa501-119">Процедуры, приведенные в этой статье, относятся к системам, на которых установлены последние обновления системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="aa501-119">The procedures in this article apply to systems that have been updated with the latest security updates.</span></span> <span data-ttu-id="aa501-120">После установки новой версии Microsoft Edge старая версия (устаревшая версия Microsoft Edge) будет скрыта.</span><span class="sxs-lookup"><span data-stu-id="aa501-120">When the new version of Microsoft Edge is installed, the old version (Microsoft Edge Legacy) will be hidden.</span></span> <span data-ttu-id="aa501-121">По умолчанию при попытке запуска старой версии Microsoft Edge будет открываться новая версия Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa501-121">By default, all attempts to launch the old version will redirect the user to the newly installed version of Microsoft Edge.</span></span> <span data-ttu-id="aa501-122">В этой статье описано, как продолжить использование устаревшей версии Microsoft Edge после установки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa501-122">This article describes how you can keep using Microsoft Edge Legacy after you install Microsoft Edge.</span></span>

## <span data-ttu-id="aa501-123">Краткое руководство: параллельное использование канала Microsoft Edge Beta и устаревшей версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="aa501-123">Quickstart: Side-by-side experience with Microsoft Edge Beta Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="aa501-124">Прежде чем следовать подробным инструкциям в этой статье, выполните следующие два действия, чтобы позволить вашим пользователям параллельно запускать устаревшую версию Microsoft Edge и версию Microsoft Edge [канала Beta](microsoft-edge-channels.md).</span><span class="sxs-lookup"><span data-stu-id="aa501-124">Before using the detailed instructions in this article, consider the following two steps to let your users run Microsoft Edge Legacy and the Microsoft Edge [Beta channel](microsoft-edge-channels.md) side-by-side.</span></span>

1. <span data-ttu-id="aa501-125">Запретите автоматическую установку версии Microsoft Edge из стабильного канала через [Центр обновления Windows](https://support.microsoft.com/help/12373/windows-update-faq).</span><span class="sxs-lookup"><span data-stu-id="aa501-125">Prevent the automatic install of the Stable Channel of Microsoft Edge by [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).</span></span>

   > [!TIP]
   > <span data-ttu-id="aa501-126">Отключите автоматическую доставку Microsoft Edge с помощью [набора средств блокировки](microsoft-edge-blocker-toolkit.md).</span><span class="sxs-lookup"><span data-stu-id="aa501-126">Use the [Blocker Toolkit](microsoft-edge-blocker-toolkit.md) to disable automatic delivery of Microsoft Edge.</span></span>

2. <span data-ttu-id="aa501-127">Установите новую версию Microsoft Edge из [канала Beta](https://www.microsoft.com/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="aa501-127">Install the [Beta channel](https://www.microsoft.com/edge/business/download) of the new version of Microsoft Edge.</span></span>

   > [!NOTE]
   > <span data-ttu-id="aa501-128">Ознакомьтесь с [дополнительными сведениями](#additional-information) о параметрах раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="aa501-128">Read [Additional information](#additional-information) for information about Registry Key settings.</span></span>

<span data-ttu-id="aa501-129">Это решение для параллельного запуска проще и требует меньше действий по администрированию, чем подробное решение, описанное в этой статье.</span><span class="sxs-lookup"><span data-stu-id="aa501-129">This side-by-side solution is less complex and requires less management than the detailed solution described in this article.</span></span> <span data-ttu-id="aa501-130">Тем не менее, это решение означает, что будет использоваться версия из канала Beta, а не из стабильного канала.</span><span class="sxs-lookup"><span data-stu-id="aa501-130">However, this solution does mean that you'll be running the Beta Channel rather than the Stable Channel.</span></span>

## <span data-ttu-id="aa501-131">Параллельное взаимодействие версии Microsoft Edge стабильного канала и устаревшей версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="aa501-131">Side-by-side experience with Microsoft Edge Stable Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="aa501-132">После установки следующей версии Microsoft Edge из стабильного канала на уровне системы текущая версия (устаревшая версия Microsoft Edge) будет скрыта.</span><span class="sxs-lookup"><span data-stu-id="aa501-132">Installing the Stable Channel of the next version of Microsoft Edge at the system-level will cause the current version (Microsoft Edge Legacy) to be hidden.</span></span> <span data-ttu-id="aa501-133">Если вы хотите, чтобы пользователи параллельно видели обе версии Microsoft Edge в Windows, этого можно достичь, присвоив групповой политике **Разрешить параллельный запуск разных типов браузеров Microsoft Edge** значение **Включено**.</span><span class="sxs-lookup"><span data-stu-id="aa501-133">If you want to let your users see both versions of Microsoft Edge side by side in Windows, you can enable this experience by setting the **Allow Microsoft Edge Side by Side browser experience** group policy to **Enabled**.</span></span>

<span data-ttu-id="aa501-134">Информация по этой групповой политике приведена [здесь](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)</span><span class="sxs-lookup"><span data-stu-id="aa501-134">This group policy is documented [here](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)</span></span>

### <span data-ttu-id="aa501-135">Чтобы настроить политику параллельной работы в браузере, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="aa501-135">To set up the side-by-side browser experience policy:</span></span>

1. <span data-ttu-id="aa501-136">Установите определения политики от [Microsoft Edge для бизнеса](https://www.microsoft.com/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="aa501-136">Install the Policy Definitions from [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).</span></span>

   - <span data-ttu-id="aa501-137">Выберите КАНАЛ, СБОРКУ и ПЛАТФОРМУ, которые нужно использовать, и нажмите кнопку ПОЛУЧИТЬ ФАЙЛЫ ПОЛИТИКИ.</span><span class="sxs-lookup"><span data-stu-id="aa501-137">Pick the CHANNEL/BUILD and PLATFORM you want to use, and then click GET POLICY FILES.</span></span>
   - <span data-ttu-id="aa501-138">Извлеките ZIP-файлы.</span><span class="sxs-lookup"><span data-stu-id="aa501-138">Extract the zipped files.</span></span>
   - <span data-ttu-id="aa501-139">Скопируйте файлы msedge.admx и msedgeupdate.admx в каталог `C:\Windows\PolicyDefinitions`.</span><span class="sxs-lookup"><span data-stu-id="aa501-139">Copy msedge.admx and msedgeupdate.admx to the `C:\Windows\PolicyDefinitions` directory.</span></span>
   - <span data-ttu-id="aa501-140">Скопируйте файлы msedge.adml и msedgeupdate.adml (из каталога соответствующего языка/языкового стандарта) в каталог `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]`.</span><span class="sxs-lookup"><span data-stu-id="aa501-140">Copy msedge.adml and msedgeupdate.adml (from the appropriate language/locale directory) to the `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` directory.</span></span>

2. <span data-ttu-id="aa501-141">Откройте редактор групповой политики (gpedit.msc).</span><span class="sxs-lookup"><span data-stu-id="aa501-141">Open the Group Policy Editor (gpedit.msc).</span></span>
3. <span data-ttu-id="aa501-142">В разделе **Конфигурация компьютера** перейдите к подразделу *Административные шаблоны>Центр обновления Microsoft Edge>Приложения*.</span><span class="sxs-lookup"><span data-stu-id="aa501-142">Under **Computer Configuration**, go to *Administrative Templates>Microsoft Edge Update>Applications*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="aa501-143">Если вы не видите папку *Центр обновления Microsoft Edge*, убедитесь, что шаг 1 был выполнен верно.</span><span class="sxs-lookup"><span data-stu-id="aa501-143">If you don't see the *Microsoft Edge Update* folder, verify that step 1 was completed correctly.</span></span>

4. <span data-ttu-id="aa501-144">В разделе **Приложения** дважды щелкните «Разрешить параллельный запуск разных типов браузеров Microsoft Edge».</span><span class="sxs-lookup"><span data-stu-id="aa501-144">Under **Applications**, double-click "Allow Microsoft Edge Side by Side browser experience".</span></span> <span data-ttu-id="aa501-145">Ознакомьтесь с нашими [рекомендациями](#best-practice-guidance), прежде чем перейти к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="aa501-145">See our [best practice guidance](#best-practice-guidance) before continuing to the next step.</span></span>

    > [!NOTE]
    > <span data-ttu-id="aa501-146">По умолчанию этой групповой политике задано значение "Не настроено", из-за чего устаревшая версия Microsoft Edge скрывается после установки новой версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa501-146">By default, this group policy is set to "Not configured", which results in Microsoft Edge Legacy being hidden when the new version of Microsoft Edge is installed.</span></span>

5. <span data-ttu-id="aa501-147">Выберите **Включено**, затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="aa501-147">Select **Enabled** and then click **OK**.</span></span>  

<span data-ttu-id="aa501-148">После настройки этой политики следующему разделу реестра будет присвоено значение "00000001":</span><span class="sxs-lookup"><span data-stu-id="aa501-148">Setting this policy will set the following Registry Key  to '00000001':</span></span>

- <span data-ttu-id="aa501-149">Обозначения:</span><span class="sxs-lookup"><span data-stu-id="aa501-149">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- <span data-ttu-id="aa501-150">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="aa501-150">Value Name:</span></span> `Allowsxs`
- <span data-ttu-id="aa501-151">Тип значения:</span><span class="sxs-lookup"><span data-stu-id="aa501-151">Value Type:</span></span> `'REG_DWORD'`

#### <span data-ttu-id="aa501-152">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="aa501-152">Best practice guidance</span></span>

<span data-ttu-id="aa501-153">Для наилучших результатов политику **Разрешить параллельный запуск разных типов браузеров Microsoft Edge** следует включить до развертывания новой версии Microsoft Edge на устройствах пользователей.</span><span class="sxs-lookup"><span data-stu-id="aa501-153">For the best experience, the **Allow Microsoft Edge Side by Side browser experience** should be enabled before the new version of Microsoft Edge is deployed to your users' devices.</span></span>

<span data-ttu-id="aa501-154">Если групповую политику включить после развертывания Microsoft Edge, возникнут побочные эффекты и потребуются действия, указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="aa501-154">If the group policy is enabled after Microsoft Edge is deployed, there are the following side effects and required actions:</span></span>

1. <span data-ttu-id="aa501-155">Политика **Разрешить параллельный запуск разных типов браузеров Microsoft Edge** вступит в силу только после повторного запуска установщика новой версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa501-155">**Allow Microsoft Edge Side by Side browser experience** won't take effect until after the installer for the new version of Microsoft Edge is run again.</span></span>

   > [!NOTE]
   > <span data-ttu-id="aa501-156">Установщик можно запустить напрямую или автоматически при обновлении новой версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa501-156">The installer can be run directly or automatically when the new version of Microsoft Edge updates.</span></span>

2. <span data-ttu-id="aa501-157">Устаревшую версию Microsoft Edge потребуется повторно закрепить в меню "Пуск" или на панели задач, так как при развертывании новой версии Microsoft Edge закрепление переносится.</span><span class="sxs-lookup"><span data-stu-id="aa501-157">Microsoft Edge Legacy will need to be re-pinned to Start or the Taskbar because the pin is migrated when the new version of Microsoft Edge is deployed.</span></span>
3. <span data-ttu-id="aa501-158">Сайты, закрепленные в меню "Пуск" или на панели задач для устаревшей версии Microsoft Edge, перенесутся в новую версию Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa501-158">Sites that were pinned to Start or the Taskbar for Microsoft Edge Legacy will be migrated to the new version of Microsoft Edge.</span></span>

## <span data-ttu-id="aa501-159">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="aa501-159">Additional information</span></span>

<span data-ttu-id="aa501-160">После обновления систем и установки следующей версии Microsoft Edgeиз стабильного канала устанавливаются следующий раздел реестра и значения:</span><span class="sxs-lookup"><span data-stu-id="aa501-160">After the systems are fully updated and the Stable channel of the next version of Microsoft Edge is installed, the following registry key and value is set:</span></span>

- <span data-ttu-id="aa501-161">Обозначения:</span><span class="sxs-lookup"><span data-stu-id="aa501-161">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- <span data-ttu-id="aa501-162">Значение раздела:</span><span class="sxs-lookup"><span data-stu-id="aa501-162">Key value:</span></span> `BrowserReplacement`

  > [!IMPORTANT]
  > <span data-ttu-id="aa501-163">Этот раздел перезаписывается при каждом обновлении стабильного канала для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa501-163">This key is over-written every time the Microsoft Edge Stable channel is updated.</span></span> <span data-ttu-id="aa501-164">Рекомендуется НЕ удалять этот раздел, чтобы сохранить пользователям доступ к обеим версиям Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa501-164">As a best practice, we recommend that you DO NOT delete this key to allow users to access both versions of Microsoft Edge.</span></span>

## <span data-ttu-id="aa501-165">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="aa501-165">See also</span></span>

- [<span data-ttu-id="aa501-166">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="aa501-166">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="aa501-167">Обновления Windows для поддержки Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="aa501-167">Windows updates to support Microsoft Edge</span></span>](microsoft-edge-sysupdate-windows-updates.md)
