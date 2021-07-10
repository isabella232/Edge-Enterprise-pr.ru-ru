---
title: Настройка параметров политики Microsoft Edge для Windows с помощью Microsoft Intune
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Настройка параметров политики Microsoft Edge для Windows с помощью Microsoft Intune.
ms.openlocfilehash: adcd80f68250a9694b9bbaa21fb7941ebcbaf15a
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641675"
---
# <a name="configure-microsoft-edge-policy-settings-with-microsoft-intune"></a>Настройка параметров политики Microsoft Edge с помощью Microsoft Intune

В этой статье приводятся инструкции по настройке параметров политики Microsoft Edge для Windows 10 с помощью Microsoft Intune.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

Вы можете настроить политики и параметры Microsoft Edge, добавив профиль конфигурации устройства в Microsoft Intune. Использование Intune для управления и применения политик аналогично использованию групповой политики Active Directory или настройке локальных параметров объекта групповой политики (GPO) на устройствах пользователей.

Для получения дополнительных сведений об управлении политиками Microsoft Edge с помощью Microsoft Intune см. статью [Управление веб-доступом, используя Microsoft Edge с Microsoft Intune](/intune/manage-microsoft-edge), но помните, что эта статья относится к Microsoft Edge версии 45 и более ранним и, таким образом, может содержать сведения и ссылки, неприменимые к Microsoft Edge Enterprise версии 77 и более поздним.

> [!TIP]
> Сведения о том, как настроить Microsoft Edge на macOS с помощью Microsoft Intune, см. в разделе [Настройка для macOS](configure-microsoft-edge-on-mac.md).

## <a name="create-a-profile-to-manage-settings-in-microsoft-edge-for-windows-10"></a>Создание профиля для управления параметрами в Microsoft Edge для Windows 10

Используя административные шаблоны в Microsoft Intune, можно управлять групповыми политиками Microsoft Edge на устройствах с Windows 10 с помощью облака. В этом разделе приведены инструкции по созданию шаблона для настройки параметров приложений, работающих с Microsoft Edge. При создании шаблона он создает профиль конфигурации устройства. Затем вы можете назначить или развернуть этот профиль на устройствах с Windows 10 в вашей организации.

### <a name="prerequisites"></a>Предварительные требования

- Windows 10 со следующими минимальными системными требованиями:
  - Windows 10 версии 1909
  - Windows 10, версия 1903 с установленным обновлением [KB4512941](https://support.microsoft.com/kb/4512941)
  - Windows 10, версия 1809 с установленным обновлением [KB4512534](https://support.microsoft.com/kb/4512534)
  - Windows 10, версия 1803 с установленным обновлением [KB4512509](https://support.microsoft.com/kb/4512509)
  - Windows 10, версия 1709 с установленным обновлением [KB4516071](https://support.microsoft.com/kb/4516071)

### <a name="use-administrative-templates-to-create-a-policy-for-microsoft-edge"></a>Использование административных шаблонов для создания политики Microsoft Edge

Эта процедура использует административные шаблоны (которые могут быть вам знакомы в рамках групповой политики), встроенные в Intune. С помощью этих шаблонов можно создать политику для Microsoft Edge, выбрав параметры из предварительно настроенного списка.

1. Войдите на портал [Диспетчера конечных точек (Майкрософт)](https://endpoint.microsoft.com/).
2. В области навигации слева выберите пункт **Устройства**.
3. Из пункта **Устройства** | **Обзор** выберите **Профили конфигурации** (под заголовком политики).
4. На верхней панели команд выберите **Создать профиль**.
5. В раскрывающемся списке под пунктом **Платформы**выберите **Windows 10 и более поздние версии**.
6. В раскрывающемся списке под пунктом **Профиль** выберите **Административные шаблоны** а затем нажмите кнопку **Создать**. На следующем снимке экрана показаны раскрывающиеся списки, в которых можно выбрать платформу и тип профиля.

    ![Выбор платформы и типа профиля](./media/configure-edge-with-intune/create-profile-platform.png)

7. На вкладке **Основы** введите описательное **Имя** (например, Политика Microsoft Edge). Дополнительно введите **Описание** для политики.
На следующем снимке экрана показана форма для вкладки **Основы**, а в строке меню показаны следующие действия (в виде затемненных вкладок) для создания профиля.

   ![Введите "Имя" и "Описание"](./media/configure-edge-with-intune/create-profile-basics-tab.png)

8. Выберите **Далее**.
9. На вкладке **Параметры конфигурации** выберите папку Microsoft Edge в одном из следующих расположений:

   - под папкой "Конфигурация компьютера"
   - под папкой "Конфигурация пользователя"

   Доступные параметры Microsoft Edge будут показаны в области справа. Например, на снимке экрана ниже показана *Конфигурация компьютера/Microsoft Edge/Разрешить ограничения загрузки*.

   ![Вкладка "Параметры конфигурации"](./media/configure-edge-with-intune/create-profile-configuration-settings-tab.png)

   > [!NOTE]
   > Полный список всех актуальных доступных параметров для Microsoft Edge приведен в разделах [Microsoft Edge – Политики](./microsoft-edge-policies.md) и [Microsoft Edge – Обновление политик](./microsoft-edge-update-policies.md).

10. Используйте поле поиска ("Поиск элементов для фильтрации..."), чтобы найти конкретный параметр для настройки. В этом примере строка поиска – это "Домашняя страница". На следующем снимке экрана показаны результаты поиска.

    ![Результаты поиска](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-search.png)

11. Найдя параметр для настройки, выберите его, чтобы вывести значения, которые можно задать. На следующем снимке экрана мы выбрали "Настроить URL-адрес домашней страницы".

    ![Настройка URL-адреса домашней страницы](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-edit-pol.png)

12. Включите политику и введите значения для URL-адреса домашней страницы, как показано на предыдущем снимке экрана.

13. Нажмите кнопку **ОК**. В столбце "Состояние" должно отображаться значение "Включено", как показано на снимке экрана ниже.

    ![Состояние параметра "Включено"](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-set-enabled.png)

14. Нажмите кнопку **Далее**.

15. На вкладке **Теги области** добавьте "Тег области" при необходимости, в противном случае нажмите кнопку **Далее**.

16. На вкладке **Назначения** выберите пункт **+ Выбрать группы для включения**, чтобы назначить эту политику группе Azure Active Directory (Azure AD), содержащей устройства или пользователей, для которых вы хотите предоставить этот параметр политики. См. раздел [Назначение профилей пользователей и устройств в Microsoft Intune](/intune/device-profile-assign) для получения инструкций по назначению профиля группам пользователей или устройств в Azure AD.

    ![Выбор групп для включения](./media/configure-edge-with-intune/create-profile-assignments-tab.png)

17. Нажмите кнопку **Далее**.

18. На вкладке **Проверка и создание** просмотрите сводку изменений, чтобы убедиться в корректности изменений, а затем нажмите кнопку **Создать**.

19. На снимке экрана ниже показана новая созданная политика (политика Microsoft Edge).

    ![Выбор групп для включения](./media/configure-edge-with-intune/create-profile-new-policy-finished.png)

Дополнительные сведения о профилях Windows 10 см. в разделе [Использование шаблонов Windows 10 для настройки параметров групповой политики в Microsoft Intune](/intune/administrative-templates-windows).

## <a name="see-also"></a>Статьи по теме

- [Использование целевой страницы Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Управление веб-доступом, используя Microsoft Edge с Microsoft Intune](/intune/manage-microsoft-edge)
- [Использование шаблонов Windows 10 для настройки параметров групповой политики в Microsoft Intune](/intune/administrative-templates-windows)
- [Развертывание Microsoft Edge с помощью Microsoft Intune](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)