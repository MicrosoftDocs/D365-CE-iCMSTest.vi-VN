---
title: FindWindow search path tag in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Thẻ <FindWindow> chứa một danh sách các yếu tố phù hợp bị loại trừ theo thứ tự danh sách của chúng bên trong thẻ. Chủ đề này mô tả các yếu tố <FindWindow> với mã ví dụ.
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
ms.assetid: 5aeb435d-5206-4cda-aa9e-db69aaa2f515
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
ms.openlocfilehash: 335821fbf96a7e989e4879d3cc260e9a0dc367fe
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386295"
---
# <a name="findwindow-search-path-tag-in-unified-service-desk"></a>FindWindow search path tag in Unified Service Desk
Thẻ `<FindWindow>` chứa một danh sách các yếu tố phù hợp bị loại trừ theo thứ tự danh sách của chúng bên trong thẻ. Chủ đề này mô tả các yếu tố `<FindWindow>` với mã ví dụ.  
  
<a name="elements"></a>   
## <a name="findwindow-elements"></a>\<FindWindow> elements  
 Đoạn mã sau đây hiển thị các yếu tố trong thẻ `<FindWindow>`  
  
```vb  
# RELAX NG XML grammar for FindWindow   
# http://relaxng.org/compact-tutorial-20030326.html   
#   
Grammar  
{   
start = FindWindow FindWindow = element   
FindWindow  
{   
  element ControlId { attribute match { xsd:integer }?, text }*  
& element Caption { attribute match { xsd:integer }?, text }*  
& element CaptionStartsWith { same as Caption }*  
& element CaptionEndsWith { same as Caption }*  
& element CaptionContains { same as Caption }*  
& element Class { attribute match { xsd:integer }?, text }*  
& element ClassStartsWith { same as Class }*  
& element ClassEndsWith { same as Class }*  
& element ClassContains { same as Class }*  
& element Position { xsd:integer, xsd:integer } *  
& element Find { Caption & Class }*  
& element Desktop { empty }*  
& element Application { empty }*  
& element Owner { empty }*  
& element RelaxProcessIdRestriction { empty }*  
& element RelaxThreadIdRestriction { empty }*  
}  
}  
  
```  
  
 Bảng sau mô tả các yếu tố `<FindWinow>`.  
  
|Yếu tố|Mô tả|  
|-------------|-----------------|  
|`ControlId`|Cửa sổ với ID|  
|`Caption`|Văn bản chú thích cửa sổ.|  
|`CaptionStartsWith`|Chú thích bắt đầu bằng văn bản|  
|`CaptionEndsWith`|Chú thích kết thúc bằng văn bản.|  
|`CaptionContains`|Chú thích có chứa văn bản.|  
|`Class`|Cửa sổ với tên lớp|  
|`ClassStartsWith`|Tên lớp bắt đầu bằng văn bản.|  
|`ClassEndsWith`|Tên lớp kết thúc bằng văn bản.|  
|`ClassContains`|Lớp có chứa văn bản.|  
|`Position`|Tìm kiếm một cửa sổ ở một vị trí đã chỉ định. Vị trí được định nghĩa là ở góc trên bên trái của cửa sổ như tọa độ (x, y). The position is calculated either from the \<Application/> (default) or from the \<Desktop/>. If \<Desktop/> is used, it must be specified before the \<Position> element.|  
|Find|Tìm kiếm cửa sổ được chỉ định qua yếu tố `Class` hoặc `Caption`. Các yếu tố tương tự như `FindWindow` có thể được sử dụng tại đây (`Caption`,  `CaptionStartsWith`,  `CaptionEndsWith`,  `CaptionContains`,  `Class`,  `ClassStartsWith`,  `ClassEndsWith` hoặc `ClassContains`).|  
|`Desktop`|Đặt điểm tìm cho máy tính để bàn|  
|`Application`|Đặt điểm tìm cho cửa sổ ứng dụng cấp cao nhất.|  
|`Owner`|Cửa sổ với chủ sở hữu được chỉ định.|  
|`RelaxProcessIdRestriction`|Bao gồm các cửa sổ với các ID quá trình khác nhau trong tìm kiếm. Theo mặc định, tất cả cửa sổ thuộc về cùng ID quá trình.|  
|`RelaxThreadIdRestriction`|Bao gồm các cửa sổ với các ID chuỗi chủ đề khác nhau trong quá trình tìm kiếm. Theo mặc định, tất cả cửa sổ thuộc về cùng ID chuỗi chủ đề.|  
  
<a name="samplecode"></a>   
## <a name="sample-code"></a>Mã mẫu  
 Tập hợp mẫu sau cho biết cách sử dụng các thuộc tính khác nhau.  
  
```xml  
The following sample searches for a window with the control ID 1003.  
<FindWindow>  
<ControlID>1003</ControlID>  
</FindWindow>  
  
The following sample searches for a window with the class name SunAWTFrame.  
<FindWindow>  
<Class>SunAWTFrame</Class>  
</FindWindow>  
  
The following sample searches for a window at desktop position x200 y400.   
<FindWindow>  
<Desktop/>  
<Position>200,400</Position>  
</FindWindow>  
  
The following sample searches for the second application with the caption CurrencyConv that is not within the same process as the DDA loaded application.   
  
<FindWindow>  
<RelaxProcessIdRestriction/>  
<Caption match="2">CurrencyConv</Caption>  
</FindWindow>  
  
```  
  
### <a name="see-also"></a>Xem thêm  
 [JavaDDA](../unified-service-desk/javadda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
