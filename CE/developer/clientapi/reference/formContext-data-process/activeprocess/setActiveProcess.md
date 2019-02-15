---
title: setActiveProcess (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 0d4c2d8a-a2fb-4cdd-9153-041646068992
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9f6cfd47887dae13464a0563680aa78c16d82275
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386243"
---
# <a name="setactiveprocess-client-api-reference"></a>setActiveProcess (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setActiveProcess-description.md](./includes/setActiveProcess-description.md)]

If there is an active instance of the process, the entity record is loaded with the process instance ID. If there is no active instance of the process, a new process instance is created and the entity record is loaded with the process instance ID. If there are multiple instances of the current process, the record is loaded with the first instance of the active process as per the defaulting logic, that is the most recently used process instance per user.

## <a name="syntax"></a>Cú pháp

`formContext.data.process.setActiveProcess(processId, callbackFunction);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|processInstanceId|Chuỗi|Có|The Id of the process to set as the active process.|
|callbackFunction|Hàm|Không|A function to call when the operation is complete. This callback function is passed one of the following string values to indicate whether the operation succeeded:<br/>- **success**: The operation succeeded.<br/>- **invalid**: The processId isn’t valid or the process isn’t enabled.|

### <a name="related-topics"></a>Chủ đề liên quan

[getActiveProcess](getActiveProcess.md)

[setActiveProcessInstance](../setActiveProcessInstance.md)

[formContext.data.process](../../formContext-data-process.md)
 


