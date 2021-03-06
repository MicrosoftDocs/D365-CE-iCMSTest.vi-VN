---
title: AccControl Tag | MicrosoftDocs
description: Learn about the AccControl tag that uses the IAccessible interface from Microsoft Active Accessibility (MSAA).
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
ms.assetid: e4d9d212-1709-4983-8d57-9359cda932fd
caps.latest.revision: 8
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: ceb972e7f2876882cd2486f0fb1bcf970bda1520
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388441"
---
# <a name="acccontrol-tag"></a>Thẻ AccControl
Thẻ `AccControl` sử dụng giao diện [IAccessible](https://msdn.microsoft.com/library/accessibility.iaccessible\(v=vs.110\).aspx) từ Microsoft Active Accessibility (MSAA). Thẻ AccControl có:  
  
- Thuộc tính `Name` để xác định tên thân thiện với người dùng cho một kiểm soát.  
  
- Thẻ `Path` xác định đường dẫn tìm kiếm cho kiểm soát trong cây `IAccessibility` của ứng dụng. The `<Path>` tag contains the following: [FindWindow Tag](../unified-service-desk/find-window-tag.md) and [Next Tag](../unified-service-desk/next-tag-windda.md).  
  
  The following XML example shows a control definition using the `AccControl` tag.  
  
```xml  
<AccControl name="Control Name">  
   <Path>   
      <FindWindow>  
         <CaptionStartsWith>Customer App</CaptionStartsWith>  
      </FindWindow>  
      <Next/>  
      <Next match="2">Customer Name:</Next>  
   </Path>  
</AccControl>  
```  
  
> [!NOTE]
>  Một số yếu tố trong thẻ `Path` có thuộc tính `<match>` mà bạn có thể sử dụng để thêm bộ đếm vào mô tả tìm kiếm. Both the following examples return the same search result, but the first example implements the `<match>` tag:  
> 
> - **Ví dụ 1**  
> 
>    ```  
>    <Caption match="2">Test Application</Caption>  
>    ```  
>   - Ví dụ 2:  
> 
>     ```  
>     <Caption>Test Application</Caption>  
>     <Caption>Test Application</Caption>  
>     ```  
> 
>   Nếu `<match>` không được chỉ định, giá trị mặc định là 0.  
  
 The [String)](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.datadrivenadapterbase.getcontrolvalue\(system.string,system.string\)) method on an `AccControl` tag is always mapped to the `get_accValue` method on the subject `IAccessible` node, unless the node contains `role="radio button"` or `role="check box"`. In these cases, the [String)](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.datadrivenadapterbase.getcontrolvalue\(system.string,system.string\)) method returns `True` or `False`, depending on whether the state of the node is selected.  
  
 The [String)](https://docs.microsoft.com/dotnet/api/microsoft.uii.hostedapplicationtoolkit.datadrivenadapter.datadrivenadapterbase.setcontrolvalue\(system.string,system.string,system.string\)) method on an `AccControl` tag is always mapped to the `set_accValue` method on the subject `IAccessible` node, with the exception of nodes that have `role="radio button"` or `role="check box"`. Trong trường hợp nút radio, ngoại lệ `UnsupportedControlOperation` được đưa ra vì nút radio không thể được gán giá trị `True` hoặc `False`.  
  
 The following example displays the [RELAX NG](http://relaxng.org/compact-tutorial-20030326.html) XML code for the \<Path> tag.  
  
```xml  
# RELAX NG XML grammar for Path  
# http://relaxng.org/compact-tutorial-20030326.html  
#  
grammar   
{  
   start = Path  
   Path = element Path   
   {   
      FindWindow* & element Next   
      { attribute match { xsd:integer }?  
      ,attribute offset { xsd:integer  }?,text? }*   
   }  
}  
```  
  
### <a name="see-also"></a>Xem thêm  
 [Win DDA](../unified-service-desk/windda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
