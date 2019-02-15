---
title: Order results using entity attributes with LINQ (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how you can use lookup or OptionSet (Picklist) attributes to order results within a LINQ query
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
- LINQ queries, using OptionSet (Picklist) attributes to order results in LINQ queries
- LINQ queries, ordering query results by using entity attributes with LINQ
- LINQ queries, using a lookup value in an order by clause (example of)
- arranging results in order by using entity attributes with LINQ
- ordering results by using entity attributes with LINQ
ms.assetid: 72904866-87bd-4f4c-9fec-695e6f47a6b2
caps.latest.revision: 24
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4bb8f23a40ad977d7ef95b2f1441e05e9d4ab135
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385822"
---
# <a name="order-results-using-entity-attributes-with-linq"></a><span data-ttu-id="8c8ac-103">Order results using entity attributes with LINQ</span><span class="sxs-lookup"><span data-stu-id="8c8ac-103">Order results using entity attributes with LINQ</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="8c8ac-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use lookup or OptionSet (Picklist) attributes to order results within a LINQ query.</span><span class="sxs-lookup"><span data-stu-id="8c8ac-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use lookup or OptionSet (Picklist) attributes to order results within a LINQ query.</span></span> <span data-ttu-id="8c8ac-105">This topic shows several examples of this type of query.</span><span class="sxs-lookup"><span data-stu-id="8c8ac-105">This topic shows several examples of this type of query.</span></span>  
  
## <a name="using-a-lookup-value-to-order-by"></a><span data-ttu-id="8c8ac-106">Using a Lookup Value to Order By</span><span class="sxs-lookup"><span data-stu-id="8c8ac-106">Using a Lookup Value to Order By</span></span>  
 <span data-ttu-id="8c8ac-107">The following sample shows use the lookup attribute `PrimaryContactId` in an `Order By` clause.</span><span class="sxs-lookup"><span data-stu-id="8c8ac-107">The following sample shows use the lookup attribute `PrimaryContactId` in an `Order By` clause.</span></span>  
  
 [!code-csharp[Query#linqexamples38](../../snippets/csharp/CRMV8/query/cs/linqexamples38.cs#linqexamples38)]  
  
## <a name="using-a-picklist-to-order-by"></a><span data-ttu-id="8c8ac-108">Using a Picklist to Order By</span><span class="sxs-lookup"><span data-stu-id="8c8ac-108">Using a Picklist to Order By</span></span>  
 <span data-ttu-id="8c8ac-109">The following sample shows use of a lookup value to order by.</span><span class="sxs-lookup"><span data-stu-id="8c8ac-109">The following sample shows use of a lookup value to order by.</span></span>  
  
 [!code-csharp[Query#linqexamples39](../../snippets/csharp/CRMV8/query/cs/linqexamples39.cs#linqexamples39)]  
  
### <a name="see-also"></a><span data-ttu-id="8c8ac-110">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="8c8ac-110">See also</span></span>  
 <span data-ttu-id="8c8ac-111">[Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md) </span><span class="sxs-lookup"><span data-stu-id="8c8ac-111">[Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md) </span></span>  
 [<span data-ttu-id="8c8ac-112">Page large result sets with LINQ</span><span class="sxs-lookup"><span data-stu-id="8c8ac-112">Page large result sets with LINQ</span></span>](page-large-result-sets-linq.md)
