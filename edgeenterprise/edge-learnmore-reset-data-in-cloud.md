---
title: Сброс данных Microsoft Edge
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 07/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Как сбросить данные Microsoft Edge в облаке
ms.openlocfilehash: dc6c0ae1b1bc31228e9b9b1de315a19e99149134
ms.sourcegitcommit: 2a00571483e1d169b2b3b59f4fce43262f460a9a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2021
ms.locfileid: "11643744"
---
# <a name="reset-microsoft-edge-data-in-the-cloud"></a><span data-ttu-id="a1a1c-103">Сброс данных Microsoft Edge в облаке</span><span class="sxs-lookup"><span data-stu-id="a1a1c-103">Reset Microsoft Edge data in the cloud</span></span>

<span data-ttu-id="a1a1c-104">В этой статье описаны действия по сбросу данных Microsoft Edge в облаке.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-104">This article describes the steps for resetting your Microsoft Edge data in the cloud.</span></span>

> [!NOTE]
> <span data-ttu-id="a1a1c-105">Эта статья относится к Microsoft Edge версии 88 или более поздней, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-105">This article applies to Microsoft Edge version 88 or later unless otherwise noted.</span></span>

> [!NOTE]
> <span data-ttu-id="a1a1c-106">Если ваш клиент находится в среде GCC Mod, администратору клиента необходимо будет подать запрос в службу поддержки Майкрософт, чтобы сбросить данные.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-106">If your tenant is in a GCC Mod environment, your tenant admin will need to file a support request with Microsoft to reset your data.</span></span>

## <a name="overview"></a><span data-ttu-id="a1a1c-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="a1a1c-107">Overview</span></span>

<span data-ttu-id="a1a1c-108">Существуют ситуации, в которых необходимо сбросить данные Microsoft Edge в облаке.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-108">There are situations in which you want to reset your Microsoft Edge data in the cloud.</span></span> <span data-ttu-id="a1a1c-109">Например, вы хотите синхронизировать свои данные, но Microsoft Edge сообщает, что не может это сделать.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-109">For example,  you want to synchronize your data, but Microsoft Edge reports that it is unable to synchronize the data.</span></span> <span data-ttu-id="a1a1c-110">Кроме того, может потребоваться удалить данные из облака Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-110">Or you might want to make sure that your data is removed from Microsoft’s cloud.</span></span> <span data-ttu-id="a1a1c-111">В обоих случаях Microsoft Edge позволяет выполнить сброс данных в облаке.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-111">In both cases, Microsoft Edge lets you perform a cloud data reset.</span></span>

## <a name="back-up-your-favorites"></a><span data-ttu-id="a1a1c-112">Создание резервной копии избранного</span><span class="sxs-lookup"><span data-stu-id="a1a1c-112">Back up your favorites</span></span>

<span data-ttu-id="a1a1c-113">Перед выполнением сброса рекомендуется создать резервную копию избранного.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-113">Before performing a reset, we recommend that you back up your favorites.</span></span> <span data-ttu-id="a1a1c-114">Для этого выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-114">Use the following steps to back up your favorites.</span></span>

1. <span data-ttu-id="a1a1c-115">В правом верхнем углу Microsoft Edge выберите **Настройки и прочее > Избранное > Дополнительные параметры > Экспорт избранного**.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-115">In the upper-right corner of Microsoft Edge, select **Settings and more > Favorites > More options > Export favorites**.</span></span>
2. <span data-ttu-id="a1a1c-116">Выберите файл, в который вы хотите сохранить избранное.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-116">Choose the file to where you want to save your favorites.</span></span> <span data-ttu-id="a1a1c-117">Вы можете ввести собственное имя файла или использовать имя, которое Microsoft Edge предоставляет по умолчанию, — "favorites_month_day_year.html".</span><span class="sxs-lookup"><span data-stu-id="a1a1c-117">You can type your own filename or use the name that Microsoft Edge provides by default,  "favorites_month_day_year.html" as a filename.</span></span> <span data-ttu-id="a1a1c-118">Например, "favorites_12_17_20.html".</span><span class="sxs-lookup"><span data-stu-id="a1a1c-118">For example, "favorites_12_17_20.html".</span></span> <span data-ttu-id="a1a1c-119">Если позднее вам потребуется восстановить избранное, вы сможете восстановить его из этого файла.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-119">If you need to restore your favorites later, you can do so from that file.</span></span>
3. <span data-ttu-id="a1a1c-120">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-120">Click **Save**.</span></span>

## <a name="perform-a-reset-to-fix-a-synchronization-problem"></a><span data-ttu-id="a1a1c-121">Выполнение сброса для устранения проблемы с синхронизацией</span><span class="sxs-lookup"><span data-stu-id="a1a1c-121">Perform a reset to fix a synchronization problem</span></span>

<span data-ttu-id="a1a1c-122">Если Microsoft Edge сообщает, что не может синхронизировать ваши данные, и предлагает их сбросить, выполните сброс, чтобы устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-122">If Microsoft Edge reports that it can't synchronize your data and suggests resetting your data, perform a reset to fix the problem.</span></span>

<span data-ttu-id="a1a1c-123">Для этого выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-123">Use the following steps to do a reset.</span></span>

1. <span data-ttu-id="a1a1c-124">Сначала убедитесь, что вы вышли из Microsoft Edge на всех ваших устройствах, в том числе мобильных, за исключением устройства, на котором выполняется сброс.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-124">First, make sure that you’re signed out of Microsoft Edge on all your devices, including your mobile devices, except the device you are performing the reset on.</span></span> <span data-ttu-id="a1a1c-125">Чтобы выйти из Microsoft Edge, в правом верхнем углу Microsoft Edge выберите **Настройки и прочее > Настройки > Выход**. При выходе не выбирайте параметр очистки избранного, настроек и других данных с локального устройства.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-125">To sign out of Microsoft Edge, in the upper-right corner of Microsoft Edge select **Settings and more > Settings > Sign out**. When signing out, do not select the option to clear favorites, settings, and etc. from your local device.</span></span>
2. <span data-ttu-id="a1a1c-126">Выполнив выход на всех остальных устройствах, откройте Microsoft Edge на компьютере. В правом верхнем углу Microsoft Edge выберите **Настройки и прочее > Синхронизация > Сбросить синхронизацию**. В появившемся диалоговом окне выберите возобновление синхронизации после сброса данных, а затем нажмите **Сбросить**.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-126">After you sign out of all your other devices, open Microsoft Edge on your desktop.In the upper-right corner of Microsoft Edge **Select Settings and more > Sync > Reset sync**. In the resulting dialog box, choose to resume sync after resetting data, and then select **Reset**.</span></span>

## <a name="perform-a-reset-to-remove-your-data-from-microsofts-cloud"></a><span data-ttu-id="a1a1c-127">Выполнение сброса для удаления данных из облака Майкрософт</span><span class="sxs-lookup"><span data-stu-id="a1a1c-127">Perform a reset to remove your data from Microsoft’s cloud</span></span>

<span data-ttu-id="a1a1c-128">Если необходимо удалить данные из облака Майкрософт, выполните следующие действия по сбросу данных.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-128">If you want to remove your data from Microsoft’s cloud, use the following steps to do a reset.</span></span>

1. <span data-ttu-id="a1a1c-129">Остановите синхронизацию на всех устройствах, за исключением устройства, на котором выполняется сброс.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-129">Stop synchronization on devices except the device you are performing the reset on.</span></span>  <span data-ttu-id="a1a1c-130">В правом верхнем углу Microsoft Edge выберите **Настройки и прочее > Настройки > Синхронизация > Отключить синхронизацию**.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-130">In the upper-right corner of Microsoft Edge, select **Settings and more > Settings > Sync > Turn off sync**.</span></span>  
2. <span data-ttu-id="a1a1c-131">После остановки синхронизации в правом верхнем углу Microsoft Edge выберите **Настройки и прочее > Синхронизация > Сбросить синхронизацию**. В появившемся диалоговом окне **не** выбирайте возобновление синхронизации после сброса данных.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-131">After you stop synchronization, in the upper-right corner of Microsoft Edge select **Settings and more > Sync > Reset sync**. In the resulting dialog box, **do not** choose to resume sync after resetting data.</span></span> <span data-ttu-id="a1a1c-132">Нажмите **Сбросить**.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-132">Select **Reset**.</span></span>

## <a name="what-to-expect-during-and-after-a-data-reset"></a><span data-ttu-id="a1a1c-133">Чего ожидать во время и после сброса данных</span><span class="sxs-lookup"><span data-stu-id="a1a1c-133">What to expect during and after a data reset</span></span>

<span data-ttu-id="a1a1c-134">Сброс данных может занять от нескольких секунд до нескольких минут в зависимости от объема сохраненных данных в облаке Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-134">A data reset can take from a few seconds to a few minutes, depending on how much data you have stored in Microsoft’s cloud.</span></span> <span data-ttu-id="a1a1c-135">В некоторых случаях может появиться сообщение о том, что сброс не удалось выполнить, и предложение повторить попытку.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-135">In some cases, you might see a message saying that a reset could not be completed and a suggestion to reset again.</span></span> <span data-ttu-id="a1a1c-136">В этом случае подождите несколько часов и попробуйте сбросить данные снова.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-136">In this case, wait a few hours and try to reset the data again.</span></span> <span data-ttu-id="a1a1c-137">Если вы по-прежнему не можете сбросить данные, обратитесь в службу поддержки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-137">If you are still unable to reset your data, contact Microsoft Edge Support.</span></span>

<span data-ttu-id="a1a1c-138">После выполнения сброса данных данные с вашего устройства снова будут синхронизироваться, если вы выбрали параметр возобновления синхронизации после сброса.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-138">After a data reset has been successfully completed, data will once again synchronize from your device if you chose to resume sync after the reset.</span></span> <span data-ttu-id="a1a1c-139">Если потребуется синхронизировать данные с других устройств, вам нужно будет войти на них снова.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-139">You will need to sign back in on your other devices if you want to sync from those devices.</span></span> <span data-ttu-id="a1a1c-140">Однако если вы решили не возобновлять синхронизацию, данные Microsoft Edge будут удалены из облака и ваши данные больше не будут синхронизироваться.</span><span class="sxs-lookup"><span data-stu-id="a1a1c-140">However, if you didn’t choose to resume sync, then your Microsoft Edge data is removed from the cloud and your data will no longer synchronize.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1a1c-141">См. также</span><span class="sxs-lookup"><span data-stu-id="a1a1c-141">See also</span></span>

- [<span data-ttu-id="a1a1c-142">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="a1a1c-142">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="a1a1c-143">Синхронизация Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="a1a1c-143">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)