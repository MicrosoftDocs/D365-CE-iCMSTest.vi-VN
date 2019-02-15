---
title: Create an entity using the Web API (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Read how to create a POST request to send data to create an entity on Dynamics 365 for Customer Engagement using the Web API
ms.custom: ''
ms.date: 11/16/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 244259ca-2fbc-4fd4-9a74-6166e6683355
caps.latest.revision: 51
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bfc5c70b52602111951e4165d2903f17b366aa63
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386740"
---
# <a name="create-an-entity-using-the-web-api"></a><span data-ttu-id="003e4-103">Create an entity using the Web API</span><span class="sxs-lookup"><span data-stu-id="003e4-103">Create an entity using the Web API</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="003e4-104">Use a POST request to send data to create an entity.</span><span class="sxs-lookup"><span data-stu-id="003e4-104">Use a POST request to send data to create an entity.</span></span> <span data-ttu-id="003e4-105">You can create multiple related entities in a single operation using ‘deep insert’.</span><span class="sxs-lookup"><span data-stu-id="003e4-105">You can create multiple related entities in a single operation using ‘deep insert’.</span></span> <span data-ttu-id="003e4-106">You also need to know how to set values to associate a new entity to existing entities using the @odata.bind annotation.</span><span class="sxs-lookup"><span data-stu-id="003e4-106">You also need to know how to set values to associate a new entity to existing entities using the @odata.bind annotation.</span></span>  

> [!NOTE]
> <span data-ttu-id="003e4-107">For information about how to create and update the entity metadata using the Web API, see [Create and update entity definitions using the Web API](create-update-entity-definitions-using-web-api.md).</span><span class="sxs-lookup"><span data-stu-id="003e4-107">For information about how to create and update the entity metadata using the Web API, see [Create and update entity definitions using the Web API](create-update-entity-definitions-using-web-api.md).</span></span>

<a name="bkmk_basicCreate"></a>

## <a name="basic-create"></a><span data-ttu-id="003e4-108">Basic Create</span><span class="sxs-lookup"><span data-stu-id="003e4-108">Basic Create</span></span>

 <span data-ttu-id="003e4-109">This example creates a new account entity.</span><span class="sxs-lookup"><span data-stu-id="003e4-109">This example creates a new account entity.</span></span> <span data-ttu-id="003e4-110">The response `OData-EntityId` header contains the Uri of the created entity.</span><span class="sxs-lookup"><span data-stu-id="003e4-110">The response `OData-EntityId` header contains the Uri of the created entity.</span></span>

 <span data-ttu-id="003e4-111">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="003e4-111">**Request**</span></span>

```http

POST [Organization URI]/api/data/v9.0/accounts HTTP/1.1
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "name": "Sample Account",
    "creditonhold": false,
    "address1_latitude": 47.639583,
    "description": "This is the description of the sample account",
    "revenue": 5000000,
    "accountcategorycode": 1
}
```

 <span data-ttu-id="003e4-112">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="003e4-112">**Response**</span></span>

```http

HTTP/1.1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.0/accounts(7eb682f1-ca75-e511-80d4-00155d2a68d1)
```

 <span data-ttu-id="003e4-113">To create a new entity you must identify the valid property names and types.</span><span class="sxs-lookup"><span data-stu-id="003e4-113">To create a new entity you must identify the valid property names and types.</span></span> <span data-ttu-id="003e4-114">For all system entities and attributes, you can find this information in the topic for that entity in the [Web API EntityType Reference](../about-entity-reference.md).</span><span class="sxs-lookup"><span data-stu-id="003e4-114">For all system entities and attributes, you can find this information in the topic for that entity in the [Web API EntityType Reference](../about-entity-reference.md).</span></span> <span data-ttu-id="003e4-115">For custom entities or attributes, refer to the definition of that entity in the [CSDL metadata document](web-api-types-operations.md#bkmk_csdl).</span><span class="sxs-lookup"><span data-stu-id="003e4-115">For custom entities or attributes, refer to the definition of that entity in the [CSDL metadata document](web-api-types-operations.md#bkmk_csdl).</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="003e4-116">[Entity types](web-api-types-operations.md#bkmk_entityTypes)</span><span class="sxs-lookup"><span data-stu-id="003e4-116">[Entity types](web-api-types-operations.md#bkmk_entityTypes)</span></span>

<a name="bkmk_CreateRelated"></a>

## <a name="create-related-entities-in-one-operation"></a><span data-ttu-id="003e4-117">Create related entities in one operation</span><span class="sxs-lookup"><span data-stu-id="003e4-117">Create related entities in one operation</span></span>

 <span data-ttu-id="003e4-118">You can create entities related to each other by defining them as navigation properties values.</span><span class="sxs-lookup"><span data-stu-id="003e4-118">You can create entities related to each other by defining them as navigation properties values.</span></span> <span data-ttu-id="003e4-119">This is known as *deep insert*.</span><span class="sxs-lookup"><span data-stu-id="003e4-119">This is known as *deep insert*.</span></span>

 <span data-ttu-id="003e4-120">As with a basic create, the response `OData-EntityId` header contains the Uri of the created entity.</span><span class="sxs-lookup"><span data-stu-id="003e4-120">As with a basic create, the response `OData-EntityId` header contains the Uri of the created entity.</span></span> <span data-ttu-id="003e4-121">The URIs for the related entities created aren’t returned.</span><span class="sxs-lookup"><span data-stu-id="003e4-121">The URIs for the related entities created aren’t returned.</span></span>

 <span data-ttu-id="003e4-122">For example, the following request body posted to the `Account` entity set will create a total of four new entities in the context of creating an account.</span><span class="sxs-lookup"><span data-stu-id="003e4-122">For example, the following request body posted to the `Account` entity set will create a total of four new entities in the context of creating an account.</span></span>

- <span data-ttu-id="003e4-123">A contact is created because it is defined as an object property of the single-valued navigation property `primarycontactid`.</span><span class="sxs-lookup"><span data-stu-id="003e4-123">A contact is created because it is defined as an object property of the single-valued navigation property `primarycontactid`.</span></span>

- <span data-ttu-id="003e4-124">An opportunity is created because it is defined as an object within an array that is set to the value of a collection-valued navigation property `opportunity_customer_accounts`.</span><span class="sxs-lookup"><span data-stu-id="003e4-124">An opportunity is created because it is defined as an object within an array that is set to the value of a collection-valued navigation property `opportunity_customer_accounts`.</span></span>

- <span data-ttu-id="003e4-125">A task is created because it is defined an object within an array that is set to the value of a collection-valued navigation property `Opportunity_Tasks`.</span><span class="sxs-lookup"><span data-stu-id="003e4-125">A task is created because it is defined an object within an array that is set to the value of a collection-valued navigation property `Opportunity_Tasks`.</span></span>

<span data-ttu-id="003e4-126">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="003e4-126">**Request**</span></span>

```http
POST [Organization URI]/api/data/v9.0/accounts HTTP/1.1
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
 "name": "Sample Account",
 "primarycontactid":
 {
     "firstname": "John",
     "lastname": "Smith"
 },
 "opportunity_customer_accounts":
 [
  {
      "name": "Opportunity associated to Sample Account",
      "Opportunity_Tasks":
      [
       { "subject": "Task associated to opportunity" }
      ]
  }
 ]
}
```

<span data-ttu-id="003e4-127">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="003e4-127">**Response**</span></span>

 ```http

HTTP/1.1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.0/accounts(3c6e4b5f-86f6-e411-80dd-00155d2a68cb)
```

<a name="bkmk_associateOnCreate"></a>

## <a name="associate-entities-on-create"></a><span data-ttu-id="003e4-128">Associate entities on create</span><span class="sxs-lookup"><span data-stu-id="003e4-128">Associate entities on create</span></span>

 <span data-ttu-id="003e4-129">To associate new entities to existing entities when they are created you must set the value of single-valued navigation properties using the `@odata.bind` annotation.</span><span class="sxs-lookup"><span data-stu-id="003e4-129">To associate new entities to existing entities when they are created you must set the value of single-valued navigation properties using the `@odata.bind` annotation.</span></span>

 <span data-ttu-id="003e4-130">The following request body posted to the accounts entity set will create a new account associated with an existing contact with the `contactid` value of 00000000-0000-0000-0000-000000000001.</span><span class="sxs-lookup"><span data-stu-id="003e4-130">The following request body posted to the accounts entity set will create a new account associated with an existing contact with the `contactid` value of 00000000-0000-0000-0000-000000000001.</span></span>

<span data-ttu-id="003e4-131">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="003e4-131">**Request**</span></span>

```http

POST [Organization URI]/api/data/v9.0/accounts HTTP/1.1
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
"name":"Sample Account",
"primarycontactid@odata.bind":"/contacts(00000000-0000-0000-0000-000000000001)"
}
```

<span data-ttu-id="003e4-132">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="003e4-132">**Response**</span></span>

```http

HTTP/1.1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000002)
```

> [!NOTE]
> <span data-ttu-id="003e4-133">Associating entities this way using a collection-valued navigation property is not supported by the Web API.</span><span class="sxs-lookup"><span data-stu-id="003e4-133">Associating entities this way using a collection-valued navigation property is not supported by the Web API.</span></span>

<a name="bkmk_SuppressDuplicateDetection"></a>

## <a name="check-for-duplicate-records"></a><span data-ttu-id="003e4-134">Check for Duplicate records</span><span class="sxs-lookup"><span data-stu-id="003e4-134">Check for Duplicate records</span></span>

 <span data-ttu-id="003e4-135">By default, duplicate detection is suppressed when you are creating records using the Web API.</span><span class="sxs-lookup"><span data-stu-id="003e4-135">By default, duplicate detection is suppressed when you are creating records using the Web API.</span></span> <span data-ttu-id="003e4-136">You must include the `MSCRM.SuppressDuplicateDetection: false` header with your POST request to enable duplicate detection .</span><span class="sxs-lookup"><span data-stu-id="003e4-136">You must include the `MSCRM.SuppressDuplicateDetection: false` header with your POST request to enable duplicate detection .</span></span> <span data-ttu-id="003e4-137">Duplicate detection only applies when the organization has enabled duplicate detection, the entity is enabled for duplicate detection, and there are active duplicate detection rules being applied.</span><span class="sxs-lookup"><span data-stu-id="003e4-137">Duplicate detection only applies when the organization has enabled duplicate detection, the entity is enabled for duplicate detection, and there are active duplicate detection rules being applied.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="003e4-138">[Detect duplicate data for developers](../detect-duplicate-data-for-developers.md)</span><span class="sxs-lookup"><span data-stu-id="003e4-138">[Detect duplicate data for developers](../detect-duplicate-data-for-developers.md)</span></span>

 <span data-ttu-id="003e4-139">See [Manage duplicate detection during Create and Update operations using Web API](manage-duplicate-detection-create-update.md#bkmk_create) for more information on how to check for duplicate records during Create operation.</span><span class="sxs-lookup"><span data-stu-id="003e4-139">See [Manage duplicate detection during Create and Update operations using Web API](manage-duplicate-detection-create-update.md#bkmk_create) for more information on how to check for duplicate records during Create operation.</span></span>

<a name="bkmk_initializefrom"></a>

## <a name="create-a-new-entity-from-another-entity"></a><span data-ttu-id="003e4-140">Create a new entity from another entity</span><span class="sxs-lookup"><span data-stu-id="003e4-140">Create a new entity from another entity</span></span>

<span data-ttu-id="003e4-141">Use `InitializeFrom function` to create a new record in the context of an existing record where a mapping exists between the entities to which the records belong.</span><span class="sxs-lookup"><span data-stu-id="003e4-141">Use `InitializeFrom function` to create a new record in the context of an existing record where a mapping exists between the entities to which the records belong.</span></span> 

<span data-ttu-id="003e4-142">The following example shows how to create an account record using the attribute values of an existing record of account entity with `accountid` value equal to c65127ed-2097-e711-80eb-00155db75426.</span><span class="sxs-lookup"><span data-stu-id="003e4-142">The following example shows how to create an account record using the attribute values of an existing record of account entity with `accountid` value equal to c65127ed-2097-e711-80eb-00155db75426.</span></span>

<span data-ttu-id="003e4-143">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="003e4-143">**Request**</span></span>

```http
GET [Organization URI]/api/data/v9.0/InitializeFrom(EntityMoniker=@p1,TargetEntityName=@p2,TargetFieldType=@p3)?@p1={'@odata.id':'accounts(c65127ed-2097-e711-80eb-00155db75426)'}&@p2='account'&@p3=Microsoft.Dynamics.CRM.TargetFieldType'ValidForCreate' HTTP/1.1
If-None-Match: null
OData-Version: 4.0
OData-MaxVersion: 4.0
Content-Type: application/json
Accept: application/json
```

<span data-ttu-id="003e4-144">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="003e4-144">**Response**</span></span>

```json
{
        "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#accounts/$entity",
        "@odata.type": "#Microsoft.Dynamics.CRM.account",
        "parentaccountid@odata.bind": "accounts(c65127ed-2097-e711-80eb-00155db75426)",
        "transactioncurrencyid@odata.bind": "transactioncurrencies(732e87e1-1d96-e711-80e4-00155db75426)",
        "address1_line1":"123 Maple St.",
        "address1_city":"Seattle",
        "address1_country":"United States of America"
}
```

<span data-ttu-id="003e4-145">The response received from InitializeFrom request consists of values of mapped attributes between the source entity and target entity and the GUID of parent record.</span><span class="sxs-lookup"><span data-stu-id="003e4-145">The response received from InitializeFrom request consists of values of mapped attributes between the source entity and target entity and the GUID of parent record.</span></span> <span data-ttu-id="003e4-146">The attribute mapping between entities that have an entity relationship is different for different entity sets and is customizable, so the response from InitializeFrom function request may vary for different entities and organizations.</span><span class="sxs-lookup"><span data-stu-id="003e4-146">The attribute mapping between entities that have an entity relationship is different for different entity sets and is customizable, so the response from InitializeFrom function request may vary for different entities and organizations.</span></span> <span data-ttu-id="003e4-147">When this response is passed in the body of create request of the new record, these attribute values are replicated in the new record.</span><span class="sxs-lookup"><span data-stu-id="003e4-147">When this response is passed in the body of create request of the new record, these attribute values are replicated in the new record.</span></span> <span data-ttu-id="003e4-148">The values of custom mapped attributes also get set in the new record during the process.</span><span class="sxs-lookup"><span data-stu-id="003e4-148">The values of custom mapped attributes also get set in the new record during the process.</span></span>

> [!NOTE]
> <span data-ttu-id="003e4-149">To determine whether two entities can be mapped, use this query:</span><span class="sxs-lookup"><span data-stu-id="003e4-149">To determine whether two entities can be mapped, use this query:</span></span>  
<span data-ttu-id="003e4-150">GET [Organization URI]/api/data/v9.0/entitymaps?$select=sourceentityname,targetentityname&$orderby=sourceentityname</span><span class="sxs-lookup"><span data-stu-id="003e4-150">GET [Organization URI]/api/data/v9.0/entitymaps?$select=sourceentityname,targetentityname&$orderby=sourceentityname</span></span>

<span data-ttu-id="003e4-151">Other attribute values can also be set and/or modified for the new record by adding them in the JSON request body, as shown in the example below.</span><span class="sxs-lookup"><span data-stu-id="003e4-151">Other attribute values can also be set and/or modified for the new record by adding them in the JSON request body, as shown in the example below.</span></span>

```http
POST [Organization URI]/api/data/v9.0/accounts HTTP/1.1
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

    {
        "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#accounts/$entity",
        "@odata.type": "#Microsoft.Dynamics.CRM.account",
        "parentaccountid@odata.bind": "accounts(c65127ed-2097-e711-80eb-00155db75426)",
        "transactioncurrencyid@odata.bind": "transactioncurrencies(732e87e1-1d96-e711-80e4-00155db75426)",
        "name":"Contoso Ltd",
        "numberofemployees":"200",
        "address1_line1":"100 Maple St.",
        "address1_city":"Seattle",
        "address1_country":"United States of America",
        "fax":"73737"
    }
}
```

<a name="bkmk_createWithDataReturned"></a>

## <a name="create-with-data-returned"></a><span data-ttu-id="003e4-152">Create with data returned</span><span class="sxs-lookup"><span data-stu-id="003e4-152">Create with data returned</span></span>

> [!NOTE]
> <span data-ttu-id="003e4-153">This capability was added with [!INCLUDE[pn_crm_8_2_0_both](../../includes/pn-crm-8-2-0-both.md)].</span><span class="sxs-lookup"><span data-stu-id="003e4-153">This capability was added with [!INCLUDE[pn_crm_8_2_0_both](../../includes/pn-crm-8-2-0-both.md)].</span></span>

 <span data-ttu-id="003e4-154">You can compose your POST request so that data from the created record will be returned with a status of 201 (Created).</span><span class="sxs-lookup"><span data-stu-id="003e4-154">You can compose your POST request so that data from the created record will be returned with a status of 201 (Created).</span></span>  <span data-ttu-id="003e4-155">To get his result, you must use the `return=representation` preference in the request headers.</span><span class="sxs-lookup"><span data-stu-id="003e4-155">To get his result, you must use the `return=representation` preference in the request headers.</span></span>

 <span data-ttu-id="003e4-156">To control which properties are returned, append the `$select` query option to the URL to the entity set.</span><span class="sxs-lookup"><span data-stu-id="003e4-156">To control which properties are returned, append the `$select` query option to the URL to the entity set.</span></span>  <span data-ttu-id="003e4-157">The `$expand` query option will be ignored if used.</span><span class="sxs-lookup"><span data-stu-id="003e4-157">The `$expand` query option will be ignored if used.</span></span>

 <span data-ttu-id="003e4-158">When an entity is created in this way the `OData-EntityId` header containing the URI to the created record is not returned.</span><span class="sxs-lookup"><span data-stu-id="003e4-158">When an entity is created in this way the `OData-EntityId` header containing the URI to the created record is not returned.</span></span>

 <span data-ttu-id="003e4-159">This example creates a new account entity and returns the requested data in the response.</span><span class="sxs-lookup"><span data-stu-id="003e4-159">This example creates a new account entity and returns the requested data in the response.</span></span>

<span data-ttu-id="003e4-160">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="003e4-160">**Request**</span></span>

 ```http

POST [Organization URI]/api/data/v9.0/accounts?$select=name,creditonhold,address1_latitude,description,revenue,accountcategorycode,createdon HTTP/1.1
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json
Content-Type: application/json; charset=utf-8
Prefer: return=representation

{
    "name": "Sample Account",
    "creditonhold": false,
    "address1_latitude": 47.639583,
    "description": "This is the description of the sample account",
    "revenue": 5000000,
    "accountcategorycode": 1
}
```

<span data-ttu-id="003e4-161">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="003e4-161">**Response**</span></span>

```http

HTTP/1.1 201 Created
Content-Type: application/json; odata.metadata=minimal
Preference-Applied: return=representation
OData-Version: 4.0

{
    "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#accounts/$entity",
    "@odata.etag": "W/\"536530\"",
    "accountid": "d6f193fc-ce85-e611-80d8-00155d2a68de",
    "accountcategorycode": 1,
    "description": "This is the description of the sample account",
    "address1_latitude": 47.63958,
    "creditonhold": false,
    "name": "Sample Account",
    "createdon": "2016-09-28T22:57:53Z",
    "revenue": 5000000.0000,
    "_transactioncurrencyid_value": "048dddaa-6f7f-e611-80d3-00155db5e0b6"
}
```

### <a name="see-also"></a><span data-ttu-id="003e4-162">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="003e4-162">See also</span></span>

 [<span data-ttu-id="003e4-163">Web API Basic Operations Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="003e4-163">Web API Basic Operations Sample (C#)</span></span>](web-api-basic-operations-sample-csharp.md)<br />
 [<span data-ttu-id="003e4-164">Web API Basic Operations Sample (Client-side JavaScript)</span><span class="sxs-lookup"><span data-stu-id="003e4-164">Web API Basic Operations Sample (Client-side JavaScript)</span></span>](web-api-basic-operations-sample-client-side-javascript.md)<br />
 <xref href="Microsoft.Dynamics.CRM.InitializeFrom?text=InitializeFrom Function" />  
 [<span data-ttu-id="003e4-165">Perform operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="003e4-165">Perform operations using the Web API</span></span>](perform-operations-web-api.md)<br />
 [<span data-ttu-id="003e4-166">Compose Http requests and handle errors</span><span class="sxs-lookup"><span data-stu-id="003e4-166">Compose Http requests and handle errors</span></span>](compose-http-requests-handle-errors.md)<br />
 [<span data-ttu-id="003e4-167">Query Data using the Web API</span><span class="sxs-lookup"><span data-stu-id="003e4-167">Query Data using the Web API</span></span>](query-data-web-api.md)<br />
 [<span data-ttu-id="003e4-168">Retrieve an entity using the Web API</span><span class="sxs-lookup"><span data-stu-id="003e4-168">Retrieve an entity using the Web API</span></span>](retrieve-entity-using-web-api.md)<br />
 [<span data-ttu-id="003e4-169">Cập nhật và xóa các thực thể bằng cách sử dụng Web API</span><span class="sxs-lookup"><span data-stu-id="003e4-169">Update and delete entities using the Web API</span></span>](update-delete-entities-using-web-api.md)<br />
 [<span data-ttu-id="003e4-170">Associate and disassociate entities using the Web API</span><span class="sxs-lookup"><span data-stu-id="003e4-170">Associate and disassociate entities using the Web API</span></span>](associate-disassociate-entities-using-web-api.md)<br />
 [<span data-ttu-id="003e4-171">Use Web API functions</span><span class="sxs-lookup"><span data-stu-id="003e4-171">Use Web API functions</span></span>](use-web-api-functions.md)<br />
 [<span data-ttu-id="003e4-172">Sử dụng hành động Web API</span><span class="sxs-lookup"><span data-stu-id="003e4-172">Use Web API actions</span></span>](use-web-api-actions.md)<br />
 [<span data-ttu-id="003e4-173">Execute batch operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="003e4-173">Execute batch operations using the Web API</span></span>](execute-batch-operations-using-web-api.md)<br />
 [<span data-ttu-id="003e4-174">Impersonate another user using the Web API</span><span class="sxs-lookup"><span data-stu-id="003e4-174">Impersonate another user using the Web API</span></span>](impersonate-another-user-web-api.md)<br />
 [<span data-ttu-id="003e4-175">Perform conditional operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="003e4-175">Perform conditional operations using the Web API</span></span>](perform-conditional-operations-using-web-api.md)<br />
