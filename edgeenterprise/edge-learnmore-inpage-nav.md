---
title: Сохранение навигации в пределах страницы в режиме Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Сохранение навигации в пределах страницы в режиме Internet Explorer
ms.openlocfilehash: 20b18d121c3babfaacffd4a08316b25be714d95e
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641365"
---
# <a name="keep-in-page-navigation-in-internet-explorer-mode"></a><span data-ttu-id="31cb6-103">Сохранение навигации в пределах страницы в режиме Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="31cb6-103">Keep in-page navigation in Internet Explorer mode</span></span>

<span data-ttu-id="31cb6-104">Эту политику можно использовать в качестве временного решения, чтобы все переходы в пределах страницы с сайтов в режиме Internet Explorer (IE) оставались в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="31cb6-104">You can use this policy as a temporary solution to force all in-page navigation from Internet Explorer mode (IE mode) sites to stay in IE mode.</span></span>

<span data-ttu-id="31cb6-105">Переход в пределах страницы начинается со ссылки, сценария или формы на текущей странице.</span><span class="sxs-lookup"><span data-stu-id="31cb6-105">An in-page navigation is started from a link, a script, or a form on the current page.</span></span> <span data-ttu-id="31cb6-106">Также это также может быть перенаправление на сервере предыдущей попытки перехода в пределах страницы.</span><span class="sxs-lookup"><span data-stu-id="31cb6-106">It can also be a server-side redirect of a previous in-page navigation attempt.</span></span> <span data-ttu-id="31cb6-107">И наоборот, пользователь может начать переход, не ограниченный текущей страницей и независимый от нее, несколькими способами, используя элементы управления браузера.</span><span class="sxs-lookup"><span data-stu-id="31cb6-107">Conversely, a user can start a navigation that isn't in-page that's independent of the current page in several ways by using the browser controls.</span></span> <span data-ttu-id="31cb6-108">Например, с помощью адресной строки, кнопки "Назад" или ссылки в избранном.</span><span class="sxs-lookup"><span data-stu-id="31cb6-108">For example, using the address bar, the back button, or a favorite link.</span></span>

>[!NOTE]
><span data-ttu-id="31cb6-109">Эта статья относится к Microsoft Edge версии 81 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="31cb6-109">This article applies to Microsoft Edge version 81 or later.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="31cb6-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="31cb6-110">Prerequisites</span></span>

<span data-ttu-id="31cb6-111">Для этой политики необходимы следующие обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="31cb6-111">The following Windows updates are required for this policy:</span></span>

- <span data-ttu-id="31cb6-112">Windows10 версии 1909 и 1903, Windows Server версии 1909 и 1903 ([KB4532695](https://support.microsoft.com/help/4532695))</span><span class="sxs-lookup"><span data-stu-id="31cb6-112">Windows 10 version 1909 & 1903, Windows Server version 1909 & 1903  ([KB4532695](https://support.microsoft.com/help/4532695))</span></span>
- <span data-ttu-id="31cb6-113">Windows10 версии 1809, Windows Serverверсии 1809, Windows Server2019 ([KB4534321](https://support.microsoft.com/help/4534321))</span><span class="sxs-lookup"><span data-stu-id="31cb6-113">Windows 10 version 1809, Windows Server version 1809, Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))</span></span>
- <span data-ttu-id="31cb6-114">Windows10 версии 1803 ([KB4534308](https://support.microsoft.com/help/4534308))</span><span class="sxs-lookup"><span data-stu-id="31cb6-114">Windows 10 version 1803 ([KB4534308](https://support.microsoft.com/help/4534308))</span></span>
- <span data-ttu-id="31cb6-115">Windows10 версии 1709 ([KB4534318](https://support.microsoft.com/help/4534318))</span><span class="sxs-lookup"><span data-stu-id="31cb6-115">Windows 10 version 1709 ([KB4534318](https://support.microsoft.com/help/4534318))</span></span>


## <a name="about-this-policy"></a><span data-ttu-id="31cb6-116">Об этой политике</span><span class="sxs-lookup"><span data-stu-id="31cb6-116">About this policy</span></span>

<span data-ttu-id="31cb6-117">Настоящая политика дает вам время на обнаружение и настройку всех серверов проверки подлинности, используемых сайтами в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="31cb6-117">This policy gives you time to identify and configure all of the authentication servers used by your IE mode sites.</span></span> <span data-ttu-id="31cb6-118">Однако данная политика может привести к неправильной работе браузера, когда некоторые сайты иногда отображаются в режиме IE, а иногда— в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="31cb6-118">However, this policy can result in an inconsistent browsing experience, where some sites are rendered in IE mode and at other times rendered in Microsoft Edge mode.</span></span> <span data-ttu-id="31cb6-119">Это зависит от того, был ли начат переход на сайт со страницы в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="31cb6-119">This experience depends on whether the navigation to the site began from an IE mode page.</span></span> <span data-ttu-id="31cb6-120">Такой нестабильности будет подвержен любой сайт, не настроенный явно для открытия в определенном модуле отрисовки.</span><span class="sxs-lookup"><span data-stu-id="31cb6-120">Any site that isn't explicitly configured to open in a specific rendering engine will be subject to this inconsistency.</span></span>

<span data-ttu-id="31cb6-121">Если эта политика включена, рекомендуем отключить ее после того, как вы определите все серверы проверки подлинности и внесете их в список сайтов как нейтральные.</span><span class="sxs-lookup"><span data-stu-id="31cb6-121">If you enable this policy, we recommend that you disable it after you've identified all the authentication servers and added them to the site list as neutral.</span></span> <span data-ttu-id="31cb6-122">Это действие гарантирует, что ваши современные сайты не откроются случайно в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="31cb6-122">This action ensures that your modern sites never inadvertently render in IE mode.</span></span>

## <a name="keep-in-page-navigation-in-ie-mode"></a><span data-ttu-id="31cb6-123">Сохранение навигации в пределах страницы в режиме IE</span><span class="sxs-lookup"><span data-stu-id="31cb6-123">Keep in-page navigation in IE mode</span></span>

<span data-ttu-id="31cb6-124">Чтобы оставить автоматические переходы или все переходы в пределах страницы в режиме Internet Explorer, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="31cb6-124">To keep automatic or all in-page navigation in Internet Explorer mode, follow these steps:</span></span>

1. <span data-ttu-id="31cb6-125">Откройте редактор локальных групповых политик.</span><span class="sxs-lookup"><span data-stu-id="31cb6-125">Open Local Group Policy Editor.</span></span>
2. <span data-ttu-id="31cb6-126">Щелкните **Конфигурация компьютера** > **Административные шаблоны** > **Microsoft Edge**.</span><span class="sxs-lookup"><span data-stu-id="31cb6-126">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
3. <span data-ttu-id="31cb6-127">В разделе **Настройка** дважды щелкните пункт **Указать, как будут действовать переходы в пределах страницы на ненастроенные сайты, начинаемые со страниц в режиме Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="31cb6-127">Under **Setting**, double-click **Specify how "in-page" navigations to unconfigured sites behave when started from Internet Explorer mode pages**.</span></span>

   ![Параметр политики переходов в пределах страницы](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-settings.png)

4. <span data-ttu-id="31cb6-129">Выберите **Включено**.</span><span class="sxs-lookup"><span data-stu-id="31cb6-129">Select **Enabled**</span></span> 

   ![Включение политики переходов в пределах страницы](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-enable.png)

5. <span data-ttu-id="31cb6-131">В раскрывающемся списке выберите одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="31cb6-131">Choose one of the following options from the dropdown list:</span></span>

   - <span data-ttu-id="31cb6-132">**По умолчанию**— в этом режиме будут открываться только сайты, настроенные на открытие в режиме Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="31cb6-132">**Default** - Only sites configured to open in Internet Explorer mode will open in that mode.</span></span> <span data-ttu-id="31cb6-133">Все сайты, не настроенные для открытия в режиме Internet Explorer, будут перенаправляться обратно в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="31cb6-133">Any site not configured to open in Internet Explorer mode will be redirected back to Microsoft Edge.</span></span>
   - <span data-ttu-id="31cb6-134">**Сохранять только автоматические переходы в режиме Internet Explorer**— используйте этот параметр, если режим Internet Explorer должен использоваться по умолчанию для всех автоматических переходов (таких как перенаправление 302) на ненастроенные сайты.</span><span class="sxs-lookup"><span data-stu-id="31cb6-134">**Keep only automatic navigations in Internet Explorer mode** - Use this option if you want the default experience except that all automatic navigations (such as 302 redirects) to unconfigured sites will be kept in Internet Explorer mode.</span></span>
   - <span data-ttu-id="31cb6-135">**Сохранение всей навигации на странице в режиме Internet Explorer**  \* *_(Наименее рекомендуемый)_*_ — Все навигации со страниц, загруженных в режиме IE, до неконфигуративных сайтов, хранятся в режиме Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="31cb6-135">**Keep all in-page navigation in Internet Explorer mode** \**_(Least Recommended)_*_ - All navigations from pages loaded in IE mode to unconfigured sites are kept in Internet Explorer mode.</span></span>

6. <span data-ttu-id="31cb6-136">Нажмите*кнопку _OK*\* или **применить** для сохранения параметров политики.</span><span class="sxs-lookup"><span data-stu-id="31cb6-136">Click _*OK*\* or **Apply** to save the policy settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="31cb6-137">См. также</span><span class="sxs-lookup"><span data-stu-id="31cb6-137">See also</span></span>

- [<span data-ttu-id="31cb6-138">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="31cb6-138">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
