---
title: Use the early bound entity classes to associate records (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how you can create an association between related records using AddLink method in OrganizationServiceContext class for a one-to-many relationship and Associate method in IOrganizationService class using for a many-to-many relationship
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
- adding or updating associations between related records, early bound-entity classes
- using early-bound entity classes in code, adding or updating associations between related records
- using early bound-entity classes to add or update associations between related records
ms.assetid: 72e6f386-94f0-43a9-aa33-d13a6b2b9628
caps.latest.revision: 24
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 54051d0de5e7d94f7f79b948305b4048b929c978
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388462"
---
# <a name="use-the-early-bound-entity-classes-to-associate-records"></a><span data-ttu-id="4515d-103">Use the early bound entity classes to associate records</span><span class="sxs-lookup"><span data-stu-id="4515d-103">Use the early bound entity classes to associate records</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="4515d-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps, you can create an association by using early binding in several ways.</span><span class="sxs-lookup"><span data-stu-id="4515d-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps, you can create an association by using early binding in several ways.</span></span> <span data-ttu-id="4515d-105">To create a one-to-many relationship, you can use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.AddLink(Microsoft.Xrm.Sdk.Entity,Microsoft.Xrm.Sdk.Relationship,Microsoft.Xrm.Sdk.Entity)> method in the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> class.</span><span class="sxs-lookup"><span data-stu-id="4515d-105">To create a one-to-many relationship, you can use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.AddLink(Microsoft.Xrm.Sdk.Entity,Microsoft.Xrm.Sdk.Relationship,Microsoft.Xrm.Sdk.Entity)> method in the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> class.</span></span> <span data-ttu-id="4515d-106">To create a many-to-many relationship, you can use the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Associate*> method in the<xref:Microsoft.Xrm.Sdk.IOrganizationService> class to create an association.</span><span class="sxs-lookup"><span data-stu-id="4515d-106">To create a many-to-many relationship, you can use the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Associate*> method in the<xref:Microsoft.Xrm.Sdk.IOrganizationService> class to create an association.</span></span> <span data-ttu-id="4515d-107">You can also create the association by updating the foreign key of the target entity to match the primary key of the new source entity.</span><span class="sxs-lookup"><span data-stu-id="4515d-107">You can also create the association by updating the foreign key of the target entity to match the primary key of the new source entity.</span></span>  
  
 <span data-ttu-id="4515d-108">To remove an association, you can use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.DeleteLink(Microsoft.Xrm.Sdk.Entity,Microsoft.Xrm.Sdk.Relationship,Microsoft.Xrm.Sdk.Entity)> method in the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> class or the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Disassociate*> method.</span><span class="sxs-lookup"><span data-stu-id="4515d-108">To remove an association, you can use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.DeleteLink(Microsoft.Xrm.Sdk.Entity,Microsoft.Xrm.Sdk.Relationship,Microsoft.Xrm.Sdk.Entity)> method in the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> class or the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Disassociate*> method.</span></span> <span data-ttu-id="4515d-109">You can also set the foreign key to **null**.</span><span class="sxs-lookup"><span data-stu-id="4515d-109">You can also set the foreign key to **null**.</span></span>  
  
 <span data-ttu-id="4515d-110">For a complete sample showing how to add and remove associations, see [Sample: Associate Using Strong Types](sample-associate-records-early-bound.md).</span><span class="sxs-lookup"><span data-stu-id="4515d-110">For a complete sample showing how to add and remove associations, see [Sample: Associate Using Strong Types](sample-associate-records-early-bound.md).</span></span>  
  
## <a name="use-the-addlink-method"></a><span data-ttu-id="4515d-111">Use the AddLink method</span><span class="sxs-lookup"><span data-stu-id="4515d-111">Use the AddLink method</span></span>  
 <span data-ttu-id="4515d-112">You can use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.AddLink(Microsoft.Xrm.Sdk.Entity,Microsoft.Xrm.Sdk.Relationship,Microsoft.Xrm.Sdk.Entity)> method to create associations.</span><span class="sxs-lookup"><span data-stu-id="4515d-112">You can use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.AddLink(Microsoft.Xrm.Sdk.Entity,Microsoft.Xrm.Sdk.Relationship,Microsoft.Xrm.Sdk.Entity)> method to create associations.</span></span> <span data-ttu-id="4515d-113">You must call the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.SaveChanges> method before the server is updated with the new link information.</span><span class="sxs-lookup"><span data-stu-id="4515d-113">You must call the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.SaveChanges> method before the server is updated with the new link information.</span></span>  
  
 <span data-ttu-id="4515d-114">The following code example shows how to create an association between a contact and an account.</span><span class="sxs-lookup"><span data-stu-id="4515d-114">The following code example shows how to create an association between a contact and an account.</span></span>  
  
```csharp  
Relationship relationship = new Relationship("account_primary_contact");  
context.AddLink(contact, relationship, account);  
context.SaveChanges();  
```  
  
## <a name="use-the-associate-method"></a><span data-ttu-id="4515d-115">Use the Associate method</span><span class="sxs-lookup"><span data-stu-id="4515d-115">Use the Associate method</span></span>  
 <span data-ttu-id="4515d-116">You use the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Associate*> method to create both one-to-many and many-to-many associations.</span><span class="sxs-lookup"><span data-stu-id="4515d-116">You use the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Associate*> method to create both one-to-many and many-to-many associations.</span></span> <span data-ttu-id="4515d-117">The following code example shows how to create a one-to-many association between an account and a contact.</span><span class="sxs-lookup"><span data-stu-id="4515d-117">The following code example shows how to create a one-to-many association between an account and a contact.</span></span>  
  
```csharp  
Relationship relationship2 = new Relationship("account_primary_contact");  
EntityReferenceCollection relatedEntities = new EntityReferenceCollection();  
relatedEntities.Add(new EntityReference(Account.EntityLogicalName, firstaccount.Id));  
_serviceProxy.Associate(Contact.EntityLogicalName, firstcontact.Id, relationship2, relatedEntities);  
```  
  
### <a name="see-also"></a><span data-ttu-id="4515d-118">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="4515d-118">See also</span></span>  
 <span data-ttu-id="4515d-119">[Use the Early Bound Entity Classes](use-early-bound-entity-classes-code.md) </span><span class="sxs-lookup"><span data-stu-id="4515d-119">[Use the Early Bound Entity Classes](use-early-bound-entity-classes-code.md) </span></span>  
 <span data-ttu-id="4515d-120">[Mix Early and Late Bound Entities](mix-early-late-bound-entities.md) </span><span class="sxs-lookup"><span data-stu-id="4515d-120">[Mix Early and Late Bound Entities](mix-early-late-bound-entities.md) </span></span>  
 [<span data-ttu-id="4515d-121">Use the Early Bound Entity Classes for Create, Update and Delete</span><span class="sxs-lookup"><span data-stu-id="4515d-121">Use the Early Bound Entity Classes for Create, Update and Delete</span></span>](use-early-bound-entity-classes-create-update-delete.md)
