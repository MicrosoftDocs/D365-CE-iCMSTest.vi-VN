---
title: getEntityReference (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: b8e23eee-f20f-4db9-9cc6-7fa5dd7ce2bb
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: aa247d5e7eadaa7a6a627e260f916611e077f045
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387456"
---
# <a name="getentityreference-client-api-reference"></a>getEntityReference (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getEntityReference-description.md](./includes/getEntityReference-description.md)]

## <a name="grid-types-supported"></a>Grid types supported

Read-only and editable grids

## <a name="syntax"></a>Cú pháp

`gridEntity.getEntityReference();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Lookup

**Description**: Lookup object that references the record in the row. The object has the following attributes:
- **entityType**: String. The logical name for the record in the row. The same data returned by the **GridEntity**.[getEntityName](getEntityName.md) method.
- **id**: String. The Id for the record in the row. The same data returned by the **GridEntity**.[getId](getId.md) method.
- **name**: String. The primary attribute value for the record in the row. The same data returned by the **GridEntity**.[getPrimaryAttributeValue](getPrimaryAttributeValue.md) method.

## <a name="remarks"></a>Chú thích

To get the `gridEntity` object, see [GridEntity](../gridentity.md). 

