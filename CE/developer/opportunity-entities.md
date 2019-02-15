---
title: Opportunity entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'Learn about opportunity entites that help you to create a new opportunity to monitor or convert an lead to an opportunity. The entities that can be associated with an opportunity to provide information about the sales engagement are activities, notes and attachments, competitors, quotes, orders, and sales literature. '
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
- opportunity entities, linking to accounts or contacts
- opportunity entities, rating opportunities
- opportunity entities, definition
- opportunity entities, converting leads to opportunities
- opportunity entities, associated products and activities
- opportunities
- opportunity entities, introduction
- tracking opportunities, opportunity entities
- converting leads to opportunities, opportunity entities
- opportunity entities, information contained
ms.assetid: 6097776b-f5a0-47e8-9e9e-1d0259d351d4
caps.latest.revision: 20
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 83d57b16b4dfd8ebe205f6ffa9b9cbcd19ba8dc8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385674"
---
# <a name="opportunity-entities"></a><span data-ttu-id="9ab64-104">Opportunity entities</span><span class="sxs-lookup"><span data-stu-id="9ab64-104">Opportunity entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9ab64-105">The *opportunity* entity represents a potential sale to new or established customers.</span><span class="sxs-lookup"><span data-stu-id="9ab64-105">The *opportunity* entity represents a potential sale to new or established customers.</span></span> <span data-ttu-id="9ab64-106">It helps you to forecast future business demands and sales revenues.</span><span class="sxs-lookup"><span data-stu-id="9ab64-106">It helps you to forecast future business demands and sales revenues.</span></span> <span data-ttu-id="9ab64-107">You can create a new opportunity in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] to monitor an inquiry from your existing customer, or convert a qualified lead into an opportunity.</span><span class="sxs-lookup"><span data-stu-id="9ab64-107">You can create a new opportunity in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] to monitor an inquiry from your existing customer, or convert a qualified lead into an opportunity.</span></span> <span data-ttu-id="9ab64-108">Salespeople often use opportunities to keep track of the sales engagements that they are currently working on.</span><span class="sxs-lookup"><span data-stu-id="9ab64-108">Salespeople often use opportunities to keep track of the sales engagements that they are currently working on.</span></span>  
  
 <span data-ttu-id="9ab64-109">You can track the estimated revenue, estimated close date, and rating of the opportunity as well as what stage the opportunity is in.</span><span class="sxs-lookup"><span data-stu-id="9ab64-109">You can track the estimated revenue, estimated close date, and rating of the opportunity as well as what stage the opportunity is in.</span></span> <span data-ttu-id="9ab64-110">You can track the potential customer’s name and salesperson’s name.</span><span class="sxs-lookup"><span data-stu-id="9ab64-110">You can track the potential customer’s name and salesperson’s name.</span></span> <span data-ttu-id="9ab64-111">You can monitor activities related to the potential sale, such as telephone calls, email messages, and tasks.</span><span class="sxs-lookup"><span data-stu-id="9ab64-111">You can monitor activities related to the potential sale, such as telephone calls, email messages, and tasks.</span></span>  
  
 <span data-ttu-id="9ab64-112">An opportunity must be associated with one account or contact.</span><span class="sxs-lookup"><span data-stu-id="9ab64-112">An opportunity must be associated with one account or contact.</span></span> <span data-ttu-id="9ab64-113">An account and a contact may have links to multiple opportunities.</span><span class="sxs-lookup"><span data-stu-id="9ab64-113">An account and a contact may have links to multiple opportunities.</span></span> <span data-ttu-id="9ab64-114">Opportunities contain competitor information that helps you to analyze and find effective selling strategies.</span><span class="sxs-lookup"><span data-stu-id="9ab64-114">Opportunities contain competitor information that helps you to analyze and find effective selling strategies.</span></span>  
  
 <span data-ttu-id="9ab64-115">Each opportunity may have multiple products associated with it.</span><span class="sxs-lookup"><span data-stu-id="9ab64-115">Each opportunity may have multiple products associated with it.</span></span> <span data-ttu-id="9ab64-116">An association between an opportunity and a product is represented by the opportunity product entity.</span><span class="sxs-lookup"><span data-stu-id="9ab64-116">An association between an opportunity and a product is represented by the opportunity product entity.</span></span>  
  
 <span data-ttu-id="9ab64-117">After you determine whether the prospective customer or an existing customer wants to purchase your product or service, you may close an opportunity.</span><span class="sxs-lookup"><span data-stu-id="9ab64-117">After you determine whether the prospective customer or an existing customer wants to purchase your product or service, you may close an opportunity.</span></span> <span data-ttu-id="9ab64-118">By closing an opportunity, you deactivate it, but you do not delete it.</span><span class="sxs-lookup"><span data-stu-id="9ab64-118">By closing an opportunity, you deactivate it, but you do not delete it.</span></span> <span data-ttu-id="9ab64-119">This gives you an option to reopen it later.</span><span class="sxs-lookup"><span data-stu-id="9ab64-119">This gives you an option to reopen it later.</span></span> <span data-ttu-id="9ab64-120">When you close an opportunity, an opportunity close activity is created.</span><span class="sxs-lookup"><span data-stu-id="9ab64-120">When you close an opportunity, an opportunity close activity is created.</span></span> <span data-ttu-id="9ab64-121">It is represented by the opportunity close entity.</span><span class="sxs-lookup"><span data-stu-id="9ab64-121">It is represented by the opportunity close entity.</span></span> <span data-ttu-id="9ab64-122">You can use this entity to store information about the revenue, why you closed the opportunity, close date, and the competitor.</span><span class="sxs-lookup"><span data-stu-id="9ab64-122">You can use this entity to store information about the revenue, why you closed the opportunity, close date, and the competitor.</span></span> <span data-ttu-id="9ab64-123">It also contains the information about the user that created the opportunity.</span><span class="sxs-lookup"><span data-stu-id="9ab64-123">It also contains the information about the user that created the opportunity.</span></span>  
  
 <span data-ttu-id="9ab64-124">The entities that can be associated with an opportunity to provide a complete set of information about the sales engagement include: activities, notes and attachments, competitors, quotes, orders, and sales literature.</span><span class="sxs-lookup"><span data-stu-id="9ab64-124">The entities that can be associated with an opportunity to provide a complete set of information about the sales engagement include: activities, notes and attachments, competitors, quotes, orders, and sales literature.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="9ab64-125">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9ab64-125">See also</span></span>  
 <span data-ttu-id="9ab64-126">[Creating an Opportunity](create-opportunity.md) </span><span class="sxs-lookup"><span data-stu-id="9ab64-126">[Creating an Opportunity](create-opportunity.md) </span></span>  
 <span data-ttu-id="9ab64-127">[Converting an Opportunity to a Quote, Sales Order or Invoice](convert-opportunity-quote-sales-order-invoice.md) </span><span class="sxs-lookup"><span data-stu-id="9ab64-127">[Converting an Opportunity to a Quote, Sales Order or Invoice](convert-opportunity-quote-sales-order-invoice.md) </span></span>  
 <span data-ttu-id="9ab64-128">[Opportunity Entity](entities/opportunity.md) </span><span class="sxs-lookup"><span data-stu-id="9ab64-128">[Opportunity Entity](entities/opportunity.md) </span></span>  
 <span data-ttu-id="9ab64-129">[OpportunityProduct Entity](entities/opportunityproduct.md) </span><span class="sxs-lookup"><span data-stu-id="9ab64-129">[OpportunityProduct Entity](entities/opportunityproduct.md) </span></span>  
 <span data-ttu-id="9ab64-130">[OpportunityClose Entity](entities/opportunityclose.md) </span><span class="sxs-lookup"><span data-stu-id="9ab64-130">[OpportunityClose Entity](entities/opportunityclose.md) </span></span>  
 <span data-ttu-id="9ab64-131">[Sample: Create an Opportunity (Early Bound)](sample-create-opportunity-early-bound.md) </span><span class="sxs-lookup"><span data-stu-id="9ab64-131">[Sample: Create an Opportunity (Early Bound)](sample-create-opportunity-early-bound.md) </span></span>  
 <span data-ttu-id="9ab64-132">[Sample: Retrieve an Opportunity (Early Bound)](sample-retrieve-opportunity-early-bound.md) </span><span class="sxs-lookup"><span data-stu-id="9ab64-132">[Sample: Retrieve an Opportunity (Early Bound)](sample-retrieve-opportunity-early-bound.md) </span></span>  
 <span data-ttu-id="9ab64-133">[Sample: Convert an Opportunity to a Quote (Early Bound)](sample-convert-opportunity-quote-early-bound.md) </span><span class="sxs-lookup"><span data-stu-id="9ab64-133">[Sample: Convert an Opportunity to a Quote (Early Bound)](sample-convert-opportunity-quote-early-bound.md) </span></span>  
 <span data-ttu-id="9ab64-134">[Thực thể bán hàng](sales-entities-lead-opportunity-competitor-quote-order-invoice.md) </span><span class="sxs-lookup"><span data-stu-id="9ab64-134">[Sales Entities](sales-entities-lead-opportunity-competitor-quote-order-invoice.md) </span></span>  
 <span data-ttu-id="9ab64-135">[Quote, order, and invoice entities](quote-order-invoice-entities.md) </span><span class="sxs-lookup"><span data-stu-id="9ab64-135">[Quote, order, and invoice entities](quote-order-invoice-entities.md) </span></span>  
 [<span data-ttu-id="9ab64-136">Set default price level for opportunity, quote, order, invoice</span><span class="sxs-lookup"><span data-stu-id="9ab64-136">Set default price level for opportunity, quote, order, invoice</span></span>](set-default-price-level-for-opportunity-quote-order-invoice.md)
