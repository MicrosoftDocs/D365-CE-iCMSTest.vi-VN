---
title: What's new in Unified Service Desk for developers and customizers | MicrosoftDocs
description: Learn about the new features for developers and customizers in Unified Service Desk.
keywords: ''
ms.date: 12/17/2018
ms.service:
- dynamics-365-customerservice
ms.custom:
- dyn365-USD
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 1c6da924-cfef-4cbf-a6d5-63af8f1a640d
author: kabala123
ms.author: kabala
manager: shujoshi
ms.tgt_pltfrm: ''
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 49b785b90063546a209624b18257faa6e3b15124
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386033"
---
# <a name="whats-new-in-unified-service-desk-for-developers-and-customizers"></a>Tính năng mới trong Unified Service Desk cho nhà phát triển và người tùy chỉnh

::: moniker range="dynamics-usd-4"

##  <a name="whats-new-in-includepn-unified-service-desk-4-1includespn-unified-service-desk-4-1md"></a>Nội dung mới trong [!INCLUDE[pn-unified-service-desk-4-1](../includes/pn-unified-service-desk-4-1.md)]

### <a name="preview-hosting-application-in-microsoft-using-the-edge-process-hosting-type"></a>Preview: Hosting application in Microsoft using the Edge Process hosting type

Use the Microsoft Edge, the modern, faster, safer and responsive web browser to host applications in Unified Service Desk.
Select Edge Process as the hosting method for the CRM Dialog, CRM Page, KM Control, and Standard Web Application type of hosted controls.

More information: [Edge process](edge-process.md)

## <a name="whats-new-in-includepn-unified-service-desk-4-0includespn-unified-service-desk-4-0md"></a>Nội dung mới trong [!INCLUDE[pn-unified-service-desk-4-0](../includes/pn-unified-service-desk-4-0.md)]

This topic contains information about changes in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] for developers and system customizers. 

### <a name="general-availability-support-for-unified-interface-apps-in-unified-service-desk"></a>General Availability: Support for Unified Interface apps in Unified Service Desk

With the release of [!include[pn-crm-9-0-0-online](../includes/pn-crm-9-0-0-online.md)], we've introduced a new user experience -[Unified Interface](/dynamics365/customer-engagement/admin/about-unified-interface), which uses responsive web design principles to provide an optimal viewing and interaction experience for any screen size, device, or orientation.  [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] supports the apps built using Unified Interface framework. That is, you can load a URL or page from Dynamics 365 for Customer Engagement apps, which is built based on the Unified Interface framework.

A new hosted control type called **Unified Interface Page** is introduced, which you need to set as **USD Component Type** while creating a hosted control to use a URL or page from [!include[pn-dynamics-crm](../includes/pn-dynamics-crm.md)] apps.

The experience of the supportability is that the Unified Interface Page hosted control type exposes number of predefined UII actions and events that are unique to handling of Dynamics 365 for Customer Engagement apps windows built using Unified Interface framework including list manipulation actions, and a find action for displaying a quick search or advanced search page.

## <a name="preview-features"></a>Preview features

### <a name="stack-notification-in-unified-service-desk"></a>Thông báo xếp chồng trong Unified Service Desk

You can configure stack notifications in Unified Service Desk to display popup notification messages to your customer service agents that contains general information or some customer or process-related information that the agent can act on.
Điều này sẽ tạo điều kiện cho các thông báo Toast đồng thời trong môi trường đa phiên. 

Two new parameters are introduced: **stack** and **stackHeight**, for which you can set the values to show the notifications in a stack with a certain height.

[!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Stack Notifications](configure-notifications-unified-service-desk.md#stack-notifications) and [Popup Notification Hosted Control](popup-notification-hosted-control.md)

### <a name="switch-between-local-sessions-and-between-local-and-global-sessions"></a>Switch between local sessions, and between local and global sessions

When you are working on a case (local session) and want to review your Dashboard (global session) or another case (local session), you can easily switch from the case to Dashboard or another case, without affecting your session timer. Điều này có nghĩa là khi bạn chuyển từ phiên cục bộ, bộ đếm thời gian phiên của bạn sẽ không đếm cho đến khi bạn chuyển ngược lại về phiên. This helps in efficiently measure the agents' productivity.

Using **SwitchSession** action, you can now switch between local sessions. Also, you can switch sessions between local and global by passing the global session ID retrieved from the context using the replacement parameter.

[!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [SwitchSession Action](session-tabs-hosted-control.md#switchsession)

::: moniker-end

::: moniker range="dynamics-usd-3"

<a name="WhatsNew33"></a>   

## <a name="whats-new-in-include-pn-unified-service-desk-3-3includespn-unified-service-desk-3-3md"></a>Nội dung mới trong [!INCLUDE [pn-unified-service-desk-3-3](../includes/pn-unified-service-desk-3-3.md)]

Developers and customizers will be able to use the following new features in the [!INCLUDE [pn-unified-service-desk-3-3](../includes/pn-unified-service-desk-3-3.md)] release.

### <a name="videos"></a>Video

See the video to know [What's New in Unified Service Desk 3.3](https://go.microsoft.com/fwlink/?linkid=2008774).

### <a name="public-preview-feature-support-for-unified-interface-apps-in-includepnunifiedservicedeskincludespn-unified-service-deskmd"></a>Public Preview Feature: Support for Unified Interface Apps in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]

With this release, [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] supports the apps built using Unified Interface framework. That is, you can load a URL or page from Dynamics 365 for Customer Engagement apps, which is built based on the Unified Interface framework.

The experience of the supportability is that the Unified Interface Page hosted control type exposes number of predefined UII actions and events that are unique to handling of Dynamics 365 for Customer Engagement apps windows built using Unified Interface framework including list manipulation actions, and a find action for displaying a quick search or advanced search page. 

A new hosted control type called **Unified Interface Page** is introduced, which you need to set as **USD Component Type** while creating a hosted control to use URL or page from [!include[pn-dynamics-crm](../includes/pn-dynamics-crm.md)] apps. 

When you sign in to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], you can see an app module selection window that is introduced as part of the Unified Interface supportability. You need to select a Unified Interface app from the list and experience the app in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].

### <a name="custom-styles-field--in-toolbar"></a>Custom Styles field  in Toolbar

You can now customize the toolbar in Unified Service Desk using the custom styles field in the Toolbar configuration window.  The Custom Styles field supports Extensible Application Markup Language (XAML) that defines <xref:System.Windows.ResourceDictionary> of <xref:System.Windows.Style> and <xref:System.Windows.Media.Brush> resources.
 
The resources in the dictionary refers to other resources that are available on Unified Service Desk client application. Loading and parsing the XAML string is performed at runtime to create <xref:System.Windows.ResourceDictionary> and merge the resources of the toolbar control with the <xref:System.Windows.ResourceDictionary>. In addition, the <xref:System.Windows.ResourceDictionary> can have styles for button types inside a toolbar. Using the styles, you can customize the toolbars and buttons.

[!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configure toolbars in your application](../unified-service-desk/configure-toolbars-application.md) and [Toolbars in Unified Service Desk](../unified-service-desk/toolbars-unified-service-desk.md)

<a name="WhatsNew32"></a>   

## <a name="whats-new-in-include-pn-unified-service-desk-3-2includespn-unified-service-desk-3-2md"></a>Nội dung mới trong [!INCLUDE [pn-unified-service-desk-3-2](../includes/pn-unified-service-desk-3-2.md)] 

There are no developer/customizer-specific changes in this release. For a list of new features in this release, see [New feature information for administrators](admin/whats-new-unified-service-desk-administrators.md)

<a name="WhatsNew31"></a>   
## <a name="whats-new-in-include-pn-unified-service-desk-3-1includespn-unified-service-desk-3-1md"></a>Nội dung mới trong [!INCLUDE [pn-unified-service-desk-3-1](../includes/pn-unified-service-desk-3-1.md)] 

There are no developer/customizer-specific changes in this release. For a list of new features in this release, see [New feature information for administrators](admin/whats-new-unified-service-desk-administrators.md)


<a name="WhatsNew3"></a>   
## <a name="whats-new-in-include-pn-unified-service-desk-3-0includespn-unified-service-desk-3-0md"></a>Nội dung mới trong [!INCLUDE [pn-unified-service-desk-3-0](../includes/pn-unified-service-desk-3-0.md)]  
 
Developers and customizers will be able to use the following new features in the [!INCLUDE [pn-unified-service-desk-3-0](../includes/pn-unified-service-desk-3-0.md)] release.

### <a name="display-customer-data-faster-to-your-agents-by-pre-fetching-entity-data-from-customer-engagement"></a>Display customer data faster to your agents by pre-fetching entity data from Customer Engagement

[!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] giờ đã cho phép bạn tải thông tin có liên quan đối với một bản ghi thực thể trong ngữ cảnh cùng với trang bản ghi thực thể mà không cần phải đợi cho đến khi đã tải toàn bộ trang web thực thể trong ứng dụng khách. Thông tin thực thể tìm nạp được điền trong ngữ cảnh [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] để kích hoạt mọi kiểm soát tổ chức nhằm nhanh chóng hiển thị thông tin thực thể có liên quan trên ứng dụng khách. Use the new **Pre-Fetch Data** check box while configuring a **CRM Page** type of hosted control. 

Đồng thời, một sự kiện mới có tên **DataReady** đã được thêm vào loại **Trang CRM** của kiểm soát tổ chức để giúp bạn thực hiện hành động ngay khi thông tin có liên quan cho một bản ghi thực thể được tải trong ngữ cảnh [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)]. 

More information: [CRM Page (Hosted Control)](crm-page-hosted-control.md)

### <a name="asynchronously-create-entity-records-to-prevent-execution-blocking"></a>Tạo các bản ghi thực thể không đồng bộ để tránh trường hợp chặn thực thi

The **CreateEntity** action on the Global Manager hosted control synchronously creates an entity record on the main thread, and [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] has to wait for the **CreateEntity** action to complete before proceeding with the next task. Điều này dẫn đến tình trạng [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] không phản hồi cho đến khi hoàn thành xong hành động, và đây có thể là điều không mong muốn trong một số trường hợp.

In this release, we are introducing a new data parameter, **RunAsync**, for the **CreateEntity** action that you can use to set the action to run asynchronously so that [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] is not blocked and remains responsive during the action execution.

More information: [CreateEntity](global-manager-hosted-control.md#createentity) action

### <a name="keyboard-shortcuts-for-toolbar-buttons-notifications-and-panel-navigation"></a>Lối tắt bàn phím cho các nút thanh công cụ, thông báo và điều hướng bảng điều khiển

- Các nút trên thanh công cụ giờ đã hỗ trợ lối tắt bàn phím và có thể được xác định trong khi tạo nút trên thanh công cụ. Điều này cho phép tổng đài viên thực thi các hành động đã được đặt cấu hình đối với nút thanh công cụ từ bất kỳ vị trí nào trong máy khách [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] mà không cần phải bấm vào nút. Các phím lối tắt cho một nút trên thanh công cụ chỉ hoạt động nếu các điều kiện hiển hiện và kích hoạt cho nút, các nút trước đó (nếu có) và bản thân thanh công cụ đánh giá là đúng. More information: [Toolbars in Unified Service Desk](toolbars-unified-service-desk.md)

- [Thông báo](configure-notifications-unified-service-desk.md) in [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] giờ đã hỗ trợ lối tắt bàn phím. Sử dụng lối tắt bàn phím mặc định Alt+1 để đặt trọng tâm của bạn vào một thông báo. Nếu có nhiều thông báo hiển thị, bạn có thể ấn Alt+1 lặp lại để di chuyển tuần hoàn qua tất cả các thông báo hiện hoạt trên màn hình. Để thay đổi phím lối tắt trên bàn phím đối với thông báo, hãy dùng tùy chọn UII **PopupNavigationShortcut** mới để chỉ định các phím lối tắt theo ý muốn.

- Trước đây, lối tắt bàn phím, Ctrl+0, được dùng để di chuyển tuần hoàn theo chiều ngang qua tất cả các bảng điều khiển hiện hoạt, và bạn không thể thay đổi lối tắt này sang bất kỳ tổ hợp phím nào khác.
  Hiện tại, bạn có thể chỉ định các phím lối tắt theo ý muốn để di chuyển tuần hoàn theo chiều ngang qua tất cả các bảng điều khiển hiện hoạt bằng cách dùng UII mới có tên **PanelNavigationShortcut**. More information: [Keyboard shortcuts for panels](keyboard-shortcuts-panels.md)

### <a name="debugger-control-enhancements"></a>Nâng cao kiểm soát trình gỡ lỗi

Kiểm soát Trình gỡ lỗi đã được nâng cao để đưa ra những tính năng mới sau đây, giúp nhà phát triển và người tùy chỉnh trong việc gỡ lỗi và khắc phục sự cố mã tùy chỉnh và thay đổi cấu hình dễ dàng hơn:

-   **Sắp xếp dữ liệu**: Sắp xếp dữ liệu trong các cột của thẻ **Cuộc gọi Hành động** để hiển thị dữ liệu theo thứ tự tăng dần hoặc giảm dần trong một cột. Bạn cũng có thể đặt lại tất cả các dữ liệu cột đã sắp xếp để trở về dữ liệu mặc định hiển thị trong thẻ **Cuộc gọi Hành động** bằng cách chọn biểu tượng **Đặt lại các cột đã sắp xếp**.

-   **Phát lại cuộc gọi hành động**: Nhanh chóng chạy lại một cuộc gọi hành động bằng cách bấm chuột phải vào bản ghi cuộc gọi hành động trong thẻ **Cuộc gọi Hành động**, sau đó chọn **Phát lại** từ menu lối tắt. Bạn cũng có thể chọn chỉnh sửa tham số dữ liệu cho một cuộc gọi hành động và chạy lại bằng cách bấm chuột phải vào cuộc gọi hành động trong thẻ **Cuộc gọi Hành động**, sau đó chọn **Sửa** từ menu lối tắt. Thao tác này sẽ tải định nghĩa cuộc gọi hành động trong thẻ **Hành động Trực tiếp**, tại đây, bạn có thể sửa đổi thông tin yêu cầu và chạy lại.

-   **Phát lại sự kiện**: Nhanh chóng chạy lại một sự kiện bằng cách bấm chuột phải vào bản ghi sự kiện trong thẻ **Cuộc gọi Hành động**, sau đó chọn **Phát lại** từ menu lối tắt. Không như cuộc gọi hành động, bạn không thể chỉnh sửa một sự kiện và chạy lại.

-   **Cải thiện thẻ Hành động Trực tiếp**: Xóa thông tin khỏi tất cả các trường trong thẻ **Hành động Trực tiếp** bằng cách chọn biểu tượng **Xóa**.

-   **Cải thiện đối với tham số thay thế:** Trong thẻ **Tham số Dữ liệu**, bạn giờ có thể thêm một tham số thay thế cùng với giá trị của tham số đó, sao chép giá trị của tham số thay thế và chỉnh sửa một giá trị của tham số thay thế bằng cách dùng các biểu tượng mới.

### <a name="configure-jaws-screen-reader-support"></a>Đặt cấu hình hỗ trợ bộ đọc màn hình JAWS

[!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] giờ đã hỗ trợ [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] (Truy cập Công việc kèm theo Giọng nói) phiên bản 18 cho bộ đọc màn hình Windows cho đầu ra giọng nói trong máy khách [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)]. Tất cả các kiểm soát là một phần của gói Máy khách Web [!INCLUDE[pn-ms-dyn-365](../includes/pn-ms-dyn-365.md)] đều tuân thủ [!INCLUDE[pn-jaws](../includes/pn-jaws.md)].
For the custom controls that you develop as part of the solution package, you need to define the necessary properties to make the controls JAWS compliant.

Bạn có thể đặt cấu hỗ trợ bộ đọc màn hình [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] cho các kiểm soát có thể đặt trọng tâm.
By design of the product, the tab position does not focus the non-focusable controls. Hence, [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] does not read controls that are non focusable, such as text block, image, and labels. Tuy nhiên, có một cách giải quyết là bạn tạo một kiểm soát phi trọng tâm dưới dạng kiểm soát người dùng (đưa vào \<UserControl\>) để hỗ trợ bộ đọc màn hình [!INCLUDE[pn-jaws](../includes/pn-jaws.md)].

Đồng thời, bộ đọc màn hình [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] không hỗ trợ đọc văn bản chú giải công cụ cho nút. But, you can create [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] custom scripts and use  in [!INCLUDE[pn-unified-service-desk](../includes/pn-unified-service-desk.md)] to enable [!INCLUDE[pn-jaws](../includes/pn-jaws.md)] screen reader to read tooltip text.

More information: [Configure JAWS screen reader support](configure-jaws-screen-reader-support.md)

::: moniker-end

### <a name="see-also"></a>Xem thêm  
 [What’s New in Unified Service Desk for administrators](admin/whats-new-unified-service-desk-administrators.md)   
 
