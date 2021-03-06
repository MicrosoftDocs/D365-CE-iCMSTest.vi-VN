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
# <a name="pass-customer-engagement-data-from-a-page-as-a-parameter-to-ribbon-actions"></a>Pass Customer Engagement data from a page as a parameter to ribbon actions

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

When you define an action in a ribbon, you frequently have to pass data from the page to either a [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] function or a URL. This topic describes options for using the [\<CrmParameter\>](https://msdn.microsoft.com/library/gg309332.aspx) element to retrieve these values.

## <a name="form-and-grid-context-in-ribbon-actions"></a>Form and grid context in ribbon actions

To pass in the execution context (*form context* or *grid context*) information to JavaScript function for your ribbon actions, specify **PrimaryControl** as the `<CrmParameter>` value in your ribbon definition. The passed in PrimaryControl value is used as an argument in your JavaScript function that provides the *form context* or *grid context* depending on where the ribbon command is executed. 

For example, here is a sample ribbon definition where we pass in the **PrimaryControl** parameter to the JavaScript function:

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

Next, in the **new_mySampleScript.js** web resource file referenced in the example above, define your JavaScript function with the **primaryControl** variable as an argument. This argument provides the *form* or *grid* context depending on where the ribbon command is executed:

```JavaScript
function mySampleFunction(primaryControl) {
    var formContext = primaryControl;
    // Perform operations using the formContext object
}
```

You can also specify **CommandProperties** as `<CrmParameter>` value in your ribbon definition to pass details about the event from the ribbon control. You can use this to send contextual information to your JavaScript function where specific actions can be determined based on the context of the event.

> [!NOTE]
> Getting *form context* and *grid context* for JavaScript functions for ribbon actions is different from how you get these values in form scripting. For information about form scripting and how to get these contexts, see [Client API form context](../clientapi/clientapi-form-context.md) and [Client API grid context](../clientapi/clientapi-grid-context.md).

## <a name="form-values"></a>Form values

With a form ribbon, you can use the `data.entity`.[attributes](../clientapi/reference/attributes.md) collection and the `ui`.[controls](../clientapi/reference/controls.md) collection to retrieve and set values for known fields. 

For example, the following sample code shows how to retrieve the account name field on the account form, and then set a value in the websiteurl field based on the account name value:

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

  
## <a name="grid-values"></a>Grid values  
 The majority of the values available for the `<CrmParameter>` element are related to working with data displayed in a grid or hierarchy chart. By using the `Value` attribute enumeration options, you can easily isolate items by:  
  
- **Selected items**  
  
    -   SelectedControlSelectedItemCount  
  
    -   SelectedControlSelectedItemIds  
  
    -   SelectedControlSelectedItemReferences  
  
- **All items**  
  
    -   SelectedControlAllItemCount  
  
    -   SelectedControlAllItemIds  
  
    -   SelectedControlAllItemReferences  
  
- **Unselected items**  
  
    -   SelectedControlUnselectedItemCount  
  
    -   SelectedControlUnselectedItemIds  
  
    -   SelectedControlUnselectedItemReferences  
  
  For each of these groupings, you can gather the number of items and the GUID identifier. If you are passing the values to a URL, you can also retrieve `EntityReference` objects that contain all the information that you need to uniquely identify the objects in the grid. These parameters apply whether the page viewed is the main grid (`HomepageGrid`) or a sub grid located in a form. When used together with the `SelectedEntityTypeName` parameter, you have all the information that you must have to pass to another application.  
  
 
  
## <a name="other-context-information"></a>Other context information  
 In addition to data values, you can retrieve client context information by using [\<CrmParameter\>](https://msdn.microsoft.com/library/gg309332.aspx).  You can use the following options as the value for the `CrmParameter` element: `OrgName`, `OrgLcid`, and `UserLcid`.
 
 For a `<Url>` action, you can also use the `PassParams` attribute to include contextual information.  
  
 The `Value` options `PrimaryEntityTypeName` and `FirstPrimaryItemId` provide information for an entity record. You can use `PrimaryItemIds` for a `HomepageGrid` ribbon to get a list of all the displayed items.
  
### <a name="see-also"></a>Xem thêm  
 [Customize the Ribbon for Microsoft Dynamics 365 for Customer Engagement](customize-commands-ribbon.md)   
 [Passing Parameters to a URL using the Ribbon](pass-parameters-url-by-using-ribbon.md)    
 [Define Ribbon Actions](define-ribbon-actions.md)   
 [Define Custom Actions to modify the Ribbon](define-custom-actions-modify-ribbon.md)<br>
 [Client API form context](../clientapi/clientapi-form-context.md)<br>
 [Client API grid context](../clientapi/clientapi-grid-context.md)<br>
 
