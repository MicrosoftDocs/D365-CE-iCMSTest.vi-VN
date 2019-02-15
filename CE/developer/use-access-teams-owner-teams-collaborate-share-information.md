---
title: Use access teams and owner teams to collaborate and share information (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about using access teams and owner teams to colloborate and share information.
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
- owner team
- team template
- team
- access team
ms.assetid: 16f99b97-6ce5-4f65-abdd-f836dc54f9d3
caps.latest.revision: 75
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 57a4ebf3928e29e3d2408d898f0f7063fa03da23
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387664"
---
# <a name="use-access-teams-and-owner-teams-to-collaborate-and-share-information"></a>Use access teams and owner teams to collaborate and share information

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

With *owner* teams or *access* teams, you can easily share business objects and collaborate with the users across business units in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)]. A team belongs to one business unit, but it can include users from other business units. Một người dùng có thể liên kết với hơn một nhóm.  
  
 Nhóm chủ sở hữu nắm giữ bản ghi và có vai trò bảo mật được gán cho nhóm. Các đặc quyền được xác định bởi các vai trò bảo mật này. Ngoài các đặc quyền được cung cấp bởi nhóm, thành viên trong nhóm có đặc quyền được xác định bởi vai trò bảo mật cá nhân của họ và các vai trò từ các nhóm khác mà trong đó họ là thành viên. Một nhóm có đầy đủ quyền truy cập vào các bản ghi mà nhóm đó sở hữu.  
  
> [!NOTE]
>  Mặc dù nhóm cung cấp quyền truy cập vào một nhóm người dùng, bạn vẫn phải kết hợp người dùng cá nhân với các vai trò bảo mật cấp đặc quyền mà họ cần để tạo, cập nhật hoặc xóa bản ghi do người dùng sở hữu. These privileges cannot be applied by assigning security roles to a team and then adding the user to that team.  
  
 Nhóm truy cập không sở hữu các bản ghi và không có vai trò bảo mật được gán cho nhóm. Thành viên nhóm có các đặc quyền được xác định bởi vai trò bảo mật cá nhân của họ và các vai trò từ các nhóm khác mà trong đó họ là thành viên. Các bản ghi được chia sẻ với một nhóm truy cập và nhóm được cấp quyền truy cập vào các bản ghi, ví dụ như Đọc, Viết hoặc Gắn thêm.  
  
 The team functionality is supported by the `Team` entity and the `TeamTemplate` entity. The `Team` entity is used to create owner teams and user-created access teams. For auto-created access teams, the `Team` entity and the `TeamTemplate` entity are used.  
  
<a name="BKMK_OwnerAccess"></a>   
## <a name="owner-team-or-access-team"></a>Nhóm chủ sở hữu nhóm hoặc nhóm truy cập?  
 Chọn loại nhóm có thể phụ thuộc vào các mục tiêu, bản chất của dự án, và thậm chí kích thước của tổ chức của bạn. Có một vài nguyên tắc mà bạn có thể sử dụng khi lựa chọn loại nhóm.  
  
### <a name="when-to-use-owner-teams"></a>Khi nào thì sử dụng nhóm chủ sở hữu  
  
- Owning records by entities other than users is required by your company’s business policies.  
  
- Số lượng các nhóm được biết đến khi thời gian thiết kế hệ thống [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] của bạn.  
  
- Báo cáo hàng ngày về tiến trình của việc sở hữu nhóm được yêu cầu.  
  
### <a name="when-to-use-access-teams"></a>Khi nào thì sử dụng nhóm truy cập  
  
- Các nhóm được hình thành và giải thể linh hoạt. This typically happens if the clear criteria for defining the teams, such as established territory, product, or volume aren’t provided.  
  
- The number of teams isn’t known at the design time of your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] system.  
  
- Các thành viên nhóm yêu cầu quyền truy cập khác vào các hồ sơ mà nhóm sở hữu. Bạn có thể chia sẻ một hồ sơ với một số nhóm truy cập, mỗi nhóm cung cấp quyền truy cập khác nhau trên hồ sơ. For example, one team is granted the Read access right on the account and another team, the Read, Write and Share access rights on the same account.  
  
- Một tập hợp người dùng duy nhất yêu cầu quyền truy cập vào một hồ sơ duy nhất mà không cần quyền sở hữu hồ sơ.  
  
> [!NOTE]
>  Another kind of “access team” is addressed by the access team templates that are used by the web application. This is the type of team that changes often, such as a specific account record’s sales team. When a user is added to a sales team in an account, the web application, behind the scenes, creates a team specific to this record and adds the user to it.  
>   
>  This type of access team isn’t covered in this topic.  
  
<a name="BKMK_SettingUp"></a>   
## <a name="setting-up-teams"></a>Setting up teams  
 In addition to owner and access team types, the access teams are further subdivided into user-created and auto-created (system-managed) teams. The setup information is specific to each team type.  
  
### <a name="owner-team"></a>Owner team  
 An owner team can own multiple records. To create an owner team, use the `Team` entity and set the `Team.TeamType` attribute to `Owner`. For a list of the `TeamType` values, refer to the `Team` entity metadata.  
  
> [!NOTE]
> [!INCLUDE[metadata_browser](../includes/metadata-browser.md)]  
  
 To make a team an owner of the record, you have to assign a record to the team. To assign, use the <xref:Microsoft.Crm.Sdk.Messages.AssignRequest> message. To assign records to an owner team in bulk, use the <xref:Microsoft.Crm.Sdk.Messages.ReassignObjectsOwnerRequest> message or the <xref:Microsoft.Crm.Sdk.Messages.ReassignObjectsSystemUserRequest> message.  
  
 A record owned by the team must have the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.OwnershipType> property set to <xref:Microsoft.Xrm.Sdk.Metadata.OwnershipTypes>.`TeamOwned`.  
  
 If an owner team doesn’t own records and doesn’t have security roles assigned to the team, it can be converted to an access team, by using the <xref:Microsoft.Crm.Sdk.Messages.ConvertOwnerTeamToAccessTeamRequest> message. It is a one way conversion. Bạn không thể chuyển đổi nhóm truy cập trở lại thành nhóm chủ sở hữu. Trong quá trình chuyển đổi, tất cả các hàng đợi và hộp thư kết hợp với nhóm sẽ bị xóa.  
  
 To add or remove team members, use the <xref:Microsoft.Crm.Sdk.Messages.AddMembersTeamRequest> message and the <xref:Microsoft.Crm.Sdk.Messages.RemoveMembersTeamRequest> message.  
  
### <a name="user-created-access-team"></a>User-created access team  
 Bạn có thể chia sẻ nhiều bản ghi với một nhóm truy cập do người dùng tạo. To create an access team, use the team entity and set the `Team.TeamType` attribute to `Access`. For a list of the `TeamType` values, refer to the `Team` entity metadata. [!INCLUDE[view_metadata](../includes/view-metadata.md)]  
  
 To share a record with the user-created access team, use the <xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest> message. For user-created teams, the `Team.SystemManaged` attribute is `false`. For a list of the `Team.SystemManaged` values, refer to the `Team` entity metadata. [!INCLUDE[view_metadata](../includes/view-metadata.md)]  
  
 To add or remove team members, use the <xref:Microsoft.Crm.Sdk.Messages.AddMembersTeamRequest> message and the <xref:Microsoft.Crm.Sdk.Messages.RemoveMembersTeamRequest> message.  
  
 To provide the team members with different access rights on the records, create several teams and grant each team a different set of access rights on the records.  
  
### <a name="auto-created-system-managed-access-team"></a>Auto-created (system-managed) access team  
 An auto-created (system-managed) team is created for a specific record and can’t be shared with other records. For system-managed teams, you have to provide a team template. To create a template, use the team template entity. In the template, you have to specify the entity type and the access rights on the entity record, such as Read or Write that are granted to the team users when the team is created. The entity that you specify in the template must be enabled for auto created access teams. To provide the team members with different access rights on the record, create several team templates. For example, for the account entity, provide one template with the Read access right for team that only needs to view the record. Provide a second template with the Read, Write and Share access rights, for team that require more access to the same record.  
  
 To enable an entity for the auto-created access teams, set the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.AutoCreateAccessTeams> attribute to `true`.  
  
 A maximum number of team templates that you can create for an entity is specified in the <xref:Microsoft.Xrm.Sdk.Deployment.TeamSettings.MaxAutoCreatedAccessTeamsPerEntity> deployment setting. Giá trị mặc định là 2. A maximum number of entities that you can enable for auto created access teams is specified in the <xref:Microsoft.Xrm.Sdk.Deployment.TeamSettings.MaxEntitiesEnabledForAutoCreatedAccessTeams> deployment setting. Giá trị mặc định là 5. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Deployment Entities and Deployment Configuration Settings](https://msdn.microsoft.com/library/gg328063.aspx) and [Administer the deployment using Windows PowerShell](https://technet.microsoft.com/library/dn531202.aspx)  
  
 The users are automatically added and removed in the system-managed team, when you add or remove the users in a particular record by using the <xref:Microsoft.Crm.Sdk.Messages.AddUserToRecordTeamRequest> message and the <xref:Microsoft.Crm.Sdk.Messages.RemoveUserFromRecordTeamRequest> message. The actual team is created when you add the first user to the record and the team ID is returned in <xref:Microsoft.Crm.Sdk.Messages.AddUserToRecordTeamResponse.AccessTeamId>. The `Team.SystemManaged` attribute for this team is set to `true`. For a list of the `Team.SystemManaged` values, refer to the `Team` entity metadata. [!INCLUDE[view_metadata](../includes/view-metadata.md)] The caller of the message must have the Share privilege on the entity and the access rights on the record that match the access rights provided in the template. For example, if the template specifies the Read access rights, the calling user must have the Read access rights on the record. Để được thêm vào nhóm, mức truy cập tối thiểu người dùng phải có trên các thực thể xác định trong mẫu là quyền đọc cơ bản (người dùng).  
  
 Because of the parental relation between the team template and system-managed access teams, when you delete a template, all teams associated with the template are deleted according to the cascading rules.  
  
 If you change access rights for the team template, the changes are only applied to the new auto-created access teams. Các nhóm đã tồn tại không bị ảnh hưởng.  
  
<a name="BKMK_ShortSummary"></a>   
## <a name="quick-reference-to-teams"></a>Quick reference to teams  
 Use the following information as a quick reference to the available teams.  
  
|Nhóm|When to use?|What entity to use?|Use team template?|What messages to use to add or remove team members?|Owns records?|How many records owns or has access to?|Has security roles assigned?|  
|----------|------------------|-------------------------|------------------------|---------------------------------------------------------|-------------------|---------------------------------------------|----------------------------------|  
|Chủ sở hữu|Record ownership by the team is required.<br /><br /> The number of teams is known at the design time.|`Team`|Không|<xref:Microsoft.Crm.Sdk.Messages.AddMembersTeamRequest> <br /> <xref:Microsoft.Crm.Sdk.Messages.RemoveMembersTeamRequest>.|Có|Can own multiple records.|Có|  
|Access, user-created|Multiple records have to be shared with the team.<br /><br /> The number of teams isn’t known at design time.<br /><br /> Team members require different access rights on the records.|`Team`|Không|<xref:Microsoft.Crm.Sdk.Messages.AddMembersTeamRequest> <br /> <xref:Microsoft.Crm.Sdk.Messages.RemoveMembersTeamRequest>|Không|Can access multiple records.|Không. Provides access rights on the record.|  
|Access, auto-created (system-managed)|Unique set of users works on a single record.<br /><br /> Team members require different access rights on the records.<br /><br /> Creating teams automatically per record is desirable.|`TeamTemplate`<br /><br /> `Team`|Có|<xref:Microsoft.Crm.Sdk.Messages.AddUserToRecordTeamRequest> <br /> <xref:Microsoft.Crm.Sdk.Messages.RemoveUserFromRecordTeamRequest>|Không|Can access only one record.|Không. Provides access rights on the record.|  
  
> [!NOTE]
>  Owner teams and access teams provide access rights to the record and related records, such as to an account and all opportunities related to this account. In case of parental relationship between the records, cascading rules are applied. For the owner teams, you can access entities based on the roles assigned to the user plus the roles assigned to the team that a user is a member of. This allows a user to have privileges outside their business unit. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Entity Relationship Behavior](entity-relationship-behavior.md)  
> 
> [!NOTE]
>  Người dùng phải có đầy đủ đặc quyền để tham gia một nhóm truy cập. Ví dụ: nếu nhóm truy cập có quyền truy cập Xóa đối với một tài khoản, người dùng phải có đặc quyền Xóa trên đối với thực thể Tài khoản để tham gia nhóm. Nếu bạn đang cố gắng thêm người dùng không có đủ đặc quyền, bạn sẽ thấy thông báo lỗi này: "Bạn không thể thêm người dùng vào nhóm truy cập vì người dùng không có đủ đặc quyền đối với thực thể".  
  
### <a name="see-also"></a>Xem thêm  
 [Sample: Share a record using an access team](sample-share-record-using-access-team.md)   
 [Quản lý nhóm](https://technet.microsoft.com/library/dn531089.aspx)   
 [Whitepaper: Access Teams with Microsoft Dynamics CRM 2013](http://download.microsoft.com/download/E/9/0/E9009308-CA01-4B37-B03C-435B8ACB49B4/Access%20Teams%20with%20Microsoft%20Dynamics%20CRM%202013.pdf)   
 [Whitepaper: Scalable security modeling with Microsoft Dynamics CRM](http://go.microsoft.com/fwlink/p/?LinkID=328757)   
 [User and Team Entities](user-team-entities.md)   
 [Team Entity](entities/team.md)   
 [TeamTemplate Entity](entities/teamtemplate.md)   
 [Administer the deployment using Windows PowerShell](https://technet.microsoft.com/library/dn531202.aspx)   
 [Use record-based security to control access to records](security-dev/use-record-based-security-control-access-records.md)   
 [How Role-Based Security Can Be Used to Control Access to Entities In Dynamics 365 for Customer Engagement apps](security-dev/how-role-based-security-control-access-entities.md)   
 [Cascading Behavior](entity-relationship-behavior.md#BKMK_CascadingBehavior)
