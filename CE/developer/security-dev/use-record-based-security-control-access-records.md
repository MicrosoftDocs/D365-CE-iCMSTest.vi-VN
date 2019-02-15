---
title: Use record-based security to control access to records (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Provides record-based security to manage access rights to individual Customer Engagement records.
ms.custom: ''
ms.date: 08/18/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: f2b7ddcc-6678-492f-8b4b-478e00049362
caps.latest.revision: 39
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4a0c99130f75bfeac4e25e7d03f7af39c5ec3080
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388542"
---
# <a name="use-record-based-security-to-control-access-to-records"></a>Use record-based security to control access to records

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

Record-based security in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps applies to individual records. It is provided by using access rights.  
  
 The relationship between an access right and a privilege is that access rights apply only after privileges have taken effect. For example, if a user does not have the privilege to read accounts, that user is unable to read any account, regardless of the access rights another user might grant to a specific account through sharing.  
  
<a name="BKMK_AccessRights"></a>   
## <a name="access-rights"></a>Access rights  
 An access right is granted to a user for a particular record. The following table lists the descriptions for these access rights.  
  
|Access right|<xref:Microsoft.Crm.Sdk.Messages.AccessRights> enumeration value|Mô tả|  
|------------------|---------------------------------------------------------------------------------------------------------------------|-----------------|  
|Đọc|ReadAccess|Controls whether the user can read a record.|  
|Ghi|WriteAccess|Controls whether the user can update a record.|  
|Chỉ định|AssignAccess|Controls whether the user can assign a record to another user.|  
|Nối|AppendAccess|Controls whether the user can attach another record to the specified record.<br /><br /> Quyền truy cập Gắn thêm và Gắn thêm vào hoạt động kết hợp. Mỗi khi người dùng đính kèm một bản ghi vào bản ghi khác, người dùng này phải có cả hai quyền. Ví dụ: khi bạn đính kèm ghi chú vào một trường hợp, bạn phải có quyền truy Gắn thêm ngay trên ghi chú và quyền Gắn thêm vào ngay trên trường hợp để thực hiện thao tác này.|  
|Gắn thêm vào|AppendToAccess|Controls whether the user can append the record in question to another record.<br /><br /> Quyền truy cập Gắn thêm và Gắn thêm vào hoạt động kết hợp. Để biết thêm thông tin, hãy xem mô tả về đặc quyền Gắn thêm.|  
|Chia sẻ|ShareAccess|Controls whether the user can share a record with another user or team. Sharing gives another user access to a record. For more information, see [Sharing Records](use-record-based-security-control-access-records.md#BKMK_SharingInstances).|  
|Xóa|DeleteAccess|Controls whether the user can delete a record.|  
  
### <a name="create-access"></a>Create access  
 The right to create a record for an entity type is not included in the previous table because this right does not apply to an individual record, but instead to a class of entities. Create is handled as a privilege instead of as an access right. The user who creates a record has all rights on that record, unless his or her other privileges forbid a specific right.  
  
 The Create privilege controls whether you can create a record. If you have the Create privilege with Local, Deep, or Global access, you can create records for other users. If you have Create and Read privileges with Basic access, you can create records for yourself.  
  
 For more information about dependencies that relate to create privileges, see [Dependencies between access rights](use-record-based-security-control-access-records.md#dependencies).  
  
<a name="BKMK_SharingInstances"></a>   
## <a name="sharing-records"></a>Chia sẻ hồ sơ  
 Sharing lets users give other users or teams access to specific customer information. This is useful for sharing information with users in roles that have only the Basic access level. For example, in an organization that gives salespeople Basic read and write access to accounts, a salesperson can share an opportunity with another salesperson so that they can both track the progress of an important sale.  
  
 For security reasons, develop the practice of sharing only the necessary records with the smallest set of users possible. Only grant the minimum access required for users to do their jobs.  
  
 [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps provides the following sharing capabilities:  
  
- **Share**. Any user who has share privileges on a given entity type can share records of that type with any other user or team in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps. To share a record, use <xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>.  
  
     When you share a record with another user, indicate what access rights (Read, Write, Delete, Append, Assign, and Share) you want to grant to the other user. Access rights on a shared record can be different for each user with whom the record is shared. However, you cannot give a user any rights that he or she would not have for that type of entity, based on the role assigned to that user. For example, if a user does not have Read privileges on accounts and you share an account with that user, the user will be unable to see that account.  
  
- **Modify share**. You can modify the rights granted to a shared record after it has been shared. To modify sharing for a record, use the <xref:Microsoft.Crm.Sdk.Messages.ModifyAccessRequest>.  
  
- **Remove share**. If you share a record with another user or team, you can stop sharing the record. After you remove sharing for a record, the other user or team loses access rights to the record. To remove sharing for a record, use the <xref:Microsoft.Crm.Sdk.Messages.RevokeAccessRequest>.  
  
> [!TIP]
>  Use <xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>, <xref:Microsoft.Crm.Sdk.Messages.ModifyAccessRequest>, and <xref:Microsoft.Crm.Sdk.Messages.RevokeAccessRequest> for sharing.  
  
 A user might have access to the same record in more than one context. For example, a user might share a record directly with specific access rights, and he or she might also be on a team in which the same record is shared with different access rights. In this case, the access rights that this user has on the record are the union of all the rights.  
  
 For a list of entities that support sharing, see the <xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>.  
  
<a name="BKMK_SharingAndInheritance"></a>   
### <a name="sharing-and-inheritance"></a>Sharing and inheritance  
 If a record is created and the parent record has certain sharing properties, the new record inherits those properties. For example, Joe and Mike are working on a high priority lead. Joe creates a new lead and two activities, shares the lead with Mike, and selects cascade sharing. Mike makes a telephone call and sends an email regarding the new lead. Joe sees that Mike has contacted the company two times, so he does not make another call.  
  
 Sharing is maintained on individual records. A record inherits the sharing properties from its parent and also maintains its own sharing properties. Therefore, a record can have two sets of sharing properties—one that it has on its own and one that it inherits from its parent.  
  
 Removing the share of a parent record removes the sharing properties of objects (records) that it inherited from the parent. That is, all users who previously had visibility into this record no longer have visibility. Child objects still could be shared to some of these users if they were shared individually, not from the parent record.  
  
<a name="BKMK_AssigningRecords"></a>   
## <a name="assigning-records"></a>Đang gán bản ghi  
 Anyone with Assign privileges on a record can assign that record to another user. When a record is assigned, the new user or team becomes the owner of the record and its related records. The original user or team loses ownership of the record, but automatically shares it with the new owner.  
  
 In [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps, the system administrator can decide for an organization whether records should be shared with previous owners or not after the assign operation. If **Share with previous owner** is selected, then the previous owner shares the record with all access rights after the assign operation. Otherwise, the previous owner does not share the record and may not have access to the record, depending on his or her privileges. The `Organization.ShareRoPreviousOwnerOnAssign` attribute controls this setting.  
  
 For a list of entities that support Assign, see the <xref:Microsoft.Crm.Sdk.Messages.AssignRequest>.  
  
<a name="bkmk_retrievingaccess"></a>   
## <a name="retrieving-the-access-rights-for-a-record"></a>Retrieving the access rights for a record  
 Use the <xref:Microsoft.Crm.Sdk.Messages.RetrievePrincipalAccessRequest> message to retrieve the access rights the specified security principal (user or team) has to a record.  
  
 Use the <xref:Microsoft.Crm.Sdk.Messages.RetrieveSharedPrincipalsAndAccessRequest> message to retrieves all the security principals (users or teams) that have access to a record, together with their access rights to that record.  
  
<a name="dependencies"></a>   
## <a name="dependencies-between-access-rights"></a>Dependencies between access rights  
 Sometimes, security dependencies exist because it is necessary to have more than one access right to perform a given action. For example, if you have the **create** access right for accounts, you can create a record of the account entity type. However, unless you also have **read** access for accounts, you cannot create an account record and be the owner of that new record.  
  
 The following table lists the access right dependencies for the actions specified.  
  
|Hành động|Access rights required|  
|------------|----------------------------|  
|To **Create** a record and be the record owner|CREATE<br /><br /> READ|  
|To **Share** a record|SHARE. This right is required by the person doing the share operation.<br /><br /> READ. This right is required by the person doing the share operation and also by the person with whom the record is being shared.|  
|To **Assign** a record|ASSIGN<br /><br /> WRITE<br /><br /> READ|  
|To **Append To** a record|WRITE<br /><br />READ<br /><br /> APPENDTO|  
|To **Append** a record|WRITE<br /><br />READ<br /><br /> APPEND|  
  
 Another type of dependency exists when objects are subordinate to another object. For example, the opportunity object cannot exist on its own. Each opportunity is always attached to an account or contact. To create an opportunity, you must have the access right **appendto** on accounts and the access right **append** on opportunities.  
  
### <a name="see-also"></a>Xem thêm  
 [The Security Model of Microsoft Dynamics 365 for Customer Engagement apps](Security-model.md)   
 [How role-based security can be used to control access to entities in Microsoft Dynamics 365 for Customer Engagement apps](how-role-based-security-control-access-entities.md)  [How field security can be used to control access to field values in Microsoft Dynamics 365 for Customer Engagement apps](use-field-security-control-access-field-values.md)   
 [Introduction to Entities in Microsoft Dynamics 365 for Customer Engagement apps](../introduction-entities.md)   
 [Entity Relationship Behavior](../entity-relationship-behavior.md)   
 <xref:Microsoft.Crm.Sdk.Messages.AccessRights>   
 <xref:Microsoft.Crm.Sdk.Messages.RetrievePrincipalAccessRequest>
