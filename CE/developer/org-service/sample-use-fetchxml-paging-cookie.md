---
title: 'Sample: Use FetchXML with a paging cookie (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to use the paging cookie in a FetchXML query to retrieve successive pages of query results. It uses the IOrganizationService. QueryBase) method
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
- retrieving successive pages of query results by using FetchXML sample
- FetchXML queries, samples
- using FetchXML with a paging cookie sample
- building queries with FetchXML, samples
- sample for retrieving successive pages of query results by using FetchXML
- sample for using FetchXML with a paging cookie
ms.assetid: 1d8acb4e-f8c3-478a-ae4f-e462973cd63d
caps.latest.revision: 27
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ef0c1f82033c2070dff459bdc538519e96c36c35
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388018"
---
# <a name="sample-use-fetchxml-with-a-paging-cookie"></a>Sample: Use FetchXML with a paging cookie

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps. Download the complete sample here [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e) 

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="example"></a>Ví dụ  
 This sample shows how to use the paging cookie in a FetchXML query to retrieve successive pages of query results. It uses the<xref:Microsoft.Xrm.Sdk.IOrganizationService>. <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method.  
  
 [!code-csharp[Query#FetchPagingWithCookie](../../snippets/csharp/CRMV8/query/cs/fetchpagingwithcookie.cs#fetchpagingwithcookie)]  
  
### <a name="see-also"></a>Xem thêm  
 [Build Queries with FetchXML](build-queries-fetchxml.md)   
 [Sample: Convert queries between Fetch and QueryExpression](sample-convert-queries-fetch-queryexpression.md)   
 [Sample: CrmServiceHelper Class](helper-code-serverconnection-class.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>   
 [Using FetchXML Aggregration](use-fetchxml-aggregation.md)   
 [Using FetchXML](use-fetchxml-construct-query.md)
