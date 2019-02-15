---
title: Convert an opportunity to a quote, sales order or invoice (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about converting an opportunity to a quote, sales order, or invoice.
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
- converting an opportunity to a quote; sales order; or invoice, messages to use
- opportunity entities, converting an opportunity to a quote; sales order; or invoice
ms.assetid: b350a766-5369-4a74-a1fc-573f03fa24e4
caps.latest.revision: 26
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3a18a6381add368be008c1967b8b42a001f1d320
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388518"
---
# <a name="convert-an-opportunity-to-a-quote-sales-order-or-invoice"></a><span data-ttu-id="4c23e-103">Convert an opportunity to a quote, sales order or invoice</span><span class="sxs-lookup"><span data-stu-id="4c23e-103">Convert an opportunity to a quote, sales order or invoice</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="4c23e-104">Opportunities, quotes, sales orders, and invoices are all part of the sales process.</span><span class="sxs-lookup"><span data-stu-id="4c23e-104">Opportunities, quotes, sales orders, and invoices are all part of the sales process.</span></span> <span data-ttu-id="4c23e-105">An opportunity is a possibility to sell products and services to a qualified customer.</span><span class="sxs-lookup"><span data-stu-id="4c23e-105">An opportunity is a possibility to sell products and services to a qualified customer.</span></span> <span data-ttu-id="4c23e-106">If an opportunity is won, you may convert it to a quote, or to a sales order or an invoice.</span><span class="sxs-lookup"><span data-stu-id="4c23e-106">If an opportunity is won, you may convert it to a quote, or to a sales order or an invoice.</span></span> <span data-ttu-id="4c23e-107">The catalog products and write-in products that are included in an opportunity are added to a quote, a sales order, or an invoice during conversion.</span><span class="sxs-lookup"><span data-stu-id="4c23e-107">The catalog products and write-in products that are included in an opportunity are added to a quote, a sales order, or an invoice during conversion.</span></span> <span data-ttu-id="4c23e-108">An opportunity, a quote, a sales order, and an invoice share common data that can be reused in the flow of the sales process.</span><span class="sxs-lookup"><span data-stu-id="4c23e-108">An opportunity, a quote, a sales order, and an invoice share common data that can be reused in the flow of the sales process.</span></span> <span data-ttu-id="4c23e-109">The shared data includes user information, product price and discounts, freight amount, total costs, and tax.</span><span class="sxs-lookup"><span data-stu-id="4c23e-109">The shared data includes user information, product price and discounts, freight amount, total costs, and tax.</span></span>  
  
## <a name="converting-an-opportunity-to-a-quote-a-sales-order-or-an-invoice"></a><span data-ttu-id="4c23e-110">Converting an Opportunity to a Quote, a Sales Order, or an Invoice</span><span class="sxs-lookup"><span data-stu-id="4c23e-110">Converting an Opportunity to a Quote, a Sales Order, or an Invoice</span></span>  
 <span data-ttu-id="4c23e-111">The following table lists the messages that you can use to convert an opportunity to a quote, a sales order, or an invoice.</span><span class="sxs-lookup"><span data-stu-id="4c23e-111">The following table lists the messages that you can use to convert an opportunity to a quote, a sales order, or an invoice.</span></span>  
  
|<span data-ttu-id="4c23e-112">Thông báo</span><span class="sxs-lookup"><span data-stu-id="4c23e-112">Message</span></span>|<span data-ttu-id="4c23e-113">Mô tả</span><span class="sxs-lookup"><span data-stu-id="4c23e-113">Description</span></span>|  
|-------------|-----------------|  
|<xref:Microsoft.Crm.Sdk.Messages.GenerateQuoteFromOpportunityRequest>|<span data-ttu-id="4c23e-114">Generates a quote from an opportunity.</span><span class="sxs-lookup"><span data-stu-id="4c23e-114">Generates a quote from an opportunity.</span></span>|  
|<xref:Microsoft.Crm.Sdk.Messages.GenerateSalesOrderFromOpportunityRequest>|<span data-ttu-id="4c23e-115">Generates a sales order from an opportunity.</span><span class="sxs-lookup"><span data-stu-id="4c23e-115">Generates a sales order from an opportunity.</span></span>|  
|<xref:Microsoft.Crm.Sdk.Messages.GenerateInvoiceFromOpportunityRequest>|<span data-ttu-id="4c23e-116">Generates an invoice from an opportunity.</span><span class="sxs-lookup"><span data-stu-id="4c23e-116">Generates an invoice from an opportunity.</span></span>|  
  
## <a name="copying-products-from-an-opportunity-to-a-quote-a-sales-order-or-on-invoice"></a><span data-ttu-id="4c23e-117">Copying Products from an Opportunity to a Quote, a Sales Order, or on Invoice</span><span class="sxs-lookup"><span data-stu-id="4c23e-117">Copying Products from an Opportunity to a Quote, a Sales Order, or on Invoice</span></span>  
 <span data-ttu-id="4c23e-118">The following table lists the messages that you can use to add products from a new opportunity to existing quotes, invoices, or sales orders.</span><span class="sxs-lookup"><span data-stu-id="4c23e-118">The following table lists the messages that you can use to add products from a new opportunity to existing quotes, invoices, or sales orders.</span></span>  
  
|<span data-ttu-id="4c23e-119">Thông báo</span><span class="sxs-lookup"><span data-stu-id="4c23e-119">Message</span></span>|<span data-ttu-id="4c23e-120">Mô tả</span><span class="sxs-lookup"><span data-stu-id="4c23e-120">Description</span></span>|  
|-------------|-----------------|  
|<xref:Microsoft.Crm.Sdk.Messages.GetQuoteProductsFromOpportunityRequest>|<span data-ttu-id="4c23e-121">Retrieves the products from an opportunity and copies them to the specified quote.</span><span class="sxs-lookup"><span data-stu-id="4c23e-121">Retrieves the products from an opportunity and copies them to the specified quote.</span></span>|  
|<xref:Microsoft.Crm.Sdk.Messages.GetSalesOrderProductsFromOpportunityRequest>|<span data-ttu-id="4c23e-122">Retrieves the products from an opportunity and copies them to the specified sales order.</span><span class="sxs-lookup"><span data-stu-id="4c23e-122">Retrieves the products from an opportunity and copies them to the specified sales order.</span></span>|  
|<xref:Microsoft.Crm.Sdk.Messages.GetInvoiceProductsFromOpportunityRequest>|<span data-ttu-id="4c23e-123">Retrieves the products from an opportunity and copies them to the specified invoice.</span><span class="sxs-lookup"><span data-stu-id="4c23e-123">Retrieves the products from an opportunity and copies them to the specified invoice.</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="4c23e-124">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="4c23e-124">See also</span></span>  
 <span data-ttu-id="4c23e-125">[Opportunity Entities](opportunity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="4c23e-125">[Opportunity Entities](opportunity-entities.md) </span></span>  
 <span data-ttu-id="4c23e-126">[Creating an Opportunity](create-opportunity.md) </span><span class="sxs-lookup"><span data-stu-id="4c23e-126">[Creating an Opportunity](create-opportunity.md) </span></span>  
 <span data-ttu-id="4c23e-127">[Quote, Order and Invoice Entities](quote-order-invoice-entities.md) </span><span class="sxs-lookup"><span data-stu-id="4c23e-127">[Quote, Order and Invoice Entities](quote-order-invoice-entities.md) </span></span>  
 <span data-ttu-id="4c23e-128">[Thực thể bán hàng](sales-entities-lead-opportunity-competitor-quote-order-invoice.md) </span><span class="sxs-lookup"><span data-stu-id="4c23e-128">[Sales Entities](sales-entities-lead-opportunity-competitor-quote-order-invoice.md) </span></span>  
 [<span data-ttu-id="4c23e-129">Opportunity Entity</span><span class="sxs-lookup"><span data-stu-id="4c23e-129">Opportunity Entity</span></span>](entities/opportunity.md)
