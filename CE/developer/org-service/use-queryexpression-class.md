---
title: Use the QueryExpression class (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: In Dynamics 365 for Customer Engagement (online) Customer Engagement, you can use the QueryExpression class to build complex queries for use with the IOrganizationService.QueryBase) method or the RetrieveMultipleRequest message
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
- building queries by using QueryExpression, QueryExpression class
- QueryExpression class, building complex queries
- QueryExpression class, obtaining record counts with the ReturnTotalRecordCount property
- QueryExpression class, difference between the QueryByAttribute class
- using the QueryExpression class
- QueryExpression class, about; properties for; and code example
ms.assetid: f5d2195b-8cae-49d6-a493-6f8b92e7f54e
caps.latest.revision: 29
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: cd1a065fa135c812c9b05d827e9a08cbdff0fb36
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388326"
---
# <a name="use-the-queryexpression-class"></a><span data-ttu-id="f1e89-103">Use the QueryExpression class</span><span class="sxs-lookup"><span data-stu-id="f1e89-103">Use the QueryExpression class</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="f1e89-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> class to build complex queries for use with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span><span class="sxs-lookup"><span data-stu-id="f1e89-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> class to build complex queries for use with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span></span> <span data-ttu-id="f1e89-105">method or the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest> message.</span><span class="sxs-lookup"><span data-stu-id="f1e89-105">method or the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest> message.</span></span> <span data-ttu-id="f1e89-106">You can set query parameters to the <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> by using the <xref:Microsoft.Xrm.Sdk.Query.ConditionExpression>, <xref:Microsoft.Xrm.Sdk.Query.ColumnSet>, and <xref:Microsoft.Xrm.Sdk.Query.FilterExpression> classes.</span><span class="sxs-lookup"><span data-stu-id="f1e89-106">You can set query parameters to the <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> by using the <xref:Microsoft.Xrm.Sdk.Query.ConditionExpression>, <xref:Microsoft.Xrm.Sdk.Query.ColumnSet>, and <xref:Microsoft.Xrm.Sdk.Query.FilterExpression> classes.</span></span>  
  
 <span data-ttu-id="f1e89-107">The <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> class lets you create complex queries.</span><span class="sxs-lookup"><span data-stu-id="f1e89-107">The <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> class lets you create complex queries.</span></span> <span data-ttu-id="f1e89-108">The <xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute> class is designed to be a simple way to search for entities where attributes match specified values.</span><span class="sxs-lookup"><span data-stu-id="f1e89-108">The <xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute> class is designed to be a simple way to search for entities where attributes match specified values.</span></span>  
  
 <span data-ttu-id="f1e89-109">The following table lists the properties that you set to create a query expression.</span><span class="sxs-lookup"><span data-stu-id="f1e89-109">The following table lists the properties that you set to create a query expression.</span></span>  
  
|<span data-ttu-id="f1e89-110">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="f1e89-110">Property</span></span>|<span data-ttu-id="f1e89-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="f1e89-111">Description</span></span>|  
|--------------|-----------------|  
|<xref:Microsoft.Xrm.Sdk.Query.QueryExpression.EntityName>|<span data-ttu-id="f1e89-112">Specifies which type of entity will be retrieved.</span><span class="sxs-lookup"><span data-stu-id="f1e89-112">Specifies which type of entity will be retrieved.</span></span> <span data-ttu-id="f1e89-113">A query expression can only retrieve a collection of one entity type.</span><span class="sxs-lookup"><span data-stu-id="f1e89-113">A query expression can only retrieve a collection of one entity type.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Query.QueryExpression.ColumnSet>|<span data-ttu-id="f1e89-114">Specifies the set of attributes (columns) to retrieve.</span><span class="sxs-lookup"><span data-stu-id="f1e89-114">Specifies the set of attributes (columns) to retrieve.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Query.QueryExpression.Criteria>|<span data-ttu-id="f1e89-115">Specifies complex conditional and logical filter expressions that filter the results of the query.</span><span class="sxs-lookup"><span data-stu-id="f1e89-115">Specifies complex conditional and logical filter expressions that filter the results of the query.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Query.QueryExpression.Distinct>|<span data-ttu-id="f1e89-116">Specifies whether the results of the query contain duplicate records.</span><span class="sxs-lookup"><span data-stu-id="f1e89-116">Specifies whether the results of the query contain duplicate records.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Query.QueryExpression.LinkEntities>|<span data-ttu-id="f1e89-117">Specifies the links between multiple entity types.</span><span class="sxs-lookup"><span data-stu-id="f1e89-117">Specifies the links between multiple entity types.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Query.QueryExpression.Orders>|<span data-ttu-id="f1e89-118">Specifies the order in which the records are returned from the query.</span><span class="sxs-lookup"><span data-stu-id="f1e89-118">Specifies the order in which the records are returned from the query.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Query.QueryExpression.PageInfo>|<span data-ttu-id="f1e89-119">Specifies the number of pages and the number of records per page returned from the query.</span><span class="sxs-lookup"><span data-stu-id="f1e89-119">Specifies the number of pages and the number of records per page returned from the query.</span></span>|  
  
<a name="record_count"></a>   
## <a name="record-count"></a><span data-ttu-id="f1e89-120">Record count</span><span class="sxs-lookup"><span data-stu-id="f1e89-120">Record count</span></span>  
 <span data-ttu-id="f1e89-121">To find out how many records the query returned, set the <xref:Microsoft.Xrm.Sdk.Query.PagingInfo.ReturnTotalRecordCount> property to true before executing the query.</span><span class="sxs-lookup"><span data-stu-id="f1e89-121">To find out how many records the query returned, set the <xref:Microsoft.Xrm.Sdk.Query.PagingInfo.ReturnTotalRecordCount> property to true before executing the query.</span></span> <span data-ttu-id="f1e89-122">When you do this, the <xref:Microsoft.Xrm.Sdk.EntityCollection.TotalRecordCount> will be set.</span><span class="sxs-lookup"><span data-stu-id="f1e89-122">When you do this, the <xref:Microsoft.Xrm.Sdk.EntityCollection.TotalRecordCount> will be set.</span></span> <span data-ttu-id="f1e89-123">Otherwise, this value will be -1.</span><span class="sxs-lookup"><span data-stu-id="f1e89-123">Otherwise, this value will be -1.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f1e89-124">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="f1e89-124">Example</span></span>  
 <span data-ttu-id="f1e89-125">The following sample shows how to use the <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> class.</span><span class="sxs-lookup"><span data-stu-id="f1e89-125">The following sample shows how to use the <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> class.</span></span>  
  
```csharp  
//  Query using ConditionExpression and FilterExpression  
ConditionExpression condition1 = new ConditionExpression();  
condition1.AttributeName = "lastname";  
condition1.Operator = ConditionOperator.Equal;  
condition1.Values.Add("Brown");              
  
FilterExpression filter1 = new FilterExpression();  
filter1.Conditions.Add(condition1);  
  
QueryExpression query = new QueryExpression("contact");  
query.ColumnSet.AddColumns("firstname", "lastname");  
query.Criteria.AddFilter(filter1);  
  
EntityCollection result1 = _serviceProxy.RetrieveMultiple(query);  
Console.WriteLine();Console.WriteLine("Query using Query Expression with ConditionExpression and FilterExpression");  
Console.WriteLine("---------------------------------------");  
foreach (var a in result1.Entities)  
{  
    Console.WriteLine("Name: " + a.Attributes["firstname"] + " " + a.Attributes["lastname"]);  
}  
Console.WriteLine("---------------------------------------");  
```  
  
### <a name="see-also"></a><span data-ttu-id="f1e89-126">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="f1e89-126">See also</span></span>  
 <span data-ttu-id="f1e89-127">[Building Queries with QueryExpression](build-queries-with-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="f1e89-127">[Building Queries with QueryExpression](build-queries-with-queryexpression.md) </span></span>  
 <span data-ttu-id="f1e89-128">[Use the ColumnSet Class](use-the-columnset-class.md) </span><span class="sxs-lookup"><span data-stu-id="f1e89-128">[Use the ColumnSet Class](use-the-columnset-class.md) </span></span>  
 <span data-ttu-id="f1e89-129">[Using the ConditionExpression Class](use-conditionexpression-class.md) </span><span class="sxs-lookup"><span data-stu-id="f1e89-129">[Using the ConditionExpression Class](use-conditionexpression-class.md) </span></span>  
 <span data-ttu-id="f1e89-130">[Using the FilterExpression Class](use-filterexpression-class.md) </span><span class="sxs-lookup"><span data-stu-id="f1e89-130">[Using the FilterExpression Class](use-filterexpression-class.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Query.QueryExpression>
