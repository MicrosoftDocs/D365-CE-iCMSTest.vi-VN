---
title: getAttribute (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9ef1c886-a0b8-4ba9-bb9f-e6ecfa9d6dff
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fe690beea6321eabb7cd4ee07ed701022abd4435
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388705"
---
# <a name="getattribute-client-api-reference"></a>getAttribute (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns a string value that represents the type of attribute. 

## <a name="attribute-types-supported"></a>Attribute types supported

Tất cả

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getAttributeType()`

## <a name="return-value"></a>Giá trị trả lại

This method will return one of the following **string** values:

- boolean
- ngày giờ
- thập phân
- double
- số nguyên
- lookup
- memo
- money
- multioptionset
- optionset
- chuỗi
