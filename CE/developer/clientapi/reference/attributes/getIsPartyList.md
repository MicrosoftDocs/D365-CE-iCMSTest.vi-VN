---
title: getIsPartyList (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 487d0923-9675-4308-b88e-fdbf91853a98
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f899aee0c52999dd99c70a7e7fbd6db28e71f57f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387668"
---
# <a name="getispartylist-client-api-reference"></a>getIsPartyList (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns a Boolean value indicating whether the lookup represents a partylist lookup. Partylist lookups allow for multiple records to be set, such as the **To:** field for an email entity record.

## <a name="attribute-types-supported"></a>Attribute types supported

Tra cứu

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getIsPartyList()`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean. 

**Description**: True if the lookup attribute is a partylist, otherwise false.

