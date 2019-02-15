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
# <a name="page-large-result-sets-with-fetchxml"></a><span data-ttu-id="69c2c-103">Page large result sets with FetchXML</span><span class="sxs-lookup"><span data-stu-id="69c2c-103">Page large result sets with FetchXML</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="69c2c-104">You can page the results of a FetchXML query by using the paging cookie.</span><span class="sxs-lookup"><span data-stu-id="69c2c-104">You can page the results of a FetchXML query by using the paging cookie.</span></span> <span data-ttu-id="69c2c-105">The paging cookie is a performance feature that makes paging in the application faster for very large datasets.</span><span class="sxs-lookup"><span data-stu-id="69c2c-105">The paging cookie is a performance feature that makes paging in the application faster for very large datasets.</span></span> <span data-ttu-id="69c2c-106">When you query for a set of records, the result will contain a value for the paging cookie.</span><span class="sxs-lookup"><span data-stu-id="69c2c-106">When you query for a set of records, the result will contain a value for the paging cookie.</span></span> <span data-ttu-id="69c2c-107">For better performance, you can pass that value when you retrieve the next set of records.</span><span class="sxs-lookup"><span data-stu-id="69c2c-107">For better performance, you can pass that value when you retrieve the next set of records.</span></span>  
  
 <span data-ttu-id="69c2c-108">FetchXML and <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> use different formats for their paging cookies.</span><span class="sxs-lookup"><span data-stu-id="69c2c-108">FetchXML and <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> use different formats for their paging cookies.</span></span> <span data-ttu-id="69c2c-109">If you convert from one query format to the other by using the <xref:Microsoft.Crm.Sdk.Messages.FetchXmlToQueryExpressionRequest> message or the <xref:Microsoft.Crm.Sdk.Messages.QueryExpressionToFetchXmlRequest> message, the paging cookie value is ignored.</span><span class="sxs-lookup"><span data-stu-id="69c2c-109">If you convert from one query format to the other by using the <xref:Microsoft.Crm.Sdk.Messages.FetchXmlToQueryExpressionRequest> message or the <xref:Microsoft.Crm.Sdk.Messages.QueryExpressionToFetchXmlRequest> message, the paging cookie value is ignored.</span></span> <span data-ttu-id="69c2c-110">In addition, if you request nonconsecutive pages, the paging cookie value is ignored.</span><span class="sxs-lookup"><span data-stu-id="69c2c-110">In addition, if you request nonconsecutive pages, the paging cookie value is ignored.</span></span>  
  
 <span data-ttu-id="69c2c-111">When you use the paging cookie with FetchXML, make sure that you use the correct encoding.</span><span class="sxs-lookup"><span data-stu-id="69c2c-111">When you use the paging cookie with FetchXML, make sure that you use the correct encoding.</span></span> <span data-ttu-id="69c2c-112">The following example shows the correct encoding when using the paging cookie with FetchXML:</span><span class="sxs-lookup"><span data-stu-id="69c2c-112">The following example shows the correct encoding when using the paging cookie with FetchXML:</span></span>  
  
```csharp  
strQueryXML = @"  
<fetch mapping='logical' paging-cookie='&lt;cookie page=&quot;1&quot;&gt;&lt;accountid last=&quot;{E062B974-7F8D-DC11-9048-0003FF27AC3B}&quot; first=&quot;{60B934EF-798D-DC11-9048-0003FF27AC3B}&quot;/&gt;&lt;/cookie&gt;' page='2' count='2'>  
 <entity name='account'>  
  <all-attributes/>  
 </entity>  
</fetch>";  
```  
  
## <a name="fetchxml-and-the-paging-cookie-example"></a><span data-ttu-id="69c2c-113">FetchXML and the Paging Cookie Example</span><span class="sxs-lookup"><span data-stu-id="69c2c-113">FetchXML and the Paging Cookie Example</span></span>  
 <span data-ttu-id="69c2c-114">The following example shows how to use the paging cookie with a FetchXML query.</span><span class="sxs-lookup"><span data-stu-id="69c2c-114">The following example shows how to use the paging cookie with a FetchXML query.</span></span> <span data-ttu-id="69c2c-115">For the complete sample code, see [Sample: Use FetchXML with a Paging Cookie](sample-use-fetchxml-paging-cookie.md).</span><span class="sxs-lookup"><span data-stu-id="69c2c-115">For the complete sample code, see [Sample: Use FetchXML with a Paging Cookie](sample-use-fetchxml-paging-cookie.md).</span></span>  
  
 [!code-csharp[Query#FetchPagingWithCookie1](../../snippets/csharp/CRMV8/query/cs/fetchpagingwithcookie1.cs#fetchpagingwithcookie1)]  

## <a name="when-not-to-use-paging-cookies"></a><span data-ttu-id="69c2c-116">When not to use paging cookies</span><span class="sxs-lookup"><span data-stu-id="69c2c-116">When not to use paging cookies</span></span>

<span data-ttu-id="69c2c-117">Paging cookies depend on the common case where each row returned represents a unique entity record.</span><span class="sxs-lookup"><span data-stu-id="69c2c-117">Paging cookies depend on the common case where each row returned represents a unique entity record.</span></span> <span data-ttu-id="69c2c-118">There are some queries you can construct using `link-entity` that will provide rows that combine data from the primary entity with related entities.</span><span class="sxs-lookup"><span data-stu-id="69c2c-118">There are some queries you can construct using `link-entity` that will provide rows that combine data from the primary entity with related entities.</span></span> <span data-ttu-id="69c2c-119">This will result in multiple primary entity rows that refer to the same primary key value.</span><span class="sxs-lookup"><span data-stu-id="69c2c-119">This will result in multiple primary entity rows that refer to the same primary key value.</span></span> <span data-ttu-id="69c2c-120">If you depend on paging cookies in this situation you will get inconsistent results.</span><span class="sxs-lookup"><span data-stu-id="69c2c-120">If you depend on paging cookies in this situation you will get inconsistent results.</span></span>

<span data-ttu-id="69c2c-121">In this case, here are several strategies you can apply.</span><span class="sxs-lookup"><span data-stu-id="69c2c-121">In this case, here are several strategies you can apply.</span></span>

### <a name="write-your-fetchxml-query-so-that-the-primary-entity-ids-are-unique"></a><span data-ttu-id="69c2c-122">Write your FetchXml Query so that the primary entity ids are unique</span><span class="sxs-lookup"><span data-stu-id="69c2c-122">Write your FetchXml Query so that the primary entity ids are unique</span></span>

<span data-ttu-id="69c2c-123">If your query includes only one link-entity and doesn't include many-to-many relationships, you can usually make the related entity the primary entity in your query to resolve this.</span><span class="sxs-lookup"><span data-stu-id="69c2c-123">If your query includes only one link-entity and doesn't include many-to-many relationships, you can usually make the related entity the primary entity in your query to resolve this.</span></span>

### <a name="dont-use-the-paging-cookie"></a><span data-ttu-id="69c2c-124">Don't use the paging cookie</span><span class="sxs-lookup"><span data-stu-id="69c2c-124">Don't use the paging cookie</span></span>

<span data-ttu-id="69c2c-125">Rather than include the paging cookie in your FetchXml, simply update the `page` value.</span><span class="sxs-lookup"><span data-stu-id="69c2c-125">Rather than include the paging cookie in your FetchXml, simply update the `page` value.</span></span> <span data-ttu-id="69c2c-126">This will work but there will be some performance impact.</span><span class="sxs-lookup"><span data-stu-id="69c2c-126">This will work but there will be some performance impact.</span></span>

### <a name="split-your-query-into-multiple-queries"></a><span data-ttu-id="69c2c-127">Split your query into multiple queries</span><span class="sxs-lookup"><span data-stu-id="69c2c-127">Split your query into multiple queries</span></span>

<span data-ttu-id="69c2c-128">You can compose multiple queries which you then join the results together in your code.</span><span class="sxs-lookup"><span data-stu-id="69c2c-128">You can compose multiple queries which you then join the results together in your code.</span></span>

### <a name="see-also"></a><span data-ttu-id="69c2c-129">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="69c2c-129">See also</span></span>  
 <span data-ttu-id="69c2c-130">[Sample: Use FetchXML with a Paging Cookie](sample-use-fetchxml-paging-cookie.md) </span><span class="sxs-lookup"><span data-stu-id="69c2c-130">[Sample: Use FetchXML with a Paging Cookie](sample-use-fetchxml-paging-cookie.md) </span></span>  
 <span data-ttu-id="69c2c-131">[Building Queries with FetchXML](build-queries-fetchxml.md) </span><span class="sxs-lookup"><span data-stu-id="69c2c-131">[Building Queries with FetchXML](build-queries-fetchxml.md) </span></span>  
 <span data-ttu-id="69c2c-132">[Fiscal date query operators in FetchXML](fiscal-date-older-datetime-query-operators-fetchxml.md) </span><span class="sxs-lookup"><span data-stu-id="69c2c-132">[Fiscal date query operators in FetchXML](fiscal-date-older-datetime-query-operators-fetchxml.md) </span></span>  
 <span data-ttu-id="69c2c-133">[Using FetchXML](use-fetchxml-construct-query.md) </span><span class="sxs-lookup"><span data-stu-id="69c2c-133">[Using FetchXML](use-fetchxml-construct-query.md) </span></span>  
 [<span data-ttu-id="69c2c-134">Page large result sets with QueryExpression</span><span class="sxs-lookup"><span data-stu-id="69c2c-134">Page large result sets with QueryExpression</span></span>](page-large-result-sets-with-queryexpression.md)
