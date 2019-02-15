---
title: Use Web API actions (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
descriptions: Actions are reusable operations that can be performed using the Web API. These are used with a POST request to modify data on Dynamics 365 for Customer Engagement
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 53eafd67-385a-485b-9022-5127df08ea2f
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 793a2909e0f696a459eac2b35947e5d5ad5e4cf7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386789"
---
# <a name="use-web-api-actions"></a><span data-ttu-id="03c41-102">Use Web API actions</span><span class="sxs-lookup"><span data-stu-id="03c41-102">Use Web API actions</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="03c41-103">Actions and functions represent re-usable operations you can perform using the Web API.</span><span class="sxs-lookup"><span data-stu-id="03c41-103">Actions and functions represent re-usable operations you can perform using the Web API.</span></span> <span data-ttu-id="03c41-104">Use a POST request with actions listed in <xref:Microsoft.Dynamics.CRM.ActionIndex> to perform operations that have side effects.</span><span class="sxs-lookup"><span data-stu-id="03c41-104">Use a POST request with actions listed in <xref:Microsoft.Dynamics.CRM.ActionIndex> to perform operations that have side effects.</span></span> <span data-ttu-id="03c41-105">You can also define custom actions and they’ll be available for you to use.</span><span class="sxs-lookup"><span data-stu-id="03c41-105">You can also define custom actions and they’ll be available for you to use.</span></span>

<a name="bkmk_unboundActions"></a>

## <a name="unbound-actions"></a><span data-ttu-id="03c41-106">Unbound actions</span><span class="sxs-lookup"><span data-stu-id="03c41-106">Unbound actions</span></span>

 <span data-ttu-id="03c41-107">Actions are defined in [CSDL metadata document](web-api-types-operations.md#bkmk_csdl).</span><span class="sxs-lookup"><span data-stu-id="03c41-107">Actions are defined in [CSDL metadata document](web-api-types-operations.md#bkmk_csdl).</span></span> <span data-ttu-id="03c41-108">As an example, the following is the definition of the <xref href="Microsoft.Dynamics.CRM.WinOpportunity?text=WinOpportunity Action" /> represented in the metadata document.</span><span class="sxs-lookup"><span data-stu-id="03c41-108">As an example, the following is the definition of the <xref href="Microsoft.Dynamics.CRM.WinOpportunity?text=WinOpportunity Action" /> represented in the metadata document.</span></span>

```xml
<Action Name="WinOpportunity">
  <Parameter Name="OpportunityClose" Type="mscrm.opportunityclose" Nullable="false" />
  <Parameter Name="Status" Type="Edm.Int32" Nullable="false" />
</Action>
```

 <span data-ttu-id="03c41-109">The WinOpportunity action corresponds to the <xref:Microsoft.Crm.Sdk.Messages.WinOpportunityRequest> using the organization service.</span><span class="sxs-lookup"><span data-stu-id="03c41-109">The WinOpportunity action corresponds to the <xref:Microsoft.Crm.Sdk.Messages.WinOpportunityRequest> using the organization service.</span></span> <span data-ttu-id="03c41-110">Use this action to set the state of an opportunity to Won and create an <xref href="Microsoft.Dynamics.CRM.opportunityclose?text=opportunityclose EntityType" /> to record the event.</span><span class="sxs-lookup"><span data-stu-id="03c41-110">Use this action to set the state of an opportunity to Won and create an <xref href="Microsoft.Dynamics.CRM.opportunityclose?text=opportunityclose EntityType" /> to record the event.</span></span> <span data-ttu-id="03c41-111">This action doesn’t include a return value.</span><span class="sxs-lookup"><span data-stu-id="03c41-111">This action doesn’t include a return value.</span></span> <span data-ttu-id="03c41-112">If it succeeds, the operation is complete.</span><span class="sxs-lookup"><span data-stu-id="03c41-112">If it succeeds, the operation is complete.</span></span>

 <span data-ttu-id="03c41-113">The `OpportunityClose` parameter requires a JSON representation of the opportunityclose entity to create in the operation.</span><span class="sxs-lookup"><span data-stu-id="03c41-113">The `OpportunityClose` parameter requires a JSON representation of the opportunityclose entity to create in the operation.</span></span> <span data-ttu-id="03c41-114">This entity must be related to the opportunity issuing the opportunityid single-valued navigation property.</span><span class="sxs-lookup"><span data-stu-id="03c41-114">This entity must be related to the opportunity issuing the opportunityid single-valued navigation property.</span></span> <span data-ttu-id="03c41-115">In the JSON this is set using the `@odata.bind` annotation as explained in [Associate entities on create](create-entity-web-api.md#bkmk_associateOnCreate).</span><span class="sxs-lookup"><span data-stu-id="03c41-115">In the JSON this is set using the `@odata.bind` annotation as explained in [Associate entities on create](create-entity-web-api.md#bkmk_associateOnCreate).</span></span>

 <span data-ttu-id="03c41-116">The `Status` parameter must be set to the status to for the opportunity when it is closed.</span><span class="sxs-lookup"><span data-stu-id="03c41-116">The `Status` parameter must be set to the status to for the opportunity when it is closed.</span></span> <span data-ttu-id="03c41-117">You can find the default value for this in the <xref href="Microsoft.Dynamics.CRM.opportunity?text=opportunity EntityType" /> statuscode property.</span><span class="sxs-lookup"><span data-stu-id="03c41-117">You can find the default value for this in the <xref href="Microsoft.Dynamics.CRM.opportunity?text=opportunity EntityType" /> statuscode property.</span></span> <span data-ttu-id="03c41-118">The **Won** option has a value of 3.</span><span class="sxs-lookup"><span data-stu-id="03c41-118">The **Won** option has a value of 3.</span></span> <span data-ttu-id="03c41-119">You may ask yourself, why is it necessary to set this value when there is only one status reason option that represents **Won**?</span><span class="sxs-lookup"><span data-stu-id="03c41-119">You may ask yourself, why is it necessary to set this value when there is only one status reason option that represents **Won**?</span></span> <span data-ttu-id="03c41-120">The reason is because you may define custom status options to represent a win, such as **Big Win** or **Small Win**, so the value could potentially be different from 3 in that situation.</span><span class="sxs-lookup"><span data-stu-id="03c41-120">The reason is because you may define custom status options to represent a win, such as **Big Win** or **Small Win**, so the value could potentially be different from 3 in that situation.</span></span>

 <span data-ttu-id="03c41-121">The following example is the HTTP request and response to call the `WinOpportunity` action for an opportunity with an opportunityid value of `b3828ac8-917a-e511-80d2-00155d2a68d2`.</span><span class="sxs-lookup"><span data-stu-id="03c41-121">The following example is the HTTP request and response to call the `WinOpportunity` action for an opportunity with an opportunityid value of `b3828ac8-917a-e511-80d2-00155d2a68d2`.</span></span>

 <span data-ttu-id="03c41-122">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="03c41-122">**Request**</span></span>

```http
POST [Organization URI]/api/data/v9.0/WinOpportunity HTTP/1.1
Accept: application/json
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0

{
 "Status": 3,
 "OpportunityClose": {
  "subject": "Won Opportunity",
  "opportunityid@odata.bind": "[Organization URI]/api/data/v9.0/opportunities(b3828ac8-917a-e511-80d2-00155d2a68d2)"
 }
}
```

 <span data-ttu-id="03c41-123">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="03c41-123">**Response**</span></span>

```http
HTTP/1.1 204 No Content
OData-Version: 4.0
```

<a name="bkmk_boundActions"></a>

## <a name="bound-actions"></a><span data-ttu-id="03c41-124">Bound actions</span><span class="sxs-lookup"><span data-stu-id="03c41-124">Bound actions</span></span>

 <span data-ttu-id="03c41-125">In the [CSDL metadata document](web-api-types-operations.md#bkmk_csdl), when an `Action` element represents a bound action, it has an `IsBound` attribute with the value `true`.</span><span class="sxs-lookup"><span data-stu-id="03c41-125">In the [CSDL metadata document](web-api-types-operations.md#bkmk_csdl), when an `Action` element represents a bound action, it has an `IsBound` attribute with the value `true`.</span></span> <span data-ttu-id="03c41-126">The first `Parameter` element defined within the action represents the entity that the operation is bound to.</span><span class="sxs-lookup"><span data-stu-id="03c41-126">The first `Parameter` element defined within the action represents the entity that the operation is bound to.</span></span> <span data-ttu-id="03c41-127">When the `Type` attribute of the parameter is a collection, the operation is bound to a collection of entities.</span><span class="sxs-lookup"><span data-stu-id="03c41-127">When the `Type` attribute of the parameter is a collection, the operation is bound to a collection of entities.</span></span> <span data-ttu-id="03c41-128">As an example, the following is the definition of the <xref href="Microsoft.Dynamics.CRM.AddToQueue?text=AddToQueue Action" /> represented in the CSDL:</span><span class="sxs-lookup"><span data-stu-id="03c41-128">As an example, the following is the definition of the <xref href="Microsoft.Dynamics.CRM.AddToQueue?text=AddToQueue Action" /> represented in the CSDL:</span></span>

```xml
 <ComplexType Name="AddToQueueResponse">
 <Property Name="QueueItemId" Type="Edm.Guid" Nullable="false" />
 </ComplexType>
 <Action Name="AddToQueue" IsBound="true">
  <Parameter Name="entity" Type="mscrm.queue" Nullable="false" />
  <Parameter Name="Target" Type="mscrm.crmbaseentity" Nullable="false" />
  <Parameter Name="SourceQueue" Type="mscrm.queue" />
  <Parameter Name="QueueItemProperties" Type="mscrm.queueitem" />
  <ReturnType Type="mscrm.AddToQueueResponse" Nullable="false" />
</Action>
```

 <span data-ttu-id="03c41-129">This bound action is equivalent to the <xref:Microsoft.Crm.Sdk.Messages.AddToQueueRequest> used by the organization service.</span><span class="sxs-lookup"><span data-stu-id="03c41-129">This bound action is equivalent to the <xref:Microsoft.Crm.Sdk.Messages.AddToQueueRequest> used by the organization service.</span></span> <span data-ttu-id="03c41-130">In the Web API this action is bound to the <xref href="Microsoft.Dynamics.CRM.queue?text=queue EntityType" />) that represents the <xref:Microsoft.Crm.Sdk.Messages.AddToQueueRequest>.<xref:Microsoft.Crm.Sdk.Messages.AddToQueueRequest.DestinationQueueId></span><span class="sxs-lookup"><span data-stu-id="03c41-130">In the Web API this action is bound to the <xref href="Microsoft.Dynamics.CRM.queue?text=queue EntityType" />) that represents the <xref:Microsoft.Crm.Sdk.Messages.AddToQueueRequest>.<xref:Microsoft.Crm.Sdk.Messages.AddToQueueRequest.DestinationQueueId></span></span> <span data-ttu-id="03c41-131">property.</span><span class="sxs-lookup"><span data-stu-id="03c41-131">property.</span></span> <span data-ttu-id="03c41-132">This action accepts several additional parameters and returns a <xref href="Microsoft.Dynamics.CRM.AddToQueueResponse?text=AddToQueueResponse ComplexType" /> corresponding to the <xref:Microsoft.Crm.Sdk.Messages.AddToQueueResponse> returned by the organization service.</span><span class="sxs-lookup"><span data-stu-id="03c41-132">This action accepts several additional parameters and returns a <xref href="Microsoft.Dynamics.CRM.AddToQueueResponse?text=AddToQueueResponse ComplexType" /> corresponding to the <xref:Microsoft.Crm.Sdk.Messages.AddToQueueResponse> returned by the organization service.</span></span> <span data-ttu-id="03c41-133">When an action returns a complex type, the definition of the complex type will appear directly above the action in the CSDL.</span><span class="sxs-lookup"><span data-stu-id="03c41-133">When an action returns a complex type, the definition of the complex type will appear directly above the action in the CSDL.</span></span>

 <span data-ttu-id="03c41-134">A bound action must be invoked using a URI to set the first parameter value.</span><span class="sxs-lookup"><span data-stu-id="03c41-134">A bound action must be invoked using a URI to set the first parameter value.</span></span> <span data-ttu-id="03c41-135">You cannot set it as a named parameter value.</span><span class="sxs-lookup"><span data-stu-id="03c41-135">You cannot set it as a named parameter value.</span></span>

 <span data-ttu-id="03c41-136">When invoking a bound function, you must include the full name of the function including the `Microsoft.Dynamics.CRM` namespace.</span><span class="sxs-lookup"><span data-stu-id="03c41-136">When invoking a bound function, you must include the full name of the function including the `Microsoft.Dynamics.CRM` namespace.</span></span> <span data-ttu-id="03c41-137">If you do not include the full name, you will get the following error: Status Code:400 Request message has unresolved parameters.</span><span class="sxs-lookup"><span data-stu-id="03c41-137">If you do not include the full name, you will get the following error: Status Code:400 Request message has unresolved parameters.</span></span>

 <span data-ttu-id="03c41-138">The following example shows using the <xref href="Microsoft.Dynamics.CRM.AddToQueue?text=AddToQueue Action" /> to add a letter to a queue.</span><span class="sxs-lookup"><span data-stu-id="03c41-138">The following example shows using the <xref href="Microsoft.Dynamics.CRM.AddToQueue?text=AddToQueue Action" /> to add a letter to a queue.</span></span> <span data-ttu-id="03c41-139">Because the type of the `Target` parameter type is not specific (`mscrm.crmbaseentity`), you must explicitly declare type of the object using the `@odata.type` property value of the full name of the entity, including the `Microsoft.Dynamics.CRM` namespace.</span><span class="sxs-lookup"><span data-stu-id="03c41-139">Because the type of the `Target` parameter type is not specific (`mscrm.crmbaseentity`), you must explicitly declare type of the object using the `@odata.type` property value of the full name of the entity, including the `Microsoft.Dynamics.CRM` namespace.</span></span> <span data-ttu-id="03c41-140">In this case, `Microsoft.Dynamics.CRM.letter`.</span><span class="sxs-lookup"><span data-stu-id="03c41-140">In this case, `Microsoft.Dynamics.CRM.letter`.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="03c41-141">[Specify entity parameter type](#bkmk_specifyentityparametertype)</span><span class="sxs-lookup"><span data-stu-id="03c41-141">[Specify entity parameter type](#bkmk_specifyentityparametertype)</span></span>

 <span data-ttu-id="03c41-142">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="03c41-142">**Request**</span></span>

```http
POST [Organization URI]/api/data/v9.0/queues(56ae8258-4878-e511-80d4-00155d2a68d1)/Microsoft.Dynamics.CRM.AddToQueue HTTP/1.1
Accept: application/json
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0

{
 "Target": {
  "activityid": "59ae8258-4878-e511-80d4-00155d2a68d1",
  "@odata.type": "Microsoft.Dynamics.CRM.letter"
 }
}
```

 <span data-ttu-id="03c41-143">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="03c41-143">**Response**</span></span>

```http

HTTP/1.1 200 OK
Content-Type: application/json; odata.metadata=minimal
OData-Version: 4.0

{
 "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#Microsoft.Dynamics.CRM.AddToQueueResponse",
 "QueueItemId": "5aae8258-4878-e511-80d4-00155d2a68d1"
}
```

<a name="bkmk_customActions"></a>

## <a name="use-a-custom-action"></a><span data-ttu-id="03c41-144">Use a custom action</span><span class="sxs-lookup"><span data-stu-id="03c41-144">Use a custom action</span></span>

 <span data-ttu-id="03c41-145">If you define custom actions for your organization or solution these will also be included in the [CSDL metadata document](web-api-types-operations.md#bkmk_csdl).</span><span class="sxs-lookup"><span data-stu-id="03c41-145">If you define custom actions for your organization or solution these will also be included in the [CSDL metadata document](web-api-types-operations.md#bkmk_csdl).</span></span> <span data-ttu-id="03c41-146">For information about creating actions using the customization tools in the application, see the TechNet topic [Actions](https://technet.microsoft.com/library/dn531060.aspx).</span><span class="sxs-lookup"><span data-stu-id="03c41-146">For information about creating actions using the customization tools in the application, see the TechNet topic [Actions](https://technet.microsoft.com/library/dn531060.aspx).</span></span> <span data-ttu-id="03c41-147">For information about creating and using your own custom actions, see [Create your own actions](../create-own-actions.md).</span><span class="sxs-lookup"><span data-stu-id="03c41-147">For information about creating and using your own custom actions, see [Create your own actions](../create-own-actions.md).</span></span>

 <span data-ttu-id="03c41-148">Regardless of whether the operations included in your custom action have side effects, they can potentially modify data and therefore are considered actions rather than functions.</span><span class="sxs-lookup"><span data-stu-id="03c41-148">Regardless of whether the operations included in your custom action have side effects, they can potentially modify data and therefore are considered actions rather than functions.</span></span> <span data-ttu-id="03c41-149">There is no way to create a custom function.</span><span class="sxs-lookup"><span data-stu-id="03c41-149">There is no way to create a custom function.</span></span>

### <a name="custom-action-example-add-a-note-to-a-contact"></a><span data-ttu-id="03c41-150">Custom action example: Add a note to a contact</span><span class="sxs-lookup"><span data-stu-id="03c41-150">Custom action example: Add a note to a contact</span></span>

 <span data-ttu-id="03c41-151">Let’s say that you want to create a custom action that will add a new note to a specific contact.</span><span class="sxs-lookup"><span data-stu-id="03c41-151">Let’s say that you want to create a custom action that will add a new note to a specific contact.</span></span> <span data-ttu-id="03c41-152">You can create a custom action bound to the contact entity with the following properties.</span><span class="sxs-lookup"><span data-stu-id="03c41-152">You can create a custom action bound to the contact entity with the following properties.</span></span>

|<span data-ttu-id="03c41-153">UI Label</span><span class="sxs-lookup"><span data-stu-id="03c41-153">UI Label</span></span>|<span data-ttu-id="03c41-154">Value</span><span class="sxs-lookup"><span data-stu-id="03c41-154">Value</span></span>|
|--------------|-----------|
|<span data-ttu-id="03c41-155">**Tên quy trình**</span><span class="sxs-lookup"><span data-stu-id="03c41-155">**Process Name**</span></span>|<span data-ttu-id="03c41-156">AddNoteToContact</span><span class="sxs-lookup"><span data-stu-id="03c41-156">AddNoteToContact</span></span>|
|<span data-ttu-id="03c41-157">**Tên Duy nhất**</span><span class="sxs-lookup"><span data-stu-id="03c41-157">**Unique Name**</span></span>|<span data-ttu-id="03c41-158">new_AddNoteToContact</span><span class="sxs-lookup"><span data-stu-id="03c41-158">new_AddNoteToContact</span></span>|
|<span data-ttu-id="03c41-159">**Thực thể**</span><span class="sxs-lookup"><span data-stu-id="03c41-159">**Entity**</span></span>|<span data-ttu-id="03c41-160">người liên hệ</span><span class="sxs-lookup"><span data-stu-id="03c41-160">Contact</span></span>|
|<span data-ttu-id="03c41-161">**Thể loại**</span><span class="sxs-lookup"><span data-stu-id="03c41-161">**Category**</span></span>|<span data-ttu-id="03c41-162">Hành động</span><span class="sxs-lookup"><span data-stu-id="03c41-162">Action</span></span>|

 <span data-ttu-id="03c41-163">**Process Arguments**</span><span class="sxs-lookup"><span data-stu-id="03c41-163">**Process Arguments**</span></span>

|<span data-ttu-id="03c41-164">Tên</span><span class="sxs-lookup"><span data-stu-id="03c41-164">Name</span></span>|<span data-ttu-id="03c41-165">Loại</span><span class="sxs-lookup"><span data-stu-id="03c41-165">Type</span></span>|<span data-ttu-id="03c41-166">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="03c41-166">Required</span></span>|<span data-ttu-id="03c41-167">Hướng</span><span class="sxs-lookup"><span data-stu-id="03c41-167">Direction</span></span>|
|----------|----------|--------------|---------------|
|<span data-ttu-id="03c41-168">NoteTitle</span><span class="sxs-lookup"><span data-stu-id="03c41-168">NoteTitle</span></span>|<span data-ttu-id="03c41-169">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="03c41-169">String</span></span>|<span data-ttu-id="03c41-170">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="03c41-170">Required</span></span>|<span data-ttu-id="03c41-171">Đầu vào</span><span class="sxs-lookup"><span data-stu-id="03c41-171">Input</span></span>|
|<span data-ttu-id="03c41-172">NoteText</span><span class="sxs-lookup"><span data-stu-id="03c41-172">NoteText</span></span>|<span data-ttu-id="03c41-173">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="03c41-173">String</span></span>|<span data-ttu-id="03c41-174">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="03c41-174">Required</span></span>|<span data-ttu-id="03c41-175">Đầu vào</span><span class="sxs-lookup"><span data-stu-id="03c41-175">Input</span></span>|
|<span data-ttu-id="03c41-176">NoteReference</span><span class="sxs-lookup"><span data-stu-id="03c41-176">NoteReference</span></span>|<span data-ttu-id="03c41-177">EntityReference</span><span class="sxs-lookup"><span data-stu-id="03c41-177">EntityReference</span></span>|<span data-ttu-id="03c41-178">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="03c41-178">Required</span></span>|<span data-ttu-id="03c41-179">Đầu ra</span><span class="sxs-lookup"><span data-stu-id="03c41-179">Output</span></span>|

 <span data-ttu-id="03c41-180">**Bước**</span><span class="sxs-lookup"><span data-stu-id="03c41-180">**Steps**</span></span>

|<span data-ttu-id="03c41-181">Tên</span><span class="sxs-lookup"><span data-stu-id="03c41-181">Name</span></span>|<span data-ttu-id="03c41-182">Step Type</span><span class="sxs-lookup"><span data-stu-id="03c41-182">Step Type</span></span>|<span data-ttu-id="03c41-183">Mô tả</span><span class="sxs-lookup"><span data-stu-id="03c41-183">Description</span></span>|
|----------|---------------|-----------------|
|<span data-ttu-id="03c41-184">Create the note</span><span class="sxs-lookup"><span data-stu-id="03c41-184">Create the note</span></span>|<span data-ttu-id="03c41-185">Tạo Bản ghi</span><span class="sxs-lookup"><span data-stu-id="03c41-185">Create Record</span></span>|<span data-ttu-id="03c41-186">Title = {NoteTitle(Arguments)}</span><span class="sxs-lookup"><span data-stu-id="03c41-186">Title = {NoteTitle(Arguments)}</span></span><br /> <span data-ttu-id="03c41-187">Note Body = {NoteText(Arguments)}</span><span class="sxs-lookup"><span data-stu-id="03c41-187">Note Body = {NoteText(Arguments)}</span></span><br /> <span data-ttu-id="03c41-188">Regarding = {Contact{Contact}}</span><span class="sxs-lookup"><span data-stu-id="03c41-188">Regarding = {Contact{Contact}}</span></span>|
|<span data-ttu-id="03c41-189">Return a reference to the note</span><span class="sxs-lookup"><span data-stu-id="03c41-189">Return a reference to the note</span></span>|<span data-ttu-id="03c41-190">Gán giá trị</span><span class="sxs-lookup"><span data-stu-id="03c41-190">Assign Value</span></span>|<span data-ttu-id="03c41-191">NoteReference Value = {Note(Create the note (Note))}</span><span class="sxs-lookup"><span data-stu-id="03c41-191">NoteReference Value = {Note(Create the note (Note))}</span></span>|

 <span data-ttu-id="03c41-192">After you publish and activate the custom action, when you download the CSDL you will find this new action defined.</span><span class="sxs-lookup"><span data-stu-id="03c41-192">After you publish and activate the custom action, when you download the CSDL you will find this new action defined.</span></span>

```xml

<Action Name="new_AddNoteToContact" IsBound="true">
  <Parameter Name="entity" Type="mscrm.contact" Nullable="false" />
  <Parameter Name="NoteTitle" Type="Edm.String" Nullable="false" Unicode="false" />
  <Parameter Name="NoteText" Type="Edm.String" Nullable="false" Unicode="false" />
  <ReturnType Type="mscrm.annotation" Nullable="false" />
</Action>
```

 <span data-ttu-id="03c41-193">The following HTTP request and response shows how to call the custom action and the response it returns if successful.</span><span class="sxs-lookup"><span data-stu-id="03c41-193">The following HTTP request and response shows how to call the custom action and the response it returns if successful.</span></span>  

 <span data-ttu-id="03c41-194">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="03c41-194">**Request**</span></span>

```http
POST [Organization URI]/api/data/v9.0/contacts(94d8c461-a27a-e511-80d2-00155d2a68d2)/Microsoft.Dynamics.CRM.new_AddNoteToContact HTTP/1.1
Accept: application/json
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0

{
 "NoteTitle": "New Note Title",
 "NoteText": "This is the text of the note"
}
```


 <span data-ttu-id="03c41-195">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="03c41-195">**Response**</span></span>

```http

HTTP/1.1 200 OK
Content-Type: application/json; odata.metadata=minimal
OData-Version: 4.0

{
 "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#annotations/$entity",
 "annotationid": "9ad8c461-a27a-e511-80d2-00155d2a68d2"
}
```

<a name="bkmk_specifyentityparametertype"></a>

## <a name="specify-entity-parameter-type"></a><span data-ttu-id="03c41-196">Specify entity parameter type</span><span class="sxs-lookup"><span data-stu-id="03c41-196">Specify entity parameter type</span></span>

 <span data-ttu-id="03c41-197">When an action requires an entity as a parameter and the type of entity is ambiguous, you must use the `@odata.type` property to specify the type of entity.</span><span class="sxs-lookup"><span data-stu-id="03c41-197">When an action requires an entity as a parameter and the type of entity is ambiguous, you must use the `@odata.type` property to specify the type of entity.</span></span> <span data-ttu-id="03c41-198">The value of this property is the fully qualified name of the entity, which follows this pattern: `Microsoft.Dynamics.CRM.`+*\<entity logical name>*.</span><span class="sxs-lookup"><span data-stu-id="03c41-198">The value of this property is the fully qualified name of the entity, which follows this pattern: `Microsoft.Dynamics.CRM.`+*\<entity logical name>*.</span></span>

 <span data-ttu-id="03c41-199">As shown in the [Bound actions](#bkmk_boundActions) section above, the `Target` parameter to the <xref href="Microsoft.Dynamics.CRM.AddToQueue?text=AddToQueue Action" /> is an activity.</span><span class="sxs-lookup"><span data-stu-id="03c41-199">As shown in the [Bound actions](#bkmk_boundActions) section above, the `Target` parameter to the <xref href="Microsoft.Dynamics.CRM.AddToQueue?text=AddToQueue Action" /> is an activity.</span></span> <span data-ttu-id="03c41-200">But since all activities inherit from the <xref href="Microsoft.Dynamics.CRM.activitypointer?text=activitypointer EntityType" />, you must include the following property in the entity JSON to specify the type of entity is a letter: `"@odata.type": "Microsoft.Dynamics.CRM.letter"`.</span><span class="sxs-lookup"><span data-stu-id="03c41-200">But since all activities inherit from the <xref href="Microsoft.Dynamics.CRM.activitypointer?text=activitypointer EntityType" />, you must include the following property in the entity JSON to specify the type of entity is a letter: `"@odata.type": "Microsoft.Dynamics.CRM.letter"`.</span></span>

 <span data-ttu-id="03c41-201">Two other examples are <xref href="Microsoft.Dynamics.CRM.AddMembersTeam?text=AddMembersTeam Action" /> and <xref href="Microsoft.Dynamics.CRM.RemoveMembersTeam?text=RemoveMembersTeam Action" /> because the `Members` parameter is a collection of  <xref href="Microsoft.Dynamics.CRM.systemuser?text=systemuser EntityType" /> which inherits it's `ownerid` primary key from the <xref href="Microsoft.Dynamics.CRM.principal?text=principal EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="03c41-201">Two other examples are <xref href="Microsoft.Dynamics.CRM.AddMembersTeam?text=AddMembersTeam Action" /> and <xref href="Microsoft.Dynamics.CRM.RemoveMembersTeam?text=RemoveMembersTeam Action" /> because the `Members` parameter is a collection of  <xref href="Microsoft.Dynamics.CRM.systemuser?text=systemuser EntityType" /> which inherits it's `ownerid` primary key from the <xref href="Microsoft.Dynamics.CRM.principal?text=principal EntityType" />.</span></span> <span data-ttu-id="03c41-202">If you pass the following JSON to represent a single systemuser in the collection, it is clear that the entity is a systemuser and not a <xref href="Microsoft.Dynamics.CRM.team?text=team EntityType" />, which also inherits from the principal entitytype.</span><span class="sxs-lookup"><span data-stu-id="03c41-202">If you pass the following JSON to represent a single systemuser in the collection, it is clear that the entity is a systemuser and not a <xref href="Microsoft.Dynamics.CRM.team?text=team EntityType" />, which also inherits from the principal entitytype.</span></span>

```json
{
 "Members": [{
  "@odata.type": "Microsoft.Dynamics.CRM.systemuser",
  "ownerid": "5dbf5efc-4507-e611-80de-5065f38a7b01"
 }]
}
```

 <span data-ttu-id="03c41-203">If you do not specify the type of entity in this situation, you can get the following error: `"EdmEntityObject passed should have the key property value set."`.</span><span class="sxs-lookup"><span data-stu-id="03c41-203">If you do not specify the type of entity in this situation, you can get the following error: `"EdmEntityObject passed should have the key property value set."`.</span></span>

### <a name="see-also"></a><span data-ttu-id="03c41-204">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="03c41-204">See also</span></span>

 [<span data-ttu-id="03c41-205">Web API Functions and Actions Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="03c41-205">Web API Functions and Actions Sample (C#)</span></span>](web-api-functions-actions-sample-csharp.md)<br />
 [<span data-ttu-id="03c41-206">Web API Functions and Actions Sample (Client-side JavaScript)</span><span class="sxs-lookup"><span data-stu-id="03c41-206">Web API Functions and Actions Sample (Client-side JavaScript)</span></span>](web-api-functions-actions-sample-client-side-javascript.md)<br />
 [<span data-ttu-id="03c41-207">Perform operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="03c41-207">Perform operations using the Web API</span></span>](perform-operations-web-api.md)<br />
 [<span data-ttu-id="03c41-208">Compose Http requests and handle errors</span><span class="sxs-lookup"><span data-stu-id="03c41-208">Compose Http requests and handle errors</span></span>](compose-http-requests-handle-errors.md)<br />
 [<span data-ttu-id="03c41-209">Query Data using the Web API</span><span class="sxs-lookup"><span data-stu-id="03c41-209">Query Data using the Web API</span></span>](query-data-web-api.md)<br />
 [<span data-ttu-id="03c41-210">Create an entity using the Web API</span><span class="sxs-lookup"><span data-stu-id="03c41-210">Create an entity using the Web API</span></span>](create-entity-web-api.md)<br />
 [<span data-ttu-id="03c41-211">Retrieve an entity using the Web API</span><span class="sxs-lookup"><span data-stu-id="03c41-211">Retrieve an entity using the Web API</span></span>](retrieve-entity-using-web-api.md)<br />
 [<span data-ttu-id="03c41-212">Update and delete entities using the Web API</span><span class="sxs-lookup"><span data-stu-id="03c41-212">Update and delete entities using the Web API</span></span>](update-delete-entities-using-web-api.md)<br />
 [<span data-ttu-id="03c41-213">Associate and disassociate entities using the Web API</span><span class="sxs-lookup"><span data-stu-id="03c41-213">Associate and disassociate entities using the Web API</span></span>](associate-disassociate-entities-using-web-api.md)<br />
 [<span data-ttu-id="03c41-214">Use Web API functions</span><span class="sxs-lookup"><span data-stu-id="03c41-214">Use Web API functions</span></span>](use-web-api-functions.md)<br />
 [<span data-ttu-id="03c41-215">Execute batch operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="03c41-215">Execute batch operations using the Web API</span></span>](execute-batch-operations-using-web-api.md)<br />
 [<span data-ttu-id="03c41-216">Impersonate another user using the Web API</span><span class="sxs-lookup"><span data-stu-id="03c41-216">Impersonate another user using the Web API</span></span>](impersonate-another-user-web-api.md)<br />
 [<span data-ttu-id="03c41-217">Perform conditional operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="03c41-217">Perform conditional operations using the Web API</span></span>](perform-conditional-operations-using-web-api.md)<br />
