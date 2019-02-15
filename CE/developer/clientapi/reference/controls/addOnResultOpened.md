---
title: addOnResultOpened (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 5f0eabe1-985a-4e89-b23a-72657208ae7e
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7cf70763e1f6e404eb9c278797949ef80ab0fdc8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388390"
---
# <a name="addonresultopened-client-api-reference"></a>addOnResultOpened (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Adds an event handler to the [OnResultOpened](../events/onresultopened.md) event. 

## <a name="control-types-supported"></a>Control types supported

knowledge base search control

## <a name="syntax"></a>Cú pháp

```
var kbSearchControl = formContext.getControl("<name>");
kbSearchControl.addOnResultOpened(myFunction);
```

## <a name="parameters"></a>Tham số

|Tên | Loại | Bắt buộc | Mô tả|
|--|--|--|--|
|myFunction |Hàm |Có|The function to add to the **OnResultOpened** event. The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.|

### <a name="related-topics"></a>Chủ đề liên quan

[OnResultOpened event](../events/onresultopened.md)

[removeOnResultOpened](removeOnResultOpened.md)
