---
title: Standard Web Application (Hosted Control) in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about Standard Web Application type of hosted control in Unified Service Desk.
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
ms.assetid: 0c2f9b12-07f1-455a-9e2d-9a51351f3188
caps.latest.revision: 12
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 91e1081a13f6f964ea92b6f966dce6e30295f6d4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387346"
---
# <a name="standard-web-application-hosted-control"></a>Standard Web Application (Hosted Control)
The **Standard Web Application** hosted control type is similar to the **CRM Page** type except that it is intended to host non-[!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps pages, such as external web pages, and provides script injection for relevant features of external web pages. Giống như kiểm soát tổ chức **Trang CRM**, các trang này có thể được tự động. Phương pháp tự động hóa được ưa thích đó là thông qua chèn [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] bao gồm gọi chức năng [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] đã được xác định trong trang hoặc thao tác DOM. Hành động `RunScript` cũng có thể được sử dụng để có được giá trị từ trang.  

> [!NOTE]
>  Loại kiểm soát tổ chức này không hỗ trợ [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)], giúp tạo điều kiện cho nhiệm vụ tự động hóa giao diện người dùng của ứng dụng tổ chức. HAT bao gồm các bộ điều hợp định hướng dữ liệu (DDA), quá trình tự động hóa và mối liên kết mô tả (quy trình làm việc của Windows) để tự động hóa các ứng dụng. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Use UII automation adapter to interact with external and web applications](../unified-service-desk/use-uii-automation-adapter-interact-external-web-applications.md)  

<a name="create"></a>   
## <a name="create-a-standard-web-application-hosted-control"></a>Tạo kiểm soát tổ chức ứng dụng Web tiêu chuẩn  
 While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create. Phần này cung cấp thông tin về các trường cụ thể là duy nhất đối với loại kiểm soát được lưu trữ của **Ứng dụng Web tiêu chuẩn**. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

 ![Standard Web Application hosted control](../unified-service-desk/media/crm-itpro-usd-standardwebapplicationhostedcontrol.png "Standard Web Application hosted control")  

 In the **New Hosted Control** screen:  

- Trong vùng **Unified Service Desk**, chọn **Ứng dụng Web tiêu chuẩn** từ danh sách thả xuống **Loại Thành phần USD**.  

- From the **Allow Multiple Pages** drop-down list, select **Yes** to automatically create a drop-down list when a second URL is called or a window navigation rule directs a page to the tab. This will allow the user to quickly search between the pages that are attached to this control. Nếu bạn chọn **Không**, khi [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] nhận được cuộc gọi hành động điều hướng hoặc trang được định tuyến đến tab, nó sẽ thay thế trang hiện đang được hiển thị và cập nhật lịch sử trình duyệt.  

- The **Hosting Type** drop-down list specifies how you want this control to be hosted. You can choose **IE Process** default or **Internal WPF**. For more information, see [Select a hosting method for hosted controls](../unified-service-desk/select-hosting-method-controls.md).  

- Under the **Common Properties** area, select the **Application is Global** check box to set the hosted control as global. Kiểm soát tổ chức chung có thể được hiển thị bên ngoài phiên khách hàng. Kiểm soát giống như bảng thông tin của tổng đài viên, tường hoặc tìm kiếm là những hình thức sử dụng chung cho kiểm soát tổ chức chung. Kiểm soát tổ chức chung không có trạng thái phiên dành riêng cho phiên để khi bạn thay đổi phiên, các kiểm soát tổ chức chung tương tự vẫn được duy trì. Nếu hộp kiểm không được chọn, kiểm soát tổ chức trở thành kiểu dựa trên phiên. Kiểm soát dựa trên phiên tồn tại trong ngữ cảnh của phiên khách hàng. Nếu người dùng thay đổi sang một phiên khác, tất cả các trang phiên từ phiên trước đó được ẩn.  

- In the **Display Group** field, specify a panel where this hosted control will be displayed. For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels](../unified-service-desk/panels-panel-types-panel-layouts.md#Panels).  

<a name="actions"></a>   
## <a name="predefined-uii-actions"></a>Predefined UII actions  
 Đây là những thao tác UII được xác định trước có sẵn cho loại kiểm soát tổ chức này.  

<a name="Close"></a>   
### <a name="close"></a>Đóng  
 This action is used to close the hosted control.  

### <a name="fireevent"></a>FireEvent  
 Khuyến khích sự kiện được người dùng xác định từ loại hình kiểm soát tổ chức này.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên của sự kiện do người dùng xác định.|  

 Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này. For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).  

### <a name="goback"></a>Quay lại  
 Hành động này là tương đương với việc nhấp vào nút quay lại trên phiên bản trình duyệt.  

### <a name="goforward"></a>Chuyển về phía trước  
 This action is equivalent to clicking the forward button on the browser instance.  

### <a name="gohome"></a>Về Trang chủ  
 This action goes to the initial URL specified for this browser instance.  

<a name="MoveToPanel"></a>   
### <a name="movetopanel"></a>MoveToPanel  
 This action is used to move hosted controls between panels at runtime.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|ứng dụng|Name of the hosted control to be moved.|  
|bảng điều khiển|Target panel for the hosted control.|  

### <a name="navigate"></a>Navigate  
 This action is used to navigate to a url.  


|     Tham số     |                                                                                                                                                                                                                                      Mô tả                                                                                                                                                                                                                                      |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        url        |                                                                                                                                                                                                                The URL to navigate to. This is a mandatory parameter.                                                                                                                                                                                                                 |
|      Noscan       |                                                                                                                                                                                          If this parameter is supplied and **True**, the data parameters will not be captured from the page.                                                                                                                                                                                          |
|  HideCommandBar   |                                                                                                                                                                                If this parameter is supplied and **True**, the inner frame will be displayed instead of loading the page command bar.                                                                                                                                                                                 |
| HideNavigationBar |                                                                                                                                                                                      If this parameter is supplied and **True**, the navigation panel on the target web page won't be displayed.                                                                                                                                                                                      |
|       Nền tảng       |                                                                                                                                                                        When frames exist on the page, this parameter would specify the name of the frame to navigate, rather than navigating the main window.                                                                                                                                                                         |
|     postdata      |                 Data that is sent to the server as part of a HTTPPOST transaction. A POST transaction is typically used to send data gathered by an HTML page. In [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], this data can be received from any event triggered using "<http://event/?>". Ví dụ: `[[postdata]+]`<br /><br /> Ngoài ra, dữ liệu có thể được thông qua như là chuỗi được mã hóa với loại tiêu đề trong định dạng dự định.                 |
|      tiêu đề       | Giá trị chuỗi chứa tiêu đề HTTP bổ sung để gửi tới máy chủ. Khi `postdata` tham số được sử dụng trong hành động `Navigate`, bạn cũng nên chỉ định giá trị thích hợp cho tham số `header`. Ví dụ: `Content-Type:application/x-www-form-urlencoded`<br /><br /> If a [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]POST event triggers the `Navigate` action, the default value of this parameter should be `header=[[header]+]` |

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

### <a name="runscript"></a>Chạy mã lệnh  
 This action injects JavaScript into the main frame of the application. You should avoid using [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps client SDK calls with this action; instead, use the **RunXrmCommand** action.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||The data parameter is the JavaScript that will be injected into the form. **Note:**  The replacement parameters can be used in the script, and they will be replaced before the script is executed.|  

<a name="SetSize"></a>   
### <a name="setsize"></a>SetSize  
 This action explicitly sets the width and height of the hosted control. Quá trình này đặc biệt hữu ích khi sử dụng tính năng "tự động" trong bố cục bảng điều khiển của bạn.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|chiều rộng|The width of the hosted control.|  
|chiều cao|The height of the hosted control.|  

### <a name="waitforcomplete"></a>Chờ để hoàn tất  
 Hành động này có thể được sử dụng để ngăn chặn việc xử lý cho đến khi URL hoàn tất tải.  

> [!NOTE]
>  Some web pages, particularly [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps pages, have multiple frames. Hành động này chỉ chờ nền tảng chính để hoàn tất.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|mili giây|Tham số tùy chọn để cho biết thời gian tính theo mili giây để đợi đến hết thời gian chờ.|  

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
 [Hành động UII](../unified-service-desk/uii-actions.md)   
 [Sự kiện](../unified-service-desk/events.md)   
 [View predefined actions and events for a hosted control](../unified-service-desk/view-predefined-actions-events-hosted-control.md)   
 [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md)   
 [Walkthrough 2: Display an external webpage in your agent application](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md)   
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)
