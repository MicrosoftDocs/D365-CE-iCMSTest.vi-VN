---
title: Use a left outer join in QueryExpression to query for records &quot;not in&quot; | MicrosoftDocs
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 92be6428-d93a-4837-abd6-df052ecfa8a9
caps.latest.revision: 9
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 1b6f41454f73a844f39bf4464362fd2bfac24a19
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387967"
---
# <a name="use-a-left-outer-join-in-queryexpression-to-query-for-records-quotnot-inquot"></a><span data-ttu-id="8b2a1-102">Use a left outer join in QueryExpression to query for records &quot;not in&quot;</span><span class="sxs-lookup"><span data-stu-id="8b2a1-102">Use a left outer join in QueryExpression to query for records &quot;not in&quot;</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="8b2a1-103">You can use a left outer join by using the <xref:Microsoft.Crm.Sdk.Messages.SearchByKeywordsKbArticleRequest.QueryExpression> class to perform a query that filters on the join table, such as to find all contacts who did not have any campaign activities in the past two months.</span><span class="sxs-lookup"><span data-stu-id="8b2a1-103">You can use a left outer join by using the <xref:Microsoft.Crm.Sdk.Messages.SearchByKeywordsKbArticleRequest.QueryExpression> class to perform a query that filters on the join table, such as to find all contacts who did not have any campaign activities in the past two months.</span></span> <span data-ttu-id="8b2a1-104">Another common use for this type of a query is to find records “not in” a set, such as in these cases:</span><span class="sxs-lookup"><span data-stu-id="8b2a1-104">Another common use for this type of a query is to find records “not in” a set, such as in these cases:</span></span>  
  
- <span data-ttu-id="8b2a1-105">Find all leads that have no tasks</span><span class="sxs-lookup"><span data-stu-id="8b2a1-105">Find all leads that have no tasks</span></span>  
  
- <span data-ttu-id="8b2a1-106">Find all accounts that have no contacts</span><span class="sxs-lookup"><span data-stu-id="8b2a1-106">Find all accounts that have no contacts</span></span>  
  
- <span data-ttu-id="8b2a1-107">Find all leads that have one or more tasks</span><span class="sxs-lookup"><span data-stu-id="8b2a1-107">Find all leads that have one or more tasks</span></span>  
  
  <span data-ttu-id="8b2a1-108">A left outer join returns each row that satisfies the join of the first input with the second input.</span><span class="sxs-lookup"><span data-stu-id="8b2a1-108">A left outer join returns each row that satisfies the join of the first input with the second input.</span></span> <span data-ttu-id="8b2a1-109">It also returns any rows from the first input that had no matching rows in the second input.</span><span class="sxs-lookup"><span data-stu-id="8b2a1-109">It also returns any rows from the first input that had no matching rows in the second input.</span></span> <span data-ttu-id="8b2a1-110">The nonmatching rows in the second input are returned as null values.</span><span class="sxs-lookup"><span data-stu-id="8b2a1-110">The nonmatching rows in the second input are returned as null values.</span></span>  
  
  <span data-ttu-id="8b2a1-111">You can perform a left outer join in `QueryExpression` by using the `entityname` attribute as a condition operator.</span><span class="sxs-lookup"><span data-stu-id="8b2a1-111">You can perform a left outer join in `QueryExpression` by using the `entityname` attribute as a condition operator.</span></span> <span data-ttu-id="8b2a1-112">The `entityname` attribute is valid in conditions, filters, and nested filters.</span><span class="sxs-lookup"><span data-stu-id="8b2a1-112">The `entityname` attribute is valid in conditions, filters, and nested filters.</span></span>  
  
## <a name="find-all-leads-that-have-no-tasks-using-an-alias"></a><span data-ttu-id="8b2a1-113">Find all leads that have no tasks, using an alias</span><span class="sxs-lookup"><span data-stu-id="8b2a1-113">Find all leads that have no tasks, using an alias</span></span>  
 <span data-ttu-id="8b2a1-114">The following example shows how to construct this query:</span><span class="sxs-lookup"><span data-stu-id="8b2a1-114">The following example shows how to construct this query:</span></span>  
  
```csharp 
QueryExpression qx = new QueryExpression("lead");  
qx.ColumnSet.AddColumn("subject");  
  
LinkEntity link = qx.AddLink("task", "leadid", "regardingobjectid", JoinOperator.LeftOuter);  
link.Columns.AddColumn("subject");  
link.EntityAlias = "tsk";  
  
qx.Criteria = new FilterExpression();  
qx.Criteria.AddCondition("tsk", "activityid", ConditionOperator.Null);  
  
```  
  
 <span data-ttu-id="8b2a1-115">This is equivalent to the following SQL:</span><span class="sxs-lookup"><span data-stu-id="8b2a1-115">This is equivalent to the following SQL:</span></span>  
  
```sql 
SELECT lead.FullName  
FROM Leads as lead  
LEFT OUTER JOIN Tasks as ab  
ON (lead.leadId  =  ab.RegardingObjectId)  
WHERE ab.RegardingObjectId is null  
  
```  
  
### <a name="see-also"></a><span data-ttu-id="8b2a1-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="8b2a1-116">See also</span></span>  
 <span data-ttu-id="8b2a1-117">[Build Queries with QueryExpression](org-service/build-queries-with-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="8b2a1-117">[Build Queries with QueryExpression](org-service/build-queries-with-queryexpression.md) </span></span>  
 <span data-ttu-id="8b2a1-118">[Test for a Null Value](org-service/test-null-value.md) </span><span class="sxs-lookup"><span data-stu-id="8b2a1-118">[Test for a Null Value](org-service/test-null-value.md) </span></span>  
 <span data-ttu-id="8b2a1-119">[Using the QueryExpression Class](org-service/use-queryexpression-class.md) </span><span class="sxs-lookup"><span data-stu-id="8b2a1-119">[Using the QueryExpression Class](org-service/use-queryexpression-class.md) </span></span>  
 [<span data-ttu-id="8b2a1-120">Using the QueryByAttribute Class</span><span class="sxs-lookup"><span data-stu-id="8b2a1-120">Using the QueryByAttribute Class</span></span>](org-service/use-querybyattribute-class.md)
