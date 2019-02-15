---
title: xRM messages in the Organization service (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read about the data messages available in the xRM namespace
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
- Microsoft.Xrm.Sdk.Messages namespace, list of data and metadata messages in
- Xrm namespace, list of data and metadata messages in
- Xrm messages in the organization service
- IOrganizationService web service, Xrm messages in
- Xrm messages in the IOrganizationService
- organization service web service, Xrm messages in
ms.assetid: f392ebae-4012-4861-a335-42e1d9243409
caps.latest.revision: 39
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2839a961b017aa9649ed5f54042a4d93988a546d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386762"
---
# <a name="xrm-messages-in-the-organization-service"></a><span data-ttu-id="9e2ff-103">xRM messages in the Organization service</span><span class="sxs-lookup"><span data-stu-id="9e2ff-103">xRM messages in the Organization service</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9e2ff-104">The <xref:Microsoft.Xrm.Sdk.Messages> namespace supports the core messages used to work with the data stored in any entity.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-104">The <xref:Microsoft.Xrm.Sdk.Messages> namespace supports the core messages used to work with the data stored in any entity.</span></span> <span data-ttu-id="9e2ff-105">This namespace also contains the messages you can use to retrieve and customize the metadata for entities, attributes, and relationships.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-105">This namespace also contains the messages you can use to retrieve and customize the metadata for entities, attributes, and relationships.</span></span>  

 <span data-ttu-id="9e2ff-106">Messages are used with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span><span class="sxs-lookup"><span data-stu-id="9e2ff-106">Messages are used with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span></span> <span data-ttu-id="9e2ff-107">method.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-107">method.</span></span> <span data-ttu-id="9e2ff-108">All messages available in the <xref:Microsoft.Xrm.Sdk.Messages> namespace apply to all three deployment types.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-108">All messages available in the <xref:Microsoft.Xrm.Sdk.Messages> namespace apply to all three deployment types.</span></span>  

 <span data-ttu-id="9e2ff-109">The request page indicates whether the message works while online (connected to the server) or offline (disconnected from the server).</span><span class="sxs-lookup"><span data-stu-id="9e2ff-109">The request page indicates whether the message works while online (connected to the server) or offline (disconnected from the server).</span></span>  

## <a name="data-messages"></a><span data-ttu-id="9e2ff-110">Data messages</span><span class="sxs-lookup"><span data-stu-id="9e2ff-110">Data messages</span></span>  
 <span data-ttu-id="9e2ff-111">The following table lists the data messages available in the xRM namespace.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-111">The following table lists the data messages available in the xRM namespace.</span></span>  


|                               <span data-ttu-id="9e2ff-112">Thông báo</span><span class="sxs-lookup"><span data-stu-id="9e2ff-112">Message</span></span>                               |                                                             <span data-ttu-id="9e2ff-113">Mô tả</span><span class="sxs-lookup"><span data-stu-id="9e2ff-113">Description</span></span>                                                              |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
|         <xref:Microsoft.Xrm.Sdk.Messages.AssociateRequest>          |                                  <span data-ttu-id="9e2ff-114">Creates a link between records that participate in a relationship.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-114">Creates a link between records that participate in a relationship.</span></span>                                  |
| <xref:Microsoft.Xrm.Sdk.Messages.ConvertDateAndTimeBehaviorRequest> |                                           [!INCLUDE[internal](../../includes/internal.md)]                                           |
|           <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest>           |                    <span data-ttu-id="9e2ff-115">Creates a record of any type that supports the **Create** message, including custom entities.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-115">Creates a record of any type that supports the **Create** message, including custom entities.</span></span>                     |
|           <xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest>           |                                                     <span data-ttu-id="9e2ff-116">Deletes an existing record.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-116">Deletes an existing record.</span></span>                                                      |
|        <xref:Microsoft.Xrm.Sdk.Messages.DisassociateRequest>        |                                                  <span data-ttu-id="9e2ff-117">Removes the link between records.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-117">Removes the link between records.</span></span>                                                   |
|        <xref:Microsoft.Xrm.Sdk.Messages.ExecuteAsyncRequest>        | <span data-ttu-id="9e2ff-118">Executes a message asynchronously.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-118">Executes a message asynchronously.</span></span> <span data-ttu-id="9e2ff-119">Currently this only supports the <xref:Microsoft.Crm.Sdk.Messages.ImportSolutionRequest> message.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-119">Currently this only supports the <xref:Microsoft.Crm.Sdk.Messages.ImportSolutionRequest> message.</span></span> |
|     <xref:Microsoft.Xrm.Sdk.Messages.ExecuteTransactionRequest>     |                                 <span data-ttu-id="9e2ff-120">Executes multiple message requests in a single database transaction.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-120">Executes multiple message requests in a single database transaction.</span></span>                                 |
|    <xref:Microsoft.Xrm.Sdk.Messages.ReactivateEntityKeyRequest>     |                                <span data-ttu-id="9e2ff-121">Submits a new asynchronous system job to create the index for the key.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-121">Submits a new asynchronous system job to create the index for the key.</span></span>                                |
|   <xref:Microsoft.Xrm.Sdk.Messages.RetrieveEntityChangesRequest>    |                                       <span data-ttu-id="9e2ff-122">Retrieves the changes in an entity since the last sync.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-122">Retrieves the changes in an entity since the last sync.</span></span>                                        |
|          <xref:Microsoft.Xrm.Sdk.Messages.RetrieveRequest>          |                                                         <span data-ttu-id="9e2ff-123">Retrieves a record.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-123">Retrieves a record.</span></span>                                                          |
|      <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest>      |             <span data-ttu-id="9e2ff-124">Retrieves a collection of records.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-124">Retrieves a collection of records.</span></span> <span data-ttu-id="9e2ff-125">The query can be specified using a query expression or a FetchXML query.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-125">The query can be specified using a query expression or a FetchXML query.</span></span>              |
|           <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest>           |                                                     <span data-ttu-id="9e2ff-126">Updates an existing record.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-126">Updates an existing record.</span></span>                                                      |
|           <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest>           |                                                     <span data-ttu-id="9e2ff-127">Updates or inserts a record.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-127">Updates or inserts a record.</span></span>                                                     |

## <a name="metadata-messages"></a><span data-ttu-id="9e2ff-128">Metadata messages</span><span class="sxs-lookup"><span data-stu-id="9e2ff-128">Metadata messages</span></span>  
 <span data-ttu-id="9e2ff-129">The following table lists the metadata messages available in the XRM namespace.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-129">The following table lists the metadata messages available in the XRM namespace.</span></span>  

|<span data-ttu-id="9e2ff-130">Thông báo</span><span class="sxs-lookup"><span data-stu-id="9e2ff-130">Message</span></span>|<span data-ttu-id="9e2ff-131">Mô tả</span><span class="sxs-lookup"><span data-stu-id="9e2ff-131">Description</span></span>|  
|-------------|-----------------|  
|<xref:Microsoft.Xrm.Sdk.Messages.CanBeReferencedRequest>|<span data-ttu-id="9e2ff-132">Checks to see if the specified entity can be the primary entity (one) in a one-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-132">Checks to see if the specified entity can be the primary entity (one) in a one-to-many relationship.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.CanBeReferencingRequest>|<span data-ttu-id="9e2ff-133">Checks to see if the specified entity can be the referencing entity (many) in a one-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-133">Checks to see if the specified entity can be the referencing entity (many) in a one-to-many relationship.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.CanManyToManyRequest>|<span data-ttu-id="9e2ff-134">Checks to see if the entity can participate in a many-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-134">Checks to see if the entity can participate in a many-to-many relationship.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest>|<span data-ttu-id="9e2ff-135">Creates a custom attribute for an entity.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-135">Creates a custom attribute for an entity.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.CreateEntityKeyRequest>|<span data-ttu-id="9e2ff-136">Creates an alternate key for an entity.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-136">Creates an alternate key for an entity.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest>|<span data-ttu-id="9e2ff-137">Creates a custom entity.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-137">Creates a custom entity.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.CreateManyToManyRequest>|<span data-ttu-id="9e2ff-138">Creates a many-to-many relationship between two entities.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-138">Creates a many-to-many relationship between two entities.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.CreateOneToManyRequest>|<span data-ttu-id="9e2ff-139">Creates a one-to-many relationship between two entities.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-139">Creates a one-to-many relationship between two entities.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.CreateOptionSetRequest>|<span data-ttu-id="9e2ff-140">Creates a custom global option set.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-140">Creates a custom global option set.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.DeleteAttributeRequest>|<span data-ttu-id="9e2ff-141">Deletes an attribute from an entity.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-141">Deletes an attribute from an entity.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.DeleteEntityKeyRequest>|<span data-ttu-id="9e2ff-142">Deletes the alternate key for an entity.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-142">Deletes the alternate key for an entity.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.DeleteEntityRequest>|<span data-ttu-id="9e2ff-143">Deletes an entity.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-143">Deletes an entity.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.DeleteOptionSetRequest>|<span data-ttu-id="9e2ff-144">Deletes an option set.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-144">Deletes an option set.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.DeleteOptionValueRequest>|<span data-ttu-id="9e2ff-145">Deletes an option value from a list of options.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-145">Deletes an option value from a list of options.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.DeleteRelationshipRequest>|<span data-ttu-id="9e2ff-146">Deletes a relationship.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-146">Deletes a relationship.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.ExecuteMultipleRequest>|<span data-ttu-id="9e2ff-147">Executes one or more message requests as a single batch operation.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-147">Executes one or more message requests as a single batch operation.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.GetValidManyToManyRequest>|<span data-ttu-id="9e2ff-148">Returns the set of entities that can participate in a many-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-148">Returns the set of entities that can participate in a many-to-many relationship.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.GetValidReferencedEntitiesRequest>|<span data-ttu-id="9e2ff-149">Returns the set of entities that are valid as the primary entity (one) from the specified entity in a one-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-149">Returns the set of entities that are valid as the primary entity (one) from the specified entity in a one-to-many relationship.</span></span> <span data-ttu-id="9e2ff-150">If no entity is specified, this message returns all entities that can be the primary entity in a one-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-150">If no entity is specified, this message returns all entities that can be the primary entity in a one-to-many relationship.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.GetValidReferencingEntitiesRequest>|<span data-ttu-id="9e2ff-151">Returns the set of entities that are valid as the related entity (many) to the specified entity in a one-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-151">Returns the set of entities that are valid as the related entity (many) to the specified entity in a one-to-many relationship.</span></span> <span data-ttu-id="9e2ff-152">If no entity is specified, this message returns all entities that can be the related entity in a one-to-many relationship.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-152">If no entity is specified, this message returns all entities that can be the related entity in a one-to-many relationship.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.InsertOptionValueRequest>|<span data-ttu-id="9e2ff-153">Inserts an option value into a list of options.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-153">Inserts an option value into a list of options.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.InsertStatusValueRequest>|<span data-ttu-id="9e2ff-154">Inserts a status value into a list of status values.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-154">Inserts a status value into a list of status values.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.IsDataEncryptionActiveRequest>|<span data-ttu-id="9e2ff-155">Checks if data encryption is currently running (active or inactive).</span><span class="sxs-lookup"><span data-stu-id="9e2ff-155">Checks if data encryption is currently running (active or inactive).</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.OrderOptionRequest>|<span data-ttu-id="9e2ff-156">Sets the order of a list of options.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-156">Sets the order of a list of options.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest>|<span data-ttu-id="9e2ff-157">Retrieves the metadata for all entities.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-157">Retrieves the metadata for all entities.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllOptionSetsRequest>|<span data-ttu-id="9e2ff-158">Retrieves information about all global option sets.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-158">Retrieves information about all global option sets.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveAttributeRequest>|<span data-ttu-id="9e2ff-159">Retrieves the metadata for the specified attribute.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-159">Retrieves the metadata for the specified attribute.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveDataEncryptionKeyRequest>|<span data-ttu-id="9e2ff-160">Retrieves the data encryption key value.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-160">Retrieves the data encryption key value.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveEntityChangesRequest>|<span data-ttu-id="9e2ff-161">Retrieves the changes for an entity.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-161">Retrieves the changes for an entity.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveEntityKeyRequest>|<span data-ttu-id="9e2ff-162">Retrieves an alternate key for an entity.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-162">Retrieves an alternate key for an entity.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveEntityRequest>|<span data-ttu-id="9e2ff-163">Retrieves the metadata for the specified entity.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-163">Retrieves the metadata for the specified entity.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveManagedPropertyRequest>|<span data-ttu-id="9e2ff-164">Retrieves a managed property definition.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-164">Retrieves a managed property definition.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveMetadataChangesRequest>|<span data-ttu-id="9e2ff-165">Retrieves a collection of metadata records that satisfy the specified criteria.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-165">Retrieves a collection of metadata records that satisfy the specified criteria.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveOptionSetRequest>|<span data-ttu-id="9e2ff-166">Retrieves a specified option set.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-166">Retrieves a specified option set.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveRelationshipRequest>|<span data-ttu-id="9e2ff-167">Retrieve the metadata for the specified relationship.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-167">Retrieve the metadata for the specified relationship.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveTimestampRequest>|<span data-ttu-id="9e2ff-168">Retrieves a time stamp indicating the last time that the metadata was changed.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-168">Retrieves a time stamp indicating the last time that the metadata was changed.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.SetDataEncryptionKeyRequest>|<span data-ttu-id="9e2ff-169">Sets or restores the data encryption key.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-169">Sets or restores the data encryption key.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.UpdateAttributeRequest>|<span data-ttu-id="9e2ff-170">Updates the metadata for an attribute.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-170">Updates the metadata for an attribute.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest>|<span data-ttu-id="9e2ff-171">Updates the metadata for an entity.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-171">Updates the metadata for an entity.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.UpdateOptionSetRequest>|<span data-ttu-id="9e2ff-172">Updates an option set.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-172">Updates an option set.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.UpdateOptionValueRequest>|<span data-ttu-id="9e2ff-173">Updates the metadata for an option value.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-173">Updates the metadata for an option value.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.UpdateRelationshipRequest>|<span data-ttu-id="9e2ff-174">Updates the metadata for a relationship.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-174">Updates the metadata for a relationship.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.UpdateStateValueRequest>|<span data-ttu-id="9e2ff-175">Updates the metadata for a state value.</span><span class="sxs-lookup"><span data-stu-id="9e2ff-175">Updates the metadata for a state value.</span></span>|  

### <a name="see-also"></a><span data-ttu-id="9e2ff-176">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9e2ff-176">See also</span></span>  
 <span data-ttu-id="9e2ff-177">[Web Services: IOrganizationService](use-organization-service-read-write-data-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="9e2ff-177">[Web Services: IOrganizationService](use-organization-service-read-write-data-metadata.md) </span></span>  
 <span data-ttu-id="9e2ff-178">[Dynamics 365 for Customer Engagement apps Messages in the Organization Service](organization-service-messages.md) </span><span class="sxs-lookup"><span data-stu-id="9e2ff-178">[Dynamics 365 for Customer Engagement apps Messages in the Organization Service](organization-service-messages.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.Messages>
