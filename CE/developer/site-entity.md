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
# <a name="site-entity"></a>Site entity

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

The *site* entity represents a location or branch office where an organization does business. Many [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] customers have multiple sites. Sites enable resources, services, and appointments to be defined at a particular location with an associated time zone. Location, correct selection of resources, and time zone are important elements in the scheduling of service appointments when multiple locations of doing business are involved. You can use sites to limit what resources, such as users and equipment, can be scheduled for a specific service activity.  
  
 When you search for an available service activity resource calendar time slot, to avoid making an appointment in the wrong location, the scheduler must be able to select the site or delivery location as a constraint to the search. For example, a customer may ask for an appointment at the Seattle office. To support this, there must be a site named Seattle and there must be required resources assigned to the service type to be performed. When generating appointment proposals, [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] must be able to avoid proposing appointments with resources that can’t physically be together to provide the service. The site entity serves this purpose. Sites provide for the grouping of resources, such as users and facility/equipment, services, and appointments, according to a location with an associated time zone and locale.  
  
### <a name="see-also"></a>Xem thêm  
 [Site Entity](entities/site.md)   
 [Business Management Entities](business-management-entities.md)
