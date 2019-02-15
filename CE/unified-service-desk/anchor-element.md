---
title: AnchorElement | MicrosoftDocs
description: The topic explains about <AnchorElement> element which is one of the binding elements of the WebDDA.
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
ms.assetid: 2332b53a-92e6-419f-aace-af6dfda0dcb7
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
ms.openlocfilehash: 8a86b56f35c2113d688cace91316e66f707d3cc4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388519"
---
# <a name="anchorelement"></a>AnchorElement
Yếu tố `<AnchorElement>` là một trong các yếu tố liên kết của WebDDA.  
  
## <a name="anchorelement-syntax"></a>\<AnchorElement> syntax  
 `<AnchorElement>` associates a named control to an `<a/> HTML`  element. Đoạn mã sau hiển thị cách sử dụng `<AnchorElement>`.  
  
```xml  
<AnchorElement name="control name">  
Search Path Elements  
</AnchorElement>  
  
```  
  
## <a name="anchorelement-elements"></a>\<AnchorElement> elements  
 Bảng sau mô tả các yếu tố khác nhau của `<AnchorElement>`:  
  
|Yếu tố|Mô tả|  
|-------------|----------------|  
|`FindControl`|Trả về **True** hoặc **False** tùy theo có thể tìm thấy kiểm soát trên giao diện người dùng (UI) hay không.|  
|`GetControlValue`|Returns the URL text.|  
|`SetControlValue`|Throws an `UnsupportedControlOperation` exception.|  
|`ExecuteControlAction`|Navigates to the specified URL.|  
  
### <a name="see-also"></a>Xem thêm  
 [WebDDA](../unified-service-desk/web-dda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
