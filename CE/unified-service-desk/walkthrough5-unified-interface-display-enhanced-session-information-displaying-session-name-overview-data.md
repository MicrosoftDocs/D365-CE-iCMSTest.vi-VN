---
title: 'Walkthrough 5: Display enhanced session information by displaying session name and overview data | MicrosoftDocs'
description: Demonstrates how to dynamically display session name and session overview information in Unified Service Desk to enhance the customer-interaction experience for your agents.
ms.custom: ''
ms.date: 05/07/2018
ms.reviewer: ''
ms.service: usd
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: ED76404B-A0DD-4F59-83FB-C1036BE92961
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: f9173a9ef8570fb35e78574299379ec411c40add
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388492"
---
# <a name="walkthrough-5-display-enhanced-session-information-by-displaying-session-name-and-overview-data"></a>Walkthrough 5: Display enhanced session information by displaying session name and overview data
In the previous walkthrough, [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md), you learned how to display your customer record stored in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps in a session in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. However, the experience would be better if you can identify each session with a unique name along with some key overview information about the record in a session.  
  
 Cách này trình cách cách hiển thị tên phiên và thông tin tổng quan về phiên động để nâng cao trải nghiệm tương tác khách hàng cho các tổng đài viên của bạn. This walkthrough is built on top of the previous walkthrough, [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md).  
  
## <a name="prerequisites"></a>Điều kiện tiên quyết  
  
- You must have completed [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) and [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md). The configurations that you completed in those walkthroughs are required in this walkthrough.  
  
- Cách này giả định rằng bạn sẽ đang sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên ở cuối cách này để kiểm tra ứng dụng. If a different user will be testing the application, you must assign the user to **Contoso Configuration**. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)  
  
- You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  
  
  - **Session Lines** and **Session Tabs** type of hosted control. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Session Lines (Hosted Control)](../unified-service-desk/session-lines-hosted-control.md) and [Session Tabs (Hosted Control)](../unified-service-desk/session-tabs-hosted-control.md)  
  
  - Configure session name and session overview information. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configure session information](../unified-service-desk/configure-session-information.md)  
  
  - Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)  
  
## <a name="in-this-walkthrough"></a>In This Walkthrough  
 [Bước 1: Tạo loại dòng phiên của kiểm soát tổ chức để hiển thị thông tin tổng quan về phiên](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md#Step1)  
  
 [Bước 2: Xác định thông tin tên phiên](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md#Step2)  
  
 [Bước 3: Xác định thông tin tổng quan về phiên](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md#Step3)  
  
 [Bước 4: Thêm kiểm soát vào cấu hình](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md#Step4)  
  
 [Bước 5: Kiểm tra ứng dụng](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md#Step5)  
  
 [Kết luận](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md#Conclusion)  
  
<a name="Step1"></a>   
## <a name="step-1-create-a-session-lines-type-of-hosted-control-to-display-session-overview-information"></a>Step 1: Create a Session Lines type of hosted control to display session overview information  
 To display session overview information in your agent application, create an instance of a **Session Lines** type of hosted control in your agent application.  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. Click **Hosted Controls**.  
  
4. Bấm vào **Mới**.  
  
5. On the **New Hosted Control** page, specify the following values:  
  
   |Trường|Giá trị|  
   |-----------|-----------|  
   |Tên|Tổng quan về phiên contoso|  
   |USD Component Type|Dòng Phiên|  
   |Nhóm hiển thị|Bảng điều khiển Trình khám phá phiên|  
  
   ![Create a Session Lines hosted control](../unified-service-desk/media/crm-itpro-usd-wt05-01-unified-interface.png "Create a Session Lines hosted control")  
  
6. Bấm vào **Lưu**. 
  
<a name="Step2"></a>   
## <a name="step-2-define-session-name-information"></a>Step 2: Define session name information  
 To dynamically display the session tab name, you’ll configure a session lines rule using the replacement parameters.  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. Click **Session Lines**.  
  
4. Bấm vào **Mới**.  
  
5. On the **New Session Information** page, specify the following values:  
  
   |Trường|Giá trị|  
   |-----------|-----------|  
   |Đơn hàng|Bất kỳ giá trị ngẫu nhiên; nói 5|  
   |Tên|Tên phiên Contoso|  
   |Thực thể được chọn|tài khoản|  
   |Loại|Tên Phiên|  
   |Hiển thị|Phiên: [[account.name]]<br /><br /> Chúng tôi đang sử dụng các tham số thay thế để xác định định dạng tên tab phiên. In this case the session name will be **Session:** followed by the name of the account record that is displayed in the session.|  
  
   ![Define session tab name text and format](../unified-service-desk/media/crm-itpro-usd-wt05-02-unified-interface.png "Define session tab name text and format")  
  
6. Bấm vào **Lưu**.  
  
<a name="Step3"></a>   
## <a name="step-3-define-session-overview-information"></a>Step 3: Define session overview information  
 Define the session overview information to display in the **Session Lines** type of hosted control that you configured in step 1.  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. Click **Session Lines**.  
  
4. Bấm vào **Mới**.  
  
5. On the **New Session Information** page, specify the following values.  
  
   - **Order**: Any random value; say 6.  
  
   - **Name**: Contoso Session Overview Info  
  
   - **Selected Entity**: account  
  
   - **Type**: Session Overview  
  
   - **Display**:  
  
       ```xaml  
       <Grid Margin="0"      xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"      xmlns:CCA="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics">  
         <Grid.RowDefinitions>  
           <RowDefinition Height="auto" />  
           <RowDefinition Height="auto" />  
           <RowDefinition Height="auto" />  
           <RowDefinition Height="auto" />  
           <RowDefinition Height="auto" />  
           <RowDefinition Height="auto" />  
         </Grid.RowDefinitions>  
         <Grid.ColumnDefinitions>  
           <ColumnDefinition Width="80"/>  
           <ColumnDefinition Width="*" />  
           <ColumnDefinition Width="auto" />  
         </Grid.ColumnDefinitions>  
         <TextBlock Margin="5,0,0,0" Grid.Row="0" TextWrapping="Wrap" Padding="3,0,0,3" Grid.ColumnSpan="3" FontFamily="Tohoma" FontSize="14" Style="{DynamicResource AutoCollapse}" Text="Primary Contact: [[account.primarycontactid.name]x]" />  
         <TextBlock Margin="5,0,0,0" Grid.Row="1" TextWrapping="Wrap" Padding="3,0,0,3" Grid.ColumnSpan="3" FontFamily="Tohoma" FontSize="14" Text="[[account.address1_line1]x]"/>  
         <TextBlock Margin="5,0,0,0" Grid.Row="2" TextWrapping="Wrap" Padding="3,0,0,3" Grid.ColumnSpan="3" FontFamily="Tohoma" FontSize="14" Style="{DynamicResource AutoCollapse}" Text="[[account.address1_line2]+x]" />  
         <TextBlock Margin="5,0,0,0" Grid.Row="3" TextWrapping="Wrap" Padding="3,0,0,3" Grid.ColumnSpan="3" FontFamily="Tohoma" FontSize="14" Style="{DynamicResource AutoCollapse}" Text="[[account.address1_line3]+x]" />  
         <TextBlock Margin="5,0,0,0" Grid.Row="4" TextWrapping="Wrap" Padding="3,0,0,3" Grid.ColumnSpan="3" FontFamily="Tohoma" FontSize="14" Style="{DynamicResource AutoCollapse}" Text="[[account.address1_city]x], [[account.address1_stateorprovince]x] [[account.address1_postalcode]x]" />  
         <TextBlock Margin="5,0,0,0" Grid.Row="5" TextWrapping="Wrap" Padding="3,0,0,3" Grid.ColumnSpan="3" FontFamily="Tohoma" FontSize="14" Style="{DynamicResource AutoCollapse}" Text="Phone: [[account.telephone1]x]" />  
       </Grid>  
       ```  
  
       > [!NOTE]
       >  This sample uses XAML and replacement parameters to define the session overview information that displays the current account’s primary contact, address, and phone number in the session overview area.  
  
   ![Define session overview information](../unified-service-desk/media/crm-itpro-usd-wt05-03-unified-interface.png "Define session overview information")  
  
6. Bấm vào **Lưu**.
  
<a name="Step4"></a>   
## <a name="step-4-add-the-controls-to-the-configuration"></a>Step 4: Add the controls to the configuration  
 In this step, you’ll add the hosted control and session line rules that were configured in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration. **Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).  
  
 Add the following to **Contoso Configuration**.  
  
|Tên kiểm soát|Loại kiểm soát|  
|------------------|------------------|  
|Tổng quan về phiên contoso|Kiểm soát tổ chức|  
|Tên phiên Contoso|Dòng Phiên|  
|Thông tin Tổng quan về phiên contoso|Dòng Phiên|  
  
 To add a control to the configuration:  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. Bấm **Cấu hình**.  
  
4. Click **Contoso Configuration** to open the definition.  
  
5. Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Kiểm soát tổ chức**.  
  
6. Trên trang tiếp theo, bấm vào **Thêm Kiểm soát Tổ chức Hiện có**, nhập “`Contoso Session Overview`” vào thanh tìm kiếm, rồi nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.  
  
7. Trong hộp kết quả tìm kiếm, hãy nhấp vào kiểm soát tổ chức để thêm vào **Cấu hình Contoso**.  
  
8. Tương tự, thêm kiểm soát dòng phiên bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Dòng phiên**.  
  
9. Bấm vào **Lưu**.  
  
<a name="Step5"></a>   
## <a name="step-5-test-the-application"></a>Step 5: Test the application  
  
1. Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] by using the same user credentials that is assigned to Contoso Configuration in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md). For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)  
  
2. Click the down arrow next to the **Search** button in the toolbar, and then click **Account** to display the account records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.  
  
3. Click the expander to display the left pane (SessionExplorerPanel).  
  
   ![Choose the expander in Unified Service Desk](../unified-service-desk/media/usd-choose-expander-unified-interface-left-pane.png "Choose the expander in Unified Service Desk") 
  
4. Click any of the account records to display the respective account information in a session in the agent application. Lưu ý rằng tên của tab phiên hiển thị từ **phiên:** theo sau là tên tài khoản hiện tại. The left pane displays the session overview information that was defined earlier.  
  
   ![Session name and overview information](../unified-service-desk/media/crm-itpro-usd-wt05-05-unified-interface.png "Session name and overview information")  
  
5. If you open another account record, it will be displayed in another session in your client application. To open another account, click the down arrow next to the **Search** button, click **Account**, and then click an account name to display the account information in another session.  
  
   ![Multiple sessions in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt05-06-unified-interface.png "Multiple sessions in Unified Service Desk")
  
<a name="Conclusion"></a>   
## <a name="conclusion"></a>Kết luận  
 In this walkthrough, you saw how to use the session lines configuration rules to contextually display the session tab name and key overview information about the record in a session in your agent application. You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.  
  
### <a name="see-also"></a>Xem thêm

 [Support for Unified Interface Apps in Unified Service Desk](../unified-service-desk/admin/Support-unified-interfaces-apps-usd.md)
 
 [Unified Interface Page (Hosted Control)](../unified-service-desk/unified-interface-page-hosted-control.md)

 [Unified Service Desk and Unified Interface Configuration Walkthroughs](../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md)

 [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)

 [Walkthrough 2: Display an external webpage in your agent application](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md)

 [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)

 [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md)

 [Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md)

 [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)
