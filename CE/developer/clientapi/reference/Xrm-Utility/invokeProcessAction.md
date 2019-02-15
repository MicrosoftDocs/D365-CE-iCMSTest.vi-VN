---
title: invokeProcessAction (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: e71012ba-249d-4ae7-8891-f7d3ae16a20a
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5091cc9650de3ea4a9ae739dc6fa2adff88877cd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387439"
---
# <a name="invokeprocessaction-client-api-reference"></a>invokeProcessAction (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/invokeProcessAction-description.md](./includes/invokeProcessAction-description.md)] 

For more information about actions, see [Actions overview](../../../../customize/actions.md)

## <a name="syntax"></a>Cú pháp

`Xrm.Utility.invokeProcessAction(name,parameters).then(successCallback, errorCallback)`

## <a name="parameters"></a>Tham số

|Tên |Loại |Bắt buộc |Mô tả |
|---|---|---|---|
|tên|Chuỗi|Có|Name of the process action to invoke.|
|parameters|đối tượng|Không|An object containing input parameters for the action. You define an object using `key:value` pairs of items, where `key` is of **String** type.|
|successCallback |Hàm |Có |A function to call when the action is invoked.  |
|errorCallback |Hàm |Có |A function to call when the operation fails.  |

## <a name="returns"></a>Returns

On success, returns Web API result along with any action output.

### <a name="related-topics"></a>Chủ đề liên quan

[Tổng quan về các tác vụ](../../../../customize/actions.md)

[Xrm.Utility](../xrm-utility.md)


