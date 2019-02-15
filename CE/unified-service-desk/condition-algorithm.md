---
title: Condition Algorithm | MicrosoftDocs
description: The topic describes the groupings of a control that needs to be uniquely identified by specifying some property condition to distinguish it from other controls.
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
ms.assetid: 855ec0d6-33a4-450f-a77a-b580b2b24946
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
ms.openlocfilehash: b61f6553d88bbf19612cc49f7bab0473b3cf46fc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387246"
---
# <a name="condition-algorithm"></a>Thuật toán Điều kiện
Một kiểm soát cần phải được xác định duy nhất bằng cách xác định một số điều kiện thuộc tính để phân biệt nó với các kiểm soát khác. Chủ đề này mô tả nhóm giúp xác định các điều kiện.  
  
## <a name="conditions-to-uniquely-identify-the-controls"></a>Điều kiện để nhận dạng duy nhất các kiểm soát  
  
-   `NoCondition`:  `NoCondition` nên được đưa ra để chỉ định yếu tố đầu tiên của cây.  
  
-   `PropertyCondition`: Điều kiện chỉ định thuộc tính thực và giá trị mong muốn. Sau đây là một ví dụ.  
  
    ```xml  
    <PropertyCondition Name="ControlType">ControlType.Pane</PropertyCondition>  
  
    ```  
  
     Điều kiện này chỉ định rằng `ControlType` nên là `"ControlType.Pane".`  
  
-   `AndCondition`:  
  
    -   Điều này nhóm các điều kiện và kết quả thuộc tính trong TruePositive nếu tất cả điều kiện thuộc tính đều được thỏa mãn.  
  
    -   Tối thiểu hai điều kiện phải được cung cấp trong nhóm `AndCondition`. Sau đây là một ví dụ.  
  
        ```xml  
        <AndCondition Id="SearchCondition">  
        <PropertyCondition Name="Name">System and Security</PropertyCondition>  
        <PropertyCondition Name="ControlType">Hyperlink</PropertyCondition>  
        </AndCondition>  
  
        ```  
  
         Điều kiện này chỉ định rằng cả hai thuộc tính `ControlType` và `Name` đều cần được thỏa mãn. `Name` và `Value` có thể được xác định từ chi tiết UISpy của kiểm soát.  
  
-   `OrCondition`:  
  
    -   Điều này nhóm các điều kiện và kết quả thuộc tính trong `TruePositive` nếu bất kỳ một điều kiện thuộc tính nào được thỏa mãn.  
  
    -   Tối thiểu hai điều kiện phải được cung cấp trong nhóm `OrCondition`. Sau đây là một ví dụ.  
  
        ```xml  
        <OrCondition Id="SearchCondition">  
        <PropertyCondition Name="Name">System and Security</PropertyCondition>  
        <PropertyCondition Name="ControlType">Hyperlink</PropertyCondition>  
        </OrCondition>    
        ```  
  
         Điều kiện này chỉ định rằng thuộc tính `ControlType` hoặc `Name` cần được thỏa mãn. `Name` và `Value` có thể được xác định từ chi tiết UISpy của kiểm soát.  
  
-   `NotCondition`:  
  
    -   Điều này nhóm các điều kiện và kết quả thuộc tính trong `TruePositive` nếu điều kiện thuộc tính không được thỏa mãn.  
  
    -   Chỉ một điều kiện có thể được cung cấp trong nhóm `NotCondition`. Sau đây là một ví dụ.  
  
        ```xml  
        <NotCondition Id="SearchCondition">  
        <PropertyCondition Name="Name">System and Security</PropertyCondition>  
        </NotCondition>  
  
        ```  
  
         Điều kiện này chỉ định nếu điều kiện thuộc tính `Name` không được thỏa mãn. `Name` và `Value` có thể được xác định từ chi tiết UISpy của kiểm soát.  
  
-   `NestedCondition`:  
  
    -   Nhóm lồng nhau phải được chỉ định, chẳng hạn như `OrCondition` trong `AndCondition`. Điều kiện con cuối cùng nên là `PropertyCondition`.  
  
    -   Bất kỳ thuộc tính thuộc loại sau đây đều có thể được bao gồm trong điều kiện:  
  
        -   `System.Boolean`  
  
        -   `System.String`  
  
        -   `System.Windows.Rect`  
  
        -   `System.Windows.Point`  
  
        -   `System.Windows.Automation.OrientationType`  
  
        -   `System.Windows.Automation.ControlType`  
  
### <a name="see-also"></a>Xem thêm  
 [UIADDA](../unified-service-desk/uiadda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
