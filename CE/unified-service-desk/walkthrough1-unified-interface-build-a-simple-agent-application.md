---
title: 'Walkthrough 1: Build a simple agent application in Unified Service Desk for Dynamics 365 for Customer Engagement apps (Unified Interface apps) (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: Demonstrates how to set up a basic agent application from scratch using Unified Service Desk that can connect to Customer Engagement.
keywords: ''
ms.date: 05/07/2018
ms.service:
- usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 75042EF8-9CA4-464B-A587-47B1F8265210
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
ms.openlocfilehash: da14ff2b3c3ce13a79701d5036ae79b2f7428098
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387075"
---
# <a name="walkthrough-1-build-a-simple-agent-application-for-unified-interface-apps"></a>Walkthrough 1: Build a simple agent application for Unified Interface Apps
This walkthrough demonstrates how to set up a basic agent application from scratch using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] that can connect to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps. Ứng dụng tổng đài viên này cung cấp cho bạn máy tính để bàn trống không có bất kỳ chức năng và bạn có thể sử dụng nó khi bạn đi qua phần còn lại của các cách trong phần này. In this walkthrough, you’ll use the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration to filter out existing controls in the "New Environment" sample application package from appearing in your agent application.
  
## <a name="prerequisites"></a>Điều kiện tiên quyết  
  
- A [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] package must be deployed on your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance, and the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application must already be installed to test the application at the end of the walkthrough. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Install, upgrade, and deploy Unified Service Desk](../unified-service-desk/admin/install-upgrade-deploy-unified-service-desk.md)  
  
- You must have required [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps permissions to configure [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] and access the required [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps entities. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Access management in Unified Service Desk](../unified-service-desk/admin/security-unified-service-desk.md)  
  
- You must be familiar with the following concepts in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  
  
  - [Kiểm soát Tổ chức Unified Service Desk](../unified-service-desk/unified-service-desk-hosted-controls.md)  
  
  - Ba loại kiểm soát tổ chức này: Trình quản lý kết nối, trình quản lý chung và Bố cục bảng điều khiển. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)  
  
  - Lọc quyền truy sử dụng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)  
  
<a name="Top"></a>   
## <a name="in-this-walkthrough"></a>In This Walkthrough  
 [Bước 1: Tạo ra kiểm soát tổ chức cơ bản](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md#Step1) 
  
 [Bước 2: Thêm kiểm soát tổ chức vào cấu hình](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md#Step2)  
  
 [Bước 3: Chỉ định người dùng cho cấu hình](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md#Step3)  
  
 [Bước 4: Kiểm tra ứng dụng](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md#Step4)  
  
 [Kết luận](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md#Conclusion)  
  
<a name="Step1"></a>   
## <a name="step-1-create-the-basic-hosted-controls"></a>Bước 1: Tạo ra kiểm soát tổ chức cơ bản  
 Create the following three types of hosted control so that the application can connect to an instance of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps: Connection Manager, Global Manager, and Panel Type.  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. Click **Hosted Controls**.  
  
4. Bấm vào **Mới**.  
  
5. On the **New Hosted Control** page, specify the following values.  
  
   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Trình Quản lý kết nối contoso|  
   |Thứ tự Sắp xếp|1|  
   |USD Component Type|Trình Quản lý kết nối|  
  
   ![Connection Manager hosted control](../unified-service-desk/media/crm-itpro-usd-wt01-01.png "Connection Manager hosted control")
  
6. Bấm vào **Lưu**.  
  
7. Bấm vào **Mới** để tạo kiểm soát tổ chức khác.  
  
8. On the **New Hosted Control** page, specify the following values.  
  
   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Contoso Global Manager|  
   |Thứ tự Sắp xếp|2|  
   |USD Component Type|Trình Quản lý chung|  
  
   ![Global Manager hosted control](../unified-service-desk/media/crm-itpro-usd-wt01-02.png "Global Manager hosted control")
  
9. Bấm vào **Lưu**.  
  
10. Click **New** to create another hosted control.  
  
11. On the **New Hosted Control** page, specify the following values.  
  
    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Bố cục Bảng điều khiển chính Contoso|  
    |Loại Thành phần USD|Bố cục bảng điều khiển|  
    |Loại bảng điều khiển|Bảng điều khiển chính tiêu chuẩn|  
    |Application is Dynamic|Không|  
    |User Can Close|Bỏ chọn|  
  
    ![Panel Layout hosted control](../unified-service-desk/media/crm-itpro-usd-wt01-03.png "Panel Layout hosted control")  
  
12. Bấm vào **Lưu**.  
  
> [!IMPORTANT]
>  Nếu bạn không tạo loại **Bố cục bảng điều khiển** của kiểm soát tổ chức trong ứng dụng tổng đài viên của bạn, bố cục bảng điều khiển mặc định, **Bảng điều khiển chính tiêu chuẩn**, được tạo tự động khi bạn chạy ứng dụng khách. 
  
<a name="Step2"></a>   
## <a name="step-2-add-the-hosted-controls-to-a-configuration"></a>Bước 2: Thêm kiểm soát tổ chức vào cấu hình  
 Cấu hình trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] giúp bạn lọc các truy cập vào các thành phần được hiển thị trong ứng dụng tổng đài viên cho người dùng. Trong bước này, tạo cấu hình, và sau đó thêm kiểm soát tổ chức được tạo ra trước đó vào cấu hình.  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. Bấm **Cấu hình**.  
  
4. Bấm vào **Mới**.  
  
5. On the **New Configuration** page, type `Contoso Configuration` as the name of the configuration, and click **Save**.  
  
6. Sau khi cấu hình mới được lưu, trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh tên cấu hình, và sau đó chọn **Kiểm soát tổ chức**.  
  
7. Bấm vào **Thêm kiểm soát tổ chức hiện có**, nhập `Contoso` trong thanh tìm kiếm và sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.  
  
8. Ba hình thức kiểm soát tổ chức được thêm trước đó hiển thị trong kết quả tìm kiếm. Nhấp vào liên kết **Tìm kiếm thêm Hồ sơ**.  
  
9. Chọn ba kiểm soát tổ chức, bấm vào **Chọn**, và sau đó nhấp vào **thêm**.  
  
   ![Add the hosted controls to the configuration](../unified-service-desk/media/crm-itpro-usd-wt01-04.PNG "Add the hosted controls to the configuration")  
  
10. Kiểm soát tổ chức được thêm vào cấu hình. Bấm vào **Lưu**.  
  
<a name="Step3"></a>   
## <a name="step-3-assign-users-to-the-configuration"></a>Bước 3: Chỉ định người dùng cho cấu hình  
 Trong bước này, chỉ định người dùng cho cấu hình do đó khi họ đăng nhập bằng cách sử dụng ứng dụng khách [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], họ chỉ có thể truy cập ba kiểm soát tổ chức đã được thêm vào cấu hình này. Đối với cách này, chỉ chỉ định một người dùng cho cấu hình người sẽ thử nghiệm các ứng dụng ở phần cuối của cách này.  
  
1. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và sau đó chọn **Người dùng được gán**.  
  
2. Trên trang tiếp theo, bấm vào **Thêm Người dùng hiện có**, nhập tên của người dùng trong thanh tìm kiếm, sau đó nhấn ENTER hoặc nhấp biểu tượng tìm kiếm.  
  
3. Từ kết quả tìm kiếm, nhấp vào tên người dùng mà bạn muốn được chỉ định cho cấu hình. Người dùng được thêm vào cấu hình. Trong trường hợp này, chỉ định **Randy Blythe** cho cấu hình. Bấm vào **Lưu**.  
  
   ![User added to the configuration](../unified-service-desk/media/crm-itpro-usd-wt01-05.png "User added to the configuration") 
  
<a name="Step4"></a>   
## <a name="step-4-test-the-application"></a>Step 4: Test the application  
 Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in the previous step. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).  
  
 Ứng dụng tổng đài viên của bạn sẽ trông như sau.  
  
 ![Basic agent application without any controls](../unified-service-desk/media/crm-itpro-usd-wt01-06.png "Basic agent application without any controls")  
  
 Máy tính để bàn trong ứng dụng tổng đài viên là máy tính trống bởi vì không có kiểm soát nào khác được thêm vào **Cấu hình Contoso** ngoài kiểm soát tổ chức cần thiết để thiết lập ứng dụng tổng đài viên cơ bản. Trong phần còn lại của các cách, bạn sẽ thấy kiểm soát xuất hiện trong ứng dụng tổng đài viên vì bạn dần dần đặt cấu hình và thêm các kiểm soát vào **Cấu hình Contoso**. 
  
<a name="Conclusion"></a>   
## <a name="conclusion"></a>Kết luận  
 In this walkthrough, you saw how to quickly build a basic agent application that can connect to an instance of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps. You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.  
  
### <a name="see-also"></a>Xem thêm

 [Support for Unified Interface Apps in Unified Service Desk](../unified-service-desk/admin/Support-unified-interfaces-apps-usd.md)

 [Unified Interface Page (Hosted Control)](../unified-service-desk/unified-interface-page-hosted-control.md)

 [Unified Service Desk and Unified Interface Configuration Walkthroughs](../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md)
  
 [Walkthrough 2: Display an external webpage in your agent application](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md)

 [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)

 [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md)

 [Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md)

 [Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md)

 [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)
