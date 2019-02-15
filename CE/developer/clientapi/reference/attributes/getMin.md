---
title: getMin (Client API reference)| MicrosoftDocs
ms.date: 08/13/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9a04b52a-2bc7-4572-bd3e-8b9622602092
author: KumarVivek
ms.author: kvivek
manager: annbe
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d51a312f433d2565d21088fe17c479beea485008
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388320"
---
# <a name="getmin-client-api-reference"></a>getMin (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns a number indicating the minimum allowed value for an attribute. 

## <a name="attribute-types-supported"></a>Attribute types supported

Decimal, integer, double, money

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getMin()`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Number. 

**Description**: The minimum allowed value for the attribute.

