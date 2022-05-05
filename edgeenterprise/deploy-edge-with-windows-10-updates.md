---
title: Развертывание Microsoft Edge с обновлениями Windows 10
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 05/04/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Развертывание Microsoft Edge с обновлениями Windows 10
ms.openlocfilehash: eec21e3f797166b31b0ac632f94103b866491066
ms.sourcegitcommit: 592f6e40b13e28af588473b2a75c3ae697e5db2d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2022
ms.locfileid: "12505692"
---
# <a name="deploy-microsoft-edge-with-windows-10-updates"></a>Развертывание Microsoft Edge с обновлениями Windows 10

В этой статье содержатся сведения для пользователей, развертывающих Microsoft Edge с помощью обновлений Windows 10.

## <a name="for-windows-10-release-20h2"></a>Для выпуска Windows 10 20H2

Windows 10 20H2 и более поздних версий Microsoft Edge предварительно установленные в качестве браузера по умолчанию. Однако версия 84 edge, поставляемая с Windows 10 20H2, и версия 92 Edge, поставляемая с Windows 10 21H2, устарела. Хотя Microsoft Edge автоматически обновится до более новой версии после входа пользователя, так как время обновления зависит от различных факторов, это может быть несколько нерекомендуемым. Для организаций, которым требуется более полный контроль и требуется обновить Edge (стабильный канал) до последней версии перед входом пользователя, можно использовать следующую команду PowerShell для принудительного обновления Edge во время Windows OOBE.

`Start-Process -FilePath "C:\Program Files (x86)\Microsoft\EdgeUpdate\MicrosoftEdgeUpdate.exe" -argumentlist "/silent /install appguid={56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}&appname=Microsoft%20Edge&needsadmin=True"`

При использовании Windows Autopilot можно заключить этот скрипт в intunewin-файл с помощью средства подготовки содержимого [Microsoft Win32](/mem/intune/apps/apps-win32-prepare). Затем его можно задать в качестве обязательного приложения для страницы состояния регистрации (ESP) при необходимости.

> [!NOTE]
> Если в настоящее время вы используете такие [](/deployedge/microsoft-edge-update-policies#target-channel-override) политики, как переопределение целевого канала или переопределение целевой версии, чтобы оставаться в более старой версии Microsoft Edge, имейте в виду, что описанный выше сценарий не будет учитывать какие-либо политики и просто обновит его до последней версии.[](/deployedge/microsoft-edge-update-policies#targetversionprefix) По умолчанию Microsoft Edge не переход на более раннюю версию, в том числе после получения таких политик.

## <a name="for-windows-10-releases-rs4-through-20h1"></a>Для выпусков Windows 10 RS4-20H1

Службы Windows Server Update Services (WSUS) имеют обновления для каждой версии Windows 10 с RS4 по 20H1. Эти обновления удалят классическое приложение Microsoft Edge Legacy и заменит его на Microsoft Edge. Дополнительные сведения, которые позволят определить, какое обновление WSUS подойдет для вашей версии Windows, см. [в этой статье](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c).

## <a name="for-windows-10-releases-prior-to-rs4-and-windows-7-81-and-earlier"></a>Для выпусков Windows 10 до RS4 (а также Windows 7, 8.1 и более ранних версий)

Обновления Windows для установки Microsoft Edge недоступны для этих версий. Рассмотрите другие варианты развертывания Microsoft Edge на этих устройствах, такие как [диспетчер конфигураций](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) или [Intune.](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Планирование развертывания Microsoft Edge](deploy-edge-plan-deployment.md)
