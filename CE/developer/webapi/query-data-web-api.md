---
title: Query Data using the Web API (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read about the various ways to query Dynamics 365 for Customer Engagement data using the Dynamics 365 for Customer Engagement Web API and various system query options that can be applied in these queries
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: fc3ade34-9c4e-4c33-88a4-aa3842c5eee1
caps.latest.revision: 78
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9c5d9d746582984651751f2fa9cc94564525b3a7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386187"
---
# <a name="query-data-using-the-web-api"></a>Query Data using the Web API

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

If you want to retrieve data for an entity set, use a GET request. When retrieving data, you can apply query options to set criteria for the data you want and the entity properties that should be returned.  
    
<a name="bkmk_basicQuery"></a>
 
## <a name="basic-query-example"></a>Basic query example

 This example queries the accounts entity set and uses the `$select` and `$top` system query options to return the name property for the first three accounts:  
  
 **Yêu cầu**

```http 
GET [Organization URI]/api/data/v9.0/accounts?$select=name&$top=3 HTTP/1.1  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
  
```  
  
**Phản hồi**

```http 
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
  
{  
"@odata.context": "[Organization URI]/api/data/v9.0/$metadata#accounts(name)",  
"value": [  
{  
"@odata.etag": "W/\"501097\"",  
"name": "Fourth Coffee (sample)",  
"accountid": "89390c24-9c72-e511-80d4-00155d2a68d1"  
},  
{  
"@odata.etag": "W/\"501098\"",  
"name": "Litware, Inc. (sample)",  
"accountid": "8b390c24-9c72-e511-80d4-00155d2a68d1"  
},  
{  
"@odata.etag": "W/\"501099\"",  
"name": "Adventure Works (sample)",  
"accountid": "8d390c24-9c72-e511-80d4-00155d2a68d1"  
}  
]  
}  
```  
  
<a name="bkmk_limits"></a>

## <a name="limits-on-number-of-entities-returned"></a>Limits on number of entities returned

 Unless you specify a smaller page size, a maximum of 5000 entities will be returned for each request. If there are more entities that match the query filter criteria, a @odata.nextLink property will be returned with the results. Use the value of the @odata.nextLink property with a new GET request to return the next page of data.  
  
> [!NOTE]
>  Queries on model entities aren’t limited or paged. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Query Metadata using the Web API](query-metadata-web-api.md)  
  
<a name="bkmk_specifyNumber"></a>

## <a name="specify-the-number-of-entities-to-return-in-a-page"></a>Specify the number of entities to return in a page

 Use the odata.maxpagesize preference value to request the number of entities returned in the response.  
  
> [!NOTE]
>  You can’t use an odata.maxpagesize preference value greater than 5000.  
  
 The following example queries the accounts  entity set and returns the `name` property for the first three accounts.  
  
 **Yêu cầu**

```http 
GET [Organization URI]/api/data/v9.0/accounts?$select=name HTTP/1.1  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Prefer: odata.maxpagesize=3  
```  
  
 **Phản hồi**  

```http 
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Content-Length: 402  
Preference-Applied: odata.maxpagesize=3  
  
{  
"@odata.context": "[Organization URI]/api/data/v9.0/$metadata#accounts(name)",  
"value": [  
{  
"@odata.etag": "W/\"437194\"",  
"name": "Fourth Coffee (sample)",  
"accountid": "7d51925c-cde2-e411-80db-00155d2a68cb"  
},  
{  
"@odata.etag": "W/\"437195\"",  
"name": "Litware, Inc. (sample)",  
"accountid": "7f51925c-cde2-e411-80db-00155d2a68cb"  
},  
{  
"@odata.etag": "W/\"468026\"",  
"name": "Adventure Works (sample)",  
"accountid": "8151925c-cde2-e411-80db-00155d2a68cb"  
}  
],  
"@odata.nextLink": "[Organization URI]/api/data/v9.0/accounts?$select=name&$skiptoken=%3Ccookie%20pagenumber=%222%22%20pagingcookie=%22%253ccookie%2520page%253d%25221%2522%253e%253caccountid%2520last%253d%2522%257b8151925C-CDE2-E411-80DB-00155D2A68CB%257d%2522%2520first%253d%2522%257b7D51925C-CDE2-E411-80DB-00155D2A68CB%257d%2522%2520%252f%253e%253c%252fcookie%253e%22%20/%3E"  
}  
```  
  
 Use the value of the `@odata.nextLink` property to request the next set of records. Don’t change or append any additional system query options to the value. For every subsequent request for additional pages, you should use the same odata.maxpagesize preference value used in the original request. Also, cache the results returned or the value of the @odata.nextLink property so that previously retrieved pages can be returned to.  
  
> [!NOTE]
>  The value of the @odata.nextLink property is URI encoded. If you URI encode the value before you send it, the XML cookie information in the URL will cause an error.  
  
<a name="bkmk_applyqueryOptions"></a>

## <a name="apply-system-query-options"></a>Apply system query options

 Each of the system query options you append to the URL for the entity set is added using the syntax for query strings. The first is appended after [?] and subsequent query options are separated using [&]. All query options are case-sensitive as shown in the following example.  
  
```http 
GET [Organization URI]/api/data/v9.0/accounts?$select=name,revenue&$top=3&$filter=revenue gt 100000  
```  
  
<a name="bkmk_requestProperties"></a>
 
## <a name="request-specific-properties"></a>Request specific properties

 Use the `$select` system query option to limit the properties returned as shown in the following example.  
  
```http 
GET [Organization URI]/api/data/v9.0/accounts?$select=name,revenue  
```  
  
> [!IMPORTANT]
>  This is a performance best practice. If properties aren’t specified using `$select`, all properties will be returned.  
  
 When you request certain types of properties you can expect additional read-only properties to be returned automatically.  
  
 If you request a money value, the `_transactioncurrencyid_value` lookup property will be returned. This property contains only the GUID value of the transaction currency so you could use this value to retrieve information about the currency using the <xref href="Microsoft.Dynamics.CRM.transactioncurrency?text=transactioncurrency EntityType" />. Alternatively, by requesting annotations you can also get additional data in the same request. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Retrieve data about lookup properties](#bkmk_lookupProperty)  
  
 If you request a property that is part of a composite attribute for an address, you will get the composite property as well. For example, if your query requests the `address1_line1` property for a contact, the `address1_composite` property will be returned as well. 
  
<a name="bkmk_filter"></a>
 
## <a name="filter-results"></a>Filter results

 Use the `$filter` system query option to set criteria for which entities will be returned.  
  
<a name="bkmk_buildInFilterOperators"></a>

### <a name="standard-filter-operators"></a>Standard filter operators

 The Web API supports the standard OData filter operators listed in the following table.  
  
|Toán tử|Mô tả|Ví dụ|  
|--------------|-----------------|-------------|  
|**Comparison Operators**|||  
|`eq`|Equal|`$filter=revenue eq 100000`|  
|`ne`|Not Equal|`$filter=revenue ne 100000`|  
|`gt`|Lớn hơn|`$filter=revenue gt 100000`|  
|`ge`|Greater than or equal|`$filter=revenue ge 100000`|  
|`lt`|Nhỏ hơn|`$filter=revenue lt 100000`|  
|`le`|Less than or equal|`$filter=revenue le 100000`|  
|**Logical Operators**|||  
|`and`|Logical and|`$filter=revenue lt 100000 and revenue gt 2000`|  
|`or`|Logical or|`$filter=contains(name,'(sample)') or contains(name,'test')`|  
|`not`|Logical negation|`$filter=not contains(name,'sample')`|  
|**Grouping Operators**|||  
|`( )`|Precedence grouping|`(contains(name,'sample') or contains(name,'test')) and revenue gt 5000`|  
  
> [!NOTE]
>  This is a sub-set of the [11.2.5.1.1 Built-in Filter Operations](http://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part1-protocol/odata-v4.0-errata02-os-part1-protocol-complete.html). Arithmetic operators and the comparison has operator are not supported in the Web API.  
  
<a name="bkmk_buildInQueryFunctions"></a>

### <a name="standard-query-functions"></a>Standard query functions  
 
 OData string query functions:
 
|Hàm|Ví dụ|  
|--------------|-------------|  
|`contains`|`$filter=contains(name,'(sample)')`|  
|`endswith`|`$filter=endswith(name,'Inc.')`|  
|`startswith`|`$filter=startswith(name,'a')`|

  
> [!NOTE]
>  This is a sub-set of the [11.2.5.1.2 Built-in Query Functions](http://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part1-protocol/odata-v4.0-errata02-os-part1-protocol-complete.html). `Date`, `Math`, `Type`, `Geo` and other string functions aren’t supported in the web API.  
  
### <a name="includepndynamicscrmincludespn-dynamics-crmmd-web-api-query-functions"></a>[!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Web API query functions
 
 [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps provides a number of special functions that accept parameters, return Boolean values, and can be used as filter criteria in a query. See <xref:Microsoft.Dynamics.CRM.QueryFunctionIndex> for a list of these functions. The following is an example of the <xref href="Microsoft.Dynamics.CRM.Between?text=Between Function" /> searching for accounts with a number of employees between 5 and 2000.  
  
```http 
GET [Organization URI]/api/data/v9.0/accounts?$select=name,numberofemployees&$filter=Microsoft.Dynamics.CRM.Between(PropertyName='numberofemployees',PropertyValues=["5","2000"])  
```  
  
 [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Compose a query with functions](use-web-api-functions.md#bkmk_composeQueryWithFunctions).  
  
<a name="bkmk_order"></a>
 
## <a name="order-results"></a>Order results

 Specify the order in which items are returned using the `$orderby` system query option. Use the `asc` or `desc` suffix to specify ascending or descending order respectively. The default is ascending if the suffix isn’t applied. The following example shows retrieving the name and revenue properties of accounts ordered by ascending revenue and by descending name.  
  
```http 
GET [Organization URI]/api/data/v9.0/accounts?$select=name,revenue,&$orderby=revenue asc,name desc&$filter=revenue ne null  
```  
  
<a name="bkmk_useParameterAliases"></a>

## <a name="aggregate-and-grouping-results"></a>Aggregate and Grouping results

By using `$apply` you can aggregate and group your data dynamically.  Possible use cases with `$apply`:

|Use Case|Ví dụ|
|--------------|-------------| 
|List of unique statuses in the query|`$apply=groupby((statuscode))`|
|Aggregate sum of the estimated value|`$apply=aggregate(estimatedvalue with sum as total)`|
|Average size of the deal based on estimated value and status|`$apply=groupby((statuscode),aggregate(estimatedvalue with average as averagevalue)`|
|Sum of estimated value based on status|`$apply=groupby((statuscode),aggregate(estimatedvalue with sum as total))`|
|Total opportunity revenue by Account name|`$apply=groupby((parentaccountid/name),aggregate(estimatedvalue with sum as total))`|
|Last created record date and time|`$apply=aggregate(createdon with max as lastCreate)`|
|First created record date and time|`$apply=aggregate(createdon with min as firstCreate)`|

The aggregate functions are limited to a collection of 50,000 records.  Further information around using aggregate functionality with Dynamics 365 for Customer Engagement apps can be found here: [Use FetchXML to construct a query](../org-service/use-fetchxml-construct-query.md)

Additional details on OData data aggregation can be found here: [http://docs.oasis-open.org/odata/odata-data-aggregation-ext/v4.0/cs01/odata-data-aggregation-ext-v4.0-cs01.html](http://docs.oasis-open.org/odata/odata-data-aggregation-ext/v4.0/cs01/odata-data-aggregation-ext-v4.0-cs01.html).  Note that Dynamics 365 for Customer Engagement apps only supports a sub-set of these aggregate methods.

## <a name="use-parameter-aliases-with-system-query-options"></a>Use parameter aliases with system query options

 You can use parameter aliases for `$filter` and `$orderby` system query options. Parameter aliases allow for the same value to be used multiple times in a request. If the alias isn’t assigned a value it is assumed to be null.  
  
 Without parameter aliases:

```http  
GET [Organization URI]/api/data/v9.0/accounts?$select=name,revenue,&$orderby=revenue asc,name desc&$filter=revenue ne null  
```  
  
 With parameter aliases:

```http  
GET [Organization URI]/api/data/v9.0/accounts?$select=name,revenue,&$orderby=@p1 asc,@p2 desc&$filter=@p1 ne @p3&@p1=revenue&@p2=name  
```  
  
 You can also use parameter aliases when using functions. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Use Web API functions](use-web-api-functions.md)  
  
<a name="bkmk_limitResults"></a>
 
## <a name="limit-results"></a>Limit results

 You can limit the number of results returned by using the `$top` system query option. The following example will return just the first three account entities.  
  
```http 
GET [Organization URI]/api/data/v9.0/accounts?$select=name,revenue&$top=3  
```  
  
> [!NOTE]
>  Limiting results using `$top` will prevent `odata.maxpagesize` preference from being applied. You can use `odata.maxpagesize` preference or `$top`, but not both at the same time. For more information about `odata.maxpagesize`, see [Specify the number of entities to return in a page](query-data-web-api.md#bkmk_specifyNumber).  
>   
>  You should also not use `$top` with `$count`.  
  
<a name="bkmk_retrieveCount"></a>
 
## <a name="retrieve-a-count-of-entities"></a>Retrieve a count of entities

 Use the `$count` system query option with a value of `true` to include a count of entities that match the filter criteria up to 5000.  
  
> [!NOTE]
>  The count value does not represent the total number of entities in the system. It is limited by the maximum number of entities that  can be returned. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Limits on number of entities returned](#bkmk_limits)  
  
 The response `@odata.count` property will contain the number of entities that match the filter criteria irrespective of an `odata.maxpagesize` preference limitation.  
  
> [!NOTE]
>  You should not use `$top` with `$count`.  
  
 The following example shows that there are ten accounts that match the criteria where the name contains “sample”, but only the first three accounts are returned.  
  
 **Yêu cầu**

```http 
GET [Organization URI]/api/data/v9.0/accounts?$select=name&$filter=contains(name,'sample')&$count=true HTTP/1.1  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Prefer: odata.maxpagesize=3  
```  
  
 **Phản hồi** 
 
```http 
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.maxpagesize=3  
  
{  
"@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts(name)",  
"@odata.count":10,  
"value":[  
{  
"@odata.etag":"W/\"502482\"","name":"Fourth Coffee (sample)","accountid":"655eaf89-f083-e511-80d3-00155d2a68d3"  
},{  
"@odata.etag":"W/\"502483\"","name":"Litware, Inc. (sample)","accountid":"675eaf89-f083-e511-80d3-00155d2a68d3"  
},{  
"@odata.etag":"W/\"502484\"","name":"Adventure Works (sample)","accountid":"695eaf89-f083-e511-80d3-00155d2a68d3"  
}  
],"@odata.nextLink":"[Organization URI]/api/data/v9.0/accounts?$select=name&$filter=contains(name,'sample')&$skiptoken=%3Ccookie%20pagenumber=%222%22%20pagingcookie=%22%253ccookie%2520page%253d%25221%2522%253e%253caccountid%2520last%253d%2522%257b695EAF89-F083-E511-80D3-00155D2A68D3%257d%2522%2520first%253d%2522%257b655EAF89-F083-E511-80D3-00155D2A68D3%257d%2522%2520%252f%253e%253c%252fcookie%253e%22%20istracking=%22False%22%20/%3E"  
}  
  
```  
  
 If you don’t want to return any data except for the count, you can apply `$count` to any collection to get just the value.  
  
 **Yêu cầu**  

```http 
GET [Organization URI]/api/data/v9.0/accounts/$count HTTP/1.1  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
```  
  
 **Phản hồi**  
```http 
HTTP/1.1 200 OK  
Content-Type: text/plain  
OData-Version: 4.0  
  
10  
```  
  
<a name="bkmk_includeFormattedValues"></a>

## <a name="include-formatted-values"></a>Include formatted values

 When you want to receive formatted values for properties with the results, use the `odata.include-annotations` preference with the value of `OData.Community.Display.V1.FormattedValue`. The response will include these values with properties that match the following naming convention:  
  
```  
<propertyname>@OData.Community.Display.V1.FormattedValue  
```  
 The following example queries the accounts entity set and returns the first record, including properties that support formatted values.  
  
 **Yêu cầu**

```http 
GET [Organization URI]/api/data/v9.0/accounts?$select=name,donotpostalmail,accountratingcode,numberofemployees,revenue&$top=1 HTTP/1.1  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Prefer: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
```  
  
 **Phản hồi**  
```http 
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
  
{  
"@odata.context": "[Organization URI]/api/data/v9.0/$metadata#accounts(name,donotpostalmail,accountratingcode,numberofemployees,revenue)",  
"value": [  
{  
"@odata.etag": "W/"502170"",  
"name": "Fourth Coffee (sample)",  
"donotpostalmail@OData.Community.Display.V1.FormattedValue": "Allow",  
"donotpostalmail": false,  
"accountratingcode@OData.Community.Display.V1.FormattedValue": "Default Value",  
"accountratingcode": 1,  
"numberofemployees@OData.Community.Display.V1.FormattedValue": "9,500",  
"numberofemployees": 9500,  
"revenue@OData.Community.Display.V1.FormattedValue": "$100,000.00",  
"revenue": 100000,  
"accountid": "89390c24-9c72-e511-80d4-00155d2a68d1",  
"transactioncurrencyid_value": "50b6dd7b-f16d-e511-80d0-00155db07cb1" } ]  
}    
```  
  
<a name="bkmk_lookupProperty"></a>

## <a name="retrieve-data-about-lookup-properties"></a>Retrieve data about lookup properties

 If your query includes lookup properties you can request annotations that will provide additional information about the data in these properties. Most of the time, the same data is can be derived with knowledge of the single-valued navigation properties and the data included in the related entities. However, in cases where the property represents a lookup attribute that can refer to more than one type of entity, this information can tell you what type of entity is referenced by the lookup property. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Lookup properties](web-api-types-operations.md#bkmk_lookupProperties)  
  
 There are two additional types of annotations available for these properties,  
  
|Annotation|Mô tả|  
|----------------|-----------------|  
|Microsoft.Dynamics.CRM.associatednavigationproperty|The name of the single-valued navigation property that includes the reference to the entity.|  
|Microsoft.Dynamics.CRM.lookuplogicalname|The logical name of the entity referenced by the lookup.|  
  
 These properties also can include formatted values as described in [Include formatted values](query-data-web-api.md#bkmk_includeFormattedValues). Just like formatted values, you can return the other annotations using the `odata.include-annotations` preference set to the specific type of annotation you want, or you can set the value to `"*"` and return all three. The following sample shows the request and response to retrieve information about the incident entity `_customerid_value` lookup property with annotations included.  
  
 **Yêu cầu**  

```http 
GET [Organization URI]/api/data/v9.0/incidents(39dd0b31-ed8b-e511-80d2-00155d2a68d4)?$select=title,customerid_value&$expand=customerid_contact($select=fullname) HTTP/1.1  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Prefer: odata.include-annotations="*"  
```  
  
 **Phản hồi**  

```http 
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="*"  
  
{  
"@odata.context":"[Organization URI]/api/data/v9.0/$metadata#incidents(title,_customerid_value,customerid_contact(fullname))/$entity",  
"@odata.etag":"W/\"504696\"",  
"_customerid_value@Microsoft.Dynamics.CRM.associatednavigationproperty":"customerid_contact",  
"_customerid_value@Microsoft.Dynamics.CRM.lookuplogicalname":"contact",  
"_customerid_value@OData.Community.Display.V1.FormattedValue":"Susanna Stubberod (sample)",  
"_customerid_value":"7ddd0b31-ed8b-e511-80d2-00155d2a68d4",  
"incidentid":"39dd0b31-ed8b-e511-80d2-00155d2a68d4",  
"customerid_contact":{  
"@odata.etag":"W/\"503587\"",  
"fullname":"Susanna Stubberod (sample)",  
"contactid":"7ddd0b31-ed8b-e511-80d2-00155d2a68d4"  
}  
}  
```  
  
<a name="BKMK_FilterNavProperties"></a>

## <a name="filter-records-based-on-single-valued-navigation-property"></a>Filter records based on single-valued navigation property

 Navigation properties let you access data related to the current entity. *Single-valued* navigation properties correspond to Lookup attributes that support many-to-one relationships and allow setting a reference to another entity. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Navigation properties](web-api-types-operations.md#bkmk_navprops)  
  
 You can filter your entity set records based on single-valued navigation property  values. For example, you can retrieve child accounts for the specified account. You can only use the primary attribute value of the entity referenced by the single-valued navigation property to filter records.  
  
> [!NOTE]
>  The capability to filter records  based on single-valued navigation property was introduced in [!INCLUDE[pn_crm_8_1_0_online](../../includes/pn-crm-8-1-0-online.md)] and [!INCLUDE[pn_crm_8_1_0_op](../../includes/pn-crm-8-1-0-op.md)].  
  
 Ví dụ:  
  
-   Retrieve all the matching accounts for a specified Contact ID  
  
    **Yêu cầu** 
 
    ```http 
    GET [Organization URI]/api/data/v9.0/accounts?$select=name&$filter=primarycontactid/contactid%20eq%20a0dbf27c-8efb-e511-80d2-00155db07c77 HTTP/1.1  
    Accept: application/json  
    OData-MaxVersion: 4.0  
    OData-Version: 4.0  
    ```  
  
    **Phản hồi**  

    ```http 
    HTTP/1.1 200 OK  
    Content-Type: application/json; odata.metadata=minimal  
    OData-Version: 4.0  
  
    {  
    "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts(name)",  
    "value":[  
    {  
    "@odata.etag":"W/\"513479\"",  
    "name":"Adventure Works (sample)",  
    "accountid":"3adbf27c-8efb-e511-80d2-00155db07c77"  
    },{  
    "@odata.etag":"W/\"514057\"",  
    "name":"Blue Yonder Airlines (sample)",  
    "accountid":"3edbf27c-8efb-e511-80d2-00155db07c77"  
    }  
    ]  
    }  
    ```  
  
-   Retrieve child accounts for the specified Account ID.  
  
    **Yêu cầu**  

    ```http 
    GET [Organization URI]/api/data/v9.0/accounts?$select=name&$filter=parentaccountid/accountid%20eq%203adbf27c-8efb-e511-80d2-00155db07c77  
    Accept: application/json  
    OData-MaxVersion: 4.0  
    OData-Version: 4.0  
    ```  
  
    **Phản hồi**  

    ```http 
    HTTP/1.1 200 OK  
    Content-Type: application/json; odata.metadata=minimal  
    OData-Version: 4.0  
  
    {  
    "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts(name)",  
    "value":[  
    {  
    "@odata.etag":"W/\"514058\"",  
    "name":"Sample Child Account 1",  
    "accountid":"915e89f5-29fc-e511-80d2-00155db07c77"  
    },{  
    "@odata.etag":"W/\"514061\"",  
    "name":"Sample Child Account 2",  
    "accountid":"03312500-2afc-e511-80d2-00155db07c77"  
    }  
    ]  
    }    
    ```  
  
<a name="bkmk_expandRelated"></a>

## <a name="retrieve-related-entities-by-expanding-navigation-properties"></a>Retrieve related entities by expanding navigation properties

 Use the `$expand` system query option in the navigation properties to control what data from related entities is returned. There are two types of navigation properties:  
  
- *Single-valued* navigation properties correspond to Lookup attributes that support many-to-one relationships and allow setting a reference to another entity.  
  
- *Collection-valued* navigation properties correspond to one-to-many or many-to-many relationships.  
  
  If you include only the name of the navigation property, you’ll receive all the properties for related records. You can limit the properties returned for related records using the `$select` system query option in parentheses after the navigation property name. Use this for both single-valued and collection-valued navigation properties.  
  
> [!NOTE]
>  The capability to retrieve  related entities for entity sets was introduced in [!INCLUDE[pn_crm_8_1_0_online](../../includes/pn-crm-8-1-0-online.md)] and [!INCLUDE[pn_crm_8_1_0_op](../../includes/pn-crm-8-1-0-op.md)].  
> 
>  To retrieve related entities for an entity instance, see [Retrieve related entities for an entity by expanding navigation properties](retrieve-entity-using-web-api.md#bkmk_expandRelated).  
  
- **Retrieve related entities by expanding single-valued navigation properties**: The following example demonstrates how to retrieve the contact for all the account records. For the related contact records, we are only retrieving the contactid and fullname.  
  
     **Yêu cầu**  

    ```http 
    GET [Organization URI]/api/data/v9.0/accounts?$select=name&$expand=primarycontactid($select=contactid,fullname) HTTP/1.1  
    Accept: application/json  
    OData-MaxVersion: 4.0  
    OData-Version: 4.0  
    ```  
  
     **Phản hồi** 
 
    ```http 
    HTTP/1.1 200 OK  
    Content-Type: application/json; odata.metadata=minimal  
    OData-Version: 4.0  
  
    {  
    "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts(name,primarycontactid,primarycontactid(contactid,fullname))","value":[  
    {  
    "@odata.etag":"W/\"513475\"","name":"Fourth Coffee (sample)","accountid":"36dbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "contactid":"9cdbf27c-8efb-e511-80d2-00155db07c77","fullname":"Yvonne McKay (sample)"  
    }  
    },{  
    "@odata.etag":"W/\"513477\"","name":"Litware, Inc. (sample)","accountid":"38dbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "contactid":"9edbf27c-8efb-e511-80d2-00155db07c77","fullname":"Susanna Stubberod (sample)"  
    }  
    },{  
    "@odata.etag":"W/\"513479\"","name":"Adventure Works (sample)","accountid":"3adbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "contactid":"a0dbf27c-8efb-e511-80d2-00155db07c77","fullname":"Nancy Anderson (sample)"  
    }  
    },{  
    "@odata.etag":"W/\"513481\"","name":"Fabrikam, Inc. (sample)","accountid":"3cdbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "contactid":"a2dbf27c-8efb-e511-80d2-00155db07c77","fullname":"Maria Campbell (sample)"  
    }  
    },{  
    "@odata.etag":"W/\"514057\"","name":"Blue Yonder Airlines (sample)","accountid":"3edbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "contactid":"a0dbf27c-8efb-e511-80d2-00155db07c77","fullname":"Nancy Anderson (sample)"  
    }  
    },{  
    "@odata.etag":"W/\"513485\"","name":"City Power & Light (sample)","accountid":"40dbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "contactid":"a6dbf27c-8efb-e511-80d2-00155db07c77","fullname":"Scott Konersmann (sample)"  
    }  
    },{  
    "@odata.etag":"W/\"513487\"","name":"Contoso Pharmaceuticals (sample)","accountid":"42dbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "contactid":"a8dbf27c-8efb-e511-80d2-00155db07c77","fullname":"Robert Lyon (sample)"  
    }  
    },{  
    "@odata.etag":"W/\"513489\"","name":"Alpine Ski House (sample)","accountid":"44dbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "contactid":"aadbf27c-8efb-e511-80d2-00155db07c77","fullname":"Paul Cannon (sample)"  
    }  
    },{  
    "@odata.etag":"W/\"513491\"","name":"A. Datum Corporation (sample)","accountid":"46dbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "contactid":"acdbf27c-8efb-e511-80d2-00155db07c77","fullname":"Rene Valdes (sample)"  
    }  
    },{  
    "@odata.etag":"W/\"513493\"","name":"Coho Winery (sample)","accountid":"48dbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "contactid":"aedbf27c-8efb-e511-80d2-00155db07c77","fullname":"Jim Glynn (sample)"  
    }  
    }  
    ]  
    }    
    ```  

Instead of returning the related entities for entity sets, you can also return references (links) to the related entities by expanding the single-valued navigation property with the `$ref` option. The following example returns links to the contact records for all the accounts.  
  
 **Yêu cầu**

```http  
    GET [Organization URI]/api/data/v9.0/accounts?$select=name&$expand=primarycontactid/$ref HTTP/1.1  
    Accept: application/json  
    OData-MaxVersion: 4.0  
    OData-Version: 4.0  
```  
  
 **Phản hồi**
 
```http 
    HTTP/1.1 200 OK  
    Content-Type: application/json; odata.metadata=minimal  
    OData-Version: 4.0  
  
    {  
    "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts(name,primarycontactid)","value":[  
    {  
    "@odata.etag":"W/\"513475\"","name":"Fourth Coffee (sample)","_primarycontactid_value":"9cdbf27c-8efb-e511-80d2-00155db07c77","accountid":"36dbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "@odata.id":"[Organization URI]/api/data/v9.0/contacts(9cdbf27c-8efb-e511-80d2-00155db07c77)"  
    }  
    },{  
    "@odata.etag":"W/\"513477\"","name":"Litware, Inc. (sample)","_primarycontactid_value":"9edbf27c-8efb-e511-80d2-00155db07c77","accountid":"38dbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "@odata.id":"[Organization URI]/api/data/v9.0/contacts(9edbf27c-8efb-e511-80d2-00155db07c77)"  
    }  
    },{  
    "@odata.etag":"W/\"513479\"","name":"Adventure Works (sample)","_primarycontactid_value":"a0dbf27c-8efb-e511-80d2-00155db07c77","accountid":"3adbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "@odata.id":"[Organization URI]/api/data/v9.0/contacts(a0dbf27c-8efb-e511-80d2-00155db07c77)"  
    }  
    },{  
    "@odata.etag":"W/\"513481\"","name":"Fabrikam, Inc. (sample)","_primarycontactid_value":"a2dbf27c-8efb-e511-80d2-00155db07c77","accountid":"3cdbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "@odata.id":"[Organization URI]/api/data/v9.0/contacts(a2dbf27c-8efb-e511-80d2-00155db07c77)"  
    }  
    },{  
    "@odata.etag":"W/\"514057\"","name":"Blue Yonder Airlines (sample)","_primarycontactid_value":"a0dbf27c-8efb-e511-80d2-00155db07c77","accountid":"3edbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "@odata.id":"[Organization URI]/api/data/v9.0/contacts(a0dbf27c-8efb-e511-80d2-00155db07c77)"  
    }  
    },{  
    "@odata.etag":"W/\"513485\"","name":"City Power & Light (sample)","_primarycontactid_value":"a6dbf27c-8efb-e511-80d2-00155db07c77","accountid":"40dbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "@odata.id":"[Organization URI]/api/data/v9.0/contacts(a6dbf27c-8efb-e511-80d2-00155db07c77)"  
    }  
    },{  
    "@odata.etag":"W/\"513487\"","name":"Contoso Pharmaceuticals (sample)","_primarycontactid_value":"a8dbf27c-8efb-e511-80d2-00155db07c77","accountid":"42dbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "@odata.id":"[Organization URI]/api/data/v9.0/contacts(a8dbf27c-8efb-e511-80d2-00155db07c77)"  
    }  
    },{  
    "@odata.etag":"W/\"513489\"","name":"Alpine Ski House (sample)","_primarycontactid_value":"aadbf27c-8efb-e511-80d2-00155db07c77","accountid":"44dbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "@odata.id":"[Organization URI]/api/data/v9.0/contacts(aadbf27c-8efb-e511-80d2-00155db07c77)"  
    }  
    },{  
    "@odata.etag":"W/\"513491\"","name":"A. Datum Corporation (sample)","_primarycontactid_value":"acdbf27c-8efb-e511-80d2-00155db07c77","accountid":"46dbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "@odata.id":"[Organization URI]/api/data/v9.0/contacts(acdbf27c-8efb-e511-80d2-00155db07c77)"  
    }  
    },{  
    "@odata.etag":"W/\"513493\"","name":"Coho Winery (sample)","_primarycontactid_value":"aedbf27c-8efb-e511-80d2-00155db07c77","accountid":"48dbf27c-8efb-e511-80d2-00155db07c77","primarycontactid":{  
    "@odata.id":"[Organization URI]/api/data/v9.0/contacts(aedbf27c-8efb-e511-80d2-00155db07c77)"  
    }  
    }  
    ]  
    }  
```  

- **Retrieve related entities by expanding collection-valued navigation properties**: If you expand on collection-valued navigation parameters to retrieve related entities for entity sets, an @odata.nextLink property will be returned for the related entities. You should use the value of the @odata.nextLink property with a new GET request to return the required data.  
  
    The following example retrieves the tasks assigned to the top 5 account records.  
  
     **Yêu cầu**

    ```http 
        GET [Organization URI]/api/data/v9.0/accounts?$top=5&$select=name&$expand=Account_Tasks($select%20=%20subject,%20scheduledstart) HTTP/1.1  
        Accept: application/json  
        OData-MaxVersion: 4.0  
        OData-Version: 4.0  
    ```  
  
     **Phản hồi** 
 
    ```http 
        HTTP/1.1 200 OK  
        Content-Type: application/json; odata.metadata=minimal  
        OData-Version: 4.0  
  
        {  
        "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts(name,Account_Tasks,Account_Tasks(subject,scheduledstart))","value":[  
        {  
        "@odata.etag":"W/\"513475\"","name":"Fourth Coffee (sample)","accountid":"36dbf27c-8efb-e511-80d2-00155db07c77","Account_Tasks":[  
  
        ],"Account_Tasks@odata.nextLink":"[Organization URI]/api/data/v9.0/accounts(36dbf27c-8efb-e511-80d2-00155db07c77)/Account_Tasks?$select%20=%20subject,%20scheduledstart"  
        },{  
        "@odata.etag":"W/\"513477\"","name":"Litware, Inc. (sample)","accountid":"38dbf27c-8efb-e511-80d2-00155db07c77","Account_Tasks":[  
  
        ],"Account_Tasks@odata.nextLink":"[Organization URI]/api/data/v9.0/accounts(38dbf27c-8efb-e511-80d2-00155db07c77)/Account_Tasks?$select%20=%20subject,%20scheduledstart"  
        },{  
        "@odata.etag":"W/\"514074\"","name":"Adventure Works (sample)","accountid":"3adbf27c-8efb-e511-80d2-00155db07c77","Account_Tasks":[  
  
        ],"Account_Tasks@odata.nextLink":"[Organization URI]/api/data/v9.0/accounts(3adbf27c-8efb-e511-80d2-00155db07c77)/Account_Tasks?$select%20=%20subject,%20scheduledstart"  
        },{  
        "@odata.etag":"W/\"513481\"","name":"Fabrikam, Inc. (sample)","accountid":"3cdbf27c-8efb-e511-80d2-00155db07c77","Account_Tasks":[  
  
        ],"Account_Tasks@odata.nextLink":"[Organization URI]/api/data/v9.0/accounts(3cdbf27c-8efb-e511-80d2-00155db07c77)/Account_Tasks?$select%20=%20subject,%20scheduledstart"  
        },{  
        "@odata.etag":"W/\"514057\"","name":"Blue Yonder Airlines (sample)","accountid":"3edbf27c-8efb-e511-80d2-00155db07c77","Account_Tasks":[  
  
        ],"Account_Tasks@odata.nextLink":"[Organization URI]/api/data/v9.0/accounts(3edbf27c-8efb-e511-80d2-00155db07c77)/Account_Tasks?$select%20=%20subject,%20scheduledstart"  
        }  
        ]  
        }  
    ```  
  
- **Retrieve related entities by expanding both single-valued and collection-valued navigation properties**: The following example demonstrates how you can expand related entities for entity sets using both single- and collection-valued navigation properties. As explained earlier, expanding on collection-valued navigation properties to retrieve related entities for entity sets returns an @odata.nextLink property for the related entities. You should use the value of the @odata.nextLink property with a new GET request to return the required data.  
  
     In this example, we are retrieving the contact and tasks assigned to the top 3 accounts.  
  
     **Yêu cầu**

    ```http 
    GET [Organization URI]/api/data/v9.0/accounts?$top=3&$select=name&$expand=primarycontactid($select=contactid,fullname),Account_Tasks($select=subject,scheduledstart)  HTTP/1.1  
    Accept: application/json  
    OData-MaxVersion: 4.0  
    OData-Version: 4.0  
    ```  
  
     **Phản hồi**  

    ```http 
    HTTP/1.1 200 OK  
    Content-Type: application/json; odata.metadata=minimal  
    OData-Version: 4.0  
  
    {  
    "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#accounts(name,primarycontactid,Account_Tasks,primarycontactid(contactid,fullname),Account_Tasks(subject,scheduledstart))","value":[  
    {  
    "@odata.etag":"W/\"550614\"",  
    "name":"Fourth Coffee (sample)",  
    "accountid":"5b9648c3-68f7-e511-80d3-00155db53318",  
    "primarycontactid":{  
    "contactid":"c19648c3-68f7-e511-80d3-00155db53318",  
    "fullname":"Yvonne McKay (sample)"  
    },  
    "Account_Tasks":[  
  
    ],"Account_Tasks@odata.nextLink":"[Organization URI]/api/data/v9.0/accounts(5b9648c3-68f7-e511-80d3-00155db53318)/Account_Tasks?$select=subject,scheduledstart"  
    },{  
    "@odata.etag":"W/\"550615\"",  
    "name":"Litware, Inc. (sample)",  
    "accountid":"5d9648c3-68f7-e511-80d3-00155db53318",  
    "primarycontactid":{  
    "contactid":"c39648c3-68f7-e511-80d3-00155db53318",  
    "fullname":"Susanna Stubberod (sample)"  
    },"Account_Tasks":[  
  
    ],"Account_Tasks@odata.nextLink":"[Organization URI]/api/data/v9.0/accounts(5d9648c3-68f7-e511-80d3-00155db53318)/Account_Tasks?$select=subject,scheduledstart"  
    },{  
    "@odata.etag":"W/\"550616\"",  
    "name":"Adventure Works (sample)",  
    "accountid":"5f9648c3-68f7-e511-80d3-00155db53318",  
    "primarycontactid":{  
    "contactid":"c59648c3-68f7-e511-80d3-00155db53318",  
    "fullname":"Nancy Anderson (sample)"  
    },"Account_Tasks":[  
  
    ],"Account_Tasks@odata.nextLink":"[Organization URI]/api/data/v9.0/accounts(5f9648c3-68f7-e511-80d3-00155db53318)/Account_Tasks?$select=subject,scheduledstart"  
    }  
    ]  
    }  
    ```

## <a name="filter-results-based-on-values-of-collection-valued-navigation-properties"></a>Filter results based on values of collection-valued navigation properties

You cannot use OData $filter to set criteria that applies to values in collection valued navigation properties in a single operation.
You have two options:
*   Construct a query using FetchXML.  More information: Use custom FetchXML
*   Iterate over results filtering individual entities based on values in the collection using multiple operations.

Generally, using FetchXML should provide better performance because the filtering can be applied server-side in a single operation. The example shown below illustrates how to apply filter on values of collection properties for a link-entity.

```xml
<fetch version="1.0" output-format="xml-platform" mapping="logical" distinct="true">
  <entity name="systemuser">
    <attribute name="fullname" />
    <attribute name="businessunitid" />
    <attribute name="title" />
    <attribute name="address1_telephone1" />
    <attribute name="positionid" />
    <attribute name="systemuserid" />
    <order attribute="fullname" descending="false" />
    <link-entity name="teammembership" from="systemuserid" to="systemuserid" visible="false" intersect="true">
      <link-entity name="team" from="teamid" to="teamid" alias="ab">
        <filter type="and">
          <condition attribute="administratorid" operator="eq-userid" />
        </filter>
      </link-entity>
    </link-entity>
  </entity>
</fetch>
```
  
### <a name="see-also"></a>Xem thêm

 [Web API Query Data Sample (C#)](web-api-query-data-sample-csharp.md)   
 [Web API Query Data Sample (Client-side JavaScript)](web-api-query-data-sample-client-side-javascript.md)   
 [Perform operations using the Web API](perform-operations-web-api.md)   
 [Compose Http requests and handle errors](compose-http-requests-handle-errors.md)   
 [Create an entity using the Web API](create-entity-web-api.md)   
 [Retrieve an entity using the Web API](retrieve-entity-using-web-api.md)   
 [Update and delete entities using the Web API](update-delete-entities-using-web-api.md)   
 [Associate and disassociate entities using the Web API](associate-disassociate-entities-using-web-api.md)   
 [Use Web API functions](use-web-api-functions.md)   
 [Use Web API actions](use-web-api-actions.md)   
 [Execute batch operations using the Web API](execute-batch-operations-using-web-api.md)   
 [Impersonate another user using the Web API](impersonate-another-user-web-api.md)   
 [Perform conditional operations using the Web API](perform-conditional-operations-using-web-api.md)