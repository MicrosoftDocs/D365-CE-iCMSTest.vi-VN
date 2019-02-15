---
title: Set default price level for opportunity, quote, order, and invoice (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Automatically set a default price level (price list) for an opportunity, quote, order, or invoice based on the sales territory of the user who creates or updates that entity.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: ba21b67a-bc6c-4082-8f67-ab0b20c8ffbc
caps.latest.revision: 14
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 23844c8ba7acfb6a996839ed316390ee732af8f5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385934"
---
# <a name="set-default-price-level-for-opportunity-quote-order-and-invoice"></a><span data-ttu-id="2dc65-103">Set default price level for opportunity, quote, order, and invoice</span><span class="sxs-lookup"><span data-stu-id="2dc65-103">Set default price level for opportunity, quote, order, and invoice</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="2dc65-104">You can automatically set a default price level (price list) for an opportunity, quote, order, or invoice based on the sales territory of the user who creates or updates the opportunity, quote, order, or invoice record.</span><span class="sxs-lookup"><span data-stu-id="2dc65-104">You can automatically set a default price level (price list) for an opportunity, quote, order, or invoice based on the sales territory of the user who creates or updates the opportunity, quote, order, or invoice record.</span></span>  
  
<a name="Enable"></a>   
## <a name="enable-automatic-selection-of-default-price-level"></a><span data-ttu-id="2dc65-105">Enable automatic selection of default price level</span><span class="sxs-lookup"><span data-stu-id="2dc65-105">Enable automatic selection of default price level</span></span>  
 <span data-ttu-id="2dc65-106">To enable selection of default price level for opportunities, quotes, orders, or invoices based on the sales territory relationship, the following conditions must be true:</span><span class="sxs-lookup"><span data-stu-id="2dc65-106">To enable selection of default price level for opportunities, quotes, orders, or invoices based on the sales territory relationship, the following conditions must be true:</span></span>  
  
- <span data-ttu-id="2dc65-107">The value of the `Organization.UseInbuiltRuleForDefaultPriceSelectionRule` attribute is set to 1 (true).</span><span class="sxs-lookup"><span data-stu-id="2dc65-107">The value of the `Organization.UseInbuiltRuleForDefaultPriceSelectionRule` attribute is set to 1 (true).</span></span> <span data-ttu-id="2dc65-108">By default, the value is set to 1 (true).</span><span class="sxs-lookup"><span data-stu-id="2dc65-108">By default, the value is set to 1 (true).</span></span>  
  
   <span data-ttu-id="2dc65-109">You can also use the **Sales** tab in the system settings area in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] to specify whether the default price level should be automatically selected for opportunities.</span><span class="sxs-lookup"><span data-stu-id="2dc65-109">You can also use the **Sales** tab in the system settings area in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] to specify whether the default price level should be automatically selected for opportunities.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="2dc65-110">[Configure product catalog information](http://go.microsoft.com/fwlink/p/?LinkId=512492)</span><span class="sxs-lookup"><span data-stu-id="2dc65-110">[Configure product catalog information](http://go.microsoft.com/fwlink/p/?LinkId=512492)</span></span>  
  
- <span data-ttu-id="2dc65-111">A price level is associated with a territory using the **Territory Default Pricelist** connection role, and the territory is assigned to the user who creates or updates the opportunity, quote, order, or invoice record.</span><span class="sxs-lookup"><span data-stu-id="2dc65-111">A price level is associated with a territory using the **Territory Default Pricelist** connection role, and the territory is assigned to the user who creates or updates the opportunity, quote, order, or invoice record.</span></span>  
  
- <span data-ttu-id="2dc65-112">The user has permission on the price level that is associated with the territory by using the **Territory Default Pricelist** connection role.</span><span class="sxs-lookup"><span data-stu-id="2dc65-112">The user has permission on the price level that is associated with the territory by using the **Territory Default Pricelist** connection role.</span></span>  
  
  [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] <span data-ttu-id="2dc65-113">internally uses the <xref:Microsoft.Crm.Sdk.Messages.GetDefaultPriceLevelRequest> message to determine the default price level for an opportunity, quote, order, or invoice based on the current user and the territory relationship with the price level.</span><span class="sxs-lookup"><span data-stu-id="2dc65-113">internally uses the <xref:Microsoft.Crm.Sdk.Messages.GetDefaultPriceLevelRequest> message to determine the default price level for an opportunity, quote, order, or invoice based on the current user and the territory relationship with the price level.</span></span> <span data-ttu-id="2dc65-114">This is how the price level is set:</span><span class="sxs-lookup"><span data-stu-id="2dc65-114">This is how the price level is set:</span></span>  
  
- <span data-ttu-id="2dc65-115">If a single price level is returned, the price level is automatically set for the opportunity, quote, order, or invoice record that the user is creating or updating.</span><span class="sxs-lookup"><span data-stu-id="2dc65-115">If a single price level is returned, the price level is automatically set for the opportunity, quote, order, or invoice record that the user is creating or updating.</span></span>  
  
- <span data-ttu-id="2dc65-116">If multiple price levels are returned, the price level field isn’t populated and the user must specify a price level for the opportunity, quote, order, or invoice record.</span><span class="sxs-lookup"><span data-stu-id="2dc65-116">If multiple price levels are returned, the price level field isn’t populated and the user must specify a price level for the opportunity, quote, order, or invoice record.</span></span>  
  
<a name="Disable"></a>   
## <a name="disable-automatic-selection-of-default-price-level"></a><span data-ttu-id="2dc65-117">Disable automatic selection of default price level</span><span class="sxs-lookup"><span data-stu-id="2dc65-117">Disable automatic selection of default price level</span></span>  
 <span data-ttu-id="2dc65-118">You can turn off the automatic selection of a default price level for your opportunity, quote, order, or invoice by setting the value of the `Organization.UseInbuiltRuleForDefaultPriceSelectionRule` attribute to 0 (`false`), or by using the **Sales** tab in the system settings area in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)].</span><span class="sxs-lookup"><span data-stu-id="2dc65-118">You can turn off the automatic selection of a default price level for your opportunity, quote, order, or invoice by setting the value of the `Organization.UseInbuiltRuleForDefaultPriceSelectionRule` attribute to 0 (`false`), or by using the **Sales** tab in the system settings area in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="2dc65-119">[Configure product catalog information](http://go.microsoft.com/fwlink/p/?LinkId=512492)</span><span class="sxs-lookup"><span data-stu-id="2dc65-119">[Configure product catalog information](http://go.microsoft.com/fwlink/p/?LinkId=512492)</span></span>  
  
<a name="Extend"></a>   
## <a name="extend-default-price-level-selection"></a><span data-ttu-id="2dc65-120">Extend default price level selection</span><span class="sxs-lookup"><span data-stu-id="2dc65-120">Extend default price level selection</span></span>  
 <span data-ttu-id="2dc65-121">Instead of using the out-of-box rule for the selection of default price level for an opportunity, quote, order, and invoice, you can use the <xref:Microsoft.Crm.Sdk.Messages.GetDefaultPriceLevelRequest> message to specify your custom logic for selecting default price level.</span><span class="sxs-lookup"><span data-stu-id="2dc65-121">Instead of using the out-of-box rule for the selection of default price level for an opportunity, quote, order, and invoice, you can use the <xref:Microsoft.Crm.Sdk.Messages.GetDefaultPriceLevelRequest> message to specify your custom logic for selecting default price level.</span></span>  
  
> [!NOTE]
> [!INCLUDE[cc_feature_included_with_2015_update_1_admins](../includes/cc-feature-included-with-2015-update-1-admins.md)]  
  
 <span data-ttu-id="2dc65-122">To extend the default price level selection:</span><span class="sxs-lookup"><span data-stu-id="2dc65-122">To extend the default price level selection:</span></span>  
  
1. <span data-ttu-id="2dc65-123">Ensure that the value of the `Organization.UseInbuiltRuleForDefaultPriceSelectionRule` attribute is set to 1 (true).</span><span class="sxs-lookup"><span data-stu-id="2dc65-123">Ensure that the value of the `Organization.UseInbuiltRuleForDefaultPriceSelectionRule` attribute is set to 1 (true).</span></span>  
  
2. <span data-ttu-id="2dc65-124">Create a plug-in that contains custom code for returning price levels based on your business requirement.</span><span class="sxs-lookup"><span data-stu-id="2dc65-124">Create a plug-in that contains custom code for returning price levels based on your business requirement.</span></span>  
  
3. <span data-ttu-id="2dc65-125">Register the plug-in on the `GetDefaultPriceLevel` message.</span><span class="sxs-lookup"><span data-stu-id="2dc65-125">Register the plug-in on the `GetDefaultPriceLevel` message.</span></span>  
  
   <span data-ttu-id="2dc65-126">When you register a plug-in on the `GetDefaultPriceLevel` message, every time you create an opportunity, quote, order, or invoice record in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], the plug-in is executed to return the price level based on your custom code.</span><span class="sxs-lookup"><span data-stu-id="2dc65-126">When you register a plug-in on the `GetDefaultPriceLevel` message, every time you create an opportunity, quote, order, or invoice record in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], the plug-in is executed to return the price level based on your custom code.</span></span>  
  
-   <span data-ttu-id="2dc65-127">If a single price level is returned as a result of the plug-in execution, the price level is set for the opportunity, quote, order, or invoice record that the user is creating.</span><span class="sxs-lookup"><span data-stu-id="2dc65-127">If a single price level is returned as a result of the plug-in execution, the price level is set for the opportunity, quote, order, or invoice record that the user is creating.</span></span>  
  
-   <span data-ttu-id="2dc65-128">If multiple price levels are returned as a result of the plug-in execution, the price level field is not populated and the user specifies a price level for the opportunity, quote, order, or invoice record.</span><span class="sxs-lookup"><span data-stu-id="2dc65-128">If multiple price levels are returned as a result of the plug-in execution, the price level field is not populated and the user specifies a price level for the opportunity, quote, order, or invoice record.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2dc65-129">When you extend the default price level selection by registering a plug-in on the `GetDefaultPriceLevel` message, the out-of-box selection of price level is disabled.</span><span class="sxs-lookup"><span data-stu-id="2dc65-129">When you extend the default price level selection by registering a plug-in on the `GetDefaultPriceLevel` message, the out-of-box selection of price level is disabled.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="2dc65-130">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="2dc65-130">See also</span></span>  
 <span data-ttu-id="2dc65-131">[PriceLevel Entity](entities/pricelevel.md) </span><span class="sxs-lookup"><span data-stu-id="2dc65-131">[PriceLevel Entity](entities/pricelevel.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.GetDefaultPriceLevelRequest>   
 <span data-ttu-id="2dc65-132">[Territory Entity](entities/territory.md) </span><span class="sxs-lookup"><span data-stu-id="2dc65-132">[Territory Entity](entities/territory.md) </span></span>  
 <span data-ttu-id="2dc65-133">[Opportunity Entities](opportunity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="2dc65-133">[Opportunity Entities](opportunity-entities.md) </span></span>  
 <span data-ttu-id="2dc65-134">[Quote, order, and invoice entities](quote-order-invoice-entities.md) </span><span class="sxs-lookup"><span data-stu-id="2dc65-134">[Quote, order, and invoice entities](quote-order-invoice-entities.md) </span></span>  
 [<span data-ttu-id="2dc65-135">Write a Plug-in</span><span class="sxs-lookup"><span data-stu-id="2dc65-135">Write a Plug-in</span></span>](write-plugin.md)
