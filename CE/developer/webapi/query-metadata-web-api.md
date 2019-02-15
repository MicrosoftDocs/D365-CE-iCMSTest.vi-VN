---
title: Query metadata using the Web API (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: The capability to query system metadata is available using the Web API as well as using the organization service by using RetrieveMetadataChangesRequest
ms.custom: ''
ms.date: 11/04/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 3ad4a332-a304-421f-a9fa-82ea3e0503fe
caps.latest.revision: 18
author: brandonsimons
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: dc6c350827ff5b22cd866614da657fc28a97e30f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386674"
---
# <a name="query-metadata-using-the-web-api"></a><span data-ttu-id="7fd4b-103">Query metadata using the Web API</span><span class="sxs-lookup"><span data-stu-id="7fd4b-103">Query metadata using the Web API</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="7fd4b-104">Because [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps is a metadata-driven application, developers may need to query the system metadata at run-time to adapt to how an organization has been configured.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-104">Because [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps is a metadata-driven application, developers may need to query the system metadata at run-time to adapt to how an organization has been configured.</span></span> <span data-ttu-id="7fd4b-105">This capability uses a RESTful query style.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-105">This capability uses a RESTful query style.</span></span>

> [!NOTE]
> <span data-ttu-id="7fd4b-106">You can also construct a query using an object-based style using the <xref href="Microsoft.Dynamics.CRM.EntityQueryExpression?text=EntityQueryExpression ComplexType" /> with the <xref href="Microsoft.Dynamics.CRM.RetrieveMetadataChanges?text=RetrieveMetadataChanges Function" />.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-106">You can also construct a query using an object-based style using the <xref href="Microsoft.Dynamics.CRM.EntityQueryExpression?text=EntityQueryExpression ComplexType" /> with the <xref href="Microsoft.Dynamics.CRM.RetrieveMetadataChanges?text=RetrieveMetadataChanges Function" />.</span></span> <span data-ttu-id="7fd4b-107">This function allows for capturing changes to metadata between two periods of time as well as returning a limited set of metadata defined by a query you specify.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-107">This function allows for capturing changes to metadata between two periods of time as well as returning a limited set of metadata defined by a query you specify.</span></span>

<a name="bkmk_QueryingEntityMetadata"></a>

## <a name="querying-the-entitymetadata-entity-type"></a><span data-ttu-id="7fd4b-108">Querying the EntityMetadata entity type</span><span class="sxs-lookup"><span data-stu-id="7fd4b-108">Querying the EntityMetadata entity type</span></span>

<span data-ttu-id="7fd4b-109">You’ll use the same techniques described in [Query Data using the Web API](query-data-web-api.md) when you query EntityMetadata, with a few variations.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-109">You’ll use the same techniques described in [Query Data using the Web API](query-data-web-api.md) when you query EntityMetadata, with a few variations.</span></span> <span data-ttu-id="7fd4b-110">Use the `EntityDefinitions` entity set path to retrieve information about the <xref href="Microsoft.Dynamics.CRM.EntityMetadata?text=EntityMetadata EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-110">Use the `EntityDefinitions` entity set path to retrieve information about the <xref href="Microsoft.Dynamics.CRM.EntityMetadata?text=EntityMetadata EntityType" />.</span></span> <span data-ttu-id="7fd4b-111">EntityMetadata entities contain a lot of data so you will want to be careful to only retrieve the data that you need.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-111">EntityMetadata entities contain a lot of data so you will want to be careful to only retrieve the data that you need.</span></span> <span data-ttu-id="7fd4b-112">The following example shows the data returned for just the `DisplayName`, `IsKnowledgeManagementEnabled`, and `EntitySetName` properties of the metadata for the `Account` entity.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-112">The following example shows the data returned for just the `DisplayName`, `IsKnowledgeManagementEnabled`, and `EntitySetName` properties of the metadata for the `Account` entity.</span></span> <span data-ttu-id="7fd4b-113">The `MetadataId` property value is always returned.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-113">The `MetadataId` property value is always returned.</span></span>  

 <span data-ttu-id="7fd4b-114">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="7fd4b-114">**Request**</span></span>

```http
GET [Organization URI]/api/data/v9.0/EntityDefinitions(LogicalName='account')?$select=DisplayName,IsKnowledgeManagementEnabled,EntitySetName HTTP/1.1  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
```

 <span data-ttu-id="7fd4b-115">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="7fd4b-115">**Response**</span></span>
```http
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  

{  
 "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#EntityDefinitions(DisplayName,IsKnowledgeManagementEnabled,EntitySetName)",  
 "value": [  
  {  
   "DisplayName": {  
    "LocalizedLabels": [  
     {  
      "Label": "Account",  
      "LanguageCode": 1033,  
      "IsManaged": true,  
      "MetadataId": "2a4901bf-2241-db11-898a-0007e9e17ebd",  
      "HasChanged": null  
     }  
    ],  
    "UserLocalizedLabel": {  
     "Label": "Account",  
     "LanguageCode": 1033,  
     "IsManaged": true,  
     "MetadataId": "2a4901bf-2241-db11-898a-0007e9e17ebd",  
     "HasChanged": null  
    }  
   },  
   "IsKnowledgeManagementEnabled": false,  
   "EntitySetName": "accounts",  
   "MetadataId": "70816501-edb9-4740-a16c-6a5efbc05d84"  
  }  
 ]  
}  
```

<span data-ttu-id="7fd4b-116">You can use any of the `EntityMetadata` properties with `$select` system query options and you can use `$filter` on any properties which use primitive or enumeration values.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-116">You can use any of the `EntityMetadata` properties with `$select` system query options and you can use `$filter` on any properties which use primitive or enumeration values.</span></span>  

<span data-ttu-id="7fd4b-117">There are no limits on the number of metadata entities that will be returned in a query.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-117">There are no limits on the number of metadata entities that will be returned in a query.</span></span> <span data-ttu-id="7fd4b-118">There is no paging.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-118">There is no paging.</span></span> <span data-ttu-id="7fd4b-119">All matching resources will be returned in the first response.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-119">All matching resources will be returned in the first response.</span></span>  

<a name="bkmk_filterEnumTypes"></a>

## <a name="use-enum-types-in-filter-operations"></a><span data-ttu-id="7fd4b-120">Use enum types in $filter operations</span><span class="sxs-lookup"><span data-stu-id="7fd4b-120">Use enum types in $filter operations</span></span>

<span data-ttu-id="7fd4b-121">When you need to filter metadata entities based on the value of a property that uses an enumeration, you must include the namespace of the enumeration before the string value.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-121">When you need to filter metadata entities based on the value of a property that uses an enumeration, you must include the namespace of the enumeration before the string value.</span></span> <span data-ttu-id="7fd4b-122">Enum types are used as property values only in metadata entities and complex types.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-122">Enum types are used as property values only in metadata entities and complex types.</span></span> <span data-ttu-id="7fd4b-123">For example, if you need to filter entities based on the `OwnershipType` property, which uses the <xref href="Microsoft.Dynamics.CRM.OwnershipTypes?text=OwnershipTypes EnumType" />, you can use the following `$filter` to return only those entities that are UserOwned.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-123">For example, if you need to filter entities based on the `OwnershipType` property, which uses the <xref href="Microsoft.Dynamics.CRM.OwnershipTypes?text=OwnershipTypes EnumType" />, you can use the following `$filter` to return only those entities that are UserOwned.</span></span>

```http
GET [Organization URI]/api/data/v9.0/EntityDefinitions?$select=LogicalName&$filter=OwnershipType eq Microsoft.Dynamics.CRM.OwnershipTypes'UserOwned'  
```

<a name="bkmk_complexTypesAsFilters"></a>

## <a name="use-complex-types-in-filter-operations"></a><span data-ttu-id="7fd4b-124">Use complex types in $filter operations</span><span class="sxs-lookup"><span data-stu-id="7fd4b-124">Use complex types in $filter operations</span></span>

<span data-ttu-id="7fd4b-125">When you need to filter metadata entities based on the value of a property that uses a complex type, you must include the path to the underlying primitive type.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-125">When you need to filter metadata entities based on the value of a property that uses a complex type, you must include the path to the underlying primitive type.</span></span> <span data-ttu-id="7fd4b-126">Complex types are used as property values only in metadata entities.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-126">Complex types are used as property values only in metadata entities.</span></span> <span data-ttu-id="7fd4b-127">For example, if you need to filter entities based on the CanCreateAttributes property, which uses the <xref href="Microsoft.Dynamics.CRM.BooleanManagedProperty?text=BooleanManagedProperty ComplexType" />, you can use the following `$filter` to return only those entities that have a `Value` of `true`.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-127">For example, if you need to filter entities based on the CanCreateAttributes property, which uses the <xref href="Microsoft.Dynamics.CRM.BooleanManagedProperty?text=BooleanManagedProperty ComplexType" />, you can use the following `$filter` to return only those entities that have a `Value` of `true`.</span></span>

```http
GET [Organization URI]/api/data/v9.0/EntityDefinitions?$select=LogicalName&$filter=CanCreateAttributes/Value eq true  
```

<span data-ttu-id="7fd4b-128">This pattern works with <xref href="Microsoft.Dynamics.CRM.BooleanManagedProperty?text=BooleanManagedProperty ComplexType" /> because the primitive value to check is one level deep.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-128">This pattern works with <xref href="Microsoft.Dynamics.CRM.BooleanManagedProperty?text=BooleanManagedProperty ComplexType" /> because the primitive value to check is one level deep.</span></span> <span data-ttu-id="7fd4b-129">However, this does not work on properties of <xref href="Microsoft.Dynamics.CRM.Label?text=Label ComplexType" />.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-129">However, this does not work on properties of <xref href="Microsoft.Dynamics.CRM.Label?text=Label ComplexType" />.</span></span>  

<a name="bkmk_queryAttributes"></a>

## <a name="querying-entitymetadata-attributes"></a><span data-ttu-id="7fd4b-130">Querying EntityMetadata attributes</span><span class="sxs-lookup"><span data-stu-id="7fd4b-130">Querying EntityMetadata attributes</span></span>

<span data-ttu-id="7fd4b-131">You can query entity attributes in the context of an entity by expanding the `Attributes` collection-valued navigation property but this will only include the common properties available in the <xref href="Microsoft.Dynamics.CRM.AttributeMetadata?text=AttributeMetadata EntityType" /> which all attributes share.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-131">You can query entity attributes in the context of an entity by expanding the `Attributes` collection-valued navigation property but this will only include the common properties available in the <xref href="Microsoft.Dynamics.CRM.AttributeMetadata?text=AttributeMetadata EntityType" /> which all attributes share.</span></span> <span data-ttu-id="7fd4b-132">For example the following query will return the `LogicalName` of the entity and all the expanded Attributes which have an `AttributeType` value equal to the <xref href="Microsoft.Dynamics.CRM.AttributeTypeCode?text=AttributeTypeCode EnumType" /> value of `Picklist`.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-132">For example the following query will return the `LogicalName` of the entity and all the expanded Attributes which have an `AttributeType` value equal to the <xref href="Microsoft.Dynamics.CRM.AttributeTypeCode?text=AttributeTypeCode EnumType" /> value of `Picklist`.</span></span>

<a name="bkmk_queryAttributesexample"></a>

```http
GET [Organization URI]/api/data/v9.0/EntityDefinitions(LogicalName='account')?$select=LogicalName&$expand=Attributes($select=LogicalName;$filter=AttributeType eq Microsoft.Dynamics.CRM.AttributeTypeCode'Picklist')  
```

<span data-ttu-id="7fd4b-133">But you can’t include the `OptionSet` or `GlobalOptionSet` collection-valued navigation properties that <xref href="Microsoft.Dynamics.CRM.PicklistAttributeMetadata?text=PicklistAttributeMetadata EntityType" /> attributes have within the `$select` filter of this query.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-133">But you can’t include the `OptionSet` or `GlobalOptionSet` collection-valued navigation properties that <xref href="Microsoft.Dynamics.CRM.PicklistAttributeMetadata?text=PicklistAttributeMetadata EntityType" /> attributes have within the `$select` filter of this query.</span></span>  

<span data-ttu-id="7fd4b-134">In order to retrieve the properties of a specific type of attribute you must cast the `Attributes` collection-valued navigation property to the type you want.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-134">In order to retrieve the properties of a specific type of attribute you must cast the `Attributes` collection-valued navigation property to the type you want.</span></span> <span data-ttu-id="7fd4b-135">The following query will return only the <xref href="Microsoft.Dynamics.CRM.PicklistAttributeMetadata?text=PicklistAttributeMetadata EntityType" /> attributes and will include the `LogicalName` as well as expanding the `OptionSet` and `GlobalOptionSet` collection-valued navigation properties</span><span class="sxs-lookup"><span data-stu-id="7fd4b-135">The following query will return only the <xref href="Microsoft.Dynamics.CRM.PicklistAttributeMetadata?text=PicklistAttributeMetadata EntityType" /> attributes and will include the `LogicalName` as well as expanding the `OptionSet` and `GlobalOptionSet` collection-valued navigation properties</span></span>  

```http
GET [Organization URI]/api/data/v9.0/EntityDefinitions(LogicalName='account')/Attributes/Microsoft.Dynamics.CRM.PicklistAttributeMetadata?$select=LogicalName&$expand=OptionSet,GlobalOptionSet  
```

> [!NOTE]
> <span data-ttu-id="7fd4b-136">Despite the fact that the `OptionSet` and `GlobalOptionSet` collection-valued navigation properties are defined within <xref href="Microsoft.Dynamics.CRM.EnumAttributeMetadata?text=EnumAttributeMetadata EntityType" />, you cannot cast the attributes to this type.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-136">Despite the fact that the `OptionSet` and `GlobalOptionSet` collection-valued navigation properties are defined within <xref href="Microsoft.Dynamics.CRM.EnumAttributeMetadata?text=EnumAttributeMetadata EntityType" />, you cannot cast the attributes to this type.</span></span> <span data-ttu-id="7fd4b-137">This means that if you want to filter on other types which also inherit these properties (see [Entity types that inherit from EnumAttributeMetadata](/dynamics365/customer-engagement/web-api/enumattributemetadata?view=dynamics-ce-odata-9#Derived_Types) ), you must perform separate queries to filter for each type.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-137">This means that if you want to filter on other types which also inherit these properties (see [Entity types that inherit from EnumAttributeMetadata](/dynamics365/customer-engagement/web-api/enumattributemetadata?view=dynamics-ce-odata-9#Derived_Types) ), you must perform separate queries to filter for each type.</span></span>

<span data-ttu-id="7fd4b-138">Another example of this is accessing the `Precision` property available in <xref href="Microsoft.Dynamics.CRM.MoneyAttributeMetadata?text=MoneyAttributeMetadata EntityType" /> and <xref href="Microsoft.Dynamics.CRM.DecimalAttributeMetadata?text=DecimalAttributeMetadata EntityType" /> attributes.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-138">Another example of this is accessing the `Precision` property available in <xref href="Microsoft.Dynamics.CRM.MoneyAttributeMetadata?text=MoneyAttributeMetadata EntityType" /> and <xref href="Microsoft.Dynamics.CRM.DecimalAttributeMetadata?text=DecimalAttributeMetadata EntityType" /> attributes.</span></span> <span data-ttu-id="7fd4b-139">To access this property you must cast the attributes collection either as <xref href="Microsoft.Dynamics.CRM.MoneyAttributeMetadata?text=MoneyAttributeMetadata EntityType" /> or <xref href="Microsoft.Dynamics.CRM.DecimalAttributeMetadata?text=DecimalAttributeMetadata EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-139">To access this property you must cast the attributes collection either as <xref href="Microsoft.Dynamics.CRM.MoneyAttributeMetadata?text=MoneyAttributeMetadata EntityType" /> or <xref href="Microsoft.Dynamics.CRM.DecimalAttributeMetadata?text=DecimalAttributeMetadata EntityType" />.</span></span> <span data-ttu-id="7fd4b-140">An example showing casting to `MoneyAttributeMetadata` is shown here.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-140">An example showing casting to `MoneyAttributeMetadata` is shown here.</span></span>

```http
GET [Organization URI]/api/data/v9.0/EntityDefinitions(LogicalName='account')/Attributes/Microsoft.Dynamics.CRM.MoneyAttributeMetadata?$select=LogicalName,Precision
```

### <a name="filtering-by-required-level"></a><span data-ttu-id="7fd4b-141">Filtering by required level</span><span class="sxs-lookup"><span data-stu-id="7fd4b-141">Filtering by required level</span></span>

<span data-ttu-id="7fd4b-142">The <xref href="Microsoft.Dynamics.CRM.AttributeMetadata?text=AttributeMetadata EntityType" /> `RequiredLevel` property uses a special <xref href="Microsoft.Dynamics.CRM.AttributeRequiredLevelManagedProperty?text=AttributeRequiredLevelManagedProperty ComplexType" /> where the `Value` property is a <xref href="Microsoft.Dynamics.CRM.AttributeRequiredLevel?text=AttributeRequiredLevel EnumType" />.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-142">The <xref href="Microsoft.Dynamics.CRM.AttributeMetadata?text=AttributeMetadata EntityType" /> `RequiredLevel` property uses a special <xref href="Microsoft.Dynamics.CRM.AttributeRequiredLevelManagedProperty?text=AttributeRequiredLevelManagedProperty ComplexType" /> where the `Value` property is a <xref href="Microsoft.Dynamics.CRM.AttributeRequiredLevel?text=AttributeRequiredLevel EnumType" />.</span></span> <span data-ttu-id="7fd4b-143">In this case you must combine patterns found in [Use complex types in $filter operations](query-metadata-web-api.md#bkmk_complexTypesAsFilters) and [Use enum types in $filter operations](query-metadata-web-api.md#bkmk_filterEnumTypes) to filter by this unique property.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-143">In this case you must combine patterns found in [Use complex types in $filter operations](query-metadata-web-api.md#bkmk_complexTypesAsFilters) and [Use enum types in $filter operations](query-metadata-web-api.md#bkmk_filterEnumTypes) to filter by this unique property.</span></span> <span data-ttu-id="7fd4b-144">The following query will filter those attributes in the account entity that are ApplicationRequired.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-144">The following query will filter those attributes in the account entity that are ApplicationRequired.</span></span>

```http
GET [Organization URI]/api/data/v9.0/EntityDefinitions(LogicalName='account')/Attributes?$select=SchemaName&$filter=RequiredLevel/Value eq Microsoft.Dynamics.CRM.AttributeRequiredLevel'ApplicationRequired'  
```

<a name="bkmk_retrieveAttributes"></a>

## <a name="retrieving-attributes"></a><span data-ttu-id="7fd4b-145">Retrieving attributes</span><span class="sxs-lookup"><span data-stu-id="7fd4b-145">Retrieving attributes</span></span>

<span data-ttu-id="7fd4b-146">When you know the MetadataId for both the EntityMetadata and the AttributeMetadata, you can retrieve an individual attribute and access the property values using a query like the following.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-146">When you know the MetadataId for both the EntityMetadata and the AttributeMetadata, you can retrieve an individual attribute and access the property values using a query like the following.</span></span> <span data-ttu-id="7fd4b-147">This query retrieves the LogicalName property of the attribute as well as expanding the OptionSet collection-valued navigation property.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-147">This query retrieves the LogicalName property of the attribute as well as expanding the OptionSet collection-valued navigation property.</span></span> <span data-ttu-id="7fd4b-148">Note that you must cast the attribute as a Microsoft.Dynamics.CRM.PicklistAttributeMetadata to access the OptionSet collection-valued navigation property.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-148">Note that you must cast the attribute as a Microsoft.Dynamics.CRM.PicklistAttributeMetadata to access the OptionSet collection-valued navigation property.</span></span>  

 <span data-ttu-id="7fd4b-149">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="7fd4b-149">**Request**</span></span>
 ```http
GET [Organization URI]/api/data/v9.0/EntityDefinitions(LogicalName='account')/Attributes(5967e7cc-afbb-4c10-bf7e-e7ef430c52be)/Microsoft.Dynamics.CRM.PicklistAttributeMetadata?$select=LogicalName&$expand=OptionSet HTTP/1.1  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
```

 <span data-ttu-id="7fd4b-150">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="7fd4b-150">**Response**</span></span>
 ```http
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0

{
 "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#EntityDefinitions(70816501-edb9-4740-a16c-6a5efbc05d84)/Attributes/Microsoft.Dynamics.CRM.PicklistAttributeMetadata(LogicalName,OptionSet)/$entity",  
 "LogicalName": "preferredappointmentdaycode",  
 "MetadataId": "5967e7cc-afbb-4c10-bf7e-e7ef430c52be",  
 "OptionSet@odata.context": "[Organization URI]/api/data/v9.0/$metadata#EntityDefinitions(70816501-edb9-4740-a16c-6a5efbc05d84)/Attributes(5967e7cc-afbb-4c10-bf7e-e7ef430c52be)/Microsoft.Dynamics.CRM.PicklistAttributeMetadata/OptionSet/$entity",  
 "OptionSet": {  
  "Options": [  
   {  
    "Value": 0,  
    "Label": {  
     "LocalizedLabels": [  
      {  
       "Label": "Sunday",  
       "LanguageCode": 1033,  
       "IsManaged": true,  
       "MetadataId": "21d6a218-2341-db11-898a-0007e9e17ebd",  
       "HasChanged": null  
      }  
     ],  
     "UserLocalizedLabel": {  
      "Label": "Sunday",  
      "LanguageCode": 1033,  
      "IsManaged": true,  
      "MetadataId": "21d6a218-2341-db11-898a-0007e9e17ebd",  
      "HasChanged": null  
     }  
    },  
    "Description": {  
     "LocalizedLabels": [],  
     "UserLocalizedLabel": null  
    },  
    "Color": null,  
    "IsManaged": true,  
    "MetadataId": null,  
    "HasChanged": null  
   }  
Additional options removed for brevity  
  ],  
  "Description": {  
   "LocalizedLabels": [  
    {  
     "Label": "Day of the week that the account prefers for scheduling service activities.",  
     "LanguageCode": 1033,  
     "IsManaged": true,  
     "MetadataId": "1b67144d-ece0-4e83-a38b-b4d48e3f35d5",  
     "HasChanged": null  
    }  
   ],  
   "UserLocalizedLabel": {  
    "Label": "Day of the week that the account prefers for scheduling service activities.",  
    "LanguageCode": 1033,  
    "IsManaged": true,  
    "MetadataId": "1b67144d-ece0-4e83-a38b-b4d48e3f35d5",  
    "HasChanged": null  
   }  
  },  
  "DisplayName": {  
   "LocalizedLabels": [  
    {  
     "Label": "Preferred Day",  
     "LanguageCode": 1033,  
     "IsManaged": true,  
     "MetadataId": "ebb7e979-f9e3-40cd-a86d-50b479b1c5a4",  
     "HasChanged": null  
    }  
   ],  
   "UserLocalizedLabel": {  
    "Label": "Preferred Day",  
    "LanguageCode": 1033,  
    "IsManaged": true,  
    "MetadataId": "ebb7e979-f9e3-40cd-a86d-50b479b1c5a4",  
    "HasChanged": null  
   }  
  },  
  "IsCustomOptionSet": false,  
  "IsGlobal": false,  
  "IsManaged": true,  
  "IsCustomizable": {  
   "Value": true,  
   "CanBeChanged": false,  
   "ManagedPropertyLogicalName": "iscustomizable"  
  },  
  "Name": "account_preferredappointmentdaycode",  
  "OptionSetType": "Picklist",  
  "IntroducedVersion": null,  
  "MetadataId": "53f9933c-18a0-40a6-b4a5-b9610a101735",  
  "HasChanged": null  
 }  
}  
```

<span data-ttu-id="7fd4b-151">If you don’t require any properties of the attribute and only want the values of a collection-valued navigation property such as OptionsSet, you can include that in the URL and limit the properties with a `$select` system query option for a somewhat more efficient query.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-151">If you don’t require any properties of the attribute and only want the values of a collection-valued navigation property such as OptionsSet, you can include that in the URL and limit the properties with a `$select` system query option for a somewhat more efficient query.</span></span> <span data-ttu-id="7fd4b-152">In the following example only the Options property of the OptionSet are included.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-152">In the following example only the Options property of the OptionSet are included.</span></span>  

 <span data-ttu-id="7fd4b-153">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="7fd4b-153">**Request**</span></span>
 ```http
GET [Organization URI]/api/data/v9.0/EntityDefinitions(LogicalName='account')/Attributes(5967e7cc-afbb-4c10-bf7e-e7ef430c52be)/Microsoft.Dynamics.CRM.PicklistAttributeMetadata/OptionSet?$select=Options HTTP/1.1  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
```

 <span data-ttu-id="7fd4b-154">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="7fd4b-154">**Response**</span></span>
 ```http
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  

{  
 "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#EntityDefinitions('account')/Attributes(5967e7cc-afbb-4c10-bf7e-e7ef430c52be)/Microsoft.Dynamics.CRM.PicklistAttributeMetadata/OptionSet(Options)/$entity",  
 "Options": [{  
   "Value": 0,  
   "Label": {  
    "LocalizedLabels": [{  
     "Label": "Sunday",  
     "LanguageCode": 1033,  
     "IsManaged": true,  
     "MetadataId": "21d6a218-2341-db11-898a-0007e9e17ebd",  
     "HasChanged": null  
    }],  
    "UserLocalizedLabel": {  
     "Label": "Sunday",  
     "LanguageCode": 1033,  
     "IsManaged": true,  
     "MetadataId": "21d6a218-2341-db11-898a-0007e9e17ebd",  
     "HasChanged": null  
    }  
   },  
   "Description": {  
    "LocalizedLabels": [],  
    "UserLocalizedLabel": null  
   },  
   "Color": null,  
   "IsManaged": true,  
   "MetadataId": null,  
   "HasChanged": null  
  }  
Additional options removed for brevity  
 ],  
 "MetadataId": "53f9933c-18a0-40a6-b4a5-b9610a101735"  
}  
```

<a name="bkmk_queryRelationshipMetadata"></a>

## <a name="querying-relationship-metadata"></a><span data-ttu-id="7fd4b-155">Querying relationship metadata</span><span class="sxs-lookup"><span data-stu-id="7fd4b-155">Querying relationship metadata</span></span>

<span data-ttu-id="7fd4b-156">You can retrieve relationship metadata in the context of a given entity much in the same way that you can query attributes.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-156">You can retrieve relationship metadata in the context of a given entity much in the same way that you can query attributes.</span></span> <span data-ttu-id="7fd4b-157">The `ManyToManyRelationships`, `ManyToOneRelationships`, and `OneToManyRelationships` collection-valued navigation properties can be queried just like the `Attributes` collection-valued navigation property.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-157">The `ManyToManyRelationships`, `ManyToOneRelationships`, and `OneToManyRelationships` collection-valued navigation properties can be queried just like the `Attributes` collection-valued navigation property.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="7fd4b-158">[Querying EntityMetadata Attributes](query-metadata-web-api.md#bkmk_queryAttributes)</span><span class="sxs-lookup"><span data-stu-id="7fd4b-158">[Querying EntityMetadata Attributes](query-metadata-web-api.md#bkmk_queryAttributes)</span></span>  

<span data-ttu-id="7fd4b-159">However, entity relationships can also be queried using the `RelationshipDefinitions` entity set.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-159">However, entity relationships can also be queried using the `RelationshipDefinitions` entity set.</span></span> <span data-ttu-id="7fd4b-160">You can use a query like the following to get the `SchemaName` property for every relationship.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-160">You can use a query like the following to get the `SchemaName` property for every relationship.</span></span>

```http
GET [Organization URI]/api/data/v9.0/RelationshipDefinitions?$select=SchemaName  
```

<span data-ttu-id="7fd4b-161">The properties available when querying this entity set are limited to those in the <xref href="Microsoft.Dynamics.CRM.RelationshipMetadataBase?text=RelationshipMetadataBase EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-161">The properties available when querying this entity set are limited to those in the <xref href="Microsoft.Dynamics.CRM.RelationshipMetadataBase?text=RelationshipMetadataBase EntityType" />.</span></span> <span data-ttu-id="7fd4b-162">To access properties from the entity types that inherit from `RelationshipMetadataBase` you need to include a cast in the query like the following one to return only <xref href="Microsoft.Dynamics.CRM.OneToManyRelationshipMetadata?text=OneToManyRelationshipMetadata EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-162">To access properties from the entity types that inherit from `RelationshipMetadataBase` you need to include a cast in the query like the following one to return only <xref href="Microsoft.Dynamics.CRM.OneToManyRelationshipMetadata?text=OneToManyRelationshipMetadata EntityType" />.</span></span>  

```http
GET [Organization URI]/api/data/v9.0/RelationshipDefinitions/Microsoft.Dynamics.CRM.OneToManyRelationshipMetadata?$select=SchemaName  
```

<span data-ttu-id="7fd4b-163">Because the entities returned are typed as `OneToManyRelationshipMetadata`, you can filter on the properties such as `ReferencedEntity` to construct a query to return only the one-to-many entity relationships for a specific entity, such as the account entity as shown in the following query:</span><span class="sxs-lookup"><span data-stu-id="7fd4b-163">Because the entities returned are typed as `OneToManyRelationshipMetadata`, you can filter on the properties such as `ReferencedEntity` to construct a query to return only the one-to-many entity relationships for a specific entity, such as the account entity as shown in the following query:</span></span>  

```http
GET [Organization URI]/api/data/v9.0/RelationshipDefinitions/Microsoft.Dynamics.CRM.OneToManyRelationshipMetadata?$select=SchemaName&$filter=ReferencedEntity eq 'account' 
```

<span data-ttu-id="7fd4b-164">That query will return essentially the same results as the following query, which is filtered because it is included in the `EntityMetadataOneToManyRelationships` collection-valued navigation property of the account entity.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-164">That query will return essentially the same results as the following query, which is filtered because it is included in the `EntityMetadataOneToManyRelationships` collection-valued navigation property of the account entity.</span></span> <span data-ttu-id="7fd4b-165">The difference is that for the previous query you don’t need to know the `MetadataId` for the account entity.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-165">The difference is that for the previous query you don’t need to know the `MetadataId` for the account entity.</span></span>  

```http
GET [Organization URI]/api/data/v9.0/EntityDefinitions(LogicalName='account')/OneToManyRelationships?$select=SchemaName  
```

<a name="bkmk_GlobalOptionSets"></a>

## <a name="querying-global-optionsets"></a><span data-ttu-id="7fd4b-166">Querying Global OptionSets</span><span class="sxs-lookup"><span data-stu-id="7fd4b-166">Querying Global OptionSets</span></span>

<span data-ttu-id="7fd4b-167">You can use the `GlobalOptionSetDefinitions` entity set path to retrieve information about global option sets, but this path does not support the use of the `$filter` system query option.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-167">You can use the `GlobalOptionSetDefinitions` entity set path to retrieve information about global option sets, but this path does not support the use of the `$filter` system query option.</span></span> <span data-ttu-id="7fd4b-168">So, unless you know the `MetadataId` for a specific global option set, you can only retrieve all of them.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-168">So, unless you know the `MetadataId` for a specific global option set, you can only retrieve all of them.</span></span> <span data-ttu-id="7fd4b-169">You can also access the definition of a global option set from within the `GlobalOptionSet` single-valued navigation property for any attribute that uses it.</span><span class="sxs-lookup"><span data-stu-id="7fd4b-169">You can also access the definition of a global option set from within the `GlobalOptionSet` single-valued navigation property for any attribute that uses it.</span></span> <span data-ttu-id="7fd4b-170">This is available for all the [EnumAttributeMetadata EntityType Derived Types](/dynamics365/customer-engagement/web-api/enumattributemetadata?view=dynamics-ce-odata-9#Derived_Types).</span><span class="sxs-lookup"><span data-stu-id="7fd4b-170">This is available for all the [EnumAttributeMetadata EntityType Derived Types](/dynamics365/customer-engagement/web-api/enumattributemetadata?view=dynamics-ce-odata-9#Derived_Types).</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="7fd4b-171">[Retrieving attributes](query-metadata-web-api.md#bkmk_retrieveAttributes)</span><span class="sxs-lookup"><span data-stu-id="7fd4b-171">[Retrieving attributes](query-metadata-web-api.md#bkmk_retrieveAttributes)</span></span>  

### <a name="see-also"></a><span data-ttu-id="7fd4b-172">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="7fd4b-172">See also</span></span>

[<span data-ttu-id="7fd4b-173">Use the Web API with Dynamics 365 for Customer Engagement apps metadata</span><span class="sxs-lookup"><span data-stu-id="7fd4b-173">Use the Web API with Dynamics 365 for Customer Engagement apps metadata</span></span>](use-web-api-metadata.md)<br />
[<span data-ttu-id="7fd4b-174">Retrieve metadata by name or MetadataId</span><span class="sxs-lookup"><span data-stu-id="7fd4b-174">Retrieve metadata by name or MetadataId</span></span>](retrieve-metadata-name-metadataid.md)<br />
[<span data-ttu-id="7fd4b-175">Metadata entites and attributes using the Web API</span><span class="sxs-lookup"><span data-stu-id="7fd4b-175">Metadata entites and attributes using the Web API</span></span>](create-update-entity-definitions-using-web-api.md)<br />
[<span data-ttu-id="7fd4b-176">Metadata entity relationships using the Web API</span><span class="sxs-lookup"><span data-stu-id="7fd4b-176">Metadata entity relationships using the Web API</span></span>](create-update-entity-relationships-using-web-api.md)
