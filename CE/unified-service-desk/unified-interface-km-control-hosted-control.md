---
title: Unified Interface KM Control (Hosted Control) in Unified Service Desk for Dynamics 365 for Customer Engagement apps Unified Interface App| MicrosoftDocs
description: Learn using the KM Control type of hosted control to display knowledge base articles in Dynamics 365 for Customer Engagement apps in your agent application.
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
ms.assetid: B999CDBB-3E08-4558-ACA6-5651ABE2C973
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
monikerRange: '>=dynamics-usd-4'
ms.openlocfilehash: e9dbe1245d26ef2d633643f2208c4be3eab0877b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386701"
---
# <a name="unified-interface-km-control-hosted-control"></a>Unified Interface KM Control (Hosted Control)

Use the **Unified Interface KM Control** type of hosted control to display knowledge base articles in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps in your agent application. Using the new hosted control, your service agents can search for articles, associate or disassociate an article with a case, copy a link to an article, and send it through email or in chat without having to switch applications. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Use Dynamics 365 for Customer Engagement apps knowledge base for effective customer engagement](../unified-service-desk/use-dynamics-365-knowledge-effective-customer-engagement.md) and [Configure Unified Service Desk to use Dynamics 365 for Customer Engagement apps knowledge](../unified-service-desk/configure-unified-service-desk-use-dynamics-365-knowledge.md)

> [!NOTE]
> The Unified Interface KM Control supports all searche techniques available in Dynamics 365 for Customer Engagement apps except the **Relevance Search**. More informaiton: [Relevance search for knowledge management](https://docs.microsoft.com/en-us/business-applications-release-notes/October18/service/customer-service-core-release-notes/relevance-search-for-knowledge-management)

<a name="Create"></a>   
## <a name="create-a-km-control-hosted-control"></a>Tạo kiểm soát tổ chức Kiểm soát KM  
 While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create. This section provides information about the specific fields that are unique to the **Unified Interface KM Control** hosted control type. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

 ![Unified Interface KM Control hosted control](../unified-service-desk/media/usd-unified-interface-kmcontrolhostedcontrol.png "Unified Interface KM Control hosted control")  

 In the **New Hosted Control** screen:

- Under **Unified Service Desk** area, select **Unified Interface KM Control** from the **USD Component Type** drop-down list.  

- Danh sách thả xuống **Cho phép Nhiều Trang** không được hỗ trợ cho loại kiểm soát tổ chức này.  

- The **Hosting Type** is **IE Process** (default). For more information, see [Select a hosting method for hosted controls](../unified-service-desk/select-hosting-method-controls.md).  

- Under the **Common Properties** area, select the **Application is Global** check box to set the hosted control as global. Kiểm soát tổ chức chung có thể được hiển thị bên ngoài phiên khách hàng. Kiểm soát giống như bảng thông tin của tổng đài viên, tường hoặc tìm kiếm là những hình thức sử dụng chung cho kiểm soát tổ chức chung. Kiểm soát tổ chức chung không có trạng thái phiên dành riêng cho phiên để khi bạn thay đổi phiên, các kiểm soát tổ chức chung tương tự vẫn được duy trì. Nếu hộp kiểm không được chọn, kiểm soát tổ chức trở thành kiểu dựa trên phiên. Kiểm soát dựa trên phiên tồn tại trong ngữ cảnh của phiên khách hàng. Nếu người dùng thay đổi sang một phiên khác, tất cả các trang phiên từ phiên trước đó được ẩn.  

- Trường **Hiển thị nhóm** hiển thị bảng điều khiển nơi hiển thị kiểm soát tổ chức này. In the knowledge management package, the Unified Interface KM Control is displayed in the **RighPanel**; however, you can choose to display it in the **LeftPanel** or **MainPanel** as per your requirement. For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md).  

  For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  

<a name="actions"></a>   
## <a name="predefined-uii-actions"></a>Predefined UII actions  
 These are the predefined actions for this hosted control type.  

<a name="Associate"></a>   
### <a name="associate"></a>Liên kết  
 Associates a knowledge base record in Dynamics 365 for Customer Engagement apps with the parent entity record in **Unified Interface KM Control**.  


|     Tham số     | Mô tả |
|-------------------|------------------|
|  entitytypename   | Tên logic của thực thể cha mẹ để liên kết bản ghi trong cơ sở kiến thức. Ví dụ: `entitytypename=incident`|
|     recordid      | ID của hồ sơ thực thể cha mẹ để liên kết bản ghi trong cơ sở kiến thức.|
|  articleuniqueid  | The unique ID of the article in that you want to associate. Ví dụ: `articleuniqueid=7924/8112/Article/41`|
|   articletitle    |  A string value representing article's title that you want to associate. Ví dụ: `articletitle=Diffused Sunlight and Weather Conditions` |
| articlepublicurl  | The public URL of the article that you want to associate. If you are using native [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps knowledge base, the articles should have already been published to an external portal (select **Use an external portal** in the **Knowledge Base management Settings** dialog box in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps) so that you can use the article URL in this parameter.<br /><br /> Ví dụ: `articlepublicurl=http://support.microsoft.com/kb/{kbnum}` |

<a name="Close"></a>   
### <a name="close"></a>Đóng  
 Closes the **Unified Interface KM Control** hosted control.  

<a name="Disassociate"></a>   
### <a name="disassociate"></a>Dừng liên kết  
 Disassociates a knowledge base record, which is already associated to the parent entity record in **Unified Interface KM Control**.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`articleuniqueid`|The unique ID of the article that you want to disassociate. Ví dụ: `articleuniqueid=7924/8112/Article/41`|  
|`relatedentityrecordid`|ID của hồ sơ thực thể cha mẹ mà sẽ liên kết với bản ghi trong cơ sở kiến thức.|  
|`entityname`|Tên logic của thực thể cha mẹ mà sẽ liên kết với bản ghi trong cơ sở kiến thức. Ví dụ: `entitytypename=incident`|  

### <a name="fireevent"></a>FireEvent  
 Fires a user-defined event from the **Unified Interface KM Control** hosted control.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`name`|Tên của sự kiện do người dùng xác định.|  

 Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này. For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).  

<a name="MoveToPanel"></a>   
### <a name="movetopanel"></a>MoveToPanel  
 Di chuyển kiểm soát tổ chức tới bảng điều khiển được chỉ định trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] tại thời gian chạy.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`app`|Name of the hosted control to be moved.|  
|`panel`|Tên của bảng điều khiển mục tiêu để di chuyển kiểm soát tổ chức đến.|  

### <a name="popup"></a>Cửa sổ bật lên  
 Bật lên URL từ kiểm soát tổ chức và chạy nguyên tắc điều hướng cửa sổ với hình thức kiểm soát tổ chức để định tuyến cửa sổ bật lên đến vị trí thích hợp.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`url`|Routes a popup from the hosted control using this URL as if it were a popup requested form the displayed control.|  
|`frame`|Nền tảng mà cửa sổ bật lên xuất phát.|  

<a name="RealignWindow"></a>   
### <a name="realignwindow"></a>RealignWindow  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]

<a name="Search"></a>   
### <a name="search"></a>Search  
 Searches records in the **Unified Interface KM Control** by passing search string as parameter.  


| Tham số  | Mô tả |
|------------|------------------------|
|   truy vấn    | Một giá trị chuỗi được tìm kiếm trong kiểm soát tổ chức. Ví dụ: `query=contoso`. This will fetch all the knowledge articles from [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps that have names starting with the word "contoso". |
|  kết quả   | Một giá trị số nguyên sẽ chỉ ra số lượng kết quả tìm kiếm được hiển thị trong kiểm soát tổ chức. Ví dụ: chỉ định `results=5` sẽ hiển thị 5 kết quả tìm kiếm trong kiểm soát được tổ chức. Nếu không có giá trị nào hoặc một giá trị sai được cung cấp cho tham số dữ liệu này thì giá trị mặc định (10) sẽ được sử dụng. Giá trị tối đa được phép cho tham số dữ liệu này là 20. |
|   bộ lọc   | Một giá trị số nguyên sẽ chỉ ra loại bài viết trong cơ sở kiến thức được hiển thị trong kiểm soát tổ chức:<br /><br /> -   `0`: Draft<br />-   `1`: Approved<br />-   `3`: Published<br /><br /> Ví dụ: chỉ định `filter=3` để chỉ hiển thị các bài viết trong cơ sở kiến thức đã xuất bản.<br /><br /> Nếu không có giá trị nào hoặc một giá trị sai được cung cấp thì giá trị mặc định (3) sẽ được sử dụng. |
| blockClick | Một giá trị số nguyên để chỉ ra có nên chặn hiển thị nội dung nội tuyến khi kết quả tìm kiếm được bấm vào trong kiểm soát tổ chức không. Đặt vào trong `0` để mở nội dung nội tuyến khi bấm vào, đặt `1` để chặn mở nội dung nội tuyến. Ví dụ: `blocked=1`<br /><br /> Nếu không có giá trị nào hoặc một giá trị sai được cung cấp thì giá trị mặc định (0) sẽ được sử dụng. If you have the set the value to 1 to block the content, the [ResultOpen](../unified-service-desk/km-control-hosted-control.md#ResultOpen) event will still be fired. |
|    sắp xếp    | Một giá trị số nguyên để chỉ ra các tùy chọn sắp xếp cho bài viết trong cơ sở kiến thức trong kết quả tìm kiếm:<br /><br /> -   `1`: Mức độ liên quan (mặc định)<br />-   `2`: Xếp hạng<br />-   `3`: Số lượt xem<br />-   `4`: Ngày sửa đổi lần cuối (cũ nhất trước tiên)<br />-   `5`: Ngày sửa đổi lần cuối (mới nhất trước tiên)<br /><br /> Ví dụ: chỉ định `sort=2` để sắp xếp các bài viết dựa trên xếp hạng.<br /><br /> Nếu không có giá trị nào hoặc một giá trị sai được cung cấp thì giá trị mặc định (1) sẽ được sử dụng cho tham số dữ liệu này. |

<a name="SetArticleContext"></a>   
### <a name="setarticlecontext"></a>SetArticleContext  
 Attaches data to the current knowledge base article in **Unified Interface KM Control**.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`articleapplication`|Tên của kiểm soát tổ chức nơi hiển thị bài viết trong cơ sở kiến thức.|  
|`articledata`|An article record object value passed from the [ResultOpen](../unified-service-desk/km-control-hosted-control.md#ResultOpen) event.|  

<a name="SetSearchProps"></a>   
### <a name="setsearchprops"></a>SetSearchProps  
 Enables different type of filters to search for knowledge base articles in **Unified Interface KM Control**.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`showFilter`|Cho biết có bật bộ lọc loại bài viết để tìm kiếm bài viết trong cơ sở kiến thức hay không. Đặt `0` để ẩn bộ lọc và `1` để hiển thị bộ lọc. Ví dụ: `showFilter=1`.<br /><br /> Nếu không có giá trị nào hoặc giá trị sai được cung cấp thì giá trị mặc định (0) sẽ được sử dụng.|  
|`showLang`|Cho biết có bật bộ lọc ngôn ngữ để tìm kiếm bài viết trong cơ sở kiến thức hay không. Đặt `0` để ẩn bộ lọc và `1` để hiển thị bộ lọc. Ví dụ: `showLang=1`.<br /><br /> Nếu không có giá trị nào hoặc giá trị sai được cung cấp thì giá trị mặc định (0) sẽ được sử dụng.|

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
 Occurs when a search result is opened for reading content in **Unified Interface KM Control**.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`postdata`|The formdata object containing a set of key/value pairs representing form fields and their values for a knowledge article.|  

<a name="SearchComplete"></a>   
### <a name="searchcomplete"></a>SearchComplete  
 Xảy ra sau khi tìm kiếm bài viết trong cơ sở kiến thức được hoàn tất, và kết quả tìm kiếm đã tải trong kiểm soát tổ chức.  

### <a name="selectionchange"></a>SelectionChange  
 Occurs when a result is selected in **Unified Interface KM Control**.  

|Tham số|Mô tả|  
|---------------|-----------------|  
|`postdata`|The formdata object containing a set of key/value pairs representing form fields and their values for a knowledge article.|  

### <a name="see-also"></a>Xem thêm
 
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)
