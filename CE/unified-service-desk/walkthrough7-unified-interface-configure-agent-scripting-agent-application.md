---
title: 'Walkthrough 7: Configure agent scripting in your agent application | MicrosoftDocs'
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
ms.assetid: E85F8E08-2C2C-4CC1-90B3-1E9656836B37
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
ms.openlocfilehash: 13c9da83eb9b17d66a5bec436b3e7ced3301c7ad
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387930"
---
# <a name="walkthrough-7-configure-agent-scripting-in-your-agent-application"></a><span data-ttu-id="a92c8-102">Walkthrough 7: Configure agent scripting in your agent application</span><span class="sxs-lookup"><span data-stu-id="a92c8-102">Walkthrough 7: Configure agent scripting in your agent application</span></span>
<span data-ttu-id="a92c8-103">Agent scripting in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] helps to guide your agents during customer interaction.</span><span class="sxs-lookup"><span data-stu-id="a92c8-103">Agent scripting in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] helps to guide your agents during customer interaction.</span></span> <span data-ttu-id="a92c8-104">Cách này trình bày cách tạo mã lệnh tổng đài viên đơn giảm giúp tổng đài viên nhanh chóng tạo trường hợp mới cho tài khoản hoặc tìm các trường hợp hiện có từ ứng dụng tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="a92c8-104">This walkthrough demonstrates how to create a simple agent script that helps the agents quickly create a new case for an account or browse existing cases from the agent application.</span></span> <span data-ttu-id="a92c8-105">Mã lệnh tổng đài viên đã tạo trong cách này được thực hiện khi tổng đài viên dừng một hồ sơ tài khoản để xem, hồ sơ đó được hiển thị trong phiên trong ứng dụng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="a92c8-105">The agent script created in this walkthrough is invoked when the agent pulls up an account record to view, which is displayed in a session in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client.</span></span> <span data-ttu-id="a92c8-106">Mã lệnh cung cấp ba tùy chọn sau:</span><span class="sxs-lookup"><span data-stu-id="a92c8-106">The script provides the following three options:</span></span>  

-   <span data-ttu-id="a92c8-107">Tạo ra một trường hợp cho tài khoản hiện tại</span><span class="sxs-lookup"><span data-stu-id="a92c8-107">Create a case for the current account</span></span>  

-   <span data-ttu-id="a92c8-108">Display existing cases for the current account</span><span class="sxs-lookup"><span data-stu-id="a92c8-108">Display existing cases for the current account</span></span>  

-   <span data-ttu-id="a92c8-109">Close the session</span><span class="sxs-lookup"><span data-stu-id="a92c8-109">Close the session</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="a92c8-110">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="a92c8-110">Prerequisites</span></span>  

- <span data-ttu-id="a92c8-111">You must have completed [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) and [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="a92c8-111">You must have completed [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) and [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md).</span></span> <span data-ttu-id="a92c8-112">The configurations that you completed in those walkthroughs are required in this walkthrough.</span><span class="sxs-lookup"><span data-stu-id="a92c8-112">The configurations that you completed in those walkthroughs are required in this walkthrough.</span></span>  

- <span data-ttu-id="a92c8-113">Cách này giả định rằng bạn sẽ sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="a92c8-113">This walkthrough assumes that you’ll be using the same user credential that you used in walkthrough 1 to sign in to the agent application.</span></span> <span data-ttu-id="a92c8-114">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-114">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a92c8-115">[Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)</span><span class="sxs-lookup"><span data-stu-id="a92c8-115">[Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)</span></span>  

- <span data-ttu-id="a92c8-116">You must know be familiar with the following concepts in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="a92c8-116">You must know be familiar with the following concepts in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  

  - <span data-ttu-id="a92c8-117">**Agent Scripting** type of hosted control and how to configure agent scripts.</span><span class="sxs-lookup"><span data-stu-id="a92c8-117">**Agent Scripting** type of hosted control and how to configure agent scripts.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a92c8-118">[Agent Scripting (Hosted Control)](../unified-service-desk/agent-scripting-hosted-control.md) and [Guide customer interactions with agent scripts](../unified-service-desk/guide-customer-interactions-agent-scripts.md)</span><span class="sxs-lookup"><span data-stu-id="a92c8-118">[Agent Scripting (Hosted Control)](../unified-service-desk/agent-scripting-hosted-control.md) and [Guide customer interactions with agent scripts](../unified-service-desk/guide-customer-interactions-agent-scripts.md)</span></span>  

  - <span data-ttu-id="a92c8-119">How to configure [Action calls](../unified-service-desk/action-calls.md)</span><span class="sxs-lookup"><span data-stu-id="a92c8-119">How to configure [Action calls](../unified-service-desk/action-calls.md)</span></span>  

  - <span data-ttu-id="a92c8-120">How to configure window navigation rules.</span><span class="sxs-lookup"><span data-stu-id="a92c8-120">How to configure window navigation rules.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a92c8-121">[Use window navigation rules in Unified Service Desk](../unified-service-desk/use-window-navigation-rules-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="a92c8-121">[Use window navigation rules in Unified Service Desk](../unified-service-desk/use-window-navigation-rules-unified-service-desk.md)</span></span>  

  - <span data-ttu-id="a92c8-122">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span><span class="sxs-lookup"><span data-stu-id="a92c8-122">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a92c8-123">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="a92c8-123">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span></span>  

## <a name="in-this-walkthrough"></a><span data-ttu-id="a92c8-124">In This Walkthrough</span><span class="sxs-lookup"><span data-stu-id="a92c8-124">In This Walkthrough</span></span>  
 [<span data-ttu-id="a92c8-125">Bước 1: Tạo một loại mã lệnh tổng đài viên của kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="a92c8-125">Step 1: Create an Agent Scripting type of hosted control</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step1)  

 [<span data-ttu-id="a92c8-126">Bước 2: Tạo kiểm soát tổ chức để hiển thị biểu mẫu trường hợp mới và trường hợp hiện có</span><span class="sxs-lookup"><span data-stu-id="a92c8-126">Step 2: Create hosted controls to display the new case form and existing cases</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step2)  

 [<span data-ttu-id="a92c8-127">Bước 3: Tạo một tác vụ mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="a92c8-127">Step 3: Create an agent script task</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step3)  

 [<span data-ttu-id="a92c8-128">Bước 4: Thêm câu trả lời, cuộc gọi hành động và nguyên tắc điều hướng cửa sổ để tạo trường hợp từ mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="a92c8-128">Step 4: Add the answer, action call, and window navigation rule for creating a case from the agent script</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step4)  

 [<span data-ttu-id="a92c8-129">Bước 5: Thêm câu trả lời và cuộc gọi hành động để hiển thị trường hợp sẵn có</span><span class="sxs-lookup"><span data-stu-id="a92c8-129">Step 5: Add the answer and action calls for displaying existing cases</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step5)  

 [<span data-ttu-id="a92c8-130">Bước 6: Thêm câu trả lời và cuộc gọi hành động để đóng phiên</span><span class="sxs-lookup"><span data-stu-id="a92c8-130">Step 6: Add the answer and action calls for closing the session</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step6)  

 [<span data-ttu-id="a92c8-131">Bước 7: Tạo cuộc gọi hành động để hiển thị mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="a92c8-131">Step 7: Create an action call to display the agent script</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step7)  

 [<span data-ttu-id="a92c8-132">Bước 8: Hiển thị mã lệnh tổng đài viên khi hồ sơ tài khoản được hiển thị trong phiên.</span><span class="sxs-lookup"><span data-stu-id="a92c8-132">Step 8: Display the agent script when the account record is displayed in a session</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step8)  

 [<span data-ttu-id="a92c8-133">Bước 9: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="a92c8-133">Step 9: Add the controls to the configuration</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step9)  

 [<span data-ttu-id="a92c8-134">Bước 10: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="a92c8-134">Step 10: Test the application</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Step10)  

 [<span data-ttu-id="a92c8-135">Kết luận</span><span class="sxs-lookup"><span data-stu-id="a92c8-135">Conclusion</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md#Conclusion)  

<a name="Step1"></a>   
## <a name="step-1-create-an-agent-scripting-type-of-hosted-control"></a><span data-ttu-id="a92c8-136">Step 1: Create an Agent Scripting type of hosted control</span><span class="sxs-lookup"><span data-stu-id="a92c8-136">Step 1: Create an Agent Scripting type of hosted control</span></span>  
 <span data-ttu-id="a92c8-137">An instance of the **Agent Scripting** type of hosted control must be available in your agent application to display agent scripts.</span><span class="sxs-lookup"><span data-stu-id="a92c8-137">An instance of the **Agent Scripting** type of hosted control must be available in your agent application to display agent scripts.</span></span>  

1. <span data-ttu-id="a92c8-138">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="a92c8-138">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="a92c8-139">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-139">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="a92c8-140">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-140">Click **New**.</span></span>  

5. <span data-ttu-id="a92c8-141">On the **New Hosted Control** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="a92c8-141">On the **New Hosted Control** page, specify the following values.</span></span>  

   |<span data-ttu-id="a92c8-142">Trường</span><span class="sxs-lookup"><span data-stu-id="a92c8-142">Field</span></span>|<span data-ttu-id="a92c8-143">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a92c8-143">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="a92c8-144">Tên</span><span class="sxs-lookup"><span data-stu-id="a92c8-144">Name</span></span>|<span data-ttu-id="a92c8-145">Mã lệnh tổng đài viên Contoso</span><span class="sxs-lookup"><span data-stu-id="a92c8-145">Contoso Agent Scripting</span></span>|  
   |<span data-ttu-id="a92c8-146">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="a92c8-146">USD Component Type</span></span>|<span data-ttu-id="a92c8-147">Mã lệnh của tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="a92c8-147">Agent Scripting</span></span>|  
   |<span data-ttu-id="a92c8-148">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="a92c8-148">Display Group</span></span>|<span data-ttu-id="a92c8-149">Bảng điều khiển quy trình làm việc</span><span class="sxs-lookup"><span data-stu-id="a92c8-149">WorkflowPanel</span></span>|  

   <span data-ttu-id="a92c8-150">![Create an Agent Scripting hosted control](../unified-service-desk/media/usd-create-agent-scripting-hosted-control-unified-interface.png "Create an Agent Scripting hosted control")</span><span class="sxs-lookup"><span data-stu-id="a92c8-150">![Create an Agent Scripting hosted control](../unified-service-desk/media/usd-create-agent-scripting-hosted-control-unified-interface.png "Create an Agent Scripting hosted control")</span></span> 

6. <span data-ttu-id="a92c8-151">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-151">Click **Save**.</span></span>  

<a name="Step2"></a>   
## <a name="step-2-create-hosted-controls-to-display-the-new-case-form-and-existing-cases"></a><span data-ttu-id="a92c8-152">Step 2: Create hosted controls to display the new case form and existing cases</span><span class="sxs-lookup"><span data-stu-id="a92c8-152">Step 2: Create hosted controls to display the new case form and existing cases</span></span>  
 <span data-ttu-id="a92c8-153">In this step, you’ll create two hosted controls of Unified Interface Page type to display the new case creation form and existing cases for the current account.</span><span class="sxs-lookup"><span data-stu-id="a92c8-153">In this step, you’ll create two hosted controls of Unified Interface Page type to display the new case creation form and existing cases for the current account.</span></span>  

1. <span data-ttu-id="a92c8-154">Trên trang kiểm soát tổ chức, bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-154">On the hosted controls page, click **New**.</span></span>  

2. <span data-ttu-id="a92c8-155">Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="a92c8-155">On the **New Hosted Control** page, specify the following values:</span></span>  

   |<span data-ttu-id="a92c8-156">Trường</span><span class="sxs-lookup"><span data-stu-id="a92c8-156">Field</span></span>|<span data-ttu-id="a92c8-157">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a92c8-157">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="a92c8-158">Tên</span><span class="sxs-lookup"><span data-stu-id="a92c8-158">Name</span></span>|<span data-ttu-id="a92c8-159">Contoso new case form</span><span class="sxs-lookup"><span data-stu-id="a92c8-159">Contoso new case form</span></span>|  
   |<span data-ttu-id="a92c8-160">Tên Hiển thị</span><span class="sxs-lookup"><span data-stu-id="a92c8-160">Display Name</span></span>|<span data-ttu-id="a92c8-161">Trường hợp mới</span><span class="sxs-lookup"><span data-stu-id="a92c8-161">New Case</span></span>|  
   |<span data-ttu-id="a92c8-162">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="a92c8-162">USD Component Type</span></span>|<span data-ttu-id="a92c8-163">Unified Interface Page</span><span class="sxs-lookup"><span data-stu-id="a92c8-163">Unified Interface Page</span></span>|  
   |<span data-ttu-id="a92c8-164">Allow Multiple Pages</span><span class="sxs-lookup"><span data-stu-id="a92c8-164">Allow Multiple Pages</span></span>|<span data-ttu-id="a92c8-165">Không</span><span class="sxs-lookup"><span data-stu-id="a92c8-165">No</span></span>|
   |<span data-ttu-id="a92c8-166">Application is Global</span><span class="sxs-lookup"><span data-stu-id="a92c8-166">Application is Global</span></span>|<span data-ttu-id="a92c8-167">Không được chọn</span><span class="sxs-lookup"><span data-stu-id="a92c8-167">Not checked</span></span>|  
   |<span data-ttu-id="a92c8-168">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="a92c8-168">Display Group</span></span>|<span data-ttu-id="a92c8-169">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="a92c8-169">MainPanel</span></span>|  

   <span data-ttu-id="a92c8-170">![Create a Unified Interface Page hosted control](../unified-service-desk/media/usd-create-page-hosted-control-2-case-form-unified-interface.png "Create a Unified Interface Page hosted control")</span><span class="sxs-lookup"><span data-stu-id="a92c8-170">![Create a Unified Interface Page hosted control](../unified-service-desk/media/usd-create-page-hosted-control-2-case-form-unified-interface.png "Create a Unified Interface Page hosted control")</span></span> 

3. <span data-ttu-id="a92c8-171">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-171">Click **Save**.</span></span>  

4. <span data-ttu-id="a92c8-172">On the hosted controls page, click **New** to create another hosted control.</span><span class="sxs-lookup"><span data-stu-id="a92c8-172">On the hosted controls page, click **New** to create another hosted control.</span></span>  

5. <span data-ttu-id="a92c8-173">Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="a92c8-173">On the **New Hosted Control** page, specify the following values:</span></span>  

   |<span data-ttu-id="a92c8-174">Trường</span><span class="sxs-lookup"><span data-stu-id="a92c8-174">Field</span></span>|<span data-ttu-id="a92c8-175">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a92c8-175">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="a92c8-176">Tên</span><span class="sxs-lookup"><span data-stu-id="a92c8-176">Name</span></span>|<span data-ttu-id="a92c8-177">Contoso existing cases for an account</span><span class="sxs-lookup"><span data-stu-id="a92c8-177">Contoso existing cases for an account</span></span>|  
   |<span data-ttu-id="a92c8-178">Tên Hiển thị</span><span class="sxs-lookup"><span data-stu-id="a92c8-178">Display Name</span></span>|<span data-ttu-id="a92c8-179">Trường hợp cho [[$Context.name]]</span><span class="sxs-lookup"><span data-stu-id="a92c8-179">Cases for [[$Context.name]]</span></span><br> <span data-ttu-id="a92c8-180">**Note:**  We are using the replacement parameter to dynamically display the name of the current account from the execution context as the hosted control display name.</span><span class="sxs-lookup"><span data-stu-id="a92c8-180">**Note:**  We are using the replacement parameter to dynamically display the name of the current account from the execution context as the hosted control display name.</span></span>|  
   |<span data-ttu-id="a92c8-181">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="a92c8-181">USD Component Type</span></span>|<span data-ttu-id="a92c8-182">Unified Interface Page</span><span class="sxs-lookup"><span data-stu-id="a92c8-182">Unified Interface Page</span></span>|  
   |<span data-ttu-id="a92c8-183">Allow Multiple Pages</span><span class="sxs-lookup"><span data-stu-id="a92c8-183">Allow Multiple Pages</span></span>|<span data-ttu-id="a92c8-184">Không</span><span class="sxs-lookup"><span data-stu-id="a92c8-184">No</span></span>|
   |<span data-ttu-id="a92c8-185">Application is Global</span><span class="sxs-lookup"><span data-stu-id="a92c8-185">Application is Global</span></span>|<span data-ttu-id="a92c8-186">Không được chọn</span><span class="sxs-lookup"><span data-stu-id="a92c8-186">Not checked</span></span>|  
   |<span data-ttu-id="a92c8-187">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="a92c8-187">Display Group</span></span>|<span data-ttu-id="a92c8-188">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="a92c8-188">MainPanel</span></span>|  

   <span data-ttu-id="a92c8-189">![Create a Unified Interface Page hosted control](../unified-service-desk/media/usd-create-agent-script-task-existing-case-form-account-unified-interface.png "Create a Unified Interface Page hosted control")</span><span class="sxs-lookup"><span data-stu-id="a92c8-189">![Create a Unified Interface Page hosted control](../unified-service-desk/media/usd-create-agent-script-task-existing-case-form-account-unified-interface.png "Create a Unified Interface Page hosted control")</span></span>  

6. <span data-ttu-id="a92c8-190">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-190">Click **Save**.</span></span>  

<a name="Step3"></a>   
## <a name="step-3-create-an-agent-script-task"></a><span data-ttu-id="a92c8-191">Step 3: Create an agent script task</span><span class="sxs-lookup"><span data-stu-id="a92c8-191">Step 3: Create an agent script task</span></span>  
 <span data-ttu-id="a92c8-192">Create an agent script task to display when an account record is displayed in a session.</span><span class="sxs-lookup"><span data-stu-id="a92c8-192">Create an agent script task to display when an account record is displayed in a session.</span></span>  

1. <span data-ttu-id="a92c8-193">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="a92c8-193">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="a92c8-194">Click **Agent Scripts**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-194">Click **Agent Scripts**.</span></span>  

4. <span data-ttu-id="a92c8-195">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-195">Click **New**.</span></span>  

5. <span data-ttu-id="a92c8-196">On the **New Agent Script Task** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="a92c8-196">On the **New Agent Script Task** page, specify the following values:</span></span>  

   |<span data-ttu-id="a92c8-197">Trường</span><span class="sxs-lookup"><span data-stu-id="a92c8-197">Field</span></span>|<span data-ttu-id="a92c8-198">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a92c8-198">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="a92c8-199">Tên</span><span class="sxs-lookup"><span data-stu-id="a92c8-199">Name</span></span>|<span data-ttu-id="a92c8-200">Contoso: Chào mừng bạn đến với Phiên tài khoản</span><span class="sxs-lookup"><span data-stu-id="a92c8-200">Contoso: Welcome to Account Session</span></span>|  
   |<span data-ttu-id="a92c8-201">Bắt đầu nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="a92c8-201">Start Task</span></span>|<span data-ttu-id="a92c8-202">No</span><span class="sxs-lookup"><span data-stu-id="a92c8-202">No</span></span>|  
   |<span data-ttu-id="a92c8-203">Văn bản mã lệnh</span><span class="sxs-lookup"><span data-stu-id="a92c8-203">ScriptText</span></span>|<span data-ttu-id="a92c8-204">Chào mừng bạn đến [[$Context.name]].</span><span class="sxs-lookup"><span data-stu-id="a92c8-204">Welcome [[$Context.name]].</span></span> <span data-ttu-id="a92c8-205">Tên tôi là [[$User.firstname]].</span><span class="sxs-lookup"><span data-stu-id="a92c8-205">My name is [[$User.firstname]].</span></span> <span data-ttu-id="a92c8-206">Is this call regarding a new or an existing service request?</span><span class="sxs-lookup"><span data-stu-id="a92c8-206">Is this call regarding a new or an existing service request?</span></span><br><span data-ttu-id="a92c8-207">**Note:**  We are using replacement parameters to dynamically display the account name and the current agent’s name to the agent at runtime.</span><span class="sxs-lookup"><span data-stu-id="a92c8-207">**Note:**  We are using replacement parameters to dynamically display the account name and the current agent’s name to the agent at runtime.</span></span>|  
   |<span data-ttu-id="a92c8-208">Hướng dẫn</span><span class="sxs-lookup"><span data-stu-id="a92c8-208">Instructions</span></span>|<span data-ttu-id="a92c8-209">Based on the customer response, click one of the tasks below.</span><span class="sxs-lookup"><span data-stu-id="a92c8-209">Based on the customer response, click one of the tasks below.</span></span>|  

   <span data-ttu-id="a92c8-210">![Create an agent script task](../unified-service-desk/media/usd-create-new-agent-script-task-2-unified-interface.png "Create an agent script task")</span><span class="sxs-lookup"><span data-stu-id="a92c8-210">![Create an agent script task](../unified-service-desk/media/usd-create-new-agent-script-task-2-unified-interface.png "Create an agent script task")</span></span>

6. <span data-ttu-id="a92c8-211">Click **Save** to create the agent script.</span><span class="sxs-lookup"><span data-stu-id="a92c8-211">Click **Save** to create the agent script.</span></span>  

<a name="Step4"></a>   
## <a name="step-4-add-the-answer-action-call-and-window-navigation-rule-for-creating-a-case-from-the-agent-script"></a><span data-ttu-id="a92c8-212">Step 4: Add the answer, action call, and window navigation rule for creating a case from the agent script</span><span class="sxs-lookup"><span data-stu-id="a92c8-212">Step 4: Add the answer, action call, and window navigation rule for creating a case from the agent script</span></span>  
 <span data-ttu-id="a92c8-213">Trong bước này, bạn sẽ tạo ra câu trả lời, cuộc gọi hành động và nguyên tắc điều hướng cửa sổ để hiển thị biểu mẫu trường hợp mới với một số giá trị được xác định trước từ hồ sơ tài khoản đang hiện hoạt.</span><span class="sxs-lookup"><span data-stu-id="a92c8-213">In this step, you’ll create answer, action call, and window navigation rule for displaying a new case form with some prepopulated values from the currently active account record.</span></span>  

1. <span data-ttu-id="a92c8-214">In the **Answers** area of the agent script task that you created in step 4, click **+** to create answer.</span><span class="sxs-lookup"><span data-stu-id="a92c8-214">In the **Answers** area of the agent script task that you created in step 4, click **+** to create answer.</span></span>  

2. <span data-ttu-id="a92c8-215">In the search box, press ENTER or click the search icon, and then click **New** in the search results box.</span><span class="sxs-lookup"><span data-stu-id="a92c8-215">In the search box, press ENTER or click the search icon, and then click **New** in the search results box.</span></span>  

   <span data-ttu-id="a92c8-216">![Create an answer for an agent script task](../unified-service-desk/media/usd-create-answer-agent-script-task-unified-interface.png "Create an answer for an agent script task")</span><span class="sxs-lookup"><span data-stu-id="a92c8-216">![Create an answer for an agent script task](../unified-service-desk/media/usd-create-answer-agent-script-task-unified-interface.png "Create an answer for an agent script task")</span></span>

3. <span data-ttu-id="a92c8-217">On the **New Agent Script Answer** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="a92c8-217">On the **New Agent Script Answer** page, specify the following values:</span></span>  

   |<span data-ttu-id="a92c8-218">Trường</span><span class="sxs-lookup"><span data-stu-id="a92c8-218">Field</span></span>|<span data-ttu-id="a92c8-219">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a92c8-219">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="a92c8-220">Tên</span><span class="sxs-lookup"><span data-stu-id="a92c8-220">Name</span></span>|<span data-ttu-id="a92c8-221">Contoso: Trường hợp mới</span><span class="sxs-lookup"><span data-stu-id="a92c8-221">Contoso: New case</span></span>|  
   |<span data-ttu-id="a92c8-222">Văn bản câu trả lời</span><span class="sxs-lookup"><span data-stu-id="a92c8-222">Answer Text</span></span>|<span data-ttu-id="a92c8-223">Create a case</span><span class="sxs-lookup"><span data-stu-id="a92c8-223">Create a case</span></span>|  
   |<span data-ttu-id="a92c8-224">Nhiệm vụ được liên kết</span><span class="sxs-lookup"><span data-stu-id="a92c8-224">Linked Task</span></span>|<span data-ttu-id="a92c8-225">Contoso: Welcome to Account Session</span><span class="sxs-lookup"><span data-stu-id="a92c8-225">Contoso: Welcome to Account Session</span></span>|  
   |<span data-ttu-id="a92c8-226">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="a92c8-226">Order</span></span>|<span data-ttu-id="a92c8-227">1</span><span class="sxs-lookup"><span data-stu-id="a92c8-227">1</span></span>|  

   <span data-ttu-id="a92c8-228">![Create an answer in Unified Service Desk](../unified-service-desk/media/usd-create-new-case-agent-script-answer-unified-interface.png "Create an answer in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="a92c8-228">![Create an answer in Unified Service Desk](../unified-service-desk/media/usd-create-new-case-agent-script-answer-unified-interface.png "Create an answer in Unified Service Desk")</span></span>

4. <span data-ttu-id="a92c8-229">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-229">Click **Save**.</span></span>  

5. <span data-ttu-id="a92c8-230">Next, add an action call to this answer to display a new case form for the account when the agent clicks this answer.</span><span class="sxs-lookup"><span data-stu-id="a92c8-230">Next, add an action call to this answer to display a new case form for the account when the agent clicks this answer.</span></span> <span data-ttu-id="a92c8-231">On the nav bar, click the down arrow next to **Contoso: New case**, and select **Actions**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-231">On the nav bar, click the down arrow next to **Contoso: New case**, and select **Actions**.</span></span>  

   <span data-ttu-id="a92c8-232">![Create an action call for the answer](../unified-service-desk/media/usd-create-action-call-answer.png "Create an action call for the answer")</span><span class="sxs-lookup"><span data-stu-id="a92c8-232">![Create an action call for the answer](../unified-service-desk/media/usd-create-action-call-answer.png "Create an action call for the answer")</span></span>  

6. <span data-ttu-id="a92c8-233">On the next page, click **Add Existing Action Call**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-233">On the next page, click **Add Existing Action Call**.</span></span>  

7. <span data-ttu-id="a92c8-234">In the search box, press ENTER or click the search icon, and then click **New** to create an action call.</span><span class="sxs-lookup"><span data-stu-id="a92c8-234">In the search box, press ENTER or click the search icon, and then click **New** to create an action call.</span></span>  

8. <span data-ttu-id="a92c8-235">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="a92c8-235">On the **New Action Call** page, specify the following values:</span></span>  

   |<span data-ttu-id="a92c8-236">Trường</span><span class="sxs-lookup"><span data-stu-id="a92c8-236">Field</span></span>|<span data-ttu-id="a92c8-237">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a92c8-237">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="a92c8-238">Tên</span><span class="sxs-lookup"><span data-stu-id="a92c8-238">Name</span></span>|<span data-ttu-id="a92c8-239">Cuộc gọi hành động contoso: Tạo trường hợp</span><span class="sxs-lookup"><span data-stu-id="a92c8-239">Contoso Action Call: Create Case</span></span>|  
   |<span data-ttu-id="a92c8-240">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="a92c8-240">Order</span></span>|<span data-ttu-id="a92c8-241">1</span><span class="sxs-lookup"><span data-stu-id="a92c8-241">1</span></span>|  
   |<span data-ttu-id="a92c8-242">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="a92c8-242">Hosted Control</span></span>|<span data-ttu-id="a92c8-243">Biểu mẫu trường hợp mới</span><span class="sxs-lookup"><span data-stu-id="a92c8-243">Contoso new case form</span></span>|  
   |<span data-ttu-id="a92c8-244">Hành động</span><span class="sxs-lookup"><span data-stu-id="a92c8-244">Action</span></span>|<span data-ttu-id="a92c8-245">New_CRM_Page</span><span class="sxs-lookup"><span data-stu-id="a92c8-245">New_CRM_Page</span></span>|  
   |<span data-ttu-id="a92c8-246">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="a92c8-246">Data</span></span>|<span data-ttu-id="a92c8-247">LogicalName=incident</span><span class="sxs-lookup"><span data-stu-id="a92c8-247">LogicalName=incident</span></span><br /> <span data-ttu-id="a92c8-248">customerid=EntityReference([[$Context.InitialEntity]],[[$Context.Id]])</span><span class="sxs-lookup"><span data-stu-id="a92c8-248">customerid=EntityReference([[$Context.InitialEntity]],[[$Context.Id]])</span></span>  <br /> <span data-ttu-id="a92c8-249">customeridname=[[$Context.name]]</span><span class="sxs-lookup"><span data-stu-id="a92c8-249">customeridname=[[$Context.name]]</span></span> <br /> <span data-ttu-id="a92c8-250">primarycontactid=[[$Context.primarycontactid.id]+]</span><span class="sxs-lookup"><span data-stu-id="a92c8-250">primarycontactid=[[$Context.primarycontactid.id]+]</span></span>  <br /> <span data-ttu-id="a92c8-251">primarycontactidname=[[$Context.primarycontactid.name]+]</span><span class="sxs-lookup"><span data-stu-id="a92c8-251">primarycontactidname=[[$Context.primarycontactid.name]+]</span></span><br><span data-ttu-id="a92c8-252">**Note:**  The new case form will be populated with the current account record data to help the agent quickly create a case for the customer.</span><span class="sxs-lookup"><span data-stu-id="a92c8-252">**Note:**  The new case form will be populated with the current account record data to help the agent quickly create a case for the customer.</span></span>|  

   <span data-ttu-id="a92c8-253">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-new-agent-script-answer-create-case-new-action-call-unified-interface.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="a92c8-253">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-new-agent-script-answer-create-case-new-action-call-unified-interface.png "Create an action call in Unified Service Desk")</span></span> 

9. <span data-ttu-id="a92c8-254">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-254">Click **Save**.</span></span>  

10. <span data-ttu-id="a92c8-255">Next, create a window navigation rule to display the new case form.</span><span class="sxs-lookup"><span data-stu-id="a92c8-255">Next, create a window navigation rule to display the new case form.</span></span> [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)] 

11. <span data-ttu-id="a92c8-256">Click **Window Navigation Rules**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-256">Click **Window Navigation Rules**.</span></span>  

12. <span data-ttu-id="a92c8-257">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-257">Click **New**.</span></span>  

13. <span data-ttu-id="a92c8-258">On the **New Window Navigation Rule** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="a92c8-258">On the **New Window Navigation Rule** page, specify the following values.</span></span>  

    |<span data-ttu-id="a92c8-259">Trường</span><span class="sxs-lookup"><span data-stu-id="a92c8-259">Field</span></span>|<span data-ttu-id="a92c8-260">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a92c8-260">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="a92c8-261">Tên</span><span class="sxs-lookup"><span data-stu-id="a92c8-261">Name</span></span>|<span data-ttu-id="a92c8-262">Trường hợp mới Contoso cho nguyên tắc phiên tài khoản</span><span class="sxs-lookup"><span data-stu-id="a92c8-262">Contoso New Case for Account Session Rule</span></span>|  
    |<span data-ttu-id="a92c8-263">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="a92c8-263">Order</span></span>|<span data-ttu-id="a92c8-264">20</span><span class="sxs-lookup"><span data-stu-id="a92c8-264">20</span></span>|  
    |<span data-ttu-id="a92c8-265">Từ</span><span class="sxs-lookup"><span data-stu-id="a92c8-265">From</span></span>|<span data-ttu-id="a92c8-266">Contoso new case form</span><span class="sxs-lookup"><span data-stu-id="a92c8-266">Contoso new case form</span></span>|  
    |<span data-ttu-id="a92c8-267">Thực thể</span><span class="sxs-lookup"><span data-stu-id="a92c8-267">Entity</span></span>|<span data-ttu-id="a92c8-268">sự cố</span><span class="sxs-lookup"><span data-stu-id="a92c8-268">incident</span></span>|  
    |<span data-ttu-id="a92c8-269">Loại định tuyến</span><span class="sxs-lookup"><span data-stu-id="a92c8-269">Route Type</span></span>|<span data-ttu-id="a92c8-270">In Place</span><span class="sxs-lookup"><span data-stu-id="a92c8-270">In Place</span></span>|  
    |<span data-ttu-id="a92c8-271">Điểm đến</span><span class="sxs-lookup"><span data-stu-id="a92c8-271">Destination</span></span>|<span data-ttu-id="a92c8-272">Thẻ</span><span class="sxs-lookup"><span data-stu-id="a92c8-272">Tab</span></span>|  
    |<span data-ttu-id="a92c8-273">Hành động</span><span class="sxs-lookup"><span data-stu-id="a92c8-273">Action</span></span>|<span data-ttu-id="a92c8-274">In Place</span><span class="sxs-lookup"><span data-stu-id="a92c8-274">In Place</span></span>|
    |<span data-ttu-id="a92c8-275">Hide Command Bar</span><span class="sxs-lookup"><span data-stu-id="a92c8-275">Hide Command Bar</span></span>|<span data-ttu-id="a92c8-276">Không</span><span class="sxs-lookup"><span data-stu-id="a92c8-276">No</span></span>|  
    |<span data-ttu-id="a92c8-277">Hide Navigation Bar</span><span class="sxs-lookup"><span data-stu-id="a92c8-277">Hide Navigation Bar</span></span>|<span data-ttu-id="a92c8-278">Có</span><span class="sxs-lookup"><span data-stu-id="a92c8-278">Yes</span></span>|

    <span data-ttu-id="a92c8-279">![Create a window navigation rule](../unified-service-desk/media/usd-new-navigation-rule-case-account-session-rule.png "Create a window navigation rule")</span><span class="sxs-lookup"><span data-stu-id="a92c8-279">![Create a window navigation rule](../unified-service-desk/media/usd-new-navigation-rule-case-account-session-rule.png "Create a window navigation rule")</span></span>  

14. <span data-ttu-id="a92c8-280">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-280">Click **Save**.</span></span>  

<a name="Step5"></a>   
## <a name="step-5-add-the-answer-and-action-calls-for-displaying-existing-cases"></a><span data-ttu-id="a92c8-281">Step 5: Add the answer and action calls for displaying existing cases</span><span class="sxs-lookup"><span data-stu-id="a92c8-281">Step 5: Add the answer and action calls for displaying existing cases</span></span>  
 <span data-ttu-id="a92c8-282">Trong bước này, thêm câu trả lời và cuộc gọi hành động để hiển thị các trường hợp sẵn có cho tài khoản hiện tại.</span><span class="sxs-lookup"><span data-stu-id="a92c8-282">In this step, add answer and action calls for displaying existing cases for the current account.</span></span>  

1. <span data-ttu-id="a92c8-283">In the **Answers** area of the **Contoso: Welcome to Account Session** agent script, click **+** to create an answer.</span><span class="sxs-lookup"><span data-stu-id="a92c8-283">In the **Answers** area of the **Contoso: Welcome to Account Session** agent script, click **+** to create an answer.</span></span>  

2. <span data-ttu-id="a92c8-284">In the search box, press ENTER or click the search icon, and then click **New** in the search results box.</span><span class="sxs-lookup"><span data-stu-id="a92c8-284">In the search box, press ENTER or click the search icon, and then click **New** in the search results box.</span></span>  

3. <span data-ttu-id="a92c8-285">Trên trang **Câu trả lời mã lệnh tổng đài viên mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="a92c8-285">On the **New Agent Script Answer** page, specify the following values.</span></span>  


   |    <span data-ttu-id="a92c8-286">Trường</span><span class="sxs-lookup"><span data-stu-id="a92c8-286">Field</span></span>    |                <span data-ttu-id="a92c8-287">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a92c8-287">Value</span></span>                |
   |-------------|-------------------------------------|
   |    <span data-ttu-id="a92c8-288">Tên</span><span class="sxs-lookup"><span data-stu-id="a92c8-288">Name</span></span>     |       <span data-ttu-id="a92c8-289">Contoso: Trường hợp hiện có</span><span class="sxs-lookup"><span data-stu-id="a92c8-289">Contoso: Existing cases</span></span>       |
   | <span data-ttu-id="a92c8-290">Văn bản câu trả lời</span><span class="sxs-lookup"><span data-stu-id="a92c8-290">Answer Text</span></span> |       <span data-ttu-id="a92c8-291">Hiển thị trường hợp hiện có</span><span class="sxs-lookup"><span data-stu-id="a92c8-291">Display existing cases</span></span>        |
   | <span data-ttu-id="a92c8-292">Nhiệm vụ được liên kết</span><span class="sxs-lookup"><span data-stu-id="a92c8-292">Linked Task</span></span> | <span data-ttu-id="a92c8-293">Contoso: Chào mừng bạn đến với Phiên tài khoản</span><span class="sxs-lookup"><span data-stu-id="a92c8-293">Contoso: Welcome to Account Session</span></span> |
   |    <span data-ttu-id="a92c8-294">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="a92c8-294">Order</span></span>    |                  <span data-ttu-id="a92c8-295">2</span><span class="sxs-lookup"><span data-stu-id="a92c8-295">2</span></span>                  |


4. <span data-ttu-id="a92c8-296">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-296">Click **Save**.</span></span>  

5. <span data-ttu-id="a92c8-297">Tiếp theo, thêm cuộc gọi hành động vào câu trả lời này để hiển thị các trường hợp sẵn có cho tài khoản hiện tại.</span><span class="sxs-lookup"><span data-stu-id="a92c8-297">Next, add an action call to this answer to display the existing cases for the current account.</span></span> <span data-ttu-id="a92c8-298">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Trường hợp hiện có** và chọn **Hành động**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-298">On the nav bar, click the down arrow next to **Contoso: Existing Cases**, and select **Actions**.</span></span>  

6. <span data-ttu-id="a92c8-299">Trên trang tiếp theo, bấm vào **thêm cuộc gọi hành động hiện có**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-299">On the next page, click **Add Existing Action Call**.</span></span>  

7. <span data-ttu-id="a92c8-300">Trong hộp tìm kiếm, nhấn ENTER hoặc nhấp vào biểu tượng tìm kiếm, sau đó nhấp vào **Mới** để tạo cuộc gọi hàn động.</span><span class="sxs-lookup"><span data-stu-id="a92c8-300">In the search box, press ENTER or click the search icon, and then click **New** to create an action call.</span></span>  

8. <span data-ttu-id="a92c8-301">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="a92c8-301">On the **New Action Call** page, specify the following values:</span></span>  


   |     <span data-ttu-id="a92c8-302">Trường</span><span class="sxs-lookup"><span data-stu-id="a92c8-302">Field</span></span>      |                         <span data-ttu-id="a92c8-303">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a92c8-303">Value</span></span>                         |
   |----------------|-------------------------------------------------------|
   |      <span data-ttu-id="a92c8-304">Tên</span><span class="sxs-lookup"><span data-stu-id="a92c8-304">Name</span></span>      |      <span data-ttu-id="a92c8-305">Cuộc gọi hành động Contoso: Hiển thị trường hợp hiện có</span><span class="sxs-lookup"><span data-stu-id="a92c8-305">Contoso Action Call: Display Existing Cases</span></span>      |
   |     <span data-ttu-id="a92c8-306">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="a92c8-306">Order</span></span>      |                           <span data-ttu-id="a92c8-307">1</span><span class="sxs-lookup"><span data-stu-id="a92c8-307">1</span></span>                           |
   | <span data-ttu-id="a92c8-308">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="a92c8-308">Hosted Control</span></span> |         <span data-ttu-id="a92c8-309">Contoso existing cases for an account</span><span class="sxs-lookup"><span data-stu-id="a92c8-309">Contoso existing cases for an account</span></span>         |
   |     <span data-ttu-id="a92c8-310">Hành động</span><span class="sxs-lookup"><span data-stu-id="a92c8-310">Action</span></span>     |                    <span data-ttu-id="a92c8-311">Chế độ xem Liên kết</span><span class="sxs-lookup"><span data-stu-id="a92c8-311">AssociatedView</span></span>                     |
   |      <span data-ttu-id="a92c8-312">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="a92c8-312">Data</span></span>      | <span data-ttu-id="a92c8-313">navItemId=[[$Context.Id]]</span><span class="sxs-lookup"><span data-stu-id="a92c8-313">navItemId=[[$Context.Id]]</span></span> <br /><span data-ttu-id="a92c8-314">type=[[$Context.etn]]</span><span class="sxs-lookup"><span data-stu-id="a92c8-314">type=[[$Context.etn]]</span></span> |


9. <span data-ttu-id="a92c8-315">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-315">Click **Save**.</span></span>  

10. <span data-ttu-id="a92c8-316">Add another action call to set the focus on the new case form.</span><span class="sxs-lookup"><span data-stu-id="a92c8-316">Add another action call to set the focus on the new case form.</span></span> <span data-ttu-id="a92c8-317">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="a92c8-317">On the **New Action Call** page, specify the following values:</span></span>  

    |<span data-ttu-id="a92c8-318">Trường</span><span class="sxs-lookup"><span data-stu-id="a92c8-318">Field</span></span>|<span data-ttu-id="a92c8-319">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a92c8-319">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="a92c8-320">Tên</span><span class="sxs-lookup"><span data-stu-id="a92c8-320">Name</span></span>|<span data-ttu-id="a92c8-321">Cuộc gọi hành động Contoso: Tập trung vào trường hợp hiện có</span><span class="sxs-lookup"><span data-stu-id="a92c8-321">Contoso Action Call: Set Focus on Existing Cases</span></span>|  
    |<span data-ttu-id="a92c8-322">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="a92c8-322">Order</span></span>|<span data-ttu-id="a92c8-323">2</span><span class="sxs-lookup"><span data-stu-id="a92c8-323">2</span></span>|  
    |<span data-ttu-id="a92c8-324">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="a92c8-324">Hosted Control</span></span>|<span data-ttu-id="a92c8-325">Trình quản lý chung contoso</span><span class="sxs-lookup"><span data-stu-id="a92c8-325">Contoso Global Manager</span></span>|  
    |<span data-ttu-id="a92c8-326">Hành động</span><span class="sxs-lookup"><span data-stu-id="a92c8-326">Action</span></span>|<span data-ttu-id="a92c8-327">Hiển thị tab</span><span class="sxs-lookup"><span data-stu-id="a92c8-327">ShowTab</span></span>|  
    |<span data-ttu-id="a92c8-328">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="a92c8-328">Data</span></span>|<span data-ttu-id="a92c8-329">Contoso existing cases for an account</span><span class="sxs-lookup"><span data-stu-id="a92c8-329">Contoso existing cases for an account</span></span>|  

    <span data-ttu-id="a92c8-330">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call-set-focus-existing-cases.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="a92c8-330">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call-set-focus-existing-cases.png "Create an action call in Unified Service Desk")</span></span> 

11. <span data-ttu-id="a92c8-331">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-331">Click **Save**.</span></span>  

<a name="Step6"></a>   
## <a name="step-6-add-the-answer-and-action-calls-for-closing-the-session"></a><span data-ttu-id="a92c8-332">Step 6: Add the answer and action calls for closing the session</span><span class="sxs-lookup"><span data-stu-id="a92c8-332">Step 6: Add the answer and action calls for closing the session</span></span>  
 <span data-ttu-id="a92c8-333">Trong bước này, thêm câu trả lời và cuộc gọi hành động để đóng phiên.</span><span class="sxs-lookup"><span data-stu-id="a92c8-333">In this step, add answer and action calls for closing the current session.</span></span>  

1. <span data-ttu-id="a92c8-334">In the **Answers** area of the **Contoso: Welcome to Account Session** agent script, click **+** to create an answer.</span><span class="sxs-lookup"><span data-stu-id="a92c8-334">In the **Answers** area of the **Contoso: Welcome to Account Session** agent script, click **+** to create an answer.</span></span>  

2. <span data-ttu-id="a92c8-335">In the search box, press ENTER or click the search icon, and then click **New** in the search results box.</span><span class="sxs-lookup"><span data-stu-id="a92c8-335">In the search box, press ENTER or click the search icon, and then click **New** in the search results box.</span></span>  

3. <span data-ttu-id="a92c8-336">Trên trang **Câu trả lời mã lệnh tổng đài viên mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="a92c8-336">On the **New Agent Script Answer** page, specify the following values:</span></span>  


   |    <span data-ttu-id="a92c8-337">Trường</span><span class="sxs-lookup"><span data-stu-id="a92c8-337">Field</span></span>    |                <span data-ttu-id="a92c8-338">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a92c8-338">Value</span></span>                |
   |-------------|-------------------------------------|
   |    <span data-ttu-id="a92c8-339">Tên</span><span class="sxs-lookup"><span data-stu-id="a92c8-339">Name</span></span>     |       <span data-ttu-id="a92c8-340">Contoso: Đóng phiên</span><span class="sxs-lookup"><span data-stu-id="a92c8-340">Contoso: Close session</span></span>        |
   | <span data-ttu-id="a92c8-341">Văn bản câu trả lời</span><span class="sxs-lookup"><span data-stu-id="a92c8-341">Answer Text</span></span> |            <span data-ttu-id="a92c8-342">Đóng phiên</span><span class="sxs-lookup"><span data-stu-id="a92c8-342">Close session</span></span>            |
   | <span data-ttu-id="a92c8-343">Nhiệm vụ được liên kết</span><span class="sxs-lookup"><span data-stu-id="a92c8-343">Linked Task</span></span> | <span data-ttu-id="a92c8-344">Contoso: Chào mừng bạn đến với Phiên tài khoản</span><span class="sxs-lookup"><span data-stu-id="a92c8-344">Contoso: Welcome to Account Session</span></span> |
   |    <span data-ttu-id="a92c8-345">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="a92c8-345">Order</span></span>    |                  <span data-ttu-id="a92c8-346">3</span><span class="sxs-lookup"><span data-stu-id="a92c8-346">3</span></span>                  |


4. <span data-ttu-id="a92c8-347">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-347">Click **Save**.</span></span>  

5. <span data-ttu-id="a92c8-348">Tiếp theo, thêm cuộc gọi hành động cho câu trả lời này để đóng phiên.</span><span class="sxs-lookup"><span data-stu-id="a92c8-348">Next, add an action call to this answer to close the session.</span></span> <span data-ttu-id="a92c8-349">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Contoso: Đóng phiên** và chọn Hành động.</span><span class="sxs-lookup"><span data-stu-id="a92c8-349">On the nav bar, click the down arrow next to **Contoso: Close session**, and select Actions.</span></span>  

6. <span data-ttu-id="a92c8-350">Trên trang tiếp theo, bấm vào **thêm cuộc gọi hành động hiện có**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-350">On the next page, click **Add Existing Action Call**.</span></span>  

7. <span data-ttu-id="a92c8-351">Trong hộp tìm kiếm, nhấn ENTER hoặc nhấp vào biểu tượng tìm kiếm, sau đó nhấp vào **Mới** để tạo cuộc gọi hàn động.</span><span class="sxs-lookup"><span data-stu-id="a92c8-351">In the search box, press ENTER or click the search icon, and then click **New** to create an action call.</span></span>  

8. <span data-ttu-id="a92c8-352">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="a92c8-352">On the **New Action Call** page, specify the following values.</span></span>  

   |<span data-ttu-id="a92c8-353">Trường</span><span class="sxs-lookup"><span data-stu-id="a92c8-353">Field</span></span>|<span data-ttu-id="a92c8-354">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a92c8-354">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="a92c8-355">Tên</span><span class="sxs-lookup"><span data-stu-id="a92c8-355">Name</span></span>|<span data-ttu-id="a92c8-356">Contoso Action Call: Close Session</span><span class="sxs-lookup"><span data-stu-id="a92c8-356">Contoso Action Call: Close Session</span></span>|  
   |<span data-ttu-id="a92c8-357">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="a92c8-357">Hosted Control</span></span>|<span data-ttu-id="a92c8-358">Contoso Session Tab</span><span class="sxs-lookup"><span data-stu-id="a92c8-358">Contoso Session Tab</span></span> <br> <span data-ttu-id="a92c8-359">**Note:**  The Contoso Session Tab hosted control was created in [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="a92c8-359">**Note:**  The Contoso Session Tab hosted control was created in [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md).</span></span>|  
   |<span data-ttu-id="a92c8-360">Hành động</span><span class="sxs-lookup"><span data-stu-id="a92c8-360">Action</span></span>|<span data-ttu-id="a92c8-361">Đóng phiên</span><span class="sxs-lookup"><span data-stu-id="a92c8-361">CloseSession</span></span>|  
   |<span data-ttu-id="a92c8-362">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="a92c8-362">Data</span></span>|<span data-ttu-id="a92c8-363">sessionid=[[$Context.SessionId]]</span><span class="sxs-lookup"><span data-stu-id="a92c8-363">sessionid=[[$Context.SessionId]]</span></span>|  

   <span data-ttu-id="a92c8-364">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-close-session-action-call.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="a92c8-364">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-close-session-action-call.png "Create an action call in Unified Service Desk")</span></span> 

9. <span data-ttu-id="a92c8-365">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-365">Click **Save**.</span></span>  

<a name="Step7"></a>   
## <a name="step-7-create-an-action-call-to-display-the-agent-script"></a><span data-ttu-id="a92c8-366">Step 7: Create an action call to display the agent script</span><span class="sxs-lookup"><span data-stu-id="a92c8-366">Step 7: Create an action call to display the agent script</span></span>  
 <span data-ttu-id="a92c8-367">In this step, create an action call to display the agent script.</span><span class="sxs-lookup"><span data-stu-id="a92c8-367">In this step, create an action call to display the agent script.</span></span>  

1. <span data-ttu-id="a92c8-368">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="a92c8-368">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="a92c8-369">Click **Action Calls**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-369">Click **Action Calls**.</span></span>  

4. <span data-ttu-id="a92c8-370">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-370">Click **New**.</span></span>  

5. <span data-ttu-id="a92c8-371">On the **New Action Call** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="a92c8-371">On the **New Action Call** page, specify the following values.</span></span>  

   |<span data-ttu-id="a92c8-372">Trường</span><span class="sxs-lookup"><span data-stu-id="a92c8-372">Field</span></span>|<span data-ttu-id="a92c8-373">Giá trị</span><span class="sxs-lookup"><span data-stu-id="a92c8-373">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="a92c8-374">Tên</span><span class="sxs-lookup"><span data-stu-id="a92c8-374">Name</span></span>|<span data-ttu-id="a92c8-375">Các cuộc gọi hành động contoso: Tải mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="a92c8-375">Contoso Action Call: Load Agent Script</span></span>|  
   |<span data-ttu-id="a92c8-376">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="a92c8-376">Hosted Control</span></span>|<span data-ttu-id="a92c8-377">Mã lệnh tổng đài viên Contoso</span><span class="sxs-lookup"><span data-stu-id="a92c8-377">Contoso Agent Scripting</span></span>|  
   |<span data-ttu-id="a92c8-378">Hành động</span><span class="sxs-lookup"><span data-stu-id="a92c8-378">Action</span></span>|<span data-ttu-id="a92c8-379">Đi đến tác vụ</span><span class="sxs-lookup"><span data-stu-id="a92c8-379">GoToTask</span></span>|  
   |<span data-ttu-id="a92c8-380">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="a92c8-380">Data</span></span>|<span data-ttu-id="a92c8-381">Contoso: Welcome to Account Session</span><span class="sxs-lookup"><span data-stu-id="a92c8-381">Contoso: Welcome to Account Session</span></span>|  

   <span data-ttu-id="a92c8-382">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-add-load-agent-script-action-call.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="a92c8-382">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-add-load-agent-script-action-call.png "Create an action call in Unified Service Desk")</span></span>  

6. <span data-ttu-id="a92c8-383">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-383">Click **Save**.</span></span>  

<a name="Step8"></a>   
## <a name="step-8-display-the-agent-script-when-the-account-record-is-displayed-in-a-session"></a><span data-ttu-id="a92c8-384">Step 8: Display the agent script when the account record is displayed in a session</span><span class="sxs-lookup"><span data-stu-id="a92c8-384">Step 8: Display the agent script when the account record is displayed in a session</span></span>  
 <span data-ttu-id="a92c8-385">In this step, add the action call created in the previous step to the **PageReady** event on the **Contoso Account Session** hosted control so that after it’s loaded, the action call is executed to load the agent script.</span><span class="sxs-lookup"><span data-stu-id="a92c8-385">In this step, add the action call created in the previous step to the **PageReady** event on the **Contoso Account Session** hosted control so that after it’s loaded, the action call is executed to load the agent script.</span></span> <span data-ttu-id="a92c8-386">The **Contoso Account Session** hosted control was created in [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="a92c8-386">The **Contoso Account Session** hosted control was created in [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md).</span></span>  

1. <span data-ttu-id="a92c8-387">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="a92c8-387">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="a92c8-388">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-388">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="a92c8-389">Search for the **Contoso Account Session** hosted control, and click it to open the hosted control definition.</span><span class="sxs-lookup"><span data-stu-id="a92c8-389">Search for the **Contoso Account Session** hosted control, and click it to open the hosted control definition.</span></span> 

5. <span data-ttu-id="a92c8-390">On the nav bar, click the down arrow next to **Contoso Account Session**, and then click **Events**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-390">On the nav bar, click the down arrow next to **Contoso Account Session**, and then click **Events**.</span></span>  

   <span data-ttu-id="a92c8-391">![Configure events for a hosted control](../unified-service-desk/media/usd-configure-events-hosted-control.png "Configure events for a hosted control")</span><span class="sxs-lookup"><span data-stu-id="a92c8-391">![Configure events for a hosted control](../unified-service-desk/media/usd-configure-events-hosted-control.png "Configure events for a hosted control")</span></span>  

6. <span data-ttu-id="a92c8-392">On the events page, click **PageReady**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-392">On the events page, click **PageReady**.</span></span>  

7. <span data-ttu-id="a92c8-393">On the **PageReady** page, click **+** in the **Active Actions** area to add an action call to the event.</span><span class="sxs-lookup"><span data-stu-id="a92c8-393">On the **PageReady** page, click **+** in the **Active Actions** area to add an action call to the event.</span></span>  

8. <span data-ttu-id="a92c8-394">Trong hộp tìm kiếm, nhập “`Contoso Action Call: Load Agent Script`” và nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="a92c8-394">In the search box, type “`Contoso Action Call: Load Agent Script`”, and press ENTER or click the search icon.</span></span>  

9. <span data-ttu-id="a92c8-395">Trong kết quả tìm kiếm, bấm vào **Cuộc gọi hành động Contoso: Tải mã lệnh tổng đài viên** để thêm.</span><span class="sxs-lookup"><span data-stu-id="a92c8-395">In the search results, click **Contoso Action Call: Load Agent Script** to add it.</span></span>  

10. <span data-ttu-id="a92c8-396">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-396">Click **Save**.</span></span>  

<a name="Step9"></a>   
## <a name="step-9-add-the-controls-to-the-configuration"></a><span data-ttu-id="a92c8-397">Bước 9: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="a92c8-397">Step 9: Add the controls to the configuration</span></span>  
 <span data-ttu-id="a92c8-398">In this step, add the action calls, agent script, hosted controls, and window navigation rule that you configured in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span><span class="sxs-lookup"><span data-stu-id="a92c8-398">In this step, add the action calls, agent script, hosted controls, and window navigation rule that you configured in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span></span> <span data-ttu-id="a92c8-399">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="a92c8-399">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span></span>  

 <span data-ttu-id="a92c8-400">Add the following to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-400">Add the following to **Contoso Configuration**.</span></span>  

|<span data-ttu-id="a92c8-401">Tên kiểm soát</span><span class="sxs-lookup"><span data-stu-id="a92c8-401">Control name</span></span>|<span data-ttu-id="a92c8-402">Loại kiểm soát</span><span class="sxs-lookup"><span data-stu-id="a92c8-402">Control type</span></span>|  
|------------------|------------------|  
|<span data-ttu-id="a92c8-403">Cuộc gọi hành động contoso: Tạo trường hợp</span><span class="sxs-lookup"><span data-stu-id="a92c8-403">Contoso Action Call: Create Case</span></span>|<span data-ttu-id="a92c8-404">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="a92c8-404">Action call</span></span>|  
|<span data-ttu-id="a92c8-405">Cuộc gọi hành động Contoso: Hiển thị trường hợp hiện có</span><span class="sxs-lookup"><span data-stu-id="a92c8-405">Contoso Action Call: Display Existing Cases</span></span>|<span data-ttu-id="a92c8-406">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="a92c8-406">Action Call</span></span>|  
|<span data-ttu-id="a92c8-407">Cuộc gọi hành động Contoso: Tập trung vào trường hợp hiện có</span><span class="sxs-lookup"><span data-stu-id="a92c8-407">Contoso Action Call: Set Focus on Existing Cases</span></span>|<span data-ttu-id="a92c8-408">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="a92c8-408">Action Call</span></span>|  
|<span data-ttu-id="a92c8-409">Các cuộc gọi hành động contoso: Đóng phiên</span><span class="sxs-lookup"><span data-stu-id="a92c8-409">Contoso Action Call: Close Session</span></span>|<span data-ttu-id="a92c8-410">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="a92c8-410">Action Call</span></span>|  
|<span data-ttu-id="a92c8-411">Các cuộc gọi hành động contoso: Tải mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="a92c8-411">Contoso Action Call: Load Agent Script</span></span>|<span data-ttu-id="a92c8-412">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="a92c8-412">Action Call</span></span>|  
|<span data-ttu-id="a92c8-413">Contoso: Chào mừng bạn đến với Phiên tài khoản</span><span class="sxs-lookup"><span data-stu-id="a92c8-413">Contoso: Welcome to Account Session</span></span>|<span data-ttu-id="a92c8-414">Mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="a92c8-414">Agent Script</span></span>|  
|<span data-ttu-id="a92c8-415">Mã lệnh tổng đài viên Contoso</span><span class="sxs-lookup"><span data-stu-id="a92c8-415">Contoso Agent Scripting</span></span>|<span data-ttu-id="a92c8-416">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="a92c8-416">Hosted Control</span></span>|  
|<span data-ttu-id="a92c8-417">Biểu mẫu trường hợp mới</span><span class="sxs-lookup"><span data-stu-id="a92c8-417">Contoso new case form</span></span>|<span data-ttu-id="a92c8-418">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="a92c8-418">Hosted Control</span></span>|  
|<span data-ttu-id="a92c8-419">Trường hợp sẵn có Contoso cho tài khoản</span><span class="sxs-lookup"><span data-stu-id="a92c8-419">Contoso existing cases for an account</span></span>|<span data-ttu-id="a92c8-420">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="a92c8-420">Hosted Control</span></span>|  
|<span data-ttu-id="a92c8-421">Trường hợp mới Contoso cho nguyên tắc phiên tài khoản</span><span class="sxs-lookup"><span data-stu-id="a92c8-421">Contoso New Case for Account Session Rule</span></span>|<span data-ttu-id="a92c8-422">Window navigation rule</span><span class="sxs-lookup"><span data-stu-id="a92c8-422">Window navigation rule</span></span>|  

 <span data-ttu-id="a92c8-423">To add a control to the configuration:</span><span class="sxs-lookup"><span data-stu-id="a92c8-423">To add a control to the configuration:</span></span>  

1. <span data-ttu-id="a92c8-424">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="a92c8-424">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="a92c8-425">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-425">Click **Configuration**.</span></span>  

4. <span data-ttu-id="a92c8-426">Click **Contoso Configuration** to open the definition.</span><span class="sxs-lookup"><span data-stu-id="a92c8-426">Click **Contoso Configuration** to open the definition.</span></span>  

5. <span data-ttu-id="a92c8-427">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-427">On the nav bar, click the down arrow next to **Contoso Configuration**, and select **Action Calls**.</span></span>  

6. <span data-ttu-id="a92c8-428">Trên trang tiếp theo, bấm vào **Thêm cuộc gọi hành động hiện có**, nhập "Cuộc gọi hành động Contoso" trong thanh tìm kiếm, sau đó nhấn ENTER hoặc nhấp biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="a92c8-428">On the next page, click **Add Existing Action Call**, type “Contoso Action Call” in the search bar, and then press ENTER or click the search icon.</span></span>  

7. <span data-ttu-id="a92c8-429">Chọn năm cuộc gọi hành động từ hộp kết quả tìm kiếm để thêm chúng vào **Cấu hình Contoso**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-429">Select the five action calls from the search results box to add them to **Contoso Configuration**.</span></span>  

8. <span data-ttu-id="a92c8-430">Tương tự, thêm mã lệnh tổng đài viên, kiểm soát tổ chức và nguyên tắc điều hướng cửa sổ bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Mã lệnh tổng đài viên** **Kiểm soát tổ chức** và **Nguyên tắc điều hướng cửa sổ** lần lượt.</span><span class="sxs-lookup"><span data-stu-id="a92c8-430">Similarly, add the agent script, hosted controls, and window navigation rule by clicking the down arrow next to **Contoso Configuration**, and clicking **Agent Scripts** **Hosted Controls** and **Window navigation Rules** respectively.</span></span>  

9. <span data-ttu-id="a92c8-431">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a92c8-431">Click **Save**.</span></span> 

<a name="Step10"></a>   
## <a name="step-10-test-the-application"></a><span data-ttu-id="a92c8-432">Step 10: Test the application</span><span class="sxs-lookup"><span data-stu-id="a92c8-432">Step 10: Test the application</span></span>  

1. <span data-ttu-id="a92c8-433">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] by using the same user credentials that is assigned to Contoso Configuration in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="a92c8-433">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] by using the same user credentials that is assigned to Contoso Configuration in [Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span></span> <span data-ttu-id="a92c8-434">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to CRM instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)</span><span class="sxs-lookup"><span data-stu-id="a92c8-434">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to CRM instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)</span></span>  

2. <span data-ttu-id="a92c8-435">Click the down arrow next to the **SEARCH** button in the toolbar, and then click **Account** to display the account records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="a92c8-435">Click the down arrow next to the **SEARCH** button in the toolbar, and then click **Account** to display the account records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span>  

3. <span data-ttu-id="a92c8-436">Click the expander to display the left pane.</span><span class="sxs-lookup"><span data-stu-id="a92c8-436">Click the expander to display the left pane.</span></span>  

   <span data-ttu-id="a92c8-437">![Choose the expander in Unified Service Desk](../unified-service-desk/media/usd-choose-expander.png "Choose the expander in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="a92c8-437">![Choose the expander in Unified Service Desk](../unified-service-desk/media/usd-choose-expander.png "Choose the expander in Unified Service Desk")</span></span>  

4. <span data-ttu-id="a92c8-438">Click on any of the account records to display the respective account information in a session.</span><span class="sxs-lookup"><span data-stu-id="a92c8-438">Click on any of the account records to display the respective account information in a session.</span></span> <span data-ttu-id="a92c8-439">In the left pane, the **Contoso: Welcome to Account Session** agent script appears.</span><span class="sxs-lookup"><span data-stu-id="a92c8-439">In the left pane, the **Contoso: Welcome to Account Session** agent script appears.</span></span>  

   <span data-ttu-id="a92c8-440">![Agent script in Unified Service Desk](../unified-service-desk/media/usd-agent-script.png "Agent script in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="a92c8-440">![Agent script in Unified Service Desk](../unified-service-desk/media/usd-agent-script.png "Agent script in Unified Service Desk")</span></span>  

5. <span data-ttu-id="a92c8-441">In the agent script:</span><span class="sxs-lookup"><span data-stu-id="a92c8-441">In the agent script:</span></span>  

   1.  <span data-ttu-id="a92c8-442">Click **New case** to open a new case form with pre-populated values (in the red box) from the current account record.</span><span class="sxs-lookup"><span data-stu-id="a92c8-442">Click **New case** to open a new case form with pre-populated values (in the red box) from the current account record.</span></span>  

   <span data-ttu-id="a92c8-443">![New case form using the agent script](../unified-service-desk/media/usd-new-case-form-agent-script.png "New case form using the agent script")</span><span class="sxs-lookup"><span data-stu-id="a92c8-443">![New case form using the agent script](../unified-service-desk/media/usd-new-case-form-agent-script.png "New case form using the agent script")</span></span>  

   2.  <span data-ttu-id="a92c8-444">Click **Display existing cases** to display the associated cases for the current account record.</span><span class="sxs-lookup"><span data-stu-id="a92c8-444">Click **Display existing cases** to display the associated cases for the current account record.</span></span>  

   <span data-ttu-id="a92c8-445">![Display existing cases for an account](../unified-service-desk/media/usd-show-cases-account.png "Display existing cases for an account")</span><span class="sxs-lookup"><span data-stu-id="a92c8-445">![Display existing cases for an account](../unified-service-desk/media/usd-show-cases-account.png "Display existing cases for an account")</span></span>  

   3.  <span data-ttu-id="a92c8-446">Click **Close session** to close the current session.</span><span class="sxs-lookup"><span data-stu-id="a92c8-446">Click **Close session** to close the current session.</span></span>  

<a name="Conclusion"></a>   
## <a name="conclusion"></a><span data-ttu-id="a92c8-447">Kết luận</span><span class="sxs-lookup"><span data-stu-id="a92c8-447">Conclusion</span></span>  
 <span data-ttu-id="a92c8-448">In this walkthrough, you learned how to configure a simple agent script to guide your call center agents.</span><span class="sxs-lookup"><span data-stu-id="a92c8-448">In this walkthrough, you learned how to configure a simple agent script to guide your call center agents.</span></span> [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="a92c8-449">allows you to create more complex scripts with branching logic that contain child answers and actions.</span><span class="sxs-lookup"><span data-stu-id="a92c8-449">allows you to create more complex scripts with branching logic that contain child answers and actions.</span></span> <span data-ttu-id="a92c8-450">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span><span class="sxs-lookup"><span data-stu-id="a92c8-450">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span></span>  

### <a name="see-also"></a><span data-ttu-id="a92c8-451">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a92c8-451">See also</span></span>

 [<span data-ttu-id="a92c8-452">Support for Unified Interface Apps in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="a92c8-452">Support for Unified Interface Apps in Unified Service Desk</span></span>](../unified-service-desk/admin/Support-unified-interfaces-apps-usd.md)

 [<span data-ttu-id="a92c8-453">Unified Interface Page (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="a92c8-453">Unified Interface Page (Hosted Control)</span></span>](../unified-service-desk/unified-interface-page-hosted-control.md)

 [<span data-ttu-id="a92c8-454">Unified Service Desk and Unified Interface Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="a92c8-454">Unified Service Desk and Unified Interface Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md)

 [<span data-ttu-id="a92c8-455">Walkthrough 1: Build a simple agent application for Unified Interface Apps</span><span class="sxs-lookup"><span data-stu-id="a92c8-455">Walkthrough 1: Build a simple agent application for Unified Interface Apps</span></span>](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)

 [<span data-ttu-id="a92c8-456">Walkthrough 2: Display an external webpage in your agent application</span><span class="sxs-lookup"><span data-stu-id="a92c8-456">Walkthrough 2: Display an external webpage in your agent application</span></span>](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md)

 [<span data-ttu-id="a92c8-457">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application</span><span class="sxs-lookup"><span data-stu-id="a92c8-457">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application</span></span>](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)

 [<span data-ttu-id="a92c8-458">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application</span><span class="sxs-lookup"><span data-stu-id="a92c8-458">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application</span></span>](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md)

 [<span data-ttu-id="a92c8-459">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span><span class="sxs-lookup"><span data-stu-id="a92c8-459">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span></span>](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md)

 [<span data-ttu-id="a92c8-460">Walkthrough 6: Configure the Debugger hosted control in your agent application</span><span class="sxs-lookup"><span data-stu-id="a92c8-460">Walkthrough 6: Configure the Debugger hosted control in your agent application</span></span>](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md)
