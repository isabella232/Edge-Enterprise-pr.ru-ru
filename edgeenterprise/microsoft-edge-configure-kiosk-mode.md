---
title: Настройка режима терминала в Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 09/22/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Настройка режима терминала в Microsoft Edge
ms.openlocfilehash: d7c9df82079f8343d43ccfd312623e6e01358fa9
ms.sourcegitcommit: 858227653fc89532d1d274735f53280e27b2a8c0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/22/2020
ms.locfileid: "11072718"
---
# <span data-ttu-id="fd54c-103">Настройка режима терминала в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fd54c-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="fd54c-104">В этой статье рассказывается, как настроить параметры режим терминала в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fd54c-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="fd54c-105">Кроме того, вы можете воспользоваться схемой функций, которые мы настраиваем.</span><span class="sxs-lookup"><span data-stu-id="fd54c-105">There's also a roadmap of features we are targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="fd54c-106">Эта статья относится к Microsoft Edge версии 87 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="fd54c-106">This article applies to Microsoft Edge version 87 or later.</span></span>

<span data-ttu-id="fd54c-107">Сведения о режиме терминала в Microsoft Edge Legacy (версии 45 или более ранней версии) см. в разделе [Развертывание режима терминала в Microsoft Edge](https://aka.ms/edgekioskmode).</span><span class="sxs-lookup"><span data-stu-id="fd54c-107">For information about Microsoft Edge Legacy kiosk mode (version 45 and earlier) see [Deploy Microsoft Edge kiosk mode](https://aka.ms/edgekioskmode).</span></span>

## <span data-ttu-id="fd54c-108">Обзор</span><span class="sxs-lookup"><span data-stu-id="fd54c-108">Overview</span></span>

<span data-ttu-id="fd54c-109">Режим терминала Microsoft Edge предлагает два варианта блокировки браузера, чтобы организации могли создавать, управлять и обеспечивать наилучшие условия для своих клиентов.</span><span class="sxs-lookup"><span data-stu-id="fd54c-109">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="fd54c-110">Доступны следующие варианты блокировки:</span><span class="sxs-lookup"><span data-stu-id="fd54c-110">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="fd54c-111">Цифровые или интерактивные вывески отображают конкретный сайт в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="fd54c-111">The Digital/Interactive signage experience displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="fd54c-112">В общедоступном браузере работает ограниченная версия Microsoft Edge с несколькими вкладками.</span><span class="sxs-lookup"><span data-stu-id="fd54c-112">The public-browsing experience runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="fd54c-113">В обоих случаях выполняется сеанс Microsoft Edge InPrivate, который защищает пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="fd54c-113">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="fd54c-114">Настройка режима терминала в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fd54c-114">Set up Microsoft Edge kiosk mode</span></span>  

<span data-ttu-id="fd54c-115">Начальный набор функций режима терминала теперь доступен для тестирования на канале Microsoft Edge Canary, версия 87.</span><span class="sxs-lookup"><span data-stu-id="fd54c-115">An initial set of kiosk mode features are now available to test with Microsoft Edge Canary Channel, version 87.</span></span> <span data-ttu-id="fd54c-116">Вы можете скачать Microsoft Edge Canary со страницы [каналов предварительной оценки Microsoft Edge](https://www.microsoftedgeinsider.com/download).</span><span class="sxs-lookup"><span data-stu-id="fd54c-116">You can download Microsoft Edge Canary from the [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) page.</span></span>

### <span data-ttu-id="fd54c-117">Возможности режима терминала</span><span class="sxs-lookup"><span data-stu-id="fd54c-117">Kiosk mode features</span></span>

<span data-ttu-id="fd54c-118">Доступны следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="fd54c-118">The following features are available:</span></span>

- <span data-ttu-id="fd54c-119">Навигация в InPrivate.</span><span class="sxs-lookup"><span data-stu-id="fd54c-119">InPrivate navigation.</span></span> <span data-ttu-id="fd54c-120">Защита пользовательских данных путем удаления данных браузера и их загрузки после завершении сеанса.</span><span class="sxs-lookup"><span data-stu-id="fd54c-120">Protects user data by deleting browser data and downloads when the session ends.</span></span>
- <span data-ttu-id="fd54c-121">Политика для настройки функции удаления загрузки при выходе.</span><span class="sxs-lookup"><span data-stu-id="fd54c-121">Policy to configure Delete downloads on exit.</span></span>
- <span data-ttu-id="fd54c-122">Сброс сеанса пользователя после определенного периода бездействия.</span><span class="sxs-lookup"><span data-stu-id="fd54c-122">Reset user session after a certain period of inactivity.</span></span>
- <span data-ttu-id="fd54c-123">Первоначальный набор функций блокировки.</span><span class="sxs-lookup"><span data-stu-id="fd54c-123">Initial set of lockdown functionality.</span></span> <span data-ttu-id="fd54c-124">Доступны следующие функции:</span><span class="sxs-lookup"><span data-stu-id="fd54c-124">The following functions are available:</span></span>

  - <span data-ttu-id="fd54c-125">Контекстное меню мыши</span><span class="sxs-lookup"><span data-stu-id="fd54c-125">Mouse context menu</span></span>
  - <span data-ttu-id="fd54c-126">Средства разработчика F12</span><span class="sxs-lookup"><span data-stu-id="fd54c-126">F12 Developer Tools</span></span>
  - <span data-ttu-id="fd54c-127">F11 Выход из полноэкранного режима (в полноэкранном режиме)</span><span class="sxs-lookup"><span data-stu-id="fd54c-127">F11 Exit full screen (while in full screen mode)</span></span>
  - <span data-ttu-id="fd54c-128">Блокировка первоначального набора страниц *Edge://*</span><span class="sxs-lookup"><span data-stu-id="fd54c-128">Blocking of the initial set of *Edge://* pages</span></span>

> [!NOTE]
> <span data-ttu-id="fd54c-129">По мере развития режима терминала будет появляться все больше функций.</span><span class="sxs-lookup"><span data-stu-id="fd54c-129">As kiosk mode evolves, more features will be available.</span></span>

### <span data-ttu-id="fd54c-130">Использование возможностей режима терминала</span><span class="sxs-lookup"><span data-stu-id="fd54c-130">Use kiosk mode features</span></span>

<span data-ttu-id="fd54c-131">Функции режима терминала Microsoft Edge можно вызывать с помощью следующих параметров командной строки Windows 10:</span><span class="sxs-lookup"><span data-stu-id="fd54c-131">You can invoke Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="fd54c-132">Цифровая или интерактивная вывеска режима терминала:</span><span class="sxs-lookup"><span data-stu-id="fd54c-132">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="fd54c-133">Общедоступный просмотр режима терминала:</span><span class="sxs-lookup"><span data-stu-id="fd54c-133">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

#### <span data-ttu-id="fd54c-134">Дополнительные параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="fd54c-134">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="fd54c-135">: Отключение первого запуска Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fd54c-135">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="fd54c-136">: Изменение времени в минутах от последнего действия пользователя до того, как режим терминала Microsoft Edge сбросит сеанс пользователя.</span><span class="sxs-lookup"><span data-stu-id="fd54c-136">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="fd54c-137">Поддерживаются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fd54c-137">The following values are supported:</span></span>

  - <span data-ttu-id="fd54c-138">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fd54c-138">Default values</span></span>
    - <span data-ttu-id="fd54c-139">Полный экран — отключен</span><span class="sxs-lookup"><span data-stu-id="fd54c-139">Full screen - turned off</span></span>
    - <span data-ttu-id="fd54c-140">Общедоступный просмотр — 5 минут</span><span class="sxs-lookup"><span data-stu-id="fd54c-140">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="fd54c-141">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="fd54c-141">Allowed values</span></span>
    - <span data-ttu-id="fd54c-142">0 — отключение таймера</span><span class="sxs-lookup"><span data-stu-id="fd54c-142">0 - turns off the timer</span></span>
    - <span data-ttu-id="fd54c-143">1-1440 минут для сброса таймера в состоянии покоя</span><span class="sxs-lookup"><span data-stu-id="fd54c-143">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="fd54c-144">Настройка режима терминала с ограниченным доступом</span><span class="sxs-lookup"><span data-stu-id="fd54c-144">Set up kiosk mode with assigned access</span></span>

<span data-ttu-id="fd54c-145">Режим терминала Microsoft Edge с ограниченным доступом в настоящее время доступен для тестирования в последней [сборке Windows 10 Insider Preview](https://insider.windows.com/) версии 20215 или выше, а также в [канале Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download) версии 87.0.644 или выше.</span><span class="sxs-lookup"><span data-stu-id="fd54c-145">Microsoft Edge kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644 or higher.</span></span>

**<span data-ttu-id="fd54c-146">Откуда загрузить Windows Insider Preview?</span><span class="sxs-lookup"><span data-stu-id="fd54c-146">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="fd54c-147">Чтобы установить сборку Windows 10 Insider Preview на компьютер с Windows, следуйте инструкциям, указанным в разделе [Начало работы со сборками Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="fd54c-147">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="fd54c-148">Настройка с помощью параметров Windows</span><span class="sxs-lookup"><span data-stu-id="fd54c-148">Configure using Windows Settings</span></span>

<span data-ttu-id="fd54c-149">Параметры Windows — это самый простой способ настроить одно или два устройства с одним приложением в режиме терминала.</span><span class="sxs-lookup"><span data-stu-id="fd54c-149">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="fd54c-150">Для настройки компьютера с одним приложением в режиме терминала выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="fd54c-150">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="fd54c-151">Установите последний выпуск Windows 10 Insider Preview версии 20215 или выше.</span><span class="sxs-lookup"><span data-stu-id="fd54c-151">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="fd54c-152">Следуйте инструкциям, указанным в разделе [Начало работы со сборками Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="fd54c-152">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="fd54c-153">Установите последнюю версию [канала разработки Microsoft Edge](https://www.microsoftedgeinsider.com/download), 87.0.644 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="fd54c-153">Install the latest version of [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), 87.0.644 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="fd54c-154">Поскольку требуется установка на уровне устройства, поддерживается только канал, не связанный с Canary.</span><span class="sxs-lookup"><span data-stu-id="fd54c-154">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="fd54c-155">На компьютере терминала откройте параметры Windows и в поле поиска введите слово «терминал».</span><span class="sxs-lookup"><span data-stu-id="fd54c-155">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="fd54c-156">Чтобы открыть диалоговое окно для создания терминала, выберите  **Настройка терминала (ограниченный доступ)**, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="fd54c-156">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Настройка терминала с ограниченным доступом":::

4. <span data-ttu-id="fd54c-158">На странице **Настройка киоска** нажмите **Начать**.</span><span class="sxs-lookup"><span data-stu-id="fd54c-158">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Страница терминала — начать":::

5. <span data-ttu-id="fd54c-160">Введите имя для создания новой учетной записи в терминале или выберите существующую учетную запись из раскрывающегося списка и нажмите  **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fd54c-160">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Режим терминала — создание учетной записи":::

6. <span data-ttu-id="fd54c-162">На странице **Выбор приложения терминала**  выберите **Microsoft Edge** и нажмите кнопку  **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fd54c-162">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="fd54c-163">Это относится только к каналам Microsoft Edge Dev, бета-версиям канала и стабильным каналам.</span><span class="sxs-lookup"><span data-stu-id="fd54c-163">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Режим терминала — выбор приложения":::

7. <span data-ttu-id="fd54c-165">Выберите один из следующих вариантов отображения Microsoft Edge при работе в режиме терминала:</span><span class="sxs-lookup"><span data-stu-id="fd54c-165">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="fd54c-166">Цифровые или интерактивные вывески — Отображают конкретный сайт в полноэкранном режиме в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fd54c-166">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="fd54c-167">Общедоступный браузер — Запускает ограниченную версию Microsoft Edge с несколькими вкладками.</span><span class="sxs-lookup"><span data-stu-id="fd54c-167">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Экран режима терминала — цифровой указатель полного экрана":::

8. <span data-ttu-id="fd54c-169">Нажмите  **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fd54c-169">Select **Next**.</span></span>
9. <span data-ttu-id="fd54c-170">Введите URL-адрес для загрузки при запуске киоска.</span><span class="sxs-lookup"><span data-stu-id="fd54c-170">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Режим терминала — введите URL-адрес":::

10. <span data-ttu-id="fd54c-172">Примите значение по умолчанию (5 минут) для времени простоя или укажите свое значение.</span><span class="sxs-lookup"><span data-stu-id="fd54c-172">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Режим терминала — введите время простоя":::

11. <span data-ttu-id="fd54c-174">Нажмите  **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fd54c-174">Click **Next**.</span></span>
12. <span data-ttu-id="fd54c-175">Закройте окно  **Параметры** , чтобы сохранить и применить свой выбор.</span><span class="sxs-lookup"><span data-stu-id="fd54c-175">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Режим терминала — завершение настройки":::

13. <span data-ttu-id="fd54c-177">Выйдите из устройства терминала и войдите в систему с локальной учетной записью терминала, чтобы проверить настройку.</span><span class="sxs-lookup"><span data-stu-id="fd54c-177">Sign off from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="fd54c-178">Функциональные ограничения</span><span class="sxs-lookup"><span data-stu-id="fd54c-178">Functional limitations</span></span>

<span data-ttu-id="fd54c-179">С выпуском этой предварительной версии режима терминала мы продолжаем работать над улучшением продукта и добавлением новых функций.</span><span class="sxs-lookup"><span data-stu-id="fd54c-179">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="fd54c-180">Хотя режим терминала в настоящее время не поддерживает следующие функции, ведется работа над следующими возможностями:</span><span class="sxs-lookup"><span data-stu-id="fd54c-180">Although kiosk mode doesn't currently support the following functionality, work is underway on the following features:</span></span>

- <span data-ttu-id="fd54c-181">Коллекции</span><span class="sxs-lookup"><span data-stu-id="fd54c-181">Collections</span></span>
- <span data-ttu-id="fd54c-182">Расширения</span><span class="sxs-lookup"><span data-stu-id="fd54c-182">Extensions</span></span>
- <span data-ttu-id="fd54c-183">Режим Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="fd54c-183">Internet Explorer mode</span></span>
- <span data-ttu-id="fd54c-184">Application Guard в Защитнике Windows (WDAG)</span><span class="sxs-lookup"><span data-stu-id="fd54c-184">Windows Defender Application Guard (WDAG)</span></span>

## <span data-ttu-id="fd54c-185">Стратегия</span><span class="sxs-lookup"><span data-stu-id="fd54c-185">Roadmap</span></span>

### <span data-ttu-id="fd54c-186">Позже в этом году (2020)</span><span class="sxs-lookup"><span data-stu-id="fd54c-186">Later this year (2020)</span></span>

<span data-ttu-id="fd54c-187">Будут добавлены следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="fd54c-187">We'll add the following features:</span></span>

- <span data-ttu-id="fd54c-188">Кнопка завершения сеанса</span><span class="sxs-lookup"><span data-stu-id="fd54c-188">End session button</span></span>
- <span data-ttu-id="fd54c-189">URL-адреса адресной строки только для чтения</span><span class="sxs-lookup"><span data-stu-id="fd54c-189">Read only URL address bar</span></span>  
  - <span data-ttu-id="fd54c-190">Настраивается с помощью групповой политики</span><span class="sxs-lookup"><span data-stu-id="fd54c-190">Configurable with group policy</span></span>
  - <span data-ttu-id="fd54c-191">Если этот параметр включен, пользователи не смогут редактировать URL-адрес адресной строки, чтобы попытаться перейти на другую страницу.</span><span class="sxs-lookup"><span data-stu-id="fd54c-191">When enabled, users will be prevented from editing the address bar URL to try navigating away to another page.</span></span>

- <span data-ttu-id="fd54c-192">Дополнительные функции блокировки:</span><span class="sxs-lookup"><span data-stu-id="fd54c-192">More lockdown functions:</span></span>

  - <span data-ttu-id="fd54c-193">Дополнительные ускорители будут заблокированы (например, CTRL + N).</span><span class="sxs-lookup"><span data-stu-id="fd54c-193">Additional accelerators will be blocked (for example, CTRL+N)</span></span>
  - <span data-ttu-id="fd54c-194">В меню параметров «…» будут включены только необходимые параметры (например, «Печать», «Справка», «Отзыв» и «Чтение вслух»).</span><span class="sxs-lookup"><span data-stu-id="fd54c-194">The "…" settings menu will enable only required options (for example, Print, Help,  Feedback, and Read aloud)</span></span>
  - <span data-ttu-id="fd54c-195">Блокировка дополнительных *edge://* страниц (например, *edge://settings*)</span><span class="sxs-lookup"><span data-stu-id="fd54c-195">Additional *edge://* pages lockdown (for example, *edge://settings*)</span></span>
  - <span data-ttu-id="fd54c-196">Настройка пользовательского интерфейса параметров печати</span><span class="sxs-lookup"><span data-stu-id="fd54c-196">Configure print options UI</span></span>
  - <span data-ttu-id="fd54c-197">Ограничение проводника только папкой загрузки.</span><span class="sxs-lookup"><span data-stu-id="fd54c-197">Limiting file explorer to the download folder only.</span></span>

### <span data-ttu-id="fd54c-198">В начале 2021 года</span><span class="sxs-lookup"><span data-stu-id="fd54c-198">In early 2021</span></span>

<span data-ttu-id="fd54c-199">Будут добавлены следующая поддержка и возможности:</span><span class="sxs-lookup"><span data-stu-id="fd54c-199">We'll add the following support and features:</span></span>

- <span data-ttu-id="fd54c-200">Общая доступность режима терминала Microsoft Edge с одним приложением на Windows с ограниченным доступом.</span><span class="sxs-lookup"><span data-stu-id="fd54c-200">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows.</span></span>
- <span data-ttu-id="fd54c-201">Дополнительные возможности для обеспечения равных условий с устаревшей версией Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fd54c-201">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="fd54c-202">Интеграция с Intune для настройки устройств с использованием пользовательского интерфейса профиля режима терминала.</span><span class="sxs-lookup"><span data-stu-id="fd54c-202">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>

## <span data-ttu-id="fd54c-203">См. также</span><span class="sxs-lookup"><span data-stu-id="fd54c-203">See also</span></span>

- [<span data-ttu-id="fd54c-204">Настройка терминалов и цифровых вывесок в выпусках Windows для настольных компьютеров</span><span class="sxs-lookup"><span data-stu-id="fd54c-204">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="fd54c-205">Развертывание режима терминала в Microsoft Edge Legacy</span><span class="sxs-lookup"><span data-stu-id="fd54c-205">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode) 
- [<span data-ttu-id="fd54c-206">Планирование развертывания Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fd54c-206">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="fd54c-207">Использование целевой страницы Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="fd54c-207">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)