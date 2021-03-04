---
title: Защита от потери данных в Microsoft Edge
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 03/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Защита от потери данных в Microsoft Edge
ms.openlocfilehash: f25e1fa7a610645f6ca0ca10cbcfc69ae8689b7a
ms.sourcegitcommit: f14286edec59ee9183bdf38c15fc890881efd64f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "11384987"
---
# <a name="data-loss-prevention-dlp-in-microsoft-edge"></a>Защита от потери данных в Microsoft Edge

Защита от потери данных — это система технологий, определяющая и защищающая конфиденциальные корпоративные данные от несанкционированного раскрытия. Чтобы обеспечить соблюдение бизнес-стандартов и отраслевых норм, организации должны защищать конфиденциальные данные и предотвращать несанкционированное раскрытие. Конфиденциальная информация включает финансовые данные и личные сведения (PII), такие как номера кредитных карт, номера социального страхования или медицинские записи, а также многое другое.

Удаленная работа повысила важность использования защиты от потери данных. С увеличением личных и рабочих операций на устройствах в организациях повышается риск несанкционированного распространения корпоративных данных за пределами рабочего места.

Такое смешение действий пользователей распространяется на различные устройства, когда данные перемещаются между личными и корпоративными устройствами в различных общедоступных и закрытых сетях. Итоговым результатом стал существенно возросший риск раскрытия конфиденциальных данных.

Microsoft Edge изначально поддерживает два разных решения для защиты от потери данных: защита от потери данных в конечной точке Майкрософт и Windows Information Protection (WIP).

## <a name="microsoft-endpoint-data-loss-prevention-endpoint-dlp"></a>Защита от потери данных в конечной точке Майкрософт (Endpoint DLP)

Защита от потери данных в конечной точке Майкрософт — это защита от потери данных нового поколения, использующая современные концепции, такие как защита, ориентированная на данные. Она встроена в Windows 10 и Microsoft Edge, поэтому на устройстве не требуются дополнительные агенты или подключаемые модули.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 85 или более поздней.

Чтобы узнать больше о политике защиты от потери данных (DLP) конечной точки, используйте следующие ресурсы.

- [Видео. Microsoft Edge и защита от потери данных](microsoft-edge-video-security-dlp.md)
- [Сведения о защите от потери данных в конечной точке Microsoft 365](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide&preserve-view=true)
- [Начало работы с функцией защиты от потери данных в конечной точке](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-getting-started?view=o365-worldwide&preserve-view=true)

Microsoft Edge внедряет настроенные администратором политики для конфиденциальных файлов и записывает события аудита для несоответствующих действий.

Ниже перечислены некоторые пользовательские действия, доступные для аудита и управления на устройствах с Windows 10:

- Отправка файла. Защита от отправки конфиденциального файла в неавторизованные облачные расположения. <!-- The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.-->
- Защита буфера обмена. Защита от копирования конфиденциальных данных из файла.
- Защита печати. Защита конфиденциального файла от печати.
- Сохранение на USB или в сети. Защита конфиденциального файла от сохранения на съемном USB-накопителе или в неавторизованных сетевых расположениях.

Дополнительные сведения о действиях пользователей, доступных для аудита и управления, см. в разделе [Действия в конечных точках, доступные для отслеживания и реагирования](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on&preserve-view=true).

## <a name="windows-information-protection"></a>Windows Information Protection

См. статью [Поддержка Windows Information Protection (WIP) в Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection) с описанием того, как Microsoft Edge поддерживает Windows Information Protection (WIP). Вы можете узнать больше о системных требованиях, преимуществах и поддерживаемых функциях в следующих разделах:

- [Требования к системе](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#system-requirements)
- [Преимущества Windows Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#windows-information-protection-benefits)
- [Возможности WIP, поддерживаемые в Microsoft Edge](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-information-protection#wip-features-supported-in-microsoft-edge)

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Видео. Защита от потери данных — Microsoft Edge](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [Обзор защиты от потери данных](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies?view=o365-worldwide&preserve-view=true)
- [Защита корпоративных данных с помощью Windows Information Protection](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)
