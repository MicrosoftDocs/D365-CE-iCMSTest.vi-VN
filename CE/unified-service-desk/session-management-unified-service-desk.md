---
title: Session management in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about session context and session management in Unified Service Desk.
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
ms.assetid: 9430fbca-3c70-4a62-a259-2c9c00871057
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: bdb929b33e85e8d8c9c82e3dbe9120063c61f866
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385581"
---
# <a name="session-management-in-unified-service-desk"></a>Session management in Unified Service Desk
Whenever you search for customer information in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], the system fetches the information from [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, and stores it in a session. Thông tin về các phiên và hồ sơ khách hàng đã tìm nạp được lưu trữ trong bối cảnh phiên. Bạn có thể xem thông tin về các phiên và bối cảnh phiên trong tham số **$Session** và **$Context** trong kiểm soát tổ chức **trình gỡ lỗi**.  
  
 Each session in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client is displayed in a tab in the main screen, and you can identify a session using the *session name* displayed on the tab. An area of the screen just below the tab displays information related to the customer. Phần này được gọi là vùng *tổng quan phiên* và có thể chứa các đánh dấu XAML mà hiển thị thành phần giao diện người dùng chẳng hạn như hộp văn bản, nút hoặc liên kết. Cả hai khu vực này có thể hiển thị bất kỳ thông tin nào từ một trong hai phiên bối cảnh hoặc các dữ liệu từ cửa sổ, kết quả tìm kiếm CTI hoặc tìm kiếm thực thể đã thực hiện được hiển thị.  
  
<a name="SessionContext"></a>   
## <a name="session-and-context-information"></a>Thông tin phiên và bối cảnh  
 Chúng ta hãy xem cách lưu trữ phiên và dữ liệu ngữ cảnh trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] khi bạn tìm kiếm thông tin khách hàng.  
  
1. Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. Bấm vào **tìm kiếm** trong thanh công cụ, và sau đó nhấp vào tên tài khoản để tìm kiếm.  
  
3. The customer information is displayed in a session tab. Open the **Debugger** hosted control by clicking the down arrow next to the settings option in the top-right corner, and selecting **Debug**.  
  
4. Nhấp vào tab **Tham số dữ liệu** và mở rộng **$Session** để xem thông tin phiên hiện tại.  
  
   ![Current session information](../unified-service-desk/media/usd-session-info.png "Current session information")  
  
5. Bây giờ, mở rộng tham số **$Context** để xem thông tin về hồ sơ khách hàng chẳng hạn như ID khách hàng, địa chỉ, và v.v. Bạn cũng sẽ tìm thấy thông tin về phiên.  
  
   ![Current session context information](../unified-service-desk/media/usd-session-context.png "Current session context information")  
  
<a name="SessionName"></a>   
## <a name="session-name"></a>Tên Phiên  
 Tên phiên là nhãn văn bản được hiển thị trên tab; nó giúp xác định phiên giao dịch cho tổng đài viên.  
  
 ![Session name in Unified Service Desk](../unified-service-desk/media/usd-session-name.png "Session name in Unified Service Desk")  
  
 In this example, there are two session tabs with the following session names: **Sidney Higa (sample)- Maintenance** and **Like some of our new products (sample)** – Information.  
  
 Tab phiên đầu tiên là cho các tài khoản, và tab phiên thứ hai là dành cho các trường hợp. You can define the format of the text for the session name for an entity using the **Session Lines** configuration (**Settings** > **Unified Service Desk** > **Session Lines**) in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps. For more information, see [Configure the session tab name format](../unified-service-desk/configure-session-information.md#SessionName).  
  
<a name="SessionOverview"></a>   
## <a name="session-overview"></a>Tổng quan về phiên  
 Mục nhập tổng quan phiên là duy nhất trong một thực tế có thể hiển thị nhiều theo kiểu xếp chồng trong vùng giao diện người dùng (UI). Mỗi mục tổng quan phiên có tất cả các thông số thay thế được thay thế thành công sẽ hiển thị trong cửa sổ đầu ra. For example, the following two session overview entries are available for the Adventure Works (sample)-US session tab: **General** and **Social Info**.  
  
 ![Session overview entries in Unified Service Desk](../unified-service-desk/media/usd-session-overview-1.png "Session overview entries in Unified Service Desk")  
  
 Những mục không được xác định thông thường bởi người dùng kinh doanh, tuy nhiên, người dùng kinh doanh có tay nghề có thể sao chép và dán mục sẵn có và thay thế các giá trị mà sẽ đáp ứng nhu cầu của họ. This is because the entries are actually XAML markup often seen in [!INCLUDE[pn_MS_Silverlight_full](../includes/pn-ms-silverlight-full.md)] or [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)] applications. Chúng có thể được tạo ra với công cụ thiết kế chẳng hạn như [!INCLUDE[pn_blend_for_visual_studio](../includes/pn-blend-for-visual-studio.md)] theo kiểu đồ họa hoặc bằng trình chỉnh sửa văn bản. The XAML markup must be properly formatted for it to display correctly in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
 You can define the session overview information for an entity using the **Session Lines** configuration (**Settings** > **Unified Service Desk** > **Session Lines**) in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps. For more information, see [Define session overview information](../unified-service-desk/configure-session-information.md#SessionOverview).  
  
### <a name="see-also"></a>Xem thêm  
 [Đặt cấu hình phiên thông tin](../unified-service-desk/configure-session-information.md)   
 [Dòng phiên (Kiểm soát tổ chức)](../unified-service-desk/session-lines-hosted-control.md)   
 [Tab Phiên (Kiểm soát tổ chức)](../unified-service-desk/session-tabs-hosted-control.md)   
 [Trình gỡ lỗi (Kiểm soát tổ chức)](../unified-service-desk/debugger-hosted-control.md)   
 [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md)   
 [Cách 5: Hiển thị thông tin phiên bổ sung bằng cách hiển thị tên và dữ liệu tổng quan về phiên](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md)
