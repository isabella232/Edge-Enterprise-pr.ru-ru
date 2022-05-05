---
title: Настройка режима терминала в Microsoft Edge
ms.author: v-danwesley
author: dan-wesley
manager: srugh
ms.date: 05/02/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Сведения о возможностях режима терминала и настройке параметров режима терминала Microsoft Edge.
ms.openlocfilehash: 17ec165ce86155a03e5adc757ddafcad3e3c9819
ms.sourcegitcommit: 592f6e40b13e28af588473b2a75c3ae697e5db2d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2022
ms.locfileid: "12505502"
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
|Блокировка F11 (вход и выход из полноэкранного режима) | Y | Y |89|Y|
|Блокировка F12 (запуск средств разработчика) | Y | Y |89|Y|
| Поддержка нескольких вкладок | N| Y|89|Y|
|[Разрешить поддержку URL-адресов](./microsoft-edge-policies.md#urlallowlist) (политика)|Y|Y|89|N|
|[Блокировать поддержку URL-адресов](./microsoft-edge-policies.md#urlblocklist) (политика)|Y|Y|89|N|
|[Показывать кнопку "Домой"](./microsoft-edge-policies.md#showhomebutton) (политика)|N|Y|89|Y|
|[Управление избранным](./microsoft-edge-policies.md#managedfavorites) (политика)|N|Y|89|Y|
|[Включить принтер](./microsoft-edge-policies.md#printingenabled) (политика)|Y|Y|89|Y|
|[Настройка URL-адреса страницы "Новая вкладка"](./microsoft-edge-policies.md#newtabpagelocation) (политика)|N|Y|89|Y|
|Кнопка завершения сеанса * | N| Y|89|Y|
|Все внутренние URL-адреса Microsoft Edge блокируются, кроме *edge://downloads* и *edge://print* |N|Y|89|Y|
| Блокировка CTRL+N (открытие нового окна) * | Y | Y |89|Y|
| Блокировка CTRL+T (открытие новой вкладки) |Y | N |89|Y|
|Параметры и другое (...) будут отображать только обязательные параметры  |Y |Y |89|Y|
|Ограничение запуска других приложений из браузера|Y|Y|90|Y|
|Блокировка параметров печати пользовательского интерфейса|Y|Y|90|Y|
|[Настройка новой вкладки в качестве домашней страницы](./microsoft-edge-policies.md#homepageisnewtabpage) (политика)|N|Y|90|Y|

> [!NOTE]
> Функции с символом "*" в конце включены только в сценарии одного приложения с ограниченным доступом.

## <a name="use-kiosk-mode-features"></a>Использование возможностей режима терминала

Microsoft Edge режима киоска можно вызвать с помощью следующих параметров Windows 10 командной строки для цифровых и интерактивных вывесок и общедоступного просмотра.

### <a name="kiosk-mode-digitalinteractive-signage"></a>Цифровая/интерактивная вывеска в режиме терминала
 
```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen
```

### <a name="kiosk-mode-public-browsing"></a>Режим терминала : общедоступный просмотр

```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing
```

### <a name="kiosk-mode-download-files-on-exit"></a>Загрузка файлов в режиме киоска при выходе

Чтобы настроить Microsoft Edge для удаления скачанных файлов при закрытии экземпляра киоска, необходимо настроить следующие две групповые политики:
- [Удаление скачиваемых файлов при выходе](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) = включено
- [Set download directory](./microsoft-edge-policies.md#downloaddirectory) = ${local_app_data}\Microsoft\Edge\KioskDownloads 


### <a name="additional-command-line-options"></a>Дополнительные параметры командной строки

- **--no-first-run**: Отключить функцию первого запуска Microsoft Edge.

   ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --no-first-run
  ```

  ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --no-first-run
  ```

- **--kiosk-idle-timeout-minutes=**: измените время (в минутах) с последнего действия пользователя, прежде чем Microsoft Edge режим киоска сбрасывает сеанс пользователя, закрыв браузер. Примечание. Этот флаг не будет перезапущен Microsoft Edge после закрытия. Для автоматического перезапуска Edge после истечении времени ожидания простоя требуется отдельная технология, например назначенный доступ или запуск оболочки. Замените слово "значение" в следующем примере на количество минут.

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

### <a name="single-app-kiosk"></a>Киоск с одним приложением

Режим киоска в Microsoft Edge версии 90 предлагает обширный список возможностей. См. раздел "Поддерживаемые возможности режима киоска".
Следующие обновления Windows позволяют настроить Microsoft Edge с помощью одного приложения с ограниченным доступом.

|Операционная система|Версия|Обновления|
|--|--|--|
|Windows 10 | 2004 или более поздней версии|[KB4601382 или более поздней версии](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows 10| 1909| [KB4601380 или более поздней версии](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

Вы можете управлять одним приложением с ограниченным доступом в режиме киоска в Microsoft Edge с помощью [параметров Windows](/deployedge/microsoft-edge-configure-kiosk-mode#configure-using-windows-settings) и Intune.

### <a name="multi-app-kiosk"></a>Киоск с несколькими приложениями

Microsoft Edge можно запустить с [ограниченным доступом для нескольких приложений](/windows/configuration/lock-down-windows-10-to-specific-apps) в Windows 10, что является эквивалентом типа режима терминала «Обычный просмотр веб-страниц» в устаревшей версии Microsoft Edge. Чтобы настроить ограниченный доступ для нескольких приложений в Microsoft Edge, следуйте инструкциям по [настройке режима терминала с несколькими приложениями](/windows/configuration/lock-down-windows-10-to-specific-apps). (AUMID для канала Microsoft Edge Stable **Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe! MSEDGE**).

При использовании Microsoft Edge с доступом с несколькими приложениями можно настроить киоск Microsoft Edge для использования политик браузера [Microsoft Edge](./microsoft-edge-policies.md) для настройки интерфейса просмотра в соответствии с вашими уникальными требованиями.

### <a name="configure-using-windows-settings"></a>Настройка с помощью параметров Windows

Параметры Windows — это самый простой способ настроить одно или два устройства с одним приложением в режиме терминала. Для настройки киоска с одним приложением выполните указанные ниже действия.

1. Минимальные обновления для операционных систем приводятся в таблице ниже.

|Операционная система|Версия|Обновления|
|--|--|--|
|Windows 10 | 2004 или более поздней версии|[KB4601382 или более поздней версии](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows 10| 1909| [KB4601380 или более поздней версии](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

2. Чтобы протестировать новые возможности, можно скачать [Microsoft Edge Stable](https://www.microsoft.com/edge/business/download) версии 89 или более поздней.

3. На компьютере в режиме киоска откройте параметры Windows и в поле поиска введите слово "киоск". Чтобы открыть диалоговое окно для создания терминала, выберите  **Настройка терминала (ограниченный доступ)**, как показано на следующем снимке экрана.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Настройка терминала с ограниченным доступом":::

4. На странице **"Настройка киоска**  **"** выберите начало работы.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Страница терминала — начать":::

5. Введите имя, чтобы создать новую учетную запись киоска, или выберите существующую учетную запись из заполненного раскрывающегося списка, а затем  **selectNext**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Режим терминала — создание учетной записи":::

6. На странице **"Выбор киоска** " выберите Microsoft Edge, **а** затем  **selectNext**.

   > [!NOTE]
   > Это относится только к каналам Microsoft Edge Dev, Beta и Stable.

     :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5c-choose-a-kiosk-app.png" alt-text="Отображение режима киоска — цифровой указатель полноэкранного режима":::

7. Выберите один из следующих вариантов отображения Microsoft Edge при работе в режиме киоска:

   - Цифровые или интерактивные вывески — Отображают конкретный сайт в полноэкранном режиме в Microsoft Edge.
   - Общедоступный браузер — запускает ограниченную версию Microsoft Edge с несколькими вкладками.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Способ использования киоска — цифровой указатель полноэкранного режима":::

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
- [Расширения](./microsoft-edge-policies.md#extensions-policies)
- [BackgroundModeEnabled](./microsoft-edge-policies.md#backgroundmodeenabled)
- [UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed)

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Планирование развертывания Microsoft Edge](deploy-edge-plan-deployment.md)
- [Настройка терминалов и цифровых вывесок в выпусках Windows для настольных компьютеров](/windows/configuration/kiosk-methods)
- [Планирование перехода в режим терминала](microsoft-edge-kiosk-mode-transition-plan.md)
