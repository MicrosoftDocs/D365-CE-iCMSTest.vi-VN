---
title: getText (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 649fe7b0-016d-409f-ba3c-b14e0f1953e0
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0fcbb426cf8a30d6ca918934c030d3ef84805f60
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387036"
---
# <a name="gettext-client-api-reference"></a>getText (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns a string value of the text for the currently selected option for an **optionset** or **multiselectoptionset** attribute. 

## <a name="attribute-types-supported"></a>Attribute types supported

optionset, multiselectoptionset

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getText()`

## <a name="return-value"></a>Giá trị trả lại

**Type**: String. 

**Description**: The **text** value of the selected option.

### <a name="related-topics"></a>Chủ đề liên quan
[getInitialValue (Client API reference)](getInitialValue.md)

[getOption (Client API reference)](getOption.md)

[getOptions (Client API reference)](getOptions.md)

[getSelectedOption (Client API reference)](getSelectedOption.md) 


