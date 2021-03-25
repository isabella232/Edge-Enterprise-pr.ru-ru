---
title: Вопросы и ответы о режиме IE
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/15/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Вопросы и ответы и устранение неполадок с Microsoft Edge в режиме IE
ms.openlocfilehash: f5279caddb5d3dfabaf04be6bd927f7095be1fc9
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447733"
---
# <a name="ie-mode-faq"></a>Вопросы и ответы о режиме IE

Данная статья содержит советы по устранению неполадок и ответы на часто задаваемые вопросы для Microsoft Edge версии 77 или более поздней.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней; каналы **Stable**, **Beta** и **Dev**.


## <a name="troubleshoot-ie-mode"></a>Устранение неполадок режима IE

Используйте сведения из этого раздела для диагностики и устранения проблем в режиме IE.

### <a name="internet-explorer-mode-diagnostic-information"></a>Диагностические сведения о режиме Internet Explorer

Диагностические сведения о режиме Internet Explorer можно получить на вкладке "Совместимость Microsoft Edge". Чтобы открыть ее, перейдите по адресу *edge://compat/iediagnostic*. Эта страница может отображать сообщения диагностики. Эта страница также содержит сведения о настройке для следующих категорий:

- **Проверка раздела реестра**. (Отображается, только если проверка не пройдена.) Проверяет правильность настройки интеграции Internet Explorer в реестре. Если настройка выполнена неправильно, пользователь может нажать **Исправить**, чтобы устранить проблему.
- **Режим Internet Explorer**. Отображает используемую версию API на основе конфигурации и ОС. При наличии проблемы пользователю может быть предложено установить **Центр обновления Windows**.
- **Настройка режима Internet Explorer**. Указывает, включен ли режим Internet Explorer и как он настроен.
- **Командная строка**. Отображает командную строку и параметры, используемые для запуска Microsoft Edge.
- **Параметры групповой политики**. Указывает, настроен ли режим IE с помощью групповых политик, и какие политики применяются.

### <a name="error-message-to-open-this-page-in-internet-explorer-mode-reinstall-microsoft-edge-with-administrator-privileges"></a>Сообщение об ошибке: "Чтобы открыть эту страницу в режиме Internet Explorer, переустановите Microsoft Edge с правами администратора".

Эта ошибка может возникнуть, если у вас нет всех необходимых обновлений для Windows. Необходимые версии Windows и Microsoft Edge см. в предварительных условиях, перечисленных в статье [Сведения о режиме IE](./edge-ie-mode.md).

Если вы уже установили все необходимые обновления для Windows, эта ошибка может появляться в следующих случаях:

- Вы используете канал Canary, установленный на уровне пользователя по умолчанию.
- Вы используете канал Stable, Beta или Dev, но при установке уровня прав запрос на повышение уровня был отменен. При отмене запроса на повышение прав установка продолжается на уровне пользователя.
- Internet Explorer 11 отключен в компонентах Windows.

Возможные решения:

- Запустите установщик для любого канала на уровне системы: `installer.exe --system-level`.
- Включите Internet Explorer 11 в компонентах Windows.

Чтобы убедиться, что Microsoft Edge установлен на уровне системы, введите "edge://version" в адресной строке Microsoft Edge. Путь к исполняемому файлу будет начинаться с *C:\Program Files*, что указывает на установку на уровне системы. Если путь к исполняемому файлу начинается с *C:\Users\*, удалите, а затем переустановите Microsoft Edge с правами администратора.

### <a name="error-message-to-open-this-page-in-ie-mode-try-restarting-microsoft-edge"></a>Сообщение об ошибке: "Чтобы открыть эту страницу в режиме IE, попробуйте перезапустить Microsoft Edge".

Эта ошибка может отображаться, если в Internet Explorer произошла непредвиденная ошибка. Перезапуск Microsoft Edge обычно исправляет эту ошибку.

### <a name="error-message-turn-off-remote-debugging-to-open-this-site-in-ie-mode-otherwise-it-might-not-work-as-expected"></a>Сообщение об ошибке: "Отключите удаленную отладку, чтобы открыть этот сайт в режиме IE, в противном случае он может работать неправильно".

Эта ошибка может возникнуть, если вы используете удаленную отладку и переходите на веб-страницу, настроенную для работы в режиме IE. Вы можете продолжить работу, но страница будет отображаться с использованием Microsoft Edge.

### <a name="error-message-error-could-not-retrieve-emie-site-list"></a>Сообщение об ошибке: "Ошибка: не удалось получить список сайтов EMIE".

Эта ошибка может появиться на странице *edge://compat/enterprise*, указывая на то, что загрузка списка сайтов не удалась. Начиная с Microsoft Edge версии 87, когда файлы cookie блокированы для сторонних запросов с помощью политики [BlockThirdPartyCookies,](./microsoft-edge-policies.md#blockthirdpartycookies) HTTP-проверка подлинности также невозможна. Вы можете разрешить файлы cookie для определенного домена, где размещен список сайтов в режиме предприятия, с помощью политики [CookiesAllowedForURLs](./microsoft-edge-policies.md#cookiesallowedforurls), с целью обеспечить успешную загрузку списка сайтов.

## <a name="frequently-asked-questions"></a>Часто задаваемые вопросы

### <a name="will-ie-mode-replace-internet-explorer-11"></a>Заменит ли режим IE браузер Internet Explorer 11?

Мы стремимся поддерживать Internet Explorer, чтобы он оставался надежным и безопасным браузером. Internet Explorer все еще является компонентом Windows и на него распространяется жизненный цикл поддержки ОС Windows, в которой установлен браузер. Дополнительные сведения см. в разделе [Вопросы и ответы по жизненному циклу— Internet Explorer](https://support.microsoft.com/help/17454/). Несмотря на то что корпорация Майкрософт продолжает поддерживать и обновлять Internet Explorer, новейшие функции и обновления платформы будут доступны только в Microsoft Edge.

### <a name="can-i-use-open-with-explorer-or-view-in-file-explorer-in-sharepoint-with-ie-mode"></a>Можно ли использовать параметры "Открыть в проводнике" или "Просмотреть в проводнике" в SharePoint в режиме IE?

Да, если они поддерживаются в автономном режиме Internet Explorer 11, они доступны в режиме IE. Однако вместо использования параметра "Открыть в проводнике" для управления файлами и папками за пределами SharePoint рекомендуется [синхронизировать файлы SharePoint](https://support.office.com/en-us/article/sync-sharepoint-files-with-the-onedrive-sync-app-6de9ede8-5b6e-4503-80b2-6190f3354a88) либо [переместить или скопировать файлы в SharePoint](https://support.office.com/en-us/article/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc).

### <a name="does-ie-mode-on-microsoft-edge-support-the-nomerge-option-that-was-supported-in-internet-explorer-11"></a>Поддерживает ли режим IE в Microsoft Edge параметр *nomerge*, который поддерживался в Internet Explorer 11?

В Microsoft Edge нет явной командной строки, чтобы зеркально отразить параметр *nomerge*, но существует несколько альтернативных способов, рекомендуемых для обеспечения этой функции.

1. Используйте профили в Microsoft Edge. Каждый профиль сопоставляется с различным сеансом IE для страниц в режиме IE, поэтому их действие аналогично параметру *nomerge*.
2. Используйте командную строку `--user-data-dir=<path>`, но с разными путями для каждого сеанса. При необходимости вы можете создать служебную программу, запускаемую пользователем, которая будет запускать Microsoft Edge и изменять путь для сеанса.

Если ни один из вышеперечисленных вариантов не работает для вашего сценария, сообщите нам через один из каналов обратной связи: службу технической поддержки Майкрософт или [форум TechCommunity](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise).

### <a name="can-i-save-links-as-webpages-in-internet-explorer-mode"></a>Можно ли сохранять ссылки как веб-страницы в режиме Internet Explorer?

Да, вы можете включить параметр "Сохранить объект как" в контекстном меню для режима Internet Explorer в Microsoft Edge. Для этого настройте групповую политику *"Разрешить использование параметра "Сохранить объект как" в режиме Internet Explorer"* в разделе *Конфигурация компьютера > Административные шаблоны > Компоненты Windows > Internet Explorer*.
Механизм сохранения работает так же, как и в Internet Explorer. Если объект сохранен как HTML-файл, при повторном открытии файла страница отобразится в Microsoft Edge.
 
Обратите внимание, что для этой функции требуются следующие минимальные обновления операционной системы:
- Windows 10, версия 2004, Windows Server, версия 2004, Windows 10, версия 20H2: [KB4580364](https://support.microsoft.com/help/4580364/windows-10-update-kb4580364)
- Windows 10, версия 1903, Windows 10, версия 1909, Windows Server, версия 1903: [KB4580386](https://support.microsoft.com/help/4580386/windows-10-update-kb4580386)
- Windows 10, версия 1809, Windows Server, версия 1809, Windows Server 2019: [KB4580390](https://support.microsoft.com/help/4580390/windows-10-update-kb4580390)
- Windows 10, версия 1803: [KB4586785](https://support.microsoft.com/help/4586785/windows-10-update-kb4586785)
- Windows 10, версия 1607: [KB4586830](https://support.microsoft.com/help/4586830/windows-10-update-kb4586830)
- Windows 10, версия 1507: [KB4586787](https://support.microsoft.com/help/4586787/windows-10-update-kb4586787)


## <a name="see-also"></a>Статьи по теме

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Сведения о режиме IE](./edge-ie-mode.md)
- [Дополнительные сведения о режиме предприятия](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)