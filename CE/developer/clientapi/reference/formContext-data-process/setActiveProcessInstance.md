---
title: setActiveProcessInstance (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: c01a9445-00b6-4152-a482-df830f91a3ea
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 26492510b322dae7ad8edca1639c7ac19615d78f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387336"
---
# <a name="setactiveprocessinstance-client-api-reference"></a>setActiveProcessInstance (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setActiveProcessInstance-description.md](./includes/setActiveProcessInstance-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.process.setActiveProcessInstance(processInstanceId, callbackFunction);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|processInstanceId|Chuỗi|Có|The Id of the process instance to set as the active instance.|
|callbackFunction|Hàm|Không|A function to call when the operation is complete. This callback function is passed one of the following string values to indicate whether the operation succeeded:<br/>- **success**: The operation succeeded.<br/>- **invalid**: The processInstanceId isn’t valid or the process isn’t enabled.|

### <a name="related-topics"></a>Chủ đề liên quan

[getProcessInstances](getProcessInstances.md)

[formContext.data.process](../formContext-data-process.md)
 


