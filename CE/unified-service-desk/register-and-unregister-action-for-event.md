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
# <a name="register-and-unregister-action-for-event-in-unified-service-desk"></a>Register and unregister action for event in Unified Service Desk
Chủ đề này mô tả các sự kiện có thể được đăng ký/chưa đăng ký cho một hành động.  
  
## <a name="uia-events"></a>Sự kiện UIA  
 Sự kiện UIA sau có thể được đăng ký cho một hành động:  
  
-   Sự kiện hành động yếu đố  
  
-   Sự kiện thay đổi thuộc tính:  
  
    -   Các sự kiện thay đổi thuộc tính yêu cầu quản lý thuộc tính mà sự kiện cần được phát triển. DDA cơ sở không hỗ trợ việc chấp nhận các đối số phụ để truy xuất tên thuộc tính.  
  
    -   Điều này được xử lý như một phần của khả năng mở rộng dữ liệu.  
  
    -   Theo mặc định, sự kiện **PropertyChange** tìm kiếm **NameProperty** và **EnabledProperty**.  
  
-   Sự kiện thay đổi máy tính để bàn chung (sự kiện cấp ứng dụng)  
  
-   Sự kiện  
  
## <a name="event-names"></a>Tên sự kiện  
 Có thể sử dụng tên sự kiện sau để đăng ký các hoạt động đăng ký/hủy đăng ký:  
  
-   [AsyncContentLoadedEvent](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.asynccontentloadedevent.aspx)  
  
-   [AutomationFocusChangedEvent](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.automationfocuschangedevent.aspx)  
  
-   [AutomationPropertyChangedEvent](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.automationpropertychangedevent.aspx)  
  
-   [LayoutInvalidatedEvent](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.layoutinvalidatedevent.aspx)  
  
-   [MenuClosedEvent](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.menuclosedevent.aspx)  
  
-   [MenuOpenedEvent](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.menuopenedevent.aspx)  
  
-   [ToolTipClosedEvent](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.tooltipclosedevent.aspx)  
  
-   [ToolTipOpenedEvent](https://msdn.microsoft.com/library/vstudio/system.windows.automation.automationelementidentifiers.tooltipopenedevent.aspx)  
  
-   [ElementAddedToSelectionEvent](https://msdn.microsoft.com/library/vstudio/system.windows.automation.selectionitempattern.elementaddedtoselectionevent.aspx)  
  
-   [ElementRemovedFromSelectionEvent](https://msdn.microsoft.com/library/vstudio/system.windows.automation.selectionitempattern.elementremovedfromselectionevent.aspx)  
  
-   [ElementSelectedEvent](https://msdn.microsoft.com/library/vstudio/system.windows.automation.selectionitempattern.elementselectedevent.aspx)  
  
-   [InvalidatedEvent](https://msdn.microsoft.com/library/system.windows.automation.selectionpattern.invalidatedevent.aspx)  
  
-   [InvokedEvent](https://msdn.microsoft.com/library/vstudio/system.windows.automation.invokepattern.invokedevent.aspx)  
  
-   [TextChangedEvent](https://msdn.microsoft.com/library/system.windows.automation.textpatternidentifiers.textchangedevent.aspx)  
  
-   [TextSelectionChangedEvent](https://msdn.microsoft.com/library/system.windows.automation.textpatternidentifiers.textselectionchangedevent.aspx)  
  
> [!NOTE]
>  Đối với một sự kiện mở/đóng Windows, kiểm soát cha mẹ phải được đăng ký cho sự kiện này. Đối với Mục menu, trước khi đăng ký sự kiện, mục menu phải hiển thị trong UI. Kiểm soát `Execute` tương ứng cần thực hiện để hiển thị.  For an application main window, the following binding needs to be added: `<UIElement type="ControlType.Window" name="ApplicationMainWindow" />` For the desktop, the following binding needs to be added: `<UIElement StartFromDesktop="True" type="ControlType.Pane" name="Desktop">`  
  
### <a name="see-also"></a>Xem thêm  
 [UIADDA](../unified-service-desk/uiadda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
