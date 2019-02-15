---
title: getSubmitMode (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: a3231438-3821-4dce-b118-d63e6ce85e01
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 05805855194ce259d855c06cf05a695ea5ad818e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388768"
---
# <a name="getsubmitmode-client-api-reference"></a>getSubmitMode (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns a string indicating when data from the attribute will be submitted when the record is saved. 

## <a name="attribute-types-supported"></a>Attribute types supported

Tất cả

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getSubmitMode()`

## <a name="return-value"></a>Giá trị trả lại

**Type**: String. 

**Description**: Returns one of the following values:
- always
- never
- dirty

### <a name="related-topic"></a>Related topic
[setSubmitMode (Client API reference)](setSubmitMode.md)

