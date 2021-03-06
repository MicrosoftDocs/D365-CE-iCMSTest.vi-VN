---
title: BusinessUnit entity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: A business unit is a unit of the top-level organization. Business units can be parents of other business units (child business units). The first business unit created for an organization is called the root business unit.
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
- businessunit entities
- business unit entities
- business unit, definition
ms.assetid: bf38e07e-37a2-419b-bd5e-d259d97a3c70
caps.latest.revision: 24
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9b747032510a3bc67413502eb7c27f8cd3764e33
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386489"
---
# <a name="businessunit-entity"></a>BusinessUnit entity

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

An organization in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], such as a holding company or a corporation, is made up of business units. A *business unit* is a unit of the top-level organization. Business units can be parents of other business units (child business units). The first business unit created for an organization is called the root business unit. Business units can be deleted, however, the root business unit can’t be deleted.  
  
 A *parent business unit* is any business unit with one or more business units that report to it in the hierarchy.  
  
 A *child business unit* is a business unit that is immediately under another business unit in the business hierarchy of an organization.  
  
 A business unit can own records as defined in the ownership type in the metadata definition for an entity. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Entity Ownership](introduction-entities.md#EntityOwnership)  
  
 You can call the <xref:Microsoft.Crm.Sdk.Messages.WhoAmIRequest> message to find out the business unit for the currently logged on or impersonated user.  
  
### <a name="see-also"></a>Xem thêm  
 [Administration and Security Entities](administration-security-entities.md)   
 [BusinessUnit Entity](entities/businessunit.md)   
 [User and team entities](user-team-entities.md)   
