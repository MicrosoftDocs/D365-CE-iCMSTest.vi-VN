---
title: Provide feedback about Unified Service Desk (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about providing feedback about Unified Service Desk.
ms.custom: ''
ms.date: 04/24/2018
ms.service: usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 23F085E7-C2E2-44C0-80C1-9E65CCA209E9
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 5989d7148c8f4c3133df2501860850ecba2c56cb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382517"
---
# <a name="provide-feedback-about-includepnunifiedservicedeskincludespn-unified-service-deskmd"></a>Provide feedback about [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]

Have a comment or suggestion about [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]? We need your feedback to help us deliver a reliable product. Good or bad, the quickest route to get your comments to our team is right from within [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. 

With [!INCLUDE[pn-unified-service-desk-3-3](../../includes/pn-unified-service-desk-3-3.md)], you can see **Provide Feedback** option as a smiley on the toolbar.

## <a name="walkthrough-configure-provide-feedback-window-in-your-agent-application"></a>Walkthrough: Configure provide feedback window in your agent application

The walkthrough demonstrates how to set up provide feedback window in your agent application. In this walkthrough, you will learn to create **Provide Feedback** button on the **About Toolbar** toolbar container and associate an Action Call to the button.

### <a name="prerequisites"></a>Điều kiện tiên quyết

Bạn phải biết về những điều sau trong [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]:<br>  
    - The Toolbar Container type of hosted control. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Hosted control types and action/event reference](../../unified-service-desk/hosted-control-types-action-event-reference.md)  

    - Cuộc gọi hành động và cách cấu hình. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Action calls](../../unified-service-desk/action-calls.md)

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a>Trong cách này

 [Bước 1: Tạo loại bộ chứa công cụ của kiểm soát tổ chức](#Step1)

 [Bước 2: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ](#Step2)

 [Step 3: Add toolbar button and action call to display the feedback window](#Step3)

 [Bước 4: Thêm kiểm soát vào cấu hình](#Step4)

 [Step 5: Test the provide feedback option in the application](#Step5)

 [Kết luận](#Conclusion)

<a name="Step1"></a>   
## <a name="step-1-create-a-toolbar-container-type-of-hosted-control"></a>Bước 1: Tạo loại bộ chứa công cụ của kiểm soát tổ chức  

 Toolbar Container type of hosted control are used to hold and display the toolbars in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. Trong phần này, bạn sẽ tạo ra kiểm soát tổ chức **Bộ chứa thanh công cụ** mà sẽ xuất hiện ở phía trên cùng của ứng dụng khách.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]  
3. Click **Hosted Controls**.  

4. Bấm vào **Mới**.  

5. On the **New Hosted Control** page, specify the following values  


   |       Trường        |          Value          |
   |--------------------|-------------------------|
   |        Tên        | About Toolbar Container |
   | USD Component Type |    Bộ chứa thanh công cụ    |
   |   Nhóm hiển thị    |       AboutPanel        |


6. Bấm vào **Lưu**.  

<a name="Step2"></a>   
## <a name="step-2-add-a-toolbar-and-attach-it-to-the-toolbar-container"></a>Bước 2: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ  
 In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 1. This is done to display the toolbar in your agent application.  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]

3. Bấm vào **Thanh công cụ**.  

4. Bấm vào **Mới**.

5. On the **New Toolbar** page, type **About Toolbar** in the **Name** box, and then click **Save**.  

6. Attach the toolbar to the toolbar container hosted control created in step 1. On the nav bar, click the down arrow next to **About Toolbar**, and click **Hosted Controls**.  

7. On the next page, click **Add Existing Hosted Control**, type `About Toolbar Container` in the search bar, and then press **ENTER** or click the search icon.

8. From the search result, click **About Toolbar Container** to add.  

9. Bấm vào **Lưu**.

<a name="Step3"></a>   
## <a name="step-3-add-toolbar-button-and-action-call-to-display-the-feedback-window"></a>Step 3: Add toolbar button and action call to display the feedback window

 In this step, you’ll add button on the toolbar and attach action call to the button so that when the button is clicked, **Provide Feedback** window is displayed in the hosted control that were created in step 1.

1. After you save the toolbar in step 2, the **Buttons** area becomes available. In the **Buttons** area, click **+** on the right corner to add a button.  

2. On the **New Toolbar Button** page, specify the following values:  

    |Trường|Value|  
    |-----------|-----------|  
    |Tên|Provide Feedback|
    |Hình ảnh|msdyusd_Feedback_16|
    |Chú giải công cụ|Provide Feedback|  
    |Thứ tự|102|

3. Bấm vào **Lưu**.

4. You need add the action call to display the **Provide Feedback** in the hosted control created in step 1.

    In the **Actions** area, click **+** on the right corner to add an action call.  

5. In the search box in the **Actions** area, press **ENTER** or click the search icon.  

6. Trong hộp tìm kiếm kết quả, bấm vào **Mới** ở góc dưới bên phải để tạo ra cuộc gọi hành động cho nút thanh công cụ này.

7. On the **New Action Call** page, specify the following values:

    |Trường|Value|  
    |-----------|-----------|  
    |Tên|Show FeedBack Window|  
    |Thứ tự|1|  
    |Kiểm soát được lưu trữ|CRM Global Manager|  
    |Hành động|ShowFeedback|

8. Bấm vào **Lưu**. The new action call gets added to the **Provide Feedback** button.

<a name="Step4"></a>   
## <a name="step-4-add-the-controls-to-the-configuration"></a>Bước 4: Thêm kiểm soát vào cấu hình  
 In this step, you’ll add the action call, hosted control, and toolbar that were created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration. If you have not created **Contoso Configuration**. Visit, [Walkthrough 1: Build a simple agent application](../../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).

 Add the following to **Contoso Configuration**.

|Tên kiểm soát|Loại kiểm soát|  
|------------------|------------------|  
|Show FeedBack Window|Cuộc gọi hành động| 
|About Toolbar Container|Kiểm soát được lưu trữ| 
|Provide Feedback|Thanh công cụ|

 To add a control to the configuration:  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]  

3. Bấm **Cấu hình**.  

4. Click **Contoso Configuration** to open the definition.  

5. On the nav bar, click the down arrow next to **Contoso Configuration**, and select **Action Calls**.  

6. On the next page, click **Add Existing Action Call**, type `Show FeedBack Window` in the search bar, and then press **ENTER** or click the search icon.  

7. The action call listed earlier are displayed in the search results. Add these action call.  

8. Similarly, add the hosted control and the toolbar by clicking the down arrow next to **Contoso Configuration**, and clicking **Hosted Controls** and **Toolbars** respectively.  

9. Bấm vào **Lưu**.


<a name="Step5"></a> 
## <a name="step-5-test-the-provide-feedback-option-in-the-application"></a>Step 5: Test the provide feedback option in the application

Start the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance where you configured [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration**. For information about connecting to a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).

Your agent application will now have a **Smiley** button in the toolbar area.

1. On the toolbar, select the **Provide Feedback** smiley. <br/>The **Feedback** window appears.<br>
2. Select a smiley from the list:
   - Good
   - Normal
   - Không hợp lệ
3. Type your feedback or suggestion in the text box. 
4. Select **Submit** to send your feedback to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)].<br>

   ![Provide feedback smiley and window](../media/provide-feedback-smiley-window.PNG "Provide feedback smiley and window")


<a name="Conclusion"></a> 
## <a name="conclusion"></a>Kết luận

 In this walkthrough, you learned how to set up provide feedback button in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application.  

> [!Note]
> It is recommended that you do not submit any feedback containing personal or other data that is subject to legal or regulatory compliance requirements.
> 
> [!Note]
> Setting the **HelpImproveUsd** global option to **False**, disables the data collection and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] dose not send information to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)]. If the data collection is disabled, then agent or system administrator cannot provide feedback due to insufficient permissions.<br>
> ![Insufficient Permissions](../media/insufficient-permissions-provide-feedback-window.PNG "Insufficient Permissions")

## <a name="see-also"></a>Xem thêm

[Help improve Unified Service Desk](../admin/help-improve-unified-service-desk.md)
