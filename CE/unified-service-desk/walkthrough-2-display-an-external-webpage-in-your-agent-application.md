---
title: 'Walkthrough 2: Display an external webpage in your agent application | MicrosoftDocs'
description: Demonstrates how to display an external web page in Unified Service Desk.
ms.custom:
- dyn365-USD
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 516ceb5c-755a-49ab-89f5-fea3559b48cd
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 2d6b3ed05dee3bda75360e2b9924211e85699498
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387001"
---
# <a name="walkthrough-2-display-an-external-webpage-in-your-agent-application"></a><span data-ttu-id="94b3e-103">Walkthrough 2: Display an external webpage in your agent application</span><span class="sxs-lookup"><span data-stu-id="94b3e-103">Walkthrough 2: Display an external webpage in your agent application</span></span>
<span data-ttu-id="94b3e-104">This walkthrough demonstrates how to display a webpage or external URL in your agent application.</span><span class="sxs-lookup"><span data-stu-id="94b3e-104">This walkthrough demonstrates how to display a webpage or external URL in your agent application.</span></span> <span data-ttu-id="94b3e-105">In this walkthrough, you’ll learn how to display the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] Guide, which is available online at http://go.microsoft.com/fwlink/?LinkID=856273, in the client application.</span><span class="sxs-lookup"><span data-stu-id="94b3e-105">In this walkthrough, you’ll learn how to display the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] Guide, which is available online at http://go.microsoft.com/fwlink/?LinkID=856273, in the client application.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="94b3e-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="94b3e-106">Prerequisites</span></span>  

- <span data-ttu-id="94b3e-107">You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="94b3e-107">You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span> <span data-ttu-id="94b3e-108">The configurations that you completed in the first walkthrough are required in this walkthrough.</span><span class="sxs-lookup"><span data-stu-id="94b3e-108">The configurations that you completed in the first walkthrough are required in this walkthrough.</span></span>  

- <span data-ttu-id="94b3e-109">Cách này giả định rằng bạn sẽ sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng ở cuối cách 1 để đăng nhập vào ứng dụng tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="94b3e-109">This walkthrough assumes that you will be using the same user credential that you used at the end of Walkthrough 1 to sign in to the agent application.</span></span> <span data-ttu-id="94b3e-110">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-110">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="94b3e-111">[Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)</span><span class="sxs-lookup"><span data-stu-id="94b3e-111">[Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)</span></span>  

- <span data-ttu-id="94b3e-112">You must be familiar with the following concepts in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="94b3e-112">You must be familiar with the following concepts in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  

  - <span data-ttu-id="94b3e-113">These two types of hosted controls: Standard Web Application and Toolbar Container.</span><span class="sxs-lookup"><span data-stu-id="94b3e-113">These two types of hosted controls: Standard Web Application and Toolbar Container.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="94b3e-114">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span><span class="sxs-lookup"><span data-stu-id="94b3e-114">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span></span>  

  - <span data-ttu-id="94b3e-115">How to configure [Action calls](../unified-service-desk/action-calls.md)</span><span class="sxs-lookup"><span data-stu-id="94b3e-115">How to configure [Action calls](../unified-service-desk/action-calls.md)</span></span>  

  - <span data-ttu-id="94b3e-116">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span><span class="sxs-lookup"><span data-stu-id="94b3e-116">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="94b3e-117">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="94b3e-117">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span></span>  

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a><span data-ttu-id="94b3e-118">In This Walkthrough</span><span class="sxs-lookup"><span data-stu-id="94b3e-118">In This Walkthrough</span></span>  
 [<span data-ttu-id="94b3e-119">Bước 1: Tạo kiểm soát tổ chức để hiển thị trang web</span><span class="sxs-lookup"><span data-stu-id="94b3e-119">Step 1: Create a hosted control to display the webpage</span></span>](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md#Step1)  

 [<span data-ttu-id="94b3e-120">Bước 2: Tạo loại bộ chứa công cụ của kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="94b3e-120">Step 2: Create a toolbar container type of hosted control</span></span>](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md#Step2)  

 [<span data-ttu-id="94b3e-121">Bước 3: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="94b3e-121">Step 3: Add a toolbar and attach it to the toolbar container</span></span>](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md#Step3)  

 [<span data-ttu-id="94b3e-122">Bước 4: Thêm nút thanh công cụ và các cuộc gọi hành động để hiển thị trang web</span><span class="sxs-lookup"><span data-stu-id="94b3e-122">Step 4: Add a toolbar button and action calls to display the webpage</span></span>](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md#Step4)  

 [<span data-ttu-id="94b3e-123">Bước 5: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="94b3e-123">Step 5: Add the controls to the configuration</span></span>](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md#Step5)  

 [<span data-ttu-id="94b3e-124">Bước 6: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="94b3e-124">Step 6: Test the application</span></span>](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md#Step6)  

 [<span data-ttu-id="94b3e-125">Kết luận</span><span class="sxs-lookup"><span data-stu-id="94b3e-125">Conclusion</span></span>](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md#Conclusion)  

<a name="Step1"></a>   
## <a name="step-1-create-a-hosted-control-to-display-the-webpage"></a><span data-ttu-id="94b3e-126">Step 1: Create a hosted control to display the webpage</span><span class="sxs-lookup"><span data-stu-id="94b3e-126">Step 1: Create a hosted control to display the webpage</span></span>  
 <span data-ttu-id="94b3e-127">In this step, you’ll create a hosted control of Standard Web Application type to display the webpage.</span><span class="sxs-lookup"><span data-stu-id="94b3e-127">In this step, you’ll create a hosted control of Standard Web Application type to display the webpage.</span></span>  

1. <span data-ttu-id="94b3e-128">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="94b3e-128">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="94b3e-129">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-129">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="94b3e-130">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-130">Click **New**.</span></span>  

5. <span data-ttu-id="94b3e-131">On the **New Hosted Control** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="94b3e-131">On the **New Hosted Control** page, specify the following values:</span></span>  

   |<span data-ttu-id="94b3e-132">Trường</span><span class="sxs-lookup"><span data-stu-id="94b3e-132">Field</span></span>|<span data-ttu-id="94b3e-133">Giá trị</span><span class="sxs-lookup"><span data-stu-id="94b3e-133">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="94b3e-134">Tên</span><span class="sxs-lookup"><span data-stu-id="94b3e-134">Name</span></span>|<span data-ttu-id="94b3e-135">Contoso trợ giúp</span><span class="sxs-lookup"><span data-stu-id="94b3e-135">Contoso Help</span></span>|  
   |<span data-ttu-id="94b3e-136">Tên hiển thị</span><span class="sxs-lookup"><span data-stu-id="94b3e-136">Display Name</span></span>|<span data-ttu-id="94b3e-137">Contoso trợ giúp</span><span class="sxs-lookup"><span data-stu-id="94b3e-137">Contoso Help</span></span>|  
   |<span data-ttu-id="94b3e-138">Loại Thành phần USD</span><span class="sxs-lookup"><span data-stu-id="94b3e-138">USD Component Type</span></span>|<span data-ttu-id="94b3e-139">Ứng dụng web tiêu chuẩn</span><span class="sxs-lookup"><span data-stu-id="94b3e-139">Standard Web Application</span></span>|  
   |<span data-ttu-id="94b3e-140">Cho phép nhiều trang</span><span class="sxs-lookup"><span data-stu-id="94b3e-140">Allow Multiple Pages</span></span>|<span data-ttu-id="94b3e-141">No</span><span class="sxs-lookup"><span data-stu-id="94b3e-141">No</span></span>|  
   |<span data-ttu-id="94b3e-142">Loại tổ chức</span><span class="sxs-lookup"><span data-stu-id="94b3e-142">Hosting Type</span></span>|<span data-ttu-id="94b3e-143">WPF nội bộ</span><span class="sxs-lookup"><span data-stu-id="94b3e-143">Internal WPF</span></span>|  
   |<span data-ttu-id="94b3e-144">Application is Global</span><span class="sxs-lookup"><span data-stu-id="94b3e-144">Application is Global</span></span>|<span data-ttu-id="94b3e-145">Đã kiểm tra</span><span class="sxs-lookup"><span data-stu-id="94b3e-145">Checked</span></span>|  
   |<span data-ttu-id="94b3e-146">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="94b3e-146">Display Group</span></span>|<span data-ttu-id="94b3e-147">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="94b3e-147">MainPanel</span></span>|  

   <span data-ttu-id="94b3e-148">![Standard Web Application hosted control](../unified-service-desk/media/crm-itpro-usd-wt02-01.png "Standard Web Application hosted control")</span><span class="sxs-lookup"><span data-stu-id="94b3e-148">![Standard Web Application hosted control](../unified-service-desk/media/crm-itpro-usd-wt02-01.png "Standard Web Application hosted control")</span></span>  

6. <span data-ttu-id="94b3e-149">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-149">Click **Save**.</span></span>  

<a name="Step2"></a>   
## <a name="step-2-create-a-toolbar-container-type-of-hosted-control"></a><span data-ttu-id="94b3e-150">Step 2: Create a toolbar container type of hosted control</span><span class="sxs-lookup"><span data-stu-id="94b3e-150">Step 2: Create a toolbar container type of hosted control</span></span>  
 <span data-ttu-id="94b3e-151">Kiểm soát tổ chức bộ chứa thanh công cụ được sử dụng để giữ và hiển thị thanh công cụ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="94b3e-151">Toolbar Container hosted controls are used to hold and display the toolbars in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="94b3e-152">In this section, you’ll create a **Toolbar Container** type of hosted control that appears in the toolbar region of the client application.</span><span class="sxs-lookup"><span data-stu-id="94b3e-152">In this section, you’ll create a **Toolbar Container** type of hosted control that appears in the toolbar region of the client application.</span></span>  

1. <span data-ttu-id="94b3e-153">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="94b3e-153">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="94b3e-154">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-154">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="94b3e-155">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-155">Click **New**.</span></span>  

5. <span data-ttu-id="94b3e-156">On the **New Hosted Control** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="94b3e-156">On the **New Hosted Control** page, specify the following values:</span></span>  

   |<span data-ttu-id="94b3e-157">Trường</span><span class="sxs-lookup"><span data-stu-id="94b3e-157">Field</span></span>|<span data-ttu-id="94b3e-158">Giá trị</span><span class="sxs-lookup"><span data-stu-id="94b3e-158">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="94b3e-159">Tên</span><span class="sxs-lookup"><span data-stu-id="94b3e-159">Name</span></span>|<span data-ttu-id="94b3e-160">Contoso về Bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="94b3e-160">Contoso About Toolbar Container</span></span>|  
   |<span data-ttu-id="94b3e-161">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="94b3e-161">USD Component Type</span></span>|<span data-ttu-id="94b3e-162">Bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="94b3e-162">Toolbar Container</span></span>|  
   |<span data-ttu-id="94b3e-163">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="94b3e-163">Display Group</span></span>|<span data-ttu-id="94b3e-164">AboutPanel</span><span class="sxs-lookup"><span data-stu-id="94b3e-164">AboutPanel</span></span>|  

   <span data-ttu-id="94b3e-165">![Toolbar Container hosted control](../unified-service-desk/media/crm-itpro-usd-wt02-02.png "Toolbar Container hosted control")</span><span class="sxs-lookup"><span data-stu-id="94b3e-165">![Toolbar Container hosted control](../unified-service-desk/media/crm-itpro-usd-wt02-02.png "Toolbar Container hosted control")</span></span>  

6. <span data-ttu-id="94b3e-166">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-166">Click **Save**.</span></span>  

<a name="Step3"></a>   
## <a name="step-3-add-a-toolbar-and-attach-it-to-the-toolbar-container"></a><span data-ttu-id="94b3e-167">Step 3: Add a toolbar and attach it to the toolbar container</span><span class="sxs-lookup"><span data-stu-id="94b3e-167">Step 3: Add a toolbar and attach it to the toolbar container</span></span>  
 <span data-ttu-id="94b3e-168">In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 2.</span><span class="sxs-lookup"><span data-stu-id="94b3e-168">In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 2.</span></span> <span data-ttu-id="94b3e-169">This is done to display the toolbar in your agent application.</span><span class="sxs-lookup"><span data-stu-id="94b3e-169">This is done to display the toolbar in your agent application.</span></span>  

1. <span data-ttu-id="94b3e-170">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="94b3e-170">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="94b3e-171">Bấm vào **Thanh công cụ**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-171">Click **Toolbars**.</span></span>  

4. <span data-ttu-id="94b3e-172">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-172">Click **New**.</span></span>  

5. <span data-ttu-id="94b3e-173">On the **New Toolbar** page, type **Contoso About Toolbar** in the **Name** box, and then click **Save**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-173">On the **New Toolbar** page, type **Contoso About Toolbar** in the **Name** box, and then click **Save**.</span></span>  

6. <span data-ttu-id="94b3e-174">Attach the toolbar to the toolbar container hosted control created in step 2.</span><span class="sxs-lookup"><span data-stu-id="94b3e-174">Attach the toolbar to the toolbar container hosted control created in step 2.</span></span> <span data-ttu-id="94b3e-175">On the nav bar, click the down arrow next to **Contoso About Toolbar**, and click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-175">On the nav bar, click the down arrow next to **Contoso About Toolbar**, and click **Hosted Controls**.</span></span>  

7. <span data-ttu-id="94b3e-176">Trên trang tiếp theo, bấm vào **Thêm kiểm soát tổ chức hiện có**, nhập `Contoso About Toolbar Container` trong thanh tìm kiếm và sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="94b3e-176">On the next page, click **Add Existing Hosted Control**, type `Contoso About Toolbar Container` in the search bar, and then press ENTER or click the search icon.</span></span>  

8. <span data-ttu-id="94b3e-177">Từ kết quả tìm kiếm, chọn **Bộ chứa thanh công cụ về Contoso**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-177">From the search results, select **Contoso About Toolbar Container**.</span></span>  

9. <span data-ttu-id="94b3e-178">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-178">Click **Save**.</span></span>  

<a name="Step4"></a>   
## <a name="step-4-add-a-toolbar-button-and-action-calls-to-display-the-webpage"></a><span data-ttu-id="94b3e-179">Bước 4: Thêm nút thanh công cụ và các cuộc gọi hành động để hiển thị trang web</span><span class="sxs-lookup"><span data-stu-id="94b3e-179">Step 4: Add a toolbar button and action calls to display the webpage</span></span>  
 <span data-ttu-id="94b3e-180">Trong bước này, thêm một nút trên thanh công cụ và đính kèm một cuộc gọi hành động cho nút để khi nút được nhấn vào, trang web đã chỉ định được hiển thị trong kiểm soát tổ chức mà bạn đã tạo ở bước 1.</span><span class="sxs-lookup"><span data-stu-id="94b3e-180">In this step, add a button on the toolbar and attach an action call to the button so that when the button is clicked, the specified webpage is displayed in the hosted control that you created in step 1.</span></span>  

1. <span data-ttu-id="94b3e-181">After you save the toolbar in step 3, the **Buttons** area becomes available.</span><span class="sxs-lookup"><span data-stu-id="94b3e-181">After you save the toolbar in step 3, the **Buttons** area becomes available.</span></span> <span data-ttu-id="94b3e-182">In the **Buttons** area, click **+** on the right corner to add a button.</span><span class="sxs-lookup"><span data-stu-id="94b3e-182">In the **Buttons** area, click **+** on the right corner to add a button.</span></span>  

2. <span data-ttu-id="94b3e-183">On the **New Toolbar Button** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="94b3e-183">On the **New Toolbar Button** page, specify the following values.</span></span>  

   |<span data-ttu-id="94b3e-184">Trường</span><span class="sxs-lookup"><span data-stu-id="94b3e-184">Field</span></span>|<span data-ttu-id="94b3e-185">Value</span><span class="sxs-lookup"><span data-stu-id="94b3e-185">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="94b3e-186">Tên</span><span class="sxs-lookup"><span data-stu-id="94b3e-186">Name</span></span>|<span data-ttu-id="94b3e-187">Contoso Show Help</span><span class="sxs-lookup"><span data-stu-id="94b3e-187">Contoso Show Help</span></span>|  
   |<span data-ttu-id="94b3e-188">Văn bản nút</span><span class="sxs-lookup"><span data-stu-id="94b3e-188">Button Text</span></span>|<span data-ttu-id="94b3e-189">Hiển thị trợ giúp</span><span class="sxs-lookup"><span data-stu-id="94b3e-189">Show Help</span></span>|  

   <span data-ttu-id="94b3e-190">![Create a new toolbar button](../unified-service-desk/media/crm-itpro-usd-wt02-03.png "Create a new toolbar button")</span><span class="sxs-lookup"><span data-stu-id="94b3e-190">![Create a new toolbar button](../unified-service-desk/media/crm-itpro-usd-wt02-03.png "Create a new toolbar button")</span></span>  

3. <span data-ttu-id="94b3e-191">Click **Save** to save the record, and enable the **Actions** area.</span><span class="sxs-lookup"><span data-stu-id="94b3e-191">Click **Save** to save the record, and enable the **Actions** area.</span></span>  

4. <span data-ttu-id="94b3e-192">Add two action calls to specify the URL of the webpage to navigate to for the hosted control that you created in step 1.</span><span class="sxs-lookup"><span data-stu-id="94b3e-192">Add two action calls to specify the URL of the webpage to navigate to for the hosted control that you created in step 1.</span></span> <span data-ttu-id="94b3e-193">Additionally, create another action call to on the **Contoso Global Manager** hosted control to display the hosted control created in step 1 in the agent application.</span><span class="sxs-lookup"><span data-stu-id="94b3e-193">Additionally, create another action call to on the **Contoso Global Manager** hosted control to display the hosted control created in step 1 in the agent application.</span></span>  

    <span data-ttu-id="94b3e-194">In the **Actions** area, click **+** on the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="94b3e-194">In the **Actions** area, click **+** on the right corner to add an action call.</span></span>  

5. <span data-ttu-id="94b3e-195">In the search box in the **Actions** area, press ENTER or click the search icon.</span><span class="sxs-lookup"><span data-stu-id="94b3e-195">In the search box in the **Actions** area, press ENTER or click the search icon.</span></span>  

6. <span data-ttu-id="94b3e-196">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span><span class="sxs-lookup"><span data-stu-id="94b3e-196">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>  

   <span data-ttu-id="94b3e-197">![Choose New to create an action call](../unified-service-desk/media/crm-itpro-usd-wt02-04.png "Choose New to create an action call")</span><span class="sxs-lookup"><span data-stu-id="94b3e-197">![Choose New to create an action call](../unified-service-desk/media/crm-itpro-usd-wt02-04.png "Choose New to create an action call")</span></span>  

7. <span data-ttu-id="94b3e-198">On the **New Action Call** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="94b3e-198">On the **New Action Call** page, specify the following values:</span></span>  


   |     <span data-ttu-id="94b3e-199">Trường</span><span class="sxs-lookup"><span data-stu-id="94b3e-199">Field</span></span>      |                        <span data-ttu-id="94b3e-200">Giá trị</span><span class="sxs-lookup"><span data-stu-id="94b3e-200">Value</span></span>                        |
   |----------------|-----------------------------------------------------|
   |      <span data-ttu-id="94b3e-201">Tên</span><span class="sxs-lookup"><span data-stu-id="94b3e-201">Name</span></span>      |          <span data-ttu-id="94b3e-202">Cuộc gọi hành động Contoso: Hiển thị trợ giúp</span><span class="sxs-lookup"><span data-stu-id="94b3e-202">Contoso Action Call: Display Help</span></span>          |
   |     <span data-ttu-id="94b3e-203">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="94b3e-203">Order</span></span>      |                          <span data-ttu-id="94b3e-204">1</span><span class="sxs-lookup"><span data-stu-id="94b3e-204">1</span></span>                          |
   | <span data-ttu-id="94b3e-205">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="94b3e-205">Hosted Control</span></span> |                    <span data-ttu-id="94b3e-206">Contoso trợ giúp</span><span class="sxs-lookup"><span data-stu-id="94b3e-206">Contoso Help</span></span>                     |
   |     <span data-ttu-id="94b3e-207">Hành động</span><span class="sxs-lookup"><span data-stu-id="94b3e-207">Action</span></span>     |                      <span data-ttu-id="94b3e-208">Navigate</span><span class="sxs-lookup"><span data-stu-id="94b3e-208">Navigate</span></span>                       |
   |      <span data-ttu-id="94b3e-209">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="94b3e-209">Data</span></span>      | <span data-ttu-id="94b3e-210">url=<http://go.microsoft.com/fwlink/?LinkID=856273></span><span class="sxs-lookup"><span data-stu-id="94b3e-210">url=<http://go.microsoft.com/fwlink/?LinkID=856273></span></span> |

   <span data-ttu-id="94b3e-211">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-05.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="94b3e-211">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-05.png "Create an action call in Unified Service Desk")</span></span>  

8. <span data-ttu-id="94b3e-212">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-212">Click **Save**.</span></span> <span data-ttu-id="94b3e-213">The new action call is added to the **Contoso Show Help** button.</span><span class="sxs-lookup"><span data-stu-id="94b3e-213">The new action call is added to the **Contoso Show Help** button.</span></span>  

9. <span data-ttu-id="94b3e-214">Add another action call to the button to set the focus on the hosted control that displays the webpage in the client application.</span><span class="sxs-lookup"><span data-stu-id="94b3e-214">Add another action call to the button to set the focus on the hosted control that displays the webpage in the client application.</span></span> <span data-ttu-id="94b3e-215">In the **Actions** area, click **+** in the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="94b3e-215">In the **Actions** area, click **+** in the right corner to add an action call.</span></span>  

10. <span data-ttu-id="94b3e-216">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span><span class="sxs-lookup"><span data-stu-id="94b3e-216">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>  

11. <span data-ttu-id="94b3e-217">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="94b3e-217">On the **New Action Call** page, specify the following values.</span></span>  

    |<span data-ttu-id="94b3e-218">Trường</span><span class="sxs-lookup"><span data-stu-id="94b3e-218">Field</span></span>|<span data-ttu-id="94b3e-219">Giá trị</span><span class="sxs-lookup"><span data-stu-id="94b3e-219">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="94b3e-220">Tên</span><span class="sxs-lookup"><span data-stu-id="94b3e-220">Name</span></span>|<span data-ttu-id="94b3e-221">Cuộc gọi hành động Contoso: Hiển thị kiểm soát tổ chức trợ giúp</span><span class="sxs-lookup"><span data-stu-id="94b3e-221">Contoso Action Call: Display Help Hosted Control</span></span>|  
    |<span data-ttu-id="94b3e-222">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="94b3e-222">Order</span></span>|<span data-ttu-id="94b3e-223">2</span><span class="sxs-lookup"><span data-stu-id="94b3e-223">2</span></span>|  
    |<span data-ttu-id="94b3e-224">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="94b3e-224">Hosted Control</span></span>|<span data-ttu-id="94b3e-225">Contoso Global Manager</span><span class="sxs-lookup"><span data-stu-id="94b3e-225">Contoso Global Manager</span></span>|  
    |<span data-ttu-id="94b3e-226">Hành động</span><span class="sxs-lookup"><span data-stu-id="94b3e-226">Action</span></span>|<span data-ttu-id="94b3e-227">Hiển thị tab</span><span class="sxs-lookup"><span data-stu-id="94b3e-227">ShowTab</span></span>|  
    |<span data-ttu-id="94b3e-228">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="94b3e-228">Data</span></span>|<span data-ttu-id="94b3e-229">Contoso trợ giúp</span><span class="sxs-lookup"><span data-stu-id="94b3e-229">Contoso Help</span></span>|  

    <span data-ttu-id="94b3e-230">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-06.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="94b3e-230">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-06.png "Create an action call in Unified Service Desk")</span></span>  

12. <span data-ttu-id="94b3e-231">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-231">Click **Save**.</span></span> <span data-ttu-id="94b3e-232">The new action call gets added to the **Contoso Show Help** button.</span><span class="sxs-lookup"><span data-stu-id="94b3e-232">The new action call gets added to the **Contoso Show Help** button.</span></span> <span data-ttu-id="94b3e-233">You can see both action calls added to the toolbar button.</span><span class="sxs-lookup"><span data-stu-id="94b3e-233">You can see both action calls added to the toolbar button.</span></span>  

    <span data-ttu-id="94b3e-234">![Action calls added to the toolbar button](../unified-service-desk/media/crm-itpro-usd-wt02-07.png "Action calls added to the toolbar button")</span><span class="sxs-lookup"><span data-stu-id="94b3e-234">![Action calls added to the toolbar button](../unified-service-desk/media/crm-itpro-usd-wt02-07.png "Action calls added to the toolbar button")</span></span>  

<a name="Step5"></a>   
## <a name="step-5-add-the-controls-to-the-configuration"></a><span data-ttu-id="94b3e-235">Step 5: Add the controls to the configuration</span><span class="sxs-lookup"><span data-stu-id="94b3e-235">Step 5: Add the controls to the configuration</span></span>  
 <span data-ttu-id="94b3e-236">In this step, add the action calls, hosted controls, and toolbar that you created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span><span class="sxs-lookup"><span data-stu-id="94b3e-236">In this step, add the action calls, hosted controls, and toolbar that you created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span></span> <span data-ttu-id="94b3e-237">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="94b3e-237">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span>  

 <span data-ttu-id="94b3e-238">Add the following to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-238">Add the following to **Contoso Configuration**.</span></span>  

|<span data-ttu-id="94b3e-239">Tên kiểm soát</span><span class="sxs-lookup"><span data-stu-id="94b3e-239">Control name</span></span>|<span data-ttu-id="94b3e-240">Loại kiểm soát</span><span class="sxs-lookup"><span data-stu-id="94b3e-240">Control type</span></span>|  
|------------------|------------------|  
|<span data-ttu-id="94b3e-241">Cuộc gọi hành động Contoso: Hiển thị trợ giúp</span><span class="sxs-lookup"><span data-stu-id="94b3e-241">Contoso Action Call: Display Help</span></span>|<span data-ttu-id="94b3e-242">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="94b3e-242">Action Call</span></span>|  
|<span data-ttu-id="94b3e-243">Cuộc gọi hành động Contoso: Hiển thị kiểm soát tổ chức trợ giúp</span><span class="sxs-lookup"><span data-stu-id="94b3e-243">Contoso Action Call: Display Help Hosted Control</span></span>|<span data-ttu-id="94b3e-244">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="94b3e-244">Action Call</span></span>|  
|<span data-ttu-id="94b3e-245">Contoso trợ giúp</span><span class="sxs-lookup"><span data-stu-id="94b3e-245">Contoso Help</span></span>|<span data-ttu-id="94b3e-246">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="94b3e-246">Hosted Control</span></span>|  
|<span data-ttu-id="94b3e-247">Contoso về Bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="94b3e-247">Contoso About Toolbar Container</span></span>|<span data-ttu-id="94b3e-248">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="94b3e-248">Hosted Control</span></span>|  
|<span data-ttu-id="94b3e-249">Contoso About Toolbar</span><span class="sxs-lookup"><span data-stu-id="94b3e-249">Contoso About Toolbar</span></span>|<span data-ttu-id="94b3e-250">Thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="94b3e-250">Toolbar</span></span>|  

 <span data-ttu-id="94b3e-251">To add a control to the configuration:</span><span class="sxs-lookup"><span data-stu-id="94b3e-251">To add a control to the configuration:</span></span>  

1. <span data-ttu-id="94b3e-252">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="94b3e-252">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. <span data-ttu-id="94b3e-253">Trên thanh điều hướng, nhấp vào **Microsoft Dynamics 365 for Customer Engagement**, và sau đó chọn **Cài đặt**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-253">On the nav bar, click **Microsoft Dynamics 365 for Customer Engagement**, and then select **Settings**.</span></span>  

3. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

4. <span data-ttu-id="94b3e-254">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-254">Click **Configuration**.</span></span>  

5. <span data-ttu-id="94b3e-255">Bấm vào **Cấu hình Contoso** để mở định nghĩa.</span><span class="sxs-lookup"><span data-stu-id="94b3e-255">Click **Contoso Configuration** to open the definition.</span></span>  

6. <span data-ttu-id="94b3e-256">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-256">On the nav bar, click the down arrow next to **Contoso Configuration**, and select **Action Calls**.</span></span>  

7. <span data-ttu-id="94b3e-257">Trên trang tiếp theo, bấm vào **Thêm Cuộc gọi Hành động Hiện có**, nhập “`Contoso Action Call`” vào thanh tìm kiếm, sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="94b3e-257">On the next page, click **Add Existing Action Call**, type “`Contoso Action Call`” in the search bar, and then press ENTER or click the search icon.</span></span>  

8. <span data-ttu-id="94b3e-258">Cả cuộc gọi hành động được hiển thị trong kết quả tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="94b3e-258">Both action calls are displayed in the search results.</span></span> <span data-ttu-id="94b3e-259">Thêm cả hai người trong số chúng.</span><span class="sxs-lookup"><span data-stu-id="94b3e-259">Add both of them.</span></span>  

9. <span data-ttu-id="94b3e-260">Tương tự, thêm cả hai kiểm soát tổ chức và thanh công cụ bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Kiểm soát tổ chức** và **thanh công cụ** lần lượt.</span><span class="sxs-lookup"><span data-stu-id="94b3e-260">Similarly, add both of the hosted controls and the toolbar by clicking the down arrow next to **Contoso Configuration**, and clicking **Hosted Controls** and **Toolbars** respectively.</span></span>  

10. <span data-ttu-id="94b3e-261">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="94b3e-261">Click **Save**.</span></span>  

<a name="Step6"></a>   
## <a name="step-6-test-the-application"></a><span data-ttu-id="94b3e-262">Step 6: Test the application</span><span class="sxs-lookup"><span data-stu-id="94b3e-262">Step 6: Test the application</span></span>  
 <span data-ttu-id="94b3e-263">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="94b3e-263">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span> <span data-ttu-id="94b3e-264">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)</span><span class="sxs-lookup"><span data-stu-id="94b3e-264">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)</span></span>  

 <span data-ttu-id="94b3e-265">Your agent application will now have a **Show Help** button at the top-right corner:</span><span class="sxs-lookup"><span data-stu-id="94b3e-265">Your agent application will now have a **Show Help** button at the top-right corner:</span></span>  

 <span data-ttu-id="94b3e-266">![Show Help button in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-08.png "Show Help button in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="94b3e-266">![Show Help button in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-08.png "Show Help button in Unified Service Desk")</span></span>  

 <span data-ttu-id="94b3e-267">Clicking **Show Help** displays the specified web URL within the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application.</span><span class="sxs-lookup"><span data-stu-id="94b3e-267">Clicking **Show Help** displays the specified web URL within the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application.</span></span>  

 <span data-ttu-id="94b3e-268">![Help displayed in the client application](../unified-service-desk/media/crm-itpro-usd-wt02-09.png "Help displayed in the client application")</span><span class="sxs-lookup"><span data-stu-id="94b3e-268">![Help displayed in the client application](../unified-service-desk/media/crm-itpro-usd-wt02-09.png "Help displayed in the client application")</span></span>  

<a name="Conclusion"></a>   
## <a name="conclusion"></a><span data-ttu-id="94b3e-269">Kết luận</span><span class="sxs-lookup"><span data-stu-id="94b3e-269">Conclusion</span></span>  
 <span data-ttu-id="94b3e-270">In this walkthrough, you learned how to display a webpage in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.</span><span class="sxs-lookup"><span data-stu-id="94b3e-270">In this walkthrough, you learned how to display a webpage in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.</span></span> <span data-ttu-id="94b3e-271">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span><span class="sxs-lookup"><span data-stu-id="94b3e-271">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span></span>  

### <a name="see-also"></a><span data-ttu-id="94b3e-272">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="94b3e-272">See also</span></span>  
 <span data-ttu-id="94b3e-273">[Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="94b3e-273">[Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) </span></span>  
 <span data-ttu-id="94b3e-274">[Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="94b3e-274">[Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md) </span></span>  
 <span data-ttu-id="94b3e-275">[Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="94b3e-275">[Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md) </span></span>  
 <span data-ttu-id="94b3e-276">[Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md) </span><span class="sxs-lookup"><span data-stu-id="94b3e-276">[Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md) </span></span>  
 <span data-ttu-id="94b3e-277">[Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="94b3e-277">[Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md) </span></span>  
 <span data-ttu-id="94b3e-278">[Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="94b3e-278">[Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md) </span></span>  
 <span data-ttu-id="94b3e-279">[Walkthrough 8: Use Parature knowledge within your agent application](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="94b3e-279">[Walkthrough 8: Use Parature knowledge within your agent application](../unified-service-desk/walkthrough-8-use-dynamics-365-knowledge-base-within-agent-application.md) </span></span>  
 [<span data-ttu-id="94b3e-280">Unified Service Desk Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="94b3e-280">Unified Service Desk Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)  
