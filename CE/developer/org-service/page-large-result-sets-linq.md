---
title: Page large result sets with LINQ (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how you can page the results of a large .NET Language-Integrated Query (LINQ) query by using the Take and Skip operators
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- paging the results of large LINQ queries, LINQ paging example
- LINQ queries, paging the results of large LINQ queries
- paging the results of large LINQ queries, by using the Take and Skip operators
ms.assetid: f1c3d6f5-1dfa-4eb6-aaf8-9b58f9ba358d
caps.latest.revision: 18
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b2693be15b62715931d0182e09f49e343dc530d5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386948"
---
# <a name="page-large-result-sets-with-linq"></a><span data-ttu-id="8c235-103">Page large result sets with LINQ</span><span class="sxs-lookup"><span data-stu-id="8c235-103">Page large result sets with LINQ</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="8c235-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement you can page the results of a large [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] query by using the `Take` and `Skip` operators.</span><span class="sxs-lookup"><span data-stu-id="8c235-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement you can page the results of a large [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] query by using the `Take` and `Skip` operators.</span></span> <span data-ttu-id="8c235-105">The `Take` operator retrieves a specified number of results and the `Skip` operator skips over a specified number of results.</span><span class="sxs-lookup"><span data-stu-id="8c235-105">The `Take` operator retrieves a specified number of results and the `Skip` operator skips over a specified number of results.</span></span>  
  
## <a name="linq-paging-example"></a><span data-ttu-id="8c235-106">LINQ paging example</span><span class="sxs-lookup"><span data-stu-id="8c235-106">LINQ paging example</span></span>  
 <span data-ttu-id="8c235-107">The following example shows how to page the results of a LINQ query by using the `Take` and `Skip` operators:</span><span class="sxs-lookup"><span data-stu-id="8c235-107">The following example shows how to page the results of a LINQ query by using the `Take` and `Skip` operators:</span></span>  
  
 [!code-csharp[Query#UseLinqQuery1](../../snippets/csharp/CRMV8/query/cs/uselinqquery1.cs#uselinqquery1)]  
  
### <a name="see-also"></a><span data-ttu-id="8c235-108">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="8c235-108">See also</span></span>  
 <span data-ttu-id="8c235-109">[Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md) </span><span class="sxs-lookup"><span data-stu-id="8c235-109">[Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md) </span></span>  
 [<span data-ttu-id="8c235-110">LINQ query examples</span><span class="sxs-lookup"><span data-stu-id="8c235-110">LINQ query examples</span></span>](linq-query-examples.md)
