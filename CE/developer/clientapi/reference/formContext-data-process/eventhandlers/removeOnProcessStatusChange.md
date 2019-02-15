---
title: removeOnProcessStatusChange (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 5e41f59e-ddb3-4d47-b45b-454aa9e04439
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 66a48419d85a1c303f89a5d4214fd2adb99741a1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387319"
---
# <a name="removeonprocessstatuschange-client-api-reference"></a>removeOnProcessStatusChange (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/removeOnProcessStatusChange-description.md](./includes/removeOnProcessStatusChange-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.process.removeOnProcessStatusChange(myFunction);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|myFunction|Function reference|Có|The function to be removed from the [OnProcessStatusChange](../../events/onprocessstatuschange.md) event.|

### <a name="related-topics"></a>Chủ đề liên quan

[addOnProcessStatusChange](addOnProcessStatusChange.md)
 
[formContext.data.process](../../formContext-data-process.md)
 


