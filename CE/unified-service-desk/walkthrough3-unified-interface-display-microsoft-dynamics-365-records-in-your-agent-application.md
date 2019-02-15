---
title: 'Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records of Unified Interface app in your agent application | MicrosoftDocs'
description: Demonstrates how to display Unified Interface apps records in Unified Service Desk.
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
ms.assetid: FD393D95-FBB9-434B-86B1-23747FBB5B70
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
ms.openlocfilehash: 69cba200c28ce9b840260016cb99d75728671ad2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386286"
---
# <a name="walkthrough-3-display-microsoft-dynamics-365-for-customer-engagement-apps-unified-interface-apps-records-in-your-agent-application"></a>Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application
This walkthrough demonstrates how to display [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps records of Unified Interface Apps in your agent application. In this walkthrough, you’ll display all the account and contact records in the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance. You’ll also create a search button with drop-down menu items for displaying accounts and contacts in the agent application.  

## <a name="prerequisites"></a>Điều kiện tiên quyết  

- You must have completed [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md). The configurations that you completed in walkthrough 1 are required in this walkthrough.  

- Cách này giả định rằng bạn sẽ đang sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên ở cuối cách này để kiểm tra ứng dụng. If a different user will be testing the application, you must assign the user to **Contoso Configuration**. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)  

- You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  

  - The following two types of hosted controls: Unified Interface Page and Toolbar Container. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)  

  - Action call and how to configure it. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Action calls](../unified-service-desk/action-calls.md)  

  - Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)  

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a>In This Walkthrough  
 [Step 1: Create Unified Interface Page type of hosted controls to display account and contact records](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step1)  

 [Bước 2: Tạo loại bộ chứa công cụ của kiểm soát tổ chức](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step2)  

 [Bước 3: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step3)  

 [Step 4: Add toolbar buttons and action calls to display Dynamics 365 for Customer Engagement apps records](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step4)  

 [Bước 5: Thêm kiểm soát vào cấu hình](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step5)  

 [Bước 6: Kiểm tra ứng dụng](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step6)  

 [Kết luận](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md#Conclusion)

<a name="Step1"></a>   
## <a name="step-1-create-unified-interface-page-type-of-hosted-controls-to-display-account-and-contact-records"></a>Step 1: Create Unified Interface Page type of hosted controls to display account and contact records  
 In this step, you’ll create two hosted controls of **Unified Interface Page** type to display the account and contact records respectively.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Click **Hosted Controls**.  

4. Bấm vào **Mới**.  

5. On the **New Hosted Control** page, specify the following values:  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Contoso Accounts Search|  
   |Tên Hiển thị|Contoso: Tài khoản|  
   |USD Component Type|Unified Interface Page|  
   |Allow Multiple Pages|Không|
   |Pre-Fetch Data|Đã kiểm tra|
   |Application is Global|Đã kiểm tra|  
   |Nhóm hiển thị|Bảng điều khiển chính|  

   ![Create a hosted control for displaying accounts](../unified-service-desk/media/crm-itpro-usd-wt03-01-unified-interface.png "Create a hosted control for displaying accounts")  

6. Bấm vào **Lưu**.  

7. Click **New** to create another hosted control for displaying contact records.  

8. Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau:  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Contoso Contacts Search|  
   |Tên Hiển thị|Contoso: Liên hệ|  
   |USD Component Type|Unified Interface Page|  
   |Allow Multiple Pages|Không|
   |Pre-Fetch Data|Đã kiểm tra|
   |Application is Global|Đã kiểm tra|  
   |Nhóm hiển thị|Bảng điều khiển chính|  

   ![Create hosted control for displaying contacts](../unified-service-desk/media/crm-itpro-usd-wt03-02-unified-interface.png "Create hosted control for displaying contacts")  

9. Bấm vào **Lưu**.  

<a name="Step2"></a>   
## <a name="step-2-create-a-toolbar-container-type-of-hosted-control"></a>Step 2: Create a toolbar container type of hosted control  
 Loại bộ chứa thanh công cụ của kiểm soát tổ chức được sử dụng để giữ và hiển thị thanh công cụ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. In this section, you’ll create a **Toolbar Container** hosted control that will appear at the top of the client application.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Click **Hosted Controls**.  

4. Bấm vào **Mới**.  

5. On the **New Hosted Control** page, specify the following values  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Bộ chứa thanh công cụ chính Contoso|  
   |USD Component Type|Bộ chứa thanh công cụ|  
   |Nhóm hiển thị|Bàng điều khiển thanh công cụ|  

   ![Toolbar Container hosted control](../unified-service-desk/media/crm-itpro-usd-wt03-03-unified-interface.png "Toolbar Container hosted control")

6. Bấm vào **Lưu**.  

<a name="Step3"></a>   
## <a name="step-3-add-a-toolbar-and-attach-it-to-the-toolbar-container"></a>Step 3: Add a toolbar and attach it to the toolbar container  
 In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 2. This is done to display the toolbar in your agent application.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Bấm vào **Thanh công cụ**.  

4. Bấm vào **Mới**.  

5. On the **New Toolbar** page, type **Contoso Main Toolbar** in the **Name** box, and then click **Save**.  

6. Attach the toolbar to the toolbar container hosted control created in step 2. On the nav bar, click the down arrow next to **Contoso Main Toolbar**, and click **Hosted Controls**.  

7. Trên trang tiếp theo, bấm vào **Thêm kiểm soát tổ chức hiện có**, nhập `Contoso Main Toolbar Container` trong thanh tìm kiếm và sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.  

8. Từ kết quả tìm kiếm, hãy nhấp vào **Bộ chứa thanh công cụ chính Contoso** để thêm.  

9. Bấm vào **Lưu**.  

<a name="Step4"></a>   
## <a name="step-4-add-toolbar-buttons-and-action-calls-to-display-dynamics-365-for-customer-engagement-apps-records--from-unified-interface-apps"></a>Step 4: Add toolbar buttons and action calls to display Dynamics 365 for Customer Engagement apps records  from Unified Interface Apps
 In this step, you’ll add buttons on the toolbar and attach action calls to the buttons so that when the button is clicked, appropriate [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records are displayed in the hosted controls that were created in step 1. You’ll configure the search button so that clicking the button displays the account and contact submenu items, and clicking a button displays the respective [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records.  

1. After you save the toolbar in step 3, the **Buttons** area becomes available. In the **Buttons** area, click **+** on the right corner to add a button.  

2. On the **New Toolbar Button** page, specify the following values:  


   |    Trường    |                                          Giá trị                                           |
   |-------------|------------------------------------------------------------------------------------------|
   |    Tên     |                                  Contoso Search Button                                   |
   | Văn bản nút |                                          TÌM KIẾM                                          |
   |   Chú giải công cụ   | Search [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps accounts and contacts |
   |    Thứ tự    |                                            1                                             |

   ![Create the Search toolbar button](../unified-service-desk/media/crm-itpro-usd-wt03-04.png "Create the Search toolbar button")

3. Bấm vào **Lưu**.

4. On the nav bar, click the down arrow next to Contoso Search Button, and click Toolbar Buttons.

   > [!NOTE]
   >  Bạn hiện đang thêm nút thanh công cụ phụ vào nút thanh công cụ hiện có để tạo cấu trúc menu phụ.

5. Trên trang tiếp theo, bấm vào **thêm nút thanh công cụ mới**.

6. Trên trang **Nút thanh công cụ mới**, chỉ định các giá trị sau.

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Nút tài khoản tìm kiếm Contoso|  
   |Văn bản nút|Tài khoản|  
   |Đơn hàng|1<br /><br /> Trường **Thứ tự** xác định vị trí của nút trên thanh công cụ. Buttons are arranged from left to right or top to bottom in an ascending order.|  

   ![Create a tooolbar button for Account submenu](../unified-service-desk/media/crm-itpro-usd-wt03-05.png "Create a tooolbar button for Account submenu")  

7. Bấm vào **Lưu**.  

8. You’ll now add two action calls: first to display the account records in the hosted control created in step 1 and the second one on the Contoso Global Manager hosted control to display the account hosted control.  

    In the **Actions** area, click **+** on the right corner to add an action call.  

9. In the search box in the **Actions** area, press ENTER or click the search icon.  

10. In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.  

    ![Choose New to create an action call](../unified-service-desk/media/crm-itpro-usd-wt03-06.png "Choose New to create an action call")  

11. On the **New Action Call** page, specify the following values:  

    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Các cuộc gọi hành động contoso: Tìm tài khoản|  
    |Đơn hàng|1|  
    |Kiểm soát được lưu trữ|Contoso Accounts Search|  
    |Hành động|Find|  
    |Dữ liệu|tài khoản|  

    ![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-07.png "Create an action call in Unified Service Desk")  

12. Bấm vào **Lưu**. The new action call gets added to the **Contoso Search Account Button** button.  

13. You’ll add another action call to the button to set the focus on the hosted control that displays the account records in the client application. In the **Actions** area, click **+** on the right corner to add an action call.  

14. In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.  

15. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.  

    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Cuộc gọi hành động contoso: Hiển thị tìm kiếm tài khoản|  
    |Đơn hàng|2|  
    |Kiểm soát tổ chức|Contoso Global Manager|  
    |Hành động|Hiển thị tab|  
    |Dữ liệu|Contoso Accounts Search|  

    ![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-08.png "Create an action call in Unified Service Desk")  

16. Bấm vào **Lưu**. The new action call gets added to the **Contoso Search Account Button** button.  

17. Điều hướng đến nút thanh công cụ **Nút tìm kiếm Contoso** để thêm nút phụ để tìm kiếm và hiển thị liên hệ. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Nút tìm kiếm Contoso** và chọn **Nút thanh công cụ**.  

18. Trên trang tiếp theo, bấm vào **thêm nút thanh công cụ mới**.  

19. Trên trang **Nút thanh công cụ mới**, chỉ định các giá trị sau:  

    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Nút Liên hệ tìm kiếm Contoso|  
    |Văn bản nút|Người liên hệ|  
    |Đơn hàng|2<br /><br /> Trường **Thứ tự** xác định vị trí của nút trên thanh công cụ. Buttons are arranged from left to right or top to bottom in an ascending order.|  

    ![Create a toolbar button for contacts search](../unified-service-desk/media/crm-itpro-usd-wt03-09.png "Create a toolbar button for contacts search")  

20. Bấm vào **Lưu**.  

21. You’ll now add two action calls: first to display the contact records in the hosted control that were created in step 1 and the second one on the Contoso Global Manager hosted control to display the contacts hosted control.  

     In the **Actions** area, click **+** on the right corner to add an action call.  

22. In the search box in the **Actions** area, press ENTER or click the search icon.  

23. Trong hộp tìm kiếm kết quả, bấm vào **Mới** ở góc dưới bên phải để tạo ra cuộc gọi hành động cho nút thanh công cụ này.  

24. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:  

    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Các cuộc gọi hành động contoso: Tìm liên hệ|  
    |Đơn hàng|1|  
    |Kiểm soát được lưu trữ|Contoso Contacts Search|  
    |Hành động|Find|  
    |Dữ liệu|người liên hệ|  

    ![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-10.png "Create an action call in Unified Service Desk")  

25. Bấm vào **Lưu**. The new action call gets added to the **Contoso Search Contact Button** toolbar button.  

26. You’ll add another action call to the button to set the focus on the hosted control that displays the contact records in the client application. In the **Actions** area, click **+** on the right corner to add an action call.  

27. In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.  

28. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.  

    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Cuộc gọi hành động contoso: Hiển thị tìm kiếm liên hệ|  
    |Đơn hàng|2|  
    |Kiểm soát tổ chức|Contoso Global Manager|  
    |Hành động|Hiển thị tab|  
    |Dữ liệu|Contoso Contacts Search|  

    ![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-11.png "Create an action call in Unified Service Desk")  

29. Bấm vào **Lưu**. The new action call gets added to the **Contoso Search Contact Button** toolbar button.  

<a name="Step5"></a>   
## <a name="step-5-add-the-controls-to-the-configuration"></a>Bước 5: Thêm kiểm soát vào cấu hình  
 In this step, you’ll add the action calls, hosted controls, and toolbar that were created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration. **Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).  

 Add the following to **Contoso Configuration**.  

|Tên kiểm soát|Loại kiểm soát|  
|------------------|------------------|  
|Các cuộc gọi hành động contoso: Tìm tài khoản|Cuộc gọi hành động|  
|Cuộc gọi hành động contoso: Hiển thị tìm kiếm tài khoản|Cuộc gọi hành động|  
|Các cuộc gọi hành động contoso: Tìm liên hệ|Cuộc gọi hành động|  
|Cuộc gọi hành động contoso: Hiển thị tìm kiếm liên hệ|Cuộc gọi hành động|  
|Tìm kiếm tài khoản Contoso|Kiểm soát tổ chức|  
|Tìm kiếm liên hệ Contoso|Kiểm soát tổ chức|  
|Bộ chứa thanh công cụ chính Contoso|Kiểm soát tổ chức|  
|Contoso Main Toolbar|Thanh công cụ|  

 To add a control to the configuration:  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Bấm **Cấu hình**.  

4. Click **Contoso Configuration** to open the definition.  

5. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.  

6. Trên trang tiếp theo, bấm vào **Thêm Cuộc gọi Hành động Hiện có**, nhập “`Contoso Action Call`” vào thanh tìm kiếm, sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.  

7. Các cuộc gọi hành động được liệt kê trước đó được hiển thị trong kết quả tìm kiếm. Thêm các cuộc gọi hành động này.  

8. Tương tự, thêm kiểm soát tổ chức và thanh công cụ bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Kiểm soát tổ chức** và **thanh công cụ** lần lượt.  

9. Bấm vào **Lưu**.  

<a name="Step6"></a>   
## <a name="step-6-test-the-application"></a>Step 6: Test the application  
 Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md). For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).  

 Your agent application will now have a **SEARCH** button in the toolbar area with two child buttons (**Account** and **Contact**) that are displayed on clicking the down arrow.  

 ![Display account and contact records](../unified-service-desk/media/crm-itpro-usd-wt03-12.png "Display account and contact records")  

 Click **Account** or **Contact** under the **SEARCH** button to display the respective records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance in separate tabs in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.  

 ![Dynamics 365 for Customer Engagement apps contact records displayed](../unified-service-desk/media/crm-itpro-usd-wt03-13-unified-interface.png "Dynamics 365 for Customer Engagement apps contact records displayed")  

<a name="Conclusion"></a>   
## <a name="conclusion"></a>Kết luận  
 In this walkthrough, you learned how to display [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records from Unified Interface Apps in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application. You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.

### <a name="see-also"></a>Xem thêm
 [Support for Unified Interface Apps in Unified Service Desk](../unified-service-desk/admin/Support-unified-interfaces-apps-usd.md)

 [Unified Interface Page (Hosted Control)](../unified-service-desk/unified-interface-page-hosted-control.md)

 [Unified Service Desk and Unified Interface Configuration Walkthroughs](../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md)

 [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)   

 [Walkthrough 2: Display an external webpage in your agent application](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md)
 
 [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md)   

 [Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md) 

 [Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md)

 [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)
