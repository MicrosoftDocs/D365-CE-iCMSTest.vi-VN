---
title: getOptions (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 83347491-68d2-4844-bda4-0cd0abde2edf
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2b358d63ee252b63c218bc930094bd79137a4421
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385624"
---
# <a name="getoptions-client-api-reference"></a>getOptions (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns an array of option objects representing valid options for an attribute. 

## <a name="attribute-types-supported"></a>Attribute types supported

OptionSet, MultiSelectOptionSet

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getOptions()`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Array of option objects. 

**Description**: The array of option objects representing valid options.

