---
title: Сброс данных Microsoft Edge
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 04/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Как сбросить данные Microsoft Edge в облаке
ms.openlocfilehash: 6dcbf2a80705aa87a35b50d41e0dbaa266ed4384
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617329"
---
# <a name="reset-microsoft-edge-data-in-the-cloud"></a><span data-ttu-id="2e944-103">Сброс данных Microsoft Edge в облаке</span><span class="sxs-lookup"><span data-stu-id="2e944-103">Reset Microsoft Edge data in the cloud</span></span>

<span data-ttu-id="2e944-104">В этой статье описаны действия по сбросу данных Microsoft Edge в облаке.</span><span class="sxs-lookup"><span data-stu-id="2e944-104">This article describes the steps for resetting your Microsoft Edge data in the cloud.</span></span>

> [!NOTE]
> <span data-ttu-id="2e944-105">Эта статья относится к Microsoft Edge версии 88 или более поздней, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="2e944-105">This article applies to Microsoft Edge version 88 or later unless otherwise noted.</span></span>

> [!NOTE]
> <span data-ttu-id="2e944-106">Если ваш клиент находится в среде GCC Mod, администратору клиента необходимо будет подать запрос в службу поддержки Майкрософт, чтобы сбросить данные.</span><span class="sxs-lookup"><span data-stu-id="2e944-106">If your tenant is in a GCC Mod environment, your tenant admin will need to file a support request with Microsoft to reset your data.</span></span>

## <a name="overview"></a><span data-ttu-id="2e944-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="2e944-107">Overview</span></span>

<span data-ttu-id="2e944-108">Существуют ситуации, в которых необходимо сбросить данные Microsoft Edge в облаке.</span><span class="sxs-lookup"><span data-stu-id="2e944-108">There are situations in which you want to reset your Microsoft Edge data in the cloud.</span></span> <span data-ttu-id="2e944-109">Например, вы хотите синхронизировать свои данные, но Microsoft Edge сообщает, что не может это сделать.</span><span class="sxs-lookup"><span data-stu-id="2e944-109">For example,  you want to synchronize your data, but Microsoft Edge reports that it is unable to synchronize the data.</span></span> <span data-ttu-id="2e944-110">Кроме того, может потребоваться удалить данные из облака Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2e944-110">Or you might want to make sure that your data is removed from Microsoft’s cloud.</span></span> <span data-ttu-id="2e944-111">В обоих случаях Microsoft Edge позволяет выполнить сброс данных в облаке.</span><span class="sxs-lookup"><span data-stu-id="2e944-111">In both cases, Microsoft Edge lets you perform a cloud data reset.</span></span>

## <a name="back-up-your-favorites"></a><span data-ttu-id="2e944-112">Создание резервной копии избранного</span><span class="sxs-lookup"><span data-stu-id="2e944-112">Back up your favorites</span></span>

<span data-ttu-id="2e944-113">Перед выполнением сброса рекомендуется создать резервную копию избранного.</span><span class="sxs-lookup"><span data-stu-id="2e944-113">Before performing a reset, we recommend that you back up your favorites.</span></span> <span data-ttu-id="2e944-114">Для этого выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2e944-114">Use the following steps to back up your favorites.</span></span>

1. <span data-ttu-id="2e944-115">В Microsoft Edge выберите **Параметры и другое > Избранное > Дополнительные параметры > Экспорт избранного**.</span><span class="sxs-lookup"><span data-stu-id="2e944-115">In Microsoft Edge, select **Settings and more > Favorites > More options > Export favorites**.</span></span>
2. <span data-ttu-id="2e944-116">Выберите файл, в который вы хотите сохранить избранное.</span><span class="sxs-lookup"><span data-stu-id="2e944-116">Choose the file to where you want to save your favorites.</span></span> <span data-ttu-id="2e944-117">Вы можете ввести собственное имя файла или использовать имя, которое Microsoft Edge предоставляет по умолчанию, — "favorites_month_day_year.html".</span><span class="sxs-lookup"><span data-stu-id="2e944-117">You can type your own filename or use the name that Microsoft Edge provides by default,  "favorites_month_day_year.html" as a filename.</span></span> <span data-ttu-id="2e944-118">Например, "favorites_12_17_20.html".</span><span class="sxs-lookup"><span data-stu-id="2e944-118">For example, "favorites_12_17_20.html".</span></span> <span data-ttu-id="2e944-119">Если позднее вам потребуется восстановить избранное, вы сможете восстановить его из этого файла.</span><span class="sxs-lookup"><span data-stu-id="2e944-119">If you need to restore your favorites later, you can do so from that file.</span></span>
3. <span data-ttu-id="2e944-120">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2e944-120">Click **Save**.</span></span>

## <a name="perform-a-reset-to-fix-a-synchronization-problem"></a><span data-ttu-id="2e944-121">Выполнение сброса для устранения проблемы с синхронизацией</span><span class="sxs-lookup"><span data-stu-id="2e944-121">Perform a reset to fix a synchronization problem</span></span>

<span data-ttu-id="2e944-122">Если Microsoft Edge сообщает, что не может синхронизировать ваши данные, и предлагает их сбросить, выполните сброс, чтобы устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="2e944-122">If Microsoft Edge reports that it can't synchronize your data and suggests resetting your data, perform a reset to fix the problem.</span></span>

<span data-ttu-id="2e944-123">Для этого выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2e944-123">Use the following steps to do a reset.</span></span>

1. <span data-ttu-id="2e944-124">Сначала убедитесь, что вы вышли из Microsoft Edge на всех ваших устройствах, в том числе мобильных, за исключением устройства, на котором выполняется сброс.</span><span class="sxs-lookup"><span data-stu-id="2e944-124">First, make sure that you’re signed out of Microsoft Edge on all your devices, including your mobile devices, except the device you are performing the reset on.</span></span> <span data-ttu-id="2e944-125">Чтобы выйти из Microsoft Edge, выберите **Параметры и другое > Параметры > Выход**. При выходе не выбирайте параметр очистки избранного, параметров и т. д. с локального устройства.</span><span class="sxs-lookup"><span data-stu-id="2e944-125">To sign out of Microsoft Edge, select **Settings and more > Settings > Sign out**. When signing out, do not select the option to clear favorites, settings, and etc. from your local device.</span></span>
2. <span data-ttu-id="2e944-126">Выполнив выход на всех остальных устройствах, откройте Microsoft Edge на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="2e944-126">After you sign out of all your other devices, open Microsoft Edge on your desktop.</span></span> <span data-ttu-id="2e944-127">Выберите **Параметры и другое > Синхронизация > Сбросить синхронизацию**. В появившемся диалоговом окне выберите параметр возобновления синхронизации после сброса данных, а затем нажмите кнопку **Сбросить**.</span><span class="sxs-lookup"><span data-stu-id="2e944-127">**Select Settings and more > Sync > Reset sync**. In the resulting dialog box, choose to resume sync after resetting data, and then select **Reset**.</span></span>

## <a name="perform-a-reset-to-remove-your-data-from-microsofts-cloud"></a><span data-ttu-id="2e944-128">Выполнение сброса для удаления данных из облака Майкрософт</span><span class="sxs-lookup"><span data-stu-id="2e944-128">Perform a reset to remove your data from Microsoft’s cloud</span></span>

<span data-ttu-id="2e944-129">Если необходимо удалить данные из облака Майкрософт, выполните следующие действия по сбросу данных.</span><span class="sxs-lookup"><span data-stu-id="2e944-129">If you want to remove your data from Microsoft’s cloud, use the following steps to do a reset.</span></span>

1. <span data-ttu-id="2e944-130">Остановите синхронизацию на всех устройствах, за исключением устройства, на котором выполняется сброс.</span><span class="sxs-lookup"><span data-stu-id="2e944-130">Stop synchronization on devices except the device you are performing the reset on.</span></span>  <span data-ttu-id="2e944-131">В Microsoft Edge выберите **Параметры и другое > Параметры > Синхронизация > Отключить синхронизацию**.</span><span class="sxs-lookup"><span data-stu-id="2e944-131">In Microsoft Edge, select **Settings and more > Settings > Sync > Turn off sync**.</span></span>  
2. <span data-ttu-id="2e944-132">После остановки синхронизации выберите **Параметры и другое > Синхронизация > Сбросить синхронизацию**. В появившемся диалоговом окне **не** выбирайте параметр возобновления синхронизации после сброса данных.</span><span class="sxs-lookup"><span data-stu-id="2e944-132">After you stop synchronization, select **Settings and more > Sync > Reset sync**. In the resulting dialog box, **do not** choose to resume sync after resetting data.</span></span> <span data-ttu-id="2e944-133">Нажмите кнопку **Сбросить**.</span><span class="sxs-lookup"><span data-stu-id="2e944-133">Select **Reset**.</span></span>

## <a name="what-to-expect-during-and-after-a-data-reset"></a><span data-ttu-id="2e944-134">Чего ожидать во время и после сброса данных</span><span class="sxs-lookup"><span data-stu-id="2e944-134">What to expect during and after a data reset</span></span>

<span data-ttu-id="2e944-135">Сброс данных может занять от нескольких секунд до нескольких минут в зависимости от объема сохраненных данных в облаке Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2e944-135">A data reset can take from a few seconds to a few minutes, depending on how much data you have stored in Microsoft’s cloud.</span></span> <span data-ttu-id="2e944-136">В некоторых случаях может появиться сообщение о том, что сброс не удалось выполнить, и предложение повторить попытку.</span><span class="sxs-lookup"><span data-stu-id="2e944-136">In some cases, you might see a message saying that a reset could not be completed and a suggestion to reset again.</span></span> <span data-ttu-id="2e944-137">В этом случае подождите несколько часов и попробуйте сбросить данные снова.</span><span class="sxs-lookup"><span data-stu-id="2e944-137">In this case, wait a few hours and try to reset the data again.</span></span> <span data-ttu-id="2e944-138">Если вы по-прежнему не можете сбросить данные, обратитесь в службу поддержки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2e944-138">If you are still unable to reset your data, contact Microsoft Edge Support.</span></span>

<span data-ttu-id="2e944-139">После выполнения сброса данных данные с вашего устройства снова будут синхронизироваться, если вы выбрали параметр возобновления синхронизации после сброса.</span><span class="sxs-lookup"><span data-stu-id="2e944-139">After a data reset has been successfully completed, data will once again synchronize from your device if you chose to resume sync after the reset.</span></span> <span data-ttu-id="2e944-140">Если потребуется синхронизировать данные с других устройств, вам нужно будет войти на них снова.</span><span class="sxs-lookup"><span data-stu-id="2e944-140">You will need to sign back in on your other devices if you want to sync from those devices.</span></span> <span data-ttu-id="2e944-141">Однако если вы решили не возобновлять синхронизацию, данные Microsoft Edge будут удалены из облака и ваши данные больше не будут синхронизироваться.</span><span class="sxs-lookup"><span data-stu-id="2e944-141">However, if you didn’t choose to resume sync, then your Microsoft Edge data is removed from the cloud and your data will no longer synchronize.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e944-142">См. также</span><span class="sxs-lookup"><span data-stu-id="2e944-142">See also</span></span>

- [<span data-ttu-id="2e944-143">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="2e944-143">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="2e944-144">Синхронизация Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="2e944-144">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)