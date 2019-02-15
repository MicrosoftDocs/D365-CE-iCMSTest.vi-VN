---
title: CRM Dialog (Hosted Control) | MicrosoftDocs
description: Learn about using the CRM Dialog hosted control type to work with Dynamics 365 for Customer Engagement apps dialog. You can call the StartDialog action on your CRM Dialog hosted control to start a Dynamics 365 for Customer Engagement apps dialog within Unified Service Desk.
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
ms.assetid: b500941a-1b20-4c0e-b51e-511aeb07e52d
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
ms.openlocfilehash: 3c350e34eb402863026707dc002c1d57158bbc9d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388479"
---
# <a name="crm-dialog-hosted-control"></a>CRM Dialog (Hosted Control)
Use the **CRM Dialog** hosted control type to work with Dynamics 365 for Customer Engagement apps dialog. You can call the **StartDialog** action on your CRM Dialog hosted control to start a Dynamics 365 for Customer Engagement apps dialog within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  

<a name="Create"></a>   
## <a name="create-a-crm-dialog-hosted-control"></a>Tạo kiểm soát tổ chức hộp thoại CRM  
 While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create. Phần này cung cấp thông tin về các trường cụ thể mà là duy nhất cho loại kiểm soát tổ chức **Hộp thoại CRM**. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

 ![Dynamics 365 for Customer Engagement dialog hosted control](../unified-service-desk/media/crm-itpro-usd-crmdialoghostedcontrol.PNG "Dynamics 365 for Customer Engagement apps dialog hosted control")  

 In the **New Hosted Control** screen:  

- Trong vùng **Unified Service Desk**, chọn **Hộp thoại CRM** từ danh sách thả xuống **Loại Thành phần USD**.  

- Danh sách thả xuống **Loại tổ chức** xác định cách bạn muốn kiểm soát này được tổ chức. Bạn có thể chọn **WPF nội bộ** (mặc định) hoặc **Xử lý IE**. For more information, see [Select a hosting method for hosted controls](../unified-service-desk/select-hosting-method-controls.md).  

- Under the **Common Properties** area, select the **Application is Global** check box to set the hosted control as global. Kiểm soát tổ chức chung có thể được hiển thị bên ngoài phiên khách hàng. Kiểm soát giống như bảng thông tin của tổng đài viên, tường hoặc tìm kiếm là những hình thức sử dụng chung cho kiểm soát tổ chức chung. Kiểm soát tổ chức chung không có trạng thái phiên dành riêng cho phiên để khi bạn thay đổi phiên, các kiểm soát tổ chức chung tương tự vẫn được duy trì. Nếu hộp kiểm không được chọn, kiểm soát tổ chức trở thành kiểu dựa trên phiên. Kiểm soát dựa trên phiên tồn tại trong ngữ cảnh của phiên khách hàng. Nếu người dùng thay đổi sang một phiên khác, tất cả các trang phiên từ phiên trước đó được ẩn.  

- Trường **Hiển thị nhóm** hiển thị bảng điều khiển nơi hiển thị kiểm soát tổ chức này. **MainPanel** is the most common for this hosted control type. For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md#Panels). For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

<a name="actions"></a>   
## <a name="predefined-uii-actions"></a>Predefined UII actions  
 These are the predefined actions for this hosted control type.  

<a name="Close"></a>   
### <a name="close"></a>Đóng  
 This action is used to close the hosted control.  

### <a name="fireevent"></a>FireEvent  
 Khuyến khích sự kiện được người dùng xác định từ loại hình kiểm soát tổ chức này.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên của sự kiện do người dùng xác định.|  

 Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này. For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).  

<a name="MoveToPanel"></a>   
### <a name="movetopanel"></a>MoveToPanel  
 This action is used to move hosted controls between panels at runtime.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|ứng dụng|Name of the hosted control to be moved.|  
|bảng điều khiển|Target panel for the hosted control.|  

### <a name="newcrmpage"></a>New_CRM_Page  
 Creates a page for creating a new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps record of the entity specified, and treats the page as a popup from the specified hosted control. Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi trang tạo hồ sơ thực thể được hiển thị.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|LogicalName|Tên logic của thực thể để tạo phiên bản mới.|  

> [!NOTE]
>  Phần còn lại của các tham số nên bao gồm tên = cặp giá trị. These are the additional pre-populated values in the form for creating a new record for the specified entity. For more information about using this action, see step 4 in [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md).  

### <a name="opencrmpage"></a>Open_CRM_Page  
 Opens an existing instance of the entity specified and identified by the ID, and treats the page as a popup from the specified hosted control. Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi thư mục bật lên nên sẽ được hiển thị.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|LogicalName|Tên logic của thực thể hợp lý của thực thể để mở.|  
|id|ID của hồ sơ thực thể để mở.|  

### <a name="popup"></a>Bật lên  
 Bật lên URL từ kiểm soát tổ chức và chạy nguyên tắc điều hướng cửa sổ chống lại hình thức kiểm soát tổ chức để định tuyến bật lên đến vị trí thích hợp.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|url|Routes a popup from this hosted control using this URL as if it were a popup requested from the displayed control.|  
|nền tảng|The frame from which this popup originated.|  

<a name="RealignWindow"></a>   
### <a name="realignwindow"></a>RealignWindow  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]

<a name="SetSize"></a>   
### <a name="setsize"></a>SetSize  
 This action explicitly sets the width and height of the hosted control. Quá trình này đặc biệt hữu ích khi sử dụng tính năng "tự động" trong bố cục bảng điều khiển của bạn.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|chiều rộng|Chiều rộng của kiểm soát tổ chức.|  
|chiều cao|Chiều cao của kiểm soát tổ chức.|  

### <a name="startdialog"></a>Hộp thoại bắt đầu  
 Hành động này phải có một số thông số nhưng cho hộp thoại không liên quan đến một hồ sơ cụ thể, bạn chỉ có thể chỉ định các tham số **tên**.  


| Tham số |                                                                                      Mô tả                                                                                       |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Tên    |                        The name of the dialog as seen in the **Settings** > **Process** section of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.                        |
| DialogId  |                 Bạn cũng có thể chỉ định hộp thoại bằng ID. Nếu bạn chỉ định tham số **DialogId**, nó sẽ được sử dụng bởi các hành động thay vì các tham số **tên**.                 |
|  Thực thể   |    Đây là loại thực thể mà hộp thoại phải chạy chống lại. Điều này là bắt buộc nếu bạn sử dụng tham số **DialogId**. Nó là không cần thiết, nếu tham số **tên** được sử dụng.     |
|    Id     | Đây là ID của các thực thể mà phiên hộp thoại áp dụng. Nếu tham số này không được chỉ định, hộp thoại chạy chống lại sự xâm nhập đầu tiên của loại thích hợp trong hệ thống. |

 Khi hộp thoại kết thúc, nó sẽ nhắc người dùng đóng cửa sổ. Nếu người sử dụng khẳng định, tab trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] cũng sẽ đóng điều này do thiết kế.  

<a name="events"></a>   
## <a name="predefined-events"></a>Sự kiện được xác định trước  
 Các sự kiện được xác định trước sau đây được liên kết với loại kiểm soát tổ chức này.  

### <a name="browserdocumentcomplete"></a>Duyệt Tài liệu hoàn chỉnh  
 Xảy ra khi trang đã hoàn tất tải. Trên loại **Trang CRM** của kiểm soát tổ chức, sự kiện này xảy ra sau khi dữ liệu đã được lưu vào danh sách tham số thay thế. Sự kiện này chỉ xảy ra một lần, mặc dù nhiều nền tảng sẽ được khởi động riêng lẻ sự kiện **BrowserDocumentComplete** của chúng.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|url|URL của trang đã hoàn tất tải.|  

### <a name="popuprouted"></a>Bật lên đã lên lịch  
 Xảy ra sau khi một cửa sổ bật lên đã được hệ thống xác định.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|url|The URL of the popup that was routed.|  

### <a name="see-also"></a>Xem thêm  
 [Trang CRM (Kiểm soát tổ chức)](../unified-service-desk/crm-page-hosted-control.md)   
 [Hành động UII](../unified-service-desk/uii-actions.md)   
 [Sự kiện](../unified-service-desk/events.md)   
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)   
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)   
 [Administration Guide for Unified Service Desk for Microsoft Dynamics 365 for Customer Engagement apps](http://go.microsoft.com/fwlink/p/?LinkID=394402)
