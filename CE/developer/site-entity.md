---
title: Site entity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
decription: The site entity serves the purpose of sites providing for the grouping of resources, such as users and facility/equipment, services, and appointments, according to a location with an associated time zone and locale.
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
- sites
- site entity, scheduling appointments
- site entity, grouping resources
- locations, site entity
- site entity, limiting resources
- site entity, locations and offices
- site entity, offices
- site entity, definition
- offices, site entity
ms.assetid: a7915e27-dc79-4480-9ff1-f87e8d761ecb
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a60776057d94f8c6d087053756ceeb3e62b5d177
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386353"
---
# <a name="site-entity"></a><span data-ttu-id="41ea4-102">Site entity</span><span class="sxs-lookup"><span data-stu-id="41ea4-102">Site entity</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="41ea4-103">The *site* entity represents a location or branch office where an organization does business.</span><span class="sxs-lookup"><span data-stu-id="41ea4-103">The *site* entity represents a location or branch office where an organization does business.</span></span> <span data-ttu-id="41ea4-104">Many [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] customers have multiple sites.</span><span class="sxs-lookup"><span data-stu-id="41ea4-104">Many [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] customers have multiple sites.</span></span> <span data-ttu-id="41ea4-105">Sites enable resources, services, and appointments to be defined at a particular location with an associated time zone.</span><span class="sxs-lookup"><span data-stu-id="41ea4-105">Sites enable resources, services, and appointments to be defined at a particular location with an associated time zone.</span></span> <span data-ttu-id="41ea4-106">Location, correct selection of resources, and time zone are important elements in the scheduling of service appointments when multiple locations of doing business are involved.</span><span class="sxs-lookup"><span data-stu-id="41ea4-106">Location, correct selection of resources, and time zone are important elements in the scheduling of service appointments when multiple locations of doing business are involved.</span></span> <span data-ttu-id="41ea4-107">You can use sites to limit what resources, such as users and equipment, can be scheduled for a specific service activity.</span><span class="sxs-lookup"><span data-stu-id="41ea4-107">You can use sites to limit what resources, such as users and equipment, can be scheduled for a specific service activity.</span></span>  
  
 <span data-ttu-id="41ea4-108">When you search for an available service activity resource calendar time slot, to avoid making an appointment in the wrong location, the scheduler must be able to select the site or delivery location as a constraint to the search.</span><span class="sxs-lookup"><span data-stu-id="41ea4-108">When you search for an available service activity resource calendar time slot, to avoid making an appointment in the wrong location, the scheduler must be able to select the site or delivery location as a constraint to the search.</span></span> <span data-ttu-id="41ea4-109">For example, a customer may ask for an appointment at the Seattle office.</span><span class="sxs-lookup"><span data-stu-id="41ea4-109">For example, a customer may ask for an appointment at the Seattle office.</span></span> <span data-ttu-id="41ea4-110">To support this, there must be a site named Seattle and there must be required resources assigned to the service type to be performed.</span><span class="sxs-lookup"><span data-stu-id="41ea4-110">To support this, there must be a site named Seattle and there must be required resources assigned to the service type to be performed.</span></span> <span data-ttu-id="41ea4-111">When generating appointment proposals, [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] must be able to avoid proposing appointments with resources that can’t physically be together to provide the service.</span><span class="sxs-lookup"><span data-stu-id="41ea4-111">When generating appointment proposals, [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] must be able to avoid proposing appointments with resources that can’t physically be together to provide the service.</span></span> <span data-ttu-id="41ea4-112">The site entity serves this purpose.</span><span class="sxs-lookup"><span data-stu-id="41ea4-112">The site entity serves this purpose.</span></span> <span data-ttu-id="41ea4-113">Sites provide for the grouping of resources, such as users and facility/equipment, services, and appointments, according to a location with an associated time zone and locale.</span><span class="sxs-lookup"><span data-stu-id="41ea4-113">Sites provide for the grouping of resources, such as users and facility/equipment, services, and appointments, according to a location with an associated time zone and locale.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="41ea4-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="41ea4-114">See also</span></span>  
 <span data-ttu-id="41ea4-115">[Site Entity](entities/site.md) </span><span class="sxs-lookup"><span data-stu-id="41ea4-115">[Site Entity](entities/site.md) </span></span>  
 [<span data-ttu-id="41ea4-116">Business Management Entities</span><span class="sxs-lookup"><span data-stu-id="41ea4-116">Business Management Entities</span></span>](business-management-entities.md)
