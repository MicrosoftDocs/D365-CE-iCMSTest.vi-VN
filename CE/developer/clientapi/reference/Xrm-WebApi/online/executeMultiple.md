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
# <a name="xrmwebapionlineexecutemultiple-client-api-reference"></a>Xrm.WebApi.online.executeMultiple (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/executeMultiple-description.md](../includes/executeMultiple-description.md)]

> [!NOTE]
> This method is supported only for the online mode ([Xrm.WebApi.online](../online.md)).

If you want to execute multiple requests in a transaction, you must pass in a change set as a parameter to this method. [Change sets](../../../../webapi/execute-batch-operations-using-web-api.md#bkmk_ChangeSets) represent a collection of operations that are executed in a transaction. You can also pass in individual requests and change sets together as parameters to this method.

> [!NOTE]
> You cannot include read operations (retrieve, retrieve multiple, and Web API functions) as part of a change set; this is as per the OData v4 specifications.

## <a name="syntax"></a>Cú pháp

**Execute multiple requests:**

```JavaScript
var requests = [req1, req2, req3];
Xrm.WebApi.online.executeMultiple(requests).then(successCallback, errorCallback);
```

**Execute multiple requests in a transaction:**

In this case, `req1`, `req2`, and `req3` will be executed in transaction.

```JavaScript
var changeSet = [req1, req2, req3];
var requests = [changeSet];
Xrm.WebApi.online.executeMultiple(requests).then(successCallback, errorCallback);
```


**Execute a mix of individual requests and multiple requests in a transaction:**

In this case, `req1`, `req2`, and `req3` will be executed in transaction, but `req4` and `req5` will be executed individually.

```JavaScript
var changeSet = [req1, req2, req3];
var requests = [req4, req5, changeset];
Xrm.WebApi.online.executeMultiple(requests).then(successCallback, errorCallback);
```

## <a name="parameters"></a>Tham số

<table style="width:100%">
<tr>
<th>Tên</th>
<th>Loại</th>
<th>Bắt buộc</th>
<th>Mô tả</th>
</tr>
<tr>
<td>requests</td>
<td>Array of objects</td>
<td>Có</td>
<td><p>An array of one of one of the following types:</p>
<ul>
<li>objects where each object is an action, function, or CRUD request that you want to execute against the Web API endpoint. Each object exposes a <b>getMetadata</b> method that lets you define the metadata for the action, function or CRUD request you want to execute. This is the same object that you pass in the <code>execute</code> method. For information about the object, see <a href="execute.md">execute</a>.</li>
<li>Change set (an array of objects), where each object in the change set is as defined above. In this case, all the request objects specified in the change set will get executed in a transaction.</li>
</ul>
<p>See request examples earlier in the <strong>Syntax</strong> section for more information.</p>
</td>
</tr>
<tr>
<td>successCallback</td>
<td>Hàm</td>
<td>Không</td>
<td><p>A function to call when operation is executed suucessfully. An array of response objects are passed to the function where weach response object has the following attributes:</p>
<ul>
<li><b>body</b>: (Optional). Object. Response body.</li>
<li><b>headers</b>: Object. Response headers.</li>
<li><b>ok</b>: Boolean. Indicates whether the request was successful.</li>
<li><b>status</b>: Number. Numeric value in the response status code. For example: <b>200</b></li>
<li><b>statusText</b>: String. Description of the response status code. For example: <b>OK</b></li>
<li><b>type</b>: String. Response type. Values are: the empty string (default), &quot;arraybuffer&quot;, &quot;blob&quot;, &quot;document&quot;, &quot;json&quot;, and &quot;text&quot;.</b></li>
<li><b>url</b>: String. Request URL of the action, function, or CRUD request that was sent to the Web API endpoint.</b></li>
</ul>
</td>
</tr>
<tr>
<td>errorCallback</td>
<td>Hàm</td>
<td>Không</td>
<td>A function to call when the operation fails.</td>
</tr>
</table>

## <a name="return-value"></a>Giá trị trả lại

On success, returns a promise containing an array of objects with the attributes specified earlier in the description of **successCallback** function.

### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.WebApi.online](../online.md)

