---
title: Настройка Microsoft Edge для macOS с помощью файла PLIST
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 11/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Настройка параметров политики Microsoft Edge в macOS с помощью файла PLIST
ms.openlocfilehash: 3f297c11d8009c85a1bc5e17447681ee2b9ef1e2
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447453"
---
# <a name="configure-microsoft-edge-policy-settings-for-macos-using-a-plist"></a><span data-ttu-id="ffd74-103">Настройка параметров политики Microsoft Edge для macOS с помощью файла PLIST</span><span class="sxs-lookup"><span data-stu-id="ffd74-103">Configure Microsoft Edge policy settings for macOS using a .plist</span></span>

<span data-ttu-id="ffd74-104">В этой статье описано, как настроить Microsoft Edge в macOS с помощью файла со списком свойств (.plist).</span><span class="sxs-lookup"><span data-stu-id="ffd74-104">This article describes how to configure Microsoft Edge on macOS using a property list (.plist) file.</span></span> <span data-ttu-id="ffd74-105">Вы узнаете, как создать этот файл и развернуть его в Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="ffd74-105">You'll learn how to create this file and then deploy it to Microsoft Intune.</span></span>

<span data-ttu-id="ffd74-106">Дополнительные сведения см. в разделе [Общие сведения о файлах со списком свойств](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (веб-сайт компании Apple) и [Пользовательские параметры полезных данных](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).</span><span class="sxs-lookup"><span data-stu-id="ffd74-106">For more information, see [About Information Property List Files](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (Apple's website) and [Custom payload settings](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).</span></span>

> [!NOTE]
> <span data-ttu-id="ffd74-107">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ffd74-107">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="configure-microsoft-edge-policies-on-macos"></a><span data-ttu-id="ffd74-108">Настройка политик Microsoft Edge в macOS</span><span class="sxs-lookup"><span data-stu-id="ffd74-108">Configure Microsoft Edge policies on macOS</span></span>

<span data-ttu-id="ffd74-109">Первый этап — это создание файла со списком свойств.</span><span class="sxs-lookup"><span data-stu-id="ffd74-109">The first step is to create your plist.</span></span> <span data-ttu-id="ffd74-110">Вы можете создать файл PLIST в любом текстовом редакторе или использовать [Терминал для создания профиля конфигурации](#create-a-configuration-profile-using-terminal).</span><span class="sxs-lookup"><span data-stu-id="ffd74-110">You can create the plist file with any text editor or you can use [Terminal to create the configuration profile](#create-a-configuration-profile-using-terminal).</span></span> <span data-ttu-id="ffd74-111">Однако проще создавать и редактировать файл PLIST с помощью средства форматирования XML-кода.</span><span class="sxs-lookup"><span data-stu-id="ffd74-111">However, it's easier to create and edit a plist file using a tool that formats the XML code for you.</span></span> <span data-ttu-id="ffd74-112">*Xcode* — это бесплатная интегрированная среда разработки, которую можно получить в одном из следующих мест.</span><span class="sxs-lookup"><span data-stu-id="ffd74-112">*Xcode* is a free integrated development environment that you can get from one of the following locations:</span></span>

- [<span data-ttu-id="ffd74-113">Веб-сайт для разработчиков Apple</span><span class="sxs-lookup"><span data-stu-id="ffd74-113">Apple developer website</span></span>](https://developer.apple.com/xcode/)
- [<span data-ttu-id="ffd74-114">Магазин App Store для Mac</span><span class="sxs-lookup"><span data-stu-id="ffd74-114">Mac App Store</span></span>](https://apps.apple.com/app/xcode/id497799835?mt=12)

<span data-ttu-id="ffd74-115">Список поддерживаемых политик и предпочтительные имена для их разделов см. в [Справочнике по политикам браузера Microsoft Edge](microsoft-edge-policies.md).</span><span class="sxs-lookup"><span data-stu-id="ffd74-115">For a list of supported policies and their preference key names, see [Microsoft Edge browser policies reference](microsoft-edge-policies.md).</span></span> <span data-ttu-id="ffd74-116">В файле шаблонов политик, который можно скачать на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise), есть образец файла пример PLIST (*itadminexample.plist*) в папке **Примеры**.</span><span class="sxs-lookup"><span data-stu-id="ffd74-116">In the policy templates file, which can be downloaded from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise), there's an example plist (*itadminexample.plist*) in the **examples** folder.</span></span> <span data-ttu-id="ffd74-117">Образец файла содержит все поддерживаемые типы данных, которые можно настроить для определения параметров политики.</span><span class="sxs-lookup"><span data-stu-id="ffd74-117">The example file contains all supported data types that you can customize to define your policy settings.</span></span> 

<span data-ttu-id="ffd74-118">Следующий шаг после создания содержимого файла PLIST — присвоить ему имя, используя предпочтительный домен Microsoft Edge, то есть *com.microsoft.Edge*.</span><span class="sxs-lookup"><span data-stu-id="ffd74-118">The next step after you create the contents of your plist, is to name it using the Microsoft Edge preference domain, *com.microsoft.Edge*.</span></span> <span data-ttu-id="ffd74-119">Имя чувствительно к регистру и не должно содержать настраиваемый канал, так как оно применяется ко всем каналам Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ffd74-119">The name is case sensitive and should not include the channel you are targeting because it applies to all Microsoft Edge channels.</span></span> <span data-ttu-id="ffd74-120">Именем файла PLIST должно быть **_com.microsoft.Edge.plist_**.</span><span class="sxs-lookup"><span data-stu-id="ffd74-120">The plist file name must be **_com.microsoft.Edge.plist_**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ffd74-121">Начиная со сборки 78.0.249.2 все каналы Microsoft Edge в macOS выполняют считывание из основного домена **com.microsoft.Edge**.</span><span class="sxs-lookup"><span data-stu-id="ffd74-121">Starting with build 78.0.249.2, all Microsoft Edge channels on macOS read from the **com.microsoft.Edge** preference domain.</span></span> <span data-ttu-id="ffd74-122">Все предыдущие выпуски выполняют считывание из домена, относящегося к каналу, например из домена **com.microsoft.Edge.Dev** для канала Dev.</span><span class="sxs-lookup"><span data-stu-id="ffd74-122">All prior releases read from a channel specific domain, such as **com.microsoft.Edge.Dev** for Dev channel.</span></span>

<span data-ttu-id="ffd74-123">Последним шагом является развертывание файла PLIST на устройствах Mac ваших пользователей с помощью предпочитаемого поставщика MDM, например Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="ffd74-123">The last step is to deploy your plist to your users' Mac devices using your preferred MDM provider, such as Microsoft Intune.</span></span> <span data-ttu-id="ffd74-124">Инструкции см. в разделе [Развертывание файла PLIST](#deploy-your-plist).</span><span class="sxs-lookup"><span data-stu-id="ffd74-124">For instructions see [Deploy your plist](#deploy-your-plist).</span></span>

### <a name="create-a-configuration-profile-using-terminal"></a><span data-ttu-id="ffd74-125">Создание профиля конфигурации с помощью терминала</span><span class="sxs-lookup"><span data-stu-id="ffd74-125">Create a configuration profile using Terminal</span></span>

1. <span data-ttu-id="ffd74-126">В терминале используйте следующую команду, чтобы создать файл PLIST для Microsoft Edge на компьютере с использованием предпочтительных параметров.</span><span class="sxs-lookup"><span data-stu-id="ffd74-126">In Terminal, use the following command to create a plist for Microsoft Edge on your desktop with your preferred settings:</span></span>

   ```cmd
   /usr/bin/defaults write ~/Desktop/com.microsoft.Edge.plist RestoreOnStartup -int 1
   ```

2. <span data-ttu-id="ffd74-127">Преобразуйте файл PLIST из двоичного формата в текстовый.</span><span class="sxs-lookup"><span data-stu-id="ffd74-127">Convert the plist from binary to plain text format:</span></span>

   ```cmd
   /usr/bin/plutil -convert xml1 ~/Desktop/com.microsoft.Edge.plist
   ```

<span data-ttu-id="ffd74-128">После преобразования файла проверьте правильность данных политики и наличие в них необходимых параметров для профиля конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ffd74-128">After converting the file verify that your policy data is correct and contains the settings you want for your configuration profile.</span></span>

> [!NOTE]
> <span data-ttu-id="ffd74-129">Файл plist или xml должен содержать только пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="ffd74-129">Only key value pairs should be in the contents of the plist or xml file.</span></span> <span data-ttu-id="ffd74-130">Перед отправкой файла в Intune удалите из него все значения \<plist> и \<dict>, а также заголовки xml.</span><span class="sxs-lookup"><span data-stu-id="ffd74-130">Prior to uploading your file into Intune remove all the \<plist> and \<dict> values, and xml headers from your file.</span></span> <span data-ttu-id="ffd74-131">Файл должен содержать только пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="ffd74-131">The file should only contain key value pairs.</span></span>

## <a name="deploy-your-plist"></a><span data-ttu-id="ffd74-132">Развертывание файла PLIST</span><span class="sxs-lookup"><span data-stu-id="ffd74-132">Deploy your plist</span></span>

<span data-ttu-id="ffd74-133">Для Microsoft Intune создайте новый профиль конфигурации устройства, предназначенный для платформы macOS, и выберите тип профиля *Файл основных параметров*.</span><span class="sxs-lookup"><span data-stu-id="ffd74-133">For Microsoft Intune create a new device configuration profile targeting the macOS platform and select the *Preference file* profile type.</span></span> <span data-ttu-id="ffd74-134">Выберите **com.microsoft.Edge** в качестве предпочтительного доменного имени и добавьте файл PLIST.</span><span class="sxs-lookup"><span data-stu-id="ffd74-134">Target **com.microsoft.Edge** as the preference domain name and upload your plist.</span></span> <span data-ttu-id="ffd74-135">Дополнительные сведения см. в разделе [Добавление файла со списком свойств на устройства macOS с помощью Microsoft Intune](/intune/configuration/preference-file-settings-macos).</span><span class="sxs-lookup"><span data-stu-id="ffd74-135">For more information see [Add a property list file to macOS devices using Microsoft Intune](/intune/configuration/preference-file-settings-macos).</span></span>

<span data-ttu-id="ffd74-136">Для Jamf добавьте файл PLIST как полезные данные *Настраиваемые параметры*.</span><span class="sxs-lookup"><span data-stu-id="ffd74-136">For Jamf upload the .plist file as a *Custom Settings* payload.</span></span>

## <a name="see-also"></a><span data-ttu-id="ffd74-137">См. также</span><span class="sxs-lookup"><span data-stu-id="ffd74-137">See also</span></span>

- [<span data-ttu-id="ffd74-138">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="ffd74-138">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="ffd74-139">Настройка для macOS с помощью Jamf</span><span class="sxs-lookup"><span data-stu-id="ffd74-139">Configure for macOS with Jamf</span></span>](configure-microsoft-edge-on-mac-jamf.md)
- [<span data-ttu-id="ffd74-140">Настройка для Windows</span><span class="sxs-lookup"><span data-stu-id="ffd74-140">Configure for Windows</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="ffd74-141">Настройка для Windows с помощью Intune</span><span class="sxs-lookup"><span data-stu-id="ffd74-141">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)