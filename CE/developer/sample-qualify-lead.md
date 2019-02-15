---
title: 'Sample: Qualify a lead (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to qualify a lead and create an account, contact, or opportunity.
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
- sample for qualifying leads
- qualifying leads, sample
- creating lead-based accounts; contacts; or opportunities, sample
- sample that creates lead-based accounts; contacts; or opportunities
ms.assetid: fb89b821-ed96-4a24-bae9-3e217f2cf1dc
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 950aa5f22194a42be1e7177e15301a300ec47f78
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385708"
---
# <a name="sample-qualify-a-lead"></a>Sample: Qualify a lead

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample here [Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to qualify a lead and create an account, contact, or opportunity based on the lead.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[BusinessManagement#WorkingWithLeads](../snippets/csharp/CRMV8/businessmanagement/cs/workingwithleads.cs#workingwithleads)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sales Entities (Lead, Opportunity, Competitor, Quote, Order, Invoice)](sales-entities-lead-opportunity-competitor-quote-order-invoice.md)   
 <xref:Microsoft.Crm.Sdk.Messages.QualifyLeadRequest>   
 [Lead Entity](lead-entity.md)
