---
title: Что такое режим Internet Explorer?
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 08/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Узнайте, как режим Internet Explorer в Microsoft Edge предоставляет доступ к сайтам, которым требуется Internet Explorer 11, а также доступ к современным сайтам.
ms.openlocfilehash: a426d9bd9d2ac3d81682e9fc2304e9e90d3461f8
ms.sourcegitcommit: 4442aa94d4ff2fef8dd6f389ec0c6823b150d04f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2021
ms.locfileid: "12053328"
---
# <a name="what-is-internet-explorer-ie-mode"></a>Что такое режим Internet Explorer (IE)?

>[!Note]
> Поддержка классических приложений Internet Explorer 11 будет прекращена и больше не будет поддерживаться 15 июня 2022 г. (список области применения см. в [часто задаваемых вопросах](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). Те же приложения и сайты IE11, которые вы используете сегодня, можно открывать в Microsoft Edge в режиме Internet Explorer. 
            [Более подробную информацию см. здесь.](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)
          

Мы создали режим Internet Explorer (IE) в Microsoft Edge для организаций, которые по-прежнему нуждаются в Internet Explorer 11 для обеспечения обратной совместимости с существующими веб-сайтами, но также нуждаются в современном браузере. Эта функция упрощает использование в организациях одного браузера: для устаревших веб-страниц и приложений или для современных веб-страниц и приложений. В этой статье представлены начальные сведения по использованию Microsoft Edge в режиме IE.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## <a name="what-is-ie-mode"></a>Что такое режим IE?

Режим IE в Microsoft Edge упрощает использование всех нужных организации сайтов в одном браузере. В нем используется интегрированный модуль Chromium для современных сайтов и модуль Trident MSHTML из Internet Explorer 11 (IE11) для устаревших сайтов.

Когда сайт загружается в режиме IE, индикатор логотипа Internet Explorer отображается в левой части панели навигации. Вы можете щелкнуть индикатор логотипа Internet Explorer, чтобы отобразить дополнительные сведения, как показано ниже:

  ![Индикатор логотипа IE](./media/ie-mode/ie-logo-indicator1.png)

Только специально настроенные (с помощью политики) сайты будут использовать режим IE. Все остальные сайты будут отображаться в виде современных веб-сайтов. Чтобы сайт применял режим IE, выполните одно из указанных ниже действий.

- Укажите сайт в XML-файле списка сайтов в режиме предприятия, определенном в одной из следующих политик:
  - Microsoft Edge 78 или более поздней версии, "Настройка списка сайтов в режиме предприятия"
  - Internet Explorer "Использование списка веб-сайтов IE в режиме предприятия"
  > [!NOTE]
  > Мы обрабатываем только один список сайтов в режиме предприятия. Политика списка сайтов Microsoft Edge имеет приоритет над политикой списка сайтов Internet Explorer.
- Настройте групповую политику **Отправить все сайты интрасети в Internet Explorer** и присвойте ей значение **Включено** (Microsoft Edge 77 или более поздней версии).

### <a name="ie-mode-supports-the-following-internet-explorer-functionality"></a>Режим IE поддерживает следующие функциональные возможности Internet Explorer

- Все режимы работы с документами и режимы предприятия
- Элементы ActiveX (например, Java или Silverlight) 
            **Примечание**: Silverlight [прекратит получать поддержку](https://support.microsoft.com/windows/silverlight-end-of-support-0a3be3c7-bead-e203-2dfd-74f0a64f1788) 12 октября 2021 г. 
- Вспомогательные объекты браузера 
- Параметры и групповые политики Internet Explorer, влияющие на параметры зон безопасности и защищенный режим
- Средства разработчика F12 для IE при запуске с [IEChooser](/deployedge/edge-ie-mode-faq#how-can-i-debug-my-legacy-application-while-using-ie-mode-on-microsoft-edge-)
- Расширения Microsoft Edge (расширения, взаимодействующие непосредственно с содержимым страницы IE, не поддерживаются).

### <a name="ie-mode-doesnt-support-the-following-internet-explorer-functionality"></a>Режим IE не поддерживает следующие функциональные возможности Internet Explorer

- Панели инструментов Internet Explorer
- Параметры Internet Explorer и групповые политики, которые контролируют меню навигации.
- Средства разработчика F12 для IE11 или Microsoft Edge

## <a name="prerequisites"></a>Предварительные условия

Для использования Microsoft Edge в режиме IE должны быть соблюдены следующие условия.

> [!IMPORTANT]
> Чтобы обеспечить успешную работу, установите последние обновления для Windows и Microsoft Edge. В противном случае может произойти сбой в режиме IE.

1. Минимальные системные обновления для операционных систем приводятся в таблице ниже.

 | Операционная система | Версия       | Обновления |
 |------------------|---------------|---------|
 | Windows 10;       | 1909 или более поздней версии |         |
 | Windows 10;       | 1903          | 
            [KB4501375](https://support.microsoft.com/help/4501375/windows-10-update-kb4501375) или более поздней версии |
 | Windows Server   | 1903          | 
            [KB4501375](https://support.microsoft.com/help/4501375/windows-10-update-kb4501375) или более поздней версии |
 | Windows 10;       | 1809          | 
            [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) или более поздней версии |
 | Windows Server   | 1809          | 
            [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) или более поздней версии |
 | Windows Server   | 2019          | 
            [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) или более поздней версии |
 | Windows 10;       | 1803          | 
            [KB4512509](https://support.microsoft.com/help/4512509/windows-10-update-kb4512509) или более поздней версии |
 | Windows 10;       | 1709          | 
            [KB4512494](https://support.microsoft.com/help/4512494/windows-10-update-kb4512494) или более поздней версии |
 | Windows 10;       | 1607          | 
            [KB4516061](https://support.microsoft.com/help/4516061/windows-10-update-kb4516061) или более поздней версии |
 | Windows Server   | 2016          | 
            [KB4516061](https://support.microsoft.com/help/4516061/windows-10-update-kb4516061) или более поздней версии |
 | Windows 10;       | первоначальная версия, июль 2015 г. | 
            [KB4520011](https://support.microsoft.com/help/4520011/windows-10-update-kb4520011) или более поздней версии |
 | Windows 8       | 8.1              | 
            [KB4507463](https://support.microsoft.com/help/4507463/july-16-2019-kb4507463-os-build-preview-of-monthly-rollup) или более поздней версии либо [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) или более поздней версии |
 | Windows Server   | 2012 R2       | 
            [KB4507463](https://support.microsoft.com/help/4507463/july-16-2019-kb4507463-os-build-preview-of-monthly-rollup) или более поздней версии либо [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) или более поздней версии |
 | Windows 8  | Встроенный            | Установите [KB4492872](https://support.microsoft.com/help/4492872/update-for-internet-explorer-april-16-2019), чтобы перейти на Internet Explorer 11; затем установите [KB4507447](https://support.microsoft.com/help/4507447/windows-server-2012-update-kb4507447) или более поздней версии либо [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) или более поздней версии |
 | Windows Server   | 2012           | Установите [KB4492872](https://support.microsoft.com/help/4492872/update-for-internet-explorer-april-16-2019), чтобы перейти на Internet Explorer 11; затем установите [KB4507447](https://support.microsoft.com/help/4507447/windows-server-2012-update-kb4507447) или более поздней версии либо [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) или более поздней версии |
 | Windows 7;        |  с пакетом обновления 1 (SP1)**        | 
            [KB4507437](https://support.microsoft.com/help/4507437/windows-7-update-kb4507437) или более поздней версии либо [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) или более поздней версии |
 | Windows Server   |  2008 R2**    | 
            [KB4507437](https://support.microsoft.com/help/4507437/windows-7-update-kb4507437) или более поздней версии либо [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) или более поздней версии |
  > [!IMPORTANT]
  > ** Microsoft Edge будет поддерживать Windows 7 и Windows Server 2008 R2 даже после прекращения поддержки этих операционных систем. Для поддержки режима IE в указанных операционных системах на устройствах должны быть установлены [расширенные обновления системы безопасности для Windows 7](https://support.microsoft.com/help/4527878/faq-about-extended-security-updates-for-windows-7). Рекомендуется как можно скорее перейти на поддерживаемую операционную систему, чтобы обеспечить безопасность. Поддержку Microsoft Edge с расширенными обновлениями системы безопасности следует считать временным явлением при переходе на поддерживаемую ОС.

2. Административный шаблон Microsoft Edge. Дополнительные сведения см. в разделе [Настройка Microsoft Edge](./configure-microsoft-edge.md).
3. Internet Explorer 11 включен в компонентах Windows.

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Дополнительные сведения о режиме предприятия](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
