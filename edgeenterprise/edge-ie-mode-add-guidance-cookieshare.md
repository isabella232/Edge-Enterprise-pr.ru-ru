---
title: Обмен файлами cookie между Microsoft Edge и Internet Explorer
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/08/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Узнайте, как совместно использовать файлы cookie между Microsoft Edge и Internet Explorer
ms.openlocfilehash: 403404c96b91cde62e714324864b87ff2e57f8db
ms.sourcegitcommit: dd8cdbd35726c795ddce917e549ddf17ee7f5290
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/11/2022
ms.locfileid: "12473418"
---
# <a name="cookie-sharing-between-microsoft-edge-and-internet-explorer"></a>Обмен файлами cookie между Microsoft Edge и Internet Explorer

>[!Note]
> 15 июня 2022 г. поддержка классических приложений Internet Explorer (IE) 11 будет прекращена. Чтобы узнать, что находится в области действия и вне ее, когда IE 11 прекращает работу, см. часто задаваемые вопросы о прекращении поддержки классических приложений [Internet Explorer 11](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549). Те же приложения и сайты IE 11, которые вы используете сегодня, Microsoft Edge в режиме Internet Explorer. Дополнительные сведения см. [в статье о будущем Internet Explorer Windows 10 в Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

В этой статье объясняется, как настроить общий доступ к файлам cookie сеанса между Microsoft Edge процессом и процессом Internet Explorer при использовании режима Internet Explorer.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 87 или более поздней.

## <a name="prerequisites"></a>Предварительные условия

Чтобы поделиться файлами cookie сеанса из Microsoft Edge в Internet Explorer:

- Обновления Windows

  - Windows 11
  - Windows 10 версии 2004, Windows Server версии 2004 — KB4571744 и выше
  - Windows 10 версии 1909, Windows Server версии 1909 — KB4566116 и выше
  - Windows 10 версии 1903, Windows Server версии 1903 — KB4566116 и выше
  - Windows 10, версии 1809, Windows Server версии 1809 и Windows Server 2019 — KB4571748 и выше
  - Windows 10 версии 1803 — KB4577032 и выше
  - Windows 10 Корпоративная LTSC 2016 и Windows Server 2016 — KB4580346 или более поздней версии
  - Windows 10 Корпоративная 2015 с долгосрочным обслуживанием — KB4580327 или более поздней версии
  - Windows 8.1 и Windows Server 2012 R2 — KB4586768 или более поздней версии
  - Windows 10 Корпоративная LTSC 2016 и Windows Server 2016 — KB4580346 или более поздней версии
  - Windows 10 Корпоративная 2015 с долгосрочным обслуживанием — KB4580327 или более поздней версии
  - Windows 8.1 и Windows Server 2012 R2 — KB4586768 или более поздней версии
- Microsoft Edge версии 87 или более поздней
- [Режим IE,](./edge-ie-mode.md) настроенный с помощью списка сайтов в режиме предприятия

Чтобы совместно использовать файлы cookie сеанса между Microsoft Edge и Internet Explorer:

- Обновления Windows
  
  - Windows 11 — KB5010414 или более поздней версии
  - Windows Server 2022 — KB5010421 или более поздней версии
  - Windows 10 версии 20H2 — KB5010415 или более поздней
  - Windows 10 версии 21H1 — KB5010415 или более поздней
  - Windows 10 версии 21H2— KB5010415 или более поздней
- Microsoft Edge версии 99 или более поздней
- [Режим IE,](./edge-ie-mode.md) настроенный с помощью списка сайтов в режиме предприятия

## <a name="overview"></a>Обзор

Распространенной конфигурацией в крупных организациях является наличие приложения, работающего на основе связи современного браузера с другим приложением, которое может быть настроено на открытие в режиме Internet Explorer с поддержкой единого входа (SSO) в рамках рабочего процесса.

По умолчанию процессы Microsoft Edge и Internet Explorer не совместно используют файлы cookie сеанса, и в некоторых случаях такое отсутствие общего доступа может быть неудобно. Например, если пользователю необходимо повторно выполнить аутентификацию в режиме Internet Explorer или при выходе из сеанса Microsoft Edge не выход из сеанса режима Internet Explorer. В таких сценариях вы можете настроить определенный набор файлов cookie (с помощью единого входа) для отправки из Microsoft Edge в Internet Explorer, чтобы проверка подлинности выполнялась проще благодаря устранению необходимости в повторной проверке.

> [!NOTE]
> Перед Microsoft Edge версии 99 файлы cookie сеанса можно использовать только из Microsoft Edge Internet Explorer. Начиная с Microsoft Edge версии 99, общий доступ к файлам cookie сеанса в обратном режиме (из Internet Explorer в Microsoft Edge) возможен.

## <a name="how-cookie-sharing-works"></a>Как работает отправка файлов cookie

XML Enterprise списка сайтов в режиме интеграции расширяется, позволяя большему набору элементов указывать файлы cookie сеанса, которые должны совместно использоваться Microsoft Edge Internet Explorer.

При первом создании вкладки режима Internet Explorer в сеансе Microsoft Edge все соответствующие файлы cookie становятся общими для сеанса Internet Explorer. После этого каждый раз, когда файл cookie, соответствующий правилу, добавляется, удаляется или изменен, он отправляется как обновление в сеанс Internet Explorer. Набор общих файлов cookie также повторно оценивается при обновлении списка сайтов.

### <a name="updated-schema-elements"></a>Обновленные элементы схемы

В таблице ниже описан элемент \<shared-cookie\>, добавленный для поддержки функции отправки файлов cookie.

| Элемент| Описание |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br>ИЛИ<br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |**(Обязательно)** Элемент \<shared-cookie\> требует как минимум атрибут *domain* (для файлов cookie домена) или *host* (для файлов cookie, предназначенных только для узла) и атрибут *name*.<br>Эти атрибуты должны точно соответствовать домену и имени файла cookie соответственно. **Обратите внимание**, что поддомены не совпадают.<br><br>Атрибут *domain* используется для файлов cookie домена (начальная точка разрешена, но необязательна).<br>Атрибут *host* используется только для файлов cookie, предназначенных для узла (начальная точка является ошибкой). Указание обоих аргументов (или их отсутствие) приведет к ошибке.<br>* Файл cookie — это файл cookie домена, если домен был указан в строке файла cookie (с помощью HTTP-заголовка отклика Set-cookie или API JS document.cookie). Файл cookie домена применяется к указанному домену и всем поддоменам. Если домен не указан в строке файла cookie, файл cookie является файлом cookie только для узла и применяется только к определенному узлу, для которого он был задан. Некоторые классы URL-адресов, такие как имена узлов с одним словом (например, http://intranetsite) и IP-адреса) (например, http://10.0.0.1) могут задавать только файлы cookie только для узла).    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | **(Необязательно)** Можно указать атрибут *path*. Если атрибут path не указан (или атрибут path не заполнен), все файлы cookie, совпадающие с доменом/узлом и именем, соответствуют политике независимо от пути (правило подстановочного знака).<br><br>Если путь указан, это должно быть точное совпадение.<br>Если файл cookie соответствует правилу с путем, оно имеет приоритет над правилом без пути. |
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1" **source-engine**="MSEdge"\>\</shared-cookie\><br><br>ИЛИ<br><br>\<shared-cookie **domain**=".contoso.com" **name**="cookie1" **source-engine**="IE11"\>\</shared-cookie\><br><br>ИЛИ<br><br>\<shared-cookie **domain**=".contoso.com" **name**="cookie1" **source-engine**="Both"\>\</shared-cookie\> | **(Необязательно)** Атрибут исходного модуля указывает, как файлы cookie сеанса совместно используются Microsoft Edge и Internet Explorer. Где:<br><br>- **MSEdge**. Совместное использование файлов cookie сеанса Microsoft Edge в Internet Explorer.<br>- **IE11**.  Совместное использование файлов cookie сеанса из Internet Explorer в Microsoft Edge.<br>- **И то, и другое**. Совместное использование файлов cookie сеанса в Microsoft Edge и Internet Explorer.<br>- **Значение по умолчанию или не указано**. Файлы cookie сеанса будут совместно использоваться из Microsoft Edge в Internet Explorer. |

#### <a name="sharing-example"></a>Пример отправки

```xml
<site-list version="1"> 
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie>  
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c"> 
</shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie3" source-engine="MSEdge"></shared-cookie> 
</site-list> 
```

## <a name="see-also"></a>См. также

- [Сведения о режиме IE](./edge-ie-mode.md)
- [Сведения о настраиваемых сайтах](./edge-learnmore-configurable-sites-ie-mode.md)
- [Дополнительные сведения о режиме предприятия](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
