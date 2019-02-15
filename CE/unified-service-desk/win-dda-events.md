---
title: WinDDA events in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about the Windows DDA (WinDDA) events in Unified Service Desk.
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
ms.assetid: 188f3d5a-4460-47c1-bdcc-f4a431173a1b
caps.latest.revision: 9
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 3bec8486b81ec719ad935971560e89f0846742a4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387127"
---
# <a name="windda-events"></a><span data-ttu-id="5708f-103">Sự kiện WinDDA</span><span class="sxs-lookup"><span data-stu-id="5708f-103">WinDDA events</span></span>
<span data-ttu-id="5708f-104">Bộ chuyển đổi định hướng dữ liệu [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] (DDA) phân biệt giữa hai loại sự kiện, sự kiện ứng dụng và sự kiện kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="5708f-104">The [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] data-driven adapter (DDA) distinguishes between two types of events, application events and control events.</span></span> <span data-ttu-id="5708f-105">Chủ đề này mô tả hai sự kiện này.</span><span class="sxs-lookup"><span data-stu-id="5708f-105">This topic describes these two events.</span></span>  
  
<a name="control"></a>   
## <a name="control-events"></a><span data-ttu-id="5708f-106">Sự kiện kiểm soát</span><span class="sxs-lookup"><span data-stu-id="5708f-106">Control events</span></span>  
 <span data-ttu-id="5708f-107">Các sự kiện kiểm soát được bắt đầu bởi các kiểm soát trong ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="5708f-107">Control events are fired by controls in an application.</span></span> <span data-ttu-id="5708f-108">Đối với tất cả các sự kiện này, tên kiểm soát phải được chỉ định trong quá trình đăng ký (`RegisterActionForEvent`).</span><span class="sxs-lookup"><span data-stu-id="5708f-108">For all of these events, the control name must be specified during registration (`RegisterActionForEvent`).</span></span> <span data-ttu-id="5708f-109">Các điều khiển cũng phải có thể được truy cập trong ứng dụng trong khi đăng ký.</span><span class="sxs-lookup"><span data-stu-id="5708f-109">The controls must also be accessible in the application during registration.</span></span> <span data-ttu-id="5708f-110">You can use the [FindControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.operationtype.findcontrol) method or add an exception handler to ensure that the control is accessible.</span><span class="sxs-lookup"><span data-stu-id="5708f-110">You can use the [FindControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.operationtype.findcontrol) method or add an exception handler to ensure that the control is accessible.</span></span>  
  
 <span data-ttu-id="5708f-111">Nhà máy Phần mềm [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)] liệt kê các sự kiện được hỗ trợ cho một loại kiểm soát Giao diện Người dùng (UI) cụ thể.</span><span class="sxs-lookup"><span data-stu-id="5708f-111">The [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)] Software Factory lists the events that are supported for a specific User Interface (UI) control type.</span></span> <span data-ttu-id="5708f-112">Nếu bạn không chỉ định loại trong Trình kiểm tra [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)], [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] liệt kê tất cả sự kiện cho kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="5708f-112">If you do not specify the type in the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] Inspector, [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] lists all events for the control.</span></span> <span data-ttu-id="5708f-113">Tất cả sự kiện kiểm soát có sẵn được liệt kê bởi Nhà máy Phần mềm [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)] nếu không có loại kiểm soát nào được phát hiện.</span><span class="sxs-lookup"><span data-stu-id="5708f-113">All available control events are listed by the [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)] Software Factory if no control type is detected.</span></span> <span data-ttu-id="5708f-114">Bảng sau mô tả các sự kiện kiểm soát được hỗ trợ.</span><span class="sxs-lookup"><span data-stu-id="5708f-114">The following table describes the supported control events.</span></span>  
  
|<span data-ttu-id="5708f-115">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="5708f-115">Element</span></span>|<span data-ttu-id="5708f-116">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5708f-116">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="5708f-117">GotFocus</span><span class="sxs-lookup"><span data-stu-id="5708f-117">GotFocus</span></span>|<span data-ttu-id="5708f-118">Sự kiện này được đưa lên khi kiểm soát nhắm được trọng tâm.</span><span class="sxs-lookup"><span data-stu-id="5708f-118">The event is raised when the control gets the focus.</span></span>|  
|<span data-ttu-id="5708f-119">LostFocus</span><span class="sxs-lookup"><span data-stu-id="5708f-119">LostFocus</span></span>|<span data-ttu-id="5708f-120">Sự kiện này được đưa lên khi kiểm soát mất trọng tâm.</span><span class="sxs-lookup"><span data-stu-id="5708f-120">The event is raised when the control loses the focus.</span></span>|  
|<span data-ttu-id="5708f-121">ButtonPressed</span><span class="sxs-lookup"><span data-stu-id="5708f-121">ButtonPressed</span></span>|<span data-ttu-id="5708f-122">Sự kiện này được nêu khi nút được bấm.</span><span class="sxs-lookup"><span data-stu-id="5708f-122">The event is raised when the button is clicked.</span></span>|  
|<span data-ttu-id="5708f-123">ButtonReleased</span><span class="sxs-lookup"><span data-stu-id="5708f-123">ButtonReleased</span></span>|<span data-ttu-id="5708f-124">Sự kiện này được nêu khi nút được nhả.</span><span class="sxs-lookup"><span data-stu-id="5708f-124">The event is raised when the button is released.</span></span>|  
|<span data-ttu-id="5708f-125">CheckBoxSet</span><span class="sxs-lookup"><span data-stu-id="5708f-125">CheckBoxSet</span></span>|<span data-ttu-id="5708f-126">Sự kiện được nêu khi hộp kiểm được chọn.</span><span class="sxs-lookup"><span data-stu-id="5708f-126">The event is raised when the check box is selected.</span></span>|  
|<span data-ttu-id="5708f-127">CheckBoxCleared</span><span class="sxs-lookup"><span data-stu-id="5708f-127">CheckBoxCleared</span></span>|<span data-ttu-id="5708f-128">Sự kiện được nêu khi hộp kiểm bị xóa.</span><span class="sxs-lookup"><span data-stu-id="5708f-128">The event is raised when the check box is cleared.</span></span>|  
|<span data-ttu-id="5708f-129">RadioButtonSet</span><span class="sxs-lookup"><span data-stu-id="5708f-129">RadioButtonSet</span></span>|<span data-ttu-id="5708f-130">Sự kiện được nêu khi nút radio được chọn.</span><span class="sxs-lookup"><span data-stu-id="5708f-130">The event is raised when the radio button is selected.</span></span>|  
  
 <span data-ttu-id="5708f-131">Bảng sau liệt kê các sự kiện mà mỗi kiểm soát hỗ trợ.</span><span class="sxs-lookup"><span data-stu-id="5708f-131">The following table lists the events that each control supports.</span></span>  
  
|<span data-ttu-id="5708f-132">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="5708f-132">Element</span></span>|<span data-ttu-id="5708f-133">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5708f-133">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="5708f-134">Nút nhấn</span><span class="sxs-lookup"><span data-stu-id="5708f-134">Push Button</span></span>|<span data-ttu-id="5708f-135">ButtonPressed, ButtonReleased, GotFocus, LostFocus</span><span class="sxs-lookup"><span data-stu-id="5708f-135">ButtonPressed, ButtonReleased, GotFocus, LostFocus</span></span>|  
|<span data-ttu-id="5708f-136">Hộp kiểm</span><span class="sxs-lookup"><span data-stu-id="5708f-136">Check Box</span></span>|<span data-ttu-id="5708f-137">GotFocus, CheckBoxSet, CheckBoxCleared, LostFocus</span><span class="sxs-lookup"><span data-stu-id="5708f-137">GotFocus, CheckBoxSet, CheckBoxCleared, LostFocus</span></span>|  
|<span data-ttu-id="5708f-138">Nút Radio</span><span class="sxs-lookup"><span data-stu-id="5708f-138">Radio Button</span></span>|<span data-ttu-id="5708f-139">GotFocus, RadioButtonSet, LostFocus</span><span class="sxs-lookup"><span data-stu-id="5708f-139">GotFocus, RadioButtonSet, LostFocus</span></span>|  
|<span data-ttu-id="5708f-140">Văn bản</span><span class="sxs-lookup"><span data-stu-id="5708f-140">Text</span></span>|<span data-ttu-id="5708f-141">GotFocus, LostFocus</span><span class="sxs-lookup"><span data-stu-id="5708f-141">GotFocus, LostFocus</span></span>|  
|<span data-ttu-id="5708f-142">Văn bản Có thể chỉnh sửa</span><span class="sxs-lookup"><span data-stu-id="5708f-142">Editable Text</span></span>|<span data-ttu-id="5708f-143">GotFocus, LostFocus</span><span class="sxs-lookup"><span data-stu-id="5708f-143">GotFocus, LostFocus</span></span>|  
  
<a name="application"></a>   
## <a name="application-events"></a><span data-ttu-id="5708f-144">Sự kiện Ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="5708f-144">Application events</span></span>  
 <span data-ttu-id="5708f-145">Sự kiện ứng dụng không bị ràng buộc cho một kiểm soát; Vì vậy, bạn không cần phải chỉ định một tên kiểm soát trong hoạt động `RegisterActionForEvent`.</span><span class="sxs-lookup"><span data-stu-id="5708f-145">Application events are not bound to a control; therefore, you do not have to specify a control name in the `RegisterActionForEvent` activity.</span></span> <span data-ttu-id="5708f-146">Bảng sau mô tả các sự kiện ứng dụng có sẵn trong [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)]:</span><span class="sxs-lookup"><span data-stu-id="5708f-146">The following table describes the application events that are available in the [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)]:</span></span>  
  
|<span data-ttu-id="5708f-147">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="5708f-147">Element</span></span>|<span data-ttu-id="5708f-148">Mô tả</span><span class="sxs-lookup"><span data-stu-id="5708f-148">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="5708f-149">WindowShown</span><span class="sxs-lookup"><span data-stu-id="5708f-149">WindowShown</span></span>|<span data-ttu-id="5708f-150">Sự kiện được nêu khi cửa sổ được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="5708f-150">The event is raised when the window is displayed.</span></span>|  
|<span data-ttu-id="5708f-151">WindowDisappeared</span><span class="sxs-lookup"><span data-stu-id="5708f-151">WindowDisappeared</span></span>|<span data-ttu-id="5708f-152">Sự kiện được nêu khi cửa sổ bị ẩn.</span><span class="sxs-lookup"><span data-stu-id="5708f-152">The event is raised when the window is hidden.</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="5708f-153">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="5708f-153">See also</span></span>  
 <span data-ttu-id="5708f-154">[Win DDA](../unified-service-desk/windda.md) </span><span class="sxs-lookup"><span data-stu-id="5708f-154">[Win DDA](../unified-service-desk/windda.md) </span></span>  
 [<span data-ttu-id="5708f-155">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="5708f-155">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
