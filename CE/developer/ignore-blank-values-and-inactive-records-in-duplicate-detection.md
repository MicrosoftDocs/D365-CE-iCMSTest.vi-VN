---
title: Ignore blank values and inactive records in duplicate detection (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Improve result quality by creating duplicate detection rules that ignore blank values and inactive records.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 7b905429-1bde-4ba5-a523-62ab770b2582
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: de7a16a8efbc26de016cefad9a2770b0d0487988
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386760"
---
# <a name="ignore-blank-values-and-inactive-records-in-duplicate-detection"></a>Ignore blank values and inactive records in duplicate detection

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

You can improve data results by creating duplicate detection rules that ignore blank values and inactive records. This will help to refine your results and reduce the amount of erroneous data.  
  
## <a name="rules-for-ignoring-blank-values-and-inactive-records"></a>Rules for Ignoring Blank Values and Inactive Records  
 A duplicate detection rule can have more than one rule condition. For example, you can specify that an account is a duplicate of another record if both of the following conditions are satisfied:  
  
- Account names match in both records.  
  
- Email IDs match in both records.  
  
  However, with this rule, the system flags any two records as duplicates if the account names match and the email IDs are null values. In another example, two records are flagged as duplicates if their email IDs and status match. In this case, all active, and inactive, records that have email IDs equal to **null** are flagged as duplicates. This may flood a system with a large number of unintended duplicate records. To avoid flagging inactive records and records with null values as duplicates, two new attributes were added, `IgnoreBlankValues`and `ExcludeInactiveRecords`.  
  
  The following table describes the new attributes.  
  
|          Thực thể          |        Thuộc tính         |  Loại   |                                                                                                                                                                                                                                                                    Mô tả                                                                                                                                                                                                                                                                     |
|--------------------------|--------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `DuplicateRuleCondition` |   `IgnoreBlankValues`    | Boolean | Specifies whether to consider blank values as non-duplicate values. The default value of this attribute is `false`. Set it to `true`if you do not want the duplicate detection rule to consider **null**) values as equal. When you upgrade from earlier versions of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, this attribute is set to `false`.<br /><br /> Quan trọng:<br /><br /> For a duplicate detection rule with one condition, if you set the attribute value to `false`, it is treated by the system as a `true`value. |
|     `DuplicateRule`      | `ExcludeInactiveRecords` | Boolean |                                                                       Specifies whether to flag inactive records as duplicates. The default value is `false`. Set it to                              `true`if you do not want inactive records to be flagged as duplicates, even if they meet duplication detection rule criteria. When you upgrade from earlier versions of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, this attribute is set to `false`.                                                                        |
  
 There are entities that have states other than Active and Inactive. If you set the `ExcludeInactiveRecords`attribute to `true`, the duplicate detection process will consider matching records only in the Active states or in states that are considered Active.  
  
 The following table lists the entity records and the corresponding states.  
  
|Entity Record|Considered as Active State|Considered as Inactive State|  
|-------------------|--------------------------------|----------------------------------|  
|`Appointment`|Open, Scheduled|Completed, Canceled|  
|`CampaignActivity`|Mở|Closed, Canceled|  
|`CampaignResponse`|Mở|Completed, Canceled|  
|`Contract`|Draft, Invoiced, On Hold|Canceled, Expired|  
|`ContractDetail`|Existing, Renewed|Canceled, Expired|  
|`Email`|Mở|Completed, Canceled|  
|`Fax`|Mở|Completed, Canceled|  
|`Incident`|Hoạt động|Resolved, Canceled, Closed|  
|`Invoice`|Hoạt động|Closed, Paid, Canceled|  
|`KbArticle`|Draft, Unapproved, Published|Không áp dụng|  
|`Lead`|Mở|Qualified, Disqualified|  
|`Letter`|Mở|Completed, Canceled|  
|`Opportunity`|Mở|Won, Lost|  
|`PhoneCall`|Mở|Completed, Canceled|  
|`Quote`|Draft, Active|Won, Closed|  
|`SalesOrder`|Active, Submitted, Invoiced|Canceled, Fulfilled|  
|`ServiceAppointment`|Open, Scheduled|Closed, Canceled|  
|`Task`|Mở|Completed, Canceled|  
  
 For example, if you set the `ExcludeInactiveRecords`attribute to `true`, only active, submitted, and invoiced sales orders will be considered for matching during duplicate detection.  
  
### <a name="see-also"></a>Xem thêm  
 [Detect Duplicate Data in Dynamics 365 for Customer Engagement apps](detect-duplicate-data-for-developers.md)   
 [Enable and Disable duplicate detection](enable-disable-duplicate-detection.md)
