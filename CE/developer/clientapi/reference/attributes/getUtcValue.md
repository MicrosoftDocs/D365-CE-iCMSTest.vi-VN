---
title: getUtcValue (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: ebd1526e-d014-41a3-973d-75742b9cfbd3
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5950a6dcdc180fdcc00330e5e8c79b3604ed0ef9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385859"
---
# <a name="getutcvalue-client-api-reference"></a>getUtcValue (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns a UTC-equivalent date and time value of the value stored in a **datetime** type of attribute. UTC stands for Coordinated Universal Time.

## <a name="attribute-types-supported"></a>Attribute types supported

ngày giờ

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getUtcValue()`

## <a name="return-value"></a>Giá trị trả lại

**Type**: datetime. 

**Description**: The UTC-equivalent date and time value of the value stored in an attribute.


### <a name="related-topic"></a>Related topic
[setUtcValue (Client API reference)](setUtcValue.md)

