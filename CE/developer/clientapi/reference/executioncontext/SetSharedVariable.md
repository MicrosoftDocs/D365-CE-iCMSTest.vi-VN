---
title: setSharedVariable (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Learn about the getEventSource method that returns a reference to the form or an item on the form depending on where the method was called.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 702a13c1-f4ae-4de2-9e8b-95360ad9240c
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3a48c3169d57fb1febc97f76717943963418a8f2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385965"
---
# <a name="setsharedvariable-client-api-reference"></a>setSharedVariable (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Sets the value of a variable to be used by a handler after the current handler completes.

## <a name="syntax"></a>Cú pháp

`ExecutionContextObj.setSharedVariable(key, value)`

## <a name="parameters"></a>Tham số

- **key**: String: The name of the variable
- **Value**: Object. The values to set



## <a name="return-value"></a>Return value

**Type**: Object

**Description**: The specific type depends on what the value object is.

### <a name="related-topics"></a>Chủ đề liên quan
[getSharedVariable](getSharedVariable.md)

[Execution context](../execution-context.md)





