---
title: 'Walkthrough 1: Build a simple agent application in Unified Service Desk for Dynamics 365 for Customer Engagement apps (Unified Interface apps) (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: Demonstrates how to set up a basic agent application from scratch using Unified Service Desk that can connect to Customer Engagement.
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
ms.assetid: 75042EF8-9CA4-464B-A587-47B1F8265210
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
ms.openlocfilehash: da14ff2b3c3ce13a79701d5036ae79b2f7428098
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387075"
---
# <a name="walkthrough-1-build-a-simple-agent-application-for-unified-interface-apps"></a><span data-ttu-id="61dd4-103">Walkthrough 1: Build a simple agent application for Unified Interface Apps</span><span class="sxs-lookup"><span data-stu-id="61dd4-103">Walkthrough 1: Build a simple agent application for Unified Interface Apps</span></span>
<span data-ttu-id="61dd4-104">This walkthrough demonstrates how to set up a basic agent application from scratch using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] that can connect to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="61dd4-104">This walkthrough demonstrates how to set up a basic agent application from scratch using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] that can connect to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="61dd4-105">Ứng dụng tổng đài viên này cung cấp cho bạn máy tính để bàn trống không có bất kỳ chức năng và bạn có thể sử dụng nó khi bạn đi qua phần còn lại của các cách trong phần này.</span><span class="sxs-lookup"><span data-stu-id="61dd4-105">This agent application provides you with an empty desktop without any functionality, and you can use it when you go through the rest of the walkthroughs in this section.</span></span> <span data-ttu-id="61dd4-106">In this walkthrough, you’ll use the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration to filter out existing controls in the "New Environment" sample application package from appearing in your agent application.</span><span class="sxs-lookup"><span data-stu-id="61dd4-106">In this walkthrough, you’ll use the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration to filter out existing controls in the "New Environment" sample application package from appearing in your agent application.</span></span>
  
## <a name="prerequisites"></a><span data-ttu-id="61dd4-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="61dd4-107">Prerequisites</span></span>  
  
- <span data-ttu-id="61dd4-108">A [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] package must be deployed on your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance, and the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application must already be installed to test the application at the end of the walkthrough.</span><span class="sxs-lookup"><span data-stu-id="61dd4-108">A [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] package must be deployed on your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance, and the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application must already be installed to test the application at the end of the walkthrough.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="61dd4-109">[Install, upgrade, and deploy Unified Service Desk](../unified-service-desk/admin/install-upgrade-deploy-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="61dd4-109">[Install, upgrade, and deploy Unified Service Desk](../unified-service-desk/admin/install-upgrade-deploy-unified-service-desk.md)</span></span>  
  
- <span data-ttu-id="61dd4-110">You must have required [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps permissions to configure [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] and access the required [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps entities.</span><span class="sxs-lookup"><span data-stu-id="61dd4-110">You must have required [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps permissions to configure [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] and access the required [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps entities.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="61dd4-111">[Access management in Unified Service Desk](../unified-service-desk/admin/security-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="61dd4-111">[Access management in Unified Service Desk](../unified-service-desk/admin/security-unified-service-desk.md)</span></span>  
  
- <span data-ttu-id="61dd4-112">You must be familiar with the following concepts in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="61dd4-112">You must be familiar with the following concepts in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  
  
  - [<span data-ttu-id="61dd4-113">Kiểm soát Tổ chức Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="61dd4-113">Unified Service Desk Hosted Controls</span></span>](../unified-service-desk/unified-service-desk-hosted-controls.md)  
  
  - <span data-ttu-id="61dd4-114">Ba loại kiểm soát tổ chức này: Trình quản lý kết nối, trình quản lý chung và Bố cục bảng điều khiển.</span><span class="sxs-lookup"><span data-stu-id="61dd4-114">These three types of hosted controls: Connection Manager, Global Manager, and Panel Layout.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="61dd4-115">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span><span class="sxs-lookup"><span data-stu-id="61dd4-115">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span></span>  
  
  - <span data-ttu-id="61dd4-116">Lọc quyền truy sử dụng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="61dd4-116">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="61dd4-117">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="61dd4-117">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span></span>  
  
<a name="Top"></a>   
## <a name="in-this-walkthrough"></a><span data-ttu-id="61dd4-118">In This Walkthrough</span><span class="sxs-lookup"><span data-stu-id="61dd4-118">In This Walkthrough</span></span>  
 [<span data-ttu-id="61dd4-119">Bước 1: Tạo ra kiểm soát tổ chức cơ bản</span><span class="sxs-lookup"><span data-stu-id="61dd4-119">Step 1: Create the basic hosted controls</span></span>](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md#Step1) 
  
 [<span data-ttu-id="61dd4-120">Bước 2: Thêm kiểm soát tổ chức vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="61dd4-120">Step 2: Add the hosted controls to a configuration</span></span>](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md#Step2)  
  
 [<span data-ttu-id="61dd4-121">Bước 3: Chỉ định người dùng cho cấu hình</span><span class="sxs-lookup"><span data-stu-id="61dd4-121">Step 3: Assign users to the configuration</span></span>](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md#Step3)  
  
 [<span data-ttu-id="61dd4-122">Bước 4: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="61dd4-122">Step 4: Test the application</span></span>](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md#Step4)  
  
 [<span data-ttu-id="61dd4-123">Kết luận</span><span class="sxs-lookup"><span data-stu-id="61dd4-123">Conclusion</span></span>](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md#Conclusion)  
  
<a name="Step1"></a>   
## <a name="step-1-create-the-basic-hosted-controls"></a><span data-ttu-id="61dd4-124">Bước 1: Tạo ra kiểm soát tổ chức cơ bản</span><span class="sxs-lookup"><span data-stu-id="61dd4-124">Step 1: Create the basic hosted controls</span></span>  
 <span data-ttu-id="61dd4-125">Create the following three types of hosted control so that the application can connect to an instance of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps: Connection Manager, Global Manager, and Panel Type.</span><span class="sxs-lookup"><span data-stu-id="61dd4-125">Create the following three types of hosted control so that the application can connect to an instance of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps: Connection Manager, Global Manager, and Panel Type.</span></span>  
  
1. <span data-ttu-id="61dd4-126">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="61dd4-126">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="61dd4-127">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="61dd4-127">Click **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="61dd4-128">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="61dd4-128">Click **New**.</span></span>  
  
5. <span data-ttu-id="61dd4-129">On the **New Hosted Control** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="61dd4-129">On the **New Hosted Control** page, specify the following values.</span></span>  
  
   |<span data-ttu-id="61dd4-130">Trường</span><span class="sxs-lookup"><span data-stu-id="61dd4-130">Field</span></span>|<span data-ttu-id="61dd4-131">Giá trị</span><span class="sxs-lookup"><span data-stu-id="61dd4-131">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="61dd4-132">Tên</span><span class="sxs-lookup"><span data-stu-id="61dd4-132">Name</span></span>|<span data-ttu-id="61dd4-133">Trình Quản lý kết nối contoso</span><span class="sxs-lookup"><span data-stu-id="61dd4-133">Contoso Connection Manager</span></span>|  
   |<span data-ttu-id="61dd4-134">Thứ tự Sắp xếp</span><span class="sxs-lookup"><span data-stu-id="61dd4-134">Sort Order</span></span>|<span data-ttu-id="61dd4-135">1</span><span class="sxs-lookup"><span data-stu-id="61dd4-135">1</span></span>|  
   |<span data-ttu-id="61dd4-136">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="61dd4-136">USD Component Type</span></span>|<span data-ttu-id="61dd4-137">Trình Quản lý kết nối</span><span class="sxs-lookup"><span data-stu-id="61dd4-137">Connection Manager</span></span>|  
  
   <span data-ttu-id="61dd4-138">![Connection Manager hosted control](../unified-service-desk/media/crm-itpro-usd-wt01-01.png "Connection Manager hosted control")</span><span class="sxs-lookup"><span data-stu-id="61dd4-138">![Connection Manager hosted control](../unified-service-desk/media/crm-itpro-usd-wt01-01.png "Connection Manager hosted control")</span></span>
  
6. <span data-ttu-id="61dd4-139">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="61dd4-139">Click **Save**.</span></span>  
  
7. <span data-ttu-id="61dd4-140">Bấm vào **Mới** để tạo kiểm soát tổ chức khác.</span><span class="sxs-lookup"><span data-stu-id="61dd4-140">Click **New** to create another hosted control.</span></span>  
  
8. <span data-ttu-id="61dd4-141">On the **New Hosted Control** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="61dd4-141">On the **New Hosted Control** page, specify the following values.</span></span>  
  
   |<span data-ttu-id="61dd4-142">Trường</span><span class="sxs-lookup"><span data-stu-id="61dd4-142">Field</span></span>|<span data-ttu-id="61dd4-143">Giá trị</span><span class="sxs-lookup"><span data-stu-id="61dd4-143">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="61dd4-144">Tên</span><span class="sxs-lookup"><span data-stu-id="61dd4-144">Name</span></span>|<span data-ttu-id="61dd4-145">Contoso Global Manager</span><span class="sxs-lookup"><span data-stu-id="61dd4-145">Contoso Global Manager</span></span>|  
   |<span data-ttu-id="61dd4-146">Thứ tự Sắp xếp</span><span class="sxs-lookup"><span data-stu-id="61dd4-146">Sort Order</span></span>|<span data-ttu-id="61dd4-147">2</span><span class="sxs-lookup"><span data-stu-id="61dd4-147">2</span></span>|  
   |<span data-ttu-id="61dd4-148">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="61dd4-148">USD Component Type</span></span>|<span data-ttu-id="61dd4-149">Trình Quản lý chung</span><span class="sxs-lookup"><span data-stu-id="61dd4-149">Global Manager</span></span>|  
  
   <span data-ttu-id="61dd4-150">![Global Manager hosted control](../unified-service-desk/media/crm-itpro-usd-wt01-02.png "Global Manager hosted control")</span><span class="sxs-lookup"><span data-stu-id="61dd4-150">![Global Manager hosted control](../unified-service-desk/media/crm-itpro-usd-wt01-02.png "Global Manager hosted control")</span></span>
  
9. <span data-ttu-id="61dd4-151">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="61dd4-151">Click **Save**.</span></span>  
  
10. <span data-ttu-id="61dd4-152">Click **New** to create another hosted control.</span><span class="sxs-lookup"><span data-stu-id="61dd4-152">Click **New** to create another hosted control.</span></span>  
  
11. <span data-ttu-id="61dd4-153">On the **New Hosted Control** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="61dd4-153">On the **New Hosted Control** page, specify the following values.</span></span>  
  
    |<span data-ttu-id="61dd4-154">Trường</span><span class="sxs-lookup"><span data-stu-id="61dd4-154">Field</span></span>|<span data-ttu-id="61dd4-155">Giá trị</span><span class="sxs-lookup"><span data-stu-id="61dd4-155">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="61dd4-156">Tên</span><span class="sxs-lookup"><span data-stu-id="61dd4-156">Name</span></span>|<span data-ttu-id="61dd4-157">Bố cục Bảng điều khiển chính Contoso</span><span class="sxs-lookup"><span data-stu-id="61dd4-157">Contoso Main Panel Layout</span></span>|  
    |<span data-ttu-id="61dd4-158">Loại Thành phần USD</span><span class="sxs-lookup"><span data-stu-id="61dd4-158">USD Component Type</span></span>|<span data-ttu-id="61dd4-159">Bố cục bảng điều khiển</span><span class="sxs-lookup"><span data-stu-id="61dd4-159">Panel Layout</span></span>|  
    |<span data-ttu-id="61dd4-160">Loại bảng điều khiển</span><span class="sxs-lookup"><span data-stu-id="61dd4-160">Panel Type</span></span>|<span data-ttu-id="61dd4-161">Bảng điều khiển chính tiêu chuẩn</span><span class="sxs-lookup"><span data-stu-id="61dd4-161">Standard Main Panel</span></span>|  
    |<span data-ttu-id="61dd4-162">Application is Dynamic</span><span class="sxs-lookup"><span data-stu-id="61dd4-162">Application is Dynamic</span></span>|<span data-ttu-id="61dd4-163">Không</span><span class="sxs-lookup"><span data-stu-id="61dd4-163">No</span></span>|  
    |<span data-ttu-id="61dd4-164">User Can Close</span><span class="sxs-lookup"><span data-stu-id="61dd4-164">User Can Close</span></span>|<span data-ttu-id="61dd4-165">Bỏ chọn</span><span class="sxs-lookup"><span data-stu-id="61dd4-165">Unchecked</span></span>|  
  
    <span data-ttu-id="61dd4-166">![Panel Layout hosted control](../unified-service-desk/media/crm-itpro-usd-wt01-03.png "Panel Layout hosted control")</span><span class="sxs-lookup"><span data-stu-id="61dd4-166">![Panel Layout hosted control](../unified-service-desk/media/crm-itpro-usd-wt01-03.png "Panel Layout hosted control")</span></span>  
  
12. <span data-ttu-id="61dd4-167">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="61dd4-167">Click **Save**.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="61dd4-168">Nếu bạn không tạo loại **Bố cục bảng điều khiển** của kiểm soát tổ chức trong ứng dụng tổng đài viên của bạn, bố cục bảng điều khiển mặc định, **Bảng điều khiển chính tiêu chuẩn**, được tạo tự động khi bạn chạy ứng dụng khách.</span><span class="sxs-lookup"><span data-stu-id="61dd4-168">If you don’t create a **Panel Layout** type of hosted control in your agent application, the default panel layout, **Standard Main Panel**, is created automatically when you run the client application.</span></span> 
  
<a name="Step2"></a>   
## <a name="step-2-add-the-hosted-controls-to-a-configuration"></a><span data-ttu-id="61dd4-169">Bước 2: Thêm kiểm soát tổ chức vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="61dd4-169">Step 2: Add the hosted controls to a configuration</span></span>  
 <span data-ttu-id="61dd4-170">Cấu hình trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] giúp bạn lọc các truy cập vào các thành phần được hiển thị trong ứng dụng tổng đài viên cho người dùng.</span><span class="sxs-lookup"><span data-stu-id="61dd4-170">A configuration in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] helps you filter access to components that are displayed in the agent application to a user.</span></span> <span data-ttu-id="61dd4-171">Trong bước này, tạo cấu hình, và sau đó thêm kiểm soát tổ chức được tạo ra trước đó vào cấu hình.</span><span class="sxs-lookup"><span data-stu-id="61dd4-171">In this step, create a configuration, and then add the hosted controls created earlier to the configuration.</span></span>  
  
1. <span data-ttu-id="61dd4-172">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="61dd4-172">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="61dd4-173">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="61dd4-173">Click **Configuration**.</span></span>  
  
4. <span data-ttu-id="61dd4-174">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="61dd4-174">Click **New**.</span></span>  
  
5. <span data-ttu-id="61dd4-175">On the **New Configuration** page, type `Contoso Configuration` as the name of the configuration, and click **Save**.</span><span class="sxs-lookup"><span data-stu-id="61dd4-175">On the **New Configuration** page, type `Contoso Configuration` as the name of the configuration, and click **Save**.</span></span>  
  
6. <span data-ttu-id="61dd4-176">Sau khi cấu hình mới được lưu, trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh tên cấu hình, và sau đó chọn **Kiểm soát tổ chức**.</span><span class="sxs-lookup"><span data-stu-id="61dd4-176">After the new configuration is saved, on the nav bar, click the down arrow next to the configuration name, and then select **Hosted Controls**.</span></span>  
  
7. <span data-ttu-id="61dd4-177">Bấm vào **Thêm kiểm soát tổ chức hiện có**, nhập `Contoso` trong thanh tìm kiếm và sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="61dd4-177">Click **Add Existing Hosted Control**, type `Contoso` in the search bar, and then press ENTER or click the search icon.</span></span>  
  
8. <span data-ttu-id="61dd4-178">Ba hình thức kiểm soát tổ chức được thêm trước đó hiển thị trong kết quả tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="61dd4-178">The three hosted controls added earlier display in the search results.</span></span> <span data-ttu-id="61dd4-179">Nhấp vào liên kết **Tìm kiếm thêm Hồ sơ**.</span><span class="sxs-lookup"><span data-stu-id="61dd4-179">Click the **Look up more Records** link.</span></span>  
  
9. <span data-ttu-id="61dd4-180">Chọn ba kiểm soát tổ chức, bấm vào **Chọn**, và sau đó nhấp vào **thêm**.</span><span class="sxs-lookup"><span data-stu-id="61dd4-180">Select the three hosted controls, click **Select**, and then click **Add**.</span></span>  
  
   <span data-ttu-id="61dd4-181">![Add the hosted controls to the configuration](../unified-service-desk/media/crm-itpro-usd-wt01-04.PNG "Add the hosted controls to the configuration")</span><span class="sxs-lookup"><span data-stu-id="61dd4-181">![Add the hosted controls to the configuration](../unified-service-desk/media/crm-itpro-usd-wt01-04.PNG "Add the hosted controls to the configuration")</span></span>  
  
10. <span data-ttu-id="61dd4-182">Kiểm soát tổ chức được thêm vào cấu hình.</span><span class="sxs-lookup"><span data-stu-id="61dd4-182">The hosted controls are added to the configuration.</span></span> <span data-ttu-id="61dd4-183">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="61dd4-183">Click **Save**.</span></span>  
  
<a name="Step3"></a>   
## <a name="step-3-assign-users-to-the-configuration"></a><span data-ttu-id="61dd4-184">Bước 3: Chỉ định người dùng cho cấu hình</span><span class="sxs-lookup"><span data-stu-id="61dd4-184">Step 3: Assign users to the configuration</span></span>  
 <span data-ttu-id="61dd4-185">Trong bước này, chỉ định người dùng cho cấu hình do đó khi họ đăng nhập bằng cách sử dụng ứng dụng khách [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], họ chỉ có thể truy cập ba kiểm soát tổ chức đã được thêm vào cấu hình này.</span><span class="sxs-lookup"><span data-stu-id="61dd4-185">In this step, assign users to the configuration so that when they sign in using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, they can only access the three hosted controls that are added to this configuration.</span></span> <span data-ttu-id="61dd4-186">Đối với cách này, chỉ chỉ định một người dùng cho cấu hình người sẽ thử nghiệm các ứng dụng ở phần cuối của cách này.</span><span class="sxs-lookup"><span data-stu-id="61dd4-186">For this walkthrough, assign only a single user to the configuration who will be testing the application at the end of the walkthrough.</span></span>  
  
1. <span data-ttu-id="61dd4-187">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và sau đó chọn **Người dùng được gán**.</span><span class="sxs-lookup"><span data-stu-id="61dd4-187">On the nav bar, click the down arrow next to the **Contoso Configuration**, and then select **Assigned Users**.</span></span>  
  
2. <span data-ttu-id="61dd4-188">Trên trang tiếp theo, bấm vào **Thêm Người dùng hiện có**, nhập tên của người dùng trong thanh tìm kiếm, sau đó nhấn ENTER hoặc nhấp biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="61dd4-188">On the next page, click **Add Existing User**, type the name of the user in the search bar, and then press ENTER or click the search icon.</span></span>  
  
3. <span data-ttu-id="61dd4-189">Từ kết quả tìm kiếm, nhấp vào tên người dùng mà bạn muốn được chỉ định cho cấu hình.</span><span class="sxs-lookup"><span data-stu-id="61dd4-189">From the search result, click the user name that you want to be assigned to the configuration.</span></span> <span data-ttu-id="61dd4-190">Người dùng được thêm vào cấu hình.</span><span class="sxs-lookup"><span data-stu-id="61dd4-190">The user is added to the configuration.</span></span> <span data-ttu-id="61dd4-191">Trong trường hợp này, chỉ định **Randy Blythe** cho cấu hình.</span><span class="sxs-lookup"><span data-stu-id="61dd4-191">In this case, assign **Randy Blythe** to the configuration.</span></span> <span data-ttu-id="61dd4-192">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="61dd4-192">Click **Save**.</span></span>  
  
   <span data-ttu-id="61dd4-193">![User added to the configuration](../unified-service-desk/media/crm-itpro-usd-wt01-05.png "User added to the configuration")</span><span class="sxs-lookup"><span data-stu-id="61dd4-193">![User added to the configuration](../unified-service-desk/media/crm-itpro-usd-wt01-05.png "User added to the configuration")</span></span> 
  
<a name="Step4"></a>   
## <a name="step-4-test-the-application"></a><span data-ttu-id="61dd4-194">Step 4: Test the application</span><span class="sxs-lookup"><span data-stu-id="61dd4-194">Step 4: Test the application</span></span>  
 <span data-ttu-id="61dd4-195">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in the previous step.</span><span class="sxs-lookup"><span data-stu-id="61dd4-195">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in the previous step.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="61dd4-196">[Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span><span class="sxs-lookup"><span data-stu-id="61dd4-196">[Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span></span>  
  
 <span data-ttu-id="61dd4-197">Ứng dụng tổng đài viên của bạn sẽ trông như sau.</span><span class="sxs-lookup"><span data-stu-id="61dd4-197">Your agent application will look like the following.</span></span>  
  
 <span data-ttu-id="61dd4-198">![Basic agent application without any controls](../unified-service-desk/media/crm-itpro-usd-wt01-06.png "Basic agent application without any controls")</span><span class="sxs-lookup"><span data-stu-id="61dd4-198">![Basic agent application without any controls](../unified-service-desk/media/crm-itpro-usd-wt01-06.png "Basic agent application without any controls")</span></span>  
  
 <span data-ttu-id="61dd4-199">Máy tính để bàn trong ứng dụng tổng đài viên là máy tính trống bởi vì không có kiểm soát nào khác được thêm vào **Cấu hình Contoso** ngoài kiểm soát tổ chức cần thiết để thiết lập ứng dụng tổng đài viên cơ bản.</span><span class="sxs-lookup"><span data-stu-id="61dd4-199">The desktop in the agent application is empty because no other controls were added to **Contoso Configuration** apart from the hosted controls required for setting up a basic agent application.</span></span> <span data-ttu-id="61dd4-200">Trong phần còn lại của các cách, bạn sẽ thấy kiểm soát xuất hiện trong ứng dụng tổng đài viên vì bạn dần dần đặt cấu hình và thêm các kiểm soát vào **Cấu hình Contoso**.</span><span class="sxs-lookup"><span data-stu-id="61dd4-200">In the rest of the walkthroughs, you’ll see controls appear in the agent application as you progressively configure and add controls to **Contoso Configuration**.</span></span> 
  
<a name="Conclusion"></a>   
## <a name="conclusion"></a><span data-ttu-id="61dd4-201">Kết luận</span><span class="sxs-lookup"><span data-stu-id="61dd4-201">Conclusion</span></span>  
 <span data-ttu-id="61dd4-202">In this walkthrough, you saw how to quickly build a basic agent application that can connect to an instance of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="61dd4-202">In this walkthrough, you saw how to quickly build a basic agent application that can connect to an instance of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span></span> <span data-ttu-id="61dd4-203">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span><span class="sxs-lookup"><span data-stu-id="61dd4-203">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="61dd4-204">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="61dd4-204">See also</span></span>

 [<span data-ttu-id="61dd4-205">Support for Unified Interface Apps in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="61dd4-205">Support for Unified Interface Apps in Unified Service Desk</span></span>](../unified-service-desk/admin/Support-unified-interfaces-apps-usd.md)

 [<span data-ttu-id="61dd4-206">Unified Interface Page (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="61dd4-206">Unified Interface Page (Hosted Control)</span></span>](../unified-service-desk/unified-interface-page-hosted-control.md)

 [<span data-ttu-id="61dd4-207">Unified Service Desk and Unified Interface Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="61dd4-207">Unified Service Desk and Unified Interface Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md)
  
 [<span data-ttu-id="61dd4-208">Walkthrough 2: Display an external webpage in your agent application</span><span class="sxs-lookup"><span data-stu-id="61dd4-208">Walkthrough 2: Display an external webpage in your agent application</span></span>](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md)

 [<span data-ttu-id="61dd4-209">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application</span><span class="sxs-lookup"><span data-stu-id="61dd4-209">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application</span></span>](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md)

 [<span data-ttu-id="61dd4-210">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application</span><span class="sxs-lookup"><span data-stu-id="61dd4-210">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application</span></span>](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md)

 [<span data-ttu-id="61dd4-211">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span><span class="sxs-lookup"><span data-stu-id="61dd4-211">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span></span>](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md)

 [<span data-ttu-id="61dd4-212">Walkthrough 6: Configure the Debugger hosted control in your agent application</span><span class="sxs-lookup"><span data-stu-id="61dd4-212">Walkthrough 6: Configure the Debugger hosted control in your agent application</span></span>](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md)

 [<span data-ttu-id="61dd4-213">Walkthrough 7: Configure agent scripting in your agent application</span><span class="sxs-lookup"><span data-stu-id="61dd4-213">Walkthrough 7: Configure agent scripting in your agent application</span></span>](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)
