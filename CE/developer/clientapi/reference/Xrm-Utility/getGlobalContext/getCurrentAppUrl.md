---
title: getCurrentAppUrl (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 89123cde-7c66-4c7d-94e4-e287285019f8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4e45a90c0aad12598388f322a57bd53f3f41b6a0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388403"
---
# <a name="getcurrentappurl-client-api-reference"></a>getCurrentAppUrl (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns the URL of the current business app in Customer Engagement.

## <a name="syntax"></a>Cú pháp

```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.getCurrentAppUrl();
``` 

## <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: URL of the current business app. Possible return values:

|Value |Máy khách |
|---|---|
|https://[org].crm.dynamics.com/main.aspx?appid=[GUID]|Dynamics 365 for Customer Engagement apps |
|https://[server]/[org]/main.aspx?appid=[GUID]|Dynamics 365 for Customer Engagement (on-premises) apps |

### <a name="related-topics"></a>Chủ đề liên quan

[Create and manage custom business apps using code](../../../../create-manage-custom-business-apps-using-code.md)

[Xrm.Utility.getGlobalContext](../getGlobalContext.md) 