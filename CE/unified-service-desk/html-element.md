---
title: HtmlElement in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The <HTMLElement> element associates a named control to the HTML object specified by the search path. Chủ đề này mô tả các yếu tố của <HTMLElement>.
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
ms.assetid: 72a912d3-c16d-4e38-9367-bc2722ac0fa6
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
ms.openlocfilehash: 8e80aa1c6cad4c93dd1a5db12710a7472ea7e3cb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387780"
---
# <a name="htmlelement-in-unified-service-desk"></a>HtmlElement in Unified Service Desk
The `<HTMLElement>` element associates a named control to the `HTML` object specified by the search path. Chủ đề này mô tả các yếu tố của `<HTMLElement>`.  
  
## <a name="htmlelement-syntax"></a>\<HTMLElement> syntax  
 The following code snippet shows how \<HTMLElement> is used:  
  
```xml  
<HTMLElement name="control name">  
Search Path Elements  
</HTMLElement>  
```  
  
## <a name="elements-of-htmlelement"></a>Elements of \<HTMLElement>  
 Bảng sau mô tả các yếu tố của thẻ `<HTMLElement>`.  
  
|Yếu tố|Mô tả|  
|-------------|-----------------|  
|`FindControl`|Trả về `True` nếu kiểm soát có thể được tìm thấy trên giao diện người dùng (UI), nếu không `False`.|  
|`GetControlValue`|Trả về nội dung của đối tượng `HTML`.|  
|`SetControlValue`|Throws an `UnsupportedControlOperation` exception.|  
|`ExecuteControlAction`|Executes a `Click()` command on the control.|  
  
### <a name="see-also"></a>Xem thêm  
 [WebDDA](../unified-service-desk/web-dda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
