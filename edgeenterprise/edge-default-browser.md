---
title: Установка Microsoft Edge браузером по умолчанию в Windows и macOS
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 1/15/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Узнайте, как задать Microsoft Edge в качестве браузера по умолчанию
ms.openlocfilehash: c8cc45e0fe42dcbbd828dd81ae568f141cda2985
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980862"
---
# Установка Microsoft Edge в качестве браузера по умолчанию

В этой статье описывается, как можно задать Microsoft Edge браузером по умолчанию в Windows и macOS.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней в среде Windows 8 и Windows 10. Для Windows 7 и macOS см. раздел, посвященный политике [Установка Microsoft Edge браузером по умолчанию](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled).

## Введение

Вы можете использовать групповую политику **Задать файл конфигурации сопоставлений по умолчанию** или параметр системы управления мобильными устройствами [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration), чтобы сделать Microsoft Edge браузером по умолчанию в своей организации.

Чтобы задать Microsoft Edge Stable в качестве браузера по умолчанию для открытия HTML-файлов, ссылок http/https и файлов PDF, используйте следующий пример файла сопоставления приложений:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations> 
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> Чтобы настроить Microsoft Edge Beta в качестве браузера по умолчанию, задайте параметру **ApplicationName** значение "Microsoft Edge Beta", а параметру **ProgId** значение "MSEdgeBHTML". Чтобы настроить Microsoft Edge Dev в качестве браузера по умолчанию, задайте параметру **ApplicationName** значение "Microsoft Edge Dev", а параметру **ProgId** значение "MSEdgeDHTML".


> [!NOTE]
> Сопоставления файлов по умолчанию не применяются, если на целевом устройстве не установлен браузер Microsoft Edge. В этом случае пользователям будет предложено выбрать приложение по умолчанию при открытии ссылки или файла HTM/HTML.

## Установка Microsoft Edge в качестве браузера по умолчанию на устройствах, присоединенных к домену

Вы можете задать Microsoft Edge в качестве браузера по умолчанию на устройствах, присоединенных к домену, настроив групповую политику **Задать файл конфигурации сопоставлений по умолчанию**. При включении этой групповой политики также необходимо создать и сохранить файл конфигурации сопоставлений по умолчанию. Этот файл хранится локально или в сетевой папке. Подробнее о создании этого файла см. в разделе [Экспорт и импорт файлов сопоставлений приложений по умолчанию](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).

### Чтобы настроить групповую политику для файла конфигурации сопоставлений по умолчанию и файла конфигурации сопоставлений протокола, выполните следующие действия.

1. В редакторе групповых политик перейдите к разделу **Computer Configuration\Administrative Templates\Windows Components\File Explorer**.
2. Выберите **Задать файл конфигурации сопоставлений по умолчанию**.
3. Щелкните **параметр политики**, а затем выберите **Включить**.
4. В области **Параметры** введите расположение файла конфигурации сопоставлений по умолчанию.
5. Нажмите **ОК**, чтобы сохранить параметры политики.

В примере на следующем снимке экрана показан файл сопоставлений с именем *appassoc.xml* в сетевой папке, доступной с целевого устройства.

   ![Включение сопоставления файлов в групповой политике](./media/edge-learnmore-make-edge-default-browser/edge-learnmore-app-associations.png)

   > [!NOTE]
   > Если этот параметр включен и устройство пользователя подключено к домену, файл конфигурации сопоставлений обрабатывается при следующем входе пользователя в систему.

## Установка Microsoft Edge в качестве браузера по умолчанию на устройствах, присоединенных к Azure Active Directory

Чтобы задать Microsoft Edge в качестве браузера по умолчанию на устройствах, подключенных к Azure Active Directory, выполните действия в разделе, посвященном параметру системы управления мобильными устройствами [DefaultAssociationsConfiguration](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration), используя следующий пример файла сопоставления приложений.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> Чтобы настроить Microsoft Edge Beta в качестве браузера по умолчанию, задайте параметру **ApplicationName** значение "Microsoft Edge Beta", а параметру **ProgId** значение "MSEdgeBHTML". Чтобы настроить Microsoft Edge Dev в качестве браузера по умолчанию, задайте параметру **ApplicationName** значение "Microsoft Edge Dev", а параметру **ProgId** значение "MSEdgeDHTML".

## Установка Microsoft Edge браузером по умолчанию в macOS

При попытке программно назначить браузер по умолчанию в macOS появляется запрос для пользователя. Этот запрос является функцией безопасности macOS, автоматический запуск которой можно отключить только с помощью AppleScript.

Из-за этого ограничения существует два основных метода установки Microsoft Edge в качестве браузера по умолчанию в macOS. Первый вариант: установить на устройство образ macOS, в котором Microsoft Edge уже задан как браузер по умолчанию. Второй вариант: использование политики [Установить Microsoft Edge браузером по умолчанию](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled), которая предлагает пользователю назначить Microsoft Edge браузером по умолчанию.

При использовании любого из этих методов пользователь может изменить браузер по умолчанию. Это связано с тем, что по соображениям безопасности настройка браузера по умолчанию не может быть заблокирована программным способом. По этой причине рекомендуется развертывать политику **Установить Microsoft Edge браузером по умолчанию**, даже если вы создаете образ с Microsoft Edge в качестве браузера по умолчанию. Если эта политика настроена и пользователь изменяет браузер по умолчанию с Microsoft Edge, при следующем открытии Microsoft Edge пользователю будет предложено назначить его браузером по умолчанию.

## Статьи по теме

- [Планирование развертывания Microsoft Edge](https://docs.microsoft.com/DeployEdge/deploy-edge-plan-deployment)
- [Использование целевой страницы Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Установка Microsoft Edge в качестве браузера по умолчанию (Windows 7 и macOS)](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultbrowsersettingenabled)
- [Windows 10: руководство по настройке сопоставления файлов для ИТ-специалистов](https://docs.microsoft.com/archive/blogs/windowsinternals/windows-10-how-to-configure-file-associations-for-it-pros)
- [Экспорт и импорт сопоставлений приложений по умолчанию](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)
  - [Обзор платформы DISM](https://docs.microsoft.com/windows-hardware/manufacture/desktop/what-is-dism)
  - [Система обслуживания образов развертывания и управления ими (DISM)](https://docs.microsoft.com/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows)
