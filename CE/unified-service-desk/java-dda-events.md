---
title: JavaDDA Events in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: 'The topic describes the JavaDDA events. Java data-driven adapter (JavaDDA) provides a set of events to trigger automation executions in the Hosted Application Toolkit (HAT). The events correspond to the events in the Java runtime. Tất cả các sự kiện được liên kết với kiểm soát trên giao diện người dùng (UI). '
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
ms.assetid: ce7727d3-3b19-4615-b639-e04561038f5f
caps.latest.revision: 5
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: fdf0855c0dd09b56f1bba578f20bf0ca13d4c174
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387981"
---
# <a name="javadda-events-in-unified-service-desk"></a><span data-ttu-id="ee6c5-106">JavaDDA Events in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="ee6c5-106">JavaDDA Events in Unified Service Desk</span></span>
<span data-ttu-id="ee6c5-107">Bộ chuyển đổi định hướng dữ liệu [!INCLUDE[pn_Java](../includes/pn-java.md)] (JavaDDA) cung cấp một chuỗi sự kiện để kích hoạt thực hiện tự động hóa trong [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)].</span><span class="sxs-lookup"><span data-stu-id="ee6c5-107">[!INCLUDE[pn_Java](../includes/pn-java.md)] data-driven adapter (JavaDDA) provides a set of events to trigger automation executions in the [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)].</span></span> <span data-ttu-id="ee6c5-108">Sự kiện tương ứng với các sự kiện trong thời gian chạy [!INCLUDE[pn_Java](../includes/pn-java.md)].</span><span class="sxs-lookup"><span data-stu-id="ee6c5-108">The events correspond to the events in the [!INCLUDE[pn_Java](../includes/pn-java.md)] runtime.</span></span> <span data-ttu-id="ee6c5-109">Tất cả các sự kiện được liên kết với kiểm soát trên giao diện người dùng (UI).</span><span class="sxs-lookup"><span data-stu-id="ee6c5-109">All events are bound to the controls on the user interface (UI).</span></span> <span data-ttu-id="ee6c5-110">Để đăng ký sự kiện này, kiểm soát phải xuất hiện trong UI.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-110">To register for the event, the control must be present in the UI.</span></span> <span data-ttu-id="ee6c5-111">Sử dụng hoạt động `FindControl` để xem kiểm soát có tồn tại không.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-111">Use the `FindControl` activity to see if the control exists.</span></span> <span data-ttu-id="ee6c5-112">Chủ đề này mô tả các sự kiện DDA [!INCLUDE[pn_Java](../includes/pn-java.md)].</span><span class="sxs-lookup"><span data-stu-id="ee6c5-112">This topic describes the [!INCLUDE[pn_Java](../includes/pn-java.md)]DDA events.</span></span>  
  
## <a name="javadda-events"></a><span data-ttu-id="ee6c5-113">Sự kiện JavaDDA</span><span class="sxs-lookup"><span data-stu-id="ee6c5-113">JavaDDA events</span></span>  
 <span data-ttu-id="ee6c5-114">Bảng sau liệt kê các sự kiện có sẵn trong DDA [!INCLUDE[pn_Java](../includes/pn-java.md)]:</span><span class="sxs-lookup"><span data-stu-id="ee6c5-114">The following table lists the events available in the [!INCLUDE[pn_Java](../includes/pn-java.md)]DDA:</span></span>  
  
|<span data-ttu-id="ee6c5-115">Sự kiện</span><span class="sxs-lookup"><span data-stu-id="ee6c5-115">Event</span></span>||<span data-ttu-id="ee6c5-116">Mô tả</span><span class="sxs-lookup"><span data-stu-id="ee6c5-116">Description</span></span>|  
|-----------|-|-----------------|  
|`CheckBoxSelected`|<span data-ttu-id="ee6c5-117">Được gọi khi hộp kiểm được chọn (đã đặt đánh dấu).</span><span class="sxs-lookup"><span data-stu-id="ee6c5-117">Invoked when the check box is selected (marker set).</span></span>|  
|`CheckBoxCleared`|<span data-ttu-id="ee6c5-118">Được gọi khi hộp kiểm bị xóa (đánh dấu chưa được đặt).</span><span class="sxs-lookup"><span data-stu-id="ee6c5-118">Invoked when the check box is cleared (marker not set).</span></span>|  
|`RadioButtonSelected`|<span data-ttu-id="ee6c5-119">Được gọi khi nút radio được chọn.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-119">Invoked when the radio button is selected.</span></span>|  
|`RadioButtonCleared`|<span data-ttu-id="ee6c5-120">Được gọi khi nút radio bị xóa.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-120">Invoked when the radio button is cleared.</span></span>|  
|`ButtonPressed`|<span data-ttu-id="ee6c5-121">Được gọi khi nút được nhấn (ngược với bấm, một thông cáo báo chí).</span><span class="sxs-lookup"><span data-stu-id="ee6c5-121">Invoked when the button is pressed (versus a click, which is press-release).</span></span>|  
|`ButtonReleased`|<span data-ttu-id="ee6c5-122">Được gọi khi nút được nhả ra.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-122">Invoked when the button is released.</span></span>|  
|`GotFocus`|<span data-ttu-id="ee6c5-123">Sự kiện này được đưa lên khi kiểm soát nhắm được trọng tâm.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-123">The event is raised when the control gets the focus.</span></span>|  
|`LostFocus`|<span data-ttu-id="ee6c5-124">Sự kiện này được đưa lên khi kiểm soát mất trọng tâm.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-124">The event is raised when the control loses the focus.</span></span>|  
|`MenuSelected`|<span data-ttu-id="ee6c5-125">Được gọi khi mục menu được chọn.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-125">Invoked when the menu item is selected.</span></span>|  
|`MenuDeSelected`|<span data-ttu-id="ee6c5-126">Được gọi khi mục menu được bỏ chọn.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-126">Invoked when the menu item is unselected.</span></span>|  
|`MenuCanceled`|<span data-ttu-id="ee6c5-127">Được gọi khi lựa chọn menu bị hủy.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-127">Invoked when the menu selection is canceled.</span></span>|  
|`TreeNodeCollapsed`|<span data-ttu-id="ee6c5-128">Được gọi khi nút cây bị thu hẹp.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-128">Invoked when the tree node is collapsed.</span></span>|  
|`TreeNodeExpanded`|<span data-ttu-id="ee6c5-129">Được gọi khi nút cây được mở rộng.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-129">Invoked when the tree node is expanded.</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="ee6c5-130">Khi nhiều trường hợp của cùng một bên ngoài [!INCLUDE[pn_Java](../includes/pn-java.md)] ứng dụng được lưu trữ bên ngoài của máy tính nhân viên, chẳng hạn như khi các [!INCLUDE[pn_Java](../includes/pn-java.md)] ứng dụng là một ứng dụng phiên, [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] không thể phân biệt giữa các trường hợp, trừ khi các liên kết đã được cấp quyền theo cách mà kiểm soát có thể được phân biệt giữa hai phiên bản.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-130">When multiple instances of the same external [!INCLUDE[pn_Java](../includes/pn-java.md)] applications are hosted outside of the agent desktop, such as when the [!INCLUDE[pn_Java](../includes/pn-java.md)] application is a session application, [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] can’t distinguish between instances unless the bindings have been authored in such a way that controls can be distinguished between the two instances.</span></span> <span data-ttu-id="ee6c5-131">Với các ứng dụng `Win32` điển hình, điều này được thực hiện bằng cách hạn chế ID quá trình cụ thể nhưng là không thể với các ứng dụng [!INCLUDE[pn_Java](../includes/pn-java.md)] và cần để ý nhiều hơn trong việc cấp quyền liên kết.</span><span class="sxs-lookup"><span data-stu-id="ee6c5-131">With typical `Win32` applications, this is done by limiting to a particular process ID, but this isn’t possible with [!INCLUDE[pn_Java](../includes/pn-java.md)] applications, and greater care must be taken in authoring the binding.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ee6c5-132">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ee6c5-132">See also</span></span>  
 <span data-ttu-id="ee6c5-133">[JavaDDA](../unified-service-desk/javadda.md) </span><span class="sxs-lookup"><span data-stu-id="ee6c5-133">[JavaDDA](../unified-service-desk/javadda.md) </span></span>  
 [<span data-ttu-id="ee6c5-134">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="ee6c5-134">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
