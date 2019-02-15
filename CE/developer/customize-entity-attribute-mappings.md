---
title: Customize entity and attribute mappings (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about mapping attributes between entities that have an entity relationship. Điều này cho phép bạn thiết lập giá trị mặc định cho bản ghi được tạo ra trong ngữ cảnh của bản ghi khác. Use the customization tools in the application to map attributes.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- attribute maps, requirements for
- customizing entity and attribute mappings, using entity and attribute mapping data
- mapping entities and attributes, auto-mapping attributes between entities
- creating or updating attribute map records, requirements for attribute maps
- customizing entity and attribute mappings, creating new entity records that are related
- customizing entity and attribute mappings, auto-mapping attributes between entities
- mapping entities and attributes, mapping behavior in Dynamics CRM
- customizing entity and attribute mappings, using mapping to streamline data entry when creating new records
- customizing entity and attribute mappings, setting default values for records created in context of other records
- customizing entity and attribute mappings, mapping attributes between entities that have entity relationships
- customizing entity and attribute mappings, mapping behavior in Dynamics CRM
- mapping behavior in Dynamics CRM
- entity and attribute mappings, mapping attributes between entities that have entity relationships
- auto-mapping attributes between entities
- mapping entities and attributes, mapping attributes between entities that have entity relationships
ms.assetid: de18a3d7-4d6a-4ec8-8a26-570818a4cf7a
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7c5c60113f13c21423dd31d8433315553308f6c8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386847"
---
# <a name="customize-entity-and-attribute-mappings"></a><span data-ttu-id="769ba-105">Customize entity and attribute mappings</span><span class="sxs-lookup"><span data-stu-id="769ba-105">Customize entity and attribute mappings</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="769ba-106">Bạn có thể ánh xạ các thuộc tính giữa các thực thể có một mối quan hệ thực thể.</span><span class="sxs-lookup"><span data-stu-id="769ba-106">You can map attributes between entities that have an entity relationship.</span></span> <span data-ttu-id="769ba-107">This lets you set default values for a record that is created in the context of another record.</span><span class="sxs-lookup"><span data-stu-id="769ba-107">This lets you set default values for a record that is created in the context of another record.</span></span> <span data-ttu-id="769ba-108">Use the customization tools in the application to map attributes.</span><span class="sxs-lookup"><span data-stu-id="769ba-108">Use the customization tools in the application to map attributes.</span></span> <span data-ttu-id="769ba-109">See [Create and edit entity relationships : Mapping Entity Fields](../customize/map-entity-fields.md#BKMK_mappingEntityFields).</span><span class="sxs-lookup"><span data-stu-id="769ba-109">See [Create and edit entity relationships : Mapping Entity Fields](../customize/map-entity-fields.md#BKMK_mappingEntityFields).</span></span>

<!-- See [Entity and attribute mappings](../customize/default-entity-attribute-mappings.md) for a table that shows the default system entity and field mappings. --> 

<a name="bkmk_BehaviorintheApplication"></a>

## <a name="behavior-in-the-application"></a><span data-ttu-id="769ba-110">Behavior in the application</span><span class="sxs-lookup"><span data-stu-id="769ba-110">Behavior in the application</span></span>

 <span data-ttu-id="769ba-111">Mapping in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps streamlines data entry when you create new records that are associated with another record.</span><span class="sxs-lookup"><span data-stu-id="769ba-111">Mapping in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps streamlines data entry when you create new records that are associated with another record.</span></span> <span data-ttu-id="769ba-112">When an entity has an entity relationship with another entity, you can create new related entity records by using the **Create Related** tab in the ribbon.</span><span class="sxs-lookup"><span data-stu-id="769ba-112">When an entity has an entity relationship with another entity, you can create new related entity records by using the **Create Related** tab in the ribbon.</span></span> <span data-ttu-id="769ba-113">When you create a new record in this manner, mapped data from the primary entity record is copied to the form for the new related entity record.</span><span class="sxs-lookup"><span data-stu-id="769ba-113">When you create a new record in this manner, mapped data from the primary entity record is copied to the form for the new related entity record.</span></span> <span data-ttu-id="769ba-114">By mapping entity attributes, you control what data is copied by adding new mappings in the relationship between the two entities.</span><span class="sxs-lookup"><span data-stu-id="769ba-114">By mapping entity attributes, you control what data is copied by adding new mappings in the relationship between the two entities.</span></span> <span data-ttu-id="769ba-115">If you create a record in any way other than from the associated view of the primary entity, data is not mapped.</span><span class="sxs-lookup"><span data-stu-id="769ba-115">If you create a record in any way other than from the associated view of the primary entity, data is not mapped.</span></span>  

 <span data-ttu-id="769ba-116">For example, you might want to set up a mapping between the address fields in accounts and the address fields in contacts.</span><span class="sxs-lookup"><span data-stu-id="769ba-116">For example, you might want to set up a mapping between the address fields in accounts and the address fields in contacts.</span></span> <span data-ttu-id="769ba-117">With this mapping, when a user adds a contact associated with a specific account, the address fields for the contact are populated automatically.</span><span class="sxs-lookup"><span data-stu-id="769ba-117">With this mapping, when a user adds a contact associated with a specific account, the address fields for the contact are populated automatically.</span></span>  

 <span data-ttu-id="769ba-118">You can map one attribute to multiple target attributes.</span><span class="sxs-lookup"><span data-stu-id="769ba-118">You can map one attribute to multiple target attributes.</span></span> <span data-ttu-id="769ba-119">For example, you can map address information in an account to both the billing and shipping addresses in an order.</span><span class="sxs-lookup"><span data-stu-id="769ba-119">For example, you can map address information in an account to both the billing and shipping addresses in an order.</span></span>  

 <span data-ttu-id="769ba-120">Mapping is applied before a new, related record is created.</span><span class="sxs-lookup"><span data-stu-id="769ba-120">Mapping is applied before a new, related record is created.</span></span> <span data-ttu-id="769ba-121">Users can make changes before saving the record.</span><span class="sxs-lookup"><span data-stu-id="769ba-121">Users can make changes before saving the record.</span></span> <span data-ttu-id="769ba-122">Các thay đổi sau này với các dữ liệu trong bản ghi chính không được áp dụng cho hồ sơ có liên quan.</span><span class="sxs-lookup"><span data-stu-id="769ba-122">Later changes to the data in the primary record are not applied to the related record.</span></span>  

<a name="bkmk_UsingEntityandAttributeMappingData"></a>

## <a name="using-entity-and-attribute-mapping-data"></a><span data-ttu-id="769ba-123">Using entity and attribute mapping data</span><span class="sxs-lookup"><span data-stu-id="769ba-123">Using entity and attribute mapping data</span></span>

### <a name="using-web-api"></a><span data-ttu-id="769ba-124">Using Web API</span><span class="sxs-lookup"><span data-stu-id="769ba-124">Using Web API</span></span>

<span data-ttu-id="769ba-125">When working with the Web API, you can use <xref href="Microsoft.Dynamics.CRM.InitializeFrom?text=InitializeFrom Function" /> to create new records in the context of existing records where a mapping exists between the entities.</span><span class="sxs-lookup"><span data-stu-id="769ba-125">When working with the Web API, you can use <xref href="Microsoft.Dynamics.CRM.InitializeFrom?text=InitializeFrom Function" /> to create new records in the context of existing records where a mapping exists between the entities.</span></span> 

<span data-ttu-id="769ba-126">The response received from InitializeFrom request consists of values of mapped attributes between the source entity and target entity and the GUID of parent record.</span><span class="sxs-lookup"><span data-stu-id="769ba-126">The response received from InitializeFrom request consists of values of mapped attributes between the source entity and target entity and the GUID of parent record.</span></span> <span data-ttu-id="769ba-127">The attribute mapping between entities that have an entity relationship is different for different entity sets and is customizable, so the response from InitializeFrom function request may vary for different entities and organizations.</span><span class="sxs-lookup"><span data-stu-id="769ba-127">The attribute mapping between entities that have an entity relationship is different for different entity sets and is customizable, so the response from InitializeFrom function request may vary for different entities and organizations.</span></span> <span data-ttu-id="769ba-128">When this response is passed in the body of create request of the new record, these attribute values are replicated in the new record.</span><span class="sxs-lookup"><span data-stu-id="769ba-128">When this response is passed in the body of create request of the new record, these attribute values are replicated in the new record.</span></span> <span data-ttu-id="769ba-129">The values of custom mapped attributes also get set in the new record during the process.</span><span class="sxs-lookup"><span data-stu-id="769ba-129">The values of custom mapped attributes also get set in the new record during the process.</span></span>

> [!NOTE] 
> <span data-ttu-id="769ba-130">To determine if two entities can be mapped, use the following Web API request:</span><span class="sxs-lookup"><span data-stu-id="769ba-130">To determine if two entities can be mapped, use the following Web API request:</span></span><br/>`GET [Organization URI]/api/data/v9.0/entitymaps?$select=sourceentityname,targetentityname&$orderby=sourceentityname`

<span data-ttu-id="769ba-131">For more information see [Create a new entity from another entity](webapi/create-entity-web-api.md#create-a-new-entity-from-another-entity).</span><span class="sxs-lookup"><span data-stu-id="769ba-131">For more information see [Create a new entity from another entity](webapi/create-entity-web-api.md#create-a-new-entity-from-another-entity).</span></span>

### <a name="using-organization-service"></a><span data-ttu-id="769ba-132">Using Organization Service</span><span class="sxs-lookup"><span data-stu-id="769ba-132">Using Organization Service</span></span>

 <span data-ttu-id="769ba-133">When creating new records in the context of an existing record where a mapping exists between the entities, you can use the <xref:Microsoft.Crm.Sdk.Messages.InitializeFromRequest> message to define a new record that contains the values specified in the mapping.</span><span class="sxs-lookup"><span data-stu-id="769ba-133">When creating new records in the context of an existing record where a mapping exists between the entities, you can use the <xref:Microsoft.Crm.Sdk.Messages.InitializeFromRequest> message to define a new record that contains the values specified in the mapping.</span></span> <span data-ttu-id="769ba-134">You can then use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span><span class="sxs-lookup"><span data-stu-id="769ba-134">You can then use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span></span>
 <span data-ttu-id="769ba-135"><xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*> method to save the record.</span><span class="sxs-lookup"><span data-stu-id="769ba-135"><xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*> method to save the record.</span></span> <span data-ttu-id="769ba-136">In this manner, any mappings that you define are applied.</span><span class="sxs-lookup"><span data-stu-id="769ba-136">In this manner, any mappings that you define are applied.</span></span>  

 <span data-ttu-id="769ba-137">Valid entity maps are created when an entity relationship is created.</span><span class="sxs-lookup"><span data-stu-id="769ba-137">Valid entity maps are created when an entity relationship is created.</span></span> <span data-ttu-id="769ba-138">Use the `entity_map_attribute_maps` entity relationship to retrieve the attribute maps for the pair of entities specified by the entity map.</span><span class="sxs-lookup"><span data-stu-id="769ba-138">Use the `entity_map_attribute_maps` entity relationship to retrieve the attribute maps for the pair of entities specified by the entity map.</span></span>  
 <span data-ttu-id="769ba-139">You can create or update attribute map records.</span><span class="sxs-lookup"><span data-stu-id="769ba-139">You can create or update attribute map records.</span></span> <span data-ttu-id="769ba-140">The following requirements must be met for attribute maps:</span><span class="sxs-lookup"><span data-stu-id="769ba-140">The following requirements must be met for attribute maps:</span></span>  
- <span data-ttu-id="769ba-141">The <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata> type must match.</span><span class="sxs-lookup"><span data-stu-id="769ba-141">The <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata> type must match.</span></span>
- <span data-ttu-id="769ba-142">The length of the target field cannot be shorter than the source field.</span><span class="sxs-lookup"><span data-stu-id="769ba-142">The length of the target field cannot be shorter than the source field.</span></span>
- <span data-ttu-id="769ba-143">The format must match.</span><span class="sxs-lookup"><span data-stu-id="769ba-143">The format must match.</span></span>
- <span data-ttu-id="769ba-144">The target field must not be used in another mapping.</span><span class="sxs-lookup"><span data-stu-id="769ba-144">The target field must not be used in another mapping.</span></span>
- <span data-ttu-id="769ba-145">The source field must be visible on the entity form.</span><span class="sxs-lookup"><span data-stu-id="769ba-145">The source field must be visible on the entity form.</span></span>
- <span data-ttu-id="769ba-146">The target field must be a field in which a user can enter data.</span><span class="sxs-lookup"><span data-stu-id="769ba-146">The target field must be a field in which a user can enter data.</span></span>
- <span data-ttu-id="769ba-147">Address ID values cannot be mapped.</span><span class="sxs-lookup"><span data-stu-id="769ba-147">Address ID values cannot be mapped.</span></span>
- <span data-ttu-id="769ba-148">PartyList attributes, where <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.AttributeType></span><span class="sxs-lookup"><span data-stu-id="769ba-148">PartyList attributes, where <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.AttributeType></span></span> <span data-ttu-id="769ba-149">is <xref:Microsoft.Xrm.Sdk.Metadata.AttributeTypeCode>.PartyList cannot be mapped.</span><span class="sxs-lookup"><span data-stu-id="769ba-149">is <xref:Microsoft.Xrm.Sdk.Metadata.AttributeTypeCode>.PartyList cannot be mapped.</span></span>

<a name="bkmk_Automapping"></a>

## <a name="auto-mapping-attributes-between-entities"></a><span data-ttu-id="769ba-150">Auto-mapping attributes between entities</span><span class="sxs-lookup"><span data-stu-id="769ba-150">Auto-mapping attributes between entities</span></span>

 <span data-ttu-id="769ba-151">You can edit attribute mappings between entities for entity relationships that support mapping.</span><span class="sxs-lookup"><span data-stu-id="769ba-151">You can edit attribute mappings between entities for entity relationships that support mapping.</span></span> 

 <span data-ttu-id="769ba-152">In addition to creating each attribute map manually, you can use the `AutoMapEntity` message(<xref href="Microsoft.Dynamics.CRM.AutoMapEntity?text=AutoMapEntity Action" /> or <xref:Microsoft.Crm.Sdk.Messages.AutoMapEntityRequest> class) to generate a new set of attribute mappings.</span><span class="sxs-lookup"><span data-stu-id="769ba-152">In addition to creating each attribute map manually, you can use the `AutoMapEntity` message(<xref href="Microsoft.Dynamics.CRM.AutoMapEntity?text=AutoMapEntity Action" /> or <xref:Microsoft.Crm.Sdk.Messages.AutoMapEntityRequest> class) to generate a new set of attribute mappings.</span></span> <span data-ttu-id="769ba-153">This message performs the action found under the **Generate Mappings** menu option in the **More Actions** menu on the toolbar.</span><span class="sxs-lookup"><span data-stu-id="769ba-153">This message performs the action found under the **Generate Mappings** menu option in the **More Actions** menu on the toolbar.</span></span> <span data-ttu-id="769ba-154">This message maps all the attributes between the two related entities where the attribute names and types are identical.</span><span class="sxs-lookup"><span data-stu-id="769ba-154">This message maps all the attributes between the two related entities where the attribute names and types are identical.</span></span> <span data-ttu-id="769ba-155">This message is provided as a productivity enhancement so that you do not have to manually add all attribute mappings.</span><span class="sxs-lookup"><span data-stu-id="769ba-155">This message is provided as a productivity enhancement so that you do not have to manually add all attribute mappings.</span></span> <span data-ttu-id="769ba-156">Instead, you can generate a set of likely mappings and minimize the amount of manual work to add or remove individual mappings to meet your requirements.</span><span class="sxs-lookup"><span data-stu-id="769ba-156">Instead, you can generate a set of likely mappings and minimize the amount of manual work to add or remove individual mappings to meet your requirements.</span></span>  

> [!NOTE]
> <span data-ttu-id="769ba-157">Automatically generating mappings in this manner will remove any previously defined attribute mappings and may include mappings that you do not want.</span><span class="sxs-lookup"><span data-stu-id="769ba-157">Automatically generating mappings in this manner will remove any previously defined attribute mappings and may include mappings that you do not want.</span></span>  

<a name="BKMK_mapping"></a>

## <a name="retrieve-the-entity-and-attribute-mappings"></a><span data-ttu-id="769ba-158">Retrieve the entity and attribute mappings</span><span class="sxs-lookup"><span data-stu-id="769ba-158">Retrieve the entity and attribute mappings</span></span>

 <span data-ttu-id="769ba-159">An easy way to see the mappings that have been created is to use the following FetchXML query.</span><span class="sxs-lookup"><span data-stu-id="769ba-159">An easy way to see the mappings that have been created is to use the following FetchXML query.</span></span> <span data-ttu-id="769ba-160">For more information on how to run this query, see [Use FetchXML to Construct a Query](org-service/use-fetchxml-construct-query.md).</span><span class="sxs-lookup"><span data-stu-id="769ba-160">For more information on how to run this query, see [Use FetchXML to Construct a Query](org-service/use-fetchxml-construct-query.md).</span></span>

```xml

<fetch version='1.0' mapping='logical' distinct='false'>
   <entity name='entitymap'>
      <attribute name='sourceentityname'/>
      <attribute name='targetentityname'/>
      <link-entity name='attributemap' alias='attributemap' to='entitymapid' from='entitymapid' link-type='inner'>
         <attribute name='sourceattributename'/>
         <attribute name='targetattributename'/>
      </link-entity>
   </entity>
 </fetch>
```

### <a name="see-also"></a><span data-ttu-id="769ba-161">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="769ba-161">See also</span></span>

 <span data-ttu-id="769ba-162">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](org-service/use-organization-service-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="769ba-162">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](org-service/use-organization-service-metadata.md) </span></span>  
 [<span data-ttu-id="769ba-163">Create and edit entity relationships: Mapping Entity Fields</span><span class="sxs-lookup"><span data-stu-id="769ba-163">Create and edit entity relationships: Mapping Entity Fields</span></span>](../customize/map-entity-fields.md#BKMK_mappingEntityFields)
