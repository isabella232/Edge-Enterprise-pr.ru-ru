---
title: Вопросы и ответы о браузере Edge в организации
ms.author: jwhit
author: jwhit-MSFT
manager: laurawi
ms.date: 08/03/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Вопросы и ответы о развертывании браузера Microsoft Edge в организации
ms.openlocfilehash: 0f6891f4f7187b23f6e3d4e7880fdafa49def351
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980895"
---
# Вопросы и ответы о браузере Microsoft Edge в организации

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## Как узнать используемую версию Microsoft Edge?

В правом верхнем углу щелкните Microsoft Edge, затем значок многоточия (**…**), а затем нажмите **Параметры**. Выберите **Сведения о Microsoft Edge**, чтобы просмотреть свою версию Microsoft Edge.

## Будут ли выходить обновления для Internet Explorer 11?

Мы стремимся поддерживать Internet Explorer, чтобы он оставался надежным и безопасным браузером. Internet Explorer все еще является компонентом Windows и на него распространяется жизненный цикл поддержки ОС Windows, в которой установлен браузер. Дополнительные сведения см. в разделе [Вопросы и ответы по жизненному циклу— Internet Explorer](https://support.microsoft.com/help/17454/). Несмотря на то что корпорация Майкрософт продолжает поддерживать и обновлять Internet Explorer, новейшие функции и обновления платформы будут доступны только в Microsoft Edge.

## Можно ли запускать текущую версию Microsoft Edge (Microsoft Edge Legacy) вместе с новой версией?

Да. После 15 января 2020г. новая версия Microsoft Edge (на основе Chromium) будет распространятся для устройств с Windows 10 версии 1803 Домашняя и Pro. Присоединенные к домену устройства исключены из этого обновления. Дополнительные сведения см. в разделе [Обзор обновлений Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-blocker-toolkit#overview). Можно параллельно использовать Microsoft Edge Legacy в период оценки новой версии Microsoft Edge. Дополнительные сведения см. в разделе [Доступ к старой версии версии Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge). Кроме того, в каждом из новых каналов Microsoft Edge поддерживается параллельное использование разных версий браузера. Дополнительные сведения см. в разделе [Обзор каналов Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-channels).

## Поддерживает ли Microsoft Edge (на основе Chromium) элементы ActiveX или вспомогательные объекты браузера, такие как Silverlight или Java?

Нет. Microsoft Edge не поддерживает элементы ActiveX и вспомогательные объекты браузера, такие как Silverlight или Java. Но если вы применяете веб-приложения, использующие элементы ActiveX, вспомогательные объекты браузера или устаревшие режимы работы с документами в Internet Explorer 11, то можно настроить их запуск в режиме IE в новом Microsoft Edge. Дополнительные сведения см. в статье [Настройка режима IE в Microsoft Edge](https://docs.microsoft.com/DeployEdge/edge-ie-mode).

## Будет ли избранное перенесено из текущей версии Microsoft Edge в новую или потребуется добавлять его повторно?

В данный Microsoft Edge поддерживает импорт из существующих установок Microsoft Edge, Chrome, Internet Explorer и Firefox (на Win10). Импорт поддерживают следующие параметры: закладки, журнал, пароли и данные автозаполнения (платежи, адреса и универсальные формы). Вы можете импортировать данные во время первого запуска или из параметров браузера.  

## В чем разница между каналами и сборками Stable, Beta, Dev и Canary?

Канал Stable следующей версии Microsoft Edge — это наиболее стабильный канал с корпоративными возможностями, готовыми для [пилотного развертывания и оценки](https://aka.ms/EdgeEnterprise) в масштабах всей организации. Канал Beta позволяет проверить следующий выпуск Stable с участием показательной выборки пользователей. Каналы Stable и Beta будут обновляться приблизительно каждые шесть недель. Каналы Dev и Canary продолжат обновляться еженедельно и ежедневно соответственно. Автономные установщики (файлы MSI и PKG) доступны только для каналов Stable, Beta и Dev. Дополнительные сведения см. в разделе [Обзор каналов Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-channels).

## Какие расширения поддерживает новая версия Microsoft Edge?

Microsoft Edge поддерживает расширения с [ портала Microsoft Edge Insider Addons](https://go.microsoft.com/fwlink/?linkid=2081222) и из [интернет-магазина Chrome](https://go.microsoft.com/fwlink/?linkid=2072338).

## Есть ли поддержка средств управления мобильными устройствами (MDM) и Microsoft Intune?

Да. Теперь поддерживается настройка Microsoft Edge в Windows 10 с помощью Microsoft Intune и средств управления мобильными устройствами (MDM). Дополнительные сведения см. в разделе [Настройка Microsoft Edge с помощью Microsoft Intune](configure-edge-with-intune.md) и [Настройка Microsoft Edge с помощью средств управления мобильными устройствами](configure-edge-with-mdm.md).

## Поддерживают ли службы WSUS начальное развертывание нового браузера Microsoft Edge?

Нет. Службы WSUS поддерживает обновление существующих экземпляров Microsoft Edge, установленных с помощью MSI, но их невозможно использовать для начального развертывания. Если целью является полное управление обновлениями через службы WSUS, начальное развертывание можно выполнить с помощью средства управления, такого как [ConfigMgr](https://docs.microsoft.com/configmgr/apps/deploy-use/deploy-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json).

## См. также

- [Целевая страница с документацией по Microsoft Edge Enterprise](https://docs.microsoft.com/DeployEdge/)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
