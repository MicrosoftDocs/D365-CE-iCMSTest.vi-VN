---
title: setRequiredLevel (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 67a96fc4-4d65-4858-90da-f41eeba0365a
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3ec91975dbd973b1ae630bc9e4c68e1be2b8de6a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388185"
---
# <a name="setrequiredlevel-client-api-reference"></a>setRequiredLevel (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Sets whether data is required or recommended for the attribute before the record can be saved.

> [!IMPORTANT]
> Reducing the required level of an attribute can cause an error when the page is saved. If the attribute is required by the server, an error will occur if there is no value for the attribute. 

## <a name="attribute-types-supported"></a>Attribute types supported

Tất cả

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).setRequiredLevel(requirementLevel)`

## <a name="parameters"></a>Tham số

**Type**: String. 

**Description**: Set the level to one of the following values:
- không
- required
- recommended

### <a name="related-topic"></a>Related topic
[getRequiredLevel (Client API reference)](getRequiredLevel.md)


