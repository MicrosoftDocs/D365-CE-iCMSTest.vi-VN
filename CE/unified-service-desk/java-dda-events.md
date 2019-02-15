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
# <a name="javadda-events-in-unified-service-desk"></a>JavaDDA Events in Unified Service Desk
Bộ chuyển đổi định hướng dữ liệu [!INCLUDE[pn_Java](../includes/pn-java.md)] (JavaDDA) cung cấp một chuỗi sự kiện để kích hoạt thực hiện tự động hóa trong [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)]. Sự kiện tương ứng với các sự kiện trong thời gian chạy [!INCLUDE[pn_Java](../includes/pn-java.md)]. Tất cả các sự kiện được liên kết với kiểm soát trên giao diện người dùng (UI). Để đăng ký sự kiện này, kiểm soát phải xuất hiện trong UI. Sử dụng hoạt động `FindControl` để xem kiểm soát có tồn tại không. Chủ đề này mô tả các sự kiện DDA [!INCLUDE[pn_Java](../includes/pn-java.md)].  
  
## <a name="javadda-events"></a>Sự kiện JavaDDA  
 Bảng sau liệt kê các sự kiện có sẵn trong DDA [!INCLUDE[pn_Java](../includes/pn-java.md)]:  
  
|Sự kiện||Mô tả|  
|-----------|-|-----------------|  
|`CheckBoxSelected`|Được gọi khi hộp kiểm được chọn (đã đặt đánh dấu).|  
|`CheckBoxCleared`|Được gọi khi hộp kiểm bị xóa (đánh dấu chưa được đặt).|  
|`RadioButtonSelected`|Được gọi khi nút radio được chọn.|  
|`RadioButtonCleared`|Được gọi khi nút radio bị xóa.|  
|`ButtonPressed`|Được gọi khi nút được nhấn (ngược với bấm, một thông cáo báo chí).|  
|`ButtonReleased`|Được gọi khi nút được nhả ra.|  
|`GotFocus`|Sự kiện này được đưa lên khi kiểm soát nhắm được trọng tâm.|  
|`LostFocus`|Sự kiện này được đưa lên khi kiểm soát mất trọng tâm.|  
|`MenuSelected`|Được gọi khi mục menu được chọn.|  
|`MenuDeSelected`|Được gọi khi mục menu được bỏ chọn.|  
|`MenuCanceled`|Được gọi khi lựa chọn menu bị hủy.|  
|`TreeNodeCollapsed`|Được gọi khi nút cây bị thu hẹp.|  
|`TreeNodeExpanded`|Được gọi khi nút cây được mở rộng.|  
  
> [!NOTE]
>  Khi nhiều trường hợp của cùng một bên ngoài [!INCLUDE[pn_Java](../includes/pn-java.md)] ứng dụng được lưu trữ bên ngoài của máy tính nhân viên, chẳng hạn như khi các [!INCLUDE[pn_Java](../includes/pn-java.md)] ứng dụng là một ứng dụng phiên, [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] không thể phân biệt giữa các trường hợp, trừ khi các liên kết đã được cấp quyền theo cách mà kiểm soát có thể được phân biệt giữa hai phiên bản. Với các ứng dụng `Win32` điển hình, điều này được thực hiện bằng cách hạn chế ID quá trình cụ thể nhưng là không thể với các ứng dụng [!INCLUDE[pn_Java](../includes/pn-java.md)] và cần để ý nhiều hơn trong việc cấp quyền liên kết.  
  
### <a name="see-also"></a>Xem thêm  
 [JavaDDA](../unified-service-desk/javadda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
