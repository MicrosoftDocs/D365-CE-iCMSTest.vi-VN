---
title: Debugger (Hosted Control) | MicrosoftDocs
description: Learn about using Debugger hosted control type in Unified Service Desk to configure a debugger control in Unified Service Desk to provide you with insights about the process and code executions in the agent application.
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
ms.assetid: 227bba2c-87d2-489c-b91b-5fad0d3c1042
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
ms.openlocfilehash: fedc54aca5c6111ff9fe81dbff569635c736b974
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387683"
---
# <a name="debugger-hosted-control"></a>Debugger (Hosted Control)
Sử dụng loại kiểm soát tổ chức **trình gỡ lỗi** trong Unified Service Desk để cấu hình kiểm soát trình gỡ lỗi trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để cung cấp cho bạn những hiểu biết về các quá trình và thực hiện mã trong ứng dụng tổng đài viên. Tất cả ba mẫu ứng dụng trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] đi kèm với kiểm soát tổ chức trình gỡ lỗi cấu hình sẵn. For more information, see [Debug issues in Unified Service Desk](http://go.microsoft.com/fwlink/p/?LinkId=518149) in the Unified Service Desk Administration Guide.  
  
<a name="Create"></a>   
## <a name="create-a-debugger-hosted-control"></a>Tạo kiểm soát tổ chức trình gỡ lỗi  
 While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create. Phần này cung cấp thông tin về các trường cụ thể mà là duy nhất cho loại kiểm soát tổ chức **Trình gỡ lỗi**. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  
  
 ![Debugger hosted control](../unified-service-desk/media/crm-itpro-usd-debuggerhostedcontrol.PNG "Debugger hosted control")  
  
 In the **New Hosted Control** screen:  
  
- Trong vùng **Unified Service Desk**, chọn **Trình gỡ lỗi** từ danh sách thả xuống **Loại Thành phần USD**.  
  
- Trường **Hiển thị nhóm** hiển thị bảng điều khiển nơi hiển thị kiểm soát tổ chức này. **MainPanel** is the most common for this hosted control type. For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md). For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  
  
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
  
### <a name="setreplacementparameter"></a>Đặt Thông số thay thế  
 Thiết lập giá trị tham số tùy ý thay thế thành giá trị được chỉ định.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|appname|Tên tổ chức kiểm soát hoặc trường quan trọng cho các tham số thay thế.|  
|tham số|Tên chính phụ tham số thay thế.|  
|giá trị|Giá trị để đặt.|  
|chung|Đặt giá trị này thành **đúng** để đặt giá trị trong phiên giao dịch chung.<br /><br /> Đặt giá trị này thành **sai** để đặt giá trị trong phiên hiện hoạt.|  
  
### <a name="testscriptlet"></a>TestScriptlet  
 Chạy JavaScript được chỉ định như thể nó là một scriptlet. Khi thực hiện thành công, kết quả hiển thị trong một hộp thư.  
  
<a name="events"></a>   
## <a name="predefined-events"></a>Sự kiện được xác định trước  
 There aren’t any predefined events available for this hosted control type.  
  
### <a name="see-also"></a>Xem thêm  
 [Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md)   
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)   
 [Administration Guide for Unified Service Desk for Microsoft Dynamics CRM](http://go.microsoft.com/fwlink/p/?LinkID=394402)
