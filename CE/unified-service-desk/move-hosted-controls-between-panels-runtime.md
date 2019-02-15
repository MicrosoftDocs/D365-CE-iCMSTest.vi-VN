---
title: Move hosted controls between panels at runtime in Unified Service Desk for Dynamics 365 for Customer Engagement apps Customer Enagagement| MicrosoftDocs
description: Learn about moving hosted controls between panels at runtime Unified Service Desk.
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
ms.assetid: 77956def-6316-45b2-9fc3-eee2b06bb505
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
ms.openlocfilehash: 4d5b59caa6520510aeb42c9cf03e923889f17ce5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386083"
---
# <a name="move-hosted-controls-between-panels-at-runtime-unified-service-desk"></a>Move hosted controls between panels at runtime Unified Service Desk
[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]cung cấp khả năng di chuyển ứng dụng giữa các bảng điều khiển tại thời gian chạy. Bạn có thể làm như vậy bằng cách sử dụng thao tác [MoveToPanel](../unified-service-desk/global-manager-hosted-control.md#MoveToPanel) cho loại kiểm soát tổ chức của **Trình quản lý chung**. Thao tác này có hai tham số:  
  
- **ứng dụng**: tên của loại hình kiểm soát tổ chức được di chuyển.  
  
- **bảng điều khiển**: bảng điều khiển đích cho kiểm soát tổ chức.  
  
  This can also be done through code where developers can program this while creating new panel types. [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] provides a special panel called the `Unknown` panel. Bảng điều khiển này là một bộ nhớ tạm thời cho các kiểm soát tổ chức khi dự định đặt bố cục bảng điều khiển, chưa được nạp. Let’s suppose that you have a **Horizontal Split** panel populated with a **CRM Page** type of hosted control, but you have closed your **Horizontal Split** panel. The **CRM Page** hosted control is still loaded but has been moved to the **Unknown** panel, which is not visible. Once the **Horizontal Split** panel is loaded again, the **CRM Page** hosted control would be moved from the **Unknown** panel to the appropriate panel again.  
  
```  
IDesktopFeatureAccess desktop = AifServiceContainer.Instance.GetService<IDesktopFeatureAccess>();  
if (desktop != null)  
{  
   desktop.SendApplicationToUnknownPanel(this, tabApp);  
}  
```  
  
 The [IDesktopFeatureAccess](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.basecontrol.idesktopfeatureaccess) class has another function, [String)](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.basecontrol.idesktopfeatureaccess.moveapplicationtopanel\(microsoft.uii.csr.ihostedapplication,system.string\)), which allows you to move a hosted control from and to arbitrary panels. Chức năng này phải có tham chiếu đến các ứng dụng tổ chức mà bạn muốn di chuyển và chuỗi đại diện cho tên bảng điều khiển chính là tên của kiểm soát tổ chức được xác định làm bố cục bảng điều khiển.  
  
### <a name="see-also"></a>Xem thêm  
 [Panels, panel types, and panel layouts in Unified Service Desk](../unified-service-desk/panels-panel-types-panel-layouts.md)   
 [Trình quản lý chung (Kiểm soát tổ chức)](../unified-service-desk/global-manager-hosted-control.md)   
 [Trang CRM (Kiểm soát tổ chức)](../unified-service-desk/crm-page-hosted-control.md)
