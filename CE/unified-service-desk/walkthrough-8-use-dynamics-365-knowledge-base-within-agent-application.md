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
# <a name="walkthrough-8-use-customer-engagement-knowledge-base-within-your-agent-application"></a><span data-ttu-id="a2ae8-103">Walkthrough 8: Use Customer Engagement knowledge base within your agent application</span><span class="sxs-lookup"><span data-stu-id="a2ae8-103">Walkthrough 8: Use Customer Engagement knowledge base within your agent application</span></span>
<span data-ttu-id="a2ae8-104">This walkthrough demonstrates how to configure a panel in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the **KM Control** hosted control that displays knowledge base records from your [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] instance.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-104">This walkthrough demonstrates how to configure a panel in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the **KM Control** hosted control that displays knowledge base records from your [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] instance.</span></span>  

 <span data-ttu-id="a2ae8-105">Trong cách này, bạn sẽ:</span><span class="sxs-lookup"><span data-stu-id="a2ae8-105">In this walkthrough, you’ll:</span></span>  

- <span data-ttu-id="a2ae8-106">Display knowledge base articles from Dynamics 365 for Customer Engagement apps to appear in a search panel in context with your currently open case record in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="a2ae8-106">Display knowledge base articles from Dynamics 365 for Customer Engagement apps to appear in a search panel in context with your currently open case record in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="a2ae8-107">Người dùng có thể lọc và sắp xếp các kết quả dựa trên nhiều tiêu chí.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-107">Users can filter and sort the results based on various criteria.</span></span> <span data-ttu-id="a2ae8-108">Moreover, the search panel automatically appears when you open a case session, and automatically hides when you close the session.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-108">Moreover, the search panel automatically appears when you open a case session, and automatically hides when you close the session.</span></span>  

- <span data-ttu-id="a2ae8-109">Hiển thị bài viết trong một tab khi bạn chọn tiêu đề bài viết trong bảng điều khiển tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-109">Display the article in a tab when you choose the article title in the search panel.</span></span>  

- <span data-ttu-id="a2ae8-110">Đặt cấu hình các hành động theo ngữ cảnh cho bài viết trong tab nơi bài viết được hiển thị, chẳng hạn như bản sao một liên kết bài viết hoặc liên kết một bài viết với trường hợp hiện tại.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-110">Configure contextual actions for the article in the tab where it is displayed, such as copy an article link or associate an article with the current case.</span></span>  

  [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a2ae8-111">[Use Dynamics 365 for Customer Engagement apps knowledge for effective customer engagement](../unified-service-desk/use-dynamics-365-knowledge-effective-customer-engagement.md)</span><span class="sxs-lookup"><span data-stu-id="a2ae8-111">[Use Dynamics 365 for Customer Engagement apps knowledge for effective customer engagement](../unified-service-desk/use-dynamics-365-knowledge-effective-customer-engagement.md)</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="a2ae8-112">Cách này không yêu cầu bạn hoàn thành các cách khác trước khi bạn có thể dùng cách này.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-112">This walkthrough doesn’t require you to complete other walkthroughs before you can use this one.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="a2ae8-113">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="a2ae8-113">Prerequisites</span></span>  

- <span data-ttu-id="a2ae8-114">Deploy the "New Environment" sample application package to your [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] instance.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-114">Deploy the "New Environment" sample application package to your [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] instance.</span></span> <span data-ttu-id="a2ae8-115">The walkthrough uses some of the controls and configuration in the "New Environment" sample application package that are created in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps when you deploy the sample application.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-115">The walkthrough uses some of the controls and configuration in the "New Environment" sample application package that are created in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps when you deploy the sample application.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a2ae8-116">[Deploy sample Unified Service Desk applications to CRM server using Package Deployer](admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md)</span><span class="sxs-lookup"><span data-stu-id="a2ae8-116">[Deploy sample Unified Service Desk applications to CRM server using Package Deployer](admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md)</span></span>    

- <span data-ttu-id="a2ae8-117">Bạn phải biết về những điều sau trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="a2ae8-117">You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  

  - <span data-ttu-id="a2ae8-118">The `KM Control` and `Panel Layout` types of hosted controls:.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-118">The `KM Control` and `Panel Layout` types of hosted controls:.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a2ae8-119">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span><span class="sxs-lookup"><span data-stu-id="a2ae8-119">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span></span>  

  - <span data-ttu-id="a2ae8-120">Concepts about using the `KM Control` type of hosted control to configure knowledge management.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-120">Concepts about using the `KM Control` type of hosted control to configure knowledge management.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a2ae8-121">[Configure Dynamics 365 for Customer Engagement apps knowledge in Unified Service Desk](../unified-service-desk/configure-unified-service-desk-use-dynamics-365-knowledge.md)</span><span class="sxs-lookup"><span data-stu-id="a2ae8-121">[Configure Dynamics 365 for Customer Engagement apps knowledge in Unified Service Desk](../unified-service-desk/configure-unified-service-desk-use-dynamics-365-knowledge.md)</span></span>  

  - <span data-ttu-id="a2ae8-122">How to configure action calls.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-122">How to configure action calls.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a2ae8-123">[Action calls](../unified-service-desk/action-calls.md)</span><span class="sxs-lookup"><span data-stu-id="a2ae8-123">[Action calls](../unified-service-desk/action-calls.md)</span></span>  

  - <span data-ttu-id="a2ae8-124">Sự kiện.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-124">Events.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a2ae8-125">[Events](../unified-service-desk/events.md)</span><span class="sxs-lookup"><span data-stu-id="a2ae8-125">[Events](../unified-service-desk/events.md)</span></span>  

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a><span data-ttu-id="a2ae8-126">In This Walkthrough</span><span class="sxs-lookup"><span data-stu-id="a2ae8-126">In This Walkthrough</span></span>  
 [<span data-ttu-id="a2ae8-127">Bước 1: Tạo kiểm soát tổ chức loại Kiểm soát KM</span><span class="sxs-lookup"><span data-stu-id="a2ae8-127">Step 1: Create a hosted control of type KM Control</span></span>](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step1)  

 [<span data-ttu-id="a2ae8-128">Bước 2: Đặt cấu hình cuộc gọi hành động để hiển thị tìm kiếm cơ sở kiến thức</span><span class="sxs-lookup"><span data-stu-id="a2ae8-128">Step 2: Configure an action call to display the knowledge base search</span></span>](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step2)  

 [<span data-ttu-id="a2ae8-129">Bước 3: Đặt cấu hình cuộc gọi hành động để tự động hiển thị và ẩn bảng điều khiển tìm kiếm cơ sở kiến thức</span><span class="sxs-lookup"><span data-stu-id="a2ae8-129">Step 3: Configure action calls to automatically display and hide the knowledge base search panel</span></span>](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step3)  

 [<span data-ttu-id="a2ae8-130">Step 4: Configure an action call to automatically search knowledge base using the incident (case) title</span><span class="sxs-lookup"><span data-stu-id="a2ae8-130">Step 4: Configure an action call to automatically search knowledge base using the incident (case) title</span></span>](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step4)  

 [<span data-ttu-id="a2ae8-131">Bước 5: Đặt cấu hình kiểm soát tổ chức và các cuộc gọi hành động để hiển thị một bài viết trong một tab</span><span class="sxs-lookup"><span data-stu-id="a2ae8-131">Step 5: Configure hosted controls and action calls to display an article in a tab</span></span>](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step5)  

 [<span data-ttu-id="a2ae8-132">Bước 6: Đặt cấu hình các hành động theo ngữ cảnh cho bài viết cơ sở kiến thức trong tab</span><span class="sxs-lookup"><span data-stu-id="a2ae8-132">Step 6: Configure contextual actions for the knowledge base article in the tab</span></span>](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step6)  

 [<span data-ttu-id="a2ae8-133">Bước 7: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="a2ae8-133">Step 7: Test the application</span></span>](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Step7)  

 [<span data-ttu-id="a2ae8-134">Kết luận</span><span class="sxs-lookup"><span data-stu-id="a2ae8-134">Conclusion</span></span>](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md#Conclusion)  

<a name="Step1"></a>   
## <a name="step-1-create-a-hosted-control-of-type-km-control"></a><span data-ttu-id="a2ae8-135">Bước 1: Tạo kiểm soát tổ chức loại Kiểm soát KM</span><span class="sxs-lookup"><span data-stu-id="a2ae8-135">Step 1: Create a hosted control of type KM Control</span></span>  
 <span data-ttu-id="a2ae8-136">Trong bước này, bạn sẽ tạo kiểm soát tổ chức loại **Kiểm soát KM** để hiển thị ngăn tìm kiếm cơ sở kiến thức.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-136">In this step, you’ll create a hosted control of type **KM Control** to display the knowledge base search pane.</span></span>  

1. <span data-ttu-id="a2ae8-137">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-137">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="a2ae8-138">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-138">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="a2ae8-139">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-139">Click **New**.</span></span>  

5. <span data-ttu-id="a2ae8-140">Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-140">On the **New Hosted Control** page, specify the following values.</span></span>  

   |<span data-ttu-id="a2ae8-141">Trường</span><span class="sxs-lookup"><span data-stu-id="a2ae8-141">Field</span></span>|<span data-ttu-id="a2ae8-142">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a2ae8-142">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="a2ae8-143">Tên</span><span class="sxs-lookup"><span data-stu-id="a2ae8-143">Name</span></span>|<span data-ttu-id="a2ae8-144">Tìm kiếm KB Mẫu</span><span class="sxs-lookup"><span data-stu-id="a2ae8-144">Sample KB Search</span></span>|  
   |<span data-ttu-id="a2ae8-145">Tên Hiển thị</span><span class="sxs-lookup"><span data-stu-id="a2ae8-145">Display Name</span></span>|<span data-ttu-id="a2ae8-146">Tìm kiếm KB Mẫu</span><span class="sxs-lookup"><span data-stu-id="a2ae8-146">Sample KB Search</span></span>|  
   |<span data-ttu-id="a2ae8-147">Loại thành phần USD</span><span class="sxs-lookup"><span data-stu-id="a2ae8-147">USD Component Type</span></span>|<span data-ttu-id="a2ae8-148">Kiểm soát KM</span><span class="sxs-lookup"><span data-stu-id="a2ae8-148">KM Control</span></span>|  
   |<span data-ttu-id="a2ae8-149">Cho phép nhiều trang</span><span class="sxs-lookup"><span data-stu-id="a2ae8-149">Allow Multiple Pages</span></span>|<span data-ttu-id="a2ae8-150">No</span><span class="sxs-lookup"><span data-stu-id="a2ae8-150">No</span></span>|  
   |<span data-ttu-id="a2ae8-151">Loại lưu trữ</span><span class="sxs-lookup"><span data-stu-id="a2ae8-151">Hosting Type</span></span>|<span data-ttu-id="a2ae8-152">WPF nội bộ</span><span class="sxs-lookup"><span data-stu-id="a2ae8-152">Internal WPF</span></span>|  
   |<span data-ttu-id="a2ae8-153">Application is Global</span><span class="sxs-lookup"><span data-stu-id="a2ae8-153">Application is Global</span></span>|<span data-ttu-id="a2ae8-154">Đã kiểm tra</span><span class="sxs-lookup"><span data-stu-id="a2ae8-154">Checked</span></span>|  
   |<span data-ttu-id="a2ae8-155">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="a2ae8-155">Display Group</span></span>|<span data-ttu-id="a2ae8-156">RightPanel</span><span class="sxs-lookup"><span data-stu-id="a2ae8-156">RightPanel</span></span>|  

   <span data-ttu-id="a2ae8-157">![Create a KM Control hosted control](../unified-service-desk/media/usd-createkmcontrol.png "Create a KM Control hosted control")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-157">![Create a KM Control hosted control](../unified-service-desk/media/usd-createkmcontrol.png "Create a KM Control hosted control")</span></span>  

6. <span data-ttu-id="a2ae8-158">Bấm vào **Lưu và Đóng**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-158">Click **Save and Close**.</span></span>  

<a name="Step2"></a>   
## <a name="step-2-configure-an-action-call-to-display-the-knowledge-base-search"></a><span data-ttu-id="a2ae8-159">Bước 2: Đặt cấu hình cuộc gọi hành động để hiển thị tìm kiếm cơ sở kiến thức</span><span class="sxs-lookup"><span data-stu-id="a2ae8-159">Step 2: Configure an action call to display the knowledge base search</span></span>  
 <span data-ttu-id="a2ae8-160">Tạo một cuộc gọi hành động để hiển thị kiểm soát tổ chức mới tạo trong máy tính để bàn của tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-160">Create an action call to display the newly created hosted control in the agent desktop.</span></span> <span data-ttu-id="a2ae8-161">You’ll use the `default` action for the newly created hosted control to display it.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-161">You’ll use the `default` action for the newly created hosted control to display it.</span></span> <span data-ttu-id="a2ae8-162">After creating the action, add it to the `SessionNew` event for the **Dynamics 365 for Customer Engagement apps Global Manager** hosted control to automatically load and display the hosted control when a new session is created on opening a case.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-162">After creating the action, add it to the `SessionNew` event for the **Dynamics 365 for Customer Engagement apps Global Manager** hosted control to automatically load and display the hosted control when a new session is created on opening a case.</span></span>  

1. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

2. <span data-ttu-id="a2ae8-163">Bấm **Cuộc gọi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-163">Click **Action Calls**.</span></span>  

3. <span data-ttu-id="a2ae8-164">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-164">Click **New**.</span></span>  

4. <span data-ttu-id="a2ae8-165">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-165">On the **New Action Call** page, specify the following values.</span></span>  

   |<span data-ttu-id="a2ae8-166">Trường</span><span class="sxs-lookup"><span data-stu-id="a2ae8-166">Field</span></span>|<span data-ttu-id="a2ae8-167">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a2ae8-167">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="a2ae8-168">Tên</span><span class="sxs-lookup"><span data-stu-id="a2ae8-168">Name</span></span>|<span data-ttu-id="a2ae8-169">Mẫu: Mở Kiểm soát Tìm kiếm KB</span><span class="sxs-lookup"><span data-stu-id="a2ae8-169">Sample: Open KB Search Control</span></span>|  
   |<span data-ttu-id="a2ae8-170">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="a2ae8-170">Hosted Control</span></span>|<span data-ttu-id="a2ae8-171">Tìm kiếm KB Mẫu</span><span class="sxs-lookup"><span data-stu-id="a2ae8-171">Sample KB Search</span></span>|  
   |<span data-ttu-id="a2ae8-172">Hành động</span><span class="sxs-lookup"><span data-stu-id="a2ae8-172">Action</span></span>|<span data-ttu-id="a2ae8-173">mặc định</span><span class="sxs-lookup"><span data-stu-id="a2ae8-173">default</span></span>|  

   <span data-ttu-id="a2ae8-174">![Action call to open the KB Search panel](../unified-service-desk/media/usd-openkmcontrol.png "Action call to open the KB Search panel")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-174">![Action call to open the KB Search panel](../unified-service-desk/media/usd-openkmcontrol.png "Action call to open the KB Search panel")</span></span>  

5. <span data-ttu-id="a2ae8-175">Bấm **Lưu và đóng**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-175">Click **Save and close**.</span></span>  

6. <span data-ttu-id="a2ae8-176">Truy cập trang **Unified Service Desk**, rồi bấm vào **Sự kiện**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-176">Go to **Unified Service Desk** page, and then click **Events**.</span></span>  

7. <span data-ttu-id="a2ae8-177">Tìm kiếm sự kiện `SessionNew`, rồi bấm vào sự kiện để mở trang cấu hình sự kiện.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-177">Search for the `SessionNew` event, and then click it to open the event configuration page.</span></span>  

8. <span data-ttu-id="a2ae8-178">Click the **Add Action Call record** button to add the action call.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-178">Click the **Add Action Call record** button to add the action call.</span></span>  

   <span data-ttu-id="a2ae8-179">![Add action to event](../unified-service-desk/media/usd-addactiontoevent.png "Add action to event")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-179">![Add action to event](../unified-service-desk/media/usd-addactiontoevent.png "Add action to event")</span></span>  

9. <span data-ttu-id="a2ae8-180">Type `Sample: Open KB Search Control` in the search box, and press ENTER or click the search button to add the action to the event.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-180">Type `Sample: Open KB Search Control` in the search box, and press ENTER or click the search button to add the action to the event.</span></span> <span data-ttu-id="a2ae8-181">Change the order of the added action to 1, and then click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-181">Change the order of the added action to 1, and then click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner.</span></span>  

<a name="Step3"></a>   
## <a name="step-3-configure-action-calls-to-automatically-display-and-hide-the-knowledge-base-search-panel"></a><span data-ttu-id="a2ae8-182">Bước 3: Đặt cấu hình cuộc gọi hành động để tự động hiển thị và ẩn bảng điều khiển tìm kiếm cơ sở kiến thức</span><span class="sxs-lookup"><span data-stu-id="a2ae8-182">Step 3: Configure action calls to automatically display and hide the knowledge base search panel</span></span>  
 <span data-ttu-id="a2ae8-183">Create two action calls to display and hide the panel (`RightPanel`) that will display the newly added hosted control.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-183">Create two action calls to display and hide the panel (`RightPanel`) that will display the newly added hosted control.</span></span> <span data-ttu-id="a2ae8-184">Tiếp theo, thêm các kiểm soát tổ chức đó vào sự kiện phù hợp để tự động hiển thị (mở rộng) và ẩn (thu hẹp) bảng điều khiển trong máy tính để bàn của tổng đài viên khi phiên mới được tạo và phiên này đóng tương ứng.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-184">Next, add those to appropriate events to automatically display (expand) and hide (collapse) the panel in the agent desktop when a new session is created and the session is closed respectively.</span></span>  

 <span data-ttu-id="a2ae8-185">Use the new `SetVisualProperty` action to control the visual properties of the panel layout (**Main Layout** hosted control in the “Base sample application”).</span><span class="sxs-lookup"><span data-stu-id="a2ae8-185">Use the new `SetVisualProperty` action to control the visual properties of the panel layout (**Main Layout** hosted control in the “Base sample application”).</span></span> <span data-ttu-id="a2ae8-186">`SetVisualProperty` has to be manually added to the hosted control to be used.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-186">`SetVisualProperty` has to be manually added to the hosted control to be used.</span></span> <span data-ttu-id="a2ae8-187">Tuy nhiên, nếu bạn tạo phiên bản **Bố cục Bảng điều khiển** loại kiểm soát tổ chức mới, `SetVisualProperty` sẽ sẵn có theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-187">However, if you create a new instance of a **Panel Layout** type of hosted control, `SetVisualProperty` will be available by default.</span></span>  

1. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

2. <span data-ttu-id="a2ae8-188">Bấm **Kiểm soát Tổ chức**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-188">Click **Hosted Controls**.</span></span>  

3. <span data-ttu-id="a2ae8-189">Bấm vào **Bố cục Chính** trong danh sách kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-189">Click **Main Layout** in the list of hosted controls.</span></span>  

   > [!NOTE]
   >  <span data-ttu-id="a2ae8-190">The **Main Layout** hosted control is available when you deploy the Base sample application in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-190">The **Main Layout** hosted control is available when you deploy the Base sample application in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span>  

4. <span data-ttu-id="a2ae8-191">Bấm vào mũi tên xuống bên cạnh **Bố cục chính**, rồi bấm vào **Hành động UII**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-191">Click the down arrow next to **Main layout**, and then click **UII Actions**.</span></span>  

   <span data-ttu-id="a2ae8-192">![Add UII action](../unified-service-desk/media/usd-adduiiaction.png "Add UII action")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-192">![Add UII action](../unified-service-desk/media/usd-adduiiaction.png "Add UII action")</span></span>  

5. <span data-ttu-id="a2ae8-193">Bấm vào **Thêm Hoạt động UII mới**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-193">Click **Add New UII Action**.</span></span>  

6. <span data-ttu-id="a2ae8-194">Trên trang **Hành động UII Mới**, nhập `SetVisualProperty` vào trường **Tên** rồi bấm vào **Lưu và Đóng**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-194">On the **New UII Action** page, type `SetVisualProperty` in the **Name** field, and then click **Save and Close**.</span></span>  

   <span data-ttu-id="a2ae8-195">![Create a UII action for Main Layout hosted control](../unified-service-desk/media/usd-createuiiaction.png "Create a UII action for Main Layout hosted control")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-195">![Create a UII action for Main Layout hosted control](../unified-service-desk/media/usd-createuiiaction.png "Create a UII action for Main Layout hosted control")</span></span>  

    <span data-ttu-id="a2ae8-196">Cuộc gọi hành động mới được thêm vào kiểm soát tổ chức **Bố cục chính** và sẵn sàng được sử dụng.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-196">The new action call gets added to the **Main layout** hosted control, and is ready to be used.</span></span>  

7. <span data-ttu-id="a2ae8-197">Trên ngăn điều hướng, bấm vào **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-197">On the navigation pane, click **Unified Service Desk**.</span></span>  

8. <span data-ttu-id="a2ae8-198">Bấm **Cuộc gọi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-198">Click **Action Calls**.</span></span>  

9. <span data-ttu-id="a2ae8-199">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-199">Click **New**.</span></span>  

10. <span data-ttu-id="a2ae8-200">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-200">On the **New Action Call** page, specify the following values.</span></span>  


    |     <span data-ttu-id="a2ae8-201">Trường</span><span class="sxs-lookup"><span data-stu-id="a2ae8-201">Field</span></span>      |                                                                                              <span data-ttu-id="a2ae8-202">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a2ae8-202">Value</span></span>                                                                                               |
    |----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    |      <span data-ttu-id="a2ae8-203">Tên</span><span class="sxs-lookup"><span data-stu-id="a2ae8-203">Name</span></span>      |                                                                                <span data-ttu-id="a2ae8-204">Mẫu: Mở rộng Hành động Bảng điều khiển Phải</span><span class="sxs-lookup"><span data-stu-id="a2ae8-204">Sample: Expand Right Panel Action</span></span>                                                                                 |
    | <span data-ttu-id="a2ae8-205">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="a2ae8-205">Hosted Control</span></span> | <span data-ttu-id="a2ae8-206">Main Layout **Note:**  The **Main Layout** hosted control is available when you deploy the Base sample application in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-206">Main Layout **Note:**  The **Main Layout** hosted control is available when you deploy the Base sample application in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span> |
    |     <span data-ttu-id="a2ae8-207">Hành động</span><span class="sxs-lookup"><span data-stu-id="a2ae8-207">Action</span></span>     |                                                                                        <span data-ttu-id="a2ae8-208">SetVisualProperty</span><span class="sxs-lookup"><span data-stu-id="a2ae8-208">SetVisualProperty</span></span>                                                                                         |
    |      <span data-ttu-id="a2ae8-209">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="a2ae8-209">Data</span></span>      |                                                           <span data-ttu-id="a2ae8-210">elementname=RightPanelExpander</span><span class="sxs-lookup"><span data-stu-id="a2ae8-210">elementname=RightPanelExpander</span></span><br /><span data-ttu-id="a2ae8-211">propertyname=IsExpanded</span><span class="sxs-lookup"><span data-stu-id="a2ae8-211">propertyname=IsExpanded</span></span><br /><span data-ttu-id="a2ae8-212">value=true</span><span class="sxs-lookup"><span data-stu-id="a2ae8-212">value=true</span></span>                                                            |

    <span data-ttu-id="a2ae8-213">![Create action call](../unified-service-desk/media/usd-expandrightpanelaction.png "Create action call")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-213">![Create action call](../unified-service-desk/media/usd-expandrightpanelaction.png "Create action call")</span></span>  

11. <span data-ttu-id="a2ae8-214">Click **Save and Close**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-214">Click **Save and Close**.</span></span>  

12. <span data-ttu-id="a2ae8-215">Bấm vào **Mới** để tạo cuộc gọi hành động mới.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-215">Click **New** to create another action call.</span></span>  

13. <span data-ttu-id="a2ae8-216">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="a2ae8-216">On the **New Action Call** page, specify the following values:</span></span>  


    |     <span data-ttu-id="a2ae8-217">Trường</span><span class="sxs-lookup"><span data-stu-id="a2ae8-217">Field</span></span>      |                                                                                              <span data-ttu-id="a2ae8-218">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a2ae8-218">Value</span></span>                                                                                               |
    |----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    |      <span data-ttu-id="a2ae8-219">Tên</span><span class="sxs-lookup"><span data-stu-id="a2ae8-219">Name</span></span>      |                                                                               <span data-ttu-id="a2ae8-220">Mẫu: Thu hẹp Hành động Bảng điều khiển Phải</span><span class="sxs-lookup"><span data-stu-id="a2ae8-220">Sample: Collapse Right Panel Action</span></span>                                                                                |
    | <span data-ttu-id="a2ae8-221">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="a2ae8-221">Hosted Control</span></span> | <span data-ttu-id="a2ae8-222">Main Layout **Note:**  The **Main Layout** hosted control is available when you deploy the Base sample application in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-222">Main Layout **Note:**  The **Main Layout** hosted control is available when you deploy the Base sample application in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span> |
    |     <span data-ttu-id="a2ae8-223">Hành động</span><span class="sxs-lookup"><span data-stu-id="a2ae8-223">Action</span></span>     |                                                                                        <span data-ttu-id="a2ae8-224">SetVisualProperty</span><span class="sxs-lookup"><span data-stu-id="a2ae8-224">SetVisualProperty</span></span>                                                                                         |
    |      <span data-ttu-id="a2ae8-225">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="a2ae8-225">Data</span></span>      |                                                           <span data-ttu-id="a2ae8-226">elementname=RightPanelExpander</span><span class="sxs-lookup"><span data-stu-id="a2ae8-226">elementname=RightPanelExpander</span></span><br /><span data-ttu-id="a2ae8-227">propertyname=IsExpanded</span><span class="sxs-lookup"><span data-stu-id="a2ae8-227">propertyname=IsExpanded</span></span><br /><span data-ttu-id="a2ae8-228">value=false</span><span class="sxs-lookup"><span data-stu-id="a2ae8-228">value=false</span></span>                                                           |

    <span data-ttu-id="a2ae8-229">![Create action call](../unified-service-desk/media/usd-collapserightpanelaction.png "Create action call")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-229">![Create action call](../unified-service-desk/media/usd-collapserightpanelaction.png "Create action call")</span></span>  

14. <span data-ttu-id="a2ae8-230">Click **Save and Close**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-230">Click **Save and Close**.</span></span>  

15. <span data-ttu-id="a2ae8-231">Go to **Unified Service Desk** page, and then click **Events**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-231">Go to **Unified Service Desk** page, and then click **Events**.</span></span>  

16. <span data-ttu-id="a2ae8-232">Search for the `SessionNew` event, and then click it to open the event configuration page.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-232">Search for the `SessionNew` event, and then click it to open the event configuration page.</span></span>  

17. <span data-ttu-id="a2ae8-233">Click the **Add Action Call record** button to add the action call.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-233">Click the **Add Action Call record** button to add the action call.</span></span>  

    <span data-ttu-id="a2ae8-234">![Add action to event](../unified-service-desk/media/usd-addactiontoevent.png "Add action to event")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-234">![Add action to event](../unified-service-desk/media/usd-addactiontoevent.png "Add action to event")</span></span>  

18. <span data-ttu-id="a2ae8-235">Type `Sample: Expand Right Panel Action` in the search box, and press ENTER or click the search button to add the action to the event.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-235">Type `Sample: Expand Right Panel Action` in the search box, and press ENTER or click the search button to add the action to the event.</span></span> <span data-ttu-id="a2ae8-236">Change the **Order** of the added action to 2, and then click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-236">Change the **Order** of the added action to 2, and then click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner.</span></span>  

19. <span data-ttu-id="a2ae8-237">Go to **Unified Service Desk** page, and then click **Events**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-237">Go to **Unified Service Desk** page, and then click **Events**.</span></span>  

20. <span data-ttu-id="a2ae8-238">Search for the `SessionClosed` event for the **Dynamics 365 for Customer Engagement apps Global Manager** hosted control, and then click it to open the event configuration page.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-238">Search for the `SessionClosed` event for the **Dynamics 365 for Customer Engagement apps Global Manager** hosted control, and then click it to open the event configuration page.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="a2ae8-239">Ensure that you are editing the configuration of the `SessionClosed` event for the **Dynamics 365 for Customer Engagement apps Global Manager** hosted control.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-239">Ensure that you are editing the configuration of the `SessionClosed` event for the **Dynamics 365 for Customer Engagement apps Global Manager** hosted control.</span></span>  

21. <span data-ttu-id="a2ae8-240">Click the **Add Action Call record** button to add the action call.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-240">Click the **Add Action Call record** button to add the action call.</span></span>  

    <span data-ttu-id="a2ae8-241">![Add action call to event](../unified-service-desk/media/usd-addactiontosessionclosedevent.png "Add action call to event")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-241">![Add action call to event](../unified-service-desk/media/usd-addactiontosessionclosedevent.png "Add action call to event")</span></span>  

22. <span data-ttu-id="a2ae8-242">Type `Sample: Collapse Right Panel Action` in the search box, and press ENTER or click the search button to add the action to the event.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-242">Type `Sample: Collapse Right Panel Action` in the search box, and press ENTER or click the search button to add the action to the event.</span></span> <span data-ttu-id="a2ae8-243">Change the order of the added action to 1, and then click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-243">Change the order of the added action to 1, and then click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner.</span></span>  

<a name="Step4"></a>   
## <a name="step-4-configure-an-action-call-to-automatically-search-the-knowledge-base-using-the-incident-case-title"></a><span data-ttu-id="a2ae8-244">Bước 4: Đặt cấu hình một cuộc gọi hành động để tự động tìm kiếm cơ sở kiến thức bằng cách sử dụng tiêu đề sự cố (trường hợp)</span><span class="sxs-lookup"><span data-stu-id="a2ae8-244">Step 4: Configure an action call to automatically search the knowledge base using the incident (case) title</span></span>  
 <span data-ttu-id="a2ae8-245">Tạo một cuộc gọi hành động để tự động điền tiêu đề trường hợp trong kiểm soát tìm kiếm cơ sở kiến thức để tìm kiếm dựa trên tên tiêu đề trường hợp.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-245">Create an action call to automatically populate the case title in the knowledge base search control to search based on the case title name.</span></span> <span data-ttu-id="a2ae8-246">After creating the action, you’ll add it to the `BrowserDocumentComplete` event of the **Incident** hosted control to fire this action after the case records have loaded in the agent desktop.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-246">After creating the action, you’ll add it to the `BrowserDocumentComplete` event of the **Incident** hosted control to fire this action after the case records have loaded in the agent desktop.</span></span>  

> [!NOTE]
>  <span data-ttu-id="a2ae8-247">The **Incident** hosted control is created when you deploy the Base sample application in your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-247">The **Incident** hosted control is created when you deploy the Base sample application in your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps instance.</span></span>  

1. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

2. <span data-ttu-id="a2ae8-248">Bấm **Cuộc gọi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-248">Click **Action Calls**.</span></span>  

3. <span data-ttu-id="a2ae8-249">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-249">Click **New**.</span></span>  

4. <span data-ttu-id="a2ae8-250">Trên trang **Cuộc gọi Hành động Mới**, chỉ định các giá trị sau</span><span class="sxs-lookup"><span data-stu-id="a2ae8-250">On the **New Action Call** page, specify the following values</span></span>  

   |<span data-ttu-id="a2ae8-251">Trường</span><span class="sxs-lookup"><span data-stu-id="a2ae8-251">Field</span></span>|<span data-ttu-id="a2ae8-252">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a2ae8-252">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="a2ae8-253">Tên</span><span class="sxs-lookup"><span data-stu-id="a2ae8-253">Name</span></span>|<span data-ttu-id="a2ae8-254">Mẫu: Tìm kiếm KB bằng Hành động Tiêu đề Sự cố (Trường hợp)</span><span class="sxs-lookup"><span data-stu-id="a2ae8-254">Sample: Search KB with Incident (Case) Title Action</span></span>|  
   |<span data-ttu-id="a2ae8-255">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="a2ae8-255">Hosted Control</span></span>|<span data-ttu-id="a2ae8-256">Sample KB Search</span><span class="sxs-lookup"><span data-stu-id="a2ae8-256">Sample KB Search</span></span>|  
   |<span data-ttu-id="a2ae8-257">Hành động</span><span class="sxs-lookup"><span data-stu-id="a2ae8-257">Action</span></span>|<span data-ttu-id="a2ae8-258">Search</span><span class="sxs-lookup"><span data-stu-id="a2ae8-258">Search</span></span>|  
   |<span data-ttu-id="a2ae8-259">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="a2ae8-259">Data</span></span>|<span data-ttu-id="a2ae8-260">query=[[incident.title]+]</span><span class="sxs-lookup"><span data-stu-id="a2ae8-260">query=[[incident.title]+]</span></span>|  

   > [!TIP]
   >  <span data-ttu-id="a2ae8-261">Bạn có thể sử dụng tham số dữ liệu bổ sung trong hành động `Search` để xác định tham số tìm kiếm cơ sở kiến thức như số lượng kết quả tìm kiếm để trở về, loại bài viết cơ sở kiến thức được lựa chọn tìm kiếm, và sắp xếp.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-261">You can use additional data parameters in the `Search` action to specify knowledge base search parameters such as the number of search results to return, the type of knowledge base articles to be searched, and sorting options.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a2ae8-262">[Search](../unified-service-desk/km-control-hosted-control.md#Search)</span><span class="sxs-lookup"><span data-stu-id="a2ae8-262">[Search](../unified-service-desk/km-control-hosted-control.md#Search)</span></span>  

   <span data-ttu-id="a2ae8-263">![Create an action call](../unified-service-desk/media/usd-searchkbwithcasetitleaction.png "Create an action call")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-263">![Create an action call](../unified-service-desk/media/usd-searchkbwithcasetitleaction.png "Create an action call")</span></span>  

5. <span data-ttu-id="a2ae8-264">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-264">Click **Save**.</span></span>  

6. <span data-ttu-id="a2ae8-265">On the navigation pane, click **Unified Service Desk**, and then click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-265">On the navigation pane, click **Unified Service Desk**, and then click **Hosted Controls**.</span></span>  

7. <span data-ttu-id="a2ae8-266">Bấm vào **Sự cố** từ danh sách kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-266">Click **Incident** from the list of hosted controls.</span></span>  

8. <span data-ttu-id="a2ae8-267">Bấm vào mũi tên xuống bên cạnh **Sự cố** rồi bấm vào **Sự kiện**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-267">Click the down arrow next to **Incident**, and then click **Events**.</span></span>  

   <span data-ttu-id="a2ae8-268">![View events for the Incident hosted control](../unified-service-desk/media/usd-addactiontoincidentevent.png "View events for the Incident hosted control")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-268">![View events for the Incident hosted control](../unified-service-desk/media/usd-addactiontoincidentevent.png "View events for the Incident hosted control")</span></span>  

9. <span data-ttu-id="a2ae8-269">Trong danh sách sự kiện cho kiểm soát tổ chức **Sự cố**, bấm vào `BrowserDocumentComplete`.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-269">In the events list for the **Incident** hosted control, click `BrowserDocumentComplete`.</span></span>  

10. <span data-ttu-id="a2ae8-270">Click the **Add Action Call record** button to add the action call.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-270">Click the **Add Action Call record** button to add the action call.</span></span>  

    <span data-ttu-id="a2ae8-271">![Add action to BrowserDocumentComplete event](../unified-service-desk/media/usd-addactiontobrowserdocumentcomplete.png "Add action to BrowserDocumentComplete event")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-271">![Add action to BrowserDocumentComplete event](../unified-service-desk/media/usd-addactiontobrowserdocumentcomplete.png "Add action to BrowserDocumentComplete event")</span></span>  

11. <span data-ttu-id="a2ae8-272">Type `Sample: Search KB with Incident (Case) Title Action` in the search box, and press ENTER or click the search button to add the action to the event.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-272">Type `Sample: Search KB with Incident (Case) Title Action` in the search box, and press ENTER or click the search button to add the action to the event.</span></span> <span data-ttu-id="a2ae8-273">Click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-273">Click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner.</span></span>  

> [!NOTE]
>  <span data-ttu-id="a2ae8-274">At this point, the knowledge base search control is configured to display knowledge bases from \Dynamics 365 for Customer Engagement apps in context with the currently opened case record.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-274">At this point, the knowledge base search control is configured to display knowledge bases from \Dynamics 365 for Customer Engagement apps in context with the currently opened case record.</span></span> <span data-ttu-id="a2ae8-275">Ngoài ra, bảng điều khiển tìm kiếm cơ sở kiến thức được cấu hình để tự động hiển thị khi một phiên được tạo và tự động ẩn khi bạn đóng phiên.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-275">Also, the knowledge base search panel is configured to automatically display when a session is created, and automatically hide when you close the session.</span></span> <span data-ttu-id="a2ae8-276">You can test this by running the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application and connecting to the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps instance where you performed steps 1 through 4 of this walkthrough.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-276">You can test this by running the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application and connecting to the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps instance where you performed steps 1 through 4 of this walkthrough.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)]  
> 
>  <span data-ttu-id="a2ae8-277">Perform the rest of the steps to display a knowledge base article from the search results in a tab, and configure contextual actions for a selected knowledge base article in the search panel such as copying an article link and associating the article to the current case.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-277">Perform the rest of the steps to display a knowledge base article from the search results in a tab, and configure contextual actions for a selected knowledge base article in the search panel such as copying an article link and associating the article to the current case.</span></span>  

<a name="Step5"></a>   
## <a name="step-5-configure-hosted-controls-and-action-calls-to-display-an-article-in-a-tab"></a><span data-ttu-id="a2ae8-278">Bước 5: Đặt cấu hình kiểm soát tổ chức và các cuộc gọi hành động để hiển thị một bài viết trong một tab</span><span class="sxs-lookup"><span data-stu-id="a2ae8-278">Step 5: Configure hosted controls and action calls to display an article in a tab</span></span>  
 <span data-ttu-id="a2ae8-279">Trong bước này, bạn sẽ:</span><span class="sxs-lookup"><span data-stu-id="a2ae8-279">In this step, you will:</span></span>  

-   <span data-ttu-id="a2ae8-280">Đặt cấu hình kiểm soát tổ chức loại **Ứng dụng Web Tiêu chuẩn** để hiển thị bài viết cơ sở kiến thức.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-280">Configure a hosted control of type **Standard Web Application** to display the knowledge base article.</span></span>  

-   <span data-ttu-id="a2ae8-281">Đặt cấu hình cuộc gọi hành động để hiển thị bài viết trong kiểm soát tổ chức có tiêu đề được bấm vào trong ngăn tìm kiếm cơ sở kiến thức.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-281">Configure action calls to display the article in the hosted control whose title is clicked in the knowledge base search pane.</span></span>  

-   <span data-ttu-id="a2ae8-282">Add the action calls to the [ResultOpen](../unified-service-desk/km-control-hosted-control.md#ResultOpen) event of the `KM Control` hosted control so that the action calls are executed when somebody clicks on the KB article title.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-282">Add the action calls to the [ResultOpen](../unified-service-desk/km-control-hosted-control.md#ResultOpen) event of the `KM Control` hosted control so that the action calls are executed when somebody clicks on the KB article title.</span></span>  

1. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

2. <span data-ttu-id="a2ae8-283">Bấm **Kiểm soát Tổ chức**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-283">Click **Hosted Controls**.</span></span>  

3. <span data-ttu-id="a2ae8-284">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-284">Click **New**.</span></span>  

4. <span data-ttu-id="a2ae8-285">On the **New Hosted Control** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-285">On the **New Hosted Control** page, specify the following values.</span></span>  

   |<span data-ttu-id="a2ae8-286">Trường</span><span class="sxs-lookup"><span data-stu-id="a2ae8-286">Field</span></span>|<span data-ttu-id="a2ae8-287">Value</span><span class="sxs-lookup"><span data-stu-id="a2ae8-287">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="a2ae8-288">Tên</span><span class="sxs-lookup"><span data-stu-id="a2ae8-288">Name</span></span>|<span data-ttu-id="a2ae8-289">Bài viết KB Mẫu</span><span class="sxs-lookup"><span data-stu-id="a2ae8-289">Sample KB Article</span></span>|  
   |<span data-ttu-id="a2ae8-290">Tên Hiển thị</span><span class="sxs-lookup"><span data-stu-id="a2ae8-290">Display Name</span></span>|<span data-ttu-id="a2ae8-291">[[Sample KB Article.question]+]</span><span class="sxs-lookup"><span data-stu-id="a2ae8-291">[[Sample KB Article.question]+]</span></span>|  
   |<span data-ttu-id="a2ae8-292">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="a2ae8-292">USD Component Type</span></span>|<span data-ttu-id="a2ae8-293">Ứng dụng web chuẩn</span><span class="sxs-lookup"><span data-stu-id="a2ae8-293">Standard Web Application</span></span>|  
   |<span data-ttu-id="a2ae8-294">Cho phép nhiều trang</span><span class="sxs-lookup"><span data-stu-id="a2ae8-294">Allow Multiple Pages</span></span>|<span data-ttu-id="a2ae8-295">No</span><span class="sxs-lookup"><span data-stu-id="a2ae8-295">No</span></span>|  
   |<span data-ttu-id="a2ae8-296">Loại lưu trữ</span><span class="sxs-lookup"><span data-stu-id="a2ae8-296">Hosting Type</span></span>|<span data-ttu-id="a2ae8-297">WPF nội bộ</span><span class="sxs-lookup"><span data-stu-id="a2ae8-297">Internal WPF</span></span>|  
   |<span data-ttu-id="a2ae8-298">Application is Global</span><span class="sxs-lookup"><span data-stu-id="a2ae8-298">Application is Global</span></span>|<span data-ttu-id="a2ae8-299">Clear</span><span class="sxs-lookup"><span data-stu-id="a2ae8-299">Clear</span></span>|  
   |<span data-ttu-id="a2ae8-300">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="a2ae8-300">Display Group</span></span>|<span data-ttu-id="a2ae8-301">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="a2ae8-301">MainPanel</span></span>|  

   <span data-ttu-id="a2ae8-302">![New hosted control for displaying the KB article](../unified-service-desk/media/usd-samplekbarticlehostedcontrol.png "New hosted control for displaying the KB article")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-302">![New hosted control for displaying the KB article](../unified-service-desk/media/usd-samplekbarticlehostedcontrol.png "New hosted control for displaying the KB article")</span></span>  

5. <span data-ttu-id="a2ae8-303">Click **Save and Close**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-303">Click **Save and Close**.</span></span>  

6. <span data-ttu-id="a2ae8-304">You’ll now create an action call to set the context of the selected article in the knowledge base search pane.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-304">You’ll now create an action call to set the context of the selected article in the knowledge base search pane.</span></span> <span data-ttu-id="a2ae8-305">The context information is required if you want to perform additional actions on the currently displayed knowledge base article such as dynamically displaying the tab title based on the knowledge base article question title, copying the link of the article, and associating or dissociating an article with an incident (case) record.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-305">The context information is required if you want to perform additional actions on the currently displayed knowledge base article such as dynamically displaying the tab title based on the knowledge base article question title, copying the link of the article, and associating or dissociating an article with an incident (case) record.</span></span>  

[!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]

7. <span data-ttu-id="a2ae8-306">Click **Action Calls**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-306">Click **Action Calls**.</span></span>  

8. <span data-ttu-id="a2ae8-307">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-307">Click **New**.</span></span>  

9. <span data-ttu-id="a2ae8-308">On the **New Action Call** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-308">On the **New Action Call** page, specify the following values.</span></span>  

    |<span data-ttu-id="a2ae8-309">Trường</span><span class="sxs-lookup"><span data-stu-id="a2ae8-309">Field</span></span>|<span data-ttu-id="a2ae8-310">Value</span><span class="sxs-lookup"><span data-stu-id="a2ae8-310">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="a2ae8-311">Tên</span><span class="sxs-lookup"><span data-stu-id="a2ae8-311">Name</span></span>|<span data-ttu-id="a2ae8-312">Mẫu: Thiết lập Hành động Ngữ cảnh Bài viết KB</span><span class="sxs-lookup"><span data-stu-id="a2ae8-312">Sample: Set KB Article Context Action</span></span>|  
    |<span data-ttu-id="a2ae8-313">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="a2ae8-313">Order</span></span>|<span data-ttu-id="a2ae8-314">1</span><span class="sxs-lookup"><span data-stu-id="a2ae8-314">1</span></span>|  
    |<span data-ttu-id="a2ae8-315">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="a2ae8-315">Hosted Control</span></span>|<span data-ttu-id="a2ae8-316">Sample KB Search</span><span class="sxs-lookup"><span data-stu-id="a2ae8-316">Sample KB Search</span></span>|  
    |<span data-ttu-id="a2ae8-317">Hành động</span><span class="sxs-lookup"><span data-stu-id="a2ae8-317">Action</span></span>|<span data-ttu-id="a2ae8-318">SetArticleContext</span><span class="sxs-lookup"><span data-stu-id="a2ae8-318">SetArticleContext</span></span>|  
    |<span data-ttu-id="a2ae8-319">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="a2ae8-319">Data</span></span>|<span data-ttu-id="a2ae8-320">articleapplication=Sample KB Article</span><span class="sxs-lookup"><span data-stu-id="a2ae8-320">articleapplication=Sample KB Article</span></span><br /><span data-ttu-id="a2ae8-321">articledata=[[postdata]+]</span><span class="sxs-lookup"><span data-stu-id="a2ae8-321">articledata=[[postdata]+]</span></span>|  

   <span data-ttu-id="a2ae8-322">![Action call for setting article context](../unified-service-desk/media/usd-actioncallsetarticlecontext.png "Action call for setting article context")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-322">![Action call for setting article context](../unified-service-desk/media/usd-actioncallsetarticlecontext.png "Action call for setting article context")</span></span>  

10. <span data-ttu-id="a2ae8-323">Click **Save and Close**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-323">Click **Save and Close**.</span></span>  

11. <span data-ttu-id="a2ae8-324">Bấm vào **Mới** để tạo cuộc gọi hành động khác để hiển thị bài viết trong kiểm soát tổ chức được tạo trước đây trong bước này.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-324">Click **New** to create another action call for displaying the article in the hosted control created earlier in this step.</span></span>  

12. <span data-ttu-id="a2ae8-325">On the **New Action Call** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-325">On the **New Action Call** page, specify the following values.</span></span>  

   |<span data-ttu-id="a2ae8-326">Trường</span><span class="sxs-lookup"><span data-stu-id="a2ae8-326">Field</span></span>|<span data-ttu-id="a2ae8-327">Value</span><span class="sxs-lookup"><span data-stu-id="a2ae8-327">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="a2ae8-328">Tên</span><span class="sxs-lookup"><span data-stu-id="a2ae8-328">Name</span></span>|<span data-ttu-id="a2ae8-329">Mẫu: Mở Hành động Bài viết KB</span><span class="sxs-lookup"><span data-stu-id="a2ae8-329">Sample: Open KB Article Action</span></span>|  
   |<span data-ttu-id="a2ae8-330">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="a2ae8-330">Order</span></span>|<span data-ttu-id="a2ae8-331">2</span><span class="sxs-lookup"><span data-stu-id="a2ae8-331">2</span></span>|  
   |<span data-ttu-id="a2ae8-332">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="a2ae8-332">Hosted Control</span></span>|<span data-ttu-id="a2ae8-333">Sample KB Article</span><span class="sxs-lookup"><span data-stu-id="a2ae8-333">Sample KB Article</span></span>|  
   |<span data-ttu-id="a2ae8-334">Hành động</span><span class="sxs-lookup"><span data-stu-id="a2ae8-334">Action</span></span>|<span data-ttu-id="a2ae8-335">Navigate</span><span class="sxs-lookup"><span data-stu-id="a2ae8-335">Navigate</span></span>|  
   |<span data-ttu-id="a2ae8-336">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="a2ae8-336">Data</span></span>|<span data-ttu-id="a2ae8-337">url=[[Sample KB Search.articleurl]]</span><span class="sxs-lookup"><span data-stu-id="a2ae8-337">url=[[Sample KB Search.articleurl]]</span></span><br /><span data-ttu-id="a2ae8-338">header=[[header]+]</span><span class="sxs-lookup"><span data-stu-id="a2ae8-338">header=[[header]+]</span></span><br /><span data-ttu-id="a2ae8-339">postdata=[[postdata]]</span><span class="sxs-lookup"><span data-stu-id="a2ae8-339">postdata=[[postdata]]</span></span>|  

   <span data-ttu-id="a2ae8-340">![Action call to display the KB article](../unified-service-desk/media/usd-actioncallopenkbarticle.png "Action call to display the KB article")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-340">![Action call to display the KB article](../unified-service-desk/media/usd-actioncallopenkbarticle.png "Action call to display the KB article")</span></span>  

13. <span data-ttu-id="a2ae8-341">Click **Save and Close**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-341">Click **Save and Close**.</span></span>  

14. <span data-ttu-id="a2ae8-342">Bấm vào **Mới** để tạo cuộc gọi hành động khác để hiển thị kiểm soát tổ chức được tạo trước đây trong bước này trong bảng điều khiển chính.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-342">Click **New** to create another action call for displaying the hosted control created earlier in this step in the main panel.</span></span>  

15. <span data-ttu-id="a2ae8-343">Trên trang **Cuộc gọi Hành động Mới**, chỉ định các giá trị sau</span><span class="sxs-lookup"><span data-stu-id="a2ae8-343">On the **New Action Call** page, specify the following values</span></span>  

   |<span data-ttu-id="a2ae8-344">Trường</span><span class="sxs-lookup"><span data-stu-id="a2ae8-344">Field</span></span>|<span data-ttu-id="a2ae8-345">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a2ae8-345">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="a2ae8-346">Tên</span><span class="sxs-lookup"><span data-stu-id="a2ae8-346">Name</span></span>|<span data-ttu-id="a2ae8-347">Mẫu: Hiển thị Hành động Tab Bài viết KB</span><span class="sxs-lookup"><span data-stu-id="a2ae8-347">Sample: Show KB Article Tab Action</span></span>|  
   |<span data-ttu-id="a2ae8-348">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="a2ae8-348">Order</span></span>|<span data-ttu-id="a2ae8-349">50</span><span class="sxs-lookup"><span data-stu-id="a2ae8-349">50</span></span>|  
   |<span data-ttu-id="a2ae8-350">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="a2ae8-350">Hosted Control</span></span>|<span data-ttu-id="a2ae8-351">Dynamics 365 for Customer Engagement apps Global Manager</span><span class="sxs-lookup"><span data-stu-id="a2ae8-351">Dynamics 365 for Customer Engagement apps Global Manager</span></span>|  
   |<span data-ttu-id="a2ae8-352">Hành động</span><span class="sxs-lookup"><span data-stu-id="a2ae8-352">Action</span></span>|<span data-ttu-id="a2ae8-353">Hiển thị tab</span><span class="sxs-lookup"><span data-stu-id="a2ae8-353">ShowTab</span></span>|  
   |<span data-ttu-id="a2ae8-354">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="a2ae8-354">Data</span></span>|<span data-ttu-id="a2ae8-355">Sample KB Article</span><span class="sxs-lookup"><span data-stu-id="a2ae8-355">Sample KB Article</span></span>|  

   <span data-ttu-id="a2ae8-356">![Action call to display the KB article in a tab](../unified-service-desk/media/usd-actionshowkbarticletab.png "Action call to display the KB article in a tab")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-356">![Action call to display the KB article in a tab](../unified-service-desk/media/usd-actionshowkbarticletab.png "Action call to display the KB article in a tab")</span></span>  

16. <span data-ttu-id="a2ae8-357">Click **Save and Close**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-357">Click **Save and Close**.</span></span>  

17. <span data-ttu-id="a2ae8-358">Now, you’ll add all the three new actions created in this step to the [ResultOpen](../unified-service-desk/km-control-hosted-control.md#ResultOpen) event of the **KM Control** hosted control that you created earlier.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-358">Now, you’ll add all the three new actions created in this step to the [ResultOpen](../unified-service-desk/km-control-hosted-control.md#ResultOpen) event of the **KM Control** hosted control that you created earlier.</span></span>  

     <span data-ttu-id="a2ae8-359">Trên ngăn điều hướng, bấm vào **Unified Service Desk** rồi bấm vào **Sự kiện**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-359">On the navigation pane, click **Unified Service Desk**, and then click **Events**.</span></span>  

18. <span data-ttu-id="a2ae8-360">Tìm kiếm sự kiện `ResultOpen` và bấm vào tên sự kiện để mở ngăn thông tin sự kiện.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-360">Search for `ResultOpen` event, and click the event name to open the event information page.</span></span>  

19. <span data-ttu-id="a2ae8-361">Click the **Add Action Call record** button to add an action call.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-361">Click the **Add Action Call record** button to add an action call.</span></span>  

20. <span data-ttu-id="a2ae8-362">Type `Sample: Set KB Article Context Action` in the search box, and press ENTER or click the search button to add the action to the event.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-362">Type `Sample: Set KB Article Context Action` in the search box, and press ENTER or click the search button to add the action to the event.</span></span>  

21. <span data-ttu-id="a2ae8-363">Repeat the previous step with the `Sample: Open KB Article Action` and `Sample: Show KB Article Tab Action` action calls to add them to the event.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-363">Repeat the previous step with the `Sample: Open KB Article Action` and `Sample: Show KB Article Tab Action` action calls to add them to the event.</span></span>  

22. <span data-ttu-id="a2ae8-364">Click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-364">Click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner.</span></span>  

<a name="Step6"></a>   
## <a name="step-6-configure-contextual-actions-for-the-knowledge-base-article-in-the-tab"></a><span data-ttu-id="a2ae8-365">Bước 6: Đặt cấu hình các hành động theo ngữ cảnh cho bài viết cơ sở kiến thức trong tab</span><span class="sxs-lookup"><span data-stu-id="a2ae8-365">Step 6: Configure contextual actions for the knowledge base article in the tab</span></span>  
 <span data-ttu-id="a2ae8-366">In this step, you’ll add buttons on the toolbar of the hosted control configured in the previous step (Step 5) and attach action calls to the buttons so that when the button is clicked, appropriate actions are performed in the context of the currently displayed article in the tab. You’ll configure a toolbar with two buttons and respective action calls for the buttons.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-366">In this step, you’ll add buttons on the toolbar of the hosted control configured in the previous step (Step 5) and attach action calls to the buttons so that when the button is clicked, appropriate actions are performed in the context of the currently displayed article in the tab. You’ll configure a toolbar with two buttons and respective action calls for the buttons.</span></span>  

1. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

2. <span data-ttu-id="a2ae8-367">Bấm vào **Thanh công cụ**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-367">Click **Toolbars**.</span></span>  

3. <span data-ttu-id="a2ae8-368">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-368">Click **New**.</span></span>  

4. <span data-ttu-id="a2ae8-369">Trên trang **Thanh công cụ Mới**, nhập `Sample: KB Toolbar` vào trường **Tên** và bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-369">On the **New Toolbar** page, type `Sample: KB Toolbar` in the **Name** field, and click **Save**.</span></span>  

5. <span data-ttu-id="a2ae8-370">In the **Buttons** area, click the **+** symbol to add buttons to the toolbar.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-370">In the **Buttons** area, click the **+** symbol to add buttons to the toolbar.</span></span>  

6. <span data-ttu-id="a2ae8-371">Trên trang **Nút thanh công cụ mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-371">On the **New Toolbar Button** page, specify the following values.</span></span>  

   |<span data-ttu-id="a2ae8-372">Trường</span><span class="sxs-lookup"><span data-stu-id="a2ae8-372">Field</span></span>|<span data-ttu-id="a2ae8-373">Value</span><span class="sxs-lookup"><span data-stu-id="a2ae8-373">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="a2ae8-374">Tên</span><span class="sxs-lookup"><span data-stu-id="a2ae8-374">Name</span></span>|<span data-ttu-id="a2ae8-375">Sao chép Liên kết</span><span class="sxs-lookup"><span data-stu-id="a2ae8-375">Copy Link</span></span>|  
   |<span data-ttu-id="a2ae8-376">Văn bản nút</span><span class="sxs-lookup"><span data-stu-id="a2ae8-376">Button Text</span></span>|<span data-ttu-id="a2ae8-377">Sao chép Liên kết</span><span class="sxs-lookup"><span data-stu-id="a2ae8-377">Copy Link</span></span>|  
   |<span data-ttu-id="a2ae8-378">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="a2ae8-378">Order</span></span>|<span data-ttu-id="a2ae8-379">1 **Note:**  The **Order** field defines the position of buttons in the toolbar.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-379">1 **Note:**  The **Order** field defines the position of buttons in the toolbar.</span></span> <span data-ttu-id="a2ae8-380">Nút được sắp xếp từ trái sang phải hoặc trên xuống dưới theo một thứ tự tăng dần.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-380">Buttons are arranged from left to right or top to bottom in an ascending order.</span></span>|  

   <span data-ttu-id="a2ae8-381">![New toolbar button](../unified-service-desk/media/usd-newtoolbarbutton1.png "New toolbar button")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-381">![New toolbar button](../unified-service-desk/media/usd-newtoolbarbutton1.png "New toolbar button")</span></span>  

7. <span data-ttu-id="a2ae8-382">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-382">Click **Save**.</span></span>  

8. <span data-ttu-id="a2ae8-383">You’ll now create an action call for this button to copy the link of the currently displayed article when somebody clicks the button.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-383">You’ll now create an action call for this button to copy the link of the currently displayed article when somebody clicks the button.</span></span>  

    <span data-ttu-id="a2ae8-384">In the **Actions** area, click **+** on the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-384">In the **Actions** area, click **+** on the right corner to add an action call.</span></span>  

9. <span data-ttu-id="a2ae8-385">In the search box in the **Actions** area, press ENTER or click the search button.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-385">In the search box in the **Actions** area, press ENTER or click the search button.</span></span>  

10. <span data-ttu-id="a2ae8-386">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-386">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>  

    <span data-ttu-id="a2ae8-387">![Create a new action call for the toolbar button](../unified-service-desk/media/usd-actioncallfortoolbarbutton.png "Create a new action call for the toolbar button")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-387">![Create a new action call for the toolbar button](../unified-service-desk/media/usd-actioncallfortoolbarbutton.png "Create a new action call for the toolbar button")</span></span>  

11. <span data-ttu-id="a2ae8-388">On the **New Action Call** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-388">On the **New Action Call** page, specify the following values.</span></span>  


    |     <span data-ttu-id="a2ae8-389">Trường</span><span class="sxs-lookup"><span data-stu-id="a2ae8-389">Field</span></span>      |                 <span data-ttu-id="a2ae8-390">Value</span><span class="sxs-lookup"><span data-stu-id="a2ae8-390">Value</span></span>                 |
    |----------------|---------------------------------------|
    |      <span data-ttu-id="a2ae8-391">Tên</span><span class="sxs-lookup"><span data-stu-id="a2ae8-391">Name</span></span>      |  <span data-ttu-id="a2ae8-392">Mẫu: Sao chép Hành động Liên kết Bài viết KB</span><span class="sxs-lookup"><span data-stu-id="a2ae8-392">Sample: Copy KB Article Link Action</span></span>  |
    | <span data-ttu-id="a2ae8-393">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="a2ae8-393">Hosted Control</span></span> |      <span data-ttu-id="a2ae8-394">Dynamics 365 for Customer Engagement apps Global Manager</span><span class="sxs-lookup"><span data-stu-id="a2ae8-394">Dynamics 365 for Customer Engagement apps Global Manager</span></span>      |
    |     <span data-ttu-id="a2ae8-395">Hành động</span><span class="sxs-lookup"><span data-stu-id="a2ae8-395">Action</span></span>     |            <span data-ttu-id="a2ae8-396">CopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="a2ae8-396">CopyToClipboard</span></span>            |
    |      <span data-ttu-id="a2ae8-397">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="a2ae8-397">Data</span></span>      | <span data-ttu-id="a2ae8-398">data=[[Sample KB Article.publicUrl]+]</span><span class="sxs-lookup"><span data-stu-id="a2ae8-398">data=[[Sample KB Article.publicUrl]+]</span></span> |


12. <span data-ttu-id="a2ae8-399">Click **Save and Close**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-399">Click **Save and Close**.</span></span> <span data-ttu-id="a2ae8-400">Cuộc gọi hành động mới được thêm vào nút **Sao chép Liên kết**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-400">The new action call gets added to the **Copy Link** button.</span></span>  

13. <span data-ttu-id="a2ae8-401">Click **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner of the page.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-401">Click **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner of the page.</span></span>  

14. <span data-ttu-id="a2ae8-402">Đóng trang nút thanh công cụ **Sao chép Liên kết** và trả lại trang **Mẫu: Thanh công cụ KB** để thêm một nút khác.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-402">Close the **Copy Link** toolbar button page, and return to the **Sample: KB Toolbar** page to add another button.</span></span>  

15. <span data-ttu-id="a2ae8-403">In the **Buttons** area, click the + button to add buttons to the toolbar.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-403">In the **Buttons** area, click the + button to add buttons to the toolbar.</span></span>  

16. <span data-ttu-id="a2ae8-404">On the **New Toolbar Button** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-404">On the **New Toolbar Button** page, specify the following values.</span></span>  


    |    <span data-ttu-id="a2ae8-405">Trường</span><span class="sxs-lookup"><span data-stu-id="a2ae8-405">Field</span></span>    |                                                                              <span data-ttu-id="a2ae8-406">Value</span><span class="sxs-lookup"><span data-stu-id="a2ae8-406">Value</span></span>                                                                               |
    |-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    |    <span data-ttu-id="a2ae8-407">Tên</span><span class="sxs-lookup"><span data-stu-id="a2ae8-407">Name</span></span>     |                                                                           <span data-ttu-id="a2ae8-408">Liên kết Bài viết</span><span class="sxs-lookup"><span data-stu-id="a2ae8-408">Link Article</span></span>                                                                           |
    | <span data-ttu-id="a2ae8-409">Văn bản nút</span><span class="sxs-lookup"><span data-stu-id="a2ae8-409">Button Text</span></span> |                                                                           <span data-ttu-id="a2ae8-410">Liên kết Bài viết</span><span class="sxs-lookup"><span data-stu-id="a2ae8-410">Link Article</span></span>                                                                           |
    |    <span data-ttu-id="a2ae8-411">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="a2ae8-411">Order</span></span>    | <span data-ttu-id="a2ae8-412">2 **Note:**  The **Order** field defines the position of buttons in the toolbar.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-412">2 **Note:**  The **Order** field defines the position of buttons in the toolbar.</span></span> <span data-ttu-id="a2ae8-413">Nút được sắp xếp từ trái sang phải hoặc trên xuống dưới theo một thứ tự tăng dần.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-413">Buttons are arranged from left to right or top to bottom in an ascending order.</span></span> |


17. <span data-ttu-id="a2ae8-414">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-414">Click **Save**.</span></span>  

18. <span data-ttu-id="a2ae8-415">Bây giờ bạn sẽ tạo ra một cuộc gọi hành động cho nút này để liên kết bài viết hiện được hiển thị với bản ghi trường hợp hiện tại.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-415">You’ll now create an action call for this button to associate the currently displayed article with the current case record.</span></span>  

     <span data-ttu-id="a2ae8-416">In the **Actions** area, click **+** on the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-416">In the **Actions** area, click **+** on the right corner to add an action call.</span></span>  

19. <span data-ttu-id="a2ae8-417">In the search box in the **Actions** area, press ENTER or click the search button.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-417">In the search box in the **Actions** area, press ENTER or click the search button.</span></span>  

20. <span data-ttu-id="a2ae8-418">Trong hộp kết quả tìm kiếm, bấm vào **Mới** ở góc dưới bên phải để tạo cuộc gọi hành động cho nút thanh công cụ này.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-418">In the search results box, click **New** in the lower-right corner to create an action call for this toolbar button.</span></span>  

21. <span data-ttu-id="a2ae8-419">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="a2ae8-419">On the **New Action Call** page, specify the following values:</span></span>  

    |<span data-ttu-id="a2ae8-420">Trường</span><span class="sxs-lookup"><span data-stu-id="a2ae8-420">Field</span></span>|<span data-ttu-id="a2ae8-421">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a2ae8-421">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="a2ae8-422">Tên</span><span class="sxs-lookup"><span data-stu-id="a2ae8-422">Name</span></span>|<span data-ttu-id="a2ae8-423">Mẫu: Liên kết Bài viết KB với Hành động Trường hợp</span><span class="sxs-lookup"><span data-stu-id="a2ae8-423">Sample: Associate KB Article to Case Action</span></span>|  
    |<span data-ttu-id="a2ae8-424">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="a2ae8-424">Hosted Control</span></span>|<span data-ttu-id="a2ae8-425">Sample KB Search</span><span class="sxs-lookup"><span data-stu-id="a2ae8-425">Sample KB Search</span></span>|  
    |<span data-ttu-id="a2ae8-426">Hành động</span><span class="sxs-lookup"><span data-stu-id="a2ae8-426">Action</span></span>|<span data-ttu-id="a2ae8-427">Liên kết</span><span class="sxs-lookup"><span data-stu-id="a2ae8-427">Associate</span></span>|  
    |<span data-ttu-id="a2ae8-428">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="a2ae8-428">Data</span></span>|<span data-ttu-id="a2ae8-429">entitytypename=incident</span><span class="sxs-lookup"><span data-stu-id="a2ae8-429">entitytypename=incident</span></span><br /><span data-ttu-id="a2ae8-430">recordid =[[incident.Id]]</span><span class="sxs-lookup"><span data-stu-id="a2ae8-430">recordid =[[incident.Id]]</span></span> <br /><span data-ttu-id="a2ae8-431">articleuniqueid=[[Sample KB Article.articleUId]]</span><span class="sxs-lookup"><span data-stu-id="a2ae8-431">articleuniqueid=[[Sample KB Article.articleUId]]</span></span> <br /><span data-ttu-id="a2ae8-432">articletitle=[[Sample KB Article.question]]</span><span class="sxs-lookup"><span data-stu-id="a2ae8-432">articletitle=[[Sample KB Article.question]]</span></span> <br /><span data-ttu-id="a2ae8-433">articleprivateurl=[[Sample KB Article.serviceDeskUri]]</span><span class="sxs-lookup"><span data-stu-id="a2ae8-433">articleprivateurl=[[Sample KB Article.serviceDeskUri]]</span></span> <br /><span data-ttu-id="a2ae8-434">articlepublicurl=[[Sample KB Article.publicUrl]+]</span><span class="sxs-lookup"><span data-stu-id="a2ae8-434">articlepublicurl=[[Sample KB Article.publicUrl]+]</span></span>|  

    <span data-ttu-id="a2ae8-435">![New action call to associate KB article to case](../unified-service-desk/media/usd-actioncalltoassociatearticle.png "New action call to associate KB article to case")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-435">![New action call to associate KB article to case](../unified-service-desk/media/usd-actioncalltoassociatearticle.png "New action call to associate KB article to case")</span></span>  

22. <span data-ttu-id="a2ae8-436">Click **Save and Close**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-436">Click **Save and Close**.</span></span> <span data-ttu-id="a2ae8-437">Cuộc gọi hành động mới được thêm vào nút **Liên kết Bài viết**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-437">The new action call gets added to the **Link Article** button.</span></span>  

23. <span data-ttu-id="a2ae8-438">Click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner of the page.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-438">Click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner of the page.</span></span>  

24. <span data-ttu-id="a2ae8-439">Đóng trang nút thanh công cụ **Liên kết Bài viết** và trả lại trang **Mẫu: Thanh công cụ KB**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-439">Close the **Link Article** toolbar button page, and return to the **Sample: KB Toolbar** page.</span></span>  

25. <span data-ttu-id="a2ae8-440">Bây giờ chúng tôi sẽ liên kết thanh công cụ **Mẫu: Thanh công cụ KB** với kiểm soát tổ chức (**Bài viết KB Mẫu**) nơi bạn muốn hiển thị.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-440">We will now associate the **Sample: KB Toolbar** tool bar to the hosted control (**Sample KB Article**) where we want it to be displayed.</span></span>  

26. <span data-ttu-id="a2ae8-441">Trên thanh điều hướng, bấm vào mũi tên xuống bên cạnh **Mẫu: Thanh công cụ KB** rồi bấm vào **Kiểm soát Tổ chức**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-441">On the navigation bar, click the down arrow next to **Sample: KB Toolbar**, and then click **Hosted Controls**.</span></span>  

    <span data-ttu-id="a2ae8-442">![Add tool bar to a hosted control](../unified-service-desk/media/usd-addtoolbartohostedcontrol.png "Add tool bar to a hosted control")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-442">![Add tool bar to a hosted control](../unified-service-desk/media/usd-addtoolbartohostedcontrol.png "Add tool bar to a hosted control")</span></span>  

27. <span data-ttu-id="a2ae8-443">Bấm vào **Thêm Kiểm soát Tổ chức Hiện có**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-443">Click **Add Existing Hosted Control**.</span></span>  

28. <span data-ttu-id="a2ae8-444">Trong hộp tìm kiếm, nhập `Sample KB Article` và nhấn ENTER hoặc bấm vào nút tìm kiếm để thêm kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-444">In the search box, type `Sample KB Article`, and press ENTER or click the search button to add the hosted control.</span></span>  

29. <span data-ttu-id="a2ae8-445">Click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner of the page.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-445">Click the **Save**![Auto save button](../unified-service-desk/media/crm-itpro-cust-autosaveicon.png "Auto save button") button in the lower-right corner of the page.</span></span>  

<a name="Step7"></a>   
## <a name="step-7-test-the-application"></a><span data-ttu-id="a2ae8-446">Bước 7: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="a2ae8-446">Step 7: Test the application</span></span>  
 <span data-ttu-id="a2ae8-447">Để kiểm tra ứng dụng:</span><span class="sxs-lookup"><span data-stu-id="a2ae8-447">To test the application:</span></span>  

1. <span data-ttu-id="a2ae8-448">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] entities as described earlier.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-448">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] entities as described earlier.</span></span>  

2. <span data-ttu-id="a2ae8-449">Trong ứng dụng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], bấm vào **Công việc Của tôi** trên thanh công cụ để hiển thị danh sách các trường hợp được chỉ định cho bạn.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-449">In the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application, click **My Work** in the toolbar to display a list of cases assigned to you.</span></span>  

3. <span data-ttu-id="a2ae8-450">In the **My Work** tab, click a case title to open it in a session.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-450">In the **My Work** tab, click a case title to open it in a session.</span></span> <span data-ttu-id="a2ae8-451">Bảng điều khiển Tìm kiếm KB Mẫu được tự động hiển thị ở phía bên phải, với tiêu đề trường hợp hiện tại được điền trước vào hộp tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-451">The Sample KB Search panel is automatically displayed on the right side, with the current case title pre-populated in the search box.</span></span>  

   <span data-ttu-id="a2ae8-452">![KB Search pane in your agent desktop](../unified-service-desk/media/usd-kmcontrolinaction.png "KB Search pane in your agent desktop")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-452">![KB Search pane in your agent desktop](../unified-service-desk/media/usd-kmcontrolinaction.png "KB Search pane in your agent desktop")</span></span>  

4. <span data-ttu-id="a2ae8-453">Nhấp vào một tiêu đề trường hợp trong kết quả tìm kiếm để hiển thị các bài viết trong bảng điều khiển chính.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-453">Click a case title in the search results to display the article in the main panel.</span></span> <span data-ttu-id="a2ae8-454">Thông báo hai nút trong tab bài viết: **Sao chép Liên kết** và **Liên kết Bài viết**.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-454">Notice the two buttons in the article tab: **Copy Link** and **Link Article**.</span></span>  

   <span data-ttu-id="a2ae8-455">![Article displayed in the main panel](../unified-service-desk/media/usd-kbarticleinmainpanel.png "Article displayed in the main panel")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-455">![Article displayed in the main panel](../unified-service-desk/media/usd-kbarticleinmainpanel.png "Article displayed in the main panel")</span></span>  

   -   <span data-ttu-id="a2ae8-456">Bấm vào **Sao chép Liên kết** để sao chép URL của bài viết.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-456">Click **Copy Link** to copy the URL of the article.</span></span> <span data-ttu-id="a2ae8-457">You can paste the URL in the browser to go directly to the article or can copy it in an email and send it to your customer.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-457">You can paste the URL in the browser to go directly to the article or can copy it in an email and send it to your customer.</span></span>  

   -   <span data-ttu-id="a2ae8-458">Bấm **Liên kết Bài viết** để liên kết bài viết với trường hợp hiện tại.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-458">Click **Link Article** to associate the article with the current case.</span></span> <span data-ttu-id="a2ae8-459">Thông báo được hiển thị ở đầu bảng điều khiển Tìm kiếm KB Mẫu để thông báo cho bạn rằng bài viết đã được liên kết.</span><span class="sxs-lookup"><span data-stu-id="a2ae8-459">A message is displayed at the top of the Sample KB Search panel to inform you that the article has been linked.</span></span>  

   <span data-ttu-id="a2ae8-460">![Link article to a case](../unified-service-desk/media/usd-linkarticletocase.png "Link article to a case")</span><span class="sxs-lookup"><span data-stu-id="a2ae8-460">![Link article to a case](../unified-service-desk/media/usd-linkarticletocase.png "Link article to a case")</span></span>  

<a name="Conclusion"></a>   
## <a name="conclusion"></a><span data-ttu-id="a2ae8-461">Kết luận</span><span class="sxs-lookup"><span data-stu-id="a2ae8-461">Conclusion</span></span>  
 <span data-ttu-id="a2ae8-462">In this walkthrough, you learned how to use the KM Control hosted control to use Dynamics 365 for Customer Engagement apps knowledge from within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="a2ae8-462">In this walkthrough, you learned how to use the KM Control hosted control to use Dynamics 365 for Customer Engagement apps knowledge from within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  

### <a name="see-also"></a><span data-ttu-id="a2ae8-463">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a2ae8-463">See also</span></span>  
 [<span data-ttu-id="a2ae8-464">Use Dynamics 365 for Customer Engagement apps knowledge for effective customer engagement</span><span class="sxs-lookup"><span data-stu-id="a2ae8-464">Use Dynamics 365 for Customer Engagement apps knowledge for effective customer engagement</span></span>](../unified-service-desk/use-dynamics-365-knowledge-effective-customer-engagement.md)   

 [<span data-ttu-id="a2ae8-465">Configure Dynamics 365 for Customer Engagement apps knowledge in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="a2ae8-465">Configure Dynamics 365 for Customer Engagement apps knowledge in Unified Service Desk</span></span>](../unified-service-desk/configure-unified-service-desk-use-dynamics-365-knowledge.md)   

 [<span data-ttu-id="a2ae8-466">Kiểm soát KM (Kiểm soát Tổ chức)</span><span class="sxs-lookup"><span data-stu-id="a2ae8-466">KM Control (Hosted Control)</span></span>](../unified-service-desk/km-control-hosted-control.md)   

 [<span data-ttu-id="a2ae8-467">Unified Interface KM Control (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="a2ae8-467">Unified Interface KM Control (Hosted Control)</span></span>](../unified-service-desk/unified-interface-km-control-hosted-control.md)

 [<span data-ttu-id="a2ae8-468">Unified Service Desk Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="a2ae8-468">Unified Service Desk Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
