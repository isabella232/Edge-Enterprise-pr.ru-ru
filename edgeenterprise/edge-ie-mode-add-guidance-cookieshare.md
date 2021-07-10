---
title: Отправка файлов cookie из Microsoft Edge в Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 'Как отправлять файлы cookie из Microsoft Edge в Internet Explorer '
ms.openlocfilehash: 8f1a38106e49f71aa9d27f32cfecbd0df44eaf9f
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641845"
---
# <a name="cookie-sharing-from-microsoft-edge-to-internet-explorer"></a>Отправка файлов cookie из Microsoft Edge в Internet Explorer

>[!Note]
> Поддержка классического приложения Internet Explorer 11 будет прекращена 15 июня 2022 г. (список области применения см. в [вопросах и ответах](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Те же приложения и сайты IE11, которые вы используете сегодня, можно открывать в Microsoft Edge в режиме Internet Explorer. Дополнительные сведения см. [здесь](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

В этой статье объясняется, как настроить отправку файлов cookie сеанса из процесса Microsoft Edge в процесс Internet Explorer, используя режим Internet Explorer.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 87 или более поздней.

## <a name="prerequisites"></a>Предварительные условия

- Обновления Windows

  - Windows 10 версии 2004, Windows Server версии 2004 — KB4571744 и выше
  - Windows 10 версии 1909, Windows Server версии 1909 — KB4566116 и выше
  - Windows 10 версии 1903, Windows Server версии 1903 — KB4566116 и выше
  - Windows 10, версии 1809, Windows Server версии 1809 и Windows Server 2019 — KB4571748 и выше
  - Windows 10 версии 1803 — KB4577032 и выше

- Microsoft Edge версии 87 или более поздней
- [Режим IE,](./edge-ie-mode.md) настроенный с помощью списка сайтов в режиме предприятия

## <a name="overview"></a>Обзор

Распространенной конфигурацией в крупных организациях является наличие приложения, работающего на основе связи современного браузера с другим приложением, которое может быть настроено на открытие в режиме Internet Explorer с поддержкой единого входа (SSO) в рамках рабочего процесса.

По умолчанию процессы Microsoft Edge и Internet Explorer не делятся файлами cookie сеансов, что иногда может быть неудобным. Например, если пользователю требуется повторно пройти проверку подлинности в режиме Internet Explorer или при выходе из сеанса Microsoft Edge требуется не выходить из сеанса в режиме Internet Explorer. В таких сценариях вы можете настроить определенный набор файлов cookie (с помощью единого входа) на отправку из Microsoft Edge в Internet Explorer, чтобы проверка подлинности выполнялась проще благодаря устранению повторной проверки подлинности.

> [!NOTE]
> Файлы cookie сеанса можно отправлять только из Microsoft Edge в Internet Explorer. Отправка файлов cookie в обратном направлении (из Internet Explorer в Microsoft Edge) невозможна.

## <a name="how-cookie-sharing-works"></a>Как работает отправка файлов cookie

XML-файл списка сайтов в режиме предприятия расширен для разрешения дополнительных элементов, чтобы указать файлы cookie, которые требуется отправить из сеанса Microsoft Edge в Internet Explorer.  

При первом создании вкладки режима Internet Explorer в сеансе Microsoft Edge все соответствующие файлы cookie становятся общими для сеанса Internet Explorer. В дальнейшем при каждом добавлении, удалении или изменении файла cookie, соответствующего правилу, он отправляется в виде обновления в сеанс Internet Explorer. При обновлении списка сайтов набор общих файлов cookie также оценивается повторно.

### <a name="updated-schema-elements"></a>Обновленные элементы схемы

В таблице ниже описан элемент \<shared-cookie\>, добавленный для поддержки функции отправки файлов cookie.

| Элемент| Описание |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br>ИЛИ<br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |**(Обязательно)** Элемент \<shared-cookie\> требует как минимум атрибут *domain* (для файлов cookie домена) или *host* (для файлов cookie, предназначенных только для узла) и атрибут *name*.<br>Они должны в точности совпадать с доменом и именем файла cookie соответственно. **Обратите внимание**, что поддомены не совпадают.<br><br>Атрибут *domain* используется для файлов cookie домена (начальная точка разрешена, но необязательна).<br>Атрибут *host* используется только для файлов cookie, предназначенных для узла (начальная точка является ошибкой). Указание обоих аргументов (или их отсутствие) приведет к ошибке.<br>* Файл cookie — это файл cookie домена, если домен был указан в строке файла cookie (с помощью HTTP-заголовка отклика Set-cookie или API JS document.cookie). Файл cookie домена применяется к указанному домену и всем поддоменам. Если домен не был указан в строке файла cookie, файл cookie предназначается только для узла и применяется только к определенному узлу, для которого он был настроен. Обратите внимание, что некоторые классы URL-адресов, такие как имена узлов из одного слова (например, http://intranetsite) и IP-адреса (например, http://10.0.0.1), могут задавать только файлы cookie, предназначенные для узла.    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | **(Необязательно)** Можно указать атрибут *path*. Если атрибут path не указан (или атрибут path не заполнен), все файлы cookie, совпадающие с доменом/узлом и именем, соответствуют политике независимо от пути (правило подстановочного знака).<br><br>Если путь указан, это должно быть точное совпадение.<br>Если файл cookie соответствует правилу с путем, оно имеет приоритет над правилом без пути. |

#### <a name="sharing-example"></a>Пример отправки

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## <a name="see-also"></a>См. также

- [Сведения о режиме IE](./edge-ie-mode.md)
- [Сведения о настраиваемых сайтах](./edge-learnmore-configurable-sites-ie-mode.md)
- [Дополнительные сведения о режиме предприятия](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)