---
title: addOnPostSearch (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: c398dbca-0ead-487a-8a92-35b1f2953bf6
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fd6e6f9426297f8424916a5a5020b6c787325cd1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388439"
---
# <a name="removeonpostsearch-client-api-reference"></a>removeOnPostSearch (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Removes an event handler from the [PostSearch](../events/postsearch.md) event. 

## <a name="control-types-supported"></a>Control types supported

knowledge base search control

## <a name="syntax"></a>Cú pháp

```
var kbSearchControl = formContext.getControl("<name>";
kbSearchControl.removeOnPostSearch(myFunction);
```

## <a name="parameters"></a>Tham số

|Tên | Loại | Bắt buộc | Mô tả|
|--|--|--|--|
|myFunction |Hàm |Có|The function to remove from the **PostSearch** event.| 

### <a name="related-topics"></a>Chủ đề liên quan

[PostSearch event](../events/postsearch.md)

[addOnPostSearch](addOnPostSearch.md) 


