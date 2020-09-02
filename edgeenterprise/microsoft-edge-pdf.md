---
title: Средство чтения PDF в Microsoft Edge
ms.author: adigan
author: dan-wesley
manager: balajek
ms.date: 08/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Узнайте о средстве чтения PDF в Microsoft Edge.
ms.openlocfilehash: c189bc08d4af0c9d5c4d9c573e0b5b7ef32a7fb3
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980983"
---
# <span data-ttu-id="10c14-103">Средство чтения PDF в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="10c14-103">PDF reader in Microsoft Edge</span></span>

<span data-ttu-id="10c14-104">PDF-файлы являются неотъемлемой частью нашей повседневной работы.</span><span class="sxs-lookup"><span data-stu-id="10c14-104">PDF files make up a substantial part of our day-to-day lives.</span></span> <span data-ttu-id="10c14-105">Они встречаются нам в виде контрактов и соглашений, информационных бюллетеней, форм, исследовательских статей, резюме ит.д.</span><span class="sxs-lookup"><span data-stu-id="10c14-105">They come in the form of contracts and agreements, newsletters, forms, research articles, resumes, and so on.</span></span> <span data-ttu-id="10c14-106">Для чтения этих файлов требуется надежное, безопасное и мощное программное средство, которое может использоваться на предприятиях.</span><span class="sxs-lookup"><span data-stu-id="10c14-106">These files highlight the need for a reliable, secure, and powerful PDF reader that can be adopted by Enterprises.</span></span>

<span data-ttu-id="10c14-107">Microsoft Edge содержит встроенное средство чтения PDF-файлов, позволяющее открывать файлы, хранящиеся на локальном устройстве или в сети, а также внедренные в веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="10c14-107">Microsoft Edge comes with a built-in PDF reader that lets you open your local pdf files, online pdf files, or pdf files embedded in web pages.</span></span> <span data-ttu-id="10c14-108">Вы можете добавлять в них заметки с помощью функций выделения и рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="10c14-108">You can annotate these files with ink and highlighting.</span></span> <span data-ttu-id="10c14-109">Данное средство чтения PDF-файлов представляет собой единое приложение, подходящее как для веб-страниц, так и для документов в формате PDF.</span><span class="sxs-lookup"><span data-stu-id="10c14-109">This PDF reader gives users a single application to meet web page and PDF document needs.</span></span> <span data-ttu-id="10c14-110">Средство чтения PDF в Microsoft Edge— это безопасное и надежное приложение, которое работает на компьютерах под управлением Windows и macOS.</span><span class="sxs-lookup"><span data-stu-id="10c14-110">The Microsoft Edge PDF reader is a secure and reliable application that works across the Windows and macOS desktop platforms.</span></span>

> [!NOTE]
> <span data-ttu-id="10c14-111">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="10c14-111">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="10c14-112">Предварительные требования, поддержка и ограничения</span><span class="sxs-lookup"><span data-stu-id="10c14-112">Prerequisites, support, and constraints</span></span>

<span data-ttu-id="10c14-113">В таблице ниже показано, какие каналы и версии Microsoft Edge поддерживают соответствующие функции средства чтения PDF-файлов.</span><span class="sxs-lookup"><span data-stu-id="10c14-113">The following table shows which channels and versions of Microsoft Edge support each PDF reader feature.</span></span>

| <span data-ttu-id="10c14-114">Функция</span><span class="sxs-lookup"><span data-stu-id="10c14-114">Feature</span></span> | <span data-ttu-id="10c14-115">Стабильная версия канала</span><span class="sxs-lookup"><span data-stu-id="10c14-115">Stable channel version</span></span> |
|---------|------------------------|
| <span data-ttu-id="10c14-116">Просмотр и печать локальных, сетевых и внедренных PDF-файлов</span><span class="sxs-lookup"><span data-stu-id="10c14-116">View and print local, online, and embedded PDF files</span></span> | <span data-ttu-id="10c14-117">79.0.309.71</span><span class="sxs-lookup"><span data-stu-id="10c14-117">79.0.309.71</span></span>                |
| <span data-ttu-id="10c14-118">Базовое заполнение форм</span><span class="sxs-lookup"><span data-stu-id="10c14-118">Basic form filling</span></span><br><span data-ttu-id="10c14-119">(формы JavaScript не поддерживаются)</span><span class="sxs-lookup"><span data-stu-id="10c14-119">(JavaScript forms aren't supported)</span></span> | <span data-ttu-id="10c14-120">79.0.309.71</span><span class="sxs-lookup"><span data-stu-id="10c14-120">79.0.309.71</span></span>           |
| <span data-ttu-id="10c14-121">Рукописный ввод</span><span class="sxs-lookup"><span data-stu-id="10c14-121">Inking</span></span>  | <span data-ttu-id="10c14-122">80.0.361.48</span><span class="sxs-lookup"><span data-stu-id="10c14-122">80.0.361.48</span></span>            |
| <span data-ttu-id="10c14-123">Настройка рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="10c14-123">Ink customization</span></span> | <span data-ttu-id="10c14-124">83.0.478.54</span><span class="sxs-lookup"><span data-stu-id="10c14-124">83.0.478.54</span></span>  |
| <span data-ttu-id="10c14-125">Выделить</span><span class="sxs-lookup"><span data-stu-id="10c14-125">Highlight</span></span>  | <span data-ttu-id="10c14-126">81.0.416.53</span><span class="sxs-lookup"><span data-stu-id="10c14-126">81.0.416.53</span></span>         |
| <span data-ttu-id="10c14-127">Чтение вслух</span><span class="sxs-lookup"><span data-stu-id="10c14-127">Read Aloud</span></span> | <span data-ttu-id="10c14-128">В настоящее время продвигается в [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/)</span><span class="sxs-lookup"><span data-stu-id="10c14-128">Currently being promoted in [Microsoft Edge Insider](https://www.microsoftedgeinsider.com/) channels</span></span> |
| <span data-ttu-id="10c14-129">Просмотр файлов с защитой MIP</span><span class="sxs-lookup"><span data-stu-id="10c14-129">View MIP protected files</span></span> | <span data-ttu-id="10c14-130">Поддержка Windows в версии 80.0.361.48</span><span class="sxs-lookup"><span data-stu-id="10c14-130">Windows support in 80.0.361.48</span></span><br><span data-ttu-id="10c14-131">Поддержка Mac в версии 81.0.416.53</span><span class="sxs-lookup"><span data-stu-id="10c14-131">Mac support in 81.0.416.53</span></span> |
|  <span data-ttu-id="10c14-132">Просмотр файлов с защитой IRM</span><span class="sxs-lookup"><span data-stu-id="10c14-132">View IRM protected files</span></span>  | <span data-ttu-id="10c14-133">83.0.478.37</span><span class="sxs-lookup"><span data-stu-id="10c14-133">83.0.478.37</span></span>            |

### <span data-ttu-id="10c14-134">Ограничения</span><span class="sxs-lookup"><span data-stu-id="10c14-134">Constraints</span></span>

<span data-ttu-id="10c14-135">Обратите внимание на перечисленные ниже ограничения для действующего средства чтения PDF-файлов.</span><span class="sxs-lookup"><span data-stu-id="10c14-135">Note the following constraints for the current PDF reader:</span></span>

-  <span data-ttu-id="10c14-136">Архитектура форм XML (XML Forms Architecture, XFA) является устаревшим форматом, который не поддерживается в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="10c14-136">XML Forms Architecture (XFA), is a legacy format of forms that isn't  supported in Microsoft Edge.</span></span>
-  <span data-ttu-id="10c14-137">Документацию по сценариям специальных возможностей, которые на данный момент не поддерживаются, можно найти в блоге [Отчеты о соответствии специальных возможностей Майкрософт](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/).</span><span class="sxs-lookup"><span data-stu-id="10c14-137">Documentation related to Accessibility scenarios that currently aren't supported can be found on the [Microsoft Accessibility Conformance Reports](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/) blog.</span></span>

## <span data-ttu-id="10c14-138">Возможности</span><span class="sxs-lookup"><span data-stu-id="10c14-138">Features</span></span>

### <span data-ttu-id="10c14-139">Рукописный ввод</span><span class="sxs-lookup"><span data-stu-id="10c14-139">Inking</span></span>

<span data-ttu-id="10c14-140">С помощью функции рукописного ввода в PDF-файлах удобно создавать заметки для справки, а также подписывать или заполнять формы в формате PDF.</span><span class="sxs-lookup"><span data-stu-id="10c14-140">Inking on PDF files comes in handy to take quick notes for easy reference, sign, or fill out PDF forms.</span></span> <span data-ttu-id="10c14-141">Теперь эта возможность доступна в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="10c14-141">This capability is now available in Microsoft Edge.</span></span> <span data-ttu-id="10c14-142">Помимо рукописного ввода, вы можете использовать различные цвета и ширину росчерка пера, чтобы привлечь внимание к соответствующим частям PDF-файла.</span><span class="sxs-lookup"><span data-stu-id="10c14-142">In addition to inking PDF files as needed, you can use color and stroke width to bring attention to different parts of the PDF file.</span></span> <span data-ttu-id="10c14-143">На следующем снимке экрана показано, как добавлять рукописные данные на страницу PDF-файла.</span><span class="sxs-lookup"><span data-stu-id="10c14-143">The next screenshot shows how a user can add inking to a pdf page.</span></span>

<!-- SCREENSHOT -->
![Добавление рукописных данных на страницу PDF-файла](media/microsoft-edge-pdf/pdf-reader-inking.png)

### <span data-ttu-id="10c14-145">Выделить</span><span class="sxs-lookup"><span data-stu-id="10c14-145">Highlight</span></span>

<span data-ttu-id="10c14-146">Средство чтения PDF в Microsoft Edge позволяет добавлять и редактировать выделенные фрагменты.</span><span class="sxs-lookup"><span data-stu-id="10c14-146">PDF reader in Microsoft Edge comes with support for adding and editing highlights.</span></span> <span data-ttu-id="10c14-147">Чтобы создать выделенный фрагмент, необходимо просто выделить текст, щелкнуть на нем правой кнопкой мыши, выбрать в меню пункт выделения и указать требуемый цвет.</span><span class="sxs-lookup"><span data-stu-id="10c14-147">To create a highlight, the user simply needs to select the text, right-click on it, select highlights in the menu and choose the desired color.</span></span> <span data-ttu-id="10c14-148">На следующем снимке экрана показаны доступные варианты выделения.</span><span class="sxs-lookup"><span data-stu-id="10c14-148">The next screenshot shows the highlight options that are available.</span></span>

![Использование функции выделения в средстве чтения PDF-файлов](media/microsoft-edge-pdf/pdf-reader-highlight.png)

### <span data-ttu-id="10c14-150">Чтение вслух</span><span class="sxs-lookup"><span data-stu-id="10c14-150">Read Aloud</span></span>

<span data-ttu-id="10c14-151">Функция чтения PDF-файлов вслух позволяет удобно прослушивать их содержимое в ходе выполнения других важных задач.</span><span class="sxs-lookup"><span data-stu-id="10c14-151">Read Aloud for PDF adds the convenience of listening to PDF content while carrying out other tasks that may be important to users.</span></span> <span data-ttu-id="10c14-152">Кроме того, она помогает учащимся сосредоточиться на содержимом файла, что существенно упрощает процесс обучения.</span><span class="sxs-lookup"><span data-stu-id="10c14-152">It also helps auditory learners focus on the content, which makes learning much easier.</span></span> <span data-ttu-id="10c14-153">На следующем снимке экрана показан пример использования функции чтения вслух.</span><span class="sxs-lookup"><span data-stu-id="10c14-153">The next screenshot shows a Read Aloud example.</span></span> <span data-ttu-id="10c14-154">Выделенный фрагмент— это текст, чтение которого выполняется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="10c14-154">The highlighting shows the text that is currently being read.</span></span>

![Использование функции выделения в средстве чтения PDF-файлов](media/microsoft-edge-pdf/pdf-reader-read-aloud-example.png)

### <span data-ttu-id="10c14-156">Защищенные PDF-файлы</span><span class="sxs-lookup"><span data-stu-id="10c14-156">Protected PDFs</span></span>

<span data-ttu-id="10c14-157">Технология защиты [Microsoft Information Protection (MIP)](https://docs.microsoft.com/microsoft-365/compliance/protect-information?view=o365-worldwide) обеспечивает безопасную совместную работу пользователей при соблюдении политик соответствия требованиям, действующих в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="10c14-157">[Microsoft Information Protection (MIP)](https://docs.microsoft.com/microsoft-365/compliance/protect-information?view=o365-worldwide) enables users to collaborate with others securely, while adhering to your organization's compliance policies.</span></span> <span data-ttu-id="10c14-158">Действия, которые пользователи могут выполнять над защищенным файлом, определяются назначенными им правами доступа.</span><span class="sxs-lookup"><span data-stu-id="10c14-158">After a file is protected, the actions users can take on it are determined by the permissions assigned to them.</span></span>

<span data-ttu-id="10c14-159">Файлы можно открывать непосредственно в браузере, не загружая никакого дополнительного программного обеспечения и не устанавливая никаких надстроек.</span><span class="sxs-lookup"><span data-stu-id="10c14-159">These files can be opened directly in the browser, without the need to download any other software, or install any add-in.</span></span> <span data-ttu-id="10c14-160">Таким образом, возможности обеспечения безопасности MIP встраиваются напрямую в браузер с целью оптимизации рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="10c14-160">This integrates the security provided by MIP directly into the browser, providing a seamless workflow.</span></span>

<!-- SCREENSHOT -->
![Защищенный PDF-документ.](media/microsoft-edge-pdf/pdf-reader-protected-pdf2.png)

<span data-ttu-id="10c14-162">Помимо файлов с защитой MIP, непосредственно в браузере также можно открывать PDF-файлы из защищенных библиотек SharePoint с [управлением правами на доступ к данным (IRM)](https://docs.microsoft.com/microsoft-365/compliance/set-up-irm-in-sp-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="10c14-162">In addition to MIP protected files, PDF files in [Information Rights Management (IRM)](https://docs.microsoft.com/microsoft-365/compliance/set-up-irm-in-sp-admin-center?view=o365-worldwide) protected SharePoint libraries can also be opened natively in the browser.</span></span>

<span data-ttu-id="10c14-163">С помощью Microsoft Edge можно просматривать файлы с защитой MIP, хранящиеся на локальном устройстве или в облаке.</span><span class="sxs-lookup"><span data-stu-id="10c14-163">With Microsoft Edge, users can view MIP protected files saved locally, or in the cloud.</span></span> <span data-ttu-id="10c14-164">Если файл сохранен на локальном устройстве, его можно открыть напрямую в браузере.</span><span class="sxs-lookup"><span data-stu-id="10c14-164">If saved locally, the file can be opened directly in the browser.</span></span> <span data-ttu-id="10c14-165">Если файл открывается из облачной службы, например SharePoint, возможно, пользователю потребуется выбрать пункт «Открыть в браузере».</span><span class="sxs-lookup"><span data-stu-id="10c14-165">If the file is opened from a cloud service as SharePoint, the user may need to use the "Open in browser" option.</span></span>

<span data-ttu-id="10c14-166">Если для профиля пользователя, с помощью которого выполнен вход в Microsoft Edge, назначены права доступа хотя бы на просмотр, файл откроется в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="10c14-166">If the profile that the user is logged into Microsoft Edge with has at least view permissions to the file, the file will open in Microsoft Edge.</span></span>

<!-- SCREENSHOT -->
![Запрос на сохранение PDF-страницы SharePoint с защитой MIP](media/microsoft-edge-pdf/pdf-reader-sharepoint-irm.png)

## <span data-ttu-id="10c14-168">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="10c14-168">Accessibility</span></span>

<span data-ttu-id="10c14-169">Средство чтения PDF-файлов поддерживает специальные возможности клавиатуры, режим высокой контрастности и средство чтения с экрана на устройствах под управлением Windows и macOS.</span><span class="sxs-lookup"><span data-stu-id="10c14-169">The PDF reader comes with support for Keyboard accessibility, High contrast mode, and screen reader support across Windows and macOS devices.</span></span>

### <span data-ttu-id="10c14-170">Специальные возможности клавиатуры</span><span class="sxs-lookup"><span data-stu-id="10c14-170">Keyboard Accessibility</span></span>

<span data-ttu-id="10c14-171">Эта функция позволяет с помощью клавиатуры переходить к различным частям документа, с которыми можно взаимодействовать, например к полям формы и выделенным фрагментам.</span><span class="sxs-lookup"><span data-stu-id="10c14-171">Users can use navigate to different parts of the document that a user can interact with, such as form fields and highlights, using the keyboard.</span></span>

<!-- SCREENSHOT -->

### <span data-ttu-id="10c14-172">Режим высокой контрастности</span><span class="sxs-lookup"><span data-stu-id="10c14-172">High contrast mode</span></span>

<span data-ttu-id="10c14-173">Для отображения контента в режиме высокой контрастности в средстве чтения PDF-файлов используются настройки, заданные на уровне операционной системы.</span><span class="sxs-lookup"><span data-stu-id="10c14-173">PDF reader will use the settings defined at the operating system level to render PDF content in high contrast mode.</span></span>

<!-- SCREENSHOT -->
<!--![High contrast mode for pdf file](media/microsoft-edge-pdf/pdf-reader-high-contrast.png)-->

### <span data-ttu-id="10c14-174">Поддержка средства чтения с экрана</span><span class="sxs-lookup"><span data-stu-id="10c14-174">Screen reader support</span></span>

<span data-ttu-id="10c14-175">Пользователи могут перемещаться по PDF-файлам и читать их с помощью средств чтения с экрана на компьютерах Windows и Mac.</span><span class="sxs-lookup"><span data-stu-id="10c14-175">Users can navigate through and read PDF files using screen readers on Windows and Mac computers.</span></span> <!--The next screenshot shows the toolbar that users can use for audio settings when they're using the Read Aloud option in PDF reader. -->

<!-- SCREENSHOT -->
<!--
![Screen reader toolbar](media/microsoft-edge-pdf/pdf-reader-read-aloud.png) -->

## <span data-ttu-id="10c14-176">Безопасность и надежность</span><span class="sxs-lookup"><span data-stu-id="10c14-176">Security and reliability</span></span>

<span data-ttu-id="10c14-177">Безопасность является одним из важнейших принципов для любой организации.</span><span class="sxs-lookup"><span data-stu-id="10c14-177">Security is among the most important tenets for any organization.</span></span> <span data-ttu-id="10c14-178">Безопасность средства чтения PDF-файлов— неотъемлемая часть системы безопасности Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="10c14-178">PDF reader security is an integral part of the Microsoft Edge security design.</span></span> <span data-ttu-id="10c14-179">Две важнейшие функции обеспечения безопасности. Применительно к средству чтения PDF-файлов важнейшими функциями обеспечения безопасности являются изоляция процессов и Application Guard в Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="10c14-179">Two of the most important security features From a PDF reader perspective, two important security features are process isolation and Microsoft Defender Application Guard (Application Guard).</span></span>

- <span data-ttu-id="10c14-180">Изоляция процессов.</span><span class="sxs-lookup"><span data-stu-id="10c14-180">Process isolation.</span></span> <span data-ttu-id="10c14-181">PDF-файлы, открытые с разных веб-сайтов, полностью изолированы с точки зрения процессов.</span><span class="sxs-lookup"><span data-stu-id="10c14-181">PDFs opened from different web sites are completely process isolated.</span></span> <span data-ttu-id="10c14-182">Браузеру не нужно взаимодействовать ни с какими веб-сайтами или PDF-файлами, открытыми из другого источника.</span><span class="sxs-lookup"><span data-stu-id="10c14-182">The browser doesn't have to communicate with any websites, or PDF files opened from another source.</span></span> <span data-ttu-id="10c14-183">При просмотре файлов обеспечивается защита от любых действий злоумышленников, планирующих использовать в качестве направления атак взломанные PDF-файлы.</span><span class="sxs-lookup"><span data-stu-id="10c14-183">PDF browsing is secure from any attacks that plan to use compromised PDFs as an attack surface.</span></span>

- <span data-ttu-id="10c14-184">Application Guard.</span><span class="sxs-lookup"><span data-stu-id="10c14-184">Application Guard.</span></span> <span data-ttu-id="10c14-185">С помощью Application Guard администраторы могут задать список сайтов, которым доверяет их организация.</span><span class="sxs-lookup"><span data-stu-id="10c14-185">With Application Guard, admins can set a list of sites that are trusted by their organization.</span></span> <span data-ttu-id="10c14-186">При открытии пользователем любого другого сайта он откроется в отдельном окне Application Guard, которое запускается в собственном контейнере.</span><span class="sxs-lookup"><span data-stu-id="10c14-186">If users open any other sites, they are opened in a separate Application Guard window that runs in its own container.</span></span> <span data-ttu-id="10c14-187">Контейнер помогает защитить от несанкционированного доступа корпоративную сеть и любые данные на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="10c14-187">The container helps protect the corporate network and any data on user's computer from being compromised.</span></span><br><br>
<span data-ttu-id="10c14-188">Эта защита также распространяется на все PDF-файлы, просматриваемые в сети.</span><span class="sxs-lookup"><span data-stu-id="10c14-188">This protection also applies to any online PDF files that are viewed.</span></span> <span data-ttu-id="10c14-189">Кроме того, все PDF-файлы, загруженные из окна Application Guard, сохраняются и при необходимости повторно открываются в контейнере.</span><span class="sxs-lookup"><span data-stu-id="10c14-189">Further, any PDF files that are downloaded from an Application Guard window are stored, and when needed, re-opened in the container.</span></span> <span data-ttu-id="10c14-190">Это помогает обеспечить безопасность вашей среды не только при загрузке файла, но и в течение всего его жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="10c14-190">This helps keeps your environment secure not just when the file is downloaded, but through its whole lifecycle.</span></span> <span data-ttu-id="10c14-191">Дополнительные сведения см. в разделе [Application Guard](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard).</span><span class="sxs-lookup"><span data-stu-id="10c14-191">For more information, see [Application Guard](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard).</span></span>

### <span data-ttu-id="10c14-192">надежность;</span><span class="sxs-lookup"><span data-stu-id="10c14-192">Reliability</span></span>

<span data-ttu-id="10c14-193">Поскольку браузер Microsoft Edge создан на основе Chromium, пользователи могут ожидать от него такого же уровня надежности, что и в Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="10c14-193">Because Microsoft Edge is Chromium-based, users can expect the same level of reliability that they're used to seeing in Google Chrome.</span></span>

## <span data-ttu-id="10c14-194">Развертывание и обновление средства чтения PDF-файлов</span><span class="sxs-lookup"><span data-stu-id="10c14-194">Deploy and update PDF reader</span></span>

<span data-ttu-id="10c14-195">Средство чтения PDF-файлов развертывается и обновляется вместе с остальными компонентами браузера Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="10c14-195">The PDF reader gets deployed and updated with the rest of the Microsoft Edge browser.</span></span> <span data-ttu-id="10c14-196">Дополнительные сведения о развертывании Microsoft Edge см. в видео [Развертывание Microsoft Edge на сотнях или тысячах устройств](microsoft-edge-video-deploy.md).</span><span class="sxs-lookup"><span data-stu-id="10c14-196">To learn more about deploying Microsoft Edge, watch the [Deploy Microsoft Edge to hundreds or thousands of devices](microsoft-edge-video-deploy.md) video.</span></span> <span data-ttu-id="10c14-197">Вы также можете найти дополнительную информацию о развертывании на главной странице [документации по Microsoft Edge](https://docs.microsoft.com/DeployEdge/).</span><span class="sxs-lookup"><span data-stu-id="10c14-197">You can also find more deployment information on the [Microsoft Edge documentation](https://docs.microsoft.com/DeployEdge/) landing page.</span></span>

> [!TIP]
> <span data-ttu-id="10c14-198">Вы можете сделать Microsoft Edge средством чтения PDF-файлов по умолчанию для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="10c14-198">You can make Microsoft Edge the default PDF reader for your organization.</span></span> <span data-ttu-id="10c14-199">Для этого [выполните описанные здесь действия](https://docs.microsoft.com/deployedge/edge-default-browser).</span><span class="sxs-lookup"><span data-stu-id="10c14-199">To do this, [follow these steps](https://docs.microsoft.com/deployedge/edge-default-browser).</span></span>

## <span data-ttu-id="10c14-200">Стратегия развития и отзывы</span><span class="sxs-lookup"><span data-stu-id="10c14-200">Roadmap and feedback</span></span>

<span data-ttu-id="10c14-201">Стратегия развития средства чтения PDF в Microsoft Edge описана [здесь](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667).</span><span class="sxs-lookup"><span data-stu-id="10c14-201">The roadmap for PDF Reader in Microsoft Edge is available [here](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667).</span></span>

<span data-ttu-id="10c14-202">Мы внимательно изучаем ваши отзывы о функциях, которые вы считаете важными.</span><span class="sxs-lookup"><span data-stu-id="10c14-202">We're actively looking at feedback from you about the features you find important.</span></span> <span data-ttu-id="10c14-203">Для отправки нам отзывов можно использовать [Microsoft Edge UserVoice](https://microsoftedge.uservoice.com/) и форум [Microsoft Edge Insider](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider).</span><span class="sxs-lookup"><span data-stu-id="10c14-203">Feel free to send us feedback through [Microsoft Edge UserVoice](https://microsoftedge.uservoice.com/) and on [Microsoft Edge Insider](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider) forum.</span></span>

## <span data-ttu-id="10c14-204">См. также</span><span class="sxs-lookup"><span data-stu-id="10c14-204">See also</span></span>

- [<span data-ttu-id="10c14-205">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="10c14-205">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)