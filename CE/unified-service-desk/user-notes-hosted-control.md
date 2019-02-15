---
title: User Notes (Hosted Control) in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about the User Notes type of hosted control in Unified Servoce Desk.
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
ms.assetid: 7d3fec60-2f91-4b25-8a80-f41def5a5f74
caps.latest.revision: 7
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: cfe1da43c461a72cfe491e52678e13e238afa6f3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385568"
---
# <a name="user-notes-hosted-control"></a><span data-ttu-id="a9b4b-103">User Notes (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="a9b4b-103">User Notes (Hosted Control)</span></span>
<span data-ttu-id="a9b4b-104">Sử dụng loại kiểm soát tổ chức **ghi chú người dùng** để cung cấp cho các tổng đài viên một tấm ghi để nhập ghi chú trong quá trình tương tác.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-104">Use **User Notes** hosted control type to provide agents with a scratch pad to type notes during an interaction.</span></span> <span data-ttu-id="a9b4b-105">Có thể áp dụng kiểm tra chính tả cho từng ngôn ngữ cho thành phần này bằng cách gọi thao tác **Đặt ngôn ngữ**.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-105">Language specific spell checking can be applied to this component by calling the **SetLanguage** action.</span></span> <span data-ttu-id="a9b4b-106">Thành phần này không tự động chọn ngôn ngữ hiện tại của người dùng, theo thiết kế.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-106">This component does not automatically pick up the current language of the user, by design.</span></span> <span data-ttu-id="a9b4b-107">Khả năng thay đổi ngôn ngữ được sử dụng nhằm mục đích cung cấp khả năng thiết lập ngôn ngữ thích hợp cho các giao dịch.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-107">The ability to change the language used is intended to provide the ability to set the language appropriate for the transaction.</span></span> <span data-ttu-id="a9b4b-108">Ví dụ, xem xét có tổng đài viên song ngữ có thể nói tiếng Anh và tiếng Tây Ban Nha.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-108">For example, consider there is a bilingual agent that can speak English and Spanish.</span></span> <span data-ttu-id="a9b4b-109">IVR có thể vượt qua lựa chọn ngôn ngữ từ hệ thống điện thoại đến bộ điều hợp CRI của ứng dụng tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-109">The IVR may pass the language selection from the phone system to the agent application’s CTI adapter.</span></span> <span data-ttu-id="a9b4b-110">Lựa chọn ngôn ngữ này sau đó có thể được sử dụng để thiết lập ngôn ngữ để kiểm tra chính tả cho kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-110">This language selection can then be used to set the spell check language for this hosted control.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a9b4b-111">Kiểm soát tổ chức không tự động xác định tham số thay thế.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-111">This hosted control does not automatically populate replacement parameters.</span></span> <span data-ttu-id="a9b4b-112">The [UpdateReplacementParameters](#UpdateReplacementParameters) action can be called to take the current notes and populate the replacement parameters.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-112">The [UpdateReplacementParameters](#UpdateReplacementParameters) action can be called to take the current notes and populate the replacement parameters.</span></span> <span data-ttu-id="a9b4b-113">Các tham số thay thế có thể được sử dụng để sao chép các ghi chú đến trường hợp.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-113">The replacement parameters can be used to copy the notes to the case.</span></span>  
  
<a name="Create"></a>   
## <a name="create-a-user-notes-hosted-control"></a><span data-ttu-id="a9b4b-114">Tạo kiểm soát tổ chức ghi chú người dùng</span><span class="sxs-lookup"><span data-stu-id="a9b4b-114">Create a User Notes hosted control</span></span>  
 <span data-ttu-id="a9b4b-115">Trong khi tạo một hình thức kiểm soát tổ chức mới, các trường trong màn hình **Kiểm soát tổ chức mới** thay đổi dựa vào loại tổ chức tổ chức bạn muốn tạo.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-115">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span></span> <span data-ttu-id="a9b4b-116">Phần này cung cấp thông tin về các trường cụ thể mà là duy nhất cho loại kiểm soát tổ chức **Ghi chú người dùng**.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-116">This section provides information about the specific fields that are unique to the **User Notes** hosted control type.</span></span> <span data-ttu-id="a9b4b-117">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="a9b4b-117">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span></span>  
  
 <span data-ttu-id="a9b4b-118">![User Notes hosted control](../unified-service-desk/media/crm-itpro-usd-usernoteshostedcontrol.png "User Notes hosted control")</span><span class="sxs-lookup"><span data-stu-id="a9b4b-118">![User Notes hosted control](../unified-service-desk/media/crm-itpro-usd-usernoteshostedcontrol.png "User Notes hosted control")</span></span>  
  
 <span data-ttu-id="a9b4b-119">Trong màn hình **Kiểm soát tổ chức mới**:</span><span class="sxs-lookup"><span data-stu-id="a9b4b-119">In the **New Hosted Control** screen:</span></span>  
  
- <span data-ttu-id="a9b4b-120">Từ danh sách thả xuống **Loại thành phần USD**, chọn **Ghi chú người dùng**.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-120">From the **USD Component Type** drop-down list, select **User Notes**.</span></span>  
  
- <span data-ttu-id="a9b4b-121">Trong trường **Hiển thị nhóm**, xác định bảng điều khiển nơi hiển thị kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-121">In the **Display Group** field, specify a panel where this hosted control will be displayed.</span></span> <span data-ttu-id="a9b4b-122">For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels](../unified-service-desk/panels-panel-types-panel-layouts.md#Panels).</span><span class="sxs-lookup"><span data-stu-id="a9b4b-122">For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels](../unified-service-desk/panels-panel-types-panel-layouts.md#Panels).</span></span>  
  
<a name="Actions"></a>   
## <a name="predefined-uii-actions"></a><span data-ttu-id="a9b4b-123">Thao tác UII được xác định trước</span><span class="sxs-lookup"><span data-stu-id="a9b4b-123">Predefined UII actions</span></span>  
 <span data-ttu-id="a9b4b-124">Đây là những thao tác được xác định trước cho loại kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-124">These are the predefined actions for this hosted control type.</span></span>  
  
<a name="Close"></a>   
### <a name="close"></a><span data-ttu-id="a9b4b-125">Đóng</span><span class="sxs-lookup"><span data-stu-id="a9b4b-125">Close</span></span>  
 <span data-ttu-id="a9b4b-126">Hành động này được sử dụng để đóng kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-126">This action is used to close the hosted control.</span></span>  
  
### <a name="fireevent"></a><span data-ttu-id="a9b4b-127">FireEvent</span><span class="sxs-lookup"><span data-stu-id="a9b4b-127">FireEvent</span></span>  
 <span data-ttu-id="a9b4b-128">Khuyến khích sự kiện được người dùng xác định từ loại hình kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-128">Fires a user-defined event from this hosted control.</span></span>  
  
|<span data-ttu-id="a9b4b-129">Tham số</span><span class="sxs-lookup"><span data-stu-id="a9b4b-129">Parameter</span></span>|<span data-ttu-id="a9b4b-130">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a9b4b-130">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a9b4b-131">tên</span><span class="sxs-lookup"><span data-stu-id="a9b4b-131">name</span></span>|<span data-ttu-id="a9b4b-132">Tên của sự kiện do người dùng xác định.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-132">Name of the user-defined event.</span></span>|  
  
 <span data-ttu-id="a9b4b-133">Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-133">All subsequent name=value pairs become the parameters to the event.</span></span> <span data-ttu-id="a9b4b-134">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span><span class="sxs-lookup"><span data-stu-id="a9b4b-134">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span></span>  
  
<a name="MoveToPanel"></a>   
### <a name="movetopanel"></a><span data-ttu-id="a9b4b-135">MoveToPanel</span><span class="sxs-lookup"><span data-stu-id="a9b4b-135">MoveToPanel</span></span>  
 <span data-ttu-id="a9b4b-136">Hành động này được sử dụng để di chuyển kiểm soát tổ chức giữa các bảng điều khiển tại thời gian chạy.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-136">This action is used to move hosted controls between panels at runtime.</span></span>  
  
|<span data-ttu-id="a9b4b-137">Tham số</span><span class="sxs-lookup"><span data-stu-id="a9b4b-137">Parameter</span></span>|<span data-ttu-id="a9b4b-138">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a9b4b-138">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a9b4b-139">ứng dụng</span><span class="sxs-lookup"><span data-stu-id="a9b4b-139">app</span></span>|<span data-ttu-id="a9b4b-140">Tên của kiểm soát tổ chức được di chuyển.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-140">Name of the hosted control to be moved.</span></span>|  
|<span data-ttu-id="a9b4b-141">bảng điều khiển</span><span class="sxs-lookup"><span data-stu-id="a9b4b-141">panel</span></span>|<span data-ttu-id="a9b4b-142">Bảng điều khiển đích cho kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-142">Target panel for the hosted control.</span></span>|  
  
### <a name="newcrmpage"></a><span data-ttu-id="a9b4b-143">New_CRM_Page</span><span class="sxs-lookup"><span data-stu-id="a9b4b-143">New_CRM_Page</span></span>  
 <span data-ttu-id="a9b4b-144">Creates a page for creating a new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps record of the entity specified, and treats the page as a popup from the specified hosted control.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-144">Creates a page for creating a new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps record of the entity specified, and treats the page as a popup from the specified hosted control.</span></span> <span data-ttu-id="a9b4b-145">Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi trang tạo hồ sơ thực thể được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-145">The window navigation rules are evaluated to determine the location where the page to create the entity record is displayed.</span></span>  
  
|<span data-ttu-id="a9b4b-146">Tham số</span><span class="sxs-lookup"><span data-stu-id="a9b4b-146">Parameter</span></span>|<span data-ttu-id="a9b4b-147">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a9b4b-147">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a9b4b-148">LogicalName</span><span class="sxs-lookup"><span data-stu-id="a9b4b-148">LogicalName</span></span>|<span data-ttu-id="a9b4b-149">Tên logic của thực thể để tạo phiên bản mới.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-149">The logical name of the entity for creating a new instance.</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="a9b4b-150">Phần còn lại của các tham số nên bao gồm tên = cặp giá trị.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-150">The rest of the parameters should consist of name=value pairs.</span></span> <span data-ttu-id="a9b4b-151">Đây là các giá trị nhập sẵn bổ sung trong hình thức để tạo hồ sơ mới cho thực thể đã chỉ định.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-151">These are the additional pre-populated values in the form for creating a new record for the specified entity.</span></span> <span data-ttu-id="a9b4b-152">For more information about using this action, see step 4 in [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="a9b4b-152">For more information about using this action, see step 4 in [Walkthrough 7: Configure agent scripting in your agent application](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md).</span></span>  
  
### <a name="opencrmpage"></a><span data-ttu-id="a9b4b-153">Open_CRM_Page</span><span class="sxs-lookup"><span data-stu-id="a9b4b-153">Open_CRM_Page</span></span>  
 <span data-ttu-id="a9b4b-154">Mở một phiên bản hiện tại của các thực thể được chỉ định và xác định theo ID và xử lý trang như một thư mục bật lên từ kiểm soát tổ chức được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-154">Opens an existing instance of the entity specified and identified by the ID, and treats the page as a popup from the specified hosted control.</span></span> <span data-ttu-id="a9b4b-155">Các quy tắc chuyển hướng cửa sổ được đánh giá để xác định vị trí nơi thư mục bật lên nên sẽ được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-155">The window navigation rules are evaluated to determine the location where the popup should be displayed.</span></span>  
  
|<span data-ttu-id="a9b4b-156">Tham số</span><span class="sxs-lookup"><span data-stu-id="a9b4b-156">Parameter</span></span>|<span data-ttu-id="a9b4b-157">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a9b4b-157">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a9b4b-158">LogicalName</span><span class="sxs-lookup"><span data-stu-id="a9b4b-158">LogicalName</span></span>|<span data-ttu-id="a9b4b-159">Tên logic của thực thể hợp lý của thực thể để mở.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-159">The logical name of the entity to open.</span></span>|  
|<span data-ttu-id="a9b4b-160">id</span><span class="sxs-lookup"><span data-stu-id="a9b4b-160">id</span></span>|<span data-ttu-id="a9b4b-161">ID của hồ sơ thực thể để mở.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-161">The ID of the entity record to open.</span></span>|  
  
### <a name="popup"></a><span data-ttu-id="a9b4b-162">Bật lên</span><span class="sxs-lookup"><span data-stu-id="a9b4b-162">Popup</span></span>  
 <span data-ttu-id="a9b4b-163">Bật lên URL từ kiểm soát tổ chức và chạy nguyên tắc điều hướng cửa sổ chống lại hình thức kiểm soát tổ chức để định tuyến bật lên đến vị trí thích hợp.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-163">Pops up a URL from the hosted control and runs the window navigation rules against it for routing the popup to the appropriate location.</span></span>  
  
|<span data-ttu-id="a9b4b-164">Tham số</span><span class="sxs-lookup"><span data-stu-id="a9b4b-164">Parameter</span></span>|<span data-ttu-id="a9b4b-165">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a9b4b-165">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a9b4b-166">url</span><span class="sxs-lookup"><span data-stu-id="a9b4b-166">url</span></span>|<span data-ttu-id="a9b4b-167">Định tuyến bật lên từ kiểm soát tổ chức này sử dụng URL này như thể nó là một thư mục bật lên được yêu cầu từ kiểm soát được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-167">Routes a popup from this hosted control using this URL as if it were a popup requested from the displayed control.</span></span>|  
|<span data-ttu-id="a9b4b-168">nền tảng</span><span class="sxs-lookup"><span data-stu-id="a9b4b-168">frame</span></span>|<span data-ttu-id="a9b4b-169">Nền tảng mà thư mục bật lên xuất phát.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-169">The frame from which this popup originated.</span></span>|  
  
<a name="RealignWindow"></a>   
### <a name="realignwindow"></a><span data-ttu-id="a9b4b-170">RealignWindow</span><span class="sxs-lookup"><span data-stu-id="a9b4b-170">RealignWindow</span></span>  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]
  
<a name="SetSize"></a>   
### <a name="setsize"></a><span data-ttu-id="a9b4b-171">SetSize</span><span class="sxs-lookup"><span data-stu-id="a9b4b-171">SetSize</span></span>  
 <span data-ttu-id="a9b4b-172">Hành động này đặt chiều rộng và chiều cao của kiểm soát tổ chức một cách rõ ràng.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-172">This action explicitly sets the width and height of the hosted control.</span></span> <span data-ttu-id="a9b4b-173">Quá trình này đặc biệt hữu ích khi sử dụng tính năng "tự động" trong bố cục bảng điều khiển của bạn.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-173">This is particularly useful when using "auto" in your panel layouts.</span></span>  
  
|<span data-ttu-id="a9b4b-174">Tham số</span><span class="sxs-lookup"><span data-stu-id="a9b4b-174">Parameter</span></span>|<span data-ttu-id="a9b4b-175">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a9b4b-175">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a9b4b-176">chiều rộng</span><span class="sxs-lookup"><span data-stu-id="a9b4b-176">width</span></span>|<span data-ttu-id="a9b4b-177">Chiều rộng của kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-177">The width of the hosted control.</span></span>|  
|<span data-ttu-id="a9b4b-178">chiều cao</span><span class="sxs-lookup"><span data-stu-id="a9b4b-178">height</span></span>|<span data-ttu-id="a9b4b-179">Chiều cao của kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-179">The height of the hosted control.</span></span>|  
  
<a name="UpdateReplacementParameters"></a>   
### <a name="updatereplacementparameters"></a><span data-ttu-id="a9b4b-180">Cập nhật tham số thay thế</span><span class="sxs-lookup"><span data-stu-id="a9b4b-180">UpdateReplacementParameters</span></span>  
 <span data-ttu-id="a9b4b-181">Hành động này được sử dụng để cập nhật một cách rõ ràng dữ liệu kiểm soát tổ chức **ghi chú người dùng** vào danh sách tham số thay thế.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-181">This action is used to explicitly update the **User Notes** hosted control data into the replacement parameter list.</span></span> <span data-ttu-id="a9b4b-182">Điều này là không giống như các loại kiểm soát tổ chức khác nơi dữ liệu kiểm soát tổ chức được cập nhật tự động vào tham số thay thế.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-182">This is unlike other hosted control types where the hosted control data is automatically updated into the replacement parameters.</span></span>  
  
<a name="Event"></a>   
## <a name="predefined-events"></a><span data-ttu-id="a9b4b-183">Sự kiện được xác định trước</span><span class="sxs-lookup"><span data-stu-id="a9b4b-183">Predefined events</span></span>  
 <span data-ttu-id="a9b4b-184">Sự kiện được xác định trước sau đây có sẵn cho loại kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-184">The following predefined events are available for this hosted control type.</span></span>  
  
### <a name="loaded"></a><span data-ttu-id="a9b4b-185">Đã tải</span><span class="sxs-lookup"><span data-stu-id="a9b4b-185">Loaded</span></span>  
 <span data-ttu-id="a9b4b-186">Xảy ra khi kiểm soát tổ chức đã hoàn tất tải.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-186">Occurs when the hosted control has finished loading.</span></span>  
  
### <a name="popuprouted"></a><span data-ttu-id="a9b4b-187">Bật lên đã lên lịch</span><span class="sxs-lookup"><span data-stu-id="a9b4b-187">PopupRouted</span></span>  
 <span data-ttu-id="a9b4b-188">Xảy ra sau khi một cửa sổ bật lên đã được hệ thống xác định.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-188">Occurs after a popup has been routed by the system.</span></span>  
  
|<span data-ttu-id="a9b4b-189">Tham số</span><span class="sxs-lookup"><span data-stu-id="a9b4b-189">Parameter</span></span>|<span data-ttu-id="a9b4b-190">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a9b4b-190">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a9b4b-191">url</span><span class="sxs-lookup"><span data-stu-id="a9b4b-191">url</span></span>|<span data-ttu-id="a9b4b-192">URL của cửa sổ bật lên đã được xác định.</span><span class="sxs-lookup"><span data-stu-id="a9b4b-192">The URL of the popup that was routed.</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="a9b4b-193">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a9b4b-193">See also</span></span>  
 <span data-ttu-id="a9b4b-194">[Hành động UII](../unified-service-desk/uii-actions.md) </span><span class="sxs-lookup"><span data-stu-id="a9b4b-194">[UII actions](../unified-service-desk/uii-actions.md) </span></span>  
 <span data-ttu-id="a9b4b-195">[Sự kiện](../unified-service-desk/events.md) </span><span class="sxs-lookup"><span data-stu-id="a9b4b-195">[Events](../unified-service-desk/events.md) </span></span>  
 <span data-ttu-id="a9b4b-196">[Xem sự kiện và hành động xác định trước cho kiểm soát tổ chức](../unified-service-desk/view-predefined-actions-events-hosted-control.md) </span><span class="sxs-lookup"><span data-stu-id="a9b4b-196">[View predefined actions and events for a hosted control](../unified-service-desk/view-predefined-actions-events-hosted-control.md) </span></span>  
 <span data-ttu-id="a9b4b-197">[Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="a9b4b-197">[Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md) </span></span>  
 <span data-ttu-id="a9b4b-198">[Tham chiếu loại kiểm soát tổ chức và hoạt động/sự kiện](../unified-service-desk/hosted-control-types-action-event-reference.md) </span><span class="sxs-lookup"><span data-stu-id="a9b4b-198">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md) </span></span>  
 [<span data-ttu-id="a9b4b-199">Administration Guide for Unified Service Desk for Microsoft Dynamics CRM</span><span class="sxs-lookup"><span data-stu-id="a9b4b-199">Administration Guide for Unified Service Desk for Microsoft Dynamics CRM</span></span>](http://go.microsoft.com/fwlink/p/?LinkID=394402)
