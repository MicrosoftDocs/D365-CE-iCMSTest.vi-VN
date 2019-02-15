---
title: clearFormNotification (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 6c57db71-a76d-404c-852e-9c36a1c549ee
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d60ec5344717164aa87b49c6f552d442ff213d1c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387841"
---
# <a name="clearformnotification-client-api-reference"></a>clearFormNotification (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/clearFormNotification-description.md](./includes/clearFormNotification-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.ui.clearFormNotification(uniqueId)`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|uniqueId|Chuỗi|Có|A unique identifier for the message to be cleared that was set using the [setFormNotification](setFormNotification.md) method.|

## <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean

**Description**: true if the method succeeded, false otherwise. 


### <a name="related-topics"></a>Chủ đề liên quan

[setFormNotification](setFormNotification.md)

[formContext.ui](../formContext-ui.md)

[formContext](../../clientapi-form-context.md)

