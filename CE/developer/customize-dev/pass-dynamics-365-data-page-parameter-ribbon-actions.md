---
title: Pass Customer Engagement data from a page as a parameter to Ribbon actions (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'The topic describes options for using the <CrmParameter> element to retrieve these values. '
ms.custom: ''
ms.date: 01/22/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- ribbon, pass data to
ms.assetid: 15245f11-a7e6-445a-8f18-06765268f1ad
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a74ebc6998e93778159ea359ffca9e7adc02b1d3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388476"
---
# <a name="pass-customer-engagement-data-from-a-page-as-a-parameter-to-ribbon-actions"></a><span data-ttu-id="c090a-103">Pass Customer Engagement data from a page as a parameter to ribbon actions</span><span class="sxs-lookup"><span data-stu-id="c090a-103">Pass Customer Engagement data from a page as a parameter to ribbon actions</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c090a-104">When you define an action in a ribbon, you frequently have to pass data from the page to either a [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] function or a URL.</span><span class="sxs-lookup"><span data-stu-id="c090a-104">When you define an action in a ribbon, you frequently have to pass data from the page to either a [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] function or a URL.</span></span> <span data-ttu-id="c090a-105">This topic describes options for using the [\<CrmParameter\>](https://msdn.microsoft.com/library/gg309332.aspx) element to retrieve these values.</span><span class="sxs-lookup"><span data-stu-id="c090a-105">This topic describes options for using the [\<CrmParameter\>](https://msdn.microsoft.com/library/gg309332.aspx) element to retrieve these values.</span></span>

## <a name="form-and-grid-context-in-ribbon-actions"></a><span data-ttu-id="c090a-106">Form and grid context in ribbon actions</span><span class="sxs-lookup"><span data-stu-id="c090a-106">Form and grid context in ribbon actions</span></span>

<span data-ttu-id="c090a-107">To pass in the execution context (*form context* or *grid context*) information to JavaScript function for your ribbon actions, specify **PrimaryControl** as the `<CrmParameter>` value in your ribbon definition.</span><span class="sxs-lookup"><span data-stu-id="c090a-107">To pass in the execution context (*form context* or *grid context*) information to JavaScript function for your ribbon actions, specify **PrimaryControl** as the `<CrmParameter>` value in your ribbon definition.</span></span> <span data-ttu-id="c090a-108">The passed in PrimaryControl value is used as an argument in your JavaScript function that provides the *form context* or *grid context* depending on where the ribbon command is executed.</span><span class="sxs-lookup"><span data-stu-id="c090a-108">The passed in PrimaryControl value is used as an argument in your JavaScript function that provides the *form context* or *grid context* depending on where the ribbon command is executed.</span></span> 

<span data-ttu-id="c090a-109">For example, here is a sample ribbon definition where we pass in the **PrimaryControl** parameter to the JavaScript function:</span><span class="sxs-lookup"><span data-stu-id="c090a-109">For example, here is a sample ribbon definition where we pass in the **PrimaryControl** parameter to the JavaScript function:</span></span>

```xml
<CommandDefinition Id="SampleCommand">
  <EnableRules/>
  <DisplayRules/>
  <Actions>
    <JavaScriptFunction Library="$webresource:new_mySampleScript.js" FunctionName="mySampleFunction">
      <CrmParameter Value="PrimaryControl" />
    </JavaScriptFunction>
  </Actions>
</CommandDefinition>
```

<span data-ttu-id="c090a-110">Next, in the **new_mySampleScript.js** web resource file referenced in the example above, define your JavaScript function with the **primaryControl** variable as an argument.</span><span class="sxs-lookup"><span data-stu-id="c090a-110">Next, in the **new_mySampleScript.js** web resource file referenced in the example above, define your JavaScript function with the **primaryControl** variable as an argument.</span></span> <span data-ttu-id="c090a-111">This argument provides the *form* or *grid* context depending on where the ribbon command is executed:</span><span class="sxs-lookup"><span data-stu-id="c090a-111">This argument provides the *form* or *grid* context depending on where the ribbon command is executed:</span></span>

```JavaScript
function mySampleFunction(primaryControl) {
    var formContext = primaryControl;
    // Perform operations using the formContext object
}
```

<span data-ttu-id="c090a-112">You can also specify **CommandProperties** as `<CrmParameter>` value in your ribbon definition to pass details about the event from the ribbon control.</span><span class="sxs-lookup"><span data-stu-id="c090a-112">You can also specify **CommandProperties** as `<CrmParameter>` value in your ribbon definition to pass details about the event from the ribbon control.</span></span> <span data-ttu-id="c090a-113">You can use this to send contextual information to your JavaScript function where specific actions can be determined based on the context of the event.</span><span class="sxs-lookup"><span data-stu-id="c090a-113">You can use this to send contextual information to your JavaScript function where specific actions can be determined based on the context of the event.</span></span>

> [!NOTE]
> <span data-ttu-id="c090a-114">Getting *form context* and *grid context* for JavaScript functions for ribbon actions is different from how you get these values in form scripting.</span><span class="sxs-lookup"><span data-stu-id="c090a-114">Getting *form context* and *grid context* for JavaScript functions for ribbon actions is different from how you get these values in form scripting.</span></span> <span data-ttu-id="c090a-115">For information about form scripting and how to get these contexts, see [Client API form context](../clientapi/clientapi-form-context.md) and [Client API grid context](../clientapi/clientapi-grid-context.md).</span><span class="sxs-lookup"><span data-stu-id="c090a-115">For information about form scripting and how to get these contexts, see [Client API form context](../clientapi/clientapi-form-context.md) and [Client API grid context](../clientapi/clientapi-grid-context.md).</span></span>

## <a name="form-values"></a><span data-ttu-id="c090a-116">Form values</span><span class="sxs-lookup"><span data-stu-id="c090a-116">Form values</span></span>

<span data-ttu-id="c090a-117">With a form ribbon, you can use the `data.entity`.[attributes](../clientapi/reference/attributes.md) collection and the `ui`.[controls](../clientapi/reference/controls.md) collection to retrieve and set values for known fields.</span><span class="sxs-lookup"><span data-stu-id="c090a-117">With a form ribbon, you can use the `data.entity`.[attributes](../clientapi/reference/attributes.md) collection and the `ui`.[controls](../clientapi/reference/controls.md) collection to retrieve and set values for known fields.</span></span> 

<span data-ttu-id="c090a-118">For example, the following sample code shows how to retrieve the account name field on the account form, and then set a value in the websiteurl field based on the account name value:</span><span class="sxs-lookup"><span data-stu-id="c090a-118">For example, the following sample code shows how to retrieve the account name field on the account form, and then set a value in the websiteurl field based on the account name value:</span></span>

```JavaScript
function mySampleFunction(primaryControl) {
    var formContext = primaryControl;    
    var accountName = formContext.getControl("name").getAttribute().getValue();    

    // Set the WebSiteURL field if account name contains "Contoso"
    if (accountName.toLowerCase().search("contoso") != -1) {
        formContext.getAttribute("websiteurl").setValue("http://www.contoso.com");
    }
    else {
        Xrm.Navigation.openAlertDialog({ text: "Account name does not contain 'Contoso'." });
    }
}
```

  
## <a name="grid-values"></a><span data-ttu-id="c090a-119">Grid values</span><span class="sxs-lookup"><span data-stu-id="c090a-119">Grid values</span></span>  
 <span data-ttu-id="c090a-120">The majority of the values available for the `<CrmParameter>` element are related to working with data displayed in a grid or hierarchy chart.</span><span class="sxs-lookup"><span data-stu-id="c090a-120">The majority of the values available for the `<CrmParameter>` element are related to working with data displayed in a grid or hierarchy chart.</span></span> <span data-ttu-id="c090a-121">By using the `Value` attribute enumeration options, you can easily isolate items by:</span><span class="sxs-lookup"><span data-stu-id="c090a-121">By using the `Value` attribute enumeration options, you can easily isolate items by:</span></span>  
  
- <span data-ttu-id="c090a-122">**Selected items**</span><span class="sxs-lookup"><span data-stu-id="c090a-122">**Selected items**</span></span>  
  
    -   <span data-ttu-id="c090a-123">SelectedControlSelectedItemCount</span><span class="sxs-lookup"><span data-stu-id="c090a-123">SelectedControlSelectedItemCount</span></span>  
  
    -   <span data-ttu-id="c090a-124">SelectedControlSelectedItemIds</span><span class="sxs-lookup"><span data-stu-id="c090a-124">SelectedControlSelectedItemIds</span></span>  
  
    -   <span data-ttu-id="c090a-125">SelectedControlSelectedItemReferences</span><span class="sxs-lookup"><span data-stu-id="c090a-125">SelectedControlSelectedItemReferences</span></span>  
  
- <span data-ttu-id="c090a-126">**All items**</span><span class="sxs-lookup"><span data-stu-id="c090a-126">**All items**</span></span>  
  
    -   <span data-ttu-id="c090a-127">SelectedControlAllItemCount</span><span class="sxs-lookup"><span data-stu-id="c090a-127">SelectedControlAllItemCount</span></span>  
  
    -   <span data-ttu-id="c090a-128">SelectedControlAllItemIds</span><span class="sxs-lookup"><span data-stu-id="c090a-128">SelectedControlAllItemIds</span></span>  
  
    -   <span data-ttu-id="c090a-129">SelectedControlAllItemReferences</span><span class="sxs-lookup"><span data-stu-id="c090a-129">SelectedControlAllItemReferences</span></span>  
  
- <span data-ttu-id="c090a-130">**Unselected items**</span><span class="sxs-lookup"><span data-stu-id="c090a-130">**Unselected items**</span></span>  
  
    -   <span data-ttu-id="c090a-131">SelectedControlUnselectedItemCount</span><span class="sxs-lookup"><span data-stu-id="c090a-131">SelectedControlUnselectedItemCount</span></span>  
  
    -   <span data-ttu-id="c090a-132">SelectedControlUnselectedItemIds</span><span class="sxs-lookup"><span data-stu-id="c090a-132">SelectedControlUnselectedItemIds</span></span>  
  
    -   <span data-ttu-id="c090a-133">SelectedControlUnselectedItemReferences</span><span class="sxs-lookup"><span data-stu-id="c090a-133">SelectedControlUnselectedItemReferences</span></span>  
  
  <span data-ttu-id="c090a-134">For each of these groupings, you can gather the number of items and the GUID identifier.</span><span class="sxs-lookup"><span data-stu-id="c090a-134">For each of these groupings, you can gather the number of items and the GUID identifier.</span></span> <span data-ttu-id="c090a-135">If you are passing the values to a URL, you can also retrieve `EntityReference` objects that contain all the information that you need to uniquely identify the objects in the grid.</span><span class="sxs-lookup"><span data-stu-id="c090a-135">If you are passing the values to a URL, you can also retrieve `EntityReference` objects that contain all the information that you need to uniquely identify the objects in the grid.</span></span> <span data-ttu-id="c090a-136">These parameters apply whether the page viewed is the main grid (`HomepageGrid`) or a sub grid located in a form.</span><span class="sxs-lookup"><span data-stu-id="c090a-136">These parameters apply whether the page viewed is the main grid (`HomepageGrid`) or a sub grid located in a form.</span></span> <span data-ttu-id="c090a-137">When used together with the `SelectedEntityTypeName` parameter, you have all the information that you must have to pass to another application.</span><span class="sxs-lookup"><span data-stu-id="c090a-137">When used together with the `SelectedEntityTypeName` parameter, you have all the information that you must have to pass to another application.</span></span>  
  
 
  
## <a name="other-context-information"></a><span data-ttu-id="c090a-138">Other context information</span><span class="sxs-lookup"><span data-stu-id="c090a-138">Other context information</span></span>  
 <span data-ttu-id="c090a-139">In addition to data values, you can retrieve client context information by using [\<CrmParameter\>](https://msdn.microsoft.com/library/gg309332.aspx).</span><span class="sxs-lookup"><span data-stu-id="c090a-139">In addition to data values, you can retrieve client context information by using [\<CrmParameter\>](https://msdn.microsoft.com/library/gg309332.aspx).</span></span>  <span data-ttu-id="c090a-140">You can use the following options as the value for the `CrmParameter` element: `OrgName`, `OrgLcid`, and `UserLcid`.</span><span class="sxs-lookup"><span data-stu-id="c090a-140">You can use the following options as the value for the `CrmParameter` element: `OrgName`, `OrgLcid`, and `UserLcid`.</span></span>
 
 <span data-ttu-id="c090a-141">For a `<Url>` action, you can also use the `PassParams` attribute to include contextual information.</span><span class="sxs-lookup"><span data-stu-id="c090a-141">For a `<Url>` action, you can also use the `PassParams` attribute to include contextual information.</span></span>  
  
 <span data-ttu-id="c090a-142">The `Value` options `PrimaryEntityTypeName` and `FirstPrimaryItemId` provide information for an entity record.</span><span class="sxs-lookup"><span data-stu-id="c090a-142">The `Value` options `PrimaryEntityTypeName` and `FirstPrimaryItemId` provide information for an entity record.</span></span> <span data-ttu-id="c090a-143">You can use `PrimaryItemIds` for a `HomepageGrid` ribbon to get a list of all the displayed items.</span><span class="sxs-lookup"><span data-stu-id="c090a-143">You can use `PrimaryItemIds` for a `HomepageGrid` ribbon to get a list of all the displayed items.</span></span>
  
### <a name="see-also"></a><span data-ttu-id="c090a-144">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c090a-144">See also</span></span>  
 <span data-ttu-id="c090a-145">[Customize the Ribbon for Microsoft Dynamics 365 for Customer Engagement](customize-commands-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="c090a-145">[Customize the Ribbon for Microsoft Dynamics 365 for Customer Engagement](customize-commands-ribbon.md) </span></span>  
 <span data-ttu-id="c090a-146">[Passing Parameters to a URL using the Ribbon](pass-parameters-url-by-using-ribbon.md)  </span><span class="sxs-lookup"><span data-stu-id="c090a-146">[Passing Parameters to a URL using the Ribbon](pass-parameters-url-by-using-ribbon.md)  </span></span>  
 <span data-ttu-id="c090a-147">[Define Ribbon Actions](define-ribbon-actions.md) </span><span class="sxs-lookup"><span data-stu-id="c090a-147">[Define Ribbon Actions](define-ribbon-actions.md) </span></span>  
 [<span data-ttu-id="c090a-148">Define Custom Actions to modify the Ribbon</span><span class="sxs-lookup"><span data-stu-id="c090a-148">Define Custom Actions to modify the Ribbon</span></span>](define-custom-actions-modify-ribbon.md)<br>
 [<span data-ttu-id="c090a-149">Client API form context</span><span class="sxs-lookup"><span data-stu-id="c090a-149">Client API form context</span></span>](../clientapi/clientapi-form-context.md)<br>
 [<span data-ttu-id="c090a-150">Client API grid context</span><span class="sxs-lookup"><span data-stu-id="c090a-150">Client API grid context</span></span>](../clientapi/clientapi-grid-context.md)<br>
 
