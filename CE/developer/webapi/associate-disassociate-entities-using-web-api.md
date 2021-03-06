---
title: Associate and disassociate entities using the Web API (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how to add  reference to a collection-valued navigation property, remove a reference and change an existing reference using the Web API
ms.custom: ''
ms.date: 11/30/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: ad4e4eac-117a-4958-9df0-b7353305b0c7
caps.latest.revision: 13
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d698ab71417b3dbeee98992608428ccbf2371c14
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386813"
---
# <a name="associate-and-disassociate-entities-using-the-web-api"></a>Associate and disassociate entities using the Web API

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

There are several methods you can use to associate and disassociate entities. Which method you apply depends on whether you’re creating or updating the entities and whether you’re operating in the context of the referenced entity or the referencing entity.  

<a name="bkmk_Addareferencetoacollection"></a>

## <a name="add-a-reference-to-a-collection-valued-navigation-property"></a>Add a reference to a collection-valued navigation property

 The following example shows how to associate an existing opportunity entity with the opportunityid value of 00000000-0000-0000-0000-000000000001 to the collection-valued opportunity_customer_accounts navigation property for an account entity with the `accountid` value of 00000000-0000-0000-0000-000000000002. This is a 1:N relationship but you can perform the same operation for an N:N relationship.  
  
**Yêu cầu**  
```http  
POST [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000002)/opportunity_customer_accounts/$ref HTTP/1.1   
Content-Type: application/json   
Accept: application/json   
OData-MaxVersion: 4.0   
OData-Version: 4.0  
  
{  
"@odata.id":"[Organization URI]/api/data/v9.0/opportunities(00000000-0000-0000-0000-000000000001)"  
}  
```  
  
**Phản hồi**  
```http 
HTTP/1.1 204 No Content  
OData-Version: 4.0  
```  
  
<a name="bkmk_Removeareferencetoanentity"></a>

## <a name="remove-a-reference-to-an-entity"></a>Remove a reference to an entity

 Use a DELETE request to remove a reference to an entity. The way you do it is different depending on whether you’re referring to a collection-valued navigation property or a single-valued navigation property.  
  
 **Yêu cầu**  
 For a collection-valued navigation property, use the following.  
  
```http  
DELETE [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000002)/opportunity_customer_accounts/$ref?$id=[Organization URI]/api/data/v9.0/opportunities(00000000-0000-0000-0000-000000000001) HTTP/1.1  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
```  
  
 Or, use this.  
  
```http 
DELETE [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000002)/opportunity_customer_accounts(00000000-0000-0000-0000-000000000001)/$ref HTTP/1.1  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
```  
  
 **Yêu cầu**  
 For a single-valued navigation property, remove the `$id` query string parameter.  
  
```http 
DELETE [Organization URI]/api/data/v9.0/opportunities(00000000-0000-0000-0000-000000000001)/customerid_account/$ref HTTP/1.1  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
```  
  
 **Phản hồi**  
 Either way, a successful response has status 204.  
  
```http 
HTTP/1.1 204 No Content  
OData-Version: 4.0  
```  
  
<a name="bkmk_Changethereferenceinasingle"></a>
 
## <a name="change-the-reference-in-a-single-valued-navigation-property"></a>Change the reference in a single-valued navigation property

 You can associate entities by setting the value of a single-valued navigation property using PUT request with the following pattern.  
  
 **Yêu cầu**

```http 
PUT [Organization URI]/api/data/v9.0/opportunities(00000000-0000-0000-0000-000000000001)/customerid_account/$ref HTTP/1.1  
Content-Type: application/json  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
  
{  
 "@odata.id":"[Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000002)"  
}  
```  
  
 **Phản hồi**  

```http 
HTTP/1.1 204 No Content  
OData-Version: 4.0  
```  
  
<a name="bkmk_Associateentitiesoncreate"></a>

## <a name="associate-entities-on-create"></a>Associate entities on create

 As described in [Create related entities in one operation](create-entity-web-api.md#bkmk_CreateRelated), new entities can be created with relationships using *deep insert*.  
  
<a name="bkmk_Associateentitiesonupdate"></a>

## <a name="associate-entities-on-update-using-single-valued-navigation-property"></a>Associate entities on update using single-valued navigation property

 You can associate entities on update using the same message described in [Basic update](update-delete-entities-using-web-api.md#bkmk_update) but you must use the @odata.bind annotation to set the value of a single-valued navigation property. The following example changes the account associated to an opportunity using the `customerid_account` single-valued navigation property.  
  
 **Yêu cầu**

```http 
PATCH [Organization URI]/api/data/v9.0/opportunities(00000000-0000-0000-0000-000000000001) HTTP/1.1  
Content-Type: application/json  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
  
{  
 "customerid_account@odata.bind":"[Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000002)"  
}  
```  
  
 **Phản hồi**  

```http 
HTTP/1.1 204 No Content  
OData-Version: 4.0  
```  
<a name="bkmk_Associateentitiesonupdate_multi"></a>

## <a name="associate-entities-on-update-using-collection-valued-navigation-property"></a>Associate entities on update using collection-valued navigation property

The following example shows how to associate multiple existing [ActivityParty](../entities/activityparty.md) entities with an [Email](../entities/email.md) entity using collection-valued navigation property `email_activity_parties`.

> [!NOTE]
> Associating multiple entities with an entity on update is a special scenario that is possible only with <xref href="Microsoft.Dynamics.CRM.activityparty?text=activityparty EntityType" />.

**Yêu cầu**

```HTTP
PUT [Organization URI]/api/data/v9.0/emails(2479d20d-3a39-e711-8145-e0071b6a2001)/email_activity_parties
Content-Type: application/json  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0

{
    "value": [
        {
            "partyid_contact@odata.bind":"contacts(a30d4045-fc46-e711-8115-e0071b66df51)",
            "participationtypemask":3
            
        },
        {
            "partyid_contact@odata.bind":"contacts(1dcdda07-3a39-e711-8145-e0071b6a2001)",
            "participationtypemask":2
            
        }
        ]
}
```

**Phản hồi**

```HTTP
HTTP/1.1 204 No Content  
OData-Version: 4.0 
```

### <a name="see-also"></a>Xem thêm

 [Web API Basic Operations Sample (C#)](web-api-basic-operations-sample-csharp.md)   
 [Web API Basic Operations Sample (Client-side JavaScript)](web-api-basic-operations-sample-client-side-javascript.md)   
 [Perform operations using the Web API](perform-operations-web-api.md)   
 [Compose Http requests and handle errors](compose-http-requests-handle-errors.md)   
 [Query Data using the Web API](query-data-web-api.md)   
 [Create an entity using the Web API](create-entity-web-api.md)   
 [Retrieve an entity using the Web API](retrieve-entity-using-web-api.md)   
 [Update and delete entities using the Web API](update-delete-entities-using-web-api.md)   
 [Use Web API functions](use-web-api-functions.md)   
 [Use Web API actions](use-web-api-actions.md)   
 [Execute batch operations using the Web API](execute-batch-operations-using-web-api.md)   
 [Impersonate another user using the Web API](impersonate-another-user-web-api.md)   
 [Perform conditional operations using the Web API](perform-conditional-operations-using-web-api.md)
