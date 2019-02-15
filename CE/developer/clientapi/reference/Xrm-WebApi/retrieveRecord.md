---
title: retrieveRecord (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: d4e92999-3b79-4783-8cac-f656fc5f7fda
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c9c325ba74878a7a3bf445016fd1365b54aae497
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385488"
---
# <a name="retrieverecord-client-api-reference"></a><span data-ttu-id="272cc-102">retrieveRecord (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="272cc-102">retrieveRecord (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/retrieveRecord-description.md](./includes/retrieveRecord-description.md)] 

## <a name="syntax"></a><span data-ttu-id="272cc-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="272cc-103">Syntax</span></span>

`Xrm.WebApi.retrieveRecord(entityLogicalName, id, options).then(successCallback, errorCallback);`

## <a name="parameters"></a><span data-ttu-id="272cc-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="272cc-104">Parameters</span></span>

<table style="width:100%">
<tr>
<th><span data-ttu-id="272cc-105">Tên</span><span class="sxs-lookup"><span data-stu-id="272cc-105">Name</span></span></th>
<th><span data-ttu-id="272cc-106">Loại</span><span class="sxs-lookup"><span data-stu-id="272cc-106">Type</span></span></th>
<th><span data-ttu-id="272cc-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="272cc-107">Required</span></span></th>
<th><span data-ttu-id="272cc-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="272cc-108">Description</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="272cc-109">entityLogicalName</span><span class="sxs-lookup"><span data-stu-id="272cc-109">entityLogicalName</span></span></td>
<td><span data-ttu-id="272cc-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="272cc-110">String</span></span></td>
<td><span data-ttu-id="272cc-111">Có</span><span class="sxs-lookup"><span data-stu-id="272cc-111">Yes</span></span></td>
<td><span data-ttu-id="272cc-112">The entity logical name of the record you want to retrieve.</span><span class="sxs-lookup"><span data-stu-id="272cc-112">The entity logical name of the record you want to retrieve.</span></span> <span data-ttu-id="272cc-113">For example: &quot;account&quot;.</span><span class="sxs-lookup"><span data-stu-id="272cc-113">For example: &quot;account&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="272cc-114">ID</span><span class="sxs-lookup"><span data-stu-id="272cc-114">id</span></span></td>
<td><span data-ttu-id="272cc-115">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="272cc-115">String</span></span></td>
<td><span data-ttu-id="272cc-116">Có</span><span class="sxs-lookup"><span data-stu-id="272cc-116">Yes</span></span></td>
<td><span data-ttu-id="272cc-117">GUID of the entity record you want to retrieve.</span><span class="sxs-lookup"><span data-stu-id="272cc-117">GUID of the entity record you want to retrieve.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="272cc-118">tùy chọn</span><span class="sxs-lookup"><span data-stu-id="272cc-118">options</span></span></td>
<td><span data-ttu-id="272cc-119">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="272cc-119">String</span></span></td>
<td><span data-ttu-id="272cc-120">Không</span><span class="sxs-lookup"><span data-stu-id="272cc-120">No</span></span></td>
<td><p><span data-ttu-id="272cc-121">OData system query options, <b>$select</b> and <b>$expand</b>, to retrieve your data.</span><span class="sxs-lookup"><span data-stu-id="272cc-121">OData system query options, <b>$select</b> and <b>$expand</b>, to retrieve your data.</span></span></p>
<ul><li><span data-ttu-id="272cc-122">Use the <b>$select</b> system query option to limit the properties returned by including a comma-separated list of property names.</span><span class="sxs-lookup"><span data-stu-id="272cc-122">Use the <b>$select</b> system query option to limit the properties returned by including a comma-separated list of property names.</span></span> <span data-ttu-id="272cc-123">This is an important performance best practice.</span><span class="sxs-lookup"><span data-stu-id="272cc-123">This is an important performance best practice.</span></span> <span data-ttu-id="272cc-124">If properties aren’t specified using <b>$select</b>, all properties will be returned.</span><span class="sxs-lookup"><span data-stu-id="272cc-124">If properties aren’t specified using <b>$select</b>, all properties will be returned.</span></span></li>
<li><span data-ttu-id="272cc-125">Use the <b>$expand</b> system query option to control what data from related entities is returned.</span><span class="sxs-lookup"><span data-stu-id="272cc-125">Use the <b>$expand</b> system query option to control what data from related entities is returned.</span></span> <span data-ttu-id="272cc-126">If you just include the name of the navigation property, you’ll receive all the properties for related records.</span><span class="sxs-lookup"><span data-stu-id="272cc-126">If you just include the name of the navigation property, you’ll receive all the properties for related records.</span></span> <span data-ttu-id="272cc-127">You can limit the properties returned for related records using the <b>$select</b> system query option in parentheses after the navigation property name.</span><span class="sxs-lookup"><span data-stu-id="272cc-127">You can limit the properties returned for related records using the <b>$select</b> system query option in parentheses after the navigation property name.</span></span> <span data-ttu-id="272cc-128">Use this for both <i>single-valued</i> and <i>collection-valued</i> navigation properties.</span><span class="sxs-lookup"><span data-stu-id="272cc-128">Use this for both <i>single-valued</i> and <i>collection-valued</i> navigation properties.</span></span></li>
</ul>
<p><span data-ttu-id="272cc-129">You specify the query options starting with <code>?</code>.</span><span class="sxs-lookup"><span data-stu-id="272cc-129">You specify the query options starting with <code>?</code>.</span></span> <span data-ttu-id="272cc-130">You can also specify multiple query options by using <code>&amp;</code> to separate the query options.</span><span class="sxs-lookup"><span data-stu-id="272cc-130">You can also specify multiple query options by using <code>&amp;</code> to separate the query options.</span></span> <span data-ttu-id="272cc-131">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="272cc-131">For example:</span></span></p>
<code>?$select=name&amp;$expand=primarycontactid($select=contactid,fullname)</code>
<p><span data-ttu-id="272cc-132">See examples later in this topic to see how you can define the <code>options</code> parameter for various retrieve scenarios.</span><span class="sxs-lookup"><span data-stu-id="272cc-132">See examples later in this topic to see how you can define the <code>options</code> parameter for various retrieve scenarios.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="272cc-133">successCallback</span><span class="sxs-lookup"><span data-stu-id="272cc-133">successCallback</span></span></td>
<td><span data-ttu-id="272cc-134">Hàm</span><span class="sxs-lookup"><span data-stu-id="272cc-134">Function</span></span></td>
<td><span data-ttu-id="272cc-135">Không</span><span class="sxs-lookup"><span data-stu-id="272cc-135">No</span></span></td>
<td><p><span data-ttu-id="272cc-136">A function to call when a record is retrieved.</span><span class="sxs-lookup"><span data-stu-id="272cc-136">A function to call when a record is retrieved.</span></span> <span data-ttu-id="272cc-137">A JSON object with the retrieved properties and values will be passed to the function.</span><span class="sxs-lookup"><span data-stu-id="272cc-137">A JSON object with the retrieved properties and values will be passed to the function.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="272cc-138">errorCallback</span><span class="sxs-lookup"><span data-stu-id="272cc-138">errorCallback</span></span></td>
<td><span data-ttu-id="272cc-139">Hàm</span><span class="sxs-lookup"><span data-stu-id="272cc-139">Function</span></span></td>
<td><span data-ttu-id="272cc-140">Không</span><span class="sxs-lookup"><span data-stu-id="272cc-140">No</span></span></td>
<td><span data-ttu-id="272cc-141">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="272cc-141">A function to call when the operation fails.</span></span></td>
</tr>
</table>

## <a name="return-value"></a><span data-ttu-id="272cc-142">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="272cc-142">Return Value</span></span>

<span data-ttu-id="272cc-143">On success, returns a promise containing a JSON object with the retrieved attributes and their values.</span><span class="sxs-lookup"><span data-stu-id="272cc-143">On success, returns a promise containing a JSON object with the retrieved attributes and their values.</span></span>

## <a name="examples"></a><span data-ttu-id="272cc-144">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="272cc-144">Examples</span></span>

### <a name="basic-retrieve"></a><span data-ttu-id="272cc-145">Basic retrieve</span><span class="sxs-lookup"><span data-stu-id="272cc-145">Basic retrieve</span></span> 

<span data-ttu-id="272cc-146">Retrieves the name and revenue of an account record with record ID = 5531d753-95af-e711-a94e-000d3a11e605.</span><span class="sxs-lookup"><span data-stu-id="272cc-146">Retrieves the name and revenue of an account record with record ID = 5531d753-95af-e711-a94e-000d3a11e605.</span></span>

```JavaScript
Xrm.WebApi.retrieveRecord("account", "5531d753-95af-e711-a94e-000d3a11e605", "?$select=name,revenue").then(
    function success(result) {
        console.log(`Retrieved values: Name: ${result.name}, Revenue: ${result.revenue}`);
        // perform operations on record retrieval
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```

<span data-ttu-id="272cc-147">The above example displays the following in your console; you might see other values depending on your data:</span><span class="sxs-lookup"><span data-stu-id="272cc-147">The above example displays the following in your console; you might see other values depending on your data:</span></span>

`Retrieved values: Name: Sample Account, Revenue: 5000000`

### <a name="retrieve-related-entities-for-an-entity-instance-by-expanding-single-valued-navigation-properties"></a><span data-ttu-id="272cc-148">Retrieve related entities for an entity instance by expanding single-valued navigation properties</span><span class="sxs-lookup"><span data-stu-id="272cc-148">Retrieve related entities for an entity instance by expanding single-valued navigation properties</span></span>

 <span data-ttu-id="272cc-149">The following example demonstrates how to retrieve the contact for an account record with record ID = a8a19cdd-88df-e311-b8e5-6c3be5a8b200.</span><span class="sxs-lookup"><span data-stu-id="272cc-149">The following example demonstrates how to retrieve the contact for an account record with record ID = a8a19cdd-88df-e311-b8e5-6c3be5a8b200.</span></span> <span data-ttu-id="272cc-150">For the related contact record, we are only retrieving the **contactid** and **fullname** properties.</span><span class="sxs-lookup"><span data-stu-id="272cc-150">For the related contact record, we are only retrieving the **contactid** and **fullname** properties.</span></span>

```JavaScript
Xrm.WebApi.retrieveRecord("account", "a8a19cdd-88df-e311-b8e5-6c3be5a8b200", "?$select=name&$expand=primarycontactid($select=contactid,fullname)").then(
    function success(result) {
        console.log(`Retrieved values: Name: ${result.name}, Primary Contact ID: ${result.primarycontactid.contactid}, Primary Contact Name: ${result.primarycontactid.fullname}`);
        // perform operations on record retrieval
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```

<span data-ttu-id="272cc-151">The above example displays the following in your console; you might see other values depending on your data:</span><span class="sxs-lookup"><span data-stu-id="272cc-151">The above example displays the following in your console; you might see other values depending on your data:</span></span>

`Retrieved values: Name: Adventure Works, Primary Contact ID: 49a0e5b9-88df-e311-b8e5-6c3be5a8b200, Primary Contact Name: Adrian Dumitrascu`

 
### <a name="related-topics"></a><span data-ttu-id="272cc-152">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="272cc-152">Related topics</span></span>

[<span data-ttu-id="272cc-153">Xrm.WebApi.retrieveMultipleRecords</span><span class="sxs-lookup"><span data-stu-id="272cc-153">Xrm.WebApi.retrieveMultipleRecords</span></span>](retrieveMultipleRecords.md)

[<span data-ttu-id="272cc-154">Xrm.WebApi</span><span class="sxs-lookup"><span data-stu-id="272cc-154">Xrm.WebApi</span></span>](../xrm-webapi.md)




