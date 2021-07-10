---
title: Microsoft Edge и Application Guard в Microsoft Defender
ms.author: srugh
author: AndreaLBarr
manager: seanlyn
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Поддержка Microsoft Edge для Application Guard в Microsoft Defender
ms.openlocfilehash: e6498ecdb0f2bf0ecb3ae12a602b73704c6c4599
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642545"
---
# <a name="microsoft-edge-support-for-microsoft-defender-application-guard"></a>Поддержка Microsoft Edge для Application Guard в Microsoft Defender

В этой статье описывается, как Microsoft Edge поддерживает Application Guard в Microsoft Defender (Application Guard).

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## <a name="overview"></a>Обзор

Архитекторам систем безопасности на предприятии приходится иметь дело с противоречиями, которые существуют между производительностью и безопасностью. Достаточно просто заблокировать браузер, чтобы можно было загружать информацию лишь с нескольких надежных сайтов. Этот подход повысит общий уровень безопасности, но может оказаться менее продуктивным. Если снять некоторые ограничения, чтобы увеличить производительность, ухудшится профиль риска. Установить баланс совсем не просто!

Еще сложнее поспевать за новыми угрозами на фоне постоянных изменений. Браузеры остаются основной мишенью для атак на клиентских устройствах, поскольку они в основном используются для доступа к ненадежному содержимому из ненадежных источников, его загрузки и открытия. Злоумышленники постоянно разрабатывают новые мошеннические схемы и виды атак, целью которых является браузер. Предотвращение случаев нарушения безопасности или стратегии обнаружения и реагирования не могут гарантировать абсолютную защиту.

Ключевой стратегией безопасности, использование которой следует рассмотреть, является [метод предположения нарушения безопасности (Assume Breach)](/office365/Enterprise/office-365-monitoring-and-testing#assume-breach-methodology), в рамках которого предполагается, что атака будет успешной по меньшей мере один раз, несмотря на усилия предотвратить ее. Такой образ мышления побуждает создавать защиту, чтобы предотвратить последствия нарушения, благодаря чему корпоративная сеть и другие ресурсы остаются защищенными.  Эта стратегия поддерживается при развертывании Application Guard для Microsoft Edge.

## <a name="about-application-guard"></a>О расширении Application Guard

В расширении Application Guard, разработанном для Windows 10 и Microsoft Edge, используется изоляция на аппаратном уровне. Такой подход позволяет запустить навигацию по ненадежному сайту внутри контейнера. Изоляция на аппаратном уровне помогает предприятиям защитить корпоративную сеть и данные в случае, если пользователи посещают скомпрометированные или вредоносные сайты.

Администратор предприятия определяет, какие веб-сайты, облачные ресурсы и внутренние сети можно считать доверенными. Все сайты, которые не входят в список надежных сайтов, считаются ненадежными. Эти сайты изолируются от корпоративной сети и данных на устройстве пользователя.

Дополнительные сведения:

- посмотрите наше видео об [изоляции браузера Microsoft Edge с использованием Application Guard](microsoft-edge-video-security-application-guard.md)
- см. раздел [Что представляет собой Application Guard и как он работает?](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview#what-is-application-guard-and-how-does-it-work)

На следующем снимке экрана приводится пример сообщения Application Guard, показывающего, что пользователь просматривает безопасные сайты.

![Сообщение Application Guard о безопасном просмотре](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-1.png)

## <a name="whats-new"></a>Что нового

Поддержка Application Guard в новом браузере Microsoft Edge характеризуется равенством функций с устаревшей версией Microsoft Edge и включает ряд улучшений.

### <a name="favorites-synchronizing-from-the-host-to-the-container"></a>Синхронизация избранного с узла с контейнером

Некоторые из наших клиентов просили о синхронизации избранного между браузером узла и контейнером в Application Guard. Начиная с Microsoft Edge версии 91, пользователи могут настроить Application Guard для синхронизации избранного с узла с контейнером. Это гарантирует появление нового избранного в контейнере.

Управление поддержкой осуществляется с помощью политики. Чтобы включить или отключить синхронизацию избранного, обновите политику Microsoft Edge [ApplicationGuardFavoritesSyncEnabled](/deployedge/microsoft-edge-policies#applicationguardfavoritessyncenabled).

> [!Note]
> По соображениям безопасности синхронизация избранного возможна только с узла в контейнер, а не наоборот. Чтобы обеспечить единый список избранного на узле и в контейнере, мы отключили управление избранным внутри контейнера.

### <a name="identify-network-traffic-originating-from-the-container"></a>Определение трафика из контейнера

Несколько клиентов используют WDAG в определенной конфигурации, для которой нужно определить трафик из контейнера. Некоторые из возможных сценариев:

- Ограничение доступа только к нескольким недоверенным сайтам
- Разрешение доступа к Интернету только из контейнера

Начиная с Microsoft Edge версии 91, для назначения тегов трафику из контейнеров Application Guard существует встроенная поддержка, что позволяет предприятиям использовать прокси-сервер для фильтрации трафика и применять определенные политики. Вы можете использовать заголовок, чтобы определить, какой трафик проходит через контейнер или узел, с помощью [ApplicationGuardTrafficIdentificationEnabled](/deployedge/microsoft-edge-policies#applicationguardtrafficidentificationenabled).

### <a name="extension-support-inside-the-container"></a>Поддержка расширения внутри контейнера

Поддержка расширения внутри контейнера является одним из самых популярных запросов клиентов. Сценарии включают от запуска функций блокирования рекламы внутри контейнера, чтобы повысить производительность браузера, до возможности запускать настраиваемые расширения собственной разработки внутри контейнера.

Расширение, установленное внутри контейнера, поддерживается, начиная с Microsoft Edge версии 81. Управление этой поддержкой осуществляется с помощью политики. `updateURL`, которые используются в политике [ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist), следует добавить как нейтральные ресурсы в политики сетевой изоляции, используемые расширением Application Guard.

Ниже перечислены некоторые примеры поддержки контейнеров.

- Принудительная установка расширения на узле
- Удаление расширения с узла
- Блокировка расширений на узле

> [!NOTE]
> Кроме того, можно вручную установить отдельные расширения внутри контейнера из хранилища расширений. Расширения, установленные вручную, сохраняются в контейнере только в том случае, если включена политика [Разрешить сохраняемость](/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard#application-specific-settings).

### <a name="identifying-application-guard-traffic-via-dual-proxy"></a>Идентификация трафика Application Guard с использованием двойного прокси-сервера

Некоторые корпоративные пользователи разворачивают Application Guard для определенного варианта использования, при котором им необходимо идентифицировать веб-трафик, исходящий из контейнера Application Guard в Microsoft Defender на уровне прокси-сервера. С версии 84 стабильного канала Microsoft Edge поддерживает двойной прокси-сервер для соблюдения этого требования. Вы можете настроить эту функцию с помощью политики [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy).

На следующем рисунке показана архитектура двойного прокси-сервера для Microsoft Edge.

![Архитектура с двойным прокси-сервером для Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-dual-proxy.png)

### <a name="diagnostic-page-for-troubleshooting"></a>Страница диагностики для устранения неполадок

Другой проблемный вопрос для пользователей – устранение ошибок конфигурации Application Guard на устройстве, если сообщается о проблеме. В Microsoft Edge есть страница диагностики (`edge://application-guard-internals`), с помощью которой пользователи могут устранять неполадки. В эту диагностику входит проверка достоверности URL-адреса на основе конфигурации, используемой на устройстве пользователя.

На следующем снимке экрана показана страница диагностики на нескольких вкладках, помогающая диагностировать обнаруженные пользователями неполадки на устройстве.

![Страница диагностики Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-2.png)

### <a name="microsoft-edge-updates-in-the-container"></a>Обновления Microsoft Edge в контейнере

Обновления устаревшей версии Microsoft Edge в контейнере входят в цикл обновления ОС Windows. Так как новая версия Microsoft Edge обновляется независимо от ОС Windows, она не зависит от обновлений контейнера. Канал и версия Microsoft Edge реплицируются внутри контейнера.

## <a name="prerequisites"></a>Предварительные условия

К устройствам, использующим Application Guard в Microsoft Edge, применяются следующие требования:

- Windows 10 1809 (RS5) и более поздней версии.
- Только номера SKU клиентов Windows

  > [!NOTE]
  > Расширение Application Guard поддерживается только для номеров SKU клиентов Windows 10 Pro и Windows 10 Корпоративная.

- Одно из решений для управления, описанных в статье [Требования к программному обеспечению](/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard#software-requirements)

## <a name="how-to-install-application-guard"></a>Установка Application Guard

В следующих статьях приведены сведения, необходимые для установки, настройки и тестирования Application Guard в Microsoft Edge.

- [Требования к системе](/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard)
- [Установка Application Guard в Microsoft Defender](/windows/security/threat-protection/microsoft-defender-application-guard/install-md-app-guard)
- [Настройка параметров групповой политики Microsoft Defender](/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard)
- [Тестирование Application Guard](/windows/security/threat-protection/microsoft-defender-application-guard/test-scenarios-md-app-guard)

## <a name="frequently-asked-questions"></a>Часто задаваемые вопросы

### <a name="does-application-guard-work-in-ie-mode"></a>Работает ли Application Guard в режиме IE?

Функциональность Application Guard поддерживается в режиме IE, но мы не ожидаем особой пользы от данного компонента в этом режиме. Режим IE рекомендуется развертывать для списка доверенных внутренних сайтов, а Application Guard — только для недоверенных сайтов. Убедитесь в том, что все сайты и IP-адреса в режиме IE также добавлены в политику сетевой изоляции, чтобы они рассматривались как надежные ресурсы в Application Guard.

### <a name="do-i-need-to-install-the-application-guard-chrome-extension"></a>Нужно ли мне устанавливать расширение Application Guard для Chrome?

Нет, для функции Application Guard имеется встроенная поддержка в Microsoft Edge. На самом деле, расширение Application Guard для Chrome не поддерживается в Microsoft Edge.

### <a name="are-there-any-other-platform-related-faqs"></a>Есть ли другие вопросы и ответы, связанные с платформой?

Да. [Вопросы и ответы об Application Guard в Microsoft Defender](/windows/security/threat-protection/microsoft-defender-application-guard/faq-md-app-guard) 

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Advanced Threat Protection в Microsoft Defender](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [Видео. Изоляция браузера Microsoft Edge с использованием Application Guard](https://www.youtube.com/watch?v=zQjaRqNXMqw&t=3s)