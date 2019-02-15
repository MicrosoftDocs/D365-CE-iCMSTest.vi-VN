---
title: Debugger (Hosted Control) | MicrosoftDocs
description: Learn about using Debugger hosted control type in Unified Service Desk to configure a debugger control in Unified Service Desk to provide you with insights about the process and code executions in the agent application.
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
ms.assetid: 227bba2c-87d2-489c-b91b-5fad0d3c1042
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
ms.openlocfilehash: fedc54aca5c6111ff9fe81dbff569635c736b974
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387683"
---
# <a name="debugger-hosted-control"></a><span data-ttu-id="46cd4-103">Debugger (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="46cd4-103">Debugger (Hosted Control)</span></span>
<span data-ttu-id="46cd4-104">Sử dụng loại kiểm soát tổ chức **trình gỡ lỗi** trong Unified Service Desk để cấu hình kiểm soát trình gỡ lỗi trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để cung cấp cho bạn những hiểu biết về các quá trình và thực hiện mã trong ứng dụng tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="46cd4-104">Use **Debugger** hosted control type in Unified Service Desk to configure a debugger control in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to provide you with insights about the process and code executions in the agent application.</span></span> <span data-ttu-id="46cd4-105">Tất cả ba mẫu ứng dụng trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] đi kèm với kiểm soát tổ chức trình gỡ lỗi cấu hình sẵn.</span><span class="sxs-lookup"><span data-stu-id="46cd4-105">All the three sample applications in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] come with a preconfigured Debugger hosted control.</span></span> <span data-ttu-id="46cd4-106">For more information, see [Debug issues in Unified Service Desk](http://go.microsoft.com/fwlink/p/?LinkId=518149) in the Unified Service Desk Administration Guide.</span><span class="sxs-lookup"><span data-stu-id="46cd4-106">For more information, see [Debug issues in Unified Service Desk](http://go.microsoft.com/fwlink/p/?LinkId=518149) in the Unified Service Desk Administration Guide.</span></span>  
  
<a name="Create"></a>   
## <a name="create-a-debugger-hosted-control"></a><span data-ttu-id="46cd4-107">Tạo kiểm soát tổ chức trình gỡ lỗi</span><span class="sxs-lookup"><span data-stu-id="46cd4-107">Create a Debugger hosted control</span></span>  
 <span data-ttu-id="46cd4-108">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span><span class="sxs-lookup"><span data-stu-id="46cd4-108">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span></span> <span data-ttu-id="46cd4-109">Phần này cung cấp thông tin về các trường cụ thể mà là duy nhất cho loại kiểm soát tổ chức **Trình gỡ lỗi**.</span><span class="sxs-lookup"><span data-stu-id="46cd4-109">This section provides information about the specific fields that are unique to the **Debugger** hosted control type.</span></span> <span data-ttu-id="46cd4-110">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="46cd4-110">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span></span>  
  
 <span data-ttu-id="46cd4-111">![Debugger hosted control](../unified-service-desk/media/crm-itpro-usd-debuggerhostedcontrol.PNG "Debugger hosted control")</span><span class="sxs-lookup"><span data-stu-id="46cd4-111">![Debugger hosted control](../unified-service-desk/media/crm-itpro-usd-debuggerhostedcontrol.PNG "Debugger hosted control")</span></span>  
  
 <span data-ttu-id="46cd4-112">In the **New Hosted Control** screen:</span><span class="sxs-lookup"><span data-stu-id="46cd4-112">In the **New Hosted Control** screen:</span></span>  
  
- <span data-ttu-id="46cd4-113">Trong vùng **Unified Service Desk**, chọn **Trình gỡ lỗi** từ danh sách thả xuống **Loại Thành phần USD**.</span><span class="sxs-lookup"><span data-stu-id="46cd4-113">Under **Unified Service Desk** area, select **Debugger** from the **USD Component Type** drop-down list.</span></span>  
  
- <span data-ttu-id="46cd4-114">Trường **Hiển thị nhóm** hiển thị bảng điều khiển nơi hiển thị kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="46cd4-114">The **Display Group** field displays the panel where this hosted control will be displayed.</span></span> <span data-ttu-id="46cd4-115">**MainPanel** is the most common for this hosted control type.</span><span class="sxs-lookup"><span data-stu-id="46cd4-115">**MainPanel** is the most common for this hosted control type.</span></span> <span data-ttu-id="46cd4-116">For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="46cd4-116">For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md).</span></span> <span data-ttu-id="46cd4-117">For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="46cd4-117">For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span></span>  
  
<a name="actions"></a>   
## <a name="predefined-uii-actions"></a><span data-ttu-id="46cd4-118">Predefined UII actions</span><span class="sxs-lookup"><span data-stu-id="46cd4-118">Predefined UII actions</span></span>  
 <span data-ttu-id="46cd4-119">These are the predefined actions for this hosted control type.</span><span class="sxs-lookup"><span data-stu-id="46cd4-119">These are the predefined actions for this hosted control type.</span></span>  
  
<a name="Close"></a>   
### <a name="close"></a><span data-ttu-id="46cd4-120">Đóng</span><span class="sxs-lookup"><span data-stu-id="46cd4-120">Close</span></span>  
 <span data-ttu-id="46cd4-121">This action is used to close the hosted control.</span><span class="sxs-lookup"><span data-stu-id="46cd4-121">This action is used to close the hosted control.</span></span>  
  
### <a name="fireevent"></a><span data-ttu-id="46cd4-122">FireEvent</span><span class="sxs-lookup"><span data-stu-id="46cd4-122">FireEvent</span></span>  
 <span data-ttu-id="46cd4-123">Khuyến khích sự kiện được người dùng xác định từ loại hình kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="46cd4-123">Fires a user-defined event from this hosted control.</span></span>  
  
|<span data-ttu-id="46cd4-124">Tham số</span><span class="sxs-lookup"><span data-stu-id="46cd4-124">Parameter</span></span>|<span data-ttu-id="46cd4-125">Mô tả</span><span class="sxs-lookup"><span data-stu-id="46cd4-125">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="46cd4-126">tên</span><span class="sxs-lookup"><span data-stu-id="46cd4-126">name</span></span>|<span data-ttu-id="46cd4-127">Tên của sự kiện do người dùng xác định.</span><span class="sxs-lookup"><span data-stu-id="46cd4-127">Name of the user-defined event.</span></span>|  
  
 <span data-ttu-id="46cd4-128">Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này.</span><span class="sxs-lookup"><span data-stu-id="46cd4-128">All subsequent name=value pairs become the parameters to the event.</span></span> <span data-ttu-id="46cd4-129">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span><span class="sxs-lookup"><span data-stu-id="46cd4-129">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span></span>  
  
<a name="MoveToPanel"></a>   
### <a name="movetopanel"></a><span data-ttu-id="46cd4-130">MoveToPanel</span><span class="sxs-lookup"><span data-stu-id="46cd4-130">MoveToPanel</span></span>  
 <span data-ttu-id="46cd4-131">This action is used to move hosted controls between panels at runtime.</span><span class="sxs-lookup"><span data-stu-id="46cd4-131">This action is used to move hosted controls between panels at runtime.</span></span>  
  
|<span data-ttu-id="46cd4-132">Tham số</span><span class="sxs-lookup"><span data-stu-id="46cd4-132">Parameter</span></span>|<span data-ttu-id="46cd4-133">Mô tả</span><span class="sxs-lookup"><span data-stu-id="46cd4-133">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="46cd4-134">ứng dụng</span><span class="sxs-lookup"><span data-stu-id="46cd4-134">app</span></span>|<span data-ttu-id="46cd4-135">Name of the hosted control to be moved.</span><span class="sxs-lookup"><span data-stu-id="46cd4-135">Name of the hosted control to be moved.</span></span>|  
|<span data-ttu-id="46cd4-136">bảng điều khiển</span><span class="sxs-lookup"><span data-stu-id="46cd4-136">panel</span></span>|<span data-ttu-id="46cd4-137">Target panel for the hosted control.</span><span class="sxs-lookup"><span data-stu-id="46cd4-137">Target panel for the hosted control.</span></span>|  
  
### <a name="newcrmpage"></a><span data-ttu-id="46cd4-138">New_CRM_Page</span><span class="sxs-lookup"><span data-stu-id="46cd4-138">New_CRM_Page</span></span>  
 <span data-ttu-id="46cd4-139">Creates a page for creating a new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps record of the entity specified, and treats the page as a popup from the specified hosted control.</span><span class="sxs-lookup"><span data-stu-id="46cd4-139">Creates a page for creating a new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps record of the entity specified, and treats the page as a popup from the specified hosted control.</span></span> <span data-ttu-id="46cd4-140">Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi trang tạo hồ sơ thực thể được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="46cd4-140">The window navigation rules are evaluated to determine the location where the page to create the entity record is displayed.</span></span>  
  
|<span data-ttu-id="46cd4-141">Tham số</span><span class="sxs-lookup"><span data-stu-id="46cd4-141">Parameter</span></span>|<span data-ttu-id="46cd4-142">Mô tả</span><span class="sxs-lookup"><span data-stu-id="46cd4-142">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="46cd4-143">LogicalName</span><span class="sxs-lookup"><span data-stu-id="46cd4-143">LogicalName</span></span>|<span data-ttu-id="46cd4-144">Tên logic của thực thể để tạo phiên bản mới.</span><span class="sxs-lookup"><span data-stu-id="46cd4-144">The logical name of the entity for creating a new instance.</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="46cd4-145">Phần còn lại của các tham số nên bao gồm tên = cặp giá trị.</span><span class="sxs-lookup"><span data-stu-id="46cd4-145">The rest of the parameters should consist of name=value pairs.</span></span> <span data-ttu-id="46cd4-146">These are the additional pre-populated values in the form for creating a new record for the specified entity.</span><span class="sxs-lookup"><span data-stu-id="46cd4-146">These are the additional pre-populated values in the form for creating a new record for the specified entity.</span></span> <span data-ttu-id="46cd4-147">For more information about using this action, see step 4 in [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="46cd4-147">For more information about using this action, see step 4 in [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md).</span></span>  
  
### <a name="opencrmpage"></a><span data-ttu-id="46cd4-148">Open_CRM_Page</span><span class="sxs-lookup"><span data-stu-id="46cd4-148">Open_CRM_Page</span></span>  
 <span data-ttu-id="46cd4-149">Opens an existing instance of the entity specified and identified by the ID, and treats the page as a popup from the specified hosted control.</span><span class="sxs-lookup"><span data-stu-id="46cd4-149">Opens an existing instance of the entity specified and identified by the ID, and treats the page as a popup from the specified hosted control.</span></span> <span data-ttu-id="46cd4-150">Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi thư mục bật lên nên sẽ được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="46cd4-150">The window navigation rules are evaluated to determine the location where the popup should be displayed.</span></span>  
  
|<span data-ttu-id="46cd4-151">Tham số</span><span class="sxs-lookup"><span data-stu-id="46cd4-151">Parameter</span></span>|<span data-ttu-id="46cd4-152">Mô tả</span><span class="sxs-lookup"><span data-stu-id="46cd4-152">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="46cd4-153">LogicalName</span><span class="sxs-lookup"><span data-stu-id="46cd4-153">LogicalName</span></span>|<span data-ttu-id="46cd4-154">Tên logic của thực thể hợp lý của thực thể để mở.</span><span class="sxs-lookup"><span data-stu-id="46cd4-154">The logical name of the entity to open.</span></span>|  
|<span data-ttu-id="46cd4-155">id</span><span class="sxs-lookup"><span data-stu-id="46cd4-155">id</span></span>|<span data-ttu-id="46cd4-156">ID của hồ sơ thực thể để mở.</span><span class="sxs-lookup"><span data-stu-id="46cd4-156">The ID of the entity record to open.</span></span>|  
  
### <a name="popup"></a><span data-ttu-id="46cd4-157">Bật lên</span><span class="sxs-lookup"><span data-stu-id="46cd4-157">Popup</span></span>  
 <span data-ttu-id="46cd4-158">Bật lên URL từ kiểm soát tổ chức và chạy nguyên tắc điều hướng cửa sổ chống lại hình thức kiểm soát tổ chức để định tuyến bật lên đến vị trí thích hợp.</span><span class="sxs-lookup"><span data-stu-id="46cd4-158">Pops up a URL from the hosted control and runs the window navigation rules against it for routing the popup to the appropriate location.</span></span>  
  
|<span data-ttu-id="46cd4-159">Tham số</span><span class="sxs-lookup"><span data-stu-id="46cd4-159">Parameter</span></span>|<span data-ttu-id="46cd4-160">Mô tả</span><span class="sxs-lookup"><span data-stu-id="46cd4-160">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="46cd4-161">url</span><span class="sxs-lookup"><span data-stu-id="46cd4-161">url</span></span>|<span data-ttu-id="46cd4-162">Routes a popup from this hosted control using this URL as if it were a popup requested from the displayed control.</span><span class="sxs-lookup"><span data-stu-id="46cd4-162">Routes a popup from this hosted control using this URL as if it were a popup requested from the displayed control.</span></span>|  
|<span data-ttu-id="46cd4-163">nền tảng</span><span class="sxs-lookup"><span data-stu-id="46cd4-163">frame</span></span>|<span data-ttu-id="46cd4-164">The frame from which this popup originated.</span><span class="sxs-lookup"><span data-stu-id="46cd4-164">The frame from which this popup originated.</span></span>|  
  
<a name="RealignWindow"></a>   
### <a name="realignwindow"></a><span data-ttu-id="46cd4-165">RealignWindow</span><span class="sxs-lookup"><span data-stu-id="46cd4-165">RealignWindow</span></span>  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]
  
<a name="SetSize"></a>   
### <a name="setsize"></a><span data-ttu-id="46cd4-166">SetSize</span><span class="sxs-lookup"><span data-stu-id="46cd4-166">SetSize</span></span>  
 <span data-ttu-id="46cd4-167">This action explicitly sets the width and height of the hosted control.</span><span class="sxs-lookup"><span data-stu-id="46cd4-167">This action explicitly sets the width and height of the hosted control.</span></span> <span data-ttu-id="46cd4-168">Quá trình này đặc biệt hữu ích khi sử dụng tính năng "tự động" trong bố cục bảng điều khiển của bạn.</span><span class="sxs-lookup"><span data-stu-id="46cd4-168">This is particularly useful when using "auto" in your panel layouts.</span></span>  
  
|<span data-ttu-id="46cd4-169">Tham số</span><span class="sxs-lookup"><span data-stu-id="46cd4-169">Parameter</span></span>|<span data-ttu-id="46cd4-170">Mô tả</span><span class="sxs-lookup"><span data-stu-id="46cd4-170">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="46cd4-171">chiều rộng</span><span class="sxs-lookup"><span data-stu-id="46cd4-171">width</span></span>|<span data-ttu-id="46cd4-172">The width of the hosted control.</span><span class="sxs-lookup"><span data-stu-id="46cd4-172">The width of the hosted control.</span></span>|  
|<span data-ttu-id="46cd4-173">chiều cao</span><span class="sxs-lookup"><span data-stu-id="46cd4-173">height</span></span>|<span data-ttu-id="46cd4-174">The height of the hosted control.</span><span class="sxs-lookup"><span data-stu-id="46cd4-174">The height of the hosted control.</span></span>|  
  
### <a name="setreplacementparameter"></a><span data-ttu-id="46cd4-175">Đặt Thông số thay thế</span><span class="sxs-lookup"><span data-stu-id="46cd4-175">SetReplacementParameter</span></span>  
 <span data-ttu-id="46cd4-176">Thiết lập giá trị tham số tùy ý thay thế thành giá trị được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="46cd4-176">Sets an arbitrary replacement parameter value to a specified value.</span></span>  
  
|<span data-ttu-id="46cd4-177">Tham số</span><span class="sxs-lookup"><span data-stu-id="46cd4-177">Parameter</span></span>|<span data-ttu-id="46cd4-178">Mô tả</span><span class="sxs-lookup"><span data-stu-id="46cd4-178">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="46cd4-179">appname</span><span class="sxs-lookup"><span data-stu-id="46cd4-179">appname</span></span>|<span data-ttu-id="46cd4-180">Tên tổ chức kiểm soát hoặc trường quan trọng cho các tham số thay thế.</span><span class="sxs-lookup"><span data-stu-id="46cd4-180">The hosted control name or key field for the replacement parameter.</span></span>|  
|<span data-ttu-id="46cd4-181">tham số</span><span class="sxs-lookup"><span data-stu-id="46cd4-181">param</span></span>|<span data-ttu-id="46cd4-182">Tên chính phụ tham số thay thế.</span><span class="sxs-lookup"><span data-stu-id="46cd4-182">The replacement parameter sub key name.</span></span>|  
|<span data-ttu-id="46cd4-183">giá trị</span><span class="sxs-lookup"><span data-stu-id="46cd4-183">value</span></span>|<span data-ttu-id="46cd4-184">Giá trị để đặt.</span><span class="sxs-lookup"><span data-stu-id="46cd4-184">The value to set.</span></span>|  
|<span data-ttu-id="46cd4-185">chung</span><span class="sxs-lookup"><span data-stu-id="46cd4-185">global</span></span>|<span data-ttu-id="46cd4-186">Đặt giá trị này thành **đúng** để đặt giá trị trong phiên giao dịch chung.</span><span class="sxs-lookup"><span data-stu-id="46cd4-186">Set this to **true** to set the value in the global session.</span></span><br /><br /> <span data-ttu-id="46cd4-187">Đặt giá trị này thành **sai** để đặt giá trị trong phiên hiện hoạt.</span><span class="sxs-lookup"><span data-stu-id="46cd4-187">Set this to **false** to set the value in the active session.</span></span>|  
  
### <a name="testscriptlet"></a><span data-ttu-id="46cd4-188">TestScriptlet</span><span class="sxs-lookup"><span data-stu-id="46cd4-188">TestScriptlet</span></span>  
 <span data-ttu-id="46cd4-189">Chạy JavaScript được chỉ định như thể nó là một scriptlet.</span><span class="sxs-lookup"><span data-stu-id="46cd4-189">Runs the specified JavaScript as if it were a scriptlet.</span></span> <span data-ttu-id="46cd4-190">Khi thực hiện thành công, kết quả hiển thị trong một hộp thư.</span><span class="sxs-lookup"><span data-stu-id="46cd4-190">Upon successful execution, the result is displayed in a message box.</span></span>  
  
<a name="events"></a>   
## <a name="predefined-events"></a><span data-ttu-id="46cd4-191">Sự kiện được xác định trước</span><span class="sxs-lookup"><span data-stu-id="46cd4-191">Predefined events</span></span>  
 <span data-ttu-id="46cd4-192">There aren’t any predefined events available for this hosted control type.</span><span class="sxs-lookup"><span data-stu-id="46cd4-192">There aren’t any predefined events available for this hosted control type.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="46cd4-193">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="46cd4-193">See also</span></span>  
 <span data-ttu-id="46cd4-194">[Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="46cd4-194">[Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md) </span></span>  
 <span data-ttu-id="46cd4-195">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md) </span><span class="sxs-lookup"><span data-stu-id="46cd4-195">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md) </span></span>  
 [<span data-ttu-id="46cd4-196">Administration Guide for Unified Service Desk for Microsoft Dynamics CRM</span><span class="sxs-lookup"><span data-stu-id="46cd4-196">Administration Guide for Unified Service Desk for Microsoft Dynamics CRM</span></span>](http://go.microsoft.com/fwlink/p/?LinkID=394402)
