---
title: Узнайте, каким образом Microsoft Edge обрабатывает скачивание смешанного содержимого
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 11/24/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Узнайте о скачивании смешенного содержимого и об обработке такого скачивания в Microsoft Edge.
ms.openlocfilehash: 2bee6416f6c4573ed3273264a771bf704bc2ed09
ms.sourcegitcommit: 592f6e40b13e28af588473b2a75c3ae697e5db2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2022
ms.locfileid: "12505392"
---
# <a name="learn-how-microsoft-edge-handles-mixed-content-downloads"></a>Узнайте, каким образом Microsoft Edge обрабатывает скачивание смешанного содержимого

В этой статье дается определение скачивания смешанного содержимого и поясняется, как Microsoft Edge обрабатывает такое скачивание.

>[!NOTE]
>Эта статья относится к Microsoft Edge версии 85 или более поздней.

## <a name="what-are-mixed-content-downloads"></a>Что такое скачивание смешанного содержимого?

Скачивание смешанного содержимого выполняется при запуске скачивания с HTML-страницы, загруженной по защищенному соединению HTTPS, при наличии одного из следующих условий:

- Одно или несколько перенаправлений расположения скачивания были загружены по незащищенному соединению HTTP.
- Окончательное расположение скачивания было загружено по незащищенному соединению HTTP.

В любом из описанных выше сценариев происходит скачивание смешанного содержимого, поскольку запрос был сделан с помощью безопасного протокола HTTPS, а для получения доступа к итоговому месту назначения используются протоколы HTTP и HTTPS. В современных браузерах отображаются предупреждения о таком типе содержимого, указывая, что при скачивании данные могут передаваться без защиты, хотя доступ к исходной странице был защищенным.

## <a name="download-warnings-and-user-options"></a>Предупреждения при скачивании и пользовательские параметры

Предупреждение при скачивании гарантирует, что пользователи знают о том, что скачиваемый файл может быть прочитан злоумышленниками в их сети. Это предупреждение позволяет пользователю принять обоснованное решение о том, следует ли скачивать файл.

В Microsoft Edge скачивание смешанного содержимого блокируется, но пользователи могут переопределить это поведение и скачать файл, если захотят. В Microsoft Edge планируется начать блокировать скачивание исполняемых файлов смешанного содержимого, начиная с Microsoft Edge версии 85, а в будущих выпусках будут блокироваться различные типы файлов.

> [!NOTE]
> Развертывание этой функции может быть изменено на основе расписания выпусков и отзывов пользователей.

<!-- The schedule of the block for different filetypes is to be determined and may be impacted by usage data and user feedback. -->

В области загрузки предупреждение о блокировании выглядит, как пример на следующем снимке экрана.

 ![Предупреждение о смешанном содержимом в области загрузки](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-tray-warning.png)

На странице загрузок предупреждение о блокировании выглядит, как следующий пример снимка экрана:

 ![Запрос на переопределение для смешанного содержимого](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-page-warning.png)

Если пользователь решит продолжить скачивание, ему будет предложено подтвердить свое действие. На следующем снимке экрана показан пример запроса подтверждения.

 ![Выбор режима Internet Explorer](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-override.png)

## <a name="supporting-policies"></a>Вспомогательные политики

Организации, которые хотят исключить блокировку смешанного содержимого для определенных веб-сайтов, могут для этого использовать политику [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls).

## <a name="content-license"></a>Лицензия на содержимое

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и предоставленные на сайте Chromium.org. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). Исходная страница Chromium находится [здесь](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Эта работа предоставляется в рамках международной лицензии <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
