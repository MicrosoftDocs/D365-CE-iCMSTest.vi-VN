---
title: 'Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application | MicrosoftDocs'
description: Demonstrates how to display Customer Engagement records in Unified Service Desk.
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
ms.assetid: 0affe8ba-fddc-4ded-b733-735833209b53
caps.latest.revision: 8
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: f1004646ac10778a280d9c8359bc99d16159be98
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385996"
---
# <a name="walkthrough-3-display-microsoft-dynamics-365-for-customer-engagement-apps-records-in-your-agent-application"></a><span data-ttu-id="b5f5a-103">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application</span><span class="sxs-lookup"><span data-stu-id="b5f5a-103">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application</span></span>
<span data-ttu-id="b5f5a-104">This walkthrough demonstrates how to display [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps records in your agent application.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-104">This walkthrough demonstrates how to display [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps records in your agent application.</span></span> <span data-ttu-id="b5f5a-105">In this walkthrough, you’ll display all the account and contact records in the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-105">In this walkthrough, you’ll display all the account and contact records in the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span> <span data-ttu-id="b5f5a-106">Bạn cũng sẽ tạo ra nút tìm kiếm với các mục trình đơn thả xuống để hiển thị tài khoản và địa chỉ liên lạc trong ứng dụng tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-106">You’ll also create a search button with drop-down menu items for displaying accounts and contacts in the agent application.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="b5f5a-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="b5f5a-107">Prerequisites</span></span>  

- <span data-ttu-id="b5f5a-108">You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="b5f5a-108">You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span> <span data-ttu-id="b5f5a-109">Các cấu hình mà bạn hoàn thành trong cách 1 được yêu cầu trong cách này.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-109">The configurations that you completed in walkthrough 1 are required in this walkthrough.</span></span>  

- <span data-ttu-id="b5f5a-110">Cách này giả định rằng bạn sẽ đang sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên ở cuối cách này để kiểm tra ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-110">This walkthrough assumes that you will be using the same user credential that you used in walkthrough 1 to sign in to the agent application at the end of the walkthrough to test the application.</span></span> <span data-ttu-id="b5f5a-111">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-111">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="b5f5a-112">[Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)</span><span class="sxs-lookup"><span data-stu-id="b5f5a-112">[Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)</span></span>  

- <span data-ttu-id="b5f5a-113">You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-113">You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  

  - <span data-ttu-id="b5f5a-114">Hai loại kiểm soát tổ chức sau: Trang CRM và bộ chứa thanh công cụ.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-114">The following two types of hosted controls: CRM Page and Toolbar Container.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="b5f5a-115">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span><span class="sxs-lookup"><span data-stu-id="b5f5a-115">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span></span>  

  - <span data-ttu-id="b5f5a-116">Action call and how to configure it.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-116">Action call and how to configure it.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="b5f5a-117">[Action calls](../unified-service-desk/action-calls.md)</span><span class="sxs-lookup"><span data-stu-id="b5f5a-117">[Action calls](../unified-service-desk/action-calls.md)</span></span>  

  - <span data-ttu-id="b5f5a-118">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-118">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="b5f5a-119">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="b5f5a-119">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span></span>  

<a name="Top"></a>   
## <a name="in-this-walkthrough"></a><span data-ttu-id="b5f5a-120">In This Walkthrough</span><span class="sxs-lookup"><span data-stu-id="b5f5a-120">In This Walkthrough</span></span>  
 [<span data-ttu-id="b5f5a-121">Bước 1: Tạo loại trang CRM của kiểm soát tổ chức để hiển thị hồ sơ tài khoản và liên hệ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-121">Step 1: Create CRM Page type of hosted controls to display account and contact records</span></span>](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step1)  

 [<span data-ttu-id="b5f5a-122">Bước 2: Tạo loại bộ chứa công cụ của kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="b5f5a-122">Step 2: Create a toolbar container type of hosted control</span></span>](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step2)  

 [<span data-ttu-id="b5f5a-123">Bước 3: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-123">Step 3: Add a toolbar and attach it to the toolbar container</span></span>](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step3)  

 [<span data-ttu-id="b5f5a-124">Step 4: Add toolbar buttons and action calls to display Dynamics 365 for Customer Engagement apps records</span><span class="sxs-lookup"><span data-stu-id="b5f5a-124">Step 4: Add toolbar buttons and action calls to display Dynamics 365 for Customer Engagement apps records</span></span>](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step4)  

 [<span data-ttu-id="b5f5a-125">Bước 5: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="b5f5a-125">Step 5: Add the controls to the configuration</span></span>](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step5)  

 [<span data-ttu-id="b5f5a-126">Bước 6: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="b5f5a-126">Step 6: Test the application</span></span>](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md#Step6)  

 [<span data-ttu-id="b5f5a-127">Kết luận</span><span class="sxs-lookup"><span data-stu-id="b5f5a-127">Conclusion</span></span>](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md#Conclusion)  

<a name="Step1"></a>   
## <a name="step-1-create-crm-page-type-of-hosted-controls-to-display-account-and-contact-records"></a><span data-ttu-id="b5f5a-128">Bước 1: Tạo loại trang CRM của kiểm soát tổ chức để hiển thị hồ sơ tài khoản và liên hệ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-128">Step 1: Create CRM Page type of hosted controls to display account and contact records</span></span>  
 <span data-ttu-id="b5f5a-129">In this step, you’ll create two hosted controls of **[!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps Page** type to display the account and contact records respectively.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-129">In this step, you’ll create two hosted controls of **[!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps Page** type to display the account and contact records respectively.</span></span>  

1. <span data-ttu-id="b5f5a-130">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-130">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="b5f5a-131">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-131">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="b5f5a-132">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-132">Click **New**.</span></span>  

5. <span data-ttu-id="b5f5a-133">On the **New Hosted Control** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-133">On the **New Hosted Control** page, specify the following values:</span></span>  

   |<span data-ttu-id="b5f5a-134">Trường</span><span class="sxs-lookup"><span data-stu-id="b5f5a-134">Field</span></span>|<span data-ttu-id="b5f5a-135">Giá trị</span><span class="sxs-lookup"><span data-stu-id="b5f5a-135">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="b5f5a-136">Tên</span><span class="sxs-lookup"><span data-stu-id="b5f5a-136">Name</span></span>|<span data-ttu-id="b5f5a-137">Tìm kiếm tài khoản Contoso</span><span class="sxs-lookup"><span data-stu-id="b5f5a-137">Contoso Accounts Search</span></span>|  
   |<span data-ttu-id="b5f5a-138">Tên hiển thị</span><span class="sxs-lookup"><span data-stu-id="b5f5a-138">Display Name</span></span>|<span data-ttu-id="b5f5a-139">Contoso: Tài khoản</span><span class="sxs-lookup"><span data-stu-id="b5f5a-139">Contoso: Accounts</span></span>|  
   |<span data-ttu-id="b5f5a-140">Loại Thành phần USD</span><span class="sxs-lookup"><span data-stu-id="b5f5a-140">USD Component Type</span></span>|<span data-ttu-id="b5f5a-141">Trang CRM</span><span class="sxs-lookup"><span data-stu-id="b5f5a-141">CRM Page</span></span>|  
   |<span data-ttu-id="b5f5a-142">Cho phép nhiều trang</span><span class="sxs-lookup"><span data-stu-id="b5f5a-142">Allow Multiple Pages</span></span>|<span data-ttu-id="b5f5a-143">No</span><span class="sxs-lookup"><span data-stu-id="b5f5a-143">No</span></span>|  
   |<span data-ttu-id="b5f5a-144">Loại tổ chức</span><span class="sxs-lookup"><span data-stu-id="b5f5a-144">Hosting Type</span></span>|<span data-ttu-id="b5f5a-145">WPF nội bộ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-145">Internal WPF</span></span>|  
   |<span data-ttu-id="b5f5a-146">Application is Global</span><span class="sxs-lookup"><span data-stu-id="b5f5a-146">Application is Global</span></span>|<span data-ttu-id="b5f5a-147">Đã kiểm tra</span><span class="sxs-lookup"><span data-stu-id="b5f5a-147">Checked</span></span>|  
   |<span data-ttu-id="b5f5a-148">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="b5f5a-148">Display Group</span></span>|<span data-ttu-id="b5f5a-149">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="b5f5a-149">MainPanel</span></span>|  

   <span data-ttu-id="b5f5a-150">![Create a hosted control for displaying accounts](../unified-service-desk/media/crm-itpro-usd-wt03-01.png "Create a hosted control for displaying accounts")</span><span class="sxs-lookup"><span data-stu-id="b5f5a-150">![Create a hosted control for displaying accounts](../unified-service-desk/media/crm-itpro-usd-wt03-01.png "Create a hosted control for displaying accounts")</span></span>  

6. <span data-ttu-id="b5f5a-151">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-151">Click **Save**.</span></span>  

7. <span data-ttu-id="b5f5a-152">Bấm vào **Mới** để tạo ra kiểm soát tổ chức khác để hiển thị hồ sơ liên lạc.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-152">Click **New** to create another hosted control for displaying contact records.</span></span>  

8. <span data-ttu-id="b5f5a-153">Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-153">On the **New Hosted Control** page, specify the following values:</span></span>  

   |<span data-ttu-id="b5f5a-154">Trường</span><span class="sxs-lookup"><span data-stu-id="b5f5a-154">Field</span></span>|<span data-ttu-id="b5f5a-155">Giá trị</span><span class="sxs-lookup"><span data-stu-id="b5f5a-155">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="b5f5a-156">Tên</span><span class="sxs-lookup"><span data-stu-id="b5f5a-156">Name</span></span>|<span data-ttu-id="b5f5a-157">Tìm kiếm liên hệ Contoso</span><span class="sxs-lookup"><span data-stu-id="b5f5a-157">Contoso Contacts Search</span></span>|  
   |<span data-ttu-id="b5f5a-158">Tên hiển thị</span><span class="sxs-lookup"><span data-stu-id="b5f5a-158">Display Name</span></span>|<span data-ttu-id="b5f5a-159">Contoso: Liên hệ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-159">Contoso: Contacts</span></span>|  
   |<span data-ttu-id="b5f5a-160">Loại Thành phần USD</span><span class="sxs-lookup"><span data-stu-id="b5f5a-160">USD Component Type</span></span>|<span data-ttu-id="b5f5a-161">Trang CRM</span><span class="sxs-lookup"><span data-stu-id="b5f5a-161">CRM Page</span></span>|  
   |<span data-ttu-id="b5f5a-162">Cho phép nhiều trang</span><span class="sxs-lookup"><span data-stu-id="b5f5a-162">Allow Multiple Pages</span></span>|<span data-ttu-id="b5f5a-163">No</span><span class="sxs-lookup"><span data-stu-id="b5f5a-163">No</span></span>|  
   |<span data-ttu-id="b5f5a-164">Loại tổ chức</span><span class="sxs-lookup"><span data-stu-id="b5f5a-164">Hosting Type</span></span>|<span data-ttu-id="b5f5a-165">WPF nội bộ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-165">Internal WPF</span></span>|  
   |<span data-ttu-id="b5f5a-166">Application is Global</span><span class="sxs-lookup"><span data-stu-id="b5f5a-166">Application is Global</span></span>|<span data-ttu-id="b5f5a-167">Đã kiểm tra</span><span class="sxs-lookup"><span data-stu-id="b5f5a-167">Checked</span></span>|  
   |<span data-ttu-id="b5f5a-168">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="b5f5a-168">Display Group</span></span>|<span data-ttu-id="b5f5a-169">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="b5f5a-169">MainPanel</span></span>|  

   <span data-ttu-id="b5f5a-170">![Create hosted control for displaying contacts](../unified-service-desk/media/crm-itpro-usd-wt03-02.png "Create hosted control for displaying contacts")</span><span class="sxs-lookup"><span data-stu-id="b5f5a-170">![Create hosted control for displaying contacts](../unified-service-desk/media/crm-itpro-usd-wt03-02.png "Create hosted control for displaying contacts")</span></span>  

9. <span data-ttu-id="b5f5a-171">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-171">Click **Save**.</span></span>  

<a name="Step2"></a>   
## <a name="step-2-create-a-toolbar-container-type-of-hosted-control"></a><span data-ttu-id="b5f5a-172">Bước 2: Tạo loại bộ chứa công cụ của kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="b5f5a-172">Step 2: Create a toolbar container type of hosted control</span></span>  
 <span data-ttu-id="b5f5a-173">Loại bộ chứa thanh công cụ của kiểm soát tổ chức được sử dụng để giữ và hiển thị thanh công cụ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="b5f5a-173">Toolbar Container type of hosted controls are used to hold and display the toolbars in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="b5f5a-174">In this section, you’ll create a **Toolbar Container** hosted control that will appear at the top of the client application.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-174">In this section, you’ll create a **Toolbar Container** hosted control that will appear at the top of the client application.</span></span>  

1. <span data-ttu-id="b5f5a-175">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-175">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="b5f5a-176">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-176">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="b5f5a-177">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-177">Click **New**.</span></span>  

5. <span data-ttu-id="b5f5a-178">On the **New Hosted Control** page, specify the following values</span><span class="sxs-lookup"><span data-stu-id="b5f5a-178">On the **New Hosted Control** page, specify the following values</span></span>  

   |<span data-ttu-id="b5f5a-179">Trường</span><span class="sxs-lookup"><span data-stu-id="b5f5a-179">Field</span></span>|<span data-ttu-id="b5f5a-180">Giá trị</span><span class="sxs-lookup"><span data-stu-id="b5f5a-180">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="b5f5a-181">Tên</span><span class="sxs-lookup"><span data-stu-id="b5f5a-181">Name</span></span>|<span data-ttu-id="b5f5a-182">Bộ chứa thanh công cụ chính Contoso</span><span class="sxs-lookup"><span data-stu-id="b5f5a-182">Contoso Main Toolbar Container</span></span>|  
   |<span data-ttu-id="b5f5a-183">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="b5f5a-183">USD Component Type</span></span>|<span data-ttu-id="b5f5a-184">Bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-184">Toolbar Container</span></span>|  
   |<span data-ttu-id="b5f5a-185">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="b5f5a-185">Display Group</span></span>|<span data-ttu-id="b5f5a-186">Bàng điều khiển thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-186">ToolbarPanel</span></span>|  

   <span data-ttu-id="b5f5a-187">![Toolbar Container hosted control](../unified-service-desk/media/crm-itpro-usd-wt03-03.png "Toolbar Container hosted control")</span><span class="sxs-lookup"><span data-stu-id="b5f5a-187">![Toolbar Container hosted control](../unified-service-desk/media/crm-itpro-usd-wt03-03.png "Toolbar Container hosted control")</span></span>  

6. <span data-ttu-id="b5f5a-188">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-188">Click **Save**.</span></span>  

<a name="Step3"></a>   
## <a name="step-3-add-a-toolbar-and-attach-it-to-the-toolbar-container"></a><span data-ttu-id="b5f5a-189">Bước 3: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-189">Step 3: Add a toolbar and attach it to the toolbar container</span></span>  
 <span data-ttu-id="b5f5a-190">In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 2.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-190">In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 2.</span></span> <span data-ttu-id="b5f5a-191">This is done to display the toolbar in your agent application.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-191">This is done to display the toolbar in your agent application.</span></span>  

1. <span data-ttu-id="b5f5a-192">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-192">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="b5f5a-193">Bấm vào **Thanh công cụ**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-193">Click **Toolbars**.</span></span>  

4. <span data-ttu-id="b5f5a-194">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-194">Click **New**.</span></span>  

5. <span data-ttu-id="b5f5a-195">Trên trang **thanh công cụ mới**, nhập **Thanh công cụ chính Contoso** trong hộp **tên**, sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-195">On the **New Toolbar** page, type **Contoso Main Toolbar** in the **Name** box, and then click **Save**.</span></span>  

6. <span data-ttu-id="b5f5a-196">Attach the toolbar to the toolbar container hosted control created in step 2.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-196">Attach the toolbar to the toolbar container hosted control created in step 2.</span></span> <span data-ttu-id="b5f5a-197">On the nav bar, click the down arrow next to **Contoso Main Toolbar**, and click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-197">On the nav bar, click the down arrow next to **Contoso Main Toolbar**, and click **Hosted Controls**.</span></span>  

7. <span data-ttu-id="b5f5a-198">Trên trang tiếp theo, bấm vào **Thêm kiểm soát tổ chức hiện có**, nhập `Contoso Main Toolbar Container` trong thanh tìm kiếm và sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-198">On the next page, click **Add Existing Hosted Control**, type `Contoso Main Toolbar Container` in the search bar, and then press ENTER or click the search icon.</span></span>  

8. <span data-ttu-id="b5f5a-199">Từ kết quả tìm kiếm, hãy nhấp vào **Bộ chứa thanh công cụ chính Contoso** để thêm.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-199">From the search result, click **Contoso Main Toolbar Container** to add.</span></span>  

9. <span data-ttu-id="b5f5a-200">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-200">Click **Save**.</span></span>  

<a name="Step4"></a>   
## <a name="step-4-add-toolbar-buttons-and-action-calls-to-display-dynamics-365-for-customer-engagement-apps-records"></a><span data-ttu-id="b5f5a-201">Step 4: Add toolbar buttons and action calls to display Dynamics 365 for Customer Engagement apps records</span><span class="sxs-lookup"><span data-stu-id="b5f5a-201">Step 4: Add toolbar buttons and action calls to display Dynamics 365 for Customer Engagement apps records</span></span>  
 <span data-ttu-id="b5f5a-202">In this step, you’ll add buttons on the toolbar and attach action calls to the buttons so that when the button is clicked, appropriate [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records are displayed in the hosted controls that were created in step 1.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-202">In this step, you’ll add buttons on the toolbar and attach action calls to the buttons so that when the button is clicked, appropriate [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records are displayed in the hosted controls that were created in step 1.</span></span> <span data-ttu-id="b5f5a-203">You’ll configure the search button so that clicking the button displays the account and contact submenu items, and clicking a button displays the respective [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-203">You’ll configure the search button so that clicking the button displays the account and contact submenu items, and clicking a button displays the respective [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records.</span></span>  

1. <span data-ttu-id="b5f5a-204">Sau khi bạn lưu thanh công cụ trong bước 3, vùng **nút** sẽ có sẵn.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-204">After you save the toolbar in step 3, the **Buttons** area becomes available.</span></span> <span data-ttu-id="b5f5a-205">In the **Buttons** area, click **+** on the right corner to add a button.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-205">In the **Buttons** area, click **+** on the right corner to add a button.</span></span>  

2. <span data-ttu-id="b5f5a-206">On the **New Toolbar Button** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-206">On the **New Toolbar Button** page, specify the following values:</span></span>  


   |    <span data-ttu-id="b5f5a-207">Trường</span><span class="sxs-lookup"><span data-stu-id="b5f5a-207">Field</span></span>    |                                          <span data-ttu-id="b5f5a-208">Giá trị</span><span class="sxs-lookup"><span data-stu-id="b5f5a-208">Value</span></span>                                           |
   |-------------|------------------------------------------------------------------------------------------|
   |    <span data-ttu-id="b5f5a-209">Tên</span><span class="sxs-lookup"><span data-stu-id="b5f5a-209">Name</span></span>     |                                  <span data-ttu-id="b5f5a-210">Nút tìm kiếm Contoso</span><span class="sxs-lookup"><span data-stu-id="b5f5a-210">Contoso Search Button</span></span>                                   |
   | <span data-ttu-id="b5f5a-211">Văn bản nút</span><span class="sxs-lookup"><span data-stu-id="b5f5a-211">Button Text</span></span> |                                          <span data-ttu-id="b5f5a-212">TÌM KIẾM</span><span class="sxs-lookup"><span data-stu-id="b5f5a-212">SEARCH</span></span>                                          |
   |   <span data-ttu-id="b5f5a-213">Chú giải công cụ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-213">Tooltip</span></span>   | <span data-ttu-id="b5f5a-214">Search [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps accounts and contacts</span><span class="sxs-lookup"><span data-stu-id="b5f5a-214">Search [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps accounts and contacts</span></span> |
   |    <span data-ttu-id="b5f5a-215">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="b5f5a-215">Order</span></span>    |                                            <span data-ttu-id="b5f5a-216">1</span><span class="sxs-lookup"><span data-stu-id="b5f5a-216">1</span></span>                                             |

   <span data-ttu-id="b5f5a-217">![Create the Search toolbar button](../unified-service-desk/media/crm-itpro-usd-wt03-04.png "Create the Search toolbar button")</span><span class="sxs-lookup"><span data-stu-id="b5f5a-217">![Create the Search toolbar button](../unified-service-desk/media/crm-itpro-usd-wt03-04.png "Create the Search toolbar button")</span></span>  

3. <span data-ttu-id="b5f5a-218">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-218">Click **Save**.</span></span>  

4. <span data-ttu-id="b5f5a-219">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh Nút Tìm kiếm và bấm vào Nút trên thanh công cụ.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-219">On the nav bar, click the down arrow next to Contoso Search Button, and click Toolbar Buttons.</span></span>  

   > [!NOTE]
   >  <span data-ttu-id="b5f5a-220">Bạn hiện đang thêm nút thanh công cụ phụ vào nút thanh công cụ hiện có để tạo cấu trúc menu phụ.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-220">You are now adding child toolbar buttons to an existing toolbar button to create a submenu structure.</span></span>  

5. <span data-ttu-id="b5f5a-221">Trên trang tiếp theo, bấm vào **thêm nút thanh công cụ mới**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-221">On the next page, click **Add New Toolbar Button**.</span></span>  

6. <span data-ttu-id="b5f5a-222">Trên trang **Nút thanh công cụ mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-222">On the **New Toolbar Button** page, specify the following values.</span></span>  

   |<span data-ttu-id="b5f5a-223">Trường</span><span class="sxs-lookup"><span data-stu-id="b5f5a-223">Field</span></span>|<span data-ttu-id="b5f5a-224">Giá trị</span><span class="sxs-lookup"><span data-stu-id="b5f5a-224">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="b5f5a-225">Tên</span><span class="sxs-lookup"><span data-stu-id="b5f5a-225">Name</span></span>|<span data-ttu-id="b5f5a-226">Nút tài khoản tìm kiếm Contoso</span><span class="sxs-lookup"><span data-stu-id="b5f5a-226">Contoso Search Account Button</span></span>|  
   |<span data-ttu-id="b5f5a-227">Văn bản nút</span><span class="sxs-lookup"><span data-stu-id="b5f5a-227">Button Text</span></span>|<span data-ttu-id="b5f5a-228">Tài khoản</span><span class="sxs-lookup"><span data-stu-id="b5f5a-228">Account</span></span>|  
   |<span data-ttu-id="b5f5a-229">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="b5f5a-229">Order</span></span>|<span data-ttu-id="b5f5a-230">1</span><span class="sxs-lookup"><span data-stu-id="b5f5a-230">1</span></span><br /><br /> <span data-ttu-id="b5f5a-231">Trường **Thứ tự** xác định vị trí của nút trên thanh công cụ.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-231">The **Order** field defines the position of buttons in the toolbar.</span></span> <span data-ttu-id="b5f5a-232">Buttons are arranged from left to right or top to bottom in an ascending order.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-232">Buttons are arranged from left to right or top to bottom in an ascending order.</span></span>|  

   <span data-ttu-id="b5f5a-233">![Create a tooolbar button for Account submenu](../unified-service-desk/media/crm-itpro-usd-wt03-05.png "Create a tooolbar button for Account submenu")</span><span class="sxs-lookup"><span data-stu-id="b5f5a-233">![Create a tooolbar button for Account submenu](../unified-service-desk/media/crm-itpro-usd-wt03-05.png "Create a tooolbar button for Account submenu")</span></span>  

7. <span data-ttu-id="b5f5a-234">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-234">Click **Save**.</span></span>  

8. <span data-ttu-id="b5f5a-235">Bây giờ bạn sẽ thêm hai cuộc gọi hành động: cuộc gọi đầu tiên là để hiển thị các hồ sơ tài khoản trong kiểm soát tổ chức đã tạo ở bước 1 và cuộc gọi thứ hai trên kiếm soát tổ chức trình quản lý chung Contoso để hiển thị kiểm soát tổ chức tài khoản.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-235">You’ll now add two action calls: first to display the account records in the hosted control created in step 1 and the second one on the Contoso Global Manager hosted control to display the account hosted control.</span></span>  

    <span data-ttu-id="b5f5a-236">In the **Actions** area, click **+** on the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-236">In the **Actions** area, click **+** on the right corner to add an action call.</span></span>  

9. <span data-ttu-id="b5f5a-237">Trong hộp tìm kiếm trong vùng **hành động**, nhấn ENTER hoặc nhấp biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-237">In the search box in the **Actions** area, press ENTER or click the search icon.</span></span>  

10. <span data-ttu-id="b5f5a-238">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-238">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>  

    <span data-ttu-id="b5f5a-239">![Choose New to create an action call](../unified-service-desk/media/crm-itpro-usd-wt03-06.png "Choose New to create an action call")</span><span class="sxs-lookup"><span data-stu-id="b5f5a-239">![Choose New to create an action call](../unified-service-desk/media/crm-itpro-usd-wt03-06.png "Choose New to create an action call")</span></span>  

11. <span data-ttu-id="b5f5a-240">On the **New Action Call** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-240">On the **New Action Call** page, specify the following values:</span></span>  

    |<span data-ttu-id="b5f5a-241">Trường</span><span class="sxs-lookup"><span data-stu-id="b5f5a-241">Field</span></span>|<span data-ttu-id="b5f5a-242">Giá trị</span><span class="sxs-lookup"><span data-stu-id="b5f5a-242">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="b5f5a-243">Tên</span><span class="sxs-lookup"><span data-stu-id="b5f5a-243">Name</span></span>|<span data-ttu-id="b5f5a-244">Các cuộc gọi hành động contoso: Tìm tài khoản</span><span class="sxs-lookup"><span data-stu-id="b5f5a-244">Contoso Action Call: Search Account</span></span>|  
    |<span data-ttu-id="b5f5a-245">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="b5f5a-245">Order</span></span>|<span data-ttu-id="b5f5a-246">1</span><span class="sxs-lookup"><span data-stu-id="b5f5a-246">1</span></span>|  
    |<span data-ttu-id="b5f5a-247">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-247">Hosted Control</span></span>|<span data-ttu-id="b5f5a-248">Tìm kiếm tài khoản Contoso</span><span class="sxs-lookup"><span data-stu-id="b5f5a-248">Contoso Accounts Search</span></span>|  
    |<span data-ttu-id="b5f5a-249">Hành động</span><span class="sxs-lookup"><span data-stu-id="b5f5a-249">Action</span></span>|<span data-ttu-id="b5f5a-250">Find</span><span class="sxs-lookup"><span data-stu-id="b5f5a-250">Find</span></span>|  
    |<span data-ttu-id="b5f5a-251">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="b5f5a-251">Data</span></span>|<span data-ttu-id="b5f5a-252">tài khoản</span><span class="sxs-lookup"><span data-stu-id="b5f5a-252">account</span></span>|  

    <span data-ttu-id="b5f5a-253">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-07.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="b5f5a-253">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-07.png "Create an action call in Unified Service Desk")</span></span>  

12. <span data-ttu-id="b5f5a-254">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-254">Click **Save**.</span></span> <span data-ttu-id="b5f5a-255">Cuộc gọi hành động mới được thêm vào nút **Nút tài khoản tìm kiếm Contoso**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-255">The new action call gets added to the **Contoso Search Account Button** button.</span></span>  

13. <span data-ttu-id="b5f5a-256">Bạn sẽ thêm một cuộc gọi hành động vào nút để đặt trọng tâm trên kiểm soát tổ chức mà hiển thị các hồ sơ tài khoản trong ứng dụng khách.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-256">You’ll add another action call to the button to set the focus on the hosted control that displays the account records in the client application.</span></span> <span data-ttu-id="b5f5a-257">In the **Actions** area, click **+** on the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-257">In the **Actions** area, click **+** on the right corner to add an action call.</span></span>  

14. <span data-ttu-id="b5f5a-258">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-258">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>  

15. <span data-ttu-id="b5f5a-259">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-259">On the **New Action Call** page, specify the following values.</span></span>  

    |<span data-ttu-id="b5f5a-260">Trường</span><span class="sxs-lookup"><span data-stu-id="b5f5a-260">Field</span></span>|<span data-ttu-id="b5f5a-261">Giá trị</span><span class="sxs-lookup"><span data-stu-id="b5f5a-261">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="b5f5a-262">Tên</span><span class="sxs-lookup"><span data-stu-id="b5f5a-262">Name</span></span>|<span data-ttu-id="b5f5a-263">Cuộc gọi hành động contoso: Hiển thị tìm kiếm tài khoản</span><span class="sxs-lookup"><span data-stu-id="b5f5a-263">Contoso Action Call: Display Account Search</span></span>|  
    |<span data-ttu-id="b5f5a-264">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="b5f5a-264">Order</span></span>|<span data-ttu-id="b5f5a-265">2</span><span class="sxs-lookup"><span data-stu-id="b5f5a-265">2</span></span>|  
    |<span data-ttu-id="b5f5a-266">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="b5f5a-266">Hosted Control</span></span>|<span data-ttu-id="b5f5a-267">Trình quản lý chung contoso</span><span class="sxs-lookup"><span data-stu-id="b5f5a-267">Contoso Global Manager</span></span>|  
    |<span data-ttu-id="b5f5a-268">Hành động</span><span class="sxs-lookup"><span data-stu-id="b5f5a-268">Action</span></span>|<span data-ttu-id="b5f5a-269">Hiển thị tab</span><span class="sxs-lookup"><span data-stu-id="b5f5a-269">ShowTab</span></span>|  
    |<span data-ttu-id="b5f5a-270">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="b5f5a-270">Data</span></span>|<span data-ttu-id="b5f5a-271">Contoso Accounts Search</span><span class="sxs-lookup"><span data-stu-id="b5f5a-271">Contoso Accounts Search</span></span>|  

    <span data-ttu-id="b5f5a-272">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-08.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="b5f5a-272">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-08.png "Create an action call in Unified Service Desk")</span></span>  

16. <span data-ttu-id="b5f5a-273">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-273">Click **Save**.</span></span> <span data-ttu-id="b5f5a-274">The new action call gets added to the **Contoso Search Account Button** button.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-274">The new action call gets added to the **Contoso Search Account Button** button.</span></span>  

17. <span data-ttu-id="b5f5a-275">Điều hướng đến nút thanh công cụ **Nút tìm kiếm Contoso** để thêm nút phụ để tìm kiếm và hiển thị liên hệ.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-275">Navigate to **Contoso Search Button** toolbar button to add a child button for searching and displaying contacts.</span></span> <span data-ttu-id="b5f5a-276">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Nút tìm kiếm Contoso** và chọn **Nút thanh công cụ**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-276">On the nav bar, click the down arrow next to **Contoso Search Button**, and select **Toolbar Buttons**.</span></span>  

18. <span data-ttu-id="b5f5a-277">Trên trang tiếp theo, bấm vào **thêm nút thanh công cụ mới**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-277">On the next page, click **Add New Toolbar Button**.</span></span>  

19. <span data-ttu-id="b5f5a-278">Trên trang **Nút thanh công cụ mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-278">On the **New Toolbar Button** page, specify the following values:</span></span>  

    |<span data-ttu-id="b5f5a-279">Trường</span><span class="sxs-lookup"><span data-stu-id="b5f5a-279">Field</span></span>|<span data-ttu-id="b5f5a-280">Giá trị</span><span class="sxs-lookup"><span data-stu-id="b5f5a-280">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="b5f5a-281">Tên</span><span class="sxs-lookup"><span data-stu-id="b5f5a-281">Name</span></span>|<span data-ttu-id="b5f5a-282">Nút Liên hệ tìm kiếm Contoso</span><span class="sxs-lookup"><span data-stu-id="b5f5a-282">Contoso Search Contact Button</span></span>|  
    |<span data-ttu-id="b5f5a-283">Văn bản nút</span><span class="sxs-lookup"><span data-stu-id="b5f5a-283">Button Text</span></span>|<span data-ttu-id="b5f5a-284">Người liên hệ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-284">Contact</span></span>|  
    |<span data-ttu-id="b5f5a-285">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="b5f5a-285">Order</span></span>|<span data-ttu-id="b5f5a-286">2</span><span class="sxs-lookup"><span data-stu-id="b5f5a-286">2</span></span><br /><br /> <span data-ttu-id="b5f5a-287">Trường **Thứ tự** xác định vị trí của nút trên thanh công cụ.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-287">The **Order** field defines the position of buttons in the toolbar.</span></span> <span data-ttu-id="b5f5a-288">Buttons are arranged from left to right or top to bottom in an ascending order.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-288">Buttons are arranged from left to right or top to bottom in an ascending order.</span></span>|  

    <span data-ttu-id="b5f5a-289">![Create a toolbar button for contacts search](../unified-service-desk/media/crm-itpro-usd-wt03-09.png "Create a toolbar button for contacts search")</span><span class="sxs-lookup"><span data-stu-id="b5f5a-289">![Create a toolbar button for contacts search](../unified-service-desk/media/crm-itpro-usd-wt03-09.png "Create a toolbar button for contacts search")</span></span>  

20. <span data-ttu-id="b5f5a-290">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-290">Click **Save**.</span></span>  

21. <span data-ttu-id="b5f5a-291">Bây giờ bạn sẽ thêm hai cuộc gọi hành động: cuộc gọi đầu tiên là để hiển thị các hồ sơ liên hệ trong kiểm soát tổ chức đã tạo ở bước 1 và cuộc gọi thứ hai trên kiếm soát tổ chức trình quản lý chung Contoso để hiển thị kiểm soát tổ chức liên hệ.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-291">You’ll now add two action calls: first to display the contact records in the hosted control that were created in step 1 and the second one on the Contoso Global Manager hosted control to display the contacts hosted control.</span></span>  

     <span data-ttu-id="b5f5a-292">In the **Actions** area, click **+** on the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-292">In the **Actions** area, click **+** on the right corner to add an action call.</span></span>  

22. <span data-ttu-id="b5f5a-293">In the search box in the **Actions** area, press ENTER or click the search icon.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-293">In the search box in the **Actions** area, press ENTER or click the search icon.</span></span>  

23. <span data-ttu-id="b5f5a-294">Trong hộp tìm kiếm kết quả, bấm vào **Mới** ở góc dưới bên phải để tạo ra cuộc gọi hành động cho nút thanh công cụ này.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-294">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>  

24. <span data-ttu-id="b5f5a-295">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-295">On the **New Action Call** page, specify the following values:</span></span>  

    |<span data-ttu-id="b5f5a-296">Trường</span><span class="sxs-lookup"><span data-stu-id="b5f5a-296">Field</span></span>|<span data-ttu-id="b5f5a-297">Giá trị</span><span class="sxs-lookup"><span data-stu-id="b5f5a-297">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="b5f5a-298">Tên</span><span class="sxs-lookup"><span data-stu-id="b5f5a-298">Name</span></span>|<span data-ttu-id="b5f5a-299">Các cuộc gọi hành động contoso: Tìm liên hệ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-299">Contoso Action Call: Search Contact</span></span>|  
    |<span data-ttu-id="b5f5a-300">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="b5f5a-300">Order</span></span>|<span data-ttu-id="b5f5a-301">1</span><span class="sxs-lookup"><span data-stu-id="b5f5a-301">1</span></span>|  
    |<span data-ttu-id="b5f5a-302">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-302">Hosted Control</span></span>|<span data-ttu-id="b5f5a-303">Tìm kiếm liên hệ Contoso</span><span class="sxs-lookup"><span data-stu-id="b5f5a-303">Contoso Contacts Search</span></span>|  
    |<span data-ttu-id="b5f5a-304">Hành động</span><span class="sxs-lookup"><span data-stu-id="b5f5a-304">Action</span></span>|<span data-ttu-id="b5f5a-305">Find</span><span class="sxs-lookup"><span data-stu-id="b5f5a-305">Find</span></span>|  
    |<span data-ttu-id="b5f5a-306">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="b5f5a-306">Data</span></span>|<span data-ttu-id="b5f5a-307">người liên hệ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-307">contact</span></span>|  

    <span data-ttu-id="b5f5a-308">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-10.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="b5f5a-308">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-10.png "Create an action call in Unified Service Desk")</span></span>  

25. <span data-ttu-id="b5f5a-309">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-309">Click **Save**.</span></span> <span data-ttu-id="b5f5a-310">Cuộc gọi hành động mới được thêm vào nút thanh công cụ **Nút liên hệ tìm kiếm Contoso**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-310">The new action call gets added to the **Contoso Search Contact Button** toolbar button.</span></span>  

26. <span data-ttu-id="b5f5a-311">Bạn sẽ thêm một cuộc gọi hành động vào nút để đặt trọng tâm trên kiểm soát tổ chức mà hiển thị các hồ sơ liên hệ trong ứng dụng khách.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-311">You’ll add another action call to the button to set the focus on the hosted control that displays the contact records in the client application.</span></span> <span data-ttu-id="b5f5a-312">In the **Actions** area, click **+** on the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-312">In the **Actions** area, click **+** on the right corner to add an action call.</span></span>  

27. <span data-ttu-id="b5f5a-313">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-313">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>  

28. <span data-ttu-id="b5f5a-314">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-314">On the **New Action Call** page, specify the following values.</span></span>  

    |<span data-ttu-id="b5f5a-315">Trường</span><span class="sxs-lookup"><span data-stu-id="b5f5a-315">Field</span></span>|<span data-ttu-id="b5f5a-316">Giá trị</span><span class="sxs-lookup"><span data-stu-id="b5f5a-316">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="b5f5a-317">Tên</span><span class="sxs-lookup"><span data-stu-id="b5f5a-317">Name</span></span>|<span data-ttu-id="b5f5a-318">Cuộc gọi hành động contoso: Hiển thị tìm kiếm liên hệ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-318">Contoso Action Call: Display Contact Search</span></span>|  
    |<span data-ttu-id="b5f5a-319">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="b5f5a-319">Order</span></span>|<span data-ttu-id="b5f5a-320">2</span><span class="sxs-lookup"><span data-stu-id="b5f5a-320">2</span></span>|  
    |<span data-ttu-id="b5f5a-321">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="b5f5a-321">Hosted Control</span></span>|<span data-ttu-id="b5f5a-322">Contoso Global Manager</span><span class="sxs-lookup"><span data-stu-id="b5f5a-322">Contoso Global Manager</span></span>|  
    |<span data-ttu-id="b5f5a-323">Hành động</span><span class="sxs-lookup"><span data-stu-id="b5f5a-323">Action</span></span>|<span data-ttu-id="b5f5a-324">Hiển thị tab</span><span class="sxs-lookup"><span data-stu-id="b5f5a-324">ShowTab</span></span>|  
    |<span data-ttu-id="b5f5a-325">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="b5f5a-325">Data</span></span>|<span data-ttu-id="b5f5a-326">Contoso Contacts Search</span><span class="sxs-lookup"><span data-stu-id="b5f5a-326">Contoso Contacts Search</span></span>|  

    <span data-ttu-id="b5f5a-327">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-11.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="b5f5a-327">![Create an action call in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt03-11.png "Create an action call in Unified Service Desk")</span></span>  

29. <span data-ttu-id="b5f5a-328">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-328">Click **Save**.</span></span> <span data-ttu-id="b5f5a-329">The new action call gets added to the **Contoso Search Contact Button** toolbar button.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-329">The new action call gets added to the **Contoso Search Contact Button** toolbar button.</span></span>  

<a name="Step5"></a>   
## <a name="step-5-add-the-controls-to-the-configuration"></a><span data-ttu-id="b5f5a-330">Bước 5: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="b5f5a-330">Step 5: Add the controls to the configuration</span></span>  
 <span data-ttu-id="b5f5a-331">Trong bước này, bạn sẽ thêm cuộc gọi hành động, kiểm soát tổ chức và thanh công cụ đã tạo trong cách này vào **Cấu hình Contoso** để hiển thị các kiểm soát này cho người dùng được chỉ định cho cấu hình này.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-331">In this step, you’ll add the action calls, hosted controls, and toolbar that were created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span></span> <span data-ttu-id="b5f5a-332">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="b5f5a-332">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span>  

 <span data-ttu-id="b5f5a-333">Add the following to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-333">Add the following to **Contoso Configuration**.</span></span>  

|<span data-ttu-id="b5f5a-334">Tên kiểm soát</span><span class="sxs-lookup"><span data-stu-id="b5f5a-334">Control name</span></span>|<span data-ttu-id="b5f5a-335">Loại kiểm soát</span><span class="sxs-lookup"><span data-stu-id="b5f5a-335">Control type</span></span>|  
|------------------|------------------|  
|<span data-ttu-id="b5f5a-336">Các cuộc gọi hành động contoso: Tìm tài khoản</span><span class="sxs-lookup"><span data-stu-id="b5f5a-336">Contoso Action Call: Search Account</span></span>|<span data-ttu-id="b5f5a-337">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="b5f5a-337">Action Call</span></span>|  
|<span data-ttu-id="b5f5a-338">Cuộc gọi hành động contoso: Hiển thị tìm kiếm tài khoản</span><span class="sxs-lookup"><span data-stu-id="b5f5a-338">Contoso Action Call: Display Account Search</span></span>|<span data-ttu-id="b5f5a-339">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="b5f5a-339">Action Call</span></span>|  
|<span data-ttu-id="b5f5a-340">Các cuộc gọi hành động contoso: Tìm liên hệ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-340">Contoso Action Call: Search Contact</span></span>|<span data-ttu-id="b5f5a-341">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="b5f5a-341">Action Call</span></span>|  
|<span data-ttu-id="b5f5a-342">Cuộc gọi hành động contoso: Hiển thị tìm kiếm liên hệ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-342">Contoso Action Call: Display Contact Search</span></span>|<span data-ttu-id="b5f5a-343">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="b5f5a-343">Action Call</span></span>|  
|<span data-ttu-id="b5f5a-344">Tìm kiếm tài khoản Contoso</span><span class="sxs-lookup"><span data-stu-id="b5f5a-344">Contoso Accounts Search</span></span>|<span data-ttu-id="b5f5a-345">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="b5f5a-345">Hosted Control</span></span>|  
|<span data-ttu-id="b5f5a-346">Tìm kiếm liên hệ Contoso</span><span class="sxs-lookup"><span data-stu-id="b5f5a-346">Contoso Contacts Search</span></span>|<span data-ttu-id="b5f5a-347">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="b5f5a-347">Hosted Control</span></span>|  
|<span data-ttu-id="b5f5a-348">Bộ chứa thanh công cụ chính Contoso</span><span class="sxs-lookup"><span data-stu-id="b5f5a-348">Contoso Main Toolbar Container</span></span>|<span data-ttu-id="b5f5a-349">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="b5f5a-349">Hosted Control</span></span>|  
|<span data-ttu-id="b5f5a-350">Thanh công cụ chính Contoso</span><span class="sxs-lookup"><span data-stu-id="b5f5a-350">Contoso Main Toolbar</span></span>|<span data-ttu-id="b5f5a-351">Thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="b5f5a-351">Toolbar</span></span>|  

 <span data-ttu-id="b5f5a-352">To add a control to the configuration:</span><span class="sxs-lookup"><span data-stu-id="b5f5a-352">To add a control to the configuration:</span></span>  

1. <span data-ttu-id="b5f5a-353">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-353">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="b5f5a-354">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-354">Click **Configuration**.</span></span>  

4. <span data-ttu-id="b5f5a-355">Click **Contoso Configuration** to open the definition.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-355">Click **Contoso Configuration** to open the definition.</span></span>  

5. <span data-ttu-id="b5f5a-356">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-356">On the nav bar, click the down arrow next to **Contoso Configuration**, and select **Action Calls**.</span></span>  

6. <span data-ttu-id="b5f5a-357">Trên trang tiếp theo, bấm vào **Thêm Cuộc gọi Hành động Hiện có**, nhập “`Contoso Action Call`” vào thanh tìm kiếm, sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-357">On the next page, click **Add Existing Action Call**, type “`Contoso Action Call`” in the search bar, and then press ENTER or click the search icon.</span></span>  

7. <span data-ttu-id="b5f5a-358">Các cuộc gọi hành động được liệt kê trước đó được hiển thị trong kết quả tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-358">The action calls listed earlier are displayed in the search results.</span></span> <span data-ttu-id="b5f5a-359">Thêm các cuộc gọi hành động này.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-359">Add these action calls.</span></span>  

8. <span data-ttu-id="b5f5a-360">Tương tự, thêm kiểm soát tổ chức và thanh công cụ bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Kiểm soát tổ chức** và **thanh công cụ** lần lượt.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-360">Similarly, add the hosted controls and the toolbar by clicking the down arrow next to **Contoso Configuration**, and clicking **Hosted Controls** and **Toolbars** respectively.</span></span>  

9. <span data-ttu-id="b5f5a-361">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-361">Click **Save**.</span></span>  

<a name="Step6"></a>   
## <a name="step-6-test-the-application"></a><span data-ttu-id="b5f5a-362">Bước 6: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="b5f5a-362">Step 6: Test the application</span></span>  
 <span data-ttu-id="b5f5a-363">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="b5f5a-363">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span> <span data-ttu-id="b5f5a-364">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span><span class="sxs-lookup"><span data-stu-id="b5f5a-364">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span></span>  

 <span data-ttu-id="b5f5a-365">Ứng dụng tổng đài viên của bạn bây giờ sẽ có nút **TÌM KIẾM** trong vùng thanh công cụ có hai nút phụ (**tài khoản** và **liên hệ**) mà được hiển thị khi nhấn vào mũi tên xuống.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-365">Your agent application will now have a **SEARCH** button in the toolbar area with two child buttons (**Account** and **Contact**) that are displayed on clicking the down arrow.</span></span>  

 <span data-ttu-id="b5f5a-366">![Display account and contact records](../unified-service-desk/media/crm-itpro-usd-wt03-12.png "Display account and contact records")</span><span class="sxs-lookup"><span data-stu-id="b5f5a-366">![Display account and contact records](../unified-service-desk/media/crm-itpro-usd-wt03-12.png "Display account and contact records")</span></span>  

 <span data-ttu-id="b5f5a-367">Click **Account** or **Contact** under the **SEARCH** button to display the respective records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance in separate tabs in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-367">Click **Account** or **Contact** under the **SEARCH** button to display the respective records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance in separate tabs in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.</span></span>  

 <span data-ttu-id="b5f5a-368">![Dynamics 365 for Customer Engagement apps contact records displayed](../unified-service-desk/media/crm-itpro-usd-wt03-13.png "Dynamics 365 for Customer Engagement apps contact records displayed")</span><span class="sxs-lookup"><span data-stu-id="b5f5a-368">![Dynamics 365 for Customer Engagement apps contact records displayed](../unified-service-desk/media/crm-itpro-usd-wt03-13.png "Dynamics 365 for Customer Engagement apps contact records displayed")</span></span>  

<a name="Conclusion"></a>   
## <a name="conclusion"></a><span data-ttu-id="b5f5a-369">Kết luận</span><span class="sxs-lookup"><span data-stu-id="b5f5a-369">Conclusion</span></span>  
 <span data-ttu-id="b5f5a-370">In this walkthrough, you learned how to display [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-370">In this walkthrough, you learned how to display [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application.</span></span> <span data-ttu-id="b5f5a-371">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span><span class="sxs-lookup"><span data-stu-id="b5f5a-371">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span></span>  

### <a name="see-also"></a><span data-ttu-id="b5f5a-372">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b5f5a-372">See also</span></span>  
 <span data-ttu-id="b5f5a-373">[Cách 1: Xây dựng ứng dụng tổng đài viên đơn giản](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="b5f5a-373">[Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) </span></span>  
 <span data-ttu-id="b5f5a-374">[Cách 2: Hiển thị trang web bên ngoài trong ứng dụng tổng đài viên của bạn](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="b5f5a-374">[Walkthrough 2: Display an external webpage in your agent application](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md) </span></span>  
 <span data-ttu-id="b5f5a-375">[Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="b5f5a-375">[Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md) </span></span>  
 <span data-ttu-id="b5f5a-376">[Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md) </span><span class="sxs-lookup"><span data-stu-id="b5f5a-376">[Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md) </span></span>  
 <span data-ttu-id="b5f5a-377">[Hướng 6: Đặt cấu hình kiểm soát tổ chức trình gỡ lỗi trong ứng dụng tổng đài viên của bạn](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="b5f5a-377">[Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md) </span></span>  
 <span data-ttu-id="b5f5a-378">[Cách 7: Đặt cấu hình mã lệnh tổng đài viên trong ứng dụng tổng đài viên của bạn](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="b5f5a-378">[Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md) </span></span>  
 [<span data-ttu-id="b5f5a-379">Unified Service Desk Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="b5f5a-379">Unified Service Desk Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
