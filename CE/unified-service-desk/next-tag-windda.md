---
title: Next Tag (WinDDA) in Unified Service Desk for Dynamics 365 for Customer Engagement apps Customer Enagagement| MicrosoftDocs
description: The topic describes the attributes of the Next tag (winDDA).
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
ms.assetid: 4369bd08-3009-47cd-be60-20bed9df50fc
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
ms.openlocfilehash: e282769e56fe42f6b4a23ecd71d86d9e00d722dc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387103"
---
# <a name="next-tag-windda-in-unified-service-desk"></a>Next Tag (WinDDA) in Unified Service Desk
Thẻ `<Next/>` có thể bao gồm thuộc tính `match` tùy chọn và thuộc tính `offset` tùy chọn. Thuộc tính `match` có giá trị mặc định là `"1"` và thuộc tính bù có giá trị mặc định là `"0"`. Mỗi yếu tố `<Next/>` truy xuất mức độ tiếp theo của hệ thống cấp bậc [IAccessible](https://msdn.microsoft.com/library/accessibility.iaccessible\(v=vs.110\).aspx) và quét để có kết quả phù hợp giữa văn bản bên trong và `Name` của mỗi nút `IAccessible`. Chủ đề này mô tả các thuộc tính của thẻ `Next`.  
  
## <a name="attributes-of-next"></a>Attributes of \<Next>  
  
- `Match` – Trả về thuộc tính phù hợp thứ nth.  
  
- `Offset` – Trả lại thuộc tính nth sau thuộc tính phù hợp.  
  
- `Culture` – Sử dụng thẻ `culture`.  
  
  The `match="2"` attribute specifies how many times a text match has to occur for the criteria to be satisfied. Khi đạt đến con số này, các thuộc tính `offset` có thể được sử dụng để chọn một nút liền kề `IAccessible` với các nút được kết hợp thành công. Giá trị bù đắp được bao quanh, do đó không thể tham chiếu bên ngoài dãy `IAccessible` con. Thẻ văn hóa cho phép bạn tìm kiếm các thuộc tính dành riêng cho ngôn ngữ để hiển thị trong ví dụ sau:  
  
```xml  
<AccControl name="closeButton">  
<Path>  
<Next culture="en-us">Close</Next>  
<Next culture="de-de">Beenden</Next>  
<Next culture="fr-fr">Fermer</Next>  
</Path>  
</AccControl>  
  
```  
  
 Mẫu sau tìm kiếm kiểm soát ở hai vị trí sau kiểm soát thứ tư với chú thích `Name`.  
  
```xml  
<AccControl name="NameBox">  
<Path>  
<Next match="4", offset="4">Name</Next>  
</Path>  
</AccControl>  
  
```  
  
### <a name="see-also"></a>Xem thêm  
 [Win DDA](../unified-service-desk/windda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
