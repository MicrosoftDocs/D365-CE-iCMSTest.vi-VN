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
# <a name="getattribute-client-api-reference"></a><span data-ttu-id="725cb-102">getAttribute (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="725cb-102">getAttribute (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="725cb-103">Returns the attribute that the control is bound to.</span><span class="sxs-lookup"><span data-stu-id="725cb-103">Returns the attribute that the control is bound to.</span></span>

<span data-ttu-id="725cb-104">Controls that aren’t bound to an attribute (subgrid, web resource, and IFRAME) don’t have this method.</span><span class="sxs-lookup"><span data-stu-id="725cb-104">Controls that aren’t bound to an attribute (subgrid, web resource, and IFRAME) don’t have this method.</span></span> <span data-ttu-id="725cb-105">An error will be thrown if you attempt to use this method on one of these controls.</span><span class="sxs-lookup"><span data-stu-id="725cb-105">An error will be thrown if you attempt to use this method on one of these controls.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="725cb-106">Control types supported</span><span class="sxs-lookup"><span data-stu-id="725cb-106">Control types supported</span></span>

<span data-ttu-id="725cb-107">Standard, Lookup, OptionSet</span><span class="sxs-lookup"><span data-stu-id="725cb-107">Standard, Lookup, OptionSet</span></span>

## <a name="syntax"></a><span data-ttu-id="725cb-108">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="725cb-108">Syntax</span></span>

`formContext.getControl(arg).getAttribute();`

## <a name="return-value"></a><span data-ttu-id="725cb-109">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="725cb-109">Return Value</span></span>

<span data-ttu-id="725cb-110">**Type**: Object</span><span class="sxs-lookup"><span data-stu-id="725cb-110">**Type**: Object</span></span>

<span data-ttu-id="725cb-111">**Description**: An attribute</span><span class="sxs-lookup"><span data-stu-id="725cb-111">**Description**: An attribute</span></span>

## <a name="remarks"></a><span data-ttu-id="725cb-112">Chú thích</span><span class="sxs-lookup"><span data-stu-id="725cb-112">Remarks</span></span>

<span data-ttu-id="725cb-113">The constituent controls within a [quick view control](../formContext-ui-quickForms.md) are included in the controls collection and these controls have the **getAttribute** method.</span><span class="sxs-lookup"><span data-stu-id="725cb-113">The constituent controls within a [quick view control](../formContext-ui-quickForms.md) are included in the controls collection and these controls have the **getAttribute** method.</span></span> <span data-ttu-id="725cb-114">However, the attribute is not part of the attribute collection for the entity.</span><span class="sxs-lookup"><span data-stu-id="725cb-114">However, the attribute is not part of the attribute collection for the entity.</span></span> <span data-ttu-id="725cb-115">While you can retrieve the value for that attribute using [getValue](getValue.md) and even change the value using [setValue](setValue.md), changes you make will not be saved with the entity.</span><span class="sxs-lookup"><span data-stu-id="725cb-115">While you can retrieve the value for that attribute using [getValue](getValue.md) and even change the value using [setValue](setValue.md), changes you make will not be saved with the entity.</span></span>
 
<span data-ttu-id="725cb-116">The following code shows using the value the contact **mobilephone** attribute when displayed on an account entity form using a quick view control named **contactQuickForm**.</span><span class="sxs-lookup"><span data-stu-id="725cb-116">The following code shows using the value the contact **mobilephone** attribute when displayed on an account entity form using a quick view control named **contactQuickForm**.</span></span> <span data-ttu-id="725cb-117">This code hides the control when the value of the attribute is **null**.</span><span class="sxs-lookup"><span data-stu-id="725cb-117">This code hides the control when the value of the attribute is **null**.</span></span>

```JavaScript
var quickViewMobilePhoneControl = formContext.getControl("contactQuickForm_contactQuickForm_contact_mobilephone");
if (quickViewMobilePhoneControl.getAttribute().getValue() == null) {
    quickViewMobilePhoneControl.setVisible(false);
}
```


[<span data-ttu-id="725cb-118">Quick view control</span><span class="sxs-lookup"><span data-stu-id="725cb-118">Quick view control</span></span>](../formContext-ui-quickForms.md)

[<span data-ttu-id="725cb-119">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="725cb-119">Attributes</span></span>](../attributes.md)


