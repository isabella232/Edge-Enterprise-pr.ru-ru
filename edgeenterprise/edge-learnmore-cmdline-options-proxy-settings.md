---
title: Параметры прокси-сервера Microsoft Edge
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 'Использование параметров командной строки для настройки параметров прокси-сервера '
ms.openlocfilehash: b5e2326e075ad89481560a6642944a8e88f4daa3
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10980960"
---
# Использование параметров командной строки в Microsoft Edge для настройки параметров прокси-сервера

В этой статье описано, как использовать параметры командной строки для переопределения стандартных параметров сети системы.

>[!NOTE]
>Эта статья относится к Microsoft Edge версии 77 или более поздней.

## Параметры сети системы

По умолчанию в сетевом стеке Microsoft Edge используются параметры сети системы. К этим параметрам относятся *параметры прокси-сервера* и *хранилища сертификатов и закрытых ключей*.

Бывают случаи, когда пользователи запрашивают альтернативу использованию параметров прокси-сервера, заданных по умолчанию в системе. Эти сценарии реализуются в Microsoft Edge за счет поддержки браузером параметров командной строки, которые можно использовать для задания пользовательских параметров прокси-сервера.

Эти параметры командной строки соответствуют следующим политикам в группе **Прокси-сервер**:

- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist)
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode)
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl)
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver)
- [ProxySettings](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxysettings)

## Параметры командной строки для параметров прокси-сервера

Microsoft Edge поддерживает следующие параметры командной строки, связанные с прокси-сервером.

 **`--no-proxy-server`**
 
Сообщает Microsoft Edge не использовать прокси-сервер, даже если система настроена на использование одного из них. Переопределяет любые другие предоставленные параметры прокси-сервера.

**`--proxy-auto-detect`**

Сообщает Microsoft Edge выполнить попытку автоматического удаления конфигурации прокси-сервера. Этот аргумент игнорируется, если настроен `--proxy-server`.

**`--proxy-server=<scheme>=<uri>[:<port>][;...] | <uri>[:<port>] | "direct://"`**

Сообщает Microsoft Edge использовать настраиваемую конфигурацию прокси-сервера. Задать настраиваемую конфигурацию прокси-сервера можно тремя способами.

1. Предоставьте разделенный точкой с запятой файл сопоставления схемы списка с парами URL-адреса/порты. Например, `--proxy-server="http=proxy1:8080;ftp=ftpproxy"` сообщает Microsoft Edge использовать прокси-сервер HTTP типа "proxy1:8080" для URL-адресов "http" и прокси-сервер HTTP типа "ftpproxy:80" для URL-адресов "ftp".
2. Предоставьте один универсальный код ресурса с необязательным портом для использования во всех URL-адресах. Например, `--proxy-server="proxy2:8080"` будет использовать прокси-сервер по адресу "proxy2:8080" для всего трафика.
3. С помощью специального значения "direct://". Например, при использовании `--proxy-server="direct://"` все подключения не будут использовать прокси-сервер. 

>[!NOTE]
>Можно настроить, чтобы Microsoft Edge пытался использовать прокси-сервер и в случае его недоступности переходил к прямому подключению. Например, `--proxy-server="http://proxy2:8080,direct://`.

**`--proxy-bypass-list=(<trailing_domain>|<ip-address>)[:<port>][;...]`**

Сообщает Microsoft Edge обходить любой прокси-сервер заданный для списка узлов, разделенных точкой с запятой. Этот флаг необходимо использовать с `--proxy-server`.

>[!NOTE]
>При сопоставлении доменов не требуются разделители в виде точки ".". Запрос "\*microsoft.com" будет сопоставлен с "imicrosoft.com". Например, `--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` будет использовать прокси-сервер "proxy2" на порте 8080 для всех узлов, кроме запросов для \*.microsoft.com, example.com и 127.0.0.1 на порте 8080. В предыдущем примере запросы imicrosoft.com будут все равно передаваться через прокси-сервер. Однако запросы iexample.com будут обходить прокси-сервер, так как вместо \*.example.com был указан запрос \*example.com.

**`--proxy-pac-url=<pac-file-url>`**

Сообщает Microsoft Edge использовать PAC-файл по указанному URL-адресу. Например, `--proxy-pac-url="https://wpad/proxy.pac"` сообщает Microsoft Edge разрешать данные прокси для URL-запросов, используя файл **proxy.pac**.

## Лицензия на содержимое

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и предоставленные на сайте Chromium.org. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). Исходная страница Chromium находится [здесь](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Эта работа предоставляется в рамках международной лицензии <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## См. также

- Сведения о расширенных параметрах конфигурации и дополнительных параметрах см. в [документации по прокси-серверу](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md) в проекте с открытым исходным кодом Chromium.
- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
