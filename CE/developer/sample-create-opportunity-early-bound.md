---
title: 'Sample: Create an opportunity (early bound) (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to create an opportunity that contains a product from the product catalog.
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
- creating opportunities from products in the catalog, Sample
- sample for creating opportunities from products in the catalog
ms.assetid: 005993c4-468b-4b55-a555-833b4ead0d43
caps.latest.revision: 15
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f08e55aea74e417d63d73d5b9cb8e60bec7e4cd8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386523"
---
# <a name="sample-create-an-opportunity-early-bound"></a>Sample: Create an opportunity (early bound)

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. [Download the Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62)

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create an opportunity that contains a product from the product catalog and from a write-in product.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[BusinessManagement#CreateOpportunity](../snippets/csharp/CRMV8/businessmanagement/cs/createopportunity.cs#createopportunity)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md)   
 [Opportunity Entities](opportunity-entities.md)   
 [Sample: Retrieve an Opportunity (Early Bound)](sample-retrieve-opportunity-early-bound.md)
