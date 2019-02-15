---
title: CTI Desktop Manager (Hosted Control) | MicrosoftDocs
description: Learn about using the CTI Desktop Manager hosted control type to plug in a computer telephony integration (CTI) adapter into Unified Service Desk to handle screen popping, call routing, softphone control, and other CTI functionalities.
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
ms.assetid: 9fb92472-39af-4816-84eb-4d5ffb8b4b4f
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 4c4ac1f0cb882b892b948c1ec447132dd8c1dbb0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387665"
---
# <a name="cti-desktop-manager-hosted-control"></a>CTI Desktop Manager (Hosted Control)
Use the **CTI Desktop Manager** hosted control type to plug in a computer telephony integration (CTI) adapter into [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to handle screen popping, call routing, softphone control, and other CTI functionalities.  

<a name="Create"></a>   
## <a name="create-a-cti-desktop-manager-hosted-control"></a>Tạo kiểm soát tổ chức Trình quản lý Máy tính để bàn CTI  
 For information about creating a CTI Desktop Manager and configuring the corresponding hosted control, see [Create a CTI Desktop Manager](../unified-service-desk/create-cti-desktop-manager.md).  

<a name="Actions"></a>   
## <a name="predefined-uii-actions"></a>Predefined UII actions  
 These are the predefined actions for this hosted control type.  

<a name="Close"></a>   
### <a name="close"></a>Đóng  
 This action is used to close the hosted control. Unlike the **CloseActive** action, if this tab (hosted control) is displaying more than one page, it will close all the pages displayed in the tab in your agent application.  

### <a name="closeandprompt"></a>Đóng và Nhắc  
 This action closes the hosted control, but prompts the user to save or abandon the changes before closing.  

### <a name="disabletoolbarbutton"></a>Tắt nút thanh công cụ  
 Hành động này vô hiệu hóa nút thanh công cụ được chỉ định trên thanh công cụ trong ứng dụng tổng đài viên của bạn.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||Tên của nút thanh công cụ để vô hiệu hóa.|  

### <a name="enabletoolbarbutton"></a>Bật nút thanh công cụ  
 Hành động này bật nút thanh công cụ được chỉ định trên thanh công cụ trong ứng dụng tổng đài viên của bạn.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||Name of the toolbar button to enable.|  

### <a name="find"></a>Find  
 Navigate to the quick find list view of the specified entity.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||The data parameter should specify the entity logical name of the quick find list view to display. There are some special case values:<br /><br /> -   Use **case** or **incident** to display the quick find list view for cases.<br />-   Use **advfind** to display the advanced find view.<br />-   Use **activities** or **activity** to display the quick find list view for activities.|  

### <a name="fireevent"></a>FireEvent  
 Fires a user-defined event from this hosted control.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên của sự kiện do người dùng xác định.|  

 Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này. For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).  

### <a name="goback"></a>Quay lại  
 This action is equivalent to clicking the back button on the browser instance.  

### <a name="goforward"></a>Chuyển về phía trước  
 This action is equivalent to clicking the forward button on the browser instance.  

### <a name="gohome"></a>Về Trang chủ  
 This action goes to the initial URL specified for this browser instance.  

### <a name="loadarea"></a>Vùng tải  
 This action loads a specific area from [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps. This is equivalent to selecting an area in the navigation pane (such as Sales, Service, and Marketing). Các tham số chỉ là tên của vùng nhấp vào. Ví dụ: **Vùng dịch vụ**.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|nền tảng|Tên nền tảng chịu ảnh hưởng. If no name is specified, it will automatically target the first frame found on the page.|  

<a name="MoveToPanel"></a>   
### <a name="movetopanel"></a>MoveToPanel  
 This action is used to move hosted controls between panels at runtime.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|ứng dụng|Name of the hosted control to be moved.|  
|bảng điều khiển|Target panel for the hosted control.|  

### <a name="navigate"></a>Navigate  
 This action is used to navigate to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps url.  


|     Tham số     |                                                                                                                                                                                                                                       Mô tả                                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        url        |                                                                                                                                                                                                                  The URL to navigate to. This is a mandatory parameter.                                                                                                                                                                                                                  |
|      Noscan       |                                                                                                                                                                                           If this parameter is supplied and **True**, the data parameters will not be captured from the page.                                                                                                                                                                                            |
|  HideCommandBar   |                                                                                                                                                        If this parameter is supplied and **True**, the inner frame will be displayed without loading the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps command bar.                                                                                                                                                        |
| HideNavigationBar |                                                                                                                                                          If this parameter is supplied and **True**, the form will be displayed without loading the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps navigation bar.                                                                                                                                                          |
|       Nền tảng       |                                                                                                                                                                          When frames exist on the page, this parameter would specify the name of the frame to navigate, rather than navigating the main window.                                                                                                                                                                          |
|     postdata      |                Data that is sent to the server as part of an HTTPPOST transaction. A POST transaction is typically used to send data gathered by an HTML page. In [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], this data can be received from any event triggered using "<http://event/?>". Ví dụ: `[[postdata]+]`<br /><br /> Alternatively, the data can be passed as an encoded string with its header type in the intended format.                 |
|      tiêu đề       | Giá trị chuỗi chứa tiêu đề HTTP bổ sung để gửi tới máy chủ. When the `postdata` parameter is used in the `Navigate` action, you should also specify an appropriate value for the `header` parameter. Ví dụ: `Content-Type:application/x-www-form-urlencoded`<br /><br /> If a [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]POST event triggers the `Navigate` action, the default value of this parameter should be `header=[[header]+]` |

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

### <a name="reroute"></a>Định tuyến lại  
 This action takes the currently displayed URL, and sends it through the window navigation rules from the current hosted control as a popup.  

### <a name="runscript"></a>Chạy mã lệnh  
 This action injects JavaScript into the main frame of the application. You should avoid using [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps client SDK calls with this action; instead, use the **RunXrmCommand** action.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||The data parameter is the JavaScript that will be injected into the form. **Note:**  The replacement parameters can be used in the script, and they will be replaced before the script is executed.|  

<a name="RunXrmCommand"></a>   
### <a name="runxrmcommand"></a>Chạy lệnh Xrm  
 This action is used to inject [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps SDK JavaScript into the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps form.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||The data parameter is the JavaScript that will be injected into the form. **Note:**  The replacement parameters can be used in the script, and they will be replaced before the script is executed.|  

### <a name="save"></a>Lưu  
 This action saves the current Dynamics 365 for Customer Engagement apps page.  

<a name="SaveAll"></a>   
### <a name="saveall"></a>Lưu tất cả  
 This action saves all forms in hosted control that allows multiple pages to be displayed (**Allow Multiple Pages** = Yes). If the hosted control allows only a single page to be displayed (**Allow Multiple Pages** = No), this is equivalent to the **Save** action.  

### <a name="saveandclose"></a>Lưu và Đóng  
 This action saves the dirty data on the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps form, and closes the hosted control.  

<a name="SetSize"></a>   
### <a name="setsize"></a>SetSize  
 This action explicitly sets the width and height of the hosted control. Quá trình này đặc biệt hữu ích khi sử dụng tính năng "tự động" trong bố cục bảng điều khiển của bạn.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|chiều rộng|The width of the hosted control.|  
|chiều cao|The height of the hosted control.|  

### <a name="togglenavigation"></a>Chuyển đổi điều hướng  
 This action collapses or expands the navigation pane on the left panel of the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps window. The navigation must contain a navigation panel for this action to work.  

### <a name="toggleribbon"></a>Chuyển đổi Ruy băng  
 This action collapses or expands the ribbon. Nếu bạn ẩn các ruy băng trong hành động **điều hướng**, ruy băng sẽ không được hiển thị và hành động này không hoạt động. Hành động này sẽ chỉ làm việc khi ruy băng đã được tải lúc đầu.  

### <a name="waitforcomplete"></a>Chờ để hoàn tất  
 This action can be used to block the processing until the URL finishes loading.  

> [!NOTE]
>  Some web pages, particularly [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps pages, have multiple frames. This action waits for only the main frame to complete.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|mili giây|Tham số tùy chọn để cho biết thời gian tính theo mili giây để đợi đến hết thời gian chờ.|  

<a name="Events"></a>   
## <a name="predefined-events"></a>Sự kiện được xác định trước  
 These are the predefined events for this hosted control type.  

### <a name="browserdocumentcomplete"></a>Duyệt Tài liệu hoàn chỉnh  
 Xảy ra khi trang đã hoàn tất tải.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|url|The URL of the page that has finished loading.|  

### <a name="frameloadcomplete"></a>FrameLoadComplete  
 Occurs any time when a frame has completed loading. Sự kiện này có thể xảy ra nhiều lần cho mỗi lần tải trang khi iFrame hoặc nền tảng được sử dụng trên trang. This event corresponds to the individual `BrowserDocumentComplete` events in code.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|nền tảng|The name of the frame that finished loading.|  
|url|URL của nền tảng đã hoàn tất tải.|  

### <a name="popuprouted"></a>Bật lên đã lên lịch  
 Xảy ra sau khi một cửa sổ bật lên đã được hệ thống xác định.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|url|The URL of the popup that was routed.|  

### <a name="see-also"></a>Xem thêm  
 [Integrate with CTI systems using CTI adapters](../unified-service-desk/integrate-cti-systems-cti-adapters.md)
