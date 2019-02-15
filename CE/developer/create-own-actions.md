---
title: Create your own actions (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Actions are custom messages that help in extending functionality of Dynamics 365 for Customer Engagement apps. Learn more about how to create your own actions
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- workflow, action
ms.assetid: 98ee20a1-e4b2-4e42-a6ed-583b901507b3
caps.latest.revision: 44
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: db12a4e8936be602541f4bdc8784fa4b4c7239de
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385956"
---
# <a name="create-your-own-actions"></a><span data-ttu-id="d55a7-104">Create your own actions</span><span class="sxs-lookup"><span data-stu-id="d55a7-104">Create your own actions</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d55a7-105">You can extend the functionality of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps by creating custom messages known as *actions*.</span><span class="sxs-lookup"><span data-stu-id="d55a7-105">You can extend the functionality of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps by creating custom messages known as *actions*.</span></span> <span data-ttu-id="d55a7-106">These actions will have associated request/response classes and a Web API action will be generated.</span><span class="sxs-lookup"><span data-stu-id="d55a7-106">These actions will have associated request/response classes and a Web API action will be generated.</span></span> <span data-ttu-id="d55a7-107">Actions are typically used to add new domain specific functionality to the organization web service or to combine multiple organization web service message requests into a single request.</span><span class="sxs-lookup"><span data-stu-id="d55a7-107">Actions are typically used to add new domain specific functionality to the organization web service or to combine multiple organization web service message requests into a single request.</span></span> <span data-ttu-id="d55a7-108">For example, in a support call center, you may want to combine the Create, Assign, and Setstate messages into a single new Escalate message.</span><span class="sxs-lookup"><span data-stu-id="d55a7-108">For example, in a support call center, you may want to combine the Create, Assign, and Setstate messages into a single new Escalate message.</span></span>  
  
 <span data-ttu-id="d55a7-109">The business logic of an action is implemented using a workflow.</span><span class="sxs-lookup"><span data-stu-id="d55a7-109">The business logic of an action is implemented using a workflow.</span></span> <span data-ttu-id="d55a7-110">When you create an action, the associated real-time workflow is automatically registered to execute in stage 30 (core operation) of the execution pipeline.</span><span class="sxs-lookup"><span data-stu-id="d55a7-110">When you create an action, the associated real-time workflow is automatically registered to execute in stage 30 (core operation) of the execution pipeline.</span></span> <span data-ttu-id="d55a7-111">For more information about real-time workflows, see [Workflow types](process-categories.md).</span><span class="sxs-lookup"><span data-stu-id="d55a7-111">For more information about real-time workflows, see [Workflow types](process-categories.md).</span></span>  
  
 <span data-ttu-id="d55a7-112">While actions are supported in both [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps, creating an action in code (using XAML) is only supported by  on-premises and IFD deployments.</span><span class="sxs-lookup"><span data-stu-id="d55a7-112">While actions are supported in both [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps, creating an action in code (using XAML) is only supported by  on-premises and IFD deployments.</span></span> <span data-ttu-id="d55a7-113">Online customers must create actions interactively in the web application.</span><span class="sxs-lookup"><span data-stu-id="d55a7-113">Online customers must create actions interactively in the web application.</span></span>  
  
[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)]

<a name="about_actions"></a>   

## <a name="about-action-definitions"></a><span data-ttu-id="d55a7-114">About action definitions</span><span class="sxs-lookup"><span data-stu-id="d55a7-114">About action definitions</span></span>  

 <span data-ttu-id="d55a7-115">An action is defined by using a `Workflow` entity record, similar to a real-time workflow.</span><span class="sxs-lookup"><span data-stu-id="d55a7-115">An action is defined by using a `Workflow` entity record, similar to a real-time workflow.</span></span> <span data-ttu-id="d55a7-116">Some key points of what an action is and how it works are in the following list:</span><span class="sxs-lookup"><span data-stu-id="d55a7-116">Some key points of what an action is and how it works are in the following list:</span></span>  
  
- <span data-ttu-id="d55a7-117">Can be associated with a single entity or be global (not associated with any particular entity).</span><span class="sxs-lookup"><span data-stu-id="d55a7-117">Can be associated with a single entity or be global (not associated with any particular entity).</span></span>  
  
- <span data-ttu-id="d55a7-118">Is executed in the core operation stage 30 of the event execution pipeline.</span><span class="sxs-lookup"><span data-stu-id="d55a7-118">Is executed in the core operation stage 30 of the event execution pipeline.</span></span>  
  
- <span data-ttu-id="d55a7-119">Supports the invocation of plug-ins registered in the pre-operation and post-operation stages of the event execution pipeline.</span><span class="sxs-lookup"><span data-stu-id="d55a7-119">Supports the invocation of plug-ins registered in the pre-operation and post-operation stages of the event execution pipeline.</span></span>  
  
- <span data-ttu-id="d55a7-120">Can have plug-ins registered in the pre-operation or post-operation stages only when the action status is Activated.</span><span class="sxs-lookup"><span data-stu-id="d55a7-120">Can have plug-ins registered in the pre-operation or post-operation stages only when the action status is Activated.</span></span>  
  
- <span data-ttu-id="d55a7-121">Is available through the Web API or `organization.svc` and `organization.svc/web` endpoints.</span><span class="sxs-lookup"><span data-stu-id="d55a7-121">Is available through the Web API or `organization.svc` and `organization.svc/web` endpoints.</span></span>  
  
- <span data-ttu-id="d55a7-122">Can be executed using a [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resource.</span><span class="sxs-lookup"><span data-stu-id="d55a7-122">Can be executed using a [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resource.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="d55a7-123">[Execute an action using a JavaScript web resource](create-own-actions.md#BKMK_JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d55a7-123">[Execute an action using a JavaScript web resource](create-own-actions.md#BKMK_JavaScript)</span></span>  
  
- <span data-ttu-id="d55a7-124">Always runs under the security context of the calling user.</span><span class="sxs-lookup"><span data-stu-id="d55a7-124">Always runs under the security context of the calling user.</span></span>  
  
- <span data-ttu-id="d55a7-125">Record can’t be deleted while there are plug-in steps registered on the action.</span><span class="sxs-lookup"><span data-stu-id="d55a7-125">Record can’t be deleted while there are plug-in steps registered on the action.</span></span>  
  
- <span data-ttu-id="d55a7-126">Can optionally, through a configuration setting, participate in the current database transaction.</span><span class="sxs-lookup"><span data-stu-id="d55a7-126">Can optionally, through a configuration setting, participate in the current database transaction.</span></span>  
  
- <span data-ttu-id="d55a7-127">Doesn’t support a scope where the execution is restricted to a user, business unit, or organization.</span><span class="sxs-lookup"><span data-stu-id="d55a7-127">Doesn’t support a scope where the execution is restricted to a user, business unit, or organization.</span></span> <span data-ttu-id="d55a7-128">Actions always execute in organization scope.</span><span class="sxs-lookup"><span data-stu-id="d55a7-128">Actions always execute in organization scope.</span></span>  
  
- <span data-ttu-id="d55a7-129">Supports input and output arguments.</span><span class="sxs-lookup"><span data-stu-id="d55a7-129">Supports input and output arguments.</span></span>  
  
- <span data-ttu-id="d55a7-130">Supports auditing of data changes.</span><span class="sxs-lookup"><span data-stu-id="d55a7-130">Supports auditing of data changes.</span></span>  
  
- <span data-ttu-id="d55a7-131">Isn’t supported with offline clients.</span><span class="sxs-lookup"><span data-stu-id="d55a7-131">Isn’t supported with offline clients.</span></span>  
  
- <span data-ttu-id="d55a7-132">Can be invoked  by a web service method call.</span><span class="sxs-lookup"><span data-stu-id="d55a7-132">Can be invoked  by a web service method call.</span></span>  
  
- <span data-ttu-id="d55a7-133">Can be invoked directly from a workflow.</span><span class="sxs-lookup"><span data-stu-id="d55a7-133">Can be invoked directly from a workflow.</span></span>  
  
<a name="bkmk_permissions"></a>   
## <a name="required-permissions"></a><span data-ttu-id="d55a7-134">Các quyền bắt buộc</span><span class="sxs-lookup"><span data-stu-id="d55a7-134">Required permissions</span></span>  
 <span data-ttu-id="d55a7-135">A security privilege named Activate Real-time Processes (`prvActivateSynchronousWorkflow`) is required to activate an action’s real-time workflow so that it can be executed.</span><span class="sxs-lookup"><span data-stu-id="d55a7-135">A security privilege named Activate Real-time Processes (`prvActivateSynchronousWorkflow`) is required to activate an action’s real-time workflow so that it can be executed.</span></span> <span data-ttu-id="d55a7-136">This is in addition to any privileges needed to create a workflow.</span><span class="sxs-lookup"><span data-stu-id="d55a7-136">This is in addition to any privileges needed to create a workflow.</span></span>  
  
<a name="bkmk_create"></a>   
## <a name="create-an-action-using-code"></a><span data-ttu-id="d55a7-137">Create an action using code</span><span class="sxs-lookup"><span data-stu-id="d55a7-137">Create an action using code</span></span>  
 <span data-ttu-id="d55a7-138">Typically, an action would be implemented by a customizer using the interactive workflow designer of the web application.</span><span class="sxs-lookup"><span data-stu-id="d55a7-138">Typically, an action would be implemented by a customizer using the interactive workflow designer of the web application.</span></span> <span data-ttu-id="d55a7-139">However, developers can implement actions using SDK calls and deploy to an on-premises or IFD server if desired.</span><span class="sxs-lookup"><span data-stu-id="d55a7-139">However, developers can implement actions using SDK calls and deploy to an on-premises or IFD server if desired.</span></span>  
  
 <span data-ttu-id="d55a7-140">The workflow entity attributes that are used for an action are described in the following table.</span><span class="sxs-lookup"><span data-stu-id="d55a7-140">The workflow entity attributes that are used for an action are described in the following table.</span></span> <span data-ttu-id="d55a7-141">Sample code for a real-time workflow can be found in the topic [Create a real-time workflow in code](create-real-time-workflows.md#bkmk_create).</span><span class="sxs-lookup"><span data-stu-id="d55a7-141">Sample code for a real-time workflow can be found in the topic [Create a real-time workflow in code](create-real-time-workflows.md#bkmk_create).</span></span>  
  
|<span data-ttu-id="d55a7-142">Workflow attribute</span><span class="sxs-lookup"><span data-stu-id="d55a7-142">Workflow attribute</span></span>|<span data-ttu-id="d55a7-143">Mô tả</span><span class="sxs-lookup"><span data-stu-id="d55a7-143">Description</span></span>|  
|------------------------|-----------------|  
|`Category`|<span data-ttu-id="d55a7-144">Set to `WorkflowCategory.CustomOperation`.</span><span class="sxs-lookup"><span data-stu-id="d55a7-144">Set to `WorkflowCategory.CustomOperation`.</span></span>|  
|`SyncWorkflowLogOnError`|<span data-ttu-id="d55a7-145">When `true`, errors are logged to `ProcessSession` records.</span><span class="sxs-lookup"><span data-stu-id="d55a7-145">When `true`, errors are logged to `ProcessSession` records.</span></span> <span data-ttu-id="d55a7-146">Unlike asynchronous workflows, real-time workflow execution isn’t logged to `System Job` records.</span><span class="sxs-lookup"><span data-stu-id="d55a7-146">Unlike asynchronous workflows, real-time workflow execution isn’t logged to `System Job` records.</span></span>|  
|`Mode`|<span data-ttu-id="d55a7-147">Not used.</span><span class="sxs-lookup"><span data-stu-id="d55a7-147">Not used.</span></span>|  
|`IsTransacted`|<span data-ttu-id="d55a7-148">Set to `true` if the action should participate in the database transaction; otherwise, `false`.</span><span class="sxs-lookup"><span data-stu-id="d55a7-148">Set to `true` if the action should participate in the database transaction; otherwise, `false`.</span></span> <span data-ttu-id="d55a7-149">Default is `true`.</span><span class="sxs-lookup"><span data-stu-id="d55a7-149">Default is `true`.</span></span>|  
|`UniqueName`|<span data-ttu-id="d55a7-150">A unique name for the action.</span><span class="sxs-lookup"><span data-stu-id="d55a7-150">A unique name for the action.</span></span> <span data-ttu-id="d55a7-151">The name is composed of a publisher prefix + "_" + the unique name.</span><span class="sxs-lookup"><span data-stu-id="d55a7-151">The name is composed of a publisher prefix + "_" + the unique name.</span></span>|  
|`Xaml`|<span data-ttu-id="d55a7-152">Set to the XAML code that defines your action’s real-time workflow.</span><span class="sxs-lookup"><span data-stu-id="d55a7-152">Set to the XAML code that defines your action’s real-time workflow.</span></span> <span data-ttu-id="d55a7-153">There is no way to refer to another existing real-time workflow.</span><span class="sxs-lookup"><span data-stu-id="d55a7-153">There is no way to refer to another existing real-time workflow.</span></span>|  
  
### <a name="add-input-and-output-arguments"></a><span data-ttu-id="d55a7-154">Add input and output arguments</span><span class="sxs-lookup"><span data-stu-id="d55a7-154">Add input and output arguments</span></span>  
 <span data-ttu-id="d55a7-155">Actions support input and output arguments that can be added to the workflow using a [DynamicActivityProperty](https://msdn.microsoft.com/library/system.activities.dynamicactivityproperty.aspx) type.</span><span class="sxs-lookup"><span data-stu-id="d55a7-155">Actions support input and output arguments that can be added to the workflow using a [DynamicActivityProperty](https://msdn.microsoft.com/library/system.activities.dynamicactivityproperty.aspx) type.</span></span> <span data-ttu-id="d55a7-156">When you add these arguments to an action’s workflow, they become properties in the message request and response classes associated with that action.</span><span class="sxs-lookup"><span data-stu-id="d55a7-156">When you add these arguments to an action’s workflow, they become properties in the message request and response classes associated with that action.</span></span> <span data-ttu-id="d55a7-157">For example, the following example shows C# and XAML code for two input and one output arguments.</span><span class="sxs-lookup"><span data-stu-id="d55a7-157">For example, the following example shows C# and XAML code for two input and one output arguments.</span></span>  
  
```csharp  
DynamicActivityProperty inputProperty1 = new DynamicActivityProperty     { Name = "Subject", Type = typeof(InArgument<string>) };  
DynamicActivityProperty inputProperty2 = new DynamicActivityProperty     { Name = "EntityCollection", Type = typeof(InArgument<EntityCollection>) };  
DynamicActivityProperty outputProperty1 = new DynamicActivityProperty     { Name = "Output", Type = typeof(OutArgument<string>) };  
  
inputProperty1.Attributes.Add(new ArgumentRequiredAttribute(true));  
inputProperty1.Attributes.Add(new ArgumentDescriptionAttribute("The subject"));  
inputProperty1.Attributes.Add(new ArgumentDirectionAttribute(Microsoft.Xrm.Sdk.Workflow.ArgumentDirection.Input));  
  
inputProperty2.Attributes.Add(new ArgumentRequiredAttribute(false));  
inputProperty2.Attributes.Add(new ArgumentDescriptionAttribute("The entity collection"));  
inputProperty2.Attributes.Add(new ArgumentDirectionAttribute(Microsoft.Xrm.Sdk.Workflow.ArgumentDirection.Input));  
  
outputProperty1.Attributes.Add(new ArgumentRequiredAttribute(false));  
outputProperty1.Attributes.Add(new ArgumentDescriptionAttribute("The output"));  
outputProperty1.Attributes.Add(new ArgumentDirectionAttribute(Microsoft.Xrm.Sdk.Workflow.ArgumentDirection.Output));  
```  
  
```xaml
<x:Property Name="Subject"  
            Type="InArgument(x:String)">  
 <x:Property.Attributes>  
  <mxsw:ArgumentRequiredAttribute Value="True" />  
  <mxsw:ArgumentTargetAttribute Value="False" />  
  <mxsw:ArgumentDescriptionAttribute Value="The subject " />  
  <mxsw:ArgumentDirectionAttribute Value="Input" />  
  <mxsw:ArgumentEntityAttribute Value="" />  
 </x:Property.Attributes>  
</x:Property>  
<x:Property Name="EntityCollection"  
            Type="InArgument(mxs:EntityCollection)">  
 <x:Property.Attributes>  
  <mxsw:ArgumentRequiredAttribute Value="False" />  
  <mxsw:ArgumentTargetAttribute Value="False" />  
  <mxsw:ArgumentDescriptionAttribute Value="The entity collection" />  
  <mxsw:ArgumentDirectionAttribute Value="Input" />  
  <mxsw:ArgumentEntityAttribute Value="" />  
 </x:Property.Attributes>  
</x:Property>  
<x:Property Name="Output"  
            Type="OutArgument(x:String)">  
 <x:Property.Attributes>  
  <mxsw:ArgumentRequiredAttribute Value="False" />  
  <mxsw:ArgumentTargetAttribute Value="False" />  
  <mxsw:ArgumentDescriptionAttribute Value="The output" />  
  <mxsw:ArgumentDirectionAttribute Value="Output" />  
  <mxsw:ArgumentEntityAttribute Value="" />  
 </x:Property.Attributes>  
</x:Property>  
```  
  
 <span data-ttu-id="d55a7-158">The names used for the properties should be consistent with argument names since code generation will define these names as request or response properties.</span><span class="sxs-lookup"><span data-stu-id="d55a7-158">The names used for the properties should be consistent with argument names since code generation will define these names as request or response properties.</span></span>  
  
 <span data-ttu-id="d55a7-159">Supported argument types for the input and output arguments are shown in the following table.</span><span class="sxs-lookup"><span data-stu-id="d55a7-159">Supported argument types for the input and output arguments are shown in the following table.</span></span>  
  
|<span data-ttu-id="d55a7-160">.NET Type</span><span class="sxs-lookup"><span data-stu-id="d55a7-160">.NET Type</span></span>|<span data-ttu-id="d55a7-161">Argument Type</span><span class="sxs-lookup"><span data-stu-id="d55a7-161">Argument Type</span></span>|  
|---------------|-------------------|  
|<span data-ttu-id="d55a7-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d55a7-162">System.Int32</span></span>|<span data-ttu-id="d55a7-163">Số nguyên</span><span class="sxs-lookup"><span data-stu-id="d55a7-163">Integer</span></span>|  
|<span data-ttu-id="d55a7-164">System.String</span><span class="sxs-lookup"><span data-stu-id="d55a7-164">System.String</span></span>|<span data-ttu-id="d55a7-165">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="d55a7-165">String</span></span>|  
|<xref:Microsoft.Xrm.Sdk.EntityReference>|<span data-ttu-id="d55a7-166">EntityReference</span><span class="sxs-lookup"><span data-stu-id="d55a7-166">EntityReference</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Entity>|<span data-ttu-id="d55a7-167">Thực thể</span><span class="sxs-lookup"><span data-stu-id="d55a7-167">Entity</span></span>|  
|<xref:Microsoft.Xrm.Sdk.EntityCollection>|<span data-ttu-id="d55a7-168">EntityCollection</span><span class="sxs-lookup"><span data-stu-id="d55a7-168">EntityCollection</span></span>|  
|<span data-ttu-id="d55a7-169">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="d55a7-169">System.DateTime</span></span>|<span data-ttu-id="d55a7-170">Ngày Giờ</span><span class="sxs-lookup"><span data-stu-id="d55a7-170">DateTime</span></span>|  
|<span data-ttu-id="d55a7-171">System.Double</span><span class="sxs-lookup"><span data-stu-id="d55a7-171">System.Double</span></span>|<span data-ttu-id="d55a7-172">Nổi</span><span class="sxs-lookup"><span data-stu-id="d55a7-172">Float</span></span>|  
|<span data-ttu-id="d55a7-173">System.Decimal</span><span class="sxs-lookup"><span data-stu-id="d55a7-173">System.Decimal</span></span>|<span data-ttu-id="d55a7-174">Thập phân</span><span class="sxs-lookup"><span data-stu-id="d55a7-174">Decimal</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Money>|<span data-ttu-id="d55a7-175">Loại tiền</span><span class="sxs-lookup"><span data-stu-id="d55a7-175">Money</span></span>|  
|<span data-ttu-id="d55a7-176">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d55a7-176">System.Boolean</span></span>|<span data-ttu-id="d55a7-177">Boolean</span><span class="sxs-lookup"><span data-stu-id="d55a7-177">Boolean</span></span>|  
|<xref:Microsoft.Xrm.Sdk.OptionSetValue>|<span data-ttu-id="d55a7-178">Danh sách chọn</span><span class="sxs-lookup"><span data-stu-id="d55a7-178">Picklist</span></span>|  
  
 <span data-ttu-id="d55a7-179">Supported argument attributes are listed in the following table.</span><span class="sxs-lookup"><span data-stu-id="d55a7-179">Supported argument attributes are listed in the following table.</span></span>  
  
|<span data-ttu-id="d55a7-180">Argument Attribute</span><span class="sxs-lookup"><span data-stu-id="d55a7-180">Argument Attribute</span></span>|<span data-ttu-id="d55a7-181">Mô tả</span><span class="sxs-lookup"><span data-stu-id="d55a7-181">Description</span></span>|  
|------------------------|-----------------|  
|<xref:Microsoft.Xrm.Sdk.Workflow.ArgumentRequiredAttribute>|<span data-ttu-id="d55a7-182">Indicates if the argument is required.</span><span class="sxs-lookup"><span data-stu-id="d55a7-182">Indicates if the argument is required.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Workflow.ArgumentDirectionAttribute>|<span data-ttu-id="d55a7-183">Indicates if the argument’s direction is an input or output.</span><span class="sxs-lookup"><span data-stu-id="d55a7-183">Indicates if the argument’s direction is an input or output.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Workflow.ArgumentDescriptionAttribute>|<span data-ttu-id="d55a7-184">Specifies a description for the argument.</span><span class="sxs-lookup"><span data-stu-id="d55a7-184">Specifies a description for the argument.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Workflow.ArgumentEntityAttribute>|<span data-ttu-id="d55a7-185">Used if you want to pass in an entity.</span><span class="sxs-lookup"><span data-stu-id="d55a7-185">Used if you want to pass in an entity.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Workflow.ArgumentTargetAttribute>|<span data-ttu-id="d55a7-186">This attribute is automatically generated or added.</span><span class="sxs-lookup"><span data-stu-id="d55a7-186">This attribute is automatically generated or added.</span></span> <span data-ttu-id="d55a7-187">It points to the primary entity for which the workflow is run.</span><span class="sxs-lookup"><span data-stu-id="d55a7-187">It points to the primary entity for which the workflow is run.</span></span> <span data-ttu-id="d55a7-188">This attribute is optional for global actions.</span><span class="sxs-lookup"><span data-stu-id="d55a7-188">This attribute is optional for global actions.</span></span>|  
  
<a name="bkmk_package"></a>   
## <a name="package-an-action-for-distribution"></a><span data-ttu-id="d55a7-189">Package an action for distribution</span><span class="sxs-lookup"><span data-stu-id="d55a7-189">Package an action for distribution</span></span>  
 <span data-ttu-id="d55a7-190">To distribute your action so that it can be imported into a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps organization, add your action to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps solution.</span><span class="sxs-lookup"><span data-stu-id="d55a7-190">To distribute your action so that it can be imported into a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps organization, add your action to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps solution.</span></span> <span data-ttu-id="d55a7-191">This is easily done using the web application by navigating to **Settings** > **Customizations** > **Solutions**.</span><span class="sxs-lookup"><span data-stu-id="d55a7-191">This is easily done using the web application by navigating to **Settings** > **Customizations** > **Solutions**.</span></span> <span data-ttu-id="d55a7-192">You can also write code to create the solution.</span><span class="sxs-lookup"><span data-stu-id="d55a7-192">You can also write code to create the solution.</span></span> <span data-ttu-id="d55a7-193">For more information about solutions, see [Package and distribute extensions](package-distribute-extensions-use-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="d55a7-193">For more information about solutions, see [Package and distribute extensions](package-distribute-extensions-use-solutions.md).</span></span>  
  
<a name="bkmk_gentypes"></a>   
## <a name="generate-early-bound-types-for-an-action"></a><span data-ttu-id="d55a7-194">Generate early-bound types for an action</span><span class="sxs-lookup"><span data-stu-id="d55a7-194">Generate early-bound types for an action</span></span>  
 <span data-ttu-id="d55a7-195">Using the CrmSvcUtil tool, you can generate request and response classes for your action to include in your application code.</span><span class="sxs-lookup"><span data-stu-id="d55a7-195">Using the CrmSvcUtil tool, you can generate request and response classes for your action to include in your application code.</span></span> <span data-ttu-id="d55a7-196">However, before you generate these classes, be sure to activate the action.</span><span class="sxs-lookup"><span data-stu-id="d55a7-196">However, before you generate these classes, be sure to activate the action.</span></span>  
  
<span data-ttu-id="d55a7-197">To download the CrmSvcUtil.exe, see [Download tools from NuGet](download-tools-NuGet.md).</span><span class="sxs-lookup"><span data-stu-id="d55a7-197">To download the CrmSvcUtil.exe, see [Download tools from NuGet](download-tools-NuGet.md).</span></span>
  
 <span data-ttu-id="d55a7-198">The following sample shows the format for running the tool from the command line for an on-premises installation of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="d55a7-198">The following sample shows the format for running the tool from the command line for an on-premises installation of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="d55a7-199">You supply the parameter values for your installation.</span><span class="sxs-lookup"><span data-stu-id="d55a7-199">You supply the parameter values for your installation.</span></span>  
  
```ms-dos  
CrmSvcUtil.exe /url:http://<serverName>/<organizationName>/XRMServices/2011/Organization.svc /out:<outputFilename>.cs /username:<username> /password:<password> /domain:<domainName> /namespace:<outputNamespace> /serviceContextName:<serviceContextName> /generateActions  
```  
  
 <span data-ttu-id="d55a7-200">The following sample shows the format for running the tool from the command line with [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="d55a7-200">The following sample shows the format for running the tool from the command line with [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span></span> <span data-ttu-id="d55a7-201">You supply the parameter values appropriate for your account and server.</span><span class="sxs-lookup"><span data-stu-id="d55a7-201">You supply the parameter values appropriate for your account and server.</span></span>  
  
```ms-dos  
CrmSvcUtil.exe /url:https://<organizationUrlName>.api.crm.dynamics.com/XRMServices/2011/Organization.svc /out:<outputFilename>.cs /username:<username> /password:<password> /namespace:<outputNamespace> /serviceContextName:<serviceContextName> /generateActions  
```  
  
 <span data-ttu-id="d55a7-202">Notice the use of the `/generateActions` parameter.</span><span class="sxs-lookup"><span data-stu-id="d55a7-202">Notice the use of the `/generateActions` parameter.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="d55a7-203">[Create Early Bound Entity Classes with the Code Generation Tool (CrmSvcUtil.exe)](org-service/create-early-bound-entity-classes-code-generation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="d55a7-203">[Create Early Bound Entity Classes with the Code Generation Tool (CrmSvcUtil.exe)](org-service/create-early-bound-entity-classes-code-generation-tool.md).</span></span>  
  
 <span data-ttu-id="d55a7-204">You can use early-bound or late-bound types with the generated request and response classes for your action.</span><span class="sxs-lookup"><span data-stu-id="d55a7-204">You can use early-bound or late-bound types with the generated request and response classes for your action.</span></span>  
  
<a name="bkmk_executeWebAPI"></a>   
## <a name="execute-an-action-using-the-web-api"></a><span data-ttu-id="d55a7-205">Execute an action using the Web API</span><span class="sxs-lookup"><span data-stu-id="d55a7-205">Execute an action using the Web API</span></span>  
 <span data-ttu-id="d55a7-206">A new action is created in the Web API when it is created.</span><span class="sxs-lookup"><span data-stu-id="d55a7-206">A new action is created in the Web API when it is created.</span></span> <span data-ttu-id="d55a7-207">If the action is created in the context of an entity, it is bound to that entity.</span><span class="sxs-lookup"><span data-stu-id="d55a7-207">If the action is created in the context of an entity, it is bound to that entity.</span></span> <span data-ttu-id="d55a7-208">Otherwise it is an unbound action.</span><span class="sxs-lookup"><span data-stu-id="d55a7-208">Otherwise it is an unbound action.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="d55a7-209">[Use Web API actions](webapi/use-web-api-actions.md).</span><span class="sxs-lookup"><span data-stu-id="d55a7-209">[Use Web API actions](webapi/use-web-api-actions.md).</span></span>  
  
<a name="bkmk_execute"></a>   
## <a name="execute-an-action-using-the-organization-service"></a><span data-ttu-id="d55a7-210">Execute an action using the organization service</span><span class="sxs-lookup"><span data-stu-id="d55a7-210">Execute an action using the organization service</span></span>  
 <span data-ttu-id="d55a7-211">To execute an action using the organization web service using managed code, follow these steps.</span><span class="sxs-lookup"><span data-stu-id="d55a7-211">To execute an action using the organization web service using managed code, follow these steps.</span></span>  
  
1. <span data-ttu-id="d55a7-212">Include the early-bound types file that you generated using the CrmSvcUtil tool in your application’s project.</span><span class="sxs-lookup"><span data-stu-id="d55a7-212">Include the early-bound types file that you generated using the CrmSvcUtil tool in your application’s project.</span></span>  
  
2. <span data-ttu-id="d55a7-213">In your application code, instantiate your action’s request and populate any required properties.</span><span class="sxs-lookup"><span data-stu-id="d55a7-213">In your application code, instantiate your action’s request and populate any required properties.</span></span>  
  
3. <span data-ttu-id="d55a7-214">Invoke <xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*>, passing your request as an argument.</span><span class="sxs-lookup"><span data-stu-id="d55a7-214">Invoke <xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*>, passing your request as an argument.</span></span>  
  
   <span data-ttu-id="d55a7-215">Before you run your application code, make sure the action is activated.</span><span class="sxs-lookup"><span data-stu-id="d55a7-215">Before you run your application code, make sure the action is activated.</span></span> <span data-ttu-id="d55a7-216">Otherwise, you’ll receive a run-time error.</span><span class="sxs-lookup"><span data-stu-id="d55a7-216">Otherwise, you’ll receive a run-time error.</span></span>  
  
<a name="BKMK_JavaScript"></a>   
### <a name="execute-an-action-using-a-javascript-web-resource"></a><span data-ttu-id="d55a7-217">Execute an action using a JavaScript web resource</span><span class="sxs-lookup"><span data-stu-id="d55a7-217">Execute an action using a JavaScript web resource</span></span>  
 <span data-ttu-id="d55a7-218">An action can be executed using the Web API just like any system action.</span><span class="sxs-lookup"><span data-stu-id="d55a7-218">An action can be executed using the Web API just like any system action.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="d55a7-219">[Use Web API actions](webapi/use-web-api-actions.md).</span><span class="sxs-lookup"><span data-stu-id="d55a7-219">[Use Web API actions](webapi/use-web-api-actions.md).</span></span>  
  
 <span data-ttu-id="d55a7-220">The [Sdk.Soap.js](http://code.msdn.microsoft.com/SdkSoapjs-9b51b99a) sample library demonstrates how messages can be used with [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resources and the Organization service (organization.svc/web).</span><span class="sxs-lookup"><span data-stu-id="d55a7-220">The [Sdk.Soap.js](http://code.msdn.microsoft.com/SdkSoapjs-9b51b99a) sample library demonstrates how messages can be used with [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resources and the Organization service (organization.svc/web).</span></span> <span data-ttu-id="d55a7-221">Use the companion [Sdk.Soap.js Action Message Generator](http://code.msdn.microsoft.com/SdkSoapjs-Action-Message-971be943) sample to generate [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] libraries that can be used with Sdk.Soap.js in the same way you can use the libraries for system messages provided in that sample.</span><span class="sxs-lookup"><span data-stu-id="d55a7-221">Use the companion [Sdk.Soap.js Action Message Generator](http://code.msdn.microsoft.com/SdkSoapjs-Action-Message-971be943) sample to generate [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] libraries that can be used with Sdk.Soap.js in the same way you can use the libraries for system messages provided in that sample.</span></span> <span data-ttu-id="d55a7-222">The files generated using the `Sdk.Soap.js` Action Message Generator are separate [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] libraries for each action.</span><span class="sxs-lookup"><span data-stu-id="d55a7-222">The files generated using the `Sdk.Soap.js` Action Message Generator are separate [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] libraries for each action.</span></span> <span data-ttu-id="d55a7-223">Each library contains a request and response class that correspond to the classes generated by the CrmSvcUtil.</span><span class="sxs-lookup"><span data-stu-id="d55a7-223">Each library contains a request and response class that correspond to the classes generated by the CrmSvcUtil.</span></span>  
  
<a name="bkmk_execute-process"></a>   
## <a name="execute-an-action-using-a-process"></a><span data-ttu-id="d55a7-224">Execute an action using a process</span><span class="sxs-lookup"><span data-stu-id="d55a7-224">Execute an action using a process</span></span>  
 <span data-ttu-id="d55a7-225">You can execute an action from workflows, dialogs, or other process actions.</span><span class="sxs-lookup"><span data-stu-id="d55a7-225">You can execute an action from workflows, dialogs, or other process actions.</span></span> <span data-ttu-id="d55a7-226">Activated custom actions are available to processes by selecting the **Perform Action** item in the **Add Step** drop down of the web application process form.</span><span class="sxs-lookup"><span data-stu-id="d55a7-226">Activated custom actions are available to processes by selecting the **Perform Action** item in the **Add Step** drop down of the web application process form.</span></span> <span data-ttu-id="d55a7-227">After the step is added to your process, you can select your new custom action (or any action) from the **Action** list provided in the step.</span><span class="sxs-lookup"><span data-stu-id="d55a7-227">After the step is added to your process, you can select your new custom action (or any action) from the **Action** list provided in the step.</span></span> <span data-ttu-id="d55a7-228">Select **Set Properties** in the step to specify any input parameters that your custom action requires.</span><span class="sxs-lookup"><span data-stu-id="d55a7-228">Select **Set Properties** in the step to specify any input parameters that your custom action requires.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d55a7-229">If a custom action has unsupported parameter types, for example Picklist, Entity, or Entity Collection, the custom action isn’t listed in the **Action** list.</span><span class="sxs-lookup"><span data-stu-id="d55a7-229">If a custom action has unsupported parameter types, for example Picklist, Entity, or Entity Collection, the custom action isn’t listed in the **Action** list.</span></span>  
> 
>  <span data-ttu-id="d55a7-230">The ability to execute an action from a process was introduced with [!INCLUDE[pn_crm_online_2015_update_1](../includes/pn-crm-online-2015-update-1.md)].</span><span class="sxs-lookup"><span data-stu-id="d55a7-230">The ability to execute an action from a process was introduced with [!INCLUDE[pn_crm_online_2015_update_1](../includes/pn-crm-online-2015-update-1.md)].</span></span>  
  
 <span data-ttu-id="d55a7-231">The existing <xref:Microsoft.Xrm.Sdk.IExecutionContext.Depth> platform checks ensure an infinite loop does not occur.</span><span class="sxs-lookup"><span data-stu-id="d55a7-231">The existing <xref:Microsoft.Xrm.Sdk.IExecutionContext.Depth> platform checks ensure an infinite loop does not occur.</span></span> <span data-ttu-id="d55a7-232">For more information on depth limits see <xref:Microsoft.Xrm.Sdk.Deployment.WorkflowSettings.MaxDepth>.</span><span class="sxs-lookup"><span data-stu-id="d55a7-232">For more information on depth limits see <xref:Microsoft.Xrm.Sdk.Deployment.WorkflowSettings.MaxDepth>.</span></span>  
  
<a name="bkmk_longrunning"></a>   
## <a name="watch-out-for-long-running-actions"></a><span data-ttu-id="d55a7-233">Watch out for long running actions</span><span class="sxs-lookup"><span data-stu-id="d55a7-233">Watch out for long running actions</span></span>  
 <span data-ttu-id="d55a7-234">If one of the steps in the action’s real-time workflow is a custom workflow activity, that custom workflow activity is executed inside the isolated sandbox run-time environment and will be subject to the two minute timeout limit, similar to how sandboxed plug-ins are managed.</span><span class="sxs-lookup"><span data-stu-id="d55a7-234">If one of the steps in the action’s real-time workflow is a custom workflow activity, that custom workflow activity is executed inside the isolated sandbox run-time environment and will be subject to the two minute timeout limit, similar to how sandboxed plug-ins are managed.</span></span> <span data-ttu-id="d55a7-235">However, there are no restrictions on the amount of overall time the action itself can take.</span><span class="sxs-lookup"><span data-stu-id="d55a7-235">However, there are no restrictions on the amount of overall time the action itself can take.</span></span> <span data-ttu-id="d55a7-236">In addition, if an action participates in a transaction, where rollback is enabled, [!INCLUDE[pn_SQL_Server_short](../includes/pn-sql-server-short.md)] timeouts will apply.</span><span class="sxs-lookup"><span data-stu-id="d55a7-236">In addition, if an action participates in a transaction, where rollback is enabled, [!INCLUDE[pn_SQL_Server_short](../includes/pn-sql-server-short.md)] timeouts will apply.</span></span>  
  
> [!TIP]
>  <span data-ttu-id="d55a7-237">A best practice recommendation is that long running operations should be executed outside of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps using .NET asynchronous or background processes.</span><span class="sxs-lookup"><span data-stu-id="d55a7-237">A best practice recommendation is that long running operations should be executed outside of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps using .NET asynchronous or background processes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d55a7-238">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d55a7-238">See also</span></span>  
 <span data-ttu-id="d55a7-239">[Create real-time workflows](create-real-time-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d55a7-239">[Create real-time workflows](create-real-time-workflows.md) </span></span>  
 <span data-ttu-id="d55a7-240">[Use dialogs for guided processes](use-dialogs-guided-processes.md) </span><span class="sxs-lookup"><span data-stu-id="d55a7-240">[Use dialogs for guided processes](use-dialogs-guided-processes.md) </span></span>  
 <span data-ttu-id="d55a7-241">[Event Execution Pipeline](event-execution-pipeline.md) </span><span class="sxs-lookup"><span data-stu-id="d55a7-241">[Event Execution Pipeline](event-execution-pipeline.md) </span></span>  
 <span data-ttu-id="d55a7-242">[Write Workflows to Automate Business Processes](automate-business-processes-customer-engagement.md) </span><span class="sxs-lookup"><span data-stu-id="d55a7-242">[Write Workflows to Automate Business Processes](automate-business-processes-customer-engagement.md) </span></span>  
 [<span data-ttu-id="d55a7-243">Tùy chỉnh hệ thống của bạn</span><span class="sxs-lookup"><span data-stu-id="d55a7-243">Customize your system</span></span>](https://technet.microsoft.com/library/dn531158.aspx)
