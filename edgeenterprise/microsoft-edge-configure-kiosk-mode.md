---
title: Настройка режима терминала в Microsoft Edge
ms.author: aguta
author: aguta
manager: srugh
ms.date: 01/21/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Настройка режима терминала в Microsoft Edge
ms.openlocfilehash: be353a0e13e9234de40296a2e8dcc31b1b800f52
ms.sourcegitcommit: 8a88fd38bdb5e132e89bf17dd2b5fb72f5d1b4b9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297475"
---
# Настройка режима терминала в Microsoft Edge

В этой статье рассказывается, как настроить параметры режим терминала в Microsoft Edge. Кроме того, представлена дорожная карта реализации функций, над которыми мы работаем.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 87 или более поздней.

## Обзор

Режим терминала Microsoft Edge предлагает два варианта блокировки браузера, чтобы организации могли создавать, управлять и обеспечивать наилучшие условия для своих клиентов. Доступны следующие варианты блокировки:  

- **Цифровые или интерактивные вывески** отображают конкретный сайт в полноэкранном режиме.
- **Общедоступный просмотр** запускает ограниченную версию Microsoft Edge с несколькими вкладками.

В обоих случаях выполняется сеанс Microsoft Edge InPrivate, который защищает пользовательские данные.

## Настройка режима терминала в Microsoft Edge

Начальный набор функций режима терминала доступен для тестирования в стабильном канале Microsoft Edge, версия 87. Последнюю версию можно скачать из [Microsoft Edge (официальный стабильный канал).](https://www.microsoft.com/edge)

### Поддерживаемые функции режима терминала

В следующей таблице перечислены функции, поддерживаемые режимом терминала.

|Функция|Цифровая/интерактивная вывеска|Общедоступный просмотр|Доступно в Microsoft Edge версии (и выше)|
|-|-|-|-|
|Навигация в InPrivate|Y|Y|87|
|Сброс при неактивности|Y|Y|87|
|[Адресная строка только для чтения](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (политика) |N|Y |87|
|[Удаление загружаемых данных при выходе](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (политика)  | Y|Y |87|
|Блокировка F11 (вход и выход из полноэкранного режима) | Y | Y | 87 |
|Блокировка F12 (запуск средств разработчика) | Y | Y | 87 |
| Поддержка нескольких вкладок | N| Y| 87|
|Кнопка завершения сеанса | N| Y| 88|
|Все внутренние URL-адреса Microsoft Edge блокируются, кроме *edge://downloads* и *edge://print* |N|Y|88|
| Блокировка CTRL+N (открытие нового окна) | Y | Y | 89 |
| Блокировка CTRL+T (открытие новой вкладки) | N | Y | 89 |
|Параметры и другое (...)— отображение только обязательных параметров  |N |Y |89 |

> [!NOTE]
> По мере развития режима терминала будет появляться все больше функций.

## Использование возможностей режима терминала

Функции режима терминала Microsoft Edge можно вызывать с помощью следующих параметров командной строки Windows 10:

- Цифровая или интерактивная вывеска режима терминала: `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- Общедоступный просмотр режима терминала: `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### Дополнительные параметры командной строки

- `--no-first-run` : Отключение первого запуска Microsoft Edge.
- `--kiosk-idle-timeout-minutes` : Изменение времени в минутах от последнего действия пользователя до того, как режим терминала Microsoft Edge сбросит сеанс пользователя. Поддерживаются следующие значения:

  - Значения по умолчанию
    - Полный экран — отключен
    - Общедоступный просмотр — 5 минут
  - Допустимые значения
    - 0 — отключение таймера
    - 1-1440 минут для сброса таймера простоя

## Поддерживаемые политики режима терминала

Используйте любую из политик Microsoft Edge, перечисленных в следующей таблице, чтобы улучшить работу терминала для настроенного вами типа режима терминала Microsoft Edge. Дополнительные информацию об этих политиках см. в [справочнике по политикам браузера Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-policies).

> [!NOTE]
> Конфигурация политик не ограничивается политиками, перечисленными в следующей таблице, однако другие политики следует проверить и убедиться, что они не оказывают негативного влияния на функциональность режима терминала.

|Групповая политика|Цифровая/интерактивная вывеска|Одно приложение для общего просмотра|
|--|--|--|
|[Вывод на печать](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printing-policies) | Y|Y |
|[HomePageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation) |N | Y|
|[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton) |N | Y|
|[NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) |N |Y |
|[FavoritesBarEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled) |N |Y |
|[URLAllowlist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) |Y |Y |
|[URLBlocklist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) |Y | Y|
|[ManagedSearchEngines](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedsearchengines) |N | Y|
|[UserFeedbackAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed) |N | Y|
|[VerticalTabsAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#verticaltabsallowed) | N|Y |
|[Параметры SmartScreen](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreen-settings-policies) |Y |Y |

## Microsoft Edge с ограниченным доступом

### Режим терминала с одним приложением

В настоящее время Microsoft Edge поддерживает набор таких же типов режимов терминала с ограниченным доступом для одного приложения, как и устаревшая версия Microsoft Edge, со следующими вариантами блокировки: цифровая или интерактивная вывеска и общедоступный просмотр.  

Режим терминала с ограниченным доступом в настоящее время доступен для тестирования в последней  [сборке Windows 10 Insider Preview](https://insider.windows.com/) версии 20215 или выше, а также в  [канале Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download) версии 87.0.644.4 или выше.

**Откуда загрузить Windows Insider Preview?**

Чтобы установить сборку Windows 10 Insider Preview на компьютер с Windows, следуйте инструкциям, указанным в разделе  [Начало работы со сборками Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).

### Режим терминала с несколькими приложениями

Microsoft Edge можно запустить с [ограниченным доступом для нескольких приложений](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) в Windows 10, что является эквивалентом типа режима терминала «Обычный просмотр веб-страниц» в устаревшей версии Microsoft Edge. Чтобы настроить ограниченный доступ для нескольких приложений в Microsoft Edge, следуйте инструкциям по [настройке режима терминала с несколькими приложениями](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps). (AUMID для Microsoft Edge из стабильного канала— **MSEdge**).

При использовании Microsoft Edge с назначенным доступом для нескольких приложений можно настроить терминал Microsoft Edge для использования [политик браузера Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies), чтобы задать условия просмотра в зависимости от ваших уникальных требований.

### Настройка с помощью параметров Windows

Параметры Windows — это самый простой способ настроить одно или два устройства с одним приложением в режиме терминала. Для настройки компьютера с одним приложением в режиме терминала выполните указанные ниже действия.

1. Установите последний выпуск Windows 10 Insider Preview версии 20215 или выше. Следуйте инструкциям, указанным в разделе [Начало работы со сборками Windows 10 Insider Preview](https://docs.microsoft.com/windows-insider/get-started).
2. Установите последнюю версию [стабильного канала Microsoft Edge](https://www.microsoft.com/edge) версии 87 или более поздней.  Чтобы протестировать новейшие функции, можно скачать последний канал [Microsoft Edge Dev](https://www.microsoftedgeinsider.com/download)версии 89 или более поздней версии.

   > [!IMPORTANT]
   > Поскольку требуется установка на уровне устройства, поддерживается только канал, не связанный с Canary.

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

## Функциональные ограничения

С выпуском этой предварительной версии режима терминала мы продолжаем работать над улучшением продукта и добавлением новых функций.

Мы рекомендуем отключить:

- [StartupBoostEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#startupboostenabled)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [Расширения](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions-policies)
- [BackgroundModeEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#backgroundmodeenabled)

## Стратегия

### В начале 2021 года

Будут добавлены следующая поддержка и возможности:

- Общая доступность режима киоска Microsoft Edge с одним приложением с единым доступом в Windows 10 1909 и более поздних версиях.
- Дополнительные возможности для обеспечения равных условий с устаревшей версией Microsoft Edge.
- Интеграция с Intune для настройки устройств с использованием пользовательского интерфейса профиля режима терминала.
- Дополнительные сочетания клавиш будут заблокированы.
- Ограничение запуска других приложений из браузера.

## См. также

- [Настройка терминалов и цифровых вывесок в выпусках Windows для настольных компьютеров](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Развертывание режима терминала в Microsoft Edge Legacy](https://aka.ms/edgekioskmode)
- [Планирование развертывания Microsoft Edge](deploy-edge-plan-deployment.md)
- [Использование целевой страницы Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
