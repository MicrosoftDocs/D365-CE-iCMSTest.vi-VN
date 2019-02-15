---
title: Privilege and role entities (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: A privilege is a permission to perform an action on a specific entity type in Dynamics 365 for Customer Engagement apps. The platform checks for the privilege and fails if the user does not hold the privilege. A privilege has an associated access level that determines the depth within the organization to which the privilege applies.
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
- role or security role, definition
- privilege, definition
- privilege entity
- role (security role) entity
ms.assetid: 3b566768-60e2-4c06-bb99-e6b0aacc0bc9
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5d234af8ca1acdcdf1308fd81b8ba65a17974710
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388610"
---
# <a name="privilege-and-role-entities"></a><span data-ttu-id="e664b-105">Privilege and role entities</span><span class="sxs-lookup"><span data-stu-id="e664b-105">Privilege and role entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e664b-106">A *privilege* is a permission to perform an action on a specific entity type in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="e664b-106">A *privilege* is a permission to perform an action on a specific entity type in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="e664b-107">The platform checks for the privilege and fails if the user does not hold the privilege.</span><span class="sxs-lookup"><span data-stu-id="e664b-107">The platform checks for the privilege and fails if the user does not hold the privilege.</span></span> <span data-ttu-id="e664b-108">A privilege has an associated access level that determines the depth within the organization to which the privilege applies.</span><span class="sxs-lookup"><span data-stu-id="e664b-108">A privilege has an associated access level that determines the depth within the organization to which the privilege applies.</span></span>  
  
 <span data-ttu-id="e664b-109">A *role*, or security role, is a grouping of security privileges.</span><span class="sxs-lookup"><span data-stu-id="e664b-109">A *role*, or security role, is a grouping of security privileges.</span></span> <span data-ttu-id="e664b-110">Users are assigned roles that authorize their access to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="e664b-110">Users are assigned roles that authorize their access to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span></span> <span data-ttu-id="e664b-111">A user must be assigned to at least one role.</span><span class="sxs-lookup"><span data-stu-id="e664b-111">A user must be assigned to at least one role.</span></span> <span data-ttu-id="e664b-112">It isn’t sufficient to be a member of a team that has an assigned role.</span><span class="sxs-lookup"><span data-stu-id="e664b-112">It isn’t sufficient to be a member of a team that has an assigned role.</span></span>  
  
 <span data-ttu-id="e664b-113">For more information about access levels and roles, see [How Role-Based Security Can Be Used to Control Access to Entities In Dynamics 365 for Customer Engagement apps](security-dev/how-role-based-security-control-access-entities.md).</span><span class="sxs-lookup"><span data-stu-id="e664b-113">For more information about access levels and roles, see [How Role-Based Security Can Be Used to Control Access to Entities In Dynamics 365 for Customer Engagement apps](security-dev/how-role-based-security-control-access-entities.md).</span></span>  
  
 <span data-ttu-id="e664b-114">The following illustration shows the entity relationships for this area.</span><span class="sxs-lookup"><span data-stu-id="e664b-114">The following illustration shows the entity relationships for this area.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="e664b-115">[Key to Entity Diagrams](key-entity-diagrams.md)</span><span class="sxs-lookup"><span data-stu-id="e664b-115">[Key to Entity Diagrams](key-entity-diagrams.md)</span></span>  
  
 <span data-ttu-id="e664b-116">![Privilege and role entity relationship diagram](media/role.png "Privilege and role entity relationship diagram")</span><span class="sxs-lookup"><span data-stu-id="e664b-116">![Privilege and role entity relationship diagram](media/role.png "Privilege and role entity relationship diagram")</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e664b-117">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e664b-117">See also</span></span>  
 <span data-ttu-id="e664b-118">[Role Entity](entities/role.md) </span><span class="sxs-lookup"><span data-stu-id="e664b-118">[Role Entity](entities/role.md) </span></span>  
 <span data-ttu-id="e664b-119">[Privilege Entity](entities/privilege.md) </span><span class="sxs-lookup"><span data-stu-id="e664b-119">[Privilege Entity](entities/privilege.md) </span></span>  
 <span data-ttu-id="e664b-120">[Sample: Assign a Security Role to Team](sample-associate-security-role-team.md) </span><span class="sxs-lookup"><span data-stu-id="e664b-120">[Sample: Assign a Security Role to Team](sample-associate-security-role-team.md) </span></span>  
 <span data-ttu-id="e664b-121">[Sample: Associate a Security Role to a User](sample-associate-security-role-user.md) </span><span class="sxs-lookup"><span data-stu-id="e664b-121">[Sample: Associate a Security Role to a User](sample-associate-security-role-user.md) </span></span>  
 <span data-ttu-id="e664b-122">[Sample: Determine Whether a User has a Role](sample-determine-user-role.md) </span><span class="sxs-lookup"><span data-stu-id="e664b-122">[Sample: Determine Whether a User has a Role](sample-determine-user-role.md) </span></span>  
 <span data-ttu-id="e664b-123">[Sample: Remove a Role for a User](sample-remove-role-user.md) </span><span class="sxs-lookup"><span data-stu-id="e664b-123">[Sample: Remove a Role for a User](sample-remove-role-user.md) </span></span>  
 <span data-ttu-id="e664b-124">[Sample: Retrieve the Roles for an Organization](sample-retrieve-roles-organization.md) </span><span class="sxs-lookup"><span data-stu-id="e664b-124">[Sample: Retrieve the Roles for an Organization](sample-retrieve-roles-organization.md) </span></span>  
 [<span data-ttu-id="e664b-125">Administration and Security Entities</span><span class="sxs-lookup"><span data-stu-id="e664b-125">Administration and Security Entities</span></span>](administration-security-entities.md)
