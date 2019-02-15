---
title: Use field security to control access to field values (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Provides field-level security to restrict access to high business impact (custom and OOB) fields to specific users and teams.
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
- field-level security in CRM, when aggregating on secured attributes
- field-level security in CRM, explained
- field-level security in CRM, when ordering on secured attributes
- controlling access to field values by using field-level security
- field-level security in CRM, behavior of secured fields when sharing records
- secured fields
- field-level security in CRM, behavior of secured fields for Create or Update
- field-level security in CRM, when grouping on secured attributes
- field-level security in CRM, behavior of secured fields for filtered views or offline synchronization
- using field-level security to control access to field values in CRM
- security roles that allow access to secured fields
- field-level security in CRM, secured attributes in column sets
- field-level security in CRM, secured attributes in the filter condition
ms.assetid: bd42f612-f01c-47dd-9859-69f6024af263
caps.latest.revision: 42
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 409c53c43d670424fbe76e28d982e139ed9fed6e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388327"
---
# <a name="use-field-security-to-control-access-to-field-values"></a><span data-ttu-id="44a98-103">Use field security to control access to field values</span><span class="sxs-lookup"><span data-stu-id="44a98-103">Use field security to control access to field values</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="44a98-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps, you use field-level security to restrict access to high business impact fields to specific users and teams.</span><span class="sxs-lookup"><span data-stu-id="44a98-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps, you use field-level security to restrict access to high business impact fields to specific users and teams.</span></span> <span data-ttu-id="44a98-105">For example, you use this to enable only certain users to read or update the credit score for a customer.</span><span class="sxs-lookup"><span data-stu-id="44a98-105">For example, you use this to enable only certain users to read or update the credit score for a customer.</span></span> <span data-ttu-id="44a98-106">For this release, field-level security can be applied to both custom fields and many out-of-box (OOB) fields.</span><span class="sxs-lookup"><span data-stu-id="44a98-106">For this release, field-level security can be applied to both custom fields and many out-of-box (OOB) fields.</span></span>  
  
 <span data-ttu-id="44a98-107">The following steps describe how to restrict access to a field:</span><span class="sxs-lookup"><span data-stu-id="44a98-107">The following steps describe how to restrict access to a field:</span></span>  
  
1. <span data-ttu-id="44a98-108">Enable field-level security for an attribute</span><span class="sxs-lookup"><span data-stu-id="44a98-108">Enable field-level security for an attribute</span></span>  
  
2. <span data-ttu-id="44a98-109">Create a field-level security profile</span><span class="sxs-lookup"><span data-stu-id="44a98-109">Create a field-level security profile</span></span>  
  
3. <span data-ttu-id="44a98-110">Associate users or teams with the profile</span><span class="sxs-lookup"><span data-stu-id="44a98-110">Associate users or teams with the profile</span></span>  
  
4. <span data-ttu-id="44a98-111">Add specific field permissions, such as Create, Update or Read for a specific attribute to the profile</span><span class="sxs-lookup"><span data-stu-id="44a98-111">Add specific field permissions, such as Create, Update or Read for a specific attribute to the profile</span></span>  
  
   <span data-ttu-id="44a98-112">The following diagram shows the interaction between role-based security, record-based security, and field-level security.</span><span class="sxs-lookup"><span data-stu-id="44a98-112">The following diagram shows the interaction between role-based security, record-based security, and field-level security.</span></span>  
  
   <span data-ttu-id="44a98-113">![Role-based compared to field-level security](../media/crm-v5s-sm-fieldlevelsecurity.png "Role-based compared to field-level security")</span><span class="sxs-lookup"><span data-stu-id="44a98-113">![Role-based compared to field-level security](../media/crm-v5s-sm-fieldlevelsecurity.png "Role-based compared to field-level security")</span></span>  
  
   <span data-ttu-id="44a98-114">Role-based security lets you see a specific entity type, record-based security lets you see individual records, and field-level security lets you see specific fields.</span><span class="sxs-lookup"><span data-stu-id="44a98-114">Role-based security lets you see a specific entity type, record-based security lets you see individual records, and field-level security lets you see specific fields.</span></span>  
  
   [<span data-ttu-id="44a98-115">Video: Field Level Security in Microsoft Dynamics CRM 2015</span><span class="sxs-lookup"><span data-stu-id="44a98-115">Video: Field Level Security in Microsoft Dynamics CRM 2015</span></span>](http://youtu.be/Czc9sKvWd9k)  
  
## <a name="frequently-asked-questions"></a><span data-ttu-id="44a98-116">Câu hỏi thường gặp</span><span class="sxs-lookup"><span data-stu-id="44a98-116">Frequently asked questions</span></span>  
  
-   [<span data-ttu-id="44a98-117">Which attributes can be secured?</span><span class="sxs-lookup"><span data-stu-id="44a98-117">Which attributes can be secured?</span></span>](use-field-security-control-access-field-values.md#bkmk_canbesecured)  
  
-   [<span data-ttu-id="44a98-118">Which security roles allow you to see secured fields?</span><span class="sxs-lookup"><span data-stu-id="44a98-118">Which security roles allow you to see secured fields?</span></span>](use-field-security-control-access-field-values.md#BKMK_SecurityRoles)  
  
-   [<span data-ttu-id="44a98-119">How do secured fields behave for Retrieve and RetrieveMultiple?</span><span class="sxs-lookup"><span data-stu-id="44a98-119">How do secured fields behave for Retrieve and RetrieveMultiple?</span></span>](use-field-security-control-access-field-values.md#BKMK_Retrieve)  
  
-   [<span data-ttu-id="44a98-120">How do secured fields behave for create or update?</span><span class="sxs-lookup"><span data-stu-id="44a98-120">How do secured fields behave for create or update?</span></span>](use-field-security-control-access-field-values.md#BKMK_createAndUpdate)  
  
-   [<span data-ttu-id="44a98-121">How do secured fields behave when records are shared?</span><span class="sxs-lookup"><span data-stu-id="44a98-121">How do secured fields behave when records are shared?</span></span>](use-field-security-control-access-field-values.md#BKMK_Sharing)  
  
-   [<span data-ttu-id="44a98-122">How do secured fields behave for filtered views?</span><span class="sxs-lookup"><span data-stu-id="44a98-122">How do secured fields behave for filtered views?</span></span>](use-field-security-control-access-field-values.md#BKMK_filteredViews)  
  
-   [<span data-ttu-id="44a98-123">How do secured fields behave for offline synchronization?</span><span class="sxs-lookup"><span data-stu-id="44a98-123">How do secured fields behave for offline synchronization?</span></span>](use-field-security-control-access-field-values.md#BKMK_OfflineSync)  
  
<a name="bkmk_canbesecured"></a>   
## <a name="which-attributes-can-be-secured"></a><span data-ttu-id="44a98-124">Which attributes can be secured?</span><span class="sxs-lookup"><span data-stu-id="44a98-124">Which attributes can be secured?</span></span>  
 <span data-ttu-id="44a98-125">To see which attributes can be secured, you can query the entity metadata for the following properties:</span><span class="sxs-lookup"><span data-stu-id="44a98-125">To see which attributes can be secured, you can query the entity metadata for the following properties:</span></span>  
  
- <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.CanBeSecuredForCreate>  
  
- <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.CanBeSecuredForRead>  
  
- <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.CanBeSecuredForUpdate>  
  
  <span data-ttu-id="44a98-126">There are thousands of attributes that can be secured, so there are two easier ways to look for this information.</span><span class="sxs-lookup"><span data-stu-id="44a98-126">There are thousands of attributes that can be secured, so there are two easier ways to look for this information.</span></span> [!INCLUDE[metadata_browser](../../includes/metadata-browser.md)]  
  
  <span data-ttu-id="44a98-127">There are a few additional rules that apply to certain attribute data types:</span><span class="sxs-lookup"><span data-stu-id="44a98-127">There are a few additional rules that apply to certain attribute data types:</span></span>  
  
- <span data-ttu-id="44a98-128">Boolean attributes can be secured for create and update operations but not for read.</span><span class="sxs-lookup"><span data-stu-id="44a98-128">Boolean attributes can be secured for create and update operations but not for read.</span></span>  
  
- <span data-ttu-id="44a98-129">Option set attributes can be secured for create, update, and read when a default value is unspecified.</span><span class="sxs-lookup"><span data-stu-id="44a98-129">Option set attributes can be secured for create, update, and read when a default value is unspecified.</span></span>  
  
<a name="BKMK_SecurityRoles"></a>   
## <a name="which-security-roles-allow-you-to-see-secured-fields"></a><span data-ttu-id="44a98-130">Which security roles allow you to see secured fields?</span><span class="sxs-lookup"><span data-stu-id="44a98-130">Which security roles allow you to see secured fields?</span></span>  
 <span data-ttu-id="44a98-131">The System Administrator field security profile gives full access to all secured fields in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)].</span><span class="sxs-lookup"><span data-stu-id="44a98-131">The System Administrator field security profile gives full access to all secured fields in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)].</span></span>  <span data-ttu-id="44a98-132">By default, all users who have the System Administrator security role have this profile.</span><span class="sxs-lookup"><span data-stu-id="44a98-132">By default, all users who have the System Administrator security role have this profile.</span></span> <span data-ttu-id="44a98-133">This profile is system managed and can’t be updated or deleted.</span><span class="sxs-lookup"><span data-stu-id="44a98-133">This profile is system managed and can’t be updated or deleted.</span></span>  
  
<a name="BKMK_Retrieve"></a>   
## <a name="how-do-secured-fields-behave-for-retrieve-and-retrievemultiple"></a><span data-ttu-id="44a98-134">How do secured fields behave for Retrieve and RetrieveMultiple?</span><span class="sxs-lookup"><span data-stu-id="44a98-134">How do secured fields behave for Retrieve and RetrieveMultiple?</span></span>  
 <span data-ttu-id="44a98-135">When you call the `Retrieve` or `RetrieveMultiple` methods or messages, [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] evaluates if the caller and the impersonated user have access to each retrieved record (this is the regular security process) and each secured field.</span><span class="sxs-lookup"><span data-stu-id="44a98-135">When you call the `Retrieve` or `RetrieveMultiple` methods or messages, [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] evaluates if the caller and the impersonated user have access to each retrieved record (this is the regular security process) and each secured field.</span></span> <span data-ttu-id="44a98-136">The call does not throw an exception if the criteria contain secured fields for which the caller does not have access.</span><span class="sxs-lookup"><span data-stu-id="44a98-136">The call does not throw an exception if the criteria contain secured fields for which the caller does not have access.</span></span> <span data-ttu-id="44a98-137">Instead, null values are returned for secured fields if they are part of the output column set.</span><span class="sxs-lookup"><span data-stu-id="44a98-137">Instead, null values are returned for secured fields if they are part of the output column set.</span></span>  
  
 <span data-ttu-id="44a98-138">The following describes more about the retrieve multiple behaviors for secured fields.</span><span class="sxs-lookup"><span data-stu-id="44a98-138">The following describes more about the retrieve multiple behaviors for secured fields.</span></span>  
  
### <a name="when-a-secured-attribute-is-in-the-column-set"></a><span data-ttu-id="44a98-139">When a secured attribute is in the column set</span><span class="sxs-lookup"><span data-stu-id="44a98-139">When a secured attribute is in the column set</span></span>  
 <span data-ttu-id="44a98-140">If the caller (or impersonated user) does not have read access to the secured fields that are included in a column set, the value returns as **null**.</span><span class="sxs-lookup"><span data-stu-id="44a98-140">If the caller (or impersonated user) does not have read access to the secured fields that are included in a column set, the value returns as **null**.</span></span> <span data-ttu-id="44a98-141">You cannot tell the difference between a returned **null** value caused by no data or caused by insufficient access.</span><span class="sxs-lookup"><span data-stu-id="44a98-141">You cannot tell the difference between a returned **null** value caused by no data or caused by insufficient access.</span></span>  
  
### <a name="when-a-secured-attribute-is-in-the-filter-condition"></a><span data-ttu-id="44a98-142">When a secured attribute is in the filter condition</span><span class="sxs-lookup"><span data-stu-id="44a98-142">When a secured attribute is in the filter condition</span></span>  
 <span data-ttu-id="44a98-143">If the caller (or impersonated user) does not have access to the secured fields that are included in the filter criteria, the field value is substituted with **null** during the evaluation of the filter.</span><span class="sxs-lookup"><span data-stu-id="44a98-143">If the caller (or impersonated user) does not have access to the secured fields that are included in the filter criteria, the field value is substituted with **null** during the evaluation of the filter.</span></span>  
  
 <span data-ttu-id="44a98-144">In the following table, the caller has access to all attributes except those indicated with an asterisk (\*).</span><span class="sxs-lookup"><span data-stu-id="44a98-144">In the following table, the caller has access to all attributes except those indicated with an asterisk (\*).</span></span>  
  
|<span data-ttu-id="44a98-145">Record Number</span><span class="sxs-lookup"><span data-stu-id="44a98-145">Record Number</span></span>|<span data-ttu-id="44a98-146">Value of the Name attribute</span><span class="sxs-lookup"><span data-stu-id="44a98-146">Value of the Name attribute</span></span>|<span data-ttu-id="44a98-147">Value of the Description attribute</span><span class="sxs-lookup"><span data-stu-id="44a98-147">Value of the Description attribute</span></span>|<span data-ttu-id="44a98-148">Value of the Can Be Contacted attribute</span><span class="sxs-lookup"><span data-stu-id="44a98-148">Value of the Can Be Contacted attribute</span></span>|  
|-------------------|---------------------------------|----------------------------------------|---------------------------------------------|  
|<span data-ttu-id="44a98-149">1</span><span class="sxs-lookup"><span data-stu-id="44a98-149">1</span></span>|<span data-ttu-id="44a98-150">A</span><span class="sxs-lookup"><span data-stu-id="44a98-150">A</span></span>|<span data-ttu-id="44a98-151">AAA</span><span class="sxs-lookup"><span data-stu-id="44a98-151">AAA</span></span>|<span data-ttu-id="44a98-152">Đúng</span><span class="sxs-lookup"><span data-stu-id="44a98-152">True</span></span>|  
|<span data-ttu-id="44a98-153">2</span><span class="sxs-lookup"><span data-stu-id="44a98-153">2</span></span>|<span data-ttu-id="44a98-154">B</span><span class="sxs-lookup"><span data-stu-id="44a98-154">B</span></span>|<span data-ttu-id="44a98-155">BBB</span><span class="sxs-lookup"><span data-stu-id="44a98-155">BBB</span></span>|<span data-ttu-id="44a98-156">Sai</span><span class="sxs-lookup"><span data-stu-id="44a98-156">False</span></span>|  
|<span data-ttu-id="44a98-157">3</span><span class="sxs-lookup"><span data-stu-id="44a98-157">3</span></span>|<span data-ttu-id="44a98-158">C</span><span class="sxs-lookup"><span data-stu-id="44a98-158">C</span></span>|<span data-ttu-id="44a98-159">CCC</span><span class="sxs-lookup"><span data-stu-id="44a98-159">CCC</span></span>|<span data-ttu-id="44a98-160">**True** <sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-160">**True** <sup>\*</sup></span></span>|  
|<span data-ttu-id="44a98-161">4</span><span class="sxs-lookup"><span data-stu-id="44a98-161">4</span></span>|<span data-ttu-id="44a98-162">D</span><span class="sxs-lookup"><span data-stu-id="44a98-162">D</span></span>|<span data-ttu-id="44a98-163">DDD</span><span class="sxs-lookup"><span data-stu-id="44a98-163">DDD</span></span>|<span data-ttu-id="44a98-164">Rỗng</span><span class="sxs-lookup"><span data-stu-id="44a98-164">Null</span></span>|  
|<span data-ttu-id="44a98-165">*5* <sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-165">*5* <sup>\*</sup></span></span>|<span data-ttu-id="44a98-166">*E* <sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-166">*E* <sup>\*</sup></span></span>|<span data-ttu-id="44a98-167">*EEE* <sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-167">*EEE* <sup>\*</sup></span></span>|<span data-ttu-id="44a98-168">*Null* <sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-168">*Null* <sup>\*</sup></span></span>|  
  
 <span data-ttu-id="44a98-169">When the filter is `CanbeContacted == True`, only record one is returned.</span><span class="sxs-lookup"><span data-stu-id="44a98-169">When the filter is `CanbeContacted == True`, only record one is returned.</span></span>  
  
 <span data-ttu-id="44a98-170">When the filter is `IsNULL` (CanbeContacted), records 3 and 4 are returned.</span><span class="sxs-lookup"><span data-stu-id="44a98-170">When the filter is `IsNULL` (CanbeContacted), records 3 and 4 are returned.</span></span> <span data-ttu-id="44a98-171">Since record 3 is hidden from the user, it is treated as **null** during condition evaluation and will be evaluated as `True` for `ISNull`.</span><span class="sxs-lookup"><span data-stu-id="44a98-171">Since record 3 is hidden from the user, it is treated as **null** during condition evaluation and will be evaluated as `True` for `ISNull`.</span></span>  
  
### <a name="when-aggregating-on-secured-attributes"></a><span data-ttu-id="44a98-172">When aggregating on secured attributes</span><span class="sxs-lookup"><span data-stu-id="44a98-172">When aggregating on secured attributes</span></span>  
 <span data-ttu-id="44a98-173">Secured values are substituted with a null value, so normal SQL aggregation behavior applies.</span><span class="sxs-lookup"><span data-stu-id="44a98-173">Secured values are substituted with a null value, so normal SQL aggregation behavior applies.</span></span>  
  
### <a name="when-grouping-on-secured-attributes"></a><span data-ttu-id="44a98-174">When grouping on secured attributes</span><span class="sxs-lookup"><span data-stu-id="44a98-174">When grouping on secured attributes</span></span>  
 <span data-ttu-id="44a98-175">If the caller (or impersonated user) does not have access to the attribute used for grouping, the value is treated as **null** and the results are grouped together with all **null** values.</span><span class="sxs-lookup"><span data-stu-id="44a98-175">If the caller (or impersonated user) does not have access to the attribute used for grouping, the value is treated as **null** and the results are grouped together with all **null** values.</span></span>  
  
 <span data-ttu-id="44a98-176">In the following example, the caller has access to some attributes.</span><span class="sxs-lookup"><span data-stu-id="44a98-176">In the following example, the caller has access to some attributes.</span></span> <span data-ttu-id="44a98-177">**Bold** indicates no access to attributes, also indicated with <em>. \*Italics</em> indicate a record for which the caller does not have read access, also indicated with \*\*.</span><span class="sxs-lookup"><span data-stu-id="44a98-177">**Bold** indicates no access to attributes, also indicated with <em>. \*Italics</em> indicate a record for which the caller does not have read access, also indicated with \*\*.</span></span>  
  
|<span data-ttu-id="44a98-178">Tên</span><span class="sxs-lookup"><span data-stu-id="44a98-178">Name</span></span>|<span data-ttu-id="44a98-179">Mô tả</span><span class="sxs-lookup"><span data-stu-id="44a98-179">Description</span></span>|<span data-ttu-id="44a98-180">Number of orders</span><span class="sxs-lookup"><span data-stu-id="44a98-180">Number of orders</span></span>|<span data-ttu-id="44a98-181">Tiểu bang</span><span class="sxs-lookup"><span data-stu-id="44a98-181">State</span></span>|  
|----------|-----------------|----------------------|-----------|  
|<span data-ttu-id="44a98-182">A</span><span class="sxs-lookup"><span data-stu-id="44a98-182">A</span></span>|<span data-ttu-id="44a98-183">AAA</span><span class="sxs-lookup"><span data-stu-id="44a98-183">AAA</span></span>|<span data-ttu-id="44a98-184">1</span><span class="sxs-lookup"><span data-stu-id="44a98-184">1</span></span>|<span data-ttu-id="44a98-185">WA</span><span class="sxs-lookup"><span data-stu-id="44a98-185">WA</span></span>|  
|<span data-ttu-id="44a98-186">B</span><span class="sxs-lookup"><span data-stu-id="44a98-186">B</span></span>|<span data-ttu-id="44a98-187">BBB</span><span class="sxs-lookup"><span data-stu-id="44a98-187">BBB</span></span>|<span data-ttu-id="44a98-188">4</span><span class="sxs-lookup"><span data-stu-id="44a98-188">4</span></span>|<span data-ttu-id="44a98-189">WA</span><span class="sxs-lookup"><span data-stu-id="44a98-189">WA</span></span>|  
|<span data-ttu-id="44a98-190">C</span><span class="sxs-lookup"><span data-stu-id="44a98-190">C</span></span>|<span data-ttu-id="44a98-191">CCC</span><span class="sxs-lookup"><span data-stu-id="44a98-191">CCC</span></span>|<span data-ttu-id="44a98-192">4</span><span class="sxs-lookup"><span data-stu-id="44a98-192">4</span></span>|<span data-ttu-id="44a98-193">CA</span><span class="sxs-lookup"><span data-stu-id="44a98-193">CA</span></span>|  
|<span data-ttu-id="44a98-194">*D* <sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-194">*D* <sup>\*\*</sup></span></span>|<span data-ttu-id="44a98-195">*DDD* <sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-195">*DDD* <sup>\*\*</sup></span></span>|<span data-ttu-id="44a98-196">*3* <sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-196">*3* <sup>\*\*</sup></span></span>|<span data-ttu-id="44a98-197">*MA* <sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-197">*MA* <sup>\*\*</sup></span></span>|  
|<span data-ttu-id="44a98-198">E</span><span class="sxs-lookup"><span data-stu-id="44a98-198">E</span></span>|<span data-ttu-id="44a98-199">EEE</span><span class="sxs-lookup"><span data-stu-id="44a98-199">EEE</span></span>|<span data-ttu-id="44a98-200">0</span><span class="sxs-lookup"><span data-stu-id="44a98-200">0</span></span>|<span data-ttu-id="44a98-201">CA</span><span class="sxs-lookup"><span data-stu-id="44a98-201">CA</span></span>|  
|<span data-ttu-id="44a98-202">F</span><span class="sxs-lookup"><span data-stu-id="44a98-202">F</span></span>|<span data-ttu-id="44a98-203">FFF</span><span class="sxs-lookup"><span data-stu-id="44a98-203">FFF</span></span>|<span data-ttu-id="44a98-204">0</span><span class="sxs-lookup"><span data-stu-id="44a98-204">0</span></span>|<span data-ttu-id="44a98-205">**WA** <sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-205">**WA** <sup>\*</sup></span></span>|  
|<span data-ttu-id="44a98-206">G</span><span class="sxs-lookup"><span data-stu-id="44a98-206">G</span></span>|<span data-ttu-id="44a98-207">GGG</span><span class="sxs-lookup"><span data-stu-id="44a98-207">GGG</span></span>|<span data-ttu-id="44a98-208">2</span><span class="sxs-lookup"><span data-stu-id="44a98-208">2</span></span>|<span data-ttu-id="44a98-209">**CA** <sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-209">**CA** <sup>\*</sup></span></span>|  
  
 <span data-ttu-id="44a98-210">`Select State, Total(orders) Group by (STATE)` results in the following:</span><span class="sxs-lookup"><span data-stu-id="44a98-210">`Select State, Total(orders) Group by (STATE)` results in the following:</span></span>  
  
 <span data-ttu-id="44a98-211">WA–5</span><span class="sxs-lookup"><span data-stu-id="44a98-211">WA–5</span></span>  
  
 <span data-ttu-id="44a98-212">CA–4</span><span class="sxs-lookup"><span data-stu-id="44a98-212">CA–4</span></span>  
  
 <span data-ttu-id="44a98-213">**null**–2</span><span class="sxs-lookup"><span data-stu-id="44a98-213">**null**–2</span></span>  
  
### <a name="when-ordering-on-secured-attributes"></a><span data-ttu-id="44a98-214">When ordering on secured attributes</span><span class="sxs-lookup"><span data-stu-id="44a98-214">When ordering on secured attributes</span></span>  
 <span data-ttu-id="44a98-215">If the caller (or impersonated user) does not have access to secured fields that are included in an order by condition, the values will be treated as if they are **null**.</span><span class="sxs-lookup"><span data-stu-id="44a98-215">If the caller (or impersonated user) does not have access to secured fields that are included in an order by condition, the values will be treated as if they are **null**.</span></span>  
  
 <span data-ttu-id="44a98-216">In the following example, the caller has access to attributes that are in plain text.</span><span class="sxs-lookup"><span data-stu-id="44a98-216">In the following example, the caller has access to attributes that are in plain text.</span></span> <span data-ttu-id="44a98-217">**Bold** indicates no access to attributes, also indicated with an asterisk (<em>). \*Italics</em> indicate a record for which the caller does not have read access, also indicated with \*\*.</span><span class="sxs-lookup"><span data-stu-id="44a98-217">**Bold** indicates no access to attributes, also indicated with an asterisk (<em>). \*Italics</em> indicate a record for which the caller does not have read access, also indicated with \*\*.</span></span>  
  
|<span data-ttu-id="44a98-218">Tên</span><span class="sxs-lookup"><span data-stu-id="44a98-218">Name</span></span>|<span data-ttu-id="44a98-219">Mô tả</span><span class="sxs-lookup"><span data-stu-id="44a98-219">Description</span></span>|<span data-ttu-id="44a98-220">CanbeContacted</span><span class="sxs-lookup"><span data-stu-id="44a98-220">CanbeContacted</span></span>|  
|----------|-----------------|--------------------|  
|<span data-ttu-id="44a98-221">A</span><span class="sxs-lookup"><span data-stu-id="44a98-221">A</span></span>|<span data-ttu-id="44a98-222">AAA</span><span class="sxs-lookup"><span data-stu-id="44a98-222">AAA</span></span>|<span data-ttu-id="44a98-223">Đúng</span><span class="sxs-lookup"><span data-stu-id="44a98-223">True</span></span>|  
|<span data-ttu-id="44a98-224">B</span><span class="sxs-lookup"><span data-stu-id="44a98-224">B</span></span>|<span data-ttu-id="44a98-225">BBB</span><span class="sxs-lookup"><span data-stu-id="44a98-225">BBB</span></span>|<span data-ttu-id="44a98-226">Sai</span><span class="sxs-lookup"><span data-stu-id="44a98-226">False</span></span>|  
|<span data-ttu-id="44a98-227">C</span><span class="sxs-lookup"><span data-stu-id="44a98-227">C</span></span>|<span data-ttu-id="44a98-228">**CCC** <sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-228">**CCC** <sup>\*</sup></span></span>|<span data-ttu-id="44a98-229">**True** <sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-229">**True** <sup>\*</sup></span></span>|  
|<span data-ttu-id="44a98-230">D</span><span class="sxs-lookup"><span data-stu-id="44a98-230">D</span></span>|<span data-ttu-id="44a98-231">DDD</span><span class="sxs-lookup"><span data-stu-id="44a98-231">DDD</span></span>|<span data-ttu-id="44a98-232">Rỗng</span><span class="sxs-lookup"><span data-stu-id="44a98-232">Null</span></span>|  
|<span data-ttu-id="44a98-233">E</span><span class="sxs-lookup"><span data-stu-id="44a98-233">E</span></span>|<span data-ttu-id="44a98-234">**EEE** <sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-234">**EEE** <sup>\*</sup></span></span>|<span data-ttu-id="44a98-235">**Null** <sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-235">**Null** <sup>\*</sup></span></span>|  
|<span data-ttu-id="44a98-236">*F* <sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-236">*F* <sup>\*\*</sup></span></span>|<span data-ttu-id="44a98-237">*FFF* <sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-237">*FFF* <sup>\*\*</sup></span></span>|<span data-ttu-id="44a98-238">*True* <sup>\*\*</sup></span><span class="sxs-lookup"><span data-stu-id="44a98-238">*True* <sup>\*\*</sup></span></span>|  
|<span data-ttu-id="44a98-239">G</span><span class="sxs-lookup"><span data-stu-id="44a98-239">G</span></span>|<span data-ttu-id="44a98-240">Rỗng</span><span class="sxs-lookup"><span data-stu-id="44a98-240">Null</span></span>|<span data-ttu-id="44a98-241">Đúng</span><span class="sxs-lookup"><span data-stu-id="44a98-241">True</span></span>|  
  
 <span data-ttu-id="44a98-242">`Select Name order by Description ascending` results in the following:</span><span class="sxs-lookup"><span data-stu-id="44a98-242">`Select Name order by Description ascending` results in the following:</span></span>  
  
 <span data-ttu-id="44a98-243">{G,E,C},A, B, D, will be returned.</span><span class="sxs-lookup"><span data-stu-id="44a98-243">{G,E,C},A, B, D, will be returned.</span></span>  
  
<a name="BKMK_createAndUpdate"></a>   
## <a name="how-do-secured-fields-behave-for-create-or-update"></a><span data-ttu-id="44a98-244">How do secured fields behave for create or update?</span><span class="sxs-lookup"><span data-stu-id="44a98-244">How do secured fields behave for create or update?</span></span>  
 <span data-ttu-id="44a98-245">A programmer may build a client that uses `Create` and `Update` methods that interact with secured fields.</span><span class="sxs-lookup"><span data-stu-id="44a98-245">A programmer may build a client that uses `Create` and `Update` methods that interact with secured fields.</span></span> <span data-ttu-id="44a98-246">When you call the `Create` or `Update` method, passing data for secured fields and the caller does not have sufficient permissions, an exception is thrown.</span><span class="sxs-lookup"><span data-stu-id="44a98-246">When you call the `Create` or `Update` method, passing data for secured fields and the caller does not have sufficient permissions, an exception is thrown.</span></span>  
  
<a name="BKMK_Sharing"></a>   
## <a name="how-do-secured-fields-behave-when-records-are-shared"></a><span data-ttu-id="44a98-247">How do secured fields behave when records are shared?</span><span class="sxs-lookup"><span data-stu-id="44a98-247">How do secured fields behave when records are shared?</span></span>  
 <span data-ttu-id="44a98-248">A user with access to a secured field in a record can share it with another user or team.</span><span class="sxs-lookup"><span data-stu-id="44a98-248">A user with access to a secured field in a record can share it with another user or team.</span></span> <span data-ttu-id="44a98-249">The user can only give the access that they have on the record.</span><span class="sxs-lookup"><span data-stu-id="44a98-249">The user can only give the access that they have on the record.</span></span> <span data-ttu-id="44a98-250">For example, to share the record and grant Update privileges, the user must have update privileges.</span><span class="sxs-lookup"><span data-stu-id="44a98-250">For example, to share the record and grant Update privileges, the user must have update privileges.</span></span>  
  
 <span data-ttu-id="44a98-251">You can share a secured field on a particular record with Read and/or Update with a security principal (user or team).</span><span class="sxs-lookup"><span data-stu-id="44a98-251">You can share a secured field on a particular record with Read and/or Update with a security principal (user or team).</span></span>  <span data-ttu-id="44a98-252">The user or team members with whom the record was shared now have that type of secured field access **only** on the shared secured fields on **only** that particular record, even if the user or team member to whom it was shared does not have a field security profile that gives them access.</span><span class="sxs-lookup"><span data-stu-id="44a98-252">The user or team members with whom the record was shared now have that type of secured field access **only** on the shared secured fields on **only** that particular record, even if the user or team member to whom it was shared does not have a field security profile that gives them access.</span></span>  
  
<a name="BKMK_filteredViews"></a>   
## <a name="how-do-secured-fields-behave-for-filtered-views"></a><span data-ttu-id="44a98-253">How do secured fields behave for filtered views?</span><span class="sxs-lookup"><span data-stu-id="44a98-253">How do secured fields behave for filtered views?</span></span>  
 <span data-ttu-id="44a98-254">An administrator secures a number of fields for access in the application and wants the fields not to be available in reports.</span><span class="sxs-lookup"><span data-stu-id="44a98-254">An administrator secures a number of fields for access in the application and wants the fields not to be available in reports.</span></span> <span data-ttu-id="44a98-255">This allows for maintaining the same set of reports for all users.</span><span class="sxs-lookup"><span data-stu-id="44a98-255">This allows for maintaining the same set of reports for all users.</span></span> <span data-ttu-id="44a98-256">Filtered views will not return data for the secured fields if the calling user does not have authorization for the fields.</span><span class="sxs-lookup"><span data-stu-id="44a98-256">Filtered views will not return data for the secured fields if the calling user does not have authorization for the fields.</span></span> <span data-ttu-id="44a98-257">When no field security is applied for any of the view’s attributes, the filtered views return complete data.</span><span class="sxs-lookup"><span data-stu-id="44a98-257">When no field security is applied for any of the view’s attributes, the filtered views return complete data.</span></span>  
  
<a name="BKMK_OfflineSync"></a>   
## <a name="how-do-secured-fields-behave-for-offline-synchronization"></a><span data-ttu-id="44a98-258">How do secured fields behave for offline synchronization?</span><span class="sxs-lookup"><span data-stu-id="44a98-258">How do secured fields behave for offline synchronization?</span></span>  
 <span data-ttu-id="44a98-259">If you are using [!INCLUDE[pn_crm_outlook_offline_access](../../includes/pn-crm-outlook-offline-access.md)], only the secured field values that you have access to replicate into the offline database.</span><span class="sxs-lookup"><span data-stu-id="44a98-259">If you are using [!INCLUDE[pn_crm_outlook_offline_access](../../includes/pn-crm-outlook-offline-access.md)], only the secured field values that you have access to replicate into the offline database.</span></span> <span data-ttu-id="44a98-260">If you don’t have access to the data, it is not saved offline.</span><span class="sxs-lookup"><span data-stu-id="44a98-260">If you don’t have access to the data, it is not saved offline.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="44a98-261">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="44a98-261">See also</span></span>  
 <span data-ttu-id="44a98-262">[Video: Field Level Security in Microsoft Dynamics CRM 2015](http://youtu.be/Czc9sKvWd9k) </span><span class="sxs-lookup"><span data-stu-id="44a98-262">[Video: Field Level Security in Microsoft Dynamics CRM 2015](http://youtu.be/Czc9sKvWd9k) </span></span>  
 <span data-ttu-id="44a98-263">[The Security Model of Microsoft Dynamics 365 for Customer Engagement](security-model.md) </span><span class="sxs-lookup"><span data-stu-id="44a98-263">[The Security Model of Microsoft Dynamics 365 for Customer Engagement](security-model.md) </span></span>  
 <span data-ttu-id="44a98-264">[Cách sử dụng bảo mật dựa trên vai trò để kiểm soát quyền truy cập vào các thực thể trong Microsoft Dynamics 365 for Customer Engagement](how-role-based-security-control-access-entities.md) </span><span class="sxs-lookup"><span data-stu-id="44a98-264">[How role-based security can be used to control access to entities in Microsoft Dynamics 365 for Customer Engagement](how-role-based-security-control-access-entities.md) </span></span>  
 [<span data-ttu-id="44a98-265">Use record-based security to control access to records</span><span class="sxs-lookup"><span data-stu-id="44a98-265">Use record-based security to control access to records</span></span>](use-record-based-security-control-access-records.md)
