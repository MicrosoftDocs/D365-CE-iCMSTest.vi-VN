---
title: removePreSearch (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 2451c4ac-527c-4487-8f52-bde1690c5bde
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c96c3dbe2fcbfedcb5a24193b22657bd4313310d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385702"
---
# <a name="removepresearch-client-api-reference"></a>removePreSearch (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Removes event handler functions that have previously been set for the [PreSearch](../events/PreSearch.md) event.

## <a name="control-types-supported"></a>Control types supported

Tra cứu

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).removePreSearch(myFunction)`

## <a name="parameters"></a>Tham số

|Tên | Loại | Bắt buộc | Mô tả|
|--|--|--|--|
|myFunction |Hàm |Có| The function to remove. The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.|

### <a name="related-topics"></a>Chủ đề liên quan

[PreSearch event](../events/PreSearch.md)

[addPreSearch](addPreSearch.md) 


