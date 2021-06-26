---
title: Формат фильтрации для политик URL-адресов Microsoft Edge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Сведения о формате фильтрации, используемом для политик URLBlocklist и URLAllowlist в Microsoft Edge.
ms.openlocfilehash: 94378a9193269c73a7439dd019d6cb2d6ac547df
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617269"
---
# <a name="filter-format-for-url-list-based-policies"></a><span data-ttu-id="3ec2f-103">Формат фильтрации для политик на основе списка URL-адресов</span><span class="sxs-lookup"><span data-stu-id="3ec2f-103">Filter format for URL list-based policies</span></span>

<span data-ttu-id="3ec2f-104">В этой статье описывается формат фильтрации, используемый для политик на основе списка URL-адресов Microsoft Edge (например, [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist) и [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls).</span><span class="sxs-lookup"><span data-stu-id="3ec2f-104">This article describes the filter format used for the Microsoft Edge URL list-based policies (For example, [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist), and [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls) policies.</span></span>

> [!NOTE]
> <span data-ttu-id="3ec2f-105">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="the-filter-format"></a><span data-ttu-id="3ec2f-106">Формат фильтрации</span><span class="sxs-lookup"><span data-stu-id="3ec2f-106">The filter format</span></span>

<span data-ttu-id="3ec2f-107">Используется следующий формат фильтрации:</span><span class="sxs-lookup"><span data-stu-id="3ec2f-107">The filter format is:</span></span>

```
    [scheme://][.]host[:port][/path][@query]
```

<span data-ttu-id="3ec2f-108">Поля в формате фильтрации:</span><span class="sxs-lookup"><span data-stu-id="3ec2f-108">The fields in the filter format are:</span></span>

| <span data-ttu-id="3ec2f-109">Поле</span><span class="sxs-lookup"><span data-stu-id="3ec2f-109">Field</span></span> | <span data-ttu-id="3ec2f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="3ec2f-110">Description</span></span> |
| --- | --- |
| <span data-ttu-id="3ec2f-111">**схема** (*необязательно*)</span><span class="sxs-lookup"><span data-stu-id="3ec2f-111">**scheme** (*optional*)</span></span> | <span data-ttu-id="3ec2f-112">Это может быть http://, https://, ftp://, edge:// и т. д.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-112">It can be http://, https://, ftp://, edge://, etc.</span></span> |
| <span data-ttu-id="3ec2f-113">**узел** (*обязательно*)</span><span class="sxs-lookup"><span data-stu-id="3ec2f-113">**host** (*required*)</span></span> | <span data-ttu-id="3ec2f-114">Это должно быть действительное имя узла. Также можно использовать подстановочный знак ("\*").</span><span class="sxs-lookup"><span data-stu-id="3ec2f-114">It must be a valid host name and you can use a wildcard ("\*").</span></span> <span data-ttu-id="3ec2f-115">Для отключения сопоставления дочерних доменов добавьте необязательную точку (".") перед **узлом**.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-115">To disable subdomain matching, include an optional dot (".") before **host**.</span></span> <span data-ttu-id="3ec2f-116">Можно указать имя узла литерала IP-адреса, но подстановочные знаки не поддерживаются для имени узла литерала IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-116">A single IP Address Literal hostname may be specified, but wildcarding is not supported for an IP Address Literal hostname.</span></span> |
| <span data-ttu-id="3ec2f-117">**порт** (*необязательно*)</span><span class="sxs-lookup"><span data-stu-id="3ec2f-117">**port** (*optional*)</span></span> | <span data-ttu-id="3ec2f-118">Допускаются значения в диапазоне от 1 до 65535.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-118">Valid values range from 1 to 65535.</span></span> |
| <span data-ttu-id="3ec2f-119">**путь** (*необязательно*)</span><span class="sxs-lookup"><span data-stu-id="3ec2f-119">**path** (*optional*)</span></span> | <span data-ttu-id="3ec2f-120">В пути можно использовать любую строку.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-120">You can use any string in the path.</span></span> |
| <span data-ttu-id="3ec2f-121">**запрос** (*необязательно*)</span><span class="sxs-lookup"><span data-stu-id="3ec2f-121">**query** (*optional*)</span></span> | <span data-ttu-id="3ec2f-122">**Запрос** — это маркеры типа "ключ-значение" или "ключ", разделенные амперсандом ("&").</span><span class="sxs-lookup"><span data-stu-id="3ec2f-122">The **query** is either key-value or key-only tokens separated by an ampersand ("&").</span></span> <span data-ttu-id="3ec2f-123">Маркеры типа "ключ-значение" следует разделять знаком равенства ("=").</span><span class="sxs-lookup"><span data-stu-id="3ec2f-123">Separate key-value tokens with an equal sign ("=").</span></span> <span data-ttu-id="3ec2f-124">Чтобы обозначить сопоставление префиксов, можно использовать звездочку ("\*") в конце **запроса**.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-124">To indicate a prefix match, you can use an asterisk ("\*") at the end of the **query**.</span></span> |

## <a name="comparing-the-filter-format-to-the-url-format"></a><span data-ttu-id="3ec2f-125">Сравнение формата фильтрации с форматом URL-адреса</span><span class="sxs-lookup"><span data-stu-id="3ec2f-125">Comparing the filter format to the URL format</span></span>

<span data-ttu-id="3ec2f-126">Формат фильтрации похож на формат URL-адреса, за исключением следующих различий:</span><span class="sxs-lookup"><span data-stu-id="3ec2f-126">The filter format resembles the URL format, except for the following differences:</span></span>

- <span data-ttu-id="3ec2f-127">При добавлении элемента "user:pass" он будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-127">If you include "user:pass", it will be ignored.</span></span> <span data-ttu-id="3ec2f-128">Например, http://user:pass@ftp.contoso.com/pub/example.iso.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-128">For example, http://user:pass@ftp.contoso.com/pub/example.iso.</span></span>
- <span data-ttu-id="3ec2f-129">При добавлении идентификатора фрагмента ("#") он и все следующие за ним элементы игнорируются.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-129">If you include a fragment identifier ("#"), it and everything that follows the identifier is ignored.</span></span>
- <span data-ttu-id="3ec2f-130">В качестве **узла** можно использовать подстановочный знак ("\*"). Перед ним можно поставить точку (".").</span><span class="sxs-lookup"><span data-stu-id="3ec2f-130">You can use a wildcard ("\*") as the **host** and you can prefix it with a dot (".").</span></span>
- <span data-ttu-id="3ec2f-131">В качестве суффикса **узла**можно использовать косую черту ("/") или точку (".").</span><span class="sxs-lookup"><span data-stu-id="3ec2f-131">You can use a forward slash ("/") or a dot (".") as a suffix for the **host**.</span></span> <span data-ttu-id="3ec2f-132">В этом случае суффикс игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-132">In this case, the suffix is ignored.</span></span>

## <a name="filter-selection-criteria"></a><span data-ttu-id="3ec2f-133">Условия выбора фильтра</span><span class="sxs-lookup"><span data-stu-id="3ec2f-133">Filter selection criteria</span></span>

<span data-ttu-id="3ec2f-134">Выбранный для URL-адреса фильтр — это наиболее точное совпадение, находимое после обработки следующих правил выбора фильтра.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-134">The filter selected for a URL is the most specific match found after processing the following filter selection rules:</span></span>

1. <span data-ttu-id="3ec2f-135">Сначала выбираются фильтры самым длинным совпадением **узла**.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-135">Filters with the longest **host** match are selected first.</span></span>
2. <span data-ttu-id="3ec2f-136">Из выбранных фильтров все фильтры с несовпадающими схемами или портами отклоняются.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-136">From the selected filters, any filter with a non-matching scheme or port is discarded.</span></span>
3. <span data-ttu-id="3ec2f-137">Из оставшихся фильтров выбирается фильтр с самым длинным совпадающим **путем**.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-137">From the remaining filters, the filter with the longest matching **path** is selected.</span></span>
4. <span data-ttu-id="3ec2f-138">Из оставшихся фильтров выбирается фильтр с самым длинным набором маркеров запросов.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-138">From the remaining filters, the filter with the longest set of query tokens is selected.</span></span> <span data-ttu-id="3ec2f-139">На этом этапе фильтр списка разрешений имеет приоритет над фильтром списка блокировок, если оба фильтра имеют одинаковую длину **пути** и количество маркеров **запросов**.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-139">At this step, the allow list filter takes precedence over the block list filter if both filters have the same **path** length and number of **query** tokens.</span></span>
5. <span data-ttu-id="3ec2f-140">Если допустимого фильтра нет, то крайний левый дочерний домен удаляется из **узла**, а процесс выбора начинается с шага 1.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-140">If there's no valid filter remaining, then the left-most subdomain is removed from **host** and the selection process starts over at step 1.</span></span> <span data-ttu-id="3ec2f-141">Поиск **узла**, отмеченного звездочкой ("\*"), выполняется в последний момент, и он сопоставляется со всеми узлами.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-141">The special asterisk ("\*") **host** is the last searched and it matches all hosts.</span></span>
6. <span data-ttu-id="3ec2f-142">Если фильтр доступен, он блокирует или разрешает URL-запрос.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-142">If a filter's available, it blocks or allows the URL request.</span></span>

   >[!NOTE]
   ><span data-ttu-id="3ec2f-143">Запрос URL-адреса разрешен по умолчанию при отсутствии совпадений при фильтрации.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-143">The default behavior is to allow the URL request if no filter is matched.</span></span>

## <a name="example-filter-selection-criteria"></a><span data-ttu-id="3ec2f-144">Пример условий выбора фильтра</span><span class="sxs-lookup"><span data-stu-id="3ec2f-144">Example filter selection criteria</span></span>

<span data-ttu-id="3ec2f-145">В этом примере при поиске совпадения с "https://sub.contoso.com/docs" средство выбора фильтра будет выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-145">In this example, when searching for a match to "https://sub.contoso.com/docs" the filter selection will:</span></span>

1. <span data-ttu-id="3ec2f-146">Выполнять поиск фильтра "sub.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="3ec2f-146">Search for a filter for "sub.contoso.com".</span></span> <span data-ttu-id="3ec2f-147">Если фильтр найден, поиск переходит к шагу 2.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-147">If it finds a filter, the search moves to step 2.</span></span> <span data-ttu-id="3ec2f-148">Если фильтр не найден, средство выбора фильтра попытается снова выполнить поиск фильтра по элементам "contoso.com", "com" и, наконец, "".</span><span class="sxs-lookup"><span data-stu-id="3ec2f-148">If a filter isn't found, then it tries again with "contoso.com", "com", and finally "".</span></span>
2. <span data-ttu-id="3ec2f-149">Из выбранных фильтров все фильтры без элемента "http" в **схеме** удаляются.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-149">From the selected filters, any that don't have "http" in the **scheme** are removed.</span></span>
3. <span data-ttu-id="3ec2f-150">Из оставшихся фильтров все фильтры с точным номером порта, отличным от "80", удаляются.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-150">From the remaining filters, any that have an exact port number that isn't "80" are removed.</span></span>
4. <span data-ttu-id="3ec2f-151">Из оставшихся фильтров все фильтры без префикса "/docs" для **пути**, удаляются.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-151">From the remaining filters, any that don't have "/docs" as a prefix of the **path** are removed.</span></span>
5. <span data-ttu-id="3ec2f-152">Из оставшихся фильтров выбирается и применяется фильтр с самым длинным префиксом пути.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-152">From the remaining filters, the filter with the longest path prefix is selected and applied.</span></span> <span data-ttu-id="3ec2f-153">Если фильтр не найден, процесс выбора начинается снова с шага 1.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-153">If a filter isn't found, the selection process starts over again at step 1.</span></span> <span data-ttu-id="3ec2f-154">Процесс повторяется со следующим дочерним доменом.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-154">The process is repeated with the next subdomain.</span></span>

### <a name="additional-filter-information"></a><span data-ttu-id="3ec2f-155">Дополнительные сведения фильтрации</span><span class="sxs-lookup"><span data-stu-id="3ec2f-155">Additional filter information</span></span>

<span data-ttu-id="3ec2f-156">Если в фильтре перед **узлом** стоит точка ("."), фильтруются только точные совпадения **узла**.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-156">If a filter has a dot (".") prefixing the **host** then only exact **host** matches are filtered.</span></span> <span data-ttu-id="3ec2f-157">Пример</span><span class="sxs-lookup"><span data-stu-id="3ec2f-157">For example:</span></span>

- <span data-ttu-id="3ec2f-158">"contoso.com" (без точки) будет сопоставляться с "contoso.com", "www.contoso.com" и "sub.www.contoso.com"</span><span class="sxs-lookup"><span data-stu-id="3ec2f-158">"contoso.com" (no dot) will match "contoso.com", "www.contoso.com", and "sub.www.contoso.com"</span></span>
- <span data-ttu-id="3ec2f-159">".www.contoso.com" (с точкой-префиксом) будет сопоставляться только с "www.contoso.com"</span><span class="sxs-lookup"><span data-stu-id="3ec2f-159">".www.contoso.com" (with a dot prefix) will only match "www.contoso.com"</span></span>

<span data-ttu-id="3ec2f-160">Вы можете использовать как стандартную, так и пользовательскую **схему**.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-160">You can use either a standard or custom **schema**.</span></span> <span data-ttu-id="3ec2f-161">Поддерживаются следующие стандартные схемы:</span><span class="sxs-lookup"><span data-stu-id="3ec2f-161">Supported standard schemas include:</span></span>

- <span data-ttu-id="3ec2f-162">_about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_ и _wss_.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-162">_about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_, and _wss_.</span></span>

<span data-ttu-id="3ec2f-163">Любая другая **схема** рассматривается как пользовательская**схема**, однако допускается использование только шаблонов _schema:\*_ и _schema://\*_.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-163">Any other **schema** is treated as a custom **schema**, but only the _schema:\*_ and _schema://\*_ patterns are allowed.</span></span> <span data-ttu-id="3ec2f-164">Например:</span><span class="sxs-lookup"><span data-stu-id="3ec2f-164">For example:</span></span>

- <span data-ttu-id="3ec2f-165">"custom:\*" или "custom://\*" будет сопоставляться с "custom:app"</span><span class="sxs-lookup"><span data-stu-id="3ec2f-165">"custom:\*" or "custom://\*" will match "custom:app"</span></span>
- <span data-ttu-id="3ec2f-166">"custom:app" или "custom://app" являются недопустимыми</span><span class="sxs-lookup"><span data-stu-id="3ec2f-166">"custom:app" or "custom://app" are invalid</span></span>

<span data-ttu-id="3ec2f-167">**схема** и **узел** не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-167">**schema** and **host** aren't case-sensitive.</span></span> <span data-ttu-id="3ec2f-168">Пример</span><span class="sxs-lookup"><span data-stu-id="3ec2f-168">For example:</span></span>

- <span data-ttu-id="3ec2f-169">Фильтр "http://contoso.com" совпадает с "HTTP://contoso.com", "http://contoso.COM "и "http://contoso.com"</span><span class="sxs-lookup"><span data-stu-id="3ec2f-169">"http://contoso.com" filter matches "HTTP://contoso.com", "http://contoso.COM", and "http://contoso.com"</span></span>

<span data-ttu-id="3ec2f-170">**путь** и **запрос** чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-170">**path** and **query** are case-sensitive.</span></span> <span data-ttu-id="3ec2f-171">Пример</span><span class="sxs-lookup"><span data-stu-id="3ec2f-171">For example:</span></span>

- <span data-ttu-id="3ec2f-172">Фильтр "http://contoso.com/path?query=A" не совпадает с "http://contoso.com/Path?query=A" или "http://contoso.com/path?Query=A".</span><span class="sxs-lookup"><span data-stu-id="3ec2f-172">"http://contoso.com/path?query=A" filter doesn't match "http://contoso.com/Path?query=A" or "http://contoso.com/path?Query=A".</span></span> <span data-ttu-id="3ec2f-173">Он совпадает с "http://contoso.COM/path?query=A".</span><span class="sxs-lookup"><span data-stu-id="3ec2f-173">It does match "http://contoso.COM/path?query=A".</span></span>

## <a name="content-license"></a><span data-ttu-id="3ec2f-174">Лицензия на содержимое</span><span class="sxs-lookup"><span data-stu-id="3ec2f-174">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="3ec2f-175">Некоторые части этой страницы представляют собой измененные материалы, созданные и предоставленные на сайте Chromium.org. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span><span class="sxs-lookup"><span data-stu-id="3ec2f-175">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="3ec2f-176">Исходная [страница Chromium находится здесь](https://www.chromium.org/administrators/url-blacklist-filter-format).</span><span class="sxs-lookup"><span data-stu-id="3ec2f-176">The original [Chromium page can be found here](https://www.chromium.org/administrators/url-blacklist-filter-format).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="3ec2f-177">Эта работа предоставляется в рамках международной лицензии <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec2f-177">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ec2f-178">См. также</span><span class="sxs-lookup"><span data-stu-id="3ec2f-178">See also</span></span>

- [<span data-ttu-id="3ec2f-179">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="3ec2f-179">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
