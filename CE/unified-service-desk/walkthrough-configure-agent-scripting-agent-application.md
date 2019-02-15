---
title: 'Walkthrough 7: Configure agent scripting in your agent application | MicrosoftDocs'
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
ms.assetid: 083926df-aa2e-410c-9d23-719450c77edb
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: d4f37edc7b36e0e3c6c9576ece72db46e9a0313d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386313"
---
# <a name="walkthrough-7-configure-agent-scripting-in-your-agent-application"></a><span data-ttu-id="edec9-102">Walkthrough 7: Configure agent scripting in your agent application</span><span class="sxs-lookup"><span data-stu-id="edec9-102">Walkthrough 7: Configure agent scripting in your agent application</span></span>
<span data-ttu-id="edec9-103">Mã lệnh tổng đài viên trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] giúp hướng dẫn tổng đài viên của bạn trong suốt quá trình tương tác với khách hàng.</span><span class="sxs-lookup"><span data-stu-id="edec9-103">Agent scripting in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] helps to guide your agents during customer interaction.</span></span> <span data-ttu-id="edec9-104">Cách này trình bày cách tạo mã lệnh tổng đài viên đơn giảm giúp tổng đài viên nhanh chóng tạo trường hợp mới cho tài khoản hoặc tìm các trường hợp hiện có từ ứng dụng tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="edec9-104">This walkthrough demonstrates how to create a simple agent script that helps the agents quickly create a new case for an account or browse existing cases from the agent application.</span></span> <span data-ttu-id="edec9-105">Mã lệnh tổng đài viên đã tạo trong cách này được thực hiện khi tổng đài viên dừng một hồ sơ tài khoản để xem, hồ sơ đó được hiển thị trong phiên trong ứng dụng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="edec9-105">The agent script created in this walkthrough is invoked when the agent pulls up an account record to view, which is displayed in a session in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client.</span></span> <span data-ttu-id="edec9-106">Mã lệnh cung cấp ba tùy chọn sau:</span><span class="sxs-lookup"><span data-stu-id="edec9-106">The script provides the following three options:</span></span>  

-   <span data-ttu-id="edec9-107">Tạo ra một trường hợp cho tài khoản hiện tại</span><span class="sxs-lookup"><span data-stu-id="edec9-107">Create a case for the current account</span></span>  

-   <span data-ttu-id="edec9-108">Hiển thị các trường hợp có sẵn cho tài khoản hiện tại</span><span class="sxs-lookup"><span data-stu-id="edec9-108">Display existing cases for the current account</span></span>  

-   <span data-ttu-id="edec9-109">Close the session</span><span class="sxs-lookup"><span data-stu-id="edec9-109">Close the session</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="edec9-110">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="edec9-110">Prerequisites</span></span>  

- <span data-ttu-id="edec9-111">You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) and [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="edec9-111">You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) and [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md).</span></span> <span data-ttu-id="edec9-112">The configurations that you completed in those walkthroughs are required in this walkthrough.</span><span class="sxs-lookup"><span data-stu-id="edec9-112">The configurations that you completed in those walkthroughs are required in this walkthrough.</span></span>  

- <span data-ttu-id="edec9-113">Cách này giả định rằng bạn sẽ sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="edec9-113">This walkthrough assumes that you’ll be using the same user credential that you used in walkthrough 1 to sign in to the agent application.</span></span> <span data-ttu-id="edec9-114">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="edec9-114">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="edec9-115">[Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)</span><span class="sxs-lookup"><span data-stu-id="edec9-115">[Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)</span></span>  

- <span data-ttu-id="edec9-116">Bạn phải làm quen với các khái niệm sau trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="edec9-116">You must know be familiar with the following concepts in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  

  - <span data-ttu-id="edec9-117">**Agent Scripting** type of hosted control and how to configure agent scripts.</span><span class="sxs-lookup"><span data-stu-id="edec9-117">**Agent Scripting** type of hosted control and how to configure agent scripts.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="edec9-118">[Agent Scripting (Hosted Control)](../unified-service-desk/agent-scripting-hosted-control.md) and [Guide customer interactions with agent scripts](../unified-service-desk/guide-customer-interactions-agent-scripts.md)</span><span class="sxs-lookup"><span data-stu-id="edec9-118">[Agent Scripting (Hosted Control)](../unified-service-desk/agent-scripting-hosted-control.md) and [Guide customer interactions with agent scripts](../unified-service-desk/guide-customer-interactions-agent-scripts.md)</span></span>  

  - <span data-ttu-id="edec9-119">How to configure [Action calls](../unified-service-desk/action-calls.md)</span><span class="sxs-lookup"><span data-stu-id="edec9-119">How to configure [Action calls](../unified-service-desk/action-calls.md)</span></span>  

  - <span data-ttu-id="edec9-120">Cách cấu hình nguyên tắc điều hướng cửa sổ.</span><span class="sxs-lookup"><span data-stu-id="edec9-120">How to configure window navigation rules.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="edec9-121">[Use window navigation rules in Unified Service Desk](../unified-service-desk/use-window-navigation-rules-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="edec9-121">[Use window navigation rules in Unified Service Desk](../unified-service-desk/use-window-navigation-rules-unified-service-desk.md)</span></span>  

  - <span data-ttu-id="edec9-122">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span><span class="sxs-lookup"><span data-stu-id="edec9-122">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="edec9-123">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="edec9-123">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span></span>  

## <a name="in-this-walkthrough"></a><span data-ttu-id="edec9-124">In This Walkthrough</span><span class="sxs-lookup"><span data-stu-id="edec9-124">In This Walkthrough</span></span>  
 [<span data-ttu-id="edec9-125">Bước 1: Tạo một loại mã lệnh tổng đài viên của kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="edec9-125">Step 1: Create an Agent Scripting type of hosted control</span></span>](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md#Step1)  

 [<span data-ttu-id="edec9-126">Bước 2: Tạo kiểm soát tổ chức để hiển thị biểu mẫu trường hợp mới và trường hợp hiện có</span><span class="sxs-lookup"><span data-stu-id="edec9-126">Step 2: Create hosted controls to display the new case form and existing cases</span></span>](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md#Step2)  

 [<span data-ttu-id="edec9-127">Bước 3: Tạo một tác vụ mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="edec9-127">Step 3: Create an agent script task</span></span>](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md#Step3)  

 [<span data-ttu-id="edec9-128">Bước 4: Thêm câu trả lời, cuộc gọi hành động và nguyên tắc điều hướng cửa sổ để tạo trường hợp từ mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="edec9-128">Step 4: Add the answer, action call, and window navigation rule for creating a case from the agent script</span></span>](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md#Step4)  

 [<span data-ttu-id="edec9-129">Bước 5: Thêm câu trả lời và cuộc gọi hành động để hiển thị trường hợp sẵn có</span><span class="sxs-lookup"><span data-stu-id="edec9-129">Step 5: Add the answer and action calls for displaying existing cases</span></span>](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md#Step5)  

 [<span data-ttu-id="edec9-130">Bước 6: Thêm câu trả lời và cuộc gọi hành động để đóng phiên</span><span class="sxs-lookup"><span data-stu-id="edec9-130">Step 6: Add the answer and action calls for closing the session</span></span>](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md#Step6)  

 [<span data-ttu-id="edec9-131">Bước 7: Tạo cuộc gọi hành động để hiển thị mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="edec9-131">Step 7: Create an action call to display the agent script</span></span>](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md#Step7)  

 [<span data-ttu-id="edec9-132">Bước 8: Hiển thị mã lệnh tổng đài viên khi hồ sơ tài khoản được hiển thị trong phiên.</span><span class="sxs-lookup"><span data-stu-id="edec9-132">Step 8: Display the agent script when the account record is displayed in a session</span></span>](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md#Step8)  

 [<span data-ttu-id="edec9-133">Bước 9: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="edec9-133">Step 9: Add the controls to the configuration</span></span>](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md#Step9)  

 [<span data-ttu-id="edec9-134">Bước 10: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="edec9-134">Step 10: Test the application</span></span>](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md#Step10)  

 [<span data-ttu-id="edec9-135">Kết luận</span><span class="sxs-lookup"><span data-stu-id="edec9-135">Conclusion</span></span>](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md#Conclusion)  

<a name="Step1"></a>   
## <a name="step-1-create-an-agent-scripting-type-of-hosted-control"></a><span data-ttu-id="edec9-136">Bước 1: Tạo một loại mã lệnh tổng đài viên của kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="edec9-136">Step 1: Create an Agent Scripting type of hosted control</span></span>  
 <span data-ttu-id="edec9-137">Một phiên bản của loại **Mã lệnh tổng đài viên** của kiểm soát tổ chức phải có sẵn trong ứng dụng tổng đài viên của bạn để hiển thị mã lệnh tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="edec9-137">An instance of the **Agent Scripting** type of hosted control must be available in your agent application to display agent scripts.</span></span>  

1. <span data-ttu-id="edec9-138">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="edec9-138">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="edec9-139">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="edec9-139">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="edec9-140">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="edec9-140">Click **New**.</span></span>  

5. <span data-ttu-id="edec9-141">On the **New Hosted Control** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="edec9-141">On the **New Hosted Control** page, specify the following values.</span></span>  

   |<span data-ttu-id="edec9-142">Trường</span><span class="sxs-lookup"><span data-stu-id="edec9-142">Field</span></span>|<span data-ttu-id="edec9-143">Giá trị</span><span class="sxs-lookup"><span data-stu-id="edec9-143">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="edec9-144">Tên</span><span class="sxs-lookup"><span data-stu-id="edec9-144">Name</span></span>|<span data-ttu-id="edec9-145">Mã lệnh tổng đài viên Contoso</span><span class="sxs-lookup"><span data-stu-id="edec9-145">Contoso Agent Scripting</span></span>|  
   |<span data-ttu-id="edec9-146">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="edec9-146">USD Component Type</span></span>|<span data-ttu-id="edec9-147">Mã lệnh của tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="edec9-147">Agent Scripting</span></span>|  
   |<span data-ttu-id="edec9-148">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="edec9-148">Display Group</span></span>|<span data-ttu-id="edec9-149">Bảng điều khiển quy trình làm việc</span><span class="sxs-lookup"><span data-stu-id="edec9-149">WorkflowPanel</span></span>|  

   <span data-ttu-id="edec9-150">![Create an Agent Scripting hosted control](../unified-service-desk/media/usd-create-agent-scripting-hosted-control.png "Create an Agent Scripting hosted control")</span><span class="sxs-lookup"><span data-stu-id="edec9-150">![Create an Agent Scripting hosted control](../unified-service-desk/media/usd-create-agent-scripting-hosted-control.png "Create an Agent Scripting hosted control")</span></span>  

6. <span data-ttu-id="edec9-151">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="edec9-151">Click **Save**.</span></span>  

<a name="Step2"></a>   
## <a name="step-2-create-hosted-controls-to-display-the-new-case-form-and-existing-cases"></a><span data-ttu-id="edec9-152">Bước 2: Tạo kiểm soát tổ chức để hiển thị biểu mẫu trường hợp mới và trường hợp hiện có</span><span class="sxs-lookup"><span data-stu-id="edec9-152">Step 2: Create hosted controls to display the new case form and existing cases</span></span>  
 <span data-ttu-id="edec9-153">Trong bước này, bạn sẽ tạo hai kiểm soát tổ chức của loại Trang CRM để hiển thị biểu mẫu tạo trường hợp mới và trường hợp hiện có cho tài khoản hiện tại.</span><span class="sxs-lookup"><span data-stu-id="edec9-153">In this step, you’ll create two hosted controls of CRM Page type to display the new case creation form and existing cases for the current account.</span></span>  

1. <span data-ttu-id="edec9-154">Trên trang kiểm soát tổ chức, bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="edec9-154">On the hosted controls page, click **New**.</span></span>  

2. <span data-ttu-id="edec9-155">Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="edec9-155">On the **New Hosted Control** page, specify the following values:</span></span>  

   |<span data-ttu-id="edec9-156">Trường</span><span class="sxs-lookup"><span data-stu-id="edec9-156">Field</span></span>|<span data-ttu-id="edec9-157">Giá trị</span><span class="sxs-lookup"><span data-stu-id="edec9-157">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="edec9-158">Tên</span><span class="sxs-lookup"><span data-stu-id="edec9-158">Name</span></span>|<span data-ttu-id="edec9-159">Biểu mẫu trường hợp mới</span><span class="sxs-lookup"><span data-stu-id="edec9-159">Contoso new case form</span></span>|  
   |<span data-ttu-id="edec9-160">Tên hiển thị</span><span class="sxs-lookup"><span data-stu-id="edec9-160">Display Name</span></span>|<span data-ttu-id="edec9-161">Trường hợp mới</span><span class="sxs-lookup"><span data-stu-id="edec9-161">New Case</span></span>|  
   |<span data-ttu-id="edec9-162">Loại Thành phần USD</span><span class="sxs-lookup"><span data-stu-id="edec9-162">USD Component Type</span></span>|<span data-ttu-id="edec9-163">Trang CRM</span><span class="sxs-lookup"><span data-stu-id="edec9-163">CRM Page</span></span>|  
   |<span data-ttu-id="edec9-164">Cho phép nhiều trang</span><span class="sxs-lookup"><span data-stu-id="edec9-164">Allow Multiple Pages</span></span>|<span data-ttu-id="edec9-165">No</span><span class="sxs-lookup"><span data-stu-id="edec9-165">No</span></span>|  
   |<span data-ttu-id="edec9-166">Loại tổ chức</span><span class="sxs-lookup"><span data-stu-id="edec9-166">Hosting Type</span></span>|<span data-ttu-id="edec9-167">WPF nội bộ</span><span class="sxs-lookup"><span data-stu-id="edec9-167">Internal WPF</span></span>|  
   |<span data-ttu-id="edec9-168">Application is Global</span><span class="sxs-lookup"><span data-stu-id="edec9-168">Application is Global</span></span>|<span data-ttu-id="edec9-169">Không được chọn</span><span class="sxs-lookup"><span data-stu-id="edec9-169">Not checked</span></span>|  
   |<span data-ttu-id="edec9-170">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="edec9-170">Display Group</span></span>|<span data-ttu-id="edec9-171">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="edec9-171">MainPanel</span></span>|  

   <span data-ttu-id="edec9-172">![Create a CRM Page hosted control](../unified-service-desk/media/usd-create-page-hosted-control-2.png "Create a CRM Page hosted control")</span><span class="sxs-lookup"><span data-stu-id="edec9-172">![Create a CRM Page hosted control](../unified-service-desk/media/usd-create-page-hosted-control-2.png "Create a CRM Page hosted control")</span></span>  

3. <span data-ttu-id="edec9-173">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="edec9-173">Click **Save**.</span></span>  

4. <span data-ttu-id="edec9-174">Trên trang kiểm soát tổ chức, bấm vào **Mới** để tạo kiểm soát tổ chức khác.</span><span class="sxs-lookup"><span data-stu-id="edec9-174">On the hosted controls page, click **New** to create another hosted control.</span></span>  

5. <span data-ttu-id="edec9-175">Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="edec9-175">On the **New Hosted Control** page, specify the following values:</span></span>  

   |<span data-ttu-id="edec9-176">Trường</span><span class="sxs-lookup"><span data-stu-id="edec9-176">Field</span></span>|<span data-ttu-id="edec9-177">Giá trị</span><span class="sxs-lookup"><span data-stu-id="edec9-177">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="edec9-178">Tên</span><span class="sxs-lookup"><span data-stu-id="edec9-178">Name</span></span>|<span data-ttu-id="edec9-179">Trường hợp sẵn có Contoso cho tài khoản</span><span class="sxs-lookup"><span data-stu-id="edec9-179">Contoso existing cases for an account</span></span>|  
   |<span data-ttu-id="edec9-180">Tên Hiển thị</span><span class="sxs-lookup"><span data-stu-id="edec9-180">Display Name</span></span>|<span data-ttu-id="edec9-181">Cases for [[$Context.name]] **Note:**  We are using the replacement parameter to dynamically display the name of the current account from the execution context as the hosted control display name.</span><span class="sxs-lookup"><span data-stu-id="edec9-181">Cases for [[$Context.name]] **Note:**  We are using the replacement parameter to dynamically display the name of the current account from the execution context as the hosted control display name.</span></span>|  
   |<span data-ttu-id="edec9-182">Loại Thành phần USD</span><span class="sxs-lookup"><span data-stu-id="edec9-182">USD Component Type</span></span>|<span data-ttu-id="edec9-183">Trang CRM</span><span class="sxs-lookup"><span data-stu-id="edec9-183">CRM Page</span></span>|  
   |<span data-ttu-id="edec9-184">Cho phép nhiều trang</span><span class="sxs-lookup"><span data-stu-id="edec9-184">Allow Multiple Pages</span></span>|<span data-ttu-id="edec9-185">No</span><span class="sxs-lookup"><span data-stu-id="edec9-185">No</span></span>|  
   |<span data-ttu-id="edec9-186">Loại tổ chức</span><span class="sxs-lookup"><span data-stu-id="edec9-186">Hosting Type</span></span>|<span data-ttu-id="edec9-187">WPF nội bộ</span><span class="sxs-lookup"><span data-stu-id="edec9-187">Internal WPF</span></span>|  
   |<span data-ttu-id="edec9-188">Application is Global</span><span class="sxs-lookup"><span data-stu-id="edec9-188">Application is Global</span></span>|<span data-ttu-id="edec9-189">Không được chọn</span><span class="sxs-lookup"><span data-stu-id="edec9-189">Not checked</span></span>|  
   |<span data-ttu-id="edec9-190">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="edec9-190">Display Group</span></span>|<span data-ttu-id="edec9-191">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="edec9-191">MainPanel</span></span>|  

   <span data-ttu-id="edec9-192">![Create a CRM Page hosted control](../unified-service-desk/media/usd-create-agent-script-task.png "Create a CRM Page hosted control")</span><span class="sxs-lookup"><span data-stu-id="edec9-192">![Create a CRM Page hosted control](../unified-service-desk/media/usd-create-agent-script-task.png "Create a CRM Page hosted control")</span></span>  

6. <span data-ttu-id="edec9-193">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="edec9-193">Click **Save**.</span></span>  

<a name="Step3"></a>   
## <a name="step-3-create-an-agent-script-task"></a><span data-ttu-id="edec9-194">Bước 3: Tạo một tác vụ mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="edec9-194">Step 3: Create an agent script task</span></span>  
 <span data-ttu-id="edec9-195">Tạo một tác vụ mã lệnh tổng đài viên để hiển thị thời điểm hồ sơ tài khoản được hiển thị trong một phiên.</span><span class="sxs-lookup"><span data-stu-id="edec9-195">Create an agent script task to display when an account record is displayed in a session.</span></span>  

1. <span data-ttu-id="edec9-196">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="edec9-196">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="edec9-197">Click **Agent Scripts**.</span><span class="sxs-lookup"><span data-stu-id="edec9-197">Click **Agent Scripts**.</span></span>  

4. <span data-ttu-id="edec9-198">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="edec9-198">Click **New**.</span></span>  

5. <span data-ttu-id="edec9-199">Trên trang **Tác vụ mã lệnh tổng đài viên mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="edec9-199">On the **New Agent Script Task** page, specify the following values:</span></span>  

   |<span data-ttu-id="edec9-200">Trường</span><span class="sxs-lookup"><span data-stu-id="edec9-200">Field</span></span>|<span data-ttu-id="edec9-201">Giá trị</span><span class="sxs-lookup"><span data-stu-id="edec9-201">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="edec9-202">Tên</span><span class="sxs-lookup"><span data-stu-id="edec9-202">Name</span></span>|<span data-ttu-id="edec9-203">Contoso: Chào mừng bạn đến với Phiên tài khoản</span><span class="sxs-lookup"><span data-stu-id="edec9-203">Contoso: Welcome to Account Session</span></span>|  
   |<span data-ttu-id="edec9-204">Bắt đầu nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="edec9-204">Start Task</span></span>|<span data-ttu-id="edec9-205">No</span><span class="sxs-lookup"><span data-stu-id="edec9-205">No</span></span>|  
   |<span data-ttu-id="edec9-206">Văn bản mã lệnh</span><span class="sxs-lookup"><span data-stu-id="edec9-206">ScriptText</span></span>|<span data-ttu-id="edec9-207">Chào mừng bạn đến [[$Context.name]].</span><span class="sxs-lookup"><span data-stu-id="edec9-207">Welcome [[$Context.name]].</span></span> <span data-ttu-id="edec9-208">Tên tôi là [[$User.firstname]].</span><span class="sxs-lookup"><span data-stu-id="edec9-208">My name is [[$User.firstname]].</span></span> <span data-ttu-id="edec9-209">Cuộc gọi này có liên quan đến yêu cầu dịch vụ hiện tại hoặc mới không?</span><span class="sxs-lookup"><span data-stu-id="edec9-209">Is this call regarding a new or an existing service request?</span></span> <span data-ttu-id="edec9-210">**Note:**  We are using replacement parameters to dynamically display the account name and the current agent’s name to the agent at runtime.</span><span class="sxs-lookup"><span data-stu-id="edec9-210">**Note:**  We are using replacement parameters to dynamically display the account name and the current agent’s name to the agent at runtime.</span></span>|  
   |<span data-ttu-id="edec9-211">Hướng dẫn</span><span class="sxs-lookup"><span data-stu-id="edec9-211">Instructions</span></span>|<span data-ttu-id="edec9-212">Dựa trên phản ứng của khách hàng, bấm vào một trong những nhiệm vụ dưới đây.</span><span class="sxs-lookup"><span data-stu-id="edec9-212">Based on the customer response, click one of the tasks below.</span></span>|  

   <span data-ttu-id="edec9-213">![Create an agent script task](../unified-service-desk/media/usd-create-agent-script-task-2.png "Create an agent script task")</span><span class="sxs-lookup"><span data-stu-id="edec9-213">![Create an agent script task](../unified-service-desk/media/usd-create-agent-script-task-2.png "Create an agent script task")</span></span>  

6. <span data-ttu-id="edec9-214">Bấm vào **Lưu** để tạo mã lệnh tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="edec9-214">Click **Save** to create the agent script.</span></span>  

<a name="Step4"></a>   
## <a name="step-4-add-the-answer-action-call-and-window-navigation-rule-for-creating-a-case-from-the-agent-script"></a><span data-ttu-id="edec9-215">Bước 4: Thêm câu trả lời, cuộc gọi hành động và nguyên tắc điều hướng cửa sổ để tạo trường hợp từ mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="edec9-215">Step 4: Add the answer, action call, and window navigation rule for creating a case from the agent script</span></span>  
 <span data-ttu-id="edec9-216">Trong bước này, bạn sẽ tạo ra câu trả lời, cuộc gọi hành động và nguyên tắc điều hướng cửa sổ để hiển thị biểu mẫu trường hợp mới với một số giá trị được xác định trước từ hồ sơ tài khoản đang hiện hoạt.</span><span class="sxs-lookup"><span data-stu-id="edec9-216">In this step, you’ll create answer, action call, and window navigation rule for displaying a new case form with some prepopulated values from the currently active account record.</span></span>  

1. <span data-ttu-id="edec9-217">In the **Answers** area of the agent script task that you created in step 4, click **+** to create answer.</span><span class="sxs-lookup"><span data-stu-id="edec9-217">In the **Answers** area of the agent script task that you created in step 4, click **+** to create answer.</span></span>  

2. <span data-ttu-id="edec9-218">Trong hộp tìm kiếm, nhấn ENTER hoặc nhấp vào biểu tượng tìm kiếm, sau đó nhấp vào **Mới** trong hộp tìm kiếm kết quả.</span><span class="sxs-lookup"><span data-stu-id="edec9-218">In the search box, press ENTER or click the search icon, and then click **New** in the search results box.</span></span>  

   <span data-ttu-id="edec9-219">![Create an answer for an agent script task](../unified-service-desk/media/usd-create-answer-agent-script-task.png "Create an answer for an agent script task")</span><span class="sxs-lookup"><span data-stu-id="edec9-219">![Create an answer for an agent script task](../unified-service-desk/media/usd-create-answer-agent-script-task.png "Create an answer for an agent script task")</span></span>  

3. <span data-ttu-id="edec9-220">Trên trang **Câu trả lời mã lệnh tổng đài viên mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="edec9-220">On the **New Agent Script Answer** page, specify the following values:</span></span>  

   |<span data-ttu-id="edec9-221">Trường</span><span class="sxs-lookup"><span data-stu-id="edec9-221">Field</span></span>|<span data-ttu-id="edec9-222">Giá trị</span><span class="sxs-lookup"><span data-stu-id="edec9-222">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="edec9-223">Tên</span><span class="sxs-lookup"><span data-stu-id="edec9-223">Name</span></span>|<span data-ttu-id="edec9-224">Contoso: Trường hợp mới</span><span class="sxs-lookup"><span data-stu-id="edec9-224">Contoso: New case</span></span>|  
   |<span data-ttu-id="edec9-225">Văn bản câu trả lời</span><span class="sxs-lookup"><span data-stu-id="edec9-225">Answer Text</span></span>|<span data-ttu-id="edec9-226">Create a case</span><span class="sxs-lookup"><span data-stu-id="edec9-226">Create a case</span></span>|  
   |<span data-ttu-id="edec9-227">Nhiệm vụ được liên kết</span><span class="sxs-lookup"><span data-stu-id="edec9-227">Linked Task</span></span>|<span data-ttu-id="edec9-228">Contoso: Chào mừng bạn đến với Phiên tài khoản</span><span class="sxs-lookup"><span data-stu-id="edec9-228">Contoso: Welcome to Account Session</span></span>|  
   |<span data-ttu-id="edec9-229">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="edec9-229">Order</span></span>|<span data-ttu-id="edec9-230">1</span><span class="sxs-lookup"><span data-stu-id="edec9-230">1</span></span>|  

   <span data-ttu-id="edec9-231">![Create an answer in Unified Service Desk](../unified-service-desk/media/usd-create-answer.png "Create an answer in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="edec9-231">![Create an answer in Unified Service Desk](../unified-service-desk/media/usd-create-answer.png "Create an answer in Unified Service Desk")</span></span>  

4. <span data-ttu-id="edec9-232">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="edec9-232">Click **Save**.</span></span>  

5. <span data-ttu-id="edec9-233">Tiếp theo, thêm cuộc gọi hành động cho câu trả lời này để hiển thị biểu mẫu trường hợp mới cho tài khoản khi tổng đài viên nhấp vào câu trả lời này.</span><span class="sxs-lookup"><span data-stu-id="edec9-233">Next, add an action call to this answer to display a new case form for the account when the agent clicks this answer.</span></span> <span data-ttu-id="edec9-234">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Contoso: trường hợp mới** và chọn **Hành động**.</span><span class="sxs-lookup"><span data-stu-id="edec9-234">On the nav bar, click the down arrow next to **Contoso: New case**, and select **Actions**.</span></span>  

   <span data-ttu-id="edec9-235">![Create an action call for the answer](../unified-service-desk/media/usd-create-action-call-answer.png "Create an action call for the answer")</span><span class="sxs-lookup"><span data-stu-id="edec9-235">![Create an action call for the answer](../unified-service-desk/media/usd-create-action-call-answer.png "Create an action call for the answer")</span></span>  

6. <span data-ttu-id="edec9-236">Trên trang tiếp theo, bấm vào **thêm cuộc gọi hành động hiện có**.</span><span class="sxs-lookup"><span data-stu-id="edec9-236">On the next page, click **Add Existing Action Call**.</span></span>  

7. <span data-ttu-id="edec9-237">Trong hộp tìm kiếm, nhấn ENTER hoặc nhấp vào biểu tượng tìm kiếm, sau đó nhấp vào **Mới** để tạo cuộc gọi hàn động.</span><span class="sxs-lookup"><span data-stu-id="edec9-237">In the search box, press ENTER or click the search icon, and then click **New** to create an action call.</span></span>  

8. <span data-ttu-id="edec9-238">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="edec9-238">On the **New Action Call** page, specify the following values:</span></span>  

   |<span data-ttu-id="edec9-239">Trường</span><span class="sxs-lookup"><span data-stu-id="edec9-239">Field</span></span>|<span data-ttu-id="edec9-240">Giá trị</span><span class="sxs-lookup"><span data-stu-id="edec9-240">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="edec9-241">Tên</span><span class="sxs-lookup"><span data-stu-id="edec9-241">Name</span></span>|<span data-ttu-id="edec9-242">Cuộc gọi hành động contoso: Tạo trường hợp</span><span class="sxs-lookup"><span data-stu-id="edec9-242">Contoso Action Call: Create Case</span></span>|  
   |<span data-ttu-id="edec9-243">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="edec9-243">Order</span></span>|<span data-ttu-id="edec9-244">1</span><span class="sxs-lookup"><span data-stu-id="edec9-244">1</span></span>|  
   |<span data-ttu-id="edec9-245">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="edec9-245">Hosted Control</span></span>|<span data-ttu-id="edec9-246">Biểu mẫu trường hợp mới</span><span class="sxs-lookup"><span data-stu-id="edec9-246">Contoso new case form</span></span>|  
   |<span data-ttu-id="edec9-247">Hành động</span><span class="sxs-lookup"><span data-stu-id="edec9-247">Action</span></span>|<span data-ttu-id="edec9-248">New_CRM_Page</span><span class="sxs-lookup"><span data-stu-id="edec9-248">New_CRM_Page</span></span>|  
   |<span data-ttu-id="edec9-249">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="edec9-249">Data</span></span>|<span data-ttu-id="edec9-250">LogicalName=incident</span><span class="sxs-lookup"><span data-stu-id="edec9-250">LogicalName=incident</span></span><br /> <span data-ttu-id="edec9-251">customerid=EntityReference([[$Context.InitialEntity]],[[$Context.Id]])</span><span class="sxs-lookup"><span data-stu-id="edec9-251">customerid=EntityReference([[$Context.InitialEntity]],[[$Context.Id]])</span></span>  <br /> <span data-ttu-id="edec9-252">customeridname=[[$Context.name]]</span><span class="sxs-lookup"><span data-stu-id="edec9-252">customeridname=[[$Context.name]]</span></span> <br /> <span data-ttu-id="edec9-253">primarycontactid=[[$Context.primarycontactid.id]+]</span><span class="sxs-lookup"><span data-stu-id="edec9-253">primarycontactid=[[$Context.primarycontactid.id]+]</span></span>  <br /> <span data-ttu-id="edec9-254">primarycontactidname=[[$Context.primarycontactid.name]+] **Note:**  The new case form will be populated with the current account record data to help the agent quickly create a case for the customer.</span><span class="sxs-lookup"><span data-stu-id="edec9-254">primarycontactidname=[[$Context.primarycontactid.name]+] **Note:**  The new case form will be populated with the current account record data to help the agent quickly create a case for the customer.</span></span>|  

   <span data-ttu-id="edec9-255">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call-answer.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="edec9-255">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call-answer.png "Create an action call in Unified Service Desk")</span></span>  

9. <span data-ttu-id="edec9-256">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="edec9-256">Click **Save**.</span></span>  

10. <span data-ttu-id="edec9-257">Sau đó, tạo quy tắc chuyển hướng cửa sổ để hiển thị biểu mẫu trường hợp mới.</span><span class="sxs-lookup"><span data-stu-id="edec9-257">Next, create a window navigation rule to display the new case form.</span></span> [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

11. <span data-ttu-id="edec9-258">Click **Window Navigation Rules**.</span><span class="sxs-lookup"><span data-stu-id="edec9-258">Click **Window Navigation Rules**.</span></span>  

12. <span data-ttu-id="edec9-259">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="edec9-259">Click **New**.</span></span>  

13. <span data-ttu-id="edec9-260">Trên trang **Nguyên tắc điều hướng cửa sổ mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="edec9-260">On the **New Window Navigation Rule** page, specify the following values.</span></span>  

    |<span data-ttu-id="edec9-261">Trường</span><span class="sxs-lookup"><span data-stu-id="edec9-261">Field</span></span>|<span data-ttu-id="edec9-262">Giá trị</span><span class="sxs-lookup"><span data-stu-id="edec9-262">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="edec9-263">Tên</span><span class="sxs-lookup"><span data-stu-id="edec9-263">Name</span></span>|<span data-ttu-id="edec9-264">Trường hợp mới Contoso cho nguyên tắc phiên tài khoản</span><span class="sxs-lookup"><span data-stu-id="edec9-264">Contoso New Case for Account Session Rule</span></span>|  
    |<span data-ttu-id="edec9-265">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="edec9-265">Order</span></span>|<span data-ttu-id="edec9-266">20</span><span class="sxs-lookup"><span data-stu-id="edec9-266">20</span></span>|  
    |<span data-ttu-id="edec9-267">Từ</span><span class="sxs-lookup"><span data-stu-id="edec9-267">From</span></span>|<span data-ttu-id="edec9-268">Biểu mẫu trường hợp mới</span><span class="sxs-lookup"><span data-stu-id="edec9-268">Contoso new case form</span></span>|  
    |<span data-ttu-id="edec9-269">Thực thể</span><span class="sxs-lookup"><span data-stu-id="edec9-269">Entity</span></span>|<span data-ttu-id="edec9-270">sự cố</span><span class="sxs-lookup"><span data-stu-id="edec9-270">incident</span></span>|  
    |<span data-ttu-id="edec9-271">Loại định tuyến</span><span class="sxs-lookup"><span data-stu-id="edec9-271">Route Type</span></span>|<span data-ttu-id="edec9-272">Bật lên</span><span class="sxs-lookup"><span data-stu-id="edec9-272">Popup</span></span>|  
    |<span data-ttu-id="edec9-273">Điểm đến</span><span class="sxs-lookup"><span data-stu-id="edec9-273">Destination</span></span>|<span data-ttu-id="edec9-274">Tab</span><span class="sxs-lookup"><span data-stu-id="edec9-274">Tab</span></span>|  
    |<span data-ttu-id="edec9-275">Hành động</span><span class="sxs-lookup"><span data-stu-id="edec9-275">Action</span></span>|<span data-ttu-id="edec9-276">Cửa sổ lộ trình</span><span class="sxs-lookup"><span data-stu-id="edec9-276">Route Window</span></span>|  
    |<span data-ttu-id="edec9-277">Tab Mục tiêu</span><span class="sxs-lookup"><span data-stu-id="edec9-277">Target Tab</span></span>|<span data-ttu-id="edec9-278">Biểu mẫu trường hợp mới</span><span class="sxs-lookup"><span data-stu-id="edec9-278">Contoso new case form</span></span>|  
    |<span data-ttu-id="edec9-279">Hiển thị Tab</span><span class="sxs-lookup"><span data-stu-id="edec9-279">Show Tab</span></span>|<span data-ttu-id="edec9-280">Biểu mẫu trường hợp mới</span><span class="sxs-lookup"><span data-stu-id="edec9-280">Contoso new case form</span></span>|  
    |<span data-ttu-id="edec9-281">Hide Command Bar</span><span class="sxs-lookup"><span data-stu-id="edec9-281">Hide Command Bar</span></span>|<span data-ttu-id="edec9-282">Không</span><span class="sxs-lookup"><span data-stu-id="edec9-282">No</span></span>|  
    |<span data-ttu-id="edec9-283">Hide Navigation Bar</span><span class="sxs-lookup"><span data-stu-id="edec9-283">Hide Navigation Bar</span></span>|<span data-ttu-id="edec9-284">Có</span><span class="sxs-lookup"><span data-stu-id="edec9-284">Yes</span></span>|  

    <span data-ttu-id="edec9-285">![Create a window navigation rule](../unified-service-desk/media/usd-window-navigation-rule.png "Create a window navigation rule")</span><span class="sxs-lookup"><span data-stu-id="edec9-285">![Create a window navigation rule](../unified-service-desk/media/usd-window-navigation-rule.png "Create a window navigation rule")</span></span>  

14. <span data-ttu-id="edec9-286">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="edec9-286">Click **Save**.</span></span>  

<a name="Step5"></a>   
## <a name="step-5-add-the-answer-and-action-calls-for-displaying-existing-cases"></a><span data-ttu-id="edec9-287">Bước 5: Thêm câu trả lời và cuộc gọi hành động để hiển thị trường hợp sẵn có</span><span class="sxs-lookup"><span data-stu-id="edec9-287">Step 5: Add the answer and action calls for displaying existing cases</span></span>  
 <span data-ttu-id="edec9-288">Trong bước này, thêm câu trả lời và cuộc gọi hành động để hiển thị các trường hợp sẵn có cho tài khoản hiện tại.</span><span class="sxs-lookup"><span data-stu-id="edec9-288">In this step, add answer and action calls for displaying existing cases for the current account.</span></span>  

1. <span data-ttu-id="edec9-289">In the **Answers** area of the **Contoso: Welcome to Account Session** agent script, click **+** to create an answer.</span><span class="sxs-lookup"><span data-stu-id="edec9-289">In the **Answers** area of the **Contoso: Welcome to Account Session** agent script, click **+** to create an answer.</span></span>  

2. <span data-ttu-id="edec9-290">In the search box, press ENTER or click the search icon, and then click **New** in the search results box.</span><span class="sxs-lookup"><span data-stu-id="edec9-290">In the search box, press ENTER or click the search icon, and then click **New** in the search results box.</span></span>  

3. <span data-ttu-id="edec9-291">Trên trang **Câu trả lời mã lệnh tổng đài viên mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="edec9-291">On the **New Agent Script Answer** page, specify the following values.</span></span>  


   |    <span data-ttu-id="edec9-292">Trường</span><span class="sxs-lookup"><span data-stu-id="edec9-292">Field</span></span>    |                <span data-ttu-id="edec9-293">Giá trị</span><span class="sxs-lookup"><span data-stu-id="edec9-293">Value</span></span>                |
   |-------------|-------------------------------------|
   |    <span data-ttu-id="edec9-294">Tên</span><span class="sxs-lookup"><span data-stu-id="edec9-294">Name</span></span>     |       <span data-ttu-id="edec9-295">Contoso: Trường hợp hiện có</span><span class="sxs-lookup"><span data-stu-id="edec9-295">Contoso: Existing cases</span></span>       |
   | <span data-ttu-id="edec9-296">Văn bản câu trả lời</span><span class="sxs-lookup"><span data-stu-id="edec9-296">Answer Text</span></span> |       <span data-ttu-id="edec9-297">Hiển thị trường hợp hiện có</span><span class="sxs-lookup"><span data-stu-id="edec9-297">Display existing cases</span></span>        |
   | <span data-ttu-id="edec9-298">Nhiệm vụ được liên kết</span><span class="sxs-lookup"><span data-stu-id="edec9-298">Linked Task</span></span> | <span data-ttu-id="edec9-299">Contoso: Chào mừng bạn đến với Phiên tài khoản</span><span class="sxs-lookup"><span data-stu-id="edec9-299">Contoso: Welcome to Account Session</span></span> |
   |    <span data-ttu-id="edec9-300">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="edec9-300">Order</span></span>    |                  <span data-ttu-id="edec9-301">2</span><span class="sxs-lookup"><span data-stu-id="edec9-301">2</span></span>                  |


4. <span data-ttu-id="edec9-302">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="edec9-302">Click **Save**.</span></span>  

5. <span data-ttu-id="edec9-303">Tiếp theo, thêm cuộc gọi hành động vào câu trả lời này để hiển thị các trường hợp sẵn có cho tài khoản hiện tại.</span><span class="sxs-lookup"><span data-stu-id="edec9-303">Next, add an action call to this answer to display the existing cases for the current account.</span></span> <span data-ttu-id="edec9-304">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Trường hợp hiện có** và chọn **Hành động**.</span><span class="sxs-lookup"><span data-stu-id="edec9-304">On the nav bar, click the down arrow next to **Contoso: Existing Cases**, and select **Actions**.</span></span>  

6. <span data-ttu-id="edec9-305">Trên trang tiếp theo, bấm vào **thêm cuộc gọi hành động hiện có**.</span><span class="sxs-lookup"><span data-stu-id="edec9-305">On the next page, click **Add Existing Action Call**.</span></span>  

7. <span data-ttu-id="edec9-306">Trong hộp tìm kiếm, nhấn ENTER hoặc nhấp vào biểu tượng tìm kiếm, sau đó nhấp vào **Mới** để tạo cuộc gọi hàn động.</span><span class="sxs-lookup"><span data-stu-id="edec9-306">In the search box, press ENTER or click the search icon, and then click **New** to create an action call.</span></span>  

8. <span data-ttu-id="edec9-307">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="edec9-307">On the **New Action Call** page, specify the following values:</span></span>  

   |<span data-ttu-id="edec9-308">Trường</span><span class="sxs-lookup"><span data-stu-id="edec9-308">Field</span></span>|<span data-ttu-id="edec9-309">Giá trị</span><span class="sxs-lookup"><span data-stu-id="edec9-309">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="edec9-310">Tên</span><span class="sxs-lookup"><span data-stu-id="edec9-310">Name</span></span>|<span data-ttu-id="edec9-311">Cuộc gọi hành động Contoso: Hiển thị trường hợp hiện có</span><span class="sxs-lookup"><span data-stu-id="edec9-311">Contoso Action Call: Display Existing Cases</span></span>|  
   |<span data-ttu-id="edec9-312">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="edec9-312">Order</span></span>|<span data-ttu-id="edec9-313">1</span><span class="sxs-lookup"><span data-stu-id="edec9-313">1</span></span>|  
   |<span data-ttu-id="edec9-314">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="edec9-314">Hosted Control</span></span>|<span data-ttu-id="edec9-315">Trường hợp sẵn có Contoso cho tài khoản</span><span class="sxs-lookup"><span data-stu-id="edec9-315">Contoso existing cases for an account</span></span>|  
   |<span data-ttu-id="edec9-316">Hành động</span><span class="sxs-lookup"><span data-stu-id="edec9-316">Action</span></span>|<span data-ttu-id="edec9-317">Chế độ xem Liên kết</span><span class="sxs-lookup"><span data-stu-id="edec9-317">AssociatedView</span></span>|  
   |<span data-ttu-id="edec9-318">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="edec9-318">Data</span></span>|<span data-ttu-id="edec9-319">navItemName=Cases</span><span class="sxs-lookup"><span data-stu-id="edec9-319">navItemName=Cases</span></span><br /><span data-ttu-id="edec9-320">Id=[[$Context.Id]]</span><span class="sxs-lookup"><span data-stu-id="edec9-320">Id=[[$Context.Id]]</span></span> <br /><span data-ttu-id="edec9-321">type=[[$Context.etc]]</span><span class="sxs-lookup"><span data-stu-id="edec9-321">type=[[$Context.etc]]</span></span> <br /><span data-ttu-id="edec9-322">tabset=areaService</span><span class="sxs-lookup"><span data-stu-id="edec9-322">tabset=areaService</span></span>|  

   <span data-ttu-id="edec9-323">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="edec9-323">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call.png "Create an action call in Unified Service Desk")</span></span>  

9. <span data-ttu-id="edec9-324">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="edec9-324">Click **Save**.</span></span>  

10. <span data-ttu-id="edec9-325">Thêm một cuộc gọi hành động khác để chú trọng vào biểu mẫu trường hợp mới.</span><span class="sxs-lookup"><span data-stu-id="edec9-325">Add another action call to set the focus on the new case form.</span></span> <span data-ttu-id="edec9-326">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="edec9-326">On the **New Action Call** page, specify the following values:</span></span>  

    |<span data-ttu-id="edec9-327">Trường</span><span class="sxs-lookup"><span data-stu-id="edec9-327">Field</span></span>|<span data-ttu-id="edec9-328">Giá trị</span><span class="sxs-lookup"><span data-stu-id="edec9-328">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="edec9-329">Tên</span><span class="sxs-lookup"><span data-stu-id="edec9-329">Name</span></span>|<span data-ttu-id="edec9-330">Cuộc gọi hành động Contoso: Tập trung vào trường hợp hiện có</span><span class="sxs-lookup"><span data-stu-id="edec9-330">Contoso Action Call: Set Focus on Existing Cases</span></span>|  
    |<span data-ttu-id="edec9-331">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="edec9-331">Order</span></span>|<span data-ttu-id="edec9-332">2</span><span class="sxs-lookup"><span data-stu-id="edec9-332">2</span></span>|  
    |<span data-ttu-id="edec9-333">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="edec9-333">Hosted Control</span></span>|<span data-ttu-id="edec9-334">Trình quản lý chung contoso</span><span class="sxs-lookup"><span data-stu-id="edec9-334">Contoso Global Manager</span></span>|  
    |<span data-ttu-id="edec9-335">Hành động</span><span class="sxs-lookup"><span data-stu-id="edec9-335">Action</span></span>|<span data-ttu-id="edec9-336">Hiển thị tab</span><span class="sxs-lookup"><span data-stu-id="edec9-336">ShowTab</span></span>|  
    |<span data-ttu-id="edec9-337">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="edec9-337">Data</span></span>|<span data-ttu-id="edec9-338">Contoso existing cases for an account</span><span class="sxs-lookup"><span data-stu-id="edec9-338">Contoso existing cases for an account</span></span>|  

    <span data-ttu-id="edec9-339">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call-2.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="edec9-339">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call-2.png "Create an action call in Unified Service Desk")</span></span>  

11. <span data-ttu-id="edec9-340">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="edec9-340">Click **Save**.</span></span>  

<a name="Step6"></a>   
## <a name="step-6-add-the-answer-and-action-calls-for-closing-the-session"></a><span data-ttu-id="edec9-341">Bước 6: Thêm câu trả lời và cuộc gọi hành động để đóng phiên</span><span class="sxs-lookup"><span data-stu-id="edec9-341">Step 6: Add the answer and action calls for closing the session</span></span>  
 <span data-ttu-id="edec9-342">Trong bước này, thêm câu trả lời và cuộc gọi hành động để đóng phiên.</span><span class="sxs-lookup"><span data-stu-id="edec9-342">In this step, add answer and action calls for closing the current session.</span></span>  

1. <span data-ttu-id="edec9-343">In the **Answers** area of the **Contoso: Welcome to Account Session** agent script, click **+** to create an answer.</span><span class="sxs-lookup"><span data-stu-id="edec9-343">In the **Answers** area of the **Contoso: Welcome to Account Session** agent script, click **+** to create an answer.</span></span>  

2. <span data-ttu-id="edec9-344">In the search box, press ENTER or click the search icon, and then click **New** in the search results box.</span><span class="sxs-lookup"><span data-stu-id="edec9-344">In the search box, press ENTER or click the search icon, and then click **New** in the search results box.</span></span>  

3. <span data-ttu-id="edec9-345">Trên trang **Câu trả lời mã lệnh tổng đài viên mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="edec9-345">On the **New Agent Script Answer** page, specify the following values:</span></span>  


   |    <span data-ttu-id="edec9-346">Trường</span><span class="sxs-lookup"><span data-stu-id="edec9-346">Field</span></span>    |                <span data-ttu-id="edec9-347">Giá trị</span><span class="sxs-lookup"><span data-stu-id="edec9-347">Value</span></span>                |
   |-------------|-------------------------------------|
   |    <span data-ttu-id="edec9-348">Tên</span><span class="sxs-lookup"><span data-stu-id="edec9-348">Name</span></span>     |       <span data-ttu-id="edec9-349">Contoso: Đóng phiên</span><span class="sxs-lookup"><span data-stu-id="edec9-349">Contoso: Close session</span></span>        |
   | <span data-ttu-id="edec9-350">Văn bản câu trả lời</span><span class="sxs-lookup"><span data-stu-id="edec9-350">Answer Text</span></span> |            <span data-ttu-id="edec9-351">Đóng phiên</span><span class="sxs-lookup"><span data-stu-id="edec9-351">Close session</span></span>            |
   | <span data-ttu-id="edec9-352">Nhiệm vụ được liên kết</span><span class="sxs-lookup"><span data-stu-id="edec9-352">Linked Task</span></span> | <span data-ttu-id="edec9-353">Contoso: Chào mừng bạn đến với Phiên tài khoản</span><span class="sxs-lookup"><span data-stu-id="edec9-353">Contoso: Welcome to Account Session</span></span> |
   |    <span data-ttu-id="edec9-354">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="edec9-354">Order</span></span>    |                  <span data-ttu-id="edec9-355">3</span><span class="sxs-lookup"><span data-stu-id="edec9-355">3</span></span>                  |


4. <span data-ttu-id="edec9-356">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="edec9-356">Click **Save**.</span></span>  

5. <span data-ttu-id="edec9-357">Tiếp theo, thêm cuộc gọi hành động cho câu trả lời này để đóng phiên.</span><span class="sxs-lookup"><span data-stu-id="edec9-357">Next, add an action call to this answer to close the session.</span></span> <span data-ttu-id="edec9-358">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Contoso: Đóng phiên** và chọn Hành động.</span><span class="sxs-lookup"><span data-stu-id="edec9-358">On the nav bar, click the down arrow next to **Contoso: Close session**, and select Actions.</span></span>  

6. <span data-ttu-id="edec9-359">Trên trang tiếp theo, bấm vào **thêm cuộc gọi hành động hiện có**.</span><span class="sxs-lookup"><span data-stu-id="edec9-359">On the next page, click **Add Existing Action Call**.</span></span>  

7. <span data-ttu-id="edec9-360">Trong hộp tìm kiếm, nhấn ENTER hoặc nhấp vào biểu tượng tìm kiếm, sau đó nhấp vào **Mới** để tạo cuộc gọi hàn động.</span><span class="sxs-lookup"><span data-stu-id="edec9-360">In the search box, press ENTER or click the search icon, and then click **New** to create an action call.</span></span>  

8. <span data-ttu-id="edec9-361">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="edec9-361">On the **New Action Call** page, specify the following values.</span></span>  

   |<span data-ttu-id="edec9-362">Trường</span><span class="sxs-lookup"><span data-stu-id="edec9-362">Field</span></span>|<span data-ttu-id="edec9-363">Giá trị</span><span class="sxs-lookup"><span data-stu-id="edec9-363">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="edec9-364">Tên</span><span class="sxs-lookup"><span data-stu-id="edec9-364">Name</span></span>|<span data-ttu-id="edec9-365">Các cuộc gọi hành động contoso: Đóng phiên</span><span class="sxs-lookup"><span data-stu-id="edec9-365">Contoso Action Call: Close Session</span></span>|  
   |<span data-ttu-id="edec9-366">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="edec9-366">Hosted Control</span></span>|<span data-ttu-id="edec9-367">Contoso Session Tab **Note:**  The Contoso Session Tab hosted control was created in [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="edec9-367">Contoso Session Tab **Note:**  The Contoso Session Tab hosted control was created in [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md).</span></span>|  
   |<span data-ttu-id="edec9-368">Hành động</span><span class="sxs-lookup"><span data-stu-id="edec9-368">Action</span></span>|<span data-ttu-id="edec9-369">Đóng phiên</span><span class="sxs-lookup"><span data-stu-id="edec9-369">CloseSession</span></span>|  
   |<span data-ttu-id="edec9-370">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="edec9-370">Data</span></span>|<span data-ttu-id="edec9-371">sessionid=[[$Context.SessionId]]</span><span class="sxs-lookup"><span data-stu-id="edec9-371">sessionid=[[$Context.SessionId]]</span></span>|  

   <span data-ttu-id="edec9-372">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call-3.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="edec9-372">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call-3.png "Create an action call in Unified Service Desk")</span></span>  

9. <span data-ttu-id="edec9-373">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="edec9-373">Click **Save**.</span></span>  

<a name="Step7"></a>   
## <a name="step-7-create-an-action-call-to-display-the-agent-script"></a><span data-ttu-id="edec9-374">Bước 7: Tạo cuộc gọi hành động để hiển thị mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="edec9-374">Step 7: Create an action call to display the agent script</span></span>  
 <span data-ttu-id="edec9-375">Trong bước này, tạo cuộc gọi hành động để hiển thị mã lệnh tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="edec9-375">In this step, create an action call to display the agent script.</span></span>  

1. <span data-ttu-id="edec9-376">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="edec9-376">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="edec9-377">Click **Action Calls**.</span><span class="sxs-lookup"><span data-stu-id="edec9-377">Click **Action Calls**.</span></span>  

4. <span data-ttu-id="edec9-378">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="edec9-378">Click **New**.</span></span>  

5. <span data-ttu-id="edec9-379">On the **New Action Call** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="edec9-379">On the **New Action Call** page, specify the following values.</span></span>  

   |<span data-ttu-id="edec9-380">Trường</span><span class="sxs-lookup"><span data-stu-id="edec9-380">Field</span></span>|<span data-ttu-id="edec9-381">Giá trị</span><span class="sxs-lookup"><span data-stu-id="edec9-381">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="edec9-382">Tên</span><span class="sxs-lookup"><span data-stu-id="edec9-382">Name</span></span>|<span data-ttu-id="edec9-383">Các cuộc gọi hành động contoso: Tải mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="edec9-383">Contoso Action Call: Load Agent Script</span></span>|  
   |<span data-ttu-id="edec9-384">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="edec9-384">Hosted Control</span></span>|<span data-ttu-id="edec9-385">Mã lệnh tổng đài viên Contoso</span><span class="sxs-lookup"><span data-stu-id="edec9-385">Contoso Agent Scripting</span></span>|  
   |<span data-ttu-id="edec9-386">Hành động</span><span class="sxs-lookup"><span data-stu-id="edec9-386">Action</span></span>|<span data-ttu-id="edec9-387">Đi đến tác vụ</span><span class="sxs-lookup"><span data-stu-id="edec9-387">GoToTask</span></span>|  
   |<span data-ttu-id="edec9-388">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="edec9-388">Data</span></span>|<span data-ttu-id="edec9-389">Contoso: Welcome to Account Session</span><span class="sxs-lookup"><span data-stu-id="edec9-389">Contoso: Welcome to Account Session</span></span>|  

   <span data-ttu-id="edec9-390">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call-4.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="edec9-390">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call-4.png "Create an action call in Unified Service Desk")</span></span>  

6. <span data-ttu-id="edec9-391">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="edec9-391">Click **Save**.</span></span>  

<a name="Step8"></a>   
## <a name="step-8-display-the-agent-script-when-the-account-record-is-displayed-in-a-session"></a><span data-ttu-id="edec9-392">Bước 8: Hiển thị mã lệnh tổng đài viên khi hồ sơ tài khoản được hiển thị trong phiên.</span><span class="sxs-lookup"><span data-stu-id="edec9-392">Step 8: Display the agent script when the account record is displayed in a session</span></span>  
 <span data-ttu-id="edec9-393">Trong bước này, thêm cuộc gọi hành động đã tạo ở bước trước vào sự kiện **BrowserDocumentComplete** trên kiểm soát tổ chức **Phiên tài khoản Contoso** để sau khi được tải, các cuộc gọi hành động được thực hiện để tải mã lệnh tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="edec9-393">In this step, add the action call created in the previous step to the **BrowserDocumentComplete** event on the **Contoso Account Session** hosted control so that after it’s loaded, the action call is executed to load the agent script.</span></span> <span data-ttu-id="edec9-394">The **Contoso Account Session** hosted control was created in [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="edec9-394">The **Contoso Account Session** hosted control was created in [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md).</span></span>  

1. <span data-ttu-id="edec9-395">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="edec9-395">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="edec9-396">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="edec9-396">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="edec9-397">Tìm kiếm kiểm soát tổ chức **Phiên tài khoản Contoso** và bấm vào nó để mở định nghĩa kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="edec9-397">Search for the **Contoso Account Session** hosted control, and click it to open the hosted control definition.</span></span>  

5. <span data-ttu-id="edec9-398">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Phiên tài khoản Contoso**, sau đó nhấp vào **Sự kiện**.</span><span class="sxs-lookup"><span data-stu-id="edec9-398">On the nav bar, click the down arrow next to **Contoso Account Session**, and then click **Events**.</span></span>  

   <span data-ttu-id="edec9-399">![Configure events for a hosted control](../unified-service-desk/media/usd-configure-events-hosted-control.png "Configure events for a hosted control")</span><span class="sxs-lookup"><span data-stu-id="edec9-399">![Configure events for a hosted control](../unified-service-desk/media/usd-configure-events-hosted-control.png "Configure events for a hosted control")</span></span>  

6. <span data-ttu-id="edec9-400">Trên trang sự kiện, bấm vào **BrowserDocumentComplete**.</span><span class="sxs-lookup"><span data-stu-id="edec9-400">On the events page, click **BrowserDocumentComplete**.</span></span>  

7. <span data-ttu-id="edec9-401">On the **BrowserDocumentComplete** page, click **+** in the **Active Actions** area to add an action call to the event.</span><span class="sxs-lookup"><span data-stu-id="edec9-401">On the **BrowserDocumentComplete** page, click **+** in the **Active Actions** area to add an action call to the event.</span></span>  

8. <span data-ttu-id="edec9-402">Trong hộp tìm kiếm, nhập “`Contoso Action Call: Load Agent Script`” và nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="edec9-402">In the search box, type “`Contoso Action Call: Load Agent Script`”, and press ENTER or click the search icon.</span></span>  

9. <span data-ttu-id="edec9-403">Trong kết quả tìm kiếm, bấm vào **Cuộc gọi hành động Contoso: Tải mã lệnh tổng đài viên** để thêm.</span><span class="sxs-lookup"><span data-stu-id="edec9-403">In the search results, click **Contoso Action Call: Load Agent Script** to add it.</span></span>  

10. <span data-ttu-id="edec9-404">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="edec9-404">Click **Save**.</span></span>  

<a name="Step9"></a>   
## <a name="step-9-add-the-controls-to-the-configuration"></a><span data-ttu-id="edec9-405">Bước 9: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="edec9-405">Step 9: Add the controls to the configuration</span></span>  
 <span data-ttu-id="edec9-406">Trong bước này, thêm cuộc gọi hành động, mã lệnh tổng đài viên, kiểm soát tổ chức và nguyên tắc điều hướng cửa sổ mà bạn đã cấu hình trong cách này thành **Cấu hình Contoso** để hiển thị các kiểm soát này cho người dùng được chỉ định cho cấu hình này.</span><span class="sxs-lookup"><span data-stu-id="edec9-406">In this step, add the action calls, agent script, hosted controls, and window navigation rule that you configured in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span></span> <span data-ttu-id="edec9-407">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="edec9-407">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span>  

 <span data-ttu-id="edec9-408">Add the following to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="edec9-408">Add the following to **Contoso Configuration**.</span></span>  

|<span data-ttu-id="edec9-409">Tên kiểm soát</span><span class="sxs-lookup"><span data-stu-id="edec9-409">Control name</span></span>|<span data-ttu-id="edec9-410">Loại kiểm soát</span><span class="sxs-lookup"><span data-stu-id="edec9-410">Control type</span></span>|  
|------------------|------------------|  
|<span data-ttu-id="edec9-411">Cuộc gọi hành động contoso: Tạo trường hợp</span><span class="sxs-lookup"><span data-stu-id="edec9-411">Contoso Action Call: Create Case</span></span>|<span data-ttu-id="edec9-412">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="edec9-412">Action call</span></span>|  
|<span data-ttu-id="edec9-413">Cuộc gọi hành động Contoso: Hiển thị trường hợp hiện có</span><span class="sxs-lookup"><span data-stu-id="edec9-413">Contoso Action Call: Display Existing Cases</span></span>|<span data-ttu-id="edec9-414">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="edec9-414">Action Call</span></span>|  
|<span data-ttu-id="edec9-415">Cuộc gọi hành động Contoso: Tập trung vào trường hợp hiện có</span><span class="sxs-lookup"><span data-stu-id="edec9-415">Contoso Action Call: Set Focus on Existing Cases</span></span>|<span data-ttu-id="edec9-416">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="edec9-416">Action Call</span></span>|  
|<span data-ttu-id="edec9-417">Các cuộc gọi hành động contoso: Đóng phiên</span><span class="sxs-lookup"><span data-stu-id="edec9-417">Contoso Action Call: Close Session</span></span>|<span data-ttu-id="edec9-418">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="edec9-418">Action Call</span></span>|  
|<span data-ttu-id="edec9-419">Các cuộc gọi hành động contoso: Tải mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="edec9-419">Contoso Action Call: Load Agent Script</span></span>|<span data-ttu-id="edec9-420">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="edec9-420">Action Call</span></span>|  
|<span data-ttu-id="edec9-421">Contoso: Chào mừng bạn đến với Phiên tài khoản</span><span class="sxs-lookup"><span data-stu-id="edec9-421">Contoso: Welcome to Account Session</span></span>|<span data-ttu-id="edec9-422">Mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="edec9-422">Agent Script</span></span>|  
|<span data-ttu-id="edec9-423">Mã lệnh tổng đài viên Contoso</span><span class="sxs-lookup"><span data-stu-id="edec9-423">Contoso Agent Scripting</span></span>|<span data-ttu-id="edec9-424">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="edec9-424">Hosted Control</span></span>|  
|<span data-ttu-id="edec9-425">Biểu mẫu trường hợp mới</span><span class="sxs-lookup"><span data-stu-id="edec9-425">Contoso new case form</span></span>|<span data-ttu-id="edec9-426">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="edec9-426">Hosted Control</span></span>|  
|<span data-ttu-id="edec9-427">Trường hợp sẵn có Contoso cho tài khoản</span><span class="sxs-lookup"><span data-stu-id="edec9-427">Contoso existing cases for an account</span></span>|<span data-ttu-id="edec9-428">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="edec9-428">Hosted Control</span></span>|  
|<span data-ttu-id="edec9-429">Trường hợp mới Contoso cho nguyên tắc phiên tài khoản</span><span class="sxs-lookup"><span data-stu-id="edec9-429">Contoso New Case for Account Session Rule</span></span>|<span data-ttu-id="edec9-430">Window navigation rule</span><span class="sxs-lookup"><span data-stu-id="edec9-430">Window navigation rule</span></span>|  

 <span data-ttu-id="edec9-431">To add a control to the configuration:</span><span class="sxs-lookup"><span data-stu-id="edec9-431">To add a control to the configuration:</span></span>  

1. <span data-ttu-id="edec9-432">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="edec9-432">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="edec9-433">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="edec9-433">Click **Configuration**.</span></span>  

4. <span data-ttu-id="edec9-434">Click **Contoso Configuration** to open the definition.</span><span class="sxs-lookup"><span data-stu-id="edec9-434">Click **Contoso Configuration** to open the definition.</span></span>  

5. <span data-ttu-id="edec9-435">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="edec9-435">On the nav bar, click the down arrow next to **Contoso Configuration**, and select **Action Calls**.</span></span>  

6. <span data-ttu-id="edec9-436">Trên trang tiếp theo, bấm vào **Thêm cuộc gọi hành động hiện có**, nhập "Cuộc gọi hành động Contoso" trong thanh tìm kiếm, sau đó nhấn ENTER hoặc nhấp biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="edec9-436">On the next page, click **Add Existing Action Call**, type “Contoso Action Call” in the search bar, and then press ENTER or click the search icon.</span></span>  

7. <span data-ttu-id="edec9-437">Chọn năm cuộc gọi hành động từ hộp kết quả tìm kiếm để thêm chúng vào **Cấu hình Contoso**.</span><span class="sxs-lookup"><span data-stu-id="edec9-437">Select the five action calls from the search results box to add them to **Contoso Configuration**.</span></span>  

8. <span data-ttu-id="edec9-438">Tương tự, thêm mã lệnh tổng đài viên, kiểm soát tổ chức và nguyên tắc điều hướng cửa sổ bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Mã lệnh tổng đài viên** **Kiểm soát tổ chức** và **Nguyên tắc điều hướng cửa sổ** lần lượt.</span><span class="sxs-lookup"><span data-stu-id="edec9-438">Similarly, add the agent script, hosted controls, and window navigation rule by clicking the down arrow next to **Contoso Configuration**, and clicking **Agent Scripts** **Hosted Controls** and **Window navigation Rules** respectively.</span></span>  

9. <span data-ttu-id="edec9-439">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="edec9-439">Click **Save**.</span></span>  

<a name="Step10"></a>   
## <a name="step-10-test-the-application"></a><span data-ttu-id="edec9-440">Bước 10: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="edec9-440">Step 10: Test the application</span></span>  

1. <span data-ttu-id="edec9-441">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] by using the same user credentials that is assigned to Contoso Configuration in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="edec9-441">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] by using the same user credentials that is assigned to Contoso Configuration in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span> <span data-ttu-id="edec9-442">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to CRM instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)</span><span class="sxs-lookup"><span data-stu-id="edec9-442">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to CRM instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)</span></span>  

2. <span data-ttu-id="edec9-443">Click the down arrow next to the **SEARCH** button in the toolbar, and then click **Account** to display the account records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="edec9-443">Click the down arrow next to the **SEARCH** button in the toolbar, and then click **Account** to display the account records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span>  

3. <span data-ttu-id="edec9-444">Nhấp vào trình mở rộng để hiển thị bảng điều khiển bên trái.</span><span class="sxs-lookup"><span data-stu-id="edec9-444">Click the expander to display the left pane.</span></span>  

   <span data-ttu-id="edec9-445">![Choose the expander in Unified Service Desk](../unified-service-desk/media/usd-choose-expander.png "Choose the expander in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="edec9-445">![Choose the expander in Unified Service Desk](../unified-service-desk/media/usd-choose-expander.png "Choose the expander in Unified Service Desk")</span></span>  

4. <span data-ttu-id="edec9-446">Nhấp vào bất kỳ hồ sơ tài khoản nào để hiện thị thông tin tài khoản tương ứng trong phiên.</span><span class="sxs-lookup"><span data-stu-id="edec9-446">Click on any of the account records to display the respective account information in a session.</span></span> <span data-ttu-id="edec9-447">Trong bảng điều khiển bên trái, mã lệnh tổng đài viên **Contoso: Chào mừng bạn đến với phiên tài khoản** xuất hiện.</span><span class="sxs-lookup"><span data-stu-id="edec9-447">In the left pane, the **Contoso: Welcome to Account Session** agent script appears.</span></span>  

   <span data-ttu-id="edec9-448">![Agent script in Unified Service Desk](../unified-service-desk/media/usd-agent-script.png "Agent script in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="edec9-448">![Agent script in Unified Service Desk](../unified-service-desk/media/usd-agent-script.png "Agent script in Unified Service Desk")</span></span>  

5. <span data-ttu-id="edec9-449">Trong mã lệnh tổng đài viên:</span><span class="sxs-lookup"><span data-stu-id="edec9-449">In the agent script:</span></span>  

   1.  <span data-ttu-id="edec9-450">Bấm vào **trường hợp mới** để mở biểu mẫu trường hợp mới với giá trị nhập sẵn (trong hộp màu đỏ) từ hồ sơ tài khoản hiện tại.</span><span class="sxs-lookup"><span data-stu-id="edec9-450">Click **New case** to open a new case form with pre-populated values (in the red box) from the current account record.</span></span>  

   <span data-ttu-id="edec9-451">![New case form using the agent script](../unified-service-desk/media/usd-new-case-form-agent-script.png "New case form using the agent script")</span><span class="sxs-lookup"><span data-stu-id="edec9-451">![New case form using the agent script](../unified-service-desk/media/usd-new-case-form-agent-script.png "New case form using the agent script")</span></span>  

   2.  <span data-ttu-id="edec9-452">Bấm vào **Hiển thị các trường hợp hiện có** để hiển thị các trường hợp được liên kết cho hồ sơ tài khoản hiện tại.</span><span class="sxs-lookup"><span data-stu-id="edec9-452">Click **Display existing cases** to display the associated cases for the current account record.</span></span>  

   <span data-ttu-id="edec9-453">![Display existing cases for an account](../unified-service-desk/media/usd-show-cases-account.png "Display existing cases for an account")</span><span class="sxs-lookup"><span data-stu-id="edec9-453">![Display existing cases for an account](../unified-service-desk/media/usd-show-cases-account.png "Display existing cases for an account")</span></span>  

   3.  <span data-ttu-id="edec9-454">Bấm vào **đóng phiên** để đóng phiên hiện tại.</span><span class="sxs-lookup"><span data-stu-id="edec9-454">Click **Close session** to close the current session.</span></span>  

<a name="Conclusion"></a>   
## <a name="conclusion"></a><span data-ttu-id="edec9-455">Kết luận</span><span class="sxs-lookup"><span data-stu-id="edec9-455">Conclusion</span></span>  
 <span data-ttu-id="edec9-456">In this walkthrough, you learned how to configure a simple agent script to guide your call center agents.</span><span class="sxs-lookup"><span data-stu-id="edec9-456">In this walkthrough, you learned how to configure a simple agent script to guide your call center agents.</span></span> [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="edec9-457">allows you to create more complex scripts with branching logic that contain child answers and actions.</span><span class="sxs-lookup"><span data-stu-id="edec9-457">allows you to create more complex scripts with branching logic that contain child answers and actions.</span></span> <span data-ttu-id="edec9-458">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span><span class="sxs-lookup"><span data-stu-id="edec9-458">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span></span>  

### <a name="see-also"></a><span data-ttu-id="edec9-459">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="edec9-459">See also</span></span>  
 [<span data-ttu-id="edec9-460">Cách 1: Xây dựng ứng dụng tổng đài viên đơn giản</span><span class="sxs-lookup"><span data-stu-id="edec9-460">Walkthrough 1: Build a simple agent application</span></span>](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)   

 [<span data-ttu-id="edec9-461">Cách 2: Hiển thị trang web bên ngoài trong ứng dụng tổng đài viên của bạn</span><span class="sxs-lookup"><span data-stu-id="edec9-461">Walkthrough 2: Display an external webpage in your agent application</span></span>](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md)   

 [<span data-ttu-id="edec9-462">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application</span><span class="sxs-lookup"><span data-stu-id="edec9-462">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application</span></span>](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md)   

 [<span data-ttu-id="edec9-463">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application</span><span class="sxs-lookup"><span data-stu-id="edec9-463">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application</span></span>](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md)   

 [<span data-ttu-id="edec9-464">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span><span class="sxs-lookup"><span data-stu-id="edec9-464">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span></span>](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md)   

 [<span data-ttu-id="edec9-465">Hướng 6: Đặt cấu hình kiểm soát tổ chức trình gỡ lỗi trong ứng dụng tổng đài viên của bạn</span><span class="sxs-lookup"><span data-stu-id="edec9-465">Walkthrough 6: Configure the Debugger hosted control in your agent application</span></span>](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md)   

 [<span data-ttu-id="edec9-466">Unified Service Desk Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="edec9-466">Unified Service Desk Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
