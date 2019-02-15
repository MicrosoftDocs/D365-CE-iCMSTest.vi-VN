---
title: addOnSelection (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 66cfb2ff-4d78-4bb9-8dc0-e214ae1d2880
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0af1072cfee4d775d683a2bb8ff6ebdeaeb9ffd1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386563"
---
# <a name="addonselection-client-api-reference"></a>addOnSelection (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Adds an event handler to the [OnSelection](../events/onselection.md) event. 

## <a name="control-types-supported"></a>Control types supported

Knowledge base search control

## <a name="syntax"></a>Cú pháp

```
var kbSearchControl = formContext.getControl("<name>");
kbSearchControl.addOnSelection(myFunction);
```

## <a name="parameters"></a>Tham số

|Tên | Loại | Bắt buộc | Mô tả|
|--|--|--|--|
|myFunction |Hàm |Có|The function to add to the **OnSelection** event. The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.|

### <a name="related-topics"></a>Chủ đề liên quan

[OnSelection event](../events/onselection.md)

[removeOnSelection](removeOnSelection.md)
