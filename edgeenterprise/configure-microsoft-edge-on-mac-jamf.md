---
title: Настройте Microsoft Edge на macOS с помощью Jamf
ms.author: brianalt
author: dan-wesley
manager: laurawi
ms.date: 02/20/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Настройте параметры политики Microsoft Edge на устройствах Mac с помощью Jamf
ms.openlocfilehash: 336bdfed2c53811615b0183dc5ca7db916cd7428
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980818"
---
# <span data-ttu-id="d945b-103">Настройте параметры политики Microsoft Edge в macOS с помощью Jamf</span><span class="sxs-lookup"><span data-stu-id="d945b-103">Configure Microsoft Edge policy settings on macOS with Jamf</span></span>

<span data-ttu-id="d945b-104">В этой статье описывается, как настроить параметры политики в macOS с помощью файла манифеста политики Microsoft Edge в Jamf Pro 10.19.</span><span class="sxs-lookup"><span data-stu-id="d945b-104">This article describes how to configure policy settings on macOS using a Microsoft Edge policy manifest file on Jamf Pro 10.19.</span></span>

<span data-ttu-id="d945b-105">Вы также можете настроить параметры политики Microsoft Edge в macOS с помощью файла списка свойств (.plist).</span><span class="sxs-lookup"><span data-stu-id="d945b-105">You can also configure Microsoft Edge policy settings on macOS by using a property list (.plist) file.</span></span> <span data-ttu-id="d945b-106">Для получения дополнительной информации см. [Настройка для MacOS с использованием .plist](configure-microsoft-edge-on-mac.md)</span><span class="sxs-lookup"><span data-stu-id="d945b-106">For more information, see [Configure for macOS using a .plist](configure-microsoft-edge-on-mac.md)</span></span>


## <span data-ttu-id="d945b-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="d945b-107">Prerequisites</span></span>

<span data-ttu-id="d945b-108">Требуется следующее программное обеспечение:</span><span class="sxs-lookup"><span data-stu-id="d945b-108">The following software is required:</span></span>

- <span data-ttu-id="d945b-109">Канал Microsoft Edge Stable 81</span><span class="sxs-lookup"><span data-stu-id="d945b-109">Microsoft Edge Stable channel 81</span></span>
- <span data-ttu-id="d945b-110">Файл шаблонов политики, версия 81.0.416.3</span><span class="sxs-lookup"><span data-stu-id="d945b-110">Policy Templates file, version 81.0.416.3</span></span>
- <span data-ttu-id="d945b-111">Jamf Pro, версия 10,19</span><span class="sxs-lookup"><span data-stu-id="d945b-111">Jamf Pro, Version 10.19</span></span>

## <span data-ttu-id="d945b-112">О меню приложения и пользовательских настроек Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="d945b-112">About the Jamf Pro Application & Custom Settings menu</span></span>

<span data-ttu-id="d945b-113">До Jamf Pro 10.18 управление Office 365 включало в себя создание файла .plist вручную.</span><span class="sxs-lookup"><span data-stu-id="d945b-113">Before Jamf Pro 10.18, managing Office 365 involved manually building a .plist file.</span></span> <span data-ttu-id="d945b-114">Это был трудоемкий рабочий процесс, который требовал сильной технической подготовки.</span><span class="sxs-lookup"><span data-stu-id="d945b-114">This was a time-consuming workflow that required a strong technical background.</span></span> <span data-ttu-id="d945b-115">Jamf Pro 10.18 устранил эти барьеры, оптимизировав процесс настройки.</span><span class="sxs-lookup"><span data-stu-id="d945b-115">Jamf Pro 10.18 eliminated those barriers by streamlining the configuration process.</span></span> <span data-ttu-id="d945b-116">Однако ИТ-администраторы могут использовать этот новый пользовательский интерфейс только для конкретных приложений и доменов предпочтений, указанных в Jamf.</span><span class="sxs-lookup"><span data-stu-id="d945b-116">However, IT Admins could only use this new user interface for specific applications and preference domains specified by Jamf.</span></span>

<span data-ttu-id="d945b-117">В Jamf Pro 10.19 пользователь может загрузить манифест JSON в виде «пользовательской схемы», чтобы указать любой домен настроек, и из этого манифеста будет создан графический интерфейс пользователя.</span><span class="sxs-lookup"><span data-stu-id="d945b-117">In Jamf Pro 10.19, a user can upload a JSON manifest as a "custom schema" to target any preference domain, and the graphical user interface will be generated from this manifest.</span></span> <span data-ttu-id="d945b-118">Созданная пользовательская схема соответствует спецификации JSON Schema.</span><span class="sxs-lookup"><span data-stu-id="d945b-118">The custom schema that's created follows the JSON Schema specification.</span></span>

<span data-ttu-id="d945b-119">Для получения дополнительной информации см. [Профили конфигурации компьютера](https://jamf.it/computer-configuration-profiles) в Руководстве администратора Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="d945b-119">For more information, see [Computer Configuration Profiles](https://jamf.it/computer-configuration-profiles) in the Jamf Pro Administrator's Guide.</span></span>

## <span data-ttu-id="d945b-120">Получить манифест политики для конкретной версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d945b-120">Get the policy manifest for a specific version of Microsoft Edge</span></span>

<span data-ttu-id="d945b-121">Чтобы получить манифест политики:</span><span class="sxs-lookup"><span data-stu-id="d945b-121">To get the policy manifest:</span></span>

- <span data-ttu-id="d945b-122">Перейдите на [целевую страницу Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="d945b-122">Go to the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>
- <span data-ttu-id="d945b-123">В раскрывающемся списке "Канал/Версия" выберите \*\*любой канал версии 81 или более поздней.\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="d945b-123">On the Channel/Version dropdown list, select \*\*any channel with version 81 or later.\*\*\*.</span></span>
- <span data-ttu-id="d945b-124">В раскрывающемся списке "Сборка" выберите любой элемент \*\*сборка 81 или более поздняя.\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="d945b-124">On the Build dropdown list, select any \*\*81 build or later.\*\*\*.</span></span>
- <span data-ttu-id="d945b-125">Нажмите ПОЛУЧИТЬ ФАЙЛЫ ПОЛИТИКИ, чтобы загрузить наш пакет шаблонов политики.</span><span class="sxs-lookup"><span data-stu-id="d945b-125">Click GET POLICY FILES to download our policy templates bundle.</span></span>

  > [!NOTE]
  > <span data-ttu-id="d945b-126">В настоящее время пакет шаблонов политик подписан как файл CAB.</span><span class="sxs-lookup"><span data-stu-id="d945b-126">Currently, the policy templates bundle is signed as a CAB file.</span></span> <span data-ttu-id="d945b-127">Вам понадобится сторонний инструмент, такой как The Unarchiver, чтобы открыть файл в macOS.</span><span class="sxs-lookup"><span data-stu-id="d945b-127">You'll need to use a 3rd party tool, such as The Unarchiver to open the file on macOS.</span></span>

<span data-ttu-id="d945b-128">После распаковки CAB-файла распакуйте ZIP-файл и перейдите в каталог верхнего уровня “mac”.</span><span class="sxs-lookup"><span data-stu-id="d945b-128">After you unpack the CAB file, unpack the ZIP file and navigate to the "mac" top level directory.</span></span> <span data-ttu-id="d945b-129">Манифест, который называется «policy_manifest.json», находится в этом каталоге.</span><span class="sxs-lookup"><span data-stu-id="d945b-129">The manifest, which is named "policy_manifest.json", is in this directory.</span></span>

<span data-ttu-id="d945b-130">Этот манифест будет опубликован в каждом пакете политики, начиная со сборки 81.0.416.3.</span><span class="sxs-lookup"><span data-stu-id="d945b-130">This manifest will be published in every policy bundle starting with build 81.0.416.3.</span></span> <span data-ttu-id="d945b-131">Если вы хотите протестировать политики в канале Dev, вы можете взять манифест, связанный с каждым выпуском Dev, и протестировать его в Jamf Pro.</span><span class="sxs-lookup"><span data-stu-id="d945b-131">If you want to test policies in the Dev channel, you can take the manifest associated with each Dev release and test it in Jamf Pro.</span></span>  

## <span data-ttu-id="d945b-132">Используйте манифест политики в Jamf Pro</span><span class="sxs-lookup"><span data-stu-id="d945b-132">Use the policy manifest in Jamf Pro</span></span>

<span data-ttu-id="d945b-133">Используйте следующие шаги, чтобы загрузить манифест политики в Jamf Pro, а затем создать профиль политики для macOS.</span><span class="sxs-lookup"><span data-stu-id="d945b-133">Use the following steps to upload the policy manifest to Jamf Pro and then create a policy profile for macOS.</span></span>

1. <span data-ttu-id="d945b-134">Войдите в Jamf.</span><span class="sxs-lookup"><span data-stu-id="d945b-134">Sign in to Jamf.</span></span>
2. <span data-ttu-id="d945b-135">Выберите вкладку **Компьютер**.</span><span class="sxs-lookup"><span data-stu-id="d945b-135">Select the **Computer** tab.</span></span>
3. <span data-ttu-id="d945b-136">В разделе **Управление контентом** выберите **Профили конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="d945b-136">Under **Content Management**, select **Configuration Profiles**.</span></span>
4. <span data-ttu-id="d945b-137">На странице **Профили конфигурации** выберите **+ Новый**.</span><span class="sxs-lookup"><span data-stu-id="d945b-137">On the **Configuration Profiles** page, click **+ New**.</span></span>

   ![Добавить новый профиль в Jamf](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles.png)

5. <span data-ttu-id="d945b-139">В разделе **Новый Профиль Конфигурации MacOS**>\*\*Параметры \*\* выберите **Приложения и пользовательские настройки**.</span><span class="sxs-lookup"><span data-stu-id="d945b-139">On **New macOS Configuration Profile**>**Options**, select **Application & Custom Settings**.</span></span>
6. <span data-ttu-id="d945b-140">Во всплывающем окне **Приложения и пользовательские настройки** нажмите **Настроить**.</span><span class="sxs-lookup"><span data-stu-id="d945b-140">On the **Application & Custom Settings** popup window, click **Configure**.</span></span>

   ![Настройка приложения и пользовательских настроек](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom.png)

7. <span data-ttu-id="d945b-142">В разделе **Приложения и пользовательские настройки** установите значения, показанные на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="d945b-142">In the **Application & Custom Settings** section, set the values shown in the following screen shot.</span></span>

   ![Исходный профиль и пользовательская схема](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-schema.png)

   - <span data-ttu-id="d945b-144">В качестве **Метода создания** выберите **Настроить параметры**.</span><span class="sxs-lookup"><span data-stu-id="d945b-144">For **Creation Method**, pick **Configure settings**.</span></span>
   - <span data-ttu-id="d945b-145">В качестве **Источника** выберите **Пользовательскую схему**.</span><span class="sxs-lookup"><span data-stu-id="d945b-145">For **Source**, pick **Custom Schema**.</span></span>
   - <span data-ttu-id="d945b-146">В поле **Предпочтительный домен** укажите имя своего домена.</span><span class="sxs-lookup"><span data-stu-id="d945b-146">For **Preference Domain**, provide the name of your domain.</span></span> <span data-ttu-id="d945b-147">В этом примере в качестве домена используется *com.microsoft.Edge*.</span><span class="sxs-lookup"><span data-stu-id="d945b-147">This example uses *com.microsoft.Edge* as the domain.</span></span>
   - <span data-ttu-id="d945b-148">Для **Пользовательской схемы** вставьте содержимое файла манифеста policy_manifest.json.</span><span class="sxs-lookup"><span data-stu-id="d945b-148">For **Custom Schema**, paste the contents of the "policy_manifest.json" manifest file.</span></span>
   - <span data-ttu-id="d945b-149">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d945b-149">Click **Save**.</span></span>

8. <span data-ttu-id="d945b-150">После сохранения профиля Jamf отобразит раздел **Общие**, показанный на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="d945b-150">After you save the profile, Jamf displays the **General** section shown in the next screen shot.</span></span>

   ![Настройка общего раздела](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-general-setting.png)

   - <span data-ttu-id="d945b-152">Укажите отображаемое **Имя** для профиля и **Описание**.</span><span class="sxs-lookup"><span data-stu-id="d945b-152">Provide a display **Name** for the profile and a **Description**.</span></span>
   - <span data-ttu-id="d945b-153">Оставьте настройку по умолчанию для **Категории**, которой является **Нет**.</span><span class="sxs-lookup"><span data-stu-id="d945b-153">Keep the default setting for **Category**, which is **None**.</span></span>
   - <span data-ttu-id="d945b-154">Для **Метода распространения** доступны следующие варианты: **Автоматическая установка** или **Сделать доступным в самообслуживании**.</span><span class="sxs-lookup"><span data-stu-id="d945b-154">For **Distribution Method**, the options are **Install Automatically** or **Make Available in Self Service**.</span></span>
   - <span data-ttu-id="d945b-155">Для **Уровня** доступны следующие варианты: **Уровень пользователя** или **Уровень компьютера**.</span><span class="sxs-lookup"><span data-stu-id="d945b-155">For **Level**, the options are **User Level** or **Computer Level**.</span></span>
   - <span data-ttu-id="d945b-156">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d945b-156">Click **Save**.</span></span>

9. <span data-ttu-id="d945b-157">После сохранения раздела «Общие» Jamf показывает профиль конфигурации «Microsoft Edge Beta Channel», настроенный для нашего примера.</span><span class="sxs-lookup"><span data-stu-id="d945b-157">After you save the General section, Jamf shows the "Microsoft Edge Beta Channel" configuration profile set up for our example.</span></span> <span data-ttu-id="d945b-158">На следующем снимке экрана обратите внимание, что вы можете продолжить работу с профилем, нажав **Изменить**, или, если вы закончили, нажмите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="d945b-158">In the next screen shot, note that you can keep working the profile by clicking **Edit** or if you're finished, click **Done**.</span></span>

   ![Новый профиль конфигурации с опциями](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel.png)

   > [!NOTE]
   > <span data-ttu-id="d945b-160">Вы можете редактировать этот профиль после того, как он был сохранен и в другой сессии Jamf.</span><span class="sxs-lookup"><span data-stu-id="d945b-160">You can edit this profile after it's been saved and in another Jamf session.</span></span> <span data-ttu-id="d945b-161">Например, вы можете решить изменить метод распространения, чтобы сделать его доступным в режиме самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="d945b-161">For example, you might decide to change the Distribution Method to Make Available in Self Service.</span></span>

   <span data-ttu-id="d945b-162">Чтобы выполнить дальнейшее редактирование на канале Microsoft Edge Stable или удалить его, выберите имя профиля, показанное на следующем снимке экрана профилей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d945b-162">To do a follow up edit on the Microsoft Edge Stable Channel, or delete it, select the profile name, shown in the following Configuration Profiles screen shot.</span></span>

   ![Список профилей конфигурации](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel-done.png)

<span data-ttu-id="d945b-164">После создания нового профиля конфигурации вы все равно должны настроить **Область применения** для этого профиля.</span><span class="sxs-lookup"><span data-stu-id="d945b-164">After you create the new configuration profile you still have to configure the **Scope** for the profile.</span></span>

### <span data-ttu-id="d945b-165">Чтобы настроить Область применения</span><span class="sxs-lookup"><span data-stu-id="d945b-165">To configure the scope</span></span>

1. <span data-ttu-id="d945b-166">Для **Целей** укажите следующие минимальные параметры:</span><span class="sxs-lookup"><span data-stu-id="d945b-166">For **Targets**, provide the following minimum settings:</span></span>

   - <span data-ttu-id="d945b-167">ЦЕЛЕВЫЕ КОМПЬЮТЕРЫ:</span><span class="sxs-lookup"><span data-stu-id="d945b-167">TARGET COMPUTERS.</span></span> <span data-ttu-id="d945b-168">Возможные варианты: Конкретные компьютеры или Все компьютеры.</span><span class="sxs-lookup"><span data-stu-id="d945b-168">The options are Specific Computers or All Computers.</span></span>
   - <span data-ttu-id="d945b-169">ЦЕЛЕВЫЕ ПОЛЬЗОВАТЕЛИ.</span><span class="sxs-lookup"><span data-stu-id="d945b-169">TARGET USERS.</span></span> <span data-ttu-id="d945b-170">Варианты: Конкретные пользователи или Все пользователи.</span><span class="sxs-lookup"><span data-stu-id="d945b-170">The options are Specific Users or All Users.</span></span>
   - <span data-ttu-id="d945b-171">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d945b-171">Click **Save**.</span></span>
2. <span data-ttu-id="d945b-172">Для **Ограничений** оставьте настройку по умолчанию: Нет.</span><span class="sxs-lookup"><span data-stu-id="d945b-172">For **Limitations**, keep the default setting: None.</span></span> <span data-ttu-id="d945b-173">Нажмите кнопку **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="d945b-173">Click **Cancel**.</span></span>
3. <span data-ttu-id="d945b-174">Для **Исключений** оставьте настройку по умолчанию: Нет.</span><span class="sxs-lookup"><span data-stu-id="d945b-174">For **Exclusions**, keep the default setting: None.</span></span> <span data-ttu-id="d945b-175">Нажмите кнопку **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="d945b-175">Click **Cancel**.</span></span>

## <span data-ttu-id="d945b-176">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="d945b-176">Frequently Asked Questions</span></span>

### <span data-ttu-id="d945b-177">Можно ли настроить Microsoft Edge для использования основных параметров?</span><span class="sxs-lookup"><span data-stu-id="d945b-177">Can Microsoft Edge be configured to use master preferences?</span></span>

<span data-ttu-id="d945b-178">Да. Microsoft Edge можно настроить для использования файла основных параметров.</span><span class="sxs-lookup"><span data-stu-id="d945b-178">Yes, you can configure Microsoft Edge to use a master preferences file.</span></span>

<span data-ttu-id="d945b-179">Файл основных параметров позволяет настроить параметры по умолчанию для профиля пользователя браузера при развертывании Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d945b-179">A master preferences file lets you configure default settings for a browser user profile when Microsoft Edge is deployed.</span></span> <span data-ttu-id="d945b-180">Вы также можете использовать файл основных параметров для применения параметров на компьютерах, не управляемых системой управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="d945b-180">You can also use a master preferences file to apply settings on computers that aren't managed by a device management system.</span></span> <span data-ttu-id="d945b-181">Эти параметры применяются к профилю пользователя, когда пользователь запускает браузер в первый раз.</span><span class="sxs-lookup"><span data-stu-id="d945b-181">These settings are applied to the user’s profile the first time the user runs the browser.</span></span> <span data-ttu-id="d945b-182">После того как пользователь запустит браузер, изменения в файл основных параметров не применяются.</span><span class="sxs-lookup"><span data-stu-id="d945b-182">After the user runs the browser, changes to the master preferences file aren’t applied.</span></span> <span data-ttu-id="d945b-183">Пользователь может изменять параметры в файле основных параметров в браузере.</span><span class="sxs-lookup"><span data-stu-id="d945b-183">A user can change settings from the master preferences in the browser.</span></span> <span data-ttu-id="d945b-184">Если необходимо сделать параметр обязательным или изменить параметр после первого запуска браузера, необходимо использовать политику.</span><span class="sxs-lookup"><span data-stu-id="d945b-184">If you want to make a setting mandatory or change a setting after the first run of the browser, you must use a policy.</span></span>

<span data-ttu-id="d945b-185">Файл основных параметров позволяет настраивать различные параметры и предпочтения для браузера, включая те, которые используются совместно с другими браузерами на основе Chromium и относятся к Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d945b-185">A master preferences file lets you to customize many different settings and preferences for the browser, including those shared with other Chromium based browsers and specific to Microsoft Edge.</span></span>  <span data-ttu-id="d945b-186">Параметры, связанные с политикой, можно настроить с помощью файла основных параметров.</span><span class="sxs-lookup"><span data-stu-id="d945b-186">Policy related preferences can be configured using the master preferences file.</span></span> <span data-ttu-id="d945b-187">В случаях, когда задана политика и соответствующий файл основных параметров, приоритет имеет заданная политика.</span><span class="sxs-lookup"><span data-stu-id="d945b-187">In cases where a policy is set and there’s a corresponding master preference set, the policy setting takes precedence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d945b-188">Все доступные параметры могут не соответствовать терминологии Microsoft Edge и соглашениям об именовании.</span><span class="sxs-lookup"><span data-stu-id="d945b-188">All the available preferences might not be consistent with Microsoft Edge terminology and naming conventions.</span></span>  <span data-ttu-id="d945b-189">Правильная работа этих параметров не гарантируется в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="d945b-189">There’s no guarantee that these preferences will continue to work as expected in future releases.</span></span> <span data-ttu-id="d945b-190">В более поздних версиях эти параметры могут быть изменены или проигнорированы.</span><span class="sxs-lookup"><span data-stu-id="d945b-190">Preferences might be changed or ignored in later versions.</span></span>

<span data-ttu-id="d945b-191">Файл основных параметров — это текстовый файл, отформатированный с использованием разметки JSON.</span><span class="sxs-lookup"><span data-stu-id="d945b-191">A master preferences file is a text file that’s formatted using JSON markup.</span></span> <span data-ttu-id="d945b-192">Этот файл необходимо добавлять в тот же каталог, где находится исполняемый файл msedge.exe.</span><span class="sxs-lookup"><span data-stu-id="d945b-192">This file needs to be added to the same directory as the msedge.exe executable.</span></span> <span data-ttu-id="d945b-193">Для корпоративных развертываний на уровне системы в macOS этим каталогом обычно является: "*~/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*" or "*/Library/Microsoft/Microsoft Edge Master Preferences*".</span><span class="sxs-lookup"><span data-stu-id="d945b-193">For system wide enterprise deployments on macOS this is typically: “*~/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*" or "*/Library/Microsoft/Microsoft Edge Master Preferences*”.</span></span>

## <span data-ttu-id="d945b-194">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d945b-194">See also</span></span>

- [<span data-ttu-id="d945b-195">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="d945b-195">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="d945b-196">Настройка для macOS с Intune</span><span class="sxs-lookup"><span data-stu-id="d945b-196">Configure for macOS with Intune</span></span>](configure-microsoft-edge-on-mac.md)
- [<span data-ttu-id="d945b-197">Настройка для Windows</span><span class="sxs-lookup"><span data-stu-id="d945b-197">Configure for Windows</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="d945b-198">Настройка для Windows с помощью Intune</span><span class="sxs-lookup"><span data-stu-id="d945b-198">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)
