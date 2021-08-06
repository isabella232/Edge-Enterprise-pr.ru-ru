---
title: Локальная синхронизация для пользователей Active Directory (AD)
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Локальная синхронизация для пользователей Active Directory (AD)
ms.openlocfilehash: e6b123122e6fb5cd97f72423cff079f61eee2f1836f217fe1970bc05492a0f69
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "11727562"
---
# <a name="on-premises-sync-for-active-directory-ad-users"></a>Локальная синхронизация для пользователей Active Directory (AD)

В этой статье объясняется, как пользователи Active Directory (AD) могут перемещать избранное и параметры Microsoft Edge между компьютерами, не подключаясь к облачным службам (Майкрософт).

> [!NOTE]
> Эта статья относится к Microsoft Edge версии 85 или более поздней.

## <a name="introduction"></a>Введение

Для синхронизации данных пользователя в Microsoft Edge обычно требуется учетная запись Майкрософт или учетная запись Azure Active Directory (Azure AD), а также подключение к облачным службам (Майкрософт). При использовании локальной синхронизации Microsoft Edge сохраняет избранное и параметры пользователя Active Directory в файле, который можно перемещать между различными компьютерами. Локальная синхронизация не влияет на облачную синхронизацию профилей, для которых она разрешена.

## <a name="how-it-works"></a>Принцип работы

Microsoft Edge позволяет связать профили с учетными записями Active Directory (AD), которые невозможно использовать с облачной синхронизацией. При включении локальной синхронизации данные из профиля AD сохраняются в файле profile.pb. По умолчанию этот файл хранится в *%APPDATA%/Microsoft/Edge*. Записанный файл можно перемещать между несколькими компьютерами, и на каждом из них будет выполняться чтение и запись данных пользователя. Microsoft Edge только считывает и записывает из этого файла; ответственность за перемещение файла по мере необходимости лежит на администраторе.

## <a name="use-on-premises-sync"></a>Использование локальной синхронизации

Чтобы использовать локальную синхронизацию, необходимо включить ее, связать профиль с учетной записью AD и при необходимости изменить расположение данных пользователя.

### <a name="enable-on-premises-sync"></a>Включение локальной синхронизации

Чтобы включить локальную синхронизацию в Microsoft Edge, настройте политику [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled).

### <a name="ensure-that-a-profile-is-associated-with-an-active-directory-account"></a>Убедитесь, что профиль связан с учетной записью Active Directory

Для выполнения локальной синхронизации необходим профиль, связанный с учетной записью Active Directory (AD). При отсутствии такого профиля локальная синхронизация не выполняется. Чтобы убедиться, что пользователи входят в систему с помощью учетной записи AD, настройте политику [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin). При локальной синхронизации Microsoft Edge использует только AD для установления удостоверения для данных пользователя, и нет прямой связи между тем, как Microsoft Edge считывает и записывает локальные данные, и тем, как администратор настроил роуминг для пользователя AD.

### <a name="change-the-location-of-the-user-data-optional"></a>Изменение расположения данных пользователя (необязательно)

По умолчанию данные пользователя хранятся в файле **profile.pb** в *%APPDATA%/Microsoft/Edge*. Чтобы изменить расположение этого файла, настройте политику [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation).

## <a name="changes-in-the-user-experience-when-on-premises-sync-is-enabled"></a>Изменения во взаимодействии с пользователем при включении локальной синхронизации

Если включена локальная синхронизация, пользователям не будет предложено включить синхронизацию. Кроме того, пользователи не могут отключить синхронизацию в параметрах синхронизации или включить типы синхронизации, которые не поддерживаются локальной синхронизацией.

## <a name="on-premises-sync-usage-notes"></a>Заметки об использовании локальной синхронизации

### <a name="running-cloud-sync-and-on-premises-sync-on-the-same-computer"></a>Выполнение облачной синхронизации и локальной синхронизации на одном компьютере

Локальная синхронизация не влияет на облачную синхронизацию. Если в Microsoft Edge есть несколько учетных записей Майкрософт или профилей Azure Active Directory, которые синхронизируются с облаком, эти профили продолжат синхронизироваться при включении локальной синхронизации.

### <a name="running-microsoft-edge-on-more-than-one-computer-at-a-time-isnt-recommended"></a>Не рекомендуется запуск Microsoft Edge на нескольких компьютерах одновременно

Так как при локальной синхронизации выполняется перемещение файла данных пользователя между компьютерами, изменения между одновременными сеансами не синхронизируются. Поэтому локальную синхронизацию лучше всего использовать на одном компьютере. Если выполняются одновременные локальные сеансы, данные на любом из компьютеров могут неожиданно переопределяться данными с другого компьютера при следующем запуске сеанса браузера.

> [!NOTE]
> Microsoft Edge блокирует файл **profile.pb** при включении локальной синхронизации. Если один файл **profile.pb** совместно используется на нескольких компьютерах с помощью перенаправления папок, тогда можно запускать только один экземпляр Microsoft Edge, использующий этот файл.

### <a name="using-other-sync-policies-with-on-premises-sync"></a>Использование других политик синхронизации при локальной синхронизации

Политику [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) можно использовать для выборочного отключения избранного или параметров синхронизации при необходимости. Политика [SyncDisabled](./microsoft-edge-policies.md#syncdisabled) не влияет на локальную синхронизацию.

## <a name="see-also"></a>См. также

- [Целевая страница Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge и службы переноса параметров в рамках предприятия Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Синхронизация Microsoft Edge Enterprise](microsoft-edge-enterprise-sync.md)