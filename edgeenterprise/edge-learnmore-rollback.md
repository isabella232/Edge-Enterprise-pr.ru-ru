---
title: Откат Microsoft Edge для предприятий
ms.author: v-danwes
author: dan-wesley
manager: srugh
ms.date: 07/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Как откатить Microsoft Edge к предыдущей версии
ms.openlocfilehash: 9af0881a079dd3059e567eaadb912b3d929924c4
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980897"
---
# <span data-ttu-id="ea252-103">Как откатить Microsoft Edge к предыдущей версии</span><span class="sxs-lookup"><span data-stu-id="ea252-103">How to roll back Microsoft Edge to a previous version</span></span>

<span data-ttu-id="ea252-104">В этой статье описано, как вернуться к предыдущей версии Microsoft Edge с помощью функции отката.</span><span class="sxs-lookup"><span data-stu-id="ea252-104">This article describes how to roll back to a previous version of Microsoft Edge using the rollback feature.</span></span>

>[!NOTE]
><span data-ttu-id="ea252-105">Эта статья относится к Microsoft Edge версии 86 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ea252-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <span data-ttu-id="ea252-106">Знакомство с откатом</span><span class="sxs-lookup"><span data-stu-id="ea252-106">Introduction to rollback</span></span>

<span data-ttu-id="ea252-107">Откат позволяет вам заменить версию браузера Microsoft Edge более ранней.</span><span class="sxs-lookup"><span data-stu-id="ea252-107">Rollback lets you replace your Microsoft Edge browser version with an earlier version.</span></span> <span data-ttu-id="ea252-108">Эта функция разработана в качестве средства предохранения для предприятий, разворачивающих Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ea252-108">This feature is designed to be a safety net for enterprises deploying Microsoft Edge.</span></span> <span data-ttu-id="ea252-109">Она предоставляет способ устранения проблем с Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ea252-109">It provides a way to troubleshoot issues with Microsoft Edge.</span></span> <span data-ttu-id="ea252-110">Преимущество отката — это возможность легко и быстро вернуться к предыдущей версии браузера.</span><span class="sxs-lookup"><span data-stu-id="ea252-110">The benefits of rollback are the ability to revert to previous browser version easily and quickly.</span></span> <span data-ttu-id="ea252-111">Откат снижает возможное воздействие проблем Microsoft Edge на бизнес-операции.</span><span class="sxs-lookup"><span data-stu-id="ea252-111">Rollback reduces the potential impact that a Microsoft Edge issue has on business operations.</span></span>

## <span data-ttu-id="ea252-112">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="ea252-112">Before you begin</span></span>

<span data-ttu-id="ea252-113">Важно понимать, как функция отката установлена в среде Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ea252-113">It's important to understand how the rollback feature is installed in a Microsoft Edge environment.</span></span> <span data-ttu-id="ea252-114">Вы можете развернуть откат двумя способами: вручную с помощью MSI или с помощью обновления Microsoft Edge и групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ea252-114">You can deploy rollback using two different methods: manually with an MSI or by using Microsoft Edge update and Group Policy.</span></span> <span data-ttu-id="ea252-115">Кроме того, мы рекомендуем использовать избранные групповые политики для плавного развертывания.</span><span class="sxs-lookup"><span data-stu-id="ea252-115">We also  encourage using a selection of Group Policies for a smoother deployment.</span></span>

### <span data-ttu-id="ea252-116">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="ea252-116">Recommendations</span></span>

<span data-ttu-id="ea252-117">Функция отката предназначена для временного решения проблем, которые могут возникнуть при обновлении браузера Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ea252-117">The rollback feature is meant to be a temporary fix for issues you might find in a Microsoft Edge browser update.</span></span> <span data-ttu-id="ea252-118">Пользователям рекомендуется устанавливать последнюю версию браузера Microsoft Edge, чтобы использовать защиту, обеспечиваемую новейшими обновлениями для системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="ea252-118">We recommend that users install the latest version of the Microsoft Edge browser to use the protection provided by the latest security updates.</span></span> <span data-ttu-id="ea252-119">Откат к более ранней версии сопровождается риском возникновения известных проблем безопасности.</span><span class="sxs-lookup"><span data-stu-id="ea252-119">Rollback to an earlier version risks exposure to known security issues.</span></span>

<span data-ttu-id="ea252-120">Перед временным откатом версии браузера мы также настоятельно рекомендуем включить синхронизацию для всех пользователей в организации.</span><span class="sxs-lookup"><span data-stu-id="ea252-120">Before temporarily rolling back your browser version, we also highly recommend that you enable Sync for all the users in your organization.</span></span> <span data-ttu-id="ea252-121">Если не включить синхронизацию, возникает риск необратимой потери данных браузера.</span><span class="sxs-lookup"><span data-stu-id="ea252-121">If you don't turn on Sync, there's a risk of permanent browsing data loss.</span></span> <span data-ttu-id="ea252-122">Дополнительные сведения о синхронизации см. в статье [Синхронизация Microsoft Edge](microsoft-edge-enterprise-sync.md).</span><span class="sxs-lookup"><span data-stu-id="ea252-122">For more information about Sync, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md).</span></span>

> [!CAUTION]
> <span data-ttu-id="ea252-123">Используйте откат только при необходимости. Он всегда сопровождается риском потери данных.</span><span class="sxs-lookup"><span data-stu-id="ea252-123">Only use rollback when necessary, there's always the risk of data loss.</span></span>

## <span data-ttu-id="ea252-124">Включение отката вручную с помощью MSI</span><span class="sxs-lookup"><span data-stu-id="ea252-124">Enable rollback manually with an MSI</span></span>

<span data-ttu-id="ea252-125">Чтобы выполнить откат вручную с помощью MSI, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ea252-125">Use the following steps to roll back manually with an MSI.</span></span>

1. <span data-ttu-id="ea252-126">Отключите Центр обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ea252-126">Disable Microsoft Edge Updates.</span></span>

   > [!NOTE]
   > <span data-ttu-id="ea252-127">Рекомендуем установить самые последние административные шаблоны.</span><span class="sxs-lookup"><span data-stu-id="ea252-127">We recommend that you install the most current Administrative templates.</span></span> <span data-ttu-id="ea252-128">Дополнительные сведения см. в разделе [Скачивание и установка административного шаблона Microsoft Edge](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).</span><span class="sxs-lookup"><span data-stu-id="ea252-128">For more information, see [Download and install the Microsoft Edge administrative template](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).</span></span>

   - <span data-ttu-id="ea252-129">Откройте редактор локальных групповых политик и перейдите в раздел *Конфигурация компьютера > Административные шаблоны > Центр обновления Microsoft Edge > Приложения > Microsoft Edge >*.</span><span class="sxs-lookup"><span data-stu-id="ea252-129">Open the local Group Policy Editor and go to *Computer Configuration>Administrative Templates>Microsoft Edge Update>Applications>Microsoft Edge>*.</span></span>
   - <span data-ttu-id="ea252-130">Щелкните **Переопределение политики обновления** и выберите **Включено**.</span><span class="sxs-lookup"><span data-stu-id="ea252-130">Select **Update policy override** and then select **Enabled**.</span></span>
   - <span data-ttu-id="ea252-131">В разделе **Параметры** выберите **Обновление отключено** в раскрывающемся списке политик.</span><span class="sxs-lookup"><span data-stu-id="ea252-131">Under **Options**, pick **Update disabled** from the Policy dropdown list.</span></span>

2. <span data-ttu-id="ea252-132">Получите установщик MSI.</span><span class="sxs-lookup"><span data-stu-id="ea252-132">Get the MSI.</span></span>

   - <span data-ttu-id="ea252-133">Скачайте MSI для версии, на которую вы хотите откатиться, [отсюда](https://www.microsoft.com/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="ea252-133">Download the MSI for the version you want to roll back to [from here](https://www.microsoft.com/edge/business/download).</span></span>
   - <span data-ttu-id="ea252-134">Сохраните MSI на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="ea252-134">Save the MSI to your desktop.</span></span>

3. <span data-ttu-id="ea252-135">Выполните команду отката.</span><span class="sxs-lookup"><span data-stu-id="ea252-135">Run the rollback command.</span></span>

   - <span data-ttu-id="ea252-136">Откройте командную строку Windows с помощью параметра **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="ea252-136">Open the Windows command prompt with **Run as administrator**.</span></span>
   - <span data-ttu-id="ea252-137">Введите следующую команду, где *C:\Users\username\Desktop\test*  — это путь к скачанному MSI-файлу, а FileName — это имя MSI-файла:</span><span class="sxs-lookup"><span data-stu-id="ea252-137">Type the following command, where: *C:\Users\username\Desktop\test* is the path to the MSI you downloaded, and FileName is the name of the .msi file:</span></span><br>
 `C:\Users\username\Desktop\test>msiexec /I FileName.msi /qn ALLOWDOWNGRADE=1`<br>
     > [!NOTE]
     > <span data-ttu-id="ea252-138">Дополнительные сведения о команде msiexec см. в статье [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).</span><span class="sxs-lookup"><span data-stu-id="ea252-138">For more information about msiexec, see [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).</span></span>
   - <span data-ttu-id="ea252-139">Закройте и снова откройте Microsoft Edge, чтобы убедиться в выполнении отката.</span><span class="sxs-lookup"><span data-stu-id="ea252-139">Close and reopen Microsoft Edge to verify that the rollback worked.</span></span> <span data-ttu-id="ea252-140">В разделе **Настройки и прочее** (ALT+F), откройте **Настройки** и выберите **О программе Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="ea252-140">Under **Settings and more** (ALT + F), go to **Settings** and select **About Microsoft Edge**.</span></span>

## <span data-ttu-id="ea252-141">Включение отката с помощью обновления Microsoft Edge и групповой политики</span><span class="sxs-lookup"><span data-stu-id="ea252-141">Enable rollback with Microsoft Edge update and Group Policy</span></span>

<span data-ttu-id="ea252-142">Чтобы включить откат с помощью обновления Microsoft Edge и групповой политики, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ea252-142">Use the following steps to enable rollback with Microsoft Edge update and Group Policy.</span></span>

1. <span data-ttu-id="ea252-143">Откройте редактор локальных групповых политик и перейдите в раздел *Конфигурация компьютера > Административные шаблоны > Центр обновления Microsoft Edge > Приложения > Microsoft Edge >*.</span><span class="sxs-lookup"><span data-stu-id="ea252-143">Open the local Group Policy Editor and go to *Computer Configuration>Administrative Templates>Microsoft Edge Update>Applications>Microsoft Edge>*.</span></span>
2. <span data-ttu-id="ea252-144">Нажмите **Откат до целевой версии** и выберите **Включено**.</span><span class="sxs-lookup"><span data-stu-id="ea252-144">Select **Rollback to target version** and then select **Enabled**.</span></span>
3. <span data-ttu-id="ea252-145">Щелкните **Переопределение целевой версии** и выберите версию браузера, на которую нужно откатиться.</span><span class="sxs-lookup"><span data-stu-id="ea252-145">Select **Target version override** and pick the browser version you want to roll back to.</span></span>
4. <span data-ttu-id="ea252-146">Щелкните **Переопределение политики обновления** и выберите **Включено**.</span><span class="sxs-lookup"><span data-stu-id="ea252-146">Select **Update policy override** and then select **Enabled**.</span></span> <span data-ttu-id="ea252-147">В разделе **Параметры** выберите один из следующих вариантов в раскрывающемся списке политик (кроме **Обновление отключено**):</span><span class="sxs-lookup"><span data-stu-id="ea252-147">Under **Options**, pick one of the following options from the Policy dropdown list (except for **Update disabled**):</span></span>

   - <span data-ttu-id="ea252-148">Всегда разрешать обновления</span><span class="sxs-lookup"><span data-stu-id="ea252-148">Always allow updates</span></span>
   - <span data-ttu-id="ea252-149">Только автоматические обновления</span><span class="sxs-lookup"><span data-stu-id="ea252-149">Automatic silent updates only</span></span>
   - <span data-ttu-id="ea252-150">Только обновления вручную</span><span class="sxs-lookup"><span data-stu-id="ea252-150">Manual updates only</span></span>  

5. <span data-ttu-id="ea252-151">Откат произойдет при следующей проверке обновлений Центром обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ea252-151">Rollback will happen the next time Microsoft Edge Update checks for an update.</span></span>

   > [!NOTE]
   > <span data-ttu-id="ea252-152">Если вы хотите откатиться сразу, вам потребуется изменить интервал опроса Центра обновления Microsoft Edge или включить откат с помощью MSI.</span><span class="sxs-lookup"><span data-stu-id="ea252-152">If you want rollback to happen right away you have to change the Microsoft Edge Update polling interval or enable rollback using an MSI.</span></span>

### <span data-ttu-id="ea252-153">Распространенные ошибки отката</span><span class="sxs-lookup"><span data-stu-id="ea252-153">Common rollback errors</span></span>

<span data-ttu-id="ea252-154">Следующие ошибки препятствуют откату:</span><span class="sxs-lookup"><span data-stu-id="ea252-154">The following errors will prevent rollback:</span></span>

- <span data-ttu-id="ea252-155">Ввод неподдерживаемой целевой версии</span><span class="sxs-lookup"><span data-stu-id="ea252-155">Input is an unsupported target version</span></span>
- <span data-ttu-id="ea252-156">Ввод несуществующий целевой версии</span><span class="sxs-lookup"><span data-stu-id="ea252-156">Input is a non-existent target version</span></span>
- <span data-ttu-id="ea252-157">Введенные данные неправильно отформатированы</span><span class="sxs-lookup"><span data-stu-id="ea252-157">Input is incorrectly formatted</span></span>

### <span data-ttu-id="ea252-158">Рекомендуемые групповые политики</span><span class="sxs-lookup"><span data-stu-id="ea252-158">Recommended Group Policies</span></span>

<span data-ttu-id="ea252-159">Для отката настоятельно рекомендуется использовать следующие групповые политики и параметры.</span><span class="sxs-lookup"><span data-stu-id="ea252-159">The following group policies and settings are highly recommended for using rollback.</span></span>

#### <span data-ttu-id="ea252-160">Групповые политики синхронизации</span><span class="sxs-lookup"><span data-stu-id="ea252-160">Sync Group Policies</span></span>

- <span data-ttu-id="ea252-161">ForceSync.</span><span class="sxs-lookup"><span data-stu-id="ea252-161">ForceSync.</span></span> <span data-ttu-id="ea252-162">Присвойте политике ForceSync значение "Включено".</span><span class="sxs-lookup"><span data-stu-id="ea252-162">Set ForceSync to enabled.</span></span> <span data-ttu-id="ea252-163">Эта политика принудительно включает синхронизацию для всех пользователей Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="ea252-163">This policy will force enable Sync on all Azure Active Directory (Azure AD) users.</span></span> <span data-ttu-id="ea252-164">Эта политика действует только в версиях Microsoft Edge 86 и более поздних.</span><span class="sxs-lookup"><span data-stu-id="ea252-164">This policy is only effective for Microsoft Edge versions 86 and later.</span></span>
- <span data-ttu-id="ea252-165">Политика *Настроить список типов, исключаемых из политики синхронизации* позволяет администраторам указывать, какие данные могут синхронизировать пользователи.</span><span class="sxs-lookup"><span data-stu-id="ea252-165">The *Configure the list of the types that are excluded from synchronization policy* allows admins to control what data can be synced by users.</span></span>

#### <span data-ttu-id="ea252-166">Групповые политики перезапуска браузера</span><span class="sxs-lookup"><span data-stu-id="ea252-166">Browser restart Group Policies</span></span>

<span data-ttu-id="ea252-167">Рекомендуем принудительно использовать перезапуск для пользователей после включения отката.</span><span class="sxs-lookup"><span data-stu-id="ea252-167">We recommend forcing a restart on users after rollback is enabled.</span></span>

- <span data-ttu-id="ea252-168">Включите политику *Уведомлять пользователя, что для ожидающих обновлений рекомендуется или требуется перезапуск браузера*.</span><span class="sxs-lookup"><span data-stu-id="ea252-168">Enable *Notify a user that a browser restart is recommended or required for pending updates*.</span></span> <span data-ttu-id="ea252-169">В разделе параметров выберите **Обязательно**.</span><span class="sxs-lookup"><span data-stu-id="ea252-169">Under Options, select **Required**.</span></span>
- <span data-ttu-id="ea252-170">Включите параметр *Установить период времени для уведомлений об обновлениях* и задайте нужное время в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="ea252-170">Enable *Set the time period for update notifications* and then set the desired time in milliseconds.</span></span>

## <span data-ttu-id="ea252-171">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="ea252-171">Frequently asked questions</span></span>

### <span data-ttu-id="ea252-172">Откат вручную с помощью MSI</span><span class="sxs-lookup"><span data-stu-id="ea252-172">Manual MSI rollback</span></span>

#### <span data-ttu-id="ea252-173">Какие общие сбои MSI могут возникать?</span><span class="sxs-lookup"><span data-stu-id="ea252-173">What generic MSI failures that can happen?</span></span>

1. <span data-ttu-id="ea252-174">Если групповая политика установки обновлений отключена, откат не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea252-174">If the Install update group policy is disabled, rollback won't occur.</span></span>

   - <span data-ttu-id="ea252-175">Чтобы использовать откат, присвойте политике установки значение **Включено**.</span><span class="sxs-lookup"><span data-stu-id="ea252-175">To use rollback, make sure Install is set to **Enabled**.</span></span> <span data-ttu-id="ea252-176">Если эта политика отключена, каналы Microsoft Edge не устанавливаются.</span><span class="sxs-lookup"><span data-stu-id="ea252-176">When this policy is disabled, it prevents Microsoft Edge channels from being installed.</span></span> <span data-ttu-id="ea252-177">Дополнительные сведения см. в разделе [Установка](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).</span><span class="sxs-lookup"><span data-stu-id="ea252-177">For more information, see [Install](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).</span></span>

2. <span data-ttu-id="ea252-178">Если обновление компонента паравиртуализации отсутствует, установка Microsoft Edge будет блокироваться, если не включен параметр *Разрешить параллельный запуск разных типов браузеров Microsoft Edge*.</span><span class="sxs-lookup"><span data-stu-id="ea252-178">If Enlightenment Updates aren't present, Microsoft Edge installations will be blocked unless *Allow Microsoft Edge Side by Side browser experience* is enabled.</span></span>

   - <span data-ttu-id="ea252-179">Для Windows версий 1903 и 1909: если последнее обновление было выполнено до октября 2019 г., у вас может возникать эта проблема.</span><span class="sxs-lookup"><span data-stu-id="ea252-179">For Windows versions 1903 and 1909: If your last update was before October 2019, you may have this issue.</span></span>
   - <span data-ttu-id="ea252-180">Для Windows версий 1709, 1803 и 1809: если последнее обновление было выполнено до ноября 2019 г., у вас может возникать эта проблема.</span><span class="sxs-lookup"><span data-stu-id="ea252-180">For Windows versions 1709, 1803, and 1809: If your last update was before November 2019, you may have this issue.</span></span><br>
<span data-ttu-id="ea252-181">Дополнительные сведения см. в разделе [Обновления Windows для обеспечения поддержки следующей версии Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates).</span><span class="sxs-lookup"><span data-stu-id="ea252-181">For more information, see [Windows updates to support the next version of Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)</span></span>

#### <span data-ttu-id="ea252-182">После использования командной строки отображается следующее сообщение об ошибке и откат не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea252-182">The following error message was shown after using the Command Prompt and rollback didn't occur.</span></span> <span data-ttu-id="ea252-183">В чем заключается проблема?</span><span class="sxs-lookup"><span data-stu-id="ea252-183">What's wrong?</span></span>

![Сообщение о состоянии отката](./media/edge-learnmore-rollback/edge-rollback-cmd-flag-error.png)

<span data-ttu-id="ea252-185">Команда *ALLOWDOWNGRADE=1* не выполнена.</span><span class="sxs-lookup"><span data-stu-id="ea252-185">*ALLOWDOWNGRADE=1* was not executed.</span></span>

### <span data-ttu-id="ea252-186">Откат с помощью Центра обновления Microsoft Edge и групповой политики</span><span class="sxs-lookup"><span data-stu-id="ea252-186">Microsoft Edge Update and Group Policy rollback</span></span>

#### <span data-ttu-id="ea252-187">Я настроил политику *Откат до целевой версии*, включил *Переопределение политики обновления*, ввел нужную версию браузера для политики *Переопределение целевой версии*, но версия браузера отличается от ожидаемой.</span><span class="sxs-lookup"><span data-stu-id="ea252-187">I set *Rollback to target version*, enabled *Update policy override*, input my desired browser version for *Target version override*, but the browser version wasn't what I expected.</span></span> <span data-ttu-id="ea252-188">В чем заключается проблема?</span><span class="sxs-lookup"><span data-stu-id="ea252-188">What's wrong?</span></span>

<span data-ttu-id="ea252-189">Некоторые распространенные ошибки, препятствующие откату:</span><span class="sxs-lookup"><span data-stu-id="ea252-189">Some common errors that prevent rollback are:</span></span>

- <span data-ttu-id="ea252-190">Если политика "Откат до целевой версии" не настроена, откат не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea252-190">If Rollback to target version isn't set, rollback will not be executed.</span></span>
- <span data-ttu-id="ea252-191">Существует одна из следующих проблем с параметром переопределения целевой версии:</span><span class="sxs-lookup"><span data-stu-id="ea252-191">There are one of the following issues with the target version override setting:</span></span>

  - <span data-ttu-id="ea252-192">Переопределение целевой версии настроено на неподдерживаемую целевую версию.</span><span class="sxs-lookup"><span data-stu-id="ea252-192">Target version override is set to an unsupported target version.</span></span>
  - <span data-ttu-id="ea252-193">Переопределение целевой версии настроено на несуществующую целевую версию.</span><span class="sxs-lookup"><span data-stu-id="ea252-193">Target version override is set to a non-existent target version.</span></span>
  - <span data-ttu-id="ea252-194">Введенные данные переопределения целевой версии имеют неверный формат.</span><span class="sxs-lookup"><span data-stu-id="ea252-194">Target version override input is incorrectly formatted.</span></span>

- <span data-ttu-id="ea252-195">Если параметру переопределения политики обновления присвоено значение "Обновления отключены", Центр обновления Microsoft Edge не будет принимать обновления.</span><span class="sxs-lookup"><span data-stu-id="ea252-195">If Update policy override is set to "Updates disabled", Microsoft Edge Update won't accept any updates.</span></span> <span data-ttu-id="ea252-196">В результате откат не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea252-196">This results in rollback not getting executed.</span></span>

### <span data-ttu-id="ea252-197">Я правильно настроил все групповые политики, но откат не выполнен.</span><span class="sxs-lookup"><span data-stu-id="ea252-197">I set all the group policies correctly, but rollback didn't execute.</span></span> <span data-ttu-id="ea252-198">Что случилось?</span><span class="sxs-lookup"><span data-stu-id="ea252-198">What happened?</span></span>

<span data-ttu-id="ea252-199">Центр обновления Microsoft Edge еще не проверял наличие обновлений.</span><span class="sxs-lookup"><span data-stu-id="ea252-199">Microsoft Edge Update hasn't run a check for updates yet.</span></span> <span data-ttu-id="ea252-200">По умолчанию автоматическая проверка наличия обновлений выполняется каждые 10 часов.</span><span class="sxs-lookup"><span data-stu-id="ea252-200">By default, auto-update checks for updates every 10 hours.</span></span> <span data-ttu-id="ea252-201">Вы можете устранить эту проблему, изменив интервал опроса Центра обновления Microsoft Edge с помощью групповой политики переопределения периода автоматической проверки обновлений.</span><span class="sxs-lookup"><span data-stu-id="ea252-201">You can fix this by changing Microsoft Edge Update's polling interval with the Auto-update check period override group policy.</span></span> <span data-ttu-id="ea252-202">Дополнительные сведения см. в политике [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes).</span><span class="sxs-lookup"><span data-stu-id="ea252-202">For more information, see the [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes) policy.</span></span>

### <span data-ttu-id="ea252-203">В качестве ИТ-администратора я правильно выполнил все действия для отката.</span><span class="sxs-lookup"><span data-stu-id="ea252-203">As an IT admin, I followed all the steps for rollback correctly.</span></span> <span data-ttu-id="ea252-204">Откат выполнен только для части моей группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="ea252-204">Only a portion of my user group was rolled back.</span></span> <span data-ttu-id="ea252-205">Почему другие пользователи еще не откатились?</span><span class="sxs-lookup"><span data-stu-id="ea252-205">Why haven't the other users been rolled back yet?</span></span>

<span data-ttu-id="ea252-206">Параметр групповой политики еще не синхронизирован со всеми клиентами.</span><span class="sxs-lookup"><span data-stu-id="ea252-206">The group policy setting hasn't synced to all the clients yet.</span></span> <span data-ttu-id="ea252-207">Когда администраторы настраивают групповую политику, клиенты не сразу получают эти параметры.</span><span class="sxs-lookup"><span data-stu-id="ea252-207">When admins set a group policy, clients don't receive these settings instantaneously.</span></span>

<!--
You can update all users' group policy with the  

When admins set all users don't get this setting instantaneously 

GP Update force group policy – link to this 

-->





## <span data-ttu-id="ea252-208">См. также</span><span class="sxs-lookup"><span data-stu-id="ea252-208">See also</span></span>

- [<span data-ttu-id="ea252-209">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="ea252-209">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
