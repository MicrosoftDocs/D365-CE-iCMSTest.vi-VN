---
title: CRM Dialog (Hosted Control) | MicrosoftDocs
description: Learn about using the CRM Dialog hosted control type to work with Dynamics 365 for Customer Engagement apps dialog. You can call the StartDialog action on your CRM Dialog hosted control to start a Dynamics 365 for Customer Engagement apps dialog within Unified Service Desk.
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
ms.assetid: b500941a-1b20-4c0e-b51e-511aeb07e52d
caps.latest.revision: 8
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 3c350e34eb402863026707dc002c1d57158bbc9d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388479"
---
# <a name="crm-dialog-hosted-control"></a><span data-ttu-id="70a21-104">CRM Dialog (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="70a21-104">CRM Dialog (Hosted Control)</span></span>
<span data-ttu-id="70a21-105">Use the **CRM Dialog** hosted control type to work with Dynamics 365 for Customer Engagement apps dialog.</span><span class="sxs-lookup"><span data-stu-id="70a21-105">Use the **CRM Dialog** hosted control type to work with Dynamics 365 for Customer Engagement apps dialog.</span></span> <span data-ttu-id="70a21-106">You can call the **StartDialog** action on your CRM Dialog hosted control to start a Dynamics 365 for Customer Engagement apps dialog within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="70a21-106">You can call the **StartDialog** action on your CRM Dialog hosted control to start a Dynamics 365 for Customer Engagement apps dialog within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  

<a name="Create"></a>   
## <a name="create-a-crm-dialog-hosted-control"></a><span data-ttu-id="70a21-107">Tạo kiểm soát tổ chức hộp thoại CRM</span><span class="sxs-lookup"><span data-stu-id="70a21-107">Create a CRM Dialog hosted control</span></span>  
 <span data-ttu-id="70a21-108">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span><span class="sxs-lookup"><span data-stu-id="70a21-108">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span></span> <span data-ttu-id="70a21-109">Phần này cung cấp thông tin về các trường cụ thể mà là duy nhất cho loại kiểm soát tổ chức **Hộp thoại CRM**.</span><span class="sxs-lookup"><span data-stu-id="70a21-109">This section provides information about the specific fields that are unique to the **CRM Dialog** hosted control type.</span></span> <span data-ttu-id="70a21-110">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="70a21-110">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span></span>  

 <span data-ttu-id="70a21-111">![Dynamics 365 for Customer Engagement dialog hosted control](../unified-service-desk/media/crm-itpro-usd-crmdialoghostedcontrol.PNG "Dynamics 365 for Customer Engagement apps dialog hosted control")</span><span class="sxs-lookup"><span data-stu-id="70a21-111">![Dynamics 365 for Customer Engagement dialog hosted control](../unified-service-desk/media/crm-itpro-usd-crmdialoghostedcontrol.PNG "Dynamics 365 for Customer Engagement apps dialog hosted control")</span></span>  

 <span data-ttu-id="70a21-112">In the **New Hosted Control** screen:</span><span class="sxs-lookup"><span data-stu-id="70a21-112">In the **New Hosted Control** screen:</span></span>  

- <span data-ttu-id="70a21-113">Trong vùng **Unified Service Desk**, chọn **Hộp thoại CRM** từ danh sách thả xuống **Loại Thành phần USD**.</span><span class="sxs-lookup"><span data-stu-id="70a21-113">Under **Unified Service Desk** area, select **CRM Dialog** from the **USD Component Type** drop-down list.</span></span>  

- <span data-ttu-id="70a21-114">Danh sách thả xuống **Loại tổ chức** xác định cách bạn muốn kiểm soát này được tổ chức.</span><span class="sxs-lookup"><span data-stu-id="70a21-114">The **Hosting Type** drop-down list specifies how you want this control to be hosted.</span></span> <span data-ttu-id="70a21-115">Bạn có thể chọn **WPF nội bộ** (mặc định) hoặc **Xử lý IE**.</span><span class="sxs-lookup"><span data-stu-id="70a21-115">You can choose **Internal WPF** (default) or **IE Process**.</span></span> <span data-ttu-id="70a21-116">For more information, see [Select a hosting method for hosted controls](../unified-service-desk/select-hosting-method-controls.md).</span><span class="sxs-lookup"><span data-stu-id="70a21-116">For more information, see [Select a hosting method for hosted controls](../unified-service-desk/select-hosting-method-controls.md).</span></span>  

- <span data-ttu-id="70a21-117">Under the **Common Properties** area, select the **Application is Global** check box to set the hosted control as global.</span><span class="sxs-lookup"><span data-stu-id="70a21-117">Under the **Common Properties** area, select the **Application is Global** check box to set the hosted control as global.</span></span> <span data-ttu-id="70a21-118">Kiểm soát tổ chức chung có thể được hiển thị bên ngoài phiên khách hàng.</span><span class="sxs-lookup"><span data-stu-id="70a21-118">Global hosted controls can be displayed outside of a customer session.</span></span> <span data-ttu-id="70a21-119">Kiểm soát giống như bảng thông tin của tổng đài viên, tường hoặc tìm kiếm là những hình thức sử dụng chung cho kiểm soát tổ chức chung.</span><span class="sxs-lookup"><span data-stu-id="70a21-119">Controls like the agents’ dashboard, wall or search are common uses for global hosted controls.</span></span> <span data-ttu-id="70a21-120">Kiểm soát tổ chức chung không có trạng thái phiên dành riêng cho phiên để khi bạn thay đổi phiên, các kiểm soát tổ chức chung tương tự vẫn được duy trì.</span><span class="sxs-lookup"><span data-stu-id="70a21-120">Global hosted controls do not have do not have session-specific state so when you change sessions, these same global hosted controls remain.</span></span> <span data-ttu-id="70a21-121">Nếu hộp kiểm không được chọn, kiểm soát tổ chức trở thành kiểu dựa trên phiên.</span><span class="sxs-lookup"><span data-stu-id="70a21-121">If the check box is not selected, the hosted control becomes session based.</span></span> <span data-ttu-id="70a21-122">Kiểm soát dựa trên phiên tồn tại trong ngữ cảnh của phiên khách hàng.</span><span class="sxs-lookup"><span data-stu-id="70a21-122">Session-based controls exist in the context of the customer session.</span></span> <span data-ttu-id="70a21-123">Nếu người dùng thay đổi sang một phiên khác, tất cả các trang phiên từ phiên trước đó được ẩn.</span><span class="sxs-lookup"><span data-stu-id="70a21-123">If the user changes to another session, all the session pages from the previous session are hidden.</span></span>  

- <span data-ttu-id="70a21-124">Trường **Hiển thị nhóm** hiển thị bảng điều khiển nơi hiển thị kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="70a21-124">The **Display Group** field displays the panel where this hosted control will be displayed.</span></span> <span data-ttu-id="70a21-125">**MainPanel** is the most common for this hosted control type.</span><span class="sxs-lookup"><span data-stu-id="70a21-125">**MainPanel** is the most common for this hosted control type.</span></span> <span data-ttu-id="70a21-126">For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md#Panels).</span><span class="sxs-lookup"><span data-stu-id="70a21-126">For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md#Panels).</span></span> <span data-ttu-id="70a21-127">For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="70a21-127">For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span></span>  

<a name="actions"></a>   
## <a name="predefined-uii-actions"></a><span data-ttu-id="70a21-128">Predefined UII actions</span><span class="sxs-lookup"><span data-stu-id="70a21-128">Predefined UII actions</span></span>  
 <span data-ttu-id="70a21-129">These are the predefined actions for this hosted control type.</span><span class="sxs-lookup"><span data-stu-id="70a21-129">These are the predefined actions for this hosted control type.</span></span>  

<a name="Close"></a>   
### <a name="close"></a><span data-ttu-id="70a21-130">Đóng</span><span class="sxs-lookup"><span data-stu-id="70a21-130">Close</span></span>  
 <span data-ttu-id="70a21-131">This action is used to close the hosted control.</span><span class="sxs-lookup"><span data-stu-id="70a21-131">This action is used to close the hosted control.</span></span>  

### <a name="fireevent"></a><span data-ttu-id="70a21-132">FireEvent</span><span class="sxs-lookup"><span data-stu-id="70a21-132">FireEvent</span></span>  
 <span data-ttu-id="70a21-133">Khuyến khích sự kiện được người dùng xác định từ loại hình kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="70a21-133">Fires a user-defined event from this hosted control.</span></span>  

|<span data-ttu-id="70a21-134">Tham số</span><span class="sxs-lookup"><span data-stu-id="70a21-134">Parameter</span></span>|<span data-ttu-id="70a21-135">Mô tả</span><span class="sxs-lookup"><span data-stu-id="70a21-135">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="70a21-136">tên</span><span class="sxs-lookup"><span data-stu-id="70a21-136">name</span></span>|<span data-ttu-id="70a21-137">Tên của sự kiện do người dùng xác định.</span><span class="sxs-lookup"><span data-stu-id="70a21-137">Name of the user-defined event.</span></span>|  

 <span data-ttu-id="70a21-138">Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này.</span><span class="sxs-lookup"><span data-stu-id="70a21-138">All subsequent name=value pairs become the parameters to the event.</span></span> <span data-ttu-id="70a21-139">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span><span class="sxs-lookup"><span data-stu-id="70a21-139">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span></span>  

<a name="MoveToPanel"></a>   
### <a name="movetopanel"></a><span data-ttu-id="70a21-140">MoveToPanel</span><span class="sxs-lookup"><span data-stu-id="70a21-140">MoveToPanel</span></span>  
 <span data-ttu-id="70a21-141">This action is used to move hosted controls between panels at runtime.</span><span class="sxs-lookup"><span data-stu-id="70a21-141">This action is used to move hosted controls between panels at runtime.</span></span>  

|<span data-ttu-id="70a21-142">Tham số</span><span class="sxs-lookup"><span data-stu-id="70a21-142">Parameter</span></span>|<span data-ttu-id="70a21-143">Mô tả</span><span class="sxs-lookup"><span data-stu-id="70a21-143">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="70a21-144">ứng dụng</span><span class="sxs-lookup"><span data-stu-id="70a21-144">app</span></span>|<span data-ttu-id="70a21-145">Name of the hosted control to be moved.</span><span class="sxs-lookup"><span data-stu-id="70a21-145">Name of the hosted control to be moved.</span></span>|  
|<span data-ttu-id="70a21-146">bảng điều khiển</span><span class="sxs-lookup"><span data-stu-id="70a21-146">panel</span></span>|<span data-ttu-id="70a21-147">Target panel for the hosted control.</span><span class="sxs-lookup"><span data-stu-id="70a21-147">Target panel for the hosted control.</span></span>|  

### <a name="newcrmpage"></a><span data-ttu-id="70a21-148">New_CRM_Page</span><span class="sxs-lookup"><span data-stu-id="70a21-148">New_CRM_Page</span></span>  
 <span data-ttu-id="70a21-149">Creates a page for creating a new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps record of the entity specified, and treats the page as a popup from the specified hosted control.</span><span class="sxs-lookup"><span data-stu-id="70a21-149">Creates a page for creating a new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps record of the entity specified, and treats the page as a popup from the specified hosted control.</span></span> <span data-ttu-id="70a21-150">Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi trang tạo hồ sơ thực thể được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="70a21-150">The window navigation rules are evaluated to determine the location where the page to create the entity record is displayed.</span></span>  

|<span data-ttu-id="70a21-151">Tham số</span><span class="sxs-lookup"><span data-stu-id="70a21-151">Parameter</span></span>|<span data-ttu-id="70a21-152">Mô tả</span><span class="sxs-lookup"><span data-stu-id="70a21-152">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="70a21-153">LogicalName</span><span class="sxs-lookup"><span data-stu-id="70a21-153">LogicalName</span></span>|<span data-ttu-id="70a21-154">Tên logic của thực thể để tạo phiên bản mới.</span><span class="sxs-lookup"><span data-stu-id="70a21-154">The logical name of the entity for creating a new instance.</span></span>|  

> [!NOTE]
>  <span data-ttu-id="70a21-155">Phần còn lại của các tham số nên bao gồm tên = cặp giá trị.</span><span class="sxs-lookup"><span data-stu-id="70a21-155">The rest of the parameters should consist of name=value pairs.</span></span> <span data-ttu-id="70a21-156">These are the additional pre-populated values in the form for creating a new record for the specified entity.</span><span class="sxs-lookup"><span data-stu-id="70a21-156">These are the additional pre-populated values in the form for creating a new record for the specified entity.</span></span> <span data-ttu-id="70a21-157">For more information about using this action, see step 4 in [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="70a21-157">For more information about using this action, see step 4 in [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md).</span></span>  

### <a name="opencrmpage"></a><span data-ttu-id="70a21-158">Open_CRM_Page</span><span class="sxs-lookup"><span data-stu-id="70a21-158">Open_CRM_Page</span></span>  
 <span data-ttu-id="70a21-159">Opens an existing instance of the entity specified and identified by the ID, and treats the page as a popup from the specified hosted control.</span><span class="sxs-lookup"><span data-stu-id="70a21-159">Opens an existing instance of the entity specified and identified by the ID, and treats the page as a popup from the specified hosted control.</span></span> <span data-ttu-id="70a21-160">Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi thư mục bật lên nên sẽ được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="70a21-160">The window navigation rules are evaluated to determine the location where the popup should be displayed.</span></span>  

|<span data-ttu-id="70a21-161">Tham số</span><span class="sxs-lookup"><span data-stu-id="70a21-161">Parameter</span></span>|<span data-ttu-id="70a21-162">Mô tả</span><span class="sxs-lookup"><span data-stu-id="70a21-162">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="70a21-163">LogicalName</span><span class="sxs-lookup"><span data-stu-id="70a21-163">LogicalName</span></span>|<span data-ttu-id="70a21-164">Tên logic của thực thể hợp lý của thực thể để mở.</span><span class="sxs-lookup"><span data-stu-id="70a21-164">The logical name of the entity to open.</span></span>|  
|<span data-ttu-id="70a21-165">id</span><span class="sxs-lookup"><span data-stu-id="70a21-165">id</span></span>|<span data-ttu-id="70a21-166">ID của hồ sơ thực thể để mở.</span><span class="sxs-lookup"><span data-stu-id="70a21-166">The ID of the entity record to open.</span></span>|  

### <a name="popup"></a><span data-ttu-id="70a21-167">Bật lên</span><span class="sxs-lookup"><span data-stu-id="70a21-167">Popup</span></span>  
 <span data-ttu-id="70a21-168">Bật lên URL từ kiểm soát tổ chức và chạy nguyên tắc điều hướng cửa sổ chống lại hình thức kiểm soát tổ chức để định tuyến bật lên đến vị trí thích hợp.</span><span class="sxs-lookup"><span data-stu-id="70a21-168">Pops up a URL from the hosted control and runs the window navigation rules against it for routing the popup to the appropriate location.</span></span>  

|<span data-ttu-id="70a21-169">Tham số</span><span class="sxs-lookup"><span data-stu-id="70a21-169">Parameter</span></span>|<span data-ttu-id="70a21-170">Mô tả</span><span class="sxs-lookup"><span data-stu-id="70a21-170">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="70a21-171">url</span><span class="sxs-lookup"><span data-stu-id="70a21-171">url</span></span>|<span data-ttu-id="70a21-172">Routes a popup from this hosted control using this URL as if it were a popup requested from the displayed control.</span><span class="sxs-lookup"><span data-stu-id="70a21-172">Routes a popup from this hosted control using this URL as if it were a popup requested from the displayed control.</span></span>|  
|<span data-ttu-id="70a21-173">nền tảng</span><span class="sxs-lookup"><span data-stu-id="70a21-173">frame</span></span>|<span data-ttu-id="70a21-174">The frame from which this popup originated.</span><span class="sxs-lookup"><span data-stu-id="70a21-174">The frame from which this popup originated.</span></span>|  

<a name="RealignWindow"></a>   
### <a name="realignwindow"></a><span data-ttu-id="70a21-175">RealignWindow</span><span class="sxs-lookup"><span data-stu-id="70a21-175">RealignWindow</span></span>  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]

<a name="SetSize"></a>   
### <a name="setsize"></a><span data-ttu-id="70a21-176">SetSize</span><span class="sxs-lookup"><span data-stu-id="70a21-176">SetSize</span></span>  
 <span data-ttu-id="70a21-177">This action explicitly sets the width and height of the hosted control.</span><span class="sxs-lookup"><span data-stu-id="70a21-177">This action explicitly sets the width and height of the hosted control.</span></span> <span data-ttu-id="70a21-178">Quá trình này đặc biệt hữu ích khi sử dụng tính năng "tự động" trong bố cục bảng điều khiển của bạn.</span><span class="sxs-lookup"><span data-stu-id="70a21-178">This is particularly useful when using "auto" in your panel layouts.</span></span>  

|<span data-ttu-id="70a21-179">Tham số</span><span class="sxs-lookup"><span data-stu-id="70a21-179">Parameter</span></span>|<span data-ttu-id="70a21-180">Mô tả</span><span class="sxs-lookup"><span data-stu-id="70a21-180">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="70a21-181">chiều rộng</span><span class="sxs-lookup"><span data-stu-id="70a21-181">width</span></span>|<span data-ttu-id="70a21-182">Chiều rộng của kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="70a21-182">The width of the hosted control.</span></span>|  
|<span data-ttu-id="70a21-183">chiều cao</span><span class="sxs-lookup"><span data-stu-id="70a21-183">height</span></span>|<span data-ttu-id="70a21-184">Chiều cao của kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="70a21-184">The height of the hosted control.</span></span>|  

### <a name="startdialog"></a><span data-ttu-id="70a21-185">Hộp thoại bắt đầu</span><span class="sxs-lookup"><span data-stu-id="70a21-185">StartDialog</span></span>  
 <span data-ttu-id="70a21-186">Hành động này phải có một số thông số nhưng cho hộp thoại không liên quan đến một hồ sơ cụ thể, bạn chỉ có thể chỉ định các tham số **tên**.</span><span class="sxs-lookup"><span data-stu-id="70a21-186">This action takes several parameters but for dialogs that do not relate to a specific record, you can just specify the **Name** parameter.</span></span>  


| <span data-ttu-id="70a21-187">Tham số</span><span class="sxs-lookup"><span data-stu-id="70a21-187">Parameter</span></span> |                                                                                      <span data-ttu-id="70a21-188">Mô tả</span><span class="sxs-lookup"><span data-stu-id="70a21-188">Description</span></span>                                                                                       |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="70a21-189">Tên</span><span class="sxs-lookup"><span data-stu-id="70a21-189">Name</span></span>    |                        <span data-ttu-id="70a21-190">The name of the dialog as seen in the **Settings** > **Process** section of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="70a21-190">The name of the dialog as seen in the **Settings** > **Process** section of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span></span>                        |
| <span data-ttu-id="70a21-191">DialogId</span><span class="sxs-lookup"><span data-stu-id="70a21-191">DialogId</span></span>  |                 <span data-ttu-id="70a21-192">Bạn cũng có thể chỉ định hộp thoại bằng ID.</span><span class="sxs-lookup"><span data-stu-id="70a21-192">You can also specify the dialog by its ID.</span></span> <span data-ttu-id="70a21-193">Nếu bạn chỉ định tham số **DialogId**, nó sẽ được sử dụng bởi các hành động thay vì các tham số **tên**.</span><span class="sxs-lookup"><span data-stu-id="70a21-193">If you specify the **DialogId** parameter, it will be used by the action instead of the **Name** parameter.</span></span>                 |
|  <span data-ttu-id="70a21-194">Thực thể</span><span class="sxs-lookup"><span data-stu-id="70a21-194">Entity</span></span>   |    <span data-ttu-id="70a21-195">Đây là loại thực thể mà hộp thoại phải chạy chống lại.</span><span class="sxs-lookup"><span data-stu-id="70a21-195">This is the type of entity that the dialog is to be run against.</span></span> <span data-ttu-id="70a21-196">Điều này là bắt buộc nếu bạn sử dụng tham số **DialogId**.</span><span class="sxs-lookup"><span data-stu-id="70a21-196">This is required if you use the **DialogId** parameter.</span></span> <span data-ttu-id="70a21-197">Nó là không cần thiết, nếu tham số **tên** được sử dụng.</span><span class="sxs-lookup"><span data-stu-id="70a21-197">It is not required, if the **Name** parameter is used.</span></span>     |
|    <span data-ttu-id="70a21-198">Id</span><span class="sxs-lookup"><span data-stu-id="70a21-198">Id</span></span>     | <span data-ttu-id="70a21-199">Đây là ID của các thực thể mà phiên hộp thoại áp dụng.</span><span class="sxs-lookup"><span data-stu-id="70a21-199">This is the ID of the entity to which the Dialog session applies.</span></span> <span data-ttu-id="70a21-200">Nếu tham số này không được chỉ định, hộp thoại chạy chống lại sự xâm nhập đầu tiên của loại thích hợp trong hệ thống.</span><span class="sxs-lookup"><span data-stu-id="70a21-200">If this parameter is not specified, the dialog is run against the first entry of the appropriate type in the system.</span></span> |

 <span data-ttu-id="70a21-201">Khi hộp thoại kết thúc, nó sẽ nhắc người dùng đóng cửa sổ.</span><span class="sxs-lookup"><span data-stu-id="70a21-201">When the dialog is finished, it will prompt the user to close the window.</span></span> <span data-ttu-id="70a21-202">Nếu người sử dụng khẳng định, tab trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] cũng sẽ đóng điều này do thiết kế.</span><span class="sxs-lookup"><span data-stu-id="70a21-202">If the user affirms, the tab in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] will close as well, which is by design.</span></span>  

<a name="events"></a>   
## <a name="predefined-events"></a><span data-ttu-id="70a21-203">Sự kiện được xác định trước</span><span class="sxs-lookup"><span data-stu-id="70a21-203">Predefined events</span></span>  
 <span data-ttu-id="70a21-204">Các sự kiện được xác định trước sau đây được liên kết với loại kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="70a21-204">The following predefined events are associated with this hosted control type.</span></span>  

### <a name="browserdocumentcomplete"></a><span data-ttu-id="70a21-205">Duyệt Tài liệu hoàn chỉnh</span><span class="sxs-lookup"><span data-stu-id="70a21-205">BrowserDocumentComplete</span></span>  
 <span data-ttu-id="70a21-206">Xảy ra khi trang đã hoàn tất tải.</span><span class="sxs-lookup"><span data-stu-id="70a21-206">Occurs when the page has finished loading.</span></span> <span data-ttu-id="70a21-207">Trên loại **Trang CRM** của kiểm soát tổ chức, sự kiện này xảy ra sau khi dữ liệu đã được lưu vào danh sách tham số thay thế.</span><span class="sxs-lookup"><span data-stu-id="70a21-207">On a **CRM Page** type of hosted control, this event occurs after the data has been saved to the replacement parameter list.</span></span> <span data-ttu-id="70a21-208">Sự kiện này chỉ xảy ra một lần, mặc dù nhiều nền tảng sẽ được khởi động riêng lẻ sự kiện **BrowserDocumentComplete** của chúng.</span><span class="sxs-lookup"><span data-stu-id="70a21-208">This event occurs only once, even though multiple frames will have individually fired their **BrowserDocumentComplete** events.</span></span>  

|<span data-ttu-id="70a21-209">Tham số</span><span class="sxs-lookup"><span data-stu-id="70a21-209">Parameter</span></span>|<span data-ttu-id="70a21-210">Mô tả</span><span class="sxs-lookup"><span data-stu-id="70a21-210">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="70a21-211">url</span><span class="sxs-lookup"><span data-stu-id="70a21-211">url</span></span>|<span data-ttu-id="70a21-212">URL của trang đã hoàn tất tải.</span><span class="sxs-lookup"><span data-stu-id="70a21-212">The URL of the page that has finished loading.</span></span>|  

### <a name="popuprouted"></a><span data-ttu-id="70a21-213">Bật lên đã lên lịch</span><span class="sxs-lookup"><span data-stu-id="70a21-213">PopupRouted</span></span>  
 <span data-ttu-id="70a21-214">Xảy ra sau khi một cửa sổ bật lên đã được hệ thống xác định.</span><span class="sxs-lookup"><span data-stu-id="70a21-214">Occurs after a popup has been routed by the system.</span></span>  

|<span data-ttu-id="70a21-215">Tham số</span><span class="sxs-lookup"><span data-stu-id="70a21-215">Parameter</span></span>|<span data-ttu-id="70a21-216">Mô tả</span><span class="sxs-lookup"><span data-stu-id="70a21-216">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="70a21-217">url</span><span class="sxs-lookup"><span data-stu-id="70a21-217">url</span></span>|<span data-ttu-id="70a21-218">The URL of the popup that was routed.</span><span class="sxs-lookup"><span data-stu-id="70a21-218">The URL of the popup that was routed.</span></span>|  

### <a name="see-also"></a><span data-ttu-id="70a21-219">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="70a21-219">See also</span></span>  
 <span data-ttu-id="70a21-220">[Trang CRM (Kiểm soát tổ chức)](../unified-service-desk/crm-page-hosted-control.md) </span><span class="sxs-lookup"><span data-stu-id="70a21-220">[CRM Page (Hosted Control)](../unified-service-desk/crm-page-hosted-control.md) </span></span>  
 <span data-ttu-id="70a21-221">[Hành động UII](../unified-service-desk/uii-actions.md) </span><span class="sxs-lookup"><span data-stu-id="70a21-221">[UII actions](../unified-service-desk/uii-actions.md) </span></span>  
 <span data-ttu-id="70a21-222">[Sự kiện](../unified-service-desk/events.md) </span><span class="sxs-lookup"><span data-stu-id="70a21-222">[Events](../unified-service-desk/events.md) </span></span>  
 <span data-ttu-id="70a21-223">[Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="70a21-223">[Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md) </span></span>  
 <span data-ttu-id="70a21-224">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md) </span><span class="sxs-lookup"><span data-stu-id="70a21-224">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md) </span></span>  
 [<span data-ttu-id="70a21-225">Administration Guide for Unified Service Desk for Microsoft Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="70a21-225">Administration Guide for Unified Service Desk for Microsoft Dynamics 365 for Customer Engagement apps</span></span>](http://go.microsoft.com/fwlink/p/?LinkID=394402)
