---
title: InputElement in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The topic describes the elements of <IntputElement>.
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
ms.assetid: 80a0bb8c-e9c1-45d4-9600-fc929654f681
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
ms.openlocfilehash: beb9d1a8ffb531e857d76bf48b3d0b8f87ebcc8d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387724"
---
# <a name="inputelement-in-unified-service-desk"></a>InputElement in Unified Service Desk
Yếu tố `<InputElement>` liên kết kiểm soát có tên với yếu tố `<input/> HTML` nếu yếu tố này có một trong các giá trị `type=attribute` sau: `check box`, `radio`, `text`, `password`, `submit`, `reset`, `hidden`, `image` hoặc `file`. Chủ đề này mô tả các yếu tố của `<IntputElement>`.  
  
## <a name="inputelement-syntax"></a>\<InputElement> syntax  
 Đoạn mã sau hiển thị cách sử dụng `<InputElement>`:  
  
```xml  
<InputElement name="control name" type="type">  
Search Path Elements  
</InputElement>  
  
```  
  
## <a name="elements-of-inputelement"></a>Elements of \<InputElement>  
 Bảng sau mô tả các yếu tố của thẻ `<InputElement>`.  
  
|Yếu tố|Mô tả|  
|-------------|-----------------|  
|`FindControl`|Trả về `True` nếu kiểm soát có thể được tìm thấy trên giao diện người dùng (UI), nếu không `False`|  
|`GetControlValue`|Trả về `True` hoặc `False` (giá trị chuỗi) khi `type="checkbox"` hoặc `type="radio"`. Trả về giá trị của yếu tố cho tất cả các loại khác.|  
|`SetControlValue`|Đặt thành `True` hoặc `False` khi `type="checkbox"` hoặc `type="radio"`. Thiết lập giá trị của yếu tố khi `type="text"` hoặc `type="password"` hoặc `type="hidden"`. Áp dụng một ngoại lệ `UnsupportedControlOperation` cho tất cả các loại khác.|  
|`ExecuteControlAction`|Đảo ngược `True` hoặc trạng thái `False` hiện có khi `type="checkbox"`. Đặt trạng thái thành `True` khi `type="radio"`. Trả về `UnsupportedControlOperation` khi `type="text"` hoặc `type="password"` hoặc `type="hidden"`. Gây ra vấn đề `Click()` cho tất cả các loại khác.|  
  
### <a name="see-also"></a>Xem thêm  
 [WebDDA](../unified-service-desk/web-dda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
