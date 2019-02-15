---
title: FindControl Operation in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The topic describes the two approaches that can be used to identify a user interface (UI) control.
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
ms.assetid: 58f889c3-86d3-4f0d-b39b-9955200b582a
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
ms.openlocfilehash: b1f34b152b01996325cf4f783826904a3e9a5dc6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387771"
---
# <a name="findcontrol-operation-in-unified-service-desk"></a>FindControl Operation in Unified Service Desk
Chủ đề này mô tả hai cách tiếp cận có thể được sử dụng để xác định một kiểm soát giao diện người dùng (UI).  
  
<a name="tree"></a>   
## <a name="ui-tree-based-identification"></a>Nhận dạng UI dựa trên cấu trúc cây  
 Cách tiếp cận này ghi lại cấu trúc cây kiểm soát hoàn chỉnh. Cách này sử dụng tất cả thuộc tính kiểm soát để đi tới kiểm soát cuối cùng.  
  
 Mục sau là định dạng liên kết mẫu:  
  
```xml  
<UIElement Name="UISystemandSecurityHyperlink">  
<UIObject MatchCount="1">                              
              <AndCondition>  
                <PropertyCondition Name="Name">CPCategoryPanel</PropertyCondition>  
                <PropertyCondition Name="ControlType">Pane</PropertyCondition>  
              </AndCondition>  
                <UIObject>                                     
                  <AndCondition>  
                    <PropertyCondition Name="Name">System and Security</PropertyCondition>  
                    <PropertyCondition Name="ControlType">Hyperlink</PropertyCondition>  
                  </AndCondition>                    
                </UIObject>  
            </UIObject>  
<UIElement>  
  
```  
  
 Các thẻ được giải thích như sau:  
  
-   `<UIElement>` – Đây là nút gốc, có thuộc tính `Name`:  
  
    -   `Name` – Lấy tên thân thiện sẽ được sử dụng trong DDA.  
  
    -   `StartFromDesktop` – Xác định xem tìm kiếm từ máy tính để bàn hay từ cha mẹ hiện tại.  
  
    -   `ParentUIElement` – Chỉ định `UIElement` cần dùng làm kiểm soát cha mẹ. Đối với các nút, cần chỉ định "khung" là `ParentUIElement`. Điều này sẽ hữu ích khi bạn tạo một liên kết theo cách thủ công.  
  
    -   `MatchCount` – Chỉ định số lượng kết quả phù hợp. Nếu có nhiều hơn một kiểm soát có cùng thuộc tính, số lượng sẽ được xác định dựa trên chỉ mục này.  
  
-   `<UIObject>` – Nút này ghi lại cấu trúc cây hoàn chỉnh để xác định kiểm soát:  
  
    -   `<PropertyCondition Name="Name">CPCategoryPanel</PropertyCondition>` – Ghi lại điều kiện thuộc tính mà kiểm soát đang tìm kiếm. Điều kiện này sẽ được nhóm trong `AndCondition/OrCondition/NotCondition`. If there is only one `PropertyCondition`, it should be presented in root node without any grouping.  `Name` represents the name of the control property.  
  
    -   `AndCondition`,  `OrCondition` và `NotCondition` – Nhóm các điều kiện cho điều kiện thuộc tính.  
  
    -   `<AndCondition Id="SearchCondition">` – Captures the property condition with which the control can be identified.  `Id` represents the condition list ID. Có thể sử dụng nhiều hơn một `AndCondition` khi nhóm được cung cấp sau này.  
  
    -   `<OrCondition Id="SearchCondition">` – Captures the property condition with which the control can be identified.   `Id` represents the condition list ID. Có thể sử dụng nhiều hơn một `OrCondition` khi nhóm được cung cấp sau này.  
  
    -   `<NotCondition Id="SearchCondition">` – Captures the property condition with which the control can be identified.  `Id` represents the condition list ID. Có thể sử dụng nhiều hơn một `NotCondition` khi nhóm được cung cấp sau này.  
  
    -   `AndCondition`,  `NotCondition`, and `OrCondition` – Có thể được lồng nhau nhưng chúng cần được nhóm chính xác. The top XML bindings should have only one condition, and they can be internally grouped.  
  
<a name="offset"></a>   
## <a name="offset-based-identification"></a>Nhận dạng dựa trên khoảng bù  
 Cách tiếp cận này là rất dễ sử dụng và cũng xây dựng các liên kết.  
  
> [!NOTE]
>  Cách tiếp cận này không phải là có thể sử dụng khi vị trí cây kiểm soát tiếp tục thay đổi, bởi vì nó sử dụng số vị trí trong Cây UI để xác định các kiểm soát. Nếu vị trí Cây UI được thay đổi tự động, cách tiếp cận này là không sử dụng được.  
  
 Thuộc tính `MatchCount` sẽ được sử dụng như mức độ bù đắp. Điều kiện sẽ được cung cấp nếu cần.  
  
 Mục sau hiển thị định dạng liên kết mẫu.  
  
```xml  
<UIElement name="textBoxTabPage1">  
          <UIObject MatchCount="2">              
            <UIObject  MatchCount="1">               
              <UIObject   MatchCount="2">                  
              </UIObject>  
            </UIObject>  
          </UIObject>  
        </UIElement>  
  
```  
  
### <a name="see-also"></a>Xem thêm  
 [UIADDA](../unified-service-desk/uiadda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
