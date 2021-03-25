---
title: Настройка параметров политики Microsoft Edge для Windows с помощью Microsoft Intune
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/18/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Настройка параметров политики Microsoft Edge для Windows с помощью Microsoft Intune.
ms.openlocfilehash: 0189a3fc2f9dc115563e7cf6dca1df960680bf22
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447563"
---
# <a name="configure-microsoft-edge-policy-settings-with-microsoft-intune"></a><span data-ttu-id="18c44-103">Настройка параметров политики Microsoft Edge с помощью Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="18c44-103">Configure Microsoft Edge policy settings with Microsoft Intune</span></span>

<span data-ttu-id="18c44-104">В этой статье приводятся инструкции по настройке параметров политики Microsoft Edge для Windows 10 с помощью Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="18c44-104">This article explains how to configure Microsoft Edge policy settings for Windows 10 using Microsoft Intune.</span></span>

> [!NOTE]
> <span data-ttu-id="18c44-105">Эта статья относится к Microsoft Edge версии 77 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="18c44-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="18c44-106">Вы можете настроить политики и параметры Microsoft Edge, добавив профиль конфигурации устройства в Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="18c44-106">You can configure Microsoft Edge policies and settings by adding a device configuration profile to Microsoft Intune.</span></span> <span data-ttu-id="18c44-107">Использование Intune для управления и применения политик аналогично использованию групповой политики Active Directory или настройке локальных параметров объекта групповой политики (GPO) на устройствах пользователей.</span><span class="sxs-lookup"><span data-stu-id="18c44-107">Using Intune to manage and enforce policies is equivalent to using Active Directory Group Policy or configuring local Group Policy Object (GPO) settings on user devices.</span></span>

<span data-ttu-id="18c44-108">Для получения дополнительных сведений об управлении политиками Microsoft Edge с помощью Microsoft Intune см. статью [Управление веб-доступом, используя Microsoft Edge с Microsoft Intune](/intune/manage-microsoft-edge), но помните, что эта статья относится к Microsoft Edge версии 45 и более ранним и, таким образом, может содержать сведения и ссылки, неприменимые к Microsoft Edge Enterprise версии 77 и более поздним.</span><span class="sxs-lookup"><span data-stu-id="18c44-108">For more information about managing Microsoft Edge policies with Microsoft Intune, you can read [Manage web access by using Microsoft Edge with Microsoft Intune](/intune/manage-microsoft-edge), but keep in mind that the linked article is specific to Microsoft Edge version 45 and earlier and therefore may contain information and references that don't apply to Microsoft Edge Enterprise version 77 and later.</span></span>

> [!TIP]
> <span data-ttu-id="18c44-109">Сведения о том, как настроить Microsoft Edge на macOS с помощью Microsoft Intune, см. в разделе [Настройка для macOS](configure-microsoft-edge-on-mac.md).</span><span class="sxs-lookup"><span data-stu-id="18c44-109">For information on how to configure Microsoft Edge on macOS using Microsoft Intune, see [Configure for macOS](configure-microsoft-edge-on-mac.md).</span></span>

## <a name="create-a-profile-to-manage-settings-in-microsoft-edge-for-windows-10"></a><span data-ttu-id="18c44-110">Создание профиля для управления параметрами в Microsoft Edge для Windows 10</span><span class="sxs-lookup"><span data-stu-id="18c44-110">Create a profile to manage settings in Microsoft Edge for Windows 10</span></span>

<span data-ttu-id="18c44-111">Используя административные шаблоны в Microsoft Intune, можно управлять групповыми политиками Microsoft Edge на устройствах с Windows 10 с помощью облака.</span><span class="sxs-lookup"><span data-stu-id="18c44-111">Using Administrative Templates in Microsoft Intune, you can manage Microsoft Edge group policies on your Windows 10 devices using the cloud.</span></span> <span data-ttu-id="18c44-112">В этом разделе приведены инструкции по созданию шаблона для настройки параметров приложений, работающих с Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="18c44-112">This section will help you create a template to configure Microsoft Edge-specific application settings.</span></span> <span data-ttu-id="18c44-113">При создании шаблона он создает профиль конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="18c44-113">When you create the template, it creates a device configuration profile.</span></span> <span data-ttu-id="18c44-114">Затем вы можете назначить или развернуть этот профиль на устройствах с Windows 10 в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="18c44-114">You can then assign or deploy this profile to Windows 10 devices in your organization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="18c44-115">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="18c44-115">Prerequisites</span></span>

- <span data-ttu-id="18c44-116">Windows 10 со следующими минимальными системными требованиями:</span><span class="sxs-lookup"><span data-stu-id="18c44-116">Windows 10 with the following minimum system requirements:</span></span>
  - <span data-ttu-id="18c44-117">Windows10 версии 1909</span><span class="sxs-lookup"><span data-stu-id="18c44-117">Windows 10, version 1909</span></span>
  - <span data-ttu-id="18c44-118">Windows 10, версия 1903 с установленным обновлением [KB4512941](https://support.microsoft.com/kb/4512941)</span><span class="sxs-lookup"><span data-stu-id="18c44-118">Windows 10, version 1903 with [KB4512941](https://support.microsoft.com/kb/4512941) installed</span></span>
  - <span data-ttu-id="18c44-119">Windows 10, версия 1809 с установленным обновлением [KB4512534](https://support.microsoft.com/kb/4512534)</span><span class="sxs-lookup"><span data-stu-id="18c44-119">Windows 10, version 1809 with [KB4512534](https://support.microsoft.com/kb/4512534) installed</span></span>
  - <span data-ttu-id="18c44-120">Windows 10, версия 1803 с установленным обновлением [KB4512509](https://support.microsoft.com/kb/4512509)</span><span class="sxs-lookup"><span data-stu-id="18c44-120">Windows 10, version 1803 with [KB4512509](https://support.microsoft.com/kb/4512509) installed</span></span>
  - <span data-ttu-id="18c44-121">Windows 10, версия 1709 с установленным обновлением [KB4516071](https://support.microsoft.com/kb/4516071)</span><span class="sxs-lookup"><span data-stu-id="18c44-121">Windows 10, version 1709 with [KB4516071](https://support.microsoft.com/kb/4516071) installed</span></span>

### <a name="use-administrative-templates-to-create-a-policy-for-microsoft-edge"></a><span data-ttu-id="18c44-122">Использование административных шаблонов для создания политики Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="18c44-122">Use Administrative Templates to create a policy for Microsoft Edge</span></span>

<span data-ttu-id="18c44-123">Эта процедура использует административные шаблоны (которые могут быть вам знакомы в рамках групповой политики), встроенные в Intune.</span><span class="sxs-lookup"><span data-stu-id="18c44-123">This procedure leverages Administrative templates (which you might be familiar with from Group Policy) that are built into Intune.</span></span> <span data-ttu-id="18c44-124">С помощью этих шаблонов можно создать политику для Microsoft Edge, выбрав параметры из предварительно настроенного списка.</span><span class="sxs-lookup"><span data-stu-id="18c44-124">You can use these templates to create a policy for Microsoft Edge by selecting settings from a pre-configured list.</span></span>

1. <span data-ttu-id="18c44-125">Войдите на портал [Диспетчера конечных точек (Майкрософт)](https://endpoint.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="18c44-125">Sign in to the [Microsoft Endpoint Manager](https://endpoint.microsoft.com/) portal.</span></span>
2. <span data-ttu-id="18c44-126">В области навигации слева выберите пункт **Устройства**.</span><span class="sxs-lookup"><span data-stu-id="18c44-126">Select **Devices** in the left-hand navigation pane.</span></span>
3. <span data-ttu-id="18c44-127">Из пункта **Устройства** | **Обзор** выберите **Профили конфигурации** (под заголовком политики).</span><span class="sxs-lookup"><span data-stu-id="18c44-127">From **Devices** | **Overview**, select **Configuration Profiles** (under Policy heading).</span></span>
4. <span data-ttu-id="18c44-128">На верхней панели команд выберите **Создать профиль**.</span><span class="sxs-lookup"><span data-stu-id="18c44-128">On the top command bar, select **Create profile**.</span></span>
5. <span data-ttu-id="18c44-129">В раскрывающемся списке под пунктом **Платформы**выберите **Windows 10 и более поздние версии**.</span><span class="sxs-lookup"><span data-stu-id="18c44-129">In the drop-down list below **Platform**, select **Windows 10 and later**.</span></span>
6. <span data-ttu-id="18c44-130">В раскрывающемся списке под пунктом **Профиль** выберите **Административные шаблоны** а затем нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="18c44-130">In the drop-down list below **Profile**, select **Administrative Templates** and then click the **Create** button.</span></span> <span data-ttu-id="18c44-131">На следующем снимке экрана показаны раскрывающиеся списки, в которых можно выбрать платформу и тип профиля.</span><span class="sxs-lookup"><span data-stu-id="18c44-131">The next screenshot shows the drop-down lists to select the platform and type of profile.</span></span>

    ![Выбор платформы и типа профиля](./media/configure-edge-with-intune/create-profile-platform.png)

7. <span data-ttu-id="18c44-133">На вкладке **Основы** введите описательное **Имя** (например, Политика Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="18c44-133">On the **Basics** tab, enter a descriptive **Name**, such as Microsoft Edge Policy.</span></span> <span data-ttu-id="18c44-134">Дополнительно введите **Описание** для политики.</span><span class="sxs-lookup"><span data-stu-id="18c44-134">Optionally, enter a  **Description** for the policy.</span></span>
<span data-ttu-id="18c44-135">На следующем снимке экрана показана форма для вкладки **Основы**, а в строке меню показаны следующие действия (в виде затемненных вкладок) для создания профиля.</span><span class="sxs-lookup"><span data-stu-id="18c44-135">The next screenshot shows the form for the **Basics** tab and the menu bar shows the next steps (as grayed out tabs) to create the profile.</span></span>

   ![Введите "Имя" и "Описание"](./media/configure-edge-with-intune/create-profile-basics-tab.png)

8. <span data-ttu-id="18c44-137">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="18c44-137">Select **Next**.</span></span>
9. <span data-ttu-id="18c44-138">На вкладке **Параметры конфигурации** выберите папку Microsoft Edge в одном из следующих расположений:</span><span class="sxs-lookup"><span data-stu-id="18c44-138">On the **Configuration settings** tab, select the Microsoft Edge folder in one of the following locations:</span></span>

   - <span data-ttu-id="18c44-139">под папкой "Конфигурация компьютера"</span><span class="sxs-lookup"><span data-stu-id="18c44-139">below the Computer Configuration folder</span></span>
   - <span data-ttu-id="18c44-140">под папкой "Конфигурация пользователя"</span><span class="sxs-lookup"><span data-stu-id="18c44-140">below the User Configuration folder.</span></span>

   <span data-ttu-id="18c44-141">Доступные параметры Microsoft Edge будут показаны в области справа.</span><span class="sxs-lookup"><span data-stu-id="18c44-141">The available settings for Microsoft Edge will be shown on the right pane.</span></span> <span data-ttu-id="18c44-142">Например, на снимке экрана ниже показана *Конфигурация компьютера/Microsoft Edge/Разрешить ограничения загрузки*.</span><span class="sxs-lookup"><span data-stu-id="18c44-142">For example, *Computer Configuration/Microsoft Edge/Allow download restrictions* shown in the following screenshot.</span></span>

   ![Вкладка "Параметры конфигурации"](./media/configure-edge-with-intune/create-profile-configuration-settings-tab.png)

   > [!NOTE]
   > <span data-ttu-id="18c44-144">Полный список всех актуальных доступных параметров для Microsoft Edge приведен в разделах [Microsoft Edge – Политики](./microsoft-edge-policies.md) и [Microsoft Edge – Обновление политик](./microsoft-edge-update-policies.md).</span><span class="sxs-lookup"><span data-stu-id="18c44-144">See [Microsoft Edge – Policies](./microsoft-edge-policies.md) and [Microsoft Edge – Update policies](./microsoft-edge-update-policies.md) for the most complete and up to date list of all the available settings for Microsoft Edge.</span></span>

10. <span data-ttu-id="18c44-145">Используйте поле поиска ("Поиск элементов для фильтрации..."), чтобы найти конкретный параметр для настройки.</span><span class="sxs-lookup"><span data-stu-id="18c44-145">Use the search field ("Search to filter items ...") to find a specific setting you want to configure.</span></span> <span data-ttu-id="18c44-146">В этом примере строка поиска – это "Домашняя страница".</span><span class="sxs-lookup"><span data-stu-id="18c44-146">In this example, the search string is "home page".</span></span> <span data-ttu-id="18c44-147">На следующем снимке экрана показаны результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="18c44-147">The next screenshot shows the search results.</span></span>

    ![Результаты поиска](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-search.png)

11. <span data-ttu-id="18c44-149">Найдя параметр для настройки, выберите его, чтобы вывести значения, которые можно задать.</span><span class="sxs-lookup"><span data-stu-id="18c44-149">After you find the setting you intend to configure, select it to expose the values you can set.</span></span> <span data-ttu-id="18c44-150">На следующем снимке экрана мы выбрали "Настроить URL-адрес домашней страницы".</span><span class="sxs-lookup"><span data-stu-id="18c44-150">In the next screenshot, we selected "Configure the home page URL" as an example.</span></span>

    ![Настройка URL-адреса домашней страницы](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-edit-pol.png)

12. <span data-ttu-id="18c44-152">Включите политику и введите значения для URL-адреса домашней страницы, как показано на предыдущем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="18c44-152">Enable the policy and enter a value for the Home page URL, as shown in the previous screenshot.</span></span>

13. <span data-ttu-id="18c44-153">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="18c44-153">Click **OK**.</span></span> <span data-ttu-id="18c44-154">В столбце "Состояние" должно отображаться значение "Включено", как показано на снимке экрана ниже.</span><span class="sxs-lookup"><span data-stu-id="18c44-154">The settings "State" column should appear as "Enabled", as shown in the following screenshot example.</span></span>

    ![Состояние параметра "Включено"](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-set-enabled.png)

14. <span data-ttu-id="18c44-156">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="18c44-156">Click the **Next** button.</span></span>

15. <span data-ttu-id="18c44-157">На вкладке **Теги области** добавьте "Тег области" при необходимости, в противном случае нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="18c44-157">On the **Scope tags** tab, add a Scope tag if wanted, otherwise click the **Next** button.</span></span>

16. <span data-ttu-id="18c44-158">На вкладке **Назначения** выберите пункт **+ Выбрать группы для включения**, чтобы назначить эту политику группе Azure Active Directory (Azure AD), содержащей устройства или пользователей, для которых вы хотите предоставить этот параметр политики.</span><span class="sxs-lookup"><span data-stu-id="18c44-158">On the **Assignments** tab, click **+ Select groups to include** to assign this policy to the Azure Active Directory (Azure AD) group that contains the devices or the users that you want to receive this policy setting.</span></span> <span data-ttu-id="18c44-159">См. раздел [Назначение профилей пользователей и устройств в Microsoft Intune](/intune/device-profile-assign) для получения инструкций по назначению профиля группам пользователей или устройств в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="18c44-159">See [Assign user and device profiles in Microsoft Intune](/intune/device-profile-assign) for information about how to assign the profile to your Azure AD user or device groups.</span></span>

    ![Выбор групп для включения](./media/configure-edge-with-intune/create-profile-assignments-tab.png)

17. <span data-ttu-id="18c44-161">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="18c44-161">Click the **Next** button.</span></span>

18. <span data-ttu-id="18c44-162">На вкладке **Проверка и создание** просмотрите сводку изменений, чтобы убедиться в корректности изменений, а затем нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="18c44-162">On the **Review + create** tab, review the summary of your changes to ensure it's correct and then click the **Create** button.</span></span>

19. <span data-ttu-id="18c44-163">На снимке экрана ниже показана новая созданная политика (политика Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="18c44-163">The newly created policy (Microsoft Edge Policy) is shown in the following screenshot.</span></span>

    ![Выбор групп для включения](./media/configure-edge-with-intune/create-profile-new-policy-finished.png)

<span data-ttu-id="18c44-165">Дополнительные сведения о профилях Windows 10 см. в разделе [Использование шаблонов Windows 10 для настройки параметров групповой политики в Microsoft Intune](/intune/administrative-templates-windows).</span><span class="sxs-lookup"><span data-stu-id="18c44-165">For more information about Windows 10 profiles, see [Use Windows 10 templates to configure group policy settings in Microsoft Intune](/intune/administrative-templates-windows).</span></span>

## <a name="see-also"></a><span data-ttu-id="18c44-166">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="18c44-166">See also</span></span>

- [<span data-ttu-id="18c44-167">Использование целевой страницы Microsoft Edge Enterprise</span><span class="sxs-lookup"><span data-stu-id="18c44-167">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="18c44-168">Управление веб-доступом, используя Microsoft Edge с Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="18c44-168">Manage web access by using Microsoft Edge with Microsoft Intune</span></span>](/intune/manage-microsoft-edge)
- [<span data-ttu-id="18c44-169">Использование шаблонов Windows 10 для настройки параметров групповой политики в Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="18c44-169">Use Windows 10 templates to configure group policy settings in Microsoft Intune</span></span>](/intune/administrative-templates-windows)
- [<span data-ttu-id="18c44-170">Развертывание Microsoft Edge с помощью Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="18c44-170">Deploy Microsoft Edge using Microsoft Intune</span></span>](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)