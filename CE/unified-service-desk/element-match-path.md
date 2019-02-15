---
title: ElementMatchPath in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: '<ElementMatchPath> tag uses a sequence of HTML tags delimited by forward slashes. Chủ đề này mô tả cách hoạt động của <ElementMatchPath>. '
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
ms.assetid: 2db66e85-cba1-4a37-bfbf-2190966295af
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
ms.openlocfilehash: d349876f4451ef57f0bda0a0e6ac3d215a4579cc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385470"
---
# <a name="elementmatchpath-in-unified-service-desk"></a>ElementMatchPath in Unified Service Desk
Thẻ `<ElementMatchPath>` sử dụng chuỗi các thẻ `HTML` được phân tách bởi gạch chéo. Chủ đề này mô tả cách hoạt động của `<ElementMatchPath>`.  
  
## <a name="elementmatchpath-syntax"></a>\<ElementMatchPath> syntax  
 Đoạn mã sau hiển thị cách sử dụng `<ElementMatchPath>`:  
  
```xml  
<html >  
<head>  
    <title>Sample</title>  
</head>  
<body>  
    <form id="HAT form">  
        <p>HAT</p>  
        <p><input id="CB1" type="checkbox" />Customer Care Framework</p>  
    </form>  
</body>  
</html>  
  
```  
  
 Đường dẫn kết nối cho `checkbox` như sau:  
  
```xml  
<ElementMatchPath>/html/body/form/p[1]/input</ElementMatchPath>  
  
```  
  
 Trình tự này theo dõi đường dẫn điều hướng từ gốc của `DOM` tới yếu tố mục tiêu, yếu tố cuối cùng trong danh sách. Mỗi thẻ kế tiếp biểu thị con của thẻ cha mẹ trước. Các thẻ `HTML` có thể có hạn định số, tùy chọn có dạng *[n]*, trong đó *n* là một số nguyên. Hạn định `[0]` là mặt định khi không có giá trị nào được chỉ định. The qualifier *[1]* represents the second matching sibling at that `DOM` level, and so on. Hạn định đặc biệt `[-1]` biểu thị cho cặp phù hợp cuối cùng tại cấp độ `DOM` bất kể độ dài của danh sách. Trong ví dụ trên, thẻ `<p>` thứ hai trong thẻ `<form>` được sử dụng làm gốc cho nút con tiếp theo trong cây `DOM`.  
  
### <a name="see-also"></a>Xem thêm  
 [WebDDA](../unified-service-desk/web-dda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
