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
# <a name="deleterecord-client-api-reference"></a>deleteRecord (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/deleteRecord-description.md](./includes/deleteRecord-description.md)] 

## <a name="syntax"></a>Cú pháp

`Xrm.WebApi.deleteRecord(entityLogicalName, id).then(successCallback, errorCallback);`

## <a name="parameters"></a>Tham số

<table style="width:100%">
<tr>
<th>Tên</th>
<th>Loại</th>
<th>Bắt buộc</th>
<th>Mô tả</th>
</tr>
<tr>
<td>entityLogicalName</td>
<td>Chuỗi</td>
<td>Có</td>
<td>The entity logical name of the record you want to delete. For example: &quot;account&quot;. </td>
</tr>
<tr>
<td>ID</td>
<td>Chuỗi</td>
<td>Có</td>
<td>GUID of the entity record you want to delete.</td>
</tr>
<tr>
<td>successCallback</td>
<td>Hàm</td>
<td>Không</td>
<td><p>A function to call when a record is deleted. An object with the following properties will be passed to identify the deleted record:</p>
<ul>
<li><b>entityType</b>: String. The entity type of the record.</li>
<li><b>id</b>: String. GUID of the record.</li>
<li><b>name</b>: String. Name of the record.</li>
</ul></td>
</tr>
<tr>
<td>errorCallback</td>
<td>Hàm</td>
<td>Không</td>
<td>A function to call when the operation fails.</td>
</tr>
</table>

## <a name="return-value"></a>Giá trị trả lại

On success, returns a promise object containing the attributes specified earlier in the description of the **successCallback** parameter.

## <a name="examples"></a>Ví dụ

These examples use some of the same request objects as demonstrated in [Update and delete entities using the Web API](../../../webapi/update-delete-entities-using-web-api.md) to define the data object for updating an entity record.

Deletes an account with record ID = 5531d753-95af-e711-a94e-000d3a11e605.

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
 
### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.WebApi](../xrm-webapi.md)




