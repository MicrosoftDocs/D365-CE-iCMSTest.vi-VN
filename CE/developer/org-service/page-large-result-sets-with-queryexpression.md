---
title: Page large result sets with QueryExpression (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: In Dynamics 365 for Customer Engagement (online) Customer Engagement, you can use the paging cookie feature to make paging in an application faster for large datasets. The feature is available in both FetchXML and QueryExpression queries
ms.custom: ''
ms.date: 09/13/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 0be338b9-dbb1-41b6-b313-c632e40d2af5
caps.latest.revision: 29
author: mayadumesh
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b9741321906bcdf0052255de4e13abc88816af70
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387079"
---
# <a name="page-large-result-sets-with-queryexpression"></a>Page large result sets with QueryExpression

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the paging cookie feature to make paging in an application faster for large datasets. The feature is available in both FetchXML and <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> queries. When you use the paging cookie feature when querying a set of records, the result contains a value for the paging cookie. To improve system performance, you can then pass that value when you retrieve the next set of records.  
  
 <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> and FetchXML use different formats for their paging cookies. If you convert from one query format to the other by using the <xref:Microsoft.Crm.Sdk.Messages.QueryExpressionToFetchXmlRequest> message or the <xref:Microsoft.Crm.Sdk.Messages.FetchXmlToQueryExpressionRequest> message, the paging cookie value is ignored. In addition, if you request nonconsecutive pages, the paging cookie value is ignored.  
  
<a name="QueryExpression"></a> 

## <a name="using-a-paging-cookie-with-queryexpression"></a>Using a paging cookie with QueryExpression  
 The following example shows how to use the paging cookie with a query expression. For the complete sample code, see [Sample: Use QueryExpression with a paging cookie](sample-use-queryexpression-with-a-paging-cookie.md).  
  
 [!code-csharp[Query#QueryExpressionPagingWithCookie1](../../snippets/csharp/CRMV8/query/cs/queryexpressionpagingwithcookie1.cs#queryexpressionpagingwithcookie1)]  
  
## <a name="when-not-to-use-paging"></a>When not to use paging 


Paging depends on the common case where each row returned represents a unique entity record. There are some queries you can construct that will provide rows that combine data from the primary entity with related entities. This will result in multiple primary entity rows that refer to the same primary key value. If you depend on paging in this situation you will get inconsistent results.

In this case, here are several strategies you can apply.

### <a name="write-your-query-so-that-the-primary-entity-ids-are-unique"></a>Write your Query so that the primary entity ids are unique

If your query includes only one related entity and doesn't include many-to-many relationships, you can usually make the related entity the primary entity in your query to resolve this.

### <a name="dont-set-the-pagingcookie"></a>Don't set the PagingCookie 

Rather than include the paging, just set the `PageNumber`. This will work but there will be some performance impact for large data sets.

### <a name="split-your-query-into-multiple-queries"></a>Split your query into multiple queries

You can compose multiple queries which you then join the results together in your code.

### <a name="see-also"></a>Xem thêm  
 [Building Queries with QueryExpression](build-queries-with-queryexpression.md)   
 [Sample: Use QueryExpression with a paging cookie](sample-use-queryexpression-with-a-paging-cookie.md)   
 [Sample: Retrieve with one-to-many relationship](sample-retrieve-with-one-to-many-relationship.md)   
 [Using the QueryExpression Class](use-queryexpression-class.md)   
 [Page Large Result Sets with FetchXML](page-large-result-sets-with-fetchxml.md)
