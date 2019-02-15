---
title: Enable and disable duplicate detection (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: This topic covers information on how to enable duplicate detection for all entities in an organization, for a specific entity and for specific operations and how to disable duplicate detection globally or for an entity type by unpublishing the duplicate detection rules or by deleting the published rules.
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
- duplicate detection, enabling
- 'enabling duplicate detection, in three areas: globally; for entities; for specific operations'
- 'enabling duplicate detection, how to enable: messages; properties; and attributes to set'
- enabling duplicate detection, rules must be published before running
ms.assetid: B8CD2072-F254-4BA8-9087-79EC79DFE48C
caps.latest.revision: 14
author: SushantSikka
ms.author: susikka
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ca7b10a49a5bd8e383722bf47e3fd920113b48fd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387178"
---
# <a name="enable-and-disable-duplicate-detection"></a><span data-ttu-id="cbefe-103">Enable and Disable duplicate detection</span><span class="sxs-lookup"><span data-stu-id="cbefe-103">Enable and Disable duplicate detection</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="cbefe-104">This topic covers information on how to enable and disable duplicate detection in Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="cbefe-104">This topic covers information on how to enable and disable duplicate detection in Dynamics 365 for Customer Engagement apps.</span></span>

<a name="bkmk_enable"></a>

## <a name="enable-duplicate-detection"></a><span data-ttu-id="cbefe-105">Enable duplicate detection</span><span class="sxs-lookup"><span data-stu-id="cbefe-105">Enable duplicate detection</span></span>

<span data-ttu-id="cbefe-106">Before running duplicate detection, enable it for each of the following:</span><span class="sxs-lookup"><span data-stu-id="cbefe-106">Before running duplicate detection, enable it for each of the following:</span></span>  
  
-   <span data-ttu-id="cbefe-107">Globally (for all entities in the organization).</span><span class="sxs-lookup"><span data-stu-id="cbefe-107">Globally (for all entities in the organization).</span></span>  
  
-   <span data-ttu-id="cbefe-108">For an entity.</span><span class="sxs-lookup"><span data-stu-id="cbefe-108">For an entity.</span></span>  
  
-   <span data-ttu-id="cbefe-109">For specific operations.</span><span class="sxs-lookup"><span data-stu-id="cbefe-109">For specific operations.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cbefe-110">You must enable duplicate detection in all three areas to detect duplicates for an entity and for operations on an entity.</span><span class="sxs-lookup"><span data-stu-id="cbefe-110">You must enable duplicate detection in all three areas to detect duplicates for an entity and for operations on an entity.</span></span>  
  
### <a name="enable-duplicate-detection-globally"></a><span data-ttu-id="cbefe-111">Enable duplicate detection globally</span><span class="sxs-lookup"><span data-stu-id="cbefe-111">Enable duplicate detection globally</span></span>  
  
-   <span data-ttu-id="cbefe-112">Use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message to set the `Organization.IsDuplicateDetectionEnabled` attribute to `true`.</span><span class="sxs-lookup"><span data-stu-id="cbefe-112">Use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message to set the `Organization.IsDuplicateDetectionEnabled` attribute to `true`.</span></span>
-   <span data-ttu-id="cbefe-113">Read [Turn duplicate detection rules on or off for the whole organization](../admin/turn-duplicate-detection-rules-off-whole-organization.md) to find out how you can use the user interface to enable duplicate detection for the entire organization.</span><span class="sxs-lookup"><span data-stu-id="cbefe-113">Read [Turn duplicate detection rules on or off for the whole organization](../admin/turn-duplicate-detection-rules-off-whole-organization.md) to find out how you can use the user interface to enable duplicate detection for the entire organization.</span></span>
  
### <a name="enable-duplicate-detection-for-an-entity"></a><span data-ttu-id="cbefe-114">Enable duplicate detection for an entity</span><span class="sxs-lookup"><span data-stu-id="cbefe-114">Enable duplicate detection for an entity</span></span>  
  
-   <span data-ttu-id="cbefe-115">Use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message to set the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsDuplicateDetectionEnabled> property to `true`.</span><span class="sxs-lookup"><span data-stu-id="cbefe-115">Use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message to set the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsDuplicateDetectionEnabled> property to `true`.</span></span>  
  
### <a name="enable-duplicate-detection-for-specific-operations"></a><span data-ttu-id="cbefe-116">Enable duplicate detection for specific operations</span><span class="sxs-lookup"><span data-stu-id="cbefe-116">Enable duplicate detection for specific operations</span></span>  
  
- <span data-ttu-id="cbefe-117">Set the following attributes to `true`:</span><span class="sxs-lookup"><span data-stu-id="cbefe-117">Set the following attributes to `true`:</span></span>  
  
  - <span data-ttu-id="cbefe-118">`Organization.IsDuplicateDetectionEnabledForOnlineCreateUpdate`.</span><span class="sxs-lookup"><span data-stu-id="cbefe-118">`Organization.IsDuplicateDetectionEnabledForOnlineCreateUpdate`.</span></span> <span data-ttu-id="cbefe-119">Create and update records in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] by using the Web application or [!INCLUDE[pn_crm_for_outlook_full](../includes/pn-crm-for-outlook-full.md)].</span><span class="sxs-lookup"><span data-stu-id="cbefe-119">Create and update records in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] by using the Web application or [!INCLUDE[pn_crm_for_outlook_full](../includes/pn-crm-for-outlook-full.md)].</span></span> <span data-ttu-id="cbefe-120">This attribute enables or disables duplicate detection for records created or updated with the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> and <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> messages.</span><span class="sxs-lookup"><span data-stu-id="cbefe-120">This attribute enables or disables duplicate detection for records created or updated with the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> and <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> messages.</span></span> <span data-ttu-id="cbefe-121">However, it does not affect records created or updated with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="cbefe-121">However, it does not affect records created or updated with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span> <span data-ttu-id="cbefe-122">and <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span><span class="sxs-lookup"><span data-stu-id="cbefe-122">and <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span></span> <span data-ttu-id="cbefe-123">methods.</span><span class="sxs-lookup"><span data-stu-id="cbefe-123">methods.</span></span>  
  
  - <span data-ttu-id="cbefe-124">`Organization.IsDuplicateDetectionEnabledForOfflineSync`.</span><span class="sxs-lookup"><span data-stu-id="cbefe-124">`Organization.IsDuplicateDetectionEnabledForOfflineSync`.</span></span> <span data-ttu-id="cbefe-125">Synchronize offline records when [!INCLUDE[pn_crm_for_outlook_full](../includes/pn-crm-for-outlook-full.md)] goes from offline to online.</span><span class="sxs-lookup"><span data-stu-id="cbefe-125">Synchronize offline records when [!INCLUDE[pn_crm_for_outlook_full](../includes/pn-crm-for-outlook-full.md)] goes from offline to online.</span></span>  
  
  - <span data-ttu-id="cbefe-126">`Organization.IsDuplicateDetectionEnabledForImport`.</span><span class="sxs-lookup"><span data-stu-id="cbefe-126">`Organization.IsDuplicateDetectionEnabledForImport`.</span></span> <span data-ttu-id="cbefe-127">Import bulk data.</span><span class="sxs-lookup"><span data-stu-id="cbefe-127">Import bulk data.</span></span>  
  
  > [!NOTE]
  >  <span data-ttu-id="cbefe-128">You do not have to publish the duplicate detection rules to enable duplicate detection for these operations.</span><span class="sxs-lookup"><span data-stu-id="cbefe-128">You do not have to publish the duplicate detection rules to enable duplicate detection for these operations.</span></span> <span data-ttu-id="cbefe-129">However, you must publish the duplicate detection rules before you perform the operations.</span><span class="sxs-lookup"><span data-stu-id="cbefe-129">However, you must publish the duplicate detection rules before you perform the operations.</span></span>  

<a name="bkmk_disable"></a>

## <a name="disable-duplicate-detection"></a><span data-ttu-id="cbefe-130">Disable duplicate detection</span><span class="sxs-lookup"><span data-stu-id="cbefe-130">Disable duplicate detection</span></span>

<span data-ttu-id="cbefe-131">Disable duplicate detection globally or for an entity type by unpublishing the duplicate detection rules or by deleting the published rules.</span><span class="sxs-lookup"><span data-stu-id="cbefe-131">Disable duplicate detection globally or for an entity type by unpublishing the duplicate detection rules or by deleting the published rules.</span></span>  
  
 <span data-ttu-id="cbefe-132">**Disable duplicate detection globally**</span><span class="sxs-lookup"><span data-stu-id="cbefe-132">**Disable duplicate detection globally**</span></span>  
  
 <span data-ttu-id="cbefe-133">To disable duplicate detection globally, use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message to set the `Organization.IsDuplicateDetectionEnabled` attribute to `false`.</span><span class="sxs-lookup"><span data-stu-id="cbefe-133">To disable duplicate detection globally, use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message to set the `Organization.IsDuplicateDetectionEnabled` attribute to `false`.</span></span> <span data-ttu-id="cbefe-134">This automatically unpublishes all duplicate detection rules for all entity types in the organization.</span><span class="sxs-lookup"><span data-stu-id="cbefe-134">This automatically unpublishes all duplicate detection rules for all entity types in the organization.</span></span>  
  
 <span data-ttu-id="cbefe-135">**Disable duplicate detection for an entity**</span><span class="sxs-lookup"><span data-stu-id="cbefe-135">**Disable duplicate detection for an entity**</span></span>  
  
 <span data-ttu-id="cbefe-136">To disable duplicate detection for an entity type, do one of the following:</span><span class="sxs-lookup"><span data-stu-id="cbefe-136">To disable duplicate detection for an entity type, do one of the following:</span></span>  
  
-   <span data-ttu-id="cbefe-137">Use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest> message to set the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsDuplicateDetectionEnabled> property to `false`.</span><span class="sxs-lookup"><span data-stu-id="cbefe-137">Use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest> message to set the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsDuplicateDetectionEnabled> property to `false`.</span></span> <span data-ttu-id="cbefe-138">This automatically unpublishes all duplicate detection rules for an entity type.</span><span class="sxs-lookup"><span data-stu-id="cbefe-138">This automatically unpublishes all duplicate detection rules for an entity type.</span></span> <span data-ttu-id="cbefe-139">This removes duplicate detection support for the entity type and you cannot create a new duplicate detection rule for this entity type.</span><span class="sxs-lookup"><span data-stu-id="cbefe-139">This removes duplicate detection support for the entity type and you cannot create a new duplicate detection rule for this entity type.</span></span>  
  
-   <span data-ttu-id="cbefe-140">Unpublish all duplicate detection rules for an entity type by using the <xref:Microsoft.Crm.Sdk.Messages.UnpublishDuplicateRuleRequest> message.</span><span class="sxs-lookup"><span data-stu-id="cbefe-140">Unpublish all duplicate detection rules for an entity type by using the <xref:Microsoft.Crm.Sdk.Messages.UnpublishDuplicateRuleRequest> message.</span></span>  
  
<span data-ttu-id="cbefe-141">**Delete published duplicate detection rules**</span><span class="sxs-lookup"><span data-stu-id="cbefe-141">**Delete published duplicate detection rules**</span></span>  
  
<span data-ttu-id="cbefe-142">Delete all published rules in the system to disable duplicate detection globally, or delete published rules for specific entity types by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span><span class="sxs-lookup"><span data-stu-id="cbefe-142">Delete all published rules in the system to disable duplicate detection globally, or delete published rules for specific entity types by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span></span> <span data-ttu-id="cbefe-143">method.</span><span class="sxs-lookup"><span data-stu-id="cbefe-143">method.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cbefe-144">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="cbefe-144">See Also</span></span>

[<span data-ttu-id="cbefe-145">Phát hiện trùng lặp</span><span class="sxs-lookup"><span data-stu-id="cbefe-145">Duplicate Detection</span></span>](detect-duplicate-data-for-developers.md)  
<span data-ttu-id="cbefe-146">[Running Duplicate Detection](run-duplicate-detection.md) </span><span class="sxs-lookup"><span data-stu-id="cbefe-146">[Running Duplicate Detection](run-duplicate-detection.md) </span></span>  
[<span data-ttu-id="cbefe-147">Duplicate Rule entities</span><span class="sxs-lookup"><span data-stu-id="cbefe-147">Duplicate Rule entities</span></span>](duplicaterule-entities.md) 
