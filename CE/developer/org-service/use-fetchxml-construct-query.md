---
title: Use FetchXML to construct a query (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: 'This article discusses how to create and execute a FetchXML query '
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
- using FetchXML to construct queries, building the XML query strings
- FetchXML queries, how privileges of logged-on users affect the returned records
- using FetchXML to construct queries, code examples
- creating queries with FetchXML, using FetchXML to construct queries
- using FetchXML to construct queries, executing by using the IOrganizationService.RetrieveMultiple method
- using FetchXML to construct queries, conforming with schema definitions of the FetchXML language
- using FetchXML to construct queries, privileges of logged-on users affect the returned records
- FetchXML queries, using FetchXML to construct queries
- building queries with FetchXML, using FetchXML to construct queries
ms.assetid: 273dd192-cc12-4ab0-84ec-1ea1b8f367c3
caps.latest.revision: 37
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4caf10bef552743bf9cdbb8d357882fd600f7018
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386452"
---
# <a name="use-fetchxml-to-construct-a-query"></a><span data-ttu-id="9e9a0-103">Use FetchXML to construct a query</span><span class="sxs-lookup"><span data-stu-id="9e9a0-103">Use FetchXML to construct a query</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9e9a0-104">To execute a FetchXML query in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you must first build the XML query string.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-104">To execute a FetchXML query in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you must first build the XML query string.</span></span> <span data-ttu-id="9e9a0-105">After you create the query string, use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span><span class="sxs-lookup"><span data-stu-id="9e9a0-105">After you create the query string, use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span></span> <span data-ttu-id="9e9a0-106">method to execute the query string.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-106">method to execute the query string.</span></span> <span data-ttu-id="9e9a0-107">The privileges of the logged on user affects the set of records returned.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-107">The privileges of the logged on user affects the set of records returned.</span></span> <span data-ttu-id="9e9a0-108">Only records for which the logged on user has read access will be returned.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-108">Only records for which the logged on user has read access will be returned.</span></span>  
  
 <span data-ttu-id="9e9a0-109">The FetchXML query string must conform to the schema definition for the FetchXML language.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-109">The FetchXML query string must conform to the schema definition for the FetchXML language.</span></span> <span data-ttu-id="9e9a0-110">For more information, see [Fetch XML Schema](fetchxml-schema.md).</span><span class="sxs-lookup"><span data-stu-id="9e9a0-110">For more information, see [Fetch XML Schema](fetchxml-schema.md).</span></span>  
  
 <span data-ttu-id="9e9a0-111">You can save a query by creating a `SavedQuery` record, as demonstrated in [Sample: Validate and Execute a Saved Query](sample-validate-execute-saved-query.md).</span><span class="sxs-lookup"><span data-stu-id="9e9a0-111">You can save a query by creating a `SavedQuery` record, as demonstrated in [Sample: Validate and Execute a Saved Query](sample-validate-execute-saved-query.md).</span></span> <span data-ttu-id="9e9a0-112">Set `visible` on the `link-entity` node to `false` to hide the linked entity in the **Advanced Find** user interface.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-112">Set `visible` on the `link-entity` node to `false` to hide the linked entity in the **Advanced Find** user interface.</span></span> <span data-ttu-id="9e9a0-113">It will still participate in the execution of the query and will return the appropriate results.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-113">It will still participate in the execution of the query and will return the appropriate results.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="9e9a0-114">Don’t retrieve all attributes in a query because of the negative effect on performance.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-114">Don’t retrieve all attributes in a query because of the negative effect on performance.</span></span> <span data-ttu-id="9e9a0-115">This is particularly true if the query is used as a parameter to an update request.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-115">This is particularly true if the query is used as a parameter to an update request.</span></span> <span data-ttu-id="9e9a0-116">In an update, if all attributes are included this sets all field values, even if they are unchanged, and often triggers cascaded updates to child records.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-116">In an update, if all attributes are included this sets all field values, even if they are unchanged, and often triggers cascaded updates to child records.</span></span>  
  
## <a name="create-the-query-string"></a><span data-ttu-id="9e9a0-117">Create the Query String</span><span class="sxs-lookup"><span data-stu-id="9e9a0-117">Create the Query String</span></span>  
 <span data-ttu-id="9e9a0-118">In the following example, the **FetchXML** statement retrieves all accounts:</span><span class="sxs-lookup"><span data-stu-id="9e9a0-118">In the following example, the **FetchXML** statement retrieves all accounts:</span></span>  
  
```xml  
  
<fetch mapping='logical'>   
   <entity name='account'>  
      <attribute name='accountid'/>   
      <attribute name='name'/>   
</entity>  
</fetch>  
  
```  
  
 <span data-ttu-id="9e9a0-119">In the following example, the **FetchXML** statement retrieves all accounts where the last name of the owning user is not equal to Cannon:</span><span class="sxs-lookup"><span data-stu-id="9e9a0-119">In the following example, the **FetchXML** statement retrieves all accounts where the last name of the owning user is not equal to Cannon:</span></span>  
  
```xml  
  
<fetch mapping='logical'>  
   <entity name='account'>   
      <attribute name='accountid'/>   
      <attribute name='name'/>   
      <link-entity name='systemuser' to='owninguser'>   
         <filter type='and'>   
            <condition attribute='lastname' operator='ne' value='Cannon' />   
          </filter>   
      </link-entity>   
   </entity>   
</fetch>  
  
```  
  
 <span data-ttu-id="9e9a0-120">In the following example, the **FetchXML** statement uses count to set the maximum number of records returned from the query.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-120">In the following example, the **FetchXML** statement uses count to set the maximum number of records returned from the query.</span></span> <span data-ttu-id="9e9a0-121">In this case first 3 accounts are returned from the query,</span><span class="sxs-lookup"><span data-stu-id="9e9a0-121">In this case first 3 accounts are returned from the query,</span></span>  
  
```  
<fetch mapping='logical' count='3'>  
  <entity name='account'>  
   <attribute name='name' alias='name'/>  
  </entity></fetch>  
```  
  
 <span data-ttu-id="9e9a0-122">This example shows an inner join between EntityMap and AttributeMap where the EntityMapID matches.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-122">This example shows an inner join between EntityMap and AttributeMap where the EntityMapID matches.</span></span>  
  
```  
<fetch version='1.0' mapping='logical' distinct='false'>  
   <entity name='entitymap'>  
      <attribute name='sourceentityname'/>  
      <attribute name='targetentityname'/>  
      <link-entity name='attributemap' alias='attributemap' to='entitymapid' from='entitymapid' link-type='inner'>  
         <attribute name='sourceattributename'/>  
         <attribute name='targetattributename'/>  
      </link-entity>  
   </entity>  
 </fetch>  
```  
  
## <a name="execute-the-query"></a><span data-ttu-id="9e9a0-123">Execute the Query</span><span class="sxs-lookup"><span data-stu-id="9e9a0-123">Execute the Query</span></span>  
 <span data-ttu-id="9e9a0-124">The following code shows how to execute a **FetchXML** query:</span><span class="sxs-lookup"><span data-stu-id="9e9a0-124">The following code shows how to execute a **FetchXML** query:</span></span>  
  
```csharp  
  
// Retrieve all accounts owned by the user with read access rights to the accounts and   
// where the last name of the user is not Cannon.   
string fetch2 = @"  
   <fetch mapping='logical'>  
     <entity name='account'>   
        <attribute name='accountid'/>   
        <attribute name='name'/>   
        <link-entity name='systemuser' to='owninguser'>   
           <filter type='and'>   
              <condition attribute='lastname' operator='ne' value='Cannon' />   
           </filter>   
        </link-entity>   
     </entity>   
   </fetch> ";   
  
EntityCollection result = _serviceProxy.RetrieveMultiple(new FetchExpression(fetch2));
foreach (var c in result.Entities)
{
   System.Console.WriteLine(c.Attributes["name"]);
}  
```  
  
## <a name="query-results"></a><span data-ttu-id="9e9a0-125">Query Results</span><span class="sxs-lookup"><span data-stu-id="9e9a0-125">Query Results</span></span>  
 <span data-ttu-id="9e9a0-126">When you execute a FetchXML query by using the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy>.<xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.RetrieveMultiple(Microsoft.Xrm.Sdk.Query.QueryBase)></span><span class="sxs-lookup"><span data-stu-id="9e9a0-126">When you execute a FetchXML query by using the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy>.<xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.RetrieveMultiple(Microsoft.Xrm.Sdk.Query.QueryBase)></span></span> <span data-ttu-id="9e9a0-127">method authenticates the user.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-127">method authenticates the user.</span></span> <span data-ttu-id="9e9a0-128">method, the return value is an <xref:Microsoft.Xrm.Sdk.EntityCollection> that contains the results of the query.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-128">method, the return value is an <xref:Microsoft.Xrm.Sdk.EntityCollection> that contains the results of the query.</span></span> <span data-ttu-id="9e9a0-129">You can then iterate through the entity collection.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-129">You can then iterate through the entity collection.</span></span> <span data-ttu-id="9e9a0-130">The previous example uses the `foreach` loop to iterate through the result collection of the FetchXML query.</span><span class="sxs-lookup"><span data-stu-id="9e9a0-130">The previous example uses the `foreach` loop to iterate through the result collection of the FetchXML query.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="9e9a0-131">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9e9a0-131">See also</span></span>  
 <span data-ttu-id="9e9a0-132">[Build Queries with FetchXML](build-queries-fetchxml.md) </span><span class="sxs-lookup"><span data-stu-id="9e9a0-132">[Build Queries with FetchXML](build-queries-fetchxml.md) </span></span>  
 <span data-ttu-id="9e9a0-133">[Use FetchXML Aggregation](use-fetchxml-aggregation.md) </span><span class="sxs-lookup"><span data-stu-id="9e9a0-133">[Use FetchXML Aggregation](use-fetchxml-aggregation.md) </span></span>  
 [<span data-ttu-id="9e9a0-134">Fetch XML Schema</span><span class="sxs-lookup"><span data-stu-id="9e9a0-134">Fetch XML Schema</span></span>](fetchxml-schema.md)
