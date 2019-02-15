---
title: Use the FilterExpression class (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how you can use the FilterExpression class to build a query that expresses multiple conditions
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
- helper methods for creating queries, FilterExpression class
- FilterExpression class, about; properties for; and code example
- creating queries that express multiple conditions, FilterExpression class
- creating queries, that are equivalent to SQL expressions
- using the FilterExpression class
- FilterExpression class, methods that help you create queries
- building queries that express multiple conditions, FilterExpression class
ms.assetid: 8385883e-8933-419c-91d0-25353e59a1a1
caps.latest.revision: 35
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f681c8f7741a83a67ecc9fefb447e3333e0acb5b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385622"
---
# <a name="use-the-filterexpression-class"></a>Use the FilterExpression class

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the <xref:Microsoft.Xrm.Sdk.Query.FilterExpression> class to build a query that expresses multiple conditions. For example, you can create a query expression that is the equivalent of a SQL statement such as `([FirstName] = 'Joe' OR [FirstName] = 'John') AND [City] = 'Redmond'`.  
  
 The following table lists the properties for the <xref:Microsoft.Xrm.Sdk.Query.FilterExpression> class.  
  
|||  
|-|-|  
|Thuộc tính|Mô tả|  
|<xref:Microsoft.Xrm.Sdk.Query.FilterExpression.Conditions>|Gets or sets condition expressions that include attributes, condition operators, and attribute values.|  
|<xref:Microsoft.Xrm.Sdk.Query.FilterExpression.FilterOperator>|Gets or sets logical `AND/OR` filter operators. This is set by using the <xref:Microsoft.Xrm.Sdk.Query.LogicalOperator> enumeration.|  
|<xref:Microsoft.Xrm.Sdk.Query.FilterExpression.Filters>|Gets or sets a hierarchy of condition and logical filter expressions that filter the results of the query.|  
|<xref:Microsoft.Xrm.Sdk.Query.FilterExpression.IsQuickFindFilter>|Gets or sets a value that indicates whether the expression is part of a quick find query.|  
  
 The <xref:Microsoft.Xrm.Sdk.Query.FilterExpression> class also includes several helper methods that make it easier to create queries. The <xref:Microsoft.Xrm.Sdk.Query.FilterExpression>.<xref:Microsoft.Xrm.Sdk.Query.ConditionExpression> method adds a <xref:Microsoft.Xrm.Sdk.Query.ConditionExpression> to the <xref:Microsoft.Xrm.Sdk.Query.FilterExpression.Conditions> property for the <xref:Microsoft.Xrm.Sdk.Query.FilterExpression>, reducing the amount of code needed to construct the condition expression. The <xref:Microsoft.Xrm.Sdk.Query.FilterExpression.AddFilter*>.<xref:Microsoft.Xrm.Sdk.Query.LogicalOperator> method adds a new filter to the <xref:Microsoft.Xrm.Sdk.Query.FilterExpression.Filters> property of the <xref:Microsoft.Xrm.Sdk.Query.FilterExpression> class.  
  
<a name="example"></a>   
## <a name="filter-expression-example"></a>Filter expression example  
 The following code example shows how to use the <xref:Microsoft.Xrm.Sdk.Query.FilterExpression> class.  
  
```csharp  
QueryExpression query = new QueryExpression("contact");   
query.ColumnSet.AddColumns("firstname", "lastname", "address1_city");   
  
query.Criteria = new FilterExpression();   
query.Criteria.AddCondition("address1_city", ConditionOperator.Equal, "Redmond");   
  
FilterExpression childFilter = query.Criteria.AddFilter(LogicalOperator.Or);   
childFilter.AddCondition("lastname", ConditionOperator.Equal, "Tharpe");   
childFilter.AddCondition("lastname", ConditionOperator.Equal, "Brown");   
  
// Pass query to service proxy   
EntityCollection results = _serviceProxy.RetrieveMultiple(query);   
Console.WriteLine();   
Console.WriteLine("Query using QE with multiple conditions and filters");   
Console.WriteLine("---------------------------------------");   
  
// Print results   
foreach (var a in results.Entities)   
{   
Console.WriteLine("Name: {0} {1}", a.GetAttributeValue<string>("firstname"), a.GetAttributeValue<string>("lastname"));   
Console.WriteLine("City: {0}", a.GetAttributeValue<string>("address1_city"));   
}   
Console.WriteLine("---------------------------------------");  
```  
  
<a name="quickfindfilter"></a>   
## <a name="about-the-isquickfindfilter-property"></a>About the IsQuickFindFilter property  
 You can use the <xref:Microsoft.Xrm.Sdk.Query.FilterExpression>.<xref:Microsoft.Xrm.Sdk.Query.FilterExpression.IsQuickFindFilter> property, that is analogous to the `isquickfindfields` attribute that exists on the `filter` node in Fetch XML. When a Fetch query is saved, this is stored in the `SavedQuery` and `UserQuery` entities `IsQuickFind` properties. The <xref:Microsoft.Xrm.Sdk.Query.FilterExpression.IsQuickFindFilter> property was added to provide consistency between Query Expression and Fetch XML queries.  
  
 The following rules apply to the <xref:Microsoft.Xrm.Sdk.Query.FilterExpression.IsQuickFindFilter> property:  
  
-   This field can only be set to `true` for filter expressions with a logical operator of type <xref:Microsoft.Xrm.Sdk.Query.LogicalOperator>.`Or`. If it is set for expressions with a logical operator of type <xref:Microsoft.Xrm.Sdk.Query.LogicalOperator>.`And`, the <xref:Microsoft.Xrm.Sdk.Query.FilterExpression.IsQuickFindFilter> property is ignored.  
  
-   Only one filter expression in a filter expression hierarchy can be set with <xref:Microsoft.Xrm.Sdk.Query.FilterExpression.IsQuickFindFilter> = **true**. If more than one is found, an exception is thrown.  
  
-   If a filter expression has <xref:Microsoft.Xrm.Sdk.Query.FilterExpression.IsQuickFindFilter> set to **true**, it cannot have any child filter expression properties, it can only have <xref:Microsoft.Xrm.Sdk.Query.ConditionExpression> properties. If you add a child filter expression, an exception is thrown.  
  
-   All condition expressions related to a filter expression with <xref:Microsoft.Xrm.Sdk.Query.FilterExpression.IsQuickFindFilter> set to **true** must be single non-null value conditions. In other words, given that a condition is made up of attribute, operator, and value, only conditions where the value property is a single value that is not **null** are supported. In addition, the only condition operators supported on these condition expressions are ones that work with a single value that is not null. If a **null** value or multiple values are detected, an exception is thrown.  
  
### <a name="see-also"></a>Xem thêm  
 [Building Queries with QueryExpression](build-queries-with-queryexpression.md)   
 [Use a left outer join in QueryExpression to query for records "not in"](use-left-outer-join-queryexpression-query-records-not-in.md)   
 [Using the ConditionExpression Class](use-conditionexpression-class.md)   
 <xref:Microsoft.Xrm.Sdk.Query.FilterExpression>