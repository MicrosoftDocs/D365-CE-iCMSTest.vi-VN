---
title: Xrm.WebApi.online.executeMultiple (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 03/20/2018
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
ms.openlocfilehash: bf00725886d6b6d1a35440494bb50d765616cf4c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386897"
---
# <a name="xrmwebapionlineexecutemultiple-client-api-reference"></a><span data-ttu-id="a37e6-102">Xrm.WebApi.online.executeMultiple (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="a37e6-102">Xrm.WebApi.online.executeMultiple (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/executeMultiple-description.md](../includes/executeMultiple-description.md)]

> [!NOTE]
> <span data-ttu-id="a37e6-103">This method is supported only for the online mode ([Xrm.WebApi.online](../online.md)).</span><span class="sxs-lookup"><span data-stu-id="a37e6-103">This method is supported only for the online mode ([Xrm.WebApi.online](../online.md)).</span></span>

<span data-ttu-id="a37e6-104">If you want to execute multiple requests in a transaction, you must pass in a change set as a parameter to this method.</span><span class="sxs-lookup"><span data-stu-id="a37e6-104">If you want to execute multiple requests in a transaction, you must pass in a change set as a parameter to this method.</span></span> <span data-ttu-id="a37e6-105">[Change sets](../../../../webapi/execute-batch-operations-using-web-api.md#bkmk_ChangeSets) represent a collection of operations that are executed in a transaction.</span><span class="sxs-lookup"><span data-stu-id="a37e6-105">[Change sets](../../../../webapi/execute-batch-operations-using-web-api.md#bkmk_ChangeSets) represent a collection of operations that are executed in a transaction.</span></span> <span data-ttu-id="a37e6-106">You can also pass in individual requests and change sets together as parameters to this method.</span><span class="sxs-lookup"><span data-stu-id="a37e6-106">You can also pass in individual requests and change sets together as parameters to this method.</span></span>

> [!NOTE]
> <span data-ttu-id="a37e6-107">You cannot include read operations (retrieve, retrieve multiple, and Web API functions) as part of a change set; this is as per the OData v4 specifications.</span><span class="sxs-lookup"><span data-stu-id="a37e6-107">You cannot include read operations (retrieve, retrieve multiple, and Web API functions) as part of a change set; this is as per the OData v4 specifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="a37e6-108">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="a37e6-108">Syntax</span></span>

<span data-ttu-id="a37e6-109">**Execute multiple requests:**</span><span class="sxs-lookup"><span data-stu-id="a37e6-109">**Execute multiple requests:**</span></span>

```JavaScript
var requests = [req1, req2, req3];
Xrm.WebApi.online.executeMultiple(requests).then(successCallback, errorCallback);
```

<span data-ttu-id="a37e6-110">**Execute multiple requests in a transaction:**</span><span class="sxs-lookup"><span data-stu-id="a37e6-110">**Execute multiple requests in a transaction:**</span></span>

<span data-ttu-id="a37e6-111">In this case, `req1`, `req2`, and `req3` will be executed in transaction.</span><span class="sxs-lookup"><span data-stu-id="a37e6-111">In this case, `req1`, `req2`, and `req3` will be executed in transaction.</span></span>

```JavaScript
var changeSet = [req1, req2, req3];
var requests = [changeSet];
Xrm.WebApi.online.executeMultiple(requests).then(successCallback, errorCallback);
```


<span data-ttu-id="a37e6-112">**Execute a mix of individual requests and multiple requests in a transaction:**</span><span class="sxs-lookup"><span data-stu-id="a37e6-112">**Execute a mix of individual requests and multiple requests in a transaction:**</span></span>

<span data-ttu-id="a37e6-113">In this case, `req1`, `req2`, and `req3` will be executed in transaction, but `req4` and `req5` will be executed individually.</span><span class="sxs-lookup"><span data-stu-id="a37e6-113">In this case, `req1`, `req2`, and `req3` will be executed in transaction, but `req4` and `req5` will be executed individually.</span></span>

```JavaScript
var changeSet = [req1, req2, req3];
var requests = [req4, req5, changeset];
Xrm.WebApi.online.executeMultiple(requests).then(successCallback, errorCallback);
```

## <a name="parameters"></a><span data-ttu-id="a37e6-114">Tham số</span><span class="sxs-lookup"><span data-stu-id="a37e6-114">Parameters</span></span>

<table style="width:100%">
<tr>
<th><span data-ttu-id="a37e6-115">Tên</span><span class="sxs-lookup"><span data-stu-id="a37e6-115">Name</span></span></th>
<th><span data-ttu-id="a37e6-116">Loại</span><span class="sxs-lookup"><span data-stu-id="a37e6-116">Type</span></span></th>
<th><span data-ttu-id="a37e6-117">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="a37e6-117">Required</span></span></th>
<th><span data-ttu-id="a37e6-118">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a37e6-118">Description</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="a37e6-119">requests</span><span class="sxs-lookup"><span data-stu-id="a37e6-119">requests</span></span></td>
<td><span data-ttu-id="a37e6-120">Array of objects</span><span class="sxs-lookup"><span data-stu-id="a37e6-120">Array of objects</span></span></td>
<td><span data-ttu-id="a37e6-121">Có</span><span class="sxs-lookup"><span data-stu-id="a37e6-121">Yes</span></span></td>
<td><p><span data-ttu-id="a37e6-122">An array of one of one of the following types:</span><span class="sxs-lookup"><span data-stu-id="a37e6-122">An array of one of one of the following types:</span></span></p>
<ul>
<li><span data-ttu-id="a37e6-123">objects where each object is an action, function, or CRUD request that you want to execute against the Web API endpoint.</span><span class="sxs-lookup"><span data-stu-id="a37e6-123">objects where each object is an action, function, or CRUD request that you want to execute against the Web API endpoint.</span></span> <span data-ttu-id="a37e6-124">Each object exposes a <b>getMetadata</b> method that lets you define the metadata for the action, function or CRUD request you want to execute.</span><span class="sxs-lookup"><span data-stu-id="a37e6-124">Each object exposes a <b>getMetadata</b> method that lets you define the metadata for the action, function or CRUD request you want to execute.</span></span> <span data-ttu-id="a37e6-125">This is the same object that you pass in the <code>execute</code> method.</span><span class="sxs-lookup"><span data-stu-id="a37e6-125">This is the same object that you pass in the <code>execute</code> method.</span></span> <span data-ttu-id="a37e6-126">For information about the object, see <a href="execute.md">execute</a>.</span><span class="sxs-lookup"><span data-stu-id="a37e6-126">For information about the object, see <a href="execute.md">execute</a>.</span></span></li>
<li><span data-ttu-id="a37e6-127">Change set (an array of objects), where each object in the change set is as defined above.</span><span class="sxs-lookup"><span data-stu-id="a37e6-127">Change set (an array of objects), where each object in the change set is as defined above.</span></span> <span data-ttu-id="a37e6-128">In this case, all the request objects specified in the change set will get executed in a transaction.</span><span class="sxs-lookup"><span data-stu-id="a37e6-128">In this case, all the request objects specified in the change set will get executed in a transaction.</span></span></li>
</ul>
<p><span data-ttu-id="a37e6-129">See request examples earlier in the <strong>Syntax</strong> section for more information.</span><span class="sxs-lookup"><span data-stu-id="a37e6-129">See request examples earlier in the <strong>Syntax</strong> section for more information.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a37e6-130">successCallback</span><span class="sxs-lookup"><span data-stu-id="a37e6-130">successCallback</span></span></td>
<td><span data-ttu-id="a37e6-131">Hàm</span><span class="sxs-lookup"><span data-stu-id="a37e6-131">Function</span></span></td>
<td><span data-ttu-id="a37e6-132">Không</span><span class="sxs-lookup"><span data-stu-id="a37e6-132">No</span></span></td>
<td><p><span data-ttu-id="a37e6-133">A function to call when operation is executed suucessfully.</span><span class="sxs-lookup"><span data-stu-id="a37e6-133">A function to call when operation is executed suucessfully.</span></span> <span data-ttu-id="a37e6-134">An array of response objects are passed to the function where weach response object has the following attributes:</span><span class="sxs-lookup"><span data-stu-id="a37e6-134">An array of response objects are passed to the function where weach response object has the following attributes:</span></span></p>
<ul>
<li><span data-ttu-id="a37e6-135"><b>body</b>: (Optional).</span><span class="sxs-lookup"><span data-stu-id="a37e6-135"><b>body</b>: (Optional).</span></span> <span data-ttu-id="a37e6-136">Object.</span><span class="sxs-lookup"><span data-stu-id="a37e6-136">Object.</span></span> <span data-ttu-id="a37e6-137">Response body.</span><span class="sxs-lookup"><span data-stu-id="a37e6-137">Response body.</span></span></li>
<li><span data-ttu-id="a37e6-138"><b>headers</b>: Object.</span><span class="sxs-lookup"><span data-stu-id="a37e6-138"><b>headers</b>: Object.</span></span> <span data-ttu-id="a37e6-139">Response headers.</span><span class="sxs-lookup"><span data-stu-id="a37e6-139">Response headers.</span></span></li>
<li><span data-ttu-id="a37e6-140"><b>ok</b>: Boolean.</span><span class="sxs-lookup"><span data-stu-id="a37e6-140"><b>ok</b>: Boolean.</span></span> <span data-ttu-id="a37e6-141">Indicates whether the request was successful.</span><span class="sxs-lookup"><span data-stu-id="a37e6-141">Indicates whether the request was successful.</span></span></li>
<li><span data-ttu-id="a37e6-142"><b>status</b>: Number.</span><span class="sxs-lookup"><span data-stu-id="a37e6-142"><b>status</b>: Number.</span></span> <span data-ttu-id="a37e6-143">Numeric value in the response status code.</span><span class="sxs-lookup"><span data-stu-id="a37e6-143">Numeric value in the response status code.</span></span> <span data-ttu-id="a37e6-144">For example: <b>200</b></span><span class="sxs-lookup"><span data-stu-id="a37e6-144">For example: <b>200</b></span></span></li>
<li><span data-ttu-id="a37e6-145"><b>statusText</b>: String.</span><span class="sxs-lookup"><span data-stu-id="a37e6-145"><b>statusText</b>: String.</span></span> <span data-ttu-id="a37e6-146">Description of the response status code.</span><span class="sxs-lookup"><span data-stu-id="a37e6-146">Description of the response status code.</span></span> <span data-ttu-id="a37e6-147">For example: <b>OK</b></span><span class="sxs-lookup"><span data-stu-id="a37e6-147">For example: <b>OK</b></span></span></li>
<li><span data-ttu-id="a37e6-148"><b>type</b>: String.</span><span class="sxs-lookup"><span data-stu-id="a37e6-148"><b>type</b>: String.</span></span> <span data-ttu-id="a37e6-149">Response type.</span><span class="sxs-lookup"><span data-stu-id="a37e6-149">Response type.</span></span> <span data-ttu-id="a37e6-150">Values are: the empty string (default), &quot;arraybuffer&quot;, &quot;blob&quot;, &quot;document&quot;, &quot;json&quot;, and &quot;text&quot;.</span><span class="sxs-lookup"><span data-stu-id="a37e6-150">Values are: the empty string (default), &quot;arraybuffer&quot;, &quot;blob&quot;, &quot;document&quot;, &quot;json&quot;, and &quot;text&quot;.</span></span></b></li>
<li><span data-ttu-id="a37e6-151"><b>url</b>: String.</span><span class="sxs-lookup"><span data-stu-id="a37e6-151"><b>url</b>: String.</span></span> <span data-ttu-id="a37e6-152">Request URL of the action, function, or CRUD request that was sent to the Web API endpoint.</span><span class="sxs-lookup"><span data-stu-id="a37e6-152">Request URL of the action, function, or CRUD request that was sent to the Web API endpoint.</span></span></b></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a37e6-153">errorCallback</span><span class="sxs-lookup"><span data-stu-id="a37e6-153">errorCallback</span></span></td>
<td><span data-ttu-id="a37e6-154">Hàm</span><span class="sxs-lookup"><span data-stu-id="a37e6-154">Function</span></span></td>
<td><span data-ttu-id="a37e6-155">Không</span><span class="sxs-lookup"><span data-stu-id="a37e6-155">No</span></span></td>
<td><span data-ttu-id="a37e6-156">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="a37e6-156">A function to call when the operation fails.</span></span></td>
</tr>
</table>

## <a name="return-value"></a><span data-ttu-id="a37e6-157">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="a37e6-157">Return Value</span></span>

<span data-ttu-id="a37e6-158">On success, returns a promise containing an array of objects with the attributes specified earlier in the description of **successCallback** function.</span><span class="sxs-lookup"><span data-stu-id="a37e6-158">On success, returns a promise containing an array of objects with the attributes specified earlier in the description of **successCallback** function.</span></span>

### <a name="related-topics"></a><span data-ttu-id="a37e6-159">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="a37e6-159">Related topics</span></span>

[<span data-ttu-id="a37e6-160">Xrm.WebApi.online</span><span class="sxs-lookup"><span data-stu-id="a37e6-160">Xrm.WebApi.online</span></span>](../online.md)

