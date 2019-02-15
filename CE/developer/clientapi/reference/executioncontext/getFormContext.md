---
title: getFormContext (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Learn about the getFormContext method that returns a reference to the form or an item on the form depending on where the method was called.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9f3b2fed-fde5-46e4-8c59-43aa51aa82df
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8d9bf92a7f5d321b8c1dcc99091d89e3b1b7b433
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388294"
---
# <a name="getformcontext-client-api-reference"></a><span data-ttu-id="7d77e-103">getFormContext (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="7d77e-103">getFormContext (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="7d77e-104">Returns a reference to the form or an item on the form depending on where the method was called.</span><span class="sxs-lookup"><span data-stu-id="7d77e-104">Returns a reference to the form or an item on the form depending on where the method was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d77e-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="7d77e-105">Syntax</span></span>

`ExecutionContextObj.getFormContext()`

## <a name="return-value"></a><span data-ttu-id="7d77e-106">Return value</span><span class="sxs-lookup"><span data-stu-id="7d77e-106">Return value</span></span>

<span data-ttu-id="7d77e-107">**Type**: Object</span><span class="sxs-lookup"><span data-stu-id="7d77e-107">**Type**: Object</span></span>

<span data-ttu-id="7d77e-108">**Description**: Returns a reference to the form or an item on the form such as editable grid depending on where the method was called.</span><span class="sxs-lookup"><span data-stu-id="7d77e-108">**Description**: Returns a reference to the form or an item on the form such as editable grid depending on where the method was called.</span></span> <span data-ttu-id="7d77e-109">This method enables you to create common event handlers that can operate either on a form or an item on the form depending on where its called.</span><span class="sxs-lookup"><span data-stu-id="7d77e-109">This method enables you to create common event handlers that can operate either on a form or an item on the form depending on where its called.</span></span>

## <a name="example"></a><span data-ttu-id="7d77e-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="7d77e-110">Example</span></span>

<span data-ttu-id="7d77e-111">The following sample code demonstrates how you can create a method that sets notification on a form field or editable grid cell depending on where you registered the script ([Field OnChange](../events/attribute-onchange.md) event or editable grid [OnChange](../events/grid-onchange.md) event):</span><span class="sxs-lookup"><span data-stu-id="7d77e-111">The following sample code demonstrates how you can create a method that sets notification on a form field or editable grid cell depending on where you registered the script ([Field OnChange](../events/attribute-onchange.md) event or editable grid [OnChange](../events/grid-onchange.md) event):</span></span>

```JavaScript
function commonEventHandler(executionContext) {
    var formContext = executionContext.getFormContext();    
    var telephoneAttr = formContext.data.entity.attributes.getByName('telephone1');
    var isNumberWithCountryCode = telephoneAttr.getValue().substring(0,1) === '+';

    // telephoneField will be a form control if invoked from a form OnChange event;
    // telephoneField will be a editable grid GridCell object if invoked from editable grid OnChange event.
    var telephoneField = telephoneAttr.controls.getByIndex(0);

    if (!isNumberWithCountryCode) {
        telephoneField.setNotification('Please include the country code beginning with ‘+’.', 'countryCodeNotification');
    }
    else {
        telephoneField.clearNotification('countryCodeNotification');
    }
}
```


### <a name="related-topics"></a><span data-ttu-id="7d77e-112">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="7d77e-112">Related topics</span></span>
[<span data-ttu-id="7d77e-113">Execution context</span><span class="sxs-lookup"><span data-stu-id="7d77e-113">Execution context</span></span>](../execution-context.md)

[<span data-ttu-id="7d77e-114">Form context</span><span class="sxs-lookup"><span data-stu-id="7d77e-114">Form context</span></span>](../../clientapi-form-context.md)





