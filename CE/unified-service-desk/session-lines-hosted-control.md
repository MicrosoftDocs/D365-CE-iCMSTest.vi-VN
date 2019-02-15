---
title: Session Lines (Hosted Control) in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about Session Lines type of hosted control in Unified Service Desk.
ms.custom:
- dyn365-USD
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 7dfc327f-4a42-44e6-be16-333fd9c4c277
caps.latest.revision: 8
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 2f86f4656a7c915a8f8ad5b0aec34b7b7c47d1bc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385705"
---
# <a name="session-lines-hosted-control"></a>Session Lines (Hosted Control)
Sử dụng loại **Dòng phiên** của kiểm soát tổ chức để đặt cấu hình thông tin tổng quan phiên cho các phiên trong ứng dụng tổng đài viên của bạn. This hosted control reads the overview information that you configure in your agent application using **Session Lines** (**Settings** > **Unified Service Desk** > **Session Lines**), and an instance of this hosted control type must be available in your agent application for the session overview information to be displayed. For more information about session overview, see [Session overview](../unified-service-desk/session-management-unified-service-desk.md#SessionOverview) and [Define session overview information](../unified-service-desk/configure-session-information.md#SessionOverview).  
  
<a name="Create"></a>   
## <a name="create-a-session-lines-hosted-control"></a>Tạo kiểm soát tổ chức dòng phiên  
 While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create. Phần này cung cấp thông tin về các trường cụ thể mà là duy nhất cho loại kiểm soát tổ chức **Dòng Phiên**. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  
  
 ![Create a Session Lines hosted control](../unified-service-desk/media/crm-itpro-usd-sessionlines.png "Create a Session Lines hosted control")  
  
 Trong màn hình Kiểm soát được lưu trữ mới:  
  
- Under **[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]** area, select **Session Lines** from the **USD Component Type** drop-down list.  
  
- Trường **Hiển thị nhóm** hiển thị bảng điều khiển nơi hiển thị kiểm soát tổ chức này. **Bảng điều khiển trình khám phá phiên** là bảng điều khiển phổ biến nhất cho loại kiểm soát tổ chức. For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md#Panels)  
  
  For information about **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  
  
<a name="Actions"></a>   
## <a name="predefined-uii-actions"></a>Predefined UII actions  
 These are the predefined actions for this hosted control type.  
  
### <a name="fireevent"></a>FireEvent  
 Fires a user-defined event from this hosted control.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên của sự kiện do người dùng xác định.|  
  
 Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này. For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).  
  
### <a name="realignwindow"></a>RealignWindow  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]
  
<a name="Events"></a>   
## <a name="predefined-events"></a>Sự kiện được xác định trước  
 Không có bất kỳ sự kiện được xác định trước nào cho loại kiểm soát tổ chức này.  
  
### <a name="see-also"></a>Xem thêm  
 [Session management in Unified Service Desk](../unified-service-desk/session-management-unified-service-desk.md)   
 [Session Tabs (Hosted Control)](../unified-service-desk/session-tabs-hosted-control.md)   
 [Cách 5: Hiển thị thông tin phiên bổ sung bằng cách hiển thị tên và dữ liệu tổng quan về phiên](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md)   
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)
