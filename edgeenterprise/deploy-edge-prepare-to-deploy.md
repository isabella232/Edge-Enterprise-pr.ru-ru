---
title: Microsoft Edge в вашей среде
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge в вашей среде
ms.openlocfilehash: 2381380cb399f6a1fbb5efa9378ffeba20fa774f
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979665"
---
# <a name="microsoft-edge-in-your-environment"></a>Microsoft Edge в вашей среде

В этой статье описывается, как подготовиться к развертыванию Microsoft Edge, когда устаревшая версия Microsoft Edge завершит службу.

Как было объявлено в [записи блога](https://aka.ms/EdgeLegacyEOS) группы по продуктам Microsoft Edge, поддержка устаревшей версии Microsoft Edge для настольных компьютеров завершится 9 марта 2021 г. Апрельский выпуск вторничного обновления (или "B") удалит устаревшую версию Microsoft Edge с устройств под управлением Windows 10 (версий начиная с RS4 и по 20H1) и заменит ее на Microsoft Edge.

## <a name="how-to-prepare"></a>Подготовка

Чтобы подготовиться к установке Microsoft Edge на устройствах с Windows 10 RS4-20H1 вторничным обновлением в апреле, рекомендуем прочитать статью [Планирование развертывания Microsoft Edge](deploy-edge-plan-deployment.md).

Составив план развертывания, используйте один из следующих подходов для подготовки к развертыванию Microsoft Edge.

- **Установите групповые политики для настройки подхода к обновлению Microsoft Edge.** Дополнительные сведения см. в [справке по настройке параметров политики Microsoft Edge в Windows](configure-microsoft-edge.md). Обратите особое внимание на [справочные материалы по политике обновления](microsoft-edge-update-policies.md). Если установить групповые политики для управления обновлениями до установки апрельского вторничного обновления, Microsoft Edge сразу же начнет соблюдать вашу политику. Если никакая групповая политика не установлена, Microsoft Edge автоматически обновится.

- **Удалите настольное приложение устаревшей версии Microsoft Edge до даты окончания ее службы 9 марта 2021г. и разверните Microsoft Edge**. Для Windows 10 RS4-20H1 это можно сделать с помощью Обновлений Windows. Дополнительные сведения см. в статье [Развертывание Microsoft Edge с обновлениями Windows 10](deploy-edge-with-windows-10-updates.md).

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Планирование развертывания Microsoft Edge](deploy-edge-plan-deployment.md)