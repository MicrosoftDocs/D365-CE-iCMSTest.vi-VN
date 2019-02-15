---
title: 'Sample: Search and retrieve articles (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: The sample code demonstrates how to search by body, keyword, and title, and retrieve articles by topic incident subject and topic incident product.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 50692599-5afe-45b4-b2b6-f9ec6784272e
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4e7e59443104910101782774c1e9d782ca033537
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385848"
---
# <a name="sample-search-and-retrieve-articles"></a>Sample: Search and retrieve articles

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Sample: Work with Service entities](https://code.msdn.microsoft.com/Service-Samples-f42adf82).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to search by body, keyword, and title, and retrieve articles by topic incident subject and topic incident product.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Service#SearchAndRetrieveArticles](../snippets/csharp/CRMV8/service/cs/searchandretrievearticles.cs#searchandretrievearticles)]  
  
### <a name="see-also"></a>Xem thêm  
 [Service Entities (Contract, Incident, Knowledge Base)](service-entities.md)   
 [Knowledge Base Entities](knowledge-management-entities.md)   
 <xref:Microsoft.Crm.Sdk.Messages.SearchByBodyKbArticleRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.SearchByKeywordsKbArticleRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.SearchByTitleKbArticleRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveByTopIncidentSubjectKbArticleRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveByTopIncidentProductKbArticleRequest>
