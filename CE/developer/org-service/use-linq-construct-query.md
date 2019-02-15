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
# <a name="use-linq-to-construct-a-query"></a>Use LINQ to construct a query

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

The [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] query provider in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps uses standard LINQ syntax. The first step in creating a LINQ query is to identify the relevant entity types and the relationships between them. You can then specify the data source and the other query parameters.  

 The `from` clause is used to return a single “root” entity. The query provider can only return entities of a single entity type. The `orderby` and `select` clauses must reference this root entity. You can use `join` clauses to add entities with a relationship to the “root” entity.  

<a name="bkmk_operators"></a>   
## <a name="linq-operators"></a>LINQ operators  
 All LINQ query expressions have a similar format. The following table shows the most common clauses in a LINQ query expression when using the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps LINQ query provider.  

### <a name="from"></a>from  
 When using the generated service context and early binding, use the `IQueryable` entity set, such as `AccountSet`, in the generated context.  

 When not using the generated context, the `CreateQuery` method on the organization service context object gives you access to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps entities.  

 Ví dụ:   

 Using the generated service context:  

```csharp  
var query1 = from c in context.ContactSet  
select c;  
```  

 Using the `CreateQuery` method:  

```csharp  
var query1 = from c in context.CreateQuery<Contact>()  
select c;  
```  

### <a name="join"></a>tham gia  
 The `join` clause represents an inner join. You use the clause to work with two or more entities that can be joined with a common attribute value.  

 Ví dụ:   

```csharp  
from c in context.ContactSet  
join a in context.AccountSet on c.ContactId equals a.PrimaryContactId.Id  
```  

### <a name="where"></a>địa điểm  
 The `where` clause applies a filter to the results, often using a Boolean expression. The filter specifies which elements to exclude from the source sequence. Each `where` clause can only contain conditions against a single entity type. A composite condition involving multiple entities is not valid. Instead, each entity should be filtered in separate `where` clauses.  

 Ví dụ:   

```csharp  
from a in context.AccountSet  
where (a.Name.StartsWith("Contoso") && a.Address1_StateOrProvince == "WA")  
```  

### <a name="orderby"></a>orderby  
 The `orderby` operator puts the returned query attributes in a specified order.  

 Ví dụ:   

```csharp  
var query1 = from c in context.CreateQuery<Contact>()     
    orderby c.FullName ascending     
    select c;  
foreach ( var q in query1)     
{  
    Console.WriteLine(q.FirstName + " " + q.LastName);     
}  
```  

### <a name="select"></a>chọn  
 The `select` clause defines the form of the data returned. The clause creates a column set based on the query expression results. You can also define an instance of a new object to work with. The newly created object using the `select` clause is not created on the server, but is a local instance.  

 Ví dụ:   

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
## <a name="linq-limitations"></a>LINQ limitations  
 The LINQ query provider supports a subset of the LINQ operators. Not all conditions that can be expressed in LINQ are supported. The following table shows some of the limitations of the basic LINQ operators.  


|   Toán tử LINQ   |                                                                                                                                              Giới hạn                                                                                                                                              |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|      `join`       |                                                                                                                Represents an inner or outer join. Only left outer joins are supported.                                                                                                                |
|      `from`       |                                                                                                                                 Supports one `from` clause per query.                                                                                                                                 |
|      `where`      | The left side of the clause must be an attribute name and the right side of the clause must be a value. You cannot set the left side to a constant. Both the sides of the clause cannot be constants.<br /><br /> Supports the `String` functions `Contains`, `StartsWith`, `EndsWith`, and `Equals`. |
|     `groupBy`     |                               Chưa được hỗ trợ. FetchXML supports grouping options that are not available with the LINQ query provider. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Use FetchXML Aggregation](use-fetchxml-aggregation.md)                               |
|     `orderBy`     |                                                                                                                  Supports ordering by entity attributes, such as `Contact.FullName`.                                                                                                                  |
|     `select`      |                                                                                                                       Supports anonymous types, constructors, and initializers.                                                                                                                       |
|      `last`       |                                                                                                                                 The `last` operator is not supported.                                                                                                                                 |
| `skip` và `take` |                                                                                       Supports `skip` and `take` using server-side paging. The `skip` value must be greater than or equal to the `take` value.                                                                                        |
|    `aggregate`    |                             Chưa được hỗ trợ. FetchXML supports aggregation options that are not available with the LINQ query provider. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Use FetchXML Aggregation](use-fetchxml-aggregation.md)                              |

<a name="filter"></a>   
## <a name="filter-multiple-entities"></a>Filter multiple entities  
 You can create complex [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] queries in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps and [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps. You use multiple `Join` clauses with filter clauses to create a result that is filtered on attributes from several entities.  

 The following sample shows how to create a LINQ query that works with two entities and filters the result based on values from each of the entities.  

 [!code-csharp[query#linqexamples3](../../snippets/csharp/CRMV8/query/cs/linqexamples3.cs#linqexamples3)]  

### <a name="see-also"></a>Xem thêm  
 [Sample: Create a LINQ Query](sample-create-linq-query.md)   
 [Sample: LINQ Query Examples](sample-complex-linq-queries.md)   
 [Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md)   
 [Use Late-Bound Entity Class with a LINQ Query](use-late-bound-entity-class-linq-query.md)   
 [Blog: LINQPad 4 Driver for Dynamics CRM REST/Web API are available on CodePlex](http://blogs.msdn.com/b/crminthefield/archive/2015/06/11/linqpad-4-driver-for-dynamics-crm-rest-webapi-are-available-on-codeplex.aspx)