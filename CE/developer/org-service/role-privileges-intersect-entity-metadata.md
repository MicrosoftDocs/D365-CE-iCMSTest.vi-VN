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
# <a name="role-privileges-intersect-entity-metadata"></a><span data-ttu-id="c05b4-103">Role Privileges intersect entity metadata</span><span class="sxs-lookup"><span data-stu-id="c05b4-103">Role Privileges intersect entity metadata</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c05b4-104">The `RolePrivileges` intersect entity is the intersect table for the following many-to-many relationships for the `Role` entity.</span><span class="sxs-lookup"><span data-stu-id="c05b4-104">The `RolePrivileges` intersect entity is the intersect table for the following many-to-many relationships for the `Role` entity.</span></span>  
  
|<span data-ttu-id="c05b4-105">Relationship schema name</span><span class="sxs-lookup"><span data-stu-id="c05b4-105">Relationship schema name</span></span>|<span data-ttu-id="c05b4-106">Entity 1</span><span class="sxs-lookup"><span data-stu-id="c05b4-106">Entity 1</span></span>|<span data-ttu-id="c05b4-107">Entity 2</span><span class="sxs-lookup"><span data-stu-id="c05b4-107">Entity 2</span></span>|  
|------------------------------|--------------|--------------|  
|<span data-ttu-id="c05b4-108">roleprivileges_association</span><span class="sxs-lookup"><span data-stu-id="c05b4-108">roleprivileges_association</span></span>|<span data-ttu-id="c05b4-109">Đặc quyền</span><span class="sxs-lookup"><span data-stu-id="c05b4-109">Privilege</span></span>|<span data-ttu-id="c05b4-110">Vai trò</span><span class="sxs-lookup"><span data-stu-id="c05b4-110">Role</span></span>|  
  
 <span data-ttu-id="c05b4-111">If you are not using early bound types, you might need to know the names of the attributes in this entity to effectively build a query.</span><span class="sxs-lookup"><span data-stu-id="c05b4-111">If you are not using early bound types, you might need to know the names of the attributes in this entity to effectively build a query.</span></span> <span data-ttu-id="c05b4-112">This information is provided in the following table.</span><span class="sxs-lookup"><span data-stu-id="c05b4-112">This information is provided in the following table.</span></span> [!INCLUDE[metadata_browser](../../includes/metadata-browser.md)]  
  
### <a name="see-also"></a><span data-ttu-id="c05b4-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c05b4-113">See also</span></span>  
 <span data-ttu-id="c05b4-114">[Retrieve Records for Many-To-Many Relationships using Intersect Entities](retrieve-records-many-to-many-relationships-intersect-entities.md) </span><span class="sxs-lookup"><span data-stu-id="c05b4-114">[Retrieve Records for Many-To-Many Relationships using Intersect Entities](retrieve-records-many-to-many-relationships-intersect-entities.md) </span></span>  
 <span data-ttu-id="c05b4-115">[CampaignActivityItem intersect entity metadata](campaignactivityitem-intersect-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="c05b4-115">[CampaignActivityItem intersect entity metadata](campaignactivityitem-intersect-entity-metadata.md) </span></span>  
 <span data-ttu-id="c05b4-116">[CampaignItem intersect entity metadata](campaignitem-intersect-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="c05b4-116">[CampaignItem intersect entity metadata](campaignitem-intersect-entity-metadata.md) </span></span>  
 <span data-ttu-id="c05b4-117">[ListMember intersect entity metadata](listmember-intersect-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="c05b4-117">[ListMember intersect entity metadata](listmember-intersect-entity-metadata.md) </span></span>  
 <span data-ttu-id="c05b4-118">[Sample: Retrieve records from an intersect table](sample-retrieve-records-intersect-table.md) </span><span class="sxs-lookup"><span data-stu-id="c05b4-118">[Sample: Retrieve records from an intersect table](sample-retrieve-records-intersect-table.md) </span></span>  
 [<span data-ttu-id="c05b4-119">Privilege and role entities</span><span class="sxs-lookup"><span data-stu-id="c05b4-119">Privilege and role entities</span></span>](../privilege-role-entities.md)
