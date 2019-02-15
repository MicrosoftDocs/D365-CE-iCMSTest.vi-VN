---
title: 'Walkthrough 6: Configure the Debugger hosted control in your agent application | MicrosoftDocs'
description: ''
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
ms.assetid: B87B63D0-7BE3-4B43-806A-29429D9DE75A
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
ms.openlocfilehash: 65a46785236e8b187a190b7e7aef3e16176cf989
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385539"
---
# <a name="walkthrough-6-configure-the-debugger-hosted-control-in-your-agent-application"></a>Walkthrough 6: Configure the Debugger hosted control in your agent application
[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]cung cấp loại **trình gỡ lỗi** của kiểm soát tổ chức, cung cấp cho bạn thông tin quan trọng về cấu hình [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] của bạn mà sẽ giúp bạn xây dựng thành công ứng dụng tổng đài viên và khắc phục sự cố trong cấu hình của bạn. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Debug issues in Unified Service Desk](../unified-service-desk/debug-issues-unified-service-desk.md )  

 Cách này trình bày cách cấu hình kiểm soát tổ chức trình gỡ lỗi cho ứng dụng tổng đài viên của bạn.  

## <a name="prerequisites"></a>Điều kiện tiên quyết  

- You must have completed [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) and [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md). Các cấu hình mà bạn hoàn thành trong các cách này được yêu cầu trong cách này.  

- Cách này giả định rằng bạn sẽ đang sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên ở cuối cách này để kiểm tra ứng dụng. Nếu một người dùng khác sẽ thử nghiệm các ứng dụng, bạn phải gán người dùng vào **Cấu hình Contoso**. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)  

- You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  

  - Kiểm soát tổ chức trình gỡ lỗi. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Debugger (Hosted Control)](../unified-service-desk/debugger-hosted-control.md)  

  - Action call and how to configure it. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Action calls](../unified-service-desk/action-calls.md)  

  - Lọc quyền truy cập bằng cách sử dụng cấu hình [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Manage access using Unified Service Desk configuration](admin/manage-access-using-unified-service-desk-configuration.md)  

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a>In This Walkthrough  
 [Bước 1: Tạo loại trình gỡ lỗi của kiểm soát tổ chức](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md#Step1)  

 [Bước 2: Thêm nút thanh công cụ và cuộc gọi hành động để hiển thị kiểm soát tổ chức trình gỡ lỗi](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md#Step2)  

 [Bước 3: Thêm kiểm soát vào cấu hình](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md#Step3)  

 [Bước 4: Kiểm tra ứng dụng](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md#Step4)  

 [Kết luận](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md#conclusion)  

<a name="Step1"></a>   
## <a name="step-1-create-a-debugger-type-of-hosted-control"></a>Bước 1: Tạo loại trình gỡ lỗi của kiểm soát tổ chức  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Click **Hosted Controls**.  

4. Bấm vào **Mới**.  

5. On the **New Hosted Control** page, specify the following values:  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Trình gỡ lỗi Contoso|  
   |Thứ tự Sắp xếp|3|  
   |Tên hiển thị|Trình gỡ lỗi Contoso|  
   |USD Component Type|Trình gỡ lỗi|  
   |Nhóm hiển thị|Bảng điều khiển chính|  

   ![Create a Debugger hosted control](../unified-service-desk/media/usd-create-debugger-hosted-control-unified-interface.png "Create a Debugger hosted control")  

6. Bấm vào **Lưu**.  

<a name="Step2"></a>   
## <a name="step-2-add-toolbar-button-and-action-call-to-display-the-debugger-hosted-control"></a>Bước 2: Thêm nút thanh công cụ và cuộc gọi hành động để hiển thị kiểm soát tổ chức trình gỡ lỗi  
 Add a toolbar button to **Contoso Main Toolbar** (created in [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)), and then add an action call for the button to display the **Contoso Debugger** hosted control that you created in step 1.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Bấm vào **Thanh công cụ**.  

4. Bấm vào **Thanh công cụ chính Contoso**.  

5. In the **Buttons** area, click **+** to add a toolbar button.  

6. On the **New Toolbar Button** page, specify the following values.  


   |    Trường    |                                                                                Value                                                                                 |
   |-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    Tên     |                                                                       Nút Trình gỡ lỗi Contoso                                                                        |
   | Văn bản nút |                                                                               TRÌNH GỠ LỖI                                                                               |
   |    Thứ tự    | 3 <br> **Note:** The **Order** field defines the position of buttons in the toolbar. Buttons are arranged from left to right or top to bottom in an ascending order. |


7. Bấm vào **Lưu**.  

8. In the **Actions** area, click **+** to create an action call for the button  

9. Trong hộp tìm kiếm, nhấn **ENTER** hoặc nhấp vào biểu tượng tìm kiếm, và sau đó nhấp vào **Mới** ở góc dưới bên phải của ngăn kết quả tìm kiếm để tạo cuộc gọi hành động.  

10. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.  

    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Cuộc gọi hành động Contoso: Hiển thị Trình gỡ lỗi|  
    |Đơn hàng|1|  
    |Kiểm soát tổ chức|Trình quản lý chung contoso|  
    |Hành động|CallDoAction|  
    |Dữ liệu|action=default<br/>application=Contoso Debugger|  

    ![Create action call in Unified Service Desk](../unified-service-desk/media/usd-session-tab-name-format-action-call-unified-interface.png "Create action call in Unified Service Desk")  

11. Bấm vào **Lưu**.  

<a name="Step3"></a>   
## <a name="step-3-add-the-controls-to-the-configuration"></a>Bước 3: Thêm kiểm soát vào cấu hình  
 Thêm cuộc gọi hành động và kiểm soát tổ chức mà bạn đã tạo trong cách này vào **Cấu hình Contoso** để hiển thị các kiểm soát này cho người dùng được chỉ định cho cấu hình này. **Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).  

 Add the following to **Contoso Configuration**.  

|Tên kiểm soát|Loại kiểm soát|  
|------------------|------------------|  
|Cuộc gọi hành động Contoso: Hiển thị Trình gỡ lỗi|Cuộc gọi hành động|  
|Trình gỡ lỗi Contoso|Kiểm soát được lưu trữ|  

 To add a control to the configuration:  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Bấm **Cấu hình**.  

4. Click **Contoso Configuration** to open the definition.  

5. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.  

6. Trên trang tiếp theo, bấm vào **Thêm Cuộc gọi Hành động Hiện có**, nhập “`Contoso Action Call: Show Debugger`” vào thanh tìm kiếm, sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.  

7. In the search results, click the action call name to add it.  

8. Tương tự, thêm kiểm soát tổ chức bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Kiểm soát tổ chức**. 

9. Bấm vào **Lưu**.  

<a name="Step4"></a>   
## <a name="step-4-test-the-application"></a>Bước 4: Kiểm tra ứng dụng  
 Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md). For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).  

 Ứng dụng tổng đài viên của bạn bây giờ sẽ có nút **TRÌNH GỠ LỖI** trong vùng thanh công cụ. Bấm nút này sẽ hiển thị kiểm soát trình gỡ lỗi.  

 ![Debugger in your agent application](../unified-service-desk/media/usd-debugger-agent-application.png "Debugger in your agent application")  

<a name="conclusion"></a>  
## <a name="conclusion"></a>Kết luận 
 Trong cách này, bạn sẽ biết cách cấu hình kiểm soát tổ chức trình gỡ lỗi trong ứng dụng tổng đài viên của bạn. Bạn cũng biết cách lọc quyền truy cập vào kiểm soát [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] bằng cách sử dụng cấu hình.  

### <a name="see-also"></a>Xem thêm

 [Support for Unified Interface Apps in Unified Service Desk](../unified-service-desk/admin/Support-unified-interfaces-apps-usd.md)

 [Unified Interface Page (Hosted Control)](../unified-service-desk/unified-interface-page-hosted-control.md)

 [Unified Service Desk and Unified Interface Configuration Walkthroughs](../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md) 

 [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)

 [Cách 2: Hiển thị trang web bên ngoài trong ứng dụng tổng đài viên của bạn](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md)

 [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)

 [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md)

 [Cách 5: Hiển thị thông tin phiên bổ sung bằng cách hiển thị tên và dữ liệu tổng quan về phiên](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md)

 [Cách 7: Đặt cấu hình mã lệnh tổng đài viên trong ứng dụng tổng đài viên của bạn](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)
