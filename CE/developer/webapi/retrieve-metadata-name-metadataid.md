---
title: Retrieve metadata by name or MetadataId (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Dynamics 365 for Customer Engagement (online) Customer Engagement uses a metadata driven architecture to provide the flexibility to create custom entities and additional system entity attributes.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 80bcdd8e-7c4f-4fd5-8708-00345f5d0408
caps.latest.revision: 8
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6bd521a23d58c6ceec0f011e3c022f0d8acaa553
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388281"
---
# <a name="retrieve-metadata-by-name-or-metadataid"></a><span data-ttu-id="d8734-103">Retrieve metadata by name or MetadataId</span><span class="sxs-lookup"><span data-stu-id="d8734-103">Retrieve metadata by name or MetadataId</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d8734-104">Your applications can adapt to configuration changes by querying the metadata.</span><span class="sxs-lookup"><span data-stu-id="d8734-104">Your applications can adapt to configuration changes by querying the metadata.</span></span> <span data-ttu-id="d8734-105">When you know one of the key properties of a metadata item, you can retrieve metadata definitions using the Web API.</span><span class="sxs-lookup"><span data-stu-id="d8734-105">When you know one of the key properties of a metadata item, you can retrieve metadata definitions using the Web API.</span></span>  

<a name="bkmk_byName"></a>

## <a name="retrieve-metadata-items-by-name"></a><span data-ttu-id="d8734-106">Retrieve metadata items by name</span><span class="sxs-lookup"><span data-stu-id="d8734-106">Retrieve metadata items by name</span></span>
  
> [!NOTE]
>  <span data-ttu-id="d8734-107">This capability was added with [!INCLUDE[pn_crm_8_2_0_both](../../includes/pn-crm-8-2-0-both.md)].</span><span class="sxs-lookup"><span data-stu-id="d8734-107">This capability was added with [!INCLUDE[pn_crm_8_2_0_both](../../includes/pn-crm-8-2-0-both.md)].</span></span>  
  
 <span data-ttu-id="d8734-108">All retrievable metadata items have a `MetadataId` primary key that can be used to retrieve individual items.</span><span class="sxs-lookup"><span data-stu-id="d8734-108">All retrievable metadata items have a `MetadataId` primary key that can be used to retrieve individual items.</span></span> <span data-ttu-id="d8734-109">For those types of metadata which have a defined alternate key, you can retrieve them by name.</span><span class="sxs-lookup"><span data-stu-id="d8734-109">For those types of metadata which have a defined alternate key, you can retrieve them by name.</span></span>  
  
 <span data-ttu-id="d8734-110">Retrieving items by name is generally easier because you probably already have some reference to the metadata item name in your code.</span><span class="sxs-lookup"><span data-stu-id="d8734-110">Retrieving items by name is generally easier because you probably already have some reference to the metadata item name in your code.</span></span> <span data-ttu-id="d8734-111">The following table lists the alternate key properties for retrieving metadata items by name</span><span class="sxs-lookup"><span data-stu-id="d8734-111">The following table lists the alternate key properties for retrieving metadata items by name</span></span>  
  
|<span data-ttu-id="d8734-112">Metadata item</span><span class="sxs-lookup"><span data-stu-id="d8734-112">Metadata item</span></span>|<span data-ttu-id="d8734-113">Alternate Key</span><span class="sxs-lookup"><span data-stu-id="d8734-113">Alternate Key</span></span>|<span data-ttu-id="d8734-114">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="d8734-114">Example</span></span>|  
|-------------------|-------------------|-------------|  
|<span data-ttu-id="d8734-115">Thực thể</span><span class="sxs-lookup"><span data-stu-id="d8734-115">Entity</span></span>|<span data-ttu-id="d8734-116">Tên logic</span><span class="sxs-lookup"><span data-stu-id="d8734-116">LogicalName</span></span>|`GET /api/data/v9.0/EntityDefinitions(LogicalName='account')`|  
|<span data-ttu-id="d8734-117">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="d8734-117">Attribute</span></span>|<span data-ttu-id="d8734-118">Tên logic</span><span class="sxs-lookup"><span data-stu-id="d8734-118">LogicalName</span></span>|`GET /api/data/v9.0/EntityDefinitions(LogicalName='account')/Attributes(LogicalName='emailaddress1')`|  
|<span data-ttu-id="d8734-119">Mối quan hệ</span><span class="sxs-lookup"><span data-stu-id="d8734-119">Relationship</span></span>|<span data-ttu-id="d8734-120">SchemaName</span><span class="sxs-lookup"><span data-stu-id="d8734-120">SchemaName</span></span>|`GET /api/data/v9.0/RelationshipDefinitions(SchemaName='Account_Tasks')`|  
|<span data-ttu-id="d8734-121">Global Option Set</span><span class="sxs-lookup"><span data-stu-id="d8734-121">Global Option Set</span></span>|<span data-ttu-id="d8734-122">Tên</span><span class="sxs-lookup"><span data-stu-id="d8734-122">Name</span></span>|`GET /api/data/v9.0/GlobalOptionSetDefinitions(Name='metric_goaltype')`|  
  
<a name="bkmk_exampleByName"></a>

### <a name="example-retrieve-metadata-items-by-name"></a><span data-ttu-id="d8734-123">Example: Retrieve metadata items by name</span><span class="sxs-lookup"><span data-stu-id="d8734-123">Example: Retrieve metadata items by name</span></span>

 <span data-ttu-id="d8734-124">A common item of metadata that people want to retrieve are the options configured for a particular  attribute.</span><span class="sxs-lookup"><span data-stu-id="d8734-124">A common item of metadata that people want to retrieve are the options configured for a particular  attribute.</span></span> <span data-ttu-id="d8734-125">The following example shows how to retrieve the `OptionSet` and `GlobalOptionSet` properties of a  <xref href="Microsoft.Dynamics.CRM.PicklistAttributeMetadata?text=PicklistAttributeMetadata EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="d8734-125">The following example shows how to retrieve the `OptionSet` and `GlobalOptionSet` properties of a  <xref href="Microsoft.Dynamics.CRM.PicklistAttributeMetadata?text=PicklistAttributeMetadata EntityType" />.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d8734-126">Expanding both the `OptionSet` and `GlobalOptionSet` single-valued navigation properties of   <xref href="Microsoft.Dynamics.CRM.PicklistAttributeMetadata?text=PicklistAttributeMetadata EntityType" /> allows you to get the option definition whether the attribute is configured to use global optionsets or the 'local' optionset within the entity.</span><span class="sxs-lookup"><span data-stu-id="d8734-126">Expanding both the `OptionSet` and `GlobalOptionSet` single-valued navigation properties of   <xref href="Microsoft.Dynamics.CRM.PicklistAttributeMetadata?text=PicklistAttributeMetadata EntityType" /> allows you to get the option definition whether the attribute is configured to use global optionsets or the 'local' optionset within the entity.</span></span> <span data-ttu-id="d8734-127">If it is a 'local' optionset, the  `GlobalOptionSet` property will be null as shown below.</span><span class="sxs-lookup"><span data-stu-id="d8734-127">If it is a 'local' optionset, the  `GlobalOptionSet` property will be null as shown below.</span></span>  
>   
>  <span data-ttu-id="d8734-128">If the attribute used a global optionset, the `GlobalOptionSet` property would contain the defined options and the `OptionSet` property would be null.</span><span class="sxs-lookup"><span data-stu-id="d8734-128">If the attribute used a global optionset, the `GlobalOptionSet` property would contain the defined options and the `OptionSet` property would be null.</span></span>  
  
 <span data-ttu-id="d8734-129">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d8734-129">**Request**</span></span>  

```http  
GET [Organization URI]/api/data/v9.0/EntityDefinitions(LogicalName='account')/Attributes(LogicalName='accountcategorycode')/Microsoft.Dynamics.CRM.PicklistAttributeMetadata?$select=LogicalName&$expand=OptionSet($select=Options),GlobalOptionSet($select=Options) HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
```  
  
 <span data-ttu-id="d8734-130">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d8734-130">**Response**</span></span>  

```http   
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
  
{  
    "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#EntityDefinitions('account')/Attributes/Microsoft.Dynamics.CRM.PicklistAttributeMetadata(LogicalName,OptionSet,GlobalOptionSet,OptionSet(Options),GlobalOptionSet(Options))/$entity",  
    "LogicalName": "accountcategorycode",  
    "MetadataId": "118771ca-6fb9-4f60-8fd4-99b6124b63ad",  
    "OptionSet@odata.context": "[Organization URI]/api/data/v9.0/$metadata#EntityDefinitions('account')/Attributes(118771ca-6fb9-4f60-8fd4-99b6124b63ad)/Microsoft.Dynamics.CRM.PicklistAttributeMetadata/OptionSet(Options)/$entity",  
    "OptionSet": {  
        "Options": [{  
            "Value": 1,  
            "Label": {  
                "LocalizedLabels": [{  
                    "Label": "Preferred Customer",  
                    "LanguageCode": 1033,  
                    "IsManaged": true,  
                    "MetadataId": "0bd8a218-2341-db11-898a-0007e9e17ebd",  
                    "HasChanged": null  
                }],  
                "UserLocalizedLabel": {  
                    "Label": "Preferred Customer",  
                    "LanguageCode": 1033,  
                    "IsManaged": true,  
                    "MetadataId": "0bd8a218-2341-db11-898a-0007e9e17ebd",  
                    "HasChanged": null  
                }  
            },  
            "Description": {  
                "LocalizedLabels": [  
  
                ],  
                "UserLocalizedLabel": null  
            },  
            "Color": null,  
            "IsManaged": true,  
            "MetadataId": null,  
            "HasChanged": null  
        }, {  
            "Value": 2,  
            "Label": {  
                "LocalizedLabels": [{  
                    "Label": "Standard",  
                    "LanguageCode": 1033,  
                    "IsManaged": true,  
                    "MetadataId": "0dd8a218-2341-db11-898a-0007e9e17ebd",  
                    "HasChanged": null  
                }],  
                "UserLocalizedLabel": {  
                    "Label": "Standard",  
                    "LanguageCode": 1033,  
                    "IsManaged": true,  
                    "MetadataId": "0dd8a218-2341-db11-898a-0007e9e17ebd",  
                    "HasChanged": null  
                }  
            },  
            "Description": {  
                "LocalizedLabels": [  
  
                ],  
                "UserLocalizedLabel": null  
            },  
            "Color": null,  
            "IsManaged": true,  
            "MetadataId": null,  
            "HasChanged": null  
        }],  
        "MetadataId": "b994cdd8-5ce9-4ab9-bdd3-8888ebdb0407"  
    },  
    "GlobalOptionSet": null  
}  
```  
  
<a name="bkmk_byMetadataId"></a>
   
## <a name="retrieve-metadata-items-by-metadataid"></a><span data-ttu-id="d8734-131">Retrieve metadata items by MetadataId</span><span class="sxs-lookup"><span data-stu-id="d8734-131">Retrieve metadata items by MetadataId</span></span>

 <span data-ttu-id="d8734-132">Because the `MetadataId` is the primary key for metadata items, retrieving individual items follows the same pattern used to retrieve business data entities.</span><span class="sxs-lookup"><span data-stu-id="d8734-132">Because the `MetadataId` is the primary key for metadata items, retrieving individual items follows the same pattern used to retrieve business data entities.</span></span>  
  
|<span data-ttu-id="d8734-133">Metadata item</span><span class="sxs-lookup"><span data-stu-id="d8734-133">Metadata item</span></span>|<span data-ttu-id="d8734-134">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="d8734-134">Example</span></span>|  
|-------------------|-------------|  
|<span data-ttu-id="d8734-135">Thực thể</span><span class="sxs-lookup"><span data-stu-id="d8734-135">Entity</span></span>|`GET /api/data/v9.0/EntityDefinitions(<Entity MetadataId>)`|  
|<span data-ttu-id="d8734-136">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="d8734-136">Attribute</span></span>|`GET /api/data/v9.0/EntityDefinitions(<Entity MetadataId>)/Attributes(<Attribute MetadataId>)`|  
|<span data-ttu-id="d8734-137">Mối quan hệ</span><span class="sxs-lookup"><span data-stu-id="d8734-137">Relationship</span></span>|`GET /api/data/v9.0/RelationshipDefinitions(<Relationship MetadataId>)`|  
|<span data-ttu-id="d8734-138">Global Option Set</span><span class="sxs-lookup"><span data-stu-id="d8734-138">Global Option Set</span></span>|`GET /api/data/v9.0/GlobalOptionSetDefinitions(<OptionSet MetadataId>)`|  
  
### <a name="example-retrieve-metadata-items-by-metadataid"></a><span data-ttu-id="d8734-139">Example: Retrieve metadata items by MetadataId</span><span class="sxs-lookup"><span data-stu-id="d8734-139">Example: Retrieve metadata items by MetadataId</span></span>  
 <span data-ttu-id="d8734-140">To achieve the same result as shown in [Example: Retrieve metadata items by name](#bkmk_exampleByName), you will need to perform a series of query operations to get the `MetadataId` by filtering by the entity `LogicalName` and then by the attribute `LogicalName`.</span><span class="sxs-lookup"><span data-stu-id="d8734-140">To achieve the same result as shown in [Example: Retrieve metadata items by name](#bkmk_exampleByName), you will need to perform a series of query operations to get the `MetadataId` by filtering by the entity `LogicalName` and then by the attribute `LogicalName`.</span></span>  
  
 <span data-ttu-id="d8734-141">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d8734-141">**Request**</span></span>

```http  
GET [Organization URI]/api/data/v9.0/EntityDefinitions?$filter=LogicalName%20eq%20'account'&$select=MetadataId HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
```  
  
 <span data-ttu-id="d8734-142">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d8734-142">**Response**</span></span>

```http  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
  
{  
  "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#EntityDefinitions(MetadataId)","value":[  
    {  
      "MetadataId":"70816501-edb9-4740-a16c-6a5efbc05d84"  
    }  
  ]  
}  
```  
  
 <span data-ttu-id="d8734-143">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d8734-143">**Request**</span></span>

```http  
GET [Organization URI]/api/data/v9.0/EntityDefinitions(70816501-edb9-4740-a16c-6a5efbc05d84)/Attributes?$filter=LogicalName%20eq%20'accountcategorycode'&$select=MetadataId HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
```  
  
 <span data-ttu-id="d8734-144">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d8734-144">**Response**</span></span>

```http  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
  
{  
    "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#EntityDefinitions(70816501-edb9-4740-a16c-6a5efbc05d84)/Attributes(MetadataId)","value":[  
    {  
        "@odata.type": "#Microsoft.Dynamics.CRM.PicklistAttributeMetadata",  
        "MetadataId": "118771ca-6fb9-4f60-8fd4-99b6124b63ad"  
    }  
    ]  
}  
```  
  
 <span data-ttu-id="d8734-145">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d8734-145">**Request**</span></span>

```http  
GET [Organization URI]/api/data/v9.0/EntityDefinitions(70816501-edb9-4740-a16c-6a5efbc05d84)/Attributes(118771ca-6fb9-4f60-8fd4-99b6124b63ad)/Microsoft.Dynamics.CRM.PicklistAttributeMetadata?$select=LogicalName&$expand=OptionSet($select=Options),GlobalOptionSet($select=Options) HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
```  
  
 <span data-ttu-id="d8734-146">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d8734-146">**Response**</span></span>

```http
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
  
{  
    "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#EntityDefinitions(70816501-edb9-4740-a16c-6a5efbc05d84)/Attributes/Microsoft.Dynamics.CRM.PicklistAttributeMetadata(LogicalName,OptionSet,GlobalOptionSet,OptionSet(Options),GlobalOptionSet(Options))/$entity",  
    "LogicalName": "accountcategorycode",  
    "MetadataId": "118771ca-6fb9-4f60-8fd4-99b6124b63ad",  
    "OptionSet@odata.context": "[Organization URI]/api/data/v9.0/$metadata#EntityDefinitions(70816501-edb9-4740-a16c-6a5efbc05d84)/Attributes(118771ca-6fb9-4f60-8fd4-99b6124b63ad)/Microsoft.Dynamics.CRM.PicklistAttributeMetadata/OptionSet(Options)/$entity",  
    "OptionSet": {  
        "Options": [{  
            "Value": 1,  
            "Label": {  
                "LocalizedLabels": [{  
                    "Label": "Preferred Customer",  
                    "LanguageCode": 1033,  
                    "IsManaged": true,  
                    "MetadataId": "0bd8a218-2341-db11-898a-0007e9e17ebd",  
                    "HasChanged": null  
                }],  
                "UserLocalizedLabel": {  
                    "Label": "Preferred Customer",  
                    "LanguageCode": 1033,  
                    "IsManaged": true,  
                    "MetadataId": "0bd8a218-2341-db11-898a-0007e9e17ebd",  
                    "HasChanged": null  
                }  
            },  
            "Description": {  
                "LocalizedLabels": [  
  
                ],  
                "UserLocalizedLabel": null  
            },  
            "Color": null,  
            "IsManaged": true,  
            "MetadataId": null,  
            "HasChanged": null  
        }, {  
            "Value": 2,  
            "Label": {  
                "LocalizedLabels": [{  
                    "Label": "Standard",  
                    "LanguageCode": 1033,  
                    "IsManaged": true,  
                    "MetadataId": "0dd8a218-2341-db11-898a-0007e9e17ebd",  
                    "HasChanged": null  
                }],  
                "UserLocalizedLabel": {  
                    "Label": "Standard",  
                    "LanguageCode": 1033,  
                    "IsManaged": true,  
                    "MetadataId": "0dd8a218-2341-db11-898a-0007e9e17ebd",  
                    "HasChanged": null  
                }  
            },  
            "Description": {  
                "LocalizedLabels": [  
  
                ],  
                "UserLocalizedLabel": null  
            },  
            "Color": null,  
            "IsManaged": true,  
            "MetadataId": null,  
            "HasChanged": null  
        }],  
        "MetadataId": "b994cdd8-5ce9-4ab9-bdd3-8888ebdb0407"  
    },  
    "GlobalOptionSet": null  
}  
```  
  
### <a name="see-also"></a><span data-ttu-id="d8734-147">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d8734-147">See also</span></span>

 <span data-ttu-id="d8734-148">[Use the Web API with Dynamics 365 for Customer Engagement apps metadata](use-web-api-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="d8734-148">[Use the Web API with Dynamics 365 for Customer Engagement apps metadata](use-web-api-metadata.md) </span></span>  
 <span data-ttu-id="d8734-149">[Query metadata using the Web API](query-metadata-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="d8734-149">[Query metadata using the Web API](query-metadata-web-api.md) </span></span>  
 <span data-ttu-id="d8734-150">[Create and update entity definitions using the Web API](create-update-entity-definitions-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="d8734-150">[Create and update entity definitions using the Web API](create-update-entity-definitions-using-web-api.md) </span></span>  
 [<span data-ttu-id="d8734-151">Create and update entity relationships using the Web API</span><span class="sxs-lookup"><span data-stu-id="d8734-151">Create and update entity relationships using the Web API</span></span>](create-update-entity-relationships-using-web-api.md)
