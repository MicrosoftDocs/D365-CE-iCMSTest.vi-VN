---
title: getMax (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 6bcd4b47-b3b6-4a9c-899f-a5dce4cbab51
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 1cd7ca2a9c9874b9a15fe0869f4f8f566f3f2542
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388811"
---
# <a name="getmax-client-api-reference"></a>getMax (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns a number indicating the maximum allowed value for an attribute. 

## <a name="attribute-types-supported"></a>Attribute types supported

decimal, integer, double, money

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getMax()`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Number. 

**Description**: The maximum allowed value for the attribute.

