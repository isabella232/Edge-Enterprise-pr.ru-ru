---
title: Обзор системы безопасности Microsoft Edge
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 04/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Обзор развертывания системы безопасности Microsoft Edge
ms.openlocfilehash: f22f2dcbace00cd535d201950c2af488c708525b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980996"
---
# <span data-ttu-id="c5539-103">Обзор системы безопасности Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c5539-103">Overview of Microsoft Edge security</span></span>
  
<span data-ttu-id="c5539-104">ИТ-администраторы предприятия постоянно сталкиваются с множеством существующих и новых проблем безопасности, обеспечивая защиту корпоративной сети и устройств от вредоносных атак и одновременно предотвращая несанкционированный доступ к корпоративным данным и их утечки.</span><span class="sxs-lookup"><span data-stu-id="c5539-104">IT admins in the enterprise are constantly facing a myriad of existing and emerging security challenges while protecting the corporate network and devices from malicious attacks and preventing unauthorized access and leaks of corporate data.</span></span> <span data-ttu-id="c5539-105">Microsoft Edge предоставляет несколько встроенных уникальных возможностей, которые помогают решать эти проблемы.</span><span class="sxs-lookup"><span data-stu-id="c5539-105">Microsoft Edge provides several natively built, unique capabilities that help address these challenges.</span></span>

> [!NOTE]
> <span data-ttu-id="c5539-106">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="c5539-106">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="c5539-107">Условный доступ</span><span class="sxs-lookup"><span data-stu-id="c5539-107">Conditional Access</span></span>

<span data-ttu-id="c5539-108">Ключевыми аспектами обеспечения безопасности в облаке являются идентификация и предоставление доступа к управлению облачными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="c5539-108">A key aspect of cloud security is identity and access when it comes to managing your cloud resources.</span></span> <span data-ttu-id="c5539-109">В мире с преобладанием мобильных и облачных технологий пользователи могут получать доступ к ресурсам организации с помощью различных устройств и приложений из любого места.</span><span class="sxs-lookup"><span data-stu-id="c5539-109">In a mobile-first, cloud-first world, users can access your organization's resources using a variety of devices and apps from anywhere.</span></span> <span data-ttu-id="c5539-110">В результате этого недостаточно уделять внимание только тому, кто может получить доступ к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="c5539-110">As a result of this, just focusing on who can access a resource is not sufficient.</span></span> <span data-ttu-id="c5539-111">Также необходимо учитывать, каким образом осуществляется обращение к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="c5539-111">You also need to factor in how a resource is accessed.</span></span> <span data-ttu-id="c5539-112">Условный доступ в Azure Active Directory (Azure AD) помогает сохранять баланс между безопасностью и производительностью.</span><span class="sxs-lookup"><span data-stu-id="c5539-112">Azure Active Directory (Azure AD) Conditional Access helps you master the balance between security and productivity.</span></span>

### <span data-ttu-id="c5539-113">Доступ к ресурсам, защищенным с помощью функции условного доступа, в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c5539-113">Accessing Conditional Access protected resources in Microsoft Edge</span></span>

<span data-ttu-id="c5539-114">В Microsoft Edge реализована встроенная поддержка условного доступа Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c5539-114">Microsoft Edge natively supports Azure AD Conditional Access.</span></span> <span data-ttu-id="c5539-115">Устанавливать отдельное расширение не требуется.</span><span class="sxs-lookup"><span data-stu-id="c5539-115">There's no need to install a separate extension.</span></span> <span data-ttu-id="c5539-116">При входе в профиль Microsoft Edge с корпоративными учетными данными Azure AD браузер Microsoft Edge обеспечивает простой доступ к корпоративным облачным ресурсам, защищенным с помощью функции условного доступа.</span><span class="sxs-lookup"><span data-stu-id="c5539-116">When you're signed into a Microsoft Edge profile with enterprise Azure AD credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using Conditional Access.</span></span>

<span data-ttu-id="c5539-117">На совместимом устройстве идентификатор, обращающийся к ресурсу, должен соответствовать идентификатору в профиле.</span><span class="sxs-lookup"><span data-stu-id="c5539-117">On a compliant device, the identity accessing the resource should match the identity on the profile.</span></span>  <span data-ttu-id="c5539-118">Если это не так, вы увидите сообщение, аналогичное следующему.</span><span class="sxs-lookup"><span data-stu-id="c5539-118">If it doesn't, you'll see a message like the one in the next screenshot.</span></span> <span data-ttu-id="c5539-119">На снимка экрана "testadmin@evostsoneboxtest.com" — это учетная запись входа, необходимая для доступа к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="c5539-119">In the screenshot example, "testadmin@evostsoneboxtest.com" is the sign-in account needed to access the resource.</span></span>

![Сообщение от функции условного доступа в браузере](./media/edge-security/microsoft-edge-security-conditional-access.png)

<span data-ttu-id="c5539-121">Чтобы продолжить, необходимо переключиться на требуемый профиль (если таковой имеется) или создать профиль с совпадающим идентификатором.</span><span class="sxs-lookup"><span data-stu-id="c5539-121">To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.</span></span>

<span data-ttu-id="c5539-122">Чтобы войти в систему и настроить профиль, щелкните аватар в правом верхнем углу браузера.</span><span class="sxs-lookup"><span data-stu-id="c5539-122">To sign in and work with your profile, click the account picture in the top right corner of the browser.</span></span> <span data-ttu-id="c5539-123">В раскрывающемся меню можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c5539-123">You can use the dropdown menu to:</span></span>

- <span data-ttu-id="c5539-124">Выбрать другой профиль.</span><span class="sxs-lookup"><span data-stu-id="c5539-124">Select another profile.</span></span> <span data-ttu-id="c5539-125">Щелкните имя профиля.</span><span class="sxs-lookup"><span data-stu-id="c5539-125">Click the profile name.</span></span>
- <span data-ttu-id="c5539-126">Создать профиль.</span><span class="sxs-lookup"><span data-stu-id="c5539-126">Create a profile.</span></span> <span data-ttu-id="c5539-127">Щелкните **Добавить профиль**.</span><span class="sxs-lookup"><span data-stu-id="c5539-127">Click **Add a profile**.</span></span>
- <span data-ttu-id="c5539-128">Управлять профилями.</span><span class="sxs-lookup"><span data-stu-id="c5539-128">Manage your profiles.</span></span> <span data-ttu-id="c5539-129">Щелкните **Управление параметрами профиля**.</span><span class="sxs-lookup"><span data-stu-id="c5539-129">Click **Manage profile settings**.</span></span>

<span data-ttu-id="c5539-130">Эта функция доступна на всех платформах, включая все поддерживаемые версии Windows и macOS.</span><span class="sxs-lookup"><span data-stu-id="c5539-130">This support is available across all platforms, including all supported versions of Windows and macOS.</span></span>

### <span data-ttu-id="c5539-131">Развертывание функции условного доступа в Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="c5539-131">How to deploy Conditional Access in Azure Active Directory</span></span>

<span data-ttu-id="c5539-132">В разделе [Развертывание функции условного доступа](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) представлено подробное руководство по развертыванию функции условного доступа в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c5539-132">[Deploy Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help deploy Conditional Access in Azure Active Directory.</span></span>

## <span data-ttu-id="c5539-133">См. также</span><span class="sxs-lookup"><span data-stu-id="c5539-133">See also</span></span>

- [<span data-ttu-id="c5539-134">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="c5539-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="c5539-135">Видео: безопасность, совместимость и управляемость</span><span class="sxs-lookup"><span data-stu-id="c5539-135">Video: Security, compatibility, and manageability</span></span>](/microsoft-edge-video-security-compatibility-manageability.md)
