---
title: Microsoft Edge отключит изменение document.domain
ms.author: niarci
author: dan-wesley
manager: erikan
ms.date: 04/25/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge отключит изменение document.domain
ms.openlocfilehash: 197334da0f70aa2cfa081a240de383c79fbbf701
ms.sourcegitcommit: 592f6e40b13e28af588473b2a75c3ae697e5db2d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2022
ms.locfileid: "12505734"
---
# <a name="microsoft-edge-will-disable-modifying-documentdomain"></a>Microsoft Edge отключит изменение`document.domain`

> [!NOTE]
> Эта статья относится к Microsoft Edge стабильной версии 106 или более поздней.

> [!WARNING]
> Если веб-сайт `document.domain`полагается на то, что с помощью политики одного источника вы можете отключить ее, вам потребуется выполнить действие. Продолжайте читать дополнительные сведения о том, почему это изменяется, [](#alternative-cross-origin-communication) или перейдите к альтернативному обмену данными между источниками, чтобы узнать о альтернативных механизмах для обеспечения взаимодействия между источниками.

## <a name="introduction"></a>Введение

Свойство domain интерфейса Document получает или задает часть домена источника текущего документа, используемую политикой [того же источника](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy).

Начиная с Microsoft Edge версии 106 попытки `document.domain` изменить свойство с помощью JavaScript будут игнорироваться. Для обмена данными между источниками необходимо использовать альтернативные подходы, `postMessage()` например API обмена сообщениями каналов.

В качестве альтернативы, если веб-сайт `document.domain` использует политику одного источника, которая работает правильно, `Origin-Agent-Cluster: ?0` сайт может отправить заголовок. Этот заголовок должен быть отправлен из всех других документов, для которых требуется заголовок.

> [!NOTE]
> `document.domain` не оказывает влияния, если только один документ задает его.

## <a name="why-make-documentdomain-immutable"></a>Зачем делать `document.domain` неизменяемым?

Некоторые веб-сайты разрешают `document.domain` обмен данными между страницами "один сайт, но независимо от источника". Настройка `document.domain` позволяет легко обмениваться данными с документами одного сайта. Так как это изменение [отключает](https://html.spec.whatwg.org/multipage/origin.html#relaxing-the-same-origin-restriction) политику одного источника, родительская страница может получить доступ к документу iframe того же сайта и просмотреть дерево DOM и наоборот.

> [!IMPORTANT]
> Сайты с одинаковым и межсайтовом доступом имеют одинаковые [значения eTLD+1](https://web.dev/same-site-same-origin/#:~:text=the%20whole%20site%20name%20is%20known%20as%20the%20etld%2B1) , но разные поддомены.

Предположим, что страница внедрения `https://parent.example.com` страницы iframe из `https://video.example.com`. Эти страницы имеют одинаковые значения eTLD+1 () с`example.com` разными поддоменами. Если для обеих `document.domain` страниц задано значение `'example.com'`, браузер обрабатывает эти две страницы так, как если бы они были одинаковыми.

Этот метод удобен. но это создает угрозу безопасности.  

## <a name="security-concerns-with-documentdomain"></a>Проблемы безопасности с помощью `document.domain`

Связанные с безопасностью `document.domain` проблемы привели к изменению спецификации, которая предупреждает разработчиков об этой проблеме и сообщает им, чтобы избежать ее использования, если это возможно. Текущее обсуждение с [другими поставщиками браузеров](https://github.com/w3ctag/design-reviews/issues/564) выполняется в том же направлении.

В следующих примерах показано, как злоумышленник может использовать его `document.domain`.

Рассмотрим общую службу размещения, которая предоставляет уникальный поддомен каждому клиенту. Если разработчик задается `document.domain` на своей странице, страница злоумышленника, обслуживаемая из другого поддомена, может задать то же значение и изменить содержимое страницы-злоумышленника.

Аналогичным образом рассмотрим общую службу размещения, которая обслуживает страницы с использованием разных портов для каждого клиента. Если разработчик задается `document.domain` на своей странице, страница злоумышленника, обслуживаемая из другого порта, может задать то же значение и изменить содержимое страницы-злоумышленника. Эта атака возможна, так `document.domain` как игнорирует компонент номера порта источника.

> [!NOTE]
>Дополнительные сведения о последствиях `document.domain`настройки для безопасности см. в статье [Document.domain на сайте MDN](https://developer.mozilla.org/docs/Web/API/Document/domain#setter).

## <a name="how-will-i-know-if-my-site-is-affected"></a>Как узнать, затронут ли мой сайт?

Если это изменение повлияет на веб-сайт, Microsoft Edge появится предупреждение на панели "Проблемы devTools". На следующем снимке экрана показан пример этого предупреждения.

:::image type="content" source="media/edge-learnmore-origin-keyed-agent-cluster/document-domain-modification-warning.png" alt-text="Предупреждение при изменении document.domain.":::

Если у вас настроена конечная точка отчетов, вам также будут отправляться отчеты об устаревании. Узнайте больше об [использовании API отчетов](https://web.dev/reporting-api/) с существующими службами сбора отчетов или создании собственного решения для создания отчетов.

> [!TIP]
> Вы можете запустить сайт с помощью устаревшего аудита [API LightHouse](https://web.dev/deprecations/), чтобы найти все API, которые планируется удалить из Microsoft Edge.

## <a name="alternative-cross-origin-communication"></a>Альтернативное взаимодействие между источниками

В настоящее время у вас есть два варианта замены `document.domain` веб-сайта. В большинстве случаев может заменять [postMessage()](https://developer.mozilla.org/docs/Web/API/Window/postMessage) независимо от источника или [API](https://developer.mozilla.org/docs/Web/API/Channel_Messaging_API) обмена сообщениями каналов `document.domain`.

В следующем списке показаны действия, `postMessage()` `document.domain` которые необходимо выполнить разработчику, чтобы использовать вместо межсайтовой манипуляции с DOM.

1. `https://parent.example.com` отправляет сообщение через элемент `postMessage()` iframe, содержащий `https://video.example.com` запрос на изменение собственной виртуальной машины DOM.
2. `https://video.example.com` управляет своим doM и использует для `postMessage` уведомления родительского объекта об успешном выполнении.
3. `https://parent.example.com` подтверждает успешное выполнение.

Для шага 1 в:`https://parent.example.com`

```

// Configure a handler to receive messages from the subframe.
iframe.addEventListener('message', (event) => { 

// Reject all messages except from https://video.example.com 
  if (event.origin !== 'https://video.example.com') return;
  
  // Filter success messages 
    if (event.data === 'succeeded') { 

    // DOM manipulation is succeeded 

  } 

}); 

// Send a message to the subframe at https://video.example.com

iframe.postMessage('Request DOM manipulation', 'https://video.example.com'); 

```

Для шага 2 в:`https://video.example.com`

```

// Configure a handler to receive messages from the parent frame.
window.addEventListener('message', (event) => {
 
  // Reject all messages except ones from https://parent.example.com 
  
  if (event.origin !== 'https://parent.example.com') return;
  
  // Perform requested DOM manipulation on https://video.example.com.
  
  if (event.data === "showTheButton") {
     document.getElementById('btnContinue').style.visibility = 'visible';
     // Send a success message back to the parent.

     event.source.postMessage('succeeded', event.origin); 
  }
}); 

```

### <a name="send-the-origin-agent-cluster-0-header-as-a-last-resort"></a>Отправка `Origin-Agent-Cluster: ?0` заголовка в крайнем случае

Если у вас есть веской причины `document.domain`продолжить настройку, можно `Origin-Agent-Cluster: ?0` отправить заголовок ответа в целевом документе.

```
Origin-Agent-Cluster: ?0 
```

Заголовок `Origin-Agent-Cluster` указывает браузеру, должен ли документ обрабатываться кластером агента с ключом источника. Дополнительные сведения см. в `Origin-Agent-Cluster`статье ["Запрос изоляции производительности с помощью заголовка Origin-Agent-Cluster"](https://web.dev/origin-agent-cluster/).

При отправке этого заголовка документ может `document.domain` продолжать задаваться даже после того, как он станет неизменяемым по умолчанию.

## <a name="browser-compatibility"></a>Совместимость браузера

Следующие организации поддерживают нерекомендуемый `document.domain` режим в целях совместимости браузера.

- В [спецификации источника](https://html.spec.whatwg.org/multipage/origin.html#:~:text=Because%20of%20these%20security%20pitfalls%2C%20this%20feature%20is%20in%20the%20process%20of%20being%20removed%20from%20the%20web%20platform) указывается, что компонент должен быть удален.
- [Стандартная позиция Mozilla](https://github.com/mozilla/standards-positions/issues/601) по умолчанию `document.domain` рассматривает возможность отключения прототипов.
- [WebKit](https://github.com/w3ctag/design-reviews/issues/564#issuecomment-768450217) указывает, что он в умеренной положительной части о нерекомендуемом методе `document.domain` задания.

## <a name="other-resources"></a>Другие ресурсы

- [Document.domain](https://developer.mozilla.org/docs/Web/API/Document/domain)
- [Изоляция и нерекомендуемая изоляция источника `document.domain`](https://github.com/mikewest/deprecating-document-domain/)
- [Нерекомендуемый `document.domain` метод задания](https://github.com/w3ctag/design-reviews/issues/564)

## <a name="content-license"></a>Лицензия на содержимое

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и предоставленные на сайте Chromium.org. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). Исходная страница Chromium находится [здесь](https://developer.chrome.com/blog/immutable-document-domain/).

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Эта работа предоставляется в рамках международной лицензии <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
