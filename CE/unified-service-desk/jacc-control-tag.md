---
title: JAccControl Tag in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: <JAccControl> liên kết kiểm soát tổ chức có tên với yếu tố khả năng kiểm soát Java được chỉ định trong đường dẫn tìm kiếm. Chủ đề này mô tả các yếu tố của thẻ <AccControl>.
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
ms.assetid: e6b76e86-3b62-4e34-9d3e-03abf30bad4f
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
ms.openlocfilehash: 41d58e919853b33c65ad829b5fe3a0a0aad22702
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385756"
---
# <a name="jacccontrol-tag-in-unified-service-desk"></a>JAccControl Tag in Unified Service Desk
`<JAccControl>` liên kết kiểm soát tổ chức có tên với yếu tố khả năng kiểm soát Java được chỉ định trong đường dẫn tìm kiếm. Chủ đề này mô tả các yếu tố của thẻ `<AccControl>`.  
  
## <a name="jacccontrol-syntax"></a>\<JAccControl> syntax  
 Đoạn mã sau hiển thị cách sử dụng thẻ `<JAccControl>`:  
  
```xml  
<JAccControl name="control name">  
<Path>  
...      
</Path>  
</JAccControl>  
  
```  
  
## <a name="elements-of-jacccontrol"></a>Elements of \<JAccControl>  
 Bảng sau mô tả các yếu tố của thẻ `<JAccControl>`.  
  
|Yếu tố|Mô tả|  
|-------------|-----------------|  
|`FindControl`|Trả về `True` nếu kiểm soát được tìm thấy trên UI, nếu không sẽ trả lại **False**.|  
|`GetControlValue`|Trả về nội dung của kiểm soát.|  
|`SetControlValue`|Đặt nội dung của kiểm soát, một số kiểm soát không thể thay đổi nội dung của chúng.|  
|`ExecuteControlAction`|Thực hiện lệnh mặc định cho kiểm soát này, tùy thuộc vào việc tích hợp khả năng tiếp cận Java.|  
  
> [!NOTE]
>  Sử dụng loại kiểm soát này cho tất cả các yếu tố không phải là cây hoặc yếu tố lựa chọn, chẳng hạn danh sách.  
  
### <a name="see-also"></a>Xem thêm  
 [JavaDDA](../unified-service-desk/javadda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
