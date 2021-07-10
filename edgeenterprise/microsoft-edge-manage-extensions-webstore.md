---
title: Внутреннее тестирование расширений Microsoft Edge
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Узнайте, как упаковать и выполнить внутреннее тестирование расширений Microsoft Edge на предприятии.
ms.openlocfilehash: aef4438212829006e39572fa938462f13721c580
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642875"
---
# <a name="self-host-microsoft-edge-extensions"></a><span data-ttu-id="db702-103">Внутреннее тестирование расширений Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="db702-103">Self-host Microsoft Edge extensions</span></span>

<span data-ttu-id="db702-104">Данная статья содержит основные рекомендации по упаковке расширения для размещения в собственном интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="db702-104">This article provides basic guidance for packaging an extension to host on your own webstore.</span></span> <span data-ttu-id="db702-105">Она также содержит инструкции по развертыванию расширений для устройств и пользователей в организации.</span><span class="sxs-lookup"><span data-stu-id="db702-105">It also includes instructions on how to deploy extensions to devices and users in your organization.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="db702-106">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="db702-106">Prerequisites</span></span>

<span data-ttu-id="db702-107">Для выполнения внутреннего тестирования собственных расширений необходимо предоставить собственные службы веб-хостинга для расширений и их файлов манифеста.</span><span class="sxs-lookup"><span data-stu-id="db702-107">To self-host your own extensions, you will need to provide your own web hosting services for the extensions and their manifest files.</span></span>

 <span data-ttu-id="db702-108">Следующие действия предполагают, что вы уже создали расширение, имеете некоторый опыт работы с XML-файлами, имеете рабочие знания по настройке групповой политики и знаете, как использовать реестр Windows.</span><span class="sxs-lookup"><span data-stu-id="db702-108">The following steps assume that you’ve already created your extension, have some experience with XML files, have a working knowledge of configuring group policy, and know how to use the Windows registry.</span></span>

## <a name="publish-an-extension"></a><span data-ttu-id="db702-109">Публикация расширения</span><span class="sxs-lookup"><span data-stu-id="db702-109">Publish an extension</span></span>

<span data-ttu-id="db702-110">Перед публикацией расширения его необходимо упаковать в файл CRX (расширение Chrome).</span><span class="sxs-lookup"><span data-stu-id="db702-110">Before you publish an extension it needs to be packed into a CRX (Chrome extension) file.</span></span> <span data-ttu-id="db702-111">В качестве руководства по упаковке расширения в качестве файла CRX используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="db702-111">Use the following steps as a guide to packing an extension as a CRX file.</span></span>

1. <span data-ttu-id="db702-112">В адресной строке Microsoft Edge перейдите в *edge://extensions* и включите **режим разработчика**, если он еще не включен.</span><span class="sxs-lookup"><span data-stu-id="db702-112">In the Microsoft Edge address bar, go to *edge://extensions* and turn on **Developer mode** if it’s not already enabled.</span></span>
2. <span data-ttu-id="db702-113">В разделе **Установленные расширения** щелкните **Расширение пакета**, чтобы создать файл CRX.</span><span class="sxs-lookup"><span data-stu-id="db702-113">Under **Installed extensions**, click **Pack Extension** to create the CRX file.</span></span>
3. <span data-ttu-id="db702-114">Используйте диалоговое окно **Расширение пакета**, чтобы найти каталог с источником расширения.</span><span class="sxs-lookup"><span data-stu-id="db702-114">Use the **Pack extension** dialog to find the directory that has the source for the extension.</span></span> <span data-ttu-id="db702-115">Выберите каталог и нажмите кнопку **Расширение пакета**.</span><span class="sxs-lookup"><span data-stu-id="db702-115">Select the directory and then click **Pack extension**.</span></span>  <span data-ttu-id="db702-116">Это создаст файл CRX вместе с файлом PEM.</span><span class="sxs-lookup"><span data-stu-id="db702-116">This will create your CRX file, along with a PEM file.</span></span> <span data-ttu-id="db702-117">Сохраните файл PEM, так как он необходим для обновления версии до расширения.</span><span class="sxs-lookup"><span data-stu-id="db702-117">Save the PEM file because it’s needed for making version updates to the extension.</span></span> <span data-ttu-id="db702-118">На следующем снимке экрана показано диалоговое окно **Расширение пакета** для размещения корневого каталога расширения.</span><span class="sxs-lookup"><span data-stu-id="db702-118">The next screenshot shows the **Pack extension** dialog for locating the root directory of the extension.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-pack-dialog.png" alt-text="Диалоговое окно расширения пакета для поиска исходного кода расширения.":::

   > [!IMPORTANT]
   > <span data-ttu-id="db702-120">Сохраните файл PEM в безопасном месте, потому что это ключ для расширения и он понадобится для будущих обновлений.</span><span class="sxs-lookup"><span data-stu-id="db702-120">Store the PEM file in a safe location because it’s the key for the extension and it’s needed for future updates.</span></span>

4. <span data-ttu-id="db702-121">Перетащите файл CRX в окно расширений и убедитесь, что он загружается.</span><span class="sxs-lookup"><span data-stu-id="db702-121">Drag the CRX file into your extensions window and make sure that it loads.</span></span>
5. <span data-ttu-id="db702-122">Проверьте расширение и обратите внимание на поле идентификатора (это ИД CRX) и номер версии.</span><span class="sxs-lookup"><span data-stu-id="db702-122">Test the extension and take note of the ID field (this is the CRX ID) and version number.</span></span> <span data-ttu-id="db702-123">Эти сведения потребуются позже.</span><span class="sxs-lookup"><span data-stu-id="db702-123">You’ll need this information later.</span></span> <span data-ttu-id="db702-124">На следующем снимке экрана показано тестовое расширение с его ИД CRX.</span><span class="sxs-lookup"><span data-stu-id="db702-124">The next screenshot shows a test extension with its CRX ID.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-test-extension.png" alt-text="Пример расширения, показывающий ИД CRX":::

6. <span data-ttu-id="db702-126">Загрузите CRX-файл на узел и обратите внимание на URL-адрес расположения, из который он будет скачен.</span><span class="sxs-lookup"><span data-stu-id="db702-126">Upload the the CRX file to the host and note the URL of the location it will be downloaded from.</span></span> <span data-ttu-id="db702-127">Эти сведения необходимы для XML-файла манифеста.</span><span class="sxs-lookup"><span data-stu-id="db702-127">This information is needed for the XML manifest file.</span></span>
7. <span data-ttu-id="db702-128">Чтобы создать XML-файл манифеста с ИД приложения или расширения, URL-адресом загрузки и версией, определите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="db702-128">To create a manifest XML file with the app/extension ID, download URL, and version, define the following fields:</span></span>  

   - <span data-ttu-id="db702-129">**appid** — ИД расширения из шага 5</span><span class="sxs-lookup"><span data-stu-id="db702-129">**appid** - The extension ID from step 5</span></span>
   - <span data-ttu-id="db702-130">**codebase** — расположение загрузки файла CRX из шага 6</span><span class="sxs-lookup"><span data-stu-id="db702-130">**codebase** - The download location for the CRX file from step 6</span></span>
   - <span data-ttu-id="db702-131">**версия** — версия приложения или расширения, которая должна соответствовать версии, указанной в манифесте расширения.</span><span class="sxs-lookup"><span data-stu-id="db702-131">**version** - The version of the app/extension, which should match the version specified in the manifest of the extension.</span></span>

   <span data-ttu-id="db702-132">В следующем фрагменте кода показан пример XML-файла манифеста.</span><span class="sxs-lookup"><span data-stu-id="db702-132">The next code snippet shows an example of an XML manifest file.</span></span>

   ```xml
   <?xml version='1.0' encoding='UTF-8'?> 
   <gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'> 
     <app appid='ekilpdeokbpjmminmhfcgkncmmohmfeb'> 
     <updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.0' /> 
     </app> 
   </gupdate> 
   ```

   <span data-ttu-id="db702-133">Дополнительные сведения см. в статье [Автоматическое обновление расширений в Microsoft Edge — Разработка Microsoft Edge](/microsoft-edge/extensions-chromium/enterprise/auto-update).</span><span class="sxs-lookup"><span data-stu-id="db702-133">For more information, see [Auto-update extensions in Microsoft Edge - Microsoft Edge Development](/microsoft-edge/extensions-chromium/enterprise/auto-update).</span></span>

8. <span data-ttu-id="db702-134">Загрузите завершенный XML-файл в папку, из которой его можно скачать, с помощью URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="db702-134">Upload the completed XML file to a location where it can be downloaded from, noting the URL.</span></span> <span data-ttu-id="db702-135">Этот URL-адрес потребуется при установке расширения с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="db702-135">This URL will be needed when you install the extension using a group policy.</span></span> <span data-ttu-id="db702-136">См. статью [Распространение частного расширения](#distribute-a-privately-hosted-extension).</span><span class="sxs-lookup"><span data-stu-id="db702-136">See [Distribute a privately hosted extension](#distribute-a-privately-hosted-extension).</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="db702-137">Расположение размещения расширения не требует проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="db702-137">The hosting location for the extension doesn’t need authentication.</span></span> <span data-ttu-id="db702-138">Оно должно быть доступно на устройствах пользователей, где бы они ни использовались.</span><span class="sxs-lookup"><span data-stu-id="db702-138">It needs to be accessible by user devices wherever they might be used.</span></span>

## <a name="publish-updates-to-an-extension"></a><span data-ttu-id="db702-139">Публикация обновлений для расширения</span><span class="sxs-lookup"><span data-stu-id="db702-139">Publish updates to an extension</span></span>

<span data-ttu-id="db702-140">После изменения и проверки обновленного расширения его можно опубликовать.</span><span class="sxs-lookup"><span data-stu-id="db702-140">After you change and test the updated extension you can publish it.</span></span> <span data-ttu-id="db702-141">Используйте следующие действия в качестве руководства для публикации обновления.</span><span class="sxs-lookup"><span data-stu-id="db702-141">Use the following steps as a guide for publishing an update.</span></span>

1. <span data-ttu-id="db702-142">Измените номер версии в файле manifest.JSON расширения до более высокого числа с использованием следующего синтаксиса: `"version":"versionString"`.</span><span class="sxs-lookup"><span data-stu-id="db702-142">Change the version number in your extension's manifest.JSON file to a higher number using the following syntax: `"version":"versionString"`.</span></span> <span data-ttu-id="db702-143">Если "версия" — "1.0", то ее можно обновить до "версии" — "1.1" или любого числа выше "1.0".</span><span class="sxs-lookup"><span data-stu-id="db702-143">If the "version":"1.0", then you can update to "version":"1.1" or any number higher than "1.0".</span></span>
2. <span data-ttu-id="db702-144">Обновите "версию" `<updatecheck>` в XML-файле, чтобы она соответствовала номеру, который вы указали в файле манифеста на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="db702-144">Update the "version" of `<updatecheck>` in the XML file to match the number that you put in the manifest file in the previous step.</span></span> <span data-ttu-id="db702-145">Например:</span><span class="sxs-lookup"><span data-stu-id="db702-145">For example:</span></span><br>`<updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.1' />`
3. <span data-ttu-id="db702-146">Создайте файл CRX, который включает новые изменения.</span><span class="sxs-lookup"><span data-stu-id="db702-146">Create a CRX file that includes the new changes.</span></span> <span data-ttu-id="db702-147">Перейдите *edge://extensions* и включите **режим разработчика**.</span><span class="sxs-lookup"><span data-stu-id="db702-147">Go to *edge://extensions* and enable **Developer mode**.</span></span>
4. <span data-ttu-id="db702-148">Щелкните **Расширение пакета** и перейдите в каталог для источника расширения.</span><span class="sxs-lookup"><span data-stu-id="db702-148">Click **Pack extension** and go to the directory for the extension source.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="db702-149">Используйте тот же PEM-файл, который был создан и сохранен при первом создании CRX-файла.</span><span class="sxs-lookup"><span data-stu-id="db702-149">Use the same PEM file that was generated and saved the first time the CRX file was created.</span></span> <span data-ttu-id="db702-150">Если вы не используете тот же файл PEM, идентификатор приложения для расширения изменится, и обновление будет рассматриваться как новое расширение.</span><span class="sxs-lookup"><span data-stu-id="db702-150">If you don't use the same PEM file the app ID of the extension will change and the update will be treated as a new extension.</span></span>

5. <span data-ttu-id="db702-151">Перетащите CRX-файл в окно расширений и убедитесь, что он загружается.</span><span class="sxs-lookup"><span data-stu-id="db702-151">Drag and drop the CRX file into the extensions window and verify that it loads.</span></span>
6. <span data-ttu-id="db702-152">Проверьте обновленное расширение.</span><span class="sxs-lookup"><span data-stu-id="db702-152">Test the updated extension.</span></span>
7. <span data-ttu-id="db702-153">Замените старый CRX-файл и XML-файл новыми файлами для обновленного расширения.</span><span class="sxs-lookup"><span data-stu-id="db702-153">Replace the old CRX file and XML file with the new files for the updated extension.</span></span>

<span data-ttu-id="db702-154">Изменения расширения будут внесены в ходе следующего цикла синхронизации политики.</span><span class="sxs-lookup"><span data-stu-id="db702-154">The extension's changes will be picked up during the next policy sync cycle.</span></span> <span data-ttu-id="db702-155">Дополнительные сведения об обновлении расширений см. в статьях: [Обновить URL-адрес](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) и [Обновить манифест](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).</span><span class="sxs-lookup"><span data-stu-id="db702-155">For more information about updating extensions, see: [Update URL](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) and [Update manifest](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).</span></span>

## <a name="distribute-a-privately-hosted-extension"></a><span data-ttu-id="db702-156">Распространение частного расширения</span><span class="sxs-lookup"><span data-stu-id="db702-156">Distribute a privately hosted extension</span></span>

<span data-ttu-id="db702-157">Вы можете поделиться ссылкой на расположение, в котором находится CRX-файл, и как только пользователи введут URL-адрес в браузере, расширение будет загружено и установлено.</span><span class="sxs-lookup"><span data-stu-id="db702-157">You can share the link of the location where the CRX file is hosted, and as soon as users enter the URL in their browser the extension will be downloaded and installed.</span></span> <span data-ttu-id="db702-158">Пользователи могут включить расширение со страницы edge://extensions.</span><span class="sxs-lookup"><span data-stu-id="db702-158">Users can enable the extension from the edge://extensions page.</span></span> <span data-ttu-id="db702-159">Чтобы разрешить пользователям устанавливать собственные расширения, необходимо добавить идентификаторы CRX расширений в политику [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist).</span><span class="sxs-lookup"><span data-stu-id="db702-159">To allow users to install self-hosted extensions, you need to add the extension CRX IDs to the [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist) policy.</span></span>

<span data-ttu-id="db702-160">Кроме того, можно использовать групповую политику [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) для принудительной установки расширения на устройства пользователей.</span><span class="sxs-lookup"><span data-stu-id="db702-160">Alternatively, you can use group policy [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) to Force-install an extension on your users’ devices.</span></span>

<span data-ttu-id="db702-161">Эти политики можно применить к выбранным пользователям, устройствам или обоим.</span><span class="sxs-lookup"><span data-stu-id="db702-161">You can apply these policies to your selected users, devices, or both.</span></span> <span data-ttu-id="db702-162">Однако помните, что обновления политики не происходят мгновенно, и потребуется время, чтобы параметры политики вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="db702-162">Remember though that policy updates are not instantaneous, and it will take time for the policy settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="db702-163">См. также</span><span class="sxs-lookup"><span data-stu-id="db702-163">See also</span></span>

- [<span data-ttu-id="db702-164">Управление расширениями Microsoft Edge на предприятии</span><span class="sxs-lookup"><span data-stu-id="db702-164">Manage Microsoft Edge extensions in the enterprise</span></span>](microsoft-edge-manage-extensions.md)
- [<span data-ttu-id="db702-165">Использование групповых политик для управления расширениями Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="db702-165">Use group policies to manage Microsoft Edge extensions</span></span>](microsoft-edge-manage-extensions-policies.md)
- [<span data-ttu-id="db702-166">Подробное руководство по политике ExtensionSettings</span><span class="sxs-lookup"><span data-stu-id="db702-166">Detailed guide to the ExtensionSettings policy</span></span>](microsoft-edge-manage-extensions-ref-guide.md)
- [<span data-ttu-id="db702-167">Вопросы и ответы по расширениям Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="db702-167">FAQ for Microsoft Edge Extensions</span></span>](microsoft-edge-manage-extensions-faq.md)
- [<span data-ttu-id="db702-168">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="db702-168">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
