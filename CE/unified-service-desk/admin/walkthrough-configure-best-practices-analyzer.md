---
title: 'Walkthrough: Configure Best Practices Analyzer in Unified Service Desk (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: Learn about downloading and installing the Best Practices Analyzer.
ms.custom: ''
ms.date: 05/15/2018
ms.service: usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: C1F329C3-2E00-40A5-8BA3-1B6BC16444EA
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: d049d824bdf545b659d79999f4d081d586835658
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382469"
---
# <a name="walkthrough-configure-includepn-best-practices-analyzerincludespn-best-practices-analyzermd-in-includepnunifiedservicedeskincludespn-unified-service-deskmd"></a><span data-ttu-id="2b5f7-103">Walkthrough: Configure [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]</span><span class="sxs-lookup"><span data-stu-id="2b5f7-103">Walkthrough: Configure [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]</span></span>

<span data-ttu-id="2b5f7-104">This walkthrough demonstrates how to configure and setup [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] in your agent application.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-104">This walkthrough demonstrates how to configure and setup [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] in your agent application.</span></span>

<span data-ttu-id="2b5f7-105">![Generate Best Practices Analyzer report](../media/bpa-report-generation-new.gif "Generate Best Practices Analyzer report")</span><span class="sxs-lookup"><span data-stu-id="2b5f7-105">![Generate Best Practices Analyzer report](../media/bpa-report-generation-new.gif "Generate Best Practices Analyzer report")</span></span>

<a name="Step1"></a>   
## <a name="step-1-create-a-includepn-best-practices-analyzerincludespn-best-practices-analyzermd-and-toolbar-container-hosted-control"></a><span data-ttu-id="2b5f7-106">Step 1: Create a [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] and toolbar container hosted control</span><span class="sxs-lookup"><span data-stu-id="2b5f7-106">Step 1: Create a [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] and toolbar container hosted control</span></span>

<span data-ttu-id="2b5f7-107">In this step, you will create a [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] and toolbar container hosted control.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-107">In this step, you will create a [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] and toolbar container hosted control.</span></span>

1. <span data-ttu-id="2b5f7-108">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-108">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]

3. <span data-ttu-id="2b5f7-109">Bấm **Kiểm soát Tổ chức**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-109">Click **Hosted Controls**.</span></span>  

4. <span data-ttu-id="2b5f7-110">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-110">Click **New**.</span></span>  

5. <span data-ttu-id="2b5f7-111">Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="2b5f7-111">On the **New Hosted Control** page, specify the following values:</span></span>  


   |         <span data-ttu-id="2b5f7-112">Trường</span><span class="sxs-lookup"><span data-stu-id="2b5f7-112">Field</span></span>          |                                         <span data-ttu-id="2b5f7-113">Value</span><span class="sxs-lookup"><span data-stu-id="2b5f7-113">Value</span></span>                                         |
   |------------------------|---------------------------------------------------------------------------------------|
   |          <span data-ttu-id="2b5f7-114">Tên</span><span class="sxs-lookup"><span data-stu-id="2b5f7-114">Name</span></span>          | [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]  |
   |      <span data-ttu-id="2b5f7-115">Tên Hiển thị</span><span class="sxs-lookup"><span data-stu-id="2b5f7-115">Display Name</span></span>      | [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]  |
   |   <span data-ttu-id="2b5f7-116">Loại thành phần USD</span><span class="sxs-lookup"><span data-stu-id="2b5f7-116">USD Component Type</span></span>   |                                  <span data-ttu-id="2b5f7-117">USD Hosted Control</span><span class="sxs-lookup"><span data-stu-id="2b5f7-117">USD Hosted Control</span></span>                                   |
   | <span data-ttu-id="2b5f7-118">Ứng dụng toàn cầu</span><span class="sxs-lookup"><span data-stu-id="2b5f7-118">Application is Global</span></span>  |                                        <span data-ttu-id="2b5f7-119">Đã kiểm tra</span><span class="sxs-lookup"><span data-stu-id="2b5f7-119">Checked</span></span>                                        |
   |     <span data-ttu-id="2b5f7-120">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="2b5f7-120">Display Group</span></span>      |                                       <span data-ttu-id="2b5f7-121">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="2b5f7-121">MainPanel</span></span>                                       |
   | <span data-ttu-id="2b5f7-122">Ứng dụng động</span><span class="sxs-lookup"><span data-stu-id="2b5f7-122">Application is Dynamic</span></span> |                                        <span data-ttu-id="2b5f7-123">Đã kiểm tra</span><span class="sxs-lookup"><span data-stu-id="2b5f7-123">Checked</span></span>                                        |
   |     <span data-ttu-id="2b5f7-124">Người dùng có thể đóng</span><span class="sxs-lookup"><span data-stu-id="2b5f7-124">User Can Close</span></span>     |                                        <span data-ttu-id="2b5f7-125">Đã kiểm tra</span><span class="sxs-lookup"><span data-stu-id="2b5f7-125">Checked</span></span>                                        |
   |      <span data-ttu-id="2b5f7-126">URI cụm tổ hợp</span><span class="sxs-lookup"><span data-stu-id="2b5f7-126">Assembly URI</span></span>      |               `Microsoft.Crm.UnifiedServiceDesk.BestPracticesAnalyser`                |
   |     <span data-ttu-id="2b5f7-127">Loại cụm tổ hợp</span><span class="sxs-lookup"><span data-stu-id="2b5f7-127">Assembly Type</span></span>      | `Microsoft.Crm.UnifiedServiceDesk.BestPracticesAnalyser.BestPracticesAnalyserControl` |

    <span data-ttu-id="2b5f7-128">![Create Best Practices Analyzer hosted control](../media/usd-create-bpa-hosted-control.PNG "Create Best Practices Analyzer hosted control")</span><span class="sxs-lookup"><span data-stu-id="2b5f7-128">![Create Best Practices Analyzer hosted control](../media/usd-create-bpa-hosted-control.PNG "Create Best Practices Analyzer hosted control")</span></span>

6. <span data-ttu-id="2b5f7-129">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-129">Click **Save**.</span></span>

7. <span data-ttu-id="2b5f7-130">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-130">Click **New**.</span></span>  

8. <span data-ttu-id="2b5f7-131">Trên trang **Kiểm soát tổ chức mới**, chỉ định các giá trị sau</span><span class="sxs-lookup"><span data-stu-id="2b5f7-131">On the **New Hosted Control** page, specify the following values</span></span>  

   |<span data-ttu-id="2b5f7-132">Trường</span><span class="sxs-lookup"><span data-stu-id="2b5f7-132">Field</span></span>|<span data-ttu-id="2b5f7-133">Value</span><span class="sxs-lookup"><span data-stu-id="2b5f7-133">Value</span></span>|  
   |-----------|-----------|
   |<span data-ttu-id="2b5f7-134">Tên</span><span class="sxs-lookup"><span data-stu-id="2b5f7-134">Name</span></span>|<span data-ttu-id="2b5f7-135">About Toolbar Container</span><span class="sxs-lookup"><span data-stu-id="2b5f7-135">About Toolbar Container</span></span>|
   |<span data-ttu-id="2b5f7-136">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="2b5f7-136">USD Component Type</span></span>|<span data-ttu-id="2b5f7-137">Bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="2b5f7-137">Toolbar Container</span></span>|
   |<span data-ttu-id="2b5f7-138">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="2b5f7-138">Display Group</span></span>|<span data-ttu-id="2b5f7-139">AboutPanel</span><span class="sxs-lookup"><span data-stu-id="2b5f7-139">AboutPanel</span></span>|

    <span data-ttu-id="2b5f7-140">![Create Toolbar Container hosted control](../media/usd-create-about-toolbar-container-hosted-control.PNG "Create Toolbar Container hosted control")</span><span class="sxs-lookup"><span data-stu-id="2b5f7-140">![Create Toolbar Container hosted control](../media/usd-create-about-toolbar-container-hosted-control.PNG "Create Toolbar Container hosted control")</span></span>

9. <span data-ttu-id="2b5f7-141">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-141">Click **Save**.</span></span>

<a name="Step2"></a>   
## <a name="step-2-add-a-toolbar-and-attach-it-to-the-toolbar-container"></a><span data-ttu-id="2b5f7-142">Bước 2: Thêm thanh công cụ và gắn nó vào bộ chứa thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="2b5f7-142">Step 2: Add a toolbar and attach it to the toolbar container</span></span>

 <span data-ttu-id="2b5f7-143">In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 1.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-143">In this step, you’ll create a toolbar, and attach the toolbar to the toolbar container hosted control created in step 1.</span></span>

1. <span data-ttu-id="2b5f7-144">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-144">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]

3. <span data-ttu-id="2b5f7-145">Bấm vào **Thanh công cụ**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-145">Click **Toolbars**.</span></span>  

4. <span data-ttu-id="2b5f7-146">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-146">Click **New**.</span></span>

5. <span data-ttu-id="2b5f7-147">On the **New Toolbar** page, type **About Toolbar** in the **Name** box, and then click **Save**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-147">On the **New Toolbar** page, type **About Toolbar** in the **Name** box, and then click **Save**.</span></span>  

6. <span data-ttu-id="2b5f7-148">Attach the toolbar to the toolbar container hosted control created in step 1.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-148">Attach the toolbar to the toolbar container hosted control created in step 1.</span></span> <span data-ttu-id="2b5f7-149">On the nav bar, click the down arrow next to **About Toolbar**, and click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-149">On the nav bar, click the down arrow next to **About Toolbar**, and click **Hosted Controls**.</span></span>  

7. <span data-ttu-id="2b5f7-150">On the next page, click **Add Existing Hosted Control**, type `About Toolbar Container` in the search bar, and then press **ENTER** or click the search icon.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-150">On the next page, click **Add Existing Hosted Control**, type `About Toolbar Container` in the search bar, and then press **ENTER** or click the search icon.</span></span>

8. <span data-ttu-id="2b5f7-151">From the search result, click **About Toolbar Container** to add.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-151">From the search result, click **About Toolbar Container** to add.</span></span>

     <span data-ttu-id="2b5f7-152">![Create toolbar and attach it to Toolbar Container hosted control](../media/usd-create-toolbar-attach-toolbar-container-hosted-control.PNG "Create toolbar and attach it to Toolbar Container hosted control")</span><span class="sxs-lookup"><span data-stu-id="2b5f7-152">![Create toolbar and attach it to Toolbar Container hosted control](../media/usd-create-toolbar-attach-toolbar-container-hosted-control.PNG "Create toolbar and attach it to Toolbar Container hosted control")</span></span>

9. <span data-ttu-id="2b5f7-153">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-153">Click **Save**.</span></span>

<a name="Step3"></a>   
## <a name="step-3-add-toolbar-button"></a><span data-ttu-id="2b5f7-154">Step 3: Add toolbar button</span><span class="sxs-lookup"><span data-stu-id="2b5f7-154">Step 3: Add toolbar button</span></span>

 <span data-ttu-id="2b5f7-155">In this step, you’ll create two buttons - **Settings** and **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**, and **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** button under **Settings** button.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-155">In this step, you’ll create two buttons - **Settings** and **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**, and **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** button under **Settings** button.</span></span>

1. <span data-ttu-id="2b5f7-156">Sau khi bạn lưu thanh công cụ trong bước 2, vùng **nút** sẽ có sẵn.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-156">After you save the toolbar in step 2, the **Buttons** area becomes available.</span></span> <span data-ttu-id="2b5f7-157">In the **Buttons** area, click **+** on the right corner to add a button.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-157">In the **Buttons** area, click **+** on the right corner to add a button.</span></span>  

2. <span data-ttu-id="2b5f7-158">Trên trang **Nút thanh công cụ mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="2b5f7-158">On the **New Toolbar Button** page, specify the following values:</span></span>  

    |<span data-ttu-id="2b5f7-159">Trường</span><span class="sxs-lookup"><span data-stu-id="2b5f7-159">Field</span></span>|<span data-ttu-id="2b5f7-160">Value</span><span class="sxs-lookup"><span data-stu-id="2b5f7-160">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="2b5f7-161">Tên</span><span class="sxs-lookup"><span data-stu-id="2b5f7-161">Name</span></span>|<span data-ttu-id="2b5f7-162">Thiết đặt</span><span class="sxs-lookup"><span data-stu-id="2b5f7-162">Settings</span></span>|
    |<span data-ttu-id="2b5f7-163">Hình ảnh</span><span class="sxs-lookup"><span data-stu-id="2b5f7-163">Image</span></span>|<span data-ttu-id="2b5f7-164">msdyusd_settings_16</span><span class="sxs-lookup"><span data-stu-id="2b5f7-164">msdyusd_settings_16</span></span>|
    |<span data-ttu-id="2b5f7-165">Chú giải công cụ</span><span class="sxs-lookup"><span data-stu-id="2b5f7-165">Tooltip</span></span>|<span data-ttu-id="2b5f7-166">Thiết đặt</span><span class="sxs-lookup"><span data-stu-id="2b5f7-166">Settings</span></span>|  
    |<span data-ttu-id="2b5f7-167">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="2b5f7-167">Order</span></span>|<span data-ttu-id="2b5f7-168">100</span><span class="sxs-lookup"><span data-stu-id="2b5f7-168">100</span></span>|

     <span data-ttu-id="2b5f7-169">![Create Settings toolbar button](../media/usd-create-settings-toolbar-button.PNG "Create Settings toolbar button")</span><span class="sxs-lookup"><span data-stu-id="2b5f7-169">![Create Settings toolbar button](../media/usd-create-settings-toolbar-button.PNG "Create Settings toolbar button")</span></span>

3. <span data-ttu-id="2b5f7-170">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-170">Click **Save**.</span></span>

4. <span data-ttu-id="2b5f7-171">After you save the **Settings** toolbar button, Click **New** to create another button called **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-171">After you save the **Settings** toolbar button, Click **New** to create another button called **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**.</span></span>

5. <span data-ttu-id="2b5f7-172">On the **New Toolbar Button** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="2b5f7-172">On the **New Toolbar Button** page, specify the following values:</span></span>  


   |    <span data-ttu-id="2b5f7-173">Trường</span><span class="sxs-lookup"><span data-stu-id="2b5f7-173">Field</span></span>    |                                        <span data-ttu-id="2b5f7-174">Value</span><span class="sxs-lookup"><span data-stu-id="2b5f7-174">Value</span></span>                                         |
   |-------------|--------------------------------------------------------------------------------------|
   |    <span data-ttu-id="2b5f7-175">Tên</span><span class="sxs-lookup"><span data-stu-id="2b5f7-175">Name</span></span>     | [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] |
   | <span data-ttu-id="2b5f7-176">Văn bản nút</span><span class="sxs-lookup"><span data-stu-id="2b5f7-176">Button Text</span></span> |                         <span data-ttu-id="2b5f7-177">[[$Resources.BestPracticesAnalyzer]]</span><span class="sxs-lookup"><span data-stu-id="2b5f7-177">[[$Resources.BestPracticesAnalyzer]]</span></span>                         |
   |   <span data-ttu-id="2b5f7-178">Chú giải công cụ</span><span class="sxs-lookup"><span data-stu-id="2b5f7-178">Tooltip</span></span>   | [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] |
   |    <span data-ttu-id="2b5f7-179">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="2b5f7-179">Order</span></span>    |                                          <span data-ttu-id="2b5f7-180">4</span><span class="sxs-lookup"><span data-stu-id="2b5f7-180">4</span></span>                                           |

    <span data-ttu-id="2b5f7-181">![Create Best Practices Analyzer toolbar button](../media/usd-create-best-practices-analyzer-button.PNG "Create Best Practices Analyzer toolbar button")</span><span class="sxs-lookup"><span data-stu-id="2b5f7-181">![Create Best Practices Analyzer toolbar button](../media/usd-create-best-practices-analyzer-button.PNG "Create Best Practices Analyzer toolbar button")</span></span>

6. <span data-ttu-id="2b5f7-182">Attach the  **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** button under **Settings** button.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-182">Attach the  **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** button under **Settings** button.</span></span> <span data-ttu-id="2b5f7-183">On the nav bar, click the down arrow next to **Settings**, and click **Toolbar Buttons**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-183">On the nav bar, click the down arrow next to **Settings**, and click **Toolbar Buttons**.</span></span>  

7. <span data-ttu-id="2b5f7-184">On the next page, click **Add Existing Toolbar Button**, type `Best Practices Analyzer` in the search bar, and then press **ENTER** or click the search icon.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-184">On the next page, click **Add Existing Toolbar Button**, type `Best Practices Analyzer` in the search bar, and then press **ENTER** or click the search icon.</span></span>

<span data-ttu-id="2b5f7-185">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-185">Click **Save**.</span></span>

<a name="Step4"></a>   
## <a name="step-4-add-action-calls-to-display-the-includepn-best-practices-analyzerincludespn-best-practices-analyzermd"></a><span data-ttu-id="2b5f7-186">Step 4: Add action calls to display the [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]</span><span class="sxs-lookup"><span data-stu-id="2b5f7-186">Step 4: Add action calls to display the [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]</span></span>

<span data-ttu-id="2b5f7-187">In this step, you'll add actions calls the to **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** toolbar button so that when you click on it, **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** tab is displayed in the hosted control that you created in step 1.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-187">In this step, you'll add actions calls the to **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** toolbar button so that when you click on it, **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** tab is displayed in the hosted control that you created in step 1.</span></span>

1. <span data-ttu-id="2b5f7-188">In the **Settings** toolbar button page, on the nav bar, click the down arrow next to **Settings**, and click **Toolbar Buttons**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-188">In the **Settings** toolbar button page, on the nav bar, click the down arrow next to **Settings**, and click **Toolbar Buttons**.</span></span>

2. <span data-ttu-id="2b5f7-189">Select **Best Practices Analyzer** toolbar button from the list.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-189">Select **Best Practices Analyzer** toolbar button from the list.</span></span>

3. <span data-ttu-id="2b5f7-190">In the **Actions** area, click **+** on the right corner to add a button, and press **ENTER** or click the search icon.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-190">In the **Actions** area, click **+** on the right corner to add a button, and press **ENTER** or click the search icon.</span></span>  

4. <span data-ttu-id="2b5f7-191">Trong hộp tìm kiếm kết quả, bấm vào **Mới** ở góc dưới bên phải để tạo ra cuộc gọi hành động cho nút thanh công cụ này.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-191">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>

5. <span data-ttu-id="2b5f7-192">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="2b5f7-192">On the **New Action Call** page, specify the following values:</span></span>


   |     <span data-ttu-id="2b5f7-193">Trường</span><span class="sxs-lookup"><span data-stu-id="2b5f7-193">Field</span></span>      |                                               <span data-ttu-id="2b5f7-194">Value</span><span class="sxs-lookup"><span data-stu-id="2b5f7-194">Value</span></span>                                               |
   |----------------|---------------------------------------------------------------------------------------------------|
   |      <span data-ttu-id="2b5f7-195">Tên</span><span class="sxs-lookup"><span data-stu-id="2b5f7-195">Name</span></span>      | <span data-ttu-id="2b5f7-196">Action Call: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]</span><span class="sxs-lookup"><span data-stu-id="2b5f7-196">Action Call: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]</span></span> |
   |     <span data-ttu-id="2b5f7-197">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="2b5f7-197">Order</span></span>      |                                                 <span data-ttu-id="2b5f7-198">1</span><span class="sxs-lookup"><span data-stu-id="2b5f7-198">1</span></span>                                                 |
   | <span data-ttu-id="2b5f7-199">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="2b5f7-199">Hosted Control</span></span> |       [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]        |
   |     <span data-ttu-id="2b5f7-200">Hành động</span><span class="sxs-lookup"><span data-stu-id="2b5f7-200">Action</span></span>     |                                              <span data-ttu-id="2b5f7-201">mặc định</span><span class="sxs-lookup"><span data-stu-id="2b5f7-201">default</span></span>                                              |

    <span data-ttu-id="2b5f7-202">![Create action call for Best Practices Analyzer](../media/usd-create-action-call-best-practices-analyzer.PNG "Create action call for Best Practices Analyzer")</span><span class="sxs-lookup"><span data-stu-id="2b5f7-202">![Create action call for Best Practices Analyzer](../media/usd-create-action-call-best-practices-analyzer.PNG "Create action call for Best Practices Analyzer")</span></span>

6. <span data-ttu-id="2b5f7-203">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-203">Click **Save**.</span></span>

7. <span data-ttu-id="2b5f7-204">In the **Actions** area, click **+** on the right corner and type **Action Call: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** in the text box and Press **ENTER** or click on the search icon.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-204">In the **Actions** area, click **+** on the right corner and type **Action Call: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** in the text box and Press **ENTER** or click on the search icon.</span></span>

8. <span data-ttu-id="2b5f7-205">Select the **Action Call: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-205">Select the **Action Call: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**.</span></span> <br>
   <span data-ttu-id="2b5f7-206">The new action call is added to the **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** button.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-206">The new action call is added to the **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** button.</span></span>

9. <span data-ttu-id="2b5f7-207">You’ll add another action call to the button to set the focus on the hosted control that show the [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] in the client application.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-207">You’ll add another action call to the button to set the focus on the hosted control that show the [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] in the client application.</span></span> <span data-ttu-id="2b5f7-208">In the **Actions** area, click **+** on the right corner to add an action call.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-208">In the **Actions** area, click **+** on the right corner to add an action call.</span></span>

10. <span data-ttu-id="2b5f7-209">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-209">In the search results box, click **New** in the lower right corner to create an action call for this toolbar button.</span></span>  

11. <span data-ttu-id="2b5f7-210">Trên trang **Cuộc gọi hành động mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-210">On the **New Action Call** page, specify the following values.</span></span>


    |     <span data-ttu-id="2b5f7-211">Trường</span><span class="sxs-lookup"><span data-stu-id="2b5f7-211">Field</span></span>      |                                            <span data-ttu-id="2b5f7-212">Value</span><span class="sxs-lookup"><span data-stu-id="2b5f7-212">Value</span></span>                                            |
    |----------------|---------------------------------------------------------------------------------------------|
    |      <span data-ttu-id="2b5f7-213">Tên</span><span class="sxs-lookup"><span data-stu-id="2b5f7-213">Name</span></span>      | <span data-ttu-id="2b5f7-214">Focus: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]</span><span class="sxs-lookup"><span data-stu-id="2b5f7-214">Focus: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]</span></span> |
    |     <span data-ttu-id="2b5f7-215">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="2b5f7-215">Order</span></span>      |                                              <span data-ttu-id="2b5f7-216">4</span><span class="sxs-lookup"><span data-stu-id="2b5f7-216">4</span></span>                                              |
    | <span data-ttu-id="2b5f7-217">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="2b5f7-217">Hosted Control</span></span> |                                     <span data-ttu-id="2b5f7-218">Trình quản lý Chung CRM</span><span class="sxs-lookup"><span data-stu-id="2b5f7-218">CRM Global Manager</span></span>                                      |
    |     <span data-ttu-id="2b5f7-219">Hành động</span><span class="sxs-lookup"><span data-stu-id="2b5f7-219">Action</span></span>     |                                           <span data-ttu-id="2b5f7-220">Hiển thị tab</span><span class="sxs-lookup"><span data-stu-id="2b5f7-220">ShowTab</span></span>                                           |
    |      <span data-ttu-id="2b5f7-221">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="2b5f7-221">Data</span></span>      |    [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]     |

    <span data-ttu-id="2b5f7-222">![Create action call to focus on Best Practices Analyzer](../media/usd-create-action-call-focus-best-practices-analyzer.PNG "Create action call to focus on Best Practices Analyzer")</span><span class="sxs-lookup"><span data-stu-id="2b5f7-222">![Create action call to focus on Best Practices Analyzer](../media/usd-create-action-call-focus-best-practices-analyzer.PNG "Create action call to focus on Best Practices Analyzer")</span></span>    

12. <span data-ttu-id="2b5f7-223">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-223">Click **Save**.</span></span>

13. <span data-ttu-id="2b5f7-224">In the **Actions** area, click **+** on the right corner and type **Focus: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** in the text box and Press **ENTER** or click on the search icon.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-224">In the **Actions** area, click **+** on the right corner and type **Focus: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** in the text box and Press **ENTER** or click on the search icon.</span></span>

14. <span data-ttu-id="2b5f7-225">Select the **Focus: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-225">Select the **Focus: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**.</span></span><br>
    <span data-ttu-id="2b5f7-226">The new action call is added to the **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** button.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-226">The new action call is added to the **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** button.</span></span>

<a name="Step5"></a>   
## <a name="step-5-add-the-controls-to-the-configuration"></a><span data-ttu-id="2b5f7-227">Bước 5: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="2b5f7-227">Step 5: Add the controls to the configuration</span></span>  
 <span data-ttu-id="2b5f7-228">In this step, you’ll add the action call, hosted control, toolbar, toolbar buttons, and action calls that were created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-228">In this step, you’ll add the action call, hosted control, toolbar, toolbar buttons, and action calls that were created in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span></span> <span data-ttu-id="2b5f7-229">If you have not created **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-229">If you have not created **Contoso Configuration**.</span></span> <span data-ttu-id="2b5f7-230">Visit, [Walkthrough 1: Build a simple agent application](../../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="2b5f7-230">Visit, [Walkthrough 1: Build a simple agent application](../../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span>

 <span data-ttu-id="2b5f7-231">Thêm sau đây vào **Cấu hình Contoso**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-231">Add the following to **Contoso Configuration**.</span></span>


|                                           <span data-ttu-id="2b5f7-232">Tên kiểm soát</span><span class="sxs-lookup"><span data-stu-id="2b5f7-232">Control name</span></span>                                            |  <span data-ttu-id="2b5f7-233">Loại kiểm soát</span><span class="sxs-lookup"><span data-stu-id="2b5f7-233">Control type</span></span>  |
|---------------------------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="2b5f7-234">Action Call: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]</span><span class="sxs-lookup"><span data-stu-id="2b5f7-234">Action Call: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]</span></span> |  <span data-ttu-id="2b5f7-235">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="2b5f7-235">Action Call</span></span>   |
|    <span data-ttu-id="2b5f7-236">Focus: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]</span><span class="sxs-lookup"><span data-stu-id="2b5f7-236">Focus: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]</span></span>    |  <span data-ttu-id="2b5f7-237">Cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="2b5f7-237">Action Call</span></span>   |
|                                      <span data-ttu-id="2b5f7-238">About Toolbar Container</span><span class="sxs-lookup"><span data-stu-id="2b5f7-238">About Toolbar Container</span></span>                                      | <span data-ttu-id="2b5f7-239">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="2b5f7-239">Hosted Control</span></span> |
|       [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]        | <span data-ttu-id="2b5f7-240">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="2b5f7-240">Hosted Control</span></span> |
|                                           <span data-ttu-id="2b5f7-241">About Toolbar</span><span class="sxs-lookup"><span data-stu-id="2b5f7-241">About Toolbar</span></span>                                           |    <span data-ttu-id="2b5f7-242">Thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="2b5f7-242">Toolbar</span></span>     |

 <span data-ttu-id="2b5f7-243">Để thêm kiểm soát vào cấu hình:</span><span class="sxs-lookup"><span data-stu-id="2b5f7-243">To add a control to the configuration:</span></span>  

1. <span data-ttu-id="2b5f7-244">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-244">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]

3. <span data-ttu-id="2b5f7-245">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-245">Click **Configuration**.</span></span>  

4. <span data-ttu-id="2b5f7-246">Bấm vào **Cấu hình Contoso** để mở định nghĩa.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-246">Click **Contoso Configuration** to open the definition.</span></span>  

5. <span data-ttu-id="2b5f7-247">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Cuộc gọi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-247">On the nav bar, click the down arrow next to **Contoso Configuration**, and select **Action Calls**.</span></span>  

6. <span data-ttu-id="2b5f7-248">On the next page, click **Add Existing Action Call**, type **Action Call: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** in the search bar, and then press **ENTER** or click the search icon.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-248">On the next page, click **Add Existing Action Call**, type **Action Call: [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]** in the search bar, and then press **ENTER** or click the search icon.</span></span>  

7. <span data-ttu-id="2b5f7-249">The action call listed earlier are displayed in the search results.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-249">The action call listed earlier are displayed in the search results.</span></span> <span data-ttu-id="2b5f7-250">Add these action call.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-250">Add these action call.</span></span>

8. <span data-ttu-id="2b5f7-251">Similarly, add the hosted control and the toolbar by clicking the down arrow next to **Contoso Configuration**, and clicking **Hosted Controls** and **Toolbars** respectively.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-251">Similarly, add the hosted control and the toolbar by clicking the down arrow next to **Contoso Configuration**, and clicking **Hosted Controls** and **Toolbars** respectively.</span></span>

9. <span data-ttu-id="2b5f7-252">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-252">Click **Save**.</span></span>

<a name="Step6"></a>   
## <a name="step-6-test-includepn-best-practices-analyzerincludespn-best-practices-analyzermd-in-your-agent-application"></a><span data-ttu-id="2b5f7-253">Step 6: Test [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] in your agent application</span><span class="sxs-lookup"><span data-stu-id="2b5f7-253">Step 6: Test [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] in your agent application</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="2b5f7-254">is a hosted control that helps you analyze the various parameters of your local computer (system configurations and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]), [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations in Dynamics 365, and Internet Explorer settings in your local computer.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-254">is a hosted control that helps you analyze the various parameters of your local computer (system configurations and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]), [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations in Dynamics 365, and Internet Explorer settings in your local computer.</span></span> <span data-ttu-id="2b5f7-255">After the analysis, [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] displays a report that recommends mitigation steps in case of a warning or error.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-255">After the analysis, [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] displays a report that recommends mitigation steps in case of a warning or error.</span></span>

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="2b5f7-256">works best when you handle the warning and error as recommended—this helps you to serve your customers without interruption.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-256">works best when you handle the warning and error as recommended—this helps you to serve your customers without interruption.</span></span>

<span data-ttu-id="2b5f7-257">To analyze parameters on your computer, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations, and internet settings, against the best practices rules:</span><span class="sxs-lookup"><span data-stu-id="2b5f7-257">To analyze parameters on your computer, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations, and internet settings, against the best practices rules:</span></span>

1. <span data-ttu-id="2b5f7-258">Sign in to the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-258">Sign in to the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application.</span></span>

2. <span data-ttu-id="2b5f7-259">On the toolbar, select the **Settings** list.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-259">On the toolbar, select the **Settings** list.</span></span>

3. <span data-ttu-id="2b5f7-260">Select **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-260">Select **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**.</span></span>

    <span data-ttu-id="2b5f7-261">![Create action call to focus on Best Practices Analyzer](../media/best-practices-analyzer-button.PNG "Create action call to focus on Best Practices Analyzer")</span><span class="sxs-lookup"><span data-stu-id="2b5f7-261">![Create action call to focus on Best Practices Analyzer](../media/best-practices-analyzer-button.PNG "Create action call to focus on Best Practices Analyzer")</span></span>

4. <span data-ttu-id="2b5f7-262">Select **Start Analysis**.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-262">Select **Start Analysis**.</span></span><br>
   [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="2b5f7-263">displays the report—it can help you determine your next steps.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-263">displays the report—it can help you determine your next steps.</span></span>

> [!Note]
> <span data-ttu-id="2b5f7-264">When you relaunch [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and select **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**, the last report that was generated appears in the report area.</span><span class="sxs-lookup"><span data-stu-id="2b5f7-264">When you relaunch [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and select **[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]**, the last report that was generated appears in the report area.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b5f7-265">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="2b5f7-265">See also</span></span>

[<span data-ttu-id="2b5f7-266">Analyze best practices in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="2b5f7-266">Analyze best practices in Unified Service Desk</span></span>](../admin/analyze-best-practices-unified-service-desk.md)

[<span data-ttu-id="2b5f7-267">Download and install Best Practices Analyzer</span><span class="sxs-lookup"><span data-stu-id="2b5f7-267">Download and install Best Practices Analyzer</span></span>](../admin/download-install-best-practices-analyzer.md)

[<span data-ttu-id="2b5f7-268">Read Best Practices Analyzer report</span><span class="sxs-lookup"><span data-stu-id="2b5f7-268">Read Best Practices Analyzer report</span></span>](../admin/read-best-practices-analyzer-report.md)

[<span data-ttu-id="2b5f7-269">Best practice rule categories and parameters</span><span class="sxs-lookup"><span data-stu-id="2b5f7-269">Best practice rule categories and parameters</span></span>](../admin/compliance-categories-parameters-bpa.md)

[<span data-ttu-id="2b5f7-270">System configurations</span><span class="sxs-lookup"><span data-stu-id="2b5f7-270">System configurations</span></span>](../admin/system-configurations-bpa.md)

[<span data-ttu-id="2b5f7-271">Internet Explorer settings</span><span class="sxs-lookup"><span data-stu-id="2b5f7-271">Internet Explorer settings</span></span>](../admin/internet-explorer-settings-bpa.md)

[<span data-ttu-id="2b5f7-272">Unified Service Desk configurations</span><span class="sxs-lookup"><span data-stu-id="2b5f7-272">Unified Service Desk configurations</span></span>](../admin/unified-service-desk-configurations-bpa.md)
