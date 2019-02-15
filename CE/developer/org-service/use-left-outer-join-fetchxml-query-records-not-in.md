---
title: Use a left outer join in FetchXML to query for records &quot;not in&quot; (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Read how to use a left outer join in FetchXML to perform a query that filters on the join table and build a query to find records “not in” a set
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: c4f2e2df-7b9a-4842-ba1e-29c5b59d8fc7
caps.latest.revision: 11
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d9223dbeacc213883ccc4697928e8ecfb7040acf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388660"
---
# <a name="use-a-left-outer-join-in-fetchxml-to-query-for-records-quotnot-inquot"></a><span data-ttu-id="cd128-103">Use a left outer join in FetchXML to query for records &quot;not in&quot;</span><span class="sxs-lookup"><span data-stu-id="cd128-103">Use a left outer join in FetchXML to query for records &quot;not in&quot;</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="cd128-104">You can use a left outer join in FetchXML to perform a query that filters on the join table, such as to find all contacts who did not have any campaign activities in the past two months.</span><span class="sxs-lookup"><span data-stu-id="cd128-104">You can use a left outer join in FetchXML to perform a query that filters on the join table, such as to find all contacts who did not have any campaign activities in the past two months.</span></span> <span data-ttu-id="cd128-105">Another common use for this type of a query is to find records “not in” a set, such as in these cases:</span><span class="sxs-lookup"><span data-stu-id="cd128-105">Another common use for this type of a query is to find records “not in” a set, such as in these cases:</span></span>  
  
- <span data-ttu-id="cd128-106">Find all leads that have no tasks</span><span class="sxs-lookup"><span data-stu-id="cd128-106">Find all leads that have no tasks</span></span>  
  
- <span data-ttu-id="cd128-107">Find all accounts that have no contacts</span><span class="sxs-lookup"><span data-stu-id="cd128-107">Find all accounts that have no contacts</span></span>  
  
- <span data-ttu-id="cd128-108">Find all leads that have one or more tasks</span><span class="sxs-lookup"><span data-stu-id="cd128-108">Find all leads that have one or more tasks</span></span>  
  
  <span data-ttu-id="cd128-109">A left outer join returns each row that satisfies the join of the first input with the second input.</span><span class="sxs-lookup"><span data-stu-id="cd128-109">A left outer join returns each row that satisfies the join of the first input with the second input.</span></span> <span data-ttu-id="cd128-110">It also returns any rows from the first input that had no matching rows in the second input.</span><span class="sxs-lookup"><span data-stu-id="cd128-110">It also returns any rows from the first input that had no matching rows in the second input.</span></span> <span data-ttu-id="cd128-111">The nonmatching rows in the second input are returned as null values.</span><span class="sxs-lookup"><span data-stu-id="cd128-111">The nonmatching rows in the second input are returned as null values.</span></span>  
  
  <span data-ttu-id="cd128-112">You can perform a left outer join in FetchXML by using the `entityname` attribute as a condition operator.</span><span class="sxs-lookup"><span data-stu-id="cd128-112">You can perform a left outer join in FetchXML by using the `entityname` attribute as a condition operator.</span></span> <span data-ttu-id="cd128-113">The `entityname` attribute is valid in conditions, filters, and nested filters.</span><span class="sxs-lookup"><span data-stu-id="cd128-113">The `entityname` attribute is valid in conditions, filters, and nested filters.</span></span>  
  
  <span data-ttu-id="cd128-114">You can create a query using a left outer join programmatically and execute the query using the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest>, and you can save the query by creating a `SavedQuery` record.</span><span class="sxs-lookup"><span data-stu-id="cd128-114">You can create a query using a left outer join programmatically and execute the query using the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest>, and you can save the query by creating a `SavedQuery` record.</span></span> <span data-ttu-id="cd128-115">You can open a saved query that contains a left outer join in the Advanced Find or Saved Query editors in the web application and execute and view results, but some editor functionality is disabled.</span><span class="sxs-lookup"><span data-stu-id="cd128-115">You can open a saved query that contains a left outer join in the Advanced Find or Saved Query editors in the web application and execute and view results, but some editor functionality is disabled.</span></span> <span data-ttu-id="cd128-116">Those editors will allow modifications to the query, such as to change the columns returned, but the editor does not support changing the left outer join.</span><span class="sxs-lookup"><span data-stu-id="cd128-116">Those editors will allow modifications to the query, such as to change the columns returned, but the editor does not support changing the left outer join.</span></span>  
  
## <a name="example-find-all-accounts-that-have-no-leads"></a><span data-ttu-id="cd128-117">Example: Find all accounts that have no leads</span><span class="sxs-lookup"><span data-stu-id="cd128-117">Example: Find all accounts that have no leads</span></span>  
 <span data-ttu-id="cd128-118">The following shows how to construct the query in FetchXML:</span><span class="sxs-lookup"><span data-stu-id="cd128-118">The following shows how to construct the query in FetchXML:</span></span>  
  
```xml  
<fetch mapping='logical'>  
 <entity name='account'>  
  <attribute name='name'/>  
  <link-entity name='lead'  
               from='leadid'  
               to='originatingleadid'  
               link-type='outer'/>  
  <filter type='and'>  
   <condition entityname='lead'  
              attribute='leadid'  
              operator='null'/>  
  </filter>  
 </entity>  
</fetch>  
  
```  
  
## <a name="example-find-all-leads-that-have-no-tasks-using-an-alias"></a><span data-ttu-id="cd128-119">Example: Find all leads that have no tasks, using an alias</span><span class="sxs-lookup"><span data-stu-id="cd128-119">Example: Find all leads that have no tasks, using an alias</span></span>  
 <span data-ttu-id="cd128-120">The following shows how to construct the query in FetchXML:</span><span class="sxs-lookup"><span data-stu-id="cd128-120">The following shows how to construct the query in FetchXML:</span></span>  
  
```xml  
<fetch version="1.0" output-format="xml-platform" mapping="logical" distinct="true">  
  <entity name="lead">  
    <attribute name="fullname" />  
    <link-entity name="task" from="regardingobjectid" to="leadid" alias="ab" link-type="outer">  
       <attribute name="regardingobjectid" />  
    </link-entity>  
    <filter type="and">  
        <condition entityname="ab" attribute="regardingobjectid" operator="null" />  
    </filter>  
  </entity>  
<fetch/>  
  
```  
  
 <span data-ttu-id="cd128-121">This is equivalent to the following SQL:</span><span class="sxs-lookup"><span data-stu-id="cd128-121">This is equivalent to the following SQL:</span></span>  
  
```sql  
SELECT lead.FullName  
FROM Leads as lead  
LEFT OUTER JOIN Tasks as ab  
ON (lead.leadId  =  ab.RegardingObjectId)  
WHERE ab.RegardingObjectId is null  
  
```  
  
### <a name="see-also"></a><span data-ttu-id="cd128-122">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="cd128-122">See also</span></span>  
 <span data-ttu-id="cd128-123">[Build Queries with FetchXML](build-queries-fetchxml.md) </span><span class="sxs-lookup"><span data-stu-id="cd128-123">[Build Queries with FetchXML](build-queries-fetchxml.md) </span></span>  
 <span data-ttu-id="cd128-124">[Sample: Use Aggregation in FetchXML](sample-use-aggregation-fetchxml.md) </span><span class="sxs-lookup"><span data-stu-id="cd128-124">[Sample: Use Aggregation in FetchXML](sample-use-aggregation-fetchxml.md) </span></span>  
 <span data-ttu-id="cd128-125">[Use FetchXML to Construct a Query](use-fetchxml-construct-query.md) </span><span class="sxs-lookup"><span data-stu-id="cd128-125">[Use FetchXML to Construct a Query](use-fetchxml-construct-query.md) </span></span>  
 [<span data-ttu-id="cd128-126">Sample: Validate and Execute a Saved Query</span><span class="sxs-lookup"><span data-stu-id="cd128-126">Sample: Validate and Execute a Saved Query</span></span>](sample-validate-execute-saved-query.md)
