---
title: Web API Conditional Operations Sample (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: This group of samples demonstrate how to perform operations that are conditionally based upon the version of the entity record contained on the Dynamics 365 for Customer Engagement server and/or currently maintained by the client
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: f2e5d22b-93fe-43b7-af15-3e281f3b3084
caps.latest.revision: 13
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 31106284d8eed74e10b5119ef7a30fa09a471c71
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387898"
---
# <a name="web-api-conditional-operations-sample"></a><span data-ttu-id="9ff3f-103">Web API Conditional Operations Sample</span><span class="sxs-lookup"><span data-stu-id="9ff3f-103">Web API Conditional Operations Sample</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9ff3f-104">This group of samples demonstrate how to perform operations that are conditionally based upon the version of the entity record contained on the Dynamics 365 for Customer Engagement server and/or currently maintained by the client.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-104">This group of samples demonstrate how to perform operations that are conditionally based upon the version of the entity record contained on the Dynamics 365 for Customer Engagement server and/or currently maintained by the client.</span></span> <span data-ttu-id="9ff3f-105">For more information, see [Perform conditional operations using the Web API](perform-conditional-operations-using-web-api.md).</span><span class="sxs-lookup"><span data-stu-id="9ff3f-105">For more information, see [Perform conditional operations using the Web API](perform-conditional-operations-using-web-api.md).</span></span> <span data-ttu-id="9ff3f-106">This sample is implemented as a separate project for the following languages:</span><span class="sxs-lookup"><span data-stu-id="9ff3f-106">This sample is implemented as a separate project for the following languages:</span></span>  

 [<span data-ttu-id="9ff3f-107">Web API Conditional Operations Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="9ff3f-107">Web API Conditional Operations Sample (C#)</span></span>](web-api-conditional-operations-sample-csharp.md)  

 <span data-ttu-id="9ff3f-108">The Dynamics 365 for Customer Engagement Web API follows the conventions of the [OData v4.0](http://www.odata.org/documentation/) protocol, which uses [ETags](http://docs.oasis-open.org/odata/odata/v4.0/errata03/os/complete/part1-protocol/odata-v4.0-errata03-os-part1-protocol-complete.html#_Toc453752236) to implement resource version control.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-108">The Dynamics 365 for Customer Engagement Web API follows the conventions of the [OData v4.0](http://www.odata.org/documentation/) protocol, which uses [ETags](http://docs.oasis-open.org/odata/odata/v4.0/errata03/os/complete/part1-protocol/odata-v4.0-errata03-os-part1-protocol-complete.html#_Toc453752236) to implement resource version control.</span></span> <span data-ttu-id="9ff3f-109">Web API conditional operations depend upon this versioning  mechanism.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-109">Web API conditional operations depend upon this versioning  mechanism.</span></span>  

 <span data-ttu-id="9ff3f-110">This topic explains the structure and content of the samples at a higher, language-neutral level.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-110">This topic explains the structure and content of the samples at a higher, language-neutral level.</span></span> <span data-ttu-id="9ff3f-111">It details the HTTP requests and responses, and the associated program output, where applicable.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-111">It details the HTTP requests and responses, and the associated program output, where applicable.</span></span> <span data-ttu-id="9ff3f-112">Review the linked sample topics above to obtain language-specific implementations and related details about how to perform the operations described in this topic.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-112">Review the linked sample topics above to obtain language-specific implementations and related details about how to perform the operations described in this topic.</span></span>  

## <a name="demonstrates"></a><span data-ttu-id="9ff3f-113">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="9ff3f-113">Demonstrates</span></span>

 <span data-ttu-id="9ff3f-114">This sample is divided into three principal sections, listed in the following table.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-114">This sample is divided into three principal sections, listed in the following table.</span></span>   <span data-ttu-id="9ff3f-115">Each section contains a set of related Web API operations which are discussed in greater detail in the associated conceptual section of the topic [Perform conditional operations using the Web API](perform-conditional-operations-using-web-api.md) .</span><span class="sxs-lookup"><span data-stu-id="9ff3f-115">Each section contains a set of related Web API operations which are discussed in greater detail in the associated conceptual section of the topic [Perform conditional operations using the Web API](perform-conditional-operations-using-web-api.md) .</span></span>  

|<span data-ttu-id="9ff3f-116">Code section</span><span class="sxs-lookup"><span data-stu-id="9ff3f-116">Code section</span></span>|<span data-ttu-id="9ff3f-117">Associated conceptual topics</span><span class="sxs-lookup"><span data-stu-id="9ff3f-117">Associated conceptual topics</span></span>|  
|------------------|----------------------------------|  
|[<span data-ttu-id="9ff3f-118">Conditional GET</span><span class="sxs-lookup"><span data-stu-id="9ff3f-118">Conditional GET</span></span>](#bkmk_conditionalGet)|[<span data-ttu-id="9ff3f-119">Conditional retrievals</span><span class="sxs-lookup"><span data-stu-id="9ff3f-119">Conditional retrievals</span></span>](perform-conditional-operations-using-web-api.md#bkmk_DetectIfChanged)|  
|[<span data-ttu-id="9ff3f-120">Optimistic concurrency on delete and update</span><span class="sxs-lookup"><span data-stu-id="9ff3f-120">Optimistic concurrency on delete and update</span></span>](#bkmk_optimisiticConcurrency)|[<span data-ttu-id="9ff3f-121">Apply optimistic concurrency</span><span class="sxs-lookup"><span data-stu-id="9ff3f-121">Apply optimistic concurrency</span></span>](perform-conditional-operations-using-web-api.md#bkmk_Applyoptimisticconcurrency)|  
|[<span data-ttu-id="9ff3f-122">Controlling upsert operations</span><span class="sxs-lookup"><span data-stu-id="9ff3f-122">Controlling upsert operations</span></span>](#bkmk_controllingUpsert)|[<span data-ttu-id="9ff3f-123">Limit upsert operations</span><span class="sxs-lookup"><span data-stu-id="9ff3f-123">Limit upsert operations</span></span>](perform-conditional-operations-using-web-api.md#bkmk_limitUpsertOperations)|  

 <span data-ttu-id="9ff3f-124">The following sections contain a brief discussion of the Dynamics 365 for Customer Engagement Web API operations performed, along with the corresponding HTTP messages and associated console output which is the same for each language implementation.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-124">The following sections contain a brief discussion of the Dynamics 365 for Customer Engagement Web API operations performed, along with the corresponding HTTP messages and associated console output which is the same for each language implementation.</span></span> <span data-ttu-id="9ff3f-125">For brevity, less pertinent HTTP headers have been omitted.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-125">For brevity, less pertinent HTTP headers have been omitted.</span></span> <span data-ttu-id="9ff3f-126">The URIs of the records will vary with the base organization address and the ID of the record assigned by your Dynamics 365 for Customer Engagement server.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-126">The URIs of the records will vary with the base organization address and the ID of the record assigned by your Dynamics 365 for Customer Engagement server.</span></span>  

<a name="bkmk_sampleData"></a>

## <a name="sample-data"></a><span data-ttu-id="9ff3f-127">Dữ liệu mẫu</span><span class="sxs-lookup"><span data-stu-id="9ff3f-127">Sample data</span></span>

 <span data-ttu-id="9ff3f-128">The sample creates the following record before the principal code sections are executed.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-128">The sample creates the following record before the principal code sections are executed.</span></span>  

|<span data-ttu-id="9ff3f-129">Loại thực thể</span><span class="sxs-lookup"><span data-stu-id="9ff3f-129">Entity type</span></span>|<span data-ttu-id="9ff3f-130">Client-assigned properties</span><span class="sxs-lookup"><span data-stu-id="9ff3f-130">Client-assigned properties</span></span>|<span data-ttu-id="9ff3f-131">Server-assigned properties</span><span class="sxs-lookup"><span data-stu-id="9ff3f-131">Server-assigned properties</span></span>|  
|-----------------|---------------------------------|---------------------------------|  
|<xref:Microsoft.Dynamics.CRM.account>|<span data-ttu-id="9ff3f-132">Name: `Contoso Ltd.`</span><span class="sxs-lookup"><span data-stu-id="9ff3f-132">Name: `Contoso Ltd.`</span></span> <br /><span data-ttu-id="9ff3f-133">Revenue: `5000000`</span><span class="sxs-lookup"><span data-stu-id="9ff3f-133">Revenue: `5000000`</span></span><br /><span data-ttu-id="9ff3f-134">Telephone: `555-0000`</span><span class="sxs-lookup"><span data-stu-id="9ff3f-134">Telephone: `555-0000`</span></span><br /><span data-ttu-id="9ff3f-135">Description: `Parent company of Contoso Pharmaceuticals, etc.`</span><span class="sxs-lookup"><span data-stu-id="9ff3f-135">Description: `Parent company of Contoso Pharmaceuticals, etc.`</span></span>|<span data-ttu-id="9ff3f-136">ID:  `14e151db-9b4f-e611-80e0-00155da84c08`</span><span class="sxs-lookup"><span data-stu-id="9ff3f-136">ID:  `14e151db-9b4f-e611-80e0-00155da84c08`</span></span><br /><span data-ttu-id="9ff3f-137">Initial Etag:  `W/"628448"`</span><span class="sxs-lookup"><span data-stu-id="9ff3f-137">Initial Etag:  `W/"628448"`</span></span>|  

<a name="bkmk_conditionalGet"></a>

## <a name="conditional-get"></a><span data-ttu-id="9ff3f-138">Conditional GET</span><span class="sxs-lookup"><span data-stu-id="9ff3f-138">Conditional GET</span></span>

 <span data-ttu-id="9ff3f-139">This section of the program demonstrates how to perform conditional retrievals in order to optimize network bandwidth and server processing while still maintaining the most current record state on the client.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-139">This section of the program demonstrates how to perform conditional retrievals in order to optimize network bandwidth and server processing while still maintaining the most current record state on the client.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="9ff3f-140">[Conditional retrievals](perform-conditional-operations-using-web-api.md#bkmk_DetectIfChanged)</span><span class="sxs-lookup"><span data-stu-id="9ff3f-140">[Conditional retrievals](perform-conditional-operations-using-web-api.md#bkmk_DetectIfChanged)</span></span>  

1. <span data-ttu-id="9ff3f-141">Attempt to retrieve the account `Contoso Ltd.` only if it does *not* match the current version, identified by the initial ETag value that was returned when the account record was created.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-141">Attempt to retrieve the account `Contoso Ltd.` only if it does *not* match the current version, identified by the initial ETag value that was returned when the account record was created.</span></span> <span data-ttu-id="9ff3f-142">This condition is represented by the `If-None-Match` header.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-142">This condition is represented by the `If-None-Match` header.</span></span>  

   <span data-ttu-id="9ff3f-143">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-143">**Request**</span></span>  

   ```http  
   GET http://[Organization URI]/api/data/v9.0/accounts(14e151db-9b4f-e611-80e0-00155da84c08)?$select=name,revenue,telephone1,description HTTP/1.1  
   If-None-Match: W/"628448"  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   Accept: application/json  

   ```  

   <span data-ttu-id="9ff3f-144">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-144">**Response**</span></span>  

   ```http  
   HTTP/1.1 304 Not Modified  
   ```  

   <span data-ttu-id="9ff3f-145">**Console output**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-145">**Console output**</span></span>  

   ```  
   Instance retrieved using ETag: W/"628448"  
   Expected outcome: Entity was not modified so nothing was returned.  
   ```  

    <span data-ttu-id="9ff3f-146">The response value, `304 Not Modified`, indicates that the current record is the most current, so the server does *not* return the requested record in the response body.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-146">The response value, `304 Not Modified`, indicates that the current record is the most current, so the server does *not* return the requested record in the response body.</span></span>  

2. <span data-ttu-id="9ff3f-147">Update the account by modifying its primary telephone number property.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-147">Update the account by modifying its primary telephone number property.</span></span>  

   <span data-ttu-id="9ff3f-148">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-148">**Request**</span></span>  

   ```http
   PUT http://[Organization URI]/api/data/v9.0/accounts(14e151db-9b4f-e611-80e0-00155da84c08)/telephone1 HTTP/1.1  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   Accept: application/json  
   Content-Type: application/json  
   {  
     "value": "555-0001"  
   }  
   ```  

   <span data-ttu-id="9ff3f-149">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-149">**Response**</span></span>  

   ```http
   HTTP/1.1 204 No Content  
   ```  

   <span data-ttu-id="9ff3f-150">**Console output**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-150">**Console output**</span></span>  

   ```  
   Account telephone number updated.  
   ```  

3. <span data-ttu-id="9ff3f-151">Re-attempt the same conditional GET operation, again using the original ETag value.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-151">Re-attempt the same conditional GET operation, again using the original ETag value.</span></span> <span data-ttu-id="9ff3f-152">This time the operation returns the requested data because the version on the server is different (and newer) than the version identified in the request.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-152">This time the operation returns the requested data because the version on the server is different (and newer) than the version identified in the request.</span></span> <span data-ttu-id="9ff3f-153">As in all record retrievals, the response includes an ETag header that identifies the current version.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-153">As in all record retrievals, the response includes an ETag header that identifies the current version.</span></span>  

   <span data-ttu-id="9ff3f-154">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-154">**Request**</span></span>  

   ```http
   GET http://[Organization URI]/api/data/v9.0/accounts(14e151db-9b4f-e611-80e0-00155da84c08)?$select=name,revenue,telephone1,description HTTP/1.1  
   If-None-Match: W/"628448"  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   Accept: application/json  
   ```  

   <span data-ttu-id="9ff3f-155">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-155">**Response**</span></span>  

   ```http
   HTTP/1.1 200 OK  
   Content-Type: application/json; odata.metadata=minimal  
   ETag: W/"628460"  
   {  
     "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#accounts(name,revenue,telephone1,description)/$entity",  
     "@odata.etag":"W/\"628460\"",  
     "name":"Contoso Ltd",  
     "revenue":5000000.0000,  
     "telephone1":"555-0001",  
     "description":"Parent company of Contoso Pharmaceuticals, etc.",  
     "accountid":"14e151db-9b4f-e611-80e0-00155da84c08",  
     "_transactioncurrencyid_value":"0d4ed62e-95f7-e511-80d1-00155da84c03"  
   }  
   ```  

   <span data-ttu-id="9ff3f-156">**Console output**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-156">**Console output**</span></span>  

   ```
   Instance retrieved using ETag: W/"628448"  
   {  
     "@odata.context": "http://[Organization URI]/api/data/v9.0/$metadata#accounts(name,revenue,telephone1,description)/$entity",  
     "@odata.etag": "W/\"628460\"",  
     "name": "Contoso Ltd",  
     "revenue": 5000000.0,  
     "telephone1": "555-0001",  
     "description": "Parent company of Contoso Pharmaceuticals, etc.",  
     "accountid": "14e151db-9b4f-e611-80e0-00155da84c08",  
     "_transactioncurrencyid_value": "0d4ed62e-95f7-e511-80d1-00155da84c03"  
   }  
   ```  

<a name="bkmk_optimisiticConcurrency"></a>

## <a name="optimistic-concurrency-on-delete-and-update"></a><span data-ttu-id="9ff3f-157">Optimistic concurrency on delete and update</span><span class="sxs-lookup"><span data-stu-id="9ff3f-157">Optimistic concurrency on delete and update</span></span>

 <span data-ttu-id="9ff3f-158">This section of the program demonstrates how to perform conditional delete and update operations.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-158">This section of the program demonstrates how to perform conditional delete and update operations.</span></span>  <span data-ttu-id="9ff3f-159">The most common use for such operations is in implementing an optimistic concurrency approach to record processing in a multi-user environment.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-159">The most common use for such operations is in implementing an optimistic concurrency approach to record processing in a multi-user environment.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="9ff3f-160">[Apply optimistic concurrency](perform-conditional-operations-using-web-api.md#bkmk_Applyoptimisticconcurrency)</span><span class="sxs-lookup"><span data-stu-id="9ff3f-160">[Apply optimistic concurrency](perform-conditional-operations-using-web-api.md#bkmk_Applyoptimisticconcurrency)</span></span>  

1. <span data-ttu-id="9ff3f-161">Attempt to delete original account if and only if it matches the original version (ETag value).</span><span class="sxs-lookup"><span data-stu-id="9ff3f-161">Attempt to delete original account if and only if it matches the original version (ETag value).</span></span>  <span data-ttu-id="9ff3f-162">This condition is represented by the `If-Match` header.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-162">This condition is represented by the `If-Match` header.</span></span>  <span data-ttu-id="9ff3f-163">This operation fails because the account record was updated in the previous section, so as a result, its version was updated on the server.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-163">This operation fails because the account record was updated in the previous section, so as a result, its version was updated on the server.</span></span>  

   <span data-ttu-id="9ff3f-164">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-164">**Request**</span></span>  

   ```http
   DELETE http://[Organization URI]/api/data/v9.0/accounts(14e151db-9b4f-e611-80e0-00155da84c08) HTTP/1.1  
   If-Match: W/"628448"  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   Accept: application/json  
   ```  

   <span data-ttu-id="9ff3f-165">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-165">**Response**</span></span>  

   ```http  
   HTTP/1.1 412 Precondition Failed  
   Content-Type: application/json; odata.metadata=minimal  
   OData-Version: 4.0  
   {  
     "error":{  
       "code":"","message":"The version of the existing record doesn't match the RowVersion property provided.", . . .  
       }  
   }  
   ```  

   <span data-ttu-id="9ff3f-166">**Console output**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-166">**Console output**</span></span>  

   ```  
   Expected Error: The version of the existing record doesn't match the property provided.  
           Account not deleted using ETag 'W/"628448"', status code: '412'.  
   ```  

2. <span data-ttu-id="9ff3f-167">Attempt to update the account if and only if it matches the original ETag value.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-167">Attempt to update the account if and only if it matches the original ETag value.</span></span>  <span data-ttu-id="9ff3f-168">Again, this condition is represented by the `If-Match` header and the operation fails for the same reason.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-168">Again, this condition is represented by the `If-Match` header and the operation fails for the same reason.</span></span>  

   <span data-ttu-id="9ff3f-169">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-169">**Request**</span></span>  

   ```http  
   PATCH http://[Organization URI]/api/data/v9.0/accounts(14e151db-9b4f-e611-80e0-00155da84c08) HTTP/1.1  
   If-Match: W/"628448"  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   Accept: application/json  
   Content-Type: application/json; charset=utf-8  
   {  
     "telephone1": "555-0002",  
     "revenue": 6000000  
   }    
   ```  

   <span data-ttu-id="9ff3f-170">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-170">**Response**</span></span>  

   ```http  
   HTTP/1.1 412 Precondition Failed  
   Content-Type: application/json; odata.metadata=minimal  
   OData-Version: 4.0  
   {  
     "error":{  
       "code":"","message":"The version of the existing record doesn't match the RowVersion property provided.", . . .   
     }  
   }    
   ```  

   <span data-ttu-id="9ff3f-171">**Console output**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-171">**Console output**</span></span>  

   ```  
   Expected Error: The version of the existing record doesn't match the property provided.  
           Account not updated using ETag 'W/"628448"', status code: '412'.  
   ```  

3. <span data-ttu-id="9ff3f-172">Re-attempt an update, but instead use the current ETag value obtained from the last record retrieval in the previous section.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-172">Re-attempt an update, but instead use the current ETag value obtained from the last record retrieval in the previous section.</span></span>  

   <span data-ttu-id="9ff3f-173">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-173">**Request**</span></span>  

   ```http
   PATCH http://[Organization URI]/api/data/v9.0/accounts(14e151db-9b4f-e611-80e0-00155da84c08) HTTP/1.1  
   If-Match: W/"628460"  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   Accept: application/json  
   {  
     "telephone1": "555-0003",  
     "revenue": 6000000  
   }  
   ```  

   <span data-ttu-id="9ff3f-174">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-174">**Response**</span></span>  

   ```http
   HTTP/1.1 204 No Content  
   ```  

   <span data-ttu-id="9ff3f-175">**Console output**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-175">**Console output**</span></span>  

   ```  
   Account successfully updated using ETag: W/"628460", status code: '204'.  
   ```  

4. <span data-ttu-id="9ff3f-176">Confirm the update succeeded by retrieving and outputting the current account state.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-176">Confirm the update succeeded by retrieving and outputting the current account state.</span></span>  <span data-ttu-id="9ff3f-177">This uses a basic GET request.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-177">This uses a basic GET request.</span></span>  

   <span data-ttu-id="9ff3f-178">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-178">**Request**</span></span>  

   ```http 
   GET http://[Organization URI]/api/data/v9.0/accounts(14e151db-9b4f-e611-80e0-00155da84c08)?$select=name,revenue,telephone1,description HTTP/1.1  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   Accept: application/json  
   ```  

   <span data-ttu-id="9ff3f-179">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-179">**Response**</span></span>  

   ```http
   HTTP/1.1 200 OK  
   Content-Type: application/json; odata.metadata=minimal  
   ETag: W/"628461"  
   OData-Version: 4.0  
   {  
     "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#accounts(name,revenue,telephone1,description)/$entity",  
     "@odata.etag":"W/\"628461\"",  
     "name":"Contoso Ltd",  
     "revenue":6000000.0000,  
     "telephone1":"555-0003",  
     "description":"Parent company of Contoso Pharmaceuticals, etc.",  
     "accountid":"14e151db-9b4f-e611-80e0-00155da84c08",  
     "_transactioncurrencyid_value":"0d4ed62e-95f7-e511-80d1-00155da84c03"  
   }  
   ```  

   <span data-ttu-id="9ff3f-180">**Console output**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-180">**Console output**</span></span>  

   ```
   {  
     "@odata.context": "http://[Organization URI]/api/data/v9.0/$metadata#accounts(name,revenue,telephone1,description)/$entity",  
     "@odata.etag": "W/\"628461\"",  
     "name": "Contoso Ltd",  
     "revenue": 6000000.0,  
     "telephone1": "555-0003",  
     "description": "Parent company of Contoso Pharmaceuticals, etc.",  
     "accountid": "14e151db-9b4f-e611-80e0-00155da84c08",  
     "_transactioncurrencyid_value": "0d4ed62e-95f7-e511-80d1-00155da84c03"  
   }  
   ```  

<a name="bkmk_controllingUpsert"></a>

## <a name="controlling-upsert-operations"></a><span data-ttu-id="9ff3f-181">Controlling upsert operations</span><span class="sxs-lookup"><span data-stu-id="9ff3f-181">Controlling upsert operations</span></span>

 <span data-ttu-id="9ff3f-182">This section of the program demonstrates how to perform conditional `PATCH` operations, limiting upsert operations to perform as either update-only or insert-only operations.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-182">This section of the program demonstrates how to perform conditional `PATCH` operations, limiting upsert operations to perform as either update-only or insert-only operations.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="9ff3f-183">[Limit upsert operations](perform-conditional-operations-using-web-api.md#bkmk_limitUpsertOperations)</span><span class="sxs-lookup"><span data-stu-id="9ff3f-183">[Limit upsert operations](perform-conditional-operations-using-web-api.md#bkmk_limitUpsertOperations)</span></span>  

1. <span data-ttu-id="9ff3f-184">Attempt to insert, without updating, the primary telephone and revenue properties for this account.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-184">Attempt to insert, without updating, the primary telephone and revenue properties for this account.</span></span> <span data-ttu-id="9ff3f-185">The `If-None-Match` header with the value of  `*` represents this upsert condition.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-185">The `If-None-Match` header with the value of  `*` represents this upsert condition.</span></span> <span data-ttu-id="9ff3f-186">This operation fails because this account record still exists on the server (unless it was concurrently deleted by another user or process).</span><span class="sxs-lookup"><span data-stu-id="9ff3f-186">This operation fails because this account record still exists on the server (unless it was concurrently deleted by another user or process).</span></span>  

   <span data-ttu-id="9ff3f-187">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-187">**Request**</span></span>  

   ```http
   PATCH http://[Organization URI]/api/data/v9.0/accounts(14e151db-9b4f-e611-80e0-00155da84c08) HTTP/1.1  
   If-None-Match: *  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   Accept: application/json  
   Content-Type: application/json; charset=utf-8  
   {  
     "telephone1": "555-0004",  
     "revenue": 7500000  
   }  
   ```  

   <span data-ttu-id="9ff3f-188">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-188">**Response**</span></span>  

   ```http
   HTTP/1.1 412 Precondition Failed  
   Content-Type: application/json; odata.metadata=minimal  
   OData-Version: 4.0  
   {  
     "error":{  
       "code":"","message":"A record with matching key values already exists.", . . .  
     }  
   }  
   ```  

   <span data-ttu-id="9ff3f-189">**Console output**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-189">**Console output**</span></span>  

   ```   
   Expected Error: A record with matching key values already exists.  
           Account not updated using ETag 'W/"628448", status code: '412'.    
   ```  

2. <span data-ttu-id="9ff3f-190">Attempt to perform the same update operation without creation.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-190">Attempt to perform the same update operation without creation.</span></span> <span data-ttu-id="9ff3f-191">To accomplish this, the conditional `If-Match` header is used with a value of `*`.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-191">To accomplish this, the conditional `If-Match` header is used with a value of `*`.</span></span>  <span data-ttu-id="9ff3f-192">This operation succeeds because the record exists on the server.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-192">This operation succeeds because the record exists on the server.</span></span>  

   <span data-ttu-id="9ff3f-193">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-193">**Request**</span></span>  

   ```http
   PATCH http://[Organization URI]/api/data/v9.0/accounts(14e151db-9b4f-e611-80e0-00155da84c08) HTTP/1.1  
   If-Match: *  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   Accept: application/json  
   Content-Type: application/json; charset=utf-8  
   {  
     "telephone1": "555-0005",  
     "revenue": 7500000  
   }  
   ```  

   <span data-ttu-id="9ff3f-194">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-194">**Response**</span></span>  

   ```http
   HTTP/1.1 204 No Content  
   ```  

   <span data-ttu-id="9ff3f-195">**Console output**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-195">**Console output**</span></span>  

   ```  
   Account updated using If-Match '*'  
   ```  

3. <span data-ttu-id="9ff3f-196">Retrieve and output the current account state with a basic `GET` request.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-196">Retrieve and output the current account state with a basic `GET` request.</span></span> <span data-ttu-id="9ff3f-197">Note that the returned ETag value has changed to reflect the new, updated version of the account record.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-197">Note that the returned ETag value has changed to reflect the new, updated version of the account record.</span></span>  

   <span data-ttu-id="9ff3f-198">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-198">**Request**</span></span>  

   ```http  
   GET http://[Organization URI]/api/data/v9.0/accounts(14e151db-9b4f-e611-80e0-00155da84c08)?$select=name,revenue,telephone1,description HTTP/1.1  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   Accept: application/json    
   ```  

   <span data-ttu-id="9ff3f-199">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-199">**Response**</span></span>  

   ```http  
   HTTP/1.1 200 OK  
   Content-Type: application/json; odata.metadata=minimal  
   ETag: W/"628463"  
   OData-Version: 4.0  
   {  
     "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#accounts(name,revenue,telephone1,description)/$entity",  
     "@odata.etag":"W/\"628463\"",  
     "name":"Contoso Ltd","revenue":7500000.0000,  
     "telephone1":"555-0005",  
     "description":"Parent company of Contoso Pharmaceuticals, etc.",  
     "accountid":"14e151db-9b4f-e611-80e0-00155da84c08",  
     "_transactioncurrencyid_value":"0d4ed62e-95f7-e511-80d1-00155da84c03"  
   }    
   ```  

   <span data-ttu-id="9ff3f-200">**Console output**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-200">**Console output**</span></span>  

   ```http    
   {  
     "@odata.context": "http://[Organization URI]/api/data/v9.0/$metadata#accounts(name,revenue,telephone1,description)/$entity",  
     "@odata.etag": "W/\"628463\"",  
     "name": "Contoso Ltd",  
     "revenue": 7500000.0,  
     "telephone1": "555-0005",  
     "description": "Parent company of Contoso Pharmaceuticals, etc.",  
     "accountid": "14e151db-9b4f-e611-80e0-00155da84c08",  
     "_transactioncurrencyid_value": "0d4ed62e-95f7-e511-80d1-00155da84c03"  
   }    
   ```  

4. <span data-ttu-id="9ff3f-201">Delete the account with a basic `DELETE`.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-201">Delete the account with a basic `DELETE`.</span></span>  

   <span data-ttu-id="9ff3f-202">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-202">**Request**</span></span>  

   ```http    
   DELETE http://[Organization URI]/api/data/v9.0/accounts(14e151db-9b4f-e611-80e0-00155da84c08) HTTP/1.1  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   Accept: application/json    
   ```  

   <span data-ttu-id="9ff3f-203">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-203">**Response**</span></span>  

   ```http
   HTTP/1.1 204 No Content  
   ```  

   <span data-ttu-id="9ff3f-204">**Console output**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-204">**Console output**</span></span>  

   ```  
   Account was deleted.  
   ```  

5. <span data-ttu-id="9ff3f-205">Just as in step 2, attempt to update the account if it exists.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-205">Just as in step 2, attempt to update the account if it exists.</span></span>  <span data-ttu-id="9ff3f-206">Again, this condition is represented by the `If-Match` header with a value of `*`.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-206">Again, this condition is represented by the `If-Match` header with a value of `*`.</span></span>  <span data-ttu-id="9ff3f-207">This operation fails because this record was just deleted.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-207">This operation fails because this record was just deleted.</span></span> <span data-ttu-id="9ff3f-208">However, if this `If-Match` header was absent, then the resulting basic upsert operation should successfully create a new record.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-208">However, if this `If-Match` header was absent, then the resulting basic upsert operation should successfully create a new record.</span></span>  

   <span data-ttu-id="9ff3f-209">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-209">**Request**</span></span>  

   ```http  
   PATCH http://[Organization URI]/api/data/v9.0/accounts(14e151db-9b4f-e611-80e0-00155da84c08) HTTP/1.1  
   If-Match: *  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   Accept: application/json  
   Content-Type: application/json; charset=utf-8  
   {  
     "telephone1": "555-0006",  
     "revenue": 7500000  
   }    
   ```  

   <span data-ttu-id="9ff3f-210">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-210">**Response**</span></span>  

   ```http    
   HTTP/1.1 404 Not Found  
   Content-Type: application/json; odata.metadata=minimal  
   OData-Version: 4.0  
   {  
     "error":{  
       "code":"","message":"account With Id = 14e151db-9b4f-e611-80e0-00155da84c08 Does Not Exist", . . .  
     }  
   }    
   ```  

   <span data-ttu-id="9ff3f-211">**Console output**</span><span class="sxs-lookup"><span data-stu-id="9ff3f-211">**Console output**</span></span>  

   ```    
   Expected Error: Account with Id = 14e151db-9b4f-e611-80e0-00155da84c08 does not exist.  
   Account not updated because it does not exist, status code: '404'.    
   ```  

   <span data-ttu-id="9ff3f-212">There is no need to cleanup sample data because the one account record was already deleted in step 4.</span><span class="sxs-lookup"><span data-stu-id="9ff3f-212">There is no need to cleanup sample data because the one account record was already deleted in step 4.</span></span>  

### <a name="see-also"></a><span data-ttu-id="9ff3f-213">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9ff3f-213">See also</span></span>

 <span data-ttu-id="9ff3f-214">[Use the Dynamics 365 for Customer Engagement Web API](../use-microsoft-dynamics-365-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="9ff3f-214">[Use the Dynamics 365 for Customer Engagement Web API](../use-microsoft-dynamics-365-web-api.md) </span></span>  
 <span data-ttu-id="9ff3f-215">[Perform conditional operations using the Web API](perform-conditional-operations-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="9ff3f-215">[Perform conditional operations using the Web API](perform-conditional-operations-using-web-api.md) </span></span>  
 [<span data-ttu-id="9ff3f-216">Web API Conditional Operations Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="9ff3f-216">Web API Conditional Operations Sample (C#)</span></span>](web-api-conditional-operations-sample-csharp.md)   
