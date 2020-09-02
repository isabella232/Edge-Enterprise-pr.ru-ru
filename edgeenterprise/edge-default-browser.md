---
title: Установка Microsoft Edge браузером по умолчанию в Windows и macOS
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 1/15/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Узнайте, как задать Microsoft Edge в качестве браузера по умолчанию
ms.openlocfilehash: c8cc45e0fe42dcbbd828dd81ae568f141cda2985
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980862"
---
# <span data-ttu-id="d3e72-103">Установка Microsoft Edge в качестве браузера по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d3e72-103">Set Microsoft Edge as the default browser</span></span>

<span data-ttu-id="d3e72-104">В этой статье описывается, как можно задать Microsoft Edge браузером по умолчанию в Windows и macOS.</span><span class="sxs-lookup"><span data-stu-id="d3e72-104">This article explains how you can set Microsoft Edge as the default browser on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="d3e72-105">Эта статья относится к Microsoft Edge версии 77 или более поздней в среде Windows 8 и Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d3e72-105">This article applies to Microsoft Edge version 77 or later on Windows 8 and Windows 10.</span></span> <span data-ttu-id="d3e72-106">Для Windows 7 и macOS см. раздел, посвященный политике [Установка Microsoft Edge браузером по умолчанию](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled).</span><span class="sxs-lookup"><span data-stu-id="d3e72-106">For Windows 7 and macOS, see the [Set Microsoft Edge as default browser](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled) policy.</span></span>

## <span data-ttu-id="d3e72-107">Введение</span><span class="sxs-lookup"><span data-stu-id="d3e72-107">Introduction</span></span>

<span data-ttu-id="d3e72-108">Вы можете использовать групповую политику **Задать файл конфигурации сопоставлений по умолчанию** или параметр системы управления мобильными устройствами [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration), чтобы сделать Microsoft Edge браузером по умолчанию в своей организации.</span><span class="sxs-lookup"><span data-stu-id="d3e72-108">You can use the **Set a default associations configuration file** Group Policy or the [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) Mobile Device Management setting to set Microsoft Edge as the default browser for your organization.</span></span>

<span data-ttu-id="d3e72-109">Чтобы задать Microsoft Edge Stable в качестве браузера по умолчанию для открытия HTML-файлов, ссылок http/https и файлов PDF, используйте следующий пример файла сопоставления приложений:</span><span class="sxs-lookup"><span data-stu-id="d3e72-109">To set Microsoft Edge Stable as the default browser for html files, http/https links, and PDF files use the following application association file example:</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations> 
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> <span data-ttu-id="d3e72-110">Чтобы настроить Microsoft Edge Beta в качестве браузера по умолчанию, задайте параметру **ApplicationName** значение "Microsoft Edge Beta", а параметру **ProgId** значение "MSEdgeBHTML".</span><span class="sxs-lookup"><span data-stu-id="d3e72-110">To set Microsoft Edge Beta as the default browser, set **ApplicationName** to "Microsoft Edge Beta" and **ProgId** to "MSEdgeBHTML".</span></span> <span data-ttu-id="d3e72-111">Чтобы настроить Microsoft Edge Dev в качестве браузера по умолчанию, задайте параметру **ApplicationName** значение "Microsoft Edge Dev", а параметру **ProgId** значение "MSEdgeDHTML".</span><span class="sxs-lookup"><span data-stu-id="d3e72-111">To set Microsoft Edge Dev as the default browser, set **ApplicationName** to "Microsoft Edge Dev" and **ProgId** to "MSEdgeDHTML".</span></span>


> [!NOTE]
> <span data-ttu-id="d3e72-112">Сопоставления файлов по умолчанию не применяются, если на целевом устройстве не установлен браузер Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d3e72-112">The default file associations aren't applied if Microsoft Edge isn't installed on the target device.</span></span> <span data-ttu-id="d3e72-113">В этом случае пользователям будет предложено выбрать приложение по умолчанию при открытии ссылки или файла HTM/HTML.</span><span class="sxs-lookup"><span data-stu-id="d3e72-113">In this scenario, users are prompted to select their default application when they open a link or a htm/html file.</span></span>

## <span data-ttu-id="d3e72-114">Установка Microsoft Edge в качестве браузера по умолчанию на устройствах, присоединенных к домену</span><span class="sxs-lookup"><span data-stu-id="d3e72-114">Set Microsoft Edge as the default browser on domain-joined devices</span></span>

<span data-ttu-id="d3e72-115">Вы можете задать Microsoft Edge в качестве браузера по умолчанию на устройствах, присоединенных к домену, настроив групповую политику **Задать файл конфигурации сопоставлений по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="d3e72-115">You can set Microsoft Edge as the default browser on domain-joined devices by configuring the **Set a default associations configuration file** group policy.</span></span> <span data-ttu-id="d3e72-116">При включении этой групповой политики также необходимо создать и сохранить файл конфигурации сопоставлений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d3e72-116">Turning this group policy on requires you to create and store a default associations configuration file.</span></span> <span data-ttu-id="d3e72-117">Этот файл хранится локально или в сетевой папке.</span><span class="sxs-lookup"><span data-stu-id="d3e72-117">This file is stored locally or on a network share.</span></span> <span data-ttu-id="d3e72-118">Подробнее о создании этого файла см. в разделе [Экспорт и импорт файлов сопоставлений приложений по умолчанию](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).</span><span class="sxs-lookup"><span data-stu-id="d3e72-118">For more information about creating this file, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).</span></span>

### <span data-ttu-id="d3e72-119">Чтобы настроить групповую политику для файла конфигурации сопоставлений по умолчанию и файла конфигурации сопоставлений протокола, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d3e72-119">To configure the group policy for a default file type and protocol associations configuration file:</span></span>

1. <span data-ttu-id="d3e72-120">В редакторе групповых политик перейдите к разделу **Computer Configuration\Administrative Templates\Windows Components\File Explorer**.</span><span class="sxs-lookup"><span data-stu-id="d3e72-120">Open the Group Policy editor and go to the **Computer Configuration\Administrative Templates\Windows Components\File Explorer**.</span></span>
2. <span data-ttu-id="d3e72-121">Выберите **Задать файл конфигурации сопоставлений по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="d3e72-121">Select **Set a default associations configuration file**.</span></span>
3. <span data-ttu-id="d3e72-122">Щелкните **параметр политики**, а затем выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="d3e72-122">Click **policy setting**, and then click **Enabled**.</span></span>
4. <span data-ttu-id="d3e72-123">В области **Параметры** введите расположение файла конфигурации сопоставлений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d3e72-123">Under **Options:**, type the location to your default associations configuration file.</span></span>
5. <span data-ttu-id="d3e72-124">Нажмите **ОК**, чтобы сохранить параметры политики.</span><span class="sxs-lookup"><span data-stu-id="d3e72-124">Click **OK** to save the policy settings.</span></span>

<span data-ttu-id="d3e72-125">В примере на следующем снимке экрана показан файл сопоставлений с именем *appassoc.xml* в сетевой папке, доступной с целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="d3e72-125">The example in the next screenshot shows an associations file named *appassoc.xml* on a network share that is accessible from the target device.</span></span>

   ![Включение сопоставления файлов в групповой политике](./media/edge-learnmore-make-edge-default-browser/edge-learnmore-app-associations.png)

   > [!NOTE]
   > <span data-ttu-id="d3e72-127">Если этот параметр включен и устройство пользователя подключено к домену, файл конфигурации сопоставлений обрабатывается при следующем входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="d3e72-127">If this setting is enabled and the user's device is domain-joined, the associations configuration file is processed the next time the user signs on.</span></span>

## <span data-ttu-id="d3e72-128">Установка Microsoft Edge в качестве браузера по умолчанию на устройствах, присоединенных к Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="d3e72-128">Set Microsoft Edge as the default browser on Azure Active Directory joined devices</span></span>

<span data-ttu-id="d3e72-129">Чтобы задать Microsoft Edge в качестве браузера по умолчанию на устройствах, подключенных к Azure Active Directory, выполните действия в разделе, посвященном параметру системы управления мобильными устройствами [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration), используя следующий пример файла сопоставления приложений.</span><span class="sxs-lookup"><span data-stu-id="d3e72-129">To set Microsoft Edge as the default browser on Azure Active Directory joined devices follow the steps in the [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) Mobile Device Management setting using the following application association file as an example.</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> <span data-ttu-id="d3e72-130">Чтобы настроить Microsoft Edge Beta в качестве браузера по умолчанию, задайте параметру **ApplicationName** значение "Microsoft Edge Beta", а параметру **ProgId** значение "MSEdgeBHTML".</span><span class="sxs-lookup"><span data-stu-id="d3e72-130">To set Microsoft Edge Beta as the default browser, set **ApplicationName** to "Microsoft Edge Beta" and **ProgId** to "MSEdgeBHTML".</span></span> <span data-ttu-id="d3e72-131">Чтобы настроить Microsoft Edge Dev в качестве браузера по умолчанию, задайте параметру **ApplicationName** значение "Microsoft Edge Dev", а параметру **ProgId** значение "MSEdgeDHTML".</span><span class="sxs-lookup"><span data-stu-id="d3e72-131">To set Microsoft Edge Dev as the default browser, set **ApplicationName** to "Microsoft Edge Dev" and **ProgId** to "MSEdgeDHTML".</span></span>

## <span data-ttu-id="d3e72-132">Установка Microsoft Edge браузером по умолчанию в macOS</span><span class="sxs-lookup"><span data-stu-id="d3e72-132">Set Microsoft Edge as the default browser on macOS</span></span>

<span data-ttu-id="d3e72-133">При попытке программно назначить браузер по умолчанию в macOS появляется запрос для пользователя.</span><span class="sxs-lookup"><span data-stu-id="d3e72-133">Attempting to programmatically set the default browser on macOS causes a prompt to appear for the end user.</span></span> <span data-ttu-id="d3e72-134">Этот запрос является функцией безопасности macOS, автоматический запуск которой можно отключить только с помощью AppleScript.</span><span class="sxs-lookup"><span data-stu-id="d3e72-134">This prompt is a macOS security feature that can only be automated away by using an AppleScript.</span></span>

<span data-ttu-id="d3e72-135">Из-за этого ограничения существует два основных метода установки Microsoft Edge в качестве браузера по умолчанию в macOS.</span><span class="sxs-lookup"><span data-stu-id="d3e72-135">Because of this limitation, there are two main methods for setting Microsoft Edge as the default browser on a macOS.</span></span> <span data-ttu-id="d3e72-136">Первый вариант: установить на устройство образ macOS, в котором Microsoft Edge уже задан как браузер по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d3e72-136">The first option is to flash the device with an image of macOS where Microsoft Edge has already been set as the default browser.</span></span> <span data-ttu-id="d3e72-137">Второй вариант: использование политики [Установить Microsoft Edge браузером по умолчанию](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled), которая предлагает пользователю назначить Microsoft Edge браузером по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d3e72-137">The other option is to use the [Set Microsoft Edge as default browser](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled) policy, which prompts the user to set Microsoft Edge as the default browser.</span></span>

<span data-ttu-id="d3e72-138">При использовании любого из этих методов пользователь может изменить браузер по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d3e72-138">When using either of these methods, it is still possible for a user to change the default browser.</span></span> <span data-ttu-id="d3e72-139">Это связано с тем, что по соображениям безопасности настройка браузера по умолчанию не может быть заблокирована программным способом.</span><span class="sxs-lookup"><span data-stu-id="d3e72-139">This is because for security reasons, the default browser preference can’t be blocked programmatically.</span></span> <span data-ttu-id="d3e72-140">По этой причине рекомендуется развертывать политику **Установить Microsoft Edge браузером по умолчанию**, даже если вы создаете образ с Microsoft Edge в качестве браузера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d3e72-140">For this reason, we recommend that you deploy the **Set Microsoft Edge as default browser** policy even if you create an image with Microsoft Edge as the default browser.</span></span> <span data-ttu-id="d3e72-141">Если эта политика настроена и пользователь изменяет браузер по умолчанию с Microsoft Edge, при следующем открытии Microsoft Edge пользователю будет предложено назначить его браузером по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d3e72-141">If the policy is set and a user changes the default browser from Microsoft Edge the next time they open Microsoft Edge, they will be prompted to set it as the default.</span></span>

## <span data-ttu-id="d3e72-142">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d3e72-142">See also</span></span>

- [<span data-ttu-id="d3e72-143">Планирование развертывания Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d3e72-143">Plan your deployment of Microsoft Edge</span></span>](https://docs.microsoft.com/DeployEdge/deploy-edge-plan-deployment)
- [<span data-ttu-id="d3e72-144">Использование целевой страницы Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="d3e72-144">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="d3e72-145">Установка Microsoft Edge в качестве браузера по умолчанию (Windows 7 и macOS)</span><span class="sxs-lookup"><span data-stu-id="d3e72-145">Set Microsoft Edge as default browser (Windows 7 and macOS)</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled)
- [<span data-ttu-id="d3e72-146">Windows 10: руководство по настройке сопоставления файлов для ИТ-специалистов</span><span class="sxs-lookup"><span data-stu-id="d3e72-146">Windows 10 – How to configure file associations for IT Pros?</span></span>](https://docs.microsoft.com/archive/blogs/windowsinternals/windows-10-how-to-configure-file-associations-for-it-pros)
- [<span data-ttu-id="d3e72-147">Экспорт и импорт сопоставлений приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d3e72-147">Export or Import Default Application Associations</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)
  - [<span data-ttu-id="d3e72-148">Обзор платформы DISM</span><span class="sxs-lookup"><span data-stu-id="d3e72-148">DISM Overview</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/what-is-dism)
  - [<span data-ttu-id="d3e72-149">Система обслуживания образов развертывания и управления ими (DISM)</span><span class="sxs-lookup"><span data-stu-id="d3e72-149">DISM - Deployment Image Servicing and Management</span></span>](https://docs.microsoft.com/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows)
