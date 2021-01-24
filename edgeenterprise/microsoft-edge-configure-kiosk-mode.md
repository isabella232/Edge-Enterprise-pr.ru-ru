---
title: Настройка режима терминала в Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 01/21/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Настройка режима терминала в Microsoft Edge
ms.openlocfilehash: be353a0e13e9234de40296a2e8dcc31b1b800f52
ms.sourcegitcommit: 8a88fd38bdb5e132e89bf17dd2b5fb72f5d1b4b9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297475"
---
# <span data-ttu-id="9a747-103">Настройка режима терминала в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9a747-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="9a747-104">В этой статье рассказывается, как настроить параметры режим терминала в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a747-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="9a747-105">Кроме того, представлена дорожная карта реализации функций, над которыми мы работаем.</span><span class="sxs-lookup"><span data-stu-id="9a747-105">There's also a roadmap of features we're targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="9a747-106">Эта статья относится к Microsoft Edge версии 87 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="9a747-106">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="9a747-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="9a747-107">Overview</span></span>

<span data-ttu-id="9a747-108">Режим терминала Microsoft Edge предлагает два варианта блокировки браузера, чтобы организации могли создавать, управлять и обеспечивать наилучшие условия для своих клиентов.</span><span class="sxs-lookup"><span data-stu-id="9a747-108">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="9a747-109">Доступны следующие варианты блокировки:</span><span class="sxs-lookup"><span data-stu-id="9a747-109">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="9a747-110">**Цифровые или интерактивные вывески** отображают конкретный сайт в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="9a747-110">**Digital/Interactive Signage** experience - Displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="9a747-111">**Общедоступный просмотр** запускает ограниченную версию Microsoft Edge с несколькими вкладками.</span><span class="sxs-lookup"><span data-stu-id="9a747-111">**Public-Browsing** experience - Runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="9a747-112">В обоих случаях выполняется сеанс Microsoft Edge InPrivate, который защищает пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="9a747-112">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="9a747-113">Настройка режима терминала в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9a747-113">Set up Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="9a747-114">Начальный набор функций режима терминала доступен для тестирования в стабильном канале Microsoft Edge, версия 87.</span><span class="sxs-lookup"><span data-stu-id="9a747-114">An initial set of kiosk mode features is available to test with Microsoft Edge Stable Channel, version 87.</span></span> <span data-ttu-id="9a747-115">Последнюю версию можно скачать из [Microsoft Edge (официальный стабильный канал).](https://www.microsoft.com/edge)</span><span class="sxs-lookup"><span data-stu-id="9a747-115">You can download the latest version from [Microsoft Edge (Official Stable Channel)](https://www.microsoft.com/edge).</span></span>

### <span data-ttu-id="9a747-116">Поддерживаемые функции режима терминала</span><span class="sxs-lookup"><span data-stu-id="9a747-116">Kiosk mode supported features</span></span>

<span data-ttu-id="9a747-117">В следующей таблице перечислены функции, поддерживаемые режимом терминала.</span><span class="sxs-lookup"><span data-stu-id="9a747-117">The following table lists the features supported by kiosk mode.</span></span>

|<span data-ttu-id="9a747-118">Функция</span><span class="sxs-lookup"><span data-stu-id="9a747-118">Feature</span></span>|<span data-ttu-id="9a747-119">Цифровая/интерактивная вывеска</span><span class="sxs-lookup"><span data-stu-id="9a747-119">Digital\Interactive Signage</span></span>|<span data-ttu-id="9a747-120">Общедоступный просмотр</span><span class="sxs-lookup"><span data-stu-id="9a747-120">Public browsing</span></span>|<span data-ttu-id="9a747-121">Доступно в Microsoft Edge версии (и выше)</span><span class="sxs-lookup"><span data-stu-id="9a747-121">Available with Microsoft Edge version (and higher)</span></span>|
|-|-|-|-|
|<span data-ttu-id="9a747-122">Навигация в InPrivate</span><span class="sxs-lookup"><span data-stu-id="9a747-122">InPrivate Navigation</span></span>|<span data-ttu-id="9a747-123">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-123">Y</span></span>|<span data-ttu-id="9a747-124">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-124">Y</span></span>|<span data-ttu-id="9a747-125">87</span><span class="sxs-lookup"><span data-stu-id="9a747-125">87</span></span>|
|<span data-ttu-id="9a747-126">Сброс при неактивности</span><span class="sxs-lookup"><span data-stu-id="9a747-126">Reset on inactivity</span></span>|<span data-ttu-id="9a747-127">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-127">Y</span></span>|<span data-ttu-id="9a747-128">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-128">Y</span></span>|<span data-ttu-id="9a747-129">87</span><span class="sxs-lookup"><span data-stu-id="9a747-129">87</span></span>|
|<span data-ttu-id="9a747-130">[Адресная строка только для чтения](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (политика)</span><span class="sxs-lookup"><span data-stu-id="9a747-130">[Read only address bar](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (policy)</span></span> |<span data-ttu-id="9a747-131">N</span><span class="sxs-lookup"><span data-stu-id="9a747-131">N</span></span>|<span data-ttu-id="9a747-132">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-132">Y</span></span> |<span data-ttu-id="9a747-133">87</span><span class="sxs-lookup"><span data-stu-id="9a747-133">87</span></span>|
|<span data-ttu-id="9a747-134">[Удаление загружаемых данных при выходе](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (политика)</span><span class="sxs-lookup"><span data-stu-id="9a747-134">[Delete downloads on exit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (policy)</span></span>  | <span data-ttu-id="9a747-135">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-135">Y</span></span>|<span data-ttu-id="9a747-136">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-136">Y</span></span> |<span data-ttu-id="9a747-137">87</span><span class="sxs-lookup"><span data-stu-id="9a747-137">87</span></span>|
|<span data-ttu-id="9a747-138">Блокировка F11 (вход и выход из полноэкранного режима)</span><span class="sxs-lookup"><span data-stu-id="9a747-138">F11 blocked (enter/exit full-screen)</span></span> | <span data-ttu-id="9a747-139">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-139">Y</span></span> | <span data-ttu-id="9a747-140">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-140">Y</span></span> | <span data-ttu-id="9a747-141">87</span><span class="sxs-lookup"><span data-stu-id="9a747-141">87</span></span> |
|<span data-ttu-id="9a747-142">Блокировка F12 (запуск средств разработчика)</span><span class="sxs-lookup"><span data-stu-id="9a747-142">F12 blocked (launch Developer Tools)</span></span> | <span data-ttu-id="9a747-143">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-143">Y</span></span> | <span data-ttu-id="9a747-144">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-144">Y</span></span> | <span data-ttu-id="9a747-145">87</span><span class="sxs-lookup"><span data-stu-id="9a747-145">87</span></span> |
| <span data-ttu-id="9a747-146">Поддержка нескольких вкладок</span><span class="sxs-lookup"><span data-stu-id="9a747-146">Multi tab support</span></span> | <span data-ttu-id="9a747-147">N</span><span class="sxs-lookup"><span data-stu-id="9a747-147">N</span></span>| <span data-ttu-id="9a747-148">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-148">Y</span></span>| <span data-ttu-id="9a747-149">87</span><span class="sxs-lookup"><span data-stu-id="9a747-149">87</span></span>|
|<span data-ttu-id="9a747-150">Кнопка завершения сеанса</span><span class="sxs-lookup"><span data-stu-id="9a747-150">End session button</span></span> | <span data-ttu-id="9a747-151">N</span><span class="sxs-lookup"><span data-stu-id="9a747-151">N</span></span>| <span data-ttu-id="9a747-152">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-152">Y</span></span>| <span data-ttu-id="9a747-153">88</span><span class="sxs-lookup"><span data-stu-id="9a747-153">88</span></span>|
|<span data-ttu-id="9a747-154">Все внутренние URL-адреса Microsoft Edge блокируются, кроме *edge://downloads* и *edge://print*</span><span class="sxs-lookup"><span data-stu-id="9a747-154">All internal Microsoft Edge URLs are blocked, except for *edge://downloads* and *edge://print*</span></span> |<span data-ttu-id="9a747-155">N</span><span class="sxs-lookup"><span data-stu-id="9a747-155">N</span></span>|<span data-ttu-id="9a747-156">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-156">Y</span></span>|<span data-ttu-id="9a747-157">88</span><span class="sxs-lookup"><span data-stu-id="9a747-157">88</span></span>|
| <span data-ttu-id="9a747-158">Блокировка CTRL+N (открытие нового окна)</span><span class="sxs-lookup"><span data-stu-id="9a747-158">CTRL+N blocked (open a new window)</span></span> | <span data-ttu-id="9a747-159">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-159">Y</span></span> | <span data-ttu-id="9a747-160">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-160">Y</span></span> | <span data-ttu-id="9a747-161">89</span><span class="sxs-lookup"><span data-stu-id="9a747-161">89</span></span> |
| <span data-ttu-id="9a747-162">Блокировка CTRL+T (открытие новой вкладки)</span><span class="sxs-lookup"><span data-stu-id="9a747-162">CTRL+T blocked (open new tab)</span></span> | <span data-ttu-id="9a747-163">N</span><span class="sxs-lookup"><span data-stu-id="9a747-163">N</span></span> | <span data-ttu-id="9a747-164">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-164">Y</span></span> | <span data-ttu-id="9a747-165">89</span><span class="sxs-lookup"><span data-stu-id="9a747-165">89</span></span> |
|<span data-ttu-id="9a747-166">Параметры и другое (...)— отображение только обязательных параметров</span><span class="sxs-lookup"><span data-stu-id="9a747-166">Settings and more (...) will display only the required options</span></span>  |<span data-ttu-id="9a747-167">N</span><span class="sxs-lookup"><span data-stu-id="9a747-167">N</span></span> |<span data-ttu-id="9a747-168">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-168">Y</span></span> |<span data-ttu-id="9a747-169">89</span><span class="sxs-lookup"><span data-stu-id="9a747-169">89</span></span> |

> [!NOTE]
> <span data-ttu-id="9a747-170">По мере развития режима терминала будет появляться все больше функций.</span><span class="sxs-lookup"><span data-stu-id="9a747-170">As kiosk mode evolves, more features will be available.</span></span>

## <span data-ttu-id="9a747-171">Использование возможностей режима терминала</span><span class="sxs-lookup"><span data-stu-id="9a747-171">Use kiosk mode features</span></span>

<span data-ttu-id="9a747-172">Функции режима терминала Microsoft Edge можно вызывать с помощью следующих параметров командной строки Windows 10:</span><span class="sxs-lookup"><span data-stu-id="9a747-172">Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="9a747-173">Цифровая или интерактивная вывеска режима терминала:</span><span class="sxs-lookup"><span data-stu-id="9a747-173">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="9a747-174">Общедоступный просмотр режима терминала:</span><span class="sxs-lookup"><span data-stu-id="9a747-174">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### <span data-ttu-id="9a747-175">Дополнительные параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="9a747-175">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="9a747-176">: Отключение первого запуска Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a747-176">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="9a747-177">: Изменение времени в минутах от последнего действия пользователя до того, как режим терминала Microsoft Edge сбросит сеанс пользователя.</span><span class="sxs-lookup"><span data-stu-id="9a747-177">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="9a747-178">Поддерживаются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9a747-178">The following values are supported:</span></span>

  - <span data-ttu-id="9a747-179">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9a747-179">Default values</span></span>
    - <span data-ttu-id="9a747-180">Полный экран — отключен</span><span class="sxs-lookup"><span data-stu-id="9a747-180">Full screen - turned off</span></span>
    - <span data-ttu-id="9a747-181">Общедоступный просмотр — 5 минут</span><span class="sxs-lookup"><span data-stu-id="9a747-181">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="9a747-182">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="9a747-182">Allowed values</span></span>
    - <span data-ttu-id="9a747-183">0 — отключение таймера</span><span class="sxs-lookup"><span data-stu-id="9a747-183">0 - turns off the timer</span></span>
    - <span data-ttu-id="9a747-184">1-1440 минут для сброса таймера простоя</span><span class="sxs-lookup"><span data-stu-id="9a747-184">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="9a747-185">Поддерживаемые политики режима терминала</span><span class="sxs-lookup"><span data-stu-id="9a747-185">Support policies for kiosk mode</span></span>

<span data-ttu-id="9a747-186">Используйте любую из политик Microsoft Edge, перечисленных в следующей таблице, чтобы улучшить работу терминала для настроенного вами типа режима терминала Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a747-186">Use any of the Microsoft Edge policies listed in the following table to enhance the kiosk experience for the Microsoft Edge kiosk mode type you configure.</span></span> <span data-ttu-id="9a747-187">Дополнительные информацию об этих политиках см. в [справочнике по политикам браузера Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-policies).</span><span class="sxs-lookup"><span data-stu-id="9a747-187">To learn more about these policies, see [Microsoft Edge – Browser policy reference](https://docs.microsoft.com/deployedge/microsoft-edge-policies).</span></span>

> [!NOTE]
> <span data-ttu-id="9a747-188">Конфигурация политик не ограничивается политиками, перечисленными в следующей таблице, однако другие политики следует проверить и убедиться, что они не оказывают негативного влияния на функциональность режима терминала.</span><span class="sxs-lookup"><span data-stu-id="9a747-188">Policy configuration isn't limited to the policies listed in the following table, however additional policies should be tested to ensure that kiosk mode functionality isn't negatively affected.</span></span>

|<span data-ttu-id="9a747-189">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="9a747-189">Group policy</span></span>|<span data-ttu-id="9a747-190">Цифровая/интерактивная вывеска</span><span class="sxs-lookup"><span data-stu-id="9a747-190">Digital\Interactive signage</span></span>|<span data-ttu-id="9a747-191">Одно приложение для общего просмотра</span><span class="sxs-lookup"><span data-stu-id="9a747-191">Public browsing single-app</span></span>|
|--|--|--|
|[<span data-ttu-id="9a747-192">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="9a747-192">Printing</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printing-policies) | <span data-ttu-id="9a747-193">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-193">Y</span></span>|<span data-ttu-id="9a747-194">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-194">Y</span></span> |
|[<span data-ttu-id="9a747-195">HomePageLocation</span><span class="sxs-lookup"><span data-stu-id="9a747-195">HomePageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation) |<span data-ttu-id="9a747-196">N</span><span class="sxs-lookup"><span data-stu-id="9a747-196">N</span></span> | <span data-ttu-id="9a747-197">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-197">Y</span></span>|
|[<span data-ttu-id="9a747-198">ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="9a747-198">ShowHomeButton</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton) |<span data-ttu-id="9a747-199">N</span><span class="sxs-lookup"><span data-stu-id="9a747-199">N</span></span> | <span data-ttu-id="9a747-200">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-200">Y</span></span>|
|[<span data-ttu-id="9a747-201">NewTabPageLocation</span><span class="sxs-lookup"><span data-stu-id="9a747-201">NewTabPageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) |<span data-ttu-id="9a747-202">N</span><span class="sxs-lookup"><span data-stu-id="9a747-202">N</span></span> |<span data-ttu-id="9a747-203">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-203">Y</span></span> |
|[<span data-ttu-id="9a747-204">FavoritesBarEnabled</span><span class="sxs-lookup"><span data-stu-id="9a747-204">FavoritesBarEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled) |<span data-ttu-id="9a747-205">N</span><span class="sxs-lookup"><span data-stu-id="9a747-205">N</span></span> |<span data-ttu-id="9a747-206">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-206">Y</span></span> |
|[<span data-ttu-id="9a747-207">URLAllowlist</span><span class="sxs-lookup"><span data-stu-id="9a747-207">URLAllowlist</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) |<span data-ttu-id="9a747-208">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-208">Y</span></span> |<span data-ttu-id="9a747-209">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-209">Y</span></span> |
|[<span data-ttu-id="9a747-210">URLBlocklist</span><span class="sxs-lookup"><span data-stu-id="9a747-210">URLBlocklist</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) |<span data-ttu-id="9a747-211">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-211">Y</span></span> | <span data-ttu-id="9a747-212">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-212">Y</span></span>|
|[<span data-ttu-id="9a747-213">ManagedSearchEngines</span><span class="sxs-lookup"><span data-stu-id="9a747-213">ManagedSearchEngines</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedsearchengines) |<span data-ttu-id="9a747-214">N</span><span class="sxs-lookup"><span data-stu-id="9a747-214">N</span></span> | <span data-ttu-id="9a747-215">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-215">Y</span></span>|
|[<span data-ttu-id="9a747-216">UserFeedbackAllowed</span><span class="sxs-lookup"><span data-stu-id="9a747-216">UserFeedbackAllowed</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed) |<span data-ttu-id="9a747-217">N</span><span class="sxs-lookup"><span data-stu-id="9a747-217">N</span></span> | <span data-ttu-id="9a747-218">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-218">Y</span></span>|
|[<span data-ttu-id="9a747-219">VerticalTabsAllowed</span><span class="sxs-lookup"><span data-stu-id="9a747-219">VerticalTabsAllowed</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#verticaltabsallowed) | <span data-ttu-id="9a747-220">N</span><span class="sxs-lookup"><span data-stu-id="9a747-220">N</span></span>|<span data-ttu-id="9a747-221">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-221">Y</span></span> |
|[<span data-ttu-id="9a747-222">Параметры SmartScreen</span><span class="sxs-lookup"><span data-stu-id="9a747-222">SmartScreen settings</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreen-settings-policies) |<span data-ttu-id="9a747-223">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-223">Y</span></span> |<span data-ttu-id="9a747-224">Y</span><span class="sxs-lookup"><span data-stu-id="9a747-224">Y</span></span> |

## <span data-ttu-id="9a747-225">Microsoft Edge с ограниченным доступом</span><span class="sxs-lookup"><span data-stu-id="9a747-225">Microsoft Edge with assigned access</span></span>

### <span data-ttu-id="9a747-226">Режим терминала с одним приложением</span><span class="sxs-lookup"><span data-stu-id="9a747-226">Single app kiosk</span></span>

<span data-ttu-id="9a747-227">В настоящее время Microsoft Edge поддерживает набор таких же типов режимов терминала с ограниченным доступом для одного приложения, как и устаревшая версия Microsoft Edge, со следующими вариантами блокировки: цифровая или интерактивная вывеска и общедоступный просмотр.</span><span class="sxs-lookup"><span data-stu-id="9a747-227">Microsoft Edge currently supports a subset of the same Microsoft Edge Legacy kiosk mode types for single-app assigned access with the following lockdown experiences: Digital/Interactive signage, and Public-browsing.</span></span>  

<span data-ttu-id="9a747-228">Режим терминала с ограниченным доступом в настоящее время доступен для тестирования в последней  [сборке Windows 10 Insider Preview](https://insider.windows.com/) версии 20215 или выше, а также в  [канале Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download) версии 87.0.644.4 или выше.</span><span class="sxs-lookup"><span data-stu-id="9a747-228">Kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 or higher.</span></span>

**<span data-ttu-id="9a747-229">Откуда загрузить Windows Insider Preview?</span><span class="sxs-lookup"><span data-stu-id="9a747-229">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="9a747-230">Чтобы установить сборку Windows 10 Insider Preview на компьютер с Windows, следуйте инструкциям, указанным в разделе  [Начало работы со сборками Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="9a747-230">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="9a747-231">Режим терминала с несколькими приложениями</span><span class="sxs-lookup"><span data-stu-id="9a747-231">Multi-app kiosk</span></span>

<span data-ttu-id="9a747-232">Microsoft Edge можно запустить с [ограниченным доступом для нескольких приложений](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) в Windows 10, что является эквивалентом типа режима терминала «Обычный просмотр веб-страниц» в устаревшей версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a747-232">Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type.</span></span> <span data-ttu-id="9a747-233">Чтобы настроить ограниченный доступ для нескольких приложений в Microsoft Edge, следуйте инструкциям по [настройке режима терминала с несколькими приложениями](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span><span class="sxs-lookup"><span data-stu-id="9a747-233">To configure Microsoft Edge with multi-app assigned access, follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span></span> <span data-ttu-id="9a747-234">(AUMID для Microsoft Edge из стабильного канала— **MSEdge**).</span><span class="sxs-lookup"><span data-stu-id="9a747-234">(The AUMID for the Microsoft Edge Stable channel is **MSEdge**).</span></span>

<span data-ttu-id="9a747-235">При использовании Microsoft Edge с назначенным доступом для нескольких приложений можно настроить терминал Microsoft Edge для использования [политик браузера Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies), чтобы задать условия просмотра в зависимости от ваших уникальных требований.</span><span class="sxs-lookup"><span data-stu-id="9a747-235">When using Microsoft Edge with multi-app assigned access, you can configure Microsoft Edge kiosk to use the[Microsoft Edge browser policies](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) to configure the browsing experience to meet your unique requirements.</span></span>

### <span data-ttu-id="9a747-236">Настройка с помощью параметров Windows</span><span class="sxs-lookup"><span data-stu-id="9a747-236">Configure using Windows Settings</span></span>

<span data-ttu-id="9a747-237">Параметры Windows — это самый простой способ настроить одно или два устройства с одним приложением в режиме терминала.</span><span class="sxs-lookup"><span data-stu-id="9a747-237">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="9a747-238">Для настройки компьютера с одним приложением в режиме терминала выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="9a747-238">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="9a747-239">Установите последний выпуск Windows 10 Insider Preview версии 20215 или выше.</span><span class="sxs-lookup"><span data-stu-id="9a747-239">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="9a747-240">Следуйте инструкциям, указанным в разделе [Начало работы со сборками Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).</span><span class="sxs-lookup"><span data-stu-id="9a747-240">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="9a747-241">Установите последнюю версию [стабильного канала Microsoft Edge](https://www.microsoft.com/edge) версии 87 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="9a747-241">Install the latest version of [Microsoft Edge Stable channel](https://www.microsoft.com/edge), version 87 or higher.</span></span>  <span data-ttu-id="9a747-242">Чтобы протестировать новейшие функции, можно скачать последний канал [Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download)версии 89 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="9a747-242">To test the latest features, you can download the latest [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), version 89 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="9a747-243">Поскольку требуется установка на уровне устройства, поддерживается только канал, не связанный с Canary.</span><span class="sxs-lookup"><span data-stu-id="9a747-243">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="9a747-244">На компьютере терминала откройте параметры Windows и в поле поиска введите слово «терминал».</span><span class="sxs-lookup"><span data-stu-id="9a747-244">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="9a747-245">Чтобы открыть диалоговое окно для создания терминала, выберите  **Настройка терминала (ограниченный доступ)**, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="9a747-245">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Настройка терминала с ограниченным доступом":::

4. <span data-ttu-id="9a747-247">На странице **Настройка киоска** нажмите **Начать**.</span><span class="sxs-lookup"><span data-stu-id="9a747-247">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Страница терминала — начать":::

5. <span data-ttu-id="9a747-249">Введите имя для создания новой учетной записи в терминале или выберите существующую учетную запись из раскрывающегося списка и нажмите  **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9a747-249">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Режим терминала — создание учетной записи":::

6. <span data-ttu-id="9a747-251">На странице **Выбор приложения терминала**  выберите **Microsoft Edge** и нажмите кнопку  **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9a747-251">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="9a747-252">Это относится только к каналам Microsoft Edge Dev, бета-версиям канала и стабильным каналам.</span><span class="sxs-lookup"><span data-stu-id="9a747-252">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Режим терминала — выбор приложения":::

7. <span data-ttu-id="9a747-254">Выберите один из следующих вариантов отображения Microsoft Edge при работе в режиме терминала:</span><span class="sxs-lookup"><span data-stu-id="9a747-254">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="9a747-255">Цифровые или интерактивные вывески — Отображают конкретный сайт в полноэкранном режиме в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a747-255">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="9a747-256">Общедоступный браузер — Запускает ограниченную версию Microsoft Edge с несколькими вкладками.</span><span class="sxs-lookup"><span data-stu-id="9a747-256">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Экран режима терминала — цифровой указатель полного экрана":::

8. <span data-ttu-id="9a747-258">Нажмите  **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9a747-258">Select **Next**.</span></span>
9. <span data-ttu-id="9a747-259">Введите URL-адрес для загрузки при запуске киоска.</span><span class="sxs-lookup"><span data-stu-id="9a747-259">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Режим терминала — введите URL-адрес":::

10. <span data-ttu-id="9a747-261">Примите значение по умолчанию (5 минут) для времени простоя или укажите свое значение.</span><span class="sxs-lookup"><span data-stu-id="9a747-261">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Режим терминала — введите время простоя":::

11. <span data-ttu-id="9a747-263">Нажмите  **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9a747-263">Click **Next**.</span></span>
12. <span data-ttu-id="9a747-264">Закройте окно  **Параметры** , чтобы сохранить и применить свой выбор.</span><span class="sxs-lookup"><span data-stu-id="9a747-264">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Режим терминала — завершение настройки":::

13. <span data-ttu-id="9a747-266">Выйдите из устройства терминала и войдите в локальную учетную запись терминала, чтобы проверить конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="9a747-266">Sign out from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="9a747-267">Функциональные ограничения</span><span class="sxs-lookup"><span data-stu-id="9a747-267">Functional limitations</span></span>

<span data-ttu-id="9a747-268">С выпуском этой предварительной версии режима терминала мы продолжаем работать над улучшением продукта и добавлением новых функций.</span><span class="sxs-lookup"><span data-stu-id="9a747-268">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="9a747-269">Мы рекомендуем отключить:</span><span class="sxs-lookup"><span data-stu-id="9a747-269">We recommend that you turn off:</span></span>

- [<span data-ttu-id="9a747-270">StartupBoostEnabled</span><span class="sxs-lookup"><span data-stu-id="9a747-270">StartupBoostEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#startupboostenabled)
- [<span data-ttu-id="9a747-271">InternetExplorerIntegrationLevel</span><span class="sxs-lookup"><span data-stu-id="9a747-271">InternetExplorerIntegrationLevel</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [<span data-ttu-id="9a747-272">Расширения</span><span class="sxs-lookup"><span data-stu-id="9a747-272">Extensions</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions-policies)
- [<span data-ttu-id="9a747-273">BackgroundModeEnabled</span><span class="sxs-lookup"><span data-stu-id="9a747-273">BackgroundModeEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#backgroundmodeenabled)

## <span data-ttu-id="9a747-274">Стратегия</span><span class="sxs-lookup"><span data-stu-id="9a747-274">Roadmap</span></span>

### <span data-ttu-id="9a747-275">В начале 2021 года</span><span class="sxs-lookup"><span data-stu-id="9a747-275">In early 2021</span></span>

<span data-ttu-id="9a747-276">Будут добавлены следующая поддержка и возможности:</span><span class="sxs-lookup"><span data-stu-id="9a747-276">We'll add the following support and features:</span></span>

- <span data-ttu-id="9a747-277">Общая доступность режима киоска Microsoft Edge с одним приложением с единым доступом в Windows 10 1909 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="9a747-277">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows 10 1909 and higher.</span></span>
- <span data-ttu-id="9a747-278">Дополнительные возможности для обеспечения равных условий с устаревшей версией Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a747-278">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="9a747-279">Интеграция с Intune для настройки устройств с использованием пользовательского интерфейса профиля режима терминала.</span><span class="sxs-lookup"><span data-stu-id="9a747-279">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>
- <span data-ttu-id="9a747-280">Дополнительные сочетания клавиш будут заблокированы.</span><span class="sxs-lookup"><span data-stu-id="9a747-280">Additional keyboard shortcuts will be blocked.</span></span>
- <span data-ttu-id="9a747-281">Ограничение запуска других приложений из браузера.</span><span class="sxs-lookup"><span data-stu-id="9a747-281">Restrict the launch of other applications from the browser.</span></span>

## <span data-ttu-id="9a747-282">См. также</span><span class="sxs-lookup"><span data-stu-id="9a747-282">See also</span></span>

- [<span data-ttu-id="9a747-283">Настройка терминалов и цифровых вывесок в выпусках Windows для настольных компьютеров</span><span class="sxs-lookup"><span data-stu-id="9a747-283">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="9a747-284">Развертывание режима терминала в Microsoft Edge Legacy</span><span class="sxs-lookup"><span data-stu-id="9a747-284">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode)
- [<span data-ttu-id="9a747-285">Планирование развертывания Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9a747-285">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="9a747-286">Использование целевой страницы Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="9a747-286">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
