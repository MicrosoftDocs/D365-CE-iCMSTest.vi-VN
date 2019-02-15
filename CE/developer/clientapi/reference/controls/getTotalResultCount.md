---
title: getTotalResultCount (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1f9169ce-cba3-4bb6-af20-f86140139cfe
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 23fd1bf802636bfd7022089c4e4cb54e7d937925
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385961"
---
# <a name="gettotalresultcount-client-api-reference"></a>getTotalResultCount (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Gets the count of results found in the search control. 

## <a name="control-types-supported"></a>Control types supported

knowledge base search control

## <a name="syntax"></a>Cú pháp

```
var kbSearchControl = formContext.getControl("<name>");
var searchCount = kbSearchControl.getTotalResultCount();
```

## <a name="return-value"></a>Giá trị trả lại

**Type**: Number

**Description**: The count of the search result.
