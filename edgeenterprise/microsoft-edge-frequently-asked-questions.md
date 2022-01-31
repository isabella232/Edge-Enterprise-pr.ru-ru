---
title: Часто задаваемые вопросы (часто задаваемые вопросы) о Microsoft Edge на предприятии
ms.author: collw
author: dan-wesley
manager: seanlynd
ms.date: 01/11/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Часто задаваемые вопросы (часто задаваемые вопросы) о Microsoft Edge на предприятии
ms.openlocfilehash: 86f1fdee4697d8087014e35daf41b600eeb62471
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2022
ms.locfileid: "12298325"
---
# <a name="microsoft-edge-frequently-asked-questions"></a>Microsoft Edge часто задают вопросы

В этой статье содержатся часто задаваемые вопросы (часто задаваемые вопросы) Microsoft Edge на предприятии.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## <a name="how-do-i-know-which-version-of-microsoft-edge-i-have"></a>Как узнать используемую версию Microsoft Edge?

Выберите значок эллипсов **(...)** в правом верхнем углу Microsoft Edge, а затем **Параметры**. Выберите **Сведения о Microsoft Edge**, чтобы просмотреть свою версию Microsoft Edge.

## <a name="what-about-internet-explorer-11"></a>Как насчет Internet Explorer 11?

15 июня 2022 г. настольное приложение Internet Explorer 11 будет снято с службы поддержки. Чтобы узнать, что имеется в области, см. в Windows 10 Обозреватель Интернета [в Microsoft Edge.](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/) Те же приложения и сайты IE11, которые вы используете сегодня, можно открывать в Microsoft Edge в режиме Internet Explorer. Дополнительные сведения см. в [веб-сайте Internet Explorer 11 desktop app retirement FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549).

## <a name="does-microsoft-edge-support-activex-controls-or-browser-helper-objects-like-silverlight-or-java"></a>Поддерживает Microsoft Edge элементы ActiveX или объекты помощника браузера, такие как Silverlight или Java?

Нет. Microsoft Edge не поддерживает элементы управления ActiveX или объекты поддержки браузера (BHOs), такие как Silverlight или Java. Однако при запуске веб-приложений, в которых используются ActiveX, BHOs или устаревшие режимы документов в Internet Explorer 11, их можно настроить для работы в режиме IE на Microsoft Edge. Дополнительные сведения см. в статье [Настройка режима IE в Microsoft Edge](./edge-ie-mode.md).

## <a name="will-favorites-be-ported-over-from-the-current-version-of-microsoft-edge-or-will-i-have-to-re-add-them"></a>Будут ли перенастрояться избранное из текущей версии Microsoft Edge или мне придется их повторно добавлять?

Microsoft Edge поддерживает импорт из существующих установок Microsoft Edge, Chrome, Internet Explorer и Firefox (на Win10). Для импорта поддерживаются следующие параметры: Bookmarks, History, Passwords и Autofill (платежи, адреса и общие формы). Вы можете импортировать данные во время первого запуска или из параметров браузера.

## <a name="whats-the-difference-between-the-stable-beta-dev-and-canary-channelsbuilds"></a>В чем разница между каналами и сборками Stable, Beta, Dev и Canary?

Стабильный канал Microsoft Edge является самым стабильным каналом, который мы предлагаем [](https://aka.ms/EdgeEnterprise) с корпоративными функциями, готовыми для пилотирования и оценки по всей организации. Канал Beta позволяет проверить следующий выпуск Stable с участием показательной выборки пользователей. Стабильные и бета-каналы обновляются примерно каждые шесть недель. Каналы Dev и Canary продолжают обновляться еженедельно и ежедневно соответственно. Автономные установщики (MSIs и PKG-файлы) доступны только для каналов Stable, Beta и Dev. Дополнительные сведения см. в разделе [Обзор каналов Microsoft Edge](./microsoft-edge-channels.md).

## <a name="what-kind-of-extension-support-do-i-have-with-microsoft-edge"></a>Какая поддержка расширения у меня с Microsoft Edge?

Microsoft Edge поддерживает расширения из [Microsoft Edge и](https://go.microsoft.com/fwlink/?linkid=2081222) [интернет-магазин Chrome.](https://go.microsoft.com/fwlink/?linkid=2072338)

## <a name="do-you-support-mobile-device-management-mdm-and-microsoft-intune"></a>Есть ли поддержка средств управления мобильными устройствами (MDM) и Microsoft Intune?

Да. Теперь поддерживается настройка Microsoft Edge в Windows 10 с помощью Microsoft Intune и средств управления мобильными устройствами (MDM). Дополнительные сведения см. в разделе [Настройка Microsoft Edge с помощью Microsoft Intune](./configure-edge-with-intune.md) и [Настройка Microsoft Edge с помощью средств управления мобильными устройствами](./configure-edge-with-mdm.md).

## <a name="does-windows-server-update-services-wsus-support-the-initial-deployment-of-microsoft-edge"></a>Поддерживает Windows Server Update Services (WSUS) начальное развертывание Microsoft Edge?

Да. В каталоге обновлений [Майкрософт](https://www.catalog.update.microsoft.com/Search.aspx?q=the%20new%20microsoft%20edge%20for%20windows) есть пакеты, которые можно использовать для начального развертывания Microsoft Edge через WSUS. После первоначального развертывания по умолчанию настраиваются автоматические обновления. Подробнее см. [Обновление в WSUS для нового браузера Microsoft Edge для Windows 10 версий 1809, 1903, 1909 и 2004: 29октября 2020г](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge).

 Ручное обновление можно сделать с помощью средства управления конфигурацией, например [ConfigMgr.](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)

## <a name="are-initial-preferences-supported"></a>Поддерживаются ли начальные предпочтения?

Да. Дополнительные сведения см. в [Microsoft Edge Параметры начальных предпочтений для первого запуска](./initial-preferences-support-on-microsoft-edge-browser.md)

## <a name="see-also"></a>См. также

- [Целевая страница с документацией по Microsoft Edge Enterprise](./index.yml)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
  