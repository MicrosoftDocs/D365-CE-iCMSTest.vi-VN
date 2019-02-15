---
title: CampaignActivityItem intersect entity metadata (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: The CampaignActivityItem intersect entity is the intersect table for the following many-to-many relationships for the CampaignActivity entity
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d2d7d3ee-c6e1-4c86-844f-68f9b5c843b8
caps.latest.revision: 19
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6de3acf9d0e4597a035631d7d3539b2dfab7bfdf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386263"
---
# <a name="campaignactivityitem-intersect-entity-metadata"></a>CampaignActivityItem intersect entity metadata

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

The `CampaignActivityItem` intersect entity is the intersect table for the following many-to-many relationships for the `CampaignActivity` entity.  
  
|Relationship schema name|Entity 1|Entity 2|  
|------------------------------|--------------|--------------|  
|campaignactivitysalesliterature_association|hoạt động chiến dịch|salesliterature|  
|campaignactivitylist_association|hoạt động chiến dịch|list|  
  
 If you are not using early bound types, you might need to know the names of the attributes in this entity to effectively build a query. This information is provided in the following table. [!INCLUDE[metadata_browser](../../includes/metadata-browser.md)]  
  
### <a name="see-also"></a>Xem thêm  
 [Retrieve Records for Many-To-Many Relationships using Intersect Entities](retrieve-records-many-to-many-relationships-intersect-entities.md)   
 [CampaignItem intersect entity metadata](campaignitem-intersect-entity-metadata.md)   
 [ListMember intersect entity metadata](listmember-intersect-entity-metadata.md)   
 [Role Privileges intersect entity metadata](role-privileges-intersect-entity-metadata.md)   
 [Sample: Retrieve records from an intersect table](sample-retrieve-records-intersect-table.md)   
 [Campaign entities](../campaign-entities.md)
