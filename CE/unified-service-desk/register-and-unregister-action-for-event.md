---
title: Register and unregister action for event in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The topic describes the events that can be registered/unregistered for an action.
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
ms.assetid: 26d5f5a6-2c9d-421c-bf44-1a87afdb5c33
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
ms.openlocfilehash: d36da0fd9fc5569e41f0fb7ed90cc27c7bf91bb5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386227"
---
# <a name="register-and-unregister-action-for-event-in-unified-service-desk"></a><span data-ttu-id="694a9-103">Register and unregister action for event in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="694a9-103">Register and unregister action for event in Unified Service Desk</span></span>
<span data-ttu-id="694a9-104">Chủ đề này mô tả các sự kiện có thể được đăng ký/chưa đăng ký cho một hành động.</span><span class="sxs-lookup"><span data-stu-id="694a9-104">This topic describes the events that can be registered/unregistered for an action.</span></span>  
  
## <a name="uia-events"></a><span data-ttu-id="694a9-105">Sự kiện UIA</span><span class="sxs-lookup"><span data-stu-id="694a9-105">UIA events</span></span>  
 <span data-ttu-id="694a9-106">Sự kiện UIA sau có thể được đăng ký cho một hành động:</span><span class="sxs-lookup"><span data-stu-id="694a9-106">The following UIA events can be registered for an action:</span></span>  
  
-   <span data-ttu-id="694a9-107">Sự kiện hành động yếu đố</span><span class="sxs-lookup"><span data-stu-id="694a9-107">Element action events</span></span>  
  
-   <span data-ttu-id="694a9-108">Sự kiện thay đổi thuộc tính:</span><span class="sxs-lookup"><span data-stu-id="694a9-108">Property change events:</span></span>  
  
    -   <span data-ttu-id="694a9-109">Các sự kiện thay đổi thuộc tính yêu cầu quản lý thuộc tính mà sự kiện cần được phát triển.</span><span class="sxs-lookup"><span data-stu-id="694a9-109">Property change events require monitoring of the property for which the event needs to be raised.</span></span> <span data-ttu-id="694a9-110">DDA cơ sở không hỗ trợ việc chấp nhận các đối số phụ để truy xuất tên thuộc tính.</span><span class="sxs-lookup"><span data-stu-id="694a9-110">Base DDA does not support accepting the extra argument for retrieving the property name.</span></span>  
  
    -   <span data-ttu-id="694a9-111">Điều này được xử lý như một phần của khả năng mở rộng dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="694a9-111">This is handled as part of data extensibility.</span></span>  
  
    -   <span data-ttu-id="694a9-112">Theo mặc định, sự kiện **PropertyChange** tìm kiếm **NameProperty** và **EnabledProperty**.</span><span class="sxs-lookup"><span data-stu-id="694a9-112">By default, the **PropertyChange** event looks for **NameProperty** and **EnabledProperty**.</span></span>  
  
-   <span data-ttu-id="694a9-113">Sự kiện thay đổi máy tính để bàn chung (sự kiện cấp ứng dụng)</span><span class="sxs-lookup"><span data-stu-id="694a9-113">Global desktop change events (application-level events)</span></span>  
  
-   <span data-ttu-id="694a9-114">Sự kiện</span><span class="sxs-lookup"><span data-stu-id="694a9-114">Events</span></span>  
  
## <a name="event-names"></a><span data-ttu-id="694a9-115">Tên sự kiện</span><span class="sxs-lookup"><span data-stu-id="694a9-115">Event names</span></span>  
 <span data-ttu-id="694a9-116">Có thể sử dụng tên sự kiện sau để đăng ký các hoạt động đăng ký/hủy đăng ký:</span><span class="sxs-lookup"><span data-stu-id="694a9-116">The following event names can be used to subscribe in the register/unregister activities:</span></span>  
  
-   [<span data-ttu-id="694a9-117">AsyncContentLoadedEvent</span><span class="sxs-lookup"><span data-stu-id="694a9-117">AsyncContentLoadedEvent</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.asynccontentloadedevent.aspx)  
  
-   [<span data-ttu-id="694a9-118">AutomationFocusChangedEvent</span><span class="sxs-lookup"><span data-stu-id="694a9-118">AutomationFocusChangedEvent</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.automationfocuschangedevent.aspx)  
  
-   [<span data-ttu-id="694a9-119">AutomationPropertyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="694a9-119">AutomationPropertyChangedEvent</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.automationpropertychangedevent.aspx)  
  
-   [<span data-ttu-id="694a9-120">LayoutInvalidatedEvent</span><span class="sxs-lookup"><span data-stu-id="694a9-120">LayoutInvalidatedEvent</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.layoutinvalidatedevent.aspx)  
  
-   [<span data-ttu-id="694a9-121">MenuClosedEvent</span><span class="sxs-lookup"><span data-stu-id="694a9-121">MenuClosedEvent</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.menuclosedevent.aspx)  
  
-   [<span data-ttu-id="694a9-122">MenuOpenedEvent</span><span class="sxs-lookup"><span data-stu-id="694a9-122">MenuOpenedEvent</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.menuopenedevent.aspx)  
  
-   [<span data-ttu-id="694a9-123">ToolTipClosedEvent</span><span class="sxs-lookup"><span data-stu-id="694a9-123">ToolTipClosedEvent</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.tooltipclosedevent.aspx)  
  
-   [<span data-ttu-id="694a9-124">ToolTipOpenedEvent</span><span class="sxs-lookup"><span data-stu-id="694a9-124">ToolTipOpenedEvent</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.tooltipopenedevent.aspx)  
  
-   [<span data-ttu-id="694a9-125">ElementAddedToSelectionEvent</span><span class="sxs-lookup"><span data-stu-id="694a9-125">ElementAddedToSelectionEvent</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.selectionitempattern.elementaddedtoselectionevent.aspx)  
  
-   [<span data-ttu-id="694a9-126">ElementRemovedFromSelectionEvent</span><span class="sxs-lookup"><span data-stu-id="694a9-126">ElementRemovedFromSelectionEvent</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.selectionitempattern.elementremovedfromselectionevent.aspx)  
  
-   [<span data-ttu-id="694a9-127">ElementSelectedEvent</span><span class="sxs-lookup"><span data-stu-id="694a9-127">ElementSelectedEvent</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.selectionitempattern.elementselectedevent.aspx)  
  
-   [<span data-ttu-id="694a9-128">InvalidatedEvent</span><span class="sxs-lookup"><span data-stu-id="694a9-128">InvalidatedEvent</span></span>](https://msdn.microsoft.com/library/system.windows.automation.selectionpattern.invalidatedevent.aspx)  
  
-   [<span data-ttu-id="694a9-129">InvokedEvent</span><span class="sxs-lookup"><span data-stu-id="694a9-129">InvokedEvent</span></span>](https://msdn.microsoft.com/library/vstudio/system.windows.automation.invokepattern.invokedevent.aspx)  
  
-   [<span data-ttu-id="694a9-130">TextChangedEvent</span><span class="sxs-lookup"><span data-stu-id="694a9-130">TextChangedEvent</span></span>](https://msdn.microsoft.com/library/system.windows.automation.textpatternidentifiers.textchangedevent.aspx)  
  
-   [<span data-ttu-id="694a9-131">TextSelectionChangedEvent</span><span class="sxs-lookup"><span data-stu-id="694a9-131">TextSelectionChangedEvent</span></span>](https://msdn.microsoft.com/library/system.windows.automation.textpatternidentifiers.textselectionchangedevent.aspx)  
  
> [!NOTE]
>  <span data-ttu-id="694a9-132">Đối với một sự kiện mở/đóng Windows, kiểm soát cha mẹ phải được đăng ký cho sự kiện này.</span><span class="sxs-lookup"><span data-stu-id="694a9-132">For a Windows open/closed event, the parent control should be registered for the event.</span></span> <span data-ttu-id="694a9-133">Đối với Mục menu, trước khi đăng ký sự kiện, mục menu phải hiển thị trong UI.</span><span class="sxs-lookup"><span data-stu-id="694a9-133">For menu Items, before registering for the event, the menu item should be visible in the UI.</span></span> <span data-ttu-id="694a9-134">Kiểm soát `Execute` tương ứng cần thực hiện để hiển thị.</span><span class="sxs-lookup"><span data-stu-id="694a9-134">The corresponding `Execute` control needs to be done to make this visible.</span></span>  <span data-ttu-id="694a9-135">For an application main window, the following binding needs to be added: `<UIElement type="ControlType.Window" name="ApplicationMainWindow" />` For the desktop, the following binding needs to be added: `<UIElement StartFromDesktop="True" type="ControlType.Pane" name="Desktop">`</span><span class="sxs-lookup"><span data-stu-id="694a9-135">For an application main window, the following binding needs to be added: `<UIElement type="ControlType.Window" name="ApplicationMainWindow" />` For the desktop, the following binding needs to be added: `<UIElement StartFromDesktop="True" type="ControlType.Pane" name="Desktop">`</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="694a9-136">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="694a9-136">See also</span></span>  
 <span data-ttu-id="694a9-137">[UIADDA](../unified-service-desk/uiadda.md) </span><span class="sxs-lookup"><span data-stu-id="694a9-137">[UIADDA](../unified-service-desk/uiadda.md) </span></span>  
 [<span data-ttu-id="694a9-138">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="694a9-138">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
