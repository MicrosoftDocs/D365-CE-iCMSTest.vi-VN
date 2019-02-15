---
title: Work with attribute metadata (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'The sample code demonstrates creating, retriving, updating and attributes, and creating lookup, creating a picklist that uses a global option set, inserting a new status value, updating a state value and so on. '
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 5fc61379-4811-4b3c-9bac-2227ce5662e2
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d125377c604634edc2a1f205f4782aebf4e87a0e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387491"
---
# <a name="work-with-attribute-metadata"></a><span data-ttu-id="ccd6d-103">Work with attribute metadata</span><span class="sxs-lookup"><span data-stu-id="ccd6d-103">Work with attribute metadata</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ccd6d-104">This topic uses code snippets from the [Sample: Work with attribute metadata](sample-work-attribute-metadata.md) to show how to perform common tasks when working with attributes.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-104">This topic uses code snippets from the [Sample: Work with attribute metadata](sample-work-attribute-metadata.md) to show how to perform common tasks when working with attributes.</span></span>
  
<a name="BKMK_CreateAttributes"></a>   
## <a name="create-attributes"></a><span data-ttu-id="ccd6d-105">Create attributes</span><span class="sxs-lookup"><span data-stu-id="ccd6d-105">Create attributes</span></span>  
 <span data-ttu-id="ccd6d-106">You create attributes by defining one of the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata> types and then passing it to the <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest> message.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-106">You create attributes by defining one of the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata> types and then passing it to the <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest> message.</span></span>  
  
 <span data-ttu-id="ccd6d-107">The following sample defines the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata> for a number of different types of attributes and adds them to a `List<AttributeMetadata>`.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-107">The following sample defines the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata> for a number of different types of attributes and adds them to a `List<AttributeMetadata>`.</span></span> <span data-ttu-id="ccd6d-108">At the end of the code the attribute definitions are passed to an instance of the <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest> class and the attribute is created using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span><span class="sxs-lookup"><span data-stu-id="ccd6d-108">At the end of the code the attribute definitions are passed to an instance of the <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest> class and the attribute is created using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span></span> <span data-ttu-id="ccd6d-109">method.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-109">method.</span></span>  
  
 <span data-ttu-id="ccd6d-110">The following sample assumes that the current customization prefix is ‘new’ because that is the default customization prefix for the organization solution publisher.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-110">The following sample assumes that the current customization prefix is ‘new’ because that is the default customization prefix for the organization solution publisher.</span></span> <span data-ttu-id="ccd6d-111">You should use the customization prefix for the solution publisher that makes sense for your solution context.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-111">You should use the customization prefix for the solution publisher that makes sense for your solution context.</span></span>  
  
 [!code-csharp[Attributes#WorkWithAttributes2](../../snippets/csharp/CRMV8/attributes/cs/workwithattributes2.cs#workwithattributes2)]  
  
<a name="BKMK_RetrieveAttribute"></a>   
## <a name="retrieve-an-attribute"></a><span data-ttu-id="ccd6d-112">Retrieve an attribute</span><span class="sxs-lookup"><span data-stu-id="ccd6d-112">Retrieve an attribute</span></span>  
 <span data-ttu-id="ccd6d-113">This sample shows how to retrieve the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata> for an attribute using the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAttributeRequest>.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-113">This sample shows how to retrieve the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata> for an attribute using the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAttributeRequest>.</span></span> <span data-ttu-id="ccd6d-114">This sample retrieves the metadata for a custom <xref:Microsoft.Xrm.Sdk.Metadata.StringAttributeMetadata> attribute called ‘new_string’ from the Contact entity that was created in [Create Attributes](work-attribute-metadata.md#BKMK_CreateAttributes).</span><span class="sxs-lookup"><span data-stu-id="ccd6d-114">This sample retrieves the metadata for a custom <xref:Microsoft.Xrm.Sdk.Metadata.StringAttributeMetadata> attribute called ‘new_string’ from the Contact entity that was created in [Create Attributes](work-attribute-metadata.md#BKMK_CreateAttributes).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ccd6d-115">Because <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAttributeRequest.RetrieveAsIfPublished> is true, this request returns the current unpublished definition of this attribute.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-115">Because <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAttributeRequest.RetrieveAsIfPublished> is true, this request returns the current unpublished definition of this attribute.</span></span> <span data-ttu-id="ccd6d-116">You might use this if you are creating an Attribute editor and you want to retrieve the unpublished definition of the attribute.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-116">You might use this if you are creating an Attribute editor and you want to retrieve the unpublished definition of the attribute.</span></span> <span data-ttu-id="ccd6d-117">Otherwise, you should not specify `RetrieveAsIfPublished`.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-117">Otherwise, you should not specify `RetrieveAsIfPublished`.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="ccd6d-118">[Retrieving unpublished metadata](../customize-dev/publish-customizations.md#retrieving-unpublished-metadata).</span><span class="sxs-lookup"><span data-stu-id="ccd6d-118">[Retrieving unpublished metadata](../customize-dev/publish-customizations.md#retrieving-unpublished-metadata).</span></span>  
  
 [!code-csharp[Attributes#WorkWithAttributes4](../../snippets/csharp/CRMV8/attributes/cs/workwithattributes4.cs#workwithattributes4)]  
  
<a name="BKMK_UpdateAttribute"></a>   
## <a name="update-an-attribute"></a><span data-ttu-id="ccd6d-119">Update an attribute</span><span class="sxs-lookup"><span data-stu-id="ccd6d-119">Update an attribute</span></span>  
 <span data-ttu-id="ccd6d-120">This sample shows how to update an attribute.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-120">This sample shows how to update an attribute.</span></span> <span data-ttu-id="ccd6d-121">This sample uses the <xref:Microsoft.Xrm.Sdk.Messages.UpdateAttributeRequest> to change the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.DisplayName></span><span class="sxs-lookup"><span data-stu-id="ccd6d-121">This sample uses the <xref:Microsoft.Xrm.Sdk.Messages.UpdateAttributeRequest> to change the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.DisplayName></span></span> <span data-ttu-id="ccd6d-122">property of a previously retrieved custom attribute for the `Contact` entity.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-122">property of a previously retrieved custom attribute for the `Contact` entity.</span></span>  
  
 [!code-csharp[Attributes#WorkWithAttributes5](../../snippets/csharp/CRMV8/attributes/cs/workwithattributes5.cs#workwithattributes5)]  
  
<a name="BKMK_CreateLookupAttribute"></a>   
## <a name="create-a-lookup-attribute"></a><span data-ttu-id="ccd6d-123">Create a lookup attribute</span><span class="sxs-lookup"><span data-stu-id="ccd6d-123">Create a lookup attribute</span></span>  
 <span data-ttu-id="ccd6d-124">A lookup attribute is created by using the <xref:Microsoft.Xrm.Sdk.Messages.CreateOneToManyRequest>.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-124">A lookup attribute is created by using the <xref:Microsoft.Xrm.Sdk.Messages.CreateOneToManyRequest>.</span></span>  
  
 <span data-ttu-id="ccd6d-125">This sample code shows how to create a lookup attribute.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-125">This sample code shows how to create a lookup attribute.</span></span> <span data-ttu-id="ccd6d-126">For the complete sample, see [Sample: Create and update entity metadata](sample-create-update-entity-metadata.md)</span><span class="sxs-lookup"><span data-stu-id="ccd6d-126">For the complete sample, see [Sample: Create and update entity metadata](sample-create-update-entity-metadata.md)</span></span>  
  
 [!code-csharp[Entities#CreateUpdateEntityMetadata5](../../snippets/csharp/CRMV8/entities/cs/createupdateentitymetadata5.cs#createupdateentitymetadata5)]  
  
<a name="BKMK_createcustlookup"></a>   
## <a name="create-a-customer-lookup-attribute"></a><span data-ttu-id="ccd6d-127">Create a customer lookup attribute</span><span class="sxs-lookup"><span data-stu-id="ccd6d-127">Create a customer lookup attribute</span></span>  
 <span data-ttu-id="ccd6d-128">Unlike a lookup attribute, a customer lookup attribute is created using the <xref:Microsoft.Xrm.Sdk.Messages.CreateCustomerRelationshipsRequest> message, which adds two relationships to the lookup attribute: one to the `Account` entity and the other one to the `Contact` entity.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-128">Unlike a lookup attribute, a customer lookup attribute is created using the <xref:Microsoft.Xrm.Sdk.Messages.CreateCustomerRelationshipsRequest> message, which adds two relationships to the lookup attribute: one to the `Account` entity and the other one to the `Contact` entity.</span></span> <span data-ttu-id="ccd6d-129">You cannot add relationship to any other entity except for `Account` and `Contact` entities for a customer lookup attribute.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-129">You cannot add relationship to any other entity except for `Account` and `Contact` entities for a customer lookup attribute.</span></span>  
  
> [!NOTE]
> [!INCLUDE[cc_feature_included_with_update_8_1_0_admins](../../includes/cc-feature-included-with-update-8-1-0-admins.md)]  
  
 <span data-ttu-id="ccd6d-130">This sample code shows how to create a customer lookup attribute.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-130">This sample code shows how to create a customer lookup attribute.</span></span> <span data-ttu-id="ccd6d-131">For the complete sample, see [Sample: Create and update entity metadata](sample-create-update-entity-metadata.md)</span><span class="sxs-lookup"><span data-stu-id="ccd6d-131">For the complete sample, see [Sample: Create and update entity metadata](sample-create-update-entity-metadata.md)</span></span>  
  
 [!code-csharp[Entities#CreateUpdateEntityMetadata13](../../snippets/csharp/CRMV8/entities/cs/createupdateentitymetadata13.cs#createupdateentitymetadata13)]  
  
<a name="BKMK_CreatePicklistGlobalOptionSet"></a>   
## <a name="create-a-picklist-that-uses-a-global-option-set"></a><span data-ttu-id="ccd6d-132">Create a picklist that uses a global option set</span><span class="sxs-lookup"><span data-stu-id="ccd6d-132">Create a picklist that uses a global option set</span></span>  
 <span data-ttu-id="ccd6d-133">This sample shows how to create a <xref:Microsoft.Xrm.Sdk.Metadata.PicklistAttributeMetadata> attribute that is associated with a global option set.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-133">This sample shows how to create a <xref:Microsoft.Xrm.Sdk.Metadata.PicklistAttributeMetadata> attribute that is associated with a global option set.</span></span>  
  
 <span data-ttu-id="ccd6d-134">The following sample uses <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest> to set the options for a <xref:Microsoft.Xrm.Sdk.Metadata.PicklistAttributeMetadata> attribute to use a global option set with a name represented by the string variable `_globalOptionSetName`.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-134">The following sample uses <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest> to set the options for a <xref:Microsoft.Xrm.Sdk.Metadata.PicklistAttributeMetadata> attribute to use a global option set with a name represented by the string variable `_globalOptionSetName`.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="ccd6d-135">[Customize Global Option Sets in Dynamics 365 for Customer Engagement apps](customize-global-option-sets.md)</span><span class="sxs-lookup"><span data-stu-id="ccd6d-135">[Customize Global Option Sets in Dynamics 365 for Customer Engagement apps](customize-global-option-sets.md)</span></span>  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets3](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets3.cs#workwithglobaloptionsets3)]  
  
<a name="BKMK_InsertNewStatusValue"></a>   
## <a name="insert-a-new-status-value"></a><span data-ttu-id="ccd6d-136">Insert a new status value</span><span class="sxs-lookup"><span data-stu-id="ccd6d-136">Insert a new status value</span></span>  
 <span data-ttu-id="ccd6d-137">This sample shows how to insert a new **Status Reason** option for <xref:Microsoft.Xrm.Sdk.Metadata.StatusAttributeMetadata> attribute.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-137">This sample shows how to insert a new **Status Reason** option for <xref:Microsoft.Xrm.Sdk.Metadata.StatusAttributeMetadata> attribute.</span></span>  
  
 <span data-ttu-id="ccd6d-138">The following sample uses the <xref:Microsoft.Xrm.Sdk.Messages.InsertStatusValueRequest> to specify a new option for the `Contact` entity `Contact.StatusCode` attribute that is valid when the `Contact.StateCode` is 0 (Active).</span><span class="sxs-lookup"><span data-stu-id="ccd6d-138">The following sample uses the <xref:Microsoft.Xrm.Sdk.Messages.InsertStatusValueRequest> to specify a new option for the `Contact` entity `Contact.StatusCode` attribute that is valid when the `Contact.StateCode` is 0 (Active).</span></span> <span data-ttu-id="ccd6d-139">The <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span><span class="sxs-lookup"><span data-stu-id="ccd6d-139">The <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span></span> <span data-ttu-id="ccd6d-140">method processes the request.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-140">method processes the request.</span></span>  
  
 <span data-ttu-id="ccd6d-141">The following sample allows two valid **Status Reason** options for active contacts: **Active** and **Dormant**.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-141">The following sample allows two valid **Status Reason** options for active contacts: **Active** and **Dormant**.</span></span>  
  
 [!code-csharp[Attributes#WorkWithAttributes3](../../snippets/csharp/CRMV8/attributes/cs/workwithattributes3.cs#workwithattributes3)]  
  
<a name="BKMK_UpdateStateValue"></a>   
## <a name="update-a-state-value"></a><span data-ttu-id="ccd6d-142">Update a state value</span><span class="sxs-lookup"><span data-stu-id="ccd6d-142">Update a state value</span></span>  
 <span data-ttu-id="ccd6d-143">This sample shows how to change the label for an option in a <xref:Microsoft.Xrm.Sdk.Metadata.StateAttributeMetadata> attribute.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-143">This sample shows how to change the label for an option in a <xref:Microsoft.Xrm.Sdk.Metadata.StateAttributeMetadata> attribute.</span></span>  
  
 <span data-ttu-id="ccd6d-144">The following sample uses <xref:Microsoft.Xrm.Sdk.Messages.UpdateStateValueRequest> to change the `Contact.StateCode` option label from **Active** to **Open**.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-144">The following sample uses <xref:Microsoft.Xrm.Sdk.Messages.UpdateStateValueRequest> to change the `Contact.StateCode` option label from **Active** to **Open**.</span></span>  
  
 [!code-csharp[Attributes#WorkWithAttributes6](../../snippets/csharp/CRMV8/attributes/cs/workwithattributes6.cs#workwithattributes6)]  
  
 <span data-ttu-id="ccd6d-145">You cannot add or remove `StateCode` options, but you can change the labels for the options.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-145">You cannot add or remove `StateCode` options, but you can change the labels for the options.</span></span>  
  
<a name="BKMK_InsertNewOptionLocalOptionSet"></a>   
## <a name="insert-a-new-option-in-a-local-option-set"></a><span data-ttu-id="ccd6d-146">Insert a new option in a local option set</span><span class="sxs-lookup"><span data-stu-id="ccd6d-146">Insert a new option in a local option set</span></span>  
 <span data-ttu-id="ccd6d-147">This sample shows how to add a new option to a local option set.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-147">This sample shows how to add a new option to a local option set.</span></span> <span data-ttu-id="ccd6d-148">The following sample uses <xref:Microsoft.Xrm.Sdk.Messages.InsertOptionValueRequest> to add a new option to a custom <xref:Microsoft.Xrm.Sdk.Metadata.PicklistAttributeMetadata> attribute for the `Contact` entity.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-148">The following sample uses <xref:Microsoft.Xrm.Sdk.Messages.InsertOptionValueRequest> to add a new option to a custom <xref:Microsoft.Xrm.Sdk.Metadata.PicklistAttributeMetadata> attribute for the `Contact` entity.</span></span>  
  
 [!code-csharp[Attributes#WorkWithAttributes7](../../snippets/csharp/CRMV8/attributes/cs/workwithattributes7.cs#workwithattributes7)]  
  
<a name="BKMK_ChangeOrderOptionLocalOptionSet"></a>   
## <a name="change-the-order-of-options-in-a-local-option-set"></a><span data-ttu-id="ccd6d-149">Change the order of options in a local option set</span><span class="sxs-lookup"><span data-stu-id="ccd6d-149">Change the order of options in a local option set</span></span>  
 <span data-ttu-id="ccd6d-150">This sample shows how to change the order of options in a local option set.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-150">This sample shows how to change the order of options in a local option set.</span></span> <span data-ttu-id="ccd6d-151">The following sample retrieves a custom <xref:Microsoft.Xrm.Sdk.Metadata.PicklistAttributeMetadata> attribute and changes the order of the original options using the [OrderBy](https://msdn.microsoft.com/library/system.linq.enumerable.orderby.aspx)**LINQ** function to sort items in ascending order by the label text.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-151">The following sample retrieves a custom <xref:Microsoft.Xrm.Sdk.Metadata.PicklistAttributeMetadata> attribute and changes the order of the original options using the [OrderBy](https://msdn.microsoft.com/library/system.linq.enumerable.orderby.aspx)**LINQ** function to sort items in ascending order by the label text.</span></span> <span data-ttu-id="ccd6d-152">Then it uses <xref:Microsoft.Xrm.Sdk.Messages.OrderOptionRequest> to set the new order of the options for the attribute.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-152">Then it uses <xref:Microsoft.Xrm.Sdk.Messages.OrderOptionRequest> to set the new order of the options for the attribute.</span></span>  
  
 <span data-ttu-id="ccd6d-153">Use the [OrderByDecending](https://msdn.microsoft.com/library/system.linq.enumerable.orderbydescending.aspx) linq function to order the items in descending order.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-153">Use the [OrderByDecending](https://msdn.microsoft.com/library/system.linq.enumerable.orderbydescending.aspx) linq function to order the items in descending order.</span></span>  
  
 [!code-csharp[Attributes#WorkWithAttributes8](../../snippets/csharp/CRMV8/attributes/cs/workwithattributes8.cs#workwithattributes8)]  
  
<a name="BKMK_DeleteAttribute"></a>   
## <a name="delete-an-attribute"></a><span data-ttu-id="ccd6d-154">Delete an attribute</span><span class="sxs-lookup"><span data-stu-id="ccd6d-154">Delete an attribute</span></span>  
 <span data-ttu-id="ccd6d-155">This sample shows how to delete attributes stored in a `List<`<xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata>`>` that were created for the `Contact` entity in [Create Attributes](work-attribute-metadata.md#BKMK_CreateAttributes).</span><span class="sxs-lookup"><span data-stu-id="ccd6d-155">This sample shows how to delete attributes stored in a `List<`<xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata>`>` that were created for the `Contact` entity in [Create Attributes](work-attribute-metadata.md#BKMK_CreateAttributes).</span></span> <span data-ttu-id="ccd6d-156">For each <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata> the <xref:Microsoft.Xrm.Sdk.Messages.DeleteAttributeRequest> prepares the request that is processed using <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*>.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-156">For each <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata> the <xref:Microsoft.Xrm.Sdk.Messages.DeleteAttributeRequest> prepares the request that is processed using <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*>.</span></span>  
  
 [!code-csharp[Attributes#WorkWithAttributes9](../../snippets/csharp/CRMV8/attributes/cs/workwithattributes9.cs#workwithattributes9)]  
  
### <a name="see-also"></a><span data-ttu-id="ccd6d-157">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ccd6d-157">See also</span></span>  
 <span data-ttu-id="ccd6d-158">[Customize entity attribute metadata](../customize-entity-attribute-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="ccd6d-158">[Customize entity attribute metadata](../customize-entity-attribute-metadata.md) </span></span>  
 <span data-ttu-id="ccd6d-159">[Entity Attribute Metadata Messages](../entity-attribute-metadata-messages.md) </span><span class="sxs-lookup"><span data-stu-id="ccd6d-159">[Entity Attribute Metadata Messages](../entity-attribute-metadata-messages.md) </span></span>  
 <span data-ttu-id="ccd6d-160">[Sample: Work with Attributes](sample-work-attribute-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="ccd6d-160">[Sample: Work with Attributes](sample-work-attribute-metadata.md) </span></span>  
 [<span data-ttu-id="ccd6d-161">Customize Entity and Attribute Mappings</span><span class="sxs-lookup"><span data-stu-id="ccd6d-161">Customize Entity and Attribute Mappings</span></span>](../customize-entity-attribute-mappings.md)
