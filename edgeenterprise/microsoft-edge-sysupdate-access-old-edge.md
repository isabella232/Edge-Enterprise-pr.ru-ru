---
title: Доступ к старой версии Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Узнайте, как получить доступ к устаревшей версии Microsoft Edge.
ms.openlocfilehash: b521ab9ea093b62db7268e6bf2f4d656b3dc8d4b
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447093"
---
# <a name="access-microsoft-edge-legacy-after-installing-the-new-version-of-microsoft-edge"></a><span data-ttu-id="0c3b5-103">Получение доступа к устаревшей версии Microsoft Edge после установки новой версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0c3b5-103">Access Microsoft Edge Legacy after installing the new version of Microsoft Edge</span></span>

<span data-ttu-id="0c3b5-104">Устаревшая версия Microsoft Edge перестанет получать обновления для системы безопасности 9 марта 2021 г.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-104">Microsoft Edge Legacy will stop receiving security updates on March 9, 2021.</span></span> <span data-ttu-id="0c3b5-105">Вы сможете получать доступ к устаревшей версии Microsoft Edge до 13 апреля.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-105">You can access Microsoft Edge Legacy until April 13.</span></span> <span data-ttu-id="0c3b5-106">Дополнительные сведения см. в [записи блога](https://aka.ms/EdgeLegacyEOS) команды разработчиков продукта Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-106">For more information, see Microsoft Edge Product Team’s [blog post](https://aka.ms/EdgeLegacyEOS).</span></span>

> [!NOTE]
> <span data-ttu-id="0c3b5-107">Эта статья относится к Microsoft Edge из [стабильного канала](microsoft-edge-channels.md).</span><span class="sxs-lookup"><span data-stu-id="0c3b5-107">This article applies to the Microsoft Edge [Stable channel](microsoft-edge-channels.md).</span></span>

<span data-ttu-id="0c3b5-108">Хотя в большинстве организаций рекомендуется заменить устаревшую версию Microsoft Edge новой версией, есть несколько ситуаций, в которых пользователям потребуется доступ к обеим версиям.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-108">While most organizations will want to replace Microsoft Edge Legacy with the new version, there are some situations where users will need access to both versions.</span></span> <span data-ttu-id="0c3b5-109">Например:</span><span class="sxs-lookup"><span data-stu-id="0c3b5-109">For example:</span></span>

- <span data-ttu-id="0c3b5-110">Служба поддержки и техническая поддержка, взаимодействующие с пользователями, применяющими любую или обе версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-110">Helpdesk and support staff who interact with users who are using either or both versions of Microsoft Edge.</span></span>
- <span data-ttu-id="0c3b5-111">Разработчики, поддерживающие пользователей, которые применяют любую или обе версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-111">Developers who support customers who are using either or both versions of Microsoft Edge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c3b5-112">Использование устаревшей версии Microsoft Edge параллельно с новой версией Microsoft Edge не рекомендуется для рабочей среды.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-112">Running Microsoft Edge Legacy side-by-side with the new version of Microsoft Edge is not recommended for use in production.</span></span> <span data-ttu-id="0c3b5-113">Эту конфигурацию следует использовать только в определенных случаях, когда требуется тестирование с обеими версиями браузера.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-113">This configuration should only be used in specific cases where testing with both browser versions is required.</span></span>
>
> <span data-ttu-id="0c3b5-114">Поддержка классического приложения устаревшей версии Microsoft Edge будет прекращена 9 марта 2021 г. Вместо него будет использоваться новая версия Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-114">The Microsoft Edge Legacy desktop app will reach end of support on March 9, 2021 in favor of the new Microsoft Edge.</span></span> <span data-ttu-id="0c3b5-115">Это означает, что устаревшая версия Microsoft Edge не будет получать обновления для системы безопасности после этой даты.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-115">This means that Microsoft Edge Legacy will not receive security updates after that date.</span></span> <span data-ttu-id="0c3b5-116">Это изменение применяется ко всем интерфейсам, работающим в классическом приложении устаревшей версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-116">This change is applicable to all experiences that run in the Microsoft Edge Legacy desktop app.</span></span> <span data-ttu-id="0c3b5-117">[Подробнее](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span><span class="sxs-lookup"><span data-stu-id="0c3b5-117">[Learn more](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="0c3b5-118">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="0c3b5-118">Before you begin</span></span>
> [!NOTE]
> <span data-ttu-id="0c3b5-119">С Windows 10 версии 20H2 устаревшая версия Microsoft Edge отсутствует.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-119">Starting with Windows 10 version 20H2 Microsoft Edge Legacy is no longer included.</span></span> <span data-ttu-id="0c3b5-120">Начиная с этой версии Windows 10 параллельная работа не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-120">Starting with this version of Windows 10 the side-by-side experience is not supported.</span></span>

<span data-ttu-id="0c3b5-121">Процедуры, приведенные в этой статье, относятся к системам, на которых установлены последние обновления системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-121">The procedures in this article apply to systems that have been updated with the latest security updates.</span></span> <span data-ttu-id="0c3b5-122">После установки новой версии Microsoft Edge старая версия (устаревшая версия Microsoft Edge) будет скрыта.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-122">When the new version of Microsoft Edge is installed, the old version (Microsoft Edge Legacy) will be hidden.</span></span> <span data-ttu-id="0c3b5-123">По умолчанию при попытке запуска старой версии Microsoft Edge будет открываться новая версия Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-123">By default, all attempts to launch the old version will redirect the user to the newly installed version of Microsoft Edge.</span></span> <span data-ttu-id="0c3b5-124">В этой статье описано, как продолжить использование устаревшей версии Microsoft Edge после установки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-124">This article describes how you can keep using Microsoft Edge Legacy after you install Microsoft Edge.</span></span>

## <a name="quickstart-side-by-side-experience-with-microsoft-edge-beta-channel-and-microsoft-edge-legacy"></a><span data-ttu-id="0c3b5-125">Краткое руководство: параллельное использование канала Microsoft Edge Beta и устаревшей версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0c3b5-125">Quickstart: Side-by-side experience with Microsoft Edge Beta Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="0c3b5-126">Прежде чем следовать подробным инструкциям в этой статье, выполните следующие два действия, чтобы позволить вашим пользователям параллельно запускать устаревшую версию Microsoft Edge и версию Microsoft Edge [канала Beta](microsoft-edge-channels.md).</span><span class="sxs-lookup"><span data-stu-id="0c3b5-126">Before using the detailed instructions in this article, consider the following two steps to let your users run Microsoft Edge Legacy and the Microsoft Edge [Beta channel](microsoft-edge-channels.md) side-by-side.</span></span>

1. <span data-ttu-id="0c3b5-127">Запретите автоматическую установку версии Microsoft Edge из стабильного канала через [Центр обновления Windows](https://support.microsoft.com/help/12373/windows-update-faq).</span><span class="sxs-lookup"><span data-stu-id="0c3b5-127">Prevent the automatic install of the Stable Channel of Microsoft Edge by [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).</span></span>
2. <span data-ttu-id="0c3b5-128">Установите новую версию Microsoft Edge из [канала Beta](https://www.microsoft.com/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="0c3b5-128">Install the [Beta channel](https://www.microsoft.com/edge/business/download) of the new version of Microsoft Edge.</span></span>

   > [!NOTE]
   > <span data-ttu-id="0c3b5-129">Ознакомьтесь с [дополнительными сведениями](#additional-information) о параметрах раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-129">Read [Additional information](#additional-information) for information about Registry Key settings.</span></span>

<span data-ttu-id="0c3b5-130">Это решение для параллельного запуска проще и требует меньше действий по администрированию, чем подробное решение, описанное в этой статье.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-130">This side-by-side solution is less complex and requires less management than the detailed solution described in this article.</span></span> <span data-ttu-id="0c3b5-131">Тем не менее, это решение означает, что будет использоваться версия из канала Beta, а не из стабильного канала.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-131">However, this solution does mean that you'll be running the Beta Channel rather than the Stable Channel.</span></span>

## <a name="side-by-side-experience-with-microsoft-edge-stable-channel-and-microsoft-edge-legacy"></a><span data-ttu-id="0c3b5-132">Параллельное взаимодействие версии Microsoft Edge стабильного канала и устаревшей версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0c3b5-132">Side-by-side experience with Microsoft Edge Stable Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="0c3b5-133">После установки следующей версии Microsoft Edge из стабильного канала на уровне системы текущая версия (устаревшая версия Microsoft Edge) будет скрыта.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-133">Installing the Stable Channel of the next version of Microsoft Edge at the system-level will cause the current version (Microsoft Edge Legacy) to be hidden.</span></span> <span data-ttu-id="0c3b5-134">Если вы хотите, чтобы пользователи параллельно видели обе версии Microsoft Edge в Windows, этого можно достичь, присвоив групповой политике **Разрешить параллельный запуск разных типов браузеров Microsoft Edge** значение **Включено**.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-134">If you want to let your users see both versions of Microsoft Edge side by side in Windows, you can enable this experience by setting the **Allow Microsoft Edge Side by Side browser experience** group policy to **Enabled**.</span></span>

<span data-ttu-id="0c3b5-135">Информация по этой групповой политике приведена [здесь](./microsoft-edge-update-policies.md#allowsxs)</span><span class="sxs-lookup"><span data-stu-id="0c3b5-135">This group policy is documented [here](./microsoft-edge-update-policies.md#allowsxs)</span></span>

### <a name="to-set-up-the-side-by-side-browser-experience-policy"></a><span data-ttu-id="0c3b5-136">Чтобы настроить политику параллельной работы в браузере, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-136">To set up the side-by-side browser experience policy:</span></span>

1. <span data-ttu-id="0c3b5-137">Установите определения политики от [Microsoft Edge для бизнеса](https://www.microsoft.com/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="0c3b5-137">Install the Policy Definitions from [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).</span></span>

   - <span data-ttu-id="0c3b5-138">Выберите КАНАЛ, СБОРКУ и ПЛАТФОРМУ, которые нужно использовать, и нажмите кнопку ПОЛУЧИТЬ ФАЙЛЫ ПОЛИТИКИ.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-138">Pick the CHANNEL/BUILD and PLATFORM you want to use, and then click GET POLICY FILES.</span></span>
   - <span data-ttu-id="0c3b5-139">Извлеките ZIP-файлы.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-139">Extract the zipped files.</span></span>
   - <span data-ttu-id="0c3b5-140">Скопируйте файлы msedge.admx и msedgeupdate.admx в каталог `C:\Windows\PolicyDefinitions`.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-140">Copy msedge.admx and msedgeupdate.admx to the `C:\Windows\PolicyDefinitions` directory.</span></span>
   - <span data-ttu-id="0c3b5-141">Скопируйте файлы msedge.adml и msedgeupdate.adml (из каталога соответствующего языка/языкового стандарта) в каталог `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]`.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-141">Copy msedge.adml and msedgeupdate.adml (from the appropriate language/locale directory) to the `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` directory.</span></span>

2. <span data-ttu-id="0c3b5-142">Откройте редактор групповой политики (gpedit.msc).</span><span class="sxs-lookup"><span data-stu-id="0c3b5-142">Open the Group Policy Editor (gpedit.msc).</span></span>
3. <span data-ttu-id="0c3b5-143">В разделе **Конфигурация компьютера** перейдите к подразделу *Административные шаблоны>Центр обновления Microsoft Edge>Приложения*.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-143">Under **Computer Configuration**, go to *Administrative Templates>Microsoft Edge Update>Applications*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0c3b5-144">Если вы не видите папку *Центр обновления Microsoft Edge*, убедитесь, что шаг 1 был выполнен верно.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-144">If you don't see the *Microsoft Edge Update* folder, verify that step 1 was completed correctly.</span></span>

4. <span data-ttu-id="0c3b5-145">В разделе **Приложения** дважды щелкните «Разрешить параллельный запуск разных типов браузеров Microsoft Edge».</span><span class="sxs-lookup"><span data-stu-id="0c3b5-145">Under **Applications**, double-click "Allow Microsoft Edge Side by Side browser experience".</span></span> <span data-ttu-id="0c3b5-146">Ознакомьтесь с нашими [рекомендациями](#best-practice-guidance), прежде чем перейти к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-146">See our [best practice guidance](#best-practice-guidance) before continuing to the next step.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0c3b5-147">По умолчанию этой групповой политике задано значение "Не настроено", из-за чего устаревшая версия Microsoft Edge скрывается после установки новой версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-147">By default, this group policy is set to "Not configured", which results in Microsoft Edge Legacy being hidden when the new version of Microsoft Edge is installed.</span></span>

5. <span data-ttu-id="0c3b5-148">Выберите **Включено**, затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-148">Select **Enabled** and then click **OK**.</span></span>  

<span data-ttu-id="0c3b5-149">После настройки этой политики следующему разделу реестра будет присвоено значение "00000001":</span><span class="sxs-lookup"><span data-stu-id="0c3b5-149">Setting this policy will set the following Registry Key  to '00000001':</span></span>

- <span data-ttu-id="0c3b5-150">Обозначения:</span><span class="sxs-lookup"><span data-stu-id="0c3b5-150">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- <span data-ttu-id="0c3b5-151">Имя значения:</span><span class="sxs-lookup"><span data-stu-id="0c3b5-151">Value Name:</span></span> `Allowsxs`
- <span data-ttu-id="0c3b5-152">Тип значения:</span><span class="sxs-lookup"><span data-stu-id="0c3b5-152">Value Type:</span></span> `'REG_DWORD'`

#### <a name="best-practice-guidance"></a><span data-ttu-id="0c3b5-153">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="0c3b5-153">Best practice guidance</span></span>

<span data-ttu-id="0c3b5-154">Для наилучших результатов политику **Разрешить параллельный запуск разных типов браузеров Microsoft Edge** следует включить до развертывания новой версии Microsoft Edge на устройствах пользователей.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-154">For the best experience, the **Allow Microsoft Edge Side by Side browser experience** should be enabled before the new version of Microsoft Edge is deployed to your users' devices.</span></span>

<span data-ttu-id="0c3b5-155">Если групповую политику включить после развертывания Microsoft Edge, возникнут побочные эффекты и потребуются действия, указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-155">If the group policy is enabled after Microsoft Edge is deployed, there are the following side effects and required actions:</span></span>

1. <span data-ttu-id="0c3b5-156">Политика **Разрешить параллельный запуск разных типов браузеров Microsoft Edge** вступит в силу только после повторного запуска установщика новой версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-156">**Allow Microsoft Edge Side by Side browser experience** won't take effect until after the installer for the new version of Microsoft Edge is run again.</span></span>

   > [!NOTE]
   > <span data-ttu-id="0c3b5-157">Установщик можно запустить напрямую или автоматически при обновлении новой версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-157">The installer can be run directly or automatically when the new version of Microsoft Edge updates.</span></span>

2. <span data-ttu-id="0c3b5-158">Устаревшую версию Microsoft Edge потребуется повторно закрепить в меню "Пуск" или на панели задач, так как при развертывании новой версии Microsoft Edge закрепление переносится.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-158">Microsoft Edge Legacy will need to be re-pinned to Start or the Taskbar because the pin is migrated when the new version of Microsoft Edge is deployed.</span></span>
3. <span data-ttu-id="0c3b5-159">Сайты, закрепленные в меню "Пуск" или на панели задач для устаревшей версии Microsoft Edge, перенесутся в новую версию Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-159">Sites that were pinned to Start or the Taskbar for Microsoft Edge Legacy will be migrated to the new version of Microsoft Edge.</span></span>

## <a name="additional-information"></a><span data-ttu-id="0c3b5-160">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="0c3b5-160">Additional information</span></span>

<span data-ttu-id="0c3b5-161">После обновления систем и установки следующей версии Microsoft Edgeиз стабильного канала устанавливаются следующий раздел реестра и значения:</span><span class="sxs-lookup"><span data-stu-id="0c3b5-161">After the systems are fully updated and the Stable channel of the next version of Microsoft Edge is installed, the following registry key and value is set:</span></span>

- <span data-ttu-id="0c3b5-162">Обозначения:</span><span class="sxs-lookup"><span data-stu-id="0c3b5-162">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- <span data-ttu-id="0c3b5-163">Значение раздела:</span><span class="sxs-lookup"><span data-stu-id="0c3b5-163">Key value:</span></span> `BrowserReplacement`

  > [!IMPORTANT]
  > <span data-ttu-id="0c3b5-164">Этот раздел перезаписывается при каждом обновлении стабильного канала для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-164">This key is over-written every time the Microsoft Edge Stable channel is updated.</span></span> <span data-ttu-id="0c3b5-165">Рекомендуется НЕ удалять этот раздел, чтобы сохранить пользователям доступ к обеим версиям Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0c3b5-165">As a best practice, we recommend that you DO NOT delete this key to allow users to access both versions of Microsoft Edge.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c3b5-166">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0c3b5-166">See also</span></span>

- [<span data-ttu-id="0c3b5-167">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="0c3b5-167">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="0c3b5-168">Обновления Windows для поддержки Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0c3b5-168">Windows updates to support Microsoft Edge</span></span>](microsoft-edge-sysupdate-windows-updates.md)