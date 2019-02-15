---
title: Process classes, attributes, and types (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'The topic provides information about the process classes and types found in Dynamics 365 for Customer Engagement that you can use to work with the custom activities. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 16b56acb-9329-4ee1-9c65-b55af707551b
caps.latest.revision: 26
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 02daad62f92b0cdf9cfb9ba7b22a13f9c350d4eb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388307"
---
# <a name="process-classes-attributes-and-types"></a>Process classes, attributes, and types

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This topic provides information about the process classes and types found in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement that you can use to work with the custom activities.  
  
<a name="ProcessClasses"></a>
   
## <a name="process-classes"></a>Process classes  

 The process classes are available in the <xref:Microsoft.Xrm.Sdk.Workflow> namespace (Microsoft.Xrm.Sdk.Workflow.dll). You can use these classes to create custom activities in [!INCLUDE[pn_Windows_Workflow_Foundation](../../includes/pn-windows-workflow-foundation.md)], and then use the activities in the **Processes** area of [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)], or in the XAML workflows. For detailed information about the process classes, see <xref:Microsoft.Xrm.Sdk.Workflow>.  
  
<a name="AttributesandMicrosoftDynamicsCRMTypes"></a>
   
## <a name="attributes-and-includepndynamicscrmincludespn-dynamics-crmmd-types"></a>Attributes and [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] types
  
 The [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] types are found in the <xref:Microsoft.Xrm.Sdk> namespace (Microsoft.Xrm.Sdk.dll). Use the <xref:Microsoft.Xrm.Sdk.Workflow.InputAttribute> and <xref:Microsoft.Xrm.Sdk.Workflow.OutputAttribute> classes to annotate input and output properties.  
  
 The following types are supported for custom workflow activities:  
  
- `Bool`  
  
- `DateTime`  
  
- `Decimal`  
  
- `Double`  
  
- <xref:Microsoft.Xrm.Sdk.EntityReference>  
  
- `Int`  
  
- `Money`  
  
- <xref:Microsoft.Xrm.Sdk.OptionSetValue>  
  
- `String`  
  
  Apart from the `Input`, `Output`, and `Default` attributes, some of the supported [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] types in the custom workflow activities require you to specify additional attributes such as `ReferenceTarget` and `AttributeTarget`. These are described in the following section.  
  
<a name="InputAttribute"></a>

## <a name="inputattribute-and-outputattribute"></a>InputAttribute and OutputAttribute  

 The following sample shows how to add the input and output attributes to a Money parameter used in a custom workflow activity. It also shows how to specify a default value for the property.  
  
```csharp  
[Input("Money input")]  
[Output("Money output")]  
[Default("232.3")]  
public InOutArgument<Money> MoneyParameter { get; set; }  
```  
  
<a name="DefaultAttribute"></a>

## <a name="defaultattribute"></a>DefaultAttribute  

 You can use the <xref:Microsoft.Xrm.Sdk.Workflow.DefaultAttribute> class to specify a default value for an input parameter. The following examples show how to set the default value for each type using the `Default` attribute.  
  
### <a name="bool"></a>Bool  
  
```csharp  
[Input("Bool input")]  
[Output("Bool output")]  
[Default("True")]  
public InOutArgument<bool> Bool { get; set; }  
```  
  
### <a name="datetime"></a>Ngày Giờ  
  
```csharp  
[Input("DateTime input")]  
[Output("DateTime output")]  
[Default("2004-07-09T02:54:00Z")]  
public InOutArgument<DateTime> DateTime { get; set; }  
```  
  
### <a name="decimal"></a>Thập phân  
  
```csharp  
[Input("Decimal input")]  
[Output("Decimal output")]  
[Default("23.45")]  
public InOutArgument<decimal> Decimal { get; set; }  
```  
  
### <a name="double"></a>Gấp đôi  
  
```csharp  
[Input("Double input")]  
[Output("Double output")]  
[Default("252.2")]  
public InOutArgument<double> Double { get; set; }  
```  
  
### <a name="entityreference"></a>EntityReference  
  
```csharp  
[Input("EntityReference input")]  
[Output("EntityReference output")]  
[ReferenceTarget("account")]  
[Default("3B036E3E-94F9-DE11-B508-00155DBA2902", "account")]  
public InOutArgument<EntityReference> EntityReference { get; set; }  
```  
  
### <a name="int"></a>Int  
  
```csharp  
[Input("Int input")]  
[Output("Int output")]  
[Default("2322")]  
public InOutArgument<int> Int { get; set; }  
```  
  
### <a name="money"></a>Loại tiền  
  
```csharp  
[Input("Money input")]  
[Output("Money output")]  
[Default("232.3")]  
public InOutArgument<Money> Money { get; set; }  
```  
  
### <a name="optionsetvalue"></a>OptionSetValue  
  
```csharp  
[Input("OptionSetValue input")]  
[Output("OptionSetValue output")]  
[AttributeTarget("account", "industrycode")]  
[Default("3")]  
public InOutArgument<OptionSetValue> OptionSetValue { get; set; }  
```  
  
### <a name="string"></a>Chuỗi  
  
```csharp  
[Input("String input")]  
[Output("String output")]  
[Default("string default")]  
public InOutArgument<string> String { get; set; }  
```  
  
<a name="ReferenceTargetAttributeforEntityReferenceType"></a>   

## <a name="referencetargetattribute"></a>ReferenceTargetAttribute  

 The <xref:Microsoft.Xrm.Sdk.EntityReference> attribute type requires you to specify the entity type being referenced using the <xref:Microsoft.Xrm.Sdk.Workflow.ReferenceTargetAttribute> class. The following sample shows how to add the input and output attributes to an `AccountReference` parameter in a custom workflow activity by using the `ReferenceTarget` attribute.  
  
```csharp  
[Input("EntityReference input")]  
[Output("EntityReference output")]  
[ReferenceTarget("account")]  
[Default("3B036E3E-94F9-DE11-B508-00155DBA2902", "account")]  
public InOutArgument<EntityReference> AccountReference { get; set; }  
```  
  
<a name="AttributeTargetAttributeforOptionSetValueType"></a>   
## <a name="attributetargetattribute"></a>AttributeTargetAttribute  
 The <xref:Microsoft.Xrm.Sdk.OptionSetValue> attribute type requires you to specify the entity and the attribute being referenced using the <xref:Microsoft.Xrm.Sdk.Workflow.AttributeTargetAttribute> class. The following sample shows how to add the input and output attributes to an `OptionSetValue` parameter in a custom workflow activity by using the `AttributeTarget` attribute.  
  
```csharp  
[Input("OptionSetValue input")]  
[Output("OptionSetValue output")]  
[AttributeTarget("account", "industrycode")]  
[Default("3")]  
public InOutArgument<OptionSetValue> OptionSetValue { get; set; }  
```  
  
<a name="RequiredArgumentAttribute"></a> 
  
## <a name="requiredargumentattribute"></a>RequiredArgumentAttribute  

 You can use the `System.Activities.RequiredArgumentAttribute` class to specify that an input parameter is required.  
  
```csharp   
[RequiredArgument]  
[Input("Update Next Birthdate for")]  
[ReferenceTarget("contact")]  
public InArgument<EntityReference> Contact { get; set; }  
```  
  
### <a name="see-also"></a>Xem thêm  

 [Custom workflow activities (workflow assemblies)](../custom-workflow-activities-workflow-assemblies.md)   
 [Adding Metadata to the Custom Workflow Activity](add-metadata-custom-workflow-activity.md)   
 [Sample: Create a custom workflow activity](sample-create-custom-workflow-activity.md)
