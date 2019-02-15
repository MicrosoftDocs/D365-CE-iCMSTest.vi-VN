---
title: Service entities in Dynamics 365 for Customer Engagement (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about service entites that are targeted at the customer service department of an organization.
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
- service entities (contract; incident; knowledge base), introduction
- customer service department, entities for
ms.assetid: 4a81b285-0ebc-446e-920e-ac7d82d4b027
caps.latest.revision: 25
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9ee699362af65473e109bdbe2916811f660d84b0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386958"
---
# <a name="service-entities-in-dynamics-365-for-customer-engagement"></a><span data-ttu-id="59279-103">Service entities in Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="59279-103">Service entities in Dynamics 365 for Customer Engagement</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="59279-104">The entities described in this section are targeted at the customer service department of an organization.</span><span class="sxs-lookup"><span data-stu-id="59279-104">The entities described in this section are targeted at the customer service department of an organization.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="59279-105">In addition to the entities linked to later in this topic, there are several entities that will appear to support a set of messages or could be used with the<xref:Microsoft.Xrm.Sdk.IOrganizationService> methods.</span><span class="sxs-lookup"><span data-stu-id="59279-105">In addition to the entities linked to later in this topic, there are several entities that will appear to support a set of messages or could be used with the<xref:Microsoft.Xrm.Sdk.IOrganizationService> methods.</span></span> <span data-ttu-id="59279-106">However, the following entities are for internal use only:</span><span class="sxs-lookup"><span data-stu-id="59279-106">However, the following entities are for internal use only:</span></span>  
> 
> - <span data-ttu-id="59279-107">`ConvertRule` (Automatic Record Creation and Update Rule): Defines the rules for automatic record creation and updates.</span><span class="sxs-lookup"><span data-stu-id="59279-107">`ConvertRule` (Automatic Record Creation and Update Rule): Defines the rules for automatic record creation and updates.</span></span>  
>   -   <span data-ttu-id="59279-108">`ConvertRuleItem` (Case Creation Rule Item): Defines the individual conditions required for creating and updating record automatically.</span><span class="sxs-lookup"><span data-stu-id="59279-108">`ConvertRuleItem` (Case Creation Rule Item): Defines the individual conditions required for creating and updating record automatically.</span></span>  
>   -   <span data-ttu-id="59279-109">`RoutingRule` (Routing Rule Set): Defines a set of rules to route cases automatically to queues, users, or teams.</span><span class="sxs-lookup"><span data-stu-id="59279-109">`RoutingRule` (Routing Rule Set): Defines a set of rules to route cases automatically to queues, users, or teams.</span></span>  
>   -   <span data-ttu-id="59279-110">`RoutingRuleItem` (Rule Item): Defines the individual conditions required for routing the cases.</span><span class="sxs-lookup"><span data-stu-id="59279-110">`RoutingRuleItem` (Rule Item): Defines the individual conditions required for routing the cases.</span></span>  
>   -   <span data-ttu-id="59279-111">`SLA`: Contains information about the service level agreements for cases that belong to different customers.</span><span class="sxs-lookup"><span data-stu-id="59279-111">`SLA`: Contains information about the service level agreements for cases that belong to different customers.</span></span>  
>   -   <span data-ttu-id="59279-112">`SLAItem` (SLA Item): Contains information about a tracked service level agreement (SLA) key performance indicator and the condition when it is applicable for case records.</span><span class="sxs-lookup"><span data-stu-id="59279-112">`SLAItem` (SLA Item): Contains information about a tracked service level agreement (SLA) key performance indicator and the condition when it is applicable for case records.</span></span>  
> 
>   <span data-ttu-id="59279-113">While these entities appear to support common messages and methods, they also have a dependency on the web application so that certain messages will not work as expected when called directly from the web services.</span><span class="sxs-lookup"><span data-stu-id="59279-113">While these entities appear to support common messages and methods, they also have a dependency on the web application so that certain messages will not work as expected when called directly from the web services.</span></span> <span data-ttu-id="59279-114">You should not use these entities in your code.</span><span class="sxs-lookup"><span data-stu-id="59279-114">You should not use these entities in your code.</span></span>  
> 
>   <span data-ttu-id="59279-115">However, with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)], you can use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message on the `ConvertRule`, `RoutingRule`, and `SLA` entities to programmatically activate or deactivate these entity records.</span><span class="sxs-lookup"><span data-stu-id="59279-115">However, with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)], you can use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message on the `ConvertRule`, `RoutingRule`, and `SLA` entities to programmatically activate or deactivate these entity records.</span></span> <span data-ttu-id="59279-116">For information about changing the state of an entity record using the `Update` message, see [Perform specialized operations using Update](org-service/perform-specialized-operations-using-update.md)</span><span class="sxs-lookup"><span data-stu-id="59279-116">For information about changing the state of an entity record using the `Update` message, see [Perform specialized operations using Update](org-service/perform-specialized-operations-using-update.md)</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="59279-117">In This Section</span><span class="sxs-lookup"><span data-stu-id="59279-117">In This Section</span></span>  
 [<span data-ttu-id="59279-118">Contract Entities</span><span class="sxs-lookup"><span data-stu-id="59279-118">Contract Entities</span></span>](contract-entities.md)  
  
 [<span data-ttu-id="59279-119">Incident (Case) Entities</span><span class="sxs-lookup"><span data-stu-id="59279-119">Incident (Case) Entities</span></span>](incident-case-entities.md)  
  
 [<span data-ttu-id="59279-120">Knowledge Base Entities</span><span class="sxs-lookup"><span data-stu-id="59279-120">Knowledge Base Entities</span></span>](knowledge-management-entities.md)  
  
 [<span data-ttu-id="59279-121">Entitlement Entities</span><span class="sxs-lookup"><span data-stu-id="59279-121">Entitlement Entities</span></span>](entitlement-entities.md)  
  
 [<span data-ttu-id="59279-122">Apply SLAs to entities</span><span class="sxs-lookup"><span data-stu-id="59279-122">Apply SLAs to entities</span></span>](apply-slas-entities.md)  
  
 [<span data-ttu-id="59279-123">SlaKpiInstance Entity</span><span class="sxs-lookup"><span data-stu-id="59279-123">SlaKpiInstance Entity</span></span>](entities/slakpiinstance.md)  
  
## <a name="related-sections"></a><span data-ttu-id="59279-124">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="59279-124">Related Sections</span></span>  
 [<span data-ttu-id="59279-125">Model Your Business Data With Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="59279-125">Model Your Business Data With Dynamics 365 for Customer Engagement apps</span></span>](model-business-data.md)  
  
 [<span data-ttu-id="59279-126">Activity Entities</span><span class="sxs-lookup"><span data-stu-id="59279-126">Activity Entities</span></span>](activity-entities.md)  
  
 [<span data-ttu-id="59279-127">Server-side Synchronization Entities</span><span class="sxs-lookup"><span data-stu-id="59279-127">Server-side Synchronization Entities</span></span>](server-side-synchronization-entities.md)  
  
 [<span data-ttu-id="59279-128">Goal Management Entities</span><span class="sxs-lookup"><span data-stu-id="59279-128">Goal Management Entities</span></span>](goal-management-entities.md)  
  
 [<span data-ttu-id="59279-129">Product Catalog Entities</span><span class="sxs-lookup"><span data-stu-id="59279-129">Product Catalog Entities</span></span>](product-catalog-entities.md)  
  
 [<span data-ttu-id="59279-130">Sales Literature Entities</span><span class="sxs-lookup"><span data-stu-id="59279-130">Sales Literature Entities</span></span>](sales-literature-entities.md)
