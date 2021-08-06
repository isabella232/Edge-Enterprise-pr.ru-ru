---
title: Автоматизация развертывания Microsoft Edge в среде macOS с помощью Jamf
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Инструкции по автоматизации развертывания Microsoft Edge в среде macOS с помощью Jamf.
ms.openlocfilehash: ab860bf90aa2472dd3a0437dfc98261421c8b5467d8e2f5cb28d511f5b7b0d51
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "11726338"
---
# <a name="deploy-to-macos-with-jamf"></a>Развертывание в macOS с помощью Jamf

В этой статье описано, как выполнить развертывание Microsoft Edge в среде macOS с помощью Jamf.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## <a name="prerequisites"></a>Что вам понадобится

Перед развертыванием Microsoft Edge убедитесь, что выполнены следующие необходимые условия.

- Файл установки Microsoft Edge — **MicrosoftEdgeDev-\<version\>.pkg** находится в доступном сетевом расположении. Вы можете скачать файлы установки Microsoft Edge Enterprise с [целевой страницы Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise).
- У вас есть учетная запись Jamf Cloud с уровнем доступа и правами, необходимыми для создания и развертывания установочных файлов на компьютерах.

## <a name="to-deploy-microsoft-edge-using-jamf"></a>Чтобы развернуть Microsoft Edge с помощью Jamf, выполните следующие действия.

1. Войдите в Jamf и перейдите в раздел **Все параметры**.

    ![Откройте "Все параметры"](./media/mac-deploy/jamf-dash-main-open-settings.png)

2. В разделе **Все параметры** выберите **Управление компьютерами**.

    ![Выберите "Управление компьютерами"](./media/mac-deploy/jamf-all-settings-computer-mgmt.png)

3. В разделе **Управление компьютерами** выберите **Пакеты**.

    ![Выберите "Пакеты"](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkgs.png)

4. На странице **Пакеты** нажмите кнопку **+ Создать**, чтобы добавить новый пакет.

    ![Выберите "Создать", чтобы добавить новый пакет](./media/mac-deploy/jamf-all-settings-computer-mgmt-new-pkg.png)

5. На странице **Новый пакет** введите сведения о пакете и нажмите кнопку **Сохранить**. (Например, ОТОБРАЖАЕМОЕ ИМЯ, СВЕДЕНИЯ или ЗАМЕТКИ.)

    ![Выберите "Сохранить", чтобы сохранить сведения о пакете](./media/mac-deploy/jamf-all-settings-computer-mgmt-save-pkg-info.png)

6. Выберите **Компьютеры** в строке меню, а затем — **Политики** на панели навигации.

7. Нажмите кнопку **+ Создать**, чтобы открыть панель **Новая политика**.

    ![Выберите "Создать", чтобы создать новую политику](./media/mac-deploy/jamf-all-settings-computer-new-policy.png)

8. На вкладке **Параметры** выберите **Общие**.

    - В разделе **ОТОБРАЖАЕМОЕ ИМЯ** введите отображаемое имя политики.
    - В разделе **Триггер** выберите событие, которое будет запускать политику. (В следующем примере таким событием является "Запуск".)

    ![Введите сведения о развертывании](./media/mac-deploy/jamf-all-settings-computer-cfg-policy.png)

9. На вкладке **Параметры** выберите **Пакеты**.

10. Во всплывающем окне **Настройка пакетов** выберите **Настроить**.

    ![Настройка пакета](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-configure.png)

11. Добавленный пакет отобразится на панели **Пакеты**. Щелкните **Добавить**. В этом примере пакет "MicrosoftEdgeBeta" представлен на следующем снимке экрана.

    ![Добавление пакета](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-add-beta.png)

12. На странице **Новая политика** используйте раскрывающиеся списки для выбора **ТОЧКИ РАСПРОСТРАНЕНИЯ** и **ДЕЙСТВИЯ**, которые будет использовать и выполнять политика. Нажмите кнопку **Сохранить**. На следующем снимке экрана в качестве примера представлены "Each computer's default distribution point" (Точка распространения по умолчанию каждого компьютера) и "Install" (Установить).

    ![Выбор точки распространения и действия](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkg-cfg-distro.png)

13. На странице **Новая политика** перейдите на вкладку **Область**. Областью развертывания можно управлять на основе компьютеров или пользователей. В этом примере выберите **Все компьютеры** в раскрывающемся списке **КОНЕЧНЫЕ КОМПЬЮТЕРЫ**, а затем нажмите **Сохранить**.

    ![Выбор области развертывания](./media/mac-deploy/jamf-all-settings-computer-mgmt-add-target.png)

14. На этом этапе вы можете просмотреть политику развертывания Microsoft Edge. Если варианты развертывания соответствуют вашим требованиям, нажмите кнопку **Готово**.

    ![Нажмите кнопку "Готово"](./media/mac-deploy/jamf-all-settings-computer-mgmt-finish-add-deployment.png)

    > [!NOTE]
    > Вы можете вернуться к политике развертывания в любое время, чтобы изменить параметры.

Поздравляем! Вы только что завершили настройку развертывания Microsoft Edge для macOS с помощью Jamf. Когда заданным условием триггера станет значение "true", пакет будет развернут на указанных компьютерах.

## <a name="see-also"></a>Статьи по теме

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Jamf.com](https://www.jamf.com/)
- [Интеграция Jamf с Microsoft Intune](/intune/conditional-access-integrate-jamf)