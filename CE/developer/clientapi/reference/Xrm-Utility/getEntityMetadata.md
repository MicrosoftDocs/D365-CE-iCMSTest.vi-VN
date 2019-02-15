---
title: getEntityMetadata (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 05/02/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 89123cde-7c66-4c7d-94e4-e287285019f8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 396c9a4ecccde61007f238c4e98721202e3dea7d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385689"
---
# <a name="getentitymetadata"></a><span data-ttu-id="32653-102">getEntityMetadata</span><span class="sxs-lookup"><span data-stu-id="32653-102">getEntityMetadata</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getEntityMetadata-description.md](./includes/getEntityMetadata-description.md)] 

## <a name="syntax"></a><span data-ttu-id="32653-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="32653-103">Syntax</span></span>

`Xrm.Utility.getEntityMetadata(entityName,attributes).then(successCallback, errorCallback)`

## <a name="parameters"></a><span data-ttu-id="32653-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="32653-104">Parameters</span></span>

|<span data-ttu-id="32653-105">Tên</span><span class="sxs-lookup"><span data-stu-id="32653-105">Name</span></span> |<span data-ttu-id="32653-106">Loại</span><span class="sxs-lookup"><span data-stu-id="32653-106">Type</span></span> |<span data-ttu-id="32653-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="32653-107">Required</span></span> |<span data-ttu-id="32653-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="32653-108">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="32653-109">entityName</span><span class="sxs-lookup"><span data-stu-id="32653-109">entityName</span></span>|<span data-ttu-id="32653-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="32653-110">String</span></span>|<span data-ttu-id="32653-111">Có</span><span class="sxs-lookup"><span data-stu-id="32653-111">Yes</span></span>|<span data-ttu-id="32653-112">The logical name of the entity.</span><span class="sxs-lookup"><span data-stu-id="32653-112">The logical name of the entity.</span></span>|
|<span data-ttu-id="32653-113">attributes</span><span class="sxs-lookup"><span data-stu-id="32653-113">attributes</span></span>|<span data-ttu-id="32653-114">array of strings</span><span class="sxs-lookup"><span data-stu-id="32653-114">array of strings</span></span>|<span data-ttu-id="32653-115">Không</span><span class="sxs-lookup"><span data-stu-id="32653-115">No</span></span>|<span data-ttu-id="32653-116">The attributes to get metadata for.</span><span class="sxs-lookup"><span data-stu-id="32653-116">The attributes to get metadata for.</span></span>|
|<span data-ttu-id="32653-117">successCallback</span><span class="sxs-lookup"><span data-stu-id="32653-117">successCallback</span></span>|<span data-ttu-id="32653-118">function</span><span class="sxs-lookup"><span data-stu-id="32653-118">function</span></span>|<span data-ttu-id="32653-119">Không</span><span class="sxs-lookup"><span data-stu-id="32653-119">No</span></span>|<span data-ttu-id="32653-120">A function to call when the entity metadata is returned.</span><span class="sxs-lookup"><span data-stu-id="32653-120">A function to call when the entity metadata is returned.</span></span>|
|<span data-ttu-id="32653-121">errorCallback</span><span class="sxs-lookup"><span data-stu-id="32653-121">errorCallback</span></span>|<span data-ttu-id="32653-122">function</span><span class="sxs-lookup"><span data-stu-id="32653-122">function</span></span>|<span data-ttu-id="32653-123">Không</span><span class="sxs-lookup"><span data-stu-id="32653-123">No</span></span>|<span data-ttu-id="32653-124">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="32653-124">A function to call when the operation fails.</span></span>|

## <a name="returns"></a><span data-ttu-id="32653-125">Returns</span><span class="sxs-lookup"><span data-stu-id="32653-125">Returns</span></span>

<span data-ttu-id="32653-126">**Type**: Object</span><span class="sxs-lookup"><span data-stu-id="32653-126">**Type**: Object</span></span>

<span data-ttu-id="32653-127">**Description**: An object containing the entity metadata information with the following attributes.</span><span class="sxs-lookup"><span data-stu-id="32653-127">**Description**: An object containing the entity metadata information with the following attributes.</span></span>

<table>
<tr>
<th><span data-ttu-id="32653-128">Attribute Name</span><span class="sxs-lookup"><span data-stu-id="32653-128">Attribute Name</span></span></th>
<th><span data-ttu-id="32653-129">Loại</span><span class="sxs-lookup"><span data-stu-id="32653-129">Type</span></span></th>
<th><span data-ttu-id="32653-130">Mô tả</span><span class="sxs-lookup"><span data-stu-id="32653-130">Description</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="32653-131">ActivityTypeMask</span><span class="sxs-lookup"><span data-stu-id="32653-131">ActivityTypeMask</span></span></td>
<td><span data-ttu-id="32653-132">Số</span><span class="sxs-lookup"><span data-stu-id="32653-132">Number</span></span></td>
<td><span data-ttu-id="32653-133">Whether a custom activity should appear in the activity menus in the Web application.</span><span class="sxs-lookup"><span data-stu-id="32653-133">Whether a custom activity should appear in the activity menus in the Web application.</span></span> <span data-ttu-id="32653-134">0 indicates that the custom activity doesn't appear; 1 indicates that it does appear.</span><span class="sxs-lookup"><span data-stu-id="32653-134">0 indicates that the custom activity doesn't appear; 1 indicates that it does appear.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-135">AutoRouteToOwnerQueue</span><span class="sxs-lookup"><span data-stu-id="32653-135">AutoRouteToOwnerQueue</span></span></td>
<td><span data-ttu-id="32653-136">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-136">Boolean</span></span></td>
<td><span data-ttu-id="32653-137">Indicates whether to automatically move records to the owner’s default queue when a record of this type is created or assigned.</span><span class="sxs-lookup"><span data-stu-id="32653-137">Indicates whether to automatically move records to the owner’s default queue when a record of this type is created or assigned.</span></span> </td>
</tr>

<tr>
<td><span data-ttu-id="32653-138">CanEnableSyncToExternalSearchIndex</span><span class="sxs-lookup"><span data-stu-id="32653-138">CanEnableSyncToExternalSearchIndex</span></span></td>
<td><span data-ttu-id="32653-139">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-139">Boolean</span></span></td>
<td><span data-ttu-id="32653-140">Chỉ sử dụng nội bộ.</span><span class="sxs-lookup"><span data-stu-id="32653-140">For internal use only.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-141">CanTriggerWorkflow</span><span class="sxs-lookup"><span data-stu-id="32653-141">CanTriggerWorkflow</span></span></td>
<td><span data-ttu-id="32653-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-142">Boolean</span></span></td>
<td><span data-ttu-id="32653-143">Indicates whether the entity can trigger a workflow process.</span><span class="sxs-lookup"><span data-stu-id="32653-143">Indicates whether the entity can trigger a workflow process.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-144">Mô tả</span><span class="sxs-lookup"><span data-stu-id="32653-144">Description</span></span></td>
<td><span data-ttu-id="32653-145">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="32653-145">String</span></span></td>
<td><span data-ttu-id="32653-146">Description for the entity.</span><span class="sxs-lookup"><span data-stu-id="32653-146">Description for the entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-147">DisplayCollectionName</span><span class="sxs-lookup"><span data-stu-id="32653-147">DisplayCollectionName</span></span></td>
<td><span data-ttu-id="32653-148">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="32653-148">String</span></span></td>
<td><span data-ttu-id="32653-149">Plural display name for the entity.</span><span class="sxs-lookup"><span data-stu-id="32653-149">Plural display name for the entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-150">DisplayName</span><span class="sxs-lookup"><span data-stu-id="32653-150">DisplayName</span></span></td>
<td><span data-ttu-id="32653-151">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="32653-151">String</span></span></td>
<td><span data-ttu-id="32653-152">Display name for the entity.</span><span class="sxs-lookup"><span data-stu-id="32653-152">Display name for the entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-153">EnforceStateTransitions</span><span class="sxs-lookup"><span data-stu-id="32653-153">EnforceStateTransitions</span></span></td>
<td><span data-ttu-id="32653-154">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-154">Boolean</span></span></td>
<td><span data-ttu-id="32653-155">Indicates whether the entity will enforce custom state transitions.</span><span class="sxs-lookup"><span data-stu-id="32653-155">Indicates whether the entity will enforce custom state transitions.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-156">EntityColor</span><span class="sxs-lookup"><span data-stu-id="32653-156">EntityColor</span></span></td>
<td><span data-ttu-id="32653-157">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="32653-157">String</span></span></td>
<td><span data-ttu-id="32653-158">The hexadecimal code to represent the color to be used for this entity in the application.</span><span class="sxs-lookup"><span data-stu-id="32653-158">The hexadecimal code to represent the color to be used for this entity in the application.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-159">EntitySetName</span><span class="sxs-lookup"><span data-stu-id="32653-159">EntitySetName</span></span></td>
<td><span data-ttu-id="32653-160">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="32653-160">String</span></span></td>
<td><span data-ttu-id="32653-161">The name of the Web API entity set for this entity.</span><span class="sxs-lookup"><span data-stu-id="32653-161">The name of the Web API entity set for this entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-162">HasActivities</span><span class="sxs-lookup"><span data-stu-id="32653-162">HasActivities</span></span></td>
<td><span data-ttu-id="32653-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-163">Boolean</span></span></td>
<td><span data-ttu-id="32653-164">Indicates whether activities are associated with this entity.</span><span class="sxs-lookup"><span data-stu-id="32653-164">Indicates whether activities are associated with this entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-165">IsActivity</span><span class="sxs-lookup"><span data-stu-id="32653-165">IsActivity</span></span></td>
<td><span data-ttu-id="32653-166">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-166">Boolean</span></span></td>
<td><span data-ttu-id="32653-167">Indicates whether the entity is an activity.</span><span class="sxs-lookup"><span data-stu-id="32653-167">Indicates whether the entity is an activity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-168">IsActivityParty</span><span class="sxs-lookup"><span data-stu-id="32653-168">IsActivityParty</span></span></td>
<td><span data-ttu-id="32653-169">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-169">Boolean</span></span></td>
<td><span data-ttu-id="32653-170">Indicates whether the email messages can be sent to an email address stored in a record of this type.</span><span class="sxs-lookup"><span data-stu-id="32653-170">Indicates whether the email messages can be sent to an email address stored in a record of this type.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-171">IsBusinessProcessEnabled</span><span class="sxs-lookup"><span data-stu-id="32653-171">IsBusinessProcessEnabled</span></span></td>
<td><span data-ttu-id="32653-172">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-172">Boolean</span></span></td>
<td><span data-ttu-id="32653-173">Indicates whether the entity is enabled for business process flows.</span><span class="sxs-lookup"><span data-stu-id="32653-173">Indicates whether the entity is enabled for business process flows.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-174">IsBPFEntity</span><span class="sxs-lookup"><span data-stu-id="32653-174">IsBPFEntity</span></span></td>
<td><span data-ttu-id="32653-175">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-175">Boolean</span></span></td>
<td><span data-ttu-id="32653-176">Indicates whether the entity is a business process flow entity.</span><span class="sxs-lookup"><span data-stu-id="32653-176">Indicates whether the entity is a business process flow entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-177">IsChildEntity</span><span class="sxs-lookup"><span data-stu-id="32653-177">IsChildEntity</span></span></td>
<td><span data-ttu-id="32653-178">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-178">Boolean</span></span></td>
<td><span data-ttu-id="32653-179">Indicates whether the entity is a child entity.</span><span class="sxs-lookup"><span data-stu-id="32653-179">Indicates whether the entity is a child entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-180">IsConnectionsEnabled</span><span class="sxs-lookup"><span data-stu-id="32653-180">IsConnectionsEnabled</span></span></td>
<td><span data-ttu-id="32653-181">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-181">Boolean</span></span></td>
<td><span data-ttu-id="32653-182">Indicates whether connections are enabled for this entity.</span><span class="sxs-lookup"><span data-stu-id="32653-182">Indicates whether connections are enabled for this entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-183">IsCustomEntity</span><span class="sxs-lookup"><span data-stu-id="32653-183">IsCustomEntity</span></span></td>
<td><span data-ttu-id="32653-184">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-184">Boolean</span></span></td>
<td><span data-ttu-id="32653-185">Indicates whether the entity is a custom entity.</span><span class="sxs-lookup"><span data-stu-id="32653-185">Indicates whether the entity is a custom entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-186">IsCustomizable</span><span class="sxs-lookup"><span data-stu-id="32653-186">IsCustomizable</span></span></td>
<td><span data-ttu-id="32653-187">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-187">Boolean</span></span></td>
<td><span data-ttu-id="32653-188">Indicates whether the entity is customizable.</span><span class="sxs-lookup"><span data-stu-id="32653-188">Indicates whether the entity is customizable.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-189">IsDocumentManagementEnabled</span><span class="sxs-lookup"><span data-stu-id="32653-189">IsDocumentManagementEnabled</span></span></td>
<td><span data-ttu-id="32653-190">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-190">Boolean</span></span></td>
<td><span data-ttu-id="32653-191">Indicates whether document management is enabled.</span><span class="sxs-lookup"><span data-stu-id="32653-191">Indicates whether document management is enabled.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-192">IsDocumentRecommendationsEnabled</span><span class="sxs-lookup"><span data-stu-id="32653-192">IsDocumentRecommendationsEnabled</span></span></td>
<td><span data-ttu-id="32653-193">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-193">Boolean</span></span></td>
<td><span data-ttu-id="32653-194">Indicates whether the documemt recommendations is enabled.</span><span class="sxs-lookup"><span data-stu-id="32653-194">Indicates whether the documemt recommendations is enabled.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-195">IsDuplicateDetectionEnabled</span><span class="sxs-lookup"><span data-stu-id="32653-195">IsDuplicateDetectionEnabled</span></span></td>
<td><span data-ttu-id="32653-196">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-196">Boolean</span></span></td>
<td><span data-ttu-id="32653-197">Indicates whether duplicate detection is enabled.</span><span class="sxs-lookup"><span data-stu-id="32653-197">Indicates whether duplicate detection is enabled.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-198">IsEnabledForCharts</span><span class="sxs-lookup"><span data-stu-id="32653-198">IsEnabledForCharts</span></span></td>
<td><span data-ttu-id="32653-199">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-199">Boolean</span></span></td>
<td><span data-ttu-id="32653-200">Indicates whether charts are enabled.</span><span class="sxs-lookup"><span data-stu-id="32653-200">Indicates whether charts are enabled.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-201">IsImportable</span><span class="sxs-lookup"><span data-stu-id="32653-201">IsImportable</span></span></td>
<td><span data-ttu-id="32653-202">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-202">Boolean</span></span></td>
<td><span data-ttu-id="32653-203">Indicates whether the entity can be imported using the Import Wizard.</span><span class="sxs-lookup"><span data-stu-id="32653-203">Indicates whether the entity can be imported using the Import Wizard.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-204">IsInteractionCentricEnabled</span><span class="sxs-lookup"><span data-stu-id="32653-204">IsInteractionCentricEnabled</span></span></td>
<td><span data-ttu-id="32653-205">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-205">Boolean</span></span></td>
<td><span data-ttu-id="32653-206">Indicates the entity is enabled for interactive experience.</span><span class="sxs-lookup"><span data-stu-id="32653-206">Indicates the entity is enabled for interactive experience.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-207">IsKnowledgeManagementEnabled</span><span class="sxs-lookup"><span data-stu-id="32653-207">IsKnowledgeManagementEnabled</span></span></td>
<td><span data-ttu-id="32653-208">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-208">Boolean</span></span></td>
<td><span data-ttu-id="32653-209">Indicates whether knowledge management is enabled for the entity.</span><span class="sxs-lookup"><span data-stu-id="32653-209">Indicates whether knowledge management is enabled for the entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-210">IsMailMergeEnabled</span><span class="sxs-lookup"><span data-stu-id="32653-210">IsMailMergeEnabled</span></span></td>
<td><span data-ttu-id="32653-211">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-211">Boolean</span></span></td>
<td><span data-ttu-id="32653-212">Indicates whether mail merge is enabled for this entity.</span><span class="sxs-lookup"><span data-stu-id="32653-212">Indicates whether mail merge is enabled for this entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-213">IsManaged</span><span class="sxs-lookup"><span data-stu-id="32653-213">IsManaged</span></span></td>
<td><span data-ttu-id="32653-214">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-214">Boolean</span></span></td>
<td><span data-ttu-id="32653-215">Indicates whether the entity is part of a managed solution.</span><span class="sxs-lookup"><span data-stu-id="32653-215">Indicates whether the entity is part of a managed solution.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-216">IsOneNoteIntegrationEnabled</span><span class="sxs-lookup"><span data-stu-id="32653-216">IsOneNoteIntegrationEnabled</span></span></td>
<td><span data-ttu-id="32653-217">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-217">Boolean</span></span></td>
<td><span data-ttu-id="32653-218">Indicates whether OneNote integration is enabled for the entity.</span><span class="sxs-lookup"><span data-stu-id="32653-218">Indicates whether OneNote integration is enabled for the entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-219">IsOptimisticConcurrencyEnabled</span><span class="sxs-lookup"><span data-stu-id="32653-219">IsOptimisticConcurrencyEnabled</span></span></td>
<td><span data-ttu-id="32653-220">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-220">Boolean</span></span></td>
<td><span data-ttu-id="32653-221">Indicates whether optimistic concurrency is enabled for the entity.</span><span class="sxs-lookup"><span data-stu-id="32653-221">Indicates whether optimistic concurrency is enabled for the entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-222">IsQuickCreateEnabled</span><span class="sxs-lookup"><span data-stu-id="32653-222">IsQuickCreateEnabled</span></span></td>
<td><span data-ttu-id="32653-223">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-223">Boolean</span></span></td>
<td><span data-ttu-id="32653-224">Indicates whether the entity is enabled for quick create forms.</span><span class="sxs-lookup"><span data-stu-id="32653-224">Indicates whether the entity is enabled for quick create forms.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-225">IsStateModelAware</span><span class="sxs-lookup"><span data-stu-id="32653-225">IsStateModelAware</span></span></td>
<td><span data-ttu-id="32653-226">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-226">Boolean</span></span></td>
<td><span data-ttu-id="32653-227">Indicates whether the entity supports setting custom state transitions.</span><span class="sxs-lookup"><span data-stu-id="32653-227">Indicates whether the entity supports setting custom state transitions.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-228">IsValidForAdvancedFind</span><span class="sxs-lookup"><span data-stu-id="32653-228">IsValidForAdvancedFind</span></span></td>
<td><span data-ttu-id="32653-229">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-229">Boolean</span></span></td>
<td><span data-ttu-id="32653-230">Indicates whether the entity is will be shown in Advanced Find.</span><span class="sxs-lookup"><span data-stu-id="32653-230">Indicates whether the entity is will be shown in Advanced Find.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-231">IsVisibleInMobileClient</span><span class="sxs-lookup"><span data-stu-id="32653-231">IsVisibleInMobileClient</span></span></td>
<td><span data-ttu-id="32653-232">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-232">Boolean</span></span></td>
<td><span data-ttu-id="32653-233">Indicates whether Microsoft Dynamics 365 for tablets users can see data for this entity.</span><span class="sxs-lookup"><span data-stu-id="32653-233">Indicates whether Microsoft Dynamics 365 for tablets users can see data for this entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-234">IsEnabledInUnifiedInterface</span><span class="sxs-lookup"><span data-stu-id="32653-234">IsEnabledInUnifiedInterface</span></span></td>
<td><span data-ttu-id="32653-235">Boolean</span><span class="sxs-lookup"><span data-stu-id="32653-235">Boolean</span></span></td>
<td><span data-ttu-id="32653-236">Indicates whether the entity is enabled for Unified Interface.</span><span class="sxs-lookup"><span data-stu-id="32653-236">Indicates whether the entity is enabled for Unified Interface.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-237">LogicalCollectionName</span><span class="sxs-lookup"><span data-stu-id="32653-237">LogicalCollectionName</span></span></td>
<td><span data-ttu-id="32653-238">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="32653-238">String</span></span></td>
<td><span data-ttu-id="32653-239">The logical collection name.</span><span class="sxs-lookup"><span data-stu-id="32653-239">The logical collection name.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-240">Tên logic</span><span class="sxs-lookup"><span data-stu-id="32653-240">LogicalName</span></span></td>
<td><span data-ttu-id="32653-241">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="32653-241">String</span></span></td>
<td><span data-ttu-id="32653-242">The logical name for the entity.</span><span class="sxs-lookup"><span data-stu-id="32653-242">The logical name for the entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-243">ObjectTypeCode</span><span class="sxs-lookup"><span data-stu-id="32653-243">ObjectTypeCode</span></span></td>
<td><span data-ttu-id="32653-244">Số</span><span class="sxs-lookup"><span data-stu-id="32653-244">Number</span></span></td>
<td><span data-ttu-id="32653-245">Mã loại thực thể.</span><span class="sxs-lookup"><span data-stu-id="32653-245">The entity type code.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-246">OwnershipType</span><span class="sxs-lookup"><span data-stu-id="32653-246">OwnershipType</span></span></td>
<td><span data-ttu-id="32653-247">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="32653-247">String</span></span></td>
<td><span data-ttu-id="32653-248">The ownership type for the entity: &quot;UserOwned&quot; or &quot;OrganizationOwned&quot;.</span><span class="sxs-lookup"><span data-stu-id="32653-248">The ownership type for the entity: &quot;UserOwned&quot; or &quot;OrganizationOwned&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-249">PrimaryIdAttribute</span><span class="sxs-lookup"><span data-stu-id="32653-249">PrimaryIdAttribute</span></span></td>
<td><span data-ttu-id="32653-250">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="32653-250">String</span></span></td>
<td><span data-ttu-id="32653-251">The name of the attribute that is the primary id for the entity.</span><span class="sxs-lookup"><span data-stu-id="32653-251">The name of the attribute that is the primary id for the entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-252">PrimaryImageAttribute</span><span class="sxs-lookup"><span data-stu-id="32653-252">PrimaryImageAttribute</span></span></td>
<td><span data-ttu-id="32653-253">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="32653-253">String</span></span></td>
<td><span data-ttu-id="32653-254">The name of the primary image attribute for an entity.</span><span class="sxs-lookup"><span data-stu-id="32653-254">The name of the primary image attribute for an entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-255">PrimaryNameAttribute</span><span class="sxs-lookup"><span data-stu-id="32653-255">PrimaryNameAttribute</span></span></td>
<td><span data-ttu-id="32653-256">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="32653-256">String</span></span></td>
<td><span data-ttu-id="32653-257">The name of the primary attribute for an entity.</span><span class="sxs-lookup"><span data-stu-id="32653-257">The name of the primary attribute for an entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="32653-258">Quyền</span><span class="sxs-lookup"><span data-stu-id="32653-258">Privileges</span></span></td>
<td><span data-ttu-id="32653-259">Array of objects</span><span class="sxs-lookup"><span data-stu-id="32653-259">Array of objects</span></span></td>
<td><span data-ttu-id="32653-260">The privilege metadata for the entity where <em>each</em> object contains the following attributes to define the security privilege for access to an entity:</span><span class="sxs-lookup"><span data-stu-id="32653-260">The privilege metadata for the entity where <em>each</em> object contains the following attributes to define the security privilege for access to an entity:</span></span>
<ul>
<li><span data-ttu-id="32653-261"><b>CanBeBasic</b>: Boolean.</span><span class="sxs-lookup"><span data-stu-id="32653-261"><b>CanBeBasic</b>: Boolean.</span></span> <span data-ttu-id="32653-262">Whether the privilege can be basic access level.</span><span class="sxs-lookup"><span data-stu-id="32653-262">Whether the privilege can be basic access level.</span></span></li>
<li><span data-ttu-id="32653-263"><b>CanBeDeep</b>: Boolean.</span><span class="sxs-lookup"><span data-stu-id="32653-263"><b>CanBeDeep</b>: Boolean.</span></span> <span data-ttu-id="32653-264">Whether the privilege can be deep access level.</span><span class="sxs-lookup"><span data-stu-id="32653-264">Whether the privilege can be deep access level.</span></span></li>
<li><span data-ttu-id="32653-265"><b>CanBeEntityReference</b>: Boolean.</span><span class="sxs-lookup"><span data-stu-id="32653-265"><b>CanBeEntityReference</b>: Boolean.</span></span> <span data-ttu-id="32653-266">Whether the privilege for an external party can be basic access level.</span><span class="sxs-lookup"><span data-stu-id="32653-266">Whether the privilege for an external party can be basic access level.</span></span></li>
<li><span data-ttu-id="32653-267"><b>CanBeGlobal</b>: Boolean.</span><span class="sxs-lookup"><span data-stu-id="32653-267"><b>CanBeGlobal</b>: Boolean.</span></span> <span data-ttu-id="32653-268">Whether the privilege can be global access level.</span><span class="sxs-lookup"><span data-stu-id="32653-268">Whether the privilege can be global access level.</span></span></li>
<li><span data-ttu-id="32653-269"><b>CanBeLocal</b>: Boolean.</span><span class="sxs-lookup"><span data-stu-id="32653-269"><b>CanBeLocal</b>: Boolean.</span></span> <span data-ttu-id="32653-270">Whether the privilege can be local access level.</span><span class="sxs-lookup"><span data-stu-id="32653-270">Whether the privilege can be local access level.</span></span></li>
<li><span data-ttu-id="32653-271"><b>CanBeParentEntityReference</b>: Boolean.</span><span class="sxs-lookup"><span data-stu-id="32653-271"><b>CanBeParentEntityReference</b>: Boolean.</span></span> <span data-ttu-id="32653-272">Whether the privilege for an external party can be parent access level.</span><span class="sxs-lookup"><span data-stu-id="32653-272">Whether the privilege for an external party can be parent access level.</span></span></li>
<li><span data-ttu-id="32653-273"><b>Name</b>: String.</span><span class="sxs-lookup"><span data-stu-id="32653-273"><b>Name</b>: String.</span></span> <span data-ttu-id="32653-274">The name of the privilege.</span><span class="sxs-lookup"><span data-stu-id="32653-274">The name of the privilege.</span></span></li>
<li><span data-ttu-id="32653-275"><b>PrivilegeId</b>: String.</span><span class="sxs-lookup"><span data-stu-id="32653-275"><b>PrivilegeId</b>: String.</span></span> <span data-ttu-id="32653-276">The ID of the privilege.</span><span class="sxs-lookup"><span data-stu-id="32653-276">The ID of the privilege.</span></span></li>
<li><span data-ttu-id="32653-277"><b>PrivilegeType</b>: Number.</span><span class="sxs-lookup"><span data-stu-id="32653-277"><b>PrivilegeType</b>: Number.</span></span> <span data-ttu-id="32653-278">The type of privilege, which is one of the following:</span><span class="sxs-lookup"><span data-stu-id="32653-278">The type of privilege, which is one of the following:</span></span></li>
<ul>
<li><span data-ttu-id="32653-279">0: None</span><span class="sxs-lookup"><span data-stu-id="32653-279">0: None</span></span></li>
<li><span data-ttu-id="32653-280">1: Create</span><span class="sxs-lookup"><span data-stu-id="32653-280">1: Create</span></span></li>
<li><span data-ttu-id="32653-281">2: Read</span><span class="sxs-lookup"><span data-stu-id="32653-281">2: Read</span></span></li>
<li><span data-ttu-id="32653-282">3: Write</span><span class="sxs-lookup"><span data-stu-id="32653-282">3: Write</span></span></li>
<li><span data-ttu-id="32653-283">4: Delete</span><span class="sxs-lookup"><span data-stu-id="32653-283">4: Delete</span></span></li>
<li><span data-ttu-id="32653-284">5: Assign</span><span class="sxs-lookup"><span data-stu-id="32653-284">5: Assign</span></span></li>
<li><span data-ttu-id="32653-285">6: Share</span><span class="sxs-lookup"><span data-stu-id="32653-285">6: Share</span></span></li>
<li><span data-ttu-id="32653-286">7: Append</span><span class="sxs-lookup"><span data-stu-id="32653-286">7: Append</span></span></li>
<li><span data-ttu-id="32653-287">8: AppendTo</span><span class="sxs-lookup"><span data-stu-id="32653-287">8: AppendTo</span></span></li>
</ul>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="32653-288">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="32653-288">Attributes</span></span></td>
<td><span data-ttu-id="32653-289">Thu thập</span><span class="sxs-lookup"><span data-stu-id="32653-289">Collection</span></span></td>
<td><span data-ttu-id="32653-290">A collection of attribute metadata objects.</span><span class="sxs-lookup"><span data-stu-id="32653-290">A collection of attribute metadata objects.</span></span> <span data-ttu-id="32653-291">The object returned depends on the type of attribute metadata.</span><span class="sxs-lookup"><span data-stu-id="32653-291">The object returned depends on the type of attribute metadata.</span></span>
<p><span data-ttu-id="32653-292"><b>Attribute metadata for the <i>base</i> type</b></span><span class="sxs-lookup"><span data-stu-id="32653-292"><b>Attribute metadata for the <i>base</i> type</b></span></span><br/>
<span data-ttu-id="32653-293">An object returned with the following properties:</span><span class="sxs-lookup"><span data-stu-id="32653-293">An object returned with the following properties:</span></span></p>
<ul>
<li><span data-ttu-id="32653-294"><b>AttributeType</b>: Number.</span><span class="sxs-lookup"><span data-stu-id="32653-294"><b>AttributeType</b>: Number.</span></span> <span data-ttu-id="32653-295">Type of an attribute.</span><span class="sxs-lookup"><span data-stu-id="32653-295">Type of an attribute.</span></span> <span data-ttu-id="32653-296">For a list of attribute type values, see <a href="https://docs.microsoft.com/dotnet/api/microsoft.xrm.sdk.metadata.attributetypecode">AttributeTypeCode</a></span><span class="sxs-lookup"><span data-stu-id="32653-296">For a list of attribute type values, see <a href="https://docs.microsoft.com/dotnet/api/microsoft.xrm.sdk.metadata.attributetypecode">AttributeTypeCode</a></span></span></li>
<li><span data-ttu-id="32653-297"><b>DisplayName</b>: String.</span><span class="sxs-lookup"><span data-stu-id="32653-297"><b>DisplayName</b>: String.</span></span> <span data-ttu-id="32653-298">Display name for the attribute.</span><span class="sxs-lookup"><span data-stu-id="32653-298">Display name for the attribute.</span></span></li>
<li><span data-ttu-id="32653-299"><b>EntityLogicalName</b>: String.</span><span class="sxs-lookup"><span data-stu-id="32653-299"><b>EntityLogicalName</b>: String.</span></span> <span data-ttu-id="32653-300">Logical name of the entity that contains the attribute.</span><span class="sxs-lookup"><span data-stu-id="32653-300">Logical name of the entity that contains the attribute.</span></span></li>
<li><span data-ttu-id="32653-301"><b>LogicalName</b>: String.</span><span class="sxs-lookup"><span data-stu-id="32653-301"><b>LogicalName</b>: String.</span></span> <span data-ttu-id="32653-302">Logical name for the attribute.</span><span class="sxs-lookup"><span data-stu-id="32653-302">Logical name for the attribute.</span></span></li></ul>

<p><span data-ttu-id="32653-303"><b>Attribute metadata for the <i>boolean</i> type</b></span><span class="sxs-lookup"><span data-stu-id="32653-303"><b>Attribute metadata for the <i>boolean</i> type</b></span></span><br/>
<span data-ttu-id="32653-304">An object returned with the following properties in addition to the <i>base</i> attribute metadata type properties:</span><span class="sxs-lookup"><span data-stu-id="32653-304">An object returned with the following properties in addition to the <i>base</i> attribute metadata type properties:</span></span></p>
<ul>
<li><span data-ttu-id="32653-305"><b>DefaultFormValue</b>: Boolean.</span><span class="sxs-lookup"><span data-stu-id="32653-305"><b>DefaultFormValue</b>: Boolean.</span></span> <span data-ttu-id="32653-306">Default value for a Boolean option set.</span><span class="sxs-lookup"><span data-stu-id="32653-306">Default value for a Boolean option set.</span></span></li>
<li><span data-ttu-id="32653-307"><b>OptionSet</b>: Object.</span><span class="sxs-lookup"><span data-stu-id="32653-307"><b>OptionSet</b>: Object.</span></span> <span data-ttu-id="32653-308">Options for the boolean attribute where each option is a key:value pair.</span><span class="sxs-lookup"><span data-stu-id="32653-308">Options for the boolean attribute where each option is a key:value pair.</span></span></li></ul>

<p><span data-ttu-id="32653-309"><b>Attribute metadata for the <i>enum</i> type</b></span><span class="sxs-lookup"><span data-stu-id="32653-309"><b>Attribute metadata for the <i>enum</i> type</b></span></span><br/>
<span data-ttu-id="32653-310">An object returned with the following properties in addition to the <i>base</i> attribute metadata type properties:</span><span class="sxs-lookup"><span data-stu-id="32653-310">An object returned with the following properties in addition to the <i>base</i> attribute metadata type properties:</span></span></p>
<ul>
<li><span data-ttu-id="32653-311"><b>OptionSet</b>: Object.</span><span class="sxs-lookup"><span data-stu-id="32653-311"><b>OptionSet</b>: Object.</span></span> <span data-ttu-id="32653-312">Options for the attribute where each option is a key:value pair.</span><span class="sxs-lookup"><span data-stu-id="32653-312">Options for the attribute where each option is a key:value pair.</span></span></li></ul>

<p><span data-ttu-id="32653-313"><b>Attribute metadata for the <i>picklist</i> type</b></span><span class="sxs-lookup"><span data-stu-id="32653-313"><b>Attribute metadata for the <i>picklist</i> type</b></span></span><br/>
<span data-ttu-id="32653-314">An object returned with the following properties in addition to the <i>base</i> attribute metadata type properties:</span><span class="sxs-lookup"><span data-stu-id="32653-314">An object returned with the following properties in addition to the <i>base</i> attribute metadata type properties:</span></span></p>
<ul>
<li><span data-ttu-id="32653-315"><b>DefaultFormValue</b>: Number.</span><span class="sxs-lookup"><span data-stu-id="32653-315"><b>DefaultFormValue</b>: Number.</span></span> <span data-ttu-id="32653-316">Default form value for the attribute.</span><span class="sxs-lookup"><span data-stu-id="32653-316">Default form value for the attribute.</span></span></li>
<li><span data-ttu-id="32653-317"><b>OptionSet</b>: Object.</span><span class="sxs-lookup"><span data-stu-id="32653-317"><b>OptionSet</b>: Object.</span></span> <span data-ttu-id="32653-318">Options for the attribute where each option is a key:value pair.</span><span class="sxs-lookup"><span data-stu-id="32653-318">Options for the attribute where each option is a key:value pair.</span></span></li></ul>

<p><span data-ttu-id="32653-319"><b>Attribute metadata for the <i>state</i> type</b></span><span class="sxs-lookup"><span data-stu-id="32653-319"><b>Attribute metadata for the <i>state</i> type</b></span></span><br/>
<span data-ttu-id="32653-320">An object returned with the following properties in addition to the <i>base</i> attribute metadata type properties:</span><span class="sxs-lookup"><span data-stu-id="32653-320">An object returned with the following properties in addition to the <i>base</i> attribute metadata type properties:</span></span></p>
<ul>
<li><span data-ttu-id="32653-321"><b>OptionSet</b>: Object.</span><span class="sxs-lookup"><span data-stu-id="32653-321"><b>OptionSet</b>: Object.</span></span> <span data-ttu-id="32653-322">Options for the attribute where each option is a key:value pair.</span><span class="sxs-lookup"><span data-stu-id="32653-322">Options for the attribute where each option is a key:value pair.</span></span></li></ul>
<p><span data-ttu-id="32653-323">The object also contains the following methods:</span><span class="sxs-lookup"><span data-stu-id="32653-323">The object also contains the following methods:</span></span></p>
<ul>
<li><span data-ttu-id="32653-324"><b>getDefaultStatus(arg)</b>: Returns the default status (number) based on the passed in state value for an entity.</span><span class="sxs-lookup"><span data-stu-id="32653-324"><b>getDefaultStatus(arg)</b>: Returns the default status (number) based on the passed in state value for an entity.</span></span> <span data-ttu-id="32653-325">For default state and status values for an entity, see entity metadata information of the entity in <a href="https://docs.microsoft.com/powerapps/developer/common-data-service/reference/about-entity-reference">entity reference</a>.</span><span class="sxs-lookup"><span data-stu-id="32653-325">For default state and status values for an entity, see entity metadata information of the entity in <a href="https://docs.microsoft.com/powerapps/developer/common-data-service/reference/about-entity-reference">entity reference</a>.</span></span></li>
<li><span data-ttu-id="32653-326"><b>getStatusValuesForState(arg)</b>: Returns possible status values (array of numbers) for a specified state value.</span><span class="sxs-lookup"><span data-stu-id="32653-326"><b>getStatusValuesForState(arg)</b>: Returns possible status values (array of numbers) for a specified state value.</span></span> <span data-ttu-id="32653-327">For state and status values for an entity, see entity metadata information of the entity in <a href="https://docs.microsoft.com/powerapps/developer/common-data-service/reference/about-entity-reference">entity reference</a>.</span><span class="sxs-lookup"><span data-stu-id="32653-327">For state and status values for an entity, see entity metadata information of the entity in <a href="https://docs.microsoft.com/powerapps/developer/common-data-service/reference/about-entity-reference">entity reference</a>.</span></span></li></ul>

<p><span data-ttu-id="32653-328"><b>Attribute metadata for the <i>status</i> type</b></span><span class="sxs-lookup"><span data-stu-id="32653-328"><b>Attribute metadata for the <i>status</i> type</b></span></span><br/>
<span data-ttu-id="32653-329">An object returned with the following properties in addition to the <i>base</i> attribute metadata type properties:</span><span class="sxs-lookup"><span data-stu-id="32653-329">An object returned with the following properties in addition to the <i>base</i> attribute metadata type properties:</span></span></p>
<ul>
<li><span data-ttu-id="32653-330"><b>OptionSet</b>: Object.</span><span class="sxs-lookup"><span data-stu-id="32653-330"><b>OptionSet</b>: Object.</span></span> <span data-ttu-id="32653-331">Options for the attribute where each option is a key:value pair.</span><span class="sxs-lookup"><span data-stu-id="32653-331">Options for the attribute where each option is a key:value pair.</span></span></li></ul>
<p><span data-ttu-id="32653-332">The object also contains the following method:</span><span class="sxs-lookup"><span data-stu-id="32653-332">The object also contains the following method:</span></span></p>
<ul>
<li><span data-ttu-id="32653-333"><b>getState(arg)</b>: Returns the state value (number) for the specified status value (number).</span><span class="sxs-lookup"><span data-stu-id="32653-333"><b>getState(arg)</b>: Returns the state value (number) for the specified status value (number).</span></span> <span data-ttu-id="32653-334">For default state and status values for an entity, see entity metadata information of the entity in <a href="https://docs.microsoft.com/powerapps/developer/common-data-service/reference/about-entity-reference">entity reference</a>.</span><span class="sxs-lookup"><span data-stu-id="32653-334">For default state and status values for an entity, see entity metadata information of the entity in <a href="https://docs.microsoft.com/powerapps/developer/common-data-service/reference/about-entity-reference">entity reference</a>.</span></span></li>
</ul>
</td>
</tr>
</table>

### <a name="related-topics"></a><span data-ttu-id="32653-335">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="32653-335">Related topics</span></span>

[<span data-ttu-id="32653-336">Xrm.Utility</span><span class="sxs-lookup"><span data-stu-id="32653-336">Xrm.Utility</span></span>](../xrm-utility.md)

