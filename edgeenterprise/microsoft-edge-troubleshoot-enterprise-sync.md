---
title: Диагностика и устранение проблем синхронизации Microsoft Edge
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Инструкции и средства, доступные администратору Microsoft Edge для устранения неполадок и решения распространенных проблем синхронизации для предприятий
ms.openlocfilehash: 767b26c74e91213b407e8264a8ed185f38dfc2e9
ms.sourcegitcommit: 86e0de9b27ad4297a6d5a57c866d7ef4fc7bb0cd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "11400207"
---
# <a name="diagnose-and-fix-microsoft-edge-sync-issues"></a>Диагностика и устранение проблем синхронизации Microsoft Edge

В этой статье содержится руководство по устранению наиболее распространенных проблем синхронизации в среде Azure Active Directory (Azure AD). Эта статья также содержит сведения о рекомендуемых средствах для сбора журналов, необходимых для устранения проблем синхронизации.

Если у пользователя возникла проблема с синхронизацией данных браузера на устройствах, он может попытаться [сбросить синхронизацию](edge-learnmore-reset-data-in-cloud.md). Если это не поможет, администраторы или сотрудники службы поддержки могут использовать следующие инструкции для устранения проблемы синхронизации.

> [!NOTE]
> Применяется к Microsoft Edge версии 77 или более поздней, если не указано иное.

## <a name="identity-issues-versus-sync-issues"></a>Проблемы с удостоверениями и проблемы синхронизации

Перед началом работы важно понять разницу между проблемами с удостоверениями и проблемами синхронизации. Наиболее популярный способ сохранения удостоверений пользователей в браузере — поддержка синхронизации. Поэтому проблемы с удостоверениями часто путают с проблемами синхронизации. Прежде чем приступить к устранению неполадок синхронизации, необходимо понять разницу между проблемами с удостоверениями и проблемами синхронизации.

Прежде чем решать проблему синхронизации, проверьте, вошел ли пользователь в браузер с помощью действительной учетной записи.

На следующем снимке экрана показан пример ошибки удостоверения. Сообщение об ошибке: "**Последняя ошибка токена, EDGE_AUTH_ERROR: 3, 54, 3ea**", которая находится в *edge://sync-internals* в разделе **Учетные данные**:

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Последняя ошибка токена EDGE_AUTH_ERROR: 3,54, 3ea":::

## <a name="common-sync-issues"></a>Распространенные проблемы синхронизации

### <a name="issue-cant-access-m365-or-azure-information-protection-subscription"></a>Проблема: Нет доступа к подписке M365 или Azure Information Protection.

У вас есть предыдущая подписка M365 или Azure Information Protection (AIP), срок действия которой истек, и которая затем была заменена новой подпиской? Если да, то ИД клиента изменился и данные службы нужно сбросить. Инструкции по сбросу данных см. в разделе **Ошибка кодировщика**.

### <a name="issue-sync-is-not-available-for-this-account"></a>Проблема: "Синхронизация для этой учетной записи недоступна".

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

### <a name="issue-stuck-at-setting-up-sync-or-couldnt-connect-to-the-sync-server-retrying"></a>Проблема: Зависание с состоянием "Настройка синхронизации..." или "Не удалось подключиться к серверу синхронизации. Выполняется повторная попытка..."

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

### <a name="issue-cryptographer-error-encountered"></a>Проблема: Ошибка кодировщика

Эта ошибка отображается в разделе **Сведения о типе** в *edge://sync-internals* и может означать, что требуется сбросить данные на стороне службы пользователя. В следующем примере показано сообщение об ошибке шифрования:
<br>"Error:GenerateCryptoErrorsForTypes@.. /.. /components/sync/driver/data_type_manager_impl.cc:42, произошла ошибка кодировщика".

1. Перезапустите Microsoft Edge, перейдите в *edge://sync-internals* и проверьте раздел "**Состояние ключа учетной записи AAD**"
   - Пункт "Последний результат MIP" имеет значение "Успешно": ошибка кодировщика означает, что данные сервера могут быть зашифрованы с помощью потерянного ключа. Для возобновления синхронизации требуется сброс данных.
   - Пункт "Последний результат MIP" имеет значение "Нет разрешений": возможно, это вызвано изменением Azure AD или изменением подписки клиента. Для возобновления синхронизации требуется сброс данных.
   - Другие ошибки могут означать проблемы с конфигурацией сервера.
2. Если требуется сброс данных, см. статью [Сброс данных Microsoft Edge в облаке](edge-learnmore-reset-data-in-cloud.md).

### <a name="issue-sync-has-been-turned-off-by-your-administrator"></a>Проблема: "Синхронизация отключена администратором".

Убедитесь, что [политика SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled) не установлена.

## <a name="see-also"></a>См. также

- [Синхронизация Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
