---
title: setNotification (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
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
ms.openlocfilehash: 3ebf8e1351bb3ca55934c884c1bada69d055c4fd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385803"
---
# <a name="setnotification-client-api-reference"></a>setNotification (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Displays an error message for the control to indicate that data isn’t valid. When this method is used,  a red "X" icon appears next to the control. On Dynamics 365 for Customer Engagement apps mobile clients, tapping on the icon will display the message. 

## <a name="control-types-supported"></a>Control types supported

Tất cả

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).setNotification(message,uniqueId);`

## <a name="parameters"></a>Tham số

|Tên | Loại | Bắt buộc | Mô tả|
|--|--|--|--|
|message |Chuỗi |Có|The message to display.| 
|uniqueId |Chuỗi |Không|The ID to use to clear this message when using the **clearNotification** method.
| | |

## <a name="return-value"></a>Giá trị trả lại
**Type**: Boolean 

**Description**: Indicates whether the method succeeded.

## <a name="remarks"></a>Chú thích

Setting an error notification on a control will block the form from saving.

### <a name="related-topics"></a>Chủ đề liên quan

[addNotification](addNotification.md)

[clearNotification](clearNotification.md)
