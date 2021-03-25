---
title: Обновления Windows для Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Обновления Windows для Microsoft Edge.
ms.openlocfilehash: 880e5a591ee23ff852981e73fe4fc4cd815be9ad
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447153"
---
# <a name="windows-updates-to-support-the-next-version-of-microsoft-edge"></a><span data-ttu-id="3b056-103">Обновления Windows для обеспечения поддержки следующей версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3b056-103">Windows updates to support the next version of Microsoft Edge</span></span>

<span data-ttu-id="3b056-104">В этой статье описывается, как будет выполняться обновление Windows для обеспечения поддержки следующей версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3b056-104">This article describes how Windows will be updated to support the next version of Microsoft Edge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b056-105">Обратитесь к [записи блога](https://aka.ms/EdgeLegacyEOS) команды разработки продукта Microsoft Edge по поводу завершения обслуживания устаревшей версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3b056-105">Refer to the Microsoft Edge product team [blog post](https://aka.ms/EdgeLegacyEOS) about Microsoft Edge Legacy end of service.</span></span>

> [!NOTE]
> <span data-ttu-id="3b056-106">Эта статья относится к Microsoft Edge из стабильного канала.</span><span class="sxs-lookup"><span data-stu-id="3b056-106">This article applies to the Microsoft Edge Stable channel.</span></span>

## <a name="microsoft-edge-and-the-windows-release-cycle"></a><span data-ttu-id="3b056-107">Цикл выпуска Microsoft Edge и Windows</span><span class="sxs-lookup"><span data-stu-id="3b056-107">Microsoft Edge and the Windows release cycle</span></span>

<span data-ttu-id="3b056-108">Новая версия Microsoft Edge будет поддерживать более гибкие возможности обновления, которые будут предоставляться для нее чаще.</span><span class="sxs-lookup"><span data-stu-id="3b056-108">The next version of Microsoft Edge features more frequent and more flexible updating capabilities.</span></span> <span data-ttu-id="3b056-109">Так как выпуски браузера не привязаны к основным выпускам Windows, изменения будут вноситься в операционную систему, чтобы гарантировать оптимальную совместимость следующей версии Microsoft Edge с Windows.</span><span class="sxs-lookup"><span data-stu-id="3b056-109">Because browser releases aren't bound to the Windows major releases, changes will be made to the operating system to ensure that the next version of Microsoft Edge fits seamlessly into Windows.</span></span> <span data-ttu-id="3b056-110">Результатом будет выпуск обновления компонентов в 6-недельном цикле (приблизительно).</span><span class="sxs-lookup"><span data-stu-id="3b056-110">As a result, feature updates will be released on a 6-week cycle (approximately).</span></span> <span data-ttu-id="3b056-111">Обновления для системы безопасности и совместимости будут предоставляться по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="3b056-111">Security and compatibility updates will be shipped as needed.</span></span>

## <a name="updates-and-the-user-experience"></a><span data-ttu-id="3b056-112">Обновления и интерфейс</span><span class="sxs-lookup"><span data-stu-id="3b056-112">Updates and the user experience</span></span>

<span data-ttu-id="3b056-113">Обновления не будут затрагивать интерфейс до тех пор, пока следующая версия Microsoft Edge не будет установлена в рамках канала Stable.</span><span class="sxs-lookup"><span data-stu-id="3b056-113">Updates won’t change the user experience until the Stable channel of the next version of Microsoft Edge is installed.</span></span> <span data-ttu-id="3b056-114">Установка Microsoft Edge в рамках каналов Beta, Dev или Canary не приведет к внесению каких-либо изменений в Windows.</span><span class="sxs-lookup"><span data-stu-id="3b056-114">Installing Microsoft Edge Beta, Dev, or Canary won’t trigger any changes in Windows.</span></span> <span data-ttu-id="3b056-115">Эти выпуски браузера будут установлены вместе с имеющимися версиями браузера.</span><span class="sxs-lookup"><span data-stu-id="3b056-115">These browser releases will be installed alongside existing browsers.</span></span>

<span data-ttu-id="3b056-116">После применения всех обновлений и установки следующей версии Microsoft Edge в рамках канала Stable на системном уровне, в системе вступят в силу следующие изменения.</span><span class="sxs-lookup"><span data-stu-id="3b056-116">When all the updates are applied AND the Stable channel of the next version of Microsoft Edge is installed at the system-level, the following changes will take effect on the system:</span></span>

- <span data-ttu-id="3b056-117">Все закрепленные в меню "Пуск" элементы, плитки и ярлыки для текущей версии Microsoft Edge будут перенесены в следующую версию Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3b056-117">All start menu pins, tiles, and shortcuts for the current version of Microsoft Edge will migrate to the next version of Microsoft Edge.</span></span>
- <span data-ttu-id="3b056-118">Все закрепленные на панели задач элементы и ярлыки для текущей версии Microsoft Edge будут перенесены в следующую версию Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3b056-118">All taskbar pins and shortcuts for the current version of Microsoft Edge will migrate to the next version of Microsoft Edge.</span></span>
- <span data-ttu-id="3b056-119">Следующая версия Microsoft Edge будет закреплена на панели задач.</span><span class="sxs-lookup"><span data-stu-id="3b056-119">The next version of Microsoft Edge will be pinned to the taskbar.</span></span> <span data-ttu-id="3b056-120">Если текущая версия Microsoft Edge уже закреплена, она будет заменена.</span><span class="sxs-lookup"><span data-stu-id="3b056-120">If the current version of Microsoft Edge is already pinned, it will be replaced.</span></span>
- <span data-ttu-id="3b056-121">После установки новой версии Microsoft Edge на рабочий стол будет добавлен ярлык.</span><span class="sxs-lookup"><span data-stu-id="3b056-121">The next version of Microsoft Edge will add a shortcut to the desktop.</span></span> <span data-ttu-id="3b056-122">Если у текущей версии Microsoft Edge уже есть ярлык, он будет заменен.</span><span class="sxs-lookup"><span data-stu-id="3b056-122">If the current version of Microsoft Edge already has a shortcut, it will be replaced.</span></span>
- <span data-ttu-id="3b056-123">Большинство протоколов, которые Microsoft Edge обрабатывает по умолчанию, будут перенесены в следующую версию Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3b056-123">Most protocols that Microsoft Edge handles by default will be migrated to the next version of Microsoft Edge.</span></span>
- <span data-ttu-id="3b056-124">Текущая версия Microsoft Edge будет скрыта на всех интерфейсах в ОС, включая параметры, все приложения и все диалоговые окна поддержки файлов и протоколов.</span><span class="sxs-lookup"><span data-stu-id="3b056-124">Current Microsoft Edge will be hidden from all UX surfaces in the OS, including settings, all apps, and any file or protocol support dialogs.</span></span>
- <span data-ttu-id="3b056-125">При попытке запуска текущей версии Microsoft Edge будут открываться следующая версия Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3b056-125">All attempts to launch the current version of Microsoft Edge will redirect to the next version of Microsoft Edge.</span></span>

  > [!NOTE]
  > <span data-ttu-id="3b056-126">Процессы установки на уровне пользователя не будут приводить к таким результатам.</span><span class="sxs-lookup"><span data-stu-id="3b056-126">User-level installs won’t trigger these behaviors.</span></span>

<span data-ttu-id="3b056-127">Наряду с предыдущими изменениями будут происходить другие изменения независимо от того, установлен ли браузер Microsoft Edge в рамках канала Stable.</span><span class="sxs-lookup"><span data-stu-id="3b056-127">Along with the previous changes, there are changes that will happen regardless of whether the Stable channel of the next version of Microsoft Edge is installed.</span></span>

- <span data-ttu-id="3b056-128">Microsoft Edge отменит регистрацию электронных книг и протоколов XML, которые не поддерживаются в новой версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3b056-128">Microsoft Edge will de-register for the books and XML protocols that the next version of Microsoft Edge doesn't support.</span></span> <span data-ttu-id="3b056-129">Для пользователей, которые попытаются открыть эти протоколы, будет отображаться диалоговое окно с запросом на выбор приложения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3b056-129">Users attempting to open these protocols will get a dialog that prompts them to choose a default app.</span></span> <span data-ttu-id="3b056-130">Дополнительные сведения об изменениях в поддержке электронных книг см. в разделе [Скачайте приложение для работы с файлами в формате ePub, чтобы продолжить чтение](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsupport.microsoft.com%2Fhelp%2F4517840&data=02%7C01%7Cv-danwes%40microsoft.com%7Cc9f8571b880549c30fcf08d72be5eaf9%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637026138803983526&sdata=qtb3DvVZQ6H%2FFXnBievkl%2B%2BngAQXwl340PcH8kRc3y4%3D&reserved=0).</span><span class="sxs-lookup"><span data-stu-id="3b056-130">Learn more about changes to books support at [Download an ePub app to keep reading e-books](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsupport.microsoft.com%2Fhelp%2F4517840&data=02%7C01%7Cv-danwes%40microsoft.com%7Cc9f8571b880549c30fcf08d72be5eaf9%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637026138803983526&sdata=qtb3DvVZQ6H%2FFXnBievkl%2B%2BngAQXwl340PcH8kRc3y4%3D&reserved=0).</span></span>

## <a name="timeline"></a><span data-ttu-id="3b056-131">Информация о сроках</span><span class="sxs-lookup"><span data-stu-id="3b056-131">Timeline</span></span>

<span data-ttu-id="3b056-132">Изменения, необходимые для реализации поддержки описанного интерфейса, будут внесены в составе трех обновлений для разных версий Windows.</span><span class="sxs-lookup"><span data-stu-id="3b056-132">The changes needed to support the described experience will be delivered with three updates for different versions of Windows.</span></span>

### <a name="windows-versions-1903-and-1909"></a><span data-ttu-id="3b056-133">Windows версий 1903 и 1909</span><span class="sxs-lookup"><span data-stu-id="3b056-133">Windows versions 1903 and 1909</span></span>

- <span data-ttu-id="3b056-134">Первый набор изменений в необязательном обновлении за июль 2019 года, предоставленном вместе с обновлением для системы безопасности за август 2019 года.</span><span class="sxs-lookup"><span data-stu-id="3b056-134">First set of changes in optional July 2019 update, delivered with the August 2019 security update.</span></span>
- <span data-ttu-id="3b056-135">Второй набор изменений в необязательном обновлении за август 2019 года, предоставленном вместе с обновлением для системы безопасности за сентябрь 2019 года.</span><span class="sxs-lookup"><span data-stu-id="3b056-135">Second set of changes in the optional August 2019 update, delivered with the September 2019 security update.</span></span>

  > [!NOTE]
  > <span data-ttu-id="3b056-136">Вместе с этим обновлением Microsoft Edge отменит регистрацию протокола XML.</span><span class="sxs-lookup"><span data-stu-id="3b056-136">This is the update where Microsoft Edge will de-register for the XML protocol.</span></span>

- <span data-ttu-id="3b056-137">Третий набор изменений в необязательном обновлении за сентябрь 2019 года, предоставленном вместе с обновлением для системы безопасности за октябрь 2019 года.</span><span class="sxs-lookup"><span data-stu-id="3b056-137">Third set of changes in the optional September 2019 update, delivered with the October 2019 security update.</span></span>

  > [!NOTE]
  > <span data-ttu-id="3b056-138">Вместе с этим обновлением Microsoft Edge перестанет поддерживать электронные книги.</span><span class="sxs-lookup"><span data-stu-id="3b056-138">This is the update where Microsoft Edge will no longer support eBooks.</span></span>

### <a name="windows-versions-1709-1803-and-1809"></a><span data-ttu-id="3b056-139">Windows версий 1709, 1803 и 1809</span><span class="sxs-lookup"><span data-stu-id="3b056-139">Windows versions 1709, 1803, and 1809</span></span>

- <span data-ttu-id="3b056-140">Первый набор изменений в необязательном обновлении за август 2019 года, предоставленном вместе с обновлением для системы безопасности за сентябрь 2019 года.</span><span class="sxs-lookup"><span data-stu-id="3b056-140">First set of changes in an optional August 2019 update, delivered with the September 2019 security update.</span></span>
- <span data-ttu-id="3b056-141">Второй набор изменений в необязательном обновлении за сентябрь 2019 года, предоставленном вместе с обновлением для системы безопасности за октябрь 2019 года.</span><span class="sxs-lookup"><span data-stu-id="3b056-141">Second set of changes in an optional September 2019 update, delivered with the October 2019 security update.</span></span>

  > [!NOTE]
  > <span data-ttu-id="3b056-142">Вместе с этим обновлением Microsoft Edge отменит регистрацию протокола XML.</span><span class="sxs-lookup"><span data-stu-id="3b056-142">This is the update where Microsoft Edge will de-register for the XML protocol.</span></span>

- <span data-ttu-id="3b056-143">Третий набор изменений в необязательном обновлении за октябрь 2019 года, предоставленном вместе с обновлением для системы безопасности за ноябрь 2019 года.</span><span class="sxs-lookup"><span data-stu-id="3b056-143">Third set of changes in an optional October 2019 update, delivered with the November 2019 security update.</span></span>

  > [!NOTE]
  > <span data-ttu-id="3b056-144">Вместе с этим обновлением Microsoft Edge перестанет поддерживать электронные книги.</span><span class="sxs-lookup"><span data-stu-id="3b056-144">This is the update where Microsoft Edge will no longer support eBooks.</span></span>

<span data-ttu-id="3b056-145">В следующей таблице приведены подробные сведения о соответствующих обновлениях в каждом наборе изменений.</span><span class="sxs-lookup"><span data-stu-id="3b056-145">The following table gives the details for specific updates in each set of changes.</span></span>

| <span data-ttu-id="3b056-146">Windows 10</span><span class="sxs-lookup"><span data-stu-id="3b056-146">Windows 10</span></span> | <span data-ttu-id="3b056-147">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3b056-147">More Information</span></span> | <span data-ttu-id="3b056-148">Требуется скачивание</span><span class="sxs-lookup"><span data-stu-id="3b056-148">Required Download</span></span> |
|--|--|--|
| <span data-ttu-id="3b056-149">Версия 1709</span><span class="sxs-lookup"><span data-stu-id="3b056-149">Version 1709</span></span> | [<span data-ttu-id="3b056-150">KB4525241</span><span class="sxs-lookup"><span data-stu-id="3b056-150">KB4525241</span></span>](https://support.microsoft.com/help/4525241/windows-10-update-kb4525241) | [<span data-ttu-id="3b056-151">Накопительный пакет обновления для Windows 10 версии 1709</span><span class="sxs-lookup"><span data-stu-id="3b056-151">Cumulative Update for Windows 10 Version 1709</span></span>](https://www.catalog.update.microsoft.com/Search.aspx?q=4525241) |
| <span data-ttu-id="3b056-152">Версия 1803</span><span class="sxs-lookup"><span data-stu-id="3b056-152">Version 1803</span></span>  | [<span data-ttu-id="3b056-153">KB4525237</span><span class="sxs-lookup"><span data-stu-id="3b056-153">KB4525237</span></span>](https://support.microsoft.com/help/4525237/windows-10-update-kb4525237) | [<span data-ttu-id="3b056-154">Накопительный пакет обновления для Windows 10 версии 1803</span><span class="sxs-lookup"><span data-stu-id="3b056-154">Cumulative Update for Windows 10 Version 1803</span></span>](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4525237) |
| <span data-ttu-id="3b056-155">Версия 1809</span><span class="sxs-lookup"><span data-stu-id="3b056-155">Version 1809</span></span>  | [<span data-ttu-id="3b056-156">KB4523205</span><span class="sxs-lookup"><span data-stu-id="3b056-156">KB4523205</span></span>](https://support.microsoft.com/help/4523205/windows-10-update-kb4523205) | [<span data-ttu-id="3b056-157">Накопительный пакет обновления для Windows 10 версии 1809</span><span class="sxs-lookup"><span data-stu-id="3b056-157">Cumulative Update for Windows 10 Version 1809</span></span>](https://www.catalog.update.microsoft.com/Search.aspx?q=4523205) |
| <span data-ttu-id="3b056-158">Версии 1903 и 1909</span><span class="sxs-lookup"><span data-stu-id="3b056-158">Version 1903 and 1909</span></span> |[<span data-ttu-id="3b056-159">KB4517389</span><span class="sxs-lookup"><span data-stu-id="3b056-159">KB4517389</span></span>](https://support.microsoft.com/help/4517389/windows-10-update-kb4517389)  | [<span data-ttu-id="3b056-160">Накопительный пакет обновления для Windows 10 версий 1903 и 1909</span><span class="sxs-lookup"><span data-stu-id="3b056-160">Cumulative Update for Windows 10 Version 1903 and 1909</span></span>](https://www.catalog.update.microsoft.com/Search.aspx?q=4517389) |

## <a name="see-also"></a><span data-ttu-id="3b056-161">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3b056-161">See also</span></span>

- [<span data-ttu-id="3b056-162">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="3b056-162">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="3b056-163">Документация по Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3b056-163">Microsoft Edge documentation</span></span>](./index.yml)