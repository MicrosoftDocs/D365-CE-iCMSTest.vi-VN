---
title: 'Sample: Use QueryExpression with a paging cookie (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: The following sample shows how to use the QueryBase) method to return the 1:N related entities of an entity along with the primary entity
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 9999be1f-59fa-41f9-baff-e02ab92e5dc4
caps.latest.revision: 9
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3a9de2101f53b96ae37ef3baf35506b2e26a554e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385473"
---
# <a name="sample-use-queryexpression-with-a-paging-cookie"></a>Sample: Use QueryExpression with a paging cookie

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps. Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).   

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
 
## <a name="example"></a>Ví dụ  
 This sample shows how to use the paging cookie in a QueryExpression query to retrieve successive pages of query results. It uses the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method.  
  
 [!code-csharp[Query#QueryExpressionPagingWithCookie](../../snippets/csharp/CRMV8/query/cs/queryexpressionpagingwithcookie.cs#queryexpressionpagingwithcookie)]  
  
### <a name="see-also"></a>Xem thêm  
 [Page large result sets with QueryExpression](page-large-result-sets-with-queryexpression.md)   
 [Build Queries with QueryExpression](build-queries-with-queryexpression.md)   
 [Sample: Convert queries between Fetch and QueryExpression](sample-convert-queries-fetch-queryexpression.md)   
 [Sample: CrmServiceHelper Class](helper-code-serverconnection-class.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>
