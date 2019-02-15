---
title: Retrieve and execute predefined queries (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Dynamics 365 for Customer Engagement provides a way for administrators to create system views that are available to all users. Read how you can compose a predefined query and use FetchXML to create a query string to retrieve data
ms.custom: ''
ms.date: 06/14/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 3d771a18-3dc5-4372-a7c7-40b3b1f986d8
caps.latest.revision: 16
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9470ca42a2d81e9256dcc15e81d41db75afe6210
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388268"
---
# <a name="retrieve-and-execute-predefined-queries"></a><span data-ttu-id="a08e7-104">Retrieve and execute predefined queries</span><span class="sxs-lookup"><span data-stu-id="a08e7-104">Retrieve and execute predefined queries</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] <span data-ttu-id="a08e7-105">apps provides a way for administrators to create system views that are available to all users.</span><span class="sxs-lookup"><span data-stu-id="a08e7-105">apps provides a way for administrators to create system views that are available to all users.</span></span> <span data-ttu-id="a08e7-106">Individual users can save the advanced find queries for re-use in the application.</span><span class="sxs-lookup"><span data-stu-id="a08e7-106">Individual users can save the advanced find queries for re-use in the application.</span></span> <span data-ttu-id="a08e7-107">Both of these represent predefined queries you can retrieve and execute using the Web API.</span><span class="sxs-lookup"><span data-stu-id="a08e7-107">Both of these represent predefined queries you can retrieve and execute using the Web API.</span></span> <span data-ttu-id="a08e7-108">You can also compose a query using FetchXml and use that to retrieve data.</span><span class="sxs-lookup"><span data-stu-id="a08e7-108">You can also compose a query using FetchXml and use that to retrieve data.</span></span>

<a name="bkmk_predefinedQueries"></a>

## <a name="predefined-queries"></a><span data-ttu-id="a08e7-109">Predefined queries</span><span class="sxs-lookup"><span data-stu-id="a08e7-109">Predefined queries</span></span>

[!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] <span data-ttu-id="a08e7-110">apps allows you to define, save, and execute two types of queries as listed here.</span><span class="sxs-lookup"><span data-stu-id="a08e7-110">apps allows you to define, save, and execute two types of queries as listed here.</span></span>


|   <span data-ttu-id="a08e7-111">Query type</span><span class="sxs-lookup"><span data-stu-id="a08e7-111">Query type</span></span>    |                                                                                                                                                 <span data-ttu-id="a08e7-112">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a08e7-112">Description</span></span>                                                                                                                                                  |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a08e7-113">**Saved Query**</span><span class="sxs-lookup"><span data-stu-id="a08e7-113">**Saved Query**</span></span> |       <span data-ttu-id="a08e7-114">System-defined views for an entity.</span><span class="sxs-lookup"><span data-stu-id="a08e7-114">System-defined views for an entity.</span></span> <span data-ttu-id="a08e7-115">These views are stored in the <xref href="Microsoft.Dynamics.CRM.savedquery?text=savedquery EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="a08e7-115">These views are stored in the <xref href="Microsoft.Dynamics.CRM.savedquery?text=savedquery EntityType" />.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="a08e7-116">[Customize Entity Views](../customize-dev/customize-entity-views.md)</span><span class="sxs-lookup"><span data-stu-id="a08e7-116">[Customize Entity Views](../customize-dev/customize-entity-views.md)</span></span>        |
| <span data-ttu-id="a08e7-117">**User Query**</span><span class="sxs-lookup"><span data-stu-id="a08e7-117">**User Query**</span></span>  | <span data-ttu-id="a08e7-118">Advanced Find searches saved by users for an entity.</span><span class="sxs-lookup"><span data-stu-id="a08e7-118">Advanced Find searches saved by users for an entity.</span></span> <span data-ttu-id="a08e7-119">These views are stored in the <xref href="Microsoft.Dynamics.CRM.userquery?text=userquery EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="a08e7-119">These views are stored in the <xref href="Microsoft.Dynamics.CRM.userquery?text=userquery EntityType" />.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="a08e7-120">[UserQuery (Saved View) Entity](../userquery-saved-view-entity.md)</span><span class="sxs-lookup"><span data-stu-id="a08e7-120">[UserQuery (Saved View) Entity](../userquery-saved-view-entity.md)</span></span> |

<span data-ttu-id="a08e7-121">Records for both of these types of entities contain the FetchXML definition for the data to return.</span><span class="sxs-lookup"><span data-stu-id="a08e7-121">Records for both of these types of entities contain the FetchXML definition for the data to return.</span></span> <span data-ttu-id="a08e7-122">You can query the respective entity type to retrieve the primary key value.</span><span class="sxs-lookup"><span data-stu-id="a08e7-122">You can query the respective entity type to retrieve the primary key value.</span></span> <span data-ttu-id="a08e7-123">With the primary key value, you can execute the query by passing the primary key value.</span><span class="sxs-lookup"><span data-stu-id="a08e7-123">With the primary key value, you can execute the query by passing the primary key value.</span></span> <span data-ttu-id="a08e7-124">For example, to execute the **Active Accounts** saved query, you must first get the primary key using a query like this.</span><span class="sxs-lookup"><span data-stu-id="a08e7-124">For example, to execute the **Active Accounts** saved query, you must first get the primary key using a query like this.</span></span>

```http
GET [Organization URI]/api/data/v9.0/savedqueries?$select=name,savedqueryid&$filter=name eq 'Active Accounts'
```

<span data-ttu-id="a08e7-125">You can then use the `savedqueryid` value and pass it as the value to the savedQuery parameter to the accounts entity set.</span><span class="sxs-lookup"><span data-stu-id="a08e7-125">You can then use the `savedqueryid` value and pass it as the value to the savedQuery parameter to the accounts entity set.</span></span>

```http
GET [Organization URI]/api/data/v9.0/accounts?savedQuery=00000000-0000-0000-00aa-000010001002
```

<span data-ttu-id="a08e7-126">Use the same approach to get the userqueryid and pass it as the value to the `userQuery` parameter to the entity set that matches the corresponding `returnedtypecode` of the saved query.</span><span class="sxs-lookup"><span data-stu-id="a08e7-126">Use the same approach to get the userqueryid and pass it as the value to the `userQuery` parameter to the entity set that matches the corresponding `returnedtypecode` of the saved query.</span></span>

```http
GET [Organization URI]/api/data/v9.0/accounts?userQuery=121c6fd8-1975-e511-80d4-00155d2a68d1
```

### <a name="apply-a-query-to-any-collection-of-the-appropriate-type"></a><span data-ttu-id="a08e7-127">Apply a query to any collection of the appropriate type</span><span class="sxs-lookup"><span data-stu-id="a08e7-127">Apply a query to any collection of the appropriate type</span></span>

<span data-ttu-id="a08e7-128">In addition to simply applying the saved query to the main entity set collection, you can also use a saved query or user query to apply the same filtering on any collection of the appropriate type of entities.</span><span class="sxs-lookup"><span data-stu-id="a08e7-128">In addition to simply applying the saved query to the main entity set collection, you can also use a saved query or user query to apply the same filtering on any collection of the appropriate type of entities.</span></span> <span data-ttu-id="a08e7-129">For example, if you want to apply a query against just the entities related to a specific entity, you can apply the same pattern.</span><span class="sxs-lookup"><span data-stu-id="a08e7-129">For example, if you want to apply a query against just the entities related to a specific entity, you can apply the same pattern.</span></span> <span data-ttu-id="a08e7-130">For example, the following URL will apply the **Open Opportunities** query against the opportunities related to a specific account via the `opportunity_parent_account` collection-valued navigation property.</span><span class="sxs-lookup"><span data-stu-id="a08e7-130">For example, the following URL will apply the **Open Opportunities** query against the opportunities related to a specific account via the `opportunity_parent_account` collection-valued navigation property.</span></span>

```http
GET [Organization URI]/api/data/v9.0/accounts(8f390c24-9c72-e511-80d4-00155d2a68d1)/opportunity_parent_account/?savedQuery=00000000-0000-0000-00aa-000010003001
```

<a name="bkmk_useFetchXML"></a>

## <a name="use-custom-fetchxml"></a><span data-ttu-id="a08e7-131">Use custom FetchXML</span><span class="sxs-lookup"><span data-stu-id="a08e7-131">Use custom FetchXML</span></span>

<span data-ttu-id="a08e7-132">FetchXML is a proprietary query language that provides capabilities to perform aggregation.</span><span class="sxs-lookup"><span data-stu-id="a08e7-132">FetchXML is a proprietary query language that provides capabilities to perform aggregation.</span></span> <span data-ttu-id="a08e7-133">The saved queries and user queries stored in <xref href="Microsoft.Dynamics.CRM.savedquery?text=savedquery EntityType" /> and <xref href="Microsoft.Dynamics.CRM.userquery?text=userquery EntityType" /> respectively both include a fetchxml property that defines the query.</span><span class="sxs-lookup"><span data-stu-id="a08e7-133">The saved queries and user queries stored in <xref href="Microsoft.Dynamics.CRM.savedquery?text=savedquery EntityType" /> and <xref href="Microsoft.Dynamics.CRM.userquery?text=userquery EntityType" /> respectively both include a fetchxml property that defines the query.</span></span> <span data-ttu-id="a08e7-134">You can use FetchXML directly with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span><span class="sxs-lookup"><span data-stu-id="a08e7-134">You can use FetchXML directly with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span></span> <span data-ttu-id="a08e7-135">method or with the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest>.</span><span class="sxs-lookup"><span data-stu-id="a08e7-135">method or with the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest>.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="a08e7-136">[Build Queries with FetchXML](../org-service/build-queries-fetchxml.md)</span><span class="sxs-lookup"><span data-stu-id="a08e7-136">[Build Queries with FetchXML](../org-service/build-queries-fetchxml.md)</span></span>

<span data-ttu-id="a08e7-137">You can pass URL encoded FetchXML as a query to the entity set corresponding to the root entity of the query using the `fetchXml` query string parameter to return the results from the Web API.</span><span class="sxs-lookup"><span data-stu-id="a08e7-137">You can pass URL encoded FetchXML as a query to the entity set corresponding to the root entity of the query using the `fetchXml` query string parameter to return the results from the Web API.</span></span> <span data-ttu-id="a08e7-138">For example, you can have the following FetchXML that has account as the entity.</span><span class="sxs-lookup"><span data-stu-id="a08e7-138">For example, you can have the following FetchXML that has account as the entity.</span></span>  

```xml  
<fetch mapping='logical'>
   <entity name='account'>
      <attribute name='accountid'/>
      <attribute name='name'/>
</entity>
</fetch>
```

<span data-ttu-id="a08e7-139">The URL encoded value of this FetchXML is as shown here.</span><span class="sxs-lookup"><span data-stu-id="a08e7-139">The URL encoded value of this FetchXML is as shown here.</span></span>

```text
%3Cfetch%20mapping='logical'%3E%3Centity%20name='account'%3E%3Cattribute%20name='accountid'/%3E%3Cattribute%20name='name'/%3E%3C/entity%3E%3C/fetch%3E
```

<span data-ttu-id="a08e7-140">Most programming languages include a function to URL encode a string.</span><span class="sxs-lookup"><span data-stu-id="a08e7-140">Most programming languages include a function to URL encode a string.</span></span> <span data-ttu-id="a08e7-141">For example, in [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] you use the [encodeURI](http://www.ecma-international.org/ecma-262/5.1/) function.</span><span class="sxs-lookup"><span data-stu-id="a08e7-141">For example, in [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)] you use the [encodeURI](http://www.ecma-international.org/ecma-262/5.1/) function.</span></span> <span data-ttu-id="a08e7-142">You should URL encode any request that you send to any RESTful web service.</span><span class="sxs-lookup"><span data-stu-id="a08e7-142">You should URL encode any request that you send to any RESTful web service.</span></span> <span data-ttu-id="a08e7-143">If you paste a URL into the address bar of your browser it should URL encode the address automatically.</span><span class="sxs-lookup"><span data-stu-id="a08e7-143">If you paste a URL into the address bar of your browser it should URL encode the address automatically.</span></span> <span data-ttu-id="a08e7-144">The following example shows a GET request using the FetchXML shown previously using the entity set path for accounts.</span><span class="sxs-lookup"><span data-stu-id="a08e7-144">The following example shows a GET request using the FetchXML shown previously using the entity set path for accounts.</span></span>

<span data-ttu-id="a08e7-145">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="a08e7-145">**Request**</span></span>

```http
GET [Organization URI]/api/data/v9.0/accounts?fetchXml=%3Cfetch%20mapping='logical'%3E%3Centity%20name='account'%3E%3Cattribute%20name='accountid'/%3E%3Cattribute%20name='name'/%3E%3C/entity%3E%3C/fetch%3E HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="a08e7-146">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="a08e7-146">**Response**</span></span>

```http
HTTP/1.1 200 OK
Content-Type: application/json; odata.metadata=minimal
OData-Version: 4.0

{  
  "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts(accountid,name)","value":[  
    {  
      "@odata.etag":"W/\"506678\"","accountid":"89390c24-9c72-e511-80d4-00155d2a68d1","name":"Fourth Coffee (sample)"  
    },{  
      "@odata.etag":"W/\"502172\"","accountid":"8b390c24-9c72-e511-80d4-00155d2a68d1","name":"Litware, Inc. (sample)"  
    },{  
      "@odata.etag":"W/\"502174\"","accountid":"8d390c24-9c72-e511-80d4-00155d2a68d1","name":"Adventure Works (sample)"  
    },{  
      "@odata.etag":"W/\"506705\"","accountid":"8f390c24-9c72-e511-80d4-00155d2a68d1","name":"Fabrikam, Inc. (sample)"  
    },{  
      "@odata.etag":"W/\"506701\"","accountid":"91390c24-9c72-e511-80d4-00155d2a68d1","name":"Blue Yonder Airlines (sample)"  
    },{  
      "@odata.etag":"W/\"502180\"","accountid":"93390c24-9c72-e511-80d4-00155d2a68d1","name":"City Power & Light (sample)"  
    },{  
      "@odata.etag":"W/\"502182\"","accountid":"95390c24-9c72-e511-80d4-00155d2a68d1","name":"Contoso Pharmaceuticals (sample)"  
    },{  
      "@odata.etag":"W/\"506704\"","accountid":"97390c24-9c72-e511-80d4-00155d2a68d1","name":"Alpine Ski House (sample)"  
    },{  
      "@odata.etag":"W/\"502186\"","accountid":"99390c24-9c72-e511-80d4-00155d2a68d1","name":"A. Datum Corporation (sample)"  
    },{  
      "@odata.etag":"W/\"502188\"","accountid":"9b390c24-9c72-e511-80d4-00155d2a68d1","name":"Coho Winery (sample)"  
    },{  
      "@odata.etag":"W/\"504177\"","accountid":"0a3238d4-f973-e511-80d4-00155d2a68d1","name":"Litware, Inc."  
    }  
  ]  
}  
```

<a name="bkmk_WebAPIFetchPaging"></a>

### <a name="paging-with-fetchxml"></a><span data-ttu-id="a08e7-147">Paging with FetchXML</span><span class="sxs-lookup"><span data-stu-id="a08e7-147">Paging with FetchXML</span></span>

<span data-ttu-id="a08e7-148">With FetchXML you can apply paging by setting the `page` and `count` attributes of the `fetch` element.</span><span class="sxs-lookup"><span data-stu-id="a08e7-148">With FetchXML you can apply paging by setting the `page` and `count` attributes of the `fetch` element.</span></span> <span data-ttu-id="a08e7-149">For example, to set a query for accounts and limit the number of entities to 2 and to return just the first page, the following fetchXML:</span><span class="sxs-lookup"><span data-stu-id="a08e7-149">For example, to set a query for accounts and limit the number of entities to 2 and to return just the first page, the following fetchXML:</span></span>

```xml
<fetch mapping="logical" page="1" count="2">  
 <entity name="account">  
  <attribute name="accountid" />  
  <attribute name="name" />  
  <attribute name="industrycode" />  
 <order attribute="name" />  
 </entity>  
</fetch>
```

<span data-ttu-id="a08e7-150">With a request using FetchXML you can also request a paging cookie and include it with your query.</span><span class="sxs-lookup"><span data-stu-id="a08e7-150">With a request using FetchXML you can also request a paging cookie and include it with your query.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="a08e7-151">[Page large result sets with FetchXML](../org-service/page-large-result-sets-with-fetchxml.md)</span><span class="sxs-lookup"><span data-stu-id="a08e7-151">[Page large result sets with FetchXML](../org-service/page-large-result-sets-with-fetchxml.md)</span></span>  

<span data-ttu-id="a08e7-152">A paging cookie must be requested as an annotation.</span><span class="sxs-lookup"><span data-stu-id="a08e7-152">A paging cookie must be requested as an annotation.</span></span> <span data-ttu-id="a08e7-153">Set the `odata.include-annotations` preference to use (or include) `Microsoft.Dynamics.CRM.fetchxmlpagingcookie` and a `@Microsoft.Dynamics.CRM.fetchxmlpagingcookie` property will be returned with the result.</span><span class="sxs-lookup"><span data-stu-id="a08e7-153">Set the `odata.include-annotations` preference to use (or include) `Microsoft.Dynamics.CRM.fetchxmlpagingcookie` and a `@Microsoft.Dynamics.CRM.fetchxmlpagingcookie` property will be returned with the result.</span></span>

<a name="bkmk_FetchXMLwithinBatch"></a>

### <a name="use-fetchxml-within-a-batch-request"></a><span data-ttu-id="a08e7-154">Use FetchXML within a Batch request</span><span class="sxs-lookup"><span data-stu-id="a08e7-154">Use FetchXML within a Batch request</span></span>

<span data-ttu-id="a08e7-155">The length of a URL in a `GET` request is limited.</span><span class="sxs-lookup"><span data-stu-id="a08e7-155">The length of a URL in a `GET` request is limited.</span></span> <span data-ttu-id="a08e7-156">Including FetchXML as a parameter in the URL can reach this limit.</span><span class="sxs-lookup"><span data-stu-id="a08e7-156">Including FetchXML as a parameter in the URL can reach this limit.</span></span>  <span data-ttu-id="a08e7-157">You can execute a `$batch` operation using a `POST` request as a way to move the FetchXML out of the URL and into the body of the request where this limit will not apply.</span><span class="sxs-lookup"><span data-stu-id="a08e7-157">You can execute a `$batch` operation using a `POST` request as a way to move the FetchXML out of the URL and into the body of the request where this limit will not apply.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="a08e7-158">[Execute batch operations using the Web API](execute-batch-operations-using-web-api.md).</span><span class="sxs-lookup"><span data-stu-id="a08e7-158">[Execute batch operations using the Web API](execute-batch-operations-using-web-api.md).</span></span>

#### <a name="example"></a><span data-ttu-id="a08e7-159">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="a08e7-159">Example</span></span>

<span data-ttu-id="a08e7-160">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="a08e7-160">**Request**</span></span>

```http
POST [Organization URI]/api/data/v9.0/$batch HTTP/1.1

Content-Type:multipart/mixed;boundary=batch_AAA123
Accept:application/json
OData-MaxVersion:4.0
OData-Version:4.0

--batch_AAA123
Content-Type: application/http
Content-Transfer-Encoding: binary

GET [Organization URI]/api/data/v9.0/accounts?fetchXml=%3Cfetch%20mapping='logical'%3E%3Centity%20name='account'%3E%3Cattribute%20name='accountid'/%3E%3Cattribute%20name='name'/%3E%3Cattribute%20name='telephone1'/%3E%3Cattribute%20name='accountid'/%3E%3Cattribute%20name='creditonhold'/%3E%3C/entity%3E%3C/fetch%3E HTTP/1.1
Content-Type: application/json
OData-Version: 4.0
OData-MaxVersion: 4.0

--batch_AAA123--
```

<span data-ttu-id="a08e7-161">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="a08e7-161">**Response**</span></span>

```json
--batchresponse_cbfd44cd-a322-484e-913b-49e18af44e34
Content-Type: application/http
Content-Transfer-Encoding: binary

HTTP/1.1 200 OK
Content-Type: application/json; odata.metadata=minimal
OData-Version: 4.0

{  
   "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts(accountid,name,telephone1,creditonhold)",
   "value":[  
      {  
         "@odata.etag":"W/\"563737\"",
         "accountid":"1f55c679-485e-e811-8151-000d3aa3c22a",
         "name":"Fourth Coffee (sample)",
         "telephone1":"+1-425-555-0121",
         "creditonhold":false
      },
      {  
         "@odata.etag":"W/\"563739\"",
         "accountid":"2555c679-485e-e811-8151-000d3aa3c22a",
         "name":"Litware, Inc. (sample)",
         "telephone1":"+1-425-555-0120",
         "creditonhold":false
      }
   ]
}
--batchresponse_cbfd44cd-a322-484e-913b-49e18af44e34--
```



## <a name="see-also"></a><span data-ttu-id="a08e7-162">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a08e7-162">See also</span></span>

 [<span data-ttu-id="a08e7-163">Web API Query Data Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="a08e7-163">Web API Query Data Sample (C#)</span></span>](web-api-query-data-sample-csharp.md)<br />
 [<span data-ttu-id="a08e7-164">Web API Query Data Sample (Client-side JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a08e7-164">Web API Query Data Sample (Client-side JavaScript)</span></span>](web-api-query-data-sample-client-side-javascript.md)<br />
 [<span data-ttu-id="a08e7-165">Perform operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="a08e7-165">Perform operations using the Web API</span></span>](perform-operations-web-api.md)<br />
 [<span data-ttu-id="a08e7-166">Compose Http requests and handle errors</span><span class="sxs-lookup"><span data-stu-id="a08e7-166">Compose Http requests and handle errors</span></span>](compose-http-requests-handle-errors.md)<br />
 [<span data-ttu-id="a08e7-167">Query Data using the Web API</span><span class="sxs-lookup"><span data-stu-id="a08e7-167">Query Data using the Web API</span></span>](query-data-web-api.md)<br />
 [<span data-ttu-id="a08e7-168">Create an entity using the Web API</span><span class="sxs-lookup"><span data-stu-id="a08e7-168">Create an entity using the Web API</span></span>](create-entity-web-api.md)<br />
 [<span data-ttu-id="a08e7-169">Retrieve an entity using the Web API</span><span class="sxs-lookup"><span data-stu-id="a08e7-169">Retrieve an entity using the Web API</span></span>](retrieve-entity-using-web-api.md)<br />
 [<span data-ttu-id="a08e7-170">Update and delete entities using the Web API</span><span class="sxs-lookup"><span data-stu-id="a08e7-170">Update and delete entities using the Web API</span></span>](update-delete-entities-using-web-api.md)<br />
 [<span data-ttu-id="a08e7-171">Associate and disassociate entities using the Web API</span><span class="sxs-lookup"><span data-stu-id="a08e7-171">Associate and disassociate entities using the Web API</span></span>](associate-disassociate-entities-using-web-api.md)<br />
 [<span data-ttu-id="a08e7-172">Use Web API functions</span><span class="sxs-lookup"><span data-stu-id="a08e7-172">Use Web API functions</span></span>](use-web-api-functions.md)<br />
 [<span data-ttu-id="a08e7-173">Use Web API actions</span><span class="sxs-lookup"><span data-stu-id="a08e7-173">Use Web API actions</span></span>](use-web-api-actions.md)<br />
 [<span data-ttu-id="a08e7-174">Execute batch operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="a08e7-174">Execute batch operations using the Web API</span></span>](execute-batch-operations-using-web-api.md)<br />
 [<span data-ttu-id="a08e7-175">Impersonate another user using the Web API</span><span class="sxs-lookup"><span data-stu-id="a08e7-175">Impersonate another user using the Web API</span></span>](impersonate-another-user-web-api.md)<br />
 [<span data-ttu-id="a08e7-176">Perform conditional operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="a08e7-176">Perform conditional operations using the Web API</span></span>](perform-conditional-operations-using-web-api.md)<br />
