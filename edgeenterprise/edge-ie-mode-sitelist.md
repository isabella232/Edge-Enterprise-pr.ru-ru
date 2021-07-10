---
title: Стратегия настройки корпоративных сайтов
ms.author: shisub
author: shisub
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Пошаговое руководство по настройке списка сайтов в режиме предприятия для режима Internet Explorer.
ms.openlocfilehash: 72de393a5da0b4b0e2950951ae527f6ef870e110
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641815"
---
# <a name="enterprise-site-configuration-strategy"></a><span data-ttu-id="ed0eb-103">Стратегия настройки корпоративных сайтов</span><span class="sxs-lookup"><span data-stu-id="ed0eb-103">Enterprise site configuration strategy</span></span>

>[!Note]
> <span data-ttu-id="ed0eb-104">Поддержка классических приложений Internet Explorer 11 будет прекращена и больше не будет поддерживаться 15 июня 2022 г. (список области применения см. в [часто задаваемых вопросах](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span><span class="sxs-lookup"><span data-stu-id="ed0eb-104">The Internet Explorer 11 desktop application will be retired and go out of support on June 15, 2022 (for a list of what’s in scope, [see the FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span></span> <span data-ttu-id="ed0eb-105">Те же приложения и сайты IE11, которые вы используете сегодня, можно открывать в Microsoft Edge в режиме Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-105">The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode.</span></span> <span data-ttu-id="ed0eb-106">[Более подробную информацию см. здесь.](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)</span><span class="sxs-lookup"><span data-stu-id="ed0eb-106">[Learn more here](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span></span>

<span data-ttu-id="ed0eb-107">В этой статье описываются изменения, внесенные в список сайтов в режиме предприятия для поддержки режима Internet Explorer в Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-107">This article describes changes to the Enterprise Mode Site List to support Internet Explorer mode for Microsoft Edge version 77 and later.</span></span>

<span data-ttu-id="ed0eb-108">Дополнительные сведения о схеме для XML-файла списка сайтов в режиме предприятия см. в статье [Руководство по схеме режима предприятия версии 2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="ed0eb-108">For more information on the schema for the Enterprise Mode Site List XML file, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

> [!NOTE]
> <span data-ttu-id="ed0eb-109">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-109">This article applies to Microsoft Edge version 77 or later.</span></span>
<!--
## Updated schema elements

The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:

| **Element** | **Description** |
| --- | --- |
| \<open-in app="**true**"\> | A child element that controls what browser is used for sites. This element is required for sites that need to **open in IE11**.|

**Example:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

The following table shows the possible values of the \<open-in\> element:

| **Value** | **Description** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Opens the site in IE mode or a full IE11 window. To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Opens the site in a full IE11 window |
| **\<open-in\>MSEdge\</open-in\>** | Opens the site in Microsoft Edge |
| **\<open-in\>None or not specified\</open-in\>** | Opens the site in the default browser or in the browser where the user navigated to the site. |
|**\<open-in\>Configurable\</open-in\>** | Allows the site to participate in IE mode engine determination. To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_. Adding it to the other 'open-in' elements won't change browser behavior.   -->

## <a name="configuration-strategy"></a><span data-ttu-id="ed0eb-110">Стратегия настройки</span><span class="sxs-lookup"><span data-stu-id="ed0eb-110">Configuration strategy</span></span>

<span data-ttu-id="ed0eb-111">В стратегию настройки сайтов для режима IE входят следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ed0eb-111">The following steps are part of a site configuration strategy for IE mode:</span></span>
1. <span data-ttu-id="ed0eb-112">Подготовка списка сайтов</span><span class="sxs-lookup"><span data-stu-id="ed0eb-112">Prepare your site list</span></span>
2. <span data-ttu-id="ed0eb-113">Настройка нейтральных сайтов</span><span class="sxs-lookup"><span data-stu-id="ed0eb-113">Configure neutral sites</span></span>
3. <span data-ttu-id="ed0eb-114">(Необязательно) Использование общего доступа к файлам cookie при необходимости</span><span class="sxs-lookup"><span data-stu-id="ed0eb-114">(Optional) Use cookie sharing if necessary</span></span>

<!--
Step 1.  – if you don’t have one use Site Discovery Step-by-Step
Step 2 – Neutral sites + sticky mode
        Use more examples and explain sticky mode better
Step 3 – If that doesn’t cover your needs, then use Cookie sharing -->

## <a name="prepare-your-site-list"></a><span data-ttu-id="ed0eb-115">Подготовка списка сайтов</span><span class="sxs-lookup"><span data-stu-id="ed0eb-115">Prepare your site list</span></span>

<span data-ttu-id="ed0eb-116">Если у вас уже есть список сайтов в режиме предприятия для IE11 или устаревшей версии Microsoft Edge, его можно использовать повторно для настройки режима IE.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-116">If you already have an Enterprise Mode site list for IE11 or Microsoft Edge Legacy, you can reuse it to configure IE mode.</span></span>

<span data-ttu-id="ed0eb-117">Если у вас нет списка сайтов, для его заполнения можно использовать [средство обнаружения корпоративных сайтов](/deployedge/edge-ie-mode-site-discovery).</span><span class="sxs-lookup"><span data-stu-id="ed0eb-117">However, if you don't have a site list, you can use the [Enterprise Site Discovery tool](/deployedge/edge-ie-mode-site-discovery) to populate your site list.</span></span>

## <a name="configure-neutral-sites"></a><span data-ttu-id="ed0eb-118">Настройка нейтральных сайтов</span><span class="sxs-lookup"><span data-stu-id="ed0eb-118">Configure neutral sites</span></span>

<span data-ttu-id="ed0eb-119">Чтобы режим IE работал правильно, требуется явным образом настроить серверы проверки подлинности и единого входа в качестве нейтральных сайтов.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-119">In order for IE mode to work properly, authentication / Single Sign-On (SSO) servers will need to be explicitly configured as neutral sites.</span></span> <span data-ttu-id="ed0eb-120">В противном случае страницы в режиме IE попытаются выполнить перенаправление в Microsoft Edge, и проверка подлинности завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-120">Otherwise, IE mode pages will try to redirect to Microsoft Edge, and authentication will fail.</span></span>

<span data-ttu-id="ed0eb-121">Нейтральный сайт будет использовать браузер, в котором начат переход: Microsoft Edge или режим IE.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-121">A neutral site will use the browser where the navigation started - either Microsoft Edge or IE mode.</span></span> <span data-ttu-id="ed0eb-122">Настройка нейтральных сайтов гарантирует, что все приложения, использующие эти серверы проверки подлинности (современные и устаревшие), продолжат работать.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-122">Configuring neutral sites ensures that all applications using these authentication servers, both modern and legacy, continue to work.</span></span>

<span data-ttu-id="ed0eb-123">Вы можете настроить нейтральные сайты, выбрав "Нет" в раскрывающемся списке *Открыть в* инструмента Enterprise Mode Site List Manager или непосредственно обновив XML-файл списка сайтов:</span><span class="sxs-lookup"><span data-stu-id="ed0eb-123">You can configure neutral sites by setting the *Open In* dropdown to 'None' in the Enterprise Mode Site List Manager tool or by directly updating the site list XML:</span></span>

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

<span data-ttu-id="ed0eb-124">Чтобы определить серверы проверки подлинности, проверьте трафик из приложения с помощью средств разработчика IE11.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-124">To identify authentication servers, inspect the network traffic from an application using the IE11 Developer Tools.</span></span> <span data-ttu-id="ed0eb-125">Если вам требуется больше времени, чтобы определить серверы проверки подлинности, можно настроить политику, сохраняющую все переходы в пределах страницы в режиме IE, чтобы пользователи могли продолжать свои рабочие процессы без перерывов.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-125">If you need more time to identify your authentication servers, you can configure a policy to keep all in-page navigations in IE mode to allow your users to continue their workflows uninterrupted.</span></span> <span data-ttu-id="ed0eb-126">При необходимости отключите этот параметр после определения и добавления серверов проверки подлинности в список сайтов, чтобы свести к минимуму использование режима IE.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-126">To minimize the use of IE mode when unnecessary, disable this setting once you've identified and added your authentication servers to the site list.</span></span> <span data-ttu-id="ed0eb-127">Дополнительные сведения см. в разделе [Сохранение переходов в пределах страницы в режиме IE](/deployedge/edge-learnmore-inpage-nav).</span><span class="sxs-lookup"><span data-stu-id="ed0eb-127">For more information, see [Keep in-page navigation in IE mode](/deployedge/edge-learnmore-inpage-nav).</span></span>

>[!NOTE]
   ><span data-ttu-id="ed0eb-128">Схема режима предприятия версии 1 не поддерживается для интеграции с режимом IE.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-128">Enterprise Mode schema v.1 isn't supported for IE mode integration.</span></span> <span data-ttu-id="ed0eb-129">Если вы используете схему версии 1 в Internet Explorer 11, необходимо обновить схему до версии 2.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-129">If you are currently using schema v.1 with Internet Explorer 11, you must upgrade to schema v.2.</span></span> <span data-ttu-id="ed0eb-130">Дополнительные сведения см. в разделе [Руководство по схеме режима предприятия версии 2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="ed0eb-130">For more information, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

## <a name="optional-use-cookie-sharing-if-necessary"></a><span data-ttu-id="ed0eb-131">(Необязательно) Использование общего доступа к файлам cookie при необходимости</span><span class="sxs-lookup"><span data-stu-id="ed0eb-131">(Optional) Use cookie sharing if necessary</span></span>

<span data-ttu-id="ed0eb-132">По умолчанию процессы Microsoft Edge и Internet Explorer не делятся файлами cookie сеансов, и в некоторых случаях при использовании режима IE это может быть неудобно.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-132">By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this lack of sharing can be inconvenient in some cases while using IE mode.</span></span> <span data-ttu-id="ed0eb-133">Например, если пользователю необходимо выполнить повторную проверку подлинности в режиме IE и он уже привык это делать или если при выходе из сеанса Microsoft Edge он не выходит из сеанса в режиме Internet Explorer для выполнения критически важных транзакций.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-133">For example, when a user has to reauthenticate in IE mode when previously they are accustomed to doing so or when signing out of a Microsoft Edge session doesn’t sign out of the Internet Explorer mode session for critical transactions.</span></span> <span data-ttu-id="ed0eb-134">В таких сценариях вы можете настроить определенный набор файлов cookie (с помощью единого входа) для отправки из Microsoft Edge в Internet Explorer, чтобы проверка подлинности выполнялась проще благодаря устранению необходимости в повторной проверке.</span><span class="sxs-lookup"><span data-stu-id="ed0eb-134">In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to reauthenticate.</span></span> <span data-ttu-id="ed0eb-135">Дополнительные сведения см. в разделе [Отправка файлов cookie из Microsoft Edge в Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).</span><span class="sxs-lookup"><span data-stu-id="ed0eb-135">For more information, see [Cookie sharing from Microsoft Edge to Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).</span></span>

## <a name="see-also"></a><span data-ttu-id="ed0eb-136">См. также</span><span class="sxs-lookup"><span data-stu-id="ed0eb-136">See also</span></span>

- [<span data-ttu-id="ed0eb-137">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="ed0eb-137">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="ed0eb-138">Сведения о режиме IE</span><span class="sxs-lookup"><span data-stu-id="ed0eb-138">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="ed0eb-139">Дополнительные сведения о режиме предприятия</span><span class="sxs-lookup"><span data-stu-id="ed0eb-139">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
