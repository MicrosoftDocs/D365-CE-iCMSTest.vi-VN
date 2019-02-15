---
title: Configure entities and attributes for auditing (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Explains configuration requirements to enable and disable auditing of entities and their attributes.
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
- enabling and disabling auditing, how to
- configuring entities and attributes for auditing, required security roles for enabling or disabling auditing
- enabling and disabling auditing, default settings for enabled auditing
- configuring entities and attributes for auditing, auditable entities
- configuring entities and attributes for auditing, difference between enabling for different levels
- auditing, see 'auditing entity data changes in Microsoft Dynamics CRM'
- enabling and disabling auditing, auditable entities
- configuring entities and attributes for auditing, default settings for enabled auditing
- auditing levels, descriptions of the three levels
- enabling and disabling auditing, list of entities that cannot be audited
- security roles for enabling or disabling auditing, required role levels
- configuring entities and attributes for auditing, descriptions of the three auditing levels
- configuring entities and attributes for auditing, list of entities that cannot be audited
ms.assetid: 4e36f9d4-08cd-4f57-a02b-33581e54ce5f
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 00571eb43c6b2f842e071add5fafe6cc7009dafc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386629"
---
# <a name="configure-entities-and-attributes-for-auditing"></a><span data-ttu-id="1f5b5-103">Configure entities and attributes for auditing</span><span class="sxs-lookup"><span data-stu-id="1f5b5-103">Configure entities and attributes for auditing</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="1f5b5-104">There are three levels where auditing can be configured: organization, entity, and attribute.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-104">There are three levels where auditing can be configured: organization, entity, and attribute.</span></span> <span data-ttu-id="1f5b5-105">The organization level is the highest level, followed by the entity level, and finally the attribute level.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-105">The organization level is the highest level, followed by the entity level, and finally the attribute level.</span></span> <span data-ttu-id="1f5b5-106">For attribute auditing to take place, auditing must be enabled at the attribute, entity, and organization levels.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-106">For attribute auditing to take place, auditing must be enabled at the attribute, entity, and organization levels.</span></span> <span data-ttu-id="1f5b5-107">For entity auditing to take place, auditing must be enabled at the entity and organization levels.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-107">For entity auditing to take place, auditing must be enabled at the entity and organization levels.</span></span>  
  
 <span data-ttu-id="1f5b5-108">There is a slight difference in how auditing is enabled or disable for an organization compared to an entity or attribute.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-108">There is a slight difference in how auditing is enabled or disable for an organization compared to an entity or attribute.</span></span> <span data-ttu-id="1f5b5-109">You enable or disable auditing at the organization level by setting a particular attribute value of the organization record.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-109">You enable or disable auditing at the organization level by setting a particular attribute value of the organization record.</span></span> <span data-ttu-id="1f5b5-110">However, for entities and attributes, you set a property value of the entity or attribute metadata.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-110">However, for entities and attributes, you set a property value of the entity or attribute metadata.</span></span>  
  
 <span data-ttu-id="1f5b5-111">A user must be assigned the System Administrator or System Customizer role to enable or disable auditing.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-111">A user must be assigned the System Administrator or System Customizer role to enable or disable auditing.</span></span>  
  
## <a name="enabling-auditing"></a><span data-ttu-id="1f5b5-112">Enabling auditing</span><span class="sxs-lookup"><span data-stu-id="1f5b5-112">Enabling auditing</span></span>  
 <span data-ttu-id="1f5b5-113">By setting the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsAuditEnabled> property of an entity’s metadata and the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.IsAuditEnabled> property of each desired attribute’s metadata to `true`, data changes to records of those entities can be logged by the platform.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-113">By setting the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsAuditEnabled> property of an entity’s metadata and the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.IsAuditEnabled> property of each desired attribute’s metadata to `true`, data changes to records of those entities can be logged by the platform.</span></span> <span data-ttu-id="1f5b5-114">However, when enabling auditing on an entity, all of the entity’s attributes are enabled for auditing by default.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-114">However, when enabling auditing on an entity, all of the entity’s attributes are enabled for auditing by default.</span></span> <span data-ttu-id="1f5b5-115">Of course you can explicitly disable auditing on any or all of the attributes as needed.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-115">Of course you can explicitly disable auditing on any or all of the attributes as needed.</span></span> <span data-ttu-id="1f5b5-116">The <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsAuditEnabled> property can be set when entity or attribute metadata is created or updated through the following requests: <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest>, <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest>, <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest>, <xref:Microsoft.Xrm.Sdk.Messages.UpdateAttributeRequest>.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-116">The <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsAuditEnabled> property can be set when entity or attribute metadata is created or updated through the following requests: <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest>, <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest>, <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest>, <xref:Microsoft.Xrm.Sdk.Messages.UpdateAttributeRequest>.</span></span>  
  
 <span data-ttu-id="1f5b5-117">After changing the entity attribute metadata, you must publish the entity by using <xref:Microsoft.Crm.Sdk.Messages.PublishXmlRequest>.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-117">After changing the entity attribute metadata, you must publish the entity by using <xref:Microsoft.Crm.Sdk.Messages.PublishXmlRequest>.</span></span> <span data-ttu-id="1f5b5-118">Changing the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsAuditEnabled> property at the entity level does not require publishing.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-118">Changing the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsAuditEnabled> property at the entity level does not require publishing.</span></span> <span data-ttu-id="1f5b5-119">Typically, customization and publishing is performed by the same user.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-119">Typically, customization and publishing is performed by the same user.</span></span> <span data-ttu-id="1f5b5-120">However, if these tasks are performed by different users, auditing will record the publish action, the user that initiated the publish operation, and not the update action.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-120">However, if these tasks are performed by different users, auditing will record the publish action, the user that initiated the publish operation, and not the update action.</span></span>  
  
 <span data-ttu-id="1f5b5-121">In addition, auditing is enabled at the organization level by setting the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsAuditEnabled> attribute value of the target organization record to `true`.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-121">In addition, auditing is enabled at the organization level by setting the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsAuditEnabled> attribute value of the target organization record to `true`.</span></span>  
  
## <a name="disabling-auditing"></a><span data-ttu-id="1f5b5-122">Disabling auditing</span><span class="sxs-lookup"><span data-stu-id="1f5b5-122">Disabling auditing</span></span>  
 <span data-ttu-id="1f5b5-123">To disable auditing, just set <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsAuditEnabled>, as described previously, to `false`.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-123">To disable auditing, just set <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsAuditEnabled>, as described previously, to `false`.</span></span> <span data-ttu-id="1f5b5-124">Publish the entity customizations if you have disabled auditing on any attributes.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-124">Publish the entity customizations if you have disabled auditing on any attributes.</span></span> <span data-ttu-id="1f5b5-125">You can disable auditing for a whole organization by setting the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsAuditEnabled> attribute to `false` in the target organization’s record.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-125">You can disable auditing for a whole organization by setting the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsAuditEnabled> attribute to `false` in the target organization’s record.</span></span>  
  
## <a name="entities-that-can-be-audited"></a><span data-ttu-id="1f5b5-126">Entities that can be audited</span><span class="sxs-lookup"><span data-stu-id="1f5b5-126">Entities that can be audited</span></span>  
 <span data-ttu-id="1f5b5-127">All custom and most customizable entities can be audited.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-127">All custom and most customizable entities can be audited.</span></span> <span data-ttu-id="1f5b5-128">For a list of customizable entities, see [Which Entities are Customizable?](which-entities-are-customizable.md).</span><span class="sxs-lookup"><span data-stu-id="1f5b5-128">For a list of customizable entities, see [Which Entities are Customizable?](which-entities-are-customizable.md).</span></span>  
  
 <span data-ttu-id="1f5b5-129">The following table lists the non-customizable entities that cannot be audited.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-129">The following table lists the non-customizable entities that cannot be audited.</span></span> <span data-ttu-id="1f5b5-130">This table was obtained by testing for a `CanModifyAuditSettings` attribute value of `false` on each entity’s metadata.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-130">This table was obtained by testing for a `CanModifyAuditSettings` attribute value of `false` on each entity’s metadata.</span></span>  
  
||  
|-|  
|<span data-ttu-id="1f5b5-131">ActivityPointer</span><span class="sxs-lookup"><span data-stu-id="1f5b5-131">ActivityPointer</span></span>|  
|<span data-ttu-id="1f5b5-132">Annotation</span><span class="sxs-lookup"><span data-stu-id="1f5b5-132">Annotation</span></span>|  
|<span data-ttu-id="1f5b5-133">BulkOperation</span><span class="sxs-lookup"><span data-stu-id="1f5b5-133">BulkOperation</span></span>|  
|<span data-ttu-id="1f5b5-134">Calendar</span><span class="sxs-lookup"><span data-stu-id="1f5b5-134">Calendar</span></span>|  
|<span data-ttu-id="1f5b5-135">CalendarRule</span><span class="sxs-lookup"><span data-stu-id="1f5b5-135">CalendarRule</span></span>|  
|<span data-ttu-id="1f5b5-136">CustomerOpportunityRole</span><span class="sxs-lookup"><span data-stu-id="1f5b5-136">CustomerOpportunityRole</span></span>|  
|<span data-ttu-id="1f5b5-137">Giảm giá</span><span class="sxs-lookup"><span data-stu-id="1f5b5-137">Discount</span></span>|  
|<span data-ttu-id="1f5b5-138">DiscountType</span><span class="sxs-lookup"><span data-stu-id="1f5b5-138">DiscountType</span></span>|  
|<span data-ttu-id="1f5b5-139">IncidentResolution</span><span class="sxs-lookup"><span data-stu-id="1f5b5-139">IncidentResolution</span></span>|  
|<span data-ttu-id="1f5b5-140">KbArticle</span><span class="sxs-lookup"><span data-stu-id="1f5b5-140">KbArticle</span></span>|  
|<span data-ttu-id="1f5b5-141">KbArticleComment</span><span class="sxs-lookup"><span data-stu-id="1f5b5-141">KbArticleComment</span></span>|  
|<span data-ttu-id="1f5b5-142">KbArticleTemplate</span><span class="sxs-lookup"><span data-stu-id="1f5b5-142">KbArticleTemplate</span></span>|  
|<span data-ttu-id="1f5b5-143">Thông báo</span><span class="sxs-lookup"><span data-stu-id="1f5b5-143">Notification</span></span>|  
|<span data-ttu-id="1f5b5-144">OpportunityClose</span><span class="sxs-lookup"><span data-stu-id="1f5b5-144">OpportunityClose</span></span>|  
|<span data-ttu-id="1f5b5-145">OrderClose</span><span class="sxs-lookup"><span data-stu-id="1f5b5-145">OrderClose</span></span>|  
|<span data-ttu-id="1f5b5-146">ProductPriceLevel</span><span class="sxs-lookup"><span data-stu-id="1f5b5-146">ProductPriceLevel</span></span>|  
|<span data-ttu-id="1f5b5-147">QuoteClose</span><span class="sxs-lookup"><span data-stu-id="1f5b5-147">QuoteClose</span></span>|  
|<span data-ttu-id="1f5b5-148">RecurrenceRule</span><span class="sxs-lookup"><span data-stu-id="1f5b5-148">RecurrenceRule</span></span>|  
|<span data-ttu-id="1f5b5-149">Nguồn lực</span><span class="sxs-lookup"><span data-stu-id="1f5b5-149">Resource</span></span>|  
|<span data-ttu-id="1f5b5-150">Nhóm Nguồn lực</span><span class="sxs-lookup"><span data-stu-id="1f5b5-150">ResourceGroup</span></span>|  
|<span data-ttu-id="1f5b5-151">ResourceGroupExpansion</span><span class="sxs-lookup"><span data-stu-id="1f5b5-151">ResourceGroupExpansion</span></span>|  
|<span data-ttu-id="1f5b5-152">ResourceSpec</span><span class="sxs-lookup"><span data-stu-id="1f5b5-152">ResourceSpec</span></span>|  
|<span data-ttu-id="1f5b5-153">SalesLiteratureItem</span><span class="sxs-lookup"><span data-stu-id="1f5b5-153">SalesLiteratureItem</span></span>|  
|<span data-ttu-id="1f5b5-154">SalesProcessInstance</span><span class="sxs-lookup"><span data-stu-id="1f5b5-154">SalesProcessInstance</span></span>|  
|<span data-ttu-id="1f5b5-155">Dịch vụ </span><span class="sxs-lookup"><span data-stu-id="1f5b5-155">Service</span></span>|  
|<span data-ttu-id="1f5b5-156">Chủ đề</span><span class="sxs-lookup"><span data-stu-id="1f5b5-156">Subject</span></span>|  
|<span data-ttu-id="1f5b5-157">Mẫu</span><span class="sxs-lookup"><span data-stu-id="1f5b5-157">Template</span></span>|  
|<span data-ttu-id="1f5b5-158">UoM</span><span class="sxs-lookup"><span data-stu-id="1f5b5-158">UoM</span></span>|  
|<span data-ttu-id="1f5b5-159">UoMSchedule</span><span class="sxs-lookup"><span data-stu-id="1f5b5-159">UoMSchedule</span></span>|  
|<span data-ttu-id="1f5b5-160">Quy trình</span><span class="sxs-lookup"><span data-stu-id="1f5b5-160">Workflow</span></span>|  
|<span data-ttu-id="1f5b5-161">WorkflowLog</span><span class="sxs-lookup"><span data-stu-id="1f5b5-161">WorkflowLog</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="1f5b5-162">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1f5b5-162">See also</span></span>  
 <span data-ttu-id="1f5b5-163">[Data Management in Dynamics 365 for Customer Engagement apps](manage-data.md) </span><span class="sxs-lookup"><span data-stu-id="1f5b5-163">[Data Management in Dynamics 365 for Customer Engagement apps](manage-data.md) </span></span>  
 <span data-ttu-id="1f5b5-164">[Audit entity data changes](audit-entity-data-changes.md) </span><span class="sxs-lookup"><span data-stu-id="1f5b5-164">[Audit entity data changes](audit-entity-data-changes.md) </span></span>  
 <span data-ttu-id="1f5b5-165">[Retrieve and delete the history of audited data changes](retrieve-and-delete-the-history-of-audited-data-changes.md) </span><span class="sxs-lookup"><span data-stu-id="1f5b5-165">[Retrieve and delete the history of audited data changes](retrieve-and-delete-the-history-of-audited-data-changes.md) </span></span>  
 <span data-ttu-id="1f5b5-166">[Sample: Audit Entity Data Changes](sample-audit-entity-data-changes.md) </span><span class="sxs-lookup"><span data-stu-id="1f5b5-166">[Sample: Audit Entity Data Changes](sample-audit-entity-data-changes.md) </span></span>  
 [<span data-ttu-id="1f5b5-167">Auditing Data Changes in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="1f5b5-167">Auditing Data Changes in Dynamics 365 for Customer Engagement apps</span></span>](audit-entity-data-changes.md)
