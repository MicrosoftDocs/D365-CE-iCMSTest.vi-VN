---
title: Create an entity using the Web API (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Read how to create a POST request to send data to create an entity on Dynamics 365 for Customer Engagement using the Web API
ms.custom: ''
ms.date: 11/16/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 244259ca-2fbc-4fd4-9a74-6166e6683355
caps.latest.revision: 51
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bfc5c70b52602111951e4165d2903f17b366aa63
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386740"
---
# <a name="create-an-entity-using-the-web-api"></a>Create an entity using the Web API

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

Use a POST request to send data to create an entity. You can create multiple related entities in a single operation using ‘deep insert’. You also need to know how to set values to associate a new entity to existing entities using the @odata.bind annotation.  

> [!NOTE]
> For information about how to create and update the entity metadata using the Web API, see [Create and update entity definitions using the Web API](create-update-entity-definitions-using-web-api.md).

<a name="bkmk_basicCreate"></a>

## <a name="basic-create"></a>Basic Create

 This example creates a new account entity. The response `OData-EntityId` header contains the Uri of the created entity.

 **Yêu cầu**

```http

POST [Organization URI]/api/data/v9.0/accounts HTTP/1.1
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "name": "Sample Account",
    "creditonhold": false,
    "address1_latitude": 47.639583,
    "description": "This is the description of the sample account",
    "revenue": 5000000,
    "accountcategorycode": 1
}
```

 **Phản hồi**

```http

HTTP/1.1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.0/accounts(7eb682f1-ca75-e511-80d4-00155d2a68d1)
```

 To create a new entity you must identify the valid property names and types. For all system entities and attributes, you can find this information in the topic for that entity in the [Web API EntityType Reference](../about-entity-reference.md). For custom entities or attributes, refer to the definition of that entity in the [CSDL metadata document](web-api-types-operations.md#bkmk_csdl). [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Entity types](web-api-types-operations.md#bkmk_entityTypes)

<a name="bkmk_CreateRelated"></a>

## <a name="create-related-entities-in-one-operation"></a>Create related entities in one operation

 You can create entities related to each other by defining them as navigation properties values. This is known as *deep insert*.

 As with a basic create, the response `OData-EntityId` header contains the Uri of the created entity. The URIs for the related entities created aren’t returned.

 For example, the following request body posted to the `Account` entity set will create a total of four new entities in the context of creating an account.

- A contact is created because it is defined as an object property of the single-valued navigation property `primarycontactid`.

- An opportunity is created because it is defined as an object within an array that is set to the value of a collection-valued navigation property `opportunity_customer_accounts`.

- A task is created because it is defined an object within an array that is set to the value of a collection-valued navigation property `Opportunity_Tasks`.

**Yêu cầu**

```http
POST [Organization URI]/api/data/v9.0/accounts HTTP/1.1
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

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
```

**Phản hồi**

 ```http

HTTP/1.1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.0/accounts(3c6e4b5f-86f6-e411-80dd-00155d2a68cb)
```

<a name="bkmk_associateOnCreate"></a>

## <a name="associate-entities-on-create"></a>Associate entities on create

 To associate new entities to existing entities when they are created you must set the value of single-valued navigation properties using the `@odata.bind` annotation.

 The following request body posted to the accounts entity set will create a new account associated with an existing contact with the `contactid` value of 00000000-0000-0000-0000-000000000001.

**Yêu cầu**

```http

POST [Organization URI]/api/data/v9.0/accounts HTTP/1.1
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
"name":"Sample Account",
"primarycontactid@odata.bind":"/contacts(00000000-0000-0000-0000-000000000001)"
}
```

**Phản hồi**

```http

HTTP/1.1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000002)
```

> [!NOTE]
> Associating entities this way using a collection-valued navigation property is not supported by the Web API.

<a name="bkmk_SuppressDuplicateDetection"></a>

## <a name="check-for-duplicate-records"></a>Check for Duplicate records

 By default, duplicate detection is suppressed when you are creating records using the Web API. You must include the `MSCRM.SuppressDuplicateDetection: false` header with your POST request to enable duplicate detection . Duplicate detection only applies when the organization has enabled duplicate detection, the entity is enabled for duplicate detection, and there are active duplicate detection rules being applied. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Detect duplicate data for developers](../detect-duplicate-data-for-developers.md)

 See [Manage duplicate detection during Create and Update operations using Web API](manage-duplicate-detection-create-update.md#bkmk_create) for more information on how to check for duplicate records during Create operation.

<a name="bkmk_initializefrom"></a>

## <a name="create-a-new-entity-from-another-entity"></a>Create a new entity from another entity

Use `InitializeFrom function` to create a new record in the context of an existing record where a mapping exists between the entities to which the records belong. 

The following example shows how to create an account record using the attribute values of an existing record of account entity with `accountid` value equal to c65127ed-2097-e711-80eb-00155db75426.

**Yêu cầu**

```http
GET [Organization URI]/api/data/v9.0/InitializeFrom(EntityMoniker=@p1,TargetEntityName=@p2,TargetFieldType=@p3)?@p1={'@odata.id':'accounts(c65127ed-2097-e711-80eb-00155db75426)'}&@p2='account'&@p3=Microsoft.Dynamics.CRM.TargetFieldType'ValidForCreate' HTTP/1.1
If-None-Match: null
OData-Version: 4.0
OData-MaxVersion: 4.0
Content-Type: application/json
Accept: application/json
```

**Phản hồi**

```json
{
        "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#accounts/$entity",
        "@odata.type": "#Microsoft.Dynamics.CRM.account",
        "parentaccountid@odata.bind": "accounts(c65127ed-2097-e711-80eb-00155db75426)",
        "transactioncurrencyid@odata.bind": "transactioncurrencies(732e87e1-1d96-e711-80e4-00155db75426)",
        "address1_line1":"123 Maple St.",
        "address1_city":"Seattle",
        "address1_country":"United States of America"
}
```

The response received from InitializeFrom request consists of values of mapped attributes between the source entity and target entity and the GUID of parent record. The attribute mapping between entities that have an entity relationship is different for different entity sets and is customizable, so the response from InitializeFrom function request may vary for different entities and organizations. When this response is passed in the body of create request of the new record, these attribute values are replicated in the new record. The values of custom mapped attributes also get set in the new record during the process.

> [!NOTE]
> To determine whether two entities can be mapped, use this query:  
GET [Organization URI]/api/data/v9.0/entitymaps?$select=sourceentityname,targetentityname&$orderby=sourceentityname

Other attribute values can also be set and/or modified for the new record by adding them in the JSON request body, as shown in the example below.

```http
POST [Organization URI]/api/data/v9.0/accounts HTTP/1.1
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

    {
        "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#accounts/$entity",
        "@odata.type": "#Microsoft.Dynamics.CRM.account",
        "parentaccountid@odata.bind": "accounts(c65127ed-2097-e711-80eb-00155db75426)",
        "transactioncurrencyid@odata.bind": "transactioncurrencies(732e87e1-1d96-e711-80e4-00155db75426)",
        "name":"Contoso Ltd",
        "numberofemployees":"200",
        "address1_line1":"100 Maple St.",
        "address1_city":"Seattle",
        "address1_country":"United States of America",
        "fax":"73737"
    }
}
```

<a name="bkmk_createWithDataReturned"></a>

## <a name="create-with-data-returned"></a>Create with data returned

> [!NOTE]
> This capability was added with [!INCLUDE[pn_crm_8_2_0_both](../../includes/pn-crm-8-2-0-both.md)].

 You can compose your POST request so that data from the created record will be returned with a status of 201 (Created).  To get his result, you must use the `return=representation` preference in the request headers.

 To control which properties are returned, append the `$select` query option to the URL to the entity set.  The `$expand` query option will be ignored if used.

 When an entity is created in this way the `OData-EntityId` header containing the URI to the created record is not returned.

 This example creates a new account entity and returns the requested data in the response.

**Yêu cầu**

 ```http

POST [Organization URI]/api/data/v9.0/accounts?$select=name,creditonhold,address1_latitude,description,revenue,accountcategorycode,createdon HTTP/1.1
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json
Content-Type: application/json; charset=utf-8
Prefer: return=representation

{
    "name": "Sample Account",
    "creditonhold": false,
    "address1_latitude": 47.639583,
    "description": "This is the description of the sample account",
    "revenue": 5000000,
    "accountcategorycode": 1
}
```

**Phản hồi**

```http

HTTP/1.1 201 Created
Content-Type: application/json; odata.metadata=minimal
Preference-Applied: return=representation
OData-Version: 4.0

{
    "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#accounts/$entity",
    "@odata.etag": "W/\"536530\"",
    "accountid": "d6f193fc-ce85-e611-80d8-00155d2a68de",
    "accountcategorycode": 1,
    "description": "This is the description of the sample account",
    "address1_latitude": 47.63958,
    "creditonhold": false,
    "name": "Sample Account",
    "createdon": "2016-09-28T22:57:53Z",
    "revenue": 5000000.0000,
    "_transactioncurrencyid_value": "048dddaa-6f7f-e611-80d3-00155db5e0b6"
}
```

### <a name="see-also"></a>Xem thêm

 [Web API Basic Operations Sample (C#)](web-api-basic-operations-sample-csharp.md)<br />
 [Web API Basic Operations Sample (Client-side JavaScript)](web-api-basic-operations-sample-client-side-javascript.md)<br />
 <xref href="Microsoft.Dynamics.CRM.InitializeFrom?text=InitializeFrom Function" />  
 [Perform operations using the Web API](perform-operations-web-api.md)<br />
 [Compose Http requests and handle errors](compose-http-requests-handle-errors.md)<br />
 [Query Data using the Web API](query-data-web-api.md)<br />
 [Retrieve an entity using the Web API](retrieve-entity-using-web-api.md)<br />
 [Cập nhật và xóa các thực thể bằng cách sử dụng Web API](update-delete-entities-using-web-api.md)<br />
 [Associate and disassociate entities using the Web API](associate-disassociate-entities-using-web-api.md)<br />
 [Use Web API functions](use-web-api-functions.md)<br />
 [Sử dụng hành động Web API](use-web-api-actions.md)<br />
 [Execute batch operations using the Web API](execute-batch-operations-using-web-api.md)<br />
 [Impersonate another user using the Web API](impersonate-another-user-web-api.md)<br />
 [Perform conditional operations using the Web API](perform-conditional-operations-using-web-api.md)<br />
