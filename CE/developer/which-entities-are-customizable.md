---
title: Which entities are customizable? (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about the entities properties that are customizable.
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
- which entities are customizable?
- entity metadata properties that control customization
- customizing entities, fully customizable entities
- customizing entities, properties of customizable entities
- customizing entities, entity metadata properties that control customization
- entities, which entities are customizable?
- customizing entities, which entities are customizable?
ms.assetid: f9807600-8cfd-4879-9005-f3a2068aceb8
caps.latest.revision: 30
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d26d99a1e4e2c815f9254c003c15312352227218
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386639"
---
# <a name="which-entities-are-customizable"></a>Which entities are customizable?

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement has 271 entities; of these, 98 entities are customizable. Any custom entities that you add are also customizable. Creators of managed solutions can use managed properties to select whether to enable customization of entities in their solutions. The specific customizations that are allowed for customizable entities are defined by other properties.  
  
<a name="properties"></a>   
## <a name="entitymetadata-properties-that-control-customization"></a>EntityMetadata properties that control customization  
 The following entity metadata properties define what types of customizations any entity will support.  
  
|Thuộc tính|Mô tả|  
|--------------|-----------------|  
|IsCustomizable|Specifies whether an entity allows customization.|  
|IsRenameable|Specifies whether you can change the display name for an entity in the application.|  
|CanBeRelatedEntityInRelationship|Specifies whether you can add a lookup attribute to an entity to establish a custom entity relationship.|  
|CanBePrimaryEntityInRelationship|Specifies whether you can set the entity to be the primary entity in a custom entity relationship.|  
|CanBeInManyToMany|Specifies whether the entity can participate in a many-to-many custom entity relationship.|  
|CanCreateForms|Specifies whether you can create custom forms for the entity.|  
|CanCreateCharts|Specifies whether you can create charts for the entity.|  
|CanCreateViews|Specifies whether you can create views for the entity.|  
|CanCreateAttributes|Specifies whether you can create attributes for the entity.|  
|CanModifyAdditionalSettings|Specifies whether any other entity properties not represented by a managed property can be changed.|  
  
<a name="fully"></a>   
## <a name="fully-customizable-entities"></a>Fully customizable entities  
 The following table lists the entities that support all the customization capabilities. Any custom entities you add will support the same capabilities.  
  
|||||||  
|-|-|-|-|-|-|  
|Khách hàng|Chiến dịch|CampaignActivity|CampaignResponse|Đối thủ cạnh tranh|Connection|  
|người liên hệ|Hợp đồng|Email|Fax|Mục tiêu|Sự cố|  
|Hóa đơn|InvoiceDetail|Khách hàng tiềm năng|Thư tín|Danh sách|Cơ hội|  
|OpportunityProduct|Cuộc gọi Điện thoại |Sản phẩm|QueueItem|Báo giá|QuoteDetail|  
|SalesLiterature|SalesOrder|SalesOrderDetail|ServiceAppointment|Người dùng hệ thống|Nhiệm vụ|  
|Vùng lãnh thổ||||||  
  
<a name="customizable_entity_properies"></a>   
## <a name="customizable-entity-properties"></a>Customizable entity properties  
 The following table lists the customizable entities and the values for the entity metadata properties that control customizations.  
  
|`DisplayName`|`IsCustomizable`|`CanBeInManyToMany`|`CanBePrimaryEntityInRelationship`|`CanBeRelatedEntityInRelationship`|`CanCreateAttributes`|`CanCreateCharts`|`CanCreateForms`|`CanCreateViews`|`CanModifyAdditionalSettings`|`IsRenameable`|  
|-------------------|----------------------|-------------------------|----------------------------------------|----------------------------------------|---------------------------|-----------------------|----------------------|----------------------|-----------------------------------|--------------------|  
|Khách hàng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|ActivityMimeAttachment|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|ActivityPointer|Đúng|Sai|Sai|Sai|Sai|Đúng|Sai|Đúng|Đúng|Đúng|  
|Annotation|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Đúng|Sai|  
|Cuộc hẹn|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Sai|Đúng|Đúng|Đúng|  
|BulkOperation|Đúng|Sai|Sai|Sai|Sai|Đúng|Sai|Đúng|Đúng|Đúng|  
|Đơn vị kinh doanh|Đúng|Đúng|Đúng|Đúng|Đúng|Sai|Đúng|Đúng|Đúng|Đúng|  
|Chiến dịch|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|CampaignActivity|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|CampaignResponse|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|Đối thủ cạnh tranh|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|CompetitorAddress|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Connection|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|Vai trò Kết nối|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Đúng|  
|người liên hệ|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|Hợp đồng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|ContractDetail|Đúng|Đúng|Đúng|Đúng|Đúng|Sai|Đúng|Đúng|Đúng|Đúng|  
|ContractTemplate|Đúng|Sai|Đúng|Sai|Sai|Sai|Sai|Sai|Đúng|Đúng|  
|CustomerAddress|Đúng|Đúng|Đúng|Đúng|Đúng|Sai|Đúng|Đúng|Đúng|Đúng|  
|CustomerOpportunityRole|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Giảm giá|Đúng|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|DiscountType|Đúng|Đúng|Đúng|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Quy tắc trùng lặp|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Điều kiện Quy tắc Trùng lặp|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Email|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|Cấu hình Máy chủ Email|Đúng|Sai|Đúng|Đúng|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Thiết bị|Đúng|Đúng|Đúng|Đúng|Đúng|Sai|Đúng|Đúng|Đúng|Đúng|  
|Fax|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|Quyền của Trường|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Cấu hình Bảo mật Trường|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Mục tiêu|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|GoalRollupQuery|Đúng|Đúng|Đúng|Đúng|Sai|Đúng|Sai|Đúng|Đúng|Đúng|  
|Nhập Bản đồ|Đúng|Sai|Đúng|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Sự cố|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|IncidentResolution|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Đúng|  
|Địa chỉ Nội bộ|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Hóa đơn|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|InvoiceDetail|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|KbArticle|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Sai|Đúng|Đúng|Đúng|  
|KbArticleTemplate|Đúng|Sai|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|  
|Khách hàng tiềm năng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|LeadAddress|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Thư tín|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|Danh sách|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|Hộp thư|Đúng|Sai|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Sai|  
|MailMergeTemplate|Đúng|Đúng|Đúng|Đúng|Đúng|Sai|Đúng|Đúng|Đúng|Đúng|  
|Metric|Đúng|Đúng|Đúng|Đúng|Sai|Đúng|Sai|Đúng|Đúng|Đúng|  
|Cơ hội|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|OpportunityClose|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|OpportunityProduct|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|OrderClose|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Tổ chức|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Cuộc gọi Điện thoại |Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|PriceLevel|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Sai|  
|ProcessSession|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Đúng|Sai|  
|ProcessStage|Đúng|Sai|Đúng|Đúng|Sai|Sai|Sai|Sai|Đúng|Sai|  
|ProcessTrigger|Đúng|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Sản phẩm|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|ProductPriceLevel|Đúng|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Nhà phát hành|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Hàng đợi|Đúng|Đúng|Đúng|Đúng|Đúng|Sai|Đúng|Đúng|Đúng|Đúng|  
|QueueItem|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|Báo giá|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|QuoteClose|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|QuoteProduct|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|RecurringAppointmentMaster|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Sai|Đúng|Đúng|Đúng|  
|Báo cáo|Đúng|Sai|Sai|Sai|Sai|Đúng|Sai|Đúng|Đúng|Đúng|  
|ReportCategory|Đúng|Đúng|Đúng|Đúng|Đúng|Sai|Đúng|Đúng|Đúng|Sai|  
|Nguồn lực|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Nhóm Nguồn lực|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|ResourceGroupExpansion|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Vai trò|Đúng|Sai|Đúng|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|RolePrivileges|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Trường tổng số|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Đúng|  
|SalesLiterature|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|SalesOrder|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|SalesOrderDetail|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|Yêu cầu đã lưu|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|SavedQueryVisualization|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Dịch vụ |Đúng|Sai|Đúng|Sai|Sai|Đúng|Sai|Đúng|Đúng|Sai|  
|ServiceAppointment|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|SharePointDocumentLocation|Đúng|Đúng|Đúng|Đúng|Đúng|Sai|Đúng|Đúng|Đúng|Đúng|  
|Trang SharePoint|Đúng|Đúng|Đúng|Đúng|Đúng|Sai|Đúng|Đúng|Đúng|Đúng|  
|Trang|Đúng|Sai|Đúng|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Giải pháp|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Chủ đề|Đúng|Sai|Đúng|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Người dùng hệ thống|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|Nhiệm vụ|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|Nhóm|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Sai|  
|Mẫu Nhóm|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Sai|  
|Mẫu|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Đúng|Đúng|  
|Vùng lãnh thổ|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|Đúng|  
|TransactionCurrency|Đúng|Đúng|Đúng|Sai|Sai|Sai|Sai|Sai|Đúng|Đúng|  
|UoM|Đúng|Đúng|Đúng|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|UoMSchedule|Đúng|Sai|Đúng|Sai|Sai|Đúng|Sai|Đúng|Đúng|Sai|  
|UserQuery|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|UserQueryVisualization|Đúng|Sai|Sai|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
|Quy trình|Đúng|Sai|Đúng|Sai|Sai|Sai|Sai|Sai|Đúng|Sai|  
  
### <a name="see-also"></a>Xem thêm  
 [Using Managed Properties](use-managed-properties.md)   
 [Customize Entity Metadata](customize-entity-metadata.md)   
 [Create a Custom Entity](org-service/create-custom-entity.md)   
 [Change Entity Icons](modify-icons-entity.md)   
 [Change Entity Messages](modify-messages-entity.md)   
 [Sample: Create and Update Entity Metadata](org-service/sample-create-update-entity-metadata.md)
