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
# <a name="page-large-result-sets-with-queryexpression"></a><span data-ttu-id="d164d-104">Page large result sets with QueryExpression</span><span class="sxs-lookup"><span data-stu-id="d164d-104">Page large result sets with QueryExpression</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d164d-105">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the paging cookie feature to make paging in an application faster for large datasets.</span><span class="sxs-lookup"><span data-stu-id="d164d-105">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the paging cookie feature to make paging in an application faster for large datasets.</span></span> <span data-ttu-id="d164d-106">The feature is available in both FetchXML and <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> queries.</span><span class="sxs-lookup"><span data-stu-id="d164d-106">The feature is available in both FetchXML and <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> queries.</span></span> <span data-ttu-id="d164d-107">When you use the paging cookie feature when querying a set of records, the result contains a value for the paging cookie.</span><span class="sxs-lookup"><span data-stu-id="d164d-107">When you use the paging cookie feature when querying a set of records, the result contains a value for the paging cookie.</span></span> <span data-ttu-id="d164d-108">To improve system performance, you can then pass that value when you retrieve the next set of records.</span><span class="sxs-lookup"><span data-stu-id="d164d-108">To improve system performance, you can then pass that value when you retrieve the next set of records.</span></span>  
  
 <span data-ttu-id="d164d-109"><xref:Microsoft.Xrm.Sdk.Query.QueryExpression> and FetchXML use different formats for their paging cookies.</span><span class="sxs-lookup"><span data-stu-id="d164d-109"><xref:Microsoft.Xrm.Sdk.Query.QueryExpression> and FetchXML use different formats for their paging cookies.</span></span> <span data-ttu-id="d164d-110">If you convert from one query format to the other by using the <xref:Microsoft.Crm.Sdk.Messages.QueryExpressionToFetchXmlRequest> message or the <xref:Microsoft.Crm.Sdk.Messages.FetchXmlToQueryExpressionRequest> message, the paging cookie value is ignored.</span><span class="sxs-lookup"><span data-stu-id="d164d-110">If you convert from one query format to the other by using the <xref:Microsoft.Crm.Sdk.Messages.QueryExpressionToFetchXmlRequest> message or the <xref:Microsoft.Crm.Sdk.Messages.FetchXmlToQueryExpressionRequest> message, the paging cookie value is ignored.</span></span> <span data-ttu-id="d164d-111">In addition, if you request nonconsecutive pages, the paging cookie value is ignored.</span><span class="sxs-lookup"><span data-stu-id="d164d-111">In addition, if you request nonconsecutive pages, the paging cookie value is ignored.</span></span>  
  
<a name="QueryExpression"></a> 

## <a name="using-a-paging-cookie-with-queryexpression"></a><span data-ttu-id="d164d-112">Using a paging cookie with QueryExpression</span><span class="sxs-lookup"><span data-stu-id="d164d-112">Using a paging cookie with QueryExpression</span></span>  
 <span data-ttu-id="d164d-113">The following example shows how to use the paging cookie with a query expression.</span><span class="sxs-lookup"><span data-stu-id="d164d-113">The following example shows how to use the paging cookie with a query expression.</span></span> <span data-ttu-id="d164d-114">For the complete sample code, see [Sample: Use QueryExpression with a paging cookie](sample-use-queryexpression-with-a-paging-cookie.md).</span><span class="sxs-lookup"><span data-stu-id="d164d-114">For the complete sample code, see [Sample: Use QueryExpression with a paging cookie](sample-use-queryexpression-with-a-paging-cookie.md).</span></span>  
  
 [!code-csharp[Query#QueryExpressionPagingWithCookie1](../../snippets/csharp/CRMV8/query/cs/queryexpressionpagingwithcookie1.cs#queryexpressionpagingwithcookie1)]  
  
## <a name="when-not-to-use-paging"></a><span data-ttu-id="d164d-115">When not to use paging</span><span class="sxs-lookup"><span data-stu-id="d164d-115">When not to use paging</span></span> 


<span data-ttu-id="d164d-116">Paging depends on the common case where each row returned represents a unique entity record.</span><span class="sxs-lookup"><span data-stu-id="d164d-116">Paging depends on the common case where each row returned represents a unique entity record.</span></span> <span data-ttu-id="d164d-117">There are some queries you can construct that will provide rows that combine data from the primary entity with related entities.</span><span class="sxs-lookup"><span data-stu-id="d164d-117">There are some queries you can construct that will provide rows that combine data from the primary entity with related entities.</span></span> <span data-ttu-id="d164d-118">This will result in multiple primary entity rows that refer to the same primary key value.</span><span class="sxs-lookup"><span data-stu-id="d164d-118">This will result in multiple primary entity rows that refer to the same primary key value.</span></span> <span data-ttu-id="d164d-119">If you depend on paging in this situation you will get inconsistent results.</span><span class="sxs-lookup"><span data-stu-id="d164d-119">If you depend on paging in this situation you will get inconsistent results.</span></span>

<span data-ttu-id="d164d-120">In this case, here are several strategies you can apply.</span><span class="sxs-lookup"><span data-stu-id="d164d-120">In this case, here are several strategies you can apply.</span></span>

### <a name="write-your-query-so-that-the-primary-entity-ids-are-unique"></a><span data-ttu-id="d164d-121">Write your Query so that the primary entity ids are unique</span><span class="sxs-lookup"><span data-stu-id="d164d-121">Write your Query so that the primary entity ids are unique</span></span>

<span data-ttu-id="d164d-122">If your query includes only one related entity and doesn't include many-to-many relationships, you can usually make the related entity the primary entity in your query to resolve this.</span><span class="sxs-lookup"><span data-stu-id="d164d-122">If your query includes only one related entity and doesn't include many-to-many relationships, you can usually make the related entity the primary entity in your query to resolve this.</span></span>

### <a name="dont-set-the-pagingcookie"></a><span data-ttu-id="d164d-123">Don't set the PagingCookie</span><span class="sxs-lookup"><span data-stu-id="d164d-123">Don't set the PagingCookie</span></span> 

<span data-ttu-id="d164d-124">Rather than include the paging, just set the `PageNumber`.</span><span class="sxs-lookup"><span data-stu-id="d164d-124">Rather than include the paging, just set the `PageNumber`.</span></span> <span data-ttu-id="d164d-125">This will work but there will be some performance impact for large data sets.</span><span class="sxs-lookup"><span data-stu-id="d164d-125">This will work but there will be some performance impact for large data sets.</span></span>

### <a name="split-your-query-into-multiple-queries"></a><span data-ttu-id="d164d-126">Split your query into multiple queries</span><span class="sxs-lookup"><span data-stu-id="d164d-126">Split your query into multiple queries</span></span>

<span data-ttu-id="d164d-127">You can compose multiple queries which you then join the results together in your code.</span><span class="sxs-lookup"><span data-stu-id="d164d-127">You can compose multiple queries which you then join the results together in your code.</span></span>

### <a name="see-also"></a><span data-ttu-id="d164d-128">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d164d-128">See also</span></span>  
 <span data-ttu-id="d164d-129">[Building Queries with QueryExpression](build-queries-with-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="d164d-129">[Building Queries with QueryExpression](build-queries-with-queryexpression.md) </span></span>  
 <span data-ttu-id="d164d-130">[Sample: Use QueryExpression with a paging cookie](sample-use-queryexpression-with-a-paging-cookie.md) </span><span class="sxs-lookup"><span data-stu-id="d164d-130">[Sample: Use QueryExpression with a paging cookie](sample-use-queryexpression-with-a-paging-cookie.md) </span></span>  
 <span data-ttu-id="d164d-131">[Sample: Retrieve with one-to-many relationship](sample-retrieve-with-one-to-many-relationship.md) </span><span class="sxs-lookup"><span data-stu-id="d164d-131">[Sample: Retrieve with one-to-many relationship](sample-retrieve-with-one-to-many-relationship.md) </span></span>  
 <span data-ttu-id="d164d-132">[Using the QueryExpression Class](use-queryexpression-class.md) </span><span class="sxs-lookup"><span data-stu-id="d164d-132">[Using the QueryExpression Class](use-queryexpression-class.md) </span></span>  
 [<span data-ttu-id="d164d-133">Page Large Result Sets with FetchXML</span><span class="sxs-lookup"><span data-stu-id="d164d-133">Page Large Result Sets with FetchXML</span></span>](page-large-result-sets-with-fetchxml.md)
