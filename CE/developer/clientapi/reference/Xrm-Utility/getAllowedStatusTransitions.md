---
title: getAllowedStatusTransitions (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 28c36741-0070-435c-a42f-49f4dda2ef7f
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 27d5582aecc1566ef588f0af0cb8a1b61b601b0d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387586"
---
# <a name="getallowedstatustransitions-client-api-reference"></a>getAllowedStatusTransitions (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getAllowedStatusTransitions-description.md](./includes/getAllowedStatusTransitions-description.md)] 

## <a name="syntax"></a>Cú pháp

`Xrm.Utility.getAllowedStatusTransitions(entityName,stateCode).then(successCallback, errorCallback)`

## <a name="parameters"></a>Tham số

|Tên |Loại |Bắt buộc |Mô tả |
|---|---|---|---|
|entityName|Chuỗi|Có|The logical name of the entity.|
|stateCode|Số|Có|The state code to find out the allowed status transition values.|
|successCallback|Hàm|Không|The function to execute when the operation succeeds.|
|errorCallback|Hàm|Không|The function to execute when the operation fails.|


### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.Utility](../xrm-utility.md)



