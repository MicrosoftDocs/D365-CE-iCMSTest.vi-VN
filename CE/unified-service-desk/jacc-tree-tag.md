---
title: JAccTree Tag in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The topic describes the elements of <JAccTree>.
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
ms.assetid: f1a3a64c-b154-4ccb-82f0-5399745d9a6e
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
ms.openlocfilehash: 91d7c69bf38c22a83f509d7e06cb75d793da96c6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387404"
---
# <a name="jacctree-tag-in-unified-service-desk"></a>JAccTree Tag in Unified Service Desk
`JAccTree` liên kết kiểm soát tổ chức có tên với yếu tố cây khả năng tiếp cận Java được chỉ định trong đường dẫn tìm kiếm. Chủ đề này mô tả các yếu tố của `<JAccTree>`  
  
## <a name="jacctree-syntax"></a>\<JAccTree> syntax  
 Đoạn mã sau hiển thị cú pháp của `<JAccTree>`  
  
```xml  
<JAccTree name="control name">  
<Path>  
       ...      
</Path>  
</JAccTree>  
  
```  
  
## <a name="elements-of-jacctree"></a>Elements of \<JAccTree>  
 Bảng sau mô tả các yếu tố của thẻ `<JAccTree>`.  
  
|Yếu tố|Mô tả|  
|-------------|-----------------|  
|`FindControl`|Trả về `True` hoặc `False` tùy thuộc vào việc kiểm soát có thể được tìm thấy trên UI hay không.|  
|`GetControlValue`|Trả về nội dung của kiểm soát.|  
|`SetControlValue`|Đặt nội dung của kiểm soát.|  
|`ExecuteControlAction`|Bật tắt trạng thái nút cây – mở rộng hoặc thu hẹp.|  
  
### <a name="see-also"></a>Xem thêm  
 [JavaDDA](../unified-service-desk/javadda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
