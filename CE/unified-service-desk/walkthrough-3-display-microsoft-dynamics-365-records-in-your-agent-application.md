---
title: 'Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application | MicrosoftDocs'
description: Demonstrates how to display Customer Engagement records in Unified Service Desk.
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
ms.assetid: 0affe8ba-fddc-4ded-b733-735833209b53
caps.latest.revision: 8
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: f1004646ac10778a280d9c8359bc99d16159be98
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385996"
---
# <a name="walkthrough-3-display-microsoft-dynamics-365-for-customer-engagement-apps-records-in-your-agent-application"></a>Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application
This walkthrough demonstrates how to display [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps records in your agent application. In this walkthrough, you’ll display all the account and contact records in the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance. Bạn cũng sẽ tạo ra nút tìm kiếm với các mục trình đơn thả xuống để hiển thị tài khoản và địa chỉ liên lạc trong ứng dụng tổng đài viên.  

## <a name="prerequisites"></a>Điều kiện tiên quyết  

- You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md). Các cấu hình mà bạn hoàn thành trong cách 1 được yêu cầu trong cách này.  

- Cách này giả định rằng bạn sẽ đang sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên ở cuối cách này để kiểm tra ứng dụng. If a different user will be testing the application, you must assign the user to **Contoso Configuration**. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)  

- You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  

  - Hai loại kiểm soát tổ chức sau: Trang CRM và bộ chứa thanh công cụ. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)  

  - Action call and how to configure it. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Action calls](../unified-service-desk/action-calls.md)  

  - Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)  

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a>In This Walkthrough  
 [Bước 1: Tạo loại trang CRM của kiểm soát tổ chức để hiển thị hồ sơ tài khoản và liên hệ](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step1)  

 [Bước 2: Tạo loại bộ chứa công cụ của kiểm soát tổ chức](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step2)  

 [Bước 3: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step3)  

 [Step 4: Add toolbar buttons and action calls to display Dynamics 365 for Customer Engagement apps records](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step4)  

 [Bước 5: Thêm kiểm soát vào cấu hình](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step5)  

 [Bước 6: Kiểm tra ứng dụng](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step6)  

 [Kết luận](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md#Conclusion)  

<a name="Step1"></a>   
## <a name="step-1-create-crm-page-type-of-hosted-controls-to-display-account-and-contact-records"></a>Bước 1: Tạo loại trang CRM của kiểm soát tổ chức để hiển thị hồ sơ tài khoản và liên hệ  
 In this step, you’ll create two hosted controls of **[!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps Page** type to display the account and contact records respectively.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Click **Hosted Controls**.  

4. Bấm vào **Mới**.  

5. On the **New Hosted Control** page, specify the following values:  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Tìm kiếm tài khoản Contoso|  
   |Tên hiển thị|Contoso: Tài khoản|  
   |Loại Thành phần USD|Trang CRM|  
   |Cho phép nhiều trang|No|  
   |Loại tổ chức|WPF nội bộ|  
   |Application is Global|Đã kiểm tra|  
   |Nhóm hiển thị|Bảng điều khiển chính|  

   ![Create a hosted control for displaying accounts](../unified-service-desk/media/crm-itpro-usd-wt03-01.png "Create a hosted control for displaying accounts")  

6. Bấm vào **Lưu**.  

7. Bấm vào **Mới** để tạo ra kiểm soát tổ chức khác để hiển thị hồ sơ liên lạc.  

8. Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau:  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Tìm kiếm liên hệ Contoso|  
   |Tên hiển thị|Contoso: Liên hệ|  
   |Loại Thành phần USD|Trang CRM|  
   |Cho phép nhiều trang|No|  
   |Loại tổ chức|WPF nội bộ|  
   |Application is Global|Đã kiểm tra|  
   |Nhóm hiển thị|Bảng điều khiển chính|  

   ![Create hosted control for displaying contacts](../unified-service-desk/media/crm-itpro-usd-wt03-02.png "Create hosted control for displaying contacts")  

9. Bấm vào **Lưu**.  

<a name="Step2"></a>   
## <a name="step-2-create-a-toolbar-container-type-of-hosted-control"></a>Bước 2: Tạo loại bộ chứa công cụ của kiểm soát tổ chức  
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

   ![Toolbar Container hosted control](../unified-service-desk/media/crm-itpro-usd-wt03-03.png "Toolbar Container hosted control")  

6. Bấm vào **Lưu**.  

<a name="Step3"></a>   
## <a name="step-3-add-a-toolbar-and-attach-it-to-the-toolbar-container"></a>Bước 3: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ  
 In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 2. This is done to display the toolbar in your agent application.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Bấm vào **Thanh công cụ**.  

4. Bấm vào **Mới**.  

5. Trên trang **thanh công cụ mới**, nhập **Thanh công cụ chính Contoso** trong hộp **tên**, sau đó nhấp vào **Lưu**.  

6. Attach the toolbar to the toolbar container hosted control created in step 2. On the nav bar, click the down arrow next to **Contoso Main Toolbar**, and click **Hosted Controls**.  

7. Trên trang tiếp theo, bấm vào **Thêm kiểm soát tổ chức hiện có**, nhập `Contoso Main Toolbar Container` trong thanh tìm kiếm và sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.  

8. Từ kết quả tìm kiếm, hãy nhấp vào **Bộ chứa thanh công cụ chính Contoso** để thêm.  

9. Bấm vào **Lưu**.  

<a name="Step4"></a>   
## <a name="step-4-add-toolbar-buttons-and-action-calls-to-display-dynamics-365-for-customer-engagement-apps-records"></a>Step 4: Add toolbar buttons and action calls to display Dynamics 365 for Customer Engagement apps records  
 In this step, you’ll add buttons on the toolbar and attach action calls to the buttons so that when the button is clicked, appropriate [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records are displayed in the hosted controls that were created in step 1. You’ll configure the search button so that clicking the button displays the account and contact submenu items, and clicking a button displays the respective [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records.  

1. Sau khi bạn lưu thanh công cụ trong bước 3, vùng **nút** sẽ có sẵn. In the **Buttons** area, click **+** on the right corner to add a button.  

2. On the **New Toolbar Button** page, specify the following values:  


   |    Trường    |                                          Giá trị                                           |
   |-------------|------------------------------------------------------------------------------------------|
   |    Tên     |                                  Nút tìm kiếm Contoso                                   |
   | Văn bản nút |                                          TÌM KIẾM                                          |
   |   Chú giải công cụ   | Search [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps accounts and contacts |
   |    Thứ tự    |                                            1                                             |

   ![Create the Search toolbar button](../unified-service-desk/media/crm-itpro-usd-wt03-04.png "Create the Search toolbar button")  

3. Bấm vào **Lưu**.  

4. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh Nút Tìm kiếm và bấm vào Nút trên thanh công cụ.  

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

8. Bây giờ bạn sẽ thêm hai cuộc gọi hành động: cuộc gọi đầu tiên là để hiển thị các hồ sơ tài khoản trong kiểm soát tổ chức đã tạo ở bước 1 và cuộc gọi thứ hai trên kiếm soát tổ chức trình quản lý chung Contoso để hiển thị kiểm soát tổ chức tài khoản.  

    In the **Actions** area, click **+** on the right corner to add an action call.  

9. Trong hộp tìm kiếm trong vùng **hành động**, nhấn ENTER hoặc nhấp biểu tượng tìm kiếm.  

10. In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.  

    ![Choose New to create an action call](../unified-service-desk/media/crm-itpro-usd-wt03-06.png "Choose New to create an action call")  

11. On the **New Action Call** page, specify the following values:  

    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Các cuộc gọi hành động contoso: Tìm tài khoản|  
    |Đơn hàng|1|  
    |Kiểm soát được lưu trữ|Tìm kiếm tài khoản Contoso|  
    |Hành động|Find|  
    |Dữ liệu|tài khoản|  

    ![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-07.png "Create an action call in Unified Service Desk")  

12. Bấm vào **Lưu**. Cuộc gọi hành động mới được thêm vào nút **Nút tài khoản tìm kiếm Contoso**.  

13. Bạn sẽ thêm một cuộc gọi hành động vào nút để đặt trọng tâm trên kiểm soát tổ chức mà hiển thị các hồ sơ tài khoản trong ứng dụng khách. In the **Actions** area, click **+** on the right corner to add an action call.  

14. In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.  

15. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.  

    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Cuộc gọi hành động contoso: Hiển thị tìm kiếm tài khoản|  
    |Đơn hàng|2|  
    |Kiểm soát tổ chức|Trình quản lý chung contoso|  
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

21. Bây giờ bạn sẽ thêm hai cuộc gọi hành động: cuộc gọi đầu tiên là để hiển thị các hồ sơ liên hệ trong kiểm soát tổ chức đã tạo ở bước 1 và cuộc gọi thứ hai trên kiếm soát tổ chức trình quản lý chung Contoso để hiển thị kiểm soát tổ chức liên hệ.  

     In the **Actions** area, click **+** on the right corner to add an action call.  

22. In the search box in the **Actions** area, press ENTER or click the search icon.  

23. Trong hộp tìm kiếm kết quả, bấm vào **Mới** ở góc dưới bên phải để tạo ra cuộc gọi hành động cho nút thanh công cụ này.  

24. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:  

    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Các cuộc gọi hành động contoso: Tìm liên hệ|  
    |Đơn hàng|1|  
    |Kiểm soát được lưu trữ|Tìm kiếm liên hệ Contoso|  
    |Hành động|Find|  
    |Dữ liệu|người liên hệ|  

    ![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-10.png "Create an action call in Unified Service Desk")  

25. Bấm vào **Lưu**. Cuộc gọi hành động mới được thêm vào nút thanh công cụ **Nút liên hệ tìm kiếm Contoso**.  

26. Bạn sẽ thêm một cuộc gọi hành động vào nút để đặt trọng tâm trên kiểm soát tổ chức mà hiển thị các hồ sơ liên hệ trong ứng dụng khách. In the **Actions** area, click **+** on the right corner to add an action call.  

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
 Trong bước này, bạn sẽ thêm cuộc gọi hành động, kiểm soát tổ chức và thanh công cụ đã tạo trong cách này vào **Cấu hình Contoso** để hiển thị các kiểm soát này cho người dùng được chỉ định cho cấu hình này. **Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).  

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
|Thanh công cụ chính Contoso|Thanh công cụ|  

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
## <a name="step-6-test-the-application"></a>Bước 6: Kiểm tra ứng dụng  
 Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md). For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).  

 Ứng dụng tổng đài viên của bạn bây giờ sẽ có nút **TÌM KIẾM** trong vùng thanh công cụ có hai nút phụ (**tài khoản** và **liên hệ**) mà được hiển thị khi nhấn vào mũi tên xuống.  

 ![Display account and contact records](../unified-service-desk/media/crm-itpro-usd-wt03-12.png "Display account and contact records")  

 Click **Account** or **Contact** under the **SEARCH** button to display the respective records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance in separate tabs in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.  

 ![Dynamics 365 for Customer Engagement apps contact records displayed](../unified-service-desk/media/crm-itpro-usd-wt03-13.png "Dynamics 365 for Customer Engagement apps contact records displayed")  

<a name="Conclusion"></a>   
## <a name="conclusion"></a>Kết luận  
 In this walkthrough, you learned how to display [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application. You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.  

### <a name="see-also"></a>Xem thêm  
 [Cách 1: Xây dựng ứng dụng tổng đài viên đơn giản](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)   
 [Cách 2: Hiển thị trang web bên ngoài trong ứng dụng tổng đài viên của bạn](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md)   
 [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md)   
 [Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md)   
 [Hướng 6: Đặt cấu hình kiểm soát tổ chức trình gỡ lỗi trong ứng dụng tổng đài viên của bạn](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md)   
 [Cách 7: Đặt cấu hình mã lệnh tổng đài viên trong ứng dụng tổng đài viên của bạn](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md)   
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
