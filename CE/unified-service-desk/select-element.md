---
title: SelectElement in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about SelectElement in Unified Service Desk to search for a named control on the HTML page.
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
ms.assetid: 6a5148e9-871e-41d1-8f70-b11175b1c42c
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
ms.openlocfilehash: f23443cd311594e095fa3a5988e5501ad5bc2566
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385938"
---
# <a name="selectelement-in-unified-service-desk"></a>SelectElement in Unified Service Desk
Yếu tố `<SelectElement>` tìm kiếm một kiểm soát được đặt tên trên trang `HTML` và trả lại hoặc đảo ngược giá trị của nó. Chủ đề này mô tả các yếu tố của `<SelectElement>`  
  
## <a name="selectelement-syntax"></a>\<SelectElement> syntax  
 Đoạn mã sau hiển thị cách sử dụng `<SelectElement>`:  
  
```xml  
<SelectElement name="control name">  
Search Path Elements  
</SelectElement>  
  
```  
  
## <a name="elements-of-selectelement"></a>Elements of \<SelectElement>  
 Bảng sau mô tả các yếu tố của thẻ `<SelectElement>`.  
  
|Yếu tố|Mô tả|  
|-------------|-----------------|  
|`FindControl`|Trả về `True` hoặc `False` tùy thuộc vào việc kiểm soát có thể được tìm thấy trên giao diện người dùng (UI) hay không.|  
|`GetControlValue`|Trả về (các) mục đã chọn dưới dạng danh sách được phân tách bằng dấu phẩy.|  
|`SetControlValue`|Đảo ngược trạng thái lựa chọn của mục phù hợp đầu tiên trong danh sách. Điều này xóa toàn bộ lựa chọn khi văn bản thiết lập được cung cấp trống.|  
|`ExecuteControlAction`|Đối với chế độ một lựa chọn, điều này đảo ngược trạng thái lựa chọn của lựa chọn hiện tại. Đối với chế độ đa lựa chọn, điều này thêm mục chưa chọn tiếp theo vào lựa chọn hiện tại|  
  
### <a name="see-also"></a>Xem thêm  
 [WebDDA](../unified-service-desk/web-dda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
