---
title: getRequiredLevel (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: c0b6ea26-2a11-4a49-8ecf-fe700e782bf3
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6b6ee7539e0a0849856ed59e641ef5f0eb53fede
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387872"
---
# <a name="getrequiredlevel-client-api-reference"></a>getRequiredLevel (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns a string value indicating whether a value for the attribute is required or recommended. 

## <a name="attribute-types-supported"></a>Attribute types supported

Tất cả

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getRequiredLevel()`

## <a name="return-value"></a>Giá trị trả lại

**Type**: String. 

**Description**: Returns one of the following values:
- không
- required
- recommended

### <a name="related-topic"></a>Related topic
[setRequiredLevel (Client API reference)](setRequiredLevel.md)
