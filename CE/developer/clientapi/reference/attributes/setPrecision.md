---
title: setPrecision (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 580aebec-c1d1-4e4a-8c20-ced859569fb2
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ddb7a8f0b9aad91f402808ae7bf60945083ada0a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387117"
---
# <a name="setprecision-client-api-reference"></a>setPrecision (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Sets the number of digits allowed to the right of the decimal point. 

## <a name="attribute-types-supported"></a>Attribute types supported

Money, decimal, double, and integer

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).setPrecision(value);`

## <a name="parameter"></a>Tham số

 Parameter Name| Loại| Mô tả  |
| --------|-----------| -----|
|giá trị| Số| Number of digits allowed to the right of the decimal point.|

### <a name="related-topics"></a>Chủ đề liên quan

[getPrecision](getPrecision.md)

