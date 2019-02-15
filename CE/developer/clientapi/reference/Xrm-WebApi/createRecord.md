---
title: createRecord (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: ''
keywords: ''
ms.date: 12/18/2017
ms.service:
- crm-online
ms.topic: reference
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 848c277b-bd44-4388-852a-0f59a3a15538
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5b5e473b749233dbab9767ea1b8b37aa5d8b3963
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388432"
---
# <a name="createrecord-client-api-reference"></a><span data-ttu-id="7ed47-102">createRecord (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="7ed47-102">createRecord (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/createRecord-description.md](./includes/createRecord-description.md)] 

## <a name="syntax"></a><span data-ttu-id="7ed47-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="7ed47-103">Syntax</span></span>

`Xrm.WebApi.createRecord(entityLogicalName, data).then(successCallback, errorCallback);`

## <a name="parameters"></a><span data-ttu-id="7ed47-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="7ed47-104">Parameters</span></span>

<table style="width:100%">
<tr>
<th><span data-ttu-id="7ed47-105">Tên</span><span class="sxs-lookup"><span data-stu-id="7ed47-105">Name</span></span></th>
<th><span data-ttu-id="7ed47-106">Loại</span><span class="sxs-lookup"><span data-stu-id="7ed47-106">Type</span></span></th>
<th><span data-ttu-id="7ed47-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="7ed47-107">Required</span></span></th>
<th><span data-ttu-id="7ed47-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="7ed47-108">Description</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="7ed47-109">entityLogicalName</span><span class="sxs-lookup"><span data-stu-id="7ed47-109">entityLogicalName</span></span></td>
<td><span data-ttu-id="7ed47-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="7ed47-110">String</span></span></td>
<td><span data-ttu-id="7ed47-111">Có</span><span class="sxs-lookup"><span data-stu-id="7ed47-111">Yes</span></span></td>
<td><span data-ttu-id="7ed47-112">Logical name of the entity you want to create.</span><span class="sxs-lookup"><span data-stu-id="7ed47-112">Logical name of the entity you want to create.</span></span> <span data-ttu-id="7ed47-113">For example: &quot;account&quot;.</span><span class="sxs-lookup"><span data-stu-id="7ed47-113">For example: &quot;account&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ed47-114">dữ liệu</span><span class="sxs-lookup"><span data-stu-id="7ed47-114">data</span></span></td>
<td><span data-ttu-id="7ed47-115">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="7ed47-115">Object</span></span></td>
<td><span data-ttu-id="7ed47-116">Có</span><span class="sxs-lookup"><span data-stu-id="7ed47-116">Yes</span></span></td>
<td><p><span data-ttu-id="7ed47-117">A JSON object defining the attributes and values for the new entity record.</span><span class="sxs-lookup"><span data-stu-id="7ed47-117">A JSON object defining the attributes and values for the new entity record.</span></span></p>
<p><span data-ttu-id="7ed47-118">See examples later in this topic to see how you can define the <code>data</code> object for various create scenarios.</span><span class="sxs-lookup"><span data-stu-id="7ed47-118">See examples later in this topic to see how you can define the <code>data</code> object for various create scenarios.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7ed47-119">successCallback</span><span class="sxs-lookup"><span data-stu-id="7ed47-119">successCallback</span></span></td>
<td><span data-ttu-id="7ed47-120">Hàm</span><span class="sxs-lookup"><span data-stu-id="7ed47-120">Function</span></span></td>
<td><span data-ttu-id="7ed47-121">Không</span><span class="sxs-lookup"><span data-stu-id="7ed47-121">No</span></span></td>
<td><p><span data-ttu-id="7ed47-122">A function to call when a record is created.</span><span class="sxs-lookup"><span data-stu-id="7ed47-122">A function to call when a record is created.</span></span> <span data-ttu-id="7ed47-123">An object with the following properties will be passed to identify the new record:</span><span class="sxs-lookup"><span data-stu-id="7ed47-123">An object with the following properties will be passed to identify the new record:</span></span></p>
<ul>
<li><span data-ttu-id="7ed47-124"><b>entityType</b>: String.</span><span class="sxs-lookup"><span data-stu-id="7ed47-124"><b>entityType</b>: String.</span></span> <span data-ttu-id="7ed47-125">The entity logical name of the new record.</span><span class="sxs-lookup"><span data-stu-id="7ed47-125">The entity logical name of the new record.</span></span></li>
<li><span data-ttu-id="7ed47-126"><b>id</b>: String.</span><span class="sxs-lookup"><span data-stu-id="7ed47-126"><b>id</b>: String.</span></span> <span data-ttu-id="7ed47-127">GUID of the new record.</span><span class="sxs-lookup"><span data-stu-id="7ed47-127">GUID of the new record.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="7ed47-128">errorCallback</span><span class="sxs-lookup"><span data-stu-id="7ed47-128">errorCallback</span></span></td>
<td><span data-ttu-id="7ed47-129">Hàm</span><span class="sxs-lookup"><span data-stu-id="7ed47-129">Function</span></span></td>
<td><span data-ttu-id="7ed47-130">Không</span><span class="sxs-lookup"><span data-stu-id="7ed47-130">No</span></span></td>
<td><span data-ttu-id="7ed47-131">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="7ed47-131">A function to call when the operation fails.</span></span> <span data-ttu-id="7ed47-132">An object with the following properties will be passed:</span><span class="sxs-lookup"><span data-stu-id="7ed47-132">An object with the following properties will be passed:</span></span>
<ul>
<li><span data-ttu-id="7ed47-133"><b>errorCode</b>: Number.</span><span class="sxs-lookup"><span data-stu-id="7ed47-133"><b>errorCode</b>: Number.</span></span> <span data-ttu-id="7ed47-134">The error code.</span><span class="sxs-lookup"><span data-stu-id="7ed47-134">The error code.</span></span></li>
<li><span data-ttu-id="7ed47-135"><b>message</b>: String.</span><span class="sxs-lookup"><span data-stu-id="7ed47-135"><b>message</b>: String.</span></span> <span data-ttu-id="7ed47-136">An error message describing the issue.</span><span class="sxs-lookup"><span data-stu-id="7ed47-136">An error message describing the issue.</span></span></li>
</ul></td>
</tr>
</table>

## <a name="return-value"></a><span data-ttu-id="7ed47-137">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="7ed47-137">Return Value</span></span>

<span data-ttu-id="7ed47-138">On success, returns a promise object containing the attributes specified earlier in the description of the **successCallback** parameter.</span><span class="sxs-lookup"><span data-stu-id="7ed47-138">On success, returns a promise object containing the attributes specified earlier in the description of the **successCallback** parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="7ed47-139">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="7ed47-139">Examples</span></span>

<span data-ttu-id="7ed47-140">These examples use the same request objects as demonstrated in [Create an entity using the Web API](../../../webapi/create-entity-web-api.md) to define the data object for creating an entity record.</span><span class="sxs-lookup"><span data-stu-id="7ed47-140">These examples use the same request objects as demonstrated in [Create an entity using the Web API](../../../webapi/create-entity-web-api.md) to define the data object for creating an entity record.</span></span>

### <a name="basic-create"></a><span data-ttu-id="7ed47-141">Basic create</span><span class="sxs-lookup"><span data-stu-id="7ed47-141">Basic create</span></span> 

<span data-ttu-id="7ed47-142">Creates a sample account record.</span><span class="sxs-lookup"><span data-stu-id="7ed47-142">Creates a sample account record.</span></span>

```JavaScript
// define the data to create new account
var data =
    {
        "name": "Sample Account",
        "creditonhold": false,
        "address1_latitude": 47.639583,
        "description": "This is the description of the sample account",
        "revenue": 5000000,
        "accountcategorycode": 1
    }

// create account record
Xrm.WebApi.createRecord("account", data).then(
    function success(result) {
        console.log("Account created with ID: " + result.id);
        // perform operations on record creation
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```

### <a name="create-related-entity-records-along-with-the-primary-record"></a><span data-ttu-id="7ed47-143">Create related entity records along with the primary record</span><span class="sxs-lookup"><span data-stu-id="7ed47-143">Create related entity records along with the primary record</span></span>

 <span data-ttu-id="7ed47-144">You can create entities related to each other by defining them as navigation properties values.</span><span class="sxs-lookup"><span data-stu-id="7ed47-144">You can create entities related to each other by defining them as navigation properties values.</span></span> <span data-ttu-id="7ed47-145">This is known as *deep insert*.</span><span class="sxs-lookup"><span data-stu-id="7ed47-145">This is known as *deep insert*.</span></span> <span data-ttu-id="7ed47-146">In this example, we will create a sample account record along with the primary contact record and an associated opportunity record.</span><span class="sxs-lookup"><span data-stu-id="7ed47-146">In this example, we will create a sample account record along with the primary contact record and an associated opportunity record.</span></span>

```JavaScript
// define data to create primary and related entity records
var data =
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

// create account record
Xrm.WebApi.createRecord("account", data).then(
    function success(result) {
        console.log("Account created with ID: " + result.id);
        // perform operations on record creation
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```

### <a name="associate-entities-on-creating-new-records"></a><span data-ttu-id="7ed47-147">Associate entities on creating new records</span><span class="sxs-lookup"><span data-stu-id="7ed47-147">Associate entities on creating new records</span></span>

<span data-ttu-id="7ed47-148">To associate new entity records to existing entity records, set the value of single-valued navigation properties using the `@odata.bind` annotation.</span><span class="sxs-lookup"><span data-stu-id="7ed47-148">To associate new entity records to existing entity records, set the value of single-valued navigation properties using the `@odata.bind` annotation.</span></span> <span data-ttu-id="7ed47-149">However, for mobile clients in the offline mode, you cannot use the `@odata.bind` annotation, and instead have to pass a **lookup** object (**logicalname** and **id**) pointing to the target record.</span><span class="sxs-lookup"><span data-stu-id="7ed47-149">However, for mobile clients in the offline mode, you cannot use the `@odata.bind` annotation, and instead have to pass a **lookup** object (**logicalname** and **id**) pointing to the target record.</span></span> <span data-ttu-id="7ed47-150">Here are code examples for both the scenarios:</span><span class="sxs-lookup"><span data-stu-id="7ed47-150">Here are code examples for both the scenarios:</span></span> 


<span data-ttu-id="7ed47-151">**For online scenario (connected to server)**</span><span class="sxs-lookup"><span data-stu-id="7ed47-151">**For online scenario (connected to server)**</span></span>

<span data-ttu-id="7ed47-152">The following example creates an account record, and associates it to an existing contact record to set the latter as the primary contact for the new account record:</span><span class="sxs-lookup"><span data-stu-id="7ed47-152">The following example creates an account record, and associates it to an existing contact record to set the latter as the primary contact for the new account record:</span></span>

```JavaScript
var data =
    {
        "name": "Sample Account",
        "primarycontactid@odata.bind": "/contacts(465b158c-541c-e511-80d3-3863bb347ba8)"
    }

// create account record
Xrm.WebApi.createRecord("account", data).then(
    function success(result) {
        console.log("Account created with ID: " + result.id);
        // perform operations on record creation
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```

<span data-ttu-id="7ed47-153">**For mobile offline scenario**</span><span class="sxs-lookup"><span data-stu-id="7ed47-153">**For mobile offline scenario**</span></span>

<span data-ttu-id="7ed47-154">Here is the updated sample code to create an account record, and associate it to an existing contact record to set the latter as the primary contact for the new account record from mobile clients when working in the offline mode:</span><span class="sxs-lookup"><span data-stu-id="7ed47-154">Here is the updated sample code to create an account record, and associate it to an existing contact record to set the latter as the primary contact for the new account record from mobile clients when working in the offline mode:</span></span>

```JavaScript
var data =
    {
        "name": "Sample Account",
        "primarycontactid":
        {
            "logicalname": "contact",
            "id": "465b158c-541c-e511-80d3-3863bb347ba8"
        } 
    }

// create account record
Xrm.WebApi.offline.createRecord("account", data).then(
    function success(result) {
        console.log("Account created with ID: " + result.id);
        // perform operations on record creation
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
``` 
 
### <a name="related-topics"></a><span data-ttu-id="7ed47-155">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="7ed47-155">Related topics</span></span>

[<span data-ttu-id="7ed47-156">Create an entity using the Web API</span><span class="sxs-lookup"><span data-stu-id="7ed47-156">Create an entity using the Web API</span></span>](../../../webapi/create-entity-web-api.md)

[<span data-ttu-id="7ed47-157">Xrm.WebApi</span><span class="sxs-lookup"><span data-stu-id="7ed47-157">Xrm.WebApi</span></span>](../xrm-webapi.md)
