---
title: Стратегия настройки корпоративных сайтов
ms.author: shisub
author: shisub
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Пошаговое руководство по настройке списка сайтов в режиме предприятия для режима Internet Explorer.
ms.openlocfilehash: 72de393a5da0b4b0e2950951ae527f6ef870e110
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979893"
---
# <a name="enterprise-site-configuration-strategy"></a>Стратегия настройки корпоративных сайтов

>[!Note]
> Поддержка классических приложений Internet Explorer 11 будет прекращена и больше не будет поддерживаться 15 июня 2022 г. (список области применения см. в [часто задаваемых вопросах](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Те же приложения и сайты IE11, которые вы используете сегодня, можно открывать в Microsoft Edge в режиме Internet Explorer. [Более подробную информацию см. здесь.](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)

В этой статье описываются изменения, внесенные в список сайтов в режиме предприятия для поддержки режима Internet Explorer в Microsoft Edge версии 77 или более поздней.

Дополнительные сведения о схеме для XML-файла списка сайтов в режиме предприятия см. в статье [Руководство по схеме режима предприятия версии 2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.
<!--
## Updated schema elements

The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:

| **Element** | **Description** |
| --- | --- |
| \<open-in app="**true**"\> | A child element that controls what browser is used for sites. This element is required for sites that need to **open in IE11**.|

**Example:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

The following table shows the possible values of the \<open-in\> element:

| **Value** | **Description** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Opens the site in IE mode or a full IE11 window. To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Opens the site in a full IE11 window |
| **\<open-in\>MSEdge\</open-in\>** | Opens the site in Microsoft Edge |
| **\<open-in\>None or not specified\</open-in\>** | Opens the site in the default browser or in the browser where the user navigated to the site. |
|**\<open-in\>Configurable\</open-in\>** | Allows the site to participate in IE mode engine determination. To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_. Adding it to the other 'open-in' elements won't change browser behavior.   -->

## <a name="configuration-strategy"></a>Стратегия настройки

В стратегию настройки сайтов для режима IE входят следующие действия:
1. Подготовка списка сайтов
2. Настройка нейтральных сайтов
3. (Необязательно) Использование общего доступа к файлам cookie при необходимости

<!--
Step 1.  – if you don’t have one use Site Discovery Step-by-Step
Step 2 – Neutral sites + sticky mode
        Use more examples and explain sticky mode better
Step 3 – If that doesn’t cover your needs, then use Cookie sharing -->

## <a name="prepare-your-site-list"></a>Подготовка списка сайтов

Если у вас уже есть список сайтов в режиме предприятия для IE11 или устаревшей версии Microsoft Edge, его можно использовать повторно для настройки режима IE.

Если у вас нет списка сайтов, для его заполнения можно использовать [средство обнаружения корпоративных сайтов](/deployedge/edge-ie-mode-site-discovery).

## <a name="configure-neutral-sites"></a>Настройка нейтральных сайтов

Чтобы режим IE работал правильно, требуется явным образом настроить серверы проверки подлинности и единого входа в качестве нейтральных сайтов. В противном случае страницы в режиме IE попытаются выполнить перенаправление в Microsoft Edge, и проверка подлинности завершится сбоем.

Нейтральный сайт будет использовать браузер, в котором начат переход: Microsoft Edge или режим IE. Настройка нейтральных сайтов гарантирует, что все приложения, использующие эти серверы проверки подлинности (современные и устаревшие), продолжат работать.

Вы можете настроить нейтральные сайты, выбрав "Нет" в раскрывающемся списке *Открыть в* инструмента Enterprise Mode Site List Manager или непосредственно обновив XML-файл списка сайтов:

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

Чтобы определить серверы проверки подлинности, проверьте трафик из приложения с помощью средств разработчика IE11. Если вам требуется больше времени, чтобы определить серверы проверки подлинности, можно настроить политику, сохраняющую все переходы в пределах страницы в режиме IE, чтобы пользователи могли продолжать свои рабочие процессы без перерывов. При необходимости отключите этот параметр после определения и добавления серверов проверки подлинности в список сайтов, чтобы свести к минимуму использование режима IE. Дополнительные сведения см. в разделе [Сохранение переходов в пределах страницы в режиме IE](/deployedge/edge-learnmore-inpage-nav).

>[!NOTE]
   >Схема режима предприятия версии 1 не поддерживается для интеграции с режимом IE. Если вы используете схему версии 1 в Internet Explorer 11, необходимо обновить схему до версии 2. Дополнительные сведения см. в разделе [Руководство по схеме режима предприятия версии 2](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

## <a name="optional-use-cookie-sharing-if-necessary"></a>(Необязательно) Использование общего доступа к файлам cookie при необходимости

По умолчанию процессы Microsoft Edge и Internet Explorer не делятся файлами cookie сеансов, и в некоторых случаях при использовании режима IE это может быть неудобно. Например, если пользователю необходимо выполнить повторную проверку подлинности в режиме IE и он уже привык это делать или если при выходе из сеанса Microsoft Edge он не выходит из сеанса в режиме Internet Explorer для выполнения критически важных транзакций. В таких сценариях вы можете настроить определенный набор файлов cookie (с помощью единого входа) для отправки из Microsoft Edge в Internet Explorer, чтобы проверка подлинности выполнялась проще благодаря устранению необходимости в повторной проверке. Дополнительные сведения см. в разделе [Отправка файлов cookie из Microsoft Edge в Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Сведения о режиме IE](./edge-ie-mode.md)
- [Дополнительные сведения о режиме предприятия](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
