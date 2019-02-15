---
title: 'Walkthrough 2: Display an external webpage in your agent application | MicrosoftDocs'
description: Demonstrates how to display an external web page in Unified Service Desk.
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
ms.assetid: 516ceb5c-755a-49ab-89f5-fea3559b48cd
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 2d6b3ed05dee3bda75360e2b9924211e85699498
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387001"
---
# <a name="walkthrough-2-display-an-external-webpage-in-your-agent-application"></a>Walkthrough 2: Display an external webpage in your agent application
This walkthrough demonstrates how to display a webpage or external URL in your agent application. In this walkthrough, you’ll learn how to display the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] Guide, which is available online at http://go.microsoft.com/fwlink/?LinkID=856273, in the client application.  

## <a name="prerequisites"></a>Điều kiện tiên quyết  

- You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md). The configurations that you completed in the first walkthrough are required in this walkthrough.  

- Cách này giả định rằng bạn sẽ sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng ở cuối cách 1 để đăng nhập vào ứng dụng tổng đài viên. If a different user will be testing the application, you must assign the user to **Contoso Configuration**. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)  

- You must be familiar with the following concepts in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  

  - These two types of hosted controls: Standard Web Application and Toolbar Container. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)  

  - How to configure [Action calls](../unified-service-desk/action-calls.md)  

  - Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)  

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a>In This Walkthrough  
 [Bước 1: Tạo kiểm soát tổ chức để hiển thị trang web](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md#Step1)  

 [Bước 2: Tạo loại bộ chứa công cụ của kiểm soát tổ chức](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md#Step2)  

 [Bước 3: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md#Step3)  

 [Bước 4: Thêm nút thanh công cụ và các cuộc gọi hành động để hiển thị trang web](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md#Step4)  

 [Bước 5: Thêm kiểm soát vào cấu hình](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md#Step5)  

 [Bước 6: Kiểm tra ứng dụng](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md#Step6)  

 [Kết luận](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md#Conclusion)  

<a name="Step1"></a>   
## <a name="step-1-create-a-hosted-control-to-display-the-webpage"></a>Step 1: Create a hosted control to display the webpage  
 In this step, you’ll create a hosted control of Standard Web Application type to display the webpage.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Click **Hosted Controls**.  

4. Bấm vào **Mới**.  

5. On the **New Hosted Control** page, specify the following values:  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Contoso trợ giúp|  
   |Tên hiển thị|Contoso trợ giúp|  
   |Loại Thành phần USD|Ứng dụng web tiêu chuẩn|  
   |Cho phép nhiều trang|No|  
   |Loại tổ chức|WPF nội bộ|  
   |Application is Global|Đã kiểm tra|  
   |Nhóm hiển thị|Bảng điều khiển chính|  

   ![Standard Web Application hosted control](../unified-service-desk/media/crm-itpro-usd-wt02-01.png "Standard Web Application hosted control")  

6. Bấm vào **Lưu**.  

<a name="Step2"></a>   
## <a name="step-2-create-a-toolbar-container-type-of-hosted-control"></a>Step 2: Create a toolbar container type of hosted control  
 Kiểm soát tổ chức bộ chứa thanh công cụ được sử dụng để giữ và hiển thị thanh công cụ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. In this section, you’ll create a **Toolbar Container** type of hosted control that appears in the toolbar region of the client application.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Click **Hosted Controls**.  

4. Bấm vào **Mới**.  

5. On the **New Hosted Control** page, specify the following values:  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Contoso về Bộ chứa thanh công cụ|  
   |USD Component Type|Bộ chứa thanh công cụ|  
   |Nhóm hiển thị|AboutPanel|  

   ![Toolbar Container hosted control](../unified-service-desk/media/crm-itpro-usd-wt02-02.png "Toolbar Container hosted control")  

6. Bấm vào **Lưu**.  

<a name="Step3"></a>   
## <a name="step-3-add-a-toolbar-and-attach-it-to-the-toolbar-container"></a>Step 3: Add a toolbar and attach it to the toolbar container  
 In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 2. This is done to display the toolbar in your agent application.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Bấm vào **Thanh công cụ**.  

4. Bấm vào **Mới**.  

5. On the **New Toolbar** page, type **Contoso About Toolbar** in the **Name** box, and then click **Save**.  

6. Attach the toolbar to the toolbar container hosted control created in step 2. On the nav bar, click the down arrow next to **Contoso About Toolbar**, and click **Hosted Controls**.  

7. Trên trang tiếp theo, bấm vào **Thêm kiểm soát tổ chức hiện có**, nhập `Contoso About Toolbar Container` trong thanh tìm kiếm và sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.  

8. Từ kết quả tìm kiếm, chọn **Bộ chứa thanh công cụ về Contoso**.  

9. Bấm vào **Lưu**.  

<a name="Step4"></a>   
## <a name="step-4-add-a-toolbar-button-and-action-calls-to-display-the-webpage"></a>Bước 4: Thêm nút thanh công cụ và các cuộc gọi hành động để hiển thị trang web  
 Trong bước này, thêm một nút trên thanh công cụ và đính kèm một cuộc gọi hành động cho nút để khi nút được nhấn vào, trang web đã chỉ định được hiển thị trong kiểm soát tổ chức mà bạn đã tạo ở bước 1.  

1. After you save the toolbar in step 3, the **Buttons** area becomes available. In the **Buttons** area, click **+** on the right corner to add a button.  

2. On the **New Toolbar Button** page, specify the following values.  

   |Trường|Value|  
   |-----------|-----------|  
   |Tên|Contoso Show Help|  
   |Văn bản nút|Hiển thị trợ giúp|  

   ![Create a new toolbar button](../unified-service-desk/media/crm-itpro-usd-wt02-03.png "Create a new toolbar button")  

3. Click **Save** to save the record, and enable the **Actions** area.  

4. Add two action calls to specify the URL of the webpage to navigate to for the hosted control that you created in step 1. Additionally, create another action call to on the **Contoso Global Manager** hosted control to display the hosted control created in step 1 in the agent application.  

    In the **Actions** area, click **+** on the right corner to add an action call.  

5. In the search box in the **Actions** area, press ENTER or click the search icon.  

6. In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.  

   ![Choose New to create an action call](../unified-service-desk/media/crm-itpro-usd-wt02-04.png "Choose New to create an action call")  

7. On the **New Action Call** page, specify the following values:  


   |     Trường      |                        Giá trị                        |
   |----------------|-----------------------------------------------------|
   |      Tên      |          Cuộc gọi hành động Contoso: Hiển thị trợ giúp          |
   |     Thứ tự      |                          1                          |
   | Kiểm soát được lưu trữ |                    Contoso trợ giúp                     |
   |     Hành động     |                      Navigate                       |
   |      Dữ liệu      | url=<http://go.microsoft.com/fwlink/?LinkID=856273> |

   ![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-05.png "Create an action call in Unified Service Desk")  

8. Bấm vào **Lưu**. The new action call is added to the **Contoso Show Help** button.  

9. Add another action call to the button to set the focus on the hosted control that displays the webpage in the client application. In the **Actions** area, click **+** in the right corner to add an action call.  

10. In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.  

11. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.  

    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Cuộc gọi hành động Contoso: Hiển thị kiểm soát tổ chức trợ giúp|  
    |Đơn hàng|2|  
    |Kiểm soát được lưu trữ|Contoso Global Manager|  
    |Hành động|Hiển thị tab|  
    |Dữ liệu|Contoso trợ giúp|  

    ![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-06.png "Create an action call in Unified Service Desk")  

12. Bấm vào **Lưu**. The new action call gets added to the **Contoso Show Help** button. You can see both action calls added to the toolbar button.  

    ![Action calls added to the toolbar button](../unified-service-desk/media/crm-itpro-usd-wt02-07.png "Action calls added to the toolbar button")  

<a name="Step5"></a>   
## <a name="step-5-add-the-controls-to-the-configuration"></a>Step 5: Add the controls to the configuration  
 In this step, add the action calls, hosted controls, and toolbar that you created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration. **Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).  

 Add the following to **Contoso Configuration**.  

|Tên kiểm soát|Loại kiểm soát|  
|------------------|------------------|  
|Cuộc gọi hành động Contoso: Hiển thị trợ giúp|Cuộc gọi hành động|  
|Cuộc gọi hành động Contoso: Hiển thị kiểm soát tổ chức trợ giúp|Cuộc gọi hành động|  
|Contoso trợ giúp|Kiểm soát tổ chức|  
|Contoso về Bộ chứa thanh công cụ|Kiểm soát tổ chức|  
|Contoso About Toolbar|Thanh công cụ|  

 To add a control to the configuration:  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. Trên thanh điều hướng, nhấp vào **Microsoft Dynamics 365 for Customer Engagement**, và sau đó chọn **Cài đặt**.  

3. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

4. Bấm **Cấu hình**.  

5. Bấm vào **Cấu hình Contoso** để mở định nghĩa.  

6. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.  

7. Trên trang tiếp theo, bấm vào **Thêm Cuộc gọi Hành động Hiện có**, nhập “`Contoso Action Call`” vào thanh tìm kiếm, sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.  

8. Cả cuộc gọi hành động được hiển thị trong kết quả tìm kiếm. Thêm cả hai người trong số chúng.  

9. Tương tự, thêm cả hai kiểm soát tổ chức và thanh công cụ bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Kiểm soát tổ chức** và **thanh công cụ** lần lượt.  

10. Bấm vào **Lưu**.  

<a name="Step6"></a>   
## <a name="step-6-test-the-application"></a>Step 6: Test the application  
 Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md). For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)  

 Your agent application will now have a **Show Help** button at the top-right corner:  

 ![Show Help button in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-08.png "Show Help button in Unified Service Desk")  

 Clicking **Show Help** displays the specified web URL within the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application.  

 ![Help displayed in the client application](../unified-service-desk/media/crm-itpro-usd-wt02-09.png "Help displayed in the client application")  

<a name="Conclusion"></a>   
## <a name="conclusion"></a>Kết luận  
 In this walkthrough, you learned how to display a webpage in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application. You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.  

### <a name="see-also"></a>Xem thêm  
 [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)   
 [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md)   
 [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md)   
 [Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md)   
 [Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md)   
 [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md)   
 [Walkthrough 8: Use Parature knowledge within your agent application](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md)   
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)  
