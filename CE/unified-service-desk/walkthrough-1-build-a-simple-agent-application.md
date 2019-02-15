---
title: 'Walkthrough 1: Build a simple agent application in Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs'
description: Demonstrates how to set up a basic agent application from scratch using Unified Service Desk that can connect to Customer Engagement.
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
ms.assetid: 9e6470a9-329c-4152-bd14-d61555be1ee5
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 0e62327a4121a13553d8ee3047fe5e1163535b17
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387948"
---
# <a name="walkthrough-1-build-a-simple-agent-application"></a><span data-ttu-id="01bd8-103">Walkthrough 1: Build a simple agent application</span><span class="sxs-lookup"><span data-stu-id="01bd8-103">Walkthrough 1: Build a simple agent application</span></span>
<span data-ttu-id="01bd8-104">This walkthrough demonstrates how to set up a basic agent application from scratch using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] that can connect to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="01bd8-104">This walkthrough demonstrates how to set up a basic agent application from scratch using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] that can connect to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="01bd8-105">This agent application provides you with an empty desktop without any functionality, and you can use it when you go through the rest of the walkthroughs in this section.</span><span class="sxs-lookup"><span data-stu-id="01bd8-105">This agent application provides you with an empty desktop without any functionality, and you can use it when you go through the rest of the walkthroughs in this section.</span></span> <span data-ttu-id="01bd8-106">In this walkthrough, you’ll use the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration to filter out existing controls in the "New Environment" sample application package from appearing in your agent application.</span><span class="sxs-lookup"><span data-stu-id="01bd8-106">In this walkthrough, you’ll use the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration to filter out existing controls in the "New Environment" sample application package from appearing in your agent application.</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="01bd8-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="01bd8-107">Prerequisites</span></span>  
  
- <span data-ttu-id="01bd8-108">A [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] package must be deployed on your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance, and the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application must already be installed to test the application at the end of the walkthrough.</span><span class="sxs-lookup"><span data-stu-id="01bd8-108">A [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] package must be deployed on your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance, and the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application must already be installed to test the application at the end of the walkthrough.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="01bd8-109">[Install, upgrade, and deploy Unified Service Desk](../unified-service-desk/admin/install-upgrade-deploy-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="01bd8-109">[Install, upgrade, and deploy Unified Service Desk](../unified-service-desk/admin/install-upgrade-deploy-unified-service-desk.md)</span></span>  
  
- <span data-ttu-id="01bd8-110">You must have required [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps permissions to configure [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] and access the required [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps entities.</span><span class="sxs-lookup"><span data-stu-id="01bd8-110">You must have required [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps permissions to configure [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] and access the required [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps entities.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="01bd8-111">[Access management in Unified Service Desk](../unified-service-desk/admin/security-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="01bd8-111">[Access management in Unified Service Desk](../unified-service-desk/admin/security-unified-service-desk.md)</span></span>  
  
- <span data-ttu-id="01bd8-112">You must be familiar with the following concepts in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="01bd8-112">You must be familiar with the following concepts in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  
  
  - [<span data-ttu-id="01bd8-113">Unified Service Desk Hosted Controls</span><span class="sxs-lookup"><span data-stu-id="01bd8-113">Unified Service Desk Hosted Controls</span></span>](../unified-service-desk/unified-service-desk-hosted-controls.md)  
  
  - <span data-ttu-id="01bd8-114">These three types of hosted controls: Connection Manager, Global Manager, and Panel Layout.</span><span class="sxs-lookup"><span data-stu-id="01bd8-114">These three types of hosted controls: Connection Manager, Global Manager, and Panel Layout.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="01bd8-115">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span><span class="sxs-lookup"><span data-stu-id="01bd8-115">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)</span></span>  
  
  - <span data-ttu-id="01bd8-116">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="01bd8-116">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="01bd8-117">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="01bd8-117">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span></span>  
  
<a name="Top"></a>   
## <a name="in-this-walkthrough"></a><span data-ttu-id="01bd8-118">In This Walkthrough</span><span class="sxs-lookup"><span data-stu-id="01bd8-118">In This Walkthrough</span></span>  
 [<span data-ttu-id="01bd8-119">Bước 1: Tạo ra kiểm soát tổ chức cơ bản</span><span class="sxs-lookup"><span data-stu-id="01bd8-119">Step 1: Create the basic hosted controls</span></span>](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md#Step1)  
  
 [<span data-ttu-id="01bd8-120">Bước 2: Thêm kiểm soát tổ chức vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="01bd8-120">Step 2: Add the hosted controls to a configuration</span></span>](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md#Step2)  
  
 [<span data-ttu-id="01bd8-121">Bước 3: Chỉ định người dùng cho cấu hình</span><span class="sxs-lookup"><span data-stu-id="01bd8-121">Step 3: Assign users to the configuration</span></span>](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md#Step3)  
  
 [<span data-ttu-id="01bd8-122">Bước 4: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="01bd8-122">Step 4: Test the application</span></span>](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md#Step4)  
  
 [<span data-ttu-id="01bd8-123">Kết luận</span><span class="sxs-lookup"><span data-stu-id="01bd8-123">Conclusion</span></span>](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md#Conclusion)  
  
<a name="Step1"></a>   
## <a name="step-1-create-the-basic-hosted-controls"></a><span data-ttu-id="01bd8-124">Step 1: Create the basic hosted controls</span><span class="sxs-lookup"><span data-stu-id="01bd8-124">Step 1: Create the basic hosted controls</span></span>  
 <span data-ttu-id="01bd8-125">Create the following three types of hosted control so that the application can connect to an instance of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps: Connection Manager, Global Manager, and Panel Type.</span><span class="sxs-lookup"><span data-stu-id="01bd8-125">Create the following three types of hosted control so that the application can connect to an instance of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps: Connection Manager, Global Manager, and Panel Type.</span></span>  
  
1. <span data-ttu-id="01bd8-126">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="01bd8-126">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="01bd8-127">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="01bd8-127">Click **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="01bd8-128">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="01bd8-128">Click **New**.</span></span>  
  
5. <span data-ttu-id="01bd8-129">On the **New Hosted Control** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="01bd8-129">On the **New Hosted Control** page, specify the following values.</span></span>  
  
   |<span data-ttu-id="01bd8-130">Trường</span><span class="sxs-lookup"><span data-stu-id="01bd8-130">Field</span></span>|<span data-ttu-id="01bd8-131">Giá trị</span><span class="sxs-lookup"><span data-stu-id="01bd8-131">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="01bd8-132">Tên</span><span class="sxs-lookup"><span data-stu-id="01bd8-132">Name</span></span>|<span data-ttu-id="01bd8-133">Contoso Connection Manager</span><span class="sxs-lookup"><span data-stu-id="01bd8-133">Contoso Connection Manager</span></span>|  
   |<span data-ttu-id="01bd8-134">Thứ tự Sắp xếp</span><span class="sxs-lookup"><span data-stu-id="01bd8-134">Sort Order</span></span>|<span data-ttu-id="01bd8-135">1</span><span class="sxs-lookup"><span data-stu-id="01bd8-135">1</span></span>|  
   |<span data-ttu-id="01bd8-136">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="01bd8-136">USD Component Type</span></span>|<span data-ttu-id="01bd8-137">Trình Quản lý kết nối</span><span class="sxs-lookup"><span data-stu-id="01bd8-137">Connection Manager</span></span>|  
  
   <span data-ttu-id="01bd8-138">![Connection Manager hosted control](../unified-service-desk/media/crm-itpro-usd-wt01-01.png "Connection Manager hosted control")</span><span class="sxs-lookup"><span data-stu-id="01bd8-138">![Connection Manager hosted control](../unified-service-desk/media/crm-itpro-usd-wt01-01.png "Connection Manager hosted control")</span></span>  
  
6. <span data-ttu-id="01bd8-139">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="01bd8-139">Click **Save**.</span></span>  
  
7. <span data-ttu-id="01bd8-140">Click **New** to create another hosted control.</span><span class="sxs-lookup"><span data-stu-id="01bd8-140">Click **New** to create another hosted control.</span></span>  
  
8. <span data-ttu-id="01bd8-141">On the **New Hosted Control** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="01bd8-141">On the **New Hosted Control** page, specify the following values.</span></span>  
  
   |<span data-ttu-id="01bd8-142">Trường</span><span class="sxs-lookup"><span data-stu-id="01bd8-142">Field</span></span>|<span data-ttu-id="01bd8-143">Giá trị</span><span class="sxs-lookup"><span data-stu-id="01bd8-143">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="01bd8-144">Tên</span><span class="sxs-lookup"><span data-stu-id="01bd8-144">Name</span></span>|<span data-ttu-id="01bd8-145">Contoso Global Manager</span><span class="sxs-lookup"><span data-stu-id="01bd8-145">Contoso Global Manager</span></span>|  
   |<span data-ttu-id="01bd8-146">Thứ tự Sắp xếp</span><span class="sxs-lookup"><span data-stu-id="01bd8-146">Sort Order</span></span>|<span data-ttu-id="01bd8-147">2</span><span class="sxs-lookup"><span data-stu-id="01bd8-147">2</span></span>|  
   |<span data-ttu-id="01bd8-148">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="01bd8-148">USD Component Type</span></span>|<span data-ttu-id="01bd8-149">Trình Quản lý chung</span><span class="sxs-lookup"><span data-stu-id="01bd8-149">Global Manager</span></span>|  
  
   <span data-ttu-id="01bd8-150">![Global Manager hosted control](../unified-service-desk/media/crm-itpro-usd-wt01-02.png "Global Manager hosted control")</span><span class="sxs-lookup"><span data-stu-id="01bd8-150">![Global Manager hosted control](../unified-service-desk/media/crm-itpro-usd-wt01-02.png "Global Manager hosted control")</span></span>  
  
9. <span data-ttu-id="01bd8-151">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="01bd8-151">Click **Save**.</span></span>  
  
10. <span data-ttu-id="01bd8-152">Click **New** to create another hosted control.</span><span class="sxs-lookup"><span data-stu-id="01bd8-152">Click **New** to create another hosted control.</span></span>  
  
11. <span data-ttu-id="01bd8-153">On the **New Hosted Control** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="01bd8-153">On the **New Hosted Control** page, specify the following values.</span></span>  
  
    |<span data-ttu-id="01bd8-154">Trường</span><span class="sxs-lookup"><span data-stu-id="01bd8-154">Field</span></span>|<span data-ttu-id="01bd8-155">Giá trị</span><span class="sxs-lookup"><span data-stu-id="01bd8-155">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="01bd8-156">Tên</span><span class="sxs-lookup"><span data-stu-id="01bd8-156">Name</span></span>|<span data-ttu-id="01bd8-157">Bố cục Bảng điều khiển chính Contoso</span><span class="sxs-lookup"><span data-stu-id="01bd8-157">Contoso Main Panel Layout</span></span>|  
    |<span data-ttu-id="01bd8-158">Loại Thành phần USD</span><span class="sxs-lookup"><span data-stu-id="01bd8-158">USD Component Type</span></span>|<span data-ttu-id="01bd8-159">Bố cục bảng điều khiển</span><span class="sxs-lookup"><span data-stu-id="01bd8-159">Panel Layout</span></span>|  
    |<span data-ttu-id="01bd8-160">Loại bảng điều khiển</span><span class="sxs-lookup"><span data-stu-id="01bd8-160">Panel Type</span></span>|<span data-ttu-id="01bd8-161">Standard Main Panel</span><span class="sxs-lookup"><span data-stu-id="01bd8-161">Standard Main Panel</span></span>|  
    |<span data-ttu-id="01bd8-162">Application is Dynamic</span><span class="sxs-lookup"><span data-stu-id="01bd8-162">Application is Dynamic</span></span>|<span data-ttu-id="01bd8-163">Không</span><span class="sxs-lookup"><span data-stu-id="01bd8-163">No</span></span>|  
    |<span data-ttu-id="01bd8-164">User Can Close</span><span class="sxs-lookup"><span data-stu-id="01bd8-164">User Can Close</span></span>|<span data-ttu-id="01bd8-165">Bỏ chọn</span><span class="sxs-lookup"><span data-stu-id="01bd8-165">Unchecked</span></span>|  
  
    <span data-ttu-id="01bd8-166">![Panel Layout hosted control](../unified-service-desk/media/crm-itpro-usd-wt01-03.png "Panel Layout hosted control")</span><span class="sxs-lookup"><span data-stu-id="01bd8-166">![Panel Layout hosted control](../unified-service-desk/media/crm-itpro-usd-wt01-03.png "Panel Layout hosted control")</span></span>  
  
12. <span data-ttu-id="01bd8-167">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="01bd8-167">Click **Save**.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="01bd8-168">If you don’t create a **Panel Layout** type of hosted control in your agent application, the default panel layout, **Standard Main Panel**, is created automatically when you run the client application.</span><span class="sxs-lookup"><span data-stu-id="01bd8-168">If you don’t create a **Panel Layout** type of hosted control in your agent application, the default panel layout, **Standard Main Panel**, is created automatically when you run the client application.</span></span>  
  
<a name="Step2"></a>   
## <a name="step-2-add-the-hosted-controls-to-a-configuration"></a><span data-ttu-id="01bd8-169">Bước 2: Thêm kiểm soát tổ chức vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="01bd8-169">Step 2: Add the hosted controls to a configuration</span></span>  
 <span data-ttu-id="01bd8-170">Cấu hình trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] giúp bạn lọc các truy cập vào các thành phần được hiển thị trong ứng dụng tổng đài viên cho người dùng.</span><span class="sxs-lookup"><span data-stu-id="01bd8-170">A configuration in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] helps you filter access to components that are displayed in the agent application to a user.</span></span> <span data-ttu-id="01bd8-171">In this step, create a configuration, and then add the hosted controls created earlier to the configuration.</span><span class="sxs-lookup"><span data-stu-id="01bd8-171">In this step, create a configuration, and then add the hosted controls created earlier to the configuration.</span></span>  
  
1. <span data-ttu-id="01bd8-172">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="01bd8-172">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="01bd8-173">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="01bd8-173">Click **Configuration**.</span></span>  
  
4. <span data-ttu-id="01bd8-174">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="01bd8-174">Click **New**.</span></span>  
  
5. <span data-ttu-id="01bd8-175">On the **New Configuration** page, type `Contoso Configuration` as the name of the configuration, and click **Save**.</span><span class="sxs-lookup"><span data-stu-id="01bd8-175">On the **New Configuration** page, type `Contoso Configuration` as the name of the configuration, and click **Save**.</span></span>  
  
6. <span data-ttu-id="01bd8-176">Sau khi cấu hình mới được lưu, trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh tên cấu hình, và sau đó chọn **Kiểm soát tổ chức**.</span><span class="sxs-lookup"><span data-stu-id="01bd8-176">After the new configuration is saved, on the nav bar, click the down arrow next to the configuration name, and then select **Hosted Controls**.</span></span>  
  
7. <span data-ttu-id="01bd8-177">Bấm vào **Thêm kiểm soát tổ chức hiện có**, nhập `Contoso` trong thanh tìm kiếm và sau đó nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="01bd8-177">Click **Add Existing Hosted Control**, type `Contoso` in the search bar, and then press ENTER or click the search icon.</span></span>  
  
8. <span data-ttu-id="01bd8-178">Ba hình thức kiểm soát tổ chức được thêm trước đó hiển thị trong kết quả tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="01bd8-178">The three hosted controls added earlier display in the search results.</span></span> <span data-ttu-id="01bd8-179">Nhấp vào liên kết **Tìm kiếm thêm Hồ sơ**.</span><span class="sxs-lookup"><span data-stu-id="01bd8-179">Click the **Look up more Records** link.</span></span>  
  
9. <span data-ttu-id="01bd8-180">Select the three hosted controls, click **Select**, and then click **Add**.</span><span class="sxs-lookup"><span data-stu-id="01bd8-180">Select the three hosted controls, click **Select**, and then click **Add**.</span></span>  
  
   <span data-ttu-id="01bd8-181">![Add the hosted controls to the configuration](../unified-service-desk/media/crm-itpro-usd-wt01-04.PNG "Add the hosted controls to the configuration")</span><span class="sxs-lookup"><span data-stu-id="01bd8-181">![Add the hosted controls to the configuration](../unified-service-desk/media/crm-itpro-usd-wt01-04.PNG "Add the hosted controls to the configuration")</span></span>  
  
10. <span data-ttu-id="01bd8-182">The hosted controls are added to the configuration.</span><span class="sxs-lookup"><span data-stu-id="01bd8-182">The hosted controls are added to the configuration.</span></span> <span data-ttu-id="01bd8-183">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="01bd8-183">Click **Save**.</span></span>  
  
<a name="Step3"></a>   
## <a name="step-3-assign-users-to-the-configuration"></a><span data-ttu-id="01bd8-184">Bước 3: Chỉ định người dùng cho cấu hình</span><span class="sxs-lookup"><span data-stu-id="01bd8-184">Step 3: Assign users to the configuration</span></span>  
 <span data-ttu-id="01bd8-185">Trong bước này, chỉ định người dùng cho cấu hình do đó khi họ đăng nhập bằng cách sử dụng ứng dụng khách [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], họ chỉ có thể truy cập ba kiểm soát tổ chức đã được thêm vào cấu hình này.</span><span class="sxs-lookup"><span data-stu-id="01bd8-185">In this step, assign users to the configuration so that when they sign in using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, they can only access the three hosted controls that are added to this configuration.</span></span> <span data-ttu-id="01bd8-186">Đối với cách này, chỉ chỉ định một người dùng cho cấu hình người sẽ thử nghiệm các ứng dụng ở phần cuối của cách này.</span><span class="sxs-lookup"><span data-stu-id="01bd8-186">For this walkthrough, assign only a single user to the configuration who will be testing the application at the end of the walkthrough.</span></span>  
  
1. <span data-ttu-id="01bd8-187">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và sau đó chọn **Người dùng được gán**.</span><span class="sxs-lookup"><span data-stu-id="01bd8-187">On the nav bar, click the down arrow next to the **Contoso Configuration**, and then select **Assigned Users**.</span></span>  
  
2. <span data-ttu-id="01bd8-188">Trên trang tiếp theo, bấm vào **Thêm Người dùng hiện có**, nhập tên của người dùng trong thanh tìm kiếm, sau đó nhấn ENTER hoặc nhấp biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="01bd8-188">On the next page, click **Add Existing User**, type the name of the user in the search bar, and then press ENTER or click the search icon.</span></span>  
  
3. <span data-ttu-id="01bd8-189">Từ kết quả tìm kiếm, nhấp vào tên người dùng mà bạn muốn được chỉ định cho cấu hình.</span><span class="sxs-lookup"><span data-stu-id="01bd8-189">From the search result, click the user name that you want to be assigned to the configuration.</span></span> <span data-ttu-id="01bd8-190">Người dùng được thêm vào cấu hình.</span><span class="sxs-lookup"><span data-stu-id="01bd8-190">The user is added to the configuration.</span></span> <span data-ttu-id="01bd8-191">In this case, assign **Randy Blythe** to the configuration.</span><span class="sxs-lookup"><span data-stu-id="01bd8-191">In this case, assign **Randy Blythe** to the configuration.</span></span> <span data-ttu-id="01bd8-192">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="01bd8-192">Click **Save**.</span></span>  
  
   <span data-ttu-id="01bd8-193">![User added to the configuration](../unified-service-desk/media/crm-itpro-usd-wt01-05.png "User added to the configuration")</span><span class="sxs-lookup"><span data-stu-id="01bd8-193">![User added to the configuration](../unified-service-desk/media/crm-itpro-usd-wt01-05.png "User added to the configuration")</span></span>  
  
<a name="Step4"></a>   
## <a name="step-4-test-the-application"></a><span data-ttu-id="01bd8-194">Step 4: Test the application</span><span class="sxs-lookup"><span data-stu-id="01bd8-194">Step 4: Test the application</span></span>  
 <span data-ttu-id="01bd8-195">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in the previous step.</span><span class="sxs-lookup"><span data-stu-id="01bd8-195">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] using the same user credentials that you assigned to the **Contoso Configuration** in the previous step.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="01bd8-196">[Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span><span class="sxs-lookup"><span data-stu-id="01bd8-196">[Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md).</span></span>  
  
 <span data-ttu-id="01bd8-197">Your agent application will look like the following.</span><span class="sxs-lookup"><span data-stu-id="01bd8-197">Your agent application will look like the following.</span></span>  
  
 <span data-ttu-id="01bd8-198">![Basic agent application without any controls](../unified-service-desk/media/crm-itpro-usd-wt01-06.png "Basic agent application without any controls")</span><span class="sxs-lookup"><span data-stu-id="01bd8-198">![Basic agent application without any controls](../unified-service-desk/media/crm-itpro-usd-wt01-06.png "Basic agent application without any controls")</span></span>  
  
 <span data-ttu-id="01bd8-199">The desktop in the agent application is empty because no other controls were added to **Contoso Configuration** apart from the hosted controls required for setting up a basic agent application.</span><span class="sxs-lookup"><span data-stu-id="01bd8-199">The desktop in the agent application is empty because no other controls were added to **Contoso Configuration** apart from the hosted controls required for setting up a basic agent application.</span></span> <span data-ttu-id="01bd8-200">Trong phần còn lại của các cách, bạn sẽ thấy kiểm soát xuất hiện trong ứng dụng tổng đài viên vì bạn dần dần đặt cấu hình và thêm các kiểm soát vào **Cấu hình Contoso**.</span><span class="sxs-lookup"><span data-stu-id="01bd8-200">In the rest of the walkthroughs, you’ll see controls appear in the agent application as you progressively configure and add controls to **Contoso Configuration**.</span></span>  
  
<a name="Conclusion"></a>   
## <a name="conclusion"></a><span data-ttu-id="01bd8-201">Kết luận</span><span class="sxs-lookup"><span data-stu-id="01bd8-201">Conclusion</span></span>  
 <span data-ttu-id="01bd8-202">In this walkthrough, you saw how to quickly build a basic agent application that can connect to an instance of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="01bd8-202">In this walkthrough, you saw how to quickly build a basic agent application that can connect to an instance of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span></span> <span data-ttu-id="01bd8-203">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span><span class="sxs-lookup"><span data-stu-id="01bd8-203">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="01bd8-204">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="01bd8-204">See also</span></span>  
 <span data-ttu-id="01bd8-205">[Walkthrough 2: Display an external webpage in your agent application](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="01bd8-205">[Walkthrough 2: Display an external webpage in your agent application](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md) </span></span>  
 <span data-ttu-id="01bd8-206">[Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="01bd8-206">[Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md) </span></span>  
 <span data-ttu-id="01bd8-207">[Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="01bd8-207">[Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md) </span></span>  
 <span data-ttu-id="01bd8-208">[Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md) </span><span class="sxs-lookup"><span data-stu-id="01bd8-208">[Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md) </span></span>  
 <span data-ttu-id="01bd8-209">[Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="01bd8-209">[Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md) </span></span>  
 <span data-ttu-id="01bd8-210">[Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="01bd8-210">[Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md) </span></span>  
 [<span data-ttu-id="01bd8-211">Unified Service Desk Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="01bd8-211">Unified Service Desk Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)   
 
