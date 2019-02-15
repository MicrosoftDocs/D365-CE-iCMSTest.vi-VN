---
title: Search Path Node Tag in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about Search Path node that describes the search path to identify the control in the Java accessibility tree.
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
ms.assetid: 31b95b66-c66b-4b84-b74c-941d18dac910
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
ms.openlocfilehash: f36eccca3eede16ec58910cdbfe7c27ec6cf8a10
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387406"
---
# <a name="search-path-node-tag-in-unified-service-desk"></a>Search Path Node Tag in Unified Service Desk
Nút Đường dẫn Tìm kiếm mô tả đường dẫn tìm kiếm để xác định kiểm soát trong cây khả năng tiếp cận Java. Có bốn yếu tố đường dẫn tìm kiếm có thể được sử dụng để xác định kiểm soát UI mong muốn.  
  
 Các yếu tố được thực hiện theo thứ tự mà chúng được liệt kê trong nút **Đường dẫn**. **Next** and **NextRole** are elements to navigate the Java accessibility tree. `FindWindow` is used to identify the window hosting the Java application. Vì vậy, `FindWindow` nên là yếu tố đầu tiên trong danh sách tìm kiếm.Ví dụ sau cho thấy các liên kết cho kiểm soát Java `TestButton`. Kiểm soát này ở trong cửa sổ có tên lớp `SunAWTFrame` và chú thích `Input`. Đây là yếu tố UI đầu tiên trong cây khả năng tiếp cận của ứng dụng để phù hợp với vai trò nút nhấn.  
  
```xml  
<Controls>  
<JAccControl name="TestButton">  
<Path>  
<FindWindow>  
<Class>SunAWTFrame</Class>  
<Caption>Input</Caption>  
</FindWindow>  
<NextRole match="1">push button</NextRole>  
</Path>  
</JAccControl>  
</Controls>  
  
```  
  
### <a name="see-also"></a>Xem thêm  
 [JavaDDA](../unified-service-desk/javadda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
