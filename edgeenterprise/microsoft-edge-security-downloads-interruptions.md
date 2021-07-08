---
title: Прерывание скачивания потенциально опасных файлов
ms.author: kvice
author: AndreaLBarr
manager: srugh
ms.date: 05/20/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Прерывание скачивания потенциально опасных файлов
ms.openlocfilehash: 6239fd766c9e10d070188133a84ec0d7ce42a882
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618258"
---
# <a name="interrupting-downloads-of-potentially-dangerous-files"></a>Прерывание скачивания потенциально опасных файлов

Компонент политик типов файлов Microsoft Edge позволяет классифицировать файлы по уровню опасности, чтобы безвредные файлы (например, файлы `.txt`) можно было беспрепятственно скачать, а потенциально опасные файлы (например, файлы `.dll`) подвергнуть более тщательной проверке и проявить большую бдительность при их использовании.

## <a name="determining-the-danger-level-of-a-file-type"></a>Определение уровня опасности типа файла

Microsoft Edge наследует политики типов файлов от вышестоящего браузера Chromium. Текущее содержимое списка можно просмотреть [здесь](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb). В списке вы увидите, что каждый тип имеет свойство danger_level с одним из трех значений: `DANGEROUS`, `NOT_DANGEROUS` или `ALLOW_ON_USER_GESTURE`.

Первые два простые: **NOT_DANGEROUS** означает, что файл можно безопасно скачать, даже если скачивание является случайным. **DANGEROUS** означает, что браузер всегда должен предупреждать пользователя о том, что скачивание может нанести вред устройству.

Третий параметр, **ALLOW_ON_USER_GESTURE**, более сложный. Такие файлы потенциально опасны, но, скорее всего, окажутся безвредными, если пользователь запросил скачивание. Microsoft Edge позволит автоматически продолжить такое скачивание, если выполняются два условия:

1. Наличие [жеста пользователя](https://textslashplain.com/2020/05/18/browser-basics-user-gestures/), связанного с сетевым запросом, который инициировал скачивание (например, пользователь щелкнул ссылку на скачиваемый файл).
2. Наличие зафиксированного посещения ссылающегося источника (страница со ссылкой на скачиваемый файл) до последней полуночи (например, вчера или ранее). Это подразумевает наличие истории посещений сайта пользователем.

Скачивание также будет автоматически продолжено, если пользователь явно инициировал его с помощью команды контекстного меню **Сохранить ссылку как**, ввел URL-адрес скачиваемого файла непосредственно в адресную строку браузера или если фильтр SmartScreen в Microsoft Defender показал, что файл является безопасным.

**Обновление.** Начиная с версии 91, Microsoft Edge будет прерывать скачивание в случае отсутствия требуемого жеста.

## <a name="user-experience-for-downloads-lacking-gestures"></a>Пользовательский интерфейс для скачивания без жестов

Если скачивание потенциально опасного типа файлов начинается без требуемого жеста, Microsoft Edge сообщает, что скачивание "заблокировано". Команды с именем `Keep` и `Delete` доступны в … меню для скачиваемого элемента, чтобы пользователь мог продолжить или отменить скачивание.

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/Dowload-was-blocked.png" alt-text="Скачивание заблокировано":::

На странице `edge://downloads` пользователь увидит те же параметры:

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/msg-keep-delete-option.png" alt-text="Параметр удаления/сохранения MSG-файлов":::

## <a name="enterprise-controls"></a>Элементы управления для предприятия

Хотя пользователи вряд ли столкнутся с прерыванием скачивания на сайтах, которые они используют каждый день, это может произойти при законном скачивании на редко используемых сайтах. Чтобы упростить пользовательский интерфейс для предприятий, можно использовать групповую политику.

Предприятия могут использовать политику [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) для указания типов файлов, которые разрешено скачивать с определенных сайтов без прерывания. Например, следующая политика позволяет скачивать без прерывания XML-файлы с сайтов contoso.com и woodgrovebank.com, а также MSG-файлы с любого сайта.

`[{"file_extension":"xml","domains":["contoso.com", "woodgrovebank.com"]},
{"file_extension":"msg", "domains": ["*"]}]`

## <a name="file-types-requiring-a-gesture"></a>Типы файлов, требующие жеста

Последние [политики типов файлов](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb) публикуются в исходном коде Chromium. На май 2021 г. типы файлов с `danger_level` из `ALLOW_ON_USER_GESTURE` по крайней мере на одной платформе ОС включают:
`crx, pl, py, pyc, pyo, pyw, rb, efi, oxt, msi, msp, mst, ade, adp, mad, maf, mag, mam, maq, mar, mas, mat, mav, maw, mda, mdb, mde, mdt, mdw, mdz, accdb, accde, accdr, accda, ocx, ops, paf, pcd, pif, plg, prf, prg, pst, cpi, partial, xrm-ms, rels, svg, xml, xsl, xsd, ps1, ps1xml, ps2, ps2xml, psc1, psc2, js, jse, vb, vbe, vbs, vbscript, ws, wsc, wsf, wsh, msh, msh1, msh2, mshxml, msh1xml, msh2xml, ad, app, application, appref-ms, asp, asx, bas, bat, chi, chm, cmd, com, cpl, crt, cer, der, eml, exe, fon, fxp, hlp, htt, inf, ins, inx, isu, isp, job, lnk, mau, mht, mhtml, mmc, msc, msg, reg, rgs, scr, sct, search-ms, settingcontent-ms, shb, shs, slk, u3p, vdx, vsx, vtx, vsdx, vssx, vstx, vsdm, vssm, vstm, vsd, vsmacros, vss, vst, vsw, xnk, cdr, dart, dc42, diskcopy42, dmg, dmgpart, dvdr, dylib, img, imgpart, ndif, service, smi, sparsebundle, sparseimage, toast, udif, action, definition, wflow, caction, as, cpgz, command, mpkg, pax, workflow, xip, mobileconfig, configprofile, internetconnect, networkconnect, pkg, deb, pet, pup, rpm, slp, out, run, bash, csh, ksh, sh, shar, tcsh, desktop, dex,apk`

## <a name="danger-level-may-vary-by-operating-system"></a>Уровень опасности зависит от операционной системы

Параметры типа файлов иногда различаются в зависимости от платформы клиентской ОС. Например, `.exe` не опасен на компьютере Mac, а `.applescript` безвреден в Windows.
