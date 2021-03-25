---
title: Защита от потери данных в Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 03/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Защита от потери данных в Microsoft Edge
ms.openlocfilehash: ac34386ed1b691d7b45f30c2b2ec295955d11104
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447933"
---
# <a name="data-loss-prevention-dlp-in-microsoft-edge"></a><span data-ttu-id="76c93-103">Защита от потери данных в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="76c93-103">Data Loss Prevention (DLP) in Microsoft Edge</span></span>

<span data-ttu-id="76c93-104">Защита от потери данных — это система технологий, определяющая и защищающая конфиденциальные корпоративные данные от несанкционированного раскрытия.</span><span class="sxs-lookup"><span data-stu-id="76c93-104">Data loss prevention (DLP) is a system of technologies that identify and safeguard sensitive enterprise data from unauthorized disclosure.</span></span> <span data-ttu-id="76c93-105">Чтобы обеспечить соблюдение бизнес-стандартов и отраслевых норм, организации должны защищать конфиденциальные данные и предотвращать несанкционированное раскрытие.</span><span class="sxs-lookup"><span data-stu-id="76c93-105">To comply with business standards and industry regulations, organizations must protect sensitive information and prevent its unauthorized disclosure.</span></span> <span data-ttu-id="76c93-106">Конфиденциальная информация включает финансовые данные и личные сведения (PII), такие как номера кредитных карт, номера социального страхования или медицинские записи, а также многое другое.</span><span class="sxs-lookup"><span data-stu-id="76c93-106">Sensitive information includes financial data or personally identifiable information (PII) such as credit card numbers, social security numbers, or health records, among many other things.</span></span>

<span data-ttu-id="76c93-107">Удаленная работа повысила важность использования защиты от потери данных.</span><span class="sxs-lookup"><span data-stu-id="76c93-107">Remote work has increased the emphasis on using DLP.</span></span> <span data-ttu-id="76c93-108">С увеличением личных и рабочих операций на устройствах в организациях повышается риск несанкционированного распространения корпоративных данных за пределами рабочего места.</span><span class="sxs-lookup"><span data-stu-id="76c93-108">With the growing use of personal and work activities on devices, enterprises are seeing an increased risk of unauthorized sharing of corporate data outside the workplace.</span></span>

<span data-ttu-id="76c93-109">Такое смешение действий пользователей распространяется на различные устройства, когда данные перемещаются между личными и корпоративными устройствами в различных общедоступных и закрытых сетях.</span><span class="sxs-lookup"><span data-stu-id="76c93-109">This blending of user activities has spread to devices as well, where data is moved between personal and corporate devices over a variety of public and private networks.</span></span> <span data-ttu-id="76c93-110">Итоговым результатом стал существенно возросший риск раскрытия конфиденциальных данных.</span><span class="sxs-lookup"><span data-stu-id="76c93-110">The net result is a dramatically increased risk of exposing sensitive data.</span></span>

<span data-ttu-id="76c93-111">Microsoft Edge изначально поддерживает два разных решения для защиты от потери данных: защита от потери данных в конечной точке Майкрософт и Windows Information Protection (WIP).</span><span class="sxs-lookup"><span data-stu-id="76c93-111">Microsoft Edge natively supports two different DLP solutions, Microsoft Endpoint DLP and Windows Information Protection (WIP).</span></span>

## <a name="microsoft-endpoint-data-loss-prevention-endpoint-dlp"></a><span data-ttu-id="76c93-112">Защита от потери данных в конечной точке Майкрософт (Endpoint DLP)</span><span class="sxs-lookup"><span data-stu-id="76c93-112">Microsoft Endpoint data loss prevention (Endpoint DLP)</span></span>

<span data-ttu-id="76c93-113">Защита от потери данных в конечной точке Майкрософт — это защита от потери данных нового поколения, использующая современные концепции, такие как защита, ориентированная на данные.</span><span class="sxs-lookup"><span data-stu-id="76c93-113">Microsoft Endpoint DLP is the next generation of data loss prevention using modern concepts such as data-centric protection.</span></span> <span data-ttu-id="76c93-114">Она встроена в Windows 10 и Microsoft Edge, поэтому на устройстве не требуются дополнительные агенты или подключаемые модули.</span><span class="sxs-lookup"><span data-stu-id="76c93-114">It's built-in to Windows 10 and Microsoft Edge so it doesn't need additional agents or plugins on the device.</span></span>

> [!NOTE]
> <span data-ttu-id="76c93-115">Эта статья относится к Microsoft Edge версии 85 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="76c93-115">This applies to Microsoft Edge version 85 or later.</span></span>

<span data-ttu-id="76c93-116">Чтобы узнать больше о политике защиты от потери данных (DLP) конечной точки, используйте следующие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="76c93-116">To learn more about Endpoint DLP, use the following resources:</span></span>

- [<span data-ttu-id="76c93-117">Видео. Microsoft Edge и защита от потери данных</span><span class="sxs-lookup"><span data-stu-id="76c93-117">Video: Microsoft Edge and Data loss prevention (DLP)</span></span>](microsoft-edge-video-security-dlp.md)
- [<span data-ttu-id="76c93-118">Сведения о защите от потери данных в конечной точке Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="76c93-118">Learn about Microsoft 365 Endpoint data loss prevention</span></span>](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide)
- [<span data-ttu-id="76c93-119">Начало работы с функцией защиты от потери данных в конечной точке</span><span class="sxs-lookup"><span data-stu-id="76c93-119">Get started with Endpoint data loss prevention</span></span>](/microsoft-365/compliance/endpoint-dlp-getting-started?preserve-view=true&view=o365-worldwide)

<span data-ttu-id="76c93-120">Microsoft Edge внедряет настроенные администратором политики для конфиденциальных файлов и записывает события аудита для несоответствующих действий.</span><span class="sxs-lookup"><span data-stu-id="76c93-120">Microsoft Edge enforces admin configured policies for sensitive files and records audit events for non-compliant activities.</span></span>

<span data-ttu-id="76c93-121">Ниже перечислены некоторые пользовательские действия, доступные для аудита и управления на устройствах с Windows 10:</span><span class="sxs-lookup"><span data-stu-id="76c93-121">Some of the user activities that you can audit and manage on devices running Windows 10 include the following activities:</span></span>

- <span data-ttu-id="76c93-122">Отправка файла. Защита от отправки конфиденциального файла в неавторизованные облачные расположения.</span><span class="sxs-lookup"><span data-stu-id="76c93-122">File Upload: Protect sensitive file upload to unauthorized cloud locations.</span></span> <!-- The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.-->
- <span data-ttu-id="76c93-123">Защита буфера обмена. Защита от копирования конфиденциальных данных из файла.</span><span class="sxs-lookup"><span data-stu-id="76c93-123">Clipboard Protection: Protect sensitive data from being copied out of the file.</span></span>
- <span data-ttu-id="76c93-124">Защита печати. Защита конфиденциального файла от печати.</span><span class="sxs-lookup"><span data-stu-id="76c93-124">Print Protection: Protect sensitive file from being printed.</span></span>
- <span data-ttu-id="76c93-125">Сохранение на USB или в сети. Защита конфиденциального файла от сохранения на съемном USB-накопителе или в неавторизованных сетевых расположениях.</span><span class="sxs-lookup"><span data-stu-id="76c93-125">Save to USB/Network: Protect sensitive file from being saved to removable USB storage or unauthorized network locations.</span></span>

<span data-ttu-id="76c93-126">Дополнительные сведения о действиях пользователей, доступных для аудита и управления, см. в разделе [Действия в конечных точках, доступные для отслеживания и реагирования](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).</span><span class="sxs-lookup"><span data-stu-id="76c93-126">For more detailed information about user activities you can audit and manage, see [Endpoint activities you can monitor and take action on](/microsoft-365/compliance/endpoint-dlp-learn-about?preserve-view=true&view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).</span></span>

## <a name="windows-information-protection"></a><span data-ttu-id="76c93-127">Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="76c93-127">Windows Information Protection</span></span>

<span data-ttu-id="76c93-128">См. статью [Поддержка Windows Information Protection (WIP) в Microsoft Edge](./microsoft-edge-security-windows-information-protection.md) с описанием того, как Microsoft Edge поддерживает Windows Information Protection (WIP).</span><span class="sxs-lookup"><span data-stu-id="76c93-128">Check out [Support for Windows Information Protection](./microsoft-edge-security-windows-information-protection.md), which describes how Microsoft Edge supports Windows Information Protection (WIP).</span></span> <span data-ttu-id="76c93-129">Вы можете узнать больше о системных требованиях, преимуществах и поддерживаемых функциях в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="76c93-129">You can learn moe about system requirements, benefits, and supported features in the following sections:</span></span>

- [<span data-ttu-id="76c93-130">Требования к системе</span><span class="sxs-lookup"><span data-stu-id="76c93-130">System Requirements</span></span>](./microsoft-edge-security-windows-information-protection.md#system-requirements)
- [<span data-ttu-id="76c93-131">Преимущества Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="76c93-131">Windows Information Protection Benefits</span></span>](./microsoft-edge-security-windows-information-protection.md#windows-information-protection-benefits)
- [<span data-ttu-id="76c93-132">Возможности WIP, поддерживаемые в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="76c93-132">WIP features supported in Microsoft Edge</span></span>](./microsoft-edge-security-windows-information-protection.md#wip-features-supported-in-microsoft-edge)

## <a name="see-also"></a><span data-ttu-id="76c93-133">См. также</span><span class="sxs-lookup"><span data-stu-id="76c93-133">See also</span></span>

- [<span data-ttu-id="76c93-134">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="76c93-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="76c93-135">Видео. Защита от потери данных — Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="76c93-135">Video: Data loss prevention - Microsoft Edge</span></span>](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [<span data-ttu-id="76c93-136">Обзор защиты от потери данных</span><span class="sxs-lookup"><span data-stu-id="76c93-136">Overview of data loss prevention</span></span>](/microsoft-365/compliance/data-loss-prevention-policies?preserve-view=true&view=o365-worldwide)
- [<span data-ttu-id="76c93-137">Защита корпоративных данных с помощью Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="76c93-137">Protect your enterprise data using Windows Information Protection</span></span>](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)