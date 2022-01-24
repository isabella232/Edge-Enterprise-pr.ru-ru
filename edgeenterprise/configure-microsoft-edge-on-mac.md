---
title: Настройка Microsoft Edge macOS с помощью списка свойств.
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 12/14/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Узнайте, как настроить Microsoft Edge параметров политики на macOS с помощью списка свойств, которые можно развернуть для Microsoft Intune.
ms.openlocfilehash: 4cb3d635c8fc108a3b81ec17175ce0e3d8fa287a
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2022
ms.locfileid: "12297707"
---
# <a name="configure-microsoft-edge-policy-settings-for-macos-using-a-property-list"></a>Настройка параметров Microsoft Edge для macOS с помощью списка свойств

В этой статье описывается настройка Microsoft Edge macOS с помощью файла списка свойств (\.plist). Вы узнаете, как создать этот файл и развернуть его в Microsoft Intune.

Дополнительные сведения см. в разделе [Общие сведения о файлах со списком свойств](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (веб-сайт компании Apple) и [Пользовательские параметры полезных данных](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## <a name="configure-microsoft-edge-policies-on-macos"></a>Настройка политик Microsoft Edge в macOS

Первый этап — это создание файла со списком свойств. Файл plist можно создать с помощью любого редактора текста. Другим вариантом является использование [терминала для создания профиля конфигурации.](#create-a-configuration-profile-using-terminal) Однако проще создавать и редактировать файл plist с помощью средства, который форматирует XML-код для вас. *Xcode* — это бесплатная интегрированная среда разработки, доступная в следующих расположениях:

- [Веб-сайт для разработчиков Apple](https://developer.apple.com/xcode/)
- [Магазин App Store для Mac](https://apps.apple.com/app/xcode/id497799835?mt=12)

Список поддерживаемых политик и предпочтительные имена для их разделов см. в [Справочнике по политикам браузера Microsoft Edge](./microsoft-edge-policies.md). В файле шаблонов политики, который можно скачать с Microsoft Edge Enterprise [страницы,](https://aka.ms/EdgeEnterprise)в папке примеров есть пример plist *(itadminexample.plist).* **** Этот файл содержит все поддерживаемые типы данных, которые можно настроить для определения параметров политики.

После создания содержимого списка назовите список с помощью домена Microsoft Edge, который является *"com.microsoft.Edge".* Это имя является чувствительным к делу и не должно включать канал, на который вы нацелены, так как оно применимо ко всем Microsoft Edge каналам. Именем файла PLIST должно быть **_com.microsoft.Edge.plist_**.

> [!IMPORTANT]
> Начиная со сборки 78.0.249.2 все каналы Microsoft Edge в macOS выполняют считывание из основного домена **com.microsoft.Edge**. Все предыдущие выпуски выполняют считывание из домена, относящегося к каналу, например из домена **com.microsoft.Edge.Dev** для канала Dev.

Последним шагом является развертывание файла PLIST на устройствах Mac ваших пользователей с помощью предпочитаемого поставщика MDM, например Microsoft Intune. Инструкции см. в разделе [Развертывание файла PLIST](#deploy-your-plist).

### <a name="create-a-configuration-profile-using-terminal"></a>Создание профиля конфигурации с помощью терминала

1. В терминале используйте следующую команду, чтобы создать файл PLIST для Microsoft Edge на компьютере с использованием предпочтительных параметров.

   ```cmd
   /usr/bin/defaults write ~/Desktop/com.microsoft.Edge.plist RestoreOnStartup -int 1
   ```

2. Преобразуйте файл PLIST из двоичного формата в текстовый.

   ```cmd
   /usr/bin/plutil -convert xml1 ~/Desktop/com.microsoft.Edge.plist
   ```

После преобразования файла убедитесь, что данные политики верны и содержат параметры, необходимо создать профиль конфигурации.

> [!NOTE]
> Файл plist или xml должен содержать только пары "ключ-значение". Перед отправкой файла в Intune удалите из него все значения \<plist> и \<dict>, а также заголовки xml. Файл должен содержать только пары "ключ-значение".

## <a name="deploy-your-plist"></a>Развертывание файла PLIST

С Microsoft Intune создайте новый профиль конфигурации устройства, нацеленный на платформу macOS, и выберите тип профиля файла *Preference.* Выберите **com.microsoft.Edge** в качестве предпочтительного доменного имени и добавьте файл PLIST. Дополнительные сведения см. в [материалах Add a property list file to macOS devices using Microsoft Intune.](/intune/configuration/preference-file-settings-macos)

Для Jamf загрузите файл \.plist в качестве *настраиваемой* Параметры полезной нагрузки.

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Настройка для macOS с помощью Jamf](configure-microsoft-edge-on-mac-jamf.md)
- [Настройка для Windows](configure-microsoft-edge.md)
- [Настройка для Windows с помощью Intune](configure-edge-with-intune.md)