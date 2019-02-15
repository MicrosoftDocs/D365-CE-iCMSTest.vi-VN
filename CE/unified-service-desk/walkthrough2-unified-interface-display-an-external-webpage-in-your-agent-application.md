---
title: 'Walkthrough 2: Display an external webpage in your agent application | MicrosoftDocs'
description: Demonstrates how to display an external web page in Unified Service Desk.
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
ms.assetid: C616E47C-E7D4-4195-8F53-1139F7514BFA
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
ms.openlocfilehash: f372c1f929775229a7f33ae55818f163745c91bf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386864"
---
# <a name="walkthrough-2-display-an-external-webpage-in-your-agent-application"></a><span data-ttu-id="e2a16-103">Walkthrough 2: Display an external webpage in your agent application</span><span class="sxs-lookup"><span data-stu-id="e2a16-103">Walkthrough 2: Display an external webpage in your agent application</span></span>
<span data-ttu-id="e2a16-104">Cách này mô tả cách hiển thị trang web hoặc URL bên ngoài trong ứng dụng tổng đài viên của bạn.</span><span class="sxs-lookup"><span data-stu-id="e2a16-104">This walkthrough demonstrates how to display a webpage or external URL in your agent application.</span></span> <span data-ttu-id="e2a16-105">In this walkthrough, you’ll learn how to display the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] Guide, which is available online at http://go.microsoft.com/fwlink/?LinkID=856273, in the client application.</span><span class="sxs-lookup"><span data-stu-id="e2a16-105">In this walkthrough, you’ll learn how to display the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] Guide, which is available online at http://go.microsoft.com/fwlink/?LinkID=856273, in the client application.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e2a16-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="e2a16-106">Prerequisites</span></span>  

- <span data-ttu-id="e2a16-107">You must have completed [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="e2a16-107">You must have completed [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span></span> <span data-ttu-id="e2a16-108">Các cấu hình mà bạn hoàn thành trong cách đầu tiên được yêu cầu trong cách này.</span><span class="sxs-lookup"><span data-stu-id="e2a16-108">The configurations that you completed in the first walkthrough are required in this walkthrough.</span></span>  

- <span data-ttu-id="e2a16-109">Cách này giả định rằng bạn sẽ sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng ở cuối cách 1 để đăng nhập vào ứng dụng tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="e2a16-109">This walkthrough assumes that you will be using the same user credential that you used at the end of Walkthrough 1 to sign in to the agent application.</span></span> <span data-ttu-id="e2a16-110">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-110">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="e2a16-111">[Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)</span><span class="sxs-lookup"><span data-stu-id="e2a16-111">[Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)</span></span>  

- <span data-ttu-id="e2a16-112">Bạn phải làm quen với các khái niệm sau trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="e2a16-112">You must be familiar with the following concepts in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  

  - <span data-ttu-id="e2a16-113">Hai loại kiểm soát tổ chức: Ứng dụng web tiêu chuẩn và bộ chứa thanh công cụ.</span><span class="sxs-lookup"><span data-stu-id="e2a16-113">These two types of hosted controls: Standard Web Application and Toolbar Container.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="e2a16-114">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span><span class="sxs-lookup"><span data-stu-id="e2a16-114">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span></span>  

  - <span data-ttu-id="e2a16-115">How to configure [Action calls](../unified-service-desk/action-calls.md)</span><span class="sxs-lookup"><span data-stu-id="e2a16-115">How to configure [Action calls](../unified-service-desk/action-calls.md)</span></span>  

  - <span data-ttu-id="e2a16-116">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span><span class="sxs-lookup"><span data-stu-id="e2a16-116">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="e2a16-117">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="e2a16-117">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span></span>  

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a><span data-ttu-id="e2a16-118">In This Walkthrough</span><span class="sxs-lookup"><span data-stu-id="e2a16-118">In This Walkthrough</span></span>  
 [<span data-ttu-id="e2a16-119">Bước 1: Tạo kiểm soát tổ chức để hiển thị trang web</span><span class="sxs-lookup"><span data-stu-id="e2a16-119">Step 1: Create a hosted control to display the webpage</span></span>](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md#Step1)  

 [<span data-ttu-id="e2a16-120">Bước 2: Tạo loại bộ chứa công cụ của kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="e2a16-120">Step 2: Create a toolbar container type of hosted control</span></span>](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md#Step2)  

 [<span data-ttu-id="e2a16-121">Bước 3: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="e2a16-121">Step 3: Add a toolbar and attach it to the toolbar container</span></span>](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md#Step3)  

 [<span data-ttu-id="e2a16-122">Bước 4: Thêm nút thanh công cụ và các cuộc gọi hành động để hiển thị trang web</span><span class="sxs-lookup"><span data-stu-id="e2a16-122">Step 4: Add a toolbar button and action calls to display the webpage</span></span>](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md#Step4)  

 [<span data-ttu-id="e2a16-123">Bước 5: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="e2a16-123">Step 5: Add the controls to the configuration</span></span>](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md#Step5)  

 [<span data-ttu-id="e2a16-124">Bước 6: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="e2a16-124">Step 6: Test the application</span></span>](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md#Step6)  

 [<span data-ttu-id="e2a16-125">Kết luận</span><span class="sxs-lookup"><span data-stu-id="e2a16-125">Conclusion</span></span>](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md#Conclusion)  

<a name="Step1"></a>   
## <a name="step-1-create-a-hosted-control-to-display-the-webpage"></a><span data-ttu-id="e2a16-126">Bước 1: Tạo kiểm soát tổ chức để hiển thị trang web</span><span class="sxs-lookup"><span data-stu-id="e2a16-126">Step 1: Create a hosted control to display the webpage</span></span>  
 <span data-ttu-id="e2a16-127">Trong bước này, bạn sẽ tạo ra kiểm soát tổ chúc của loại ứng dụng web tiêu chuẩn để hiển thị trang web.</span><span class="sxs-lookup"><span data-stu-id="e2a16-127">In this step, you’ll create a hosted control of Standard Web Application type to display the webpage.</span></span>  

1. <span data-ttu-id="e2a16-128">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="e2a16-128">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="e2a16-129">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-129">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="e2a16-130">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-130">Click **New**.</span></span>  

5. <span data-ttu-id="e2a16-131">On the **New Hosted Control** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="e2a16-131">On the **New Hosted Control** page, specify the following values:</span></span>  

   |<span data-ttu-id="e2a16-132">Trường</span><span class="sxs-lookup"><span data-stu-id="e2a16-132">Field</span></span>|<span data-ttu-id="e2a16-133">Giá trị</span><span class="sxs-lookup"><span data-stu-id="e2a16-133">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="e2a16-134">Tên</span><span class="sxs-lookup"><span data-stu-id="e2a16-134">Name</span></span>|<span data-ttu-id="e2a16-135">Contoso trợ giúp</span><span class="sxs-lookup"><span data-stu-id="e2a16-135">Contoso Help</span></span>|  
   |<span data-ttu-id="e2a16-136">Tên hiển thị</span><span class="sxs-lookup"><span data-stu-id="e2a16-136">Display Name</span></span>|<span data-ttu-id="e2a16-137">Contoso trợ giúp</span><span class="sxs-lookup"><span data-stu-id="e2a16-137">Contoso Help</span></span>|  
   |<span data-ttu-id="e2a16-138">Loại Thành phần USD</span><span class="sxs-lookup"><span data-stu-id="e2a16-138">USD Component Type</span></span>|<span data-ttu-id="e2a16-139">Standard Web Application</span><span class="sxs-lookup"><span data-stu-id="e2a16-139">Standard Web Application</span></span>|  
   |<span data-ttu-id="e2a16-140">Allow Multiple Pages</span><span class="sxs-lookup"><span data-stu-id="e2a16-140">Allow Multiple Pages</span></span>|<span data-ttu-id="e2a16-141">Không</span><span class="sxs-lookup"><span data-stu-id="e2a16-141">No</span></span>|  
   |<span data-ttu-id="e2a16-142">Loại lưu trữ</span><span class="sxs-lookup"><span data-stu-id="e2a16-142">Hosting Type</span></span>|<span data-ttu-id="e2a16-143">IE Process</span><span class="sxs-lookup"><span data-stu-id="e2a16-143">IE Process</span></span>|

   <span data-ttu-id="e2a16-144">![Standard Web Application hosted control](../unified-service-desk/media/crm-itpro-usd-wt02-01-unified-interface.png "Standard Web Application hosted control")</span><span class="sxs-lookup"><span data-stu-id="e2a16-144">![Standard Web Application hosted control](../unified-service-desk/media/crm-itpro-usd-wt02-01-unified-interface.png "Standard Web Application hosted control")</span></span> 

6. <span data-ttu-id="e2a16-145">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-145">Click **Save**.</span></span>  

<a name="Step2"></a>   
## <a name="step-2-create-a-toolbar-container-type-of-hosted-control"></a><span data-ttu-id="e2a16-146">Step 2: Create a toolbar container type of hosted control</span><span class="sxs-lookup"><span data-stu-id="e2a16-146">Step 2: Create a toolbar container type of hosted control</span></span>  
 <span data-ttu-id="e2a16-147">Kiểm soát tổ chức bộ chứa thanh công cụ được sử dụng để giữ và hiển thị thanh công cụ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="e2a16-147">Toolbar Container hosted controls are used to hold and display the toolbars in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="e2a16-148">Trong phần này, bạn sẽ tạo loại **Bộ chứa thanh công cụ** của kiểm soát tổ chức mà sẽ xuất hiện trong vùng thanh công cụ của ứng dụng khách.</span><span class="sxs-lookup"><span data-stu-id="e2a16-148">In this section, you’ll create a **Toolbar Container** type of hosted control that appears in the toolbar region of the client application.</span></span>  

1. <span data-ttu-id="e2a16-149">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="e2a16-149">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="e2a16-150">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-150">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="e2a16-151">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-151">Click **New**.</span></span>  

5. <span data-ttu-id="e2a16-152">On the **New Hosted Control** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="e2a16-152">On the **New Hosted Control** page, specify the following values:</span></span>  

   |<span data-ttu-id="e2a16-153">Trường</span><span class="sxs-lookup"><span data-stu-id="e2a16-153">Field</span></span>|<span data-ttu-id="e2a16-154">Giá trị</span><span class="sxs-lookup"><span data-stu-id="e2a16-154">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="e2a16-155">Tên</span><span class="sxs-lookup"><span data-stu-id="e2a16-155">Name</span></span>|<span data-ttu-id="e2a16-156">Contoso về Bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="e2a16-156">Contoso About Toolbar Container</span></span>|  
   |<span data-ttu-id="e2a16-157">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="e2a16-157">USD Component Type</span></span>|<span data-ttu-id="e2a16-158">Bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="e2a16-158">Toolbar Container</span></span>|  
   |<span data-ttu-id="e2a16-159">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="e2a16-159">Display Group</span></span>|<span data-ttu-id="e2a16-160">Bàng điều khiển thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="e2a16-160">ToolbarPanel</span></span>|

   <span data-ttu-id="e2a16-161">![Toolbar Container hosted control](../unified-service-desk/media/crm-itpro-usd-wt02-02-unified-interface.png "Toolbar Container hosted control")</span><span class="sxs-lookup"><span data-stu-id="e2a16-161">![Toolbar Container hosted control](../unified-service-desk/media/crm-itpro-usd-wt02-02-unified-interface.png "Toolbar Container hosted control")</span></span> 

6. <span data-ttu-id="e2a16-162">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-162">Click **Save**.</span></span>  

<a name="Step3"></a>   
## <a name="step-3-add-a-toolbar-and-attach-it-to-the-toolbar-container"></a><span data-ttu-id="e2a16-163">Step 3: Add a toolbar and attach it to the toolbar container</span><span class="sxs-lookup"><span data-stu-id="e2a16-163">Step 3: Add a toolbar and attach it to the toolbar container</span></span>  
 <span data-ttu-id="e2a16-164">In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 2.</span><span class="sxs-lookup"><span data-stu-id="e2a16-164">In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 2.</span></span> <span data-ttu-id="e2a16-165">This is done to display the toolbar in your agent application.</span><span class="sxs-lookup"><span data-stu-id="e2a16-165">This is done to display the toolbar in your agent application.</span></span>  

1. <span data-ttu-id="e2a16-166">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="e2a16-166">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="e2a16-167">Bấm vào **Thanh công cụ**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-167">Click **Toolbars**.</span></span>  

4. <span data-ttu-id="e2a16-168">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-168">Click **New**.</span></span>  

5. <span data-ttu-id="e2a16-169">Trên trang **thanh công cụ mới**, nhập **Contoso về Thanh công cụ** trong hộp **tên**, sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-169">On the **New Toolbar** page, type **Contoso About Toolbar** in the **Name** box, and then click **Save**.</span></span>  

6. <span data-ttu-id="e2a16-170">Attach the toolbar to the toolbar container hosted control created in step 2.</span><span class="sxs-lookup"><span data-stu-id="e2a16-170">Attach the toolbar to the toolbar container hosted control created in step 2.</span></span> <span data-ttu-id="e2a16-171">On the nav bar, click the down arrow next to **Contoso About Toolbar**, and click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-171">On the nav bar, click the down arrow next to **Contoso About Toolbar**, and click **Hosted Controls**.</span></span>  

7. <span data-ttu-id="e2a16-172">Trên trang tiếp theo, bấm vào **Thêm kiểm soát tổ chức hiện có**, nhập `Contoso About Toolbar Container` trong thanh tìm kiếm và sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="e2a16-172">On the next page, click **Add Existing Hosted Control**, type `Contoso About Toolbar Container` in the search bar, and then press ENTER or click the search icon.</span></span>  

8. <span data-ttu-id="e2a16-173">Từ kết quả tìm kiếm, chọn **Bộ chứa thanh công cụ về Contoso**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-173">From the search results, select **Contoso About Toolbar Container**.</span></span>  

9. <span data-ttu-id="e2a16-174">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-174">Click **Save**.</span></span>  

<a name="Step4"></a>   
## <a name="step-4-add-a-toolbar-button-and-action-calls-to-display-the-webpage"></a><span data-ttu-id="e2a16-175">Bước 4: Thêm nút thanh công cụ và các cuộc gọi hành động để hiển thị trang web</span><span class="sxs-lookup"><span data-stu-id="e2a16-175">Step 4: Add a toolbar button and action calls to display the webpage</span></span>  
 <span data-ttu-id="e2a16-176">Trong bước này, thêm một nút trên thanh công cụ và đính kèm một cuộc gọi hành động cho nút để khi nút được nhấn vào, trang web đã chỉ định được hiển thị trong kiểm soát tổ chức mà bạn đã tạo ở bước 1.</span><span class="sxs-lookup"><span data-stu-id="e2a16-176">In this step, add a button on the toolbar and attach an action call to the button so that when the button is clicked, the specified webpage is displayed in the hosted control that you created in step 1.</span></span>  

1. <span data-ttu-id="e2a16-177">After you save the toolbar in step 3, the **Buttons** area becomes available.</span><span class="sxs-lookup"><span data-stu-id="e2a16-177">After you save the toolbar in step 3, the **Buttons** area becomes available.</span></span> <span data-ttu-id="e2a16-178">In the **Buttons** area, click **+** on the right corner to add a button.</span><span class="sxs-lookup"><span data-stu-id="e2a16-178">In the **Buttons** area, click **+** on the right corner to add a button.</span></span>  

2. <span data-ttu-id="e2a16-179">On the **New Toolbar Button** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="e2a16-179">On the **New Toolbar Button** page, specify the following values.</span></span>  

   |<span data-ttu-id="e2a16-180">Trường</span><span class="sxs-lookup"><span data-stu-id="e2a16-180">Field</span></span>|<span data-ttu-id="e2a16-181">Value</span><span class="sxs-lookup"><span data-stu-id="e2a16-181">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="e2a16-182">Tên</span><span class="sxs-lookup"><span data-stu-id="e2a16-182">Name</span></span>|<span data-ttu-id="e2a16-183">Contoso Hiển thị trợ giúp</span><span class="sxs-lookup"><span data-stu-id="e2a16-183">Contoso Show Help</span></span>|  
   |<span data-ttu-id="e2a16-184">Văn bản nút</span><span class="sxs-lookup"><span data-stu-id="e2a16-184">Button Text</span></span>|<span data-ttu-id="e2a16-185">Hiển thị trợ giúp</span><span class="sxs-lookup"><span data-stu-id="e2a16-185">Show Help</span></span>|  

   <span data-ttu-id="e2a16-186">![Create a new toolbar button](../unified-service-desk/media/crm-itpro-usd-wt02-03.png "Create a new toolbar button")</span><span class="sxs-lookup"><span data-stu-id="e2a16-186">![Create a new toolbar button](../unified-service-desk/media/crm-itpro-usd-wt02-03.png "Create a new toolbar button")</span></span>  

3. <span data-ttu-id="e2a16-187">Bấm vào **Lưu** để lưu hồ sơ và bật vùng **Hoạt động**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-187">Click **Save** to save the record, and enable the **Actions** area.</span></span>  

4. <span data-ttu-id="e2a16-188">Add two action calls to specify the URL of the webpage to navigate to for the hosted control that you created in step 1.</span><span class="sxs-lookup"><span data-stu-id="e2a16-188">Add two action calls to specify the URL of the webpage to navigate to for the hosted control that you created in step 1.</span></span> <span data-ttu-id="e2a16-189">Additionally, create another action call to on the **Contoso Global Manager** hosted control to display the hosted control created in step 1 in the agent application.</span><span class="sxs-lookup"><span data-stu-id="e2a16-189">Additionally, create another action call to on the **Contoso Global Manager** hosted control to display the hosted control created in step 1 in the agent application.</span></span>  

    <span data-ttu-id="e2a16-190">In the **Actions** area, click **+** on the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="e2a16-190">In the **Actions** area, click **+** on the right corner to add an action call.</span></span>  

5. <span data-ttu-id="e2a16-191">In the search box in the **Actions** area, press ENTER or click the search icon.</span><span class="sxs-lookup"><span data-stu-id="e2a16-191">In the search box in the **Actions** area, press ENTER or click the search icon.</span></span>  

6. <span data-ttu-id="e2a16-192">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span><span class="sxs-lookup"><span data-stu-id="e2a16-192">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>  

   <span data-ttu-id="e2a16-193">![Choose New to create an action call](../unified-service-desk/media/crm-itpro-usd-wt02-04.png "Choose New to create an action call")</span><span class="sxs-lookup"><span data-stu-id="e2a16-193">![Choose New to create an action call](../unified-service-desk/media/crm-itpro-usd-wt02-04.png "Choose New to create an action call")</span></span>  

7. <span data-ttu-id="e2a16-194">On the **New Action Call** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="e2a16-194">On the **New Action Call** page, specify the following values:</span></span>  


   |     <span data-ttu-id="e2a16-195">Trường</span><span class="sxs-lookup"><span data-stu-id="e2a16-195">Field</span></span>      |                        <span data-ttu-id="e2a16-196">Giá trị</span><span class="sxs-lookup"><span data-stu-id="e2a16-196">Value</span></span>                        |
   |----------------|-----------------------------------------------------|
   |      <span data-ttu-id="e2a16-197">Tên</span><span class="sxs-lookup"><span data-stu-id="e2a16-197">Name</span></span>      |          <span data-ttu-id="e2a16-198">Cuộc gọi hành động Contoso: Hiển thị trợ giúp</span><span class="sxs-lookup"><span data-stu-id="e2a16-198">Contoso Action Call: Display Help</span></span>          |
   |     <span data-ttu-id="e2a16-199">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="e2a16-199">Order</span></span>      |                          <span data-ttu-id="e2a16-200">1</span><span class="sxs-lookup"><span data-stu-id="e2a16-200">1</span></span>                          |
   | <span data-ttu-id="e2a16-201">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="e2a16-201">Hosted Control</span></span> |                    <span data-ttu-id="e2a16-202">Contoso trợ giúp</span><span class="sxs-lookup"><span data-stu-id="e2a16-202">Contoso Help</span></span>                     |
   |     <span data-ttu-id="e2a16-203">Hành động</span><span class="sxs-lookup"><span data-stu-id="e2a16-203">Action</span></span>     |                      <span data-ttu-id="e2a16-204">Navigate</span><span class="sxs-lookup"><span data-stu-id="e2a16-204">Navigate</span></span>                       |
   |      <span data-ttu-id="e2a16-205">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="e2a16-205">Data</span></span>      | <span data-ttu-id="e2a16-206">url=<http://go.microsoft.com/fwlink/?LinkID=856273></span><span class="sxs-lookup"><span data-stu-id="e2a16-206">url=<http://go.microsoft.com/fwlink/?LinkID=856273></span></span> |

   <span data-ttu-id="e2a16-207">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-05-unified-interface.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="e2a16-207">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-05-unified-interface.png "Create an action call in Unified Service Desk")</span></span>  

8. <span data-ttu-id="e2a16-208">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-208">Click **Save**.</span></span> <span data-ttu-id="e2a16-209">Cuộc gọi hành động mới được thêm vào nút **Contoso Hiển thị Trợ giúp**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-209">The new action call is added to the **Contoso Show Help** button.</span></span>  

9. <span data-ttu-id="e2a16-210">Thêm một cuộc gọi hành động vào nút để đặt trọng tâm trên kiểm soát tổ chức mà hiển thị trang web trong ứng dụng khách.</span><span class="sxs-lookup"><span data-stu-id="e2a16-210">Add another action call to the button to set the focus on the hosted control that displays the webpage in the client application.</span></span> <span data-ttu-id="e2a16-211">In the **Actions** area, click **+** in the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="e2a16-211">In the **Actions** area, click **+** in the right corner to add an action call.</span></span>  

10. <span data-ttu-id="e2a16-212">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span><span class="sxs-lookup"><span data-stu-id="e2a16-212">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>  

11. <span data-ttu-id="e2a16-213">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="e2a16-213">On the **New Action Call** page, specify the following values.</span></span>  

    |<span data-ttu-id="e2a16-214">Trường</span><span class="sxs-lookup"><span data-stu-id="e2a16-214">Field</span></span>|<span data-ttu-id="e2a16-215">Giá trị</span><span class="sxs-lookup"><span data-stu-id="e2a16-215">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="e2a16-216">Tên</span><span class="sxs-lookup"><span data-stu-id="e2a16-216">Name</span></span>|<span data-ttu-id="e2a16-217">Cuộc gọi hành động Contoso: Hiển thị kiểm soát tổ chức trợ giúp</span><span class="sxs-lookup"><span data-stu-id="e2a16-217">Contoso Action Call: Display Help Hosted Control</span></span>|  
    |<span data-ttu-id="e2a16-218">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="e2a16-218">Order</span></span>|<span data-ttu-id="e2a16-219">2</span><span class="sxs-lookup"><span data-stu-id="e2a16-219">2</span></span>|  
    |<span data-ttu-id="e2a16-220">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="e2a16-220">Hosted Control</span></span>|<span data-ttu-id="e2a16-221">Contoso Global Manager</span><span class="sxs-lookup"><span data-stu-id="e2a16-221">Contoso Global Manager</span></span>|  
    |<span data-ttu-id="e2a16-222">Hành động</span><span class="sxs-lookup"><span data-stu-id="e2a16-222">Action</span></span>|<span data-ttu-id="e2a16-223">Hiển thị tab</span><span class="sxs-lookup"><span data-stu-id="e2a16-223">ShowTab</span></span>|  
    |<span data-ttu-id="e2a16-224">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="e2a16-224">Data</span></span>|<span data-ttu-id="e2a16-225">Contoso trợ giúp</span><span class="sxs-lookup"><span data-stu-id="e2a16-225">Contoso Help</span></span>|  

    <span data-ttu-id="e2a16-226">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-06-unified-interface.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="e2a16-226">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-06-unified-interface.png "Create an action call in Unified Service Desk")</span></span>  

12. <span data-ttu-id="e2a16-227">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-227">Click **Save**.</span></span> <span data-ttu-id="e2a16-228">Cuộc gọi hành động mới được thêm vào nút **Contoso Hiển thị Trợ giúp**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-228">The new action call gets added to the **Contoso Show Help** button.</span></span> <span data-ttu-id="e2a16-229">Bạn có thể nhìn thấy cả hai cuộc gọi hành động thêm vào nút thanh công cụ.</span><span class="sxs-lookup"><span data-stu-id="e2a16-229">You can see both action calls added to the toolbar button.</span></span>  

    <span data-ttu-id="e2a16-230">![Action calls added to the toolbar button](../unified-service-desk/media/crm-itpro-usd-wt02-07.png "Action calls added to the toolbar button")</span><span class="sxs-lookup"><span data-stu-id="e2a16-230">![Action calls added to the toolbar button](../unified-service-desk/media/crm-itpro-usd-wt02-07.png "Action calls added to the toolbar button")</span></span>  

<a name="Step5"></a>   
## <a name="step-5-add-the-controls-to-the-configuration"></a><span data-ttu-id="e2a16-231">Step 5: Add the controls to the configuration</span><span class="sxs-lookup"><span data-stu-id="e2a16-231">Step 5: Add the controls to the configuration</span></span>  
 <span data-ttu-id="e2a16-232">Trong bước này, bạn sẽ thêm cuộc gọi hành động, kiểm soát tổ chức và thanh công cụ đã tạo trong cách này vào **Cấu hình Contoso** để hiển thị các kiểm soát này cho người dùng được chỉ định cho cấu hình này.</span><span class="sxs-lookup"><span data-stu-id="e2a16-232">In this step, add the action calls, hosted controls, and toolbar that you created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span></span> <span data-ttu-id="e2a16-233">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="e2a16-233">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span></span>  

 <span data-ttu-id="e2a16-234">Add the following to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-234">Add the following to **Contoso Configuration**.</span></span>  

|<span data-ttu-id="e2a16-235">Tên kiểm soát</span><span class="sxs-lookup"><span data-stu-id="e2a16-235">Control name</span></span>|<span data-ttu-id="e2a16-236">Loại kiểm soát</span><span class="sxs-lookup"><span data-stu-id="e2a16-236">Control type</span></span>|  
|------------------|------------------|  
|<span data-ttu-id="e2a16-237">Cuộc gọi hành động Contoso: Hiển thị trợ giúp</span><span class="sxs-lookup"><span data-stu-id="e2a16-237">Contoso Action Call: Display Help</span></span>|<span data-ttu-id="e2a16-238">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="e2a16-238">Action Call</span></span>|  
|<span data-ttu-id="e2a16-239">Cuộc gọi hành động Contoso: Hiển thị kiểm soát tổ chức trợ giúp</span><span class="sxs-lookup"><span data-stu-id="e2a16-239">Contoso Action Call: Display Help Hosted Control</span></span>|<span data-ttu-id="e2a16-240">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="e2a16-240">Action Call</span></span>|  
|<span data-ttu-id="e2a16-241">Contoso trợ giúp</span><span class="sxs-lookup"><span data-stu-id="e2a16-241">Contoso Help</span></span>|<span data-ttu-id="e2a16-242">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="e2a16-242">Hosted Control</span></span>|  
|<span data-ttu-id="e2a16-243">Contoso về Bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="e2a16-243">Contoso About Toolbar Container</span></span>|<span data-ttu-id="e2a16-244">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="e2a16-244">Hosted Control</span></span>|  
|<span data-ttu-id="e2a16-245">Contoso về thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="e2a16-245">Contoso About Toolbar</span></span>|<span data-ttu-id="e2a16-246">Thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="e2a16-246">Toolbar</span></span>|  

 <span data-ttu-id="e2a16-247">To add a control to the configuration:</span><span class="sxs-lookup"><span data-stu-id="e2a16-247">To add a control to the configuration:</span></span>  

1. <span data-ttu-id="e2a16-248">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="e2a16-248">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. <span data-ttu-id="e2a16-249">On the nav bar, click **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-249">On the nav bar, click **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.</span></span>  

3. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

4. <span data-ttu-id="e2a16-250">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-250">Click **Configuration**.</span></span>  

5. <span data-ttu-id="e2a16-251">Click **Contoso Configuration** to open the definition.</span><span class="sxs-lookup"><span data-stu-id="e2a16-251">Click **Contoso Configuration** to open the definition.</span></span>  

6. <span data-ttu-id="e2a16-252">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-252">On the nav bar, click the down arrow next to **Contoso Configuration**, and select **Action Calls**.</span></span>  

7. <span data-ttu-id="e2a16-253">Trên trang tiếp theo, bấm vào **Thêm Cuộc gọi Hành động Hiện có**, nhập “`Contoso Action Call`” vào thanh tìm kiếm, sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="e2a16-253">On the next page, click **Add Existing Action Call**, type “`Contoso Action Call`” in the search bar, and then press ENTER or click the search icon.</span></span>  

8. <span data-ttu-id="e2a16-254">Cả cuộc gọi hành động được hiển thị trong kết quả tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="e2a16-254">Both action calls are displayed in the search results.</span></span> <span data-ttu-id="e2a16-255">Thêm cả hai người trong số chúng.</span><span class="sxs-lookup"><span data-stu-id="e2a16-255">Add both of them.</span></span>  

9. <span data-ttu-id="e2a16-256">Tương tự, thêm cả hai kiểm soát tổ chức và thanh công cụ bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Kiểm soát tổ chức** và **thanh công cụ** lần lượt.</span><span class="sxs-lookup"><span data-stu-id="e2a16-256">Similarly, add both of the hosted controls and the toolbar by clicking the down arrow next to **Contoso Configuration**, and clicking **Hosted Controls** and **Toolbars** respectively.</span></span>  

10. <span data-ttu-id="e2a16-257">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="e2a16-257">Click **Save**.</span></span>  

<a name="Step6"></a>   
## <a name="step-6-test-the-application"></a><span data-ttu-id="e2a16-258">Step 6: Test the application</span><span class="sxs-lookup"><span data-stu-id="e2a16-258">Step 6: Test the application</span></span>  
 <span data-ttu-id="e2a16-259">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="e2a16-259">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span></span> <span data-ttu-id="e2a16-260">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)</span><span class="sxs-lookup"><span data-stu-id="e2a16-260">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)</span></span> 

 <span data-ttu-id="e2a16-261">Ứng dụng đại lý của bạn bây giờ sẽ có nút **Hiển thị trợ giúp** ở góc trên bên phải:</span><span class="sxs-lookup"><span data-stu-id="e2a16-261">Your agent application will now have a **Show Help** button at the top-right corner:</span></span>  

 <span data-ttu-id="e2a16-262">![Show Help button in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-08.png "Show Help button in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="e2a16-262">![Show Help button in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt02-08.png "Show Help button in Unified Service Desk")</span></span>  

 <span data-ttu-id="e2a16-263">Nhấn vào **Hiển thị trợ giúp** Hiển thị URL web đã chỉ định trong ứng dụng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="e2a16-263">Clicking **Show Help** displays the specified web URL within the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application.</span></span>  

 <span data-ttu-id="e2a16-264">![Help displayed in the client application](../unified-service-desk/media/crm-itpro-usd-wt02-09.png "Help displayed in the client application")</span><span class="sxs-lookup"><span data-stu-id="e2a16-264">![Help displayed in the client application](../unified-service-desk/media/crm-itpro-usd-wt02-09.png "Help displayed in the client application")</span></span>  

<a name="Conclusion"></a>   
## <a name="conclusion"></a><span data-ttu-id="e2a16-265">Kết luận</span><span class="sxs-lookup"><span data-stu-id="e2a16-265">Conclusion</span></span>  
 <span data-ttu-id="e2a16-266">Trong cách này, bạn học cách hiển thị trang web [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] trong ứng dụng khách.</span><span class="sxs-lookup"><span data-stu-id="e2a16-266">In this walkthrough, you learned how to display a webpage in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.</span></span> <span data-ttu-id="e2a16-267">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span><span class="sxs-lookup"><span data-stu-id="e2a16-267">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span></span>  

### <a name="see-also"></a><span data-ttu-id="e2a16-268">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e2a16-268">See also</span></span>
 [<span data-ttu-id="e2a16-269">Support for Unified Interface Apps in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="e2a16-269">Support for Unified Interface Apps in Unified Service Desk</span></span>](../unified-service-desk/admin/Support-unified-interfaces-apps-usd.md)

 [<span data-ttu-id="e2a16-270">Unified Interface Page (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="e2a16-270">Unified Interface Page (Hosted Control)</span></span>](../unified-service-desk/unified-interface-page-hosted-control.md)

 [<span data-ttu-id="e2a16-271">Unified Service Desk and Unified Interface Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="e2a16-271">Unified Service Desk and Unified Interface Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md)

 [<span data-ttu-id="e2a16-272">Walkthrough 1: Build a simple agent application for Unified Interface Apps</span><span class="sxs-lookup"><span data-stu-id="e2a16-272">Walkthrough 1: Build a simple agent application for Unified Interface Apps</span></span>](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)

 [<span data-ttu-id="e2a16-273">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application</span><span class="sxs-lookup"><span data-stu-id="e2a16-273">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application</span></span>](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)

 [<span data-ttu-id="e2a16-274">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application</span><span class="sxs-lookup"><span data-stu-id="e2a16-274">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application</span></span>](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md)

 [<span data-ttu-id="e2a16-275">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span><span class="sxs-lookup"><span data-stu-id="e2a16-275">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span></span>](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md)

 [<span data-ttu-id="e2a16-276">Walkthrough 6: Configure the Debugger hosted control in your agent application</span><span class="sxs-lookup"><span data-stu-id="e2a16-276">Walkthrough 6: Configure the Debugger hosted control in your agent application</span></span>](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md)

 [<span data-ttu-id="e2a16-277">Walkthrough 7: Configure agent scripting in your agent application</span><span class="sxs-lookup"><span data-stu-id="e2a16-277">Walkthrough 7: Configure agent scripting in your agent application</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)
