---
title: Client API execution context in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: conceptual
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1fcbf0fd-4e47-4352-a555-9315f7e57331
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d4df59501df501cab84a0e7cbe749df7dbf695a5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385465"
---
# <a name="execution-context-client-api-reference"></a>Execution context (Client API reference)

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

The execution context defines the event context in which your code executes. More information: [Client API execution context](../clientapi-execution-context.md).

The execution context object provides the following methods.

|Phương pháp |Mô tả |
|---|---|
|[getDepth](executioncontext/getDepth.md)|Returns a value that indicates the order in which this handler is executed.|
|[getEventArgs](executioncontext/getEventArgs.md)|Returns an object with methods to manage the **OnSave** event.|
|[getEventSource](executioncontext/getEventSource.md)|Returns a reference to the object that the event occurred on.|
|[getFormContext](executioncontext/getFormContext.md)|Returns a reference to the form or an item on the form depending on where the method was called.|
|[getSharedVariable](executioncontext/getSharedVariable.md)|Retrieves a variable set using the [setSharedVariable](executioncontext/setSharedVariable.md) method.|
|[setSharedVariable](executioncontext/setSharedVariable.md)|Sets the value of a variable to be used by a handler after the current handler completes.|

### <a name="related-topics"></a>Chủ đề liên quan

[Client API execution context](../clientapi-execution-context.md)

[Save event arguments](save-event-arguments.md)

[Understand Client API object model](../understand-clientapi-object-model.md) 

