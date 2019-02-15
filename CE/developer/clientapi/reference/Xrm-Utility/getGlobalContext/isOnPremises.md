---
title: isOnPremise (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 855767c5-c48f-47a2-8f99-52423221d974
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c0ec37b0ef8edb01f578e8e11db60be5e9c08b32
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387107"
---
# <a name="isonpremise-client-api-reference"></a>isOnPremise (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns a boolean value indicating if the Customer Engagement instance is hosted on-premises or online. 

## <a name="syntax"></a>Cú pháp

```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.isOnPremises();
```

## <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean

**Description**: **true** if the Customer Engagement instance is on-premises; **false** otherwise.

### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.Utility.getGlobalContext](../getGlobalContext.md)



