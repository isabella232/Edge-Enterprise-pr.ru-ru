---
title: Определение и прерывание скачивания потенциально опасных файлов
ms.author: kvice
author: AndreaLBarr
manager: srugh
ms.date: 01/10/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Понять, Microsoft Edge определяет и прерывает загрузки потенциально опасных файлов
ms.openlocfilehash: 436c85248ef4012d75a9786c36e8f48d53f720d1
ms.sourcegitcommit: e7f3098d8b7d91cae20b5778a71a87daababc312
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2022
ms.locfileid: "12298197"
---
# <a name="identify-and-interrupt-downloads-of-potentially-dangerous-files"></a>Определение и прерывание скачивания потенциально опасных файлов

Microsoft Edge типа файлов классифицирует файлы по уровню "опасности" для управления загрузкой файлов. Безобидный файл (например, файл) можно скачать свободно, а потенциально опасный файл, например, подвергается более высокой степени `.txt` `.dll` проверки. Это тщательное изучение обеспечивает более тщательное пользовательское впечатление.

## <a name="how-microsoft-edge-determines-the-danger-level-of-a-file-type"></a>Определение Microsoft Edge уровня опасности типа файла

Microsoft Edge наследует политики типа файлов из Chromium браузера. Эти типы файлов и их классификацию можно просмотреть в [download_file_types.asciipb.](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb;drc=af17ad3f07c1d8a24381eb7669bec0c2ffb86521) В этом файле вы увидите, что каждый тип имеет **danger_level,** которое является одним из трех значений: `DANGEROUS` , , или `NOT_DANGEROUS` `ALLOW_ON_USER_GESTURE` .

Следующие две классификации просты:

- **NOT_DANGEROUS** означает, что файл является безопасным для скачивания, даже если запрос на скачивание был случайным.
- **DANGEROUS** означает, что браузер всегда должен предупреждать пользователя о том, что скачивание может нанести вред устройству.

Третий параметр, **ALLOW_ON_USER_GESTURE** более тонкий. Эти файлы потенциально опасны, но, скорее всего, безвредны, если пользователь запрашивает скачивание. Microsoft Edge эти загрузки будут автоматически продолжены, если одно из следующих условий будет выполнены:

- Существует жест [пользователя, связанный](https://textslashplain.com/2020/05/18/browser-basics-user-gestures/) с сетевым запросом, который начал скачивать. Например, пользователь щелкнул ссылку на скачивание.
- До последней полуночи (то есть вчера или ранее) записи зафиксировали предварительное посещение ссылаемого источника (страницы, ссылаясь на скачивание). Этот записанный визит означает, что пользователь имеет историю посещения сайта.

Загрузка также будет продолжаться автоматически, если пользователь явно **** запускает ее с помощью ссылки Сохранить в качестве команды меню контекста, вводит URL-адрес загрузки непосредственно в адресную планку браузера, или если фильтр SmartScreen в Microsoft Defender указывает, что файл является безопасным.

> [!NOTE]
> Начиная с версии 91, Microsoft Edge прерывает загрузки, не требуемые жесты.

## <a name="user-experience-for-downloads-that-lack-a-gesture"></a>Пользовательский интерфейс для скачивания без жеста

Если загрузка потенциально опасного типа начинается без требуемого жеста, Microsoft Edge заявляет, что загрузка "была заблокирована". Команды с `Keep` именем `Delete` и доступны из **...** (ellipsis) параметр на элементе загрузки, чтобы позволить пользователю продолжить или отменить скачивание.

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/Dowload-was-blocked.png" alt-text="Загрузка заблокирована, пользователь может сохранить или удалить скачивание.":::

На странице пользователь увидит те же `edge://downloads` параметры. На следующем скриншоте показаны и примеры этих параметров.

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/msg-keep-delete-option.png" alt-text="Загрузка заблокирована, но пользователь может сохранить или удалить скачивание.":::

## <a name="enterprise-controls-for-downloads"></a>Enterprise для скачивания

Хотя пользователи вряд ли столкнутся с прерыванием скачивания на сайтах, которые они используют каждый день, это может произойти при законном скачивании на редко используемых сайтах. Чтобы упростить пользовательский интерфейс для предприятий, можно использовать групповую политику.

Предприятия могут использовать политику [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) для указания типов файлов, которые разрешено скачивать с определенных сайтов без прерывания. Например, следующая политика позволяет скачивать XML-файлы с contoso.com и woodgrovebank.com, а файлы MSG скачивать с любого сайта.

`[{"file_extension":"xml","domains":["contoso.com", "woodgrovebank.com"]},
{"file_extension":"msg", "domains": ["*"]}]`

## <a name="file-types-requiring-a-gesture"></a>Типы файлов, требующие жеста

Последние [политики типов файлов](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb;drc=af17ad3f07c1d8a24381eb7669bec0c2ffb86521) публикуются в исходном коде Chromium. На май 2021 г. типы файлов с `danger_level` из `ALLOW_ON_USER_GESTURE` по крайней мере на одной платформе ОС включают:
`crx, pl, py, pyc, pyo, pyw, rb, efi, oxt, msi, msp, mst, ade, adp, mad, maf, mag, mam, maq, mar, mas, mat, mav, maw, mda, mdb, mde, mdt, mdw, mdz, accdb, accde, accdr, accda, ocx, ops, paf, pcd, pif, plg, prf, prg, pst, cpi, partial, xrm-ms, rels, svg, xml, xsl, xsd, ps1, ps1xml, ps2, ps2xml, psc1, psc2, js, jse, vb, vbe, vbs, vbscript, ws, wsc, wsf, wsh, msh, msh1, msh2, mshxml, msh1xml, msh2xml, ad, app, application, appref-ms, asp, asx, bas, bat, chi, chm, cmd, com, cpl, crt, cer, der, eml, exe, fon, fxp, hlp, htt, inf, ins, inx, isu, isp, job, lnk, mau, mht, mhtml, mmc, msc, msg, reg, rgs, scr, sct, search-ms, settingcontent-ms, shb, shs, slk, u3p, vdx, vsx, vtx, vsdx, vssx, vstx, vsdm, vssm, vstm, vsd, vsmacros, vss, vst, vsw, xnk, cdr, dart, dc42, diskcopy42, dmg, dmgpart, dvdr, dylib, img, imgpart, ndif, service, smi, sparsebundle, sparseimage, toast, udif, action, definition, wflow, caction, as, cpgz, command, mpkg, pax, workflow, xip, mobileconfig, configprofile, internetconnect, networkconnect, pkg, deb, pet, pup, rpm, slp, out, run, bash, csh, ksh, sh, shar, tcsh, desktop, dex,apk`

## <a name="the-file-type-danger-level-may-vary-by-operating-system"></a>Уровень опасности типа файла может варьироваться в зависимости от операционной системы

Параметры типа файлов иногда различаются в зависимости от платформы клиентской ОС. Например, на Mac файл не опасен, а на `.exe` `.applescript` Windows.
