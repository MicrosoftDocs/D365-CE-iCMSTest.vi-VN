---
title: Use Postman to perform operations with Web API(Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Learn how to compose and send Web API requests using Postman.
ms.custom: ''
ms.date: 07/23/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: AB50128B-D8E3-47A3-A0F8-9594EF6B7022
caps.latest.revision: 7
author: SushantSikka
ms.author: susikka
manager: sakudes
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7845ec64b51e19da24062535ba8de14fc71715fb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388674"
---
# <a name="use-postman-to-perform-operations-with-web-api"></a><span data-ttu-id="74ddb-103">Use Postman to perform operations with Web API</span><span class="sxs-lookup"><span data-stu-id="74ddb-103">Use Postman to perform operations with Web API</span></span>

<span data-ttu-id="74ddb-104">Use Postman to compose and send Web API requests and view responses.</span><span class="sxs-lookup"><span data-stu-id="74ddb-104">Use Postman to compose and send Web API requests and view responses.</span></span> <span data-ttu-id="74ddb-105">This topic describes how to create Web API requests that perform CRUD operations and use functions and actions using Postman.</span><span class="sxs-lookup"><span data-stu-id="74ddb-105">This topic describes how to create Web API requests that perform CRUD operations and use functions and actions using Postman.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74ddb-106">You will need to have an environment created using the steps described in   [Setup a Postman environment](setup-postman-environment.md)</span><span class="sxs-lookup"><span data-stu-id="74ddb-106">You will need to have an environment created using the steps described in   [Setup a Postman environment](setup-postman-environment.md)</span></span>

<span data-ttu-id="74ddb-107">The environment created using the instructions in [Setup a Postman environment](setup-postman-environment.md), creates a `{{webapiurl}}`  Postman variable that provides the base URL for requests.</span><span class="sxs-lookup"><span data-stu-id="74ddb-107">The environment created using the instructions in [Setup a Postman environment](setup-postman-environment.md), creates a `{{webapiurl}}`  Postman variable that provides the base URL for requests.</span></span> <span data-ttu-id="74ddb-108">Append to this variable to define the URL for your requests.</span><span class="sxs-lookup"><span data-stu-id="74ddb-108">Append to this variable to define the URL for your requests.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74ddb-109">Use the correct instructions to create your environment depending on your deployment type.</span><span class="sxs-lookup"><span data-stu-id="74ddb-109">Use the correct instructions to create your environment depending on your deployment type.</span></span>
>
>    |<span data-ttu-id="74ddb-110">Trực tuyến</span><span class="sxs-lookup"><span data-stu-id="74ddb-110">Online</span></span>|<span data-ttu-id="74ddb-111">On-premises</span><span class="sxs-lookup"><span data-stu-id="74ddb-111">On-premises</span></span>|
>    |--|--|
>    |[<span data-ttu-id="74ddb-112">Connect with an Online environment</span><span class="sxs-lookup"><span data-stu-id="74ddb-112">Connect with an Online environment</span></span>](setup-postman-environment.md#bkmk_connectonline)|[<span data-ttu-id="74ddb-113">Connect with an On-premise environment</span><span class="sxs-lookup"><span data-stu-id="74ddb-113">Connect with an On-premise environment</span></span>](setup-postman-environment.md#bkmk_connectonpremise)|


<span data-ttu-id="74ddb-114">Depending on the type of operation you want to perform, you will use different HTTP methods and values.</span><span class="sxs-lookup"><span data-stu-id="74ddb-114">Depending on the type of operation you want to perform, you will use different HTTP methods and values.</span></span> <span data-ttu-id="74ddb-115">The following sections demonstrate common operations.</span><span class="sxs-lookup"><span data-stu-id="74ddb-115">The following sections demonstrate common operations.</span></span>

## <a name="retrieve-multiple-records"></a><span data-ttu-id="74ddb-116">Retrieve multiple records</span><span class="sxs-lookup"><span data-stu-id="74ddb-116">Retrieve multiple records</span></span>

<span data-ttu-id="74ddb-117">Use a `GET` request to retrieve a set of records.</span><span class="sxs-lookup"><span data-stu-id="74ddb-117">Use a `GET` request to retrieve a set of records.</span></span> <span data-ttu-id="74ddb-118">The following example will retrieve the first three account records.</span><span class="sxs-lookup"><span data-stu-id="74ddb-118">The following example will retrieve the first three account records.</span></span>

> [!NOTE]
> <span data-ttu-id="74ddb-119">Web API requests should include certain HTTP headers.</span><span class="sxs-lookup"><span data-stu-id="74ddb-119">Web API requests should include certain HTTP headers.</span></span> <span data-ttu-id="74ddb-120">Every request should include the Accept header value of `application/json`, even when no response body is expected.</span><span class="sxs-lookup"><span data-stu-id="74ddb-120">Every request should include the Accept header value of `application/json`, even when no response body is expected.</span></span> <span data-ttu-id="74ddb-121">The current OData version is `4.0`, so include header `OData-Version: 4.0`.</span><span class="sxs-lookup"><span data-stu-id="74ddb-121">The current OData version is `4.0`, so include header `OData-Version: 4.0`.</span></span> <span data-ttu-id="74ddb-122">Include the `OData-MaxVersion` header so that there is no ambiguity about version with new releases of OData.</span><span class="sxs-lookup"><span data-stu-id="74ddb-122">Include the `OData-MaxVersion` header so that there is no ambiguity about version with new releases of OData.</span></span> [!INCLUDE[](../../includes/proc-more-information.md)] <span data-ttu-id="74ddb-123">[HTTP headers](compose-http-requests-handle-errors.md#http-headers).</span><span class="sxs-lookup"><span data-stu-id="74ddb-123">[HTTP headers](compose-http-requests-handle-errors.md#http-headers).</span></span>

<span data-ttu-id="74ddb-124">**Ví dụ**</span><span class="sxs-lookup"><span data-stu-id="74ddb-124">**Example**</span></span>


<span data-ttu-id="74ddb-125">`GET` `{{webapiurl}}accounts?$select=name,accountnumber&$top=3`</span><span class="sxs-lookup"><span data-stu-id="74ddb-125">`GET` `{{webapiurl}}accounts?$select=name,accountnumber&$top=3`</span></span>

<span data-ttu-id="74ddb-126">![Retrieve multiple records using Postman](../media/postman-retrieve-multiple.png "Retrieve multiple records using Postman")</span><span class="sxs-lookup"><span data-stu-id="74ddb-126">![Retrieve multiple records using Postman](../media/postman-retrieve-multiple.png "Retrieve multiple records using Postman")</span></span>

<span data-ttu-id="74ddb-127">The body of the response will look like this:</span><span class="sxs-lookup"><span data-stu-id="74ddb-127">The body of the response will look like this:</span></span>

```json
{
    "@odata.context": "https://yourorg.crm.dynamics.com/api/data/v9.0/$metadata#accounts(name,accountnumber)",
    "value": [
        {
            "@odata.etag": "W/\"2291741\"",
            "name": "Contoso Ltd",
            "accountnumber": null,
            "accountid": "9c706dc8-d2f5-e711-a956-000d3a328903"
        },
        {
            "@odata.etag": "W/\"2291742\"",
            "name": "Fourth Coffee",
            "accountnumber": null,
            "accountid": "a2706dc8-d2f5-e711-a956-000d3a328903"
        },
        {
            "@odata.etag": "W/\"2291743\"",
            "name": "Contoso Ltd",
            "accountnumber": null,
            "accountid": "9c3216b8-3efb-e711-a957-000d3a328903"
        }
    ]
}
```

<span data-ttu-id="74ddb-128">More information: [Query data using the Web API](query-data-web-api.md).</span><span class="sxs-lookup"><span data-stu-id="74ddb-128">More information: [Query data using the Web API](query-data-web-api.md).</span></span>

## <a name="retrieve-a-particular-record"></a><span data-ttu-id="74ddb-129">Retrieve a particular record</span><span class="sxs-lookup"><span data-stu-id="74ddb-129">Retrieve a particular record</span></span>

<span data-ttu-id="74ddb-130">Use a `GET` request to retrieve a record.</span><span class="sxs-lookup"><span data-stu-id="74ddb-130">Use a `GET` request to retrieve a record.</span></span> <span data-ttu-id="74ddb-131">The following example will retrieve two properties from a specific account and expand information about the related primary contact to include their full name.</span><span class="sxs-lookup"><span data-stu-id="74ddb-131">The following example will retrieve two properties from a specific account and expand information about the related primary contact to include their full name.</span></span>


<span data-ttu-id="74ddb-132">`GET` `{{webapiurl}}accounts(`*&lt;accountid&gt;*`)?$select=name,accountnumber&$expand=primarycontactid($select=fullname)`</span><span class="sxs-lookup"><span data-stu-id="74ddb-132">`GET` `{{webapiurl}}accounts(`*&lt;accountid&gt;*`)?$select=name,accountnumber&$expand=primarycontactid($select=fullname)`</span></span>

<span data-ttu-id="74ddb-133">![Retrieve a record using Postman](../media/postman-retrieve-record.png "Retrieve a record using Postman")</span><span class="sxs-lookup"><span data-stu-id="74ddb-133">![Retrieve a record using Postman](../media/postman-retrieve-record.png "Retrieve a record using Postman")</span></span>

<span data-ttu-id="74ddb-134">The body of the response will look like this:</span><span class="sxs-lookup"><span data-stu-id="74ddb-134">The body of the response will look like this:</span></span>

```json
{
    "@odata.context": "https://yourorg.crm.dynamics.com/api/data/v9.0/$metadata#accounts(name,accountnumber,primarycontactid(fullname))/$entity",
    "@odata.etag": "W/\"2291742\"",
    "name": "Fourth Coffee",
    "accountnumber": null,
    "accountid": "a2706dc8-d2f5-e711-a956-000d3a328903",
    "primarycontactid": {
        "@odata.etag": "W/\"1697263\"",
        "fullname": "Susie Curtis",
        "contactid": "a3706dc8-d2f5-e711-a956-000d3a328903"
    }
}
```
<span data-ttu-id="74ddb-135">More information: [Retrieve an entity using the Web API](retrieve-entity-using-web-api.md).</span><span class="sxs-lookup"><span data-stu-id="74ddb-135">More information: [Retrieve an entity using the Web API](retrieve-entity-using-web-api.md).</span></span>

## <a name="create-a-record"></a><span data-ttu-id="74ddb-136">Tạo bản ghi</span><span class="sxs-lookup"><span data-stu-id="74ddb-136">Create a record</span></span>

<span data-ttu-id="74ddb-137">Use a `POST` request to send data to create a record.</span><span class="sxs-lookup"><span data-stu-id="74ddb-137">Use a `POST` request to send data to create a record.</span></span> <span data-ttu-id="74ddb-138">Set the URL to the entity set name for an entity, in this case, the account entity, and set the headers as shown below.</span><span class="sxs-lookup"><span data-stu-id="74ddb-138">Set the URL to the entity set name for an entity, in this case, the account entity, and set the headers as shown below.</span></span>

<span data-ttu-id="74ddb-139">`POST` `{{webapiurl}}accounts`</span><span class="sxs-lookup"><span data-stu-id="74ddb-139">`POST` `{{webapiurl}}accounts`</span></span>

<span data-ttu-id="74ddb-140">![Create a new record using Web API](../media/postman-create-records.png "Create a new record using Web API")</span><span class="sxs-lookup"><span data-stu-id="74ddb-140">![Create a new record using Web API](../media/postman-create-records.png "Create a new record using Web API")</span></span>

<span data-ttu-id="74ddb-141">Set the Body of the request with information about the account to create.</span><span class="sxs-lookup"><span data-stu-id="74ddb-141">Set the Body of the request with information about the account to create.</span></span>

<span data-ttu-id="74ddb-142">![Body of the request to create a record using Web API](../media/postman-create-record-body.png "Body of the request to create a record using Web API")</span><span class="sxs-lookup"><span data-stu-id="74ddb-142">![Body of the request to create a record using Web API](../media/postman-create-record-body.png "Body of the request to create a record using Web API")</span></span>

<span data-ttu-id="74ddb-143">When you send this request, the body will be empty, but the ID of the created account will be in the **OData-EntityId** header value.</span><span class="sxs-lookup"><span data-stu-id="74ddb-143">When you send this request, the body will be empty, but the ID of the created account will be in the **OData-EntityId** header value.</span></span>

<span data-ttu-id="74ddb-144">More information: [Create an entity using the Web API](create-entity-web-api.md).</span><span class="sxs-lookup"><span data-stu-id="74ddb-144">More information: [Create an entity using the Web API](create-entity-web-api.md).</span></span>

## <a name="update-a-record"></a><span data-ttu-id="74ddb-145">Update a record</span><span class="sxs-lookup"><span data-stu-id="74ddb-145">Update a record</span></span>

<span data-ttu-id="74ddb-146">Use `PATCH` method to update an entity record, as shown in the example below.</span><span class="sxs-lookup"><span data-stu-id="74ddb-146">Use `PATCH` method to update an entity record, as shown in the example below.</span></span>

<span data-ttu-id="74ddb-147">`PATCH` `{{webapiurl}}accounts(`*&lt;accountid&gt;*`)`</span><span class="sxs-lookup"><span data-stu-id="74ddb-147">`PATCH` `{{webapiurl}}accounts(`*&lt;accountid&gt;*`)`</span></span>

<span data-ttu-id="74ddb-148">![Update a record using Web API](../media/postman-update-record.png "Update a record using Web API")</span><span class="sxs-lookup"><span data-stu-id="74ddb-148">![Update a record using Web API](../media/postman-update-record.png "Update a record using Web API")</span></span>

<span data-ttu-id="74ddb-149">When you send this request, the response body will be empty, but the ID of the updated account will be in the **OData-EntityId** header value.</span><span class="sxs-lookup"><span data-stu-id="74ddb-149">When you send this request, the response body will be empty, but the ID of the updated account will be in the **OData-EntityId** header value.</span></span>

<span data-ttu-id="74ddb-150">More information: [Update and delete entities using the Web API](update-delete-entities-using-web-api.md).</span><span class="sxs-lookup"><span data-stu-id="74ddb-150">More information: [Update and delete entities using the Web API](update-delete-entities-using-web-api.md).</span></span>

## <a name="delete-a-record"></a><span data-ttu-id="74ddb-151">Delete a record</span><span class="sxs-lookup"><span data-stu-id="74ddb-151">Delete a record</span></span>

<span data-ttu-id="74ddb-152">Use `DELETE` method to delete an existing record.</span><span class="sxs-lookup"><span data-stu-id="74ddb-152">Use `DELETE` method to delete an existing record.</span></span>

<span data-ttu-id="74ddb-153">`DELETE` `{{webapiurl}}accounts(`*&lt;accountid&gt;*`)`</span><span class="sxs-lookup"><span data-stu-id="74ddb-153">`DELETE` `{{webapiurl}}accounts(`*&lt;accountid&gt;*`)`</span></span>

<span data-ttu-id="74ddb-154">![Delete a record using Web API](../media/postman-delete-record.png "Delete a record using Web API")</span><span class="sxs-lookup"><span data-stu-id="74ddb-154">![Delete a record using Web API](../media/postman-delete-record.png "Delete a record using Web API")</span></span>

<span data-ttu-id="74ddb-155">When you send this request, the account record with the given `accountid` gets deleted.</span><span class="sxs-lookup"><span data-stu-id="74ddb-155">When you send this request, the account record with the given `accountid` gets deleted.</span></span>

<span data-ttu-id="74ddb-156">More information: [Update and delete entities using the Web API](update-delete-entities-using-web-api.md).</span><span class="sxs-lookup"><span data-stu-id="74ddb-156">More information: [Update and delete entities using the Web API](update-delete-entities-using-web-api.md).</span></span>

## <a name="use-a-function"></a><span data-ttu-id="74ddb-157">Use a function</span><span class="sxs-lookup"><span data-stu-id="74ddb-157">Use a function</span></span>

<span data-ttu-id="74ddb-158">Use a `GET` request with functions listed in [Web API Function Reference](https://docs.microsoft.com/dynamics365/customer-engagement/web-api/functions?view=dynamics-ce-odata-9) to perform re-usable operations with the Web API.</span><span class="sxs-lookup"><span data-stu-id="74ddb-158">Use a `GET` request with functions listed in [Web API Function Reference](https://docs.microsoft.com/dynamics365/customer-engagement/web-api/functions?view=dynamics-ce-odata-9) to perform re-usable operations with the Web API.</span></span> <span data-ttu-id="74ddb-159">The below example shows how to send a Web API request that uses <xref href="Microsoft.Dynamics.CRM.RetrieveDuplicates?text=RetrieveDuplicates function" /> to detect and retrieve duplicates of a specified record.</span><span class="sxs-lookup"><span data-stu-id="74ddb-159">The below example shows how to send a Web API request that uses <xref href="Microsoft.Dynamics.CRM.RetrieveDuplicates?text=RetrieveDuplicates function" /> to detect and retrieve duplicates of a specified record.</span></span>

|||
|----|----|
|`GET`|<span data-ttu-id="74ddb-160">`{{webapiurl}}RetrieveDuplicates(BusinessEntity=@p1,MatchingEntityName=@p2,PagingInfo=@p3)?@p1={'@odata.type':'Microsoft.Dynamics.CRM.account','accountid':'`*&lt;accountid&gt;*`'}&@p2='account'&@p3={'PageNumber':1,'Count':50}`</span><span class="sxs-lookup"><span data-stu-id="74ddb-160">`{{webapiurl}}RetrieveDuplicates(BusinessEntity=@p1,MatchingEntityName=@p2,PagingInfo=@p3)?@p1={'@odata.type':'Microsoft.Dynamics.CRM.account','accountid':'`*&lt;accountid&gt;*`'}&@p2='account'&@p3={'PageNumber':1,'Count':50}`</span></span>|

<span data-ttu-id="74ddb-161">![Create a Web API request that uses functions](../media/postman-use-function.png "Create a Web API request that uses functions")</span><span class="sxs-lookup"><span data-stu-id="74ddb-161">![Create a Web API request that uses functions](../media/postman-use-function.png "Create a Web API request that uses functions")</span></span>

<span data-ttu-id="74ddb-162">Functions return either a collection or a complex type.</span><span class="sxs-lookup"><span data-stu-id="74ddb-162">Functions return either a collection or a complex type.</span></span> <span data-ttu-id="74ddb-163">The response from the above <xref href="Microsoft.Dynamics.CRM.RetrieveDuplicates?text=RetrieveDuplicates function" /> should look like the following.</span><span class="sxs-lookup"><span data-stu-id="74ddb-163">The response from the above <xref href="Microsoft.Dynamics.CRM.RetrieveDuplicates?text=RetrieveDuplicates function" /> should look like the following.</span></span>

```json
{
        {
    "@odata.context": "https://yourorgname.crm.dynamics.com/api/data/v9.0/$metadata#accounts",
    "value": [
        <Omitted for brevity: JSON data for any matching accounts including all properties>
    ]
}
}
```

<span data-ttu-id="74ddb-164">More information: [Use Web API functions](use-web-api-functions.md).</span><span class="sxs-lookup"><span data-stu-id="74ddb-164">More information: [Use Web API functions](use-web-api-functions.md).</span></span>

## <a name="use-an-action"></a><span data-ttu-id="74ddb-165">Use an action</span><span class="sxs-lookup"><span data-stu-id="74ddb-165">Use an action</span></span>

<span data-ttu-id="74ddb-166">Use a `POST` request with actions listed in [Web API Action Reference](https://docs.microsoft.com/dynamics365/customer-engagement/web-api/actions?view=dynamics-ce-odata-9) to perform operations that have side-effects.</span><span class="sxs-lookup"><span data-stu-id="74ddb-166">Use a `POST` request with actions listed in [Web API Action Reference](https://docs.microsoft.com/dynamics365/customer-engagement/web-api/actions?view=dynamics-ce-odata-9) to perform operations that have side-effects.</span></span>

<span data-ttu-id="74ddb-167">The below example shows how to use <xref href="Microsoft.Dynamics.CRM.BulkDetectDuplicates?text=BulkDetectDuplicates action" />.</span><span class="sxs-lookup"><span data-stu-id="74ddb-167">The below example shows how to use <xref href="Microsoft.Dynamics.CRM.BulkDetectDuplicates?text=BulkDetectDuplicates action" />.</span></span>

<span data-ttu-id="74ddb-168">`POST` `{{webapiurl}}BulkDetectDuplicates`</span><span class="sxs-lookup"><span data-stu-id="74ddb-168">`POST` `{{webapiurl}}BulkDetectDuplicates`</span></span>

<span data-ttu-id="74ddb-169">![Create a Web API request that uses actions](../media/postman-use-action.png "Create a Web API request that uses actions")</span><span class="sxs-lookup"><span data-stu-id="74ddb-169">![Create a Web API request that uses actions](../media/postman-use-action.png "Create a Web API request that uses actions")</span></span>

<span data-ttu-id="74ddb-170">The above request submits an asynchronous duplicate detection job that runs in the background.</span><span class="sxs-lookup"><span data-stu-id="74ddb-170">The above request submits an asynchronous duplicate detection job that runs in the background.</span></span> <span data-ttu-id="74ddb-171">The duplicates are detected according to the published duplicate rules for the entity type.</span><span class="sxs-lookup"><span data-stu-id="74ddb-171">The duplicates are detected according to the published duplicate rules for the entity type.</span></span> <span data-ttu-id="74ddb-172"><xref href="Microsoft.Dynamics.CRM.BulkDetectDuplicatesResponse?text=BulkDetectDuplicatesResponse ComplexType" /> is returned as a response from <xref href="Microsoft.Dynamics.CRM.BulkDetectDuplicates?text=BulkDetectDuplicates action" />.</span><span class="sxs-lookup"><span data-stu-id="74ddb-172"><xref href="Microsoft.Dynamics.CRM.BulkDetectDuplicatesResponse?text=BulkDetectDuplicatesResponse ComplexType" /> is returned as a response from <xref href="Microsoft.Dynamics.CRM.BulkDetectDuplicates?text=BulkDetectDuplicates action" />.</span></span> <span data-ttu-id="74ddb-173">The response includes `JobId` property which contains the GUID of the asynchronous duplicate detection job that detects and logs duplicate records.</span><span class="sxs-lookup"><span data-stu-id="74ddb-173">The response includes `JobId` property which contains the GUID of the asynchronous duplicate detection job that detects and logs duplicate records.</span></span>

<span data-ttu-id="74ddb-174">More information: [Use Web API actions](use-web-api-actions.md).</span><span class="sxs-lookup"><span data-stu-id="74ddb-174">More information: [Use Web API actions](use-web-api-actions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="74ddb-175">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="74ddb-175">See Also</span></span>

[<span data-ttu-id="74ddb-176">Use Postman with Web API</span><span class="sxs-lookup"><span data-stu-id="74ddb-176">Use Postman with Web API</span></span>](use-postman-web-api.md)<br>
[<span data-ttu-id="74ddb-177">Perform operations with Web API</span><span class="sxs-lookup"><span data-stu-id="74ddb-177">Perform operations with Web API</span></span>](perform-operations-web-api.md)
