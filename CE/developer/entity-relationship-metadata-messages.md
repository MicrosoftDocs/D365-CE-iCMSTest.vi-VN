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
# <a name="entity-relationship-metadata-messages"></a><span data-ttu-id="9befb-103">Entity relationship metadata messages</span><span class="sxs-lookup"><span data-stu-id="9befb-103">Entity relationship metadata messages</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9befb-104">Entity relationships define how entities are related to each other.</span><span class="sxs-lookup"><span data-stu-id="9befb-104">Entity relationships define how entities are related to each other.</span></span> <span data-ttu-id="9befb-105">This includes information about how relationships are represented in the application.</span><span class="sxs-lookup"><span data-stu-id="9befb-105">This includes information about how relationships are represented in the application.</span></span> <span data-ttu-id="9befb-106">Also, when actions are performed on a record, the relationship indicates what actions to perform on related records.</span><span class="sxs-lookup"><span data-stu-id="9befb-106">Also, when actions are performed on a record, the relationship indicates what actions to perform on related records.</span></span>  
  
## <a name="entity-relationship-messages"></a><span data-ttu-id="9befb-107">Entity relationship messages</span><span class="sxs-lookup"><span data-stu-id="9befb-107">Entity relationship messages</span></span>  
 <span data-ttu-id="9befb-108">The following table lists the messages that you can use to create, retrieve, update, and delete entity relationships.</span><span class="sxs-lookup"><span data-stu-id="9befb-108">The following table lists the messages that you can use to create, retrieve, update, and delete entity relationships.</span></span>  
  
|<span data-ttu-id="9befb-109">Thông báo</span><span class="sxs-lookup"><span data-stu-id="9befb-109">Message</span></span>|<span data-ttu-id="9befb-110">Mô tả</span><span class="sxs-lookup"><span data-stu-id="9befb-110">Description</span></span>|  
|-------------|-----------------|  
|<xref:Microsoft.Xrm.Sdk.Messages.CreateManyToManyRequest>|<span data-ttu-id="9befb-111">Creates a many-to-many relationship between two entities.</span><span class="sxs-lookup"><span data-stu-id="9befb-111">Creates a many-to-many relationship between two entities.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.CreateOneToManyRequest>|<span data-ttu-id="9befb-112">Creates a one-to-many relationship between two entities.</span><span class="sxs-lookup"><span data-stu-id="9befb-112">Creates a one-to-many relationship between two entities.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.DeleteRelationshipRequest>|<span data-ttu-id="9befb-113">Deletes an entity relationship.</span><span class="sxs-lookup"><span data-stu-id="9befb-113">Deletes an entity relationship.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveRelationshipRequest>|<span data-ttu-id="9befb-114">Retrieves an entity relationship.</span><span class="sxs-lookup"><span data-stu-id="9befb-114">Retrieves an entity relationship.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.UpdateRelationshipRequest>|<span data-ttu-id="9befb-115">Updates an entity relationship.</span><span class="sxs-lookup"><span data-stu-id="9befb-115">Updates an entity relationship.</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="9befb-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9befb-116">See also</span></span>  
 <span data-ttu-id="9befb-117">[Customize Entity Relationship Metadata](customize-entity-relationship-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="9befb-117">[Customize Entity Relationship Metadata](customize-entity-relationship-metadata.md) </span></span>  
 <span data-ttu-id="9befb-118">[Entity Relationship Eligibility](entity-relationship-eligibility.md) </span><span class="sxs-lookup"><span data-stu-id="9befb-118">[Entity Relationship Eligibility](entity-relationship-eligibility.md) </span></span>  
 [<span data-ttu-id="9befb-119">Entity Relationship Behavior</span><span class="sxs-lookup"><span data-stu-id="9befb-119">Entity Relationship Behavior</span></span>](entity-relationship-behavior.md)
