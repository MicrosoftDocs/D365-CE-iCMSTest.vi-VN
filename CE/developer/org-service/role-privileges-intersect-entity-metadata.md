---
title: Role Privileges intersect entity metadata (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: The RolePrivileges intersect entity is the intersect table for the following many-to-many relationships for the Role entity
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: a85583a8-9f2b-401f-926d-7872e3885852
caps.latest.revision: 14
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3135ed7e40a62e7aa996c361bf7fde534c4eb33a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388453"
---
# <a name="role-privileges-intersect-entity-metadata"></a>Role Privileges intersect entity metadata

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

The `RolePrivileges` intersect entity is the intersect table for the following many-to-many relationships for the `Role` entity.  
  
|Relationship schema name|Entity 1|Entity 2|  
|------------------------------|--------------|--------------|  
|roleprivileges_association|Đặc quyền|Vai trò|  
  
 If you are not using early bound types, you might need to know the names of the attributes in this entity to effectively build a query. This information is provided in the following table. [!INCLUDE[metadata_browser](../../includes/metadata-browser.md)]  
  
### <a name="see-also"></a>Xem thêm  
 [Retrieve Records for Many-To-Many Relationships using Intersect Entities](retrieve-records-many-to-many-relationships-intersect-entities.md)   
 [CampaignActivityItem intersect entity metadata](campaignactivityitem-intersect-entity-metadata.md)   
 [CampaignItem intersect entity metadata](campaignitem-intersect-entity-metadata.md)   
 [ListMember intersect entity metadata](listmember-intersect-entity-metadata.md)   
 [Sample: Retrieve records from an intersect table](sample-retrieve-records-intersect-table.md)   
 [Privilege and role entities](../privilege-role-entities.md)
