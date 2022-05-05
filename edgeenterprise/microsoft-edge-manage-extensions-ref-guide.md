---
title: Подробное руководство по политике ExtensionSettings
ms.author: aspoddar
author: dan-wesley
manager: balajek
ms.date: 01/12/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Подробное руководство по настройке расширений Microsoft Edge с помощью политики ExtensionSettings.
ms.openlocfilehash: e020e6b082021b3c876992a59a3b3436a24789c0
ms.sourcegitcommit: 592f6e40b13e28af588473b2a75c3ae697e5db2d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2022
ms.locfileid: "12505472"
---
# <a name="a-detailed-guide-to-configuring-extensions-using-the-extensionsettings-policy"></a>Подробное руководство по настройке расширений с помощью политики ExtensionSettings

Microsoft Edge предлагает несколько способов управления расширениями. Распространенным способом является настройка нескольких политик в одном месте с помощью строки JSON в редакторе групповой политики Windows или в реестре Windows, используя политику[ExtensionSettings.](/deployedge/microsoft-edge-policies#extensionsettings)

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздних версий.

## <a name="before-you-begin"></a>Перед началом работы

Решите, следует ли задать все параметры управления расширениями в политике ExtensionSettings или настроить эти элементы управления с помощью других политик.
  
Политика ExtensionSettings может заменять другие политики, которые были установлены в других частях групповой политики, включая следующие:

- [ExtensionAllowedTypes](/DeployEdge/microsoft-edge-policies#extensionallowedtypes)
- [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist)
- [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ExtensionInstallSources](/DeployEdge/microsoft-edge-policies#extensioninstallsources)
- [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallsources)

## <a name="extensionsettings-policy-fields"></a>Поля политики ExtensionSettings

Эта политика может управлять такими параметрами, как URL-адрес обновления, из которого будет скачан расширение для начальной установки, и заблокированные разрешения. Эту политику также можно использовать для определения разрешений, которые не разрешены для запуска. Доступные поля политик описаны в следующей таблице.

| Поле политики | Описание |
|--|--|
| **allowed_types** | Можно использовать только для настройки конфигурации по умолчанию,*. Указывает, какие типы приложений или расширений разрешено устанавливать на Microsoft Edge. Значение представляет собой список строк, каждая из которых должна иметь одно из следующих значений: "extension", "theme", "user_script", и "hosted_app".   |
| **blocked_install_message**| Если вы блокируете установку определенных расширений пользователями, можно указать сообщение, которое будет отображаться в браузере, если пользователи попытаются установить их.<br>Добавление текста к универсальному сообщению об ошибке, отображаемому на веб-сайте надстроек Microsoft Edge. Например, вы можете сообщить пользователям, как связаться с ИТ-отделом, или почему конкретное расширение недоступно. Сообщение должно содержать не более 1 000 символов.   |
|**blocked_permissions**  | Не позволяет пользователям устанавливать и запускать расширения, которые требуют определенных разрешений API, запрещенных вашей организацией. Например, можно заблокировать расширения, которые обращаются к файлам cookie. Если расширение требует разрешения, которое вы заблокировали, пользователь не может установить его. Если пользователи ранее установили расширение, оно больше не будет загружаться. Если расширение содержит заблокированные разрешения в качестве необязательных требований, оно устанавливается в обычном режиме. Затем при запуске расширения заблокированные разрешения будут автоматически отклонены.<br>Список доступных разрешений см. в разделе [Объявление разрешений.](/microsoft-edge/extensions-chromium/enterprise/declare-permissions)   |
| **installation_mode**| Указывает, добавляются ли в Microsoft Edge расширения, которые вы указываете, и если дат, то как. Можно задать один из следующих режимов установки:<br>— allowed: пользователи могут установить расширение. Если не определен режим установки, этот параметр применяется по умолчанию.<br>— blocked: пользователи не могут установить расширение.<br>— force_installed: автоматическая установка расширения без взаимодействия с пользователем. Пользователи не могут удалить его. Также необходимо определить расположение загрузки расширения с помощью update_url. **Примечание.** Этот параметр нельзя использовать с *, потому что Microsoft Edge не сможет определить, какое расширение нужно автоматически установить.<br>— normal_installed: автоматически устанавливать расширение без взаимодействия с пользователем. Пользователи могут отключить его. Также необходимо определить расположение загрузки расширения с помощью update_url. **Примечание.** Этот параметр нельзя использовать с *, потому что Microsoft Edge не сможет определить, какое расширение нужно автоматически установить.<br>— removed: пользователи не могут установить расширение. Если пользователи ранее устанавливали расширение, Microsoft Edge удалит его. |
| **install_sources** | Можно использовать только для настройки конфигурации по умолчанию,*. Указывает, с каких URL-адресов можно устанавливать расширения. Этим шаблонам должно быть разрешено как местоположение файла *.crx, так и страница, с которой начинается загрузка (реферер). Примеры шаблонов URL см. в разделе [Шаблоны соответствия](/microsoft-edge/extensions-chromium/enterprise/match-patterns).  |
| **minimum_version_required** |Microsoft Edge отключает расширения, в том числе вынужденно установленные расширения, с версией старше указанной минимальной версии.<br>Формат строки версии тот же, что и в манифесте расширения.     |
| **update_url** | Применяется только к force_installed и  normal_installed. Указывает, откуда Microsoft Edge следует скачать расширение. Если расширение расположено на веб-сайте надстроек Microsoft Edge, используйте это расположение: `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.<br>Microsoft Edge использует URL-адрес, указанный вами для начальной установки расширения. Для последующих обновлений расширения Microsoft Edge использует URL-адрес в манифесте расширения.   |
| **runtime_allowed_hosts**| Позволяет расширениям взаимодействовать с указанными веб-сайтами, даже если они также определены в runtime_blocked_hosts. Можно указать до 100 элементов. Элементы сверх этого числа удаляются.<br>Формат шаблона узла аналогичен  [шаблонам соответствия](/microsoft-edge/extensions-chromium/enterprise/match-patterns) , но нельзя задать путь. Например:<br>- *://*.example.com<br>- *://example.* — поддерживаются подстановочные знаки eTLD     |
| **runtime_blocked_hosts**| Запретить расширениям взаимодействовать с указанными веб-сайтами или изменять их. Изменения включают блокировку внедрения JavaScript, доступ к файлам cookie и изменения по веб-запросу.<br>Можно указать до 100 элементов. Элементы сверх этого числа удаляются.<br>Формат шаблона узла похож на шаблоны соответствия, но нельзя задать путь. Например:<br>- *://*.example.com<br>- *://example.* — поддерживаются подстановочные знаки eTLD   |
| **override_update_url**| Доступно из Microsoft Edge 93<br>`true`Если для этого поля задано значение Microsoft Edge использует URL-адрес обновления, указанный в политике ExtensionSettings или в политике ExtensionInstallForcelist, для последующих обновлений расширений.<br>Если это поле не задано `false`или имеет значение Microsoft Edge использует URL-адрес, указанный в манифесте расширения, для обновлений.|
| **toolbar_state**| Доступно из Microsoft Edge 94<br>Этот параметр политики позволяет принудительно отображать установленное расширение на панели инструментов. Состояние по умолчанию — для `default_shown` всех расширений. Для этого параметра возможны следующие состояния.<br>-`force_shown`: можно принудительно отобразить установленное расширение на панели инструментов. Пользователи не смогут скрыть указанный значок расширения на панели инструментов.<br>-`default_hidden`: в этом состоянии расширения скрыты на панели инструментов при установке. При необходимости пользователи могут отображать их на панели инструментов.<br>-`default_shown`: это параметр по умолчанию для всех установленных расширений в браузере. |

Следующие ключи разрешены в глобальной области (*):

- blocked_permissions
- installation_mode — только `"blocked"`или `"allowed"``"removed"` являются допустимыми значениями в этой области.
- runtime_blocked_hosts
- blocked_install_message
- allowed_types
- runtime_allowed_hosts
- install_sources

Следующие ключи разрешены в отдельной области расширения:

- blocked_permissions
- minimum_version_required
- blocked_install_message
- installation_mode - `"blocked"`, `"allowed"`, `"removed"`, и `"force_installed"``"normal_installed"` являются возможными значениями.
- runtime_allowed_hosts
- update_url
- override_update_url
- runtime_blocked_hosts
- toolbar_state

В области URL-адреса обновления разрешены следующие ключи:

- blocked_permissions
- installation_mode — только `"blocked"`или `"allowed"``"removed"` являются допустимыми значениями в этой области.

## <a name="configure-using-a-json-string-in-windows-group-policy-editor"></a>Настройка строки JSON в редакторе групповой политики Windows

При использовании политики параметров расширения с помощью GPO предполагается, что вы уже импортировали ADM/ADMX для политик Microsoft Edge.

1. Откройте редактор групповой политики и перейдите **к Microsoft Edge > расширениям > настроить политику параметров управления расширениями**.
2. Включите политику и введите ее компактные данные нотации объектов JavaScript (JSON) в текстовом поле в виде одной строки без разрывов строк.
3. Чтобы проверить политику и сжать ее до одной строки, используйте средство сжатия JSON.

### <a name="properly-format-json-for-the-extension-settings-policy"></a>Правильное форматирование JSON для политики параметров расширения

Необходимо понимать две части этой политики: область по умолчанию и отдельная область. Область по умолчанию охватывает все расширения без их собственных областей. Индивидуальная область применяется только к данному расширению.  

Область по умолчанию отмечена звездочкой (*). В следующем примере определяется область по умолчанию и индивидуальная область расширения.

```json
{ 
   “*”: {}, 
   “nckgahadagoaajjgafhacjanaoiihapd”: {} 
} 
```

Расширение получит параметры только одной из областей. Если для расширения существует индивидуальная область расширения, её параметры применяются к данному расширению. Если не существует отдельной области расширения, то расширение будет использовать область по умолчанию.  

Следующий образец JSON запрещает любому расширению запуск `.example.com`, а также блокирует любое расширение, требующее разрешения "USB".

```json
{ 
  "*": { 
    "runtime_blocked_hosts": ["*://*.example.com"], 
    "blocked_permissions": ["usb"] 
  } 
} 
```

**Сжатая JSON**

```json
{"*":{"runtime_blocked_hosts":["*://*.example.com"],"blocked_permissions":["usb"]}} 
```

### <a name="a-few-more-json-examples-for-extension-settings"></a>Еще несколько примеров JSON для параметров расширения

#### <a name="using-installation_mode-property-to-allow-and-block-extensions"></a>Использование свойства installation_mode для разрешения и блокировки расширений

- Пользователь может установить все расширения — параметр по умолчанию

  `{ "*": {"installation_mode": "allowed" }}`
- Пользователь не может устанавливать расширения.  

  `{ "*": {"installation_mode": "blocked" }}`

- Укажите пользовательское сообщение, которое будет отображаться при блокировке установки.

   `{"*": {"blocked_install_message": ["Call IT(408 - 555 - 1234) for an exception"]}}`

#### <a name="using-installation_mode-property-to-force-install-extensions"></a>Использование свойства installation_mode для принудительной установки расширений

При использовании свойства installation_mode как "force_installed" расширение автоматически устанавливается без взаимодействия с пользователем. Пользователь не может выключить или удалить расширение. Если расширение установлено как "normal" или "force", поле ** update_ur** тоже должно быть заполнено. Это поле указывает, откуда можно установить расширение. Используйте следующие расположения для поля **update_url**:

- Если скачиваемые расширения размещены в магазине надстроек Microsoft Edge, используйте [https://edge.microsoft.com/extensionwebstorebase/v1/crx](https://edge.microsoft.com/extensionwebstorebase/v1/crx).
- Если загружаемое расширение размещено в интернет-магазине Chrome, используйте [https://clients2.google.com/service/update2/crx](https://clients2.google.com/service/update2/crx).
- Если расширение размещено на вашем собственном сервере, используйте такой URL-адрес, с которого Microsoft Edge может скачать упакованное расширение (crx-файл). Пример JSON

   `{"nckgahadagoaajjgafhacjanaoiihapd": {"installation_mode": "force_installed","update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"}}`
  
В предыдущем примере при использовании normal_installed вместо force_installed расширение устанавливается автоматически без взаимодействия с пользователем, но оно может быть отключено.  

   > [!TIP]
   > Правильно отформатировать строку JSON может быть сложно. Перед реализацией политики используйте проверку JSON. Или попробуйте раннюю версию [Extension Settings Generator Tool](https://microsoft.github.io/edge-extension-settings-generator/minimal)

## <a name="configure-using-the-windows-registry"></a>Настройка с помощью реестра Windows

Политика ExtensionSettings должна быть записана в этот раздел реестра:

`HKLM\Software\Policies\Microsoft\Edge\`

> [!NOTE]
> Вместо HKLM можно использовать HKCU. Эквивалентный путь можно настроить с помощью объекта групповой политики (GPO).  

Для Microsoft Edge все параметры будут запускаться в этом разделе:

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\`

Следующий раздел, который следует создать, — это либо ID расширения для индивидуальной области, либо звездочка (*) для области по умолчанию. Например, для параметров, применимых к Google Hangouts, в реестре используется следующее расположение:

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\nckgahadagoaajjgafhacjanaoiihapd`

Для параметров, которые применяются к области по умолчанию (звездочка), используйте следующее расположение в реестре:

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\*`

Для различных параметров требуются различные форматы, в зависимости от того, являются ли они строкой или массивом строк. Значения массива требуют формата [＂значение＂]. Строки могут быть введены без изменений. В следующем списке показано, какие параметры являются массивами или строками:

- nstallation_mode = Строка
- update_url = Строка
- blocked_permissions = Массив строк
- allowed_permissions = Массив строк
- minimum_version_required = Строка
- runtime_blocked_hosts = Массив строк
- runtime_allowed_hosts = Массив строк
- blocked_install_message = Строка


## <a name="see-also"></a>См. также

- [Управление расширениями Microsoft Edge на предприятии](microsoft-edge-manage-extensions.md)
- [Использование групповых политик для управления расширениями Microsoft Edge](microsoft-edge-manage-extensions-policies.md)
- [Часто задаваемые вопросы о расширениях Microsoft Edge](microsoft-edge-manage-extensions-faq.md)
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
