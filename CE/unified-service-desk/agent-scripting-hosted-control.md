---
title: Agent Scripting (Hosted Control) | MicrosoftDocs
description: Learn about using Agent Scripting type of hosted control to define a call script that provides instructions to the call center agent to guide them during a customer interaction for a given session.
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
ms.assetid: 4d34fda6-6b17-4c94-8881-39962c85e6d0
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
ms.openlocfilehash: 9173e687f848ff12485cd002405c99558842284a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388477"
---
# <a name="agent-scripting-hosted-control"></a>Agent Scripting (Hosted Control)
Sử dụng loại kiểm soát tổ chức **Mã lệnh tổng đài viên** để xác định mã lệnh cuộc gọi mà cung cấp hướng dẫn cho tổng đài viên trung tâm cuộc gọi để hướng dẫn họ trong suốt quá trình tương tác khách hàng cho phiên nhất định. For more information, see [Guide customer interactions with agent scripts](../unified-service-desk/guide-customer-interactions-agent-scripts.md).  
  
<a name="AgentScripting"></a>   
## <a name="create-an-agent-scripting-hosted-control"></a>Tạo kiểm soát tổ chức mã lệnh tổng đài viên  
 While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create. Phần này cung cấp thông tin về các trường cụ thể mà là duy nhất cho loại kiểm soát tổ chức **Mã lệnh tổng đài viên**. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  
  
  <!-- Missing graphic below--> <!-- ![Agent scripting hosted control](../unified-service-desk/media/usd-agent-scripthostedcontrol.PNG "Agent scripting hosted control")  -->
  
 Trong màn hình **Kiểm soát tổ chức mới**, dưới khu vực **Unified Service Desk**, chọn **Mã lệnh tổng đài viên** từ danh sách thả xuống **Loại Thành phần USD**. WorkflowPanel là bảng phổ biến nhất cho loại kiểm soát tổ chức này và loại tương tự được hiển thị trong trường **Hiển thị nhóm**. For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md). For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  
  
<a name="actions"></a>   
## <a name="predefined-uii-actions"></a>Predefined UII actions  
 Hành động sau đây được hỗ trợ cho loại kiểm soát tổ chức này.  
  
### <a name="back"></a>Back  
 Trở về bước trước trong lịch sử.  
  
<a name="Close"></a>   
### <a name="close"></a>Đóng  
 This action is used to close the hosted control.  
  
### <a name="fireevent"></a>FireEvent  
 Khuyến khích sự kiện được người dùng xác định từ loại hình kiểm soát tổ chức này.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên của sự kiện do người dùng xác định.|  
  
 Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này. For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).  
  
<a name="GoToTask"></a>   
### <a name="gototask"></a>Đi đến tác vụ  
 Hành động này sẽ hiển thị nhiệm vụ tổng đài viên được chỉ định. The available agent task names can be seen in the **Agent Scripts** section in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps (**Settings** > **Agent Scripts**).  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
||Chỉ định tên của nhiệm vụ tổng đài viên để hiển thị trong trường **dữ liệu**.|  
  
### <a name="gototaskbycontext"></a>GoToTaskByContext  
 Hoạt động này bị phản đối. Sử dụng hoạt động **GoToTask**.  
  
### <a name="gototaskbydnis"></a>GotoTaskByDnis  
 Hoạt động này bị phản đối. Sử dụng hoạt động **GoToTask**.  
  
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
|chiều rộng|The width of the hosted control.|  
|chiều cao|The height of the hosted control.|  
  
<a name="ShowSendButton"></a>   
### <a name="showsendbutton"></a>ShowSendButton  
 Hành động này sẽ hiển thị nút **gửi** trên mã lệnh tổng đài viên trong ứng dụng khách. This button is typically used for chat sessions, and when the user clicks the button, the [SendClicked](../unified-service-desk/agent-scripting-hosted-control.md#SendClicked) event is fired, which is used to write the script text to the chat window.  
  
<a name="events"></a>   
## <a name="predefined-events"></a>Sự kiện được xác định trước  
 Các sự kiện được xác định trước sau đây được liên kết với loại kiểm soát tổ chức này.  
  
### <a name="allanswersvisited"></a>AllAnswersVisited  
 Xảy ra khi tất cả các câu trả lời cho nhiệm vụ hiện tại đã được nhấp. Điều này là hữu ích cho danh sách kiểm tra. Về cơ bản, mỗi câu trả lời được chỉ quay lại cùng một nhiệm vụ. Vì vậy khi bạn nhấp vào nút, chúng sẽ hiển thị các hộp kiểm bên cạnh chúng. Sau khi tất cả được chọn, sự kiện này được bắt đầu.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|nhiệm vụ|Tên nhiệm vụ mà khi tất cả các câu trả lời đã được nhấp.|  
|id|ID của nhiệm vụ mà khi tất cả các câu trả lời đã được nhấp.|  
  
<a name="SendClicked"></a>   
### <a name="sendclicked"></a>SendClicked  
 Xảy ra khi nút **gửi** trên mã lệnh tổng đài viên trong ứng dụng khách được nhấp. To display the **Send** Button, you should call the [ShowSendButton](../unified-service-desk/agent-scripting-hosted-control.md#ShowSendButton) action.  
  
### <a name="taskupdated"></a>TaskUpdated  
 Xảy ra mỗi khi mã lệnh tổng đài viên được đạt tới, cho dù do người dùng nhấp vào một câu trả lời, hoặc bởi một số thành phần gọi một trong những hành động trên kiểm soát tổ chức này.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|nhiệm vụ|Tên của nhiệm vụ mã lệnh tổng đài viên mà đã đạt được. Với menu chính, mà không phải là một nhiệm vụ được liệt kê trong cấu hình của mã lệnh tổng đài viên, một sự kiện được bắt đầu bằng tham số này được thành "[Menu chính]".|  
  
### <a name="see-also"></a>Xem thêm  
 [Guide customer interactions with agent scripts](../unified-service-desk/guide-customer-interactions-agent-scripts.md)   
 [Cấu hình và quản lý mã lệnh tổng đài viên](../unified-service-desk/configure-manage-agent-scripts.md)   
 [Hành động UII](../unified-service-desk/uii-actions.md)   
 [Sự kiện](../unified-service-desk/events.md)   
 [View predefined actions and events for a hosted control](../unified-service-desk/view-predefined-actions-events-hosted-control.md)   
 [View embedded help for actions and events](../unified-service-desk/view-embedded-help-for-actions-and-events.md)   
 [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md)   
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)   
 [Administration Guide for Unified Service Desk for Microsoft Dynamics CRM](http://go.microsoft.com/fwlink/p/?LinkID=394402)
