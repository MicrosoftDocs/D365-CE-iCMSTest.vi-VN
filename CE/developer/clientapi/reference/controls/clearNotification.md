---
title: clearNotification (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4d025f92-db16-440c-9f82-e40d71e09862
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c12b39f383689e5f522f2e16e0ccfc95bb6b4961
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388309"
---
# <a name="clearnotification-client-api-reference"></a>clearNotification (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Remove a message already displayed for a control.

## <a name="control-types-supported"></a>Control types supported

Tất cả

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).clearNotification(uniqueId);`

## <a name="parameters"></a>Tham số

|Tên | Loại | Bắt buộc | Mô tả|
|--|--|--|--|
|uniqueId |Chuỗi |Không|The ID to use to clear a specific message that was set using **setNotification** or **addNotification**. If the **uniqueId** parameter isn’t specified, the currently displayed notification will be cleared.| 


## <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean 

**Description**: Indicates whether the method succeeded. 

### <a name="related-topics"></a>Chủ đề liên quan

[addNotification](addNotification.md)

[setNotification](setNotification.md)
