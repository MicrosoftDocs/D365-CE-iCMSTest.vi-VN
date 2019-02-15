---
title: Quote, order, and invoice entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about quote, sales order (order), and invoice building.
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
- sales order (order), definition
- quote; order; and invoice entities, introduction
- quote close activity, definition
- quote, definition
- invoice, definition
- order entity, introduction
- quote detail (quote product), definition
- invoice entity, introduction
ms.assetid: 1ad567c4-6065-48ab-a277-15fbcc5a9d1a
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e51c56c78ea3b0436ce0c86d3641206893580328
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387271"
---
# <a name="quote-order-and-invoice-entities"></a><span data-ttu-id="95348-103">Quote, order, and invoice entities</span><span class="sxs-lookup"><span data-stu-id="95348-103">Quote, order, and invoice entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] <span data-ttu-id="95348-104">supports robust *quote*, *sales order (order)*, and *invoice* building.</span><span class="sxs-lookup"><span data-stu-id="95348-104">supports robust *quote*, *sales order (order)*, and *invoice* building.</span></span> <span data-ttu-id="95348-105">You can build a quote by selecting products directly from the product catalog, specifying the price list (such as wholesale or retail), and entering the requested number of units.</span><span class="sxs-lookup"><span data-stu-id="95348-105">You can build a quote by selecting products directly from the product catalog, specifying the price list (such as wholesale or retail), and entering the requested number of units.</span></span> <span data-ttu-id="95348-106">If you have permission, you can also apply discounts.</span><span class="sxs-lookup"><span data-stu-id="95348-106">If you have permission, you can also apply discounts.</span></span> <span data-ttu-id="95348-107">Multiple pricing models are supported, such as wholesale versus retail, and discounting can be done by line item based on volume or manual override.</span><span class="sxs-lookup"><span data-stu-id="95348-107">Multiple pricing models are supported, such as wholesale versus retail, and discounting can be done by line item based on volume or manual override.</span></span> <span data-ttu-id="95348-108">In addition, overall discounts can be applied to the whole quote.</span><span class="sxs-lookup"><span data-stu-id="95348-108">In addition, overall discounts can be applied to the whole quote.</span></span>  
  
 <span data-ttu-id="95348-109">A quote is a formal offer for products or services proposed at specific prices and related payment terms that is sent to a prospective customer.</span><span class="sxs-lookup"><span data-stu-id="95348-109">A quote is a formal offer for products or services proposed at specific prices and related payment terms that is sent to a prospective customer.</span></span> <span data-ttu-id="95348-110">You can create a quote, save it as a draft, and specify whether it is active (presented to the customer) or closed (completed, either as an order or not).</span><span class="sxs-lookup"><span data-stu-id="95348-110">You can create a quote, save it as a draft, and specify whether it is active (presented to the customer) or closed (completed, either as an order or not).</span></span> <span data-ttu-id="95348-111">A quote can have a due date (when it was promised to the customer), effective dates (when it must be accepted or rejected by), and the requested delivery dates.</span><span class="sxs-lookup"><span data-stu-id="95348-111">A quote can have a due date (when it was promised to the customer), effective dates (when it must be accepted or rejected by), and the requested delivery dates.</span></span> <span data-ttu-id="95348-112">In addition, a quote can contain many "ship to" addresses (by line item) or a "will call" setting for items to be picked up by the customer.</span><span class="sxs-lookup"><span data-stu-id="95348-112">In addition, a quote can contain many "ship to" addresses (by line item) or a "will call" setting for items to be picked up by the customer.</span></span>  
  
 <span data-ttu-id="95348-113">If a quote is created from an opportunity, [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] will use the products associated with the opportunity as the basis for the draft.</span><span class="sxs-lookup"><span data-stu-id="95348-113">If a quote is created from an opportunity, [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] will use the products associated with the opportunity as the basis for the draft.</span></span> <span data-ttu-id="95348-114">When a quote is converted to an order, the user can keep the opportunity open or close it.</span><span class="sxs-lookup"><span data-stu-id="95348-114">When a quote is converted to an order, the user can keep the opportunity open or close it.</span></span> <span data-ttu-id="95348-115">If the user closes it, the final revenue amount is recorded.</span><span class="sxs-lookup"><span data-stu-id="95348-115">If the user closes it, the final revenue amount is recorded.</span></span>  
  
 <span data-ttu-id="95348-116">A quote can be associated with the following entities:</span><span class="sxs-lookup"><span data-stu-id="95348-116">A quote can be associated with the following entities:</span></span>  
  
- <span data-ttu-id="95348-117">One or more products and one price list</span><span class="sxs-lookup"><span data-stu-id="95348-117">One or more products and one price list</span></span>  
  
- <span data-ttu-id="95348-118">One or more competitors</span><span class="sxs-lookup"><span data-stu-id="95348-118">One or more competitors</span></span>  
  
- <span data-ttu-id="95348-119">An opportunity</span><span class="sxs-lookup"><span data-stu-id="95348-119">An opportunity</span></span>  
  
- <span data-ttu-id="95348-120">A customer</span><span class="sxs-lookup"><span data-stu-id="95348-120">A customer</span></span>  
  
- <span data-ttu-id="95348-121">One or more notes and attachments</span><span class="sxs-lookup"><span data-stu-id="95348-121">One or more notes and attachments</span></span>  
  
- <span data-ttu-id="95348-122">One or more customer addresses</span><span class="sxs-lookup"><span data-stu-id="95348-122">One or more customer addresses</span></span>  
  
  <span data-ttu-id="95348-123">The `quote detail (quote product)` entity represents a line item in a quote.</span><span class="sxs-lookup"><span data-stu-id="95348-123">The `quote detail (quote product)` entity represents a line item in a quote.</span></span> <span data-ttu-id="95348-124">Each quote can have multiple quote detail (quote product) records.</span><span class="sxs-lookup"><span data-stu-id="95348-124">Each quote can have multiple quote detail (quote product) records.</span></span>  
  
  <span data-ttu-id="95348-125">The `quote close activity` entity represents an activity that is generated when a quote is closed.</span><span class="sxs-lookup"><span data-stu-id="95348-125">The `quote close activity` entity represents an activity that is generated when a quote is closed.</span></span>  
  
  <span data-ttu-id="95348-126">A sales order (order) is a quote that has been accepted.</span><span class="sxs-lookup"><span data-stu-id="95348-126">A sales order (order) is a quote that has been accepted.</span></span> <span data-ttu-id="95348-127">This entity is called an order in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="95348-127">This entity is called an order in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span>  
  
  <span data-ttu-id="95348-128">An invoice is an order that has been billed.</span><span class="sxs-lookup"><span data-stu-id="95348-128">An invoice is an order that has been billed.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="95348-129">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="95348-129">See Also</span></span>  
 <span data-ttu-id="95348-130">[Quote Entity](entities/quote.md) </span><span class="sxs-lookup"><span data-stu-id="95348-130">[Quote Entity](entities/quote.md) </span></span>  
 <span data-ttu-id="95348-131">[QuoteDetail Entity](entities/quotedetail.md) </span><span class="sxs-lookup"><span data-stu-id="95348-131">[QuoteDetail Entity](entities/quotedetail.md) </span></span>  
 <span data-ttu-id="95348-132">[QuoteClose Entity](entities/quoteclose.md) </span><span class="sxs-lookup"><span data-stu-id="95348-132">[QuoteClose Entity](entities/quoteclose.md) </span></span>  
 <span data-ttu-id="95348-133">[SalesOrder Entity](entities/salesorder.md) </span><span class="sxs-lookup"><span data-stu-id="95348-133">[SalesOrder Entity](entities/salesorder.md) </span></span>  
 <span data-ttu-id="95348-134">[SalesOrderDetail Entity](entities/salesorderdetail.md) </span><span class="sxs-lookup"><span data-stu-id="95348-134">[SalesOrderDetail Entity](entities/salesorderdetail.md) </span></span>  
 <span data-ttu-id="95348-135">[OrderClose Entity](entities/orderclose.md) </span><span class="sxs-lookup"><span data-stu-id="95348-135">[OrderClose Entity](entities/orderclose.md) </span></span>  
 <span data-ttu-id="95348-136">[Invoice Entity](entities/invoice.md) </span><span class="sxs-lookup"><span data-stu-id="95348-136">[Invoice Entity](entities/invoice.md) </span></span>  
 <span data-ttu-id="95348-137">[InvoiceDetail Entity](entities/invoicedetail.md) </span><span class="sxs-lookup"><span data-stu-id="95348-137">[InvoiceDetail Entity](entities/invoicedetail.md) </span></span>  
 <span data-ttu-id="95348-138">[Sample: Set Negative Prices in Opportunities, Quotes and Sales Orders](sample-set-negative-prices-opportunities-quotes-sales-orders.md) </span><span class="sxs-lookup"><span data-stu-id="95348-138">[Sample: Set Negative Prices in Opportunities, Quotes and Sales Orders](sample-set-negative-prices-opportunities-quotes-sales-orders.md) </span></span>  
 <span data-ttu-id="95348-139">[Sample: Process Quotes, Sales Orders and Invoices](sample-process-quotes-sales-orders-invoices.md) </span><span class="sxs-lookup"><span data-stu-id="95348-139">[Sample: Process Quotes, Sales Orders and Invoices](sample-process-quotes-sales-orders-invoices.md) </span></span>  
 <span data-ttu-id="95348-140">[Sample: Fulfill a Sales Order](sample-fulfill-sales-order.md) </span><span class="sxs-lookup"><span data-stu-id="95348-140">[Sample: Fulfill a Sales Order](sample-fulfill-sales-order.md) </span></span>  
 <span data-ttu-id="95348-141">[Opportunity Entities](opportunity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="95348-141">[Opportunity Entities](opportunity-entities.md) </span></span>  
 <span data-ttu-id="95348-142">[Thực thể bán hàng](sales-entities-lead-opportunity-competitor-quote-order-invoice.md) </span><span class="sxs-lookup"><span data-stu-id="95348-142">[Sales Entities](sales-entities-lead-opportunity-competitor-quote-order-invoice.md) </span></span>  
 [<span data-ttu-id="95348-143">Set default price level for opportunity, quote, order, invoice</span><span class="sxs-lookup"><span data-stu-id="95348-143">Set default price level for opportunity, quote, order, invoice</span></span>](set-default-price-level-for-opportunity-quote-order-invoice.md)
