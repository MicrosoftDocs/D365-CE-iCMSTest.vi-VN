---
title: Retrieve data with queries using SDK assemblies (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: There are several ways to create queries in Dynamics 365 for Customer Engagement (online) Customer Engagement. This topic lists the basic capabilities of each query style
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
- queries, using to retrieve data
- creating queries to retrieve data, by using FetchXML
- creating queries to retrieve data, by using .NET language-Integrated Query (LINQ)
- retrieving data, by creating queries
- creating queries to retrieve data, early and late binding scenarios
- creating queries to retrieve data, by using QueryExpression
ms.assetid: e9d32d0c-c0f1-43bf-8bc8-a1f8836f661a
caps.latest.revision: 30
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0428853dd8ef84b87eb86b955dcb5d45211283a1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387343"
---
# <a name="retrieve-data-with-queries-using-sdk-assemblies"></a><span data-ttu-id="5e019-104">Retrieve data with queries using SDK assemblies</span><span class="sxs-lookup"><span data-stu-id="5e019-104">Retrieve data with queries using SDK assemblies</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5e019-105">There are several ways to create queries in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="5e019-105">There are several ways to create queries in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="5e019-106">You can use [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] in early and late binding scenarios, you can write queries by using FetchXML, the proprietary [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps query language, or you can build a query by using QueryExpression and the <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> class.</span><span class="sxs-lookup"><span data-stu-id="5e019-106">You can use [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] in early and late binding scenarios, you can write queries by using FetchXML, the proprietary [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps query language, or you can build a query by using QueryExpression and the <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> class.</span></span>  
  
 <span data-ttu-id="5e019-107">The following table lists the basic capabilities of each query style.</span><span class="sxs-lookup"><span data-stu-id="5e019-107">The following table lists the basic capabilities of each query style.</span></span>  
  
|<span data-ttu-id="5e019-108">Query style</span><span class="sxs-lookup"><span data-stu-id="5e019-108">Query style</span></span>|<span data-ttu-id="5e019-109">Khả năng</span><span class="sxs-lookup"><span data-stu-id="5e019-109">Capabilities</span></span>|  
|-----------------|------------------|  
|<span data-ttu-id="5e019-110">XML tìm nạp dữ liệu</span><span class="sxs-lookup"><span data-stu-id="5e019-110">FetchXML</span></span>|<span data-ttu-id="5e019-111">Supports all the features of `QueryExpression` plus aggregates and grouping.</span><span class="sxs-lookup"><span data-stu-id="5e019-111">Supports all the features of `QueryExpression` plus aggregates and grouping.</span></span> <span data-ttu-id="5e019-112">Queries are built as XML statements.</span><span class="sxs-lookup"><span data-stu-id="5e019-112">Queries are built as XML statements.</span></span>|  
|<span data-ttu-id="5e019-113">QueryExpression</span><span class="sxs-lookup"><span data-stu-id="5e019-113">QueryExpression</span></span>|<span data-ttu-id="5e019-114">Queries are built as an object model.</span><span class="sxs-lookup"><span data-stu-id="5e019-114">Queries are built as an object model.</span></span> <span data-ttu-id="5e019-115">Supports all the features in FetchXML except for aggregates and grouping.</span><span class="sxs-lookup"><span data-stu-id="5e019-115">Supports all the features in FetchXML except for aggregates and grouping.</span></span>|  
|<span data-ttu-id="5e019-116">LINQ</span><span class="sxs-lookup"><span data-stu-id="5e019-116">LINQ</span></span>|<span data-ttu-id="5e019-117">Queries are built using standard language, but internally uses `QueryExpression` so is limited to the features of `QueryExpression`.</span><span class="sxs-lookup"><span data-stu-id="5e019-117">Queries are built using standard language, but internally uses `QueryExpression` so is limited to the features of `QueryExpression`.</span></span>|  
  
 <span data-ttu-id="5e019-118">Use FetchXML to create queries that return aggregates such as the sum of a value for all returned records.</span><span class="sxs-lookup"><span data-stu-id="5e019-118">Use FetchXML to create queries that return aggregates such as the sum of a value for all returned records.</span></span> <span data-ttu-id="5e019-119">You can also perform “group by” operations with FetchXML.</span><span class="sxs-lookup"><span data-stu-id="5e019-119">You can also perform “group by” operations with FetchXML.</span></span>  
  
 [!INCLUDE[pn_LINQ](../../includes/pn-linq.md)] <span data-ttu-id="5e019-120">uses standard query patterns.</span><span class="sxs-lookup"><span data-stu-id="5e019-120">uses standard query patterns.</span></span> <span data-ttu-id="5e019-121">The <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> class contains the LINQ query provider and is efficient at creating multiple associations.</span><span class="sxs-lookup"><span data-stu-id="5e019-121">The <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> class contains the LINQ query provider and is efficient at creating multiple associations.</span></span>  
  
 <span data-ttu-id="5e019-122">The following messages are useful for working with queries when you want to convert between FetchXml and QueryExpression: <xref:Microsoft.Crm.Sdk.Messages.FetchXmlToQueryExpressionRequest> and <xref:Microsoft.Crm.Sdk.Messages.QueryExpressionToFetchXmlRequest>.</span><span class="sxs-lookup"><span data-stu-id="5e019-122">The following messages are useful for working with queries when you want to convert between FetchXml and QueryExpression: <xref:Microsoft.Crm.Sdk.Messages.FetchXmlToQueryExpressionRequest> and <xref:Microsoft.Crm.Sdk.Messages.QueryExpressionToFetchXmlRequest>.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="5e019-123">In this section</span><span class="sxs-lookup"><span data-stu-id="5e019-123">In this section</span></span>  
 [<span data-ttu-id="5e019-124">Build Queries with LINQ (.NET Language-Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="5e019-124">Build Queries with LINQ (.NET Language-Integrated Query)</span></span>](build-queries-with-linq-net-language-integrated-query.md)  
  
 [<span data-ttu-id="5e019-125">Building Queries with FetchXML</span><span class="sxs-lookup"><span data-stu-id="5e019-125">Building Queries with FetchXML</span></span>](build-queries-fetchxml.md)  
  
 [<span data-ttu-id="5e019-126">Building Queries with QueryExpression</span><span class="sxs-lookup"><span data-stu-id="5e019-126">Building Queries with QueryExpression</span></span>](build-queries-with-queryexpression.md)  
  
 [<span data-ttu-id="5e019-127">Dữ liệu phân cấp truy vấn</span><span class="sxs-lookup"><span data-stu-id="5e019-127">Query hierarchical data</span></span>](query-hierarchical-data.md)  
  
 [<span data-ttu-id="5e019-128">Retrieve Records for Many-To-Many Relationships using Intersect Entities</span><span class="sxs-lookup"><span data-stu-id="5e019-128">Retrieve Records for Many-To-Many Relationships using Intersect Entities</span></span>](retrieve-records-many-to-many-relationships-intersect-entities.md)  
  
 [<span data-ttu-id="5e019-129">FetchXML Schema</span><span class="sxs-lookup"><span data-stu-id="5e019-129">FetchXML Schema</span></span>](fetchxml-schema.md)
