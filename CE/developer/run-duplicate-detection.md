---
title: Run duplicate detection (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Execute duplicate detection for a specific record, entity type, or during create or update operations.
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 08699dd9-623a-4fee-8b2e-fba850cc2a58
caps.latest.revision: 39
author: susikka
ms.author: susikka
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d300013f493f594a96875d68c5b7f763fedb78a4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386229"
---
# <a name="run-duplicate-detection"></a><span data-ttu-id="c1903-103">Run duplicate detection</span><span class="sxs-lookup"><span data-stu-id="c1903-103">Run duplicate detection</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c1903-104">There are several ways to perform duplicate detection after you enable it and publish the duplicate detection rules.</span><span class="sxs-lookup"><span data-stu-id="c1903-104">There are several ways to perform duplicate detection after you enable it and publish the duplicate detection rules.</span></span>  

<a name="BKMK_RetDupwebapi"></a>

## <a name="retrieve-and-detect-duplicates-for-a-specified-record"></a><span data-ttu-id="c1903-105">Retrieve and detect duplicates for a specified record</span><span class="sxs-lookup"><span data-stu-id="c1903-105">Retrieve and detect duplicates for a specified record</span></span>

<span data-ttu-id="c1903-106">Detect and retrieve duplicates:</span><span class="sxs-lookup"><span data-stu-id="c1903-106">Detect and retrieve duplicates:</span></span>

- <span data-ttu-id="c1903-107">Before you create an entity</span><span class="sxs-lookup"><span data-stu-id="c1903-107">Before you create an entity</span></span>
- <span data-ttu-id="c1903-108">For an existing entity</span><span class="sxs-lookup"><span data-stu-id="c1903-108">For an existing entity</span></span>
- <span data-ttu-id="c1903-109">For other entities that correspond to duplicate rules across entities.</span><span class="sxs-lookup"><span data-stu-id="c1903-109">For other entities that correspond to duplicate rules across entities.</span></span> <span data-ttu-id="c1903-110">For example, any Lead entity which matches a contact entity.</span><span class="sxs-lookup"><span data-stu-id="c1903-110">For example, any Lead entity which matches a contact entity.</span></span>

### <a name="options"></a><span data-ttu-id="c1903-111">Tùy chọn:</span><span class="sxs-lookup"><span data-stu-id="c1903-111">Options:</span></span>

- <span data-ttu-id="c1903-112">Web API: <xref href="Microsoft.Dynamics.CRM.RetrieveDuplicates?text=RetrieveDuplicates Function" /></span><span class="sxs-lookup"><span data-stu-id="c1903-112">Web API: <xref href="Microsoft.Dynamics.CRM.RetrieveDuplicates?text=RetrieveDuplicates Function" /></span></span>
- <span data-ttu-id="c1903-113">Organization Service: <xref:Microsoft.Crm.Sdk.Messages.RetrieveDuplicatesRequest></span><span class="sxs-lookup"><span data-stu-id="c1903-113">Organization Service: <xref:Microsoft.Crm.Sdk.Messages.RetrieveDuplicatesRequest></span></span>


### <a name="example-detect-duplicates-for-a-specified-record-using-web-api"></a><span data-ttu-id="c1903-114">Example: Detect duplicates for a specified record using Web API</span><span class="sxs-lookup"><span data-stu-id="c1903-114">Example: Detect duplicates for a specified record using Web API</span></span>

<span data-ttu-id="c1903-115">The following example shows how to detect duplicates of a specified record using `RetrieveDuplicates` function.</span><span class="sxs-lookup"><span data-stu-id="c1903-115">The following example shows how to detect duplicates of a specified record using `RetrieveDuplicates` function.</span></span>

<span data-ttu-id="c1903-116">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="c1903-116">**Request**</span></span>
```http
GET [Organization URI]/api/data/v9.0/RetrieveDuplicates(BusinessEntity=@p1,MatchingEntityName=@p2,PagingInfo=@p3)?@p1={'@odata.type':'Microsoft.Dynamics.CRM.account','accountid':'0d1156d2-1598-e711-80e8-00155db64062'}&@p2='account'&@p3={'PageNumber':1,'Count':50} HTTP/1.1
If-None-Match: null
OData-Version: 4.0
OData-MaxVersion: 4.0
Content-Type: application/json
Accept: application/json
```
<span data-ttu-id="c1903-117">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="c1903-117">**Response**</span></span>
```json
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0

{
    "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#accounts",
    "value": [
        <Omitted for brevity: JSON data for any matching accounts including all properties>
    ]
}
```

<a name="BKMK_DupEntwebapi"></a>

## <a name="detect-duplicates-for-an-entity-type"></a><span data-ttu-id="c1903-118">Detect duplicates for an entity type</span><span class="sxs-lookup"><span data-stu-id="c1903-118">Detect duplicates for an entity type</span></span>

<span data-ttu-id="c1903-119">Submit an asynchronous duplicate detection job that runs in the background.</span><span class="sxs-lookup"><span data-stu-id="c1903-119">Submit an asynchronous duplicate detection job that runs in the background.</span></span> <span data-ttu-id="c1903-120">The duplicates are detected according to the published duplicate rules for the entity type.</span><span class="sxs-lookup"><span data-stu-id="c1903-120">The duplicates are detected according to the published duplicate rules for the entity type.</span></span> <span data-ttu-id="c1903-121">The detected duplicates are stored as `DuplicateRecord` records in Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="c1903-121">The detected duplicates are stored as `DuplicateRecord` records in Dynamics 365 for Customer Engagement apps.</span></span> 

<span data-ttu-id="c1903-122">A maximum of 5000 duplicates are returned by the duplicate detection job.</span><span class="sxs-lookup"><span data-stu-id="c1903-122">A maximum of 5000 duplicates are returned by the duplicate detection job.</span></span>

### <a name="options"></a><span data-ttu-id="c1903-123">Tùy chọn</span><span class="sxs-lookup"><span data-stu-id="c1903-123">Options</span></span>

- <span data-ttu-id="c1903-124">Web API: <xref href="Microsoft.Dynamics.CRM.BulkDetectDuplicates?text=BulkDetectDuplicates Action" /></span><span class="sxs-lookup"><span data-stu-id="c1903-124">Web API: <xref href="Microsoft.Dynamics.CRM.BulkDetectDuplicates?text=BulkDetectDuplicates Action" /></span></span>
- <span data-ttu-id="c1903-125">Organization Service: <xref:Microsoft.Crm.Sdk.Messages.BulkDetectDuplicatesRequest></span><span class="sxs-lookup"><span data-stu-id="c1903-125">Organization Service: <xref:Microsoft.Crm.Sdk.Messages.BulkDetectDuplicatesRequest></span></span>

### <a name="example-detect-duplicates-for-an-entity-type-using-the-web-api"></a><span data-ttu-id="c1903-126">Example: Detect duplicates for an entity type using the Web API</span><span class="sxs-lookup"><span data-stu-id="c1903-126">Example: Detect duplicates for an entity type using the Web API</span></span> 

<span data-ttu-id="c1903-127">The following example shows how to detect duplicates for an entity type by creating an asynchronous job using `BulkDetectDuplicates` action.</span><span class="sxs-lookup"><span data-stu-id="c1903-127">The following example shows how to detect duplicates for an entity type by creating an asynchronous job using `BulkDetectDuplicates` action.</span></span>

<span data-ttu-id="c1903-128">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="c1903-128">**Request**</span></span>
```http
POST [Organization URI]/api/data/v9.0/BulkDetectDuplicates HTTP/1.1
If-None-Match: null
OData-Version: 4.0
Content-Type: application/json
Accept: application/json
OData-MaxVersion: 4.0

{
    "Query": {
        "@odata.type": "#Microsoft.Dynamics.CRM.QueryExpression",
        "EntityName": "lead"
    },
    "JobName": "jobname1",
    "SendEmailNotification": false,
    "TemplateId": "07B94C1D-C85F-492F-B120-F0A743C540E6",
    "ToRecipients": [],
    "CCRecipients": [],
    "RecurrencePattern": "",
    "RecurrenceStartTime": "2015-07-15T05:30:00Z"
}  
```
<span data-ttu-id="c1903-129">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="c1903-129">**Response**</span></span>
```json
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0

{
    "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#Microsoft.Dynamics.CRM.BulkDetectDuplicatesResponse",
    "JobId": "efaff068-7598-e711-80e8-00155db64062"
}
```
<span data-ttu-id="c1903-130">The above request creates an asynchronous duplicate detection job whose JobID is returned in the response.</span><span class="sxs-lookup"><span data-stu-id="c1903-130">The above request creates an asynchronous duplicate detection job whose JobID is returned in the response.</span></span> <span data-ttu-id="c1903-131">The JobID returned from the above request can be used to fetch duplicate records in an entity type, as shown in the example below.</span><span class="sxs-lookup"><span data-stu-id="c1903-131">The JobID returned from the above request can be used to fetch duplicate records in an entity type, as shown in the example below.</span></span>

<span data-ttu-id="c1903-132">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="c1903-132">**Request**</span></span>
```http
GET [Organization URI]/api/data/v9.0/asyncoperations(efaff068-7598-e711-80e8-00155db64062)/AsyncOperation_DuplicateBaseRecord
If-None-Match: null
OData-Version: 4.0
OData-MaxVersion: 4.0
Content-Type: application/json
Accept: application/json
```
<span data-ttu-id="c1903-133">The FetchXML equivalent of the above request is shown below.</span><span class="sxs-lookup"><span data-stu-id="c1903-133">The FetchXML equivalent of the above request is shown below.</span></span>

```xml
<fetch>
    <entity name="duplicaterecord">
        <attribute name="owninguser" />
        <attribute name="ownerid" />
        <attribute name="baserecordid" />
        <attribute name="duplicateid" />
        <attribute name="owningbusinessunit" />
        <attribute name="createdon" />
        <attribute name="asyncoperationid" />
        <filter>
            <condition attribute="asyncoperationid" operator="eq" value="efaff068-7598-e711-80e8-00155db64062" />
        </filter>
    </entity>
</fetch>
```

<span data-ttu-id="c1903-134">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="c1903-134">**Response**</span></span>
```json
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0

{  
   "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#duplicaterecords",
   "value":[  
      {  
         "owninguser":"b3ac4144-6d9a-e711-811c-000d3a75ce72",
         "_ownerid_value":"b3ac4144-6d9a-e711-811c-000d3a75ce72",
         "_baserecordid_value":"3a6fc65b-3f9c-e711-811c-000d3a75ce72",
         "duplicateid":"489a879c-019b-4c28-8539-51ebc850d18f",
         "createdon":"2017-09-19T03:34:25Z",
         "owningbusinessunit":"20a44144-6d9a-e711-811c-000d3a75ce72",
         "_asyncoperationid_value":"efaff068-7598-e711-80e8-00155db64062",
         "_duplicateruleid_value":null,
         "_duplicaterecordid_value":null
      },
      {  
         "owninguser":"b3ac4144-6d9a-e711-811c-000d3a75ce72",
         "_ownerid_value":"b3ac4144-6d9a-e711-811c-000d3a75ce72",
         "_baserecordid_value":"406fc65b-3f9c-e711-811c-000d3a75ce72",
         "duplicateid":"0a4a7dea-1488-4e05-b5eb-c2925ad2925a",
         "createdon":"2017-09-19T03:34:25Z",
         "owningbusinessunit":"20a44144-6d9a-e711-811c-000d3a75ce72",
         "_asyncoperationid_value":"efaff068-7598-e711-80e8-00155db64062",
         "_duplicateruleid_value":null,
         "_duplicaterecordid_value":null
      }
   ]
}
```
<span data-ttu-id="c1903-135">The GUID of the base record is stored as `baserecordid` in the `DuplicateRecord` records.</span><span class="sxs-lookup"><span data-stu-id="c1903-135">The GUID of the base record is stored as `baserecordid` in the `DuplicateRecord` records.</span></span> <span data-ttu-id="c1903-136">`duplicateid`, in the above response is the unique identifier of the duplicate record.</span><span class="sxs-lookup"><span data-stu-id="c1903-136">`duplicateid`, in the above response is the unique identifier of the duplicate record.</span></span> <span data-ttu-id="c1903-137">`asyncoperationid` is the unique idenitifier of the system job that created that record.</span><span class="sxs-lookup"><span data-stu-id="c1903-137">`asyncoperationid` is the unique idenitifier of the system job that created that record.</span></span> <span data-ttu-id="c1903-138">And, `ownerid` is the unique identifier of the user or team that owns the duplicate record.</span><span class="sxs-lookup"><span data-stu-id="c1903-138">And, `ownerid` is the unique identifier of the user or team that owns the duplicate record.</span></span> <span data-ttu-id="c1903-139">See [DuplicateRecord Entity](entities/duplicaterecord.md) for more information.</span><span class="sxs-lookup"><span data-stu-id="c1903-139">See [DuplicateRecord Entity](entities/duplicaterecord.md) for more information.</span></span>

> [!NOTE]
>  <span data-ttu-id="c1903-140">Before creating and executing duplicate detection jobs, make sure that there are appropriate duplicate detection rules in place.</span><span class="sxs-lookup"><span data-stu-id="c1903-140">Before creating and executing duplicate detection jobs, make sure that there are appropriate duplicate detection rules in place.</span></span> <span data-ttu-id="c1903-141">Dynamics 365 for Customer Engagement includes default duplicate detection rules for accounts, contacts, and leads, but not for other types of records.</span><span class="sxs-lookup"><span data-stu-id="c1903-141">Dynamics 365 for Customer Engagement includes default duplicate detection rules for accounts, contacts, and leads, but not for other types of records.</span></span> <span data-ttu-id="c1903-142">If you want the system to detect duplicates for other record types, you’ll need to create a new rule.</span><span class="sxs-lookup"><span data-stu-id="c1903-142">If you want the system to detect duplicates for other record types, you’ll need to create a new rule.</span></span> <span data-ttu-id="c1903-143">For information on how to create a duplicate detection rule, see [Duplicate detection rules](../admin/set-up-duplicate-detection-rules-keep-data-clean.md).</span><span class="sxs-lookup"><span data-stu-id="c1903-143">For information on how to create a duplicate detection rule, see [Duplicate detection rules](../admin/set-up-duplicate-detection-rules-keep-data-clean.md).</span></span>

<a name="BKMK_CRwebapi"></a>

## <a name="detect-duplicates-during-create-and-update-operations"></a><span data-ttu-id="c1903-144">Detect duplicates during Create and Update operations</span><span class="sxs-lookup"><span data-stu-id="c1903-144">Detect duplicates during Create and Update operations</span></span>

<span data-ttu-id="c1903-145">By default, duplicate detection is suppressed when you are creating or updating a record using Web API.</span><span class="sxs-lookup"><span data-stu-id="c1903-145">By default, duplicate detection is suppressed when you are creating or updating a record using Web API.</span></span> <span data-ttu-id="c1903-146">Use `MSCRM.SuppressDuplicateDetection` header and set its value to `false` while creating or updating a record.</span><span class="sxs-lookup"><span data-stu-id="c1903-146">Use `MSCRM.SuppressDuplicateDetection` header and set its value to `false` while creating or updating a record.</span></span> <span data-ttu-id="c1903-147">Duplicate detection only applies when the organization has duplicate detection enabled, the entity is enabled for duplicate detection, and there are active duplicate detection rules being applied.</span><span class="sxs-lookup"><span data-stu-id="c1903-147">Duplicate detection only applies when the organization has duplicate detection enabled, the entity is enabled for duplicate detection, and there are active duplicate detection rules being applied.</span></span>

<span data-ttu-id="c1903-148">See more on how to detect duplicates during Create and Update operation in [Manage duplicate detection during Create and Update operation using Web API](duplicate-detection-create-update.md)</span><span class="sxs-lookup"><span data-stu-id="c1903-148">See more on how to detect duplicates during Create and Update operation in [Manage duplicate detection during Create and Update operation using Web API](duplicate-detection-create-update.md)</span></span>

<a name="BKMK_dupdetos"></a>
###  <a name="example-duplicate-detection-using-the-organization-service"></a><span data-ttu-id="c1903-149">Example: Duplicate detection using the Organization Service</span><span class="sxs-lookup"><span data-stu-id="c1903-149">Example: Duplicate detection using the Organization Service</span></span>

 <span data-ttu-id="c1903-150">The following example shows how to pass the duplicate detection option as a part of the `CreateRequest` and `UpdateRequest` messages:</span><span class="sxs-lookup"><span data-stu-id="c1903-150">The following example shows how to pass the duplicate detection option as a part of the `CreateRequest` and `UpdateRequest` messages:</span></span>  
  
 [!code-csharp[DuplicateDetection#InvokeDuplicateDetectionForCreateAndUpdate1](../snippets/csharp/CRMV8/duplicatedetection/cs/invokeduplicatedetectionforcreateandupdate1.cs#invokeduplicatedetectionforcreateandupdate1)]  
  
### <a name="see-also"></a><span data-ttu-id="c1903-151">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c1903-151">See also</span></span>  
 <span data-ttu-id="c1903-152">[Phát hiện trùng lặp](detect-duplicate-data-for-developers.md) </span><span class="sxs-lookup"><span data-stu-id="c1903-152">[Duplicate Detection](detect-duplicate-data-for-developers.md) </span></span>  
 <span data-ttu-id="c1903-153">[Enable and disable duplicate detection](enable-disable-duplicate-detection.md) </span><span class="sxs-lookup"><span data-stu-id="c1903-153">[Enable and disable duplicate detection](enable-disable-duplicate-detection.md) </span></span>  
 <span data-ttu-id="c1903-154">[Use Messages (Request and Response Classes) with the Execute Method](org-service/use-messages-request-response-classes-execute-method.md) </span><span class="sxs-lookup"><span data-stu-id="c1903-154">[Use Messages (Request and Response Classes) with the Execute Method](org-service/use-messages-request-response-classes-execute-method.md) </span></span>  
 [<span data-ttu-id="c1903-155">Duplicate Detection Messages</span><span class="sxs-lookup"><span data-stu-id="c1903-155">Duplicate Detection Messages</span></span>](duplicate-detection-messages.md)
