---
title: FindWindow Tag in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Thẻ <FindWindow> bao gồm danh sách các yếu tố phụ thể hiện một chuỗi toán thử phù hợp, tất cả chúng cần thành công cho cửa sổ mục tiêu để được xem xét tìm thấy.
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
ms.assetid: 1e3efa2f-e888-4a92-a32a-1990735fd936
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
ms.openlocfilehash: 02db1269d611580cbd6d2fd5de9036a83f6ce8fd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387182"
---
# <a name="findwindow-tag-in-unified-service-desk"></a>FindWindow Tag in Unified Service Desk
Thẻ `<FindWindow>` bao gồm danh sách các yếu tố phụ thể hiện một chuỗi toán thử phù hợp, tất cả chúng cần thành công cho cửa sổ mục tiêu để được xem xét tìm thấy.  
  
 Đoạn mã sau đây cho thấy cách sử dụng các yếu tố `<FindWindow>` khác nhau để tìm cửa sổ mục tiêu:  
  
```xml  
# RELAX NG XML grammar for FindWindow  
# http://relaxng.org/compact-tutorial-20030326.html  
#  
grammar {  
   start      = FindWindow  
   FindWindow = element FindWindow {  
element ControlId { attribute match { xsd:integer }?, text }*  
& element Caption { attribute match { xsd:integer }?, text }*  
& element CaptionStartsWith { same as Caption }*  
& element CaptionEndsWith { same as Caption }*  
& element CaptionContains { same as Caption }*  
& element Class { attribute match { xsd:integer }?, text }*  
& element ClassStartsWith { same as Class }*  
& element ClassEndsWith { same as Class }*  
& element ClassContains { same as Class }*  
& element Find { Caption & Class }*  
& element Desktop { empty }*  
& element Application { empty }*  
& element Owner { empty }*  
& element RelaxProcessIdRestriction { empty }*  
& element RelaxThreadIdRestriction  { empty }*  
}  
}  
  
```  
  
### <a name="findwindow-tag-elements"></a>\<FindWindow> tag elements  
 Bảng sau mô tả các yếu tố khác nhau của thẻ `<FindWindow>`:  
  
|Yếu tố|Mô tả|  
|-------------|-----------------|  
|ControlId|Cửa sổ với ID.|  
|Caption|Văn bản chú thích cửa sổ.|  
|CaptionStartsWith|Chú thích bắt đầu bằng văn bản.|  
|CaptionEndsWith|Chú thích kết thúc bằng văn bản.|  
|CaptionContains|Chú thích có chứa văn bản.|  
|Lớp|Cửa sổ với tên lớp.|  
|ClassStartsWith|Tên lớp bắt đầu bằng văn bản.|  
|ClassEndsWith|Tên lớp kết thúc bằng văn bản.|  
|ClassContains|Lớp có chứa văn bản.|  
|Find|Tìm kiếm cho cửa sổ như được chỉ định qua yếu tố `Class` hoặc `Caption`.|  
|Desktop|Đặt điểm tìm cho máy tính để bàn.|  
|Application|Đặt điểm tìm cho cửa sổ ứng dụng cấp cao nhất.|  
|Chủ sở hữu|Cửa sổ với chủ sở hữu được chỉ định.|  
|RelaxProcessIdRestriction|Bao gồm các cửa sổ với các ID quá trình khác nhau trong tìm kiếm. Theo mặc định, tất cả cửa sổ thuộc về cùng ID quá trình.|  
|RelaxThreadIdRestriction|Bao gồm các cửa sổ với ID chuỗi chủ đề khác nhau trong quá trình tìm kiếm. Theo mặc định, tất cả cửa sổ thuộc về cùng ID chuỗi chủ đề.|  
  
 The following XML shows control definition using the **\<FindWindow>** tag.  
  
```xml  
<FindWindow>  
<Desktop/>  
<Caption match="1">Font</Caption>  
<Class>#32770</Class>  
<Caption>OK</Caption>  
</FindWindow>  
<FindWindow>  
<Application/>  
<ControlId>7d</ControlId>  
</FindWindow>  
<FindWindow>  
<Desktop/>  
<Class>Notepad</Class>  
</FindWindow>  
  
```  
  
 Trong ví dụ `XML` trước, các yếu tố có các định nghĩa sau:  
  
- `<Application/>` – Đặt cửa sổ ngữ cảnh thành cửa sổ ứng dụng cấp cao nhất. By default, the context is initialized to the top-level window before the first child node in \<FindWindow/>.  
  
- `<Desktop/>` – Đặt cửa sổ bối cảnh ở cửa sổ máy tính để bàn cấp gốc.  
  
- \<Caption match="1">Font\</Caption> – Searches the window hierarchy, starting at the current context window and working down the hierarchy, for the first window with caption text that matches the text provided. Nếu `match="2"`, nó tìm kiếm cửa sổ thứ hai với văn bản chú thích phù hợp với văn bản đã cung cấp. Nếu không có thuộc tính `match` được cung cấp,  `match="1"` là mặc định. So sánh văn bản là kết quả phù hợp chuỗi con so với văn bản chú thích. Nếu văn bản được cung cấp có thể được tìm thấy là chuỗi con trong chú thích của cửa sổ chủ đề, đó được coi là một kết quả phù hợp. Cửa sổ ghép đôi phù hợp sẽ trở thành cửa sổ ngữ cảnh mới. Nếu không tìm thấy kết quả phù hợp, tìm kiếm thất bại. Theo mặc định, chỉ có cửa sổ thuộc cùng `ProcessId` và `ThreadId` mới được coi là kết quả phù hợp.  
  
- `<Class>#32770</Class>` – Tìm kiếm hệ thống cấp bậc cửa sổ, cho cửa sổ đầu tiên với văn bản lớp phù hợp với văn bản đã chọn. Tất cả các chi tiết hành vi khác giống nhau để `<Caption/>.`  
  
- `<ControlId>7d</ControlId>` – Tìm kiếm hệ thống cấp bậc cửa sổ, cho cửa sổ đầu tiên với ID kiểm soát phù hợp với giá trị đã cung cấp. Đây phải là kết quả phù hợp chính xác. Tất cả các chi tiết hành vi khác giống nhau để `<Caption/>`.  
  
  The following XML searches for the window with the caption **OK** in the first window with the caption **Font** and the class ID 32770, starting at the desktop.  
  
```xml  
<FindWindow>  
<Desktop/>  
<Caption match="1">Font</Caption>  
<Class>#32770</Class>  
<Caption>OK</Caption>  
</FindWindow>  
  
```  
  
 `XML` sau tìm kiếm cửa sổ với ID Kiểm soát 7D, bắt đầu ở cửa sổ cấp cao nhất của ứng dụng.  
  
```xml  
<FindWindow>  
<Application/>  
<ControlId>7d</ControlId>  
</FindWindow>  
  
```  
  
 `XML` sau tìm kiếm cửa sổ (đầu tiên) với tên lớp **Notepad**, bắt đầu tại màn hình.  
  
```xml  
<FindWindow>  
<Desktop/>  
<Class>Notepad</Class>  
</FindWindow>  
  
```  
  
### <a name="see-also"></a>Xem thêm  
 [Win DDA](../unified-service-desk/windda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
