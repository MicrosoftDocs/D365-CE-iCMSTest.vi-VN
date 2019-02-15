---
title: FindIEFrame in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The topic describes the attributes of <FindIEFrame> that searches for an application by its caption and selects a DOM of the window or a specific frame within a window.
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
ms.assetid: fc973cc7-d4af-4bdb-813a-4204ac46f939
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
ms.openlocfilehash: b5ac613ecf30dd0ecca8614f6683f6b887ca582b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387957"
---
# <a name="findieframe-in-unified-service-desk"></a>FindIEFrame in Unified Service Desk
Thẻ `<FindIEFrame>` tìm kiếm ứng dụng bằng chú thích của ứng dụng và chọn `DOM` của cửa sổ hoặc khung cụ thể bên trong cửa sổ. Một ví dụ là một cửa sổ bật lên. Thẻ này có thể khám phá cửa sổ bật lên bất kể nó có liên quan gì đến ứng dụng web được lưu trữ không. Chủ đề này mô tả các thuộc tính của `<FindIEFrame>`  
  
## <a name="findieframe-syntax"></a>\<FindIEFrame> syntax  
 Đoạn mã sau hiển thị cách sử dụng `<FindIEFrame>`:  
  
```xml  
<FindIEFrame> [matchtype="equals|startswith|endswith|contains"] [match="n"][relaxProcessIdRestriction="true|false"] >  
text to match against window caption  
</FindIEFrame>  
  
```  
  
## <a name="attributes-of-findieframe"></a>Attributes of \<FindIEFrame>  
 Bảng sau mô tả các thuộc tính tùy chọn của thẻ `<FindIEFrame>`.  
  
|Yếu tố|Mô tả|  
|-------------|-----------------|  
|`matchtype`|Chỉ định cách kết hợp chú thích. Các giá trị có thể là `equals`, `startswith`, `endswith` hoặc `contains`. Bất kỳ giá trị nào khác sẽ đặt một ngoại lệ.|  
|`match`|Chọn khung **thứ n** phù hợp với đặc điểm kỹ thuật. Mặc định: **1**.|  
|`relaxProcessIdRestriction`|Tìm kiếm cửa sổ/khung phù hợp trong quá trình ứng dụng được lưu trữ (`False`) hoặc tìm kiếm qua tất cả quá trình (`True`).|  
  
 Mẫu mã sau đây hiển thị các liên kết cho kiểm soát có tên `PopupWindowText`. Kiểm soát trong văn bản là một cửa sổ bật lên `HTML`; trong trường hợp này, đó là cửa sổ bật lên trong **Ứng dụng Web Mẫu**.  
  
```xml  
<HtmlElement name="PopupWindowText" type="HtmlElement">  
<FindIEFrame>http://uiiserver1/Microsoft.Cti.Samples.DemoWebApplication/popup1.htm - Windows Internet Explorer</FindIEFrame>  
<ElementMatchPath>/HTML/BODY/P/FONT</ElementMatchPath>  
</HtmlElement>  
  
```  
  
### <a name="see-also"></a>Xem thêm  
 [WebDDA](../unified-service-desk/web-dda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
