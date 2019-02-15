---
title: Create and update entity relationships using the Web API (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about creating and updating entity Dynamics 365 for Customer Engagement (online) Customer Engagement uses a metadata driven architecture to provide the flexibility to create custom entities and additional system entity attributes.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 923538e2-15fe-4718-8eae-d939c5d200cd
caps.latest.revision: 15
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 78f974c1f20d22d779a8c501ffae4e1f0efb54b8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388524"
---
# <a name="create-and-update-entity-relationships-using-the-web-api"></a><span data-ttu-id="6f322-103">Create and update entity relationships using the Web API</span><span class="sxs-lookup"><span data-stu-id="6f322-103">Create and update entity relationships using the Web API</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6f322-104">The Web API supports working with relationship metadata.</span><span class="sxs-lookup"><span data-stu-id="6f322-104">The Web API supports working with relationship metadata.</span></span> <span data-ttu-id="6f322-105">The concepts described in [Customize Entity Relationship Metadata](../customize-entity-relationship-metadata.md) also apply to the Web API.</span><span class="sxs-lookup"><span data-stu-id="6f322-105">The concepts described in [Customize Entity Relationship Metadata](../customize-entity-relationship-metadata.md) also apply to the Web API.</span></span>  

<a name="bkmk_RelationshipEligibility"></a>

## <a name="eligibility-for-relationships"></a><span data-ttu-id="6f322-106">Eligibility for relationships</span><span class="sxs-lookup"><span data-stu-id="6f322-106">Eligibility for relationships</span></span>

 <span data-ttu-id="6f322-107">Before you create an entity relationship you should confirm whether the entity is eligible to participate in the relationship.</span><span class="sxs-lookup"><span data-stu-id="6f322-107">Before you create an entity relationship you should confirm whether the entity is eligible to participate in the relationship.</span></span> <span data-ttu-id="6f322-108">You can use the actions listed in the following table to determine eligibility.</span><span class="sxs-lookup"><span data-stu-id="6f322-108">You can use the actions listed in the following table to determine eligibility.</span></span> <span data-ttu-id="6f322-109">These actions correspond to the organization service messages described in [Entity relationship eligibility](../entity-relationship-eligibility.md).</span><span class="sxs-lookup"><span data-stu-id="6f322-109">These actions correspond to the organization service messages described in [Entity relationship eligibility](../entity-relationship-eligibility.md).</span></span>  
  
|<span data-ttu-id="6f322-110">Hành động</span><span class="sxs-lookup"><span data-stu-id="6f322-110">Action</span></span>|<span data-ttu-id="6f322-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="6f322-111">Description</span></span>|  
|------------|-----------------|  
|<xref href="Microsoft.Dynamics.CRM.CanBeReferenced?text=CanBeReferenced Action" />|<span data-ttu-id="6f322-112">Checks whether the specified entity can be the primary entity (one) in a one-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="6f322-112">Checks whether the specified entity can be the primary entity (one) in a one-to-many relationship.</span></span>|  
|<xref href="Microsoft.Dynamics.CRM.CanBeReferencing?text=CanBeReferencing Action" />|<span data-ttu-id="6f322-113">Checks whether the specified entity can be the referencing entity (many) in a one-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="6f322-113">Checks whether the specified entity can be the referencing entity (many) in a one-to-many relationship.</span></span>|  
|<xref href="Microsoft.Dynamics.CRM.CanManyToMany?text=CanManyToMany Action" />|<span data-ttu-id="6f322-114">Checks whether the entity can participate in a many-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="6f322-114">Checks whether the entity can participate in a many-to-many relationship.</span></span>|  
|<xref href="Microsoft.Dynamics.CRM.GetValidManyToMany?text=GetValidManyToMany Function" />|<span data-ttu-id="6f322-115">Returns the set of entities that can participate in a many-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="6f322-115">Returns the set of entities that can participate in a many-to-many relationship.</span></span>|  
|<xref href="Microsoft.Dynamics.CRM.GetValidReferencedEntities?text=GetValidReferencedEntities Function" />|<span data-ttu-id="6f322-116">Returns the set of entities that are valid as the primary entity (one) from the specified entity in a one-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="6f322-116">Returns the set of entities that are valid as the primary entity (one) from the specified entity in a one-to-many relationship.</span></span>|  
|<xref href="Microsoft.Dynamics.CRM.GetValidReferencingEntities?text=GetValidReferencingEntities Function" />|<span data-ttu-id="6f322-117">Returns the set of entities that are valid as the related entity (many) to the specified entity in a one-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="6f322-117">Returns the set of entities that are valid as the related entity (many) to the specified entity in a one-to-many relationship.</span></span>|  
  
<a name="bkmk_createOnetoMany"></a>

## <a name="create-a-one-to-many-relationship"></a><span data-ttu-id="6f322-118">Create a one-to-many relationship</span><span class="sxs-lookup"><span data-stu-id="6f322-118">Create a one-to-many relationship</span></span>

 <span data-ttu-id="6f322-119">When you create a one-to-many relationship, you define it by using the <xref href="Microsoft.Dynamics.CRM.OneToManyRelationshipMetadata?text=OneToManyRelationshipMetadata EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="6f322-119">When you create a one-to-many relationship, you define it by using the <xref href="Microsoft.Dynamics.CRM.OneToManyRelationshipMetadata?text=OneToManyRelationshipMetadata EntityType" />.</span></span> <span data-ttu-id="6f322-120">This definition includes the lookup attribute, which is defined by using <xref href="Microsoft.Dynamics.CRM.LookupAttributeMetadata?text=LookupAttributeMetadata EntityType" /> and also requires complex properties using <xref href="Microsoft.Dynamics.CRM.AssociatedMenuConfiguration?text=AssociatedMenuConfiguration ComplexType" />, <xref href="Microsoft.Dynamics.CRM.CascadeConfiguration?text=CascadeConfiguration ComplexType" />, <xref href="Microsoft.Dynamics.CRM.Label?text=Label ComplexType" /> and <xref href="Microsoft.Dynamics.CRM.LocalizedLabel?text=LocalizedLabel ComplexType" />.</span><span class="sxs-lookup"><span data-stu-id="6f322-120">This definition includes the lookup attribute, which is defined by using <xref href="Microsoft.Dynamics.CRM.LookupAttributeMetadata?text=LookupAttributeMetadata EntityType" /> and also requires complex properties using <xref href="Microsoft.Dynamics.CRM.AssociatedMenuConfiguration?text=AssociatedMenuConfiguration ComplexType" />, <xref href="Microsoft.Dynamics.CRM.CascadeConfiguration?text=CascadeConfiguration ComplexType" />, <xref href="Microsoft.Dynamics.CRM.Label?text=Label ComplexType" /> and <xref href="Microsoft.Dynamics.CRM.LocalizedLabel?text=LocalizedLabel ComplexType" />.</span></span> <span data-ttu-id="6f322-121">The lookup attribute is set to the Lookup single-valued navigation property of the `OneToManyRelationshipMetadata` object and gets created at the same time using *deep insert*.</span><span class="sxs-lookup"><span data-stu-id="6f322-121">The lookup attribute is set to the Lookup single-valued navigation property of the `OneToManyRelationshipMetadata` object and gets created at the same time using *deep insert*.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="6f322-122">[Create related entities in one operation](create-entity-web-api.md#bkmk_CreateRelated) and [One-to-many relationships](../customize-entity-relationship-metadata.md#BKMK_OneToManyRelationships)</span><span class="sxs-lookup"><span data-stu-id="6f322-122">[Create related entities in one operation](create-entity-web-api.md#bkmk_CreateRelated) and [One-to-many relationships](../customize-entity-relationship-metadata.md#BKMK_OneToManyRelationships)</span></span>  
  
 <span data-ttu-id="6f322-123">If you want to apply a custom navigation property name for a one-to-many relationship you can set values for the `ReferencingEntityNavigationPropertyName` and `ReferencedEntityNavigationPropertyName` properties.</span><span class="sxs-lookup"><span data-stu-id="6f322-123">If you want to apply a custom navigation property name for a one-to-many relationship you can set values for the `ReferencingEntityNavigationPropertyName` and `ReferencedEntityNavigationPropertyName` properties.</span></span>  
  
 <span data-ttu-id="6f322-124">Once you have generated the necessary JSON to define the relationship and the lookup attribute, `POST` the JSON to the RelationshipDefinitions entity set.</span><span class="sxs-lookup"><span data-stu-id="6f322-124">Once you have generated the necessary JSON to define the relationship and the lookup attribute, `POST` the JSON to the RelationshipDefinitions entity set.</span></span> <span data-ttu-id="6f322-125">You must include the `@odata.type` property value of Microsoft.Dynamics.CRM.OneToManyRelationshipMetadata to clarify the type of relationship you’re creating because this same entity set is used to create many-to-many relationships.</span><span class="sxs-lookup"><span data-stu-id="6f322-125">You must include the `@odata.type` property value of Microsoft.Dynamics.CRM.OneToManyRelationshipMetadata to clarify the type of relationship you’re creating because this same entity set is used to create many-to-many relationships.</span></span> <span data-ttu-id="6f322-126">The uri for the resulting relationship is returned in the response.</span><span class="sxs-lookup"><span data-stu-id="6f322-126">The uri for the resulting relationship is returned in the response.</span></span>  
  
 <span data-ttu-id="6f322-127">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="6f322-127">**Request**</span></span>  
```http 
POST [Organization URI]/api/data/v9.0/RelationshipDefinitions HTTP/1.1  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
  
{  
 "SchemaName": "new_contact_new_bankaccount",  
 "@odata.type": "Microsoft.Dynamics.CRM.OneToManyRelationshipMetadata",  
 "AssociatedMenuConfiguration": {  
  "Behavior": "UseCollectionName",  
  "Group": "Details",  
  "Label": {  
   "@odata.type": "Microsoft.Dynamics.CRM.Label",  
   "LocalizedLabels": [  
    {  
     "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
     "Label": "Bank Accounts",  
     "LanguageCode": 1033  
    }  
   ],  
   "UserLocalizedLabel": {  
    "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
    "Label": "Bank Accounts",  
    "LanguageCode": 1033  
   }  
  },  
  "Order": 10000  
 },  
 "CascadeConfiguration": {  
  "Assign": "Cascade",  
  "Delete": "Cascade",  
  "Merge": "Cascade",  
  "Reparent": "Cascade",  
  "Share": "Cascade",  
  "Unshare": "Cascade"  
 },  
 "ReferencedAttribute": "contactid",  
 "ReferencedEntity": "contact",  
 "ReferencingEntity": "new_bankaccount",  
 "Lookup": {  
  "AttributeType": "Lookup",  
  "AttributeTypeName": {  
   "Value": "LookupType"  
  },  
  "Description": {  
   "@odata.type": "Microsoft.Dynamics.CRM.Label",  
   "LocalizedLabels": [  
    {  
     "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
     "Label": "The owner of the account",  
     "LanguageCode": 1033  
    }  
   ],  
   "UserLocalizedLabel": {  
    "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
    "Label": "The owner of the account",  
    "LanguageCode": 1033  
   }  
  },  
  "DisplayName": {  
   "@odata.type": "Microsoft.Dynamics.CRM.Label",  
   "LocalizedLabels": [  
    {  
     "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
     "Label": "Account Owner",  
     "LanguageCode": 1033  
    }  
   ],  
   "UserLocalizedLabel": {  
    "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
    "Label": "Account Owner",  
    "LanguageCode": 1033  
   }  
  },  
  "RequiredLevel": {  
   "Value": "ApplicationRequired",  
   "CanBeChanged": true,  
   "ManagedPropertyLogicalName": "canmodifyrequirementlevelsettings"  
  },  
  "SchemaName": "new_AccountOwner",  
  "@odata.type": "Microsoft.Dynamics.CRM.LookupAttributeMetadata"  
 }  
}  
```  
  
 <span data-ttu-id="6f322-128">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="6f322-128">**Response**</span></span>  
```http 
HTTP/1.1 204 No Content  
OData-Version: 4.0  
OData-EntityId: [Organization URI]/api/data/v9.0/RelationshipDefinitions(d475020f-5d7c-e511-80d2-00155d2a68d2)  
```  
  
<a name="bkmk_CreateManyToMany"></a>
  
## <a name="create-a-many-to-many-relationship"></a><span data-ttu-id="6f322-129">Create a many-to-many relationship</span><span class="sxs-lookup"><span data-stu-id="6f322-129">Create a many-to-many relationship</span></span>

 <span data-ttu-id="6f322-130">When you create a many-to-many relationship, you must the relationship by using the <xref href="Microsoft.Dynamics.CRM.ManyToManyRelationshipMetadata?text=ManyToManyRelationshipMetadata EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="6f322-130">When you create a many-to-many relationship, you must the relationship by using the <xref href="Microsoft.Dynamics.CRM.ManyToManyRelationshipMetadata?text=ManyToManyRelationshipMetadata EntityType" />.</span></span> <span data-ttu-id="6f322-131">This definition includes the name of the intersect entity to be created as well as how the relationship should be displayed in the application by using <xref href="Microsoft.Dynamics.CRM.AssociatedMenuConfiguration?text=AssociatedMenuConfiguration ComplexType" />, <xref href="Microsoft.Dynamics.CRM.Label?text=Label ComplexType" /> and <xref href="Microsoft.Dynamics.CRM.LocalizedLabel?text=LocalizedLabel ComplexType" />.</span><span class="sxs-lookup"><span data-stu-id="6f322-131">This definition includes the name of the intersect entity to be created as well as how the relationship should be displayed in the application by using <xref href="Microsoft.Dynamics.CRM.AssociatedMenuConfiguration?text=AssociatedMenuConfiguration ComplexType" />, <xref href="Microsoft.Dynamics.CRM.Label?text=Label ComplexType" /> and <xref href="Microsoft.Dynamics.CRM.LocalizedLabel?text=LocalizedLabel ComplexType" />.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="6f322-132">[Many-to-many relationships](../customize-entity-relationship-metadata.md#BKMK_ManyToManyRelationships)</span><span class="sxs-lookup"><span data-stu-id="6f322-132">[Many-to-many relationships](../customize-entity-relationship-metadata.md#BKMK_ManyToManyRelationships)</span></span>  
  
 <span data-ttu-id="6f322-133">If you want to apply a custom navigation property name for a many-to-many relationship, you can set values for the `Entity1NavigationPropertyName` and `Entity2NavigationPropertyName` properties.</span><span class="sxs-lookup"><span data-stu-id="6f322-133">If you want to apply a custom navigation property name for a many-to-many relationship, you can set values for the `Entity1NavigationPropertyName` and `Entity2NavigationPropertyName` properties.</span></span>  
  
 <span data-ttu-id="6f322-134">Once you have generated the necessary JSON to define the relationship, `POST` the JSON to the RelationshipDefinitions entity set.</span><span class="sxs-lookup"><span data-stu-id="6f322-134">Once you have generated the necessary JSON to define the relationship, `POST` the JSON to the RelationshipDefinitions entity set.</span></span> <span data-ttu-id="6f322-135">You must include the `@odata.type` property value of Microsoft.Dynamics.CRM.ManyToManyRelationshipMetadata to clarify the type of relationship you’re creating because this same entity set is used to create one-to-many relationships.</span><span class="sxs-lookup"><span data-stu-id="6f322-135">You must include the `@odata.type` property value of Microsoft.Dynamics.CRM.ManyToManyRelationshipMetadata to clarify the type of relationship you’re creating because this same entity set is used to create one-to-many relationships.</span></span> <span data-ttu-id="6f322-136">The uri for the resulting relationship is returned in the response.</span><span class="sxs-lookup"><span data-stu-id="6f322-136">The uri for the resulting relationship is returned in the response.</span></span>  
  
 <span data-ttu-id="6f322-137">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="6f322-137">**Request**</span></span>
  
```http 
POST [Organization URI]/api/data/v9.0/RelationshipDefinitions HTTP/1.1  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
  
{  
 "SchemaName": "new_accounts_campaigns",  
 "@odata.type": "Microsoft.Dynamics.CRM.ManyToManyRelationshipMetadata",  
 "Entity1AssociatedMenuConfiguration": {  
  "Behavior": "UseLabel",  
  "Group": "Details",  
  "Label": {  
   "@odata.type": "Microsoft.Dynamics.CRM.Label",  
   "LocalizedLabels": [  
    {  
     "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
     "Label": "Account",  
     "LanguageCode": 1033  
    }  
   ],  
   "UserLocalizedLabel": {  
    "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
    "Label": "Account",  
    "LanguageCode": 1033  
   }  
  },  
  "Order": 10000  
 },  
 "Entity1LogicalName": "account",  
 "Entity2AssociatedMenuConfiguration": {  
  "Behavior": "UseLabel",  
  "Group": "Details",  
  "Label": {  
   "@odata.type": "Microsoft.Dynamics.CRM.Label",  
   "LocalizedLabels": [  
    {  
     "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
     "Label": "Campaign",  
     "LanguageCode": 1033  
    }  
   ],  
   "UserLocalizedLabel": {  
    "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
    "Label": "Campaign",  
    "LanguageCode": 1033  
   }  
  },  
  "Order": 10000  
 },  
 "Entity2LogicalName": "campaign",  
 "IntersectEntityName": "new_accounts_campaigns"  
}  
```  
  
 <span data-ttu-id="6f322-138">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="6f322-138">**Response**</span></span>  
```http 
HTTP/1.1 204 No Content  
OData-Version: 4.0  
OData-EntityId: [Organization URI]/api/data/v9.0/RelationshipDefinitions(420245fa-c77c-e511-80d2-00155d2a68d2)    
```  
  
<a name="bkmk_updateRelationships"></a>

## <a name="update-relationships"></a><span data-ttu-id="6f322-139">Update Relationships</span><span class="sxs-lookup"><span data-stu-id="6f322-139">Update Relationships</span></span>

 <span data-ttu-id="6f322-140">As discussed in [Update entities](create-update-entity-definitions-using-web-api.md#bkmk_updateEntities), you update relationships using the HTTP PUT method to replace the existing definition with changes you want to apply.</span><span class="sxs-lookup"><span data-stu-id="6f322-140">As discussed in [Update entities](create-update-entity-definitions-using-web-api.md#bkmk_updateEntities), you update relationships using the HTTP PUT method to replace the existing definition with changes you want to apply.</span></span> <span data-ttu-id="6f322-141">You can’t edit individual properties using the HTTP PATCH method as you can with business data entities.</span><span class="sxs-lookup"><span data-stu-id="6f322-141">You can’t edit individual properties using the HTTP PATCH method as you can with business data entities.</span></span> <span data-ttu-id="6f322-142">Just like with entities and attributes, you should include a `MSCRM.MergeLabels` header with the value set to `true` to avoid overwriting localized labels not included in your update and you must publish customizations before they are active in the system.</span><span class="sxs-lookup"><span data-stu-id="6f322-142">Just like with entities and attributes, you should include a `MSCRM.MergeLabels` header with the value set to `true` to avoid overwriting localized labels not included in your update and you must publish customizations before they are active in the system.</span></span>  
  
<a name="bkmk_deleteRelationship"></a>
 
## <a name="delete-relationships"></a><span data-ttu-id="6f322-143">Delete Relationships</span><span class="sxs-lookup"><span data-stu-id="6f322-143">Delete Relationships</span></span>

 <span data-ttu-id="6f322-144">To delete a relationship using the Web API, use the HTTP DELETE method with the URI for the relationship.</span><span class="sxs-lookup"><span data-stu-id="6f322-144">To delete a relationship using the Web API, use the HTTP DELETE method with the URI for the relationship.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6f322-145">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="6f322-145">See also</span></span>

 <span data-ttu-id="6f322-146">[Customize entity relationship metadata](../customize-entity-relationship-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="6f322-146">[Customize entity relationship metadata](../customize-entity-relationship-metadata.md) </span></span>  
 <span data-ttu-id="6f322-147">[Use the Web API with Dynamics 365 for Customer Engagement apps metadata](use-web-api-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="6f322-147">[Use the Web API with Dynamics 365 for Customer Engagement apps metadata](use-web-api-metadata.md) </span></span>  
 <span data-ttu-id="6f322-148">[Query Metadata using the Web API](query-metadata-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="6f322-148">[Query Metadata using the Web API](query-metadata-web-api.md) </span></span>  
 <span data-ttu-id="6f322-149">[Retrieve metadata by name or MetadataId](retrieve-metadata-name-metadataid.md) </span><span class="sxs-lookup"><span data-stu-id="6f322-149">[Retrieve metadata by name or MetadataId](retrieve-metadata-name-metadataid.md) </span></span>  
 [<span data-ttu-id="6f322-150">Model entites and attributes using the Web API</span><span class="sxs-lookup"><span data-stu-id="6f322-150">Model entites and attributes using the Web API</span></span>](create-update-entity-definitions-using-web-api.md)
