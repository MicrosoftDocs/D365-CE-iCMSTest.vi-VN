---
title: addOnPostSearch (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/04/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9d000628-5dbe-45bd-9c47-e19187ffdae7
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bbed161a94b47159aa4e47003f1ad153fbc623dd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388393"
---
# <a name="addonpostsearch-client-api-reference"></a>addOnPostSearch (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Adds an event handler to the [PostSearch](../events/postsearch.md) event. 

## <a name="control-types-supported"></a>Control types supported

knowledge base search control

## <a name="syntax"></a>Cú pháp

```
var kbSearchControl = formContext.getControl("<name>");
kbSearchControl.addOnPostSearch(myFunction);
```

## <a name="parameters"></a>Tham số

|Tên | Loại | Bắt buộc | Mô tả|
|--|--|--|--|
|myFunction |Hàm |Có|The function to add to the **PostSearch** event. The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.| 

### <a name="related-topics"></a>Chủ đề liên quan

[PostSearch event](../events/postsearch.md)

[removeOnPostSearch](removeOnPostSearch.md)
