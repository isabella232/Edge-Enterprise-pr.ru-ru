---
title: Планирование перехода в режим терминала
ms.author: aguta
author: aguta
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Планирование перехода в режим терминала
ms.openlocfilehash: 95c50b39eb6e844ae4309b260087931232276d45
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642915"
---
# <a name="plan-your-kiosk-mode-transition"></a>Планирование перехода в режим терминала

В этой статье содержится руководство по переходу терминала с устаревшей версии Microsoft Edge на Microsoft Edge.  

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 87 или более поздней; каналы Stable, Beta и Dev.

> [!IMPORTANT]
> Когда 9 марта 2021 г. завершится поддержка устаревшей версии Microsoft Edge, она будет удалена и заменена Microsoft Edge на Chromium в рамках обновления Windows в апреле. Подробные сведения можно найти [в этой записи блога.](https://aka.ms/EdgeLegacyEOS) Чтобы продолжить использовать сценарии терминала на основе браузера, необходимо установить Microsoft Edge на Chromium и настроить режим терминала до выпуска Обновлений Windows за апрель на вашем устройстве.

## <a name="kiosk-setup-steps"></a>Действия по настройке терминала

Чтобы настроить терминал в Microsoft Edge, воспользуйтесь следующими действиями.

**Шаг 1. Оцените свои потребности с учетом выпущенных (и предстоящих) функциональных возможностей режима терминала.** В следующей таблице перечислены функции, поддерживаемые режимом терминала в Microsoft Edge и устаревшей версии Microsoft Edge. Используйте эту таблицу в качестве руководства по переходу на Microsoft Edge путем сравнения поддержки этих функций в обоих выпусках Microsoft Edge.

|Функция|Цифровая/интерактивная вывеска|Общедоступный просмотр|Доступно в Microsoft Edge версии (и выше)|Доступно в устаревшей версии Microsoft Edge|
|-|-|-|-|-|
|Навигация в InPrivate|Y|Y|89|Y|
|Сброс при неактивности|Y|Y|89|Y|
|[Адресная строка только для чтения](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (политика) |N|Y |89|N|
|[Удаление загружаемых данных при выходе](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (политика)  | Y|Y |89|N|
|Блокировка F11 (вход и выход из полноэкранного режима) | Y | Y | 89 |Y|
|Блокировка F12 (запуск средств разработчика) | Y | Y | 89 |Y|
| Поддержка нескольких вкладок | N| Y| 89|Y|
|[Разрешить поддержку URL-адресов](./microsoft-edge-policies.md#urlallowlist) (политика)|Y|Y|89|N|
|[Блокировать поддержку URL-адресов](./microsoft-edge-policies.md#urlblocklist) (политика)|Y|Y|89|N|
|[Показывать кнопку "Домой"](./microsoft-edge-policies.md#showhomebutton) (политика)|N|Y|89|Y|
|[Управление избранным](./microsoft-edge-policies.md#managedfavorites) (политика)|N|Y|89|Y|
|[Включить принтер](./microsoft-edge-policies.md#printingenabled) (политика)|Y|Y|89|Y|
|[Настройка URL-адреса страницы "Новая вкладка"](./microsoft-edge-policies.md#newtabpagelocation) (политика)|N|Y|89|Y|
|Кнопка завершения сеанса | N| Y| 89|Y|
|Все внутренние URL-адреса Microsoft Edge блокируются, кроме *edge://downloads* и *edge://print* |N|Y|89|Y|
| Блокировка CTRL+N (открытие нового окна) | Y | Y | 89 |Y|
| Блокировка CTRL+T (открытие новой вкладки) |Y | Y | 89 |Y|
|Параметры и другое (...) будут отображать только обязательные параметры  |Y |Y |89 |Y|
|Ограничение запуска других приложений из браузера|Y|Y|90|Y|
|Блокировка параметров печати пользовательского интерфейса|Y|Y|90|Y|
|[Настройка новой вкладки в качестве домашней страницы](./microsoft-edge-policies.md#homepageisnewtabpage) (политика)|N|Y|90|Y|

> [!NOTE]
> Сведения о расписании выпусков Microsoft Edge см. в [расписании выпусков Microsoft Edge.](microsoft-edge-release-schedule.md)

**Шаг 2. Тестирование нового терминала в Microsoft Edge.** Рекомендуется протестировать настройку режима терминала в Microsoft Edge. Быстрый и простой способ протестировать режим терминала — настроить отдельное приложение с ограниченным доступом с помощью параметров Windows, как описано далее.

1. Минимальные системные обновления для операционных систем приводятся в таблице ниже.

|Операционная система|Версия|Обновления|
|--|--|--|
|Windows 10 | 2004 или более поздней версии|[KB4601382 или более поздней версии](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows 10| 1909| [KB4601380 или более поздней версии](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

2. Чтобы протестировать новейшие функции, можно скачать последний [канал Microsoft Edge Stable](https://www.microsoftedgeinsider.com/download) версии 89 или более поздней.

   > [!IMPORTANT]
   > Поскольку требуется установка на уровне устройства, канал Canary не поддерживается.

3. На компьютере терминала откройте параметры Windows и в поле поиска введите слово "терминал". Чтобы открыть диалоговое окно для создания терминала, выберите  **Настройка терминала (ограниченный доступ)**, как показано на следующем снимке экрана.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Настройка терминала с ограниченным доступом":::

4. На странице **Настройка киоска** нажмите **Начать**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Страница терминала — начать":::

5. Введите имя для создания новой учетной записи в терминале или выберите существующую учетную запись из раскрывающегося списка и нажмите  **Далее**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Режим терминала — создание учетной записи":::

6. На странице **Выбор приложения терминала**  выберите **Microsoft Edge** и нажмите кнопку  **Далее**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5c-choose-a-kiosk-app.png" alt-text="Выберите терминал — цифровой указатель полного экрана":::

7. Выберите один из следующих вариантов отображения Microsoft Edge при работе в режиме терминала:

   - Цифровые или интерактивные вывески — отображают конкретный сайт в полноэкранном режиме в Microsoft Edge.
   - Общедоступный браузер — Запускает ограниченную версию Microsoft Edge с несколькими вкладками.
 
    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Экран режима терминала — цифровой указатель полного экрана":::

8. Нажмите  **Далее**.
9. Введите URL-адрес для загрузки при запуске киоска.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Режим терминала — введите URL-адрес":::

10. Примите значение по умолчанию (5 минут) для времени простоя или укажите свое значение.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Режим терминала — введите время простоя":::

11. Нажмите  **Далее**.
12. Закройте окно  **Параметры** , чтобы сохранить и применить свой выбор.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Режим терминала — завершение настройки":::

13. Выйдите из устройства терминала и войдите в локальную учетную запись терминала, чтобы проверить конфигурацию.

**Шаг 3. Разработка плана перехода.** На основе ваших потребностей в тестировании и организационных потребностей рекомендуется разработать план перехода и перейти на Microsoft Edge на Chromium до завершения поддержки устаревшей версии Microsoft Edge 9 марта 2021 г.

## <a name="additional-scenarios-that-require-you-to-recreate-an-existing-kiosk-mode"></a>Дополнительные сценарии, которые требуют воссоздания существующего режима терминала

При обновлении до Windows 10 версии 20H2 будет установлен Microsoft Edge на Chromium, а устаревшая версия Microsoft Edge будет скрыта. В этом случае вам потребуется снова настроить режим терминала в Microsoft Edge на Chromium.

## <a name="how-to-get-help"></a>Как получить справку

Режим терминала может быть важной частью вашей повседневной деятельности, поэтому мы хотим сделать этот переход как можно более плавным и помочь вам избежать сбоев. Если вашей компании требуется помощь при переходе на Microsoft Edge на Chromium:

- [Поддержка](https://support.serviceshub.microsoft.com/supportforbusiness/create?sapId=a77ee9b7-b6b6-aa08-d7b9-887ebe228207) доступна от корпорации Майкрософт. 
- [Поддержка FastTrack](https://www.microsoft.com/fasttrack/microsoft-365/microsoft-edge?rtc=1) также доступна без дополнительной оплаты клиентам, имеющим 150 или более платных рабочих мест Windows 10 Корпоративная.
- [Служба Assure для приложений](https://www.microsoft.com/en-us/fasttrack/microsoft-365/app-assure) доступна при возникновении проблем с совместимостью сайта или приложения.

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Новый Microsoft Edge заменит устаревшую версию Microsoft Edge в апрельском выпуске обновления Windows 10 во вторник](https://techcommunity.microsoft.com/t5/microsoft-365-blog/new-microsoft-edge-to-replace-microsoft-edge-legacy-with-april-s/ba-p/2114224)