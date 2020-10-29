---
title: Обратная совместимость для корпоративной страницы новой вкладки
ms.author: ruchir
author: dan-wesley
manager: vwehren
ms.date: 10/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Обратная совместимость для корпоративной страницы новой вкладки
ms.openlocfilehash: c10671a6ec8e1ff4dcb0db3f3c085f82ae973122
ms.sourcegitcommit: af6ab070d0c09bca4a9cf505b107ed7e04839763
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2020
ms.locfileid: "11144497"
---
# <span data-ttu-id="c421d-103">Обратная совместимость для корпоративной страницы новой вкладки</span><span class="sxs-lookup"><span data-stu-id="c421d-103">Backwards compatibility for the Enterprise New tab page</span></span>

<span data-ttu-id="c421d-104">В этой статье описано изменение страницы новой вкладки, а также способ обеспечения обратной совместимости для пользователей в Microsoft Edge версии 87 и более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="c421d-104">This article describes the change to the New tab page and how users can be backwards compatible with Microsoft Edge version 87 and earlier.</span></span>

> [!NOTE]
> <span data-ttu-id="c421d-105">Эта статья относится к Microsoft Edge версии 87 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="c421d-105">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="c421d-106">Информационные веб-каналы из одной конечной точки</span><span class="sxs-lookup"><span data-stu-id="c421d-106">Information feeds from single endpoint</span></span>

<span data-ttu-id="c421d-107">Новая версия корпоративной страницы новой вкладки объединяет соответствующий контент Microsoft 365 с важными и подходящими отраслевыми информационными веб-каналами, которые предоставляются посредством конечной точки MSN.com</span><span class="sxs-lookup"><span data-stu-id="c421d-107">The new version of the Enterprise New tab page combines compliant Microsoft 365 content with industry relevant and compliant information feeds that are served via the MSN.com endpoint.</span></span>

> [!NOTE]
> <span data-ttu-id="c421d-108">Контент Office 365 изначально предоставлялся с помощью домена [Office.com](https://www.office.com).</span><span class="sxs-lookup"><span data-stu-id="c421d-108">Office 365 content was originally served using the [Office.com](https://www.office.com) domain.</span></span>

<span data-ttu-id="c421d-109">Если доступ к домену MSN.com ограничен в вашей организации, настоятельно рекомендуется предоставить пользователям доступ к этому [URL-адресу](https://ntp.msn.com).</span><span class="sxs-lookup"><span data-stu-id="c421d-109">If access to the MSN.com domain is restricted for your organization, we strongly recommend giving users access to this [url](https://ntp.msn.com).</span></span>

<span data-ttu-id="c421d-110">Если вам нужно больше времени для разрешения доступа к домену MSN, рекомендуется использовать политику [NewTabPageSetFeedType](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagesetfeedtype), позволяющую выбрать веб-канал Microsoft News или Office 365 на странице новой вкладки.</span><span class="sxs-lookup"><span data-stu-id="c421d-110">If you need more time to enable access to the MSN domain, we recommend using the [NewTabPageSetFeedType](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagesetfeedtype), that lets you choose either the Microsoft News or Office 365 feed experience for the new tab page.</span></span>

### <span data-ttu-id="c421d-111">Продолжение использования Office.com</span><span class="sxs-lookup"><span data-stu-id="c421d-111">Keep using Office.com</span></span>

 <span data-ttu-id="c421d-112">Вы можете настроить политику **NewTabPageSetFeedType**, чтобы использовать устаревший домен Office.com.</span><span class="sxs-lookup"><span data-stu-id="c421d-112">You can configure the **NewTabPageSetFeedType** policy to keep using the deprecated Office.com domain.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c421d-113">Политика **NewTabPageSetFeedType** и домен Office.com, предоставляющие контент Office 365, перестанут работать после выпуска Microsoft Edge версии 90.</span><span class="sxs-lookup"><span data-stu-id="c421d-113">The **NewTabPageSetFeedType** policy and the Office.com domain that serves Office 365 content will quit working when Microsoft Edge version 90 is released.</span></span>

<span data-ttu-id="c421d-114">Следующие параметры политики обеспечат отображение на корпоративной странице новой вкладки контента документа Office из домена Office.com.</span><span class="sxs-lookup"><span data-stu-id="c421d-114">The following policy settings will force the Enterprise New tab page to render Office document content from the Office.com domain.</span></span>

- <span data-ttu-id="c421d-115">Настройте политику как **обязательную**.</span><span class="sxs-lookup"><span data-stu-id="c421d-115">Set the policy as **Mandatory**.</span></span>
- <span data-ttu-id="c421d-116">Установите для сопоставления политики значение **Office (1) = Office 365 feed experience**.</span><span class="sxs-lookup"><span data-stu-id="c421d-116">Set the value of the policy mapping to **Office (1) = Office 365 feed experience**.</span></span>

<span data-ttu-id="c421d-117">Если переключение на Office.com невозможно, отправьте нам отзыв.</span><span class="sxs-lookup"><span data-stu-id="c421d-117">If the switch to the Office.com isn't possible, reach out and send us feedback.</span></span> <span data-ttu-id="c421d-118">Кроме того, можно настроить политику [NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation), чтобы она указывала на URL-адрес конечной точки, разрешенный в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="c421d-118">Another option is to configure the [NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) so it points to an endpoint URL that's allowed by your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="c421d-119">Политика **NewTabPageLocation** имеет приоритет, если политика **NewTabPageSetFeedType** также настроена.</span><span class="sxs-lookup"><span data-stu-id="c421d-119">The **NewTabPageLocation** policy has precedence if the **NewTabPageSetFeedType** policy is also configured.</span></span>

## <span data-ttu-id="c421d-120">Корпоративным пользователям теперь будет доступен контент Microsoft News в канале "Моя лента"</span><span class="sxs-lookup"><span data-stu-id="c421d-120">Enterprise users will now get Microsoft news content via My Feed</span></span>

<span data-ttu-id="c421d-121">Корпоративная страница новой вкладки предлагает отраслевые сведения в канале **Моя лента** и контент Office 365 в одном представлении для пользователей, вошедших в свою учетную запись Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="c421d-121">The Enterprise New tab page will offer industry relevant information in **My Feed** and Office 365 content in a single view for users signed in with their Azure Active Directory (Azure AD) account.</span></span> <span data-ttu-id="c421d-122">Для пользователей, вошедших с помощью учетной записи Azure Active Directory (Azure AD) и выбравших параметр Microsoft News во всплывающем окне параметров, представление страницы новой вкладки будет заменено на контент канала **Моя лента**.</span><span class="sxs-lookup"><span data-stu-id="c421d-122">For users signed in with their Azure Active Directory (Azure AD) who selected the Microsoft News option in the settings flyout, their new tab page view will be replaced with **My Feed** content.</span></span> <span data-ttu-id="c421d-123">Когда они откроют страницу новой вкладки в браузере, она будет выглядеть, как показано в примере на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="c421d-123">When they open a new tab page in the browser it will look like the example in the next screenshot.</span></span>

![Страница новой вкладки с отображением контента из канала "Моя лента".](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-myfeed-view.png)

> [!NOTE]
> <span data-ttu-id="c421d-125">Пользователям, не вошедшим в Azure AD, будет по-прежнему отображаться веб-канал MSN News при открытии новой вкладки.</span><span class="sxs-lookup"><span data-stu-id="c421d-125">Users who aren't signed in with Azure AD will continue to see the MSN News feed when they open a new tab.</span></span>

## <span data-ttu-id="c421d-126">Макет страницы</span><span class="sxs-lookup"><span data-stu-id="c421d-126">Page layout</span></span>

<span data-ttu-id="c421d-127">После изменений страницы новой вкладки макет страницы больше не должен управлять двумя определенными типами контента (Office 365 и Microsoft News), поэтому переключатель контента недоступен.</span><span class="sxs-lookup"><span data-stu-id="c421d-127">With the changes to the New tab page, the Page layout no longer has to control two specific content types (Office 365 and Microsoft News), so the content toggle isn't available.</span></span> <span data-ttu-id="c421d-128">На следующем снимке экрана показано всплывающее окно макета страницы.</span><span class="sxs-lookup"><span data-stu-id="c421d-128">The next screenshot shows the flyout for the Page layout.</span></span>

![Представление макета страницы для страницы новой вкладки.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-page-layout.png)

<span data-ttu-id="c421d-130">Если вы хотите продолжать обращаться к контенту Microsoft News, не связанному с вашей организацией, вы должны использовать другой профиль браузера.</span><span class="sxs-lookup"><span data-stu-id="c421d-130">If you want to keep accessing Microsoft News content that isn't tied to your organization, you must use a different browser profile.</span></span> <span data-ttu-id="c421d-131">Перейдите на страницу *edge://settings/profiles* и выйдите из профиля Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c421d-131">Go to  *edge://settings/profiles* and sign out of your Azure AD profile.</span></span> <span data-ttu-id="c421d-132">В результате этого действия отобразится стандартное представление корпоративной страницы новой вкладки.</span><span class="sxs-lookup"><span data-stu-id="c421d-132">This action will bring up the  standard view for the Enterprise new tab page.</span></span> 

## <span data-ttu-id="c421d-133">См. также</span><span class="sxs-lookup"><span data-stu-id="c421d-133">See also</span></span>

- [<span data-ttu-id="c421d-134">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="c421d-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="c421d-135">Режим предприятия для Internet Explorer11</span><span class="sxs-lookup"><span data-stu-id="c421d-135">Enterprise Mode for Internet Explorer 11</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
