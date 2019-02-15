---
title: getPrimaryAttributeValue (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4bd76f0c-5905-4bc2-a423-7d74a267a464
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d7af3f82c33b296698c18af9a48793a95eca05b5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386245"
---
# <a name="getprimaryattributevalue-client-api-reference"></a>getPrimaryAttributeValue (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getPrimaryAttributeValue-description.md](./includes/getPrimaryAttributeValue-description.md)]

## <a name="grid-types-supported"></a>Grid types supported

Read-only grid

## <a name="syntax"></a>Cú pháp

`gridEntity.getPrimaryAttributeValue();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: The primary attribute value for the record in the row.

## <a name="remarks"></a>Chú thích

To get the `gridEntity` object, see [GridEntity](../gridentity.md). 

