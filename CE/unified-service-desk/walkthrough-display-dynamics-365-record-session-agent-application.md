---
title: 'Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application | MicrosoftDocs'
description: Demonstrates how to display Customer Engagement records in a session in your agent application using window navigation rules and session controls in Unified Service Desk.
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
ms.assetid: aabfbcd2-1289-4291-9ce7-9ffe0f03c3c7
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
ms.openlocfilehash: 219ccf291c26436049c1a9cc88de9f900e2cf3f7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387267"
---
# <a name="walkthrough-4-display-a-microsoft-dynamics-365-for-customer-engagement-apps-record-in-a-session-in-your-agent-application"></a>Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application
This walkthrough demonstrates how to display [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps records in a session in your agent application using window navigation rules and session controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Nó cũng trình bày việc sử dụng các tham số thay thế để hiển thị động tên của kiểm soát tổ chức dựa trên hồ sơ tài khoản hiện đang được hiển thị. This walkthrough is built on top of the previous walkthrough, [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md), to display an account record in a session when you click on one of the accounts in the **Account** search result window.  
  
## <a name="prerequisites"></a>Điều kiện tiên quyết  
  
- You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) and [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md). Các cấu hình mà bạn hoàn thành trong các cách này được yêu cầu trong cách này.  
  
- Cách này giả định rằng bạn sẽ đang sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên ở cuối cách này để kiểm tra ứng dụng. If a different user will be testing the application, you must assign the user to **Contoso Configuration**. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)  
  
- You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  
  
  - Loại kiểm soát tổ chức **Tab Phiên**. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Session Tabs (Hosted Control)](../unified-service-desk/session-tabs-hosted-control.md)  
  
  - How to configure [Action calls](../unified-service-desk/action-calls.md)  
  
  - How to configure window navigation rules. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Use window navigation rules in Unified Service Desk](../unified-service-desk/use-window-navigation-rules-unified-service-desk.md)  
  
  - Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)  
  
## <a name="in-this-walkthrough"></a>In This Walkthrough  
 [Bước 1: Tạo kiểm soát tổ chức theo phạm vi phiên để hiển thị hồ sơ tài khoản trong phiên](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md#Step1)  
  
 [Bước 2: Đặt cấu hình các sự kiện để đóng kiểm soát tổ chức từ nơi xuất phát tìm kiếm](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md#Step2)  
  
 [Bước 3: Tạo kiểm soát tổ chức tab phiên](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md#Step3)  
  
 [Bước 4: Tạo quy tắc chuyển hướng cửa sổ để hiển thị hồ sơ tài khoản trong phiên](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md#Step4)  
  
 [Bước 5: Thêm kiểm soát vào cấu hình](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md#Step5)  
  
 [Bước 6: Kiểm tra ứng dụng](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md#Step6)  
  
 [Kết luận](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md#Conclusion)  
  
<a name="Step1"></a>   
## <a name="step-1-create-a-session-scoped-hosted-control-to-display-account-record-in-a-session"></a>Bước 1: Tạo kiểm soát tổ chức theo phạm vi phiên để hiển thị hồ sơ tài khoản trong phiên  
 Trong bước này, bạn sẽ tạo kiểm soát tổ chức theo phạm vi phiên để hiển thị hồ sơ tài khoản trong phiên.  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. Click **Hosted Controls**.  
  
4. Bấm vào **Mới**.  
  
5. On the **New Hosted Control** page, specify the following values.  
  
   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Phiên Tài khoản contoso|  
   |Tên Hiển thị|[[account.name]] **Note:**  We will use replacement parameter to dynamically display the name of the selected account as hosted control display name.|  
   |Loại Thành phần USD|Trang CRM|  
   |Cho phép nhiều trang|No|  
   |Loại lưu trữ|WPF nội bộ|  
   |Application is Global|Not checked **Note:**  This ensures that the hosted control is session-scoped, that is, only displayed in a session.|  
   |Nhóm hiển thị|Bảng điều khiển chính|  
  
   ![Create a session-scoped hosted control](../unified-service-desk/media/usd-create-session-scoped-hosted-control.png "Create a session-scoped hosted control")  
  
6. Bấm vào **Lưu**.  
  
<a name="Step2"></a>   
## <a name="step-2-configure-the-event-to-close-the-hosted-control-from-where-the-search-originated"></a>Bước 2: Đặt cấu hình các sự kiện để đóng kiểm soát tổ chức từ nơi xuất phát tìm kiếm  
 Trong bước này, bạn sẽ đặt cấu hình sự kiện **BrowserDocumentComplete** trên kiểm soát tổ chức **Phiên tài khoản Contoso** để khi nó được tải, kiểm soát tổ chức chính từ nơi người dùng nhấp vào để mở tài khoản, **Tìm kiếm tài khoản Contoso** bị đóng lại. The **Contoso Accounts Search** hosted control was created in [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md). Điều này được thực hiện để đảm bảo rằng người dùng không thể mở thông tin tài khoản khác trong cùng một tab phiên.  
  
1. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh kiểm soát tổ chức **Phiên tài khoản Contoso**, sau đó nhấp vào **Sự kiện**.  
  
   ![Configure events for a hosted control](../unified-service-desk/media/usd-configure-events-hosted-control2.png "Configure events for a hosted control")  
  
2. On the events page, click **BrowserDocumentComplete**.  
  
3. On the **BrowserDocumentComplete** page, click **+** in the **Active Actions** area to add an action call to the event.  
  
4. Trong hộp tìm kiếm, nhấn biểu tượng tìm kiếm hoặc nhấn ENTER, sau đó nhấp vào **Mới** ở góc dưới bên phải của hộp kết quả tìm kiểm.  
  
   ![Add an action call to an event](../unified-service-desk/media/usd-add-action-call-event.png "Add an action call to an event")  
  
5. On the **New Action Call** page, specify the following values.  
  
   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Các cuộc gọi hành động contoso: Đóng Tìm kiếm tài khoản|  
   |Kiểm soát được lưu trữ|Tìm kiếm tài khoản Contoso|  
   |Hành động|Đóng|  
  
   ![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call.png "Create an action call in Unified Service Desk")  
  
6. Bấm vào **Lưu** để thêm cuộc gọi hành động vào sự kiện **BrowserDocumentComplete**.  
  
<a name="Step3"></a>   
## <a name="step-3-create-a-session-tabs-hosted-control"></a>Bước 3: Tạo kiểm soát tổ chức tab phiên  
 Để hiển thị hồ sơ trong phiên trong ứng dụng tổng đài viên của bạn, một phiên bản loại **Tab phiên** của kiểm soát tổ chức phải được cấu hình trong ứng dụng tổng đài viên của bạn.  
  
1. Trên trang kiểm soát tổ chức, bấm vào **Mới**.  
  
2. Trên trang Kiểm soát tổ chức mới, chỉ định các giá trị sau.  
  
   |Trường|Value|  
   |-----------|-----------|  
   |Tên|Tab phiên Contoso|  
   |USD Component Type|Tab Phiên|  
  
   ![Create a Session Tabs hosted control](../unified-service-desk/media/usd-create-session-tabs-hosted-control.png "Create a Session Tabs hosted control")  
  
3. Bấm vào **Lưu**.  
  
<a name="Step4"></a>   
## <a name="step-4-create-a-window-navigation-rule-to-display-the-account-record-in-a-session"></a>Bước 4: Tạo quy tắc chuyển hướng cửa sổ để hiển thị hồ sơ tài khoản trong phiên  
 Trong bước này, bạn sẽ tạo một quy tắc chuyển hướng cửa sổ hiển thị hồ sơ trong phiên khi người dùng nhấp vào bất kỳ tài khoản nào trong cửa sổ kết quả tìm kiếm.  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. Click **Window Navigation Rules**.  
  
4. Bấm vào **Mới**.  
  
5. On the **New Window Navigation Rule** page, specify the following values.  
  
   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Quy tắc Phiên Tài khoản contoso|  
   |Đơn hàng|5|  
   |Từ|Tìm kiếm tài khoản Contoso|  
   |Thực thể|tài khoản|  
   |Loại định tuyến|Bật lên|  
   |Điểm đến|Tab|  
   |Hành động|Tạo phiên làm việc|  
   |Tab Mục tiêu|Phiên Tài khoản contoso|  
   |Hiển thị Tab|Contoso Account Session|  
   |Hide Command Bar|Không|  
   |Hide Navigation Bar|Có|  
  
   ![Create a window navigation rule](../unified-service-desk/media/usd-create-window-navigation-rule.png "Create a window navigation rule")  
  
6. Bấm vào **Lưu**.  
  
<a name="Step5"></a>   
## <a name="step-5-add-the-controls-to-the-configuration"></a>Step 5: Add the controls to the configuration  
 Trong bước này, bạn sẽ thêm cuộc gọi hành động, sự kiện, kiểm soát tổ chức và nguyên tắc điều hướng cửa sổ mà bạn đã cấu hình trong cách này thành **Cấu hình Contoso** để hiển thị các kiểm soát này cho người dùng được chỉ định cho cấu hình này. **Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).  
  
 Add the following to **Contoso Configuration**.  
  
|Tên kiểm soát|Loại kiểm soát|  
|------------------|------------------|  
|Các cuộc gọi hành động contoso: Đóng Tìm kiếm tài khoản|Cuộc gọi hành động|  
|Duyệt Tài liệu hoàn chỉnh|Sự kiện cho kiểm soát tổ chức Phiên tài khoản Contoso.|  
|Phiên Tài khoản contoso|Kiểm soát tổ chức|  
|Tab phiên Contoso|Kiểm soát tổ chức|  
|Quy tắc Phiên Tài khoản contoso|Window navigation rule|  
  
 To add a control to the configuration:  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. Bấm **Cấu hình**.  
  
4. Click **Contoso Configuration** to open the definition.  
  
5. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.  
  
6. Trên trang tiếp theo, bấm vào **Thêm Cuộc gọi Hành động Hiện có**, nhập “`Contoso Action Call: Close Accounts Search`” vào thanh tìm kiếm, sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.  
  
7. Trong hộp kết quả tìm kiếm, hãy nhấp vào cuộc gọi hành động để thêm vào **Cấu hình Contoso**.  
  
8. Tương tự, thêm sự kiện, kiểm soát tổ chức và nguyên tắc điều hướng cửa sổ bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Sự kiện** **Kiểm soát tổ chức** và **Nguyên tắc điều hướng cửa sổ** lần lượt.  
  
9. Bấm vào **Lưu**.  
  
<a name="Step6"></a>   
## <a name="step-6-test-the-application"></a>Step 6: Test the application  
  
1. Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured Unified Service Desk by using the same user credentials that is assigned to Contoso Configuration in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md). For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to CRM instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).  
  
2. To display the account records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance, click the down arrow next to the **Search** button in the toolbar, and then click **Account**.  
  
3. Click any of the account records to display the respective account information in a session; the information is displayed under a session tab. Note that the name of the hosted control tab that contains the account record automatically displays the account name because earlier you used replacement parameters to dynamically display the current account name instead of a static value.  
  
   ![Account record displayed in a session](../unified-service-desk/media/usd-account-record-session.png "Account record displayed in a session")  
  
4. Nếu bạn mở một hồ sơ tài khoản khác, nó sẽ được hiển thị trong một phiên khác trong ứng dụng khách của bạn. Để mở một tài khoản khác, bấm vào mũi tên xuống bên cạnh nút **Tìm kiếm**, hãy nhấp vào **Tài khoản**, và sau đó nhấp vào tên tài khoản để hiển thị các thông tin tài khoản trong một phiên khác.  
  
   ![Multiple sessions in Unified Service Desk](../unified-service-desk/media/usd-multiple-sessions.png "Multiple sessions in Unified Service Desk")  
  
<a name="Conclusion"></a>   
## <a name="conclusion"></a>Kết luận  
 In this walkthrough, you learned how to use the session hosted control and window navigation rules to display [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records in a session in your agent application. You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.  
  
> [!NOTE]
>  Try the next walkthrough to present enhanced session information in your agent application: [Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md).  
  
### <a name="see-also"></a>Xem thêm  
 [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)   
 
 [Walkthrough 2: Display an external webpage in your agent application](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md)   
 
 [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md)   
 
 [Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md)   
 
 [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md)   
 
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
