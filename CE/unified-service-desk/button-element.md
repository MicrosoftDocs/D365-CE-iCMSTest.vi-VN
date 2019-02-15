---
title: ButtonElement | MicrosoftDocs
description: The topic explains about <ButtonElement> element syntax and the elements, which is one of the binding elements of the WebDDA.
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
ms.assetid: a67be8bc-6d28-4c99-a62a-397169a92eec
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
ms.openlocfilehash: 33ab4a99c2931b678ef70db9211b9241d116873c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387194"
---
# <a name="buttonelement"></a>ButtonElement
`<ButtonElement>` là một trong các yếu tố liên kết của WebDDA. Chủ đề này mô tả cú pháp và các yếu tố của `<ButtonElement>`  
  
## <a name="buttonelement-syntax"></a>\<ButtonElement> syntax  
 Yếu tố `<ButtonElement>` liên kết kiểm soát có tên với yếu tố `<button/> HTML`. Đoạn mã sau hiển thị cách sử dụng `<ButtonElement>`:  
  
```xml  
<ButtonElement name="control name">  
Search Path Elements  
</ButtonElement>  
  
```  
  
## <a name="elements-of-buttonelement"></a>Elements of \<ButtonElement>  
 Bảng sau mô tả các yếu tố của `<ButtonElement>`  
  
|Yếu tố|Mô tả|  
|-------------|-----------------|  
|FindControl|Trả về `True` hoặc `False` tùy theo kiểm soát có thể được tìm thấy trên UI hay không.|  
|GetControlValue|Trả về văn bản URL.|  
|SetControlValue|Bỏ một ngoại lệ `UnsupportedControlOperation`.|  
|ExecuteControlAction|Thực hiện một lệnh `Click()` trên kiểm soát.|  
  
### <a name="see-also"></a>Xem thêm  
 [WebDDA](../unified-service-desk/web-dda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
