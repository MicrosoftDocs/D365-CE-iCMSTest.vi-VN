---
title: Control Operations (Get, Set, Execute) | MicrosoftDocs
description: Thao tác trên một kiểm soát được thi hành dựa trên các mẫu trưng bày yếu tố tự động hóa. Chủ đề này mô tả các thao tác mà có thể được thực hiện trên các kiểm soát và hành vi mặc định của các thao tác này cho các kiểm soát khác nhau.
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
ms.assetid: f158113b-b492-44e2-8fec-65a10c5d0118
caps.latest.revision: 6
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 6cc4da7053ec9e6c689b15b66c7b2b28f27fd502
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387548"
---
# <a name="control-operations-get-set-execute"></a>Control Operations (Get, Set, Execute)
The operations on a control are executed based on the patterns the automation element exhibits. Chủ đề này mô tả các thao tác mà có thể được thực hiện trên các kiểm soát và hành vi mặc định của các thao tác này cho các kiểm soát khác nhau.  
  
 Các thao tác sau có thể thực hiện trên các kiểm soát được xác định:  
  
- Nhận Loại Kiểm soát  
  
- Nhận Loại Kiểm soát  
  
- Thi hành Loại Kiểm soát  
  
  Bảng sau trình bày hành vi mặc định của các thao tác sau cho các kiểm soát khác nhau:  
  
|Sl. Số|Loại kiểm soát|Tải |Set|Thực thi|  
|----------------|------------------|---------|---------|-------------|  
|1|Nút|Nhận tên|-|Gọi|  
|2|Calendar|Nhận ngày đã chọn (không phải ngày mặc định)|-|-|  
|3|Checkbox|Nhận trạng thái bật/tắt|-|Chuyển|  
|4|Combobox|Nhận tên mục đã chọn (trong nhiều lựa chọn trả về, trả về tên tách riêng)|-|Mở rộng hoặc thu hẹp|  
|5|Datagrid|Gets the selected item name (in multiple selection returns, it returns separated names)|-|-|  
|6|Datailtem|Nhận tên mục đã chọn.|Chọn mục|-|  
|7|document|Nhận văn bản|-|-|  
|8|Sửa|Gets the text|Đặt văn bản|Chọn văn bản|  
|9|Nhóm|Gets the text|-|Expands or collapses|  
|10|headercontrol|-|-|-|  
|11|headeritem|Gets the text|-|Gọi|  
|12|hyperlink|Gets the text|-|Gọi|  
|13|Hình ảnh|-|Selects the item|Gọi|  
|14|Danh sách|Gets the selected item name (in multiple selection returns, it returns separated names)|-|-|  
|15|Listitem|Nhận tên mục đã chọn|Selects the item|Gọi, mở rộng hoặc bật tắt|  
|16|Menu|-|-|-|  
|17|Menubar|-|-|Expands or collapses|  
|18|Menuitem|Gets the text|-|Invokes, expands or toggles|  
|19|Pane|-|-|-|  
|20|progressbar|Nhận phạm vi|Đặt phạm vi (nếu có thể)|-|  
|21|radiobutton|Selects the item|Selects the item|-|  
|22|scrollbar|Gets the range|Đặt phạm vi|-|  
|23|Separator|-|-|-|  
|24|slidercontrol|Gets the range|Sets the range|-|  
|25|spinner|Gets the range|Sets the range|-|  
|26|splitbutton|-|-|Invokes, expands or toggles|  
|27|statusbar|-|-|-|  
|28|Thẻ|-|-|-|  
|29|Tabitem|Nhận trạng thái lựa chọn|Chọn tab|-|  
|30|Table|-|-|-|  
|31|Text|Gets the text|-|-|  
|32|Thumb|-|-|-|  
|33|Titlebar|-|-|-|  
|34|Thanh công cụ|-|-|Expands or collapses|  
|35|Chú giải công cụ|Gets the text|-|-|  
|36|Tree|Gets the text|Selects the item|-|  
|37|Treeitem|Gets the text|Selects the item|Invokes, expands or toggles|  
|38|window|-|-|-|  
  
### <a name="see-also"></a>Xem thêm  
 [UIADDA](../unified-service-desk/uiadda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
