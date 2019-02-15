---
title: Use LINQ to construct a query (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Discusses how to use .NET Language-Integrated Query(LINQ) query provider in Dynamics 365 for Customer Engagement to construct a query
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
- LINQ operators and their limitations, select clause
- LINQ operators and their limitations, orderby operator
- LINQ operators and their limitations, from clause
- LINQ operators and their limitations
- LINQ operators and their limitations, join clause
- LINQ operators and their limitations, where clause
- LINQ queries, using LINQ to construct queries
- using LINQ to construct queries, LINQ operators and their limitations
ms.assetid: 8fda7c51-ce40-4263-aeac-804dc79ea212
caps.latest.revision: 41
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b604ef2fb4a8dd9a163614b8d428658a330daea0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386866"
---
# <a name="use-linq-to-construct-a-query"></a><span data-ttu-id="06b69-103">Use LINQ to construct a query</span><span class="sxs-lookup"><span data-stu-id="06b69-103">Use LINQ to construct a query</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="06b69-104">The [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] query provider in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps uses standard LINQ syntax.</span><span class="sxs-lookup"><span data-stu-id="06b69-104">The [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] query provider in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps uses standard LINQ syntax.</span></span> <span data-ttu-id="06b69-105">The first step in creating a LINQ query is to identify the relevant entity types and the relationships between them.</span><span class="sxs-lookup"><span data-stu-id="06b69-105">The first step in creating a LINQ query is to identify the relevant entity types and the relationships between them.</span></span> <span data-ttu-id="06b69-106">You can then specify the data source and the other query parameters.</span><span class="sxs-lookup"><span data-stu-id="06b69-106">You can then specify the data source and the other query parameters.</span></span>  

 <span data-ttu-id="06b69-107">The `from` clause is used to return a single “root” entity.</span><span class="sxs-lookup"><span data-stu-id="06b69-107">The `from` clause is used to return a single “root” entity.</span></span> <span data-ttu-id="06b69-108">The query provider can only return entities of a single entity type.</span><span class="sxs-lookup"><span data-stu-id="06b69-108">The query provider can only return entities of a single entity type.</span></span> <span data-ttu-id="06b69-109">The `orderby` and `select` clauses must reference this root entity.</span><span class="sxs-lookup"><span data-stu-id="06b69-109">The `orderby` and `select` clauses must reference this root entity.</span></span> <span data-ttu-id="06b69-110">You can use `join` clauses to add entities with a relationship to the “root” entity.</span><span class="sxs-lookup"><span data-stu-id="06b69-110">You can use `join` clauses to add entities with a relationship to the “root” entity.</span></span>  

<a name="bkmk_operators"></a>   
## <a name="linq-operators"></a><span data-ttu-id="06b69-111">LINQ operators</span><span class="sxs-lookup"><span data-stu-id="06b69-111">LINQ operators</span></span>  
 <span data-ttu-id="06b69-112">All LINQ query expressions have a similar format.</span><span class="sxs-lookup"><span data-stu-id="06b69-112">All LINQ query expressions have a similar format.</span></span> <span data-ttu-id="06b69-113">The following table shows the most common clauses in a LINQ query expression when using the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps LINQ query provider.</span><span class="sxs-lookup"><span data-stu-id="06b69-113">The following table shows the most common clauses in a LINQ query expression when using the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps LINQ query provider.</span></span>  

### <a name="from"></a><span data-ttu-id="06b69-114">from</span><span class="sxs-lookup"><span data-stu-id="06b69-114">from</span></span>  
 <span data-ttu-id="06b69-115">When using the generated service context and early binding, use the `IQueryable` entity set, such as `AccountSet`, in the generated context.</span><span class="sxs-lookup"><span data-stu-id="06b69-115">When using the generated service context and early binding, use the `IQueryable` entity set, such as `AccountSet`, in the generated context.</span></span>  

 <span data-ttu-id="06b69-116">When not using the generated context, the `CreateQuery` method on the organization service context object gives you access to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps entities.</span><span class="sxs-lookup"><span data-stu-id="06b69-116">When not using the generated context, the `CreateQuery` method on the organization service context object gives you access to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps entities.</span></span>  

 <span data-ttu-id="06b69-117">Ví dụ: </span><span class="sxs-lookup"><span data-stu-id="06b69-117">Example:</span></span>  

 <span data-ttu-id="06b69-118">Using the generated service context:</span><span class="sxs-lookup"><span data-stu-id="06b69-118">Using the generated service context:</span></span>  

```csharp  
var query1 = from c in context.ContactSet  
select c;  
```  

 <span data-ttu-id="06b69-119">Using the `CreateQuery` method:</span><span class="sxs-lookup"><span data-stu-id="06b69-119">Using the `CreateQuery` method:</span></span>  

```csharp  
var query1 = from c in context.CreateQuery<Contact>()  
select c;  
```  

### <a name="join"></a><span data-ttu-id="06b69-120">tham gia</span><span class="sxs-lookup"><span data-stu-id="06b69-120">join</span></span>  
 <span data-ttu-id="06b69-121">The `join` clause represents an inner join.</span><span class="sxs-lookup"><span data-stu-id="06b69-121">The `join` clause represents an inner join.</span></span> <span data-ttu-id="06b69-122">You use the clause to work with two or more entities that can be joined with a common attribute value.</span><span class="sxs-lookup"><span data-stu-id="06b69-122">You use the clause to work with two or more entities that can be joined with a common attribute value.</span></span>  

 <span data-ttu-id="06b69-123">Ví dụ: </span><span class="sxs-lookup"><span data-stu-id="06b69-123">Example:</span></span>  

```csharp  
from c in context.ContactSet  
join a in context.AccountSet on c.ContactId equals a.PrimaryContactId.Id  
```  

### <a name="where"></a><span data-ttu-id="06b69-124">địa điểm</span><span class="sxs-lookup"><span data-stu-id="06b69-124">where</span></span>  
 <span data-ttu-id="06b69-125">The `where` clause applies a filter to the results, often using a Boolean expression.</span><span class="sxs-lookup"><span data-stu-id="06b69-125">The `where` clause applies a filter to the results, often using a Boolean expression.</span></span> <span data-ttu-id="06b69-126">The filter specifies which elements to exclude from the source sequence.</span><span class="sxs-lookup"><span data-stu-id="06b69-126">The filter specifies which elements to exclude from the source sequence.</span></span> <span data-ttu-id="06b69-127">Each `where` clause can only contain conditions against a single entity type.</span><span class="sxs-lookup"><span data-stu-id="06b69-127">Each `where` clause can only contain conditions against a single entity type.</span></span> <span data-ttu-id="06b69-128">A composite condition involving multiple entities is not valid.</span><span class="sxs-lookup"><span data-stu-id="06b69-128">A composite condition involving multiple entities is not valid.</span></span> <span data-ttu-id="06b69-129">Instead, each entity should be filtered in separate `where` clauses.</span><span class="sxs-lookup"><span data-stu-id="06b69-129">Instead, each entity should be filtered in separate `where` clauses.</span></span>  

 <span data-ttu-id="06b69-130">Ví dụ: </span><span class="sxs-lookup"><span data-stu-id="06b69-130">Example:</span></span>  

```csharp  
from a in context.AccountSet  
where (a.Name.StartsWith("Contoso") && a.Address1_StateOrProvince == "WA")  
```  

### <a name="orderby"></a><span data-ttu-id="06b69-131">orderby</span><span class="sxs-lookup"><span data-stu-id="06b69-131">orderby</span></span>  
 <span data-ttu-id="06b69-132">The `orderby` operator puts the returned query attributes in a specified order.</span><span class="sxs-lookup"><span data-stu-id="06b69-132">The `orderby` operator puts the returned query attributes in a specified order.</span></span>  

 <span data-ttu-id="06b69-133">Ví dụ: </span><span class="sxs-lookup"><span data-stu-id="06b69-133">Example:</span></span>  

```csharp  
var query1 = from c in context.CreateQuery<Contact>()     
    orderby c.FullName ascending     
    select c;  
foreach ( var q in query1)     
{  
    Console.WriteLine(q.FirstName + " " + q.LastName);     
}  
```  

### <a name="select"></a><span data-ttu-id="06b69-134">chọn</span><span class="sxs-lookup"><span data-stu-id="06b69-134">select</span></span>  
 <span data-ttu-id="06b69-135">The `select` clause defines the form of the data returned.</span><span class="sxs-lookup"><span data-stu-id="06b69-135">The `select` clause defines the form of the data returned.</span></span> <span data-ttu-id="06b69-136">The clause creates a column set based on the query expression results.</span><span class="sxs-lookup"><span data-stu-id="06b69-136">The clause creates a column set based on the query expression results.</span></span> <span data-ttu-id="06b69-137">You can also define an instance of a new object to work with.</span><span class="sxs-lookup"><span data-stu-id="06b69-137">You can also define an instance of a new object to work with.</span></span> <span data-ttu-id="06b69-138">The newly created object using the `select` clause is not created on the server, but is a local instance.</span><span class="sxs-lookup"><span data-stu-id="06b69-138">The newly created object using the `select` clause is not created on the server, but is a local instance.</span></span>  

 <span data-ttu-id="06b69-139">Ví dụ: </span><span class="sxs-lookup"><span data-stu-id="06b69-139">Example:</span></span>  

```csharp  
select new Contact     
{  
    ContactId = c.ContactId,  
    FirstName = c.FirstName,  
    LastName = c.LastName,  
    Address1_Telephone1 = c.Address1_Telephone1     
};  
```  

<a name="limitations"></a>   
## <a name="linq-limitations"></a><span data-ttu-id="06b69-140">LINQ limitations</span><span class="sxs-lookup"><span data-stu-id="06b69-140">LINQ limitations</span></span>  
 <span data-ttu-id="06b69-141">The LINQ query provider supports a subset of the LINQ operators.</span><span class="sxs-lookup"><span data-stu-id="06b69-141">The LINQ query provider supports a subset of the LINQ operators.</span></span> <span data-ttu-id="06b69-142">Not all conditions that can be expressed in LINQ are supported.</span><span class="sxs-lookup"><span data-stu-id="06b69-142">Not all conditions that can be expressed in LINQ are supported.</span></span> <span data-ttu-id="06b69-143">The following table shows some of the limitations of the basic LINQ operators.</span><span class="sxs-lookup"><span data-stu-id="06b69-143">The following table shows some of the limitations of the basic LINQ operators.</span></span>  


|   <span data-ttu-id="06b69-144">Toán tử LINQ</span><span class="sxs-lookup"><span data-stu-id="06b69-144">LINQ Operator</span></span>   |                                                                                                                                              <span data-ttu-id="06b69-145">Giới hạn</span><span class="sxs-lookup"><span data-stu-id="06b69-145">Limitations</span></span>                                                                                                                                              |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|      `join`       |                                                                                                                <span data-ttu-id="06b69-146">Represents an inner or outer join.</span><span class="sxs-lookup"><span data-stu-id="06b69-146">Represents an inner or outer join.</span></span> <span data-ttu-id="06b69-147">Only left outer joins are supported.</span><span class="sxs-lookup"><span data-stu-id="06b69-147">Only left outer joins are supported.</span></span>                                                                                                                |
|      `from`       |                                                                                                                                 <span data-ttu-id="06b69-148">Supports one `from` clause per query.</span><span class="sxs-lookup"><span data-stu-id="06b69-148">Supports one `from` clause per query.</span></span>                                                                                                                                 |
|      `where`      | <span data-ttu-id="06b69-149">The left side of the clause must be an attribute name and the right side of the clause must be a value.</span><span class="sxs-lookup"><span data-stu-id="06b69-149">The left side of the clause must be an attribute name and the right side of the clause must be a value.</span></span> <span data-ttu-id="06b69-150">You cannot set the left side to a constant.</span><span class="sxs-lookup"><span data-stu-id="06b69-150">You cannot set the left side to a constant.</span></span> <span data-ttu-id="06b69-151">Both the sides of the clause cannot be constants.</span><span class="sxs-lookup"><span data-stu-id="06b69-151">Both the sides of the clause cannot be constants.</span></span><br /><br /> <span data-ttu-id="06b69-152">Supports the `String` functions `Contains`, `StartsWith`, `EndsWith`, and `Equals`.</span><span class="sxs-lookup"><span data-stu-id="06b69-152">Supports the `String` functions `Contains`, `StartsWith`, `EndsWith`, and `Equals`.</span></span> |
|     `groupBy`     |                               <span data-ttu-id="06b69-153">Chưa được hỗ trợ.</span><span class="sxs-lookup"><span data-stu-id="06b69-153">Not supported.</span></span> <span data-ttu-id="06b69-154">FetchXML supports grouping options that are not available with the LINQ query provider.</span><span class="sxs-lookup"><span data-stu-id="06b69-154">FetchXML supports grouping options that are not available with the LINQ query provider.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="06b69-155">[Use FetchXML Aggregation](use-fetchxml-aggregation.md)</span><span class="sxs-lookup"><span data-stu-id="06b69-155">[Use FetchXML Aggregation](use-fetchxml-aggregation.md)</span></span>                               |
|     `orderBy`     |                                                                                                                  <span data-ttu-id="06b69-156">Supports ordering by entity attributes, such as `Contact.FullName`.</span><span class="sxs-lookup"><span data-stu-id="06b69-156">Supports ordering by entity attributes, such as `Contact.FullName`.</span></span>                                                                                                                  |
|     `select`      |                                                                                                                       <span data-ttu-id="06b69-157">Supports anonymous types, constructors, and initializers.</span><span class="sxs-lookup"><span data-stu-id="06b69-157">Supports anonymous types, constructors, and initializers.</span></span>                                                                                                                       |
|      `last`       |                                                                                                                                 <span data-ttu-id="06b69-158">The `last` operator is not supported.</span><span class="sxs-lookup"><span data-stu-id="06b69-158">The `last` operator is not supported.</span></span>                                                                                                                                 |
| <span data-ttu-id="06b69-159">`skip` và `take`</span><span class="sxs-lookup"><span data-stu-id="06b69-159">`skip` and `take`</span></span> |                                                                                       <span data-ttu-id="06b69-160">Supports `skip` and `take` using server-side paging.</span><span class="sxs-lookup"><span data-stu-id="06b69-160">Supports `skip` and `take` using server-side paging.</span></span> <span data-ttu-id="06b69-161">The `skip` value must be greater than or equal to the `take` value.</span><span class="sxs-lookup"><span data-stu-id="06b69-161">The `skip` value must be greater than or equal to the `take` value.</span></span>                                                                                        |
|    `aggregate`    |                             <span data-ttu-id="06b69-162">Chưa được hỗ trợ.</span><span class="sxs-lookup"><span data-stu-id="06b69-162">Not supported.</span></span> <span data-ttu-id="06b69-163">FetchXML supports aggregation options that are not available with the LINQ query provider.</span><span class="sxs-lookup"><span data-stu-id="06b69-163">FetchXML supports aggregation options that are not available with the LINQ query provider.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="06b69-164">[Use FetchXML Aggregation](use-fetchxml-aggregation.md)</span><span class="sxs-lookup"><span data-stu-id="06b69-164">[Use FetchXML Aggregation](use-fetchxml-aggregation.md)</span></span>                              |

<a name="filter"></a>   
## <a name="filter-multiple-entities"></a><span data-ttu-id="06b69-165">Filter multiple entities</span><span class="sxs-lookup"><span data-stu-id="06b69-165">Filter multiple entities</span></span>  
 <span data-ttu-id="06b69-166">You can create complex [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] queries in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps and [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="06b69-166">You can create complex [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] queries in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps and [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps.</span></span> <span data-ttu-id="06b69-167">You use multiple `Join` clauses with filter clauses to create a result that is filtered on attributes from several entities.</span><span class="sxs-lookup"><span data-stu-id="06b69-167">You use multiple `Join` clauses with filter clauses to create a result that is filtered on attributes from several entities.</span></span>  

 <span data-ttu-id="06b69-168">The following sample shows how to create a LINQ query that works with two entities and filters the result based on values from each of the entities.</span><span class="sxs-lookup"><span data-stu-id="06b69-168">The following sample shows how to create a LINQ query that works with two entities and filters the result based on values from each of the entities.</span></span>  

 [!code-csharp[query#linqexamples3](../../snippets/csharp/CRMV8/query/cs/linqexamples3.cs#linqexamples3)]  

### <a name="see-also"></a><span data-ttu-id="06b69-169">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="06b69-169">See also</span></span>  
 <span data-ttu-id="06b69-170">[Sample: Create a LINQ Query](sample-create-linq-query.md) </span><span class="sxs-lookup"><span data-stu-id="06b69-170">[Sample: Create a LINQ Query](sample-create-linq-query.md) </span></span>  
 <span data-ttu-id="06b69-171">[Sample: LINQ Query Examples](sample-complex-linq-queries.md) </span><span class="sxs-lookup"><span data-stu-id="06b69-171">[Sample: LINQ Query Examples](sample-complex-linq-queries.md) </span></span>  
 <span data-ttu-id="06b69-172">[Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md) </span><span class="sxs-lookup"><span data-stu-id="06b69-172">[Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md) </span></span>  
 <span data-ttu-id="06b69-173">[Use Late-Bound Entity Class with a LINQ Query](use-late-bound-entity-class-linq-query.md) </span><span class="sxs-lookup"><span data-stu-id="06b69-173">[Use Late-Bound Entity Class with a LINQ Query](use-late-bound-entity-class-linq-query.md) </span></span>  
 [<span data-ttu-id="06b69-174">Blog: LINQPad 4 Driver for Dynamics CRM REST/Web API are available on CodePlex</span><span class="sxs-lookup"><span data-stu-id="06b69-174">Blog: LINQPad 4 Driver for Dynamics CRM REST/Web API are available on CodePlex</span></span>](http://blogs.msdn.com/b/crminthefield/archive/2015/06/11/linqpad-4-driver-for-dynamics-crm-rest-webapi-are-available-on-codeplex.aspx)
