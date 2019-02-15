---
title: Unified Service Desk configurations (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about the Unified Service Desk configurations that you make in Dynamics 365 for Customer Engagement on which the Best practices Analyer performs analysis and displays a report.
keywords: ''
ms.date: 04/24/2018
ms.service:
- usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: D390F342-BDD0-4921-959D-66D2CF822A59
author: kabala123
ms.author: kabala
manager: shujoshi
ms.openlocfilehash: ac4672db580c3ed767c9b0caf6a82076f2b001f7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382587"
---
# <a name="includepnunifiedservicedeskincludespn-unified-service-deskmd-configurations"></a>[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="3f195-103">Configurations</span><span class="sxs-lookup"><span data-stu-id="3f195-103">Configurations</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-104">analyzes the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations that you make in Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="3f195-104">analyzes the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations that you make in Dynamics 365 for Customer Engagement apps.</span></span>

## <a name="internal-wpf-hosting-type"></a><span data-ttu-id="3f195-105">Internal WPF Hosting Type</span><span class="sxs-lookup"><span data-stu-id="3f195-105">Internal WPF Hosting Type</span></span>
 
[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-106">checks for **Internal WPF** hosting type hosted controls that you configure in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and displays a warning when one or more Internal WPF hosting type hosted controls are configured.</span><span class="sxs-lookup"><span data-stu-id="3f195-106">checks for **Internal WPF** hosting type hosted controls that you configure in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and displays a warning when one or more Internal WPF hosting type hosted controls are configured.</span></span>

<span data-ttu-id="3f195-107">We recommend that you move the **Hosting Type** of all the hosted controls of component type **CRM Page** or **Standard Web Application** from **Internal WPF** to **IE Process**.</span><span class="sxs-lookup"><span data-stu-id="3f195-107">We recommend that you move the **Hosting Type** of all the hosted controls of component type **CRM Page** or **Standard Web Application** from **Internal WPF** to **IE Process**.</span></span>

### <a name="mitigation"></a><span data-ttu-id="3f195-108">Mitigation</span><span class="sxs-lookup"><span data-stu-id="3f195-108">Mitigation</span></span>

<span data-ttu-id="3f195-109">For all the hosted controls of component type **CRM Page** or **Standard Web Application**, we recommend that you move the hosting type from **Internal WPF** to **IE Process**.</span><span class="sxs-lookup"><span data-stu-id="3f195-109">For all the hosted controls of component type **CRM Page** or **Standard Web Application**, we recommend that you move the hosting type from **Internal WPF** to **IE Process**.</span></span>

1. <span data-ttu-id="3f195-110">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="3f195-110">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>
2. <span data-ttu-id="3f195-111">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="3f195-111">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Hosted Controls**.</span></span>
3. <span data-ttu-id="3f195-112">Select the applicable hosted controls from the list.</span><span class="sxs-lookup"><span data-stu-id="3f195-112">Select the applicable hosted controls from the list.</span></span> </br><span data-ttu-id="3f195-113">You can change the hosting type for only CRM Page and Standard Web Application hosted controls.</span><span class="sxs-lookup"><span data-stu-id="3f195-113">You can change the hosting type for only CRM Page and Standard Web Application hosted controls.</span></span>
4. <span data-ttu-id="3f195-114">In the **Hosting Type** list, select **IE Process**.</span><span class="sxs-lookup"><span data-stu-id="3f195-114">In the **Hosting Type** list, select **IE Process**.</span></span>
5. <span data-ttu-id="3f195-115">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="3f195-115">Select **Save**.</span></span>

## <a name="actions-calls-in-pageloadcomplete-event"></a><span data-ttu-id="3f195-116">Actions Calls in PageLoadComplete Event</span><span class="sxs-lookup"><span data-stu-id="3f195-116">Actions Calls in PageLoadComplete Event</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-117">checks and displays a warning message when you associate any action calls with the **PageLoadComplete** event.</span><span class="sxs-lookup"><span data-stu-id="3f195-117">checks and displays a warning message when you associate any action calls with the **PageLoadComplete** event.</span></span>
<!--Editing: Above, I changed "PageLoadDocument" to "PageLoadComplete"; please correct if this is wrong. -->

<span data-ttu-id="3f195-118">Action calls that are associated with the **PageLoadComplete** event occur several times per page load when an iFrame or frame is used on the CRM entity forms.</span><span class="sxs-lookup"><span data-stu-id="3f195-118">Action calls that are associated with the **PageLoadComplete** event occur several times per page load when an iFrame or frame is used on the CRM entity forms.</span></span>

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="3f195-119">works best when **PageLoadComplete** is replaced with a **BrowserDocumentComplete** or **DataReady** event if you're using this event for CRM entity forms.</span><span class="sxs-lookup"><span data-stu-id="3f195-119">works best when **PageLoadComplete** is replaced with a **BrowserDocumentComplete** or **DataReady** event if you're using this event for CRM entity forms.</span></span>

### <a name="mitigation"></a><span data-ttu-id="3f195-120">Mitigation</span><span class="sxs-lookup"><span data-stu-id="3f195-120">Mitigation</span></span>

<span data-ttu-id="3f195-121">Replace the **PageLoadComplete** event with a **BrowserDocumentComplete** event or **DataReady** event if you're using it for CRM entity forms.</span><span class="sxs-lookup"><span data-stu-id="3f195-121">Replace the **PageLoadComplete** event with a **BrowserDocumentComplete** event or **DataReady** event if you're using it for CRM entity forms.</span></span>

> [!Note]
> <span data-ttu-id="3f195-122">The **DataReady** event is available for use in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] 3.0 or later.</span><span class="sxs-lookup"><span data-stu-id="3f195-122">The **DataReady** event is available for use in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] 3.0 or later.</span></span>

## <a name="actions-calls-with-events"></a><span data-ttu-id="3f195-123">Actions Calls with Events</span><span class="sxs-lookup"><span data-stu-id="3f195-123">Actions Calls with Events</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-124">checks and displays a warning when you associate 10 or more action calls with the events listed in the following table.</span><span class="sxs-lookup"><span data-stu-id="3f195-124">checks and displays a warning when you associate 10 or more action calls with the events listed in the following table.</span></span>

|<span data-ttu-id="3f195-125">Sự kiện</span><span class="sxs-lookup"><span data-stu-id="3f195-125">Event</span></span>|<span data-ttu-id="3f195-126">Mô tả</span><span class="sxs-lookup"><span data-stu-id="3f195-126">Description</span></span>|
|-----------|------------|
|<span data-ttu-id="3f195-127">**DesktopReady**</span><span class="sxs-lookup"><span data-stu-id="3f195-127">**DesktopReady**</span></span>|<span data-ttu-id="3f195-128">A **DesktopReady** event occurs on startup after all the desktop initialization are complete and the connections to Dynamics 365 for Customer Engagement are established.</span><span class="sxs-lookup"><span data-stu-id="3f195-128">A **DesktopReady** event occurs on startup after all the desktop initialization are complete and the connections to Dynamics 365 for Customer Engagement are established.</span></span>
|<span data-ttu-id="3f195-129">**Phiên mới**</span><span class="sxs-lookup"><span data-stu-id="3f195-129">**SessionNew**</span></span>|<span data-ttu-id="3f195-130">A **SessionNew** event occurs when a new session is created.</span><span class="sxs-lookup"><span data-stu-id="3f195-130">A **SessionNew** event occurs when a new session is created.</span></span>|
|<span data-ttu-id="3f195-131">**Phiên đã kích hoạt**</span><span class="sxs-lookup"><span data-stu-id="3f195-131">**SessionActivated**</span></span>|<span data-ttu-id="3f195-132">A **SessionActivated** event occurs when a new session is activated.</span><span class="sxs-lookup"><span data-stu-id="3f195-132">A **SessionActivated** event occurs when a new session is activated.</span></span>|
|<span data-ttu-id="3f195-133">**Phiên đã hủy kích hoạt**</span><span class="sxs-lookup"><span data-stu-id="3f195-133">**SessionDeactivated**</span></span>|<span data-ttu-id="3f195-134">A **SessionDeactivated** event occurs when a new session is deactivated.</span><span class="sxs-lookup"><span data-stu-id="3f195-134">A **SessionDeactivated** event occurs when a new session is deactivated.</span></span>|
|<span data-ttu-id="3f195-135">**Đã đóng phiên**</span><span class="sxs-lookup"><span data-stu-id="3f195-135">**SessionClosed**</span></span>|<span data-ttu-id="3f195-136">A **SessionClosed** event occurs when a session is closed.</span><span class="sxs-lookup"><span data-stu-id="3f195-136">A **SessionClosed** event occurs when a session is closed.</span></span>|

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="3f195-137">works best when you associate 10 or fewer actions with any event.</span><span class="sxs-lookup"><span data-stu-id="3f195-137">works best when you associate 10 or fewer actions with any event.</span></span>

### <a name="mitigation"></a><span data-ttu-id="3f195-138">Mitigation</span><span class="sxs-lookup"><span data-stu-id="3f195-138">Mitigation</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-139">recommends optimizing to associate 10 or fewers action calls with **DesktopReady**, **SessionNew** **SessionActivated**, **SessionDeactivated**, and **SessionClosed** events.</span><span class="sxs-lookup"><span data-stu-id="3f195-139">recommends optimizing to associate 10 or fewers action calls with **DesktopReady**, **SessionNew** **SessionActivated**, **SessionDeactivated**, and **SessionClosed** events.</span></span>

## <a name="number-of-navigation-rules"></a><span data-ttu-id="3f195-140">Number of Navigation Rules</span><span class="sxs-lookup"><span data-stu-id="3f195-140">Number of Navigation Rules</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-141">checks for the number of navigation rules that you configure in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and displays a warning message when the value is more than **50**.</span><span class="sxs-lookup"><span data-stu-id="3f195-141">checks for the number of navigation rules that you configure in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and displays a warning message when the value is more than **50**.</span></span>

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="3f195-142">works best when 50 or fewer navigation rules are configured.</span><span class="sxs-lookup"><span data-stu-id="3f195-142">works best when 50 or fewer navigation rules are configured.</span></span>

### <a name="mitigation"></a><span data-ttu-id="3f195-143">Mitigation</span><span class="sxs-lookup"><span data-stu-id="3f195-143">Mitigation</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-144">recommends optimizing the number of navigation rules in the range between 0 and 50.</span><span class="sxs-lookup"><span data-stu-id="3f195-144">recommends optimizing the number of navigation rules in the range between 0 and 50.</span></span>

## <a name="show-script-errors-showscripterrors"></a><span data-ttu-id="3f195-145">Show Script Errors (ShowScriptErrors)</span><span class="sxs-lookup"><span data-stu-id="3f195-145">Show Script Errors (ShowScriptErrors)</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-146">checks for the **ShowScriptErrors** value and displays a warning message when the value is set to **true**.</span><span class="sxs-lookup"><span data-stu-id="3f195-146">checks for the **ShowScriptErrors** value and displays a warning message when the value is set to **true**.</span></span>

<span data-ttu-id="3f195-147">When you enable Show Script Errors, you often see pop-up error messages.</span><span class="sxs-lookup"><span data-stu-id="3f195-147">When you enable Show Script Errors, you often see pop-up error messages.</span></span>

<span data-ttu-id="3f195-148">To work without interruption, you can set the **ShowScriptErrors** value to **false**.</span><span class="sxs-lookup"><span data-stu-id="3f195-148">To work without interruption, you can set the **ShowScriptErrors** value to **false**.</span></span>

### <a name="mitigation"></a><span data-ttu-id="3f195-149">Mitigation</span><span class="sxs-lookup"><span data-stu-id="3f195-149">Mitigation</span></span>

<span data-ttu-id="3f195-150">Set **ShowScriptErrors** to **false**:</span><span class="sxs-lookup"><span data-stu-id="3f195-150">Set **ShowScriptErrors** to **false**:</span></span>

1. <span data-ttu-id="3f195-151">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="3f195-151">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>
2. <span data-ttu-id="3f195-152">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**</span><span class="sxs-lookup"><span data-stu-id="3f195-152">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**</span></span>
3. <span data-ttu-id="3f195-153">In the list of options, select **ShowScriptErrors**.</span><span class="sxs-lookup"><span data-stu-id="3f195-153">In the list of options, select **ShowScriptErrors**.</span></span>
4. <span data-ttu-id="3f195-154">In the **Value** field, select **false**.</span><span class="sxs-lookup"><span data-stu-id="3f195-154">In the **Value** field, select **false**.</span></span>
5. <span data-ttu-id="3f195-155">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="3f195-155">Select **Save**.</span></span>

[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="3f195-156">[Manage Options for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/manage-options-unified-service-desk)</span><span class="sxs-lookup"><span data-stu-id="3f195-156">[Manage Options for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/manage-options-unified-service-desk)</span></span>

## <a name="client-caching"></a><span data-ttu-id="3f195-157">Client Caching</span><span class="sxs-lookup"><span data-stu-id="3f195-157">Client Caching</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-158">checks for the client caching option and displays a warning message when the field is blank.</span><span class="sxs-lookup"><span data-stu-id="3f195-158">checks for the client caching option and displays a warning message when the field is blank.</span></span>

<span data-ttu-id="3f195-159">You can use client caching to reduce the amount of bandwidth required during [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] startup.</span><span class="sxs-lookup"><span data-stu-id="3f195-159">You can use client caching to reduce the amount of bandwidth required during [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] startup.</span></span>

### <a name="mitigation"></a><span data-ttu-id="3f195-160">Mitigation</span><span class="sxs-lookup"><span data-stu-id="3f195-160">Mitigation</span></span>

<span data-ttu-id="3f195-161">Enable client caching:</span><span class="sxs-lookup"><span data-stu-id="3f195-161">Enable client caching:</span></span>

1. <span data-ttu-id="3f195-162">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="3f195-162">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>
2. <span data-ttu-id="3f195-163">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**</span><span class="sxs-lookup"><span data-stu-id="3f195-163">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**</span></span>
3. <span data-ttu-id="3f195-164">To create a new option, select **New** on the command bar.</span><span class="sxs-lookup"><span data-stu-id="3f195-164">To create a new option, select **New** on the command bar.</span></span>
4. <span data-ttu-id="3f195-165">For the new option, select **ClientCacheVersionNumber** in the **Name** box, and then type an alphanumeric number in the **Value** box.</span><span class="sxs-lookup"><span data-stu-id="3f195-165">For the new option, select **ClientCacheVersionNumber** in the **Name** box, and then type an alphanumeric number in the **Value** box.</span></span> <br/><span data-ttu-id="3f195-166">Giá trị số và chữ cái được sử dụng như là khóa bộ nhớ đệm cho [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="3f195-166">The alphanumeric value is used as the cache key for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="3f195-167">The alphanumeric value can be of any value but unique for each time you change.</span><span class="sxs-lookup"><span data-stu-id="3f195-167">The alphanumeric value can be of any value but unique for each time you change.</span></span>
5. <span data-ttu-id="3f195-168">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="3f195-168">Select **Save**.</span></span>

> [!Note]
> <span data-ttu-id="3f195-169">When an agent launches the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client again, client caching isn't used.</span><span class="sxs-lookup"><span data-stu-id="3f195-169">When an agent launches the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client again, client caching isn't used.</span></span> <span data-ttu-id="3f195-170">However, it doesn't delete or refresh the client cache store for the agent.</span><span class="sxs-lookup"><span data-stu-id="3f195-170">However, it doesn't delete or refresh the client cache store for the agent.</span></span> <span data-ttu-id="3f195-171">When you remove the **DisableCaching** key for the agent, the agent returns to using the previously stored client cache store.</span><span class="sxs-lookup"><span data-stu-id="3f195-171">When you remove the **DisableCaching** key for the agent, the agent returns to using the previously stored client cache store.</span></span>

[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="3f195-172">[Enable client caching](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/configure-client-caching-unified-service-desk)</span><span class="sxs-lookup"><span data-stu-id="3f195-172">[Enable client caching](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/configure-client-caching-unified-service-desk)</span></span>

## <a name="maximum-number-of-sessions-maxnumberofsessions"></a><span data-ttu-id="3f195-173">Maximum Number of Sessions (maxNumberOfSessions)</span><span class="sxs-lookup"><span data-stu-id="3f195-173">Maximum Number of Sessions (maxNumberOfSessions)</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-174">checks for the **maxNumberOfSessions** option and displays a warning message or an error message in accordance with the following table.</span><span class="sxs-lookup"><span data-stu-id="3f195-174">checks for the **maxNumberOfSessions** option and displays a warning message or an error message in accordance with the following table.</span></span>

|<span data-ttu-id="3f195-175">Mức độ nghiêm trọng</span><span class="sxs-lookup"><span data-stu-id="3f195-175">Severity</span></span>| <span data-ttu-id="3f195-176">maxNumberOfSessions</span><span class="sxs-lookup"><span data-stu-id="3f195-176">maxNumberOfSessions</span></span> |
|---------|---------------------|
| <span data-ttu-id="3f195-177">Lỗi</span><span class="sxs-lookup"><span data-stu-id="3f195-177">Error</span></span>   | <span data-ttu-id="3f195-178">0</span><span class="sxs-lookup"><span data-stu-id="3f195-178">0</span></span>                   |
| <span data-ttu-id="3f195-179">Lỗi</span><span class="sxs-lookup"><span data-stu-id="3f195-179">Error</span></span>   | <span data-ttu-id="3f195-180">More than 5</span><span class="sxs-lookup"><span data-stu-id="3f195-180">More than 5</span></span>         |
| <span data-ttu-id="3f195-181">Cảnh báo</span><span class="sxs-lookup"><span data-stu-id="3f195-181">Warning</span></span> | <span data-ttu-id="3f195-182">4 or 5</span><span class="sxs-lookup"><span data-stu-id="3f195-182">4 or 5</span></span>              |

<span data-ttu-id="3f195-183">**maxNumberOfSesions** indicates the maximum number of simultaneous sessions that each user can open using [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="3f195-183">**maxNumberOfSesions** indicates the maximum number of simultaneous sessions that each user can open using [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span>

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="3f195-184">works best when the **maxNumberOfSesions** value is more than **0** and less than or equal to **3**.</span><span class="sxs-lookup"><span data-stu-id="3f195-184">works best when the **maxNumberOfSesions** value is more than **0** and less than or equal to **3**.</span></span>

### <a name="mitigation"></a><span data-ttu-id="3f195-185">Mitigation</span><span class="sxs-lookup"><span data-stu-id="3f195-185">Mitigation</span></span>

<span data-ttu-id="3f195-186">Set the **maxNumberOfSesions** value to less than or equal to **3**:</span><span class="sxs-lookup"><span data-stu-id="3f195-186">Set the **maxNumberOfSesions** value to less than or equal to **3**:</span></span> 

1. <span data-ttu-id="3f195-187">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="3f195-187">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>
2. <span data-ttu-id="3f195-188">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**</span><span class="sxs-lookup"><span data-stu-id="3f195-188">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**</span></span>
3. <span data-ttu-id="3f195-189">In the list of options, select **maxNumberOfSesions**.</span><span class="sxs-lookup"><span data-stu-id="3f195-189">In the list of options, select **maxNumberOfSesions**.</span></span>
4. <span data-ttu-id="3f195-190">In the **Value** field, type **3**.</span><span class="sxs-lookup"><span data-stu-id="3f195-190">In the **Value** field, type **3**.</span></span>
5. <span data-ttu-id="3f195-191">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="3f195-191">Select **Save**.</span></span>

[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="3f195-192">[Manage Options for Unified Service Desk](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/manage-options-unified-service-desk)</span><span class="sxs-lookup"><span data-stu-id="3f195-192">[Manage Options for Unified Service Desk](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/manage-options-unified-service-desk)</span></span>

## <a name="help-improve-includepnunifiedservicedeskincludespn-unified-service-deskmd-helpimproveusd"></a><span data-ttu-id="3f195-193">Help Improve [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] (HelpImproveUSD)</span><span class="sxs-lookup"><span data-stu-id="3f195-193">Help Improve [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] (HelpImproveUSD)</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-194">checks for `HelpImproveUSD` User Interface Integration (UII) option and displays a warning message when the value is set to **false**.</span><span class="sxs-lookup"><span data-stu-id="3f195-194">checks for `HelpImproveUSD` User Interface Integration (UII) option and displays a warning message when the value is set to **false**.</span></span>

<span data-ttu-id="3f195-195">By using the Help Improve [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] program, organization-wide agents can send improvement program information to Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3f195-195">By using the Help Improve [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] program, organization-wide agents can send improvement program information to Microsoft.</span></span> <span data-ttu-id="3f195-196">To enable the program, activate (set to **true**) the **HelpImproveUSD** option.</span><span class="sxs-lookup"><span data-stu-id="3f195-196">To enable the program, activate (set to **true**) the **HelpImproveUSD** option.</span></span>

### <a name="mitigation"></a><span data-ttu-id="3f195-197">Mitigation</span><span class="sxs-lookup"><span data-stu-id="3f195-197">Mitigation</span></span>

<span data-ttu-id="3f195-198">Set `HelpImproveUSD` to **true**:</span><span class="sxs-lookup"><span data-stu-id="3f195-198">Set `HelpImproveUSD` to **true**:</span></span>

1. <span data-ttu-id="3f195-199">Sign in to Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="3f195-199">Sign in to Dynamics 365 for Customer Engagement apps.</span></span>
2. <span data-ttu-id="3f195-200">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**</span><span class="sxs-lookup"><span data-stu-id="3f195-200">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**</span></span>
3. <span data-ttu-id="3f195-201">To create a new option, select **New** on the command bar.</span><span class="sxs-lookup"><span data-stu-id="3f195-201">To create a new option, select **New** on the command bar.</span></span>
4. <span data-ttu-id="3f195-202">On the New Option page, select **HelpImproveUSD** in the **Global Options** list.</span><span class="sxs-lookup"><span data-stu-id="3f195-202">On the New Option page, select **HelpImproveUSD** in the **Global Options** list.</span></span>
5. <span data-ttu-id="3f195-203">In the **Value** field, select **true**.</span><span class="sxs-lookup"><span data-stu-id="3f195-203">In the **Value** field, select **true**.</span></span>
6. <span data-ttu-id="3f195-204">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="3f195-204">Select **Save**.</span></span>

[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="3f195-205">[Enable client caching](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/configure-client-caching-unified-service-desk)</span><span class="sxs-lookup"><span data-stu-id="3f195-205">[Enable client caching](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/configure-client-caching-unified-service-desk)</span></span>

## <a name="internet-explorer-pooling-internetexplorerpooling"></a><span data-ttu-id="3f195-206">Internet Explorer Pooling (InternetExplorerPooling)</span><span class="sxs-lookup"><span data-stu-id="3f195-206">Internet Explorer Pooling (InternetExplorerPooling)</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-207">checks for the **InternetExplorerPooling** UII option and displays a warning message when the value is set to **false**.</span><span class="sxs-lookup"><span data-stu-id="3f195-207">checks for the **InternetExplorerPooling** UII option and displays a warning message when the value is set to **false**.</span></span>

<span data-ttu-id="3f195-208">Internet Explorer Pooling enhances performance of CRM entity page loading in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="3f195-208">Internet Explorer Pooling enhances performance of CRM entity page loading in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span><br> [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="3f195-209">works best when the **InternetExplorerPooling** option is set to **true**.</span><span class="sxs-lookup"><span data-stu-id="3f195-209">works best when the **InternetExplorerPooling** option is set to **true**.</span></span> <span data-ttu-id="3f195-210">You must configure the **InternetExplorerPooling** option to set it to **true**.</span><span class="sxs-lookup"><span data-stu-id="3f195-210">You must configure the **InternetExplorerPooling** option to set it to **true**.</span></span>

### <a name="mitigation"></a><span data-ttu-id="3f195-211">Mitigation</span><span class="sxs-lookup"><span data-stu-id="3f195-211">Mitigation</span></span>

<span data-ttu-id="3f195-212">Set the **InternetExplorerPooling** option to **true**:</span><span class="sxs-lookup"><span data-stu-id="3f195-212">Set the **InternetExplorerPooling** option to **true**:</span></span>

1. <span data-ttu-id="3f195-213">Sign in to Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="3f195-213">Sign in to Dynamics 365 for Customer Engagement apps.</span></span>
2. <span data-ttu-id="3f195-214">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**</span><span class="sxs-lookup"><span data-stu-id="3f195-214">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**</span></span>
3. <span data-ttu-id="3f195-215">On the **Active UII Options** page, select **New**.</span><span class="sxs-lookup"><span data-stu-id="3f195-215">On the **Active UII Options** page, select **New**.</span></span>
4. <span data-ttu-id="3f195-216">In the **Global Option** field, select **Others**.</span><span class="sxs-lookup"><span data-stu-id="3f195-216">In the **Global Option** field, select **Others**.</span></span>
5. <span data-ttu-id="3f195-217">In the **Name** field, enter **InternetExplorerPooling**.</span><span class="sxs-lookup"><span data-stu-id="3f195-217">In the **Name** field, enter **InternetExplorerPooling**.</span></span>
6. <span data-ttu-id="3f195-218">In the **Value** field, select **true**.</span><span class="sxs-lookup"><span data-stu-id="3f195-218">In the **Value** field, select **true**.</span></span>
7. <span data-ttu-id="3f195-219">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="3f195-219">Select **Save**.</span></span>

[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="3f195-220">[**Enable Internet Explorer pooling**](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/performance-enhancement-crm-entity-page-loads)</span><span class="sxs-lookup"><span data-stu-id="3f195-220">[**Enable Internet Explorer pooling**](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/performance-enhancement-crm-entity-page-loads)</span></span>

## <a name="activity-tracking-enabled"></a><span data-ttu-id="3f195-221">Activity Tracking Enabled</span><span class="sxs-lookup"><span data-stu-id="3f195-221">Activity Tracking Enabled</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-222">checks for the **Activity Tracking Enabled** option and displays a warning message when the option is disabled.</span><span class="sxs-lookup"><span data-stu-id="3f195-222">checks for the **Activity Tracking Enabled** option and displays a warning message when the option is disabled.</span></span>

<span data-ttu-id="3f195-223">By using Activity Tracking Enabled options, you can track all the events for audit and diagnostic purposes.</span><span class="sxs-lookup"><span data-stu-id="3f195-223">By using Activity Tracking Enabled options, you can track all the events for audit and diagnostic purposes.</span></span>

### <a name="mitigation"></a><span data-ttu-id="3f195-224">Mitigation</span><span class="sxs-lookup"><span data-stu-id="3f195-224">Mitigation</span></span>

<span data-ttu-id="3f195-225">Enable the **Activity Tracking Enabled** option:</span><span class="sxs-lookup"><span data-stu-id="3f195-225">Enable the **Activity Tracking Enabled** option:</span></span>

1. <span data-ttu-id="3f195-226">Sign in to Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="3f195-226">Sign in to Dynamics 365 for Customer Engagement apps.</span></span>
2. <span data-ttu-id="3f195-227">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Audit & Diagnostics Settings**</span><span class="sxs-lookup"><span data-stu-id="3f195-227">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Audit & Diagnostics Settings**</span></span>
3. <span data-ttu-id="3f195-228">In the **Audit Settings** section, select the **Activity Tracking Enabled** check box.</span><span class="sxs-lookup"><span data-stu-id="3f195-228">In the **Audit Settings** section, select the **Activity Tracking Enabled** check box.</span></span>
4. <span data-ttu-id="3f195-229">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="3f195-229">Select **Save**.</span></span>

[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="3f195-230">[**Auditing**](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk)</span><span class="sxs-lookup"><span data-stu-id="3f195-230">[**Auditing**](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk)</span></span>

## <a name="diagnostic-tracking-enabled"></a><span data-ttu-id="3f195-231">Diagnostic Tracking Enabled</span><span class="sxs-lookup"><span data-stu-id="3f195-231">Diagnostic Tracking Enabled</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-232">checks for the **Diagnostic Tracking Enabled** option and displays a warning message when the option is disabled.</span><span class="sxs-lookup"><span data-stu-id="3f195-232">checks for the **Diagnostic Tracking Enabled** option and displays a warning message when the option is disabled.</span></span>
<span data-ttu-id="3f195-233">By using **Diagnostic Tracking Enabled**, you can record operational events and errors in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] log files.</span><span class="sxs-lookup"><span data-stu-id="3f195-233">By using **Diagnostic Tracking Enabled**, you can record operational events and errors in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] log files.</span></span>

### <a name="mitigation"></a><span data-ttu-id="3f195-234">Mitigation</span><span class="sxs-lookup"><span data-stu-id="3f195-234">Mitigation</span></span>

<span data-ttu-id="3f195-235">Enable the **Diagnostic Tracking Enabled** option:</span><span class="sxs-lookup"><span data-stu-id="3f195-235">Enable the **Diagnostic Tracking Enabled** option:</span></span>

1. <span data-ttu-id="3f195-236">Sign in to Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="3f195-236">Sign in to Dynamics 365 for Customer Engagement apps.</span></span>
2. <span data-ttu-id="3f195-237">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Audit & Diagnostics Settings**</span><span class="sxs-lookup"><span data-stu-id="3f195-237">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Audit & Diagnostics Settings**</span></span>
3. <span data-ttu-id="3f195-238">In the **Diagnostic Settings** section, select the **Diagnostic Tracking Enabled** check box.</span><span class="sxs-lookup"><span data-stu-id="3f195-238">In the **Diagnostic Settings** section, select the **Diagnostic Tracking Enabled** check box.</span></span>
4. <span data-ttu-id="3f195-239">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="3f195-239">Select **Save**.</span></span>

[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="3f195-240">[**Diagnostics**](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk)</span><span class="sxs-lookup"><span data-stu-id="3f195-240">[**Diagnostics**](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk)</span></span>

## <a name="enable-exit-monitoring"></a><span data-ttu-id="3f195-241">Enable Exit Monitoring</span><span class="sxs-lookup"><span data-stu-id="3f195-241">Enable Exit Monitoring</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-242">checks for the **Enable Exit Monitoring** option and displays a warning message when the option is disabled.</span><span class="sxs-lookup"><span data-stu-id="3f195-242">checks for the **Enable Exit Monitoring** option and displays a warning message when the option is disabled.</span></span>

<span data-ttu-id="3f195-243">**Enable Exit Monitoring** collects diagnostics logs and exit logs in the event of an exception in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.</span><span class="sxs-lookup"><span data-stu-id="3f195-243">**Enable Exit Monitoring** collects diagnostics logs and exit logs in the event of an exception in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.</span></span>

### <a name="mitigation"></a><span data-ttu-id="3f195-244">Mitigation</span><span class="sxs-lookup"><span data-stu-id="3f195-244">Mitigation</span></span>

<span data-ttu-id="3f195-245">Enable the **Enable Exit Monitoring** option:</span><span class="sxs-lookup"><span data-stu-id="3f195-245">Enable the **Enable Exit Monitoring** option:</span></span>

1. <span data-ttu-id="3f195-246">Sign in to Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="3f195-246">Sign in to Dynamics 365 for Customer Engagement apps.</span></span>
2. <span data-ttu-id="3f195-247">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Audit & Diagnostics Settings**</span><span class="sxs-lookup"><span data-stu-id="3f195-247">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Audit & Diagnostics Settings**</span></span>
3. <span data-ttu-id="3f195-248">In the **Diagnostic Settings** section, select the **Enable Exit Monitoring** check box.</span><span class="sxs-lookup"><span data-stu-id="3f195-248">In the **Diagnostic Settings** section, select the **Enable Exit Monitoring** check box.</span></span>
4. <span data-ttu-id="3f195-249">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="3f195-249">Select **Save**.</span></span>

[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="3f195-250">[**Diagnostics**](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk)</span><span class="sxs-lookup"><span data-stu-id="3f195-250">[**Diagnostics**](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk)</span></span>

## <a name="enable-crash-dump-generation"></a><span data-ttu-id="3f195-251">Enable Crash Dump Generation</span><span class="sxs-lookup"><span data-stu-id="3f195-251">Enable Crash Dump Generation</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-252">checks for the **Enable Crash Dump Generation** option and displays a warning message when the option is disabled.</span><span class="sxs-lookup"><span data-stu-id="3f195-252">checks for the **Enable Crash Dump Generation** option and displays a warning message when the option is disabled.</span></span>

<span data-ttu-id="3f195-253">By using Enable Crash Dump Generation, you can collect dump files during a fatal exception of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="3f195-253">By using Enable Crash Dump Generation, you can collect dump files during a fatal exception of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span>

### <a name="mitigation"></a><span data-ttu-id="3f195-254">Mitigation</span><span class="sxs-lookup"><span data-stu-id="3f195-254">Mitigation</span></span>

<span data-ttu-id="3f195-255">Enable the **Enable Crash Dump Generation** option:</span><span class="sxs-lookup"><span data-stu-id="3f195-255">Enable the **Enable Crash Dump Generation** option:</span></span>

1. <span data-ttu-id="3f195-256">Sign in to Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="3f195-256">Sign in to Dynamics 365 for Customer Engagement apps.</span></span>
2. <span data-ttu-id="3f195-257">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Audit & Diagnostics Settings**</span><span class="sxs-lookup"><span data-stu-id="3f195-257">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Audit & Diagnostics Settings**</span></span>
3. <span data-ttu-id="3f195-258">In the **Diagnostic Settings** section, select the **Enable Crash Dump Generation** check box.</span><span class="sxs-lookup"><span data-stu-id="3f195-258">In the **Diagnostic Settings** section, select the **Enable Crash Dump Generation** check box.</span></span>
4. <span data-ttu-id="3f195-259">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="3f195-259">Select **Save**.</span></span>

[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="3f195-260">[**Diagnostics**](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk)</span><span class="sxs-lookup"><span data-stu-id="3f195-260">[**Diagnostics**](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk)</span></span>  

## <a name="internet-explorer-webpage-recovery-iewebpagerecovery"></a><span data-ttu-id="3f195-261">Internet Explorer Webpage Recovery (IEWebPageRecovery)</span><span class="sxs-lookup"><span data-stu-id="3f195-261">Internet Explorer Webpage Recovery (IEWebPageRecovery)</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-262">checks for the **IEWebPageRecovery** UII option and displays an error message when the option is set to **false**.</span><span class="sxs-lookup"><span data-stu-id="3f195-262">checks for the **IEWebPageRecovery** UII option and displays an error message when the option is set to **false**.</span></span>

<span data-ttu-id="3f195-263">**IEWebPageRecovery** is an UII option that a system administrator can modify.</span><span class="sxs-lookup"><span data-stu-id="3f195-263">**IEWebPageRecovery** is an UII option that a system administrator can modify.</span></span> <span data-ttu-id="3f195-264">The option helps recover unresponsive Internet Explorer webpages.</span><span class="sxs-lookup"><span data-stu-id="3f195-264">The option helps recover unresponsive Internet Explorer webpages.</span></span> [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="3f195-265">works best when the **IEWebPageRecovery** option is set to **true**.</span><span class="sxs-lookup"><span data-stu-id="3f195-265">works best when the **IEWebPageRecovery** option is set to **true**.</span></span>

### <a name="mitigation"></a><span data-ttu-id="3f195-266">Mitigation</span><span class="sxs-lookup"><span data-stu-id="3f195-266">Mitigation</span></span>

<span data-ttu-id="3f195-267">Set the `IEWebPageRecovery` option to **true**.</span><span class="sxs-lookup"><span data-stu-id="3f195-267">Set the `IEWebPageRecovery` option to **true**.</span></span>

1. <span data-ttu-id="3f195-268">Sign in to Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="3f195-268">Sign in to Dynamics 365 for Customer Engagement apps.</span></span>
2. <span data-ttu-id="3f195-269">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**</span><span class="sxs-lookup"><span data-stu-id="3f195-269">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**</span></span>
3. <span data-ttu-id="3f195-270">In the list of options, select **IEWebPageRecovery**.</span><span class="sxs-lookup"><span data-stu-id="3f195-270">In the list of options, select **IEWebPageRecovery**.</span></span>
4. <span data-ttu-id="3f195-271">In the **Value** field, select **true**.</span><span class="sxs-lookup"><span data-stu-id="3f195-271">In the **Value** field, select **true**.</span></span>
5. <span data-ttu-id="3f195-272">Specify **Save**.</span><span class="sxs-lookup"><span data-stu-id="3f195-272">Specify **Save**.</span></span>

[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="3f195-273">[Manage Options for Unified Service Desk](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/manage-options-unified-service-desk)</span><span class="sxs-lookup"><span data-stu-id="3f195-273">[Manage Options for Unified Service Desk](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/manage-options-unified-service-desk)</span></span>

## <a name="process-termination-threshold-processterminationthreshold"></a><span data-ttu-id="3f195-274">Process Termination Threshold (ProcessTerminationThreshold)</span><span class="sxs-lookup"><span data-stu-id="3f195-274">Process Termination Threshold (ProcessTerminationThreshold)</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="3f195-275">checks for the **ProcessTerminationThreshold** UII option and displays an error message when the value is set to **0**.</span><span class="sxs-lookup"><span data-stu-id="3f195-275">checks for the **ProcessTerminationThreshold** UII option and displays an error message when the value is set to **0**.</span></span>

<span data-ttu-id="3f195-276">**ProcessTerminationThreshold** indicates the timeout period for the duration (in milliseconds) that the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] monitoring process (usdmp.exe) waits before terminating an unresponsive Internet Explorer process, which also causes [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to become unresponsive.</span><span class="sxs-lookup"><span data-stu-id="3f195-276">**ProcessTerminationThreshold** indicates the timeout period for the duration (in milliseconds) that the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] monitoring process (usdmp.exe) waits before terminating an unresponsive Internet Explorer process, which also causes [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to become unresponsive.</span></span> [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="3f195-277">works best when **ProcessTerminationThreshold** option is set between the range **0** and **30000**.</span><span class="sxs-lookup"><span data-stu-id="3f195-277">works best when **ProcessTerminationThreshold** option is set between the range **0** and **30000**.</span></span>

### <a name="mitigation"></a><span data-ttu-id="3f195-278">Mitigation</span><span class="sxs-lookup"><span data-stu-id="3f195-278">Mitigation</span></span>

<span data-ttu-id="3f195-279">Set the **ProcessTerminationThreshold** value between the range **0** and **30000**:</span><span class="sxs-lookup"><span data-stu-id="3f195-279">Set the **ProcessTerminationThreshold** value between the range **0** and **30000**:</span></span>

1. <span data-ttu-id="3f195-280">Sign in to Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="3f195-280">Sign in to Dynamics 365 for Customer Engagement apps.</span></span>
2. <span data-ttu-id="3f195-281">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**</span><span class="sxs-lookup"><span data-stu-id="3f195-281">Go to **Settings** > **[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]** > **Options**</span></span>
3. <span data-ttu-id="3f195-282">In the list of options, select **ProcessTerminationThreshold**.</span><span class="sxs-lookup"><span data-stu-id="3f195-282">In the list of options, select **ProcessTerminationThreshold**.</span></span>
4. <span data-ttu-id="3f195-283">In the **Value** field, type a value between **0** and **30000**.</span><span class="sxs-lookup"><span data-stu-id="3f195-283">In the **Value** field, type a value between **0** and **30000**.</span></span>
5. <span data-ttu-id="3f195-284">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="3f195-284">Select **Save**.</span></span>

[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="3f195-285">[Manage Options for Unified Service Desk](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/manage-options-unified-service-desk)</span><span class="sxs-lookup"><span data-stu-id="3f195-285">[Manage Options for Unified Service Desk](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/admin/manage-options-unified-service-desk)</span></span>

## <a name="see-also"></a><span data-ttu-id="3f195-286">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3f195-286">See also</span></span>

[<span data-ttu-id="3f195-287">Analyze best practices in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="3f195-287">Analyze best practices in Unified Service Desk</span></span>](../admin/analyze-best-practices-unified-service-desk.md)

[<span data-ttu-id="3f195-288">Download and install Best Practices Analyzer</span><span class="sxs-lookup"><span data-stu-id="3f195-288">Download and install Best Practices Analyzer</span></span>](../admin/download-install-best-practices-analyzer.md)

[<span data-ttu-id="3f195-289">Read Best Practices Analyzer report</span><span class="sxs-lookup"><span data-stu-id="3f195-289">Read Best Practices Analyzer report</span></span>](../admin/read-best-practices-analyzer-report.md)

[<span data-ttu-id="3f195-290">Best practice rule categories and parameters</span><span class="sxs-lookup"><span data-stu-id="3f195-290">Best practice rule categories and parameters</span></span>](../admin/compliance-categories-parameters-bpa.md)

[<span data-ttu-id="3f195-291">System configurations</span><span class="sxs-lookup"><span data-stu-id="3f195-291">System configurations</span></span>](../admin/system-configurations-bpa.md)

[<span data-ttu-id="3f195-292">Internet Explorer settings</span><span class="sxs-lookup"><span data-stu-id="3f195-292">Internet Explorer settings</span></span>](../admin/internet-explorer-settings-bpa.md)
