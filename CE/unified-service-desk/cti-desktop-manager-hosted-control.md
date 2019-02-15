---
title: CTI Desktop Manager (Hosted Control) | MicrosoftDocs
description: Learn about using the CTI Desktop Manager hosted control type to plug in a computer telephony integration (CTI) adapter into Unified Service Desk to handle screen popping, call routing, softphone control, and other CTI functionalities.
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
ms.assetid: 9fb92472-39af-4816-84eb-4d5ffb8b4b4f
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 4c4ac1f0cb882b892b948c1ec447132dd8c1dbb0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387665"
---
# <a name="cti-desktop-manager-hosted-control"></a><span data-ttu-id="016c1-103">CTI Desktop Manager (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="016c1-103">CTI Desktop Manager (Hosted Control)</span></span>
<span data-ttu-id="016c1-104">Use the **CTI Desktop Manager** hosted control type to plug in a computer telephony integration (CTI) adapter into [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to handle screen popping, call routing, softphone control, and other CTI functionalities.</span><span class="sxs-lookup"><span data-stu-id="016c1-104">Use the **CTI Desktop Manager** hosted control type to plug in a computer telephony integration (CTI) adapter into [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to handle screen popping, call routing, softphone control, and other CTI functionalities.</span></span>  

<a name="Create"></a>   
## <a name="create-a-cti-desktop-manager-hosted-control"></a><span data-ttu-id="016c1-105">Tạo kiểm soát tổ chức Trình quản lý Máy tính để bàn CTI</span><span class="sxs-lookup"><span data-stu-id="016c1-105">Create a CTI Desktop Manager hosted control</span></span>  
 <span data-ttu-id="016c1-106">For information about creating a CTI Desktop Manager and configuring the corresponding hosted control, see [Create a CTI Desktop Manager](../unified-service-desk/create-cti-desktop-manager.md).</span><span class="sxs-lookup"><span data-stu-id="016c1-106">For information about creating a CTI Desktop Manager and configuring the corresponding hosted control, see [Create a CTI Desktop Manager](../unified-service-desk/create-cti-desktop-manager.md).</span></span>  

<a name="Actions"></a>   
## <a name="predefined-uii-actions"></a><span data-ttu-id="016c1-107">Predefined UII actions</span><span class="sxs-lookup"><span data-stu-id="016c1-107">Predefined UII actions</span></span>  
 <span data-ttu-id="016c1-108">These are the predefined actions for this hosted control type.</span><span class="sxs-lookup"><span data-stu-id="016c1-108">These are the predefined actions for this hosted control type.</span></span>  

<a name="Close"></a>   
### <a name="close"></a><span data-ttu-id="016c1-109">Đóng</span><span class="sxs-lookup"><span data-stu-id="016c1-109">Close</span></span>  
 <span data-ttu-id="016c1-110">This action is used to close the hosted control.</span><span class="sxs-lookup"><span data-stu-id="016c1-110">This action is used to close the hosted control.</span></span> <span data-ttu-id="016c1-111">Unlike the **CloseActive** action, if this tab (hosted control) is displaying more than one page, it will close all the pages displayed in the tab in your agent application.</span><span class="sxs-lookup"><span data-stu-id="016c1-111">Unlike the **CloseActive** action, if this tab (hosted control) is displaying more than one page, it will close all the pages displayed in the tab in your agent application.</span></span>  

### <a name="closeandprompt"></a><span data-ttu-id="016c1-112">Đóng và Nhắc</span><span class="sxs-lookup"><span data-stu-id="016c1-112">CloseAndPrompt</span></span>  
 <span data-ttu-id="016c1-113">This action closes the hosted control, but prompts the user to save or abandon the changes before closing.</span><span class="sxs-lookup"><span data-stu-id="016c1-113">This action closes the hosted control, but prompts the user to save or abandon the changes before closing.</span></span>  

### <a name="disabletoolbarbutton"></a><span data-ttu-id="016c1-114">Tắt nút thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="016c1-114">DisableToolbarButton</span></span>  
 <span data-ttu-id="016c1-115">Hành động này vô hiệu hóa nút thanh công cụ được chỉ định trên thanh công cụ trong ứng dụng tổng đài viên của bạn.</span><span class="sxs-lookup"><span data-stu-id="016c1-115">This action disables the specified toolbar button on the toolbar in your agent application.</span></span>  

|<span data-ttu-id="016c1-116">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-116">Parameter</span></span>|<span data-ttu-id="016c1-117">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-117">Description</span></span>|  
|---------------|-----------------|  
||<span data-ttu-id="016c1-118">Tên của nút thanh công cụ để vô hiệu hóa.</span><span class="sxs-lookup"><span data-stu-id="016c1-118">Name of the toolbar button to disable.</span></span>|  

### <a name="enabletoolbarbutton"></a><span data-ttu-id="016c1-119">Bật nút thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="016c1-119">EnableToolbarButton</span></span>  
 <span data-ttu-id="016c1-120">Hành động này bật nút thanh công cụ được chỉ định trên thanh công cụ trong ứng dụng tổng đài viên của bạn.</span><span class="sxs-lookup"><span data-stu-id="016c1-120">This action enables the specified toolbar button on the toolbar in your agent application.</span></span>  

|<span data-ttu-id="016c1-121">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-121">Parameter</span></span>|<span data-ttu-id="016c1-122">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-122">Description</span></span>|  
|---------------|-----------------|  
||<span data-ttu-id="016c1-123">Name of the toolbar button to enable.</span><span class="sxs-lookup"><span data-stu-id="016c1-123">Name of the toolbar button to enable.</span></span>|  

### <a name="find"></a><span data-ttu-id="016c1-124">Find</span><span class="sxs-lookup"><span data-stu-id="016c1-124">Find</span></span>  
 <span data-ttu-id="016c1-125">Navigate to the quick find list view of the specified entity.</span><span class="sxs-lookup"><span data-stu-id="016c1-125">Navigate to the quick find list view of the specified entity.</span></span>  

|<span data-ttu-id="016c1-126">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-126">Parameter</span></span>|<span data-ttu-id="016c1-127">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-127">Description</span></span>|  
|---------------|-----------------|  
||<span data-ttu-id="016c1-128">The data parameter should specify the entity logical name of the quick find list view to display.</span><span class="sxs-lookup"><span data-stu-id="016c1-128">The data parameter should specify the entity logical name of the quick find list view to display.</span></span> <span data-ttu-id="016c1-129">There are some special case values:</span><span class="sxs-lookup"><span data-stu-id="016c1-129">There are some special case values:</span></span><br /><br /> <span data-ttu-id="016c1-130">-   Use **case** or **incident** to display the quick find list view for cases.</span><span class="sxs-lookup"><span data-stu-id="016c1-130">-   Use **case** or **incident** to display the quick find list view for cases.</span></span><br /><span data-ttu-id="016c1-131">-   Use **advfind** to display the advanced find view.</span><span class="sxs-lookup"><span data-stu-id="016c1-131">-   Use **advfind** to display the advanced find view.</span></span><br /><span data-ttu-id="016c1-132">-   Use **activities** or **activity** to display the quick find list view for activities.</span><span class="sxs-lookup"><span data-stu-id="016c1-132">-   Use **activities** or **activity** to display the quick find list view for activities.</span></span>|  

### <a name="fireevent"></a><span data-ttu-id="016c1-133">FireEvent</span><span class="sxs-lookup"><span data-stu-id="016c1-133">FireEvent</span></span>  
 <span data-ttu-id="016c1-134">Fires a user-defined event from this hosted control.</span><span class="sxs-lookup"><span data-stu-id="016c1-134">Fires a user-defined event from this hosted control.</span></span>  

|<span data-ttu-id="016c1-135">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-135">Parameter</span></span>|<span data-ttu-id="016c1-136">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-136">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="016c1-137">tên</span><span class="sxs-lookup"><span data-stu-id="016c1-137">name</span></span>|<span data-ttu-id="016c1-138">Tên của sự kiện do người dùng xác định.</span><span class="sxs-lookup"><span data-stu-id="016c1-138">Name of the user-defined event.</span></span>|  

 <span data-ttu-id="016c1-139">Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này.</span><span class="sxs-lookup"><span data-stu-id="016c1-139">All subsequent name=value pairs become the parameters to the event.</span></span> <span data-ttu-id="016c1-140">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span><span class="sxs-lookup"><span data-stu-id="016c1-140">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span></span>  

### <a name="goback"></a><span data-ttu-id="016c1-141">Quay lại</span><span class="sxs-lookup"><span data-stu-id="016c1-141">GoBack</span></span>  
 <span data-ttu-id="016c1-142">This action is equivalent to clicking the back button on the browser instance.</span><span class="sxs-lookup"><span data-stu-id="016c1-142">This action is equivalent to clicking the back button on the browser instance.</span></span>  

### <a name="goforward"></a><span data-ttu-id="016c1-143">Chuyển về phía trước</span><span class="sxs-lookup"><span data-stu-id="016c1-143">GoForward</span></span>  
 <span data-ttu-id="016c1-144">This action is equivalent to clicking the forward button on the browser instance.</span><span class="sxs-lookup"><span data-stu-id="016c1-144">This action is equivalent to clicking the forward button on the browser instance.</span></span>  

### <a name="gohome"></a><span data-ttu-id="016c1-145">Về Trang chủ</span><span class="sxs-lookup"><span data-stu-id="016c1-145">GoHome</span></span>  
 <span data-ttu-id="016c1-146">This action goes to the initial URL specified for this browser instance.</span><span class="sxs-lookup"><span data-stu-id="016c1-146">This action goes to the initial URL specified for this browser instance.</span></span>  

### <a name="loadarea"></a><span data-ttu-id="016c1-147">Vùng tải</span><span class="sxs-lookup"><span data-stu-id="016c1-147">LoadArea</span></span>  
 <span data-ttu-id="016c1-148">This action loads a specific area from [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="016c1-148">This action loads a specific area from [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span></span> <span data-ttu-id="016c1-149">This is equivalent to selecting an area in the navigation pane (such as Sales, Service, and Marketing).</span><span class="sxs-lookup"><span data-stu-id="016c1-149">This is equivalent to selecting an area in the navigation pane (such as Sales, Service, and Marketing).</span></span> <span data-ttu-id="016c1-150">Các tham số chỉ là tên của vùng nhấp vào.</span><span class="sxs-lookup"><span data-stu-id="016c1-150">The only parameter is the name of the area to click.</span></span> <span data-ttu-id="016c1-151">Ví dụ: **Vùng dịch vụ**.</span><span class="sxs-lookup"><span data-stu-id="016c1-151">For example: **areaService**.</span></span>  

|<span data-ttu-id="016c1-152">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-152">Parameter</span></span>|<span data-ttu-id="016c1-153">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-153">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="016c1-154">nền tảng</span><span class="sxs-lookup"><span data-stu-id="016c1-154">frame</span></span>|<span data-ttu-id="016c1-155">Tên nền tảng chịu ảnh hưởng.</span><span class="sxs-lookup"><span data-stu-id="016c1-155">The name of the frame to affect.</span></span> <span data-ttu-id="016c1-156">If no name is specified, it will automatically target the first frame found on the page.</span><span class="sxs-lookup"><span data-stu-id="016c1-156">If no name is specified, it will automatically target the first frame found on the page.</span></span>|  

<a name="MoveToPanel"></a>   
### <a name="movetopanel"></a><span data-ttu-id="016c1-157">MoveToPanel</span><span class="sxs-lookup"><span data-stu-id="016c1-157">MoveToPanel</span></span>  
 <span data-ttu-id="016c1-158">This action is used to move hosted controls between panels at runtime.</span><span class="sxs-lookup"><span data-stu-id="016c1-158">This action is used to move hosted controls between panels at runtime.</span></span>  

|<span data-ttu-id="016c1-159">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-159">Parameter</span></span>|<span data-ttu-id="016c1-160">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-160">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="016c1-161">ứng dụng</span><span class="sxs-lookup"><span data-stu-id="016c1-161">app</span></span>|<span data-ttu-id="016c1-162">Name of the hosted control to be moved.</span><span class="sxs-lookup"><span data-stu-id="016c1-162">Name of the hosted control to be moved.</span></span>|  
|<span data-ttu-id="016c1-163">bảng điều khiển</span><span class="sxs-lookup"><span data-stu-id="016c1-163">panel</span></span>|<span data-ttu-id="016c1-164">Target panel for the hosted control.</span><span class="sxs-lookup"><span data-stu-id="016c1-164">Target panel for the hosted control.</span></span>|  

### <a name="navigate"></a><span data-ttu-id="016c1-165">Navigate</span><span class="sxs-lookup"><span data-stu-id="016c1-165">Navigate</span></span>  
 <span data-ttu-id="016c1-166">This action is used to navigate to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps url.</span><span class="sxs-lookup"><span data-stu-id="016c1-166">This action is used to navigate to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps url.</span></span>  


|     <span data-ttu-id="016c1-167">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-167">Parameter</span></span>     |                                                                                                                                                                                                                                       <span data-ttu-id="016c1-168">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-168">Description</span></span>                                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        <span data-ttu-id="016c1-169">url</span><span class="sxs-lookup"><span data-stu-id="016c1-169">url</span></span>        |                                                                                                                                                                                                                  <span data-ttu-id="016c1-170">The URL to navigate to.</span><span class="sxs-lookup"><span data-stu-id="016c1-170">The URL to navigate to.</span></span> <span data-ttu-id="016c1-171">This is a mandatory parameter.</span><span class="sxs-lookup"><span data-stu-id="016c1-171">This is a mandatory parameter.</span></span>                                                                                                                                                                                                                  |
|      <span data-ttu-id="016c1-172">Noscan</span><span class="sxs-lookup"><span data-stu-id="016c1-172">Noscan</span></span>       |                                                                                                                                                                                           <span data-ttu-id="016c1-173">If this parameter is supplied and **True**, the data parameters will not be captured from the page.</span><span class="sxs-lookup"><span data-stu-id="016c1-173">If this parameter is supplied and **True**, the data parameters will not be captured from the page.</span></span>                                                                                                                                                                                            |
|  <span data-ttu-id="016c1-174">HideCommandBar</span><span class="sxs-lookup"><span data-stu-id="016c1-174">HideCommandBar</span></span>   |                                                                                                                                                        <span data-ttu-id="016c1-175">If this parameter is supplied and **True**, the inner frame will be displayed without loading the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps command bar.</span><span class="sxs-lookup"><span data-stu-id="016c1-175">If this parameter is supplied and **True**, the inner frame will be displayed without loading the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps command bar.</span></span>                                                                                                                                                        |
| <span data-ttu-id="016c1-176">HideNavigationBar</span><span class="sxs-lookup"><span data-stu-id="016c1-176">HideNavigationBar</span></span> |                                                                                                                                                          <span data-ttu-id="016c1-177">If this parameter is supplied and **True**, the form will be displayed without loading the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps navigation bar.</span><span class="sxs-lookup"><span data-stu-id="016c1-177">If this parameter is supplied and **True**, the form will be displayed without loading the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps navigation bar.</span></span>                                                                                                                                                          |
|       <span data-ttu-id="016c1-178">Nền tảng</span><span class="sxs-lookup"><span data-stu-id="016c1-178">Frame</span></span>       |                                                                                                                                                                          <span data-ttu-id="016c1-179">When frames exist on the page, this parameter would specify the name of the frame to navigate, rather than navigating the main window.</span><span class="sxs-lookup"><span data-stu-id="016c1-179">When frames exist on the page, this parameter would specify the name of the frame to navigate, rather than navigating the main window.</span></span>                                                                                                                                                                          |
|     <span data-ttu-id="016c1-180">postdata</span><span class="sxs-lookup"><span data-stu-id="016c1-180">postdata</span></span>      |                <span data-ttu-id="016c1-181">Data that is sent to the server as part of an HTTPPOST transaction.</span><span class="sxs-lookup"><span data-stu-id="016c1-181">Data that is sent to the server as part of an HTTPPOST transaction.</span></span> <span data-ttu-id="016c1-182">A POST transaction is typically used to send data gathered by an HTML page.</span><span class="sxs-lookup"><span data-stu-id="016c1-182">A POST transaction is typically used to send data gathered by an HTML page.</span></span> <span data-ttu-id="016c1-183">In [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], this data can be received from any event triggered using "<http://event/?>".</span><span class="sxs-lookup"><span data-stu-id="016c1-183">In [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], this data can be received from any event triggered using "<http://event/?>".</span></span> <span data-ttu-id="016c1-184">Ví dụ: `[[postdata]+]`</span><span class="sxs-lookup"><span data-stu-id="016c1-184">Example: `[[postdata]+]`</span></span><br /><br /> <span data-ttu-id="016c1-185">Alternatively, the data can be passed as an encoded string with its header type in the intended format.</span><span class="sxs-lookup"><span data-stu-id="016c1-185">Alternatively, the data can be passed as an encoded string with its header type in the intended format.</span></span>                 |
|      <span data-ttu-id="016c1-186">tiêu đề</span><span class="sxs-lookup"><span data-stu-id="016c1-186">header</span></span>       | <span data-ttu-id="016c1-187">Giá trị chuỗi chứa tiêu đề HTTP bổ sung để gửi tới máy chủ.</span><span class="sxs-lookup"><span data-stu-id="016c1-187">A string value that contains additional HTTP headers to send to the server.</span></span> <span data-ttu-id="016c1-188">When the `postdata` parameter is used in the `Navigate` action, you should also specify an appropriate value for the `header` parameter.</span><span class="sxs-lookup"><span data-stu-id="016c1-188">When the `postdata` parameter is used in the `Navigate` action, you should also specify an appropriate value for the `header` parameter.</span></span> <span data-ttu-id="016c1-189">Ví dụ: `Content-Type:application/x-www-form-urlencoded`</span><span class="sxs-lookup"><span data-stu-id="016c1-189">Example: `Content-Type:application/x-www-form-urlencoded`</span></span><br /><br /> <span data-ttu-id="016c1-190">If a [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]POST event triggers the `Navigate` action, the default value of this parameter should be `header=[[header]+]`</span><span class="sxs-lookup"><span data-stu-id="016c1-190">If a [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]POST event triggers the `Navigate` action, the default value of this parameter should be `header=[[header]+]`</span></span> |

### <a name="newcrmpage"></a><span data-ttu-id="016c1-191">New_CRM_Page</span><span class="sxs-lookup"><span data-stu-id="016c1-191">New_CRM_Page</span></span>  
 <span data-ttu-id="016c1-192">Creates a page for creating a new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps record of the entity specified, and treats the page as a popup from the specified hosted control.</span><span class="sxs-lookup"><span data-stu-id="016c1-192">Creates a page for creating a new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps record of the entity specified, and treats the page as a popup from the specified hosted control.</span></span> <span data-ttu-id="016c1-193">Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi trang tạo hồ sơ thực thể được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="016c1-193">The window navigation rules are evaluated to determine the location where the page to create the entity record is displayed.</span></span>  

|<span data-ttu-id="016c1-194">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-194">Parameter</span></span>|<span data-ttu-id="016c1-195">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-195">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="016c1-196">LogicalName</span><span class="sxs-lookup"><span data-stu-id="016c1-196">LogicalName</span></span>|<span data-ttu-id="016c1-197">Tên logic của thực thể để tạo phiên bản mới.</span><span class="sxs-lookup"><span data-stu-id="016c1-197">The logical name of the entity for creating a new instance.</span></span>|  

> [!NOTE]
>  <span data-ttu-id="016c1-198">Phần còn lại của các tham số nên bao gồm tên = cặp giá trị.</span><span class="sxs-lookup"><span data-stu-id="016c1-198">The rest of the parameters should consist of name=value pairs.</span></span> <span data-ttu-id="016c1-199">These are the additional pre-populated values in the form for creating a new record for the specified entity.</span><span class="sxs-lookup"><span data-stu-id="016c1-199">These are the additional pre-populated values in the form for creating a new record for the specified entity.</span></span> <span data-ttu-id="016c1-200">For more information about using this action, see step 4 in [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="016c1-200">For more information about using this action, see step 4 in [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md).</span></span>  

### <a name="opencrmpage"></a><span data-ttu-id="016c1-201">Open_CRM_Page</span><span class="sxs-lookup"><span data-stu-id="016c1-201">Open_CRM_Page</span></span>  
 <span data-ttu-id="016c1-202">Opens an existing instance of the entity specified and identified by the ID, and treats the page as a popup from the specified hosted control.</span><span class="sxs-lookup"><span data-stu-id="016c1-202">Opens an existing instance of the entity specified and identified by the ID, and treats the page as a popup from the specified hosted control.</span></span> <span data-ttu-id="016c1-203">Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi thư mục bật lên nên sẽ được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="016c1-203">The window navigation rules are evaluated to determine the location where the popup should be displayed.</span></span>  

|<span data-ttu-id="016c1-204">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-204">Parameter</span></span>|<span data-ttu-id="016c1-205">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-205">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="016c1-206">LogicalName</span><span class="sxs-lookup"><span data-stu-id="016c1-206">LogicalName</span></span>|<span data-ttu-id="016c1-207">Tên logic của thực thể hợp lý của thực thể để mở.</span><span class="sxs-lookup"><span data-stu-id="016c1-207">The logical name of the entity to open.</span></span>|  
|<span data-ttu-id="016c1-208">id</span><span class="sxs-lookup"><span data-stu-id="016c1-208">id</span></span>|<span data-ttu-id="016c1-209">ID của hồ sơ thực thể để mở.</span><span class="sxs-lookup"><span data-stu-id="016c1-209">The ID of the entity record to open.</span></span>|  

### <a name="popup"></a><span data-ttu-id="016c1-210">Bật lên</span><span class="sxs-lookup"><span data-stu-id="016c1-210">Popup</span></span>  
 <span data-ttu-id="016c1-211">Bật lên URL từ kiểm soát tổ chức và chạy nguyên tắc điều hướng cửa sổ chống lại hình thức kiểm soát tổ chức để định tuyến bật lên đến vị trí thích hợp.</span><span class="sxs-lookup"><span data-stu-id="016c1-211">Pops up a URL from the hosted control and runs the window navigation rules against it for routing the popup to the appropriate location.</span></span>  

|<span data-ttu-id="016c1-212">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-212">Parameter</span></span>|<span data-ttu-id="016c1-213">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-213">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="016c1-214">url</span><span class="sxs-lookup"><span data-stu-id="016c1-214">url</span></span>|<span data-ttu-id="016c1-215">Routes a popup from this hosted control using this URL as if it were a popup requested from the displayed control.</span><span class="sxs-lookup"><span data-stu-id="016c1-215">Routes a popup from this hosted control using this URL as if it were a popup requested from the displayed control.</span></span>|  
|<span data-ttu-id="016c1-216">nền tảng</span><span class="sxs-lookup"><span data-stu-id="016c1-216">frame</span></span>|<span data-ttu-id="016c1-217">The frame from which this popup originated.</span><span class="sxs-lookup"><span data-stu-id="016c1-217">The frame from which this popup originated.</span></span>|  

<a name="RealignWindow"></a>   
### <a name="realignwindow"></a><span data-ttu-id="016c1-218">RealignWindow</span><span class="sxs-lookup"><span data-stu-id="016c1-218">RealignWindow</span></span>  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]

### <a name="reroute"></a><span data-ttu-id="016c1-219">Định tuyến lại</span><span class="sxs-lookup"><span data-stu-id="016c1-219">ReRoute</span></span>  
 <span data-ttu-id="016c1-220">This action takes the currently displayed URL, and sends it through the window navigation rules from the current hosted control as a popup.</span><span class="sxs-lookup"><span data-stu-id="016c1-220">This action takes the currently displayed URL, and sends it through the window navigation rules from the current hosted control as a popup.</span></span>  

### <a name="runscript"></a><span data-ttu-id="016c1-221">Chạy mã lệnh</span><span class="sxs-lookup"><span data-stu-id="016c1-221">RunScript</span></span>  
 <span data-ttu-id="016c1-222">This action injects JavaScript into the main frame of the application.</span><span class="sxs-lookup"><span data-stu-id="016c1-222">This action injects JavaScript into the main frame of the application.</span></span> <span data-ttu-id="016c1-223">You should avoid using [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps client SDK calls with this action; instead, use the **RunXrmCommand** action.</span><span class="sxs-lookup"><span data-stu-id="016c1-223">You should avoid using [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps client SDK calls with this action; instead, use the **RunXrmCommand** action.</span></span>  

|<span data-ttu-id="016c1-224">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-224">Parameter</span></span>|<span data-ttu-id="016c1-225">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-225">Description</span></span>|  
|---------------|-----------------|  
||<span data-ttu-id="016c1-226">The data parameter is the JavaScript that will be injected into the form.</span><span class="sxs-lookup"><span data-stu-id="016c1-226">The data parameter is the JavaScript that will be injected into the form.</span></span> <span data-ttu-id="016c1-227">**Note:**  The replacement parameters can be used in the script, and they will be replaced before the script is executed.</span><span class="sxs-lookup"><span data-stu-id="016c1-227">**Note:**  The replacement parameters can be used in the script, and they will be replaced before the script is executed.</span></span>|  

<a name="RunXrmCommand"></a>   
### <a name="runxrmcommand"></a><span data-ttu-id="016c1-228">Chạy lệnh Xrm</span><span class="sxs-lookup"><span data-stu-id="016c1-228">RunXrmCommand</span></span>  
 <span data-ttu-id="016c1-229">This action is used to inject [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps SDK JavaScript into the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps form.</span><span class="sxs-lookup"><span data-stu-id="016c1-229">This action is used to inject [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps SDK JavaScript into the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps form.</span></span>  

|<span data-ttu-id="016c1-230">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-230">Parameter</span></span>|<span data-ttu-id="016c1-231">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-231">Description</span></span>|  
|---------------|-----------------|  
||<span data-ttu-id="016c1-232">The data parameter is the JavaScript that will be injected into the form.</span><span class="sxs-lookup"><span data-stu-id="016c1-232">The data parameter is the JavaScript that will be injected into the form.</span></span> <span data-ttu-id="016c1-233">**Note:**  The replacement parameters can be used in the script, and they will be replaced before the script is executed.</span><span class="sxs-lookup"><span data-stu-id="016c1-233">**Note:**  The replacement parameters can be used in the script, and they will be replaced before the script is executed.</span></span>|  

### <a name="save"></a><span data-ttu-id="016c1-234">Lưu</span><span class="sxs-lookup"><span data-stu-id="016c1-234">Save</span></span>  
 <span data-ttu-id="016c1-235">This action saves the current Dynamics 365 for Customer Engagement apps page.</span><span class="sxs-lookup"><span data-stu-id="016c1-235">This action saves the current Dynamics 365 for Customer Engagement apps page.</span></span>  

<a name="SaveAll"></a>   
### <a name="saveall"></a><span data-ttu-id="016c1-236">Lưu tất cả</span><span class="sxs-lookup"><span data-stu-id="016c1-236">SaveAll</span></span>  
 <span data-ttu-id="016c1-237">This action saves all forms in hosted control that allows multiple pages to be displayed (**Allow Multiple Pages** = Yes).</span><span class="sxs-lookup"><span data-stu-id="016c1-237">This action saves all forms in hosted control that allows multiple pages to be displayed (**Allow Multiple Pages** = Yes).</span></span> <span data-ttu-id="016c1-238">If the hosted control allows only a single page to be displayed (**Allow Multiple Pages** = No), this is equivalent to the **Save** action.</span><span class="sxs-lookup"><span data-stu-id="016c1-238">If the hosted control allows only a single page to be displayed (**Allow Multiple Pages** = No), this is equivalent to the **Save** action.</span></span>  

### <a name="saveandclose"></a><span data-ttu-id="016c1-239">Lưu và Đóng</span><span class="sxs-lookup"><span data-stu-id="016c1-239">SaveAndClose</span></span>  
 <span data-ttu-id="016c1-240">This action saves the dirty data on the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps form, and closes the hosted control.</span><span class="sxs-lookup"><span data-stu-id="016c1-240">This action saves the dirty data on the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps form, and closes the hosted control.</span></span>  

<a name="SetSize"></a>   
### <a name="setsize"></a><span data-ttu-id="016c1-241">SetSize</span><span class="sxs-lookup"><span data-stu-id="016c1-241">SetSize</span></span>  
 <span data-ttu-id="016c1-242">This action explicitly sets the width and height of the hosted control.</span><span class="sxs-lookup"><span data-stu-id="016c1-242">This action explicitly sets the width and height of the hosted control.</span></span> <span data-ttu-id="016c1-243">Quá trình này đặc biệt hữu ích khi sử dụng tính năng "tự động" trong bố cục bảng điều khiển của bạn.</span><span class="sxs-lookup"><span data-stu-id="016c1-243">This is particularly useful when using "auto" in your panel layouts.</span></span>  

|<span data-ttu-id="016c1-244">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-244">Parameter</span></span>|<span data-ttu-id="016c1-245">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-245">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="016c1-246">chiều rộng</span><span class="sxs-lookup"><span data-stu-id="016c1-246">width</span></span>|<span data-ttu-id="016c1-247">The width of the hosted control.</span><span class="sxs-lookup"><span data-stu-id="016c1-247">The width of the hosted control.</span></span>|  
|<span data-ttu-id="016c1-248">chiều cao</span><span class="sxs-lookup"><span data-stu-id="016c1-248">height</span></span>|<span data-ttu-id="016c1-249">The height of the hosted control.</span><span class="sxs-lookup"><span data-stu-id="016c1-249">The height of the hosted control.</span></span>|  

### <a name="togglenavigation"></a><span data-ttu-id="016c1-250">Chuyển đổi điều hướng</span><span class="sxs-lookup"><span data-stu-id="016c1-250">ToggleNavigation</span></span>  
 <span data-ttu-id="016c1-251">This action collapses or expands the navigation pane on the left panel of the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps window.</span><span class="sxs-lookup"><span data-stu-id="016c1-251">This action collapses or expands the navigation pane on the left panel of the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps window.</span></span> <span data-ttu-id="016c1-252">The navigation must contain a navigation panel for this action to work.</span><span class="sxs-lookup"><span data-stu-id="016c1-252">The navigation must contain a navigation panel for this action to work.</span></span>  

### <a name="toggleribbon"></a><span data-ttu-id="016c1-253">Chuyển đổi Ruy băng</span><span class="sxs-lookup"><span data-stu-id="016c1-253">ToggleRibbon</span></span>  
 <span data-ttu-id="016c1-254">This action collapses or expands the ribbon.</span><span class="sxs-lookup"><span data-stu-id="016c1-254">This action collapses or expands the ribbon.</span></span> <span data-ttu-id="016c1-255">Nếu bạn ẩn các ruy băng trong hành động **điều hướng**, ruy băng sẽ không được hiển thị và hành động này không hoạt động.</span><span class="sxs-lookup"><span data-stu-id="016c1-255">If you hide the ribbon in the **Navigate** action, it will not be displayed and this action does not work.</span></span> <span data-ttu-id="016c1-256">Hành động này sẽ chỉ làm việc khi ruy băng đã được tải lúc đầu.</span><span class="sxs-lookup"><span data-stu-id="016c1-256">This action will work only when the ribbon was initially loaded.</span></span>  

### <a name="waitforcomplete"></a><span data-ttu-id="016c1-257">Chờ để hoàn tất</span><span class="sxs-lookup"><span data-stu-id="016c1-257">WaitForComplete</span></span>  
 <span data-ttu-id="016c1-258">This action can be used to block the processing until the URL finishes loading.</span><span class="sxs-lookup"><span data-stu-id="016c1-258">This action can be used to block the processing until the URL finishes loading.</span></span>  

> [!NOTE]
>  <span data-ttu-id="016c1-259">Some web pages, particularly [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps pages, have multiple frames.</span><span class="sxs-lookup"><span data-stu-id="016c1-259">Some web pages, particularly [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps pages, have multiple frames.</span></span> <span data-ttu-id="016c1-260">This action waits for only the main frame to complete.</span><span class="sxs-lookup"><span data-stu-id="016c1-260">This action waits for only the main frame to complete.</span></span>  

|<span data-ttu-id="016c1-261">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-261">Parameter</span></span>|<span data-ttu-id="016c1-262">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-262">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="016c1-263">mili giây</span><span class="sxs-lookup"><span data-stu-id="016c1-263">Milliseconds</span></span>|<span data-ttu-id="016c1-264">Tham số tùy chọn để cho biết thời gian tính theo mili giây để đợi đến hết thời gian chờ.</span><span class="sxs-lookup"><span data-stu-id="016c1-264">Optional parameter to indicate how long, in milliseconds, to wait to timeout.</span></span>|  

<a name="Events"></a>   
## <a name="predefined-events"></a><span data-ttu-id="016c1-265">Sự kiện được xác định trước</span><span class="sxs-lookup"><span data-stu-id="016c1-265">Predefined events</span></span>  
 <span data-ttu-id="016c1-266">These are the predefined events for this hosted control type.</span><span class="sxs-lookup"><span data-stu-id="016c1-266">These are the predefined events for this hosted control type.</span></span>  

### <a name="browserdocumentcomplete"></a><span data-ttu-id="016c1-267">Duyệt Tài liệu hoàn chỉnh</span><span class="sxs-lookup"><span data-stu-id="016c1-267">BrowserDocumentComplete</span></span>  
 <span data-ttu-id="016c1-268">Xảy ra khi trang đã hoàn tất tải.</span><span class="sxs-lookup"><span data-stu-id="016c1-268">Occurs when the page has finished loading.</span></span>  

|<span data-ttu-id="016c1-269">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-269">Parameter</span></span>|<span data-ttu-id="016c1-270">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-270">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="016c1-271">url</span><span class="sxs-lookup"><span data-stu-id="016c1-271">url</span></span>|<span data-ttu-id="016c1-272">The URL of the page that has finished loading.</span><span class="sxs-lookup"><span data-stu-id="016c1-272">The URL of the page that has finished loading.</span></span>|  

### <a name="frameloadcomplete"></a><span data-ttu-id="016c1-273">FrameLoadComplete</span><span class="sxs-lookup"><span data-stu-id="016c1-273">FrameLoadComplete</span></span>  
 <span data-ttu-id="016c1-274">Occurs any time when a frame has completed loading.</span><span class="sxs-lookup"><span data-stu-id="016c1-274">Occurs any time when a frame has completed loading.</span></span> <span data-ttu-id="016c1-275">Sự kiện này có thể xảy ra nhiều lần cho mỗi lần tải trang khi iFrame hoặc nền tảng được sử dụng trên trang.</span><span class="sxs-lookup"><span data-stu-id="016c1-275">This event can occur multiple times per page load when an iFrame or frame is used on the page.</span></span> <span data-ttu-id="016c1-276">This event corresponds to the individual `BrowserDocumentComplete` events in code.</span><span class="sxs-lookup"><span data-stu-id="016c1-276">This event corresponds to the individual `BrowserDocumentComplete` events in code.</span></span>  

|<span data-ttu-id="016c1-277">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-277">Parameter</span></span>|<span data-ttu-id="016c1-278">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-278">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="016c1-279">nền tảng</span><span class="sxs-lookup"><span data-stu-id="016c1-279">frame</span></span>|<span data-ttu-id="016c1-280">The name of the frame that finished loading.</span><span class="sxs-lookup"><span data-stu-id="016c1-280">The name of the frame that finished loading.</span></span>|  
|<span data-ttu-id="016c1-281">url</span><span class="sxs-lookup"><span data-stu-id="016c1-281">url</span></span>|<span data-ttu-id="016c1-282">URL của nền tảng đã hoàn tất tải.</span><span class="sxs-lookup"><span data-stu-id="016c1-282">The URL of the frame that finished loading.</span></span>|  

### <a name="popuprouted"></a><span data-ttu-id="016c1-283">Bật lên đã lên lịch</span><span class="sxs-lookup"><span data-stu-id="016c1-283">PopupRouted</span></span>  
 <span data-ttu-id="016c1-284">Xảy ra sau khi một cửa sổ bật lên đã được hệ thống xác định.</span><span class="sxs-lookup"><span data-stu-id="016c1-284">Occurs after a popup has been routed by the system.</span></span>  

|<span data-ttu-id="016c1-285">Tham số</span><span class="sxs-lookup"><span data-stu-id="016c1-285">Parameter</span></span>|<span data-ttu-id="016c1-286">Mô tả</span><span class="sxs-lookup"><span data-stu-id="016c1-286">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="016c1-287">url</span><span class="sxs-lookup"><span data-stu-id="016c1-287">url</span></span>|<span data-ttu-id="016c1-288">The URL of the popup that was routed.</span><span class="sxs-lookup"><span data-stu-id="016c1-288">The URL of the popup that was routed.</span></span>|  

### <a name="see-also"></a><span data-ttu-id="016c1-289">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="016c1-289">See also</span></span>  
 [<span data-ttu-id="016c1-290">Integrate with CTI systems using CTI adapters</span><span class="sxs-lookup"><span data-stu-id="016c1-290">Integrate with CTI systems using CTI adapters</span></span>](../unified-service-desk/integrate-cti-systems-cti-adapters.md)
