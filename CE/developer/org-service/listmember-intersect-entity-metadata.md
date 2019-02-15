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
# <a name="listmember-intersect-entity-metadata"></a><span data-ttu-id="aac53-103">ListMember intersect entity metadata</span><span class="sxs-lookup"><span data-stu-id="aac53-103">ListMember intersect entity metadata</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="aac53-104">The `ListMember` intersect entity is the intersect table for the following many-to-many relationships for the `List` entity.</span><span class="sxs-lookup"><span data-stu-id="aac53-104">The `ListMember` intersect entity is the intersect table for the following many-to-many relationships for the `List` entity.</span></span>  
  
|<span data-ttu-id="aac53-105">Relationship schema name</span><span class="sxs-lookup"><span data-stu-id="aac53-105">Relationship schema name</span></span>|<span data-ttu-id="aac53-106">Entity 1</span><span class="sxs-lookup"><span data-stu-id="aac53-106">Entity 1</span></span>|<span data-ttu-id="aac53-107">Entity 2</span><span class="sxs-lookup"><span data-stu-id="aac53-107">Entity 2</span></span>|  
|------------------------------|--------------|--------------|  
|<span data-ttu-id="aac53-108">listaccount_association</span><span class="sxs-lookup"><span data-stu-id="aac53-108">listaccount_association</span></span>|<span data-ttu-id="aac53-109">list</span><span class="sxs-lookup"><span data-stu-id="aac53-109">list</span></span>|<span data-ttu-id="aac53-110">tài khoản</span><span class="sxs-lookup"><span data-stu-id="aac53-110">account</span></span>|  
|<span data-ttu-id="aac53-111">listcontact_association</span><span class="sxs-lookup"><span data-stu-id="aac53-111">listcontact_association</span></span>|<span data-ttu-id="aac53-112">list</span><span class="sxs-lookup"><span data-stu-id="aac53-112">list</span></span>|<span data-ttu-id="aac53-113">người liên hệ</span><span class="sxs-lookup"><span data-stu-id="aac53-113">contact</span></span>|  
|<span data-ttu-id="aac53-114">listlead_association</span><span class="sxs-lookup"><span data-stu-id="aac53-114">listlead_association</span></span>|<span data-ttu-id="aac53-115">list</span><span class="sxs-lookup"><span data-stu-id="aac53-115">list</span></span>|<span data-ttu-id="aac53-116">Khách hàng tiềm năng</span><span class="sxs-lookup"><span data-stu-id="aac53-116">lead</span></span>|  
  
 <span data-ttu-id="aac53-117">If you are not using early bound types, you might need to know the names of the attributes in this entity to effectively build a query.</span><span class="sxs-lookup"><span data-stu-id="aac53-117">If you are not using early bound types, you might need to know the names of the attributes in this entity to effectively build a query.</span></span> <span data-ttu-id="aac53-118">This information is provided in the following table.</span><span class="sxs-lookup"><span data-stu-id="aac53-118">This information is provided in the following table.</span></span> [!INCLUDE[metadata_browser](../../includes/metadata-browser.md)]  
  
### <a name="see-also"></a><span data-ttu-id="aac53-119">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="aac53-119">See also</span></span>  
 <span data-ttu-id="aac53-120">[Retrieve Records for Many-To-Many Relationships using Intersect Entities](retrieve-records-many-to-many-relationships-intersect-entities.md) </span><span class="sxs-lookup"><span data-stu-id="aac53-120">[Retrieve Records for Many-To-Many Relationships using Intersect Entities](retrieve-records-many-to-many-relationships-intersect-entities.md) </span></span>  
 <span data-ttu-id="aac53-121">[CampaignActivityItem intersect entity metadata](campaignactivityitem-intersect-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="aac53-121">[CampaignActivityItem intersect entity metadata](campaignactivityitem-intersect-entity-metadata.md) </span></span>  
 <span data-ttu-id="aac53-122">[CampaignItem intersect entity metadata](campaignitem-intersect-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="aac53-122">[CampaignItem intersect entity metadata](campaignitem-intersect-entity-metadata.md) </span></span>  
 <span data-ttu-id="aac53-123">[Role Privileges intersect entity metadata](role-privileges-intersect-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="aac53-123">[Role Privileges intersect entity metadata](role-privileges-intersect-entity-metadata.md) </span></span>  
 <span data-ttu-id="aac53-124">[Sample: Retrieve records from an intersect table](sample-retrieve-records-intersect-table.md) </span><span class="sxs-lookup"><span data-stu-id="aac53-124">[Sample: Retrieve records from an intersect table](sample-retrieve-records-intersect-table.md) </span></span>  
 [<span data-ttu-id="aac53-125">Campaign Entities</span><span class="sxs-lookup"><span data-stu-id="aac53-125">Campaign Entities</span></span>](../campaign-entities.md)
