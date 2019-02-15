---
title: Agent Scripting (Hosted Control) | MicrosoftDocs
description: Learn about using Agent Scripting type of hosted control to define a call script that provides instructions to the call center agent to guide them during a customer interaction for a given session.
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
ms.assetid: 4d34fda6-6b17-4c94-8881-39962c85e6d0
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
ms.openlocfilehash: 9173e687f848ff12485cd002405c99558842284a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388477"
---
# <a name="agent-scripting-hosted-control"></a><span data-ttu-id="e10cb-103">Agent Scripting (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="e10cb-103">Agent Scripting (Hosted Control)</span></span>
<span data-ttu-id="e10cb-104">Sử dụng loại kiểm soát tổ chức **Mã lệnh tổng đài viên** để xác định mã lệnh cuộc gọi mà cung cấp hướng dẫn cho tổng đài viên trung tâm cuộc gọi để hướng dẫn họ trong suốt quá trình tương tác khách hàng cho phiên nhất định.</span><span class="sxs-lookup"><span data-stu-id="e10cb-104">Use **Agent Scripting** type of hosted control to define a call script that provides instructions to the call center agent to guide them during a customer interaction for a given session.</span></span> <span data-ttu-id="e10cb-105">For more information, see [Guide customer interactions with agent scripts](../unified-service-desk/guide-customer-interactions-agent-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="e10cb-105">For more information, see [Guide customer interactions with agent scripts](../unified-service-desk/guide-customer-interactions-agent-scripts.md).</span></span>  
  
<a name="AgentScripting"></a>   
## <a name="create-an-agent-scripting-hosted-control"></a><span data-ttu-id="e10cb-106">Tạo kiểm soát tổ chức mã lệnh tổng đài viên</span><span class="sxs-lookup"><span data-stu-id="e10cb-106">Create an Agent Scripting hosted control</span></span>  
 <span data-ttu-id="e10cb-107">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span><span class="sxs-lookup"><span data-stu-id="e10cb-107">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span></span> <span data-ttu-id="e10cb-108">Phần này cung cấp thông tin về các trường cụ thể mà là duy nhất cho loại kiểm soát tổ chức **Mã lệnh tổng đài viên**.</span><span class="sxs-lookup"><span data-stu-id="e10cb-108">This section provides information about the specific fields that are unique to the **Agent Scripting** hosted control type.</span></span> <span data-ttu-id="e10cb-109">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="e10cb-109">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span></span>  
  
  <span data-ttu-id="e10cb-110"><!-- Missing graphic below--> <!-- ![Agent scripting hosted control](../unified-service-desk/media/usd-agent-scripthostedcontrol.PNG "Agent scripting hosted control")  --></span><span class="sxs-lookup"><span data-stu-id="e10cb-110"><!-- Missing graphic below--> <!-- ![Agent scripting hosted control](../unified-service-desk/media/usd-agent-scripthostedcontrol.PNG "Agent scripting hosted control")  --></span></span>
  
 <span data-ttu-id="e10cb-111">Trong màn hình **Kiểm soát tổ chức mới**, dưới khu vực **Unified Service Desk**, chọn **Mã lệnh tổng đài viên** từ danh sách thả xuống **Loại Thành phần USD**.</span><span class="sxs-lookup"><span data-stu-id="e10cb-111">In the **New Hosted Control** screen, under the **Unified Service Desk** area, select **Agent Scripting** from the **USD Component Type** drop-down list.</span></span> <span data-ttu-id="e10cb-112">WorkflowPanel là bảng phổ biến nhất cho loại kiểm soát tổ chức này và loại tương tự được hiển thị trong trường **Hiển thị nhóm**.</span><span class="sxs-lookup"><span data-stu-id="e10cb-112">The WorkflowPanel is the most common panel for this hosted control type, and the same is displayed in the **Display Group** field.</span></span> <span data-ttu-id="e10cb-113">For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="e10cb-113">For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md).</span></span> <span data-ttu-id="e10cb-114">For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="e10cb-114">For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span></span>  
  
<a name="actions"></a>   
## <a name="predefined-uii-actions"></a><span data-ttu-id="e10cb-115">Predefined UII actions</span><span class="sxs-lookup"><span data-stu-id="e10cb-115">Predefined UII actions</span></span>  
 <span data-ttu-id="e10cb-116">Hành động sau đây được hỗ trợ cho loại kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="e10cb-116">The following actions are supported for this type of hosted control.</span></span>  
  
### <a name="back"></a><span data-ttu-id="e10cb-117">Back</span><span class="sxs-lookup"><span data-stu-id="e10cb-117">Back</span></span>  
 <span data-ttu-id="e10cb-118">Trở về bước trước trong lịch sử.</span><span class="sxs-lookup"><span data-stu-id="e10cb-118">Return to the previous step in the history.</span></span>  
  
<a name="Close"></a>   
### <a name="close"></a><span data-ttu-id="e10cb-119">Đóng</span><span class="sxs-lookup"><span data-stu-id="e10cb-119">Close</span></span>  
 <span data-ttu-id="e10cb-120">This action is used to close the hosted control.</span><span class="sxs-lookup"><span data-stu-id="e10cb-120">This action is used to close the hosted control.</span></span>  
  
### <a name="fireevent"></a><span data-ttu-id="e10cb-121">FireEvent</span><span class="sxs-lookup"><span data-stu-id="e10cb-121">FireEvent</span></span>  
 <span data-ttu-id="e10cb-122">Khuyến khích sự kiện được người dùng xác định từ loại hình kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="e10cb-122">Fires a user-defined event from this hosted control.</span></span>  
  
|<span data-ttu-id="e10cb-123">Tham số</span><span class="sxs-lookup"><span data-stu-id="e10cb-123">Parameter</span></span>|<span data-ttu-id="e10cb-124">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e10cb-124">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e10cb-125">tên</span><span class="sxs-lookup"><span data-stu-id="e10cb-125">name</span></span>|<span data-ttu-id="e10cb-126">Tên của sự kiện do người dùng xác định.</span><span class="sxs-lookup"><span data-stu-id="e10cb-126">Name of the user-defined event.</span></span>|  
  
 <span data-ttu-id="e10cb-127">Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này.</span><span class="sxs-lookup"><span data-stu-id="e10cb-127">All subsequent name=value pairs become the parameters to the event.</span></span> <span data-ttu-id="e10cb-128">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span><span class="sxs-lookup"><span data-stu-id="e10cb-128">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span></span>  
  
<a name="GoToTask"></a>   
### <a name="gototask"></a><span data-ttu-id="e10cb-129">Đi đến tác vụ</span><span class="sxs-lookup"><span data-stu-id="e10cb-129">GoToTask</span></span>  
 <span data-ttu-id="e10cb-130">Hành động này sẽ hiển thị nhiệm vụ tổng đài viên được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="e10cb-130">This action displays the specified agent task.</span></span> <span data-ttu-id="e10cb-131">The available agent task names can be seen in the **Agent Scripts** section in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps (**Settings** > **Agent Scripts**).</span><span class="sxs-lookup"><span data-stu-id="e10cb-131">The available agent task names can be seen in the **Agent Scripts** section in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps (**Settings** > **Agent Scripts**).</span></span>  
  
|<span data-ttu-id="e10cb-132">Tham số</span><span class="sxs-lookup"><span data-stu-id="e10cb-132">Parameter</span></span>|<span data-ttu-id="e10cb-133">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e10cb-133">Description</span></span>|  
|---------------|-----------------|  
||<span data-ttu-id="e10cb-134">Chỉ định tên của nhiệm vụ tổng đài viên để hiển thị trong trường **dữ liệu**.</span><span class="sxs-lookup"><span data-stu-id="e10cb-134">Specify the name of the agent task to display in the **Data** field.</span></span>|  
  
### <a name="gototaskbycontext"></a><span data-ttu-id="e10cb-135">GoToTaskByContext</span><span class="sxs-lookup"><span data-stu-id="e10cb-135">GoToTaskByContext</span></span>  
 <span data-ttu-id="e10cb-136">Hoạt động này bị phản đối.</span><span class="sxs-lookup"><span data-stu-id="e10cb-136">This action is deprecated.</span></span> <span data-ttu-id="e10cb-137">Sử dụng hoạt động **GoToTask**.</span><span class="sxs-lookup"><span data-stu-id="e10cb-137">Use the **GoToTask** action.</span></span>  
  
### <a name="gototaskbydnis"></a><span data-ttu-id="e10cb-138">GotoTaskByDnis</span><span class="sxs-lookup"><span data-stu-id="e10cb-138">GotoTaskByDnis</span></span>  
 <span data-ttu-id="e10cb-139">Hoạt động này bị phản đối.</span><span class="sxs-lookup"><span data-stu-id="e10cb-139">This action is deprecated.</span></span> <span data-ttu-id="e10cb-140">Sử dụng hoạt động **GoToTask**.</span><span class="sxs-lookup"><span data-stu-id="e10cb-140">Use the **GoToTask** action.</span></span>  
  
<a name="MoveToPanel"></a>   
### <a name="movetopanel"></a><span data-ttu-id="e10cb-141">MoveToPanel</span><span class="sxs-lookup"><span data-stu-id="e10cb-141">MoveToPanel</span></span>  
 <span data-ttu-id="e10cb-142">This action is used to move hosted controls between panels at runtime.</span><span class="sxs-lookup"><span data-stu-id="e10cb-142">This action is used to move hosted controls between panels at runtime.</span></span>  
  
|<span data-ttu-id="e10cb-143">Tham số</span><span class="sxs-lookup"><span data-stu-id="e10cb-143">Parameter</span></span>|<span data-ttu-id="e10cb-144">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e10cb-144">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e10cb-145">ứng dụng</span><span class="sxs-lookup"><span data-stu-id="e10cb-145">app</span></span>|<span data-ttu-id="e10cb-146">Name of the hosted control to be moved.</span><span class="sxs-lookup"><span data-stu-id="e10cb-146">Name of the hosted control to be moved.</span></span>|  
|<span data-ttu-id="e10cb-147">bảng điều khiển</span><span class="sxs-lookup"><span data-stu-id="e10cb-147">panel</span></span>|<span data-ttu-id="e10cb-148">Target panel for the hosted control.</span><span class="sxs-lookup"><span data-stu-id="e10cb-148">Target panel for the hosted control.</span></span>|  
  
### <a name="newcrmpage"></a><span data-ttu-id="e10cb-149">New_CRM_Page</span><span class="sxs-lookup"><span data-stu-id="e10cb-149">New_CRM_Page</span></span>  
 <span data-ttu-id="e10cb-150">Creates a page for creating a new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps record of the entity specified, and treats the page as a popup from the specified hosted control.</span><span class="sxs-lookup"><span data-stu-id="e10cb-150">Creates a page for creating a new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps record of the entity specified, and treats the page as a popup from the specified hosted control.</span></span> <span data-ttu-id="e10cb-151">Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi trang tạo hồ sơ thực thể được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="e10cb-151">The window navigation rules are evaluated to determine the location where the page to create the entity record is displayed.</span></span>  
  
|<span data-ttu-id="e10cb-152">Tham số</span><span class="sxs-lookup"><span data-stu-id="e10cb-152">Parameter</span></span>|<span data-ttu-id="e10cb-153">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e10cb-153">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e10cb-154">LogicalName</span><span class="sxs-lookup"><span data-stu-id="e10cb-154">LogicalName</span></span>|<span data-ttu-id="e10cb-155">Tên logic của thực thể để tạo phiên bản mới.</span><span class="sxs-lookup"><span data-stu-id="e10cb-155">The logical name of the entity for creating a new instance.</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="e10cb-156">Phần còn lại của các tham số nên bao gồm tên = cặp giá trị.</span><span class="sxs-lookup"><span data-stu-id="e10cb-156">The rest of the parameters should consist of name=value pairs.</span></span> <span data-ttu-id="e10cb-157">These are the additional pre-populated values in the form for creating a new record for the specified entity.</span><span class="sxs-lookup"><span data-stu-id="e10cb-157">These are the additional pre-populated values in the form for creating a new record for the specified entity.</span></span> <span data-ttu-id="e10cb-158">For more information about using this action, see step 4 in [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="e10cb-158">For more information about using this action, see step 4 in [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md).</span></span>  
  
### <a name="opencrmpage"></a><span data-ttu-id="e10cb-159">Open_CRM_Page</span><span class="sxs-lookup"><span data-stu-id="e10cb-159">Open_CRM_Page</span></span>  
 <span data-ttu-id="e10cb-160">Opens an existing instance of the entity specified and identified by the ID, and treats the page as a popup from the specified hosted control.</span><span class="sxs-lookup"><span data-stu-id="e10cb-160">Opens an existing instance of the entity specified and identified by the ID, and treats the page as a popup from the specified hosted control.</span></span> <span data-ttu-id="e10cb-161">Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi thư mục bật lên nên sẽ được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="e10cb-161">The window navigation rules are evaluated to determine the location where the popup should be displayed.</span></span>  
  
|<span data-ttu-id="e10cb-162">Tham số</span><span class="sxs-lookup"><span data-stu-id="e10cb-162">Parameter</span></span>|<span data-ttu-id="e10cb-163">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e10cb-163">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e10cb-164">LogicalName</span><span class="sxs-lookup"><span data-stu-id="e10cb-164">LogicalName</span></span>|<span data-ttu-id="e10cb-165">Tên logic của thực thể hợp lý của thực thể để mở.</span><span class="sxs-lookup"><span data-stu-id="e10cb-165">The logical name of the entity to open.</span></span>|  
|<span data-ttu-id="e10cb-166">id</span><span class="sxs-lookup"><span data-stu-id="e10cb-166">id</span></span>|<span data-ttu-id="e10cb-167">ID của hồ sơ thực thể để mở.</span><span class="sxs-lookup"><span data-stu-id="e10cb-167">The ID of the entity record to open.</span></span>|  
  
### <a name="popup"></a><span data-ttu-id="e10cb-168">Bật lên</span><span class="sxs-lookup"><span data-stu-id="e10cb-168">Popup</span></span>  
 <span data-ttu-id="e10cb-169">Bật lên URL từ kiểm soát tổ chức và chạy nguyên tắc điều hướng cửa sổ chống lại hình thức kiểm soát tổ chức để định tuyến bật lên đến vị trí thích hợp.</span><span class="sxs-lookup"><span data-stu-id="e10cb-169">Pops up a URL from the hosted control and runs the window navigation rules against it for routing the popup to the appropriate location.</span></span>  
  
|<span data-ttu-id="e10cb-170">Tham số</span><span class="sxs-lookup"><span data-stu-id="e10cb-170">Parameter</span></span>|<span data-ttu-id="e10cb-171">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e10cb-171">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e10cb-172">url</span><span class="sxs-lookup"><span data-stu-id="e10cb-172">url</span></span>|<span data-ttu-id="e10cb-173">Routes a popup from this hosted control using this URL as if it were a popup requested from the displayed control.</span><span class="sxs-lookup"><span data-stu-id="e10cb-173">Routes a popup from this hosted control using this URL as if it were a popup requested from the displayed control.</span></span>|  
|<span data-ttu-id="e10cb-174">nền tảng</span><span class="sxs-lookup"><span data-stu-id="e10cb-174">frame</span></span>|<span data-ttu-id="e10cb-175">The frame from which this popup originated.</span><span class="sxs-lookup"><span data-stu-id="e10cb-175">The frame from which this popup originated.</span></span>|  
  
<a name="RealignWindow"></a>   
### <a name="realignwindow"></a><span data-ttu-id="e10cb-176">RealignWindow</span><span class="sxs-lookup"><span data-stu-id="e10cb-176">RealignWindow</span></span>  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]
  
<a name="SetSize"></a>   
### <a name="setsize"></a><span data-ttu-id="e10cb-177">SetSize</span><span class="sxs-lookup"><span data-stu-id="e10cb-177">SetSize</span></span>  
 <span data-ttu-id="e10cb-178">This action explicitly sets the width and height of the hosted control.</span><span class="sxs-lookup"><span data-stu-id="e10cb-178">This action explicitly sets the width and height of the hosted control.</span></span> <span data-ttu-id="e10cb-179">Quá trình này đặc biệt hữu ích khi sử dụng tính năng "tự động" trong bố cục bảng điều khiển của bạn.</span><span class="sxs-lookup"><span data-stu-id="e10cb-179">This is particularly useful when using "auto" in your panel layouts.</span></span>  
  
|<span data-ttu-id="e10cb-180">Tham số</span><span class="sxs-lookup"><span data-stu-id="e10cb-180">Parameter</span></span>|<span data-ttu-id="e10cb-181">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e10cb-181">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e10cb-182">chiều rộng</span><span class="sxs-lookup"><span data-stu-id="e10cb-182">width</span></span>|<span data-ttu-id="e10cb-183">The width of the hosted control.</span><span class="sxs-lookup"><span data-stu-id="e10cb-183">The width of the hosted control.</span></span>|  
|<span data-ttu-id="e10cb-184">chiều cao</span><span class="sxs-lookup"><span data-stu-id="e10cb-184">height</span></span>|<span data-ttu-id="e10cb-185">The height of the hosted control.</span><span class="sxs-lookup"><span data-stu-id="e10cb-185">The height of the hosted control.</span></span>|  
  
<a name="ShowSendButton"></a>   
### <a name="showsendbutton"></a><span data-ttu-id="e10cb-186">ShowSendButton</span><span class="sxs-lookup"><span data-stu-id="e10cb-186">ShowSendButton</span></span>  
 <span data-ttu-id="e10cb-187">Hành động này sẽ hiển thị nút **gửi** trên mã lệnh tổng đài viên trong ứng dụng khách.</span><span class="sxs-lookup"><span data-stu-id="e10cb-187">This action displays the **Send** button on the agent script in the client application.</span></span> <span data-ttu-id="e10cb-188">This button is typically used for chat sessions, and when the user clicks the button, the [SendClicked](../unified-service-desk/agent-scripting-hosted-control.md#SendClicked) event is fired, which is used to write the script text to the chat window.</span><span class="sxs-lookup"><span data-stu-id="e10cb-188">This button is typically used for chat sessions, and when the user clicks the button, the [SendClicked](../unified-service-desk/agent-scripting-hosted-control.md#SendClicked) event is fired, which is used to write the script text to the chat window.</span></span>  
  
<a name="events"></a>   
## <a name="predefined-events"></a><span data-ttu-id="e10cb-189">Sự kiện được xác định trước</span><span class="sxs-lookup"><span data-stu-id="e10cb-189">Predefined events</span></span>  
 <span data-ttu-id="e10cb-190">Các sự kiện được xác định trước sau đây được liên kết với loại kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="e10cb-190">The following predefined events are associated with this hosted control type.</span></span>  
  
### <a name="allanswersvisited"></a><span data-ttu-id="e10cb-191">AllAnswersVisited</span><span class="sxs-lookup"><span data-stu-id="e10cb-191">AllAnswersVisited</span></span>  
 <span data-ttu-id="e10cb-192">Xảy ra khi tất cả các câu trả lời cho nhiệm vụ hiện tại đã được nhấp.</span><span class="sxs-lookup"><span data-stu-id="e10cb-192">Occurs when all answers for the current task have been clicked.</span></span> <span data-ttu-id="e10cb-193">Điều này là hữu ích cho danh sách kiểm tra.</span><span class="sxs-lookup"><span data-stu-id="e10cb-193">This is useful for checklists.</span></span> <span data-ttu-id="e10cb-194">Về cơ bản, mỗi câu trả lời được chỉ quay lại cùng một nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="e10cb-194">Basically each answer points back to the same task.</span></span> <span data-ttu-id="e10cb-195">Vì vậy khi bạn nhấp vào nút, chúng sẽ hiển thị các hộp kiểm bên cạnh chúng.</span><span class="sxs-lookup"><span data-stu-id="e10cb-195">So when you click the buttons, they will display check boxes next to them.</span></span> <span data-ttu-id="e10cb-196">Sau khi tất cả được chọn, sự kiện này được bắt đầu.</span><span class="sxs-lookup"><span data-stu-id="e10cb-196">Once all are checked, this event is fired.</span></span>  
  
|<span data-ttu-id="e10cb-197">Tham số</span><span class="sxs-lookup"><span data-stu-id="e10cb-197">Parameter</span></span>|<span data-ttu-id="e10cb-198">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e10cb-198">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e10cb-199">nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="e10cb-199">task</span></span>|<span data-ttu-id="e10cb-200">Tên nhiệm vụ mà khi tất cả các câu trả lời đã được nhấp.</span><span class="sxs-lookup"><span data-stu-id="e10cb-200">Name of the task for which all the answers have been clicked.</span></span>|  
|<span data-ttu-id="e10cb-201">id</span><span class="sxs-lookup"><span data-stu-id="e10cb-201">id</span></span>|<span data-ttu-id="e10cb-202">ID của nhiệm vụ mà khi tất cả các câu trả lời đã được nhấp.</span><span class="sxs-lookup"><span data-stu-id="e10cb-202">ID of the task for which all the answers have been clicked.</span></span>|  
  
<a name="SendClicked"></a>   
### <a name="sendclicked"></a><span data-ttu-id="e10cb-203">SendClicked</span><span class="sxs-lookup"><span data-stu-id="e10cb-203">SendClicked</span></span>  
 <span data-ttu-id="e10cb-204">Xảy ra khi nút **gửi** trên mã lệnh tổng đài viên trong ứng dụng khách được nhấp.</span><span class="sxs-lookup"><span data-stu-id="e10cb-204">Occurs when the **Send** button on the agent script in the client application is clicked.</span></span> <span data-ttu-id="e10cb-205">To display the **Send** Button, you should call the [ShowSendButton](../unified-service-desk/agent-scripting-hosted-control.md#ShowSendButton) action.</span><span class="sxs-lookup"><span data-stu-id="e10cb-205">To display the **Send** Button, you should call the [ShowSendButton](../unified-service-desk/agent-scripting-hosted-control.md#ShowSendButton) action.</span></span>  
  
### <a name="taskupdated"></a><span data-ttu-id="e10cb-206">TaskUpdated</span><span class="sxs-lookup"><span data-stu-id="e10cb-206">TaskUpdated</span></span>  
 <span data-ttu-id="e10cb-207">Xảy ra mỗi khi mã lệnh tổng đài viên được đạt tới, cho dù do người dùng nhấp vào một câu trả lời, hoặc bởi một số thành phần gọi một trong những hành động trên kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="e10cb-207">Occurs each time an agent script is reached, whether by the user clicking an answer, or by some component calling one of the actions on this hosted control.</span></span>  
  
|<span data-ttu-id="e10cb-208">Tham số</span><span class="sxs-lookup"><span data-stu-id="e10cb-208">Parameter</span></span>|<span data-ttu-id="e10cb-209">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e10cb-209">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e10cb-210">nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="e10cb-210">task</span></span>|<span data-ttu-id="e10cb-211">Tên của nhiệm vụ mã lệnh tổng đài viên mà đã đạt được.</span><span class="sxs-lookup"><span data-stu-id="e10cb-211">Name of the agent script task that was reached.</span></span> <span data-ttu-id="e10cb-212">Với menu chính, mà không phải là một nhiệm vụ được liệt kê trong cấu hình của mã lệnh tổng đài viên, một sự kiện được bắt đầu bằng tham số này được thành "[Menu chính]".</span><span class="sxs-lookup"><span data-stu-id="e10cb-212">For the main menu, which isn't a listed task in the configuration of agent scripts, an event is fired with this parameter set to "[Main Menu]".</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="e10cb-213">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e10cb-213">See also</span></span>  
 <span data-ttu-id="e10cb-214">[Guide customer interactions with agent scripts](../unified-service-desk/guide-customer-interactions-agent-scripts.md) </span><span class="sxs-lookup"><span data-stu-id="e10cb-214">[Guide customer interactions with agent scripts](../unified-service-desk/guide-customer-interactions-agent-scripts.md) </span></span>  
 <span data-ttu-id="e10cb-215">[Cấu hình và quản lý mã lệnh tổng đài viên](../unified-service-desk/configure-manage-agent-scripts.md) </span><span class="sxs-lookup"><span data-stu-id="e10cb-215">[Configure and manage agent scripts](../unified-service-desk/configure-manage-agent-scripts.md) </span></span>  
 <span data-ttu-id="e10cb-216">[Hành động UII](../unified-service-desk/uii-actions.md) </span><span class="sxs-lookup"><span data-stu-id="e10cb-216">[UII actions](../unified-service-desk/uii-actions.md) </span></span>  
 <span data-ttu-id="e10cb-217">[Sự kiện](../unified-service-desk/events.md) </span><span class="sxs-lookup"><span data-stu-id="e10cb-217">[Events](../unified-service-desk/events.md) </span></span>  
 <span data-ttu-id="e10cb-218">[View predefined actions and events for a hosted control](../unified-service-desk/view-predefined-actions-events-hosted-control.md) </span><span class="sxs-lookup"><span data-stu-id="e10cb-218">[View predefined actions and events for a hosted control](../unified-service-desk/view-predefined-actions-events-hosted-control.md) </span></span>  
 <span data-ttu-id="e10cb-219">[View embedded help for actions and events](../unified-service-desk/view-embedded-help-for-actions-and-events.md) </span><span class="sxs-lookup"><span data-stu-id="e10cb-219">[View embedded help for actions and events](../unified-service-desk/view-embedded-help-for-actions-and-events.md) </span></span>  
 <span data-ttu-id="e10cb-220">[Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="e10cb-220">[Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md) </span></span>  
 <span data-ttu-id="e10cb-221">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md) </span><span class="sxs-lookup"><span data-stu-id="e10cb-221">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md) </span></span>  
 [<span data-ttu-id="e10cb-222">Administration Guide for Unified Service Desk for Microsoft Dynamics CRM</span><span class="sxs-lookup"><span data-stu-id="e10cb-222">Administration Guide for Unified Service Desk for Microsoft Dynamics CRM</span></span>](http://go.microsoft.com/fwlink/p/?LinkID=394402)
