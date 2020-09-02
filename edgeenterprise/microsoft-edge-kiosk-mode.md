---
title: Режим терминала в Microsoft Edge
ms.author: brianalt
author: brianalt
manager: seanlynd
ms.date: 01/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Режим терминала в Microsoft Edge
ms.openlocfilehash: 7a690820752b5361349bf394055a737bd8175215
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980980"
---
# Режим терминала в Microsoft Edge

В этой статье приведены общие сведения о параметрах режима терминала в Microsoft Edge (версии 77 или более поздней версии). Также в ней описываются требования для дальнейшего использования режима терминала в Microsoft Edge Legacy (версии 45 или более ранней версии).

Сведения о режиме терминала в Microsoft Edge Legacy (версии 45 или более ранней версии) см. в разделе [Развертывание режима терминала в Microsoft Edge](https://aka.ms/edgekioskmode).

## Microsoft Edge с ограниченным доступом

Microsoft Edge можно запустить с [ограниченным доступом для нескольких приложений](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) в Windows 10, что является эквивалентом типа режима терминала «Обычный просмотр веб-страниц» в Microsoft Edge Legacy. Чтобы настроить ограниченный доступ для нескольких приложений в Microsoft Edge, следуйте инструкциям по [настройке режима терминала с несколькими приложениями](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps). AUMID для Microsoft Edge из канала Stable— **MSEdge**.

При использовании Microsoft Edge с ограниченным доступом для нескольких приложений можно использовать [политики браузера Microsoft Edge](microsoft-edge-policies.md) для настройки браузера в соответствии с вашими уникальными требованиями.

На сегодняшний день Microsoft Edge не поддерживает те же типы режимов терминала Microsoft Edge Legacy для одного приложения с ограниченным доступом и тип режима терминала «Открытый просмотр веб-страниц» для нескольких приложений с ограниченным доступом. Если вам нужен браузер для устройства в режиме терминала с одним приложением с ограниченным доступом, рекомендуется использовать [режим терминала в Microsoft Edge Legacy](https://aka.ms/edgekioskmode) или [браузер терминала Майкрософт](https://www.microsoft.com/p/kiosk-browser/9ngb5s5xg2kp?activetab=pivot:overviewtab). 

## Параметр командной строки «--kiosk» для Microsoft Edge

Можно запустить Microsoft Edge в режиме терминала с помощью параметра командной строки «`--kiosk`». При этом браузер откроется в полноэкранном режиме с отключенным сочетанием клавиш для перехода в полноэкранный режим (F11). Для этого создайте ярлык со следующим целевым значением:<br>
*`"<local path>\msedge.exe" --kiosk http://bing.com`*

> [!NOTE]
> Параметр «`--kiosk`» не помешает пользователю использовать сочетания клавиш Windows и не предотвратит запуск других приложений. Чтобы получить контроль над этими возможностями, используйте [AppLocker для создания терминала на базе Windows 10](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-applocker) и [фильтр клавиатуры](https://docs.microsoft.com/windows-hardware/customize/enterprise/keyboardfilter).

Чтобы выйти из режима терминала и закрыть браузер, воспользуйтесь сочетанием клавиш ALT+F4.

## Поддержка режима терминала в Microsoft Edge Legacy

После установки новой версии Microsoft Edge из канала Stable версия Microsoft Edge Legacy скрывается, а попытки запустить Microsoft Edge Legacy приводят к запуску новой версии. Для получения информации о:

- требованиях обновлений Windows см. в разделе [Обновления Windows для обеспечения поддержки следующей версии Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md); 
- доступе к Microsoft Edge Legacy после установки Microsoft Edge см. раздел [Доступ к Microsoft Edge Legacy после установки новой версии Microsoft Edge](microsoft-edge-sysupdate-access-old-edge.md).
 
Чтобы продолжить использовать режим терминала в Microsoft Edge Legacy на устройствах в режиме терминала, выполните одно из следующих действий. 

- Если вы собираетесь установить версию Microsoft Edge из канала Stable, хотите разрешить ее установку или она уже установлена на вашем устройстве в режиме терминала, разверните политику [Разрешить параллельный запуск разных типов браузеров Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs).
- Чтобы запретить установку версии Microsoft Edge из канала Stable на ваших устройствах в режиме терминала, разверните политику [Разрешить установку по умолчанию](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allow-installation-default) для канала Stable или воспользуйтесь [набором средств блокировки для отключения автоматической доставки Microsoft Edge](microsoft-edge-blocker-toolkit.md). 

## Статьи по теме

- [Настройка терминалов и цифровых вывесок в выпусках Windows для настольных компьютеров](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Развертывание режима терминала в Microsoft Edge Legacy](https://aka.ms/edgekioskmode) 
- [Планирование развертывания Microsoft Edge](deploy-edge-plan-deployment.md)
- [Использование целевой страницы Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
