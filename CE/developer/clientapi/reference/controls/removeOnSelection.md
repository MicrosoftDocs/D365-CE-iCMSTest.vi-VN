---
title: removeOnSelection (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 3ca41e3e-af2b-4aa8-8233-64a8c276d0ef
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2bd8b1034dba9659b388ae9b0954966633a763a7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386526"
---
# <a name="removeonselection-client-api-reference"></a>removeOnSelection (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Removes an event handler from the [OnSelection](../events/onselection.md) event. 

## <a name="control-types-supported"></a>Control types supported

Điều khiển tìm kiếm cơ sở Kiến thức

## <a name="syntax"></a>Cú pháp

```
var kbSearchControl = formContext.getControl("<name>");
kbSearchControl.removeOnSelection(myFunction);
```

## <a name="parameters"></a>Tham số

|Tên | Loại | Bắt buộc | Mô tả|
|--|--|--|--|
|myFunction |Hàm |Có|The function to remove from the **OnSelection** event.| 

### <a name="related-topics"></a>Chủ đề liên quan

[addOnSelection](addOnSelection.md)


