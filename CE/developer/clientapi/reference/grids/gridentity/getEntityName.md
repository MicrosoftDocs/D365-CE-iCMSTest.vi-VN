---
title: getEntityName (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 20f9127f-c90a-4ea9-aab3-6ef1f0347a48
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 155d041ec9f030dd66b5351116ae4fde1b9828ec
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387440"
---
# <a name="getentityname-client-api-reference"></a>getEntityName (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getEntityName-description.md](./includes/getEntityName-description.md)]

## <a name="grid-types-supported"></a>Grid types supported

Read-only and editable grids

## <a name="syntax"></a>Cú pháp

`gridEntity.getEntityName();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: The logical name for the record in the row.

## <a name="remarks"></a>Chú thích

To get the `gridEntity` object, see [GridEntity](../gridentity.md). 

