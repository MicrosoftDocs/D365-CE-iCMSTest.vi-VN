---
title: Use the ColumnSet class (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how you can use the ColumnSet class to specify what attributes to return from a query expression
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
- reducing query results by defining the attributes to return, ColumnSet class
- ColumnSet class, about and code example
- ColumnSet class, specifying what attributes to return from a query expression
- ColumnSet class, reducing query results by defining the attributes to return
- using the ColumnSet class
- specifying what attributes to return from a query expression, ColumnSet class
ms.assetid: b74367ff-cd14-4305-9601-7c00acb80a0d
caps.latest.revision: 21
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9331aa853f619eace27bf588e59df5fbdbfd4482
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385794"
---
# <a name="use-the-columnset-class"></a><span data-ttu-id="a64b5-103">Use the ColumnSet class</span><span class="sxs-lookup"><span data-stu-id="a64b5-103">Use the ColumnSet class</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a64b5-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the <xref:Microsoft.Xrm.Sdk.Query.ColumnSet> class to specify what attributes to return from a query expression.</span><span class="sxs-lookup"><span data-stu-id="a64b5-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the <xref:Microsoft.Xrm.Sdk.Query.ColumnSet> class to specify what attributes to return from a query expression.</span></span> <span data-ttu-id="a64b5-105">The query returns only non-null values.</span><span class="sxs-lookup"><span data-stu-id="a64b5-105">The query returns only non-null values.</span></span>  
  
 <span data-ttu-id="a64b5-106">You can also use the <xref:Microsoft.Xrm.Sdk.Query.ColumnSet> class to reduce the size of a query result by defining only those attributes to be returned.</span><span class="sxs-lookup"><span data-stu-id="a64b5-106">You can also use the <xref:Microsoft.Xrm.Sdk.Query.ColumnSet> class to reduce the size of a query result by defining only those attributes to be returned.</span></span>  <span data-ttu-id="a64b5-107">To improve server performance, it is recommended that you don’t execute a query that returns all columns.</span><span class="sxs-lookup"><span data-stu-id="a64b5-107">To improve server performance, it is recommended that you don’t execute a query that returns all columns.</span></span>  
  
 <span data-ttu-id="a64b5-108">The following code example shows how to use the `ColumnSet` class to specify what attributes to return from a query expression.</span><span class="sxs-lookup"><span data-stu-id="a64b5-108">The following code example shows how to use the `ColumnSet` class to specify what attributes to return from a query expression.</span></span>  
  
```csharp  
QueryExpression contactquery = new QueryExpression   
{  
   EntityName="contact",  
   ColumnSet = new ColumnSet("firstname", "lastname", "contactid")   
};  
```  
  
### <a name="see-also"></a><span data-ttu-id="a64b5-109">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a64b5-109">See also</span></span>  
 <span data-ttu-id="a64b5-110">[Using the QueryExpression Class](use-queryexpression-class.md) </span><span class="sxs-lookup"><span data-stu-id="a64b5-110">[Using the QueryExpression Class](use-queryexpression-class.md) </span></span>  
 <span data-ttu-id="a64b5-111">[Building Queries with QueryExpression](build-queries-with-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="a64b5-111">[Building Queries with QueryExpression](build-queries-with-queryexpression.md) </span></span>  
 <span data-ttu-id="a64b5-112">[Use the ConditionExpression Class](use-conditionexpression-class.md) </span><span class="sxs-lookup"><span data-stu-id="a64b5-112">[Use the ConditionExpression Class](use-conditionexpression-class.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Query.QueryExpression>   
 <xref:Microsoft.Xrm.Sdk.Query.ColumnSet>
