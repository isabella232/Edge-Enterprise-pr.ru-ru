---
title: Развертывание Microsoft Edge с помощью System Center Configuration Manager
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 09/30/2019
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Узнайте, как развернуть Microsoft Edge с помощью System Center Configuration Manager (SCCM).
ms.openlocfilehash: be14f2db3b28b7585bfad1706b9f82209235df0a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980877"
---
# <span data-ttu-id="9c975-103">Развертывание Microsoft Edge с помощью System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9c975-103">Deploy Microsoft Edge using System Center Configuration Manager</span></span>

<span data-ttu-id="9c975-104">В этой статье приведены инструкции по автоматизации развертывания Microsoft Edge с помощью System Center Configuration Manager (SCCM).</span><span class="sxs-lookup"><span data-stu-id="9c975-104">This article shows you how to automate a Microsoft Edge deployment by using System Center Configuration Manager (SCCM).</span></span>

>[!NOTE]
><span data-ttu-id="9c975-105">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="9c975-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="9c975-106">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="9c975-106">Before you begin</span></span>

<span data-ttu-id="9c975-107">Ознакомьтесь со сведениями в разделе [Введение в управление приложениями с помощью диспетчера конфигураций](https://docs.microsoft.com/sccm/apps/understand/introduction-to-application-management).</span><span class="sxs-lookup"><span data-stu-id="9c975-107">Review the information in [Introduction to application management in Configuration Manager](https://docs.microsoft.com/sccm/apps/understand/introduction-to-application-management).</span></span> <span data-ttu-id="9c975-108">В этой статье, посвященной управлению приложениями, вы ознакомитесь с необходимой терминологией, а также узнаете о том, как подготовить свой сайт к установке приложений.</span><span class="sxs-lookup"><span data-stu-id="9c975-108">This application management article will help you understand the terminology used in this article and is a guide to preparing your site to install applications.</span></span>

<span data-ttu-id="9c975-109">Скачайте файлы установки Microsoft Edge Enterprise (**MicrosoftEdgeDevEnterpriseX64.msi** и/или **MicrosoftEdgeDevEnterpriseX86.msi**) на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).</span><span class="sxs-lookup"><span data-stu-id="9c975-109">Download the Microsoft Edge Enterprise installation files (**MicrosoftEdgeDevEnterpriseX64.msi** and/or **MicrosoftEdgeDevEnterpriseX86.msi**) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="9c975-110">Убедитесь, что файлы установки Microsoft Edge хранятся в доступном сетевом расположении.</span><span class="sxs-lookup"><span data-stu-id="9c975-110">Make sure you store the Microsoft Edge installation files in an accessible network location.</span></span>

## <span data-ttu-id="9c975-111">Создание приложения</span><span class="sxs-lookup"><span data-stu-id="9c975-111">Create the application</span></span>

<span data-ttu-id="9c975-112">Вы создадите приложение, используя мастер диспетчера конфигураций.</span><span class="sxs-lookup"><span data-stu-id="9c975-112">You'll create the application using a Configuration Manager wizard.</span></span>

### <span data-ttu-id="9c975-113">Запуск мастера создания приложений и создание приложения</span><span class="sxs-lookup"><span data-stu-id="9c975-113">Start the Create Application Wizard and create the application</span></span>  

1. <span data-ttu-id="9c975-114">На консоли диспетчера конфигураций выберите **Библиотека программного обеспечения** > **Управление приложениями** > **Приложения**.</span><span class="sxs-lookup"><span data-stu-id="9c975-114">In the Configuration Manager console, click **Software Library** > **Application Management** > **Applications**.</span></span>  

2. <span data-ttu-id="9c975-115">На вкладке **Домашняя** в группе **Создать** щелкните **Создать приложение**.</span><span class="sxs-lookup"><span data-stu-id="9c975-115">On the **Home** tab, in the **Create** group, click **Create Application**.</span></span> <span data-ttu-id="9c975-116">Или щелкните правой кнопкой мыши **Приложения**на панели навигации, а затем выберите команду **Создать приложение**.</span><span class="sxs-lookup"><span data-stu-id="9c975-116">Or, right-click on **Applications** in the navigation bar and then click **Create Application**.</span></span>

    ![Создание приложения](./media/edge-ent-deployment-sccm/edge-ent-create-app-1.png)

3. <span data-ttu-id="9c975-118">На странице **Общие** **мастера создания приложений** установите флажок **Автоматически получать данные об этом приложении из файлов установки**.</span><span class="sxs-lookup"><span data-stu-id="9c975-118">On the **General** page of the **Create Application Wizard**, choose **Automatically detect information about this application from installation files**.</span></span> <span data-ttu-id="9c975-119">При этом некоторые области данных в мастере будут заполнены сведениями, извлеченными из файла установки MSI.</span><span class="sxs-lookup"><span data-stu-id="9c975-119">This pre-populates some of the information in the wizard with information that's extracted from the installation .msi file.</span></span> <span data-ttu-id="9c975-120">Укажите следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="9c975-120">Provide the following information:</span></span>  

   - <span data-ttu-id="9c975-121">**Тип**: выберите **Установщик Windows (файл \*.msi)**.</span><span class="sxs-lookup"><span data-stu-id="9c975-121">**Type**: Choose **Windows Installer (\*.msi file)**.</span></span>  

   - <span data-ttu-id="9c975-122">**Расположение**: укажите расположение (или нажмите кнопку **Обзор**, чтобы выбрать расположение) файла установки **MicrosoftEdgeDevEnterpriseX64.msi** или **MicrosoftEdgeDevEnterpriseX86.msi**.</span><span class="sxs-lookup"><span data-stu-id="9c975-122">**Location**: Type the location (or click **Browse** to select the location) of the installation file **MicrosoftEdgeDevEnterpriseX64.msi** or **MicrosoftEdgeDevEnterpriseX86.msi**.</span></span> <span data-ttu-id="9c975-123">Обратите внимание, что расположение должно быть указано в формате *\\\Server\Share\File*, чтобы диспетчер конфигураций мог найти файлы установки.</span><span class="sxs-lookup"><span data-stu-id="9c975-123">Note that the location must be specified in the form *\\\Server\Share\File* for Configuration Manager to locate the installation files.</span></span>  

   <span data-ttu-id="9c975-124">Страница **Укажите параметры для этого приложения** будет выглядеть так, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="9c975-124">Your **Specify settings for this application** page will look like the following example:</span></span>  

    ![Задайте параметры для этого приложения](./media/edge-ent-deployment-sccm/edge-ent-create-app-2.png)

4. <span data-ttu-id="9c975-126">Нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9c975-126">Click **Next**.</span></span> <span data-ttu-id="9c975-127">В разделе **Сведения** на странице **Импортированные сведения** вы увидите информацию о приложении и всех связанных с ним файлах, которые были импортированы.</span><span class="sxs-lookup"><span data-stu-id="9c975-127">Under **Details** on the **Imported Information** page, you'll see information about the application and any associated files that were imported.</span></span> <span data-ttu-id="9c975-128">Нажмите **Далее**, чтобы продолжить работу с мастером установки.</span><span class="sxs-lookup"><span data-stu-id="9c975-128">Click **Next** to continue with the wizard.</span></span>  

    ![Просмотр импортированной информации](./media/edge-ent-deployment-sccm/edge-ent-create-app-3.png)

5. <span data-ttu-id="9c975-130">На странице **Общие сведения** можно добавить дополнительные сведения о приложении.</span><span class="sxs-lookup"><span data-stu-id="9c975-130">On the **General Information** page, you can add more information about the application.</span></span> <span data-ttu-id="9c975-131">Например, версию программного обеспечения, комментарии администратора и издателя.</span><span class="sxs-lookup"><span data-stu-id="9c975-131">For example, Software version, Administrator comments, and Publisher.</span></span> <span data-ttu-id="9c975-132">Эти сведения можно использовать для сортировки и поиска приложения на консоли диспетчера конфигураций.</span><span class="sxs-lookup"><span data-stu-id="9c975-132">You can use this information to to help you sort and find the application in the Configuration Manager console.</span></span>

   <span data-ttu-id="9c975-133">Вы также можете использовать поле **Программа установки**, чтобы указать полную командную строку, которая будет использоваться для установки приложения на компьютерах.</span><span class="sxs-lookup"><span data-stu-id="9c975-133">You can also use the **Installation program** field to specify the full command line that will be used to install the application on PCs.</span></span> <span data-ttu-id="9c975-134">Это можно изменить, добавив собственные свойства (например, **/q** для автоматической установки).</span><span class="sxs-lookup"><span data-stu-id="9c975-134">You can edit this to add your own properties (for example, **/q** for an unattended installation).</span></span>

   <span data-ttu-id="9c975-135">На следующем снимке экрана показан пример, в котором используются поля **Укажите сведения об этом приложении**.</span><span class="sxs-lookup"><span data-stu-id="9c975-135">The following screenshot shows an example where the **Specify information about this application** fields are used.</span></span>

   ![Указание метаданных приложения](./media/edge-ent-deployment-sccm/edge-ent-create-app-5.png)

6. <span data-ttu-id="9c975-137">Нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9c975-137">Click **Next**.</span></span>
7. <span data-ttu-id="9c975-138">На странице **Сводка** можно подтвердить параметры приложения в разделе **Сведения**, а затем завершить работу с мастером.</span><span class="sxs-lookup"><span data-stu-id="9c975-138">On the **Summary** page, you can confirm your application settings under **Details** and then finish using the wizard.</span></span> <span data-ttu-id="9c975-139">Нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9c975-139">Click **Next**.</span></span>  

    ![Сведения о параметрах приложения](./media/edge-ent-deployment-sccm/edge-ent-create-app-6.png)

8. <span data-ttu-id="9c975-141">На странице **Завершение** щелкните **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="9c975-141">On the **Completion** page, click **Close**.</span></span>

    ![Диалоговое окно с сообщением об успешном завершении](./media/edge-ent-deployment-sccm/edge-ent-create-app-7.png)

<span data-ttu-id="9c975-143">Вы завершили создание приложения.</span><span class="sxs-lookup"><span data-stu-id="9c975-143">You've finished creating the application.</span></span> <span data-ttu-id="9c975-144">Чтобы просмотреть его в диспетчере конфигураций, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9c975-144">Use the following steps to see it in Configuration Manager:</span></span>

- <span data-ttu-id="9c975-145">Выберите рабочую область **Библиотека программного обеспечения**</span><span class="sxs-lookup"><span data-stu-id="9c975-145">select the **Software Library** workspace</span></span>
- <span data-ttu-id="9c975-146">Разверните пункт **Управление приложениями**</span><span class="sxs-lookup"><span data-stu-id="9c975-146">expand **Application Management**</span></span>
- <span data-ttu-id="9c975-147">Выберите **Приложения**.</span><span class="sxs-lookup"><span data-stu-id="9c975-147">click **Applications**.</span></span>

<span data-ttu-id="9c975-148">На следующем снимке экрана показан пример, используемый в этой статье.</span><span class="sxs-lookup"><span data-stu-id="9c975-148">The following screenshot shows the example used for this article.</span></span>  

![Приложения](./media/edge-ent-deployment-sccm/edge-ent-create-app-8.png)

## <span data-ttu-id="9c975-150">Изменение свойств приложения и параметров развертывания</span><span class="sxs-lookup"><span data-stu-id="9c975-150">Change application properties and deployment settings</span></span>

<span data-ttu-id="9c975-151">После создания приложения вы можете уточнить параметры приложения, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="9c975-151">After you create an application, you can refine the application settings if you need to.</span></span> <span data-ttu-id="9c975-152">Чтобы просмотреть свойства приложения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9c975-152">To look at the application properties:</span></span>

- <span data-ttu-id="9c975-153">Выберите приложение.</span><span class="sxs-lookup"><span data-stu-id="9c975-153">select the application</span></span>
- <span data-ttu-id="9c975-154">В разделе **Главная**>**Свойства** выберите **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="9c975-154">in **Home**>**Properties**, click **Properties**.</span></span>  

   ![Настройка свойств приложения](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-1.png)

 <span data-ttu-id="9c975-156">В диалоговом окне **Свойства приложения <application name\>** вы увидите представление элементов с вкладками, которые можно настроить для изменения режима работы приложения.</span><span class="sxs-lookup"><span data-stu-id="9c975-156">In the **<application name\> Application Properties** dialog page, you'll see a tabbed view of the items that you can configure to change the behavior of the application.</span></span> <span data-ttu-id="9c975-157">Дополнительные сведения о параметрах, которые можно настроить, см. в разделе [Создание приложений](https://docs.microsoft.com/sccm/apps/deploy-use/create-applications).</span><span class="sxs-lookup"><span data-stu-id="9c975-157">For more information about the settings you can configure, see [Create applications](https://docs.microsoft.com/sccm/apps/deploy-use/create-applications).</span></span>

<span data-ttu-id="9c975-158">В этом примере вы измените некоторые свойства типа развертывания приложения.</span><span class="sxs-lookup"><span data-stu-id="9c975-158">For this example, you'll change some properties of the application's deployment type.</span></span> <span data-ttu-id="9c975-159">Изменение свойств развертывания:</span><span class="sxs-lookup"><span data-stu-id="9c975-159">To change the deployment properties:</span></span>

1. <span data-ttu-id="9c975-160">Перейдите на вкладку **Типы развертывания**.</span><span class="sxs-lookup"><span data-stu-id="9c975-160">Click the **Deployment Types** tab.</span></span>
2. <span data-ttu-id="9c975-161">В разделе **Типы развертывания:** выберите **Имя** приложения.</span><span class="sxs-lookup"><span data-stu-id="9c975-161">Under **Deployment types:**, select the application **Name**</span></span>
3. <span data-ttu-id="9c975-162">Нажмите кнопку **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="9c975-162">Click **Edit**.</span></span>

   ![Изменение типа развертывания](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-2.png)

### <span data-ttu-id="9c975-164">Добавление требования к типу развертывания</span><span class="sxs-lookup"><span data-stu-id="9c975-164">Add a requirement to the deployment type</span></span>

 <span data-ttu-id="9c975-165">Требования обозначают условия, которые должны быть соблюдены перед установкой приложения на устройстве.</span><span class="sxs-lookup"><span data-stu-id="9c975-165">Requirements specify conditions that must be met before an application is installed on a device.</span></span> <span data-ttu-id="9c975-166">Вы можете выбрать уже готовые требования или создать собственные.</span><span class="sxs-lookup"><span data-stu-id="9c975-166">You can choose from built-in requirements or you can create your own.</span></span> <span data-ttu-id="9c975-167">Например, вы можете добавить требование, согласно которому приложение будет установлено только на компьютерах, работающих под управлением Windows 10 **x86** или **x64**, в зависимости от архитектуры целевого процессора файла установки.</span><span class="sxs-lookup"><span data-stu-id="9c975-167">For example, you can add a requirement that the application will only be installed on PCs that are running Windows 10 **x86** or **x64**, depending on the installation file's target processor architecture.</span></span> <span data-ttu-id="9c975-168">В этом примере укажите Windows 10 **x86**.</span><span class="sxs-lookup"><span data-stu-id="9c975-168">In this example, you'll specify Windows 10 **x86**.</span></span>

1. <span data-ttu-id="9c975-169">На странице свойства типа развертывания, которую вы только что открыли, перейдите на вкладку **Требования**.</span><span class="sxs-lookup"><span data-stu-id="9c975-169">From the deployment type properties page you just opened, click the **Requirements** tab.</span></span>

2. <span data-ttu-id="9c975-170">Нажмите кнопку **Добавить**, чтобы открыть диалоговое окно **Создать требование**.</span><span class="sxs-lookup"><span data-stu-id="9c975-170">Click **Add** to open the **Create Requirement** dialog.</span></span>

    ![Создание требования](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-3.png)

3. <span data-ttu-id="9c975-172">В диалоговом окне **Создать требование** укажите следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="9c975-172">In the **Create Requirement** dialog box, specify the following information:</span></span>

    - <span data-ttu-id="9c975-173">**Категория**: **устройство**</span><span class="sxs-lookup"><span data-stu-id="9c975-173">**Category**: **Device**</span></span>  

    - <span data-ttu-id="9c975-174">**Условие**: **операционная система**</span><span class="sxs-lookup"><span data-stu-id="9c975-174">**Condition**: **Operating system**</span></span>  

    - <span data-ttu-id="9c975-175">**Тип правила**: **значение**</span><span class="sxs-lookup"><span data-stu-id="9c975-175">**Rule type**: **Value**</span></span>  

    - <span data-ttu-id="9c975-176">**Оператор**: **один из**</span><span class="sxs-lookup"><span data-stu-id="9c975-176">**Operator**: **One of**</span></span>  

    - <span data-ttu-id="9c975-177">В списке операционных систем выберите **Windows 10** > **Все Windows 10 (32-разрядные)**.</span><span class="sxs-lookup"><span data-stu-id="9c975-177">From the operating systems list, select **Windows 10** > **All Windows 10 (32-bit)**.</span></span>  

    <span data-ttu-id="9c975-178">Когда все будет готово, диалоговое окно будет выглядеть так, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="9c975-178">When you're finished, the dialog will look like the following screenshot example:</span></span>

    ![Добавление требования](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-4.png)

4. <span data-ttu-id="9c975-180">Нажмите кнопку **ОК**, чтобы закрыть все открытые страницы свойств и вернуться к списку **Приложения** на консоли диспетчера конфигураций.</span><span class="sxs-lookup"><span data-stu-id="9c975-180">Click **OK** to close each open property page and return to the **Applications** list in the Configuration Manager console.</span></span>  

## <span data-ttu-id="9c975-181">Добавление содержимого приложения в точку распространения</span><span class="sxs-lookup"><span data-stu-id="9c975-181">Add the application content to a distribution point</span></span>  

<span data-ttu-id="9c975-182">Чтобы развернуть обновленное приложение на компьютерах, убедитесь, что содержимое приложения скопировано в точку распространения.</span><span class="sxs-lookup"><span data-stu-id="9c975-182">To deploy the updated application to PCs, make sure that the application content is copied to a distribution point.</span></span> <span data-ttu-id="9c975-183">Компьютеры обращаются к точке распространения для установки приложения.</span><span class="sxs-lookup"><span data-stu-id="9c975-183">PCs access the distribution point to install the application.</span></span>  

>[!TIP]
><span data-ttu-id="9c975-184">Дополнительные сведения о точках распространения и управлении содержимым в диспетчере конфигураций см. в разделе [Развертывание и администрирование содержимого для System Center Configuration Manager](https://docs.microsoft.com/sccm/core/servers/deploy/configure/deploy-and-manage-content).</span><span class="sxs-lookup"><span data-stu-id="9c975-184">To find out more about distribution points and content management in Configuration Manager, see [Deploy and manage content for System Center Configuration Manager](https://docs.microsoft.com/sccm/core/servers/deploy/configure/deploy-and-manage-content).</span></span>  

1. <span data-ttu-id="9c975-185">В консоли диспетчера конфигураций щелкните **Библиотека программного обеспечения**.</span><span class="sxs-lookup"><span data-stu-id="9c975-185">In the Configuration Manager console, click **Software Library**.</span></span>  

2. <span data-ttu-id="9c975-186">В рабочей области **Библиотека программного обеспечения** разверните пункт **Приложения**.</span><span class="sxs-lookup"><span data-stu-id="9c975-186">In the **Software Library** workspace, expand **Applications**.</span></span> <span data-ttu-id="9c975-187">В списке приложений выберите созданное вами приложение.</span><span class="sxs-lookup"><span data-stu-id="9c975-187">Select the application you created in the list of applications.</span></span>

3. <span data-ttu-id="9c975-188">На вкладке **Главная** в группе **Развертывание** выберите **Распространить содержимое**.</span><span class="sxs-lookup"><span data-stu-id="9c975-188">On the **Home** tab in the **Deployment** group, click **Distribute Content**.</span></span>  

4. <span data-ttu-id="9c975-189">На странице **Общие** **мастера распространения содержимого** проверьте правильность имени приложения и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9c975-189">On the **General** page of the **Distribute Content Wizard**, check that the application name is correct, and then click **Next**.</span></span>  

5. <span data-ttu-id="9c975-190">На странице **Содержимое** проверьте сведения, которые будут скопированы в точку распространения, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9c975-190">On the **Content** page, review the information that will be copied to the distribution point, and then click **Next**.</span></span>  

6. <span data-ttu-id="9c975-191">На странице **Места распространения содержимого** щелкните **Добавить**, чтобы выбрать одну или несколько коллекций, точки распространения или группы точек распространения, где будет установлено содержимое приложения.</span><span class="sxs-lookup"><span data-stu-id="9c975-191">On the **Content Destination** page, click **Add** to select one or more collections, distribution points, or distribution point groups on which to install the application content.</span></span>

7. <span data-ttu-id="9c975-192">Завершите работу мастера.</span><span class="sxs-lookup"><span data-stu-id="9c975-192">Complete the wizard.</span></span>

<span data-ttu-id="9c975-193">Вы можете проверить, было ли содержимое приложения успешно скопировано в точку распространения в рабочей области **Мониторинг** в разделе **Состояние распространения** > **Состояние содержимого**.</span><span class="sxs-lookup"><span data-stu-id="9c975-193">You can check that the application content was copied successfully to the distribution point from the **Monitoring** workspace, under **Distribution Status** > **Content Status**.</span></span>  

## <span data-ttu-id="9c975-194">Развертывание приложения</span><span class="sxs-lookup"><span data-stu-id="9c975-194">Deploy the application</span></span>  

<span data-ttu-id="9c975-195">Затем разверните приложение в коллекции устройств в иерархии.</span><span class="sxs-lookup"><span data-stu-id="9c975-195">Next, deploy the application to a device collection in your hierarchy.</span></span> <span data-ttu-id="9c975-196">В этом примере развертывание приложения выполняется в коллекции устройств **Все системы**.</span><span class="sxs-lookup"><span data-stu-id="9c975-196">In this example, you deploy the application to the **All Systems** device collection.</span></span>  

>[!TIP]
><span data-ttu-id="9c975-197">Помните, что приложение будет установлено только на компьютерах под управлением Windows 10 с указанной архитектурой процессора из-за требований, заданных ранее.</span><span class="sxs-lookup"><span data-stu-id="9c975-197">Remember that only Windows 10 computers of the specified processor architecture will install the application because of the requirements that you selected earlier.</span></span>  

1. <span data-ttu-id="9c975-198">В консоли диспетчера конфигураций выберите **Библиотека программного обеспечения** > **Управление приложениями** > **Приложения**.</span><span class="sxs-lookup"><span data-stu-id="9c975-198">In the Configuration Manager console, click **Software Library** > **Application Management** > **Applications**.</span></span>

2. <span data-ttu-id="9c975-199">В списке приложений выберите созданное вами ранее приложение.</span><span class="sxs-lookup"><span data-stu-id="9c975-199">From the list of applications, select the application that you created earlier.</span></span> <span data-ttu-id="9c975-200">Затем на вкладке **Главная** в группе **Развертывание** выберите **Развернуть** или щелкните правой кнопкой мыши и выберите **Развернуть**.</span><span class="sxs-lookup"><span data-stu-id="9c975-200">Then, on the **Home** tab in the **Deployment** group, click **Deploy**, or right-click the application and select **Deploy**.</span></span>

    ![Развертывание приложения](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-1.png)

3. <span data-ttu-id="9c975-202">На странице **Общие** **мастера развертывания программного обеспечения** нажмите кнопку **Обзор**, чтобы выбрать коллекцию устройств, в которой требуется развернуть приложение.</span><span class="sxs-lookup"><span data-stu-id="9c975-202">On the **General** page of the **Deploy Software Wizard**, click **Browse** to select the device collection to which you want to deploy the application.</span></span>

    ![Выполните поиск файла установки](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-2.png)

4. <span data-ttu-id="9c975-204">На странице **Содержимое** проверьте, что выбрана точка распространения, из которой компьютеры будут устанавливать приложение.</span><span class="sxs-lookup"><span data-stu-id="9c975-204">On the **Content** page, check that the distribution point from which you want PCs to install the application is selected.</span></span>

    ![Укажите точку распространения](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-6.png)

5. <span data-ttu-id="9c975-206">На странице **Параметры развертывания** убедитесь, что для параметра "Действие развертывания" задано значение **Установить**, а для параметра "Цель развертывания" — **Требуется**.</span><span class="sxs-lookup"><span data-stu-id="9c975-206">On the **Deployment Settings** page, make sure that the deployment action is set to **Install**, and the deployment purpose is set to **Required**.</span></span>

    ![Настройка параметров развертывания](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-8.png)

    >[!TIP]
    ><span data-ttu-id="9c975-208">Установив для параметра "Цель развертывания" значение **Требуется**, будет обеспечена установка приложения на компьютерах, соответствующих заданным вами требованиям.</span><span class="sxs-lookup"><span data-stu-id="9c975-208">By setting the deployment purpose to **Required**, you make sure that the application is installed on PCs that meet the requirements that you set.</span></span> <span data-ttu-id="9c975-209">Если задать для этого параметра значение **Доступно**, пользователи смогут установить приложение по запросу из центра программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="9c975-209">If you set this value to **Available**, then users can install the application on demand from Software Center.</span></span>  

6. <span data-ttu-id="9c975-210">На странице **Расписание** можно настроить время установки приложения.</span><span class="sxs-lookup"><span data-stu-id="9c975-210">On the **Scheduling** page, you can configure when the application will be installed.</span></span> <span data-ttu-id="9c975-211">В этом примере выберите **Как можно скорее после доступного времени**.</span><span class="sxs-lookup"><span data-stu-id="9c975-211">For this example, select **As soon as possible after the available time**.</span></span>

    ![Планирование развертывания](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-9.png)

7. <span data-ttu-id="9c975-213">На странице **Взаимодействие с пользователем** выберите необходимые значения и нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9c975-213">On the **User Experience** page, select your desired values and click **Next**.</span></span>

    ![Настройка взаимодействия с пользователем](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-10.png)

8. <span data-ttu-id="9c975-215">Задайте необходимые параметры оповещений и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9c975-215">Specify your desired alert options and click **Next**.</span></span>

    ![Настройка параметров оповещения](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-11.png)

9. <span data-ttu-id="9c975-217">Завершите работу мастера.</span><span class="sxs-lookup"><span data-stu-id="9c975-217">Complete the wizard.</span></span>

<span data-ttu-id="9c975-218">Используйте инструкции из раздела **Мониторинг приложения** далее, чтобы увидеть состояние развертывания приложения.</span><span class="sxs-lookup"><span data-stu-id="9c975-218">Use the information in the following **Monitor the application** section to see the status of your application deployment.</span></span>  

## <span data-ttu-id="9c975-219">Мониторинг приложения</span><span class="sxs-lookup"><span data-stu-id="9c975-219">Monitor the application</span></span>

 <span data-ttu-id="9c975-220">В этом разделе вы можете быстро просмотреть состояние развертывания только что развернутого приложения.</span><span class="sxs-lookup"><span data-stu-id="9c975-220">In this section, you'll take a quick look at the deployment status of the application that you just deployed.</span></span>  

### <span data-ttu-id="9c975-221">Чтобы просмотреть состояние развертывания:</span><span class="sxs-lookup"><span data-stu-id="9c975-221">To review the deployment status</span></span>  

1. <span data-ttu-id="9c975-222">В консоли диспетчера конфигураций выберите **Мониторинг** > **Развертывания**.</span><span class="sxs-lookup"><span data-stu-id="9c975-222">In the Configuration Manager console, click **Monitoring** > **Deployments**.</span></span>  

2. <span data-ttu-id="9c975-223">В списке развертываний выберите приложение.</span><span class="sxs-lookup"><span data-stu-id="9c975-223">From the list of deployments, select the application.</span></span>

    ![Мониторинг развертывания](./media/edge-ent-deployment-sccm/edge-ent-monitor-deployment.png)

3. <span data-ttu-id="9c975-225">На вкладке **Главная** в группе **Развертывание** нажмите кнопку **Просмотр состояния**.</span><span class="sxs-lookup"><span data-stu-id="9c975-225">On the **Home** tab in the **Deployment** group, click **View Status**.</span></span>  

4. <span data-ttu-id="9c975-226">Перейдите на одну из следующих вкладок, чтобы просмотреть другие обновления состояния развертывания приложения.</span><span class="sxs-lookup"><span data-stu-id="9c975-226">Select one of the following tabs to see more status updates about the application deployment:</span></span>  

    - <span data-ttu-id="9c975-227">**Успешное завершение**: приложение успешно установлено на указанных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="9c975-227">**Success**: The application installed successfully on the indicated PCs.</span></span>  

    - <span data-ttu-id="9c975-228">**Выполняется**: приложение еще не установлено.</span><span class="sxs-lookup"><span data-stu-id="9c975-228">**In Progress**: The application has not yet finished installing.</span></span>  

    - <span data-ttu-id="9c975-229">**Ошибка**: при установке приложения на указанных компьютерах произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="9c975-229">**Error**: An error occurred installing the application on the indicated PCs.</span></span> <span data-ttu-id="9c975-230">Кроме того, отображается дополнительная информация об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9c975-230">Further information about the error is also displayed.</span></span>  

    - <span data-ttu-id="9c975-231">**Требования не выполнены**: на указанных устройствах не была выполнена попытка установки, так как они не соответствуют заданным вами требованиям (в этом примере: из-за того, что они не работают под управлением Windows 10.)</span><span class="sxs-lookup"><span data-stu-id="9c975-231">**Requirements Not Met**: No installation attempt was made on the indicated devices because they did not meet the requirements you configured (in this example, because they do not run on Windows 10.)</span></span>

    - <span data-ttu-id="9c975-232">**Неизвестно**: диспетчеру конфигураций не удалось сообщить о состоянии развертывания.</span><span class="sxs-lookup"><span data-stu-id="9c975-232">**Unknown**: Configuration Manager was unable to report the status of the deployment.</span></span> <span data-ttu-id="9c975-233">Проверьте позже.</span><span class="sxs-lookup"><span data-stu-id="9c975-233">Check back again later.</span></span>  

    >[!TIP]
    ><span data-ttu-id="9c975-234">Есть несколько способов мониторинга развертывания приложений.</span><span class="sxs-lookup"><span data-stu-id="9c975-234">There are several ways you can monitor application deployments.</span></span> <span data-ttu-id="9c975-235">Дополнительные сведения см. в разделе [Мониторинг приложений на консоли System Center Configuration Manager](https://docs.microsoft.com/sccm/apps/deploy-use/monitor-applications-from-the-console).</span><span class="sxs-lookup"><span data-stu-id="9c975-235">For more information, see [Monitor applications from the System Center Configuration Manager console](https://docs.microsoft.com/sccm/apps/deploy-use/monitor-applications-from-the-console).</span></span>  

## <span data-ttu-id="9c975-236">Взаимодействие с конечным пользователем</span><span class="sxs-lookup"><span data-stu-id="9c975-236">End-user experience</span></span>  

<span data-ttu-id="9c975-237">Пользователи, которые используют компьютеры, управляемые диспетчером конфигураций и работающие под управлением Windows 10 с указанной архитектурой процессора, увидят сообщение о том, что им необходимо установить приложение для разработки Microsoft Edge Dev.</span><span class="sxs-lookup"><span data-stu-id="9c975-237">Users who have PCs that are managed by Configuration Manager and are running Windows 10 of the specified processor architecture, will see a message telling them that they must install the Microsoft Edge Dev application.</span></span> <span data-ttu-id="9c975-238">При использовании этого варианта установки приложение будет установлено.</span><span class="sxs-lookup"><span data-stu-id="9c975-238">When they accept this installation option, the application is installed.</span></span>  

## <span data-ttu-id="9c975-239">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="9c975-239">See also</span></span>

- [<span data-ttu-id="9c975-240">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="9c975-240">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="9c975-241">Создание и развертывание приложения с помощью System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9c975-241">Create and deploy an application with System Center Configuration Manager</span></span>](https://docs.microsoft.com/sccm/apps/get-started/create-and-deploy-an-application)
