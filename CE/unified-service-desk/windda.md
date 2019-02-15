---
title: WinDDA in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn how to use Windows data-driven adapter (WinDDA) in Unified Service Desk.
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
ms.assetid: 2fe35fec-6805-4a3c-aeea-7c2192847a3a
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
ms.openlocfilehash: 8b5d339cfee15129f416aa54b751a33f5d364e75
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387738"
---
# <a name="windda"></a>WinDDA
Bộ chuyển đổi định hướng dữ liệu [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] (WinDDA) được sử dụng để tương tác với các ứng dụng dựa trên Windows. Công nghệ quan trọng được sử dụng trong DDA là Microsoft Active Accessibility (MSAA), với một số chức năng được bao gồm qua cuộc gọi chức năng Win32. MSAA API cho phép bạn tự động hóa giao diện người dùng. Một ứng dụng có thể sử dụng API này để làm cho giao diện dễ tiếp cận hơn cho người sử dụng với khả năng tiếp cận vấn đề. Mặc dù việc sửa đổi giao diện người dùng (UI) làm cho giao diện dễ tiếp cận với người dùng hơn là mục đích chính của API, UI cũng có thể được sử dụng để tích hợp [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)]. Windows tạo ra đối tượng proxy tiếp cận cho các kiểm soát Windows không cung cấp rõ ràng hỗ trợ MSAA của riêng họ. Việc sử dụng đối tượng proxy cung cấp phương án thay thế cho phương pháp tiếp cận phổ biến hơn của việc kiểm soát ứng dụng thông qua cuộc gọi Windows API. Nó cũng cho phép bạn kiểm soát bất kỳ loại ứng dụng (ngoài Win32) cho thấy nhiều giao diện người dùng thông qua MSAA.  
  
## <a name="windda-tags-and-events"></a>Thẻ và sự kiện WinDDA  
 WinDDA bao gồm các thẻ sau đây được sử dụng để xác định một điều khiển:  
  
- [Thẻ AccControl](../unified-service-desk/acccontrol-tag.md)  
  
- [Thẻ ACCSelector](../unified-service-desk/acc-selector-tag.md)  
  
- [Thẻ Tiếp theo](../unified-service-desk/next-tag-windda.md)  
  
- [Thẻ FindWindow](../unified-service-desk/find-window-tag.md)  
  
  Chủ đề sau đây cung cấp các thông tin về các sự kiện mà WinDDA hỗ trợ:  
  
- [Sự kiện WinDDA](../unified-service-desk/win-dda-events.md)  
  
### <a name="see-also"></a>Xem thêm  
 [Use Data Driven Adapters](../unified-service-desk/use-data-driven-adapters-ddas.md)   
 [WebDDA](../unified-service-desk/web-dda.md)   
 [UIADDA](../unified-service-desk/uiadda.md)   
 [JavaDDA](../unified-service-desk/javadda.md)
