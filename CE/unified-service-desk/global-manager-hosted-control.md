---
title: Global Manager (Hosted Control) in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The Global Manager hosted control type is the core of Unified Service Desk, and an instance of this hosted control is required by Unified Service Desk.
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
ms.assetid: 8f45a5fd-2b39-4336-8326-f43dabf4389f
caps.latest.revision: 14
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: f7a250631e44650d92f33a31212149503be04ed9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386941"
---
# <a name="global-manager-hosted-control"></a>Global Manager (Hosted Control)
Loại kiểm soát tổ chức **trình quản lý chung** là cốt lõi của [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] và phiên bản của kiểm soát tổ chức này theo yêu cầu của [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. This hosted control loads and reads all the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration data from [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps at application startup, interprets the window navigation rules, provides data to the toolbar components and agent scripts, and manages the data for the session. Chỉ có thể tải phiên bản đơn của loại kiểm soát tổ chức **trình quản lý chung**.  

> [!IMPORTANT]
>  The three sample application packages for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], `New Environment`, `CRM Web Client`, and `Interactive Service Hub`, come preconfigured with an instance each of the **Global Manager** hosted control type. For information about the sample applications, see [Deploy sample Unified Service Desk applications to CRM server using Package Deployer](admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md).  

 Ngoài việc cung cấp giải thích cho hầu hết các chức năng trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], loại kiểm soát tổ chức **trình quản lý chung** cũng cung cấp các tính năng đa ngôn ngữ trong hệ thống để bạn có thể bản địa hoá các chuỗi và tin nhắn trong giao diện người dùng trong ứng dụng của bạn bằng nhiều ngôn ngữ. For more information, see [Add multilanguage support for your agent applications](../unified-service-desk/add-multilanguage-support-agent-applications.md). Nó cũng cung cấp các nhà cung cấp dịch vụ tìm kiếm, các nhà cung cấp này được tạo ra cho mục đích chung và có thể thích ứng qua quá trình cấu hình.  

<a name="CreateGlobal"></a>   
## <a name="create-a-global-manager-hosted-control"></a>Tạo kiểm soát tổ chức Trình quản lý chung  
 While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create. Phần này cung cấp thông tin về các trường cụ thể mà là duy nhất cho loại kiểm soát tổ chức **Trình quản lý chung**. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

 ![Global Manager hosted control](../unified-service-desk/media/crm-itpro-usd-globalmanagerhostedcontrol.PNG "Global Manager hosted control")  

 Trong màn hình **Kiểm soát tổ chức mới**, dưới khu vực **Unified Service Desk**, chọn **trình quản lý chung** từ danh sách thả xuống **Loại Thành phần USD**. Also, ensure that you set the **Sort Order** value of this hosted control to **2** to ensure it is loaded by your agent application immediately *after* the connection has been established to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps using the Connection Manager hosted control. For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

 Sau khi bạn lưu hồ sơ, vùng **dịch vụ ngôn ngữ** có sẵn khi bạn thêm tài nguyên để thêm chuỗi đã được bản địa hóa cho giao diện ứng dụng của ứng dụng tổng đài viên của bạn. For information about how to add language resources, see [Add multilanguage support for your agent applications](../unified-service-desk/add-multilanguage-support-agent-applications.md).  

<a name="predefined"></a>   
## <a name="predefined-uii-actions"></a>Predefined UII actions  
 Global Manager provides a series of predefined actions that allow you to manipulate [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps record data through the web services. These can be used during configuration to perform advanced functions in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.  

 Hành động UII được xác định trước sau đây có sẵn cho loại kiểm soát tổ chức **trình quản lý chung**:  

<a name="Audit"></a>   
### <a name="audit"></a>Kiểm tra  
 Thêm mục nhập kiểm tra vào bản ghi kiểm tra [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. For more information, see [Configure auditing in Unified Service Desk](admin/configure-auditing-diagnostics-unified-service-desk.md)  

|Tham số|Mô tả|  
|---------------|-----------------|  
|Tên|Tên mục kiểm tra. You must add an option under the **Options** area (**Settings** > **Unified Service Desk** > Options ([How do I get there?](http://go.microsoft.com/fwlink/p/?LinkId=525636))) with the value set to **1**.|  
|Hành động|Chuỗi đại diện cho hành động mà đang được kiểm tra.|  
|TargetApplication|Chuỗi đại diện cho ứng dụng mục tiêu để kiểm tra.|  
|Id Khách hàng|Chuỗi đại diện cho ID khách hàng của bạn.|  
|Id ngữ cảnh|Chuỗi đại diện cho ID ngữ cảnh của bạn.|  
|Id ứng dụng|GUID của kiểm soát tổ chức để kiểm tra.|  
|Trạng thái tổng đài viên|Chuỗi đại diện cho trạng thái tổng đài viên|  
|Dữ liệu hoạt động|Đây là các dữ liệu để viết vào các mục kiểm tra. Nếu tham số này không được cung cấp rõ ràng, tham số sẽ sử dụng tất cả các dòng còn lại trong trường **Dữ liệu** của định nghĩa cuộc gọi hành động.|  

<a name="CallDoAction"></a>   
### <a name="calldoaction"></a>CallDoAction  
 Gọi hành động trên kiểm soát tổ chức khác.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|bảng điều khiển|Đây là bảng điều khiển để tìm ứng dụng hiện hoạt, nếu không có ứng dụng nào được chỉ định.|  
|hành động|Đây là hành động được gọi trên kiểm soát tổ chức.|  
|dữ liệu|Đây là tham số dữ liệu để vượt qua hành động.|  
|ứng dụng|Đây là tên kiểm soát tổ chức mà bạn muốn thực hiện một cuộc gọi hành động. Nếu điều này được chỉ định, thông số **bảng điều khiển** được bỏ qua.|  

<a name="ClearAppBar"></a>   
### <a name="clearappbar"></a>Xóa thanh ứng dụng  
 Hủy đặt kiểm soát tổ chức đã chỉ định trong ứng dụng khách.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|Tên ứng dụng|Tên của kiểm soát tổ chức để bỏ gắn. Nếu tham số này không được cung cấp, cửa sổ chính của ứng dụng khách sẽ bị bỏ chặn.|  

<a name="ClearEntityList"></a>   
### <a name="clearentitylist"></a>ClearEntityList  
 Xóa danh sách kết quả tìm kiếm tích lũy và luôn được gọi trước khi gọi hành động **DoSearch**  

|Tham số|Mô tả|  
|---------------|-----------------|  
|chung|`True`nếu bạn muốn kết quả tìm kiếm gắn với phiên làm việc chung được xoá. Bạn phải cẩn thận trong khi lưu trữ kết quả tìm kiếm trong phiên chung vì những kết quả này không được hệ thống xóa tự động. Trong trường hợp này, bạn phải gọi thao tác **ClearEntityList** trước khi gọi thao tác **DoSearch**.|  

<a name="Close"></a>   
### <a name="close"></a>Đóng  
 Đóng kiểm soát tổ chức. Unlike the [CloseActive](#CloseActive) action, if this tab is displaying more than one page, it will close all the pages displayed in the tab in your agent application.  

<a name="CloseActive"></a>   
### <a name="closeactive"></a>CloseActive  
 Đóng kiểm soát tổ chức hoạt động trên bảng điều khiển đã chỉ định.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||Dòng đầu tiên trong cuộc gọi hành động nên chứa tên của bảng điều khiển để xác định vị trí của ứng dụng hiện hoạt. Nếu không có tham số được xác định, MainPanel được giả định.|  

### <a name="copytoclipboard"></a>CopyToClipboard  
 Sao chép hoặc gắn thêm URL bài viết vào Clipboard.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|dữ liệu|Dữ liệu bạn muốn sao chép. Bạn cũng có thể sử dụng tham số thay thế. Ví dụ:  `data=[[$context.title]]`|  
|thêm|Chỉ ra có nên thêm dữ liệu vào Clipboard không. Đặt `true` hoặc `false`. Ví dụ: `append=false`.|  

<a name="CopyToContext"></a>   
### <a name="copytocontext"></a>CopyToContext  
 Sao chép giá trị hoặc chuỗi giá trị vào biến thể ngữ cảnh. Biến thể ngữ cảnh có thể được xuất bản với phiên. Hành động này có một loạt các tên = cặp giá trị. Tên là tên của biến thể ngữ cảnh.  

### <a name="copylogicalentitytocontext"></a>CopyLogicalEntityToContext  
 Sao chép các giá trị từ toàn bộ lựa chọn của tham số dữ liệu vào ngữ cảnh.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|Tên logic|Loại hoặc phần tham số dữ liệu để sao chép giá trị từ đó.|  

<a name="CloseActivity"></a>   
### <a name="closeactivity"></a>Đóng hoạt động  
 Closes an activity record in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|ID|GUID của hồ sơ hoạt động để đóng.|  
|LogicalName|Tên logic của hoạt động để đóng.|  
|Mã trạng thái|Tên hiển thị của mã trạng thái cuối cùng sau khi hoạt động bị đóng.|  
|Mã trạng thái|Tên hiển thị của mã trạng thái cuối cùng sau khi hoạt động bị đóng.|  

 Ví dụ, để đóng một hoạt động cuộc gọi điện thoại, bạn phải chỉ định như sau:  

```  
Id=<GUID of the phone activity record>  

LogicalName=phonecall  

statuscode=Received  

statecode=Completed  
```  

 After the activity record is closed, the [$Return](../unified-service-desk/replacement-parameters.md#Return) system replacement parameter will be populated with a Boolean value indicating whether the action was successful.  

<a name="CreateEntity"></a>   
### <a name="createentity"></a>Tạo thực thể  
 Creates a new record in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`LogicalName`|The logical name of the entity to create the record.| 
|`RunAsync`|Set this to **True** to create the entity record asynchronously so that Unified Service Desk is not blocked and remains responsive during the action execution.<br/><br/>**Lưu ý**: Các cuộc gọi hành động phụ liên kết và các cuộc gọi hành động tiếp theo đối với hành động **CreateEntity** không đợi cho đến khi hoạt động tạo không đồng thời hoàn tất. Vì vậy, bạn phải đảm bảo rằng nếu bạn đang chạy hành động **CreateEntity** không đồng thời, các cuộc gọi hành động phụ phụ thuộc vào bản ghi đã tạo phải được đặt cấu hình để thực thi chỉ khi bản ghi đích đã hoàn tất. Bạn có thể thực hiện điều này bằng cách dùng hành động **ExecuteOnDataAvailable** trên kiểm soát tổ chức của Trình quản lý chung.| 

 Mỗi dòng tiếp theo trong danh sách tham số có chứa một loạt các tên = giá trị cặp sẽ xác định các trường khác của bạn để cư trú khi tạo.  

 Tài liệu tham khảo thực thể có thể được mô tả như sau:  

```  
Param=EntityReference(“logicalname”, “id”)  
```  

 OptionSetValues can be specified like the following:  

```  
Param=OptionSetValue(value)  
```  

 Booleans can be described like the following:  

```  
Param=Boolean(value)  
```  

 PartyList (được sử dụng với email) có thể được mô tả như sau:  

```  
Param=PartyList(email[“test@test.com”], er[“contact”, guid])  
```  

 You can use any number of `email` and `er` entries to represent email addresses and entity references respectively.  

 Các giá trị khác chẳng hạn như giá trị chuỗi có thể được xác định như sau:  

```  
Param=value  
```  

 Khi hồ sơ được tạo ra, giá trị $Return sẽ được chỉ định với các GUID của hồ sơ mới được tạo ra.  

<a name="CreateSession"></a>   
### <a name="createsession"></a>Tạo phiên  
 Tạo phiên.  

<a name="DeleteEntity"></a>   
### <a name="deleteentity"></a>Xóa Thực thể  
 Deletes a record in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|ID|ID của giá trị sẽ xóa. Id này phải là GUID của hồ sơ để xóa.|  
|Tên logic|Tên logic của thực thể để xóa.|  

<a name="route"></a>   
### <a name="doroute"></a>DoRoute  
 Có thể được sử dụng để kiểm tra quy tắc chuyển hướng cửa sổ bằng cách mô phỏng một cửa sổ bật lên từ kiểm soát tổ chức cụ thể. Thao tác này có thể được sử dụng trong sản xuất để kích hoạt các nguyên tắc điều hướng cửa sổ theo cách thủ công theo yêu cầu.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|The ID of the entity that is the target of the queueItem|  
|thực thể|Tên Logic của thực thể được mở trong cửa sổ bật lên.|  
|id|ID của thực thể sẽ được mở trong cửa sổ bật lên.|  
|nền tảng|Nền tảng mà hoạt động bật lên có thể xảy ra.|  

<a name="DoSearch"></a>   
### <a name="dosearch"></a>DoSearch  
 Calls the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps web services using the FetchXML defined as an entity search in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] For more information about defining an entity search, see [Search data using entity searches in Unified Service Desk](../unified-service-desk/search-data-entity-searches.md).  

|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên của tìm kiếm thực thể sẽ được sử dụng để tìm kiếm hồ sơ.|  
|chung|`True`nếu bạn muốn kết quả tìm kiếm gắn với phiên làm việc chung được xoá. Bạn phải cẩn thận trong khi lưu trữ kết quả tìm kiếm trong phiên chung vì những kết quả này không được hệ thống xóa tự động. Trong trường hợp này, bạn phải gọi thao tác **ClearEntityList** trước khi gọi thao tác này.|  
|maxcount|Số lượng tối đa các hồ sơ để lưu trữ trong các kết quả EntityList từ cuộc gọi này.|  

> [!NOTE]
>  By default, the page count (number of records per page) for a   result set is set to 50. This implies that if there are more than 50 records returned, it will be displayed in pages. If you want to specify a different page count value for the `DoSearch` action, specify the new value in the **EntitySearchPageCount** option. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Manage Options for Unified Service Desk](admin/manage-options-unified-service-desk.md)  
> 
>  When you call the `DoSearch` action, the **$Return** replacement parameter displays the number of records found and stored in EntityList as a result of this search. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [$Return](../unified-service-desk/replacement-parameters.md#Return).  

<a name="DisplayMessage"></a>   
### <a name="displaymessage"></a>DisplayMessage  
 Hiển thị hộp thư cho người dùng.  


| Tham số |                                                                             Mô tả                                                                             |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   văn bản    |      Đây là văn bản được hiển thị trong hộp thư. Nếu tham số này không xác định, bất kỳ văn bản còn lại nào (tham số còn lại) hoặc chuỗi rỗng sẽ được sử dụng.      |
|  chú thích  | Đây là chú thích được hiển thị trong hộp thư. If no caption is specified, **[!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps Message** will be used. |

### <a name="executeondataavailable"></a>ExecuteOnDataAvailable  
 Delays the execution of the sub-actions until a specified set of replacement parameters becomes available. A time-out value may be specified to limit the amount of time to wait for the replacement parameters to become available. If no time-out is specified, it will wait indefinitely or until the session ends. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Blog: How to use the special actions, ExecuteOnTimeout, ExecuteOnDataAvailable, ExecuteOnExpressionTrue](http://blogs.msdn.com/b/usd/archive/2015/09/25/how-to-use-the-special-actions-executeontimeout-executeondataavailable-executeonexpressiontrue.aspx)  

|Tham số|Mô tả|  
|---------------|-----------------|  
|mili giây|The time, in milliseconds, to indicate the amount of time to wait before this action expires, and is canceled. The remaining parameters should contain replacement parameters that need to exist before sub-actions can execute.<br /><br /> Data Parameter Example:<br /><br /> milliseconds=5000<br />[[account.Id]] <br />[[incident.Id]]|  

> [!IMPORTANT]
>  This action applies to all the hosted control types. This action isn’t exposed by default when you create an instance of a hosted control type. To use the `ExecuteOnDataAvailable` action with an instance of a hosted control type, you must explicitly add a UII action called `ExecuteOnDataAvailable` to the respective hosted control instance. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Add a UII action to a hosted control](../unified-service-desk/add-uii-action-hosted-control.md)  

### <a name="executeontimeout"></a>ExecuteOnTimeout  
 Delays the execution of the sub-actions until a specified time elapses. A time-out value is required to indicate when the sub-actions should be run. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Blog: How to use the special actions, ExecuteOnTimeout, ExecuteOnDataAvailable, ExecuteOnExpressionTrue](http://blogs.msdn.com/b/usd/archive/2015/09/25/how-to-use-the-special-actions-executeontimeout-executeondataavailable-executeonexpressiontrue.aspx)  

|Tham số|Mô tả|  
|---------------|-----------------|  
|mili giây|The time, in milliseconds, to indicate the amount of time to wait before the sub-actions execute.<br /><br /> Data Parameter Example:<br /><br /> milliseconds=5000|  

> [!IMPORTANT]
>  This action applies to all the hosted control types. This action isn’t exposed by default when you create an instance of a hosted control type. To use the `ExecuteOnTimeout` action with an instance of a hosted control type, you must explicitly add a UII action called `ExecuteOnTimeout` to the respective hosted control instance. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Add a UII action to a hosted control](../unified-service-desk/add-uii-action-hosted-control.md)  

### <a name="executeonexpressiontrue"></a>ExecuteOnExpressionTrue  
 Delays the execution of the sub-actions until a specified [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] expression returns `true`. A time-out value may be specified to limit the amount of time to wait before expiring. If no time-out is specified, it will wait indefinitely or until the session ends. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Blog: How to use the special actions, ExecuteOnTimeout, ExecuteOnDataAvailable, ExecuteOnExpressionTrue](http://blogs.msdn.com/b/usd/archive/2015/09/25/how-to-use-the-special-actions-executeontimeout-executeondataavailable-executeonexpressiontrue.aspx)  


|  Tham số   |                                                                                                                                                                                                                             Mô tả                                                                                                                                                                                                                             |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mili giây | The time, in milliseconds, to indicate the amount of time to wait before this action expires and is canceled. The remaining parameter is a [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] expression to evaluate. When this expression is `true`, sub-actions will execute.<br /><br /> Data Parameter Example:<br /><br /> milliseconds=5000<br />function IsAccountLoaded()<br />{<br /> return “[[account.Id]$+]” != “”;<br />}<br />IsAccountLoaded(); |

> [!IMPORTANT]
>  This action applies to all the hosted control types. This action isn’t exposed by default when you create an instance of a hosted control type. To use the `ExecuteOnExpressionTrue` action with an instance of a hosted control type, you must explicitly add a UII action called `ExecuteOnExpressionTrue` to the respective hosted control instance. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Add a UII action to a hosted control](../unified-service-desk/add-uii-action-hosted-control.md)  

<a name="ExecuteScriptlet"></a>   
### <a name="executescriptlet"></a>Thực hiện Scriptlet  
 Thực hiện scriptlet được chỉ định.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||Chỉ định tên của scriptlet để thực hiện trong trường **dữ liệu**.|  

### <a name="fireevent"></a>FireEvent  
 Fires a user-defined event from this hosted control.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên của sự kiện do người dùng xác định.|  

 Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này. For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).  

<a name="GetTemplate"></a>   
### <a name="gettemplate"></a>Tải mẫu  
 Truy xuất nội dung của mẫu email đã trộn.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên của mẫu để truy xuất.|  
|id|ID của thực thể để liên kết với mẫu này cho thao tác hợp nhất.|  

<a name="InvokeCTI"></a>   
### <a name="invokecti"></a>InvokeCTI  
 Mô phỏng sự kiện CTI  

|Tham số|Mô tả|  
|---------------|-----------------|  
|loại|This is the type of CTI event, such as phone call or chat.|  
|appname|The desktop manager name to be used for this pop-up simulation.|  
|ani|Nhận dạng số tự động (ANI) hoặc số điện thoại của người gọi.|  
|dnis|Số được quay hoặc DNIS.|  
||Tất cả các tham số còn lại sẽ được thông qua dưới dạng tham số cho bộ xử lý sự kiện CTI.|  

### <a name="launchurl"></a>LaunchURL  
 Launches a URL in [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] outside of the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application. You must specify the URL as a parameter in the **Data** field.  

<a name="LookUpQueueItem"></a>   
### <a name="lookupqueueitem"></a>LookupQueueItem  
 Looks up a queueitem in the system and obtain the information.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|ID|The ID of the entity that is the target of the queueItem|  
|EntityType|Loại hoặc tên logic của thực thể tham chiếu đến trong trường Id.|  

 Các chi tiết queueitem kết quả sẽ được đặt vào các tham số thay thế queueitem và có thể được tham chiếu sau đó.  

<a name="MoveApplicationToPanel"></a>   
### <a name="moveapplicationtopanel"></a>Di chuyển ứng dụng đến bảng điều khiển  
 Di chuyển kiểm soát tổ chức tới bảng điều khiển được chỉ định trong ứng dụng khách.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|ứng dụng|Tên của kiểm soát tổ chức để di chuyển.|  
|bảng điều khiển|Tên của bảng điều khiển mục tiêu.|  

<a name="MoveToPanel"></a>   
### <a name="movetopanel"></a>MoveToPanel  
 Di chuyển kiểm soát tổ chức giữa các bảng điều khiển tại thời gian chạy.  

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
|ID|ID của hồ sơ thực thể để mở.|  

<a name="Pause"></a>   
### <a name="pause"></a>Tạm dừng  
 Dừng thực thi hành động mà không chặn quá trình xử lý thư. Hành động này khác với việc tạm dừng các chuỗi chủ đề hiện tại trong khoảng thời gian đã chỉ định ([Thread.Sleep](https://msdn.microsoft.com/library/d00bd51t.aspx)) vì hành động này cho phép tiếp tục quá trình xử lý. Hành động này hữu ích khi bạn chờ thao tác web hoàn thành.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|mili giây|Số mili giây để tạm dừng.|  

<a name="popup"></a>   
### <a name="popup"></a>Cửa sổ bật lên  
 Bật lên URL từ kiểm soát tổ chức và chạy nguyên tắc điều hướng cửa sổ chống lại hình thức kiểm soát tổ chức để định tuyến bật lên đến vị trí thích hợp.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|url|Routes a popup from this hosted control using this URL as if it were a popup requested from the displayed control.|  
|nền tảng|The frame from which this popup originated.|  

### <a name="realignwindow"></a>RealignWindow  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]

<a name="ReadSettings"></a>   
### <a name="readsettings"></a>ReadSettings  
 Reads the previously saved settings from the [$Settings](../unified-service-desk/replacement-parameters.md#Settings) replacement parameter.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|readfromcache|`True` if you want to read the local cached version of these settings. `False` or missing otherwise.|  

<a name="RedoScreenPop"></a>   
### <a name="redoscreenpop"></a>RedoScreenPop  
 Bật lại màn hình cuối cùng. This can be useful in cases where the session limit was reached and the pop up wasn’t successful, or you closed the session but more work is required. Hành động này không yêu cầu tham số.  

<a name="ResetLocalCache"></a>   
### <a name="resetlocalcache"></a>Đặt lại bộ nhớ đệm cục bộ  
 Đặt lại bộ nhớ đệm cấu hình trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Lần tiếp theo [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] được bắt đầu, nó sẽ tải về cấu hình từ máy chủ. Người dùng phải có quyền truy cập ghi vào thực thể msdyusd_usersettings để thực hiện hành động này.  

<a name="RouteToQueue"></a>   
### <a name="routetoqueue"></a>RouteToQueue  
 Routes an entity to a queue in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|điểm đến|ID hàng đợi mục tiêu. Đây là tham số destinationqueuename độc quyền lẫn nhau|  
|destinationqueuename|Đây là tên của hàng đợi để định tuyến thực thể.|  
|entitytype|Đây là tên logic của thực thể được định tuyến.|  
|entityid|Đây là GUID/Id của thực thể được đặt vào hàng đợi.|  

<a name="SaveAll"></a>   
### <a name="saveall"></a>Lưu tất cả  
 Lưu tất cả biểu mẫu trong kiểm soát tổ chức cho phép hiển thị nhiều trang (**Cho phép Nhiều Trang** = Có). If the hosted control allows only a single page to be displayed (**Allow Multiple Pages** = No), this is equivalent to the **Save** action.  

<a name="SaveSetting"></a>   
### <a name="savesetting"></a>SaveSetting  
 Lưu một thiết đặt cụ thể cho người dùng.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên cài đặt. This will show up in the[$Settings](../unified-service-desk/replacement-parameters.md#Settings) replacement parameter.|  
|giá trị|Giá trị của cài đặt để lưu.|  

<a name="SetTheme"></a>   
### <a name="settheme"></a>SetTheme  
 Applies a theme to modify the layout or look and feel of components of the user interface. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Use themes to customize the appearance of your application](../unified-service-desk/customize-appearance-application.md)  

|Tham số|Mô tả|  
|---------------|-----------------|  
|xóa|`True`nếu bạn muốn xóa hoàn toàn chủ đề hiện tại trước khi áp dụng chủ đề đã chỉ định. If this parameter is false, or not specified, the new theme information will be merged with the current theme.|  
||Tham số còn lại (tham số còn lại sau khi các tham số khác đã xóa) nên chứa tên của chủ đề được sử dụng. Tham số này nên là tên tài nguyên web (được đổi tên thành XML và được tải lên dưới dạng tài nguyên web) tệp XAML, URL từ một máy chủ truy cập ẩn danh hoặc XAML thô đại diện cho các chủ đề.|  

<a name="SetAppBar"></a>   
### <a name="setappbar"></a>Đặt thanh ứng dụng  
 Đặt kiểm soát tổ chức tới cạnh được xác định của cửa sổ chính của ứng dụng khách.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|Tên ứng dụng|Tên của kiểm soát tổ chức để gắn. Nếu tham số này được chỉ định, cửa sổ chính lưu trữ kiểm soát tổ chức này sẽ được chỉ định.|  
|chiều rộng|Chiều rộng bằng pixel của cửa sổ được chỉ định. Nếu điều này không được chỉ định, chiều rộng hiện tại của cửa sổ sẽ được sử dụng.|  
|chiều cao|Chiều cao bằng pixel của cửa sổ được chỉ định. Nếu điều này không được chỉ định, chiều cao hiện tại của cửa sổ sẽ được sử dụng.|  
|Cạnh|Các cạnh để gắn lại. Nếu không chỉ định giá trị nào, **Giá trị hàng đầu** được giả định. Chỉ định một trong các giá trị sau: **Giá trị hàng đầu**, **Giá trị dưới cùng**, **Bên trái**, hoặc **Bên phải**.|  

<a name="StartEventTimer"></a>   
### <a name="seteventtimer"></a>Đặt bộ hẹn giờ sự kiện  
 Thiết lập bộ đếm thời gian sự kiện để bắt đầu.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên của bộ hẹn giờ sự kiện.|  

<a name="SetSize"></a>   
### <a name="setsize"></a>SetSize  
 Thiết lập chiều rộng và chiều cao của kiểm soát tổ chức. Quá trình này đặc biệt hữu ích khi sử dụng tính năng "tự động" trong bố cục bảng điều khiển của bạn.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|chiều rộng|The width of the hosted control.|  
|chiều cao|The height of the hosted control.|  

<a name="SetWindowProperty"></a>   
### <a name="setwindowproperty"></a>Đặt thuộc tính cửa sổ  
 Đặt trạng thái cửa sổ cho cửa sổ chính của ứng dụng khách.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|Trạng thái cửa sổ|Một trong các giá trị sau: **được tối đa**, **được tối thiểu**, hoặc **bình thường**.|  

### <a name="shellexecute"></a>ShellExecute  
 Hành động này được thiết kế để khởi chạy URL hoặc dòng lệnh. Note that the user must have rights to execute the application.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||Tham số duy nhất là dòng lệnh hoặc URL của ứng dụng được thực hiện.|  

<a name="ShowAbout"></a>   
### <a name="showabout"></a>Hiển thị Giới thiệu  
 Displays the about dialog box for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] that contains information such as the name of the current user, the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server and organization that the user is connected to, version number of the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and the support site URL.  

<a name="ShowTab"></a>   
### <a name="showtab"></a>Hiển thị tab  
 Đặt trọng tâm vào tab (kiểm soát tổ chức) trong ứng dụng tổng đài viên của bạn.  

|Tham số|Mô tả|  
|---------------|-----------------|  
||Dòng đầu tiên trong cuộc gọi hành động nên chứa tên của kiểm soát tổ chức để hiển thị sau. Don’t use the display name of the hosted control. For more information about using this action call, see step 4 of [Walkthrough 2: Display an external webpage in your agent application](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md).|  

<a name="StopEventTimer"></a>   
### <a name="stopeventtimer"></a>Dừng bộ hẹn giờ sự kiện  
 Dừng bộ đếm thời gian sự kiện.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên của bộ hẹn giờ sự kiện phải dừng.|  

<a name="Translate"></a>   
### <a name="translate"></a>Dịch  
 Cho phép bạn thực hiện dịch ngôn ngữ sử dụng [Trình biên dịch của Microsoft](https://datamarket.azure.com/dataset/bing/microsofttranslator).  


|  Tham số   |                                                                                                                                                                                                                                               Mô tả                                                                                                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    giá trị     | Đây là văn bản để dịch. Giá trị này có thể được thu nhỏ cho hỗ trợ nhiều dòng.<br /><br /> Một số ví dụ hợp lệ:<br /><br /> `value=$Escaped("my string<br>new line\\\"my text\\\"")`<br /><br /> `value=[[myapp.myparam]^]`<br /><br /> `value=$Escaped([[myapp.myparam]$])`<br /><br /> For more information about these replacement keys, see [Use replacement parameters to configure Unified Service Desk](../unified-service-desk/use-replacement-parameters-configure-unified-service-desk.md). |
| từ ngôn ngữ |                                                                                                      Tên của ngôn ngữ được dịch từ. Nếu trống, hệ thống sẽ cố gắng phát hiện ngôn ngữ của giá trị được xác định cần dịch trước khi dịch. For a list of valid language values, see [Translator Language Codes](https://msdn.microsoft.com/library/hh456380.aspx).                                                                                                       |
|  sang ngôn ngữ  |                                                                                                                                                                      Tên của ngôn ngữ được dịch sang. For a list of valid language values, see [Translator Language Codes](https://msdn.microsoft.com/library/hh456380.aspx).                                                                                                                                                                      |
|   id máy khách   |                                                                                                       ID máy khách thu được từ [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] cho dịch vụ dịch thuật. For information about registering with [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)], see [https://datamarket.azure.com](https://datamarket.azure.com).                                                                                                       |
| bí mật của khách hàng |                                                                                                     Bí mật của khách hàng thu được từ [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] cho dịch vụ dịch thuật. For information about registering with [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)], see [https://datamarket.azure.com](https://datamarket.azure.com).                                                                                                     |

 The translated value is displayed under the [$Return](../unified-service-desk/replacement-parameters.md#Return) replacement parameter.  

<a name="UpdateEntity"></a>   
### <a name="updateentity"></a>Cập nhật thực thể  
 Updates a record in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|ID|ID của giá trị để cập nhật. Id này phải là GUID của hồ sơ để cập nhật.|  
|LogicalName|Tên logic của thực thể để cập nhật.|  

 Mỗi dòng tiếp theo trong danh sách tham số có chứa một loạt các tên = giá trị cặp sẽ xác định các trường khác của bạn để cư trú khi cập nhật.  

 Tài liệu tham khảo thực thể có thể được mô tả như sau:  

```  
Param=EntityReference(“logicalname”, “id”)  
```  

 OptionSetValue có thể được xác định như sau:  

```  
Param=OptionSetValue(value)  
```  

 Luận lý có thể được mô tả như sau:  

```  
Param=Boolean(value)  
```  

 PartyList (được sử dụng với email) có thể được mô tả như sau:  

```  
Param=PartyList(email[“test@test.com”], er[“contact”, guid])  
```  

 Bạn có thể sử dụng bất kỳ số nào của email và mục er để đại diện cho địa chỉ email và tham chiếu thực thể tương ứng.  

 Các giá trị khác chẳng hạn như giá trị chuỗi có thể được xác định như sau:  

```  
Param=value  
```  

<a name="WorkOn"></a>   
### <a name="workon"></a>Việc cần  
 Hành động này là tương đương để chọn một mục hàng đợi từ một hàng đợi và nhấp vào nút WorkOn trên ruy băng. Hành động này đánh dấu mục hàng đợi như đang được làm việc bởi một tổng đài viên cụ thể.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|ID|This is the Id of the queueitem. See [LookupQueueItem](../unified-service-desk/global-manager-hosted-control.md#LookUpQueueItem) for information on how to obtain the ID for a target entity.|  
|Hành động|Optional parameter allowing the administrator to specify that they wish to remove the `WorkOn` attribute to return it to the queue.<br /><br /> Giá trị hợp lệ:<br /><br /> Xóa-Xóa thuộc tính WorkOn và trả mục về hàng đợi để người khác làm việc.|  

<a name="events"></a>   
## <a name="predefined-events"></a>Sự kiện được xác định trước  
 Dưới đây là các sự kiện được xác định trước được liên kết với kiểm soát tổ chức này.  

### <a name="desktopready"></a>DesktopReady  
 Occurs on startup when all the desktop initialization has completed and the connections to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps have been established. Sự kiện này sẽ chỉ được bắt đầu một lần và việc sử dụng sự kiện này để đặt chủ đề và thực hiện các thao tác khởi động khác là thao tác phổ biến.  

### <a name="sessionactivated"></a>Phiên đã kích hoạt  
 Xảy ra bất cứ khi nào một phiên được kích hoạt.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|Id phiên|ID của phiên đang hiện hoạt.|  
|IsGlobal|Cho biết liệu sự kiện này có được áp dụng cho phiên chung không. Trả về Đúng hoặc Sai.|  
|Kích hoạt|Thao tác này được đặt thành Đúng.|  

### <a name="sessionclosed"></a>Đã đóng phiên  
 Xảy ra khi một phiên đã bị đóng.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|Id phiên|ID của phiên đã bị đóng.|  
|IsGlobal|Cho biết liệu sự kiện này có được áp dụng cho phiên chung không. Trả về Đúng hoặc Sai.|  

### <a name="sessiondeactivated"></a>Phiên đã hủy kích hoạt  
 Xảy ra khi một phiên đã bị hủy kích hoạt.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|Id phiên|ID của phiên không hoạt động.|  
|IsGlobal|Cho biết liệu sự kiện này có được áp dụng cho phiên chung không. Trả về Đúng hoặc Sai.|  
|Kích hoạt|Thao tác này được đặt thành Sai.|  

<a name="sessionnew"></a>   
### <a name="sessionnew"></a>Phiên mới  
 Xảy ra khi một phiên mới đã được tạo.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|Id phiên|ID của phiên mới được tạo.|  
|IsGlobal|Trả về Đúng nếu phiên mới là phiên chung. Nếu không, trả về Sai.|  

### <a name="see-also"></a>Xem thêm  
 [Hành động UII](../unified-service-desk/uii-actions.md)   
 [Sự kiện](../unified-service-desk/events.md)   
 [View predefined actions and events for a hosted control](../unified-service-desk/view-predefined-actions-events-hosted-control.md)   
 [Xem trợ giúp được nhúng cho hành động và sự kiện](../unified-service-desk/view-embedded-help-for-actions-and-events.md)   
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)   
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)  

