---
title: Настройка и устранение неполадок синхронизации Microsoft Edge
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 01/14/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Настройка и устранение неполадок синхронизации Microsoft Edge
ms.openlocfilehash: fa9b9ead6319bceeb95066003a77be7ecf84db46
ms.sourcegitcommit: 68b50c45b2b78acec5a0776ce4ddd11410a4e382
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "11270785"
---
# Настройка и устранение неполадок синхронизации Microsoft Edge

В этой статье объясняется, как настроить и использовать Microsoft Edge для синхронизации избранного, паролей и других данных браузера на всех устройствах, на которых выполнен вход в систему. В этой статье также приводятся инструкции по устранению наиболее распространенных проблем синхронизации. Эта статья также содержит сведения о рекомендуемых средствах для сбора журналов, необходимых для устранения неполадок.

> [!NOTE]
> Применяется к Microsoft Edge версии 77 или более поздней, если не указано иное.

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

## Синхронизация групповых политик

Для настройки синхронизации Microsoft Edge и управления ею можно использовать следующие групповые политики.

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): полное отключение синхронизации.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): отключает сохранение журнала браузера и синхронизацию. Эта политика также отключает синхронизацию открытых вкладок.
- [AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): если эта политика отключена, синхронизация журнала также будет отключена.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): настройка списка типов, исключенных из синхронизации.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): разрешает профилям Active Directory (AD) использовать локальное хранилище. Дополнительные сведения см. в статье [Локальная синхронизация для пользователей Active Directory (AD)](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).
- [ForceSync:]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync) включает синхронизацию по умолчанию и не требует согласия пользователя.  

## Настройка синхронизации Microsoft Edge

Параметры конфигурации для функции синхронизации Microsoft Edge доступны в службе Azure Information Protection (AIP). Если служба AIP включена для клиента, все пользователи могут синхронизировать данные в Microsoft Edge независимо от типа лицензии. Инструкции по включению службы AIP см. [здесь](https://docs.microsoft.com/azure/information-protection/activate-office365).

Чтобы ограничить синхронизацию для определенной группы пользователей, вы можете включить для них [политику управления регистрацией в AIP](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) . Если после регистрации всех необходимых пользователей синхронизация все еще недоступна, убедитесь в том, что служба IPCv3Service включена, используя командлет PowerShell [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true).

> [!CAUTION]
> При включении службы Azure Information Protection другие приложения, такие как Microsoft Word и Microsoft Outlook, также смогут защищать контент с помощью AIP. Кроме того, любая политика управления регистрацией, используемая для ограничения синхронизации Microsoft Edge, также ограничит защиту контента с помощью AIP в других приложениях.

## Microsoft Edge и Enterprise State Roaming (ESR)

Microsoft Edge— это межплатформенное приложение с широкими возможностями синхронизации пользовательских данных на всех используемых устройствах. Приложение больше не входит состав службы Enterprise State Roaming в Azure AD. Однако в Microsoft Edge будут реализованы средства защиты данных, аналогичные ESR, такие как возможность использования собственного ключа. Дополнительные сведения см. в разделе [Microsoft Edge и Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Устранение неполадок синхронизации

В этом разделе приводятся инструкции по устранению наиболее распространенных проблем синхронизации. Эта статья также содержит сведения о рекомендуемых средствах для сбора журналов, необходимых для устранения неполадок.

### Проблемы с удостоверениями и проблемы синхронизации

Наиболее популярный способ сохранения удостоверений пользователей в браузере — поддержка синхронизации. Поэтому проблемы с удостоверениями часто путают с проблемами синхронизации. Прежде чем приступить к устранению неполадок синхронизации, необходимо понять разницу между проблемами с удостоверениями и проблемами синхронизации.

Прежде чем решать проблему синхронизации, проверьте, вошел ли пользователь в браузер с помощью действительной учетной записи.

На следующем снимке экрана показан пример ошибки удостоверения, обнаруженной в разделе **Учетные данные** в *edge://sync-internals*.

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Ошибка удостоверения":::

### Распространенные проблемы синхронизации

#### Проблема: Нет доступа к подписке M365 или Azure Information Protection.

У вас есть предыдущая подписка M365 или Azure Information Protection (AIP), срок действия которой истек, и которая затем была заменена новой подпиской? Если да, то ИД клиента изменился и данные службы нужно сбросить. Инструкции по сбросу данных см. в разделе **Ошибка кодировщика**.

#### Проблема: "Синхронизация для этой учетной записи недоступна".

Если эта ошибка обнаружена для учетной записи Azure Active Directory или если в *edge://sync-internals* отображается DISABLED_BY_ADMIN, последовательно выполните инструкции, описанные в следующей процедуре, пока проблема не будет устранена.

> [!NOTE]
> Поскольку источник этой ошибки обычно требует изменения конфигурации в клиенте Azure Active Directory, эти действия по устранению неполадок может выполнить только администратор клиента, а не пользователь.

1. Убедитесь, что у корпоративного клиента есть поддерживаемая подписка M365. Текущий список доступных типов подписки [представлен здесь](https://docs.microsoft.com/azure/information-protection/activate-office365). Если у клиента нет поддерживаемой подписки, он можно приобрести Azure Information Protection отдельно или обновиться до одной из поддерживаемых подписок.
2. Если поддерживаемая подписка доступна, убедитесь, что у клиента есть служба Azure Information Protection (AIP). Инструкции по проверке состояния службы AIP и, если требуется, по ее активации см. [здесь](https://docs.microsoft.com/azure/information-protection/activate-office365).
3. Если на шаге 2 видно, что AIP активен, но синхронизация по-прежнему не работает, включите Enterprise State Roaming (ESR). Инструкции по включению ESR см. [здесь](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-enable). Обратите внимание, что служба ESR не должна оставаться включенной. Если на этом шаге проблема исправлена, службу ESR можно отключить.
4. Убедитесь, что служба Azure Information Protection не ограничена с помощью политики регистрации. Вы можете использовать приложение PowerShell [Get-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps), чтобы узнать, включено ли ограничение. В следующих двух примерах показана неограниченная конфигурация и конфигурация, ограниченная определенной группой безопасности.

   ```powershell
    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False 
   ```

   ```powershell

    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False f1488a05-8196-40a6-9483-524948b90282   All
   ```


   Если ограничение включено, затронутый пользователь должен быть либо добавлен в группу безопасности для ограничения, либо ограничение должно быть удалено. В приведенном ниже примере регистрация ограничила AIP указанной группой безопасности и ограничение должно быть удалено с помощью приложения PowerShell [Set-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps).

5. Убедитесь, что в клиенте включена служба IPCv3Service. Приложение PowerShell [Get-AadrmConfiguration](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps) показывает состояние службы.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Проверьте, включена ли служба IPCv3Service.":::

6. Если проблема не исчезла, обратитесь в [службу поддержки Microsoft Edge](https://www.microsoftedgeinsider.com/support).

#### Проблема: Зависание с состоянием "Настройка синхронизации..." или "Не удалось подключиться к серверу синхронизации. Выполняется повторная попытка..."

1. Попробуйте выйти из системы и снова в нее войти.
2. Перейдите в *edge://sync-internals*. Если в разделе "**Сведения о типе**" присутствует следующая ошибка, переходите к следующей проблеме, **Ошибка кодировщика**.

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. Попробуйте проверить связь с конечной точкой сервера. Конечная точка сервера для клиента доступна в *edge://sync-internals*. На следующем снимке экрана показаны сведения о конечной точке в разделе **Сведения об окружении**.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info.png" alt-text="Сведения о конечной точке":::

4. Если конечная точка сервера пуста или связь с сервером не может быть проверена и в среде присутствует брандмауэр, убедитесь, что для клиентского компьютера доступны необходимые конечные точки службы.

   - Конечные точки службы синхронизации Microsoft Edge:
     - [https://edge-enterprise.activity.windows.com](https://edge-enterprise.activity.windows.com)
     - [https://edge.activity.windows.com](https://edge.activity.windows.com)
    - Конечные точки Azure Information Protection:
      - [https://api.aadrm.com](https://api.aadrm.com) (для большинства клиентов)
      - [https://api.aadrm.de](https://api.aadrm.de) (для клиентов в Германии)
      - [https://api.aadrm.cn](https://api.aadrm.cn) (для клиентов в Китае)
   - [Конечные точки службы уведомлений Windows.](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

5. Если проблема не устранена, обратитесь в [службу поддержки Microsoft Edge](https://www.microsoftedgeinsider.com/support).

### Проблема: Ошибка кодировщика

Эта ошибка отображается в разделе **Сведения о типе** в *edge://sync-internals* и может означать, что требуется сбросить данные на стороне службы пользователя. На следующем снимке экрана показан пример сведений об ошибке шифрования.

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-crypto-error-new.png" alt-text="Ошибка кодировщика.":::

1. Перезапустите Microsoft Edge, перейдите в *edge://sync-internals* и проверьте раздел "**Состояние ключа учетной записи AAD**"
   - Пункт "Последний результат MIP" имеет значение "Успешно": ошибка кодировщика означает, что данные сервера могут быть зашифрованы с помощью потерянного ключа. Для возобновления синхронизации требуется сброс данных.
   - Пункт "Последний результат MIP" имеет значение "Нет разрешений": возможно, это вызвано изменением Azure AD или изменением подписки клиента. Для возобновления синхронизации требуется сброс данных.
   - Другие ошибки могут означать проблемы с конфигурацией сервера.
2. Если требуется сброс данных, см. статью [Сброс данных Microsoft Edge в облаке](edge-learnmore-reset-data-in-cloud.md).

#### Проблема: "Синхронизация отключена администратором".

Убедитесь, что [политика SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled) не установлена.

## Вопросы и ответы

### БЕЗОПАСНОСТЬ И СООТВЕТСТВИЕ СЕРВЕРА/ДАННЫХ

#### Шифруются ли синхронизированные данные?

Данные шифруются в процессе транспортировки с использованием протокола TLS 1.2 или более поздней версии. Все типы данных дополнительно шифруются в службе Майкрософт с помощью AES128. Все типы данных, кроме используемых для синхронизации открытой вкладки и журнала, дополнительно шифруются перед покиданием устройства пользователя с использованием ключей, управляемых с помощью политики [Azure Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).

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

Синхронизация в корпоративной среде зависит от службы [Azure Information Protection](https://azure.microsoft.com/services/information-protection/), которая доступна не во всех подписках M365.

#### Основана ли функция синхронизации Microsoft Edge на Enterprise State Roaming?

Нет. ESR может использоваться для включения синхронизации, но функция синхронизации Microsoft Edge не входит в состав ESR. Дополнительные сведения см. в разделах [Функция синхронизации Microsoft Edge](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) и [Microsoft Edge и Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).

#### Будет ли Microsoft Edge поддерживать синхронизацию между Microsoft Edge и IE?

Поддержка такой синхронизации не планируется. Если для поддержки устаревших приложений вам нужен IE, подумайте об использовании [нового режима IE](https://docs.microsoft.com/deployedge/edge-ie-mode).

#### Будет ли Microsoft Edge синхронизироваться с устаревшей версией Microsoft Edge?

Нет, не будет. Мы считаем, что объединение этих двух экосистем может привести к нарушению надежности синхронизации в Microsoft Edge. Мы обеспечим перенос имеющихся данных в Microsoft Edge. Пользователи также смогут импортировать данные из браузера по своему выбору, что также означает, что Microsoft Edge не сможет синхронизироваться с Internet Explorer.

### УПРАВЛЕНИЕ СИНХРОНИЗАЦИЕЙ

#### Можно ли запретить пользователям синхронизацию с личным клиентом?

Прямо нет, но вы можете определить, с каким профилем можно входить в Microsoft Edge, с помощью политики [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern).

## См. также

- [Синхронизация Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
