---
title: Xrm.Device| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: ce572df6-aae6-431a-aa95-73eee544c7e9
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 22974db8a8f8a051e863cc5478583e5f98136acf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386307"
---
# <a name="getselectedoption-client-api-reference"></a>getSelectedOption (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns the option object or an array of option objects selected in an **optionset** or **multiselectoptionset** attribute respectively. 

## <a name="attribute-types-supported"></a>Attribute types supported

optionset, multiselectoptionset

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getSelectedOption()`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Option object for optionset; array of option objects for multiselectoptionset. 

**Description**: Returns the object with text and value properties.

### <a name="related-topics"></a>Chủ đề liên quan
[getInitialValue (Client API reference)](getInitialValue.md)

[getOption (Client API reference)](getOption.md)

[getOptions (Client API reference)](getOptions.md)

[getText (Client API reference)](getText.md)

