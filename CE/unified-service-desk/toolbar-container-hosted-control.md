---
title: Toolbar Container (Hosted Control) | MicrosoftDocs
description: Learn about using Toolbar Container type of hosted control to configure toolbars in Unified Service Desk.
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
ms.assetid: d79dc1f2-cb40-4f8a-bb7c-5e6699a5ad0d
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
ms.openlocfilehash: 575199268b7984c4ac33e3adadb435cc474747b2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385801"
---
# <a name="toolbar-container-hosted-control"></a><span data-ttu-id="458eb-103">Toolbar Container (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="458eb-103">Toolbar Container (Hosted Control)</span></span>
<span data-ttu-id="458eb-104">Sử dụng loại **Bộ chứa thanh công cụ**kiểu kiểm soát tổ chức để tạo ra thanh công cụ trong ứng dụng của bạn, mà ứng dụng này có thể hiển thị danh sách các nút có hình ảnh và văn bản có thể thực hiện thao tác.</span><span class="sxs-lookup"><span data-stu-id="458eb-104">Use **Toolbar Container** type of hosted control to create a toolbar in your application, which can display a list of buttons with images and text that can execute actions.</span></span> <span data-ttu-id="458eb-105">Bạn có thể tạo nhiều loại bộ chứa thanh công cụ kiểu kiểm soát tổ chức và đặt chúng vào bất kỳ bảng nào trong ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="458eb-105">You can create multiple Toolbar Container type of hosted controls, and place them on any panel in the application.</span></span> <span data-ttu-id="458eb-106">For more information about working with toolbars, see [Configure toolbars in your application](../unified-service-desk/configure-toolbars-application.md).</span><span class="sxs-lookup"><span data-stu-id="458eb-106">For more information about working with toolbars, see [Configure toolbars in your application](../unified-service-desk/configure-toolbars-application.md).</span></span>  
  
<a name="Create"></a>   
## <a name="create-a-toolbar-container-hosted-control"></a><span data-ttu-id="458eb-107">Tạo kiểm soát tổ chức của bộ chứa Thanh công cụ</span><span class="sxs-lookup"><span data-stu-id="458eb-107">Create a Toolbar Container hosted control</span></span>  
 <span data-ttu-id="458eb-108">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span><span class="sxs-lookup"><span data-stu-id="458eb-108">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span></span> <span data-ttu-id="458eb-109">Phần này cung cấp thông tin về các trường cụ thể là duy nhất đối với loại kiểm soát tổ chức của **bộ chứa thanh công cụ**.</span><span class="sxs-lookup"><span data-stu-id="458eb-109">This section provides information about the specific fields that are unique to the **Toolbar Container** hosted control type.</span></span> <span data-ttu-id="458eb-110">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="458eb-110">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span></span>  
  
 <span data-ttu-id="458eb-111">![Toolbar Container hosted control](../unified-service-desk/media/crm-itpro-usd-toolbarhostedcontrol.png "Toolbar Container hosted control")</span><span class="sxs-lookup"><span data-stu-id="458eb-111">![Toolbar Container hosted control](../unified-service-desk/media/crm-itpro-usd-toolbarhostedcontrol.png "Toolbar Container hosted control")</span></span>  
  
 <span data-ttu-id="458eb-112">In the **New Hosted Control** screen:</span><span class="sxs-lookup"><span data-stu-id="458eb-112">In the **New Hosted Control** screen:</span></span>  
  
- <span data-ttu-id="458eb-113">Từ danh sách thả xuống **Loại thành phần USD**, chọn **Bộ chứa thanh công cụ**.</span><span class="sxs-lookup"><span data-stu-id="458eb-113">From the **USD Component Type** drop-down list, select **Toolbar Container**.</span></span>  
  
- <span data-ttu-id="458eb-114">Trường **Hiển thị nhóm** hiển thị bảng điều khiển nơi hiển thị kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="458eb-114">The **Display Group** field displays the panel where this hosted control will be displayed.</span></span> <span data-ttu-id="458eb-115">**ToolbarPanel** là phổ biến nhất cho loại kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="458eb-115">**ToolbarPanel** is the most common for this hosted control type.</span></span> <span data-ttu-id="458eb-116">For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels](../unified-service-desk/panels-panel-types-panel-layouts.md#Panels).</span><span class="sxs-lookup"><span data-stu-id="458eb-116">For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels](../unified-service-desk/panels-panel-types-panel-layouts.md#Panels).</span></span>  
  
<a name="Actions"></a>   
## <a name="predefined-uii-actions"></a><span data-ttu-id="458eb-117">Predefined UII actions</span><span class="sxs-lookup"><span data-stu-id="458eb-117">Predefined UII actions</span></span>  
 <span data-ttu-id="458eb-118">These are the predefined actions for this hosted control type.</span><span class="sxs-lookup"><span data-stu-id="458eb-118">These are the predefined actions for this hosted control type.</span></span>  
  
### <a name="fireevent"></a><span data-ttu-id="458eb-119">FireEvent</span><span class="sxs-lookup"><span data-stu-id="458eb-119">FireEvent</span></span>  
 <span data-ttu-id="458eb-120">Fires a user-defined event from this hosted control.</span><span class="sxs-lookup"><span data-stu-id="458eb-120">Fires a user-defined event from this hosted control.</span></span>  
  
|<span data-ttu-id="458eb-121">Tham số</span><span class="sxs-lookup"><span data-stu-id="458eb-121">Parameter</span></span>|<span data-ttu-id="458eb-122">Mô tả</span><span class="sxs-lookup"><span data-stu-id="458eb-122">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="458eb-123">tên</span><span class="sxs-lookup"><span data-stu-id="458eb-123">name</span></span>|<span data-ttu-id="458eb-124">Tên của sự kiện do người dùng xác định.</span><span class="sxs-lookup"><span data-stu-id="458eb-124">Name of the user-defined event.</span></span>|  
  
 <span data-ttu-id="458eb-125">Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này.</span><span class="sxs-lookup"><span data-stu-id="458eb-125">All subsequent name=value pairs become the parameters to the event.</span></span> <span data-ttu-id="458eb-126">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span><span class="sxs-lookup"><span data-stu-id="458eb-126">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span></span>  
  
### <a name="hidetoolbar"></a><span data-ttu-id="458eb-127">HideToolbar</span><span class="sxs-lookup"><span data-stu-id="458eb-127">HideToolbar</span></span>  
 <span data-ttu-id="458eb-128">Thao tác này ẩn thanh công cụ rõ ràng từ người dùng.</span><span class="sxs-lookup"><span data-stu-id="458eb-128">This action explicitly hides a toolbar from the user.</span></span>  
  
|<span data-ttu-id="458eb-129">Tham số</span><span class="sxs-lookup"><span data-stu-id="458eb-129">Parameter</span></span>|<span data-ttu-id="458eb-130">Mô tả</span><span class="sxs-lookup"><span data-stu-id="458eb-130">Description</span></span>|  
|---------------|-----------------|  
||<span data-ttu-id="458eb-131">Chỉ định tên thanh công cụ để ẩn trong trường **Dữ liệu**.</span><span class="sxs-lookup"><span data-stu-id="458eb-131">Specify the toolbar name to hide in the **Data** field.</span></span>|  
  
### <a name="realignwindow"></a><span data-ttu-id="458eb-132">RealignWindow</span><span class="sxs-lookup"><span data-stu-id="458eb-132">RealignWindow</span></span>  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]
  
### <a name="showtoolbar"></a><span data-ttu-id="458eb-133">ShowToolbar</span><span class="sxs-lookup"><span data-stu-id="458eb-133">ShowToolbar</span></span>  
 <span data-ttu-id="458eb-134">Thao tác này hiển thị thanh công cụ rõ ràng cho người dùng.</span><span class="sxs-lookup"><span data-stu-id="458eb-134">This action explicitly shows a toolbar to the user.</span></span>  
  
|<span data-ttu-id="458eb-135">Tham số</span><span class="sxs-lookup"><span data-stu-id="458eb-135">Parameter</span></span>|<span data-ttu-id="458eb-136">Mô tả</span><span class="sxs-lookup"><span data-stu-id="458eb-136">Description</span></span>|  
|---------------|-----------------|  
||<span data-ttu-id="458eb-137">Chỉ định tên thanh công cụ để hiển thị trong trường **Dữ liệu**.</span><span class="sxs-lookup"><span data-stu-id="458eb-137">Specify the toolbar name to show in the **Data** field.</span></span>|  
  
<a name="Events"></a>   
## <a name="predefined-events"></a><span data-ttu-id="458eb-138">Sự kiện được xác định trước</span><span class="sxs-lookup"><span data-stu-id="458eb-138">Predefined events</span></span>  
 <span data-ttu-id="458eb-139">Không có bất kỳ sự kiện được xác định trước cho loại kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="458eb-139">There aren’t any predefined events available for this hosted control type.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="458eb-140">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="458eb-140">See also</span></span>  
 <span data-ttu-id="458eb-141">[Đặt cấu hình thanh công cụ trong ứng dụng của bạn](../unified-service-desk/configure-toolbars-application.md) </span><span class="sxs-lookup"><span data-stu-id="458eb-141">[Configure toolbars in your application](../unified-service-desk/configure-toolbars-application.md) </span></span>  
 <span data-ttu-id="458eb-142">[Hành động UII](../unified-service-desk/uii-actions.md) </span><span class="sxs-lookup"><span data-stu-id="458eb-142">[UII actions](../unified-service-desk/uii-actions.md) </span></span>  
 <span data-ttu-id="458eb-143">[Sự kiện](../unified-service-desk/events.md) </span><span class="sxs-lookup"><span data-stu-id="458eb-143">[Events](../unified-service-desk/events.md) </span></span>  
 <span data-ttu-id="458eb-144">[Tạo hoặc chỉnh sửa kiểm soát tổ chức](../unified-service-desk/create-edit-hosted-control.md) </span><span class="sxs-lookup"><span data-stu-id="458eb-144">[Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md) </span></span>  
 <span data-ttu-id="458eb-145">[Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="458eb-145">[Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md) </span></span>  
 <span data-ttu-id="458eb-146">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md) </span><span class="sxs-lookup"><span data-stu-id="458eb-146">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md) </span></span>  
 [<span data-ttu-id="458eb-147">Administration Guide for Unified Service Desk for Microsoft Dynamics CRM</span><span class="sxs-lookup"><span data-stu-id="458eb-147">Administration Guide for Unified Service Desk for Microsoft Dynamics CRM</span></span>](http://go.microsoft.com/fwlink/p/?LinkID=394402)
