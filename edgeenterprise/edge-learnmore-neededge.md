---
title: Перенаправление из Internet Explorer в Microsoft Edge для обеспечения совместимости с современными веб-сайтами
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 11/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Перенаправление из Internet Explorer в Microsoft Edge для обеспечения совместимости с современными веб-сайтами
ms.openlocfilehash: 7cd74eda6d8ada7647862ea69f77a982713f0c14
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617299"
---
# <a name="redirection-from-internet-explorer-to-microsoft-edge-for-compatibility-with-modern-web-sites"></a>Перенаправление из Internet Explorer в Microsoft Edge для обеспечения совместимости с современными веб-сайтами

> [!NOTE]
> Эта статья относится к Microsoft Edge из стабильного канала версии 87 или более поздней.

## <a name="overview"></a>Обзор

>[!Note]
> Поддержка классических приложений Internet Explorer 11 будет прекращена и больше не будет поддерживаться 15 июня 2022 г. (список области применения см. в [часто задаваемых вопросах](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Те же приложения и сайты IE11, которые вы используете сегодня, можно открывать в Microsoft Edge в режиме Internet Explorer. [Более подробную информацию см. здесь.](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)

Дизайн многих современных веб-сайтов несовместим с Internet Explorer. Когда пользователь Internet Explorer посещает несовместимый общедоступный сайт, для него отображается сообщение о том, что сайт несовместим с браузером и требуется вручную переключиться на другой браузер.

Необходимость ручного переключения на другой браузер изменяется с Microsoft Edge стабильного канала версии 87.

Когда пользователь переходит на сайт, несовместимый с Internet Explorer, он автоматически перенаправляется в Microsoft Edge. В этой статье описан пользовательский интерфейс перенаправления и групповые политики, которые используются для настройки или отключения автоматического перенаправления.

> [!NOTE]
> Корпорация Майкрософт поддерживает список всех сайтов, о которых известно, что они несовместимы с Internet Explorer. Дополнительные сведения см. в статье [Запрос на обновление списка несовместимых сайтов](/microsoft-edge/web-platform/ie-to-microsoft-edge-redirection#request-an-update-to-the-ie-compatibility-list)

## <a name="prerequisites"></a>Предварительные условия
- Microsoft Edge Stable версии 87 или более поздней
- Версии Windows
    - Windows10 версии1709 или более поздней
    - Windows 8.1
    - Windows 7



## <a name="redirection-experience"></a>Интерфейс перенаправления

При перенаправлении в Microsoft Edge пользователям однократно демонстрируется диалоговое окно, как на следующем снимке экрана. В этом диалоговом окне объясняется, почему выполняется перенаправление, и запрашивается согласие на копирование данных браузера и параметров из Internet Explorer в Microsoft Edge. Будут импортированы следующие данные браузера: избранное, пароли, поисковые системы, открытые вкладки, журнал, параметры, файлы cookie и домашняя страница.

![Уведомление браузера и запрос на импорт данных и настроек.](media/edge-learnmore-neededge/neededge-dialog1.png)

Даже если пользователь не предоставит согласие путем установки флажка "Всегда извлекать данные и параметры браузера из Internet Explorer", он может нажать  **Продолжить просмотр**  для продолжения сеанса.

В конце отображается баннер о несовместимости веб-сайта (показанный на следующем снимке экрана) под адресной строкой для каждого перенаправления.

![Уведомление о современных сайтах и предложение установить Microsoft Edge в качестве браузера, используемого по умолчанию, или ознакомиться с Microsoft Edge.](media/edge-learnmore-neededge/neededge-banner.png)

Баннер о несовместимости веб-сайта:

- рекомендует пользователю переключиться на Microsoft Edge
- предлагает сделать Microsoft Edge браузером, используемым по умолчанию
- дает пользователю возможность исследовать Microsoft Edge

При перенаправлении сайта из Internet Explorer в Microsoft Edge вкладка Internet Explorer, на которой началась загрузка сайта, закрывается, если для нее не предоставлено предварительное согласие. В противном случае представление активной вкладки переходит на страницу  [поддержки](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) Майкрософт, на которой объясняется, почему сайт перенаправлен в Microsoft Edge.

> [!NOTE]
> После перенаправления пользователи могут вернуться к использованию Internet Explorer для сайтов, которых нет в списке несовместимых с Internet Explorer.  

## <a name="policies-to-configure-redirection-to-microsoft-edge"></a>Политики для настройки перенаправления в Microsoft Edge

> [!NOTE]
> Эти политики будут доступны в виде обновлений ADMX-файла к 26 октября 2020 г. и будут доступны в Intune к 9 ноября 2020 г.

Чтобы включить автоматическое перенаправление в Microsoft Edge, требуется настроить три групповых политики. Вот эти политики:

- RedirectSitesFromInternetExplorerPreventBHOInstall
- RedirectSitesFromInternetExplorerRedirectMode
- HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

### <a name="policy-redirectsitesfrominternetexplorerpreventbhoinstall"></a>Политика: RedirectSitesFromInternetExplorerPreventBHOInstall

Для перенаправления из Internet Explorer в Microsoft Edge требуется вспомогательный объект браузера (BHO) Internet Explorer с именем "IEtoEdge BHO". Политика **RedirectSitesFromInternetExplorerPreventBHOInstall** определяет, устанавливается ли этот вспомогательный объект браузера.  

- Если эта политика включена, вспомогательный объект браузера, необходимый для перенаправления, не будет установлен, а для ваших пользователей по-прежнему будут отображаться сообщения о несовместимости для определенных веб-сайтов в Internet Explorer. Если вспомогательный объект браузера уже установлен, он будет удален при следующем обновлении стабильного канала Microsoft Edge.
- Если отключить или не настроить эту политику, вспомогательный объект браузера будет установлен. Такая реакция на события используется по умолчанию.

Помимо необходимости во вспомогательном объекте браузера существует зависимость от параметра **RedirectSitesFromInternetExplorerRedirectMode**, которому требуется присвоить значение "Перенаправлять сайты на основе списка несовместимых сайтов" или "Не настроено".

### <a name="policy-redirectsitesfrominternetexplorerredirectmode"></a>Политика: RedirectSitesFromInternetExplorerRedirectMode

 Эта политика соответствует параметру раздела **Браузер по умолчанию** в Microsoft Edge "Разрешить Internet Explorer открывать сайты в Microsoft Edge". Чтобы получить доступ к этому параметру, перейдите по URL-адресу *edge://settings/defaultbrowser*.  

- Если не настроить эту политику или присвоить ей значение Sitelist (Список сайтов), Internet Explorer будет перенаправлять несовместимые сайты в Microsoft Edge. Такая реакция на события используется по умолчанию.
- Чтобы отключить эту политику, выберите **Включено**, затем в раскрывающемся меню "Настройки: Перенаправление несовместимых сайтов из Internet Explorer в Microsoft Edge" выберите **Отключить**. В этом случае несовместимые сайты не перенаправляются в Microsoft Edge.

> [!NOTE]
> Если вы используете персональное устройство, не управляемое вашей организацией, в разделе **Обеспечение совместимости с Internet Explorer** вы увидите другой параметр с именем "Разрешить сайтам загрузку в режиме Internet Explorer".
>
>Если вы используете устройство, присоединенное к домену или зарегистрированное в службе управления мобильными устройствами (MDM), этот параметр не отображается.
>
> Если вместо этого вы хотите разрешить своим пользователям загружать сайты в режиме Internet Explorer, вы можете это сделать, настроив политику [Разрешить тестирование режима Internet Explorer](./microsoft-edge-policies.md#intranetredirectbehavior).

### <a name="policy-hideinternetexplorerredirectuxforincompatiblesitesenabled"></a>Политика: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

Эта политика настраивает пользовательский интерфейс для перенаправления несовместимых сайтов в Microsoft Edge.  

- Если эта политика включена, пользователям никогда не демонстрируется диалоговое окно однократного перенаправления и баннер перенаправления. Данные браузера и пользовательские параметры не импортируются.
- Если отключить или не настроить эту политику, диалоговое окно перенаправления будет отображаться при первом перенаправлении, а сохраненный баннер перенаправления будет отображаться для сеансов, начинающихся с перенаправления.

  > [!NOTE]
  > Данные браузера пользователя будут импортироваться при каждом выполнении перенаправления для пользователя. Однако это происходит только в том случае, если пользователь согласился на импорт в диалоговом окне однократного перенаправления.

## <a name="disable-redirection-to-microsoft-edge"></a>Отключение перенаправления в Microsoft Edge

Если вы хотите отключить перенаправление ДО обновления до Microsoft Edge версии 87 из стабильного канала, выполните следующее действие.

1. Присвойте политике **RedirectSitesFromInternetExplorerPreventBHOInstall** значение **Включено**.

Если вы хотите отключить перенаправление ПОСЛЕ обновления до Microsoft Edge версии 87 из стабильного канала, выполните следующие действия.

1. Установите для политики **RedirectSitesFromInternetExplorerRedirectMode** значение **Включено**, затем в раскрывающемся меню "Настройки: Перенаправление несовместимых сайтов из Internet Explorer в Microsoft Edge" выберите **Отключить**. Этот параметр прекратит перенаправление, как только политика вступит в силу.
2. Присвойте политике **RedirectSitesFromInternetExplorerPreventBHOInstall** значение **Включено**. Это приведет к удалению вспомогательного объекта браузера после следующего обновления Microsoft Edge.

## <a name="see-also"></a>См. также

- [Запрос на обновление списка несовместимых сайтов](/microsoft-edge/web-platform/ie-to-microsoft-edge-redirection#request-an-update-to-the-ie-compatibility-list)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Политики Microsoft Edge](./microsoft-edge-policies.md)