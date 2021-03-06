---
title: 'Sample: Process quotes, sales orders and invoices (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to convert an opportunity that is won to a quote, then convert a quote to a sales order, and then convert a sales order to an invoice.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- sales entities sample, converting opportunities to sales orders
- quote; order; and invoice entities sample, locking and unlocking sales orders and invoice prices
- sample for converting opportunities to sales orders, sales entities sample
- sample for locking and unlocking sales orders and invoice prices, quote; order; and invoice entities
ms.assetid: 7cf7de1a-789b-4c87-a6c3-6410a68369a1
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4e516a32612eed9937ebeb08770a1de9ab83e9d6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385676"
---
# <a name="sample-process-quotes-sales-orders-and-invoices"></a>Sample: Process quotes, sales orders and invoices

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample here [Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).   

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to convert an opportunity that is won to a quote, then convert a quote to a sales order, and then convert a sales order to an invoice. It also shows how to lock and unlock the sales order and the invoice prices.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[BusinessManagement#ProcessingQuotesAndSalesOrders](../snippets/csharp/CRMV8/businessmanagement/cs/processingquotesandsalesorders.cs#processingquotesandsalesorders)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sales Entities (Lead, Opportunity, Competitor, Quote, Order, Invoice)](sales-entities-lead-opportunity-competitor-quote-order-invoice.md)   
 [Quote, Order and Invoice Entities](quote-order-invoice-entities.md)   
 [Sample: Fulfill a Sales Order](sample-fulfill-sales-order.md)   
 <xref:Microsoft.Crm.Sdk.Messages.WinQuoteRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.ConvertQuoteToSalesOrderRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.UnlockSalesOrderPricingRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.LockSalesOrderPricingRequest>
