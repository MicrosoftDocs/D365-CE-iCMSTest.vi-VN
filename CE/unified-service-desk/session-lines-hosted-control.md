---
title: Session Lines (Hosted Control) in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about Session Lines type of hosted control in Unified Service Desk.
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
ms.assetid: 7dfc327f-4a42-44e6-be16-333fd9c4c277
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
ms.openlocfilehash: 2f86f4656a7c915a8f8ad5b0aec34b7b7c47d1bc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385705"
---
# <a name="session-lines-hosted-control"></a><span data-ttu-id="fcac9-103">Session Lines (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="fcac9-103">Session Lines (Hosted Control)</span></span>
<span data-ttu-id="fcac9-104">Sử dụng loại **Dòng phiên** của kiểm soát tổ chức để đặt cấu hình thông tin tổng quan phiên cho các phiên trong ứng dụng tổng đài viên của bạn.</span><span class="sxs-lookup"><span data-stu-id="fcac9-104">Use **Session Lines** type of hosted control to configure session overview information for sessions in your agent application.</span></span> <span data-ttu-id="fcac9-105">This hosted control reads the overview information that you configure in your agent application using **Session Lines** (**Settings** > **Unified Service Desk** > **Session Lines**), and an instance of this hosted control type must be available in your agent application for the session overview information to be displayed.</span><span class="sxs-lookup"><span data-stu-id="fcac9-105">This hosted control reads the overview information that you configure in your agent application using **Session Lines** (**Settings** > **Unified Service Desk** > **Session Lines**), and an instance of this hosted control type must be available in your agent application for the session overview information to be displayed.</span></span> <span data-ttu-id="fcac9-106">For more information about session overview, see [Session overview](../unified-service-desk/session-management-unified-service-desk.md#SessionOverview) and [Define session overview information](../unified-service-desk/configure-session-information.md#SessionOverview).</span><span class="sxs-lookup"><span data-stu-id="fcac9-106">For more information about session overview, see [Session overview](../unified-service-desk/session-management-unified-service-desk.md#SessionOverview) and [Define session overview information](../unified-service-desk/configure-session-information.md#SessionOverview).</span></span>  
  
<a name="Create"></a>   
## <a name="create-a-session-lines-hosted-control"></a><span data-ttu-id="fcac9-107">Tạo kiểm soát tổ chức dòng phiên</span><span class="sxs-lookup"><span data-stu-id="fcac9-107">Create a Session Lines hosted control</span></span>  
 <span data-ttu-id="fcac9-108">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span><span class="sxs-lookup"><span data-stu-id="fcac9-108">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span></span> <span data-ttu-id="fcac9-109">Phần này cung cấp thông tin về các trường cụ thể mà là duy nhất cho loại kiểm soát tổ chức **Dòng Phiên**.</span><span class="sxs-lookup"><span data-stu-id="fcac9-109">This section provides information about the specific fields that are unique to the **Session Lines** hosted control type.</span></span> <span data-ttu-id="fcac9-110">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="fcac9-110">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span></span>  
  
 <span data-ttu-id="fcac9-111">![Create a Session Lines hosted control](../unified-service-desk/media/crm-itpro-usd-sessionlines.png "Create a Session Lines hosted control")</span><span class="sxs-lookup"><span data-stu-id="fcac9-111">![Create a Session Lines hosted control](../unified-service-desk/media/crm-itpro-usd-sessionlines.png "Create a Session Lines hosted control")</span></span>  
  
 <span data-ttu-id="fcac9-112">Trong màn hình Kiểm soát được lưu trữ mới:</span><span class="sxs-lookup"><span data-stu-id="fcac9-112">In the New Hosted Control screen:</span></span>  
  
- <span data-ttu-id="fcac9-113">Under **[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]** area, select **Session Lines** from the **USD Component Type** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="fcac9-113">Under **[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]** area, select **Session Lines** from the **USD Component Type** drop-down list.</span></span>  
  
- <span data-ttu-id="fcac9-114">Trường **Hiển thị nhóm** hiển thị bảng điều khiển nơi hiển thị kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="fcac9-114">The **Display Group** field displays the panel where this hosted control will be displayed.</span></span> <span data-ttu-id="fcac9-115">**Bảng điều khiển trình khám phá phiên** là bảng điều khiển phổ biến nhất cho loại kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="fcac9-115">**SessionExplorerPanel** is the most common panel for this hosted control type.</span></span> <span data-ttu-id="fcac9-116">For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md#Panels)</span><span class="sxs-lookup"><span data-stu-id="fcac9-116">For information about various panels available in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Panels in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md#Panels)</span></span>  
  
  <span data-ttu-id="fcac9-117">For information about **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="fcac9-117">For information about **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span></span>  
  
<a name="Actions"></a>   
## <a name="predefined-uii-actions"></a><span data-ttu-id="fcac9-118">Predefined UII actions</span><span class="sxs-lookup"><span data-stu-id="fcac9-118">Predefined UII actions</span></span>  
 <span data-ttu-id="fcac9-119">These are the predefined actions for this hosted control type.</span><span class="sxs-lookup"><span data-stu-id="fcac9-119">These are the predefined actions for this hosted control type.</span></span>  
  
### <a name="fireevent"></a><span data-ttu-id="fcac9-120">FireEvent</span><span class="sxs-lookup"><span data-stu-id="fcac9-120">FireEvent</span></span>  
 <span data-ttu-id="fcac9-121">Fires a user-defined event from this hosted control.</span><span class="sxs-lookup"><span data-stu-id="fcac9-121">Fires a user-defined event from this hosted control.</span></span>  
  
|<span data-ttu-id="fcac9-122">Tham số</span><span class="sxs-lookup"><span data-stu-id="fcac9-122">Parameter</span></span>|<span data-ttu-id="fcac9-123">Mô tả</span><span class="sxs-lookup"><span data-stu-id="fcac9-123">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="fcac9-124">tên</span><span class="sxs-lookup"><span data-stu-id="fcac9-124">name</span></span>|<span data-ttu-id="fcac9-125">Tên của sự kiện do người dùng xác định.</span><span class="sxs-lookup"><span data-stu-id="fcac9-125">Name of the user-defined event.</span></span>|  
  
 <span data-ttu-id="fcac9-126">Tất cả tên tiếp theo = cặp giá trị trở thành tham số cho sự kiện này.</span><span class="sxs-lookup"><span data-stu-id="fcac9-126">All subsequent name=value pairs become the parameters to the event.</span></span> <span data-ttu-id="fcac9-127">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span><span class="sxs-lookup"><span data-stu-id="fcac9-127">For more information about creating a user-defined event, see [Create a user-defined event](../unified-service-desk/create-user-defined-event.md).</span></span>  
  
### <a name="realignwindow"></a><span data-ttu-id="fcac9-128">RealignWindow</span><span class="sxs-lookup"><span data-stu-id="fcac9-128">RealignWindow</span></span>  
[!INCLUDE[cc_RealignWindow_Action](../includes/cc-realignwindow-action.md)]
  
<a name="Events"></a>   
## <a name="predefined-events"></a><span data-ttu-id="fcac9-129">Sự kiện được xác định trước</span><span class="sxs-lookup"><span data-stu-id="fcac9-129">Predefined events</span></span>  
 <span data-ttu-id="fcac9-130">Không có bất kỳ sự kiện được xác định trước nào cho loại kiểm soát tổ chức này.</span><span class="sxs-lookup"><span data-stu-id="fcac9-130">There aren’t any predefined events for this hosted control type.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="fcac9-131">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="fcac9-131">See also</span></span>  
 <span data-ttu-id="fcac9-132">[Session management in Unified Service Desk](../unified-service-desk/session-management-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="fcac9-132">[Session management in Unified Service Desk](../unified-service-desk/session-management-unified-service-desk.md) </span></span>  
 <span data-ttu-id="fcac9-133">[Session Tabs (Hosted Control)](../unified-service-desk/session-tabs-hosted-control.md) </span><span class="sxs-lookup"><span data-stu-id="fcac9-133">[Session Tabs (Hosted Control)](../unified-service-desk/session-tabs-hosted-control.md) </span></span>  
 <span data-ttu-id="fcac9-134">[Cách 5: Hiển thị thông tin phiên bổ sung bằng cách hiển thị tên và dữ liệu tổng quan về phiên](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md) </span><span class="sxs-lookup"><span data-stu-id="fcac9-134">[Walkthrough 5: Display enhanced session information by displaying session name and overview data](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md) </span></span>  
 [<span data-ttu-id="fcac9-135">Hosted control types and action/event reference</span><span class="sxs-lookup"><span data-stu-id="fcac9-135">Hosted control types and action/event reference</span></span>](../unified-service-desk/hosted-control-types-action-event-reference.md)
