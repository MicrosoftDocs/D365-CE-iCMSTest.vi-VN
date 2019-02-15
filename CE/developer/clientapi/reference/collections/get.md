---
title: get method for collections (Client API reference) in Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4d025f92-db16-440c-9f82-e40d71e09862
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: edef3ef6934fecb254295f900b82590ae5d5f8f7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387786"
---
# <a name="get-method-for-collections-client-api-reference"></a>get method for collections (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/get-description.md](./includes/get-description.md)]

## <a name="syntax"></a>Cú pháp

`collection.get([String][Number][delegate function(attribute, index)])`

## <a name="parameters"></a>Tham số

|Tham số  |Return value |Loại trả về  |
|---------|------|-------|
|Không có  |All the objects in the collection  |Mảng|
|Chuỗi  |The object where the name matches the argument<br/><br/>The objects returned in the **formContext.data.process** namespace don’t contain names. So, using the string parameter for this method returns no objects.  |Đối tượng|
|Số  |The object where the index matches the number  |Đối tượng|
|delegate function(attribute, index)  |Any objects that cause the delegate function to return **true**.  |Mảng|


### <a name="related-topics"></a>Chủ đề liên quan
[Collections in Client API](../collections.md)

[forEach](forEach.md)

[getLength](getLength.md)

