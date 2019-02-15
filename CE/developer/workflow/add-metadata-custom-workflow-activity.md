---
title: Add metadata to a custom workflow activity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about adding metadata to a custom workflow activity by adding input and output parameters, and input and output attributes for the parameters.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 06607e30-352c-4f27-a82e-adad48ca0f34
caps.latest.revision: 35
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3d7e2828bc668b6fcd15bdec44d6e6492deef9a8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387731"
---
# <a name="add-metadata-to-a-custom-workflow-activity"></a><span data-ttu-id="cd8db-103">Add metadata to a custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="cd8db-103">Add metadata to a custom workflow activity</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="cd8db-104">The assembly that contains the custom workflow activity definition is annotated using the .NET attributes to provide the metadata that [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement uses at runtime to link your code to the workflow engine.</span><span class="sxs-lookup"><span data-stu-id="cd8db-104">The assembly that contains the custom workflow activity definition is annotated using the .NET attributes to provide the metadata that [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement uses at runtime to link your code to the workflow engine.</span></span> <span data-ttu-id="cd8db-105">For more information about .NET attributes, see [Extending Metadata Using Attributes](https://msdn.microsoft.com/library/5x6cd29c.aspx).</span><span class="sxs-lookup"><span data-stu-id="cd8db-105">For more information about .NET attributes, see [Extending Metadata Using Attributes](https://msdn.microsoft.com/library/5x6cd29c.aspx).</span></span>  
  
 <span data-ttu-id="cd8db-106">Before you start adding metadata to your custom workflow activity definition, ensure that you’re aware of the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] types and attributes that are supported for the custom workflow activities.</span><span class="sxs-lookup"><span data-stu-id="cd8db-106">Before you start adding metadata to your custom workflow activity definition, ensure that you’re aware of the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] types and attributes that are supported for the custom workflow activities.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="cd8db-107">see [Process Classes, Attributes, and Dynamics 365 for Customer Engagement Types](process-classes-attributes-and-types.md)</span><span class="sxs-lookup"><span data-stu-id="cd8db-107">see [Process Classes, Attributes, and Dynamics 365 for Customer Engagement Types](process-classes-attributes-and-types.md)</span></span>  
  
<a name="AddingInput"></a>   
## <a name="add-input-parameters"></a><span data-ttu-id="cd8db-108">Add input parameters</span><span class="sxs-lookup"><span data-stu-id="cd8db-108">Add input parameters</span></span>  
 <span data-ttu-id="cd8db-109">While specifying the input parameter in your workflow class, you can also specify a default value for the parameter.</span><span class="sxs-lookup"><span data-stu-id="cd8db-109">While specifying the input parameter in your workflow class, you can also specify a default value for the parameter.</span></span> <span data-ttu-id="cd8db-110">The following sample shows the definition of an input parameter.</span><span class="sxs-lookup"><span data-stu-id="cd8db-110">The following sample shows the definition of an input parameter.</span></span>  
  
```csharp  
[Input("DateTime input")]  
[Default("2004-07-09T02:54:00Z")]  
public InArgument<DateTime> Date { get; set; }  
```  
  
 <span data-ttu-id="cd8db-111">This input parameter is annotated with the .NET attribute `Input`.</span><span class="sxs-lookup"><span data-stu-id="cd8db-111">This input parameter is annotated with the .NET attribute `Input`.</span></span> <span data-ttu-id="cd8db-112">The <xref:Microsoft.Xrm.Sdk.Workflow.InputAttribute> class derives from the <xref:Microsoft.Xrm.Sdk.Workflow.ParameterAttribute> class, which takes a parameter (<xref:Microsoft.Xrm.Sdk.Workflow.ParameterAttribute>.<xref:Microsoft.Xrm.Sdk.Workflow.ParameterAttribute.Name>) to specify the name of the input attribute.</span><span class="sxs-lookup"><span data-stu-id="cd8db-112">The <xref:Microsoft.Xrm.Sdk.Workflow.InputAttribute> class derives from the <xref:Microsoft.Xrm.Sdk.Workflow.ParameterAttribute> class, which takes a parameter (<xref:Microsoft.Xrm.Sdk.Workflow.ParameterAttribute>.<xref:Microsoft.Xrm.Sdk.Workflow.ParameterAttribute.Name>) to specify the name of the input attribute.</span></span> <span data-ttu-id="cd8db-113">This name appears in the process form assistant in the web application.</span><span class="sxs-lookup"><span data-stu-id="cd8db-113">This name appears in the process form assistant in the web application.</span></span> <span data-ttu-id="cd8db-114">This lets you map an attribute as an input parameter to the process.</span><span class="sxs-lookup"><span data-stu-id="cd8db-114">This lets you map an attribute as an input parameter to the process.</span></span>  
  
 <span data-ttu-id="cd8db-115">In addition, you can make the input parameter required.</span><span class="sxs-lookup"><span data-stu-id="cd8db-115">In addition, you can make the input parameter required.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="cd8db-116">[RequiredArgumentAttribute](process-classes-attributes-and-types.md#RequiredArgumentAttribute)</span><span class="sxs-lookup"><span data-stu-id="cd8db-116">[RequiredArgumentAttribute](process-classes-attributes-and-types.md#RequiredArgumentAttribute)</span></span>  
  
<a name="Output"></a>   
## <a name="add-output-parameters"></a><span data-ttu-id="cd8db-117">Add output parameters</span><span class="sxs-lookup"><span data-stu-id="cd8db-117">Add output parameters</span></span>  
 <span data-ttu-id="cd8db-118">Output parameters are added in the same manner as the input parameters.</span><span class="sxs-lookup"><span data-stu-id="cd8db-118">Output parameters are added in the same manner as the input parameters.</span></span> <span data-ttu-id="cd8db-119">The following sample shows the definition of an output parameter.</span><span class="sxs-lookup"><span data-stu-id="cd8db-119">The following sample shows the definition of an output parameter.</span></span>  
  
```csharp  
[Output("Money output only")]  
[Default("23.3")]  
public OutArgument<Money> MoneyOutput { get; set; }  
```  
  
 <span data-ttu-id="cd8db-120">This output parameter is annotated with the .NET attribute `Output`.</span><span class="sxs-lookup"><span data-stu-id="cd8db-120">This output parameter is annotated with the .NET attribute `Output`.</span></span> <span data-ttu-id="cd8db-121">The <xref:Microsoft.Xrm.Sdk.Workflow.OutputAttribute> class derives from the <xref:Microsoft.Xrm.Sdk.Workflow.ParameterAttribute> class, which takes a parameter (<xref:Microsoft.Xrm.Sdk.Workflow.ParameterAttribute>.<xref:Microsoft.Xrm.Sdk.Workflow.ParameterAttribute.Name>) to specify the name of the output attribute.</span><span class="sxs-lookup"><span data-stu-id="cd8db-121">The <xref:Microsoft.Xrm.Sdk.Workflow.OutputAttribute> class derives from the <xref:Microsoft.Xrm.Sdk.Workflow.ParameterAttribute> class, which takes a parameter (<xref:Microsoft.Xrm.Sdk.Workflow.ParameterAttribute>.<xref:Microsoft.Xrm.Sdk.Workflow.ParameterAttribute.Name>) to specify the name of the output attribute.</span></span> <span data-ttu-id="cd8db-122">This name appears in the process form assistant in the web application.</span><span class="sxs-lookup"><span data-stu-id="cd8db-122">This name appears in the process form assistant in the web application.</span></span> <span data-ttu-id="cd8db-123">This lets you map an attribute as an output.</span><span class="sxs-lookup"><span data-stu-id="cd8db-123">This lets you map an attribute as an output.</span></span>  
  
<a name="InAndOut"></a>   
## <a name="add-input-and-output-attributes-for-the-same-parameter"></a><span data-ttu-id="cd8db-124">Add input and output attributes for the same parameter</span><span class="sxs-lookup"><span data-stu-id="cd8db-124">Add input and output attributes for the same parameter</span></span>  
 <span data-ttu-id="cd8db-125">You can use the input and output attributes for the same parameter.</span><span class="sxs-lookup"><span data-stu-id="cd8db-125">You can use the input and output attributes for the same parameter.</span></span> <span data-ttu-id="cd8db-126">In the following code example, `IntParameter` is the input as well as the output parameter.</span><span class="sxs-lookup"><span data-stu-id="cd8db-126">In the following code example, `IntParameter` is the input as well as the output parameter.</span></span>  
  
```csharp  
[Input("Int input")]  
[Output("Int output")]  
[Default("2322")]  
public InOutArgument<int> IntParameter { get; set; }  
```  
  
<a name="Additional"></a>   
## <a name="additional-attributes"></a><span data-ttu-id="cd8db-127">Additional attributes</span><span class="sxs-lookup"><span data-stu-id="cd8db-127">Additional attributes</span></span>  
 <span data-ttu-id="cd8db-128">Some types, such as `EntityReference` and `OptionSetValue`, require additional attributes apart from the `Input`, `Output`, and `Default` attributes.</span><span class="sxs-lookup"><span data-stu-id="cd8db-128">Some types, such as `EntityReference` and `OptionSetValue`, require additional attributes apart from the `Input`, `Output`, and `Default` attributes.</span></span> <span data-ttu-id="cd8db-129">The additional attributes are: `ReferenceTarget` and `AttributeTarget`.</span><span class="sxs-lookup"><span data-stu-id="cd8db-129">The additional attributes are: `ReferenceTarget` and `AttributeTarget`.</span></span> <span data-ttu-id="cd8db-130">The following sample shows the definition of a parameter of the `EntityReference` type.</span><span class="sxs-lookup"><span data-stu-id="cd8db-130">The following sample shows the definition of a parameter of the `EntityReference` type.</span></span>  
  
```csharp  
[Input("EntityReference input")]  
[Output("EntityReference output")]  
[ReferenceTarget("account")]  
[Default("3B036E3E-94F9-DE11-B508-00155DBA2902", "account")]  
public InOutArgument<EntityReference> AccountReference { get; set; }  
```  
  
 <span data-ttu-id="cd8db-131">For a list of supported types and attributes, see [Process Classes, Attributes, and Dynamics 365 for Customer Engagement Types](process-classes-attributes-and-types.md).</span><span class="sxs-lookup"><span data-stu-id="cd8db-131">For a list of supported types and attributes, see [Process Classes, Attributes, and Dynamics 365 for Customer Engagement Types](process-classes-attributes-and-types.md).</span></span>  
  
<a name="Execute"></a>   
## <a name="add-the-execute-method"></a><span data-ttu-id="cd8db-132">Add the Execute method</span><span class="sxs-lookup"><span data-stu-id="cd8db-132">Add the Execute method</span></span>  
 <span data-ttu-id="cd8db-133">Your custom workflow activity must have an `Execute` method, as shown in the following example.</span><span class="sxs-lookup"><span data-stu-id="cd8db-133">Your custom workflow activity must have an `Execute` method, as shown in the following example.</span></span>  
  
```csharp  
protected override void Execute(CodeActivityContext context)  
{  
   if (AccountReference.Get(context).Id != new Guid("3B036E3E-94F9-DE11-B508-00155DBA2902"))     
      throw new InvalidPluginExecutionException("Unexpected default value");  
}  
```  
  
### <a name="see-also"></a><span data-ttu-id="cd8db-134">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="cd8db-134">See also</span></span>  
 <span data-ttu-id="cd8db-135">[Custom workflow activities (workflow assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span><span class="sxs-lookup"><span data-stu-id="cd8db-135">[Custom workflow activities (workflow assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span></span>  
 <span data-ttu-id="cd8db-136">[Creating a Custom Workflow Activity](create-custom-workflow-activity.md) </span><span class="sxs-lookup"><span data-stu-id="cd8db-136">[Creating a Custom Workflow Activity](create-custom-workflow-activity.md) </span></span>  
 <span data-ttu-id="cd8db-137">[Using the IOrganization Web Service within a Custom Workflow Activity](use-iorganization-web-service-custom-workflow-activity.md) </span><span class="sxs-lookup"><span data-stu-id="cd8db-137">[Using the IOrganization Web Service within a Custom Workflow Activity](use-iorganization-web-service-custom-workflow-activity.md) </span></span>  
 <span data-ttu-id="cd8db-138">[Sample: Create a Custom Workflow Activity](sample-create-custom-workflow-activity.md) </span><span class="sxs-lookup"><span data-stu-id="cd8db-138">[Sample: Create a Custom Workflow Activity](sample-create-custom-workflow-activity.md) </span></span>  
 [<span data-ttu-id="cd8db-139">Process Classes, Attributes, and Dynamics 365 for Customer Engagement Types</span><span class="sxs-lookup"><span data-stu-id="cd8db-139">Process Classes, Attributes, and Dynamics 365 for Customer Engagement Types</span></span>](process-classes-attributes-and-types.md)
