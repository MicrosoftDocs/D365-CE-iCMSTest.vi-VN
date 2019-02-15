---
title: Panel Layout (Hosted Control) in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about using the Panel Layout hosted control to define the arrangement of panels in Unified Service Desk. Panels hold various hosted controls, and a panel layout defines the arrangement of various hosted controls on the main screen of the Unified Service Desk client application.
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
ms.assetid: bbc0cc8e-b45c-4ad6-a7e8-616dc1a00f53
caps.latest.revision: 7
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: b6618ca5b88c0eced94e9808357fd41e7904af9c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386793"
---
# <a name="panel-layout-hosted-control"></a>Panel Layout (Hosted Control)
Sử dụng kiểm soát tổ chức **Bố cục bảng điều khiển** để xác định sự sắp xếp của bảng trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Panels hold various hosted controls, and a panel layout defines the arrangement of various hosted controls on the main screen of the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application. [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] comes with several predefined panel types to support various layout options such as tabbed layout, deck, and stacked layout. For more information, see [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md).  
  
 Nếu loại **Bố cục bảng điều khiển** của kiểm soát tổ chức không được định nghĩa trong việc áp dụng, bảng điều khiển mặc định bố trí, bảng điều khiển chính tiêu chuẩn, được tạo ra tự động. Nếu bạn tạo loại **Bố cục bảng điều khiển** của kiểm soát tổ chức, bạn phải cấu hình thay thế cho bảng điều khiển chính tiêu chuẩn. Bất kỳ bố cục bảng điều khiển có thể được sử dụng trong vị trí của nó; tuy nhiên chúng ta thường chỉ cần xác định các bảng điều khiển chính tiêu chuẩn.  
  
## <a name="in-this-section"></a>In This Section  
 [Tạo tổ chức kiểm soát bố cục bảng điều khiển](../unified-service-desk/panel-layout-hosted-control.md#create)  
  
 [Thao tác UII được xác định trước](../unified-service-desk/panel-layout-hosted-control.md#actions)  
  
 [Sự kiện được xác định trước](../unified-service-desk/panel-layout-hosted-control.md#events)  
  
<a name="create"></a>   
## <a name="create-a-panel-layout-hosted-control"></a>Tạo tổ chức kiểm soát bố cục bảng điều khiển  
 While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create. Phần này cung cấp thông tin về các trường cụ thể mà là duy nhất cho loại kiểm soát tổ chức **Bố cục bảng điều khiển**. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  
  
 ![Panel Layout hosted control](../unified-service-desk/media/crm-itpro-usd-panellayouthostedcontrol.png "Panel Layout hosted control")  
  
 In the **New Hosted Control** screen:  
  
- Từ danh sách thả xuống **Loại thành phần USD**, chọn **Bố cục bảng điều khiển**.  
  
- Từ danh sách thả xuống **PanelType**, chọn loại bố cục bảng điều khiển để tạo ra. Bạn có thể chọn một trong các tùy chọn sau: **Bảng điều khiển chính tiêu chuẩn**, **Bảng điều khiển chính ruy băng**, **Phân chia theo chiều dọc**, **Phân chia theo chiều ngang**, **XAML**, và **người dùng định nghĩa**. Bố trí bảng điều khiển do người dùng xác định và XAML là các bảng điều khiển tuỳ chỉnh mà bạn xác định. For detailed information about each of the panel layouts, see [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md). Các trường trong trang này thay đổi dựa trên loại bảng điều khiển đã chọn.  
  
- Chọn **có** hoặc **Không** từ danh sách **ứng dụng là động** để xác định xem điều khiển lưu trữ là động hay không. Kiểm soát tổ chức động có thể là chung hoặc riêng. Kiểm soát tổ chức động chung được tải theo yêu cầu đầu tiên và bị ẩn sau đó và chúng có thể được yêu cầu tại bất kỳ thời điểm nào, chẳng hạn như trong một phiên chung, phiên bình thường hoặc quy trình làm việc. Kiểm soát tổ chức động chung chỉ có thể được tải sau khi phiên đã bắt đầu và mỗi phiên sử dụng một phiên bản ứng dụng khác nhau. Nếu kiểm soát tổ chức động là một phần của quy trình làm việc và chưa được bắt đầu khi quy trình làm việc bắt đầu, sau đó quy trình làm việc sẽ bắt đầu và đóng kiểm soát tổ chức khi quy trình làm việc hoàn tất.  
  
- Hộp kiểm**Người dùng có thể đóng** trở nên có sẵn nếu bạn chọn **có** trong danh sách **ứng dụng là động**. Chọn nó để xác định kiểm soát tổ chức có thể bị người dùng đóng.  
  
- Nếu bạn chọn **Phân chia theo chiều dọc**, **Phân chia theo chiều ngang**, **XAML**, hoặc **người dùng định nghĩa** trong danh sách **PanelType**, các hộp kiểm **ứng dụng là chung** trở nên có sẵn. Chọn nó để đặt kiểm soát tổ chức là chung. Kiểm soát tổ chức chung có thể được hiển thị bên ngoài phiên khách hàng. Kiểm soát giống như bảng thông tin của tổng đài viên, tường hoặc tìm kiếm là những hình thức sử dụng chung cho kiểm soát tổ chức chung. Kiểm soát tổ chức chung không có trạng thái phiên dành riêng cho phiên để khi bạn thay đổi phiên, các kiểm soát tổ chức chung tương tự vẫn được duy trì. Nếu hộp kiểm không được chọn, kiểm soát tổ chức trở thành kiểu dựa trên phiên. Kiểm soát dựa trên phiên tồn tại trong ngữ cảnh của phiên khách hàng. Nếu người dùng thay đổi sang một phiên khác, tất cả các trang phiên từ phiên trước đó được ẩn.  
  
- Nếu bạn chọn **Phân chia theo chiều dọc**, **Phân chia theo chiều ngang**, **XAML**, hoặc **người dùng định nghĩa** trong danh sách **PanelType**, trường **Hiển thị nhóm** trở nên có sẵn. Chỉ định một bảng điều khiển nơi kiểm soát tổ chức này sẽ được hiển thị. For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md).  
  
- Nếu bạn chọn **XAML** trong danh sách **PanelType**, trường **XAML** trở nên có sẵn nơi bạn chỉ định định nghĩa XAML cho loại bảng điều khiển của bạn.  
  
- Nếu bạn chọn **người dùng định nghĩa** trong danh sách **PanelType** trường **Cụm URI** và **Loại cụm** trở nên có sẵn. Trong trường **Cụm URI**, gõ tên của cụm của bạn. In the **Assembly Type** field, specify the following value: *\<AssemblyName>.\<ClassName>*. For detailed information about how to create a user defined panel layout see, [Create custom panel layout in Unified Service Desk](../unified-service-desk/create-custom-panel-layout.md).  
  
<a name="actions"></a>   
## <a name="predefined-uii-actions"></a>Predefined UII actions  
 These are the predefined actions for this hosted control type.  
  
<a name="Close"></a>   
### <a name="close"></a>Đóng  
 This action is used to close the hosted control.  
  
### <a name="fireevent"></a>FireEvent  
 Khuyến khích sự kiện được người dùng xác định từ loại hình kiểm soát tổ chức này.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên của sự kiện do người dùng xác định.|  
  
 Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này. For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).  
  
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
  
<a name="SetVisualProperty"></a>   
### <a name="setvisualproperty"></a>SetVisualProperty  
 Đặt thuộc tính ([UIElement](https://msdn.microsoft.com/library/windows/apps/windows.ui.xaml.uielement.aspx)) trực quan chẳng hạn như chiều cao, chiều rộng và khả năng hiển thị của một kiểm soát tổ chức. Cuộc gọi hành động này đặc biệt hữu ích để tự động hóa UI, chẳng hạn như tự động hiển thị hoặc ẩn bảng điều khiển. Familiarity with XAML and [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] layout is required for effectively using this action.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|elementname|Tên của yếu tố UI mà bạn muốn đặt thuộc tính chẳng hạn như `Expander`, `StackPanel` và `Grid`.<br /><br /> Ví dụ: `elementname=Expander`|  
|propertyname|Tên của thuộc tính cho yếu tố đã chỉ định mà bạn muốn đặt chẳng hạn như `Height`, `Width`, `Visibility` và `Color`.<br /><br /> Ví dụ: `propertyname=Visibility`|  
|giá trị|Chỉ định giá trị phù hợp cho thuộc tính đã chỉ định. Các loại giá trị được hỗ trợ cho tham số này là `string`, `enumeration`, `integer` hoặc `bool`.<br /><br /> Ví dụ: `value=Visible`|  
  
 For an example usage of this message, see [Step 3: Configure action calls to automatically display and hide the knowledge base search panel](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step3) in [Walkthrough 8: Use Parature knowledge within your agent application](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md).  
  
> [!NOTE]
>  Theo mặc định, hành động này chỉ tiếp xúc cho loại **Bố cục Bảng điều khiển** của kiểm soát tổ chức. To use the `SetVisualProperty` action with all other predefined [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] hosted control types that are derived from the [DynamicsBaseHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol) class, you must explicitly add a UII action called `SetVisualProperty` to the respective hosted control. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Add UII action for a hosted control](../unified-service-desk/add-uii-action-hosted-control.md)  
  
<a name="events"></a>   
## <a name="predefined-events"></a>Sự kiện được xác định trước  
 There aren’t any predefined events available for this hosted control type.  
  
### <a name="see-also"></a>Xem thêm  
 [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md)   
 [Hành động UII](../unified-service-desk/uii-actions.md)   
 [Sự kiện](../unified-service-desk/events.md)   
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)   
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)   
