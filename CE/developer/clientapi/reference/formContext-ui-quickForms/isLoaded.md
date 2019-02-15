---
title: isLoaded (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1870151d-6029-4733-ac35-6ee4d43f9553
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8b8f77f51b96e8e8420b6a6d64cda4379f4dc6aa
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386399"
---
# <a name="isloaded-client-api-reference"></a>isLoaded (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/isLoaded-description.md](./includes/isLoaded-description.md)]

## <a name="syntax"></a>Cú pháp

`quickViewControl.isLoaded();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean.

**Description**: true is the data binding for a constituent control is complete; false otherwise. 

## <a name="remarks"></a>Chú thích

The data binding for the constituent controls in a quick view control may not be complete during the main form **OnLoad** event because the quick view form that the control is bound to may not have loaded completely. As a result, using the [getAttribute](../controls/getattribute.md) or any data-related methods on a constituent control might not work. The **isLoaded** method for the quick view control helps determine the data binding status for constituent controls in a quick view control.

## <a name="example"></a>Ví dụ

The following sample code demonstrates how you can use the **isLoaded** method to check the binding status, and then retrieve the value of the attribute that a constituent control in a quick view control is bound to.

```JavaScript
function getAttributeValue(executionContext) {
    var formContext = executionContext.getFormContext();
    var quickViewControl = formContext.ui.quickForms.get("<QuickViewControlName>");
    if (quickViewControl != undefined) {
        if (quickViewControl.isLoaded()) {
            // Access the value of the attribute bound to the constituent control
            var myValue = quickViewControl.getControl(0).getAttribute().getValue();
            console.log(myValue);
            return;
        }
        else {
            // Wait for some time and check again
            setTimeout(getAttributeValue, 10);
        }
    }
    else {
        console.log("No data to display in the quick view control.");
        return;
    }
}
```

### <a name="related-topics"></a>Chủ đề liên quan

[formContext.ui.quickForms](../formContext-ui-quickForms.md)
