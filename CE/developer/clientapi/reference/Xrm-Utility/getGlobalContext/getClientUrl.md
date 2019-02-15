---
title: getClientUrl (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
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
ms.openlocfilehash: c8601dc7540bf43c4867f4e57a49bc46b92e9e5f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387585"
---
# <a name="getclienturl-client-api-reference"></a>getClientUrl (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns the base URL that was used to access the application.

## <a name="syntax"></a>Cú pháp

```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.getClientUrl();
``` 

## <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: The values returned will resemble those listed in the following table.


|             Value              |                                    Máy khách                                     |
|--------------------------------|-------------------------------------------------------------------------------|
| https://[org].crm.dynamics.com |                   Ứng dụng Dynamics 365 for Customer Engagement                   |
|    http(s)://[server]/[org]    |                Dynamics 365 for Customer Engagement (on-premises) apps                |
|     http://localhost:2525      | Dynamics 365 for Outlook with Offline Access when offline |

### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.Utility.getGlobalContext](../getGlobalContext.md)