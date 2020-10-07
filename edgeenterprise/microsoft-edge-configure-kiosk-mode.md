---
title: Настройка режима терминала в Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 10/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Настройка режима терминала в Microsoft Edge
ms.openlocfilehash: 799b3dd4b7fc96f0b8e5cb718bca98fd4f38ec15
ms.sourcegitcommit: 78905f66f4a6590a57c8f2bf808af92106b62996
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/05/2020
ms.locfileid: "11094866"
---
# <span data-ttu-id="ba9b6-103">Настройка режима терминала в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ba9b6-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="ba9b6-104">В этой статье рассказывается, как настроить параметры режим терминала в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="ba9b6-105">Кроме того, вы можете воспользоваться схемой функций, которые мы настраиваем.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-105">There's also a roadmap of features we are targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="ba9b6-106">Эта статья относится к Microsoft Edge версии 87 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-106">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="ba9b6-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="ba9b6-107">Overview</span></span>

<span data-ttu-id="ba9b6-108">Режим терминала Microsoft Edge предлагает два варианта блокировки браузера, чтобы организации могли создавать, управлять и обеспечивать наилучшие условия для своих клиентов.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-108">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="ba9b6-109">Доступны следующие варианты блокировки:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-109">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="ba9b6-110">Цифровые или интерактивные вывески отображают конкретный сайт в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-110">The Digital/Interactive signage experience displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="ba9b6-111">В общедоступном браузере работает ограниченная версия Microsoft Edge с несколькими вкладками.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-111">The public-browsing experience runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="ba9b6-112">В обоих случаях выполняется сеанс Microsoft Edge InPrivate, который защищает пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-112">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="ba9b6-113">Настройка режима терминала в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ba9b6-113">Set up Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="ba9b6-114">Начальный набор функций режима терминала теперь доступен для тестирования на канале Microsoft Edge Canary, версия 87.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-114">An initial set of kiosk mode features are now available to test with Microsoft Edge Canary Channel, version 87.</span></span> <span data-ttu-id="ba9b6-115">Вы можете скачать Microsoft Edge Canary со страницы [каналов предварительной оценки Microsoft Edge](https://www.microsoftedgeinsider.com/download).</span><span class="sxs-lookup"><span data-stu-id="ba9b6-115">You can download Microsoft Edge Canary from the [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) page.</span></span>

### <span data-ttu-id="ba9b6-116">Возможности режима терминала</span><span class="sxs-lookup"><span data-stu-id="ba9b6-116">Kiosk mode features</span></span>

<span data-ttu-id="ba9b6-117">Доступны следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-117">The following features are available:</span></span>

- <span data-ttu-id="ba9b6-118">Навигация в InPrivate защищает пользовательские данные путем удаления данных и загрузок браузера после завершении сеанса.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-118">InPrivate navigation protects user data by deleting browser data and downloads when the session ends.</span></span>
- <span data-ttu-id="ba9b6-119">Политика для настройки функции удаления загрузок при выходе.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-119">A policy to configure Delete downloads on exit.</span></span>
- <span data-ttu-id="ba9b6-120">Параметр для сброса сеанса пользователя после определенного периода бездействия.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-120">The option to reset a user session after a certain period of inactivity.</span></span>
- <span data-ttu-id="ba9b6-121">Первоначальный набор функций блокировки.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-121">An initial set of lockdown functionality.</span></span> <span data-ttu-id="ba9b6-122">Доступны следующие функции:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-122">The following functions are available:</span></span>

  - <span data-ttu-id="ba9b6-123">Контекстное меню мыши</span><span class="sxs-lookup"><span data-stu-id="ba9b6-123">Mouse context menu</span></span>
  - <span data-ttu-id="ba9b6-124">Средства разработчика F12</span><span class="sxs-lookup"><span data-stu-id="ba9b6-124">F12 Developer Tools</span></span>
  - <span data-ttu-id="ba9b6-125">F11 Выход из полноэкранного режима (в полноэкранном режиме)</span><span class="sxs-lookup"><span data-stu-id="ba9b6-125">F11 Exit full screen (while in full screen mode)</span></span>
  - <span data-ttu-id="ba9b6-126">Блокировка первоначального набора страниц *Edge://*</span><span class="sxs-lookup"><span data-stu-id="ba9b6-126">Blocking of the initial set of *Edge://* pages</span></span>

> [!NOTE]
> <span data-ttu-id="ba9b6-127">По мере развития режима терминала будет появляться все больше функций.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-127">As kiosk mode evolves, more features will be available.</span></span>

## <span data-ttu-id="ba9b6-128">Использование возможностей режима терминала</span><span class="sxs-lookup"><span data-stu-id="ba9b6-128">Use kiosk mode features</span></span>

<span data-ttu-id="ba9b6-129">Функции режима терминала Microsoft Edge можно вызывать с помощью следующих параметров командной строки Windows 10:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-129">You can invoke Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="ba9b6-130">Цифровая или интерактивная вывеска режима терминала:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-130">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="ba9b6-131">Общедоступный просмотр режима терминала:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-131">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### <span data-ttu-id="ba9b6-132">Дополнительные параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="ba9b6-132">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="ba9b6-133">: Отключение первого запуска Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-133">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="ba9b6-134">: Изменение времени в минутах от последнего действия пользователя до того, как режим терминала Microsoft Edge сбросит сеанс пользователя.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-134">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="ba9b6-135">Поддерживаются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-135">The following values are supported:</span></span>

  - <span data-ttu-id="ba9b6-136">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ba9b6-136">Default values</span></span>
    - <span data-ttu-id="ba9b6-137">Полный экран — отключен</span><span class="sxs-lookup"><span data-stu-id="ba9b6-137">Full screen - turned off</span></span>
    - <span data-ttu-id="ba9b6-138">Общедоступный просмотр — 5 минут</span><span class="sxs-lookup"><span data-stu-id="ba9b6-138">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="ba9b6-139">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="ba9b6-139">Allowed values</span></span>
    - <span data-ttu-id="ba9b6-140">0 — отключение таймера</span><span class="sxs-lookup"><span data-stu-id="ba9b6-140">0 - turns off the timer</span></span>
    - <span data-ttu-id="ba9b6-141">1-1440 минут для сброса таймера в состоянии покоя</span><span class="sxs-lookup"><span data-stu-id="ba9b6-141">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="ba9b6-142">Microsoft Edge с ограниченным доступом</span><span class="sxs-lookup"><span data-stu-id="ba9b6-142">Microsoft Edge with assigned access</span></span>

### <span data-ttu-id="ba9b6-143">Режим терминала с одним приложением</span><span class="sxs-lookup"><span data-stu-id="ba9b6-143">Single app kiosk</span></span>

<span data-ttu-id="ba9b6-144">В настоящее время Microsoft Edge поддерживает набор таких же типов режимов терминала с ограниченным доступом для одного приложения, как и устаревшая версия Microsoft Edge, со следующими вариантами блокировки: цифровая или интерактивная вывеска и общедоступный просмотр.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-144">Microsoft Edge currently supports a subset of the same Microsoft Edge Legacy kiosk mode types for single-app assigned access with the following lockdown experiences, Digital/Interactive signage and Public-browsing.</span></span>  

<span data-ttu-id="ba9b6-145">Режим терминала с ограниченным доступом в настоящее время доступен для тестирования в последней  [сборке Windows 10 Insider Preview](https://insider.windows.com/) версии 20215 или выше, а также в  [канале Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download) версии 87.0.644.4 или выше.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-145">Kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 or higher.</span></span>

**<span data-ttu-id="ba9b6-146">Откуда загрузить Windows Insider Preview?</span><span class="sxs-lookup"><span data-stu-id="ba9b6-146">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="ba9b6-147">Чтобы установить сборку Windows 10 Insider Preview на компьютер с Windows, следуйте инструкциям, указанным в разделе  [Начало работы со сборками Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="ba9b6-147">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="ba9b6-148">Режим терминала с несколькими приложениями</span><span class="sxs-lookup"><span data-stu-id="ba9b6-148">Multi-app kiosk</span></span>

<span data-ttu-id="ba9b6-149">Microsoft Edge можно запустить с [ограниченным доступом для нескольких приложений](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) в Windows 10, что является эквивалентом типа режима терминала «Обычный просмотр веб-страниц» в устаревшей версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-149">Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type.</span></span> <span data-ttu-id="ba9b6-150">Чтобы настроить ограниченный доступ для нескольких приложений в Microsoft Edge, следуйте инструкциям по [настройке режима терминала с несколькими приложениями](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span><span class="sxs-lookup"><span data-stu-id="ba9b6-150">To configure Microsoft Edge with multi-app assigned access follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span></span> <span data-ttu-id="ba9b6-151">(AUMID для Microsoft Edge из канала Stable— **MSEdge**).</span><span class="sxs-lookup"><span data-stu-id="ba9b6-151">(The AUMID for the Microsoft Edge Stable channel is **MSEdge**).</span></span>

<span data-ttu-id="ba9b6-152">Настройка режима терминала в Microsoft Edge При использовании Microsoft Edge с ограниченным доступом для нескольких приложений можно использовать [политики браузера Microsoft Edge](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies), чтобы настроить браузер в соответствии с вашими уникальными требованиями.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-152">Configure Microsoft Edge kiosk mode When using Microsoft Edge with multi-app assigned access you can use the [Microsoft Edge browser policies](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies) to configure the browsing experience to meet your unique requirements.</span></span>

### <span data-ttu-id="ba9b6-153">Настройка с помощью параметров Windows</span><span class="sxs-lookup"><span data-stu-id="ba9b6-153">Configure using Windows Settings</span></span>

<span data-ttu-id="ba9b6-154">Параметры Windows — это самый простой способ настроить одно или два устройства с одним приложением в режиме терминала.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-154">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="ba9b6-155">Для настройки компьютера с одним приложением в режиме терминала выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-155">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="ba9b6-156">Установите последний выпуск Windows 10 Insider Preview версии 20215 или выше.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-156">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="ba9b6-157">Следуйте инструкциям, указанным в разделе [Начало работы со сборками Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="ba9b6-157">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="ba9b6-158">Установите последнюю версию [канала Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download), 87.0.644.4 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-158">Install the latest version of [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), 87.0.644.4 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="ba9b6-159">Поскольку требуется установка на уровне устройства, поддерживается только канал, не связанный с Canary.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-159">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="ba9b6-160">На компьютере терминала откройте параметры Windows и в поле поиска введите слово «терминал».</span><span class="sxs-lookup"><span data-stu-id="ba9b6-160">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="ba9b6-161">Чтобы открыть диалоговое окно для создания терминала, выберите  **Настройка терминала (ограниченный доступ)**, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-161">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Настройка терминала с ограниченным доступом":::

4. <span data-ttu-id="ba9b6-163">На странице **Настройка киоска** нажмите **Начать**.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-163">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Настройка терминала с ограниченным доступом":::

5. <span data-ttu-id="ba9b6-165">Введите имя для создания новой учетной записи в терминале или выберите существующую учетную запись из раскрывающегося списка и нажмите  **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-165">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Настройка терминала с ограниченным доступом":::

6. <span data-ttu-id="ba9b6-167">На странице **Выбор приложения терминала**  выберите **Microsoft Edge** и нажмите кнопку  **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-167">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="ba9b6-168">Это относится только к каналам Microsoft Edge Dev, бета-версиям канала и стабильным каналам.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-168">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Настройка терминала с ограниченным доступом":::

7. <span data-ttu-id="ba9b6-170">Выберите один из следующих вариантов отображения Microsoft Edge при работе в режиме терминала:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-170">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="ba9b6-171">Цифровые или интерактивные вывески — Отображают конкретный сайт в полноэкранном режиме в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-171">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="ba9b6-172">Общедоступный браузер — Запускает ограниченную версию Microsoft Edge с несколькими вкладками.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-172">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Настройка терминала с ограниченным доступом":::

8. <span data-ttu-id="ba9b6-174">Нажмите  **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-174">Select **Next**.</span></span>
9. <span data-ttu-id="ba9b6-175">Введите URL-адрес для загрузки при запуске киоска.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-175">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Настройка терминала с ограниченным доступом":::

10. <span data-ttu-id="ba9b6-177">Примите значение по умолчанию (5 минут) для времени простоя или укажите свое значение.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-177">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Настройка терминала с ограниченным доступом":::

11. <span data-ttu-id="ba9b6-179">Нажмите  **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-179">Click **Next**.</span></span>
12. <span data-ttu-id="ba9b6-180">Закройте окно  **Параметры** , чтобы сохранить и применить свой выбор.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-180">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Настройка терминала с ограниченным доступом":::

13. <span data-ttu-id="ba9b6-182">Выйдите из устройства терминала и войдите в систему с локальной учетной записью терминала, чтобы проверить настройку.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-182">Sign off from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="ba9b6-183">Функциональные ограничения</span><span class="sxs-lookup"><span data-stu-id="ba9b6-183">Functional limitations</span></span>

<span data-ttu-id="ba9b6-184">С выпуском этой предварительной версии режима терминала мы продолжаем работать над улучшением продукта и добавлением новых функций.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-184">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="ba9b6-185">Хотя режим терминала в настоящее время не поддерживает следующие функции, ведется работа над следующими возможностями:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-185">Although kiosk mode doesn't currently support the following functionality, work is underway on the following features:</span></span>

- <span data-ttu-id="ba9b6-186">Коллекции</span><span class="sxs-lookup"><span data-stu-id="ba9b6-186">Collections</span></span>
- <span data-ttu-id="ba9b6-187">Расширения</span><span class="sxs-lookup"><span data-stu-id="ba9b6-187">Extensions</span></span>
- <span data-ttu-id="ba9b6-188">Режим Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="ba9b6-188">Internet Explorer mode</span></span>
- <span data-ttu-id="ba9b6-189">Application Guard в Защитнике Windows (WDAG)</span><span class="sxs-lookup"><span data-stu-id="ba9b6-189">Windows Defender Application Guard (WDAG)</span></span>

## <span data-ttu-id="ba9b6-190">Стратегия</span><span class="sxs-lookup"><span data-stu-id="ba9b6-190">Roadmap</span></span>

### <span data-ttu-id="ba9b6-191">Позже в этом году (2020)</span><span class="sxs-lookup"><span data-stu-id="ba9b6-191">Later this year (2020)</span></span>

<span data-ttu-id="ba9b6-192">Будут добавлены следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-192">We'll add the following features:</span></span>

- <span data-ttu-id="ba9b6-193">Кнопка завершения сеанса</span><span class="sxs-lookup"><span data-stu-id="ba9b6-193">End session button</span></span>
- <span data-ttu-id="ba9b6-194">Адресная строка только для чтения</span><span class="sxs-lookup"><span data-stu-id="ba9b6-194">Read only address bar</span></span>  
  - <span data-ttu-id="ba9b6-195">Настраивается с помощью групповой политики</span><span class="sxs-lookup"><span data-stu-id="ba9b6-195">Configurable with group policy</span></span>
  - <span data-ttu-id="ba9b6-196">Если этот параметр включен, пользователи не смогут редактировать адресную строку и переходить на другую страницу.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-196">When enabled, users will be prevented from editing the address bar and navigating to another page.</span></span>

- <span data-ttu-id="ba9b6-197">Дополнительные функции блокировки:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-197">More lockdown functions:</span></span>

  - <span data-ttu-id="ba9b6-198">Дополнительные ускорители будут заблокированы (например, CTRL + N).</span><span class="sxs-lookup"><span data-stu-id="ba9b6-198">Additional accelerators will be blocked (for example, CTRL+N)</span></span>
  - <span data-ttu-id="ba9b6-199">В меню параметров «…» будут включены только необходимые параметры (например, «Печать», «Справка», «Отзыв» и «Чтение вслух»).</span><span class="sxs-lookup"><span data-stu-id="ba9b6-199">The "…" settings menu will enable only required options (for example, Print, Help,  Feedback, and Read aloud)</span></span>
  - <span data-ttu-id="ba9b6-200">Блокировка дополнительных *edge://* страниц (например, *edge://settings*)</span><span class="sxs-lookup"><span data-stu-id="ba9b6-200">Additional *edge://* pages lockdown (for example, *edge://settings*)</span></span>
  - <span data-ttu-id="ba9b6-201">Настройка пользовательского интерфейса параметров печати</span><span class="sxs-lookup"><span data-stu-id="ba9b6-201">Configure print options UI</span></span>
  - <span data-ttu-id="ba9b6-202">Ограничение проводника только папкой загрузки.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-202">Limiting file explorer to the download folder only.</span></span>

### <span data-ttu-id="ba9b6-203">В начале 2021 года</span><span class="sxs-lookup"><span data-stu-id="ba9b6-203">In early 2021</span></span>

<span data-ttu-id="ba9b6-204">Будут добавлены следующая поддержка и возможности:</span><span class="sxs-lookup"><span data-stu-id="ba9b6-204">We'll add the following support and features:</span></span>

- <span data-ttu-id="ba9b6-205">Общая доступность режима терминала Microsoft Edge с одним приложением на Windows с ограниченным доступом.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-205">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows.</span></span>
- <span data-ttu-id="ba9b6-206">Дополнительные возможности для обеспечения равных условий с устаревшей версией Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-206">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="ba9b6-207">Интеграция с Intune для настройки устройств с использованием пользовательского интерфейса профиля режима терминала.</span><span class="sxs-lookup"><span data-stu-id="ba9b6-207">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>

## <span data-ttu-id="ba9b6-208">См. также</span><span class="sxs-lookup"><span data-stu-id="ba9b6-208">See also</span></span>

- [<span data-ttu-id="ba9b6-209">Настройка терминалов и цифровых вывесок в выпусках Windows для настольных компьютеров</span><span class="sxs-lookup"><span data-stu-id="ba9b6-209">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="ba9b6-210">Развертывание режима терминала в Microsoft Edge Legacy</span><span class="sxs-lookup"><span data-stu-id="ba9b6-210">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode)
- [<span data-ttu-id="ba9b6-211">Планирование развертывания Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ba9b6-211">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="ba9b6-212">Использование целевой страницы Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="ba9b6-212">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
