---
title: Устранение неполадок в режиме Internet Explorer (IE) и ОТВЕТ
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 01/18/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Руководство по устранению неполадок и ответ на Microsoft Edge режиме Internet Explorer
ms.openlocfilehash: 064174744dbdc8d16912e4c196a8974c243de732
ms.sourcegitcommit: 556aca8dde42dd66364427f095e8e473b86651a0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2022
ms.locfileid: "12445683"
---
# <a name="internet-explorer-ie-mode-troubleshooting-and-faq"></a>Устранение неполадок в режиме Internet Explorer (IE) и ОТВЕТ

> [!NOTE]
> 15 июня 2022 г. настольное приложение Internet Explorer 11 будет снято с службы поддержки. Чтобы узнать список областей, см. в задаваемом веб-сайте [Internet Explorer 11 для](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549) настольных приложений. Те же приложения и сайты IE11, которые вы используете сегодня, можно открывать в Microsoft Edge в режиме Internet Explorer. Дополнительные дополнительные публикации см. в Windows 10 в Microsoft Edge Internet [Explorer](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

В этой статье данная статья содержит советы по устранению неполадок и ответов на Microsoft Edge версии 77 или более поздней версии.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## <a name="what-if-i-need-help-with-setting-up-microsoft-edge-or-internet-explorer-mode"></a>Что делать, если мне нужна помощь в настройке Microsoft Edge режиме Internet Explorer?

Мы предлагаем различные варианты поддержки. Если у вас Единая поддержка Майкрософт, вы можете связаться с этой службой поддержки, чтобы помочь с переходом. Кроме того  [FastTrack](https://www.microsoft.com/en-us/fasttrack/microsoft-365/microsoft-edge?rtc=1) доступны без дополнительной платы для клиентов с 150 или более платными местами Windows 10.

Мы также рекомендуем наш Microsoft Edge режиме Internet Explorer [Getting Started guide](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWEHMs) и нашу серию блога [режимов IE](https://techcommunity.microsoft.com/t5/windows-10/internet-explorer-to-microsoft-edge-with-ie-mode-blog-series/m-p/2617124).

## <a name="common-ie-mode-issues"></a>Общие проблемы режима IE

Используйте этот раздел в качестве руководства для устранения неполадок и устранения двух наиболее распространенных проблем при переходе Microsoft Edge режиме IE. Эти проблемы:

- Неправильные конфигурации режима документа
- Неполные нейтральные конфигурации сайтов

### <a name="incorrect-document-mode-configurations"></a>Неправильные конфигурации режима документа

В этом разделе описаны симптомы и описаны действия по диагностике и устранению этой проблемы.

#### <a name="symptoms"></a>Симптомы

Пользователи будут испытывать следующие симптомы:
  
- Размер и расположение элементов страниц могут быть отключены или отсутствуют. 
- Некоторые функции могут быть потеряны или работать не так, как ожидалось. Например, кнопки, которые работали с Internet Explorer, ничего не делают и не возвращают ошибку.

#### <a name="how-to-troubleshoot-and-fix"></a>Устранение и устранение неполадок

Общая стратегия заключается в том, чтобы дублировать те же параметры, которые работали с Internet Explorer 11 для определенного сайта в нашем списке сайтов режима IE. Используйте вкладку "Эмуляция" панели инструментов разработчика F12 в IE 11, показанную на следующем скриншоте, чтобы изучить сценарий, который необходимо исправить. Чтобы открыть панель инструментов Developer, нажмите клавишу F12 и выберите **Open DevTools**.

![Вкладка Эмуляция в представлении DevTools](./media/edge-ie-mode-faq/edge-ie-mode-emulation-tab.png)

На вкладке Эмуляция показаны два фрагмента сведений, на которые необходимо сосредоточиться: режим Документа (1) и текст ниже списка выпадения (2). Эти сведения помогут объяснить, почему мы в режиме 11 (по умолчанию) для страницы или сайта, на которые мы смотрим.

Существуют различные сообщения, которые могут отображаться в режиме Document, и в нашем примере они:
  
- Мета тег с помощью X-UA-совместимый
- Http header via X-UA-compatible HTTP

Два параметра X-UA-Compatible указывают на то, что на веб-странице или веб-сервере, на котором размещен сайт, показан режим документа, который должен использоваться браузером.  

Мы хотим почти во всех случаях соблюдать режим документа. Для этого необходимо выбрать один из следующих режимов в записи списка сайтов режима IE для сайта:

- По умолчанию
- IE8 Enterprise
- IE7 Enterprise

Эти параметры уважают директивы веб-страницы или веб-сервера. Помните, что необходимо выбрать параметр, который включает указанный режим документа. В примере экрана, так как указанный режим документа 11, мы выбрали бы "По умолчанию", так как IE8 Enterprise и IE7 Enterprise не поддерживают режим документов IE 11.  

Если в режиме Документа указывается, что для сайта необходимо одно из следующих представлений о совместимости, параметр конфигурации прост.

- С помощью локальных параметров представления совместимости
- С помощью списка представлений о совместимости
- Параметры совместимости интрасети

Поскольку все параметры представления совместимости привели к поведению Enterprise IE7, выберите этот параметр в разделе "Режим компата" в записи списка сайтов режима IE.

Дополнительные сведения о логике, которую internet Explorer или IE режим использует для посадки в одном режиме doc над другим, см. в статье [Deprecated document modes and Internet Explorer 11](/internet-explorer/ie11-deploy-guide/deprecated-document-modes) .

Общее правило — использовать самый современный режим на основе логики, который позволяет сайту работать так, как ожидалось. Мы начнем с режима по умолчанию, перейдем в режим IE8 Enterprise, а затем в режим Enterprise IE7. Этот выбор позволяет ребенку использовать различные режимы документа по мере необходимости с помощью встроенной логики для их конкретных потребностей. В результате все страницы веб-сайтов не заблокированы в одном определенном режиме Документа.  

В следующей таблице перечислены доступные режимы документов для этих параметров.

| Режим на основе логики | По умолчанию | IE8 Enterprise | IE7 Enterprise |
|--|--|--|--|
| Доступные режимы документа | Режим IE11 Doc<br> Режим IE10 Doc<br>Режим IE9 Doc<br> Режим IE8 Doc<br>Режим IE7 Doc<br>Режим "Причуды IE5" | Режим IE8 Doc<br>Режим IE7 Doc<br>Режим "Причуды IE5"   | Режим IE7 Doc<br>Режим "Причуды IE5"  |

> [!NOTE]
> В некоторых случаях для работы определенного сайта или страницы требуется определенный режим документа. Мы рекомендуем использовать явные параметры режима документа только в том случае, если параметры, основанные на логике, не эффективны.

### <a name="incomplete-neutral-site-configurations"></a>Неполные нейтральные конфигурации сайтов

В этом разделе описаны симптомы и описаны действия по диагностике и устранению этой проблемы.

#### <a name="symptoms"></a>Симптомы
  
Страница полагается на SSO для проверки подлинности, но пользователи несколько раз подсказывляются для учетных данных, испытывают циклические перенаправления, ошибки проверки подлинности, или некоторые комбинации этих симптомов.
  
#### <a name="how-to-troubleshoot-and-fix"></a>Устранение и устранение неполадок
  
Прежде чем приступить к анализу сбоя рабочего процесса в Microsoft Edge, посмотрите на адресную планку логотипа режима IE "e", показанную на следующем скриншоте.

![Логотип IE в Microsoft Edge меню.](./media/edge-ie-mode-faq/edge--ie-mode-logo.png)

Если во время процесса проверки подлинности SSO мы видим "e", но оно исчезает после перенаправления, это поведение указывает на отсутствующий нейтральный сайт. После Microsoft Edge в режим IE нам необходимо оставаться там, чтобы поддерживать данные сеанса и cookie. Если URL-адрес появляется в панели адресов достаточно долго, чтобы идентифицировать его, добавьте его в список сайтов режима IE в качестве нейтрального сайта с помощью действий, описанных в [Настройка нейтральных сайтов](/deployedge/edge-ie-mode-sitelist#configure-neutral-sites).

Часто цикл перенаправления происходит так быстро, что трудно определить отсутствующие нейтральные сайты. Чтобы помочь в этом анализе, мы используем средство, встроенное в Chromium: **чистый экспорт**.

> [!TIP]
> Трассировка сети по своей сути является шумной. Чтобы свести к минимуму шум, закройте все другие экземпляры браузера и вкладки, которые не нужны для конкретного рабочего процесса, который вы изучаете.

Ниже описаны действия по устранению неполадок в нейтральной конфигурации сайта.
  
1. Откройте новую вкладку в Microsoft Edge и перейдите *к edge://net-export*.
2. Выберите **начало ведения журнала на диск**, а затем выберите расположение, в котором необходимо сохранить в результате журнал .json. Этот журнал можно безопасно удалить после устранения неполадок.
3. Откройте еще одну вкладку (сохраняйте открытую вкладку net-export) и повторите сбой рабочего процесса.
4. После завершения вернись на вкладку net-export и выберите **стоп-журнал**.
5. Выберите гиперссылку "netlog viewer".
6. На итоговой странице выберите **выберите файл**, а затем выберите файл .json, созданный на шаге 2.
7. После загрузки файла журнала выберите **События** из левого бокового меню.
8. Прокрутите сетевой журнал и определите начальный URL-адрес. (Вы также можете использовать функцию поиска, чтобы найти отправную точку.)
9. С начальной точки прокрутите вниз и найдите URL-адреса в рабочего процесса, в списке сайтов в режиме IE нет записи. Обратите особое внимание на URL-адреса с индикаторами для SSO, AUTH, LOGIN и так далее.
10. После определения URL-адреса кандидата добавьте его в список сайтов режима IE в качестве нейтрального сайта, выбрав **None** в отсеве Open-in. Проверьте рабочий процесс еще раз.

В некоторых случаях требуется несколько нейтральных записей сайта в зависимости от конкретной архитектуры сайта. Если рабочий процесс по-прежнему не выполняется после добавления нового нейтрального сайта, повторите процесс захвата нового журнала net-export и выполните другой пропуск.

В некоторых редких случаях может потребоваться настройка определенных общих файлов cookie, чтобы убедиться, что необходимая информация попадает на сайты режимов IE. Если вам известно о определенном файле cookie, необходимом, вы можете настроить общий доступ к файлам cookie с помощью действий, описанных в совместном использовании файлов cookie, от Microsoft Edge до [Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

### <a name="what-if-these-steps-dont-fix-the-issue"></a>Что делать, если эти действия не устраняют проблему?

Эта статья предназначена для устранения наиболее распространенных проблем конфигурации режима IE, но она может не охватывать все возможные сценарии. Если у вас возникла проблема, с помощью которую вы не можете устранить, обратитесь в App Assure, [https://aka.ms/AppAssure](https://aka.ms/AppAssure) и мы поможем вам с вашей проблемой.

## <a name="get-general-diagnostic-and-configuration-information"></a>Общие сведения о диагностике и конфигурации

Диагностические сведения о режиме Internet Explorer можно получить на вкладке "Совместимость Microsoft Edge". Чтобы открыть ее, перейдите по адресу *edge://compat/iediagnostic*. На странице "Диагностические сведения в режиме Internet Explorer" могут показываться диагностические сообщения, и можно экспортировать диагностические данные в XML-файл. На этой странице диагностических сведений также содержится информация о конфигурации для следующих категорий:

- **Проверка раздела реестра.** (Отображается, только если проверка не пройдена.) Проверяет правильность настройки интеграции Internet Explorer в реестре. Если нет, пользователь может выбрать **исправление проблемы** .
- **Режим Internet Explorer.** Отображает используемую версию API на основе конфигурации и ОС. При наличии проблемы пользователю может быть предложено установить Центр обновления Windows.
- **Настройка режима Internet Explorer.** Указывает, включен ли режим Internet Explorer и как он настроен.
- **Командная строка.** Показывает строку командной строки и переключатели, используемые для запуска Microsoft Edge.
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

Эта ошибка может быть указана *на edge://compat/enterprise,* указывающее на сбой загрузки списка сайтов. Начиная с Microsoft Edge версии 87, когда файлы cookie заблокированы для сторонних запросов с помощью политики [BlockThirdPartyCookies](/deployedge/microsoft-edge-policies#blockthirdpartycookies), проверка подлинности HTTP также запрещена. Вы можете разрешить файлы cookie для определенного домена, где размещен список сайтов в режиме предприятия, с помощью политики [CookiesAllowedForURLs](/deployedge/microsoft-edge-policies#cookiesallowedforurls), с целью обеспечить успешную загрузку списка сайтов.

### <a name="error-message-the-connection-for-this-site-is-not-secure"></a>Сообщение об ошибке: "Подключение для этого сайта не безопасно"

Эта ошибка может произойти, если вы пытаетесь открыть устаревший веб-сайт в режиме IE и настроить сайт для запуска в TLS 1.0 или TLS 1.1. Эти протоколы отключены по умолчанию в Microsoft Edge. Дополнительные сведения см. в [статью План изменений: TLS 1.0 и TLS 1.1](https://blogs.windows.com/msedgedev/2020/03/31/tls-1-0-tls-1-1-schedule-update-edge-ie11/) скоро будут отключены по умолчанию

### <a name="error-message-this-form-cannot-be-opened-in-a-web-browser-to-open-this-form-use-microsoft-infopath"></a>Сообщение об ошибке: "Эту форму нельзя открыть в веб-браузере. Чтобы открыть эту форму, используйте Microsoft InfoPath"

Для некоторых приложений может потребоваться загрузить веб-страницу в режиме IE. Функцию режима IE можно использовать в Microsoft Edge.

Может потребоваться также `compat-mode` установить атрибут в списке Enterprise режиме по **умолчанию**. Дополнительные сведения см. [в Enterprise Mode и Enterprise Mode Site List](/internet-explorer/ie11-deploy-guide/what-is-enterprise-mode#enterprise-mode-and-the-enterprise-mode-site-list-1).

> [!TIP]
> Пользователи могут легко просмотреть этот список сайтов и режим совместимости, введя **в Microsoft Edge**.

## <a name="frequently-asked-questions"></a>Часто задаваемые вопросы

### <a name="will-ie-mode-replace-internet-explorer-11"></a>Заменит ли режим IE браузер Internet Explorer 11?

Да, настольное приложение Internet Explorer 11 будет снято с службы поддержки 15 июня 2022 г. Чтобы узнать, что в области, см. в [faq жизненного цикла - Internet Explorer](/lifecycle/faq/internet-explorer-microsoft-edge). Те же приложения и сайты IE11, которые вы используете сегодня, можно открывать в Microsoft Edge в режиме Internet Explorer. Подробнее читайте в материале ["Будущее обозревателя Интернета" Windows 10 в Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

### <a name="can-i-use-view-in-file-explorer-in-sharepoint-online-on-microsoft-edge"></a>Можно ли использовать "View in File Explorer" SharePoint Online на Microsoft Edge?

Начиная с Microsoft Edge версии 95, вы можете включить функцию **View in File Explorer** для SharePoint современных библиотек документов в Интернете. Чтобы этот опыт был виден и работал для пользователей, необходимо включить функцию Microsoft Edge "Настройка функции View [in File Explorer для SharePoint](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) страниц в политике Microsoft Edge" и обновить конфигурацию клиента SharePoint Online. Дополнительные данные. [Просмотр SharePoint файлов с помощью обозревателя файлов в Microsoft Edge - SharePoint в Microsoft 365 | Документы Майкрософт](/SharePoint/sharepoint-view-in-edge).

Однако вместо использования параметра View in File Explorer рекомендуется управлять файлами и папками за пределами SharePoint, чтобы синхронизировать SharePoint и [Teams](https://support.microsoft.com/office/sync-sharepoint-and-teams-files-with-your-computer-6de9ede8-5b6e-4503-80b2-6190f3354a88?ui=en-us&rs=en-us&ad=us) с компьютером или переместить или скопировать файлы в [SharePoint](https://support.microsoft.com/office/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc?ui=en-us&rs=en-us&ad=us).

### <a name="does-ie-mode-on-microsoft-edge-support-the-no-merge-option-that-was-supported-in-internet-explorer-11"></a>Поддерживает ли режим IE Microsoft Edge поддерживает параметр "не-слияние", поддерживаемый в Internet Explorer 11?

Рекомендуемые альтернативы функции без слияния в Microsoft Edge являются одним из следующих действий:

1. Используйте профили в Microsoft Edge - Каждый профиль карты для различных сеансов IE для страниц режима IE, поэтому он ведет себя одинаково с параметром без слияния.
2. Используйте командную строку `--user-data-dir=<path>`, но с разными путями для каждого сеанса. При необходимости можно создать утилиту для запуска пользователя, которая запускает Microsoft Edge и изменяет путь к сеансу.

Если ни один из предыдущих параметров не работает для вашего сценария, начиная с Microsoft Edge версии 93, режим IE на Microsoft Edge будет поддерживать отсутствие слияния. Для конечных пользователей при запуске нового окна браузера из приложения режима IE оно будет в отдельном сеансе, как и поведение без слияния в IE11.

Для каждого Microsoft Edge окна при первом посещении вкладки режима IE в этом окне, если это назначенный сайт без слияния, это окно блокируется в другой сеанс IE без слияния.  Это окно остается заблокированным из всех Microsoft Edge до закрытия последней вкладки режима IE в закрытом окне. Это следует за предыдущим поведением, когда пользователи могли запускать IE без слияния и запуска Microsoft Edge без слияния с помощью других механизмов. Все сайты, открываемые в новом окне (через window.open), будут соблюдать характер слияния родительского процесса.

> [!NOTE]
> Переключение сеансов не поддерживается. Навигация в одной вкладке режима IE будет использовать один и тот же сеанс.

Вы можете проверить поведение без слияния в Microsoft Edge версии 93 или более поздней версии, следуя следующим шагам:

1. Убедитесь, что режим IE включен Microsoft Edge версии 93 или более поздней версии.
2. Можно настроить сайты, необходимые для предотвращения общего доступа к сеансам в списке Enterprise mode Site List, установив значение атрибута типа слияния на "не-слияние". Этот атрибут не применяется только в том случае, если элемент open-in заданной Microsoft Edge. По умолчанию все сайты имеют значение слияния типа слияния. (**Примечание.** Интегрированный инструмент управления списком сайтов, доступный в edge://compat/sitelistmanager, включает в себя почтовый *ящик* No **Merge** при добавлении или редактировании сайта.)

   ```
   <site url="contoso.com">
   <open-in merge-type="no-merge">IE11</open-in>
   </site>
   ```

3. Перейдите на любой сайт, настроенный как не-слияние. Сайт должен быть в своем собственном сеансе IE. Если вы откроете Microsoft Edge экземпляр или окно и перейдите на тот же сайт, он должен быть в собственном сеансе IE. Обратите внимание, что в диспетчере задач iexplore.exe несколько процессов.

Если у вас есть какие-либо отзывы, протянуть связь через один из наших каналов обратной связи: поддержка Майкрософт или [форум TechCommunity](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise) .

### <a name="can-i-save-links-as-webpages-in-internet-explorer-mode"></a>Можно ли сохранять ссылки как веб-страницы в режиме Internet Explorer?

Да, вы можете включить параметр "Сохранить объект как" в контекстном меню для режима Internet Explorer в Microsoft Edge. Для этого настройте групповую политику "Разрешить сохранение целевого показателя как в режиме *Internet Explorer*", расположенную в компьютерной конфигурации > Административные шаблоны *> Windows компоненты > Internet Explorer*. Механизм сохранения работает так же, как и в Internet Explorer, и если цель сохранена в качестве html-файла, повторное открытие файла будет отрисовки страницы в Microsoft Edge.

Для сохранения ссылок в качестве веб-страниц требуются следующие минимальные обновления операционной системы:

- Windows 10, версия 2004, Windows Server, версия 2004, Windows 10, версия 20H2: [KB4580364](https://support.microsoft.com/help/4580364/windows-10-update-kb4580364)
- Windows 10, версия 1903, Windows 10, версия 1909, Windows Server, версия 1903: [KB4580386](https://support.microsoft.com/help/4580386/windows-10-update-kb4580386)
- Windows 10, версия 1809, Windows Server, версия 1809, Windows Server 2019: [KB4580390](https://support.microsoft.com/help/4580390/windows-10-update-kb4580390)
- Windows 10, версия 1803: [KB4586785](https://support.microsoft.com/help/4586785/windows-10-update-kb4586785)
- Windows 10, версия 1607: [KB4586830](https://support.microsoft.com/help/4586830/windows-10-update-kb4586830)
- Windows 10, версия 1507: [KB4586787](https://support.microsoft.com/help/4586787/windows-10-update-kb4586787)

### <a name="can-i-test-a-site-in-microsoft-edge-while-it-is-configured-to-open-ie-mode-in-the-enterprise-mode-site-list"></a>Могу ли я протестировать сайт в Microsoft Edge, пока он настроен для открытия режима IE в списке Enterprise режима сайта?

Да, в то время как вы модернизируете устаревшие сайты, вы можете протестировать приложения, настроенные в режиме IE, на Microsoft Edge. Чтобы протестировать эти приложения, можно настроить политику [InternetExplorerModeTabInEdgeModeAllowed](/deployedge/microsoft-edge-policies#internetexplorermodetabinedgemodeallowed) . Если вы включаете эту политику, пользователи могут открывать сайты режимов IE в Microsoft Edge, выбрав Параметры и **более (** значок эллипсов ...) > Дополнительные сайты **ToolsOpen****** >  в режиме Edge.

### <a name="how-can-i-debug-my-legacy-application-while-using-ie-mode-on-microsoft-edge"></a>Как отлаживания моего устаревшего приложения при использовании режима IE на Microsoft Edge?

Вы можете использовать IEChooser для запуска devTools Internet Explorer для отладки содержимого вкладок режима IE. Чтобы использовать IEChooser, выполните следующие действия:

1. Откройте IEChooser.
   - Открывает диалоговое окно Выполнить Например, нажмите кнопку `Windows logo key` + `R`.
   - Введите `%systemroot%\system32\f12\IEChooser.exe`, а затем выберите **Ок**.
2. В IEChooser выберите запись для вкладки режима IE.

### <a name="my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported"></a>Мое приложение требует передачи данных POST между режимом IE и Microsoft Edge. Это возможно?

Начиная с канал Microsoft Edge Beta версии 96, навигация, переключаемая между режимом Internet Explorer и Microsoft Edge, будет включать данные форм и дополнительные http-заготки. Однако если данные форм включают вложения файлов, они не будут передаваться между двигателями. Какие типы данных следует включать в такие навигации, можно выбрать с помощью групповой политики [InternetExplorerIntegrationComplexNavDataTypes](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) .

Помимо Microsoft Edge версии 96, для этого Windows следующие обновления:

- Windows 11 [KB5007262](https://support.microsoft.com/topic/november-22-2021-kb5007262-os-build-22000-348-preview-7f3e18d7-4189-4882-b0e9-afc920253aee) или более поздней
- Windows Server 2022 [KB5007254](
https://support.microsoft.com/topic/november-22-2021-kb5007254-os-build-20348-380-preview-9a960291-d62e-486a-adcc-6babe5ae6fc1) или более поздней
- Windows 10 версии 2004; Windows Server версии 2004; Windows 10 версии; Windows версии 20H2 и Windows 10 версии 21H1 - [KB5006738](https://support.microsoft.com/topic/october-26-2021-kb5006738-os-builds-19041-1320-19042-1320-and-19043-1320-preview-ccbce6bf-ae00-4e66-9789-ce8e7ea35541) или более поздней версии
- Windows 10 версии 1909 [KB5007189](
https://support.microsoft.com/topic/november-9-2021-kb5007189-os-build-18362-1916-91b4647c-9979-4d84-8e64-efc8674e8c1f) или более поздней версии

### <a name="where-can-i-find-the-reload-in-internet-explorer-mode-option"></a>Где можно найти параметр "Перезагрузка в режиме Internet Explorer"?

Эта функция доступна в Microsoft Edge версии 92 или более поздней версии. Чтобы включить этот параметр, настройте "Разрешить перезагрузку сайтов в параметрах режима Internet Explorer" в Microsoft Edge "Разрешить".  Дополнительные сведения см. в [веб-сайте Enable the local site list experience](/deployedge/edge-ie-mode-local-site-list#enable-the-local-site-list-experience).

### <a name="where-is-the-file--new-session-option-in-microsoft-edge"></a>Где параметр "Файл > сеанс" в Microsoft Edge?

Современное решение браузера доступно с помощью нескольких профилей в Microsoft Edge. Эта функция позволяет создать новый сеанс с другой учетной записью. В следующих ресурсах приводится информация о преимуществах нескольких профилей и их использовании.

- [Видео: Microsoft Edge и удостоверение](/deployedge/microsoft-edge-video-identity)
- [Использование нескольких профилей на работе и дома теперь проще с Microsoft Edge](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/)

### <a name="why-am-i-getting-multiple-authentication-prompts-when-running-a-page-in-ie-mode-on-microsoft-edge"></a>Почему я получаю несколько подсказок проверки подлинности при запуске страницы в режиме IE на Microsoft Edge?

Клиентский сертификат может запрашиваться дважды в режиме IE. В первый раз диалоговое окно выбора сертификата будет отображаться в режиме IE, а во второй раз диалоговое окно будет отображаться в Microsoft Edge. Как процесс кадра, так и процесс окна должны запрашивать проверку подлинности.

После создания кэша favicon вам не будет предложено снова получить клиентский сертификат, если вы не удалите кэш. Кроме того, вы можете установить правило в конфигурации сервера, например IIS, чтобы не требовать сертификат клиента для favicon.

### <a name="why-are-there-rendering-issues-like-text-wrapping-and-content-truncation-when-child-windows-are-running-in-ie-mode-in-microsoft-edge"></a>Почему существуют проблемы с отрисовкой текста и truncation контента, когда детские окна работают в режиме IE в Microsoft Edge?

Область контента детского окна, отрисовываемого в режиме IE в Microsoft Edge немного отличается от области, которая находится в Internet Explorer 11. Если веб-страница разработана с выравниваниями или позиционированием на основе пикселей, может возникнуть неправильная визуализация, текстовая упаковка и так далее.

В версии 95 Microsoft Edge два параметра политики, которые позволяет указать настраиваемые настройки высоты и ширины всплывающих окон, созданных с сайтов режимов IE `window.open` с помощью метода. Для настройки размера окна можно использовать следующие политики:

- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/deployedge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) — этот параметр позволяет указать настраиваемую настройку на высоту всплывающих окон, созданных на сайте режима Internet Explorer.
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/deployedge/microsoft-edge-policies#internetexplorerintegrationwindowopenwidthadjustment) . Этот параметр позволяет указать настраиваемую настройку ширины всплывающих окон, созданных на сайте режима Internet Explorer.

### <a name="why-arent-pop-ups-or-redirected-websites-loading-in-ie-mode-or-in-internet-explorer-11"></a>Почему всплывающие и перенаправленные веб-сайты не загружаются в режиме IE или в Internet Explorer 11?

После настройки режима IE некоторые веб-сайты, особенно сайты, создающие новое окно или перенаправленный сайт, могут не отрисовки в режиме IE или открыться в Internet Explorer 11.

Для этого типа перенаправленного веб-сайта `allow-redirect="true"` можно использовать конфигурацию списка сайтов. Дополнительные сведения см. [в обновленной схеме элементов](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-elements).

### <a name="why-arent-websites-loading-in-ie-mode-when-i-launch-microsoft-edge-for-the-first-time"></a>Почему веб-сайты не загружаются в режиме IE при первом запуске Microsoft Edge?

Microsoft Edge необходимо скачать список сайтов режима IE, прежде чем он сможет применять параметры режима IE. Этот процесс может не завершиться после начала работы браузера. Доступна политика, которая может принудительно загрузить список сайтов перед загрузкой веб-сайта. Дополнительные сведения см. в политике [DelayNavigationsForInitialSiteListDownload](/deployedge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload).

### <a name="why-cant-i-open-files-or-pages-that-are-found-by-using-file-urls-in-microsoft-edge"></a>Почему нельзя открывать файлы или страницы, найденные с file:// URL-адресов в Microsoft Edge?

Из-за Chromium безопасности необходимо использовать режим IE. Вы можете использовать Microsoft Edge IE для загрузки веб-страниц, **размещенных** в протоколе file:// в зоне интрасети. Для этого можно использовать групповую политику [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled) .

## <a name="see-also"></a>См. также
  
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Сведения о режиме IE](./edge-ie-mode.md)
- [Дополнительные сведения о режиме предприятия](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
