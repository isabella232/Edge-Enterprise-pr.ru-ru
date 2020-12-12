---
title: Синхронизация Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 12/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Синхронизация Microsoft Edge Enterprise
ms.openlocfilehash: 791188b5d28c867d6409a4d5373ea6c1ec7e49c7
ms.sourcegitcommit: 482b2e440a62cbf974dc45ac817f9d9d187ba1b9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "11205468"
---
# Синхронизация Microsoft Edge Enterprise

В этой статье объясняется, как использовать Microsoft Edge для синхронизации избранного, паролей и других данных браузера на всех устройствах, на которых выполнен вход пользователя в систему.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней, если не указано иное.

## Обзор

Функция синхронизации Microsoft Edge позволяет пользователям получать доступ к данным браузера на всех своих устройствах, на которых они выполняют вход в систему. К данным, поддерживаемым функцией синхронизации, относятся следующие:

- Избранное
- Пароли
- Адреса и прочее (заполнения форм)
- Коллекции
- Параметры
- Расширение
- Открытые вкладки (доступно в Microsoft Edge версии 88)
- Журнал (доступно в Microsoft Edge версии 88)

Функция синхронизации включается путем предоставления пользователем согласия с этим действием. Пользователи могут включать или отключать синхронизацию для всех перечисленных выше типов данных.

> [!NOTE]
> Для обеспечения поддержки функции синхронизации передаются дополнительные данные о подключении устройства и данные конфигурации (например, имя устройства, изготовитель и модель).

## Предварительные условия

Функция синхронизации Microsoft Edge для учетных записей Azure Active Directory (Azure AD) доступна в рамках любой из этих подписок:

- Azure AD Premium (P1 или P2)
- M365 бизнес премиум
- Office 365 E1 и более поздние версии
- Azure Information Protection (AIP) (P1 или P2)
- Все подписки EDU (приложения Майкрософт для учащихся или преподавателей, Exchange Online для учащихся или преподавателей, O365 A1 или выше, M365 A1 или выше, Azure Information Protection P1 или P2 для учащихся или преподавателей)

## Настройка синхронизации Microsoft Edge

Параметры конфигурации для функции синхронизации Microsoft Edge доступны в службе Azure Information Protection (AIP). Если служба AIP включена для клиента, все пользователи могут синхронизировать данные в Microsoft Edge независимо от типа лицензии. Инструкции по включению службы AIP см. [здесь](https://docs.microsoft.com/azure/information-protection/activate-office365).

Чтобы ограничить синхронизацию для определенной группы пользователей, вы можете включить для них [политику управления регистрацией в AIP](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) . Если после регистрации всех необходимых пользователей синхронизация все еще недоступна, убедитесь в том, что служба IPCv3Service включена, используя командлет PowerShell [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true).

> [!CAUTION]
> При включении службы Azure Information Protection другие приложения, такие как Microsoft Word и Microsoft Outlook, также смогут защищать контент с помощью AIP. Кроме того, любая политика управления регистрацией, используемая для ограничения синхронизации Microsoft Edge, также ограничит защиту контента с помощью AIP в других приложениях.

## Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming

Новая версия Microsoft Edge— это межплатформенное приложение для расширенной синхронизации пользовательских данных на всех используемых устройствах. Приложение больше не входит состав службы Enterprise State Roaming в Azure AD. Однако в новой версии Microsoft Edge будут реализованы средства защиты данных, аналогичные ESR, такие как возможность использования собственного ключа. Дополнительные сведения см. в разделе [Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Синхронизация групповых политик

На функцию синхронизации Microsoft Edge влияют следующие групповые политики:

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): полное отключение синхронизации.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): отключает сохранение журнала браузера и синхронизацию. Эта политика также отключает синхронизацию открытых вкладок.
- [AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): если эта политика отключена, синхронизация журнала также будет отключена.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): настройка списка типов, исключенных из синхронизации.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): разрешает профилям Active Directory (AD) использовать локальное хранилище. Дополнительные сведения см. в статье [Локальная синхронизация для пользователей Active Directory (AD)](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).
- [ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): включает синхронизацию по умолчанию и не требует согласия пользователя для синхронизации.  

## Вопросы и ответы

### БЕЗОПАСНОСТЬ И СООТВЕТСТВИЕ СЕРВЕРА/ДАННЫХ

#### Шифруются ли синхронизированные данные?

Данные шифруются в процессе транспортировки с использованием протокола TLS 1.2 или более поздней версии. Все типы данных дополнительно шифруются в службе Майкрософт с помощью AES128. Все типы данных, кроме используемых для синхронизации открытой вкладки и журнала, дополнительно шифруются перед покиданием устройства пользователя с использованием ключей, управляемых с помощью [Azure Information Protection](https://docs.microsoft.com/azure/information-protection/).

#### Почему данные открытой вкладки и журнала не используют дополнительное шифрование на стороне клиента?  

Чтобы сократить использование ресурсов на устройствах конечных пользователей, данные журнала создаются на стороне сервера на основе перемещаемых данных открытой вкладки. Этот процесс невозможен при шифровании этих данных на стороне клиента. Чтобы отключить синхронизацию открытой вкладки и журнала, примените политику [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) или [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled).

#### Могут ли администраторы клиента использовать свой ключ?

Да, с помощью  [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).

#### Где хранятся данные синхронизации Microsoft Edge?

Синхронизированные данные учетных записей Azure AD хранятся на защищенных серверах в соответствии с идентификатором клиента. Например, данные клиента, зарегистрированного в США, хранятся на серверах, расположенных в этом географическом регионе, и к ним применяется то же самое решение для хранения, что и к приложениям Office.

#### Выходят ли данные за пределы облака Майкрософт помимо синхронизации с Microsoft Edge?

Нет.

#### Каковы условия использования синхронизации в корпоративной среде?

Условия использования функции синхронизации Microsoft Edge регулируются лицензией на программное обеспечение корпорации Майкрософт, с которой можно ознакомиться в Microsoft Edge по адресу  *edge://terms*. Ваша подписка на Azure AD и условия обслуживания в конечном итоге регулируются [условиями использования веб-служб](https://www.microsoft.com/licensing/product-licensing/products) Майкрософт.

#### Поддерживает ли Microsoft Edge стандарты соответствия требованиям облака сообщества для государственных организаций (GCC High)?

Еще нет. Для клиентов в облаке GCC High синхронизация Microsoft Edge отключена.

### ПРИМЕНЕНИЕ СИНХРОНИЗАЦИИ

#### Почему синхронизация Microsoft Edge не поддерживается во всех подписках M365?

Синхронизация в корпоративной среде зависит от службы Azure Information Protection, которая доступна не во всех подписках M365.

#### Основана ли функция синхронизации Microsoft Edge на Enterprise State Roaming?

Нет. ESR может использоваться для включения синхронизации, но функция синхронизации Microsoft Edge не входит в состав ESR. Дополнительные сведения см. в разделах [Функция синхронизации Microsoft Edge](microsoft-edge-enterprise-sync.md) и [Microsoft Edge и Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

#### Будет ли Microsoft Edge поддерживать синхронизацию между Microsoft Edge и IE?

Поддержка такой синхронизации не планируется. Если для поддержки устаревших приложений вам нужен IE, подумайте об использовании [нового режима IE](https://docs.microsoft.com/deployedge/edge-ie-mode).

#### Будет ли Microsoft Edge синхронизироваться с устаревшей версией Microsoft Edge?

Нет, не будет. Мы считаем, что объединение этих двух экосистем может привести к нарушению надежности синхронизации в Microsoft Edge. Мы обеспечим перенос имеющихся данных в Microsoft Edge. Кроме того, пользователи смогут импортировать данные из браузера, которым они пользуются. Это также означает, что синхронизация между новым браузером Microsoft Edge и браузером Internet Explorer выполняться не будет.

### УПРАВЛЕНИЕ СИНХРОНИЗАЦИЕЙ

#### Можно ли запретить пользователям синхронизацию с личным клиентом?

Прямо нет, но вы можете определить, с каким профилем можно входить в Microsoft Edge, с помощью политики [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).

## См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
