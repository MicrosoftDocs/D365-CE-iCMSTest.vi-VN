---
title: Define ribbon enable rules (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'Learn about defining specific rules to control when the ribbon elements are enabled during configuration of ribbon elements. '
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
- ribbon, enable controls
ms.assetid: f17819f8-e963-43e1-8895-36bf0cc32b0f
caps.latest.revision: 27
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2bb7178d113365fe108bb9cf77cb6930b757178a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385538"
---
# <a name="define-ribbon-enable-rules"></a><span data-ttu-id="029e4-103">Define ribbon enable rules</span><span class="sxs-lookup"><span data-stu-id="029e4-103">Define ribbon enable rules</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="029e4-104">When configuring Ribbon elements you can define specific rules to control when the ribbon elements are enabled.</span><span class="sxs-lookup"><span data-stu-id="029e4-104">When configuring Ribbon elements you can define specific rules to control when the ribbon elements are enabled.</span></span> <span data-ttu-id="029e4-105">The `<EnableRule>` element is used as follows:</span><span class="sxs-lookup"><span data-stu-id="029e4-105">The `<EnableRule>` element is used as follows:</span></span>  

-   <span data-ttu-id="029e4-106">Use the `/RuleDefinitions/EnableRules/EnableRule` element to define rules controlling when the ribbon element should be enabled.</span><span class="sxs-lookup"><span data-stu-id="029e4-106">Use the `/RuleDefinitions/EnableRules/EnableRule` element to define rules controlling when the ribbon element should be enabled.</span></span>  

-   <span data-ttu-id="029e4-107">Use the `/CommandDefinitions/CommandDefinition/EnableRules/EnableRule` element to associate specific enable rules to a command definition.</span><span class="sxs-lookup"><span data-stu-id="029e4-107">Use the `/CommandDefinitions/CommandDefinition/EnableRules/EnableRule` element to associate specific enable rules to a command definition.</span></span>  

## <a name="what-does-enabled-mean"></a><span data-ttu-id="029e4-108">What does enabled mean?</span><span class="sxs-lookup"><span data-stu-id="029e4-108">What does enabled mean?</span></span>  
 <span data-ttu-id="029e4-109">With the command bar, commands that are disabled are hidden.</span><span class="sxs-lookup"><span data-stu-id="029e4-109">With the command bar, commands that are disabled are hidden.</span></span> <span data-ttu-id="029e4-110">With the ribbon, commands that are disabled are visible but do not respond to events.</span><span class="sxs-lookup"><span data-stu-id="029e4-110">With the ribbon, commands that are disabled are visible but do not respond to events.</span></span>  

## <a name="control-when-ribbon-elements-are-enabled"></a><span data-ttu-id="029e4-111">Control when ribbon elements are enabled</span><span class="sxs-lookup"><span data-stu-id="029e4-111">Control when ribbon elements are enabled</span></span>  
 <span data-ttu-id="029e4-112">Enable rules are intended to be re-used.</span><span class="sxs-lookup"><span data-stu-id="029e4-112">Enable rules are intended to be re-used.</span></span> <span data-ttu-id="029e4-113">By defining them with rule definitions, you can use the same enable rule for many command definitions.</span><span class="sxs-lookup"><span data-stu-id="029e4-113">By defining them with rule definitions, you can use the same enable rule for many command definitions.</span></span> <span data-ttu-id="029e4-114">When more than one enable rule is defined for a command definition, all of the enable rules must evaluate as true for the ribbon element to be enabled.</span><span class="sxs-lookup"><span data-stu-id="029e4-114">When more than one enable rule is defined for a command definition, all of the enable rules must evaluate as true for the ribbon element to be enabled.</span></span>  

 <span data-ttu-id="029e4-115">All Enable rules provide an optional attribute to specify whether the default value of the rule is true or false and an optional `InvertResult` attribute to allow for returning a negative result when the item being tested returns true.</span><span class="sxs-lookup"><span data-stu-id="029e4-115">All Enable rules provide an optional attribute to specify whether the default value of the rule is true or false and an optional `InvertResult` attribute to allow for returning a negative result when the item being tested returns true.</span></span>  

 <span data-ttu-id="029e4-116">The `/RuleDefinitions/EnableRules/EnableRule` element supports the following types of rules:</span><span class="sxs-lookup"><span data-stu-id="029e4-116">The `/RuleDefinitions/EnableRules/EnableRule` element supports the following types of rules:</span></span>  

### <a name="command-client-type-rule"></a><span data-ttu-id="029e4-117">Command Client Type Rule</span><span class="sxs-lookup"><span data-stu-id="029e4-117">Command Client Type Rule</span></span>
 <span data-ttu-id="029e4-118">Uses the `<CommandClientTypeRule>` element.</span><span class="sxs-lookup"><span data-stu-id="029e4-118">Uses the `<CommandClientTypeRule>` element.</span></span> [!INCLUDE[ribbon_element_CommandClientTypeRule](../../includes/ribbon-element-commandclienttyperule.md)]  

 <span data-ttu-id="029e4-119">The `Type` values correspond to the following:</span><span class="sxs-lookup"><span data-stu-id="029e4-119">The `Type` values correspond to the following:</span></span>  


|   <span data-ttu-id="029e4-120">Value</span><span class="sxs-lookup"><span data-stu-id="029e4-120">Value</span></span>   |                                                                               <span data-ttu-id="029e4-121">Bản trình bày</span><span class="sxs-lookup"><span data-stu-id="029e4-121">Presentation</span></span>                                                                               |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Modern`  |                                       <span data-ttu-id="029e4-122">The command bar is presented using [!INCLUDE[pn_moca_full](../../includes/pn-moca-full.md)].</span><span class="sxs-lookup"><span data-stu-id="029e4-122">The command bar is presented using [!INCLUDE[pn_moca_full](../../includes/pn-moca-full.md)].</span></span>                                       |
| `Refresh` |                                                      <span data-ttu-id="029e4-123">The command bar is presented using the updated user interface.</span><span class="sxs-lookup"><span data-stu-id="029e4-123">The command bar is presented using the updated user interface.</span></span>                                                      |
| `Legacy`  | <span data-ttu-id="029e4-124">The ribbon is presented in forms for entities that were not updated or in a list view in [!INCLUDE[pn_crm_for_outlook_full](../../includes/pn-crm-for-outlook-full.md)].</span><span class="sxs-lookup"><span data-stu-id="029e4-124">The ribbon is presented in forms for entities that were not updated or in a list view in [!INCLUDE[pn_crm_for_outlook_full](../../includes/pn-crm-for-outlook-full.md)].</span></span> |

### <a name="crm-client-type-rule"></a><span data-ttu-id="029e4-125">Crm Client Type Rule</span><span class="sxs-lookup"><span data-stu-id="029e4-125">Crm Client Type Rule</span></span>
<span data-ttu-id="029e4-126">Uses the  `<CrmClientTypeRule>` element to allow definition of rules depending on the type of client used.</span><span class="sxs-lookup"><span data-stu-id="029e4-126">Uses the  `<CrmClientTypeRule>` element to allow definition of rules depending on the type of client used.</span></span> <span data-ttu-id="029e4-127">Type options are as follows:</span><span class="sxs-lookup"><span data-stu-id="029e4-127">Type options are as follows:</span></span>  

-   `Web`  

-   `Outlook`  

### <a name="crm-offline-access-state-rule"></a><span data-ttu-id="029e4-128">Crm Offline Access State Rule</span><span class="sxs-lookup"><span data-stu-id="029e4-128">Crm Offline Access State Rule</span></span>
 <span data-ttu-id="029e4-129">Uses the `<CrmOfflineAccessStateRule>` element.</span><span class="sxs-lookup"><span data-stu-id="029e4-129">Uses the `<CrmOfflineAccessStateRule>` element.</span></span> <span data-ttu-id="029e4-130">Use this criteria to enable a ribbon element based on whether [!INCLUDE[pn_crm_outlook_offline_access](../../includes/pn-crm-outlook-offline-access.md)] is currently offline.</span><span class="sxs-lookup"><span data-stu-id="029e4-130">Use this criteria to enable a ribbon element based on whether [!INCLUDE[pn_crm_outlook_offline_access](../../includes/pn-crm-outlook-offline-access.md)] is currently offline.</span></span>  

### <a name="crm-outlook-client-type-rule"></a><span data-ttu-id="029e4-131">Crm Outlook Client Type Rule</span><span class="sxs-lookup"><span data-stu-id="029e4-131">Crm Outlook Client Type Rule</span></span>
 <span data-ttu-id="029e4-132">Uses the `<CrmOutlookClientTypeRule>` element.</span><span class="sxs-lookup"><span data-stu-id="029e4-132">Uses the `<CrmOutlookClientTypeRule>` element.</span></span> <span data-ttu-id="029e4-133">Use this rule if you want to only display a button for a specific type of [!INCLUDE[pn_crm_for_outlook_full](../../includes/pn-crm-for-outlook-full.md)].</span><span class="sxs-lookup"><span data-stu-id="029e4-133">Use this rule if you want to only display a button for a specific type of [!INCLUDE[pn_crm_for_outlook_full](../../includes/pn-crm-for-outlook-full.md)].</span></span> <span data-ttu-id="029e4-134">Type options are as follows:</span><span class="sxs-lookup"><span data-stu-id="029e4-134">Type options are as follows:</span></span>  

-   `CrmForOutlook`  

-   `CrmForOutlookOfflineAccess`  

### <a name="custom-rule"></a><span data-ttu-id="029e4-135">Custom Rule</span><span class="sxs-lookup"><span data-stu-id="029e4-135">Custom Rule</span></span>
 <span data-ttu-id="029e4-136">Uses the `<CustomRule>` element.</span><span class="sxs-lookup"><span data-stu-id="029e4-136">Uses the `<CustomRule>` element.</span></span> <span data-ttu-id="029e4-137">Use this kind of rule to call a function in a JavaScript Library that returns a Boolean value.</span><span class="sxs-lookup"><span data-stu-id="029e4-137">Use this kind of rule to call a function in a JavaScript Library that returns a Boolean value.</span></span>  

> [!NOTE]
>  <span data-ttu-id="029e4-138">Custom rules that do not return a value quickly can affect the performance of the ribbon.</span><span class="sxs-lookup"><span data-stu-id="029e4-138">Custom rules that do not return a value quickly can affect the performance of the ribbon.</span></span> <span data-ttu-id="029e4-139">If you have to perform logic that might take some time to complete, use the following strategy to make your custom rule asynchronous:</span><span class="sxs-lookup"><span data-stu-id="029e4-139">If you have to perform logic that might take some time to complete, use the following strategy to make your custom rule asynchronous:</span></span>  
>   
> 1.  <span data-ttu-id="029e4-140">Define a rule that checks for a custom object.</span><span class="sxs-lookup"><span data-stu-id="029e4-140">Define a rule that checks for a custom object.</span></span> <span data-ttu-id="029e4-141">You might check for an object such as `Window.ContosoCustomObject.RuleIsTrue` that you just attach to the Window.</span><span class="sxs-lookup"><span data-stu-id="029e4-141">You might check for an object such as `Window.ContosoCustomObject.RuleIsTrue` that you just attach to the Window.</span></span>  
> 2.  <span data-ttu-id="029e4-142">If that object exists, return it.</span><span class="sxs-lookup"><span data-stu-id="029e4-142">If that object exists, return it.</span></span>  
> 3.  <span data-ttu-id="029e4-143">If that object does not exist, define the object and set the value as false.</span><span class="sxs-lookup"><span data-stu-id="029e4-143">If that object does not exist, define the object and set the value as false.</span></span>  
> 4.  <span data-ttu-id="029e4-144">Before you return a value, use [settimeout](https://msdn.microsoft.com/library/ms536753\(VS.85\).aspx) to execute an asynchronous callback function to re-set the object.</span><span class="sxs-lookup"><span data-stu-id="029e4-144">Before you return a value, use [settimeout](https://msdn.microsoft.com/library/ms536753\(VS.85\).aspx) to execute an asynchronous callback function to re-set the object.</span></span> <span data-ttu-id="029e4-145">Then return false.</span><span class="sxs-lookup"><span data-stu-id="029e4-145">Then return false.</span></span>  
> 5.  <span data-ttu-id="029e4-146">After the callback function has performed the operations that are required to determine the correct result, it sets the value of the object and uses the `refreshRibbon` method to refresh the ribbon.</span><span class="sxs-lookup"><span data-stu-id="029e4-146">After the callback function has performed the operations that are required to determine the correct result, it sets the value of the object and uses the `refreshRibbon` method to refresh the ribbon.</span></span>  
> 6.  <span data-ttu-id="029e4-147">When the ribbon is refreshed, it detects the object together with the accurate value set and the rule is evaluated.</span><span class="sxs-lookup"><span data-stu-id="029e4-147">When the ribbon is refreshed, it detects the object together with the accurate value set and the rule is evaluated.</span></span>  

### <a name="entity-rule"></a><span data-ttu-id="029e4-148">Entity Rule</span><span class="sxs-lookup"><span data-stu-id="029e4-148">Entity Rule</span></span>
 <span data-ttu-id="029e4-149">Uses the `<EntityRule>` element.</span><span class="sxs-lookup"><span data-stu-id="029e4-149">Uses the `<EntityRule>` element.</span></span> <span data-ttu-id="029e4-150">Entity rules allow for evaluation of the current entity.</span><span class="sxs-lookup"><span data-stu-id="029e4-150">Entity rules allow for evaluation of the current entity.</span></span> <span data-ttu-id="029e4-151">This is useful when you define custom actions that apply to the Entity Template instead of for specific entities.</span><span class="sxs-lookup"><span data-stu-id="029e4-151">This is useful when you define custom actions that apply to the Entity Template instead of for specific entities.</span></span> <span data-ttu-id="029e4-152">For example, you may want to add a ribbon element to all entities except for several specific entities.</span><span class="sxs-lookup"><span data-stu-id="029e4-152">For example, you may want to add a ribbon element to all entities except for several specific entities.</span></span> <span data-ttu-id="029e4-153">It is easier to define the custom action for the Entity Template that applies to all entities and then use an Entity Rule to filter out those that should be excluded.</span><span class="sxs-lookup"><span data-stu-id="029e4-153">It is easier to define the custom action for the Entity Template that applies to all entities and then use an Entity Rule to filter out those that should be excluded.</span></span>  

 <span data-ttu-id="029e4-154">The entity rule also includes an optional Context attribute to specify whether the entity is being displayed in the Form or a list (HomePageGrid).</span><span class="sxs-lookup"><span data-stu-id="029e4-154">The entity rule also includes an optional Context attribute to specify whether the entity is being displayed in the Form or a list (HomePageGrid).</span></span> <span data-ttu-id="029e4-155">The optional `AppliesTo` attribute can be set to `PrimaryEntity` or `SelectedEntity` to distinguish whether the entity is being displayed in a subgrid.</span><span class="sxs-lookup"><span data-stu-id="029e4-155">The optional `AppliesTo` attribute can be set to `PrimaryEntity` or `SelectedEntity` to distinguish whether the entity is being displayed in a subgrid.</span></span>  

### <a name="form-state-rule"></a><span data-ttu-id="029e4-156">Form State Rule</span><span class="sxs-lookup"><span data-stu-id="029e4-156">Form State Rule</span></span>
 <span data-ttu-id="029e4-157">Uses the `<FormStateRule>` element.</span><span class="sxs-lookup"><span data-stu-id="029e4-157">Uses the `<FormStateRule>` element.</span></span> <span data-ttu-id="029e4-158">Use the `FormState` rule to determine the current type of form that is displaying a record.</span><span class="sxs-lookup"><span data-stu-id="029e4-158">Use the `FormState` rule to determine the current type of form that is displaying a record.</span></span> <span data-ttu-id="029e4-159">State options are as follows:</span><span class="sxs-lookup"><span data-stu-id="029e4-159">State options are as follows:</span></span>  

-   `Create`  

-   `Existing`  

-   `ReadOnly`  

-   `Disabled`  

-   `BulkEdit`  

### <a name="or-rule"></a><span data-ttu-id="029e4-160">Or Rule</span><span class="sxs-lookup"><span data-stu-id="029e4-160">Or Rule</span></span>
 <span data-ttu-id="029e4-161">Uses the `<OrRule>` element.</span><span class="sxs-lookup"><span data-stu-id="029e4-161">Uses the `<OrRule>` element.</span></span> <span data-ttu-id="029e4-162">The `OrRule` lets you override the default AND comparison for multiple enable rule types.</span><span class="sxs-lookup"><span data-stu-id="029e4-162">The `OrRule` lets you override the default AND comparison for multiple enable rule types.</span></span> <span data-ttu-id="029e4-163">Use the `OrRule` element to define several possible valid combinations to check.</span><span class="sxs-lookup"><span data-stu-id="029e4-163">Use the `OrRule` element to define several possible valid combinations to check.</span></span>

### <a name="outlook-item-tracking-rule"></a><span data-ttu-id="029e4-164">Outlook Item Tracking Rule</span><span class="sxs-lookup"><span data-stu-id="029e4-164">Outlook Item Tracking Rule</span></span>
 <span data-ttu-id="029e4-165">Uses the `<OutlookItemTrackingRule>` element.</span><span class="sxs-lookup"><span data-stu-id="029e4-165">Uses the `<OutlookItemTrackingRule>` element.</span></span> <span data-ttu-id="029e4-166">Use the `TrackedInCrm` attribute for this element to determine whether the record is being tracked in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="029e4-166">Use the `TrackedInCrm` attribute for this element to determine whether the record is being tracked in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement.</span></span>  

### <a name="outlook-version-rule"></a><span data-ttu-id="029e4-167">Outlook Version Rule</span><span class="sxs-lookup"><span data-stu-id="029e4-167">Outlook Version Rule</span></span>
 <span data-ttu-id="029e4-168">Uses the `<OutlookVersionRule>` element.</span><span class="sxs-lookup"><span data-stu-id="029e4-168">Uses the `<OutlookVersionRule>` element.</span></span> <span data-ttu-id="029e4-169">Use this to enable a ribbon element for a specific version of [!INCLUDE[pn_MS_Outlook_Full](../../includes/pn-ms-outlook-full.md)] as follows:</span><span class="sxs-lookup"><span data-stu-id="029e4-169">Use this to enable a ribbon element for a specific version of [!INCLUDE[pn_MS_Outlook_Full](../../includes/pn-ms-outlook-full.md)] as follows:</span></span>  

-   `2003`  

-   `2007`  

-   `2010`  

### <a name="page-rule"></a><span data-ttu-id="029e4-170">Page Rule</span><span class="sxs-lookup"><span data-stu-id="029e4-170">Page Rule</span></span>
 <span data-ttu-id="029e4-171">Uses the `<PageRule>` element.</span><span class="sxs-lookup"><span data-stu-id="029e4-171">Uses the `<PageRule>` element.</span></span> <span data-ttu-id="029e4-172">This type of rule checks the URL of the page being displayed.</span><span class="sxs-lookup"><span data-stu-id="029e4-172">This type of rule checks the URL of the page being displayed.</span></span> <span data-ttu-id="029e4-173">It returns true if the `Address` matches.</span><span class="sxs-lookup"><span data-stu-id="029e4-173">It returns true if the `Address` matches.</span></span>  

### <a name="record-privilege-rule"></a><span data-ttu-id="029e4-174">Record Privilege Rule</span><span class="sxs-lookup"><span data-stu-id="029e4-174">Record Privilege Rule</span></span>
 <span data-ttu-id="029e4-175">Uses the `<RecordPrivilegeRule>` element.</span><span class="sxs-lookup"><span data-stu-id="029e4-175">Uses the `<RecordPrivilegeRule>` element.</span></span> <span data-ttu-id="029e4-176">Use this rule to determine whether the current user has privileges on a specific record.</span><span class="sxs-lookup"><span data-stu-id="029e4-176">Use this rule to determine whether the current user has privileges on a specific record.</span></span> <span data-ttu-id="029e4-177">These privileges differ from an Entity privilege because they can include privileges gained by another user sharing the record with the current user.</span><span class="sxs-lookup"><span data-stu-id="029e4-177">These privileges differ from an Entity privilege because they can include privileges gained by another user sharing the record with the current user.</span></span>  

### <a name="selection-count-rule"></a><span data-ttu-id="029e4-178">Selection Count Rule</span><span class="sxs-lookup"><span data-stu-id="029e4-178">Selection Count Rule</span></span>
 <span data-ttu-id="029e4-179">Uses the `<SelectionCountRule>` element.</span><span class="sxs-lookup"><span data-stu-id="029e4-179">Uses the `<SelectionCountRule>` element.</span></span> <span data-ttu-id="029e4-180">Use this kind of rule with a ribbon displayed for a list to enable a button when specific maximum and minimum numbers of records in the grid are selected.</span><span class="sxs-lookup"><span data-stu-id="029e4-180">Use this kind of rule with a ribbon displayed for a list to enable a button when specific maximum and minimum numbers of records in the grid are selected.</span></span> <span data-ttu-id="029e4-181">For example, if your button merges records, you should make sure at least two records are selected before enabling the ribbon control.</span><span class="sxs-lookup"><span data-stu-id="029e4-181">For example, if your button merges records, you should make sure at least two records are selected before enabling the ribbon control.</span></span>  

### <a name="sku-rule"></a><span data-ttu-id="029e4-182">Sku Rule</span><span class="sxs-lookup"><span data-stu-id="029e4-182">Sku Rule</span></span>
 <span data-ttu-id="029e4-183">Uses the `<SkuRule>` element.</span><span class="sxs-lookup"><span data-stu-id="029e4-183">Uses the `<SkuRule>` element.</span></span> <span data-ttu-id="029e4-184">Use this kind of rule to enable a ribbon element for a specific SKU version of [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] as follows:</span><span class="sxs-lookup"><span data-stu-id="029e4-184">Use this kind of rule to enable a ribbon element for a specific SKU version of [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] as follows:</span></span>  

-   `OnPremise`  

-   `Online`  

-   `Spla`  

### <a name="value-rule"></a><span data-ttu-id="029e4-185">Value Rule</span><span class="sxs-lookup"><span data-stu-id="029e4-185">Value Rule</span></span>
<span data-ttu-id="029e4-186">Uses the `<ValueRule>` element.</span><span class="sxs-lookup"><span data-stu-id="029e4-186">Uses the `<ValueRule>` element.</span></span> <span data-ttu-id="029e4-187">Use this rule to check the value of a specific field in the record being displayed in the form.</span><span class="sxs-lookup"><span data-stu-id="029e4-187">Use this rule to check the value of a specific field in the record being displayed in the form.</span></span> <span data-ttu-id="029e4-188">You must specify the `Field` and the `Value` to check.</span><span class="sxs-lookup"><span data-stu-id="029e4-188">You must specify the `Field` and the `Value` to check.</span></span>  

### <a name="see-also"></a><span data-ttu-id="029e4-189">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="029e4-189">See also</span></span>  
 <span data-ttu-id="029e4-190">[Customize commands and the ribbon](customize-commands-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="029e4-190">[Customize commands and the ribbon](customize-commands-ribbon.md) </span></span>  
 <span data-ttu-id="029e4-191">[Define Ribbon Commands](define-ribbon-commands.md) </span><span class="sxs-lookup"><span data-stu-id="029e4-191">[Define Ribbon Commands](define-ribbon-commands.md) </span></span>  
 [<span data-ttu-id="029e4-192">Define Ribbon Display Rules</span><span class="sxs-lookup"><span data-stu-id="029e4-192">Define Ribbon Display Rules</span></span>](define-ribbon-display-rules.md)
