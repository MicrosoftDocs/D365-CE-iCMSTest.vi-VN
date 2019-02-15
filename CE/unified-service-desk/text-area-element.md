---
title: TextAreaElement in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about using TextAreaElement in Unified Service Desk used to associate a named control with a text area element on the HTML page.
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
ms.assetid: eccf015f-836a-4f4d-8fe7-01ff2405d6c5
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
ms.openlocfilehash: 165c8db78df28c85a9ff6771fa44f5b130543540
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388081"
---
# <a name="textareaelement-in-unified-service-desk"></a>TextAreaElement in Unified Service Desk
Yếu tố `<TextAreaElement>` liên kết một kiểm soát có tên với yếu tố khu vực văn bản trên trang `HTML`. Chủ đề này mô tả các yếu tố của `<TextAreaElement>`.  
  
## <a name="textareaelement-syntax"></a>\<TextAreaElement> syntax  
 Đoạn mã sau hiển thị cách sử dụng `<TextAreaElement>`.  
  
```xml  
<TextAreaElement name="name goes here">  
Search Path Elements  
</TextAreaElement>  
  
```  
  
## <a name="elements-of-textareaelement"></a>Elements of \<TextAreaElement>  
 Bảng sau mô tả các yếu tố của thẻ `<TextAreaElement>`:  
  
|Yếu tố|Mô tả|  
|-------------|-----------------|  
|`FindControl`|Trả về `True` nếu kiểm soát có thể được tìm thấy trên giao diện người dùng (UI), nếu không `False`.|  
|`GetControlValue`|Trả về giá trị của yếu tố khu vực văn bản.|  
|`SetControlValue`|Đặt giá trị của yếu tố khu vực văn bản.|  
|`ExecuteControlAction`|Throws an `UnsupportedControlOperation` exception.|  
  
### <a name="see-also"></a>Xem thêm  
 [WebDDA](../unified-service-desk/web-dda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
