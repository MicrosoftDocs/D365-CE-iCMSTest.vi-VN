---
title: ListMember intersect entity metadata (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: This topic lists the various many-to-many relationships for the List entity for which the ListMember intersect entity is the intersect table
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
- marketing list metadata
- list entity, listmember intersect table
- listmember intersect entity, many-to-many (N:N) relationships for the list entity
- listmember intersect entity, table of attribute metadata
- many-to-many (N:N) relationships, for the listmember intersect entity
- listmember intersect entity, effect of early- and late-bound types on
- intersect entity metadata, listmember
ms.assetid: b8dcd1b3-6750-429e-ac7a-c0213c77e136
caps.latest.revision: 15
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0e1206221d03864232684c5fc32ade6a23c54b2a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385904"
---
# <a name="listmember-intersect-entity-metadata"></a>ListMember intersect entity metadata

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

The `ListMember` intersect entity is the intersect table for the following many-to-many relationships for the `List` entity.  
  
|Relationship schema name|Entity 1|Entity 2|  
|------------------------------|--------------|--------------|  
|listaccount_association|list|tài khoản|  
|listcontact_association|list|người liên hệ|  
|listlead_association|list|Khách hàng tiềm năng|  
  
 If you are not using early bound types, you might need to know the names of the attributes in this entity to effectively build a query. This information is provided in the following table. [!INCLUDE[metadata_browser](../../includes/metadata-browser.md)]  
  
### <a name="see-also"></a>Xem thêm  
 [Retrieve Records for Many-To-Many Relationships using Intersect Entities](retrieve-records-many-to-many-relationships-intersect-entities.md)   
 [CampaignActivityItem intersect entity metadata](campaignactivityitem-intersect-entity-metadata.md)   
 [CampaignItem intersect entity metadata](campaignitem-intersect-entity-metadata.md)   
 [Role Privileges intersect entity metadata](role-privileges-intersect-entity-metadata.md)   
 [Sample: Retrieve records from an intersect table](sample-retrieve-records-intersect-table.md)   
 [Campaign Entities](../campaign-entities.md)
