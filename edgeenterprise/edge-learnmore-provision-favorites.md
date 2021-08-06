---
title: Подготовка избранного для Microsoft Edge
ms.author: capoon
author: dan-wesley
manager: abutcher
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Подготовка избранного для Microsoft Edge
ms.openlocfilehash: 9b84c883ffd6ac39339c05a9a54a1912910341870cb35d7e338e6fde1e9ff5f3
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "11726036"
---
# <a name="provision-favorites-for-microsoft-edge"></a>Подготовка избранного для Microsoft Edge

С учетом отзывов пользователей были внесены улучшения в подготовку избранного. Начиная с Microsoft Edge версии 85 администраторам больше не нужно вручную создавать файл для подготовки избранного. Администраторы могут добавлять избранное и папки с помощью пользовательского интерфейса Microsoft Edge для создания файла, который можно экспортировать в групповую политику.

В этой статье описано, как подготовить набор избранного и папок для вашей организации. Можно использовать политику [Настроить избранное](//DeployEdge/microsoft-edge-policies#configure-favorites) для подготовки избранного и папок.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 85 или более поздней.

## <a name="prerequisites-and-recommendations"></a>Предварительные требования и рекомендации

- Microsoft Edge версии 85 с соответствующим административным шаблоном, установленным для групповых политик.
- Рекомендуется использовать новый профиль в Microsoft Edge для подготовки избранного. Все избранное, сохраненное вместе с профилем, будет включено в экспорт.  

## <a name="provision-favorites-and-folders"></a>Подготовка избранного и папок

Выполните следующие действия для подготовки избранного и папок для ваших пользователей.

1. Перейдите в адресную строку Microsoft Edge и введите этот URL-адрес: *edge://flags/#edge-favorites-admin-export*.
2. В разделе **Экспорт конфигурации избранного для администраторов**, выберите **Включено ** из раскрывающегося списка и затем нажмите **Перезапустить**.

3. Перейдите на страницу **Избранное** на странице *edge://favorites*, чтобы добавить избранное и папки, которые вы хотите подготовить.

<!--
4. On the **Favorites bar**, click **Add folder**. The folder structure of favorites that are set in the profile you're using will be reflected in the folder you provision for your users. The next screenshot shows "Managed favorites", the folder we'll use to provision favorites.

   ![Add a folder](media/edge-learnmore-provision-favorites/provision-favorites-add-folder.png)

   > [!TIP]
   > Add existing folders that contain favorites you want to provision for your users.

5. Select "Managed favorites" and then click **Add favorite**. The next screenshot shows the favorite we've added.

   ![Add a favorite](media/edge-learnmore-provision-favorites/provision-favorites-add-favorite.png)-->

4. Когда вы закончите добавлять избранное и папки, экспортируете их, чтобы их можно было использовать в политике **Настроить избранное**. Перейдите в адресную строку и перейдите к*edge://favorites*, нажмите на многоточие "**…**" и выберите **Экспорт конфигурации избранного**. На следующем снимке экрана показаны параметры, которые можно использовать при подготовке избранного.

   ![Параметры меню для работы с избранным.](media/edge-learnmore-provision-favorites/provision-favorites-menu-options.png)

5. В разделе **Экспорт конфигурации избранного** введите имя папки, которое будут видеть пользователи. Введите имя папки и выберите формат Платформы, которую хотите использовать. Щелкните **Копировать в буфер обмена**. На следующем снимке экрана показано «Управляемое избранное» для имени папки и платформы Windows.

   ![Диалоговое окно экспорта избранного в папку Windows.](media/edge-learnmore-provision-favorites/provision-favorites-export.png)

6. Откройте редактор управления групповой политикой, перейдите в раздел *Конфигурация компьютера/Административные шаблоны/* и выберите **Конфигурация избранного**. Включение политики «Настроить избранное». В разделе **Параметры:** вставьте экспортированное содержимое в текстовую область «Настроить избранное», а затем щелкните **Применить**. На следующем снимке экрана показан пример папки «Управляемое избранное» из шага 5.

   ![Используйте gpedit для включения и настройки политики «Настроить избранное».](media/edge-learnmore-provision-favorites/provision-favorites-gpedit.png)

7. Нажмите кнопку **OK** или **Применить** для сохранения настроек политики.

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)