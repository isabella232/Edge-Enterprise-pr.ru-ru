---
title: Параметры прокси-сервера Microsoft Edge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 'Использование параметров командной строки для настройки параметров прокси-сервера '
ms.openlocfilehash: 99a5f0776ea42f1e26050e0d30adb48a63907b8c
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642165"
---
# <a name="how-to-use-microsoft-edge-command-line-options-to-configure-proxy-settings"></a><span data-ttu-id="ed6bf-103">Использование параметров командной строки в Microsoft Edge для настройки параметров прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="ed6bf-103">How to use Microsoft Edge command-line options to configure proxy settings</span></span>

<span data-ttu-id="ed6bf-104">В этой статье описано, как использовать параметры командной строки для переопределения стандартных параметров сети системы.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-104">This article describes how you can use command-line options to override the default system network settings.</span></span>

>[!NOTE]
><span data-ttu-id="ed6bf-105">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="system-network-settings"></a><span data-ttu-id="ed6bf-106">Параметры сети системы</span><span class="sxs-lookup"><span data-stu-id="ed6bf-106">System network settings</span></span>

<span data-ttu-id="ed6bf-107">По умолчанию в сетевом стеке Microsoft Edge используются параметры сети системы.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-107">The Microsoft Edge network stack uses the system network settings by default.</span></span> <span data-ttu-id="ed6bf-108">К этим параметрам относятся *параметры прокси-сервера* и *хранилища сертификатов и закрытых ключей*.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-108">These settings include *proxy settings*, and *certificate and private key stores*.</span></span>

<span data-ttu-id="ed6bf-109">Бывают случаи, когда пользователи запрашивают альтернативу использованию параметров прокси-сервера, заданных по умолчанию в системе.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-109">There are scenarios where users request an alternative to using the system's default proxy settings.</span></span> <span data-ttu-id="ed6bf-110">Эти сценарии реализуются в Microsoft Edge за счет поддержки браузером параметров командной строки, которые можно использовать для задания пользовательских параметров прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-110">To support these scenarios, Microsoft Edge supports command-line options that you can use to configure custom proxy settings.</span></span>

<span data-ttu-id="ed6bf-111">Эти параметры командной строки соответствуют следующим политикам в группе **Прокси-сервер**:</span><span class="sxs-lookup"><span data-stu-id="ed6bf-111">These command-line options correspond to the following policies in the **Proxy server** group:</span></span>

- [<span data-ttu-id="ed6bf-112">ProxyBypassList</span><span class="sxs-lookup"><span data-stu-id="ed6bf-112">ProxyBypassList</span></span>](./microsoft-edge-policies.md#proxybypasslist)
- [<span data-ttu-id="ed6bf-113">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="ed6bf-113">ProxyMode</span></span>](./microsoft-edge-policies.md#proxymode)
- [<span data-ttu-id="ed6bf-114">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="ed6bf-114">ProxyPacUrl</span></span>](./microsoft-edge-policies.md#proxypacurl)
- [<span data-ttu-id="ed6bf-115">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="ed6bf-115">ProxyServer</span></span>](./microsoft-edge-policies.md#proxyserver)
- [<span data-ttu-id="ed6bf-116">ProxySettings</span><span class="sxs-lookup"><span data-stu-id="ed6bf-116">ProxySettings</span></span>](./microsoft-edge-policies.md#proxysettings)

## <a name="command-line-options-for-proxy-settings"></a><span data-ttu-id="ed6bf-117">Параметры командной строки для параметров прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="ed6bf-117">Command-line options for proxy settings</span></span>

<span data-ttu-id="ed6bf-118">Microsoft Edge поддерживает следующие параметры командной строки, связанные с прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-118">Microsoft Edge supports the following proxy-related command-line options.</span></span>

 **`--no-proxy-server`**
 
<span data-ttu-id="ed6bf-119">Сообщает Microsoft Edge не использовать прокси-сервер, даже если система настроена на использование одного из них.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-119">Tells Microsoft Edge not to use a Proxy, even if the system is otherwise configured to use one.</span></span> <span data-ttu-id="ed6bf-120">Переопределяет любые другие предоставленные параметры прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-120">It overrides any other proxy settings that are provided.</span></span>

**`--proxy-auto-detect`**

<span data-ttu-id="ed6bf-121">Сообщает Microsoft Edge выполнить попытку автоматического удаления конфигурации прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-121">Tells Microsoft Edge to try and automatically detect your proxy configuration.</span></span> <span data-ttu-id="ed6bf-122">Этот аргумент игнорируется, если настроен `--proxy-server`.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-122">This argument is ignored if `--proxy-server` is configured.</span></span>

**`--proxy-server=<scheme>=<uri>[:<port>][;...] | <uri>[:<port>] | "direct://"`**

<span data-ttu-id="ed6bf-123">Сообщает Microsoft Edge использовать настраиваемую конфигурацию прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-123">Tells Microsoft Edge to use a custom proxy configuration.</span></span> <span data-ttu-id="ed6bf-124">Задать настраиваемую конфигурацию прокси-сервера можно тремя способами.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-124">You can specify a custom proxy configuration in three ways.</span></span>

1. <span data-ttu-id="ed6bf-125">Предоставьте разделенный точкой с запятой файл сопоставления схемы списка с парами URL-адреса/порты.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-125">Provide a semicolon-separated mapping of list scheme to url/port pairs.</span></span> <span data-ttu-id="ed6bf-126">Например, `--proxy-server="http=proxy1:8080;ftp=ftpproxy"` сообщает Microsoft Edge использовать прокси-сервер HTTP типа "proxy1:8080" для URL-адресов "http" и прокси-сервер HTTP типа "ftpproxy:80" для URL-адресов "ftp".</span><span class="sxs-lookup"><span data-stu-id="ed6bf-126">For example, `--proxy-server="http=proxy1:8080;ftp=ftpproxy"` tells Microsoft Edge to use HTTP proxy "proxy1:8080" for http URLs and HTTP proxy "ftpproxy:80" for ftp URLs.</span></span>
2. <span data-ttu-id="ed6bf-127">Предоставьте один универсальный код ресурса с необязательным портом для использования во всех URL-адресах.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-127">By providing a single uri with optional port to use for all URLs.</span></span> <span data-ttu-id="ed6bf-128">Например, `--proxy-server="proxy2:8080"` будет использовать прокси-сервер по адресу "proxy2:8080" для всего трафика.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-128">For example, `--proxy-server="proxy2:8080"` will use the proxy at "proxy2:8080" for all traffic.</span></span>
3. <span data-ttu-id="ed6bf-129">С помощью специального значения "direct://".</span><span class="sxs-lookup"><span data-stu-id="ed6bf-129">By using the special "direct://" value.</span></span> <span data-ttu-id="ed6bf-130">Например, при использовании `--proxy-server="direct://"` все подключения не будут использовать прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-130">For example, `--proxy-server="direct://"` will make all connections not use a proxy.</span></span> 

>[!NOTE]
><span data-ttu-id="ed6bf-131">Можно настроить, чтобы Microsoft Edge пытался использовать прокси-сервер и в случае его недоступности переходил к прямому подключению.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-131">You can configure Microsoft Edge to try using a proxy and fallback to going direct if the proxy isn't available.</span></span> <span data-ttu-id="ed6bf-132">Например, `--proxy-server="http://proxy2:8080,direct://`.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-132">For example, `--proxy-server="http://proxy2:8080,direct://`.</span></span>

**`--proxy-bypass-list=(<trailing_domain>|<ip-address>)[:<port>][;...]`**

<span data-ttu-id="ed6bf-133">Сообщает Microsoft Edge обходить любой прокси-сервер заданный для списка узлов, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-133">Tells Microsoft Edge to bypass any specified proxy for the specified semicolon-separated list of hosts.</span></span> <span data-ttu-id="ed6bf-134">Этот флаг необходимо использовать с `--proxy-server`.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-134">This flag must be used with `--proxy-server`.</span></span>

>[!NOTE]
><span data-ttu-id="ed6bf-135">При сопоставлении доменов не требуются разделители в виде точки ".". Запрос "\*microsoft.com" будет сопоставлен с "imicrosoft.com".</span><span class="sxs-lookup"><span data-stu-id="ed6bf-135">Trailing-domain matching doesn't require "." separators, "\*microsoft.com" will match "imicrosoft.com".</span></span> <span data-ttu-id="ed6bf-136">Например, `--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` будет использовать прокси-сервер "proxy2" на порте 8080 для всех узлов, кроме запросов для \*.microsoft.com, example.com и 127.0.0.1 на порте 8080.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-136">For example, `--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` will use the proxy server "proxy2" on port 8080 for all hosts except requests for \*.microsoft.com, example.com, and 127.0.0.1 on port 8080.</span></span> <span data-ttu-id="ed6bf-137">В предыдущем примере запросы imicrosoft.com будут все равно передаваться через прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-137">In the previous example, imicrosoft.com requests will still be proxied.</span></span> <span data-ttu-id="ed6bf-138">Однако запросы iexample.com будут обходить прокси-сервер, так как вместо \*.example.com был указан запрос \*example.com.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-138">However, iexample.com requests will bypass the proxy because \*example.com was specified instead of \*.example.com.</span></span>

**`--proxy-pac-url=<pac-file-url>`**

<span data-ttu-id="ed6bf-139">Сообщает Microsoft Edge использовать PAC-файл по указанному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-139">Tells Microsoft Edge to use the PAC file at the specified URL.</span></span> <span data-ttu-id="ed6bf-140">Например, `--proxy-pac-url="https://wpad/proxy.pac"` сообщает Microsoft Edge разрешать данные прокси для URL-запросов, используя файл **proxy.pac**.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-140">For example, `--proxy-pac-url="https://wpad/proxy.pac"` tells Microsoft Edge to resolve proxy information for URL requests using the **proxy.pac** file.</span></span>

## <a name="content-license"></a><span data-ttu-id="ed6bf-141">Лицензия на содержимое</span><span class="sxs-lookup"><span data-stu-id="ed6bf-141">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="ed6bf-142">Некоторые части этой страницы представляют собой измененные материалы, созданные и предоставленные на сайте Chromium.org. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span><span class="sxs-lookup"><span data-stu-id="ed6bf-142">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="ed6bf-143">Исходная страница Chromium находится [здесь](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).</span><span class="sxs-lookup"><span data-stu-id="ed6bf-143">The original page can be found [here](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="ed6bf-144">Эта работа предоставляется в рамках международной лицензии <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-144">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed6bf-145">См. также</span><span class="sxs-lookup"><span data-stu-id="ed6bf-145">See also</span></span>

- <span data-ttu-id="ed6bf-146">Сведения о расширенных параметрах конфигурации и дополнительных параметрах см. в [документации по прокси-серверу](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md) в проекте с открытым исходным кодом Chromium.</span><span class="sxs-lookup"><span data-stu-id="ed6bf-146">To see advanced configuration settings and additional options, consult the [proxy documentation](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md) in the Chromium Open Source project.</span></span>
- [<span data-ttu-id="ed6bf-147">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="ed6bf-147">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)