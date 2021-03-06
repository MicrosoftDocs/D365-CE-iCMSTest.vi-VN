---
title: Page large result sets with FetchXML (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how you can page the results of a FetchXML query by using the paging cookie
ms.custom: ''
ms.date: 09/13/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: cd32c68c-fb8a-4018-90a3-49c6a80ca7b4
caps.latest.revision: 17
author: mayadumesh
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6d8a2e95d42d98bcd84df0c9aa980d775e101611
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387109"
---
# <a name="page-large-result-sets-with-fetchxml"></a>Page large result sets with FetchXML

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

You can page the results of a FetchXML query by using the paging cookie. The paging cookie is a performance feature that makes paging in the application faster for very large datasets. When you query for a set of records, the result will contain a value for the paging cookie. For better performance, you can pass that value when you retrieve the next set of records.  
  
 FetchXML and <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> use different formats for their paging cookies. If you convert from one query format to the other by using the <xref:Microsoft.Crm.Sdk.Messages.FetchXmlToQueryExpressionRequest> message or the <xref:Microsoft.Crm.Sdk.Messages.QueryExpressionToFetchXmlRequest> message, the paging cookie value is ignored. In addition, if you request nonconsecutive pages, the paging cookie value is ignored.  
  
 When you use the paging cookie with FetchXML, make sure that you use the correct encoding. The following example shows the correct encoding when using the paging cookie with FetchXML:  
  
```csharp  
strQueryXML = @"  
<fetch mapping='logical' paging-cookie='&lt;cookie page=&quot;1&quot;&gt;&lt;accountid last=&quot;{E062B974-7F8D-DC11-9048-0003FF27AC3B}&quot; first=&quot;{60B934EF-798D-DC11-9048-0003FF27AC3B}&quot;/&gt;&lt;/cookie&gt;' page='2' count='2'>  
 <entity name='account'>  
  <all-attributes/>  
 </entity>  
</fetch>";  
```  
  
## <a name="fetchxml-and-the-paging-cookie-example"></a>FetchXML and the Paging Cookie Example  
 The following example shows how to use the paging cookie with a FetchXML query. For the complete sample code, see [Sample: Use FetchXML with a Paging Cookie](sample-use-fetchxml-paging-cookie.md).  
  
 [!code-csharp[Query#FetchPagingWithCookie1](../../snippets/csharp/CRMV8/query/cs/fetchpagingwithcookie1.cs#fetchpagingwithcookie1)]  

## <a name="when-not-to-use-paging-cookies"></a>When not to use paging cookies

Paging cookies depend on the common case where each row returned represents a unique entity record. There are some queries you can construct using `link-entity` that will provide rows that combine data from the primary entity with related entities. This will result in multiple primary entity rows that refer to the same primary key value. If you depend on paging cookies in this situation you will get inconsistent results.

In this case, here are several strategies you can apply.

### <a name="write-your-fetchxml-query-so-that-the-primary-entity-ids-are-unique"></a>Write your FetchXml Query so that the primary entity ids are unique

If your query includes only one link-entity and doesn't include many-to-many relationships, you can usually make the related entity the primary entity in your query to resolve this.

### <a name="dont-use-the-paging-cookie"></a>Don't use the paging cookie

Rather than include the paging cookie in your FetchXml, simply update the `page` value. This will work but there will be some performance impact.

### <a name="split-your-query-into-multiple-queries"></a>Split your query into multiple queries

You can compose multiple queries which you then join the results together in your code.

### <a name="see-also"></a>Xem thêm  
 [Sample: Use FetchXML with a Paging Cookie](sample-use-fetchxml-paging-cookie.md)   
 [Building Queries with FetchXML](build-queries-fetchxml.md)   
 [Fiscal date query operators in FetchXML](fiscal-date-older-datetime-query-operators-fetchxml.md)   
 [Using FetchXML](use-fetchxml-construct-query.md)   
 [Page large result sets with QueryExpression](page-large-result-sets-with-queryexpression.md)
