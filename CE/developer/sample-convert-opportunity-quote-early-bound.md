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
# <a name="sample-convert-an-opportunity-to-a-quote-early-bound"></a><span data-ttu-id="bd299-103">Sample: Convert an opportunity to a quote (early bound)</span><span class="sxs-lookup"><span data-stu-id="bd299-103">Sample: Convert an opportunity to a quote (early bound)</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="bd299-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="bd299-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="bd299-105">[Download the business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span><span class="sxs-lookup"><span data-stu-id="bd299-105">[Download the business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bd299-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="bd299-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a><span data-ttu-id="bd299-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="bd299-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="bd299-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="bd299-108">Demonstrates</span></span>  
 <span data-ttu-id="bd299-109">This sample shows how to convert an opportunity that contains products from the product catalog and a write-in product to a quote.</span><span class="sxs-lookup"><span data-stu-id="bd299-109">This sample shows how to convert an opportunity that contains products from the product catalog and a write-in product to a quote.</span></span> <span data-ttu-id="bd299-110">It also illustrates how to overwrite a price of a product from the product catalog.</span><span class="sxs-lookup"><span data-stu-id="bd299-110">It also illustrates how to overwrite a price of a product from the product catalog.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bd299-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="bd299-111">Example</span></span>  
 [!code-csharp[BusinessManagement#ConvertOpportunityToQuote](../snippets/csharp/CRMV8/businessmanagement/cs/convertopportunitytoquote.cs#convertopportunitytoquote)]  
  
### <a name="see-also"></a><span data-ttu-id="bd299-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="bd299-112">See also</span></span>  
 <span data-ttu-id="bd299-113">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="bd299-113">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
 <span data-ttu-id="bd299-114">[Opportunity Entities](opportunity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="bd299-114">[Opportunity Entities](opportunity-entities.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.GenerateQuoteFromOpportunityRequest>
