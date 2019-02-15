---
title: getSharedVariable (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: 5308ca4da7ef19fffee5da77a9896ee9a6f859f4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386910"
---
# <a name="getsharedvariable-client-api-reference"></a>getSharedVariable (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Retrieves a variable set using the [setSharedVariable](setSharedVariable.md) method.

## <a name="syntax"></a>Cú pháp

`ExecutionContextObj.getSharedVariable(key)`

## <a name="parameters"></a>Tham số

**khóa**

   **Type**: String

   **Description**: The name of the variable.

## <a name="return-value"></a>Return value

**Type**: Object

**Description**: The specific type depends on what the value object is.

### <a name="related-topics"></a>Chủ đề liên quan
[setSharedVariable](setSharedVariable.md)

[Execution context](../execution-context.md)





