---
title: 'Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application | MicrosoftDocs'
description: Demonstrates how to display Customer Engagement records in a session in your agent application using window navigation rules and session controls in Unified Service Desk.
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
ms.assetid: aabfbcd2-1289-4291-9ce7-9ffe0f03c3c7
caps.latest.revision: 6
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 219ccf291c26436049c1a9cc88de9f900e2cf3f7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387267"
---
# <a name="walkthrough-4-display-a-microsoft-dynamics-365-for-customer-engagement-apps-record-in-a-session-in-your-agent-application"></a><span data-ttu-id="2f23e-103">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application</span><span class="sxs-lookup"><span data-stu-id="2f23e-103">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application</span></span>
<span data-ttu-id="2f23e-104">This walkthrough demonstrates how to display [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps records in a session in your agent application using window navigation rules and session controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="2f23e-104">This walkthrough demonstrates how to display [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps records in a session in your agent application using window navigation rules and session controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="2f23e-105">Nó cũng trình bày việc sử dụng các tham số thay thế để hiển thị động tên của kiểm soát tổ chức dựa trên hồ sơ tài khoản hiện đang được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="2f23e-105">It also demonstrates the use of replacement parameters to dynamically display the name of the hosted control based on the currently displayed account record.</span></span> <span data-ttu-id="2f23e-106">This walkthrough is built on top of the previous walkthrough, [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md), to display an account record in a session when you click on one of the accounts in the **Account** search result window.</span><span class="sxs-lookup"><span data-stu-id="2f23e-106">This walkthrough is built on top of the previous walkthrough, [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md), to display an account record in a session when you click on one of the accounts in the **Account** search result window.</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="2f23e-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="2f23e-107">Prerequisites</span></span>  
  
- <span data-ttu-id="2f23e-108">You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) and [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="2f23e-108">You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) and [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md).</span></span> <span data-ttu-id="2f23e-109">Các cấu hình mà bạn hoàn thành trong các cách này được yêu cầu trong cách này.</span><span class="sxs-lookup"><span data-stu-id="2f23e-109">The configurations that you completed in these walkthroughs are required in this walkthrough.</span></span>  
  
- <span data-ttu-id="2f23e-110">Cách này giả định rằng bạn sẽ đang sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên ở cuối cách này để kiểm tra ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="2f23e-110">This walkthrough assumes that you’ll be using the same user credential that you used in walkthrough 1 to sign in to the agent application at the end of the walkthrough to test the application.</span></span> <span data-ttu-id="2f23e-111">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-111">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="2f23e-112">[Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)</span><span class="sxs-lookup"><span data-stu-id="2f23e-112">[Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)</span></span>  
  
- <span data-ttu-id="2f23e-113">You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="2f23e-113">You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  
  
  - <span data-ttu-id="2f23e-114">Loại kiểm soát tổ chức **Tab Phiên**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-114">**Session Tabs** type of hosted control.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="2f23e-115">[Session Tabs (Hosted Control)](../unified-service-desk/session-tabs-hosted-control.md)</span><span class="sxs-lookup"><span data-stu-id="2f23e-115">[Session Tabs (Hosted Control)](../unified-service-desk/session-tabs-hosted-control.md)</span></span>  
  
  - <span data-ttu-id="2f23e-116">How to configure [Action calls](../unified-service-desk/action-calls.md)</span><span class="sxs-lookup"><span data-stu-id="2f23e-116">How to configure [Action calls](../unified-service-desk/action-calls.md)</span></span>  
  
  - <span data-ttu-id="2f23e-117">How to configure window navigation rules.</span><span class="sxs-lookup"><span data-stu-id="2f23e-117">How to configure window navigation rules.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="2f23e-118">[Use window navigation rules in Unified Service Desk](../unified-service-desk/use-window-navigation-rules-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="2f23e-118">[Use window navigation rules in Unified Service Desk](../unified-service-desk/use-window-navigation-rules-unified-service-desk.md)</span></span>  
  
  - <span data-ttu-id="2f23e-119">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span><span class="sxs-lookup"><span data-stu-id="2f23e-119">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="2f23e-120">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="2f23e-120">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span></span>  
  
## <a name="in-this-walkthrough"></a><span data-ttu-id="2f23e-121">In This Walkthrough</span><span class="sxs-lookup"><span data-stu-id="2f23e-121">In This Walkthrough</span></span>  
 [<span data-ttu-id="2f23e-122">Bước 1: Tạo kiểm soát tổ chức theo phạm vi phiên để hiển thị hồ sơ tài khoản trong phiên</span><span class="sxs-lookup"><span data-stu-id="2f23e-122">Step 1: Create a session-scoped hosted control to display account record in a session</span></span>](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md#Step1)  
  
 [<span data-ttu-id="2f23e-123">Bước 2: Đặt cấu hình các sự kiện để đóng kiểm soát tổ chức từ nơi xuất phát tìm kiếm</span><span class="sxs-lookup"><span data-stu-id="2f23e-123">Step 2: Configure the event to close the hosted control from where the search originated</span></span>](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md#Step2)  
  
 [<span data-ttu-id="2f23e-124">Bước 3: Tạo kiểm soát tổ chức tab phiên</span><span class="sxs-lookup"><span data-stu-id="2f23e-124">Step 3: Create a Session Tabs hosted control</span></span>](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md#Step3)  
  
 [<span data-ttu-id="2f23e-125">Bước 4: Tạo quy tắc chuyển hướng cửa sổ để hiển thị hồ sơ tài khoản trong phiên</span><span class="sxs-lookup"><span data-stu-id="2f23e-125">Step 4: Create a window navigation rule to display the account record in a session</span></span>](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md#Step4)  
  
 [<span data-ttu-id="2f23e-126">Bước 5: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="2f23e-126">Step 5: Add the controls to the configuration</span></span>](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md#Step5)  
  
 [<span data-ttu-id="2f23e-127">Bước 6: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="2f23e-127">Step 6: Test the application</span></span>](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md#Step6)  
  
 [<span data-ttu-id="2f23e-128">Kết luận</span><span class="sxs-lookup"><span data-stu-id="2f23e-128">Conclusion</span></span>](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md#Conclusion)  
  
<a name="Step1"></a>   
## <a name="step-1-create-a-session-scoped-hosted-control-to-display-account-record-in-a-session"></a><span data-ttu-id="2f23e-129">Bước 1: Tạo kiểm soát tổ chức theo phạm vi phiên để hiển thị hồ sơ tài khoản trong phiên</span><span class="sxs-lookup"><span data-stu-id="2f23e-129">Step 1: Create a session-scoped hosted control to display account record in a session</span></span>  
 <span data-ttu-id="2f23e-130">Trong bước này, bạn sẽ tạo kiểm soát tổ chức theo phạm vi phiên để hiển thị hồ sơ tài khoản trong phiên.</span><span class="sxs-lookup"><span data-stu-id="2f23e-130">In this step, you’ll create a session-scoped hosted control to display an account record in a session.</span></span>  
  
1. <span data-ttu-id="2f23e-131">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="2f23e-131">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="2f23e-132">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-132">Click **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="2f23e-133">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-133">Click **New**.</span></span>  
  
5. <span data-ttu-id="2f23e-134">On the **New Hosted Control** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="2f23e-134">On the **New Hosted Control** page, specify the following values.</span></span>  
  
   |<span data-ttu-id="2f23e-135">Trường</span><span class="sxs-lookup"><span data-stu-id="2f23e-135">Field</span></span>|<span data-ttu-id="2f23e-136">Giá trị</span><span class="sxs-lookup"><span data-stu-id="2f23e-136">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="2f23e-137">Tên</span><span class="sxs-lookup"><span data-stu-id="2f23e-137">Name</span></span>|<span data-ttu-id="2f23e-138">Phiên Tài khoản contoso</span><span class="sxs-lookup"><span data-stu-id="2f23e-138">Contoso Account Session</span></span>|  
   |<span data-ttu-id="2f23e-139">Tên Hiển thị</span><span class="sxs-lookup"><span data-stu-id="2f23e-139">Display Name</span></span>|<span data-ttu-id="2f23e-140">[[account.name]] **Note:**  We will use replacement parameter to dynamically display the name of the selected account as hosted control display name.</span><span class="sxs-lookup"><span data-stu-id="2f23e-140">[[account.name]] **Note:**  We will use replacement parameter to dynamically display the name of the selected account as hosted control display name.</span></span>|  
   |<span data-ttu-id="2f23e-141">Loại Thành phần USD</span><span class="sxs-lookup"><span data-stu-id="2f23e-141">USD Component Type</span></span>|<span data-ttu-id="2f23e-142">Trang CRM</span><span class="sxs-lookup"><span data-stu-id="2f23e-142">CRM Page</span></span>|  
   |<span data-ttu-id="2f23e-143">Cho phép nhiều trang</span><span class="sxs-lookup"><span data-stu-id="2f23e-143">Allow Multiple Pages</span></span>|<span data-ttu-id="2f23e-144">No</span><span class="sxs-lookup"><span data-stu-id="2f23e-144">No</span></span>|  
   |<span data-ttu-id="2f23e-145">Loại lưu trữ</span><span class="sxs-lookup"><span data-stu-id="2f23e-145">Hosting Type</span></span>|<span data-ttu-id="2f23e-146">WPF nội bộ</span><span class="sxs-lookup"><span data-stu-id="2f23e-146">Internal WPF</span></span>|  
   |<span data-ttu-id="2f23e-147">Application is Global</span><span class="sxs-lookup"><span data-stu-id="2f23e-147">Application is Global</span></span>|<span data-ttu-id="2f23e-148">Not checked **Note:**  This ensures that the hosted control is session-scoped, that is, only displayed in a session.</span><span class="sxs-lookup"><span data-stu-id="2f23e-148">Not checked **Note:**  This ensures that the hosted control is session-scoped, that is, only displayed in a session.</span></span>|  
   |<span data-ttu-id="2f23e-149">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="2f23e-149">Display Group</span></span>|<span data-ttu-id="2f23e-150">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="2f23e-150">MainPanel</span></span>|  
  
   <span data-ttu-id="2f23e-151">![Create a session-scoped hosted control](../unified-service-desk/media/usd-create-session-scoped-hosted-control.png "Create a session-scoped hosted control")</span><span class="sxs-lookup"><span data-stu-id="2f23e-151">![Create a session-scoped hosted control](../unified-service-desk/media/usd-create-session-scoped-hosted-control.png "Create a session-scoped hosted control")</span></span>  
  
6. <span data-ttu-id="2f23e-152">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-152">Click **Save**.</span></span>  
  
<a name="Step2"></a>   
## <a name="step-2-configure-the-event-to-close-the-hosted-control-from-where-the-search-originated"></a><span data-ttu-id="2f23e-153">Bước 2: Đặt cấu hình các sự kiện để đóng kiểm soát tổ chức từ nơi xuất phát tìm kiếm</span><span class="sxs-lookup"><span data-stu-id="2f23e-153">Step 2: Configure the event to close the hosted control from where the search originated</span></span>  
 <span data-ttu-id="2f23e-154">Trong bước này, bạn sẽ đặt cấu hình sự kiện **BrowserDocumentComplete** trên kiểm soát tổ chức **Phiên tài khoản Contoso** để khi nó được tải, kiểm soát tổ chức chính từ nơi người dùng nhấp vào để mở tài khoản, **Tìm kiếm tài khoản Contoso** bị đóng lại.</span><span class="sxs-lookup"><span data-stu-id="2f23e-154">In this step, you’ll configure the **BrowserDocumentComplete** event on the **Contoso Account Session** hosted control so that when it’s loaded, the parent hosted control from where the user clicked to open the account, **Contoso Accounts Search**, is closed.</span></span> <span data-ttu-id="2f23e-155">The **Contoso Accounts Search** hosted control was created in [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="2f23e-155">The **Contoso Accounts Search** hosted control was created in [Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md).</span></span> <span data-ttu-id="2f23e-156">Điều này được thực hiện để đảm bảo rằng người dùng không thể mở thông tin tài khoản khác trong cùng một tab phiên.</span><span class="sxs-lookup"><span data-stu-id="2f23e-156">This is done to ensure that the user can’t open other account information in the same session tab.</span></span>  
  
1. <span data-ttu-id="2f23e-157">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh kiểm soát tổ chức **Phiên tài khoản Contoso**, sau đó nhấp vào **Sự kiện**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-157">On the nav bar, click the down arrow next to the **Contoso Account Session** hosted control, and click **Events**.</span></span>  
  
   <span data-ttu-id="2f23e-158">![Configure events for a hosted control](../unified-service-desk/media/usd-configure-events-hosted-control2.png "Configure events for a hosted control")</span><span class="sxs-lookup"><span data-stu-id="2f23e-158">![Configure events for a hosted control](../unified-service-desk/media/usd-configure-events-hosted-control2.png "Configure events for a hosted control")</span></span>  
  
2. <span data-ttu-id="2f23e-159">On the events page, click **BrowserDocumentComplete**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-159">On the events page, click **BrowserDocumentComplete**.</span></span>  
  
3. <span data-ttu-id="2f23e-160">On the **BrowserDocumentComplete** page, click **+** in the **Active Actions** area to add an action call to the event.</span><span class="sxs-lookup"><span data-stu-id="2f23e-160">On the **BrowserDocumentComplete** page, click **+** in the **Active Actions** area to add an action call to the event.</span></span>  
  
4. <span data-ttu-id="2f23e-161">Trong hộp tìm kiếm, nhấn biểu tượng tìm kiếm hoặc nhấn ENTER, sau đó nhấp vào **Mới** ở góc dưới bên phải của hộp kết quả tìm kiểm.</span><span class="sxs-lookup"><span data-stu-id="2f23e-161">In the search box, click the search icon or press ENTER, and then click **New** in the lower-right corner of the search results box.</span></span>  
  
   <span data-ttu-id="2f23e-162">![Add an action call to an event](../unified-service-desk/media/usd-add-action-call-event.png "Add an action call to an event")</span><span class="sxs-lookup"><span data-stu-id="2f23e-162">![Add an action call to an event](../unified-service-desk/media/usd-add-action-call-event.png "Add an action call to an event")</span></span>  
  
5. <span data-ttu-id="2f23e-163">On the **New Action Call** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="2f23e-163">On the **New Action Call** page, specify the following values.</span></span>  
  
   |<span data-ttu-id="2f23e-164">Trường</span><span class="sxs-lookup"><span data-stu-id="2f23e-164">Field</span></span>|<span data-ttu-id="2f23e-165">Giá trị</span><span class="sxs-lookup"><span data-stu-id="2f23e-165">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="2f23e-166">Tên</span><span class="sxs-lookup"><span data-stu-id="2f23e-166">Name</span></span>|<span data-ttu-id="2f23e-167">Các cuộc gọi hành động contoso: Đóng Tìm kiếm tài khoản</span><span class="sxs-lookup"><span data-stu-id="2f23e-167">Contoso Action Call: Close Accounts Search</span></span>|  
   |<span data-ttu-id="2f23e-168">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="2f23e-168">Hosted Control</span></span>|<span data-ttu-id="2f23e-169">Tìm kiếm tài khoản Contoso</span><span class="sxs-lookup"><span data-stu-id="2f23e-169">Contoso Account Search</span></span>|  
   |<span data-ttu-id="2f23e-170">Hành động</span><span class="sxs-lookup"><span data-stu-id="2f23e-170">Action</span></span>|<span data-ttu-id="2f23e-171">Đóng</span><span class="sxs-lookup"><span data-stu-id="2f23e-171">Close</span></span>|  
  
   <span data-ttu-id="2f23e-172">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call.png "Create an action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="2f23e-172">![Create an action call in Unified Service Desk](../unified-service-desk/media/usd-create-action-call.png "Create an action call in Unified Service Desk")</span></span>  
  
6. <span data-ttu-id="2f23e-173">Bấm vào **Lưu** để thêm cuộc gọi hành động vào sự kiện **BrowserDocumentComplete**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-173">Click **Save** to add the action call to the **BrowserDocumentComplete** event.</span></span>  
  
<a name="Step3"></a>   
## <a name="step-3-create-a-session-tabs-hosted-control"></a><span data-ttu-id="2f23e-174">Bước 3: Tạo kiểm soát tổ chức tab phiên</span><span class="sxs-lookup"><span data-stu-id="2f23e-174">Step 3: Create a Session Tabs hosted control</span></span>  
 <span data-ttu-id="2f23e-175">Để hiển thị hồ sơ trong phiên trong ứng dụng tổng đài viên của bạn, một phiên bản loại **Tab phiên** của kiểm soát tổ chức phải được cấu hình trong ứng dụng tổng đài viên của bạn.</span><span class="sxs-lookup"><span data-stu-id="2f23e-175">To display records in sessions in your agent application, an instance of the **Session Tabs** type of hosted control must be configured in your agent application.</span></span>  
  
1. <span data-ttu-id="2f23e-176">Trên trang kiểm soát tổ chức, bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-176">On the hosted control page, click **New**.</span></span>  
  
2. <span data-ttu-id="2f23e-177">Trên trang Kiểm soát tổ chức mới, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="2f23e-177">On the New Hosted Control page, specify the following values.</span></span>  
  
   |<span data-ttu-id="2f23e-178">Trường</span><span class="sxs-lookup"><span data-stu-id="2f23e-178">Field</span></span>|<span data-ttu-id="2f23e-179">Value</span><span class="sxs-lookup"><span data-stu-id="2f23e-179">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="2f23e-180">Tên</span><span class="sxs-lookup"><span data-stu-id="2f23e-180">Name</span></span>|<span data-ttu-id="2f23e-181">Tab phiên Contoso</span><span class="sxs-lookup"><span data-stu-id="2f23e-181">Contoso Session Tab</span></span>|  
   |<span data-ttu-id="2f23e-182">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="2f23e-182">USD Component Type</span></span>|<span data-ttu-id="2f23e-183">Tab Phiên</span><span class="sxs-lookup"><span data-stu-id="2f23e-183">Session Tabs</span></span>|  
  
   <span data-ttu-id="2f23e-184">![Create a Session Tabs hosted control](../unified-service-desk/media/usd-create-session-tabs-hosted-control.png "Create a Session Tabs hosted control")</span><span class="sxs-lookup"><span data-stu-id="2f23e-184">![Create a Session Tabs hosted control](../unified-service-desk/media/usd-create-session-tabs-hosted-control.png "Create a Session Tabs hosted control")</span></span>  
  
3. <span data-ttu-id="2f23e-185">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-185">Click **Save**.</span></span>  
  
<a name="Step4"></a>   
## <a name="step-4-create-a-window-navigation-rule-to-display-the-account-record-in-a-session"></a><span data-ttu-id="2f23e-186">Bước 4: Tạo quy tắc chuyển hướng cửa sổ để hiển thị hồ sơ tài khoản trong phiên</span><span class="sxs-lookup"><span data-stu-id="2f23e-186">Step 4: Create a window navigation rule to display the account record in a session</span></span>  
 <span data-ttu-id="2f23e-187">Trong bước này, bạn sẽ tạo một quy tắc chuyển hướng cửa sổ hiển thị hồ sơ trong phiên khi người dùng nhấp vào bất kỳ tài khoản nào trong cửa sổ kết quả tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="2f23e-187">In this step, you’ll create a window navigation rule that displays the record in a session when the user clicks on any of the accounts in the search results window.</span></span>  
  
1. <span data-ttu-id="2f23e-188">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="2f23e-188">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="2f23e-189">Click **Window Navigation Rules**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-189">Click **Window Navigation Rules**.</span></span>  
  
4. <span data-ttu-id="2f23e-190">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-190">Click **New**.</span></span>  
  
5. <span data-ttu-id="2f23e-191">On the **New Window Navigation Rule** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="2f23e-191">On the **New Window Navigation Rule** page, specify the following values.</span></span>  
  
   |<span data-ttu-id="2f23e-192">Trường</span><span class="sxs-lookup"><span data-stu-id="2f23e-192">Field</span></span>|<span data-ttu-id="2f23e-193">Giá trị</span><span class="sxs-lookup"><span data-stu-id="2f23e-193">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="2f23e-194">Tên</span><span class="sxs-lookup"><span data-stu-id="2f23e-194">Name</span></span>|<span data-ttu-id="2f23e-195">Quy tắc Phiên Tài khoản contoso</span><span class="sxs-lookup"><span data-stu-id="2f23e-195">Contoso Account Session Rule</span></span>|  
   |<span data-ttu-id="2f23e-196">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="2f23e-196">Order</span></span>|<span data-ttu-id="2f23e-197">5</span><span class="sxs-lookup"><span data-stu-id="2f23e-197">5</span></span>|  
   |<span data-ttu-id="2f23e-198">Từ</span><span class="sxs-lookup"><span data-stu-id="2f23e-198">From</span></span>|<span data-ttu-id="2f23e-199">Tìm kiếm tài khoản Contoso</span><span class="sxs-lookup"><span data-stu-id="2f23e-199">Contoso Accounts Search</span></span>|  
   |<span data-ttu-id="2f23e-200">Thực thể</span><span class="sxs-lookup"><span data-stu-id="2f23e-200">Entity</span></span>|<span data-ttu-id="2f23e-201">tài khoản</span><span class="sxs-lookup"><span data-stu-id="2f23e-201">account</span></span>|  
   |<span data-ttu-id="2f23e-202">Loại định tuyến</span><span class="sxs-lookup"><span data-stu-id="2f23e-202">Route Type</span></span>|<span data-ttu-id="2f23e-203">Bật lên</span><span class="sxs-lookup"><span data-stu-id="2f23e-203">Popup</span></span>|  
   |<span data-ttu-id="2f23e-204">Điểm đến</span><span class="sxs-lookup"><span data-stu-id="2f23e-204">Destination</span></span>|<span data-ttu-id="2f23e-205">Tab</span><span class="sxs-lookup"><span data-stu-id="2f23e-205">Tab</span></span>|  
   |<span data-ttu-id="2f23e-206">Hành động</span><span class="sxs-lookup"><span data-stu-id="2f23e-206">Action</span></span>|<span data-ttu-id="2f23e-207">Tạo phiên làm việc</span><span class="sxs-lookup"><span data-stu-id="2f23e-207">Create Session</span></span>|  
   |<span data-ttu-id="2f23e-208">Tab Mục tiêu</span><span class="sxs-lookup"><span data-stu-id="2f23e-208">Target Tab</span></span>|<span data-ttu-id="2f23e-209">Phiên Tài khoản contoso</span><span class="sxs-lookup"><span data-stu-id="2f23e-209">Contoso Account Session</span></span>|  
   |<span data-ttu-id="2f23e-210">Hiển thị Tab</span><span class="sxs-lookup"><span data-stu-id="2f23e-210">Show Tab</span></span>|<span data-ttu-id="2f23e-211">Contoso Account Session</span><span class="sxs-lookup"><span data-stu-id="2f23e-211">Contoso Account Session</span></span>|  
   |<span data-ttu-id="2f23e-212">Hide Command Bar</span><span class="sxs-lookup"><span data-stu-id="2f23e-212">Hide Command Bar</span></span>|<span data-ttu-id="2f23e-213">Không</span><span class="sxs-lookup"><span data-stu-id="2f23e-213">No</span></span>|  
   |<span data-ttu-id="2f23e-214">Hide Navigation Bar</span><span class="sxs-lookup"><span data-stu-id="2f23e-214">Hide Navigation Bar</span></span>|<span data-ttu-id="2f23e-215">Có</span><span class="sxs-lookup"><span data-stu-id="2f23e-215">Yes</span></span>|  
  
   <span data-ttu-id="2f23e-216">![Create a window navigation rule](../unified-service-desk/media/usd-create-window-navigation-rule.png "Create a window navigation rule")</span><span class="sxs-lookup"><span data-stu-id="2f23e-216">![Create a window navigation rule](../unified-service-desk/media/usd-create-window-navigation-rule.png "Create a window navigation rule")</span></span>  
  
6. <span data-ttu-id="2f23e-217">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-217">Click **Save**.</span></span>  
  
<a name="Step5"></a>   
## <a name="step-5-add-the-controls-to-the-configuration"></a><span data-ttu-id="2f23e-218">Step 5: Add the controls to the configuration</span><span class="sxs-lookup"><span data-stu-id="2f23e-218">Step 5: Add the controls to the configuration</span></span>  
 <span data-ttu-id="2f23e-219">Trong bước này, bạn sẽ thêm cuộc gọi hành động, sự kiện, kiểm soát tổ chức và nguyên tắc điều hướng cửa sổ mà bạn đã cấu hình trong cách này thành **Cấu hình Contoso** để hiển thị các kiểm soát này cho người dùng được chỉ định cho cấu hình này.</span><span class="sxs-lookup"><span data-stu-id="2f23e-219">In this step, you’ll add the action call, event, hosted controls, and window navigation rule configured in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span></span> <span data-ttu-id="2f23e-220">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="2f23e-220">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span>  
  
 <span data-ttu-id="2f23e-221">Add the following to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-221">Add the following to **Contoso Configuration**.</span></span>  
  
|<span data-ttu-id="2f23e-222">Tên kiểm soát</span><span class="sxs-lookup"><span data-stu-id="2f23e-222">Control name</span></span>|<span data-ttu-id="2f23e-223">Loại kiểm soát</span><span class="sxs-lookup"><span data-stu-id="2f23e-223">Control type</span></span>|  
|------------------|------------------|  
|<span data-ttu-id="2f23e-224">Các cuộc gọi hành động contoso: Đóng Tìm kiếm tài khoản</span><span class="sxs-lookup"><span data-stu-id="2f23e-224">Contoso Action Call: Close Accounts Search</span></span>|<span data-ttu-id="2f23e-225">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="2f23e-225">Action call</span></span>|  
|<span data-ttu-id="2f23e-226">Duyệt Tài liệu hoàn chỉnh</span><span class="sxs-lookup"><span data-stu-id="2f23e-226">BrowserDocumentComplete</span></span>|<span data-ttu-id="2f23e-227">Sự kiện cho kiểm soát tổ chức Phiên tài khoản Contoso.</span><span class="sxs-lookup"><span data-stu-id="2f23e-227">Event for the Contoso Account Session hosted control</span></span>|  
|<span data-ttu-id="2f23e-228">Phiên Tài khoản contoso</span><span class="sxs-lookup"><span data-stu-id="2f23e-228">Contoso Account Session</span></span>|<span data-ttu-id="2f23e-229">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="2f23e-229">Hosted Control</span></span>|  
|<span data-ttu-id="2f23e-230">Tab phiên Contoso</span><span class="sxs-lookup"><span data-stu-id="2f23e-230">Contoso Session Tab</span></span>|<span data-ttu-id="2f23e-231">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="2f23e-231">Hosted Control</span></span>|  
|<span data-ttu-id="2f23e-232">Quy tắc Phiên Tài khoản contoso</span><span class="sxs-lookup"><span data-stu-id="2f23e-232">Contoso Account Session Rule</span></span>|<span data-ttu-id="2f23e-233">Window navigation rule</span><span class="sxs-lookup"><span data-stu-id="2f23e-233">Window navigation rule</span></span>|  
  
 <span data-ttu-id="2f23e-234">To add a control to the configuration:</span><span class="sxs-lookup"><span data-stu-id="2f23e-234">To add a control to the configuration:</span></span>  
  
1. <span data-ttu-id="2f23e-235">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="2f23e-235">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="2f23e-236">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-236">Click **Configuration**.</span></span>  
  
4. <span data-ttu-id="2f23e-237">Click **Contoso Configuration** to open the definition.</span><span class="sxs-lookup"><span data-stu-id="2f23e-237">Click **Contoso Configuration** to open the definition.</span></span>  
  
5. <span data-ttu-id="2f23e-238">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-238">On the nav bar, click the down arrow next to **Contoso Configuration**, and select **Action Calls**.</span></span>  
  
6. <span data-ttu-id="2f23e-239">Trên trang tiếp theo, bấm vào **Thêm Cuộc gọi Hành động Hiện có**, nhập “`Contoso Action Call: Close Accounts Search`” vào thanh tìm kiếm, sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="2f23e-239">On the next page, click **Add Existing Action Call**, type “`Contoso Action Call: Close Accounts Search`” in the search bar, and then press ENTER or click the search icon.</span></span>  
  
7. <span data-ttu-id="2f23e-240">Trong hộp kết quả tìm kiếm, hãy nhấp vào cuộc gọi hành động để thêm vào **Cấu hình Contoso**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-240">In the search result box, click the action call to add it to **Contoso Configuration**.</span></span>  
  
8. <span data-ttu-id="2f23e-241">Tương tự, thêm sự kiện, kiểm soát tổ chức và nguyên tắc điều hướng cửa sổ bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Sự kiện** **Kiểm soát tổ chức** và **Nguyên tắc điều hướng cửa sổ** lần lượt.</span><span class="sxs-lookup"><span data-stu-id="2f23e-241">Similarly, add the event, hosted controls and window navigation rule by clicking the down arrow next to **Contoso Configuration**, and clicking **Events** **Hosted Controls** and **Window navigation Rules** respectively.</span></span>  
  
9. <span data-ttu-id="2f23e-242">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-242">Click **Save**.</span></span>  
  
<a name="Step6"></a>   
## <a name="step-6-test-the-application"></a><span data-ttu-id="2f23e-243">Step 6: Test the application</span><span class="sxs-lookup"><span data-stu-id="2f23e-243">Step 6: Test the application</span></span>  
  
1. <span data-ttu-id="2f23e-244">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured Unified Service Desk by using the same user credentials that is assigned to Contoso Configuration in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="2f23e-244">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured Unified Service Desk by using the same user credentials that is assigned to Contoso Configuration in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span> <span data-ttu-id="2f23e-245">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to CRM instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span><span class="sxs-lookup"><span data-stu-id="2f23e-245">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to CRM instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span></span>  
  
2. <span data-ttu-id="2f23e-246">To display the account records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance, click the down arrow next to the **Search** button in the toolbar, and then click **Account**.</span><span class="sxs-lookup"><span data-stu-id="2f23e-246">To display the account records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance, click the down arrow next to the **Search** button in the toolbar, and then click **Account**.</span></span>  
  
3. <span data-ttu-id="2f23e-247">Click any of the account records to display the respective account information in a session; the information is displayed under a session tab. Note that the name of the hosted control tab that contains the account record automatically displays the account name because earlier you used replacement parameters to dynamically display the current account name instead of a static value.</span><span class="sxs-lookup"><span data-stu-id="2f23e-247">Click any of the account records to display the respective account information in a session; the information is displayed under a session tab. Note that the name of the hosted control tab that contains the account record automatically displays the account name because earlier you used replacement parameters to dynamically display the current account name instead of a static value.</span></span>  
  
   <span data-ttu-id="2f23e-248">![Account record displayed in a session](../unified-service-desk/media/usd-account-record-session.png "Account record displayed in a session")</span><span class="sxs-lookup"><span data-stu-id="2f23e-248">![Account record displayed in a session](../unified-service-desk/media/usd-account-record-session.png "Account record displayed in a session")</span></span>  
  
4. <span data-ttu-id="2f23e-249">Nếu bạn mở một hồ sơ tài khoản khác, nó sẽ được hiển thị trong một phiên khác trong ứng dụng khách của bạn.</span><span class="sxs-lookup"><span data-stu-id="2f23e-249">If you open another account record, it will be displayed in another session in your client application.</span></span> <span data-ttu-id="2f23e-250">Để mở một tài khoản khác, bấm vào mũi tên xuống bên cạnh nút **Tìm kiếm**, hãy nhấp vào **Tài khoản**, và sau đó nhấp vào tên tài khoản để hiển thị các thông tin tài khoản trong một phiên khác.</span><span class="sxs-lookup"><span data-stu-id="2f23e-250">To open another account, click the down arrow next to the **Search** button, click **Account**, and then click an account name to display the account information in another session.</span></span>  
  
   <span data-ttu-id="2f23e-251">![Multiple sessions in Unified Service Desk](../unified-service-desk/media/usd-multiple-sessions.png "Multiple sessions in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="2f23e-251">![Multiple sessions in Unified Service Desk](../unified-service-desk/media/usd-multiple-sessions.png "Multiple sessions in Unified Service Desk")</span></span>  
  
<a name="Conclusion"></a>   
## <a name="conclusion"></a><span data-ttu-id="2f23e-252">Kết luận</span><span class="sxs-lookup"><span data-stu-id="2f23e-252">Conclusion</span></span>  
 <span data-ttu-id="2f23e-253">In this walkthrough, you learned how to use the session hosted control and window navigation rules to display [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records in a session in your agent application.</span><span class="sxs-lookup"><span data-stu-id="2f23e-253">In this walkthrough, you learned how to use the session hosted control and window navigation rules to display [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps records in a session in your agent application.</span></span> <span data-ttu-id="2f23e-254">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span><span class="sxs-lookup"><span data-stu-id="2f23e-254">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2f23e-255">Try the next walkthrough to present enhanced session information in your agent application: [Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md).</span><span class="sxs-lookup"><span data-stu-id="2f23e-255">Try the next walkthrough to present enhanced session information in your agent application: [Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="2f23e-256">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="2f23e-256">See also</span></span>  
 [<span data-ttu-id="2f23e-257">Walkthrough 1: Build a simple agent application</span><span class="sxs-lookup"><span data-stu-id="2f23e-257">Walkthrough 1: Build a simple agent application</span></span>](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)   
 
 [<span data-ttu-id="2f23e-258">Walkthrough 2: Display an external webpage in your agent application</span><span class="sxs-lookup"><span data-stu-id="2f23e-258">Walkthrough 2: Display an external webpage in your agent application</span></span>](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md)   
 
 [<span data-ttu-id="2f23e-259">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application</span><span class="sxs-lookup"><span data-stu-id="2f23e-259">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application</span></span>](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md)   
 
 [<span data-ttu-id="2f23e-260">Walkthrough 6: Configure the Debugger hosted control in your agent application</span><span class="sxs-lookup"><span data-stu-id="2f23e-260">Walkthrough 6: Configure the Debugger hosted control in your agent application</span></span>](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md)   
 
 [<span data-ttu-id="2f23e-261">Walkthrough 7: Configure agent scripting in your agent application</span><span class="sxs-lookup"><span data-stu-id="2f23e-261">Walkthrough 7: Configure agent scripting in your agent application</span></span>](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md)   
 
 [<span data-ttu-id="2f23e-262">Unified Service Desk Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="2f23e-262">Unified Service Desk Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
