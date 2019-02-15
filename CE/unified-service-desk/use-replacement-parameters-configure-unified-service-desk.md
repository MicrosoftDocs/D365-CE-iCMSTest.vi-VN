---
title: Use replacement parameters to configure Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn how to use replacement parameters in Unified Service Desk to customize amd personalize interactions through actions and window navigation rules.
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
ms.assetid: 8d435068-1fd3-4886-b574-f1001dc21bc8
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
ms.openlocfilehash: 03b285e509a2cc44cd1cb550033ffb108ebb03a8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388698"
---
# <a name="use-replacement-parameters-to-configure-unified-service-desk"></a>Use replacement parameters to configure Unified Service Desk
Thông số thay thế có thể được sử dụng để tuỳ chỉnh tương tác trong một quá trình kinh doanh cụ thể thông qua quy tắc điều hướng cửa sổ và hành động. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Replacement parameters](../unified-service-desk/replacement-parameters.md)  

 Chủ đề này cung cấp thông tin về các phím thay thế mà bạn có thể sử dụng trong các tham số thay thế để chỉ ra cách xử lý đặc biệt về cách bạn có thể sử dụng các tham số thay thế trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] trong một số điều kiện đặc biệt.  

<a name="ReplacementKeys"></a>   
## <a name="replacement-keys"></a>Phím thay thế  
 Bảng dưới đây cung cấp các thông tin về các phím thay thế mà bạn có thể sử dụng trong các tham số thay thế.  


| Phím thay thế |                                                                                                                                                                                                                                          Mô tả                                                                                                                                                                                                                                           |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        +        |     Phím này, khi có, sẽ thay thế phím không tồn tại hoặc không có bằng một chuỗi trống.<br /><br /> For example: In the scenario where `account.name` is undefined, calling `[[account.name]]` would result in a “Not all parameters in action call *\<ActionName>* are available, aborting action call.” error. This will stop processing the rule or line item being executed.<br /><br /> However, `[[account.name]+]` will return a blank, and not raise the replacement key error.      |
|        $        |                                                                                                                                          Phím này cho phép thoát trong dấu ngoặc kép và xuống dòng. Nó thường được sử dụng như là một toán tử khi gọi một scriptlet hoặc trả về chuỗi nhiều dòng.<br /><br /> Ví dụ: `[[script.MyMultiLineString]$]`                                                                                                                                          |
|        ^        |                                                                                                                                                                    Phím này ngăn không cho thoát dấu ngoặc kép và xuống dòng và được sử dụng để làm đồng đều bộ kết quả nhiều dòng.<br /><br /> Ví dụ: `MyMultiline=[[myvalue]^]`                                                                                                                                                                     |
|        u        |                                                                                        Khóa này được sử dụng cho tham số thay thế Mã hóa URL (cũng được gọi là Mã hóa tỷ lệ).<br /><br /> For example, consider the replacement parameter in the following URL: http://mysite?something=`[[opportunity.name]u]`.<br /><br /> The following string is returned: http://mysite?something=My%20Opportunity.                                                                                        |
|        x        |                                                                                                                                                Khóa này được sử dụng cho tham số thay thế Mã hóa XML. Cho phép các ký tự XAML, chẳng hạn như <, để thoát và hiển thị đúng trong đầu ra.<br /><br /> Ví dụ, `[[myvalue]x]`.                                                                                                                                                |
|        g        |                                                                                                                                                                    Khóa này được sử dụng để trả về giá trị từ phiên chung. Nếu không tìm thấy khóa trong phiên chung, nó sẽ dẫn đến lỗi không tìm thấy khóa.                                                                                                                                                                    |
|        a        |                                                                                                                                                         Khóa này được sử dụng để trả về giá trị từ phiên đang hiện hoạt mà được tập trung. Nếu không tìm thấy khóa trong phiên hiện hoạt nó sẽ dẫn đến lỗi không tìm thấy khóa.                                                                                                                                                         |
|        v        | Khóa này được sử dụng để thay thế các khóa trong khóa thay thế.<br /><br /> Ví dụ, hãy xem xét hai giá trị sau đây:<br /><br /> -   account.name = "My Account"<br />-   mytemplate.value = "My template is `[[account.name]+]`"<br /><br /> When you invoke the `[[mytemplate.value]]`, the following string is returned: “My Template is [[account.name]+]".<br /><br /> However, when you invoke `[[mytemplate.value]v]`, the following string is returned: "My template is My Account". |

<a name="SpecializedHandlers"></a>   
## <a name="specialized-handlers"></a>Trình xử lý chuyên dụng  
 Thông thường, chúng ta có nhu cầu thực hiện mọi việc đơn giản, giống như nếu/sau đó/loại khác xây dựng mà không đảm bảo tạo ra scriptlet. Các tình huống này yêu cầu sử dụng một scriptlet bên trong một cuộc gọi hành động. There are two specialized handlers to assist when building inline scriptlets in action calls: `$Expression` and `$Multiline`.  

### <a name="expression"></a>$Biểu thức  
 Consider a situation where you need to switch display name based on the entity type code (etc) of the current entity. Bạn đang xây dựng một URL cần thông tin này. Trong tình huống này, chỉ có thể tải tài khoản hoặc liên hệ.  

 In this scenario, we are calling the **Navigate** action on a **Standard Web Application** hosted control by using the following value in the **Data** field:  

```  
url= http://mysite/showmessage.aspx?displayname={either the account or contact display name}  
```  

 To achieve this, we will use `$Expression` as follows:  

```  
url= http://mysite/showmessage.aspx?displayname=$Expression("[[$Context.etc]]" == "1" ? "[[account.name]u+]" : "[[contact.fullname]u+]")  
```  

 Điều này có hiệu quả tạo ra và chạy một scriptlet như các hành động được xử lý.  

### <a name="multiline"></a>$Đa dòng  
 Trong phần $Biểu thức, chúng tôi đã nói về cách thực hiện sriptlet nội tuyến bên trong một hành động. Trong tình hình có yêu cầu thực hiện một scriptlet phức tạp hơn và bạn vẫn không muốn sử dụng đối tượng scriptlet để lưu trữ scriptlet, lệnh $Đa dòng có thể được sử dụng để lưu trữ Scriptlet phức tạp hơn.  

 For example, using the example we used earlier in the `$Expression` section, it can be broken out as:  

```  
url= http://mysite/showmessage.aspx?displayname=$Multiline( $Expression(  
function doWork()  
{  
      If ("[[$Context.etc]]" == "1")  
          return "[[account.name]u+]"   
      else   
          return "[[contact.fullname]u+]"  
}  
doWork();   
))  
```  

### <a name="see-also"></a>Xem thêm  
 [Thông số thay thế](../unified-service-desk/replacement-parameters.md)   
 [Execute scripts using scriptlets in Unified Service Desk](../unified-service-desk/execute-scripts-using-scriptlets-unified-service-desk.md)   
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
