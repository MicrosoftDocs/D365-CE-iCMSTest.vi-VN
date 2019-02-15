---
title: Create and update entity definitions using the Web API (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about creating and updating entity definitions using the Web API.
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1f430d2d-e829-4ffa-922e-dfcfb7c9e86e
caps.latest.revision: 24
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8adf96e1510ba8c9d81edc31737b03f9619131aa
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387497"
---
# <a name="create-and-update-entity-definitions-using-the-web-api"></a><span data-ttu-id="29a78-103">Create and update entity definitions using the Web API</span><span class="sxs-lookup"><span data-stu-id="29a78-103">Create and update entity definitions using the Web API</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="29a78-104">You can perform all the same operations on model entities that you can with the organization service.</span><span class="sxs-lookup"><span data-stu-id="29a78-104">You can perform all the same operations on model entities that you can with the organization service.</span></span> <span data-ttu-id="29a78-105">This topic focuses on working with metadata entities using the Web API.</span><span class="sxs-lookup"><span data-stu-id="29a78-105">This topic focuses on working with metadata entities using the Web API.</span></span> <span data-ttu-id="29a78-106">To find details about the entity metadata properties, see [Customize Entity Metadata](../customize-entity-metadata.md) and <xref href="Microsoft.Dynamics.CRM.EntityMetadata?text=EntityMetadata EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="29a78-106">To find details about the entity metadata properties, see [Customize Entity Metadata](../customize-entity-metadata.md) and <xref href="Microsoft.Dynamics.CRM.EntityMetadata?text=EntityMetadata EntityType" />.</span></span>  

<a name="bkmk_createEntities"></a>   
## <a name="create-entities"></a><span data-ttu-id="29a78-107">Tạo các thực thể</span><span class="sxs-lookup"><span data-stu-id="29a78-107">Create entities</span></span>  
 <span data-ttu-id="29a78-108">To create an entity, POST the JSON representation of the entity data to the `EntityDefinitions` entity set path.</span><span class="sxs-lookup"><span data-stu-id="29a78-108">To create an entity, POST the JSON representation of the entity data to the `EntityDefinitions` entity set path.</span></span> <span data-ttu-id="29a78-109">The entity must include the definition for the primary name attribute for the entity.</span><span class="sxs-lookup"><span data-stu-id="29a78-109">The entity must include the definition for the primary name attribute for the entity.</span></span> <span data-ttu-id="29a78-110">You don’t need to set values for all the properties.</span><span class="sxs-lookup"><span data-stu-id="29a78-110">You don’t need to set values for all the properties.</span></span> <span data-ttu-id="29a78-111">The items on this list except for Description are required, although setting a description is a recommended best practice.</span><span class="sxs-lookup"><span data-stu-id="29a78-111">The items on this list except for Description are required, although setting a description is a recommended best practice.</span></span> <span data-ttu-id="29a78-112">Property values you do not specify will be set to default values.</span><span class="sxs-lookup"><span data-stu-id="29a78-112">Property values you do not specify will be set to default values.</span></span> <span data-ttu-id="29a78-113">To understand the default values, look at the example in the [Update entities](create-update-entity-definitions-using-web-api.md#bkmk_updateEntities) section.</span><span class="sxs-lookup"><span data-stu-id="29a78-113">To understand the default values, look at the example in the [Update entities](create-update-entity-definitions-using-web-api.md#bkmk_updateEntities) section.</span></span> <span data-ttu-id="29a78-114">The example in this topic uses the following entity properties.</span><span class="sxs-lookup"><span data-stu-id="29a78-114">The example in this topic uses the following entity properties.</span></span>  
  
|<span data-ttu-id="29a78-115">Entity property</span><span class="sxs-lookup"><span data-stu-id="29a78-115">Entity property</span></span>|<span data-ttu-id="29a78-116">Value</span><span class="sxs-lookup"><span data-stu-id="29a78-116">Value</span></span>|  
|---------------------|-----------|  
|<span data-ttu-id="29a78-117">SchemaName</span><span class="sxs-lookup"><span data-stu-id="29a78-117">SchemaName</span></span>|<span data-ttu-id="29a78-118">new_BankAccount **Note:**  You should include the customization prefix that matches the solution publisher.</span><span class="sxs-lookup"><span data-stu-id="29a78-118">new_BankAccount **Note:**  You should include the customization prefix that matches the solution publisher.</span></span> <span data-ttu-id="29a78-119">Here the default value “new_” is used, but you should choose the prefix that works for your solution.</span><span class="sxs-lookup"><span data-stu-id="29a78-119">Here the default value “new_” is used, but you should choose the prefix that works for your solution.</span></span>|  
|<span data-ttu-id="29a78-120">DisplayName</span><span class="sxs-lookup"><span data-stu-id="29a78-120">DisplayName</span></span>|<span data-ttu-id="29a78-121">Bank Account</span><span class="sxs-lookup"><span data-stu-id="29a78-121">Bank Account</span></span>|  
|<span data-ttu-id="29a78-122">DisplayCollectionName</span><span class="sxs-lookup"><span data-stu-id="29a78-122">DisplayCollectionName</span></span>|<span data-ttu-id="29a78-123">Bank Accounts</span><span class="sxs-lookup"><span data-stu-id="29a78-123">Bank Accounts</span></span>|  
|<span data-ttu-id="29a78-124">Mô tả</span><span class="sxs-lookup"><span data-stu-id="29a78-124">Description</span></span>|<span data-ttu-id="29a78-125">An entity to store information about customer bank accounts.</span><span class="sxs-lookup"><span data-stu-id="29a78-125">An entity to store information about customer bank accounts.</span></span>|  
|<span data-ttu-id="29a78-126">OwnershipType</span><span class="sxs-lookup"><span data-stu-id="29a78-126">OwnershipType</span></span>|<span data-ttu-id="29a78-127">UserOwned **Note:**  For the values you can set here, see <xref href="Microsoft.Dynamics.CRM.OwnershipTypes?text=OwnershipTypes EnumType" />.</span><span class="sxs-lookup"><span data-stu-id="29a78-127">UserOwned **Note:**  For the values you can set here, see <xref href="Microsoft.Dynamics.CRM.OwnershipTypes?text=OwnershipTypes EnumType" />.</span></span>|  
|<span data-ttu-id="29a78-128">IsActivity</span><span class="sxs-lookup"><span data-stu-id="29a78-128">IsActivity</span></span>|<span data-ttu-id="29a78-129">false</span><span class="sxs-lookup"><span data-stu-id="29a78-129">false</span></span>|  
|<span data-ttu-id="29a78-130">HasActivities</span><span class="sxs-lookup"><span data-stu-id="29a78-130">HasActivities</span></span>|<span data-ttu-id="29a78-131">false</span><span class="sxs-lookup"><span data-stu-id="29a78-131">false</span></span>|  
|<span data-ttu-id="29a78-132">HasNotes</span><span class="sxs-lookup"><span data-stu-id="29a78-132">HasNotes</span></span>|<span data-ttu-id="29a78-133">false</span><span class="sxs-lookup"><span data-stu-id="29a78-133">false</span></span>|  
  
 <span data-ttu-id="29a78-134">In addition to the properties listed previously, the `EntityMetadataAttributes` property must contain an array that includes one <xref href="Microsoft.Dynamics.CRM.StringAttributeMetadata?text=StringAttributeMetadata EntityType" /> to represent the primary name attribute for the entity.</span><span class="sxs-lookup"><span data-stu-id="29a78-134">In addition to the properties listed previously, the `EntityMetadataAttributes` property must contain an array that includes one <xref href="Microsoft.Dynamics.CRM.StringAttributeMetadata?text=StringAttributeMetadata EntityType" /> to represent the primary name attribute for the entity.</span></span> <span data-ttu-id="29a78-135">The attribute IsPrimaryName property must be true.</span><span class="sxs-lookup"><span data-stu-id="29a78-135">The attribute IsPrimaryName property must be true.</span></span> <span data-ttu-id="29a78-136">The following table describes the properties set in the example.</span><span class="sxs-lookup"><span data-stu-id="29a78-136">The following table describes the properties set in the example.</span></span>  
  
|<span data-ttu-id="29a78-137">Primary Attribute property</span><span class="sxs-lookup"><span data-stu-id="29a78-137">Primary Attribute property</span></span>|<span data-ttu-id="29a78-138">Value</span><span class="sxs-lookup"><span data-stu-id="29a78-138">Value</span></span>|  
|--------------------------------|-----------|  
|<span data-ttu-id="29a78-139">SchemaName</span><span class="sxs-lookup"><span data-stu-id="29a78-139">SchemaName</span></span>|<span data-ttu-id="29a78-140">new_AccountName</span><span class="sxs-lookup"><span data-stu-id="29a78-140">new_AccountName</span></span>|  
|<span data-ttu-id="29a78-141">RequiredLevel</span><span class="sxs-lookup"><span data-stu-id="29a78-141">RequiredLevel</span></span>|<span data-ttu-id="29a78-142">None **Note:**  For the values you can set here, see <xref href="Microsoft.Dynamics.CRM.AttributeRequiredLevelManagedProperty?text=AttributeRequiredLevelManagedProperty ComplexType" /> and <xref href="Microsoft.Dynamics.CRM.AttributeRequiredLevel?text=AttributeRequiredLevel EnumType" />.</span><span class="sxs-lookup"><span data-stu-id="29a78-142">None **Note:**  For the values you can set here, see <xref href="Microsoft.Dynamics.CRM.AttributeRequiredLevelManagedProperty?text=AttributeRequiredLevelManagedProperty ComplexType" /> and <xref href="Microsoft.Dynamics.CRM.AttributeRequiredLevel?text=AttributeRequiredLevel EnumType" />.</span></span>|  
|<span data-ttu-id="29a78-143">MaxLength</span><span class="sxs-lookup"><span data-stu-id="29a78-143">MaxLength</span></span>|<span data-ttu-id="29a78-144">100</span><span class="sxs-lookup"><span data-stu-id="29a78-144">100</span></span>|  
|<span data-ttu-id="29a78-145">FormatName</span><span class="sxs-lookup"><span data-stu-id="29a78-145">FormatName</span></span>|<span data-ttu-id="29a78-146">Text **Note:**  The primary name attribute must use Text format.</span><span class="sxs-lookup"><span data-stu-id="29a78-146">Text **Note:**  The primary name attribute must use Text format.</span></span> <span data-ttu-id="29a78-147">For format options available for other string attributes, see [StringAttributeMetadata formats](../customize-entity-attribute-metadata.md#BKMK_StringAttributeMetadataFormats).</span><span class="sxs-lookup"><span data-stu-id="29a78-147">For format options available for other string attributes, see [StringAttributeMetadata formats](../customize-entity-attribute-metadata.md#BKMK_StringAttributeMetadataFormats).</span></span>|  
|<span data-ttu-id="29a78-148">DisplayName</span><span class="sxs-lookup"><span data-stu-id="29a78-148">DisplayName</span></span>|<span data-ttu-id="29a78-149">Tên Tài khoản</span><span class="sxs-lookup"><span data-stu-id="29a78-149">Account Name</span></span>|  
|<span data-ttu-id="29a78-150">Mô tả</span><span class="sxs-lookup"><span data-stu-id="29a78-150">Description</span></span>|<span data-ttu-id="29a78-151">Type the name of the bank account.</span><span class="sxs-lookup"><span data-stu-id="29a78-151">Type the name of the bank account.</span></span>|  
|<span data-ttu-id="29a78-152">IsPrimaryName</span><span class="sxs-lookup"><span data-stu-id="29a78-152">IsPrimaryName</span></span>|<span data-ttu-id="29a78-153">true</span><span class="sxs-lookup"><span data-stu-id="29a78-153">true</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="29a78-154">When you create or update labels using the <xref href="Microsoft.Dynamics.CRM.Label?text=Label ComplexType" />, you only need to set the `LocalizedLabels` property.</span><span class="sxs-lookup"><span data-stu-id="29a78-154">When you create or update labels using the <xref href="Microsoft.Dynamics.CRM.Label?text=Label ComplexType" />, you only need to set the `LocalizedLabels` property.</span></span> <span data-ttu-id="29a78-155">The `UserLocalizedLabel` value returned is based on the user’s language preference and is read-only.</span><span class="sxs-lookup"><span data-stu-id="29a78-155">The `UserLocalizedLabel` value returned is based on the user’s language preference and is read-only.</span></span>  
  
 <span data-ttu-id="29a78-156">The following example shows the creation of a custom entity with the properties set.</span><span class="sxs-lookup"><span data-stu-id="29a78-156">The following example shows the creation of a custom entity with the properties set.</span></span> <span data-ttu-id="29a78-157">The language is English using the locale ID (LCID) of 1033.</span><span class="sxs-lookup"><span data-stu-id="29a78-157">The language is English using the locale ID (LCID) of 1033.</span></span> [!INCLUDE[LCID](../../includes/lcid.md)]  
  
 <span data-ttu-id="29a78-158">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="29a78-158">**Request**</span></span>  
```http 
POST [Organization URI]/api/data/v9.0/EntityDefinitions HTTP/1.1  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
  
{  
  "@odata.type": "Microsoft.Dynamics.CRM.EntityMetadata",  
 "Attributes": [  
  {  
   "AttributeType": "String",  
   "AttributeTypeName": {  
    "Value": "StringType"  
   },  
   "Description": {  
     "@odata.type": "Microsoft.Dynamics.CRM.Label",  
    "LocalizedLabels": [  
     {  
       "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
      "Label": "Type the name of the bank account",  
      "LanguageCode": 1033  
     }  
    ]  
   },  
   "DisplayName": {  
     "@odata.type": "Microsoft.Dynamics.CRM.Label",  
    "LocalizedLabels": [  
     {  
       "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
      "Label": "Account Name",  
      "LanguageCode": 1033  
     }  
    ]  
   },  
   "IsPrimaryName": true,  
   "RequiredLevel": {  
    "Value": "None",  
    "CanBeChanged": true,  
    "ManagedPropertyLogicalName": "canmodifyrequirementlevelsettings"  
   },  
   "SchemaName": "new_AccountName",  
    "@odata.type": "Microsoft.Dynamics.CRM.StringAttributeMetadata",  
   "FormatName": {  
    "Value": "Text"  
   },  
   "MaxLength": 100  
  }  
 ],  
 "Description": {  
   "@odata.type": "Microsoft.Dynamics.CRM.Label",  
  "LocalizedLabels": [  
   {  
     "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
    "Label": "An entity to store information about customer bank accounts",  
    "LanguageCode": 1033  
   }  
  ]  
 },  
 "DisplayCollectionName": {  
   "@odata.type": "Microsoft.Dynamics.CRM.Label",  
  "LocalizedLabels": [  
   {  
     "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
    "Label": "Bank Accounts",  
    "LanguageCode": 1033  
   }  
  ]  
 },  
 "DisplayName": {  
   "@odata.type": "Microsoft.Dynamics.CRM.Label",  
  "LocalizedLabels": [  
   {  
     "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
    "Label": "Bank Account",  
    "LanguageCode": 1033  
   }  
  ]  
 },  
 "HasActivities": false,  
 "HasNotes": false,  
 "IsActivity": false,  
 "OwnershipType": "UserOwned",  
 "SchemaName": "new_BankAccount"  
}  
```  
  
 <span data-ttu-id="29a78-159">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="29a78-159">**Response**</span></span>  
```http 
HTTP/1.1 204 No Content  
OData-Version: 4.0  
OData-EntityId: [Organization URI]/api/data/v9.0/EntityDefinitions(417129e1-207c-e511-80d2-00155d2a68d2)  
```  
  
<a name="bkmk_updateEntities"></a>
 
## <a name="update-entities"></a><span data-ttu-id="29a78-160">Update entities</span><span class="sxs-lookup"><span data-stu-id="29a78-160">Update entities</span></span>
  
> [!IMPORTANT]
>  <span data-ttu-id="29a78-161">You can’t use the HTTP PATCH method to update model entities.</span><span class="sxs-lookup"><span data-stu-id="29a78-161">You can’t use the HTTP PATCH method to update model entities.</span></span> <span data-ttu-id="29a78-162">The metadata entities have parity with the organization service <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest> that replaces the entity definition with the one included.</span><span class="sxs-lookup"><span data-stu-id="29a78-162">The metadata entities have parity with the organization service <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest> that replaces the entity definition with the one included.</span></span> <span data-ttu-id="29a78-163">Therefore, you must use the HTTP PUT method when updating model entities and be careful to include all the existing properties that you don’t intend to change.</span><span class="sxs-lookup"><span data-stu-id="29a78-163">Therefore, you must use the HTTP PUT method when updating model entities and be careful to include all the existing properties that you don’t intend to change.</span></span> <span data-ttu-id="29a78-164">You can’t update individual properties.</span><span class="sxs-lookup"><span data-stu-id="29a78-164">You can’t update individual properties.</span></span>  
  
 <span data-ttu-id="29a78-165">When you update metadata entities with labels, you should include a custom `MSCRM.MergeLabels` header to control how any labels in the update should be handled.</span><span class="sxs-lookup"><span data-stu-id="29a78-165">When you update metadata entities with labels, you should include a custom `MSCRM.MergeLabels` header to control how any labels in the update should be handled.</span></span> <span data-ttu-id="29a78-166">If a label for an item already has labels for other languages and you update it with a label that contains only one label for a specific language, the `MSCRM.MergeLabels` header controls whether to overwrite the existing labels or merge your new label with any existing language labels.</span><span class="sxs-lookup"><span data-stu-id="29a78-166">If a label for an item already has labels for other languages and you update it with a label that contains only one label for a specific language, the `MSCRM.MergeLabels` header controls whether to overwrite the existing labels or merge your new label with any existing language labels.</span></span> <span data-ttu-id="29a78-167">With `MSCRM.MergeLabels` set to `true`, any new labels defined will only overwrite existing labels when the language code matches.</span><span class="sxs-lookup"><span data-stu-id="29a78-167">With `MSCRM.MergeLabels` set to `true`, any new labels defined will only overwrite existing labels when the language code matches.</span></span> <span data-ttu-id="29a78-168">If you want to overwrite the existing labels to include only the labels you include, set `MSCRM.MergeLabels` to `false`.</span><span class="sxs-lookup"><span data-stu-id="29a78-168">If you want to overwrite the existing labels to include only the labels you include, set `MSCRM.MergeLabels` to `false`.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="29a78-169">If you don’t include a `MSCRM.MergeLabels` header, the default behavior is as if the value were `false` and any localized labels not included in your update will be lost.</span><span class="sxs-lookup"><span data-stu-id="29a78-169">If you don’t include a `MSCRM.MergeLabels` header, the default behavior is as if the value were `false` and any localized labels not included in your update will be lost.</span></span>  
  
 <span data-ttu-id="29a78-170">When you update an entity or attribute, you must use the <xref href="Microsoft.Dynamics.CRM.PublishXml?text=PublishXml Action" /> or <xref href="Microsoft.Dynamics.CRM.PublishAllXml?text=PublishAllXml Action" /> before the changes you make will be applied to the application.</span><span class="sxs-lookup"><span data-stu-id="29a78-170">When you update an entity or attribute, you must use the <xref href="Microsoft.Dynamics.CRM.PublishXml?text=PublishXml Action" /> or <xref href="Microsoft.Dynamics.CRM.PublishAllXml?text=PublishAllXml Action" /> before the changes you make will be applied to the application.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="29a78-171">[Publish Customizations](../customize-dev/publish-customizations.md)</span><span class="sxs-lookup"><span data-stu-id="29a78-171">[Publish Customizations](../customize-dev/publish-customizations.md)</span></span>  
  
 <span data-ttu-id="29a78-172">Typically, you will retrieve the JSON definition of the attribute and modify the properties before you send it back.</span><span class="sxs-lookup"><span data-stu-id="29a78-172">Typically, you will retrieve the JSON definition of the attribute and modify the properties before you send it back.</span></span> <span data-ttu-id="29a78-173">The following example contains all the metadata properties of the entity created in the [Create entities](create-update-entity-definitions-using-web-api.md#bkmk_createEntities) example, but with the DisplayName changed to “Bank Business Name.”</span><span class="sxs-lookup"><span data-stu-id="29a78-173">The following example contains all the metadata properties of the entity created in the [Create entities](create-update-entity-definitions-using-web-api.md#bkmk_createEntities) example, but with the DisplayName changed to “Bank Business Name.”</span></span> <span data-ttu-id="29a78-174">It may be useful to note that the JSON here provides the default values for properties not set in the [Create entities](create-update-entity-definitions-using-web-api.md#bkmk_createEntities) example.</span><span class="sxs-lookup"><span data-stu-id="29a78-174">It may be useful to note that the JSON here provides the default values for properties not set in the [Create entities](create-update-entity-definitions-using-web-api.md#bkmk_createEntities) example.</span></span>  
  
 <span data-ttu-id="29a78-175">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="29a78-175">**Request**</span></span>  
```http 
PUT [Organization URI]/api/data/v9.0/EntityDefinitions(417129e1-207c-e511-80d2-00155d2a68d2) HTTP/1.1  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
MSCRM.MergeLabels: true  
  
{  
 "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#EntityDefinitions/$entity",  
 "ActivityTypeMask": 0,  
 "AutoRouteToOwnerQueue": false,  
 "CanTriggerWorkflow": true,  
 "Description": {  
  "LocalizedLabels": [  
   {  
    "Label": "An entity to store information about customer bank accounts",  
    "LanguageCode": 1033,  
    "IsManaged": false,  
    "MetadataId": "edc3abd7-c5ae-4822-a3ed-51734fdd0469",  
    "HasChanged": null  
   }  
  ]  
 },  
 "DisplayCollectionName": {  
  "LocalizedLabels": [  
   {  
    "Label": "Bank Accounts",  
    "LanguageCode": 1033,  
    "IsManaged": false,  
    "MetadataId": "7c758e0c-e9cf-4947-93b0-50ec30b20f60",  
    "HasChanged": null  
   }  
  ]  
 },  
 "DisplayName": {  
  "@odata.type": "Microsoft.Dynamics.CRM.Label",  
  "LocalizedLabels": [  
   {  
    "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
    "Label": "Bank Business Name",  
    "LanguageCode": 1033  
   }  
  ]  
 },  
 "EntityHelpUrlEnabled": false,  
 "EntityHelpUrl": null,  
 "IsDocumentManagementEnabled": false,  
 "IsOneNoteIntegrationEnabled": false,  
 "IsInteractionCentricEnabled": false,  
 "IsKnowledgeManagementEnabled": false,  
 "AutoCreateAccessTeams": false,  
 "IsActivity": false,  
 "IsActivityParty": false,  
 "IsAuditEnabled": {  
  "Value": false,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canmodifyauditsettings"  
 },  
 "IsAvailableOffline": false,  
 "IsChildEntity": false,  
 "IsAIRUpdated": false,  
 "IsValidForQueue": {  
  "Value": false,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canmodifyqueuesettings"  
 },  
 "IsConnectionsEnabled": {  
  "Value": false,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canmodifyconnectionsettings"  
 },  
 "IconLargeName": null,  
 "IconMediumName": null,  
 "IconSmallName": null,  
 "IsCustomEntity": true,  
 "IsBusinessProcessEnabled": false,  
 "IsCustomizable": {  
  "Value": true,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "iscustomizable"  
 },  
 "IsRenameable": {  
  "Value": true,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "isrenameable"  
 },  
 "IsMappable": {  
  "Value": true,  
  "CanBeChanged": false,  
  "ManagedPropertyLogicalName": "ismappable"  
 },  
 "IsDuplicateDetectionEnabled": {  
  "Value": false,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canmodifyduplicatedetectionsettings"  
 },  
 "CanCreateAttributes": {  
  "Value": true,  
  "CanBeChanged": false,  
  "ManagedPropertyLogicalName": "cancreateattributes"  
 },  
 "CanCreateForms": {  
  "Value": true,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "cancreateforms"  
 },  
 "CanCreateViews": {  
  "Value": true,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "cancreateviews"  
 },  
 "CanCreateCharts": {  
  "Value": true,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "cancreatecharts"  
 },  
 "CanBeRelatedEntityInRelationship": {  
  "Value": true,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canberelatedentityinrelationship"  
 },  
 "CanBePrimaryEntityInRelationship": {  
  "Value": true,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canbeprimaryentityinrelationship"  
 },  
 "CanBeInManyToMany": {  
  "Value": true,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canbeinmanytomany"  
 },  
 "CanEnableSyncToExternalSearchIndex": {  
  "Value": true,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canenablesynctoexternalsearchindex"  
 },  
 "SyncToExternalSearchIndex": false,  
 "CanModifyAdditionalSettings": {  
  "Value": true,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canmodifyadditionalsettings"  
 },  
 "CanChangeHierarchicalRelationship": {  
  "Value": true,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canchangehierarchicalrelationship"  
 },  
 "IsOptimisticConcurrencyEnabled": true,  
 "ChangeTrackingEnabled": false,  
 "IsImportable": true,  
 "IsIntersect": false,  
 "IsMailMergeEnabled": {  
  "Value": true,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canmodifymailmergesettings"  
 },  
 "IsManaged": false,  
 "IsEnabledForCharts": true,  
 "IsEnabledForTrace": false,  
 "IsValidForAdvancedFind": true,  
 "IsVisibleInMobile": {  
  "Value": false,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canmodifymobilevisibility"  
 },  
 "IsVisibleInMobileClient": {  
  "Value": false,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canmodifymobileclientvisibility"  
 },  
 "IsReadOnlyInMobileClient": {  
  "Value": false,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canmodifymobileclientreadonly"  
 },  
 "IsOfflineInMobileClient": {  
  "Value": false,  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canmodifymobileclientoffline"  
 },  
 "DaysSinceRecordLastModified": 0,  
 "IsReadingPaneEnabled": true,  
 "IsQuickCreateEnabled": false,  
 "LogicalName": "new_bankaccount",  
 "ObjectTypeCode": 10009,  
 "OwnershipType": "UserOwned",  
 "PrimaryNameAttribute": "new_accountname",  
 "PrimaryImageAttribute": null,  
 "PrimaryIdAttribute": "new_bankaccountid",  
 "Privileges": [  
  {  
   "CanBeBasic": true,  
   "CanBeDeep": true,  
   "CanBeGlobal": true,  
   "CanBeLocal": true,  
   "CanBeEntityReference": false,  
   "CanBeParentEntityReference": false,  
   "Name": "prvCreatenew_BankAccount",  
   "PrivilegeId": "d1a8de4b-27df-42e1-bc5c-b863e002b37f",  
   "PrivilegeType": "Create"  
  },  
  {  
   "CanBeBasic": true,  
   "CanBeDeep": true,  
   "CanBeGlobal": true,  
   "CanBeLocal": true,  
   "CanBeEntityReference": false,  
   "CanBeParentEntityReference": false,  
   "Name": "prvReadnew_BankAccount",  
   "PrivilegeId": "726043b1-de2c-487e-9d6d-5629fca2bf22",  
   "PrivilegeType": "Read"  
  },  
  {  
   "CanBeBasic": true,  
   "CanBeDeep": true,  
   "CanBeGlobal": true,  
   "CanBeLocal": true,  
   "CanBeEntityReference": false,  
   "CanBeParentEntityReference": false,  
   "Name": "prvWritenew_BankAccount",  
   "PrivilegeId": "fa50c539-b6c7-4eaf-bd49-fd8224bc51b6",  
   "PrivilegeType": "Write"  
  },  
  {  
   "CanBeBasic": true,  
   "CanBeDeep": true,  
   "CanBeGlobal": true,  
   "CanBeLocal": true,  
   "CanBeEntityReference": false,  
   "CanBeParentEntityReference": false,  
   "Name": "prvDeletenew_BankAccount",  
   "PrivilegeId": "17c1fd6e-f856-45e7-b563-796f53108b85",  
   "PrivilegeType": "Delete"  
  },  
  {  
   "CanBeBasic": true,  
   "CanBeDeep": true,  
   "CanBeGlobal": true,  
   "CanBeLocal": true,  
   "CanBeEntityReference": false,  
   "CanBeParentEntityReference": false,  
   "Name": "prvAssignnew_BankAccount",  
   "PrivilegeId": "133ca81d-668e-4c19-a71e-10c6dfe099cd",  
   "PrivilegeType": "Assign"  
  },  
  {  
   "CanBeBasic": true,  
   "CanBeDeep": true,  
   "CanBeGlobal": true,  
   "CanBeLocal": true,  
   "CanBeEntityReference": false,  
   "CanBeParentEntityReference": false,  
   "Name": "prvSharenew_BankAccount",  
   "PrivilegeId": "15f27df4-9c67-47c9-b1f1-274e1c44f24a",  
   "PrivilegeType": "Share"  
  },  
  {  
   "CanBeBasic": true,  
   "CanBeDeep": true,  
   "CanBeGlobal": true,  
   "CanBeLocal": true,  
   "CanBeEntityReference": false,  
   "CanBeParentEntityReference": false,  
   "Name": "prvAppendnew_BankAccount",  
   "PrivilegeId": "ac8b1920-8f93-4e9d-94e3-c680e2a2f228",  
   "PrivilegeType": "Append"  
  },  
  {  
   "CanBeBasic": true,  
   "CanBeDeep": true,  
   "CanBeGlobal": true,  
   "CanBeLocal": true,  
   "CanBeEntityReference": false,  
   "CanBeParentEntityReference": false,  
   "Name": "prvAppendTonew_BankAccount",  
   "PrivilegeId": "f63a5f46-3bc7-4eac-81d0-7f77f566ef46",  
   "PrivilegeType": "AppendTo"  
  }  
 ],  
 "RecurrenceBaseEntityLogicalName": null,  
 "ReportViewName": "Filterednew_BankAccount",  
 "SchemaName": "new_BankAccount",  
 "IntroducedVersion": "1.0",  
 "IsStateModelAware": true,  
 "EnforceStateTransitions": false,  
 "EntityColor": null,  
 "LogicalCollectionName": "new_bankaccounts",  
 "CollectionSchemaName": "new_BankAccounts",  
 "EntitySetName": "new_bankaccounts",  
 "IsEnabledForExternalChannels": false,  
 "IsPrivate": false,  
 "MetadataId": "417129e1-207c-e511-80d2-00155d2a68d2",  
 "HasChanged": null  
}  
```  
  
 <span data-ttu-id="29a78-176">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="29a78-176">**Response**</span></span>  
```http 
HTTP/1.1 204 No Content  
OData-Version: 4.0  
```  
  
<a name="bkmk_CreateAttributes"></a>

## <a name="create-attributes"></a><span data-ttu-id="29a78-177">Create attributes</span><span class="sxs-lookup"><span data-stu-id="29a78-177">Create attributes</span></span>

 <span data-ttu-id="29a78-178">You can create attributes at the same time you create the entity by including the JSON definition of the attributes in the `Attributes` array for the entity you post in addition to the string attribute that serves as the primary name attribute.</span><span class="sxs-lookup"><span data-stu-id="29a78-178">You can create attributes at the same time you create the entity by including the JSON definition of the attributes in the `Attributes` array for the entity you post in addition to the string attribute that serves as the primary name attribute.</span></span> <span data-ttu-id="29a78-179">If you want to add attributes to an entity that is already created, you can send a POST request including the JSON definition of them to the entity `Attributes` collection-valued navigation property.</span><span class="sxs-lookup"><span data-stu-id="29a78-179">If you want to add attributes to an entity that is already created, you can send a POST request including the JSON definition of them to the entity `Attributes` collection-valued navigation property.</span></span>  
  
<a name="bkmk_CreateString"></a>

### <a name="create-a-string-attribute"></a><span data-ttu-id="29a78-180">Create a string attribute</span><span class="sxs-lookup"><span data-stu-id="29a78-180">Create a string attribute</span></span>

 <span data-ttu-id="29a78-181">The following example will use these properties to create a string attribute.</span><span class="sxs-lookup"><span data-stu-id="29a78-181">The following example will use these properties to create a string attribute.</span></span>  
  
|<span data-ttu-id="29a78-182">String attribute properties</span><span class="sxs-lookup"><span data-stu-id="29a78-182">String attribute properties</span></span>|<span data-ttu-id="29a78-183">Giá trị</span><span class="sxs-lookup"><span data-stu-id="29a78-183">Values</span></span>|  
|---------------------------------|------------|  
|<span data-ttu-id="29a78-184">SchemaName</span><span class="sxs-lookup"><span data-stu-id="29a78-184">SchemaName</span></span>|<span data-ttu-id="29a78-185">new_BankName</span><span class="sxs-lookup"><span data-stu-id="29a78-185">new_BankName</span></span>|  
|<span data-ttu-id="29a78-186">DisplayName</span><span class="sxs-lookup"><span data-stu-id="29a78-186">DisplayName</span></span>|<span data-ttu-id="29a78-187">Bank Name</span><span class="sxs-lookup"><span data-stu-id="29a78-187">Bank Name</span></span>|  
|<span data-ttu-id="29a78-188">Mô tả</span><span class="sxs-lookup"><span data-stu-id="29a78-188">Description</span></span>|<span data-ttu-id="29a78-189">Type the name of the bank.</span><span class="sxs-lookup"><span data-stu-id="29a78-189">Type the name of the bank.</span></span>|  
|<span data-ttu-id="29a78-190">RequiredLevel</span><span class="sxs-lookup"><span data-stu-id="29a78-190">RequiredLevel</span></span>|<span data-ttu-id="29a78-191">Không có</span><span class="sxs-lookup"><span data-stu-id="29a78-191">None</span></span>|  
|<span data-ttu-id="29a78-192">MaxLength</span><span class="sxs-lookup"><span data-stu-id="29a78-192">MaxLength</span></span>|<span data-ttu-id="29a78-193">100</span><span class="sxs-lookup"><span data-stu-id="29a78-193">100</span></span>|  
|<span data-ttu-id="29a78-194">FormatName</span><span class="sxs-lookup"><span data-stu-id="29a78-194">FormatName</span></span>|<span data-ttu-id="29a78-195">Text</span><span class="sxs-lookup"><span data-stu-id="29a78-195">Text</span></span>|  
  
 <span data-ttu-id="29a78-196">The following example creates a string attribute using the properties and adds it to the entity with the MetadataId value of 402fa40f-287c-e511-80d2-00155d2a68d2.</span><span class="sxs-lookup"><span data-stu-id="29a78-196">The following example creates a string attribute using the properties and adds it to the entity with the MetadataId value of 402fa40f-287c-e511-80d2-00155d2a68d2.</span></span> <span data-ttu-id="29a78-197">The URI for the attribute is returned in the response.</span><span class="sxs-lookup"><span data-stu-id="29a78-197">The URI for the attribute is returned in the response.</span></span>  
  
 <span data-ttu-id="29a78-198">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="29a78-198">**Request**</span></span>

```http 
POST [Organization URI]/api/data/v9.0/EntityDefinitions(402fa40f-287c-e511-80d2-00155d2a68d2)/Attributes HTTP/1.1  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
  
{  
 "AttributeType": "String",  
 "AttributeTypeName": {  
  "Value": "StringType"  
 },  
 "Description": {  
  "@odata.type": "Microsoft.Dynamics.CRM.Label",  
  "LocalizedLabels": [  
   {  
    "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
    "Label": "Type the name of the bank",  
    "LanguageCode": 1033  
   }  
  ]  
 },  
 "DisplayName": {  
  "@odata.type": "Microsoft.Dynamics.CRM.Label",  
  "LocalizedLabels": [  
   {  
    "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
    "Label": "Bank Name",  
    "LanguageCode": 1033  
   }  
  ]  
 },  
 "RequiredLevel": {  
  "Value": "None",  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canmodifyrequirementlevelsettings"  
 },  
 "SchemaName": "new_BankName",  
 "@odata.type": "Microsoft.Dynamics.CRM.StringAttributeMetadata",  
 "FormatName": {  
  "Value": "Text"  
 },  
 "MaxLength": 100  
}  
  
```  
  
 <span data-ttu-id="29a78-199">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="29a78-199">**Response**</span></span>  
```http 
HTTP/1.1 204 No Content  
OData-Version: 4.0  
OData-EntityId: [Organization URI]/api/data/v9.0/EntityDefinitions(402fa40f-287c-e511-80d2-00155d2a68d2)/Attributes(f01bef16-287c-e511-80d2-00155d2a68d2)  
```  
  
<a name="bkmk_createMoney"></a>

### <a name="create-a-money-attribute"></a><span data-ttu-id="29a78-200">Create a Money attribute</span><span class="sxs-lookup"><span data-stu-id="29a78-200">Create a Money attribute</span></span>

 <span data-ttu-id="29a78-201">The following example will use these properties to create a money attribute.</span><span class="sxs-lookup"><span data-stu-id="29a78-201">The following example will use these properties to create a money attribute.</span></span>  
  
|<span data-ttu-id="29a78-202">Money attribute properties</span><span class="sxs-lookup"><span data-stu-id="29a78-202">Money attribute properties</span></span>|<span data-ttu-id="29a78-203">Giá trị</span><span class="sxs-lookup"><span data-stu-id="29a78-203">Values</span></span>|  
|--------------------------------|------------|  
|<span data-ttu-id="29a78-204">SchemaName</span><span class="sxs-lookup"><span data-stu-id="29a78-204">SchemaName</span></span>|<span data-ttu-id="29a78-205">new_Balance</span><span class="sxs-lookup"><span data-stu-id="29a78-205">new_Balance</span></span>|  
|<span data-ttu-id="29a78-206">DisplayName</span><span class="sxs-lookup"><span data-stu-id="29a78-206">DisplayName</span></span>|<span data-ttu-id="29a78-207">Balance</span><span class="sxs-lookup"><span data-stu-id="29a78-207">Balance</span></span>|  
|<span data-ttu-id="29a78-208">Mô tả</span><span class="sxs-lookup"><span data-stu-id="29a78-208">Description</span></span>|<span data-ttu-id="29a78-209">Enter the balance amount.</span><span class="sxs-lookup"><span data-stu-id="29a78-209">Enter the balance amount.</span></span>|  
|<span data-ttu-id="29a78-210">RequiredLevel</span><span class="sxs-lookup"><span data-stu-id="29a78-210">RequiredLevel</span></span>|<span data-ttu-id="29a78-211">Không có</span><span class="sxs-lookup"><span data-stu-id="29a78-211">None</span></span>|  
|<span data-ttu-id="29a78-212">PrecisionSource</span><span class="sxs-lookup"><span data-stu-id="29a78-212">PrecisionSource</span></span>|<span data-ttu-id="29a78-213">2 **Note:**  For information on the valid values for PrecisionSource, see [Quantity data attributes](../introduction-entity-attributes.md#quantity-data-attributes).</span><span class="sxs-lookup"><span data-stu-id="29a78-213">2 **Note:**  For information on the valid values for PrecisionSource, see [Quantity data attributes](../introduction-entity-attributes.md#quantity-data-attributes).</span></span> <span data-ttu-id="29a78-214">The value 2 means that the level of decimal precision will match TransactionCurrency.CurrencyPrecision that is associated with the current record.</span><span class="sxs-lookup"><span data-stu-id="29a78-214">The value 2 means that the level of decimal precision will match TransactionCurrency.CurrencyPrecision that is associated with the current record.</span></span>|  
  
 <span data-ttu-id="29a78-215">The following example creates a money attribute using the properties and adds it to the entity with the MetadataId value of 402fa40f-287c-e511-80d2-00155d2a68d2.</span><span class="sxs-lookup"><span data-stu-id="29a78-215">The following example creates a money attribute using the properties and adds it to the entity with the MetadataId value of 402fa40f-287c-e511-80d2-00155d2a68d2.</span></span> <span data-ttu-id="29a78-216">The URI for the attribute is returned in the response.</span><span class="sxs-lookup"><span data-stu-id="29a78-216">The URI for the attribute is returned in the response.</span></span>  
  
 <span data-ttu-id="29a78-217">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="29a78-217">**Request**</span></span>  
```http   
POST [Organization URI]/api/data/v9.0/EntityDefinitions(402fa40f-287c-e511-80d2-00155d2a68d2)/Attributes HTTP/1.1  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
  
{  
 "AttributeType": "Money",  
 "AttributeTypeName": {  
  "Value": "MoneyType"  
 },  
 "Description": {  
  "@odata.type": "Microsoft.Dynamics.CRM.Label",  
  "LocalizedLabels": [  
   {  
    "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
    "Label": "Enter the balance amount",  
    "LanguageCode": 1033  
   }  
  ]  
 },  
 "DisplayName": {  
  "@odata.type": "Microsoft.Dynamics.CRM.Label",  
  "LocalizedLabels": [  
   {  
    "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
    "Label": "Balance",  
    "LanguageCode": 1033  
   }  
  ]  
 },  
 "RequiredLevel": {  
  "Value": "None",  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canmodifyrequirementlevelsettings"  
 },  
 "SchemaName": "new_Balance",  
 "@odata.type": "Microsoft.Dynamics.CRM.MoneyAttributeMetadata",  
 "PrecisionSource": 2  
}  
```  
  
 <span data-ttu-id="29a78-218">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="29a78-218">**Response**</span></span>  
```http 
HTTP/1.1 204 No Content  
OData-Version: 4.0  
OData-EntityId: [Organization URI]/api/data/v9.0/EntityDefinitions(402fa40f-287c-e511-80d2-00155d2a68d2)/Attributes(f11bef16-287c-e511-80d2-00155d2a68d2)  
```  
  
<a name="bkmk_createDateTime"></a>

### <a name="create-a-datetime-attribute"></a><span data-ttu-id="29a78-219">Create a datetime attribute</span><span class="sxs-lookup"><span data-stu-id="29a78-219">Create a datetime attribute</span></span>

 <span data-ttu-id="29a78-220">The following example will use these properties to create a datetime attribute.</span><span class="sxs-lookup"><span data-stu-id="29a78-220">The following example will use these properties to create a datetime attribute.</span></span>  
  
|<span data-ttu-id="29a78-221">Datetime attribute properties</span><span class="sxs-lookup"><span data-stu-id="29a78-221">Datetime attribute properties</span></span>|<span data-ttu-id="29a78-222">Giá trị</span><span class="sxs-lookup"><span data-stu-id="29a78-222">Values</span></span>|  
|-----------------------------------|------------|  
|<span data-ttu-id="29a78-223">SchemaName</span><span class="sxs-lookup"><span data-stu-id="29a78-223">SchemaName</span></span>|<span data-ttu-id="29a78-224">new_Checkeddate</span><span class="sxs-lookup"><span data-stu-id="29a78-224">new_Checkeddate</span></span>|  
|<span data-ttu-id="29a78-225">DisplayName</span><span class="sxs-lookup"><span data-stu-id="29a78-225">DisplayName</span></span>|<span data-ttu-id="29a78-226">Date</span><span class="sxs-lookup"><span data-stu-id="29a78-226">Date</span></span>|  
|<span data-ttu-id="29a78-227">Mô tả</span><span class="sxs-lookup"><span data-stu-id="29a78-227">Description</span></span>|<span data-ttu-id="29a78-228">The date the account balance was last confirmed.</span><span class="sxs-lookup"><span data-stu-id="29a78-228">The date the account balance was last confirmed.</span></span>|  
|<span data-ttu-id="29a78-229">RequiredLevel</span><span class="sxs-lookup"><span data-stu-id="29a78-229">RequiredLevel</span></span>|<span data-ttu-id="29a78-230">Không có</span><span class="sxs-lookup"><span data-stu-id="29a78-230">None</span></span>|  
|<span data-ttu-id="29a78-231">Định dạng</span><span class="sxs-lookup"><span data-stu-id="29a78-231">Format</span></span>|<span data-ttu-id="29a78-232">DateOnly **Note:**  For the valid options for this property, see <xref href="Microsoft.Dynamics.CRM.DateTimeFormat?text=DateTimeFormat EnumType" />.</span><span class="sxs-lookup"><span data-stu-id="29a78-232">DateOnly **Note:**  For the valid options for this property, see <xref href="Microsoft.Dynamics.CRM.DateTimeFormat?text=DateTimeFormat EnumType" />.</span></span>|  
  
 <span data-ttu-id="29a78-233">The following example creates a datetime attribute using the properties and adds it to the entity with the MetadataId value of 402fa40f-287c-e511-80d2-00155d2a68d2.</span><span class="sxs-lookup"><span data-stu-id="29a78-233">The following example creates a datetime attribute using the properties and adds it to the entity with the MetadataId value of 402fa40f-287c-e511-80d2-00155d2a68d2.</span></span> <span data-ttu-id="29a78-234">The URI for the attribute is returned in the response.</span><span class="sxs-lookup"><span data-stu-id="29a78-234">The URI for the attribute is returned in the response.</span></span>  
  
 <span data-ttu-id="29a78-235">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="29a78-235">**Request**</span></span>

```http 
POST [Organization URI]/api/data/v9.0/EntityDefinitions(402fa40f-287c-e511-80d2-00155d2a68d2)/Attributes HTTP/1.1  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
  
{  
 "AttributeType": "DateTime",  
 "AttributeTypeName": {  
  "Value": "DateTimeType"  
 },  
 "Description": {  
  "@odata.type": "Microsoft.Dynamics.CRM.Label",  
  "LocalizedLabels": [  
   {  
    "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
    "Label": "The date the account balance was last confirmed",  
    "LanguageCode": 1033  
   }  
  ]  
 },  
 "DisplayName": {  
  "@odata.type": "Microsoft.Dynamics.CRM.Label",  
  "LocalizedLabels": [  
   {  
    "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
    "Label": "Date",  
    "LanguageCode": 1033  
   }  
  ]  
 },  
 "RequiredLevel": {  
  "Value": "None",  
  "CanBeChanged": true,  
  "ManagedPropertyLogicalName": "canmodifyrequirementlevelsettings"  
 },  
 "SchemaName": "new_Checkeddate",  
 "@odata.type": "Microsoft.Dynamics.CRM.DateTimeAttributeMetadata",  
 "Format": "DateOnly"  
}  
```  
  
 <span data-ttu-id="29a78-236">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="29a78-236">**Response**</span></span>  
```http 
HTTP/1.1 204 No Content  
OData-Version: 4.0  
OData-EntityId: [Organization URI]/api/data/v9.0/EntityDefinitions(402fa40f-287c-e511-80d2-00155d2a68d2)/Attributes(fe1bef16-287c-e511-80d2-00155d2a68d2)  
```  
  
<a name="bkmk_CreateCustomerLookup"></a>

### <a name="create-a-customer-lookup-attribute"></a><span data-ttu-id="29a78-237">Create a customer lookup attribute</span><span class="sxs-lookup"><span data-stu-id="29a78-237">Create a customer lookup attribute</span></span>

 <span data-ttu-id="29a78-238">Unlike  other attributes, a customer lookup attribute is created using the <xref href="Microsoft.Dynamics.CRM.CreateCustomerRelationships?text=CreateCustomerRelationships Action" />.</span><span class="sxs-lookup"><span data-stu-id="29a78-238">Unlike  other attributes, a customer lookup attribute is created using the <xref href="Microsoft.Dynamics.CRM.CreateCustomerRelationships?text=CreateCustomerRelationships Action" />.</span></span> <span data-ttu-id="29a78-239">The parameters for this action require the definition of the lookup attribute and a pair of one-to-many relationships.</span><span class="sxs-lookup"><span data-stu-id="29a78-239">The parameters for this action require the definition of the lookup attribute and a pair of one-to-many relationships.</span></span>  
 <span data-ttu-id="29a78-240">A customer lookup attribute has two one-to-many relationships: one to the account entity and the other one to contact entity.</span><span class="sxs-lookup"><span data-stu-id="29a78-240">A customer lookup attribute has two one-to-many relationships: one to the account entity and the other one to contact entity.</span></span>  
  
 <span data-ttu-id="29a78-241">The following example will use these properties to create a customer lookup attribute.</span><span class="sxs-lookup"><span data-stu-id="29a78-241">The following example will use these properties to create a customer lookup attribute.</span></span>  
  
|<span data-ttu-id="29a78-242">Customer lookup attribute properties</span><span class="sxs-lookup"><span data-stu-id="29a78-242">Customer lookup attribute properties</span></span>|<span data-ttu-id="29a78-243">Giá trị</span><span class="sxs-lookup"><span data-stu-id="29a78-243">Values</span></span>|  
|------------------------------------------|------------|  
|<span data-ttu-id="29a78-244">SchemaName</span><span class="sxs-lookup"><span data-stu-id="29a78-244">SchemaName</span></span>|<span data-ttu-id="29a78-245">new_CustomerId</span><span class="sxs-lookup"><span data-stu-id="29a78-245">new_CustomerId</span></span>|  
|<span data-ttu-id="29a78-246">DisplayName</span><span class="sxs-lookup"><span data-stu-id="29a78-246">DisplayName</span></span>|<span data-ttu-id="29a78-247">Khách hàng</span><span class="sxs-lookup"><span data-stu-id="29a78-247">Customer</span></span>|  
|<span data-ttu-id="29a78-248">Mô tả</span><span class="sxs-lookup"><span data-stu-id="29a78-248">Description</span></span>|<span data-ttu-id="29a78-249">Sample Customer Lookup Attribute</span><span class="sxs-lookup"><span data-stu-id="29a78-249">Sample Customer Lookup Attribute</span></span>|  
  
 <span data-ttu-id="29a78-250">The example creates a customer lookup attribute, `new_CustomerId`, and adds it to the custom entity:  `new_bankaccount`.</span><span class="sxs-lookup"><span data-stu-id="29a78-250">The example creates a customer lookup attribute, `new_CustomerId`, and adds it to the custom entity:  `new_bankaccount`.</span></span> <span data-ttu-id="29a78-251">The response is a <xref href="Microsoft.Dynamics.CRM.CreateCustomerRelationshipsResponse?text=CreateCustomerRelationshipsResponse ComplexType" />.</span><span class="sxs-lookup"><span data-stu-id="29a78-251">The response is a <xref href="Microsoft.Dynamics.CRM.CreateCustomerRelationshipsResponse?text=CreateCustomerRelationshipsResponse ComplexType" />.</span></span>  
  
 <span data-ttu-id="29a78-252">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="29a78-252">**Request**</span></span>

```http 
POST [Organization URI]/api/data/v9.0/CreateCustomerRelationships HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Accept: application/json  
Content-Type: application/json; charset=utf-8  
  
{  
    "OneToManyRelationships": [{  
        "SchemaName": "new_bankaccount_customer_account",  
        "ReferencedEntity": "account",  
        "ReferencingEntity": "new_bankaccount"  
    }, {  
        "SchemaName": "new_bankaccount_customer_contact",  
        "ReferencedEntity": "contact",  
        "ReferencingEntity": "new_bankaccount"  
    }],  
    "Lookup": {  
        "AttributeType": "Lookup",  
        "AttributeTypeName": {  
            "Value": "LookupType"  
        },  
        "Description": {  
            "@odata.type": "Microsoft.Dynamics.CRM.Label",  
            "LocalizedLabels": [{  
                "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
                "Label": "Sample Customer Lookup Attribute",  
                "LanguageCode": 1033  
            }],  
            "UserLocalizedLabel": {  
                "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
                "Label": "Sample Customer Lookup Attribute",  
                "LanguageCode": 1033  
            }  
        },  
        "DisplayName": {  
            "@odata.type": "Microsoft.Dynamics.CRM.Label",  
            "LocalizedLabels": [{  
                "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
                "Label": "Customer",  
                "LanguageCode": 1033  
            }],  
            "UserLocalizedLabel": {  
                "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",  
                "Label": "Customer",  
                "LanguageCode": 1033  
            }  
        },  
        "SchemaName": "new_CustomerId",  
        "@odata.type": "Microsoft.Dynamics.CRM.ComplexLookupAttributeMetadata"  
    }  
}  
```  
  
 <span data-ttu-id="29a78-253">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="29a78-253">**Response**</span></span>  
```http 
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
  
{  
    "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#Microsoft.Dynamics.CRM.CreateCustomerRelationshipsResponse",  
    "RelationshipIds": [  
        "a7d261bc-3580-e611-80d7-00155d2a68de", "aed261bc-3580-e611-80d7-00155d2a68de"  
    ],  
    "AttributeId": "39a5d94c-e8a2-4a41-acc0-8487242d455e"  
}  
  
```  
  
<a name="bkmk_updateAttribute"></a>
 
## <a name="update-an-attribute"></a><span data-ttu-id="29a78-254">Update an attribute</span><span class="sxs-lookup"><span data-stu-id="29a78-254">Update an attribute</span></span>

 <span data-ttu-id="29a78-255">As mentioned in [Update entities](create-update-entity-definitions-using-web-api.md#bkmk_updateEntities), model entities are updated using the HTTP PUT method with the entire JSON definition of the current item.</span><span class="sxs-lookup"><span data-stu-id="29a78-255">As mentioned in [Update entities](create-update-entity-definitions-using-web-api.md#bkmk_updateEntities), model entities are updated using the HTTP PUT method with the entire JSON definition of the current item.</span></span> <span data-ttu-id="29a78-256">This applies to attributes as well as entities.</span><span class="sxs-lookup"><span data-stu-id="29a78-256">This applies to attributes as well as entities.</span></span> <span data-ttu-id="29a78-257">Just like with entities, you have the option to overwrite labels using the `MSCRM.MergeLabels` header with the value set to `false`, and you must publish customizations before they are active in the system.</span><span class="sxs-lookup"><span data-stu-id="29a78-257">Just like with entities, you have the option to overwrite labels using the `MSCRM.MergeLabels` header with the value set to `false`, and you must publish customizations before they are active in the system.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="29a78-258">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="29a78-258">See also</span></span>

 <span data-ttu-id="29a78-259">[Use the Web API with Dynamics 365 for Customer Engagement apps metadata](use-web-api-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="29a78-259">[Use the Web API with Dynamics 365 for Customer Engagement apps metadata](use-web-api-metadata.md) </span></span>  
 <span data-ttu-id="29a78-260">[Query Metadata using the Web API](query-metadata-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="29a78-260">[Query Metadata using the Web API](query-metadata-web-api.md) </span></span>  
 <span data-ttu-id="29a78-261">[Retrieve metadata by name or MetadataId](retrieve-metadata-name-metadataid.md) </span><span class="sxs-lookup"><span data-stu-id="29a78-261">[Retrieve metadata by name or MetadataId](retrieve-metadata-name-metadataid.md) </span></span>  
 <span data-ttu-id="29a78-262">[Model entity relationships using the Web API](create-update-entity-relationships-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="29a78-262">[Model entity relationships using the Web API](create-update-entity-relationships-using-web-api.md) </span></span>  
 <span data-ttu-id="29a78-263">[Use the Organization service with Dynamics 365 for Customer Engagement apps metadata](../org-service/use-organization-service-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="29a78-263">[Use the Organization service with Dynamics 365 for Customer Engagement apps metadata](../org-service/use-organization-service-metadata.md) </span></span>  
 [<span data-ttu-id="29a78-264">Customize Entity Attribute Metadata</span><span class="sxs-lookup"><span data-stu-id="29a78-264">Customize Entity Attribute Metadata</span></span>](../customize-entity-attribute-metadata.md)
