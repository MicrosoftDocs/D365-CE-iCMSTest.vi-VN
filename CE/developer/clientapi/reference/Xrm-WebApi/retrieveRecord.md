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
# <a name="retrieverecord-client-api-reference"></a>retrieveRecord (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/retrieveRecord-description.md](./includes/retrieveRecord-description.md)] 

## <a name="syntax"></a>Cú pháp

`Xrm.WebApi.retrieveRecord(entityLogicalName, id, options).then(successCallback, errorCallback);`

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
<td>The entity logical name of the record you want to retrieve. For example: &quot;account&quot;.</td>
</tr>
<tr>
<td>ID</td>
<td>Chuỗi</td>
<td>Có</td>
<td>GUID of the entity record you want to retrieve.</td>
</tr>
<tr>
<td>tùy chọn</td>
<td>Chuỗi</td>
<td>Không</td>
<td><p>OData system query options, <b>$select</b> and <b>$expand</b>, to retrieve your data.</p>
<ul><li>Use the <b>$select</b> system query option to limit the properties returned by including a comma-separated list of property names. This is an important performance best practice. If properties aren’t specified using <b>$select</b>, all properties will be returned.</li>
<li>Use the <b>$expand</b> system query option to control what data from related entities is returned. If you just include the name of the navigation property, you’ll receive all the properties for related records. You can limit the properties returned for related records using the <b>$select</b> system query option in parentheses after the navigation property name. Use this for both <i>single-valued</i> and <i>collection-valued</i> navigation properties.</li>
</ul>
<p>You specify the query options starting with <code>?</code>. You can also specify multiple query options by using <code>&amp;</code> to separate the query options. Ví dụ:</p>
<code>?$select=name&amp;$expand=primarycontactid($select=contactid,fullname)</code>
<p>See examples later in this topic to see how you can define the <code>options</code> parameter for various retrieve scenarios.</td>
</tr>
<tr>
<td>successCallback</td>
<td>Hàm</td>
<td>Không</td>
<td><p>A function to call when a record is retrieved. A JSON object with the retrieved properties and values will be passed to the function.</p>
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

On success, returns a promise containing a JSON object with the retrieved attributes and their values.

## <a name="examples"></a>Ví dụ

### <a name="basic-retrieve"></a>Basic retrieve 

Retrieves the name and revenue of an account record with record ID = 5531d753-95af-e711-a94e-000d3a11e605.

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

The above example displays the following in your console; you might see other values depending on your data:

`Retrieved values: Name: Sample Account, Revenue: 5000000`

### <a name="retrieve-related-entities-for-an-entity-instance-by-expanding-single-valued-navigation-properties"></a>Retrieve related entities for an entity instance by expanding single-valued navigation properties

 The following example demonstrates how to retrieve the contact for an account record with record ID = a8a19cdd-88df-e311-b8e5-6c3be5a8b200. For the related contact record, we are only retrieving the **contactid** and **fullname** properties.

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

The above example displays the following in your console; you might see other values depending on your data:

`Retrieved values: Name: Adventure Works, Primary Contact ID: 49a0e5b9-88df-e311-b8e5-6c3be5a8b200, Primary Contact Name: Adrian Dumitrascu`

 
### <a name="related-topics"></a>Chủ đề liên quan

[Xrm.WebApi.retrieveMultipleRecords](retrieveMultipleRecords.md)

[Xrm.WebApi](../xrm-webapi.md)



