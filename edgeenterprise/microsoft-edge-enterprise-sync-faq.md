---
title: Вопросы и ответы о синхронизации Microsoft Edge для предприятий
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Вопросы и ответы о синхронизации Microsoft Edge для предприятий.
ms.openlocfilehash: a13e1f02f6e871004d45f81159d5cf0a3397b6ad
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643145"
---
# <a name="microsoft-edge-enterprise-sync-faq"></a>Вопросы и ответы о синхронизации Microsoft Edge для предприятий

В этой статье содержатся ответы на самые популярные вопросы о синхронизации Microsoft Edge версии 77 или более поздней для предприятий.

## <a name="security-and-serverdata-compliance"></a>Безопасность и соответствие сервера/данных

### <a name="is-the-synced-data-encrypted"></a>Шифруются ли синхронизированные данные?

Данные шифруются в процессе транспортировки с использованием протокола TLS 1.2 или более поздней версии. Все типы данных дополнительно шифруются в службе Майкрософт с помощью AES128. Все типы данных, кроме используемых для синхронизации открытой вкладки и журнала, дополнительно шифруются перед покиданием устройства пользователя с использованием ключей, управляемых с помощью политики [Azure Information Protection](./microsoft-edge-policies.md#restrictsignintopattern).

### <a name="why-dont-open-tab-and-history-data-have-more-client-side-encryption"></a>Почему данные открытой вкладки и журнала не используют дополнительное шифрование на стороне клиента?

Чтобы сократить использование ресурсов на устройствах конечных пользователей, данные журнала создаются на стороне сервера на основе перемещаемых данных открытой вкладки. Этот процесс невозможен при шифровании этих данных на стороне клиента. Чтобы отключить синхронизацию открытой вкладки и журнала, примените политику [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) или [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled).

### <a name="can-tenant-admins-bring-their-own-key"></a>Могут ли администраторы клиента использовать свой ключ?

Да, с помощью  [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).

### <a name="where-is-microsoft-edge-sync-data-stored"></a>Где хранятся данные синхронизации Microsoft Edge?

Синхронизированные данные учетных записей Azure AD хранятся на защищенных серверах в соответствии с идентификатором клиента. Например, данные клиента, зарегистрированного в США, хранятся на серверах, расположенных в этом географическом регионе, и к ним применяется то же самое решение для хранения, что и к приложениям Office.

### <a name="does-the-data-ever-leave-microsofts-cloud-aside-from-syncing-to-microsoft-edge"></a>Выходят ли данные за пределы облака Майкрософт помимо синхронизации с Microsoft Edge?

Нет.

### <a name="what-terms-of-service-does-enterprise-sync-fall-under"></a>Каковы условия использования синхронизации в корпоративной среде?

Условия использования функции синхронизации Microsoft Edge регулируются лицензией на программное обеспечение корпорации Майкрософт, с которой можно ознакомиться в Microsoft Edge по адресу  *edge://terms*. Ваша подписка на Azure AD и условия обслуживания в конечном итоге регулируются [условиями использования веб-служб](https://www.microsoft.com/licensing/product-licensing/products) Майкрософт.

### <a name="does-microsoft-edge-support-government-community-cloud-gcc-high-compliance"></a>Поддерживает ли Microsoft Edge стандарты соответствия требованиям облака сообщества для государственных организаций (GCC High)?

Еще нет. Для клиентов в облаке GCC High синхронизация Microsoft Edge отключена.

## <a name="applying-sync"></a>Применение синхронизации

### <a name="why-isnt-microsoft-edge-sync-supported-in-all-m365-subscriptions"></a>Почему синхронизация Microsoft Edge не поддерживается во всех подписках M365?

Синхронизация в корпоративной среде зависит от службы [Azure Information Protection](https://azure.microsoft.com/services/information-protection/), которая доступна не во всех подписках M365.

### <a name="is-microsoft-edge-sync-based-on-enterprise-state-roaming"></a>Основана ли функция синхронизации Microsoft Edge на Enterprise State Roaming?

Нет. ESR может использоваться для включения синхронизации, но функция синхронизации Microsoft Edge не входит в состав ESR. Дополнительные сведения см. в разделах [Функция синхронизации Microsoft Edge](/DeployEdge/microsoft-edge-enterprise-sync) и [Microsoft Edge и Enterprise State Roaming](/DeployEdge/microsoft-edge-enterprise-state-roaming).

### <a name="will-microsoft-edge-ever-support-syncing-between-microsoft-edge-and-ie"></a>Будет ли Microsoft Edge поддерживать синхронизацию между Microsoft Edge и IE?

Поддержка такой синхронизации не планируется. Если для поддержки устаревших приложений вам нужен IE, подумайте об использовании [нового режима IE](./edge-ie-mode.md).

### <a name="will-microsoft-edge-sync-with-microsoft-edge-legacy"></a>Будет ли Microsoft Edge синхронизироваться с устаревшей версией Microsoft Edge?

Нет, не будет. Мы считаем, что объединение этих двух экосистем может привести к нарушению надежности синхронизации в Microsoft Edge. Мы обеспечим перенос имеющихся данных в Microsoft Edge. Пользователи также смогут импортировать данные из браузера по своему выбору, что также означает, что Microsoft Edge не сможет синхронизироваться с Internet Explorer.

## <a name="managing-sync"></a>Управление синхронизацией

### <a name="is-it-possible-to-stop-my-users-from-syncing-with-a-personal-tenant"></a>Можно ли запретить пользователям синхронизацию с личным клиентом?

Прямо нет, но вы можете определить, с каким профилем можно входить в Microsoft Edge, с помощью политики [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern).

## <a name="see-also"></a>См. также

- [Синхронизация Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)