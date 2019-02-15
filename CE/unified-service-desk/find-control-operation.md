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
# <a name="findcontrol-operation-in-unified-service-desk"></a><span data-ttu-id="1190f-103">FindControl Operation in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="1190f-103">FindControl Operation in Unified Service Desk</span></span>
<span data-ttu-id="1190f-104">Chủ đề này mô tả hai cách tiếp cận có thể được sử dụng để xác định một kiểm soát giao diện người dùng (UI).</span><span class="sxs-lookup"><span data-stu-id="1190f-104">This topic describes the two approaches that can be used to identify a user interface (UI) control.</span></span>  
  
<a name="tree"></a>   
## <a name="ui-tree-based-identification"></a><span data-ttu-id="1190f-105">Nhận dạng UI dựa trên cấu trúc cây</span><span class="sxs-lookup"><span data-stu-id="1190f-105">UI Tree-based identification</span></span>  
 <span data-ttu-id="1190f-106">Cách tiếp cận này ghi lại cấu trúc cây kiểm soát hoàn chỉnh.</span><span class="sxs-lookup"><span data-stu-id="1190f-106">This approach captures the complete control tree structure.</span></span> <span data-ttu-id="1190f-107">Cách này sử dụng tất cả thuộc tính kiểm soát để đi tới kiểm soát cuối cùng.</span><span class="sxs-lookup"><span data-stu-id="1190f-107">It uses all the control properties to traverse to the final control.</span></span>  
  
 <span data-ttu-id="1190f-108">Mục sau là định dạng liên kết mẫu:</span><span class="sxs-lookup"><span data-stu-id="1190f-108">The following is a sample binding format:</span></span>  
  
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
  
 <span data-ttu-id="1190f-109">Các thẻ được giải thích như sau:</span><span class="sxs-lookup"><span data-stu-id="1190f-109">The tags are explained as follows:</span></span>  
  
-   <span data-ttu-id="1190f-110">`<UIElement>` – Đây là nút gốc, có thuộc tính `Name`:</span><span class="sxs-lookup"><span data-stu-id="1190f-110">`<UIElement>` – This is the root node, which has the `Name` attribute:</span></span>  
  
    -   <span data-ttu-id="1190f-111">`Name` – Lấy tên thân thiện sẽ được sử dụng trong DDA.</span><span class="sxs-lookup"><span data-stu-id="1190f-111">`Name` – Captures the friendly name that will be used in the DDA.</span></span>  
  
    -   <span data-ttu-id="1190f-112">`StartFromDesktop` – Xác định xem tìm kiếm từ máy tính để bàn hay từ cha mẹ hiện tại.</span><span class="sxs-lookup"><span data-stu-id="1190f-112">`StartFromDesktop` – Specifies if the search is from the desktop or the current parent.</span></span>  
  
    -   <span data-ttu-id="1190f-113">`ParentUIElement` – Chỉ định `UIElement` cần dùng làm kiểm soát cha mẹ.</span><span class="sxs-lookup"><span data-stu-id="1190f-113">`ParentUIElement` – Specifies the `UIElement` that needs to be taken as a parent control.</span></span> <span data-ttu-id="1190f-114">Đối với các nút, cần chỉ định "khung" là `ParentUIElement`.</span><span class="sxs-lookup"><span data-stu-id="1190f-114">For the buttons, "pane" needs to be specified as `ParentUIElement`.</span></span> <span data-ttu-id="1190f-115">Điều này sẽ hữu ích khi bạn tạo một liên kết theo cách thủ công.</span><span class="sxs-lookup"><span data-stu-id="1190f-115">This will be useful when you create a binding manually.</span></span>  
  
    -   <span data-ttu-id="1190f-116">`MatchCount` – Chỉ định số lượng kết quả phù hợp.</span><span class="sxs-lookup"><span data-stu-id="1190f-116">`MatchCount` – Specifies the match count.</span></span> <span data-ttu-id="1190f-117">Nếu có nhiều hơn một kiểm soát có cùng thuộc tính, số lượng sẽ được xác định dựa trên chỉ mục này.</span><span class="sxs-lookup"><span data-stu-id="1190f-117">If more than one control has the same properties, it will be identified based on this index.</span></span>  
  
-   <span data-ttu-id="1190f-118">`<UIObject>` – Nút này ghi lại cấu trúc cây hoàn chỉnh để xác định kiểm soát:</span><span class="sxs-lookup"><span data-stu-id="1190f-118">`<UIObject>` – This node captures the complete tree structure to identify the control:</span></span>  
  
    -   <span data-ttu-id="1190f-119">`<PropertyCondition Name="Name">CPCategoryPanel</PropertyCondition>` – Ghi lại điều kiện thuộc tính mà kiểm soát đang tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="1190f-119">`<PropertyCondition Name="Name">CPCategoryPanel</PropertyCondition>` – Captures the property condition that the control is searched for.</span></span> <span data-ttu-id="1190f-120">Điều kiện này sẽ được nhóm trong `AndCondition/OrCondition/NotCondition`.</span><span class="sxs-lookup"><span data-stu-id="1190f-120">This will be grouped in the `AndCondition/OrCondition/NotCondition`.</span></span> <span data-ttu-id="1190f-121">If there is only one `PropertyCondition`, it should be presented in root node without any grouping.</span><span class="sxs-lookup"><span data-stu-id="1190f-121">If there is only one `PropertyCondition`, it should be presented in root node without any grouping.</span></span>  <span data-ttu-id="1190f-122">`Name` represents the name of the control property.</span><span class="sxs-lookup"><span data-stu-id="1190f-122">`Name` represents the name of the control property.</span></span>  
  
    -   <span data-ttu-id="1190f-123">`AndCondition`,  `OrCondition` và `NotCondition` – Nhóm các điều kiện cho điều kiện thuộc tính.</span><span class="sxs-lookup"><span data-stu-id="1190f-123">`AndCondition`,  `OrCondition`, and `NotCondition` – Grouping conditions for the property condition.</span></span>  
  
    -   <span data-ttu-id="1190f-124">`<AndCondition Id="SearchCondition">` – Captures the property condition with which the control can be identified.</span><span class="sxs-lookup"><span data-stu-id="1190f-124">`<AndCondition Id="SearchCondition">` – Captures the property condition with which the control can be identified.</span></span>  <span data-ttu-id="1190f-125">`Id` represents the condition list ID.</span><span class="sxs-lookup"><span data-stu-id="1190f-125">`Id` represents the condition list ID.</span></span> <span data-ttu-id="1190f-126">Có thể sử dụng nhiều hơn một `AndCondition` khi nhóm được cung cấp sau này.</span><span class="sxs-lookup"><span data-stu-id="1190f-126">More than one `AndCondition` can be used when grouping is provided later.</span></span>  
  
    -   <span data-ttu-id="1190f-127">`<OrCondition Id="SearchCondition">` – Captures the property condition with which the control can be identified.</span><span class="sxs-lookup"><span data-stu-id="1190f-127">`<OrCondition Id="SearchCondition">` – Captures the property condition with which the control can be identified.</span></span>   <span data-ttu-id="1190f-128">`Id` represents the condition list ID.</span><span class="sxs-lookup"><span data-stu-id="1190f-128">`Id` represents the condition list ID.</span></span> <span data-ttu-id="1190f-129">Có thể sử dụng nhiều hơn một `OrCondition` khi nhóm được cung cấp sau này.</span><span class="sxs-lookup"><span data-stu-id="1190f-129">More than one `OrCondition` can be used when grouping is provided later.</span></span>  
  
    -   <span data-ttu-id="1190f-130">`<NotCondition Id="SearchCondition">` – Captures the property condition with which the control can be identified.</span><span class="sxs-lookup"><span data-stu-id="1190f-130">`<NotCondition Id="SearchCondition">` – Captures the property condition with which the control can be identified.</span></span>  <span data-ttu-id="1190f-131">`Id` represents the condition list ID.</span><span class="sxs-lookup"><span data-stu-id="1190f-131">`Id` represents the condition list ID.</span></span> <span data-ttu-id="1190f-132">Có thể sử dụng nhiều hơn một `NotCondition` khi nhóm được cung cấp sau này.</span><span class="sxs-lookup"><span data-stu-id="1190f-132">More than one `NotCondition` can be used when grouping is provided later.</span></span>  
  
    -   <span data-ttu-id="1190f-133">`AndCondition`,  `NotCondition`, and `OrCondition` – Có thể được lồng nhau nhưng chúng cần được nhóm chính xác.</span><span class="sxs-lookup"><span data-stu-id="1190f-133">`AndCondition`,  `NotCondition`, and `OrCondition` – Can be nested, but they should be grouped correctly.</span></span> <span data-ttu-id="1190f-134">The top XML bindings should have only one condition, and they can be internally grouped.</span><span class="sxs-lookup"><span data-stu-id="1190f-134">The top XML bindings should have only one condition, and they can be internally grouped.</span></span>  
  
<a name="offset"></a>   
## <a name="offset-based-identification"></a><span data-ttu-id="1190f-135">Nhận dạng dựa trên khoảng bù</span><span class="sxs-lookup"><span data-stu-id="1190f-135">Offset-based Identification</span></span>  
 <span data-ttu-id="1190f-136">Cách tiếp cận này là rất dễ sử dụng và cũng xây dựng các liên kết.</span><span class="sxs-lookup"><span data-stu-id="1190f-136">This approach is very easy to use and also builds the bindings.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1190f-137">Cách tiếp cận này không phải là có thể sử dụng khi vị trí cây kiểm soát tiếp tục thay đổi, bởi vì nó sử dụng số vị trí trong Cây UI để xác định các kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="1190f-137">This approach is not usable when the control tree location keeps changing, because it uses the position number in the UI Tree to identify the controls.</span></span> <span data-ttu-id="1190f-138">Nếu vị trí Cây UI được thay đổi tự động, cách tiếp cận này là không sử dụng được.</span><span class="sxs-lookup"><span data-stu-id="1190f-138">If the UI Tree position gets changed dynamically, this approach is unusable.</span></span>  
  
 <span data-ttu-id="1190f-139">Thuộc tính `MatchCount` sẽ được sử dụng như mức độ bù đắp.</span><span class="sxs-lookup"><span data-stu-id="1190f-139">`MatchCount` attribute will be used as an offset level.</span></span> <span data-ttu-id="1190f-140">Điều kiện sẽ được cung cấp nếu cần.</span><span class="sxs-lookup"><span data-stu-id="1190f-140">Conditions shall be provided if required.</span></span>  
  
 <span data-ttu-id="1190f-141">Mục sau hiển thị định dạng liên kết mẫu.</span><span class="sxs-lookup"><span data-stu-id="1190f-141">The following shows a sample binding format.</span></span>  
  
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
  
### <a name="see-also"></a><span data-ttu-id="1190f-142">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1190f-142">See also</span></span>  
 <span data-ttu-id="1190f-143">[UIADDA](../unified-service-desk/uiadda.md) </span><span class="sxs-lookup"><span data-stu-id="1190f-143">[UIADDA](../unified-service-desk/uiadda.md) </span></span>  
 [<span data-ttu-id="1190f-144">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="1190f-144">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
