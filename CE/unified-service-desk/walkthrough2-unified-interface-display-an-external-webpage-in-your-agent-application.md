---
title: 'Walkthrough 2: Display an external webpage in your agent application | MicrosoftDocs'
description: Demonstrates how to display an external web page in Unified Service Desk.
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
ms.assetid: C616E47C-E7D4-4195-8F53-1139F7514BFA
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
ms.openlocfilehash: f372c1f929775229a7f33ae55818f163745c91bf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386864"
---
# <a name="walkthrough-2-display-an-external-webpage-in-your-agent-application"></a>Walkthrough 2: Display an external webpage in your agent application
Cách này mô tả cách hiển thị trang web hoặc URL bên ngoài trong ứng dụng tổng đài viên của bạn. In this walkthrough, you’ll learn how to display the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] Guide, which is available online at http://go.microsoft.com/fwlink/?LinkID=856273, in the client application.

## <a name="prerequisites"></a>Điều kiện tiên quyết  

- You must have completed [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md). Các cấu hình mà bạn hoàn thành trong cách đầu tiên được yêu cầu trong cách này.  

- Cách này giả định rằng bạn sẽ sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng ở cuối cách 1 để đăng nhập vào ứng dụng tổng đài viên. If a different user will be testing the application, you must assign the user to **Contoso Configuration**. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)  

- Bạn phải làm quen với các khái niệm sau trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  

  - Hai loại kiểm soát tổ chức: Ứng dụng web tiêu chuẩn và bộ chứa thanh công cụ. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)  

  - How to configure [Action calls](../unified-service-desk/action-calls.md)  

  - Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)  

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a>In This Walkthrough  
 [Bước 1: Tạo kiểm soát tổ chức để hiển thị trang web](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md#Step1)  

 [Bước 2: Tạo loại bộ chứa công cụ của kiểm soát tổ chức](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md#Step2)  

 [Bước 3: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md#Step3)  

 [Bước 4: Thêm nút thanh công cụ và các cuộc gọi hành động để hiển thị trang web](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md#Step4)  

 [Bước 5: Thêm kiểm soát vào cấu hình](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md#Step5)  

 [Bước 6: Kiểm tra ứng dụng](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md#Step6)  

 [Kết luận](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md#Conclusion)  

<a name="Step1"></a>   
## <a name="step-1-create-a-hosted-control-to-display-the-webpage"></a>Bước 1: Tạo kiểm soát tổ chức để hiển thị trang web  
 Trong bước này, bạn sẽ tạo ra kiểm soát tổ chúc của loại ứng dụng web tiêu chuẩn để hiển thị trang web.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Click **Hosted Controls**.  

4. Bấm vào **Mới**.  

5. On the **New Hosted Control** page, specify the following values:  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Contoso trợ giúp|  
   |Tên hiển thị|Contoso trợ giúp|  
   |Loại Thành phần USD|Standard Web Application|  
   |Allow Multiple Pages|Không|  
   |Loại lưu trữ|IE Process|

   ![Standard Web Application hosted control](../unified-service-desk/media/crm-itpro-usd-wt02-01-unified-interface.png "Standard Web Application hosted control") 

6. Bấm vào **Lưu**.  

<a name="Step2"></a>   
## <a name="step-2-create-a-toolbar-container-type-of-hosted-control"></a>Step 2: Create a toolbar container type of hosted control  
 Kiểm soát tổ chức bộ chứa thanh công cụ được sử dụng để giữ và hiển thị thanh công cụ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Trong phần này, bạn sẽ tạo loại **Bộ chứa thanh công cụ** của kiểm soát tổ chức mà sẽ xuất hiện trong vùng thanh công cụ của ứng dụng khách.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Click **Hosted Controls**.  

4. Bấm vào **Mới**.  

5. On the **New Hosted Control** page, specify the following values:  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Contoso về Bộ chứa thanh công cụ|  
   |USD Component Type|Bộ chứa thanh công cụ|  
   |Nhóm hiển thị|Bàng điều khiển thanh công cụ|

   ![Toolbar Container hosted control](../unified-service-desk/media/crm-itpro-usd-wt02-02-unified-interface.png "Toolbar Container hosted control") 

6. Bấm vào **Lưu**.  

<a name="Step3"></a>   
## <a name="step-3-add-a-toolbar-and-attach-it-to-the-toolbar-container"></a>Step 3: Add a toolbar and attach it to the toolbar container  
 In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 2. This is done to display the toolbar in your agent application.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Bấm vào **Thanh công cụ**.  

4. Bấm vào **Mới**.  

5. Trên trang **thanh công cụ mới**, nhập **Contoso về Thanh công cụ** trong hộp **tên**, sau đó nhấp vào **Lưu**.  

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
   |Tên|Contoso Hiển thị trợ giúp|  
   |Văn bản nút|Hiển thị trợ giúp|  

   ![Create a new toolbar button](../unified-service-desk/media/crm-itpro-usd-wt02-03.png "Create a new toolbar button")  

3. Bấm vào **Lưu** để lưu hồ sơ và bật vùng **Hoạt động**.  

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

   ![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-05-unified-interface.png "Create an action call in Unified Service Desk")  

8. Bấm vào **Lưu**. Cuộc gọi hành động mới được thêm vào nút **Contoso Hiển thị Trợ giúp**.  

9. Thêm một cuộc gọi hành động vào nút để đặt trọng tâm trên kiểm soát tổ chức mà hiển thị trang web trong ứng dụng khách. In the **Actions** area, click **+** in the right corner to add an action call.  

10. In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.  

11. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.  

    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Cuộc gọi hành động Contoso: Hiển thị kiểm soát tổ chức trợ giúp|  
    |Đơn hàng|2|  
    |Kiểm soát được lưu trữ|Contoso Global Manager|  
    |Hành động|Hiển thị tab|  
    |Dữ liệu|Contoso trợ giúp|  

    ![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-06-unified-interface.png "Create an action call in Unified Service Desk")  

12. Bấm vào **Lưu**. Cuộc gọi hành động mới được thêm vào nút **Contoso Hiển thị Trợ giúp**. Bạn có thể nhìn thấy cả hai cuộc gọi hành động thêm vào nút thanh công cụ.  

    ![Action calls added to the toolbar button](../unified-service-desk/media/crm-itpro-usd-wt02-07.png "Action calls added to the toolbar button")  

<a name="Step5"></a>   
## <a name="step-5-add-the-controls-to-the-configuration"></a>Step 5: Add the controls to the configuration  
 Trong bước này, bạn sẽ thêm cuộc gọi hành động, kiểm soát tổ chức và thanh công cụ đã tạo trong cách này vào **Cấu hình Contoso** để hiển thị các kiểm soát này cho người dùng được chỉ định cho cấu hình này. **Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).  

 Add the following to **Contoso Configuration**.  

|Tên kiểm soát|Loại kiểm soát|  
|------------------|------------------|  
|Cuộc gọi hành động Contoso: Hiển thị trợ giúp|Cuộc gọi hành động|  
|Cuộc gọi hành động Contoso: Hiển thị kiểm soát tổ chức trợ giúp|Cuộc gọi hành động|  
|Contoso trợ giúp|Kiểm soát tổ chức|  
|Contoso về Bộ chứa thanh công cụ|Kiểm soát tổ chức|  
|Contoso về thanh công cụ|Thanh công cụ|  

 To add a control to the configuration:  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. On the nav bar, click **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.  

3. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

4. Bấm **Cấu hình**.  

5. Click **Contoso Configuration** to open the definition.  

6. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.  

7. Trên trang tiếp theo, bấm vào **Thêm Cuộc gọi Hành động Hiện có**, nhập “`Contoso Action Call`” vào thanh tìm kiếm, sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.  

8. Cả cuộc gọi hành động được hiển thị trong kết quả tìm kiếm. Thêm cả hai người trong số chúng.  

9. Tương tự, thêm cả hai kiểm soát tổ chức và thanh công cụ bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Kiểm soát tổ chức** và **thanh công cụ** lần lượt.  

10. Bấm vào **Lưu**.  

<a name="Step6"></a>   
## <a name="step-6-test-the-application"></a>Step 6: Test the application  
 Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md). For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md) 

 Ứng dụng đại lý của bạn bây giờ sẽ có nút **Hiển thị trợ giúp** ở góc trên bên phải:  

 ![Show Help button in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-08.png "Show Help button in Unified Service Desk")  

 Nhấn vào **Hiển thị trợ giúp** Hiển thị URL web đã chỉ định trong ứng dụng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  

 ![Help displayed in the client application](../unified-service-desk/media/crm-itpro-usd-wt02-09.png "Help displayed in the client application")  

<a name="Conclusion"></a>   
## <a name="conclusion"></a>Kết luận  
 Trong cách này, bạn học cách hiển thị trang web [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] trong ứng dụng khách. You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.  

### <a name="see-also"></a>Xem thêm
 [Support for Unified Interface Apps in Unified Service Desk](../unified-service-desk/admin/Support-unified-interfaces-apps-usd.md)

 [Unified Interface Page (Hosted Control)](../unified-service-desk/unified-interface-page-hosted-control.md)

 [Unified Service Desk and Unified Interface Configuration Walkthroughs](../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md)

 [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)

 [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)

 [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md)

 [Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md)

 [Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md)

 [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)
