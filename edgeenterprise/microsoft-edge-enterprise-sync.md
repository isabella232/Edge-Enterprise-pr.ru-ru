---
title: Синхронизация Microsoft Edge Enterprise
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 08/03/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Синхронизация Microsoft Edge Enterprise
ms.openlocfilehash: a6d01356db478871a7c6b386bbb731b32dc4739a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980967"
---
# Синхронизация Microsoft Edge Enterprise

В этой статье объясняется, как использовать Microsoft Edge для синхронизации избранного, паролей и других данных браузера на всех устройствах, на которых выполнен вход пользователя в систему.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## Обзор

Функция синхронизации Microsoft Edge позволяет пользователям получать доступ к данным браузера на всех своих устройствах, на которых они выполняют вход в систему. К данным, поддерживаемым функцией синхронизации, относятся следующие:

- Избранное
- Пароли
- Адреса и прочее (заполнения форм)
- Коллекции
- Параметры

Функция синхронизации включается путем предоставления пользователем согласия с этим действием. Пользователи могут включать или отключать синхронизацию для всех перечисленных выше типов данных.

> [!NOTE]
> Для обеспечения поддержки функции синхронизации передаются дополнительные данные о подключении устройства и данные конфигурации (например, имя устройства, изготовитель и модель).

## Предварительные условия

Функция синхронизации Microsoft Edge для учетных записей Azure Active Directory (Azure AD) сейчас доступна в рамках следующих подписок:

- Azure AD Premium (P1 или P2)
- M365 бизнес премиум
- Office 365 E3 и более поздние версии
- Azure Information Protection (AIP) (P1 и P2)
- Все подписки EDU для образовательной сферы (O365 A1 или выше, M365 A1 или выше, либо Azure Information Protection P1 или P2 для учащихся и преподавателей)

> [!NOTE]
> Синхронизация зависит от службы защиты, предлагаемой Azure Information Protection (AIP) для защиты данных синхронизации. В настоящее время эта служба доступна для указанных выше подписок. Полный список номеров SKU с AIP см. в разделе [Ценообразование на службы защиты информации](https://azure.microsoft.com/pricing/details/information-protection/).

## Параметры конфигурации для функции синхронизации Microsoft Edge

Для включения функции синхронизации Microsoft Edge доступны следующие параметры конфигурации:

- Azure Information Protection (AIP)
- Azure AD Enterprise State Roaming (ESR)

Если обе службы AIP и ESR отключены, то пользователи увидят сообщение об ошибке, указывающее на то, что синхронизация для их учетной записи недоступна.

### Azure Information Protection (AIP)

Если служба Azure Information Protection (AIP) для клиента включена, все пользователи могут синхронизировать данные Microsoft Edge независимо от типа лицензии. Инструкции по включению службы AIP см. [здесь](https://docs.microsoft.com/azure/information-protection/activate-office365).

Чтобы ограничить синхронизацию для определенных пользователей, вы можете включить для них [Политику управления регистрацией в AADRM](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps). Если после регистрации всех необходимых пользователей синхронизация все еще недоступна, убедитесь в том, что служба IPCv3Service включена, используя командлет PowerShell [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/Get-AipServiceIPCv3?view=azureipps).

> [!CAUTION]
> Включение службы Azure Information Protection также ограничит доступ с помощью AIP для других приложений, таких как Microsoft Word или Microsoft Outlook.

### Azure AD Enterprise State Roaming (ESR)

Если функция [Enterprise State Roaming](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) (ESR) в Azure Active Directory включена для любого пользователя или клиента, они смогут использовать функцию синхронизации Microsoft Edge независимо от значения параметра политики управления регистрацией.

## Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming

Новая версия Microsoft Edge— это межплатформенное приложение для расширенной синхронизации пользовательских данных на всех используемых устройствах. Приложение больше не входит состав службы Enterprise State Roaming в Azure AD. Однако в новой версии Microsoft Edge будут реализованы средства защиты данных, аналогичные ESR, такие как возможность использования собственного ключа. Дополнительные сведения см. в разделе [Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Синхронизация групповых политик

На функцию синхронизации Microsoft Edge влияют следующие групповые политики:

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): полное отключение синхронизации.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): отключает сохранение журнала браузера и синхронизацию. Эта политика также отключает синхронизацию открытых вкладок.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Настройка списка типов, которые исключены из синхронизации.

## Вопросы и ответы

### БЕЗОПАСНОСТЬ И СООТВЕТСТВИЕ СЕРВЕРА/ДАННЫХ

#### Шифруются ли синхронизированные данные? 

Данные шифруются при передаче с использованием протокола TLS 1.2 или более поздней версии, а также дополнительно в других службах Майкрософт с использованием AES256.

#### Где хранятся данные синхронизации Microsoft Edge?

Синхронизированные данные учетных записей Azure AD хранятся на защищенных серверах в соответствии с идентификатором клиента. Например, данные клиента, зарегистрированного в США, хранятся на серверах, расположенных в этом географическом регионе, и к ним применяется то же самое решение для хранения, что и к приложениям Office.

#### Выходят ли данные за пределы облака Майкрософт помимо синхронизации с Microsoft Edge?

Нет.

#### Могут ли администраторы клиента использовать свой ключ?

Да, с помощью[ Azure Information Protection](https://azure.microsoft.com/services/information-protection/).

#### Каковы условия использования синхронизации в корпоративной среде?

Условия предоставления услуг те же, что и для вашей подписки на Azure AD. Все условия предоставления услуг в Azure AD регулируются [условиями использования веб-служб](https://www.microsoft.com/licensing/product-licensing/products) Майкрософт.

#### Поддерживает ли Microsoft Edge стандарты соответствия требованиям облака сообщества для государственных организаций (GCC High)?

Еще нет. GCC High использует уровень D, тогда как Microsoft Edge поддерживает стандарты соответствия требованиям до уровня C.

### ПРИМЕНЕНИЕ СИНХРОНИЗАЦИИ

#### Что произойдет с корпоративными клиентами и клиентами из сферы образования, которые решат продолжить использовать устаревшую версию Microsoft Edge?

Текущая версия браузера Microsoft Edge продолжит входить в состав предложения ESR.

#### Почему для синхронизации нужна подписка Azure AD Premium?

Синхронизация в корпоративной среде зависит от службы Azure Information Protection, которая доступна не для всех уровней Azure AD.

#### Основана ли функция синхронизации Microsoft Edge на Enterprise State Roaming?

Нет. ESR может использоваться для включения синхронизации, но функция синхронизации Microsoft Edge не входит в состав ESR. Дополнительные сведения см. в разделах [Функция синхронизации Microsoft Edge](microsoft-edge-enterprise-sync.md) и [Microsoft Edge и Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

#### Будет ли Microsoft Edge поддерживать синхронизацию между Microsoft Edge и IE?

Поддержка такой синхронизации не планируется. Если для поддержки устаревших приложений вам нужен IE, подумайте об использовании [нового режима IE](https://docs.microsoft.com/deployedge/edge-ie-mode).

#### Будет ли синхронизироваться новый браузер Microsoft Edge с устаревшей версией Microsoft Edge?

Нет, не будет. Мы считаем, что объединение этих двух экосистем может привести к нарушению надежности синхронизации в новой версии Microsoft Edge. Мы обеспечим перенос имеющихся данных в новую версию Microsoft Edge. Кроме того, пользователи смогут импортировать данные из браузера, которым они пользуются. Это также означает, что синхронизация между новым браузером Microsoft Edge и браузером Internet Explorer выполняться не будет.

### УПРАВЛЕНИЕ СИНХРОНИЗАЦИЕЙ

#### Можно ли запретить пользователям синхронизацию с личным клиентом?

Прямо нет, но вы можете определить, с каким профилем можно входить в Microsoft Edge, с помощью политики [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).

## См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
