---
title: Describe a relationship between entities with connection roles (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
decription: Describing a relationship between entities using create connection roles and connection role categories.
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
- connecting roles to make a relationship
- assigning roles
- applying two matching roles to connect records, reciprocal roles
- specifying categories for connection roles
- creating connection roles, related messages and attributes
- describing the relationship between records by assigning roles
- describing a relationship between entities by using connection roles
ms.assetid: 19b6da03-5c17-4f6d-8521-32aa68d60f2e
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 1bfc11e0ac1b094ee2895ba87f5da1e0b62e9ae1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388391"
---
# <a name="describe-a-relationship-between-entities-with-connection-roles"></a><span data-ttu-id="034af-102">Describe a relationship between entities with connection roles</span><span class="sxs-lookup"><span data-stu-id="034af-102">Describe a relationship between entities with connection roles</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="034af-103">You can describe the relationship between records through the roles that you assign to them.</span><span class="sxs-lookup"><span data-stu-id="034af-103">You can describe the relationship between records through the roles that you assign to them.</span></span>  
  
 <span data-ttu-id="034af-104">There are several ways you can use the connection roles in a connection:</span><span class="sxs-lookup"><span data-stu-id="034af-104">There are several ways you can use the connection roles in a connection:</span></span>  
  
-   <span data-ttu-id="034af-105">Apply the same role to the source record and to the target record.</span><span class="sxs-lookup"><span data-stu-id="034af-105">Apply the same role to the source record and to the target record.</span></span> <span data-ttu-id="034af-106">A “friend”, a “team member”, or a “colleague” are examples of roles that could be applied to both records in the connection.</span><span class="sxs-lookup"><span data-stu-id="034af-106">A “friend”, a “team member”, or a “colleague” are examples of roles that could be applied to both records in the connection.</span></span>  
  
-   <span data-ttu-id="034af-107">Apply a role to the source record or to the target record, but not to both.</span><span class="sxs-lookup"><span data-stu-id="034af-107">Apply a role to the source record or to the target record, but not to both.</span></span> <span data-ttu-id="034af-108">A “salesperson” role in a contact to opportunity connection is an example of such role.</span><span class="sxs-lookup"><span data-stu-id="034af-108">A “salesperson” role in a contact to opportunity connection is an example of such role.</span></span> <span data-ttu-id="034af-109">The records, such as opportunity, invoice, or sales order usually contain sufficient information about what they represent and do not require a role assigned to them.</span><span class="sxs-lookup"><span data-stu-id="034af-109">The records, such as opportunity, invoice, or sales order usually contain sufficient information about what they represent and do not require a role assigned to them.</span></span>  
  
-   <span data-ttu-id="034af-110">Apply two matching roles (sometimes referred to as reciprocal roles).</span><span class="sxs-lookup"><span data-stu-id="034af-110">Apply two matching roles (sometimes referred to as reciprocal roles).</span></span> <span data-ttu-id="034af-111">One role applies to a source record and the other role applies to a target record.</span><span class="sxs-lookup"><span data-stu-id="034af-111">One role applies to a source record and the other role applies to a target record.</span></span> <span data-ttu-id="034af-112">A “doctor” and a “patient”, a “parent” and a “child” are examples of matching roles.</span><span class="sxs-lookup"><span data-stu-id="034af-112">A “doctor” and a “patient”, a “parent” and a “child” are examples of matching roles.</span></span>  
  
## <a name="connection-role-categories"></a><span data-ttu-id="034af-113">Connection Role Categories</span><span class="sxs-lookup"><span data-stu-id="034af-113">Connection Role Categories</span></span>  
 <span data-ttu-id="034af-114">When you create connection roles, you can specify what category they belong to.</span><span class="sxs-lookup"><span data-stu-id="034af-114">When you create connection roles, you can specify what category they belong to.</span></span> <span data-ttu-id="034af-115">For example, you can use the following categories:</span><span class="sxs-lookup"><span data-stu-id="034af-115">For example, you can use the following categories:</span></span>  
  
- <span data-ttu-id="034af-116">Business (supplier, buyer, competitor)</span><span class="sxs-lookup"><span data-stu-id="034af-116">Business (supplier, buyer, competitor)</span></span>  
  
- <span data-ttu-id="034af-117">Family (father, sister, cousin)</span><span class="sxs-lookup"><span data-stu-id="034af-117">Family (father, sister, cousin)</span></span>  
  
- <span data-ttu-id="034af-118">Social (tennis partner, club member, friend)</span><span class="sxs-lookup"><span data-stu-id="034af-118">Social (tennis partner, club member, friend)</span></span>  
  
  <span data-ttu-id="034af-119">The category list is customizable.</span><span class="sxs-lookup"><span data-stu-id="034af-119">The category list is customizable.</span></span> <span data-ttu-id="034af-120">You can add the categories that best fit your business model.</span><span class="sxs-lookup"><span data-stu-id="034af-120">You can add the categories that best fit your business model.</span></span>  
  
## <a name="create-connection-roles"></a><span data-ttu-id="034af-121">Create Connection Roles</span><span class="sxs-lookup"><span data-stu-id="034af-121">Create Connection Roles</span></span>  
 <span data-ttu-id="034af-122">To create a connection role you must specify the following information:</span><span class="sxs-lookup"><span data-stu-id="034af-122">To create a connection role you must specify the following information:</span></span>  
  
- <span data-ttu-id="034af-123">Use the `ConnectionRole.Name` attribute to specify a role name.</span><span class="sxs-lookup"><span data-stu-id="034af-123">Use the `ConnectionRole.Name` attribute to specify a role name.</span></span>  
  
- <span data-ttu-id="034af-124">Use the `ConnectionRole.Description` attribute to add a role description.</span><span class="sxs-lookup"><span data-stu-id="034af-124">Use the `ConnectionRole.Description` attribute to add a role description.</span></span>  
  
- <span data-ttu-id="034af-125">Use the `ConnectionRole.Category` attribute to specify a role category.</span><span class="sxs-lookup"><span data-stu-id="034af-125">Use the `ConnectionRole.Category` attribute to specify a role category.</span></span> <span data-ttu-id="034af-126">The possible values for this attribute are defined in the `connectionrole_category` global option set.</span><span class="sxs-lookup"><span data-stu-id="034af-126">The possible values for this attribute are defined in the `connectionrole_category` global option set.</span></span>  
  
- <span data-ttu-id="034af-127">When you create a connection role, you can specify an entity type that the role will be applied to, such as lead, account, or competitor.</span><span class="sxs-lookup"><span data-stu-id="034af-127">When you create a connection role, you can specify an entity type that the role will be applied to, such as lead, account, or competitor.</span></span> <span data-ttu-id="034af-128">If you do not specify a particular entity type, then you can apply a connection role to all [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] entities.</span><span class="sxs-lookup"><span data-stu-id="034af-128">If you do not specify a particular entity type, then you can apply a connection role to all [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] entities.</span></span> <span data-ttu-id="034af-129">To specify the entity type, use the `ConnectionRoleObjectTypeCode.AssociatedObjectTypeCode` attribute.</span><span class="sxs-lookup"><span data-stu-id="034af-129">To specify the entity type, use the `ConnectionRoleObjectTypeCode.AssociatedObjectTypeCode` attribute.</span></span> <span data-ttu-id="034af-130">To link the connection role to a particular entity type, use the `ConnectionRoleObjectTypeCode.ConnectionRoleId` attribute.</span><span class="sxs-lookup"><span data-stu-id="034af-130">To link the connection role to a particular entity type, use the `ConnectionRoleObjectTypeCode.ConnectionRoleId` attribute.</span></span> <span data-ttu-id="034af-131">A connection role record can be referenced by multiple connection role object type code records.</span><span class="sxs-lookup"><span data-stu-id="034af-131">A connection role record can be referenced by multiple connection role object type code records.</span></span> <span data-ttu-id="034af-132">If you remove all references to the connection role record, you can apply this connection role to all [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] entities.</span><span class="sxs-lookup"><span data-stu-id="034af-132">If you remove all references to the connection role record, you can apply this connection role to all [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] entities.</span></span>  
  
  > [!TIP]
  >  <span data-ttu-id="034af-133">To find the connection roles for an account entity, in the query, specify all roles that are linked to the account entity (Entity Type Code = 1) or to all entities (Entity Type Code = 0).</span><span class="sxs-lookup"><span data-stu-id="034af-133">To find the connection roles for an account entity, in the query, specify all roles that are linked to the account entity (Entity Type Code = 1) or to all entities (Entity Type Code = 0).</span></span>  
  
## <a name="associate-and-disassociate-connection-roles"></a><span data-ttu-id="034af-134">Associate and Disassociate Connection Roles</span><span class="sxs-lookup"><span data-stu-id="034af-134">Associate and Disassociate Connection Roles</span></span>  
 <span data-ttu-id="034af-135">To associate the roles in the connection, use the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Associate*> method.</span><span class="sxs-lookup"><span data-stu-id="034af-135">To associate the roles in the connection, use the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Associate*> method.</span></span> <span data-ttu-id="034af-136">To disassociate the roles, use the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Disassociate*> method.</span><span class="sxs-lookup"><span data-stu-id="034af-136">To disassociate the roles, use the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Disassociate*> method.</span></span> <span data-ttu-id="034af-137">For more information about the `Associate` message and the `Disassociate` message, see [Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md).</span><span class="sxs-lookup"><span data-stu-id="034af-137">For more information about the `Associate` message and the `Disassociate` message, see [Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="034af-138">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="034af-138">See also</span></span>  
 <span data-ttu-id="034af-139">[Connection Entities](connection-entities.md) </span><span class="sxs-lookup"><span data-stu-id="034af-139">[Connection Entities](connection-entities.md) </span></span>  
 <span data-ttu-id="034af-140">[Sample Code for Connection Entities](sample-code-connection-entities.md) </span><span class="sxs-lookup"><span data-stu-id="034af-140">[Sample Code for Connection Entities](sample-code-connection-entities.md) </span></span>  
 <span data-ttu-id="034af-141">[Sample: Create Reciprocal Connection Role (Early Bound)](sample-create-reciprocal-connection-role-early-bound.md) </span><span class="sxs-lookup"><span data-stu-id="034af-141">[Sample: Create Reciprocal Connection Role (Early Bound)](sample-create-reciprocal-connection-role-early-bound.md) </span></span>  
 [<span data-ttu-id="034af-142">Connection Entity</span><span class="sxs-lookup"><span data-stu-id="034af-142">Connection Entity</span></span>](entities/connection.md)
