---
title: Настройка режима терминала в Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 03/16/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Сведения о возможностях режима терминала и настройке параметров режима терминала Microsoft Edge.
ms.openlocfilehash: 9d76bfcaebeaf56e627a401cc4f0375bce9d17a3
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448133"
---
# <a name="configure-microsoft-edge-kiosk-mode"></a>Настройка режима терминала в Microsoft Edge

В этой статье рассказывается, как настроить параметры режим терминала в Microsoft Edge. Кроме того, представлена дорожная карта реализации функций, над которыми мы работаем.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 87 или более поздней.

> [!IMPORTANT]
> Вызов функций режима терминала Microsoft Edge в Windows 10 с помощью аргументов командной строки, указанных в статье [Использование возможностей режима терминала](#use-kiosk-mode-features).

## <a name="overview"></a>Обзор

Режим терминала Microsoft Edge предлагает два варианта блокировки браузера, чтобы организации могли создавать, управлять и обеспечивать наилучшие условия для своих клиентов. Доступны следующие варианты блокировки:  

- **Цифровые или интерактивные вывески** отображают конкретный сайт в полноэкранном режиме.
- **Общедоступный просмотр** запускает ограниченную версию Microsoft Edge с несколькими вкладками.

В обоих случаях выполняется сеанс Microsoft Edge InPrivate, который защищает пользовательские данные.

## <a name="set-up-microsoft-edge-kiosk-mode"></a>Настройка режима терминала в Microsoft Edge

Начальный набор функций режима терминала доступен для тестирования в стабильном канале Microsoft Edge, версия 87. Последнюю версию можно скачать из [Microsoft Edge (официальный стабильный канал).](https://www.microsoft.com/edge)

### <a name="kiosk-mode-supported-features"></a>Поддерживаемые функции режима терминала

В следующей таблице перечислены функции, поддерживаемые режимом терминала в Microsoft Edge и Microsoft Edge Legacy. Используйте эту таблицу в качестве руководства по переходу на Microsoft Edge путем сравнения поддержки этих функций в обеих версиях Microsoft Edge.

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
|[Настройка URL-адреса страницы "Новая вкладка"](./microsoft-edge-policies.md#newtabpagelocation) (политика)|N|Y||Y|
|Кнопка завершения сеанса * | N| Y| 89|Y|
|Все внутренние URL-адреса Microsoft Edge блокируются, кроме *edge://downloads* и *edge://print* |N|Y|89|Y|
| Блокировка CTRL+N (открытие нового окна) * | Y | Y | 89 |Y|
| Блокировка CTRL+T (открытие новой вкладки) |Y | N | 89 |Y|
|Параметры и другое (...)будут отображать только обязательные параметры  |Y |Y |89 |Y|
|Ограничение запуска других приложений из браузера|Y|Y|90/91|Y|
|Блокировка параметров печати пользовательского интерфейса|Y|Y|90/91|Y|
|[Настройка новой вкладки в качестве домашней страницы](./microsoft-edge-policies.md#homepageisnewtabpage) (политика)|-|-|ПОДЛЕЖИТ УТОЧНЕНИЮ|Y|

> [!NOTE]
> Функции с символом "*" в конце включены только в сценарии одного приложения с ограниченным доступом.

## <a name="use-kiosk-mode-features"></a>Использование возможностей режима терминала

Функции режима терминала Microsoft Edge можно вызывать с помощью следующих параметров командной строки Windows 10 для цифровых и интерактивных вывесок и просмотра общедоступных страниц.

### <a name="kiosk-mode-digitalinteractive-signage"></a>Цифровая/интерактивная вывеска в режиме терминала
 
```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen
```

### <a name="kiosk-mode-public-browsing"></a>Режим терминала : общедоступный просмотр

```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing
```

### <a name="additional-command-line-options"></a>Дополнительные параметры командной строки

- **--no-first-run**: Отключить функцию первого запуска Microsoft Edge.

   ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --no-first-run
  ```

  ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --no-first-run
  ```

- **--kiosk-idle-timeout-minutes=**: изменить время в минутах от последнего действия пользователя до того, как режим терминала Microsoft Edge сбросит сеанс пользователя.. Замените слово "значение" в следующем примере на количество минут.

   ```
   --kiosk-idle-timeout-minutes=value
   ``` 
   Поддерживаются следующие "значения":

     - Значения по умолчанию (в минутах)
       - Полноэкранный режим — 0 (отключен)
       - Общедоступный просмотр — 5 минут
    - Допустимые значения
      - 0 — отключение таймера
      - 1-1440 минут для сброса таймера простоя


    ```
    msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --kiosk-idle-timeout-minutes=1
   ```

   ```
   msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --kiosk-idle-timeout-minutes=1
   ```

## <a name="support-policies-for-kiosk-mode"></a>Поддерживаемые политики режима терминала

Используйте любую из политик Microsoft Edge, перечисленных в следующей таблице, чтобы улучшить работу терминала для настроенного вами типа режима терминала Microsoft Edge. Дополнительные информацию об этих политиках см. в [справочнике по политикам браузера Microsoft Edge](./microsoft-edge-policies.md).

> [!NOTE]
> Конфигурация политик не ограничивается политиками, перечисленными в следующей таблице, однако другие политики следует проверить и убедиться, что они не оказывают негативного влияния на функциональность режима терминала.

|Групповая политика|Цифровая/интерактивная вывеска|Одно приложение для общего просмотра|
|--|--|--|
|[Вывод на печать](./microsoft-edge-policies.md#printing-policies) | Y|Y |
|[HomePageLocation](./microsoft-edge-policies.md#homepagelocation) |N | Y|
|[ShowHomeButton](./microsoft-edge-policies.md#showhomebutton) |N | Y|
|[NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) |N |Y |
|[FavoritesBarEnabled](./microsoft-edge-policies.md#favoritesbarenabled) |N |Y |
|[URLAllowlist](./microsoft-edge-policies.md#urlallowlist) |Y |Y |
|[URLBlocklist](./microsoft-edge-policies.md#urlblocklist) |Y | Y|
|[ManagedSearchEngines](./microsoft-edge-policies.md#managedsearchengines) |N | Y|
|[UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed) |N | Y|
|[VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) | N|Y |
|[Параметры SmartScreen](./microsoft-edge-policies.md#smartscreen-settings-policies) |Y |Y |
|[EdgeCollectionsEnabled](./microsoft-edge-policies.md#edgecollectionsenabled)|Y|Y|

## <a name="microsoft-edge-with-assigned-access"></a>Microsoft Edge с ограниченным доступом

### <a name="single-app-kiosk"></a>Режим терминала с одним приложением

В настоящее время Microsoft Edge поддерживает набор таких же типов режимов терминала с ограниченным доступом для одного приложения, как и устаревшая версия Microsoft Edge, со следующими вариантами блокировки: цифровая или интерактивная вывеска и общедоступный просмотр.  

Режим терминала Microsoft Edge с одним приложением назначенного доступа в настоящее время доступен для тестирования в составе последней сборки [Windows 10 Insider Preview](https://insider.windows.com/)версии 20215 или более поздней версии, а также в [Microsoft Edge Beta Channel](https://www.microsoftedgeinsider.com/download)версии 89 или более поздней версии.

**Откуда загрузить Windows Insider Preview?**

Чтобы установить сборку Windows 10 Insider Preview на компьютер с Windows, следуйте инструкциям, указанным в разделе  [Начало работы со сборками Windows 10 Insider Preview](/windows-insider/get-started).

### <a name="multi-app-kiosk"></a>Режим терминала с несколькими приложениями

Microsoft Edge можно запустить с [ограниченным доступом для нескольких приложений](/windows/configuration/lock-down-windows-10-to-specific-apps) в Windows 10, что является эквивалентом типа режима терминала «Обычный просмотр веб-страниц» в устаревшей версии Microsoft Edge. Чтобы настроить ограниченный доступ для нескольких приложений в Microsoft Edge, следуйте инструкциям по [настройке режима терминала с несколькими приложениями](/windows/configuration/lock-down-windows-10-to-specific-apps). (AUMID для Microsoft Edge из стабильного канала— **MSEdge**).

При использовании Microsoft Edge с назначенным доступом для нескольких приложений можно настроить терминал Microsoft Edge для использования [политик браузера Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies), чтобы задать условия просмотра в зависимости от ваших уникальных требований.

### <a name="configure-using-windows-settings"></a>Настройка с помощью параметров Windows

Параметры Windows — это самый простой способ настроить одно или два устройства с одним приложением в режиме терминала. Для настройки компьютера с одним приложением в режиме терминала выполните указанные ниже действия.

1. Установите последний выпуск Windows 10 Insider Preview версии 20215 или выше. Следуйте инструкциям в разделе [Начало работы со сборками Windows 10 Insider Preview](/windows-insider/get-started).
2. Чтобы протестировать новейшие функции, можно скачать последний канал [Microsoft Edge beta](https://www.microsoftedgeinsider.com/download)версии 89 или более поздней версии.
3. На компьютере терминала откройте параметры Windows и в поле поиска введите слово «терминал». Чтобы открыть диалоговое окно для создания терминала, выберите  **Настройка терминала (ограниченный доступ)**, как показано на следующем снимке экрана.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Настройка терминала с ограниченным доступом":::

4. На странице **Настройка киоска** нажмите **Начать**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Страница терминала — начать":::

5. Введите имя для создания новой учетной записи в терминале или выберите существующую учетную запись из раскрывающегося списка и нажмите  **Далее**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Режим терминала — создание учетной записи":::

6. На странице **Выбор приложения терминала**  выберите **Microsoft Edge** и нажмите кнопку  **Далее**.

   > [!NOTE]
   > Это относится только к каналам Microsoft Edge Dev, бета-версиям канала и стабильным каналам.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Режим терминала — выбор приложения":::

7. Выберите один из следующих вариантов отображения Microsoft Edge при работе в режиме терминала:

   - Цифровые или интерактивные вывески — Отображают конкретный сайт в полноэкранном режиме в Microsoft Edge.
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

## <a name="functional-limitations"></a>Функциональные ограничения

С выпуском этой предварительной версии режима терминала мы продолжаем работать над улучшением продукта и добавлением новых функций.

В настоящее время не поддерживаются следующие функции и рекомендуется их отключить:

- [InPrivateModeAvailability](./microsoft-edge-policies.md#inprivatemodeavailability)
- [IsolateOrigins](./microsoft-edge-policies.md#isolateorigins)
- [ManagedFavorites](./microsoft-edge-policies.md#managedfavorites)
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled)
- [EdgeCollectionsEnabled](./microsoft-edge-policies.md#edgecollectionsenabled)
- [UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed)
- [DefaultPopupsSetting](./microsoft-edge-policies.md#defaultpopupssetting)
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled)
- [InternetExplorerIntegrationLevel](./microsoft-edge-policies.md#internetexplorerintegrationlevel)
- [Расширения](./microsoft-edge-policies.md#extensions-policies)
- [BackgroundModeEnabled](./microsoft-edge-policies.md#backgroundmodeenabled)
- [UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed)

## <a name="roadmap"></a>Стратегия

### <a name="in-early-2021"></a>В начале 2021 года

Будут добавлены следующая поддержка и возможности:

- Общая доступность режима киоска Microsoft Edge с одним приложением с единым доступом в Windows 10 1909 и более поздних версиях.
- Дополнительные возможности для обеспечения равных условий с устаревшей версией Microsoft Edge.
- Интеграция с Intune для настройки устройств с использованием пользовательского интерфейса профиля режима терминала.
- Ограничение запуска других приложений из браузера.
- Блокировка параметров печати пользовательского интерфейса.

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Планирование развертывания Microsoft Edge](deploy-edge-plan-deployment.md)
- [Настройка терминалов и цифровых вывесок в выпусках Windows для настольных компьютеров](/windows/configuration/kiosk-methods)
- [Планирование перехода в режим терминала](microsoft-edge-kiosk-mode-transition-plan.md)