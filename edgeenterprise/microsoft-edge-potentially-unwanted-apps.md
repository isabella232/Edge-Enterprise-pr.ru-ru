---
title: Использование Microsoft Edge для защиты от потенциально нежелательных приложений
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 03/04/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Использование Microsoft Edge для защиты от потенциально нежелательных приложений
ms.openlocfilehash: 615442acc0e9ed58da37aa0ef8b3747e916a8024
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980815"
---
# Защита от потенциально нежелательных приложений (ПНП)

В этой статье объясняется, как защититься от потенциально нежелательных приложений (ПНП) с помощью Microsoft Edge или с помощью антивирусной программы в Microsoft Defender.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 80 или более поздней.

## Обзор

Потенциально нежелательные приложения не считаются вирусами или вредоносными программами, но могут выполнять действия, которые негативно влияют на использование и производительность конечных точек. Например, *программное обеспечение Evasion* пытается скрыться от обнаружения в продуктах обеспечения безопасности. Такое программное обеспечение повышает риск заражения вашей сети реальными вредоносными программами. К потенциально нежелательным приложениям также относятся приложения с плохой репутацией.

Описание условий, применяемых для классификации программного обеспечения в качестве ПНП, см. в статье [Потенциально нежелательные приложения](https://docs.microsoft.com/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua).

## Защита от ПНП с Microsoft Edge

В Microsoft Edge (версии 80.0.361.50 или более поздней) загрузки ПНП и связанные с ними URL-адреса ресурсов блокируются.

Вы можете настроить защиту, включив функцию **Блокировка потенциально опасных приложений** в Microsoft Edge.

> [!NOTE]
> В [своем блоге группа Microsoft Edge](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/) описывает эту функцию, и объясняет, как обрабатывать приложения с ошибками и сообщать о нежелательной программе.

### Включение защиты от ПНП:

1. Откройте **Параметры** в браузере.
2. Выберите **Конфиденциальность и службы**.
3. Убедитесь, что в разделе **Службы** включен **фильтр SmartScreen в Microsoft Defender**. Включите фильтр SmartScreen в Microsoft Defender, если это не так. На снимке экрана ниже показано, что браузер управляется организацией, а фильтр SmartScreen в Microsoft Defender включен.

   ![Включение ПНП Microsoft Edge в параметрах](./media/microsoft-edge-potentially-unwanted-apps/security-pua-setup.png)

4. В разделе **Службы** используйте переключатель, показанный на предыдущем снимке экрана, чтобы включить **Блокировку потенциально опасных приложений**.

   > [!TIP]
   > Функцию блокировки URL-адресов защиты от ПНП можно использовать, проверив ее на одной из [демонстрационных страниц](https://demo.smartscreen.msft.net/) SmartScreen в Microsoft Defender.

Когда Microsoft Edge обнаружит ПНП, появится сообщение со снимка экрана ниже.

   ![Предупреждающее сообщение ПНП Microsoft Edge](./media/microsoft-edge-potentially-unwanted-apps/security-pua-msg.png)

### Блокировка URL-адресов, связанных с ПНП

После включения ПНП защиты в Microsoft Edge, SmartScreen в Microsoft Defender защитит вас от связанных с ПНП URL-адресов.

Администраторы могут настроить способы совместной работы Microsoft Edge и SmartScreen защитника Windows несколькими способами, чтобы защитить пользователей от связанных с ПНП URL-адресов. Дополнительные сведения см. в следующих разделах:

- [Настройка параметров политик Microsoft Edge в Windows](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge)
- [Параметры SmartScreen](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreen-settings)
- [Политика SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled)
- [Настройка фильтра SmartScreen Защитника Windows](https://docs.microsoft.com/microsoft-edge/deploy/available-policies?source=docs#configure-windows-defender-smartscreen)

Администраторы могут настраивать список блокировок Advanced Threat Protection в Microsoft Defender (ATP в Microsoft Defender). С помощью портала ATP в Microsoft Defender можно [создавать индикаторы для IP и URL-адресов, а также управлять ими](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview).

## Защита от ПНП с помощью антивирусной программы в Microsoft Defender

Статья [Обнаружение и блокировка потенциально нежелательных приложений](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus) содержит сведения о том, как настроить антивирусную программу "Защитник Windows" для включения защиты от ПНП. Настроить защиту можно с помощью следующих параметров:

- [Microsoft Intune](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-intune-to-configure-pua-protection)
- [Microsoft Endpoint Configuration Manager](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-configuration-manager-to-configure-pua-protection)
- [Групповая политика](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-group-policy-to-configure-pua-protection)
- [Командлеты PowerShell](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection)

Когда защитник Windows обнаруживает файл ПНП на конечной точке, он помещает его в карантин и уведомляет пользователя ([если уведомления не отключены](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus)), как при обычном обнаружение угроз (с приставкой "ПНП:"). Обнаруженные угрозы также появляются в [списке карантина в приложении "Безопасность Windows"](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history).

### Уведомления и события ПНП

Администратор может просматривать события ПНП несколькими способами:

- В средстве просмотра событий Windows, но не в Microsoft Endpoint Configuration Manager или Intune.
- В сообщении электронной почты, если включены уведомления об обнаружении ПНП.
- В журнале событий [антивирусной программы в Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus), где события ПНП записываются с идентификатором событий 1116, с сообщением: "Платформа защиты от вредоносных программ обнаружила вредоносную или другую потенциально нежелательную программу."

> [!NOTE]
> Пользователи увидят, что приложение "*.exe заблокировано фильтром SmartScreen в Microsoft Defender, как нежелательное.

### Список разрешенных приложений

Как и в Microsoft Edge, антивирусная программа "Защитник Windows" обеспечивает возможность разрешения ошибочно заблокированных или необходимых для выполнения задачи файлов. В этом случае можно внести приложение в список разрешенных. Чтобы узнать, как исключить определенные файлы или папки, см. статью [Настройка Endpoint Protection в Configuration Manager](https://docs.microsoft.com/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders).

## См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Защита от угроз](https://docs.microsoft.com/windows/security/threat-protection/index)
- [Настройка поведенческой и эвристической защиты, а также защиты в режиме реального времени](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-protection-features-windows-defender-antivirus)
- [Защита нового поколения](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/windows-defender-antivirus-in-windows-10)
- [Базовый план безопасности для Microsoft Edge на основе Chromium (версия 79).](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/security-baseline-final-for-chromium-based-microsoft-edge/ba-p/1111863)
