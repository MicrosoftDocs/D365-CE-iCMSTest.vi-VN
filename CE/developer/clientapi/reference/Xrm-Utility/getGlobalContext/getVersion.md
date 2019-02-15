---
title: getVersion (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 2fd5c43e-5a01-431d-ac2c-abefdb8d06ac
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b7be6e9f4ab3680849063197daa8aeb6d715b8f2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388446"
---
# <a name="getversion-client-api-reference"></a>getVersion (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns the version number of the Dynamics 365 for Customer Engagement apps instance.

## <a name="syntax"></a>Cú pháp

```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.getVersion();
``` 
## <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: Version of the Customer Engagement instance. Ví dụ:

`"9.0.0.1103"`

### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.Utility.getGlobalContext](../getGlobalContext.md)
