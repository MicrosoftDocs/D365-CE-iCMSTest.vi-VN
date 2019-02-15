---
title: CRM Page (Hosted Control) | MicrosoftDocs
description: Learn about the CRM Page hosted control type to load a URL or page from Dynamics 365 for Customer Engagement apps. When a Dynamics 365 for Customer Engagement apps page is loaded within a hosted control of this type, it will automatically scan the page for data from the entity, and automatically populate the replacement parameters.
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
ms.assetid: 81102351-b49b-47fe-a28d-f70be86b20fd
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 70e7ebc1ed28d80f65a7a7ac6c055a394382d3b9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385583"
---
# <a name="crm-page-hosted-control"></a>CRM Page (Hosted Control)
Use the **CRM Page** hosted control type to load a URL or page from [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps. When a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps page is loaded within a hosted control of this type, it will automatically scan the page for data from the entity, and automatically populate the replacement parameters.  

 This hosted control type exposes a number of predefined UII actions and events that are unique to handling of Dynamics 365 for Customer Engagement apps windows including list manipulation actions, and a find action for displaying a quick search or advanced search page  

<a name="Create"></a>   
## <a name="create-a-crm-page-hosted-control"></a>Tạo kiểm soát tổ chức trang CRM  
 While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create. Phần này cung cấp thông tin về các trường cụ thể mà là duy nhất cho loại kiểm soát tổ chức **Trang CRM**. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

 ![Dynamics 365 for Customer Engagement apps page hosted control](../unified-service-desk/media/crm-itpro-usd-crmpagehostedcontrol.PNG "Dynamics 365 for Customer Engagement apps page hosted control")  

 In the **New Hosted Control** screen:  

- Trong vùng **Unified Service Desk**, chọn **Trang CRM** từ danh sách thả xuống **Loại Thành phần USD**.

- Select **Pre-fetch Data** to load related information for an entity record in the context along with the entity record page without having to wait for the full entity web page to load in the client application. Thông tin thực thể tìm nạp được điền trong ngữ cảnh [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] để kích hoạt mọi kiểm soát tổ chức nhằm nhanh chóng hiển thị thông tin thực thể có liên quan trên ứng dụng khách. Điều này có thể giúp tổng đài viên đưa ra hành động ngay lập tức, hoặc bắt đầu cuộc thảo luận với khách hàng, đồng thời tiết kiệm thời gian tương tác quan trọng.

- From the **Allow Multiple Pages** drop-down list, select **No** (default) to replace the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps page that is currently displayed, and update the browser history when [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] receives a navigate action call or a page is routed to the tab. Select **Yes** to automatically create a drop-down list when a second URL is called or a window navigation rule directs a page to the tab. This will allow the user to quickly search between the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps pages that are attached to this control. Also, when you select **Yes**, an additional field, **Maximum Browsers**, becomes available where you can specify the maximum number of pages to be displayed in the drop-down list.  

- Danh sách thả xuống **Loại tổ chức** xác định cách bạn muốn kiểm soát này được tổ chức. You can choose **IE Process** (default) or **Internal WPF** . For more information, see [Select a hosting method for hosted controls](../unified-service-desk/select-hosting-method-controls.md).  

- Dưới vùng **thuộc tính chung**, chọn hộp kiểm **Ứng dụng là ứng dụng chung** để thiết lập kiểm soát tổ chức là chung. Kiểm soát tổ chức chung có thể được hiển thị bên ngoài phiên khách hàng. Kiểm soát giống như bảng thông tin của tổng đài viên, tường hoặc tìm kiếm là những hình thức sử dụng chung cho kiểm soát tổ chức chung. Kiểm soát tổ chức chung không có trạng thái phiên dành riêng cho phiên để khi bạn thay đổi phiên, các kiểm soát tổ chức chung tương tự vẫn được duy trì. Nếu hộp kiểm không được chọn, kiểm soát tổ chức trở thành kiểu dựa trên phiên. Kiểm soát dựa trên phiên tồn tại trong ngữ cảnh của phiên khách hàng. Nếu người dùng thay đổi sang một phiên khác, tất cả các trang phiên từ phiên trước đó được ẩn.  

- Trường **Hiển thị nhóm** hiển thị bảng điều khiển nơi hiển thị kiểm soát tổ chức này. **Bảng điều khiển chính** là phổ biến nhất cho loại kiểm soát được lưu trữ này. For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md).  

  For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

<a name="actions"></a>   
## <a name="predefined-uii-actions"></a>Predefined UII actions  
 These are the predefined actions for this hosted control type.  

### <a name="associatedview"></a>Chế độ xem Liên kết  
 This action loads a specific associated view of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.  Những chế độ xem này thường được truy cập bằng cách nhấp vào mũi tên bên cạnh tên hồ sơ thực thể trong thanh điều hướng và chọn thực thể được liên kết.  


|  Tham số  |                                                 Mô tả                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| Điều hướng tên mục |                        Thực thể được liên kết mà bạn muốn hiển thị. Ví dụ: Trường hợp                        |
|     Id      |             ID của hồ sơ thực thể chính để hiển thị hồ sơ thực thể được liên kết.             |
|   tập hợp tab    | The area in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps. Ví dụ: vùng kinh doanh hoặc vùng dịch vụ. |

 For more information about using this action, see step 5 in [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md).  

<a name="Close"></a>   
### <a name="close"></a>Đóng  
 This action is used to close the hosted control. Không giống hành động **CloseActive**, nếu tab này (kiểm soát tổ chức) đang hiển thị nhiều hơn một trang, nó sẽ đóng tất cả các trang hiển thị trong tab trong ứng dụng tổng đài viên của bạn.  

<a name="CloseActive"></a>   
### <a name="closeactive"></a>CloseActive  
 Hành động này được sử dụng để đóng cửa sổ hiện hoạt trong kiểm soát tổ chức này. Nếu cửa sổ hiện hoạt là cửa sổ duy nhất được hiển thị trong kiểm soát tổ chức, kiểm soát tổ chức sẽ tự đóng. Với loại **Trang CRM** của kiểm soát tổ chức mà không cho phép nhiều trang (**cho phép nhiều trang** = Không), hành động này là tương đương với hành động **Đóng**.  

### <a name="closeandprompt"></a>Đóng và Nhắc  
 Hành động này đóng kiểm soát tổ chức nhưng nhắc người dùng lưu hoặc hủy thay đổi trước khi đóng.  

### <a name="disabletoolbarbutton"></a>Tắt nút thanh công cụ  
 Hành động này vô hiệu hóa nút thanh công cụ được chỉ định trên thanh công cụ trong ứng dụng tổng đài viên của bạn.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||Tên của nút thanh công cụ để vô hiệu hóa.|  

### <a name="enabletoolbarbutton"></a>Bật nút thanh công cụ  
 Hành động này bật nút thanh công cụ được chỉ định trên thanh công cụ trong ứng dụng tổng đài viên của bạn.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||Tên của nút thanh công cụ để bật.|  

### <a name="find"></a>Find  
 Điều hướng đến chế độ xem danh sách tìm nhanh của thực thể được chỉ định.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||Tham số dữ liệu nên chỉ định tên logic của thực thể của chế độ xem danh sách tìm nhanh để hiển thị. Có một số giá trị trường hợp đặc biệt:<br /><br /> -   Use **case** or **incident** to display the quick find list view for cases.<br />-   Use **advfind** to display the advanced find view.<br />-   Use **activities** or **activity** to display the quick find list view for activities.|  

### <a name="fireevent"></a>FireEvent  
 Khuyến khích sự kiện được người dùng xác định từ loại hình kiểm soát tổ chức này.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên của sự kiện do người dùng xác định.|  

 Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này. For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).  

### <a name="getselectedids"></a>Tải một số id đã chọn  
 Hành động này được sử dụng để truy xuất ID đã chọn từ danh sách.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||Tham số dữ liệu nên chỉ định tên danh sách để giữ ID đã chọn.|  

 Giá trị trả về chứa danh sách được phân tách bằng dấu chấm phẩy có chứa các mục đã chọn.  

### <a name="getselectedcount"></a>Tải số lượng đã chọn  
 Hành động này sẽ truy xuất số mục mà đã được chọn. Sử dụng hành động **Tải id đã chọn** để tải danh sách thực của ID cho thực thể.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||Tham số dữ liệu nên chỉ định tên danh sách để truy xuất ID đã chọn.|  

 Giá trị trả về chứa một số đại diện cho số lượng mục đã chọn.  

### <a name="gohome"></a>Về Trang chủ  
 Hành động này đi đến URL ban đầu được chỉ định cho phiên bản trình duyệt này.  

### <a name="goback"></a>Quay lại  
 Hành động này là tương đương với việc nhấp vào nút quay lại trên phiên bản trình duyệt.  

### <a name="goforward"></a>Chuyển về phía trước  
 Hành động này là tương đương với việc nhấp vào nút chuyển về phía trước trên phiên bản trình duyệt.  

### <a name="loadarea"></a>Vùng tải  
 This action loads a specific area from [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps. Điều này là tương đương với việc chọn vùng trong ngăn điều hướng (chẳng hạn như bán hàng, Dịch vụ, và tiếp thị). Các tham số chỉ là tên của vùng nhấp vào. Ví dụ: **Vùng dịch vụ**.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|nền tảng|Tên nền tảng chịu ảnh hưởng. Nếu không có tên được chỉ định, nó sẽ tự động nhắm mục tiêu nền tảng đầu tiên tìm thấy trên trang.|  

### <a name="lookupinfo"></a>Thông tin tra cứu  
 Displays a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps lookup information dialog box to allow you to select an entity from a list.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|Cho phép tắt bộ lọc|"0" hoặc "1" để cho phép người dùng tắt bộ lọc|  
|Loại mặc định|Tên logic của màn hình mặc định. Đây là một trong các giá trị số được chỉ định trong tham số loại đối tượng.|  
|ID chế độ xem mặc định|"0" hoặc "1" để hiển thị chế độ xem mặc định|  
|Tắt tìm kiếm nhanh|"0" hoặc "1" để hiển thị trường tìm kiếm nhanh|  
|Tắt trình chọn chế độ xem|"0" hoặc "1" để hiển thị bộ chọn chế độ xem|  
|Kiểu tra cứu|Một hoặc nhiều|  
|Hiển thị nút mới|"0" hoặc "1" để hiển thị nút mới|  
|Hiển thị nút thuộc tính|"0" hoặc "1" để hiển thị nút thuộc tính|  
|Duyệt|"0" hoặc "1" để xem có sử dụng chế độ duyệt web. Sau đây được đặt thành "1".|  
|Id hiện tại|Hướng dẫn cho giá trị hiện tại|  
|loại đối tượng|Danh sách các loại đối tượng để hiển thị. These are the etc types from Dynamics 365 for Customer Engagement apps. Ví dụ: "1,2" để hiển thị tài khoản và địa chỉ liên lạc.|  

<a name="MoveToPanel"></a>   
### <a name="movetopanel"></a>MoveToPanel  
 This action moves a CRM Page  hosted control to a different panel at runtime.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||The data parameter should specify the target panel name to move the hosted control to. Ví dụ: `FloatingPanel`.|  

### <a name="navigate"></a>Navigate  
 This action is used to navigate to a Dynamics 365 for Customer Engagement apps url.  


|     Tham số     |                                                                                                                                                                                                                                       Mô tả                                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        url        |                                                                                                                                                                                                                  URL để điều hướng đến. Đây là một tham số bắt buộc.                                                                                                                                                                                                                  |
|      Noscan       |                                                                                                                                                                                           Nếu tham số này được cung cấp và **Đúng**, các tham số dữ liệu sẽ không bị giữ lại từ trang.                                                                                                                                                                                            |
|  HideCommandBar   |                                                                                                                                                        If this parameter is supplied and **True**, the inner frame will be displayed without loading the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps command bar.                                                                                                                                                        |
| HideNavigationBar |                                                                                                                                                          If this parameter is supplied and **True**, the form will be displayed without loading the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps navigation bar.                                                                                                                                                          |
|       Nền tảng       |                                                                                                                                                                          Khi nền tảng tồn tại trên trang, tham số này sẽ xác định tên của nền tảng để điều hướng chứ không phải điều hướng cửa sổ chính.                                                                                                                                                                          |
|     postdata      |                Data that is sent to the server as part of an HTTPPOST transaction. A POST transaction is typically used to send data gathered by an HTML page. Trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], dữ liệu này có thể nhận được từ bất kỳ sự kiện được kích hoạt nào bằng cách sử dụng "<http://event/?>". Ví dụ: `[[postdata]+]`<br /><br /> Ngoài ra, dữ liệu có thể được thông qua dưới dạng chuỗi được mã hóa với loại tiêu đề trong định dạng dự định.                 |
|      tiêu đề       | Giá trị chuỗi chứa tiêu đề HTTP bổ sung để gửi tới máy chủ. Khi tham số `postdata` được sử dụng trong hành động `Navigate`, bạn cũng cần chỉ định giá trị phù hợp cho tham số `header`. Ví dụ: `Content-Type:application/x-www-form-urlencoded`<br /><br /> If a [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]POST event triggers the `Navigate` action, the default value of this parameter should be `header=[[header]+]` |

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

### <a name="refresh"></a>Refresh  
 Hành động này làm mới trang hiện tại.  

### <a name="reroute"></a>Định tuyến lại  
 Hành động này sẽ đưa URL đang được hiển thị và gửi URL đó qua nguyên tắc điều hướng cửa sổ từ kiểm soát tổ chức hiện tại làm cửa sổ bật lên.  

### <a name="runscript"></a>Chạy mã lệnh  
 Hành động này sẽ chèn JavaScript vào nền tảng chính của ứng dụng. You should avoid using [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps client SDK calls with this action; instead, use the **RunXrmCommand** action.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||Tham số dữ liệu là JavaScript sẽ được chèn vào biểu mẫu. **Note:**  The replacement parameters can be used in the script, and they will be replaced before the script is executed.|  

<a name="RunXrmCommand"></a>   
### <a name="runxrmcommand"></a>Chạy lệnh Xrm  
 This action is used to inject [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps SDK JavaScript into the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps form.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||The data parameter is the JavaScript that will be injected into the form. **Note:**  The replacement parameters can be used in the script, and they will be replaced before the script is executed.|  

<a name="SetSize"></a>   
### <a name="setsize"></a>SetSize  
 This action explicitly sets the width and height of the hosted control. Quá trình này đặc biệt hữu ích khi sử dụng tính năng "tự động" trong bố cục bảng điều khiển của bạn.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|chiều rộng|Chiều rộng của kiểm soát tổ chức.|  
|chiều cao|Chiều cao của kiểm soát tổ chức.|  

### <a name="saveandclose"></a>Lưu và Đóng  
 This action saves the dirty data on the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps form, and closes the hosted control.  

<a name="SaveAll"></a>   
### <a name="saveall"></a>Lưu tất cả  
 Hành động này lưu tất cả biểu mẫu trong kiểm soát tổ chức cho phép hiển thị nhiều trang (**cho phép nhiều trang** = Có). Nếu kiểm soát tổ chức chỉ cho phép hiển thị một trang (**Cho phép nhiều trang** = không), điều này tương đương với thao tác **Lưu**.  

### <a name="save"></a>Lưu  
 This action saves the current CRM Page.  

### <a name="toggleribbon"></a>Chuyển đổi Ruy băng  
 Hành động này thu nhỏ hoặc mở rộng ruy băng. Nếu bạn ẩn các ruy băng trong hành động **điều hướng**, ruy băng sẽ không được hiển thị và hành động này không hoạt động. Hành động này sẽ chỉ làm việc khi ruy băng đã được tải lúc đầu.  

### <a name="togglenavigation"></a>Chuyển đổi điều hướng  
 This action collapses or expands the navigation pane on the left panel of the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps window. Điều hướng phải chứa một bảng điều khiển điều hướng để thực hiện hành động này.  

<a name="events"></a>   
## <a name="predefined-events"></a>Sự kiện được xác định trước  
 Các sự kiện được xác định trước sau đây được liên kết với loại kiểm soát tổ chức này.  

### <a name="activeclosed"></a>Hiện hoạt đã đóng  
 Occurs when the active hosted control is closed using the [CloseActive](../unified-service-desk/crm-page-hosted-control.md#CloseActive) action.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|url|URL được hiển thị trong kiểm soát tổ chức khi bị đóng.|  

### <a name="browserdocumentcomplete"></a>Duyệt Tài liệu hoàn chỉnh  
 Xảy ra khi trang đã hoàn tất tải. Trên loại **Trang CRM** của kiểm soát tổ chức, sự kiện này xảy ra sau khi dữ liệu đã được lưu vào danh sách tham số thay thế. Sự kiện này chỉ xảy ra một lần, mặc dù nhiều nền tảng sẽ được khởi động riêng lẻ sự kiện **BrowserDocumentComplete** của chúng.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|url|URL của trang đã hoàn tất tải.|  

### <a name="dataready"></a>DataReady
Occurs as soon as the related information for an entity record is loaded in the [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] context. This event occurs before the **BrowserDocumentComplete** event. If the **Pre-Fetch Data** option is selected for the control instance then this event occurs as soon as the entity data is fetched in a separate parallel call to the server and will not wait for the full page to finish loading. The entity data is pre-fetched and the **DataReady** event is fired for inline navigations as well.

### <a name="pageloadcomplete"></a>Hoàn tất tải trang  
 Xảy ra bất cứ lúc nào khi tải nền tảng đã hoàn tất. Sự kiện này có thể xảy ra nhiều lần cho mỗi lần tải trang khi iFrame hoặc nền tảng được sử dụng trên trang. Sự kiện này tương ứng với các sự kiện **BrowserDocumentComplete** trong mã.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|nền tảng|Tên của nền tảng đã hoàn tất tải, nếu có.|  
|url|URL của nền tảng đã hoàn tất tải.|  

### <a name="popuprouted"></a>Bật lên đã lên lịch  
 Xảy ra sau khi một cửa sổ bật lên đã được hệ thống xác định.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|url|URL của cửa sổ bật lên đã được xác định.|  

### <a name="refreshrequested"></a>Làm mới được yêu cầu  
 Xảy ra khi làm mới được yêu cầu trên trang hiện tại. Làm mới có thể được yêu cầu hoặc bằng cách bấm phím F5 hoặc gọi hành động làm mới của ứng dụng.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|url|URL được hiển thị khi làm mới được yêu cầu.|  

### <a name="saved"></a>Đã lưu  
 Occurs after a record in the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps page is saved.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|id mới|ID được gán cho các hồ sơ mới được tạo.|  

### <a name="see-also"></a>Xem thêm  
 [Hộp thoại CRM (Kiểm soát tổ chức)](../unified-service-desk/crm-dialog-hosted-control.md)   
 [Hành động UII](../unified-service-desk/uii-actions.md)   
 [Sự kiện](../unified-service-desk/events.md)   
 [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md)   
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)   
 [Administration Guide for Unified Service Desk for Microsoft Dynamics 365 for Customer Engagement apps](http://go.microsoft.com/fwlink/p/?LinkID=394402)
