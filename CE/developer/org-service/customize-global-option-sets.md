---
title: Customize global option sets | MicrosoftDocs
ms.custom: ''
ms.date: 11/20/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 6786ff10-0e38-4f5c-b973-c682d1d60de5
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f71e64a19f907f8257d4adbf6aa0f821476ed12f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388234"
---
# <a name="customize-global-option-sets"></a><span data-ttu-id="1f4aa-102">Customize global option sets</span><span class="sxs-lookup"><span data-stu-id="1f4aa-102">Customize global option sets</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="1f4aa-103">Typically, you use global option sets to set fields so that different fields can share the same set of options, which are maintained in one location.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-103">Typically, you use global option sets to set fields so that different fields can share the same set of options, which are maintained in one location.</span></span> <span data-ttu-id="1f4aa-104">You can reuse global option sets.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-104">You can reuse global option sets.</span></span> <span data-ttu-id="1f4aa-105">You will also see them used in request parameters in a manner similar to an enumeration.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-105">You will also see them used in request parameters in a manner similar to an enumeration.</span></span>  
  
 <span data-ttu-id="1f4aa-106">When you define an option value by using <xref:Microsoft.Xrm.Sdk.Messages.CreateOptionSetRequest>, we recommend that you let the system assign a value.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-106">When you define an option value by using <xref:Microsoft.Xrm.Sdk.Messages.CreateOptionSetRequest>, we recommend that you let the system assign a value.</span></span> <span data-ttu-id="1f4aa-107">You do this by passing a **null** value when you create the new `OptionMetadata` instance.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-107">You do this by passing a **null** value when you create the new `OptionMetadata` instance.</span></span> <span data-ttu-id="1f4aa-108">When you define an option, it will contain an option value prefix specific to the context of the publisher set for the solution that the option set is created in.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-108">When you define an option, it will contain an option value prefix specific to the context of the publisher set for the solution that the option set is created in.</span></span> <span data-ttu-id="1f4aa-109">This prefix helps reduce the chance of creating duplicate option sets for a managed solution, and in any option sets that are defined in organizations where your managed solution is installed.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-109">This prefix helps reduce the chance of creating duplicate option sets for a managed solution, and in any option sets that are defined in organizations where your managed solution is installed.</span></span> <span data-ttu-id="1f4aa-110">For more information, see [Merge option set options](../understand-managed-solutions-merged.md#merge-option-set-options).</span><span class="sxs-lookup"><span data-stu-id="1f4aa-110">For more information, see [Merge option set options](../understand-managed-solutions-merged.md#merge-option-set-options).</span></span>  
 
 ## <a name="messages"></a><span data-ttu-id="1f4aa-111">Messages</span><span class="sxs-lookup"><span data-stu-id="1f4aa-111">Messages</span></span>  
 <span data-ttu-id="1f4aa-112">The following table lists the messages that you can use with global option sets.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-112">The following table lists the messages that you can use with global option sets.</span></span>  
  
|<span data-ttu-id="1f4aa-113">Thông báo</span><span class="sxs-lookup"><span data-stu-id="1f4aa-113">Message</span></span>|<span data-ttu-id="1f4aa-114">Web API Operation</span><span class="sxs-lookup"><span data-stu-id="1f4aa-114">Web API Operation</span></span>|<span data-ttu-id="1f4aa-115">SDK Assembly</span><span class="sxs-lookup"><span data-stu-id="1f4aa-115">SDK Assembly</span></span>|  
|-------------|----------------------------|--------------------------------|  
|<span data-ttu-id="1f4aa-116">CreateOptionSet</span><span class="sxs-lookup"><span data-stu-id="1f4aa-116">CreateOptionSet</span></span>|<span data-ttu-id="1f4aa-117">Use `POST` request to create a new global option set.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-117">Use `POST` request to create a new global option set.</span></span>|<xref:Microsoft.Xrm.Sdk.Messages.CreateOptionSetRequest>|  
|<span data-ttu-id="1f4aa-118">DeleteOptionSet</span><span class="sxs-lookup"><span data-stu-id="1f4aa-118">DeleteOptionSet</span></span>|<span data-ttu-id="1f4aa-119">Use `DELETE` request to delete a global optin set.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-119">Use `DELETE` request to delete a global optin set.</span></span>|<xref:Microsoft.Xrm.Sdk.Messages.DeleteOptionSetRequest>|  
|<span data-ttu-id="1f4aa-120">DeleteOptionValue</span><span class="sxs-lookup"><span data-stu-id="1f4aa-120">DeleteOptionValue</span></span></br><span data-ttu-id="1f4aa-121">Deletes one of the values in a global option set.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-121">Deletes one of the values in a global option set.</span></span>|<xref href="Microsoft.Dynamics.CRM.DeleteOptionValue?text=DeleteOptionValue Action" />|<xref:Microsoft.Xrm.Sdk.Messages.DeleteOptionValueRequest>|    
|<span data-ttu-id="1f4aa-122">InsertOptionValue</span><span class="sxs-lookup"><span data-stu-id="1f4aa-122">InsertOptionValue</span></span></br><span data-ttu-id="1f4aa-123">Inserts a new option into a global option set.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-123">Inserts a new option into a global option set.</span></span>|<xref href="Microsoft.Dynamics.CRM.InsertOptionValue?text=InsertOptionValue Action" />|<xref:Microsoft.Xrm.Sdk.Messages.InsertOptionValueRequest>|  
|<span data-ttu-id="1f4aa-124">InsertStatusValue</span><span class="sxs-lookup"><span data-stu-id="1f4aa-124">InsertStatusValue</span></span></br><span data-ttu-id="1f4aa-125">Inserts a new option into the global option set used in the `Status` attribute.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-125">Inserts a new option into the global option set used in the `Status` attribute.</span></span>|<xref href="Microsoft.Dynamics.CRM.InsertOptionValue?text=InsertStatusValue Action" />|<xref:Microsoft.Xrm.Sdk.Messages.InsertStatusValueRequest>|  
|<span data-ttu-id="1f4aa-126">OrderOption</span><span class="sxs-lookup"><span data-stu-id="1f4aa-126">OrderOption</span></span></br><span data-ttu-id="1f4aa-127">Changes the relative order of the options in an option set.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-127">Changes the relative order of the options in an option set.</span></span>|<xref href="Microsoft.Dynamics.CRM.OrderOption?text=OrderOption Action" />|<xref:Microsoft.Xrm.Sdk.Messages.OrderOptionRequest>|  
|<span data-ttu-id="1f4aa-128">RetrieveAllOptionSets</span><span class="sxs-lookup"><span data-stu-id="1f4aa-128">RetrieveAllOptionSets</span></span>|<span data-ttu-id="1f4aa-129">Use `GET` request to retrieve all the global option sets.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-129">Use `GET` request to retrieve all the global option sets.</span></span>|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllOptionSetsRequest>|  
|<span data-ttu-id="1f4aa-130">RetrieveOptionSet</span><span class="sxs-lookup"><span data-stu-id="1f4aa-130">RetrieveOptionSet</span></span>|<span data-ttu-id="1f4aa-131">Use `GET` request to retrieve a global option set.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-131">Use `GET` request to retrieve a global option set.</span></span>|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveOptionSetRequest>|    
|<span data-ttu-id="1f4aa-132">UpdateOptionSet</span><span class="sxs-lookup"><span data-stu-id="1f4aa-132">UpdateOptionSet</span></span>|<span data-ttu-id="1f4aa-133">Use `PUT` request to update a global option set.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-133">Use `PUT` request to update a global option set.</span></span>|<xref:Microsoft.Xrm.Sdk.Messages.UpdateOptionSetRequest>|  
|<span data-ttu-id="1f4aa-134">UpdateOptionValue</span><span class="sxs-lookup"><span data-stu-id="1f4aa-134">UpdateOptionValue</span></span>|</br><span data-ttu-id="1f4aa-135">Updates an option in a global option set.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-135">Updates an option in a global option set.</span></span>|<xref:Microsoft.Xrm.Sdk.Messages.UpdateOptionValueRequest>|  
|<span data-ttu-id="1f4aa-136">UpdateStateValue</span><span class="sxs-lookup"><span data-stu-id="1f4aa-136">UpdateStateValue</span></span></br><span data-ttu-id="1f4aa-137">Inserts a new option into the option set used in the `Status` attribute.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-137">Inserts a new option into the option set used in the `Status` attribute.</span></span>|<xref href="Microsoft.Dynamics.CRM.OrderOption?text=UpdateStateValue Action" />|<xref:Microsoft.Xrm.Sdk.Messages.UpdateStateValueRequest>|   

<a name="BKMK_RetrieveAGlobalOptionSet"></a>   
## <a name="retrieve-a-global-option-set"></a><span data-ttu-id="1f4aa-138">Retrieve a global option set</span><span class="sxs-lookup"><span data-stu-id="1f4aa-138">Retrieve a global option set</span></span>  
 <span data-ttu-id="1f4aa-139">The following sample shows how to retrieve a global option set by name using the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveOptionSetRequest> message:</span><span class="sxs-lookup"><span data-stu-id="1f4aa-139">The following sample shows how to retrieve a global option set by name using the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveOptionSetRequest> message:</span></span>  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets6](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets6.cs#workwithglobaloptionsets6)]  
  
<a name="BKMK_CreateGlobalOptionSet"></a>   
## <a name="create-a-global-option-set"></a><span data-ttu-id="1f4aa-140">Tạo bộ tùy chọn chung</span><span class="sxs-lookup"><span data-stu-id="1f4aa-140">Create a global option set</span></span>  
 <span data-ttu-id="1f4aa-141">Use the <xref:Microsoft.Xrm.Sdk.Messages.CreateOptionSetRequest> message to create a new global option set.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-141">Use the <xref:Microsoft.Xrm.Sdk.Messages.CreateOptionSetRequest> message to create a new global option set.</span></span> <span data-ttu-id="1f4aa-142">Set the <xref:Microsoft.Xrm.Sdk.Metadata.OptionSetMetadataBase.IsGlobal> property to `true` to indicate that the option set is global.</span><span class="sxs-lookup"><span data-stu-id="1f4aa-142">Set the <xref:Microsoft.Xrm.Sdk.Metadata.OptionSetMetadataBase.IsGlobal> property to `true` to indicate that the option set is global.</span></span> <span data-ttu-id="1f4aa-143">The following code example creates a global option set called “Example Option Set”:</span><span class="sxs-lookup"><span data-stu-id="1f4aa-143">The following code example creates a global option set called “Example Option Set”:</span></span>  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets2](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets2.cs#workwithglobaloptionsets2)]  
  
<a name="BKMK_CreatePicklistWithGlobalOptionSet"></a>   
## <a name="create-a-picklist-that-uses-a-global-option-set"></a><span data-ttu-id="1f4aa-144">Create a picklist that uses a global option set</span><span class="sxs-lookup"><span data-stu-id="1f4aa-144">Create a picklist that uses a global option set</span></span>  
 <span data-ttu-id="1f4aa-145">The following sample shows how to create a picklist attribute that uses a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest>:</span><span class="sxs-lookup"><span data-stu-id="1f4aa-145">The following sample shows how to create a picklist attribute that uses a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest>:</span></span>  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets3](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets3.cs#workwithglobaloptionsets3)]  
  
<a name="BKMK_UpdateGlobalOptionSet"></a>   
## <a name="update-a-global-option-set"></a><span data-ttu-id="1f4aa-146">Update a global option set</span><span class="sxs-lookup"><span data-stu-id="1f4aa-146">Update a global option set</span></span>  
 <span data-ttu-id="1f4aa-147">The following sample shows how to update the label for a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.UpdateOptionSetRequest>:</span><span class="sxs-lookup"><span data-stu-id="1f4aa-147">The following sample shows how to update the label for a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.UpdateOptionSetRequest>:</span></span>  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets4](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets4.cs#workwithglobaloptionsets4)]  
  
<a name="BKMK_OrderingOptions"></a>   
## <a name="ordering-options"></a><span data-ttu-id="1f4aa-148">Ordering options</span><span class="sxs-lookup"><span data-stu-id="1f4aa-148">Ordering options</span></span>  
 <span data-ttu-id="1f4aa-149">The following sample shows how the options in a global option set can be ordered by using <xref:Microsoft.Xrm.Sdk.Messages.OrderOptionRequest>:</span><span class="sxs-lookup"><span data-stu-id="1f4aa-149">The following sample shows how the options in a global option set can be ordered by using <xref:Microsoft.Xrm.Sdk.Messages.OrderOptionRequest>:</span></span>  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets8](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets8.cs#workwithglobaloptionsets8)]  
  
<a name="BKMK_RetrieveAllGlobalOptionSets"></a>   
## <a name="retrieve-all-global-option-sets"></a><span data-ttu-id="1f4aa-150">Retrieve all global option sets</span><span class="sxs-lookup"><span data-stu-id="1f4aa-150">Retrieve all global option sets</span></span>  
 <span data-ttu-id="1f4aa-151">The following sample shows how to retrieve all global option sets by using <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllOptionSetsRequest>:</span><span class="sxs-lookup"><span data-stu-id="1f4aa-151">The following sample shows how to retrieve all global option sets by using <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllOptionSetsRequest>:</span></span>  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets9](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets9.cs#workwithglobaloptionsets9)]  
  
<a name="BKMK_DeleteAGlobalOptionSet"></a>   
## <a name="delete-a-global-option-set"></a><span data-ttu-id="1f4aa-152">Xóa bộ tùy chọn chung</span><span class="sxs-lookup"><span data-stu-id="1f4aa-152">Delete a global option set</span></span>

 <span data-ttu-id="1f4aa-153">The following sample shows how to check whether a global option set is being used by another solution component by using `RetrieveDependentComponents` message (<xref href="Microsoft.Dynamics.CRM.RetrieveDependentComponents?text=RetrieveDependentComponents Function" /> or <xref:Microsoft.Crm.Sdk.Messages.RetrieveDependentComponentsRequest>), and then how to delete it by using `DeleteOptionSet` message (For Organization Service, use <xref:Microsoft.Xrm.Sdk.Messages.DeleteOptionSetRequest>):</span><span class="sxs-lookup"><span data-stu-id="1f4aa-153">The following sample shows how to check whether a global option set is being used by another solution component by using `RetrieveDependentComponents` message (<xref href="Microsoft.Dynamics.CRM.RetrieveDependentComponents?text=RetrieveDependentComponents Function" /> or <xref:Microsoft.Crm.Sdk.Messages.RetrieveDependentComponentsRequest>), and then how to delete it by using `DeleteOptionSet` message (For Organization Service, use <xref:Microsoft.Xrm.Sdk.Messages.DeleteOptionSetRequest>):</span></span>  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets12](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets12.cs#workwithglobaloptionsets12)]  
  
### <a name="see-also"></a><span data-ttu-id="1f4aa-154">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1f4aa-154">See also</span></span>  
 <span data-ttu-id="1f4aa-155">[Customize Dynamics 365 for Customer Engagement applications](../customize-dev/customize-applications.md) </span><span class="sxs-lookup"><span data-stu-id="1f4aa-155">[Customize Dynamics 365 for Customer Engagement applications](../customize-dev/customize-applications.md) </span></span>  
 <span data-ttu-id="1f4aa-156">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="1f4aa-156">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span></span>  
 <span data-ttu-id="1f4aa-157">[Insert, update, delete, and order global option set options](insert-update-delete-order-global-option-set-options.md) </span><span class="sxs-lookup"><span data-stu-id="1f4aa-157">[Insert, update, delete, and order global option set options](insert-update-delete-order-global-option-set-options.md) </span></span>  
 <span data-ttu-id="1f4aa-158">[Sample: Create Global Option Set](sample-create-global-option-set.md) </span><span class="sxs-lookup"><span data-stu-id="1f4aa-158">[Sample: Create Global Option Set](sample-create-global-option-set.md) </span></span>  
 <span data-ttu-id="1f4aa-159">[Sample: Work with Global Option Sets](sample-work-global-option-sets.md) </span><span class="sxs-lookup"><span data-stu-id="1f4aa-159">[Sample: Work with Global Option Sets](sample-work-global-option-sets.md) </span></span>  
 [<span data-ttu-id="1f4aa-160">Sample: Dump Global Option Set Information to a File</span><span class="sxs-lookup"><span data-stu-id="1f4aa-160">Sample: Dump Global Option Set Information to a File</span></span>](sample-dump-global-option-set-information-file.md)
