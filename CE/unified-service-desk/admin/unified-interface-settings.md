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
# <a name="preview-feature---set-default-unified-interface-app-using-unified-interface-settings"></a><span data-ttu-id="8db0e-103">Preview feature - Set default Unified Interface App using Unified Interface Settings</span><span class="sxs-lookup"><span data-stu-id="8db0e-103">Preview feature - Set default Unified Interface App using Unified Interface Settings</span></span>

<span data-ttu-id="8db0e-104">Unified Interface Settings is a new configuration element introduced under **Advanced Settings** in the Unified Service Desk Administrator app.</span><span class="sxs-lookup"><span data-stu-id="8db0e-104">Unified Interface Settings is a new configuration element introduced under **Advanced Settings** in the Unified Service Desk Administrator app.</span></span> <span data-ttu-id="8db0e-105">Unified Interface Settings enables you as an administrator to configure the default Unified Interface App for your agents and transform the Unified Service Desk sign-in experience.</span><span class="sxs-lookup"><span data-stu-id="8db0e-105">Unified Interface Settings enables you as an administrator to configure the default Unified Interface App for your agents and transform the Unified Service Desk sign-in experience.</span></span>  

<span data-ttu-id="8db0e-106">![Unified Interface Settings](../media/usd-crm-unified-interface-settings.PNG "Unified Interface Settings")</span><span class="sxs-lookup"><span data-stu-id="8db0e-106">![Unified Interface Settings](../media/usd-crm-unified-interface-settings.PNG "Unified Interface Settings")</span></span>

<span data-ttu-id="8db0e-107">In addition, you can now configure the settings like a theme, Unified Interface App, and assign users (agents) to the Unified Interface Settings record.</span><span class="sxs-lookup"><span data-stu-id="8db0e-107">In addition, you can now configure the settings like a theme, Unified Interface App, and assign users (agents) to the Unified Interface Settings record.</span></span> <span data-ttu-id="8db0e-108">After creating a Unified Interface Settings record, you can assign this record to a configuration, so that when the users (agents) sign in to Unified Service Desk client, the system authenticates the users (agents) straight away without showing the application selection window.</span><span class="sxs-lookup"><span data-stu-id="8db0e-108">After creating a Unified Interface Settings record, you can assign this record to a configuration, so that when the users (agents) sign in to Unified Service Desk client, the system authenticates the users (agents) straight away without showing the application selection window.</span></span>

> [!NOTE]
> <span data-ttu-id="8db0e-109">The Unified Interface Settings configuration option is supported only on Dynamics 365 for Customer Engagement apps (Unified Interface apps) and not supported on Dynamics 365 for Customer Engagement apps Web Client.</span><span class="sxs-lookup"><span data-stu-id="8db0e-109">The Unified Interface Settings configuration option is supported only on Dynamics 365 for Customer Engagement apps (Unified Interface apps) and not supported on Dynamics 365 for Customer Engagement apps Web Client.</span></span>


## <a name="how-to-create-unified-interface-settings-record"></a><span data-ttu-id="8db0e-110">How to create Unified Interface Settings record</span><span class="sxs-lookup"><span data-stu-id="8db0e-110">How to create Unified Interface Settings record</span></span>

1. <span data-ttu-id="8db0e-111">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps</span><span class="sxs-lookup"><span data-stu-id="8db0e-111">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps</span></span>

2. <span data-ttu-id="8db0e-112">Go to **Settings** > **My Apps** > **Unified Service Desk Administrator** app.</span><span class="sxs-lookup"><span data-stu-id="8db0e-112">Go to **Settings** > **My Apps** > **Unified Service Desk Administrator** app.</span></span>

3. <span data-ttu-id="8db0e-113">Select **Site Map**.</span><span class="sxs-lookup"><span data-stu-id="8db0e-113">Select **Site Map**.</span></span></br>
<span data-ttu-id="8db0e-114">![Select Site Map to go to Unified Interface Settings](../media/usd-crm-site-map-unified-interface-setting.PNG "Select Site Map to go to Unified Interface Settings")</span><span class="sxs-lookup"><span data-stu-id="8db0e-114">![Select Site Map to go to Unified Interface Settings](../media/usd-crm-site-map-unified-interface-setting.PNG "Select Site Map to go to Unified Interface Settings")</span></span>
 
4. <span data-ttu-id="8db0e-115">Choose **Unified Interface Settings** under **Advanced Settings**.</span><span class="sxs-lookup"><span data-stu-id="8db0e-115">Choose **Unified Interface Settings** under **Advanced Settings**.</span></span>

5. <span data-ttu-id="8db0e-116">In the **Active Unified Interface Settings** page, choose **+ New** to create a new record.</span><span class="sxs-lookup"><span data-stu-id="8db0e-116">In the **Active Unified Interface Settings** page, choose **+ New** to create a new record.</span></span>

6. <span data-ttu-id="8db0e-117">In the **New Unified Interface Settings** page, specify the following:</span><span class="sxs-lookup"><span data-stu-id="8db0e-117">In the **New Unified Interface Settings** page, specify the following:</span></span>

    | <span data-ttu-id="8db0e-118">Trường</span><span class="sxs-lookup"><span data-stu-id="8db0e-118">Field</span></span>  | <span data-ttu-id="8db0e-119">Value</span><span class="sxs-lookup"><span data-stu-id="8db0e-119">Value</span></span>  |
    |:----------|:----------|
    | <span data-ttu-id="8db0e-120">Tên</span><span class="sxs-lookup"><span data-stu-id="8db0e-120">Name</span></span>         | <span data-ttu-id="8db0e-121">Specify a name of the record.</span><span class="sxs-lookup"><span data-stu-id="8db0e-121">Specify a name of the record.</span></span></br> <span data-ttu-id="8db0e-122">For example, **Sample Setting**.</span><span class="sxs-lookup"><span data-stu-id="8db0e-122">For example, **Sample Setting**.</span></span> |
    | <span data-ttu-id="8db0e-123">Chủ đề</span><span class="sxs-lookup"><span data-stu-id="8db0e-123">Theme</span></span>        | <span data-ttu-id="8db0e-124">Select a theme for the App.</span><span class="sxs-lookup"><span data-stu-id="8db0e-124">Select a theme for the App.</span></span><br><span data-ttu-id="8db0e-125">There are two themes.</span><span class="sxs-lookup"><span data-stu-id="8db0e-125">There are two themes.</span></span><br><span data-ttu-id="8db0e-126">- Air</span><span class="sxs-lookup"><span data-stu-id="8db0e-126">- Air</span></span></br><span data-ttu-id="8db0e-127">- Unified Blue</span><span class="sxs-lookup"><span data-stu-id="8db0e-127">- Unified Blue</span></span> |
    | <span data-ttu-id="8db0e-128">Unified Interface App</span><span class="sxs-lookup"><span data-stu-id="8db0e-128">Unified Interface App</span></span> | <span data-ttu-id="8db0e-129">Select a Unified Interface App for the record.</span><span class="sxs-lookup"><span data-stu-id="8db0e-129">Select a Unified Interface App for the record.</span></span> </br> <span data-ttu-id="8db0e-130">For example, **Customer Service Hub**.</span><span class="sxs-lookup"><span data-stu-id="8db0e-130">For example, **Customer Service Hub**.</span></span>|
    | <span data-ttu-id="8db0e-131">Chủ sở hữu</span><span class="sxs-lookup"><span data-stu-id="8db0e-131">Owner</span></span> | <span data-ttu-id="8db0e-132">Add the user profile for the record by choosing the search icon.</span><span class="sxs-lookup"><span data-stu-id="8db0e-132">Add the user profile for the record by choosing the search icon.</span></span> |
    
  <span data-ttu-id="8db0e-133">![New Unified Interface Settings record](../media/usd-crm-unified-new-record-interface-settings.PNG "New Unified Interface Settings record")</span><span class="sxs-lookup"><span data-stu-id="8db0e-133">![New Unified Interface Settings record](../media/usd-crm-unified-new-record-interface-settings.PNG "New Unified Interface Settings record")</span></span>

7. <span data-ttu-id="8db0e-134">Chọn **Lưu & Đóng**.</span><span class="sxs-lookup"><span data-stu-id="8db0e-134">Select **Save & Close**.</span></span>

## <a name="add-the-unified-interface-settings-record-to-a-configuration"></a><span data-ttu-id="8db0e-135">Add the Unified Interface Settings record to a Configuration</span><span class="sxs-lookup"><span data-stu-id="8db0e-135">Add the Unified Interface Settings record to a Configuration</span></span>

<span data-ttu-id="8db0e-136">you can add the Unified Interface Settings record to a configuration in two ways:</span><span class="sxs-lookup"><span data-stu-id="8db0e-136">you can add the Unified Interface Settings record to a configuration in two ways:</span></span>

- <span data-ttu-id="8db0e-137">Assign a configuration the Unified Interface Settings page.</span><span class="sxs-lookup"><span data-stu-id="8db0e-137">Assign a configuration the Unified Interface Settings page.</span></span>
- <span data-ttu-id="8db0e-138">Assign a Unified Interface Setting record to a configuration.</span><span class="sxs-lookup"><span data-stu-id="8db0e-138">Assign a Unified Interface Setting record to a configuration.</span></span>

### <a name="assign-a-configuration-from-the-unified-interface-settings-page"></a><span data-ttu-id="8db0e-139">Assign a configuration from the Unified Interface Settings page</span><span class="sxs-lookup"><span data-stu-id="8db0e-139">Assign a configuration from the Unified Interface Settings page</span></span>

1. <span data-ttu-id="8db0e-140">Go to the Unified Interface Setting record for which you want to attach the configuration.</span><span class="sxs-lookup"><span data-stu-id="8db0e-140">Go to the Unified Interface Setting record for which you want to attach the configuration.</span></span>

2. <span data-ttu-id="8db0e-141">Choose **Related** > **Configuration**.</span><span class="sxs-lookup"><span data-stu-id="8db0e-141">Choose **Related** > **Configuration**.</span></span><br>
<span data-ttu-id="8db0e-142">![Add configuration to the unified interface setting record](../media/usd-crm-unified-interface-add-configuration.PNG "Add configuration to the unified interface setting records")</span><span class="sxs-lookup"><span data-stu-id="8db0e-142">![Add configuration to the unified interface setting record](../media/usd-crm-unified-interface-add-configuration.PNG "Add configuration to the unified interface setting records")</span></span>

3. <span data-ttu-id="8db0e-143">In the **Configuration** tab, select **Add Existing Configuration**.</span><span class="sxs-lookup"><span data-stu-id="8db0e-143">In the **Configuration** tab, select **Add Existing Configuration**.</span></span><br>
  > [!Note]
  > <span data-ttu-id="8db0e-144">You can select **Add New Configuration** to create and then add the configuration to the Unified Interface Settings record.</span><span class="sxs-lookup"><span data-stu-id="8db0e-144">You can select **Add New Configuration** to create and then add the configuration to the Unified Interface Settings record.</span></span> <span data-ttu-id="8db0e-145">In this walkthrough, we are attaching an already created configuration,**Test Configuration**, to the Unified Interface Settings record.</span><span class="sxs-lookup"><span data-stu-id="8db0e-145">In this walkthrough, we are attaching an already created configuration,**Test Configuration**, to the Unified Interface Settings record.</span></span>
  
4. <span data-ttu-id="8db0e-146">In the **Lookup Records** pane, specify the name of the configuration, and choose search icon.</span><span class="sxs-lookup"><span data-stu-id="8db0e-146">In the **Lookup Records** pane, specify the name of the configuration, and choose search icon.</span></span><br> <span data-ttu-id="8db0e-147">The configuration appears, choose the configuration and then choose **Add**.</span><span class="sxs-lookup"><span data-stu-id="8db0e-147">The configuration appears, choose the configuration and then choose **Add**.</span></span><br>
<span data-ttu-id="8db0e-148">![Add configuration to the unified interface setting record](../media/usd-crm-add-configuration-unified-interface-record.PNG "Add configuration to the unified interface setting records")</span><span class="sxs-lookup"><span data-stu-id="8db0e-148">![Add configuration to the unified interface setting record](../media/usd-crm-add-configuration-unified-interface-record.PNG "Add configuration to the unified interface setting records")</span></span>

<span data-ttu-id="8db0e-149">The configuration is added successfully and appears in the **Configuration** tab.</span><span class="sxs-lookup"><span data-stu-id="8db0e-149">The configuration is added successfully and appears in the **Configuration** tab.</span></span>

### <a name="assign-a-unified-interface-settings-record-in-the-configuration-page"></a><span data-ttu-id="8db0e-150">Assign a Unified Interface Settings record in the Configuration page</span><span class="sxs-lookup"><span data-stu-id="8db0e-150">Assign a Unified Interface Settings record in the Configuration page</span></span>

1. <span data-ttu-id="8db0e-151">Go to **Site Map** > **Configuration**.</span><span class="sxs-lookup"><span data-stu-id="8db0e-151">Go to **Site Map** > **Configuration**.</span></span>

2. <span data-ttu-id="8db0e-152">Select **+ New** to create a configuration record.</span><span class="sxs-lookup"><span data-stu-id="8db0e-152">Select **+ New** to create a configuration record.</span></span>

3. <span data-ttu-id="8db0e-153">In the **New Configuration** page, specify the required details for the fields.</span><span class="sxs-lookup"><span data-stu-id="8db0e-153">In the **New Configuration** page, specify the required details for the fields.</span></span> 

4. <span data-ttu-id="8db0e-154">In the **Unified Interface Settings** field, type the name of the existing Unified Interface record you want to assign, and choose the search icon.</span><span class="sxs-lookup"><span data-stu-id="8db0e-154">In the **Unified Interface Settings** field, type the name of the existing Unified Interface record you want to assign, and choose the search icon.</span></span><br> <span data-ttu-id="8db0e-155">Select the record when it appears..</span><span class="sxs-lookup"><span data-stu-id="8db0e-155">Select the record when it appears..</span></span><br>
<span data-ttu-id="8db0e-156">![Add unified interface setting record to the configuration](../media/usd-crm-add-unified-interface-record-configuration.PNG "Add unified interface setting record to the configuration")</span><span class="sxs-lookup"><span data-stu-id="8db0e-156">![Add unified interface setting record to the configuration](../media/usd-crm-add-unified-interface-record-configuration.PNG "Add unified interface setting record to the configuration")</span></span><br>
    >[!Note]
    > <span data-ttu-id="8db0e-157">In the above step, we added an existing Unified Interface Settings record to the configuration.</span><span class="sxs-lookup"><span data-stu-id="8db0e-157">In the above step, we added an existing Unified Interface Settings record to the configuration.</span></span> <span data-ttu-id="8db0e-158">To create a new Unified Interface Settings record, see [How to create Unified Interface Setting record](#how-to-create-unified-interface-setting-record).</span><span class="sxs-lookup"><span data-stu-id="8db0e-158">To create a new Unified Interface Settings record, see [How to create Unified Interface Setting record](#how-to-create-unified-interface-setting-record).</span></span>

5. <span data-ttu-id="8db0e-159">Select **Save & Close**.</span><span class="sxs-lookup"><span data-stu-id="8db0e-159">Select **Save & Close**.</span></span>

## <a name="login-experience-to-unified-service-desk"></a><span data-ttu-id="8db0e-160">Login experience to Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="8db0e-160">Login experience to Unified Service Desk</span></span> 

<span data-ttu-id="8db0e-161">Here are the scenarios you need to consider for signing in to Unified Service Desk.</span><span class="sxs-lookup"><span data-stu-id="8db0e-161">Here are the scenarios you need to consider for signing in to Unified Service Desk.</span></span>

### <a name="scenario-1-users-agents-assigned-to-configuration-with-a-unified-interface-settings-record"></a><span data-ttu-id="8db0e-162">Scenario 1: Users (agents) assigned to Configuration with a Unified Interface Settings record</span><span class="sxs-lookup"><span data-stu-id="8db0e-162">Scenario 1: Users (agents) assigned to Configuration with a Unified Interface Settings record</span></span>

<span data-ttu-id="8db0e-163">Add users (agents) to a **Configuration** and add a record to the **Unified Interface Settings** field in the **Configuration**.</span><span class="sxs-lookup"><span data-stu-id="8db0e-163">Add users (agents) to a **Configuration** and add a record to the **Unified Interface Settings** field in the **Configuration**.</span></span> <span data-ttu-id="8db0e-164">When the user (agent) added to the configuration signs in to Unified Service Desk, the system authenticates the user (agent) and displays the landing page of the Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="8db0e-164">When the user (agent) added to the configuration signs in to Unified Service Desk, the system authenticates the user (agent) and displays the landing page of the Unified Interface App.</span></span> 

### <a name="scenario-2-users-agents-assigned-to-configuration-without-a-unified-interface-settings-record"></a><span data-ttu-id="8db0e-165">Scenario 2: Users (agents) assigned to Configuration without a Unified Interface Settings record</span><span class="sxs-lookup"><span data-stu-id="8db0e-165">Scenario 2: Users (agents) assigned to Configuration without a Unified Interface Settings record</span></span>

<span data-ttu-id="8db0e-166">Add users (agents) to a **Configuration**, and the **Unified Interface Settings** field is empty in the **Configuration**.</span><span class="sxs-lookup"><span data-stu-id="8db0e-166">Add users (agents) to a **Configuration**, and the **Unified Interface Settings** field is empty in the **Configuration**.</span></span> <span data-ttu-id="8db0e-167">In this scenario consider three cases:</span><span class="sxs-lookup"><span data-stu-id="8db0e-167">In this scenario consider three cases:</span></span>

 - <span data-ttu-id="8db0e-168">If there is a default **Configuration** with a **Unified Interface Settings** record assigned, then the system authenticates the user (agent) and displays the landing page of Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="8db0e-168">If there is a default **Configuration** with a **Unified Interface Settings** record assigned, then the system authenticates the user (agent) and displays the landing page of Unified Interface App.</span></span>

 - <span data-ttu-id="8db0e-169">If there is a default **Configuration** with no **Unified Interface Settings** record, then during login, the system displays the application selection window for the user (agent) to select Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="8db0e-169">If there is a default **Configuration** with no **Unified Interface Settings** record, then during login, the system displays the application selection window for the user (agent) to select Unified Interface App.</span></span>

 - <span data-ttu-id="8db0e-170">If there is no default **Configuration**, then during login, the system displays the application selection window for the user (agent) to select Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="8db0e-170">If there is no default **Configuration**, then during login, the system displays the application selection window for the user (agent) to select Unified Interface App.</span></span>

### <a name="scenario-3-users-agents-assigned-to-configuration-and-unified-interface-settings-record-is-not-created"></a><span data-ttu-id="8db0e-171">Scenario 3: Users (agents) assigned to Configuration, and Unified Interface Settings record is not created</span><span class="sxs-lookup"><span data-stu-id="8db0e-171">Scenario 3: Users (agents) assigned to Configuration, and Unified Interface Settings record is not created</span></span>

<span data-ttu-id="8db0e-172">Add users (agents) to a **Configuration**, and no Unified Interface Settings records are created.</span><span class="sxs-lookup"><span data-stu-id="8db0e-172">Add users (agents) to a **Configuration**, and no Unified Interface Settings records are created.</span></span> <span data-ttu-id="8db0e-173">As a result, there are no records to select for the **Unified Interface Settings** field in the **Configuration**.</span><span class="sxs-lookup"><span data-stu-id="8db0e-173">As a result, there are no records to select for the **Unified Interface Settings** field in the **Configuration**.</span></span> <span data-ttu-id="8db0e-174">In this scenario, when the user (agent) assigned to a particular configuration signs in to Unified Service Desk, the application selection window is displayed and the user (agent) has to select the Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="8db0e-174">In this scenario, when the user (agent) assigned to a particular configuration signs in to Unified Service Desk, the application selection window is displayed and the user (agent) has to select the Unified Interface App.</span></span>


## <a name="see-also"></a><span data-ttu-id="8db0e-175">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="8db0e-175">See also</span></span>
 [<span data-ttu-id="8db0e-176">Unified Interface Page (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="8db0e-176">Unified Interface Page (Hosted Control)</span></span>](../../unified-service-desk/unified-interface-page-hosted-control.md)

 [<span data-ttu-id="8db0e-177">Unified Service Desk and Unified Interface Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="8db0e-177">Unified Service Desk and Unified Interface Configuration Walkthroughs</span></span>](../../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md)

 [<span data-ttu-id="8db0e-178">Walkthrough 1: Build a simple agent application for Unified Interface Apps</span><span class="sxs-lookup"><span data-stu-id="8db0e-178">Walkthrough 1: Build a simple agent application for Unified Interface Apps</span></span>](../../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) 

 [<span data-ttu-id="8db0e-179">Cách 2: Hiển thị trang web bên ngoài trong ứng dụng tổng đài viên của bạn</span><span class="sxs-lookup"><span data-stu-id="8db0e-179">Walkthrough 2: Display an external webpage in your agent application</span></span>](../../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md)  

 [<span data-ttu-id="8db0e-180">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application</span><span class="sxs-lookup"><span data-stu-id="8db0e-180">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application</span></span>](../../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)  

 [<span data-ttu-id="8db0e-181">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application</span><span class="sxs-lookup"><span data-stu-id="8db0e-181">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application</span></span>](../../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md)   

 [<span data-ttu-id="8db0e-182">Cách 5: Hiển thị thông tin phiên bổ sung bằng cách hiển thị tên và dữ liệu tổng quan về phiên</span><span class="sxs-lookup"><span data-stu-id="8db0e-182">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span></span>](../../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md)  

 [<span data-ttu-id="8db0e-183">Hướng 6: Đặt cấu hình kiểm soát tổ chức trình gỡ lỗi trong ứng dụng tổng đài viên của bạn</span><span class="sxs-lookup"><span data-stu-id="8db0e-183">Walkthrough 6: Configure the Debugger hosted control in your agent application</span></span>](../../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md)
 
 [<span data-ttu-id="8db0e-184">Cách 7: Đặt cấu hình mã lệnh tổng đài viên trong ứng dụng tổng đài viên của bạn</span><span class="sxs-lookup"><span data-stu-id="8db0e-184">Walkthrough 7: Configure agent scripting in your agent application</span></span>](../../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)
