---
title: Откат Microsoft Edge для предприятий
ms.author: v-danwes
author: dan-wesley
manager: srugh
ms.date: 02/04/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Как откатить Microsoft Edge к предыдущей версии
ms.openlocfilehash: 2059ea04bf8ec3a03266fe95599ea3b515b78c12
ms.sourcegitcommit: c290b0b0fa6b7d7f94dcdfdda91302da733326ec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314572"
---
# <span data-ttu-id="c5561-103">Как откатить Microsoft Edge к предыдущей версии</span><span class="sxs-lookup"><span data-stu-id="c5561-103">How to roll back Microsoft Edge to a previous version</span></span>

<span data-ttu-id="c5561-104">В этой статье описано, как вернуться к предыдущей версии Microsoft Edge с помощью функции отката.</span><span class="sxs-lookup"><span data-stu-id="c5561-104">This article describes how to roll back to a previous version of Microsoft Edge using the rollback feature.</span></span> <span data-ttu-id="c5561-105">Чтобы узнать больше об этой функции, посмотрите видео [Откат версии Microsoft Edge](microsoft-edge-video-version-rollback.md).</span><span class="sxs-lookup"><span data-stu-id="c5561-105">To learn more about this feature, watch [Video: Microsoft Edge version rollback](microsoft-edge-video-version-rollback.md).</span></span>

>[!NOTE]
><span data-ttu-id="c5561-106">Эта статья относится к Microsoft Edge версии 86 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="c5561-106">This article applies to Microsoft Edge version 86 or later.</span></span>

## <span data-ttu-id="c5561-107">Знакомство с откатом</span><span class="sxs-lookup"><span data-stu-id="c5561-107">Introduction to rollback</span></span>

<span data-ttu-id="c5561-108">Откат позволяет вам заменить версию браузера Microsoft Edge более ранней.</span><span class="sxs-lookup"><span data-stu-id="c5561-108">Rollback lets you replace your Microsoft Edge browser version with an earlier version.</span></span> <span data-ttu-id="c5561-109">Эта функция разработана в качестве средства предохранения для предприятий, разворачивающих Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c5561-109">This feature is designed to be a safety net for enterprises deploying Microsoft Edge.</span></span> <span data-ttu-id="c5561-110">Она предоставляет способ устранения проблем с Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c5561-110">It provides a way to troubleshoot issues with Microsoft Edge.</span></span> <span data-ttu-id="c5561-111">Преимущество отката — это возможность легко и быстро вернуться к предыдущей версии браузера.</span><span class="sxs-lookup"><span data-stu-id="c5561-111">The benefits of rollback are the ability to revert to previous browser version easily and quickly.</span></span> <span data-ttu-id="c5561-112">Откат снижает возможное воздействие проблем Microsoft Edge на бизнес-операции.</span><span class="sxs-lookup"><span data-stu-id="c5561-112">Rollback reduces the potential impact that a Microsoft Edge issue has on business operations.</span></span>

## <span data-ttu-id="c5561-113">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="c5561-113">Before you begin</span></span>

<span data-ttu-id="c5561-114">Важно понимать, как функция отката установлена в среде Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c5561-114">It's important to understand how the rollback feature is installed in a Microsoft Edge environment.</span></span> <span data-ttu-id="c5561-115">Вы можете развернуть откат двумя способами: вручную с помощью MSI или с помощью обновления Microsoft Edge и групповой политики.</span><span class="sxs-lookup"><span data-stu-id="c5561-115">You can deploy rollback using two different methods: manually with an MSI or by using Microsoft Edge update and Group Policy.</span></span> <span data-ttu-id="c5561-116">Кроме того, мы рекомендуем использовать избранные групповые политики для плавного развертывания.</span><span class="sxs-lookup"><span data-stu-id="c5561-116">We also wencourage using a selection of Group Policies for a smoother deployment.</span></span>

### <span data-ttu-id="c5561-117">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="c5561-117">Recommendations</span></span>

<span data-ttu-id="c5561-118">Функция отката предназначена для временного решения проблем, которые могут возникнуть при обновлении браузера Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c5561-118">The rollback feature is meant to be a temporary fix for issues you might find in a Microsoft Edge browser update.</span></span> <span data-ttu-id="c5561-119">Пользователям рекомендуется устанавливать последнюю версию браузера Microsoft Edge, чтобы использовать защиту, обеспечиваемую новейшими обновлениями для системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="c5561-119">We recommend that users install the latest version of the Microsoft Edge browser to use the protection provided by the latest security updates.</span></span> <span data-ttu-id="c5561-120">Откат к более ранней версии сопровождается риском возникновения известных проблем безопасности.</span><span class="sxs-lookup"><span data-stu-id="c5561-120">Rollback to an earlier version risks exposure to known security issues.</span></span>

<span data-ttu-id="c5561-121">Перед временным откатом версии браузера мы также настоятельно рекомендуем включить синхронизацию для всех пользователей в организации.</span><span class="sxs-lookup"><span data-stu-id="c5561-121">Before temporarily rolling back your browser version, we also highly recommend that you enable Sync for all the users in your organization.</span></span> <span data-ttu-id="c5561-122">Если не включить синхронизацию, возникает риск необратимой потери данных браузера.</span><span class="sxs-lookup"><span data-stu-id="c5561-122">If you don't turn on Sync, there's a risk of permanent browsing data loss.</span></span> <span data-ttu-id="c5561-123">Дополнительные сведения о синхронизации см. в статье [Синхронизация Microsoft Edge](microsoft-edge-enterprise-sync.md).</span><span class="sxs-lookup"><span data-stu-id="c5561-123">For more information about Sync, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md).</span></span>

> [!CAUTION]
> <span data-ttu-id="c5561-124">Используйте откат только при необходимости. Он всегда сопровождается риском потери данных.</span><span class="sxs-lookup"><span data-stu-id="c5561-124">Only use rollback when necessary, there's always the risk of data loss.</span></span>

## <span data-ttu-id="c5561-125">Включение отката вручную с помощью MSI</span><span class="sxs-lookup"><span data-stu-id="c5561-125">Enable rollback manually with an MSI</span></span>

<span data-ttu-id="c5561-126">Чтобы выполнить откат вручную с помощью MSI, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c5561-126">Use the following steps to roll back manually with an MSI.</span></span>

1. <span data-ttu-id="c5561-127">Отключите Центр обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c5561-127">Disable Microsoft Edge Updates.</span></span>

   > [!NOTE]
   > <span data-ttu-id="c5561-128">Рекомендуем установить самые последние административные шаблоны.</span><span class="sxs-lookup"><span data-stu-id="c5561-128">We recommend that you install the most current Administrative templates.</span></span> <span data-ttu-id="c5561-129">Дополнительные сведения см. в разделе [Скачивание и установка административного шаблона Microsoft Edge](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).</span><span class="sxs-lookup"><span data-stu-id="c5561-129">For more information, see [Download and install the Microsoft Edge administrative template](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).</span></span>

   - <span data-ttu-id="c5561-130">Откройте редактор локальных групповых политик и перейдите в раздел *Конфигурация компьютера > Административные шаблоны > Центр обновления Microsoft Edge > Приложения > Microsoft Edge >*.</span><span class="sxs-lookup"><span data-stu-id="c5561-130">Open the local Group Policy Editor and go to *Computer Configuration>Administrative Templates>Microsoft Edge Update>Applications>Microsoft Edge>*.</span></span>
   - <span data-ttu-id="c5561-131">Щелкните **Переопределение политики обновления** и выберите **Включено**.</span><span class="sxs-lookup"><span data-stu-id="c5561-131">Select **Update policy override** and then select **Enabled**.</span></span>
   - <span data-ttu-id="c5561-132">В разделе **Параметры** выберите **Обновление отключено** в раскрывающемся списке политик.</span><span class="sxs-lookup"><span data-stu-id="c5561-132">Under **Options**, pick **Update disabled** from the Policy dropdown list.</span></span>

2. <span data-ttu-id="c5561-133">Получите установщик MSI.</span><span class="sxs-lookup"><span data-stu-id="c5561-133">Get the MSI.</span></span>

   - <span data-ttu-id="c5561-134">Скачайте MSI для версии, на которую вы хотите откатиться, [отсюда](https://www.microsoft.com/edge/business/download).</span><span class="sxs-lookup"><span data-stu-id="c5561-134">Download the MSI for the version you want to roll back to [from here](https://www.microsoft.com/edge/business/download).</span></span>
   - <span data-ttu-id="c5561-135">Сохраните MSI на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="c5561-135">Save the MSI to your desktop.</span></span>

3. <span data-ttu-id="c5561-136">Выполните команду отката.</span><span class="sxs-lookup"><span data-stu-id="c5561-136">Run the rollback command.</span></span>

   - <span data-ttu-id="c5561-137">Откройте командную строку Windows с помощью параметра **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="c5561-137">Open the Windows command prompt with **Run as administrator**.</span></span>
   - <span data-ttu-id="c5561-138">Введите следующую команду, где *C:\Users\username\Desktop\test*  — это путь к скачанному MSI-файлу, а FileName — это имя MSI-файла:</span><span class="sxs-lookup"><span data-stu-id="c5561-138">Type the following command, where: *C:\Users\username\Desktop\test* is the path to the MSI you downloaded, and FileName is the name of the .msi file:</span></span><br>
 `C:\Users\username\Desktop\test>msiexec /I FileName.msi /qn ALLOWDOWNGRADE=1`<br>
     > [!NOTE]
     > <span data-ttu-id="c5561-139">Дополнительные сведения о команде msiexec см. в статье [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).</span><span class="sxs-lookup"><span data-stu-id="c5561-139">For more information about msiexec, see [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).</span></span>
   - <span data-ttu-id="c5561-140">Закройте и снова откройте Microsoft Edge, чтобы убедиться в выполнении отката.</span><span class="sxs-lookup"><span data-stu-id="c5561-140">Close and reopen Microsoft Edge to verify that the rollback worked.</span></span> <span data-ttu-id="c5561-141">В разделе **Настройки и прочее** (ALT+F), откройте **Настройки** и выберите **О программе Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="c5561-141">Under **Settings and more** (ALT + F), go to **Settings** and select **About Microsoft Edge**.</span></span>

## <span data-ttu-id="c5561-142">Включение отката с помощью обновления Microsoft Edge и групповой политики</span><span class="sxs-lookup"><span data-stu-id="c5561-142">Enable rollback with Microsoft Edge update and Group Policy</span></span>

<span data-ttu-id="c5561-143">Чтобы включить откат с помощью обновления Microsoft Edge и групповой политики, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c5561-143">Use the following steps to enable rollback with Microsoft Edge update and Group Policy.</span></span>

1. <span data-ttu-id="c5561-144">Откройте редактор локальных групповых политик и перейдите в раздел *Конфигурация компьютера > Административные шаблоны > Центр обновления Microsoft Edge > Приложения > Microsoft Edge >*.</span><span class="sxs-lookup"><span data-stu-id="c5561-144">Open the local Group Policy Editor and go to *Computer Configuration>Administrative Templates>Microsoft Edge Update>Applications>Microsoft Edge>*.</span></span>
2. <span data-ttu-id="c5561-145">Нажмите **Откат до целевой версии** и выберите **Включено**.</span><span class="sxs-lookup"><span data-stu-id="c5561-145">Select **Rollback to target version** and then select **Enabled**.</span></span>
3. <span data-ttu-id="c5561-146">Щелкните **Переопределение целевой версии** и выберите версию браузера, на которую нужно откатиться.</span><span class="sxs-lookup"><span data-stu-id="c5561-146">Select **Target version override** and pick the browser version you want to roll back to.</span></span>
4. <span data-ttu-id="c5561-147">Щелкните **Переопределение политики обновления** и выберите **Включено**.</span><span class="sxs-lookup"><span data-stu-id="c5561-147">Select **Update policy override** and then select **Enabled**.</span></span> <span data-ttu-id="c5561-148">В разделе **Параметры** выберите один из следующих вариантов в раскрывающемся списке политик (кроме **Обновление отключено**):</span><span class="sxs-lookup"><span data-stu-id="c5561-148">Under **Options**, pick one of the following options from the Policy dropdown list (except for **Update disabled**):</span></span>

   - <span data-ttu-id="c5561-149">Всегда разрешать обновления</span><span class="sxs-lookup"><span data-stu-id="c5561-149">Always allow updates</span></span>
   - <span data-ttu-id="c5561-150">Только автоматические обновления</span><span class="sxs-lookup"><span data-stu-id="c5561-150">Automatic silent updates only</span></span>

     > [!NOTE]
     > <span data-ttu-id="c5561-151">Чтобы принудительно выполнить обновление групповой политики, введите `gpupdate /force` в командной строке администратора Windows (Запуск от имени администратора).</span><span class="sxs-lookup"><span data-stu-id="c5561-151">To force a group policy update, type `gpupdate /force` at the Windows administrator Command Prompt (Run as administrator).</span></span>

5. <span data-ttu-id="c5561-152">Нажмите **ОК**, чтобы сохранить параметры политики.</span><span class="sxs-lookup"><span data-stu-id="c5561-152">Click **OK** to save the policy settings.</span></span> <span data-ttu-id="c5561-153">Откат произойдет при следующей проверке обновлений Центром обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c5561-153">Rollback will happen the next time Microsoft Edge Update checks for an update.</span></span> <span data-ttu-id="c5561-154">Если вы хотите ускорить обновление, вы можете изменить интервал опроса Центра обновления Microsoft Edge или включить откат с помощью MSI.</span><span class="sxs-lookup"><span data-stu-id="c5561-154">If you want the update to happen sooner, you can change the Microsoft Edge Update polling interval or enable rollback using an MSI.</span></span>

### <span data-ttu-id="c5561-155">Распространенные ошибки отката</span><span class="sxs-lookup"><span data-stu-id="c5561-155">Common rollback errors</span></span>

<span data-ttu-id="c5561-156">Следующие ошибки препятствуют откату:</span><span class="sxs-lookup"><span data-stu-id="c5561-156">The following errors will prevent rollback:</span></span>

- <span data-ttu-id="c5561-157">Ввод неподдерживаемой целевой версии</span><span class="sxs-lookup"><span data-stu-id="c5561-157">Input is an unsupported target version</span></span>
- <span data-ttu-id="c5561-158">Ввод несуществующий целевой версии</span><span class="sxs-lookup"><span data-stu-id="c5561-158">Input is a non-existent target version</span></span>
- <span data-ttu-id="c5561-159">Введенные данные неправильно отформатированы</span><span class="sxs-lookup"><span data-stu-id="c5561-159">Input is incorrectly formatted</span></span>

### <span data-ttu-id="c5561-160">Рекомендуемые групповые политики</span><span class="sxs-lookup"><span data-stu-id="c5561-160">Recommended Group Policies</span></span>

<span data-ttu-id="c5561-161">Для отката настоятельно рекомендуется использовать следующие групповые политики и параметры.</span><span class="sxs-lookup"><span data-stu-id="c5561-161">The following group policies and settings are highly recommended for using rollback.</span></span>

#### <span data-ttu-id="c5561-162">Групповые политики синхронизации</span><span class="sxs-lookup"><span data-stu-id="c5561-162">Sync Group Policies</span></span>

- <span data-ttu-id="c5561-163">ForceSync.</span><span class="sxs-lookup"><span data-stu-id="c5561-163">ForceSync.</span></span> <span data-ttu-id="c5561-164">Присвойте политике ForceSync значение "Включено".</span><span class="sxs-lookup"><span data-stu-id="c5561-164">Set ForceSync to enabled.</span></span> <span data-ttu-id="c5561-165">Эта политика принудительно включает синхронизацию для всех пользователей Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="c5561-165">This policy will force enable Sync on all Azure Active Directory (Azure AD) users.</span></span> <span data-ttu-id="c5561-166">Эта политика действует только в версиях Microsoft Edge 86 и более поздних.</span><span class="sxs-lookup"><span data-stu-id="c5561-166">This policy is only effective for Microsoft Edge versions 86 and later.</span></span>
- <span data-ttu-id="c5561-167">Политика *Настроить список типов, исключаемых из политики синхронизации* позволяет администраторам указывать, какие данные могут синхронизировать пользователи.</span><span class="sxs-lookup"><span data-stu-id="c5561-167">The *Configure the list of the types that are excluded from synchronization policy* allows admins to control what data can be synced by users.</span></span>

#### <span data-ttu-id="c5561-168">Групповые политики перезапуска браузера</span><span class="sxs-lookup"><span data-stu-id="c5561-168">Browser restart Group Policies</span></span>

<span data-ttu-id="c5561-169">Рекомендуем принудительно использовать перезапуск для пользователей после включения отката.</span><span class="sxs-lookup"><span data-stu-id="c5561-169">We recommend forcing a restart on users after rollback is enabled.</span></span>

- <span data-ttu-id="c5561-170">Включите политику *Уведомлять пользователя, что для ожидающих обновлений рекомендуется или требуется перезапуск браузера*.</span><span class="sxs-lookup"><span data-stu-id="c5561-170">Enable *Notify a user that a browser restart is recommended or required for pending updates*.</span></span> <span data-ttu-id="c5561-171">В разделе параметров выберите **Обязательно**.</span><span class="sxs-lookup"><span data-stu-id="c5561-171">Under Options, select **Required**.</span></span>
- <span data-ttu-id="c5561-172">Включите параметр *Установить период времени для уведомлений об обновлениях* и задайте нужное время в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="c5561-172">Enable *Set the time period for update notifications* and then set the desired time in milliseconds.</span></span>

## <span data-ttu-id="c5561-173">Моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="c5561-173">Snapshot</span></span>

<span data-ttu-id="c5561-174">Моментальный снимок — это копия папки данных пользователя со штампом версии.</span><span class="sxs-lookup"><span data-stu-id="c5561-174">A snapshot is a version stamped copy of the user data folder.</span></span> <span data-ttu-id="c5561-175">При обновлении версии создается моментальный снимок предыдущей версии и сохраняется в папке снимков.</span><span class="sxs-lookup"><span data-stu-id="c5561-175">During a version upgrade, a snapshot of the previous version is made and stored in the snapshot folder.</span></span> <span data-ttu-id="c5561-176">После выполнения отката снимок соответствующей версии копируется в новую папку данных пользователя и удаляется из папки снимков.</span><span class="sxs-lookup"><span data-stu-id="c5561-176">After rollback occurs, a version matched snapshot will be copied into the new user data folder and deleted from the snapshot folder.</span></span> <span data-ttu-id="c5561-177">Если при переходе на более раннюю версию снимок соответствующий версии недоступен, при откате будет использоваться синхронизация для внесения данных пользователя в новую версию Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c5561-177">If no version matched snapshot is available upon downgrade, rollback will rely on Sync to populate user data into the new Microsoft Edge version.</span></span>

<span data-ttu-id="c5561-178">Групповая политика [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userdatasnapshotretentionlimit) позволяет установить ограничение количества моментальных снимков, которые могут быть сохранены в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="c5561-178">The [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userdatasnapshotretentionlimit) group policy allows you to set a limit for the number of snapshots that can be retained at any given time.</span></span> <span data-ttu-id="c5561-179">По умолчанию сохраняются три снимка.</span><span class="sxs-lookup"><span data-stu-id="c5561-179">By default, three snapshots are kept.</span></span> <span data-ttu-id="c5561-180">Эту политику можно настроить так, чтобы сохранялось 0–5 моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="c5561-180">You can configure this policy to keep from 0-5 snapshots.</span></span>

## <span data-ttu-id="c5561-181">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="c5561-181">Frequently asked questions</span></span>

### <span data-ttu-id="c5561-182">Откат вручную с помощью MSI</span><span class="sxs-lookup"><span data-stu-id="c5561-182">Manual MSI rollback</span></span>

#### <span data-ttu-id="c5561-183">Какие общие сбои MSI могут возникать?</span><span class="sxs-lookup"><span data-stu-id="c5561-183">What generic MSI failures that can happen?</span></span>

1. <span data-ttu-id="c5561-184">Если групповая политика установки обновлений отключена, откат не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c5561-184">If the Install update group policy is disabled, rollback won't occur.</span></span>

   - <span data-ttu-id="c5561-185">Чтобы использовать откат, присвойте политике установки значение **Включено**.</span><span class="sxs-lookup"><span data-stu-id="c5561-185">To use rollback, make sure Install is set to **Enabled**.</span></span> <span data-ttu-id="c5561-186">Если эта политика отключена, каналы Microsoft Edge не устанавливаются.</span><span class="sxs-lookup"><span data-stu-id="c5561-186">When this policy is disabled, it prevents Microsoft Edge channels from being installed.</span></span> <span data-ttu-id="c5561-187">Дополнительные сведения см. в разделе [Установка](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).</span><span class="sxs-lookup"><span data-stu-id="c5561-187">For more information, see [Install](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).</span></span>

2. <span data-ttu-id="c5561-188">Если обновление компонента паравиртуализации отсутствует, установка Microsoft Edge будет блокироваться, если не включен параметр *Разрешить параллельный запуск разных типов браузеров Microsoft Edge*.</span><span class="sxs-lookup"><span data-stu-id="c5561-188">If Enlightenment Updates aren't present, Microsoft Edge installations will be blocked unless *Allow Microsoft Edge Side by Side browser experience* is enabled.</span></span>

   - <span data-ttu-id="c5561-189">Для Windows версий 1903 и 1909: если последнее обновление было выполнено до октября 2019 г., у вас может возникать эта проблема.</span><span class="sxs-lookup"><span data-stu-id="c5561-189">For Windows versions 1903 and 1909: If your last update was before October 2019, you may have this issue.</span></span>
   - <span data-ttu-id="c5561-190">Для Windows версий 1709, 1803 и 1809: если последнее обновление было выполнено до ноября 2019 г., у вас может возникать эта проблема.</span><span class="sxs-lookup"><span data-stu-id="c5561-190">For Windows versions 1709, 1803, and 1809: If your last update was before November 2019, you may have this issue.</span></span><br>
<span data-ttu-id="c5561-191">Дополнительные сведения см. в разделе [Обновления Windows для обеспечения поддержки следующей версии Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates).</span><span class="sxs-lookup"><span data-stu-id="c5561-191">For more information, see [Windows updates to support the next version of Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)</span></span>

#### <span data-ttu-id="c5561-192">После использования командной строки отображается следующее сообщение об ошибке и откат не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c5561-192">The following error message was shown after using the Command Prompt and rollback didn't occur.</span></span> <span data-ttu-id="c5561-193">В чем заключается проблема?</span><span class="sxs-lookup"><span data-stu-id="c5561-193">What's wrong?</span></span>

![Сообщение о состоянии отката](./media/edge-learnmore-rollback/edge-rollback-cmd-flag-error.png)

<span data-ttu-id="c5561-195">Команда *ALLOWDOWNGRADE=1* не выполнена.</span><span class="sxs-lookup"><span data-stu-id="c5561-195">*ALLOWDOWNGRADE=1* was not executed.</span></span>

### <span data-ttu-id="c5561-196">Откат с помощью Центра обновления Microsoft Edge и групповой политики</span><span class="sxs-lookup"><span data-stu-id="c5561-196">Microsoft Edge Update and Group Policy rollback</span></span>

#### <span data-ttu-id="c5561-197">Я настроил политику *Откат до целевой версии*, включил *Переопределение политики обновления*, ввел нужную версию браузера для политики *Переопределение целевой версии*, но версия браузера отличается от ожидаемой.</span><span class="sxs-lookup"><span data-stu-id="c5561-197">I set *Rollback to target version*, enabled *Update policy override*, input my desired browser version for *Target version override*, but the browser version wasn't what I expected.</span></span> <span data-ttu-id="c5561-198">В чем заключается проблема?</span><span class="sxs-lookup"><span data-stu-id="c5561-198">What's wrong?</span></span>

<span data-ttu-id="c5561-199">Некоторые распространенные ошибки, препятствующие откату:</span><span class="sxs-lookup"><span data-stu-id="c5561-199">Some common errors that prevent rollback are:</span></span>

- <span data-ttu-id="c5561-200">Если политика "Откат до целевой версии" не настроена, откат не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c5561-200">If Rollback to target version isn't set, rollback will not be executed.</span></span>
- <span data-ttu-id="c5561-201">Существует одна из следующих проблем с параметром переопределения целевой версии:</span><span class="sxs-lookup"><span data-stu-id="c5561-201">There are one of the following issues with the target version override setting:</span></span>

  - <span data-ttu-id="c5561-202">Переопределение целевой версии настроено на неподдерживаемую целевую версию.</span><span class="sxs-lookup"><span data-stu-id="c5561-202">Target version override is set to an unsupported target version.</span></span>
  - <span data-ttu-id="c5561-203">Переопределение целевой версии настроено на несуществующую целевую версию.</span><span class="sxs-lookup"><span data-stu-id="c5561-203">Target version override is set to a non-existent target version.</span></span>
  - <span data-ttu-id="c5561-204">Введенные данные переопределения целевой версии имеют неверный формат.</span><span class="sxs-lookup"><span data-stu-id="c5561-204">Target version override input is incorrectly formatted.</span></span>

- <span data-ttu-id="c5561-205">Если параметру переопределения политики обновления присвоено значение "Обновления отключены", Центр обновления Microsoft Edge не будет принимать обновления и откат не будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="c5561-205">If Update policy override is set to "Updates disabled", Microsoft Edge Update won't accept any updates and rollback isn't executed.</span></span>

### <span data-ttu-id="c5561-206">Я правильно настроил все групповые политики, но откат не выполнен.</span><span class="sxs-lookup"><span data-stu-id="c5561-206">I set all the group policies correctly, but rollback didn't execute.</span></span> <span data-ttu-id="c5561-207">Что случилось?</span><span class="sxs-lookup"><span data-stu-id="c5561-207">What happened?</span></span>

<span data-ttu-id="c5561-208">Центр обновления Microsoft Edge еще не проверял наличие обновлений.</span><span class="sxs-lookup"><span data-stu-id="c5561-208">Microsoft Edge Update hasn't run a check for updates yet.</span></span> <span data-ttu-id="c5561-209">По умолчанию автоматическая проверка наличия обновлений выполняется каждые 10 часов.</span><span class="sxs-lookup"><span data-stu-id="c5561-209">By default, auto-update checks for updates every 10 hours.</span></span> <span data-ttu-id="c5561-210">Вы можете устранить эту проблему, изменив интервал опроса Центра обновления Microsoft Edge с помощью групповой политики переопределения периода автоматической проверки обновлений.</span><span class="sxs-lookup"><span data-stu-id="c5561-210">You can fix this issue by changing Microsoft Edge Update's polling interval with the Auto-update check period override group policy.</span></span> <span data-ttu-id="c5561-211">Дополнительные сведения см. в политике [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes).</span><span class="sxs-lookup"><span data-stu-id="c5561-211">For more information, see the [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes) policy.</span></span>

### <span data-ttu-id="c5561-212">В качестве ИТ-администратора я правильно выполнил все действия для отката.</span><span class="sxs-lookup"><span data-stu-id="c5561-212">As an IT admin, I followed all the steps for rollback correctly.</span></span> <span data-ttu-id="c5561-213">Откат выполнен только для части моей группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="c5561-213">Only a portion of my user group was rolled back.</span></span> <span data-ttu-id="c5561-214">Почему другие пользователи еще не откатились?</span><span class="sxs-lookup"><span data-stu-id="c5561-214">Why haven't the other users been rolled back yet?</span></span>

<span data-ttu-id="c5561-215">Параметр групповой политики еще не синхронизирован со всеми клиентами.</span><span class="sxs-lookup"><span data-stu-id="c5561-215">The group policy setting hasn't synced to all the clients yet.</span></span> <span data-ttu-id="c5561-216">Когда администраторы настраивают групповую политику, клиенты не сразу получают эти параметры.</span><span class="sxs-lookup"><span data-stu-id="c5561-216">When admins set a group policy, clients don't receive these settings instantaneously.</span></span> <span data-ttu-id="c5561-217">Вы можете выполнить [принудительное удаленное обновление групповой политики](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj134201(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="c5561-217">You can [Force a Remote Group Policy Refresh](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj134201(v=ws.11)).</span></span>

## <span data-ttu-id="c5561-218">См. также</span><span class="sxs-lookup"><span data-stu-id="c5561-218">See also</span></span>

- [<span data-ttu-id="c5561-219">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="c5561-219">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="c5561-220">Видео: откат версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c5561-220">Video: Microsoft Edge version rollback</span></span>](microsoft-edge-video-version-rollback.md)
