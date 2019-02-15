---
title: ActivityPointer (activity) entity (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: The activity pointer (activity) entity represents any activity or task that is performed, or to be performed by a user. An activity is any action for which an entry can be made on a calendar
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
- creating activity records and their pointer records, activitypointer (activity) entity
- activitypointer (activity) entity, about
- activity entities, activitypointer (activity) entity
- activity types, activitypointer (activity) entity
- activitypointer (activity) entity, definition
ms.assetid: 00266be0-ee35-4504-b3d6-8ad528b82314
caps.latest.revision: 26
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5ab3020398d2f4430a6709557a96bbc517269fe5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387749"
---
# <a name="activitypointer-activity-entity"></a>ActivityPointer (activity) entity

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

The activity pointer (activity) entity represents any activity or task that is performed, or to be performed by a user. An activity is any action for which an entry can be made on a calendar.  
  
 Whenever you create an activity record in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], a corresponding activity pointer record is created. This indicates that the activity record and the corresponding activity pointer record have the same value for the `ActivityId` attribute. For example, if you create an `Email` record, the attribute values of `Email.ActivityId` and the corresponding `ActivityPointer.ActivityId` will be the same.  
  
 The `ActivityPointer.ActivityTypeCode` attribute defines the type of the activity. The possible values for this attribute are defined in `activitypointer_activitytypecode` global option set.  
  
<a name="bkmk_sortdate"></a>   
## <a name="control-how-activities-are-sorted-by-date"></a>Control how activities are sorted by date  
  
> [!NOTE]
>  This capability was introduced with [!INCLUDE[pn_crm_8_2_0_both](../includes/pn-crm-8-2-0-both.md)].  
  
 Whenever you display a list of activity entities and order them by date, you can only use the common date  attributes defined in the activitypointer entity. However, sometimes you want different sorting behaviors depending on the type of activity. For example, with the email entity you might want to sort by the senton attribute value  rather than the modifiedon attribute value.  
  
 Use the sortdate attribute to control how activities are sorted by date. By default, the sortdate attribute value is null. You must include business logic to populate the date value that will be set for this attribute and then use the sortdate attribute within the query defined for the view. You can set the sortdate attribute value using a workflow or a plugin. For consistent results you should set this value for every type of activity and any existing activity data in the system.  
  
### <a name="see-also"></a>Xem thêm  
 [Activity Entities](activity-entities.md)   
 [ActivityPointer Entity](entities/activitypointer.md)