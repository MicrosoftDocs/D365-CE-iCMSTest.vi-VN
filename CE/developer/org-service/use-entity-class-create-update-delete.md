---
title: Use the Entity class for create, update and delete (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how you can use the Entity class to create, update, and delete entities and entity attributes
ms.custom: ''
ms.date: 05/09/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d0eb57ae-7f45-4bde-964e-da2c6bd1f405
caps.latest.revision: 22
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b9e51e8547982f5e8d2cc4e3e5f86ab12fd2b242
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388469"
---
# <a name="use-the-entity-class-for-create-update-and-delete"></a><span data-ttu-id="21deb-103">Use the Entity class for create, update and delete</span><span class="sxs-lookup"><span data-stu-id="21deb-103">Use the Entity class for create, update and delete</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="21deb-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the <xref:Microsoft.Xrm.Sdk.Entity> class to create, update, and delete entities and entity attributes.</span><span class="sxs-lookup"><span data-stu-id="21deb-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the <xref:Microsoft.Xrm.Sdk.Entity> class to create, update, and delete entities and entity attributes.</span></span>  
  
## <a name="create-update-and-delete-using-the-entity-class"></a><span data-ttu-id="21deb-105">Create, update, and delete using the Entity class</span><span class="sxs-lookup"><span data-stu-id="21deb-105">Create, update, and delete using the Entity class</span></span>  
 <span data-ttu-id="21deb-106">When you work with the <xref:Microsoft.Xrm.Sdk.Entity> class and use late binding, you work with the entity and logical attribute name.</span><span class="sxs-lookup"><span data-stu-id="21deb-106">When you work with the <xref:Microsoft.Xrm.Sdk.Entity> class and use late binding, you work with the entity and logical attribute name.</span></span> <span data-ttu-id="21deb-107">This contrasts with early binding where you work with the entity and attribute schema name.</span><span class="sxs-lookup"><span data-stu-id="21deb-107">This contrasts with early binding where you work with the entity and attribute schema name.</span></span> <span data-ttu-id="21deb-108">The logical attribute name is all lowercase whereas the schema attribute name uses Pascal casing.</span><span class="sxs-lookup"><span data-stu-id="21deb-108">The logical attribute name is all lowercase whereas the schema attribute name uses Pascal casing.</span></span>  
  
 <span data-ttu-id="21deb-109">To create a new entity, you first create a new instance of the <xref:Microsoft.Xrm.Sdk.Entity> class and pass it an entity name.</span><span class="sxs-lookup"><span data-stu-id="21deb-109">To create a new entity, you first create a new instance of the <xref:Microsoft.Xrm.Sdk.Entity> class and pass it an entity name.</span></span> <span data-ttu-id="21deb-110">The following code example shows how to create a new account record.</span><span class="sxs-lookup"><span data-stu-id="21deb-110">The following code example shows how to create a new account record.</span></span>  
  
```csharp  
// Instantiate an account object.  
Entity account = new Entity("account");  
  
// Set the required attributes. For account, only the name is required.   
// See the metadata to determine   
// which attributes must be set for each entity.  
account["name"] = "Fourth Coffee";  
  
// Create an account record named Fourth Coffee.  
_accountId = _orgService.Create(account);  
```  
  
 <span data-ttu-id="21deb-111">In the example, a new entity object is created of type “account,” attributes are set, and then the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="21deb-111">In the example, a new entity object is created of type “account,” attributes are set, and then the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span> <span data-ttu-id="21deb-112">method is called to create the new record.</span><span class="sxs-lookup"><span data-stu-id="21deb-112">method is called to create the new record.</span></span>  
  
 <span data-ttu-id="21deb-113">To update an entity, you set a value for the attribute to be updated, and then call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span><span class="sxs-lookup"><span data-stu-id="21deb-113">To update an entity, you set a value for the attribute to be updated, and then call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span></span> <span data-ttu-id="21deb-114">method.</span><span class="sxs-lookup"><span data-stu-id="21deb-114">method.</span></span> 

> [!IMPORTANT]
>  <span data-ttu-id="21deb-115">When updating an entity, only include the attributes you are changing.</span><span class="sxs-lookup"><span data-stu-id="21deb-115">When updating an entity, only include the attributes you are changing.</span></span> <span data-ttu-id="21deb-116">Simply updating the attributes of an entity that you previously retrieved will update each attribute even though the value is unchanged.</span><span class="sxs-lookup"><span data-stu-id="21deb-116">Simply updating the attributes of an entity that you previously retrieved will update each attribute even though the value is unchanged.</span></span> <span data-ttu-id="21deb-117">This can cause system events that can trigger business logic that expects that the values have actually changed.</span><span class="sxs-lookup"><span data-stu-id="21deb-117">This can cause system events that can trigger business logic that expects that the values have actually changed.</span></span> <span data-ttu-id="21deb-118">This can also cause attributes to appear to have been updated in auditing data when in fact they haven’t actually changed.</span><span class="sxs-lookup"><span data-stu-id="21deb-118">This can also cause attributes to appear to have been updated in auditing data when in fact they haven’t actually changed.</span></span>
>
> <span data-ttu-id="21deb-119">You should create a new entity instance, set the id attribute and any attribute values you are changing, and use that entity instance to update the record.</span><span class="sxs-lookup"><span data-stu-id="21deb-119">You should create a new entity instance, set the id attribute and any attribute values you are changing, and use that entity instance to update the record.</span></span>


<span data-ttu-id="21deb-120">The following code example shows how to update an attribute in an account.</span><span class="sxs-lookup"><span data-stu-id="21deb-120">The following code example shows how to update an attribute in an account.</span></span>  
  
```csharp  
string newPostalCode = "98052";
Entity account = new Entity("account");  
// Create a column set to define which attributes should be retrieved.  
ColumnSet attributes = new ColumnSet(new string[] { "name", "ownerid", "address1_postalcode" });   

// Retrieve the account and its name, ownerid, and address1_postalcode attributes.  
account = _orgService.Retrieve(account.LogicalName, _accountId, attributes);  

// Test to make sure that the existing value isn’t the same as the current value  
if(account["address1_postalcode"] != newPostalCode)
{
// Create a new entity instance for update
Entity accountToUpdate = new Entity("account");  

// Set the unique identifier for the account to update.
accountToUpdate["accountid"] = account["accountid"];
// Update the postal code attribute.  
accountToUpdate["address1_postalcode"] = newPostalCode;  

// Update the account.  
_orgService.Update(accountToUpdate); 
}
```  
  
 <span data-ttu-id="21deb-121">To delete an entity, you can pass the key attribute information to the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span><span class="sxs-lookup"><span data-stu-id="21deb-121">To delete an entity, you can pass the key attribute information to the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span></span> <span data-ttu-id="21deb-122">method.</span><span class="sxs-lookup"><span data-stu-id="21deb-122">method.</span></span> <span data-ttu-id="21deb-123">The following code example shows how to use the `Delete` method.</span><span class="sxs-lookup"><span data-stu-id="21deb-123">The following code example shows how to use the `Delete` method.</span></span>  
  
```csharp 
_orgService.Delete("account", _accountId);  
```  
  
### <a name="see-also"></a><span data-ttu-id="21deb-124">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="21deb-124">See also</span></span>  
 <span data-ttu-id="21deb-125">[Use the Entity Class to Add or Update Associations Between Related Records](use-entity-class-add-update-associations-records.md) </span><span class="sxs-lookup"><span data-stu-id="21deb-125">[Use the Entity Class to Add or Update Associations Between Related Records](use-entity-class-add-update-associations-records.md) </span></span>  
 [<span data-ttu-id="21deb-126">Use the Late Bound Entity Class</span><span class="sxs-lookup"><span data-stu-id="21deb-126">Use the Late Bound Entity Class</span></span>](use-late-bound-entity-class-code.md)
