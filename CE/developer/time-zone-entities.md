---
title: Time zone entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: The time zone entities contain time zone information, such as supported time zone, time zone code, localized time zone, storing information on how times are calculated.
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
- time zone definition entity, definition
- local time
- time zone localized name entity, definition
- GMT
- UTC
- time zone entities, UTC and local time
- time zone rule entity, definition
- time zone entities, writing code for multiple time zones
- time zone entities, multiple time zones
ms.assetid: 87b89e1e-bca8-4934-9bd4-978676ccf5d1
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b947c80aaa073e5ab7f309a29d5c07c432f778d9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388339"
---
# <a name="time-zone-entities"></a>Time zone entities

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

The *time zone* entities can be used when you write code that works in multiple time zones. The following three read-only entities in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] contain time zone information:  
  
- The *time zone definition entity* stores basic information about each supported time zone, including the time zone code and the standard time zone name.  
  
- The *time zone localized name* entity stores the localized time zone names.  
  
- The *time zone rule* entity stores information about how times are calculated.  
  
  The following table lists the messages that are related to time zones, but don’t refer to a specific entity.  
  
|Thông báo|Mô tả|  
|-------------|-----------------|  
|<xref:Microsoft.Crm.Sdk.Messages.GetTimeZoneCodeByLocalizedNameRequest>|Retrieves all the time zone definitions for the specified locale, returning only the display name attribute.|  
|<xref:Microsoft.Crm.Sdk.Messages.LocalTimeFromUtcTimeRequest>|Retrieves the local time for the specified UTC time.|  
|<xref:Microsoft.Crm.Sdk.Messages.UtcTimeFromLocalTimeRequest>|Retrieves the UTC time for the specified local time.|  
  
### <a name="see-also"></a>Xem thêm  
 [Business Management Entities](business-management-entities.md)   
 [Sample: Retrieve Time Zone Information](sample-retrieve-time-zone-information.md)   
 [timezonedefinition EntityType](entities/timezonedefinition.md)   
 [timezonelocalizedname EntityType](entities/timezonelocalizedname.md)   
 [timezonerule EntityType](entities/timezonerule.md)   
 [Sample: Retrieve Time Zone Information](sample-retrieve-time-zone-information.md)   
 [Transaction Currency (Currency) Entity](transaction-currency-currency-entity.md)