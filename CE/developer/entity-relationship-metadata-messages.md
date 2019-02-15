---
title: Entity relationship metadata messages (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: The article describes the messages that you can use to create, retrieve, update, and delete entity relationships
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
- entity relationship messages, list of messages with descriptions
- entity relationship metadata messages, list of messages with descriptions
- entity relationship eligibility, messages for
- relationships, list of messages for entity relationships
ms.assetid: 14b504b9-addb-40cd-aeef-a45a6a24bbcb
caps.latest.revision: 16
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8e936146a005aee98b5a4b7df823a61969308b5f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385802"
---
# <a name="entity-relationship-metadata-messages"></a>Entity relationship metadata messages

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Entity relationships define how entities are related to each other. This includes information about how relationships are represented in the application. Also, when actions are performed on a record, the relationship indicates what actions to perform on related records.  
  
## <a name="entity-relationship-messages"></a>Entity relationship messages  
 The following table lists the messages that you can use to create, retrieve, update, and delete entity relationships.  
  
|Thông báo|Mô tả|  
|-------------|-----------------|  
|<xref:Microsoft.Xrm.Sdk.Messages.CreateManyToManyRequest>|Creates a many-to-many relationship between two entities.|  
|<xref:Microsoft.Xrm.Sdk.Messages.CreateOneToManyRequest>|Creates a one-to-many relationship between two entities.|  
|<xref:Microsoft.Xrm.Sdk.Messages.DeleteRelationshipRequest>|Deletes an entity relationship.|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveRelationshipRequest>|Retrieves an entity relationship.|  
|<xref:Microsoft.Xrm.Sdk.Messages.UpdateRelationshipRequest>|Updates an entity relationship.|  
  
### <a name="see-also"></a>Xem thêm  
 [Customize Entity Relationship Metadata](customize-entity-relationship-metadata.md)   
 [Entity Relationship Eligibility](entity-relationship-eligibility.md)   
 [Entity Relationship Behavior](entity-relationship-behavior.md)
