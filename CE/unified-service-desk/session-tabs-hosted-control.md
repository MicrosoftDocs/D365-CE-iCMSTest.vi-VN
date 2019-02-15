---
title: Session Tabs (Hosted Control) in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about Session Tabs type of hosted control in Unified Service Desk.
keywords: ''
ms.date: 08/17/2018
ms.service:
- dynamics-365-customerservice
ms.custom:
- dyn365-USD
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 590fe7cf-9281-41ee-ba7e-c0914ef9e44a
author: kabala123
ms.author: kabala
manager: shujoshi
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 7c359dc8d0a6124bcf619e912fd89b4e24ac28b3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388736"
---
# <a name="session-tabs-hosted-control"></a>Session Tabs (Hosted Control)
Sử dụng loại **Tab phiên** của kiểm soát tổ chức để hiển thị thông tin khách hàng trong tab phiên trong ứng dụng tổng đài viên của bạn. Kiểm soát tổ chức có thể đọc cấu hình dòng phiên cho cấu hình tên phiên và có thể đánh giá dòng phiên nào nên được sử dụng để tạo tên phiên. Một phiên bản của loại kiểm soát tổ chức này phải có sẵn trong ứng dụng tổng đài viên của bạn để hiển thị tab phiên. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Session management in Unified Service Desk](../unified-service-desk/session-management-unified-service-desk.md)  
  
<a name="Create"></a>   
## <a name="create-a-session-tab-hosted-control"></a>Tạo kiểm soát tổ chức tab phiên  
 While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create. Khi bạn chọn **tab phiên** từ danh sách thả xuống **Loại thành phần USD ** trong màn hình **Kiểm soát tổ chức mới**, bạn không phải chọn bất kỳ trường nào khác. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  
  
<a name="Actions"></a>   
## <a name="predefined-uii-actions"></a>Predefined UII actions  
 These are the predefined actions for this hosted control type.  
  
### <a name="chatagentindicator"></a>ChatAgentIndicator  
 Hành động này được sử dụng để chỉ ra rằng hệ thống đang chờ đợi tổng đài viên thực hiện hành động. Nó cũng sẽ hiển thị thời gian chỉ số tiến độ và đặt lại về 0.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|Id phiên|Đây là ID của phiên. ID cũng có thể được lấy từ bối cảnh sử dụng tham số thay thế: [[context.sessionid]]|  
  
### <a name="chatcustomerindicator"></a>ChatCustomerIndicator  
 Hành động này được sử dụng để chỉ ra rằng hệ thống đang chờ đợi khách hàng thực hiện hành động. Nó cũng sẽ hiển thị thời gian chỉ số tiến độ và đặt lại về 0.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|Id phiên|Đây là ID của phiên. ID cũng có thể được lấy từ bối cảnh sử dụng tham số thay thế: [[context.sessionid]]|  
  
### <a name="closesession"></a>Đóng phiên  
 Hành động này sẽ đóng một phiên. Trước khi đóng phiên, sự kiện **SessionClosing** được bắt đầu, tiếp theo là sự kiện **SessionClosed**.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|Id phiên|Đây là ID phiên mà bạn muốn đóng. Bạn nên chỉ định tham số này để đảm bảo rằng phiên làm việc bắt buộc đóng. Nếu tham số này không được cung cấp, hành động này đóng phiên hiện tại.|  
  
### <a name="fireevent"></a>FireEvent  
 Fires a user-defined event from this hosted control.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên của sự kiện do người dùng xác định.|  
  
 Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này. For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).  
  
### <a name="hidechatindicator"></a>HideChatIndicator  
 Hành động này được sử dụng chỉ để ẩn chỉ số trò chuyện.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|Id phiên|Đây là ID của phiên. The ID can also be retrieved from the context using the replacement parameter: [[context.sessionid]]|  
  
### <a name="hideprogressindicator"></a>HideProgressIndicator  
 Hành động này được sử dụng chỉ để ẩn chỉ số tiến độ.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|Id phiên|Đây là ID phiên giao dịch mà bạn muốn ẩn chỉ số tiến độ. The ID can also be retrieved from the context using the replacement parameter: [[context.sessionid]]|  
  
<a name="RealignWindow"></a>   
### <a name="realignwindow"></a>RealignWindow  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]
  
### <a name="resetprogressindicator"></a>ResetProgressIndicator  
 This action is used to reset the progress timer on the session tab. The progress indicator runs for 3 minutes.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|Id phiên|Đây là ID phiên giao dịch mà bạn muốn đặt lại chỉ số tiến độ. The ID can also be retrieved from the context using the replacement parameter: [[context.sessionid]]|

### <a name="switchsession"></a>SwitchSession  
 This action is used to switch the session between the local sessions. Also, switch from local to global session.
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|Id phiên|This is the ID of the global or local session. The global session ID can also be retrieved from the context using the replacement parameter: [[$Session.Global]g]</br>Ví dụ: `sessionid=[[$Session.Global]g]`| 
  
<a name="Events"></a>   
## <a name="predefined-events"></a>Sự kiện được xác định trước  
 The following predefined events are associated with this hosted control type. Bạn cũng có thể tạo sự kiện do người dùng xác định cho kiểm soát tổ chức. For information, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).  
  
### <a name="sessionclosed"></a>Đã đóng phiên  
 Xảy ra sau khi phiên được đóng lại.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|Id phiên|Đây là ID phiên đã bị đóng.|  
|IsGlobal|Trong phiên bản **trình quản lý chung** của sự kiện này, cờ IsGlobal cũng được thông qua. Nếu phiên chung đã đóng, cờ sẽ **Đúng**, nếu không, **sai**.|  
  
### <a name="sessioncloserequested"></a>SessionCloseRequested  
 Xảy ra khi "X" được nhấp vào trên một tab phiên làm việc trong các ứng dụng tổng đài viên. Nếu sự kiện này không được xử lý, Hệ thống sẽ tự động đóng phiên. Nếu sự kiện này được xử lý, Hệ thống sẽ không tự động đóng phiên và bạn phải đính kèm một cuộc gọi hành động cho sự kiện này mà gọi hành động **CloseSession** trên kiểm soát tổ chức **tab phiên** của bạn để đóng phiên một cách rõ ràng.  
  
### <a name="sessionclosing"></a>Đang đóng phiên  
 Xảy ra trước khi một phiên đã bị đóng.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|ID phiên|Đây là ID phiên đã bị đóng.|  
  
### <a name="see-also"></a>Xem thêm  
 [Session management in Unified Service Desk](../unified-service-desk/session-management-unified-service-desk.md)   
 [Session Lines (Hosted Control)](../unified-service-desk/session-lines-hosted-control.md)   
 [Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md)   
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)   
