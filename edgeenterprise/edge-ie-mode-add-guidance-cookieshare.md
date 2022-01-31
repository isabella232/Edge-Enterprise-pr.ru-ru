---
title: Отправка файлов cookie из Microsoft Edge в Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/04/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Узнайте, как обмениваться файлами cookie из Microsoft Edge internet Explorer
ms.openlocfilehash: ddd8cb519f2cb22cf238f96d144197a623eb18bc
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2022
ms.locfileid: "12298127"
---
# <a name="cookie-sharing-from-microsoft-edge-to-internet-explorer"></a>Отправка файлов cookie из Microsoft Edge в Internet Explorer

>[!Note]
> 15 июня 2022 г. настольное приложение Internet Explorer (IE) 11 будет отменено и не будет поддерживаться. Чтобы узнать, что имеется в области и выходит за рамки, когда IE 11 будет снят с работы, см. в faQ для настольных приложений [Internet Explorer 11.](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549) Те же приложения и сайты IE 11, которые вы используете сегодня, могут открываться Microsoft Edge режиме Internet Explorer. Дополнительные дополнительные информации см. в Windows 10 Обозреватель интернета [в Microsoft Edge.](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)

В этой статье рассказывается о настройке общего доступа к файлам cookie сеанса из процесса Microsoft Edge в процесс Internet Explorer при использовании режима Internet Explorer.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 87 или более поздней.

## <a name="prerequisites"></a>Предварительные условия

- Обновления Windows

  - Windows 10 версии 2004, Windows Server версии 2004 — KB4571744 и выше
  - Windows 10 версии 1909, Windows Server версии 1909 — KB4566116 и выше
  - Windows 10 версии 1903, Windows Server версии 1903 — KB4566116 и выше
  - Windows 10, версии 1809, Windows Server версии 1809 и Windows Server 2019 — KB4571748 и выше
  - Windows 10 версии 1803 — KB4577032 и выше
  - Windows 10 Корпоративная LTSC и Windows Server 2016 - KB4580346 или выше
  - Windows 10 Корпоративная 2015 с долгосрочным обслуживанием - KB4580327 или выше
  - Windows 8.1 и Windows Server 2012 R2 - KB4586768 или выше
  - Windows 10 Корпоративная LTSC и Windows Server 2016 - KB4580346 или выше
  - Windows 10 Корпоративная 2015 с долгосрочным обслуживанием - KB4580327 или выше
  - Windows 8.1 и Windows Server 2012 R2 - KB4586768 или выше

- Microsoft Edge версии 87 или более поздней
- [Режим IE,](./edge-ie-mode.md) настроенный с помощью списка сайтов в режиме предприятия

## <a name="overview"></a>Обзор

Распространенной конфигурацией в крупных организациях является наличие приложения, работающего на основе связи современного браузера с другим приложением, которое может быть настроено на открытие в режиме Internet Explorer с поддержкой единого входа (SSO) в рамках рабочего процесса.

По умолчанию процессы Microsoft Edge и Internet Explorer не имеют общего доступа к файлам cookie сеанса, и в некоторых случаях такое отсутствие общего доступа может быть неудобным. Например, если пользователю необходимо повторно проверить в режиме Internet Explorer или при выходе из сеанса Microsoft Edge не выходит из сеанса internet Explorer. В таких сценариях вы можете настроить определенный набор файлов cookie (с помощью единого входа) для отправки из Microsoft Edge в Internet Explorer, чтобы проверка подлинности выполнялась проще благодаря устранению необходимости в повторной проверке.

> [!NOTE]
> Файлы cookie сеанса можно отправлять только из Microsoft Edge в Internet Explorer. Отправка файлов cookie в обратном направлении (из Internet Explorer в Microsoft Edge) невозможна.

## <a name="how-cookie-sharing-works"></a>Как работает отправка файлов cookie

XML списка Enterprise mode расширен, чтобы разрешить дополнительным элементам указывать файлы cookie, которые необходимо использовать в сеансе Microsoft Edge Internet Explorer.  

При первом создании вкладки режима Internet Explorer в сеансе Microsoft Edge все соответствующие файлы cookie становятся общими для сеанса Internet Explorer. После этого файл cookie, который соответствует правилу, добавляется, удаляется или видоизменяется, он отправляется в качестве обновления для сеанса Internet Explorer. Набор общих файлов cookie также обновляется при обновлении списка сайтов.

### <a name="updated-schema-elements"></a>Обновленные элементы схемы

В таблице ниже описан элемент \<shared-cookie\>, добавленный для поддержки функции отправки файлов cookie.

| Элемент| Описание |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br>ИЛИ<br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |**(Обязательно)** Элемент \<shared-cookie\> требует как минимум атрибут *domain* (для файлов cookie домена) или *host* (для файлов cookie, предназначенных только для узла) и атрибут *name*.<br>Эти атрибуты должны точно совпадать с доменом и именем cookie соответственно. **Обратите внимание**, что поддомены не совпадают.<br><br>Атрибут *domain* используется для файлов cookie домена (начальная точка разрешена, но необязательна).<br>Атрибут *host* используется только для файлов cookie, предназначенных для узла (начальная точка является ошибкой). Указание обоих аргументов (или их отсутствие) приведет к ошибке.<br>* Файл cookie — это файл cookie домена, если домен был указан в строке файла cookie (с помощью HTTP-заголовка отклика Set-cookie или API JS document.cookie). Файл cookie домена применяется к указанному домену и всем поддоменам. Если домен не указан в строке cookie, cookie является cookie только для хостов и применяется только к определенному хосту, для который он был задан. В некоторых классах URL-адресов, таких как одно слово hostnames (например, и IP-адреса (например, можно установить только файлы cookie только для http://intranetsite) http://10.0.0.1) хостов).    |
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
