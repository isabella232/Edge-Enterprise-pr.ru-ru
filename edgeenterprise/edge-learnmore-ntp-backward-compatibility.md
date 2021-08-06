---
title: Обратная совместимость для корпоративной страницы новой вкладки
ms.author: ruchir
author: dan-wesley
manager: vwehren
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Обратная совместимость для корпоративной страницы новой вкладки
ms.openlocfilehash: 9643a7009fdc60859efaadc2adff6e47ce0918567195e9745a4a93c151aefc80
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "11724228"
---
# <a name="backwards-compatibility-for-the-enterprise-new-tab-page"></a>Обратная совместимость для корпоративной страницы новой вкладки

В этой статье описано изменение страницы новой вкладки, а также способ обеспечения обратной совместимости для пользователей в Microsoft Edge версии 87 и более ранних версиях.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 87 или более поздней.

## <a name="information-feeds-from-single-endpoint"></a>Информационные веб-каналы из одной конечной точки

Новая версия корпоративной страницы новой вкладки объединяет соответствующий контент Microsoft 365 с важными и подходящими отраслевыми информационными веб-каналами, которые предоставляются посредством конечной точки MSN.com

> [!NOTE]
> Контент Office 365 изначально предоставлялся с помощью домена [Office.com](https://www.office.com).

Если доступ к домену MSN.com ограничен в вашей организации, настоятельно рекомендуется предоставить пользователям доступ к этому [URL-адресу](https://ntp.msn.com).

Если вам нужно больше времени для разрешения доступа к домену MSN, рекомендуется использовать политику [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype), позволяющую выбрать веб-канал Microsoft News или Office 365 на странице новой вкладки.

### <a name="keep-using-officecom"></a>Продолжение использования Office.com

 Вы можете настроить политику **NewTabPageSetFeedType**, чтобы использовать устаревший домен Office.com.

> [!IMPORTANT]
> Политика **NewTabPageSetFeedType** и домен Office.com, предоставляющие контент Office 365, перестанут работать после выпуска Microsoft Edge версии 90.

Следующие параметры политики обеспечат отображение на корпоративной странице новой вкладки контента документа Office из домена Office.com.

- Настройте политику как **обязательную**.
- Установите для сопоставления политики значение **Office (1) = Office 365 feed experience**.

Если переключение на Office.com невозможно, отправьте нам отзыв. Кроме того, можно настроить политику [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation), чтобы она указывала на URL-адрес конечной точки, разрешенный в вашей организации.

> [!NOTE]
> Политика **NewTabPageLocation** имеет приоритет, если политика **NewTabPageSetFeedType** также настроена.

## <a name="enterprise-users-will-now-get-microsoft-news-content-via-my-feed"></a>Корпоративным пользователям теперь будет доступен контент Microsoft News в канале "Моя лента"

Корпоративная страница новой вкладки предлагает отраслевые сведения в канале **Моя лента** и контент Office 365 в одном представлении для пользователей, вошедших в свою учетную запись Azure Active Directory (Azure AD). Для пользователей, вошедших с помощью учетной записи Azure Active Directory (Azure AD) и выбравших параметр Microsoft News во всплывающем окне параметров, представление страницы новой вкладки будет заменено на контент канала **Моя лента**. Когда они откроют страницу новой вкладки в браузере, она будет выглядеть, как показано в примере на следующем снимке экрана.

![Страница новой вкладки с отображением контента из канала "Моя лента".](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-myfeed-view.png)

> [!NOTE]
> Пользователям, не вошедшим в Azure AD, будет по-прежнему отображаться веб-канал MSN News при открытии новой вкладки.

## <a name="page-layout"></a>Макет страницы

После изменений страницы новой вкладки макет страницы больше не должен управлять двумя определенными типами контента (Office 365 и Microsoft News), поэтому переключатель контента недоступен. На следующем снимке экрана показано всплывающее окно макета страницы.

![Представление макета страницы для страницы новой вкладки.](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-page-layout.png)

Если вы хотите продолжать обращаться к контенту Microsoft News, не связанному с вашей организацией, вы должны использовать другой профиль браузера. Перейдите на страницу *edge://settings/profiles* и выйдите из профиля Azure AD. В результате этого действия отобразится стандартное представление корпоративной страницы новой вкладки. 

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Режим предприятия для Internet Explorer 11](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)