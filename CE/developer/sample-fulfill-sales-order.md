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
# <a name="sample-fulfill-a-sales-order"></a><span data-ttu-id="39328-103">Sample: Fulfill a sales order</span><span class="sxs-lookup"><span data-stu-id="39328-103">Sample: Fulfill a sales order</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="39328-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="39328-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="39328-105">Download the complete sample here [Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span><span class="sxs-lookup"><span data-stu-id="39328-105">Download the complete sample here [Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="39328-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="39328-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a><span data-ttu-id="39328-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="39328-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="39328-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="39328-108">Demonstrates</span></span>  
 <span data-ttu-id="39328-109">This sample shows how to create a sales order and then close it by fulfilling it.</span><span class="sxs-lookup"><span data-stu-id="39328-109">This sample shows how to create a sales order and then close it by fulfilling it.</span></span>  
  
## <a name="example"></a><span data-ttu-id="39328-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="39328-110">Example</span></span>  
 [!code-csharp[BusinessManagement#FulfillSalesOrder](../snippets/csharp/CRMV8/businessmanagement/cs/fulfillsalesorder.cs#fulfillsalesorder)]  
  
### <a name="see-also"></a><span data-ttu-id="39328-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="39328-111">See also</span></span>  
 <span data-ttu-id="39328-112">[Sales Entities (Lead, Opportunity, Competitor, Quote, Order, Invoice)](sales-entities-lead-opportunity-competitor-quote-order-invoice.md) </span><span class="sxs-lookup"><span data-stu-id="39328-112">[Sales Entities (Lead, Opportunity, Competitor, Quote, Order, Invoice)](sales-entities-lead-opportunity-competitor-quote-order-invoice.md) </span></span>  
 <span data-ttu-id="39328-113">[Quote, order, and invoice entities](quote-order-invoice-entities.md) </span><span class="sxs-lookup"><span data-stu-id="39328-113">[Quote, order, and invoice entities](quote-order-invoice-entities.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.FulfillSalesOrderRequest>
