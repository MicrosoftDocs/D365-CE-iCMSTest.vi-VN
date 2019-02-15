---
title: 'Walkthrough 8: Use Customer Engagement knowledge base within your agent application | MicrosoftDocs'
description: Demonstrates how to configure a panel in Unified Service Desk to display knowledge base records.
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
ms.assetid: accd2d7a-9210-403a-abab-52c1cef11757
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
ms.openlocfilehash: 4745641a340624d413834529aebb8deea7c94bb7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385519"
---
# <a name="walkthrough-8-use-customer-engagement-knowledge-base-within-your-agent-application"></a>Walkthrough 8: Use Customer Engagement knowledge base within your agent application
This walkthrough demonstrates how to configure a panel in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the **KM Control** hosted control that displays knowledge base records from your [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] instance.  

 Trong cách này, bạn sẽ:  

- Display knowledge base articles from Dynamics 365 for Customer Engagement apps to appear in a search panel in context with your currently open case record in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Người dùng có thể lọc và sắp xếp các kết quả dựa trên nhiều tiêu chí. Moreover, the search panel automatically appears when you open a case session, and automatically hides when you close the session.  

- Hiển thị bài viết trong một tab khi bạn chọn tiêu đề bài viết trong bảng điều khiển tìm kiếm.  

- Đặt cấu hình các hành động theo ngữ cảnh cho bài viết trong tab nơi bài viết được hiển thị, chẳng hạn như bản sao một liên kết bài viết hoặc liên kết một bài viết với trường hợp hiện tại.  

  [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Use Dynamics 365 for Customer Engagement apps knowledge for effective customer engagement](../unified-service-desk/use-dynamics-365-knowledge-effective-customer-engagement.md)  

> [!IMPORTANT]
>  Cách này không yêu cầu bạn hoàn thành các cách khác trước khi bạn có thể dùng cách này.  

## <a name="prerequisites"></a>Điều kiện tiên quyết  

- Deploy the "New Environment" sample application package to your [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] instance. The walkthrough uses some of the controls and configuration in the "New Environment" sample application package that are created in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps when you deploy the sample application. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Deploy sample Unified Service Desk applications to CRM server using Package Deployer](admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md)    

- Bạn phải biết về những điều sau trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  

  - The `KM Control` and `Panel Layout` types of hosted controls:. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)  

  - Concepts about using the `KM Control` type of hosted control to configure knowledge management. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configure Dynamics 365 for Customer Engagement apps knowledge in Unified Service Desk](../unified-service-desk/configure-unified-service-desk-use-dynamics-365-knowledge.md)  

  - How to configure action calls. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Action calls](../unified-service-desk/action-calls.md)  

  - Sự kiện. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Events](../unified-service-desk/events.md)  

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a>In This Walkthrough  
 [Bước 1: Tạo kiểm soát tổ chức loại Kiểm soát KM](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step1)  

 [Bước 2: Đặt cấu hình cuộc gọi hành động để hiển thị tìm kiếm cơ sở kiến thức](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step2)  

 [Bước 3: Đặt cấu hình cuộc gọi hành động để tự động hiển thị và ẩn bảng điều khiển tìm kiếm cơ sở kiến thức](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step3)  

 [Step 4: Configure an action call to automatically search knowledge base using the incident (case) title](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step4)  

 [Bước 5: Đặt cấu hình kiểm soát tổ chức và các cuộc gọi hành động để hiển thị một bài viết trong một tab](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step5)  

 [Bước 6: Đặt cấu hình các hành động theo ngữ cảnh cho bài viết cơ sở kiến thức trong tab](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step6)  

 [Bước 7: Kiểm tra ứng dụng](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step7)  

 [Kết luận](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Conclusion)  

<a name="Step1"></a>   
## <a name="step-1-create-a-hosted-control-of-type-km-control"></a>Bước 1: Tạo kiểm soát tổ chức loại Kiểm soát KM  
 Trong bước này, bạn sẽ tạo kiểm soát tổ chức loại **Kiểm soát KM** để hiển thị ngăn tìm kiếm cơ sở kiến thức.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Click **Hosted Controls**.  

4. Bấm vào **Mới**.  

5. Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau.  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Tìm kiếm KB Mẫu|  
   |Tên Hiển thị|Tìm kiếm KB Mẫu|  
   |Loại thành phần USD|Kiểm soát KM|  
   |Cho phép nhiều trang|No|  
   |Loại lưu trữ|WPF nội bộ|  
   |Application is Global|Đã kiểm tra|  
   |Nhóm hiển thị|RightPanel|  

   ![Create a KM Control hosted control](../unified-service-desk/media/usd-createkmcontrol.png "Create a KM Control hosted control")  

6. Bấm vào **Lưu và Đóng**.  

<a name="Step2"></a>   
## <a name="step-2-configure-an-action-call-to-display-the-knowledge-base-search"></a>Bước 2: Đặt cấu hình cuộc gọi hành động để hiển thị tìm kiếm cơ sở kiến thức  
 Tạo một cuộc gọi hành động để hiển thị kiểm soát tổ chức mới tạo trong máy tính để bàn của tổng đài viên. You’ll use the `default` action for the newly created hosted control to display it. After creating the action, add it to the `SessionNew` event for the **Dynamics 365 for Customer Engagement apps Global Manager** hosted control to automatically load and display the hosted control when a new session is created on opening a case.  

1. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

2. Bấm **Cuộc gọi Hành động**.  

3. Bấm vào **Mới**.  

4. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Mẫu: Mở Kiểm soát Tìm kiếm KB|  
   |Kiểm soát được lưu trữ|Tìm kiếm KB Mẫu|  
   |Hành động|mặc định|  

   ![Action call to open the KB Search panel](../unified-service-desk/media/usd-openkmcontrol.png "Action call to open the KB Search panel")  

5. Bấm **Lưu và đóng**.  

6. Truy cập trang **Unified Service Desk**, rồi bấm vào **Sự kiện**.  

7. Tìm kiếm sự kiện `SessionNew`, rồi bấm vào sự kiện để mở trang cấu hình sự kiện.  

8. Click the **Add Action Call record** button to add the action call.  

   ![Add action to event](../unified-service-desk/media/usd-addactiontoevent.png "Add action to event")  

9. Type `Sample: Open KB Search Control` in the search box, and press ENTER or click the search button to add the action to the event. Change the order of the added action to 1, and then click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner.  

<a name="Step3"></a>   
## <a name="step-3-configure-action-calls-to-automatically-display-and-hide-the-knowledge-base-search-panel"></a>Bước 3: Đặt cấu hình cuộc gọi hành động để tự động hiển thị và ẩn bảng điều khiển tìm kiếm cơ sở kiến thức  
 Create two action calls to display and hide the panel (`RightPanel`) that will display the newly added hosted control. Tiếp theo, thêm các kiểm soát tổ chức đó vào sự kiện phù hợp để tự động hiển thị (mở rộng) và ẩn (thu hẹp) bảng điều khiển trong máy tính để bàn của tổng đài viên khi phiên mới được tạo và phiên này đóng tương ứng.  

 Use the new `SetVisualProperty` action to control the visual properties of the panel layout (**Main Layout** hosted control in the “Base sample application”). `SetVisualProperty` has to be manually added to the hosted control to be used. Tuy nhiên, nếu bạn tạo phiên bản **Bố cục Bảng điều khiển** loại kiểm soát tổ chức mới, `SetVisualProperty` sẽ sẵn có theo mặc định.  

1. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

2. Bấm **Kiểm soát Tổ chức**.  

3. Bấm vào **Bố cục Chính** trong danh sách kiểm soát tổ chức.  

   > [!NOTE]
   >  The **Main Layout** hosted control is available when you deploy the Base sample application in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.  

4. Bấm vào mũi tên xuống bên cạnh **Bố cục chính**, rồi bấm vào **Hành động UII**.  

   ![Add UII action](../unified-service-desk/media/usd-adduiiaction.png "Add UII action")  

5. Bấm vào **Thêm Hoạt động UII mới**.  

6. Trên trang **Hành động UII Mới**, nhập `SetVisualProperty` vào trường **Tên** rồi bấm vào **Lưu và Đóng**.  

   ![Create a UII action for Main Layout hosted control](../unified-service-desk/media/usd-createuiiaction.png "Create a UII action for Main Layout hosted control")  

    Cuộc gọi hành động mới được thêm vào kiểm soát tổ chức **Bố cục chính** và sẵn sàng được sử dụng.  

7. Trên ngăn điều hướng, bấm vào **Unified Service Desk**.  

8. Bấm **Cuộc gọi Hành động**.  

9. Bấm vào **Mới**.  

10. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.  


    |     Trường      |                                                                                              Giá trị                                                                                               |
    |----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    |      Tên      |                                                                                Mẫu: Mở rộng Hành động Bảng điều khiển Phải                                                                                 |
    | Kiểm soát được lưu trữ | Main Layout **Note:**  The **Main Layout** hosted control is available when you deploy the Base sample application in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance. |
    |     Hành động     |                                                                                        SetVisualProperty                                                                                         |
    |      Dữ liệu      |                                                           elementname=RightPanelExpander<br />propertyname=IsExpanded<br />value=true                                                            |

    ![Create action call](../unified-service-desk/media/usd-expandrightpanelaction.png "Create action call")  

11. Click **Save and Close**.  

12. Bấm vào **Mới** để tạo cuộc gọi hành động mới.  

13. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:  


    |     Trường      |                                                                                              Giá trị                                                                                               |
    |----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    |      Tên      |                                                                               Mẫu: Thu hẹp Hành động Bảng điều khiển Phải                                                                                |
    | Kiểm soát được lưu trữ | Main Layout **Note:**  The **Main Layout** hosted control is available when you deploy the Base sample application in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance. |
    |     Hành động     |                                                                                        SetVisualProperty                                                                                         |
    |      Dữ liệu      |                                                           elementname=RightPanelExpander<br />propertyname=IsExpanded<br />value=false                                                           |

    ![Create action call](../unified-service-desk/media/usd-collapserightpanelaction.png "Create action call")  

14. Click **Save and Close**.  

15. Go to **Unified Service Desk** page, and then click **Events**.  

16. Search for the `SessionNew` event, and then click it to open the event configuration page.  

17. Click the **Add Action Call record** button to add the action call.  

    ![Add action to event](../unified-service-desk/media/usd-addactiontoevent.png "Add action to event")  

18. Type `Sample: Expand Right Panel Action` in the search box, and press ENTER or click the search button to add the action to the event. Change the **Order** of the added action to 2, and then click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner.  

19. Go to **Unified Service Desk** page, and then click **Events**.  

20. Search for the `SessionClosed` event for the **Dynamics 365 for Customer Engagement apps Global Manager** hosted control, and then click it to open the event configuration page.  

    > [!NOTE]
    >  Ensure that you are editing the configuration of the `SessionClosed` event for the **Dynamics 365 for Customer Engagement apps Global Manager** hosted control.  

21. Click the **Add Action Call record** button to add the action call.  

    ![Add action call to event](../unified-service-desk/media/usd-addactiontosessionclosedevent.png "Add action call to event")  

22. Type `Sample: Collapse Right Panel Action` in the search box, and press ENTER or click the search button to add the action to the event. Change the order of the added action to 1, and then click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner.  

<a name="Step4"></a>   
## <a name="step-4-configure-an-action-call-to-automatically-search-the-knowledge-base-using-the-incident-case-title"></a>Bước 4: Đặt cấu hình một cuộc gọi hành động để tự động tìm kiếm cơ sở kiến thức bằng cách sử dụng tiêu đề sự cố (trường hợp)  
 Tạo một cuộc gọi hành động để tự động điền tiêu đề trường hợp trong kiểm soát tìm kiếm cơ sở kiến thức để tìm kiếm dựa trên tên tiêu đề trường hợp. After creating the action, you’ll add it to the `BrowserDocumentComplete` event of the **Incident** hosted control to fire this action after the case records have loaded in the agent desktop.  

> [!NOTE]
>  The **Incident** hosted control is created when you deploy the Base sample application in your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps instance.  

1. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

2. Bấm **Cuộc gọi Hành động**.  

3. Bấm vào **Mới**.  

4. Trên trang **Cuộc gọi Hành động Mới**, chỉ định các giá trị sau  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Mẫu: Tìm kiếm KB bằng Hành động Tiêu đề Sự cố (Trường hợp)|  
   |Kiểm soát được lưu trữ|Sample KB Search|  
   |Hành động|Search|  
   |Dữ liệu|query=[[incident.title]+]|  

   > [!TIP]
   >  Bạn có thể sử dụng tham số dữ liệu bổ sung trong hành động `Search` để xác định tham số tìm kiếm cơ sở kiến thức như số lượng kết quả tìm kiếm để trở về, loại bài viết cơ sở kiến thức được lựa chọn tìm kiếm, và sắp xếp. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Search](../unified-service-desk/km-control-hosted-control.md#Search)  

   ![Create an action call](../unified-service-desk/media/usd-searchkbwithcasetitleaction.png "Create an action call")  

5. Bấm vào **Lưu**.  

6. On the navigation pane, click **Unified Service Desk**, and then click **Hosted Controls**.  

7. Bấm vào **Sự cố** từ danh sách kiểm soát tổ chức.  

8. Bấm vào mũi tên xuống bên cạnh **Sự cố** rồi bấm vào **Sự kiện**.  

   ![View events for the Incident hosted control](../unified-service-desk/media/usd-addactiontoincidentevent.png "View events for the Incident hosted control")  

9. Trong danh sách sự kiện cho kiểm soát tổ chức **Sự cố**, bấm vào `BrowserDocumentComplete`.  

10. Click the **Add Action Call record** button to add the action call.  

    ![Add action to BrowserDocumentComplete event](../unified-service-desk/media/usd-addactiontobrowserdocumentcomplete.png "Add action to BrowserDocumentComplete event")  

11. Type `Sample: Search KB with Incident (Case) Title Action` in the search box, and press ENTER or click the search button to add the action to the event. Click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner.  

> [!NOTE]
>  At this point, the knowledge base search control is configured to display knowledge bases from \Dynamics 365 for Customer Engagement apps in context with the currently opened case record. Ngoài ra, bảng điều khiển tìm kiếm cơ sở kiến thức được cấu hình để tự động hiển thị khi một phiên được tạo và tự động ẩn khi bạn đóng phiên. You can test this by running the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application and connecting to the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps instance where you performed steps 1 through 4 of this walkthrough. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)]  
> 
>  Perform the rest of the steps to display a knowledge base article from the search results in a tab, and configure contextual actions for a selected knowledge base article in the search panel such as copying an article link and associating the article to the current case.  

<a name="Step5"></a>   
## <a name="step-5-configure-hosted-controls-and-action-calls-to-display-an-article-in-a-tab"></a>Bước 5: Đặt cấu hình kiểm soát tổ chức và các cuộc gọi hành động để hiển thị một bài viết trong một tab  
 Trong bước này, bạn sẽ:  

-   Đặt cấu hình kiểm soát tổ chức loại **Ứng dụng Web Tiêu chuẩn** để hiển thị bài viết cơ sở kiến thức.  

-   Đặt cấu hình cuộc gọi hành động để hiển thị bài viết trong kiểm soát tổ chức có tiêu đề được bấm vào trong ngăn tìm kiếm cơ sở kiến thức.  

-   Add the action calls to the [ResultOpen](../unified-service-desk/km-control-hosted-control.md#ResultOpen) event of the `KM Control` hosted control so that the action calls are executed when somebody clicks on the KB article title.  

1. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

2. Bấm **Kiểm soát Tổ chức**.  

3. Bấm vào **Mới**.  

4. On the **New Hosted Control** page, specify the following values.  

   |Trường|Value|  
   |-----------|-----------|  
   |Tên|Bài viết KB Mẫu|  
   |Tên Hiển thị|[[Sample KB Article.question]+]|  
   |USD Component Type|Ứng dụng web chuẩn|  
   |Cho phép nhiều trang|No|  
   |Loại lưu trữ|WPF nội bộ|  
   |Application is Global|Clear|  
   |Nhóm hiển thị|Bảng điều khiển chính|  

   ![New hosted control for displaying the KB article](../unified-service-desk/media/usd-samplekbarticlehostedcontrol.png "New hosted control for displaying the KB article")  

5. Click **Save and Close**.  

6. You’ll now create an action call to set the context of the selected article in the knowledge base search pane. The context information is required if you want to perform additional actions on the currently displayed knowledge base article such as dynamically displaying the tab title based on the knowledge base article question title, copying the link of the article, and associating or dissociating an article with an incident (case) record.  

[!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]

7. Click **Action Calls**.  

8. Bấm vào **Mới**.  

9. On the **New Action Call** page, specify the following values.  

    |Trường|Value|  
    |-----------|-----------|  
    |Tên|Mẫu: Thiết lập Hành động Ngữ cảnh Bài viết KB|  
    |Thứ tự|1|  
    |Kiểm soát được lưu trữ|Sample KB Search|  
    |Hành động|SetArticleContext|  
    |Dữ liệu|articleapplication=Sample KB Article<br />articledata=[[postdata]+]|  

   ![Action call for setting article context](../unified-service-desk/media/usd-actioncallsetarticlecontext.png "Action call for setting article context")  

10. Click **Save and Close**.  

11. Bấm vào **Mới** để tạo cuộc gọi hành động khác để hiển thị bài viết trong kiểm soát tổ chức được tạo trước đây trong bước này.  

12. On the **New Action Call** page, specify the following values.  

   |Trường|Value|  
   |-----------|-----------|  
   |Tên|Mẫu: Mở Hành động Bài viết KB|  
   |Thứ tự|2|  
   |Kiểm soát được lưu trữ|Sample KB Article|  
   |Hành động|Navigate|  
   |Dữ liệu|url=[[Sample KB Search.articleurl]]<br />header=[[header]+]<br />postdata=[[postdata]]|  

   ![Action call to display the KB article](../unified-service-desk/media/usd-actioncallopenkbarticle.png "Action call to display the KB article")  

13. Click **Save and Close**.  

14. Bấm vào **Mới** để tạo cuộc gọi hành động khác để hiển thị kiểm soát tổ chức được tạo trước đây trong bước này trong bảng điều khiển chính.  

15. Trên trang **Cuộc gọi Hành động Mới**, chỉ định các giá trị sau  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Mẫu: Hiển thị Hành động Tab Bài viết KB|  
   |Thứ tự|50|  
   |Kiểm soát được lưu trữ|Dynamics 365 for Customer Engagement apps Global Manager|  
   |Hành động|Hiển thị tab|  
   |Dữ liệu|Sample KB Article|  

   ![Action call to display the KB article in a tab](../unified-service-desk/media/usd-actionshowkbarticletab.png "Action call to display the KB article in a tab")  

16. Click **Save and Close**.  

17. Now, you’ll add all the three new actions created in this step to the [ResultOpen](../unified-service-desk/km-control-hosted-control.md#ResultOpen) event of the **KM Control** hosted control that you created earlier.  

     Trên ngăn điều hướng, bấm vào **Unified Service Desk** rồi bấm vào **Sự kiện**.  

18. Tìm kiếm sự kiện `ResultOpen` và bấm vào tên sự kiện để mở ngăn thông tin sự kiện.  

19. Click the **Add Action Call record** button to add an action call.  

20. Type `Sample: Set KB Article Context Action` in the search box, and press ENTER or click the search button to add the action to the event.  

21. Repeat the previous step with the `Sample: Open KB Article Action` and `Sample: Show KB Article Tab Action` action calls to add them to the event.  

22. Click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner.  

<a name="Step6"></a>   
## <a name="step-6-configure-contextual-actions-for-the-knowledge-base-article-in-the-tab"></a>Bước 6: Đặt cấu hình các hành động theo ngữ cảnh cho bài viết cơ sở kiến thức trong tab  
 In this step, you’ll add buttons on the toolbar of the hosted control configured in the previous step (Step 5) and attach action calls to the buttons so that when the button is clicked, appropriate actions are performed in the context of the currently displayed article in the tab. You’ll configure a toolbar with two buttons and respective action calls for the buttons.  

1. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

2. Bấm vào **Thanh công cụ**.  

3. Bấm vào **Mới**.  

4. Trên trang **Thanh công cụ Mới**, nhập `Sample: KB Toolbar` vào trường **Tên** và bấm vào **Lưu**.  

5. In the **Buttons** area, click the **+** symbol to add buttons to the toolbar.  

6. Trên trang **Nút thanh công cụ mới**, chỉ định các giá trị sau.  

   |Trường|Value|  
   |-----------|-----------|  
   |Tên|Sao chép Liên kết|  
   |Văn bản nút|Sao chép Liên kết|  
   |Thứ tự|1 **Note:**  The **Order** field defines the position of buttons in the toolbar. Nút được sắp xếp từ trái sang phải hoặc trên xuống dưới theo một thứ tự tăng dần.|  

   ![New toolbar button](../unified-service-desk/media/usd-newtoolbarbutton1.png "New toolbar button")  

7. Bấm vào **Lưu**.  

8. You’ll now create an action call for this button to copy the link of the currently displayed article when somebody clicks the button.  

    In the **Actions** area, click **+** on the right corner to add an action call.  

9. In the search box in the **Actions** area, press ENTER or click the search button.  

10. In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.  

    ![Create a new action call for the toolbar button](../unified-service-desk/media/usd-actioncallfortoolbarbutton.png "Create a new action call for the toolbar button")  

11. On the **New Action Call** page, specify the following values.  


    |     Trường      |                 Value                 |
    |----------------|---------------------------------------|
    |      Tên      |  Mẫu: Sao chép Hành động Liên kết Bài viết KB  |
    | Kiểm soát được lưu trữ |      Dynamics 365 for Customer Engagement apps Global Manager      |
    |     Hành động     |            CopyToClipboard            |
    |      Dữ liệu      | data=[[Sample KB Article.publicUrl]+] |


12. Click **Save and Close**. Cuộc gọi hành động mới được thêm vào nút **Sao chép Liên kết**.  

13. Click **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner of the page.  

14. Đóng trang nút thanh công cụ **Sao chép Liên kết** và trả lại trang **Mẫu: Thanh công cụ KB** để thêm một nút khác.  

15. In the **Buttons** area, click the + button to add buttons to the toolbar.  

16. On the **New Toolbar Button** page, specify the following values.  


    |    Trường    |                                                                              Value                                                                               |
    |-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    |    Tên     |                                                                           Liên kết Bài viết                                                                           |
    | Văn bản nút |                                                                           Liên kết Bài viết                                                                           |
    |    Thứ tự    | 2 **Note:**  The **Order** field defines the position of buttons in the toolbar. Nút được sắp xếp từ trái sang phải hoặc trên xuống dưới theo một thứ tự tăng dần. |


17. Bấm vào **Lưu**.  

18. Bây giờ bạn sẽ tạo ra một cuộc gọi hành động cho nút này để liên kết bài viết hiện được hiển thị với bản ghi trường hợp hiện tại.  

     In the **Actions** area, click **+** on the right corner to add an action call.  

19. In the search box in the **Actions** area, press ENTER or click the search button.  

20. Trong hộp kết quả tìm kiếm, bấm vào **Mới** ở góc dưới bên phải để tạo cuộc gọi hành động cho nút thanh công cụ này.  

21. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:  

    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Mẫu: Liên kết Bài viết KB với Hành động Trường hợp|  
    |Kiểm soát được lưu trữ|Sample KB Search|  
    |Hành động|Liên kết|  
    |Dữ liệu|entitytypename=incident<br />recordid =[[incident.Id]] <br />articleuniqueid=[[Sample KB Article.articleUId]] <br />articletitle=[[Sample KB Article.question]] <br />articleprivateurl=[[Sample KB Article.serviceDeskUri]] <br />articlepublicurl=[[Sample KB Article.publicUrl]+]|  

    ![New action call to associate KB article to case](../unified-service-desk/media/usd-actioncalltoassociatearticle.png "New action call to associate KB article to case")  

22. Click **Save and Close**. Cuộc gọi hành động mới được thêm vào nút **Liên kết Bài viết**.  

23. Click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner of the page.  

24. Đóng trang nút thanh công cụ **Liên kết Bài viết** và trả lại trang **Mẫu: Thanh công cụ KB**.  

25. Bây giờ chúng tôi sẽ liên kết thanh công cụ **Mẫu: Thanh công cụ KB** với kiểm soát tổ chức (**Bài viết KB Mẫu**) nơi bạn muốn hiển thị.  

26. Trên thanh điều hướng, bấm vào mũi tên xuống bên cạnh **Mẫu: Thanh công cụ KB** rồi bấm vào **Kiểm soát Tổ chức**.  

    ![Add tool bar to a hosted control](../unified-service-desk/media/usd-addtoolbartohostedcontrol.png "Add tool bar to a hosted control")  

27. Bấm vào **Thêm Kiểm soát Tổ chức Hiện có**.  

28. Trong hộp tìm kiếm, nhập `Sample KB Article` và nhấn ENTER hoặc bấm vào nút tìm kiếm để thêm kiểm soát tổ chức.  

29. Click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner of the page.  

<a name="Step7"></a>   
## <a name="step-7-test-the-application"></a>Bước 7: Kiểm tra ứng dụng  
 Để kiểm tra ứng dụng:  

1. Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] entities as described earlier.  

2. Trong ứng dụng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], bấm vào **Công việc Của tôi** trên thanh công cụ để hiển thị danh sách các trường hợp được chỉ định cho bạn.  

3. In the **My Work** tab, click a case title to open it in a session. Bảng điều khiển Tìm kiếm KB Mẫu được tự động hiển thị ở phía bên phải, với tiêu đề trường hợp hiện tại được điền trước vào hộp tìm kiếm.  

   ![KB Search pane in your agent desktop](../unified-service-desk/media/usd-kmcontrolinaction.png "KB Search pane in your agent desktop")  

4. Nhấp vào một tiêu đề trường hợp trong kết quả tìm kiếm để hiển thị các bài viết trong bảng điều khiển chính. Thông báo hai nút trong tab bài viết: **Sao chép Liên kết** và **Liên kết Bài viết**.  

   ![Article displayed in the main panel](../unified-service-desk/media/usd-kbarticleinmainpanel.png "Article displayed in the main panel")  

   -   Bấm vào **Sao chép Liên kết** để sao chép URL của bài viết. You can paste the URL in the browser to go directly to the article or can copy it in an email and send it to your customer.  

   -   Bấm **Liên kết Bài viết** để liên kết bài viết với trường hợp hiện tại. Thông báo được hiển thị ở đầu bảng điều khiển Tìm kiếm KB Mẫu để thông báo cho bạn rằng bài viết đã được liên kết.  

   ![Link article to a case](../unified-service-desk/media/usd-linkarticletocase.png "Link article to a case")  

<a name="Conclusion"></a>   
## <a name="conclusion"></a>Kết luận  
 In this walkthrough, you learned how to use the KM Control hosted control to use Dynamics 365 for Customer Engagement apps knowledge from within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  

### <a name="see-also"></a>Xem thêm  
 [Use Dynamics 365 for Customer Engagement apps knowledge for effective customer engagement](../unified-service-desk/use-dynamics-365-knowledge-effective-customer-engagement.md)   

 [Configure Dynamics 365 for Customer Engagement apps knowledge in Unified Service Desk](../unified-service-desk/configure-unified-service-desk-use-dynamics-365-knowledge.md)   

 [Kiểm soát KM (Kiểm soát Tổ chức)](../unified-service-desk/km-control-hosted-control.md)   

 [Unified Interface KM Control (Hosted Control)](../unified-service-desk/unified-interface-km-control-hosted-control.md)

 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
