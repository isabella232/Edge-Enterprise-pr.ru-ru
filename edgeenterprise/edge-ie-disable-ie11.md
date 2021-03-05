---
title: Отключение Internet Explorer 11
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/04/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Узнайте, как отключить Internet Explorer 11 и использовать режим Internet Explorer в Microsoft Edge.
ms.openlocfilehash: be52f33b091977aff0ca29a4e10d4fc6ea4be957
ms.sourcegitcommit: f63a30c3e64e9e57fd76b6675ddff1fc2bbbeac8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "11393613"
---
# <a name="disable-internet-explorer-11"></a>Отключение Internet Explorer 11

В этой статье описано, как отключить Internet Explorer 11 в качестве автономного браузера в вашей среде.

## <a name="prerequisites"></a>Предварительные условия

Требуются следующие обновления Windows и программное обеспечение Microsoft Edge:

- Обновления Windows

  - Windows 10 версии 2004, Windows Server версии 2004, Windows 10 версии 20H2: обновление [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) или более позднее
  - Windows 10 версии 1909, Windows Server версии 1909: обновление [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) или более позднее
  - Windows 10 версии 1809, Windows Server версии 1809 и Windows Server 2019: обновление [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) или более позднее
  - Windows 10 версии 1607, Windows Server 2016: обновление [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) или более позднее
   - Начальная версия Windows 10 (июль 2015 г.): обновление [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) или более позднее
  - Windows 8.1: обновление [KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) или более позднее
  - Windows Server 2012: обновление [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) или более позднее
  
- Стабильный канал Microsoft Edge


## <a name="overview"></a>Обзор

Организациям, которым требуется Internet Explorer 11 (IE11) для обеспечения совместимости с устаревшими программами, режим Internet Explorer (режим IE) в Microsoft Edge обеспечивает удобный интерфейс в одном браузере. Пользователи могут получать доступ к устаревшим приложениям из Microsoft Edge, не возвращаясь к IE11.

После настройки режима IE вы можете отключить IE11 в качестве автономного браузера, **не затрагивая функции режима IE** в организации, с помощью групповой политики.

> [!NOTE]
> Если вам нужно отдельное приложение IE11 для определенных сайтов и вы хотите перенаправлять весь трафик браузера в Microsoft Edge, вы можете настроить политику [Отправлять все сайты, которые не включены в список сайтов, в Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge), чтобы перенаправлять сайты из IE в Microsoft Edge.

## <a name="user-experience-after-redirecting-traffic-to-microsoft-edge"></a>Взаимодействие с пользователем после перенаправления трафика в Microsoft Edge

Если включить политику **Отключить Internet Explorer 11 в качестве автономного браузера**, действия IE11 перенаправляются в Microsoft Edge и пользователям предлагается следующее взаимодействие:

- Значок IE11 в меню "Пуск" будет удален, но останется значок на панели задач.
- При попытке запуска ярлыков или сопоставлений файлов, применяющих IE11, пользователи будут перенаправлены в Microsoft Edge для открытия этого файла или URL-адреса.
- Если пользователи попытаются запустить IE11, непосредственно вызвав двоичный файл iexplore.exe, вместо этого запустится Microsoft Edge.

В рамках настройки политики для этого интерфейса вы можете дополнительно отображать сообщение о перенаправлении для каждого пользователя, который пытается запустить IE11. Для этого сообщения можно настроить следующие варианты отображения: "Всегда" или "Однократно для пользователя". По умолчанию сообщение о перенаправлении, показанное на следующем снимке экрана, никогда не отображается.

:::image type="content" source="media/edge-ie-disable-ie11/disable-ie-redirect-msg.png" alt-text="Оповещение при попытке открыть IE после активации перенаправления в Microsoft Edge.":::

Если список сайтов в режиме предприятия содержит приложения, настроенные для открытия в приложении IE11, и вы отключили IE11 с помощью этой политики, они будут открываться в режиме IE в браузере Microsoft Edge.
> [!NOTE]
> Существует известная проблема с пользовательским потоком, если сайт настроен на открытие в IE11 и задана политика отключения IE11. Эта проблема активно исследуется.

## <a name="disable-internet-explorer-11-as-a-standalone-browser"></a>Отключение Internet Explorer 11 в качестве автономного браузера

Чтобы отключить Internet Explorer 11 с помощью групповой политики, выполните следующие действия.

1. Скачайте и установите последний  [шаблон политики Microsoft Edge](https://www.microsoft.com/edge/business/download).
2. Откройте редактор групповых политик.
3. Выберите ***Конфигурация компьютера/Административные шаблоны/Компоненты Windows/Internet Explorer***. 
4. Дважды щелкните  **Отключить Internet Explorer 11 в качестве автономного браузера**.
5. Выберите  **Включено**.
6. В разделе  **Параметры** выберите одно из следующих значений.

   - **Никогда**,  если вы не хотите уведомлять пользователей об отключении IE11.
   - **Всегда**,  если вы хотите уведомлять пользователей при каждом перенаправлении из IE11.
   - **Однократно для пользователя**,  если вы хотите уведомлять пользователей только при первом перенаправлении.

7. Нажмите  **ОК**  или  **Применить**  для сохранения этого параметра политики.

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Сведения о режиме IE](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Дополнительные сведения о режиме предприятия](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
