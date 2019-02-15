---
title: setFormNotification (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 48749e32-8490-4c8f-917c-3f1f8b9c028b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d7097f7ee2dd4557b4be9c9ba6d670c4151d31b5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388581"
---
# <a name="setformnotification-client-api-reference"></a>setFormNotification (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setFormNotification-description.md](./includes/setFormNotification-description.md)]

You can display any number of notifications and they will be displayed until they are removed using [clearFormNotification](clearFormNotification.md). The height of the notification area is limited so each new message will be added to the top. Users can scroll down to view older messages that have not yet been removed.

## <a name="syntax"></a>Cú pháp

`formContext.ui.setFormNotification(message, level, uniqueId);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|message|Chuỗi|Có|The text of the message.|
|level|Chuỗi|Có|The level of the message, which defines how the message will be displayed. Specify one of the following values:<br>`ERROR` : Notification will use the system error icon.<br/>`WARNING` : Notification will use the system warning icon.<br/>`INFO` : Notification will use the system info icon.|
|uniqueId|Chuỗi|Có|A unique identifier for the message that can be used later with [clearFormNotification](clearFormNotification.md) to remove the notification.|

## <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean

**Description**: true if the method succeeded; false otherwise. 


### <a name="related-topics"></a>Chủ đề liên quan

[clearFormNotification](clearFormNotification.md)

[formContext.ui](../formContext-ui.md)

[formContext](../../clientapi-form-context.md)

