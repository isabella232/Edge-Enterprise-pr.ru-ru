---
title: Microsoft Edge и условный доступ
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 10/02/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge и условный доступ
ms.openlocfilehash: a81d39c15f418dab6565ee7acc45de17f66e3828
ms.sourcegitcommit: 3478cfcf2b03944213a7c7c61f05490bc37aa7c4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/03/2020
ms.locfileid: "11094781"
---
# <span data-ttu-id="c017c-103">Microsoft Edge и условный доступ</span><span class="sxs-lookup"><span data-stu-id="c017c-103">Microsoft Edge and Conditional Access</span></span>
  
<span data-ttu-id="c017c-104">В этой статье описано, как Microsoft Edge поддерживает условный доступ и как получить доступ к ресурсам, защищенным с помощью условного доступа.</span><span class="sxs-lookup"><span data-stu-id="c017c-104">This article describes how Microsoft Edge supports Conditional Access, and how to access resources protected by Conditional Access.</span></span>

> [!NOTE]
> <span data-ttu-id="c017c-105">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="c017c-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="c017c-106">Ключевыми аспектами обеспечения безопасности в облаке являются идентификация и предоставление доступа к управлению облачными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="c017c-106">A key aspect of cloud security is identity and access when it comes to managing your cloud resources.</span></span> <span data-ttu-id="c017c-107">В мире с преобладанием мобильных и облачных технологий пользователи могут получать доступ к ресурсам организации с помощью различных устройств и приложений из любого места.</span><span class="sxs-lookup"><span data-stu-id="c017c-107">In a mobile-first, cloud-first world, users can access your organization's resources using a variety of devices and apps from anywhere.</span></span> <span data-ttu-id="c017c-108">В результате этого недостаточно уделять внимание только тому, кто может получить доступ к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="c017c-108">As a result of this, just focusing on who can access a resource is not sufficient.</span></span> <span data-ttu-id="c017c-109">Также необходимо учитывать, каким образом осуществляется обращение к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="c017c-109">You also need to factor in how a resource is accessed.</span></span> <span data-ttu-id="c017c-110">Условный доступ в Azure Active Directory (Azure AD) помогает сохранять баланс между безопасностью и производительностью.</span><span class="sxs-lookup"><span data-stu-id="c017c-110">Azure Active Directory (Azure AD) Conditional Access helps you master the balance between security and productivity.</span></span>

## <span data-ttu-id="c017c-111">Доступ к ресурсам, защищенным с помощью функции условного доступа, в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c017c-111">Accessing Conditional Access protected resources in Microsoft Edge</span></span>

<span data-ttu-id="c017c-112">В Microsoft Edge реализована встроенная поддержка условного доступа Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c017c-112">Microsoft Edge natively supports Azure AD Conditional Access.</span></span> <span data-ttu-id="c017c-113">Устанавливать отдельное расширение не требуется.</span><span class="sxs-lookup"><span data-stu-id="c017c-113">There's no need to install a separate extension.</span></span> <span data-ttu-id="c017c-114">При входе в профиль Microsoft Edge с корпоративными учетными данными Azure AD браузер Microsoft Edge обеспечивает простой доступ к корпоративным облачным ресурсам, защищенным с помощью функции условного доступа.</span><span class="sxs-lookup"><span data-stu-id="c017c-114">When you're signed into a Microsoft Edge profile with enterprise Azure AD credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using Conditional Access.</span></span>

<span data-ttu-id="c017c-115">На совместимом устройстве идентификатор, обращающийся к ресурсу, должен соответствовать идентификатору в профиле.</span><span class="sxs-lookup"><span data-stu-id="c017c-115">On a compliant device, the identity accessing the resource should match the identity on the profile.</span></span>  <span data-ttu-id="c017c-116">Если это не так, вы увидите сообщение, аналогичное следующему.</span><span class="sxs-lookup"><span data-stu-id="c017c-116">If it doesn't, you'll see a message like the one in the next screenshot.</span></span> <span data-ttu-id="c017c-117">На снимка экрана "testadmin@evostsoneboxtest.com" — это учетная запись входа, необходимая для доступа к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="c017c-117">In the screenshot example, "testadmin@evostsoneboxtest.com" is the sign-in account needed to access the resource.</span></span>

![Сообщение от функции условного доступа в браузере](./media/edge-security/microsoft-edge-security-conditional-access.png)

<span data-ttu-id="c017c-119">Чтобы продолжить, необходимо переключиться на требуемый профиль (если таковой имеется) или создать профиль с совпадающим идентификатором.</span><span class="sxs-lookup"><span data-stu-id="c017c-119">To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.</span></span>

<span data-ttu-id="c017c-120">Чтобы войти в систему и настроить профиль, щелкните аватар в правом верхнем углу браузера.</span><span class="sxs-lookup"><span data-stu-id="c017c-120">To sign in and work with your profile, click the account picture in the top right corner of the browser.</span></span> <span data-ttu-id="c017c-121">В раскрывающемся меню можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c017c-121">You can use the dropdown menu to:</span></span>

- <span data-ttu-id="c017c-122">Выбрать другой профиль.</span><span class="sxs-lookup"><span data-stu-id="c017c-122">Select another profile.</span></span> <span data-ttu-id="c017c-123">Щелкните имя профиля.</span><span class="sxs-lookup"><span data-stu-id="c017c-123">Click the profile name.</span></span>
- <span data-ttu-id="c017c-124">Создать профиль.</span><span class="sxs-lookup"><span data-stu-id="c017c-124">Create a profile.</span></span> <span data-ttu-id="c017c-125">Щелкните **Добавить профиль**.</span><span class="sxs-lookup"><span data-stu-id="c017c-125">Click **Add a profile**.</span></span>
- <span data-ttu-id="c017c-126">Управлять профилями.</span><span class="sxs-lookup"><span data-stu-id="c017c-126">Manage your profiles.</span></span> <span data-ttu-id="c017c-127">Щелкните **Управление параметрами профиля**.</span><span class="sxs-lookup"><span data-stu-id="c017c-127">Click **Manage profile settings**.</span></span>

<span data-ttu-id="c017c-128">Эта функция доступна на всех платформах, включая все поддерживаемые версии Windows и macOS.</span><span class="sxs-lookup"><span data-stu-id="c017c-128">This support is available across all platforms, including all supported versions of Windows and macOS.</span></span>

### <span data-ttu-id="c017c-129">Развертывание функции условного доступа в Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="c017c-129">How to deploy Conditional Access in Azure Active Directory</span></span>

<span data-ttu-id="c017c-130">В разделе [Развертывание функции условного доступа](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) представлено подробное руководство по развертыванию функции условного доступа в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c017c-130">[Deploy Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help deploy Conditional Access in Azure Active Directory.</span></span>

## <span data-ttu-id="c017c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c017c-131">See also</span></span>

- [<span data-ttu-id="c017c-132">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="c017c-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="c017c-133">Видео: безопасность, совместимость и управляемость</span><span class="sxs-lookup"><span data-stu-id="c017c-133">Video: Security, compatibility, and manageability</span></span>](/microsoft-edge-video-security-compatibility-manageability.md)
