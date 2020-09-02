---
title: Настройка Microsoft Edge с помощью средств управления мобильными устройствами
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 10/25/2019
audience: ITPro
ms.topic: technical
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Настройка Microsoft Edge с помощью средств управления мобильными устройствами.
ms.openlocfilehash: dda35199f653b3dfb8f20b33b068c59621222b36
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980837"
---
# Настройка Microsoft Edge с помощью средств управления мобильными устройствами

В этой статье приводятся инструкции по настройке Microsoft Edge в Windows 10 с помощью [Средств управления мобильными устройствами (MDM)](https://docs.microsoft.com/windows/client-management/mdm/) посредством [приема ADMX-файла](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration). Также в этой статье:

- Создание [универсального кода ресурса открытого сообщества производителей мобильной связи (OMA-URI) для политик Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).
- Настройка [Microsoft Edge в Intune с помощью приема ADMX-файла и настраиваемого кода OMA-URI](#configure-microsoft-edge-in-intune-using-admx-ingestion).

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## Что вам понадобится

Windows 10 со следующими минимальными системными требованиями:

- Windows 10, версия 1903 с установленными обновлениями [KB4512941](https://support.microsoft.com/help/4512941/) и [KB4517211](https://support.microsoft.com/help/4517211/)
- Windows 10, версия 1809 с установленными обновлениями [KB4512534](https://support.microsoft.com/help/4512534/) и [KB4520062](https://support.microsoft.com/help/4520062/)
- Windows 10, версия 1803 с установленными обновлениями [KB4512509](https://support.microsoft.com/help/4512509/) и [KB4519978](https://support.microsoft.com/help/4519978)
- Windows 10, версия 1709 с установленными обновлениями [KB4516071](https://support.microsoft.com/help/4516071/) и [KB4520006](https://support.microsoft.com/help/4520006)

## Обзор

Вы можете настроить Microsoft Edge в Windows 10 с помощью MDM с предпочтительным поставщиком средств управления корпоративной мобильной средой (EMM) или MDM, поддерживающим [примем ADMX-файлов](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).

Настройка Microsoft Edge с помощью MDM выполняется в два этапа.

1. Прием ADMX-файла Microsoft Edge поставщиком EMM или MDM. Инструкции по приему ADMX-файлов см. в документации вашего поставщика.

   > [!NOTE]
   > Инструкции для Microsoft Intune см. в разделе [Настройка Microsoft Edge в Intune с помощью приема ADMX-файла](#configure-microsoft-edge-in-intune-using-admx-ingestion).

2. [Создание кода OMA-URI для политики Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).

## Создание кода OMA-URI для политик Microsoft Edge

В следующих разделах приведены инструкции по созданию пути OMA-URI, а также поиску и определению значения в формате XML для обязательных и рекомендуемых политик браузера.

Прежде чем приступить к работе, скачайте файл шаблонов политики Microsoft Edge (MicrosoftEdgePolicyTemplates.cab) на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) и извлеките содержимое.

Определение кода OMA-URI выполняется в три этапа.

1. [Создание пути OMA-URI](#create-the-oma-uri-path)
2. [Указание базы данных OMA-URI](#specify-the-data-type)
3. [Установка значения OMA-URI](#set-the-value-for-a-browser-policy)

### Создание пути OMA-URI

Используйте следующую формулу в качестве руководства по созданию путей OMA-URI. <br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`* <br/><br/>

| Параметр         | Описание                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| \<ADMXIngestName> | Используйте имя "Edge" или имя, выбранное вами во время приема административного шаблона. Например, если вы использовали "./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx", то используйте "MicrosoftEdge".<br/><br/> Имя `<ADMXIngestionName>` должно совпадать с именем, использованным при приеме ADMX-файла. |
| \<ADMXNamespace>  | "microsoft_edge" или "microsoft_edge_recommended" в зависимости от того, какая политика задается — обязательная или рекомендуемая. |
| \<ADMXCategory>   | Параметр "parentCategory" политики определяется в ADMX-файле. Пропустите `<ADMXCategory>`, если политика не сгруппирована (не определена категория "parentCategory"). |
| \<PolicyName>     | Имя политики можно найти в статье [Справочник по политикам браузера](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies). |

#### Пример пути URI:

В этом примере предположим, что узел `<ADMXIngestName>` называется "Edge" и вы настраиваете обязательную политику. Путь URI будет выглядеть следующим образом:<br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~<ADMXCategory>/<PolicyName>`*

Если политика не входит в группу (например, DiskCacheSize), удалите "`~<ADMXCategory>`". Замените `<PolicyName>` на имя политики — DiskCacheSize. Путь URI будет выглядеть следующим образом:<br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`*

Если политика входит в группу, выполните следующие действия.

1. Откройте файл **msedge.admx** в любом XML-редакторе.
2. Найдите имя политики, которую вы хотите настроить. Например, "ExtensionInstallForceList".
3. Используйте значение атрибута *ref* из элемента *parentCategory*. Например, "Extensions" из \<parentCategory ref=" Extensions"/>.
4. Замените `<ADMXCategory>` на значение атрибута *ref* для формирования пути URI. Путь URI будет выглядеть следующим образом:<br/><br/>
*`/Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`*

### Указание базы данных

Типом данных OMA-URI всегда является "String" (строка).

### Установка значения для политики браузера

В этом разделе описывается, как задать значение в формате XML для каждого типа данных. Перейдите в [Справочник по политикам браузера](https://docs.microsoft.com/deployedge/microsoft-edge-policies), чтобы найти тип данных политики.

> [!NOTE]
> Для нелогических типов данных значение всегда начинается с `<enabled/>`.

#### Логический тип данных

Для политик с логическим типом данных используйте `<enabled/>` или `<disabled/>`.

#### Целочисленные типы данных

Значение всегда должно начинаться с элемента `<enabled/>`, за которым следует `<data id="[valueName]" value="[decimal value]"/>`.

Чтобы найти имя значения и десятичное значение для страницы новой вкладки, выполните следующие действия.

1. Откройте файл **msedge.admx** в любом XML-редакторе.
2. Найдите элемент `<policy>`, где имя атрибута совпадает с именем политики, которую вы хотите настроить. Для "RestoreOnStartup" выполните поиск по запросу `name="RestoreOnStartup"`.
3. В узле `<elements>` найдите значение, которое требуется задать.
4. Используйте значение из атрибута "valueName" в узле `<elements>`. Для "RestoreOnStartup" именем значения "valueName" будет "RestoreOnStartup".
5. Используйте значение из атрибута "value" в узле `<decimal>`. Чтобы параметр "RestoreOnStartup" открывал новую вкладку, значением должно быть "5".

Чтобы при запуске открывалась страница с новой вкладкой, используйте следующее:<br>
`<enabled/> <data id="RestoreOnStartup" value="5"/>`

#### Список строковых типов данных

Значение всегда должно начинаться с элемента `<enabled/>`, за которым следует `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`.

> [!NOTE]
> Имя атрибута "id=" не является именем политики, хотя в большинстве случаев оно совпадает с именем политики. Это значение атрибута идентификатора узла \<list>, которое находится в ADMX-файле.

Чтобы найти код listID и задать значение для блокировки URL-адреса, выполните следующие действия.

1. Откройте файл **msedge.admx** в любом XML-редакторе.
2. Найдите элемент `<policy>`, где имя атрибута совпадает с именем политики, которую вы хотите настроить. Для "URLBlocklist" выполните поиск по запросу `name="URLBlocklist"`.
3. Используйте значение в атрибуте "id" узла `<list> node for [listID]`.
4. "Value" — это список URL-адресов, разделенных точкой с запятой (;)

Например, чтобы заблокировать доступ к `contoso.com` и `https://ssl.server.com`, выполните следующие действия.<br>
`<enabled/> <data id=" URLBlocklistDesc" value="contoso.com;https://ssl.server.com"/>`

#### Словарный или строчный тип данных

Значение всегда должно начинаться с элемента `<enabled/>`, за которым следует `<data id="[textID]" value="[string]"/>`.

Чтобы найти код textID и задать значение, настройте языковой стандарт, выполнив следующие действия.

1. Откройте файл **msedge.admx** в любом XML-редакторе.
2. Найдите элемент `<policy>`, где имя атрибута совпадает с именем политики, которую вы хотите настроить. Для "ApplicationLocaleValue" выполните поиск по запросу `name="ApplicationLocaleValue"`.
3. Используйте значение в атрибуте "id" узла `<text>` для `[textID]`.
4. Значение значению "value" языковой стандарт.

Чтобы задать языковой стандарт "es-US" с помощью политики "ApplicationLocaleValue", выполните следующие действия.<br>
`<enabled/> <data id="ApplicationLocaleValue" value="es-US"/>`

### Создайте OMA-URI для рекомендуемых политик

Определение пути URI для рекомендуемых политик зависит от политики, которую вы хотите настроить.

#### Определение пути URI для рекомендуемой политики

Используйте формулу пути URI (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) и выполните следующие действия, чтобы определить путь URI:

1. Откройте файл **msedge.admx** в любом XML-редакторе.
2. Если политика, которую вы хотите настроить, не входит в группу, переходите к шагу 4 и удалите `~<ADMXCategory>` из пути.
3. Если политика, которую вы хотите настроить, входит в группу, выполните следующие действия.

   - Чтобы найти `<ADMXCategory>`, выполните поиск политики, которую нужно задать. При поиске добавьте "_recommended" к имени политики. Например, поиск "RegisteredProtocolHandlers_recommended" даст следующий результат:

        ```xml
         <policy class="Both" displayName="$(string.RegisteredProtocolHandlers)" explainText="$(string.RegisteredProtocolHandlers_Explain)" key="Software\Policies\Microsoft\Edge\Recommended" name="RegisteredProtocolHandlers_recommended" presentation="$(presentation.RegisteredProtocolHandlers)">
           <parentCategory ref="ContentSettings_recommended"/>
           <supportedOn ref="SUPPORTED_WIN7_V77"/>
           <elements>
             <text id="RegisteredProtocolHandlers" maxLength="1000000" valueName="RegisteredProtocolHandlers"/>
           </elements>
         </policy>
        ```

   - Скопируйте значение атрибута *ref* из элемента `<parentCategory>`. Для "ContentSettings" скопируйте "ContentSettings_recommended" из `<parentCategory ref=" ContentSettings_recommended"/>`.
   - Замените `<ADMXCategory>` на значение атрибута *ref* в формуле пути URI для формирования пути URI.

4. `<PolicyName>` — имя политики с добавленным элементом "_recommended".

#### Примеры путей OMA-URI для рекомендуемых политик

В следующей таблице приведены примеры путей OMA-URI для рекомендуемых политик.

|              Политика               |             OMA-URI                      |
|-----------------------------------|------------------------------------------|
| [RegisteredProtocolHandlers](https://docs.microsoft.com/deployedge/microsoft-edge-policies#registeredprotocolhandlers)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~ContentSettings_recommended/RegisteredProtocolHandlers_recommended`                        |
| [PasswordManagerEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#passwordmanagerenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~PasswordManager_recommended/PasswordManagerEnabled_recommended`                        |
| [PrintHeaderFooter](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printheaderfooter)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Printing_recommended/PrintHeaderFooter_recommended`                        |
| [SmartScreenEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreenenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~SmartScreen_recommended/SmartScreenEnabled_recommended`                        |
| [HomePageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/HomepageLocation_recommended`                        |
| [ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/ShowHomeButton_recommended`                        |
| [FavoritesBarEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~/FavoritesBarEnabled_recommended`                        |

### Примеры OMA-URI

Примеры OMA-URI с путем URI, типом и возможным значением.

#### Примеры логических типов данных

*[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ShowHomeButton):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: ShowHomeButton                                                       |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton` |
| Тип    | String (строка)                                                                               |
| Значение   | `<enabled/>`                                                                          |

*[DefaultSearchProviderEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultSearchProviderEnabled):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: DefaultSearchProviderEnabled                                         |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~DefaultSearchProvider/DefaultSearchProviderEnabled`    |
| Тип    | String (строка)                                                                               |
| Значение   | `<disable/>`                                                                          |

### Примеры целочисленных типов данных

*[AutoImportAtFirstRun](https://docs.microsoft.com/deployedge/microsoft-edge-policies#AutoImportAtFirstRun):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: AutoImportAtFirstRun                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/AutoImportAtFirstRun`   |
| Тип    | String (строка)                                                                               |
| Значение   | `<enabled/><data id="AutoImportAtFirstRun" value="1"/>`                             |

*[DefaultImagesSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultImagesSetting):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: DefaultImagesSetting                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/DefaultImagesSetting`    |
| Тип    | String (строка)                                                                               |
| Значение   | `<enabled/><data id="DefaultImagesSetting" value="2"/>`                             |

*[DiskCacheSize](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DiskCacheSize):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: DiskCacheSize                                                        |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`        |
| Тип    | String (строка)                                                                               |
| Значение   | `<enabled/><data id="DiskCacheSize" value="1000000"/>`                               |

#### Список примеров строковых типов данных
<!--
*[NotificationsAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#NotificationsAllowedForUrls):*

| Field   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: NotificationsAllowedForUrls                                          |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/NotificationsAllowedForUrls`    |
| Type    | String                                                                               |
| Value   | `<enabled/><data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com"/>`<br>For multiple list items: `<data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com;[*.]contoso.edu"/>`                               |
-->
*[RestoreOnStartupURLS](https://docs.microsoft.com/deployedge/microsoft-edge-policies#RestoreOnStartupURLS):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: RestoreOnStartupURLS                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/RestoreOnStartupURLs`    |
| Тип    | String (строка)                                                                               |
| Значение   | `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com"/>`<br>Для нескольких элементов списка: `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com&#xF000;2&#xF000;http://www.microsoft.com"/>`  |

*[ExtensionInstallForcelist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ExtensionInstallForcelist):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: ExtensionInstallForcelist                                            |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`    |
| Тип    | String (строка)                                                                               |
| Значение   | `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000;gbchcmhmhahfdphkhkmpfmihenigjmpp;https://extensionwebstorebase.edgesv.net/v1/crx"/>`                               |

#### Пример словарных или строчных типов данных

*[ProxyMode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ProxyMode):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: ProxyMode                                                            |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ProxyMode/ProxyMode`  |
| Тип    | String (строка)                                                                               |
| Значение   | `<enabled/><data id="ProxyMode" value="auto_detect"/>`                               |

## Настройка Microsoft Edge в Intune с помощью приема ADMX-файла

Для настройки Microsoft Edge с помощью Microsoft Intune рекомендуется использовать профиль "Административные шаблоны", как описано в разделе [Настройка параметров политики Microsoft Edge с помощью Microsoft Intune](https://docs.microsoft.com/deployedge/configure-edge-with-intune). Если вы хотите оценить политику, которая в данный момент недоступна в административных шаблонах Microsoft Edge, вы можете настроить Microsoft Edge в Intune, используя [пользовательские параметры для устройств с Windows 10 в Intune](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10).

В этом разделе приведены следующие инструкции:

1. [Прием ADMX-файла Microsoft Edge в Intune](#ingest-the-microsoft-edge-admx-file-into-intune)
2. [Установка политики с помощью настраиваемого кода OMA-URI в Intune](#set-a-policy-using-custom-oma-uri-in-intune)

> [!IMPORTANT]
> Для настройки одного и того же параметра Microsoft Edge в Intune не рекомендуется использовать пользовательский профиль OMA-URI и профиль административных шаблонов. Если вы развертываете одну и ту же политику, используя пользовательский OMA-URI и профиль административного шаблона, но с разными значениями, пользователи получат непредсказуемые результаты. Мы настоятельно рекомендуем удалить профиль OMA-URI перед использованием профиля административных шаблонов.

### Прием ADMX-файла Microsoft Edge в Intune

В этом разделе приведены инструкции по приему административного шаблона Microsoft Edge (файла **msedge.admx**) в Intune.

> [!WARNING]
> Не изменяйте ADMX-файл перед его использованием.

Для приема ADMX-файла выполните следующие действия:

1. Скачайте файл шаблонов политики Microsoft Edge (MicrosoftEdgePolicyTemplates.cab) на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) и извлеките содержимое. Необходимый вам файл — **msedge.admx**.
2. Войдите [на портал Microsoft Azure](https://portal.azure.com).
3. Выберите **Intune** в разделе _Все службы_ или найдите Intune в поле поиска на портале.
4. В колонке _Microsoft Intune — Обзор_ выберите **Конфигурация устройств** | **Профили**.
5. На верхней панели команд выберите **Создать профиль**.

   ![Создание профиля устройства](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile.png)

6. Предоставьте следующую информацию для профиля:

   - **Имя**: введите описательное имя. В этом примере — "Microsoft Edge ADMX ingested configuration" (Конфигурация ADMX, принимаемая Microsoft Edge).
   - **Описание**: введите необязательное описание для профиля.
   - **Платформа**: выберите "Windows 10 и более поздней версии".
   - **Тип профиля**: выберите "Настраиваемый".

7. В разделе **Пользовательские параметры OMA-URI** нажмите кнопку **Добавить**, чтобы добавить возможность приема ADMX-файла.

   ![Добавление возможности приема для OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-add-omauri.png)

8. В поле **Добавить строку** укажите следующие сведения:

   - **Имя**: введите описательное имя. В этом примере используется "Microsoft Edge ADMX ingestion" (Прием ADMX-файла браузером Microsoft Edge).
   - **Описание**: введите необязательное описание для параметра.
   - **OMA-URI**: введите "*./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*"
   - **Тип данных**: выберите "Строка".
   - **Значение**: эта область ввода появляется после выбора пункта **Тип данных**. Откройте файл msedge.admx из файла шаблонов политики Microsoft Edge, извлеченного в ходе шага 1. Скопируйте **ВЕСЬ текст** из файла msedge.admx и вставьте его в текстовое поле **Значение**, показанное на следующем снимке экрана.

        ![Добавление возможности приема ADMX-файла](./media/edge-cfg-with-mdm/configure-edge-intune-mdm-omauri-addrow-ingest.png)

   - Нажмите **ОК**.

9. В колонке **Пользовательские параметры OMA-URI** нажмите **ОК**.
10. В окне **Создание профиля** выберите **Создать**. На следующем снимке экрана представлены сведения о только что созданном профиле.

    ![Сведения в новом профиле устройства ](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-done.png)

<!--
> [!NOTE]
> You can use the preceding steps to ingest the msedgeupate.admx policy template file.
-->
### Установка политики с помощью настраиваемого кода OMA-URI в Intune

> [!NOTE]
> Перед выполнением шагов, описанных в этом разделе, необходимо выполнить действия из раздела [Прием ADMX-файла Microsoft Edge в Intune](#ingest-the-microsoft-edge-admx-file-into-intune).

1. Войдите [на портал Microsoft Azure](https://portal.azure.com).
2. Выберите **Intune** в разделе _Все службы_ или найдите Intune в поле поиска на портале.
3. Перейдите в раздел **Intune**>**Конфигурация устройств**>**Профили**.
4. Выберите профиль "Microsoft Edge ADMX ingested configuration" (Конфигурация ADMX, принимаемая Microsoft Edge) или имя, которое вы использовали для профиля.
5. Чтобы добавить параметры политики Microsoft Edge, необходимо открыть **Пользовательские параметры OMA-URI**. В разделе **Управление** выберите **Свойства**, а затем выберите **Параметры**.

    ![Настройка параметров профиля](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings.png)

6. В разделе **Пользовательские параметры OMA-URI** выберите **Добавить**.

    ![Добавление строки к параметрам OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings-add-row.png)

7. В поле **Добавить строку** укажите следующие сведения:

   - **Имя**: введите описательное имя. Мы рекомендуем использовать имя политики, которую вы хотите настроить. В этом примере используется имя "ShowHomeButton".
   - **Описание**: введите необязательное описание для параметра.
   - **OMA-URI**: введите код OMA-URI для политики. Для политики "ShowHomeButton", используемой в качестве примера, используйте следующую строку: "*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*"
   - **Тип данных**: выберите тип данных параметров политики. Для политики "ShowHomeButton" используйте "String" (строка).
   - **Значение**: введите параметр, который требуется настроить для политики. Для примера "ShowHomeButton" введите "\<enabled/>". На следующем снимке экрана показаны параметры для настройки политики.

        ![Добавление строки, пользовательские параметры OMA-URI](./media/edge-cfg-with-mdm/configure-edge-mdm-custom-omauri-setting.png)

   - Нажмите **ОК**.

8. В колонке **Пользовательские параметры OMA-URI** нажмите **ОК**.
9. В профиле **Microsoft Edge ADMX ingested configuration (Конфигурация ADMX, принимаемая Microsoft Edge) — Свойства**" (или на имени, которое вы использовали) нажмите **Сохранить**.

После создания профиля и установки свойств необходимо [назначить профиль в Microsoft Intune](https://docs.microsoft.com/intune/configuration/device-profile-assign).

#### Убедитесь, что политика настроена

Выполните следующие действия, чтобы убедиться в том, что политика Microsoft Edge использует созданный вами профиль. (Подождите, пока Microsoft Intune распространит политику на устройство, назначенное в примере профиля "Microsoft Edge ADMX ingested configuration".)

1. Откройте Microsoft Edge и перейдите по адресу *edge://policy*.
2. На странице **Политики** проверьте, указана ли политика, заданная в профиле.
3. Если политика не отображается, см. раздел [Диагностика ошибок MDM в Windows 10](https://docs.microsoft.com/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) или [Устранение неполадок с параметром политики](#troubleshoot-a-policy-setting).

#### Устранение неполадок с параметром политики

Если политика Microsoft Edge не вступает в силу, попробуйте выполнить следующие действия.

Откройте страницу *edge://policy* на целевом устройстве (устройство, которому назначен профиль в Microsoft Intune) и найдите политику. Если политики нет на странице *edge://policy*, попробуйте выполнить следующие действия.

- Убедитесь, что политика находится в реестре и является правильной. На целевом устройстве откройте редактор реестра Windows 10 (клавиша **Windows + R**, введите "*regedit*" и нажмите клавишу **Ввод**). Проверьте, правильно ли задана политика в разделе *\Software\Policies\ Microsoft\Edge*. Если вы не нашли политику в ожидаемом разделе, это значит, что политика была неправильно отправлена на устройство.
- Убедитесь, что путь OMA-URI правильный, а значение является допустимой строкой XML. Если одно из этих условий не выполнено, политика не будет отправлена на целевое устройство.

Дополнительные советы по устранению неполадок см. в разделе [Настройка Microsoft Intune](https://docs.microsoft.com/intune/fundamentals/setup-steps) и [Синхронизация устройств](https://docs.microsoft.com/intune/remote-actions/device-sync).

## Статьи по теме

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Настройка параметров политики Microsoft Edge с помощью Microsoft Intune](configure-edge-with-intune.md)
- [Управление мобильными устройствами](https://docs.microsoft.com/windows/client-management/mdm/)
- [Использование настраиваемых параметров для устройств с Windows 10 в Intune](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10)
- [Настройка политики Win32 и приложения "Мост для классических приложений"](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)
- [Общие сведения о политиках с поддержкой ADMX](https://docs.microsoft.com/windows/client-management/mdm/understanding-admx-backed-policies)
