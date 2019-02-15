---
title: Entity relationship eligibility (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: The article lists the messages that you can use to determine whether entities can participate in entity relationships
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
- determining whether entities can participate in entity relationships, messages for
- entity relationship eligibility, determining whether entities can participate in entity relationships
- entities
- confirming that entities can participate in entity relationships, messages for
ms.assetid: 960606ca-ff63-4b82-9fd6-2d2243a78043
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e060ce5ed050fc8f6187d2211260cc9d064a591a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387547"
---
# <a name="entity-relationship-eligibility"></a><span data-ttu-id="3c7ff-103">Entity relationship eligibility</span><span class="sxs-lookup"><span data-stu-id="3c7ff-103">Entity relationship eligibility</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3c7ff-104">Before you create an entity relationship you should confirm whether the entity is eligible to participate in the relationship.</span><span class="sxs-lookup"><span data-stu-id="3c7ff-104">Before you create an entity relationship you should confirm whether the entity is eligible to participate in the relationship.</span></span> <span data-ttu-id="3c7ff-105">The following table lists the messages that you can use to determine whether entities can participate in entity relationships.</span><span class="sxs-lookup"><span data-stu-id="3c7ff-105">The following table lists the messages that you can use to determine whether entities can participate in entity relationships.</span></span>  
  
|<span data-ttu-id="3c7ff-106">Thông báo</span><span class="sxs-lookup"><span data-stu-id="3c7ff-106">Message</span></span>|<span data-ttu-id="3c7ff-107">Web API Operation</span><span class="sxs-lookup"><span data-stu-id="3c7ff-107">Web API Operation</span></span>|<span data-ttu-id="3c7ff-108">SDK Assembly</span><span class="sxs-lookup"><span data-stu-id="3c7ff-108">SDK Assembly</span></span>|  
|-------------|-----------------|----------------|  
|<span data-ttu-id="3c7ff-109">CanBeReferenced</span><span class="sxs-lookup"><span data-stu-id="3c7ff-109">CanBeReferenced</span></span></br><span data-ttu-id="3c7ff-110">Checks whether the specified entity can be the primary entity (one) in a one-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="3c7ff-110">Checks whether the specified entity can be the primary entity (one) in a one-to-many relationship.</span></span>|<xref href="Microsoft.Dynamics.CRM.CanBeReferenced?text=CanBeReferenced Action" />|<xref:Microsoft.Xrm.Sdk.Messages.CanBeReferencedRequest>|  
|<span data-ttu-id="3c7ff-111">CanBeReferencing</span><span class="sxs-lookup"><span data-stu-id="3c7ff-111">CanBeReferencing</span></span></br><span data-ttu-id="3c7ff-112">Checks whether the specified entity can be the referencing entity (many) in a one-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="3c7ff-112">Checks whether the specified entity can be the referencing entity (many) in a one-to-many relationship.</span></span>|<xref href="Microsoft.Dynamics.CRM.CanBeReferencing?text=CanBeReferencing Action" />|<xref:Microsoft.Xrm.Sdk.Messages.CanBeReferencingRequest>|  
|<span data-ttu-id="3c7ff-113">CanManyToMany</span><span class="sxs-lookup"><span data-stu-id="3c7ff-113">CanManyToMany</span></span></br><span data-ttu-id="3c7ff-114">Checks whether the entity can participate in a many-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="3c7ff-114">Checks whether the entity can participate in a many-to-many relationship.</span></span>|<xref href="Microsoft.Dynamics.CRM.CanManyToMany?text=CanManyToMany Action" />|<xref:Microsoft.Xrm.Sdk.Messages.CanManyToManyRequest>|  
|<span data-ttu-id="3c7ff-115">GetValidManyToMany</span><span class="sxs-lookup"><span data-stu-id="3c7ff-115">GetValidManyToMany</span></span></br><span data-ttu-id="3c7ff-116">Returns the set of entities that can participate in a many-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="3c7ff-116">Returns the set of entities that can participate in a many-to-many relationship.</span></span>|<xref href="Microsoft.Dynamics.CRM.GetValidManyToMany?text=GetValidManyToMany Function" />|<xref:Microsoft.Xrm.Sdk.Messages.GetValidManyToManyRequest>|  
|<span data-ttu-id="3c7ff-117">GetValidReferencedEntities</span><span class="sxs-lookup"><span data-stu-id="3c7ff-117">GetValidReferencedEntities</span></span></br><span data-ttu-id="3c7ff-118">Returns the set of entities that are valid as the primary entity (one) from the specified entity in a one-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="3c7ff-118">Returns the set of entities that are valid as the primary entity (one) from the specified entity in a one-to-many relationship.</span></span>|<xref href="Microsoft.Dynamics.CRM.GetValidReferencedEntities?text=GetValidReferencedEntities Function" />|<xref:Microsoft.Xrm.Sdk.Messages.GetValidReferencedEntitiesRequest>|  
|<span data-ttu-id="3c7ff-119">GetValidReferencingEntities</span><span class="sxs-lookup"><span data-stu-id="3c7ff-119">GetValidReferencingEntities</span></span></br><span data-ttu-id="3c7ff-120">Returns the set of entities that are valid as the related entity (many) to the specified entity in a one-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="3c7ff-120">Returns the set of entities that are valid as the related entity (many) to the specified entity in a one-to-many relationship.</span></span>|<xref href="Microsoft.Dynamics.CRM.GetValidReferencingEntities?text=GetValidReferencingEntities Function" />|<xref:Microsoft.Xrm.Sdk.Messages.GetValidReferencingEntitiesRequest>|  
  
### <a name="see-also"></a><span data-ttu-id="3c7ff-121">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3c7ff-121">See also</span></span>  
 <span data-ttu-id="3c7ff-122">[Customize Entity Relationship Metadata](customize-entity-relationship-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="3c7ff-122">[Customize Entity Relationship Metadata](customize-entity-relationship-metadata.md) </span></span>  
 <span data-ttu-id="3c7ff-123">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](org-service/use-organization-service-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="3c7ff-123">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](org-service/use-organization-service-metadata.md) </span></span>  
 <span data-ttu-id="3c7ff-124">[Entity Relationship Metadata](customize-entity-relationship-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="3c7ff-124">[Entity Relationship Metadata](customize-entity-relationship-metadata.md) </span></span>  
 <span data-ttu-id="3c7ff-125">[Entity Relationship Messages](entity-relationship-metadata-messages.md) </span><span class="sxs-lookup"><span data-stu-id="3c7ff-125">[Entity Relationship Messages](entity-relationship-metadata-messages.md) </span></span>  
 <span data-ttu-id="3c7ff-126">[Entity Relationship Behavior](entity-relationship-behavior.md) </span><span class="sxs-lookup"><span data-stu-id="3c7ff-126">[Entity Relationship Behavior](entity-relationship-behavior.md) </span></span>  
 <span data-ttu-id="3c7ff-127">[Create a 1:N Entity Relationship](org-service/create-retrieve-entity-relationships.md#BKMK_Create1NEntityRelationship) </span><span class="sxs-lookup"><span data-stu-id="3c7ff-127">[Create a 1:N Entity Relationship](org-service/create-retrieve-entity-relationships.md#BKMK_Create1NEntityRelationship) </span></span>  
 [<span data-ttu-id="3c7ff-128">Create an N:N Entity Relationship</span><span class="sxs-lookup"><span data-stu-id="3c7ff-128">Create an N:N Entity Relationship</span></span>](org-service/create-retrieve-entity-relationships.md#BKMK_CreateNNEntityRelationship)
