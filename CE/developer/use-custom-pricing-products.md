---
title: Use custom pricing for products (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Use the CalculatePrice message to define custom pricing for products in opportunities, quotes, orders and invoices.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: b54fd2ea-811d-4b83-8638-86dd87038fd7
caps.latest.revision: 13
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9fb9a12efe7fd147735eebe8f7b37ca3fcd374aa
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386931"
---
# <a name="use-custom-pricing-for-products"></a><span data-ttu-id="efa91-103">Use custom pricing for products</span><span class="sxs-lookup"><span data-stu-id="efa91-103">Use custom pricing for products</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="efa91-104">The pricing engine in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] supports a standard set of pricing and discounting methods, which might be limiting to your business depending on your specific requirements for applying taxation, discounts, and other pricing rules for your products.</span><span class="sxs-lookup"><span data-stu-id="efa91-104">The pricing engine in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] supports a standard set of pricing and discounting methods, which might be limiting to your business depending on your specific requirements for applying taxation, discounts, and other pricing rules for your products.</span></span> <span data-ttu-id="efa91-105">If you want to define custom pricing for your products in opportunities, quotes, orders and invoices, you can use the `CalculatePrice` message.</span><span class="sxs-lookup"><span data-stu-id="efa91-105">If you want to define custom pricing for your products in opportunities, quotes, orders and invoices, you can use the `CalculatePrice` message.</span></span>  
  
 <span data-ttu-id="efa91-106">To use the custom pricing for your opportunities, quotes, orders, and invoices:</span><span class="sxs-lookup"><span data-stu-id="efa91-106">To use the custom pricing for your opportunities, quotes, orders, and invoices:</span></span>  
  
1. <span data-ttu-id="efa91-107">Set the value of the `Organization.OOBPriceCalculationEnabled` attribute to `0` (false).</span><span class="sxs-lookup"><span data-stu-id="efa91-107">Set the value of the `Organization.OOBPriceCalculationEnabled` attribute to `0` (false).</span></span> <span data-ttu-id="efa91-108">You can also use the **Sales** tab in the system settings area in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] to disable system pricing.</span><span class="sxs-lookup"><span data-stu-id="efa91-108">You can also use the **Sales** tab in the system settings area in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] to disable system pricing.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="efa91-109">[Configure product catalog information](http://go.microsoft.com/fwlink/p/?LinkId=512492)</span><span class="sxs-lookup"><span data-stu-id="efa91-109">[Configure product catalog information](http://go.microsoft.com/fwlink/p/?LinkId=512492)</span></span>  
  
2. <span data-ttu-id="efa91-110">Create a plug-in that contains your custom pricing code for calculating the price for your opportunity, quote, order, or invoice.</span><span class="sxs-lookup"><span data-stu-id="efa91-110">Create a plug-in that contains your custom pricing code for calculating the price for your opportunity, quote, order, or invoice.</span></span>  
  
3. <span data-ttu-id="efa91-111">Register the plug-in on the `CalculatePrice` message.</span><span class="sxs-lookup"><span data-stu-id="efa91-111">Register the plug-in on the `CalculatePrice` message.</span></span>  
  
   <span data-ttu-id="efa91-112">When the `Organization.OOBPriceCalculationEnabled` attribute is set to `0`, every time an opportunity, quote, order, or invoice is created or changes, the plug-in registered on the `CalculatePrice` executes to calculate prices as specified in your custom code in the plug-in.</span><span class="sxs-lookup"><span data-stu-id="efa91-112">When the `Organization.OOBPriceCalculationEnabled` attribute is set to `0`, every time an opportunity, quote, order, or invoice is created or changes, the plug-in registered on the `CalculatePrice` executes to calculate prices as specified in your custom code in the plug-in.</span></span> <span data-ttu-id="efa91-113">The <xref:Microsoft.Crm.Sdk.Messages.CalculatePriceRequest> message doesn’t have any usage scenario of its own.</span><span class="sxs-lookup"><span data-stu-id="efa91-113">The <xref:Microsoft.Crm.Sdk.Messages.CalculatePriceRequest> message doesn’t have any usage scenario of its own.</span></span> <span data-ttu-id="efa91-114">It’s exposed so that you can plug in your own custom pricing calculation logic if you don’t want to use the out-of-box pricing provided by [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="efa91-114">It’s exposed so that you can plug in your own custom pricing calculation logic if you don’t want to use the out-of-box pricing provided by [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span>  
  
   <span data-ttu-id="efa91-115">For a sample plug-in that calculates custom pricing for opportunities, quotes, orders, and invoices, see [Sample: Calculate Price plug-in](sample-calculate-price-plugin.md).</span><span class="sxs-lookup"><span data-stu-id="efa91-115">For a sample plug-in that calculates custom pricing for opportunities, quotes, orders, and invoices, see [Sample: Calculate Price plug-in](sample-calculate-price-plugin.md).</span></span>  
  
   <span data-ttu-id="efa91-116">If you want to revert to using the out-of-box pricing for your opportunities, quotes, orders, and invoices, set the value of the `Organization.OOBPriceCalculationEnabled` attribute to `1` (true).</span><span class="sxs-lookup"><span data-stu-id="efa91-116">If you want to revert to using the out-of-box pricing for your opportunities, quotes, orders, and invoices, set the value of the `Organization.OOBPriceCalculationEnabled` attribute to `1` (true).</span></span> <span data-ttu-id="efa91-117">You can also use the **Sales** tab in the system settings area in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] or [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)] to enable system pricing.</span><span class="sxs-lookup"><span data-stu-id="efa91-117">You can also use the **Sales** tab in the system settings area in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] or [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)] to enable system pricing.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="efa91-118">[Configure product catalog information](http://go.microsoft.com/fwlink/p/?LinkId=512492)</span><span class="sxs-lookup"><span data-stu-id="efa91-118">[Configure product catalog information](http://go.microsoft.com/fwlink/p/?LinkId=512492)</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="efa91-119">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="efa91-119">See also</span></span>  
 <span data-ttu-id="efa91-120">[Product pricing methods](product-pricing-methods.md) </span><span class="sxs-lookup"><span data-stu-id="efa91-120">[Product pricing methods](product-pricing-methods.md) </span></span>  
 <span data-ttu-id="efa91-121">[Sample: Calculate Price plug-in](sample-calculate-price-plugin.md) </span><span class="sxs-lookup"><span data-stu-id="efa91-121">[Sample: Calculate Price plug-in](sample-calculate-price-plugin.md) </span></span>  
 [<span data-ttu-id="efa91-122">Product catalog entities</span><span class="sxs-lookup"><span data-stu-id="efa91-122">Product catalog entities</span></span>](product-catalog-entities.md)
