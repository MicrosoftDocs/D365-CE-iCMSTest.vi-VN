---
title: getCurrentAppName (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: a8f83718-41a4-4958-a5ac-9b28cc2f8dba
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 003d4fd5fafd37e2ccca51851e4e041cf1fae2d7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387728"
---
# <a name="getcurrentappname-client-api-reference"></a>getCurrentAppName (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns the name of the current business app in Customer Engagement.

## <a name="syntax"></a>Cú pháp

```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.getCurrentAppName().then(successCallback, errorCallback);
``` 

## <a name="parameters"></a>Tham số

|Tên |Loại |Bắt buộc |Mô tả |
|---|---|---|---|
|successCallback |Hàm |Có |A function to call when the business app name is returned.  |
|errorCallback |Hàm |Có |A function to call when the operation fails.  |

## <a name="return-value"></a>Giá trị trả lại

If this method is called in the context of a business app, returns the name of the business app. Otherwise, it fails with an error.

### <a name="related-topics"></a>Chủ đề liên quan

[Create and manage custom business apps using code](../../../../create-manage-custom-business-apps-using-code.md)

[Xrm.Utility.getGlobalContext](../getGlobalContext.md)


