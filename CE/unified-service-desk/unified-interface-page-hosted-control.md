---
title: Unified Interface Page (Hosted Control) (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about the Unified Interface Page hosted control type to load a URL or page from Dynamics 365 for Customer Engagement apps. When a Dynamics 365 for Customer Engagement apps page is loaded within a hosted control of this type, it will automatically scan the page for data from the entity, and automatically populate the replacement parameters.
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
ms.assetid: 3AEB8475-FCBE-4526-8000-CF06CED9586C
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 2c3cfd04bf930d9707514c7ea32368b01e7bfa02
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388611"
---
# <a name="unified-interface-page-hosted-control"></a><span data-ttu-id="5752d-104">Unified Interface Page (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="5752d-104">Unified Interface Page (Hosted Control)</span></span>
<span data-ttu-id="5752d-105">Use the **Unified Interface Page** hosted control type to load a URL or page from Unified Interface Apps in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="5752d-105">Use the **Unified Interface Page** hosted control type to load a URL or page from Unified Interface Apps in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span></span> <span data-ttu-id="5752d-106">When a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps page is loaded within a hosted control of this type, it will automatically scan the page for data from the entity, and automatically populate the replacement parameters.</span><span class="sxs-lookup"><span data-stu-id="5752d-106">When a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps page is loaded within a hosted control of this type, it will automatically scan the page for data from the entity, and automatically populate the replacement parameters.</span></span>
  
 <span data-ttu-id="5752d-107">This hosted control type exposes a number of predefined UII actions and events that are unique to handling of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps [!INCLUDE[pn-ms-windows-short](../includes/pn-ms-windows-short.md)] including list manipulation actions, and a find action for displaying a quick search or advanced search page.</span><span class="sxs-lookup"><span data-stu-id="5752d-107">This hosted control type exposes a number of predefined UII actions and events that are unique to handling of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps [!INCLUDE[pn-ms-windows-short](../includes/pn-ms-windows-short.md)] including list manipulation actions, and a find action for displaying a quick search or advanced search page.</span></span>

## <a name="create-a-unified-interface-page-hosted-control"></a><span data-ttu-id="5752d-108">Create a Unified Interface Page hosted control</span><span class="sxs-lookup"><span data-stu-id="5752d-108">Create a Unified Interface Page hosted control</span></span>

<span data-ttu-id="5752d-109">Trong khi tạo một hình thức kiểm soát tổ chức mới, các trường trong màn hình Kiểm soát tổ chức mới thay đổi dựa vào loại tổ chức tổ chức bạn muốn tạo.</span><span class="sxs-lookup"><span data-stu-id="5752d-109">While creating a new hosted control, the fields in the New Hosted Control screen vary based on the type of hosted control you want to create.</span></span> <span data-ttu-id="5752d-110">This section provides information about the specific fields that are unique to the Unified Interface Page hosted control type.</span><span class="sxs-lookup"><span data-stu-id="5752d-110">This section provides information about the specific fields that are unique to the Unified Interface Page hosted control type.</span></span>

<span data-ttu-id="5752d-111">In the New Hosted Control screen:</span><span class="sxs-lookup"><span data-stu-id="5752d-111">In the New Hosted Control screen:</span></span>

- <span data-ttu-id="5752d-112">Under **[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]** area, select **Unified Interface Page** from the **USD Component Type** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="5752d-112">Under **[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]** area, select **Unified Interface Page** from the **USD Component Type** drop-down list.</span></span>

- <span data-ttu-id="5752d-113">Select **Pre-fetch Data** to load related information for an entity record in the context along with the entity record page without having to wait for the full entity web page to load in the client application.</span><span class="sxs-lookup"><span data-stu-id="5752d-113">Select **Pre-fetch Data** to load related information for an entity record in the context along with the entity record page without having to wait for the full entity web page to load in the client application.</span></span> <span data-ttu-id="5752d-114">Thông tin thực thể tìm nạp được điền trong ngữ cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để kích hoạt mọi kiểm soát tổ chức nhằm nhanh chóng hiển thị thông tin thực thể có liên quan trên ứng dụng khách.</span><span class="sxs-lookup"><span data-stu-id="5752d-114">The fetched entity information is populated in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context thus enabling any hosted control to quickly display relevant entity information on the client application.</span></span> <span data-ttu-id="5752d-115">This could help agents instantly act or kick start discussion with customers, and save crucial interaction time.</span><span class="sxs-lookup"><span data-stu-id="5752d-115">This could help agents instantly act or kick start discussion with customers, and save crucial interaction time.</span></span>

- <span data-ttu-id="5752d-116">From the **Allow Multiple Pages** drop-down list, select **No** (default) to replace the Dynamics 365 for Customer Engagement apps page that is currently displayed, and update the browser history when [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] receives a navigate action call or a page is routed to the tab. Select **Yes** to automatically create a drop-down list when a second URL is called or a window navigation rule directs a page to the tab. This allows the user to quickly search between the Dynamics 365 for Customer Engagement apps pages that are attached to this control.</span><span class="sxs-lookup"><span data-stu-id="5752d-116">From the **Allow Multiple Pages** drop-down list, select **No** (default) to replace the Dynamics 365 for Customer Engagement apps page that is currently displayed, and update the browser history when [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] receives a navigate action call or a page is routed to the tab. Select **Yes** to automatically create a drop-down list when a second URL is called or a window navigation rule directs a page to the tab. This allows the user to quickly search between the Dynamics 365 for Customer Engagement apps pages that are attached to this control.</span></span> <span data-ttu-id="5752d-117">Also, when you select **Yes**, an additional field, **Maximum Browsers**, becomes available where you can specify the maximum number of pages to be displayed in the drop-down list.</span><span class="sxs-lookup"><span data-stu-id="5752d-117">Also, when you select **Yes**, an additional field, **Maximum Browsers**, becomes available where you can specify the maximum number of pages to be displayed in the drop-down list.</span></span>

- <span data-ttu-id="5752d-118">Under the **Common Properties** area, select the **Application is Global** check box to set the hosted control as global.</span><span class="sxs-lookup"><span data-stu-id="5752d-118">Under the **Common Properties** area, select the **Application is Global** check box to set the hosted control as global.</span></span> <span data-ttu-id="5752d-119">Kiểm soát tổ chức chung có thể được hiển thị bên ngoài phiên khách hàng.</span><span class="sxs-lookup"><span data-stu-id="5752d-119">Global hosted controls can be displayed outside of a customer session.</span></span> <span data-ttu-id="5752d-120">Kiểm soát giống như bảng thông tin của tổng đài viên, tường hoặc tìm kiếm là những hình thức sử dụng chung cho kiểm soát tổ chức chung.</span><span class="sxs-lookup"><span data-stu-id="5752d-120">Controls like the agents’ dashboard, wall or search are common uses for global hosted controls.</span></span> <span data-ttu-id="5752d-121">Kiểm soát tổ chức chung không có trạng thái phiên dành riêng cho phiên để khi bạn thay đổi phiên, các kiểm soát tổ chức chung tương tự vẫn được duy trì.</span><span class="sxs-lookup"><span data-stu-id="5752d-121">Global hosted controls do not have session-specific state so when you change sessions, these same global hosted controls remain.</span></span> <span data-ttu-id="5752d-122">Nếu hộp kiểm không được chọn, kiểm soát tổ chức trở thành kiểu dựa trên phiên.</span><span class="sxs-lookup"><span data-stu-id="5752d-122">If the check box is not selected, the hosted control becomes session based.</span></span> <span data-ttu-id="5752d-123">Kiểm soát dựa trên phiên tồn tại trong ngữ cảnh của phiên khách hàng.</span><span class="sxs-lookup"><span data-stu-id="5752d-123">Session-based controls exist in the context of the customer session.</span></span> <span data-ttu-id="5752d-124">Nếu người dùng thay đổi sang một phiên khác, tất cả các trang phiên từ phiên trước đó được ẩn.</span><span class="sxs-lookup"><span data-stu-id="5752d-124">If the user changes to another session, all the session pages from the previous session are hidden.</span></span>

- <span data-ttu-id="5752d-125">Trường **Hiển thị nhóm** hiển thị bảng điều khiển nơi hiển thị kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="5752d-125">The **Display Group** field displays the panel where this hosted control will be displayed.</span></span> <span data-ttu-id="5752d-126">**MainPanel** is the most common for this hosted control type.</span><span class="sxs-lookup"><span data-stu-id="5752d-126">**MainPanel** is the most common for this hosted control type.</span></span>

<span data-ttu-id="5752d-127">For information about other **General** fields, see Create or edit a hosted control.</span><span class="sxs-lookup"><span data-stu-id="5752d-127">For information about other **General** fields, see Create or edit a hosted control.</span></span>

## <a name="predefined-uii-actions"></a><span data-ttu-id="5752d-128">Predefined UII actions</span><span class="sxs-lookup"><span data-stu-id="5752d-128">Predefined UII actions</span></span>

<span data-ttu-id="5752d-129">These are the predefined actions for this hosted control type.</span><span class="sxs-lookup"><span data-stu-id="5752d-129">These are the predefined actions for this hosted control type.</span></span>

### <a name="associatedview"></a><span data-ttu-id="5752d-130">Chế độ xem Liên kết</span><span class="sxs-lookup"><span data-stu-id="5752d-130">AssociatedView</span></span>

<span data-ttu-id="5752d-131">This action loads a specific associated view of Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="5752d-131">This action loads a specific associated view of Dynamics 365 for Customer Engagement apps.</span></span> <span data-ttu-id="5752d-132">These views are typically accessed by clicking down arrow next to an entity record name in the nav bar, and selecting the associated entities.</span><span class="sxs-lookup"><span data-stu-id="5752d-132">These views are typically accessed by clicking down arrow next to an entity record name in the nav bar, and selecting the associated entities.</span></span>

| <span data-ttu-id="5752d-133">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-133">Parameter</span></span>         | <span data-ttu-id="5752d-134">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-134">Description</span></span>                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5752d-135">etn</span><span class="sxs-lookup"><span data-stu-id="5752d-135">etn</span></span>               | <span data-ttu-id="5752d-136">The name of the entity for which you want to load list of records of the associated entity.</span><span class="sxs-lookup"><span data-stu-id="5752d-136">The name of the entity for which you want to load list of records of the associated entity.</span></span>  <span data-ttu-id="5752d-137">This is a mandatory parameter</span><span class="sxs-lookup"><span data-stu-id="5752d-137">This is a mandatory parameter</span></span>|
| <span data-ttu-id="5752d-138">ID</span><span class="sxs-lookup"><span data-stu-id="5752d-138">Id</span></span>                | <span data-ttu-id="5752d-139">The ID of the main entity record for which to display the associated entity records.</span><span class="sxs-lookup"><span data-stu-id="5752d-139">The ID of the main entity record for which to display the associated entity records.</span></span>                                    |
| <span data-ttu-id="5752d-140">navItemId</span><span class="sxs-lookup"><span data-stu-id="5752d-140">navItemId</span></span>         | <span data-ttu-id="5752d-141">Id of the navigation item corresponding to the associated entity.</span><span class="sxs-lookup"><span data-stu-id="5752d-141">Id of the navigation item corresponding to the associated entity.</span></span> <span data-ttu-id="5752d-142">More information: [formContext.ui.navigation](/dynamics365/customer-engagement/developer/clientapi/reference/formcontext-ui-navigation)</span><span class="sxs-lookup"><span data-stu-id="5752d-142">More information: [formContext.ui.navigation](/dynamics365/customer-engagement/developer/clientapi/reference/formcontext-ui-navigation)</span></span>      |
| <span data-ttu-id="5752d-143">hideCommandBar</span><span class="sxs-lookup"><span data-stu-id="5752d-143">hideCommandBar</span></span>    | <span data-ttu-id="5752d-144">If this parameter is supplied and False, the page will be displayed along with the Dynamics 365 for Customer Engagement apps command bar.</span><span class="sxs-lookup"><span data-stu-id="5752d-144">If this parameter is supplied and False, the page will be displayed along with the Dynamics 365 for Customer Engagement apps command bar.</span></span> |
| <span data-ttu-id="5752d-145">hideNavigationBar</span><span class="sxs-lookup"><span data-stu-id="5752d-145">hideNavigationBar</span></span> | <span data-ttu-id="5752d-146">If this parameter is supplied and False, the page will be displayed along with the Dynamics 365 for Customer Engagement apps navigation bar.</span><span class="sxs-lookup"><span data-stu-id="5752d-146">If this parameter is supplied and False, the page will be displayed along with the Dynamics 365 for Customer Engagement apps navigation bar.</span></span>     |

### <a name="close"></a><span data-ttu-id="5752d-147">Đóng</span><span class="sxs-lookup"><span data-stu-id="5752d-147">Close</span></span>

<span data-ttu-id="5752d-148">This action is used to close the hosted control.</span><span class="sxs-lookup"><span data-stu-id="5752d-148">This action is used to close the hosted control.</span></span> <span data-ttu-id="5752d-149">Unlike the **CloseActive** action, if this tab (hosted control) is displaying more than one page, it will close all the pages displayed in the tab in your agent application.</span><span class="sxs-lookup"><span data-stu-id="5752d-149">Unlike the **CloseActive** action, if this tab (hosted control) is displaying more than one page, it will close all the pages displayed in the tab in your agent application.</span></span>

### <a name="closeactive"></a><span data-ttu-id="5752d-150">CloseActive</span><span class="sxs-lookup"><span data-stu-id="5752d-150">CloseActive</span></span>

<span data-ttu-id="5752d-151">This action is used to close the active window within this hosted control.</span><span class="sxs-lookup"><span data-stu-id="5752d-151">This action is used to close the active window within this hosted control.</span></span> <span data-ttu-id="5752d-152">If the active window is the only window displayed in the hosted control, the hosted control itself will be closed.</span><span class="sxs-lookup"><span data-stu-id="5752d-152">If the active window is the only window displayed in the hosted control, the hosted control itself will be closed.</span></span> <span data-ttu-id="5752d-153">For **Unified Interface Page** type of hosted controls that do not allow multiple pages (**Allow Multiple Pages** = No), this action is equivalent to the **Close** action.</span><span class="sxs-lookup"><span data-stu-id="5752d-153">For **Unified Interface Page** type of hosted controls that do not allow multiple pages (**Allow Multiple Pages** = No), this action is equivalent to the **Close** action.</span></span>

### <a name="closeandprompt"></a><span data-ttu-id="5752d-154">Đóng và Nhắc</span><span class="sxs-lookup"><span data-stu-id="5752d-154">CloseAndPrompt</span></span>

<span data-ttu-id="5752d-155">This action closes the hosted control, but prompts the user to save or abandon the changes before closing.</span><span class="sxs-lookup"><span data-stu-id="5752d-155">This action closes the hosted control, but prompts the user to save or abandon the changes before closing.</span></span>

### <a name="find"></a><span data-ttu-id="5752d-156">Find</span><span class="sxs-lookup"><span data-stu-id="5752d-156">Find</span></span>

<span data-ttu-id="5752d-157">Navigate to the quick find list view of the specified entity.</span><span class="sxs-lookup"><span data-stu-id="5752d-157">Navigate to the quick find list view of the specified entity.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5752d-158"><strong>Tham số</strong></span><span class="sxs-lookup"><span data-stu-id="5752d-158"><strong>Parameter</strong></span></span></th>
<th><span data-ttu-id="5752d-159"><strong>Mô tả</strong></span><span class="sxs-lookup"><span data-stu-id="5752d-159"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5752d-160">Tham số dữ liệu nên chỉ định tên logic của thực thể của chế độ xem danh sách tìm nhanh để hiển thị.</span><span class="sxs-lookup"><span data-stu-id="5752d-160">The data parameter should specify the entity logical name of the quick find list view to display.</span></span> <span data-ttu-id="5752d-161">Có một số giá trị trường hợp đặc biệt:</span><span class="sxs-lookup"><span data-stu-id="5752d-161">There are some special case values:</span></span><br /><span data-ttu-id="5752d-162">
- Use <strong>case</strong> or <strong>incident</strong> to display the quick find list view for cases.</span><span class="sxs-lookup"><span data-stu-id="5752d-162">
- Use <strong>case</strong> or <strong>incident</strong> to display the quick find list view for cases.</span></span><br /><span data-ttu-id="5752d-163">
- Use <strong>activities</strong> or <strong>activity</strong> to display the quick find list view for activities.</span><span class="sxs-lookup"><span data-stu-id="5752d-163">
- Use <strong>activities</strong> or <strong>activity</strong> to display the quick find list view for activities.</span></span></td>
</tr>
</tbody>
</table>

### <a name="fireevent"></a><span data-ttu-id="5752d-164">FireEvent</span><span class="sxs-lookup"><span data-stu-id="5752d-164">FireEvent</span></span>

<span data-ttu-id="5752d-165">Fires a user-defined event from this hosted control.</span><span class="sxs-lookup"><span data-stu-id="5752d-165">Fires a user-defined event from this hosted control.</span></span>

| <span data-ttu-id="5752d-166">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-166">Parameter</span></span> | <span data-ttu-id="5752d-167">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-167">Description</span></span>                     |
|-----------|---------------------------------|
| <span data-ttu-id="5752d-168">tên</span><span class="sxs-lookup"><span data-stu-id="5752d-168">name</span></span>      | <span data-ttu-id="5752d-169">Tên của sự kiện do người dùng xác định.</span><span class="sxs-lookup"><span data-stu-id="5752d-169">Name of the user-defined event.</span></span> |

<span data-ttu-id="5752d-170">Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này.</span><span class="sxs-lookup"><span data-stu-id="5752d-170">All subsequent name=value pairs become the parameters to the event.</span></span> <span data-ttu-id="5752d-171">For more information about creating a user-defined event, see [Create a user-defined event](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/create-user-defined-event).</span><span class="sxs-lookup"><span data-stu-id="5752d-171">For more information about creating a user-defined event, see [Create a user-defined event](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/create-user-defined-event).</span></span>  

### <a name="getselectedids"></a><span data-ttu-id="5752d-172">Tải một số id đã chọn</span><span class="sxs-lookup"><span data-stu-id="5752d-172">GetSelectedIds</span></span>

<span data-ttu-id="5752d-173">This action is used to retrieve the selected IDs from the lists.</span><span class="sxs-lookup"><span data-stu-id="5752d-173">This action is used to retrieve the selected IDs from the lists.</span></span>

| <span data-ttu-id="5752d-174">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-174">Parameter</span></span> | <span data-ttu-id="5752d-175">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-175">Description</span></span>                                                                  |
|-----------|------------------------------------------------------------------------------|
|           | <span data-ttu-id="5752d-176">Tham số dữ liệu nên chỉ định tên danh sách để giữ ID đã chọn.</span><span class="sxs-lookup"><span data-stu-id="5752d-176">The data parameter should specify the list name to capture the selected IDs.</span></span> |

<span data-ttu-id="5752d-177">Giá trị trả về chứa danh sách được phân tách bằng dấu chấm phẩy có chứa các mục đã chọn.</span><span class="sxs-lookup"><span data-stu-id="5752d-177">The return value contains a semi-colon delimited list of IDs containing the selected items.</span></span>

### <a name="getselectedcount"></a><span data-ttu-id="5752d-178">Tải số lượng đã chọn</span><span class="sxs-lookup"><span data-stu-id="5752d-178">GetSelectedCount</span></span>

<span data-ttu-id="5752d-179">Hành động này sẽ truy xuất số mục mà đã được chọn.</span><span class="sxs-lookup"><span data-stu-id="5752d-179">This action retrieves the number of items that are selected.</span></span> <span data-ttu-id="5752d-180">Sử dụng hành động **Tải id đã chọn** để tải danh sách thực của ID cho thực thể.</span><span class="sxs-lookup"><span data-stu-id="5752d-180">Use the **GetSelectedIds** action to get the actual list of IDs for the entity.</span></span>

| <span data-ttu-id="5752d-181">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-181">Parameter</span></span> | <span data-ttu-id="5752d-182">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-182">Description</span></span>                                                                   |
|-----------|-------------------------------------------------------------------------------|
|           | <span data-ttu-id="5752d-183">Tham số dữ liệu nên chỉ định tên danh sách để truy xuất ID đã chọn.</span><span class="sxs-lookup"><span data-stu-id="5752d-183">The data parameter should specify the list name to retrieve the selected IDs.</span></span> |

<span data-ttu-id="5752d-184">The return value contains a number represented the quantity of selected items.</span><span class="sxs-lookup"><span data-stu-id="5752d-184">The return value contains a number represented the quantity of selected items.</span></span>

### <a name="gohome"></a><span data-ttu-id="5752d-185">Về Trang chủ</span><span class="sxs-lookup"><span data-stu-id="5752d-185">GoHome</span></span>

<span data-ttu-id="5752d-186">This action goes to the initial URL specified for this browser instance.</span><span class="sxs-lookup"><span data-stu-id="5752d-186">This action goes to the initial URL specified for this browser instance.</span></span>

### <a name="goback"></a><span data-ttu-id="5752d-187">Quay lại</span><span class="sxs-lookup"><span data-stu-id="5752d-187">GoBack</span></span>

<span data-ttu-id="5752d-188">Hành động này là tương đương với việc nhấp vào nút quay lại trên phiên bản trình duyệt.</span><span class="sxs-lookup"><span data-stu-id="5752d-188">This action is equivalent to clicking the back button on the browser instance.</span></span>

### <a name="goforward"></a><span data-ttu-id="5752d-189">Chuyển về phía trước</span><span class="sxs-lookup"><span data-stu-id="5752d-189">GoForward</span></span>

<span data-ttu-id="5752d-190">This action is equivalent to clicking the forward button on the browser instance.</span><span class="sxs-lookup"><span data-stu-id="5752d-190">This action is equivalent to clicking the forward button on the browser instance.</span></span>

### <a name="movetopanel"></a><span data-ttu-id="5752d-191">MoveToPanel</span><span class="sxs-lookup"><span data-stu-id="5752d-191">MoveToPanel</span></span>

<span data-ttu-id="5752d-192">This action moves a Unified Interface Page hosted control to a different panel at runtime.</span><span class="sxs-lookup"><span data-stu-id="5752d-192">This action moves a Unified Interface Page hosted control to a different panel at runtime.</span></span>

| <span data-ttu-id="5752d-193">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-193">Parameter</span></span> | <span data-ttu-id="5752d-194">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-194">Description</span></span>                                                                                                        |
|-----------|--------------------------------------------------------------------------------------------------------------------|
|           | <span data-ttu-id="5752d-195">The data parameter should specify the target panel name to move the hosted control to.</span><span class="sxs-lookup"><span data-stu-id="5752d-195">The data parameter should specify the target panel name to move the hosted control to.</span></span> <span data-ttu-id="5752d-196">For example: FloatingPanel.</span><span class="sxs-lookup"><span data-stu-id="5752d-196">For example: FloatingPanel.</span></span> |

### <a name="navigate"></a><span data-ttu-id="5752d-197">Navigate</span><span class="sxs-lookup"><span data-stu-id="5752d-197">Navigate</span></span>

<span data-ttu-id="5752d-198">This action is used to navigate to a Dynamics 365 for Customer Engagement apps url.</span><span class="sxs-lookup"><span data-stu-id="5752d-198">This action is used to navigate to a Dynamics 365 for Customer Engagement apps url.</span></span> <span data-ttu-id="5752d-199">The App Id for the App that you select from **Select App Module** window is appended automatically.</span><span class="sxs-lookup"><span data-stu-id="5752d-199">The App Id for the App that you select from **Select App Module** window is appended automatically.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5752d-200">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-200">Parameter</span></span></th>
<th><span data-ttu-id="5752d-201">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-201">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5752d-202">url</span><span class="sxs-lookup"><span data-stu-id="5752d-202">url</span></span></td>
<td><span data-ttu-id="5752d-203">The URL to navigate to.</span><span class="sxs-lookup"><span data-stu-id="5752d-203">The URL to navigate to.</span></span> <span data-ttu-id="5752d-204">This is a mandatory parameter.</span><span class="sxs-lookup"><span data-stu-id="5752d-204">This is a mandatory parameter.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5752d-205">HideCommandBar</span><span class="sxs-lookup"><span data-stu-id="5752d-205">HideCommandBar</span></span></td>
<td><span data-ttu-id="5752d-206">If this parameter is supplied and True, the inner frame will be displayed without loading the Dynamics 365 for Customer Engagement apps command bar.</span><span class="sxs-lookup"><span data-stu-id="5752d-206">If this parameter is supplied and True, the inner frame will be displayed without loading the Dynamics 365 for Customer Engagement apps command bar.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5752d-207">HideNavigationBar</span><span class="sxs-lookup"><span data-stu-id="5752d-207">HideNavigationBar</span></span></td>
<td><span data-ttu-id="5752d-208">If this parameter is supplied and True, the form will be displayed without loading the Dynamics 365 for Customer Engagement apps navigation bar.</span><span class="sxs-lookup"><span data-stu-id="5752d-208">If this parameter is supplied and True, the form will be displayed without loading the Dynamics 365 for Customer Engagement apps navigation bar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5752d-209">Nền tảng</span><span class="sxs-lookup"><span data-stu-id="5752d-209">Frame</span></span></td>
<td><span data-ttu-id="5752d-210">When frames exist on the page, this parameter would specify the name of the frame to navigate, rather than navigating the main window.</span><span class="sxs-lookup"><span data-stu-id="5752d-210">When frames exist on the page, this parameter would specify the name of the frame to navigate, rather than navigating the main window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5752d-211">postdata</span><span class="sxs-lookup"><span data-stu-id="5752d-211">postdata</span></span></td>
<td><span data-ttu-id="5752d-212">Data that is sent to the server as part of an HTTPPOST transaction.</span><span class="sxs-lookup"><span data-stu-id="5752d-212">Data that is sent to the server as part of an HTTPPOST transaction.</span></span> <span data-ttu-id="5752d-213">A POST transaction is typically used to send data gathered by an HTML page.</span><span class="sxs-lookup"><span data-stu-id="5752d-213">A POST transaction is typically used to send data gathered by an HTML page.</span></span> <span data-ttu-id="5752d-214">In <!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]: Couldn&#39;t find file ../includes/pn-unified-service-desk.md. -->[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]<!--END ERROR INCLUDE -->, this data can be received from any event triggered using &quot;<a href="http://event/?" class="uri">http://event/?</a>&quot;.</span><span class="sxs-lookup"><span data-stu-id="5752d-214">In <!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]: Couldn&#39;t find file ../includes/pn-unified-service-desk.md. -->[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]<!--END ERROR INCLUDE -->, this data can be received from any event triggered using &quot;<a href="http://event/?" class="uri">http://event/?</a>&quot;.</span></span> <span data-ttu-id="5752d-215">Example: [[postdata]+]</span><span class="sxs-lookup"><span data-stu-id="5752d-215">Example: [[postdata]+]</span></span><br />
<br />
<span data-ttu-id="5752d-216">Alternatively, the data can be passed as an encoded string with its header type in the intended format.</span><span class="sxs-lookup"><span data-stu-id="5752d-216">Alternatively, the data can be passed as an encoded string with its header type in the intended format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5752d-217">tiêu đề</span><span class="sxs-lookup"><span data-stu-id="5752d-217">header</span></span></td>
<td><span data-ttu-id="5752d-218">Giá trị chuỗi chứa tiêu đề HTTP bổ sung để gửi tới máy chủ.</span><span class="sxs-lookup"><span data-stu-id="5752d-218">A string value that contains additional HTTP headers to send to the server.</span></span> <span data-ttu-id="5752d-219">When the postdata parameter is used in the Navigate action, you should also specify an appropriate value for the header parameter.</span><span class="sxs-lookup"><span data-stu-id="5752d-219">When the postdata parameter is used in the Navigate action, you should also specify an appropriate value for the header parameter.</span></span> <span data-ttu-id="5752d-220">Example: Content-Type:application/x-www-form-urlencoded</span><span class="sxs-lookup"><span data-stu-id="5752d-220">Example: Content-Type:application/x-www-form-urlencoded</span></span><br />
<br />
<span data-ttu-id="5752d-221">If a <!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]: Couldn&#39;t find file ../includes/pn-unified-service-desk.md. -->[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]<!--END ERROR INCLUDE -->POST event triggers the Navigate action, the default value of this parameter should be header=[[header]+]</span><span class="sxs-lookup"><span data-stu-id="5752d-221">If a <!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]: Couldn&#39;t find file ../includes/pn-unified-service-desk.md. -->[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]<!--END ERROR INCLUDE -->POST event triggers the Navigate action, the default value of this parameter should be header=[[header]+]</span></span></td>
</tr>
</tbody>
</table>

### <a name="newcrmpage"></a><span data-ttu-id="5752d-222">New\_CRM\_Page</span><span class="sxs-lookup"><span data-stu-id="5752d-222">New\_CRM\_Page</span></span>

<span data-ttu-id="5752d-223">Creates a page for creating a new Dynamics 365 for Customer Engagement apps record of the entity specified, and treats the page as a popup from the specified hosted control.</span><span class="sxs-lookup"><span data-stu-id="5752d-223">Creates a page for creating a new Dynamics 365 for Customer Engagement apps record of the entity specified, and treats the page as a popup from the specified hosted control.</span></span> <span data-ttu-id="5752d-224">Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi trang tạo hồ sơ thực thể được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="5752d-224">The window navigation rules are evaluated to determine the location where the page to create the entity record is displayed.</span></span>

| <span data-ttu-id="5752d-225">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-225">Parameter</span></span>   | <span data-ttu-id="5752d-226">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-226">Description</span></span>                                                 |
|-------------|-------------------------------------------------------------|
| <span data-ttu-id="5752d-227">LogicalName</span><span class="sxs-lookup"><span data-stu-id="5752d-227">LogicalName</span></span> | <span data-ttu-id="5752d-228">Tên logic của thực thể để tạo phiên bản mới.</span><span class="sxs-lookup"><span data-stu-id="5752d-228">The logical name of the entity for creating a new instance.</span></span> |

> [!Note]
> <span data-ttu-id="5752d-229">Phần còn lại của các tham số nên bao gồm tên = cặp giá trị.</span><span class="sxs-lookup"><span data-stu-id="5752d-229">The rest of the parameters should consist of name=value pairs.</span></span> <span data-ttu-id="5752d-230">These are the additional pre-populated values in the form for creating a new record for the specified entity.</span><span class="sxs-lookup"><span data-stu-id="5752d-230">These are the additional pre-populated values in the form for creating a new record for the specified entity.</span></span> 

### <a name="opencrmpage"></a><span data-ttu-id="5752d-231">Open\_CRM\_Page</span><span class="sxs-lookup"><span data-stu-id="5752d-231">Open\_CRM\_Page</span></span>

<span data-ttu-id="5752d-232">Opens an existing instance of the entity specified and identified by the ID, and treats the page as a popup from the specified hosted control.</span><span class="sxs-lookup"><span data-stu-id="5752d-232">Opens an existing instance of the entity specified and identified by the ID, and treats the page as a popup from the specified hosted control.</span></span> <span data-ttu-id="5752d-233">Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi thư mục bật lên nên sẽ được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="5752d-233">The window navigation rules are evaluated to determine the location where the popup should be displayed.</span></span>

| <span data-ttu-id="5752d-234">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-234">Parameter</span></span>   | <span data-ttu-id="5752d-235">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-235">Description</span></span>                             |
|-------------|-----------------------------------------|
| <span data-ttu-id="5752d-236">LogicalName</span><span class="sxs-lookup"><span data-stu-id="5752d-236">LogicalName</span></span> | <span data-ttu-id="5752d-237">Tên logic của thực thể hợp lý của thực thể để mở.</span><span class="sxs-lookup"><span data-stu-id="5752d-237">The logical name of the entity to open.</span></span> |
| <span data-ttu-id="5752d-238">id</span><span class="sxs-lookup"><span data-stu-id="5752d-238">id</span></span>          | <span data-ttu-id="5752d-239">ID của hồ sơ thực thể để mở.</span><span class="sxs-lookup"><span data-stu-id="5752d-239">The ID of the entity record to open.</span></span>    |

### <a name="popup"></a><span data-ttu-id="5752d-240">Bật lên</span><span class="sxs-lookup"><span data-stu-id="5752d-240">Popup</span></span>

<span data-ttu-id="5752d-241">Bật lên URL từ kiểm soát tổ chức và chạy nguyên tắc điều hướng cửa sổ chống lại hình thức kiểm soát tổ chức để định tuyến bật lên đến vị trí thích hợp.</span><span class="sxs-lookup"><span data-stu-id="5752d-241">Pops up a URL from the hosted control and runs the window navigation rules against it for routing the popup to the appropriate location.</span></span>

| <span data-ttu-id="5752d-242">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-242">Parameter</span></span> | <span data-ttu-id="5752d-243">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-243">Description</span></span>                                                                                                        |
|-----------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5752d-244">url</span><span class="sxs-lookup"><span data-stu-id="5752d-244">url</span></span>       | <span data-ttu-id="5752d-245">Routes a popup from this hosted control using this URL as if it were a popup requested from the displayed control.</span><span class="sxs-lookup"><span data-stu-id="5752d-245">Routes a popup from this hosted control using this URL as if it were a popup requested from the displayed control.</span></span> |
| <span data-ttu-id="5752d-246">nền tảng</span><span class="sxs-lookup"><span data-stu-id="5752d-246">frame</span></span>     | <span data-ttu-id="5752d-247">The frame from which this popup originated.</span><span class="sxs-lookup"><span data-stu-id="5752d-247">The frame from which this popup originated.</span></span>                                                                        |

### <a name="realignwindow"></a><span data-ttu-id="5752d-248">RealignWindow</span><span class="sxs-lookup"><span data-stu-id="5752d-248">RealignWindow</span></span>

<span data-ttu-id="5752d-249">Hiển thị kiểm soát tổ chức tại một vị trí đã định trên màn hình.</span><span class="sxs-lookup"><span data-stu-id="5752d-249">Displays the hosted control at the specified location on a monitor.</span></span> <span data-ttu-id="5752d-250">Bạn có thể hiển thị kiểm soát tổ chức trên tối đa hai màn hình.</span><span class="sxs-lookup"><span data-stu-id="5752d-250">You can display hosted control on up to two monitors.</span></span> <span data-ttu-id="5752d-251">Hành động này áp dụng cho các phiên bản kiểm soát tổ chức được đặt cấu hình để đặt trên loại bảng điều khiển USDFloatingPanel hoặc USDFloatingToolPanel.</span><span class="sxs-lookup"><span data-stu-id="5752d-251">This action is applicable for hosted control instances that are configured to be placed on a USDFloatingPanel or USDFloatingToolPanel panel type.</span></span>

| <span data-ttu-id="5752d-252">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-252">Parameter</span></span> | <span data-ttu-id="5752d-253">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-253">Description</span></span>                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5752d-254">màn hình</span><span class="sxs-lookup"><span data-stu-id="5752d-254">screen</span></span>    | <span data-ttu-id="5752d-255">Chỉ định màn hình để hiển thị kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="5752d-255">Specifies the screen on which to display the hosted control.</span></span> <span data-ttu-id="5752d-256">Các giá trị hợp lệ là 1 hoặc 2.</span><span class="sxs-lookup"><span data-stu-id="5752d-256">Valid values are 1 or 2.</span></span> <span data-ttu-id="5752d-257">Nếu bạn không chỉ định tham số này, giá trị 1 sẽ được dùng theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="5752d-257">If you don’t specify this parameter, 1 is passed by default.</span></span>                                                                                  |
| <span data-ttu-id="5752d-258">trái</span><span class="sxs-lookup"><span data-stu-id="5752d-258">left</span></span>      | <span data-ttu-id="5752d-259">Chỉ định vị trí từ phía trái màn hình, theo tỷ lệ phần trăm, trên màn hình đích để hiển thị kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="5752d-259">Specifies the position, in percentage, from the left of the screen on the target monitor where the hosted control should be displayed.</span></span> <span data-ttu-id="5752d-260">Các giá trị hợp lệ là từ 0 đến 100.</span><span class="sxs-lookup"><span data-stu-id="5752d-260">Valid values are 0 through 100.</span></span> <span data-ttu-id="5752d-261">Nếu bạn không chỉ định tham số này, giá trị 0 sẽ được dùng theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="5752d-261">If you don’t specify this parameter, 0 is passed by default.</span></span> |
| <span data-ttu-id="5752d-262">trên cùng</span><span class="sxs-lookup"><span data-stu-id="5752d-262">top</span></span>       | <span data-ttu-id="5752d-263">Chỉ định vị trí từ phía trên cùng màn hình, theo tỷ lệ phần trăm, trên màn hình đích để hiển thị kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="5752d-263">Specifies the position, in percentage, from the top of the screen on the target monitor where the hosted control should be displayed.</span></span> <span data-ttu-id="5752d-264">Các giá trị hợp lệ là từ 0 đến 100.</span><span class="sxs-lookup"><span data-stu-id="5752d-264">Valid values are 0 through 100.</span></span> <span data-ttu-id="5752d-265">Nếu bạn không chỉ định tham số này, giá trị 0 sẽ được dùng theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="5752d-265">If you don’t specify this parameter, 0 is passed by default.</span></span>  |
| <span data-ttu-id="5752d-266">chiều rộng</span><span class="sxs-lookup"><span data-stu-id="5752d-266">width</span></span>     | <span data-ttu-id="5752d-267">Chỉ định chiều rộng của cửa sổ kiểm soát tổ chức theo tỷ lệ phần trăm trên màn hình đích.</span><span class="sxs-lookup"><span data-stu-id="5752d-267">Specifies the width, in percentage, of the hosted control window on the target monitor.</span></span> <span data-ttu-id="5752d-268">Các giá trị hợp lệ là từ 1 đến 100.</span><span class="sxs-lookup"><span data-stu-id="5752d-268">Valid values are 1 through 100.</span></span> <span data-ttu-id="5752d-269">Nếu bạn không chỉ định tham số này, giá trị 100 sẽ được dùng theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="5752d-269">If you don’t specify this parameter, 100 is passed by default.</span></span>                                              |
| <span data-ttu-id="5752d-270">chiều cao</span><span class="sxs-lookup"><span data-stu-id="5752d-270">height</span></span>    | <span data-ttu-id="5752d-271">Chỉ định chiều cao của cửa sổ kiểm soát tổ chức theo tỷ lệ phần trăm trên màn hình đích.</span><span class="sxs-lookup"><span data-stu-id="5752d-271">Specifies the height, in percentage, of the hosted control window on the target monitor.</span></span> <span data-ttu-id="5752d-272">Các giá trị hợp lệ là từ 1 đến 100.</span><span class="sxs-lookup"><span data-stu-id="5752d-272">Valid values are 1 through 100.</span></span> <span data-ttu-id="5752d-273">Nếu bạn không chỉ định tham số này, giá trị 100 sẽ được dùng theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="5752d-273">If you don’t specify this parameter, 100 is passed by default.</span></span>                                             |

### <a name="refresh"></a><span data-ttu-id="5752d-274">Refresh</span><span class="sxs-lookup"><span data-stu-id="5752d-274">Refresh</span></span>

<span data-ttu-id="5752d-275">This action refreshes the current page.</span><span class="sxs-lookup"><span data-stu-id="5752d-275">This action refreshes the current page.</span></span>

### <a name="runscript"></a><span data-ttu-id="5752d-276">Chạy mã lệnh</span><span class="sxs-lookup"><span data-stu-id="5752d-276">RunScript</span></span>  
 <span data-ttu-id="5752d-277">This action injects JavaScript into the main frame of the application.</span><span class="sxs-lookup"><span data-stu-id="5752d-277">This action injects JavaScript into the main frame of the application.</span></span> <span data-ttu-id="5752d-278">You should avoid using [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps client SDK calls with this action; instead, use the **RunXrmCommand** action.</span><span class="sxs-lookup"><span data-stu-id="5752d-278">You should avoid using [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps client SDK calls with this action; instead, use the **RunXrmCommand** action.</span></span>  
  
|<span data-ttu-id="5752d-279">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-279">Parameter</span></span>|<span data-ttu-id="5752d-280">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-280">Description</span></span>|  
|---------------|-----------------|  
||<span data-ttu-id="5752d-281">The data parameter is the JavaScript that will be injected into the form.</span><span class="sxs-lookup"><span data-stu-id="5752d-281">The data parameter is the JavaScript that will be injected into the form.</span></span> <span data-ttu-id="5752d-282">**Note:**  The replacement parameters can be used in the script, and they will be replaced before the script is executed.</span><span class="sxs-lookup"><span data-stu-id="5752d-282">**Note:**  The replacement parameters can be used in the script, and they will be replaced before the script is executed.</span></span>|
| <span data-ttu-id="5752d-283">Nền tảng</span><span class="sxs-lookup"><span data-stu-id="5752d-283">Frame</span></span> | <span data-ttu-id="5752d-284">When frames exist on the page, this parameter would specify the name of the frame to inject the JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5752d-284">When frames exist on the page, this parameter would specify the name of the frame to inject the JavaScript.</span></span> |

  
### <a name="runxrmcommand"></a><span data-ttu-id="5752d-285">Chạy lệnh Xrm</span><span class="sxs-lookup"><span data-stu-id="5752d-285">RunXrmCommand</span></span>  
 <span data-ttu-id="5752d-286">This action is used to run JavaScript code that uses [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps [Client API Reference](/dynamics365/customer-engagement/developer/clientapi/reference) into the Unified Interface Pages (entity forms and grids).</span><span class="sxs-lookup"><span data-stu-id="5752d-286">This action is used to run JavaScript code that uses [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps [Client API Reference](/dynamics365/customer-engagement/developer/clientapi/reference) into the Unified Interface Pages (entity forms and grids).</span></span> 

 <span data-ttu-id="5752d-287">You must configure the script as a function of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps JavaScript webResource.</span><span class="sxs-lookup"><span data-stu-id="5752d-287">You must configure the script as a function of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps JavaScript webResource.</span></span> <span data-ttu-id="5752d-288">The function's first parameter is a context parameter (reserved parameter) which may have one of the following values:</span><span class="sxs-lookup"><span data-stu-id="5752d-288">The function's first parameter is a context parameter (reserved parameter) which may have one of the following values:</span></span>

 - <span data-ttu-id="5752d-289">[FormContext](/dynamics365/customer-engagement/developer/clientapi/clientapi-form-context) on entity form pages</span><span class="sxs-lookup"><span data-stu-id="5752d-289">[FormContext](/dynamics365/customer-engagement/developer/clientapi/clientapi-form-context) on entity form pages</span></span>
 - <span data-ttu-id="5752d-290">[GridContext](/dynamics365/customer-engagement/developer/clientapi/clientapi-grid-context) on entity grid pages</span><span class="sxs-lookup"><span data-stu-id="5752d-290">[GridContext](/dynamics365/customer-engagement/developer/clientapi/clientapi-grid-context) on entity grid pages</span></span>
 - <span data-ttu-id="5752d-291">**undefined** on other pages</span><span class="sxs-lookup"><span data-stu-id="5752d-291">**undefined** on other pages</span></span>
  
|<span data-ttu-id="5752d-292">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-292">Parameter</span></span>|<span data-ttu-id="5752d-293">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-293">Description</span></span>|  
|---------------|-----------------|
| <span data-ttu-id="5752d-294">webResourceName</span><span class="sxs-lookup"><span data-stu-id="5752d-294">webResourceName</span></span> | <span data-ttu-id="5752d-295">Name of the web resource in which the JavaScript function you want to execute is present.</span><span class="sxs-lookup"><span data-stu-id="5752d-295">Name of the web resource in which the JavaScript function you want to execute is present.</span></span> |
| <span data-ttu-id="5752d-296">functionName</span><span class="sxs-lookup"><span data-stu-id="5752d-296">functionName</span></span> | <span data-ttu-id="5752d-297">Name of the function.</span><span class="sxs-lookup"><span data-stu-id="5752d-297">Name of the function.</span></span> |

<span data-ttu-id="5752d-298">The other parameters to the function are customer defined and can be used to pass Unified Service Desk’s replacement parameters at runtime.</span><span class="sxs-lookup"><span data-stu-id="5752d-298">The other parameters to the function are customer defined and can be used to pass Unified Service Desk’s replacement parameters at runtime.</span></span> <span data-ttu-id="5752d-299">This action accepts a list of optional parameters without keys.</span><span class="sxs-lookup"><span data-stu-id="5752d-299">This action accepts a list of optional parameters without keys.</span></span> <span data-ttu-id="5752d-300">The list of optional parameters are passed as arguments in the same order from second position after context replacement at runtime.</span><span class="sxs-lookup"><span data-stu-id="5752d-300">The list of optional parameters are passed as arguments in the same order from second position after context replacement at runtime.</span></span>

#### <a name="example"></a><span data-ttu-id="5752d-301">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="5752d-301">Example</span></span>

<span data-ttu-id="5752d-302">You want to execute **RunXrmCommand** action to fill the form attributes of a entity form, where the entity form is hosted by Unified Interface type of hosted control.</span><span class="sxs-lookup"><span data-stu-id="5752d-302">You want to execute **RunXrmCommand** action to fill the form attributes of a entity form, where the entity form is hosted by Unified Interface type of hosted control.</span></span> <span data-ttu-id="5752d-303">The value you want to fill in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]'s perspective  is a replacement parameter - `[[$Context.Key1]]`.</span><span class="sxs-lookup"><span data-stu-id="5752d-303">The value you want to fill in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]'s perspective  is a replacement parameter - `[[$Context.Key1]]`.</span></span>

<span data-ttu-id="5752d-304">In order to execute the action, you need to write JavaScript type web resource (say webResource1), and then write a function in the web resource.</span><span class="sxs-lookup"><span data-stu-id="5752d-304">In order to execute the action, you need to write JavaScript type web resource (say webResource1), and then write a function in the web resource.</span></span>

```JavaScript
function fillAttributeValue(context, attrValue)
{
 context.getAttribute(<attributeName>).setValue(attrValue);
}   
```

<span data-ttu-id="5752d-305">You need to configure the data in the action call as follows:</span><span class="sxs-lookup"><span data-stu-id="5752d-305">You need to configure the data in the action call as follows:</span></span>

```
webResourceName = webResource1
functionName = fillAttributeValue
‘[[$Context.Key1]]’
```
> [!Note]
> <span data-ttu-id="5752d-306">In the above example, observe the quotes around the replacement parameter - `[[$Context.Key1]]`.</span><span class="sxs-lookup"><span data-stu-id="5752d-306">In the above example, observe the quotes around the replacement parameter - `[[$Context.Key1]]`.</span></span> [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="5752d-307">considers only the value of the parameter (not the data type) and passes all the characters in context replaced value to the JavaScript function.</span><span class="sxs-lookup"><span data-stu-id="5752d-307">considers only the value of the parameter (not the data type) and passes all the characters in context replaced value to the JavaScript function.</span></span> <span data-ttu-id="5752d-308">You must be cautious and take care of the data type while configuring.</span><span class="sxs-lookup"><span data-stu-id="5752d-308">You must be cautious and take care of the data type while configuring.</span></span>

### <a name="setsize"></a><span data-ttu-id="5752d-309">SetSize</span><span class="sxs-lookup"><span data-stu-id="5752d-309">SetSize</span></span>

<span data-ttu-id="5752d-310">This action explicitly sets the width and height of the hosted control.</span><span class="sxs-lookup"><span data-stu-id="5752d-310">This action explicitly sets the width and height of the hosted control.</span></span> <span data-ttu-id="5752d-311">Quá trình này đặc biệt hữu ích khi sử dụng tính năng "tự động" trong bố cục bảng điều khiển của bạn.</span><span class="sxs-lookup"><span data-stu-id="5752d-311">This is particularly useful when using "auto" in your panel layouts.</span></span>

| <span data-ttu-id="5752d-312">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-312">Parameter</span></span> | <span data-ttu-id="5752d-313">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-313">Description</span></span>                       |
|-----------|-----------------------------------|
| <span data-ttu-id="5752d-314">chiều rộng</span><span class="sxs-lookup"><span data-stu-id="5752d-314">width</span></span>     | <span data-ttu-id="5752d-315">The width of the hosted control.</span><span class="sxs-lookup"><span data-stu-id="5752d-315">The width of the hosted control.</span></span>  |
| <span data-ttu-id="5752d-316">chiều cao</span><span class="sxs-lookup"><span data-stu-id="5752d-316">height</span></span>    | <span data-ttu-id="5752d-317">The height of the hosted control.</span><span class="sxs-lookup"><span data-stu-id="5752d-317">The height of the hosted control.</span></span> |

### <a name="saveandclose"></a><span data-ttu-id="5752d-318">Lưu và Đóng</span><span class="sxs-lookup"><span data-stu-id="5752d-318">SaveAndClose</span></span>

<span data-ttu-id="5752d-319">This action saves the dirty data on the Dynamics 365 for Customer Engagement apps form, and closes the hosted control.</span><span class="sxs-lookup"><span data-stu-id="5752d-319">This action saves the dirty data on the Dynamics 365 for Customer Engagement apps form, and closes the hosted control.</span></span>

### <a name="saveall"></a><span data-ttu-id="5752d-320">Lưu tất cả</span><span class="sxs-lookup"><span data-stu-id="5752d-320">SaveAll</span></span>

<span data-ttu-id="5752d-321">This action saves all forms in hosted control that allows multiple pages to be displayed (**Allow Multiple Pages** = Yes).</span><span class="sxs-lookup"><span data-stu-id="5752d-321">This action saves all forms in hosted control that allows multiple pages to be displayed (**Allow Multiple Pages** = Yes).</span></span> <span data-ttu-id="5752d-322">If the hosted control allows only a single page to be displayed (**Allow Multiple Pages** = No), this is equivalent to the **Save** action.</span><span class="sxs-lookup"><span data-stu-id="5752d-322">If the hosted control allows only a single page to be displayed (**Allow Multiple Pages** = No), this is equivalent to the **Save** action.</span></span>

### <a name="save"></a><span data-ttu-id="5752d-323">Lưu</span><span class="sxs-lookup"><span data-stu-id="5752d-323">Save</span></span>

<span data-ttu-id="5752d-324">This action saves the current Unified Interface Page.</span><span class="sxs-lookup"><span data-stu-id="5752d-324">This action saves the current Unified Interface Page.</span></span>

## <a name="predefined-events"></a><span data-ttu-id="5752d-325">Sự kiện được xác định trước</span><span class="sxs-lookup"><span data-stu-id="5752d-325">Predefined events</span></span>

<span data-ttu-id="5752d-326">The following predefined events are associated with this hosted control type.</span><span class="sxs-lookup"><span data-stu-id="5752d-326">The following predefined events are associated with this hosted control type.</span></span>

### <a name="activeclosed"></a><span data-ttu-id="5752d-327">Hiện hoạt đã đóng</span><span class="sxs-lookup"><span data-stu-id="5752d-327">ActiveClosed</span></span>

<span data-ttu-id="5752d-328">Occurs when the active hosted control is closed using the [CloseActive](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/crm-page-hosted-control#CloseActive) action.</span><span class="sxs-lookup"><span data-stu-id="5752d-328">Occurs when the active hosted control is closed using the [CloseActive](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/unified-service-desk/crm-page-hosted-control#CloseActive) action.</span></span>  

| <span data-ttu-id="5752d-329">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-329">Parameter</span></span> | <span data-ttu-id="5752d-330">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-330">Description</span></span>                                                          |
|-----------|----------------------------------------------------------------------|
| <span data-ttu-id="5752d-331">url</span><span class="sxs-lookup"><span data-stu-id="5752d-331">url</span></span>       | <span data-ttu-id="5752d-332">The URL that was displayed in the hosted control when it was closed.</span><span class="sxs-lookup"><span data-stu-id="5752d-332">The URL that was displayed in the hosted control when it was closed.</span></span> |

### <a name="dataready"></a><span data-ttu-id="5752d-333">DataReady</span><span class="sxs-lookup"><span data-stu-id="5752d-333">DataReady</span></span>

<span data-ttu-id="5752d-334">Occurs as soon as the related information for an entity record is loaded in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context.</span><span class="sxs-lookup"><span data-stu-id="5752d-334">Occurs as soon as the related information for an entity record is loaded in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context.</span></span> <span data-ttu-id="5752d-335">This event occurs before the **PageReadyFor** event.</span><span class="sxs-lookup"><span data-stu-id="5752d-335">This event occurs before the **PageReadyFor** event.</span></span> <span data-ttu-id="5752d-336">If the **Pre-Fetch Data** option is selected for the control instance then this event occurs as soon as the entity data is fetched in a separate parallel call to the server and will not wait for the full page to finish loading.</span><span class="sxs-lookup"><span data-stu-id="5752d-336">If the **Pre-Fetch Data** option is selected for the control instance then this event occurs as soon as the entity data is fetched in a separate parallel call to the server and will not wait for the full page to finish loading.</span></span> <span data-ttu-id="5752d-337">The entity data is pre-fetched and the **DataReady** event is fired for inline navigations as well.</span><span class="sxs-lookup"><span data-stu-id="5752d-337">The entity data is pre-fetched and the **DataReady** event is fired for inline navigations as well.</span></span>

### <a name="refreshrequested"></a><span data-ttu-id="5752d-338">Làm mới được yêu cầu</span><span class="sxs-lookup"><span data-stu-id="5752d-338">RefreshRequested</span></span>

<span data-ttu-id="5752d-339">Occurs when refresh is requested on the current page.</span><span class="sxs-lookup"><span data-stu-id="5752d-339">Occurs when refresh is requested on the current page.</span></span> <span data-ttu-id="5752d-340">Làm mới có thể được yêu cầu hoặc bằng cách bấm phím F5 hoặc gọi hành động làm mới của ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="5752d-340">Refresh can be requested either by pressing the F5 key or calling the Refresh action by the application.</span></span>

| <span data-ttu-id="5752d-341">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-341">Parameter</span></span> | <span data-ttu-id="5752d-342">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-342">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="5752d-343">url</span><span class="sxs-lookup"><span data-stu-id="5752d-343">url</span></span>       | <span data-ttu-id="5752d-344">The URL displayed when refresh was requested.</span><span class="sxs-lookup"><span data-stu-id="5752d-344">The URL displayed when refresh was requested.</span></span> |

### <a name="saved"></a><span data-ttu-id="5752d-345">Đã lưu</span><span class="sxs-lookup"><span data-stu-id="5752d-345">Saved</span></span>

<span data-ttu-id="5752d-346">Occurs after a record in the Dynamics 365 for Customer Engagement apps page is saved.</span><span class="sxs-lookup"><span data-stu-id="5752d-346">Occurs after a record in the Dynamics 365 for Customer Engagement apps page is saved.</span></span>

| <span data-ttu-id="5752d-347">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-347">Parameter</span></span> | <span data-ttu-id="5752d-348">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-348">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="5752d-349">id mới</span><span class="sxs-lookup"><span data-stu-id="5752d-349">newId</span></span>     | <span data-ttu-id="5752d-350">The ID assigned to the newly created record.</span><span class="sxs-lookup"><span data-stu-id="5752d-350">The ID assigned to the newly created record.</span></span> |

### <a name="navigationrequested"></a><span data-ttu-id="5752d-351">NavigationRequested</span><span class="sxs-lookup"><span data-stu-id="5752d-351">NavigationRequested</span></span>

<span data-ttu-id="5752d-352">Occurs when the navigation happens within Unified Interface apps</span><span class="sxs-lookup"><span data-stu-id="5752d-352">Occurs when the navigation happens within Unified Interface apps</span></span>

| <span data-ttu-id="5752d-353">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-353">Parameter</span></span> | <span data-ttu-id="5752d-354">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-354">Description</span></span>                       |
|-----------|-----------------------------------|
| <span data-ttu-id="5752d-355">url</span><span class="sxs-lookup"><span data-stu-id="5752d-355">url</span></span>       | <span data-ttu-id="5752d-356">The URL of the page navigated to.</span><span class="sxs-lookup"><span data-stu-id="5752d-356">The URL of the page navigated to.</span></span> |

### <a name="pageready"></a><span data-ttu-id="5752d-357">PageReady</span><span class="sxs-lookup"><span data-stu-id="5752d-357">PageReady</span></span>

<span data-ttu-id="5752d-358">Occurs when the page has finished loading.</span><span class="sxs-lookup"><span data-stu-id="5752d-358">Occurs when the page has finished loading.</span></span> <span data-ttu-id="5752d-359">On a Unified Interface Page type of hosted control, this event occurs after the data has been saved to the replacement parameter list.</span><span class="sxs-lookup"><span data-stu-id="5752d-359">On a Unified Interface Page type of hosted control, this event occurs after the data has been saved to the replacement parameter list.</span></span>

| <span data-ttu-id="5752d-360">Tham số</span><span class="sxs-lookup"><span data-stu-id="5752d-360">Parameter</span></span> | <span data-ttu-id="5752d-361">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5752d-361">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="5752d-362">url</span><span class="sxs-lookup"><span data-stu-id="5752d-362">url</span></span>       | <span data-ttu-id="5752d-363">The URL of the page that has finished loading.</span><span class="sxs-lookup"><span data-stu-id="5752d-363">The URL of the page that has finished loading.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5752d-364">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="5752d-364">See also</span></span>

<span data-ttu-id="5752d-365">[Support for Unified Interface Apps in Unified Service Desk](../unified-service-desk/admin/Support-unified-interfaces-apps-usd.md)
[Unified Service Desk and Unified Interface Configuration Walkthroughs](../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md)
[Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) 
[Walkthrough 2: Display an external webpage in your agent application](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="5752d-365">[Support for Unified Interface Apps in Unified Service Desk](../unified-service-desk/admin/Support-unified-interfaces-apps-usd.md)
[Unified Service Desk and Unified Interface Configuration Walkthroughs](../unified-service-desk/unified-service-desk-unified-interface-configuration-walkthroughs.md)
[Walkthrough 1: Build a simple agent application for Unified Interface Apps](../unified-service-desk/walkthrough1-unified-interface-build-a-simple-agent-application.md) 
[Walkthrough 2: Display an external webpage in your agent application](../unified-service-desk/walkthrough2-unified-interface-display-an-external-webpage-in-your-agent-application.md) </span></span>  
<span data-ttu-id="5752d-366">[Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="5752d-366">[Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) records in your agent application](../unified-service-desk/walkthrough3-unified-interface-display-microsoft-dynamics-365-records-in-your-agent-application.md) </span></span>  
<span data-ttu-id="5752d-367">[Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md) </span><span class="sxs-lookup"><span data-stu-id="5752d-367">[Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps (Unified Interface apps) record in a session in your agent application](../unified-service-desk/walkthrough4-unified-interface-display-dynamics-365-record-session-agent-application.md) </span></span>  
<span data-ttu-id="5752d-368">[Cách 5: Hiển thị thông tin phiên bổ sung bằng cách hiển thị tên và dữ liệu tổng quan về phiên](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md) </span><span class="sxs-lookup"><span data-stu-id="5752d-368">[Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough5-unified-interface-display-enhanced-session-information-displaying-session-name-overview-data.md) </span></span>  
<span data-ttu-id="5752d-369">[Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md)
[Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)</span><span class="sxs-lookup"><span data-stu-id="5752d-369">[Walkthrough 6: Configure the Debugger hosted control in your agent application](../unified-service-desk/walkthrough6-unified-interface-configure-debugger-hosted-control-agent-application.md)
[Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough7-unified-interface-configure-agent-scripting-agent-application.md)</span></span> 
