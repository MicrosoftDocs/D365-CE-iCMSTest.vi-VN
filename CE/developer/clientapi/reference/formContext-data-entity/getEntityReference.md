---
title: getEntityReference (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: 8b690ae0208fbdd4234d11dc6aec36a68b9de456
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387216"
---
# <a name="getentityreference-client-api-reference"></a>getEntityReference (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getEntityReference-description.md](./includes/getEntityReference-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.entity.getEntityReference();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Lookup object.

**Description**: The returned object has following three attributes:

- **entityType**: String. Logical name of the entity record. For example, "account".
- **id**: String. GUID value of the entity record.
- **name**: (Optional) String. Name of the entity record. 



