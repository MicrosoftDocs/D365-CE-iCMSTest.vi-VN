---
title: retrieveMultipleRecords (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 05/24/2018
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
ms.openlocfilehash: 3911e4dbe0ecc4642fe6d98c7693802336d5bac3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388016"
---
# <a name="retrievemultiplerecords-client-api-reference"></a><span data-ttu-id="6d47b-102">retrieveMultipleRecords (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="6d47b-102">retrieveMultipleRecords (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/retrieveMultipleRecords-description.md](./includes/retrieveMultipleRecords-description.md)] 

## <a name="syntax"></a><span data-ttu-id="6d47b-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="6d47b-103">Syntax</span></span>

`Xrm.WebApi.retrieveMultipleRecords(entityLogicalName, options, maxPageSize).then(successCallback, errorCallback);`

## <a name="parameters"></a><span data-ttu-id="6d47b-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="6d47b-104">Parameters</span></span>

<table style="width:100%">
<tr>
<th><span data-ttu-id="6d47b-105">Tên</span><span class="sxs-lookup"><span data-stu-id="6d47b-105">Name</span></span></th>
<th><span data-ttu-id="6d47b-106">Loại</span><span class="sxs-lookup"><span data-stu-id="6d47b-106">Type</span></span></th>
<th><span data-ttu-id="6d47b-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="6d47b-107">Required</span></span></th>
<th><span data-ttu-id="6d47b-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="6d47b-108">Description</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="6d47b-109">entityLogicalName</span><span class="sxs-lookup"><span data-stu-id="6d47b-109">entityLogicalName</span></span></td>
<td><span data-ttu-id="6d47b-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="6d47b-110">String</span></span></td>
<td><span data-ttu-id="6d47b-111">Có</span><span class="sxs-lookup"><span data-stu-id="6d47b-111">Yes</span></span></td>
<td><span data-ttu-id="6d47b-112">The entity logical name of the records you want to retrieve.</span><span class="sxs-lookup"><span data-stu-id="6d47b-112">The entity logical name of the records you want to retrieve.</span></span> <span data-ttu-id="6d47b-113">For example: &quot;account&quot;.</span><span class="sxs-lookup"><span data-stu-id="6d47b-113">For example: &quot;account&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6d47b-114">tùy chọn</span><span class="sxs-lookup"><span data-stu-id="6d47b-114">options</span></span></td>
<td><span data-ttu-id="6d47b-115">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="6d47b-115">String</span></span></td>
<td><span data-ttu-id="6d47b-116">Không</span><span class="sxs-lookup"><span data-stu-id="6d47b-116">No</span></span></td>
<td><p><span data-ttu-id="6d47b-117">OData system query options or FetchXML query to retrieve your data.</span><span class="sxs-lookup"><span data-stu-id="6d47b-117">OData system query options or FetchXML query to retrieve your data.</span></span> </p> 
<ul>
<li><span data-ttu-id="6d47b-118">Following system query options are supported: <b>$select</b>, <b>$top</b>, <b>$filter</b>, <b>$expand</b>, and <b>$orderby</b>.</span><span class="sxs-lookup"><span data-stu-id="6d47b-118">Following system query options are supported: <b>$select</b>, <b>$top</b>, <b>$filter</b>, <b>$expand</b>, and <b>$orderby</b>.</span></span></li>
<li><span data-ttu-id="6d47b-119">To specify a FetchXML query, use the <code>fetchXml</code> attribute to specify the query.</span><span class="sxs-lookup"><span data-stu-id="6d47b-119">To specify a FetchXML query, use the <code>fetchXml</code> attribute to specify the query.</span></span></li>
</ul>
<p><span data-ttu-id="6d47b-120">NOTE: You must always use the <b>$select</b> system query option to limit the properties returned for an entity record by including a comma-separated list of property names.</span><span class="sxs-lookup"><span data-stu-id="6d47b-120">NOTE: You must always use the <b>$select</b> system query option to limit the properties returned for an entity record by including a comma-separated list of property names.</span></span> <span data-ttu-id="6d47b-121">This is an important performance best practice.</span><span class="sxs-lookup"><span data-stu-id="6d47b-121">This is an important performance best practice.</span></span> <span data-ttu-id="6d47b-122">If properties aren’t specified using <b>$select</b>, all properties will be returned.</span><span class="sxs-lookup"><span data-stu-id="6d47b-122">If properties aren’t specified using <b>$select</b>, all properties will be returned.</span></span></li>
<p><span data-ttu-id="6d47b-123">You specify the query options starting with <code>?</code>.</span><span class="sxs-lookup"><span data-stu-id="6d47b-123">You specify the query options starting with <code>?</code>.</span></span> <span data-ttu-id="6d47b-124">You can also specify multiple system query options by using <code>&amp;</code> to separate the query options.</span><span class="sxs-lookup"><span data-stu-id="6d47b-124">You can also specify multiple system query options by using <code>&amp;</code> to separate the query options.</span></span>
<p><span data-ttu-id="6d47b-125">See examples later in this topic to see how you can define the <code>options</code> parameter for various retrieve multiple scenarios.</span><span class="sxs-lookup"><span data-stu-id="6d47b-125">See examples later in this topic to see how you can define the <code>options</code> parameter for various retrieve multiple scenarios.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6d47b-126">maxPageSize</span><span class="sxs-lookup"><span data-stu-id="6d47b-126">maxPageSize</span></span></td>
<td><span data-ttu-id="6d47b-127">Số</span><span class="sxs-lookup"><span data-stu-id="6d47b-127">Number</span></span></td>
<td><span data-ttu-id="6d47b-128">Không</span><span class="sxs-lookup"><span data-stu-id="6d47b-128">No</span></span></td>
<td><p><span data-ttu-id="6d47b-129">Specify a positive number that indicates the number of entity records to be returned per page.</span><span class="sxs-lookup"><span data-stu-id="6d47b-129">Specify a positive number that indicates the number of entity records to be returned per page.</span></span> <span data-ttu-id="6d47b-130">If you do not specify this parameter, the default value is passed as 5000.</span><span class="sxs-lookup"><span data-stu-id="6d47b-130">If you do not specify this parameter, the default value is passed as 5000.</span></span></p>
<p><span data-ttu-id="6d47b-131">If the number of records being retrieved is more than the specified <code>maxPageSize</code> value, <code>nextLink</code> attribute in the returned promise object will contain a link to retrieve the next set of entities.</span><span class="sxs-lookup"><span data-stu-id="6d47b-131">If the number of records being retrieved is more than the specified <code>maxPageSize</code> value, <code>nextLink</code> attribute in the returned promise object will contain a link to retrieve the next set of entities.</span></span> </td>
</tr>
<tr>
<td><span data-ttu-id="6d47b-132">successCallback</span><span class="sxs-lookup"><span data-stu-id="6d47b-132">successCallback</span></span></td>
<td><span data-ttu-id="6d47b-133">Hàm</span><span class="sxs-lookup"><span data-stu-id="6d47b-133">Function</span></span></td>
<td><span data-ttu-id="6d47b-134">Không</span><span class="sxs-lookup"><span data-stu-id="6d47b-134">No</span></span></td>
<td><p><span data-ttu-id="6d47b-135">A function to call when entity records are retrieved.</span><span class="sxs-lookup"><span data-stu-id="6d47b-135">A function to call when entity records are retrieved.</span></span> <span data-ttu-id="6d47b-136">An object with the following attributes is passed to the function:</span><span class="sxs-lookup"><span data-stu-id="6d47b-136">An object with the following attributes is passed to the function:</span></span></p>
<ul>
<li><span data-ttu-id="6d47b-137"><b>entities</b>: An array of JSON objects, where each object represents the retrieved entity record containing attributes and their values as <code>key: value</code> pairs.</span><span class="sxs-lookup"><span data-stu-id="6d47b-137"><b>entities</b>: An array of JSON objects, where each object represents the retrieved entity record containing attributes and their values as <code>key: value</code> pairs.</span></span> <span data-ttu-id="6d47b-138">The Id of the entity record is retrieved by default.</span><span class="sxs-lookup"><span data-stu-id="6d47b-138">The Id of the entity record is retrieved by default.</span></span></li>
<li><span data-ttu-id="6d47b-139"><b>nextLink</b>: String.</span><span class="sxs-lookup"><span data-stu-id="6d47b-139"><b>nextLink</b>: String.</span></span> <span data-ttu-id="6d47b-140">If the number of records being retrieved is more than the value specified in the <code>maxPageSize</code> parameter in the request, this attribute returns the URL to return next set of records.</span><span class="sxs-lookup"><span data-stu-id="6d47b-140">If the number of records being retrieved is more than the value specified in the <code>maxPageSize</code> parameter in the request, this attribute returns the URL to return next set of records.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="6d47b-141">errorCallback</span><span class="sxs-lookup"><span data-stu-id="6d47b-141">errorCallback</span></span></td>
<td><span data-ttu-id="6d47b-142">Hàm</span><span class="sxs-lookup"><span data-stu-id="6d47b-142">Function</span></span></td>
<td><span data-ttu-id="6d47b-143">Không</span><span class="sxs-lookup"><span data-stu-id="6d47b-143">No</span></span></td>
<td><span data-ttu-id="6d47b-144">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="6d47b-144">A function to call when the operation fails.</span></span></td>
</tr>
</table>

## <a name="return-value"></a><span data-ttu-id="6d47b-145">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="6d47b-145">Return Value</span></span>

<span data-ttu-id="6d47b-146">On success, returns a promise that contains an array of JSON objects (**entities**) containing the retrieved entity records and the **nextLink** attribute (optional) with the URL pointing to next set of records in case paging (`maxPageSize`) is specified in the request, and the record count returned exceeds the paging value.</span><span class="sxs-lookup"><span data-stu-id="6d47b-146">On success, returns a promise that contains an array of JSON objects (**entities**) containing the retrieved entity records and the **nextLink** attribute (optional) with the URL pointing to next set of records in case paging (`maxPageSize`) is specified in the request, and the record count returned exceeds the paging value.</span></span>

## <a name="examples"></a><span data-ttu-id="6d47b-147">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="6d47b-147">Examples</span></span>

<span data-ttu-id="6d47b-148">Most of the scenarios/examples mentioned in [Query Data using the Web API](../../../webapi/query-data-web-api.md) can be achieved using the **retrieveMutipleRecords** method.</span><span class="sxs-lookup"><span data-stu-id="6d47b-148">Most of the scenarios/examples mentioned in [Query Data using the Web API](../../../webapi/query-data-web-api.md) can be achieved using the **retrieveMutipleRecords** method.</span></span> <span data-ttu-id="6d47b-149">Some of the examples are listed below.</span><span class="sxs-lookup"><span data-stu-id="6d47b-149">Some of the examples are listed below.</span></span>

### <a name="basic-retrieve-multiple"></a><span data-ttu-id="6d47b-150">Basic retrieve multiple</span><span class="sxs-lookup"><span data-stu-id="6d47b-150">Basic retrieve multiple</span></span>

<span data-ttu-id="6d47b-151">This example queries the accounts entity set and uses the `$select` and `$top` system query options to return the name property for the first three accounts:</span><span class="sxs-lookup"><span data-stu-id="6d47b-151">This example queries the accounts entity set and uses the `$select` and `$top` system query options to return the name property for the first three accounts:</span></span>

```JavaScript
Xrm.WebApi.retrieveMultipleRecords("account", "?$select=name&$top=3").then(
    function success(result) {
        for (var i = 0; i < result.entities.length; i++) {
            console.log(result.entities[i]);
        }                    
        // perform additional operations on retrieved records
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```

### <a name="specify-the-number-of-entities-to-return-in-a-page"></a><span data-ttu-id="6d47b-152">Specify the number of entities to return in a page</span><span class="sxs-lookup"><span data-stu-id="6d47b-152">Specify the number of entities to return in a page</span></span>

<span data-ttu-id="6d47b-153">The following example demonstrates the use of the `maxPageSize` parameter to specify the number of records (3) to be displayed in a page.</span><span class="sxs-lookup"><span data-stu-id="6d47b-153">The following example demonstrates the use of the `maxPageSize` parameter to specify the number of records (3) to be displayed in a page.</span></span>

```JavaScript
Xrm.WebApi.retrieveMultipleRecords("account", "?$select=name", 3).then(
    function success(result) {
        for (var i = 0; i < result.entities.length; i++) {
            console.log(result.entities[i]);
        }
        console.log("Next page link: " + result.nextLink);
        // perform additional operations on retrieved records
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```

<span data-ttu-id="6d47b-154">This example will display 3 records and a link to the next page.</span><span class="sxs-lookup"><span data-stu-id="6d47b-154">This example will display 3 records and a link to the next page.</span></span> <span data-ttu-id="6d47b-155">Here is an example outout from the **Console** in the browser developer tools:</span><span class="sxs-lookup"><span data-stu-id="6d47b-155">Here is an example outout from the **Console** in the browser developer tools:</span></span>

```
{@odata.etag: "W/"1035541"", name: "A. Datum", accountid: "475b158c-541c-e511-80d3-3863bb347ba8"}
@odata.etag: "W/"1035541""accountid: "475b158c-541c-e511-80d3-3863bb347ba8"name: "A. Datum"__proto__: Object
VM5595:4 
{@odata.etag: "W/"947306"", name: "Adventure Works", accountid: "a8a19cdd-88df-e311-b8e5-6c3be5a8b200"}
VM5595:4 
{@odata.etag: "W/"1033754"", name: "Alpine Ski House", accountid: "aaa19cdd-88df-e311-b8e5-6c3be5a8b200"}
VM5595:6 
Next page link: [Organization URI]/api/data/v9.0/accounts?$select=name&$skiptoken=%3Ccookie%20pagenumber=%222%22%20pagingcookie=%22%253ccookie%2520page%253d%25221%2522%253e%253caccountid%2520last%253d%2522%257bAAA19CDD-88DF-E311-B8E5-6C3BE5A8B200%257d%2522%2520first%253d%2522%257b475B158C-541C-E511-80D3-3863BB347BA8%257d%2522%2520%252f%253e%253c%252fcookie%253e%22%20istracking=%22False%22%20/%3E
```

<span data-ttu-id="6d47b-156">Use the query part in the URL in the `nextLink` property as the value for the `options` parameter in your subsequent **retrieveMultipleRecords** call to request the next set of records.</span><span class="sxs-lookup"><span data-stu-id="6d47b-156">Use the query part in the URL in the `nextLink` property as the value for the `options` parameter in your subsequent **retrieveMultipleRecords** call to request the next set of records.</span></span> <span data-ttu-id="6d47b-157">Don’t change or append any additional system query options to the value.</span><span class="sxs-lookup"><span data-stu-id="6d47b-157">Don’t change or append any additional system query options to the value.</span></span> <span data-ttu-id="6d47b-158">For every subsequent request for additional pages, you should use the same `maxPageSize` value used in the original retrieve multiple request.</span><span class="sxs-lookup"><span data-stu-id="6d47b-158">For every subsequent request for additional pages, you should use the same `maxPageSize` value used in the original retrieve multiple request.</span></span> <span data-ttu-id="6d47b-159">Also, cache the results returned or the value of the nextLink property so that previously retrieved pages can be returned.</span><span class="sxs-lookup"><span data-stu-id="6d47b-159">Also, cache the results returned or the value of the nextLink property so that previously retrieved pages can be returned.</span></span> 

<span data-ttu-id="6d47b-160">For example, to get the next page of records, we will pass in the query part of the `nextLink` URL to the `options` parameter:</span><span class="sxs-lookup"><span data-stu-id="6d47b-160">For example, to get the next page of records, we will pass in the query part of the `nextLink` URL to the `options` parameter:</span></span>

```JavaScript
Xrm.WebApi.retrieveMultipleRecords("account", "?$select=name&$skiptoken=%3Ccookie%20pagenumber=%222%22%20pagingcookie=%22%253ccookie%2520page%253d%25221%2522%253e%253caccountid%2520last%253d%2522%257bAAA19CDD-88DF-E311-B8E5-6C3BE5A8B200%257d%2522%2520first%253d%2522%257b475B158C-541C-E511-80D3-3863BB347BA8%257d%2522%2520%252f%253e%253c%252fcookie%253e%22%20istracking=%22False%22%20/%3E", 3).then(
    function success(result) {
        for (var i = 0; i < result.entities.length; i++) {
            console.log(result.entities[i]);
        }
        console.log("Next page link: " + result.nextLink);
        // perform additional operations on retrieved records
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```

<span data-ttu-id="6d47b-161">This will return the next page of the resultset:</span><span class="sxs-lookup"><span data-stu-id="6d47b-161">This will return the next page of the resultset:</span></span>

```
{@odata.etag: "W/"1035542"", name: "Blue Yonder Airlines", accountid: "aca19cdd-88df-e311-b8e5-6c3be5a8b200"}
VM5597:4 
{@odata.etag: "W/"1031348"", name: "City Power & Light", accountid: "aea19cdd-88df-e311-b8e5-6c3be5a8b200"}
VM5597:4 
{@odata.etag: "W/"1035543"", name: "Coho Winery", accountid: "b0a19cdd-88df-e311-b8e5-6c3be5a8b200"}
VM5597:6 
Next page link: [Organization URI]/api/data/v9.0/accounts?$select=name&$skiptoken=%3Ccookie%20pagenumber=%223%22%20pagingcookie=%22%253ccookie%2520page%253d%25222%2522%253e%253caccountid%2520last%253d%2522%257bB0A19CDD-88DF-E311-B8E5-6C3BE5A8B200%257d%2522%2520first%253d%2522%257bACA19CDD-88DF-E311-B8E5-6C3BE5A8B200%257d%2522%2520%252f%253e%253c%252fcookie%253e%22%20istracking=%22False%22%20/%3E
``` 
  
> [!IMPORTANT]
>  <span data-ttu-id="6d47b-162">The value of the `nextLink` property is URI encoded.</span><span class="sxs-lookup"><span data-stu-id="6d47b-162">The value of the `nextLink` property is URI encoded.</span></span> <span data-ttu-id="6d47b-163">If you URI encode the value before you send it, the XML cookie information in the URL will cause an error.</span><span class="sxs-lookup"><span data-stu-id="6d47b-163">If you URI encode the value before you send it, the XML cookie information in the URL will cause an error.</span></span>

### <a name="retrieve-related-entities-by-expanding-navigation-properties"></a><span data-ttu-id="6d47b-164">Retrieve related entities by expanding navigation properties</span><span class="sxs-lookup"><span data-stu-id="6d47b-164">Retrieve related entities by expanding navigation properties</span></span>

<span data-ttu-id="6d47b-165">Use the **$expand** system query option in the navigation properties to control the data that is returned from related entities.</span><span class="sxs-lookup"><span data-stu-id="6d47b-165">Use the **$expand** system query option in the navigation properties to control the data that is returned from related entities.</span></span> <span data-ttu-id="6d47b-166">The following example demonstrates how to retrieve the contact for all the account records.</span><span class="sxs-lookup"><span data-stu-id="6d47b-166">The following example demonstrates how to retrieve the contact for all the account records.</span></span> <span data-ttu-id="6d47b-167">For the related contact records, we are only retrieving the `contactid` and `fullname`:</span><span class="sxs-lookup"><span data-stu-id="6d47b-167">For the related contact records, we are only retrieving the `contactid` and `fullname`:</span></span>

```JavaScript
Xrm.WebApi.retrieveMultipleRecords("account", "?$select=name&$top=3&$expand=primarycontactid($select=contactid,fullname)", 3).then(
    function success(result) {
        for (var i = 0; i < result.entities.length; i++) {
            console.log(result.entities[i]);
        }        
        // perform additional operations on retrieved records
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```


<span data-ttu-id="6d47b-168">For more examples of retrieving multiple records using Web API, see [Query Data using the Web API](../../../webapi/query-data-web-api.md).</span><span class="sxs-lookup"><span data-stu-id="6d47b-168">For more examples of retrieving multiple records using Web API, see [Query Data using the Web API](../../../webapi/query-data-web-api.md).</span></span>

 
### <a name="related-topics"></a><span data-ttu-id="6d47b-169">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="6d47b-169">Related topics</span></span>

[<span data-ttu-id="6d47b-170">Query Data using the Web API</span><span class="sxs-lookup"><span data-stu-id="6d47b-170">Query Data using the Web API</span></span>](../../../webapi/query-data-web-api.md)

[<span data-ttu-id="6d47b-171">Xrm.WebApi.retrieveRecord</span><span class="sxs-lookup"><span data-stu-id="6d47b-171">Xrm.WebApi.retrieveRecord</span></span>](retrieveRecord.md)

[<span data-ttu-id="6d47b-172">Xrm.WebApi</span><span class="sxs-lookup"><span data-stu-id="6d47b-172">Xrm.WebApi</span></span>](../xrm-webapi.md)




