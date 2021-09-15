---
title: Поддержка фильтра SmartScreen в Microsoft Defender в браузере Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Поддержка фильтра SmartScreen в Microsoft Defender в браузере Microsoft Edge
ms.openlocfilehash: 363605200c61807ca526818ab417301273d64f91
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979569"
---
# <a name="microsoft-edge-support-for-microsoft-defender-smartscreen"></a>Поддержка фильтра SmartScreen в Microsoft Defender в браузере Microsoft Edge

В этой статье описываются преимущества использования фильтра SmartScreen в Microsoft Defender, порядок работы этой функции Microsoft Edge и ее настройка.

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

Фильтр SmartScreen в Microsoft Defender — эта служба, которую использует браузер Microsoft Edge, чтобы защитить вас в Интернете. Фильтр SmartScreen в Microsoft Defender предоставляет систему раннего предупреждения о веб-сайтах, которые могут участвовать в фишинге или попытках распространения вредоносных программ с помощью целенаправленных атак. Для дополнительных сведений см. [видео: безопасный просмотр в Microsoft Edge.](microsoft-edge-video-security-smartscreen.md)

> [!NOTE]
> До Windows 10 версии 1703 эта функция называлась "фильтр SmartScreen" при использовании в браузере и "Microsoft SmartScreen" при использовании вне браузера.

## <a name="the-benefits-of-microsoft-defender-smartscreen"></a>Преимущества фильтра SmartScreen в Microsoft Defender

Фильтр SmartScreen в Microsoft Defender обладает целым рядом преимуществ, приведенных в следующем списке. Подробное описание этих преимуществ доступно в [документации фильтра SmartScreen в Microsoft Defender ](/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview#benefits-of-windows-defender-smartscreen). Преимущества:

- Поддержка защиты от фишинга и вредоносного ПО
- Защита URL-адресов и приложений на основе репутации
- Интеграция в операционную систему
- Улучшенная эвристика и диагностические данные
- Управление с помощью групповой политики и Microsoft Intune
- Блокирование URL-адресов, связанных с потенциально нежелательными приложениями

## <a name="understand-how-microsoft-defender-smartscreen-works"></a>Принцип работы фильтра SmartScreen в Microsoft Defender

Предупреждения фильтра SmartScreen в Microsoft Defender срабатывают на основе различных данных. Данные берутся из множества источников, в число которых входят отзывы пользователей, поставщики данных и аналитические модели. Эти данные помогают определять потенциально вредоносное содержимое. Фильтр SmartScreen в Microsoft Defender также проверяет загруженные приложения и установщики приложений на предмет вредоносного кода. В обоих случаях фильтр SmartScreen в Microsoft Defender предупреждает пользователей о подозрительном содержимом.

### <a name="site-analysis"></a>Анализ сайтов

Фильтр SmartScreen в Microsoft Defender определяет, является ли сайт потенциально вредоносным, с помощью следующих действий.

- Анализ просмотренных веб-страниц на предмет подозрительного поведения.
- Сверка посещенных веб-сайтов с динамическим списком фишинговых сайтов.

Если фильтр SmartScreen в Microsoft Defender определяет, что страница является вредоносной, для пользователя отображается страница с предупреждением о том, что этот сайт считается небезопасным. На следующем снимке экрана показан пример страницы предупреждения фильтра SmartScreen в Microsoft Defender, когда пользователь пытается открыть вредоносный веб-сайт.

![Страница фильтра SmartScreen в Microsoft Defender при блокировке ссылки на внешний сайт](media/microsoft-edge-security-smartscreen/microsoft-edge-smartscreen-warning.png)

В сообщении предупреждения пользователь может указать, что сайт является безопасным или небезопасным. Дополнительные сведения см. в статье [Процедура сообщения о сайте](/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device#how-users-can-report-websites-as-safe-or-unsafe).

### <a name="file-analysis"></a>Анализ файлов

Фильтр SmartScreen в Microsoft Defender определяет, может ли загруженное приложение или установщик быть потенциально вредоносным, на основе множества критериев, включая трафик загрузки, журнал загрузки, прошлые результаты антивирусных проверка и репутацию URL-адреса.

- Файлы с заведомо безопасной репутацией загружаются без каких бы то ни было уведомлений.  
- При попытке загрузить вредоносный файл отображается предупреждение о том, что файл небезопасен и считается вредоносным. На следующем снимке экрана показан пример предупреждения о вредоносном файле.

  ![Уведомление о блокировке SmartScreen в Microsoft Defender для вредоносного файла](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-known-malicious.png)

- Для неизвестных файлов отображается предупреждение о том, что файл не соответствует известным шаблонам, и рекомендуется осторожность. На следующем снимке экрана показан пример предупреждения о неизвестном файле.

  ![Уведомление о блокировке SmartScreen в Microsoft Defender для неизвестного файла](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-unknown-malicious.png)

Не все неизвестные программы являются вредоносными. Цель предупреждения о неизвестных файлах — предоставить пользователям контекст и рекомендации, особенно если это непредвиденное предупреждение.

  ![Сохранение файлов, определенных в качестве вредоносных на основании репутации](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-unknown-malicious-keep.png)

Тем не менее, пользователи могут все равно загрузить и запустить приложение, щелкнув **... | Сохранить | Показать больше | Все равно сохранить**.

> [!TIP]
> **К сведению корпоративных клиентов.** По умолчанию фильтр SmartScreen в Microsoft Defender разрешает пользователям обходить предупреждения. Такое поведение пользователей сопряжено с потенциальным риском, поэтому рекомендуем проверить эти [рекомендуемые параметры групповой политики](/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-available-settings#recommended-group-policy-and-mdm-settings-for-your-organization).

Вы увидите, как фильтр SmartScreen в Microsoft Defender реагирует на различные сценарии на нашем [демонстрационном сайте](https://demo.smartscreen.msft.net/).

## <a name="microsoft-defender-smartscreen-and-user-privacy"></a>Фильтр SmartScreen в Microsoft Defender и конфиденциальность пользователей

Фильтр SmartScreen в Microsoft Defender защищает пользователей во время просмотра веб-сайтов в Интернете с помощью системы проверки репутации. Microsoft Edge передает необходимую информацию о файле или URL-адресе в службу фильтра SmartScreen в Microsoft Defender, чтобы запустить проверку репутации. Алгоритм проверки сравнивает веб-сайт или файл с динамическими списками заведомо опасных сайтов и файлов. Во всех запросах к службе фильтра SmartScreen в Microsoft Defender применяется шифрование TLS. Служба возвращает результаты проверки репутации, после чего в Microsoft Edge может появиться предупреждение для сайта или файла. Эти результаты сохраняются на локальном устройстве.

Служба фильтра SmartScreen в Microsoft Defender сохраняет данные о проверках репутации. По мере определения новых сайтов эта служба добавляет их в динамическую базу данных заведомо вредоносных URL-адресов и файлов. Эти данные хранятся на защищенных серверах Майкрософт и используются только для служб безопасности Майкрософт. Эти данные никогда не используются для идентификации пользователей или для подготовки целенаправленных рекламных материалов для пользователя. При очистке кэша браузера удаляются все данные URL-адресов фильтра SmartScreen в Microsoft Defender, хранящиеся на локальном устройстве. При очистке журнала загрузок удаляются все данные SmartScreen о загруженных файла, хранящиеся на локальном устройстве.

Дополнительные сведения о фильтре SmartScreen в Microsoft Defender и о конфиденциальности в Microsoft Edge, см. в [технической документации по конфиденциальности Microsoft Edge](/microsoft-edge/privacy-whitepaper#smartscreen).

## <a name="microsoft-defender-smartscreen-setup-for-admins"></a>Настройка фильтра SmartScreen в Microsoft Defender для администраторов

Администраторы могут настраивать фильтр SmartScreen в Microsoft Defender с помощью групповой политики, Microsoft Intune или параметров управления мобильными устройствами (MDM). На основании настройки фильтра SmartScreen в Microsoft Defender можно отображать для пользователей страницу предупреждения и дать им возможность продолжить просмотр сайта или полностью заблокировать сайт.

### <a name="microsoft-defender-smartscreen-set-up-using-group-policy"></a>Настройка фильтра SmartScreen в Microsoft Defender с помощью групповой политики

Полный список политик SmartScreen см. в разделе [Параметры фильтра SmartScreen в Microsoft Defender](./microsoft-edge-policies.md#smartscreen-settings)

### <a name="microsoft-defender-smartscreen-set-up-using-mdm"></a>Настройка фильтра SmartScreen в Microsoft Defender с помощью MDM

Дополнительные сведения см. в следующих разделах:

- [Параметры Windows Intune для фильтра SmartScreen в Microsoft Defender](/mem/intune/protect/endpoint-protection-windows-10#windows-defender-smartscreen-settings)
- [Параметры политики MDM](/mem/intune/protect/endpoint-protection-windows-10#windows-defender-smartscreen-settings)

## <a name="microsoft-defender-smartscreen-setup-for-users"></a>Настройка фильтра SmartScreen в Microsoft Defender для пользователей

Фильтр SmartScreen в Microsoft Defender по умолчанию включен в браузере Microsoft Edge. Чтобы выключить фильтр SmartScreen в Microsoft Defender, перейдите по адресу *edge://settings/privacy > Services > Microsoft Defender SmartScreen*. Этот параметр действует для всех профилей, связанных с установкой Microsoft Edge на устройстве. Этот параметр не синхронизируется между устройствами. Этот параметр действует для просмотра в режиме InPrivate и для гостевого режима. Если для управления устройством используются групповые политики, заданные организацией, эта конфигурация доступна по адресу *edge://settings/privacy*.

> [!NOTE]
> Пользователи могут настраивать фильтр SmartScreen в Microsoft Defender на отдельном устройстве, если это не запрещено групповой политикой или MDM. Дополнительные сведения см. в статье [Настройка и использование SmartScreen Защитника Windows на отдельных устройствах](/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device).

## <a name="frequently-asked-questions"></a>Вопросы и ответы

### <a name="how-does-the-reputation-check-system-work"></a>Как работает система проверки репутации?

Когда вы просматриваете веб-сайты, фильтр SmartScreen в Microsoft Defender распределяет веб-сайты и загружаемые файлы по категориям: основной трафик, опасные или неизвестные. Основной трафик — это популярные сайты, которые фильтр SmartScreen в Microsoft Defender считает надежными. Если перейти на сайт, отмеченный в качестве опасного, фильтр SmartScreen в Microsoft Defender немедленно заблокирует доступ к этому сайту. При переходе на неизвестный сайт фильтр проверит его репутацию и определит, следует ли открывать этот сайт.

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Видео: безопасный просмотр в Microsoft Edge](microsoft-edge-video-security-smartscreen.md)
- [Обзор фильтра SmartScreen в Microsoft Defender](/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview)
- [Защита от угроз](/windows/security/threat-protection/index)
- [Защита от потенциально нежелательных приложений](./microsoft-edge-potentially-unwanted-apps.md)