---
title: Сохранение навигации в пределах страницы в режиме Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Сохранение навигации в пределах страницы в режиме Internet Explorer
ms.openlocfilehash: 0acca9e05a0d09b02fa61d5ddd7de3f7c6cabb92
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980912"
---
# <span data-ttu-id="9baaa-103">Сохранение навигации в пределах страницы в режиме Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="9baaa-103">Keep in-page navigation in Internet Explorer mode</span></span>

<span data-ttu-id="9baaa-104">Эту политику можно использовать в качестве временного решения, чтобы все переходы в пределах страницы с сайтов в режиме Internet Explorer (IE) оставались в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="9baaa-104">You can use this policy as a temporary solution to force all in-page navigation from Internet Explorer mode (IE mode) sites to stay in IE mode.</span></span>

<span data-ttu-id="9baaa-105">Переход в пределах страницы начинается со ссылки, сценария или формы на текущей странице.</span><span class="sxs-lookup"><span data-stu-id="9baaa-105">An in-page navigation is started from a link, a script, or a form on the current page.</span></span> <span data-ttu-id="9baaa-106">Также это также может быть перенаправление на сервере предыдущей попытки перехода в пределах страницы.</span><span class="sxs-lookup"><span data-stu-id="9baaa-106">It can also be a server-side redirect of a previous in-page navigation attempt.</span></span> <span data-ttu-id="9baaa-107">И наоборот, пользователь может начать переход, не ограниченный текущей страницей и независимый от нее, несколькими способами, используя элементы управления браузера.</span><span class="sxs-lookup"><span data-stu-id="9baaa-107">Conversely, a user can start a navigation that isn't in-page that's independent of the current page in several ways by using the browser controls.</span></span> <span data-ttu-id="9baaa-108">Например, с помощью адресной строки, кнопки "Назад" или ссылки в избранном.</span><span class="sxs-lookup"><span data-stu-id="9baaa-108">For example, using the address bar, the back button, or a favorite link.</span></span>

>[!NOTE]
><span data-ttu-id="9baaa-109">Эта статья относится к Microsoft Edge версии 81 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="9baaa-109">This article applies to Microsoft Edge version 81 or later.</span></span>

## <span data-ttu-id="9baaa-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="9baaa-110">Prerequisites</span></span>

<span data-ttu-id="9baaa-111">Для этой политики необходимы следующие обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="9baaa-111">The following Windows updates are required for this policy:</span></span>

- <span data-ttu-id="9baaa-112">Windows10 версии 1909 и 1903, Windows Server версии 1909 и 1903 ([KB4532695](https://support.microsoft.com/help/4532695))</span><span class="sxs-lookup"><span data-stu-id="9baaa-112">Windows 10 version 1909 & 1903, Windows Server version 1909 & 1903  ([KB4532695](https://support.microsoft.com/help/4532695))</span></span>
- <span data-ttu-id="9baaa-113">Windows10 версии 1809, Windows Serverверсии 1809, Windows Server2019 ([KB4534321](https://support.microsoft.com/help/4534321))</span><span class="sxs-lookup"><span data-stu-id="9baaa-113">Windows 10 version 1809, Windows Server version 1809, Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))</span></span>
- <span data-ttu-id="9baaa-114">Windows10 версии 1803 ([KB4534308](https://support.microsoft.com/help/4534308))</span><span class="sxs-lookup"><span data-stu-id="9baaa-114">Windows 10 version 1803 ([KB4534308](https://support.microsoft.com/help/4534308))</span></span>
- <span data-ttu-id="9baaa-115">Windows10 версии 1709 ([KB4534318](https://support.microsoft.com/help/4534318))</span><span class="sxs-lookup"><span data-stu-id="9baaa-115">Windows 10 version 1709 ([KB4534318](https://support.microsoft.com/help/4534318))</span></span>


## <span data-ttu-id="9baaa-116">Об этой политике</span><span class="sxs-lookup"><span data-stu-id="9baaa-116">About this policy</span></span>

<span data-ttu-id="9baaa-117">Настоящая политика дает вам время на обнаружение и настройку всех серверов проверки подлинности, используемых сайтами в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="9baaa-117">This policy gives you time to identify and configure all of the authentication servers used by your IE mode sites.</span></span> <span data-ttu-id="9baaa-118">Однако данная политика может привести к неправильной работе браузера, когда некоторые сайты иногда отображаются в режиме IE, а иногда— в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9baaa-118">However, this policy can result in an inconsistent browsing experience, where some sites are rendered in IE mode and at other times rendered in Microsoft Edge mode.</span></span> <span data-ttu-id="9baaa-119">Это зависит от того, был ли начат переход на сайт со страницы в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="9baaa-119">This experience depends on whether the navigation to the site began from an IE mode page.</span></span> <span data-ttu-id="9baaa-120">Такой нестабильности будет подвержен любой сайт, не настроенный явно для открытия в определенном модуле отрисовки.</span><span class="sxs-lookup"><span data-stu-id="9baaa-120">Any site that isn't explicitly configured to open in a specific rendering engine will be subject to this inconsistency.</span></span>

<span data-ttu-id="9baaa-121">Если эта политика включена, рекомендуем отключить ее после того, как вы определите все серверы проверки подлинности и внесете их в список сайтов как нейтральные.</span><span class="sxs-lookup"><span data-stu-id="9baaa-121">If you enable this policy, we recommend that you disable it after you've identified all the authentication servers and added them to the site list as neutral.</span></span> <span data-ttu-id="9baaa-122">Это действие гарантирует, что ваши современные сайты не откроются случайно в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="9baaa-122">This action ensures that your modern sites never inadvertently render in IE mode.</span></span>

## <span data-ttu-id="9baaa-123">Сохранение навигации в пределах страницы в режиме IE</span><span class="sxs-lookup"><span data-stu-id="9baaa-123">Keep in-page navigation in IE mode</span></span>

<span data-ttu-id="9baaa-124">Чтобы оставить автоматические переходы или все переходы в пределах страницы в режиме Internet Explorer, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="9baaa-124">To keep automatic or all in-page navigation in Internet Explorer mode, follow these steps:</span></span>

1. <span data-ttu-id="9baaa-125">Откройте редактор локальных групповых политик.</span><span class="sxs-lookup"><span data-stu-id="9baaa-125">Open Local Group Policy Editor.</span></span>
2. <span data-ttu-id="9baaa-126">Щелкните **Конфигурация компьютера** > **Административные шаблоны** > **Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="9baaa-126">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
3. <span data-ttu-id="9baaa-127">В разделе **Настройка** дважды щелкните пункт **Указать, как будут действовать переходы в пределах страницы на ненастроенные сайты, начинаемые со страниц в режиме Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="9baaa-127">Under **Setting**, double-click **Specify how "in-page" navigations to unconfigured sites behave when started from Internet Explorer mode pages**.</span></span>

   ![Параметр политики переходов в пределах страницы](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-settings.png)

4. <span data-ttu-id="9baaa-129">Выберите **Включено**.</span><span class="sxs-lookup"><span data-stu-id="9baaa-129">Select **Enabled**</span></span> 

   ![Включение политики переходов в пределах страницы](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-enable.png)

5. <span data-ttu-id="9baaa-131">В раскрывающемся списке выберите одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9baaa-131">Choose one of the following options from the dropdown list:</span></span>

   - <span data-ttu-id="9baaa-132">**По умолчанию**— в этом режиме будут открываться только сайты, настроенные на открытие в режиме Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9baaa-132">**Default** - Only sites configured to open in Internet Explorer mode will open in that mode.</span></span> <span data-ttu-id="9baaa-133">Все сайты, не настроенные для открытия в режиме Internet Explorer, будут перенаправляться обратно в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9baaa-133">Any site not configured to open in Internet Explorer mode will be redirected back to Microsoft Edge.</span></span>
   - <span data-ttu-id="9baaa-134">**Сохранять только автоматические переходы в режиме Internet Explorer**— используйте этот параметр, если режим Internet Explorer должен использоваться по умолчанию для всех автоматических переходов (таких как перенаправление 302) на ненастроенные сайты.</span><span class="sxs-lookup"><span data-stu-id="9baaa-134">**Keep only automatic navigations in Internet Explorer mode** - Use this option if you want the default experience except that all automatic navigations (such as 302 redirects) to unconfigured sites will be kept in Internet Explorer mode.</span></span>
   - <span data-ttu-id="9baaa-135">**Сохранять все переходы в пределах страницы в режиме Internet Explorer** ***(не рекомендуется)***— все переходы со страниц, загруженных в режиме IE, на ненастроенные сайты, сохраняются в режиме Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9baaa-135">**Keep all in-page navigation in Internet Explorer mode** ***(Least Recommended)*** - All navigations from pages loaded in IE mode to unconfigured sites are kept in Internet Explorer mode.</span></span>

6. <span data-ttu-id="9baaa-136">Нажмите кнопку **OK** или **Применить** для сохранения настроек политики.</span><span class="sxs-lookup"><span data-stu-id="9baaa-136">Click **OK** or **Apply** to save the policy settings.</span></span>

## <span data-ttu-id="9baaa-137">См. также</span><span class="sxs-lookup"><span data-stu-id="9baaa-137">See also</span></span>

- [<span data-ttu-id="9baaa-138">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="9baaa-138">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
