---
title: Документация по политикам Центра обновления Microsoft Edge
ms.author: stmoody
author: AndreaLBarr
manager: tahills
ms.date: 07/23/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
ms.custom: ''
description: Документация по всем политикам, поддерживаемым средством обновления Microsoft Edge
ms.openlocfilehash: 9c7eca4d5bdd7c87bea141a422dce3b17f22067c
ms.sourcegitcommit: 9088e839e82d80c72460586e9af0610c6ca71b83
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/23/2021
ms.locfileid: "11675946"
---
# <a name="microsoft-edge---update-policies"></a>Microsoft Edge — политики обновления

Последняя версия Microsoft Edge включает в себя следующие политики, которые можно использовать для управления процессом и временем обновления Microsoft Edge.

Сведения о других политиках, доступных в Microsoft Edge, см. в [Справочнике по политикам браузера Microsoft Edge](microsoft-edge-policies.md)
> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.
## <a name="available-policies"></a>Доступные политики
В этих таблицах указаны все групповые политики, связанные с обновлением, доступные в данном выпуске Microsoft Edge. Для получения дополнительных сведений о конкретных политиках см. ссылки в таблице.

|&nbsp;|&nbsp;| |**-**|-| |**[Приложения](#applications)**|[Параметры](#preferences)| |**[Прокси-сервер](#proxy-server)**|[Microsoft Edge WebView](#microsoft-edge-webview)|
### [<a name="applications"></a>Приложения](#applications-policies)
|Имя политики|Заголовок|
|-|-|
|[InstallDefault](#installdefault)|Разрешить установку по умолчанию|
|[UpdateDefault](#updatedefault)|Переопределение политики обновления по умолчанию|
|[Install](#install)|Разрешить установку (для канала)|
|[Update](#update)|Переопределение политики обновления (для канала)|
|[Allowsxs](#allowsxs)|Разрешить параллельный запуск разных типов браузеров Microsoft Edge|
|[CreateDesktopShortcutDefault](#createdesktopshortcutdefault)|Запрет создания ярлыка на рабочем столе при установке по умолчанию|
|[CreateDesktopShortcut](#createdesktopshortcut)|Запрет создания ярлыка на рабочем столе при установке (для каналов)|
|[RollbackToTargetVersion](#rollbacktotargetversion)|Откат к целевой версии (для каналов)|
|[TargetVersionPrefix](#targetversionprefix)|Переопределение целевой версии (для каналов)|
|[UpdaterExperimentationAndConfigurationServiceControl](#UpdaterExperimentationAndConfigurationServiceControl)| Извлечение конфигураций и экспериментов|
### [<a name="preferences"></a>Предпочтения](#preferences-policies)
|Имя политики|Заголовок|
|-|-|
|[AutoUpdateCheckPeriodMinutes](#autoupdatecheckperiodminutes)|Переопределение периода автоматической проверки обновления|
|[UpdatesSuppressed](#updatessuppressed)|Период времени в течение дня, когда будет блокироваться автоматическая проверка обновлений|

### [<a name="proxy-server"></a>Прокси-сервер](#proxy-server-policies)
|Имя политики|Действие|
|-|-|
|[ProxyMode](#proxymode)|Выбор способа задания параметров прокси-сервера|
|[ProxyPacUrl](#proxypacurl)|URL-адрес файла PAC прокси-сервера|
|[ProxyServer](#proxyserver)|Адрес или URL-адрес прокси-сервера|

### [<a name="microsoft-edge-webview"></a>Веб-представление Microsoft Edge](#microsoft-edge-webview-policies)
|Имя политики|Заголовок|
|-|-|
|[Установка](#install-webview)|Разрешить установку|
|[Обновление](#update-webview)|Переопределение политики обновления|

## <a name="applications-policies"></a>Политики приложений

[В начало](#microsoft-edge---update-policies)
### <a name="installdefault"></a>InstallDefault
#### <a name="allow-installation-default"></a>Разрешить установку по умолчанию
>Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий

#### <a name="description"></a>Описание
Вы можете указать поведение по умолчанию для всех каналов: разрешить или заблокировать Microsoft Edge на присоединенных к домену устройствах.

Вы можете переопределить эту политику для отдельных каналов, включив политику "[Разрешить установку](#install)" для конкретных каналов.

Если эта политика отключена, установка Microsoft Edge будет заблокирована. Эта политика влияет на установку программного обеспечения Microsoft Edge, только если для политики "[Разрешить установку](#install)" задано значение "Не настроено".

Эта политика не запрещает запуск Центра обновления Microsoft Edge и не запрещает пользователям устанавливать программное обеспечение Microsoft Edge другим способом.

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: InstallDefault
- Имя групповой политики: Разрешить установку по умолчанию
- Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: InstallDefault
- Тип значения: REG_DWORD
##### <a name="example-value"></a>Пример значения:
```
0x00000001
```
[В начало](#microsoft-edge---update-policies)


### <a name="updatedefault"></a>UpdateDefault
#### <a name="update-policy-override-default"></a>Переопределение политики обновления по умолчанию
>Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий

#### <a name="description"></a>Описание
Позволяет задать поведение по умолчанию для всех каналов в отношении обработки Центром обновления Microsoft Edge доступных обновлений для Microsoft Edge. Можно переопределить для отдельных каналов, задав политику "[Переопределение политики обновления](#update)" для этих конкретных каналов.

  Если эта политика включена, Центр обновления Microsoft Edge обрабатывает обновления Microsoft Edge в соответствии со значениями следующих параметров.
   - Всегда разрешать обновления: обновления всегда применяются при их обнаружении путем периодической автоматической или ручной проверки наличия обновлений.
   - Только обновления, найденные автоматически: обновления применяются только в том случае, если они были найдены при периодической автоматической проверке наличия обновлений.
   - Только обновления, найденные вручную: обновления применяются только в том случае, если пользователь запускает проверку наличия обновлений вручную.
   - Обновления отключены: обновления никогда не применяются.

  При выборе параметра "Обновления, найденные вручную" периодически проверяйте наличие обновлений с помощью механизма приложения для поиска обновлений вручную, если это возможно. При отключении обновлений разрешите периодическую автоматическую проверку наличия обновлений и их распространение для пользователей.

  Если вы не включите и не настроите эту политику, Центр обновления Microsoft Edge будет обрабатывать доступные обновления в соответствии с политикой "[Переопределение политики обновления](#update)".

  Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: UpdateDefault
- Имя групповой политики: Переопределение политики обновления по умолчанию
- Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: UpdateDefault
- Тип значения: REG_DWORD
##### <a name="example-value"></a>Пример значения:
```
0x00000003
```
[В начало](#microsoft-edge---update-policies)


### <a name="install"></a>Install
#### <a name="allow-installation"></a>Разрешить установку
>Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий

#### <a name="description"></a>Описание
Указывает, можно ли установить канал Microsoft Edge на присоединенные к домену устройства.

  Если эта политика включена для канала, установка Microsoft Edge не будет блокироваться.

  Если эта политика отключена для канала, установка Microsoft Edge будет блокироваться.

  Если эта политика не настроена для канала, конфигурация политики "[Разрешить установку по умолчанию](#installdefault)" будет определять, смогут ли пользователи устанавливать этот канал Microsoft Edge.

  Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: Install
- Имя групповой политики: Разрешить установку по умолчанию
- Путь к групповой политике: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: 
  - (Канал Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Канал Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Канал Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - Канал (Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Тип значения: REG_DWORD
##### <a name="example-value"></a>Пример значения:
```
0x00000001
```
[В начало](#microsoft-edge---update-policies)


### <a name="update"></a>Update
#### <a name="update-policy-override"></a>Переопределение политики обновления
>Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий

#### <a name="description"></a>Описание
Указывает, как Центр обновления Microsoft Edge обрабатывает доступные обновления для Microsoft Edge.

Если эта политика включена, Центр обновления Microsoft Edge обрабатывает обновления Microsoft Edge в соответствии со значениями следующих параметров.
  - Всегда разрешать обновления: обновления всегда применяются при их обнаружении путем периодической автоматической или ручной проверки наличия обновлений.
  - Только обновления, найденные автоматически: обновления применяются только в том случае, если они были найдены при периодической автоматической проверке наличия обновлений.
  - Только обновления, найденные вручную: обновления применяются только в том случае, если пользователь запускает проверку наличия обновлений вручную. (Не все приложения предоставляют интерфейс для этого варианта.)
  - Обновления отключены: обновления никогда не применяются.

При выборе параметра "Обновления, найденные вручную" периодически проверяйте наличие обновлений с помощью механизма приложения для поиска обновлений вручную, если это возможно. При отключении обновлений разрешите периодическую автоматическую проверку наличия обновлений и их распространение для пользователей.

Если вы не включите и не настроите эту политику, Центр обновления Microsoft Edge будет обрабатывать доступные обновления в соответствии с политикой "[Переопределение политики обновления по умолчанию](#updatedefault)".

Дополнительные сведения см. в статье [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406).

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: Update
- Имя групповой политики: Переопределение политики обновления
- Путь к групповой политике: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения:
  - (Канал Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Канал Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Канал Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - Канал (Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Тип значения: REG_DWORD
##### <a name="example-value"></a>Пример значения:
```
always allow updates 0x00000001
Automatic silent updates only 0x00000003
manual updates only 0x00000002
updates disabled 0x00000000
```
[В начало](#microsoft-edge---update-policies)


### <a name="allowsxs"></a>Allowsxs
#### <a name="allow-microsoft-edge-side-by-side-browser-experience"></a>Разрешить параллельный запуск разных типов браузеров Microsoft Edge
>Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий

#### <a name="description"></a>Описание
Эта политика позволяет пользователю параллельно запускать Microsoft Edge (Edge HTML) и Microsoft Edge (на основе Chromium).

Если для этой политики задано значение "Не настроено", браузер Microsoft Edge (на основе Chromium) заменит Microsoft Edge (Edge HTML) после установки Microsoft Edge (на основе Chromium) в рамках канала Stable, а также обновлений для системы безопасности за ноябрь 2019 года.  Поведение параметра "Отключено" такое же.

Если параметр "Отключено" блокирует параллельный запуск, браузер Microsoft Edge (на основе Chromium) заменит Microsoft Edge (Edge HTML) после установки Microsoft Edge (на основе Chromium) в рамках канала Stable, а также обновлений для системы безопасности за ноябрь 2019 года.  Поведение параметра "Не настроено" такое же.

Если эта политика "Включена", браузер Microsoft Edge (на основе Chromium) и браузер Microsoft Edge (HTML Edge) смогут выполняться параллельно после установки Microsoft Edge (на основе Chromium).

Чтобы эта групповая политика вступила в силу, ее необходимо настроить до выполнения автоматической установки Microsoft Edge (на основе Chromium) с помощью Центра обновления Windows. Примечание. Пользователь может заблокировать автоматическое обновление Microsoft Edge (на основе Chromium) с помощью набора средств блокировки Microsoft Edge (на основе Chromium).
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: Allowsxs
- Имя групповой политики: Разрешить параллельный запуск разных типов браузеров Microsoft Edge
- Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: Allowsxs
- Тип значения: REG_DWORD
##### <a name="example-value"></a>Пример значения:
```
0x00000001
```
[В начало](#microsoft-edge---update-policies)

### <a name="createdesktopshortcutdefault"></a>CreateDesktopShortcutDefault
#### <a name="prevent-desktop-shortcut-creation-upon-install-default"></a>Запрет создания ярлыка на рабочем столе при установке по умолчанию
>Центр обновления Microsoft Edge 1.3.128.0 и более поздних версий

#### <a name="description"></a>Описание
Позволяет указать поведение по умолчанию для всех каналов в отношении создания ярлыка на рабочем столе при установке Microsoft Edge.

  Если эта политика включена, при установке Microsoft Edge создается ярлык на рабочем столе.
Если эта политика отключена, при установке Microsoft Edge ярлык на рабочем столе не создается.
Если вы не настроите эту политику, при установке будет создан ярлык Microsoft Edge на рабочем столе.
Если Microsoft Edge уже установлен, эта политика не действует.
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: CreateDesktopShortcutDefault
- Имя групповой политики: Запрет создания ярлыка на рабочем столе при установке по умолчанию
- Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Applications
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: CreateDesktopShortcutDefault
- Тип значения: REG_DWORD
##### <a name="example-value"></a>Пример значения:
```
0x00000001
```
[В начало](#microsoft-edge---update-policies)


### <a name="createdesktopshortcut"></a>CreateDesktopShortcut
#### <a name="prevent-desktop-shortcut-creation-upon-install"></a>Запрет создания ярлыка на рабочем столе при установке
>Центр обновления Microsoft Edge 1.3.128.0 и более поздних версий

#### <a name="description"></a>Описание
Если эта политика включена, при установке Microsoft Edge создается ярлык на рабочем столе.
Если эта политика отключена, при установке Microsoft Edge ярлык на рабочем столе не создается.
Если вы не настроите эту политику, при установке будет создан ярлык Microsoft Edge на рабочем столе.
Если Microsoft Edge уже установлен, эта политика не действует.

  Если не настроить эту политику для канала, создание ярлыка при установке Microsoft Edge определяется конфигурацией политики "[Запрет создания ярлыка на рабочем столе при установке по умолчанию](#createdesktopshortcutdefault)".
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: CreateDesktopShortcut
- Имя групповой политики: Запрет создания ярлыка на рабочем столе при установке
- Путь к групповой политике: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: 
  - (Канал Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Канал Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Канал Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Канал Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Тип значения: REG_DWORD
##### <a name="example-value"></a>Пример значения:
```
0x00000001
```
[В начало](#microsoft-edge---update-policies)


### <a name="rollbacktotargetversion"></a>RollbackToTargetVersion
#### <a name="rollback-to-target-version"></a>Откат к целевой версии
>Центр обновления Microsoft Edge 1.3.133.3 и более поздних версий

#### <a name="description"></a>Описание
Указывает, что Центр обновления Microsoft Edge должен откатить установки Microsoft Edge к версии, указанной в политике "'[Переопределение целевой версии](#targetversionprefix)".

Эта политика действует, только если для политики "[Переопределение целевой версии](#targetversionprefix)" задано значение и политика "[Переопределение политики обновления](#update)" имеет одно из состояний "ВКЛ." ("Всегда разрешать обновление", "Только автоматическое обновление", "Только обновление вручную").

Если эта политика отключена или не настроена, установки, имеющие более позднюю версию, чем версия, указанная в политике "[Переопределение целевой версии](#targetversionprefix)", останутся без изменений.

Если эта политика включена, установки, имеющие более позднюю текущую версию, чем версия, указанная в политике "[Переопределение целевой версии](#targetversionprefix)", будут понижены до целевой версии.

Пользователям рекомендуется устанавливать последнюю версию браузера Microsoft Edge, чтобы обеспечить защиту, предоставляемую новейшими обновлениями для системы безопасности. Откат к более ранней версии сопровождается риском возникновения известных проблем безопасности. Эта политика предназначена для временного решения проблем, связанных с обновлением браузера Microsoft Edge.

Перед временным откатом версии браузера мы рекомендуем включить синхронизацию ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) для всех пользователей в организации. Если не включить синхронизацию, возникает риск необратимой потери данных браузера. Вся ответственность за использование этой политики ложится на пользователя.

Примечание. Все версии, доступные для отката, можно посмотреть здесь [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).

Эта политика применяется к Microsoft Edge версии 86 или более поздней версии.

Дополнительные сведения см. в статье [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918).

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: RollbackToTargetVersion
- Имя групповой политики: Откат к целевой версии
- Путь к групповой политике: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: 
  - (Канал Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Канал Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Канал Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Канал Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Тип значения: REG_DWORD
##### <a name="example-value"></a>Пример значения:
```
0x00000001
```
[В начало](#microsoft-edge---update-policies)


### <a name="targetversionprefix"></a>TargetVersionPrefix
#### <a name="target-version-override"></a>Переопределение целевой версии
>Центр обновления Microsoft Edge 1.3.119.43 и более поздних версий

#### <a name="description"></a>Описание
Если эта политика включена и включено автоматическое обновление, Microsoft Edge обновляется до версии, указанной значением этой политики.

В качестве значения политики требуется использовать определенную версию Microsoft Edge, например 83.0.499.12.

Если на устройстве установлена более поздняя версия Microsoft Edge, чем указано в значении, Microsoft Edge сохранит новую версию и не будет понижен до указанной версии.

Если указанная версия не существует или имеет неправильный формат, Microsoft Edge сохранит текущую версию и не будет автоматически обновляться до будущих версий.

Дополнительные сведения см. в статье [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707).

Эта политика доступна только для экземпляров Windows, присоединенных к домену Microsoft® Active Directory®.
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: TargetVersionPrefix
- Имя групповой политики: Переопределение целевой версии
- Путь к групповой политике: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: 
  - (Канал Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Канал Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Канал Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Канал Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Тип значения: REG_SZ
##### <a name="example-value"></a>Пример значения:
```
83.0.499.12
```
[В начало](#microsoft-edge---update-policies)

### <a name="updaterexperimentationandconfigurationservicecontrol"></a>UpdaterExperimentationAndConfigurationServiceControl
#### <a name="retrieve-configurations-and-experiments"></a>Извлечение конфигураций и экспериментов
>Центр обновления Microsoft Edge 1.3.145.1 и более поздней

#### <a name="description"></a>Описание
В Центр обновления Microsoft Edge для развертывания полезной нагрузки используется служба экспериментов и конфигурации.

Полезной нагрузки экспериментов состоит из списка ранних компонентов разработки, которые Корпорация Майкрософт позволяет для тестирования отзывов.

Если вы включаете эту политику, полезное приложение для экспериментов загружается из службы экспериментов и конфигурации.

Если отключить эту политику, связь со службой экспериментов и конфигурации полностью прекращена.

Если эта политика не настроена, на управляемом устройстве поведение будет таким же, как и политика "отключена".

Если эта политика не настроена, на неугомяемом устройстве поведение будет таким же, как и "включенная политика".

#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя GP: UpdateExperimentationAndConfigureationServiceControl
- Имя GP: связь updater Controle со службой экспериментов и конфигурации
- Путь GP: Административные шаблоны/Microsoftt Edge Update/Центр обновления Microsoft Edge
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: UpdaterExperimentationAndConfigurationServiceControl
- Тип значения: REG_DWORD
##### <a name="example-value"></a>Пример значения:
```
0x00000001
```
[В начало](#microsoft-edge---update-policies)

## <a name="preferences-policies"></a>Предпочтительные политики

[В начало](#microsoft-edge---update-policies)
### <a name="autoupdatecheckperiodminutes"></a>AutoUpdateCheckPeriodMinutes
#### <a name="auto-update-check-period-override"></a>Переопределение периода автоматической проверки обновлений
>Центр обновления Microsoft Edge 1.2.145.5 и более поздних версий

#### <a name="description"></a>Описание
Если политика включена, вы можете задать минимальное количество минут между автоматическими проверками обновлений. В противном случае по умолчанию автоматическая проверка наличия обновлений будет выполняться каждые 10 часов.

  Если необходимо отключить все автоматические проверки обновлений, задайте значение равным 0 (не рекомендуется).
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: AutoUpdateCheckPeriodMinutes
- Имя групповой политики: Переопределение периода автоматической проверки обновления
- Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Preferences
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: AutoUpdateCheckPeriodMinutes
- Тип значения: REG_DWORD
##### <a name="example-value"></a>Пример значения:
```
0x00000578
```
[В начало](#microsoft-edge---update-policies)


### <a name="updatessuppressed"></a>UpdatesSuppressed
#### <a name="time-period-in-each-day-to-suppress-auto-update-check"></a>Период времени в течение дня, когда будет блокироваться автоматическая проверка обновлений
>Центр обновления Microsoft Edge 1.3.33.5 и более поздних версий

#### <a name="description"></a>Описание
Если эта политика включена, проверки обновлений блокируются каждый день, начиная с Hour:Minute в течение заданного периода времени (в минутах). На этот период не влияет переход на летнее время. Например, если время начала равно 22:00, а длительность составляет 480 минут, обновления будут блокироваться в течение 8 часов, независимо от этапа перехода на летнее время, то есть его начала или завершения.

  Если эта политика отключена или не настроена, проверки обновлений не блокируются в течение заданного периода.
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: UpdatesSuppressed
- Имя групповой политики: Период времени в течение дня, когда будет блокироваться автоматическая проверка обновлений
  - Параметры {Hour, Minute, Duration} (Час, Минута, Длительность)
- Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Preferences
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: 
  - UpdatesSuppressedDurationMin
  - UpdatesSuppressedStartHour
  - UpdatesSuppressedStartMin
- Тип значения: REG_DWORD
##### <a name="example-value"></a>Пример значения:
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[В начало](#microsoft-edge---update-policies)

## <a name="proxy-server-policies"></a>Политики прокси-сервера

[В начало](#microsoft-edge---update-policies)
### <a name="proxymode"></a>ProxyMode
#### <a name="choose-how-to-specify-proxy-server-settings"></a>Выбор способа задания параметров прокси-сервера
>Центр обновления Microsoft Edge 1.3.21.81 и более поздних версий

#### <a name="description"></a>Описание
Позволяет указать параметры прокси-сервера, используемые Центром обновления Microsoft Edge.

  Если эта политика включена, можно выбрать один из следующих параметров прокси-сервера.
   - Если вы решите никогда не использовать прокси-сервер и всегда подключаться напрямую, все остальные параметры будут игнорироваться.
   - Если вы решите использовать системные параметры прокси-сервера или включите автоматическое определение прокси-сервера, все остальные параметры будут игнорироваться.
   - При выборе режима фиксированного прокси-сервера можно указать дополнительные параметры в политике "[Адрес или URL-адрес прокси-сервера](#proxyserver)".
   - Если вы решите использовать сценарий прокси-сервера PAC, необходимо указать URL-адрес сценария в политике "[URL-адрес файла PAC прокси-сервера](#proxypacurl)".

  Если эта политика включена, пользователи в вашей организации не смогут изменять параметры прокси-сервера в Центре обновления Microsoft Edge.

  Если эта политика отключена или не настроена, параметры прокси-сервера не будут заданы, но пользователи в вашей организации смогут задать собственные параметры прокси-сервера для Центра обновления Microsoft Edge.
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: ProxyMode
- Имя групповой политики: Выбор способа задания параметров прокси-сервера
- Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Proxy Server
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: ProxyMode
- Тип значения: REG_SZ
##### <a name="example-value"></a>Пример значения:
```
fixed_servers
```
[В начало](#microsoft-edge---update-policies)


### <a name="proxypacurl"></a>ProxyPacUrl
#### <a name="url-to-a-proxy-pac-file"></a>URL-адрес файла PAC прокси-сервера
>Центр обновления Microsoft Edge 1.3.21.81 и более поздних версий

#### <a name="description"></a>Описание
Позволяет указать URL-адрес к файлу автоматической настройки прокси-сервера (PAC).

  Если эта политика включена, вы можете указать URL-адрес для файла PAC, чтобы автоматизировать процесс выбора подходящего прокси-сервера Центром обновления Microsoft Edge для загрузки конкретного веб-сайта.

  Эта политика применяется только в том случае, если параметры прокси-сервера были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".

  Не настраивайте эту политику, если параметры прокси-сервера не были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: ProxyPacUrl
- Имя групповой политики: URL-адрес файла PAC прокси-сервера
- Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Proxy Server
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: ProxyPacUrl
- Тип значения: REG_SZ
##### <a name="example-value"></a>Пример значения:
```
https://www.microsoft.com
```
[В начало](#microsoft-edge---update-policies)


### <a name="proxyserver"></a>ProxyServer
#### <a name="address-or-url-of-proxy-server"></a>Адрес или URL-адрес прокси-сервера
>Центр обновления Microsoft Edge 1.3.21.81 и более поздних версий

#### <a name="description"></a>Описание
Позволяет указать URL-адрес прокси-сервера, который будет использовать Центр обновления Microsoft Edge.

  Если эта политика включена, вы можете задать URL-адрес прокси сервера, который будет использовать Центр обновления Microsoft Edge в вашей организации.

  Эта политика применяется только в том случае, если параметры прокси-сервера были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".

  Не настраивайте эту политику, если параметры прокси-сервера не были заданы вручную в политике "[Выбор способа задания параметров прокси-сервера](#proxymode)".
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: ProxyServer
- Имя групповой политики: Адрес или URL-адрес прокси-сервера
- Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Proxy Server
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: ProxyServer
- Тип значения: REG_SZ
##### <a name="example-value"></a>Пример значения:
```
https://www.microsoft.com
```
[В начало](#microsoft-edge---update-policies)


## <a name="microsoft-edge-webview-policies"></a>Политики веб-представления Microsoft Edge

[В начало](#microsoft-edge---update-policies)
### <a name="install-webview"></a>Установка (веб-представление)
#### <a name="allow-installation"></a>Разрешить установку
>Центр обновления Microsoft Edge 1.3.127.1 и более поздних версий

#### <a name="description"></a>Описание
Позволяет указать, можно ли установить веб-представление Microsoft Edge с помощью Центра обновления Microsoft Edge.

  - Если эта политика включена, пользователи смогут установить веб-представление Microsoft Edge с помощью Центра обновления Microsoft Edge.
  - Если эта политика отключена, пользователи не смогут установить веб-представление Microsoft Edge с помощью Центра обновления Microsoft Edge.
  - Если эта политика не настроена, возможность установки пользователями веб-представления Microsoft Edge через Центр обновления Microsoft Edge будет определяться конфигурацией политики "[Разрешить установку по умолчанию](#installdefault)".
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: Install
- Имя групповой политики: Разрешить установку по умолчанию
- Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: 
  - Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
- Тип значения: REG_DWORD
##### <a name="example-value"></a>Пример значения:
```
0x00000001
```
[В начало](#microsoft-edge---update-policies)


### <a name="update-webview"></a>Обновление (веб-представление)
#### <a name="update-policy-override"></a>Переопределение политики обновления
>Центр обновления Microsoft Edge 1.3.127.1 и более поздних версий

#### <a name="description"></a>Описание
Позволяет указать, включено ли автоматическое обновление для веб-представления Microsoft Edge. Веб-представление Microsoft Edge — это компонент, используемый приложениями для отображения веб-содержимого.
Автоматическое обновление включено по умолчанию. Отключение автоматического обновления веб-представления Microsoft Edge может привести к проблемам совместимости с приложениями, зависящими от этого компонента.

  Если эта политика включена, Центр обновления Microsoft Edge обрабатывает обновления веб-представления Microsoft Edge в соответствии со значениями следующих параметров.
  - Всегда разрешать обновления. Обновления скачиваются и применяются автоматически
  - Обновления отключены. Обновления никогда не скачиваются и не применяются

  Если эта политика не включена, обновления скачиваются и применяются автоматически.
#### <a name="windows-information-and-settings"></a>Сведения и параметры Windows
##### <a name="group-policy-admx-info"></a>Сведения о групповой политике (ADMX)
- Уникальное имя групповой политики: Update
- Имя групповой политики: Переопределение политики обновления
- Путь к групповой политике: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView
- Имя ADMX-файла групповой политики: msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Параметры реестра Windows
- Путь: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Имя значения: 
  - Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
- Тип значения: REG_DWORD
##### <a name="example-value"></a>Пример значения:
```
0x00000001
```
[В начало](#microsoft-edge---update-policies)


## <a name="see-also"></a>См. также
  - [Настройка Microsoft Edge](configure-microsoft-edge.md)
  - [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
