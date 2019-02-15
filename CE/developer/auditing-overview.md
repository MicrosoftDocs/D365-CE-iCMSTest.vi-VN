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
# <a name="auditing-overview"></a>Tổng quan về kiểm tra

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Các tổ chức thường cần phải tuân thủ nhiều quy định khác nhau để đảm bảo tính khả dụng của lịch sử tương tác khách hàng, nhật ký kiểm tra, báo cáo truy cập và các báo cáo theo dõi sự cố bảo mật. Organizations may want to track changes in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps data for security and analytical purpose.  
  
 [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps support an auditing capability where entity and attribute data changes within an organization can be recorded over time for use in analysis and reporting purposes. Auditing is supported on all custom and most customizable entities and attributes. Auditing is not supported on metadata changes, retrieve operations, export operations, or during authentication. For information on how to configure auditing, see [Configure Entities and Attributes for Auditing](configure-entities-attributes-auditing.md).  
  
## <a name="supported-for-auditing"></a>Supported for auditing  
 The following lists auditing capabilities for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps:  
<!-- TODO: Jim, I don't think this is online only. Please correct the tokens here. -->
  
* Audit of customizable entities
* Audit of custom entities
* Configure entities for audit
* Configure attributes for audit
* Privilege-based audit trail viewing
* Privilege-based audit summary viewing
* Audit log deletion for a partitioned SQL database  
* Audit log deletion for a non-partitioned SQL database 
* Audit of record create, update, and delete operations
* Audit of relationships (1:N, N:N) 
* Audit of audit events
* Audit of user access
* Adherence to regulatory standards
* Auditing APIs for developers
  
## <a name="not-supported-for-auditing"></a>Not supported for auditing  
 The following lists what cannot be audited for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps:  
  
* Audit of read operations
* Audit of metadata changes 
  
## <a name="key-concepts"></a>Key concepts  
 The following bullets identify some key auditing concepts:  
  
- You can enable or disable auditing at the organization, entity, and attribute levels. If auditing is not enabled at the organization level, auditing of entities and attributes, even if it is enabled, does not occur. By default, auditing is enabled on all auditable entity attributes, but is disabled at the entity and organization level.  
  
- For [!INCLUDE[pn-crmop-edition](../includes/pn-crm-onprem.md)] servers that use [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] Enterprise editions, auditing data is recorded over time (quarterly) in *partitions*. A partition is called an *audit log* in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps web application. Partitions are not supported, and therefore, not used, on a [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps server that is running [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)], Standard edition.  
  
- The ability to retrieve and display the audit history is restricted to users who have certain security privileges: View Audit History, and View Audit Summary. There are also privileges specific to partitions: View Audit Partitions, and Delete Audit Partitions. See the specific message request documentation for information about the required privileges for each message.  
  
- Audited data changes are stored in records of the **audit** entity.  
  
## <a name="data-that-can-be-audited"></a>Data that can be audited  
 The following list identifies the data and operations that can be audited:  
  
- Create, update, and delete operations on records.  
  
- Changes to the shared privileges of a record.  
  
- N:N association or disassociation of records.  
  
- Thay đổi đối với vai trò bảo mật.  
  
- Kiểm tra các thay đổi ở cấp độ thực thể, thuộc tính và tổ chức. Ví dụ: cho phép các kiểm tra trên một thực thể.  
  
- Xóa nhật ký kiểm tra.  
  
- When (date/time) a user accesses [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps data, for how long, and from what client.  
  
  Enabling or disabling of field level security by setting the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.IsSecured> attribute cannot be audited.  
  
### <a name="see-also"></a>Xem thêm
 [Data Management in Dynamics 365 for Customer Engagement apps](manage-data.md)   
 [Audit entity data changes](audit-entity-data-changes.md)   
 [Configure entities and attributes for auditing](configure-entities-attributes-auditing.md)       
 [Blog: Recover your deleted CRM data and recreate them using CRM API](http://blogs.msdn.com/b/crm/archive/2011/05/23/recover-your-deleted-crm-data-and-recreate-them-using-crm-api.aspx)