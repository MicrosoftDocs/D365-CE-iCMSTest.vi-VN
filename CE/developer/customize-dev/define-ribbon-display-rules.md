---
title: Define ribbon display rules (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'Learn about defining specific rules to control when the ribbon elements will display during the configuration of ribbon elements. '
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
- ribbon, display controls
ms.assetid: b247c51a-753b-48e5-9772-83346416886c
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 42bbb997c5c57f22cdef29ada02857e6f3db96ba
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385497"
---
# <a name="define-ribbon-display-rules"></a><span data-ttu-id="26701-103">Define ribbon display rules</span><span class="sxs-lookup"><span data-stu-id="26701-103">Define ribbon display rules</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="26701-104">When configuring ribbon elements, you can define specific rules to control when the ribbon elements will display.</span><span class="sxs-lookup"><span data-stu-id="26701-104">When configuring ribbon elements, you can define specific rules to control when the ribbon elements will display.</span></span>  

-   <span data-ttu-id="26701-105">Use the /`RuleDefinitions`/DisplayRules/`<DisplayRule>` element to define rules controlling when the ribbon element should be displayed.</span><span class="sxs-lookup"><span data-stu-id="26701-105">Use the /`RuleDefinitions`/DisplayRules/`<DisplayRule>` element to define rules controlling when the ribbon element should be displayed.</span></span>  

-   <span data-ttu-id="26701-106">Use the /CommandDefinitions/`CommandDefinition`/DisplayRules/`<DisplayRule>` element to associate specific display rules to a command definition.</span><span class="sxs-lookup"><span data-stu-id="26701-106">Use the /CommandDefinitions/`CommandDefinition`/DisplayRules/`<DisplayRule>` element to associate specific display rules to a command definition.</span></span>  

## <a name="control-when-ribbon-elements-are-displayed"></a><span data-ttu-id="26701-107">Control when ribbon elements are displayed</span><span class="sxs-lookup"><span data-stu-id="26701-107">Control when ribbon elements are displayed</span></span>  
 <span data-ttu-id="26701-108">By defining display rules in rule definitions, you can use the same display rule for many command definitions.</span><span class="sxs-lookup"><span data-stu-id="26701-108">By defining display rules in rule definitions, you can use the same display rule for many command definitions.</span></span> <span data-ttu-id="26701-109">When more than one display rule is defined for a command definition, all of the display rules must evaluate as true for the ribbon element to be displayed.</span><span class="sxs-lookup"><span data-stu-id="26701-109">When more than one display rule is defined for a command definition, all of the display rules must evaluate as true for the ribbon element to be displayed.</span></span>  

 <span data-ttu-id="26701-110">All display rules provide an optional attribute to specify whether the default value of the rule is true or false and an optional `InvertResult` attribute to enable returning a negative result when the item being tested returns true.</span><span class="sxs-lookup"><span data-stu-id="26701-110">All display rules provide an optional attribute to specify whether the default value of the rule is true or false and an optional `InvertResult` attribute to enable returning a negative result when the item being tested returns true.</span></span>  

 <span data-ttu-id="26701-111">The `/RuleDefinitions/DisplayRules/DisplayRule` element supports the following types of rules:</span><span class="sxs-lookup"><span data-stu-id="26701-111">The `/RuleDefinitions/DisplayRules/DisplayRule` element supports the following types of rules:</span></span>  

 `<CommandClientTypeRule>`  
[!INCLUDE[ribbon_element_CommandClientTypeRule](../../includes/ribbon-element-commandclienttyperule.md)]

 <span data-ttu-id="26701-112">The `Type` values correspond to the following:</span><span class="sxs-lookup"><span data-stu-id="26701-112">The `Type` values correspond to the following:</span></span>  


|   <span data-ttu-id="26701-113">Value</span><span class="sxs-lookup"><span data-stu-id="26701-113">Value</span></span>   |                                                                               <span data-ttu-id="26701-114">Bản trình bày</span><span class="sxs-lookup"><span data-stu-id="26701-114">Presentation</span></span>                                                                               |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Modern`  |                                       <span data-ttu-id="26701-115">The command bar is presented using [!INCLUDE[pn_moca_full](../../includes/pn-moca-full.md)].</span><span class="sxs-lookup"><span data-stu-id="26701-115">The command bar is presented using [!INCLUDE[pn_moca_full](../../includes/pn-moca-full.md)].</span></span>                                       |
| `Refresh` |                                                      <span data-ttu-id="26701-116">The command bar is presented using the updated user interface.</span><span class="sxs-lookup"><span data-stu-id="26701-116">The command bar is presented using the updated user interface.</span></span>                                                      |
| `Legacy`  | <span data-ttu-id="26701-117">The ribbon is presented in forms for entities that were not updated or in a list view in [!INCLUDE[pn_crm_for_outlook_full](../../includes/pn-crm-for-outlook-full.md)].</span><span class="sxs-lookup"><span data-stu-id="26701-117">The ribbon is presented in forms for entities that were not updated or in a list view in [!INCLUDE[pn_crm_for_outlook_full](../../includes/pn-crm-for-outlook-full.md)].</span></span> |

 `<CrmClientTypeRule>`  
 <span data-ttu-id="26701-118">Allows definition of rules depending on the type of client used.</span><span class="sxs-lookup"><span data-stu-id="26701-118">Allows definition of rules depending on the type of client used.</span></span> <span data-ttu-id="26701-119">`Type` options are as follows:</span><span class="sxs-lookup"><span data-stu-id="26701-119">`Type` options are as follows:</span></span>  

- <span data-ttu-id="26701-120">Web</span><span class="sxs-lookup"><span data-stu-id="26701-120">Web</span></span>  

- <span data-ttu-id="26701-121">Outlook</span><span class="sxs-lookup"><span data-stu-id="26701-121">Outlook</span></span>  

  `<CrmOfflineAccessStateRule>`  
  <span data-ttu-id="26701-122">Use this criteria to display a ribbon element based on whether [!INCLUDE[pn_crm_outlook_offline_access](../../includes/pn-crm-outlook-offline-access.md)] is currently offline.</span><span class="sxs-lookup"><span data-stu-id="26701-122">Use this criteria to display a ribbon element based on whether [!INCLUDE[pn_crm_outlook_offline_access](../../includes/pn-crm-outlook-offline-access.md)] is currently offline.</span></span>  

  `<CrmOutlookClientTypeRule>`  
  <span data-ttu-id="26701-123">Use this rule if you want to display a button for the specific type of [!INCLUDE[pn_crm_for_outlook_full](../../includes/pn-crm-for-outlook-full.md)].</span><span class="sxs-lookup"><span data-stu-id="26701-123">Use this rule if you want to display a button for the specific type of [!INCLUDE[pn_crm_for_outlook_full](../../includes/pn-crm-for-outlook-full.md)].</span></span> <span data-ttu-id="26701-124">`Type` options are as follows:</span><span class="sxs-lookup"><span data-stu-id="26701-124">`Type` options are as follows:</span></span>  

- <span data-ttu-id="26701-125">CrmForOutlook</span><span class="sxs-lookup"><span data-stu-id="26701-125">CrmForOutlook</span></span>  

- <span data-ttu-id="26701-126">CrmForOutlookOfflineAccess</span><span class="sxs-lookup"><span data-stu-id="26701-126">CrmForOutlookOfflineAccess</span></span>  

  `<CrmOutlookClientVersionRule>`  
  [!INCLUDE[ribbon_element_CrmOutlookClientVersionRule](../../includes/ribbon-element-crmoutlookclientversionrule.md)]

  <span data-ttu-id="26701-127">Valid values:</span><span class="sxs-lookup"><span data-stu-id="26701-127">Valid values:</span></span>  

- <span data-ttu-id="26701-128">2003</span><span class="sxs-lookup"><span data-stu-id="26701-128">2003</span></span>  

- <span data-ttu-id="26701-129">2007</span><span class="sxs-lookup"><span data-stu-id="26701-129">2007</span></span>  

- <span data-ttu-id="26701-130">2010</span><span class="sxs-lookup"><span data-stu-id="26701-130">2010</span></span>  

  `<EntityPrivilegeRule>`  
  <span data-ttu-id="26701-131">Use this kind of rule to display ribbon elements when a user has specific privileges for an entity.</span><span class="sxs-lookup"><span data-stu-id="26701-131">Use this kind of rule to display ribbon elements when a user has specific privileges for an entity.</span></span> <span data-ttu-id="26701-132">You must specify the privilege depth and the specific privilege you want to check.</span><span class="sxs-lookup"><span data-stu-id="26701-132">You must specify the privilege depth and the specific privilege you want to check.</span></span>  

  `<EntityPropertyRule>`  
  <span data-ttu-id="26701-133">Allows definition of rules depending on the Boolean values of specific entity properties.</span><span class="sxs-lookup"><span data-stu-id="26701-133">Allows definition of rules depending on the Boolean values of specific entity properties.</span></span> <span data-ttu-id="26701-134">`PropertyName` options are as follows:</span><span class="sxs-lookup"><span data-stu-id="26701-134">`PropertyName` options are as follows:</span></span>  

- <span data-ttu-id="26701-135">DuplicateDetectionEnabled</span><span class="sxs-lookup"><span data-stu-id="26701-135">DuplicateDetectionEnabled</span></span>  

- <span data-ttu-id="26701-136">GridFiltersEnabled</span><span class="sxs-lookup"><span data-stu-id="26701-136">GridFiltersEnabled</span></span>  

- <span data-ttu-id="26701-137">HasStateCode</span><span class="sxs-lookup"><span data-stu-id="26701-137">HasStateCode</span></span>  

- <span data-ttu-id="26701-138">IsConnectionsEnabled</span><span class="sxs-lookup"><span data-stu-id="26701-138">IsConnectionsEnabled</span></span>  

- <span data-ttu-id="26701-139">MailMergeEnabled</span><span class="sxs-lookup"><span data-stu-id="26701-139">MailMergeEnabled</span></span>  

- <span data-ttu-id="26701-140">WorksWithQueue</span><span class="sxs-lookup"><span data-stu-id="26701-140">WorksWithQueue</span></span>  

- <span data-ttu-id="26701-141">HasActivities</span><span class="sxs-lookup"><span data-stu-id="26701-141">HasActivities</span></span>  

- <span data-ttu-id="26701-142">IsActivity</span><span class="sxs-lookup"><span data-stu-id="26701-142">IsActivity</span></span>  

- <span data-ttu-id="26701-143">HasNotes</span><span class="sxs-lookup"><span data-stu-id="26701-143">HasNotes</span></span>  

  `<EntityRule>`  
  <span data-ttu-id="26701-144">Entity rules allow for evaluation of the current entity.</span><span class="sxs-lookup"><span data-stu-id="26701-144">Entity rules allow for evaluation of the current entity.</span></span> <span data-ttu-id="26701-145">This is useful when you define custom actions that apply to the entity template instead of for specific entities.</span><span class="sxs-lookup"><span data-stu-id="26701-145">This is useful when you define custom actions that apply to the entity template instead of for specific entities.</span></span> <span data-ttu-id="26701-146">For example, you may want to add a ribbon element to all entities except for some specific entities.</span><span class="sxs-lookup"><span data-stu-id="26701-146">For example, you may want to add a ribbon element to all entities except for some specific entities.</span></span> <span data-ttu-id="26701-147">It is easier to define the custom action for the entity template that applies to all entities and then use an entity rule to filter out those that should be excluded.</span><span class="sxs-lookup"><span data-stu-id="26701-147">It is easier to define the custom action for the entity template that applies to all entities and then use an entity rule to filter out those that should be excluded.</span></span>  

  <span data-ttu-id="26701-148">The entity rule also includes an optional context attribute to specify whether the entity is being displayed in the form or a list (HomePageGrid).</span><span class="sxs-lookup"><span data-stu-id="26701-148">The entity rule also includes an optional context attribute to specify whether the entity is being displayed in the form or a list (HomePageGrid).</span></span> <span data-ttu-id="26701-149">The optional `AppliesTo` attribute can be set to `PrimaryEntity` or `SelectedEntity` to distinguish whether the entity is being displayed in a subgrid.</span><span class="sxs-lookup"><span data-stu-id="26701-149">The optional `AppliesTo` attribute can be set to `PrimaryEntity` or `SelectedEntity` to distinguish whether the entity is being displayed in a subgrid.</span></span>  

  `<FormEntityContextRule>`  
  [!INCLUDE[ribbon_element_FormEntityContextRule](../../includes/ribbon-element-formentitycontextrule.md)]

  `<FormStateRule`  
  <span data-ttu-id="26701-150">Use the form state rule to determine the current type of form that is displaying a record.</span><span class="sxs-lookup"><span data-stu-id="26701-150">Use the form state rule to determine the current type of form that is displaying a record.</span></span> <span data-ttu-id="26701-151">`State` options are as follows:</span><span class="sxs-lookup"><span data-stu-id="26701-151">`State` options are as follows:</span></span>  

- <span data-ttu-id="26701-152">Tạo</span><span class="sxs-lookup"><span data-stu-id="26701-152">Create</span></span>  

- <span data-ttu-id="26701-153">Existing</span><span class="sxs-lookup"><span data-stu-id="26701-153">Existing</span></span>  

- <span data-ttu-id="26701-154">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="26701-154">ReadOnly</span></span>  

- <span data-ttu-id="26701-155">Đã vô hiệu hóa</span><span class="sxs-lookup"><span data-stu-id="26701-155">Disabled</span></span>  

- <span data-ttu-id="26701-156">BulkEdit</span><span class="sxs-lookup"><span data-stu-id="26701-156">BulkEdit</span></span>  

  `<FormTypeRule>`  
  [!INCLUDE[ribbon_element_FormTypeRule](../../includes/ribbon-element-formtyperule.md)]

  <span data-ttu-id="26701-157">The `Type` values correspond to the following:</span><span class="sxs-lookup"><span data-stu-id="26701-157">The `Type` values correspond to the following:</span></span>  

|<span data-ttu-id="26701-158">Value</span><span class="sxs-lookup"><span data-stu-id="26701-158">Value</span></span>|<span data-ttu-id="26701-159">Bản trình bày</span><span class="sxs-lookup"><span data-stu-id="26701-159">Presentation</span></span>|  
|-----------|------------------|  
|`Main`|<span data-ttu-id="26701-160">An entity form displayed in the application.</span><span class="sxs-lookup"><span data-stu-id="26701-160">An entity form displayed in the application.</span></span>|  
|`Preview`|<span data-ttu-id="26701-161">The entity preview form displayed as an expanding element in the grid.</span><span class="sxs-lookup"><span data-stu-id="26701-161">The entity preview form displayed as an expanding element in the grid.</span></span>|  
|`AppointmentBook`|<span data-ttu-id="26701-162">Used with the appointment, equipment, serviceappointment, and systemuser entities for the Service Scheduling user interface.</span><span class="sxs-lookup"><span data-stu-id="26701-162">Used with the appointment, equipment, serviceappointment, and systemuser entities for the Service Scheduling user interface.</span></span>|  
|`Dashboard`|<span data-ttu-id="26701-163">The form defines a dashboard.</span><span class="sxs-lookup"><span data-stu-id="26701-163">The form defines a dashboard.</span></span>|  
|`Quick`|<span data-ttu-id="26701-164">A quick view form.</span><span class="sxs-lookup"><span data-stu-id="26701-164">A quick view form.</span></span>|  
|`QuickCreate`|<span data-ttu-id="26701-165">A quick create form.</span><span class="sxs-lookup"><span data-stu-id="26701-165">A quick create form.</span></span>|  

 `<HideForTabletExperienceRule>`  
 [!INCLUDE[ribbon_element_HideForTabletExperienceRule](../../includes/ribbon-element-hidefortabletexperiencerule.md)]

 `<MiscellaneousPrivilegeRule>`  
 <span data-ttu-id="26701-166">Use this kind of rule to check for privileges that do not apply to a specific entity, such as ExportToExcel, MailMerge, or GoOffline.</span><span class="sxs-lookup"><span data-stu-id="26701-166">Use this kind of rule to check for privileges that do not apply to a specific entity, such as ExportToExcel, MailMerge, or GoOffline.</span></span>  

 `<OrganizationSettingRule>`  
 <span data-ttu-id="26701-167">Use this to display a ribbon element if specific organization settings are enabled.</span><span class="sxs-lookup"><span data-stu-id="26701-167">Use this to display a ribbon element if specific organization settings are enabled.</span></span> <span data-ttu-id="26701-168">Setting options are as follows:</span><span class="sxs-lookup"><span data-stu-id="26701-168">Setting options are as follows:</span></span>  

- <span data-ttu-id="26701-169">IsSharepointEnabled</span><span class="sxs-lookup"><span data-stu-id="26701-169">IsSharepointEnabled</span></span>  

- <span data-ttu-id="26701-170">IsSOPIntegrationEnabled</span><span class="sxs-lookup"><span data-stu-id="26701-170">IsSOPIntegrationEnabled</span></span>  

- <span data-ttu-id="26701-171">IsFiscalCalendarDefined</span><span class="sxs-lookup"><span data-stu-id="26701-171">IsFiscalCalendarDefined</span></span>  

  <span data-ttu-id="26701-172">`<OrRule>` This rule lets you override the default AND comparison for multiple display rule types.</span><span class="sxs-lookup"><span data-stu-id="26701-172">`<OrRule>` This rule lets you override the default AND comparison for multiple display rule types.</span></span> <span data-ttu-id="26701-173">Use the `OrRule` element to define several possible valid combinations to check.</span><span class="sxs-lookup"><span data-stu-id="26701-173">Use the `OrRule` element to define several possible valid combinations to check.</span></span>  

  `<OutlookRenderTypeRule>`  
  <span data-ttu-id="26701-174">Use this to display a ribbon element if the ribbon is being displayed in [!INCLUDE[pn_MS_Outlook_Short](../../includes/pn-ms-outlook-short.md)] in a specific way.</span><span class="sxs-lookup"><span data-stu-id="26701-174">Use this to display a ribbon element if the ribbon is being displayed in [!INCLUDE[pn_MS_Outlook_Short](../../includes/pn-ms-outlook-short.md)] in a specific way.</span></span> <span data-ttu-id="26701-175">`Type` options are as follows:</span><span class="sxs-lookup"><span data-stu-id="26701-175">`Type` options are as follows:</span></span>  

- <span data-ttu-id="26701-176">Web</span><span class="sxs-lookup"><span data-stu-id="26701-176">Web</span></span>  

- <span data-ttu-id="26701-177">Outlook</span><span class="sxs-lookup"><span data-stu-id="26701-177">Outlook</span></span>  

  `<OutlookVersionRule>`  
  <span data-ttu-id="26701-178">Use this to display a ribbon element for a specific version of [!INCLUDE[pn_MS_Outlook_Short](../../includes/pn-ms-outlook-short.md)].</span><span class="sxs-lookup"><span data-stu-id="26701-178">Use this to display a ribbon element for a specific version of [!INCLUDE[pn_MS_Outlook_Short](../../includes/pn-ms-outlook-short.md)].</span></span> <span data-ttu-id="26701-179">`Version` options are as follows:</span><span class="sxs-lookup"><span data-stu-id="26701-179">`Version` options are as follows:</span></span>  

- <span data-ttu-id="26701-180">2003</span><span class="sxs-lookup"><span data-stu-id="26701-180">2003</span></span>  

- <span data-ttu-id="26701-181">2007</span><span class="sxs-lookup"><span data-stu-id="26701-181">2007</span></span>  

- <span data-ttu-id="26701-182">2010</span><span class="sxs-lookup"><span data-stu-id="26701-182">2010</span></span>  

  `<PageRule>`  
  <span data-ttu-id="26701-183">This type of rule checks the URL of the page being displayed.</span><span class="sxs-lookup"><span data-stu-id="26701-183">This type of rule checks the URL of the page being displayed.</span></span> <span data-ttu-id="26701-184">It returns true if the address matches.</span><span class="sxs-lookup"><span data-stu-id="26701-184">It returns true if the address matches.</span></span>  

  <span data-ttu-id="26701-185">`<RelationshipTypeRule>` This type of rule is applied to records selected in a grid.</span><span class="sxs-lookup"><span data-stu-id="26701-185">`<RelationshipTypeRule>` This type of rule is applied to records selected in a grid.</span></span> <span data-ttu-id="26701-186">It lets you determine the type of relationship, as follows:</span><span class="sxs-lookup"><span data-stu-id="26701-186">It lets you determine the type of relationship, as follows:</span></span>  

- <span data-ttu-id="26701-187">OneToMany</span><span class="sxs-lookup"><span data-stu-id="26701-187">OneToMany</span></span>  

- <span data-ttu-id="26701-188">ManyToMany</span><span class="sxs-lookup"><span data-stu-id="26701-188">ManyToMany</span></span>  

- <span data-ttu-id="26701-189">NoRelationship</span><span class="sxs-lookup"><span data-stu-id="26701-189">NoRelationship</span></span>  

  `<SkuRule>`  
  <span data-ttu-id="26701-190">Use this kind of rule to display a ribbon element for a specific SKU version of [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement, as follows:</span><span class="sxs-lookup"><span data-stu-id="26701-190">Use this kind of rule to display a ribbon element for a specific SKU version of [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement, as follows:</span></span>  

- <span data-ttu-id="26701-191">OnPremise</span><span class="sxs-lookup"><span data-stu-id="26701-191">OnPremise</span></span>  

- <span data-ttu-id="26701-192">Trực tuyến</span><span class="sxs-lookup"><span data-stu-id="26701-192">Online</span></span>  

- <span data-ttu-id="26701-193">Spla</span><span class="sxs-lookup"><span data-stu-id="26701-193">Spla</span></span>  

  `<ValueRule>`  
  <span data-ttu-id="26701-194">Use this rule to check the value of a specific field in the record being displayed in the form.</span><span class="sxs-lookup"><span data-stu-id="26701-194">Use this rule to check the value of a specific field in the record being displayed in the form.</span></span>  

> [!NOTE]
>  <span data-ttu-id="26701-195">For commands defined for subgrid for forms using the updated user experience, value rules cannot be used within display rules.</span><span class="sxs-lookup"><span data-stu-id="26701-195">For commands defined for subgrid for forms using the updated user experience, value rules cannot be used within display rules.</span></span> <span data-ttu-id="26701-196">Use this element within an `<EnableRule>` to hide an element.</span><span class="sxs-lookup"><span data-stu-id="26701-196">Use this element within an `<EnableRule>` to hide an element.</span></span>  

### <a name="see-also"></a><span data-ttu-id="26701-197">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="26701-197">See also</span></span>  
 <span data-ttu-id="26701-198">[Tùy chỉnh lệnh và ru băng](customize-commands-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="26701-198">[Customize commands and the ribbon](customize-commands-ribbon.md) </span></span>  
 <span data-ttu-id="26701-199">[Define Ribbon Enable Rules](define-ribbon-enable-rules.md) </span><span class="sxs-lookup"><span data-stu-id="26701-199">[Define Ribbon Enable Rules](define-ribbon-enable-rules.md) </span></span>  
 [<span data-ttu-id="26701-200">Define Ribbon Actions</span><span class="sxs-lookup"><span data-stu-id="26701-200">Define Ribbon Actions</span></span>](define-ribbon-actions.md)
