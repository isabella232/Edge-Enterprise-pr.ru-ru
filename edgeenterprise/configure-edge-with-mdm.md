---
title: Настройка Microsoft Edge с помощью средств управления мобильными устройствами
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Настройка Microsoft Edge с помощью средств управления мобильными устройствами.
ms.openlocfilehash: 0927d64366652986b87c2f517ca8ebafd4c9ac55
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641655"
---
# <a name="configure-microsoft-edge-using-mobile-device-management"></a><span data-ttu-id="e0f7d-103">Настройка Microsoft Edge с помощью средств управления мобильными устройствами</span><span class="sxs-lookup"><span data-stu-id="e0f7d-103">Configure Microsoft Edge using Mobile Device Management</span></span>

<span data-ttu-id="e0f7d-104">В этой статье приводятся инструкции по настройке Microsoft Edge в Windows 10 с помощью [Средств управления мобильными устройствами (MDM)](/windows/client-management/mdm/) посредством [приема ADMX-файла](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-104">This article explains how to configure Microsoft Edge on Windows 10 using [Mobile Device Management (MDM)](/windows/client-management/mdm/) by means of [ADMX Ingestion](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span></span> <span data-ttu-id="e0f7d-105">Также в этой статье:</span><span class="sxs-lookup"><span data-stu-id="e0f7d-105">This article also describes:</span></span>

- <span data-ttu-id="e0f7d-106">Создание [универсального кода ресурса открытого сообщества производителей мобильной связи (OMA-URI) для политик Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-106">How to [create Open Mobile Alliance Uniform Resource Identifier (OMA-URI) for Microsoft Edge policies](#create-an-oma-uri-for-microsoft-edge-policies).</span></span>
- <span data-ttu-id="e0f7d-107">Настройка [Microsoft Edge в Intune с помощью приема ADMX-файла и настраиваемого кода OMA-URI](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-107">How to [configure Microsoft Edge in Intune using ADMX ingestion and custom OMA-URI](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span></span>

> [!NOTE]
> <span data-ttu-id="e0f7d-108">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-108">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e0f7d-109">Что вам понадобится</span><span class="sxs-lookup"><span data-stu-id="e0f7d-109">Prerequisites</span></span>

<span data-ttu-id="e0f7d-110">Windows 10 со следующими минимальными системными требованиями:</span><span class="sxs-lookup"><span data-stu-id="e0f7d-110">Windows 10, with the following minimum system requirements:</span></span>

- <span data-ttu-id="e0f7d-111">Windows 10, версия 1903 с установленными обновлениями [KB4512941](https://support.microsoft.com/help/4512941/) и [KB4517211](https://support.microsoft.com/help/4517211/)</span><span class="sxs-lookup"><span data-stu-id="e0f7d-111">Windows 10, version 1903 with [KB4512941](https://support.microsoft.com/help/4512941/) and [KB4517211](https://support.microsoft.com/help/4517211/) installed</span></span>
- <span data-ttu-id="e0f7d-112">Windows 10, версия 1809 с установленными обновлениями [KB4512534](https://support.microsoft.com/help/4512534/) и [KB4520062](https://support.microsoft.com/help/4520062/)</span><span class="sxs-lookup"><span data-stu-id="e0f7d-112">Windows 10, version 1809 with [KB4512534](https://support.microsoft.com/help/4512534/) and [KB4520062](https://support.microsoft.com/help/4520062/) installed</span></span>
- <span data-ttu-id="e0f7d-113">Windows 10, версия 1803 с установленными обновлениями [KB4512509](https://support.microsoft.com/help/4512509/) и [KB4519978](https://support.microsoft.com/help/4519978)</span><span class="sxs-lookup"><span data-stu-id="e0f7d-113">Windows 10, version 1803 with [KB4512509](https://support.microsoft.com/help/4512509/) and [KB4519978](https://support.microsoft.com/help/4519978) installed</span></span>
- <span data-ttu-id="e0f7d-114">Windows 10, версия 1709 с установленными обновлениями [KB4516071](https://support.microsoft.com/help/4516071/) и [KB4520006](https://support.microsoft.com/help/4520006)</span><span class="sxs-lookup"><span data-stu-id="e0f7d-114">Windows 10, version 1709 with [KB4516071](https://support.microsoft.com/help/4516071/) and [KB4520006](https://support.microsoft.com/help/4520006) installed</span></span>

## <a name="overview"></a><span data-ttu-id="e0f7d-115">Обзор</span><span class="sxs-lookup"><span data-stu-id="e0f7d-115">Overview</span></span>

<span data-ttu-id="e0f7d-116">Вы можете настроить Microsoft Edge в Windows 10 с помощью MDM с предпочтительным поставщиком средств управления корпоративной мобильной средой (EMM) или MDM, поддерживающим [примем ADMX-файлов](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-116">You can configure Microsoft Edge on Windows 10 using MDM with your preferred Enterprise Mobility Management (EMM) or MDM provider that supports [ADMX Ingestion](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span></span>

<span data-ttu-id="e0f7d-117">Настройка Microsoft Edge с помощью MDM выполняется в два этапа.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-117">Configuring Microsoft Edge with MDM is a two part process:</span></span>

1. <span data-ttu-id="e0f7d-118">Прием ADMX-файла Microsoft Edge поставщиком EMM или MDM.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-118">Ingesting the Microsoft Edge ADMX file into your EMM or MDM provider.</span></span> <span data-ttu-id="e0f7d-119">Инструкции по приему ADMX-файлов см. в документации вашего поставщика.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-119">See your provider for instructions on how to ingest an ADMX file.</span></span>

   > [!NOTE]
   > <span data-ttu-id="e0f7d-120">Инструкции для Microsoft Intune см. в разделе [Настройка Microsoft Edge в Intune с помощью приема ADMX-файла](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-120">For Microsoft Intune, see [Configure Microsoft Edge in Intune using ADMX ingestion](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span></span>

2. <span data-ttu-id="e0f7d-121">[Создание кода OMA-URI для политики Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-121">[Creating an OMA-URI for a Microsoft Edge policy](#create-an-oma-uri-for-microsoft-edge-policies).</span></span>

## <a name="create-an-oma-uri-for-microsoft-edge-policies"></a><span data-ttu-id="e0f7d-122">Создание кода OMA-URI для политик Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e0f7d-122">Create an OMA-URI for Microsoft Edge policies</span></span>

<span data-ttu-id="e0f7d-123">В следующих разделах приведены инструкции по созданию пути OMA-URI, а также поиску и определению значения в формате XML для обязательных и рекомендуемых политик браузера.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-123">The following sections describe how to create the OMA-URI path and look up and define the value in XML format for mandatory and recommended browser polices.</span></span>

<span data-ttu-id="e0f7d-124">Прежде чем приступить к работе, скачайте файл шаблонов политики Microsoft Edge (MicrosoftEdgePolicyTemplates.cab) на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) и извлеките содержимое.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-124">Before you get started download the Microsoft Edge policy templates file (MicrosoftEdgePolicyTemplates.cab) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise) and extract the contents.</span></span>

<span data-ttu-id="e0f7d-125">Определение кода OMA-URI выполняется в три этапа.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-125">There are three steps for defining the OMA-URI:</span></span>

1. [<span data-ttu-id="e0f7d-126">Создание пути OMA-URI</span><span class="sxs-lookup"><span data-stu-id="e0f7d-126">Create the OMA-URI path</span></span>](#create-the-oma-uri-path)
2. [<span data-ttu-id="e0f7d-127">Указание базы данных OMA-URI</span><span class="sxs-lookup"><span data-stu-id="e0f7d-127">Specify the OMA-URI data type</span></span>](#specify-the-data-type)
3. [<span data-ttu-id="e0f7d-128">Установка значения OMA-URI</span><span class="sxs-lookup"><span data-stu-id="e0f7d-128">Set the OMA-URI value</span></span>](#set-the-value-for-a-browser-policy)

### <a name="create-the-oma-uri-path"></a><span data-ttu-id="e0f7d-129">Создание пути OMA-URI</span><span class="sxs-lookup"><span data-stu-id="e0f7d-129">Create the OMA-URI path</span></span>

<span data-ttu-id="e0f7d-130">Используйте следующую формулу в качестве руководства по созданию путей OMA-URI.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-130">Use the following formula as a guide for creating the OMA-URI paths.</span></span> <br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`* <br/><br/>

| <span data-ttu-id="e0f7d-131">Параметр</span><span class="sxs-lookup"><span data-stu-id="e0f7d-131">Parameter</span></span>         | <span data-ttu-id="e0f7d-132">Описание</span><span class="sxs-lookup"><span data-stu-id="e0f7d-132">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| \<ADMXIngestName> | <span data-ttu-id="e0f7d-133">Используйте имя "Edge" или имя, выбранное вами во время приема административного шаблона.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-133">Use "Edge" or what you defined when ingesting the administrative template.</span></span> <span data-ttu-id="e0f7d-134">Например, если вы использовали "./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx", то используйте "MicrosoftEdge".</span><span class="sxs-lookup"><span data-stu-id="e0f7d-134">For example, if you used "./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx", then use "MicrosoftEdge".</span></span><br/><br/> <span data-ttu-id="e0f7d-135">Имя `<ADMXIngestionName>` должно совпадать с именем, использованным при приеме ADMX-файла.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-135">The `<ADMXIngestionName>` must match what was used when you ingested the ADMX file.</span></span> |
| \<ADMXNamespace>  | <span data-ttu-id="e0f7d-136">"microsoft_edge" или "microsoft_edge_recommended" в зависимости от того, какая политика задается — обязательная или рекомендуемая.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-136">Either "microsoft_edge" or "microsoft_edge_recommended" depending on whether you're setting a mandatory or recommended policy.</span></span> |
| \<ADMXCategory>   | <span data-ttu-id="e0f7d-137">Параметр "parentCategory" политики определяется в ADMX-файле.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-137">The "parentCategory" of the policy is defined in the ADMX file.</span></span> <span data-ttu-id="e0f7d-138">Пропустите `<ADMXCategory>`, если политика не сгруппирована (не определена категория "parentCategory").</span><span class="sxs-lookup"><span data-stu-id="e0f7d-138">Omit the `<ADMXCategory>` if the policy isn't grouped (No "parentCategory" defined).</span></span> |
| \<PolicyName>     | <span data-ttu-id="e0f7d-139">Имя политики можно найти в статье [Справочник по политикам браузера](./microsoft-edge-policies.md).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-139">The policy name can be found in the [Browser policy reference](./microsoft-edge-policies.md) article.</span></span> |

#### <a name="uri-path-example"></a><span data-ttu-id="e0f7d-140">Пример пути URI:</span><span class="sxs-lookup"><span data-stu-id="e0f7d-140">URI path example:</span></span>

<span data-ttu-id="e0f7d-141">В этом примере предположим, что узел `<ADMXIngestName>` называется "Edge" и вы настраиваете обязательную политику.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-141">For this example, assume the `<ADMXIngestName>` node was named “Edge" and you're setting a mandatory policy.</span></span> <span data-ttu-id="e0f7d-142">Путь URI будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e0f7d-142">The URI path would be:</span></span><br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~<ADMXCategory>/<PolicyName>`*

<span data-ttu-id="e0f7d-143">Если политика не входит в группу (например, DiskCacheSize), удалите "`~<ADMXCategory>`".</span><span class="sxs-lookup"><span data-stu-id="e0f7d-143">If the policy isn't in a group (for example, DiskCacheSize) remove "`~<ADMXCategory>`".</span></span> <span data-ttu-id="e0f7d-144">Замените `<PolicyName>` на имя политики — DiskCacheSize.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-144">Replace `<PolicyName>` with the name of the policy, DiskCacheSize.</span></span> <span data-ttu-id="e0f7d-145">Путь URI будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e0f7d-145">The URI path would be:</span></span><br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`*

<span data-ttu-id="e0f7d-146">Если политика входит в группу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-146">If the policy is in a group, follow these steps:</span></span>

1. <span data-ttu-id="e0f7d-147">Откройте файл **msedge.admx** в любом XML-редакторе.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-147">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="e0f7d-148">Найдите имя политики, которую вы хотите настроить.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-148">Search for the policy name you want to set.</span></span> <span data-ttu-id="e0f7d-149">Например, "ExtensionInstallForceList".</span><span class="sxs-lookup"><span data-stu-id="e0f7d-149">For example, "ExtensionInstallForceList".</span></span>
3. <span data-ttu-id="e0f7d-150">Используйте значение атрибута *ref* из элемента *parentCategory*.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-150">Use the value of the *ref* attribute from the *parentCategory* element.</span></span> <span data-ttu-id="e0f7d-151">Например, "Extensions" из \<parentCategory ref=" Extensions"/>.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-151">For example, "Extensions" from \<parentCategory ref=" Extensions"/>.</span></span>
4. <span data-ttu-id="e0f7d-152">Замените `<ADMXCategory>` на значение атрибута *ref* для формирования пути URI.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-152">Replace `<ADMXCategory>` with the *ref* attribute value to construct the URI path.</span></span> <span data-ttu-id="e0f7d-153">Путь URI будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e0f7d-153">The URI path would be:</span></span><br/><br/>
*`/Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`*

### <a name="specify-the-data-type"></a><span data-ttu-id="e0f7d-154">Указание базы данных</span><span class="sxs-lookup"><span data-stu-id="e0f7d-154">Specify the data type</span></span>

<span data-ttu-id="e0f7d-155">Типом данных OMA-URI всегда является "String" (строка).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-155">The OMA-URI data type is always “String”.</span></span>

### <a name="set-the-value-for-a-browser-policy"></a><span data-ttu-id="e0f7d-156">Установка значения для политики браузера</span><span class="sxs-lookup"><span data-stu-id="e0f7d-156">Set the value for a browser policy</span></span>

<span data-ttu-id="e0f7d-157">В этом разделе описывается, как задать значение в формате XML для каждого типа данных.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-157">This section describes how to set the value, in XML format, for each data type.</span></span> <span data-ttu-id="e0f7d-158">Перейдите в [Справочник по политикам браузера](./microsoft-edge-policies.md), чтобы найти тип данных политики.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-158">Go to [Browser policy reference](./microsoft-edge-policies.md) to look up the data type of the policy.</span></span>

> [!NOTE]
> <span data-ttu-id="e0f7d-159">Для нелогических типов данных значение всегда начинается с `<enabled/>`.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-159">For non-Boolean data types, the value always starts with `<enabled/>`.</span></span>

#### <a name="boolean-data-type"></a><span data-ttu-id="e0f7d-160">Логический тип данных</span><span class="sxs-lookup"><span data-stu-id="e0f7d-160">Boolean data type</span></span>

<span data-ttu-id="e0f7d-161">Для политик с логическим типом данных используйте `<enabled/>` или `<disabled/>`.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-161">For policies that are Boolean types use `<enabled/>` or `<disabled/>`.</span></span>

#### <a name="integer-data-type"></a><span data-ttu-id="e0f7d-162">Целочисленные типы данных</span><span class="sxs-lookup"><span data-stu-id="e0f7d-162">Integer data type</span></span>

<span data-ttu-id="e0f7d-163">Значение всегда должно начинаться с элемента `<enabled/>`, за которым следует `<data id="[valueName]" value="[decimal value]"/>`.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-163">The value always needs to start with the `<enabled/>` element followed by `<data id="[valueName]" value="[decimal value]"/>`.</span></span>

<span data-ttu-id="e0f7d-164">Чтобы найти имя значения и десятичное значение для страницы новой вкладки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-164">To find the value name and decimal value for a new tab page, use the following steps:</span></span>

1. <span data-ttu-id="e0f7d-165">Откройте файл **msedge.admx** в любом XML-редакторе.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-165">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="e0f7d-166">Найдите элемент `<policy>`, где имя атрибута совпадает с именем политики, которую вы хотите настроить.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-166">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="e0f7d-167">Для "RestoreOnStartup" выполните поиск по запросу `name="RestoreOnStartup"`.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-167">For "RestoreOnStartup", search for `name="RestoreOnStartup"`.</span></span>
3. <span data-ttu-id="e0f7d-168">В узле `<elements>` найдите значение, которое требуется задать.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-168">In the `<elements>` node, find the value you want to set.</span></span>
4. <span data-ttu-id="e0f7d-169">Используйте значение из атрибута "valueName" в узле `<elements>`.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-169">Use the value in the "valueName" attribute in the `<elements>` node.</span></span> <span data-ttu-id="e0f7d-170">Для "RestoreOnStartup" именем значения "valueName" будет "RestoreOnStartup".</span><span class="sxs-lookup"><span data-stu-id="e0f7d-170">For "RestoreOnStartup" the "valueName" is "RestoreOnStartup".</span></span>
5. <span data-ttu-id="e0f7d-171">Используйте значение из атрибута "value" в узле `<decimal>`.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-171">Use the value in the "value" attribute in the `<decimal>` node.</span></span> <span data-ttu-id="e0f7d-172">Чтобы параметр "RestoreOnStartup" открывал новую вкладку, значением должно быть "5".</span><span class="sxs-lookup"><span data-stu-id="e0f7d-172">For "RestoreOnStartup" to open the new tab page the value is "5".</span></span>

<span data-ttu-id="e0f7d-173">Чтобы при запуске открывалась страница с новой вкладкой, используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="e0f7d-173">To open the new tab page on startup use:</span></span><br>
`<enabled/> <data id="RestoreOnStartup" value="5"/>`

#### <a name="list-of-strings-data-type"></a><span data-ttu-id="e0f7d-174">Список строковых типов данных</span><span class="sxs-lookup"><span data-stu-id="e0f7d-174">List of strings data type</span></span>

<span data-ttu-id="e0f7d-175">Значение всегда должно начинаться с элемента `<enabled/>`, за которым следует `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-175">The value always needs to start with the `<enabled/>` element followed by `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`.</span></span>

> [!NOTE]
> <span data-ttu-id="e0f7d-176">Имя атрибута "id=" не является именем политики, хотя в большинстве случаев оно совпадает с именем политики.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-176">The "id=" attribute name isn't the policy name, even though in most cases it matches the policy name.</span></span> <span data-ttu-id="e0f7d-177">Это значение атрибута идентификатора узла \<list>, которое находится в ADMX-файле.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-177">It's the \<list> node id attribute value, which is found in the ADMX file.</span></span>

<span data-ttu-id="e0f7d-178">Чтобы найти код listID и задать значение для блокировки URL-адреса, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-178">To find the listID and define the value to block a URL, follow these steps:</span></span>

1. <span data-ttu-id="e0f7d-179">Откройте файл **msedge.admx** в любом XML-редакторе.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-179">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="e0f7d-180">Найдите элемент `<policy>`, где имя атрибута совпадает с именем политики, которую вы хотите настроить.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-180">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="e0f7d-181">Для "URLBlocklist" выполните поиск по запросу `name="URLBlocklist"`.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-181">For "URLBlocklist", search for `name="URLBlocklist"`.</span></span>
3. <span data-ttu-id="e0f7d-182">Используйте значение в атрибуте "id" узла `<list> node for [listID]`.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-182">Use the value in the "id" attribute of the `<list> node for [listID]`.</span></span>
4. <span data-ttu-id="e0f7d-183">"Value" — это список URL-адресов, разделенных точкой с запятой (;)</span><span class="sxs-lookup"><span data-stu-id="e0f7d-183">The "value" is a list of URLs separated by a semicolon (;)</span></span>

<span data-ttu-id="e0f7d-184">Например, чтобы заблокировать доступ к `contoso.com` и `https://ssl.server.com`, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-184">For example, to block access to `contoso.com` and `https://ssl.server.com`:</span></span><br>
`<enabled/> <data id=" URLBlocklistDesc" value="contoso.com;https://ssl.server.com"/>`

#### <a name="dictionary-or-string-data-type"></a><span data-ttu-id="e0f7d-185">Словарный или строчный тип данных</span><span class="sxs-lookup"><span data-stu-id="e0f7d-185">Dictionary or String data type</span></span>

<span data-ttu-id="e0f7d-186">Значение всегда должно начинаться с элемента `<enabled/>`, за которым следует `<data id="[textID]" value="[string]"/>`.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-186">The value always needs to start with the `<enabled/>` followed by `<data id="[textID]" value="[string]"/>` .</span></span>

<span data-ttu-id="e0f7d-187">Чтобы найти код textID и задать значение, настройте языковой стандарт, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-187">To find the textID and define the value set the locale, follow these steps:</span></span>

1. <span data-ttu-id="e0f7d-188">Откройте файл **msedge.admx** в любом XML-редакторе.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-188">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="e0f7d-189">Найдите элемент `<policy>`, где имя атрибута совпадает с именем политики, которую вы хотите настроить.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-189">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="e0f7d-190">Для "ApplicationLocaleValue" выполните поиск по запросу `name="ApplicationLocaleValue"`.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-190">For "ApplicationLocaleValue", search for `name="ApplicationLocaleValue"`.</span></span>
3. <span data-ttu-id="e0f7d-191">Используйте значение в атрибуте "id" узла `<text>` для `[textID]`.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-191">Use the value in the "id" attribute of the `<text>` node for `[textID]`.</span></span>
4. <span data-ttu-id="e0f7d-192">Значение значению "value" языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-192">Set the "value" to the culture code.</span></span>

<span data-ttu-id="e0f7d-193">Чтобы задать языковой стандарт "es-US" с помощью политики "ApplicationLocaleValue", выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-193">To set the locale to "es-US" with the "ApplicationLocaleValue" policy:</span></span><br>
`<enabled/> <data id="ApplicationLocaleValue" value="es-US"/>`

### <a name="create-the-oma-uri-for-a-recommended-policies"></a><span data-ttu-id="e0f7d-194">Создайте OMA-URI для рекомендуемых политик</span><span class="sxs-lookup"><span data-stu-id="e0f7d-194">Create the OMA-URI for a recommended policies</span></span>

<span data-ttu-id="e0f7d-195">Определение пути URI для рекомендуемых политик зависит от политики, которую вы хотите настроить.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-195">Defining the URI path for recommended policies depends on the policy you want to configure.</span></span>

#### <a name="to-define-the-uri-path-for-a-recommended-policy"></a><span data-ttu-id="e0f7d-196">Определение пути URI для рекомендуемой политики</span><span class="sxs-lookup"><span data-stu-id="e0f7d-196">To define the URI path for a recommended policy</span></span>

<span data-ttu-id="e0f7d-197">Используйте формулу пути URI (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) и выполните следующие действия, чтобы определить путь URI:</span><span class="sxs-lookup"><span data-stu-id="e0f7d-197">Use the URI path formula (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) and the following steps to define the URI path:</span></span>

1. <span data-ttu-id="e0f7d-198">Откройте файл **msedge.admx** в любом XML-редакторе.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-198">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="e0f7d-199">Если политика, которую вы хотите настроить, не входит в группу, переходите к шагу 4 и удалите `~<ADMXCategory>` из пути.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-199">If the policy you want to configure isn't in a group, skip to step 4 and remove `~<ADMXCategory>` from the path.</span></span>
3. <span data-ttu-id="e0f7d-200">Если политика, которую вы хотите настроить, входит в группу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-200">If the policy you want to configure is in a group:</span></span>

   - <span data-ttu-id="e0f7d-201">Чтобы найти `<ADMXCategory>`, выполните поиск политики, которую нужно задать.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-201">To look up the `<ADMXCategory>`, search for the policy you want to set.</span></span> <span data-ttu-id="e0f7d-202">При поиске добавьте "_recommended" к имени политики.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-202">When searching append "_recommended" to the policy name.</span></span> <span data-ttu-id="e0f7d-203">Например, поиск "RegisteredProtocolHandlers_recommended" даст следующий результат:</span><span class="sxs-lookup"><span data-stu-id="e0f7d-203">For example, a search for "RegisteredProtocolHandlers_recommended” has the following result:</span></span>

        ```xml
         <policy class="Both" displayName="$(string.RegisteredProtocolHandlers)" explainText="$(string.RegisteredProtocolHandlers_Explain)" key="Software\Policies\Microsoft\Edge\Recommended" name="RegisteredProtocolHandlers_recommended" presentation="$(presentation.RegisteredProtocolHandlers)">
           <parentCategory ref="ContentSettings_recommended"/>
           <supportedOn ref="SUPPORTED_WIN7_V77"/>
           <elements>
             <text id="RegisteredProtocolHandlers" maxLength="1000000" valueName="RegisteredProtocolHandlers"/>
           </elements>
         </policy>
        ```

   - <span data-ttu-id="e0f7d-204">Скопируйте значение атрибута *ref* из элемента `<parentCategory>`.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-204">Copy the value of the *ref* attribute from the `<parentCategory>` element.</span></span> <span data-ttu-id="e0f7d-205">Для "ContentSettings" скопируйте "ContentSettings_recommended" из `<parentCategory ref=" ContentSettings_recommended"/>`.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-205">For "ContentSettings", copy "ContentSettings_recommended" from `<parentCategory ref=" ContentSettings_recommended"/>`.</span></span>
   - <span data-ttu-id="e0f7d-206">Замените `<ADMXCategory>` на значение атрибута *ref* в формуле пути URI для формирования пути URI.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-206">Replace `<ADMXCategory>` with the *ref* attribute value to construct the URI path in the URI path formula.</span></span>

4. <span data-ttu-id="e0f7d-207">`<PolicyName>` — имя политики с добавленным элементом "_recommended".</span><span class="sxs-lookup"><span data-stu-id="e0f7d-207">The `<PolicyName>` is the name of the policy with "_recommended" appended to it.</span></span>

#### <a name="oma-uri-path-examples-for-recommended-policies"></a><span data-ttu-id="e0f7d-208">Примеры путей OMA-URI для рекомендуемых политик</span><span class="sxs-lookup"><span data-stu-id="e0f7d-208">OMA-URI path examples for recommended policies</span></span>

<span data-ttu-id="e0f7d-209">В следующей таблице приведены примеры путей OMA-URI для рекомендуемых политик.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-209">The following table shows examples of OMA-URI paths for recommended policies.</span></span>

|              <span data-ttu-id="e0f7d-210">Политика</span><span class="sxs-lookup"><span data-stu-id="e0f7d-210">Policy</span></span>               |             <span data-ttu-id="e0f7d-211">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="e0f7d-211">OMA-URI</span></span>                      |
|-----------------------------------|------------------------------------------|
| [<span data-ttu-id="e0f7d-212">RegisteredProtocolHandlers</span><span class="sxs-lookup"><span data-stu-id="e0f7d-212">RegisteredProtocolHandlers</span></span>](./microsoft-edge-policies.md#registeredprotocolhandlers)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~ContentSettings_recommended/RegisteredProtocolHandlers_recommended`                        |
| [<span data-ttu-id="e0f7d-213">PasswordManagerEnabled</span><span class="sxs-lookup"><span data-stu-id="e0f7d-213">PasswordManagerEnabled</span></span>](./microsoft-edge-policies.md#passwordmanagerenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~PasswordManager_recommended/PasswordManagerEnabled_recommended`                        |
| [<span data-ttu-id="e0f7d-214">PrintHeaderFooter</span><span class="sxs-lookup"><span data-stu-id="e0f7d-214">PrintHeaderFooter</span></span>](./microsoft-edge-policies.md#printheaderfooter)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Printing_recommended/PrintHeaderFooter_recommended`                        |
| [<span data-ttu-id="e0f7d-215">SmartScreenEnabled</span><span class="sxs-lookup"><span data-stu-id="e0f7d-215">SmartScreenEnabled</span></span>](./microsoft-edge-policies.md#smartscreenenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~SmartScreen_recommended/SmartScreenEnabled_recommended`                        |
| [<span data-ttu-id="e0f7d-216">HomePageLocation</span><span class="sxs-lookup"><span data-stu-id="e0f7d-216">HomePageLocation</span></span>](./microsoft-edge-policies.md#homepagelocation)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/HomepageLocation_recommended`                        |
| [<span data-ttu-id="e0f7d-217">ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="e0f7d-217">ShowHomeButton</span></span>](./microsoft-edge-policies.md#showhomebutton)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/ShowHomeButton_recommended`                        |
| [<span data-ttu-id="e0f7d-218">FavoritesBarEnabled</span><span class="sxs-lookup"><span data-stu-id="e0f7d-218">FavoritesBarEnabled</span></span>](./microsoft-edge-policies.md#favoritesbarenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~/FavoritesBarEnabled_recommended`                        |

### <a name="oma-uri-examples"></a><span data-ttu-id="e0f7d-219">Примеры OMA-URI</span><span class="sxs-lookup"><span data-stu-id="e0f7d-219">OMA-URI examples</span></span>

<span data-ttu-id="e0f7d-220">Примеры OMA-URI с путем URI, типом и возможным значением.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-220">OMA-URI examples with their URI path, type, and an example value.</span></span>

#### <a name="boolean-data-type-examples"></a><span data-ttu-id="e0f7d-221">Примеры логических типов данных</span><span class="sxs-lookup"><span data-stu-id="e0f7d-221">Boolean data type examples</span></span>

*<span data-ttu-id="e0f7d-222">[ShowHomeButton](./microsoft-edge-policies.md#showhomebutton):</span><span class="sxs-lookup"><span data-stu-id="e0f7d-222">[ShowHomeButton](./microsoft-edge-policies.md#showhomebutton):</span></span>*

| <span data-ttu-id="e0f7d-223">Поле</span><span class="sxs-lookup"><span data-stu-id="e0f7d-223">Field</span></span>   | <span data-ttu-id="e0f7d-224">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-224">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f7d-225">Имя</span><span class="sxs-lookup"><span data-stu-id="e0f7d-225">Name</span></span>    | <span data-ttu-id="e0f7d-226">Microsoft Edge: ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="e0f7d-226">Microsoft Edge: ShowHomeButton</span></span>                                                       |
| <span data-ttu-id="e0f7d-227">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="e0f7d-227">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton` |
| <span data-ttu-id="e0f7d-228">Тип</span><span class="sxs-lookup"><span data-stu-id="e0f7d-228">type</span></span>    | <span data-ttu-id="e0f7d-229">String (строка)</span><span class="sxs-lookup"><span data-stu-id="e0f7d-229">String</span></span>                                                                               |
| <span data-ttu-id="e0f7d-230">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-230">Value</span></span>   | `<enabled/>`                                                                          |

*<span data-ttu-id="e0f7d-231">[DefaultSearchProviderEnabled](./microsoft-edge-policies.md#defaultsearchproviderenabled):</span><span class="sxs-lookup"><span data-stu-id="e0f7d-231">[DefaultSearchProviderEnabled](./microsoft-edge-policies.md#defaultsearchproviderenabled):</span></span>*

| <span data-ttu-id="e0f7d-232">Поле</span><span class="sxs-lookup"><span data-stu-id="e0f7d-232">Field</span></span>   | <span data-ttu-id="e0f7d-233">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-233">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f7d-234">Имя</span><span class="sxs-lookup"><span data-stu-id="e0f7d-234">Name</span></span>    | <span data-ttu-id="e0f7d-235">Microsoft Edge: DefaultSearchProviderEnabled</span><span class="sxs-lookup"><span data-stu-id="e0f7d-235">Microsoft Edge: DefaultSearchProviderEnabled</span></span>                                         |
| <span data-ttu-id="e0f7d-236">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="e0f7d-236">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~DefaultSearchProvider/DefaultSearchProviderEnabled`    |
| <span data-ttu-id="e0f7d-237">Тип</span><span class="sxs-lookup"><span data-stu-id="e0f7d-237">type</span></span>    | <span data-ttu-id="e0f7d-238">String (строка)</span><span class="sxs-lookup"><span data-stu-id="e0f7d-238">String</span></span>                                                                               |
| <span data-ttu-id="e0f7d-239">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-239">Value</span></span>   | `<disable/>`                                                                          |

### <a name="integer-data-type-examples"></a><span data-ttu-id="e0f7d-240">Примеры целочисленных типов данных</span><span class="sxs-lookup"><span data-stu-id="e0f7d-240">Integer data type examples</span></span>

*<span data-ttu-id="e0f7d-241">[AutoImportAtFirstRun](./microsoft-edge-policies.md#autoimportatfirstrun):</span><span class="sxs-lookup"><span data-stu-id="e0f7d-241">[AutoImportAtFirstRun](./microsoft-edge-policies.md#autoimportatfirstrun):</span></span>*

| <span data-ttu-id="e0f7d-242">Поле</span><span class="sxs-lookup"><span data-stu-id="e0f7d-242">Field</span></span>   | <span data-ttu-id="e0f7d-243">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-243">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f7d-244">Имя</span><span class="sxs-lookup"><span data-stu-id="e0f7d-244">Name</span></span>    | <span data-ttu-id="e0f7d-245">Microsoft Edge: AutoImportAtFirstRun</span><span class="sxs-lookup"><span data-stu-id="e0f7d-245">Microsoft Edge: AutoImportAtFirstRun</span></span>                                                 |
| <span data-ttu-id="e0f7d-246">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="e0f7d-246">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/AutoImportAtFirstRun`   |
| <span data-ttu-id="e0f7d-247">Тип</span><span class="sxs-lookup"><span data-stu-id="e0f7d-247">type</span></span>    | <span data-ttu-id="e0f7d-248">String (строка)</span><span class="sxs-lookup"><span data-stu-id="e0f7d-248">String</span></span>                                                                               |
| <span data-ttu-id="e0f7d-249">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-249">Value</span></span>   | `<enabled/><data id="AutoImportAtFirstRun" value="1"/>`                             |

*<span data-ttu-id="e0f7d-250">[DefaultImagesSetting](./microsoft-edge-policies.md#defaultimagessetting):</span><span class="sxs-lookup"><span data-stu-id="e0f7d-250">[DefaultImagesSetting](./microsoft-edge-policies.md#defaultimagessetting):</span></span>*

| <span data-ttu-id="e0f7d-251">Поле</span><span class="sxs-lookup"><span data-stu-id="e0f7d-251">Field</span></span>   | <span data-ttu-id="e0f7d-252">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-252">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f7d-253">Имя</span><span class="sxs-lookup"><span data-stu-id="e0f7d-253">Name</span></span>    | <span data-ttu-id="e0f7d-254">Microsoft Edge: DefaultImagesSetting</span><span class="sxs-lookup"><span data-stu-id="e0f7d-254">Microsoft Edge: DefaultImagesSetting</span></span>                                                 |
| <span data-ttu-id="e0f7d-255">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="e0f7d-255">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/DefaultImagesSetting`    |
| <span data-ttu-id="e0f7d-256">Тип</span><span class="sxs-lookup"><span data-stu-id="e0f7d-256">type</span></span>    | <span data-ttu-id="e0f7d-257">String (строка)</span><span class="sxs-lookup"><span data-stu-id="e0f7d-257">String</span></span>                                                                               |
| <span data-ttu-id="e0f7d-258">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-258">Value</span></span>   | `<enabled/><data id="DefaultImagesSetting" value="2"/>`                             |

*<span data-ttu-id="e0f7d-259">[DiskCacheSize](./microsoft-edge-policies.md#diskcachesize):</span><span class="sxs-lookup"><span data-stu-id="e0f7d-259">[DiskCacheSize](./microsoft-edge-policies.md#diskcachesize):</span></span>*

| <span data-ttu-id="e0f7d-260">Поле</span><span class="sxs-lookup"><span data-stu-id="e0f7d-260">Field</span></span>   | <span data-ttu-id="e0f7d-261">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-261">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f7d-262">Имя</span><span class="sxs-lookup"><span data-stu-id="e0f7d-262">Name</span></span>    | <span data-ttu-id="e0f7d-263">Microsoft Edge: DiskCacheSize</span><span class="sxs-lookup"><span data-stu-id="e0f7d-263">Microsoft Edge: DiskCacheSize</span></span>                                                        |
| <span data-ttu-id="e0f7d-264">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="e0f7d-264">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`        |
| <span data-ttu-id="e0f7d-265">Тип</span><span class="sxs-lookup"><span data-stu-id="e0f7d-265">type</span></span>    | <span data-ttu-id="e0f7d-266">String (строка)</span><span class="sxs-lookup"><span data-stu-id="e0f7d-266">String</span></span>                                                                               |
| <span data-ttu-id="e0f7d-267">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-267">Value</span></span>   | `<enabled/><data id="DiskCacheSize" value="1000000"/>`                               |

#### <a name="list-of-strings-data-type-examples"></a><span data-ttu-id="e0f7d-268">Список примеров строковых типов данных</span><span class="sxs-lookup"><span data-stu-id="e0f7d-268">List of strings data type examples</span></span>
<!--
*[NotificationsAllowedForUrls](./microsoft-edge-policies.md#NotificationsAllowedForUrls):*

| Field   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: NotificationsAllowedForUrls                                          |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/NotificationsAllowedForUrls`    |
| Type    | String                                                                               |
| Value   | `<enabled/><data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com"/>`<br>For multiple list items: `<data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com;[*.]contoso.edu"/>`                           |
-->
*<span data-ttu-id="e0f7d-269">[RestoreOnStartupURLS](./microsoft-edge-policies.md#restoreonstartupurls):</span><span class="sxs-lookup"><span data-stu-id="e0f7d-269">[RestoreOnStartupURLS](./microsoft-edge-policies.md#restoreonstartupurls):</span></span>*

| <span data-ttu-id="e0f7d-270">Поле</span><span class="sxs-lookup"><span data-stu-id="e0f7d-270">Field</span></span>   | <span data-ttu-id="e0f7d-271">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-271">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f7d-272">Имя</span><span class="sxs-lookup"><span data-stu-id="e0f7d-272">Name</span></span>    | <span data-ttu-id="e0f7d-273">Microsoft Edge: RestoreOnStartupURLS</span><span class="sxs-lookup"><span data-stu-id="e0f7d-273">Microsoft Edge: RestoreOnStartupURLS</span></span>                                                 |
| <span data-ttu-id="e0f7d-274">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="e0f7d-274">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/RestoreOnStartupURLs`    |
| <span data-ttu-id="e0f7d-275">Тип</span><span class="sxs-lookup"><span data-stu-id="e0f7d-275">Type</span></span>    | <span data-ttu-id="e0f7d-276">String (строка)</span><span class="sxs-lookup"><span data-stu-id="e0f7d-276">String</span></span>                                                                               |
| <span data-ttu-id="e0f7d-277">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-277">Value</span></span>   | `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com"/>`<br><span data-ttu-id="e0f7d-278">Для нескольких элементов списка:</span><span class="sxs-lookup"><span data-stu-id="e0f7d-278">For multiple list items:</span></span> `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com&#xF000;2&#xF000;http://www.microsoft.com"/>`  |

*<span data-ttu-id="e0f7d-279">[ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist):</span><span class="sxs-lookup"><span data-stu-id="e0f7d-279">[ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist):</span></span>*

| <span data-ttu-id="e0f7d-280">Поле</span><span class="sxs-lookup"><span data-stu-id="e0f7d-280">Field</span></span>   | <span data-ttu-id="e0f7d-281">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-281">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f7d-282">Имя</span><span class="sxs-lookup"><span data-stu-id="e0f7d-282">Name</span></span>    | <span data-ttu-id="e0f7d-283">Microsoft Edge: ExtensionInstallForcelist</span><span class="sxs-lookup"><span data-stu-id="e0f7d-283">Microsoft Edge: ExtensionInstallForcelist</span></span>                                            |
| <span data-ttu-id="e0f7d-284">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="e0f7d-284">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`    |
| <span data-ttu-id="e0f7d-285">Тип</span><span class="sxs-lookup"><span data-stu-id="e0f7d-285">Type</span></span>    | <span data-ttu-id="e0f7d-286">String (строка)</span><span class="sxs-lookup"><span data-stu-id="e0f7d-286">String</span></span>                                                                               |
| <span data-ttu-id="e0f7d-287">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-287">Value</span></span>   | `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000;gbchcmhmhahfdphkhkmpfmihenigjmpp;https://extensionwebstorebase.edgesv.net/v1/crx"/>`                               |

#### <a name="dictionary-and-string-data-type-example"></a><span data-ttu-id="e0f7d-288">Пример словарных или строчных типов данных</span><span class="sxs-lookup"><span data-stu-id="e0f7d-288">Dictionary and String data type example</span></span>

*<span data-ttu-id="e0f7d-289">[ProxyMode](./microsoft-edge-policies.md#proxymode):</span><span class="sxs-lookup"><span data-stu-id="e0f7d-289">[ProxyMode](./microsoft-edge-policies.md#proxymode):</span></span>*

| <span data-ttu-id="e0f7d-290">Поле</span><span class="sxs-lookup"><span data-stu-id="e0f7d-290">Field</span></span>   | <span data-ttu-id="e0f7d-291">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-291">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f7d-292">Имя</span><span class="sxs-lookup"><span data-stu-id="e0f7d-292">Name</span></span>    | <span data-ttu-id="e0f7d-293">Microsoft Edge: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="e0f7d-293">Microsoft Edge: ProxyMode</span></span>                                                            |
| <span data-ttu-id="e0f7d-294">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="e0f7d-294">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ProxyMode/ProxyMode`  |
| <span data-ttu-id="e0f7d-295">Тип</span><span class="sxs-lookup"><span data-stu-id="e0f7d-295">Type</span></span>    | <span data-ttu-id="e0f7d-296">String (строка)</span><span class="sxs-lookup"><span data-stu-id="e0f7d-296">String</span></span>                                                                               |
| <span data-ttu-id="e0f7d-297">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7d-297">Value</span></span>   | `<enabled/><data id="ProxyMode" value="auto_detect"/>`                               |

## <a name="configure-microsoft-edge-in-intune-using-admx-ingestion"></a><span data-ttu-id="e0f7d-298">Настройка Microsoft Edge в Intune с помощью приема ADMX-файла</span><span class="sxs-lookup"><span data-stu-id="e0f7d-298">Configure Microsoft Edge in Intune using ADMX ingestion</span></span>

<span data-ttu-id="e0f7d-299">Для настройки Microsoft Edge с помощью Microsoft Intune рекомендуется использовать профиль "Административные шаблоны", как описано в разделе [Настройка параметров политики Microsoft Edge с помощью Microsoft Intune](./configure-edge-with-intune.md).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-299">The recommended way to configure Microsoft Edge with Microsoft Intune is to use the Administrative Templates profile as described in [Configure Microsoft Edge policy settings with Microsoft Intune](./configure-edge-with-intune.md).</span></span> <span data-ttu-id="e0f7d-300">Если вы хотите оценить политику, которая в данный момент недоступна в административных шаблонах Microsoft Edge, вы можете настроить Microsoft Edge в Intune, используя [пользовательские параметры для устройств с Windows 10 в Intune](/intune/configuration/custom-settings-windows-10).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-300">If you want to evaluate a policy that is currently not available in the Microsoft Edge Administrative Templates in Intune you can configure Microsoft Edge using  [custom settings for Windows 10 devices in Intune](/intune/configuration/custom-settings-windows-10).</span></span>

<span data-ttu-id="e0f7d-301">В этом разделе приведены следующие инструкции:</span><span class="sxs-lookup"><span data-stu-id="e0f7d-301">This section describes how to:</span></span>

1. [<span data-ttu-id="e0f7d-302">Прием ADMX-файла Microsoft Edge в Intune</span><span class="sxs-lookup"><span data-stu-id="e0f7d-302">Ingest the Microsoft Edge ADMX file into Intune</span></span>](#ingest-the-microsoft-edge-admx-file-into-intune)
2. [<span data-ttu-id="e0f7d-303">Установка политики с помощью настраиваемого кода OMA-URI в Intune</span><span class="sxs-lookup"><span data-stu-id="e0f7d-303">Set a policy using custom OMA-URI in Intune</span></span>](#set-a-policy-using-custom-oma-uri-in-intune)

> [!IMPORTANT]
> <span data-ttu-id="e0f7d-304">Для настройки одного и того же параметра Microsoft Edge в Intune не рекомендуется использовать пользовательский профиль OMA-URI и профиль административных шаблонов.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-304">As a best practice, don’t use a custom OMA-URI profile and an Administration templates profile to configure the same Microsoft Edge setting in Intune.</span></span> <span data-ttu-id="e0f7d-305">Если вы развертываете одну и ту же политику, используя пользовательский OMA-URI и профиль административного шаблона, но с разными значениями, пользователи получат непредсказуемые результаты.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-305">If you deploy the same policy using both a custom OMA-URI  and an Administrative template profile, but with different values, users will get unpredictable results.</span></span> <span data-ttu-id="e0f7d-306">Мы настоятельно рекомендуем удалить профиль OMA-URI перед использованием профиля административных шаблонов.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-306">We strongly recommend removing your OMA-URI profile before using an Administration templates profile.</span></span>

### <a name="ingest-the-microsoft-edge-admx-file-into-intune"></a><span data-ttu-id="e0f7d-307">Прием ADMX-файла Microsoft Edge в Intune</span><span class="sxs-lookup"><span data-stu-id="e0f7d-307">Ingest the Microsoft Edge ADMX file into Intune</span></span>

<span data-ttu-id="e0f7d-308">В этом разделе приведены инструкции по приему административного шаблона Microsoft Edge (файла **msedge.admx**) в Intune.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-308">This section describes how to ingest the Microsoft Edge administrative template (**msedge.admx** file) into Intune.</span></span>

> [!WARNING]
> <span data-ttu-id="e0f7d-309">Не изменяйте ADMX-файл перед его использованием.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-309">Don't modify the ADMX file before ingesting the file.</span></span>

<span data-ttu-id="e0f7d-310">Для приема ADMX-файла выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e0f7d-310">To ingest the ADMX file, follow these steps:</span></span>

1. <span data-ttu-id="e0f7d-311">Скачайте файл шаблонов политики Microsoft Edge (MicrosoftEdgePolicyTemplates.cab) на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) и извлеките содержимое.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-311">Download the Microsoft Edge policy templates file (MicrosoftEdgePolicyTemplates.cab) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise) and extract the contents.</span></span> <span data-ttu-id="e0f7d-312">Необходимый вам файл — **msedge.admx**.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-312">The file that you want to ingest is **msedge.admx**.</span></span>
2. <span data-ttu-id="e0f7d-313">Войдите [на портал Microsoft Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-313">Sign in to the [Microsoft Azure portal](https://portal.azure.com).</span></span>
3. <span data-ttu-id="e0f7d-314">Выберите **Intune** в разделе _Все службы_ или найдите Intune в поле поиска на портале.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-314">Select **Intune** from _All Services_, or search for Intune in the portal search box.</span></span>
4. <span data-ttu-id="e0f7d-315">В колонке _Microsoft Intune — Обзор_ выберите **Конфигурация устройств** | **Профили**.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-315">From _Microsoft Intune - Overview_, select **Device configuration** | **Profiles**.</span></span>
5. <span data-ttu-id="e0f7d-316">На верхней панели команд выберите **Создать профиль**.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-316">On the top command bar, select **+ Create profile**.</span></span>

   ![Создание профиля устройства](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile.png)

6. <span data-ttu-id="e0f7d-318">Предоставьте следующую информацию для профиля:</span><span class="sxs-lookup"><span data-stu-id="e0f7d-318">Provide the following profile information:</span></span>

   - <span data-ttu-id="e0f7d-319">**Имя**: введите описательное имя.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-319">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="e0f7d-320">В этом примере — "Microsoft Edge ADMX ingested configuration" (Конфигурация ADMX, принимаемая Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-320">For this example, "Microsoft Edge ADMX ingested configuration".</span></span>
   - <span data-ttu-id="e0f7d-321">**Описание**: введите необязательное описание для профиля.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-321">**Description**: Enter an optional description for the profile.</span></span>
   - <span data-ttu-id="e0f7d-322">**Платформа**: выберите "Windows 10 и более поздней версии".</span><span class="sxs-lookup"><span data-stu-id="e0f7d-322">**Platform**: Select "Windows 10 and later"</span></span>
   - <span data-ttu-id="e0f7d-323">**Тип профиля**: выберите "Настраиваемый".</span><span class="sxs-lookup"><span data-stu-id="e0f7d-323">**Profile type**: Select "Custom"</span></span>

7. <span data-ttu-id="e0f7d-324">В разделе **Пользовательские параметры OMA-URI** нажмите кнопку **Добавить**, чтобы добавить возможность приема ADMX-файла.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-324">On **Custom OMA-URI Settings**, click **Add** to add an ADMX ingestion.</span></span>

   ![Добавление возможности приема для OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-add-omauri.png)

8. <span data-ttu-id="e0f7d-326">В поле **Добавить строку** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="e0f7d-326">On **Add Row**, provide the following information:</span></span>

   - <span data-ttu-id="e0f7d-327">**Имя**: введите описательное имя.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-327">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="e0f7d-328">В этом примере используется "Microsoft Edge ADMX ingestion" (Прием ADMX-файла браузером Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-328">For this example, use "Microsoft Edge ADMX ingestion".</span></span>
   - <span data-ttu-id="e0f7d-329">**Описание**: введите необязательное описание для параметра.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-329">**Description**: Enter an optional description for the setting.</span></span>
   - <span data-ttu-id="e0f7d-330">**OMA-URI**: введите "*./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*"</span><span class="sxs-lookup"><span data-stu-id="e0f7d-330">**OMA-URI**: Enter "*./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*"</span></span>
   - <span data-ttu-id="e0f7d-331">**Тип данных**: выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="e0f7d-331">**Data type**: Select "String"</span></span>
   - <span data-ttu-id="e0f7d-332">**Значение**: эта область ввода появляется после выбора пункта **Тип данных**.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-332">**Value**: This input area appears after you select the **Data type**.</span></span> <span data-ttu-id="e0f7d-333">Откройте файл msedge.admx из файла шаблонов политики Microsoft Edge, извлеченного в ходе шага 1.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-333">Open the msedge.admx file from the Microsoft Edge policy templates file you extracted in step 1.</span></span> <span data-ttu-id="e0f7d-334">Скопируйте **ВЕСЬ текст** из файла msedge.admx и вставьте его в текстовое поле **Значение**, показанное на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-334">Copy **ALL the text** from the msedge.admx file and paste it in the **Value** text area shown in the following screenshot.</span></span>

        ![Добавление возможности приема ADMX-файла](./media/edge-cfg-with-mdm/configure-edge-intune-mdm-omauri-addrow-ingest.png)

   - <span data-ttu-id="e0f7d-336">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-336">Click **OK**.</span></span>

9. <span data-ttu-id="e0f7d-337">В колонке **Пользовательские параметры OMA-URI** нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-337">On **Custom OMA-URI Settings**, click **OK**.</span></span>
10. <span data-ttu-id="e0f7d-338">В окне **Создание профиля** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-338">On **Create profile**, click **Create**.</span></span> <span data-ttu-id="e0f7d-339">На следующем снимке экрана представлены сведения о только что созданном профиле.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-339">The next screenshot shows information about the newly created profile.</span></span>

    ![<span data-ttu-id="e0f7d-340">Сведения в новом профиле устройства</span><span class="sxs-lookup"><span data-stu-id="e0f7d-340">New device profile information</span></span> ](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-done.png)

<!--
> [!NOTE]
> You can use the preceding steps to ingest the msedgeupate.admx policy template file.
-->
### <a name="set-a-policy-using-custom-oma-uri-in-intune"></a><span data-ttu-id="e0f7d-341">Установка политики с помощью настраиваемого кода OMA-URI в Intune</span><span class="sxs-lookup"><span data-stu-id="e0f7d-341">Set a policy using custom OMA-URI in Intune</span></span>

> [!NOTE]
> <span data-ttu-id="e0f7d-342">Перед выполнением шагов, описанных в этом разделе, необходимо выполнить действия из раздела [Прием ADMX-файла Microsoft Edge в Intune](#ingest-the-microsoft-edge-admx-file-into-intune).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-342">Before using the steps in this section you must complete the steps described in [Ingest the Microsoft Edge ADMX file into Intune](#ingest-the-microsoft-edge-admx-file-into-intune).</span></span>

1. <span data-ttu-id="e0f7d-343">Войдите [на портал Microsoft Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-343">Sign in to the [Microsoft Azure portal](https://portal.azure.com).</span></span>
2. <span data-ttu-id="e0f7d-344">Выберите **Intune** в разделе _Все службы_ или найдите Intune в поле поиска на портале.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-344">Select **Intune** from _All Services_, or search for Intune in the portal search box.</span></span>
3. <span data-ttu-id="e0f7d-345">Перейдите в раздел **Intune**>**Конфигурация устройств**>**Профили**.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-345">Go to **Intune**>**Device configuration**>**Profiles**.</span></span>
4. <span data-ttu-id="e0f7d-346">Выберите профиль "Microsoft Edge ADMX ingested configuration" (Конфигурация ADMX, принимаемая Microsoft Edge) или имя, которое вы использовали для профиля.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-346">Select the "Microsoft Edge ADMX ingested configuration" profile or the name you used for the profile.</span></span>
5. <span data-ttu-id="e0f7d-347">Чтобы добавить параметры политики Microsoft Edge, необходимо открыть **Пользовательские параметры OMA-URI**.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-347">To add Microsoft Edge policy settings, you have to open **Custom OMA-URI Settings**.</span></span> <span data-ttu-id="e0f7d-348">В разделе **Управление** выберите **Свойства**, а затем выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-348">Under **Manage**, click **Properties**, and then click **Settings**.</span></span>

    ![Настройка параметров профиля](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings.png)

6. <span data-ttu-id="e0f7d-350">В разделе **Пользовательские параметры OMA-URI** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-350">On **Custom OMA-URI Settings**, click **Add**.</span></span>

    ![Добавление строки к параметрам OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings-add-row.png)

7. <span data-ttu-id="e0f7d-352">В поле **Добавить строку** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="e0f7d-352">On **Add Row**, provide the following information:</span></span>

   - <span data-ttu-id="e0f7d-353">**Имя**: введите описательное имя.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-353">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="e0f7d-354">Мы рекомендуем использовать имя политики, которую вы хотите настроить.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-354">We suggest using the policy name you want to configure.</span></span> <span data-ttu-id="e0f7d-355">В этом примере используется имя "ShowHomeButton".</span><span class="sxs-lookup"><span data-stu-id="e0f7d-355">For this example, use "ShowHomeButton".</span></span>
   - <span data-ttu-id="e0f7d-356">**Описание**: введите необязательное описание для параметра.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-356">**Description** (Optional): Enter a description for the setting.</span></span>
   - <span data-ttu-id="e0f7d-357">**OMA-URI**: введите код OMA-URI для политики.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-357">**OMA-URI**: Enter the OMA-URI for the policy.</span></span> <span data-ttu-id="e0f7d-358">Для политики "ShowHomeButton", используемой в качестве примера, используйте следующую строку: "*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*"</span><span class="sxs-lookup"><span data-stu-id="e0f7d-358">Using the for "ShowHomeButton" policy as an example, use this string: "*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*"</span></span>
   - <span data-ttu-id="e0f7d-359">**Тип данных**: выберите тип данных параметров политики.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-359">**Data type**: Select the policy settings data type.</span></span> <span data-ttu-id="e0f7d-360">Для политики "ShowHomeButton" используйте "String" (строка).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-360">For the "ShowHomeButton" policy, use "String"</span></span>
   - <span data-ttu-id="e0f7d-361">**Значение**: введите параметр, который требуется настроить для политики.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-361">**Value**: Enter the setting that you want to configure for the policy.</span></span> <span data-ttu-id="e0f7d-362">Для примера "ShowHomeButton" введите "\<enabled/>".</span><span class="sxs-lookup"><span data-stu-id="e0f7d-362">For "ShowHomeButton" example, enter "\<enabled/>".</span></span> <span data-ttu-id="e0f7d-363">На следующем снимке экрана показаны параметры для настройки политики.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-363">The following screenshot shows the settings for configuring a policy.</span></span>

        ![Добавление строки, пользовательские параметры OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-custom-omauri-setting.png)

   - <span data-ttu-id="e0f7d-365">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-365">Click **OK**.</span></span>

8. <span data-ttu-id="e0f7d-366">В колонке **Пользовательские параметры OMA-URI** нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-366">On **Custom OMA-URI Settings**, click **OK**.</span></span>
9. <span data-ttu-id="e0f7d-367">В профиле **Microsoft Edge ADMX ingested configuration (Конфигурация ADMX, принимаемая Microsoft Edge) — Свойства**" (или на имени, которое вы использовали) нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-367">On the "**Microsoft Edge ADMX ingested configuration - Properties**" profile (or the name you used), click **Save**.</span></span>

<span data-ttu-id="e0f7d-368">После создания профиля и установки свойств необходимо [назначить профиль в Microsoft Intune](/intune/configuration/device-profile-assign).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-368">After the profile is created and the properties set, you have to [assign the profile in Microsoft Intune](/intune/configuration/device-profile-assign).</span></span>

#### <a name="confirm-that-the-policy-was-set"></a><span data-ttu-id="e0f7d-369">Убедитесь, что политика настроена</span><span class="sxs-lookup"><span data-stu-id="e0f7d-369">Confirm that the policy was set</span></span>

<span data-ttu-id="e0f7d-370">Выполните следующие действия, чтобы убедиться в том, что политика Microsoft Edge использует созданный вами профиль.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-370">Use the following steps to confirm that the Microsoft Edge policy is using the profile you created.</span></span> <span data-ttu-id="e0f7d-371">(Подождите, пока Microsoft Intune распространит политику на устройство, назначенное в примере профиля "Microsoft Edge ADMX ingested configuration".)</span><span class="sxs-lookup"><span data-stu-id="e0f7d-371">(Give Microsoft Intune time to propagate the policy to a device you assigned in the "Microsoft Edge ADMX ingested configuration" profile example.)</span></span>

1. <span data-ttu-id="e0f7d-372">Откройте Microsoft Edge и перейдите по адресу *edge://policy*.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-372">Open Microsoft Edge and go to *edge://policy*.</span></span>
2. <span data-ttu-id="e0f7d-373">На странице **Политики** проверьте, указана ли политика, заданная в профиле.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-373">On the **Policies** page, see if the policy you set in the profile is listed.</span></span>
3. <span data-ttu-id="e0f7d-374">Если политика не отображается, см. раздел [Диагностика ошибок MDM в Windows 10](/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) или [Устранение неполадок с параметром политики](#troubleshoot-a-policy-setting).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-374">If your policy isn't shown, see [Diagnose MDM failures in Windows 10](/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) or [Troubleshoot a policy setting](#troubleshoot-a-policy-setting).</span></span>

#### <a name="troubleshoot-a-policy-setting"></a><span data-ttu-id="e0f7d-375">Устранение неполадок с параметром политики</span><span class="sxs-lookup"><span data-stu-id="e0f7d-375">Troubleshoot a policy setting</span></span>

<span data-ttu-id="e0f7d-376">Если политика Microsoft Edge не вступает в силу, попробуйте выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-376">If a Microsoft Edge policy isn’t taking effect, try the following steps:</span></span>

<span data-ttu-id="e0f7d-377">Откройте страницу *edge://policy* на целевом устройстве (устройство, которому назначен профиль в Microsoft Intune) и найдите политику.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-377">Open the *edge://policy* page on the target device (a device you assigned the profile to in Microsoft Intune) and search for the policy.</span></span> <span data-ttu-id="e0f7d-378">Если политики нет на странице *edge://policy*, попробуйте выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-378">If the policy isn’t on the *edge://policy* page, try the following:</span></span>

- <span data-ttu-id="e0f7d-379">Убедитесь, что политика находится в реестре и является правильной.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-379">Check that the policy is in the registry and is correct.</span></span> <span data-ttu-id="e0f7d-380">На целевом устройстве откройте редактор реестра Windows 10 (клавиша **Windows + R**, введите "*regedit*" и нажмите клавишу **Ввод**). Проверьте, правильно ли задана политика в разделе *\Software\Policies\ Microsoft\Edge*.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-380">On the target device open the Windows 10 Registry Editor (**Windows key + r**, enter “*regedit*” and then press **Enter**.) Check that the policy is correctly defined in the *\Software\Policies\ Microsoft\Edge* path.</span></span> <span data-ttu-id="e0f7d-381">Если вы не нашли политику в ожидаемом разделе, это значит, что политика была неправильно отправлена на устройство.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-381">If you don’t find the policy in the expected path, then the policy wasn’t pushed to the device correctly.</span></span>
- <span data-ttu-id="e0f7d-382">Убедитесь, что путь OMA-URI правильный, а значение является допустимой строкой XML.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-382">Check that the OMA-URI path is correct, and the value is a valid XML string.</span></span> <span data-ttu-id="e0f7d-383">Если одно из этих условий не выполнено, политика не будет отправлена на целевое устройство.</span><span class="sxs-lookup"><span data-stu-id="e0f7d-383">If either of these are incorrect the policy won’t be pushed to the target device.</span></span>

<span data-ttu-id="e0f7d-384">Дополнительные советы по устранению неполадок см. в разделе [Настройка Microsoft Intune](/intune/fundamentals/setup-steps) и [Синхронизация устройств](/intune/remote-actions/device-sync).</span><span class="sxs-lookup"><span data-stu-id="e0f7d-384">For more trouble shooting tips, see [Set up Microsoft Intune](/intune/fundamentals/setup-steps) and [Sync devices](/intune/remote-actions/device-sync).</span></span>

## <a name="see-also"></a><span data-ttu-id="e0f7d-385">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e0f7d-385">See also</span></span>

- [<span data-ttu-id="e0f7d-386">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="e0f7d-386">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="e0f7d-387">Настройка параметров политики Microsoft Edge с помощью Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="e0f7d-387">Configure Microsoft Edge policy settings with Microsoft Intune</span></span>](configure-edge-with-intune.md)
- [<span data-ttu-id="e0f7d-388">Управление мобильными устройствами</span><span class="sxs-lookup"><span data-stu-id="e0f7d-388">Mobile device management</span></span>](/windows/client-management/mdm/)
- [<span data-ttu-id="e0f7d-389">Использование настраиваемых параметров для устройств с Windows 10 в Intune</span><span class="sxs-lookup"><span data-stu-id="e0f7d-389">Use custom settings for Windows 10 devices in Intune</span></span>](/intune/configuration/custom-settings-windows-10)
- [<span data-ttu-id="e0f7d-390">Настройка политики Win32 и приложения "Мост для классических приложений"</span><span class="sxs-lookup"><span data-stu-id="e0f7d-390">Win32 and Desktop Bridge app policy configuration</span></span>](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)
- [<span data-ttu-id="e0f7d-391">Общие сведения о политиках с поддержкой ADMX</span><span class="sxs-lookup"><span data-stu-id="e0f7d-391">Understanding ADMX-backed policies</span></span>](/windows/client-management/mdm/understanding-admx-backed-policies)