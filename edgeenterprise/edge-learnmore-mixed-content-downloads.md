---
title: Microsoft Edge и скачивание смешанного содержимого
ms.author: kele
author: dan-wesley
manager: srugh
ms.date: 04/30/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge и скачивание смешанного содержимого
ms.openlocfilehash: 57da17a8684b97aad88e7837ff9d070f6862357b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980901"
---
# <span data-ttu-id="6cf7e-103">Сведения о Microsoft Edge и скачивании смешанного содержимого</span><span class="sxs-lookup"><span data-stu-id="6cf7e-103">Learn about Microsoft Edge and mixed content downloads</span></span>

<span data-ttu-id="6cf7e-104">В этой статье описаны скачивания смешанного содержимого и их обработка в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-104">This article explains mixed content downloads and how Microsoft Edge handles them.</span></span>

>[!NOTE]
><span data-ttu-id="6cf7e-105">Эта статья относится к Microsoft Edge версии 85 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-105">This article applies to Microsoft Edge version 85 or later.</span></span>

## <span data-ttu-id="6cf7e-106">Что такое скачивание смешанного содержимого?</span><span class="sxs-lookup"><span data-stu-id="6cf7e-106">What are mixed content downloads?</span></span>

<span data-ttu-id="6cf7e-107">Скачивание смешанного содержимого выполняется при запуске скачивания с HTML-страницы, загруженной по защищенному соединению HTTPS, при наличии одного из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="6cf7e-107">A mixed content download happens when you start a download from an HTML page that was loaded over a secure HTTPS connection, but one of the following conditions exists:</span></span>

- <span data-ttu-id="6cf7e-108">Одно или несколько перенаправлений расположения скачивания были загружены по незащищенному соединению HTTP.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-108">One or more of the download location's redirects was loaded over an insecure HTTP connection.</span></span>
- <span data-ttu-id="6cf7e-109">Окончательное расположение скачивания было загружено по незащищенному соединению HTTP.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-109">The final download location was loaded over an insecure HTTP connection.</span></span>

<span data-ttu-id="6cf7e-110">Оба сценария относятся к смешанному содержимому, так как запрос был выполнен с использованием защищенного HTTPS-соединения, а в достижении конечного назначения скачивания использовалось как HTTP, так и HTTPS содержимое.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-110">Either scenario is a mixed content because the request was made using secure HTTPS and both HTTP and HTTPS content are involved in reaching the final download destination.</span></span> <span data-ttu-id="6cf7e-111">Современные браузеры выводят предупреждения об этом типе содержимого, чтобы указать пользователю, что это скачивание может передаваться незащищенным образом, даже если исходная страница была защищенной.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-111">Modern browsers display warnings about this type of content to indicate to the user that this download may be transferred insecurely even though the original page accessed was secure.</span></span>

## <span data-ttu-id="6cf7e-112">Предупреждения при скачивании и пользовательские параметры</span><span class="sxs-lookup"><span data-stu-id="6cf7e-112">Download warnings and user options</span></span>

<span data-ttu-id="6cf7e-113">Предупреждение при скачивании гарантирует, что пользователи знают о том, что скачиваемый файл может быть прочитан злоумышленниками в их сети.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-113">The download warning ensures that users know that the file they're downloading could be read by malicious attackers on their network.</span></span> <span data-ttu-id="6cf7e-114">Это предупреждение позволяет пользователю принять обоснованное решение о том, следует ли скачивать файл.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-114">This warning lets a user make an informed decision on whether to download the file.</span></span>

<span data-ttu-id="6cf7e-115">В Microsoft Edge скачивание смешанного содержимого блокируется, но пользователи могут переопределить это поведение и скачать файл, если захотят.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-115">In Microsoft Edge, mixed content downloads will be blocked but users can override and download the file if they want to.</span></span> <span data-ttu-id="6cf7e-116">В Microsoft Edge планируется начать блокировать скачивание исполняемых файлов смешанного содержимого, начиная с Microsoft Edge версии 85, а в будущих выпусках будут блокироваться различные типы файлов.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-116">Microsoft Edge plans on starting to block mixed content executable file downloads starting with Microsoft Edge version 85 and will block different filetypes in future releases.</span></span>

> [!NOTE]
> <span data-ttu-id="6cf7e-117">Развертывание этой функции может быть изменено на основе расписания выпусков и отзывов пользователей.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-117">Deployment of this feature is subject to change based on release schedule and user feedback.</span></span>

<!-- The schedule of the block for different filetypes is to be determined and may be impacted by usage data and user feedback. -->

<span data-ttu-id="6cf7e-118">В области загрузки предупреждение о блокировании выглядит, как пример на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-118">In the download shelf, the block warning message looks like the example in the next screenshot.</span></span>

 ![Предупреждение о смешанном содержимом в области загрузки](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-tray-warning.png)

<span data-ttu-id="6cf7e-120">На странице загрузок предупреждение о блокировании выглядит, как следующий пример снимка экрана:</span><span class="sxs-lookup"><span data-stu-id="6cf7e-120">On the download page, the block warning looks like the following screenshot example:</span></span>

 ![Запрос на переопределение для смешанного содержимого](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-page-warning.png)

<span data-ttu-id="6cf7e-122">Если пользователь решит продолжить скачивание, ему будет предложено подтвердить свое действие.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-122">If a user decides to keep the download, they are prompted to confirm their action.</span></span> <span data-ttu-id="6cf7e-123">На следующем снимке экрана показан пример запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-123">The next screenshot shows an example of this confirmation prompt.</span></span>

 ![Выбор режима Internet Explorer](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-override.png)

## <span data-ttu-id="6cf7e-125">Вспомогательные политики</span><span class="sxs-lookup"><span data-stu-id="6cf7e-125">Supporting policies</span></span>

<span data-ttu-id="6cf7e-126">Организации, которые хотят исключить блокировку смешанного содержимого для определенных веб-сайтов, могут для этого использовать политику [InsecureContentAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#insecurecontentallowedforurls).</span><span class="sxs-lookup"><span data-stu-id="6cf7e-126">Enterprises that want to exclude mixed content blocking from specific websites can use the [InsecureContentAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#insecurecontentallowedforurls) policy to do so.</span></span>

## <span data-ttu-id="6cf7e-127">Лицензия на содержимое</span><span class="sxs-lookup"><span data-stu-id="6cf7e-127">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="6cf7e-128">Некоторые части этой страницы представляют собой измененные материалы, созданные и предоставленные на сайте Chromium.org. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span><span class="sxs-lookup"><span data-stu-id="6cf7e-128">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="6cf7e-129">Исходная страница Chromium находится [здесь](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).</span><span class="sxs-lookup"><span data-stu-id="6cf7e-129">The original page can be found [here](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="6cf7e-130">Эта работа предоставляется в рамках международной лицензии <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-130">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <span data-ttu-id="6cf7e-131">См. также</span><span class="sxs-lookup"><span data-stu-id="6cf7e-131">See also</span></span>

- [<span data-ttu-id="6cf7e-132">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="6cf7e-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
