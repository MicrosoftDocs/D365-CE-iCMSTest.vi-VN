---
title: AttributeMatchPath in Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: The topic explains about the <AttributeMatchPath> element that can be utilized by a web control configuration to find the desired control on the currently loaded HTML document using the controls attributes.
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
ms.assetid: d0fcd69d-b049-4dff-8a08-1add589d88f9
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
ms.openlocfilehash: 680817aa986c4e840727cdfcb7db98a695188bb5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385750"
---
# <a name="attributematchpath"></a>AttributeMatchPath
Yếu tố `<AttributeMatchPath>` có thể được một cấu hình kiểm soát web sử dụng để tìm kiểm soát mong muốn trên tài liệu `HTML` hiện được tải bằng các thuộc tính kiểm soát. The "match path" is an ordered list of key/value pairs that is applied by iterating through every element in the `HTML``Document Object Model (DOM)`, matching attributes along the nodes of the match path. Mỗi khóa đại diện cho tên của thuộc tính để khớp và giá trị được khớp với giá trị thuộc tính đã chỉ định trong tài liệu `HTML`. Sau khi khớp một khóa/giá trị, cặp khóa/giá trị tiếp theo trong trình tự được sử dụng để so sánh với từng yếu tố trong `DOM`. Lưu ý rằng khi **keyn+1 = keyn**, việc khớp với cặp khóa/giá trị mới bắt đầu bằng nút yếu tố tiếp theo trong `DOM`, không phải với nút hiện tại.  
  
<a name="syntax"></a>   
## <a name="attributematchpath-syntax"></a>\<AttributeMatchPath> syntax  
 Yếu tố `<AttributeMatchPath>` có thể được nhắm mục tiêu tại các khung cụ thể bên trong ứng dụng `HTML`.  
  
```xml  
<AttributeMatchPath [framename=""|framesrc=""] [framematch="n"] [matchtype="equals|startswith|endswith|contains"]>  
  
<attributeName1 [matchtype= "equals|startswith|endswith|contains"]>  
attributeValueToMatch1  
</attributeName1>  
  
<attributeName2 [matchtype= "equals|startswith|endswith|contains"]>  
attributeValueToMatch2  
</attributeName2>  
  
…  
<attributeNamen [matchtype= "equals|startswith|endswith|contains"]>  
attributeValueToMatchn  
</attributeNamen>  
  
</AttributeMatchPath>  
  
```  
  
<a name="elements"></a>   
## <a name="attributematchpath-elements"></a>\<AttributeMatchPath> elements  
 Bảng sau mô tả các yếu tố của `<AttributeMatchPath>`  
  
|Yếu tố|Mô tả|  
|-------------|-----------------|  
|Framename|Khớp tên khung của IFrame.|  
|Framesrc|Khớp nguồn của IFrame.|  
|Framematch|Khớp vị trí thứ n của khung đã chỉ định, mặc định là `1`.|  
|Matchtype|Chỉ định cách kết hợp chú thích. Các giá trị có thể là `equals`, `startswith`, `endswith` hoặc `contains`; bất kỳ giá trị nào khác sẽ thêm ngoại lệ.|  
  
 Ví dụ, nếu một ứng dụng web có nhiều hơn một khung với một tên, bạn có thể chỉ định để tìm kiếm khung thứ hai hoặc thứ ba của tên đó. Thuộc tính `framematch` là không bắt buộc, tuy nhiên được giả định là 1 trừ khi được chỉ định. Nếu `framematch` được chỉ định, `framename` hoặc `framesrc` phải được xác định; Nếu không, một ngoại lệ "Khung không tìm thấy" sẽ được thêm.  
  
> [!NOTE]
>  Nếu không thuộc tính nào trong số các thuộc tính `AttributeMatchPath` được cung cấp, thao tác sẽ diễn ra trong cửa sổ cấp đầu tiên như thể nó là một khung. Nếu cả hai `framename` và `framesrc` được chỉ định, `framesrc` được ưu tiên.  
  
 Trong ví dụ sau đây, các `matchtype` được sử dụng trên `attributeValueToMatch`.  
  
```xml  
<AttributeMatchPath>  
<key1>val1</key1>  
<key2>val2</key2>  
<key3[matchtype="equals|startswith|endswith|contains"]>attributeValueToMatch</key3>  
  .  
<keyn>valn</keyn>  
</AttributeMatchPath>  
  
```  
  
 Ví dụ sau cho thấy một đường dẫn phù hợp thuộc tính cho thẻ `Test`.  
  
```xml  
Page code:    
<Test FirstName='John' LastName='Smith'/>  
  
Match path used in control description:    
<AttributeMatchPath>  
<FirstName>John</FirstName>  
<LastName>Smith</LastName>  
</AttributeMatchPath>  
  
```  
  
> [!NOTE]
>  Chúng tôi khuyến khách bạn chỉ sử dụng ID và/hoặc tên là thuộc tính dự án. Các thuộc tính khác sẽ có tác động tiêu cực đến hiệu suất.  
  
### <a name="see-also"></a>Xem thêm  
 [WebDDA](../unified-service-desk/web-dda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
