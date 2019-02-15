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
# <a name="windda-events"></a>Sự kiện WinDDA
Bộ chuyển đổi định hướng dữ liệu [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] (DDA) phân biệt giữa hai loại sự kiện, sự kiện ứng dụng và sự kiện kiểm soát. Chủ đề này mô tả hai sự kiện này.  
  
<a name="control"></a>   
## <a name="control-events"></a>Sự kiện kiểm soát  
 Các sự kiện kiểm soát được bắt đầu bởi các kiểm soát trong ứng dụng. Đối với tất cả các sự kiện này, tên kiểm soát phải được chỉ định trong quá trình đăng ký (`RegisterActionForEvent`). Các điều khiển cũng phải có thể được truy cập trong ứng dụng trong khi đăng ký. You can use the [FindControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.operationtype.findcontrol) method or add an exception handler to ensure that the control is accessible.  
  
 Nhà máy Phần mềm [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)] liệt kê các sự kiện được hỗ trợ cho một loại kiểm soát Giao diện Người dùng (UI) cụ thể. Nếu bạn không chỉ định loại trong Trình kiểm tra [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)], [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] liệt kê tất cả sự kiện cho kiểm soát. Tất cả sự kiện kiểm soát có sẵn được liệt kê bởi Nhà máy Phần mềm [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)] nếu không có loại kiểm soát nào được phát hiện. Bảng sau mô tả các sự kiện kiểm soát được hỗ trợ.  
  
|Yếu tố|Mô tả|  
|-------------|-----------------|  
|GotFocus|Sự kiện này được đưa lên khi kiểm soát nhắm được trọng tâm.|  
|LostFocus|Sự kiện này được đưa lên khi kiểm soát mất trọng tâm.|  
|ButtonPressed|Sự kiện này được nêu khi nút được bấm.|  
|ButtonReleased|Sự kiện này được nêu khi nút được nhả.|  
|CheckBoxSet|Sự kiện được nêu khi hộp kiểm được chọn.|  
|CheckBoxCleared|Sự kiện được nêu khi hộp kiểm bị xóa.|  
|RadioButtonSet|Sự kiện được nêu khi nút radio được chọn.|  
  
 Bảng sau liệt kê các sự kiện mà mỗi kiểm soát hỗ trợ.  
  
|Yếu tố|Mô tả|  
|-------------|-----------------|  
|Nút nhấn|ButtonPressed, ButtonReleased, GotFocus, LostFocus|  
|Hộp kiểm|GotFocus, CheckBoxSet, CheckBoxCleared, LostFocus|  
|Nút Radio|GotFocus, RadioButtonSet, LostFocus|  
|Văn bản|GotFocus, LostFocus|  
|Văn bản Có thể chỉnh sửa|GotFocus, LostFocus|  
  
<a name="application"></a>   
## <a name="application-events"></a>Sự kiện Ứng dụng.  
 Sự kiện ứng dụng không bị ràng buộc cho một kiểm soát; Vì vậy, bạn không cần phải chỉ định một tên kiểm soát trong hoạt động `RegisterActionForEvent`. Bảng sau mô tả các sự kiện ứng dụng có sẵn trong [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)]:  
  
|Yếu tố|Mô tả|  
|-------------|-----------------|  
|WindowShown|Sự kiện được nêu khi cửa sổ được hiển thị.|  
|WindowDisappeared|Sự kiện được nêu khi cửa sổ bị ẩn.|  
  
### <a name="see-also"></a>Xem thêm  
 [Win DDA](../unified-service-desk/windda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
