---
title: Unified Interface Page (Hosted Control) (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about the Unified Interface Page hosted control type to load a URL or page from Dynamics 365 for Customer Engagement apps. When a Dynamics 365 for Customer Engagement apps page is loaded within a hosted control of this type, it will automatically scan the page for data from the entity, and automatically populate the replacement parameters.
keywords: ''
ms.date: 04/24/2018
ms.service:
- usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 3AEB8475-FCBE-4526-8000-CF06CED9586C
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 2c3cfd04bf930d9707514c7ea32368b01e7bfa02
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388611"
---
# <a name="unified-interface-page-hosted-control"></a>Unified Interface Page (Hosted Control)
Use the **Unified Interface Page** hosted control type to load a URL or page from Unified Interface Apps in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps. When a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps page is loaded within a hosted control of this type, it will automatically scan the page for data from the entity, and automatically populate the replacement parameters.
  
 This hosted control type exposes a number of predefined UII actions and events that are unique to handling of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps [!INCLUDE[pn-ms-windows-short](../includes/pn-ms-windows-short.md)] including list manipulation actions, and a find action for displaying a quick search or advanced search page.

## <a name="create-a-unified-interface-page-hosted-control"></a>Create a Unified Interface Page hosted control

Trong khi tạo một hình thức kiểm soát tổ chức mới, các trường trong màn hình Kiểm soát tổ chức mới thay đổi dựa vào loại tổ chức tổ chức bạn muốn tạo. This section provides information about the specific fields that are unique to the Unified Interface Page hosted control type.

In the New Hosted Control screen:

- Under **[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]** area, select **Unified Interface Page** from the **USD Component Type** drop-down list.

- Select **Pre-fetch Data** to load related information for an entity record in the context along with the entity record page without having to wait for the full entity web page to load in the client application. Thông tin thực thể tìm nạp được điền trong ngữ cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để kích hoạt mọi kiểm soát tổ chức nhằm nhanh chóng hiển thị thông tin thực thể có liên quan trên ứng dụng khách. This could help agents instantly act or kick start discussion with customers, and save crucial interaction time.

- From the **Allow Multiple Pages** drop-down list, select **No** (default) to replace the Dynamics 365 for Customer Engagement apps page that is currently displayed, and update the browser history when [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] receives a navigate action call or a page is routed to the tab. Select **Yes** to automatically create a drop-down list when a second URL is called or a window navigation rule directs a page to the tab. This allows the user to quickly search between the Dynamics 365 for Customer Engagement apps pages that are attached to this control. Also, when you select **Yes**, an additional field, **Maximum Browsers**, becomes available where you can specify the maximum number of pages to be displayed in the drop-down list.

- Under the **Common Properties** area, select the **Application is Global** check box to set the hosted control as global. Kiểm soát tổ chức chung có thể được hiển thị bên ngoài phiên khách hàng. Kiểm soát giống như bảng thông tin của tổng đài viên, tường hoặc tìm kiếm là những hình thức sử dụng chung cho kiểm soát tổ chức chung. Kiểm soát tổ chức chung không có trạng thái phiên dành riêng cho phiên để khi bạn thay đổi phiên, các kiểm soát tổ chức chung tương tự vẫn được duy trì. Nếu hộp kiểm không được chọn, kiểm soát tổ chức trở thành kiểu dựa trên phiên. Kiểm soát dựa trên phiên tồn tại trong ngữ cảnh của phiên khách hàng. Nếu người dùng thay đổi sang một phiên khác, tất cả các trang phiên từ phiên trước đó được ẩn.

- Trường **Hiển thị nhóm** hiển thị bảng điều khiển nơi hiển thị kiểm soát tổ chức này. **MainPanel** is the most common for this hosted control type.

For information about other **General** fields, see Create or edit a hosted control.

## <a name="predefined-uii-actions"></a>Predefined UII actions

These are the predefined actions for this hosted control type.

### <a name="associatedview"></a>Chế độ xem Liên kết

This action loads a specific associated view of Dynamics 365 for Customer Engagement apps. These views are typically accessed by clicking down arrow next to an entity record name in the nav bar, and selecting the associated entities.

| Tham số         | Mô tả                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| etn               | The name of the entity for which you want to load list of records of the associated entity.  This is a mandatory parameter|
| ID                | The ID of the main entity record for which to display the associated entity records.                                    |
| navItemId         | Id of the navigation item corresponding to the associated entity. More information: [formContext.ui.navigation](/dynamics365/customer-engagement/developer/clientapi/reference/formcontext-ui-navigation)      |
| hideCommandBar    | If this parameter is supplied and False, the page will be displayed along with the Dynamics 365 for Customer Engagement apps command bar. |
| hideNavigationBar | If this parameter is supplied and False, the page will be displayed along with the Dynamics 365 for Customer Engagement apps navigation bar.     |

### <a name="close"></a>Đóng

This action is used to close the hosted control. Unlike the **CloseActive** action, if this tab (hosted control) is displaying more than one page, it will close all the pages displayed in the tab in your agent application.

### <a name="closeactive"></a>CloseActive

This action is used to close the active window within this hosted control. If the active window is the only window displayed in the hosted control, the hosted control itself will be closed. For **Unified Interface Page** type of hosted controls that do not allow multiple pages (**Allow Multiple Pages** = No), this action is equivalent to the **Close** action.

### <a name="closeandprompt"></a>Đóng và Nhắc

This action closes the hosted control, but prompts the user to save or abandon the changes before closing.

### <a name="find"></a>Find

Navigate to the quick find list view of the specified entity.

<table>
<thead>
<tr class="header">
<th><strong>Tham số</strong></th>
<th><strong>Mô tả</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Tham số dữ liệu nên chỉ định tên logic của thực thể của chế độ xem danh sách tìm nhanh để hiển thị. Có một số giá trị trường hợp đặc biệt:<br />
- Use <strong>case</strong> or <strong>incident</strong> to display the quick find list view for cases.<br />
- Use <strong>activities</strong> or <strong>activity</strong> to display the quick find list view for activities.</td>
</tr>
</tbody>
</table>

### <a name="fireevent"></a>FireEvent

Fires a user-defined event from this hosted control.

| Tham số | Mô tả                     |
|-----------|---------------------------------|
| tên      | Tên của sự kiện do người dùng xác định. |

Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này. For more information about creating a user-defined event, see [Create a user-defined event](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/create-user-defined-event).  

### <a name="getselectedids"></a>Tải một số id đã chọn

This action is used to retrieve the selected IDs from the lists.

| Tham số | Mô tả                                                                  |
|-----------|------------------------------------------------------------------------------|
|           | Tham số dữ liệu nên chỉ định tên danh sách để giữ ID đã chọn. |

Giá trị trả về chứa danh sách được phân tách bằng dấu chấm phẩy có chứa các mục đã chọn.

### <a name="getselectedcount"></a>Tải số lượng đã chọn

Hành động này sẽ truy xuất số mục mà đã được chọn. Sử dụng hành động **Tải id đã chọn** để tải danh sách thực của ID cho thực thể.

| Tham số | Mô tả                                                                   |
|-----------|-------------------------------------------------------------------------------|
|           | Tham số dữ liệu nên chỉ định tên danh sách để truy xuất ID đã chọn. |

The return value contains a number represented the quantity of selected items.

### <a name="gohome"></a>Về Trang chủ

This action goes to the initial URL specified for this browser instance.

### <a name="goback"></a>Quay lại

Hành động này là tương đương với việc nhấp vào nút quay lại trên phiên bản trình duyệt.

### <a name="goforward"></a>Chuyển về phía trước

This action is equivalent to clicking the forward button on the browser instance.

### <a name="movetopanel"></a>MoveToPanel

This action moves a Unified Interface Page hosted control to a different panel at runtime.

| Tham số | Mô tả                                                                                                        |
|-----------|--------------------------------------------------------------------------------------------------------------------|
|           | The data parameter should specify the target panel name to move the hosted control to. For example: FloatingPanel. |

### <a name="navigate"></a>Navigate

This action is used to navigate to a Dynamics 365 for Customer Engagement apps url. The App Id for the App that you select from **Select App Module** window is appended automatically.

<table>
<thead>
<tr class="header">
<th>Tham số</th>
<th>Mô tả</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>url</td>
<td>The URL to navigate to. This is a mandatory parameter.</td>
</tr>
<tr class="even">
<td>HideCommandBar</td>
<td>If this parameter is supplied and True, the inner frame will be displayed without loading the Dynamics 365 for Customer Engagement apps command bar.</td>
</tr>
<tr class="odd">
<td>HideNavigationBar</td>
<td>If this parameter is supplied and True, the form will be displayed without loading the Dynamics 365 for Customer Engagement apps navigation bar.</td>
</tr>
<tr class="even">
<td>Nền tảng</td>
<td>When frames exist on the page, this parameter would specify the name of the frame to navigate, rather than navigating the main window.</td>
</tr>
<tr class="odd">
<td>postdata</td>
<td>Data that is sent to the server as part of an HTTPPOST transaction. A POST transaction is typically used to send data gathered by an HTML page. In <!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]: Couldn&#39;t find file ../includes/pn-unified-service-desk.md. -->[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]<!--END ERROR INCLUDE -->, this data can be received from any event triggered using &quot;<a href="http://event/?" class="uri">http://event/?</a>&quot;. Example: [[postdata]+]<br />
<br />
Alternatively, the data can be passed as an encoded string with its header type in the intended format.</td>
</tr>
<tr class="even">
<td>tiêu đề</td>
<td>Giá trị chuỗi chứa tiêu đề HTTP bổ sung để gửi tới máy chủ. When the postdata parameter is used in the Navigate action, you should also specify an appropriate value for the header parameter. Example: Content-Type:application/x-www-form-urlencoded<br />
<br />
If a <!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]: Couldn&#39;t find file ../includes/pn-unified-service-desk.md. -->[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]<!--END ERROR INCLUDE -->POST event triggers the Navigate action, the default value of this parameter should be header=[[header]+]</td>
</tr>
</tbody>
</table>

### <a name="newcrmpage"></a>New\_CRM\_Page

Creates a page for creating a new Dynamics 365 for Customer Engagement apps record of the entity specified, and treats the page as a popup from the specified hosted control. Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi trang tạo hồ sơ thực thể được hiển thị.

| Tham số   | Mô tả                                                 |
|-------------|-------------------------------------------------------------|
| LogicalName | Tên logic của thực thể để tạo phiên bản mới. |

> [!Note]
> Phần còn lại của các tham số nên bao gồm tên = cặp giá trị. These are the additional pre-populated values in the form for creating a new record for the specified entity. 

### <a name="opencrmpage"></a>Open\_CRM\_Page

Opens an existing instance of the entity specified and identified by the ID, and treats the page as a popup from the specified hosted control. Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi thư mục bật lên nên sẽ được hiển thị.

| Tham số   | Mô tả                             |
|-------------|-----------------------------------------|
| LogicalName | Tên logic của thực thể hợp lý của thực thể để mở. |
| id          | ID của hồ sơ thực thể để mở.    |

### <a name="popup"></a>Bật lên

Bật lên URL từ kiểm soát tổ chức và chạy nguyên tắc điều hướng cửa sổ chống lại hình thức kiểm soát tổ chức để định tuyến bật lên đến vị trí thích hợp.

| Tham số | Mô tả                                                                                                        |
|-----------|--------------------------------------------------------------------------------------------------------------------|
| url       | Routes a popup from this hosted control using this URL as if it were a popup requested from the displayed control. |
| nền tảng     | The frame from which this popup originated.                                                                        |

### <a name="realignwindow"></a>RealignWindow

Hiển thị kiểm soát tổ chức tại một vị trí đã định trên màn hình. Bạn có thể hiển thị kiểm soát tổ chức trên tối đa hai màn hình. Hành động này áp dụng cho các phiên bản kiểm soát tổ chức được đặt cấu hình để đặt trên loại bảng điều khiển USDFloatingPanel hoặc USDFloatingToolPanel.

| Tham số | Mô tả                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| màn hình    | Chỉ định màn hình để hiển thị kiểm soát tổ chức. Các giá trị hợp lệ là 1 hoặc 2. Nếu bạn không chỉ định tham số này, giá trị 1 sẽ được dùng theo mặc định.                                                                                  |
| trái      | Chỉ định vị trí từ phía trái màn hình, theo tỷ lệ phần trăm, trên màn hình đích để hiển thị kiểm soát tổ chức. Các giá trị hợp lệ là từ 0 đến 100. Nếu bạn không chỉ định tham số này, giá trị 0 sẽ được dùng theo mặc định. |
| trên cùng       | Chỉ định vị trí từ phía trên cùng màn hình, theo tỷ lệ phần trăm, trên màn hình đích để hiển thị kiểm soát tổ chức. Các giá trị hợp lệ là từ 0 đến 100. Nếu bạn không chỉ định tham số này, giá trị 0 sẽ được dùng theo mặc định.  |
| chiều rộng     | Chỉ định chiều rộng của cửa sổ kiểm soát tổ chức theo tỷ lệ phần trăm trên màn hình đích. Các giá trị hợp lệ là từ 1 đến 100. Nếu bạn không chỉ định tham số này, giá trị 100 sẽ được dùng theo mặc định.                                              |
| chiều cao    | Chỉ định chiều cao của cửa sổ kiểm soát tổ chức theo tỷ lệ phần trăm trên màn hình đích. Các giá trị hợp lệ là từ 1 đến 100. Nếu bạn không chỉ định tham số này, giá trị 100 sẽ được dùng theo mặc định.                                             |

### <a name="refresh"></a>Refresh

This action refreshes the current page.

### <a name="runscript"></a>Chạy mã lệnh  
 This action injects JavaScript into the main frame of the application. You should avoid using [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps client SDK calls with this action; instead, use the **RunXrmCommand** action.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
||The data parameter is the JavaScript that will be injected into the form. **Note:**  The replacement parameters can be used in the script, and they will be replaced before the script is executed.|
| Nền tảng | When frames exist on the page, this parameter would specify the name of the frame to inject the JavaScript. |

  
### <a name="runxrmcommand"></a>Chạy lệnh Xrm  
 This action is used to run JavaScript code that uses [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps [Client API Reference](/dynamics365/customer-engagement/developer/clientapi/reference) into the Unified Interface Pages (entity forms and grids). 

 You must configure the script as a function of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps JavaScript webResource. The function's first parameter is a context parameter (reserved parameter) which may have one of the following values:

 - [FormContext](/dynamics365/customer-engagement/developer/clientapi/clientapi-form-context) on entity form pages
 - [GridContext](/dynamics365/customer-engagement/developer/clientapi/clientapi-grid-context) on entity grid pages
 - **undefined** on other pages
  
|Tham số|Mô tả|  
|---------------|-----------------|
| webResourceName | Name of the web resource in which the JavaScript function you want to execute is present. |
| functionName | Name of the function. |

The other parameters to the function are customer defined and can be used to pass Unified Service Desk’s replacement parameters at runtime. This action accepts a list of optional parameters without keys. The list of optional parameters are passed as arguments in the same order from second position after context replacement at runtime.

#### <a name="example"></a>Ví dụ

You want to execute **RunXrmCommand** action to fill the form attributes of a entity form, where the entity form is hosted by Unified Interface type of hosted control. The value you want to fill in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]'s perspective  is a replacement parameter - `[[$Context.Key1]]`.

In order to execute the action, you need to write JavaScript type web resource (say webResource1), and then write a function in the web resource.

```JavaScript
function fillAttributeValue(context, attrValue)
{
 context.getAttribute(<attributeName>).setValue(attrValue);
}   
```

You need to configure the data in the action call as follows:

```
webResourceName = webResource1
functionName = fillAttributeValue
‘[[$Context.Key1]]’
```
> [!Note]
> In the above example, observe the quotes around the replacement parameter - `[[$Context.Key1]]`. [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] considers only the value of the parameter (not the data type) and passes all the characters in context replaced value to the JavaScript function. You must be cautious and take care of the data type while configuring.

### <a name="setsize"></a>SetSize

This action explicitly sets the width and height of the hosted control. Quá trình này đặc biệt hữu ích khi sử dụng tính năng "tự động" trong bố cục bảng điều khiển của bạn.

| Tham số | Mô tả                       |
|-----------|-----------------------------------|
| chiều rộng     | The width of the hosted control.  |
| chiều cao    | The height of the hosted control. |

### <a name="saveandclose"></a>Lưu và Đóng

This action saves the dirty data on the Dynamics 365 for Customer Engagement apps form, and closes the hosted control.

### <a name="saveall"></a>Lưu tất cả

This action saves all forms in hosted control that allows multiple pages to be displayed (**Allow Multiple Pages** = Yes). If the hosted control allows only a single page to be displayed (**Allow Multiple Pages** = No), this is equivalent to the **Save** action.

### <a name="save"></a>Lưu

This action saves the current Unified Interface Page.

## <a name="predefined-events"></a>Sự kiện được xác định trước

The following predefined events are associated with this hosted control type.

### <a name="activeclosed"></a>Hiện hoạt đã đóng

Occurs when the active hosted control is closed using the [CloseActive](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/crm-page-hosted-control#CloseActive) action.  

| Tham số | Mô tả                                                          |
|-----------|----------------------------------------------------------------------|
| url       | The URL that was displayed in the hosted control when it was closed. |

### <a name="dataready"></a>DataReady

Occurs as soon as the related information for an entity record is loaded in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context. This event occurs before the **PageReadyFor** event. If the **Pre-Fetch Data** option is selected for the control instance then this event occurs as soon as the entity data is fetched in a separate parallel call to the server and will not wait for the full page to finish loading. The entity data is pre-fetched and the **DataReady** event is fired for inline navigations as well.

### <a name="refreshrequested"></a>Làm mới được yêu cầu

Occurs when refresh is requested on the current page. Làm mới có thể được yêu cầu hoặc bằng cách bấm phím F5 hoặc gọi hành động làm mới của ứng dụng.

| Tham số | Mô tả                                   |
|-----------|-----------------------------------------------|
| url       | The URL displayed when refresh was requested. |

### <a name="saved"></a>Đã lưu

Occurs after a record in the Dynamics 365 for Customer Engagement apps page is saved.

| Tham số | Mô tả                                  |
|-----------|----------------------------------------------|
| id mới     | The ID assigned to the newly created record. |

### <a name="navigationrequested"></a>NavigationRequested

Occurs when the navigation happens within Unified Interface apps

| Tham số | Mô tả                       |
|-----------|-----------------------------------|
| url       | The URL of the page navigated to. |

### <a name="pageready"></a>PageReady

Occurs when the page has finished loading. On a Unified Interface Page type of hosted control, this event occurs after the data has been saved to the replacement parameter list.

| Tham số | Mô tả                                    |
|-----------|------------------------------------------------|
| url       | The URL of the page that has finished loading. |

## <a name="see-also"></a>Xem thêm

[Support for Unified Interface Apps in Unified Service Desk](../unified-service-desk/admin/Support-unified-interfaces-apps-usd.md)
[Unified Service Desk and Unified Interface Configuration Walkthroughs](../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md)
[Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) 
[Walkthrough 2: Display an external webpage in your agent application](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md)   
[Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)   
[Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md)   
[Cách 5: Hiển thị thông tin phiên bổ sung bằng cách hiển thị tên và dữ liệu tổng quan về phiên](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md)   
[Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md)
[Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md) 
