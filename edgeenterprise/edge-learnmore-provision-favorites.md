---
title: Подготовка избранного для Microsoft Edge
ms.author: capoon
author: dan-wesley
manager: abutcher
ms.date: 09/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Подготовка избранного для Microsoft Edge
ms.openlocfilehash: 94bd42573bdbc0fd1b971ded1c82e5fe152acc54
ms.sourcegitcommit: 854dd73eb168960c0eb4b483f81a8efe88806a64
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/29/2020
ms.locfileid: "11088719"
---
# <span data-ttu-id="37a7f-103">Подготовка избранного для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="37a7f-103">Provision favorites for Microsoft Edge</span></span>

<span data-ttu-id="37a7f-104">С учетом отзывов пользователей были внесены улучшения в подготовку избранного.</span><span class="sxs-lookup"><span data-stu-id="37a7f-104">Based on customer feedback, we've made improvements to provisioning favorites.</span></span> <span data-ttu-id="37a7f-105">Начиная с Microsoft Edge версии 85 администраторам больше не нужно вручную создавать файл для подготовки избранного.</span><span class="sxs-lookup"><span data-stu-id="37a7f-105">Starting with Microsoft Edge version 85, Admins no longer have to manually craft a file to provision favorites.</span></span> <span data-ttu-id="37a7f-106">Администраторы могут добавлять избранное и папки с помощью пользовательского интерфейса Microsoft Edge для создания файла, который можно экспортировать в групповую политику.</span><span class="sxs-lookup"><span data-stu-id="37a7f-106">Admins can add favorites and folders using the Microsoft Edge UI to generate a file that can be exported to a group policy.</span></span>

<span data-ttu-id="37a7f-107">В этой статье описано, как подготовить набор избранного и папок для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="37a7f-107">This article describes how to provision a set of favorites and folders for your organization.</span></span> <span data-ttu-id="37a7f-108">Можно использовать политику [Настроить избранное](https://docs.microsoft.com//DeployEdge/microsoft-edge-policies#configure-favorites) для подготовки избранного и папок.</span><span class="sxs-lookup"><span data-stu-id="37a7f-108">You can use the [Configure favorites](https://docs.microsoft.com//DeployEdge/microsoft-edge-policies#configure-favorites) policy to provision favorites and folders.</span></span>

> [!NOTE]
> <span data-ttu-id="37a7f-109">Эта статья относится к Microsoft Edge версии 85 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="37a7f-109">This article applies to Microsoft Edge version 85 or later.</span></span>

## <span data-ttu-id="37a7f-110">Предварительные требования и рекомендации</span><span class="sxs-lookup"><span data-stu-id="37a7f-110">Prerequisites and recommendations</span></span>

- <span data-ttu-id="37a7f-111">Microsoft Edge версии 85 с соответствующим административным шаблоном, установленным для групповых политик.</span><span class="sxs-lookup"><span data-stu-id="37a7f-111">Microsoft Edge version 85 with the appropriate administrative template installed for group policies.</span></span>
- <span data-ttu-id="37a7f-112">Рекомендуется использовать новый профиль в Microsoft Edge для подготовки избранного.</span><span class="sxs-lookup"><span data-stu-id="37a7f-112">We recommend that you use a new profile in Microsoft Edge to provision these favorites.</span></span> <span data-ttu-id="37a7f-113">Все избранное, сохраненное вместе с профилем, будет включено в экспорт.</span><span class="sxs-lookup"><span data-stu-id="37a7f-113">All favorites that are saved with the profile will be included in the export.</span></span>  

## <span data-ttu-id="37a7f-114">Подготовка избранного и папок</span><span class="sxs-lookup"><span data-stu-id="37a7f-114">Provision favorites and folders</span></span>

<span data-ttu-id="37a7f-115">Выполните следующие действия для подготовки избранного и папок для ваших пользователей.</span><span class="sxs-lookup"><span data-stu-id="37a7f-115">Use the following steps to provision favorites and folders for your users.</span></span>

1. <span data-ttu-id="37a7f-116">Перейдите в адресную строку Microsoft Edge и введите этот URL-адрес: *edge://flags/#edge-favorites-admin-export*.</span><span class="sxs-lookup"><span data-stu-id="37a7f-116">Go to the Microsoft Edge address bar and type this URL: *edge://flags/#edge-favorites-admin-export*.</span></span>
2. <span data-ttu-id="37a7f-117">В разделе **Экспорт конфигурации избранного для администраторов**, выберите \*\*Включено \*\* из раскрывающегося списка и затем нажмите **Перезапустить**.</span><span class="sxs-lookup"><span data-stu-id="37a7f-117">Under **Favorites configuration export for administrators**, pick **Enabled** from the dropdown list and then click **Restart**.</span></span>

3. <span data-ttu-id="37a7f-118">Перейдите на страницу **Избранное** на странице *edge://favorites*, чтобы добавить избранное и папки, которые вы хотите подготовить.</span><span class="sxs-lookup"><span data-stu-id="37a7f-118">Go to the **Favorites** page at *edge://favorites* so you can add the favorites and folders that you want to provision.</span></span>

<!--
4. On the **Favorites bar**, click **Add folder**. The folder structure of favorites that are set in the profile you're using will be reflected in the folder you provision for your users. The next screenshot shows "Managed favorites", the folder we'll use to provision favorites.

   ![Add a folder](media/edge-learnmore-provision-favorites/provision-favorites-add-folder.png)

   > [!TIP]
   > Add existing folders that contain favorites you want to provision for your users.

5. Select "Managed favorites" and then click **Add favorite**. The next screenshot shows the favorite we've added.

   ![Add a favorite](media/edge-learnmore-provision-favorites/provision-favorites-add-favorite.png)-->

4. <span data-ttu-id="37a7f-119">Когда вы закончите добавлять избранное и папки, экспортируете их, чтобы их можно было использовать в политике **Настроить избранное**.</span><span class="sxs-lookup"><span data-stu-id="37a7f-119">When you finish adding favorites and folders you'll export them so they can be used by the **Configure favorites** policy.</span></span> <span data-ttu-id="37a7f-120">Перейдите в адресную строку и перейдите к*edge://favorites*, нажмите на многоточие "**…**" и выберите **Экспорт конфигурации избранного**.</span><span class="sxs-lookup"><span data-stu-id="37a7f-120">Go to the address bar and navigate to *edge://favorites*, click the ellipsis "**…**" and choose **Export favorites configuration**.</span></span> <span data-ttu-id="37a7f-121">На следующем снимке экрана показаны параметры, которые можно использовать при подготовке избранного.</span><span class="sxs-lookup"><span data-stu-id="37a7f-121">The next screenshot shows the options you have when provisioning favorites.</span></span>

   ![Параметры меню для работы с избранным.](media/edge-learnmore-provision-favorites/provision-favorites-menu-options.png)

5. <span data-ttu-id="37a7f-123">В разделе **Экспорт конфигурации избранного** введите имя папки, которое будут видеть пользователи.</span><span class="sxs-lookup"><span data-stu-id="37a7f-123">Under **Export your favorites configuration** you provide a name for the folder that your users will see.</span></span> <span data-ttu-id="37a7f-124">Введите имя папки и выберите формат Платформы, которую хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="37a7f-124">Type the Folder name and pick the Platform format you want to use.</span></span> <span data-ttu-id="37a7f-125">Щелкните **Копировать в буфер обмена**.</span><span class="sxs-lookup"><span data-stu-id="37a7f-125">Click **Copy to clipboard**.</span></span> <span data-ttu-id="37a7f-126">На следующем снимке экрана показано «Управляемое избранное» для имени папки и платформы Windows.</span><span class="sxs-lookup"><span data-stu-id="37a7f-126">The next screenshot shows "Managed favorites" for the folder name and the platform is Windows.</span></span>

   ![Диалоговое окно экспорта избранного в папку Windows.](media/edge-learnmore-provision-favorites/provision-favorites-export.png)

6. <span data-ttu-id="37a7f-128">Откройте редактор управления групповой политикой, перейдите в раздел *Конфигурация компьютера/Административные шаблоны/* и выберите **Конфигурация избранного**.</span><span class="sxs-lookup"><span data-stu-id="37a7f-128">Open the Group Policy Editor, navigate to *Computer Configuration/Administrative Templates/* and pick **Configure Favorites**.</span></span> <span data-ttu-id="37a7f-129">Включение политики «Настроить избранное».</span><span class="sxs-lookup"><span data-stu-id="37a7f-129">Enable the "Configure Favorites" policy.</span></span> <span data-ttu-id="37a7f-130">В разделе **Параметры:** вставьте экспортированное содержимое в текстовую область «Настроить избранное», а затем щелкните **Применить**.</span><span class="sxs-lookup"><span data-stu-id="37a7f-130">Under **Options:**, paste the exported contents in the Configure favorites text area then click **Apply**.</span></span> <span data-ttu-id="37a7f-131">На следующем снимке экрана показан пример папки «Управляемое избранное» из шага 5.</span><span class="sxs-lookup"><span data-stu-id="37a7f-131">The next screenshot shows an example of the "Managed favorites" folder from step 5.</span></span>

   ![Используйте gpedit для включения и настройки политики «Настроить избранное».](media/edge-learnmore-provision-favorites/provision-favorites-gpedit.png)

7. <span data-ttu-id="37a7f-133">Нажмите кнопку **OK** или **Применить** для сохранения настроек политики.</span><span class="sxs-lookup"><span data-stu-id="37a7f-133">Click **OK** or **Apply** to safe the policy settings.</span></span>

## <span data-ttu-id="37a7f-134">См. также</span><span class="sxs-lookup"><span data-stu-id="37a7f-134">See also</span></span>

- [<span data-ttu-id="37a7f-135">Использование целевой страницы Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="37a7f-135">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)