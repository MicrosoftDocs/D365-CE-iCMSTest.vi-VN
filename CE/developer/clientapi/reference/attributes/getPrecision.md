---
title: getPrecision (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 610b9b53-9c29-4228-8ef3-0c05aae14a2b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ec134a84790968f55cb07bd53f6fb0aeba2695a0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388464"
---
# <a name="getprecision-client-api-reference"></a>getPrecision (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns the number of digits allowed to the right of the decimal point. 

## <a name="attribute-types-supported"></a>Attribute types supported

Money, decimal, double, and integer

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getPrecision()`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Number. 

**Description**: The number of digits allowed to the right of the decimal point.

### <a name="related-topics"></a>Chủ đề liên quan

[setPrecision](setPrecision.md)

