---
title: Функции ClickOnce и DirectInvoke в Microsoft Edge
ms.author: kele
author: dan-wesley
manager: srugh
ms.date: 04/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Сведения о функциях ClickOnce и DirectInvoke в Microsoft Edge.
ms.openlocfilehash: 8290c34bd29ca72678e3fa68f74b689d0cf797e3
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980915"
---
# <span data-ttu-id="c3fb7-103">Общие сведения о функциях ClickOnce и DirectInvoke в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c3fb7-103">Understand the ClickOnce and DirectInvoke features in Microsoft Edge</span></span>

<span data-ttu-id="c3fb7-104">ClickOnce и DirectInvoke — это функции, доступные в IE и Microsoft Edge (версии 45 и более ранних версий), которые поддерживают использование обработчика файлов для скачивания файлов с веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-104">ClickOnce and DirectInvoke are features available in IE and Microsoft Edge (version 45 and earlier) that support the use of a file handler to download files from a website.</span></span> <span data-ttu-id="c3fb7-105">Несмотря на то что у этих функций разное назначение, они позволяют указывать веб-сайтам, что запрошенный для скачивания файл, передается в обработчик файлов на устройстве пользователя.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-105">Although they serve different purposes, both features let websites specify that a file requested for download is passed to a file handler on the user's device.</span></span> <span data-ttu-id="c3fb7-106">Запросы ClickOnce обрабатываются с помощью собственного обработчика файлов в Windows.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-106">ClickOnce requests are handled by the native file handler in Windows.</span></span> <span data-ttu-id="c3fb7-107">Запросы DirectInvoke обрабатываются зарегистрированным обработчиком файлов, заданным веб-сайтом, на котором размещен файл.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-107">DirectInvoke requests are handled by a registered file handler specified by the website hosting the file.</span></span>

<span data-ttu-id="c3fb7-108">Дополнительные сведения об этих функциях см. в следующих статьях.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-108">For more information about these features, see:</span></span>

- [<span data-ttu-id="c3fb7-109">ClickOnce</span><span class="sxs-lookup"><span data-stu-id="c3fb7-109">ClickOnce</span></span>](https://docs.microsoft.com/visualstudio/deployment/clickonce-security-and-deployment?view=vs-2019)
- [<span data-ttu-id="c3fb7-110">DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="c3fb7-110">DirectInvoke</span></span>]( https://technet.microsoft.com/learning/jj215788(v=vs.94).aspx)

> [!NOTE]
> <span data-ttu-id="c3fb7-111">В данный момент в Chromium не реализована встроенная поддержка функций ClickOnce или DirectInvoke.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-111">Currently, Chromium doesn't provide native support for ClickOnce or DirectInvoke.</span></span>

## <span data-ttu-id="c3fb7-112">Обзор: необходимые условия и процессы</span><span class="sxs-lookup"><span data-stu-id="c3fb7-112">Overview: prerequisites and process</span></span>

<span data-ttu-id="c3fb7-113">Чтобы функции ClickOnce и DirectInvoke работали правильно и обработчик файлов успешно запрашивался, обработчик файлов должен быть зарегистрирован в операционной системе в качестве поддерживающего функции ClickOnce или DirectInvoke.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-113">For ClickOnce and DirectInvoke to work as designed and for the file handler to be successfully requested, the file handler must be registered to the operating system as supporting ClickOnce or DirectInvoke.</span></span> <span data-ttu-id="c3fb7-114">Обычно такая регистрация происходит, когда устанавливается исходная операционная система или когда новая устанавливаемая программа запрашивает возможность использования функции DirectInvoke для обновлений.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-114">This registration typically happens when the original operating system is installed or when a new program that's installed requests the ability to use DirectInvoke for updates.</span></span>

<span data-ttu-id="c3fb7-115">Когда веб-сайт получает запрос на скачивание, требующий наличия функций ClickOnce или DirectInvoke, выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-115">When a website receives a download request that requires ClickOnce or DirectInvoke, the following actions happen:</span></span>

- <span data-ttu-id="c3fb7-116">Веб-сайт запрашивает, чтобы браузер использовал указанный обработчик файлов.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-116">The website requests that the browser use a specified file handler.</span></span>
- <span data-ttu-id="c3fb7-117">Браузер проверяет реестр операционной системы, чтобы узнать, зарегистрирован ли обработчик файлов для запрошенного типа файла.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-117">The browser checks the operating system registry to see if the file handler is registered for the requested file type.</span></span>
- <span data-ttu-id="c3fb7-118">Если обработчик файлов зарегистрирован, браузер вызывает обработчик файлов и передает URL-адрес в качестве аргумента обработчику файлов.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-118">If the file handler is registered, the browser calls the file handler and passes the URL as an argument to the file handler.</span></span>
- <span data-ttu-id="c3fb7-119">Обработчик файлов обрабатывает URL-адрес и загружает файл.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-119">The file handler processes the URL and downloads the file.</span></span>

  > [!NOTE]
  > <span data-ttu-id="c3fb7-120">Этот URL-адрес используется для определения источника файла, а также всех параметров доступа к файлу.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-120">The URL is used to determine the source of the file, as well as any parameters to use when accessing the file.</span></span>  <span data-ttu-id="c3fb7-121">Например: конечные точки, манифест или метаданные.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-121">For example: endpoints, a manifest, or metadata.</span></span>

## <span data-ttu-id="c3fb7-122">Варианты использования</span><span class="sxs-lookup"><span data-stu-id="c3fb7-122">Use cases</span></span>

<span data-ttu-id="c3fb7-123">Следующие варианты использования являются примерами.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-123">The following use cases are representative.</span></span>

<span data-ttu-id="c3fb7-124">С помощью ClickOnce можно легко развертывать и обновлять программное обеспечение на устройствах при минимальном участии со стороны пользователя.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-124">You can use ClickOnce to easily deploy and update software on devices with minimal user interaction.</span></span> <span data-ttu-id="c3fb7-125">Пользователи могут установить и запустить Windows-приложение, щелкнув ссылку на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-125">Users can install and run a Windows application by clicking a link in a web page.</span></span> <span data-ttu-id="c3fb7-126">Если функция настроена правильно, приложение ClickOnce может устанавливать программы без необходимости в задании конфигураций для установщика пользователями.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-126">If configured correctly, the ClickOnce application can install programs without having users set configurations for the installer.</span></span> <span data-ttu-id="c3fb7-127">Например, расположения файлов, параметры установки и т. д.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-127">For example, file locations, what options to install, and so on.</span></span>

<span data-ttu-id="c3fb7-128">Варианты использования DirectInvoke зависят от того, зачем веб-сайт запрашивает DirectInvoke.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-128">DirectInvoke use cases depend on the intent of the website requesting DirectInvoke.</span></span> <span data-ttu-id="c3fb7-129">Например, для использования функции совместного редактирования файлов Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-129">For example, the collaborative file-editing feature of Microsoft Word.</span></span> <span data-ttu-id="c3fb7-130">Вместо перехода по ссылке и скачивания всей копии документа, над которым вы работаете с коллегами, функция DirectInvoke позволяет скачивать части документа, которые были изменены.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-130">Instead of clicking a link and downloading the entire copy of a document you're working on with your colleagues, DirectInvoke lets you download the parts of the document that have been changed.</span></span> <span data-ttu-id="c3fb7-131">Эта стратегия уменьшает объем передаваемых данных и помогает сократить время, необходимое для открытия документа.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-131">This strategy reduces the amount of data transferred and can reduce the time needed to open the document.</span></span>  

## <span data-ttu-id="c3fb7-132">Текущая поддержка функций ClickOnce и DirectInvoke в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c3fb7-132">Current support for ClickOnce and DirectInvoke in Microsoft Edge</span></span>

<span data-ttu-id="c3fb7-133">Поддержка ClickOnce и DirectInvoke:</span><span class="sxs-lookup"><span data-stu-id="c3fb7-133">Support for ClickOnce and DirectInvoke:</span></span>

- <span data-ttu-id="c3fb7-134">Функция DirectInvoke по умолчанию доступна всем пользователям Windows, однако функция ClickOnce отключена для всех пользователей Windows.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-134">DirectInvoke is supported out of the box for all Windows users but ClickOnce is disabled for all Windows users.</span></span>

  > [!NOTE]
  > <span data-ttu-id="c3fb7-135">Пользователи, которым требуется поддержка ClickOnce, могут перейти на страницу edge://flags/#edge-click-once и выбрать **Включить** в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-135">Users that need ClickOnce support can go to edge://flags/#edge-click-once and select **Enable** from the dropdown list.</span></span> <span data-ttu-id="c3fb7-136">После этого будет необходимо **Перезапустить**браузер.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-136">You'll have to **Restart** the browser.</span></span>

- <span data-ttu-id="c3fb7-137">Функции ClickOnce и DirectInvoke не поддерживаются на платформах, отличных от Windows.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-137">ClickOnce and DirectInvoke aren't supported on any platforms other than Windows.</span></span>
- <span data-ttu-id="c3fb7-138">Так как функция ClickOnce является ориентированной на предприятие функцией, которую использует определенная группа опытных пользователей, и не предназначена для общего использования, она по умолчанию отключена.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-138">Because ClickOnce is an enterprise-focused feature that's used by a specific group of power users and not intended for general use, ClickOnce is disabled by default.</span></span>

## <span data-ttu-id="c3fb7-139">Безопасность обработки файлов в ClickOnce и DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="c3fb7-139">ClickOnce and DirectInvoke file handling security</span></span>

<span data-ttu-id="c3fb7-140">Функции ClickOnce и DirectInvoke защищены службой проверки репутации фильтра SmartScreen в Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-140">ClickOnce and DirectInvoke are protected by Microsoft Defender SmartScreen's URL reputation scanning service.</span></span>

<span data-ttu-id="c3fb7-141">Если запрос ClickOnce или DirectInvoke помечен службой проверки репутации URL-адресов фильтра SmartScreen в Microsoft Defender как небезопасный, для пользователей с включенными функциями ClickOnce или DirectInvoke будут отображаться два всплывающих окна.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-141">If a ClickOnce or a DirectInvoke request is flagged by the Microsoft Defender SmartScreen URL reputation service as unsafe, users with ClickOnce or DirectInvoke enabled will see two popups.</span></span>

<span data-ttu-id="c3fb7-142">Первое всплывающее окно спрашивает у пользователя, хочет ли он открыть файл.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-142">The first popup asks the user if they want to open the file.</span></span> <span data-ttu-id="c3fb7-143">Это всплывающее окно отображается независимо от того, был ли файл помечен как безопасный или небезопасный.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-143">This popup is displayed regardless of whether the file was flagged as safe or unsafe.</span></span> <span data-ttu-id="c3fb7-144">Пользователь может **Сообщить, что файл небезопасен**, **Отменить** запрос или нажать **Открыть**, чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-144">The user can **Report the file as unsafe**, **Cancel** the request, or click **Open** to continue.</span></span>

   ![Запрос на открытие файла](./media/edge-learn-more-co-di/edge-clickonce-modal-1.png)

<span data-ttu-id="c3fb7-146">Если пользователь пытается открыть файл, который был помечен как небезопасный, отображается второе всплывающее окно.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-146">If the user tries to open the file, and the file was flagged as unsafe, a second popup is displayed.</span></span>  <span data-ttu-id="c3fb7-147">Это всплывающее окно предупреждает пользователя о том, что файл был помечен как небезопасный, и запрашивает подтверждение на скачивание файла.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-147">This popup warns the user that the file was flagged as unsafe, and asks them if they're sure they want to download the file.</span></span>

<span data-ttu-id="c3fb7-148">Второе всплывающее окно отображается только в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="c3fb7-148">The second popup only shows up if:</span></span>

- <span data-ttu-id="c3fb7-149">Файл является файлом ClickOnce или DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="c3fb7-149">the file is a ClickOnce or DirectInvoke file</span></span>
- <span data-ttu-id="c3fb7-150">Функции ClickOnce или DirectInvoke включены</span><span class="sxs-lookup"><span data-stu-id="c3fb7-150">ClickOnce or DirectInvoke are enabled</span></span>
- <span data-ttu-id="c3fb7-151">Файл помечен как небезопасный</span><span class="sxs-lookup"><span data-stu-id="c3fb7-151">the file is flagged as unsafe</span></span>

 ![Запрос на открытие небезопасного файла](./media/edge-learn-more-co-di/edge-clickonce-modal-2.png)

> [!NOTE]
> <span data-ttu-id="c3fb7-153">Если функции ClickOnce или DirectInvoke отключены, запрашиваемые файлы обрабатываются как обычные загрузки, и если они будут помечены как небезопасные, то эта отметка останется.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-153">If ClickOnce or DirectInvoke are disabled, requested files are treated as regular downloads and if flagged as unsafe, will be marked as unsafe.</span></span> <span data-ttu-id="c3fb7-154">Аналогичным образом обрабатываются другие небезопасные загрузки.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-154">This is consistent with the treatment of other unsafe downloads.</span></span>

## <span data-ttu-id="c3fb7-155">Политики ClickOnce и DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="c3fb7-155">ClickOnce and DirectInvoke policies</span></span>

<span data-ttu-id="c3fb7-156">Существует две групповых политики, которые можно использовать для включения и отключения функций ClickOnce и DirectInvoke для корпоративных пользователей.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-156">There are two group policies that you can use to enable or disable ClickOnce and DirectInvoke for enterprise users.</span></span> <span data-ttu-id="c3fb7-157">Этими политиками являются [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled) и [DirectInvokeEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#directinvokeenabled).</span><span class="sxs-lookup"><span data-stu-id="c3fb7-157">These two policies are [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled) and [DirectInvokeEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#directinvokeenabled).</span></span> <span data-ttu-id="c3fb7-158">Эти две политики в редакторе групповой политики называются "Разрешить пользователям открывать файлы с использованием протокола ClickOnce" и "Разрешить пользователям открывать файлы с использованием протокола DirectInvoke" соответственно.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-158">These two policies are labeled in the Group Policy Editor as "Allow users to open files using the ClickOnce protocol" and "Allow users to open files using the DirectInvoke protocol" respectively.</span></span>

## <span data-ttu-id="c3fb7-159">Поведение ClickOnce и DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="c3fb7-159">ClickOnce and DirectInvoke behavior</span></span>

<span data-ttu-id="c3fb7-160">В следующих примерах представлен процесс обработки файлов, когда функции ClickOnce и DirectInvoke включены и отключены.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-160">The following examples show file handling when ClickOnce and DirectInvoke are enabled or disabled.</span></span>

### <span data-ttu-id="c3fb7-161">Функция ClickOnce включена</span><span class="sxs-lookup"><span data-stu-id="c3fb7-161">ClickOnce enabled</span></span>

1. <span data-ttu-id="c3fb7-162">Пользователь открывает ссылку на страницу, которая запрашивает поддержку ClickOnce, и видит запрос, представленный на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-162">A user opens a link to a page that requests ClickOnce support and gets the prompt in the next screenshot.</span></span>

   ![Запрос на открытие небезопасного файла](./media/edge-learn-more-co-di/edge-clickonce-enabled-1.png)

2. <span data-ttu-id="c3fb7-164">После нажатия **Открыть** функция ClickOnce попытается запустить приложение.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-164">After the user clicks **Open**, ClickOnce attempts to launch the application.</span></span>

   ![Функция ClickOnce пытается запустить приложение](./media/edge-learn-more-co-di/edge-clickonce-enabled-launch-app.png)

3. <span data-ttu-id="c3fb7-166">После нажатия кнопки **Открыть** в браузере отобразится всплывающее окно, в котором пользователю будет предложено установить приложение.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-166">After the user clicks **Open**, the browser shows a popup that asks the user if they're sure they want to install the application.</span></span>

   ![Запрос на открытие файла](./media/edge-learn-more-co-di/edge-clickonce-enabled-2.png)

   > [!NOTE]
   > <span data-ttu-id="c3fb7-168">Интерфейс, сообщения и параметры, отображаемые обработчиком файлов ClickOnce, зависят от типа и конфигурации файла, к которому осуществляется доступ.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-168">The interface, messaging, and options shown by the ClickOnce file handler will vary depending on the type and configuration of the file that's accessed.</span></span>

### <span data-ttu-id="c3fb7-169">Функция ClickOnce отключена</span><span class="sxs-lookup"><span data-stu-id="c3fb7-169">ClickOnce disabled</span></span>

1. <span data-ttu-id="c3fb7-170">Когда пользователь открывает ссылку на страницу, которая запрашивает поддержку ClickOnce, он видит в панели загрузки сообщение, похожее на сообщение, представленное на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-170">When a user opens a link to a page that requests ClickOnce support, they will see a message in the download tray that is similar to the one in the next screenshot.</span></span>

   ![Запрос на загрузку файла](./media/edge-learn-more-co-di/edge-clickonce-disabled-1.png)

### <span data-ttu-id="c3fb7-172">Функция DirectInvoke включена</span><span class="sxs-lookup"><span data-stu-id="c3fb7-172">DirectInvoke enabled</span></span>

1. <span data-ttu-id="c3fb7-173">Пользователь открывает ссылку на страницу, которая запрашивает поддержку DirectInvoke, и видит запрос, представленный на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-173">A user opens a link to a page that requests DirectInvoke support and gets the prompt in the next screenshot.</span></span>

   ![Запрос на открытие файла](./media/edge-learn-more-co-di/edge-directinvoke-open-link-1.png)

2. <span data-ttu-id="c3fb7-175">Когда пользователь нажимает кнопку **Открыть**, открывается запрошенный обработчик файлов.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-175">When the user clicks **Open**, the requested file handler is opened.</span></span> <span data-ttu-id="c3fb7-176">В этом примере для открытия документа, показанного на предыдущем снимке экрана, используется Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-176">In this example, Microsoft Word is used to open the document that's shown in the previous screenshot.</span></span>

   > [!NOTE]
   > <span data-ttu-id="c3fb7-177">Интерфейс, сообщения и параметры, отображаемые обработчиком файлов DirectInvoke, зависят от типа и конфигурации файла, к которому осуществляется доступ.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-177">The interface, messaging, and options shown by the DirectInvoke file handler will vary depending on the type and configuration of the file that's accessed.</span></span>

### <span data-ttu-id="c3fb7-178">Функция DirectInvoke отключена</span><span class="sxs-lookup"><span data-stu-id="c3fb7-178">DirectInvoke disabled</span></span>

1. <span data-ttu-id="c3fb7-179">Когда пользователь открывает ссылку на страницу, которая запрашивает поддержку DirectInvoke, функция DirectInvoke работает так же, как при отключенной функции ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-179">When a user opens a link to a page that requests DirectInvoke support, DirectInvoke behaves the same as when ClickOnce is disabled.</span></span> <span data-ttu-id="c3fb7-180">Пользователь видит сообщение в панели загрузки, похожее на сообщение, представленное на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-180">They will see a message in the download tray that's similar to the one in the next screenshot.</span></span>

   ![Запрос на открытие файла](./media/edge-learn-more-co-di/edge-directinvoke-open-link-2.png)

## <span data-ttu-id="c3fb7-182">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c3fb7-182">See also</span></span>

- [<span data-ttu-id="c3fb7-183">Безопасность и развертывание ClickOnce</span><span class="sxs-lookup"><span data-stu-id="c3fb7-183">ClickOnce security and deployment</span></span>](https://go.microsoft.com/fwlink/?linkid=2099880)
- [<span data-ttu-id="c3fb7-184">Функция DirectInvoke в Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="c3fb7-184">DirectInvoke in Internet Explorer</span></span>](https://go.microsoft.com/fwlink/?linkid=2099871)
- [<span data-ttu-id="c3fb7-185">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="c3fb7-185">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
