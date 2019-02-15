---
title: CampaignItem intersect entity metadata (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: The CampaignItem intersect entity is the intersect table for several many-to-many relationships for the Campaign entity
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
- campaign entity, campaignitem intersect table
- campaignitem intersect entity, effect of early- and late-bound types on
- campaignitem intersect entity, many-to-many (N:N) relationships for the campaign entity
- many-to-many (N:N) relationships, for the campaignitem intersect entity
- intersect entity metadata, campaignitem
- campaignitem intersect entity, table of attribute metadata
ms.assetid: 23835406-e515-4240-a10b-3d5df12542f5
caps.latest.revision: 18
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 14c86fc47a81f0514caa8cf9aede80fbdc57615b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386101"
---
# <a name="campaignitem-intersect-entity-metadata"></a>CampaignItem intersect entity metadata

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

The `CampaignItem` intersect entity is the intersect table for the following many-to-many relationships for the `Campaign` entity.  
  
|Relationship schema name|Entity 1|Entity 2|  
|------------------------------|--------------|--------------|  
|campaignproduct_association|chiến dịch|Sản phẩm|  
|campaigncampaign_association|chiến dịch|Chiến dịch|  
|campaignsalesliterature_association|chiến dịch|SalesLiterature|  
|campaignlist_association|chiến dịch|Danh sách|  
  
 If you are not using early bound types, you might need to know the names of the attributes in this entity to effectively build a query. This information is provided in the following table. [!INCLUDE[metadata_browser](../../includes/metadata-browser.md)]  
  
### <a name="see-also"></a>Xem thêm  
 [Retrieve Records for Many-To-Many Relationships using Intersect Entities](retrieve-records-many-to-many-relationships-intersect-entities.md)   
 [CampaignActivityItem intersect entity metadata](campaignactivityitem-intersect-entity-metadata.md)   
 [ListMember intersect entity metadata](listmember-intersect-entity-metadata.md)   
 [Role Privileges intersect entity metadata](role-privileges-intersect-entity-metadata.md)   
 [Sample: Retrieve records from an intersect table](sample-retrieve-records-intersect-table.md)   
 [Campaign entities](../campaign-entities.md)
