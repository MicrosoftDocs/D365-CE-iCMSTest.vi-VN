---
title: Customize entity views (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about customizing the entity views.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: a6b5d363-4186-4bc8-a7eb-62f308fa9ef9
caps.latest.revision: 40
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9d3d738a9518ebad19f8169b91605a4c2a4e9985
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388011"
---
# <a name="customize-entity-views"></a><span data-ttu-id="cab3f-103">Customize entity views</span><span class="sxs-lookup"><span data-stu-id="cab3f-103">Customize entity views</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="cab3f-104">Entity views are special saved queries that retrieve data by using a specific filter.</span><span class="sxs-lookup"><span data-stu-id="cab3f-104">Entity views are special saved queries that retrieve data by using a specific filter.</span></span> <span data-ttu-id="cab3f-105">They also contain information about how the data in the view should be displayed in the application.</span><span class="sxs-lookup"><span data-stu-id="cab3f-105">They also contain information about how the data in the view should be displayed in the application.</span></span> <span data-ttu-id="cab3f-106">Entity views are `SavedQuery` records that you can create programmatically.</span><span class="sxs-lookup"><span data-stu-id="cab3f-106">Entity views are `SavedQuery` records that you can create programmatically.</span></span> <span data-ttu-id="cab3f-107">You can also define them as XML, and import them into [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement with an unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="cab3f-107">You can also define them as XML, and import them into [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement with an unmanaged solution.</span></span>  
  
 <span data-ttu-id="cab3f-108">An Entity view is different from a `UserQuery`.</span><span class="sxs-lookup"><span data-stu-id="cab3f-108">An Entity view is different from a `UserQuery`.</span></span> <span data-ttu-id="cab3f-109">A user query, called a Saved view in the application, is owned by an individual user, can be assigned and shared with other users, and can be viewed by other users depending on the query's access privileges.</span><span class="sxs-lookup"><span data-stu-id="cab3f-109">A user query, called a Saved view in the application, is owned by an individual user, can be assigned and shared with other users, and can be viewed by other users depending on the query's access privileges.</span></span> <span data-ttu-id="cab3f-110">This is appropriate for frequently used queries that span entity types and queries that perform aggregation.</span><span class="sxs-lookup"><span data-stu-id="cab3f-110">This is appropriate for frequently used queries that span entity types and queries that perform aggregation.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="cab3f-111">[UserQuery (Saved View) Entity](../userquery-saved-view-entity.md)</span><span class="sxs-lookup"><span data-stu-id="cab3f-111">[UserQuery (Saved View) Entity](../userquery-saved-view-entity.md)</span></span>  
  
 <span data-ttu-id="cab3f-112">You can also use the customization tool in [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] to customize views.</span><span class="sxs-lookup"><span data-stu-id="cab3f-112">You can also use the customization tool in [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] to customize views.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="cab3f-113">[Create and edit views](../../customize/create-edit-views.md)</span><span class="sxs-lookup"><span data-stu-id="cab3f-113">[Create and edit views](../../customize/create-edit-views.md)</span></span>  
  
<a name="BKMK_TypesOfViews"></a>   
## <a name="types-of-views"></a><span data-ttu-id="cab3f-114">Nhập chế độ xem</span><span class="sxs-lookup"><span data-stu-id="cab3f-114">Types of views</span></span>  
 <span data-ttu-id="cab3f-115">The following table lists the five types of views that are supported for customization.</span><span class="sxs-lookup"><span data-stu-id="cab3f-115">The following table lists the five types of views that are supported for customization.</span></span> <span data-ttu-id="cab3f-116">The type code of a view is stored in the `SavedQuery.QueryType` attribute.</span><span class="sxs-lookup"><span data-stu-id="cab3f-116">The type code of a view is stored in the `SavedQuery.QueryType` attribute.</span></span> <span data-ttu-id="cab3f-117">Note that there are other valid values for the `QueryType` attribute not listed here because this entity is also used to store [!INCLUDE[pn_MS_Outlook_Full](../../includes/pn-ms-outlook-full.md)] filters and templates.</span><span class="sxs-lookup"><span data-stu-id="cab3f-117">Note that there are other valid values for the `QueryType` attribute not listed here because this entity is also used to store [!INCLUDE[pn_MS_Outlook_Full](../../includes/pn-ms-outlook-full.md)] filters and templates.</span></span> <span data-ttu-id="cab3f-118">For more information, see [Offline and Outlook Filters and Templates](../outlook-client/offline-outlook-filters-templates.md).</span><span class="sxs-lookup"><span data-stu-id="cab3f-118">For more information, see [Offline and Outlook Filters and Templates](../outlook-client/offline-outlook-filters-templates.md).</span></span>  
  
 <span data-ttu-id="cab3f-119">When views are defined for a specific entity, the `SavedQuery.ReturnedTypeCode` attribute returns the entity logical name.</span><span class="sxs-lookup"><span data-stu-id="cab3f-119">When views are defined for a specific entity, the `SavedQuery.ReturnedTypeCode` attribute returns the entity logical name.</span></span>  
  
|<span data-ttu-id="cab3f-120">View Type</span><span class="sxs-lookup"><span data-stu-id="cab3f-120">View Type</span></span>|<span data-ttu-id="cab3f-121">Type Code</span><span class="sxs-lookup"><span data-stu-id="cab3f-121">Type Code</span></span>|<span data-ttu-id="cab3f-122">Mô tả</span><span class="sxs-lookup"><span data-stu-id="cab3f-122">Description</span></span>|  
|---------------|---------------|-----------------|  
|<span data-ttu-id="cab3f-123">**Công khai**</span><span class="sxs-lookup"><span data-stu-id="cab3f-123">**Public**</span></span>|<span data-ttu-id="cab3f-124">0</span><span class="sxs-lookup"><span data-stu-id="cab3f-124">0</span></span>|<span data-ttu-id="cab3f-125">- **Occurrence**: Many</span><span class="sxs-lookup"><span data-stu-id="cab3f-125">- **Occurrence**: Many</span></span><br /><span data-ttu-id="cab3f-126">- **Actions**: Create, Update, Delete</span><span class="sxs-lookup"><span data-stu-id="cab3f-126">- **Actions**: Create, Update, Delete</span></span><br /><span data-ttu-id="cab3f-127">- **Comments**: You can set one of these views as the default public view by setting `SavedQuery.IsDefault` to true.</span><span class="sxs-lookup"><span data-stu-id="cab3f-127">- **Comments**: You can set one of these views as the default public view by setting `SavedQuery.IsDefault` to true.</span></span>|  
|<span data-ttu-id="cab3f-128">**Tìm kiếm Nâng cao**</span><span class="sxs-lookup"><span data-stu-id="cab3f-128">**Advanced Find**</span></span>|<span data-ttu-id="cab3f-129">1</span><span class="sxs-lookup"><span data-stu-id="cab3f-129">1</span></span>|<span data-ttu-id="cab3f-130">- **Occurrence**: 1</span><span class="sxs-lookup"><span data-stu-id="cab3f-130">- **Occurrence**: 1</span></span><br /><span data-ttu-id="cab3f-131">- **Actions**: Update only.</span><span class="sxs-lookup"><span data-stu-id="cab3f-131">- **Actions**: Update only.</span></span><br /><span data-ttu-id="cab3f-132">- **Comments**: By default, this view is displayed when results are shown in **Advanced Find**.</span><span class="sxs-lookup"><span data-stu-id="cab3f-132">- **Comments**: By default, this view is displayed when results are shown in **Advanced Find**.</span></span>|  
|<span data-ttu-id="cab3f-133">**Đã liên kết**</span><span class="sxs-lookup"><span data-stu-id="cab3f-133">**Associated**</span></span>|<span data-ttu-id="cab3f-134">2</span><span class="sxs-lookup"><span data-stu-id="cab3f-134">2</span></span>|<span data-ttu-id="cab3f-135">- **Occurrence**: 1</span><span class="sxs-lookup"><span data-stu-id="cab3f-135">- **Occurrence**: 1</span></span><br /><span data-ttu-id="cab3f-136">- **Actions**: Update only,</span><span class="sxs-lookup"><span data-stu-id="cab3f-136">- **Actions**: Update only,</span></span><br /><span data-ttu-id="cab3f-137">- **Comments**: By default, this view is displayed when a grid of related records appears in the navigation pane of a record.</span><span class="sxs-lookup"><span data-stu-id="cab3f-137">- **Comments**: By default, this view is displayed when a grid of related records appears in the navigation pane of a record.</span></span>|  
|<span data-ttu-id="cab3f-138">**Tìm nhanh**</span><span class="sxs-lookup"><span data-stu-id="cab3f-138">**Quick Find**</span></span>|<span data-ttu-id="cab3f-139">4</span><span class="sxs-lookup"><span data-stu-id="cab3f-139">4</span></span>|<span data-ttu-id="cab3f-140">- **Occurrence**: 1</span><span class="sxs-lookup"><span data-stu-id="cab3f-140">- **Occurrence**: 1</span></span><br /><span data-ttu-id="cab3f-141">- **Actions**: Update only.</span><span class="sxs-lookup"><span data-stu-id="cab3f-141">- **Actions**: Update only.</span></span><br /><span data-ttu-id="cab3f-142">- **Comments**: This view defines the columns that will be searched when a user searches for records by using the search field in a list view.</span><span class="sxs-lookup"><span data-stu-id="cab3f-142">- **Comments**: This view defines the columns that will be searched when a user searches for records by using the search field in a list view.</span></span>|  
|<span data-ttu-id="cab3f-143">**Tra cứu**</span><span class="sxs-lookup"><span data-stu-id="cab3f-143">**Lookup**</span></span>|<span data-ttu-id="cab3f-144">64</span><span class="sxs-lookup"><span data-stu-id="cab3f-144">64</span></span>|<span data-ttu-id="cab3f-145">- **Occurrence**: 1</span><span class="sxs-lookup"><span data-stu-id="cab3f-145">- **Occurrence**: 1</span></span><br /><span data-ttu-id="cab3f-146">- **Actions**: Update only.</span><span class="sxs-lookup"><span data-stu-id="cab3f-146">- **Actions**: Update only.</span></span><br /><span data-ttu-id="cab3f-147">- **Comments**: This is the default view that will be used to look up a record when no other view has been configured for the lookup field.</span><span class="sxs-lookup"><span data-stu-id="cab3f-147">- **Comments**: This is the default view that will be used to look up a record when no other view has been configured for the lookup field.</span></span>|  
  
<a name="BKMK_ViewTasks"></a>   
## <a name="view-tasks"></a><span data-ttu-id="cab3f-148">View tasks</span><span class="sxs-lookup"><span data-stu-id="cab3f-148">View tasks</span></span>  
 <span data-ttu-id="cab3f-149">Because views are SavedQuery records, you can create, update, retrieve, delete and deactivate them.</span><span class="sxs-lookup"><span data-stu-id="cab3f-149">Because views are SavedQuery records, you can create, update, retrieve, delete and deactivate them.</span></span> <span data-ttu-id="cab3f-150">In addition you can edit filter criteria or configure sorting, edit columns or set a view as a default view.</span><span class="sxs-lookup"><span data-stu-id="cab3f-150">In addition you can edit filter criteria or configure sorting, edit columns or set a view as a default view.</span></span>  
  
<a name="BKMK_CreateViews"></a>   
### <a name="create-views"></a><span data-ttu-id="cab3f-151">Create views</span><span class="sxs-lookup"><span data-stu-id="cab3f-151">Create views</span></span>  
 <span data-ttu-id="cab3f-152">To create a public view, specify the following properties:</span><span class="sxs-lookup"><span data-stu-id="cab3f-152">To create a public view, specify the following properties:</span></span>  
  
- <span data-ttu-id="cab3f-153">`SavedQuery.Name`: A unique identifier for the saved query.</span><span class="sxs-lookup"><span data-stu-id="cab3f-153">`SavedQuery.Name`: A unique identifier for the saved query.</span></span>  
  
- <span data-ttu-id="cab3f-154">`SavedQuery.ReturnedTypeCode`: Matches the logical name of the entity.</span><span class="sxs-lookup"><span data-stu-id="cab3f-154">`SavedQuery.ReturnedTypeCode`: Matches the logical name of the entity.</span></span>  
  
- <span data-ttu-id="cab3f-155">`SavedQuery.FetchXml`: See [Use FetchXML to Construct a Query](../org-service/use-fetchxml-construct-query.md).</span><span class="sxs-lookup"><span data-stu-id="cab3f-155">`SavedQuery.FetchXml`: See [Use FetchXML to Construct a Query](../org-service/use-fetchxml-construct-query.md).</span></span>  
  
- <span data-ttu-id="cab3f-156">`SavedQuery.LayoutXml`: See the `layoutxml` element in the [Customization solutions file schema](customization-solutions-file-schema.md)  for the valid elements.</span><span class="sxs-lookup"><span data-stu-id="cab3f-156">`SavedQuery.LayoutXml`: See the `layoutxml` element in the [Customization solutions file schema](customization-solutions-file-schema.md)  for the valid elements.</span></span>  
  
- <span data-ttu-id="cab3f-157">`SavedQuery.QueryType`: Must always be zero (0).</span><span class="sxs-lookup"><span data-stu-id="cab3f-157">`SavedQuery.QueryType`: Must always be zero (0).</span></span>  
  
  <span data-ttu-id="cab3f-158">The following sample creates a new public view for the opportunity entity:</span><span class="sxs-lookup"><span data-stu-id="cab3f-158">The following sample creates a new public view for the opportunity entity:</span></span>  
  
  [!code-csharp[WorkWithViews#WorkWithViews1](../../snippets/csharp/CRMV8/workwithviews/cs/workwithviews1.cs#workwithviews1)]  
  
<a name="BKMK_UpdateViews"></a>   
### <a name="update-views"></a><span data-ttu-id="cab3f-159">Update views</span><span class="sxs-lookup"><span data-stu-id="cab3f-159">Update views</span></span>  
 <span data-ttu-id="cab3f-160">If the `SavedQuery.IsCustomizable` managed property allows the view to be updated, you can use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span><span class="sxs-lookup"><span data-stu-id="cab3f-160">If the `SavedQuery.IsCustomizable` managed property allows the view to be updated, you can use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span></span> <span data-ttu-id="cab3f-161">method or the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message to update the view.</span><span class="sxs-lookup"><span data-stu-id="cab3f-161">method or the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message to update the view.</span></span>  
  
<a name="BKMK_DeleteViews"></a>   
### <a name="delete-views"></a><span data-ttu-id="cab3f-162">Delete views</span><span class="sxs-lookup"><span data-stu-id="cab3f-162">Delete views</span></span>  
 <span data-ttu-id="cab3f-163">You should only delete saved queries that you have created.</span><span class="sxs-lookup"><span data-stu-id="cab3f-163">You should only delete saved queries that you have created.</span></span> <span data-ttu-id="cab3f-164">A solution component or part of the application may depend on a specific saved query.</span><span class="sxs-lookup"><span data-stu-id="cab3f-164">A solution component or part of the application may depend on a specific saved query.</span></span> <span data-ttu-id="cab3f-165">If there are queries you do not want to appear in the application, you should deactivate them.</span><span class="sxs-lookup"><span data-stu-id="cab3f-165">If there are queries you do not want to appear in the application, you should deactivate them.</span></span>  
  
<a name="BKMK_RetrieveViews"></a>   
### <a name="retrieve-views"></a><span data-ttu-id="cab3f-166">Retrieve views</span><span class="sxs-lookup"><span data-stu-id="cab3f-166">Retrieve views</span></span>  
 <span data-ttu-id="cab3f-167">Use a <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest> or <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span><span class="sxs-lookup"><span data-stu-id="cab3f-167">Use a <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest> or <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span></span> <span data-ttu-id="cab3f-168">to retrieve saved query records.</span><span class="sxs-lookup"><span data-stu-id="cab3f-168">to retrieve saved query records.</span></span>  
  
 <span data-ttu-id="cab3f-169">The following sample retrieves all the public views for the opportunity entity:</span><span class="sxs-lookup"><span data-stu-id="cab3f-169">The following sample retrieves all the public views for the opportunity entity:</span></span>  
  
 [!code-csharp[WorkWithViews#WorkWithViews2](../../snippets/csharp/CRMV8/workwithviews/cs/workwithviews2.cs#workwithviews2)]  
  
<a name="BKMK_DeactivateViews"></a>   
### <a name="deactivate-views"></a><span data-ttu-id="cab3f-170">Deactivate views</span><span class="sxs-lookup"><span data-stu-id="cab3f-170">Deactivate views</span></span>  
 <span data-ttu-id="cab3f-171">If you do not want a public view to appear in the application, you can deactivate it.</span><span class="sxs-lookup"><span data-stu-id="cab3f-171">If you do not want a public view to appear in the application, you can deactivate it.</span></span> <span data-ttu-id="cab3f-172">You cannot deactivate a public view that is set as the default view.</span><span class="sxs-lookup"><span data-stu-id="cab3f-172">You cannot deactivate a public view that is set as the default view.</span></span> <span data-ttu-id="cab3f-173">The following sample deactivates the **Closed Opportunities in Current Fiscal Year** view for the Opportunity entity:</span><span class="sxs-lookup"><span data-stu-id="cab3f-173">The following sample deactivates the **Closed Opportunities in Current Fiscal Year** view for the Opportunity entity:</span></span>  
  
 [!code-csharp[WorkWithViews#WorkWithViews3](../../snippets/csharp/CRMV8/workwithviews/cs/workwithviews3.cs#workwithviews3)]  
  
<a name="BKMK_EditFilterOrSorting"></a>   
### <a name="edit-filter-criteria-or-configure-sorting"></a><span data-ttu-id="cab3f-174">Edit filter criteria or configure sorting</span><span class="sxs-lookup"><span data-stu-id="cab3f-174">Edit filter criteria or configure sorting</span></span>  
 <span data-ttu-id="cab3f-175">To edit the filter or edit how the data is sorted, you must set the `SavedQuery.FetchXml` attribute.</span><span class="sxs-lookup"><span data-stu-id="cab3f-175">To edit the filter or edit how the data is sorted, you must set the `SavedQuery.FetchXml` attribute.</span></span> <span data-ttu-id="cab3f-176">For more information, see [Building Queries with FetchXML](../org-service/build-queries-fetchxml.md).</span><span class="sxs-lookup"><span data-stu-id="cab3f-176">For more information, see [Building Queries with FetchXML](../org-service/build-queries-fetchxml.md).</span></span>  
  
> [!TIP]
>  <span data-ttu-id="cab3f-177">If you are not familiar with FetchXML the following messages can be used to convert between QueryExpression and FetchXML:<xref:Microsoft.Crm.Sdk.Messages.QueryExpressionToFetchXmlRequest> and <xref:Microsoft.Crm.Sdk.Messages.FetchXmlToQueryExpressionRequest>.</span><span class="sxs-lookup"><span data-stu-id="cab3f-177">If you are not familiar with FetchXML the following messages can be used to convert between QueryExpression and FetchXML:<xref:Microsoft.Crm.Sdk.Messages.QueryExpressionToFetchXmlRequest> and <xref:Microsoft.Crm.Sdk.Messages.FetchXmlToQueryExpressionRequest>.</span></span>  
  
<a name="BKMK_EditColumns"></a>   
### <a name="edit-columns"></a><span data-ttu-id="cab3f-178">Edit columns</span><span class="sxs-lookup"><span data-stu-id="cab3f-178">Edit columns</span></span>  
 <span data-ttu-id="cab3f-179">The columns that you want to display in views can be taken from the entity or related entities.</span><span class="sxs-lookup"><span data-stu-id="cab3f-179">The columns that you want to display in views can be taken from the entity or related entities.</span></span> <span data-ttu-id="cab3f-180">For more information about how to specify the columns to display, see the `layoutxml` element in the [Customization solutions file schema](customization-solutions-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="cab3f-180">For more information about how to specify the columns to display, see the `layoutxml` element in the [Customization solutions file schema](customization-solutions-file-schema.md).</span></span>  
  
<a name="BKMK_CustomIcons"></a>   
### <a name="add-custom-icons-with-tooltip-for-a-column"></a><span data-ttu-id="cab3f-181">Add custom icons with tooltip for a column</span><span class="sxs-lookup"><span data-stu-id="cab3f-181">Add custom icons with tooltip for a column</span></span>  
 <span data-ttu-id="cab3f-182">You can add custom icon with tooltip text to display in a column depending on the column value; you can also specify localized tooltip text.</span><span class="sxs-lookup"><span data-stu-id="cab3f-182">You can add custom icon with tooltip text to display in a column depending on the column value; you can also specify localized tooltip text.</span></span> <span data-ttu-id="cab3f-183">This can be done by adding the custom icons as image web resources in your [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] instance and then using a [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] web resource to add [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] code for a column to display the icons depending on the column value.</span><span class="sxs-lookup"><span data-stu-id="cab3f-183">This can be done by adding the custom icons as image web resources in your [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] instance and then using a [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] web resource to add [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] code for a column to display the icons depending on the column value.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cab3f-184">This feature was introduced in the [!INCLUDE[pn_crm_8_2_0_both](../../includes/pn-crm-8-2-0-both.md)].</span><span class="sxs-lookup"><span data-stu-id="cab3f-184">This feature was introduced in the [!INCLUDE[pn_crm_8_2_0_both](../../includes/pn-crm-8-2-0-both.md)].</span></span> <span data-ttu-id="cab3f-185">Adding custom icons with tooltip is supported only for the read-only grids; this feature isn't supported for the editable grids.</span><span class="sxs-lookup"><span data-stu-id="cab3f-185">Adding custom icons with tooltip is supported only for the read-only grids; this feature isn't supported for the editable grids.</span></span> <span data-ttu-id="cab3f-186">For more information about editable grids, see [Use editable grids](use-editable-grids-dynamics-365.md).</span><span class="sxs-lookup"><span data-stu-id="cab3f-186">For more information about editable grids, see [Use editable grids](use-editable-grids-dynamics-365.md).</span></span>  
  
 <span data-ttu-id="cab3f-187">Two new attributes, `imageproviderwebresource` and `imageproviderfunctionname`,  are added to the `cell` element of the layoutxml of savedquery that lets you specify the name of a web resource and a [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] function name to display custom icons and tooltip text for a column.</span><span class="sxs-lookup"><span data-stu-id="cab3f-187">Two new attributes, `imageproviderwebresource` and `imageproviderfunctionname`,  are added to the `cell` element of the layoutxml of savedquery that lets you specify the name of a web resource and a [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] function name to display custom icons and tooltip text for a column.</span></span> <span data-ttu-id="cab3f-188">The [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] code gets executed when the page loads.</span><span class="sxs-lookup"><span data-stu-id="cab3f-188">The [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] code gets executed when the page loads.</span></span>  
  
 <span data-ttu-id="cab3f-189">You can also use the new **Web Resource** and **Function Name** fields in the **Column Properties** page while modifying the property of an attribute (column) in a view definition in the [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] web client to specify the web resource name and [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] function name.</span><span class="sxs-lookup"><span data-stu-id="cab3f-189">You can also use the new **Web Resource** and **Function Name** fields in the **Column Properties** page while modifying the property of an attribute (column) in a view definition in the [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] web client to specify the web resource name and [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] function name.</span></span>  
  
 <span data-ttu-id="cab3f-190">The following sample code demonstrates how you can programmatically specify a web resource and a [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] function name for adding custom icons and tooltip for the `opportunityratingcode` column in layoutxml:</span><span class="sxs-lookup"><span data-stu-id="cab3f-190">The following sample code demonstrates how you can programmatically specify a web resource and a [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] function name for adding custom icons and tooltip for the `opportunityratingcode` column in layoutxml:</span></span>  
  
```csharp  
System.String layoutXml =  
@"<grid name='resultset' object='3' jump='name' select='1'  
  preview='1' icon='1'>  
  <row name='result' id='opportunityid'>  
    <cell name='name' width='150' />  
    <cell name='customerid' width='150' />  
    <cell name='estimatedclosedate' width='150' />  
    <cell name='estimatedvalue' width='150' />  
    <cell name='closeprobability' width='150' />  
    <cell name='opportunityratingcode' width='150' imageproviderwebresource='new_SampleWebResource'  
          imageproviderfunctionname='displayIconTooltip' />  
    <cell name='opportunitycustomeridcontactcontactid.emailaddress1'  
        width='150' disableSorting='1' />  
  </row>  
</grid>";  
```  
  
 <span data-ttu-id="cab3f-191">The [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] function for displaying custom icons and tooltip text expects the following two arguments: the entire row object specified in layoutxml and the calling user’s Locale ID (LCID).</span><span class="sxs-lookup"><span data-stu-id="cab3f-191">The [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] function for displaying custom icons and tooltip text expects the following two arguments: the entire row object specified in layoutxml and the calling user’s Locale ID (LCID).</span></span> <span data-ttu-id="cab3f-192">The LCID parameter enables you to specify tooltip text for the icon in multiple languages.</span><span class="sxs-lookup"><span data-stu-id="cab3f-192">The LCID parameter enables you to specify tooltip text for the icon in multiple languages.</span></span> <span data-ttu-id="cab3f-193">For more information about the languages supported by CRM, see [Enable additional languages](../../customize/enable-additional-languages.md) and [Install or upgrade Language Packs for Microsoft Dynamics 365 for Customer Engagement](https://technet.microsoft.com/library/hh699674.aspx).</span><span class="sxs-lookup"><span data-stu-id="cab3f-193">For more information about the languages supported by CRM, see [Enable additional languages](../../customize/enable-additional-languages.md) and [Install or upgrade Language Packs for Microsoft Dynamics 365 for Customer Engagement](https://technet.microsoft.com/library/hh699674.aspx).</span></span> <span data-ttu-id="cab3f-194">For a list of locale ID (LCID) values that you can use in your code, see [Locale IDs Assigned by Microsoft](https://go.microsoft.com/fwlink/?linkid=829588).</span><span class="sxs-lookup"><span data-stu-id="cab3f-194">For a list of locale ID (LCID) values that you can use in your code, see [Locale IDs Assigned by Microsoft](https://go.microsoft.com/fwlink/?linkid=829588).</span></span>  
  
 <span data-ttu-id="cab3f-195">Assuming you will most likely be adding custom icons for an option set type of attribute as it has a limited set of predefined options, make sure you use the integer value of the options instead of label to avoid breaking the code due to changes in the localized label string.</span><span class="sxs-lookup"><span data-stu-id="cab3f-195">Assuming you will most likely be adding custom icons for an option set type of attribute as it has a limited set of predefined options, make sure you use the integer value of the options instead of label to avoid breaking the code due to changes in the localized label string.</span></span> <span data-ttu-id="cab3f-196">Also, in your JavaScript function, specify just the name of an image web resource that you want to use as an icon for a value in the attribute.</span><span class="sxs-lookup"><span data-stu-id="cab3f-196">Also, in your JavaScript function, specify just the name of an image web resource that you want to use as an icon for a value in the attribute.</span></span> <span data-ttu-id="cab3f-197">The image should be of 16x16 pixels size; larger images will be automatically scaled down to 16x16 pixels size.</span><span class="sxs-lookup"><span data-stu-id="cab3f-197">The image should be of 16x16 pixels size; larger images will be automatically scaled down to 16x16 pixels size.</span></span>  
  
 <span data-ttu-id="cab3f-198">The following sample code displays different icons and tooltip text based on one of the values (1: Hot, 2: Warm, 3: Cold) in the `opportunityratingcode (Rating)` attribute.</span><span class="sxs-lookup"><span data-stu-id="cab3f-198">The following sample code displays different icons and tooltip text based on one of the values (1: Hot, 2: Warm, 3: Cold) in the `opportunityratingcode (Rating)` attribute.</span></span> <span data-ttu-id="cab3f-199">Mã ví dụ cũng cho thấy cách hiển thị văn bản công cụ chú giải được bản địa hóa.</span><span class="sxs-lookup"><span data-stu-id="cab3f-199">The sample code also shows how to display localized tooltip text.</span></span> <span data-ttu-id="cab3f-200">For this sample to work, you must create three image web resources each with 16x16 images (![Hot rating button](../media/dynamics365hotgridicon.png "Hot rating button"), ![Warm rating symbol](../media/dynamics365warmgridicon.png "Warm rating symbol"), and ![Cold rating button](../media/dynamics365coldgridicon.png "Cold rating button")) in your [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] instance with the following names respectively: `new_Hot`, `new_Warm`, and `new_Cold`.</span><span class="sxs-lookup"><span data-stu-id="cab3f-200">For this sample to work, you must create three image web resources each with 16x16 images (![Hot rating button](../media/dynamics365hotgridicon.png "Hot rating button"), ![Warm rating symbol](../media/dynamics365warmgridicon.png "Warm rating symbol"), and ![Cold rating button](../media/dynamics365coldgridicon.png "Cold rating button")) in your [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] instance with the following names respectively: `new_Hot`, `new_Warm`, and `new_Cold`.</span></span>  
  
```javascript 
function displayIconTooltip(rowData, userLCID) {      
    var str = JSON.parse(rowData);  
    var coldata = str.opportunityratingcode_Value;  
    var imgName = "";  
    var tooltip = "";  
    switch (coldata) {  
        case 1:  
            imgName = "new_Hot";  
            switch (userLCID) {  
                case 1036:  
                    tooltip = "French: Opportunity is Hot";  
                    break;  
                default:  
                    tooltip = "Opportunity is Hot";  
                    break;  
            }  
            break;  
        case 2:  
            imgName = "new_Warm";  
            switch (userLCID) {  
                case 1036:  
                    tooltip = "French: Opportunity is Warm";  
                    break;  
                default:  
                    tooltip = "Opportunity is Warm";  
                    break;  
            }  
            break;  
        case 3:  
            imgName = "new_Cold";  
            switch (userLCID) {  
                case 1036:  
                    tooltip = "French: Opportunity is Cold";  
                    break;  
                default:  
                    tooltip = "Opportunity is Cold";  
                    break;  
            }  
            break;  
        default:  
            imgName = "";  
            tooltip = "";  
            break;  
    }  
    var resultarray = [imgName, tooltip];  
    return resultarray;  
}  
```  
  
 <span data-ttu-id="cab3f-201">This results in displaying the values in the `Rating` column with appropriate icons depending on the value, and icon tooltip text when you hover over the icons.</span><span class="sxs-lookup"><span data-stu-id="cab3f-201">This results in displaying the values in the `Rating` column with appropriate icons depending on the value, and icon tooltip text when you hover over the icons.</span></span>  
  
 <span data-ttu-id="cab3f-202">![Custom icons displayed for a column in a view](../media/customiconsinviews.png "Custom icons displayed for a column in a view")</span><span class="sxs-lookup"><span data-stu-id="cab3f-202">![Custom icons displayed for a column in a view](../media/customiconsinviews.png "Custom icons displayed for a column in a view")</span></span>  
  
<a name="BKMK_SetAsDefault"></a>   
### <a name="set-as-default"></a><span data-ttu-id="cab3f-203">Đặt làm mặc định</span><span class="sxs-lookup"><span data-stu-id="cab3f-203">Set as default</span></span>  
 <span data-ttu-id="cab3f-204">Only one active public view can be set as the default view.</span><span class="sxs-lookup"><span data-stu-id="cab3f-204">Only one active public view can be set as the default view.</span></span> <span data-ttu-id="cab3f-205">To make a view the default view, set the `IsDefault` property to true.</span><span class="sxs-lookup"><span data-stu-id="cab3f-205">To make a view the default view, set the `IsDefault` property to true.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="cab3f-206">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="cab3f-206">See also</span></span>  
 <span data-ttu-id="cab3f-207">[Sample: Work with Views](sample-work-views.md) </span><span class="sxs-lookup"><span data-stu-id="cab3f-207">[Sample: Work with Views](sample-work-views.md) </span></span>  
 <span data-ttu-id="cab3f-208">[Building Queries with FetchXML](../org-service/build-queries-fetchxml.md) </span><span class="sxs-lookup"><span data-stu-id="cab3f-208">[Building Queries with FetchXML](../org-service/build-queries-fetchxml.md) </span></span>  
 <span data-ttu-id="cab3f-209">[Extend the Metadata Model for Microsoft Dynamics 365 for Customer Engagement](../org-service/use-organization-service-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="cab3f-209">[Extend the Metadata Model for Microsoft Dynamics 365 for Customer Engagement](../org-service/use-organization-service-metadata.md) </span></span>  
 <span data-ttu-id="cab3f-210">[Customize Entity Forms in Microsoft Dynamics 365 for Customer Engagement](customize-entity-forms.md) </span><span class="sxs-lookup"><span data-stu-id="cab3f-210">[Customize Entity Forms in Microsoft Dynamics 365 for Customer Engagement](customize-entity-forms.md) </span></span>  
 <span data-ttu-id="cab3f-211">[Customize Global Option Sets in Microsoft Dynamics 365 for Customer Engagement](../org-service/customize-global-option-sets.md) </span><span class="sxs-lookup"><span data-stu-id="cab3f-211">[Customize Global Option Sets in Microsoft Dynamics 365 for Customer Engagement](../org-service/customize-global-option-sets.md) </span></span>  
 [<span data-ttu-id="cab3f-212">Customize Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="cab3f-212">Customize Dynamics 365 for Customer Engagement</span></span>](customize-applications.md)
