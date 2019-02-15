---
title: Unified Interface Settings (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about the Unified Interface Settings page in the Unified Service Desk Administrator app.
keywords: ''
ms.date: 08/17/2018
ms.service:
- usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 88B92EC9-81ED-4EB0-8269-2DC0624B6DBA
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
monikerRange: '>=dynamics-usd-4'
ms.openlocfilehash: 929a184b1e33749e654f45ebaffe7b9ed427f9d1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382500"
---
# <a name="preview-feature---set-default-unified-interface-app-using-unified-interface-settings"></a>Preview feature - Set default Unified Interface App using Unified Interface Settings

Unified Interface Settings is a new configuration element introduced under **Advanced Settings** in the Unified Service Desk Administrator app. Unified Interface Settings enables you as an administrator to configure the default Unified Interface App for your agents and transform the Unified Service Desk sign-in experience.  

![Unified Interface Settings](../media/usd-crm-unified-interface-settings.PNG "Unified Interface Settings")

In addition, you can now configure the settings like a theme, Unified Interface App, and assign users (agents) to the Unified Interface Settings record. After creating a Unified Interface Settings record, you can assign this record to a configuration, so that when the users (agents) sign in to Unified Service Desk client, the system authenticates the users (agents) straight away without showing the application selection window.

> [!NOTE]
> The Unified Interface Settings configuration option is supported only on Dynamics 365 for Customer Engagement apps (Unified Interface apps) and not supported on Dynamics 365 for Customer Engagement apps Web Client.


## <a name="how-to-create-unified-interface-settings-record"></a>How to create Unified Interface Settings record

1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps

2. Go to **Settings** > **My Apps** > **Unified Service Desk Administrator** app.

3. Select **Site Map**.</br>
![Select Site Map to go to Unified Interface Settings](../media/usd-crm-site-map-unified-interface-setting.PNG "Select Site Map to go to Unified Interface Settings")
 
4. Choose **Unified Interface Settings** under **Advanced Settings**.

5. In the **Active Unified Interface Settings** page, choose **+ New** to create a new record.

6. In the **New Unified Interface Settings** page, specify the following:

    | Trường  | Value  |
    |:----------|:----------|
    | Tên         | Specify a name of the record.</br> For example, **Sample Setting**. |
    | Chủ đề        | Select a theme for the App.<br>There are two themes.<br>- Air</br>- Unified Blue |
    | Unified Interface App | Select a Unified Interface App for the record. </br> For example, **Customer Service Hub**.|
    | Chủ sở hữu | Add the user profile for the record by choosing the search icon. |
    
  ![New Unified Interface Settings record](../media/usd-crm-unified-new-record-interface-settings.PNG "New Unified Interface Settings record")

7. Chọn **Lưu & Đóng**.

## <a name="add-the-unified-interface-settings-record-to-a-configuration"></a>Add the Unified Interface Settings record to a Configuration

you can add the Unified Interface Settings record to a configuration in two ways:

- Assign a configuration the Unified Interface Settings page.
- Assign a Unified Interface Setting record to a configuration.

### <a name="assign-a-configuration-from-the-unified-interface-settings-page"></a>Assign a configuration from the Unified Interface Settings page

1. Go to the Unified Interface Setting record for which you want to attach the configuration.

2. Choose **Related** > **Configuration**.<br>
![Add configuration to the unified interface setting record](../media/usd-crm-unified-interface-add-configuration.PNG "Add configuration to the unified interface setting records")

3. In the **Configuration** tab, select **Add Existing Configuration**.<br>
  > [!Note]
  > You can select **Add New Configuration** to create and then add the configuration to the Unified Interface Settings record. In this walkthrough, we are attaching an already created configuration,**Test Configuration**, to the Unified Interface Settings record.
  
4. In the **Lookup Records** pane, specify the name of the configuration, and choose search icon.<br> The configuration appears, choose the configuration and then choose **Add**.<br>
![Add configuration to the unified interface setting record](../media/usd-crm-add-configuration-unified-interface-record.PNG "Add configuration to the unified interface setting records")

The configuration is added successfully and appears in the **Configuration** tab.

### <a name="assign-a-unified-interface-settings-record-in-the-configuration-page"></a>Assign a Unified Interface Settings record in the Configuration page

1. Go to **Site Map** > **Configuration**.

2. Select **+ New** to create a configuration record.

3. In the **New Configuration** page, specify the required details for the fields. 

4. In the **Unified Interface Settings** field, type the name of the existing Unified Interface record you want to assign, and choose the search icon.<br> Select the record when it appears..<br>
![Add unified interface setting record to the configuration](../media/usd-crm-add-unified-interface-record-configuration.PNG "Add unified interface setting record to the configuration")<br>
    >[!Note]
    > In the above step, we added an existing Unified Interface Settings record to the configuration. To create a new Unified Interface Settings record, see [How to create Unified Interface Setting record](#how-to-create-unified-interface-setting-record).

5. Select **Save & Close**.

## <a name="login-experience-to-unified-service-desk"></a>Login experience to Unified Service Desk 

Here are the scenarios you need to consider for signing in to Unified Service Desk.

### <a name="scenario-1-users-agents-assigned-to-configuration-with-a-unified-interface-settings-record"></a>Scenario 1: Users (agents) assigned to Configuration with a Unified Interface Settings record

Add users (agents) to a **Configuration** and add a record to the **Unified Interface Settings** field in the **Configuration**. When the user (agent) added to the configuration signs in to Unified Service Desk, the system authenticates the user (agent) and displays the landing page of the Unified Interface App. 

### <a name="scenario-2-users-agents-assigned-to-configuration-without-a-unified-interface-settings-record"></a>Scenario 2: Users (agents) assigned to Configuration without a Unified Interface Settings record

Add users (agents) to a **Configuration**, and the **Unified Interface Settings** field is empty in the **Configuration**. In this scenario consider three cases:

 - If there is a default **Configuration** with a **Unified Interface Settings** record assigned, then the system authenticates the user (agent) and displays the landing page of Unified Interface App.

 - If there is a default **Configuration** with no **Unified Interface Settings** record, then during login, the system displays the application selection window for the user (agent) to select Unified Interface App.

 - If there is no default **Configuration**, then during login, the system displays the application selection window for the user (agent) to select Unified Interface App.

### <a name="scenario-3-users-agents-assigned-to-configuration-and-unified-interface-settings-record-is-not-created"></a>Scenario 3: Users (agents) assigned to Configuration, and Unified Interface Settings record is not created

Add users (agents) to a **Configuration**, and no Unified Interface Settings records are created. As a result, there are no records to select for the **Unified Interface Settings** field in the **Configuration**. In this scenario, when the user (agent) assigned to a particular configuration signs in to Unified Service Desk, the application selection window is displayed and the user (agent) has to select the Unified Interface App.


## <a name="see-also"></a>Xem thêm
 [Unified Interface Page (Hosted Control)](../../unified-service-desk/unified-interface-page-hosted-control.md)

 [Unified Service Desk and Unified Interface Configuration Walkthroughs](../../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md)

 [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) 

 [Cách 2: Hiển thị trang web bên ngoài trong ứng dụng tổng đài viên của bạn](../../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md)  

 [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)  

 [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md)   

 [Cách 5: Hiển thị thông tin phiên bổ sung bằng cách hiển thị tên và dữ liệu tổng quan về phiên](../../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md)  

 [Hướng 6: Đặt cấu hình kiểm soát tổ chức trình gỡ lỗi trong ứng dụng tổng đài viên của bạn](../../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md)
 
 [Cách 7: Đặt cấu hình mã lệnh tổng đài viên trong ứng dụng tổng đài viên của bạn](../../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)
