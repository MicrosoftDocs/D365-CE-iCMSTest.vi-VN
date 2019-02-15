---
title: Use the QueryByAttribute class (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: In Dynamics 365 for Customer Engagement (online) Customer Engagement, you can use the QueryByAttribute class to build queries that test a set of attributes against a set of values
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
- QueryByAttribute class, about; properties for; and code example
- building queries by using QueryExpression, QueryByAttribute class
- testing a set of attributes against a set of values, QueryByAttribute class
- QueryByAttribute class, searching for entities where attributes match specified values
- using the QueryByAttribute class
ms.assetid: 3e0b0dcd-449c-4107-9f08-ddf71db29261
caps.latest.revision: 29
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4c4e6a0fe5bf9df781e26f46de7c08e293efb0c6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387484"
---
# <a name="use-the-querybyattribute-class"></a><span data-ttu-id="813c0-103">Use the QueryByAttribute class</span><span class="sxs-lookup"><span data-stu-id="813c0-103">Use the QueryByAttribute class</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="813c0-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the <xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute> class to build queries that test a set of attributes against a set of values.</span><span class="sxs-lookup"><span data-stu-id="813c0-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the <xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute> class to build queries that test a set of attributes against a set of values.</span></span> <span data-ttu-id="813c0-105">Use this class with the <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method or the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest></span><span class="sxs-lookup"><span data-stu-id="813c0-105">Use this class with the <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method or the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest></span></span> <span data-ttu-id="813c0-106">method.</span><span class="sxs-lookup"><span data-stu-id="813c0-106">method.</span></span>
  
 <span data-ttu-id="813c0-107">The following table lists the properties that you can set to create a query expression using the <xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute> class.</span><span class="sxs-lookup"><span data-stu-id="813c0-107">The following table lists the properties that you can set to create a query expression using the <xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute> class.</span></span>  
  
|<span data-ttu-id="813c0-108">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="813c0-108">Property</span></span>|<span data-ttu-id="813c0-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="813c0-109">Description</span></span>|  
|--------------|-----------------|  
|<xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute.EntityName>|<span data-ttu-id="813c0-110">Specifies which type of entity is retrieved.</span><span class="sxs-lookup"><span data-stu-id="813c0-110">Specifies which type of entity is retrieved.</span></span> <span data-ttu-id="813c0-111">A query expression can only retrieve a collection of one entity type.</span><span class="sxs-lookup"><span data-stu-id="813c0-111">A query expression can only retrieve a collection of one entity type.</span></span> <span data-ttu-id="813c0-112">You can also pass this value by using the <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> constructor.</span><span class="sxs-lookup"><span data-stu-id="813c0-112">You can also pass this value by using the <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> constructor.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute.ColumnSet>|<span data-ttu-id="813c0-113">Specifies the set of attributes (columns) to retrieve.</span><span class="sxs-lookup"><span data-stu-id="813c0-113">Specifies the set of attributes (columns) to retrieve.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute.Attributes>|<span data-ttu-id="813c0-114">Specifies the set of attributes selected in the query.</span><span class="sxs-lookup"><span data-stu-id="813c0-114">Specifies the set of attributes selected in the query.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute.Values>|<span data-ttu-id="813c0-115">Specifies the attribute values to look for when the query is executed.</span><span class="sxs-lookup"><span data-stu-id="813c0-115">Specifies the attribute values to look for when the query is executed.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute.Orders>|<span data-ttu-id="813c0-116">Specifies the order in which the records are returned from the query.</span><span class="sxs-lookup"><span data-stu-id="813c0-116">Specifies the order in which the records are returned from the query.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute.PageInfo>|<span data-ttu-id="813c0-117">Specifies the number of pages and the number of records per page returned from the query.</span><span class="sxs-lookup"><span data-stu-id="813c0-117">Specifies the number of pages and the number of records per page returned from the query.</span></span>|  
  
 <span data-ttu-id="813c0-118">The following code example shows how to use the `QueryByAttribute` class.</span><span class="sxs-lookup"><span data-stu-id="813c0-118">The following code example shows how to use the `QueryByAttribute` class.</span></span>  
  
```csharp  
//  Create query using querybyattribute      
QueryByAttribute querybyexpression = new QueryByAttribute("account");      
querybyexpression.ColumnSet = new ColumnSet("name", "address1_city", "emailaddress1");  
  
//  Attribute to query      
querybyexpression.Attributes.AddRange("address1_city");  
  
//  Value of queried attribute to return      
querybyexpression.Values.AddRange("Detroit");      
  
//  Query passed to the service proxy      
EntityCollection retrieved = _serviceProxy.RetrieveMultiple(querybyexpression);     
  
//  Iterate through returned collection      
foreach (var c in retrieved.Entities)      
{  
      System.Console.WriteLine("Name: " + c.Attributes["name"]);  
      System.Console.WriteLine("Address: " + c.Attributes["address1_city"]);        
      System.Console.WriteLine("E-mail: " + c.Attributes["emailaddress1"]);      
}  
  
```  
  
### <a name="see-also"></a><span data-ttu-id="813c0-119">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="813c0-119">See also</span></span>  
 <span data-ttu-id="813c0-120">[Building Queries with QueryExpression](build-queries-with-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="813c0-120">[Building Queries with QueryExpression](build-queries-with-queryexpression.md) </span></span>  
 <span data-ttu-id="813c0-121">[Using the QueryExpression Class](use-queryexpression-class.md) </span><span class="sxs-lookup"><span data-stu-id="813c0-121">[Using the QueryExpression Class](use-queryexpression-class.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute>
