---
title: Настройка Microsoft Edge с помощью средств управления мобильными устройствами
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Настройка Microsoft Edge с помощью средств управления мобильными устройствами.
ms.openlocfilehash: 0927d64366652986b87c2f517ca8ebafd4c9ac55
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641655"
---
# <a name="configure-microsoft-edge-using-mobile-device-management"></a>Настройка Microsoft Edge с помощью средств управления мобильными устройствами

В этой статье приводятся инструкции по настройке Microsoft Edge в Windows 10 с помощью [Средств управления мобильными устройствами (MDM)](/windows/client-management/mdm/) посредством [приема ADMX-файла](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration). Также в этой статье:

- Создание [универсального кода ресурса открытого сообщества производителей мобильной связи (OMA-URI) для политик Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).
- Настройка [Microsoft Edge в Intune с помощью приема ADMX-файла и настраиваемого кода OMA-URI](#configure-microsoft-edge-in-intune-using-admx-ingestion).

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## <a name="prerequisites"></a>Что вам понадобится

Windows 10 со следующими минимальными системными требованиями:

- Windows 10, версия 1903 с установленными обновлениями [KB4512941](https://support.microsoft.com/help/4512941/) и [KB4517211](https://support.microsoft.com/help/4517211/)
- Windows 10, версия 1809 с установленными обновлениями [KB4512534](https://support.microsoft.com/help/4512534/) и [KB4520062](https://support.microsoft.com/help/4520062/)
- Windows 10, версия 1803 с установленными обновлениями [KB4512509](https://support.microsoft.com/help/4512509/) и [KB4519978](https://support.microsoft.com/help/4519978)
- Windows 10, версия 1709 с установленными обновлениями [KB4516071](https://support.microsoft.com/help/4516071/) и [KB4520006](https://support.microsoft.com/help/4520006)

## <a name="overview"></a>Обзор

Вы можете настроить Microsoft Edge в Windows 10 с помощью MDM с предпочтительным поставщиком средств управления корпоративной мобильной средой (EMM) или MDM, поддерживающим [примем ADMX-файлов](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).

Настройка Microsoft Edge с помощью MDM выполняется в два этапа.

1. Прием ADMX-файла Microsoft Edge поставщиком EMM или MDM. Инструкции по приему ADMX-файлов см. в документации вашего поставщика.

   > [!NOTE]
   > Инструкции для Microsoft Intune см. в разделе [Настройка Microsoft Edge в Intune с помощью приема ADMX-файла](#configure-microsoft-edge-in-intune-using-admx-ingestion).

2. [Создание кода OMA-URI для политики Microsoft Edge](#create-an-oma-uri-for-microsoft-edge-policies).

## <a name="create-an-oma-uri-for-microsoft-edge-policies"></a>Создание кода OMA-URI для политик Microsoft Edge

В следующих разделах приведены инструкции по созданию пути OMA-URI, а также поиску и определению значения в формате XML для обязательных и рекомендуемых политик браузера.

Прежде чем приступить к работе, скачайте файл шаблонов политики Microsoft Edge (MicrosoftEdgePolicyTemplates.cab) на [целевой странице Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise) и извлеките содержимое.

Определение кода OMA-URI выполняется в три этапа.

1. [Создание пути OMA-URI](#create-the-oma-uri-path)
2. [Указание базы данных OMA-URI](#specify-the-data-type)
3. [Установка значения OMA-URI](#set-the-value-for-a-browser-policy)

### <a name="create-the-oma-uri-path"></a>Создание пути OMA-URI

Используйте следующую формулу в качестве руководства по созданию путей OMA-URI. <br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`* <br/><br/>

| Параметр         | Описание                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| \<ADMXIngestName> | Используйте имя "Edge" или имя, выбранное вами во время приема административного шаблона. Например, если вы использовали "./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx", то используйте "MicrosoftEdge".<br/><br/> Имя `<ADMXIngestionName>` должно совпадать с именем, использованным при приеме ADMX-файла. |
| \<ADMXNamespace>  | "microsoft_edge" или "microsoft_edge_recommended" в зависимости от того, какая политика задается — обязательная или рекомендуемая. |
| \<ADMXCategory>   | Параметр "parentCategory" политики определяется в ADMX-файле. Пропустите `<ADMXCategory>`, если политика не сгруппирована (не определена категория "parentCategory"). |
| \<PolicyName>     | Имя политики можно найти в статье [Справочник по политикам браузера](./microsoft-edge-policies.md). |

#### <a name="uri-path-example"></a>Пример пути URI:

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

### <a name="specify-the-data-type"></a>Указание базы данных

Типом данных OMA-URI всегда является "String" (строка).

### <a name="set-the-value-for-a-browser-policy"></a>Установка значения для политики браузера

В этом разделе описывается, как задать значение в формате XML для каждого типа данных. Перейдите в [Справочник по политикам браузера](./microsoft-edge-policies.md), чтобы найти тип данных политики.

> [!NOTE]
> Для нелогических типов данных значение всегда начинается с `<enabled/>`.

#### <a name="boolean-data-type"></a>Логический тип данных

Для политик с логическим типом данных используйте `<enabled/>` или `<disabled/>`.

#### <a name="integer-data-type"></a>Целочисленные типы данных

Значение всегда должно начинаться с элемента `<enabled/>`, за которым следует `<data id="[valueName]" value="[decimal value]"/>`.

Чтобы найти имя значения и десятичное значение для страницы новой вкладки, выполните следующие действия.

1. Откройте файл **msedge.admx** в любом XML-редакторе.
2. Найдите элемент `<policy>`, где имя атрибута совпадает с именем политики, которую вы хотите настроить. Для "RestoreOnStartup" выполните поиск по запросу `name="RestoreOnStartup"`.
3. В узле `<elements>` найдите значение, которое требуется задать.
4. Используйте значение из атрибута "valueName" в узле `<elements>`. Для "RestoreOnStartup" именем значения "valueName" будет "RestoreOnStartup".
5. Используйте значение из атрибута "value" в узле `<decimal>`. Чтобы параметр "RestoreOnStartup" открывал новую вкладку, значением должно быть "5".

Чтобы при запуске открывалась страница с новой вкладкой, используйте следующее:<br>
`<enabled/> <data id="RestoreOnStartup" value="5"/>`

#### <a name="list-of-strings-data-type"></a>Список строковых типов данных

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

#### <a name="dictionary-or-string-data-type"></a>Словарный или строчный тип данных

Значение всегда должно начинаться с элемента `<enabled/>`, за которым следует `<data id="[textID]" value="[string]"/>`.

Чтобы найти код textID и задать значение, настройте языковой стандарт, выполнив следующие действия.

1. Откройте файл **msedge.admx** в любом XML-редакторе.
2. Найдите элемент `<policy>`, где имя атрибута совпадает с именем политики, которую вы хотите настроить. Для "ApplicationLocaleValue" выполните поиск по запросу `name="ApplicationLocaleValue"`.
3. Используйте значение в атрибуте "id" узла `<text>` для `[textID]`.
4. Значение значению "value" языковой стандарт.

Чтобы задать языковой стандарт "es-US" с помощью политики "ApplicationLocaleValue", выполните следующие действия.<br>
`<enabled/> <data id="ApplicationLocaleValue" value="es-US"/>`

### <a name="create-the-oma-uri-for-a-recommended-policies"></a>Создайте OMA-URI для рекомендуемых политик

Определение пути URI для рекомендуемых политик зависит от политики, которую вы хотите настроить.

#### <a name="to-define-the-uri-path-for-a-recommended-policy"></a>Определение пути URI для рекомендуемой политики

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

#### <a name="oma-uri-path-examples-for-recommended-policies"></a>Примеры путей OMA-URI для рекомендуемых политик

В следующей таблице приведены примеры путей OMA-URI для рекомендуемых политик.

|              Политика               |             OMA-URI                      |
|-----------------------------------|------------------------------------------|
| [RegisteredProtocolHandlers](./microsoft-edge-policies.md#registeredprotocolhandlers)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~ContentSettings_recommended/RegisteredProtocolHandlers_recommended`                        |
| [PasswordManagerEnabled](./microsoft-edge-policies.md#passwordmanagerenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~PasswordManager_recommended/PasswordManagerEnabled_recommended`                        |
| [PrintHeaderFooter](./microsoft-edge-policies.md#printheaderfooter)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Printing_recommended/PrintHeaderFooter_recommended`                        |
| [SmartScreenEnabled](./microsoft-edge-policies.md#smartscreenenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~SmartScreen_recommended/SmartScreenEnabled_recommended`                        |
| [HomePageLocation](./microsoft-edge-policies.md#homepagelocation)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/HomepageLocation_recommended`                        |
| [ShowHomeButton](./microsoft-edge-policies.md#showhomebutton)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/ShowHomeButton_recommended`                        |
| [FavoritesBarEnabled](./microsoft-edge-policies.md#favoritesbarenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~/FavoritesBarEnabled_recommended`                        |

### <a name="oma-uri-examples"></a>Примеры OMA-URI

Примеры OMA-URI с путем URI, типом и возможным значением.

#### <a name="boolean-data-type-examples"></a>Примеры логических типов данных

*[ShowHomeButton](./microsoft-edge-policies.md#showhomebutton):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: ShowHomeButton                                                       |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton` |
| Тип    | String (строка)                                                                               |
| Значение   | `<enabled/>`                                                                          |

*[DefaultSearchProviderEnabled](./microsoft-edge-policies.md#defaultsearchproviderenabled):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: DefaultSearchProviderEnabled                                         |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~DefaultSearchProvider/DefaultSearchProviderEnabled`    |
| Тип    | String (строка)                                                                               |
| Значение   | `<disable/>`                                                                          |

### <a name="integer-data-type-examples"></a>Примеры целочисленных типов данных

*[AutoImportAtFirstRun](./microsoft-edge-policies.md#autoimportatfirstrun):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: AutoImportAtFirstRun                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/AutoImportAtFirstRun`   |
| Тип    | String (строка)                                                                               |
| Значение   | `<enabled/><data id="AutoImportAtFirstRun" value="1"/>`                             |

*[DefaultImagesSetting](./microsoft-edge-policies.md#defaultimagessetting):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: DefaultImagesSetting                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/DefaultImagesSetting`    |
| Тип    | String (строка)                                                                               |
| Значение   | `<enabled/><data id="DefaultImagesSetting" value="2"/>`                             |

*[DiskCacheSize](./microsoft-edge-policies.md#diskcachesize):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: DiskCacheSize                                                        |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`        |
| Тип    | String (строка)                                                                               |
| Значение   | `<enabled/><data id="DiskCacheSize" value="1000000"/>`                               |

#### <a name="list-of-strings-data-type-examples"></a>Список примеров строковых типов данных
<!--
*[NotificationsAllowedForUrls](./microsoft-edge-policies.md#NotificationsAllowedForUrls):*

| Field   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: NotificationsAllowedForUrls                                          |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/NotificationsAllowedForUrls`    |
| Type    | String                                                                               |
| Value   | `<enabled/><data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com"/>`<br>For multiple list items: `<data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com;[*.]contoso.edu"/>`                           |
-->
*[RestoreOnStartupURLS](./microsoft-edge-policies.md#restoreonstartupurls):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: RestoreOnStartupURLS                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/RestoreOnStartupURLs`    |
| Тип    | String (строка)                                                                               |
| Значение   | `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com"/>`<br>Для нескольких элементов списка: `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com&#xF000;2&#xF000;http://www.microsoft.com"/>`  |

*[ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: ExtensionInstallForcelist                                            |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`    |
| Тип    | String (строка)                                                                               |
| Значение   | `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000;gbchcmhmhahfdphkhkmpfmihenigjmpp;https://extensionwebstorebase.edgesv.net/v1/crx"/>`                               |

#### <a name="dictionary-and-string-data-type-example"></a>Пример словарных или строчных типов данных

*[ProxyMode](./microsoft-edge-policies.md#proxymode):*

| Поле   | Значение                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Имя    | Microsoft Edge: ProxyMode                                                            |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ProxyMode/ProxyMode`  |
| Тип    | String (строка)                                                                               |
| Значение   | `<enabled/><data id="ProxyMode" value="auto_detect"/>`                               |

## <a name="configure-microsoft-edge-in-intune-using-admx-ingestion"></a>Настройка Microsoft Edge в Intune с помощью приема ADMX-файла

Для настройки Microsoft Edge с помощью Microsoft Intune рекомендуется использовать профиль "Административные шаблоны", как описано в разделе [Настройка параметров политики Microsoft Edge с помощью Microsoft Intune](./configure-edge-with-intune.md). Если вы хотите оценить политику, которая в данный момент недоступна в административных шаблонах Microsoft Edge, вы можете настроить Microsoft Edge в Intune, используя [пользовательские параметры для устройств с Windows 10 в Intune](/intune/configuration/custom-settings-windows-10).

В этом разделе приведены следующие инструкции:

1. [Прием ADMX-файла Microsoft Edge в Intune](#ingest-the-microsoft-edge-admx-file-into-intune)
2. [Установка политики с помощью настраиваемого кода OMA-URI в Intune](#set-a-policy-using-custom-oma-uri-in-intune)

> [!IMPORTANT]
> Для настройки одного и того же параметра Microsoft Edge в Intune не рекомендуется использовать пользовательский профиль OMA-URI и профиль административных шаблонов. Если вы развертываете одну и ту же политику, используя пользовательский OMA-URI и профиль административного шаблона, но с разными значениями, пользователи получат непредсказуемые результаты. Мы настоятельно рекомендуем удалить профиль OMA-URI перед использованием профиля административных шаблонов.

### <a name="ingest-the-microsoft-edge-admx-file-into-intune"></a>Прием ADMX-файла Microsoft Edge в Intune

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
### <a name="set-a-policy-using-custom-oma-uri-in-intune"></a>Установка политики с помощью настраиваемого кода OMA-URI в Intune

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

После создания профиля и установки свойств необходимо [назначить профиль в Microsoft Intune](/intune/configuration/device-profile-assign).

#### <a name="confirm-that-the-policy-was-set"></a>Убедитесь, что политика настроена

Выполните следующие действия, чтобы убедиться в том, что политика Microsoft Edge использует созданный вами профиль. (Подождите, пока Microsoft Intune распространит политику на устройство, назначенное в примере профиля "Microsoft Edge ADMX ingested configuration".)

1. Откройте Microsoft Edge и перейдите по адресу *edge://policy*.
2. На странице **Политики** проверьте, указана ли политика, заданная в профиле.
3. Если политика не отображается, см. раздел [Диагностика ошибок MDM в Windows 10](/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) или [Устранение неполадок с параметром политики](#troubleshoot-a-policy-setting).

#### <a name="troubleshoot-a-policy-setting"></a>Устранение неполадок с параметром политики

Если политика Microsoft Edge не вступает в силу, попробуйте выполнить следующие действия.

Откройте страницу *edge://policy* на целевом устройстве (устройство, которому назначен профиль в Microsoft Intune) и найдите политику. Если политики нет на странице *edge://policy*, попробуйте выполнить следующие действия.

- Убедитесь, что политика находится в реестре и является правильной. На целевом устройстве откройте редактор реестра Windows 10 (клавиша **Windows + R**, введите "*regedit*" и нажмите клавишу **Ввод**). Проверьте, правильно ли задана политика в разделе *\Software\Policies\ Microsoft\Edge*. Если вы не нашли политику в ожидаемом разделе, это значит, что политика была неправильно отправлена на устройство.
- Убедитесь, что путь OMA-URI правильный, а значение является допустимой строкой XML. Если одно из этих условий не выполнено, политика не будет отправлена на целевое устройство.

Дополнительные советы по устранению неполадок см. в разделе [Настройка Microsoft Intune](/intune/fundamentals/setup-steps) и [Синхронизация устройств](/intune/remote-actions/device-sync).

## <a name="see-also"></a>Статьи по теме

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Настройка параметров политики Microsoft Edge с помощью Microsoft Intune](configure-edge-with-intune.md)
- [Управление мобильными устройствами](/windows/client-management/mdm/)
- [Использование настраиваемых параметров для устройств с Windows 10 в Intune](/intune/configuration/custom-settings-windows-10)
- [Настройка политики Win32 и приложения "Мост для классических приложений"](/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)
- [Общие сведения о политиках с поддержкой ADMX](/windows/client-management/mdm/understanding-admx-backed-policies)