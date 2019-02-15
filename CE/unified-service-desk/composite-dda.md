---
title: Composite DDA | MicrosoftDocs
description: The composite data-driven adapter is an extension of the DDA architecture introduced with UII. Bộ chuyển đổi được tích hợp để giải quyết vấn đề khi bạn chỉ có thể gán một loại DDA cho một ứng dụng. Trong một số trường hợp, một ứng dụng có thể cần công nghệ khác do DDA khác cung cấp để truy cập chức năng được yêu cầu.
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
ms.assetid: dee27756-e74c-465f-a6b0-383b581e693e
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
ms.openlocfilehash: 4d63924152420f67c023d1d59d76e8031fc23b1b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388095"
---
# <a name="composite-dda"></a>DDA Tổng hợp
Bộ chuyển đổi định hướng dữ liệu tổng hợp là phần mở rộng của kiến trúc DDA được giới thiệu với [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)]. Bộ chuyển đổi được tích hợp để giải quyết vấn đề khi bạn chỉ có thể gán một loại DDA cho một ứng dụng. Trong một số trường hợp, một ứng dụng có thể cần công nghệ khác do DDA khác cung cấp để truy cập chức năng được yêu cầu. Một ví dụ cho điều này có thể là một applet Java trong ứng dụng web. Bạn có thể sử dụng DDA tổng hợp trong những tình huống.  
  
## <a name="composite-dda-bindings"></a>Liên kết DDA tổng hợp  
 Liên kết DDA tổng hợp tương tự với DDA khác. The bindings are simply added to a `<DataDrivenAdapterBindingsCollection>` collection, which supports adding bindings of different types. Mẫu sau đây hiển thị bộ sưu tập liên kết của ba DDA. Tuy nhiên, bạn chí có thể thêm một bộ sưu tập cho mỗi ứng dụng.  
  
```xml  
<DataDrivenAdapterBindingsCollection>  
   <Type>DDAType1, DDAAssembly</Type>   
   <Controls>  
    …  
   </Controls>  
</DataDrivenAdapterBindings>  
  
<DataDrivenAdapterBindings prefix="dda1">  
   <Type>DDAType2, DDAAssembly</Type>   
   <Controls>  
   …  
   </Controls>  
   </DataDrivenAdapterBindings>  
<DataDrivenAdapterBindings prefix="dda2">  
   <Type>DDAType3, DDAAssembly</Type>   
   <Controls>  
   …  
   </Controls>  
</DataDrivenAdapterBindings>  
</DataDrivenAdapterBindingsCollection>  
  
```  
  
 Mỗi thẻ trong số các thẻ `<DataDrivenAdapterBindings>` có thể có tiền tố tham số tùy chọn. Điều này cho phép sử dụng cùng tên kiểm soát tổ chức trong các phần liên kết khác nhau. Nếu tiền tố được xác định, tất cả các kiểm soát trong DDA này sẽ có tiền tố gắn vào tên kiểm soát của chúng.  
  
> [!NOTE]
>  Mỗi liên kết DDA phải luôn được gọi với tiền tố tương ứng của mình. Ví dụ: nếu `DDAType2` và `DDAType3` có kiểm soát được chỉ định trong tên `Button1`, kiểm soát tổ chức được sử dụng trong quá trình tự động hóa là `dda1Button1` và `dda2Button1`.  
> 
> [!NOTE]
>  Nếu trang web chứa kiểm soát [!INCLUDE[pn_ms_ActiveX_short](../includes/pn-ms-activex-short.md)] hoặc Applet [!INCLUDE[pn_Java](../includes/pn-java.md)], hành động mặc định của ứng dụng web không chờ kiểm soát [!INCLUDE[pn_ms_ActiveX_short](../includes/pn-ms-activex-short.md)] hoặc Applet [!INCLUDE[pn_Java](../includes/pn-java.md)] tải.  
  
### <a name="see-also"></a>Xem thêm  
 [Use Data Driven Adapters](../unified-service-desk/use-data-driven-adapters-ddas.md)
