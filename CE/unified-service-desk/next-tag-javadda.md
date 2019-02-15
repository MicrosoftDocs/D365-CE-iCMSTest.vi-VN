---
title: Next Tag in Unified Service Desk for Dynamics 365 for Customer Engagement apps Customer Enagagement| MicrosoftDocs
description: The topic describes the attributes of <Next> tag. Bạn có thể sử dụng yếu tố <Next> để đặt con trỏ tìm kiếm vào yếu tố UI tiếp theo với chú thích phù hợp. Nếu bạn sử dụng <Next/>, tìm kiếm sẽ điều hướng đến nút tiếp theo bên trong cây.
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
ms.assetid: a8eefb0b-4ad3-4d98-aed2-0373187fd2e0
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
ms.openlocfilehash: 041b434b317068633d52ac9ed09ec9d6f5c4151d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386113"
---
# <a name="next-tag-in-unified-service-desk"></a>Next Tag in Unified Service Desk
Bạn có thể sử dụng yếu tố `<Next>` để đặt con trỏ tìm kiếm vào yếu tố UI tiếp theo với chú thích phù hợp. Nếu bạn sử dụng `<Next/>`, tìm kiếm sẽ điều hướng đến nút tiếp theo bên trong cây. The `<Next/>` tag navigates down the tree branches, not among siblings within one node of the tree. Để điều hướng bên trong nút cây, hãy sử dụng thuộc tính `match` và `offset`. Chủ đề này mô tả các thuộc tính của thẻ `<Next>`.  
  
## <a name="attributes-of-next-tag"></a>Attributes of \<Next> tag  
 Bảng sau mô tả các thuộc tính của thẻ `<Next>`.  
  
|Thuộc tính|Mô tả|  
|---------------|-----------------|  
|`Match`|Yếu tố **thứ n**|  
|`Offset`|Yếu tố thứ **N** sau một yếu tố phù hợp.|  
|`Culture`|Sử dụng văn hóa|  
  
 Liên kết mẫu sau tìm nút `Close` trong một ứng dụng cho ba nền văn hóa khác nhau: Anh, Đức và Pháp:  
  
```xml  
<Controls>  
<JAccControl name="CloseButton">  
<Path>  
<FindWindow>  
<Class>SunAWTFrame</Class>  
</FindWindow>  
<Next culture="en-us">Close</Next>  
<Next culture="de-de">Beenden</Next>  
<Next culture="fr-fr">Fermer</Next>  
</Path>  
</JAccControl>  
</Controls>  
  
```  
  
 Bằng cách sử dụng các thuộc tính `match` và `offset`, bạn có thể điều hướng cây khả năng tiếp cận cho các nút có cùng tên (sử dụng `match`) hoặc không có thông tin nhận dạng (bằng `offset`). Mẫu sau chọn mục nhập cây khả năng tiếp cận thứ hai sau mục nhập thứ tư với chú thích `Name`.  
  
```xml  
<JAccControl name="TestButton">  
<Path>  
<Next match="4", offset="2" >Name</Next>  
</Path>  
</JAccControl>  
  
```  
  
> [!NOTE]
>  Các thẻ `<Next/>` và `<NextName/>` có cùng chức năng. Khi chỉ định liên kết của bạn, hãy sử dụng thẻ `<Next>` để chuyển tiếp tương thích.  
  
### <a name="see-also"></a>Xem thêm  
 [JavaDDA](../unified-service-desk/javadda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
