---
title: Run bulk delete (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Delete data in bulk by submitting an asynchronous bulk delete job via the BulkDeleteRequest message.
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
- running bulk delete, submitting a bulk delete job by using the BulkDeleteRequest message
- running bulk delete, using query expressions to describe the records to delete
- using query expressions to describe the records to delete
- bulk deletion operation entity, running bulk delete
- BulkDeleteRequest message, see 'deleting data in bulk in Microsoft Dynamics CRM'
- running bulk delete, running asynchronously without blocking other activities
- bulk delete operation records, items returned in
- submitting a bulk delete job by using the BulkDeleteRequest message, see 'deleting data in bulk in Microsoft Dynamics CRM'
- running bulk delete, required privileges
- running bulk delete, supported entities
- running bulk delete, bulk deletion operation entity
ms.assetid: e4ea7edd-d1f2-4fca-bb80-bebf0a910643
caps.latest.revision: 30
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3a49945459741e7a7e67edd9924aac7cca321210
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388515"
---
# <a name="run-bulk-delete"></a><span data-ttu-id="91a26-103">Run bulk delete</span><span class="sxs-lookup"><span data-stu-id="91a26-103">Run bulk delete</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="91a26-104">To delete data in bulk, you have to submit a bulk delete job by using the <xref:Microsoft.Crm.Sdk.Messages.BulkDeleteRequest> message.</span><span class="sxs-lookup"><span data-stu-id="91a26-104">To delete data in bulk, you have to submit a bulk delete job by using the <xref:Microsoft.Crm.Sdk.Messages.BulkDeleteRequest> message.</span></span> <span data-ttu-id="91a26-105">The bulk delete job runs asynchronously in the background without blocking other activities.</span><span class="sxs-lookup"><span data-stu-id="91a26-105">The bulk delete job runs asynchronously in the background without blocking other activities.</span></span> <span data-ttu-id="91a26-106">The query expressions that describe the records on which to run the bulk delete job are specified in the <xref:Microsoft.Crm.Sdk.Messages.BulkDeleteRequest.QuerySet> property of this request.</span><span class="sxs-lookup"><span data-stu-id="91a26-106">The query expressions that describe the records on which to run the bulk delete job are specified in the <xref:Microsoft.Crm.Sdk.Messages.BulkDeleteRequest.QuerySet> property of this request.</span></span>  
  
 <span data-ttu-id="91a26-107">A bulk delete job is represented by the bulk delete operation entity.</span><span class="sxs-lookup"><span data-stu-id="91a26-107">A bulk delete job is represented by the bulk delete operation entity.</span></span> <span data-ttu-id="91a26-108">The schema name for this entity is `BulkDeleteOperation`.</span><span class="sxs-lookup"><span data-stu-id="91a26-108">The schema name for this entity is `BulkDeleteOperation`.</span></span> <span data-ttu-id="91a26-109">A bulk delete operation record includes the following information:</span><span class="sxs-lookup"><span data-stu-id="91a26-109">A bulk delete operation record includes the following information:</span></span>  
  
- <span data-ttu-id="91a26-110">Number of records that the bulk delete job deleted.</span><span class="sxs-lookup"><span data-stu-id="91a26-110">Number of records that the bulk delete job deleted.</span></span>  
  
- <span data-ttu-id="91a26-111">Number of records that the bulk delete job failed to delete.</span><span class="sxs-lookup"><span data-stu-id="91a26-111">Number of records that the bulk delete job failed to delete.</span></span>  
  
- <span data-ttu-id="91a26-112">Whether the bulk delete job is a recurring job or not.</span><span class="sxs-lookup"><span data-stu-id="91a26-112">Whether the bulk delete job is a recurring job or not.</span></span>  
  
- <span data-ttu-id="91a26-113">Start time of the bulk delete job.</span><span class="sxs-lookup"><span data-stu-id="91a26-113">Start time of the bulk delete job.</span></span>  
  
  <span data-ttu-id="91a26-114">A bulk delete job only deletes records that are created before the job starts to run.</span><span class="sxs-lookup"><span data-stu-id="91a26-114">A bulk delete job only deletes records that are created before the job starts to run.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="91a26-115">If a bulk delete job fails or ends prematurely, any records that were deleted before the failure or ending of the job are not rolled back and remain deleted.</span><span class="sxs-lookup"><span data-stu-id="91a26-115">If a bulk delete job fails or ends prematurely, any records that were deleted before the failure or ending of the job are not rolled back and remain deleted.</span></span> <span data-ttu-id="91a26-116">The failures of the `BulkDeleteOperation` are stored in the `BulkDeleteFailure` records and can be retrieved by using the          <xref:Microsoft.Xrm.Sdk.Messages.RetrieveRequest> message or the  <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest> message.</span><span class="sxs-lookup"><span data-stu-id="91a26-116">The failures of the `BulkDeleteOperation` are stored in the `BulkDeleteFailure` records and can be retrieved by using the          <xref:Microsoft.Xrm.Sdk.Messages.RetrieveRequest> message or the  <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest> message.</span></span>  
  
 <span data-ttu-id="91a26-117">A bulk delete job deletes the specified records according to the cascading rules.</span><span class="sxs-lookup"><span data-stu-id="91a26-117">A bulk delete job deletes the specified records according to the cascading rules.</span></span> <span data-ttu-id="91a26-118">These rules are based on the relationship type between the entities.</span><span class="sxs-lookup"><span data-stu-id="91a26-118">These rules are based on the relationship type between the entities.</span></span> <span data-ttu-id="91a26-119">For more information, see [Entity Relationship Behavior](entity-relationship-behavior.md).</span><span class="sxs-lookup"><span data-stu-id="91a26-119">For more information, see [Entity Relationship Behavior](entity-relationship-behavior.md).</span></span>  
  
 <span data-ttu-id="91a26-120">To run a bulk delete job, a user must have the `BulkDelete` and `Delete` privileges for the entity types being deleted.</span><span class="sxs-lookup"><span data-stu-id="91a26-120">To run a bulk delete job, a user must have the `BulkDelete` and `Delete` privileges for the entity types being deleted.</span></span> <span data-ttu-id="91a26-121">The user must also have read permissions to the entity records that are specified in the <xref:Microsoft.Crm.Sdk.Messages.BulkDeleteRequest> message.</span><span class="sxs-lookup"><span data-stu-id="91a26-121">The user must also have read permissions to the entity records that are specified in the <xref:Microsoft.Crm.Sdk.Messages.BulkDeleteRequest> message.</span></span> <span data-ttu-id="91a26-122">By default, a system administrator has the necessary permissions; however, other users must be granted these permissions.</span><span class="sxs-lookup"><span data-stu-id="91a26-122">By default, a system administrator has the necessary permissions; however, other users must be granted these permissions.</span></span>  
  
 <span data-ttu-id="91a26-123">You can perform a bulk deletion on all entities that are supported by the delete action.</span><span class="sxs-lookup"><span data-stu-id="91a26-123">You can perform a bulk deletion on all entities that are supported by the delete action.</span></span> <span data-ttu-id="91a26-124">For information about possible actions on entity records, see [Actions on Entity Records](introduction-entities.md#ActionsOnEntityRecords).</span><span class="sxs-lookup"><span data-stu-id="91a26-124">For information about possible actions on entity records, see [Actions on Entity Records](introduction-entities.md#ActionsOnEntityRecords).</span></span>  
  
 <span data-ttu-id="91a26-125">If a plug-in or a workflow (process) is triggered by the delete action on a specific entity type, it is triggered every time that an entity record of this type is deleted by the bulk delete job.</span><span class="sxs-lookup"><span data-stu-id="91a26-125">If a plug-in or a workflow (process) is triggered by the delete action on a specific entity type, it is triggered every time that an entity record of this type is deleted by the bulk delete job.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="91a26-126">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="91a26-126">See also</span></span>

 <span data-ttu-id="91a26-127">[Delete Data in Bulk in Dynamics 365 for Customer Engagement apps](delete-data-bulk.md) </span><span class="sxs-lookup"><span data-stu-id="91a26-127">[Delete Data in Bulk in Dynamics 365 for Customer Engagement apps](delete-data-bulk.md) </span></span>  
 <span data-ttu-id="91a26-128">[Data Management in Dynamics 365 for Customer Engagement apps (Auditing, Duplicate Detection, Bulk Delete, Data Import)](manage-data.md)  </span><span class="sxs-lookup"><span data-stu-id="91a26-128">[Data Management in Dynamics 365 for Customer Engagement apps (Auditing, Duplicate Detection, Bulk Delete, Data Import)](manage-data.md)  </span></span>  
 <span data-ttu-id="91a26-129">[Entity Relationship Behavior](entity-relationship-behavior.md) </span><span class="sxs-lookup"><span data-stu-id="91a26-129">[Entity Relationship Behavior](entity-relationship-behavior.md) </span></span>  
 <span data-ttu-id="91a26-130">[Recurrence Pattern in Asynchronous Job Execution](recurrence-pattern-asynchronous-job-execution.md) </span><span class="sxs-lookup"><span data-stu-id="91a26-130">[Recurrence Pattern in Asynchronous Job Execution](recurrence-pattern-asynchronous-job-execution.md) </span></span>  
 <span data-ttu-id="91a26-131">[Sample: Bulk Delete Exported Records](sample-bulk-delete-exported-records.md) </span><span class="sxs-lookup"><span data-stu-id="91a26-131">[Sample: Bulk Delete Exported Records](sample-bulk-delete-exported-records.md) </span></span>  
 <span data-ttu-id="91a26-132">[Sample: Bulk Delete Records That Match Common Criteria](sample-bulk-delete-records-match-common-criteria.md) </span><span class="sxs-lookup"><span data-stu-id="91a26-132">[Sample: Bulk Delete Records That Match Common Criteria](sample-bulk-delete-records-match-common-criteria.md) </span></span>  
 [<span data-ttu-id="91a26-133">BulkDeleteOperation Entity</span><span class="sxs-lookup"><span data-stu-id="91a26-133">BulkDeleteOperation Entity</span></span>](entities/bulkdeleteoperation.md)
