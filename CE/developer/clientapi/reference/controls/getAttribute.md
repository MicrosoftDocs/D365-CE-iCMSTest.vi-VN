---
title: getAttribute (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 5ba037da-59f3-4e10-80f8-4e46d5410f81
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 617c1eb19b1206587d8a0501e6022ac932d56b9b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387498"
---
# <a name="getattribute-client-api-reference"></a>getAttribute (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns the attribute that the control is bound to.

Controls that aren’t bound to an attribute (subgrid, web resource, and IFRAME) don’t have this method. An error will be thrown if you attempt to use this method on one of these controls. 

## <a name="control-types-supported"></a>Control types supported

Standard, Lookup, OptionSet

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).getAttribute();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Object

**Description**: An attribute

## <a name="remarks"></a>Chú thích

The constituent controls within a [quick view control](../formContext-ui-quickForms.md) are included in the controls collection and these controls have the **getAttribute** method. However, the attribute is not part of the attribute collection for the entity. While you can retrieve the value for that attribute using [getValue](getValue.md) and even change the value using [setValue](setValue.md), changes you make will not be saved with the entity.
 
The following code shows using the value the contact **mobilephone** attribute when displayed on an account entity form using a quick view control named **contactQuickForm**. This code hides the control when the value of the attribute is **null**.

```JavaScript
var quickViewMobilePhoneControl = formContext.getControl("contactQuickForm_contactQuickForm_contact_mobilephone");
if (quickViewMobilePhoneControl.getAttribute().getValue() == null) {
    quickViewMobilePhoneControl.setVisible(false);
}
```


[Quick view control](../formContext-ui-quickForms.md)

[Thuộc tính](../attributes.md)


