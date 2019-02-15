---
title: getProcessInstances (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 12/04/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4ed6c991-59c9-4a69-90d4-635f3f1d397b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4e876e591eb117ebbb5beb937328456e5d29bfb2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387689"
---
# <a name="getprocessinstances-client-api-reference"></a>getProcessInstances (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getProcessInstances-description.md](./includes/getProcessInstances-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.process.getProcessInstances(callbackFunction(object));`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|callbackFunction|Hàm|Có|The callback function is passed an object with the following attributes and their corresponding values as the key: value pair. All returned values are of String type except for **CreatedOnDate**, which is of [Date](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date) type. <br/>- CreatedOn (deprecated)<br/>- CreatedOnDate<br/>- ProcessDefinitionID<br/>- ProcessDefinitionName<br/>- ProcessInstanceID<br/>- ProcessInstanceName<br/>- StatusCodeName<br/><br/>The process instances are filtered according to the user’s privileges.|

### <a name="related-topics"></a>Chủ đề liên quan

[setActiveProcessInstance](setActiveProcessInstance.md)

[formContext.data.process](../formContext-data-process.md)
 


