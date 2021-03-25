---
title: Отправка файлов cookie из Microsoft Edge в Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 12/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Как отправлять файлы cookie из Microsoft Edge в Internet Explorer '
ms.openlocfilehash: d94c1337b7a3dbee789efb16e9c8b0a5ebc2c23b
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447743"
---
# <a name="cookie-sharing-from-microsoft-edge-to-internet-explorer"></a><span data-ttu-id="a95fc-103">Отправка файлов cookie из Microsoft Edge в Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="a95fc-103">Cookie sharing from Microsoft Edge to Internet Explorer</span></span>

<span data-ttu-id="a95fc-104">В этой статье объясняется, как настроить отправку файлов cookie сеанса из процесса Microsoft Edge в процесс Internet Explorer, используя режим Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a95fc-104">This article explains explains how to configure session cookie sharing from a Microsoft Edge process to Internet Explorer process, while using Internet Explorer mode.</span></span>

> [!NOTE]
> <span data-ttu-id="a95fc-105">Эта статья относится к Microsoft Edge версии 87 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="a95fc-105">This article applies to Microsoft Edge version 87 or later.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a95fc-106">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="a95fc-106">Prerequisites</span></span>

- <span data-ttu-id="a95fc-107">Обновления Windows</span><span class="sxs-lookup"><span data-stu-id="a95fc-107">Windows updates</span></span>

  - <span data-ttu-id="a95fc-108">Windows 10 версии 2004, Windows Server версии 2004 — KB4571744 и выше</span><span class="sxs-lookup"><span data-stu-id="a95fc-108">Windows 10 version 2004, Windows Server version 2004 - KB4571744 or higher</span></span>
  - <span data-ttu-id="a95fc-109">Windows 10 версии 1909, Windows Server версии 1909 — KB4566116 и выше</span><span class="sxs-lookup"><span data-stu-id="a95fc-109">Windows 10 version 1909, Windows Server version 1909 – KB4566116 or higher</span></span>
  - <span data-ttu-id="a95fc-110">Windows 10 версии 1903, Windows Server версии 1903 — KB4566116 и выше</span><span class="sxs-lookup"><span data-stu-id="a95fc-110">Windows 10 version 1903, Windows Server version 1903 – KB4566116 or higher</span></span>
  - <span data-ttu-id="a95fc-111">Windows 10, версии 1809, Windows Server версии 1809 и Windows Server 2019 — KB4571748 и выше</span><span class="sxs-lookup"><span data-stu-id="a95fc-111">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB4571748 or higher</span></span>
  - <span data-ttu-id="a95fc-112">Windows 10 версии 1803 — KB4577032 и выше</span><span class="sxs-lookup"><span data-stu-id="a95fc-112">Windows 10 version 1803 – KB4577032 or higher</span></span>

- <span data-ttu-id="a95fc-113">Microsoft Edge версии 87 или более поздней</span><span class="sxs-lookup"><span data-stu-id="a95fc-113">Microsoft Edge version 87 or later</span></span>
- <span data-ttu-id="a95fc-114">[Режим IE,](./edge-ie-mode.md) настроенный с помощью списка сайтов в режиме предприятия</span><span class="sxs-lookup"><span data-stu-id="a95fc-114">[IE mode](./edge-ie-mode.md) configured with Enterprise Mode Site List</span></span>

## <a name="overview"></a><span data-ttu-id="a95fc-115">Обзор</span><span class="sxs-lookup"><span data-stu-id="a95fc-115">Overview</span></span>

<span data-ttu-id="a95fc-116">Распространенной конфигурацией в крупных организациях является наличие приложения, работающего на основе связи современного браузера с другим приложением, которое может быть настроено на открытие в режиме Internet Explorer с поддержкой единого входа (SSO) в рамках рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="a95fc-116">A common configuration in large organizations is to have an application that works on a modern browser link to another application, which might be configured to open in Internet Explorer mode with Single Sign On (SSO) enabled as part of the workflow.</span></span>

<span data-ttu-id="a95fc-117">По умолчанию процессы Microsoft Edge и Internet Explorer не делятся файлами cookie сеансов, что иногда может быть неудобным.</span><span class="sxs-lookup"><span data-stu-id="a95fc-117">By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this can be inconvenient in some cases.</span></span> <span data-ttu-id="a95fc-118">Например, если пользователю требуется повторно пройти проверку подлинности в режиме Internet Explorer или при выходе из сеанса Microsoft Edge требуется не выходить из сеанса в режиме Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a95fc-118">For example, when a user has to re-authenticate in Internet Explorer mode or when signing out of an Microsoft Edge session doesn’t sign out of the Internet Explorer mode session.</span></span> <span data-ttu-id="a95fc-119">В таких сценариях вы можете настроить определенный набор файлов cookie (с помощью единого входа) на отправку из Microsoft Edge в Internet Explorer, чтобы проверка подлинности выполнялась проще благодаря устранению повторной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a95fc-119">In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to re-authenticate.</span></span>

> [!NOTE]
> <span data-ttu-id="a95fc-120">Файлы cookie сеанса можно отправлять только из Microsoft Edge в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a95fc-120">Session cookies can only be shared from Microsoft Edge to Internet Explorer.</span></span> <span data-ttu-id="a95fc-121">Отправка файлов cookie в обратном направлении (из Internet Explorer в Microsoft Edge) невозможна.</span><span class="sxs-lookup"><span data-stu-id="a95fc-121">Sharing session cookies in reverse (from Internet Explorer to Microsoft Edge) isn't possible.</span></span>

## <a name="how-cookie-sharing-works"></a><span data-ttu-id="a95fc-122">Как работает отправка файлов cookie</span><span class="sxs-lookup"><span data-stu-id="a95fc-122">How cookie sharing works</span></span>

<span data-ttu-id="a95fc-123">XML-файл списка сайтов в режиме предприятия расширен для разрешения дополнительных элементов, чтобы указать файлы cookie, которые требуется отправить из сеанса Microsoft Edge в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a95fc-123">The Enterprise Mode site list XML has been extended to allow additional elements to specify cookies that need to be shared from a Microsoft Edge session with Internet Explorer.</span></span>  

<span data-ttu-id="a95fc-124">При первом создании вкладки режима Internet Explorer в сеансе Microsoft Edge все соответствующие файлы cookie становятся общими для сеанса Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a95fc-124">The first time an Internet Explorer mode tab is created in a Microsoft Edge session, all matching cookies are shared to the Internet Explorer session.</span></span> <span data-ttu-id="a95fc-125">В дальнейшем при каждом добавлении, удалении или изменении файла cookie, соответствующего правилу, он отправляется в виде обновления в сеанс Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a95fc-125">Subsequently, any time a cookie that matches a rule is added, deleted, or modified it is sent as an update to the Internet Explorer session.</span></span> <span data-ttu-id="a95fc-126">При обновлении списка сайтов набор общих файлов cookie также оценивается повторно.</span><span class="sxs-lookup"><span data-stu-id="a95fc-126">The set of shared cookies is also re-evaluated when the site list is updated.</span></span>

### <a name="updated-schema-elements"></a><span data-ttu-id="a95fc-127">Обновленные элементы схемы</span><span class="sxs-lookup"><span data-stu-id="a95fc-127">Updated schema elements</span></span>

<span data-ttu-id="a95fc-128">В таблице ниже описан элемент \<shared-cookie\>, добавленный для поддержки функции отправки файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="a95fc-128">The following table describes the \<shared-cookie\> element added to support the cookie sharing feature.</span></span>

| <span data-ttu-id="a95fc-129">Элемент</span><span class="sxs-lookup"><span data-stu-id="a95fc-129">Element</span></span>| <span data-ttu-id="a95fc-130">Описание</span><span class="sxs-lookup"><span data-stu-id="a95fc-130">Description</span></span> |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br><span data-ttu-id="a95fc-131">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="a95fc-131">OR</span></span><br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |<span data-ttu-id="a95fc-132">**(Обязательно)** Элемент \<shared-cookie\> требует как минимум атрибут *domain* (для файлов cookie домена) или *host* (для файлов cookie, предназначенных только для узла) и атрибут *name*.</span><span class="sxs-lookup"><span data-stu-id="a95fc-132">**(Required)** A \<shared-cookie\> element requires, at minimum, a *domain* (for domain cookies) or a *host* (for host-only cookies) attribute and a *name* attribute.</span></span><br><span data-ttu-id="a95fc-133">Они должны в точности совпадать с доменом и именем файла cookie соответственно.</span><span class="sxs-lookup"><span data-stu-id="a95fc-133">These must be exact matches to the cookie's domain and name respectively.</span></span> <span data-ttu-id="a95fc-134">**Обратите внимание**, что поддомены не совпадают.</span><span class="sxs-lookup"><span data-stu-id="a95fc-134">**Note** that subdomains do not match.</span></span><br><br><span data-ttu-id="a95fc-135">Атрибут *domain* используется для файлов cookie домена (начальная точка разрешена, но необязательна).</span><span class="sxs-lookup"><span data-stu-id="a95fc-135">The *domain* attribute is used for domain cookies (and a leading dot is allowed but optional).</span></span><br><span data-ttu-id="a95fc-136">Атрибут *host* используется только для файлов cookie, предназначенных для узла (начальная точка является ошибкой).</span><span class="sxs-lookup"><span data-stu-id="a95fc-136">The *host* attribute is used for host-only cookies (and a leading dot is an error).</span></span> <span data-ttu-id="a95fc-137">Указание обоих аргументов (или их отсутствие) приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="a95fc-137">Specifying neither or both will result in an error.</span></span><br><span data-ttu-id="a95fc-138">\* Файл cookie — это файл cookie домена, если домен был указан в строке файла cookie (с помощью HTTP-заголовка отклика Set-cookie или API JS document.cookie).</span><span class="sxs-lookup"><span data-stu-id="a95fc-138">\* A cookie is a domain cookie if a domain was specified in the cookie string (via HTTP Set-Cookie response header or document.cookie JS API).</span></span> <span data-ttu-id="a95fc-139">Файл cookie домена применяется к указанному домену и всем поддоменам.</span><span class="sxs-lookup"><span data-stu-id="a95fc-139">A domain cookie applies to the specified domain and all subdomains.</span></span> <span data-ttu-id="a95fc-140">Если домен не был указан в строке файла cookie, файл cookie предназначается только для узла и применяется только к определенному узлу, для которого он был настроен.</span><span class="sxs-lookup"><span data-stu-id="a95fc-140">If a domain was not specified in the cookie string, the cookie is a host-only cookie and only applies to the specific host that it was set for.</span></span> <span data-ttu-id="a95fc-141">Обратите внимание, что некоторые классы URL-адресов, такие как имена узлов из одного слова (например, http://intranetsite) и IP-адреса (например, http://10.0.0.1), могут задавать только файлы cookie, предназначенные для узла.</span><span class="sxs-lookup"><span data-stu-id="a95fc-141">Note that some classes of URLs such as single-word hostnames (e.g. http://intranetsite) and IP addresses (e.g. http://10.0.0.1) can only set host-only cookies.</span></span>    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | <span data-ttu-id="a95fc-142">**(Необязательно)** Можно указать атрибут *path*.</span><span class="sxs-lookup"><span data-stu-id="a95fc-142">**(Optional)** A *path* attribute may be specified.</span></span> <span data-ttu-id="a95fc-143">Если атрибут path не указан (или атрибут path не заполнен), все файлы cookie, совпадающие с доменом/узлом и именем, соответствуют политике независимо от пути (правило подстановочного знака).</span><span class="sxs-lookup"><span data-stu-id="a95fc-143">If no path attribute is specified (or if the path attribute is empty), any cookies matching domain/host and name match the policy, regardless of path (wildcard rule).</span></span><br><br><span data-ttu-id="a95fc-144">Если путь указан, это должно быть точное совпадение.</span><span class="sxs-lookup"><span data-stu-id="a95fc-144">If a path is specified, it must be an exact match.</span></span><br><span data-ttu-id="a95fc-145">Если файл cookie соответствует правилу с путем, оно имеет приоритет над правилом без пути.</span><span class="sxs-lookup"><span data-stu-id="a95fc-145">If a cookie matches a rule with a path, that takes precedence over a rule without a path.</span></span> |

#### <a name="sharing-example"></a><span data-ttu-id="a95fc-146">Пример отправки</span><span class="sxs-lookup"><span data-stu-id="a95fc-146">Sharing example</span></span>

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## <a name="see-also"></a><span data-ttu-id="a95fc-147">См. также</span><span class="sxs-lookup"><span data-stu-id="a95fc-147">See also</span></span>

- [<span data-ttu-id="a95fc-148">Сведения о режиме IE</span><span class="sxs-lookup"><span data-stu-id="a95fc-148">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="a95fc-149">Сведения о настраиваемых сайтах</span><span class="sxs-lookup"><span data-stu-id="a95fc-149">Configurable sites information</span></span>](./edge-learnmore-configurable-sites-ie-mode.md)
- [<span data-ttu-id="a95fc-150">Дополнительные сведения о режиме предприятия</span><span class="sxs-lookup"><span data-stu-id="a95fc-150">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="a95fc-151">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="a95fc-151">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)