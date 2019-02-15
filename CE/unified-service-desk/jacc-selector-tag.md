---
title: JAccSelector Tag in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The topic describes the elements of <JAccSelector>.
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
ms.assetid: 95bd8843-e924-4709-b4aa-86dbdb985b03
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
ms.openlocfilehash: 65c9788baba17721b2b3bb93468d3fad82106ea6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386289"
---
# <a name="jaccselector-tag-in-unified-service-desk"></a>JAccSelector Tag in Unified Service Desk
`<JAccSelector>` liên kết kiểm soát có tên với đối tượng khả năng tiếp cận [!INCLUDE[pn_Java](../includes/pn-java.md)] được chỉ định trong đường dẫn tìm kiếm. Bạn có thể sử dụng loại kiểm soát này cho tất cả yếu tố lựa chọn chẳng hạn như hộp danh sách hoặc danh sách trong hộp kết hợp. Chủ đề này mô tả các yếu tố của `<JAccSelector>`  
  
## <a name="jaccselector-syntax"></a>\<JAccSelector> syntax  
  
```xml  
<JAccSelector name="control name">  
<Path>  
...      
</Path>  
</JAccSelector>  
  
```  
  
## <a name="elements-of-jaccselector"></a>Elements of \<JAccSelector>  
 Bảng sau mô tả các yếu tố của thẻ `<JAccSelector>`:  
  
|Yếu tố|Mô tả|  
|-------------|-----------------|  
|`FindControl`|Trả về `True` hoặc `False` tùy thuộc vào việc kiểm soát có thể được tìm thấy trên UI hay không.|  
|`GetControlValue`|Trả về tên của (các) mục đã chọn; nhiều mục được phân cách bằng dấu phẩy.|  
|`SetControlValue`|Đặt lựa chọn trong danh sách; nhiều mục được phân cách bằng dấu phẩy.|  
|`ExecuteControlAction`|Bật tắt lựa chọn hiện thời.|  
  
> [!NOTE]
>  Một số hộp tổ hợp được thiết lập để có thể chỉnh sửa, cho phép người dùng nhập văn bản bất kỳ vào trường đầu vào. For such combo boxes, you must use the `<JAccControl>` tag in the bindings for the input box to set the value.  
  
### <a name="see-also"></a>Xem thêm  
 [JavaDDA](../unified-service-desk/javadda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
