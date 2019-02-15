---
title: Update and delete entities using the Web API (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how to perform update and delete operations on entities using the Web API
ms.custom: ''
ms.date: 05/09/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 694889fd-2b85-43a0-97bc-1e760695db31
caps.latest.revision: 17
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 33abefb0225fa67bddf0727aa87af433aaea63d8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387848"
---
# <a name="update-and-delete-entities-using-the-web-api"></a>Update and delete entities using the Web API

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

Operations to modify data are a core part of the Web API. In addition to a simple update and delete, you can perform operations on single attributes and compose *upsert* requests that will either update or insert an entity depending on whether it exists.  

> [!NOTE]
>  The metadata that defines entities is updated in a different way. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Create and update model entities using the Web API](create-update-entity-definitions-using-web-api.md)  

<a name="bkmk_update"></a>

## <a name="basic-update"></a>Basic update

 Update operations use the HTTP PATCH verb. Pass a JSON object containing the properties you want to update to the URI that represents the entity. A response with a status of 204 will be returned if the update is successful.  

 This example updates an existing account record with the `accountid` value of 00000000-0000-0000-0000-000000000001.  

> [!IMPORTANT]
>  When updating an entity, only include the properties you are changing in the request body. Simply updating the properties of an entity that you previously retrieved, and including that JSON in your request, will update each property even though the value is the same. This can cause system events that can trigger business logic that expects that the values have changed. This can cause properties to appear to have been updated in auditing data when in fact they haven’t actually changed.

 **Yêu cầu**

```http
PATCH [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001) HTTP/1.1  
Content-Type: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  

{  
    "name": "Updated Sample Account ",  
    "creditonhold": true,  
    "address1_latitude": 47.639583,  
    "description": "This is the updated description of the sample account",  
    "revenue": 6000000,  
    "accountcategorycode": 2  
}  
```  

 **Phản hồi**

```http
HTTP/1.1 204 No Content  
OData-Version: 4.0  
```  

> [!NOTE]
>  See [Associate entities on update](associate-disassociate-entities-using-web-api.md#bkmk_Associateentitiesonupdate) for information about associating entities on update.  

<a name="bkmk_updateWithDataReturned"></a>

## <a name="update-with-data-returned"></a>Update with data returned

> [!NOTE]
>  This capability was added with [!INCLUDE[pn_crm_8_2_0_both](../../includes/pn-crm-8-2-0-both.md)].  

 To retrieve data from an entity you are updating you can compose your PATCH request so that data from the created record will be returned with a status of 200 (OK).  To get his result, you must use the `return=representation` preference in the request headers.  

 To control which properties are returned, append the `$select` query option to the URL to the entity set.  The `$expand` query option will be ignored if used.  

 This example updates an account entity and returns the requested data in the response.  

 **Yêu cầu**

```http
PATCH [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)?$select=name,creditonhold,address1_latitude,description,revenue,accountcategorycode,createdon HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
Prefer: return=representation  

{"name":"Updated Sample Account"}  
```  

 **Phản hồi** 

```http
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
Preference-Applied: return=representation  
OData-Version: 4.0  

{  
    "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#accounts/$entity",  
    "@odata.etag": "W/\"536537\"",  
    "accountid": "00000000-0000-0000-0000-000000000001",  
    "accountcategorycode": 1,  
    "description": "This is the description of the sample account",  
    "address1_latitude": 47.63958,  
    "creditonhold": false,  
    "name": "Updated Sample Account",  
    "createdon": "2016-09-28T23:14:00Z",  
    "revenue": 5000000.0000,  
    "_transactioncurrencyid_value": "048dddaa-6f7f-e611-80d3-00155db5e0b6"  
}  
```  

<a name="bkmk_updateSingleProperty"></a> 

## <a name="update-a-single-property-value"></a>Update a single property value  

 When you want to update only a single property value use a PUT request with the property name appended to the Uri of the entity.  

 The following example updates the name property of an existing account entity with the `accountid` value of 00000000-0000-0000-0000-000000000001.  

 **Yêu cầu**  

```http
PUT [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)/name HTTP/1.1  
Content-Type: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  

{"value": "Updated Sample Account Name"}  
```  

 **Phản hồi**

```http
HTTP/1.1 204 No Content  
OData-Version: 4.0  
```  

<a name="bkmk_deleteSingleProperty"></a>

## <a name="delete-a-single-property-value"></a>Delete a single property value

 To delete the value of a single property use a DELETE request with the property name appended to the Uri of the entity.  

 The following example deletes the value of the `description` property of an account entity with the `accountid` value of 00000000-0000-0000-0000-000000000001.  

 **Yêu cầu**

```http
DELETE [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)/description HTTP/1.1  
Content-Type: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
```  

 **Phản hồi**

```http
HTTP/1.1 204 No Content  
OData-Version: 4.0  
```  

> [!NOTE]
>  This can’t be used with a single-valued navigation property to disassociate two entities. For an alternative approach, see [Remove a reference to an entity](associate-disassociate-entities-using-web-api.md#bkmk_Removeareferencetoanentity).  

<a name="bkmk_upsert"></a>

## <a name="upsert-an-entity"></a>Upsert an entity

 An *upsert* operation is exactly like an update. It uses a `PATCH` request and uses a URI to reference a specific entity. The difference is that if the entity doesn’t exist it will be created. If it already exists, it will be updated. Normally when creating a new entity you will let the system assign a unique identifier. This is a best practice. But if you need to create a record with a specific `id` value, an `upsert` operation provides a way to do this. This can be valuable in situation where you are synchronizing data in different systems.  

 Sometimes there are situations where you want to perform an `upsert`, but you want to prevent one of the potential default actions: either create or update.      You can accomplish this through the addition of `If-Match` or `If-None-Match` headers. For more information, see [Limit upsert operations](perform-conditional-operations-using-web-api.md#bkmk_limitUpsertOperations).  

<a name="bkmk_delete"></a>

## <a name="basic-delete"></a>Basic delete

 A delete operation is very straightforward. Use the DELETE verb with the URI of the entity you want to delete. This example message deletes an account entity with the primary key `accountid` value equal to 00000000-0000-0000-0000-000000000001.  

 **Yêu cầu**

```http
DELETE [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001) HTTP/1.1  
Content-Type: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
```  

 **Phản hồi**

 If the entity exists, you’ll get a normal response with status 204 to indicate the delete was successful. If the entity isn’t found, you’ll get a response with status 404.  

```http
HTTP/1.1 204 No Content  
OData-Version: 4.0  
```  

<a name="bkmk_duplicate"></a>

## <a name="check-for-duplicate-records"></a>Check for Duplicate records

By default, duplicate detection is suppressed when you are updating records using the Web API. You must include the `MSCRM.SuppressDuplicateDetection: false` header with your PATCH request to enable duplicate detection . Duplicate detection only applies when the organization has enabled duplicate detection, the entity is enabled for duplicate detection, and there are active duplicate detection rules being applied. For more information, see [Detect duplicate data for developers](../detect-duplicate-data-for-developers.md).

See [Detect duplicates during Update operation using the Web API](manage-duplicate-detection-create-update.md#bkmk_update) for more information on how to check for duplicate records during Update operation.

### <a name="see-also"></a>Xem thêm

 [Web API Basic Operations Sample (C#)](web-api-basic-operations-sample-csharp.md)   
 [Web API Basic Operations Sample (Client-side JavaScript)](web-api-basic-operations-sample-client-side-javascript.md)   
 [Perform operations using the Web API](perform-operations-web-api.md)   
 [Compose Http requests and handle errors](compose-http-requests-handle-errors.md)   
 [Query Data using the Web API](query-data-web-api.md)   
 [Create an entity using the Web API](create-entity-web-api.md)   
 [Retrieve an entity using the Web API](retrieve-entity-using-web-api.md)   
 [Associate and disassociate entities using the Web API](associate-disassociate-entities-using-web-api.md)   
 [Use Web API functions](use-web-api-functions.md)   
 [Use Web API actions](use-web-api-actions.md)   
 [Execute batch operations using the Web API](execute-batch-operations-using-web-api.md)   
 [Impersonate another user using the Web API](impersonate-another-user-web-api.md)   
 [Perform conditional operations using the Web API](perform-conditional-operations-using-web-api.md)