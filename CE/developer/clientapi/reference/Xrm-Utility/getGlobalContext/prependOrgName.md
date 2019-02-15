---
title: prependOrgName (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 89123cde-7c66-4c7d-94e4-e287285019f8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3bde3c4599793ca48b34249e949838d1844cccab
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386980"
---
# <a name="prependorgname-client-api-reference"></a>prependOrgName (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

Prefixes the current organization's unique name to a string, typically a URL path.

## <a name="syntax"></a>Cú pháp

 ```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.prependOrgName(sPath);
```

## <a name="parameters"></a>Tham số

|Tên |Loại |Bắt buộc |Mô tả |
|---|---|---|---|
|sPath |Chuỗi |Có |A local path to a resource. |

## <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: A path string with the organization name prefixed in the following format:

`"/"+ orgName + sPath`

### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.Utility.getGlobalContext](../getGlobalContext.md)


