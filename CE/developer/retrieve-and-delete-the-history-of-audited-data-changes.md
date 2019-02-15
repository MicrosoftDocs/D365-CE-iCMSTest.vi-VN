---
title: Retrieve and delete the history of audited data changes (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Programmatically retrieve the audit change history or delete audit records.
ms.custom: ''
ms.date: 03/20/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- retrieving and deleting changed-data history (audit history), new partitions created quarterly
- partitions created quarterly for auditing, used by Microsoft Dynamics 365 and SQL Server with auditing
- retrieving and deleting changed-data history (audit history), obtaining a list of partitions
- obtaining changed-data history
- audit records and history, retrieving and deleting data for
- deleting audit records, using Microsoft Dynamics 365 and SQL Server with auditing
- changed-data history, obtaining
- deleting change history (audit records), how to
ms.assetid: 53b9a1ac-f9c0-490f-a42f-2efc231b67ff
caps.latest.revision: 20
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bd191f4a8debc0642ebd0b35529e5d252cdbb658
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385593"
---
# <a name="retrieve-and-delete-the-history-of-audited-data-changes"></a><span data-ttu-id="04c72-103">Retrieve and delete the history of audited data changes</span><span class="sxs-lookup"><span data-stu-id="04c72-103">Retrieve and delete the history of audited data changes</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="04c72-104">After auditing is enabled and data changes are made to those entities and attributes being audited, you can proceed to obtain the data change history.</span><span class="sxs-lookup"><span data-stu-id="04c72-104">After auditing is enabled and data changes are made to those entities and attributes being audited, you can proceed to obtain the data change history.</span></span> <span data-ttu-id="04c72-105">Optionally, you can delete the audit records after you review the change history.</span><span class="sxs-lookup"><span data-stu-id="04c72-105">Optionally, you can delete the audit records after you review the change history.</span></span> <span data-ttu-id="04c72-106">Follow the sample code link at the end of this topic for more information.</span><span class="sxs-lookup"><span data-stu-id="04c72-106">Follow the sample code link at the end of this topic for more information.</span></span>  
  
## <a name="retrieve-the-change-history"></a><span data-ttu-id="04c72-107">Retrieve the change history</span><span class="sxs-lookup"><span data-stu-id="04c72-107">Retrieve the change history</span></span> 
 
 <span data-ttu-id="04c72-108">There are several messages requests that can be used to retrieve the audit change history.</span><span class="sxs-lookup"><span data-stu-id="04c72-108">There are several messages requests that can be used to retrieve the audit change history.</span></span> <span data-ttu-id="04c72-109">These requests are differentiated by the nature of what they retrieve.</span><span class="sxs-lookup"><span data-stu-id="04c72-109">These requests are differentiated by the nature of what they retrieve.</span></span> 
<!-- Bug 696490 should make the Audit entity public again: Refer to the topic  [Audit Entity](entities/audit.md) for a list of message requests related to auditing. -->
<span data-ttu-id="04c72-110">Refer to the sample link at the end of this topic for sample code that demonstrates some of these change history message requests.</span><span class="sxs-lookup"><span data-stu-id="04c72-110">Refer to the sample link at the end of this topic for sample code that demonstrates some of these change history message requests.</span></span>

## <a name="delete-the-change-history-for-a-record"></a><span data-ttu-id="04c72-111">Delete the change history for a record</span><span class="sxs-lookup"><span data-stu-id="04c72-111">Delete the change history for a record</span></span>
 
 <span data-ttu-id="04c72-112">Use the <xref:Microsoft.Crm.Sdk.Messages.DeleteRecordChangeHistoryRequest> message to delete all the audit change history records for a particular record.</span><span class="sxs-lookup"><span data-stu-id="04c72-112">Use the <xref:Microsoft.Crm.Sdk.Messages.DeleteRecordChangeHistoryRequest> message to delete all the audit change history records for a particular record.</span></span> <span data-ttu-id="04c72-113">This lets you delete the audit change history for a record instead of deleting all the audit records for a date range, which is covered in the next section.</span><span class="sxs-lookup"><span data-stu-id="04c72-113">This lets you delete the audit change history for a record instead of deleting all the audit records for a date range, which is covered in the next section.</span></span> <span data-ttu-id="04c72-114">To delete the audit change history for a record, you must have a security role with the **prvDeleteRecordChangeHistory** privilege or be a System Administrator.</span><span class="sxs-lookup"><span data-stu-id="04c72-114">To delete the audit change history for a record, you must have a security role with the **prvDeleteRecordChangeHistory** privilege or be a System Administrator.</span></span>

## <a name="delete-the-change-history-for-a-date-range"></a><span data-ttu-id="04c72-115">Delete the change history for a date range</span><span class="sxs-lookup"><span data-stu-id="04c72-115">Delete the change history for a date range</span></span>

 <span data-ttu-id="04c72-116">You can delete `audit` records for a date range using the <xref:Microsoft.Crm.Sdk.Messages.DeleteAuditDataRequest> request.</span><span class="sxs-lookup"><span data-stu-id="04c72-116">You can delete `audit` records for a date range using the <xref:Microsoft.Crm.Sdk.Messages.DeleteAuditDataRequest> request.</span></span> <span data-ttu-id="04c72-117">Audit data records are deleted sequentially from the oldest to the newest.</span><span class="sxs-lookup"><span data-stu-id="04c72-117">Audit data records are deleted sequentially from the oldest to the newest.</span></span> <span data-ttu-id="04c72-118">The functionality of this request is slightly different based on the edition of [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] being used by your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] server.</span><span class="sxs-lookup"><span data-stu-id="04c72-118">The functionality of this request is slightly different based on the edition of [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] being used by your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] server.</span></span> [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] <span data-ttu-id="04c72-119">uses an enterprise edition of [!INCLUDE[pn_SQL_Server_short](../includes/pn-sql-server-short.md)].</span><span class="sxs-lookup"><span data-stu-id="04c72-119">uses an enterprise edition of [!INCLUDE[pn_SQL_Server_short](../includes/pn-sql-server-short.md)].</span></span>

 <span data-ttu-id="04c72-120">If your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] server uses [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] standard edition, which does not support the database partitioning feature, the <xref:Microsoft.Crm.Sdk.Messages.DeleteAuditDataRequest> request deletes all audit records created up to the end date specified in the <xref:Microsoft.Crm.Sdk.Messages.DeleteAuditDataRequest.EndDate> property.</span><span class="sxs-lookup"><span data-stu-id="04c72-120">If your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] server uses [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] standard edition, which does not support the database partitioning feature, the <xref:Microsoft.Crm.Sdk.Messages.DeleteAuditDataRequest> request deletes all audit records created up to the end date specified in the <xref:Microsoft.Crm.Sdk.Messages.DeleteAuditDataRequest.EndDate> property.</span></span>

 <span data-ttu-id="04c72-121">If your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] server uses an Enterprise edition of [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] that does support partitioning, the <xref:Microsoft.Crm.Sdk.Messages.DeleteAuditDataRequest> request will delete all audit data in those partitions where the end date is before the date specified in the <xref:Microsoft.Crm.Sdk.Messages.DeleteAuditDataRequest.EndDate> property.</span><span class="sxs-lookup"><span data-stu-id="04c72-121">If your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] server uses an Enterprise edition of [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] that does support partitioning, the <xref:Microsoft.Crm.Sdk.Messages.DeleteAuditDataRequest> request will delete all audit data in those partitions where the end date is before the date specified in the <xref:Microsoft.Crm.Sdk.Messages.DeleteAuditDataRequest.EndDate> property.</span></span> <span data-ttu-id="04c72-122">Any empty partitions are also deleted.</span><span class="sxs-lookup"><span data-stu-id="04c72-122">Any empty partitions are also deleted.</span></span> <span data-ttu-id="04c72-123">However, neither the current (active) partition nor the `audit` records in that active partition can be deleted by using this request or any other request.</span><span class="sxs-lookup"><span data-stu-id="04c72-123">However, neither the current (active) partition nor the `audit` records in that active partition can be deleted by using this request or any other request.</span></span>

 <span data-ttu-id="04c72-124">New partitions are automatically created by the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] platform on a quarterly basis each year.</span><span class="sxs-lookup"><span data-stu-id="04c72-124">New partitions are automatically created by the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] platform on a quarterly basis each year.</span></span> <span data-ttu-id="04c72-125">This functionality is non-configurable and cannot be changed.</span><span class="sxs-lookup"><span data-stu-id="04c72-125">This functionality is non-configurable and cannot be changed.</span></span> <span data-ttu-id="04c72-126">You can obtain the list of partitions using the <xref:Microsoft.Crm.Sdk.Messages.RetrieveAuditPartitionListRequest> request.</span><span class="sxs-lookup"><span data-stu-id="04c72-126">You can obtain the list of partitions using the <xref:Microsoft.Crm.Sdk.Messages.RetrieveAuditPartitionListRequest> request.</span></span> <span data-ttu-id="04c72-127">If the end date of any partition is later than the current date, you cannot delete that partition or any `audit` records in it.</span><span class="sxs-lookup"><span data-stu-id="04c72-127">If the end date of any partition is later than the current date, you cannot delete that partition or any `audit` records in it.</span></span>  

### <a name="see-also"></a><span data-ttu-id="04c72-128">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="04c72-128">See also</span></span>

 [<span data-ttu-id="04c72-129">Data Management in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="04c72-129">Data Management in Dynamics 365 for Customer Engagement apps</span></span>](manage-data.md)<br />
 [<span data-ttu-id="04c72-130">Audit entity data changes</span><span class="sxs-lookup"><span data-stu-id="04c72-130">Audit entity data changes</span></span>](audit-entity-data-changes.md)<br />
 [<span data-ttu-id="04c72-131">Kiểm tra truy cập người dùng</span><span class="sxs-lookup"><span data-stu-id="04c72-131">Audit user access</span></span>](audit-user-access.md) <br />
 [<span data-ttu-id="04c72-132">Sample: Audit Entity Data Changes</span><span class="sxs-lookup"><span data-stu-id="04c72-132">Sample: Audit Entity Data Changes</span></span>](sample-audit-entity-data-changes.md)<br />
<!-- Bug 696490 should make the Audit entity public again: [Audit Entity](entities/audit.md)<br /> -->
 [<span data-ttu-id="04c72-133">Auditing Entity Data Changes in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="04c72-133">Auditing Entity Data Changes in Dynamics 365 for Customer Engagement apps</span></span>](audit-entity-data-changes.md)<br />
