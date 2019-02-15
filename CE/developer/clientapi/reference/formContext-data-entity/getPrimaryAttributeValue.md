---
title: getPrimaryAttributeValue (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1a66f93d-a47c-4316-91f1-dcf5d09f9d19
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 861259cc24573c1ca5820106385e3b5c722d8e13
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386120"
---
# <a name="getprimaryattributevalue-client-api-reference"></a>getPrimaryAttributeValue (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getPrimaryAttributeValue-description.md](./includes/getPrimaryAttributeValue-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.entity.getPrimaryAttributeValue();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: String.

**Description**: The name of the entity.

## <a name="remarks"></a>Chú thích

Each entity has one string attribute that is designated as the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.PrimaryNameAttribute>. The value for this attribute is used when links to the record are displayed.



