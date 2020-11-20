---
title: Защита от потери данных в Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 11/18/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Защита от потери данных в Microsoft Edge
ms.openlocfilehash: 72f670caf34a09cdfc7f47575f688c2a39d3c221
ms.sourcegitcommit: 5a5be508c3c9c57187aca821b4a16f639abdd7e2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "11176946"
---
# <span data-ttu-id="54810-103">Защита от потери данных в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="54810-103">Data Loss Prevention (DLP) in Microsoft Edge</span></span>

<span data-ttu-id="54810-104">Защита от потери данных — это система технологий, определяющая и защищающая конфиденциальные корпоративные данные от несанкционированного раскрытия.</span><span class="sxs-lookup"><span data-stu-id="54810-104">Data loss prevention (DLP) is a system of technologies that identify and safeguard sensitive enterprise data from unauthorized disclosure.</span></span> <span data-ttu-id="54810-105">Чтобы обеспечить соблюдение бизнес-стандартов и отраслевых норм, организации должны защищать конфиденциальные данные и предотвращать несанкционированное раскрытие.</span><span class="sxs-lookup"><span data-stu-id="54810-105">To comply with business standards and industry regulations, organizations must protect sensitive information and prevent its unauthorized disclosure.</span></span> <span data-ttu-id="54810-106">Конфиденциальная информация включает финансовые данные и личные сведения (PII), такие как номера кредитных карт, номера социального страхования или медицинские записи, а также многое другое.</span><span class="sxs-lookup"><span data-stu-id="54810-106">Sensitive information includes financial data or personally identifiable information (PII) such as credit card numbers, social security numbers, or health records, among many other things.</span></span>

<span data-ttu-id="54810-107">Удаленная работа повысила важность использования защиты от потери данных.</span><span class="sxs-lookup"><span data-stu-id="54810-107">Remote work has increased the emphasis on using DLP.</span></span> <span data-ttu-id="54810-108">С увеличением личных и рабочих операций на устройствах в организациях повышается риск несанкционированного распространения корпоративных данных за пределами рабочего места.</span><span class="sxs-lookup"><span data-stu-id="54810-108">With the growing use of personal and work activities on devices, enterprises are seeing an increased risk of unauthorized sharing of corporate data outside the workplace.</span></span>

<span data-ttu-id="54810-109">Такое смешение действий пользователей распространяется на различные устройства, когда данные перемещаются между личными и корпоративными устройствами в различных общедоступных и закрытых сетях.</span><span class="sxs-lookup"><span data-stu-id="54810-109">This blending of user activities has spread to devices as well, where data is moved between personal and corporate devices over a variety of public and private networks.</span></span> <span data-ttu-id="54810-110">Итоговым результатом стал существенно возросший риск раскрытия конфиденциальных данных.</span><span class="sxs-lookup"><span data-stu-id="54810-110">The net result is a dramatically increased risk of exposing sensitive data.</span></span>

<span data-ttu-id="54810-111">Microsoft Edge изначально поддерживает два разных решения для защиты от потери данных: защита от потери данных в конечной точке Майкрософт и Windows Information Protection (WIP).</span><span class="sxs-lookup"><span data-stu-id="54810-111">Microsoft Edge natively supports two different DLP solutions, Microsoft Endpoint DLP and Windows Information Protection (WIP).</span></span>

## <span data-ttu-id="54810-112">Защита от потери данных в конечной точке Майкрософт (Endpoint DLP)</span><span class="sxs-lookup"><span data-stu-id="54810-112">Microsoft Endpoint data loss prevention (Endpoint DLP)</span></span>

<span data-ttu-id="54810-113">Защита от потери данных в конечной точке Майкрософт — это защита от потери данных нового поколения, использующая современные концепции, такие как защита, ориентированная на данные.</span><span class="sxs-lookup"><span data-stu-id="54810-113">Microsoft Endpoint DLP is the next generation of data loss prevention using modern concepts such as data-centric protection.</span></span> <span data-ttu-id="54810-114">Она встроена в Windows 10 и Microsoft Edge, поэтому на устройстве не требуются дополнительные агенты или подключаемые модули.</span><span class="sxs-lookup"><span data-stu-id="54810-114">It's built-in to Windows 10 and Microsoft Edge so it doesn't need additional agents or plugins on the device.</span></span>

> [!NOTE]
> <span data-ttu-id="54810-115">Эта статья относится к Microsoft Edge версии 85 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="54810-115">This applies to Microsoft Edge version 85 or later.</span></span>

<span data-ttu-id="54810-116">Дополнительные сведения о защите от потери данных в конечной точке см. в следующих статьях.</span><span class="sxs-lookup"><span data-stu-id="54810-116">To learn more about Endpoint DLP:</span></span>

- [<span data-ttu-id="54810-117">Сведения о защите от потери данных в конечной точке Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="54810-117">Learn about Microsoft 365 Endpoint data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide)
- [<span data-ttu-id="54810-118">Начало работы с функцией защиты от потери данных в конечной точке</span><span class="sxs-lookup"><span data-stu-id="54810-118">Get started with Endpoint data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-getting-started?view=o365-worldwide)

<span data-ttu-id="54810-119">Microsoft Edge внедряет настроенные администратором политики для конфиденциальных файлов и записывает события аудита для несоответствующих действий.</span><span class="sxs-lookup"><span data-stu-id="54810-119">Microsoft Edge enforces admin configured policies for sensitive files and records audit events for non-compliant activities.</span></span>

<span data-ttu-id="54810-120">Ниже перечислены некоторые пользовательские действия, доступные для аудита и управления на устройствах с Windows 10:</span><span class="sxs-lookup"><span data-stu-id="54810-120">Some of the user activities that you can audit and manage on devices running Windows 10 include the following activities:</span></span>

- <span data-ttu-id="54810-121">Отправка файла. Защита от отправки конфиденциального файла в неавторизованные облачные расположения.</span><span class="sxs-lookup"><span data-stu-id="54810-121">File Upload: Protect sensitive file upload to unauthorized cloud locations.</span></span> <span data-ttu-id="54810-122">На следующих 3 снимках экрана показана последовательность того, как пользователь пытается отправить конфиденциальный файл данных в собственное локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="54810-122">The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.</span></span>
- <span data-ttu-id="54810-123">Защита буфера обмена. Защита от копирования конфиденциальных данных из файла.</span><span class="sxs-lookup"><span data-stu-id="54810-123">Clipboard Protection: Protect sensitive data from being copied out of the file.</span></span>
- <span data-ttu-id="54810-124">Защита печати. Защита конфиденциального файла от печати.</span><span class="sxs-lookup"><span data-stu-id="54810-124">Print Protection: Protect sensitive file from being printed.</span></span>
- <span data-ttu-id="54810-125">Сохранение на USB или в сети. Защита конфиденциального файла от сохранения на съемном USB-накопителе или в неавторизованных сетевых расположениях.</span><span class="sxs-lookup"><span data-stu-id="54810-125">Save to USB/Network: Protect sensitive file from being saved to removable USB storage or unauthorized network locations.</span></span>

<span data-ttu-id="54810-126">Дополнительные сведения о действиях пользователей, доступных для аудита и управления, см. в разделе [Действия в конечных точках, доступные для отслеживания и реагирования](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).</span><span class="sxs-lookup"><span data-stu-id="54810-126">For more detailed information about user activities you can audit and manage, see [Endpoint activities you can monitor and take action on](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).</span></span>

## <span data-ttu-id="54810-127">Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="54810-127">Windows Information Protection</span></span>

<span data-ttu-id="54810-128">См. статью [Поддержка Windows Information Protection (WIP) в Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection) с описанием того, как Microsoft Edge поддерживает Windows Information Protection (WIP).</span><span class="sxs-lookup"><span data-stu-id="54810-128">Check out [Support for Windows Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection), which describes how Microsoft Edge supports Windows Information Protection (WIP).</span></span> <span data-ttu-id="54810-129">Вы можете узнать больше о системных требованиях, преимуществах и поддерживаемых функциях в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="54810-129">You can learn moe about system requirements, benefits, and supported features in the following sections:</span></span>

- [<span data-ttu-id="54810-130">Требования к системе</span><span class="sxs-lookup"><span data-stu-id="54810-130">System Requirements</span></span>](https://docs.microsoft.com/deployedge/:microsoft-edge-security-windows-information-protection#system-requirements)
- [<span data-ttu-id="54810-131">Преимущества Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="54810-131">Windows Information Protection Benefits</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#windows-information-protection-benefits)
- [<span data-ttu-id="54810-132">Возможности WIP, поддерживаемые в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="54810-132">WIP features supported in Microsoft Edge</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-information-protection#wip-features-supported-in-microsoft-edge)

## <span data-ttu-id="54810-133">См. также</span><span class="sxs-lookup"><span data-stu-id="54810-133">See also</span></span>

- [<span data-ttu-id="54810-134">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="54810-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="54810-135">Видео. Защита от потери данных — Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="54810-135">Video: Data loss prevention - Microsoft Edge</span></span>](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [<span data-ttu-id="54810-136">Обзор защиты от потери данных</span><span class="sxs-lookup"><span data-stu-id="54810-136">Overview of data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies?view=o365-worldwide)
- [<span data-ttu-id="54810-137">Защита корпоративных данных с помощью Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="54810-137">Protect your enterprise data using Windows Information Protection</span></span>](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)
