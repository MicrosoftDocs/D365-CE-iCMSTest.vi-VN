---
title: 'Walkthrough 6: Configure the Debugger hosted control in your agent application | MicrosoftDocs'
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
ms.assetid: B87B63D0-7BE3-4B43-806A-29429D9DE75A
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
ms.openlocfilehash: 65a46785236e8b187a190b7e7aef3e16176cf989
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385539"
---
# <a name="walkthrough-6-configure-the-debugger-hosted-control-in-your-agent-application"></a><span data-ttu-id="0c57a-102">Walkthrough 6: Configure the Debugger hosted control in your agent application</span><span class="sxs-lookup"><span data-stu-id="0c57a-102">Walkthrough 6: Configure the Debugger hosted control in your agent application</span></span>
[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]<span data-ttu-id="0c57a-103">cung cấp loại **trình gỡ lỗi** của kiểm soát tổ chức, cung cấp cho bạn thông tin quan trọng về cấu hình [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] của bạn mà sẽ giúp bạn xây dựng thành công ứng dụng tổng đài viên và khắc phục sự cố trong cấu hình của bạn.</span><span class="sxs-lookup"><span data-stu-id="0c57a-103">provides a **Debugger** type of hosted control, which provides you key information about your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration that helps you to successfully build an agent application and troubleshoot issues in your configuration.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0c57a-104">[Debug issues in Unified Service Desk](../unified-service-desk/debug-issues-unified-service-desk.md )</span><span class="sxs-lookup"><span data-stu-id="0c57a-104">[Debug issues in Unified Service Desk](../unified-service-desk/debug-issues-unified-service-desk.md )</span></span>  

 <span data-ttu-id="0c57a-105">Cách này trình bày cách cấu hình kiểm soát tổ chức trình gỡ lỗi cho ứng dụng tổng đài viên của bạn.</span><span class="sxs-lookup"><span data-stu-id="0c57a-105">This walkthrough demonstrates how to configure a Debugger hosted control for your agent application.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="0c57a-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="0c57a-106">Prerequisites</span></span>  

- <span data-ttu-id="0c57a-107">You must have completed [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) and [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="0c57a-107">You must have completed [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) and [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md).</span></span> <span data-ttu-id="0c57a-108">Các cấu hình mà bạn hoàn thành trong các cách này được yêu cầu trong cách này.</span><span class="sxs-lookup"><span data-stu-id="0c57a-108">The configurations that you completed in those walkthroughs are required in this walkthrough.</span></span>  

- <span data-ttu-id="0c57a-109">Cách này giả định rằng bạn sẽ đang sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên ở cuối cách này để kiểm tra ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="0c57a-109">This walkthrough assumes that you’ll be using the same user credential that you used in walkthrough 1 to sign in to the agent application at the end of the walkthrough to test the application.</span></span> <span data-ttu-id="0c57a-110">Nếu một người dùng khác sẽ thử nghiệm các ứng dụng, bạn phải gán người dùng vào **Cấu hình Contoso**.</span><span class="sxs-lookup"><span data-stu-id="0c57a-110">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0c57a-111">[Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)</span><span class="sxs-lookup"><span data-stu-id="0c57a-111">[Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)</span></span>  

- <span data-ttu-id="0c57a-112">You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="0c57a-112">You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  

  - <span data-ttu-id="0c57a-113">Kiểm soát tổ chức trình gỡ lỗi.</span><span class="sxs-lookup"><span data-stu-id="0c57a-113">Debugger hosted control.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0c57a-114">[Debugger (Hosted Control)](../unified-service-desk/debugger-hosted-control.md)</span><span class="sxs-lookup"><span data-stu-id="0c57a-114">[Debugger (Hosted Control)](../unified-service-desk/debugger-hosted-control.md)</span></span>  

  - <span data-ttu-id="0c57a-115">Action call and how to configure it.</span><span class="sxs-lookup"><span data-stu-id="0c57a-115">Action call and how to configure it.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0c57a-116">[Action calls](../unified-service-desk/action-calls.md)</span><span class="sxs-lookup"><span data-stu-id="0c57a-116">[Action calls](../unified-service-desk/action-calls.md)</span></span>  

  - <span data-ttu-id="0c57a-117">Lọc quyền truy cập bằng cách sử dụng cấu hình [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="0c57a-117">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0c57a-118">[Manage access using Unified Service Desk configuration](admin/manage-access-using-unified-service-desk-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="0c57a-118">[Manage access using Unified Service Desk configuration](admin/manage-access-using-unified-service-desk-configuration.md)</span></span>  

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a><span data-ttu-id="0c57a-119">In This Walkthrough</span><span class="sxs-lookup"><span data-stu-id="0c57a-119">In This Walkthrough</span></span>  
 [<span data-ttu-id="0c57a-120">Bước 1: Tạo loại trình gỡ lỗi của kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="0c57a-120">Step 1: Create a Debugger type of hosted control</span></span>](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md#Step1)  

 [<span data-ttu-id="0c57a-121">Bước 2: Thêm nút thanh công cụ và cuộc gọi hành động để hiển thị kiểm soát tổ chức trình gỡ lỗi</span><span class="sxs-lookup"><span data-stu-id="0c57a-121">Step 2: Add toolbar button and action call to display the Debugger hosted control</span></span>](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md#Step2)  

 [<span data-ttu-id="0c57a-122">Bước 3: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="0c57a-122">Step 3: Add the controls to the configuration</span></span>](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md#Step3)  

 [<span data-ttu-id="0c57a-123">Bước 4: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="0c57a-123">Step 4: Test the application</span></span>](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md#Step4)  

 [<span data-ttu-id="0c57a-124">Kết luận</span><span class="sxs-lookup"><span data-stu-id="0c57a-124">Conclusion</span></span>](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md#conclusion)  

<a name="Step1"></a>   
## <a name="step-1-create-a-debugger-type-of-hosted-control"></a><span data-ttu-id="0c57a-125">Bước 1: Tạo loại trình gỡ lỗi của kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="0c57a-125">Step 1: Create a Debugger type of hosted control</span></span>  

1. <span data-ttu-id="0c57a-126">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="0c57a-126">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="0c57a-127">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="0c57a-127">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="0c57a-128">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="0c57a-128">Click **New**.</span></span>  

5. <span data-ttu-id="0c57a-129">On the **New Hosted Control** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="0c57a-129">On the **New Hosted Control** page, specify the following values:</span></span>  

   |<span data-ttu-id="0c57a-130">Trường</span><span class="sxs-lookup"><span data-stu-id="0c57a-130">Field</span></span>|<span data-ttu-id="0c57a-131">Giá trị</span><span class="sxs-lookup"><span data-stu-id="0c57a-131">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="0c57a-132">Tên</span><span class="sxs-lookup"><span data-stu-id="0c57a-132">Name</span></span>|<span data-ttu-id="0c57a-133">Trình gỡ lỗi Contoso</span><span class="sxs-lookup"><span data-stu-id="0c57a-133">Contoso Debugger</span></span>|  
   |<span data-ttu-id="0c57a-134">Thứ tự Sắp xếp</span><span class="sxs-lookup"><span data-stu-id="0c57a-134">Sort Order</span></span>|<span data-ttu-id="0c57a-135">3</span><span class="sxs-lookup"><span data-stu-id="0c57a-135">3</span></span>|  
   |<span data-ttu-id="0c57a-136">Tên hiển thị</span><span class="sxs-lookup"><span data-stu-id="0c57a-136">Display Name</span></span>|<span data-ttu-id="0c57a-137">Trình gỡ lỗi Contoso</span><span class="sxs-lookup"><span data-stu-id="0c57a-137">Contoso Debugger</span></span>|  
   |<span data-ttu-id="0c57a-138">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="0c57a-138">USD Component Type</span></span>|<span data-ttu-id="0c57a-139">Trình gỡ lỗi</span><span class="sxs-lookup"><span data-stu-id="0c57a-139">Debugger</span></span>|  
   |<span data-ttu-id="0c57a-140">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="0c57a-140">Display Group</span></span>|<span data-ttu-id="0c57a-141">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="0c57a-141">MainPanel</span></span>|  

   <span data-ttu-id="0c57a-142">![Create a Debugger hosted control](../unified-service-desk/media/usd-create-debugger-hosted-control-unified-interface.png "Create a Debugger hosted control")</span><span class="sxs-lookup"><span data-stu-id="0c57a-142">![Create a Debugger hosted control](../unified-service-desk/media/usd-create-debugger-hosted-control-unified-interface.png "Create a Debugger hosted control")</span></span>  

6. <span data-ttu-id="0c57a-143">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="0c57a-143">Click **Save**.</span></span>  

<a name="Step2"></a>   
## <a name="step-2-add-toolbar-button-and-action-call-to-display-the-debugger-hosted-control"></a><span data-ttu-id="0c57a-144">Bước 2: Thêm nút thanh công cụ và cuộc gọi hành động để hiển thị kiểm soát tổ chức trình gỡ lỗi</span><span class="sxs-lookup"><span data-stu-id="0c57a-144">Step 2: Add toolbar button and action call to display the Debugger hosted control</span></span>  
 <span data-ttu-id="0c57a-145">Add a toolbar button to **Contoso Main Toolbar** (created in [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)), and then add an action call for the button to display the **Contoso Debugger** hosted control that you created in step 1.</span><span class="sxs-lookup"><span data-stu-id="0c57a-145">Add a toolbar button to **Contoso Main Toolbar** (created in [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)), and then add an action call for the button to display the **Contoso Debugger** hosted control that you created in step 1.</span></span>  

1. <span data-ttu-id="0c57a-146">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="0c57a-146">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="0c57a-147">Bấm vào **Thanh công cụ**.</span><span class="sxs-lookup"><span data-stu-id="0c57a-147">Click **Toolbars**.</span></span>  

4. <span data-ttu-id="0c57a-148">Bấm vào **Thanh công cụ chính Contoso**.</span><span class="sxs-lookup"><span data-stu-id="0c57a-148">Click **Contoso Main Toolbar**.</span></span>  

5. <span data-ttu-id="0c57a-149">In the **Buttons** area, click **+** to add a toolbar button.</span><span class="sxs-lookup"><span data-stu-id="0c57a-149">In the **Buttons** area, click **+** to add a toolbar button.</span></span>  

6. <span data-ttu-id="0c57a-150">On the **New Toolbar Button** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="0c57a-150">On the **New Toolbar Button** page, specify the following values.</span></span>  


   |    <span data-ttu-id="0c57a-151">Trường</span><span class="sxs-lookup"><span data-stu-id="0c57a-151">Field</span></span>    |                                                                                <span data-ttu-id="0c57a-152">Value</span><span class="sxs-lookup"><span data-stu-id="0c57a-152">Value</span></span>                                                                                 |
   |-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    <span data-ttu-id="0c57a-153">Tên</span><span class="sxs-lookup"><span data-stu-id="0c57a-153">Name</span></span>     |                                                                       <span data-ttu-id="0c57a-154">Nút Trình gỡ lỗi Contoso</span><span class="sxs-lookup"><span data-stu-id="0c57a-154">Contoso Debugger Button</span></span>                                                                        |
   | <span data-ttu-id="0c57a-155">Văn bản nút</span><span class="sxs-lookup"><span data-stu-id="0c57a-155">Button Text</span></span> |                                                                               <span data-ttu-id="0c57a-156">TRÌNH GỠ LỖI</span><span class="sxs-lookup"><span data-stu-id="0c57a-156">DEBUGGER</span></span>                                                                               |
   |    <span data-ttu-id="0c57a-157">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="0c57a-157">Order</span></span>    | <span data-ttu-id="0c57a-158">3</span><span class="sxs-lookup"><span data-stu-id="0c57a-158">3</span></span> <br> <span data-ttu-id="0c57a-159">**Note:** The **Order** field defines the position of buttons in the toolbar.</span><span class="sxs-lookup"><span data-stu-id="0c57a-159">**Note:** The **Order** field defines the position of buttons in the toolbar.</span></span> <span data-ttu-id="0c57a-160">Buttons are arranged from left to right or top to bottom in an ascending order.</span><span class="sxs-lookup"><span data-stu-id="0c57a-160">Buttons are arranged from left to right or top to bottom in an ascending order.</span></span> |


7. <span data-ttu-id="0c57a-161">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="0c57a-161">Click **Save**.</span></span>  

8. <span data-ttu-id="0c57a-162">In the **Actions** area, click **+** to create an action call for the button</span><span class="sxs-lookup"><span data-stu-id="0c57a-162">In the **Actions** area, click **+** to create an action call for the button</span></span>  

9. <span data-ttu-id="0c57a-163">Trong hộp tìm kiếm, nhấn **ENTER** hoặc nhấp vào biểu tượng tìm kiếm, và sau đó nhấp vào **Mới** ở góc dưới bên phải của ngăn kết quả tìm kiếm để tạo cuộc gọi hành động.</span><span class="sxs-lookup"><span data-stu-id="0c57a-163">In the search box, press **ENTER** or click the search icon, and then click **New** in the lower-right corner of the search results pane to create an action call.</span></span>  

10. <span data-ttu-id="0c57a-164">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="0c57a-164">On the **New Action Call** page, specify the following values.</span></span>  

    |<span data-ttu-id="0c57a-165">Trường</span><span class="sxs-lookup"><span data-stu-id="0c57a-165">Field</span></span>|<span data-ttu-id="0c57a-166">Giá trị</span><span class="sxs-lookup"><span data-stu-id="0c57a-166">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="0c57a-167">Tên</span><span class="sxs-lookup"><span data-stu-id="0c57a-167">Name</span></span>|<span data-ttu-id="0c57a-168">Cuộc gọi hành động Contoso: Hiển thị Trình gỡ lỗi</span><span class="sxs-lookup"><span data-stu-id="0c57a-168">Contoso Action Call: Show Debugger</span></span>|  
    |<span data-ttu-id="0c57a-169">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="0c57a-169">Order</span></span>|<span data-ttu-id="0c57a-170">1</span><span class="sxs-lookup"><span data-stu-id="0c57a-170">1</span></span>|  
    |<span data-ttu-id="0c57a-171">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="0c57a-171">Hosted Control</span></span>|<span data-ttu-id="0c57a-172">Trình quản lý chung contoso</span><span class="sxs-lookup"><span data-stu-id="0c57a-172">Contoso Global Manager</span></span>|  
    |<span data-ttu-id="0c57a-173">Hành động</span><span class="sxs-lookup"><span data-stu-id="0c57a-173">Action</span></span>|<span data-ttu-id="0c57a-174">CallDoAction</span><span class="sxs-lookup"><span data-stu-id="0c57a-174">CallDoAction</span></span>|  
    |<span data-ttu-id="0c57a-175">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="0c57a-175">Data</span></span>|<span data-ttu-id="0c57a-176">action=default</span><span class="sxs-lookup"><span data-stu-id="0c57a-176">action=default</span></span><br/><span data-ttu-id="0c57a-177">application=Contoso Debugger</span><span class="sxs-lookup"><span data-stu-id="0c57a-177">application=Contoso Debugger</span></span>|  

    <span data-ttu-id="0c57a-178">![Create action call in Unified Service Desk](../unified-service-desk/media/usd-session-tab-name-format-action-call-unified-interface.png "Create action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="0c57a-178">![Create action call in Unified Service Desk](../unified-service-desk/media/usd-session-tab-name-format-action-call-unified-interface.png "Create action call in Unified Service Desk")</span></span>  

11. <span data-ttu-id="0c57a-179">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="0c57a-179">Click **Save**.</span></span>  

<a name="Step3"></a>   
## <a name="step-3-add-the-controls-to-the-configuration"></a><span data-ttu-id="0c57a-180">Bước 3: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="0c57a-180">Step 3: Add the controls to the configuration</span></span>  
 <span data-ttu-id="0c57a-181">Thêm cuộc gọi hành động và kiểm soát tổ chức mà bạn đã tạo trong cách này vào **Cấu hình Contoso** để hiển thị các kiểm soát này cho người dùng được chỉ định cho cấu hình này.</span><span class="sxs-lookup"><span data-stu-id="0c57a-181">Add the action call and hosted control that you created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span></span> <span data-ttu-id="0c57a-182">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="0c57a-182">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span></span>  

 <span data-ttu-id="0c57a-183">Add the following to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="0c57a-183">Add the following to **Contoso Configuration**.</span></span>  

|<span data-ttu-id="0c57a-184">Tên kiểm soát</span><span class="sxs-lookup"><span data-stu-id="0c57a-184">Control name</span></span>|<span data-ttu-id="0c57a-185">Loại kiểm soát</span><span class="sxs-lookup"><span data-stu-id="0c57a-185">Control type</span></span>|  
|------------------|------------------|  
|<span data-ttu-id="0c57a-186">Cuộc gọi hành động Contoso: Hiển thị Trình gỡ lỗi</span><span class="sxs-lookup"><span data-stu-id="0c57a-186">Contoso Action Call: Show Debugger</span></span>|<span data-ttu-id="0c57a-187">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="0c57a-187">Action Call</span></span>|  
|<span data-ttu-id="0c57a-188">Trình gỡ lỗi Contoso</span><span class="sxs-lookup"><span data-stu-id="0c57a-188">Contoso Debugger</span></span>|<span data-ttu-id="0c57a-189">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="0c57a-189">Hosted Control</span></span>|  

 <span data-ttu-id="0c57a-190">To add a control to the configuration:</span><span class="sxs-lookup"><span data-stu-id="0c57a-190">To add a control to the configuration:</span></span>  

1. <span data-ttu-id="0c57a-191">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="0c57a-191">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="0c57a-192">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="0c57a-192">Click **Configuration**.</span></span>  

4. <span data-ttu-id="0c57a-193">Click **Contoso Configuration** to open the definition.</span><span class="sxs-lookup"><span data-stu-id="0c57a-193">Click **Contoso Configuration** to open the definition.</span></span>  

5. <span data-ttu-id="0c57a-194">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="0c57a-194">On the nav bar, click the down arrow next to **Contoso Configuration**, and select **Action Calls**.</span></span>  

6. <span data-ttu-id="0c57a-195">Trên trang tiếp theo, bấm vào **Thêm Cuộc gọi Hành động Hiện có**, nhập “`Contoso Action Call: Show Debugger`” vào thanh tìm kiếm, sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="0c57a-195">On the next page, click **Add Existing Action Call**, type “`Contoso Action Call: Show Debugger`” in the search bar, and then press ENTER or click the search icon.</span></span>  

7. <span data-ttu-id="0c57a-196">In the search results, click the action call name to add it.</span><span class="sxs-lookup"><span data-stu-id="0c57a-196">In the search results, click the action call name to add it.</span></span>  

8. <span data-ttu-id="0c57a-197">Tương tự, thêm kiểm soát tổ chức bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Kiểm soát tổ chức**.</span><span class="sxs-lookup"><span data-stu-id="0c57a-197">Similarly, add the hosted control by clicking the down arrow next to **Contoso Configuration**, and clicking **Hosted Controls**.</span></span> 

9. <span data-ttu-id="0c57a-198">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="0c57a-198">Click **Save**.</span></span>  

<a name="Step4"></a>   
## <a name="step-4-test-the-application"></a><span data-ttu-id="0c57a-199">Bước 4: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="0c57a-199">Step 4: Test the application</span></span>  
 <span data-ttu-id="0c57a-200">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="0c57a-200">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span></span> <span data-ttu-id="0c57a-201">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span><span class="sxs-lookup"><span data-stu-id="0c57a-201">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span></span>  

 <span data-ttu-id="0c57a-202">Ứng dụng tổng đài viên của bạn bây giờ sẽ có nút **TRÌNH GỠ LỖI** trong vùng thanh công cụ.</span><span class="sxs-lookup"><span data-stu-id="0c57a-202">Your agent application will now have a **DEBUGGER** button in the toolbar area.</span></span> <span data-ttu-id="0c57a-203">Bấm nút này sẽ hiển thị kiểm soát trình gỡ lỗi.</span><span class="sxs-lookup"><span data-stu-id="0c57a-203">Clicking this button displays the Debugger control.</span></span>  

 <span data-ttu-id="0c57a-204">![Debugger in your agent application](../unified-service-desk/media/usd-debugger-agent-application.png "Debugger in your agent application")</span><span class="sxs-lookup"><span data-stu-id="0c57a-204">![Debugger in your agent application](../unified-service-desk/media/usd-debugger-agent-application.png "Debugger in your agent application")</span></span>  

<a name="conclusion"></a>  
## <a name="conclusion"></a><span data-ttu-id="0c57a-205">Kết luận</span><span class="sxs-lookup"><span data-stu-id="0c57a-205">Conclusion</span></span> 
 <span data-ttu-id="0c57a-206">Trong cách này, bạn sẽ biết cách cấu hình kiểm soát tổ chức trình gỡ lỗi trong ứng dụng tổng đài viên của bạn.</span><span class="sxs-lookup"><span data-stu-id="0c57a-206">In this walkthrough, you saw how to configure the Debugger hosted control in your agent application.</span></span> <span data-ttu-id="0c57a-207">Bạn cũng biết cách lọc quyền truy cập vào kiểm soát [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] bằng cách sử dụng cấu hình.</span><span class="sxs-lookup"><span data-stu-id="0c57a-207">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span></span>  

### <a name="see-also"></a><span data-ttu-id="0c57a-208">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="0c57a-208">See also</span></span>

 [<span data-ttu-id="0c57a-209">Support for Unified Interface Apps in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="0c57a-209">Support for Unified Interface Apps in Unified Service Desk</span></span>](../unified-service-desk/admin/Support-unified-interfaces-apps-usd.md)

 [<span data-ttu-id="0c57a-210">Unified Interface Page (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="0c57a-210">Unified Interface Page (Hosted Control)</span></span>](../unified-service-desk/unified-interface-page-hosted-control.md)

 [<span data-ttu-id="0c57a-211">Unified Service Desk and Unified Interface Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="0c57a-211">Unified Service Desk and Unified Interface Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md) 

 [<span data-ttu-id="0c57a-212">Walkthrough 1: Build a simple agent application for Unified Interface Apps</span><span class="sxs-lookup"><span data-stu-id="0c57a-212">Walkthrough 1: Build a simple agent application for Unified Interface Apps</span></span>](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)

 [<span data-ttu-id="0c57a-213">Cách 2: Hiển thị trang web bên ngoài trong ứng dụng tổng đài viên của bạn</span><span class="sxs-lookup"><span data-stu-id="0c57a-213">Walkthrough 2: Display an external webpage in your agent application</span></span>](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md)

 [<span data-ttu-id="0c57a-214">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application</span><span class="sxs-lookup"><span data-stu-id="0c57a-214">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application</span></span>](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)

 [<span data-ttu-id="0c57a-215">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application</span><span class="sxs-lookup"><span data-stu-id="0c57a-215">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application</span></span>](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md)

 [<span data-ttu-id="0c57a-216">Cách 5: Hiển thị thông tin phiên bổ sung bằng cách hiển thị tên và dữ liệu tổng quan về phiên</span><span class="sxs-lookup"><span data-stu-id="0c57a-216">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span></span>](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md)

 [<span data-ttu-id="0c57a-217">Cách 7: Đặt cấu hình mã lệnh tổng đài viên trong ứng dụng tổng đài viên của bạn</span><span class="sxs-lookup"><span data-stu-id="0c57a-217">Walkthrough 7: Configure agent scripting in your agent application</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)
