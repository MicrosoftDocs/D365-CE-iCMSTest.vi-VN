---
title: 'Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application | MicrosoftDocs'
description: Demonstrates how to display Customer Engagement records in a session in your agent application using window navigation rules and session controls in Unified Service Desk.
keywords: ''
ms.date: 12/18/2018
ms.service:
- usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 1B1325DF-1C3A-4205-9C01-E51BE0472FAD
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
ms.openlocfilehash: 472afad9d50d57c97a96c7d22ce5df6bb3fc17ce
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388330"
---
# <a name="walkthrough-4-display-a-microsoft-dynamics-365-for-customer-engagement-apps-unified-interface-apps-record-in-a-session-in-your-agent-application"></a><span data-ttu-id="86f5a-103">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application</span><span class="sxs-lookup"><span data-stu-id="86f5a-103">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application</span></span>
<span data-ttu-id="86f5a-104">This walkthrough demonstrates how to display [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps records in a session in your agent application using window navigation rules and session controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="86f5a-104">This walkthrough demonstrates how to display [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps records in a session in your agent application using window navigation rules and session controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="86f5a-105">Nó cũng trình bày việc sử dụng các tham số thay thế để hiển thị động tên của kiểm soát tổ chức dựa trên hồ sơ tài khoản hiện đang được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="86f5a-105">It also demonstrates the use of replacement parameters to dynamically display the name of the hosted control based on the currently displayed account record.</span></span> <span data-ttu-id="86f5a-106">This walkthrough is built on top of the previous walkthrough, [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md), to display an account record in a session when you click on one of the accounts in the **Account** search result window.</span><span class="sxs-lookup"><span data-stu-id="86f5a-106">This walkthrough is built on top of the previous walkthrough, [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md), to display an account record in a session when you click on one of the accounts in the **Account** search result window.</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="86f5a-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="86f5a-107">Prerequisites</span></span>  
  
- <span data-ttu-id="86f5a-108">You must have completed [Walkthrough 1: Build a simple agent application for Unified Interface app](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) and [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="86f5a-108">You must have completed [Walkthrough 1: Build a simple agent application for Unified Interface app](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) and [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md).</span></span> <span data-ttu-id="86f5a-109">The configurations that you completed in these walkthroughs are required in this walkthrough.</span><span class="sxs-lookup"><span data-stu-id="86f5a-109">The configurations that you completed in these walkthroughs are required in this walkthrough.</span></span>  
  
- <span data-ttu-id="86f5a-110">Cách này giả định rằng bạn sẽ đang sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên ở cuối cách này để kiểm tra ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="86f5a-110">This walkthrough assumes that you’ll be using the same user credential that you used in walkthrough 1 to sign in to the agent application at the end of the walkthrough to test the application.</span></span> <span data-ttu-id="86f5a-111">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-111">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="86f5a-112">[Walkthrough 1: Build a simple agent application for Unified Interface app](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)</span><span class="sxs-lookup"><span data-stu-id="86f5a-112">[Walkthrough 1: Build a simple agent application for Unified Interface app](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)</span></span>  
  
- <span data-ttu-id="86f5a-113">You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="86f5a-113">You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  
  
  - <span data-ttu-id="86f5a-114">**Session Tabs** type of hosted control.</span><span class="sxs-lookup"><span data-stu-id="86f5a-114">**Session Tabs** type of hosted control.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="86f5a-115">[Session Tabs (Hosted Control)](../unified-service-desk/session-tabs-hosted-control.md)</span><span class="sxs-lookup"><span data-stu-id="86f5a-115">[Session Tabs (Hosted Control)](../unified-service-desk/session-tabs-hosted-control.md)</span></span>  
  
  - <span data-ttu-id="86f5a-116">How to configure [Action calls](../unified-service-desk/action-calls.md)</span><span class="sxs-lookup"><span data-stu-id="86f5a-116">How to configure [Action calls](../unified-service-desk/action-calls.md)</span></span>  
  
  - <span data-ttu-id="86f5a-117">How to configure window navigation rules.</span><span class="sxs-lookup"><span data-stu-id="86f5a-117">How to configure window navigation rules.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="86f5a-118">[Use window navigation rules in Unified Service Desk](../unified-service-desk/use-window-navigation-rules-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="86f5a-118">[Use window navigation rules in Unified Service Desk](../unified-service-desk/use-window-navigation-rules-unified-service-desk.md)</span></span>  
  
  - <span data-ttu-id="86f5a-119">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span><span class="sxs-lookup"><span data-stu-id="86f5a-119">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="86f5a-120">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="86f5a-120">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span></span>  
  
## <a name="in-this-walkthrough"></a><span data-ttu-id="86f5a-121">In This Walkthrough</span><span class="sxs-lookup"><span data-stu-id="86f5a-121">In This Walkthrough</span></span>  
 [<span data-ttu-id="86f5a-122">Bước 1: Tạo kiểm soát tổ chức theo phạm vi phiên để hiển thị hồ sơ tài khoản trong phiên</span><span class="sxs-lookup"><span data-stu-id="86f5a-122">Step 1: Create a session-scoped hosted control to display account record in a session</span></span>](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md#Step1)  
  
 [<span data-ttu-id="86f5a-123">Bước 2: Đặt cấu hình các sự kiện để đóng kiểm soát tổ chức từ nơi xuất phát tìm kiếm</span><span class="sxs-lookup"><span data-stu-id="86f5a-123">Step 2: Configure the event to close the hosted control from where the search originated</span></span>](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md#Step2)  
  
 [<span data-ttu-id="86f5a-124">Bước 3: Tạo kiểm soát tổ chức tab phiên</span><span class="sxs-lookup"><span data-stu-id="86f5a-124">Step 3: Create a Session Tabs hosted control</span></span>](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md#Step3)  
  
 [<span data-ttu-id="86f5a-125">Bước 4: Tạo quy tắc chuyển hướng cửa sổ để hiển thị hồ sơ tài khoản trong phiên</span><span class="sxs-lookup"><span data-stu-id="86f5a-125">Step 4: Create a window navigation rule to display the account record in a session</span></span>](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md#Step4)  
  
 [<span data-ttu-id="86f5a-126">Bước 5: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="86f5a-126">Step 5: Add the controls to the configuration</span></span>](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md#Step5)  
  
 [<span data-ttu-id="86f5a-127">Bước 6: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="86f5a-127">Step 6: Test the application</span></span>](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md#Step6)  
  
 [<span data-ttu-id="86f5a-128">Kết luận</span><span class="sxs-lookup"><span data-stu-id="86f5a-128">Conclusion</span></span>](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md#Conclusion)
  
<a name="Step1"></a>   
## <a name="step-1-create-a-session-scoped-hosted-control-to-display-account-record-in-a-session"></a><span data-ttu-id="86f5a-129">Step 1: Create a session-scoped hosted control to display account record in a session</span><span class="sxs-lookup"><span data-stu-id="86f5a-129">Step 1: Create a session-scoped hosted control to display account record in a session</span></span>  
 <span data-ttu-id="86f5a-130">In this step, you’ll create a session-scoped hosted control to display an account record in a session.</span><span class="sxs-lookup"><span data-stu-id="86f5a-130">In this step, you’ll create a session-scoped hosted control to display an account record in a session.</span></span>  
  
1. <span data-ttu-id="86f5a-131">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="86f5a-131">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="86f5a-132">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-132">Click **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="86f5a-133">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-133">Click **New**.</span></span>  
  
5. <span data-ttu-id="86f5a-134">On the **New Hosted Control** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="86f5a-134">On the **New Hosted Control** page, specify the following values.</span></span>  
  
   |<span data-ttu-id="86f5a-135">Trường</span><span class="sxs-lookup"><span data-stu-id="86f5a-135">Field</span></span>|<span data-ttu-id="86f5a-136">Giá trị</span><span class="sxs-lookup"><span data-stu-id="86f5a-136">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="86f5a-137">Tên</span><span class="sxs-lookup"><span data-stu-id="86f5a-137">Name</span></span>|<span data-ttu-id="86f5a-138">Contoso Account Session</span><span class="sxs-lookup"><span data-stu-id="86f5a-138">Contoso Account Session</span></span>|  
   |<span data-ttu-id="86f5a-139">Tên Hiển thị</span><span class="sxs-lookup"><span data-stu-id="86f5a-139">Display Name</span></span>|<span data-ttu-id="86f5a-140">[[account.name]]</span><span class="sxs-lookup"><span data-stu-id="86f5a-140">[[account.name]]</span></span> <br><span data-ttu-id="86f5a-141">**Note:**  We will use replacement parameter to dynamically display the name of the selected account as hosted control display name.</span><span class="sxs-lookup"><span data-stu-id="86f5a-141">**Note:**  We will use replacement parameter to dynamically display the name of the selected account as hosted control display name.</span></span>|  
   |<span data-ttu-id="86f5a-142">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="86f5a-142">USD Component Type</span></span>|<span data-ttu-id="86f5a-143">Unified Interface Page</span><span class="sxs-lookup"><span data-stu-id="86f5a-143">Unified Interface Page</span></span>|  
   |<span data-ttu-id="86f5a-144">Allow Multiple Pages</span><span class="sxs-lookup"><span data-stu-id="86f5a-144">Allow Multiple Pages</span></span>|<span data-ttu-id="86f5a-145">Không</span><span class="sxs-lookup"><span data-stu-id="86f5a-145">No</span></span>|
   |<span data-ttu-id="86f5a-146">Pre-Fetch Data</span><span class="sxs-lookup"><span data-stu-id="86f5a-146">Pre-Fetch Data</span></span>|<span data-ttu-id="86f5a-147">Đã kiểm tra</span><span class="sxs-lookup"><span data-stu-id="86f5a-147">Checked</span></span>|
   |<span data-ttu-id="86f5a-148">Application is Global</span><span class="sxs-lookup"><span data-stu-id="86f5a-148">Application is Global</span></span>|<span data-ttu-id="86f5a-149">Không được chọn</span><span class="sxs-lookup"><span data-stu-id="86f5a-149">Not checked</span></span> <br><span data-ttu-id="86f5a-150">**Note:**  This ensures that the hosted control is session-scoped, that is, only displayed in a session.</span><span class="sxs-lookup"><span data-stu-id="86f5a-150">**Note:**  This ensures that the hosted control is session-scoped, that is, only displayed in a session.</span></span>|  
   |<span data-ttu-id="86f5a-151">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="86f5a-151">Display Group</span></span>|<span data-ttu-id="86f5a-152">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="86f5a-152">MainPanel</span></span>|  
  
   <span data-ttu-id="86f5a-153">![Create a session scoped hosted control](../unified-service-desk/media/usd-create-session-scoped-hosted-control-unified-interface.png "Create a session-scoped hosted control")</span><span class="sxs-lookup"><span data-stu-id="86f5a-153">![Create a session scoped hosted control](../unified-service-desk/media/usd-create-session-scoped-hosted-control-unified-interface.png "Create a session-scoped hosted control")</span></span> 
  
6. <span data-ttu-id="86f5a-154">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-154">Click **Save**.</span></span>
  
<a name="Step2"></a>   
## <a name="step-2-configure-the-event-to-close-the-hosted-control-from-where-the-search-originated"></a><span data-ttu-id="86f5a-155">Step 2: Configure the event to close the hosted control from where the search originated</span><span class="sxs-lookup"><span data-stu-id="86f5a-155">Step 2: Configure the event to close the hosted control from where the search originated</span></span>  
 <span data-ttu-id="86f5a-156">In this step, you’ll configure the **PageReady** event on the **Contoso Account Session** hosted control so that when it’s loaded, the parent hosted control from where the user clicked to open the account, **Contoso Accounts Search**, is closed.</span><span class="sxs-lookup"><span data-stu-id="86f5a-156">In this step, you’ll configure the **PageReady** event on the **Contoso Account Session** hosted control so that when it’s loaded, the parent hosted control from where the user clicked to open the account, **Contoso Accounts Search**, is closed.</span></span> <span data-ttu-id="86f5a-157">The **Contoso Accounts Search** hosted control was created in [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="86f5a-157">The **Contoso Accounts Search** hosted control was created in [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md).</span></span> <span data-ttu-id="86f5a-158">This is done to ensure that the user can’t open other account information in the same session tab.</span><span class="sxs-lookup"><span data-stu-id="86f5a-158">This is done to ensure that the user can’t open other account information in the same session tab.</span></span>  
  
1. <span data-ttu-id="86f5a-159">On the nav bar, click the down arrow next to the **Contoso Account Session** hosted control, and click **Events**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-159">On the nav bar, click the down arrow next to the **Contoso Account Session** hosted control, and click **Events**.</span></span>  
  
   <span data-ttu-id="86f5a-160">![Configure events for a hosted control](../unified-service-desk/media/usd-configure-events-hosted-control2.png "Configure events for a hosted control")</span><span class="sxs-lookup"><span data-stu-id="86f5a-160">![Configure events for a hosted control](../unified-service-desk/media/usd-configure-events-hosted-control2.png "Configure events for a hosted control")</span></span>  
  
2. <span data-ttu-id="86f5a-161">On the events page, click **PageReady**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-161">On the events page, click **PageReady**.</span></span>  
  
3. <span data-ttu-id="86f5a-162">On the **PageReady** page, click **+** in the **Active Actions** area to add an action call to the event.</span><span class="sxs-lookup"><span data-stu-id="86f5a-162">On the **PageReady** page, click **+** in the **Active Actions** area to add an action call to the event.</span></span>  
  
4. <span data-ttu-id="86f5a-163">In the search box, click the search icon or press ENTER, and then click **New** in the lower-right corner of the search results box.</span><span class="sxs-lookup"><span data-stu-id="86f5a-163">In the search box, click the search icon or press ENTER, and then click **New** in the lower-right corner of the search results box.</span></span>  
  
   <span data-ttu-id="86f5a-164">![Add an action call to an event](../unified-service-desk/media/usd-add-action-call-pageready-event.png "Add an action call to an event")</span><span class="sxs-lookup"><span data-stu-id="86f5a-164">![Add an action call to an event](../unified-service-desk/media/usd-add-action-call-pageready-event.png "Add an action call to an event")</span></span>  
  
5. <span data-ttu-id="86f5a-165">On the **New Action Call** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="86f5a-165">On the **New Action Call** page, specify the following values.</span></span>  
  
   |<span data-ttu-id="86f5a-166">Trường</span><span class="sxs-lookup"><span data-stu-id="86f5a-166">Field</span></span>|<span data-ttu-id="86f5a-167">Giá trị</span><span class="sxs-lookup"><span data-stu-id="86f5a-167">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="86f5a-168">Tên</span><span class="sxs-lookup"><span data-stu-id="86f5a-168">Name</span></span>|<span data-ttu-id="86f5a-169">Contoso Action Call: Close Accounts Search</span><span class="sxs-lookup"><span data-stu-id="86f5a-169">Contoso Action Call: Close Accounts Search</span></span>|  
   |<span data-ttu-id="86f5a-170">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="86f5a-170">Hosted Control</span></span>|<span data-ttu-id="86f5a-171">Contoso Account Search</span><span class="sxs-lookup"><span data-stu-id="86f5a-171">Contoso Account Search</span></span>|  
   |<span data-ttu-id="86f5a-172">Hành động</span><span class="sxs-lookup"><span data-stu-id="86f5a-172">Action</span></span>|<span data-ttu-id="86f5a-173">Đóng</span><span class="sxs-lookup"><span data-stu-id="86f5a-173">Close</span></span>|  
  
   <span data-ttu-id="86f5a-174">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call-pageready-close.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="86f5a-174">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call-pageready-close.png "Create an action call in Unified Service Desk")</span></span>  
  
6. <span data-ttu-id="86f5a-175">Click **Save** to add the action call to the **PageReady** event.</span><span class="sxs-lookup"><span data-stu-id="86f5a-175">Click **Save** to add the action call to the **PageReady** event.</span></span>  
  
<a name="Step3"></a>   
## <a name="step-3-create-a-session-tabs-hosted-control"></a><span data-ttu-id="86f5a-176">Bước 3: Tạo kiểm soát tổ chức tab phiên</span><span class="sxs-lookup"><span data-stu-id="86f5a-176">Step 3: Create a Session Tabs hosted control</span></span>  
 <span data-ttu-id="86f5a-177">Để hiển thị hồ sơ trong phiên trong ứng dụng tổng đài viên của bạn, một phiên bản loại **Tab phiên** của kiểm soát tổ chức phải được cấu hình trong ứng dụng tổng đài viên của bạn.</span><span class="sxs-lookup"><span data-stu-id="86f5a-177">To display records in sessions in your agent application, an instance of the **Session Tabs** type of hosted control must be configured in your agent application.</span></span>  
  
1. <span data-ttu-id="86f5a-178">Trên trang kiểm soát tổ chức, bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-178">On the hosted control page, click **New**.</span></span>  
  
2. <span data-ttu-id="86f5a-179">Trên trang Kiểm soát tổ chức mới, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="86f5a-179">On the New Hosted Control page, specify the following values.</span></span>  
  
   |<span data-ttu-id="86f5a-180">Trường</span><span class="sxs-lookup"><span data-stu-id="86f5a-180">Field</span></span>|<span data-ttu-id="86f5a-181">Value</span><span class="sxs-lookup"><span data-stu-id="86f5a-181">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="86f5a-182">Tên</span><span class="sxs-lookup"><span data-stu-id="86f5a-182">Name</span></span>|<span data-ttu-id="86f5a-183">Contoso Session Tab</span><span class="sxs-lookup"><span data-stu-id="86f5a-183">Contoso Session Tab</span></span>|  
   |<span data-ttu-id="86f5a-184">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="86f5a-184">USD Component Type</span></span>|<span data-ttu-id="86f5a-185">Tab Phiên</span><span class="sxs-lookup"><span data-stu-id="86f5a-185">Session Tabs</span></span>|  
  
   <span data-ttu-id="86f5a-186">![Create a Session Tabs hosted control](../unified-service-desk/media/usd-create-sessiontabs-hosted-control.png "Create a Session Tabs hosted control")</span><span class="sxs-lookup"><span data-stu-id="86f5a-186">![Create a Session Tabs hosted control](../unified-service-desk/media/usd-create-sessiontabs-hosted-control.png "Create a Session Tabs hosted control")</span></span>  
  
3. <span data-ttu-id="86f5a-187">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-187">Click **Save**.</span></span>  
  
<a name="Step4"></a>   
## <a name="step-4-create-a-window-navigation-rule-to-display-the-account-record-in-a-session"></a><span data-ttu-id="86f5a-188">Step 4: Create a window navigation rule to display the account record in a session</span><span class="sxs-lookup"><span data-stu-id="86f5a-188">Step 4: Create a window navigation rule to display the account record in a session</span></span>  
 <span data-ttu-id="86f5a-189">In this step, you’ll create a window navigation rule that displays the record in a session when the user clicks on any of the accounts in the search results window.</span><span class="sxs-lookup"><span data-stu-id="86f5a-189">In this step, you’ll create a window navigation rule that displays the record in a session when the user clicks on any of the accounts in the search results window.</span></span>  
  
1. <span data-ttu-id="86f5a-190">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="86f5a-190">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="86f5a-191">Click **Window Navigation Rules**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-191">Click **Window Navigation Rules**.</span></span>  
  
4. <span data-ttu-id="86f5a-192">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-192">Click **New**.</span></span>  
  
5. <span data-ttu-id="86f5a-193">On the **New Window Navigation Rule** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="86f5a-193">On the **New Window Navigation Rule** page, specify the following values.</span></span>  
  
   |<span data-ttu-id="86f5a-194">Trường</span><span class="sxs-lookup"><span data-stu-id="86f5a-194">Field</span></span>|<span data-ttu-id="86f5a-195">Giá trị</span><span class="sxs-lookup"><span data-stu-id="86f5a-195">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="86f5a-196">Tên</span><span class="sxs-lookup"><span data-stu-id="86f5a-196">Name</span></span>|<span data-ttu-id="86f5a-197">Quy tắc Phiên Tài khoản contoso</span><span class="sxs-lookup"><span data-stu-id="86f5a-197">Contoso Account Session Rule</span></span>|  
   |<span data-ttu-id="86f5a-198">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="86f5a-198">Order</span></span>|<span data-ttu-id="86f5a-199">5</span><span class="sxs-lookup"><span data-stu-id="86f5a-199">5</span></span>|  
   |<span data-ttu-id="86f5a-200">Từ</span><span class="sxs-lookup"><span data-stu-id="86f5a-200">From</span></span>|<span data-ttu-id="86f5a-201">Contoso Accounts Search</span><span class="sxs-lookup"><span data-stu-id="86f5a-201">Contoso Accounts Search</span></span>|  
   |<span data-ttu-id="86f5a-202">Thực thể</span><span class="sxs-lookup"><span data-stu-id="86f5a-202">Entity</span></span>|<span data-ttu-id="86f5a-203">tài khoản</span><span class="sxs-lookup"><span data-stu-id="86f5a-203">account</span></span>|  
   |<span data-ttu-id="86f5a-204">Loại định tuyến</span><span class="sxs-lookup"><span data-stu-id="86f5a-204">Route Type</span></span>|<span data-ttu-id="86f5a-205">In Place</span><span class="sxs-lookup"><span data-stu-id="86f5a-205">In Place</span></span>|  
   |<span data-ttu-id="86f5a-206">Điểm đến</span><span class="sxs-lookup"><span data-stu-id="86f5a-206">Destination</span></span>|<span data-ttu-id="86f5a-207">Thẻ</span><span class="sxs-lookup"><span data-stu-id="86f5a-207">Tab</span></span>|  
   |<span data-ttu-id="86f5a-208">Hành động</span><span class="sxs-lookup"><span data-stu-id="86f5a-208">Action</span></span>|<span data-ttu-id="86f5a-209">Tạo phiên làm việc</span><span class="sxs-lookup"><span data-stu-id="86f5a-209">Create Session</span></span>|  
   |<span data-ttu-id="86f5a-210">Tab Mục tiêu</span><span class="sxs-lookup"><span data-stu-id="86f5a-210">Target Tab</span></span>|<span data-ttu-id="86f5a-211">Contoso Account Session</span><span class="sxs-lookup"><span data-stu-id="86f5a-211">Contoso Account Session</span></span>|  
   |<span data-ttu-id="86f5a-212">Hiển thị Tab</span><span class="sxs-lookup"><span data-stu-id="86f5a-212">Show Tab</span></span>|<span data-ttu-id="86f5a-213">Contoso Account Session</span><span class="sxs-lookup"><span data-stu-id="86f5a-213">Contoso Account Session</span></span>|  
   |<span data-ttu-id="86f5a-214">Hide Command Bar</span><span class="sxs-lookup"><span data-stu-id="86f5a-214">Hide Command Bar</span></span>|<span data-ttu-id="86f5a-215">Không</span><span class="sxs-lookup"><span data-stu-id="86f5a-215">No</span></span>|  
   |<span data-ttu-id="86f5a-216">Hide Navigation Bar</span><span class="sxs-lookup"><span data-stu-id="86f5a-216">Hide Navigation Bar</span></span>|<span data-ttu-id="86f5a-217">Có</span><span class="sxs-lookup"><span data-stu-id="86f5a-217">Yes</span></span>|  
  
   <span data-ttu-id="86f5a-218">![Create a window navigation rule](../unified-service-desk/media/usd-create-window-navigation-rule-unified-interface.png "Create a window navigation rule")</span><span class="sxs-lookup"><span data-stu-id="86f5a-218">![Create a window navigation rule](../unified-service-desk/media/usd-create-window-navigation-rule-unified-interface.png "Create a window navigation rule")</span></span>  
  
6. <span data-ttu-id="86f5a-219">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-219">Click **Save**.</span></span>  
  
<a name="Step5"></a>   
## <a name="step-5-add-the-controls-to-the-configuration"></a><span data-ttu-id="86f5a-220">Step 5: Add the controls to the configuration</span><span class="sxs-lookup"><span data-stu-id="86f5a-220">Step 5: Add the controls to the configuration</span></span>  
 <span data-ttu-id="86f5a-221">In this step, you’ll add the action call, event, hosted controls, and window navigation rule configured in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span><span class="sxs-lookup"><span data-stu-id="86f5a-221">In this step, you’ll add the action call, event, hosted controls, and window navigation rule configured in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span></span> <span data-ttu-id="86f5a-222">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="86f5a-222">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span></span>  
  
 <span data-ttu-id="86f5a-223">Add the following to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-223">Add the following to **Contoso Configuration**.</span></span>  
  
|<span data-ttu-id="86f5a-224">Tên kiểm soát</span><span class="sxs-lookup"><span data-stu-id="86f5a-224">Control name</span></span>|<span data-ttu-id="86f5a-225">Loại kiểm soát</span><span class="sxs-lookup"><span data-stu-id="86f5a-225">Control type</span></span>|  
|------------------|------------------|  
|<span data-ttu-id="86f5a-226">Contoso Action Call: Close Accounts Search</span><span class="sxs-lookup"><span data-stu-id="86f5a-226">Contoso Action Call: Close Accounts Search</span></span>|<span data-ttu-id="86f5a-227">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="86f5a-227">Action call</span></span>|  
|<span data-ttu-id="86f5a-228">PageReady</span><span class="sxs-lookup"><span data-stu-id="86f5a-228">PageReady</span></span>|<span data-ttu-id="86f5a-229">Sự kiện cho kiểm soát tổ chức Phiên tài khoản Contoso.</span><span class="sxs-lookup"><span data-stu-id="86f5a-229">Event for the Contoso Account Session hosted control</span></span>|  
|<span data-ttu-id="86f5a-230">Contoso Account Session</span><span class="sxs-lookup"><span data-stu-id="86f5a-230">Contoso Account Session</span></span>|<span data-ttu-id="86f5a-231">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="86f5a-231">Hosted Control</span></span>|  
|<span data-ttu-id="86f5a-232">Tab phiên Contoso</span><span class="sxs-lookup"><span data-stu-id="86f5a-232">Contoso Session Tab</span></span>|<span data-ttu-id="86f5a-233">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="86f5a-233">Hosted Control</span></span>|  
|<span data-ttu-id="86f5a-234">Quy tắc Phiên Tài khoản contoso</span><span class="sxs-lookup"><span data-stu-id="86f5a-234">Contoso Account Session Rule</span></span>|<span data-ttu-id="86f5a-235">Window navigation rule</span><span class="sxs-lookup"><span data-stu-id="86f5a-235">Window navigation rule</span></span>|  
  
 <span data-ttu-id="86f5a-236">To add a control to the configuration:</span><span class="sxs-lookup"><span data-stu-id="86f5a-236">To add a control to the configuration:</span></span>  
  
1. <span data-ttu-id="86f5a-237">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="86f5a-237">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="86f5a-238">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-238">Click **Configuration**.</span></span>  
  
4. <span data-ttu-id="86f5a-239">Click **Contoso Configuration** to open the definition.</span><span class="sxs-lookup"><span data-stu-id="86f5a-239">Click **Contoso Configuration** to open the definition.</span></span>  
  
5. <span data-ttu-id="86f5a-240">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-240">On the nav bar, click the down arrow next to **Contoso Configuration**, and select **Action Calls**.</span></span>  
  
6. <span data-ttu-id="86f5a-241">Trên trang tiếp theo, bấm vào **Thêm Cuộc gọi Hành động Hiện có**, nhập “`Contoso Action Call: Close Accounts Search`” vào thanh tìm kiếm, sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="86f5a-241">On the next page, click **Add Existing Action Call**, type “`Contoso Action Call: Close Accounts Search`” in the search bar, and then press ENTER or click the search icon.</span></span>  
  
7. <span data-ttu-id="86f5a-242">Trong hộp kết quả tìm kiếm, hãy nhấp vào cuộc gọi hành động để thêm vào **Cấu hình Contoso**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-242">In the search result box, click the action call to add it to **Contoso Configuration**.</span></span>  
  
8. <span data-ttu-id="86f5a-243">Tương tự, thêm sự kiện, kiểm soát tổ chức và nguyên tắc điều hướng cửa sổ bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Sự kiện** **Kiểm soát tổ chức** và **Nguyên tắc điều hướng cửa sổ** lần lượt.</span><span class="sxs-lookup"><span data-stu-id="86f5a-243">Similarly, add the event, hosted controls and window navigation rule by clicking the down arrow next to **Contoso Configuration**, and clicking **Events** **Hosted Controls** and **Window navigation Rules** respectively.</span></span>  
  
9. <span data-ttu-id="86f5a-244">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-244">Click **Save**.</span></span>  
  
<a name="Step6"></a>   
## <a name="step-6-test-the-application"></a><span data-ttu-id="86f5a-245">Step 6: Test the application</span><span class="sxs-lookup"><span data-stu-id="86f5a-245">Step 6: Test the application</span></span>  
  
1. <span data-ttu-id="86f5a-246">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured Unified Service Desk by using the same user credentials that is assigned to Contoso Configuration in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="86f5a-246">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured Unified Service Desk by using the same user credentials that is assigned to Contoso Configuration in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md).</span></span> <span data-ttu-id="86f5a-247">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to CRM instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span><span class="sxs-lookup"><span data-stu-id="86f5a-247">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to CRM instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span></span>  
  
2. <span data-ttu-id="86f5a-248">To display the account records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance, click the down arrow next to the **Search** button in the toolbar, and then click **Account**.</span><span class="sxs-lookup"><span data-stu-id="86f5a-248">To display the account records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance, click the down arrow next to the **Search** button in the toolbar, and then click **Account**.</span></span>  
  
3. <span data-ttu-id="86f5a-249">Click any of the account records to display the respective account information in a session; the information is displayed under a session tab. Note that the name of the hosted control tab that contains the account record automatically displays the account name because earlier you used replacement parameters to dynamically display the current account name instead of a static value.</span><span class="sxs-lookup"><span data-stu-id="86f5a-249">Click any of the account records to display the respective account information in a session; the information is displayed under a session tab. Note that the name of the hosted control tab that contains the account record automatically displays the account name because earlier you used replacement parameters to dynamically display the current account name instead of a static value.</span></span>  
  
   <span data-ttu-id="86f5a-250">![Account record displayed in a session](../unified-service-desk/media/usd-account-record-session-unified-interface.png "Account record displayed in a session")</span><span class="sxs-lookup"><span data-stu-id="86f5a-250">![Account record displayed in a session](../unified-service-desk/media/usd-account-record-session-unified-interface.png "Account record displayed in a session")</span></span>  
  
4. <span data-ttu-id="86f5a-251">If you open another account record, it will be displayed in another session in your client application.</span><span class="sxs-lookup"><span data-stu-id="86f5a-251">If you open another account record, it will be displayed in another session in your client application.</span></span> <span data-ttu-id="86f5a-252">To open another account, click the down arrow next to the **Search** button, click **Account**, and then click an account name to display the account information in another session.</span><span class="sxs-lookup"><span data-stu-id="86f5a-252">To open another account, click the down arrow next to the **Search** button, click **Account**, and then click an account name to display the account information in another session.</span></span>  
  
   <span data-ttu-id="86f5a-253">![Multiple sessions in Unified Service Desk](../unified-service-desk/media/usd-multiple-sessions-unified-interface.png "Multiple sessions in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="86f5a-253">![Multiple sessions in Unified Service Desk](../unified-service-desk/media/usd-multiple-sessions-unified-interface.png "Multiple sessions in Unified Service Desk")</span></span>  
  
<a name="Conclusion"></a>   
## <a name="conclusion"></a><span data-ttu-id="86f5a-254">Kết luận</span><span class="sxs-lookup"><span data-stu-id="86f5a-254">Conclusion</span></span>  
 <span data-ttu-id="86f5a-255">In this walkthrough, you learned how to use the session hosted control and window navigation rules to display [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records in a session in your agent application.</span><span class="sxs-lookup"><span data-stu-id="86f5a-255">In this walkthrough, you learned how to use the session hosted control and window navigation rules to display [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records in a session in your agent application.</span></span> <span data-ttu-id="86f5a-256">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span><span class="sxs-lookup"><span data-stu-id="86f5a-256">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="86f5a-257">Try the next walkthrough to present enhanced session information in your agent application: [Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md).</span><span class="sxs-lookup"><span data-stu-id="86f5a-257">Try the next walkthrough to present enhanced session information in your agent application: [Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md).</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="86f5a-258">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="86f5a-258">See also</span></span>
 [<span data-ttu-id="86f5a-259">Support for Unified Interface Apps in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="86f5a-259">Support for Unified Interface Apps in Unified Service Desk</span></span>](../unified-service-desk/admin/Support-unified-interfaces-apps-usd.md)

 [<span data-ttu-id="86f5a-260">Unified Interface Page (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="86f5a-260">Unified Interface Page (Hosted Control)</span></span>](../unified-service-desk/unified-interface-page-hosted-control.md)

 [<span data-ttu-id="86f5a-261">Unified Service Desk and Unified Interface Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="86f5a-261">Unified Service Desk and Unified Interface Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md) 

 [<span data-ttu-id="86f5a-262">Cách 1: Xây dựng ứng dụng tổng đài viên đơn giản</span><span class="sxs-lookup"><span data-stu-id="86f5a-262">Walkthrough 1: Build a simple agent application</span></span>](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md)  

 [<span data-ttu-id="86f5a-263">Walkthrough 2: Display an external webpage in your agent application</span><span class="sxs-lookup"><span data-stu-id="86f5a-263">Walkthrough 2: Display an external webpage in your agent application</span></span>](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md)   

 [<span data-ttu-id="86f5a-264">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application</span><span class="sxs-lookup"><span data-stu-id="86f5a-264">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application</span></span>](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)

 [<span data-ttu-id="86f5a-265">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span><span class="sxs-lookup"><span data-stu-id="86f5a-265">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span></span>](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md) 

 [<span data-ttu-id="86f5a-266">Walkthrough 6: Configure the Debugger hosted control in your agent application</span><span class="sxs-lookup"><span data-stu-id="86f5a-266">Walkthrough 6: Configure the Debugger hosted control in your agent application</span></span>](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md)
 
 [<span data-ttu-id="86f5a-267">Walkthrough 7: Configure agent scripting in your agent application</span><span class="sxs-lookup"><span data-stu-id="86f5a-267">Walkthrough 7: Configure agent scripting in your agent application</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)
