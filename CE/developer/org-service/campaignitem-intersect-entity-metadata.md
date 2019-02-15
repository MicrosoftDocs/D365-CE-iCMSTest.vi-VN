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
# <a name="campaignitem-intersect-entity-metadata"></a><span data-ttu-id="90ecf-103">CampaignItem intersect entity metadata</span><span class="sxs-lookup"><span data-stu-id="90ecf-103">CampaignItem intersect entity metadata</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="90ecf-104">The `CampaignItem` intersect entity is the intersect table for the following many-to-many relationships for the `Campaign` entity.</span><span class="sxs-lookup"><span data-stu-id="90ecf-104">The `CampaignItem` intersect entity is the intersect table for the following many-to-many relationships for the `Campaign` entity.</span></span>  
  
|<span data-ttu-id="90ecf-105">Relationship schema name</span><span class="sxs-lookup"><span data-stu-id="90ecf-105">Relationship schema name</span></span>|<span data-ttu-id="90ecf-106">Entity 1</span><span class="sxs-lookup"><span data-stu-id="90ecf-106">Entity 1</span></span>|<span data-ttu-id="90ecf-107">Entity 2</span><span class="sxs-lookup"><span data-stu-id="90ecf-107">Entity 2</span></span>|  
|------------------------------|--------------|--------------|  
|<span data-ttu-id="90ecf-108">campaignproduct_association</span><span class="sxs-lookup"><span data-stu-id="90ecf-108">campaignproduct_association</span></span>|<span data-ttu-id="90ecf-109">chiến dịch</span><span class="sxs-lookup"><span data-stu-id="90ecf-109">campaign</span></span>|<span data-ttu-id="90ecf-110">Sản phẩm</span><span class="sxs-lookup"><span data-stu-id="90ecf-110">Product</span></span>|  
|<span data-ttu-id="90ecf-111">campaigncampaign_association</span><span class="sxs-lookup"><span data-stu-id="90ecf-111">campaigncampaign_association</span></span>|<span data-ttu-id="90ecf-112">chiến dịch</span><span class="sxs-lookup"><span data-stu-id="90ecf-112">campaign</span></span>|<span data-ttu-id="90ecf-113">Chiến dịch</span><span class="sxs-lookup"><span data-stu-id="90ecf-113">Campaign</span></span>|  
|<span data-ttu-id="90ecf-114">campaignsalesliterature_association</span><span class="sxs-lookup"><span data-stu-id="90ecf-114">campaignsalesliterature_association</span></span>|<span data-ttu-id="90ecf-115">chiến dịch</span><span class="sxs-lookup"><span data-stu-id="90ecf-115">campaign</span></span>|<span data-ttu-id="90ecf-116">SalesLiterature</span><span class="sxs-lookup"><span data-stu-id="90ecf-116">SalesLiterature</span></span>|  
|<span data-ttu-id="90ecf-117">campaignlist_association</span><span class="sxs-lookup"><span data-stu-id="90ecf-117">campaignlist_association</span></span>|<span data-ttu-id="90ecf-118">chiến dịch</span><span class="sxs-lookup"><span data-stu-id="90ecf-118">campaign</span></span>|<span data-ttu-id="90ecf-119">Danh sách</span><span class="sxs-lookup"><span data-stu-id="90ecf-119">List</span></span>|  
  
 <span data-ttu-id="90ecf-120">If you are not using early bound types, you might need to know the names of the attributes in this entity to effectively build a query.</span><span class="sxs-lookup"><span data-stu-id="90ecf-120">If you are not using early bound types, you might need to know the names of the attributes in this entity to effectively build a query.</span></span> <span data-ttu-id="90ecf-121">This information is provided in the following table.</span><span class="sxs-lookup"><span data-stu-id="90ecf-121">This information is provided in the following table.</span></span> [!INCLUDE[metadata_browser](../../includes/metadata-browser.md)]  
  
### <a name="see-also"></a><span data-ttu-id="90ecf-122">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="90ecf-122">See also</span></span>  
 <span data-ttu-id="90ecf-123">[Retrieve Records for Many-To-Many Relationships using Intersect Entities](retrieve-records-many-to-many-relationships-intersect-entities.md) </span><span class="sxs-lookup"><span data-stu-id="90ecf-123">[Retrieve Records for Many-To-Many Relationships using Intersect Entities](retrieve-records-many-to-many-relationships-intersect-entities.md) </span></span>  
 <span data-ttu-id="90ecf-124">[CampaignActivityItem intersect entity metadata](campaignactivityitem-intersect-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="90ecf-124">[CampaignActivityItem intersect entity metadata](campaignactivityitem-intersect-entity-metadata.md) </span></span>  
 <span data-ttu-id="90ecf-125">[ListMember intersect entity metadata](listmember-intersect-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="90ecf-125">[ListMember intersect entity metadata](listmember-intersect-entity-metadata.md) </span></span>  
 <span data-ttu-id="90ecf-126">[Role Privileges intersect entity metadata](role-privileges-intersect-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="90ecf-126">[Role Privileges intersect entity metadata](role-privileges-intersect-entity-metadata.md) </span></span>  
 <span data-ttu-id="90ecf-127">[Sample: Retrieve records from an intersect table](sample-retrieve-records-intersect-table.md) </span><span class="sxs-lookup"><span data-stu-id="90ecf-127">[Sample: Retrieve records from an intersect table](sample-retrieve-records-intersect-table.md) </span></span>  
 [<span data-ttu-id="90ecf-128">Campaign entities</span><span class="sxs-lookup"><span data-stu-id="90ecf-128">Campaign entities</span></span>](../campaign-entities.md)
