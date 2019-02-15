---
title: getInitialValue (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 56fb62e6-d357-4096-bf4c-f4c1b543d633
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7e471f87e59d5bb1d6f7974db62a278eb7086e1b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386397"
---
# <a name="getinitialvalue-client-api-reference"></a>getInitialValue (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns a value that represents the value set for a **Boolean**, **OptionSet** or **MultiSelectOptionSet** attribute when the form is opened.

## <a name="attribute-types-supported"></a>Attribute types supported

Boolean, OptionSet, MultiSelectOptionSet 

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getInitialValue()`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Number

**Description**: The initial value for the attribute.


