---
title: deleteRecord (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 848c277b-bd44-4388-852a-0f59a3a15538
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 228de69b76a568f16501ebf2a0508dafb1b7806e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388765"
---
# <a name="deleterecord-client-api-reference"></a><span data-ttu-id="69d1d-102">deleteRecord (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="69d1d-102">deleteRecord (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/deleteRecord-description.md](./includes/deleteRecord-description.md)] 

## <a name="syntax"></a><span data-ttu-id="69d1d-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="69d1d-103">Syntax</span></span>

`Xrm.WebApi.deleteRecord(entityLogicalName, id).then(successCallback, errorCallback);`

## <a name="parameters"></a><span data-ttu-id="69d1d-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="69d1d-104">Parameters</span></span>

<table style="width:100%">
<tr>
<th><span data-ttu-id="69d1d-105">Tên</span><span class="sxs-lookup"><span data-stu-id="69d1d-105">Name</span></span></th>
<th><span data-ttu-id="69d1d-106">Loại</span><span class="sxs-lookup"><span data-stu-id="69d1d-106">Type</span></span></th>
<th><span data-ttu-id="69d1d-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="69d1d-107">Required</span></span></th>
<th><span data-ttu-id="69d1d-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="69d1d-108">Description</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="69d1d-109">entityLogicalName</span><span class="sxs-lookup"><span data-stu-id="69d1d-109">entityLogicalName</span></span></td>
<td><span data-ttu-id="69d1d-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="69d1d-110">String</span></span></td>
<td><span data-ttu-id="69d1d-111">Có</span><span class="sxs-lookup"><span data-stu-id="69d1d-111">Yes</span></span></td>
<td><span data-ttu-id="69d1d-112">The entity logical name of the record you want to delete.</span><span class="sxs-lookup"><span data-stu-id="69d1d-112">The entity logical name of the record you want to delete.</span></span> <span data-ttu-id="69d1d-113">For example: &quot;account&quot;.</span><span class="sxs-lookup"><span data-stu-id="69d1d-113">For example: &quot;account&quot;.</span></span> </td>
</tr>
<tr>
<td><span data-ttu-id="69d1d-114">ID</span><span class="sxs-lookup"><span data-stu-id="69d1d-114">id</span></span></td>
<td><span data-ttu-id="69d1d-115">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="69d1d-115">String</span></span></td>
<td><span data-ttu-id="69d1d-116">Có</span><span class="sxs-lookup"><span data-stu-id="69d1d-116">Yes</span></span></td>
<td><span data-ttu-id="69d1d-117">GUID of the entity record you want to delete.</span><span class="sxs-lookup"><span data-stu-id="69d1d-117">GUID of the entity record you want to delete.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69d1d-118">successCallback</span><span class="sxs-lookup"><span data-stu-id="69d1d-118">successCallback</span></span></td>
<td><span data-ttu-id="69d1d-119">Hàm</span><span class="sxs-lookup"><span data-stu-id="69d1d-119">Function</span></span></td>
<td><span data-ttu-id="69d1d-120">Không</span><span class="sxs-lookup"><span data-stu-id="69d1d-120">No</span></span></td>
<td><p><span data-ttu-id="69d1d-121">A function to call when a record is deleted.</span><span class="sxs-lookup"><span data-stu-id="69d1d-121">A function to call when a record is deleted.</span></span> <span data-ttu-id="69d1d-122">An object with the following properties will be passed to identify the deleted record:</span><span class="sxs-lookup"><span data-stu-id="69d1d-122">An object with the following properties will be passed to identify the deleted record:</span></span></p>
<ul>
<li><span data-ttu-id="69d1d-123"><b>entityType</b>: String.</span><span class="sxs-lookup"><span data-stu-id="69d1d-123"><b>entityType</b>: String.</span></span> <span data-ttu-id="69d1d-124">The entity type of the record.</span><span class="sxs-lookup"><span data-stu-id="69d1d-124">The entity type of the record.</span></span></li>
<li><span data-ttu-id="69d1d-125"><b>id</b>: String.</span><span class="sxs-lookup"><span data-stu-id="69d1d-125"><b>id</b>: String.</span></span> <span data-ttu-id="69d1d-126">GUID of the record.</span><span class="sxs-lookup"><span data-stu-id="69d1d-126">GUID of the record.</span></span></li>
<li><span data-ttu-id="69d1d-127"><b>name</b>: String.</span><span class="sxs-lookup"><span data-stu-id="69d1d-127"><b>name</b>: String.</span></span> <span data-ttu-id="69d1d-128">Name of the record.</span><span class="sxs-lookup"><span data-stu-id="69d1d-128">Name of the record.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="69d1d-129">errorCallback</span><span class="sxs-lookup"><span data-stu-id="69d1d-129">errorCallback</span></span></td>
<td><span data-ttu-id="69d1d-130">Hàm</span><span class="sxs-lookup"><span data-stu-id="69d1d-130">Function</span></span></td>
<td><span data-ttu-id="69d1d-131">Không</span><span class="sxs-lookup"><span data-stu-id="69d1d-131">No</span></span></td>
<td><span data-ttu-id="69d1d-132">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="69d1d-132">A function to call when the operation fails.</span></span></td>
</tr>
</table>

## <a name="return-value"></a><span data-ttu-id="69d1d-133">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="69d1d-133">Return Value</span></span>

<span data-ttu-id="69d1d-134">On success, returns a promise object containing the attributes specified earlier in the description of the **successCallback** parameter.</span><span class="sxs-lookup"><span data-stu-id="69d1d-134">On success, returns a promise object containing the attributes specified earlier in the description of the **successCallback** parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="69d1d-135">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="69d1d-135">Examples</span></span>

<span data-ttu-id="69d1d-136">These examples use some of the same request objects as demonstrated in [Update and delete entities using the Web API](../../../webapi/update-delete-entities-using-web-api.md) to define the data object for updating an entity record.</span><span class="sxs-lookup"><span data-stu-id="69d1d-136">These examples use some of the same request objects as demonstrated in [Update and delete entities using the Web API](../../../webapi/update-delete-entities-using-web-api.md) to define the data object for updating an entity record.</span></span>

<span data-ttu-id="69d1d-137">Deletes an account with record ID = 5531d753-95af-e711-a94e-000d3a11e605.</span><span class="sxs-lookup"><span data-stu-id="69d1d-137">Deletes an account with record ID = 5531d753-95af-e711-a94e-000d3a11e605.</span></span>

```JavaScript
Xrm.WebApi.deleteRecord("account", "5531d753-95af-e711-a94e-000d3a11e605").then(
    function success(result) {
        console.log("Account deleted");
        // perform operations on record deletion
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```
 
### <a name="related-topics"></a><span data-ttu-id="69d1d-138">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="69d1d-138">Related topics</span></span>

[<span data-ttu-id="69d1d-139">Xrm.WebApi</span><span class="sxs-lookup"><span data-stu-id="69d1d-139">Xrm.WebApi</span></span>](../xrm-webapi.md)




