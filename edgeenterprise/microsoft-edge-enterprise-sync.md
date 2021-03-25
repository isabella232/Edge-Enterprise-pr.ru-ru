---
title: Настройка синхронизации Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Параметры пользователя и администратора для настройки синхронизации избранного, паролей и других данных браузера в Microsoft Edge.
ms.openlocfilehash: 93af96bd864f08bb17bb1d6f0669f602a56fd8ca
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448123"
---
# <a name="configure-microsoft-edge-enterprise-sync"></a>Настройка синхронизации Microsoft Edge Enterprise

В этой статье рассказывается о том, как администраторы могут настроить синхронизацию избранного пользователя, паролей и других данных браузера в Microsoft Edge на всех устройствах, на которых выполнен вход.

> [!NOTE]
> Применяется к Microsoft Edge версии 77 или более поздней, если не указано иное.

## <a name="overview"></a>Обзор

Функция синхронизации Microsoft Edge позволяет пользователям получать доступ к данным браузера на всех своих устройствах, на которых они выполняют вход в систему. К данным, поддерживаемым функцией синхронизации, относятся следующие:

- Избранное
- Пароли
- Адреса и прочее (заполнения форм)
- Коллекции
- Параметры
- Расширение
- Открытые вкладки (доступно в Microsoft Edge версии 88)
- Журнал (доступно в Microsoft Edge версии 88)

Функциональность синхронизации включается путем предоставления согласия пользователя. Пользователи могут включать или отключать синхронизацию для каждого из перечисленных выше типов данных. Если у пользователя возникли проблемы с синхронизацией, может потребоваться сброс синхронизации в разделе **Параметры** > **Профили** > **Сбросить синхронизацию**.

> [!NOTE]
> Для поддержки функциональности синхронизации передаются дополнительные данные о подключении устройства и конфигурации (например, имя устройства, изготовитель и модель).

## <a name="prerequisites"></a>Предварительные условия

Функция синхронизации Microsoft Edge для учетных записей Azure Active Directory (Azure AD) доступна в рамках любой из этих подписок:

- Azure AD Premium (P1 или P2)
- M365 бизнес премиум
- Office 365 E1 и более поздние версии
- Azure Information Protection (AIP) (P1 или P2)
- Все подписки EDU (приложения Майкрософт для учащихся или преподавателей, Exchange Online для учащихся или преподавателей, O365 A1 или выше, M365 A1 или выше, Azure Information Protection P1 или P2 для учащихся или преподавателей)

## <a name="sync-group-policies"></a>Синхронизация групповых политик

Администраторы могут использовать следующие групповые политики для настройки и управления синхронизацией Microsoft Edge:

- [SyncDisabled](./microsoft-edge-policies.md#syncdisabled): полное отключение синхронизации.
- [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): отключает сохранение журнала браузера и синхронизацию. Эта политика также отключает синхронизацию открытых вкладок.
- [AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): если эта политика отключена, синхронизация журнала также будет отключена.
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): настройка списка типов, исключенных из синхронизации.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): разрешает профилям Active Directory (AD) использовать локальное хранилище. Дополнительные сведения см. в статье [Локальная синхронизация для пользователей Active Directory (AD)](./microsoft-edge-on-premises-sync.md).
- [ForceSync:]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync) включает синхронизацию по умолчанию и не требует согласия пользователя.  

## <a name="configure-microsoft-edge-sync"></a>Настройка синхронизации Microsoft Edge

Параметры конфигурации для функции синхронизации Microsoft Edge доступны в службе Azure Information Protection (AIP). Если служба AIP включена для клиента, все пользователи могут синхронизировать данные в Microsoft Edge независимо от типа лицензии. Инструкции по включению службы AIP см. [здесь](/azure/information-protection/activate-office365).

Чтобы ограничить синхронизацию для определенной группы пользователей, вы можете включить для них [политику управления регистрацией в AIP](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) . Если после регистрации всех необходимых пользователей синхронизация все еще недоступна, убедитесь в том, что служба IPCv3Service включена, используя командлет PowerShell [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps).

> [!CAUTION]
> При включении службы Azure Information Protection другие приложения, такие как Microsoft Word и Microsoft Outlook, также смогут защищать контент с помощью AIP. Кроме того, любая политика управления регистрацией, используемая для ограничения синхронизации Microsoft Edge, также ограничит защиту контента с помощью AIP в других приложениях.

## <a name="microsoft-edge-and-enterprise-state-roaming-esr"></a>Microsoft Edge и Enterprise State Roaming (ESR)

Microsoft Edge— это межплатформенное приложение с широкими возможностями синхронизации пользовательских данных на всех используемых устройствах. Приложение больше не входит состав службы Enterprise State Roaming в Azure AD. Однако в Microsoft Edge будут реализованы средства защиты данных, аналогичные ESR, такие как возможность использования собственного ключа. Дополнительные сведения см. в разделе [Microsoft Edge и Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## <a name="see-also"></a>См. также

- [Синхронизация Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
- [Диагностика и устранение проблем синхронизации Microsoft Edge](microsoft-edge-troubleshoot-enterprise-sync.md)
- [Microsoft Edge и Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)