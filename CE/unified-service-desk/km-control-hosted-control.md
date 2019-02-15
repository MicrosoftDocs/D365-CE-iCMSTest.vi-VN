---
title: KM Control (Hosted Control) in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn using the KM Control type of hosted control to display knowledge base articles in Dynamics 365 for Customer Engagement apps in your agent application.
ms.custom:
- dyn365-USD
ms.date: 08/17/2018
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
ms.assetid: 8c4b9dd8-d37c-4256-b6c1-f2e42105c52b
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: b16e1cf851b9d9eea899218d8d1a92b37a6584c4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386953"
---
# <a name="km-control-hosted-control"></a>KM Control (Hosted Control)
Use the **KM Control** type of hosted control to display knowledge base articles in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps in your agent application. Using the new hosted control, your service agents can search for articles, associate or disassociate an article with a case, copy a link to an article, and send it through email or in chat without having to switch applications. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Use Dynamics 365 for Customer Engagement apps knowledge base for effective customer engagement](../unified-service-desk/use-dynamics-365-knowledge-effective-customer-engagement.md) and [Configure Unified Service Desk to use Dynamics 365 for Customer Engagement apps knowledge](../unified-service-desk/configure-unified-service-desk-use-dynamics-365-knowledge.md)

<a name="Create"></a>   
## <a name="create-a-km-control-hosted-control"></a>Create a KM Control hosted control  
 While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create. Phần này cung cấp thông tin về các trường cụ thể là duy nhất đối với loại kiểm soát tổ chức **Kiểm soát KM**. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

 ![KM Control hosted control](../unified-service-desk/media/usd-kmcontrolhostedcontrol.png "KM Control hosted control")  

 In the **New Hosted Control** screen:  

- Trong khu vực **Unified Service Desk**, chọn **Kiểm soát KM** từ danh sách thả xuống **Loại Thành phần USD**.  

- Danh sách thả xuống **Cho phép Nhiều Trang** không được hỗ trợ cho loại kiểm soát tổ chức này.  

- The **Hosting Type** drop-down list specifies how you want this control to be hosted. You can **IE Process** (default) or **Internal WPF**. For more information, see [Select a hosting method for hosted controls](../unified-service-desk/select-hosting-method-controls.md).  

- Under the **Common Properties** area, select the **Application is Global** check box to set the hosted control as global. Kiểm soát tổ chức chung có thể được hiển thị bên ngoài phiên khách hàng. Kiểm soát giống như bảng thông tin của tổng đài viên, tường hoặc tìm kiếm là những hình thức sử dụng chung cho kiểm soát tổ chức chung. Kiểm soát tổ chức chung không có trạng thái phiên dành riêng cho phiên để khi bạn thay đổi phiên, các kiểm soát tổ chức chung tương tự vẫn được duy trì. Nếu hộp kiểm không được chọn, kiểm soát tổ chức trở thành kiểu dựa trên phiên. Kiểm soát dựa trên phiên tồn tại trong ngữ cảnh của phiên khách hàng. Nếu người dùng thay đổi sang một phiên khác, tất cả các trang phiên từ phiên trước đó được ẩn.  

- Trường **Hiển thị nhóm** hiển thị bảng điều khiển nơi hiển thị kiểm soát tổ chức này. In the knowledge management package, the KM Control is displayed in the **RightPanel**; however, you can choose to display it in the **LeftPanel** or **MainPanel** as per your requirement. For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md).  

  For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

<a name="actions"></a>   
## <a name="predefined-uii-actions"></a>Predefined UII actions  
 These are the predefined actions for this hosted control type.  

<a name="Associate"></a>   
### <a name="associate"></a>Liên kết  
 Associates a knowledge base record in Dynamics 365 for Customer Engagement apps or [!INCLUDE[pn_parature](../includes/pn-parature.md)] with the parent entity record in **KM Control**.  


|     Tham số     |                                                                                                                                                                                                                                                                Mô tả                                                                                                                                                                                                                                                                 |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  entitytypename   |                                                                                                                                                                                                          Tên logic của thực thể cha mẹ để liên kết bản ghi trong cơ sở kiến thức. Ví dụ: `entitytypename=incident`                                                                                                                                                                                                           |
|     recordid      |                                                                                                                                                                                                                               The ID of the parent entity record to associate the knowledge base record to.                                                                                                                                                                                                                                |
|  articleuniqueid  |                                                                                                                                                                                                              The unique ID of the article in that you want to associate. Ví dụ: `articleuniqueid=7924/8112/Article/41`                                                                                                                                                                                                               |
|   articletitle    |                                                                                                                                                                                                A string value representing article's title that you want to associate. Ví dụ: `articletitle=Diffused Sunlight and Weather Conditions`                                                                                                                                                                                                |
| articleprivateurl |                                                                                                      The private URL of the article in Parature that you want to associate. For example: `articleprivateurl=https://demo.parature.com/ics/km/kmRefEdit.asp?questionID=41` **Note:**  This parameter is not applicable if you are using the native Dynamics 365 for Customer Engagement apps knowledge base; it’s only applicable for the Parature knowledge base.                                                                                                       |
| articlepublicurl  | The public URL of the article that you want to associate. If you are using native [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps knowledge base, the articles should have already been published to an external portal (select **Use an external portal** in the **Knowledge Base management Settings** dialog box in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps) so that you can use the article URL in this parameter.<br /><br /> Ví dụ: `articlepublicurl=http://support.microsoft.com/kb/{kbnum}` |

<a name="Close"></a>   
### <a name="close"></a>Đóng  
 Đóng kiểm soát tổ chức **Kiểm soát KM**.  

<a name="Disassociate"></a>   
### <a name="disassociate"></a>Dừng liên kết  
 Hủy liên kết bản ghi trong cơ sở kiến thức, đã được liên kết với hồ sơ thực thể cha mẹ trong **Kiểm soát KM**.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`articleuniqueid`|The unique ID of the article that you want to disassociate. Ví dụ: `articleuniqueid=7924/8112/Article/41`|  
|`relatedentityrecordid`|The ID of the parent entity record with which the knowledge base record is associated.|  
|`entityname`|The logical name of the parent entity to which the knowledge base record is associated. Ví dụ: `entitytypename=incident`|  

### <a name="fireevent"></a>FireEvent  
 Khuyến khích sự kiện do người dùng xác định từ kiểm soát tổ chức **Kiểm soát KM**.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`name`|Tên của sự kiện do người dùng xác định.|  

 Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này. For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).  

<a name="MoveToPanel"></a>   
### <a name="movetopanel"></a>MoveToPanel  
 Moves the hosted control to the specified panel in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] at runtime.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`app`|Name of the hosted control to be moved.|  
|`panel`|Name of the target panel to move the hosted control to.|  

### <a name="popup"></a>Cửa sổ bật lên  
 Pops up a URL from the hosted control, and runs the window navigation rules against it for routing the popup to the appropriate location.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`url`|Routes a popup from the hosted control using this URL as if it were a popup requested form the displayed control.|  
|`frame`|The frame from which the popup originated.|  

<a name="RealignWindow"></a>   
### <a name="realignwindow"></a>RealignWindow  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]

<a name="Search"></a>   
### <a name="search"></a>Search  
 Tìm kiếm bản ghi trong **Kiểm soát KM** bằng cách đi qua chuỗi tìm kiếm dưới dạng tham số.  


| Tham số  |                                                                                                                                                                                                                                                               Mô tả                                                                                                                                                                                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   truy vấn    |                                                                                                                 A string value to be searched in the hosted control. For example: `query=contoso`. This will fetch all the knowledge articles from [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps or [!INCLUDE[pn_parature](../includes/pn-parature.md)] that have names starting with the word "contoso".                                                                                                                 |
|  kết quả   |                                                                                     An integer value to indicate the number of search results to be displayed in the hosted control. Ví dụ: chỉ định `results=5` sẽ hiển thị 5 kết quả tìm kiếm trong kiểm soát được tổ chức. Nếu không có giá trị nào hoặc một giá trị sai được cung cấp cho tham số dữ liệu này thì giá trị mặc định (10) sẽ được sử dụng. Giá trị tối đa được phép cho tham số dữ liệu này là 20.                                                                                      |
|   bộ lọc   |                         Một giá trị số nguyên sẽ chỉ ra loại bài viết trong cơ sở kiến thức được hiển thị trong kiểm soát tổ chức:<br /><br /> -   `1`: Tất cả (Mặc định)<br />-   `2`: Tất cả Bản nháp<br />-   `3`: Tất cả Đã xuất bản<br />-   `4`: Đã xuất bản-Riêng tư<br />-   `5`: Đã xuất bản-Công khai<br />-   `6`: Đã xuất bản-Hết hạn<br /><br /> Ví dụ: chỉ định `filter=3` để chỉ hiển thị các bài viết trong cơ sở kiến thức đã xuất bản.<br /><br /> Nếu không có giá trị nào hoặc một giá trị sai được cung cấp thì giá trị mặc định (1) sẽ được sử dụng.                         |
| blockClick | Một giá trị số nguyên để chỉ ra có nên chặn hiển thị nội dung nội tuyến khi kết quả tìm kiếm được bấm vào trong kiểm soát tổ chức không. Đặt vào trong `0` để mở nội dung nội tuyến khi bấm vào, đặt `1` để chặn mở nội dung nội tuyến. Ví dụ: `blocked=1`<br /><br /> If no value or a wrong value is provided, then the default value (0) will be used. If you have the set the value to 1 to block the content, the [ResultOpen](../unified-service-desk/km-control-hosted-control.md#ResultOpen) event will still be fired. |
|    sắp xếp    |                An integer value to indicate the sorting options for the knowledge base articles in the search result:<br /><br /> -   `1`: Mức độ liên quan (mặc định)<br />-   `2`: Xếp hạng<br />-   `3`: Số lượt xem<br />-   `4`: Ngày sửa đổi lần cuối (cũ nhất trước tiên)<br />-   `5`: Ngày sửa đổi lần cuối (mới nhất trước tiên)<br /><br /> Ví dụ: chỉ định `sort=2` để sắp xếp các bài viết dựa trên xếp hạng.<br /><br /> If no value or a wrong value is provided, then the default value (1) will be used for the data parameter.                 |

<a name="SetArticleContext"></a>   
### <a name="setarticlecontext"></a>SetArticleContext  
 Đính kèm dữ liệu bài viết hiện tại trong cơ sở kiến thức trong **Kiểm soát KM**.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`articleapplication`|Name of the hosted control where the knowledge base article will be displayed.|  
|`articledata`|An article record object value passed from the [ResultOpen](../unified-service-desk/km-control-hosted-control.md#ResultOpen) event.|  

<a name="SetSearchProps"></a>   
### <a name="setsearchprops"></a>SetSearchProps  
 Bật các loại bộ lọc khác nhau để tìm kiếm bài viết trong cơ sở kiến thức trong **Kiểm soát KM**.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`showFilter`|Cho biết có bật bộ lọc loại bài viết để tìm kiếm bài viết trong cơ sở kiến thức hay không. Đặt `0` để ẩn bộ lọc và `1` để hiển thị bộ lọc. For example: `showFilter=1`.<br /><br /> Nếu không có giá trị nào hoặc giá trị sai được cung cấp thì giá trị mặc định (0) sẽ được sử dụng.|  
|`showLang`|Cho biết có bật bộ lọc ngôn ngữ để tìm kiếm bài viết trong cơ sở kiến thức hay không. Đặt `0` để ẩn bộ lọc và `1` để hiển thị bộ lọc. For example: `showLang=1`.<br /><br /> Nếu không có giá trị nào hoặc giá trị sai được cung cấp thì giá trị mặc định (0) sẽ được sử dụng.|  
|`showDept`|Cho biết có bật bộ lọc bộ phận để tìm kiếm bài viết trong cơ sở kiến thức hay không. Đặt `0` để ẩn bộ lọc và `1` để hiển thị bộ lọc. Ví dụ: `showDept=1`.<br /><br /> If no value or a wrong value is provided, default value (0) will be used.|  

<a name="SetSize"></a>   
### <a name="setsize"></a>SetSize  
 Thiết lập chiều cao và chiều rộng của kiểm soát tổ chức. Quá trình này đặc biệt hữu ích khi sử dụng tính năng "tự động" trong bố cục bảng điều khiển của bạn.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`width`|Chiều rộng của kiểm soát tổ chức.|  
|`height`|Chiều cao của kiểm soát tổ chức.|  

### <a name="setusercanclose"></a>SetUserCanClose  
 Cho phép người dùng đóng kiểm soát tổ chức bằng cách bấm vào biểu tượng X ở góc trên cùng bên phải của tab kiểm soát tổ chức.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`UserCanClose`|Đặt điều này thành `true` để cho phép người dùng đóng kiểm soát tổ chức. Nếu không, đặt `false`.|  

<a name="events"></a>   
## <a name="predefined-events"></a>Sự kiện được xác định trước  
 Các sự kiện được xác định trước sau đây được liên kết với loại kiểm soát tổ chức này.  

### <a name="popuprouted"></a>Bật lên đã lên lịch  
 Xảy ra sau khi một cửa sổ bật lên đã được hệ thống xác định.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`url`|URL của cửa sổ bật lên đã được xác định.|  

<a name="ResultOpen"></a>   
### <a name="resultopen"></a>ResultOpen  
 Xuất hiện khi kết quả tìm kiếm được mở để đọc nội dung trong **Kiểm soát KM**.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`postdata`|The formdata object containing a set of key/value pairs representing form fields and their values for a knowledge article.|  

<a name="SearchComplete"></a>   
### <a name="searchcomplete"></a>SearchComplete  
 Occurs after the knowledge base article search is complete, and the search results have loaded in the hosted control.  

### <a name="selectionchange"></a>SelectionChange  
 Xảy ra khi kết quả được chọn trong **kiểm soát KM**.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`postdata`|The formdata object containing a set of key/value pairs representing form fields and their values for a knowledge article.|  

### <a name="see-also"></a>Xem thêm  
 [Leverage knowledge for effective customer engagement](../unified-service-desk/use-dynamics-365-knowledge-effective-customer-engagement.md)   
 [Configure Dynamics 365 for Customer Engagement apps knowledge in Unified Service Desk](../unified-service-desk/configure-unified-service-desk-use-dynamics-365-knowledge.md)   
 [Walkthrough 8: Use Dynamics 365 for Customer Engagement apps knowledge within your agent application](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md)   
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)
