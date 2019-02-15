---
title: Use the early-bound entity classes for create, update, and delete (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how to create, update and delete an entity record using the early-bound entity classes and OrganizationServiceContext class
ms.custom: ''
ms.date: 05/09/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: aa467b48-73b0-465b-a434-1fcbc49b76b6
caps.latest.revision: 37
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f7bb1764256cd594166c80df10466d5a229cd644
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388496"
---
# <a name="use-the-early-bound-entity-classes-for-create-update-and-delete"></a><span data-ttu-id="d51a5-103">Use the early-bound entity classes for create, update, and delete</span><span class="sxs-lookup"><span data-stu-id="d51a5-103">Use the early-bound entity classes for create, update, and delete</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d51a5-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps, you can use the entity data model and the early-bound entity classes, created by the code generation tool ([!INCLUDE[sdk_CodeGenUtility](../../includes/sdk-codegenutility.md)]), to work with business data.</span><span class="sxs-lookup"><span data-stu-id="d51a5-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps, you can use the entity data model and the early-bound entity classes, created by the code generation tool ([!INCLUDE[sdk_CodeGenUtility](../../includes/sdk-codegenutility.md)]), to work with business data.</span></span> <span data-ttu-id="d51a5-105">You can use these early-bound classes with or without the organization service context, but a best practice is to use the generated organization service context class.</span><span class="sxs-lookup"><span data-stu-id="d51a5-105">You can use these early-bound classes with or without the organization service context, but a best practice is to use the generated organization service context class.</span></span> <span data-ttu-id="d51a5-106">The context attempts to manage relationships efficiently, but handwritten code can typically be even more efficient.</span><span class="sxs-lookup"><span data-stu-id="d51a5-106">The context attempts to manage relationships efficiently, but handwritten code can typically be even more efficient.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d51a5-107">Updates to records are made in a specific order.</span><span class="sxs-lookup"><span data-stu-id="d51a5-107">Updates to records are made in a specific order.</span></span> <span data-ttu-id="d51a5-108">First, primary entities are processed, and then related entities are processed.</span><span class="sxs-lookup"><span data-stu-id="d51a5-108">First, primary entities are processed, and then related entities are processed.</span></span> <span data-ttu-id="d51a5-109">If a change is made by the primary entity for a lookup or related entity attribute, and then a related entity updates the same attribute, the related entity value is retained.</span><span class="sxs-lookup"><span data-stu-id="d51a5-109">If a change is made by the primary entity for a lookup or related entity attribute, and then a related entity updates the same attribute, the related entity value is retained.</span></span> <span data-ttu-id="d51a5-110">In general, a lookup attribute value and its equivalent in the `RelatedEntities` (or navigation properties) for the same relationship should not be used at the same time.</span><span class="sxs-lookup"><span data-stu-id="d51a5-110">In general, a lookup attribute value and its equivalent in the `RelatedEntities` (or navigation properties) for the same relationship should not be used at the same time.</span></span>  
  
<a name="use_context"></a>   

## <a name="use-the-organizationservicecontext-class"></a><span data-ttu-id="d51a5-111">Use the OrganizationServiceContext class</span><span class="sxs-lookup"><span data-stu-id="d51a5-111">Use the OrganizationServiceContext class</span></span>  

 <span data-ttu-id="d51a5-112">The organization service context class that the code generation tool creates and that inherits from <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> is used to track data changes.</span><span class="sxs-lookup"><span data-stu-id="d51a5-112">The organization service context class that the code generation tool creates and that inherits from <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext> is used to track data changes.</span></span> <span data-ttu-id="d51a5-113">The context tracks objects that are instances of entity types that represent data in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="d51a5-113">The context tracks objects that are instances of entity types that represent data in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span></span> <span data-ttu-id="d51a5-114">You can modify, create, and delete objects in the organization service context, and [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps tracks the changes that you made to these objects.</span><span class="sxs-lookup"><span data-stu-id="d51a5-114">You can modify, create, and delete objects in the organization service context, and [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps tracks the changes that you made to these objects.</span></span> <span data-ttu-id="d51a5-115">When the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext>.<xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.SaveChanges></span><span class="sxs-lookup"><span data-stu-id="d51a5-115">When the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext>.<xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.SaveChanges></span></span> <span data-ttu-id="d51a5-116">method is called, [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)]apps generates and executes commands that perform the equivalent insert, update, or delete statements against data in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="d51a5-116">method is called, [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)]apps generates and executes commands that perform the equivalent insert, update, or delete statements against data in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span></span>  
  
 <span data-ttu-id="d51a5-117">When working with early-bound entity classes, you use the entity name and attribute schema name to specify an entity or attribute to work with.</span><span class="sxs-lookup"><span data-stu-id="d51a5-117">When working with early-bound entity classes, you use the entity name and attribute schema name to specify an entity or attribute to work with.</span></span> <span data-ttu-id="d51a5-118">Attribute schema names are defined in <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.SchemaName></span><span class="sxs-lookup"><span data-stu-id="d51a5-118">Attribute schema names are defined in <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.SchemaName></span></span> <span data-ttu-id="d51a5-119">and <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.SchemaName>, or you can use the class and property names shown in the code-generated file.The following sample shows how to assign a value to the email attribute of a new contact instance.</span><span class="sxs-lookup"><span data-stu-id="d51a5-119">and <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.SchemaName>, or you can use the class and property names shown in the code-generated file.The following sample shows how to assign a value to the email attribute of a new contact instance.</span></span>  
  
```csharp  
Contact contact = new Contact();
contact.EMailAddress1 = “sonny@contoso.com”;  
```  
  
 <span data-ttu-id="d51a5-120">For a complete code sample that shows how to use early-bound entity classes to perform basic database actions, see [Sample: Create, Retrieve, Update and Delete (CRUD) Using Strong Types](sample-create-retrieve-update-delete-records-early-bound.md).</span><span class="sxs-lookup"><span data-stu-id="d51a5-120">For a complete code sample that shows how to use early-bound entity classes to perform basic database actions, see [Sample: Create, Retrieve, Update and Delete (CRUD) Using Strong Types](sample-create-retrieve-update-delete-records-early-bound.md).</span></span>  
  
<a name="create_new"></a>   

## <a name="create-a-new-entity-record-using-the-early-bound-entity-classes-and-the-organizationservicecontext-class"></a><span data-ttu-id="d51a5-121">Create a new entity record using the early-bound entity classes and the OrganizationServiceContext class</span><span class="sxs-lookup"><span data-stu-id="d51a5-121">Create a new entity record using the early-bound entity classes and the OrganizationServiceContext class</span></span>  

 <span data-ttu-id="d51a5-122">When you want to insert data into [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps by using the entity data model, you must create an instance of an entity type and add the object to an organization service context.</span><span class="sxs-lookup"><span data-stu-id="d51a5-122">When you want to insert data into [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps by using the entity data model, you must create an instance of an entity type and add the object to an organization service context.</span></span> <span data-ttu-id="d51a5-123">The organization service context must be tracking the object before it can save the object to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="d51a5-123">The organization service context must be tracking the object before it can save the object to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span></span>  
  
 <span data-ttu-id="d51a5-124">When creating a new entity record, you add the object to the organization service context by using the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.AddObject(Microsoft.Xrm.Sdk.Entity)>.</span><span class="sxs-lookup"><span data-stu-id="d51a5-124">When creating a new entity record, you add the object to the organization service context by using the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.AddObject(Microsoft.Xrm.Sdk.Entity)>.</span></span> <span data-ttu-id="d51a5-125">method.</span><span class="sxs-lookup"><span data-stu-id="d51a5-125">method.</span></span>  
  
 <span data-ttu-id="d51a5-126">The following sample shows how to instantiate and save a new contact record by using the entity data model.</span><span class="sxs-lookup"><span data-stu-id="d51a5-126">The following sample shows how to instantiate and save a new contact record by using the entity data model.</span></span> <span data-ttu-id="d51a5-127">It also demonstrates how tp access a custom attribute.</span><span class="sxs-lookup"><span data-stu-id="d51a5-127">It also demonstrates how tp access a custom attribute.</span></span>  
  
```csharp  
OrganizationServiceContext orgContext =new OrganizationServiceContext(_serviceProxy);  
Contact contact = new Contact()     
 {  
   FirstName = "Charles",  
   LastName = "Brown",  
   Address1_Line1 = "123 Main St.",  
   Address1_City = "Des Moines",  
   Address1_StateOrProvince = "IA",  
   Address1_PostalCode = "21254",  
   new_twittername = "Chuck",  
   Telephone1 = "123-234-5678"  
 };   
orgContext.AddObject(contact);orgContext.SaveChanges();  
```  
  
 <span data-ttu-id="d51a5-128">After you add an object to the context and before the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext>.<xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.SaveChanges></span><span class="sxs-lookup"><span data-stu-id="d51a5-128">After you add an object to the context and before the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext>.<xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.SaveChanges></span></span> <span data-ttu-id="d51a5-129">method is called, the context generates an ID for the new object.</span><span class="sxs-lookup"><span data-stu-id="d51a5-129">method is called, the context generates an ID for the new object.</span></span> <span data-ttu-id="d51a5-130">An exception that contains the `SaveChangesResults` is thrown from the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.SaveChanges> method if any updates to the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps data fail.</span><span class="sxs-lookup"><span data-stu-id="d51a5-130">An exception that contains the `SaveChangesResults` is thrown from the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.SaveChanges> method if any updates to the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps data fail.</span></span>  
  
<a name="update"></a>   

## <a name="update-an-entity-record-using-early-bound-entity-classes-and-the-organizationservicecontext-class"></a><span data-ttu-id="d51a5-131">Update an entity record using early-bound entity classes and the OrganizationServiceContext class</span><span class="sxs-lookup"><span data-stu-id="d51a5-131">Update an entity record using early-bound entity classes and the OrganizationServiceContext class</span></span>  

 [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] <span data-ttu-id="d51a5-132">apps tracks changes to objects that are attached to the organization service context.</span><span class="sxs-lookup"><span data-stu-id="d51a5-132">apps tracks changes to objects that are attached to the organization service context.</span></span> <span data-ttu-id="d51a5-133">To modify an existing entity record, you must first add the object to the context.</span><span class="sxs-lookup"><span data-stu-id="d51a5-133">To modify an existing entity record, you must first add the object to the context.</span></span> <span data-ttu-id="d51a5-134">To add an object to the context, you must first retrieve the entity record from [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps and then add the object to the context by using the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.Attach(Microsoft.Xrm.Sdk.Entity)> method.</span><span class="sxs-lookup"><span data-stu-id="d51a5-134">To add an object to the context, you must first retrieve the entity record from [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps and then add the object to the context by using the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.Attach(Microsoft.Xrm.Sdk.Entity)> method.</span></span> <span data-ttu-id="d51a5-135">Once the object is being tracked by the context, you can update the record by setting the entity’s attributes.</span><span class="sxs-lookup"><span data-stu-id="d51a5-135">Once the object is being tracked by the context, you can update the record by setting the entity’s attributes.</span></span>  
  
 <span data-ttu-id="d51a5-136">The following sample shows how to update an account attribute by using early bound classes.</span><span class="sxs-lookup"><span data-stu-id="d51a5-136">The following sample shows how to update an account attribute by using early bound classes.</span></span>  
  
```csharp  
Account.EMailAddress1 = “Contoso-WebMaster@contoso.com”;  
```  
  
 <span data-ttu-id="d51a5-137">The following sample shows how to delete an attribute value.</span><span class="sxs-lookup"><span data-stu-id="d51a5-137">The following sample shows how to delete an attribute value.</span></span>  
  
```csharp  
Account.EMailAddress1 = null;  
```  
  
 <span data-ttu-id="d51a5-138">There are two partial methods named `OnPropertyChanging` and `OnPropertyChanged` for each entity.</span><span class="sxs-lookup"><span data-stu-id="d51a5-138">There are two partial methods named `OnPropertyChanging` and `OnPropertyChanged` for each entity.</span></span> <span data-ttu-id="d51a5-139">These methods are called in the property setter.</span><span class="sxs-lookup"><span data-stu-id="d51a5-139">These methods are called in the property setter.</span></span> <span data-ttu-id="d51a5-140">You can extend these methods by using partial classes to insert custom business logic.</span><span class="sxs-lookup"><span data-stu-id="d51a5-140">You can extend these methods by using partial classes to insert custom business logic.</span></span>  
  
<a name="delete"></a>   

## <a name="delete-an-entity-record-using-early-bound-entity-classes-and-the-organizationservicecontext-class"></a><span data-ttu-id="d51a5-141">Delete an entity record using early-bound entity classes and the OrganizationServiceContext class</span><span class="sxs-lookup"><span data-stu-id="d51a5-141">Delete an entity record using early-bound entity classes and the OrganizationServiceContext class</span></span>  

 <span data-ttu-id="d51a5-142">To delete an entity record, the organization service context must be tracking the object.</span><span class="sxs-lookup"><span data-stu-id="d51a5-142">To delete an entity record, the organization service context must be tracking the object.</span></span> <span data-ttu-id="d51a5-143">Once the object is on the context, you can use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.DeleteObject(Microsoft.Xrm.Sdk.Entity)> method to mark the object on the context for deletion.</span><span class="sxs-lookup"><span data-stu-id="d51a5-143">Once the object is on the context, you can use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.DeleteObject(Microsoft.Xrm.Sdk.Entity)> method to mark the object on the context for deletion.</span></span> <span data-ttu-id="d51a5-144">Note that the entity record in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps is not deleted until the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext>.<xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.SaveChanges></span><span class="sxs-lookup"><span data-stu-id="d51a5-144">Note that the entity record in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps is not deleted until the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext>.<xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceContext.SaveChanges></span></span> <span data-ttu-id="d51a5-145">method is called.</span><span class="sxs-lookup"><span data-stu-id="d51a5-145">method is called.</span></span>  
  
<a name="no_context"></a>   

## <a name="use-early-bound-entity-classes-without-a-context-object"></a><span data-ttu-id="d51a5-146">Use early-bound entity classes without a Context object</span><span class="sxs-lookup"><span data-stu-id="d51a5-146">Use early-bound entity classes without a Context object</span></span>  

 <span data-ttu-id="d51a5-147">You can use the early-bound entity classes without creating an organization service context object if you do not want to create the context object.</span><span class="sxs-lookup"><span data-stu-id="d51a5-147">You can use the early-bound entity classes without creating an organization service context object if you do not want to create the context object.</span></span> <span data-ttu-id="d51a5-148">The <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy> class includes a <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.Create(Microsoft.Xrm.Sdk.Entity)> method that can be used to save entity record changes to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="d51a5-148">The <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy> class includes a <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.Create(Microsoft.Xrm.Sdk.Entity)> method that can be used to save entity record changes to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span></span>  
  
 <span data-ttu-id="d51a5-149">The following sample shows how to use an early-bound entity class without creating an organization service context object.</span><span class="sxs-lookup"><span data-stu-id="d51a5-149">The following sample shows how to use an early-bound entity class without creating an organization service context object.</span></span> <span data-ttu-id="d51a5-150">The  <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.Create(Microsoft.Xrm.Sdk.Entity)> method returns the `GUID` id assigned to the newly created entity record.</span><span class="sxs-lookup"><span data-stu-id="d51a5-150">The  <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.Create(Microsoft.Xrm.Sdk.Entity)> method returns the `GUID` id assigned to the newly created entity record.</span></span>  
  
```csharp  
Contact contact = new Contact()  
 {  
   FirstName = "Charles",  
   LastName = "Brown",  
   Address1_Line1 = "123 Main St.",  
   Address1_City = "Des Moines",  
   Address1_StateOrProvince = "IA",  
   Address1_PostalCode = "21254",  
   Telephone1 = "123-234-5678"   
  };  
 _contactId = _serviceProxy.Create(contact);   
```  
  
 <span data-ttu-id="d51a5-151">To update an entity record in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps, you retrieve the data to be updated, make the necessary changes, and then use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy>.<xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.Update(Microsoft.Xrm.Sdk.Entity)></span><span class="sxs-lookup"><span data-stu-id="d51a5-151">To update an entity record in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps, you retrieve the data to be updated, make the necessary changes, and then use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy>.<xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.Update(Microsoft.Xrm.Sdk.Entity)></span></span> <span data-ttu-id="d51a5-152">method to commit those changes to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="d51a5-152">method to commit those changes to [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span></span> 

> [!IMPORTANT]
>  <span data-ttu-id="d51a5-153">When updating an entity, only include the attributes you are changing.</span><span class="sxs-lookup"><span data-stu-id="d51a5-153">When updating an entity, only include the attributes you are changing.</span></span> <span data-ttu-id="d51a5-154">Simply updating the attributes of an entity that you previously retrieved will update each attribute even though the value is unchanged.</span><span class="sxs-lookup"><span data-stu-id="d51a5-154">Simply updating the attributes of an entity that you previously retrieved will update each attribute even though the value is unchanged.</span></span> <span data-ttu-id="d51a5-155">This can cause system events that can trigger business logic that expects that the values have actually changed.</span><span class="sxs-lookup"><span data-stu-id="d51a5-155">This can cause system events that can trigger business logic that expects that the values have actually changed.</span></span> <span data-ttu-id="d51a5-156">This can also cause attributes to appear to have been updated in auditing data when in fact they haven’t actually changed.</span><span class="sxs-lookup"><span data-stu-id="d51a5-156">This can also cause attributes to appear to have been updated in auditing data when in fact they haven’t actually changed.</span></span> 
>
> <span data-ttu-id="d51a5-157">You should create a new entity instance, set the id attribute and any attribute values you are changing, and use that entity instance to update the record.</span><span class="sxs-lookup"><span data-stu-id="d51a5-157">You should create a new entity instance, set the id attribute and any attribute values you are changing, and use that entity instance to update the record.</span></span>


<span data-ttu-id="d51a5-158">To retrieve entity records, you use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy>.<xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.Retrieve(System.String,System.Guid,Microsoft.Xrm.Sdk.Query.ColumnSet)></span><span class="sxs-lookup"><span data-stu-id="d51a5-158">To retrieve entity records, you use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy>.<xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.Retrieve(System.String,System.Guid,Microsoft.Xrm.Sdk.Query.ColumnSet)></span></span> <span data-ttu-id="d51a5-159">method for single-object retrieval or the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy>.</span><span class="sxs-lookup"><span data-stu-id="d51a5-159">method for single-object retrieval or the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy>.</span></span> <span data-ttu-id="d51a5-160"><xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.RetrieveMultiple(Microsoft.Xrm.Sdk.Query.QueryBase)> method for retrieving multiple objects.</span><span class="sxs-lookup"><span data-stu-id="d51a5-160"><xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.RetrieveMultiple(Microsoft.Xrm.Sdk.Query.QueryBase)> method for retrieving multiple objects.</span></span> <span data-ttu-id="d51a5-161">To delete an entity record, you use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy>.<xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.Delete(System.String,System.Guid)></span><span class="sxs-lookup"><span data-stu-id="d51a5-161">To delete an entity record, you use the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy>.<xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.Delete(System.String,System.Guid)></span></span> <span data-ttu-id="d51a5-162">method.</span><span class="sxs-lookup"><span data-stu-id="d51a5-162">method.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d51a5-163">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d51a5-163">See also</span></span>  

 <span data-ttu-id="d51a5-164">[Use the Early Bound Entity Classes in Code](use-early-bound-entity-classes-code.md) </span><span class="sxs-lookup"><span data-stu-id="d51a5-164">[Use the Early Bound Entity Classes in Code](use-early-bound-entity-classes-code.md) </span></span>  
 <span data-ttu-id="d51a5-165">[Use the early bound entity classes to associate records](use-early-bound-entity-classes-associate-records.md) </span><span class="sxs-lookup"><span data-stu-id="d51a5-165">[Use the early bound entity classes to associate records](use-early-bound-entity-classes-associate-records.md) </span></span>  
 <span data-ttu-id="d51a5-166">[Create Strong Types with the Code Generation Tool (CrmSvcUtil.exe)](create-early-bound-entity-classes-code-generation-tool.md) </span><span class="sxs-lookup"><span data-stu-id="d51a5-166">[Create Strong Types with the Code Generation Tool (CrmSvcUtil.exe)](create-early-bound-entity-classes-code-generation-tool.md) </span></span>  
 [<span data-ttu-id="d51a5-167">Sample: Create, Retrieve, Update and Delete (CRUD) Using Strong Types</span><span class="sxs-lookup"><span data-stu-id="d51a5-167">Sample: Create, Retrieve, Update and Delete (CRUD) Using Strong Types</span></span>](sample-create-retrieve-update-delete-records-early-bound.md)
