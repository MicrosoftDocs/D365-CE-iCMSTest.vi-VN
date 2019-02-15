---
title: Interactive Service Hub Page (Hosted Control) in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The topic explains using the Interactive Service Hub Page hosted control type to host interactive service hub forms within Unified Service Desk to integrate the capabilities of both the applications. Interactive Service Hub provides an intuitive interface and displays all the vital information related to customers in one place that lets customer support agents focus on things that require attention.
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
ms.assetid: b318a432-a6ad-48d8-a8e0-e766b62dfe6f
caps.latest.revision: 18
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 0ac5affce35459d98a868810163e687db84476cf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386945"
---
# <a name="interactive-service-hub-page-hosted-control"></a>Interactive Service Hub Page (Hosted Control)
Use the **Interactive Service Hub Page** hosted control type to host  interactive service hub forms within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to integrate the capabilities of both the applications. Interactive Service Hub provides an intuitive interface and displays all the vital information related to customers in one place that lets customer support agents focus on things that require attention.  

 When an interactive service hub form  is loaded within the **Interactive Service Hub Page** hosted control, it will automatically scan the page for data, and automatically populate the replacement parameters in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. The **Interactive Service Hub Page** hosted control type exposes a number of predefined UII actions and events that are unique to handling of interactive service hub pages including list manipulation actions, and a find action for displaying a quick search or advanced search page.  

 Unified Service Desk provides you with a sample package, **Interactive Service Hub**, which demonstrates how easily you can integrate the interactive service hub pages within Unified Service Desk. More information: [Unified Service sample applications](admin/sample-unified-service-desk-applications.md)  

> [!NOTE]
>  You can convert your existing **CRM Page** type of hosted controls to the **Interactive Service Hub Page** type to display [interactive experience](https://go.microsoft.com/fwlink/?linkid=857057) forms used by the Interactive Service Hub application instead of the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps forms. However, there are some considerations in doing so. For more information, see [Blog: Support for Interaction Centric Forms within Unified Service Desk](https://blogs.msdn.microsoft.com/usd/2016/05/24/support-for-interaction-centric-forms-within-unified-service-desk/)  

<a name="Create"></a>   
## <a name="create-an-interactive-service-hub-page-hosted-control"></a>Create an Interactive Service Hub Page hosted control  
 While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create. This section provides information about the specific fields that are unique to the **Interactive Service Hub Page** hosted control type. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

 ![Interactive Service Hub Page hosted control](../unified-service-desk/media/interactive-service-hub-page-hosted-control.png "Interactive Service Hub Page hosted control")  

 In the **New Hosted Control** screen:  

- Under **Unified Service Desk** area, select **Interactive Service Hub Page** from the **USD Component Type** drop-down list.  

- From the **Allow Multiple Pages** drop-down list, select **No** (default) to replace the interactive service hub page that is currently displayed, and update the browser history when [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] receives a navigate action call or a page is routed to the tab. Select **Yes** to automatically create a drop-down list when a second URL is called or a window navigation rule directs a page to the tab. This will allow the user to quickly search between the interactive service hub pages that are attached to this control. Also, when you select **Yes**, an additional field, **Maximum Browsers**, becomes available where you can specify the maximum number of pages to be displayed in the drop-down list.  

- **IE Process** is the default **Hosting Type** for this hosted control type, and you cannot select any other hosting type . For information about supported hosting methods in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Select a hosting method for hosted controls](../unified-service-desk/select-hosting-method-controls.md).  

- Select the **Application is Global** check box to set the hosted control as global. Kiểm soát tổ chức chung có thể được hiển thị bên ngoài phiên khách hàng. Kiểm soát giống như bảng thông tin của tổng đài viên, tường hoặc tìm kiếm là những hình thức sử dụng chung cho kiểm soát tổ chức chung. Kiểm soát tổ chức chung không có trạng thái phiên dành riêng cho phiên để khi bạn thay đổi phiên, các kiểm soát tổ chức chung tương tự vẫn được duy trì. Nếu hộp kiểm không được chọn, kiểm soát tổ chức trở thành kiểu dựa trên phiên. Kiểm soát dựa trên phiên tồn tại trong ngữ cảnh của phiên khách hàng. Nếu người dùng thay đổi sang một phiên khác, tất cả các trang phiên từ phiên trước đó được ẩn.  

- Trường **Hiển thị nhóm** hiển thị bảng điều khiển nơi hiển thị kiểm soát tổ chức này. **MainPanel** is the most common for this hosted control type. For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md).  

- Select **Yes** or **No** from the **Application is Dynamic** list to specify whether this is a dynamic hosted control. Dynamics hosted controls allow an agent to start or close a hosted control on demand, either by using the UI or programmatically through code. More information: [Dynamic Unified Service Desk hosted controls](../unified-service-desk/unified-service-desk-hosted-controls.md#Dynamic)  

   If you select **Yes**, the **User Can Close** check box becomes available. Select this check box to let users close this hosted control.  

  For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

<a name="actions"></a>   
## <a name="predefined-uii-actions"></a>Predefined UII actions  
 These are the predefined actions for this hosted control type.  

> [!NOTE]
>  The **Interactive Service Hub Page** type of hosted control supports all the UII actions supported by the **Dynamics 365 for Customer Engagement apps page** type of hosted control. However, some UII actions are not available when you first create and save an instance of the **Interactive Service Hub Page** type hosted control. Any subsequent update to the hosted control instance adds the missing UII actions.  

### <a name="associatedview"></a>Chế độ xem Liên kết  
 This action loads a specific associated view of the interactive service hub.  These views are typically accessed by clicking down arrow next to an entity record name in the nav bar, and selecting the associated entities.  


|   Tham số   |                                                 Mô tả                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| `navItemName` |                        Thực thể được liên kết mà bạn muốn hiển thị. Ví dụ: Trường hợp                        |
|     `Id`      |             The ID of the main entity record for which to display the associated entity records.             |
|   `tabset`    | The area in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps. Examples: areaSales or areaService. |

<a name="Close"></a>   
### <a name="close"></a>Đóng  
 This action is used to close the hosted control. Unlike the **CloseActive** action, if this tab (hosted control) is displaying more than one page, it will close all the pages displayed in the tab in your agent application.  

<a name="CloseActive"></a>   
### <a name="closeactive"></a>CloseActive  
 This action is used to close the active window within this hosted control. Nếu cửa sổ hiện hoạt là cửa sổ duy nhất được hiển thị trong kiểm soát tổ chức, kiểm soát tổ chức sẽ tự đóng. If you have chosen not to allow multiple pages for your hosted control (**Allow Multiple Pages** = No), this action is equivalent to the **Close** action.  

### <a name="closeandprompt"></a>Đóng và Nhắc  
 This action prompts the user to save or abandon the changes before closing the hosted control.  

### <a name="find"></a>Find  
 Navigate to the quick find list view of the specified entity.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||The data parameter should specify the entity logical name of the quick find list view to display. There are some special case values:<br /><br /> Use `case` or `incident` to display the quick find list view for cases.<br /><br /> Use `advfind` to display the advanced find view.<br /><br /> Use `activities` or `activity` to display the quick find list view for activities.|  

### <a name="fireevent"></a>FireEvent  
 Fires a user-defined event from this hosted control.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`name`|Name of the user-defined event.|  

 Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này. For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).  

### <a name="getselectedcount"></a>Tải số lượng đã chọn  
 Hành động này sẽ truy xuất số mục mà đã được chọn. Sử dụng hành động **Tải id đã chọn** để tải danh sách thực của ID cho thực thể.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||Tham số dữ liệu nên chỉ định tên danh sách để truy xuất ID đã chọn.|  

 The return value contains a number represented the quantity of selected items.  

### <a name="getselectedids"></a>Tải một số id đã chọn  
 This action is used to retrieve the selected IDs from the lists.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||Tham số dữ liệu nên chỉ định tên danh sách để giữ ID đã chọn.|  

 Giá trị trả về chứa danh sách được phân tách bằng dấu chấm phẩy có chứa các mục đã chọn.  

### <a name="goback"></a>Quay lại  
 This action is equivalent to clicking the back button in the interactive service hub, which will take you back in the navigation stack of the interactive service hub.  

### <a name="gohome"></a>Về Trang chủ  
 This action takes you to the homepage specified by the user in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.  

<a name="MoveToPanel"></a>   
### <a name="movetopanel"></a>MoveToPanel  
 This action is used to move hosted controls between panels at runtime.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|ứng dụng|Name of the hosted control to be moved.|  
|bảng điều khiển|Target panel for the hosted control.|  

### <a name="navigate"></a>Navigate  
 This action is used to navigate to the interactive service hub URL.  


|     Tham số     |                                                                                                                                                                                                                                       Mô tả                                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        url        |                                                                                                                                                                                                                  The URL to navigate to. This is a mandatory parameter.                                                                                                                                                                                                                  |
|      Noscan       |                                                                                                                                                                                           If this parameter is supplied and **True**, the data parameters will not be captured from the page.                                                                                                                                                                                            |
|  HideCommandBar   |                                                                                                                                                                         If this parameter is supplied and **True**, the inner frame will be displayed without loading the interactive service hub  command bar.                                                                                                                                                                          |
| HideNavigationBar |                                                                                                                                                                            If this parameter is supplied and **True**, the form will be displayed without loading the interactive service hub navigation bar.                                                                                                                                                                            |
|     postdata      |                Data that is sent to the server as part of an HTTPPOST transaction. A POST transaction is typically used to send data gathered by an HTML page. In [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], this data can be received from any event triggered using "<http://event/?>". Ví dụ: `[[postdata]+]`<br /><br /> Alternatively, the data can be passed as an encoded string with its header type in the intended format.                 |
|      tiêu đề       | Giá trị chuỗi chứa tiêu đề HTTP bổ sung để gửi tới máy chủ. When the `postdata` parameter is used in the `Navigate` action, you should also specify an appropriate value for the `header` parameter. Ví dụ: `Content-Type:application/x-www-form-urlencoded`<br /><br /> If a [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]POST event triggers the `Navigate` action, the default value of this parameter should be `header=[[header]+]` |

### <a name="newcrmpage"></a>New_CRM_Page  
 Creates a page for creating a new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps record of the entity specified, and treats the page as a popup from the specified hosted control. Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi trang tạo hồ sơ thực thể được hiển thị.  

 You can pass attribute values in name=value pairs as data parameters for this action. Ví dụ:  

```  
LogicalName=incident  
title=Sample Case  

```  

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

<a name="RealignWindow"></a>   
### <a name="realignwindow"></a>RealignWindow  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]

### <a name="refresh"></a>Refresh  
 This action refreshes the current page.  

### <a name="reroute"></a>Định tuyến lại  
 This action takes the currently displayed URL, and sends it through the window navigation rules from the current hosted control as a popup.  

### <a name="runscript"></a>Chạy mã lệnh  
 This action injects JavaScript into the main frame of the application. You should avoid using [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps client SDK calls with this action; instead, use the **RunXrmCommand** action.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||Tham số dữ liệu là JavaScript sẽ được chèn vào biểu mẫu.<br /><br /> Các tham số thay thế có thể được sử dụng trong mã lệnh và chúng sẽ được thay thế trước khi thực thi mã lệnh.|  

<a name="RunXrmCommand"></a>   
### <a name="runxrmcommand"></a>Chạy lệnh Xrm  
 This action is used to inject [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps SDK JavaScript into the interactive service hub form.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||The data parameter is the JavaScript that will be injected into the form.<br /><br /> The replacement parameters can be used in the script, and they will be replaced before the script is executed.|  

### <a name="save"></a>Lưu  
 This action saves the current data on the interactive service hub form.  

<a name="SaveAll"></a>   
### <a name="saveall"></a>Lưu tất cả  
 This action saves all forms in hosted control that allows multiple pages to be displayed (**Allow Multiple Pages** = Yes). If the hosted control allows only a single page to be displayed (**Allow Multiple Pages** = No), this is equivalent to the **Save** action.  

### <a name="saveandclose"></a>Lưu và Đóng  
 This action saves the current data on the interactive service hub form, and closes the hosted control.  

<a name="SetSize"></a>   
### <a name="setsize"></a>SetSize  
 This action explicitly sets the width and height of the hosted control. This is particularly useful when using "auto" in your panel layouts.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`width`|The width of the hosted control.|  
|`height`|The height of the hosted control.|  

<a name="events"></a>   
## <a name="predefined-events"></a>Sự kiện được xác định trước  
 The following predefined events are associated with this hosted control type.  

### <a name="activeclosed"></a>Hiện hoạt đã đóng  
 Occurs when the active hosted control is closed using the [CloseActive](../unified-service-desk/crm-page-hosted-control.md#CloseActive) action.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`url`|The URL that was displayed in the hosted control when it was closed.|  

### <a name="dataready"></a>DataReady  
 Occurs after the data in the interactive service page has been saved to the replacement parameter list.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`url`|URL của trang.|  

### <a name="navigationrequested"></a>NavigationRequested  
 Occurs when navigation happens within the interactive service hub.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`url`|The URL of the page navigated to.|  

### <a name="refreshrequested"></a>Làm mới được yêu cầu  
 Xảy ra khi làm mới được yêu cầu trên trang hiện tại. Làm mới có thể được yêu cầu hoặc bằng cách bấm phím F5 hoặc gọi hành động làm mới của ứng dụng.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`url`|The URL displayed when refresh was requested.|  

### <a name="saved"></a>Đã lưu  
 Occurs after a record in the interactive service hub page is saved.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`newId`|The ID assigned to the newly created record.|  

### <a name="see-also"></a>Xem thêm  
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)   
 [Dynamics 365 for Customer Engagement apps page (Hosted Control)](../unified-service-desk/crm-page-hosted-control.md)
