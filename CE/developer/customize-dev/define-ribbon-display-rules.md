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
# <a name="define-ribbon-display-rules"></a>Define ribbon display rules

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

When configuring ribbon elements, you can define specific rules to control when the ribbon elements will display.  

-   Use the /`RuleDefinitions`/DisplayRules/`<DisplayRule>` element to define rules controlling when the ribbon element should be displayed.  

-   Use the /CommandDefinitions/`CommandDefinition`/DisplayRules/`<DisplayRule>` element to associate specific display rules to a command definition.  

## <a name="control-when-ribbon-elements-are-displayed"></a>Control when ribbon elements are displayed  
 By defining display rules in rule definitions, you can use the same display rule for many command definitions. When more than one display rule is defined for a command definition, all of the display rules must evaluate as true for the ribbon element to be displayed.  

 All display rules provide an optional attribute to specify whether the default value of the rule is true or false and an optional `InvertResult` attribute to enable returning a negative result when the item being tested returns true.  

 The `/RuleDefinitions/DisplayRules/DisplayRule` element supports the following types of rules:  

 `<CommandClientTypeRule>`  
[!INCLUDE[ribbon_element_CommandClientTypeRule](../../includes/ribbon-element-commandclienttyperule.md)]

 The `Type` values correspond to the following:  


|   Value   |                                                                               Bản trình bày                                                                               |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Modern`  |                                       The command bar is presented using [!INCLUDE[pn_moca_full](../../includes/pn-moca-full.md)].                                       |
| `Refresh` |                                                      The command bar is presented using the updated user interface.                                                      |
| `Legacy`  | The ribbon is presented in forms for entities that were not updated or in a list view in [!INCLUDE[pn_crm_for_outlook_full](../../includes/pn-crm-for-outlook-full.md)]. |

 `<CrmClientTypeRule>`  
 Allows definition of rules depending on the type of client used. `Type` options are as follows:  

- Web  

- Outlook  

  `<CrmOfflineAccessStateRule>`  
  Use this criteria to display a ribbon element based on whether [!INCLUDE[pn_crm_outlook_offline_access](../../includes/pn-crm-outlook-offline-access.md)] is currently offline.  

  `<CrmOutlookClientTypeRule>`  
  Use this rule if you want to display a button for the specific type of [!INCLUDE[pn_crm_for_outlook_full](../../includes/pn-crm-for-outlook-full.md)]. `Type` options are as follows:  

- CrmForOutlook  

- CrmForOutlookOfflineAccess  

  `<CrmOutlookClientVersionRule>`  
  [!INCLUDE[ribbon_element_CrmOutlookClientVersionRule](../../includes/ribbon-element-crmoutlookclientversionrule.md)]

  Valid values:  

- 2003  

- 2007  

- 2010  

  `<EntityPrivilegeRule>`  
  Use this kind of rule to display ribbon elements when a user has specific privileges for an entity. You must specify the privilege depth and the specific privilege you want to check.  

  `<EntityPropertyRule>`  
  Allows definition of rules depending on the Boolean values of specific entity properties. `PropertyName` options are as follows:  

- DuplicateDetectionEnabled  

- GridFiltersEnabled  

- HasStateCode  

- IsConnectionsEnabled  

- MailMergeEnabled  

- WorksWithQueue  

- HasActivities  

- IsActivity  

- HasNotes  

  `<EntityRule>`  
  Entity rules allow for evaluation of the current entity. This is useful when you define custom actions that apply to the entity template instead of for specific entities. For example, you may want to add a ribbon element to all entities except for some specific entities. It is easier to define the custom action for the entity template that applies to all entities and then use an entity rule to filter out those that should be excluded.  

  The entity rule also includes an optional context attribute to specify whether the entity is being displayed in the form or a list (HomePageGrid). The optional `AppliesTo` attribute can be set to `PrimaryEntity` or `SelectedEntity` to distinguish whether the entity is being displayed in a subgrid.  

  `<FormEntityContextRule>`  
  [!INCLUDE[ribbon_element_FormEntityContextRule](../../includes/ribbon-element-formentitycontextrule.md)]

  `<FormStateRule`  
  Use the form state rule to determine the current type of form that is displaying a record. `State` options are as follows:  

- Tạo  

- Existing  

- ReadOnly  

- Đã vô hiệu hóa  

- BulkEdit  

  `<FormTypeRule>`  
  [!INCLUDE[ribbon_element_FormTypeRule](../../includes/ribbon-element-formtyperule.md)]

  The `Type` values correspond to the following:  

|Value|Bản trình bày|  
|-----------|------------------|  
|`Main`|An entity form displayed in the application.|  
|`Preview`|The entity preview form displayed as an expanding element in the grid.|  
|`AppointmentBook`|Used with the appointment, equipment, serviceappointment, and systemuser entities for the Service Scheduling user interface.|  
|`Dashboard`|The form defines a dashboard.|  
|`Quick`|A quick view form.|  
|`QuickCreate`|A quick create form.|  

 `<HideForTabletExperienceRule>`  
 [!INCLUDE[ribbon_element_HideForTabletExperienceRule](../../includes/ribbon-element-hidefortabletexperiencerule.md)]

 `<MiscellaneousPrivilegeRule>`  
 Use this kind of rule to check for privileges that do not apply to a specific entity, such as ExportToExcel, MailMerge, or GoOffline.  

 `<OrganizationSettingRule>`  
 Use this to display a ribbon element if specific organization settings are enabled. Setting options are as follows:  

- IsSharepointEnabled  

- IsSOPIntegrationEnabled  

- IsFiscalCalendarDefined  

  `<OrRule>` This rule lets you override the default AND comparison for multiple display rule types. Use the `OrRule` element to define several possible valid combinations to check.  

  `<OutlookRenderTypeRule>`  
  Use this to display a ribbon element if the ribbon is being displayed in [!INCLUDE[pn_MS_Outlook_Short](../../includes/pn-ms-outlook-short.md)] in a specific way. `Type` options are as follows:  

- Web  

- Outlook  

  `<OutlookVersionRule>`  
  Use this to display a ribbon element for a specific version of [!INCLUDE[pn_MS_Outlook_Short](../../includes/pn-ms-outlook-short.md)]. `Version` options are as follows:  

- 2003  

- 2007  

- 2010  

  `<PageRule>`  
  This type of rule checks the URL of the page being displayed. It returns true if the address matches.  

  `<RelationshipTypeRule>` This type of rule is applied to records selected in a grid. It lets you determine the type of relationship, as follows:  

- OneToMany  

- ManyToMany  

- NoRelationship  

  `<SkuRule>`  
  Use this kind of rule to display a ribbon element for a specific SKU version of [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement, as follows:  

- OnPremise  

- Trực tuyến  

- Spla  

  `<ValueRule>`  
  Use this rule to check the value of a specific field in the record being displayed in the form.  

> [!NOTE]
>  For commands defined for subgrid for forms using the updated user experience, value rules cannot be used within display rules. Use this element within an `<EnableRule>` to hide an element.  

### <a name="see-also"></a>Xem thêm  
 [Tùy chỉnh lệnh và ru băng](customize-commands-ribbon.md)   
 [Define Ribbon Enable Rules](define-ribbon-enable-rules.md)   
 [Define Ribbon Actions](define-ribbon-actions.md)
