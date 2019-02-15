---
title: 'Walkthrough 7: Configure agent scripting in your agent application | MicrosoftDocs'
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
ms.assetid: E85F8E08-2C2C-4CC1-90B3-1E9656836B37
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
ms.openlocfilehash: 13c9da83eb9b17d66a5bec436b3e7ced3301c7ad
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387930"
---
# <a name="walkthrough-7-configure-agent-scripting-in-your-agent-application"></a>Walkthrough 7: Configure agent scripting in your agent application
Agent scripting in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] helps to guide your agents during customer interaction. Cách này trình bày cách tạo mã lệnh tổng đài viên đơn giảm giúp tổng đài viên nhanh chóng tạo trường hợp mới cho tài khoản hoặc tìm các trường hợp hiện có từ ứng dụng tổng đài viên. Mã lệnh tổng đài viên đã tạo trong cách này được thực hiện khi tổng đài viên dừng một hồ sơ tài khoản để xem, hồ sơ đó được hiển thị trong phiên trong ứng dụng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Mã lệnh cung cấp ba tùy chọn sau:  

-   Tạo ra một trường hợp cho tài khoản hiện tại  

-   Display existing cases for the current account  

-   Close the session  

## <a name="prerequisites"></a>Điều kiện tiên quyết  

- You must have completed [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) and [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md). The configurations that you completed in those walkthroughs are required in this walkthrough.  

- Cách này giả định rằng bạn sẽ sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên. If a different user will be testing the application, you must assign the user to **Contoso Configuration**. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)  

- You must know be familiar with the following concepts in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  

  - **Agent Scripting** type of hosted control and how to configure agent scripts. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Agent Scripting (Hosted Control)](../unified-service-desk/agent-scripting-hosted-control.md) and [Guide customer interactions with agent scripts](../unified-service-desk/guide-customer-interactions-agent-scripts.md)  

  - How to configure [Action calls](../unified-service-desk/action-calls.md)  

  - How to configure window navigation rules. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Use window navigation rules in Unified Service Desk](../unified-service-desk/use-window-navigation-rules-unified-service-desk.md)  

  - Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)  

## <a name="in-this-walkthrough"></a>In This Walkthrough  
 [Bước 1: Tạo một loại mã lệnh tổng đài viên của kiểm soát tổ chức](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step1)  

 [Bước 2: Tạo kiểm soát tổ chức để hiển thị biểu mẫu trường hợp mới và trường hợp hiện có](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step2)  

 [Bước 3: Tạo một tác vụ mã lệnh tổng đài viên](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step3)  

 [Bước 4: Thêm câu trả lời, cuộc gọi hành động và nguyên tắc điều hướng cửa sổ để tạo trường hợp từ mã lệnh tổng đài viên](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step4)  

 [Bước 5: Thêm câu trả lời và cuộc gọi hành động để hiển thị trường hợp sẵn có](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step5)  

 [Bước 6: Thêm câu trả lời và cuộc gọi hành động để đóng phiên](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step6)  

 [Bước 7: Tạo cuộc gọi hành động để hiển thị mã lệnh tổng đài viên](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step7)  

 [Bước 8: Hiển thị mã lệnh tổng đài viên khi hồ sơ tài khoản được hiển thị trong phiên.](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step8)  

 [Bước 9: Thêm kiểm soát vào cấu hình](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step9)  

 [Bước 10: Kiểm tra ứng dụng](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step10)  

 [Kết luận](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Conclusion)  

<a name="Step1"></a>   
## <a name="step-1-create-an-agent-scripting-type-of-hosted-control"></a>Step 1: Create an Agent Scripting type of hosted control  
 An instance of the **Agent Scripting** type of hosted control must be available in your agent application to display agent scripts.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Click **Hosted Controls**.  

4. Bấm vào **Mới**.  

5. On the **New Hosted Control** page, specify the following values.  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Mã lệnh tổng đài viên Contoso|  
   |USD Component Type|Mã lệnh của tổng đài viên|  
   |Nhóm hiển thị|Bảng điều khiển quy trình làm việc|  

   ![Create an Agent Scripting hosted control](../unified-service-desk/media/usd-create-agent-scripting-hosted-control-unified-interface.png "Create an Agent Scripting hosted control") 

6. Bấm vào **Lưu**.  

<a name="Step2"></a>   
## <a name="step-2-create-hosted-controls-to-display-the-new-case-form-and-existing-cases"></a>Step 2: Create hosted controls to display the new case form and existing cases  
 In this step, you’ll create two hosted controls of Unified Interface Page type to display the new case creation form and existing cases for the current account.  

1. Trên trang kiểm soát tổ chức, bấm vào **Mới**.  

2. Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau:  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Contoso new case form|  
   |Tên Hiển thị|Trường hợp mới|  
   |USD Component Type|Unified Interface Page|  
   |Allow Multiple Pages|Không|
   |Application is Global|Không được chọn|  
   |Nhóm hiển thị|Bảng điều khiển chính|  

   ![Create a Unified Interface Page hosted control](../unified-service-desk/media/usd-create-page-hosted-control-2-case-form-unified-interface.png "Create a Unified Interface Page hosted control") 

3. Bấm vào **Lưu**.  

4. On the hosted controls page, click **New** to create another hosted control.  

5. Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau:  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Contoso existing cases for an account|  
   |Tên Hiển thị|Trường hợp cho [[$Context.name]]<br> **Note:**  We are using the replacement parameter to dynamically display the name of the current account from the execution context as the hosted control display name.|  
   |USD Component Type|Unified Interface Page|  
   |Allow Multiple Pages|Không|
   |Application is Global|Không được chọn|  
   |Nhóm hiển thị|Bảng điều khiển chính|  

   ![Create a Unified Interface Page hosted control](../unified-service-desk/media/usd-create-agent-script-task-existing-case-form-account-unified-interface.png "Create a Unified Interface Page hosted control")  

6. Bấm vào **Lưu**.  

<a name="Step3"></a>   
## <a name="step-3-create-an-agent-script-task"></a>Step 3: Create an agent script task  
 Create an agent script task to display when an account record is displayed in a session.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Click **Agent Scripts**.  

4. Bấm vào **Mới**.  

5. On the **New Agent Script Task** page, specify the following values:  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Contoso: Chào mừng bạn đến với Phiên tài khoản|  
   |Bắt đầu nhiệm vụ|No|  
   |Văn bản mã lệnh|Chào mừng bạn đến [[$Context.name]]. Tên tôi là [[$User.firstname]]. Is this call regarding a new or an existing service request?<br>**Note:**  We are using replacement parameters to dynamically display the account name and the current agent’s name to the agent at runtime.|  
   |Hướng dẫn|Based on the customer response, click one of the tasks below.|  

   ![Create an agent script task](../unified-service-desk/media/usd-create-new-agent-script-task-2-unified-interface.png "Create an agent script task")

6. Click **Save** to create the agent script.  

<a name="Step4"></a>   
## <a name="step-4-add-the-answer-action-call-and-window-navigation-rule-for-creating-a-case-from-the-agent-script"></a>Step 4: Add the answer, action call, and window navigation rule for creating a case from the agent script  
 Trong bước này, bạn sẽ tạo ra câu trả lời, cuộc gọi hành động và nguyên tắc điều hướng cửa sổ để hiển thị biểu mẫu trường hợp mới với một số giá trị được xác định trước từ hồ sơ tài khoản đang hiện hoạt.  

1. In the **Answers** area of the agent script task that you created in step 4, click **+** to create answer.  

2. In the search box, press ENTER or click the search icon, and then click **New** in the search results box.  

   ![Create an answer for an agent script task](../unified-service-desk/media/usd-create-answer-agent-script-task-unified-interface.png "Create an answer for an agent script task")

3. On the **New Agent Script Answer** page, specify the following values:  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Contoso: Trường hợp mới|  
   |Văn bản câu trả lời|Create a case|  
   |Nhiệm vụ được liên kết|Contoso: Welcome to Account Session|  
   |Thứ tự|1|  

   ![Create an answer in Unified Service Desk](../unified-service-desk/media/usd-create-new-case-agent-script-answer-unified-interface.png "Create an answer in Unified Service Desk")

4. Bấm vào **Lưu**.  

5. Next, add an action call to this answer to display a new case form for the account when the agent clicks this answer. On the nav bar, click the down arrow next to **Contoso: New case**, and select **Actions**.  

   ![Create an action call for the answer](../unified-service-desk/media/usd-create-action-call-answer.png "Create an action call for the answer")  

6. On the next page, click **Add Existing Action Call**.  

7. In the search box, press ENTER or click the search icon, and then click **New** to create an action call.  

8. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Cuộc gọi hành động contoso: Tạo trường hợp|  
   |Đơn hàng|1|  
   |Kiểm soát tổ chức|Biểu mẫu trường hợp mới|  
   |Hành động|New_CRM_Page|  
   |Dữ liệu|LogicalName=incident<br /> customerid=EntityReference([[$Context.InitialEntity]],[[$Context.Id]])  <br /> customeridname=[[$Context.name]] <br /> primarycontactid=[[$Context.primarycontactid.id]+]  <br /> primarycontactidname=[[$Context.primarycontactid.name]+]<br>**Note:**  The new case form will be populated with the current account record data to help the agent quickly create a case for the customer.|  

   ![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-new-agent-script-answer-create-case-new-action-call-unified-interface.png "Create an action call in Unified Service Desk") 

9. Bấm vào **Lưu**.  

10. Next, create a window navigation rule to display the new case form. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)] 

11. Click **Window Navigation Rules**.  

12. Bấm vào **Mới**.  

13. On the **New Window Navigation Rule** page, specify the following values.  

    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Trường hợp mới Contoso cho nguyên tắc phiên tài khoản|  
    |Thứ tự|20|  
    |Từ|Contoso new case form|  
    |Thực thể|sự cố|  
    |Loại định tuyến|In Place|  
    |Điểm đến|Thẻ|  
    |Hành động|In Place|
    |Hide Command Bar|Không|  
    |Hide Navigation Bar|Có|

    ![Create a window navigation rule](../unified-service-desk/media/usd-new-navigation-rule-case-account-session-rule.png "Create a window navigation rule")  

14. Bấm vào **Lưu**.  

<a name="Step5"></a>   
## <a name="step-5-add-the-answer-and-action-calls-for-displaying-existing-cases"></a>Step 5: Add the answer and action calls for displaying existing cases  
 Trong bước này, thêm câu trả lời và cuộc gọi hành động để hiển thị các trường hợp sẵn có cho tài khoản hiện tại.  

1. In the **Answers** area of the **Contoso: Welcome to Account Session** agent script, click **+** to create an answer.  

2. In the search box, press ENTER or click the search icon, and then click **New** in the search results box.  

3. Trên trang **Câu trả lời mã lệnh tổng đài viên mới**, chỉ định các giá trị sau.  


   |    Trường    |                Giá trị                |
   |-------------|-------------------------------------|
   |    Tên     |       Contoso: Trường hợp hiện có       |
   | Văn bản câu trả lời |       Hiển thị trường hợp hiện có        |
   | Nhiệm vụ được liên kết | Contoso: Chào mừng bạn đến với Phiên tài khoản |
   |    Đơn hàng    |                  2                  |


4. Bấm vào **Lưu**.  

5. Tiếp theo, thêm cuộc gọi hành động vào câu trả lời này để hiển thị các trường hợp sẵn có cho tài khoản hiện tại. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Trường hợp hiện có** và chọn **Hành động**.  

6. Trên trang tiếp theo, bấm vào **thêm cuộc gọi hành động hiện có**.  

7. Trong hộp tìm kiếm, nhấn ENTER hoặc nhấp vào biểu tượng tìm kiếm, sau đó nhấp vào **Mới** để tạo cuộc gọi hàn động.  

8. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:  


   |     Trường      |                         Giá trị                         |
   |----------------|-------------------------------------------------------|
   |      Tên      |      Cuộc gọi hành động Contoso: Hiển thị trường hợp hiện có      |
   |     Đơn hàng      |                           1                           |
   | Kiểm soát tổ chức |         Contoso existing cases for an account         |
   |     Hành động     |                    Chế độ xem Liên kết                     |
   |      Dữ liệu      | navItemId=[[$Context.Id]] <br />type=[[$Context.etn]] |


9. Bấm vào **Lưu**.  

10. Add another action call to set the focus on the new case form. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:  

    |Trường|Giá trị|  
    |-----------|-----------|  
    |Tên|Cuộc gọi hành động Contoso: Tập trung vào trường hợp hiện có|  
    |Đơn hàng|2|  
    |Kiểm soát tổ chức|Trình quản lý chung contoso|  
    |Hành động|Hiển thị tab|  
    |Dữ liệu|Contoso existing cases for an account|  

    ![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call-set-focus-existing-cases.png "Create an action call in Unified Service Desk") 

11. Bấm vào **Lưu**.  

<a name="Step6"></a>   
## <a name="step-6-add-the-answer-and-action-calls-for-closing-the-session"></a>Step 6: Add the answer and action calls for closing the session  
 Trong bước này, thêm câu trả lời và cuộc gọi hành động để đóng phiên.  

1. In the **Answers** area of the **Contoso: Welcome to Account Session** agent script, click **+** to create an answer.  

2. In the search box, press ENTER or click the search icon, and then click **New** in the search results box.  

3. Trên trang **Câu trả lời mã lệnh tổng đài viên mới**, chỉ định các giá trị sau:  


   |    Trường    |                Giá trị                |
   |-------------|-------------------------------------|
   |    Tên     |       Contoso: Đóng phiên        |
   | Văn bản câu trả lời |            Đóng phiên            |
   | Nhiệm vụ được liên kết | Contoso: Chào mừng bạn đến với Phiên tài khoản |
   |    Đơn hàng    |                  3                  |


4. Bấm vào **Lưu**.  

5. Tiếp theo, thêm cuộc gọi hành động cho câu trả lời này để đóng phiên. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Contoso: Đóng phiên** và chọn Hành động.  

6. Trên trang tiếp theo, bấm vào **thêm cuộc gọi hành động hiện có**.  

7. Trong hộp tìm kiếm, nhấn ENTER hoặc nhấp vào biểu tượng tìm kiếm, sau đó nhấp vào **Mới** để tạo cuộc gọi hàn động.  

8. Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Contoso Action Call: Close Session|  
   |Kiểm soát được lưu trữ|Contoso Session Tab <br> **Note:**  The Contoso Session Tab hosted control was created in [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md).|  
   |Hành động|Đóng phiên|  
   |Dữ liệu|sessionid=[[$Context.SessionId]]|  

   ![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-close-session-action-call.png "Create an action call in Unified Service Desk") 

9. Bấm vào **Lưu**.  

<a name="Step7"></a>   
## <a name="step-7-create-an-action-call-to-display-the-agent-script"></a>Step 7: Create an action call to display the agent script  
 In this step, create an action call to display the agent script.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Click **Action Calls**.  

4. Bấm vào **Mới**.  

5. On the **New Action Call** page, specify the following values.  

   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Các cuộc gọi hành động contoso: Tải mã lệnh tổng đài viên|  
   |Kiểm soát tổ chức|Mã lệnh tổng đài viên Contoso|  
   |Hành động|Đi đến tác vụ|  
   |Dữ liệu|Contoso: Welcome to Account Session|  

   ![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-add-load-agent-script-action-call.png "Create an action call in Unified Service Desk")  

6. Bấm vào **Lưu**.  

<a name="Step8"></a>   
## <a name="step-8-display-the-agent-script-when-the-account-record-is-displayed-in-a-session"></a>Step 8: Display the agent script when the account record is displayed in a session  
 In this step, add the action call created in the previous step to the **PageReady** event on the **Contoso Account Session** hosted control so that after it’s loaded, the action call is executed to load the agent script. The **Contoso Account Session** hosted control was created in [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md).  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Click **Hosted Controls**.  

4. Search for the **Contoso Account Session** hosted control, and click it to open the hosted control definition. 

5. On the nav bar, click the down arrow next to **Contoso Account Session**, and then click **Events**.  

   ![Configure events for a hosted control](../unified-service-desk/media/usd-configure-events-hosted-control.png "Configure events for a hosted control")  

6. On the events page, click **PageReady**.  

7. On the **PageReady** page, click **+** in the **Active Actions** area to add an action call to the event.  

8. Trong hộp tìm kiếm, nhập “`Contoso Action Call: Load Agent Script`” và nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.  

9. Trong kết quả tìm kiếm, bấm vào **Cuộc gọi hành động Contoso: Tải mã lệnh tổng đài viên** để thêm.  

10. Bấm vào **Lưu**.  

<a name="Step9"></a>   
## <a name="step-9-add-the-controls-to-the-configuration"></a>Bước 9: Thêm kiểm soát vào cấu hình  
 In this step, add the action calls, agent script, hosted controls, and window navigation rule that you configured in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration. **Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).  

 Add the following to **Contoso Configuration**.  

|Tên kiểm soát|Loại kiểm soát|  
|------------------|------------------|  
|Cuộc gọi hành động contoso: Tạo trường hợp|Cuộc gọi hành động|  
|Cuộc gọi hành động Contoso: Hiển thị trường hợp hiện có|Cuộc gọi hành động|  
|Cuộc gọi hành động Contoso: Tập trung vào trường hợp hiện có|Cuộc gọi hành động|  
|Các cuộc gọi hành động contoso: Đóng phiên|Cuộc gọi hành động|  
|Các cuộc gọi hành động contoso: Tải mã lệnh tổng đài viên|Cuộc gọi hành động|  
|Contoso: Chào mừng bạn đến với Phiên tài khoản|Mã lệnh tổng đài viên|  
|Mã lệnh tổng đài viên Contoso|Kiểm soát tổ chức|  
|Biểu mẫu trường hợp mới|Kiểm soát tổ chức|  
|Trường hợp sẵn có Contoso cho tài khoản|Kiểm soát tổ chức|  
|Trường hợp mới Contoso cho nguyên tắc phiên tài khoản|Window navigation rule|  

 To add a control to the configuration:  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. Bấm **Cấu hình**.  

4. Click **Contoso Configuration** to open the definition.  

5. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.  

6. Trên trang tiếp theo, bấm vào **Thêm cuộc gọi hành động hiện có**, nhập "Cuộc gọi hành động Contoso" trong thanh tìm kiếm, sau đó nhấn ENTER hoặc nhấp biểu tượng tìm kiếm.  

7. Chọn năm cuộc gọi hành động từ hộp kết quả tìm kiếm để thêm chúng vào **Cấu hình Contoso**.  

8. Tương tự, thêm mã lệnh tổng đài viên, kiểm soát tổ chức và nguyên tắc điều hướng cửa sổ bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Mã lệnh tổng đài viên** **Kiểm soát tổ chức** và **Nguyên tắc điều hướng cửa sổ** lần lượt.  

9. Bấm vào **Lưu**. 

<a name="Step10"></a>   
## <a name="step-10-test-the-application"></a>Step 10: Test the application  

1. Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] by using the same user credentials that is assigned to Contoso Configuration in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md). For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to CRM instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)  

2. Click the down arrow next to the **SEARCH** button in the toolbar, and then click **Account** to display the account records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.  

3. Click the expander to display the left pane.  

   ![Choose the expander in Unified Service Desk](../unified-service-desk/media/usd-choose-expander.png "Choose the expander in Unified Service Desk")  

4. Click on any of the account records to display the respective account information in a session. In the left pane, the **Contoso: Welcome to Account Session** agent script appears.  

   ![Agent script in Unified Service Desk](../unified-service-desk/media/usd-agent-script.png "Agent script in Unified Service Desk")  

5. In the agent script:  

   1.  Click **New case** to open a new case form with pre-populated values (in the red box) from the current account record.  

   ![New case form using the agent script](../unified-service-desk/media/usd-new-case-form-agent-script.png "New case form using the agent script")  

   2.  Click **Display existing cases** to display the associated cases for the current account record.  

   ![Display existing cases for an account](../unified-service-desk/media/usd-show-cases-account.png "Display existing cases for an account")  

   3.  Click **Close session** to close the current session.  

<a name="Conclusion"></a>   
## <a name="conclusion"></a>Kết luận  
 In this walkthrough, you learned how to configure a simple agent script to guide your call center agents. [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] allows you to create more complex scripts with branching logic that contain child answers and actions. You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.  

### <a name="see-also"></a>Xem thêm

 [Support for Unified Interface Apps in Unified Service Desk](../unified-service-desk/admin/Support-unified-interfaces-apps-usd.md)

 [Unified Interface Page (Hosted Control)](../unified-service-desk/unified-interface-page-hosted-control.md)

 [Unified Service Desk and Unified Interface Configuration Walkthroughs](../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md)

 [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)

 [Walkthrough 2: Display an external webpage in your agent application](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md)

 [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)

 [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md)

 [Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md)

 [Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md)
