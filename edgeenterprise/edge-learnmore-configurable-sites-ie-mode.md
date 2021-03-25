---
title: Microsoft Edge и настраиваемые сайты в режиме IE
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/28/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge и настраиваемые сайты в режиме IE
ms.openlocfilehash: 1bffdef8c88b7a83d999b29763fcca258102ed51
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447333"
---
# <a name="learn-about-configurable-sites-in-ie-mode"></a><span data-ttu-id="a6ae1-103">Сведения о настраиваемых сайтах в режиме IE</span><span class="sxs-lookup"><span data-stu-id="a6ae1-103">Learn about Configurable sites in IE mode</span></span>

<span data-ttu-id="a6ae1-104">В этой статье рассматривается функция настраиваемых сайтов для списка сайтов режима предприятия в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-104">This article explains the Configurable sites feature of the Enterprise Mode Site List when using IE mode in Microsoft Edge.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a6ae1-105">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="a6ae1-105">Prerequisites</span></span>

- <span data-ttu-id="a6ae1-106">Обновления Windows</span><span class="sxs-lookup"><span data-stu-id="a6ae1-106">Windows updates</span></span>

  - <span data-ttu-id="a6ae1-107">Windows10 версии 1909, Windows server версии 1909 — KB4550945 и выше</span><span class="sxs-lookup"><span data-stu-id="a6ae1-107">Windows 10 version 1909, Windows server version 1909 – KB4550945  or higher</span></span>
  - <span data-ttu-id="a6ae1-108">Windows10 версии 1903, Windows server версии 1903 — KB4550945 и выше</span><span class="sxs-lookup"><span data-stu-id="a6ae1-108">Windows 10 version 1903, Windows server version 1903 – KB4550945  or higher</span></span>
  - <span data-ttu-id="a6ae1-109">Windows 10, версии 1809, Windows Server версии 1809 и Windows Server 2019: обновление — KB4550969 и выше</span><span class="sxs-lookup"><span data-stu-id="a6ae1-109">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB4550969 or higher</span></span>
  - <span data-ttu-id="a6ae1-110">Windows 10 версии 1803 — KB4550944 и выше</span><span class="sxs-lookup"><span data-stu-id="a6ae1-110">Windows 10 version 1803 – KB4550944 or higher</span></span>
  - <span data-ttu-id="a6ae1-111">Windows 10 версии 1607, Windows Server 2016 — KB4556826 и выше</span><span class="sxs-lookup"><span data-stu-id="a6ae1-111">Windows 10 version 1607, Windows Server 2016 - KB4556826 or higher</span></span>
  - <span data-ttu-id="a6ae1-112">Первоначальная версия Windows 10 за июль 2015 — KB4550947 и выше</span><span class="sxs-lookup"><span data-stu-id="a6ae1-112">Windows 10 initial version, July 2015 - KB4550947 or higher</span></span>
  - <span data-ttu-id="a6ae1-113">Windows 8.1 — KB4556798 и выше</span><span class="sxs-lookup"><span data-stu-id="a6ae1-113">Windows 8.1 – KB4556798 or higher</span></span>

- <span data-ttu-id="a6ae1-114">Microsoft Edge версии 83 или более ранней</span><span class="sxs-lookup"><span data-stu-id="a6ae1-114">Microsoft Edge version 83 or later</span></span>
- <span data-ttu-id="a6ae1-115">[Режим IE](./edge-ie-mode.md) настроенный с помощью списка сайтов в режиме предприятия</span><span class="sxs-lookup"><span data-stu-id="a6ae1-115">[IE mode](./edge-ie-mode.md) configured with Enterprise Mode Site List</span></span>

## <a name="overview"></a><span data-ttu-id="a6ae1-116">Обзор</span><span class="sxs-lookup"><span data-stu-id="a6ae1-116">Overview</span></span>

<span data-ttu-id="a6ae1-117">Настройка сайтов, которым требуется режим IE, в списке сайтов режима предприятия будет хорошо работать для большинства сред с устаревшими приложениями.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-117">Configuring sites needing IE mode in the Enterprise Mode Site List will work well for most environments with legacy applications.</span></span> <span data-ttu-id="a6ae1-118">В некоторых случаях это не самый лучший подход для настройки подмножества сайтов на открытие в режиме IE без обработки всего домена в этом режиме.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-118">However, in some cases this approach isn't the best to configure a subset of sites to open in IE mode without rendering an entire domain in IE mode.</span></span> <span data-ttu-id="a6ae1-119">Например, если в вашей среде есть современные и устаревшие приложения, запущенные на одном сервере, и вы хотите обрабатывать устаревшие приложения в режиме IE, а остальные — в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-119">For example, when your environment contains both modern and legacy applications running on a single server and you would like the flexibility to render only the legacy applications in IE mode and the remaining applications to render in Microsoft Edge mode.</span></span>

<span data-ttu-id="a6ae1-120">Решением является использование функции настраиваемых сайтов списка сайтов в режиме предприятия.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-120">The solution is to use the Configurable sites feature of the Enterprise Mode Site List.</span></span> <span data-ttu-id="a6ae1-121">Если эта функция включена, Microsoft Edge позволяет сайтам с тегом "конфигурируемый" участвовать в определении подсистемы режима IE.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-121">When the feature is enabled, Microsoft Edge will allow sites with the "configurable" tag to participate in IE mode engine determination.</span></span>

## <a name="how-configurable-sites-works"></a><span data-ttu-id="a6ae1-122">Принципы работы настраиваемых сайтов в режиме IE</span><span class="sxs-lookup"><span data-stu-id="a6ae1-122">How Configurable sites works</span></span>

### <a name="automatic-switching-from-the-microsoft-edge-engine-to-the-ie-mode-engine"></a><span data-ttu-id="a6ae1-123">Автоматическое переключение с подсистемы Microsoft Edge на подсистему режима IE</span><span class="sxs-lookup"><span data-stu-id="a6ae1-123">Automatic switching from the Microsoft Edge engine to the IE mode engine</span></span>

<span data-ttu-id="a6ae1-124">Для использования функции настраиваемых сайтов потребуется один или несколько сайтов в списке сайтов режима предприятия, чтобы использовать `<open-in>Configurable</open-in>`.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-124">To use the Configurable sites feature, you'll need one or more sites in the Enterprise Mode Site List to have the `<open-in>Configurable</open-in>` option.</span></span>

<span data-ttu-id="a6ae1-125">Пример.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-125">Example:</span></span>

```
<site-list version="1">
  <site url="app.com">
    <open-in>Configurable</open-in>
  </site>
</site-list>
```

<span data-ttu-id="a6ae1-126">Если включена функция настраиваемых сайтов, возникает следующее поведение:</span><span class="sxs-lookup"><span data-stu-id="a6ae1-126">When the Configurable sites feature is enabled, the following behavior occurs:</span></span>

1. <span data-ttu-id="a6ae1-127">При создании запроса на настраиваемый сайт, Microsoft Edge отправляет заголовок запроса HTTP "`X-InternetExplorerModeConfigurable: 1`".</span><span class="sxs-lookup"><span data-stu-id="a6ae1-127">When making a request to a Configurable site, Microsoft Edge will send the HTTP request header "`X-InternetExplorerModeConfigurable: 1`".</span></span>
2. <span data-ttu-id="a6ae1-128">Настраиваемый сайт может отправлять ответ перенаправления (например, HTTP 302) с помощью заголовка ответа HTTP "`X-InternetExplorerMode: 1`", чтобы запросить Microsoft Edge загружать веб-сайт в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-128">A Configurable site may send a redirect response (for example, HTTP 302) with the HTTP response header "`X-InternetExplorerMode: 1`" to request that Microsoft Edge loads the site in IE mode.</span></span>
3. <span data-ttu-id="a6ae1-129">Целью перенаправления (т. е. значение заголовка ответа **Расположение**) также должен быть **Настраиваемый** или **Нейтральный** сайт, в противном случае заголовок ответа в режиме IE будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-129">The target of the redirect (that is, the value of the **Location** response header) must also be a **Configurable** or **Neutral** site, otherwise the IE mode response header will be ignored.</span></span> <span data-ttu-id="a6ae1-130">Предполагается, что цель перенаправления, как правило, совпадает с исходным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-130">It's expected that the target of the redirect will usually be the same as the original URL.</span></span> <span data-ttu-id="a6ae1-131">Но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-131">However, it doesn't have to be.</span></span>

   > [!NOTE]
   > <span data-ttu-id="a6ae1-132">Ответ перенаправления подлежит кэшированию в соответствии с обычным режимом кэширования HTTP в Microsoft Edge для перенаправлений.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-132">The redirect response is subject to caching according to Microsoft Edge's normal HTTP caching behavior for redirects.</span></span>

### <a name="switching-back-from-ie-mode-engine-to-microsoft-edge-engine"></a><span data-ttu-id="a6ae1-133">Переключение с ядра подсистемы режима IE на подсистему Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a6ae1-133">Switching back from IE mode engine to Microsoft Edge engine</span></span>

<span data-ttu-id="a6ae1-134">Включение настраиваемых сайтов в Microsoft Edge автоматически включает следующие варианты поведения во вкладках режима IE:</span><span class="sxs-lookup"><span data-stu-id="a6ae1-134">Enabling Configurable sites in Microsoft Edge automatically enables the following behaviors in IE mode tabs:</span></span>

1. <span data-ttu-id="a6ae1-135">При создании запроса на настраиваемый сайт, вкладки режима IE отправляют заголовок запроса HTTP "`X-InternetExplorerModeConfigurable: 1`", так же как вкладки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-135">When making a request to a Configurable site, IE mode tabs will send the HTTP request header "`X-InternetExplorerModeConfigurable: 1`", the same as Microsoft Edge tabs.</span></span>
2. <span data-ttu-id="a6ae1-136">Настраиваемый сайт может отправлять ответ перенаправления (например, HTTP 302) с помощью заголовка ответа HTTP "`X-InternetExplorerMode: 0`", чтобы запросить переключение на режим Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-136">A Configurable site might send a redirect response (for example, HTTP 302) with the HTTP response header "`X-InternetExplorerMode: 0`" to request that the navigation switch back to Microsoft Edge mode.</span></span>
3. <span data-ttu-id="a6ae1-137">Целью перенаправления (т. е. значение заголовка ответа **Расположение**) также должен быть **Настраиваемый** или **Нейтральный** сайт, в противном случае заголовок ответа в режиме IE будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-137">The target of the redirect (that is, the value of the **Location** response header) must also be a **Configurable** or **Neutral** site, otherwise the IE mode response header will be ignored.</span></span> <span data-ttu-id="a6ae1-138">Предполагается, что цель перенаправления, как правило, совпадает с исходным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-138">It's expected that the target of the redirect will usually be the same as the original URL.</span></span> <span data-ttu-id="a6ae1-139">Но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-139">However, it doesn't have to be.</span></span>

   > [!NOTE]
   > <span data-ttu-id="a6ae1-140">Ответ перенаправления подлежит кэшированию в соответствии с обычным режимом кэширования HTTP в Microsoft Edge для перенаправлений.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-140">The redirect response is subject to caching according to Microsoft Edge's normal HTTP caching behavior for redirects.</span></span>

> [!TIP]
> <span data-ttu-id="a6ae1-141">Обе подсистемы браузеров отправляют одинаковый заголовок запроса "`X-InternetExplorerModeConfigurable: 1`" на настраиваемые сайты.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-141">Both browser engines send the same "`X-InternetExplorerModeConfigurable: 1`" request header to Configurable sites.</span></span> <span data-ttu-id="a6ae1-142">Необходимо использовать заголовок запроса User-Agent для различия запросов в режиме Microsoft Edge и в режиме IE, чтобы избежать перенаправления, если сайт уже загружен в нужной системе.</span><span class="sxs-lookup"><span data-stu-id="a6ae1-142">You should use the User-Agent request header to distinguish between requests from Microsoft Edge mode vs. IE mode to avoid redirecting when the site is already loading in the correct engine.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6ae1-143">См. также</span><span class="sxs-lookup"><span data-stu-id="a6ae1-143">See also</span></span>

- [<span data-ttu-id="a6ae1-144">Сведения о режиме IE</span><span class="sxs-lookup"><span data-stu-id="a6ae1-144">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="a6ae1-145">Дополнительные сведения о режиме предприятия</span><span class="sxs-lookup"><span data-stu-id="a6ae1-145">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="a6ae1-146">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="a6ae1-146">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)