---
title: Настройка сайтов в списке сайтов в режиме предприятия
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 05/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Настройка списка сайтов предприятия
ms.openlocfilehash: 9b1943e4d50dcc770b4a634b99ecbd001d1ffbcc
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447653"
---
# <a name="configure-sites-on-the-enterprise-mode-site-list"></a><span data-ttu-id="bec73-103">Настройка сайтов в списке сайтов в режиме предприятия</span><span class="sxs-lookup"><span data-stu-id="bec73-103">Configure Sites on the Enterprise Mode Site List</span></span>

<span data-ttu-id="bec73-104">В этой статье описаны изменения в списке сайтов в режиме предприятия, поддерживающем настройку режима IE в Microsoft Edge версии 77 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="bec73-104">This article describes changes to the Enterprise Mode Site List that support configuring IE mode for Microsoft Edge version 77 and later.</span></span>

<span data-ttu-id="bec73-105">Дополнительные сведения о схеме для XML-файла списка сайтов в режиме предприятия см. в статье [Руководство по схеме режима предприятия версии 2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="bec73-105">For more information on the schema for the Enterprise Mode Site List XML file, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

> [!NOTE]
> <span data-ttu-id="bec73-106">Эта статья относится к Microsoft Edge версии 77 или более поздней; каналы **Stable**, **Beta** и **Dev**.</span><span class="sxs-lookup"><span data-stu-id="bec73-106">This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.</span></span>

## <a name="updated-schema-elements"></a><span data-ttu-id="bec73-107">Обновленные элементы схемы</span><span class="sxs-lookup"><span data-stu-id="bec73-107">Updated schema elements</span></span>

<span data-ttu-id="bec73-108">В следующей таблице приводится описание элемента \<open-in app\>, добавленного в схему версии 2 режима предприятия.</span><span class="sxs-lookup"><span data-stu-id="bec73-108">The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:</span></span>

| **<span data-ttu-id="bec73-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="bec73-109">Element</span></span>** | **<span data-ttu-id="bec73-110">Описание</span><span class="sxs-lookup"><span data-stu-id="bec73-110">Description</span></span>** |
| --- | --- |
| \<open-in app="**true**"\> | <span data-ttu-id="bec73-111">Дочерний элемент, который определяет браузер, используемый для сайтов.</span><span class="sxs-lookup"><span data-stu-id="bec73-111">A child element that controls what browser is used for sites.</span></span> <span data-ttu-id="bec73-112">Этот элемент необходим для сайтов, которые должны **открываться в IE11**.</span><span class="sxs-lookup"><span data-stu-id="bec73-112">This element is required for sites that need to **open in IE11**.</span></span>|

**<span data-ttu-id="bec73-113">Пример.</span><span class="sxs-lookup"><span data-stu-id="bec73-113">Example:</span></span>**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

<span data-ttu-id="bec73-114">В следующей таблице приведены возможные значения элемента \<open-in\>.</span><span class="sxs-lookup"><span data-stu-id="bec73-114">The following table shows the possible values of the \<open-in\> element:</span></span>

| **<span data-ttu-id="bec73-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bec73-115">Value</span></span>** | **<span data-ttu-id="bec73-116">Описание</span><span class="sxs-lookup"><span data-stu-id="bec73-116">Description</span></span>** |
| --- | --- |
| **\<open-in\><span data-ttu-id="bec73-117">IE11</span><span class="sxs-lookup"><span data-stu-id="bec73-117">IE11</span></span>\</open-in\>** | <span data-ttu-id="bec73-118">Открывает сайт в режиме IE или режиме полного окна IE11.</span><span class="sxs-lookup"><span data-stu-id="bec73-118">Opens the site in IE mode or a full IE11 window.</span></span> <span data-ttu-id="bec73-119">Сведения о включении режима IE см. в статье [Настройка политик режима IE](./edge-ie-mode-policies.md)</span><span class="sxs-lookup"><span data-stu-id="bec73-119">To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)</span></span>|
| **\<open-in app="**true**"\><span data-ttu-id="bec73-120">IE11</span><span class="sxs-lookup"><span data-stu-id="bec73-120">IE11</span></span>\</open-in\>** | <span data-ttu-id="bec73-121">Открывает сайт в режиме полного окна IE11</span><span class="sxs-lookup"><span data-stu-id="bec73-121">Opens the site in a full IE11 window</span></span> |
| **\<open-in\><span data-ttu-id="bec73-122">MSEdge</span><span class="sxs-lookup"><span data-stu-id="bec73-122">MSEdge</span></span>\</open-in\>** | <span data-ttu-id="bec73-123">Открывает сайт в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bec73-123">Opens the site in Microsoft Edge</span></span> |
| **\<open-in\><span data-ttu-id="bec73-124">Нет или не указано</span><span class="sxs-lookup"><span data-stu-id="bec73-124">None or not specified</span></span>\</open-in\>** | <span data-ttu-id="bec73-125">Открывает сайт в браузере по умолчанию или браузере, в котором пользователь перешел к сайту.</span><span class="sxs-lookup"><span data-stu-id="bec73-125">Opens the site in the default browser or in the browser where the user navigated to the site.</span></span> |
|**\<open-in\><span data-ttu-id="bec73-126">Возможность настройки</span><span class="sxs-lookup"><span data-stu-id="bec73-126">Configurable</span></span>\</open-in\>** | <span data-ttu-id="bec73-127">Позволяет сайту участвовать в определении подсистемы режима IE.</span><span class="sxs-lookup"><span data-stu-id="bec73-127">Allows the site to participate in IE mode engine determination.</span></span> <span data-ttu-id="bec73-128">Дополнительные сведения см. в статье [Настраиваемые сайты в режиме IE](edge-learnmore-configurable-sites-ie-mode.md).</span><span class="sxs-lookup"><span data-stu-id="bec73-128">To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).</span></span>  |

>[!NOTE]
> <span data-ttu-id="bec73-129">Атрибут app=**"true"** распознается только в том случае, если он связан со значением _'open-in' IE11_.</span><span class="sxs-lookup"><span data-stu-id="bec73-129">The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_.</span></span> <span data-ttu-id="bec73-130">Добавление его в другие элементы 'open-in' не приведет к изменению поведения браузера.</span><span class="sxs-lookup"><span data-stu-id="bec73-130">Adding it to the other 'open-in' elements won't change browser behavior.</span></span>   

## <a name="configure-neutral-sites"></a><span data-ttu-id="bec73-131">Настройка нейтральных сайтов</span><span class="sxs-lookup"><span data-stu-id="bec73-131">Configure neutral sites</span></span>

<span data-ttu-id="bec73-132">Чтобы режим IE работал правильно, требуется явным образом настроить серверы проверки подлинности и единого входа в качестве нейтральных сайтов.</span><span class="sxs-lookup"><span data-stu-id="bec73-132">In order for IE mode to work properly, authentication / Single Sign-On servers will need to be explicitly configured as neutral sites.</span></span> <span data-ttu-id="bec73-133">В противном случае страницы в режиме IE попытаются выполнить перенаправление в Microsoft Edge, и проверка подлинности завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="bec73-133">Otherwise, IE mode pages will try to redirect to Microsoft Edge, and authentication will fail.</span></span>

<span data-ttu-id="bec73-134">Нейтральный сайт будет использовать браузер, в котором начат переход: Microsoft Edge или режим IE.</span><span class="sxs-lookup"><span data-stu-id="bec73-134">A neutral site will use the browser where the navigation started - either Microsoft Edge or IE mode.</span></span> <span data-ttu-id="bec73-135">Настройка нейтральных сайтов гарантирует, что все приложения, использующие эти серверы проверки подлинности (современные и устаревшие), продолжат работать.</span><span class="sxs-lookup"><span data-stu-id="bec73-135">Configuring neutral sites ensures that all applications using these authentication servers, both modern and legacy, continue to work.</span></span>

<span data-ttu-id="bec73-136">Вы можете настроить нейтральные сайты, выбрав "Нет" в раскрывающемся списке *Открыть в* инструмента Enterprise Mode Site List Manager или непосредственно обновив XML-файл списка сайтов:</span><span class="sxs-lookup"><span data-stu-id="bec73-136">You can configure neutral sites by setting the *Open In* dropdown to 'None' in the Enterprise Mode Site List Manager tool or by directly updating the site list XML:</span></span>

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

<span data-ttu-id="bec73-137">Чтобы определить серверы проверки подлинности, проверьте сетевой трафик из приложении с помощью средств разработчика IE11.</span><span class="sxs-lookup"><span data-stu-id="bec73-137">To identify authentication servers, inspect the network traffic from an application using the IE11 Developer Tools.</span></span> <span data-ttu-id="bec73-138">Если вам требуется больше времени, чтобы определить серверы проверки подлинности, можно настроить политику, сохраняющую для всех переходов в пределах страницы применение режима IE.</span><span class="sxs-lookup"><span data-stu-id="bec73-138">If you need more time to identify your authentication servers, you can configure a policy to keep all in-page navigation in IE mode.</span></span> <span data-ttu-id="bec73-139">Чтобы свести к минимуму использование режима IE, отключите этот параметр после определения и добавления серверов проверки подлинности в список сайтов.</span><span class="sxs-lookup"><span data-stu-id="bec73-139">To minimize the use of IE mode, disable this setting once you've identified and added your authentication servers to the site list.</span></span> <span data-ttu-id="bec73-140">Дополнительные сведения см. в разделе [Настройка переходов в пределах страницы для их сохранения в режиме IE](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect).</span><span class="sxs-lookup"><span data-stu-id="bec73-140">For more information, see [Configure in-page navigation to remain in IE mode](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect).</span></span>

>[!NOTE]
   ><span data-ttu-id="bec73-141">Схема режима предприятия версии 1 не поддерживается для интеграции с режимом IE.</span><span class="sxs-lookup"><span data-stu-id="bec73-141">Enterprise Mode schema v.1 isn't supported for IE mode integration.</span></span> <span data-ttu-id="bec73-142">Если вы используете схему версии 1 в Internet Explorer 11, необходимо обновить схему до версии 2.</span><span class="sxs-lookup"><span data-stu-id="bec73-142">If you are currently using schema v.1 with Internet Explorer 11, you must upgrade to schema v.2.</span></span> <span data-ttu-id="bec73-143">Дополнительные сведения см. в разделе [Руководство схеме версии 2 в режиме предприятия](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span><span class="sxs-lookup"><span data-stu-id="bec73-143">For more information, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

## <a name="see-also"></a><span data-ttu-id="bec73-144">См. также</span><span class="sxs-lookup"><span data-stu-id="bec73-144">See also</span></span>

- [<span data-ttu-id="bec73-145">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="bec73-145">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="bec73-146">Сведения о режиме IE</span><span class="sxs-lookup"><span data-stu-id="bec73-146">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="bec73-147">Дополнительные сведения о режиме предприятия</span><span class="sxs-lookup"><span data-stu-id="bec73-147">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)