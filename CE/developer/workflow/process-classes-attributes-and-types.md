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
# <a name="process-classes-attributes-and-types"></a><span data-ttu-id="b4ac1-103">Process classes, attributes, and types</span><span class="sxs-lookup"><span data-stu-id="b4ac1-103">Process classes, attributes, and types</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b4ac1-104">This topic provides information about the process classes and types found in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement that you can use to work with the custom activities.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-104">This topic provides information about the process classes and types found in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement that you can use to work with the custom activities.</span></span>  
  
<a name="ProcessClasses"></a>
   
## <a name="process-classes"></a><span data-ttu-id="b4ac1-105">Process classes</span><span class="sxs-lookup"><span data-stu-id="b4ac1-105">Process classes</span></span>  

 <span data-ttu-id="b4ac1-106">The process classes are available in the <xref:Microsoft.Xrm.Sdk.Workflow> namespace (Microsoft.Xrm.Sdk.Workflow.dll).</span><span class="sxs-lookup"><span data-stu-id="b4ac1-106">The process classes are available in the <xref:Microsoft.Xrm.Sdk.Workflow> namespace (Microsoft.Xrm.Sdk.Workflow.dll).</span></span> <span data-ttu-id="b4ac1-107">You can use these classes to create custom activities in [!INCLUDE[pn_Windows_Workflow_Foundation](../../includes/pn-windows-workflow-foundation.md)], and then use the activities in the **Processes** area of [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)], or in the XAML workflows.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-107">You can use these classes to create custom activities in [!INCLUDE[pn_Windows_Workflow_Foundation](../../includes/pn-windows-workflow-foundation.md)], and then use the activities in the **Processes** area of [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)], or in the XAML workflows.</span></span> <span data-ttu-id="b4ac1-108">For detailed information about the process classes, see <xref:Microsoft.Xrm.Sdk.Workflow>.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-108">For detailed information about the process classes, see <xref:Microsoft.Xrm.Sdk.Workflow>.</span></span>  
  
<a name="AttributesandMicrosoftDynamicsCRMTypes"></a>
   
## <a name="attributes-and-includepndynamicscrmincludespn-dynamics-crmmd-types"></a><span data-ttu-id="b4ac1-109">Attributes and [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] types</span><span class="sxs-lookup"><span data-stu-id="b4ac1-109">Attributes and [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] types</span></span>
  
 <span data-ttu-id="b4ac1-110">The [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] types are found in the <xref:Microsoft.Xrm.Sdk> namespace (Microsoft.Xrm.Sdk.dll).</span><span class="sxs-lookup"><span data-stu-id="b4ac1-110">The [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] types are found in the <xref:Microsoft.Xrm.Sdk> namespace (Microsoft.Xrm.Sdk.dll).</span></span> <span data-ttu-id="b4ac1-111">Use the <xref:Microsoft.Xrm.Sdk.Workflow.InputAttribute> and <xref:Microsoft.Xrm.Sdk.Workflow.OutputAttribute> classes to annotate input and output properties.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-111">Use the <xref:Microsoft.Xrm.Sdk.Workflow.InputAttribute> and <xref:Microsoft.Xrm.Sdk.Workflow.OutputAttribute> classes to annotate input and output properties.</span></span>  
  
 <span data-ttu-id="b4ac1-112">The following types are supported for custom workflow activities:</span><span class="sxs-lookup"><span data-stu-id="b4ac1-112">The following types are supported for custom workflow activities:</span></span>  
  
- `Bool`  
  
- `DateTime`  
  
- `Decimal`  
  
- `Double`  
  
- <xref:Microsoft.Xrm.Sdk.EntityReference>  
  
- `Int`  
  
- `Money`  
  
- <xref:Microsoft.Xrm.Sdk.OptionSetValue>  
  
- `String`  
  
  <span data-ttu-id="b4ac1-113">Apart from the `Input`, `Output`, and `Default` attributes, some of the supported [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] types in the custom workflow activities require you to specify additional attributes such as `ReferenceTarget` and `AttributeTarget`.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-113">Apart from the `Input`, `Output`, and `Default` attributes, some of the supported [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] types in the custom workflow activities require you to specify additional attributes such as `ReferenceTarget` and `AttributeTarget`.</span></span> <span data-ttu-id="b4ac1-114">These are described in the following section.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-114">These are described in the following section.</span></span>  
  
<a name="InputAttribute"></a>

## <a name="inputattribute-and-outputattribute"></a><span data-ttu-id="b4ac1-115">InputAttribute and OutputAttribute</span><span class="sxs-lookup"><span data-stu-id="b4ac1-115">InputAttribute and OutputAttribute</span></span>  

 <span data-ttu-id="b4ac1-116">The following sample shows how to add the input and output attributes to a Money parameter used in a custom workflow activity.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-116">The following sample shows how to add the input and output attributes to a Money parameter used in a custom workflow activity.</span></span> <span data-ttu-id="b4ac1-117">It also shows how to specify a default value for the property.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-117">It also shows how to specify a default value for the property.</span></span>  
  
```csharp  
[Input("Money input")]  
[Output("Money output")]  
[Default("232.3")]  
public InOutArgument<Money> MoneyParameter { get; set; }  
```  
  
<a name="DefaultAttribute"></a>

## <a name="defaultattribute"></a><span data-ttu-id="b4ac1-118">DefaultAttribute</span><span class="sxs-lookup"><span data-stu-id="b4ac1-118">DefaultAttribute</span></span>  

 <span data-ttu-id="b4ac1-119">You can use the <xref:Microsoft.Xrm.Sdk.Workflow.DefaultAttribute> class to specify a default value for an input parameter.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-119">You can use the <xref:Microsoft.Xrm.Sdk.Workflow.DefaultAttribute> class to specify a default value for an input parameter.</span></span> <span data-ttu-id="b4ac1-120">The following examples show how to set the default value for each type using the `Default` attribute.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-120">The following examples show how to set the default value for each type using the `Default` attribute.</span></span>  
  
### <a name="bool"></a><span data-ttu-id="b4ac1-121">Bool</span><span class="sxs-lookup"><span data-stu-id="b4ac1-121">Bool</span></span>  
  
```csharp  
[Input("Bool input")]  
[Output("Bool output")]  
[Default("True")]  
public InOutArgument<bool> Bool { get; set; }  
```  
  
### <a name="datetime"></a><span data-ttu-id="b4ac1-122">Ngày Giờ</span><span class="sxs-lookup"><span data-stu-id="b4ac1-122">DateTime</span></span>  
  
```csharp  
[Input("DateTime input")]  
[Output("DateTime output")]  
[Default("2004-07-09T02:54:00Z")]  
public InOutArgument<DateTime> DateTime { get; set; }  
```  
  
### <a name="decimal"></a><span data-ttu-id="b4ac1-123">Thập phân</span><span class="sxs-lookup"><span data-stu-id="b4ac1-123">Decimal</span></span>  
  
```csharp  
[Input("Decimal input")]  
[Output("Decimal output")]  
[Default("23.45")]  
public InOutArgument<decimal> Decimal { get; set; }  
```  
  
### <a name="double"></a><span data-ttu-id="b4ac1-124">Gấp đôi</span><span class="sxs-lookup"><span data-stu-id="b4ac1-124">Double</span></span>  
  
```csharp  
[Input("Double input")]  
[Output("Double output")]  
[Default("252.2")]  
public InOutArgument<double> Double { get; set; }  
```  
  
### <a name="entityreference"></a><span data-ttu-id="b4ac1-125">EntityReference</span><span class="sxs-lookup"><span data-stu-id="b4ac1-125">EntityReference</span></span>  
  
```csharp  
[Input("EntityReference input")]  
[Output("EntityReference output")]  
[ReferenceTarget("account")]  
[Default("3B036E3E-94F9-DE11-B508-00155DBA2902", "account")]  
public InOutArgument<EntityReference> EntityReference { get; set; }  
```  
  
### <a name="int"></a><span data-ttu-id="b4ac1-126">Int</span><span class="sxs-lookup"><span data-stu-id="b4ac1-126">Int</span></span>  
  
```csharp  
[Input("Int input")]  
[Output("Int output")]  
[Default("2322")]  
public InOutArgument<int> Int { get; set; }  
```  
  
### <a name="money"></a><span data-ttu-id="b4ac1-127">Loại tiền</span><span class="sxs-lookup"><span data-stu-id="b4ac1-127">Money</span></span>  
  
```csharp  
[Input("Money input")]  
[Output("Money output")]  
[Default("232.3")]  
public InOutArgument<Money> Money { get; set; }  
```  
  
### <a name="optionsetvalue"></a><span data-ttu-id="b4ac1-128">OptionSetValue</span><span class="sxs-lookup"><span data-stu-id="b4ac1-128">OptionSetValue</span></span>  
  
```csharp  
[Input("OptionSetValue input")]  
[Output("OptionSetValue output")]  
[AttributeTarget("account", "industrycode")]  
[Default("3")]  
public InOutArgument<OptionSetValue> OptionSetValue { get; set; }  
```  
  
### <a name="string"></a><span data-ttu-id="b4ac1-129">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="b4ac1-129">String</span></span>  
  
```csharp  
[Input("String input")]  
[Output("String output")]  
[Default("string default")]  
public InOutArgument<string> String { get; set; }  
```  
  
<a name="ReferenceTargetAttributeforEntityReferenceType"></a>   

## <a name="referencetargetattribute"></a><span data-ttu-id="b4ac1-130">ReferenceTargetAttribute</span><span class="sxs-lookup"><span data-stu-id="b4ac1-130">ReferenceTargetAttribute</span></span>  

 <span data-ttu-id="b4ac1-131">The <xref:Microsoft.Xrm.Sdk.EntityReference> attribute type requires you to specify the entity type being referenced using the <xref:Microsoft.Xrm.Sdk.Workflow.ReferenceTargetAttribute> class.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-131">The <xref:Microsoft.Xrm.Sdk.EntityReference> attribute type requires you to specify the entity type being referenced using the <xref:Microsoft.Xrm.Sdk.Workflow.ReferenceTargetAttribute> class.</span></span> <span data-ttu-id="b4ac1-132">The following sample shows how to add the input and output attributes to an `AccountReference` parameter in a custom workflow activity by using the `ReferenceTarget` attribute.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-132">The following sample shows how to add the input and output attributes to an `AccountReference` parameter in a custom workflow activity by using the `ReferenceTarget` attribute.</span></span>  
  
```csharp  
[Input("EntityReference input")]  
[Output("EntityReference output")]  
[ReferenceTarget("account")]  
[Default("3B036E3E-94F9-DE11-B508-00155DBA2902", "account")]  
public InOutArgument<EntityReference> AccountReference { get; set; }  
```  
  
<a name="AttributeTargetAttributeforOptionSetValueType"></a>   
## <a name="attributetargetattribute"></a><span data-ttu-id="b4ac1-133">AttributeTargetAttribute</span><span class="sxs-lookup"><span data-stu-id="b4ac1-133">AttributeTargetAttribute</span></span>  
 <span data-ttu-id="b4ac1-134">The <xref:Microsoft.Xrm.Sdk.OptionSetValue> attribute type requires you to specify the entity and the attribute being referenced using the <xref:Microsoft.Xrm.Sdk.Workflow.AttributeTargetAttribute> class.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-134">The <xref:Microsoft.Xrm.Sdk.OptionSetValue> attribute type requires you to specify the entity and the attribute being referenced using the <xref:Microsoft.Xrm.Sdk.Workflow.AttributeTargetAttribute> class.</span></span> <span data-ttu-id="b4ac1-135">The following sample shows how to add the input and output attributes to an `OptionSetValue` parameter in a custom workflow activity by using the `AttributeTarget` attribute.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-135">The following sample shows how to add the input and output attributes to an `OptionSetValue` parameter in a custom workflow activity by using the `AttributeTarget` attribute.</span></span>  
  
```csharp  
[Input("OptionSetValue input")]  
[Output("OptionSetValue output")]  
[AttributeTarget("account", "industrycode")]  
[Default("3")]  
public InOutArgument<OptionSetValue> OptionSetValue { get; set; }  
```  
  
<a name="RequiredArgumentAttribute"></a> 
  
## <a name="requiredargumentattribute"></a><span data-ttu-id="b4ac1-136">RequiredArgumentAttribute</span><span class="sxs-lookup"><span data-stu-id="b4ac1-136">RequiredArgumentAttribute</span></span>  

 <span data-ttu-id="b4ac1-137">You can use the `System.Activities.RequiredArgumentAttribute` class to specify that an input parameter is required.</span><span class="sxs-lookup"><span data-stu-id="b4ac1-137">You can use the `System.Activities.RequiredArgumentAttribute` class to specify that an input parameter is required.</span></span>  
  
```csharp   
[RequiredArgument]  
[Input("Update Next Birthdate for")]  
[ReferenceTarget("contact")]  
public InArgument<EntityReference> Contact { get; set; }  
```  
  
### <a name="see-also"></a><span data-ttu-id="b4ac1-138">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b4ac1-138">See also</span></span>  

 <span data-ttu-id="b4ac1-139">[Custom workflow activities (workflow assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span><span class="sxs-lookup"><span data-stu-id="b4ac1-139">[Custom workflow activities (workflow assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span></span>  
 <span data-ttu-id="b4ac1-140">[Adding Metadata to the Custom Workflow Activity](add-metadata-custom-workflow-activity.md) </span><span class="sxs-lookup"><span data-stu-id="b4ac1-140">[Adding Metadata to the Custom Workflow Activity](add-metadata-custom-workflow-activity.md) </span></span>  
 [<span data-ttu-id="b4ac1-141">Sample: Create a custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="b4ac1-141">Sample: Create a custom workflow activity</span></span>](sample-create-custom-workflow-activity.md)
