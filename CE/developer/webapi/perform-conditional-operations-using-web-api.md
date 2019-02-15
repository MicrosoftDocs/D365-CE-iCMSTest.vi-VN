---
title: Perform conditional operations using the Web API (Dynamics 365 for Customer Engagement apps SDK)| MicrosoftDocs
description: Read how to create conditions that decide whether and how to perform certain operations using the Web API
ms.custom: ''
ms.date: 02/26/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 771002b0-825a-462d-bbf0-1aeba4b726c8
caps.latest.revision: 16
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2f5eb76900be72e792661a9b5126371ec48f5764
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387666"
---
# <a name="perform-conditional-operations-using-the-web-api"></a><span data-ttu-id="1f2af-103">Perform conditional operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="1f2af-103">Perform conditional operations using the Web API</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] <span data-ttu-id="1f2af-104">apps provides support for a set of conditional operations that rely upon the standard HTTP resource versioning mechanism known as *ETags*.</span><span class="sxs-lookup"><span data-stu-id="1f2af-104">apps provides support for a set of conditional operations that rely upon the standard HTTP resource versioning mechanism known as *ETags*.</span></span>  
  
<a name="bkmk_ETags"></a>   
## <a name="etags"></a><span data-ttu-id="1f2af-105">ETags</span><span class="sxs-lookup"><span data-stu-id="1f2af-105">ETags</span></span>  
 <span data-ttu-id="1f2af-106">The HTTP protocol defines an *entity tag*, or [ETag](https://msdn.microsoft.com/en-us/library/dd541486.aspx) for short, for identifying specific versions of a resource.</span><span class="sxs-lookup"><span data-stu-id="1f2af-106">The HTTP protocol defines an *entity tag*, or [ETag](https://msdn.microsoft.com/en-us/library/dd541486.aspx) for short, for identifying specific versions of a resource.</span></span> <span data-ttu-id="1f2af-107">ETags are opaque identifiers whose exact values are implementation dependent.</span><span class="sxs-lookup"><span data-stu-id="1f2af-107">ETags are opaque identifiers whose exact values are implementation dependent.</span></span> <span data-ttu-id="1f2af-108">ETag values occur in two varieties: strong and weak validation.</span><span class="sxs-lookup"><span data-stu-id="1f2af-108">ETag values occur in two varieties: strong and weak validation.</span></span> <span data-ttu-id="1f2af-109">Strong validation indicates that a unique resource, identified by a specific URI, will be identical on the binary level if its corresponding ETag value is unchanged.</span><span class="sxs-lookup"><span data-stu-id="1f2af-109">Strong validation indicates that a unique resource, identified by a specific URI, will be identical on the binary level if its corresponding ETag value is unchanged.</span></span> <span data-ttu-id="1f2af-110">Weak validation only guarantees that the resource representation is semantically equivalent for the same ETag value.</span><span class="sxs-lookup"><span data-stu-id="1f2af-110">Weak validation only guarantees that the resource representation is semantically equivalent for the same ETag value.</span></span>  
  
 [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] <span data-ttu-id="1f2af-111">apps generates a weakly validating `@odata.etag` property for every entity instance, and this property is automatically returned with each retrieved entity record.</span><span class="sxs-lookup"><span data-stu-id="1f2af-111">apps generates a weakly validating `@odata.etag` property for every entity instance, and this property is automatically returned with each retrieved entity record.</span></span> <span data-ttu-id="1f2af-112">For more information, see [Retrieve an entity using the Web API](retrieve-entity-using-web-api.md).</span><span class="sxs-lookup"><span data-stu-id="1f2af-112">For more information, see [Retrieve an entity using the Web API](retrieve-entity-using-web-api.md).</span></span>  
  
<a name="bkmk_ifMatchHeaders"></a>   
## <a name="if-match-and-if-none-match-headers"></a><span data-ttu-id="1f2af-113">If-Match and If-None-Match headers</span><span class="sxs-lookup"><span data-stu-id="1f2af-113">If-Match and If-None-Match headers</span></span>  
 <span data-ttu-id="1f2af-114">Use [If-Match](https://tools.ietf.org/html/rfc7232#section-3.1) and [If-None-Match](https://tools.ietf.org/html/rfc7232#section-3.2) headers with ETag values to check whether the current version of a resource matches the one last retrieved, matches any previous version or matches no version.</span><span class="sxs-lookup"><span data-stu-id="1f2af-114">Use [If-Match](https://tools.ietf.org/html/rfc7232#section-3.1) and [If-None-Match](https://tools.ietf.org/html/rfc7232#section-3.2) headers with ETag values to check whether the current version of a resource matches the one last retrieved, matches any previous version or matches no version.</span></span>  <span data-ttu-id="1f2af-115">These comparisons form the basis of conditional operation support.</span><span class="sxs-lookup"><span data-stu-id="1f2af-115">These comparisons form the basis of conditional operation support.</span></span> <span data-ttu-id="1f2af-116">Dynamics 365 for Customer Engagement apps provides ETags to support conditional retrievals, optimistic concurrency, and limited upsert operations.</span><span class="sxs-lookup"><span data-stu-id="1f2af-116">Dynamics 365 for Customer Engagement apps provides ETags to support conditional retrievals, optimistic concurrency, and limited upsert operations.</span></span>
 
 <span data-ttu-id="1f2af-117">Queries which expand collection-valued navigation properties may return cached data for those properties that doesn’t reflect recent changes.</span><span class="sxs-lookup"><span data-stu-id="1f2af-117">Queries which expand collection-valued navigation properties may return cached data for those properties that doesn’t reflect recent changes.</span></span> <span data-ttu-id="1f2af-118">It is recommended to use `If-None-Match` header with value `null` to override browser caching.</span><span class="sxs-lookup"><span data-stu-id="1f2af-118">It is recommended to use `If-None-Match` header with value `null` to override browser caching.</span></span> <span data-ttu-id="1f2af-119">See [HTTP Headers](compose-http-requests-handle-errors.md#bkmk_headers) for more details.</span><span class="sxs-lookup"><span data-stu-id="1f2af-119">See [HTTP Headers](compose-http-requests-handle-errors.md#bkmk_headers) for more details.</span></span> <span data-ttu-id="1f2af-120">Use `If-None-Match` header with a specific ETag value to ensure that only changed data is returned.</span><span class="sxs-lookup"><span data-stu-id="1f2af-120">Use `If-None-Match` header with a specific ETag value to ensure that only changed data is returned.</span></span>
  
> [!WARNING]
> <span data-ttu-id="1f2af-121">Client code should not give any meaning to the specific value of an ETag, nor to any apparent relationship between ETags beyond equality or inequality.</span><span class="sxs-lookup"><span data-stu-id="1f2af-121">Client code should not give any meaning to the specific value of an ETag, nor to any apparent relationship between ETags beyond equality or inequality.</span></span> <span data-ttu-id="1f2af-122">For example, an ETag value for a more recent version of a resource is not guaranteed to be greater than the ETag value for an earlier version.</span><span class="sxs-lookup"><span data-stu-id="1f2af-122">For example, an ETag value for a more recent version of a resource is not guaranteed to be greater than the ETag value for an earlier version.</span></span> <span data-ttu-id="1f2af-123">Also, the algorithm used to generate new ETag values may change without notice between releases of a service.</span><span class="sxs-lookup"><span data-stu-id="1f2af-123">Also, the algorithm used to generate new ETag values may change without notice between releases of a service.</span></span>  
  
<a name="bkmk_DetectIfChanged"></a>   
## <a name="conditional-retrievals"></a><span data-ttu-id="1f2af-124">Conditional retrievals</span><span class="sxs-lookup"><span data-stu-id="1f2af-124">Conditional retrievals</span></span>  
 <span data-ttu-id="1f2af-125">Etags enable you to optimize record retrievals whenever you access the same record multiple times.</span><span class="sxs-lookup"><span data-stu-id="1f2af-125">Etags enable you to optimize record retrievals whenever you access the same record multiple times.</span></span> <span data-ttu-id="1f2af-126">If you have previously retrieved a record, you can pass the ETag value with the `If-None-Match` header to request data to be retrieved only if it has changed since the last time it was retrieved.</span><span class="sxs-lookup"><span data-stu-id="1f2af-126">If you have previously retrieved a record, you can pass the ETag value with the `If-None-Match` header to request data to be retrieved only if it has changed since the last time it was retrieved.</span></span> <span data-ttu-id="1f2af-127">If the data has changed, the request returns an HTTP status of 200 (OK) with the latest data in the body of the request.</span><span class="sxs-lookup"><span data-stu-id="1f2af-127">If the data has changed, the request returns an HTTP status of 200 (OK) with the latest data in the body of the request.</span></span> <span data-ttu-id="1f2af-128">If the data hasn’t changed, the HTTP status code 304 (Not Modified) is returned to indicate that the entity hasn’t been modified.</span><span class="sxs-lookup"><span data-stu-id="1f2af-128">If the data hasn’t changed, the HTTP status code 304 (Not Modified) is returned to indicate that the entity hasn’t been modified.</span></span> <span data-ttu-id="1f2af-129">The following example message pair returns data for an account entity with the `accountid` equal to `00000000-0000-0000-0000-000000000001` when the data hasn’t changed since it was last retrieved.</span><span class="sxs-lookup"><span data-stu-id="1f2af-129">The following example message pair returns data for an account entity with the `accountid` equal to `00000000-0000-0000-0000-000000000001` when the data hasn’t changed since it was last retrieved.</span></span>  

> [!NOTE]
> <span data-ttu-id="1f2af-130">Conditional retrieval works only for entities that have optimistic concurrency enabled.</span><span class="sxs-lookup"><span data-stu-id="1f2af-130">Conditional retrieval works only for entities that have optimistic concurrency enabled.</span></span> <span data-ttu-id="1f2af-131">Check if an entity has optimistic concurrency enabled using the Web API request shown below.</span><span class="sxs-lookup"><span data-stu-id="1f2af-131">Check if an entity has optimistic concurrency enabled using the Web API request shown below.</span></span> <span data-ttu-id="1f2af-132">Entities that have optimistic concurrency enabled will have <xref href="Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsOptimisticConcurrencyEnabled?text=EntityMetadata.IsOptimisticConcurrencyEnabled" /> property set to `true`.</span><span class="sxs-lookup"><span data-stu-id="1f2af-132">Entities that have optimistic concurrency enabled will have <xref href="Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsOptimisticConcurrencyEnabled?text=EntityMetadata.IsOptimisticConcurrencyEnabled" /> property set to `true`.</span></span>
> ```HTTP
> GET [Organization URI]/api/data/v9.0/EntityDefinitions(LogicalName='<Entity Logical Name>')?$select=IsOptimisticConcurrencyEnabled
> ```
> <span data-ttu-id="1f2af-133">For more information about optimistic concurrency, see [Reduce potential data loss using optimistic concurrency](../org-service/reduce-potential-data-loss-using-optimistic-concurrency.md).</span><span class="sxs-lookup"><span data-stu-id="1f2af-133">For more information about optimistic concurrency, see [Reduce potential data loss using optimistic concurrency](../org-service/reduce-potential-data-loss-using-optimistic-concurrency.md).</span></span>  

 <span data-ttu-id="1f2af-134">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="1f2af-134">**Request**</span></span>  
```http  
GET [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)?$select=accountcategorycode,accountnumber,creditonhold,createdon,numberofemployees,name,revenue   HTTP/1.1  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
If-None-Match: W/"468026"  
```  
  
 <span data-ttu-id="1f2af-135">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="1f2af-135">**Response**</span></span>  
```json  
HTTP/1.1 304 Not Modified  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
```  
  
<a name="bkmk_limitUpsertOperations"></a>
  
## <a name="limit-upsert-operations"></a><span data-ttu-id="1f2af-136">Limit upsert operations</span><span class="sxs-lookup"><span data-stu-id="1f2af-136">Limit upsert operations</span></span>

 <span data-ttu-id="1f2af-137">An upsert ordinarily operates by creating an entity if it doesn’t exist; otherwise, it updates an existing entity.</span><span class="sxs-lookup"><span data-stu-id="1f2af-137">An upsert ordinarily operates by creating an entity if it doesn’t exist; otherwise, it updates an existing entity.</span></span> <span data-ttu-id="1f2af-138">However, ETags can be used to further constrain upserts to either prevent creates or to prevent updates.</span><span class="sxs-lookup"><span data-stu-id="1f2af-138">However, ETags can be used to further constrain upserts to either prevent creates or to prevent updates.</span></span>  
  
<a name="bkmk_preventCreateOnUpsert"></a>
 
### <a name="prevent-create-in-upsert"></a><span data-ttu-id="1f2af-139">Prevent create in upsert</span><span class="sxs-lookup"><span data-stu-id="1f2af-139">Prevent create in upsert</span></span>

 <span data-ttu-id="1f2af-140">If you are updating data and there is some possibility that the entity was deleted intentionally, you will not want to re-create the entity.</span><span class="sxs-lookup"><span data-stu-id="1f2af-140">If you are updating data and there is some possibility that the entity was deleted intentionally, you will not want to re-create the entity.</span></span> <span data-ttu-id="1f2af-141">To prevent this, add an `If-Match` header to the request with a value of "`*`".</span><span class="sxs-lookup"><span data-stu-id="1f2af-141">To prevent this, add an `If-Match` header to the request with a value of "`*`".</span></span>  
  
 <span data-ttu-id="1f2af-142">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="1f2af-142">**Request**</span></span>  
```http  
PATCH [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001) HTTP/1.1  
Content-Type: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
If-Match: "*"  
  
{  
    "name": "Updated Sample Account ",  
    "creditonhold": true,  
    "address1_latitude": 47.639583,  
    "description": "This is the updated description of the sample account",  
    "revenue": 6000000,  
    "accountcategorycode": 2  
}  
```  
  
 <span data-ttu-id="1f2af-143">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="1f2af-143">**Response**</span></span>  
 <span data-ttu-id="1f2af-144">If the entity is found, you’ll get a normal response with status 204 (No Content).</span><span class="sxs-lookup"><span data-stu-id="1f2af-144">If the entity is found, you’ll get a normal response with status 204 (No Content).</span></span> <span data-ttu-id="1f2af-145">When the entity is not found, you’ll get the following response with status 404 (Not Found).</span><span class="sxs-lookup"><span data-stu-id="1f2af-145">When the entity is not found, you’ll get the following response with status 404 (Not Found).</span></span>  
  
```json  
HTTP/1.1 404 Not Found  
OData-Version: 4.0  
Content-Type: application/json; odata.metadata=minimal  
  
{  
 "error": {  
  "code": "",  
  "message": "account With Id = 00000000-0000-0000-0000-000000000001 Does Not Exist",  
  "innererror": {  
   "message": "account With Id = 00000000-0000-0000-0000-000000000001 Does Not Exist",  
   "type": "System.ServiceModel.FaultException`1[[Microsoft.Xrm.Sdk.OrganizationServiceFault, Microsoft.Xrm.Sdk, Version=8.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]",  
   "stacktrace": <stack trace removed for brevity>  
  }  
 }  
}  
```  
  
<a name="bkmk_preventUpdateInUpsert"></a>
  
### <a name="prevent-update-in-upsert"></a><span data-ttu-id="1f2af-146">Prevent update in upsert</span><span class="sxs-lookup"><span data-stu-id="1f2af-146">Prevent update in upsert</span></span>

 <span data-ttu-id="1f2af-147">If you’re inserting data, there is some possibility that a record with the same `id` value already exists in the system and you may not want to update it.</span><span class="sxs-lookup"><span data-stu-id="1f2af-147">If you’re inserting data, there is some possibility that a record with the same `id` value already exists in the system and you may not want to update it.</span></span> <span data-ttu-id="1f2af-148">To prevent this, add an `If-None-Match` header to the request with a value of "`*`".</span><span class="sxs-lookup"><span data-stu-id="1f2af-148">To prevent this, add an `If-None-Match` header to the request with a value of "`*`".</span></span>  
  
 <span data-ttu-id="1f2af-149">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="1f2af-149">**Request**</span></span>  
```http  
PATCH [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001) HTTP/1.1  
Content-Type: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
If-None-Match: "*"  
  
{  
    "name": "Updated Sample Account ",  
    "creditonhold": true,  
    "address1_latitude": 47.639583,  
    "description": "This is the updated description of the sample account",  
    "revenue": 6000000,  
    "accountcategorycode": 2  
}  
```  
  
 <span data-ttu-id="1f2af-150">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="1f2af-150">**Response**</span></span>  
 <span data-ttu-id="1f2af-151">If the entity isn’t found, you will get a normal response with status 204 (No Content).</span><span class="sxs-lookup"><span data-stu-id="1f2af-151">If the entity isn’t found, you will get a normal response with status 204 (No Content).</span></span> <span data-ttu-id="1f2af-152">When the entity is found, you’ll get the following response with status 412 (Precondition Failed).</span><span class="sxs-lookup"><span data-stu-id="1f2af-152">When the entity is found, you’ll get the following response with status 412 (Precondition Failed).</span></span>  
  
```json  
HTTP/1.1 412 Precondition Failed  
OData-Version: 4.0  
Content-Type: application/json; odata.metadata=minimal  
  
{  
  "error":{  
   "code":"",  
   "message":"A record with matching key values already exists.",  
   "innererror":{  
    "message":"Cannot insert duplicate key.",  
    "type":"System.ServiceModel.FaultException`1[[Microsoft.Xrm.Sdk.OrganizationServiceFault, Microsoft.Xrm.Sdk, Version=8.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]",  
    "stacktrace":<stack trace removed for brevity>  
    }  
  }  
}  
```  
  
<a name="bkmk_Applyoptimisticconcurrency"></a>

## <a name="apply-optimistic-concurrency"></a><span data-ttu-id="1f2af-153">Apply optimistic concurrency</span><span class="sxs-lookup"><span data-stu-id="1f2af-153">Apply optimistic concurrency</span></span>

 <span data-ttu-id="1f2af-154">You can use optimistic concurrency to detect whether an entity has been modified since it was last retrieved.</span><span class="sxs-lookup"><span data-stu-id="1f2af-154">You can use optimistic concurrency to detect whether an entity has been modified since it was last retrieved.</span></span> <span data-ttu-id="1f2af-155">If the entity you intend to update or delete has changed on the server since you retrieved it, you may not want to complete the update or delete operation.</span><span class="sxs-lookup"><span data-stu-id="1f2af-155">If the entity you intend to update or delete has changed on the server since you retrieved it, you may not want to complete the update or delete operation.</span></span> <span data-ttu-id="1f2af-156">By applying the pattern shown here you can detect this situation, retrieve the most recent version of the entity, and apply any necessary criteria to re-evaluate whether to try the operation again.</span><span class="sxs-lookup"><span data-stu-id="1f2af-156">By applying the pattern shown here you can detect this situation, retrieve the most recent version of the entity, and apply any necessary criteria to re-evaluate whether to try the operation again.</span></span>  
  
<a name="bkmk_Applyoptimisticconcurrencyondelete"></a>

### <a name="apply-optimistic-concurrency-on-delete"></a><span data-ttu-id="1f2af-157">Apply optimistic concurrency on delete</span><span class="sxs-lookup"><span data-stu-id="1f2af-157">Apply optimistic concurrency on delete</span></span>

 <span data-ttu-id="1f2af-158">The following delete request for an account with `accountid` of`00000000-0000-0000-0000-000000000001` fails because the ETag value sent with the `If-Match` header is different from the current value.</span><span class="sxs-lookup"><span data-stu-id="1f2af-158">The following delete request for an account with `accountid` of`00000000-0000-0000-0000-000000000001` fails because the ETag value sent with the `If-Match` header is different from the current value.</span></span> <span data-ttu-id="1f2af-159">If the value had matched, a 204 (No Content) status is expected.</span><span class="sxs-lookup"><span data-stu-id="1f2af-159">If the value had matched, a 204 (No Content) status is expected.</span></span>  
  
 <span data-ttu-id="1f2af-160">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="1f2af-160">**Request**</span></span>

```http  
DELETE [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001) HTTP/1.1  
If-Match: W/"470867"  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
```  
  
 <span data-ttu-id="1f2af-161">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="1f2af-161">**Response**</span></span>

```json  
HTTP/1.1 412 Precondition Failed  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
  
{  
  "error":{  
    "code":"","message":"The version of the existing record doesn't match the RowVersion property provided.",  
    "innererror":{  
      "message":"The version of the existing record doesn't match the RowVersion property provided.",  
      "type":"System.ServiceModel.FaultException`1[[Microsoft.Xrm.Sdk.OrganizationServiceFault, Microsoft.Xrm.Sdk, Version=8.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]",  
"stacktrace":"  <stack trace details omitted for brevity>  
    }  
  }  
}  
```  
  
<a name="bkmk_Applyoptimisticconcurrencyonupdate"></a>

### <a name="apply-optimistic-concurrency-on-update"></a><span data-ttu-id="1f2af-162">Apply optimistic concurrency on update</span><span class="sxs-lookup"><span data-stu-id="1f2af-162">Apply optimistic concurrency on update</span></span>

 <span data-ttu-id="1f2af-163">The following update request for an account with `accountid` of `00000000-0000-0000-0000-000000000001` fails because the ETag value sent with the `If-Match` header is different from the current value.</span><span class="sxs-lookup"><span data-stu-id="1f2af-163">The following update request for an account with `accountid` of `00000000-0000-0000-0000-000000000001` fails because the ETag value sent with the `If-Match` header is different from the current value.</span></span> <span data-ttu-id="1f2af-164">If the value had matched, a 204 (No Content) status is expected.</span><span class="sxs-lookup"><span data-stu-id="1f2af-164">If the value had matched, a 204 (No Content) status is expected.</span></span>  
  
 <span data-ttu-id="1f2af-165">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="1f2af-165">**Request**</span></span>

```http  
PATCH [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001) HTTP/1.1  
If-Match: W/"470867"  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
  
{"name":"Updated Account Name"}  
```  
  
 <span data-ttu-id="1f2af-166">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="1f2af-166">**Response**</span></span>

```json  
HTTP/1.1 412 Precondition Failed  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
  
{  
  "error":{  
    "code":"","message":"The version of the existing record doesn't match the RowVersion property provided.",  
    "innererror":{  
      "message":"The version of the existing record doesn't match the RowVersion property provided.",  
      "type":"System.ServiceModel.FaultException`1[[Microsoft.Xrm.Sdk.OrganizationServiceFault, Microsoft.Xrm.Sdk, Version=8.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]",  
"stacktrace":"  <stack trace details omitted for brevity>  
    }  
  }  
}  
```  
  
### <a name="see-also"></a><span data-ttu-id="1f2af-167">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1f2af-167">See also</span></span>

 <span data-ttu-id="1f2af-168">[Web API Conditional Operations Sample (C#)](web-api-conditional-operations-sample-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="1f2af-168">[Web API Conditional Operations Sample (C#)](web-api-conditional-operations-sample-csharp.md) </span></span>  
 <span data-ttu-id="1f2af-169">[Web API Conditional Operations Sample (Client-side JavaScript)](web-api-conditional-operations-sample-client-side-javascript.md) </span><span class="sxs-lookup"><span data-stu-id="1f2af-169">[Web API Conditional Operations Sample (Client-side JavaScript)](web-api-conditional-operations-sample-client-side-javascript.md) </span></span>  
 <span data-ttu-id="1f2af-170">[Perform operations using the Web API](perform-operations-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="1f2af-170">[Perform operations using the Web API](perform-operations-web-api.md) </span></span>  
 <span data-ttu-id="1f2af-171">[Compose Http requests and handle errors](compose-http-requests-handle-errors.md) </span><span class="sxs-lookup"><span data-stu-id="1f2af-171">[Compose Http requests and handle errors](compose-http-requests-handle-errors.md) </span></span>  
 <span data-ttu-id="1f2af-172">[Query Data using the Web API](query-data-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="1f2af-172">[Query Data using the Web API](query-data-web-api.md) </span></span>  
 <span data-ttu-id="1f2af-173">[Create an entity using the Web API](create-entity-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="1f2af-173">[Create an entity using the Web API](create-entity-web-api.md) </span></span>  
 <span data-ttu-id="1f2af-174">[Retrieve an entity using the Web API](retrieve-entity-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="1f2af-174">[Retrieve an entity using the Web API](retrieve-entity-using-web-api.md) </span></span>  
 <span data-ttu-id="1f2af-175">[Update and delete entities using the Web API](update-delete-entities-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="1f2af-175">[Update and delete entities using the Web API](update-delete-entities-using-web-api.md) </span></span>  
 <span data-ttu-id="1f2af-176">[Associate and disassociate entities using the Web API](associate-disassociate-entities-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="1f2af-176">[Associate and disassociate entities using the Web API](associate-disassociate-entities-using-web-api.md) </span></span>  
 <span data-ttu-id="1f2af-177">[Use Web API functions](use-web-api-functions.md) </span><span class="sxs-lookup"><span data-stu-id="1f2af-177">[Use Web API functions](use-web-api-functions.md) </span></span>  
 <span data-ttu-id="1f2af-178">[Use Web API actions](use-web-api-actions.md) </span><span class="sxs-lookup"><span data-stu-id="1f2af-178">[Use Web API actions](use-web-api-actions.md) </span></span>  
 <span data-ttu-id="1f2af-179">[Execute batch operations using the Web API](execute-batch-operations-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="1f2af-179">[Execute batch operations using the Web API](execute-batch-operations-using-web-api.md) </span></span>  
 [<span data-ttu-id="1f2af-180">Impersonate another user using the Web API</span><span class="sxs-lookup"><span data-stu-id="1f2af-180">Impersonate another user using the Web API</span></span>](impersonate-another-user-web-api.md)
