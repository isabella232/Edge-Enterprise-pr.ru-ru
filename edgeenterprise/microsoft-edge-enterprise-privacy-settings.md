---
title: Корпоративные параметры конфиденциальности Microsoft Edge
ms.author: likravit
author: dan-wesley
manager: srugh
ms.date: 05/26/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Настройка корпоративных параметров конфиденциальности Microsoft Edge
ms.openlocfilehash: 2b7a33087ae5110c53d18b3192486d4ae62fa540
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980968"
---
# <span data-ttu-id="7594f-103">Настройка политик Microsoft Edge для поддержки корпоративной конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="7594f-103">Configure Microsoft Edge policies to support enterprise privacy</span></span>

<span data-ttu-id="7594f-104">Корпорация Майкрософт стремится предоставлять организациям сведения и средства управления, необходимые для принятия решений о сборе данных в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7594f-104">Microsoft is committed to providing enterprises with the information and controls needed to make choices about data collection in Microsoft Edge.</span></span>

## <span data-ttu-id="7594f-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="7594f-105">Overview</span></span>

<span data-ttu-id="7594f-106">По умолчанию Microsoft Edge, развернутый на платформе, отличной от Windows, не отправляет диагностические данные или сведения о сайте в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7594f-106">By default, Microsoft Edge deployed on non-Windows platforms doesn't send diagnostic data or site information to Microsoft.</span></span> <span data-ttu-id="7594f-107">При развертывании Microsoft Edge в Windows 10 диагностические данные по умолчанию отправляются на основании пользовательского [параметра диагностических данных Windows](https://go.microsoft.com/fwlink/?linkid=2099569).</span><span class="sxs-lookup"><span data-stu-id="7594f-107">When Microsoft Edge is deployed on Windows 10, the default is to send diagnostic data based on the users' [Windows Diagnostic data setting](https://go.microsoft.com/fwlink/?linkid=2099569).</span></span>

<span data-ttu-id="7594f-108">Вы также можете настроить, как Microsoft Edge обрабатывает сбор данных для вашей организации, используя следующие групповые политики:</span><span class="sxs-lookup"><span data-stu-id="7594f-108">You can also configure how Microsoft Edge handles data collection for your organization with the following group policies:</span></span>

- <span data-ttu-id="7594f-109">[MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) — включить отчеты с данными об использовании и сбоях.</span><span class="sxs-lookup"><span data-stu-id="7594f-109">[MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - Enable usage and crash-related data reporting.</span></span>
- <span data-ttu-id="7594f-110">[SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) — отправка сведений о сайтах для улучшения служб Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7594f-110">[SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - Send site information to improve Microsoft services.</span></span>

## <span data-ttu-id="7594f-111">Настройка параметров политик.</span><span class="sxs-lookup"><span data-stu-id="7594f-111">Configure policy settings</span></span>

<span data-ttu-id="7594f-112">Прежде чем приступить к работе, скачайте и используйте последний шаблон политик Microsoft Edge (дополнительные сведения см. в разделе [Настройка Microsoft Edge](configure-microsoft-edge.md)).</span><span class="sxs-lookup"><span data-stu-id="7594f-112">Before you begin, download and use the latest Microsoft Edge Policy Template (For more information, see [Configure Microsoft Edge](configure-microsoft-edge.md).)</span></span>

### <span data-ttu-id="7594f-113">Включение отчетов с данными об использовании и сбоях</span><span class="sxs-lookup"><span data-stu-id="7594f-113">Enable usage and crash-related data reporting</span></span>

<span data-ttu-id="7594f-114">Эта политика позволяет отправлять отчеты с данными об использовании и сбоях Microsoft Edge в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7594f-114">This policy enables reporting of usage and crash-related data about Microsoft Edge to Microsoft.</span></span>

<span data-ttu-id="7594f-115">Microsoft Edge собирает ряд обязательных данных, необходимых для обеспечения безопасности, актуальности и надлежащей работы продукта.</span><span class="sxs-lookup"><span data-stu-id="7594f-115">Microsoft Edge collects a set of required data that's necessary to keep the product up to date, secure, and performing properly.</span></span> <span data-ttu-id="7594f-116">К этим данным относятся базовые сведения о подключении и конфигурации устройства из Microsoft Edge (текущее состояние согласия на сбор данных, версия приложения и состояние установки Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="7594f-116">This data includes basic device connectivity and configuration information from Microsoft Edge about the current data collection consent, app version, and installation state about your installation of Microsoft Edge.</span></span><span data-ttu-id="7594f-117"> Сбор этих данных можно отключить, отключив политику.</span><span class="sxs-lookup"><span data-stu-id="7594f-117"> This data collection can be turned off by disabling the policy.</span></span>

<span data-ttu-id="7594f-118">Включите эту политику, чтобы отправлять отчеты с данными об использовании и сбоях в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7594f-118">Enable this policy to send reporting of usage and crash-related data to Microsoft.</span></span> <span data-ttu-id="7594f-119">Отключите эту политику, чтобы не отправлять эти данные в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7594f-119">Disable this policy to not send the data to Microsoft.</span></span> <span data-ttu-id="7594f-120">В обоих случаях пользователи не смогут изменить или переопределить его.</span><span class="sxs-lookup"><span data-stu-id="7594f-120">In both cases, users can't change or override the setting.</span></span>

<span data-ttu-id="7594f-121">При запуске Microsoft Edge в Windows 10:</span><span class="sxs-lookup"><span data-stu-id="7594f-121">When Microsoft Edge is running on Windows 10:</span></span>

- <span data-ttu-id="7594f-122">Если эта политика не настроена, Microsoft Edge по умолчанию использует параметр диагностических данных Windows.</span><span class="sxs-lookup"><span data-stu-id="7594f-122">If this policy isn't configured, Microsoft Edge will default to the Windows diagnostic data setting.</span></span>
- <span data-ttu-id="7594f-123">Если эта политика включена, Microsoft Edge будет отправлять данные об использовании, только если для параметра диагностических данных Windows задано значение **Расширенный** или **Полный**.</span><span class="sxs-lookup"><span data-stu-id="7594f-123">If this policy is enabled, Microsoft Edge will only send usage data if the Windows Diagnostic data setting is set to **Enhanced** or **Full**.</span></span>
- <span data-ttu-id="7594f-124">Если эта политика отключена, Microsoft Edge не будет отправлять данные об использовании.</span><span class="sxs-lookup"><span data-stu-id="7594f-124">If this policy is disabled, Microsoft Edge will not send usage data.</span></span> <span data-ttu-id="7594f-125">Данные о сбоях отправляются в зависимости от параметра диагностических данных Windows.</span><span class="sxs-lookup"><span data-stu-id="7594f-125">Crash-related data is sent based on the Windows Diagnostic data setting.</span></span> <span data-ttu-id="7594f-126">[Дополнительные сведения о параметрах диагностических данных Windows](https://go.microsoft.com/fwlink/?linkid=2099569).</span><span class="sxs-lookup"><span data-stu-id="7594f-126">[Learn more about Windows Diagnostic data settings](https://go.microsoft.com/fwlink/?linkid=2099569).</span></span>

<span data-ttu-id="7594f-127">При запуске Microsoft Edge в Windows 7, 8 и macOS:</span><span class="sxs-lookup"><span data-stu-id="7594f-127">When Microsoft Edge is running on Windows 7, 8, and macOS:</span></span>

- <span data-ttu-id="7594f-128">Если эта политика не настроена, Microsoft Edge по умолчанию применяет настройки пользователя.</span><span class="sxs-lookup"><span data-stu-id="7594f-128">If this policy isn't configured, Microsoft Edge will default to the user's preference.</span></span>

### <span data-ttu-id="7594f-129">Отправка сведений о сайтах для улучшения служб Майкрософт</span><span class="sxs-lookup"><span data-stu-id="7594f-129">Send site information to improve Microsoft services</span></span>

<span data-ttu-id="7594f-130">Эта политика позволяет отправлять сведения о веб-сайтах, посещенных в Microsoft Edge, в корпорацию Майкрософт для улучшения продуктов и служб, таких как поиск.</span><span class="sxs-lookup"><span data-stu-id="7594f-130">This policy enables sending information about websites visited in Microsoft Edge to Microsoft to improve Microsoft products and services such as search.</span></span>

<span data-ttu-id="7594f-131">Включите эту политику, чтобы отправлять сведения о посещаемых вами веб-сайтах с помощью Microsoft Edge в Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7594f-131">Enable this policy to send information about websites visited in Microsoft Edge to Microsoft.</span></span> <span data-ttu-id="7594f-132">Отключите эту политику, чтобы не отправлять сведения о посещаемых вами веб-сайтах с помощью Microsoft Edge в Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7594f-132">Disable this policy to not send information about the websites that are visited in Microsoft Edge to Microsoft.</span></span> <span data-ttu-id="7594f-133">В обоих случаях пользователи не смогут изменить или переопределить его.</span><span class="sxs-lookup"><span data-stu-id="7594f-133">In both cases, users can't change or override the setting.</span></span>

<span data-ttu-id="7594f-134">При запуске Microsoft Edge в Windows 10:</span><span class="sxs-lookup"><span data-stu-id="7594f-134">When Microsoft Edge is running on Windows 10:</span></span>

- <span data-ttu-id="7594f-135">Если эта политика не настроена, Microsoft Edge по умолчанию использует параметр диагностических данных Windows.</span><span class="sxs-lookup"><span data-stu-id="7594f-135">If this policy isn't configured, Microsoft Edge will default to the Windows diagnostic data setting.</span></span>
- <span data-ttu-id="7594f-136">Если эта политика включена, Microsoft Edge будет отправлять данные о посещаемых веб-сайтах, только если для параметра диагностических данных Windows задано значение **Полный**.</span><span class="sxs-lookup"><span data-stu-id="7594f-136">If this policy is enabled, Microsoft Edge will only send information about the websites that are visited if the Windows Diagnostic data setting is set to **Full**.</span></span>
- <span data-ttu-id="7594f-137">Если эта политика отключена, Microsoft Edge не будет отправлять данные о посещаемых веб-сайтах.</span><span class="sxs-lookup"><span data-stu-id="7594f-137">If this policy is disabled, Microsoft Edge will not send info about websites visited.</span></span> <span data-ttu-id="7594f-138">[Дополнительные сведения о параметрах диагностических данных Windows](https://go.microsoft.com/fwlink/?linkid=2099569).</span><span class="sxs-lookup"><span data-stu-id="7594f-138">To [learn more about Windows Diagnostic data settings](https://go.microsoft.com/fwlink/?linkid=2099569).</span></span>

<span data-ttu-id="7594f-139">При запуске Microsoft Edge в Windows 7, 8 и macOS:</span><span class="sxs-lookup"><span data-stu-id="7594f-139">When Microsoft Edge is running on Windows 7, 8, and macOS:</span></span>

- <span data-ttu-id="7594f-140">Если эта политика не настроена, Microsoft Edge по умолчанию применяет настройки пользователя.</span><span class="sxs-lookup"><span data-stu-id="7594f-140">If this policy isn't configured, Microsoft Edge will default to the user's preference.</span></span>

## <span data-ttu-id="7594f-141">Сведения о реализации</span><span class="sxs-lookup"><span data-stu-id="7594f-141">Implementation details</span></span>

<span data-ttu-id="7594f-142">Для понимания нашей реализации с зависимостью от параметра диагностических данных Windows для Windows 10 в следующей таблице описывается конфигурация, если параметры **Включение отчетов с данными об использовании и сбоях** и **Отправка сведений о сайтах для улучшения служб Майкрософт** не настроены.</span><span class="sxs-lookup"><span data-stu-id="7594f-142">For Windows 10 to understand our implementation with the dependency on the Windows Diagnostic data setting, the following table describes our configuration if **Enable usage and crash-related data reporting** and **Send site information to improve Microsoft services** were not configured.</span></span>

| <span data-ttu-id="7594f-143">Параметр диагностических данных Windows</span><span class="sxs-lookup"><span data-stu-id="7594f-143">Windows Diagnostic data setting</span></span> | <span data-ttu-id="7594f-144">Включение отчетов с данными об использовании и сбоях</span><span class="sxs-lookup"><span data-stu-id="7594f-144">Enable usage and crash-related data reporting</span></span> | <span data-ttu-id="7594f-145">Отправка сведений о сайтах для улучшения служб Майкрософт</span><span class="sxs-lookup"><span data-stu-id="7594f-145">Send site information to improve Microsoft services</span></span> |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="7594f-146">Безопасность</span><span class="sxs-lookup"><span data-stu-id="7594f-146">Security</span></span>                        | <span data-ttu-id="7594f-147">Не отправляются</span><span class="sxs-lookup"><span data-stu-id="7594f-147">Not sent</span></span>                                      | <span data-ttu-id="7594f-148">Не отправляются</span><span class="sxs-lookup"><span data-stu-id="7594f-148">Not sent</span></span>                                            |
| <span data-ttu-id="7594f-149">Базовый</span><span class="sxs-lookup"><span data-stu-id="7594f-149">Basic</span></span>                           | <span data-ttu-id="7594f-150">Не отправляются</span><span class="sxs-lookup"><span data-stu-id="7594f-150">Not sent</span></span>                                      | <span data-ttu-id="7594f-151">Не отправляются</span><span class="sxs-lookup"><span data-stu-id="7594f-151">Not sent</span></span>                                            |
| <span data-ttu-id="7594f-152">Расширенный</span><span class="sxs-lookup"><span data-stu-id="7594f-152">Enhanced</span></span>                        | <span data-ttu-id="7594f-153">Отправляются</span><span class="sxs-lookup"><span data-stu-id="7594f-153">Sent</span></span>                                          | <span data-ttu-id="7594f-154">Не отправляются</span><span class="sxs-lookup"><span data-stu-id="7594f-154">Not sent</span></span>                                            |
| <span data-ttu-id="7594f-155">Полный</span><span class="sxs-lookup"><span data-stu-id="7594f-155">Full</span></span>                            | <span data-ttu-id="7594f-156">Отправляются</span><span class="sxs-lookup"><span data-stu-id="7594f-156">Sent</span></span>                                          | <span data-ttu-id="7594f-157">Отправляются</span><span class="sxs-lookup"><span data-stu-id="7594f-157">Sent</span></span>                                                |

<span data-ttu-id="7594f-158">Если конфигурация Windows 10 не соответствует приведенной выше таблице, используется тот параметр, который предполагает сбор меньшего объема данных.</span><span class="sxs-lookup"><span data-stu-id="7594f-158">If your configurations for Windows 10 are misconfigured in accordance with the preceding table, we will fall back to the lesser data collection setting.</span></span>

<span data-ttu-id="7594f-159">Например:</span><span class="sxs-lookup"><span data-stu-id="7594f-159">For example:</span></span>

- <span data-ttu-id="7594f-160">Вы устанавливаете значение **Включено** для параметра "Включение отчетов с данными об использовании и сбоях", но для параметра диагностических данных Windows задано значение **Базовый**.</span><span class="sxs-lookup"><span data-stu-id="7594f-160">You set the "Enable usage and crash-related data reporting" policy to **Enabled** but the Windows Diagnostic data setting is set to **Basic**.</span></span> <span data-ttu-id="7594f-161">В этом случае данные об использовании и сбоях не отправляются.</span><span class="sxs-lookup"><span data-stu-id="7594f-161">We won't send usage and crash-related data.</span></span>
- <span data-ttu-id="7594f-162">Вы устанавливаете значение **Выключено** для параметра "Отправка сведений о сайтах для улучшения служб Майкрософт", но для параметра диагностических данных Windows задано значение **Полный**.</span><span class="sxs-lookup"><span data-stu-id="7594f-162">You set the "Send site information to improve Microsoft services" policy to **Disabled** but the Windows Diagnostic data setting is set to **Full**.</span></span> <span data-ttu-id="7594f-163">В этом случае сведения о посещаемых вами сайтах отправляться не будут.</span><span class="sxs-lookup"><span data-stu-id="7594f-163">We won't send information about the sites that are visited.</span></span>

<span data-ttu-id="7594f-164">Правильная конфигурация для указанных выше параметров— значение **Включено** для параметра "Включение отчетов с данными об использовании и сбоях" и значение **Расширенные** или **Полные** для параметра диагностических данных Windows.</span><span class="sxs-lookup"><span data-stu-id="7594f-164">The correct implementation for the previous settings is to set the "Enable usage and crash-related data reporting" policy to **Enabled** and set the Windows Diagnostic data setting to **Enhanced** or **Full**.</span></span>

## <span data-ttu-id="7594f-165">Дополнительные параметры политики конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="7594f-165">Additional privacy policy options</span></span>

<span data-ttu-id="7594f-166">Возможно, вам потребуется использовать следующие групповые политики, связанные с конфиденциальностью данных.</span><span class="sxs-lookup"><span data-stu-id="7594f-166">You may want to consider the following group policies related to data privacy:</span></span>

- <span data-ttu-id="7594f-167">Блокировка cookie-файлов на определенных сайтах</span><span class="sxs-lookup"><span data-stu-id="7594f-167">Block cookies on specific sites</span></span>
- <span data-ttu-id="7594f-168">Блокировка сторонних cookie-файлов</span><span class="sxs-lookup"><span data-stu-id="7594f-168">Block third-party cookies</span></span>
- <span data-ttu-id="7594f-169">Настройка запрета на отслеживание</span><span class="sxs-lookup"><span data-stu-id="7594f-169">Configure Do Not Track</span></span>
- <span data-ttu-id="7594f-170">Отключение режима InPrivate</span><span class="sxs-lookup"><span data-stu-id="7594f-170">Disable InPrivate mode</span></span>

## <span data-ttu-id="7594f-171">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7594f-171">See also</span></span>

- [<span data-ttu-id="7594f-172">Целевая страница Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="7594f-172">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="7594f-173">Политики Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7594f-173">Microsoft Edge policies</span></span>](microsoft-edge-policies.md)
- [<span data-ttu-id="7594f-174">Техническая документация по конфиденциальности Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7594f-174">Microsoft Edge Privacy Whitepaper</span></span>](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper)
