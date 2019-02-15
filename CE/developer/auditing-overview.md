---
title: Auditing overview (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Overview of the audit capabilities, supported on all custom and most customizable entities and attributes, but not supported on metadata changes, retrieve operations, export operations, or during authentication.
ms.custom: ''
ms.date: 03/06/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: c3e00bf9-d973-4cf6-9527-1c12cef8a949
caps.latest.revision: 36
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5a5fc850977bbb0a01e3382c07a4918458d5e416
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386272"
---
# <a name="auditing-overview"></a><span data-ttu-id="dfbfa-103">Tổng quan về kiểm tra</span><span class="sxs-lookup"><span data-stu-id="dfbfa-103">Auditing overview</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="dfbfa-104">Các tổ chức thường cần phải tuân thủ nhiều quy định khác nhau để đảm bảo tính khả dụng của lịch sử tương tác khách hàng, nhật ký kiểm tra, báo cáo truy cập và các báo cáo theo dõi sự cố bảo mật.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-104">Organizations often need to be in compliance with various regulations to ensure availability of customer interaction history, audit logs, access reports, and security incident tracking reports.</span></span> <span data-ttu-id="dfbfa-105">Organizations may want to track changes in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps data for security and analytical purpose.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-105">Organizations may want to track changes in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps data for security and analytical purpose.</span></span>  
  
 [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="dfbfa-106">apps support an auditing capability where entity and attribute data changes within an organization can be recorded over time for use in analysis and reporting purposes.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-106">apps support an auditing capability where entity and attribute data changes within an organization can be recorded over time for use in analysis and reporting purposes.</span></span> <span data-ttu-id="dfbfa-107">Auditing is supported on all custom and most customizable entities and attributes.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-107">Auditing is supported on all custom and most customizable entities and attributes.</span></span> <span data-ttu-id="dfbfa-108">Auditing is not supported on metadata changes, retrieve operations, export operations, or during authentication.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-108">Auditing is not supported on metadata changes, retrieve operations, export operations, or during authentication.</span></span> <span data-ttu-id="dfbfa-109">For information on how to configure auditing, see [Configure Entities and Attributes for Auditing](configure-entities-attributes-auditing.md).</span><span class="sxs-lookup"><span data-stu-id="dfbfa-109">For information on how to configure auditing, see [Configure Entities and Attributes for Auditing](configure-entities-attributes-auditing.md).</span></span>  
  
## <a name="supported-for-auditing"></a><span data-ttu-id="dfbfa-110">Supported for auditing</span><span class="sxs-lookup"><span data-stu-id="dfbfa-110">Supported for auditing</span></span>  
 <span data-ttu-id="dfbfa-111">The following lists auditing capabilities for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps:</span><span class="sxs-lookup"><span data-stu-id="dfbfa-111">The following lists auditing capabilities for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps:</span></span>  
<!-- TODO: Jim, I don't think this is online only. Please correct the tokens here. -->
  
* <span data-ttu-id="dfbfa-112">Audit of customizable entities</span><span class="sxs-lookup"><span data-stu-id="dfbfa-112">Audit of customizable entities</span></span>
* <span data-ttu-id="dfbfa-113">Audit of custom entities</span><span class="sxs-lookup"><span data-stu-id="dfbfa-113">Audit of custom entities</span></span>
* <span data-ttu-id="dfbfa-114">Configure entities for audit</span><span class="sxs-lookup"><span data-stu-id="dfbfa-114">Configure entities for audit</span></span>
* <span data-ttu-id="dfbfa-115">Configure attributes for audit</span><span class="sxs-lookup"><span data-stu-id="dfbfa-115">Configure attributes for audit</span></span>
* <span data-ttu-id="dfbfa-116">Privilege-based audit trail viewing</span><span class="sxs-lookup"><span data-stu-id="dfbfa-116">Privilege-based audit trail viewing</span></span>
* <span data-ttu-id="dfbfa-117">Privilege-based audit summary viewing</span><span class="sxs-lookup"><span data-stu-id="dfbfa-117">Privilege-based audit summary viewing</span></span>
* <span data-ttu-id="dfbfa-118">Audit log deletion for a partitioned SQL database</span><span class="sxs-lookup"><span data-stu-id="dfbfa-118">Audit log deletion for a partitioned SQL database</span></span>  
* <span data-ttu-id="dfbfa-119">Audit log deletion for a non-partitioned SQL database</span><span class="sxs-lookup"><span data-stu-id="dfbfa-119">Audit log deletion for a non-partitioned SQL database</span></span> 
* <span data-ttu-id="dfbfa-120">Audit of record create, update, and delete operations</span><span class="sxs-lookup"><span data-stu-id="dfbfa-120">Audit of record create, update, and delete operations</span></span>
* <span data-ttu-id="dfbfa-121">Audit of relationships (1:N, N:N)</span><span class="sxs-lookup"><span data-stu-id="dfbfa-121">Audit of relationships (1:N, N:N)</span></span> 
* <span data-ttu-id="dfbfa-122">Audit of audit events</span><span class="sxs-lookup"><span data-stu-id="dfbfa-122">Audit of audit events</span></span>
* <span data-ttu-id="dfbfa-123">Audit of user access</span><span class="sxs-lookup"><span data-stu-id="dfbfa-123">Audit of user access</span></span>
* <span data-ttu-id="dfbfa-124">Adherence to regulatory standards</span><span class="sxs-lookup"><span data-stu-id="dfbfa-124">Adherence to regulatory standards</span></span>
* <span data-ttu-id="dfbfa-125">Auditing APIs for developers</span><span class="sxs-lookup"><span data-stu-id="dfbfa-125">Auditing APIs for developers</span></span>
  
## <a name="not-supported-for-auditing"></a><span data-ttu-id="dfbfa-126">Not supported for auditing</span><span class="sxs-lookup"><span data-stu-id="dfbfa-126">Not supported for auditing</span></span>  
 <span data-ttu-id="dfbfa-127">The following lists what cannot be audited for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps:</span><span class="sxs-lookup"><span data-stu-id="dfbfa-127">The following lists what cannot be audited for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps:</span></span>  
  
* <span data-ttu-id="dfbfa-128">Audit of read operations</span><span class="sxs-lookup"><span data-stu-id="dfbfa-128">Audit of read operations</span></span>
* <span data-ttu-id="dfbfa-129">Audit of metadata changes</span><span class="sxs-lookup"><span data-stu-id="dfbfa-129">Audit of metadata changes</span></span> 
  
## <a name="key-concepts"></a><span data-ttu-id="dfbfa-130">Key concepts</span><span class="sxs-lookup"><span data-stu-id="dfbfa-130">Key concepts</span></span>  
 <span data-ttu-id="dfbfa-131">The following bullets identify some key auditing concepts:</span><span class="sxs-lookup"><span data-stu-id="dfbfa-131">The following bullets identify some key auditing concepts:</span></span>  
  
- <span data-ttu-id="dfbfa-132">You can enable or disable auditing at the organization, entity, and attribute levels.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-132">You can enable or disable auditing at the organization, entity, and attribute levels.</span></span> <span data-ttu-id="dfbfa-133">If auditing is not enabled at the organization level, auditing of entities and attributes, even if it is enabled, does not occur.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-133">If auditing is not enabled at the organization level, auditing of entities and attributes, even if it is enabled, does not occur.</span></span> <span data-ttu-id="dfbfa-134">By default, auditing is enabled on all auditable entity attributes, but is disabled at the entity and organization level.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-134">By default, auditing is enabled on all auditable entity attributes, but is disabled at the entity and organization level.</span></span>  
  
- <span data-ttu-id="dfbfa-135">For [!INCLUDE[pn-crmop-edition](../includes/pn-crm-onprem.md)] servers that use [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] Enterprise editions, auditing data is recorded over time (quarterly) in *partitions*.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-135">For [!INCLUDE[pn-crmop-edition](../includes/pn-crm-onprem.md)] servers that use [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] Enterprise editions, auditing data is recorded over time (quarterly) in *partitions*.</span></span> <span data-ttu-id="dfbfa-136">A partition is called an *audit log* in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps web application.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-136">A partition is called an *audit log* in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps web application.</span></span> <span data-ttu-id="dfbfa-137">Partitions are not supported, and therefore, not used, on a [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps server that is running [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)], Standard edition.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-137">Partitions are not supported, and therefore, not used, on a [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps server that is running [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)], Standard edition.</span></span>  
  
- <span data-ttu-id="dfbfa-138">The ability to retrieve and display the audit history is restricted to users who have certain security privileges: View Audit History, and View Audit Summary.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-138">The ability to retrieve and display the audit history is restricted to users who have certain security privileges: View Audit History, and View Audit Summary.</span></span> <span data-ttu-id="dfbfa-139">There are also privileges specific to partitions: View Audit Partitions, and Delete Audit Partitions.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-139">There are also privileges specific to partitions: View Audit Partitions, and Delete Audit Partitions.</span></span> <span data-ttu-id="dfbfa-140">See the specific message request documentation for information about the required privileges for each message.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-140">See the specific message request documentation for information about the required privileges for each message.</span></span>  
  
- <span data-ttu-id="dfbfa-141">Audited data changes are stored in records of the **audit** entity.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-141">Audited data changes are stored in records of the **audit** entity.</span></span>  
  
## <a name="data-that-can-be-audited"></a><span data-ttu-id="dfbfa-142">Data that can be audited</span><span class="sxs-lookup"><span data-stu-id="dfbfa-142">Data that can be audited</span></span>  
 <span data-ttu-id="dfbfa-143">The following list identifies the data and operations that can be audited:</span><span class="sxs-lookup"><span data-stu-id="dfbfa-143">The following list identifies the data and operations that can be audited:</span></span>  
  
- <span data-ttu-id="dfbfa-144">Create, update, and delete operations on records.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-144">Create, update, and delete operations on records.</span></span>  
  
- <span data-ttu-id="dfbfa-145">Changes to the shared privileges of a record.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-145">Changes to the shared privileges of a record.</span></span>  
  
- <span data-ttu-id="dfbfa-146">N:N association or disassociation of records.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-146">N:N association or disassociation of records.</span></span>  
  
- <span data-ttu-id="dfbfa-147">Thay đổi đối với vai trò bảo mật.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-147">Changes to security roles.</span></span>  
  
- <span data-ttu-id="dfbfa-148">Kiểm tra các thay đổi ở cấp độ thực thể, thuộc tính và tổ chức.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-148">Audit changes at the entity, attribute, and organization level.</span></span> <span data-ttu-id="dfbfa-149">Ví dụ: cho phép các kiểm tra trên một thực thể.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-149">For example, enabling audit on an entity.</span></span>  
  
- <span data-ttu-id="dfbfa-150">Xóa nhật ký kiểm tra.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-150">Deletion of audit logs.</span></span>  
  
- <span data-ttu-id="dfbfa-151">When (date/time) a user accesses [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps data, for how long, and from what client.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-151">When (date/time) a user accesses [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps data, for how long, and from what client.</span></span>  
  
  <span data-ttu-id="dfbfa-152">Enabling or disabling of field level security by setting the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.IsSecured> attribute cannot be audited.</span><span class="sxs-lookup"><span data-stu-id="dfbfa-152">Enabling or disabling of field level security by setting the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.IsSecured> attribute cannot be audited.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="dfbfa-153">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="dfbfa-153">See also</span></span>
 <span data-ttu-id="dfbfa-154">[Data Management in Dynamics 365 for Customer Engagement apps](manage-data.md) </span><span class="sxs-lookup"><span data-stu-id="dfbfa-154">[Data Management in Dynamics 365 for Customer Engagement apps](manage-data.md) </span></span>  
 <span data-ttu-id="dfbfa-155">[Audit entity data changes](audit-entity-data-changes.md) </span><span class="sxs-lookup"><span data-stu-id="dfbfa-155">[Audit entity data changes](audit-entity-data-changes.md) </span></span>  
 <span data-ttu-id="dfbfa-156">[Configure entities and attributes for auditing](configure-entities-attributes-auditing.md)     </span><span class="sxs-lookup"><span data-stu-id="dfbfa-156">[Configure entities and attributes for auditing](configure-entities-attributes-auditing.md)     </span></span>  
 [<span data-ttu-id="dfbfa-157">Blog: Recover your deleted CRM data and recreate them using CRM API</span><span class="sxs-lookup"><span data-stu-id="dfbfa-157">Blog: Recover your deleted CRM data and recreate them using CRM API</span></span>](http://blogs.msdn.com/b/crm/archive/2011/05/23/recover-your-deleted-crm-data-and-recreate-them-using-crm-api.aspx)
