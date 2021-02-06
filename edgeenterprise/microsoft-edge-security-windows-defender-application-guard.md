---
title: Microsoft Edge и Application Guard в Microsoft Defender
ms.author: srugh
author: dan-wesley
manager: seanlyn
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Поддержка Microsoft Edge для Application Guard в Microsoft Defender
ms.openlocfilehash: 751201192c3b4e69cc866f35e51a6db23b9972f9
ms.sourcegitcommit: c290b0b0fa6b7d7f94dcdfdda91302da733326ec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314592"
---
# Поддержка Microsoft Edge для Application Guard в Microsoft Defender

В этой статье описывается, как Microsoft Edge поддерживает Application Guard в Microsoft Defender (Application Guard).

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## Обзор

Архитекторам систем безопасности на предприятии приходится иметь дело с противоречиями, которые существуют между производительностью и безопасностью. Достаточно просто заблокировать браузер, чтобы можно было загружать информацию лишь с нескольких надежных сайтов. Этот подход повысит общий уровень безопасности, но может оказаться менее продуктивным. Если снять некоторые ограничения, чтобы увеличить производительность, ухудшится профиль риска. Установить баланс совсем не просто!

Еще сложнее поспевать за новыми угрозами на фоне постоянных изменений. Браузеры остаются основной мишенью для атак на клиентских устройствах, поскольку они в основном используются для доступа к ненадежному содержимому из ненадежных источников, его загрузки и открытия. Злоумышленники постоянно разрабатывают новые мошеннические схемы и виды атак, целью которых является браузер. Предотвращение случаев нарушения безопасности или стратегии обнаружения и реагирования не могут гарантировать абсолютную защиту.

Ключевой стратегией безопасности, использование которой следует рассмотреть, является [метод предположения нарушения безопасности (Assume Breach)](https://docs.microsoft.com/office365/Enterprise/office-365-monitoring-and-testing#assume-breach-methodology), в рамках которого предполагается, что атака будет успешной по меньшей мере один раз, несмотря на усилия предотвратить ее. Такой образ мышления побуждает создавать защиту, чтобы предотвратить последствия нарушения, благодаря чему корпоративная сеть и другие ресурсы остаются защищенными.  Эта стратегия поддерживается при развертывании Application Guard для Microsoft Edge.

## О расширении Application Guard

В расширении Application Guard, разработанном для Windows 10 и Microsoft Edge, используется изоляция на аппаратном уровне. Такой подход позволяет запустить навигацию по ненадежному сайту внутри контейнера. Изоляция на аппаратном уровне помогает предприятиям защитить корпоративную сеть и данные в случае, если пользователи посещают скомпрометированные или вредоносные сайты.

Администратор предприятия определяет, какие веб-сайты, облачные ресурсы и внутренние сети можно считать доверенными. Все сайты, которые не входят в список надежных сайтов, считаются ненадежными. Эти сайты изолируются от корпоративной сети и данных на устройстве пользователя.

Дополнительные сведения:

- посмотрите наше видео об [изоляции браузера Microsoft Edge с использованием Application Guard](microsoft-edge-video-security-application-guard.md)
- см. раздел [Что представляет собой Application Guard и как он работает?](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview#what-is-application-guard-and-how-does-it-work)

На следующем снимке экрана приводится пример сообщения Application Guard, показывающего, что пользователь просматривает безопасные сайты.

![Сообщение Application Guard о безопасном просмотре](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-1.png)

## Что нового

Поддержка Application Guard в новом браузере Microsoft Edge характеризуется равенством функций с устаревшей версией Microsoft Edge и включает ряд улучшений.

### Поддержка расширения внутри контейнера

Поддержка расширения внутри контейнера является одним из самых популярных запросов клиентов. Сценарии включают от запуска функций блокирования рекламы внутри контейнера, чтобы повысить производительность браузера, до возможности запускать настраиваемые расширения собственной разработки внутри контейнера.

Расширение, установленное внутри контейнера, поддерживается, начиная с Microsoft Edge версии 81. Управление этой поддержкой осуществляется с помощью политики. `updateURL`, которые используются в политике [ExtensionInstallForcelist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#extensioninstallforcelist), следует добавить как нейтральные ресурсы в политики сетевой изоляции, используемые расширением Application Guard.

Ниже перечислены некоторые примеры поддержки контейнеров.

- Принудительная установка расширения на узле
- Удаление расширения с узла
- Блокировка расширений на узле

> [!NOTE]
> Кроме того, можно вручную установить отдельные расширения внутри контейнера из хранилища расширений. Расширения, установленные вручную, сохраняются в контейнере только в том случае, если включена политика [Разрешить сохраняемость](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard#application-specific-settings).

### Идентификация трафика Application Guard с использованием двойного прокси-сервера

Некоторые корпоративные пользователи разворачивают Application Guard для определенного варианта использования, при котором им необходимо идентифицировать веб-трафик, исходящий из контейнера Application Guard в Microsoft Defender на уровне прокси-сервера. С версии 84 стабильного канала Microsoft Edge поддерживает двойной прокси-сервер для соблюдения этого требования. Вы можете настроить эту функцию с помощью политики [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy).

На следующем рисунке показана архитектура двойного прокси-сервера для Microsoft Edge.

![Архитектура с двойным прокси-сервером для Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-dual-proxy.png)

### Страница диагностики для устранения неполадок

Другой проблемный вопрос для пользователей– устранение ошибок конфигурации Application Guard на устройстве, если сообщается о проблеме. В Microsoft Edge есть страница диагностики (`edge://application-guard-internals`), с помощью которой пользователи могут устранять неполадки. В эту диагностику входит проверка достоверности URL-адреса на основе конфигурации, используемой на устройстве пользователя.

На следующем снимке экрана показана страница диагностики на нескольких вкладках, помогающая диагностировать обнаруженные пользователями неполадки на устройстве.

![Страница диагностики Application Guard](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-2.png)

### Обновления Microsoft Edge в контейнере

Обновления устаревшей версии Microsoft Edge в контейнере входят в цикл обновления ОС Windows. Так как новая версия Microsoft Edge обновляется независимо от ОС Windows, она не зависит от обновлений контейнера. Канал и версия Microsoft Edge реплицируются внутри контейнера.

## Предварительные условия

К устройствам, использующим Application Guard в Microsoft Edge, применяются следующие требования:

- Windows 10 1809 (RS5) и более поздней версии.
- Только номера SKU клиентов Windows

  > [!NOTE]
  > Расширение Application Guard поддерживается только для номеров SKU клиентов Windows 10 Pro и Windows 10 Корпоративная.

- Одно из решений для управления, описанных в статье [Требования к программному обеспечению](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard#software-requirements)

## Установка Application Guard

В следующих статьях приведены сведения, необходимые для установки, настройки и тестирования Application Guard в Microsoft Edge.

- [Требования к системе](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard)
- [Установка Application Guard в Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/install-md-app-guard)
- [Настройка параметров групповой политики Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard)
- [Тестирование Application Guard](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/test-scenarios-md-app-guard)

## Вопросы и ответы

### Работает ли Application Guard в режиме IE?

Функциональность Application Guard поддерживается в режиме IE, но мы не ожидаем особой пользы от данной функции в этом режиме. Режим IE рекомендуется развертывать для списка надежных внутренних сайтов, а Application Guard — только для ненадежных сайтов. Убедитесь в том, что все сайты и IP-адреса в режиме IE также добавлены в политику сетевой изоляции, чтобы они рассматривались как надежные ресурсы в Application Guard.

### Нужно ли мне устанавливать расширение Application Guard для Chrome?

Нет, для функции Application Guard имеется встроенная поддержка в Microsoft Edge. На самом деле, расширение Application Guard для Chrome не поддерживается в Microsoft Edge.

### Есть ли другие вопросы и ответы, связанные с платформой?

Да. [Вопросы и ответы об Application Guard в Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/faq-md-app-guard) 

## См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Advanced Threat Protection в Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [Видео. Изоляция браузера Microsoft Edge с использованием Application Guard](https://www.youtube.com/watch?v=zQjaRqNXMqw&t=3s)
