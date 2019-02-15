---
title: Search Path Elements in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about Search Path Elements in Unified Service Desk.
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
ms.assetid: 6b9e70b9-20a1-430c-9cf0-bb8ca7b2480d
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
ms.openlocfilehash: 6236241d78c26e8a82a21f14ab01c34888d29ff2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387819"
---
# <a name="search-path-elements-in-unified-service-desk"></a>Search Path Elements in Unified Service Desk
Ứng dụng web và các trang web có thể chứa khung. Các khung có thể có các kiểm soát được liên kết. Bạn cũng có thể đặt cấu hình kiểm soát bộ chuyển đổi định hướng dữ liệu (DDA) cho các kiểm soát dựa trên khung. Ví dụ: bạn có thể cần truy cập các kiểm soát biểu mẫu `HTML` bên trong khung. Để làm điều này, bạn sẽ tìm kiếm một khung cụ thể bên trong cửa sổ cho dữ liệu cụ thể. Bạn có thể bao gồm tìm kiếm đó trong chính WebDDA.  
  
## <a name="search-path-elements"></a>Tìm kiếm yếu tố đường dẫn  
 WebDDA xác định ba yếu tố có thể được sử dụng trong đường dẫn tìm kiếm cho một kiểm soát nhất định:  
  
- [AttributeMatchPath](../unified-service-desk/attribute-match-path.md)  
  
- [ElementMatchPath](../unified-service-desk/element-match-path.md)  
  
- [FindIEFrame](../unified-service-desk/find-ie-frame.md)  
  
  Một đường dẫn tìm kiếm của kiểm soát có thể chứa nhiều yếu tố. Chúng sẽ được thực thi theo thứ tự được liệt kê trong đường dẫn tìm kiếm. Ví dụ: mô tả kiểm soát sau trước tiên tìm một cửa sổ [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] được mô tả với yếu tố `<FindIEFrame/>` và sau đó sử dụng yếu tố `<ElementMatchPath/>` để xác định kiểm soát mong muốn trong cửa sổ [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] này.  
  
```xml  
<HtmlElement name="Popup Text1" type="HtmlElement">  
<FindIEFrame matchtype="endswith">Popup - Windows Internet Explorer</FindIEFrame>  
<ElementMatchPath>/HTML/BODY/P/FONT</ElementMatchPath>  
</HtmlElement>  
  
```  
  
### <a name="see-also"></a>Xem thêm  
 [WebDDA](../unified-service-desk/web-dda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
