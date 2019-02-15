---
title: Retrieve an entity using the Web API (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how to form a GET request using the Dynamics 365 for Customer Engagement Web API to retrieve data for an entity specified as the resource with a unique identifier
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: abae4614-9e03-45e7-94fa-9e6e7225ece5
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 265bb0ed741213d4a671d0b6088da6b6f66935f9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386808"
---
# <a name="retrieve-an-entity-using-the-web-api"></a><span data-ttu-id="93f7e-103">Retrieve an entity using the Web API</span><span class="sxs-lookup"><span data-stu-id="93f7e-103">Retrieve an entity using the Web API</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="93f7e-104">Use a `GET` request to retrieve data for an entity specified as the resource with a unique identifier.</span><span class="sxs-lookup"><span data-stu-id="93f7e-104">Use a `GET` request to retrieve data for an entity specified as the resource with a unique identifier.</span></span> <span data-ttu-id="93f7e-105">When retrieving an entity you can also request specific properties and expand navigation properties to return properties from related entities.</span><span class="sxs-lookup"><span data-stu-id="93f7e-105">When retrieving an entity you can also request specific properties and expand navigation properties to return properties from related entities.</span></span>  

> [!NOTE]
>  <span data-ttu-id="93f7e-106">For information about retrieving entity metadata, see [Query Metadata using the Web API](query-metadata-web-api.md).</span><span class="sxs-lookup"><span data-stu-id="93f7e-106">For information about retrieving entity metadata, see [Query Metadata using the Web API](query-metadata-web-api.md).</span></span>

<a name="bkmk_basicRetrieve"></a>

## <a name="basic-retrieve-example"></a><span data-ttu-id="93f7e-107">Basic Retrieve example</span><span class="sxs-lookup"><span data-stu-id="93f7e-107">Basic Retrieve example</span></span>

<span data-ttu-id="93f7e-108">This example returns data for an account entity instance with the primary key value equal to 00000000-0000-0000-0000-000000000001.</span><span class="sxs-lookup"><span data-stu-id="93f7e-108">This example returns data for an account entity instance with the primary key value equal to 00000000-0000-0000-0000-000000000001.</span></span>

```http
GET [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)
```

<span data-ttu-id="93f7e-109">To retrieve more than one entity at a time, see [Basic query example](query-data-web-api.md#bkmk_basicQuery) in the [Query Data using the Web API](query-data-web-api.md) topic.</span><span class="sxs-lookup"><span data-stu-id="93f7e-109">To retrieve more than one entity at a time, see [Basic query example](query-data-web-api.md#bkmk_basicQuery) in the [Query Data using the Web API](query-data-web-api.md) topic.</span></span>

> [!CAUTION]
>  <span data-ttu-id="93f7e-110">The above example will return all the properties for account record, which is against the performance best practices for retrieving data.</span><span class="sxs-lookup"><span data-stu-id="93f7e-110">The above example will return all the properties for account record, which is against the performance best practices for retrieving data.</span></span> <span data-ttu-id="93f7e-111">This example was just to illustrate how you can do a basic retrieve of an entity instance in Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="93f7e-111">This example was just to illustrate how you can do a basic retrieve of an entity instance in Dynamics 365 for Customer Engagement apps.</span></span> <span data-ttu-id="93f7e-112">Because all the properties were returned, we haven't included the response information for the request in this example.</span><span class="sxs-lookup"><span data-stu-id="93f7e-112">Because all the properties were returned, we haven't included the response information for the request in this example.</span></span>
>
>  <span data-ttu-id="93f7e-113">As a performance best practice, you must always use the `$select` system query option to limit the properties returned while retrieving data.</span><span class="sxs-lookup"><span data-stu-id="93f7e-113">As a performance best practice, you must always use the `$select` system query option to limit the properties returned while retrieving data.</span></span> <span data-ttu-id="93f7e-114">See the following section, **Retrieve specific properties**, for information about this.</span><span class="sxs-lookup"><span data-stu-id="93f7e-114">See the following section, **Retrieve specific properties**, for information about this.</span></span>

<a name="bkmk_requestProperties"></a>

## <a name="retrieve-specific-properties"></a><span data-ttu-id="93f7e-115">Retrieve specific properties</span><span class="sxs-lookup"><span data-stu-id="93f7e-115">Retrieve specific properties</span></span>

<span data-ttu-id="93f7e-116">Use the `$select` system query option to limit the properties returned by including a comma-separated list of property names.</span><span class="sxs-lookup"><span data-stu-id="93f7e-116">Use the `$select` system query option to limit the properties returned by including a comma-separated list of property names.</span></span> <span data-ttu-id="93f7e-117">This is an important performance best practice.</span><span class="sxs-lookup"><span data-stu-id="93f7e-117">This is an important performance best practice.</span></span> <span data-ttu-id="93f7e-118">If properties aren’t specified using `$select`, all properties will be returned.</span><span class="sxs-lookup"><span data-stu-id="93f7e-118">If properties aren’t specified using `$select`, all properties will be returned.</span></span>  

<span data-ttu-id="93f7e-119">The following example retrieves `name` and `revenue` properties  for the account entity with the primary key value equal to 00000000-0000-0000-0000-000000000001</span><span class="sxs-lookup"><span data-stu-id="93f7e-119">The following example retrieves `name` and `revenue` properties  for the account entity with the primary key value equal to 00000000-0000-0000-0000-000000000001</span></span>

<span data-ttu-id="93f7e-120">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="93f7e-120">**Request**</span></span>
```http
GET [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)?$select=name,revenue HTTP/1.1
Accept: application/json
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="93f7e-121">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="93f7e-121">**Response**</span></span>
```http
HTTP/1.1 200 OK
Content-Type: application/json; odata.metadata=minimal
OData-Version: 4.0

{
"@odata.context": "[Organization URI]/api/data/v9.0/$metadata#accounts(name,revenue)/$entity",  
"@odata.etag": "W/\"502186\"",  
"name": "A. Datum Corporation (sample)",  
"revenue": 10000,  
"accountid": "00000000-0000-0000-0000-000000000001",  
"_transactioncurrencyid_value":"b2a6b689-9a39-e611-80d2-00155db44581"  
}  
```

<span data-ttu-id="93f7e-122">When you request certain types of properties you can expect additional read-only properties to be returned automatically.</span><span class="sxs-lookup"><span data-stu-id="93f7e-122">When you request certain types of properties you can expect additional read-only properties to be returned automatically.</span></span>

<span data-ttu-id="93f7e-123">If you request a money value, the `_transactioncurrencyid_value` lookup property will be returned.</span><span class="sxs-lookup"><span data-stu-id="93f7e-123">If you request a money value, the `_transactioncurrencyid_value` lookup property will be returned.</span></span> <span data-ttu-id="93f7e-124">This property contains only the GUID value of the transaction currency so you could use this value to retrieve information about the currency using the <xref href="Microsoft.Dynamics.CRM.transactioncurrency?text=transactioncurrency EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="93f7e-124">This property contains only the GUID value of the transaction currency so you could use this value to retrieve information about the currency using the <xref href="Microsoft.Dynamics.CRM.transactioncurrency?text=transactioncurrency EntityType" />.</span></span> <span data-ttu-id="93f7e-125">Alternatively, by requesting annotations you can also get additional data in the same request.</span><span class="sxs-lookup"><span data-stu-id="93f7e-125">Alternatively, by requesting annotations you can also get additional data in the same request.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="93f7e-126">[Retrieve data about lookup properties](query-data-web-api.md#bkmk_lookupProperty)</span><span class="sxs-lookup"><span data-stu-id="93f7e-126">[Retrieve data about lookup properties](query-data-web-api.md#bkmk_lookupProperty)</span></span>  

<span data-ttu-id="93f7e-127">If you request a property that is part of a composite attribute for an address, you will get the composite property as well.</span><span class="sxs-lookup"><span data-stu-id="93f7e-127">If you request a property that is part of a composite attribute for an address, you will get the composite property as well.</span></span> <span data-ttu-id="93f7e-128">For example, if your query requests the `address1_line1` property for a contact, the `address1_composite` property will be returned as well.</span><span class="sxs-lookup"><span data-stu-id="93f7e-128">For example, if your query requests the `address1_line1` property for a contact, the `address1_composite` property will be returned as well.</span></span> 

<a name="BKMK_UsingAltKeys"></a>

## <a name="retrieve-using-an-alternate-key"></a><span data-ttu-id="93f7e-129">Retrieve using an alternate key</span><span class="sxs-lookup"><span data-stu-id="93f7e-129">Retrieve using an alternate key</span></span>

<span data-ttu-id="93f7e-130">If an entity has an alternate key defined, you can also use the alternate key to retrieve the entity instead of the unique identifier for the entity.</span><span class="sxs-lookup"><span data-stu-id="93f7e-130">If an entity has an alternate key defined, you can also use the alternate key to retrieve the entity instead of the unique identifier for the entity.</span></span> <span data-ttu-id="93f7e-131">For example, if the `Contact` entity has an alternate key definition that includes both the firstname and emailaddress1 properties, you can retrieve the contact using a query with data provided for those keys as shown here.</span><span class="sxs-lookup"><span data-stu-id="93f7e-131">For example, if the `Contact` entity has an alternate key definition that includes both the firstname and emailaddress1 properties, you can retrieve the contact using a query with data provided for those keys as shown here.</span></span>

```http
GET [Organization URI]/api/data/v9.0/contacts(firstname='Joe',emailaddress1='abc@example.com')
```

<span data-ttu-id="93f7e-132">Any time you need to uniquely identify an entity to retrieve, update, or delete, you can use alternate keys configured for the entity.</span><span class="sxs-lookup"><span data-stu-id="93f7e-132">Any time you need to uniquely identify an entity to retrieve, update, or delete, you can use alternate keys configured for the entity.</span></span> <span data-ttu-id="93f7e-133">By default, there are no alternate keys configured for entities.</span><span class="sxs-lookup"><span data-stu-id="93f7e-133">By default, there are no alternate keys configured for entities.</span></span> <span data-ttu-id="93f7e-134">Alternate keys will only be available if the organization adds them.</span><span class="sxs-lookup"><span data-stu-id="93f7e-134">Alternate keys will only be available if the organization adds them.</span></span>

<a name="bkmk_retrieveSingleValue"></a>

## <a name="retrieve-a-single-property-value"></a><span data-ttu-id="93f7e-135">Retrieve a single property value</span><span class="sxs-lookup"><span data-stu-id="93f7e-135">Retrieve a single property value</span></span>

<span data-ttu-id="93f7e-136">When you only need to retrieve the value of a single property for an entity, you can append the name of the property to the URI for an entity to return only the value for that property.</span><span class="sxs-lookup"><span data-stu-id="93f7e-136">When you only need to retrieve the value of a single property for an entity, you can append the name of the property to the URI for an entity to return only the value for that property.</span></span> <span data-ttu-id="93f7e-137">This is a performance best practice because less data needs to be returned in the response.</span><span class="sxs-lookup"><span data-stu-id="93f7e-137">This is a performance best practice because less data needs to be returned in the response.</span></span>

<span data-ttu-id="93f7e-138">This example returns only the value of the name property for an account entity.</span><span class="sxs-lookup"><span data-stu-id="93f7e-138">This example returns only the value of the name property for an account entity.</span></span>

<span data-ttu-id="93f7e-139">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="93f7e-139">**Request**</span></span>
```http
GET [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)/name HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```
<span data-ttu-id="93f7e-140">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="93f7e-140">**Response**</span></span>
 ```http
HTTP/1.1 200 OK
Content-Type: application/json; odata.metadata=minimal
OData-Version: 4.0

{
"@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts(00000000-0000-0000-0000-000000000001)/name",
"value":"Adventure Works (sample)"
}
```

<a name="bkmk_retrieveNavigationPropertyValues"></a>

## <a name="retrieve-navigation-property-values"></a><span data-ttu-id="93f7e-141">Retrieve navigation property values</span><span class="sxs-lookup"><span data-stu-id="93f7e-141">Retrieve navigation property values</span></span>

<span data-ttu-id="93f7e-142">In the same way that you can retrieve individual property values, you can also access the values of navigation properties (lookup fields) by appending the name of the navigation property to the URI referencing an individual entity.</span><span class="sxs-lookup"><span data-stu-id="93f7e-142">In the same way that you can retrieve individual property values, you can also access the values of navigation properties (lookup fields) by appending the name of the navigation property to the URI referencing an individual entity.</span></span>

<span data-ttu-id="93f7e-143">The following example returns the full name of the primary contact of an account using the `primarycontactid` single-valued navigation property.</span><span class="sxs-lookup"><span data-stu-id="93f7e-143">The following example returns the full name of the primary contact of an account using the `primarycontactid` single-valued navigation property.</span></span>  

<span data-ttu-id="93f7e-144">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="93f7e-144">**Request**</span></span>
 ```http
GET [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)/primarycontactid?$select=fullname HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```
<span data-ttu-id="93f7e-145">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="93f7e-145">**Response**</span></span>
```http
HTTP/1.1 200 OK
Content-Type: application/json; odata.metadata=minimal
OData-Version: 4.0

{  
"@odata.context": "[Organization URI]/api/data/v9.0/$metadata#contacts(fullname)/$entity",  
"@odata.etag": "W/\"500128\"",  
"fullname": "Rene Valdes (sample)",  
"contactid": "ff390c24-9c72-e511-80d4-00155d2a68d1"  
}
```

<span data-ttu-id="93f7e-146">For collection-valued navigation properties you have the option to request to return only references to the related entities or just a count of the related entities.</span><span class="sxs-lookup"><span data-stu-id="93f7e-146">For collection-valued navigation properties you have the option to request to return only references to the related entities or just a count of the related entities.</span></span>

<span data-ttu-id="93f7e-147">The following example will just return references to tasks related to a specific account by adding `/$ref` to the request.</span><span class="sxs-lookup"><span data-stu-id="93f7e-147">The following example will just return references to tasks related to a specific account by adding `/$ref` to the request.</span></span>

<span data-ttu-id="93f7e-148">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="93f7e-148">**Request**</span></span>
```http
GET [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)/AccountTasks/$ref HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="93f7e-149">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="93f7e-149">**Response**</span></span>
```http
HTTP/1.1 200 OK
Content-Type: application/json; odata.metadata=minimal
OData-Version: 4.0

{  
"@odata.context": "[Organization URI]/api/data/v9.0/$metadata#Collection($ref)",  
"value": [  
{  
"@odata.id": "[Organization URI]/api/data/v9.0/tasks(6b5941dd-d175-e511-80d4-00155d2a68d1)"  
},  
{  
"@odata.id": "[Organization URI]/api/data/v9.0/tasks(fcbb60ed-d175-e511-80d4-00155d2a68d1)"  
}  
]  
}  
```
<span data-ttu-id="93f7e-150">The following example returns the number of tasks related to a specific account using the Account_Tasks collection-valued navigation property with `/$count` appended.</span><span class="sxs-lookup"><span data-stu-id="93f7e-150">The following example returns the number of tasks related to a specific account using the Account_Tasks collection-valued navigation property with `/$count` appended.</span></span>  

 <span data-ttu-id="93f7e-151">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="93f7e-151">**Request**</span></span>
```http
GET [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)/Account_Tasks/$count HTTP/1.1  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
```
<span data-ttu-id="93f7e-152">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="93f7e-152">**Response**</span></span>
```http
ï»¿2
```
> [!NOTE]
> <span data-ttu-id="93f7e-153">The value returned includes the UTF-8 byte order mark (BOM) characters (`ï»¿`) that represent that this is a UTF-8 document.</span><span class="sxs-lookup"><span data-stu-id="93f7e-153">The value returned includes the UTF-8 byte order mark (BOM) characters (`ï»¿`) that represent that this is a UTF-8 document.</span></span>

<a name="bkmk_expandRelated"></a>

## <a name="retrieve-related-entities-for-an-entity-by-expanding-navigation-properties"></a><span data-ttu-id="93f7e-154">Retrieve related entities for an entity by expanding navigation properties</span><span class="sxs-lookup"><span data-stu-id="93f7e-154">Retrieve related entities for an entity by expanding navigation properties</span></span>

<span data-ttu-id="93f7e-155">Use the `$expand` system query option to control what data from related entities is returned.</span><span class="sxs-lookup"><span data-stu-id="93f7e-155">Use the `$expand` system query option to control what data from related entities is returned.</span></span> <span data-ttu-id="93f7e-156">There are two types of navigation properties:</span><span class="sxs-lookup"><span data-stu-id="93f7e-156">There are two types of navigation properties:</span></span>  

- <span data-ttu-id="93f7e-157">*Single-valued* navigation properties correspond to Lookup attributes that support many-to-one relationships and allow setting a reference to another entity.</span><span class="sxs-lookup"><span data-stu-id="93f7e-157">*Single-valued* navigation properties correspond to Lookup attributes that support many-to-one relationships and allow setting a reference to another entity.</span></span>
- <span data-ttu-id="93f7e-158">*Collection-valued* navigation properties correspond to one-to-many or many-to-many relationships.</span><span class="sxs-lookup"><span data-stu-id="93f7e-158">*Collection-valued* navigation properties correspond to one-to-many or many-to-many relationships.</span></span>  

<span data-ttu-id="93f7e-159">If you simply include the name of the navigation property, you’ll receive all the properties for related records.</span><span class="sxs-lookup"><span data-stu-id="93f7e-159">If you simply include the name of the navigation property, you’ll receive all the properties for related records.</span></span> <span data-ttu-id="93f7e-160">You can limit the properties returned for related records using the `$select` system query option in parentheses after the navigation property name.</span><span class="sxs-lookup"><span data-stu-id="93f7e-160">You can limit the properties returned for related records using the `$select` system query option in parentheses after the navigation property name.</span></span> <span data-ttu-id="93f7e-161">Use this for both single-valued and collection-valued navigation properties.</span><span class="sxs-lookup"><span data-stu-id="93f7e-161">Use this for both single-valued and collection-valued navigation properties.</span></span>

> [!NOTE]
> <span data-ttu-id="93f7e-162">To retrieve related entities for entity sets, see [Retrieve related entities by expanding navigation properties](query-data-web-api.md#bkmk_expandRelated).</span><span class="sxs-lookup"><span data-stu-id="93f7e-162">To retrieve related entities for entity sets, see [Retrieve related entities by expanding navigation properties](query-data-web-api.md#bkmk_expandRelated).</span></span>  

- <span data-ttu-id="93f7e-163">**Retrieve related entities for an entity instance by expanding single-valued navigation properties**:</span><span class="sxs-lookup"><span data-stu-id="93f7e-163">**Retrieve related entities for an entity instance by expanding single-valued navigation properties**:</span></span> <br /><span data-ttu-id="93f7e-164">The following example demonstrates how to retrieve the contact for an account entity.</span><span class="sxs-lookup"><span data-stu-id="93f7e-164">The following example demonstrates how to retrieve the contact for an account entity.</span></span> <span data-ttu-id="93f7e-165">For the related contact record, we are only retrieving the contactid and fullname.</span><span class="sxs-lookup"><span data-stu-id="93f7e-165">For the related contact record, we are only retrieving the contactid and fullname.</span></span>

  <span data-ttu-id="93f7e-166">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="93f7e-166">**Request**</span></span>
  ```http
    GET [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)?$select=name&$expand=primarycontactid($select=contactid,fullname) HTTP/1.1  
    Accept: application/json  
    OData-MaxVersion: 4.0  
    OData-Version: 4.0  
  ```

  <span data-ttu-id="93f7e-167">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="93f7e-167">**Response**</span></span>
  ```http
    HTTP/1.1 200 OK  
    Content-Type: application/json; odata.metadata=minimal  
    OData-Version: 4.0  

    {  
    "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts(name,primarycontactid,primarycontactid(contactid,fullname))/$entity",  
    "@odata.etag":"W/\"550616\"",  
    "name":"Adventure Works (sample)",  
    "accountid":"00000000-0000-0000-0000-000000000001",  
    "primarycontactid":{  
    "@odata.etag":"W/\"550626\"",  
    "contactid":"c59648c3-68f7-e511-80d3-00155db53318",  
    "fullname":"Nancy Anderson (sample)"  
    }  
    }  
  ```
  <span data-ttu-id="93f7e-168">Instead of returning the related entities for entity instances, you can also return references (links) to the related entities by expanding the single-valued navigation property with the `$ref` option.</span><span class="sxs-lookup"><span data-stu-id="93f7e-168">Instead of returning the related entities for entity instances, you can also return references (links) to the related entities by expanding the single-valued navigation property with the `$ref` option.</span></span> <span data-ttu-id="93f7e-169">The following example returns links to the contact record for the account entity.</span><span class="sxs-lookup"><span data-stu-id="93f7e-169">The following example returns links to the contact record for the account entity.</span></span>  

  <span data-ttu-id="93f7e-170">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="93f7e-170">**Request**</span></span>
  ```http
    GET [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)?$select=name&$expand=primarycontactid/$ref HTTP/1.1  
    Accept: application/json  
    OData-MaxVersion: 4.0  
    OData-Version: 4.0  
  ```

  <span data-ttu-id="93f7e-171">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="93f7e-171">**Response**</span></span>
  ```http
    HTTP/1.1 200 OK  
    Content-Type: application/json; odata.metadata=minimal  
    OData-Version: 4.0  

    {  
    "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts(name,primarycontactid)/$entity",  
    "@odata.etag":"W/\"550616\"",  
    "name":"Adventure Works (sample)",  
    "accountid":"00000000-0000-0000-0000-000000000001",  
    "_primarycontactid_value":"c59648c3-68f7-e511-80d3-00155db53318",  
    "primarycontactid":{  
    "@odata.id":"[Organization URI]/api/data/v9.0/contacts(c59648c3-68f7-e511-80d3-00155db53318)"  
    }  
    }
  ```
- <span data-ttu-id="93f7e-172">**Retrieve related entities for an entity instance by expanding collection-valued navigation properties**:</span><span class="sxs-lookup"><span data-stu-id="93f7e-172">**Retrieve related entities for an entity instance by expanding collection-valued navigation properties**:</span></span><br /> <span data-ttu-id="93f7e-173">The following example demonstrates how you can retrieve all the tasks assigned to an account record.</span><span class="sxs-lookup"><span data-stu-id="93f7e-173">The following example demonstrates how you can retrieve all the tasks assigned to an account record.</span></span>

  <span data-ttu-id="93f7e-174">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="93f7e-174">**Request**</span></span>

  ```http
  GET [Organization URI]/api/data/v9.0/accounts(915e89f5-29fc-e511-80d2-00155db07c77)?$select=name&$expand=Account_Tasks($select=subject,scheduledstart)
  Accept: application/json
  OData-MaxVersion: 4.0
  OData-Version: 4.0
  ```

  <span data-ttu-id="93f7e-175">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="93f7e-175">**Response**</span></span>

  ```http
  HTTP/1.1 200 OK  
  Content-Type: application/json; odata.metadata=minimal  
  OData-Version: 4.0

  {
  "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts(name,Account_Tasks,Account_Tasks(subject,scheduledstart))/$entity",  
    "@odata.etag":"W/\"514069\"","name":"Sample Child Account 1","accountid":"915e89f5-29fc-e511-80d2-00155db07c77",  
    "Account_Tasks":[  
    {  
    "@odata.etag":"W/\"514085\"",  
    "subject":"Sample Task 1",  
    "scheduledstart":"2016-04-11T15:00:00Z",  
    "activityid":"a983a612-3ffc-e511-80d2-00155db07c77"  
    },{  
    "@odata.etag":"W/\"514082\"",  
    "subject":"Sample Task 2",  
    "scheduledstart":"2016-04-13T15:00:00Z",  
    "activityid":"7bcc572f-3ffc-e511-80d2-00155db07c77"  
   }  
  ]  
  }
  ```

  > [!NOTE]
  > <span data-ttu-id="93f7e-176">If you expand on collection-valued navigation parameters to retrieve related entities for *entity sets*, a @odata.nextLink property will be returned instead for the related entities.</span><span class="sxs-lookup"><span data-stu-id="93f7e-176">If you expand on collection-valued navigation parameters to retrieve related entities for *entity sets*, a @odata.nextLink property will be returned instead for the related entities.</span></span> <span data-ttu-id="93f7e-177">You should use the value of the @odata.nextLink property with a new GET request to return the required data.</span><span class="sxs-lookup"><span data-stu-id="93f7e-177">You should use the value of the @odata.nextLink property with a new GET request to return the required data.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="93f7e-178">[Retrieve related entities by expanding navigation properties](query-data-web-api.md#bkmk_expandRelated)</span><span class="sxs-lookup"><span data-stu-id="93f7e-178">[Retrieve related entities by expanding navigation properties](query-data-web-api.md#bkmk_expandRelated)</span></span>

- <span data-ttu-id="93f7e-179">**Retrieve related entities for an entity instance by expanding both single-valued and collection-valued navigation properties**: The following example demonstrates how you can expand related entities for an entity instance using both single- and collection-values navigation properties.</span><span class="sxs-lookup"><span data-stu-id="93f7e-179">**Retrieve related entities for an entity instance by expanding both single-valued and collection-valued navigation properties**: The following example demonstrates how you can expand related entities for an entity instance using both single- and collection-values navigation properties.</span></span>  

  <span data-ttu-id="93f7e-180">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="93f7e-180">**Request**</span></span>

  ```http 
    GET [Organization URI]/api/data/v9.0/accounts(99390c24-9c72-e511-80d4-00155d2a68d1)?$select=accountid&$expand=parentaccountid($select%20=%20createdon,%20name),Account_Tasks($select%20=%20subject,%20scheduledstart) HTTP/1.1  
    Accept: application/json  
    Content-Type: application/json; charset=utf-8  
    OData-MaxVersion: 4.0  
    OData-Version: 4.0
  ```

  <span data-ttu-id="93f7e-181">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="93f7e-181">**Response**</span></span>

  ```http
    HTTP/1.1 200 OK  
    Content-Type: application/json; odata.metadata=minimal  
    OData-Version: 4.0  

    {  
    "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts(accountid,parentaccountid,Account_Tasks,parentaccountid(createdon,name),Account_Tasks(subject,scheduledstart))/$entity","@odata.etag":"W/\"514069\"","accountid":"915e89f5-29fc-e511-80d2-00155db07c77",  
    "parentaccountid":{  
    "@odata.etag":"W/\"514074\"","createdon":"2016-04-06T00:29:04Z",  
    "name":"Adventure Works (sample)",  
    "accountid":"3adbf27c-8efb-e511-80d2-00155db07c77"  
    },"Account_Tasks":[  
    {  
    "@odata.etag":"W/\"514085\"",  
    "subject":"Sample Task 1",  
    "scheduledstart":"2016-04-11T15:00:00Z",  
    "activityid":"a983a612-3ffc-e511-80d2-00155db07c77"  
    },{  
    "@odata.etag":"W/\"514082\"",  
    "subject":"Sample Task 2",  
    "scheduledstart":"2016-04-13T15:00:00Z",  
    "activityid":"7bcc572f-3ffc-e511-80d2-00155db07c77"  
    }  
    ]  
    }
  ```

> [!NOTE]
> <span data-ttu-id="93f7e-182">You can’t use the `/$ref` or `/$count` path segments to return only the URI for the related entity or a count of the number of related entities.</span><span class="sxs-lookup"><span data-stu-id="93f7e-182">You can’t use the `/$ref` or `/$count` path segments to return only the URI for the related entity or a count of the number of related entities.</span></span>

<a name="bkmk_optionsOnExpand"></a>

## <a name="options-to-apply-to-expanded-entities"></a><span data-ttu-id="93f7e-183">Options to apply to expanded entities</span><span class="sxs-lookup"><span data-stu-id="93f7e-183">Options to apply to expanded entities</span></span>

 <span data-ttu-id="93f7e-184">You can apply certain system query options on the entities returned for a collection-valued navigation property.</span><span class="sxs-lookup"><span data-stu-id="93f7e-184">You can apply certain system query options on the entities returned for a collection-valued navigation property.</span></span> <span data-ttu-id="93f7e-185">Use a semicolon-separated list of system query options enclosed in parentheses after the name of the collection-valued navigation property.</span><span class="sxs-lookup"><span data-stu-id="93f7e-185">Use a semicolon-separated list of system query options enclosed in parentheses after the name of the collection-valued navigation property.</span></span> <span data-ttu-id="93f7e-186">You can use `$select`, `$filter`, `$orderby`, and `$top`.</span><span class="sxs-lookup"><span data-stu-id="93f7e-186">You can use `$select`, `$filter`, `$orderby`, and `$top`.</span></span>

 <span data-ttu-id="93f7e-187">The following example filters the results of task entities related to an account to those with a subject that ends with “1.”</span><span class="sxs-lookup"><span data-stu-id="93f7e-187">The following example filters the results of task entities related to an account to those with a subject that ends with “1.”</span></span>

```http
GET [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)?$expand=Account_Tasks($filter=endswith(subject,'1');$select=subject)  
```

<span data-ttu-id="93f7e-188">The following example specifies that related tasks should be returned in ascending order based on the `createdon` property.</span><span class="sxs-lookup"><span data-stu-id="93f7e-188">The following example specifies that related tasks should be returned in ascending order based on the `createdon` property.</span></span>

```http
GET [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)?$expand=Account_Tasks($orderby=createdon asc;$select=subject,createdon)  
```

 <span data-ttu-id="93f7e-189">The following example returns only the first related task.</span><span class="sxs-lookup"><span data-stu-id="93f7e-189">The following example returns only the first related task.</span></span>

```http
GET [Organization URI]/api/data/v9.0/accounts(00000000-0000-0000-0000-000000000001)?$expand=Account_Tasks($top=1;$select=subject)
```

> [!NOTE]
> <span data-ttu-id="93f7e-190">This is a subset of the system query options described in the “11.2.4.2.1 Expand Options” section of [OData Version 4.0 Part 1: Protocol Plus Errata 02](http://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part1-protocol/odata-v4.0-errata02-os-part1-protocol-complete.html).</span><span class="sxs-lookup"><span data-stu-id="93f7e-190">This is a subset of the system query options described in the “11.2.4.2.1 Expand Options” section of [OData Version 4.0 Part 1: Protocol Plus Errata 02](http://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part1-protocol/odata-v4.0-errata02-os-part1-protocol-complete.html).</span></span> <span data-ttu-id="93f7e-191">The options `$skip`, `$count`, `$search`, `$expand` and `$levels` aren’t supported for the Web API.</span><span class="sxs-lookup"><span data-stu-id="93f7e-191">The options `$skip`, `$count`, `$search`, `$expand` and `$levels` aren’t supported for the Web API.</span></span>

<a name="bkmk_DetectIfChanged"></a>

## <a name="detect-if-an-entity-has-changed-since-it-was-retrieved"></a><span data-ttu-id="93f7e-192">Detect if an entity has changed since it was retrieved</span><span class="sxs-lookup"><span data-stu-id="93f7e-192">Detect if an entity has changed since it was retrieved</span></span>

<span data-ttu-id="93f7e-193">As a performance best practice you should only request data that you need.</span><span class="sxs-lookup"><span data-stu-id="93f7e-193">As a performance best practice you should only request data that you need.</span></span> <span data-ttu-id="93f7e-194">If you have previously retrieved an entity record, you can use the *ETag* associated with a previously retrieved record to perform conditional retrievals on that record.</span><span class="sxs-lookup"><span data-stu-id="93f7e-194">If you have previously retrieved an entity record, you can use the *ETag* associated with a previously retrieved record to perform conditional retrievals on that record.</span></span>  <span data-ttu-id="93f7e-195">For more information, see [Conditional retrievals](perform-conditional-operations-using-web-api.md#bkmk_DetectIfChanged).</span><span class="sxs-lookup"><span data-stu-id="93f7e-195">For more information, see [Conditional retrievals](perform-conditional-operations-using-web-api.md#bkmk_DetectIfChanged).</span></span>  

<a name="bkmk_formattedValues"></a>

## <a name="retrieve-formatted-values"></a><span data-ttu-id="93f7e-196">Retrieve formatted values</span><span class="sxs-lookup"><span data-stu-id="93f7e-196">Retrieve formatted values</span></span>

<span data-ttu-id="93f7e-197">Requesting formatted values for individual record retrievals is done the same way as done when querying entity sets.</span><span class="sxs-lookup"><span data-stu-id="93f7e-197">Requesting formatted values for individual record retrievals is done the same way as done when querying entity sets.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="93f7e-198">[Include formatted values](query-data-web-api.md#bkmk_includeFormattedValues).</span><span class="sxs-lookup"><span data-stu-id="93f7e-198">[Include formatted values](query-data-web-api.md#bkmk_includeFormattedValues).</span></span>

### <a name="see-also"></a><span data-ttu-id="93f7e-199">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="93f7e-199">See also</span></span>

[<span data-ttu-id="93f7e-200">Web API Basic Operations Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="93f7e-200">Web API Basic Operations Sample (C#)</span></span>](web-api-basic-operations-sample-csharp.md)<br />
[<span data-ttu-id="93f7e-201">Web API Basic Operations Sample (Client-side JavaScript)</span><span class="sxs-lookup"><span data-stu-id="93f7e-201">Web API Basic Operations Sample (Client-side JavaScript)</span></span>](web-api-basic-operations-sample-client-side-javascript.md)<br />
[<span data-ttu-id="93f7e-202">Perform operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="93f7e-202">Perform operations using the Web API</span></span>](perform-operations-web-api.md)<br />
[<span data-ttu-id="93f7e-203">Compose Http requests and handle errors</span><span class="sxs-lookup"><span data-stu-id="93f7e-203">Compose Http requests and handle errors</span></span>](compose-http-requests-handle-errors.md)<br />
[<span data-ttu-id="93f7e-204">Query Data using the Web API</span><span class="sxs-lookup"><span data-stu-id="93f7e-204">Query Data using the Web API</span></span>](query-data-web-api.md)<br />
[<span data-ttu-id="93f7e-205">Create an entity using the Web API</span><span class="sxs-lookup"><span data-stu-id="93f7e-205">Create an entity using the Web API</span></span>](create-entity-web-api.md)<br />
[<span data-ttu-id="93f7e-206">Update and delete entities using the Web API</span><span class="sxs-lookup"><span data-stu-id="93f7e-206">Update and delete entities using the Web API</span></span>](update-delete-entities-using-web-api.md)<br />
[<span data-ttu-id="93f7e-207">Associate and disassociate entities using the Web API</span><span class="sxs-lookup"><span data-stu-id="93f7e-207">Associate and disassociate entities using the Web API</span></span>](associate-disassociate-entities-using-web-api.md)<br />
[<span data-ttu-id="93f7e-208">Use Web API functions</span><span class="sxs-lookup"><span data-stu-id="93f7e-208">Use Web API functions</span></span>](use-web-api-functions.md)<br />
[<span data-ttu-id="93f7e-209">Use Web API actions</span><span class="sxs-lookup"><span data-stu-id="93f7e-209">Use Web API actions</span></span>](use-web-api-actions.md)<br />
[<span data-ttu-id="93f7e-210">Execute batch operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="93f7e-210">Execute batch operations using the Web API</span></span>](execute-batch-operations-using-web-api.md)<br />
[<span data-ttu-id="93f7e-211">Impersonate another user using the Web API</span><span class="sxs-lookup"><span data-stu-id="93f7e-211">Impersonate another user using the Web API</span></span>](impersonate-another-user-web-api.md)<br />
[<span data-ttu-id="93f7e-212">Perform conditional operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="93f7e-212">Perform conditional operations using the Web API</span></span>](perform-conditional-operations-using-web-api.md)<br />
