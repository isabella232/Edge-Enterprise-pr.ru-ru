---
title: Устранение неполадок режима IE и вопросы с ответами
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Устранение неполадок и вопросы с ответами для режима Internet Explorer в Microsoft Edge
ms.openlocfilehash: 651fc438e64c21e33787724fb3d5931f0f5b75fa
ms.sourcegitcommit: 4ec03873a85f065d9bfa6203cfe6c3e938f79bc5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2021
ms.locfileid: "12155153"
---
# <a name="internet-explorer-ie-mode-troubleshooting-and-faq"></a>Устранение неполадок в режиме Internet Explorer (IE) и ОТВЕТ

> [!NOTE]
> 15 июня 2022 г. настольное приложение Internet Explorer 11 будет снято с службы поддержки. Чтобы узнать список того, что имеется в области, см. в faq [internet Explorer 11 desktop app retirement.](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549) Те же приложения и сайты IE11, которые вы используете сегодня, можно открывать в Microsoft Edge в режиме Internet Explorer. Дополнительные дополнительные публикации см. в Windows 10 в Microsoft Edge Internet [Explorer.](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)

Данная статья содержит советы по устранению неполадок и ответы на часто задаваемые вопросы для Microsoft Edge версии 77 или более поздней.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## <a name="troubleshoot-ie-mode"></a>Режим устранения неполадок IE

Используйте сведения из этого раздела для диагностики и устранения проблем в режиме IE.

### <a name="internet-explorer-mode--general-diagnostic-information"></a>Общие диагностические сведения режима Internet Explorer

Диагностические сведения о режиме Internet Explorer можно получить на вкладке "Совместимость Microsoft Edge". Чтобы открыть ее, перейдите по адресу *edge://compat/iediagnostic*. Эта страница может отображать сообщения диагностики. Эта страница также содержит сведения о настройке для следующих категорий:

- **Проверка раздела реестра.** (Отображается, только если проверка не пройдена.) Проверяет правильность настройки интеграции Internet Explorer в реестре. Если нет, пользователь может выбрать **исправление проблемы.**
- **Режим Internet Explorer.** Отображает используемую версию API на основе конфигурации и ОС. При наличии проблемы пользователю может быть предложено установить Центр обновления Windows.
- **Настройка режима Internet Explorer.** Указывает, включен ли режим Internet Explorer и как он настроен.
- **Командная строка.** Показывает строку командной строки и переключатели, используемые для Microsoft Edge.
- **Параметры групповой политики.** Указывает, настроен ли режим IE с помощью групповых политик, и какие политики применяются.

### <a name="error-message-to-open-this-page-in-internet-explorer-mode-reinstall-microsoft-edge-with-administrator-privileges"></a>Сообщение об ошибке: "Чтобы открыть эту страницу в режиме Internet Explorer, переустановите Microsoft Edge с правами администратора".

Вы можете увидеть эту ошибку, если у вас нет всех необходимых Windows обновлений. Необходимые версии Windows и Microsoft Edge см. в предварительных условиях, перечисленных в статье [Сведения о режиме IE](./edge-ie-mode.md).

Если вы уже установили все необходимые Windows обновления, вы можете увидеть эту ошибку, если:

- Вы используете канал Canary, установленный на уровне пользователя по умолчанию.
- Вы используете канал Stable, Beta или Dev, но при установке уровня прав запрос на повышение уровня был отменен. При отмене запроса на повышение прав установка продолжается на уровне пользователя.
- Internet Explorer 11 отключен в компонентах Windows.

Возможные решения:

- Запустите установщик для любого канала на уровне системы: `installer.exe --system-level`.
- Включите Internet Explorer 11 в компонентах Windows.

Чтобы убедиться, что Microsoft Edge установлен на уровне системы, введите "edge://version" в адресной строке Microsoft Edge. Путь к исполняемому файлу будет начинаться с *C:\Program Files*, что указывает на установку на уровне системы. Если путь выполнения начинается с *C:\Users*, удалить, а затем Microsoft Edge с привилегиями администратора.

### <a name="error-message-to-open-this-page-in-ie-mode-try-restarting-microsoft-edge"></a>Сообщение об ошибке "Чтобы открыть эту страницу в режиме IE, попробуйте перезапустить Microsoft Edge".

Вы можете увидеть эту ошибку, если в Internet Explorer произошла неожиданная ошибка. Перезапуск Microsoft Edge обычно исправляет эту ошибку.

### <a name="error-message-turn-off-remote-debugging-to-open-this-site-in-ie-mode-otherwise-it-might-not-work-as-expected"></a>Сообщение об ошибке: "Отключите удаленную отладку, чтобы открыть этот сайт в режиме IE, в противном случае он может работать неправильно".

Эта ошибка может возникнуть при удаленной отладке и переходе на веб-страницу, настроенную для работы в режиме IE. Вы можете продолжить работу, но страница будет отображаться с использованием Microsoft Edge.

### <a name="error-message-could-not-retrieve-emie-site-list"></a>Сообщение об ошибке: "Не удалось получить список сайтов EMIE".

Эта ошибка может быть указана на *edge://compat/enterprise,* указывающее на сбой загрузки списка сайтов. Начиная с Microsoft Edge версии 87, когда файлы cookie блокированы для сторонних запросов с помощью политики [BlockThirdPartyCookies,](/deployedge/microsoft-edge-policies#blockthirdpartycookies) HTTP-проверка подлинности также невозможна. Вы можете разрешить файлы cookie для определенного домена, где размещен список сайтов в режиме предприятия, с помощью политики [CookiesAllowedForURLs](/deployedge/microsoft-edge-policies#cookiesallowedforurls), с целью обеспечить успешную загрузку списка сайтов.

## <a name="frequently-asked-questions"></a>Часто задаваемые вопросы

### <a name="will-ie-mode-replace-internet-explorer-11"></a>Заменит ли режим IE браузер Internet Explorer 11?

Да, настольное приложение Internet Explorer 11 будет снято с службы поддержки 15 июня 2022 г. Чтобы узнать, что в области, см. в [faq жизненного цикла - Internet Explorer](/lifecycle/faq/internet-explorer-microsoft-edge). Те же приложения и сайты IE11, которые вы используете сегодня, можно открывать в Microsoft Edge в режиме Internet Explorer. Подробнее об этом читайте в [материале "Будущее internet Explorer на](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)Windows 10 в Microsoft Edge.

### <a name="how-can-i-debug-my-legacy-application-while-using-ie-mode-on-microsoft-edge"></a>Как отлаживания моего устаревшего приложения при использовании режима IE на Microsoft Edge?

Вы можете использовать IEChooser для запуска devTools Internet Explorer для отладки содержимого вкладок режима IE. Чтобы использовать IEChooser, выполните следующие действия:

1. Откройте IEChooser.
   - Открывает диалоговое окно Выполнить Например, нажмите `Windows logo key`  +  `R` кнопку .
   - Введите `%systemroot%\system32\f12\IEChooser.exe` , а затем выберите **Ок**.
2. В IEChooser выберите запись для вкладки режима IE.

### <a name="can-i-test-a-site-in-microsoft-edge-while-it-is-configured-to-open-ie-mode-in-the-enterprise-mode-site-list"></a>Могу ли я протестировать сайт в Microsoft Edge, пока он настроен для открытия режима IE в списке Enterprise mode site list?

Да, в то время как вы модернизируете устаревшие сайты, вы можете протестировать приложения, настроенные в режиме IE, на Microsoft Edge. Для этого можно выполнить Microsoft Edge с `--ie-mode-test` флагом командной строки. Убедитесь, что другие экземпляры Microsoft Edge запущены. Затем можно выбрать Параметры **и больше** (значок эллипсов ...) **> Дополнительные средства > открытые сайты в режиме Edge.**

### <a name="can-i-use-view-in-file-explorer-in-sharepoint-online-on-microsoft-edge"></a>Можно ли использовать "View in File Explorer" SharePoint Online на Microsoft Edge?

Начиная с Microsoft Edge версии 95, вы можете включить функцию **View in File Explorer** для SharePoint современных библиотек документов в Интернете. Чтобы этот опыт был виден и работал для пользователей, необходимо включить Microsoft Edge "Настройка функции View in File Explorer для SharePoint страниц в политике [Microsoft Edge"](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) и обновить конфигурацию клиента SharePoint Online. Дополнительные данные. Просмотр SharePoint файлов с [помощью обозревателя файлов в Microsoft Edge - SharePoint в Microsoft 365 | Microsoft Docs](/SharePoint/sharepoint-view-in-edge).

Однако вместо использования параметра View in File Explorer рекомендуемый подход к управлению файлами и папками за пределами SharePoint заключается в синхронизации SharePoint и [Teams](https://support.microsoft.com/office/sync-sharepoint-and-teams-files-with-your-computer-6de9ede8-5b6e-4503-80b2-6190f3354a88?ui=en-us&rs=en-us&ad=us) файлов с компьютером или перемещения или копирования файлов в [SharePoint](https://support.microsoft.com/office/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc?ui=en-us&rs=en-us&ad=us).

### <a name="does-ie-mode-on-microsoft-edge-support-the-no-merge-option-that-was-supported-in-internet-explorer-11"></a>Поддерживает ли режим IE в Microsoft Edge поддерживает параметр "нет слияния", поддерживаемый в Internet Explorer 11?

Рекомендуемые альтернативы функции без слияния в Microsoft Edge являются одним из следующих действий:

1. Используйте профили в Microsoft Edge - Каждый профиль карты для различных сеансов IE для страниц режима IE, поэтому он ведет себя одинаково с параметром без слияния.
2. Используйте командную строку `--user-data-dir=<path>`, но с разными путями для каждого сеанса. При необходимости вы можете создать служебную программу, запускаемую пользователем, которая будет запускать Microsoft Edge и изменять путь для сеанса.

Если ни один из предыдущих параметров не работает для вашего сценария, начиная с Microsoft Edge версии 93, режим IE на Microsoft Edge будет поддерживать отсутствие слияния. Для конечных пользователей при запуске нового окна браузера из приложения режима IE оно будет в отдельном сеансе, как и поведение без слияния в IE11.

Для каждого Microsoft Edge окна при первом посещении вкладки режима IE в этом окне, если это назначенный сайт без слияния, это окно блокируется в другой сеанс IE без слияния.  Это окно остается заблокированным из всех Microsoft Edge до закрытия последней вкладки режима IE в заблокированном окне. Это следует за предыдущим поведением, когда пользователи могли запускать IE без слияния и запуска Microsoft Edge без слияния с помощью других механизмов. Все сайты, открываемые в новом окне (через window.open), будут соблюдать характер слияния родительского процесса.

> [!NOTE]
> Переключение сеансов не поддерживается. Навигация в одной вкладке режима IE будет использовать один и тот же сеанс.

Вы можете проверить поведение без слияния в Microsoft Edge версии 93 или более поздней версии, следуя следующим шагам:

1. Убедитесь, что режим IE включен Microsoft Edge версии 93 или более поздней версии.
2. Можно настроить сайты, необходимые для предотвращения общего доступа к сеансам в списке Enterprise mode Site List, установив значение атрибута типа слияния с "no-merge". Этот атрибут не применяется только в том случае, если элемент open-in заданной Microsoft Edge. По умолчанию все сайты имеют значение слияния типа слияния. (**Примечание.** Интегрированный инструмент управления списком сайтов, доступный в *edge://compat/sitelistmanager,* включает в себя почтовый ящик Без слияния при добавлении или редактировании сайта.) ****

   ```
   <site url="contoso.com">
   <open-in merge-type="no-merge">IE11</open-in>
   </site>
   ```

3. Перейдите на любой сайт, настроенный как не-слияние. Сайт должен быть в своем собственном сеансе IE. Когда вы откроете Microsoft Edge экземпляр или окно и перейдите на тот же сайт, он должен быть в своем сеансе IE. Обратите внимание, что iexplore.exe процессов в диспетчере задач.

Если у вас есть какие-либо отзывы, протянуть связь через один из наших каналов обратной связи: поддержка Майкрософт или [форум TechCommunity.](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise)

### <a name="can-i-save-links-as-webpages-in-internet-explorer-mode"></a>Можно ли сохранять ссылки как веб-страницы в режиме Internet Explorer?

Да, вы можете включить параметр "Сохранить объект как" в контекстном меню для режима Internet Explorer в Microsoft Edge. Для этого настройте групповую политику "Разрешить сохранение целевого показателя как в режиме*Internet Explorer",* расположенную в компьютерной конфигурации > Административные шаблоны *> Windows компоненты > Internet Explorer*. Механизм сохранения работает так же, как и в Internet Explorer. Если объект сохранен как HTML-файл, при повторном открытии файла страница отобразится в Microsoft Edge.

Для сохранения ссылок в качестве веб-страниц требуются следующие минимальные обновления операционной системы:

- Windows 10, версия 2004, Windows Server, версия 2004, Windows 10, версия 20H2: [KB4580364](https://support.microsoft.com/help/4580364/windows-10-update-kb4580364)
- Windows 10, версия 1903, Windows 10, версия 1909, Windows Server, версия 1903: [KB4580386](https://support.microsoft.com/help/4580386/windows-10-update-kb4580386)
- Windows 10, версия 1809, Windows Server, версия 1809, Windows Server 2019: [KB4580390](https://support.microsoft.com/help/4580390/windows-10-update-kb4580390)
- Windows 10, версия 1803: [KB4586785](https://support.microsoft.com/help/4586785/windows-10-update-kb4586785)
- Windows 10, версия 1607: [KB4586830](https://support.microsoft.com/help/4586830/windows-10-update-kb4586830)
- Windows 10, версия 1507: [KB4586787](https://support.microsoft.com/help/4586787/windows-10-update-kb4586787)

### <a name="can-i-test-a-site-in-microsoft-edge-while-it-is-configured-to-open-ie-mode-in-the-enterprise-mode-site-list"></a>Могу ли я протестировать сайт в Microsoft Edge, пока он настроен для открытия режима IE в списке Enterprise mode site list?

Да, при модернизации устаревших сайтов можно протестировать сайты режимов IE на Microsoft Edge. Для этого можно выполнить Microsoft Edge с `--ie-mode-test` флагом командной строки. Убедитесь, что другие экземпляры Microsoft Edge запущены. Затем выберите **Параметры и больше** (значок эллипсов) ... **> Дополнительные средства > открытые сайты в режиме Edge.**

### <a name="my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported"></a>Мое приложение требует передачи данных POST между режимом IE и Microsoft Edge. Это возможно?

Начиная с канал Microsoft Edge Beta версии 96, навигация, переключаемая между режимом Internet Explorer и Microsoft Edge, будет включать данные форм и дополнительные http-заготки. Однако если данные форм включают вложения файлов, они не будут передаваться между двигателями. Какие типы данных следует включать в такие навигации, можно выбрать с помощью групповой политики [InternetExplorerIntegrationComplexNavDataTypes.](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes)

Помимо Microsoft Edge версии 96, для этого Windows следующие обновления:

- Windows 10 версии 2004; Windows Серверная версия 2004; Windows 10 версии; Windows Версия сервера 20H2 и Windows 10 версии 21H1 — KB5006738 или более поздней версии

  > [!NOTE]
  > В ближайшее время Windows 10 версии 19H2, Windows Server 2022 и Windows 11.

## <a name="see-also"></a>См. также
  
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Сведения о режиме IE](./edge-ie-mode.md)
- [Дополнительные сведения о режиме предприятия](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
