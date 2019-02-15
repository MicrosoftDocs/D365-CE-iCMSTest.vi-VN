---
title: Field security entities (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about using field security entities to apply field-level security, which restricts field access to specified users and teams.
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
- field-level security, scope of
- applying field-level security
- secured fields, sharing
- restricting field access
- field security profile records, creating
- securing fields vs. securing records
- field permission attributes
- field-level security, setting up and using
- creating field security profile records
- field access, restricting
- sharing secured fields
ms.assetid: 3fa8b175-a73e-4b38-b73d-e385a7c6ced5
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 142949378b57cb5eb74812dcaee32a42e828596c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386860"
---
# <a name="field-security-entities"></a><span data-ttu-id="e110d-103">Field security entities</span><span class="sxs-lookup"><span data-stu-id="e110d-103">Field security entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e110d-104">You use field security entities to apply field-level security, which restricts field access to specified users and teams.</span><span class="sxs-lookup"><span data-stu-id="e110d-104">You use field security entities to apply field-level security, which restricts field access to specified users and teams.</span></span> <span data-ttu-id="e110d-105">The scope of field-level security is global, which means that it applies to all records within the organization, regardless of the business unit hierarchical level to which the record or the user belongs.</span><span class="sxs-lookup"><span data-stu-id="e110d-105">The scope of field-level security is global, which means that it applies to all records within the organization, regardless of the business unit hierarchical level to which the record or the user belongs.</span></span> <span data-ttu-id="e110d-106">Field security works in all [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] clients, including the Web client, [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)], and [!INCLUDE[pn_Mobile_Express_long](../includes/pn-mobile-express-long.md)].</span><span class="sxs-lookup"><span data-stu-id="e110d-106">Field security works in all [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] clients, including the Web client, [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)], and [!INCLUDE[pn_Mobile_Express_long](../includes/pn-mobile-express-long.md)].</span></span> <span data-ttu-id="e110d-107">It applies to all components, such as the [!INCLUDE[cc-dyn365-ce-web-services](../includes/cc-dyn365-ce-web-services.md)], reports, search, offline, filtered views, auditing, and duplicate detection.</span><span class="sxs-lookup"><span data-stu-id="e110d-107">It applies to all components, such as the [!INCLUDE[cc-dyn365-ce-web-services](../includes/cc-dyn365-ce-web-services.md)], reports, search, offline, filtered views, auditing, and duplicate detection.</span></span> <span data-ttu-id="e110d-108">For this release, field security can be applied to both custom fields and many out-of-box (OOB) fields.</span><span class="sxs-lookup"><span data-stu-id="e110d-108">For this release, field security can be applied to both custom fields and many out-of-box (OOB) fields.</span></span>  
  
 <span data-ttu-id="e110d-109">For more information about how secured fields change the behavior of methods, see [How Field Security Can Be Used to Control Access to Field Values in Dynamics 365 for Customer Engagement apps](security-dev/use-field-security-control-access-field-values.md).</span><span class="sxs-lookup"><span data-stu-id="e110d-109">For more information about how secured fields change the behavior of methods, see [How Field Security Can Be Used to Control Access to Field Values in Dynamics 365 for Customer Engagement apps](security-dev/use-field-security-control-access-field-values.md).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="e110d-110">Field-level security profiles prevent unintended users from getting access to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] data based on the profile definitions.</span><span class="sxs-lookup"><span data-stu-id="e110d-110">Field-level security profiles prevent unintended users from getting access to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] data based on the profile definitions.</span></span> <span data-ttu-id="e110d-111">If the [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] ACLs are misconfigured, or if there is a SQL injection issue, adversaries can get direct access to data in [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] thereby bypassing field level security restrictions.</span><span class="sxs-lookup"><span data-stu-id="e110d-111">If the [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] ACLs are misconfigured, or if there is a SQL injection issue, adversaries can get direct access to data in [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] thereby bypassing field level security restrictions.</span></span> <span data-ttu-id="e110d-112">For more information, see [Overview of Web Application Security Threats](https://msdn.microsoft.com/library/f13d73y6.aspx).</span><span class="sxs-lookup"><span data-stu-id="e110d-112">For more information, see [Overview of Web Application Security Threats](https://msdn.microsoft.com/library/f13d73y6.aspx).</span></span>  
  
<a name="bkmk_setup"></a>   
## <a name="set-up-and-use-field-security"></a><span data-ttu-id="e110d-113">Set up and use field security</span><span class="sxs-lookup"><span data-stu-id="e110d-113">Set up and use field security</span></span>  
 <span data-ttu-id="e110d-114">To use field security you must do the following:</span><span class="sxs-lookup"><span data-stu-id="e110d-114">To use field security you must do the following:</span></span>  
  
1. <span data-ttu-id="e110d-115">Create a field security profile record</span><span class="sxs-lookup"><span data-stu-id="e110d-115">Create a field security profile record</span></span>  
  
2. <span data-ttu-id="e110d-116">Add users or teams to the profile</span><span class="sxs-lookup"><span data-stu-id="e110d-116">Add users or teams to the profile</span></span>  
  
3. <span data-ttu-id="e110d-117">Find an attribute that can be secured at the field level</span><span class="sxs-lookup"><span data-stu-id="e110d-117">Find an attribute that can be secured at the field level</span></span>  
  
4. <span data-ttu-id="e110d-118">Secure the attribute, either when you create the attribute or by updating the attribute metadata</span><span class="sxs-lookup"><span data-stu-id="e110d-118">Secure the attribute, either when you create the attribute or by updating the attribute metadata</span></span>  
  
5. <span data-ttu-id="e110d-119">Publish the attribute customizations</span><span class="sxs-lookup"><span data-stu-id="e110d-119">Publish the attribute customizations</span></span>  
  
6. <span data-ttu-id="e110d-120">Create a field permission record that defines what access (create, update, read) the profile will have for the custom attribute</span><span class="sxs-lookup"><span data-stu-id="e110d-120">Create a field permission record that defines what access (create, update, read) the profile will have for the custom attribute</span></span>  
  
   <span data-ttu-id="e110d-121">For sample code about how to perform these steps, see [Sample: Enable Field Security For An Entity](sample-enable-field-security-entity.md).</span><span class="sxs-lookup"><span data-stu-id="e110d-121">For sample code about how to perform these steps, see [Sample: Enable Field Security For An Entity](sample-enable-field-security-entity.md).</span></span>  
  
   <span data-ttu-id="e110d-122">Use the following field permission attributes to set whether the specified field security profile can create, read, or update an attribute.</span><span class="sxs-lookup"><span data-stu-id="e110d-122">Use the following field permission attributes to set whether the specified field security profile can create, read, or update an attribute.</span></span> 
   <span data-ttu-id="e110d-123">You can set or compare the value for these attributes by using the `field_security_permission_type` global option set:</span><span class="sxs-lookup"><span data-stu-id="e110d-123">You can set or compare the value for these attributes by using the `field_security_permission_type` global option set:</span></span>  
  
-   <span data-ttu-id="e110d-124">`FieldPermission`.`CanCreate`</span><span class="sxs-lookup"><span data-stu-id="e110d-124">`FieldPermission`.`CanCreate`</span></span>  
  
-   <span data-ttu-id="e110d-125">`FieldPermission`.`CanRead`</span><span class="sxs-lookup"><span data-stu-id="e110d-125">`FieldPermission`.`CanRead`</span></span>  
  
-   <span data-ttu-id="e110d-126">`FieldPermission`.`CanUpdate`</span><span class="sxs-lookup"><span data-stu-id="e110d-126">`FieldPermission`.`CanUpdate`</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="e110d-127">If low privilege users are given Read access to the field security profile entity, they can see what profiles other users have and find other users with access to secured attributes they are interested in.</span><span class="sxs-lookup"><span data-stu-id="e110d-127">If low privilege users are given Read access to the field security profile entity, they can see what profiles other users have and find other users with access to secured attributes they are interested in.</span></span> <span data-ttu-id="e110d-128">They can then use social engineering techniques to get assigned a profile with access to those secured attributes.</span><span class="sxs-lookup"><span data-stu-id="e110d-128">They can then use social engineering techniques to get assigned a profile with access to those secured attributes.</span></span>  
  
<a name="bkmk_whichattributes"></a>   
## <a name="which-attributes-can-be-secured"></a><span data-ttu-id="e110d-129">Which attributes can be secured?</span><span class="sxs-lookup"><span data-stu-id="e110d-129">Which attributes can be secured?</span></span>  
 <span data-ttu-id="e110d-130">To see which attributes can be secured, you can query the entity metadata for the following properties:</span><span class="sxs-lookup"><span data-stu-id="e110d-130">To see which attributes can be secured, you can query the entity metadata for the following properties:</span></span>  
  
- <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.CanBeSecuredForCreate>  
  
- <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.CanBeSecuredForRead>  
  
- <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.CanBeSecuredForUpdate>  
  
  <span data-ttu-id="e110d-131">There are a few additional rules that apply to certain attribute data types:</span><span class="sxs-lookup"><span data-stu-id="e110d-131">There are a few additional rules that apply to certain attribute data types:</span></span>  
  
- <span data-ttu-id="e110d-132">Boolean attributes can be secured for create and update operations but not for read.</span><span class="sxs-lookup"><span data-stu-id="e110d-132">Boolean attributes can be secured for create and update operations but not for read.</span></span>  
  
- <span data-ttu-id="e110d-133">Option set attributes can be secured for create, update, and read when a default value is unspecified.</span><span class="sxs-lookup"><span data-stu-id="e110d-133">Option set attributes can be secured for create, update, and read when a default value is unspecified.</span></span>  
  
  <span data-ttu-id="e110d-134">Có hàng ngàn các thuộc tính có thể được bảo đảm, do đó, có hai cách dễ dàng hơn để tìm kiếm thông tin này.</span><span class="sxs-lookup"><span data-stu-id="e110d-134">There are thousands of attributes that can be secured, so there are two easier ways to look for this information.</span></span> [!INCLUDE[metadata_browser](../includes/metadata-browser.md)]  
  
<a name="bkmk_sharing"></a>   
## <a name="share-secured-fields"></a><span data-ttu-id="e110d-135">Share secured fields</span><span class="sxs-lookup"><span data-stu-id="e110d-135">Share secured fields</span></span>  
 <span data-ttu-id="e110d-136">You can share secured fields much as you can share records.</span><span class="sxs-lookup"><span data-stu-id="e110d-136">You can share secured fields much as you can share records.</span></span> <span data-ttu-id="e110d-137">To do this, you create, update, or delete a `PrincipalObjectAttributeAccess` (field sharing) record, where you specify the user or team, the entity, and the permissions.</span><span class="sxs-lookup"><span data-stu-id="e110d-137">To do this, you create, update, or delete a `PrincipalObjectAttributeAccess` (field sharing) record, where you specify the user or team, the entity, and the permissions.</span></span>  
  
 <span data-ttu-id="e110d-138">The following table lists the corresponding methods for securing a field compared to securing a record.</span><span class="sxs-lookup"><span data-stu-id="e110d-138">The following table lists the corresponding methods for securing a field compared to securing a record.</span></span>  
  
|<span data-ttu-id="e110d-139">Chia sẻ bản ghi</span><span class="sxs-lookup"><span data-stu-id="e110d-139">Record sharing</span></span>|<span data-ttu-id="e110d-140">Field access sharing</span><span class="sxs-lookup"><span data-stu-id="e110d-140">Field access sharing</span></span>|  
|--------------------|--------------------------|  
|<span data-ttu-id="e110d-141">Use the <xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest> message to grant record access for a user or team.</span><span class="sxs-lookup"><span data-stu-id="e110d-141">Use the <xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest> message to grant record access for a user or team.</span></span>|<span data-ttu-id="e110d-142">Use the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message or the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="e110d-142">Use the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message or the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span> <span data-ttu-id="e110d-143">method to grant secured field access for a user or team.</span><span class="sxs-lookup"><span data-stu-id="e110d-143">method to grant secured field access for a user or team.</span></span>|  
|<span data-ttu-id="e110d-144">Use the <xref:Microsoft.Crm.Sdk.Messages.ModifyAccessRequest> message to update record access for a user or team.</span><span class="sxs-lookup"><span data-stu-id="e110d-144">Use the <xref:Microsoft.Crm.Sdk.Messages.ModifyAccessRequest> message to update record access for a user or team.</span></span>|<span data-ttu-id="e110d-145">Use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message or the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span><span class="sxs-lookup"><span data-stu-id="e110d-145">Use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> message or the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span></span> <span data-ttu-id="e110d-146">method to update secured field access for a user or team.</span><span class="sxs-lookup"><span data-stu-id="e110d-146">method to update secured field access for a user or team.</span></span>|  
|<span data-ttu-id="e110d-147">Use the <xref:Microsoft.Crm.Sdk.Messages.RevokeAccessRequest> message to remove record access for a user or team.</span><span class="sxs-lookup"><span data-stu-id="e110d-147">Use the <xref:Microsoft.Crm.Sdk.Messages.RevokeAccessRequest> message to remove record access for a user or team.</span></span>|<span data-ttu-id="e110d-148">Use the <xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest> message or the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span><span class="sxs-lookup"><span data-stu-id="e110d-148">Use the <xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest> message or the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span></span> <span data-ttu-id="e110d-149">method to remove secured field access for a user or team.</span><span class="sxs-lookup"><span data-stu-id="e110d-149">method to remove secured field access for a user or team.</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="e110d-150">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e110d-150">See also</span></span>  
 <span data-ttu-id="e110d-151">[The Security Model of Dynamics 365 for Customer Engagement apps](security-dev/security-model.md) </span><span class="sxs-lookup"><span data-stu-id="e110d-151">[The Security Model of Dynamics 365 for Customer Engagement apps](security-dev/security-model.md) </span></span>  
 <span data-ttu-id="e110d-152">[Administration and security entities](administration-security-entities.md) </span><span class="sxs-lookup"><span data-stu-id="e110d-152">[Administration and security entities](administration-security-entities.md) </span></span>  
 <span data-ttu-id="e110d-153">[FieldSecurityProfile Entity](entities/fieldsecurityprofile.md) </span><span class="sxs-lookup"><span data-stu-id="e110d-153">[FieldSecurityProfile Entity](entities/fieldsecurityprofile.md) </span></span>  
 <span data-ttu-id="e110d-154">[FieldPermission Entity](entities/fieldpermission.md) </span><span class="sxs-lookup"><span data-stu-id="e110d-154">[FieldPermission Entity](entities/fieldpermission.md) </span></span>  
 <span data-ttu-id="e110d-155">[PrincipalObjectAttributeAccess Entity](entities/principalobjectattributeaccess.md) </span><span class="sxs-lookup"><span data-stu-id="e110d-155">[PrincipalObjectAttributeAccess Entity](entities/principalobjectattributeaccess.md) </span></span>  
 <span data-ttu-id="e110d-156">[Field-level data encryption](field-level-data-encryption.md) </span><span class="sxs-lookup"><span data-stu-id="e110d-156">[Field-level data encryption](field-level-data-encryption.md) </span></span>  
 <span data-ttu-id="e110d-157">[Sample: Retrieve Field Permissions](sample-retrieve-field-permissions.md) </span><span class="sxs-lookup"><span data-stu-id="e110d-157">[Sample: Retrieve Field Permissions](sample-retrieve-field-permissions.md) </span></span>  
 <span data-ttu-id="e110d-158">[Sample: Enable Field Security For An Entity](sample-enable-field-security-entity.md) </span><span class="sxs-lookup"><span data-stu-id="e110d-158">[Sample: Enable Field Security For An Entity](sample-enable-field-security-entity.md) </span></span>  
 [<span data-ttu-id="e110d-159">Sample: Retrieve Field Sharing Records</span><span class="sxs-lookup"><span data-stu-id="e110d-159">Sample: Retrieve Field Sharing Records</span></span>](sample-retrieve-field-sharing-records.md)
