---
title: User Notes (Hosted Control) in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about the User Notes type of hosted control in Unified Servoce Desk.
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
ms.assetid: 7d3fec60-2f91-4b25-8a80-f41def5a5f74
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
ms.openlocfilehash: cfe1da43c461a72cfe491e52678e13e238afa6f3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385568"
---
# <a name="user-notes-hosted-control"></a>User Notes (Hosted Control)
Sử dụng loại kiểm soát tổ chức **ghi chú người dùng** để cung cấp cho các tổng đài viên một tấm ghi để nhập ghi chú trong quá trình tương tác. Có thể áp dụng kiểm tra chính tả cho từng ngôn ngữ cho thành phần này bằng cách gọi thao tác **Đặt ngôn ngữ**. Thành phần này không tự động chọn ngôn ngữ hiện tại của người dùng, theo thiết kế. Khả năng thay đổi ngôn ngữ được sử dụng nhằm mục đích cung cấp khả năng thiết lập ngôn ngữ thích hợp cho các giao dịch. Ví dụ, xem xét có tổng đài viên song ngữ có thể nói tiếng Anh và tiếng Tây Ban Nha. IVR có thể vượt qua lựa chọn ngôn ngữ từ hệ thống điện thoại đến bộ điều hợp CRI của ứng dụng tổng đài viên. Lựa chọn ngôn ngữ này sau đó có thể được sử dụng để thiết lập ngôn ngữ để kiểm tra chính tả cho kiểm soát tổ chức này.  
  
> [!NOTE]
>  Kiểm soát tổ chức không tự động xác định tham số thay thế. The [UpdateReplacementParameters](#UpdateReplacementParameters) action can be called to take the current notes and populate the replacement parameters. Các tham số thay thế có thể được sử dụng để sao chép các ghi chú đến trường hợp.  
  
<a name="Create"></a>   
## <a name="create-a-user-notes-hosted-control"></a>Tạo kiểm soát tổ chức ghi chú người dùng  
 Trong khi tạo một hình thức kiểm soát tổ chức mới, các trường trong màn hình **Kiểm soát tổ chức mới** thay đổi dựa vào loại tổ chức tổ chức bạn muốn tạo. Phần này cung cấp thông tin về các trường cụ thể mà là duy nhất cho loại kiểm soát tổ chức **Ghi chú người dùng**. For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).  
  
 ![User Notes hosted control](../unified-service-desk/media/crm-itpro-usd-usernoteshostedcontrol.png "User Notes hosted control")  
  
 Trong màn hình **Kiểm soát tổ chức mới**:  
  
- Từ danh sách thả xuống **Loại thành phần USD**, chọn **Ghi chú người dùng**.  
  
- Trong trường **Hiển thị nhóm**, xác định bảng điều khiển nơi hiển thị kiểm soát tổ chức. For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels](../unified-service-desk/panels-panel-types-panel-layouts.md#Panels).  
  
<a name="Actions"></a>   
## <a name="predefined-uii-actions"></a>Thao tác UII được xác định trước  
 Đây là những thao tác được xác định trước cho loại kiểm soát tổ chức này.  
  
<a name="Close"></a>   
### <a name="close"></a>Đóng  
 Hành động này được sử dụng để đóng kiểm soát tổ chức.  
  
### <a name="fireevent"></a>FireEvent  
 Khuyến khích sự kiện được người dùng xác định từ loại hình kiểm soát tổ chức này.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|tên|Tên của sự kiện do người dùng xác định.|  
  
 Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này. For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).  
  
<a name="MoveToPanel"></a>   
### <a name="movetopanel"></a>MoveToPanel  
 Hành động này được sử dụng để di chuyển kiểm soát tổ chức giữa các bảng điều khiển tại thời gian chạy.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|ứng dụng|Tên của kiểm soát tổ chức được di chuyển.|  
|bảng điều khiển|Bảng điều khiển đích cho kiểm soát tổ chức.|  
  
### <a name="newcrmpage"></a>New_CRM_Page  
 Creates a page for creating a new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps record of the entity specified, and treats the page as a popup from the specified hosted control. Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi trang tạo hồ sơ thực thể được hiển thị.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|LogicalName|Tên logic của thực thể để tạo phiên bản mới.|  
  
> [!NOTE]
>  Phần còn lại của các tham số nên bao gồm tên = cặp giá trị. Đây là các giá trị nhập sẵn bổ sung trong hình thức để tạo hồ sơ mới cho thực thể đã chỉ định. For more information about using this action, see step 4 in [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md).  
  
### <a name="opencrmpage"></a>Open_CRM_Page  
 Mở một phiên bản hiện tại của các thực thể được chỉ định và xác định theo ID và xử lý trang như một thư mục bật lên từ kiểm soát tổ chức được chỉ định. Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi thư mục bật lên nên sẽ được hiển thị.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|LogicalName|Tên logic của thực thể hợp lý của thực thể để mở.|  
|id|ID của hồ sơ thực thể để mở.|  
  
### <a name="popup"></a>Bật lên  
 Bật lên URL từ kiểm soát tổ chức và chạy nguyên tắc điều hướng cửa sổ chống lại hình thức kiểm soát tổ chức để định tuyến bật lên đến vị trí thích hợp.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|url|Định tuyến bật lên từ kiểm soát tổ chức này sử dụng URL này như thể nó là một thư mục bật lên được yêu cầu từ kiểm soát được hiển thị.|  
|nền tảng|Nền tảng mà thư mục bật lên xuất phát.|  
  
<a name="RealignWindow"></a>   
### <a name="realignwindow"></a>RealignWindow  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]
  
<a name="SetSize"></a>   
### <a name="setsize"></a>SetSize  
 Hành động này đặt chiều rộng và chiều cao của kiểm soát tổ chức một cách rõ ràng. Quá trình này đặc biệt hữu ích khi sử dụng tính năng "tự động" trong bố cục bảng điều khiển của bạn.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|chiều rộng|Chiều rộng của kiểm soát tổ chức.|  
|chiều cao|Chiều cao của kiểm soát tổ chức.|  
  
<a name="UpdateReplacementParameters"></a>   
### <a name="updatereplacementparameters"></a>Cập nhật tham số thay thế  
 Hành động này được sử dụng để cập nhật một cách rõ ràng dữ liệu kiểm soát tổ chức **ghi chú người dùng** vào danh sách tham số thay thế. Điều này là không giống như các loại kiểm soát tổ chức khác nơi dữ liệu kiểm soát tổ chức được cập nhật tự động vào tham số thay thế.  
  
<a name="Event"></a>   
## <a name="predefined-events"></a>Sự kiện được xác định trước  
 Sự kiện được xác định trước sau đây có sẵn cho loại kiểm soát tổ chức này.  
  
### <a name="loaded"></a>Đã tải  
 Xảy ra khi kiểm soát tổ chức đã hoàn tất tải.  
  
### <a name="popuprouted"></a>Bật lên đã lên lịch  
 Xảy ra sau khi một cửa sổ bật lên đã được hệ thống xác định.  
  
|Tham số|Mô tả|  
|---------------|-----------------|  
|url|URL của cửa sổ bật lên đã được xác định.|  
  
### <a name="see-also"></a>Xem thêm  
 [Hành động UII](../unified-service-desk/uii-actions.md)   
 [Sự kiện](../unified-service-desk/events.md)   
 [Xem sự kiện và hành động xác định trước cho kiểm soát tổ chức](../unified-service-desk/view-predefined-actions-events-hosted-control.md)   
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)   
 [Tham chiếu loại kiểm soát tổ chức và hoạt động/sự kiện](../unified-service-desk/hosted-control-types-action-event-reference.md)   
 [Administration Guide for Unified Service Desk for Microsoft Dynamics CRM](http://go.microsoft.com/fwlink/p/?LinkID=394402)
