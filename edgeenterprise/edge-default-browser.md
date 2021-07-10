---
title: Установка Microsoft Edge браузером по умолчанию в Windows и macOS
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Узнайте, как задать Microsoft Edge в качестве браузера по умолчанию
ms.openlocfilehash: 191d7835a0c4aacfc2fde409c57622ff5a351926
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641545"
---
# <a name="set-microsoft-edge-as-the-default-browser"></a>Установка Microsoft Edge в качестве браузера по умолчанию

В этой статье описывается, как можно задать Microsoft Edge браузером по умолчанию в Windows и macOS.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней в среде Windows 8 и Windows 10. Для Windows 7 и macOS см. раздел, посвященный политике [Установка Microsoft Edge браузером по умолчанию](./microsoft-edge-policies.md#defaultbrowsersettingenabled).

## <a name="introduction"></a>Введение

Вы можете использовать групповую политику **Задать файл конфигурации сопоставлений по умолчанию** или параметр системы управления мобильными устройствами [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration), чтобы сделать Microsoft Edge браузером по умолчанию в своей организации.

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

## <a name="set-microsoft-edge-as-the-default-browser-on-domain-joined-devices"></a>Установка Microsoft Edge в качестве браузера по умолчанию на устройствах, присоединенных к домену

Вы можете задать Microsoft Edge в качестве браузера по умолчанию на устройствах, присоединенных к домену, настроив групповую политику **Задать файл конфигурации сопоставлений по умолчанию**. При включении этой групповой политики также необходимо создать и сохранить файл конфигурации сопоставлений по умолчанию. Этот файл хранится локально или в сетевой папке. Подробнее о создании этого файла см. в разделе [Экспорт и импорт файлов сопоставлений приложений по умолчанию](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).

### <a name="to-configure-the-group-policy-for-a-default-file-type-and-protocol-associations-configuration-file"></a>Чтобы настроить групповую политику для файла конфигурации сопоставлений по умолчанию и файла конфигурации сопоставлений протокола, выполните следующие действия.

1. В редакторе групповых политик перейдите к разделу **Computer Configuration\Administrative Templates\Windows Components\File Explorer**.
2. Выберите **Задать файл конфигурации сопоставлений по умолчанию**.
3. Щелкните **параметр политики**, а затем выберите **Включить**.
4. В области **Параметры** введите расположение файла конфигурации сопоставлений по умолчанию.
5. Нажмите **ОК**, чтобы сохранить параметры политики.

В примере на следующем снимке экрана показан файл сопоставлений с именем *appassoc.xml* в сетевой папке, доступной с целевого устройства.

   ![Включение сопоставления файлов в групповой политике](./media/edge-learnmore-make-edge-default-browser/edge-learnmore-app-associations.png)

   > [!NOTE]
   > Если этот параметр включен и устройство пользователя подключено к домену, файл конфигурации сопоставлений обрабатывается при следующем входе пользователя в систему.

## <a name="set-microsoft-edge-as-the-default-browser-on-azure-active-directory-joined-devices"></a>Установка Microsoft Edge в качестве браузера по умолчанию на устройствах, присоединенных к Azure Active Directory

Чтобы задать Microsoft Edge в качестве браузера по умолчанию на устройствах, подключенных к Azure Active Directory, выполните действия в разделе, посвященном параметру системы управления мобильными устройствами [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration), используя следующий пример файла сопоставления приложений.

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

## <a name="set-microsoft-edge-as-the-default-browser-on-macos"></a>Установка Microsoft Edge браузером по умолчанию в macOS

При попытке программно назначить браузер по умолчанию в macOS появляется запрос для пользователя. Этот запрос является функцией безопасности macOS, автоматический запуск которой можно отключить только с помощью AppleScript.

Из-за этого ограничения существует два основных метода установки Microsoft Edge в качестве браузера по умолчанию в macOS. Первый вариант: установить на устройство образ macOS, в котором Microsoft Edge уже задан как браузер по умолчанию. Второй вариант: использование политики [Установить Microsoft Edge браузером по умолчанию](./microsoft-edge-policies.md#defaultbrowsersettingenabled), которая предлагает пользователю назначить Microsoft Edge браузером по умолчанию.

При использовании любого из этих методов пользователь может изменить браузер по умолчанию. Это связано с тем, что по соображениям безопасности настройка браузера по умолчанию не может быть заблокирована программным способом. По этой причине рекомендуется развертывать политику **Установить Microsoft Edge браузером по умолчанию**, даже если вы создаете образ с Microsoft Edge в качестве браузера по умолчанию. Если эта политика настроена и пользователь изменяет браузер по умолчанию с Microsoft Edge, при следующем открытии Microsoft Edge пользователю будет предложено назначить его браузером по умолчанию.

## <a name="see-also"></a>Статьи по теме

- [Планирование развертывания Microsoft Edge](./deploy-edge-plan-deployment.md)
- [Использование целевой страницы Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Установка Microsoft Edge в качестве браузера по умолчанию (Windows 7 и macOS)](./microsoft-edge-policies.md#defaultbrowsersettingenabled)
- [Windows 10: руководство по настройке сопоставления файлов для ИТ-специалистов](/archive/blogs/windowsinternals/windows-10-how-to-configure-file-associations-for-it-pros)
- [Экспорт и импорт сопоставлений приложений по умолчанию](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)
  - [Обзор платформы DISM](/windows-hardware/manufacture/desktop/what-is-dism)
  - [Система обслуживания образов развертывания и управления ими (DISM)](/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows)