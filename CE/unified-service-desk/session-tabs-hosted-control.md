---
title: Session Tabs (Hosted Control) in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about Session Tabs type of hosted control in Unified Service Desk.
keywords: ''
ms.date: 08/17/2018
ms.service:
- dynamics-365-customerservice
ms.custom:
- dyn365-USD
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 590fe7cf-9281-41ee-ba7e-c0914ef9e44a
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
ms.openlocfilehash: 7c359dc8d0a6124bcf619e912fd89b4e24ac28b3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388736"
---
# <a name="session-tabs-hosted-control"></a><span data-ttu-id="25bc2-103">Session Tabs (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="25bc2-103">Session Tabs (Hosted Control)</span></span>
<span data-ttu-id="25bc2-104">Sử dụng loại **Tab phiên** của kiểm soát tổ chức để hiển thị thông tin khách hàng trong tab phiên trong ứng dụng tổng đài viên của bạn.</span><span class="sxs-lookup"><span data-stu-id="25bc2-104">Use **Session Tabs** type of hosted control to display customer information in a session tab in your agent application.</span></span> <span data-ttu-id="25bc2-105">Kiểm soát tổ chức có thể đọc cấu hình dòng phiên cho cấu hình tên phiên và có thể đánh giá dòng phiên nào nên được sử dụng để tạo tên phiên.</span><span class="sxs-lookup"><span data-stu-id="25bc2-105">The hosted control can read the session lines configuration for the session name configuration, and can evaluate which session line should be used to create the session name.</span></span> <span data-ttu-id="25bc2-106">Một phiên bản của loại kiểm soát tổ chức này phải có sẵn trong ứng dụng tổng đài viên của bạn để hiển thị tab phiên.</span><span class="sxs-lookup"><span data-stu-id="25bc2-106">An instance of this hosted control type must be available in your agent application for the session tabs to be displayed.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="25bc2-107">[Session management in Unified Service Desk](../unified-service-desk/session-management-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="25bc2-107">[Session management in Unified Service Desk](../unified-service-desk/session-management-unified-service-desk.md)</span></span>  
  
<a name="Create"></a>   
## <a name="create-a-session-tab-hosted-control"></a><span data-ttu-id="25bc2-108">Tạo kiểm soát tổ chức tab phiên</span><span class="sxs-lookup"><span data-stu-id="25bc2-108">Create a Session Tab hosted control</span></span>  
 <span data-ttu-id="25bc2-109">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span><span class="sxs-lookup"><span data-stu-id="25bc2-109">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span></span> <span data-ttu-id="25bc2-110">Khi bạn chọn **tab phiên** từ danh sách thả xuống \*\*Loại thành phần USD \*\* trong màn hình **Kiểm soát tổ chức mới**, bạn không phải chọn bất kỳ trường nào khác.</span><span class="sxs-lookup"><span data-stu-id="25bc2-110">When you select **Session Tabs** from the **USD Component Type** drop-down list in the **New Hosted Control** screen, you don’t have to select any other fields.</span></span> <span data-ttu-id="25bc2-111">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="25bc2-111">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span></span>  
  
<a name="Actions"></a>   
## <a name="predefined-uii-actions"></a><span data-ttu-id="25bc2-112">Predefined UII actions</span><span class="sxs-lookup"><span data-stu-id="25bc2-112">Predefined UII actions</span></span>  
 <span data-ttu-id="25bc2-113">These are the predefined actions for this hosted control type.</span><span class="sxs-lookup"><span data-stu-id="25bc2-113">These are the predefined actions for this hosted control type.</span></span>  
  
### <a name="chatagentindicator"></a><span data-ttu-id="25bc2-114">ChatAgentIndicator</span><span class="sxs-lookup"><span data-stu-id="25bc2-114">ChatAgentIndicator</span></span>  
 <span data-ttu-id="25bc2-115">Hành động này được sử dụng để chỉ ra rằng hệ thống đang chờ đợi tổng đài viên thực hiện hành động.</span><span class="sxs-lookup"><span data-stu-id="25bc2-115">This action is used to indicate that the system is waiting for the agent to take action.</span></span> <span data-ttu-id="25bc2-116">Nó cũng sẽ hiển thị thời gian chỉ số tiến độ và đặt lại về 0.</span><span class="sxs-lookup"><span data-stu-id="25bc2-116">It will also show the progress indicator time, and reset to 0.</span></span>  
  
|<span data-ttu-id="25bc2-117">Tham số</span><span class="sxs-lookup"><span data-stu-id="25bc2-117">Parameter</span></span>|<span data-ttu-id="25bc2-118">Mô tả</span><span class="sxs-lookup"><span data-stu-id="25bc2-118">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="25bc2-119">Id phiên</span><span class="sxs-lookup"><span data-stu-id="25bc2-119">SessionId</span></span>|<span data-ttu-id="25bc2-120">Đây là ID của phiên.</span><span class="sxs-lookup"><span data-stu-id="25bc2-120">This is the ID of the session.</span></span> <span data-ttu-id="25bc2-121">ID cũng có thể được lấy từ bối cảnh sử dụng tham số thay thế: [[context.sessionid]]</span><span class="sxs-lookup"><span data-stu-id="25bc2-121">The ID can also be retrieved from the context using the replacement parameter: [[context.sessionid]]</span></span>|  
  
### <a name="chatcustomerindicator"></a><span data-ttu-id="25bc2-122">ChatCustomerIndicator</span><span class="sxs-lookup"><span data-stu-id="25bc2-122">ChatCustomerIndicator</span></span>  
 <span data-ttu-id="25bc2-123">Hành động này được sử dụng để chỉ ra rằng hệ thống đang chờ đợi khách hàng thực hiện hành động.</span><span class="sxs-lookup"><span data-stu-id="25bc2-123">This action is used to indicate that the system is waiting for the customer to take action.</span></span> <span data-ttu-id="25bc2-124">Nó cũng sẽ hiển thị thời gian chỉ số tiến độ và đặt lại về 0.</span><span class="sxs-lookup"><span data-stu-id="25bc2-124">It will also show the progress indicator time and reset to 0.</span></span>  
  
|<span data-ttu-id="25bc2-125">Tham số</span><span class="sxs-lookup"><span data-stu-id="25bc2-125">Parameter</span></span>|<span data-ttu-id="25bc2-126">Mô tả</span><span class="sxs-lookup"><span data-stu-id="25bc2-126">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="25bc2-127">Id phiên</span><span class="sxs-lookup"><span data-stu-id="25bc2-127">SessionId</span></span>|<span data-ttu-id="25bc2-128">Đây là ID của phiên.</span><span class="sxs-lookup"><span data-stu-id="25bc2-128">This is the ID of the session.</span></span> <span data-ttu-id="25bc2-129">ID cũng có thể được lấy từ bối cảnh sử dụng tham số thay thế: [[context.sessionid]]</span><span class="sxs-lookup"><span data-stu-id="25bc2-129">The ID can also be retrieved from the context using the replacement parameter: [[context.sessionid]]</span></span>|  
  
### <a name="closesession"></a><span data-ttu-id="25bc2-130">Đóng phiên</span><span class="sxs-lookup"><span data-stu-id="25bc2-130">CloseSession</span></span>  
 <span data-ttu-id="25bc2-131">Hành động này sẽ đóng một phiên.</span><span class="sxs-lookup"><span data-stu-id="25bc2-131">This action will close a session.</span></span> <span data-ttu-id="25bc2-132">Trước khi đóng phiên, sự kiện **SessionClosing** được bắt đầu, tiếp theo là sự kiện **SessionClosed**.</span><span class="sxs-lookup"><span data-stu-id="25bc2-132">Before the session closes, the **SessionClosing** event is fired, followed by the **SessionClosed** event.</span></span>  
  
|<span data-ttu-id="25bc2-133">Tham số</span><span class="sxs-lookup"><span data-stu-id="25bc2-133">Parameter</span></span>|<span data-ttu-id="25bc2-134">Mô tả</span><span class="sxs-lookup"><span data-stu-id="25bc2-134">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="25bc2-135">Id phiên</span><span class="sxs-lookup"><span data-stu-id="25bc2-135">SessionId</span></span>|<span data-ttu-id="25bc2-136">Đây là ID phiên mà bạn muốn đóng.</span><span class="sxs-lookup"><span data-stu-id="25bc2-136">This is the ID of the session that you want to close.</span></span> <span data-ttu-id="25bc2-137">Bạn nên chỉ định tham số này để đảm bảo rằng phiên làm việc bắt buộc đóng.</span><span class="sxs-lookup"><span data-stu-id="25bc2-137">You should specify this parameter to ensure that the required session is closed.</span></span> <span data-ttu-id="25bc2-138">Nếu tham số này không được cung cấp, hành động này đóng phiên hiện tại.</span><span class="sxs-lookup"><span data-stu-id="25bc2-138">If this parameter is not supplied, this action closes the current session.</span></span>|  
  
### <a name="fireevent"></a><span data-ttu-id="25bc2-139">FireEvent</span><span class="sxs-lookup"><span data-stu-id="25bc2-139">FireEvent</span></span>  
 <span data-ttu-id="25bc2-140">Fires a user-defined event from this hosted control.</span><span class="sxs-lookup"><span data-stu-id="25bc2-140">Fires a user-defined event from this hosted control.</span></span>  
  
|<span data-ttu-id="25bc2-141">Tham số</span><span class="sxs-lookup"><span data-stu-id="25bc2-141">Parameter</span></span>|<span data-ttu-id="25bc2-142">Mô tả</span><span class="sxs-lookup"><span data-stu-id="25bc2-142">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="25bc2-143">tên</span><span class="sxs-lookup"><span data-stu-id="25bc2-143">name</span></span>|<span data-ttu-id="25bc2-144">Tên của sự kiện do người dùng xác định.</span><span class="sxs-lookup"><span data-stu-id="25bc2-144">Name of the user-defined event.</span></span>|  
  
 <span data-ttu-id="25bc2-145">Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này.</span><span class="sxs-lookup"><span data-stu-id="25bc2-145">All subsequent name=value pairs become the parameters to the event.</span></span> <span data-ttu-id="25bc2-146">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span><span class="sxs-lookup"><span data-stu-id="25bc2-146">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span></span>  
  
### <a name="hidechatindicator"></a><span data-ttu-id="25bc2-147">HideChatIndicator</span><span class="sxs-lookup"><span data-stu-id="25bc2-147">HideChatIndicator</span></span>  
 <span data-ttu-id="25bc2-148">Hành động này được sử dụng chỉ để ẩn chỉ số trò chuyện.</span><span class="sxs-lookup"><span data-stu-id="25bc2-148">This action is used to hide the chat indicator.</span></span>  
  
|<span data-ttu-id="25bc2-149">Tham số</span><span class="sxs-lookup"><span data-stu-id="25bc2-149">Parameter</span></span>|<span data-ttu-id="25bc2-150">Mô tả</span><span class="sxs-lookup"><span data-stu-id="25bc2-150">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="25bc2-151">Id phiên</span><span class="sxs-lookup"><span data-stu-id="25bc2-151">SessionId</span></span>|<span data-ttu-id="25bc2-152">Đây là ID của phiên.</span><span class="sxs-lookup"><span data-stu-id="25bc2-152">This is the ID of the session.</span></span> <span data-ttu-id="25bc2-153">The ID can also be retrieved from the context using the replacement parameter: [[context.sessionid]]</span><span class="sxs-lookup"><span data-stu-id="25bc2-153">The ID can also be retrieved from the context using the replacement parameter: [[context.sessionid]]</span></span>|  
  
### <a name="hideprogressindicator"></a><span data-ttu-id="25bc2-154">HideProgressIndicator</span><span class="sxs-lookup"><span data-stu-id="25bc2-154">HideProgressIndicator</span></span>  
 <span data-ttu-id="25bc2-155">Hành động này được sử dụng chỉ để ẩn chỉ số tiến độ.</span><span class="sxs-lookup"><span data-stu-id="25bc2-155">This action is used to hide the progress indicator.</span></span>  
  
|<span data-ttu-id="25bc2-156">Tham số</span><span class="sxs-lookup"><span data-stu-id="25bc2-156">Parameter</span></span>|<span data-ttu-id="25bc2-157">Mô tả</span><span class="sxs-lookup"><span data-stu-id="25bc2-157">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="25bc2-158">Id phiên</span><span class="sxs-lookup"><span data-stu-id="25bc2-158">SessionId</span></span>|<span data-ttu-id="25bc2-159">Đây là ID phiên giao dịch mà bạn muốn ẩn chỉ số tiến độ.</span><span class="sxs-lookup"><span data-stu-id="25bc2-159">This is the ID of the session for which you want to hide the progress indicator.</span></span> <span data-ttu-id="25bc2-160">The ID can also be retrieved from the context using the replacement parameter: [[context.sessionid]]</span><span class="sxs-lookup"><span data-stu-id="25bc2-160">The ID can also be retrieved from the context using the replacement parameter: [[context.sessionid]]</span></span>|  
  
<a name="RealignWindow"></a>   
### <a name="realignwindow"></a><span data-ttu-id="25bc2-161">RealignWindow</span><span class="sxs-lookup"><span data-stu-id="25bc2-161">RealignWindow</span></span>  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]
  
### <a name="resetprogressindicator"></a><span data-ttu-id="25bc2-162">ResetProgressIndicator</span><span class="sxs-lookup"><span data-stu-id="25bc2-162">ResetProgressIndicator</span></span>  
 <span data-ttu-id="25bc2-163">This action is used to reset the progress timer on the session tab. The progress indicator runs for 3 minutes.</span><span class="sxs-lookup"><span data-stu-id="25bc2-163">This action is used to reset the progress timer on the session tab. The progress indicator runs for 3 minutes.</span></span>  
  
|<span data-ttu-id="25bc2-164">Tham số</span><span class="sxs-lookup"><span data-stu-id="25bc2-164">Parameter</span></span>|<span data-ttu-id="25bc2-165">Mô tả</span><span class="sxs-lookup"><span data-stu-id="25bc2-165">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="25bc2-166">Id phiên</span><span class="sxs-lookup"><span data-stu-id="25bc2-166">SessionId</span></span>|<span data-ttu-id="25bc2-167">Đây là ID phiên giao dịch mà bạn muốn đặt lại chỉ số tiến độ.</span><span class="sxs-lookup"><span data-stu-id="25bc2-167">This is the ID of the session for which you want to reset the progress indicator.</span></span> <span data-ttu-id="25bc2-168">The ID can also be retrieved from the context using the replacement parameter: [[context.sessionid]]</span><span class="sxs-lookup"><span data-stu-id="25bc2-168">The ID can also be retrieved from the context using the replacement parameter: [[context.sessionid]]</span></span>|

### <a name="switchsession"></a><span data-ttu-id="25bc2-169">SwitchSession</span><span class="sxs-lookup"><span data-stu-id="25bc2-169">SwitchSession</span></span>  
 <span data-ttu-id="25bc2-170">This action is used to switch the session between the local sessions.</span><span class="sxs-lookup"><span data-stu-id="25bc2-170">This action is used to switch the session between the local sessions.</span></span> <span data-ttu-id="25bc2-171">Also, switch from local to global session.</span><span class="sxs-lookup"><span data-stu-id="25bc2-171">Also, switch from local to global session.</span></span>
  
|<span data-ttu-id="25bc2-172">Tham số</span><span class="sxs-lookup"><span data-stu-id="25bc2-172">Parameter</span></span>|<span data-ttu-id="25bc2-173">Mô tả</span><span class="sxs-lookup"><span data-stu-id="25bc2-173">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="25bc2-174">Id phiên</span><span class="sxs-lookup"><span data-stu-id="25bc2-174">SessionId</span></span>|<span data-ttu-id="25bc2-175">This is the ID of the global or local session.</span><span class="sxs-lookup"><span data-stu-id="25bc2-175">This is the ID of the global or local session.</span></span> <span data-ttu-id="25bc2-176">The global session ID can also be retrieved from the context using the replacement parameter: [[$Session.Global]g]</span><span class="sxs-lookup"><span data-stu-id="25bc2-176">The global session ID can also be retrieved from the context using the replacement parameter: [[$Session.Global]g]</span></span></br><span data-ttu-id="25bc2-177">Ví dụ: `sessionid=[[$Session.Global]g]`</span><span class="sxs-lookup"><span data-stu-id="25bc2-177">For example: `sessionid=[[$Session.Global]g]`</span></span>| 
  
<a name="Events"></a>   
## <a name="predefined-events"></a><span data-ttu-id="25bc2-178">Sự kiện được xác định trước</span><span class="sxs-lookup"><span data-stu-id="25bc2-178">Predefined events</span></span>  
 <span data-ttu-id="25bc2-179">The following predefined events are associated with this hosted control type.</span><span class="sxs-lookup"><span data-stu-id="25bc2-179">The following predefined events are associated with this hosted control type.</span></span> <span data-ttu-id="25bc2-180">Bạn cũng có thể tạo sự kiện do người dùng xác định cho kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="25bc2-180">You can also create user-defined events for a hosted control.</span></span> <span data-ttu-id="25bc2-181">For information, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span><span class="sxs-lookup"><span data-stu-id="25bc2-181">For information, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span></span>  
  
### <a name="sessionclosed"></a><span data-ttu-id="25bc2-182">Đã đóng phiên</span><span class="sxs-lookup"><span data-stu-id="25bc2-182">SessionClosed</span></span>  
 <span data-ttu-id="25bc2-183">Xảy ra sau khi phiên được đóng lại.</span><span class="sxs-lookup"><span data-stu-id="25bc2-183">Occurs after the session is closed.</span></span>  
  
|<span data-ttu-id="25bc2-184">Tham số</span><span class="sxs-lookup"><span data-stu-id="25bc2-184">Parameter</span></span>|<span data-ttu-id="25bc2-185">Mô tả</span><span class="sxs-lookup"><span data-stu-id="25bc2-185">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="25bc2-186">Id phiên</span><span class="sxs-lookup"><span data-stu-id="25bc2-186">SessionId</span></span>|<span data-ttu-id="25bc2-187">Đây là ID phiên đã bị đóng.</span><span class="sxs-lookup"><span data-stu-id="25bc2-187">This is the ID of the session that was closed.</span></span>|  
|<span data-ttu-id="25bc2-188">IsGlobal</span><span class="sxs-lookup"><span data-stu-id="25bc2-188">IsGlobal</span></span>|<span data-ttu-id="25bc2-189">Trong phiên bản **trình quản lý chung** của sự kiện này, cờ IsGlobal cũng được thông qua.</span><span class="sxs-lookup"><span data-stu-id="25bc2-189">In the **Global Manager** version of this event, the IsGlobal flag is also passed.</span></span> <span data-ttu-id="25bc2-190">Nếu phiên chung đã đóng, cờ sẽ **Đúng**, nếu không, **sai**.</span><span class="sxs-lookup"><span data-stu-id="25bc2-190">If the global session is closed, the flag would be **True**, Otherwise, **False**.</span></span>|  
  
### <a name="sessioncloserequested"></a><span data-ttu-id="25bc2-191">SessionCloseRequested</span><span class="sxs-lookup"><span data-stu-id="25bc2-191">SessionCloseRequested</span></span>  
 <span data-ttu-id="25bc2-192">Xảy ra khi "X" được nhấp vào trên một tab phiên làm việc trong các ứng dụng tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="25bc2-192">Occurs when the "X" is clicked on a session tab in the agent application.</span></span> <span data-ttu-id="25bc2-193">Nếu sự kiện này không được xử lý, Hệ thống sẽ tự động đóng phiên.</span><span class="sxs-lookup"><span data-stu-id="25bc2-193">If this event is not handled, the system will automatically close the session.</span></span> <span data-ttu-id="25bc2-194">Nếu sự kiện này được xử lý, Hệ thống sẽ không tự động đóng phiên và bạn phải đính kèm một cuộc gọi hành động cho sự kiện này mà gọi hành động **CloseSession** trên kiểm soát tổ chức **tab phiên** của bạn để đóng phiên một cách rõ ràng.</span><span class="sxs-lookup"><span data-stu-id="25bc2-194">If the event is handled, the system will not automatically close the session, and you must attach an action call to this event that calls the **CloseSession** action on your **Session Tabs** hosted control to explicitly close the session.</span></span>  
  
### <a name="sessionclosing"></a><span data-ttu-id="25bc2-195">Đang đóng phiên</span><span class="sxs-lookup"><span data-stu-id="25bc2-195">SessionClosing</span></span>  
 <span data-ttu-id="25bc2-196">Xảy ra trước khi một phiên đã bị đóng.</span><span class="sxs-lookup"><span data-stu-id="25bc2-196">Occurs  before a session is closed.</span></span>  
  
|<span data-ttu-id="25bc2-197">Tham số</span><span class="sxs-lookup"><span data-stu-id="25bc2-197">Parameter</span></span>|<span data-ttu-id="25bc2-198">Mô tả</span><span class="sxs-lookup"><span data-stu-id="25bc2-198">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="25bc2-199">ID phiên</span><span class="sxs-lookup"><span data-stu-id="25bc2-199">SessionID</span></span>|<span data-ttu-id="25bc2-200">Đây là ID phiên đã bị đóng.</span><span class="sxs-lookup"><span data-stu-id="25bc2-200">This is the ID of the session that is closed.</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="25bc2-201">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="25bc2-201">See also</span></span>  
 <span data-ttu-id="25bc2-202">[Session management in Unified Service Desk](../unified-service-desk/session-management-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="25bc2-202">[Session management in Unified Service Desk](../unified-service-desk/session-management-unified-service-desk.md) </span></span>  
 <span data-ttu-id="25bc2-203">[Session Lines (Hosted Control)](../unified-service-desk/session-lines-hosted-control.md) </span><span class="sxs-lookup"><span data-stu-id="25bc2-203">[Session Lines (Hosted Control)](../unified-service-desk/session-lines-hosted-control.md) </span></span>  
 <span data-ttu-id="25bc2-204">[Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md) </span><span class="sxs-lookup"><span data-stu-id="25bc2-204">[Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md) </span></span>  
 [<span data-ttu-id="25bc2-205">Hosted control types and action/event reference</span><span class="sxs-lookup"><span data-stu-id="25bc2-205">Hosted control types and action/event reference</span></span>](../unified-service-desk/hosted-control-types-action-event-reference.md)   
