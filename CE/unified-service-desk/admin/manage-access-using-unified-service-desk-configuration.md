---
title: Manage access using Unified Service Desk for Dynamics 365 for Customer Engagement apps configuration | MicrosoftDocs
description: Learn to control how agents use Unified Service Desk for Dynamics 365 for Customer Engagement apps by using configuration.
ms.custom:
- dyn365-USD, dyn365-admin
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
ms.assetid: 91772c31-da1f-453b-9934-0179bc50c398
author: kabala123
ms.author: kabala
manager: shujoshi
tags:
- MigrationHO
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 5c7ca5b60aa7f17ca7c2addac4bc0bf4f8a922a8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382446"
---
# <a name="use-unified-service-desk-configuration-to-manage-access"></a><span data-ttu-id="dee42-103">Use Unified Service Desk configuration to manage access</span><span class="sxs-lookup"><span data-stu-id="dee42-103">Use Unified Service Desk configuration to manage access</span></span>
[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="dee42-104">configuration is a great way to filter things that you want your agents to see without having to manage their security roles.</span><span class="sxs-lookup"><span data-stu-id="dee42-104">configuration is a great way to filter things that you want your agents to see without having to manage their security roles.</span></span> <span data-ttu-id="dee42-105">Agents can see only those [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] components in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application that are added in a configuration assigned to them.</span><span class="sxs-lookup"><span data-stu-id="dee42-105">Agents can see only those [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] components in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application that are added in a configuration assigned to them.</span></span>  
  
 <span data-ttu-id="dee42-106">Bạn có thể thêm thành phần [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sau trong một cấu hình:</span><span class="sxs-lookup"><span data-stu-id="dee42-106">You can add the following [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] components in a configuration:</span></span>  
  
-   <span data-ttu-id="dee42-107">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="dee42-107">Action calls</span></span>  
  
-   <span data-ttu-id="dee42-108">Mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="dee42-108">Agent scripts</span></span>  
  
-   <span data-ttu-id="dee42-109">Tìm kiếm Thực thể.</span><span class="sxs-lookup"><span data-stu-id="dee42-109">Entity searches</span></span>  
  
-   <span data-ttu-id="dee42-110">Sự kiện</span><span class="sxs-lookup"><span data-stu-id="dee42-110">Events</span></span>  
  
-   <span data-ttu-id="dee42-111">Biểu mẫu</span><span class="sxs-lookup"><span data-stu-id="dee42-111">Forms</span></span>  
  
-   <span data-ttu-id="dee42-112">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="dee42-112">Hosted controls</span></span>  
  
-   <span data-ttu-id="dee42-113">Tùy chọn</span><span class="sxs-lookup"><span data-stu-id="dee42-113">Options</span></span>  
  
-   <span data-ttu-id="dee42-114">Scriptlet</span><span class="sxs-lookup"><span data-stu-id="dee42-114">Scriptlets</span></span>  
  
-   <span data-ttu-id="dee42-115">Thông tin Phiên</span><span class="sxs-lookup"><span data-stu-id="dee42-115">Session information</span></span>  
  
-   <span data-ttu-id="dee42-116">Thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="dee42-116">Toolbar</span></span>  
  
-   <span data-ttu-id="dee42-117">Nguyên tắc điều hướng cửa sổ</span><span class="sxs-lookup"><span data-stu-id="dee42-117">Window navigation rule</span></span>  
  
<a name="Create"></a>   
## <a name="create-a-unified-service-desk-configuration"></a><span data-ttu-id="dee42-118">Tạo cấu hình ứng dụng Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="dee42-118">Create a Unified Service Desk configuration</span></span>  
  
1. <span data-ttu-id="dee42-119">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="dee42-119">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="dee42-120">On the nav bar, click **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.</span><span class="sxs-lookup"><span data-stu-id="dee42-120">On the nav bar, click **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.</span></span>  
  
3. <span data-ttu-id="dee42-121">Click **Settings** > **Unified Service Desk** > **Configuration**.</span><span class="sxs-lookup"><span data-stu-id="dee42-121">Click **Settings** > **Unified Service Desk** > **Configuration**.</span></span>  
  
4. <span data-ttu-id="dee42-122">Trên trang cấu hình, bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="dee42-122">On the configuration page, click **New**.</span></span>  
  
5. <span data-ttu-id="dee42-123">On the **New Configuration** page, type the name of the configuration, and then click **Save**.</span><span class="sxs-lookup"><span data-stu-id="dee42-123">On the **New Configuration** page, type the name of the configuration, and then click **Save**.</span></span>  
  
6. <span data-ttu-id="dee42-124">Sau khi cấu hình mới được lưu, trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh tên cấu hình, và sau đó chọn Kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="dee42-124">After the new configuration is saved, on the nav bar, click the down arrow next to the configuration name.</span></span> <span data-ttu-id="dee42-125">This shows the components that can be added to a configuration.</span><span class="sxs-lookup"><span data-stu-id="dee42-125">This shows the components that can be added to a configuration.</span></span>  
  
   <span data-ttu-id="dee42-126">![Menu with components added to configuration](../../unified-service-desk/media/usd-configuration-1.PNG "Menu with components added to configuration")</span><span class="sxs-lookup"><span data-stu-id="dee42-126">![Menu with components added to configuration](../../unified-service-desk/media/usd-configuration-1.PNG "Menu with components added to configuration")</span></span>  
  
7. <span data-ttu-id="dee42-127">Bấm vào thành phần để thêm.</span><span class="sxs-lookup"><span data-stu-id="dee42-127">Click a component to add it.</span></span> <span data-ttu-id="dee42-128">Trang tìm kiếm Thực thể cho thành phần tương ứng sẽ xuất hiện.</span><span class="sxs-lookup"><span data-stu-id="dee42-128">The entity search page for the corresponding component appears.</span></span> <span data-ttu-id="dee42-129">Click **Add Existing > \<Component Name>** to search for the existing records.</span><span class="sxs-lookup"><span data-stu-id="dee42-129">Click **Add Existing > \<Component Name>** to search for the existing records.</span></span> <span data-ttu-id="dee42-130">Ví dụ, nếu bạn chọn **cuộc gọi hành động**, bấm vào **thêm cuộc gọi hành động hiện có** trên trang tìm kiếm thực thể.</span><span class="sxs-lookup"><span data-stu-id="dee42-130">For example, if you selected **Action Calls**, click **Add Existing Action Call** on the entity search page.</span></span>  
  
8. <span data-ttu-id="dee42-131">Gõ tên của các thành phần trong hộp tìm kiếm, và sau đó nhấn ENTER hoặc nhấp vào nút tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="dee42-131">Type the name of the component in the search box, and then press ENTER or click the search button.</span></span> <span data-ttu-id="dee42-132">If a record doesn’t exist, click **New** in the search results box to create an instance of the component you want to add.</span><span class="sxs-lookup"><span data-stu-id="dee42-132">If a record doesn’t exist, click **New** in the search results box to create an instance of the component you want to add.</span></span>  
  
   <span data-ttu-id="dee42-133">![Add existing component record](../../unified-service-desk/media/usd-configuration-2.PNG "Add existing component record")</span><span class="sxs-lookup"><span data-stu-id="dee42-133">![Add existing component record](../../unified-service-desk/media/usd-configuration-2.PNG "Add existing component record")</span></span>  
  
9. <span data-ttu-id="dee42-134">Repeat this with other components you want to add to the configuration.</span><span class="sxs-lookup"><span data-stu-id="dee42-134">Repeat this with other components you want to add to the configuration.</span></span>  
  
10. <span data-ttu-id="dee42-135">After you have added the components, click the **Save** button ![Auto save button](../../unified-service-desk/media/cust-auto-save-icon.png "Auto save button") to save the configuration.</span><span class="sxs-lookup"><span data-stu-id="dee42-135">After you have added the components, click the **Save** button ![Auto save button](../../unified-service-desk/media/cust-auto-save-icon.png "Auto save button") to save the configuration.</span></span>  
  
    > [!IMPORTANT]
    >  <span data-ttu-id="dee42-136">If no hosted controls are added to a configuration, or if certain hosted controls are not added, such as the Panel Layout, Global Manager, and Connection Manager hosted controls, assigned users may see a blank [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application window.</span><span class="sxs-lookup"><span data-stu-id="dee42-136">If no hosted controls are added to a configuration, or if certain hosted controls are not added, such as the Panel Layout, Global Manager, and Connection Manager hosted controls, assigned users may see a blank [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application window.</span></span> <span data-ttu-id="dee42-137">For more information about how to create a sample configuration, see [Walkthrough 1: Build a simple agent application](../../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="dee42-137">For more information about how to create a sample configuration, see [Walkthrough 1: Build a simple agent application](../../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span>  
  
<a name="default"></a>   
## <a name="set-a-configuration-as-the-default"></a><span data-ttu-id="dee42-138">Set a configuration as the default</span><span class="sxs-lookup"><span data-stu-id="dee42-138">Set a configuration as the default</span></span>  
 <span data-ttu-id="dee42-139">You can set a Configuration as the default configuration by using the Is Default attribute of the Configuration record.</span><span class="sxs-lookup"><span data-stu-id="dee42-139">You can set a Configuration as the default configuration by using the Is Default attribute of the Configuration record.</span></span> <span data-ttu-id="dee42-140">Then, any user not assigned to a Configuration will have only the Unified Service Desk components associated with the default configuration cached when they sign in to the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.</span><span class="sxs-lookup"><span data-stu-id="dee42-140">Then, any user not assigned to a Configuration will have only the Unified Service Desk components associated with the default configuration cached when they sign in to the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.</span></span>  
  
### <a name="set-a-configuration-as-the-default"></a><span data-ttu-id="dee42-141">Set a configuration as the default</span><span class="sxs-lookup"><span data-stu-id="dee42-141">Set a configuration as the default</span></span>  
  
1. <span data-ttu-id="dee42-142">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="dee42-142">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="dee42-143">On the nav bar, click **Main** > **Settings** > **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="dee42-143">On the nav bar, click **Main** > **Settings** > **Unified Service Desk**.</span></span>  
  
3. <span data-ttu-id="dee42-144">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="dee42-144">Click **Configuration**.</span></span>  
  
4. <span data-ttu-id="dee42-145">In the Active Configuration list, select for the configuration record you want to make the default.</span><span class="sxs-lookup"><span data-stu-id="dee42-145">In the Active Configuration list, select for the configuration record you want to make the default.</span></span>  
  
5. <span data-ttu-id="dee42-146">Choose **Set As Default** from the actions menu.</span><span class="sxs-lookup"><span data-stu-id="dee42-146">Choose **Set As Default** from the actions menu.</span></span>  
  
<a name="auditanddiag"></a>   
## <a name="associate-auditing-and-diagnostics-with-a-configuration"></a><span data-ttu-id="dee42-147">Associate auditing and diagnostics with a configuration</span><span class="sxs-lookup"><span data-stu-id="dee42-147">Associate auditing and diagnostics with a configuration</span></span>  
 <span data-ttu-id="dee42-148">When you associate an Audit & Diagnostics record with a configuration, only the auditing and diagnostics events specified in the Audit & Diagnostics record are logged, and only for users who are assigned to the configuration.</span><span class="sxs-lookup"><span data-stu-id="dee42-148">When you associate an Audit & Diagnostics record with a configuration, only the auditing and diagnostics events specified in the Audit & Diagnostics record are logged, and only for users who are assigned to the configuration.</span></span> <span data-ttu-id="dee42-149">The following procedure describes how to associate an existing Audit & Diagnostics record with a configuration.</span><span class="sxs-lookup"><span data-stu-id="dee42-149">The following procedure describes how to associate an existing Audit & Diagnostics record with a configuration.</span></span> <span data-ttu-id="dee42-150">For information about how to create an Audit & Diagnostics record, see [Configure auditing and diagnostics in Unified Service Desk](../../unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk.md).</span><span class="sxs-lookup"><span data-stu-id="dee42-150">For information about how to create an Audit & Diagnostics record, see [Configure auditing and diagnostics in Unified Service Desk](../../unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk.md).</span></span>  
  
1. <span data-ttu-id="dee42-151">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="dee42-151">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="dee42-152">On the nav bar, click **Main** > **Settings** > **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="dee42-152">On the nav bar, click **Main** > **Settings** > **Unified Service Desk**.</span></span>  
  
3. <span data-ttu-id="dee42-153">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="dee42-153">Click **Configuration**.</span></span>  
  
4. <span data-ttu-id="dee42-154">In the configuration list, select the configuration record you want to add an Audit & Diagnostic record for.</span><span class="sxs-lookup"><span data-stu-id="dee42-154">In the configuration list, select the configuration record you want to add an Audit & Diagnostic record for.</span></span>  
  
5. <span data-ttu-id="dee42-155">Next to **Audit & Diagnostic Settings**, type the name of the Audit & Diagnostic record in the search box, and then press ENTER or click the search button.</span><span class="sxs-lookup"><span data-stu-id="dee42-155">Next to **Audit & Diagnostic Settings**, type the name of the Audit & Diagnostic record in the search box, and then press ENTER or click the search button.</span></span>  
  
6. <span data-ttu-id="dee42-156">After you add the Audit & Diagnostics record, click the **Save** button ![Auto save button](../../unified-service-desk/media/cust-auto-save-icon.png "Auto save button") to save the configuration.</span><span class="sxs-lookup"><span data-stu-id="dee42-156">After you add the Audit & Diagnostics record, click the **Save** button ![Auto save button](../../unified-service-desk/media/cust-auto-save-icon.png "Auto save button") to save the configuration.</span></span>  
  
<a name="Assign"></a>   
## <a name="assign-users-to-a-unified-service-desk-configuration"></a><span data-ttu-id="dee42-157">Gán người dùng cho cấu hình ứng dụng Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="dee42-157">Assign users to a Unified Service Desk configuration</span></span>  
 <span data-ttu-id="dee42-158">After you create a [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration, you can assign users to it.</span><span class="sxs-lookup"><span data-stu-id="dee42-158">After you create a [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration, you can assign users to it.</span></span> <span data-ttu-id="dee42-159">Người dùng được gán cho cấu hình chỉ truy cập các thành phần trong ứng dụng khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] được thêm vào trong một cấu hình.</span><span class="sxs-lookup"><span data-stu-id="dee42-159">The users assigned to a configuration can only access components in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application that are added to the configuration.</span></span>  
  
1. <span data-ttu-id="dee42-160">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="dee42-160">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="dee42-161">On the nav bar, click **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.</span><span class="sxs-lookup"><span data-stu-id="dee42-161">On the nav bar, click **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.</span></span>  
  
3. <span data-ttu-id="dee42-162">Click **Settings** > **Unified Service Desk** > **Configuration**.</span><span class="sxs-lookup"><span data-stu-id="dee42-162">Click **Settings** > **Unified Service Desk** > **Configuration**.</span></span>  
  
4. <span data-ttu-id="dee42-163">Trong trang cấu hình, tìm kiếm đối với hồ sơ yêu cầu cấu hình.</span><span class="sxs-lookup"><span data-stu-id="dee42-163">On the configuration page, search for the required configuration record.</span></span>  
  
5. <span data-ttu-id="dee42-164">Để mở một định nghĩa cấu hình, hoặc nhấp vào tên cấu hình, hoặc chọn hồ sơ, và sau đó nhấp vào **chỉnh sửa**.</span><span class="sxs-lookup"><span data-stu-id="dee42-164">To open a configuration definition, either click the configuration name, or select the record, and then click **Edit**.</span></span> <span data-ttu-id="dee42-165">Điều này sẽ mở ra định nghĩa cấu hình.</span><span class="sxs-lookup"><span data-stu-id="dee42-165">This opens the configuration definition.</span></span>  
  
6. <span data-ttu-id="dee42-166">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh tên cấu hình và sau đó bấm vào **Người dùng được gán**.</span><span class="sxs-lookup"><span data-stu-id="dee42-166">On the nav bar, click the down arrow next to the configuration name, and then click **Assigned Users**.</span></span>  
  
   <span data-ttu-id="dee42-167">![Navigation to assign users to a configuration](../../unified-service-desk/media/usd-configuration-3.PNG "Navigation to assign users to a configuration")</span><span class="sxs-lookup"><span data-stu-id="dee42-167">![Navigation to assign users to a configuration](../../unified-service-desk/media/usd-configuration-3.PNG "Navigation to assign users to a configuration")</span></span>  
  
7. <span data-ttu-id="dee42-168">Trên trang tiếp theo, bạn có thể hoặc chỉ định cấu hình cho người dùng hiện tại, hoặc tạo một người dùng mới và chỉ định cấu hình cho nó.</span><span class="sxs-lookup"><span data-stu-id="dee42-168">On the next page, you can either assign the configuration to an existing user, or create a new user and assign the configuration to it.</span></span>  
  
8. <span data-ttu-id="dee42-169">Gõ tên của người dùng được yêu cầu trong hộp tìm kiếm, và sau đó nhấn ENTER hoặc nhấp vào nút tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="dee42-169">Type the name of the required user in the search box, and then press ENTER or click the search button.</span></span>  
  
9. <span data-ttu-id="dee42-170">Nhấp vào tên của người sử dụng cần thiết để thêm chúng vào cấu hình.</span><span class="sxs-lookup"><span data-stu-id="dee42-170">Click the names of the required users to add them to the configuration.</span></span> <span data-ttu-id="dee42-171">Click the **Save** button ![Auto save button](../../unified-service-desk/media/cust-auto-save-icon.png "Auto save button") to save your changes.</span><span class="sxs-lookup"><span data-stu-id="dee42-171">Click the **Save** button ![Auto save button](../../unified-service-desk/media/cust-auto-save-icon.png "Auto save button") to save your changes.</span></span>  
  
     <span data-ttu-id="dee42-172">Nếu bạn nhấp vào tên người dùng theo cột **tên**, Hồ sơ người sử dụng sẽ mở ra, và bạn có thể thấy rằng các [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] cấu hình được gán cho người dùng trong trường **USD cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="dee42-172">If you click the user name under the **Name** column, the user record opens, and you can see that the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration is assigned to the user in the **USD Configuration** field.</span></span>  
  
   <span data-ttu-id="dee42-173">![USD configuration assigned to a user](../../unified-service-desk/media/usd-configuration-4.PNG "USD configuration assigned to a user")</span><span class="sxs-lookup"><span data-stu-id="dee42-173">![USD configuration assigned to a user](../../unified-service-desk/media/usd-configuration-4.PNG "USD configuration assigned to a user")</span></span>  
  
   <span data-ttu-id="dee42-174">A user can only be assigned to one Configuration.</span><span class="sxs-lookup"><span data-stu-id="dee42-174">A user can only be assigned to one Configuration.</span></span> <span data-ttu-id="dee42-175">To assign a user to a different Configuration, you must first remove the existing Configuration.</span><span class="sxs-lookup"><span data-stu-id="dee42-175">To assign a user to a different Configuration, you must first remove the existing Configuration.</span></span>  
  
### <a name="remove-a-user-from-a-configuration"></a><span data-ttu-id="dee42-176">Remove a user from a Configuration</span><span class="sxs-lookup"><span data-stu-id="dee42-176">Remove a user from a Configuration</span></span>  
  
1.  <span data-ttu-id="dee42-177">Open the User form for the agent who you want to remove from a Configuration.</span><span class="sxs-lookup"><span data-stu-id="dee42-177">Open the User form for the agent who you want to remove from a Configuration.</span></span> <span data-ttu-id="dee42-178">One way you can do this is through **Settings** > **Security** > **Users**.</span><span class="sxs-lookup"><span data-stu-id="dee42-178">One way you can do this is through **Settings** > **Security** > **Users**.</span></span>  
  
2.  <span data-ttu-id="dee42-179">On the user form, click the **USD Configuration**.</span><span class="sxs-lookup"><span data-stu-id="dee42-179">On the user form, click the **USD Configuration**.</span></span>  
  
3.  <span data-ttu-id="dee42-180">Press the Delete key to remove the Configuration, and then save the form.</span><span class="sxs-lookup"><span data-stu-id="dee42-180">Press the Delete key to remove the Configuration, and then save the form.</span></span>  
  
<a name="clone"></a>   
## <a name="clone-a-configuration"></a><span data-ttu-id="dee42-181">Clone a Configuration</span><span class="sxs-lookup"><span data-stu-id="dee42-181">Clone a Configuration</span></span>  
 <span data-ttu-id="dee42-182">You can copy a Configuration by cloning it.</span><span class="sxs-lookup"><span data-stu-id="dee42-182">You can copy a Configuration by cloning it.</span></span> <span data-ttu-id="dee42-183">This lets you quickly copy an existing configuration and corresponding relationships to use for a different Configuration.</span><span class="sxs-lookup"><span data-stu-id="dee42-183">This lets you quickly copy an existing configuration and corresponding relationships to use for a different Configuration.</span></span> <span data-ttu-id="dee42-184">Because a user can only belong to a single configuration, any users associated with configuration will not be associated with the cloned configuration.</span><span class="sxs-lookup"><span data-stu-id="dee42-184">Because a user can only belong to a single configuration, any users associated with configuration will not be associated with the cloned configuration.</span></span>  
  
### <a name="clone-a-configuration"></a><span data-ttu-id="dee42-185">Clone a configuration</span><span class="sxs-lookup"><span data-stu-id="dee42-185">Clone a configuration</span></span>  
  
1. <span data-ttu-id="dee42-186">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="dee42-186">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="dee42-187">On the nav bar, click **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.</span><span class="sxs-lookup"><span data-stu-id="dee42-187">On the nav bar, click **Microsoft Dynamics 365 for Customer Engagement apps**, and then select **Settings**.</span></span>  
  
3. <span data-ttu-id="dee42-188">Click **Settings** > **Unified Service Desk** > **Configuration**.</span><span class="sxs-lookup"><span data-stu-id="dee42-188">Click **Settings** > **Unified Service Desk** > **Configuration**.</span></span>  
  
4. <span data-ttu-id="dee42-189">In the configuration list, select for the configuration record you want to clone.</span><span class="sxs-lookup"><span data-stu-id="dee42-189">In the configuration list, select for the configuration record you want to clone.</span></span>  
  
5. <span data-ttu-id="dee42-190">Choose **Clone** on the actions menu, and when prompted, click **Clone**.</span><span class="sxs-lookup"><span data-stu-id="dee42-190">Choose **Clone** on the actions menu, and when prompted, click **Clone**.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dee42-191">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="dee42-191">See also</span></span>  
 <span data-ttu-id="dee42-192">[Manage access using custom security roles](../../unified-service-desk/admin/manage-access-using-unified-service-desk-security-roles.md) </span><span class="sxs-lookup"><span data-stu-id="dee42-192">[Manage access using custom security roles](../../unified-service-desk/admin/manage-access-using-unified-service-desk-security-roles.md) </span></span>  
 <span data-ttu-id="dee42-193">[Access management in Unified Service Desk](../../unified-service-desk/admin/security-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="dee42-193">[Access management in Unified Service Desk](../../unified-service-desk/admin/security-unified-service-desk.md) </span></span>  
 [<span data-ttu-id="dee42-194">Unified Service Desk Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="dee42-194">Unified Service Desk Configuration Walkthroughs</span></span>](../../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
