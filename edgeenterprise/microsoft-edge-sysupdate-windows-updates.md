---
title: Обновления Windows для поддержки Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 11/17/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Обновления Windows для поддержки Microsoft Edge.
ms.openlocfilehash: 85f60b3ee09154c702debcfb222567996be9462f
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2022
ms.locfileid: "12298167"
---
# <a name="windows-updates-to-support-the-next-version-of-microsoft-edge"></a>Обновления Windows для обеспечения поддержки следующей версии Microsoft Edge

В этой статье описывается, как будет выполняться обновление Windows для обеспечения поддержки следующей версии Microsoft Edge

> [!IMPORTANT]
> Обратитесь к [записи блога](https://aka.ms/EdgeLegacyEOS) команды разработки продукта Microsoft Edge по поводу завершения обслуживания устаревшей версии Microsoft Edge.

> [!NOTE]
> Эта статья относится к Microsoft Edge из стабильного канала.

## <a name="microsoft-edge-and-the-windows-release-cycle"></a>Цикл выпуска Microsoft Edge и Windows

Новая версия Microsoft Edge будет поддерживать более гибкие возможности обновления, которые будут предоставляться для нее чаще. Так как выпуски браузера не привязаны к основным выпускам Windows, изменения будут вноситься в операционную систему, чтобы гарантировать оптимальную совместимость следующей версии Microsoft Edge с Windows. Результатом будет выпуск обновления компонентов в 4-недельном цикле (приблизительно). Обновления для системы безопасности и совместимости будут предоставляться по мере необходимости.

## <a name="updates-and-the-user-experience"></a>Обновления и интерфейс

Обновления не будут затрагивать интерфейс до тех пор, пока следующая версия Microsoft Edge не будет установлена в рамках канала Stable. Установка Microsoft Edge в рамках каналов Beta, Dev или Canary не приведет к внесению каких-либо изменений в Windows. Эти выпуски браузера будут установлены вместе с имеющимися версиями браузера.

После применения всех обновлений и установки следующей версии Microsoft Edge в рамках канала Stable на системном уровне, в системе вступят в силу следующие изменения.

- Все закрепленные в меню "Пуск" элементы, плитки и ярлыки для текущей версии Microsoft Edge будут перенесены в следующую версию Microsoft Edge.
- Все закрепленные на панели задач элементы и ярлыки для текущей версии Microsoft Edge будут перенесены в следующую версию Microsoft Edge.
- Следующая версия Microsoft Edge будет закреплена на панели задач. Если текущая версия Microsoft Edge уже закреплена, она будет заменена.
- После установки новой версии Microsoft Edge на рабочий стол будет добавлен ярлык. Если у текущей версии Microsoft Edge уже есть ярлык, он будет заменен.
- Большинство протоколов, которые Microsoft Edge обрабатывает по умолчанию, будут перенесены в следующую версию Microsoft Edge.
- Текущая версия Microsoft Edge будет скрыта на всех интерфейсах в ОС, включая параметры, все приложения и все диалоговые окна поддержки файлов и протоколов.
- При попытке запуска текущей версии Microsoft Edge будут открываться следующая версия Microsoft Edge.

  > [!NOTE]
  > Процессы установки на уровне пользователя не будут приводить к таким результатам.

Наряду с предыдущими изменениями будут происходить другие изменения независимо от того, установлен ли браузер Microsoft Edge в рамках канала Stable.

- Microsoft Edge отменит регистрацию электронных книг и протоколов XML, которые не поддерживаются в новой версии Microsoft Edge. Для пользователей, которые попытаются открыть эти протоколы, будет отображаться диалоговое окно с запросом на выбор приложения по умолчанию. Посетите Microsoft Store, чтобы просмотреть наши рекомендации для читателей электронных книг.
  
## <a name="older-versions-of-windows"></a>Более старые версии Windows

Чтобы развернуть Microsoft Edge на устройстве с более ранней версией Windows, чем Windows 10 RS4, используйте [диспетчер конфигураций](https://docs.microsoft.com/mem/configmgr/apps/deploy-use/deploy-edge?bc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Ftoc.json), [Microsoft Intune](https://docs.microsoft.com/mem/intune/apps/apps-windows-edge?bc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Ftoc.json) или выполните обновление до поддерживаемой версии Windows 10. В следующей статье перечислены поддерживаемые в настоящее время версии Windows 10 и Windows 11.

- [Поддерживаемые версии клиента Windows](/windows/release-health/supported-versions-windows-client)

> [!NOTE]
> Для Windows 10 RS4-20H1 разверните Windows LCU с мая 2021 года или новее, чтобы получить Microsoft Edge. Дополнительные сведения см. в статье [Журнал обновлений Windows 10](https://support.microsoft.com/topic/windows-10-update-history-1b6aac92-bf01-42b5-b158-f80c6d93eb11)

> [!IMPORTANT]
> Если вам нужны обновления, не перечисленные здесь, запустите Центр обновления Windows или обратитесь к администратору.

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Документация по Microsoft Edge](./index.yml)