---
title: 'Sample: Fulfill a sales order (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to create a sales order and then close it by fulfilling it.
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
- order entities sample, creating and closing sales orders
- sample for creating and closing sales orders, order entities sample
ms.assetid: 21eb9416-6c1f-468e-98f6-96d098d23051
caps.latest.revision: 13
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 37ff7f4ddc6acd75296f231f20f3a3f8419353e9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386421"
---
# <a name="sample-fulfill-a-sales-order"></a>Sample: Fulfill a sales order

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample here [Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62). 

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create a sales order and then close it by fulfilling it.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[BusinessManagement#FulfillSalesOrder](../snippets/csharp/CRMV8/businessmanagement/cs/fulfillsalesorder.cs#fulfillsalesorder)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sales Entities (Lead, Opportunity, Competitor, Quote, Order, Invoice)](sales-entities-lead-opportunity-competitor-quote-order-invoice.md)   
 [Quote, order, and invoice entities](quote-order-invoice-entities.md)   
 <xref:Microsoft.Crm.Sdk.Messages.FulfillSalesOrderRequest>
