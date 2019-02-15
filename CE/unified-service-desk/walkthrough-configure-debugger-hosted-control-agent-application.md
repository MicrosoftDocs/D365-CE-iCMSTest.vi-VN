---
title: 'Walkthrough 6: Configure the Debugger hosted control in your agent application | MicrosoftDocs'
description: ''
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
ms.assetid: 2d7bf294-165e-4beb-ac94-a9b1488f301e
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
ms.openlocfilehash: 37dacf9b90b769480a0852a23ba24f8729f6c609
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386573"
---
# <a name="walkthrough-6-configure-the-debugger-hosted-control-in-your-agent-application"></a>Walkthrough 6: Configure the Debugger hosted control in your agent application
[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] provides a **Debugger** type of hosted control, which provides you key information about your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration that helps you to successfully build an agent application and troubleshoot issues in your configuration. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Debug issues in Unified Service Desk](../unified-service-desk/debug-issues-unified-service-desk.md )  

 This walkthrough demonstrates how to configure a Debugger hosted control for your agent application.  

## <a name="prerequisites"></a>Điều kiện tiên quyết  

- You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) and [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md). The configurations that you completed in those walkthroughs are required in this walkthrough.  

- Cách này giả định rằng bạn sẽ đang sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên ở cuối cách này để kiểm tra ứng dụng. If a different user will be testing the application, you must assign the user to **Contoso Configuration**. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)  

- You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  

  - Debugger hosted control. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Debugger (Hosted Control)](../unified-service-desk/debugger-hosted-control.md)  

  - Action call and how to configure it. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Action calls](../unified-service-desk/action-calls.md)  

  - Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Manage access using Unified Service Desk configuration](admin/manage-access-using-unified-service-desk-configuration.md)  

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a>In This Walkthrough  
 [Bước 1: Tạo loại trình gỡ lỗi của kiểm soát tổ chức](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md#Step1)  

 [Bước 2: Thêm nút thanh công cụ và cuộc gọi hành động để hiển thị kiểm soát tổ chức trình gỡ lỗi](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md#Step2)  

 [Bước 3: Thêm kiểm soát vào cấu hình](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md#Step3)  

 [Bước 4: Kiểm tra ứng dụng](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md#Step4)  

 [Kết luận](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md#conclusion)  

<a name="Step1"></a>   
## <a name="step-1-create-a-debugger-type-of-hosted-control"></a>Step 1: Create a Debugger type of hosted control  

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

   ![Create a Debugger hosted control](../unified-service-desk/media/usd-create-session-lines-hosted-control.png "Create a Debugger hosted control")  

6. Bấm vào **Lưu**.  

<a name="Step2"></a>   
## <a name="step-2-add-toolbar-button-and-action-call-to-display-the-debugger-hosted-control"></a>Step 2: Add toolbar button and action call to display the Debugger hosted control  
 Add a toolbar button to **Contoso Main Toolbar** (created in [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md)), and then add an action call for the button to display the **Contoso Debugger** hosted control that you created in step 1.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Bấm vào **Thanh công cụ**.  

4. Click **Contoso Main Toolbar**.  

5. In the **Buttons** area, click **+** to add a toolbar button.  

6. On the **New Toolbar Button** page, specify the following values.  


   |    Trường    |                                                                              Value                                                                               |
   |-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    Tên     |                                                                     Contoso Debugger Button                                                                      |
   | Văn bản nút |                                                                             TRÌNH GỠ LỖI                                                                             |
   |    Thứ tự    | 3 **Note:**  The **Order** field defines the position of buttons in the toolbar. Buttons are arranged from left to right or top to bottom in an ascending order. |


7. Bấm vào **Lưu**.  

8. In the **Actions** area, click **+** to create an action call for the button  

9. In the search box, press **ENTER** or click the search icon, and then click **New** in the lower-right corner of the search results pane to create an action call.  

10. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.  

    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Cuộc gọi hành động Contoso: Hiển thị Trình gỡ lỗi|  
    |Đơn hàng|1|  
    |Kiểm soát tổ chức|Trình quản lý chung contoso|  
    |Hành động|CallDoAction|  
    |Dữ liệu|action=default<br />application=Contoso Debugger|  

    ![Create action call in Unified Service Desk](../unified-service-desk/media/usd-session-tab-name-format.png "Create action call in Unified Service Desk")  

11. Bấm vào **Lưu**.  

<a name="Step3"></a>   
## <a name="step-3-add-the-controls-to-the-configuration"></a>Step 3: Add the controls to the configuration  
 Add the action call and hosted control that you created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration. **Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).  

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

6. On the next page, click **Add Existing Action Call**, type “`Contoso Action Call: Show Debugger`” in the search bar, and then press ENTER or click the search icon.  

7. In the search results, click the action call name to add it.  

8. Similarly, add the hosted control by clicking the down arrow next to **Contoso Configuration**, and clicking **Hosted Controls**.  

9. Bấm vào **Lưu**.  

<a name="Step4"></a>   
## <a name="step-4-test-the-application"></a>Step 4: Test the application  
 Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md). For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).  

 Your agent application will now have a **DEBUGGER** button in the toolbar area. Clicking this button displays the Debugger control.  

 ![Debugger in your agent application](../unified-service-desk/media/usd-debugger-agent-application.png "Debugger in your agent application")  

<a name="conclusion"></a>   
## <a name="conclusion"></a>Kết luận  
 In this walkthrough, you saw how to configure the Debugger hosted control in your agent application. You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.  

### <a name="see-also"></a>Xem thêm  

 [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)   

 [Walkthrough 2: Display an external webpage in your agent application](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md)   

 [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md)   

 [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md)   

 [Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md)   

 [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md)   

 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
