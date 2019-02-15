---
title: 'Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records of Unified Interface app in your agent application | MicrosoftDocs'
description: Demonstrates how to display Unified Interface apps records in Unified Service Desk.
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
ms.assetid: FD393D95-FBB9-434B-86B1-23747FBB5B70
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
ms.openlocfilehash: 69cba200c28ce9b840260016cb99d75728671ad2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386286"
---
# <a name="walkthrough-3-display-microsoft-dynamics-365-for-customer-engagement-apps-unified-interface-apps-records-in-your-agent-application"></a><span data-ttu-id="04c1c-103">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application</span><span class="sxs-lookup"><span data-stu-id="04c1c-103">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application</span></span>
<span data-ttu-id="04c1c-104">This walkthrough demonstrates how to display [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps records of Unified Interface Apps in your agent application.</span><span class="sxs-lookup"><span data-stu-id="04c1c-104">This walkthrough demonstrates how to display [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps records of Unified Interface Apps in your agent application.</span></span> <span data-ttu-id="04c1c-105">In this walkthrough, you’ll display all the account and contact records in the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="04c1c-105">In this walkthrough, you’ll display all the account and contact records in the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span> <span data-ttu-id="04c1c-106">You’ll also create a search button with drop-down menu items for displaying accounts and contacts in the agent application.</span><span class="sxs-lookup"><span data-stu-id="04c1c-106">You’ll also create a search button with drop-down menu items for displaying accounts and contacts in the agent application.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="04c1c-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="04c1c-107">Prerequisites</span></span>  

- <span data-ttu-id="04c1c-108">You must have completed [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="04c1c-108">You must have completed [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span></span> <span data-ttu-id="04c1c-109">The configurations that you completed in walkthrough 1 are required in this walkthrough.</span><span class="sxs-lookup"><span data-stu-id="04c1c-109">The configurations that you completed in walkthrough 1 are required in this walkthrough.</span></span>  

- <span data-ttu-id="04c1c-110">Cách này giả định rằng bạn sẽ đang sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên ở cuối cách này để kiểm tra ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="04c1c-110">This walkthrough assumes that you will be using the same user credential that you used in walkthrough 1 to sign in to the agent application at the end of the walkthrough to test the application.</span></span> <span data-ttu-id="04c1c-111">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-111">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="04c1c-112">[Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)</span><span class="sxs-lookup"><span data-stu-id="04c1c-112">[Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)</span></span>  

- <span data-ttu-id="04c1c-113">You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="04c1c-113">You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  

  - <span data-ttu-id="04c1c-114">The following two types of hosted controls: Unified Interface Page and Toolbar Container.</span><span class="sxs-lookup"><span data-stu-id="04c1c-114">The following two types of hosted controls: Unified Interface Page and Toolbar Container.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="04c1c-115">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span><span class="sxs-lookup"><span data-stu-id="04c1c-115">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span></span>  

  - <span data-ttu-id="04c1c-116">Action call and how to configure it.</span><span class="sxs-lookup"><span data-stu-id="04c1c-116">Action call and how to configure it.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="04c1c-117">[Action calls](../unified-service-desk/action-calls.md)</span><span class="sxs-lookup"><span data-stu-id="04c1c-117">[Action calls](../unified-service-desk/action-calls.md)</span></span>  

  - <span data-ttu-id="04c1c-118">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span><span class="sxs-lookup"><span data-stu-id="04c1c-118">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="04c1c-119">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="04c1c-119">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span></span>  

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a><span data-ttu-id="04c1c-120">In This Walkthrough</span><span class="sxs-lookup"><span data-stu-id="04c1c-120">In This Walkthrough</span></span>  
 [<span data-ttu-id="04c1c-121">Step 1: Create Unified Interface Page type of hosted controls to display account and contact records</span><span class="sxs-lookup"><span data-stu-id="04c1c-121">Step 1: Create Unified Interface Page type of hosted controls to display account and contact records</span></span>](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step1)  

 [<span data-ttu-id="04c1c-122">Bước 2: Tạo loại bộ chứa công cụ của kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="04c1c-122">Step 2: Create a toolbar container type of hosted control</span></span>](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step2)  

 [<span data-ttu-id="04c1c-123">Bước 3: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="04c1c-123">Step 3: Add a toolbar and attach it to the toolbar container</span></span>](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step3)  

 [<span data-ttu-id="04c1c-124">Step 4: Add toolbar buttons and action calls to display Dynamics 365 for Customer Engagement apps records</span><span class="sxs-lookup"><span data-stu-id="04c1c-124">Step 4: Add toolbar buttons and action calls to display Dynamics 365 for Customer Engagement apps records</span></span>](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step4)  

 [<span data-ttu-id="04c1c-125">Bước 5: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="04c1c-125">Step 5: Add the controls to the configuration</span></span>](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step5)  

 [<span data-ttu-id="04c1c-126">Bước 6: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="04c1c-126">Step 6: Test the application</span></span>](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step6)  

 [<span data-ttu-id="04c1c-127">Kết luận</span><span class="sxs-lookup"><span data-stu-id="04c1c-127">Conclusion</span></span>](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md#Conclusion)

<a name="Step1"></a>   
## <a name="step-1-create-unified-interface-page-type-of-hosted-controls-to-display-account-and-contact-records"></a><span data-ttu-id="04c1c-128">Step 1: Create Unified Interface Page type of hosted controls to display account and contact records</span><span class="sxs-lookup"><span data-stu-id="04c1c-128">Step 1: Create Unified Interface Page type of hosted controls to display account and contact records</span></span>  
 <span data-ttu-id="04c1c-129">In this step, you’ll create two hosted controls of **Unified Interface Page** type to display the account and contact records respectively.</span><span class="sxs-lookup"><span data-stu-id="04c1c-129">In this step, you’ll create two hosted controls of **Unified Interface Page** type to display the account and contact records respectively.</span></span>  

1. <span data-ttu-id="04c1c-130">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="04c1c-130">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="04c1c-131">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-131">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="04c1c-132">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-132">Click **New**.</span></span>  

5. <span data-ttu-id="04c1c-133">On the **New Hosted Control** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="04c1c-133">On the **New Hosted Control** page, specify the following values:</span></span>  

   |<span data-ttu-id="04c1c-134">Trường</span><span class="sxs-lookup"><span data-stu-id="04c1c-134">Field</span></span>|<span data-ttu-id="04c1c-135">Giá trị</span><span class="sxs-lookup"><span data-stu-id="04c1c-135">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="04c1c-136">Tên</span><span class="sxs-lookup"><span data-stu-id="04c1c-136">Name</span></span>|<span data-ttu-id="04c1c-137">Contoso Accounts Search</span><span class="sxs-lookup"><span data-stu-id="04c1c-137">Contoso Accounts Search</span></span>|  
   |<span data-ttu-id="04c1c-138">Tên Hiển thị</span><span class="sxs-lookup"><span data-stu-id="04c1c-138">Display Name</span></span>|<span data-ttu-id="04c1c-139">Contoso: Tài khoản</span><span class="sxs-lookup"><span data-stu-id="04c1c-139">Contoso: Accounts</span></span>|  
   |<span data-ttu-id="04c1c-140">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="04c1c-140">USD Component Type</span></span>|<span data-ttu-id="04c1c-141">Unified Interface Page</span><span class="sxs-lookup"><span data-stu-id="04c1c-141">Unified Interface Page</span></span>|  
   |<span data-ttu-id="04c1c-142">Allow Multiple Pages</span><span class="sxs-lookup"><span data-stu-id="04c1c-142">Allow Multiple Pages</span></span>|<span data-ttu-id="04c1c-143">Không</span><span class="sxs-lookup"><span data-stu-id="04c1c-143">No</span></span>|
   |<span data-ttu-id="04c1c-144">Pre-Fetch Data</span><span class="sxs-lookup"><span data-stu-id="04c1c-144">Pre-Fetch Data</span></span>|<span data-ttu-id="04c1c-145">Đã kiểm tra</span><span class="sxs-lookup"><span data-stu-id="04c1c-145">Checked</span></span>|
   |<span data-ttu-id="04c1c-146">Application is Global</span><span class="sxs-lookup"><span data-stu-id="04c1c-146">Application is Global</span></span>|<span data-ttu-id="04c1c-147">Đã kiểm tra</span><span class="sxs-lookup"><span data-stu-id="04c1c-147">Checked</span></span>|  
   |<span data-ttu-id="04c1c-148">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="04c1c-148">Display Group</span></span>|<span data-ttu-id="04c1c-149">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="04c1c-149">MainPanel</span></span>|  

   <span data-ttu-id="04c1c-150">![Create a hosted control for displaying accounts](../unified-service-desk/media/crm-itpro-usd-wt03-01-unified-interface.png "Create a hosted control for displaying accounts")</span><span class="sxs-lookup"><span data-stu-id="04c1c-150">![Create a hosted control for displaying accounts](../unified-service-desk/media/crm-itpro-usd-wt03-01-unified-interface.png "Create a hosted control for displaying accounts")</span></span>  

6. <span data-ttu-id="04c1c-151">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-151">Click **Save**.</span></span>  

7. <span data-ttu-id="04c1c-152">Click **New** to create another hosted control for displaying contact records.</span><span class="sxs-lookup"><span data-stu-id="04c1c-152">Click **New** to create another hosted control for displaying contact records.</span></span>  

8. <span data-ttu-id="04c1c-153">Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="04c1c-153">On the **New Hosted Control** page, specify the following values:</span></span>  

   |<span data-ttu-id="04c1c-154">Trường</span><span class="sxs-lookup"><span data-stu-id="04c1c-154">Field</span></span>|<span data-ttu-id="04c1c-155">Giá trị</span><span class="sxs-lookup"><span data-stu-id="04c1c-155">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="04c1c-156">Tên</span><span class="sxs-lookup"><span data-stu-id="04c1c-156">Name</span></span>|<span data-ttu-id="04c1c-157">Contoso Contacts Search</span><span class="sxs-lookup"><span data-stu-id="04c1c-157">Contoso Contacts Search</span></span>|  
   |<span data-ttu-id="04c1c-158">Tên Hiển thị</span><span class="sxs-lookup"><span data-stu-id="04c1c-158">Display Name</span></span>|<span data-ttu-id="04c1c-159">Contoso: Liên hệ</span><span class="sxs-lookup"><span data-stu-id="04c1c-159">Contoso: Contacts</span></span>|  
   |<span data-ttu-id="04c1c-160">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="04c1c-160">USD Component Type</span></span>|<span data-ttu-id="04c1c-161">Unified Interface Page</span><span class="sxs-lookup"><span data-stu-id="04c1c-161">Unified Interface Page</span></span>|  
   |<span data-ttu-id="04c1c-162">Allow Multiple Pages</span><span class="sxs-lookup"><span data-stu-id="04c1c-162">Allow Multiple Pages</span></span>|<span data-ttu-id="04c1c-163">Không</span><span class="sxs-lookup"><span data-stu-id="04c1c-163">No</span></span>|
   |<span data-ttu-id="04c1c-164">Pre-Fetch Data</span><span class="sxs-lookup"><span data-stu-id="04c1c-164">Pre-Fetch Data</span></span>|<span data-ttu-id="04c1c-165">Đã kiểm tra</span><span class="sxs-lookup"><span data-stu-id="04c1c-165">Checked</span></span>|
   |<span data-ttu-id="04c1c-166">Application is Global</span><span class="sxs-lookup"><span data-stu-id="04c1c-166">Application is Global</span></span>|<span data-ttu-id="04c1c-167">Đã kiểm tra</span><span class="sxs-lookup"><span data-stu-id="04c1c-167">Checked</span></span>|  
   |<span data-ttu-id="04c1c-168">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="04c1c-168">Display Group</span></span>|<span data-ttu-id="04c1c-169">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="04c1c-169">MainPanel</span></span>|  

   <span data-ttu-id="04c1c-170">![Create hosted control for displaying contacts](../unified-service-desk/media/crm-itpro-usd-wt03-02-unified-interface.png "Create hosted control for displaying contacts")</span><span class="sxs-lookup"><span data-stu-id="04c1c-170">![Create hosted control for displaying contacts](../unified-service-desk/media/crm-itpro-usd-wt03-02-unified-interface.png "Create hosted control for displaying contacts")</span></span>  

9. <span data-ttu-id="04c1c-171">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-171">Click **Save**.</span></span>  

<a name="Step2"></a>   
## <a name="step-2-create-a-toolbar-container-type-of-hosted-control"></a><span data-ttu-id="04c1c-172">Step 2: Create a toolbar container type of hosted control</span><span class="sxs-lookup"><span data-stu-id="04c1c-172">Step 2: Create a toolbar container type of hosted control</span></span>  
 <span data-ttu-id="04c1c-173">Loại bộ chứa thanh công cụ của kiểm soát tổ chức được sử dụng để giữ và hiển thị thanh công cụ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="04c1c-173">Toolbar Container type of hosted controls are used to hold and display the toolbars in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="04c1c-174">In this section, you’ll create a **Toolbar Container** hosted control that will appear at the top of the client application.</span><span class="sxs-lookup"><span data-stu-id="04c1c-174">In this section, you’ll create a **Toolbar Container** hosted control that will appear at the top of the client application.</span></span>  

1. <span data-ttu-id="04c1c-175">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="04c1c-175">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="04c1c-176">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-176">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="04c1c-177">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-177">Click **New**.</span></span>  

5. <span data-ttu-id="04c1c-178">On the **New Hosted Control** page, specify the following values</span><span class="sxs-lookup"><span data-stu-id="04c1c-178">On the **New Hosted Control** page, specify the following values</span></span>  

   |<span data-ttu-id="04c1c-179">Trường</span><span class="sxs-lookup"><span data-stu-id="04c1c-179">Field</span></span>|<span data-ttu-id="04c1c-180">Giá trị</span><span class="sxs-lookup"><span data-stu-id="04c1c-180">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="04c1c-181">Tên</span><span class="sxs-lookup"><span data-stu-id="04c1c-181">Name</span></span>|<span data-ttu-id="04c1c-182">Bộ chứa thanh công cụ chính Contoso</span><span class="sxs-lookup"><span data-stu-id="04c1c-182">Contoso Main Toolbar Container</span></span>|  
   |<span data-ttu-id="04c1c-183">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="04c1c-183">USD Component Type</span></span>|<span data-ttu-id="04c1c-184">Bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="04c1c-184">Toolbar Container</span></span>|  
   |<span data-ttu-id="04c1c-185">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="04c1c-185">Display Group</span></span>|<span data-ttu-id="04c1c-186">Bàng điều khiển thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="04c1c-186">ToolbarPanel</span></span>|  

   <span data-ttu-id="04c1c-187">![Toolbar Container hosted control](../unified-service-desk/media/crm-itpro-usd-wt03-03-unified-interface.png "Toolbar Container hosted control")</span><span class="sxs-lookup"><span data-stu-id="04c1c-187">![Toolbar Container hosted control](../unified-service-desk/media/crm-itpro-usd-wt03-03-unified-interface.png "Toolbar Container hosted control")</span></span>

6. <span data-ttu-id="04c1c-188">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-188">Click **Save**.</span></span>  

<a name="Step3"></a>   
## <a name="step-3-add-a-toolbar-and-attach-it-to-the-toolbar-container"></a><span data-ttu-id="04c1c-189">Step 3: Add a toolbar and attach it to the toolbar container</span><span class="sxs-lookup"><span data-stu-id="04c1c-189">Step 3: Add a toolbar and attach it to the toolbar container</span></span>  
 <span data-ttu-id="04c1c-190">In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 2.</span><span class="sxs-lookup"><span data-stu-id="04c1c-190">In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 2.</span></span> <span data-ttu-id="04c1c-191">This is done to display the toolbar in your agent application.</span><span class="sxs-lookup"><span data-stu-id="04c1c-191">This is done to display the toolbar in your agent application.</span></span>  

1. <span data-ttu-id="04c1c-192">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="04c1c-192">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="04c1c-193">Bấm vào **Thanh công cụ**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-193">Click **Toolbars**.</span></span>  

4. <span data-ttu-id="04c1c-194">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-194">Click **New**.</span></span>  

5. <span data-ttu-id="04c1c-195">On the **New Toolbar** page, type **Contoso Main Toolbar** in the **Name** box, and then click **Save**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-195">On the **New Toolbar** page, type **Contoso Main Toolbar** in the **Name** box, and then click **Save**.</span></span>  

6. <span data-ttu-id="04c1c-196">Attach the toolbar to the toolbar container hosted control created in step 2.</span><span class="sxs-lookup"><span data-stu-id="04c1c-196">Attach the toolbar to the toolbar container hosted control created in step 2.</span></span> <span data-ttu-id="04c1c-197">On the nav bar, click the down arrow next to **Contoso Main Toolbar**, and click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-197">On the nav bar, click the down arrow next to **Contoso Main Toolbar**, and click **Hosted Controls**.</span></span>  

7. <span data-ttu-id="04c1c-198">Trên trang tiếp theo, bấm vào **Thêm kiểm soát tổ chức hiện có**, nhập `Contoso Main Toolbar Container` trong thanh tìm kiếm và sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="04c1c-198">On the next page, click **Add Existing Hosted Control**, type `Contoso Main Toolbar Container` in the search bar, and then press ENTER or click the search icon.</span></span>  

8. <span data-ttu-id="04c1c-199">Từ kết quả tìm kiếm, hãy nhấp vào **Bộ chứa thanh công cụ chính Contoso** để thêm.</span><span class="sxs-lookup"><span data-stu-id="04c1c-199">From the search result, click **Contoso Main Toolbar Container** to add.</span></span>  

9. <span data-ttu-id="04c1c-200">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-200">Click **Save**.</span></span>  

<a name="Step4"></a>   
## <a name="step-4-add-toolbar-buttons-and-action-calls-to-display-dynamics-365-for-customer-engagement-apps-records--from-unified-interface-apps"></a><span data-ttu-id="04c1c-201">Step 4: Add toolbar buttons and action calls to display Dynamics 365 for Customer Engagement apps records  from Unified Interface Apps</span><span class="sxs-lookup"><span data-stu-id="04c1c-201">Step 4: Add toolbar buttons and action calls to display Dynamics 365 for Customer Engagement apps records  from Unified Interface Apps</span></span>
 <span data-ttu-id="04c1c-202">In this step, you’ll add buttons on the toolbar and attach action calls to the buttons so that when the button is clicked, appropriate [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records are displayed in the hosted controls that were created in step 1.</span><span class="sxs-lookup"><span data-stu-id="04c1c-202">In this step, you’ll add buttons on the toolbar and attach action calls to the buttons so that when the button is clicked, appropriate [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records are displayed in the hosted controls that were created in step 1.</span></span> <span data-ttu-id="04c1c-203">You’ll configure the search button so that clicking the button displays the account and contact submenu items, and clicking a button displays the respective [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records.</span><span class="sxs-lookup"><span data-stu-id="04c1c-203">You’ll configure the search button so that clicking the button displays the account and contact submenu items, and clicking a button displays the respective [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records.</span></span>  

1. <span data-ttu-id="04c1c-204">After you save the toolbar in step 3, the **Buttons** area becomes available.</span><span class="sxs-lookup"><span data-stu-id="04c1c-204">After you save the toolbar in step 3, the **Buttons** area becomes available.</span></span> <span data-ttu-id="04c1c-205">In the **Buttons** area, click **+** on the right corner to add a button.</span><span class="sxs-lookup"><span data-stu-id="04c1c-205">In the **Buttons** area, click **+** on the right corner to add a button.</span></span>  

2. <span data-ttu-id="04c1c-206">On the **New Toolbar Button** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="04c1c-206">On the **New Toolbar Button** page, specify the following values:</span></span>  


   |    <span data-ttu-id="04c1c-207">Trường</span><span class="sxs-lookup"><span data-stu-id="04c1c-207">Field</span></span>    |                                          <span data-ttu-id="04c1c-208">Giá trị</span><span class="sxs-lookup"><span data-stu-id="04c1c-208">Value</span></span>                                           |
   |-------------|------------------------------------------------------------------------------------------|
   |    <span data-ttu-id="04c1c-209">Tên</span><span class="sxs-lookup"><span data-stu-id="04c1c-209">Name</span></span>     |                                  <span data-ttu-id="04c1c-210">Contoso Search Button</span><span class="sxs-lookup"><span data-stu-id="04c1c-210">Contoso Search Button</span></span>                                   |
   | <span data-ttu-id="04c1c-211">Văn bản nút</span><span class="sxs-lookup"><span data-stu-id="04c1c-211">Button Text</span></span> |                                          <span data-ttu-id="04c1c-212">TÌM KIẾM</span><span class="sxs-lookup"><span data-stu-id="04c1c-212">SEARCH</span></span>                                          |
   |   <span data-ttu-id="04c1c-213">Chú giải công cụ</span><span class="sxs-lookup"><span data-stu-id="04c1c-213">Tooltip</span></span>   | <span data-ttu-id="04c1c-214">Search [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps accounts and contacts</span><span class="sxs-lookup"><span data-stu-id="04c1c-214">Search [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps accounts and contacts</span></span> |
   |    <span data-ttu-id="04c1c-215">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="04c1c-215">Order</span></span>    |                                            <span data-ttu-id="04c1c-216">1</span><span class="sxs-lookup"><span data-stu-id="04c1c-216">1</span></span>                                             |

   <span data-ttu-id="04c1c-217">![Create the Search toolbar button](../unified-service-desk/media/crm-itpro-usd-wt03-04.png "Create the Search toolbar button")</span><span class="sxs-lookup"><span data-stu-id="04c1c-217">![Create the Search toolbar button](../unified-service-desk/media/crm-itpro-usd-wt03-04.png "Create the Search toolbar button")</span></span>

3. <span data-ttu-id="04c1c-218">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-218">Click **Save**.</span></span>

4. <span data-ttu-id="04c1c-219">On the nav bar, click the down arrow next to Contoso Search Button, and click Toolbar Buttons.</span><span class="sxs-lookup"><span data-stu-id="04c1c-219">On the nav bar, click the down arrow next to Contoso Search Button, and click Toolbar Buttons.</span></span>

   > [!NOTE]
   >  <span data-ttu-id="04c1c-220">Bạn hiện đang thêm nút thanh công cụ phụ vào nút thanh công cụ hiện có để tạo cấu trúc menu phụ.</span><span class="sxs-lookup"><span data-stu-id="04c1c-220">You are now adding child toolbar buttons to an existing toolbar button to create a submenu structure.</span></span>

5. <span data-ttu-id="04c1c-221">Trên trang tiếp theo, bấm vào **thêm nút thanh công cụ mới**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-221">On the next page, click **Add New Toolbar Button**.</span></span>

6. <span data-ttu-id="04c1c-222">Trên trang **Nút thanh công cụ mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="04c1c-222">On the **New Toolbar Button** page, specify the following values.</span></span>

   |<span data-ttu-id="04c1c-223">Trường</span><span class="sxs-lookup"><span data-stu-id="04c1c-223">Field</span></span>|<span data-ttu-id="04c1c-224">Giá trị</span><span class="sxs-lookup"><span data-stu-id="04c1c-224">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="04c1c-225">Tên</span><span class="sxs-lookup"><span data-stu-id="04c1c-225">Name</span></span>|<span data-ttu-id="04c1c-226">Nút tài khoản tìm kiếm Contoso</span><span class="sxs-lookup"><span data-stu-id="04c1c-226">Contoso Search Account Button</span></span>|  
   |<span data-ttu-id="04c1c-227">Văn bản nút</span><span class="sxs-lookup"><span data-stu-id="04c1c-227">Button Text</span></span>|<span data-ttu-id="04c1c-228">Tài khoản</span><span class="sxs-lookup"><span data-stu-id="04c1c-228">Account</span></span>|  
   |<span data-ttu-id="04c1c-229">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="04c1c-229">Order</span></span>|<span data-ttu-id="04c1c-230">1</span><span class="sxs-lookup"><span data-stu-id="04c1c-230">1</span></span><br /><br /> <span data-ttu-id="04c1c-231">Trường **Thứ tự** xác định vị trí của nút trên thanh công cụ.</span><span class="sxs-lookup"><span data-stu-id="04c1c-231">The **Order** field defines the position of buttons in the toolbar.</span></span> <span data-ttu-id="04c1c-232">Buttons are arranged from left to right or top to bottom in an ascending order.</span><span class="sxs-lookup"><span data-stu-id="04c1c-232">Buttons are arranged from left to right or top to bottom in an ascending order.</span></span>|  

   <span data-ttu-id="04c1c-233">![Create a tooolbar button for Account submenu](../unified-service-desk/media/crm-itpro-usd-wt03-05.png "Create a tooolbar button for Account submenu")</span><span class="sxs-lookup"><span data-stu-id="04c1c-233">![Create a tooolbar button for Account submenu](../unified-service-desk/media/crm-itpro-usd-wt03-05.png "Create a tooolbar button for Account submenu")</span></span>  

7. <span data-ttu-id="04c1c-234">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-234">Click **Save**.</span></span>  

8. <span data-ttu-id="04c1c-235">You’ll now add two action calls: first to display the account records in the hosted control created in step 1 and the second one on the Contoso Global Manager hosted control to display the account hosted control.</span><span class="sxs-lookup"><span data-stu-id="04c1c-235">You’ll now add two action calls: first to display the account records in the hosted control created in step 1 and the second one on the Contoso Global Manager hosted control to display the account hosted control.</span></span>  

    <span data-ttu-id="04c1c-236">In the **Actions** area, click **+** on the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="04c1c-236">In the **Actions** area, click **+** on the right corner to add an action call.</span></span>  

9. <span data-ttu-id="04c1c-237">In the search box in the **Actions** area, press ENTER or click the search icon.</span><span class="sxs-lookup"><span data-stu-id="04c1c-237">In the search box in the **Actions** area, press ENTER or click the search icon.</span></span>  

10. <span data-ttu-id="04c1c-238">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span><span class="sxs-lookup"><span data-stu-id="04c1c-238">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>  

    <span data-ttu-id="04c1c-239">![Choose New to create an action call](../unified-service-desk/media/crm-itpro-usd-wt03-06.png "Choose New to create an action call")</span><span class="sxs-lookup"><span data-stu-id="04c1c-239">![Choose New to create an action call](../unified-service-desk/media/crm-itpro-usd-wt03-06.png "Choose New to create an action call")</span></span>  

11. <span data-ttu-id="04c1c-240">On the **New Action Call** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="04c1c-240">On the **New Action Call** page, specify the following values:</span></span>  

    |<span data-ttu-id="04c1c-241">Trường</span><span class="sxs-lookup"><span data-stu-id="04c1c-241">Field</span></span>|<span data-ttu-id="04c1c-242">Giá trị</span><span class="sxs-lookup"><span data-stu-id="04c1c-242">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="04c1c-243">Tên</span><span class="sxs-lookup"><span data-stu-id="04c1c-243">Name</span></span>|<span data-ttu-id="04c1c-244">Các cuộc gọi hành động contoso: Tìm tài khoản</span><span class="sxs-lookup"><span data-stu-id="04c1c-244">Contoso Action Call: Search Account</span></span>|  
    |<span data-ttu-id="04c1c-245">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="04c1c-245">Order</span></span>|<span data-ttu-id="04c1c-246">1</span><span class="sxs-lookup"><span data-stu-id="04c1c-246">1</span></span>|  
    |<span data-ttu-id="04c1c-247">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="04c1c-247">Hosted Control</span></span>|<span data-ttu-id="04c1c-248">Contoso Accounts Search</span><span class="sxs-lookup"><span data-stu-id="04c1c-248">Contoso Accounts Search</span></span>|  
    |<span data-ttu-id="04c1c-249">Hành động</span><span class="sxs-lookup"><span data-stu-id="04c1c-249">Action</span></span>|<span data-ttu-id="04c1c-250">Find</span><span class="sxs-lookup"><span data-stu-id="04c1c-250">Find</span></span>|  
    |<span data-ttu-id="04c1c-251">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="04c1c-251">Data</span></span>|<span data-ttu-id="04c1c-252">tài khoản</span><span class="sxs-lookup"><span data-stu-id="04c1c-252">account</span></span>|  

    <span data-ttu-id="04c1c-253">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-07.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="04c1c-253">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-07.png "Create an action call in Unified Service Desk")</span></span>  

12. <span data-ttu-id="04c1c-254">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-254">Click **Save**.</span></span> <span data-ttu-id="04c1c-255">The new action call gets added to the **Contoso Search Account Button** button.</span><span class="sxs-lookup"><span data-stu-id="04c1c-255">The new action call gets added to the **Contoso Search Account Button** button.</span></span>  

13. <span data-ttu-id="04c1c-256">You’ll add another action call to the button to set the focus on the hosted control that displays the account records in the client application.</span><span class="sxs-lookup"><span data-stu-id="04c1c-256">You’ll add another action call to the button to set the focus on the hosted control that displays the account records in the client application.</span></span> <span data-ttu-id="04c1c-257">In the **Actions** area, click **+** on the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="04c1c-257">In the **Actions** area, click **+** on the right corner to add an action call.</span></span>  

14. <span data-ttu-id="04c1c-258">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span><span class="sxs-lookup"><span data-stu-id="04c1c-258">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>  

15. <span data-ttu-id="04c1c-259">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="04c1c-259">On the **New Action Call** page, specify the following values.</span></span>  

    |<span data-ttu-id="04c1c-260">Trường</span><span class="sxs-lookup"><span data-stu-id="04c1c-260">Field</span></span>|<span data-ttu-id="04c1c-261">Giá trị</span><span class="sxs-lookup"><span data-stu-id="04c1c-261">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="04c1c-262">Tên</span><span class="sxs-lookup"><span data-stu-id="04c1c-262">Name</span></span>|<span data-ttu-id="04c1c-263">Cuộc gọi hành động contoso: Hiển thị tìm kiếm tài khoản</span><span class="sxs-lookup"><span data-stu-id="04c1c-263">Contoso Action Call: Display Account Search</span></span>|  
    |<span data-ttu-id="04c1c-264">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="04c1c-264">Order</span></span>|<span data-ttu-id="04c1c-265">2</span><span class="sxs-lookup"><span data-stu-id="04c1c-265">2</span></span>|  
    |<span data-ttu-id="04c1c-266">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="04c1c-266">Hosted Control</span></span>|<span data-ttu-id="04c1c-267">Contoso Global Manager</span><span class="sxs-lookup"><span data-stu-id="04c1c-267">Contoso Global Manager</span></span>|  
    |<span data-ttu-id="04c1c-268">Hành động</span><span class="sxs-lookup"><span data-stu-id="04c1c-268">Action</span></span>|<span data-ttu-id="04c1c-269">Hiển thị tab</span><span class="sxs-lookup"><span data-stu-id="04c1c-269">ShowTab</span></span>|  
    |<span data-ttu-id="04c1c-270">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="04c1c-270">Data</span></span>|<span data-ttu-id="04c1c-271">Contoso Accounts Search</span><span class="sxs-lookup"><span data-stu-id="04c1c-271">Contoso Accounts Search</span></span>|  

    <span data-ttu-id="04c1c-272">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-08.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="04c1c-272">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-08.png "Create an action call in Unified Service Desk")</span></span>  

16. <span data-ttu-id="04c1c-273">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-273">Click **Save**.</span></span> <span data-ttu-id="04c1c-274">The new action call gets added to the **Contoso Search Account Button** button.</span><span class="sxs-lookup"><span data-stu-id="04c1c-274">The new action call gets added to the **Contoso Search Account Button** button.</span></span>  

17. <span data-ttu-id="04c1c-275">Điều hướng đến nút thanh công cụ **Nút tìm kiếm Contoso** để thêm nút phụ để tìm kiếm và hiển thị liên hệ.</span><span class="sxs-lookup"><span data-stu-id="04c1c-275">Navigate to **Contoso Search Button** toolbar button to add a child button for searching and displaying contacts.</span></span> <span data-ttu-id="04c1c-276">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Nút tìm kiếm Contoso** và chọn **Nút thanh công cụ**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-276">On the nav bar, click the down arrow next to **Contoso Search Button**, and select **Toolbar Buttons**.</span></span>  

18. <span data-ttu-id="04c1c-277">Trên trang tiếp theo, bấm vào **thêm nút thanh công cụ mới**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-277">On the next page, click **Add New Toolbar Button**.</span></span>  

19. <span data-ttu-id="04c1c-278">Trên trang **Nút thanh công cụ mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="04c1c-278">On the **New Toolbar Button** page, specify the following values:</span></span>  

    |<span data-ttu-id="04c1c-279">Trường</span><span class="sxs-lookup"><span data-stu-id="04c1c-279">Field</span></span>|<span data-ttu-id="04c1c-280">Giá trị</span><span class="sxs-lookup"><span data-stu-id="04c1c-280">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="04c1c-281">Tên</span><span class="sxs-lookup"><span data-stu-id="04c1c-281">Name</span></span>|<span data-ttu-id="04c1c-282">Nút Liên hệ tìm kiếm Contoso</span><span class="sxs-lookup"><span data-stu-id="04c1c-282">Contoso Search Contact Button</span></span>|  
    |<span data-ttu-id="04c1c-283">Văn bản nút</span><span class="sxs-lookup"><span data-stu-id="04c1c-283">Button Text</span></span>|<span data-ttu-id="04c1c-284">Người liên hệ</span><span class="sxs-lookup"><span data-stu-id="04c1c-284">Contact</span></span>|  
    |<span data-ttu-id="04c1c-285">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="04c1c-285">Order</span></span>|<span data-ttu-id="04c1c-286">2</span><span class="sxs-lookup"><span data-stu-id="04c1c-286">2</span></span><br /><br /> <span data-ttu-id="04c1c-287">Trường **Thứ tự** xác định vị trí của nút trên thanh công cụ.</span><span class="sxs-lookup"><span data-stu-id="04c1c-287">The **Order** field defines the position of buttons in the toolbar.</span></span> <span data-ttu-id="04c1c-288">Buttons are arranged from left to right or top to bottom in an ascending order.</span><span class="sxs-lookup"><span data-stu-id="04c1c-288">Buttons are arranged from left to right or top to bottom in an ascending order.</span></span>|  

    <span data-ttu-id="04c1c-289">![Create a toolbar button for contacts search](../unified-service-desk/media/crm-itpro-usd-wt03-09.png "Create a toolbar button for contacts search")</span><span class="sxs-lookup"><span data-stu-id="04c1c-289">![Create a toolbar button for contacts search](../unified-service-desk/media/crm-itpro-usd-wt03-09.png "Create a toolbar button for contacts search")</span></span>  

20. <span data-ttu-id="04c1c-290">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-290">Click **Save**.</span></span>  

21. <span data-ttu-id="04c1c-291">You’ll now add two action calls: first to display the contact records in the hosted control that were created in step 1 and the second one on the Contoso Global Manager hosted control to display the contacts hosted control.</span><span class="sxs-lookup"><span data-stu-id="04c1c-291">You’ll now add two action calls: first to display the contact records in the hosted control that were created in step 1 and the second one on the Contoso Global Manager hosted control to display the contacts hosted control.</span></span>  

     <span data-ttu-id="04c1c-292">In the **Actions** area, click **+** on the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="04c1c-292">In the **Actions** area, click **+** on the right corner to add an action call.</span></span>  

22. <span data-ttu-id="04c1c-293">In the search box in the **Actions** area, press ENTER or click the search icon.</span><span class="sxs-lookup"><span data-stu-id="04c1c-293">In the search box in the **Actions** area, press ENTER or click the search icon.</span></span>  

23. <span data-ttu-id="04c1c-294">Trong hộp tìm kiếm kết quả, bấm vào **Mới** ở góc dưới bên phải để tạo ra cuộc gọi hành động cho nút thanh công cụ này.</span><span class="sxs-lookup"><span data-stu-id="04c1c-294">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>  

24. <span data-ttu-id="04c1c-295">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="04c1c-295">On the **New Action Call** page, specify the following values:</span></span>  

    |<span data-ttu-id="04c1c-296">Trường</span><span class="sxs-lookup"><span data-stu-id="04c1c-296">Field</span></span>|<span data-ttu-id="04c1c-297">Giá trị</span><span class="sxs-lookup"><span data-stu-id="04c1c-297">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="04c1c-298">Tên</span><span class="sxs-lookup"><span data-stu-id="04c1c-298">Name</span></span>|<span data-ttu-id="04c1c-299">Các cuộc gọi hành động contoso: Tìm liên hệ</span><span class="sxs-lookup"><span data-stu-id="04c1c-299">Contoso Action Call: Search Contact</span></span>|  
    |<span data-ttu-id="04c1c-300">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="04c1c-300">Order</span></span>|<span data-ttu-id="04c1c-301">1</span><span class="sxs-lookup"><span data-stu-id="04c1c-301">1</span></span>|  
    |<span data-ttu-id="04c1c-302">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="04c1c-302">Hosted Control</span></span>|<span data-ttu-id="04c1c-303">Contoso Contacts Search</span><span class="sxs-lookup"><span data-stu-id="04c1c-303">Contoso Contacts Search</span></span>|  
    |<span data-ttu-id="04c1c-304">Hành động</span><span class="sxs-lookup"><span data-stu-id="04c1c-304">Action</span></span>|<span data-ttu-id="04c1c-305">Find</span><span class="sxs-lookup"><span data-stu-id="04c1c-305">Find</span></span>|  
    |<span data-ttu-id="04c1c-306">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="04c1c-306">Data</span></span>|<span data-ttu-id="04c1c-307">người liên hệ</span><span class="sxs-lookup"><span data-stu-id="04c1c-307">contact</span></span>|  

    <span data-ttu-id="04c1c-308">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-10.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="04c1c-308">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-10.png "Create an action call in Unified Service Desk")</span></span>  

25. <span data-ttu-id="04c1c-309">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-309">Click **Save**.</span></span> <span data-ttu-id="04c1c-310">The new action call gets added to the **Contoso Search Contact Button** toolbar button.</span><span class="sxs-lookup"><span data-stu-id="04c1c-310">The new action call gets added to the **Contoso Search Contact Button** toolbar button.</span></span>  

26. <span data-ttu-id="04c1c-311">You’ll add another action call to the button to set the focus on the hosted control that displays the contact records in the client application.</span><span class="sxs-lookup"><span data-stu-id="04c1c-311">You’ll add another action call to the button to set the focus on the hosted control that displays the contact records in the client application.</span></span> <span data-ttu-id="04c1c-312">In the **Actions** area, click **+** on the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="04c1c-312">In the **Actions** area, click **+** on the right corner to add an action call.</span></span>  

27. <span data-ttu-id="04c1c-313">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span><span class="sxs-lookup"><span data-stu-id="04c1c-313">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>  

28. <span data-ttu-id="04c1c-314">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="04c1c-314">On the **New Action Call** page, specify the following values.</span></span>  

    |<span data-ttu-id="04c1c-315">Trường</span><span class="sxs-lookup"><span data-stu-id="04c1c-315">Field</span></span>|<span data-ttu-id="04c1c-316">Giá trị</span><span class="sxs-lookup"><span data-stu-id="04c1c-316">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="04c1c-317">Tên</span><span class="sxs-lookup"><span data-stu-id="04c1c-317">Name</span></span>|<span data-ttu-id="04c1c-318">Cuộc gọi hành động contoso: Hiển thị tìm kiếm liên hệ</span><span class="sxs-lookup"><span data-stu-id="04c1c-318">Contoso Action Call: Display Contact Search</span></span>|  
    |<span data-ttu-id="04c1c-319">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="04c1c-319">Order</span></span>|<span data-ttu-id="04c1c-320">2</span><span class="sxs-lookup"><span data-stu-id="04c1c-320">2</span></span>|  
    |<span data-ttu-id="04c1c-321">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="04c1c-321">Hosted Control</span></span>|<span data-ttu-id="04c1c-322">Contoso Global Manager</span><span class="sxs-lookup"><span data-stu-id="04c1c-322">Contoso Global Manager</span></span>|  
    |<span data-ttu-id="04c1c-323">Hành động</span><span class="sxs-lookup"><span data-stu-id="04c1c-323">Action</span></span>|<span data-ttu-id="04c1c-324">Hiển thị tab</span><span class="sxs-lookup"><span data-stu-id="04c1c-324">ShowTab</span></span>|  
    |<span data-ttu-id="04c1c-325">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="04c1c-325">Data</span></span>|<span data-ttu-id="04c1c-326">Contoso Contacts Search</span><span class="sxs-lookup"><span data-stu-id="04c1c-326">Contoso Contacts Search</span></span>|  

    <span data-ttu-id="04c1c-327">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-11.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="04c1c-327">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-11.png "Create an action call in Unified Service Desk")</span></span>  

29. <span data-ttu-id="04c1c-328">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-328">Click **Save**.</span></span> <span data-ttu-id="04c1c-329">The new action call gets added to the **Contoso Search Contact Button** toolbar button.</span><span class="sxs-lookup"><span data-stu-id="04c1c-329">The new action call gets added to the **Contoso Search Contact Button** toolbar button.</span></span>  

<a name="Step5"></a>   
## <a name="step-5-add-the-controls-to-the-configuration"></a><span data-ttu-id="04c1c-330">Bước 5: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="04c1c-330">Step 5: Add the controls to the configuration</span></span>  
 <span data-ttu-id="04c1c-331">In this step, you’ll add the action calls, hosted controls, and toolbar that were created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span><span class="sxs-lookup"><span data-stu-id="04c1c-331">In this step, you’ll add the action calls, hosted controls, and toolbar that were created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span></span> <span data-ttu-id="04c1c-332">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="04c1c-332">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span></span>  

 <span data-ttu-id="04c1c-333">Add the following to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-333">Add the following to **Contoso Configuration**.</span></span>  

|<span data-ttu-id="04c1c-334">Tên kiểm soát</span><span class="sxs-lookup"><span data-stu-id="04c1c-334">Control name</span></span>|<span data-ttu-id="04c1c-335">Loại kiểm soát</span><span class="sxs-lookup"><span data-stu-id="04c1c-335">Control type</span></span>|  
|------------------|------------------|  
|<span data-ttu-id="04c1c-336">Các cuộc gọi hành động contoso: Tìm tài khoản</span><span class="sxs-lookup"><span data-stu-id="04c1c-336">Contoso Action Call: Search Account</span></span>|<span data-ttu-id="04c1c-337">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="04c1c-337">Action Call</span></span>|  
|<span data-ttu-id="04c1c-338">Cuộc gọi hành động contoso: Hiển thị tìm kiếm tài khoản</span><span class="sxs-lookup"><span data-stu-id="04c1c-338">Contoso Action Call: Display Account Search</span></span>|<span data-ttu-id="04c1c-339">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="04c1c-339">Action Call</span></span>|  
|<span data-ttu-id="04c1c-340">Các cuộc gọi hành động contoso: Tìm liên hệ</span><span class="sxs-lookup"><span data-stu-id="04c1c-340">Contoso Action Call: Search Contact</span></span>|<span data-ttu-id="04c1c-341">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="04c1c-341">Action Call</span></span>|  
|<span data-ttu-id="04c1c-342">Cuộc gọi hành động contoso: Hiển thị tìm kiếm liên hệ</span><span class="sxs-lookup"><span data-stu-id="04c1c-342">Contoso Action Call: Display Contact Search</span></span>|<span data-ttu-id="04c1c-343">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="04c1c-343">Action Call</span></span>|  
|<span data-ttu-id="04c1c-344">Tìm kiếm tài khoản Contoso</span><span class="sxs-lookup"><span data-stu-id="04c1c-344">Contoso Accounts Search</span></span>|<span data-ttu-id="04c1c-345">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="04c1c-345">Hosted Control</span></span>|  
|<span data-ttu-id="04c1c-346">Tìm kiếm liên hệ Contoso</span><span class="sxs-lookup"><span data-stu-id="04c1c-346">Contoso Contacts Search</span></span>|<span data-ttu-id="04c1c-347">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="04c1c-347">Hosted Control</span></span>|  
|<span data-ttu-id="04c1c-348">Bộ chứa thanh công cụ chính Contoso</span><span class="sxs-lookup"><span data-stu-id="04c1c-348">Contoso Main Toolbar Container</span></span>|<span data-ttu-id="04c1c-349">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="04c1c-349">Hosted Control</span></span>|  
|<span data-ttu-id="04c1c-350">Contoso Main Toolbar</span><span class="sxs-lookup"><span data-stu-id="04c1c-350">Contoso Main Toolbar</span></span>|<span data-ttu-id="04c1c-351">Thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="04c1c-351">Toolbar</span></span>|  

 <span data-ttu-id="04c1c-352">To add a control to the configuration:</span><span class="sxs-lookup"><span data-stu-id="04c1c-352">To add a control to the configuration:</span></span>  

1. <span data-ttu-id="04c1c-353">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="04c1c-353">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="04c1c-354">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-354">Click **Configuration**.</span></span>  

4. <span data-ttu-id="04c1c-355">Click **Contoso Configuration** to open the definition.</span><span class="sxs-lookup"><span data-stu-id="04c1c-355">Click **Contoso Configuration** to open the definition.</span></span>  

5. <span data-ttu-id="04c1c-356">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-356">On the nav bar, click the down arrow next to **Contoso Configuration**, and select **Action Calls**.</span></span>  

6. <span data-ttu-id="04c1c-357">Trên trang tiếp theo, bấm vào **Thêm Cuộc gọi Hành động Hiện có**, nhập “`Contoso Action Call`” vào thanh tìm kiếm, sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="04c1c-357">On the next page, click **Add Existing Action Call**, type “`Contoso Action Call`” in the search bar, and then press ENTER or click the search icon.</span></span>  

7. <span data-ttu-id="04c1c-358">Các cuộc gọi hành động được liệt kê trước đó được hiển thị trong kết quả tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="04c1c-358">The action calls listed earlier are displayed in the search results.</span></span> <span data-ttu-id="04c1c-359">Thêm các cuộc gọi hành động này.</span><span class="sxs-lookup"><span data-stu-id="04c1c-359">Add these action calls.</span></span>  

8. <span data-ttu-id="04c1c-360">Tương tự, thêm kiểm soát tổ chức và thanh công cụ bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Kiểm soát tổ chức** và **thanh công cụ** lần lượt.</span><span class="sxs-lookup"><span data-stu-id="04c1c-360">Similarly, add the hosted controls and the toolbar by clicking the down arrow next to **Contoso Configuration**, and clicking **Hosted Controls** and **Toolbars** respectively.</span></span>  

9. <span data-ttu-id="04c1c-361">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="04c1c-361">Click **Save**.</span></span>  

<a name="Step6"></a>   
## <a name="step-6-test-the-application"></a><span data-ttu-id="04c1c-362">Step 6: Test the application</span><span class="sxs-lookup"><span data-stu-id="04c1c-362">Step 6: Test the application</span></span>  
 <span data-ttu-id="04c1c-363">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="04c1c-363">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span></span> <span data-ttu-id="04c1c-364">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span><span class="sxs-lookup"><span data-stu-id="04c1c-364">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span></span>  

 <span data-ttu-id="04c1c-365">Your agent application will now have a **SEARCH** button in the toolbar area with two child buttons (**Account** and **Contact**) that are displayed on clicking the down arrow.</span><span class="sxs-lookup"><span data-stu-id="04c1c-365">Your agent application will now have a **SEARCH** button in the toolbar area with two child buttons (**Account** and **Contact**) that are displayed on clicking the down arrow.</span></span>  

 <span data-ttu-id="04c1c-366">![Display account and contact records](../unified-service-desk/media/crm-itpro-usd-wt03-12.png "Display account and contact records")</span><span class="sxs-lookup"><span data-stu-id="04c1c-366">![Display account and contact records](../unified-service-desk/media/crm-itpro-usd-wt03-12.png "Display account and contact records")</span></span>  

 <span data-ttu-id="04c1c-367">Click **Account** or **Contact** under the **SEARCH** button to display the respective records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance in separate tabs in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.</span><span class="sxs-lookup"><span data-stu-id="04c1c-367">Click **Account** or **Contact** under the **SEARCH** button to display the respective records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance in separate tabs in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.</span></span>  

 <span data-ttu-id="04c1c-368">![Dynamics 365 for Customer Engagement apps contact records displayed](../unified-service-desk/media/crm-itpro-usd-wt03-13-unified-interface.png "Dynamics 365 for Customer Engagement apps contact records displayed")</span><span class="sxs-lookup"><span data-stu-id="04c1c-368">![Dynamics 365 for Customer Engagement apps contact records displayed](../unified-service-desk/media/crm-itpro-usd-wt03-13-unified-interface.png "Dynamics 365 for Customer Engagement apps contact records displayed")</span></span>  

<a name="Conclusion"></a>   
## <a name="conclusion"></a><span data-ttu-id="04c1c-369">Kết luận</span><span class="sxs-lookup"><span data-stu-id="04c1c-369">Conclusion</span></span>  
 <span data-ttu-id="04c1c-370">In this walkthrough, you learned how to display [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records from Unified Interface Apps in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.</span><span class="sxs-lookup"><span data-stu-id="04c1c-370">In this walkthrough, you learned how to display [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records from Unified Interface Apps in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.</span></span> <span data-ttu-id="04c1c-371">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span><span class="sxs-lookup"><span data-stu-id="04c1c-371">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span></span>

### <a name="see-also"></a><span data-ttu-id="04c1c-372">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="04c1c-372">See also</span></span>
 [<span data-ttu-id="04c1c-373">Support for Unified Interface Apps in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="04c1c-373">Support for Unified Interface Apps in Unified Service Desk</span></span>](../unified-service-desk/admin/Support-unified-interfaces-apps-usd.md)

 [<span data-ttu-id="04c1c-374">Unified Interface Page (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="04c1c-374">Unified Interface Page (Hosted Control)</span></span>](../unified-service-desk/unified-interface-page-hosted-control.md)

 [<span data-ttu-id="04c1c-375">Unified Service Desk and Unified Interface Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="04c1c-375">Unified Service Desk and Unified Interface Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md)

 [<span data-ttu-id="04c1c-376">Walkthrough 1: Build a simple agent application for Unified Interface Apps</span><span class="sxs-lookup"><span data-stu-id="04c1c-376">Walkthrough 1: Build a simple agent application for Unified Interface Apps</span></span>](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)   

 [<span data-ttu-id="04c1c-377">Walkthrough 2: Display an external webpage in your agent application</span><span class="sxs-lookup"><span data-stu-id="04c1c-377">Walkthrough 2: Display an external webpage in your agent application</span></span>](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md)
 
 [<span data-ttu-id="04c1c-378">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application</span><span class="sxs-lookup"><span data-stu-id="04c1c-378">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application</span></span>](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md)   

 [<span data-ttu-id="04c1c-379">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span><span class="sxs-lookup"><span data-stu-id="04c1c-379">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span></span>](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md) 

 [<span data-ttu-id="04c1c-380">Walkthrough 6: Configure the Debugger hosted control in your agent application</span><span class="sxs-lookup"><span data-stu-id="04c1c-380">Walkthrough 6: Configure the Debugger hosted control in your agent application</span></span>](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md)

 [<span data-ttu-id="04c1c-381">Walkthrough 7: Configure agent scripting in your agent application</span><span class="sxs-lookup"><span data-stu-id="04c1c-381">Walkthrough 7: Configure agent scripting in your agent application</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)
