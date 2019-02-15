---
title: Xrm.WebApi.online.execute (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/21/2018
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
ms.openlocfilehash: 46f7e652f36724ce939506bb0404f9823f61601f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385902"
---
# <a name="xrmwebapionlineexecute-client-api-reference"></a><span data-ttu-id="a198b-102">Xrm.WebApi.online.execute (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="a198b-102">Xrm.WebApi.online.execute (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/execute-description.md](../includes/execute-description.md)]

> [!NOTE]
> <span data-ttu-id="a198b-103">This method is supported only for the online mode ([Xrm.WebApi.online](../online.md)).</span><span class="sxs-lookup"><span data-stu-id="a198b-103">This method is supported only for the online mode ([Xrm.WebApi.online](../online.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="a198b-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="a198b-104">Syntax</span></span>

`Xrm.WebApi.online.execute(request).then(successCallback, errorCallback);`

## <a name="parameters"></a><span data-ttu-id="a198b-105">Tham số</span><span class="sxs-lookup"><span data-stu-id="a198b-105">Parameters</span></span>

<table style="width:100%">
<tr>
<th><span data-ttu-id="a198b-106">Tên</span><span class="sxs-lookup"><span data-stu-id="a198b-106">Name</span></span></th>
<th><span data-ttu-id="a198b-107">Loại</span><span class="sxs-lookup"><span data-stu-id="a198b-107">Type</span></span></th>
<th><span data-ttu-id="a198b-108">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="a198b-108">Required</span></span></th>
<th><span data-ttu-id="a198b-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a198b-109">Description</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="a198b-110">yêu cầu</span><span class="sxs-lookup"><span data-stu-id="a198b-110">request</span></span></td>
<td><span data-ttu-id="a198b-111">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="a198b-111">Object</span></span></td>
<td><span data-ttu-id="a198b-112">Có</span><span class="sxs-lookup"><span data-stu-id="a198b-112">Yes</span></span></td>
<td><p><span data-ttu-id="a198b-113">Object that will be passed to the Web API endpoint to execute an action, function, or CRUD request.</span><span class="sxs-lookup"><span data-stu-id="a198b-113">Object that will be passed to the Web API endpoint to execute an action, function, or CRUD request.</span></span> <span data-ttu-id="a198b-114">The object exposes a <b>getMetadata</b> method that lets you define the metadata for the action, function or CRUD request you want to execute.</span><span class="sxs-lookup"><span data-stu-id="a198b-114">The object exposes a <b>getMetadata</b> method that lets you define the metadata for the action, function or CRUD request you want to execute.</span></span> <span data-ttu-id="a198b-115">The <b>getMetadata</b> method has the following parameters:</span><span class="sxs-lookup"><span data-stu-id="a198b-115">The <b>getMetadata</b> method has the following parameters:</span></span></p>
<ul>
<li><span data-ttu-id="a198b-116"><b>boundParameter</b>: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="a198b-116"><b>boundParameter</b>: (Optional) String.</span></span> <span data-ttu-id="a198b-117">The name of the bound parameter for the action or function to execute.</span><span class="sxs-lookup"><span data-stu-id="a198b-117">The name of the bound parameter for the action or function to execute.</span></span>
<ul><li><span data-ttu-id="a198b-118">Specify <code>undefined</code> if you are executing a CRUD request.</span><span class="sxs-lookup"><span data-stu-id="a198b-118">Specify <code>undefined</code> if you are executing a CRUD request.</span></span></li>
<li><span data-ttu-id="a198b-119">Specify <code>null</code> if the action or function to execute is not bound to any entity.</span><span class="sxs-lookup"><span data-stu-id="a198b-119">Specify <code>null</code> if the action or function to execute is not bound to any entity.</span></span></li>
<li><span data-ttu-id="a198b-120">Specify <code>entity</code> in case the action or function to execute is bound to an entity.</span><span class="sxs-lookup"><span data-stu-id="a198b-120">Specify <code>entity</code> in case the action or function to execute is bound to an entity.</span></span> </li></ul>
<li><span data-ttu-id="a198b-121"><b>operationName</b>: (Optional).</span><span class="sxs-lookup"><span data-stu-id="a198b-121"><b>operationName</b>: (Optional).</span></span> <span data-ttu-id="a198b-122">String.</span><span class="sxs-lookup"><span data-stu-id="a198b-122">String.</span></span> <span data-ttu-id="a198b-123">Name of the action, function, or one of the following values if you are executing a CRUD request: &quot;Create&quot;, &quot;Retrieve&quot;, &quot;RetrieveMultiple&quot;, &quot;Update&quot;, or &quot;Delete&quot;.</span><span class="sxs-lookup"><span data-stu-id="a198b-123">Name of the action, function, or one of the following values if you are executing a CRUD request: &quot;Create&quot;, &quot;Retrieve&quot;, &quot;RetrieveMultiple&quot;, &quot;Update&quot;, or &quot;Delete&quot;.</span></span></li>
<li><span data-ttu-id="a198b-124"><b>operationType</b>: (Optional).</span><span class="sxs-lookup"><span data-stu-id="a198b-124"><b>operationType</b>: (Optional).</span></span> <span data-ttu-id="a198b-125">Số.</span><span class="sxs-lookup"><span data-stu-id="a198b-125">Number.</span></span> <span data-ttu-id="a198b-126">Indicates the type of operation you are executing; specify one of the following values:</span><span class="sxs-lookup"><span data-stu-id="a198b-126">Indicates the type of operation you are executing; specify one of the following values:</span></span>
<br/><code>0: Action</code>
<br/><code>1: Function</code>
<br/><code>2: CRUD</code></li>
<li><span data-ttu-id="a198b-127"><b>parameterTypes</b>: Object.</span><span class="sxs-lookup"><span data-stu-id="a198b-127"><b>parameterTypes</b>: Object.</span></span> <span data-ttu-id="a198b-128">The metadata for parameter types.</span><span class="sxs-lookup"><span data-stu-id="a198b-128">The metadata for parameter types.</span></span> <span data-ttu-id="a198b-129">The object has the following attributes:</span><span class="sxs-lookup"><span data-stu-id="a198b-129">The object has the following attributes:</span></span>
<ul>
<li><span data-ttu-id="a198b-130"><b>enumProperties</b>: (Optional) Object.</span><span class="sxs-lookup"><span data-stu-id="a198b-130"><b>enumProperties</b>: (Optional) Object.</span></span> <span data-ttu-id="a198b-131">The metadata for enum types.</span><span class="sxs-lookup"><span data-stu-id="a198b-131">The metadata for enum types.</span></span> <span data-ttu-id="a198b-132">The object has two string attributes: <b>name</b> and <b>value</b></span><span class="sxs-lookup"><span data-stu-id="a198b-132">The object has two string attributes: <b>name</b> and <b>value</b></span></span></li>
<li><span data-ttu-id="a198b-133"><b>structuralProperty</b>: Number.</span><span class="sxs-lookup"><span data-stu-id="a198b-133"><b>structuralProperty</b>: Number.</span></span> <span data-ttu-id="a198b-134">The category of the parameter type.</span><span class="sxs-lookup"><span data-stu-id="a198b-134">The category of the parameter type.</span></span> <span data-ttu-id="a198b-135">Specify one of the following values:</span><span class="sxs-lookup"><span data-stu-id="a198b-135">Specify one of the following values:</span></span>
<br/><code>0: Unknown</code>
<br/><code>1: PrimitiveType</code>
<br/><code>2: ComplexType</code>
<br/><code>3: EnumerationType</code>
<br/><code>4: Collection</code>
<br/><code>5: EntityType</code></li>
<li><span data-ttu-id="a198b-136"><b>typeName</b>: String.</span><span class="sxs-lookup"><span data-stu-id="a198b-136"><b>typeName</b>: String.</span></span> <span data-ttu-id="a198b-137">The fully qualified name of the parameter type.</span><span class="sxs-lookup"><span data-stu-id="a198b-137">The fully qualified name of the parameter type.</span></span>
</ul>
</li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a198b-138">successCallback</span><span class="sxs-lookup"><span data-stu-id="a198b-138">successCallback</span></span></td>
<td><span data-ttu-id="a198b-139">Hàm</span><span class="sxs-lookup"><span data-stu-id="a198b-139">Function</span></span></td>
<td><span data-ttu-id="a198b-140">Không</span><span class="sxs-lookup"><span data-stu-id="a198b-140">No</span></span></td>
<td><p><span data-ttu-id="a198b-141">A function to call when operation is executed successfully.</span><span class="sxs-lookup"><span data-stu-id="a198b-141">A function to call when operation is executed successfully.</span></span> <span data-ttu-id="a198b-142">A response object is passed to the function with the following attributes:</span><span class="sxs-lookup"><span data-stu-id="a198b-142">A response object is passed to the function with the following attributes:</span></span></p>
<ul>
<li><span data-ttu-id="a198b-143"><b>body</b>: (Optional).</span><span class="sxs-lookup"><span data-stu-id="a198b-143"><b>body</b>: (Optional).</span></span> <span data-ttu-id="a198b-144">Object.</span><span class="sxs-lookup"><span data-stu-id="a198b-144">Object.</span></span> <span data-ttu-id="a198b-145">Response body.</span><span class="sxs-lookup"><span data-stu-id="a198b-145">Response body.</span></span></li>
<li><span data-ttu-id="a198b-146"><b>headers</b>: Object.</span><span class="sxs-lookup"><span data-stu-id="a198b-146"><b>headers</b>: Object.</span></span> <span data-ttu-id="a198b-147">Response headers.</span><span class="sxs-lookup"><span data-stu-id="a198b-147">Response headers.</span></span></li>
<li><span data-ttu-id="a198b-148"><b>ok</b>: Boolean.</span><span class="sxs-lookup"><span data-stu-id="a198b-148"><b>ok</b>: Boolean.</span></span> <span data-ttu-id="a198b-149">Indicates whether the request was successful.</span><span class="sxs-lookup"><span data-stu-id="a198b-149">Indicates whether the request was successful.</span></span></li>
<li><span data-ttu-id="a198b-150"><b>status</b>: Number.</span><span class="sxs-lookup"><span data-stu-id="a198b-150"><b>status</b>: Number.</span></span> <span data-ttu-id="a198b-151">Numeric value in the response status code.</span><span class="sxs-lookup"><span data-stu-id="a198b-151">Numeric value in the response status code.</span></span> <span data-ttu-id="a198b-152">For example: <b>200</b></span><span class="sxs-lookup"><span data-stu-id="a198b-152">For example: <b>200</b></span></span></li>
<li><span data-ttu-id="a198b-153"><b>statusText</b>: String.</span><span class="sxs-lookup"><span data-stu-id="a198b-153"><b>statusText</b>: String.</span></span> <span data-ttu-id="a198b-154">Description of the response status code.</span><span class="sxs-lookup"><span data-stu-id="a198b-154">Description of the response status code.</span></span> <span data-ttu-id="a198b-155">For example: <b>OK</b></span><span class="sxs-lookup"><span data-stu-id="a198b-155">For example: <b>OK</b></span></span></li>
<li><span data-ttu-id="a198b-156"><b>type</b>: String.</span><span class="sxs-lookup"><span data-stu-id="a198b-156"><b>type</b>: String.</span></span> <span data-ttu-id="a198b-157">Response type.</span><span class="sxs-lookup"><span data-stu-id="a198b-157">Response type.</span></span> <span data-ttu-id="a198b-158">Values are: the empty string (default), &quot;arraybuffer&quot;, &quot;blob&quot;, &quot;document&quot;, &quot;json&quot;, and &quot;text&quot;.</span><span class="sxs-lookup"><span data-stu-id="a198b-158">Values are: the empty string (default), &quot;arraybuffer&quot;, &quot;blob&quot;, &quot;document&quot;, &quot;json&quot;, and &quot;text&quot;.</span></span></b></li>
<li><span data-ttu-id="a198b-159"><b>url</b>: String.</span><span class="sxs-lookup"><span data-stu-id="a198b-159"><b>url</b>: String.</span></span> <span data-ttu-id="a198b-160">Request URL of the action, function, or CRUD request that was sent to the Web API endpoint.</span><span class="sxs-lookup"><span data-stu-id="a198b-160">Request URL of the action, function, or CRUD request that was sent to the Web API endpoint.</span></span></b></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a198b-161">errorCallback</span><span class="sxs-lookup"><span data-stu-id="a198b-161">errorCallback</span></span></td>
<td><span data-ttu-id="a198b-162">Hàm</span><span class="sxs-lookup"><span data-stu-id="a198b-162">Function</span></span></td>
<td><span data-ttu-id="a198b-163">Không</span><span class="sxs-lookup"><span data-stu-id="a198b-163">No</span></span></td>
<td><span data-ttu-id="a198b-164">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="a198b-164">A function to call when the operation fails.</span></span></td>
</tr>
</table>

## <a name="return-value"></a><span data-ttu-id="a198b-165">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="a198b-165">Return Value</span></span>

<span data-ttu-id="a198b-166">On success, returns a promise object with the attributes specified earlier in the description of **successCallback** function.</span><span class="sxs-lookup"><span data-stu-id="a198b-166">On success, returns a promise object with the attributes specified earlier in the description of **successCallback** function.</span></span>

## <a name="examples"></a><span data-ttu-id="a198b-167">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="a198b-167">Examples</span></span>

### <a name="execute-an-action"></a><span data-ttu-id="a198b-168">Execute an action</span><span class="sxs-lookup"><span data-stu-id="a198b-168">Execute an action</span></span>

<span data-ttu-id="a198b-169">The following example demonstrates how to execute the <xref:Microsoft.Dynamics.CRM.WinOpportunity> action.</span><span class="sxs-lookup"><span data-stu-id="a198b-169">The following example demonstrates how to execute the <xref:Microsoft.Dynamics.CRM.WinOpportunity> action.</span></span> <span data-ttu-id="a198b-170">The request object is created based on the action definition here: [Unbound actions](../../../../webapi/use-web-api-actions.md#bkmk_unboundActions)</span><span class="sxs-lookup"><span data-stu-id="a198b-170">The request object is created based on the action definition here: [Unbound actions](../../../../webapi/use-web-api-actions.md#bkmk_unboundActions)</span></span>

```JavaScript
var Sdk = window.Sdk || {};
/**
 * Request to win an opportunity
 * @param {Object} opportunityClose - The opportunity close activity associated with this state change.
 * @param {number} status - Status of the opportunity.
 */
Sdk.WinOpportunityRequest = function (opportunityClose, status) {
    this.OpportunityClose = opportunityClose;
    this.Status = status;

    this.getMetadata = function () {
        return {
            boundParameter: null,
            parameterTypes: {
                "OpportunityClose": {
                    "typeName": "mscrm.opportunityclose",
                    "structuralProperty": 5 // Entity Type
                },
                "Status": {
                    "typeName": "Edm.Int32",
                    "structuralProperty": 1 // Primitive Type
                }
            },
            operationType: 0, // This is an action. Use '1' for functions and '2' for CRUD
            operationName: "WinOpportunity",
        };
    };
};


var opportunityClose = {
    "opportunityid@odata.bind": "/opportunities(c60e0283-5bf2-e311-945f-6c3be5a8dd64)",
    "description": "Product and maintainance for 2018",
    "subject": "Contract for 2018"
}

// Construct a request object from the metadata
var winOpportunityRequest = new Sdk.WinOpportunityRequest(opportunityClose, 3);

// Use the request object to execute the function
Xrm.WebApi.online.execute(winOpportunityRequest).then(
    function (result) {
        if (result.ok) {
            console.log("Status: %s %s", result.status, result.statusText);
            // perform other operations as required;
        }
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```


### <a name="execute-a-function"></a><span data-ttu-id="a198b-171">Execute a function</span><span class="sxs-lookup"><span data-stu-id="a198b-171">Execute a function</span></span>

<span data-ttu-id="a198b-172">The following example demonstrates how to execute the <xref:Microsoft.Dynamics.CRM.WhoAmI> function:</span><span class="sxs-lookup"><span data-stu-id="a198b-172">The following example demonstrates how to execute the <xref:Microsoft.Dynamics.CRM.WhoAmI> function:</span></span>

```JavaScript
var Sdk = window.Sdk || {};
/**
 * Request to execute WhoAmI function
 */
Sdk.WhoAmIRequest = function () {};
Sdk.WhoAmIRequest.prototype.getMetadata = function () {
    return {
        boundParameter: null,
        parameterTypes: {},
        operationType: 1, // This is a function. Use '0' for actions and '2' for CRUD
        operationName: "WhoAmI",
    };
};

// Construct a request object from the metadata
var whoAmIRequest = new Sdk.WhoAmIRequest();

// Use the request object to execute the function
Xrm.WebApi.online.execute(whoAmIRequest).then(
    function (result) {
        if (result.ok) {
            console.log("Status: %s %s", result.status, result.statusText);
            result.json().then(
                function (response) {
                    console.log("User Id: %s", response.UserId);
                    // perform other operations as required;
                });
        }
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```

 
### <a name="related-topics"></a><span data-ttu-id="a198b-173">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="a198b-173">Related topics</span></span>

[<span data-ttu-id="a198b-174">Xrm.WebApi.online</span><span class="sxs-lookup"><span data-stu-id="a198b-174">Xrm.WebApi.online</span></span>](../online.md)




