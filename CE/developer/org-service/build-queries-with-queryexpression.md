---
title: Build queries with QueryExpression (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how you can use the QueryExpression class to programmatically build a query containing data filters and search conditions that define the scope of a database search
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
- saving queries
- query expressions, used for single-object searches
- complex queries, introduction
- building queries by using QueryExpression, creating queries that contain data filters and search conditions
- query expressions, about; definition; using
- QueryBase; QueryExpression; and QueryByAttribute classes, differences between
- building queries by using QueryExpression, introduction
- queries, samples
- QueryBase; QueryExpression; and QueryByAttribute classes, introduction to building queries
- creating queries to retrieve records, available types in CRM
- queries, simple
- queries, saving
- queries, complex
ms.assetid: 44d32c72-284a-43d3-96f5-d9b0a0486949
caps.latest.revision: 48
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6dd06870faadcab6e4c352d0daec69978b4a63cd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388094"
---
# <a name="build-queries-with-queryexpression"></a><span data-ttu-id="51765-103">Build queries with QueryExpression</span><span class="sxs-lookup"><span data-stu-id="51765-103">Build queries with QueryExpression</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="51765-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps, you can use the <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> class to programmatically build a query containing data filters and search conditions that define the scope of a database search.</span><span class="sxs-lookup"><span data-stu-id="51765-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps, you can use the <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> class to programmatically build a query containing data filters and search conditions that define the scope of a database search.</span></span> <span data-ttu-id="51765-105">A query expression is used for single-object searches.</span><span class="sxs-lookup"><span data-stu-id="51765-105">A query expression is used for single-object searches.</span></span> <span data-ttu-id="51765-106">For example, you can create a search to return all accounts that match certain search criteria.</span><span class="sxs-lookup"><span data-stu-id="51765-106">For example, you can create a search to return all accounts that match certain search criteria.</span></span> <span data-ttu-id="51765-107">The <xref:Microsoft.Xrm.Sdk.Query.QueryBase> class is the base class for query expressions.</span><span class="sxs-lookup"><span data-stu-id="51765-107">The <xref:Microsoft.Xrm.Sdk.Query.QueryBase> class is the base class for query expressions.</span></span> <span data-ttu-id="51765-108">There are two derived classes: <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> and <xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute>.</span><span class="sxs-lookup"><span data-stu-id="51765-108">There are two derived classes: <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> and <xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute>.</span></span> <span data-ttu-id="51765-109">The `QueryExpression` class supports complex queries.</span><span class="sxs-lookup"><span data-stu-id="51765-109">The `QueryExpression` class supports complex queries.</span></span> <span data-ttu-id="51765-110">The `QueryByAttribute` class is a simple means to search for entities where attributes match specified values.</span><span class="sxs-lookup"><span data-stu-id="51765-110">The `QueryByAttribute` class is a simple means to search for entities where attributes match specified values.</span></span>  
  
 <span data-ttu-id="51765-111">Query expressions are used in methods that retrieve more than one record, such as the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span><span class="sxs-lookup"><span data-stu-id="51765-111">Query expressions are used in methods that retrieve more than one record, such as the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span></span> <span data-ttu-id="51765-112">method, in messages that perform an operation on a result set specified by a query expression, such as <xref:Microsoft.Crm.Sdk.Messages.BulkDeleteRequest> and when the ID for a specific record is not known.</span><span class="sxs-lookup"><span data-stu-id="51765-112">method, in messages that perform an operation on a result set specified by a query expression, such as <xref:Microsoft.Crm.Sdk.Messages.BulkDeleteRequest> and when the ID for a specific record is not known.</span></span>  
  
 <span data-ttu-id="51765-113">In addition, there is a new attribute on the organization entity, `Organization.QuickFindRecordLimitEnabled`.</span><span class="sxs-lookup"><span data-stu-id="51765-113">In addition, there is a new attribute on the organization entity, `Organization.QuickFindRecordLimitEnabled`.</span></span> <span data-ttu-id="51765-114">When this `Boolean` attribute is `true`, a limit is imposed on quick find queries.</span><span class="sxs-lookup"><span data-stu-id="51765-114">When this `Boolean` attribute is `true`, a limit is imposed on quick find queries.</span></span> <span data-ttu-id="51765-115">If a user provides search criteria in quick find that is not selective enough, the system detects this and stops the search.</span><span class="sxs-lookup"><span data-stu-id="51765-115">If a user provides search criteria in quick find that is not selective enough, the system detects this and stops the search.</span></span> <span data-ttu-id="51765-116">This supports a faster form of quick find and can make a big performance difference.</span><span class="sxs-lookup"><span data-stu-id="51765-116">This supports a faster form of quick find and can make a big performance difference.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="51765-117">Don’t retrieve all attributes in a query because of the negative effect on performance.</span><span class="sxs-lookup"><span data-stu-id="51765-117">Don’t retrieve all attributes in a query because of the negative effect on performance.</span></span> <span data-ttu-id="51765-118">This is particularly true if the query is used as a parameter to an update request.</span><span class="sxs-lookup"><span data-stu-id="51765-118">This is particularly true if the query is used as a parameter to an update request.</span></span> <span data-ttu-id="51765-119">In an update, if all attributes are included this sets all field values, even if they are unchanged, and often triggers cascaded updates to child records.</span><span class="sxs-lookup"><span data-stu-id="51765-119">In an update, if all attributes are included this sets all field values, even if they are unchanged, and often triggers cascaded updates to child records.</span></span>  
  
 <span data-ttu-id="51765-120">There are two additional ways to create queries to retrieve records from [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="51765-120">There are two additional ways to create queries to retrieve records from [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span></span> <span data-ttu-id="51765-121">FetchXML, the proprietary [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps query language, can be used to perform some queries by using XML-based queries.</span><span class="sxs-lookup"><span data-stu-id="51765-121">FetchXML, the proprietary [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps query language, can be used to perform some queries by using XML-based queries.</span></span> <span data-ttu-id="51765-122">For more information, see [Building Queries with FetchXML](build-queries-fetchxml.md).</span><span class="sxs-lookup"><span data-stu-id="51765-122">For more information, see [Building Queries with FetchXML](build-queries-fetchxml.md).</span></span> <span data-ttu-id="51765-123">You can also use [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] to write queries.</span><span class="sxs-lookup"><span data-stu-id="51765-123">You can also use [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] to write queries.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="51765-124">[Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md).</span><span class="sxs-lookup"><span data-stu-id="51765-124">[Build Queries with LINQ (.NET Language-Integrated Query)](build-queries-with-linq-net-language-integrated-query.md).</span></span>  
  
 <span data-ttu-id="51765-125">To save a query, you can convert it to FetchXML by using the <xref:Microsoft.Crm.Sdk.Messages.QueryExpressionToFetchXmlRequest> and save it as a saved view by using the `userquery` entity.</span><span class="sxs-lookup"><span data-stu-id="51765-125">To save a query, you can convert it to FetchXML by using the <xref:Microsoft.Crm.Sdk.Messages.QueryExpressionToFetchXmlRequest> and save it as a saved view by using the `userquery` entity.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="51765-126">In This Section</span><span class="sxs-lookup"><span data-stu-id="51765-126">In This Section</span></span>  
 [<span data-ttu-id="51765-127">Using the QueryByAttribute Class</span><span class="sxs-lookup"><span data-stu-id="51765-127">Using the QueryByAttribute Class</span></span>](use-querybyattribute-class.md)  
  
 [<span data-ttu-id="51765-128">Using the QueryExpression Class</span><span class="sxs-lookup"><span data-stu-id="51765-128">Using the QueryExpression Class</span></span>](use-queryexpression-class.md)  
  
 [<span data-ttu-id="51765-129">Using the ColumnSet Class</span><span class="sxs-lookup"><span data-stu-id="51765-129">Using the ColumnSet Class</span></span>](use-the-columnset-class.md)  
  
 [<span data-ttu-id="51765-130">Using the ConditionExpression Class</span><span class="sxs-lookup"><span data-stu-id="51765-130">Using the ConditionExpression Class</span></span>](use-conditionexpression-class.md)  
  
 [<span data-ttu-id="51765-131">Using the FilterExpression Class</span><span class="sxs-lookup"><span data-stu-id="51765-131">Using the FilterExpression Class</span></span>](use-filterexpression-class.md)  
  
 [<span data-ttu-id="51765-132">Use a left outer join in QueryExpression to query for records "not in"</span><span class="sxs-lookup"><span data-stu-id="51765-132">Use a left outer join in QueryExpression to query for records "not in"</span></span>](use-left-outer-join-queryexpression-query-records-not-in.md)  
  
 [<span data-ttu-id="51765-133">Testing for a Null Value</span><span class="sxs-lookup"><span data-stu-id="51765-133">Testing for a Null Value</span></span>](test-null-value.md)  
  
 [<span data-ttu-id="51765-134">Page Large Result Sets with Query Expression and FetchXML</span><span class="sxs-lookup"><span data-stu-id="51765-134">Page Large Result Sets with Query Expression and FetchXML</span></span>](page-large-result-sets-with-queryexpression.md)  
  
 [<span data-ttu-id="51765-135">Sample: Retrieve With One-To-Many Relationship</span><span class="sxs-lookup"><span data-stu-id="51765-135">Sample: Retrieve With One-To-Many Relationship</span></span>](sample-retrieve-with-one-to-many-relationship.md)  
  
 [<span data-ttu-id="51765-136">Sample: Retrieve Multiple with Query By Attribute</span><span class="sxs-lookup"><span data-stu-id="51765-136">Sample: Retrieve Multiple with Query By Attribute</span></span>](sample-retrieve-multiple-querybyattribute-class.md)  
  
 [<span data-ttu-id="51765-137">Sample: Retrieve Multiple with Query Expression</span><span class="sxs-lookup"><span data-stu-id="51765-137">Sample: Retrieve Multiple with Query Expression</span></span>](sample-retrieve-multiple-queryexpression-class.md)  
  
 [<span data-ttu-id="51765-138">Sample: Use QueryExpression with a paging cookie</span><span class="sxs-lookup"><span data-stu-id="51765-138">Sample: Use QueryExpression with a paging cookie</span></span>](sample-use-queryexpression-with-a-paging-cookie.md)  
  
## <a name="reference"></a><span data-ttu-id="51765-139">Tham chiếu</span><span class="sxs-lookup"><span data-stu-id="51765-139">Reference</span></span>  
 <xref:Microsoft.Xrm.Sdk.Query.QueryBase>  
  
 <xref:Microsoft.Xrm.Sdk.Query.QueryExpression>  
  
 <xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute>  
  
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>  
  
 <xref:Microsoft.Xrm.Sdk.Query.ColumnSet>  
  
 <xref:Microsoft.Xrm.Sdk.Query.ConditionExpression>  
  
 <xref:Microsoft.Xrm.Sdk.Query.FilterExpression>  
  
 <xref:Microsoft.Xrm.Sdk.Query.PagingInfo.PagingCookie>  
  
### <a name="see-also"></a><span data-ttu-id="51765-140">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="51765-140">See also</span></span>  
 [<span data-ttu-id="51765-141">Sample: Convert queries between Fetch and QueryExpression</span><span class="sxs-lookup"><span data-stu-id="51765-141">Sample: Convert queries between Fetch and QueryExpression</span></span>](sample-convert-queries-fetch-queryexpression.md)
