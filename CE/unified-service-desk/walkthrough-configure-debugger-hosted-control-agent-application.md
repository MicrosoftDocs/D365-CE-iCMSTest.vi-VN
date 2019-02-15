---
title: 'Walkthrough 6: Configure the Debugger hosted control in your agent application | MicrosoftDocs'
description: ''
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
ms.assetid: 2d7bf294-165e-4beb-ac94-a9b1488f301e
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
ms.openlocfilehash: 37dacf9b90b769480a0852a23ba24f8729f6c609
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386573"
---
# <a name="walkthrough-6-configure-the-debugger-hosted-control-in-your-agent-application"></a><span data-ttu-id="361b6-102">Walkthrough 6: Configure the Debugger hosted control in your agent application</span><span class="sxs-lookup"><span data-stu-id="361b6-102">Walkthrough 6: Configure the Debugger hosted control in your agent application</span></span>
[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="361b6-103">provides a **Debugger** type of hosted control, which provides you key information about your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration that helps you to successfully build an agent application and troubleshoot issues in your configuration.</span><span class="sxs-lookup"><span data-stu-id="361b6-103">provides a **Debugger** type of hosted control, which provides you key information about your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration that helps you to successfully build an agent application and troubleshoot issues in your configuration.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="361b6-104">[Debug issues in Unified Service Desk](../unified-service-desk/debug-issues-unified-service-desk.md )</span><span class="sxs-lookup"><span data-stu-id="361b6-104">[Debug issues in Unified Service Desk](../unified-service-desk/debug-issues-unified-service-desk.md )</span></span>  

 <span data-ttu-id="361b6-105">This walkthrough demonstrates how to configure a Debugger hosted control for your agent application.</span><span class="sxs-lookup"><span data-stu-id="361b6-105">This walkthrough demonstrates how to configure a Debugger hosted control for your agent application.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="361b6-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="361b6-106">Prerequisites</span></span>  

- <span data-ttu-id="361b6-107">You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) and [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="361b6-107">You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) and [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md).</span></span> <span data-ttu-id="361b6-108">The configurations that you completed in those walkthroughs are required in this walkthrough.</span><span class="sxs-lookup"><span data-stu-id="361b6-108">The configurations that you completed in those walkthroughs are required in this walkthrough.</span></span>  

- <span data-ttu-id="361b6-109">Cách này giả định rằng bạn sẽ đang sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên ở cuối cách này để kiểm tra ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="361b6-109">This walkthrough assumes that you’ll be using the same user credential that you used in walkthrough 1 to sign in to the agent application at the end of the walkthrough to test the application.</span></span> <span data-ttu-id="361b6-110">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="361b6-110">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="361b6-111">[Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)</span><span class="sxs-lookup"><span data-stu-id="361b6-111">[Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)</span></span>  

- <span data-ttu-id="361b6-112">You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="361b6-112">You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  

  - <span data-ttu-id="361b6-113">Debugger hosted control.</span><span class="sxs-lookup"><span data-stu-id="361b6-113">Debugger hosted control.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="361b6-114">[Debugger (Hosted Control)](../unified-service-desk/debugger-hosted-control.md)</span><span class="sxs-lookup"><span data-stu-id="361b6-114">[Debugger (Hosted Control)](../unified-service-desk/debugger-hosted-control.md)</span></span>  

  - <span data-ttu-id="361b6-115">Action call and how to configure it.</span><span class="sxs-lookup"><span data-stu-id="361b6-115">Action call and how to configure it.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="361b6-116">[Action calls](../unified-service-desk/action-calls.md)</span><span class="sxs-lookup"><span data-stu-id="361b6-116">[Action calls](../unified-service-desk/action-calls.md)</span></span>  

  - <span data-ttu-id="361b6-117">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span><span class="sxs-lookup"><span data-stu-id="361b6-117">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="361b6-118">[Manage access using Unified Service Desk configuration](admin/manage-access-using-unified-service-desk-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="361b6-118">[Manage access using Unified Service Desk configuration](admin/manage-access-using-unified-service-desk-configuration.md)</span></span>  

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a><span data-ttu-id="361b6-119">In This Walkthrough</span><span class="sxs-lookup"><span data-stu-id="361b6-119">In This Walkthrough</span></span>  
 [<span data-ttu-id="361b6-120">Bước 1: Tạo loại trình gỡ lỗi của kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="361b6-120">Step 1: Create a Debugger type of hosted control</span></span>](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md#Step1)  

 [<span data-ttu-id="361b6-121">Bước 2: Thêm nút thanh công cụ và cuộc gọi hành động để hiển thị kiểm soát tổ chức trình gỡ lỗi</span><span class="sxs-lookup"><span data-stu-id="361b6-121">Step 2: Add toolbar button and action call to display the Debugger hosted control</span></span>](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md#Step2)  

 [<span data-ttu-id="361b6-122">Bước 3: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="361b6-122">Step 3: Add the controls to the configuration</span></span>](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md#Step3)  

 [<span data-ttu-id="361b6-123">Bước 4: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="361b6-123">Step 4: Test the application</span></span>](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md#Step4)  

 [<span data-ttu-id="361b6-124">Kết luận</span><span class="sxs-lookup"><span data-stu-id="361b6-124">Conclusion</span></span>](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md#conclusion)  

<a name="Step1"></a>   
## <a name="step-1-create-a-debugger-type-of-hosted-control"></a><span data-ttu-id="361b6-125">Step 1: Create a Debugger type of hosted control</span><span class="sxs-lookup"><span data-stu-id="361b6-125">Step 1: Create a Debugger type of hosted control</span></span>  

1. <span data-ttu-id="361b6-126">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="361b6-126">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="361b6-127">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="361b6-127">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="361b6-128">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="361b6-128">Click **New**.</span></span>  

5. <span data-ttu-id="361b6-129">On the **New Hosted Control** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="361b6-129">On the **New Hosted Control** page, specify the following values:</span></span>  

   |<span data-ttu-id="361b6-130">Trường</span><span class="sxs-lookup"><span data-stu-id="361b6-130">Field</span></span>|<span data-ttu-id="361b6-131">Giá trị</span><span class="sxs-lookup"><span data-stu-id="361b6-131">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="361b6-132">Tên</span><span class="sxs-lookup"><span data-stu-id="361b6-132">Name</span></span>|<span data-ttu-id="361b6-133">Trình gỡ lỗi Contoso</span><span class="sxs-lookup"><span data-stu-id="361b6-133">Contoso Debugger</span></span>|  
   |<span data-ttu-id="361b6-134">Thứ tự Sắp xếp</span><span class="sxs-lookup"><span data-stu-id="361b6-134">Sort Order</span></span>|<span data-ttu-id="361b6-135">3</span><span class="sxs-lookup"><span data-stu-id="361b6-135">3</span></span>|  
   |<span data-ttu-id="361b6-136">Tên hiển thị</span><span class="sxs-lookup"><span data-stu-id="361b6-136">Display Name</span></span>|<span data-ttu-id="361b6-137">Trình gỡ lỗi Contoso</span><span class="sxs-lookup"><span data-stu-id="361b6-137">Contoso Debugger</span></span>|  
   |<span data-ttu-id="361b6-138">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="361b6-138">USD Component Type</span></span>|<span data-ttu-id="361b6-139">Trình gỡ lỗi</span><span class="sxs-lookup"><span data-stu-id="361b6-139">Debugger</span></span>|  
   |<span data-ttu-id="361b6-140">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="361b6-140">Display Group</span></span>|<span data-ttu-id="361b6-141">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="361b6-141">MainPanel</span></span>|  

   <span data-ttu-id="361b6-142">![Create a Debugger hosted control](../unified-service-desk/media/usd-create-session-lines-hosted-control.png "Create a Debugger hosted control")</span><span class="sxs-lookup"><span data-stu-id="361b6-142">![Create a Debugger hosted control](../unified-service-desk/media/usd-create-session-lines-hosted-control.png "Create a Debugger hosted control")</span></span>  

6. <span data-ttu-id="361b6-143">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="361b6-143">Click **Save**.</span></span>  

<a name="Step2"></a>   
## <a name="step-2-add-toolbar-button-and-action-call-to-display-the-debugger-hosted-control"></a><span data-ttu-id="361b6-144">Step 2: Add toolbar button and action call to display the Debugger hosted control</span><span class="sxs-lookup"><span data-stu-id="361b6-144">Step 2: Add toolbar button and action call to display the Debugger hosted control</span></span>  
 <span data-ttu-id="361b6-145">Add a toolbar button to **Contoso Main Toolbar** (created in [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md)), and then add an action call for the button to display the **Contoso Debugger** hosted control that you created in step 1.</span><span class="sxs-lookup"><span data-stu-id="361b6-145">Add a toolbar button to **Contoso Main Toolbar** (created in [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md)), and then add an action call for the button to display the **Contoso Debugger** hosted control that you created in step 1.</span></span>  

1. <span data-ttu-id="361b6-146">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="361b6-146">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="361b6-147">Bấm vào **Thanh công cụ**.</span><span class="sxs-lookup"><span data-stu-id="361b6-147">Click **Toolbars**.</span></span>  

4. <span data-ttu-id="361b6-148">Click **Contoso Main Toolbar**.</span><span class="sxs-lookup"><span data-stu-id="361b6-148">Click **Contoso Main Toolbar**.</span></span>  

5. <span data-ttu-id="361b6-149">In the **Buttons** area, click **+** to add a toolbar button.</span><span class="sxs-lookup"><span data-stu-id="361b6-149">In the **Buttons** area, click **+** to add a toolbar button.</span></span>  

6. <span data-ttu-id="361b6-150">On the **New Toolbar Button** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="361b6-150">On the **New Toolbar Button** page, specify the following values.</span></span>  


   |    <span data-ttu-id="361b6-151">Trường</span><span class="sxs-lookup"><span data-stu-id="361b6-151">Field</span></span>    |                                                                              <span data-ttu-id="361b6-152">Value</span><span class="sxs-lookup"><span data-stu-id="361b6-152">Value</span></span>                                                                               |
   |-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    <span data-ttu-id="361b6-153">Tên</span><span class="sxs-lookup"><span data-stu-id="361b6-153">Name</span></span>     |                                                                     <span data-ttu-id="361b6-154">Contoso Debugger Button</span><span class="sxs-lookup"><span data-stu-id="361b6-154">Contoso Debugger Button</span></span>                                                                      |
   | <span data-ttu-id="361b6-155">Văn bản nút</span><span class="sxs-lookup"><span data-stu-id="361b6-155">Button Text</span></span> |                                                                             <span data-ttu-id="361b6-156">TRÌNH GỠ LỖI</span><span class="sxs-lookup"><span data-stu-id="361b6-156">DEBUGGER</span></span>                                                                             |
   |    <span data-ttu-id="361b6-157">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="361b6-157">Order</span></span>    | <span data-ttu-id="361b6-158">3 **Note:**  The **Order** field defines the position of buttons in the toolbar.</span><span class="sxs-lookup"><span data-stu-id="361b6-158">3 **Note:**  The **Order** field defines the position of buttons in the toolbar.</span></span> <span data-ttu-id="361b6-159">Buttons are arranged from left to right or top to bottom in an ascending order.</span><span class="sxs-lookup"><span data-stu-id="361b6-159">Buttons are arranged from left to right or top to bottom in an ascending order.</span></span> |


7. <span data-ttu-id="361b6-160">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="361b6-160">Click **Save**.</span></span>  

8. <span data-ttu-id="361b6-161">In the **Actions** area, click **+** to create an action call for the button</span><span class="sxs-lookup"><span data-stu-id="361b6-161">In the **Actions** area, click **+** to create an action call for the button</span></span>  

9. <span data-ttu-id="361b6-162">In the search box, press **ENTER** or click the search icon, and then click **New** in the lower-right corner of the search results pane to create an action call.</span><span class="sxs-lookup"><span data-stu-id="361b6-162">In the search box, press **ENTER** or click the search icon, and then click **New** in the lower-right corner of the search results pane to create an action call.</span></span>  

10. <span data-ttu-id="361b6-163">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="361b6-163">On the **New Action Call** page, specify the following values.</span></span>  

    |<span data-ttu-id="361b6-164">Trường</span><span class="sxs-lookup"><span data-stu-id="361b6-164">Field</span></span>|<span data-ttu-id="361b6-165">Giá trị</span><span class="sxs-lookup"><span data-stu-id="361b6-165">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="361b6-166">Tên</span><span class="sxs-lookup"><span data-stu-id="361b6-166">Name</span></span>|<span data-ttu-id="361b6-167">Cuộc gọi hành động Contoso: Hiển thị Trình gỡ lỗi</span><span class="sxs-lookup"><span data-stu-id="361b6-167">Contoso Action Call: Show Debugger</span></span>|  
    |<span data-ttu-id="361b6-168">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="361b6-168">Order</span></span>|<span data-ttu-id="361b6-169">1</span><span class="sxs-lookup"><span data-stu-id="361b6-169">1</span></span>|  
    |<span data-ttu-id="361b6-170">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="361b6-170">Hosted Control</span></span>|<span data-ttu-id="361b6-171">Trình quản lý chung contoso</span><span class="sxs-lookup"><span data-stu-id="361b6-171">Contoso Global Manager</span></span>|  
    |<span data-ttu-id="361b6-172">Hành động</span><span class="sxs-lookup"><span data-stu-id="361b6-172">Action</span></span>|<span data-ttu-id="361b6-173">CallDoAction</span><span class="sxs-lookup"><span data-stu-id="361b6-173">CallDoAction</span></span>|  
    |<span data-ttu-id="361b6-174">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="361b6-174">Data</span></span>|<span data-ttu-id="361b6-175">action=default</span><span class="sxs-lookup"><span data-stu-id="361b6-175">action=default</span></span><br /><span data-ttu-id="361b6-176">application=Contoso Debugger</span><span class="sxs-lookup"><span data-stu-id="361b6-176">application=Contoso Debugger</span></span>|  

    <span data-ttu-id="361b6-177">![Create action call in Unified Service Desk](../unified-service-desk/media/usd-session-tab-name-format.png "Create action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="361b6-177">![Create action call in Unified Service Desk](../unified-service-desk/media/usd-session-tab-name-format.png "Create action call in Unified Service Desk")</span></span>  

11. <span data-ttu-id="361b6-178">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="361b6-178">Click **Save**.</span></span>  

<a name="Step3"></a>   
## <a name="step-3-add-the-controls-to-the-configuration"></a><span data-ttu-id="361b6-179">Step 3: Add the controls to the configuration</span><span class="sxs-lookup"><span data-stu-id="361b6-179">Step 3: Add the controls to the configuration</span></span>  
 <span data-ttu-id="361b6-180">Add the action call and hosted control that you created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span><span class="sxs-lookup"><span data-stu-id="361b6-180">Add the action call and hosted control that you created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span></span> <span data-ttu-id="361b6-181">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="361b6-181">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span>  

 <span data-ttu-id="361b6-182">Add the following to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="361b6-182">Add the following to **Contoso Configuration**.</span></span>  

|<span data-ttu-id="361b6-183">Tên kiểm soát</span><span class="sxs-lookup"><span data-stu-id="361b6-183">Control name</span></span>|<span data-ttu-id="361b6-184">Loại kiểm soát</span><span class="sxs-lookup"><span data-stu-id="361b6-184">Control type</span></span>|  
|------------------|------------------|  
|<span data-ttu-id="361b6-185">Cuộc gọi hành động Contoso: Hiển thị Trình gỡ lỗi</span><span class="sxs-lookup"><span data-stu-id="361b6-185">Contoso Action Call: Show Debugger</span></span>|<span data-ttu-id="361b6-186">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="361b6-186">Action Call</span></span>|  
|<span data-ttu-id="361b6-187">Trình gỡ lỗi Contoso</span><span class="sxs-lookup"><span data-stu-id="361b6-187">Contoso Debugger</span></span>|<span data-ttu-id="361b6-188">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="361b6-188">Hosted Control</span></span>|  

 <span data-ttu-id="361b6-189">To add a control to the configuration:</span><span class="sxs-lookup"><span data-stu-id="361b6-189">To add a control to the configuration:</span></span>  

1. <span data-ttu-id="361b6-190">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="361b6-190">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="361b6-191">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="361b6-191">Click **Configuration**.</span></span>  

4. <span data-ttu-id="361b6-192">Click **Contoso Configuration** to open the definition.</span><span class="sxs-lookup"><span data-stu-id="361b6-192">Click **Contoso Configuration** to open the definition.</span></span>  

5. <span data-ttu-id="361b6-193">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="361b6-193">On the nav bar, click the down arrow next to **Contoso Configuration**, and select **Action Calls**.</span></span>  

6. <span data-ttu-id="361b6-194">On the next page, click **Add Existing Action Call**, type “`Contoso Action Call: Show Debugger`” in the search bar, and then press ENTER or click the search icon.</span><span class="sxs-lookup"><span data-stu-id="361b6-194">On the next page, click **Add Existing Action Call**, type “`Contoso Action Call: Show Debugger`” in the search bar, and then press ENTER or click the search icon.</span></span>  

7. <span data-ttu-id="361b6-195">In the search results, click the action call name to add it.</span><span class="sxs-lookup"><span data-stu-id="361b6-195">In the search results, click the action call name to add it.</span></span>  

8. <span data-ttu-id="361b6-196">Similarly, add the hosted control by clicking the down arrow next to **Contoso Configuration**, and clicking **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="361b6-196">Similarly, add the hosted control by clicking the down arrow next to **Contoso Configuration**, and clicking **Hosted Controls**.</span></span>  

9. <span data-ttu-id="361b6-197">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="361b6-197">Click **Save**.</span></span>  

<a name="Step4"></a>   
## <a name="step-4-test-the-application"></a><span data-ttu-id="361b6-198">Step 4: Test the application</span><span class="sxs-lookup"><span data-stu-id="361b6-198">Step 4: Test the application</span></span>  
 <span data-ttu-id="361b6-199">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="361b6-199">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span> <span data-ttu-id="361b6-200">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span><span class="sxs-lookup"><span data-stu-id="361b6-200">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span></span>  

 <span data-ttu-id="361b6-201">Your agent application will now have a **DEBUGGER** button in the toolbar area.</span><span class="sxs-lookup"><span data-stu-id="361b6-201">Your agent application will now have a **DEBUGGER** button in the toolbar area.</span></span> <span data-ttu-id="361b6-202">Clicking this button displays the Debugger control.</span><span class="sxs-lookup"><span data-stu-id="361b6-202">Clicking this button displays the Debugger control.</span></span>  

 <span data-ttu-id="361b6-203">![Debugger in your agent application](../unified-service-desk/media/usd-debugger-agent-application.png "Debugger in your agent application")</span><span class="sxs-lookup"><span data-stu-id="361b6-203">![Debugger in your agent application](../unified-service-desk/media/usd-debugger-agent-application.png "Debugger in your agent application")</span></span>  

<a name="conclusion"></a>   
## <a name="conclusion"></a><span data-ttu-id="361b6-204">Kết luận</span><span class="sxs-lookup"><span data-stu-id="361b6-204">Conclusion</span></span>  
 <span data-ttu-id="361b6-205">In this walkthrough, you saw how to configure the Debugger hosted control in your agent application.</span><span class="sxs-lookup"><span data-stu-id="361b6-205">In this walkthrough, you saw how to configure the Debugger hosted control in your agent application.</span></span> <span data-ttu-id="361b6-206">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span><span class="sxs-lookup"><span data-stu-id="361b6-206">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span></span>  

### <a name="see-also"></a><span data-ttu-id="361b6-207">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="361b6-207">See also</span></span>  

 [<span data-ttu-id="361b6-208">Walkthrough 1: Build a simple agent application</span><span class="sxs-lookup"><span data-stu-id="361b6-208">Walkthrough 1: Build a simple agent application</span></span>](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)   

 [<span data-ttu-id="361b6-209">Walkthrough 2: Display an external webpage in your agent application</span><span class="sxs-lookup"><span data-stu-id="361b6-209">Walkthrough 2: Display an external webpage in your agent application</span></span>](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md)   

 [<span data-ttu-id="361b6-210">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application</span><span class="sxs-lookup"><span data-stu-id="361b6-210">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application</span></span>](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md)   

 [<span data-ttu-id="361b6-211">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application</span><span class="sxs-lookup"><span data-stu-id="361b6-211">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application</span></span>](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md)   

 [<span data-ttu-id="361b6-212">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span><span class="sxs-lookup"><span data-stu-id="361b6-212">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span></span>](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md)   

 [<span data-ttu-id="361b6-213">Walkthrough 7: Configure agent scripting in your agent application</span><span class="sxs-lookup"><span data-stu-id="361b6-213">Walkthrough 7: Configure agent scripting in your agent application</span></span>](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md)   

 [<span data-ttu-id="361b6-214">Unified Service Desk Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="361b6-214">Unified Service Desk Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
