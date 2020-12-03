---
title: Автоматизация развертывания Microsoft Edge в среде macOS с помощью Jamf
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 11/30/2019
audience: ITPro
ms.topic: technical
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Инструкции по автоматизации развертывания Microsoft Edge в среде macOS с помощью Jamf.
ms.openlocfilehash: 8639c0b7bf78bb8e22370dba29b592af73d8cb40
ms.sourcegitcommit: ed6a5afabf909df87bec48671c4c47bcdfaeb7bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/02/2020
ms.locfileid: "11194727"
---
# <span data-ttu-id="cdeb7-103">Развертывание в macOS с помощью Jamf</span><span class="sxs-lookup"><span data-stu-id="cdeb7-103">Deploy to macOS with Jamf</span></span>

<span data-ttu-id="cdeb7-104">В этой статье описано, как выполнить развертывание Microsoft Edge в среде macOS с помощью Jamf.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-104">This article describes how to deploy Microsoft Edge for macOS using Jamf.</span></span>

> [!NOTE]
> <span data-ttu-id="cdeb7-105">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="cdeb7-106">Что вам понадобится</span><span class="sxs-lookup"><span data-stu-id="cdeb7-106">Prerequisites</span></span>

<span data-ttu-id="cdeb7-107">Перед развертыванием Microsoft Edge убедитесь, что выполнены следующие необходимые условия.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-107">Before you deploy Microsoft Edge, make sure you meet the following prerequisites:</span></span>

- <span data-ttu-id="cdeb7-108">Файл установки Microsoft Edge — **MicrosoftEdgeDev-\<version\>.pkg** находится в доступном сетевом расположении.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-108">The Microsoft Edge installation file,  **MicrosoftEdgeDev-\<version\>.pkg** is in an accessible location on your network.</span></span> <span data-ttu-id="cdeb7-109">Вы можете скачать файлы установки Microsoft Edge Enterprise с [целевой страницы Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="cdeb7-109">You can download the Microsoft Edge Enterprise installation files from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>
- <span data-ttu-id="cdeb7-110">У вас есть учетная запись Jamf Cloud с уровнем доступа и правами, необходимыми для создания и развертывания установочных файлов на компьютерах.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-110">You have a Jamf Cloud account with the level of access and privileges needed to create and deploy installation files to computers.</span></span>

## <span data-ttu-id="cdeb7-111">Чтобы развернуть Microsoft Edge с помощью Jamf, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-111">To deploy Microsoft Edge using Jamf:</span></span>

1. <span data-ttu-id="cdeb7-112">Войдите в Jamf и перейдите в раздел **Все параметры**.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-112">Sign on to Jamf and go to **All Settings**.</span></span>

    ![Откройте "Все параметры"](./media/mac-deploy/jamf-dash-main-open-settings.png)

2. <span data-ttu-id="cdeb7-114">В разделе **Все параметры** выберите **Управление компьютерами**.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-114">Under **All Settings**, click **Computer Management**.</span></span>

    ![Выберите "Управление компьютерами"](./media/mac-deploy/jamf-all-settings-computer-mgmt.png)

3. <span data-ttu-id="cdeb7-116">В разделе **Управление компьютерами** выберите **Пакеты**.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-116">Under **Computer Management**, click **Packages**.</span></span>

    ![Выберите "Пакеты"](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkgs.png)

4. <span data-ttu-id="cdeb7-118">На странице **Пакеты** нажмите кнопку **+ Создать**, чтобы добавить новый пакет.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-118">On the **Packages** page, click **+ New** to add a new package.</span></span>

    ![Выберите "Создать", чтобы добавить новый пакет](./media/mac-deploy/jamf-all-settings-computer-mgmt-new-pkg.png)

5. <span data-ttu-id="cdeb7-120">На странице **Новый пакет** введите сведения о пакете и нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-120">On the **New Package** page, enter the details about the package and then click **Save**.</span></span> <span data-ttu-id="cdeb7-121">(Например, ОТОБРАЖАЕМОЕ ИМЯ, СВЕДЕНИЯ или ЗАМЕТКИ.)</span><span class="sxs-lookup"><span data-stu-id="cdeb7-121">(For example, DISPLAY NAME, INFO, or NOTES.)</span></span>

    ![Выберите "Сохранить", чтобы сохранить сведения о пакете](./media/mac-deploy/jamf-all-settings-computer-mgmt-save-pkg-info.png)

6. <span data-ttu-id="cdeb7-123">Выберите **Компьютеры** в строке меню, а затем — **Политики** на панели навигации.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-123">Select **Computers** on the menu bar, and then select **Policies** in the navigation bar.</span></span>

7. <span data-ttu-id="cdeb7-124">Нажмите кнопку **+ Создать**, чтобы открыть панель **Новая политика**.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-124">Select **+ New** to display the **New Policy** pane.</span></span>

    ![Выберите "Создать", чтобы создать новую политику](./media/mac-deploy/jamf-all-settings-computer-new-policy.png)

8. <span data-ttu-id="cdeb7-126">На вкладке **Параметры** выберите **Общие**.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-126">On the **Options** tab, select **General**.</span></span>

    - <span data-ttu-id="cdeb7-127">В разделе **ОТОБРАЖАЕМОЕ ИМЯ** введите отображаемое имя политики.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-127">Under **DISPLAY NAME**, enter the display name for the policy.</span></span>
    - <span data-ttu-id="cdeb7-128">В разделе **Триггер** выберите событие, которое будет запускать политику.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-128">Under **Trigger**, select the event that will trigger the policy.</span></span> <span data-ttu-id="cdeb7-129">(В следующем примере таким событием является "Запуск".)</span><span class="sxs-lookup"><span data-stu-id="cdeb7-129">(In the following example, the event is Startup.)</span></span>

    ![Введите сведения о развертывании](./media/mac-deploy/jamf-all-settings-computer-cfg-policy.png)

9. <span data-ttu-id="cdeb7-131">На вкладке **Параметры** выберите **Пакеты**.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-131">On the **Options** tab, click **Packages**.</span></span>

10. <span data-ttu-id="cdeb7-132">Во всплывающем окне **Настройка пакетов** выберите **Настроить**.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-132">On the **Configure Packages** popup, click **Configure**.</span></span>

    ![Настройка пакета](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-configure.png)

11. <span data-ttu-id="cdeb7-134">Добавленный пакет отобразится на панели **Пакеты**.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-134">The package that you added shows on the **Packages** pane.</span></span> <span data-ttu-id="cdeb7-135">Щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-135">Click **Add**.</span></span> <span data-ttu-id="cdeb7-136">В этом примере пакет "MicrosoftEdgeBeta" представлен на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-136">For this example, the package is "MicrosoftEdgeBeta" in the following screenshot.</span></span>

    ![Добавление пакета](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-add-beta.png)

12. <span data-ttu-id="cdeb7-138">На странице **Новая политика** используйте раскрывающиеся списки для выбора **ТОЧКИ РАСПРОСТРАНЕНИЯ** и **ДЕЙСТВИЯ**, которые будет использовать и выполнять политика.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-138">On the **New Policy** page, uUse the drop-down lists to select the **DISTRIBUTION POINT** and **ACTION** to take for the policy.</span></span> <span data-ttu-id="cdeb7-139">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-139">Click **Save**.</span></span> <span data-ttu-id="cdeb7-140">На следующем снимке экрана в качестве примера представлены "Each computer's default distribution point" (Точка распространения по умолчанию каждого компьютера) и "Install" (Установить).</span><span class="sxs-lookup"><span data-stu-id="cdeb7-140">The following screenshot uses "Each computer's default distribution point" and "Install" as an example.</span></span>

    ![Выбор точки распространения и действия](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkg-cfg-distro.png)

13. <span data-ttu-id="cdeb7-142">На странице **Новая политика** перейдите на вкладку **Область**. Областью развертывания можно управлять на основе компьютеров или пользователей.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-142">On the **New Policy** page, select the **Scope** tab. You can manage the scope of the deployment based on computers or users.</span></span> <span data-ttu-id="cdeb7-143">В этом примере выберите **Все компьютеры** в раскрывающемся списке **КОНЕЧНЫЕ КОМПЬЮТЕРЫ**, а затем нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-143">For this example, select **All Computers** from the **TARGET COMPUTERS** drop-down list and then click **Save**.</span></span>

    ![Выбор области развертывания](./media/mac-deploy/jamf-all-settings-computer-mgmt-add-target.png)

14. <span data-ttu-id="cdeb7-145">На этом этапе вы можете просмотреть политику развертывания Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-145">At this point you can review the Microsoft Edge deployment policy.</span></span> <span data-ttu-id="cdeb7-146">Если варианты развертывания соответствуют вашим требованиям, нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-146">If the deployment options meet your requirements, click **Done**.</span></span>

    ![Нажмите кнопку "Готово"](./media/mac-deploy/jamf-all-settings-computer-mgmt-finish-add-deployment.png)

    > [!NOTE]
    > <span data-ttu-id="cdeb7-148">Вы можете вернуться к политике развертывания в любое время, чтобы изменить параметры.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-148">You can return to a deployment policy at any time to change settings.</span></span>

<span data-ttu-id="cdeb7-149">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="cdeb7-149">Congratulations!</span></span> <span data-ttu-id="cdeb7-150">Вы только что завершили настройку развертывания Microsoft Edge для macOS с помощью Jamf.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-150">You’ve just finished configuring Jamf to deploy Microsoft Edge for macOS.</span></span> <span data-ttu-id="cdeb7-151">Когда заданным условием триггера станет значение "true", пакет будет развернут на указанных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="cdeb7-151">When the trigger condition you defined is true, the package will get deployed to the computers you specified.</span></span>

## <span data-ttu-id="cdeb7-152">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="cdeb7-152">See also</span></span>

- [<span data-ttu-id="cdeb7-153">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="cdeb7-153">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="cdeb7-154">Jamf.com</span><span class="sxs-lookup"><span data-stu-id="cdeb7-154">Jamf.com</span></span>](https://www.jamf.com/)
- [<span data-ttu-id="cdeb7-155">Интеграция Jamf с Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="cdeb7-155">Integrate Jamf with Microsoft Intune</span></span>](https://docs.microsoft.com/intune/conditional-access-integrate-jamf)
