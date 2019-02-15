---
title: addOnStageChange (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: d18136d2-a3cf-4440-8e6b-1703594acd79
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ee4f5a4b29772eb3d2c63060537951731032781c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388306"
---
# <a name="addonstagechange-client-api-reference"></a>addOnStageChange (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/addOnStageChange-description.md](./includes/addOnStageChange-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.process.addOnStageChange(myFunction);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|myFunction|Function reference|Có|The function to be executed when the business process flow stage changes. The function will be added to the bottom of the event handler pipeline. The execution context is automatically passed as the first parameter to the function. See [Execution context](../../../clientapi-execution-context.md) for more information.<br/><br/>You should use a reference to a named function rather than an anonymous function if you may later want to remove the event handler.|

### <a name="related-topics"></a>Chủ đề liên quan
 
[removeOnStageChange](removeOnStageChange.md)

[formContext.data.process](../../formContext-data-process.md)
 


