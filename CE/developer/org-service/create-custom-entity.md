---
title: Create a custom entity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn how to create a custom user-owned entity.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: f53639b1-7d62-4470-8ca6-c9a6500c9230
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 34f18ad1250e0ea0db8e3c7337aa789507db4cb0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386133"
---
# <a name="create-a-custom-entity"></a><span data-ttu-id="669d3-103">Create a custom entity</span><span class="sxs-lookup"><span data-stu-id="669d3-103">Create a custom entity</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="669d3-104">This topic shows how to create a custom user-owned entity called **Bank Account** and add four different types of attributes to it.</span><span class="sxs-lookup"><span data-stu-id="669d3-104">This topic shows how to create a custom user-owned entity called **Bank Account** and add four different types of attributes to it.</span></span>  
  
 <span data-ttu-id="669d3-105">You can also create organization-owned custom entities.</span><span class="sxs-lookup"><span data-stu-id="669d3-105">You can also create organization-owned custom entities.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="669d3-106">[Entity ownership](../introduction-entities.md#entity-ownership)</span><span class="sxs-lookup"><span data-stu-id="669d3-106">[Entity ownership](../introduction-entities.md#entity-ownership)</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="669d3-107">You won’t be able to see this entity in the application navigation unless the entity properties are edited to set the **Areas that display this entity** are set.</span><span class="sxs-lookup"><span data-stu-id="669d3-107">You won’t be able to see this entity in the application navigation unless the entity properties are edited to set the **Areas that display this entity** are set.</span></span>  
  
<a name="BKMK_CreateCustomEntity"></a>   
## <a name="create-a-custom-entity"></a><span data-ttu-id="669d3-108">Create a custom entity</span><span class="sxs-lookup"><span data-stu-id="669d3-108">Create a custom entity</span></span>  
 <span data-ttu-id="669d3-109">The following sample uses the <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest> to create the entity and the <xref:Microsoft.Xrm.Sdk.Metadata.StringAttributeMetadata><xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest.PrimaryAttribute>.</span><span class="sxs-lookup"><span data-stu-id="669d3-109">The following sample uses the <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest> to create the entity and the <xref:Microsoft.Xrm.Sdk.Metadata.StringAttributeMetadata><xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest.PrimaryAttribute>.</span></span>  
  
 <span data-ttu-id="669d3-110">The `_customEntityName` value is “new_bankaccount”.</span><span class="sxs-lookup"><span data-stu-id="669d3-110">The `_customEntityName` value is “new_bankaccount”.</span></span>  
  
 [!code-csharp[Entities#CreateUpdateEntityMetadata1](../../snippets/csharp/CRMV8/entities/cs/createupdateentitymetadata1.cs#createupdateentitymetadata1)]  
  
<a name="BKMK_AddStringAttribute"></a>   
## <a name="add-a-string-attribute-to-the-custom-entity"></a><span data-ttu-id="669d3-111">Add a String attribute to the custom entity</span><span class="sxs-lookup"><span data-stu-id="669d3-111">Add a String attribute to the custom entity</span></span>  
 <span data-ttu-id="669d3-112">The following sample adds a <xref:Microsoft.Xrm.Sdk.Metadata.StringAttributeMetadata> attribute to the `Bank Account` entity.</span><span class="sxs-lookup"><span data-stu-id="669d3-112">The following sample adds a <xref:Microsoft.Xrm.Sdk.Metadata.StringAttributeMetadata> attribute to the `Bank Account` entity.</span></span>  
  
 [!code-csharp[Entities#CreateUpdateEntityMetadata2](../../snippets/csharp/CRMV8/entities/cs/createupdateentitymetadata2.cs#createupdateentitymetadata2)]  
  
<a name="BKMK_AddMoneyAttribute"></a>   
## <a name="add-a-money-attribute-to-the-custom-entity"></a><span data-ttu-id="669d3-113">Add a Money attribute to the custom entity</span><span class="sxs-lookup"><span data-stu-id="669d3-113">Add a Money attribute to the custom entity</span></span>  
 <span data-ttu-id="669d3-114">The following sample adds a <xref:Microsoft.Xrm.Sdk.Metadata.MoneyAttributeMetadata> attribute to the `Bank Account` entity.</span><span class="sxs-lookup"><span data-stu-id="669d3-114">The following sample adds a <xref:Microsoft.Xrm.Sdk.Metadata.MoneyAttributeMetadata> attribute to the `Bank Account` entity.</span></span>  
  
 [!code-csharp[Entities#CreateUpdateEntityMetadata3](../../snippets/csharp/CRMV8/entities/cs/createupdateentitymetadata3.cs#createupdateentitymetadata3)]  
  
<a name="BKMK_AddDateTimeAttribute"></a>   
## <a name="add-a-datetime-attribute-to-the-custom-entity"></a><span data-ttu-id="669d3-115">Add a DateTime attribute to the custom entity</span><span class="sxs-lookup"><span data-stu-id="669d3-115">Add a DateTime attribute to the custom entity</span></span>  
 <span data-ttu-id="669d3-116">The following sample adds a <xref:Microsoft.Xrm.Sdk.Metadata.DateTimeAttributeMetadata> attribute to the `Bank Account` entity.</span><span class="sxs-lookup"><span data-stu-id="669d3-116">The following sample adds a <xref:Microsoft.Xrm.Sdk.Metadata.DateTimeAttributeMetadata> attribute to the `Bank Account` entity.</span></span>  
  
 [!code-csharp[Entities#CreateUpdateEntityMetadata4](../../snippets/csharp/CRMV8/entities/cs/createupdateentitymetadata4.cs#createupdateentitymetadata4)]  
  
<a name="BKMK_AddLookupAttribute"></a>   
## <a name="add-a-lookup-attribute-to-the-custom-entity"></a><span data-ttu-id="669d3-117">Add a Lookup attribute to the custom entity</span><span class="sxs-lookup"><span data-stu-id="669d3-117">Add a Lookup attribute to the custom entity</span></span>  
 <span data-ttu-id="669d3-118">The following sample uses <xref:Microsoft.Xrm.Sdk.Messages.CreateOneToManyRequest> to create a one-to-many relationship with the `Contact` entity so that a <xref:Microsoft.Xrm.Sdk.Metadata.LookupAttributeMetadata> attribute is added to the `Bank Account` entity.</span><span class="sxs-lookup"><span data-stu-id="669d3-118">The following sample uses <xref:Microsoft.Xrm.Sdk.Messages.CreateOneToManyRequest> to create a one-to-many relationship with the `Contact` entity so that a <xref:Microsoft.Xrm.Sdk.Metadata.LookupAttributeMetadata> attribute is added to the `Bank Account` entity.</span></span>  
  
 [!code-csharp[Entities#CreateUpdateEntityMetadata5](../../snippets/csharp/CRMV8/entities/cs/createupdateentitymetadata5.cs#createupdateentitymetadata5)]  
  
### <a name="see-also"></a><span data-ttu-id="669d3-119">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="669d3-119">See also</span></span>  
 <span data-ttu-id="669d3-120">[Use the IOrganizationService Sample and Helper Code](use-sample-helper-code.md) </span><span class="sxs-lookup"><span data-stu-id="669d3-120">[Use the IOrganizationService Sample and Helper Code](use-sample-helper-code.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest>   
 <span data-ttu-id="669d3-121">[Customize entity metadata](../customize-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="669d3-121">[Customize entity metadata](../customize-entity-metadata.md) </span></span>  
 <span data-ttu-id="669d3-122">[Which Entities are Customizable?](../which-entities-are-customizable.md) </span><span class="sxs-lookup"><span data-stu-id="669d3-122">[Which Entities are Customizable?](../which-entities-are-customizable.md) </span></span>  
 <span data-ttu-id="669d3-123">[Retrieve, update, and delete entities](retrieve-update-delete-entities.md) </span><span class="sxs-lookup"><span data-stu-id="669d3-123">[Retrieve, update, and delete entities](retrieve-update-delete-entities.md) </span></span>  
 <span data-ttu-id="669d3-124">[Create and update an entity than can be emailed](create-update-entity-emailed.md) </span><span class="sxs-lookup"><span data-stu-id="669d3-124">[Create and update an entity than can be emailed](create-update-entity-emailed.md) </span></span>  
 <span data-ttu-id="669d3-125">[Create a custom activity entity](create-custom-activity-entity.md) </span><span class="sxs-lookup"><span data-stu-id="669d3-125">[Create a custom activity entity](create-custom-activity-entity.md) </span></span>  
 <span data-ttu-id="669d3-126">[Change Entity Icons](../modify-icons-entity.md) </span><span class="sxs-lookup"><span data-stu-id="669d3-126">[Change Entity Icons](../modify-icons-entity.md) </span></span>  
 [<span data-ttu-id="669d3-127">Change Entity Messages</span><span class="sxs-lookup"><span data-stu-id="669d3-127">Change Entity Messages</span></span>](../modify-messages-entity.md)
