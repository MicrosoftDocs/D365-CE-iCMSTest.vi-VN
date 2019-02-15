---
title: Toolbar Container (Hosted Control) | MicrosoftDocs
description: Learn about using Toolbar Container type of hosted control to configure toolbars in Unified Service Desk.
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
ms.assetid: d79dc1f2-cb40-4f8a-bb7c-5e6699a5ad0d
caps.latest.revision: 6
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 575199268b7984c4ac33e3adadb435cc474747b2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385801"
---
# <a name="toolbar-container-hosted-control"></a>Toolbar Container (Hosted Control)
Sử dụng loại **Bộ chứa thanh công cụ**kiểu kiểm soát tổ chức để tạo ra thanh công cụ trong ứng dụng của bạn, mà ứng dụng này có thể hiển thị danh sách các nút có hình ảnh và văn bản có thể thực hiện thao tác. Bạn có thể tạo nhiều loại bộ chứa thanh công cụ kiểu kiểm soát tổ chức và đặt chúng vào bất kỳ bảng nào trong ứng dụng. For more information about working with toolbars, see [Configure toolbars in your application](../unified-service-desk/configure-toolbars-application.md).  
  
<a name="Create"></a>   
## <a name="create-a-toolbar-container-hosted-control"></a>Tạo kiểm soát tổ chức của bộ chứa Thanh công cụ  
 While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create. Phần này cung cấp thông tin về các trường cụ thể là duy nhất đối với loại kiểm soát tổ chức của **bộ chứa thanh công cụ**. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  
  
 ![Toolbar Container hosted control](../unified-service-desk/media/crm-itpro-usd-toolbarhostedcontrol.png "Toolbar Container hosted control")  
  
 In the **New Hosted Control** screen:  
  
- Từ danh sách thả xuống **Loại thành phần USD**, chọn **Bộ chứa thanh công cụ**.  
  
- Trường **Hiển thị nhóm** hiển thị bảng điều khiển nơi hiển thị kiểm soát tổ chức này. **ToolbarPanel** là phổ biến nhất cho loại kiểm soát tổ chức này. For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels](../unified-service-desk/panels-panel-types-panel-layouts.md#Panels).  
  
<a name="Actions"></a>   
## <a name="predefined-uii-actions"></a>Predefined UII actions  
 These are the predefined actions for this hosted control type.  
  
### <a name="fireevent"></a>FireEvent  
 Fires a user-defined event from this hosted control.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên của sự kiện do người dùng xác định.|  
  
 Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này. For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).  
  
### <a name="hidetoolbar"></a>HideToolbar  
 Thao tác này ẩn thanh công cụ rõ ràng từ người dùng.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
||Chỉ định tên thanh công cụ để ẩn trong trường **Dữ liệu**.|  
  
### <a name="realignwindow"></a>RealignWindow  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]
  
### <a name="showtoolbar"></a>ShowToolbar  
 Thao tác này hiển thị thanh công cụ rõ ràng cho người dùng.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
||Chỉ định tên thanh công cụ để hiển thị trong trường **Dữ liệu**.|  
  
<a name="Events"></a>   
## <a name="predefined-events"></a>Sự kiện được xác định trước  
 Không có bất kỳ sự kiện được xác định trước cho loại kiểm soát tổ chức này.  
  
### <a name="see-also"></a>Xem thêm  
 [Đặt cấu hình thanh công cụ trong ứng dụng của bạn](../unified-service-desk/configure-toolbars-application.md)   
 [Hành động UII](../unified-service-desk/uii-actions.md)   
 [Sự kiện](../unified-service-desk/events.md)   
 [Tạo hoặc chỉnh sửa kiểm soát tổ chức](../unified-service-desk/create-edit-hosted-control.md)   
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)   
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)   
 [Administration Guide for Unified Service Desk for Microsoft Dynamics CRM](http://go.microsoft.com/fwlink/p/?LinkID=394402)
