---
title: updateRecord (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: ''
keywords: ''
ms.date: 12/18/2017
ms.service:
- crm-online
ms.topic: reference
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: f5d4c8a9-4188-472a-83bf-b986dd135754
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fe9232eda362fffdd53c44eca008fee589bfdbaf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388778"
---
# <a name="updaterecord-client-api-reference"></a><span data-ttu-id="b859c-102">updateRecord (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="b859c-102">updateRecord (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/updateRecord-description.md](./includes/updateRecord-description.md)] 

## <a name="syntax"></a><span data-ttu-id="b859c-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="b859c-103">Syntax</span></span>

`Xrm.WebApi.updateRecord(entityLogicalName, id, data).then(successCallback, errorCallback);`

## <a name="parameters"></a><span data-ttu-id="b859c-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="b859c-104">Parameters</span></span>

<table style="width:100%">
<tr>
<th><span data-ttu-id="b859c-105">Tên</span><span class="sxs-lookup"><span data-stu-id="b859c-105">Name</span></span></th>
<th><span data-ttu-id="b859c-106">Loại</span><span class="sxs-lookup"><span data-stu-id="b859c-106">Type</span></span></th>
<th><span data-ttu-id="b859c-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="b859c-107">Required</span></span></th>
<th><span data-ttu-id="b859c-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="b859c-108">Description</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="b859c-109">entityLogicalName</span><span class="sxs-lookup"><span data-stu-id="b859c-109">entityLogicalName</span></span></td>
<td><span data-ttu-id="b859c-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="b859c-110">String</span></span></td>
<td><span data-ttu-id="b859c-111">Có</span><span class="sxs-lookup"><span data-stu-id="b859c-111">Yes</span></span></td>
<td><span data-ttu-id="b859c-112">The entity logical name of the record you want to update.</span><span class="sxs-lookup"><span data-stu-id="b859c-112">The entity logical name of the record you want to update.</span></span> <span data-ttu-id="b859c-113">For example: &quot;account&quot;.</span><span class="sxs-lookup"><span data-stu-id="b859c-113">For example: &quot;account&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b859c-114">ID</span><span class="sxs-lookup"><span data-stu-id="b859c-114">id</span></span></td>
<td><span data-ttu-id="b859c-115">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="b859c-115">String</span></span></td>
<td><span data-ttu-id="b859c-116">Có</span><span class="sxs-lookup"><span data-stu-id="b859c-116">Yes</span></span></td>
<td><span data-ttu-id="b859c-117">GUID of the entity record you want to update.</span><span class="sxs-lookup"><span data-stu-id="b859c-117">GUID of the entity record you want to update.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b859c-118">dữ liệu</span><span class="sxs-lookup"><span data-stu-id="b859c-118">data</span></span></td>
<td><span data-ttu-id="b859c-119">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="b859c-119">Object</span></span></td>
<td><span data-ttu-id="b859c-120">Có</span><span class="sxs-lookup"><span data-stu-id="b859c-120">Yes</span></span></td>
<td><p><span data-ttu-id="b859c-121">A JSON object containing <code>key: value</code> pairs, where <code>key</code> is the property of the entity and</span><span class="sxs-lookup"><span data-stu-id="b859c-121">A JSON object containing <code>key: value</code> pairs, where <code>key</code> is the property of the entity and</span></span> <code>value</code> <span data-ttu-id="b859c-122">is the value of the property you want to update.</span><span class="sxs-lookup"><span data-stu-id="b859c-122">is the value of the property you want to update.</span></span></p>
<p><span data-ttu-id="b859c-123">See examples later in this topic to see how you can define the <code>data</code> object for various update scenarios.</span><span class="sxs-lookup"><span data-stu-id="b859c-123">See examples later in this topic to see how you can define the <code>data</code> object for various update scenarios.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b859c-124">successCallback</span><span class="sxs-lookup"><span data-stu-id="b859c-124">successCallback</span></span></td>
<td><span data-ttu-id="b859c-125">Hàm</span><span class="sxs-lookup"><span data-stu-id="b859c-125">Function</span></span></td>
<td><span data-ttu-id="b859c-126">Không</span><span class="sxs-lookup"><span data-stu-id="b859c-126">No</span></span></td>
<td><p><span data-ttu-id="b859c-127">A function to call when a record is updated.</span><span class="sxs-lookup"><span data-stu-id="b859c-127">A function to call when a record is updated.</span></span> <span data-ttu-id="b859c-128">An object with the following properties will be passed to identify the updated record:</span><span class="sxs-lookup"><span data-stu-id="b859c-128">An object with the following properties will be passed to identify the updated record:</span></span></p>
<ul>
<li><span data-ttu-id="b859c-129"><b>entityType</b>: String.</span><span class="sxs-lookup"><span data-stu-id="b859c-129"><b>entityType</b>: String.</span></span> <span data-ttu-id="b859c-130">The entity type of the updated record.</span><span class="sxs-lookup"><span data-stu-id="b859c-130">The entity type of the updated record.</span></span></li>
<li><span data-ttu-id="b859c-131"><b>id</b>: String.</span><span class="sxs-lookup"><span data-stu-id="b859c-131"><b>id</b>: String.</span></span> <span data-ttu-id="b859c-132">GUID of the updated record.</span><span class="sxs-lookup"><span data-stu-id="b859c-132">GUID of the updated record.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="b859c-133">errorCallback</span><span class="sxs-lookup"><span data-stu-id="b859c-133">errorCallback</span></span></td>
<td><span data-ttu-id="b859c-134">Hàm</span><span class="sxs-lookup"><span data-stu-id="b859c-134">Function</span></span></td>
<td><span data-ttu-id="b859c-135">Không</span><span class="sxs-lookup"><span data-stu-id="b859c-135">No</span></span></td>
<td><span data-ttu-id="b859c-136">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="b859c-136">A function to call when the operation fails.</span></span> <span data-ttu-id="b859c-137">An object with the following properties will be passed:</span><span class="sxs-lookup"><span data-stu-id="b859c-137">An object with the following properties will be passed:</span></span>
<ul>
<li><span data-ttu-id="b859c-138"><b>errorCode</b>: Number.</span><span class="sxs-lookup"><span data-stu-id="b859c-138"><b>errorCode</b>: Number.</span></span> <span data-ttu-id="b859c-139">The error code.</span><span class="sxs-lookup"><span data-stu-id="b859c-139">The error code.</span></span></li>
<li><span data-ttu-id="b859c-140"><b>message</b>: String.</span><span class="sxs-lookup"><span data-stu-id="b859c-140"><b>message</b>: String.</span></span> <span data-ttu-id="b859c-141">An error message describing the issue.</span><span class="sxs-lookup"><span data-stu-id="b859c-141">An error message describing the issue.</span></span></li>
</ul></td>
</tr>
</table>

## <a name="return-value"></a><span data-ttu-id="b859c-142">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="b859c-142">Return Value</span></span>

<span data-ttu-id="b859c-143">On success, returns a promise object containing the attributes specified earlier in the description of the **successCallback** parameter.</span><span class="sxs-lookup"><span data-stu-id="b859c-143">On success, returns a promise object containing the attributes specified earlier in the description of the **successCallback** parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="b859c-144">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="b859c-144">Examples</span></span>

<span data-ttu-id="b859c-145">These examples use some of the same request objects as demonstrated in [Update and delete entities using the Web API](../../../webapi/update-delete-entities-using-web-api.md) to define the data object for updating an entity record.</span><span class="sxs-lookup"><span data-stu-id="b859c-145">These examples use some of the same request objects as demonstrated in [Update and delete entities using the Web API](../../../webapi/update-delete-entities-using-web-api.md) to define the data object for updating an entity record.</span></span>

### <a name="basic-update"></a><span data-ttu-id="b859c-146">Basic update</span><span class="sxs-lookup"><span data-stu-id="b859c-146">Basic update</span></span> 

<span data-ttu-id="b859c-147">Updates an existing account record with record ID = 5531d753-95af-e711-a94e-000d3a11e605.</span><span class="sxs-lookup"><span data-stu-id="b859c-147">Updates an existing account record with record ID = 5531d753-95af-e711-a94e-000d3a11e605.</span></span>

```JavaScript
// define the data to update a record
var data =
    {
        "name": "Updated Sample Account ",
        "creditonhold": true,
        "address1_latitude": 47.639583,
        "description": "This is the updated description of the sample account",
        "revenue": 6000000,
        "accountcategorycode": 2
    }
// update the record
Xrm.WebApi.updateRecord("account", "5531d753-95af-e711-a94e-000d3a11e605", data).then(
    function success(result) {
        console.log("Account updated");
        // perform operations on record update
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```

### <a name="update-associations-to-the-related-entities"></a><span data-ttu-id="b859c-148">Update associations to the related entities</span><span class="sxs-lookup"><span data-stu-id="b859c-148">Update associations to the related entities</span></span>

<span data-ttu-id="b859c-149">To update association to the related entity records (lookups), set the value of single-valued navigation properties using the `@odata.bind` annotation to another record.</span><span class="sxs-lookup"><span data-stu-id="b859c-149">To update association to the related entity records (lookups), set the value of single-valued navigation properties using the `@odata.bind` annotation to another record.</span></span> <span data-ttu-id="b859c-150">However, for mobile clients in the offline mode, you cannot use the `@odata.bind` annotation, and instead have to pass a **lookup** object (**logicalname** and **id**) pointing to the target record.</span><span class="sxs-lookup"><span data-stu-id="b859c-150">However, for mobile clients in the offline mode, you cannot use the `@odata.bind` annotation, and instead have to pass a **lookup** object (**logicalname** and **id**) pointing to the target record.</span></span> <span data-ttu-id="b859c-151">Here are code examples for both the scenarios:</span><span class="sxs-lookup"><span data-stu-id="b859c-151">Here are code examples for both the scenarios:</span></span>

<span data-ttu-id="b859c-152">**For online scenario (connected to server)**</span><span class="sxs-lookup"><span data-stu-id="b859c-152">**For online scenario (connected to server)**</span></span>

<span data-ttu-id="b859c-153">The following example updates an account record to associate another contact record as the primary contact for the account:</span><span class="sxs-lookup"><span data-stu-id="b859c-153">The following example updates an account record to associate another contact record as the primary contact for the account:</span></span>

```JavaScript
// define the data to update a record
var data =
    {
        "primarycontactid@odata.bind": "/contacts(61a0e5b9-88df-e311-b8e5-6c3be5a8b200)"
    }
// update the record
Xrm.WebApi.updateRecord("account", "5531d753-95af-e711-a94e-000d3a11e605", data).then(
    function success(result) {
        console.log("Account updated");
        // perform operations on record update
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```

<span data-ttu-id="b859c-154">**For mobile offline scenario**</span><span class="sxs-lookup"><span data-stu-id="b859c-154">**For mobile offline scenario**</span></span>

<span data-ttu-id="b859c-155">Here is the updated sample code to update an account record to associate another contact record as the primary contact for the account from mobile clients when working in the offline mode:</span><span class="sxs-lookup"><span data-stu-id="b859c-155">Here is the updated sample code to update an account record to associate another contact record as the primary contact for the account from mobile clients when working in the offline mode:</span></span>

```JavaScript
// define the data to update a record
var data =
    {
        "primarycontactid":
        {
            "logicalname": "contact",
            "id": "61a0e5b9-88df-e311-b8e5-6c3be5a8b200"
        }
    }
// update the record
Xrm.WebApi.offline.updateRecord("account", "5531d753-95af-e711-a94e-000d3a11e605", data).then(
    function success(result) {
        console.log("Account updated");
        // perform operations on record update
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```
 
### <a name="related-topics"></a><span data-ttu-id="b859c-156">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="b859c-156">Related topics</span></span>

[<span data-ttu-id="b859c-157">Xrm.WebApi</span><span class="sxs-lookup"><span data-stu-id="b859c-157">Xrm.WebApi</span></span>](../xrm-webapi.md)
