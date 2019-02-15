---
title: Configure session information | MicrosoftDocs
description: Learn about configuring session information.
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
ms.assetid: 574034ed-82c1-4db4-ac64-786591397e74
caps.latest.revision: 5
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: c2d953516beb9e70331ca47bf7b83339ca72c037
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385493"
---
# <a name="configure-session-information"></a>Configure session information
Thông tin phiên sẽ được hiển thị dưới tab trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] theo hai vùng: tên tab phiên và tổng quan về phiên. For an overview about this, see [Session management in Unified Service Desk](../unified-service-desk/session-management-unified-service-desk.md). Bạn có thể đặt cấu hình định dạng thông tin hiển thị như tên tab phiên và tổng quan bằng cách tạo nguyên tắc dòng phiên phù hợp.  
  
<a name="SessionName"></a>   
## <a name="configure-the-session-tab-name-format"></a>Đặt cấu hình định dạng tên tab phiên  
  
1. Đăng nhập vào ứng dụng [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. Click **Session Lines**.  
  
4. Trên trang **Thông tin phiên mới**:  
  
   1.  Nhập giá trị số nguyên (nói 100) trong trường **Thứ tự** để bảo rằng quy tắc của bạn thực hiện theo thứ tự đúng.  
  
   2.  Nhập tên có nghĩa trong trường **Tên**.  
  
   3.  Trong trường **Thực thể được chọn**, nhập tên thực thể mà tab phiên sẽ được hiển thị.  
  
   4.  Từ danh sách thả xuống **Loại**, chọn **Tên phiên**.  
  
   5.  In the **Display** field, type the display format for the tab. In this case, we want to display the name of the account followed by a dash, and then the primary contact name for the account. Nhập giá trị sau: [[account.name]]-[[account.address1_primarycontactname]].  
  
   ![Configure session tab name](../unified-service-desk/media/usd-configure-session-name.png "Configure session tab name")  
  
        Alternatively, you can use replacement parameters as well to pick up values at runtime, and dynamically display the tab name. For example, to display the name of the account followed by a dash and ending with the name of the activity that started the session (such as chat, or phonecall). Type the following value: [[account.name]]-[[$Context.InitialEntity]].  
  
       > [!NOTE]
       >  If all replacement values have matching values in it’s dataset, the rule will be used and the system will stop looking for subsequent rules. If one or more replacement values can’t be replaced, because the data doesn’t exist, the rule will fail and the system will try the next rule ordering to the Order field (checked in order of lowest to highest).  
  
        In the preceding example, [[account.name]] will be looking for the name field from an account entity that has been loaded somewhere within the current session. Because we used the lowercased version of “account” that matches to the entity name in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps, it means that it is looking for the last account page loaded no matter which tab it happens to be loaded within. Because of this, if you load a subaccount and your rules have it loading in a subaccount tab (thus displaying your primary account in the Account tab, and your subaccount in your Sub Account tab), the account name that will be used will be that of the sub account. This is because the subaccount is loaded after the Account tab. If you instead wish to always use the account name of the account that is displayed in the Account tab, you would use the following: **[[Account.name]]**.  
  
        The [[$Context.InitialEntity]] value is replaced at runtime with the InitialEntity context variable. This is a special context variable populated by the system with the entity name that is used to start the session.  
  
5. Bấm vào **Lưu**.  
  
<a name="SessionOverview"></a>   
## <a name="define-session-overview-information"></a>Define session overview information  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. Click **Session Lines**.  
  
4. Trên trang **Thông tin phiên mới**,  
  
   1. Type an integer value (say 100) in the **Order** field to ensure that your rule executes in the proper order.  
  
   2. Nhập tên có nghĩa trong trường **Tên**.  
  
   3. Trong trường **Thực thể được chọn**, nhập tên thực thể mà thông tin tổng quan phiên sẽ được hiển thị.  
  
   4. Từ danh sách thả xuống **Loại**, chọn **Dòng tổng quan về phiên**.  
  
   5. In the **Display** field, specify XAML script that defines the layout and content of the overview area. You can use designer tools such as [!INCLUDE[pn_blend_for_visual_studio](../includes/pn-blend-for-visual-studio.md)] to create and design the XAML script, and then copy it in this field. The XAML script must be properly formatted for it to display correctly in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
   ![Configure session overview](../unified-service-desk/media/usd-configure-session-overview.png "Configure session overview")  
  
5. Bấm vào **Lưu**.  
  
<a name="scriptlet"></a>   
## <a name="define-session-overview-information-using-scriptlets"></a>Xác định thông tin tổng quan phiên sử dụng Scriptlet  
 Với những nhà phát triển đã quen với [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)], bạn có thể sử dụng Scriptlet để hiển thị thông tin tổng quan phiên. Ví dụ:.  
  
1. Bạn có thể tạo scriptlet, cho biết **Đầu ra địa chỉ**, mà chấp nhận tất cả các giá trị địa chỉ.  
  
2. Bằng cách sử dụng [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)], bạn có thể sử dụng các chức năng chuỗi để thực hiện nối chuỗi để tạo đầu ra mong muốn.  
  
3. In your XAML for the session overview information definition, use the following replacement parameter:  
  
   ```  
   [[script.Address Output]]  
   ```  
  
   Tại thời gian chạy, điều này khởi động việc thực hiện scriptlet mà định dạng đầu ra địa chỉ như bạn đã chỉ định. Nếu scriptlet của bạn là một ngoại lệ, các quy tắc sẽ được bỏ qua. Phương pháp này thường là phương pháp ưa thích khi kiểu `AutoCollapse` là chưa đủ để ẩn các đánh dấu liên quan trong đầu ra theo yêu cầu. The replacement parameter may output XAML as well, which will be substituted before the XAML processor interprets the final result.  
  
<a name="Alerts"></a>   
## <a name="displaying-alerts-in-the-session-overview-information"></a>Hiển thị cảnh báo trong thông tin tổng quan về phiên  
 Cảnh báo là thông báo cho người dùng về thông tin quan trọng liên quan đến khách hàng. Một hệ thống cảnh báo cơ bản được tích hợp vào cơ chế thông tin phiên. Dòng phiên được đánh giá và hiển thị khi tất cả các tham số thay thế đã được thay thế và không có ngoại lệ từ Scriptlet. Sử dụng thông tin này, bạn có thể hiển thị dòng đầu ra tùy chọn trong vùng thông tin tổng quan về phiên của màn hình dựa trên sự tồn tại hoặc lựa chọn thực thể hoặc giá trị tìm kiếm thực thể. Sau đó sử dụng Scriptlet để kiểm tra giá trị cụ thể, và trả về một giá trị nếu bạn muốn hiển thị cảnh báo hoặc thêm ngoại lệ nếu bạn không muốn hiển thị.  
  
 Đây là một scriptlet ví dụ kiểm tra để xem nếu tài khoản đã tải có được tin cậy không.  
  
 ![Example scriptlet in Unified Service Desk](../unified-service-desk/media/usd-sample-scriptlet.png "Example scriptlet in Unified Service Desk")  
  
 Nhận thấy rằng thuộc tính `creditonhold` đã được chọn cho tài khoản. Nếu giá trị là `true`, giá trị sẽ trả về `true`, nếu không hãy đưa ra ngoại lệ. Tiếp theo dưới đây là dòng tổng quan về phiên mà hiển thị hộp văn bản và nút (thông báo của tôi) nếu giá trị là `true`.  
  
 ![Display alerts in Unified Service Desk](../unified-service-desk/media/usd-sample-session-information.png "Display alerts in Unified Service Desk")  
  
 Chú ý lệnh được đánh dấu. Lệnh này trên cột mà không hiển thị cho người dùng. Thay vào đó tham số thay thế ở đây sẽ làm hiển thị hoặc bỏ qua dòng tổng quan phiên này. Nếu scriptlet Đúng về khả năng tin cậy là ngoại lệ, Hệ thống sẽ không hiển thị bất kỳ nguyên tố thông tin phiên nào. Bây giờ chúng tôi có điều kiện quyết định thời điểm cảnh báo, hãy xem nút và một số tính năng thú vị ở đây.  
  
 Since there is no code behind for this XAML, we take advantage of another XAML feature, Commands. There is a special command defined in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], “USD:ActionCommands.DoActionCommand”. Lệnh này được thiết kế để gọi hành động [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] trên bất kỳ ứng dụng trong phiên đang chạy tổng đài viên của bạn. The CommandParameter is a URL encoded action call, with the following format.  
  
```  
http://uii/[UII Hosted Application]/[Action]?[Parameter]  
```  
  
 Hành động phải được cấu hình như hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] cho ứng dụng tổ chức[!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] được chỉ định. This button calls the GotoTask action on the AgentScripting application and passes “Welcome” as the parameter. For the AgentScripting application, this call locates the task with the name, “Welcome” and jumps to that task, thus displaying a new agent script.  
  
 The image source uses a special image loader defined in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] called CRMImageLoader and must be defined in the Grid resources.  
  
 Bây giờ khi bạn chỉ định một biểu thức ràng buộc, bạn có thể chỉ định nguồn như là tên nguồn tài nguyên ảnh. This causes [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to load the image from the web resources in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps and show in the button. Using this method, you can refer to resources from [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps in your [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)] (WPF) that is in your session overview. You may also specify an insecure URL for the image source. Specifying the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps image via the URL doesn’t work because authentication with the server is required to access it. WPF components do not authenticate against the URL when it attempts to load components.  
  
### <a name="see-also"></a>Xem thêm  
 [Quản lý phiên trong Unified Service Desk](../unified-service-desk/session-management-unified-service-desk.md)   
 [Thực hiện mã lệnh sử dụng Scriptlet trong Unified Service Desk](../unified-service-desk/execute-scripts-using-scriptlets-unified-service-desk.md)   
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)   
 [Cấu hình ứng dụng tổng đài viên của bạn bằng cách sử dụng Unified Service Desk](../unified-service-desk/configure-agent-application-unified-service-desk.md)
