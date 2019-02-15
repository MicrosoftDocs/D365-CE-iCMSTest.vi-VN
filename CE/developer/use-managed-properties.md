---
title: Use managed properties (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: Managed properties help you define which of the managed solution components can be customized
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
- using managed properties, setting the IsCustomizable property
- unmanaged solutions, applying managed properties
- using managed properties, applying managed properties to unmanaged solutions
- checking managed properties for solution components, using managed properties
- managed properties, using in unmanaged solutions
- solution components, list of managed properties for each solution component
- using managed properties, list of managed properties for each solution component
- solution components, using managed properties
- using managed properties, updating managed properties
- using managed properties, checking managed properties for solution components
ms.assetid: 749edaa4-e975-4e6a-925d-6ea77bfa9112
caps.latest.revision: 24
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3576c866ff52c75709366607cf0c45468de55be3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385888"
---
# <a name="use-managed-properties"></a><span data-ttu-id="40474-103">Use managed properties</span><span class="sxs-lookup"><span data-stu-id="40474-103">Use managed properties</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="40474-104">You can control which of your managed solution components are customizable by using managed properties.</span><span class="sxs-lookup"><span data-stu-id="40474-104">You can control which of your managed solution components are customizable by using managed properties.</span></span> <span data-ttu-id="40474-105">You should allow as much customization as possible for those solution components that represent business entities.</span><span class="sxs-lookup"><span data-stu-id="40474-105">You should allow as much customization as possible for those solution components that represent business entities.</span></span> <span data-ttu-id="40474-106">This lets organizations customize your           solution to their requirements.</span><span class="sxs-lookup"><span data-stu-id="40474-106">This lets organizations customize your           solution to their requirements.</span></span> <span data-ttu-id="40474-107">Limit or eliminate customization of critical solution components that provide the core functionality of your solution so that you can predictably support and maintain it.</span><span class="sxs-lookup"><span data-stu-id="40474-107">Limit or eliminate customization of critical solution components that provide the core functionality of your solution so that you can predictably support and maintain it.</span></span>  
  
 <span data-ttu-id="40474-108">Managed properties are intended to protect your solution from modifications that may cause it to break.</span><span class="sxs-lookup"><span data-stu-id="40474-108">Managed properties are intended to protect your solution from modifications that may cause it to break.</span></span> <span data-ttu-id="40474-109">Managed properties do not provide digital rights management (DRM), or capabilities to license your solution or control who may install it.</span><span class="sxs-lookup"><span data-stu-id="40474-109">Managed properties do not provide digital rights management (DRM), or capabilities to license your solution or control who may install it.</span></span>  
  
## <a name="apply-managed-properties"></a><span data-ttu-id="40474-110">Apply managed properties</span><span class="sxs-lookup"><span data-stu-id="40474-110">Apply managed properties</span></span>  
 <span data-ttu-id="40474-111">You apply managed properties when the solution is unmanaged.</span><span class="sxs-lookup"><span data-stu-id="40474-111">You apply managed properties when the solution is unmanaged.</span></span> <span data-ttu-id="40474-112">The managed properties will take effect after you package the managed solution and install it in a different organization.</span><span class="sxs-lookup"><span data-stu-id="40474-112">The managed properties will take effect after you package the managed solution and install it in a different organization.</span></span> <span data-ttu-id="40474-113">After the managed solution is installed, the managed properties cannot be              updated except by an update of the solution by the original publisher.</span><span class="sxs-lookup"><span data-stu-id="40474-113">After the managed solution is installed, the managed properties cannot be              updated except by an update of the solution by the original publisher.</span></span>  
  
 <span data-ttu-id="40474-114">Most solution components have a **Managed Properties**button when viewing a list of solution components.</span><span class="sxs-lookup"><span data-stu-id="40474-114">Most solution components have a **Managed Properties**button when viewing a list of solution components.</span></span> <span data-ttu-id="40474-115">You can view or update the managed properties for a solution component when you click this button.</span><span class="sxs-lookup"><span data-stu-id="40474-115">You can view or update the managed properties for a solution component when you click this button.</span></span> <span data-ttu-id="40474-116">To access managed properties for solutions that do not display this button, select **Managed Properties**from the **More Actions**drop-down list.</span><span class="sxs-lookup"><span data-stu-id="40474-116">To access managed properties for solutions that do not display this button, select **Managed Properties**from the **More Actions**drop-down list.</span></span>  
  
 <span data-ttu-id="40474-117">By default, all custom solution components are customizable.</span><span class="sxs-lookup"><span data-stu-id="40474-117">By default, all custom solution components are customizable.</span></span> <span data-ttu-id="40474-118">To change the managed properties for a solution component, click the **Managed Properties**button in the toolbar for the solution component.</span><span class="sxs-lookup"><span data-stu-id="40474-118">To change the managed properties for a solution component, click the **Managed Properties**button in the toolbar for the solution component.</span></span> <span data-ttu-id="40474-119">Each solution component has a **Can be customized**(                 `IsCustomizable`) property.</span><span class="sxs-lookup"><span data-stu-id="40474-119">Each solution component has a **Can be customized**(                 `IsCustomizable`) property.</span></span> <span data-ttu-id="40474-120">As long as this property is true, more properties specific to the type of solution component can be specified.</span><span class="sxs-lookup"><span data-stu-id="40474-120">As long as this property is true, more properties specific to the type of solution component can be specified.</span></span> <span data-ttu-id="40474-121">If you set the              `IsCustomizable.Value`property to false, after the solution is installed as a managed solution the solution component will not be customizable.</span><span class="sxs-lookup"><span data-stu-id="40474-121">If you set the              `IsCustomizable.Value`property to false, after the solution is installed as a managed solution the solution component will not be customizable.</span></span> <span data-ttu-id="40474-122">The following table lists the managed properties for each solution component.</span><span class="sxs-lookup"><span data-stu-id="40474-122">The following table lists the managed properties for each solution component.</span></span>  
  
|<span data-ttu-id="40474-123">Thành phần</span><span class="sxs-lookup"><span data-stu-id="40474-123">Component</span></span>|<span data-ttu-id="40474-124">Tên Hiển thị</span><span class="sxs-lookup"><span data-stu-id="40474-124">Display Name</span></span>|<span data-ttu-id="40474-125">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="40474-125">Property</span></span>|  
|---------------|------------------|--------------|  
|<span data-ttu-id="40474-126">Thực thể</span><span class="sxs-lookup"><span data-stu-id="40474-126">Entity</span></span>|<span data-ttu-id="40474-127">Có thể tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="40474-127">Can be customized</span></span>|<span data-ttu-id="40474-128"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsCustomizable>.</span><span class="sxs-lookup"><span data-stu-id="40474-128"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsCustomizable>.</span></span>                                 `Value`|  
|<span data-ttu-id="40474-129">Thực thể</span><span class="sxs-lookup"><span data-stu-id="40474-129">Entity</span></span>|<span data-ttu-id="40474-130">Có thể sửa đổi tên hiển thị</span><span class="sxs-lookup"><span data-stu-id="40474-130">Display name can be modified</span></span>|<span data-ttu-id="40474-131"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsRenameable>.</span><span class="sxs-lookup"><span data-stu-id="40474-131"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsRenameable>.</span></span>                              `Value`|  
|<span data-ttu-id="40474-132">Thực thể</span><span class="sxs-lookup"><span data-stu-id="40474-132">Entity</span></span>|<span data-ttu-id="40474-133">Can be related entity in relationship</span><span class="sxs-lookup"><span data-stu-id="40474-133">Can be related entity in relationship</span></span>|<span data-ttu-id="40474-134"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanBeRelatedEntityInRelationship>.</span><span class="sxs-lookup"><span data-stu-id="40474-134"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanBeRelatedEntityInRelationship>.</span></span>                                 <span data-ttu-id="40474-135">`Value`(Read Only)</span><span class="sxs-lookup"><span data-stu-id="40474-135">`Value`(Read Only)</span></span>|  
|<span data-ttu-id="40474-136">Thực thể</span><span class="sxs-lookup"><span data-stu-id="40474-136">Entity</span></span>|<span data-ttu-id="40474-137">Can be primary entity in relationship</span><span class="sxs-lookup"><span data-stu-id="40474-137">Can be primary entity in relationship</span></span>|<span data-ttu-id="40474-138"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanBePrimaryEntityInRelationship>.</span><span class="sxs-lookup"><span data-stu-id="40474-138"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanBePrimaryEntityInRelationship>.</span></span>                                 <span data-ttu-id="40474-139">`Value`(Read Only)</span><span class="sxs-lookup"><span data-stu-id="40474-139">`Value`(Read Only)</span></span>|  
|<span data-ttu-id="40474-140">Thực thể</span><span class="sxs-lookup"><span data-stu-id="40474-140">Entity</span></span>|<span data-ttu-id="40474-141">Can be in many-to-many relationship</span><span class="sxs-lookup"><span data-stu-id="40474-141">Can be in many-to-many relationship</span></span>|<span data-ttu-id="40474-142"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanBeInManyToMany>.</span><span class="sxs-lookup"><span data-stu-id="40474-142"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanBeInManyToMany>.</span></span>                               <span data-ttu-id="40474-143">`Value`(Read Only)</span><span class="sxs-lookup"><span data-stu-id="40474-143">`Value`(Read Only)</span></span>|  
|<span data-ttu-id="40474-144">Thực thể</span><span class="sxs-lookup"><span data-stu-id="40474-144">Entity</span></span>|<span data-ttu-id="40474-145">Có thể tạo biểu mẫu mới</span><span class="sxs-lookup"><span data-stu-id="40474-145">New forms can be created</span></span>|<span data-ttu-id="40474-146"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanCreateForms>.</span><span class="sxs-lookup"><span data-stu-id="40474-146"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanCreateForms>.</span></span>                              `Value`|  
|<span data-ttu-id="40474-147">Thực thể</span><span class="sxs-lookup"><span data-stu-id="40474-147">Entity</span></span>|<span data-ttu-id="40474-148">Có thể tạo biểu đồ mới</span><span class="sxs-lookup"><span data-stu-id="40474-148">New charts can be created</span></span>|<span data-ttu-id="40474-149"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanCreateCharts>.</span><span class="sxs-lookup"><span data-stu-id="40474-149"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanCreateCharts>.</span></span>                               `Value`|  
|<span data-ttu-id="40474-150">Thực thể</span><span class="sxs-lookup"><span data-stu-id="40474-150">Entity</span></span>|<span data-ttu-id="40474-151">Có thể tạo dạng xem mới</span><span class="sxs-lookup"><span data-stu-id="40474-151">New views can be created</span></span>|<span data-ttu-id="40474-152"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanCreateViews>.</span><span class="sxs-lookup"><span data-stu-id="40474-152"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanCreateViews>.</span></span>                              `Value`|  
|<span data-ttu-id="40474-153">Thực thể</span><span class="sxs-lookup"><span data-stu-id="40474-153">Entity</span></span>|<span data-ttu-id="40474-154">Can change any other entity properties not represented by a managed property</span><span class="sxs-lookup"><span data-stu-id="40474-154">Can change any other entity properties not represented by a managed property</span></span>|<span data-ttu-id="40474-155"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanModifyAdditionalSettings>.</span><span class="sxs-lookup"><span data-stu-id="40474-155"><xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.CanModifyAdditionalSettings>.</span></span>                                `Value`|  
|<span data-ttu-id="40474-156">Field (Attribute)</span><span class="sxs-lookup"><span data-stu-id="40474-156">Field (Attribute)</span></span>|<span data-ttu-id="40474-157">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-157">Can be customized</span></span>|<span data-ttu-id="40474-158"><xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.IsCustomizable>.</span><span class="sxs-lookup"><span data-stu-id="40474-158"><xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.IsCustomizable>.</span></span>                                 `Value`|  
|<span data-ttu-id="40474-159">Field (Attribute)</span><span class="sxs-lookup"><span data-stu-id="40474-159">Field (Attribute)</span></span>|<span data-ttu-id="40474-160">Display name can be modified</span><span class="sxs-lookup"><span data-stu-id="40474-160">Display name can be modified</span></span>|<span data-ttu-id="40474-161"><xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.IsRenameable>.</span><span class="sxs-lookup"><span data-stu-id="40474-161"><xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.IsRenameable>.</span></span>                              `Value`|  
|<span data-ttu-id="40474-162">Field (Attribute)</span><span class="sxs-lookup"><span data-stu-id="40474-162">Field (Attribute)</span></span>|<span data-ttu-id="40474-163">Có thể thay đổi mức yêu cầu</span><span class="sxs-lookup"><span data-stu-id="40474-163">Can change requirement level</span></span>|<span data-ttu-id="40474-164"><xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.RequiredLevel>.</span><span class="sxs-lookup"><span data-stu-id="40474-164"><xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.RequiredLevel>.</span></span>                                `CanBeChanged`<br /><br /> <span data-ttu-id="40474-165">Note:</span><span class="sxs-lookup"><span data-stu-id="40474-165">Note:</span></span><br /><br /> <span data-ttu-id="40474-166">`RequiredLevel`is the only managed property to use the                                     `CanBeChanged`property.</span><span class="sxs-lookup"><span data-stu-id="40474-166">`RequiredLevel`is the only managed property to use the                                     `CanBeChanged`property.</span></span>|  
|<span data-ttu-id="40474-167">Field (Attribute)</span><span class="sxs-lookup"><span data-stu-id="40474-167">Field (Attribute)</span></span>|<span data-ttu-id="40474-168">Can change any other attribute properties not represented by a managed property</span><span class="sxs-lookup"><span data-stu-id="40474-168">Can change any other attribute properties not represented by a managed property</span></span>|<span data-ttu-id="40474-169"><xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.CanModifyAdditionalSettings>.</span><span class="sxs-lookup"><span data-stu-id="40474-169"><xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.CanModifyAdditionalSettings>.</span></span>                                 `Value`|  
|<span data-ttu-id="40474-170">Mối quan hệ của thực thể</span><span class="sxs-lookup"><span data-stu-id="40474-170">Entity Relationship</span></span>|<span data-ttu-id="40474-171">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-171">Can be customized</span></span>|<span data-ttu-id="40474-172"><xref:Microsoft.Xrm.Sdk.Metadata.RelationshipMetadataBase.IsCustomizable>.</span><span class="sxs-lookup"><span data-stu-id="40474-172"><xref:Microsoft.Xrm.Sdk.Metadata.RelationshipMetadataBase.IsCustomizable>.</span></span>                              `Value`|  
|<span data-ttu-id="40474-173">Biểu mẫu</span><span class="sxs-lookup"><span data-stu-id="40474-173">Form</span></span>|<span data-ttu-id="40474-174">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-174">Can be customized</span></span>|`SystemForm.IsCustomizable.Value`|  
|<span data-ttu-id="40474-175">Biểu đồ</span><span class="sxs-lookup"><span data-stu-id="40474-175">Chart</span></span>|<span data-ttu-id="40474-176">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-176">Can be customized</span></span>|`SavedQueryVisualization.IsCustomizable.Value`|  
|<span data-ttu-id="40474-177">Dạng xem</span><span class="sxs-lookup"><span data-stu-id="40474-177">View</span></span>|<span data-ttu-id="40474-178">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-178">Can be customized</span></span>|`SavedQuery.IsCustomizable.Value`|  
|<span data-ttu-id="40474-179">Bộ Tùy chọn</span><span class="sxs-lookup"><span data-stu-id="40474-179">Option Set</span></span>|<span data-ttu-id="40474-180">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-180">Can be customized</span></span>|<span data-ttu-id="40474-181"><xref:Microsoft.Xrm.Sdk.Metadata.OptionSetMetadataBase.IsCustomizable>.</span><span class="sxs-lookup"><span data-stu-id="40474-181"><xref:Microsoft.Xrm.Sdk.Metadata.OptionSetMetadataBase.IsCustomizable>.</span></span>                              `Value`|  
|<span data-ttu-id="40474-182">Tài nguyên Web</span><span class="sxs-lookup"><span data-stu-id="40474-182">Web Resource</span></span>|<span data-ttu-id="40474-183">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-183">Can be customized</span></span>|`WebResource.IsCustomizable.Value`|  
|<span data-ttu-id="40474-184">Quy trình</span><span class="sxs-lookup"><span data-stu-id="40474-184">Workflow</span></span>|<span data-ttu-id="40474-185">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-185">Can be customized</span></span>|`Workflow.IsCustomizable.Value`|  
|<span data-ttu-id="40474-186">Bộ</span><span class="sxs-lookup"><span data-stu-id="40474-186">Assembly</span></span>|<span data-ttu-id="40474-187">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-187">Can be customized</span></span>|`SdkMessageProcessingStep.IsCustomizable.Value`|  
|<span data-ttu-id="40474-188">Assembly Registration</span><span class="sxs-lookup"><span data-stu-id="40474-188">Assembly Registration</span></span>|<span data-ttu-id="40474-189">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-189">Can be customized</span></span>|`ServiceEndpoint.IsCustomizable.Value`|  
|<span data-ttu-id="40474-190">E-mail Template</span><span class="sxs-lookup"><span data-stu-id="40474-190">E-mail Template</span></span>|<span data-ttu-id="40474-191">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-191">Can be customized</span></span>|`Template.IsCustomizable.Value`|  
|<span data-ttu-id="40474-192">KB Article Template</span><span class="sxs-lookup"><span data-stu-id="40474-192">KB Article Template</span></span>|<span data-ttu-id="40474-193">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-193">Can be customized</span></span>|`KbArticleTemplate.IsCustomizable.Value`|  
|<span data-ttu-id="40474-194">Mẫu Hợp đồng</span><span class="sxs-lookup"><span data-stu-id="40474-194">Contract Template</span></span>|<span data-ttu-id="40474-195">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-195">Can be customized</span></span>|`ContractTemplate.IsCustomizable.Value`|  
|<span data-ttu-id="40474-196">Mẫu Trộn Thư</span><span class="sxs-lookup"><span data-stu-id="40474-196">Mail Merge Template</span></span>|<span data-ttu-id="40474-197">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-197">Can be customized</span></span>|`MailMergeTemplate.IsCustomizable.Value`|  
|<span data-ttu-id="40474-198">Bảng thông tin</span><span class="sxs-lookup"><span data-stu-id="40474-198">Dashboard</span></span>|<span data-ttu-id="40474-199">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-199">Can be customized</span></span>|`SystemForm.IsCustomizable.Value`|  
|<span data-ttu-id="40474-200">Vai trò Bảo mật</span><span class="sxs-lookup"><span data-stu-id="40474-200">Security Roles</span></span>|<span data-ttu-id="40474-201">Can be customized</span><span class="sxs-lookup"><span data-stu-id="40474-201">Can be customized</span></span>|`Role.IsCustomizable.Value`|  
  
### <a name="update-managed-properties"></a><span data-ttu-id="40474-202">Update managed properties</span><span class="sxs-lookup"><span data-stu-id="40474-202">Update managed properties</span></span>  
 <span data-ttu-id="40474-203">After you release your managed solution, you may decide that you want to change the managed properties.</span><span class="sxs-lookup"><span data-stu-id="40474-203">After you release your managed solution, you may decide that you want to change the managed properties.</span></span> <span data-ttu-id="40474-204">You can only change managed properties to make them less restrictive.</span><span class="sxs-lookup"><span data-stu-id="40474-204">You can only change managed properties to make them less restrictive.</span></span> <span data-ttu-id="40474-205">For example, after your initial release you can decide to allow customization of an                      entity.</span><span class="sxs-lookup"><span data-stu-id="40474-205">For example, after your initial release you can decide to allow customization of an                      entity.</span></span>  
  
 <span data-ttu-id="40474-206">You update managed properties for your solution by releasing an update to your solution with the changed managed properties.</span><span class="sxs-lookup"><span data-stu-id="40474-206">You update managed properties for your solution by releasing an update to your solution with the changed managed properties.</span></span> <span data-ttu-id="40474-207">Your managed solution can only be updated by another managed solution associated with the same publisher record as the original managed                       solution.</span><span class="sxs-lookup"><span data-stu-id="40474-207">Your managed solution can only be updated by another managed solution associated with the same publisher record as the original managed                       solution.</span></span> <span data-ttu-id="40474-208">If your update includes a change in managed properties to make them more restrictive, those managed property changes will be ignored but other changes in the update will be applied.</span><span class="sxs-lookup"><span data-stu-id="40474-208">If your update includes a change in managed properties to make them more restrictive, those managed property changes will be ignored but other changes in the update will be applied.</span></span>  
  
 <span data-ttu-id="40474-209">Because the original publisher is a requirement to update managed properties for a managed solution, any unmanaged solution cannot be associated with a publisher that has been used to install a managed solution.</span><span class="sxs-lookup"><span data-stu-id="40474-209">Because the original publisher is a requirement to update managed properties for a managed solution, any unmanaged solution cannot be associated with a publisher that has been used to install a managed solution.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="40474-210">This means you will not be able to develop an update for your solution by using an organization where your managed solution is installed.</span><span class="sxs-lookup"><span data-stu-id="40474-210">This means you will not be able to develop an update for your solution by using an organization where your managed solution is installed.</span></span>  
  
## <a name="check-managed-properties"></a><span data-ttu-id="40474-211">Check managed properties</span><span class="sxs-lookup"><span data-stu-id="40474-211">Check managed properties</span></span>  
 <span data-ttu-id="40474-212">Use the                <xref:Microsoft.Crm.Sdk.Messages.IsComponentCustomizableRequest>to check whether a solution component is customizable.</span><span class="sxs-lookup"><span data-stu-id="40474-212">Use the                <xref:Microsoft.Crm.Sdk.Messages.IsComponentCustomizableRequest>to check whether a solution component is customizable.</span></span> <span data-ttu-id="40474-213">Alternatively, you can check the solution component properties but you must consider that the ultimate determination of                 the meaning depends on the values of several properties.</span><span class="sxs-lookup"><span data-stu-id="40474-213">Alternatively, you can check the solution component properties but you must consider that the ultimate determination of                 the meaning depends on the values of several properties.</span></span> <span data-ttu-id="40474-214">Each solution component has an                 `IsCustomizable`property.</span><span class="sxs-lookup"><span data-stu-id="40474-214">Each solution component has an                 `IsCustomizable`property.</span></span> <span data-ttu-id="40474-215">When a solution component is installed as part of a managed solution, the                 `IsManaged`property will be true.</span><span class="sxs-lookup"><span data-stu-id="40474-215">When a solution component is installed as part of a managed solution, the                 `IsManaged`property will be true.</span></span> <span data-ttu-id="40474-216">Managed properties are only enforced for managed solutions.</span><span class="sxs-lookup"><span data-stu-id="40474-216">Managed properties are only enforced for managed solutions.</span></span> <span data-ttu-id="40474-217">When checking managed properties to determine if an individual solution component is customizable, you must check both the                `IsCustomizable`and                 `IsManaged`properties.</span><span class="sxs-lookup"><span data-stu-id="40474-217">When checking managed properties to determine if an individual solution component is customizable, you must check both the                `IsCustomizable`and                 `IsManaged`properties.</span></span> <span data-ttu-id="40474-218">A solution component where               `IsCustomizable`is false and                `IsManaged`is false, is customizable.</span><span class="sxs-lookup"><span data-stu-id="40474-218">A solution component where               `IsCustomizable`is false and                `IsManaged`is false, is customizable.</span></span>  
  
 <span data-ttu-id="40474-219">Entity and attribute have more managed properties in addition to               `IsCustomizable`.</span><span class="sxs-lookup"><span data-stu-id="40474-219">Entity and attribute have more managed properties in addition to               `IsCustomizable`.</span></span> <span data-ttu-id="40474-220">These managed properties are not updated if               `IsCustomizable`is set to false.</span><span class="sxs-lookup"><span data-stu-id="40474-220">These managed properties are not updated if               `IsCustomizable`is set to false.</span></span> <span data-ttu-id="40474-221">This means that in addition to checking the individual managed property, you must also check the               `IsCustomizable`property to see if the managed property is being enforced.</span><span class="sxs-lookup"><span data-stu-id="40474-221">This means that in addition to checking the individual managed property, you must also check the               `IsCustomizable`property to see if the managed property is being enforced.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="40474-222">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="40474-222">See also</span></span>  
 <span data-ttu-id="40474-223">[Thuộc tính được quản lý](introduction-solutions.md#BKMK_ManagedProperties) </span><span class="sxs-lookup"><span data-stu-id="40474-223">[Managed properties](introduction-solutions.md#BKMK_ManagedProperties) </span></span>  
 <span data-ttu-id="40474-224">[Plan For Solution Development](plan-solution-development.md) </span><span class="sxs-lookup"><span data-stu-id="40474-224">[Plan For Solution Development](plan-solution-development.md) </span></span>  
 <span data-ttu-id="40474-225">[Maintain Managed Solutions](maintain-managed-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="40474-225">[Maintain Managed Solutions](maintain-managed-solutions.md) </span></span>  
 <span data-ttu-id="40474-226">[Package and Distribute Extensions with Dynamics 365 for Customer Engagement Solutions](package-distribute-extensions-use-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="40474-226">[Package and Distribute Extensions with Dynamics 365 for Customer Engagement Solutions](package-distribute-extensions-use-solutions.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.IsComponentCustomizableRequest>