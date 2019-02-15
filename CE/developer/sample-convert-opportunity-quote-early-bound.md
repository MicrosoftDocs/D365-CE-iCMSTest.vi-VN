---
title: 'Sample: Convert an opportunity to a quote (early bound) (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to convert an opportunity that contains products from the product catalog and a write-in product to a quote.
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
- converting opportunities to quotes, Sample
- sample for converting opportunities to quotes
- sample for overwriting catalog prices when writing quotes
- overwriting catalog prices when writing quotes, Sample
ms.assetid: ba6294de-18cc-4689-8a3c-f6317305ff88
caps.latest.revision: 15
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f6ef4ff4c8bb4252ccb909affb9a575bd45dfc90
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387388"
---
# <a name="sample-convert-an-opportunity-to-a-quote-early-bound"></a>Sample: Convert an opportunity to a quote (early bound)

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. [Download the business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to convert an opportunity that contains products from the product catalog and a write-in product to a quote. It also illustrates how to overwrite a price of a product from the product catalog.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[BusinessManagement#ConvertOpportunityToQuote](../snippets/csharp/CRMV8/businessmanagement/cs/convertopportunitytoquote.cs#convertopportunitytoquote)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md)   
 [Opportunity Entities](opportunity-entities.md)   
 <xref:Microsoft.Crm.Sdk.Messages.GenerateQuoteFromOpportunityRequest>
