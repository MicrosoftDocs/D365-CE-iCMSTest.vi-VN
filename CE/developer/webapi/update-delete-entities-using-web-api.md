---
title: Update and delete entities using the Web API (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how to perform update and delete operations on entities using the Web API
ms.custom: ''
ms.date: 05/09/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 694889fd-2b85-43a0-97bc-1e760695db31
caps.latest.revision: 17
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 33abefb0225fa67bddf0727aa87af433aaea63d8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387848"
---
# <a name="update-and-delete-entities-using-the-web-api"></a><span data-ttu-id="79c4b-103">Update and delete entities using the Web API</span><span class="sxs-lookup"><span data-stu-id="79c4b-103">Update and delete entities using the Web API</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="79c4b-104">Operations to modify data are a core part of the Web API.</span><span class="sxs-lookup"><span data-stu-id="79c4b-104">Operations to modify data are a core part of the Web API.</span></span> <span data-ttu-id="79c4b-105">In addition to a simple update and delete, you can perform operations on single attributes and compose *upsert* requests that will either update or insert an entity depending on whether it exists.</span><span class="sxs-lookup"><span data-stu-id="79c4b-105">In addition to a simple update and delete, you can perform operations on single attributes and compose *upsert* requests that will either update or insert an entity depending on whether it exists.</span></span>  

> [!NOTE]
>  <span data-ttu-id="79c4b-106">The metadata that defines entities is updated in a different way.</span><span class="sxs-lookup"><span data-stu-id="79c4b-106">The metadata that defines entities is updated in a different way.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="79c4b-107">[Create and update model entities using the Web API](create-update-entity-definitions-using-web-api.md)</span><span class="sxs-lookup"><span data-stu-id="79c4b-107">[Create and update model entities using the Web API](create-update-entity-definitions-using-web-api.md)</span></span>  

<a name="bkmk_update"></a>

## <a name="basic-update"></a><span data-ttu-id="79c4b-108">Basic update</span><span class="sxs-lookup"><span data-stu-id="79c4b-108">Basic update</span></span>

 <span data-ttu-id="79c4b-109">Update operations use the HTTP PATCH verb.</span><span class="sxs-lookup"><span data-stu-id="79c4b-109">Update operations use the HTTP PATCH verb.</span></span> <span data-ttu-id="79c4b-110">Pass a JSON object containing the properties you want to update to the URI that represents the entity.</span><span class="sxs-lookup"><span data-stu-id="79c4b-110">Pass a JSON object containing the properties you want to update to the URI that represents the entity.</span></span> <span data-ttu-id="79c4b-111">A response with a status of 204 will be returned if the update is successful.</span><span class="sxs-lookup"><span data-stu-id="79c4b-111">A response with a status of 204 will be returned if the update is successful.</span></span>  

 <span data-ttu-id="79c4b-112">This example updates an existing account record with the `accountid` value of 00000000-0000-0000-0000-000000000001.</span><span class="sxs-lookup"><span data-stu-id="79c4b-112">This example updates an existing account record with the `accountid` value of 00000000-0000-0000-0000-000000000001.</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="79c4b-113">When updating an entity, only include the properties you are changing in the request body.</span><span class="sxs-lookup"><span data-stu-id="79c4b-113">When updating an entity, only include the properties you are changing in the request body.</span></span> <span data-ttu-id="79c4b-114">Simply updating the properties of an entity that you previously retrieved, and including that JSON in your request, will update each property even though the value is the same.</span><span class="sxs-lookup"><span data-stu-id="79c4b-114">Simply updating the properties of an entity that you previously retrieved, and including that JSON in your request, will update each property even though the value is the same.</span></span> <span data-ttu-id="79c4b-115">This can cause system events that can trigger business logic that expects that the values have changed.</span><span class="sxs-lookup"><span data-stu-id="79c4b-115">This can cause system events that can trigger business logic that expects that the values have changed.</span></span> <span data-ttu-id="79c4b-116">This can cause properties to appear to have been updated in auditing data when in fact they haven’t actually changed.</span><span class="sxs-lookup"><span data-stu-id="79c4b-116">This can cause properties to appear to have been updated in auditing data when in fact they haven’t actually changed.</span></span>

 <span data-ttu-id="79c4b-117">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="79c4b-117">**Request**</span></span>

```http
PATCH [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001) HTTP/1.1  
Content-Type: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  

{  
    "name": "Updated Sample Account ",  
    "creditonhold": true,  
    "address1_latitude": 47.639583,  
    "description": "This is the updated description of the sample account",  
    "revenue": 6000000,  
    "accountcategorycode": 2  
}  
```  

 <span data-ttu-id="79c4b-118">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="79c4b-118">**Response**</span></span>

```http
HTTP/1.1 204 No Content  
OData-Version: 4.0  
```  

> [!NOTE]
>  <span data-ttu-id="79c4b-119">See [Associate entities on update](associate-disassociate-entities-using-web-api.md#bkmk_Associateentitiesonupdate) for information about associating entities on update.</span><span class="sxs-lookup"><span data-stu-id="79c4b-119">See [Associate entities on update](associate-disassociate-entities-using-web-api.md#bkmk_Associateentitiesonupdate) for information about associating entities on update.</span></span>  

<a name="bkmk_updateWithDataReturned"></a>

## <a name="update-with-data-returned"></a><span data-ttu-id="79c4b-120">Update with data returned</span><span class="sxs-lookup"><span data-stu-id="79c4b-120">Update with data returned</span></span>

> [!NOTE]
>  <span data-ttu-id="79c4b-121">This capability was added with [!INCLUDE[pn_crm_8_2_0_both](../../includes/pn-crm-8-2-0-both.md)].</span><span class="sxs-lookup"><span data-stu-id="79c4b-121">This capability was added with [!INCLUDE[pn_crm_8_2_0_both](../../includes/pn-crm-8-2-0-both.md)].</span></span>  

 <span data-ttu-id="79c4b-122">To retrieve data from an entity you are updating you can compose your PATCH request so that data from the created record will be returned with a status of 200 (OK).</span><span class="sxs-lookup"><span data-stu-id="79c4b-122">To retrieve data from an entity you are updating you can compose your PATCH request so that data from the created record will be returned with a status of 200 (OK).</span></span>  <span data-ttu-id="79c4b-123">To get his result, you must use the `return=representation` preference in the request headers.</span><span class="sxs-lookup"><span data-stu-id="79c4b-123">To get his result, you must use the `return=representation` preference in the request headers.</span></span>  

 <span data-ttu-id="79c4b-124">To control which properties are returned, append the `$select` query option to the URL to the entity set.</span><span class="sxs-lookup"><span data-stu-id="79c4b-124">To control which properties are returned, append the `$select` query option to the URL to the entity set.</span></span>  <span data-ttu-id="79c4b-125">The `$expand` query option will be ignored if used.</span><span class="sxs-lookup"><span data-stu-id="79c4b-125">The `$expand` query option will be ignored if used.</span></span>  

 <span data-ttu-id="79c4b-126">This example updates an account entity and returns the requested data in the response.</span><span class="sxs-lookup"><span data-stu-id="79c4b-126">This example updates an account entity and returns the requested data in the response.</span></span>  

 <span data-ttu-id="79c4b-127">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="79c4b-127">**Request**</span></span>

```http
PATCH [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)?$select=name,creditonhold,address1_latitude,description,revenue,accountcategorycode,createdon HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
Prefer: return=representation  

{"name":"Updated Sample Account"}  
```  

 <span data-ttu-id="79c4b-128">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="79c4b-128">**Response**</span></span> 

```http
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
Preference-Applied: return=representation  
OData-Version: 4.0  

{  
    "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#accounts/$entity",  
    "@odata.etag": "W/\"536537\"",  
    "accountid": "00000000-0000-0000-0000-000000000001",  
    "accountcategorycode": 1,  
    "description": "This is the description of the sample account",  
    "address1_latitude": 47.63958,  
    "creditonhold": false,  
    "name": "Updated Sample Account",  
    "createdon": "2016-09-28T23:14:00Z",  
    "revenue": 5000000.0000,  
    "_transactioncurrencyid_value": "048dddaa-6f7f-e611-80d3-00155db5e0b6"  
}  
```  

<a name="bkmk_updateSingleProperty"></a> 

## <a name="update-a-single-property-value"></a><span data-ttu-id="79c4b-129">Update a single property value</span><span class="sxs-lookup"><span data-stu-id="79c4b-129">Update a single property value</span></span>  

 <span data-ttu-id="79c4b-130">When you want to update only a single property value use a PUT request with the property name appended to the Uri of the entity.</span><span class="sxs-lookup"><span data-stu-id="79c4b-130">When you want to update only a single property value use a PUT request with the property name appended to the Uri of the entity.</span></span>  

 <span data-ttu-id="79c4b-131">The following example updates the name property of an existing account entity with the `accountid` value of 00000000-0000-0000-0000-000000000001.</span><span class="sxs-lookup"><span data-stu-id="79c4b-131">The following example updates the name property of an existing account entity with the `accountid` value of 00000000-0000-0000-0000-000000000001.</span></span>  

 <span data-ttu-id="79c4b-132">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="79c4b-132">**Request**</span></span>  

```http
PUT [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)/name HTTP/1.1  
Content-Type: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  

{"value": "Updated Sample Account Name"}  
```  

 <span data-ttu-id="79c4b-133">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="79c4b-133">**Response**</span></span>

```http
HTTP/1.1 204 No Content  
OData-Version: 4.0  
```  

<a name="bkmk_deleteSingleProperty"></a>

## <a name="delete-a-single-property-value"></a><span data-ttu-id="79c4b-134">Delete a single property value</span><span class="sxs-lookup"><span data-stu-id="79c4b-134">Delete a single property value</span></span>

 <span data-ttu-id="79c4b-135">To delete the value of a single property use a DELETE request with the property name appended to the Uri of the entity.</span><span class="sxs-lookup"><span data-stu-id="79c4b-135">To delete the value of a single property use a DELETE request with the property name appended to the Uri of the entity.</span></span>  

 <span data-ttu-id="79c4b-136">The following example deletes the value of the `description` property of an account entity with the `accountid` value of 00000000-0000-0000-0000-000000000001.</span><span class="sxs-lookup"><span data-stu-id="79c4b-136">The following example deletes the value of the `description` property of an account entity with the `accountid` value of 00000000-0000-0000-0000-000000000001.</span></span>  

 <span data-ttu-id="79c4b-137">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="79c4b-137">**Request**</span></span>

```http
DELETE [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)/description HTTP/1.1  
Content-Type: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
```  

 <span data-ttu-id="79c4b-138">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="79c4b-138">**Response**</span></span>

```http
HTTP/1.1 204 No Content  
OData-Version: 4.0  
```  

> [!NOTE]
>  <span data-ttu-id="79c4b-139">This can’t be used with a single-valued navigation property to disassociate two entities.</span><span class="sxs-lookup"><span data-stu-id="79c4b-139">This can’t be used with a single-valued navigation property to disassociate two entities.</span></span> <span data-ttu-id="79c4b-140">For an alternative approach, see [Remove a reference to an entity](associate-disassociate-entities-using-web-api.md#bkmk_Removeareferencetoanentity).</span><span class="sxs-lookup"><span data-stu-id="79c4b-140">For an alternative approach, see [Remove a reference to an entity](associate-disassociate-entities-using-web-api.md#bkmk_Removeareferencetoanentity).</span></span>  

<a name="bkmk_upsert"></a>

## <a name="upsert-an-entity"></a><span data-ttu-id="79c4b-141">Upsert an entity</span><span class="sxs-lookup"><span data-stu-id="79c4b-141">Upsert an entity</span></span>

 <span data-ttu-id="79c4b-142">An *upsert* operation is exactly like an update.</span><span class="sxs-lookup"><span data-stu-id="79c4b-142">An *upsert* operation is exactly like an update.</span></span> <span data-ttu-id="79c4b-143">It uses a `PATCH` request and uses a URI to reference a specific entity.</span><span class="sxs-lookup"><span data-stu-id="79c4b-143">It uses a `PATCH` request and uses a URI to reference a specific entity.</span></span> <span data-ttu-id="79c4b-144">The difference is that if the entity doesn’t exist it will be created.</span><span class="sxs-lookup"><span data-stu-id="79c4b-144">The difference is that if the entity doesn’t exist it will be created.</span></span> <span data-ttu-id="79c4b-145">If it already exists, it will be updated.</span><span class="sxs-lookup"><span data-stu-id="79c4b-145">If it already exists, it will be updated.</span></span> <span data-ttu-id="79c4b-146">Normally when creating a new entity you will let the system assign a unique identifier.</span><span class="sxs-lookup"><span data-stu-id="79c4b-146">Normally when creating a new entity you will let the system assign a unique identifier.</span></span> <span data-ttu-id="79c4b-147">This is a best practice.</span><span class="sxs-lookup"><span data-stu-id="79c4b-147">This is a best practice.</span></span> <span data-ttu-id="79c4b-148">But if you need to create a record with a specific `id` value, an `upsert` operation provides a way to do this.</span><span class="sxs-lookup"><span data-stu-id="79c4b-148">But if you need to create a record with a specific `id` value, an `upsert` operation provides a way to do this.</span></span> <span data-ttu-id="79c4b-149">This can be valuable in situation where you are synchronizing data in different systems.</span><span class="sxs-lookup"><span data-stu-id="79c4b-149">This can be valuable in situation where you are synchronizing data in different systems.</span></span>  

 <span data-ttu-id="79c4b-150">Sometimes there are situations where you want to perform an `upsert`, but you want to prevent one of the potential default actions: either create or update.</span><span class="sxs-lookup"><span data-stu-id="79c4b-150">Sometimes there are situations where you want to perform an `upsert`, but you want to prevent one of the potential default actions: either create or update.</span></span>      <span data-ttu-id="79c4b-151">You can accomplish this through the addition of `If-Match` or `If-None-Match` headers.</span><span class="sxs-lookup"><span data-stu-id="79c4b-151">You can accomplish this through the addition of `If-Match` or `If-None-Match` headers.</span></span> <span data-ttu-id="79c4b-152">For more information, see [Limit upsert operations](perform-conditional-operations-using-web-api.md#bkmk_limitUpsertOperations).</span><span class="sxs-lookup"><span data-stu-id="79c4b-152">For more information, see [Limit upsert operations](perform-conditional-operations-using-web-api.md#bkmk_limitUpsertOperations).</span></span>  

<a name="bkmk_delete"></a>

## <a name="basic-delete"></a><span data-ttu-id="79c4b-153">Basic delete</span><span class="sxs-lookup"><span data-stu-id="79c4b-153">Basic delete</span></span>

 <span data-ttu-id="79c4b-154">A delete operation is very straightforward.</span><span class="sxs-lookup"><span data-stu-id="79c4b-154">A delete operation is very straightforward.</span></span> <span data-ttu-id="79c4b-155">Use the DELETE verb with the URI of the entity you want to delete.</span><span class="sxs-lookup"><span data-stu-id="79c4b-155">Use the DELETE verb with the URI of the entity you want to delete.</span></span> <span data-ttu-id="79c4b-156">This example message deletes an account entity with the primary key `accountid` value equal to 00000000-0000-0000-0000-000000000001.</span><span class="sxs-lookup"><span data-stu-id="79c4b-156">This example message deletes an account entity with the primary key `accountid` value equal to 00000000-0000-0000-0000-000000000001.</span></span>  

 <span data-ttu-id="79c4b-157">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="79c4b-157">**Request**</span></span>

```http
DELETE [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001) HTTP/1.1  
Content-Type: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
```  

 <span data-ttu-id="79c4b-158">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="79c4b-158">**Response**</span></span>

 <span data-ttu-id="79c4b-159">If the entity exists, you’ll get a normal response with status 204 to indicate the delete was successful.</span><span class="sxs-lookup"><span data-stu-id="79c4b-159">If the entity exists, you’ll get a normal response with status 204 to indicate the delete was successful.</span></span> <span data-ttu-id="79c4b-160">If the entity isn’t found, you’ll get a response with status 404.</span><span class="sxs-lookup"><span data-stu-id="79c4b-160">If the entity isn’t found, you’ll get a response with status 404.</span></span>  

```http
HTTP/1.1 204 No Content  
OData-Version: 4.0  
```  

<a name="bkmk_duplicate"></a>

## <a name="check-for-duplicate-records"></a><span data-ttu-id="79c4b-161">Check for Duplicate records</span><span class="sxs-lookup"><span data-stu-id="79c4b-161">Check for Duplicate records</span></span>

<span data-ttu-id="79c4b-162">By default, duplicate detection is suppressed when you are updating records using the Web API.</span><span class="sxs-lookup"><span data-stu-id="79c4b-162">By default, duplicate detection is suppressed when you are updating records using the Web API.</span></span> <span data-ttu-id="79c4b-163">You must include the `MSCRM.SuppressDuplicateDetection: false` header with your PATCH request to enable duplicate detection .</span><span class="sxs-lookup"><span data-stu-id="79c4b-163">You must include the `MSCRM.SuppressDuplicateDetection: false` header with your PATCH request to enable duplicate detection .</span></span> <span data-ttu-id="79c4b-164">Duplicate detection only applies when the organization has enabled duplicate detection, the entity is enabled for duplicate detection, and there are active duplicate detection rules being applied.</span><span class="sxs-lookup"><span data-stu-id="79c4b-164">Duplicate detection only applies when the organization has enabled duplicate detection, the entity is enabled for duplicate detection, and there are active duplicate detection rules being applied.</span></span> <span data-ttu-id="79c4b-165">For more information, see [Detect duplicate data for developers](../detect-duplicate-data-for-developers.md).</span><span class="sxs-lookup"><span data-stu-id="79c4b-165">For more information, see [Detect duplicate data for developers](../detect-duplicate-data-for-developers.md).</span></span>

<span data-ttu-id="79c4b-166">See [Detect duplicates during Update operation using the Web API](manage-duplicate-detection-create-update.md#bkmk_update) for more information on how to check for duplicate records during Update operation.</span><span class="sxs-lookup"><span data-stu-id="79c4b-166">See [Detect duplicates during Update operation using the Web API](manage-duplicate-detection-create-update.md#bkmk_update) for more information on how to check for duplicate records during Update operation.</span></span>

### <a name="see-also"></a><span data-ttu-id="79c4b-167">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="79c4b-167">See also</span></span>

 <span data-ttu-id="79c4b-168">[Web API Basic Operations Sample (C#)](web-api-basic-operations-sample-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="79c4b-168">[Web API Basic Operations Sample (C#)](web-api-basic-operations-sample-csharp.md) </span></span>  
 <span data-ttu-id="79c4b-169">[Web API Basic Operations Sample (Client-side JavaScript)](web-api-basic-operations-sample-client-side-javascript.md) </span><span class="sxs-lookup"><span data-stu-id="79c4b-169">[Web API Basic Operations Sample (Client-side JavaScript)](web-api-basic-operations-sample-client-side-javascript.md) </span></span>  
 <span data-ttu-id="79c4b-170">[Perform operations using the Web API](perform-operations-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="79c4b-170">[Perform operations using the Web API](perform-operations-web-api.md) </span></span>  
 <span data-ttu-id="79c4b-171">[Compose Http requests and handle errors](compose-http-requests-handle-errors.md) </span><span class="sxs-lookup"><span data-stu-id="79c4b-171">[Compose Http requests and handle errors](compose-http-requests-handle-errors.md) </span></span>  
 <span data-ttu-id="79c4b-172">[Query Data using the Web API](query-data-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="79c4b-172">[Query Data using the Web API](query-data-web-api.md) </span></span>  
 <span data-ttu-id="79c4b-173">[Create an entity using the Web API](create-entity-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="79c4b-173">[Create an entity using the Web API](create-entity-web-api.md) </span></span>  
 <span data-ttu-id="79c4b-174">[Retrieve an entity using the Web API](retrieve-entity-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="79c4b-174">[Retrieve an entity using the Web API](retrieve-entity-using-web-api.md) </span></span>  
 <span data-ttu-id="79c4b-175">[Associate and disassociate entities using the Web API](associate-disassociate-entities-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="79c4b-175">[Associate and disassociate entities using the Web API](associate-disassociate-entities-using-web-api.md) </span></span>  
 <span data-ttu-id="79c4b-176">[Use Web API functions](use-web-api-functions.md) </span><span class="sxs-lookup"><span data-stu-id="79c4b-176">[Use Web API functions](use-web-api-functions.md) </span></span>  
 <span data-ttu-id="79c4b-177">[Use Web API actions](use-web-api-actions.md) </span><span class="sxs-lookup"><span data-stu-id="79c4b-177">[Use Web API actions](use-web-api-actions.md) </span></span>  
 <span data-ttu-id="79c4b-178">[Execute batch operations using the Web API](execute-batch-operations-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="79c4b-178">[Execute batch operations using the Web API](execute-batch-operations-using-web-api.md) </span></span>  
 <span data-ttu-id="79c4b-179">[Impersonate another user using the Web API](impersonate-another-user-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="79c4b-179">[Impersonate another user using the Web API](impersonate-another-user-web-api.md) </span></span>  
 [<span data-ttu-id="79c4b-180">Perform conditional operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="79c4b-180">Perform conditional operations using the Web API</span></span>](perform-conditional-operations-using-web-api.md)
