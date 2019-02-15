---
title: Use the Web API with metadata (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: The section provides guidance about how to use the Web API with the entity types included in Web API Metadata EntityType Reference.
ms.custom: ''
ms.date: 11/04/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: a0edc029-c6db-48ac-9538-b0270fe94440
caps.latest.revision: 10
author: brandonsimons
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9bd7012a1426f1a3759947f085962e9c4d9cfbcf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386321"
---
# <a name="use-the-web-api-with-metadata"></a><span data-ttu-id="5d0e1-103">Use the Web API with metadata</span><span class="sxs-lookup"><span data-stu-id="5d0e1-103">Use the Web API with metadata</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5d0e1-104">You can perform any of the metadata operations with the Web API that you can perform using the organization service.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-104">You can perform any of the metadata operations with the Web API that you can perform using the organization service.</span></span> <span data-ttu-id="5d0e1-105">This section provides guidance about how to use the Web API with the entity types included in <xref:Microsoft.Dynamics.CRM.MetadataEntityTypeIndex>.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-105">This section provides guidance about how to use the Web API with the entity types included in <xref:Microsoft.Dynamics.CRM.MetadataEntityTypeIndex>.</span></span>  

<span data-ttu-id="5d0e1-106">There are four entity set paths exposed to perform operations with metadata entities as described in the following table.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-106">There are four entity set paths exposed to perform operations with metadata entities as described in the following table.</span></span>  


|<span data-ttu-id="5d0e1-107">Entity Set Path</span><span class="sxs-lookup"><span data-stu-id="5d0e1-107">Entity Set Path</span></span>|<span data-ttu-id="5d0e1-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5d0e1-108">Description</span></span>|
|--|--|
|<span data-ttu-id="5d0e1-109">[!INCLUDE [cc-webapi-serviceuri](../../includes/cc-webapi-serviceuri.md)]/EntityDefinitions</span><span class="sxs-lookup"><span data-stu-id="5d0e1-109">[!INCLUDE [cc-webapi-serviceuri](../../includes/cc-webapi-serviceuri.md)]/EntityDefinitions</span></span>|<span data-ttu-id="5d0e1-110">Contains <xref href="Microsoft.Dynamics.CRM.EntityMetadata?text=EntityMetadata EntityType" /> entities.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-110">Contains <xref href="Microsoft.Dynamics.CRM.EntityMetadata?text=EntityMetadata EntityType" /> entities.</span></span>|
|<span data-ttu-id="5d0e1-111">[!INCLUDE [cc-webapi-serviceuri](../../includes/cc-webapi-serviceuri.md)]/RelationshipDefinitions</span><span class="sxs-lookup"><span data-stu-id="5d0e1-111">[!INCLUDE [cc-webapi-serviceuri](../../includes/cc-webapi-serviceuri.md)]/RelationshipDefinitions</span></span>   | <span data-ttu-id="5d0e1-112">Contains <xref href="Microsoft.Dynamics.CRM.ManyToManyRelationshipMetadata?text=ManyToManyRelationshipMetadata EntityType" /> and <xref href="Microsoft.Dynamics.CRM.OneToManyRelationshipMetadata?text=OneToManyRelationshipMetadata EntityType" /> as both inherit from <xref href="Microsoft.Dynamics.CRM.RelationshipMetadataBase?text=RelationshipMetadataBase EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-112">Contains <xref href="Microsoft.Dynamics.CRM.ManyToManyRelationshipMetadata?text=ManyToManyRelationshipMetadata EntityType" /> and <xref href="Microsoft.Dynamics.CRM.OneToManyRelationshipMetadata?text=OneToManyRelationshipMetadata EntityType" /> as both inherit from <xref href="Microsoft.Dynamics.CRM.RelationshipMetadataBase?text=RelationshipMetadataBase EntityType" />.</span></span> |
|<span data-ttu-id="5d0e1-113">[!INCLUDE [cc-webapi-serviceuri](../../includes/cc-webapi-serviceuri.md)]/GlobalOptionSetDefinitions</span><span class="sxs-lookup"><span data-stu-id="5d0e1-113">[!INCLUDE [cc-webapi-serviceuri](../../includes/cc-webapi-serviceuri.md)]/GlobalOptionSetDefinitions</span></span> |<span data-ttu-id="5d0e1-114">Contains globally defined <xref href="Microsoft.Dynamics.CRM.BooleanOptionSetMetadata?text=BooleanOptionSetMetadata EntityType" /> and <xref href="Microsoft.Dynamics.CRM.OptionSetMetadata?text=OptionSetMetadata EntityType" /> entities as both inherit from <xref href="Microsoft.Dynamics.CRM.OptionSetMetadata?text=OptionSetMetadata EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-114">Contains globally defined <xref href="Microsoft.Dynamics.CRM.BooleanOptionSetMetadata?text=BooleanOptionSetMetadata EntityType" /> and <xref href="Microsoft.Dynamics.CRM.OptionSetMetadata?text=OptionSetMetadata EntityType" /> entities as both inherit from <xref href="Microsoft.Dynamics.CRM.OptionSetMetadata?text=OptionSetMetadata EntityType" />.</span></span>|
|<span data-ttu-id="5d0e1-115">[!INCLUDE [cc-webapi-serviceuri](../../includes/cc-webapi-serviceuri.md)]/ManagedPropertyDefinitions</span><span class="sxs-lookup"><span data-stu-id="5d0e1-115">[!INCLUDE [cc-webapi-serviceuri](../../includes/cc-webapi-serviceuri.md)]/ManagedPropertyDefinitions</span></span> |[!INCLUDE[internal](../../includes/internal.md)]|

<span data-ttu-id="5d0e1-116">Each metadata entity type uses `MetadataId` as the unique identifier property, which it inherits from the <xref href="Microsoft.Dynamics.CRM.MetadataBase?text=MetadataBase EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-116">Each metadata entity type uses `MetadataId` as the unique identifier property, which it inherits from the <xref href="Microsoft.Dynamics.CRM.MetadataBase?text=MetadataBase EntityType" />.</span></span> <span data-ttu-id="5d0e1-117">While all metadata entities have a `MetadataId`, you can’t query all of them directly.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-117">While all metadata entities have a `MetadataId`, you can’t query all of them directly.</span></span> <span data-ttu-id="5d0e1-118">For example, you can query and perform operations on attributes only in the context of the `EntityMetadata` entity that contains them.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-118">For example, you can query and perform operations on attributes only in the context of the `EntityMetadata` entity that contains them.</span></span>  

<span data-ttu-id="5d0e1-119">These entities have some substantial differences from the entities that store business and application data, for example:</span><span class="sxs-lookup"><span data-stu-id="5d0e1-119">These entities have some substantial differences from the entities that store business and application data, for example:</span></span>  

- <span data-ttu-id="5d0e1-120">The properties for metadata entities use many of the complex and enum types defined in <xref:Microsoft.Dynamics.CRM.ComplexTypeIndex> and <xref:Microsoft.Dynamics.CRM.EnumTypeIndex> rather than the primitive data types used for properties in entities that inherit from <xref href="Microsoft.Dynamics.CRM.crmbaseentity?text=crmbaseentity EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-120">The properties for metadata entities use many of the complex and enum types defined in <xref:Microsoft.Dynamics.CRM.ComplexTypeIndex> and <xref:Microsoft.Dynamics.CRM.EnumTypeIndex> rather than the primitive data types used for properties in entities that inherit from <xref href="Microsoft.Dynamics.CRM.crmbaseentity?text=crmbaseentity EntityType" />.</span></span>  

- <span data-ttu-id="5d0e1-121">Metadata entities follow a different naming convention and maintain the Pascal Case naming style used in the assemblies of the organization service.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-121">Metadata entities follow a different naming convention and maintain the Pascal Case naming style used in the assemblies of the organization service.</span></span>  

- <span data-ttu-id="5d0e1-122">Metadata entities make more extensive use of inheritance, which requires that you may need to perform casts to retrieve the data that you want.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-122">Metadata entities make more extensive use of inheritance, which requires that you may need to perform casts to retrieve the data that you want.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="5d0e1-123">In This Section</span><span class="sxs-lookup"><span data-stu-id="5d0e1-123">In This Section</span></span>

[<span data-ttu-id="5d0e1-124">Query Metadata using the Web API</span><span class="sxs-lookup"><span data-stu-id="5d0e1-124">Query Metadata using the Web API</span></span>](query-metadata-web-api.md)<br />
<span data-ttu-id="5d0e1-125">You can use the Web API to query metadata using a RESTful query style.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-125">You can use the Web API to query metadata using a RESTful query style.</span></span>  

[<span data-ttu-id="5d0e1-126">Retrieve metadata by name or MetadataId</span><span class="sxs-lookup"><span data-stu-id="5d0e1-126">Retrieve metadata by name or MetadataId</span></span>](retrieve-metadata-name-metadataid.md)<br />
<span data-ttu-id="5d0e1-127">Your applications can adapt to configuration changes by querying the metadata.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-127">Your applications can adapt to configuration changes by querying the metadata.</span></span> <span data-ttu-id="5d0e1-128">When you know one of the key properties of a metadata item, you can retrieve metadata definitions using the Web API.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-128">When you know one of the key properties of a metadata item, you can retrieve metadata definitions using the Web API.</span></span>  

[<span data-ttu-id="5d0e1-129">Create and update entity definitions using the Web API</span><span class="sxs-lookup"><span data-stu-id="5d0e1-129">Create and update entity definitions using the Web API</span></span>](create-update-entity-definitions-using-web-api.md)<br />
<span data-ttu-id="5d0e1-130">You can create and update entities and attributes using the Web API to achieve the same results you get with the organization service <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest>, <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest>, <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest>, and <xref:Microsoft.Xrm.Sdk.Messages.UpdateAttributeRequest>.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-130">You can create and update entities and attributes using the Web API to achieve the same results you get with the organization service <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest>, <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest>, <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest>, and <xref:Microsoft.Xrm.Sdk.Messages.UpdateAttributeRequest>.</span></span>  

[<span data-ttu-id="5d0e1-131">Create and update entity relationships using the Web API</span><span class="sxs-lookup"><span data-stu-id="5d0e1-131">Create and update entity relationships using the Web API</span></span>](create-update-entity-relationships-using-web-api.md)<br />
<span data-ttu-id="5d0e1-132">You can check whether entities are eligible to participate in a relationship with other entities and then create or update those relationships using the Web API.</span><span class="sxs-lookup"><span data-stu-id="5d0e1-132">You can check whether entities are eligible to participate in a relationship with other entities and then create or update those relationships using the Web API.</span></span>  

### <a name="see-also"></a><span data-ttu-id="5d0e1-133">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="5d0e1-133">See also</span></span>

[<span data-ttu-id="5d0e1-134">Metadata and data models</span><span class="sxs-lookup"><span data-stu-id="5d0e1-134">Metadata and data models</span></span>](../metadata-data-models.md)<br />
[<span data-ttu-id="5d0e1-135">Browse the Metadata for Your Organization</span><span class="sxs-lookup"><span data-stu-id="5d0e1-135">Browse the Metadata for Your Organization</span></span>](../browse-your-metadata.md)<br />
[<span data-ttu-id="5d0e1-136">Use the Organization service with Dynamics 365 for Customer Engagement apps metadata</span><span class="sxs-lookup"><span data-stu-id="5d0e1-136">Use the Organization service with Dynamics 365 for Customer Engagement apps metadata</span></span>](../org-service/use-organization-service-metadata.md)<br />
[<span data-ttu-id="5d0e1-137">Use the Dynamics 365 for Customer Engagement Web API</span><span class="sxs-lookup"><span data-stu-id="5d0e1-137">Use the Dynamics 365 for Customer Engagement Web API</span></span>](../use-microsoft-dynamics-365-web-api.md)
