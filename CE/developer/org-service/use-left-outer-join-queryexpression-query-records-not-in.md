---
title: Use a left outer join in QueryExpression to query for records &quot;not in&quot; (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how to use a left outer join by using the QueryExpression class to perform a query that filters on the join table and build a query to find records &quot;not in&quot; a set
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
ms.openlocfilehash: 2b643d12f22f129fb78f4e8e5cd0aee92be944f2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388839"
---
# <a name="use-a-left-outer-join-in-queryexpression-to-query-for-records-quotnot-inquot"></a>Use a left outer join in QueryExpression to query for records &quot;not in&quot;

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

You can use a left outer join by using the <xref:Microsoft.Crm.Sdk.Messages.SearchByKeywordsKbArticleRequest.QueryExpression> class to perform a query that filters on the join table, such as to find all contacts who did not have any campaign activities in the past two months. Another common use for this type of a query is to find records “not in” a set, such as in these cases:  
  
- Find all leads that have no tasks  
  
- Find all accounts that have no contacts  
  
- Find all leads that have one or more tasks  
  
  A left outer join returns each row that satisfies the join of the first input with the second input. It also returns any rows from the first input that had no matching rows in the second input. The nonmatching rows in the second input are returned as null values.  
  
  You can perform a left outer join in `QueryExpression` by using the `entityname` attribute as a condition operator. The `entityname` attribute is valid in conditions, filters, and nested filters.  
  
## <a name="find-all-leads-that-have-no-tasks-using-an-alias"></a>Find all leads that have no tasks, using an alias  
 The following example shows how to construct this query:  
  
```csharp
QueryExpression qx = new QueryExpression("lead");  
qx.ColumnSet.AddColumn("subject");  
  
LinkEntity link = qx.AddLink("task", "leadid", "regardingobjectid", JoinOperator.LeftOuter);  
link.Columns.AddColumn("subject");  
link.EntityAlias = "tsk";  
  
qx.Criteria = new FilterExpression();  
qx.Criteria.AddCondition("tsk", "activityid", ConditionOperator.Null);
```  
  
 This is equivalent to the following SQL:  
  
```sql
SELECT lead.FullName  
FROM Leads as lead  
LEFT OUTER JOIN Tasks as ab  
ON (lead.leadId  =  ab.RegardingObjectId)  
WHERE ab.RegardingObjectId is null
```  
  
### <a name="see-also"></a>Xem thêm  
 [Build Queries with QueryExpression](build-queries-with-queryexpression.md)   
 [Test for a Null Value](test-null-value.md)   
 [Using the QueryExpression Class](use-queryexpression-class.md)   
 [Using the QueryByAttribute Class](use-querybyattribute-class.md)
