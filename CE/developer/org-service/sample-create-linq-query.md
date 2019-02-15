---
title: 'Sample: Create a LINQ query (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to create simple .NET Language-Integrated Query (LINQ) queries
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
- LINQ query examples and samples, creating simple LINQ queries sample
- simple LINQ queries sample
- creating simple LINQ queries sample
- sample for creating simple LINQ queries
ms.assetid: 43b26b09-636e-4781-8477-65454c4c5232
caps.latest.revision: 19
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6adfec0436acd6a55fb92c9ebe1349692dc06197
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387934"
---
# <a name="sample-create-a-linq-query"></a>Sample: Create a LINQ query

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement. [!INCLUDE[sdk_download](../../includes/sdk-download.md)] Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).   

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create simple [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] queries. The following queries are demonstrated:  
  
-   Retrieve all accounts that the calling user has access to.  
  
-   Retrieve all accounts owned by the user who has read access rights to the accounts and where the last name of the user is not “Cannon.”  
  
-   Return a count of all accounts that have a county specified in their addresses.  
  
-   Return a count of states in which we have an account. This uses the `distinct` keyword that counts a state only once.  
  
-   Return contacts where the city equals “Redmond” AND the first name is “Joe” OR “John.”  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[query#CreateALinqQuery](../../snippets/csharp/CRMV8/query/cs/createalinqquery.cs#createalinqquery)]  
  
### <a name="see-also"></a>Xem thêm  
 [Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md)   
 [Sample: Complex LINQ Queries](sample-complex-linq-queries.md)   
 <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext>
