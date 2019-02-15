---
title: Manage duplicate detection for create and update operations using the Web API | MicrosoftDocs
description: Read how to detect duplicates using MSCRM.SuppressDuplicateDetection header and Dynamics 365 for Customer Engagement Web API
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: AE107774-4545-44B4-94C8-A0271EFA7876
caps.latest.revision: 11
author: SushantSikka
ms.author: susikka
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3cb54e86f0a140bce3373284bd8ea575a8542a21
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385770"
---
# <a name="manage-duplicate-detection-for-create-and-update-operations-using-the-web-api"></a><span data-ttu-id="3d44d-103">Manage duplicate detection for create and update operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="3d44d-103">Manage duplicate detection for create and update operations using the Web API</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3d44d-104">Dynamics 365 for Customer Engagement Web API allows you to detect duplicate records of an existing record in order to maintain integrity of data.</span><span class="sxs-lookup"><span data-stu-id="3d44d-104">Dynamics 365 for Customer Engagement Web API allows you to detect duplicate records of an existing record in order to maintain integrity of data.</span></span> 

## <a name="detect-duplicate-during-create-operation"></a><span data-ttu-id="3d44d-105">Detect duplicate during Create operation</span><span class="sxs-lookup"><span data-stu-id="3d44d-105">Detect duplicate during Create operation</span></span>

<span data-ttu-id="3d44d-106">Use `MSCRM.SuppressDuplicateDetection` header during `POST` request, to detect creation of a duplicate record of an existing record.</span><span class="sxs-lookup"><span data-stu-id="3d44d-106">Use `MSCRM.SuppressDuplicateDetection` header during `POST` request, to detect creation of a duplicate record of an existing record.</span></span> <span data-ttu-id="3d44d-107">The value assigned to `MSCRM.SuppressDuplicateDetection` header determines whether the Create or Update operation can be completed:</span><span class="sxs-lookup"><span data-stu-id="3d44d-107">The value assigned to `MSCRM.SuppressDuplicateDetection` header determines whether the Create or Update operation can be completed:</span></span>

- <span data-ttu-id="3d44d-108">`true` – Create or update the record, if a duplicate is found.</span><span class="sxs-lookup"><span data-stu-id="3d44d-108">`true` – Create or update the record, if a duplicate is found.</span></span>
- <span data-ttu-id="3d44d-109">`false` – Do not create or update the record, if a duplicate is found.</span><span class="sxs-lookup"><span data-stu-id="3d44d-109">`false` – Do not create or update the record, if a duplicate is found.</span></span>

> [!NOTE]
> <span data-ttu-id="3d44d-110">Passing of the `CalculateMatchCodeSynchronously` optional parameter is not required.</span><span class="sxs-lookup"><span data-stu-id="3d44d-110">Passing of the `CalculateMatchCodeSynchronously` optional parameter is not required.</span></span> <span data-ttu-id="3d44d-111">The match codes used to detect duplicates are calculated synchronously regardless of the value passed in this parameter.</span><span class="sxs-lookup"><span data-stu-id="3d44d-111">The match codes used to detect duplicates are calculated synchronously regardless of the value passed in this parameter.</span></span>

<span data-ttu-id="3d44d-112">Use preference header `MSCRM.SuppressDuplicateDetection` and set its value to `false` in the Web API request.</span><span class="sxs-lookup"><span data-stu-id="3d44d-112">Use preference header `MSCRM.SuppressDuplicateDetection` and set its value to `false` in the Web API request.</span></span>

> [!NOTE]
>  <span data-ttu-id="3d44d-113">Make sure there are appropriate duplicate detection rules in place.</span><span class="sxs-lookup"><span data-stu-id="3d44d-113">Make sure there are appropriate duplicate detection rules in place.</span></span> <span data-ttu-id="3d44d-114">Dynamics 365 for Customer Engagement apps includes default duplicate detection rules for accounts, contacts, and leads, but not for other types of records.</span><span class="sxs-lookup"><span data-stu-id="3d44d-114">Dynamics 365 for Customer Engagement apps includes default duplicate detection rules for accounts, contacts, and leads, but not for other types of records.</span></span> <span data-ttu-id="3d44d-115">Nếu bạn muốn hệ thống phát hiện bản ghi trùng lặp cho các loại bản ghi khác, bạn cần phải tạo quy tắc mới.</span><span class="sxs-lookup"><span data-stu-id="3d44d-115">If you want the system to detect duplicates for other record types, you’ll need to create a new rule.</span></span> <span data-ttu-id="3d44d-116">For information on how to create a duplicate detection rule, see [Duplicate detection rules](../../admin/set-up-duplicate-detection-rules-keep-data-clean.md).</span><span class="sxs-lookup"><span data-stu-id="3d44d-116">For information on how to create a duplicate detection rule, see [Duplicate detection rules](../../admin/set-up-duplicate-detection-rules-keep-data-clean.md).</span></span>

<a name="bkmk_create"></a>
###  <a name="example-detect-duplicates-during-create-operation-using-the-web-api"></a><span data-ttu-id="3d44d-117">Example: Detect duplicates during Create operation using the Web API</span><span class="sxs-lookup"><span data-stu-id="3d44d-117">Example: Detect duplicates during Create operation using the Web API</span></span>

<span data-ttu-id="3d44d-118">The following example shows how to detect duplicates during `Create` and `Update` operations using `MSCRM.SuppressDuplicateDetection` header in Web API request.</span><span class="sxs-lookup"><span data-stu-id="3d44d-118">The following example shows how to detect duplicates during `Create` and `Update` operations using `MSCRM.SuppressDuplicateDetection` header in Web API request.</span></span>

<span data-ttu-id="3d44d-119">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="3d44d-119">**Request**</span></span>
```http
POST [Organization URI]/org1/api/data/v9.0/leads HTTP/1.1
If-None-Match: null
OData-Version: 4.0
OData-MaxVersion: 4.0
Content-Type: application/json
Accept: application/json
MSCRM.SuppressDuplicateDetection: false

{
    "firstname":"Monte",
    "lastname":"Orton",
    "emailaddress1":"monteorton@example.com"
}
```
<span data-ttu-id="3d44d-120">If a lead record with the same `emailaddress1` attribute already exists, the following Response is returned.</span><span class="sxs-lookup"><span data-stu-id="3d44d-120">If a lead record with the same `emailaddress1` attribute already exists, the following Response is returned.</span></span>

<span data-ttu-id="3d44d-121">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="3d44d-121">**Response**</span></span>
```json
HTTP/1.1 500 Internal Server Error  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0

{
    "error": {
        "code": "0x80040333",
        "message": "A record was not created or updated because a duplicate of the current record already exists.",
        "innererror": {
            "message": "A record was not created or updated because a duplicate of the current record already exists.",
            "type": "Microsoft.Crm.CrmException",
            [ Stack Trace and internal exception details ommitted for brevity]
        }
    }
}
```
<span data-ttu-id="3d44d-122">Assign value `true` to `MSCRM.SuppressDuplicateDetection` header to allow creation of a duplicate record.</span><span class="sxs-lookup"><span data-stu-id="3d44d-122">Assign value `true` to `MSCRM.SuppressDuplicateDetection` header to allow creation of a duplicate record.</span></span>

<a name="bkmk_update"></a>

## <a name="detect-duplicates-during-update-operation"></a><span data-ttu-id="3d44d-123">Detect duplicates during Update operation</span><span class="sxs-lookup"><span data-stu-id="3d44d-123">Detect duplicates during Update operation</span></span>

<span data-ttu-id="3d44d-124">Set the value of `MSCRM.SuppressDuplicateDetection` header to `false` in your `PATCH` request to avoid creation of a duplicate record during Update operation.</span><span class="sxs-lookup"><span data-stu-id="3d44d-124">Set the value of `MSCRM.SuppressDuplicateDetection` header to `false` in your `PATCH` request to avoid creation of a duplicate record during Update operation.</span></span> <span data-ttu-id="3d44d-125">By default, duplicate detection is suppressed when you are updating records using the Web API.</span><span class="sxs-lookup"><span data-stu-id="3d44d-125">By default, duplicate detection is suppressed when you are updating records using the Web API.</span></span>

<span data-ttu-id="3d44d-126">The example shown below attempts to update an existing lead entity record which includes the same value of `emailaddress1` attribute as an existing record.</span><span class="sxs-lookup"><span data-stu-id="3d44d-126">The example shown below attempts to update an existing lead entity record which includes the same value of `emailaddress1` attribute as an existing record.</span></span>

<span data-ttu-id="3d44d-127">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="3d44d-127">**Request**</span></span>
```http
PATCH [Organization URI]/api/data/v9.0/leads(c4567bb6-47a3-e711-811b-e0071b6ac1b1) HTTP/1.1
If-None-Match: null
OData-Version: 4.0
OData-MaxVersion: 4.0
Content-Type: application/json
Accept: application/json
MSCRM.SuppressDuplicateDetection: false

{
    "firstname":"Monte",
    "lastname":"Orton",
    "emailaddress1":"monteorton@example.com"
}
```  

<span data-ttu-id="3d44d-128">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="3d44d-128">**Response**</span></span>
```json  
HTTP/1.1 500 Internal Server Error  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0

{
    "error": {
        "code": "0x80040333",
        "message": "A record was not created or updated because a duplicate of the current record already exists.",
        "innererror": {
            "message": "A record was not created or updated because a duplicate of the current record already exists.",
            "type": "Microsoft.Crm.CrmException",
            [ Stack Trace and internal exception details ommitted for brevity]
        }
    }
}
```

### <a name="see-also"></a><span data-ttu-id="3d44d-129">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3d44d-129">See Also</span></span> 
[<span data-ttu-id="3d44d-130">Run duplicate detection</span><span class="sxs-lookup"><span data-stu-id="3d44d-130">Run duplicate detection</span></span>](../run-duplicate-detection.md)  
[<span data-ttu-id="3d44d-131">Duplicate detection messages</span><span class="sxs-lookup"><span data-stu-id="3d44d-131">Duplicate detection messages</span></span>](../duplicate-detection-messages.md)
