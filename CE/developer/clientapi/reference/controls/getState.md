---
title: getState (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 199d1344-351a-44ee-8c43-f6b00b85a793
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 31f19c192efddd8d164783a0147f52494f9a2051
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387467"
---
# <a name="getstate-client-api-reference"></a>getState (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns the state of the timer control.

This method is only supported for [Unified Interface](/dynamics365/get-started/whats-new/customer-engagement/new-in-july-2017-update#unified-interface-framework-for-new-apps). 

## <a name="control-types-supported"></a>Control types supported

Đồng hồ hẹn giờ

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).getState();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Number

**Description**: Returns one of the following values:

|Value | Tiểu bang |
|--|--|
|1 | Not Set|
|2 | In progress|
|3 | Cảnh báo|
|4 | Violated|
|5 | Success|
|6 | Expired|
|7 | Đã hủy|
|8 | Paused|

### <a name="related-topics"></a>Chủ đề liên quan

[Kiểm soát](../controls.md)
