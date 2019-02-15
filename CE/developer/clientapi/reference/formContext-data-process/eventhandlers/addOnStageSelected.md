---
title: addOnStageSelected (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 5982770c-d5a4-415a-a32d-3734b6210bb9
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6a4089ec83ef62f72f4abcdca313ee855daa8a83
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388384"
---
# <a name="addonstageselected-client-api-reference"></a>addOnStageSelected (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/addOnStageSelected-description.md](./includes/addOnStageSelected-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.process.addOnStageSelected(myFunction);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|myFunction|Function reference|Có|The function to be executed when the business process flow stage is selected. The function will be added to the bottom of the event handler pipeline. The execution context is automatically passed as the first parameter to the function. See [Execution context](../../../clientapi-execution-context.md) for more information.<br/><br/>You should use a reference to a named function rather than an anonymous function if you may later want to remove the event handler.|

### <a name="related-topics"></a>Chủ đề liên quan

[removeOnStageSelected](removeOnStageSelected.md)
 
[formContext.data.process](../../formContext-data-process.md)
 


