---
title: Use the Entity class to add or update associations between related records (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how you can use the IOrganizationService. Associate and IOrganizationService.Disassociate methods to create and remove associations between related records
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: ffb2c5cb-3d16-4324-b7b8-d53eec55490d
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bc32f6b5724c50628b1a1efc1dc7aa7bedbe01d1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387022"
---
# <a name="use-the-entity-class-to-add-or-update-associations-between-related-records"></a><span data-ttu-id="7fe36-104">Use the Entity class to add or update associations between related records</span><span class="sxs-lookup"><span data-stu-id="7fe36-104">Use the Entity class to add or update associations between related records</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="7fe36-105">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span><span class="sxs-lookup"><span data-stu-id="7fe36-105">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span></span> <span data-ttu-id="7fe36-106"><xref:Microsoft.Xrm.Sdk.IOrganizationService.Associate*> and <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Disassociate*></span><span class="sxs-lookup"><span data-stu-id="7fe36-106"><xref:Microsoft.Xrm.Sdk.IOrganizationService.Associate*> and <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Disassociate*></span></span> <span data-ttu-id="7fe36-107">methods to create and remove associations between related records.</span><span class="sxs-lookup"><span data-stu-id="7fe36-107">methods to create and remove associations between related records.</span></span>  
  
 <span data-ttu-id="7fe36-108">To create an association, you first determine the unique ID of the target entity to be associated.</span><span class="sxs-lookup"><span data-stu-id="7fe36-108">To create an association, you first determine the unique ID of the target entity to be associated.</span></span> <span data-ttu-id="7fe36-109">You then create a collection of entities to be associated with the target entity.</span><span class="sxs-lookup"><span data-stu-id="7fe36-109">You then create a collection of entities to be associated with the target entity.</span></span> <span data-ttu-id="7fe36-110">Next, you define a relationship between the entities in the collection and the target entity.</span><span class="sxs-lookup"><span data-stu-id="7fe36-110">Next, you define a relationship between the entities in the collection and the target entity.</span></span> <span data-ttu-id="7fe36-111">Finally, you pass this information to the `Associate` method.</span><span class="sxs-lookup"><span data-stu-id="7fe36-111">Finally, you pass this information to the `Associate` method.</span></span> <span data-ttu-id="7fe36-112">The same information is passed to the `Disassociate` method when you remove an association.</span><span class="sxs-lookup"><span data-stu-id="7fe36-112">The same information is passed to the `Disassociate` method when you remove an association.</span></span>  
  
 <span data-ttu-id="7fe36-113">The following code example shows how to create associations between related records and how to disassociate them.</span><span class="sxs-lookup"><span data-stu-id="7fe36-113">The following code example shows how to create associations between related records and how to disassociate them.</span></span>  
  
```csharp  
// The account ID would typically be passed in as an argument or determined by a query.  
// The contact ID would typically be passed in as an argument or determined by a query.  
// Associate the accounts to the contact record.   
//Create a collection of the entity ids that will be associated to the contact.  
EntityReferenceCollection relatedEntities = new EntityReferenceCollection();  
relatedEntities.Add(new EntityReference("account", _account1Id));  
relatedEntities.Add(new EntityReference("account", _account2Id));  
relatedEntities.Add(new EntityReference("account", _account3Id));   
// Create an object that defines the relationship between the contact and account.  
Relationship relationship = new Relationship("account_primary_contact");  
  //Associate the contact with the 3 accounts.  
_orgService.Associate("contact", _contactId, relationship, relatedEntities);   
Console.WriteLine("The entities have been associated.");   
//Disassociate the records.  
_orgService.Disassociate("contact", _contactId, relationship, relatedEntities);   
Console.WriteLine("The entities have been disassociated.");  
```  
  
### <a name="see-also"></a><span data-ttu-id="7fe36-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="7fe36-114">See also</span></span>  
 <span data-ttu-id="7fe36-115">[Use the Late Bound Entity Class in Code](use-late-bound-entity-class-code.md) </span><span class="sxs-lookup"><span data-stu-id="7fe36-115">[Use the Late Bound Entity Class in Code](use-late-bound-entity-class-code.md) </span></span>  
 <span data-ttu-id="7fe36-116">[Use the Entity Class for Create, Update and Delete](use-entity-class-create-update-delete.md) </span><span class="sxs-lookup"><span data-stu-id="7fe36-116">[Use the Entity Class for Create, Update and Delete](use-entity-class-create-update-delete.md) </span></span>  
 <span data-ttu-id="7fe36-117">[Hành vi mối quan hệ của thực thể](../entity-relationship-behavior.md) </span><span class="sxs-lookup"><span data-stu-id="7fe36-117">[Entity relationship behavior](../entity-relationship-behavior.md) </span></span>  
 [<span data-ttu-id="7fe36-118">Sample: Create, Retrieve, Update and Delete (CRUD) Using Property Bag (Loosely-typed)</span><span class="sxs-lookup"><span data-stu-id="7fe36-118">Sample: Create, Retrieve, Update and Delete (CRUD) Using Property Bag (Loosely-typed)</span></span>](sample-create-retrieve-update-delete-late-bound.md)
