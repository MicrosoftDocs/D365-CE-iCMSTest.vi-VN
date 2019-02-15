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
# <a name="provide-feedback-about-includepnunifiedservicedeskincludespn-unified-service-deskmd"></a><span data-ttu-id="94216-103">Provide feedback about [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]</span><span class="sxs-lookup"><span data-stu-id="94216-103">Provide feedback about [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]</span></span>

<span data-ttu-id="94216-104">Have a comment or suggestion about [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]?</span><span class="sxs-lookup"><span data-stu-id="94216-104">Have a comment or suggestion about [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]?</span></span> <span data-ttu-id="94216-105">We need your feedback to help us deliver a reliable product.</span><span class="sxs-lookup"><span data-stu-id="94216-105">We need your feedback to help us deliver a reliable product.</span></span> <span data-ttu-id="94216-106">Good or bad, the quickest route to get your comments to our team is right from within [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="94216-106">Good or bad, the quickest route to get your comments to our team is right from within [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span> 

<span data-ttu-id="94216-107">With [!INCLUDE[pn-unified-service-desk-3-3](../../includes/pn-unified-service-desk-3-3.md)], you can see **Provide Feedback** option as a smiley on the toolbar.</span><span class="sxs-lookup"><span data-stu-id="94216-107">With [!INCLUDE[pn-unified-service-desk-3-3](../../includes/pn-unified-service-desk-3-3.md)], you can see **Provide Feedback** option as a smiley on the toolbar.</span></span>

## <a name="walkthrough-configure-provide-feedback-window-in-your-agent-application"></a><span data-ttu-id="94216-108">Walkthrough: Configure provide feedback window in your agent application</span><span class="sxs-lookup"><span data-stu-id="94216-108">Walkthrough: Configure provide feedback window in your agent application</span></span>

<span data-ttu-id="94216-109">The walkthrough demonstrates how to set up provide feedback window in your agent application.</span><span class="sxs-lookup"><span data-stu-id="94216-109">The walkthrough demonstrates how to set up provide feedback window in your agent application.</span></span> <span data-ttu-id="94216-110">In this walkthrough, you will learn to create **Provide Feedback** button on the **About Toolbar** toolbar container and associate an Action Call to the button.</span><span class="sxs-lookup"><span data-stu-id="94216-110">In this walkthrough, you will learn to create **Provide Feedback** button on the **About Toolbar** toolbar container and associate an Action Call to the button.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="94216-111">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="94216-111">Prerequisites</span></span>

<span data-ttu-id="94216-112">Bạn phải biết về những điều sau trong [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="94216-112">You must know about the following in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]:</span></span><br>  
    - <span data-ttu-id="94216-113">The Toolbar Container type of hosted control.</span><span class="sxs-lookup"><span data-stu-id="94216-113">The Toolbar Container type of hosted control.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="94216-114">[Hosted control types and action/event reference](../../unified-service-desk/hosted-control-types-action-event-reference.md)</span><span class="sxs-lookup"><span data-stu-id="94216-114">[Hosted control types and action/event reference](../../unified-service-desk/hosted-control-types-action-event-reference.md)</span></span>  

    - <span data-ttu-id="94216-115">Cuộc gọi hành động và cách cấu hình.</span><span class="sxs-lookup"><span data-stu-id="94216-115">Action call and how to configure it.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="94216-116">[Action calls](../../unified-service-desk/action-calls.md)</span><span class="sxs-lookup"><span data-stu-id="94216-116">[Action calls](../../unified-service-desk/action-calls.md)</span></span>

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a><span data-ttu-id="94216-117">Trong cách này</span><span class="sxs-lookup"><span data-stu-id="94216-117">In This Walkthrough</span></span>

 [<span data-ttu-id="94216-118">Bước 1: Tạo loại bộ chứa công cụ của kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="94216-118">Step 1: Create a toolbar container type of hosted control</span></span>](#Step1)

 [<span data-ttu-id="94216-119">Bước 2: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="94216-119">Step 2: Add a toolbar and attach it to the toolbar container</span></span>](#Step2)

 [<span data-ttu-id="94216-120">Step 3: Add toolbar button and action call to display the feedback window</span><span class="sxs-lookup"><span data-stu-id="94216-120">Step 3: Add toolbar button and action call to display the feedback window</span></span>](#Step3)

 [<span data-ttu-id="94216-121">Bước 4: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="94216-121">Step 4: Add the controls to the configuration </span></span>](#Step4)

 [<span data-ttu-id="94216-122">Step 5: Test the provide feedback option in the application</span><span class="sxs-lookup"><span data-stu-id="94216-122">Step 5: Test the provide feedback option in the application</span></span>](#Step5)

 [<span data-ttu-id="94216-123">Kết luận</span><span class="sxs-lookup"><span data-stu-id="94216-123">Conclusion</span></span>](#Conclusion)

<a name="Step1"></a>   
## <a name="step-1-create-a-toolbar-container-type-of-hosted-control"></a><span data-ttu-id="94216-124">Bước 1: Tạo loại bộ chứa công cụ của kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="94216-124">Step 1: Create a toolbar container type of hosted control</span></span>  

 <span data-ttu-id="94216-125">Toolbar Container type of hosted control are used to hold and display the toolbars in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="94216-125">Toolbar Container type of hosted control are used to hold and display the toolbars in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="94216-126">Trong phần này, bạn sẽ tạo ra kiểm soát tổ chức **Bộ chứa thanh công cụ** mà sẽ xuất hiện ở phía trên cùng của ứng dụng khách.</span><span class="sxs-lookup"><span data-stu-id="94216-126">In this section, you’ll create a **Toolbar Container** hosted control that will appear at the top of the client application.</span></span>  

1. <span data-ttu-id="94216-127">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="94216-127">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]  
3. <span data-ttu-id="94216-128">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="94216-128">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="94216-129">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="94216-129">Click **New**.</span></span>  

5. <span data-ttu-id="94216-130">On the **New Hosted Control** page, specify the following values</span><span class="sxs-lookup"><span data-stu-id="94216-130">On the **New Hosted Control** page, specify the following values</span></span>  


   |       <span data-ttu-id="94216-131">Trường</span><span class="sxs-lookup"><span data-stu-id="94216-131">Field</span></span>        |          <span data-ttu-id="94216-132">Value</span><span class="sxs-lookup"><span data-stu-id="94216-132">Value</span></span>          |
   |--------------------|-------------------------|
   |        <span data-ttu-id="94216-133">Tên</span><span class="sxs-lookup"><span data-stu-id="94216-133">Name</span></span>        | <span data-ttu-id="94216-134">About Toolbar Container</span><span class="sxs-lookup"><span data-stu-id="94216-134">About Toolbar Container</span></span> |
   | <span data-ttu-id="94216-135">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="94216-135">USD Component Type</span></span> |    <span data-ttu-id="94216-136">Bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="94216-136">Toolbar Container</span></span>    |
   |   <span data-ttu-id="94216-137">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="94216-137">Display Group</span></span>    |       <span data-ttu-id="94216-138">AboutPanel</span><span class="sxs-lookup"><span data-stu-id="94216-138">AboutPanel</span></span>        |


6. <span data-ttu-id="94216-139">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="94216-139">Click **Save**.</span></span>  

<a name="Step2"></a>   
## <a name="step-2-add-a-toolbar-and-attach-it-to-the-toolbar-container"></a><span data-ttu-id="94216-140">Bước 2: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="94216-140">Step 2: Add a toolbar and attach it to the toolbar container</span></span>  
 <span data-ttu-id="94216-141">In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 1.</span><span class="sxs-lookup"><span data-stu-id="94216-141">In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 1.</span></span> <span data-ttu-id="94216-142">This is done to display the toolbar in your agent application.</span><span class="sxs-lookup"><span data-stu-id="94216-142">This is done to display the toolbar in your agent application.</span></span>  

1. <span data-ttu-id="94216-143">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="94216-143">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]

3. <span data-ttu-id="94216-144">Bấm vào **Thanh công cụ**.</span><span class="sxs-lookup"><span data-stu-id="94216-144">Click **Toolbars**.</span></span>  

4. <span data-ttu-id="94216-145">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="94216-145">Click **New**.</span></span>

5. <span data-ttu-id="94216-146">On the **New Toolbar** page, type **About Toolbar** in the **Name** box, and then click **Save**.</span><span class="sxs-lookup"><span data-stu-id="94216-146">On the **New Toolbar** page, type **About Toolbar** in the **Name** box, and then click **Save**.</span></span>  

6. <span data-ttu-id="94216-147">Attach the toolbar to the toolbar container hosted control created in step 1.</span><span class="sxs-lookup"><span data-stu-id="94216-147">Attach the toolbar to the toolbar container hosted control created in step 1.</span></span> <span data-ttu-id="94216-148">On the nav bar, click the down arrow next to **About Toolbar**, and click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="94216-148">On the nav bar, click the down arrow next to **About Toolbar**, and click **Hosted Controls**.</span></span>  

7. <span data-ttu-id="94216-149">On the next page, click **Add Existing Hosted Control**, type `About Toolbar Container` in the search bar, and then press **ENTER** or click the search icon.</span><span class="sxs-lookup"><span data-stu-id="94216-149">On the next page, click **Add Existing Hosted Control**, type `About Toolbar Container` in the search bar, and then press **ENTER** or click the search icon.</span></span>

8. <span data-ttu-id="94216-150">From the search result, click **About Toolbar Container** to add.</span><span class="sxs-lookup"><span data-stu-id="94216-150">From the search result, click **About Toolbar Container** to add.</span></span>  

9. <span data-ttu-id="94216-151">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="94216-151">Click **Save**.</span></span>

<a name="Step3"></a>   
## <a name="step-3-add-toolbar-button-and-action-call-to-display-the-feedback-window"></a><span data-ttu-id="94216-152">Step 3: Add toolbar button and action call to display the feedback window</span><span class="sxs-lookup"><span data-stu-id="94216-152">Step 3: Add toolbar button and action call to display the feedback window</span></span>

 <span data-ttu-id="94216-153">In this step, you’ll add button on the toolbar and attach action call to the button so that when the button is clicked, **Provide Feedback** window is displayed in the hosted control that were created in step 1.</span><span class="sxs-lookup"><span data-stu-id="94216-153">In this step, you’ll add button on the toolbar and attach action call to the button so that when the button is clicked, **Provide Feedback** window is displayed in the hosted control that were created in step 1.</span></span>

1. <span data-ttu-id="94216-154">After you save the toolbar in step 2, the **Buttons** area becomes available.</span><span class="sxs-lookup"><span data-stu-id="94216-154">After you save the toolbar in step 2, the **Buttons** area becomes available.</span></span> <span data-ttu-id="94216-155">In the **Buttons** area, click **+** on the right corner to add a button.</span><span class="sxs-lookup"><span data-stu-id="94216-155">In the **Buttons** area, click **+** on the right corner to add a button.</span></span>  

2. <span data-ttu-id="94216-156">On the **New Toolbar Button** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="94216-156">On the **New Toolbar Button** page, specify the following values:</span></span>  

    |<span data-ttu-id="94216-157">Trường</span><span class="sxs-lookup"><span data-stu-id="94216-157">Field</span></span>|<span data-ttu-id="94216-158">Value</span><span class="sxs-lookup"><span data-stu-id="94216-158">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="94216-159">Tên</span><span class="sxs-lookup"><span data-stu-id="94216-159">Name</span></span>|<span data-ttu-id="94216-160">Provide Feedback</span><span class="sxs-lookup"><span data-stu-id="94216-160">Provide Feedback</span></span>|
    |<span data-ttu-id="94216-161">Hình ảnh</span><span class="sxs-lookup"><span data-stu-id="94216-161">Image</span></span>|<span data-ttu-id="94216-162">msdyusd_Feedback_16</span><span class="sxs-lookup"><span data-stu-id="94216-162">msdyusd_Feedback_16</span></span>|
    |<span data-ttu-id="94216-163">Chú giải công cụ</span><span class="sxs-lookup"><span data-stu-id="94216-163">Tooltip</span></span>|<span data-ttu-id="94216-164">Provide Feedback</span><span class="sxs-lookup"><span data-stu-id="94216-164">Provide Feedback</span></span>|  
    |<span data-ttu-id="94216-165">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="94216-165">Order</span></span>|<span data-ttu-id="94216-166">102</span><span class="sxs-lookup"><span data-stu-id="94216-166">102</span></span>|

3. <span data-ttu-id="94216-167">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="94216-167">Click **Save**.</span></span>

4. <span data-ttu-id="94216-168">You need add the action call to display the **Provide Feedback** in the hosted control created in step 1.</span><span class="sxs-lookup"><span data-stu-id="94216-168">You need add the action call to display the **Provide Feedback** in the hosted control created in step 1.</span></span>

    <span data-ttu-id="94216-169">In the **Actions** area, click **+** on the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="94216-169">In the **Actions** area, click **+** on the right corner to add an action call.</span></span>  

5. <span data-ttu-id="94216-170">In the search box in the **Actions** area, press **ENTER** or click the search icon.</span><span class="sxs-lookup"><span data-stu-id="94216-170">In the search box in the **Actions** area, press **ENTER** or click the search icon.</span></span>  

6. <span data-ttu-id="94216-171">Trong hộp tìm kiếm kết quả, bấm vào **Mới** ở góc dưới bên phải để tạo ra cuộc gọi hành động cho nút thanh công cụ này.</span><span class="sxs-lookup"><span data-stu-id="94216-171">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>

7. <span data-ttu-id="94216-172">On the **New Action Call** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="94216-172">On the **New Action Call** page, specify the following values:</span></span>

    |<span data-ttu-id="94216-173">Trường</span><span class="sxs-lookup"><span data-stu-id="94216-173">Field</span></span>|<span data-ttu-id="94216-174">Value</span><span class="sxs-lookup"><span data-stu-id="94216-174">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="94216-175">Tên</span><span class="sxs-lookup"><span data-stu-id="94216-175">Name</span></span>|<span data-ttu-id="94216-176">Show FeedBack Window</span><span class="sxs-lookup"><span data-stu-id="94216-176">Show FeedBack Window</span></span>|  
    |<span data-ttu-id="94216-177">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="94216-177">Order</span></span>|<span data-ttu-id="94216-178">1</span><span class="sxs-lookup"><span data-stu-id="94216-178">1</span></span>|  
    |<span data-ttu-id="94216-179">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="94216-179">Hosted Control</span></span>|<span data-ttu-id="94216-180">CRM Global Manager</span><span class="sxs-lookup"><span data-stu-id="94216-180">CRM Global Manager</span></span>|  
    |<span data-ttu-id="94216-181">Hành động</span><span class="sxs-lookup"><span data-stu-id="94216-181">Action</span></span>|<span data-ttu-id="94216-182">ShowFeedback</span><span class="sxs-lookup"><span data-stu-id="94216-182">ShowFeedback</span></span>|

8. <span data-ttu-id="94216-183">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="94216-183">Click **Save**.</span></span> <span data-ttu-id="94216-184">The new action call gets added to the **Provide Feedback** button.</span><span class="sxs-lookup"><span data-stu-id="94216-184">The new action call gets added to the **Provide Feedback** button.</span></span>

<a name="Step4"></a>   
## <a name="step-4-add-the-controls-to-the-configuration"></a><span data-ttu-id="94216-185">Bước 4: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="94216-185">Step 4: Add the controls to the configuration</span></span>  
 <span data-ttu-id="94216-186">In this step, you’ll add the action call, hosted control, and toolbar that were created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span><span class="sxs-lookup"><span data-stu-id="94216-186">In this step, you’ll add the action call, hosted control, and toolbar that were created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span></span> <span data-ttu-id="94216-187">If you have not created **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="94216-187">If you have not created **Contoso Configuration**.</span></span> <span data-ttu-id="94216-188">Visit, [Walkthrough 1: Build a simple agent application](../../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="94216-188">Visit, [Walkthrough 1: Build a simple agent application](../../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span>

 <span data-ttu-id="94216-189">Add the following to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="94216-189">Add the following to **Contoso Configuration**.</span></span>

|<span data-ttu-id="94216-190">Tên kiểm soát</span><span class="sxs-lookup"><span data-stu-id="94216-190">Control name</span></span>|<span data-ttu-id="94216-191">Loại kiểm soát</span><span class="sxs-lookup"><span data-stu-id="94216-191">Control type</span></span>|  
|------------------|------------------|  
|<span data-ttu-id="94216-192">Show FeedBack Window</span><span class="sxs-lookup"><span data-stu-id="94216-192">Show FeedBack Window</span></span>|<span data-ttu-id="94216-193">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="94216-193">Action Call</span></span>| 
|<span data-ttu-id="94216-194">About Toolbar Container</span><span class="sxs-lookup"><span data-stu-id="94216-194">About Toolbar Container</span></span>|<span data-ttu-id="94216-195">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="94216-195">Hosted Control</span></span>| 
|<span data-ttu-id="94216-196">Provide Feedback</span><span class="sxs-lookup"><span data-stu-id="94216-196">Provide Feedback</span></span>|<span data-ttu-id="94216-197">Thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="94216-197">Toolbar</span></span>|

 <span data-ttu-id="94216-198">To add a control to the configuration:</span><span class="sxs-lookup"><span data-stu-id="94216-198">To add a control to the configuration:</span></span>  

1. <span data-ttu-id="94216-199">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="94216-199">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="94216-200">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="94216-200">Click **Configuration**.</span></span>  

4. <span data-ttu-id="94216-201">Click **Contoso Configuration** to open the definition.</span><span class="sxs-lookup"><span data-stu-id="94216-201">Click **Contoso Configuration** to open the definition.</span></span>  

5. <span data-ttu-id="94216-202">On the nav bar, click the down arrow next to **Contoso Configuration**, and select **Action Calls**.</span><span class="sxs-lookup"><span data-stu-id="94216-202">On the nav bar, click the down arrow next to **Contoso Configuration**, and select **Action Calls**.</span></span>  

6. <span data-ttu-id="94216-203">On the next page, click **Add Existing Action Call**, type `Show FeedBack Window` in the search bar, and then press **ENTER** or click the search icon.</span><span class="sxs-lookup"><span data-stu-id="94216-203">On the next page, click **Add Existing Action Call**, type `Show FeedBack Window` in the search bar, and then press **ENTER** or click the search icon.</span></span>  

7. <span data-ttu-id="94216-204">The action call listed earlier are displayed in the search results.</span><span class="sxs-lookup"><span data-stu-id="94216-204">The action call listed earlier are displayed in the search results.</span></span> <span data-ttu-id="94216-205">Add these action call.</span><span class="sxs-lookup"><span data-stu-id="94216-205">Add these action call.</span></span>  

8. <span data-ttu-id="94216-206">Similarly, add the hosted control and the toolbar by clicking the down arrow next to **Contoso Configuration**, and clicking **Hosted Controls** and **Toolbars** respectively.</span><span class="sxs-lookup"><span data-stu-id="94216-206">Similarly, add the hosted control and the toolbar by clicking the down arrow next to **Contoso Configuration**, and clicking **Hosted Controls** and **Toolbars** respectively.</span></span>  

9. <span data-ttu-id="94216-207">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="94216-207">Click **Save**.</span></span>


<a name="Step5"></a> 
## <a name="step-5-test-the-provide-feedback-option-in-the-application"></a><span data-ttu-id="94216-208">Step 5: Test the provide feedback option in the application</span><span class="sxs-lookup"><span data-stu-id="94216-208">Step 5: Test the provide feedback option in the application</span></span>

<span data-ttu-id="94216-209">Start the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance where you configured [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="94216-209">Start the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance where you configured [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration**.</span></span> <span data-ttu-id="94216-210">For information about connecting to a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span><span class="sxs-lookup"><span data-stu-id="94216-210">For information about connecting to a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span></span>

<span data-ttu-id="94216-211">Your agent application will now have a **Smiley** button in the toolbar area.</span><span class="sxs-lookup"><span data-stu-id="94216-211">Your agent application will now have a **Smiley** button in the toolbar area.</span></span>

1. <span data-ttu-id="94216-212">On the toolbar, select the **Provide Feedback** smiley.</span><span class="sxs-lookup"><span data-stu-id="94216-212">On the toolbar, select the **Provide Feedback** smiley.</span></span> <br/><span data-ttu-id="94216-213">The **Feedback** window appears.</span><span class="sxs-lookup"><span data-stu-id="94216-213">The **Feedback** window appears.</span></span><br>
2. <span data-ttu-id="94216-214">Select a smiley from the list:</span><span class="sxs-lookup"><span data-stu-id="94216-214">Select a smiley from the list:</span></span>
   - <span data-ttu-id="94216-215">Good</span><span class="sxs-lookup"><span data-stu-id="94216-215">Good</span></span>
   - <span data-ttu-id="94216-216">Normal</span><span class="sxs-lookup"><span data-stu-id="94216-216">Normal</span></span>
   - <span data-ttu-id="94216-217">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="94216-217">Bad</span></span>
3. <span data-ttu-id="94216-218">Type your feedback or suggestion in the text box.</span><span class="sxs-lookup"><span data-stu-id="94216-218">Type your feedback or suggestion in the text box.</span></span> 
4. <span data-ttu-id="94216-219">Select **Submit** to send your feedback to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)].</span><span class="sxs-lookup"><span data-stu-id="94216-219">Select **Submit** to send your feedback to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)].</span></span><br>

   <span data-ttu-id="94216-220">![Provide feedback smiley and window](../media/provide-feedback-smiley-window.PNG "Provide feedback smiley and window")</span><span class="sxs-lookup"><span data-stu-id="94216-220">![Provide feedback smiley and window](../media/provide-feedback-smiley-window.PNG "Provide feedback smiley and window")</span></span>


<a name="Conclusion"></a> 
## <a name="conclusion"></a><span data-ttu-id="94216-221">Kết luận</span><span class="sxs-lookup"><span data-stu-id="94216-221">Conclusion</span></span>

 <span data-ttu-id="94216-222">In this walkthrough, you learned how to set up provide feedback button in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application.</span><span class="sxs-lookup"><span data-stu-id="94216-222">In this walkthrough, you learned how to set up provide feedback button in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application.</span></span>  

> [!Note]
> <span data-ttu-id="94216-223">It is recommended that you do not submit any feedback containing personal or other data that is subject to legal or regulatory compliance requirements.</span><span class="sxs-lookup"><span data-stu-id="94216-223">It is recommended that you do not submit any feedback containing personal or other data that is subject to legal or regulatory compliance requirements.</span></span>
> 
> [!Note]
> <span data-ttu-id="94216-224">Setting the **HelpImproveUsd** global option to **False**, disables the data collection and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] dose not send information to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)].</span><span class="sxs-lookup"><span data-stu-id="94216-224">Setting the **HelpImproveUsd** global option to **False**, disables the data collection and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] dose not send information to [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)].</span></span> <span data-ttu-id="94216-225">If the data collection is disabled, then agent or system administrator cannot provide feedback due to insufficient permissions.</span><span class="sxs-lookup"><span data-stu-id="94216-225">If the data collection is disabled, then agent or system administrator cannot provide feedback due to insufficient permissions.</span></span><br>
> <span data-ttu-id="94216-226">![Insufficient Permissions](../media/insufficient-permissions-provide-feedback-window.PNG "Insufficient Permissions")</span><span class="sxs-lookup"><span data-stu-id="94216-226">![Insufficient Permissions](../media/insufficient-permissions-provide-feedback-window.PNG "Insufficient Permissions")</span></span>

## <a name="see-also"></a><span data-ttu-id="94216-227">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="94216-227">See also</span></span>

[<span data-ttu-id="94216-228">Help improve Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="94216-228">Help improve Unified Service Desk</span></span>](../admin/help-improve-unified-service-desk.md)
