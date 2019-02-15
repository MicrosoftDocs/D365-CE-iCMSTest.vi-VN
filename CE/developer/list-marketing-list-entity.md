---
title: List (marketing list) entity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about list management and the list (marketing list) entity that help you create lists of potential customers or existing customers for marketing purposes.
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
- lists (marketing lists), managing
- marketing lists, see 'list (marketing list) entity'
- adding members to lists
- list (marketing list) entity, managing lists
- list (marketing list) entity, adding members to lists
- lists (marketing lists), introduction
- 'list (marketing list) entity, types of lists: dynamic and static'
ms.assetid: 720709e2-32e0-44bc-87dc-445cb5d16e91
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 80252fa791196745f57d628d2e2fb981c5e424d4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386587"
---
# <a name="list-marketing-list-entity"></a><span data-ttu-id="0c799-103">List (marketing list) entity</span><span class="sxs-lookup"><span data-stu-id="0c799-103">List (marketing list) entity</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="0c799-104">In [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], *list management* and the *list* (marketing list) entity help you create lists of potential customers or existing customers for marketing purposes.</span><span class="sxs-lookup"><span data-stu-id="0c799-104">In [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], *list management* and the *list* (marketing list) entity help you create lists of potential customers or existing customers for marketing purposes.</span></span> <span data-ttu-id="0c799-105">Typically, a list is a potential target for a campaign.</span><span class="sxs-lookup"><span data-stu-id="0c799-105">Typically, a list is a potential target for a campaign.</span></span> <span data-ttu-id="0c799-106">However, you can also use it for other marketing reasons.</span><span class="sxs-lookup"><span data-stu-id="0c799-106">However, you can also use it for other marketing reasons.</span></span> <span data-ttu-id="0c799-107">You can generate subsets of a list by using different parameters for a campaign or to run an activity in bulk mode.</span><span class="sxs-lookup"><span data-stu-id="0c799-107">You can generate subsets of a list by using different parameters for a campaign or to run an activity in bulk mode.</span></span>  
  
 <span data-ttu-id="0c799-108">There are two types of lists: static and dynamic.</span><span class="sxs-lookup"><span data-stu-id="0c799-108">There are two types of lists: static and dynamic.</span></span> <span data-ttu-id="0c799-109">To specify whether the list is static or dynamic, use the `List.Type` attribute.</span><span class="sxs-lookup"><span data-stu-id="0c799-109">To specify whether the list is static or dynamic, use the `List.Type` attribute.</span></span> <span data-ttu-id="0c799-110">All list members must be of the same entity type, such as accounts, contacts, or leads.</span><span class="sxs-lookup"><span data-stu-id="0c799-110">All list members must be of the same entity type, such as accounts, contacts, or leads.</span></span> <span data-ttu-id="0c799-111">To add the members to a static list, use the <xref:Microsoft.Crm.Sdk.Messages.AddListMembersListRequest> message.</span><span class="sxs-lookup"><span data-stu-id="0c799-111">To add the members to a static list, use the <xref:Microsoft.Crm.Sdk.Messages.AddListMembersListRequest> message.</span></span> <span data-ttu-id="0c799-112">The members for a dynamic list are selected dynamically based on the FetchXML query criteria during distribution of a campaign activity or a quick campaign.</span><span class="sxs-lookup"><span data-stu-id="0c799-112">The members for a dynamic list are selected dynamically based on the FetchXML query criteria during distribution of a campaign activity or a quick campaign.</span></span> <span data-ttu-id="0c799-113">To specify the FetchXML criteria, use the `List.Query` attribute.</span><span class="sxs-lookup"><span data-stu-id="0c799-113">To specify the FetchXML criteria, use the `List.Query` attribute.</span></span> <span data-ttu-id="0c799-114">Initially, the member count for the dynamic list is set to **null**.</span><span class="sxs-lookup"><span data-stu-id="0c799-114">Initially, the member count for the dynamic list is set to **null**.</span></span> <span data-ttu-id="0c799-115">To determine how many records in the system satisfy the FetchXML query criteria, use the aggregate function on the query.</span><span class="sxs-lookup"><span data-stu-id="0c799-115">To determine how many records in the system satisfy the FetchXML query criteria, use the aggregate function on the query.</span></span> <span data-ttu-id="0c799-116">You can create a new static list based on the existing dynamic list by using the <xref:Microsoft.Crm.Sdk.Messages.CopyDynamicListToStaticRequest> message.</span><span class="sxs-lookup"><span data-stu-id="0c799-116">You can create a new static list based on the existing dynamic list by using the <xref:Microsoft.Crm.Sdk.Messages.CopyDynamicListToStaticRequest> message.</span></span> <span data-ttu-id="0c799-117">The newly created static list is locked.</span><span class="sxs-lookup"><span data-stu-id="0c799-117">The newly created static list is locked.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0c799-118">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="0c799-118">See also</span></span>  
 <span data-ttu-id="0c799-119">[List Entity](entities/list.md) </span><span class="sxs-lookup"><span data-stu-id="0c799-119">[List Entity](entities/list.md) </span></span>  
 <span data-ttu-id="0c799-120">[Use FetchXML to Construct a Query](org-service/use-fetchxml-construct-query.md) </span><span class="sxs-lookup"><span data-stu-id="0c799-120">[Use FetchXML to Construct a Query](org-service/use-fetchxml-construct-query.md) </span></span>  
 <span data-ttu-id="0c799-121">[Use FetchXML Aggregation](org-service/use-fetchxml-aggregation.md) </span><span class="sxs-lookup"><span data-stu-id="0c799-121">[Use FetchXML Aggregation](org-service/use-fetchxml-aggregation.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.CopyDynamicListToStaticRequest>   
 <span data-ttu-id="0c799-122">[Marketing Entities (Campaign, List)](marketing-entities-campaign-list.md) </span><span class="sxs-lookup"><span data-stu-id="0c799-122">[Marketing Entities (Campaign, List)](marketing-entities-campaign-list.md) </span></span>  
 [<span data-ttu-id="0c799-123">Sample: Distribute a Quick Campaign</span><span class="sxs-lookup"><span data-stu-id="0c799-123">Sample: Distribute a Quick Campaign</span></span>](sample-distribute-a-quick-campaign.md)
