---
title: Supported messages and entities for plug-ins (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: The topic contains a table that lists the message and entity combinations that support execution of plug-ins for Dynamics 365 for Customer Engagement (online) Customer Engagement.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: b3902754-0cbc-49d5-ac37-3f6f89a89e90
caps.latest.revision: 47
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7e7029609abc06fce21c79de94cebfebb07181d0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386299"
---
# <a name="supported-messages-and-entities-for-plug-ins"></a>Supported messages and entities for plug-ins

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This topic contains a table that lists the message and entity combinations that support execution of plug-ins for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].
  
 The **Message Availability** column of the table indicates whether a message is available online, offline, or both. The **Entity Deployment** column indicates if the entity can be deployed on the server, on the client, or both. A value of **null** in the **Primary Entity** column means that there is no primary entity associated with the message. The same applies to the **Secondary Entity** column.  
  
 In plug-in code, you can send any message to the web services except those messages that create or update metadata.  
  
 Custom entities support the same base messages as system entities, depending on whether the entity is organization-owned or user-owned. Để biết thêm chi tiết, xem [Hành động trên hồ sơ thực thể](introduction-entities.md#ActionsOnEntityRecords).  
  
> [!NOTE]
>  The `SDK\Message-entity support for plug-ins.xlsx` file in the download is more up-to-date than the tables provided below. Refer to that file for the latest changes.  
> 
>  The term *offline* applies to the [!INCLUDE[pn_crm_outlook_offline_access](../includes/pn-crm-outlook-offline-access.md)]. The term *client* can apply to either [!INCLUDE[pn_crm_outlook_online](../includes/pn-crm-outlook-online.md)] or [!INCLUDE[pn_crm_outlook_offline_access](../includes/pn-crm-outlook-offline-access.md)].  
> 
>  Whether a message is available online or offline can be determined programmatically by inspecting the `SdkMessage.Availability` attribute. [!INCLUDE[metadata_browser](../includes/metadata-browser.md)]  
  
<a name="orgowned"></a>   
## <a name="supported-messages-for-custom-entities"></a>Supported messages for custom entities  
 Custom entities can be either organization-owned or user-owned, which defines the set of messages available for the entity. The following table lists the messages for custom entities that support the execution of plug-ins.  
  
|**Message Name**|**Ownership Type**|**Message Availability**|**Entity Supported Deployment**|  
|----------------------|------------------------|------------------------------|-------------------------------------|  
|Chỉ định|User-owned entities only|Máy chủ|Máy chủ|  
|Tạo|User-owned and organization-owned entities|Cả hai|Máy chủ|  
|Xóa|User-owned and organization-owned entities|Cả hai|Máy chủ|  
|GrantAccess|User-owned entities only|Máy chủ|Máy chủ|  
|ModifyAccess|User-owned entities only|Máy chủ|Máy chủ|  
|Truy xuất|User-owned and organization-owned entities|Cả hai|Máy chủ|  
|RetrieveMultiple|User-owned and organization-owned entities|Cả hai|Máy chủ|  
|RetrievePrincipalAccess|User-owned entities only|Cả hai|Máy chủ|  
|RetrieveSharedPrincipalsAndAccess|User-owned entities only|Cả hai|Máy chủ|  
|RevokeAccess|User-owned entities only|Máy chủ|Máy chủ|  
|SetState|User-owned and organization-owned entities|Cả hai|Máy chủ|  
|Update|User-owned and organization-owned entities|Cả hai|Máy chủ|  
  
<a name="DefaultEntities"></a>   
## <a name="supported-messages-for-default-entities"></a>Supported messages for default entities  
 The following table lists the message and entity combinations that support the execution of plug-ins for default, or out-of-the-box entities.  
  
|**Message Name**|**Thực thể chính**|**Secondary Entity**|**Message Availability**|**Entity Supported Deployment**|  
|----------------------|------------------------|--------------------------|------------------------------|-------------------------------------|  
|AddItem|Chiến dịch||Cả hai|Cả hai|  
|AddItem|CampaignActivity||Cả hai|Cả hai|  
|AddListMembers|Danh sách||Máy chủ|Máy chủ|  
|AddMember|Danh sách||Máy chủ|Máy chủ|  
|AddMembers|Nhóm||Máy chủ|Máy chủ|  
|AddPrincipalToQueue|Hàng đợi||Cả hai|Cả hai|  
|AddPrivileges|Vai trò||Máy chủ|Máy chủ|  
|AddProductToKit|Sản phẩm||Cả hai|Cả hai|  
|AddRecurrence|RecurringAppointmentMaster||Cả hai|Cả hai|  
|AddToQueue|QueueItem||Cả hai|Cả hai|  
|AddUserToRecordTeam|Mẫu Nhóm||Máy chủ|Máy chủ|  
|ApplyRecordCreationAndUpdateRule|||Máy chủ|Máy chủ|  
|Chỉ định|Khách hàng||Máy chủ|Máy chủ|  
|Chỉ định|Annotation||Máy chủ|Máy chủ|  
|Chỉ định|Cuộc hẹn||Máy chủ|Máy chủ|  
|Chỉ định|BookableResource||Máy chủ|Máy chủ|  
|Chỉ định|BookableResourceBooking||Máy chủ|Máy chủ|  
|Chỉ định|BookableResourceBookingHeader||Máy chủ|Máy chủ|  
|Chỉ định|BookableResourceCategory||Máy chủ|Máy chủ|  
|Chỉ định|BookableResourceCategoryAssn||Máy chủ|Máy chủ|  
|Chỉ định|BookableResourceCharacteristic||Máy chủ|Máy chủ|  
|Chỉ định|BookableResourceGroup||Máy chủ|Máy chủ|  
|Chỉ định|BookingStatus||Máy chủ|Máy chủ|  
|Chỉ định|Chiến dịch||Máy chủ|Máy chủ|  
|Chỉ định|CampaignActivity||Máy chủ|Máy chủ|  
|Chỉ định|CampaignResponse||Máy chủ|Máy chủ|  
|Chỉ định|Danh mục||Máy chủ|Máy chủ|  
|Chỉ định|Đặc điểm||Máy chủ|Máy chủ|  
|Chỉ định|Connection||Máy chủ|Máy chủ|  
|Chỉ định|người liên hệ||Máy chủ|Máy chủ|  
|Chỉ định|Hợp đồng||Máy chủ|Máy chủ|  
|Chỉ định|CustomerOpportunityRole||Máy chủ|Máy chủ|  
|Chỉ định|CustomerRelationship||Máy chủ|Máy chủ|  
|Chỉ định|Email||Máy chủ|Máy chủ|  
|Chỉ định|Chữ ký Email||Máy chủ|Máy chủ|  
|Chỉ định|Quyền được hưởng||Máy chủ|Máy chủ|  
|Chỉ định|Fax||Máy chủ|Máy chủ|  
|Chỉ định|Phản hồi||Máy chủ|Máy chủ|  
|Chỉ định|Mục tiêu||Máy chủ|Máy chủ|  
|Chỉ định|GoalRollupQuery||Máy chủ|Máy chủ|  
|Chỉ định|Sự cố||Máy chủ|Máy chủ|  
|Chỉ định|IncidentResolution||Máy chủ|Máy chủ|  
|Chỉ định|Hóa đơn||Máy chủ|Máy chủ|  
|Chỉ định|KnowledgeArticle||Máy chủ|Máy chủ|  
|Chỉ định|Bản ghi Cơ sở Kiến thức||Máy chủ|Máy chủ|  
|Chỉ định|Khách hàng tiềm năng||Máy chủ|Máy chủ|  
|Chỉ định|Thư tín||Máy chủ|Máy chủ|  
|Chỉ định|Danh sách||Máy chủ|Máy chủ|  
|Chỉ định|msdyn_PostAlbum||Máy chủ|Máy chủ|  
|Chỉ định|msdyn_cài đặt người dùng truy vấn được lưu trên tường||Máy chủ|Máy chủ|  
|Chỉ định|Cơ hội||Máy chủ|Máy chủ|  
|Chỉ định|OpportunityClose||Máy chủ|Máy chủ|  
|Chỉ định|OrderClose||Máy chủ|Máy chủ|  
|Chỉ định|PersonalDocumentTemplate||Máy chủ|Máy chủ|  
|Chỉ định|Cuộc gọi Điện thoại ||Máy chủ|Máy chủ|  
|Chỉ định|ProcessSession||Máy chủ|Máy chủ|  
|Chỉ định|Hàng đợi||Máy chủ|Máy chủ|  
|Chỉ định|Báo giá||Máy chủ|Máy chủ|  
|Chỉ định|QuoteClose||Máy chủ|Máy chủ|  
|Chỉ định|RatingModel||Máy chủ|Máy chủ|  
|Chỉ định|RatingValue||Máy chủ|Máy chủ|  
|Chỉ định|RecurringAppointmentMaster||Máy chủ|Máy chủ|  
|Chỉ định|SalesOrder||Máy chủ|Máy chủ|  
|Chỉ định|ServiceAppointment||Máy chủ|Máy chủ|  
|Chỉ định|SharePointDocumentLocation||Máy chủ|Máy chủ|  
|Chỉ định|Trang SharePoint||Máy chủ|Máy chủ|  
|Chỉ định|Phiên bản KPI SLA||Máy chủ|Máy chủ|  
|Chỉ định|SocialActivity||Máy chủ|Máy chủ|  
|Chỉ định|SocialProfile||Máy chủ|Máy chủ|  
|Chỉ định|Nhiệm vụ||Máy chủ|Máy chủ|  
|Chỉ định|Mẫu||Máy chủ|Máy chủ|  
|Chỉ định|UserForm||Máy chủ|Máy chủ|  
|Chỉ định|UserQuery||Máy chủ|Máy chủ|  
|Chỉ định|UserQueryVisualization||Máy chủ|Máy chủ|  
|Liên kết|||Cả hai|Cả hai|  
|BackgroundSend|Email||Cả hai|Cả hai|  
|Book|Cuộc hẹn||Máy chủ|Máy chủ|  
|Book|RecurringAppointmentMaster||Máy chủ|Máy chủ|  
|Book|ServiceAppointment||Máy chủ|Máy chủ|  
|CalculatePrice|Hóa đơn||Cả hai|Cả hai|  
|CalculatePrice|InvoiceDetail||Cả hai|Cả hai|  
|CalculatePrice|Cơ hội||Cả hai|Cả hai|  
|CalculatePrice|OpportunityProduct||Cả hai|Cả hai|  
|CalculatePrice|Báo giá||Cả hai|Cả hai|  
|CalculatePrice|QuoteDetail||Cả hai|Cả hai|  
|CalculatePrice|SalesOrder||Cả hai|Cả hai|  
|CalculatePrice|SalesOrderDetail||Cả hai|Cả hai|  
|Hủy|Hợp đồng||Cả hai|Cả hai|  
|Hủy|SalesOrder||Cả hai|Cả hai|  
|CheckIncoming|Email||Cả hai|Cả hai|  
|CheckPromote|Email||Cả hai|Cả hai|  
|Sao y|Hợp đồng||Cả hai|Cả hai|  
|CloneMobileOfflineProfile|MobileOfflineProfile||Máy chủ|Máy chủ|  
|CloneProduct|Sản phẩm||Máy chủ|Máy chủ|  
|Đóng|Sự cố||Cả hai|Cả hai|  
|Đóng|Báo giá||Cả hai|Cả hai|  
|CopyDynamicListToStatic|Danh sách||Máy chủ|Máy chủ|  
|CopySystemForm|SystemForm||Máy chủ|Máy chủ|  
|Tạo|Khách hàng||Cả hai|Cả hai|  
|Tạo|ActionCard||Cả hai|Cả hai|  
|Tạo|ActionCardUserSettings||Cả hai|Cả hai|  
|Tạo|ActivityMimeAttachment||Cả hai|Cả hai|  
|Tạo|Annotation||Cả hai|Cả hai|  
|Tạo|Cuộc hẹn||Cả hai|Cả hai|  
|Tạo|AzureServiceConnection||Cả hai|Máy chủ|  
|Tạo|BookableResource||Cả hai|Cả hai|  
|Tạo|BookableResourceBooking||Cả hai|Cả hai|  
|Tạo|BookableResourceBookingExchangeSyncIdMapping||Cả hai|Máy chủ|  
|Tạo|BookableResourceBookingHeader||Cả hai|Cả hai|  
|Tạo|BookableResourceCategory||Cả hai|Cả hai|  
|Tạo|BookableResourceCategoryAssn||Cả hai|Cả hai|  
|Tạo|BookableResourceCharacteristic||Cả hai|Cả hai|  
|Tạo|BookableResourceGroup||Cả hai|Cả hai|  
|Tạo|BookingStatus||Cả hai|Cả hai|  
|Tạo|BusinessProcessFlowInstance||Cả hai|Cả hai|  
|Tạo|Đơn vị kinh doanh||Cả hai|Máy chủ|  
|Tạo|BusinessUnitNewsArticle||Cả hai|Cả hai|  
|Tạo|Calendar||Cả hai|Cả hai|  
|Tạo|Chiến dịch||Cả hai|Cả hai|  
|Tạo|CampaignActivity||Cả hai|Cả hai|  
|Tạo|CampaignResponse||Cả hai|Cả hai|  
|Tạo|CardType||Cả hai|Cả hai|  
|Tạo|Danh mục||Cả hai|Cả hai|  
|Tạo|Đặc điểm||Cả hai|Cả hai|  
|Tạo|Đối thủ cạnh tranh||Cả hai|Cả hai|  
|Tạo|Connection||Cả hai|Cả hai|  
|Tạo|Vai trò Kết nối||Cả hai|Cả hai|  
|Tạo|ConnectionRoleObjectTypeCode||Cả hai|Cả hai|  
|Tạo|người liên hệ||Cả hai|Cả hai|  
|Tạo|Hợp đồng||Cả hai|Cả hai|  
|Tạo|ContractDetail||Cả hai|Cả hai|  
|Tạo|ContractTemplate||Cả hai|Máy chủ|  
|Tạo|CustomControl||Cả hai|Máy chủ|  
|Tạo|CustomControlDefaultConfig||Cả hai|Máy chủ|  
|Tạo|CustomControlResource||Cả hai|Máy chủ|  
|Tạo|CustomerAddress||Cả hai|Cả hai|  
|Tạo|CustomerOpportunityRole||Cả hai|Cả hai|  
|Tạo|CustomerRelationship||Cả hai|Cả hai|  
|Tạo|Giảm giá||Cả hai|Máy chủ|  
|Tạo|DiscountType||Cả hai|Máy chủ|  
|Tạo|DocumentTemplate||Cả hai|Cả hai|  
|Tạo|Email||Cả hai|Cả hai|  
|Tạo|Chữ ký Email||Cả hai|Cả hai|  
|Tạo|Quyền được hưởng||Cả hai|Cả hai|  
|Tạo|EntitlementChannel||Cả hai|Máy chủ|  
|Tạo|EntitlementTemplate||Cả hai|Máy chủ|  
|Tạo|EntitlementTemplateChannel||Cả hai|Máy chủ|  
|Tạo|Thiết bị||Cả hai|Máy chủ|  
|Tạo|ExchangeSyncIdMapping||Cả hai|Máy chủ|  
|Tạo|ExpiredProcess||Cả hai|Cả hai|  
|Tạo|Fax||Cả hai|Cả hai|  
|Tạo|Phản hồi||Cả hai|Cả hai|  
|Tạo|Quyền của Trường||Cả hai|Máy chủ|  
|Tạo|Cấu hình Bảo mật Trường||Cả hai|Máy chủ|  
|Tạo|Mục tiêu||Cả hai|Máy chủ|  
|Tạo|GoalRollupQuery||Cả hai|Máy chủ|  
|Tạo|HierarchyRule||Cả hai|Máy chủ|  
|Tạo|HierarchySecurityConfiguration||Cả hai|Máy chủ|  
|Tạo|Sự cố||Cả hai|Cả hai|  
|Tạo|IncidentResolution||Cả hai|Cả hai|  
|Tạo|Hóa đơn||Cả hai|Cả hai|  
|Tạo|InvoiceDetail||Cả hai|Cả hai|  
|Tạo|KbArticle||Cả hai|Cả hai|  
|Tạo|KbArticleComment||Cả hai|Cả hai|  
|Tạo|KbArticleTemplate||Cả hai|Cả hai|  
|Tạo|KnowledgeArticle||Cả hai|Cả hai|  
|Tạo|KnowledgeArticleIncident||Cả hai|Cả hai|  
|Tạo|Dạng xem bài viết kiến thức||Cả hai|Cả hai|  
|Tạo|Bản ghi Cơ sở Kiến thức||Cả hai|Cả hai|  
|Tạo|Khách hàng tiềm năng||Cả hai|Cả hai|  
|Tạo|LeadToOpportunitySalesProcess||Cả hai|Cả hai|  
|Tạo|Thư tín||Cả hai|Cả hai|  
|Tạo|Danh sách||Cả hai|Cả hai|  
|Tạo|Metric||Cả hai|Máy chủ|  
|Tạo|msdyn_PostAlbum||Cả hai|Máy chủ|  
|Tạo|msdyn_PostConfig||Cả hai|Máy chủ|  
|Tạo|msdyn_PostRuleConfig||Cả hai|Máy chủ|  
|Tạo|msdyn_wallsavedquery||Cả hai|Máy chủ|  
|Tạo|msdyn_cài đặt người dùng truy vấn được lưu trên tường||Cả hai|Máy chủ|  
|Tạo|NewProcess||Cả hai|Cả hai|  
|Tạo|Cơ hội||Cả hai|Cả hai|  
|Tạo|OpportunityClose||Cả hai|Cả hai|  
|Tạo|OpportunityProduct||Cả hai|Cả hai|  
|Tạo|OpportunitySalesProcess||Cả hai|Cả hai|  
|Tạo|OrderClose||Cả hai|Cả hai|  
|Tạo|PersonalDocumentTemplate||Cả hai|Cả hai|  
|Tạo|Cuộc gọi Điện thoại ||Cả hai|Cả hai|  
|Tạo|PhoneToCaseProcess||Cả hai|Cả hai|  
|Tạo|Vị trí||Cả hai|Máy chủ|  
|Tạo|Đăng||Cả hai|Máy chủ|  
|Tạo|PostComment||Cả hai|Máy chủ|  
|Tạo|PostFollow||Cả hai|Máy chủ|  
|Tạo|PriceLevel||Cả hai|Máy chủ|  
|Tạo|PrincipalObjectAttributeAccess||Cả hai|Máy chủ|  
|Tạo|ProcessSession||Cả hai|Cả hai|  
|Tạo|Sản phẩm||Cả hai|Máy chủ|  
|Tạo|ProductAssociation||Cả hai|Cả hai|  
|Tạo|ProductPriceLevel||Cả hai|Máy chủ|  
|Tạo|ProductSubstitute||Cả hai|Cả hai|  
|Tạo|Hàng đợi||Cả hai|Máy chủ|  
|Tạo|QueueItem||Cả hai|Cả hai|  
|Tạo|Báo giá||Cả hai|Cả hai|  
|Tạo|QuoteClose||Cả hai|Cả hai|  
|Tạo|QuoteDetail||Cả hai|Cả hai|  
|Tạo|RatingModel||Cả hai|Cả hai|  
|Tạo|RatingValue||Cả hai|Cả hai|  
|Tạo|RecommendationModelVersion||Cả hai|Máy chủ|  
|Tạo|RecommendationModelVersionHistory||Cả hai|Máy chủ|  
|Tạo|RecurrenceRule||Cả hai|Máy chủ|  
|Tạo|RecurringAppointmentMaster||Cả hai|Cả hai|  
|Tạo|Vai trò||Cả hai|Máy chủ|  
|Tạo|Trường tổng số||Cả hai|Máy chủ|  
|Tạo|SalesLiterature||Cả hai|Máy chủ|  
|Tạo|SalesLiteratureItem||Cả hai|Máy chủ|  
|Tạo|SalesOrder||Cả hai|Cả hai|  
|Tạo|SalesOrderDetail||Cả hai|Cả hai|  
|Tạo|Dịch vụ ||Cả hai|Máy chủ|  
|Tạo|ServiceAppointment||Cả hai|Cả hai|  
|Tạo|Tài liệu SharePoint||Cả hai|Cả hai|  
|Tạo|SharePointDocumentLocation||Cả hai|Máy chủ|  
|Tạo|Trang SharePoint||Cả hai|Máy chủ|  
|Tạo|SimilarityRule||Cả hai|Cả hai|  
|Tạo|Trang||Cả hai|Máy chủ|  
|Tạo|Phiên bản KPI SLA||Cả hai|Cả hai|  
|Tạo|SocialActivity||Cả hai|Cả hai|  
|Tạo|SocialProfile||Cả hai|Cả hai|  
|Tạo|Chủ đề||Cả hai|Cả hai|  
|Tạo|Người dùng hệ thống||Cả hai|Máy chủ|  
|Tạo|Nhiệm vụ||Cả hai|Cả hai|  
|Tạo|Nhóm||Cả hai|Máy chủ|  
|Tạo|Mẫu||Cả hai|Cả hai|  
|Tạo|Vùng lãnh thổ||Cả hai|Máy chủ|  
|Tạo|TextAnalyticsEntityMapping||Cả hai|Máy chủ|  
|Tạo|Chủ đề||Cả hai|Cả hai|  
|Tạo|TopicModelConfiguration||Cả hai|Cả hai|  
|Tạo|TraceLog||Cả hai|Cả hai|  
|Tạo|TransactionCurrency||Cả hai|Máy chủ|  
|Tạo|TranslationProcess||Cả hai|Cả hai|  
|Tạo|UoM||Cả hai|Máy chủ|  
|Tạo|UoMSchedule||Cả hai|Cả hai|  
|Tạo|UserMapping||Cả hai|Cả hai|  
|Tạo|UserQuery||Cả hai|Cả hai|  
|Tạo|WebResource||Cả hai|Máy chủ|  
|CreateException|Cuộc hẹn||Cả hai|Cả hai|  
|Tạo phiên bản|RecurringAppointmentMaster||Máy chủ|Máy chủ|  
|CreateKnowledgeArticleTranslation|KnowledgeArticle||Cả hai|Cả hai|  
|CreateKnowledgeArticleVersion|KnowledgeArticle||Cả hai|Cả hai|  
|Xóa|Khách hàng||Cả hai|Cả hai|  
|Xóa|ActionCard||Cả hai|Cả hai|  
|Xóa|ActivityMimeAttachment||Cả hai|Cả hai|  
|Xóa|Annotation||Cả hai|Cả hai|  
|Xóa|Cuộc hẹn||Cả hai|Cả hai|  
|Xóa|AzureServiceConnection||Cả hai|Máy chủ|  
|Xóa|BookableResource||Cả hai|Cả hai|  
|Xóa|BookableResourceBooking||Cả hai|Cả hai|  
|Xóa|BookableResourceBookingExchangeSyncIdMapping||Cả hai|Máy chủ|  
|Xóa|BookableResourceBookingHeader||Cả hai|Cả hai|  
|Xóa|BookableResourceCategory||Cả hai|Cả hai|  
|Xóa|BookableResourceCategoryAssn||Cả hai|Cả hai|  
|Xóa|BookableResourceCharacteristic||Cả hai|Cả hai|  
|Xóa|BookableResourceGroup||Cả hai|Cả hai|  
|Xóa|BookingStatus||Cả hai|Cả hai|  
|Xóa|Đơn vị kinh doanh||Cả hai|Máy chủ|  
|Xóa|BusinessUnitNewsArticle||Cả hai|Cả hai|  
|Xóa|Calendar||Cả hai|Cả hai|  
|Xóa|Chiến dịch||Cả hai|Cả hai|  
|Xóa|CampaignActivity||Cả hai|Cả hai|  
|Xóa|CampaignResponse||Cả hai|Cả hai|  
|Xóa|CardType||Cả hai|Cả hai|  
|Xóa|Danh mục||Cả hai|Cả hai|  
|Xóa|Đặc điểm||Cả hai|Cả hai|  
|Xóa|Đối thủ cạnh tranh||Cả hai|Cả hai|  
|Xóa|Connection||Cả hai|Cả hai|  
|Xóa|Vai trò Kết nối||Cả hai|Cả hai|  
|Xóa|ConnectionRoleObjectTypeCode||Cả hai|Cả hai|  
|Xóa|người liên hệ||Cả hai|Cả hai|  
|Xóa|Hợp đồng||Cả hai|Máy chủ|  
|Xóa|ContractDetail||Cả hai|Máy chủ|  
|Xóa|ContractTemplate||Cả hai|Máy chủ|  
|Xóa|CustomControl||Cả hai|Máy chủ|  
|Xóa|CustomControlDefaultConfig||Cả hai|Máy chủ|  
|Xóa|CustomControlResource||Cả hai|Máy chủ|  
|Xóa|CustomerAddress||Cả hai|Cả hai|  
|Xóa|CustomerOpportunityRole||Cả hai|Cả hai|  
|Xóa|CustomerRelationship||Cả hai|Cả hai|  
|Xóa|Giảm giá||Cả hai|Máy chủ|  
|Xóa|DiscountType||Cả hai|Máy chủ|  
|Xóa|Email||Cả hai|Cả hai|  
|Xóa|Chữ ký Email||Cả hai|Cả hai|  
|Xóa|Quyền được hưởng||Cả hai|Máy chủ|  
|Xóa|EntitlementChannel||Cả hai|Máy chủ|  
|Xóa|EntitlementTemplate||Cả hai|Máy chủ|  
|Xóa|EntitlementTemplateChannel||Cả hai|Máy chủ|  
|Xóa|Thiết bị||Cả hai|Máy chủ|  
|Xóa|ExchangeSyncIdMapping||Cả hai|Máy chủ|  
|Xóa|ExpiredProcess||Cả hai|Cả hai|  
|Xóa|Fax||Cả hai|Cả hai|  
|Xóa|Phản hồi||Cả hai|Cả hai|  
|Xóa|Quyền của Trường||Cả hai|Máy chủ|  
|Xóa|Cấu hình Bảo mật Trường||Cả hai|Máy chủ|  
|Xóa|Mục tiêu||Cả hai|Máy chủ|  
|Xóa|GoalRollupQuery||Cả hai|Máy chủ|  
|Xóa|HierarchyRule||Cả hai|Máy chủ|  
|Xóa|HierarchySecurityConfiguration||Cả hai|Máy chủ|  
|Xóa|Sự cố||Cả hai|Cả hai|  
|Xóa|IncidentResolution||Cả hai|Cả hai|  
|Xóa|Hóa đơn||Cả hai|Cả hai|  
|Xóa|InvoiceDetail||Cả hai|Cả hai|  
|Xóa|KbArticle||Cả hai|Cả hai|  
|Xóa|KbArticleComment||Cả hai|Cả hai|  
|Xóa|KbArticleTemplate||Cả hai|Cả hai|  
|Xóa|KnowledgeArticle||Cả hai|Cả hai|  
|Xóa|KnowledgeArticleIncident||Cả hai|Cả hai|  
|Xóa|Dạng xem bài viết kiến thức||Cả hai|Cả hai|  
|Xóa|Bản ghi Cơ sở Kiến thức||Cả hai|Cả hai|  
|Xóa|Khách hàng tiềm năng||Cả hai|Cả hai|  
|Xóa|LeadToOpportunitySalesProcess||Cả hai|Cả hai|  
|Xóa|Thư tín||Cả hai|Cả hai|  
|Xóa|Danh sách||Cả hai|Máy chủ|  
|Xóa|Metric||Cả hai|Máy chủ|  
|Xóa|msdyn_PostAlbum||Cả hai|Máy chủ|  
|Xóa|msdyn_PostConfig||Cả hai|Máy chủ|  
|Xóa|msdyn_PostRuleConfig||Cả hai|Máy chủ|  
|Xóa|msdyn_wallsavedquery||Cả hai|Máy chủ|  
|Xóa|msdyn_cài đặt người dùng truy vấn được lưu trên tường||Cả hai|Máy chủ|  
|Xóa|NewProcess||Cả hai|Cả hai|  
|Xóa|Cơ hội||Cả hai|Cả hai|  
|Xóa|OpportunityClose||Cả hai|Cả hai|  
|Xóa|OpportunityProduct||Cả hai|Cả hai|  
|Xóa|OpportunitySalesProcess||Cả hai|Cả hai|  
|Xóa|OrderClose||Cả hai|Cả hai|  
|Xóa|Cuộc gọi Điện thoại ||Cả hai|Cả hai|  
|Xóa|PhoneToCaseProcess||Cả hai|Cả hai|  
|Xóa|PluginTraceLog||Cả hai|Cả hai|  
|Xóa|Vị trí||Cả hai|Máy chủ|  
|Xóa|Đăng||Cả hai|Máy chủ|  
|Xóa|PostComment||Cả hai|Máy chủ|  
|Xóa|PostFollow||Cả hai|Máy chủ|  
|Xóa|PostLike||Cả hai|Máy chủ|  
|Xóa|PriceLevel||Cả hai|Cả hai|  
|Xóa|PrincipalObjectAttributeAccess||Cả hai|Máy chủ|  
|Xóa|ProcessSession||Cả hai|Cả hai|  
|Xóa|Sản phẩm||Cả hai|Cả hai|  
|Xóa|ProductAssociation||Cả hai|Cả hai|  
|Xóa|ProductPriceLevel||Cả hai|Cả hai|  
|Xóa|ProductSubstitute||Cả hai|Cả hai|  
|Xóa|Nhà phát hành||Cả hai|Máy chủ|  
|Xóa|PublisherAddress||Cả hai|Máy chủ|  
|Xóa|Hàng đợi||Cả hai|Máy chủ|  
|Xóa|QueueItem||Cả hai|Cả hai|  
|Xóa|Báo giá||Cả hai|Cả hai|  
|Xóa|QuoteClose||Cả hai|Cả hai|  
|Xóa|QuoteDetail||Cả hai|Cả hai|  
|Xóa|RatingModel||Cả hai|Cả hai|  
|Xóa|RatingValue||Cả hai|Cả hai|  
|Xóa|RecommendationModelVersionHistory||Cả hai|Máy chủ|  
|Xóa|RecurrenceRule||Cả hai|Cả hai|  
|Xóa|RecurringAppointmentMaster||Cả hai|Cả hai|  
|Xóa|Vai trò||Cả hai|Máy chủ|  
|Xóa|Trường tổng số||Cả hai|Máy chủ|  
|Xóa|SalesLiterature||Cả hai|Máy chủ|  
|Xóa|SalesLiteratureItem||Cả hai|Máy chủ|  
|Xóa|SalesOrder||Cả hai|Cả hai|  
|Xóa|SalesOrderDetail||Cả hai|Cả hai|  
|Xóa|Dịch vụ ||Cả hai|Máy chủ|  
|Xóa|ServiceAppointment||Cả hai|Cả hai|  
|Xóa|Tài liệu SharePoint||Cả hai|Cả hai|  
|Xóa|SharePointDocumentLocation||Cả hai|Máy chủ|  
|Xóa|Trang SharePoint||Cả hai|Máy chủ|  
|Xóa|SimilarityRule||Cả hai|Cả hai|  
|Xóa|Trang||Cả hai|Máy chủ|  
|Xóa|SiteMap||Cả hai|Cả hai|  
|Xóa|SocialActivity||Cả hai|Cả hai|  
|Xóa|SocialProfile||Cả hai|Cả hai|  
|Xóa|Giải pháp||Cả hai|Máy chủ|  
|Xóa|Chủ đề||Cả hai|Cả hai|  
|Xóa|Nhiệm vụ||Cả hai|Cả hai|  
|Xóa|Nhóm||Cả hai|Máy chủ|  
|Xóa|Mẫu||Cả hai|Cả hai|  
|Xóa|Vùng lãnh thổ||Cả hai|Máy chủ|  
|Xóa|TextAnalyticsEntityMapping||Cả hai|Máy chủ|  
|Xóa|Chủ đề||Cả hai|Cả hai|  
|Xóa|TopicModelConfiguration||Cả hai|Cả hai|  
|Xóa|TransactionCurrency||Cả hai|Máy chủ|  
|Xóa|TranslationProcess||Cả hai|Cả hai|  
|Xóa|UoM||Cả hai|Máy chủ|  
|Xóa|UoMSchedule||Cả hai|Cả hai|  
|Xóa|UserForm||Cả hai|Máy chủ|  
|Xóa|UserMapping||Cả hai|Cả hai|  
|Xóa|UserQuery||Cả hai|Cả hai|  
|Xóa|UserQueryVisualization||Cả hai|Cả hai|  
|Xóa|WebResource||Cả hai|Máy chủ|  
|DeleteOpenInstances|RecurringAppointmentMaster||Cả hai|Cả hai|  
|DeliverIncoming|Email||Máy chủ|Máy chủ|  
|DeliverPromote|Email||Cả hai|Cả hai|  
|Dừng liên kết|||Cả hai|Cả hai|  
|Thực thi|||Cả hai|Cả hai|  
|ExecuteById|Yêu cầu đã lưu||Cả hai|Cả hai|  
|ExecuteById|UserQuery||Cả hai|Cả hai|  
|Xuất|||Máy chủ|Máy chủ|  
|GenerateSocialProfile|SocialProfile||Cả hai|Cả hai|  
|GetDefaultPriceLevel|||Cả hai|Cả hai|  
|GrantAccess|Khách hàng||Máy chủ|Máy chủ|  
|GrantAccess|Annotation||Máy chủ|Máy chủ|  
|GrantAccess|Cuộc hẹn||Máy chủ|Máy chủ|  
|GrantAccess|BookableResource||Máy chủ|Máy chủ|  
|GrantAccess|BookableResourceBooking||Máy chủ|Máy chủ|  
|GrantAccess|BookableResourceBookingHeader||Máy chủ|Máy chủ|  
|GrantAccess|BookableResourceCategory||Máy chủ|Máy chủ|  
|GrantAccess|BookableResourceCategoryAssn||Máy chủ|Máy chủ|  
|GrantAccess|BookableResourceCharacteristic||Máy chủ|Máy chủ|  
|GrantAccess|BookableResourceGroup||Máy chủ|Máy chủ|  
|GrantAccess|BookingStatus||Máy chủ|Máy chủ|  
|GrantAccess|Chiến dịch||Máy chủ|Máy chủ|  
|GrantAccess|CampaignActivity||Máy chủ|Máy chủ|  
|GrantAccess|CampaignResponse||Máy chủ|Máy chủ|  
|GrantAccess|Danh mục||Máy chủ|Máy chủ|  
|GrantAccess|Đặc điểm||Máy chủ|Máy chủ|  
|GrantAccess|Connection||Máy chủ|Máy chủ|  
|GrantAccess|người liên hệ||Máy chủ|Máy chủ|  
|GrantAccess|Hợp đồng||Máy chủ|Máy chủ|  
|GrantAccess|CustomerOpportunityRole||Máy chủ|Máy chủ|  
|GrantAccess|CustomerRelationship||Máy chủ|Máy chủ|  
|GrantAccess|Email||Máy chủ|Máy chủ|  
|GrantAccess|Quyền được hưởng||Máy chủ|Máy chủ|  
|GrantAccess|Fax||Máy chủ|Máy chủ|  
|GrantAccess|Phản hồi||Máy chủ|Máy chủ|  
|GrantAccess|Mục tiêu||Máy chủ|Máy chủ|  
|GrantAccess|GoalRollupQuery||Máy chủ|Máy chủ|  
|GrantAccess|Sự cố||Máy chủ|Máy chủ|  
|GrantAccess|IncidentResolution||Máy chủ|Máy chủ|  
|GrantAccess|Hóa đơn||Máy chủ|Máy chủ|  
|GrantAccess|KnowledgeArticle||Máy chủ|Máy chủ|  
|GrantAccess|Bản ghi Cơ sở Kiến thức||Máy chủ|Máy chủ|  
|GrantAccess|Khách hàng tiềm năng||Máy chủ|Máy chủ|  
|GrantAccess|Thư tín||Máy chủ|Máy chủ|  
|GrantAccess|Danh sách||Máy chủ|Máy chủ|  
|GrantAccess|msdyn_PostAlbum||Máy chủ|Máy chủ|  
|GrantAccess|msdyn_cài đặt người dùng truy vấn được lưu trên tường||Máy chủ|Máy chủ|  
|GrantAccess|Cơ hội||Máy chủ|Máy chủ|  
|GrantAccess|OpportunityClose||Máy chủ|Máy chủ|  
|GrantAccess|OrderClose||Máy chủ|Máy chủ|  
|GrantAccess|PersonalDocumentTemplate||Máy chủ|Máy chủ|  
|GrantAccess|Cuộc gọi Điện thoại ||Máy chủ|Máy chủ|  
|GrantAccess|ProcessSession||Máy chủ|Máy chủ|  
|GrantAccess|Hàng đợi||Máy chủ|Máy chủ|  
|GrantAccess|Báo giá||Máy chủ|Máy chủ|  
|GrantAccess|QuoteClose||Máy chủ|Máy chủ|  
|GrantAccess|RatingModel||Máy chủ|Máy chủ|  
|GrantAccess|RatingValue||Máy chủ|Máy chủ|  
|GrantAccess|RecurringAppointmentMaster||Máy chủ|Máy chủ|  
|GrantAccess|SalesOrder||Máy chủ|Máy chủ|  
|GrantAccess|ServiceAppointment||Máy chủ|Máy chủ|  
|GrantAccess|SharePointDocumentLocation||Máy chủ|Máy chủ|  
|GrantAccess|Trang SharePoint||Máy chủ|Máy chủ|  
|GrantAccess|Phiên bản KPI SLA||Máy chủ|Máy chủ|  
|GrantAccess|SocialActivity||Máy chủ|Máy chủ|  
|GrantAccess|SocialProfile||Máy chủ|Máy chủ|  
|GrantAccess|Nhiệm vụ||Máy chủ|Máy chủ|  
|GrantAccess|Mẫu||Máy chủ|Máy chủ|  
|GrantAccess|UserForm||Máy chủ|Máy chủ|  
|GrantAccess|UserQuery||Máy chủ|Máy chủ|  
|GrantAccess|UserQueryVisualization||Máy chủ|Máy chủ|  
|Nhập|||Máy chủ|Máy chủ|  
|LockInvoicePricing|Hóa đơn||Máy chủ|Máy chủ|  
|LockSalesOrderPricing|SalesOrder||Máy chủ|Máy chủ|  
|Lose|Cơ hội||Cả hai|Cả hai|  
|Hợp nhất|Khách hàng||Máy chủ|Máy chủ|  
|Hợp nhất|người liên hệ||Máy chủ|Máy chủ|  
|Hợp nhất|Sự cố||Máy chủ|Máy chủ|  
|Hợp nhất|Khách hàng tiềm năng||Máy chủ|Máy chủ|  
|ModifyAccess|Khách hàng||Máy chủ|Máy chủ|  
|ModifyAccess|Annotation||Máy chủ|Máy chủ|  
|ModifyAccess|Cuộc hẹn||Máy chủ|Máy chủ|  
|ModifyAccess|BookableResource||Máy chủ|Máy chủ|  
|ModifyAccess|BookableResourceBooking||Máy chủ|Máy chủ|  
|ModifyAccess|BookableResourceBookingHeader||Máy chủ|Máy chủ|  
|ModifyAccess|BookableResourceCategory||Máy chủ|Máy chủ|  
|ModifyAccess|BookableResourceCategoryAssn||Máy chủ|Máy chủ|  
|ModifyAccess|BookableResourceCharacteristic||Máy chủ|Máy chủ|  
|ModifyAccess|BookableResourceGroup||Máy chủ|Máy chủ|  
|ModifyAccess|BookingStatus||Máy chủ|Máy chủ|  
|ModifyAccess|Chiến dịch||Máy chủ|Máy chủ|  
|ModifyAccess|CampaignActivity||Máy chủ|Máy chủ|  
|ModifyAccess|CampaignResponse||Máy chủ|Máy chủ|  
|ModifyAccess|Đặc điểm||Máy chủ|Máy chủ|  
|ModifyAccess|Connection||Máy chủ|Máy chủ|  
|ModifyAccess|người liên hệ||Máy chủ|Máy chủ|  
|ModifyAccess|Hợp đồng||Máy chủ|Máy chủ|  
|ModifyAccess|CustomerOpportunityRole||Máy chủ|Máy chủ|  
|ModifyAccess|CustomerRelationship||Máy chủ|Máy chủ|  
|ModifyAccess|Email||Máy chủ|Máy chủ|  
|ModifyAccess|Quyền được hưởng||Máy chủ|Máy chủ|  
|ModifyAccess|Fax||Máy chủ|Máy chủ|  
|ModifyAccess|Phản hồi||Máy chủ|Máy chủ|  
|ModifyAccess|Mục tiêu||Máy chủ|Máy chủ|  
|ModifyAccess|GoalRollupQuery||Máy chủ|Máy chủ|  
|ModifyAccess|Sự cố||Máy chủ|Máy chủ|  
|ModifyAccess|IncidentResolution||Máy chủ|Máy chủ|  
|ModifyAccess|Hóa đơn||Máy chủ|Máy chủ|  
|ModifyAccess|KnowledgeArticle||Máy chủ|Máy chủ|  
|ModifyAccess|Bản ghi Cơ sở Kiến thức||Máy chủ|Máy chủ|  
|ModifyAccess|Khách hàng tiềm năng||Máy chủ|Máy chủ|  
|ModifyAccess|Thư tín||Máy chủ|Máy chủ|  
|ModifyAccess|Danh sách||Máy chủ|Máy chủ|  
|ModifyAccess|msdyn_PostAlbum||Máy chủ|Máy chủ|  
|ModifyAccess|msdyn_cài đặt người dùng truy vấn được lưu trên tường||Máy chủ|Máy chủ|  
|ModifyAccess|Cơ hội||Máy chủ|Máy chủ|  
|ModifyAccess|OpportunityClose||Máy chủ|Máy chủ|  
|ModifyAccess|OrderClose||Máy chủ|Máy chủ|  
|ModifyAccess|PersonalDocumentTemplate||Máy chủ|Máy chủ|  
|ModifyAccess|Cuộc gọi Điện thoại ||Máy chủ|Máy chủ|  
|ModifyAccess|ProcessSession||Máy chủ|Máy chủ|  
|ModifyAccess|Hàng đợi||Máy chủ|Máy chủ|  
|ModifyAccess|Báo giá||Máy chủ|Máy chủ|  
|ModifyAccess|QuoteClose||Máy chủ|Máy chủ|  
|ModifyAccess|RatingModel||Máy chủ|Máy chủ|  
|ModifyAccess|RatingValue||Máy chủ|Máy chủ|  
|ModifyAccess|RecurringAppointmentMaster||Máy chủ|Máy chủ|  
|ModifyAccess|SalesOrder||Máy chủ|Máy chủ|  
|ModifyAccess|ServiceAppointment||Máy chủ|Máy chủ|  
|ModifyAccess|SharePointDocumentLocation||Máy chủ|Máy chủ|  
|ModifyAccess|Trang SharePoint||Máy chủ|Máy chủ|  
|ModifyAccess|Phiên bản KPI SLA||Máy chủ|Máy chủ|  
|ModifyAccess|SocialActivity||Máy chủ|Máy chủ|  
|ModifyAccess|SocialProfile||Máy chủ|Máy chủ|  
|ModifyAccess|Nhiệm vụ||Máy chủ|Máy chủ|  
|ModifyAccess|Mẫu||Máy chủ|Máy chủ|  
|ModifyAccess|UserForm||Máy chủ|Máy chủ|  
|ModifyAccess|UserQuery||Máy chủ|Máy chủ|  
|ModifyAccess|UserQueryVisualization||Máy chủ|Máy chủ|  
|PickFromQueue|QueueItem||Cả hai|Cả hai|  
|Phát hành|||Máy chủ|Máy chủ|  
|PublishAll|||Máy chủ|Máy chủ|  
|PublishTheme|Chủ đề||Máy chủ|Máy chủ|  
|QualifyLead|Khách hàng tiềm năng||Cả hai|Cả hai|  
|Recalculate|Mục tiêu||Máy chủ|Máy chủ|  
|ReleaseToQueue|QueueItem||Cả hai|Cả hai|  
|RemoveFromQueue|QueueItem||Cả hai|Cả hai|  
|RemoveItem|Chiến dịch||Cả hai|Cả hai|  
|RemoveItem|CampaignActivity||Cả hai|Cả hai|  
|RemoveMember|Danh sách||Máy chủ|Máy chủ|  
|RemoveMembers|Nhóm||Máy chủ|Máy chủ|  
|RemovePrivilege|Vai trò||Máy chủ|Máy chủ|  
|RemoveProductFromKit|||Cả hai|Cả hai|  
|RemoveRelated|Hóa đơn|người liên hệ|Cả hai|Cả hai|  
|RemoveRelated|Khách hàng tiềm năng|Khách hàng|Cả hai|Cả hai|  
|RemoveRelated|Khách hàng tiềm năng|người liên hệ|Cả hai|Cả hai|  
|RemoveRelated|Cơ hội|Khách hàng|Cả hai|Cả hai|  
|RemoveRelated|Cơ hội|Đối thủ cạnh tranh|Cả hai|Cả hai|  
|RemoveRelated|Cơ hội|người liên hệ|Cả hai|Cả hai|  
|RemoveRelated|Sản phẩm|Đối thủ cạnh tranh|Cả hai|Cả hai|  
|RemoveRelated|Sản phẩm|Khách hàng tiềm năng|Cả hai|Cả hai|  
|RemoveRelated|Báo giá|người liên hệ|Cả hai|Cả hai|  
|RemoveRelated|SalesLiterature|Đối thủ cạnh tranh|Cả hai|Cả hai|  
|RemoveRelated|SalesLiterature|Sản phẩm|Cả hai|Cả hai|  
|RemoveRelated|SalesOrder|người liên hệ|Cả hai|Cả hai|  
|RemoveUserFromRecordTeam|Mẫu Nhóm||Máy chủ|Máy chủ|  
|ReplacePrivileges|Vai trò||Máy chủ|Máy chủ|  
|Reschedule|Cuộc hẹn||Máy chủ|Máy chủ|  
|Reschedule|RecurringAppointmentMaster||Máy chủ|Máy chủ|  
|Reschedule|ServiceAppointment||Máy chủ|Máy chủ|  
|Truy xuất|Khách hàng||Cả hai|Cả hai|  
|Truy xuất|ActionCard||Cả hai|Cả hai|  
|Truy xuất|ActivityMimeAttachment||Cả hai|Cả hai|  
|Truy xuất|ActivityPointer||Cả hai|Cả hai|  
|Truy xuất|Annotation||Cả hai|Cả hai|  
|Truy xuất|AppModuleComponent||Cả hai|Cả hai|  
|Truy xuất|Cuộc hẹn||Cả hai|Cả hai|  
|Truy xuất|AzureServiceConnection||Cả hai|Cả hai|  
|Truy xuất|BookableResource||Cả hai|Cả hai|  
|Truy xuất|BookableResourceBooking||Cả hai|Cả hai|  
|Truy xuất|BookableResourceBookingExchangeSyncIdMapping||Cả hai|Máy chủ|  
|Truy xuất|BookableResourceBookingHeader||Cả hai|Cả hai|  
|Truy xuất|BookableResourceCategory||Cả hai|Cả hai|  
|Truy xuất|BookableResourceCategoryAssn||Cả hai|Cả hai|  
|Truy xuất|BookableResourceCharacteristic||Cả hai|Cả hai|  
|Truy xuất|BookableResourceGroup||Cả hai|Cả hai|  
|Truy xuất|BookingStatus||Cả hai|Cả hai|  
|Truy xuất|BusinessUnitNewsArticle||Cả hai|Cả hai|  
|Truy xuất|Calendar||Cả hai|Cả hai|  
|Truy xuất|Chiến dịch||Cả hai|Cả hai|  
|Truy xuất|CampaignActivity||Cả hai|Cả hai|  
|Truy xuất|CampaignResponse||Cả hai|Cả hai|  
|Truy xuất|CardType||Cả hai|Cả hai|  
|Truy xuất|Danh mục||Cả hai|Cả hai|  
|Truy xuất|Đặc điểm||Cả hai|Cả hai|  
|Truy xuất|Đối thủ cạnh tranh||Cả hai|Cả hai|  
|Truy xuất|Connection||Cả hai|Cả hai|  
|Truy xuất|Vai trò Kết nối||Cả hai|Cả hai|  
|Truy xuất|ConnectionRoleObjectTypeCode||Cả hai|Cả hai|  
|Truy xuất|người liên hệ||Cả hai|Cả hai|  
|Truy xuất|Hợp đồng||Cả hai|Cả hai|  
|Truy xuất|ContractDetail||Cả hai|Cả hai|  
|Truy xuất|ContractTemplate||Cả hai|Cả hai|  
|Truy xuất|CustomControl||Cả hai|Cả hai|  
|Truy xuất|CustomControlDefaultConfig||Cả hai|Cả hai|  
|Truy xuất|CustomControlResource||Cả hai|Cả hai|  
|Truy xuất|CustomerAddress||Cả hai|Cả hai|  
|Truy xuất|CustomerOpportunityRole||Cả hai|Cả hai|  
|Truy xuất|CustomerRelationship||Cả hai|Cả hai|  
|Truy xuất|Dependency||Cả hai|Máy chủ|  
|Truy xuất|Giảm giá||Cả hai|Cả hai|  
|Truy xuất|DiscountType||Cả hai|Cả hai|  
|Truy xuất|DocumentTemplate||Cả hai|Cả hai|  
|Truy xuất|Email||Cả hai|Cả hai|  
|Truy xuất|Chữ ký Email||Cả hai|Cả hai|  
|Truy xuất|Quyền được hưởng||Cả hai|Cả hai|  
|Truy xuất|EntitlementChannel||Cả hai|Cả hai|  
|Truy xuất|EntitlementTemplate||Cả hai|Cả hai|  
|Truy xuất|EntitlementTemplateChannel||Cả hai|Cả hai|  
|Truy xuất|Thiết bị||Cả hai|Cả hai|  
|Truy xuất|ExchangeSyncIdMapping||Cả hai|Máy chủ|  
|Truy xuất|Fax||Cả hai|Cả hai|  
|Truy xuất|Phản hồi||Cả hai|Cả hai|  
|Truy xuất|Mục tiêu||Cả hai|Cả hai|  
|Truy xuất|GoalRollupQuery||Cả hai|Cả hai|  
|Truy xuất|HierarchyRule||Cả hai|Cả hai|  
|Truy xuất|Sự cố||Cả hai|Cả hai|  
|Truy xuất|IncidentResolution||Cả hai|Cả hai|  
|Truy xuất|InvalidDependency||Cả hai|Máy chủ|  
|Truy xuất|Hóa đơn||Cả hai|Cả hai|  
|Truy xuất|InvoiceDetail||Cả hai|Cả hai|  
|Truy xuất|KbArticle||Cả hai|Cả hai|  
|Truy xuất|KbArticleComment||Cả hai|Cả hai|  
|Truy xuất|KbArticleTemplate||Cả hai|Cả hai|  
|Truy xuất|KnowledgeArticle||Cả hai|Cả hai|  
|Truy xuất|KnowledgeArticleIncident||Cả hai|Cả hai|  
|Truy xuất|Dạng xem bài viết kiến thức||Cả hai|Cả hai|  
|Truy xuất|Bản ghi Cơ sở Kiến thức||Cả hai|Cả hai|  
|Truy xuất|LanguageLocale||Cả hai|Cả hai|  
|Truy xuất|Khách hàng tiềm năng||Cả hai|Cả hai|  
|Truy xuất|LeadAddress||Cả hai|Cả hai|  
|Truy xuất|Thư tín||Cả hai|Cả hai|  
|Truy xuất|Danh sách||Cả hai|Cả hai|  
|Truy xuất|Metric||Cả hai|Cả hai|  
|Truy xuất|msdyn_PostAlbum||Cả hai|Máy chủ|  
|Truy xuất|msdyn_PostConfig||Cả hai|Máy chủ|  
|Truy xuất|msdyn_PostRuleConfig||Cả hai|Máy chủ|  
|Truy xuất|msdyn_wallsavedquery||Cả hai|Máy chủ|  
|Truy xuất|msdyn_cài đặt người dùng truy vấn được lưu trên tường||Cả hai|Máy chủ|  
|Truy xuất|Cơ hội||Cả hai|Cả hai|  
|Truy xuất|OpportunityClose||Cả hai|Cả hai|  
|Truy xuất|OpportunityProduct||Cả hai|Cả hai|  
|Truy xuất|OrderClose||Cả hai|Cả hai|  
|Truy xuất|PersonalDocumentTemplate||Cả hai|Cả hai|  
|Truy xuất|Cuộc gọi Điện thoại ||Cả hai|Cả hai|  
|Truy xuất|PluginTraceLog||Cả hai|Cả hai|  
|Truy xuất|Vị trí||Cả hai|Cả hai|  
|Truy xuất|Đăng||Cả hai|Máy chủ|  
|Truy xuất|PostComment||Cả hai|Máy chủ|  
|Truy xuất|PostFollow||Cả hai|Máy chủ|  
|Truy xuất|PostLike||Cả hai|Máy chủ|  
|Truy xuất|PriceLevel||Cả hai|Cả hai|  
|Truy xuất|ProcessSession||Cả hai|Cả hai|  
|Truy xuất|Sản phẩm||Cả hai|Cả hai|  
|Truy xuất|ProductAssociation||Cả hai|Cả hai|  
|Truy xuất|ProductPriceLevel||Cả hai|Cả hai|  
|Truy xuất|ProductSubstitute||Cả hai|Cả hai|  
|Truy xuất|Nhà phát hành||Cả hai|Cả hai|  
|Truy xuất|PublisherAddress||Cả hai|Máy chủ|  
|Truy xuất|Hàng đợi||Cả hai|Cả hai|  
|Truy xuất|Báo giá||Cả hai|Cả hai|  
|Truy xuất|QuoteClose||Cả hai|Cả hai|  
|Truy xuất|QuoteDetail||Cả hai|Cả hai|  
|Truy xuất|RatingModel||Cả hai|Cả hai|  
|Truy xuất|RatingValue||Cả hai|Cả hai|  
|Truy xuất|RecommendationModelVersion||Cả hai|Máy chủ|  
|Truy xuất|RecommendationModelVersionHistory||Cả hai|Máy chủ|  
|Truy xuất|RecurringAppointmentMaster||Cả hai|Cả hai|  
|Truy xuất|Trường tổng số||Cả hai|Cả hai|  
|Truy xuất|SalesLiterature||Cả hai|Cả hai|  
|Truy xuất|SalesLiteratureItem||Cả hai|Cả hai|  
|Truy xuất|SalesOrder||Cả hai|Cả hai|  
|Truy xuất|SalesOrderDetail||Cả hai|Cả hai|  
|Truy xuất|Yêu cầu đã lưu||Cả hai|Cả hai|  
|Truy xuất|SavedQueryVisualization||Cả hai|Cả hai|  
|Truy xuất|Dịch vụ ||Cả hai|Cả hai|  
|Truy xuất|ServiceAppointment||Cả hai|Cả hai|  
|Truy xuất|Tài liệu SharePoint||Cả hai|Cả hai|  
|Truy xuất|SharePointDocumentLocation||Cả hai|Máy chủ|  
|Truy xuất|Trang SharePoint||Cả hai|Máy chủ|  
|Truy xuất|SimilarityRule||Cả hai|Cả hai|  
|Truy xuất|Trang||Cả hai|Cả hai|  
|Truy xuất|SocialActivity||Cả hai|Cả hai|  
|Truy xuất|SocialProfile||Cả hai|Cả hai|  
|Truy xuất|Giải pháp||Cả hai|Cả hai|  
|Truy xuất|SolutionComponent||Cả hai|Cả hai|  
|Truy xuất|Chủ đề||Cả hai|Cả hai|  
|Truy xuất|Nhiệm vụ||Cả hai|Cả hai|  
|Truy xuất|Nhóm||Cả hai|Cả hai|  
|Truy xuất|Mẫu||Cả hai|Cả hai|  
|Truy xuất|Vùng lãnh thổ||Cả hai|Cả hai|  
|Truy xuất|TextAnalyticsEntityMapping||Cả hai|Cả hai|  
|Truy xuất|Chủ đề||Cả hai|Cả hai|  
|Truy xuất|TopicModelConfiguration||Cả hai|Cả hai|  
|Truy xuất|UoM||Cả hai|Cả hai|  
|Truy xuất|UoMSchedule||Cả hai|Cả hai|  
|Truy xuất|UserForm||Cả hai|Cả hai|  
|Truy xuất|UserMapping||Cả hai|Cả hai|  
|Truy xuất|UserQuery||Cả hai|Cả hai|  
|Truy xuất|UserQueryVisualization||Cả hai|Cả hai|  
|Truy xuất|WebResource||Cả hai|Cả hai|  
|RetrieveExchangeRate|TransactionCurrency||Cả hai|Cả hai|  
|RetrieveFilteredForms|SystemForm||Cả hai|Cả hai|  
|RetrieveMultiple|Khách hàng||Cả hai|Cả hai|  
|RetrieveMultiple|AccountLeads||Cả hai|Cả hai|  
|RetrieveMultiple|ActivityMimeAttachment||Cả hai|Cả hai|  
|RetrieveMultiple|ActivityParty||Cả hai|Cả hai|  
|RetrieveMultiple|ActivityPointer||Cả hai|Cả hai|  
|RetrieveMultiple|Annotation||Cả hai|Cả hai|  
|RetrieveMultiple|AppModuleRoles||Cả hai|Cả hai|  
|RetrieveMultiple|Cuộc hẹn||Cả hai|Cả hai|  
|RetrieveMultiple|AzureServiceConnection||Cả hai|Cả hai|  
|RetrieveMultiple|BookableResource||Cả hai|Cả hai|  
|RetrieveMultiple|BookableResourceBooking||Cả hai|Cả hai|  
|RetrieveMultiple|BookableResourceBookingExchangeSyncIdMapping||Cả hai|Máy chủ|  
|RetrieveMultiple|BookableResourceBookingHeader||Cả hai|Cả hai|  
|RetrieveMultiple|BookableResourceCategory||Cả hai|Cả hai|  
|RetrieveMultiple|BookableResourceCategoryAssn||Cả hai|Cả hai|  
|RetrieveMultiple|BookableResourceCharacteristic||Cả hai|Cả hai|  
|RetrieveMultiple|BookableResourceGroup||Cả hai|Cả hai|  
|RetrieveMultiple|BookingStatus||Cả hai|Cả hai|  
|RetrieveMultiple|BusinessUnitNewsArticle||Cả hai|Cả hai|  
|RetrieveMultiple|Calendar||Cả hai|Cả hai|  
|RetrieveMultiple|Chiến dịch||Cả hai|Cả hai|  
|RetrieveMultiple|CampaignActivity||Cả hai|Cả hai|  
|RetrieveMultiple|CampaignActivityItem||Cả hai|Cả hai|  
|RetrieveMultiple|CampaignItem||Cả hai|Cả hai|  
|RetrieveMultiple|CampaignResponse||Cả hai|Cả hai|  
|RetrieveMultiple|CardType||Cả hai|Cả hai|  
|RetrieveMultiple|Danh mục||Cả hai|Cả hai|  
|RetrieveMultiple|ChannelProperty||Cả hai|Cả hai|  
|RetrieveMultiple|ChannelPropertyGroup||Cả hai|Cả hai|  
|RetrieveMultiple|Đặc điểm||Cả hai|Cả hai|  
|RetrieveMultiple|Đối thủ cạnh tranh||Cả hai|Cả hai|  
|RetrieveMultiple|CompetitorProduct||Cả hai|Cả hai|  
|RetrieveMultiple|CompetitorSalesLiterature||Cả hai|Cả hai|  
|RetrieveMultiple|Connection||Cả hai|Cả hai|  
|RetrieveMultiple|Vai trò Kết nối||Cả hai|Cả hai|  
|RetrieveMultiple|ConnectionRoleAssociation||Cả hai|Cả hai|  
|RetrieveMultiple|ConnectionRoleObjectTypeCode||Cả hai|Cả hai|  
|RetrieveMultiple|người liên hệ||Cả hai|Cả hai|  
|RetrieveMultiple|ContactInvoices||Cả hai|Cả hai|  
|RetrieveMultiple|ContactLeads||Cả hai|Cả hai|  
|RetrieveMultiple|ContactOrders||Cả hai|Cả hai|  
|RetrieveMultiple|ContactQuotes||Cả hai|Cả hai|  
|RetrieveMultiple|Hợp đồng||Cả hai|Cả hai|  
|RetrieveMultiple|ContractDetail||Cả hai|Cả hai|  
|RetrieveMultiple|ContractTemplate||Cả hai|Cả hai|  
|RetrieveMultiple|CustomControl||Cả hai|Cả hai|  
|RetrieveMultiple|CustomControlDefaultConfig||Cả hai|Cả hai|  
|RetrieveMultiple|CustomControlResource||Cả hai|Cả hai|  
|RetrieveMultiple|CustomerAddress||Cả hai|Cả hai|  
|RetrieveMultiple|CustomerOpportunityRole||Cả hai|Cả hai|  
|RetrieveMultiple|CustomerRelationship||Cả hai|Cả hai|  
|RetrieveMultiple|Dependency||Cả hai|Máy chủ|  
|RetrieveMultiple|Giảm giá||Cả hai|Cả hai|  
|RetrieveMultiple|DiscountType||Cả hai|Cả hai|  
|RetrieveMultiple|DocumentTemplate||Cả hai|Cả hai|  
|RetrieveMultiple|DynamicProperty||Cả hai|Cả hai|  
|RetrieveMultiple|DynamicPropertyAssociation||Cả hai|Cả hai|  
|RetrieveMultiple|DynamicPropertyInstance||Cả hai|Cả hai|  
|RetrieveMultiple|DynamicPropertyOptionSetItem||Cả hai|Cả hai|  
|RetrieveMultiple|Email||Cả hai|Cả hai|  
|RetrieveMultiple|Chữ ký Email||Cả hai|Cả hai|  
|RetrieveMultiple|Quyền được hưởng||Cả hai|Cả hai|  
|RetrieveMultiple|EntitlementChannel||Cả hai|Cả hai|  
|RetrieveMultiple|EntitlementContacts||Cả hai|Cả hai|  
|RetrieveMultiple|EntitlementProducts||Cả hai|Cả hai|  
|RetrieveMultiple|EntitlementTemplate||Cả hai|Cả hai|  
|RetrieveMultiple|EntitlementTemplateChannel||Cả hai|Cả hai|  
|RetrieveMultiple|EntitlementTemplateProducts||Cả hai|Cả hai|  
|RetrieveMultiple|Thiết bị||Cả hai|Cả hai|  
|RetrieveMultiple|ExchangeSyncIdMapping||Cả hai|Máy chủ|  
|RetrieveMultiple|Fax||Cả hai|Cả hai|  
|RetrieveMultiple|Phản hồi||Cả hai|Cả hai|  
|RetrieveMultiple|Mục tiêu||Cả hai|Cả hai|  
|RetrieveMultiple|GoalRollupQuery||Cả hai|Cả hai|  
|RetrieveMultiple|HierarchySecurityConfiguration||Cả hai|Cả hai|  
|RetrieveMultiple|Sự cố||Cả hai|Cả hai|  
|RetrieveMultiple|IncidentKnowledgeBaseRecord||Cả hai|Cả hai|  
|RetrieveMultiple|IncidentResolution||Cả hai|Cả hai|  
|RetrieveMultiple|InteractionForEmail||Cả hai|Cả hai|  
|RetrieveMultiple|InvalidDependency||Cả hai|Máy chủ|  
|RetrieveMultiple|Hóa đơn||Cả hai|Cả hai|  
|RetrieveMultiple|InvoiceDetail||Cả hai|Cả hai|  
|RetrieveMultiple|KbArticle||Cả hai|Cả hai|  
|RetrieveMultiple|KbArticleComment||Cả hai|Cả hai|  
|RetrieveMultiple|KbArticleTemplate||Cả hai|Cả hai|  
|RetrieveMultiple|KnowledgeArticle||Cả hai|Cả hai|  
|RetrieveMultiple|KnowledgeArticleIncident||Cả hai|Cả hai|  
|RetrieveMultiple|KnowledgeArticlesCategories||Cả hai|Cả hai|  
|RetrieveMultiple|Dạng xem bài viết kiến thức||Cả hai|Cả hai|  
|RetrieveMultiple|Bản ghi Cơ sở Kiến thức||Cả hai|Cả hai|  
|RetrieveMultiple|LanguageLocale||Cả hai|Cả hai|  
|RetrieveMultiple|Khách hàng tiềm năng||Cả hai|Cả hai|  
|RetrieveMultiple|LeadAddress||Cả hai|Cả hai|  
|RetrieveMultiple|LeadCompetitors||Cả hai|Cả hai|  
|RetrieveMultiple|LeadProduct||Cả hai|Cả hai|  
|RetrieveMultiple|Thư tín||Cả hai|Cả hai|  
|RetrieveMultiple|License||Cả hai|Cả hai|  
|RetrieveMultiple|Danh sách||Cả hai|Cả hai|  
|RetrieveMultiple|ListMember||Cả hai|Cả hai|  
|RetrieveMultiple|Metric||Cả hai|Cả hai|  
|RetrieveMultiple|MobileOfflineProfile||Cả hai|Cả hai|  
|RetrieveMultiple|MobileOfflineProfileItem||Cả hai|Cả hai|  
|RetrieveMultiple|MobileOfflineProfileItemAssociation||Cả hai|Cả hai|  
|RetrieveMultiple|msdyn_PostAlbum||Cả hai|Máy chủ|  
|RetrieveMultiple|msdyn_PostConfig||Cả hai|Máy chủ|  
|RetrieveMultiple|msdyn_PostRuleConfig||Cả hai|Máy chủ|  
|RetrieveMultiple|msdyn_wallsavedquery||Cả hai|Máy chủ|  
|RetrieveMultiple|msdyn_cài đặt người dùng truy vấn được lưu trên tường||Cả hai|Máy chủ|  
|RetrieveMultiple|OfficeGraphDocument||Cả hai|Máy chủ|  
|RetrieveMultiple|Cơ hội||Cả hai|Cả hai|  
|RetrieveMultiple|OpportunityClose||Cả hai|Cả hai|  
|RetrieveMultiple|OpportunityCompetitors||Cả hai|Cả hai|  
|RetrieveMultiple|OpportunityProduct||Cả hai|Cả hai|  
|RetrieveMultiple|OrderClose||Cả hai|Cả hai|  
|RetrieveMultiple|PersonalDocumentTemplate||Cả hai|Cả hai|  
|RetrieveMultiple|Cuộc gọi Điện thoại ||Cả hai|Cả hai|  
|RetrieveMultiple|PluginTraceLog||Cả hai|Cả hai|  
|RetrieveMultiple|Vị trí||Cả hai|Cả hai|  
|RetrieveMultiple|Đăng||Cả hai|Máy chủ|  
|RetrieveMultiple|PostComment||Cả hai|Máy chủ|  
|RetrieveMultiple|PostFollow||Cả hai|Máy chủ|  
|RetrieveMultiple|PostLike||Cả hai|Máy chủ|  
|RetrieveMultiple|PriceLevel||Cả hai|Cả hai|  
|RetrieveMultiple|ProcessSession||Cả hai|Cả hai|  
|RetrieveMultiple|Sản phẩm||Cả hai|Cả hai|  
|RetrieveMultiple|ProductAssociation||Cả hai|Cả hai|  
|RetrieveMultiple|ProductPriceLevel||Cả hai|Cả hai|  
|RetrieveMultiple|ProductSalesLiterature||Cả hai|Cả hai|  
|RetrieveMultiple|ProductSubstitute||Cả hai|Cả hai|  
|RetrieveMultiple|Nhà phát hành||Cả hai|Cả hai|  
|RetrieveMultiple|PublisherAddress||Cả hai|Máy chủ|  
|RetrieveMultiple|Hàng đợi||Cả hai|Cả hai|  
|RetrieveMultiple|QueueMembership||Cả hai|Cả hai|  
|RetrieveMultiple|Báo giá||Cả hai|Cả hai|  
|RetrieveMultiple|QuoteClose||Cả hai|Cả hai|  
|RetrieveMultiple|QuoteDetail||Cả hai|Cả hai|  
|RetrieveMultiple|RatingModel||Cả hai|Cả hai|  
|RetrieveMultiple|RatingValue||Cả hai|Cả hai|  
|RetrieveMultiple|RecommendationModelVersion||Cả hai|Máy chủ|  
|RetrieveMultiple|RecommendationModelVersionHistory||Cả hai|Máy chủ|  
|RetrieveMultiple|RecommendedDocument||Cả hai|Máy chủ|  
|RetrieveMultiple|RecurrenceRule||Cả hai|Cả hai|  
|RetrieveMultiple|RecurringAppointmentMaster||Cả hai|Cả hai|  
|RetrieveMultiple|RolePrivileges||Cả hai|Cả hai|  
|RetrieveMultiple|Trường tổng số||Cả hai|Cả hai|  
|RetrieveMultiple|SalesLiterature||Cả hai|Cả hai|  
|RetrieveMultiple|SalesLiteratureItem||Cả hai|Cả hai|  
|RetrieveMultiple|SalesOrder||Cả hai|Cả hai|  
|RetrieveMultiple|SalesOrderDetail||Cả hai|Cả hai|  
|RetrieveMultiple|Yêu cầu đã lưu||Cả hai|Cả hai|  
|RetrieveMultiple|SavedQueryVisualization||Cả hai|Cả hai|  
|RetrieveMultiple|Dịch vụ ||Cả hai|Cả hai|  
|RetrieveMultiple|ServiceAppointment||Cả hai|Cả hai|  
|RetrieveMultiple|ServiceContractContacts||Cả hai|Cả hai|  
|RetrieveMultiple|Tài liệu SharePoint||Cả hai|Cả hai|  
|RetrieveMultiple|SharePointDocumentLocation||Cả hai|Máy chủ|  
|RetrieveMultiple|Trang SharePoint||Cả hai|Máy chủ|  
|RetrieveMultiple|SimilarityRule||Cả hai|Cả hai|  
|RetrieveMultiple|Trang||Cả hai|Cả hai|  
|RetrieveMultiple|SocialActivity||Cả hai|Cả hai|  
|RetrieveMultiple|SocialProfile||Cả hai|Cả hai|  
|RetrieveMultiple|Giải pháp||Cả hai|Cả hai|  
|RetrieveMultiple|SolutionComponent||Cả hai|Cả hai|  
|RetrieveMultiple|Chủ đề||Cả hai|Cả hai|  
|RetrieveMultiple|SystemUserLicenses||Cả hai|Cả hai|  
|RetrieveMultiple|SystemUserProfiles||Cả hai|Máy chủ|  
|RetrieveMultiple|SystemUserRoles||Cả hai|Cả hai|  
|RetrieveMultiple|Nhiệm vụ||Cả hai|Cả hai|  
|RetrieveMultiple|Nhóm||Cả hai|Cả hai|  
|RetrieveMultiple|TeamMembership||Cả hai|Cả hai|  
|RetrieveMultiple|TeamProfiles||Cả hai|Máy chủ|  
|RetrieveMultiple|TeamRoles||Cả hai|Cả hai|  
|RetrieveMultiple|Mẫu||Cả hai|Cả hai|  
|RetrieveMultiple|Vùng lãnh thổ||Cả hai|Cả hai|  
|RetrieveMultiple|TextAnalyticsEntityMapping||Cả hai|Cả hai|  
|RetrieveMultiple|Chủ đề||Cả hai|Cả hai|  
|RetrieveMultiple|TopicModelConfiguration||Cả hai|Cả hai|  
|RetrieveMultiple|UoM||Cả hai|Cả hai|  
|RetrieveMultiple|UoMSchedule||Cả hai|Cả hai|  
|RetrieveMultiple|UserEntityInstanceData||Cả hai|Cả hai|  
|RetrieveMultiple|UserForm||Cả hai|Cả hai|  
|RetrieveMultiple|UserMapping||Cả hai|Cả hai|  
|RetrieveMultiple|UserQuery||Cả hai|Cả hai|  
|RetrieveMultiple|UserQueryVisualization||Cả hai|Cả hai|  
|RetrieveMultiple|UserSettings||Cả hai|Cả hai|  
|RetrieveMultiple|WebResource||Cả hai|Cả hai|  
|RetrievePersonalWall|||Máy chủ|Máy chủ|  
|RetrievePrincipalAccess|Khách hàng||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Annotation||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Cuộc hẹn||Cả hai|Cả hai|  
|RetrievePrincipalAccess|BookableResource||Cả hai|Cả hai|  
|RetrievePrincipalAccess|BookableResourceBooking||Cả hai|Cả hai|  
|RetrievePrincipalAccess|BookableResourceBookingHeader||Cả hai|Cả hai|  
|RetrievePrincipalAccess|BookableResourceCategory||Cả hai|Cả hai|  
|RetrievePrincipalAccess|BookableResourceCategoryAssn||Cả hai|Cả hai|  
|RetrievePrincipalAccess|BookableResourceCharacteristic||Cả hai|Cả hai|  
|RetrievePrincipalAccess|BookableResourceGroup||Cả hai|Cả hai|  
|RetrievePrincipalAccess|BookingStatus||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Chiến dịch||Cả hai|Cả hai|  
|RetrievePrincipalAccess|CampaignActivity||Cả hai|Cả hai|  
|RetrievePrincipalAccess|CampaignResponse||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Danh mục||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Đặc điểm||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Connection||Cả hai|Cả hai|  
|RetrievePrincipalAccess|người liên hệ||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Hợp đồng||Cả hai|Cả hai|  
|RetrievePrincipalAccess|CustomerOpportunityRole||Cả hai|Cả hai|  
|RetrievePrincipalAccess|CustomerRelationship||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Email||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Chữ ký Email||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Quyền được hưởng||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Fax||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Phản hồi||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Mục tiêu||Cả hai|Cả hai|  
|RetrievePrincipalAccess|GoalRollupQuery||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Sự cố||Cả hai|Cả hai|  
|RetrievePrincipalAccess|IncidentResolution||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Hóa đơn||Cả hai|Cả hai|  
|RetrievePrincipalAccess|KnowledgeArticle||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Bản ghi Cơ sở Kiến thức||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Khách hàng tiềm năng||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Thư tín||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Danh sách||Cả hai|Cả hai|  
|RetrievePrincipalAccess|msdyn_PostAlbum||Cả hai|Máy chủ|  
|RetrievePrincipalAccess|msdyn_cài đặt người dùng truy vấn được lưu trên tường||Cả hai|Máy chủ|  
|RetrievePrincipalAccess|Cơ hội||Cả hai|Cả hai|  
|RetrievePrincipalAccess|OpportunityClose||Cả hai|Cả hai|  
|RetrievePrincipalAccess|OrderClose||Cả hai|Cả hai|  
|RetrievePrincipalAccess|PersonalDocumentTemplate||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Cuộc gọi Điện thoại ||Cả hai|Cả hai|  
|RetrievePrincipalAccess|ProcessSession||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Hàng đợi||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Báo giá||Cả hai|Cả hai|  
|RetrievePrincipalAccess|QuoteClose||Cả hai|Cả hai|  
|RetrievePrincipalAccess|RatingModel||Cả hai|Cả hai|  
|RetrievePrincipalAccess|RatingValue||Cả hai|Cả hai|  
|RetrievePrincipalAccess|RecurringAppointmentMaster||Cả hai|Cả hai|  
|RetrievePrincipalAccess|SalesOrder||Cả hai|Cả hai|  
|RetrievePrincipalAccess|ServiceAppointment||Cả hai|Cả hai|  
|RetrievePrincipalAccess|SharePointDocumentLocation||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Trang SharePoint||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Phiên bản KPI SLA||Cả hai|Cả hai|  
|RetrievePrincipalAccess|SocialActivity||Cả hai|Cả hai|  
|RetrievePrincipalAccess|SocialProfile||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Nhiệm vụ||Cả hai|Cả hai|  
|RetrievePrincipalAccess|Mẫu||Cả hai|Cả hai|  
|RetrievePrincipalAccess|UserForm||Cả hai|Cả hai|  
|RetrievePrincipalAccess|UserQuery||Cả hai|Cả hai|  
|RetrievePrincipalAccess|UserQueryVisualization||Cả hai|Cả hai|  
|RetrieveRecordWall|||Máy chủ|Máy chủ|  
|RetrieveSharedPrincipalsAndAccess|Khách hàng||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Annotation||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Cuộc hẹn||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|BookableResource||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|BookableResourceBooking||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|BookableResourceBookingHeader||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|BookableResourceCategory||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|BookableResourceCategoryAssn||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|BookableResourceCharacteristic||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|BookableResourceGroup||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|BookingStatus||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Chiến dịch||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|CampaignActivity||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|CampaignResponse||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Danh mục||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Đặc điểm||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Connection||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|người liên hệ||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Hợp đồng||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|CustomerOpportunityRole||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|CustomerRelationship||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Email||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Quyền được hưởng||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Fax||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Phản hồi||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Mục tiêu||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|GoalRollupQuery||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Sự cố||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|IncidentResolution||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Hóa đơn||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|KnowledgeArticle||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Bản ghi Cơ sở Kiến thức||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Khách hàng tiềm năng||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Thư tín||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Danh sách||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|msdyn_PostAlbum||Cả hai|Máy chủ|  
|RetrieveSharedPrincipalsAndAccess|msdyn_cài đặt người dùng truy vấn được lưu trên tường||Cả hai|Máy chủ|  
|RetrieveSharedPrincipalsAndAccess|Cơ hội||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|OpportunityClose||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|OrderClose||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|PersonalDocumentTemplate||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Cuộc gọi Điện thoại ||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|ProcessSession||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Hàng đợi||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Báo giá||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|QuoteClose||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|RatingModel||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|RatingValue||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|RecurringAppointmentMaster||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|SalesOrder||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|ServiceAppointment||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|SharePointDocumentLocation||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Trang SharePoint||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Phiên bản KPI SLA||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|SocialActivity||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|SocialProfile||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Nhiệm vụ||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|Mẫu||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|UserForm||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|UserQuery||Cả hai|Cả hai|  
|RetrieveSharedPrincipalsAndAccess|UserQueryVisualization||Cả hai|Cả hai|  
|RetrieveUnpublished|WebResource||Máy chủ|Máy chủ|  
|RetrieveUnpublishedMultiple|WebResource||Máy chủ|Máy chủ|  
|RetrieveUserQueues|Hàng đợi||Cả hai|Cả hai|  
|RevokeAccess|Khách hàng||Máy chủ|Máy chủ|  
|RevokeAccess|Annotation||Máy chủ|Máy chủ|  
|RevokeAccess|Cuộc hẹn||Máy chủ|Máy chủ|  
|RevokeAccess|BookableResource||Máy chủ|Máy chủ|  
|RevokeAccess|BookableResourceBooking||Máy chủ|Máy chủ|  
|RevokeAccess|BookableResourceBookingHeader||Máy chủ|Máy chủ|  
|RevokeAccess|BookableResourceCategory||Máy chủ|Máy chủ|  
|RevokeAccess|BookableResourceCategoryAssn||Máy chủ|Máy chủ|  
|RevokeAccess|BookableResourceCharacteristic||Máy chủ|Máy chủ|  
|RevokeAccess|BookableResourceGroup||Máy chủ|Máy chủ|  
|RevokeAccess|BookingStatus||Máy chủ|Máy chủ|  
|RevokeAccess|Chiến dịch||Máy chủ|Máy chủ|  
|RevokeAccess|CampaignActivity||Máy chủ|Máy chủ|  
|RevokeAccess|CampaignResponse||Máy chủ|Máy chủ|  
|RevokeAccess|Danh mục||Máy chủ|Máy chủ|  
|RevokeAccess|Đặc điểm||Máy chủ|Máy chủ|  
|RevokeAccess|Connection||Máy chủ|Máy chủ|  
|RevokeAccess|người liên hệ||Máy chủ|Máy chủ|  
|RevokeAccess|Hợp đồng||Máy chủ|Máy chủ|  
|RevokeAccess|CustomerOpportunityRole||Máy chủ|Máy chủ|  
|RevokeAccess|CustomerRelationship||Máy chủ|Máy chủ|  
|RevokeAccess|Email||Máy chủ|Máy chủ|  
|RevokeAccess|Quyền được hưởng||Máy chủ|Máy chủ|  
|RevokeAccess|Fax||Máy chủ|Máy chủ|  
|RevokeAccess|Phản hồi||Máy chủ|Máy chủ|  
|RevokeAccess|Mục tiêu||Máy chủ|Máy chủ|  
|RevokeAccess|GoalRollupQuery||Máy chủ|Máy chủ|  
|RevokeAccess|Sự cố||Máy chủ|Máy chủ|  
|RevokeAccess|IncidentResolution||Máy chủ|Máy chủ|  
|RevokeAccess|Hóa đơn||Máy chủ|Máy chủ|  
|RevokeAccess|KnowledgeArticle||Máy chủ|Máy chủ|  
|RevokeAccess|Bản ghi Cơ sở Kiến thức||Máy chủ|Máy chủ|  
|RevokeAccess|Khách hàng tiềm năng||Máy chủ|Máy chủ|  
|RevokeAccess|Thư tín||Máy chủ|Máy chủ|  
|RevokeAccess|Danh sách||Máy chủ|Máy chủ|  
|RevokeAccess|msdyn_PostAlbum||Máy chủ|Máy chủ|  
|RevokeAccess|msdyn_cài đặt người dùng truy vấn được lưu trên tường||Máy chủ|Máy chủ|  
|RevokeAccess|Cơ hội||Máy chủ|Máy chủ|  
|RevokeAccess|OpportunityClose||Máy chủ|Máy chủ|  
|RevokeAccess|OrderClose||Máy chủ|Máy chủ|  
|RevokeAccess|PersonalDocumentTemplate||Máy chủ|Máy chủ|  
|RevokeAccess|Cuộc gọi Điện thoại ||Máy chủ|Máy chủ|  
|RevokeAccess|ProcessSession||Máy chủ|Máy chủ|  
|RevokeAccess|Hàng đợi||Máy chủ|Máy chủ|  
|RevokeAccess|Báo giá||Máy chủ|Máy chủ|  
|RevokeAccess|QuoteClose||Máy chủ|Máy chủ|  
|RevokeAccess|RatingModel||Máy chủ|Máy chủ|  
|RevokeAccess|RatingValue||Máy chủ|Máy chủ|  
|RevokeAccess|RecurringAppointmentMaster||Máy chủ|Máy chủ|  
|RevokeAccess|SalesOrder||Máy chủ|Máy chủ|  
|RevokeAccess|ServiceAppointment||Máy chủ|Máy chủ|  
|RevokeAccess|SharePointDocumentLocation||Máy chủ|Máy chủ|  
|RevokeAccess|Trang SharePoint||Máy chủ|Máy chủ|  
|RevokeAccess|Phiên bản KPI SLA||Máy chủ|Máy chủ|  
|RevokeAccess|SocialActivity||Máy chủ|Máy chủ|  
|RevokeAccess|SocialProfile||Máy chủ|Máy chủ|  
|RevokeAccess|Nhiệm vụ||Máy chủ|Máy chủ|  
|RevokeAccess|Mẫu||Máy chủ|Máy chủ|  
|RevokeAccess|UserForm||Máy chủ|Máy chủ|  
|RevokeAccess|UserQuery||Máy chủ|Máy chủ|  
|RevokeAccess|UserQueryVisualization||Máy chủ|Máy chủ|  
|RouteTo|QueueItem||Cả hai|Cả hai|  
|Gửi|Email||Cả hai|Cả hai|  
|Gửi|Fax||Cả hai|Cả hai|  
|Gửi|Mẫu||Cả hai|Cả hai|  
|SendFromTemplate|Email||Máy chủ|Máy chủ|  
|SetLocLabels|||Máy chủ|Máy chủ|  
|SetRelated|Hóa đơn|người liên hệ|Cả hai|Cả hai|  
|SetRelated|Khách hàng tiềm năng|Khách hàng|Cả hai|Cả hai|  
|SetRelated|Khách hàng tiềm năng|người liên hệ|Cả hai|Cả hai|  
|SetRelated|Cơ hội|Khách hàng|Cả hai|Cả hai|  
|SetRelated|Cơ hội|Đối thủ cạnh tranh|Cả hai|Cả hai|  
|SetRelated|Cơ hội|người liên hệ|Cả hai|Cả hai|  
|SetRelated|Sản phẩm|Đối thủ cạnh tranh|Cả hai|Cả hai|  
|SetRelated|Sản phẩm|Khách hàng tiềm năng|Cả hai|Cả hai|  
|SetRelated|Báo giá|người liên hệ|Cả hai|Cả hai|  
|SetRelated|SalesLiterature|Đối thủ cạnh tranh|Cả hai|Cả hai|  
|SetRelated|SalesLiterature|Sản phẩm|Cả hai|Cả hai|  
|SetRelated|SalesOrder|người liên hệ|Cả hai|Cả hai|  
|SetState|Khách hàng||Cả hai|Cả hai|  
|SetState|Cuộc hẹn||Cả hai|Cả hai|  
|SetState|BookableResource||Cả hai|Cả hai|  
|SetState|BookableResourceBooking||Cả hai|Cả hai|  
|SetState|BookableResourceBookingHeader||Cả hai|Cả hai|  
|SetState|BookableResourceCategory||Cả hai|Cả hai|  
|SetState|BookableResourceCategoryAssn||Cả hai|Cả hai|  
|SetState|BookableResourceCharacteristic||Cả hai|Cả hai|  
|SetState|BookableResourceGroup||Cả hai|Cả hai|  
|SetState|BookingStatus||Cả hai|Cả hai|  
|SetState|Đơn vị kinh doanh||Cả hai|Máy chủ|  
|SetState|Chiến dịch||Cả hai|Cả hai|  
|SetState|CampaignActivity||Cả hai|Cả hai|  
|SetState|CampaignResponse||Cả hai|Cả hai|  
|SetState|ChannelProperty||Cả hai|Máy chủ|  
|SetState|ChannelPropertyGroup||Cả hai|Máy chủ|  
|SetState|Đặc điểm||Cả hai|Cả hai|  
|SetState|Connection||Cả hai|Cả hai|  
|SetState|Vai trò Kết nối||Cả hai|Cả hai|  
|SetState|người liên hệ||Cả hai|Cả hai|  
|SetState|Hợp đồng||Cả hai|Cả hai|  
|SetState|ContractDetail||Cả hai|Cả hai|  
|SetState|DiscountType||Cả hai|Cả hai|  
|SetState|Email||Cả hai|Cả hai|  
|SetState|Cấu hình Máy chủ Email||Cả hai|Máy chủ|  
|SetState|Quyền được hưởng||Cả hai|Cả hai|  
|SetState|ExpiredProcess||Cả hai|Cả hai|  
|SetState|Fax||Cả hai|Cả hai|  
|SetState|Phản hồi||Cả hai|Cả hai|  
|SetState|Sự cố||Cả hai|Cả hai|  
|SetState|IncidentResolution||Cả hai|Cả hai|  
|SetState|Hóa đơn||Cả hai|Cả hai|  
|SetState|KbArticle||Cả hai|Cả hai|  
|SetState|KnowledgeArticle||Cả hai|Cả hai|  
|SetState|Bản ghi Cơ sở Kiến thức||Cả hai|Cả hai|  
|SetState|LanguageLocale||Cả hai|Cả hai|  
|SetState|Khách hàng tiềm năng||Cả hai|Cả hai|  
|SetState|LeadToOpportunitySalesProcess||Cả hai|Cả hai|  
|SetState|Thư tín||Cả hai|Cả hai|  
|SetState|Danh sách||Cả hai|Cả hai|  
|SetState|msdyn_PostAlbum||Cả hai|Máy chủ|  
|SetState|msdyn_PostConfig||Cả hai|Máy chủ|  
|SetState|msdyn_PostRuleConfig||Cả hai|Máy chủ|  
|SetState|msdyn_wallsavedquery||Cả hai|Máy chủ|  
|SetState|msdyn_cài đặt người dùng truy vấn được lưu trên tường||Cả hai|Máy chủ|  
|SetState|NewProcess||Cả hai|Cả hai|  
|SetState|Cơ hội||Cả hai|Cả hai|  
|SetState|OpportunityClose||Cả hai|Cả hai|  
|SetState|OpportunitySalesProcess||Cả hai|Cả hai|  
|SetState|OrderClose||Cả hai|Cả hai|  
|SetState|Cuộc gọi Điện thoại ||Cả hai|Cả hai|  
|SetState|PhoneToCaseProcess||Cả hai|Cả hai|  
|SetState|PriceLevel||Cả hai|Cả hai|  
|SetState|Sản phẩm||Cả hai|Cả hai|  
|SetState|Hàng đợi||Cả hai|Cả hai|  
|SetState|QueueItem||Cả hai|Cả hai|  
|SetState|Báo giá||Cả hai|Cả hai|  
|SetState|QuoteClose||Cả hai|Cả hai|  
|SetState|RatingModel||Cả hai|Cả hai|  
|SetState|RatingValue||Cả hai|Cả hai|  
|SetState|RecurringAppointmentMaster||Cả hai|Cả hai|  
|SetState|SalesOrder||Cả hai|Cả hai|  
|SetState|ServiceAppointment||Cả hai|Cả hai|  
|SetState|SharePointDocumentLocation||Cả hai|Cả hai|  
|SetState|Trang SharePoint||Cả hai|Cả hai|  
|SetState|SocialActivity||Cả hai|Cả hai|  
|SetState|SocialProfile||Cả hai|Cả hai|  
|SetState|Người dùng hệ thống||Cả hai|Máy chủ|  
|SetState|Nhiệm vụ||Cả hai|Cả hai|  
|SetState|TransactionCurrency||Cả hai|Máy chủ|  
|SetState|TranslationProcess||Cả hai|Cả hai|  
|SetState|UserQuery||Cả hai|Cả hai|  
|TriggerServiceEndpointCheck|ServiceEndpoint||Máy chủ|Máy chủ|  
|UnlockInvoicePricing|||Máy chủ|Máy chủ|  
|UnlockSalesOrderPricing|||Máy chủ|Máy chủ|  
|Update|Khách hàng||Cả hai|Cả hai|  
|Update|ActionCard||Cả hai|Cả hai|  
|Update|ActivityMimeAttachment||Cả hai|Cả hai|  
|Update|Annotation||Cả hai|Cả hai|  
|Update|Cuộc hẹn||Cả hai|Cả hai|  
|Update|AzureServiceConnection||Cả hai|Máy chủ|  
|Update|BookableResource||Cả hai|Cả hai|  
|Update|BookableResourceBooking||Cả hai|Cả hai|  
|Update|BookableResourceBookingExchangeSyncIdMapping||Cả hai|Máy chủ|  
|Update|BookableResourceBookingHeader||Cả hai|Cả hai|  
|Update|BookableResourceCategory||Cả hai|Cả hai|  
|Update|BookableResourceCategoryAssn||Cả hai|Cả hai|  
|Update|BookableResourceCharacteristic||Cả hai|Cả hai|  
|Update|BookableResourceGroup||Cả hai|Cả hai|  
|Update|BookingStatus||Cả hai|Cả hai|  
|Update|BusinessProcessFlowInstance||Cả hai|Cả hai|  
|Update|Đơn vị kinh doanh||Cả hai|Máy chủ|  
|Update|BusinessUnitNewsArticle||Cả hai|Cả hai|  
|Update|Calendar||Cả hai|Cả hai|  
|Update|Chiến dịch||Cả hai|Cả hai|  
|Update|CampaignActivity||Cả hai|Cả hai|  
|Update|CampaignResponse||Cả hai|Cả hai|  
|Update|CardType||Cả hai|Cả hai|  
|Update|Danh mục||Cả hai|Cả hai|  
|Update|Đặc điểm||Cả hai|Cả hai|  
|Update|Đối thủ cạnh tranh||Cả hai|Cả hai|  
|Update|Connection||Cả hai|Cả hai|  
|Update|Vai trò Kết nối||Cả hai|Cả hai|  
|Update|người liên hệ||Cả hai|Cả hai|  
|Update|Hợp đồng||Cả hai|Cả hai|  
|Update|ContractDetail||Cả hai|Cả hai|  
|Update|ContractTemplate||Cả hai|Máy chủ|  
|Update|CustomControl||Cả hai|Máy chủ|  
|Update|CustomControlDefaultConfig||Cả hai|Máy chủ|  
|Update|CustomControlResource||Cả hai|Máy chủ|  
|Update|CustomerAddress||Cả hai|Cả hai|  
|Update|CustomerOpportunityRole||Cả hai|Cả hai|  
|Update|CustomerRelationship||Cả hai|Cả hai|  
|Update|Giảm giá||Cả hai|Cả hai|  
|Update|DiscountType||Cả hai|Cả hai|  
|Update|Email||Cả hai|Cả hai|  
|Update|Chữ ký Email||Cả hai|Cả hai|  
|Update|Quyền được hưởng||Cả hai|Cả hai|  
|Update|EntitlementChannel||Cả hai|Máy chủ|  
|Update|EntitlementTemplate||Cả hai|Máy chủ|  
|Update|EntitlementTemplateChannel||Cả hai|Máy chủ|  
|Update|Thiết bị||Cả hai|Máy chủ|  
|Update|ExchangeSyncIdMapping||Cả hai|Máy chủ|  
|Update|ExpiredProcess||Cả hai|Cả hai|  
|Update|Fax||Cả hai|Cả hai|  
|Update|Phản hồi||Cả hai|Cả hai|  
|Update|Quyền của Trường||Cả hai|Máy chủ|  
|Update|Cấu hình Bảo mật Trường||Cả hai|Máy chủ|  
|Update|Mục tiêu||Cả hai|Máy chủ|  
|Update|GoalRollupQuery||Cả hai|Máy chủ|  
|Update|HierarchyRule||Cả hai|Máy chủ|  
|Update|Sự cố||Cả hai|Cả hai|  
|Update|IncidentResolution||Cả hai|Cả hai|  
|Update|Hóa đơn||Cả hai|Cả hai|  
|Update|InvoiceDetail||Cả hai|Cả hai|  
|Update|KbArticle||Cả hai|Cả hai|  
|Update|KbArticleComment||Cả hai|Cả hai|  
|Update|KbArticleTemplate||Cả hai|Cả hai|  
|Update|KnowledgeArticle||Cả hai|Cả hai|  
|Update|KnowledgeArticleIncident||Cả hai|Cả hai|  
|Update|Dạng xem bài viết kiến thức||Cả hai|Cả hai|  
|Update|Bản ghi Cơ sở Kiến thức||Cả hai|Cả hai|  
|Update|LanguageLocale||Cả hai|Cả hai|  
|Update|Khách hàng tiềm năng||Cả hai|Cả hai|  
|Update|LeadToOpportunitySalesProcess||Cả hai|Cả hai|  
|Update|Thư tín||Cả hai|Cả hai|  
|Update|Danh sách||Cả hai|Cả hai|  
|Update|Metric||Cả hai|Máy chủ|  
|Update|msdyn_PostAlbum||Cả hai|Máy chủ|  
|Update|msdyn_PostConfig||Cả hai|Máy chủ|  
|Update|msdyn_PostRuleConfig||Cả hai|Máy chủ|  
|Update|msdyn_wallsavedquery||Cả hai|Máy chủ|  
|Update|msdyn_cài đặt người dùng truy vấn được lưu trên tường||Cả hai|Máy chủ|  
|Update|NewProcess||Cả hai|Cả hai|  
|Update|Cơ hội||Cả hai|Cả hai|  
|Update|OpportunityClose||Cả hai|Cả hai|  
|Update|OpportunityProduct||Cả hai|Cả hai|  
|Update|OpportunitySalesProcess||Cả hai|Cả hai|  
|Update|OrderClose||Cả hai|Cả hai|  
|Update|Tổ chức||Cả hai|Máy chủ|  
|Update|Cuộc gọi Điện thoại ||Cả hai|Cả hai|  
|Update|PhoneToCaseProcess||Cả hai|Cả hai|  
|Update|Vị trí||Cả hai|Máy chủ|  
|Update|PriceLevel||Cả hai|Cả hai|  
|Update|PrincipalObjectAttributeAccess||Cả hai|Máy chủ|  
|Update|ProcessSession||Cả hai|Cả hai|  
|Update|Sản phẩm||Cả hai|Cả hai|  
|Update|ProductAssociation||Cả hai|Cả hai|  
|Update|ProductPriceLevel||Cả hai|Cả hai|  
|Update|ProductSubstitute||Cả hai|Cả hai|  
|Update|Hàng đợi||Cả hai|Máy chủ|  
|Update|QueueItem||Cả hai|Cả hai|  
|Update|Báo giá||Cả hai|Cả hai|  
|Update|QuoteClose||Cả hai|Cả hai|  
|Update|QuoteDetail||Cả hai|Cả hai|  
|Update|RatingModel||Cả hai|Cả hai|  
|Update|RatingValue||Cả hai|Cả hai|  
|Update|RecommendationModelVersion||Cả hai|Máy chủ|  
|Update|RecommendationModelVersionHistory||Cả hai|Máy chủ|  
|Update|RecurrenceRule||Cả hai|Máy chủ|  
|Update|RecurringAppointmentMaster||Cả hai|Cả hai|  
|Update|Vai trò||Cả hai|Máy chủ|  
|Update|Trường tổng số||Cả hai|Máy chủ|  
|Update|SalesLiterature||Cả hai|Cả hai|  
|Update|SalesLiteratureItem||Cả hai|Cả hai|  
|Update|SalesOrder||Cả hai|Cả hai|  
|Update|SalesOrderDetail||Cả hai|Cả hai|  
|Update|Dịch vụ ||Cả hai|Máy chủ|  
|Update|ServiceAppointment||Cả hai|Cả hai|  
|Update|SharePointDocumentLocation||Cả hai|Máy chủ|  
|Update|Trang SharePoint||Cả hai|Máy chủ|  
|Update|SimilarityRule||Cả hai|Cả hai|  
|Update|Trang||Cả hai|Máy chủ|  
|Update|Phiên bản KPI SLA||Cả hai|Máy chủ|  
|Update|SocialActivity||Cả hai|Cả hai|  
|Update|SocialProfile||Cả hai|Cả hai|  
|Update|Chủ đề||Cả hai|Cả hai|  
|Update|Người dùng hệ thống||Cả hai|Máy chủ|  
|Update|Nhiệm vụ||Cả hai|Cả hai|  
|Update|Nhóm||Cả hai|Máy chủ|  
|Update|Mẫu||Cả hai|Cả hai|  
|Update|Vùng lãnh thổ||Cả hai|Máy chủ|  
|Update|TextAnalyticsEntityMapping||Cả hai|Máy chủ|  
|Update|Chủ đề||Cả hai|Cả hai|  
|Update|TopicModelConfiguration||Cả hai|Cả hai|  
|Update|TransactionCurrency||Cả hai|Máy chủ|  
|Update|TranslationProcess||Cả hai|Cả hai|  
|Update|UoM||Cả hai|Cả hai|  
|Update|UoMSchedule||Cả hai|Cả hai|  
|Update|UserForm||Cả hai|Máy chủ|  
|Update|UserMapping||Cả hai|Cả hai|  
|Update|UserQuery||Cả hai|Cả hai|  
|Update|UserQueryVisualization||Cả hai|Cả hai|  
|Update|WebResource||Cả hai|Máy chủ|  
|ValidateRecurrenceRule|RecurrenceRule||Cả hai|Cả hai|  
|Win|Cơ hội||Cả hai|Cả hai|  
|Win|Báo giá||Cả hai|Cả hai|  
  
### <a name="see-also"></a>Xem thêm  
 [Write Plug-Ins for Dynamics 365 for Customer Engagement apps](write-plugin-extend-business-processes.md)   
 [Plug-in Development](plugin-development.md)   
 [Event Framework Overview](introduction-event-framework.md)
