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
# <a name="createrecord-client-api-reference"></a>createRecord (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/createRecord-description.md](./includes/createRecord-description.md)] 

## <a name="syntax"></a>Cú pháp

`Xrm.WebApi.createRecord(entityLogicalName, data).then(successCallback, errorCallback);`

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
<td>Logical name of the entity you want to create. For example: &quot;account&quot;.</td>
</tr>
<tr>
<td>dữ liệu</td>
<td>Đối tượng</td>
<td>Có</td>
<td><p>A JSON object defining the attributes and values for the new entity record.</p>
<p>See examples later in this topic to see how you can define the <code>data</code> object for various create scenarios.</td>
</tr>
<tr>
<td>successCallback</td>
<td>Hàm</td>
<td>Không</td>
<td><p>A function to call when a record is created. An object with the following properties will be passed to identify the new record:</p>
<ul>
<li><b>entityType</b>: String. The entity logical name of the new record.</li>
<li><b>id</b>: String. GUID of the new record.</li>
</ul></td>
</tr>
<tr>
<td>errorCallback</td>
<td>Hàm</td>
<td>Không</td>
<td>A function to call when the operation fails. An object with the following properties will be passed:
<ul>
<li><b>errorCode</b>: Number. The error code.</li>
<li><b>message</b>: String. An error message describing the issue.</li>
</ul></td>
</tr>
</table>

## <a name="return-value"></a>Giá trị trả lại

On success, returns a promise object containing the attributes specified earlier in the description of the **successCallback** parameter.

## <a name="examples"></a>Ví dụ

These examples use the same request objects as demonstrated in [Create an entity using the Web API](../../../webapi/create-entity-web-api.md) to define the data object for creating an entity record.

### <a name="basic-create"></a>Basic create 

Creates a sample account record.

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

### <a name="create-related-entity-records-along-with-the-primary-record"></a>Create related entity records along with the primary record

 You can create entities related to each other by defining them as navigation properties values. This is known as *deep insert*. In this example, we will create a sample account record along with the primary contact record and an associated opportunity record.

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

### <a name="associate-entities-on-creating-new-records"></a>Associate entities on creating new records

To associate new entity records to existing entity records, set the value of single-valued navigation properties using the `@odata.bind` annotation. However, for mobile clients in the offline mode, you cannot use the `@odata.bind` annotation, and instead have to pass a **lookup** object (**logicalname** and **id**) pointing to the target record. Here are code examples for both the scenarios: 


**For online scenario (connected to server)**

The following example creates an account record, and associates it to an existing contact record to set the latter as the primary contact for the new account record:

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

**For mobile offline scenario**

Here is the updated sample code to create an account record, and associate it to an existing contact record to set the latter as the primary contact for the new account record from mobile clients when working in the offline mode:

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
 
### <a name="related-topics"></a>Chủ đề liên quan

[Create an entity using the Web API](../../../webapi/create-entity-web-api.md)

[Xrm.WebApi](../xrm-webapi.md)
