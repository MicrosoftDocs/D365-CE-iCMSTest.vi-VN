---
title: getCurrentAppProperties (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 5f8d91ff-ba0d-4e90-a79a-18e32d09baa3
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 35b704bc1065da802f4d4da4223ed316b6d157e4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387526"
---
# <a name="getcurrentappproperties-client-api-reference"></a>getCurrentAppProperties (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns the properties of the current business app in Customer Engagement.

## <a name="syntax"></a>Cú pháp

```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.getCurrentAppProperties().then(successCallback, errorCallback);
``` 

## <a name="parameters"></a>Tham số

|Tên |Loại |Bắt buộc |Mô tả |
|---|---|---|---|
|successCallback |Hàm |Có |A function to call when the business app property information is returned. An object with the following attributes (app properties) is passed to the function :<br/>- **appId**<br/>- **displayName**<br/>- **uniqueName**<br/>- **url**<br/>- **webResourceId**<br/>- **webResourceName**<br/>- **welcomePageId**<br/>- **welcomePageName**|
|errorCallback |Hàm |Có |A function to call when the operation fails.  |

## <a name="return-value"></a>Giá trị trả lại

If this method is called in the context of a business app, returns the properties of the business app. Otherwise, it fails with an error.

### <a name="related-topics"></a>Chủ đề liên quan

[Create and manage custom business apps using code](../../../../create-manage-custom-business-apps-using-code.md)

[Xrm.Utility.getGlobalContext](../getGlobalContext.md) 



