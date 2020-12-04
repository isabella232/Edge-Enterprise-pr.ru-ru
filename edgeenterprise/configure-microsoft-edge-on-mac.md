---
title: Настройка Microsoft Edge для macOS с помощью файла PLIST
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 11/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Настройка параметров политики Microsoft Edge в macOS с помощью файла PLIST
ms.openlocfilehash: abe110ab3589cc9276f28590273ece2d372be3b8
ms.sourcegitcommit: ed6a5afabf909df87bec48671c4c47bcdfaeb7bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/02/2020
ms.locfileid: "11194694"
---
# Настройка параметров политики Microsoft Edge для macOS с помощью файла PLIST

В этой статье описано, как настроить Microsoft Edge в macOS с помощью файла со списком свойств (.plist). Вы узнаете, как создать этот файл и развернуть его в Microsoft Intune.

Дополнительные сведения см. в разделе [Общие сведения о файлах со списком свойств](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (веб-сайт компании Apple) и [Пользовательские параметры полезных данных](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## Настройка политик Microsoft Edge в macOS

Первый этап — это создание файла со списком свойств. Вы можете создать файл PLIST в любом текстовом редакторе или использовать [Терминал для создания профиля конфигурации](#create-a-configuration-profile-using-terminal). Однако проще создавать и редактировать файл PLIST с помощью средства форматирования XML-кода. *Xcode* — это бесплатная интегрированная среда разработки, которую можно получить в одном из следующих мест.

- [Веб-сайт для разработчиков Apple](https://developer.apple.com/xcode/)
- [Магазин App Store для Mac](https://apps.apple.com/app/xcode/id497799835?mt=12)

Список поддерживаемых политик и предпочтительные имена для их разделов см. в [Справочнике по политикам браузера Microsoft Edge](microsoft-edge-policies.md). В файле шаблонов политик, который можно скачать на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise), есть образец файла пример PLIST (*itadminexample.plist*) в папке **Примеры**. Образец файла содержит все поддерживаемые типы данных, которые можно настроить для определения параметров политики. 

Следующий шаг после создания содержимого файла PLIST — присвоить ему имя, используя предпочтительный домен Microsoft Edge, то есть *com.microsoft.Edge*. Имя чувствительно к регистру и не должно содержать настраиваемый канал, так как оно применяется ко всем каналам Microsoft Edge. Именем файла PLIST должно быть **_com.microsoft.Edge.plist_**.

> [!IMPORTANT]
> Начиная со сборки 78.0.249.2 все каналы Microsoft Edge в macOS выполняют считывание из основного домена **com.microsoft.Edge**. Все предыдущие выпуски выполняют считывание из домена, относящегося к каналу, например из домена **com.microsoft.Edge.Dev** для канала Dev.

Последним шагом является развертывание файла PLIST на устройствах Mac ваших пользователей с помощью предпочитаемого поставщика MDM, например Microsoft Intune. Инструкции см. в разделе [Развертывание файла PLIST](#deploy-your-plist).

### Создание профиля конфигурации с помощью терминала

1. В терминале используйте следующую команду, чтобы создать файл PLIST для Microsoft Edge на компьютере с использованием предпочтительных параметров.

   ```cmd
   /usr/bin/defaults write ~/Desktop/com.microsoft.Edge.plist RestoreOnStartup -int 1
   ```

2. Преобразуйте файл PLIST из двоичного формата в текстовый.

   ```cmd
   /usr/bin/plutil -convert xml1 ~/Desktop/com.microsoft.Edge.plist
   ```

После преобразования файла проверьте правильность данных политики и наличие в них необходимых параметров для профиля конфигурации.

> [!NOTE]
> Файл plist или xml должен содержать только пары "ключ-значение". Перед отправкой файла в Intune удалите из него все значения \<plist> и \<dict>, а также заголовки xml. Файл должен содержать только пары "ключ-значение".

## Развертывание файла PLIST

Для Microsoft Intune создайте новый профиль конфигурации устройства, предназначенный для платформы macOS, и выберите тип профиля *Файл основных параметров*. Выберите **com.microsoft.Edge** в качестве предпочтительного доменного имени и добавьте файл PLIST. Дополнительные сведения см. в разделе [Добавление файла со списком свойств на устройства macOS с помощью Microsoft Intune](https://docs.microsoft.com/intune/configuration/preference-file-settings-macos).

Для Jamf добавьте файл PLIST как полезные данные *Настраиваемые параметры*.

## См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Настройка для macOS с помощью Jamf](configure-microsoft-edge-on-mac-jamf.md)
- [Настройка для Windows](configure-microsoft-edge.md)
- [Настройка для Windows с помощью Intune](configure-edge-with-intune.md)
