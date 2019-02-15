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
# <a name="condition-algorithm"></a><span data-ttu-id="ffd2d-103">Thuật toán Điều kiện</span><span class="sxs-lookup"><span data-stu-id="ffd2d-103">Condition Algorithm</span></span>
<span data-ttu-id="ffd2d-104">Một kiểm soát cần phải được xác định duy nhất bằng cách xác định một số điều kiện thuộc tính để phân biệt nó với các kiểm soát khác.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-104">A control needs to be uniquely identified by specifying some property condition to distinguish it from other controls.</span></span> <span data-ttu-id="ffd2d-105">Chủ đề này mô tả nhóm giúp xác định các điều kiện.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-105">This topic describes the groupings that help specify the condition.</span></span>  
  
## <a name="conditions-to-uniquely-identify-the-controls"></a><span data-ttu-id="ffd2d-106">Điều kiện để nhận dạng duy nhất các kiểm soát</span><span class="sxs-lookup"><span data-stu-id="ffd2d-106">Conditions to uniquely identify the controls</span></span>  
  
-   <span data-ttu-id="ffd2d-107">`NoCondition`:  `NoCondition` nên được đưa ra để chỉ định yếu tố đầu tiên của cây.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-107">`NoCondition`:  `NoCondition` should be given to specify the first element of the tree.</span></span>  
  
-   <span data-ttu-id="ffd2d-108">`PropertyCondition`: Điều kiện chỉ định thuộc tính thực và giá trị mong muốn.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-108">`PropertyCondition`: It specifies the actual property and the expected value.</span></span> <span data-ttu-id="ffd2d-109">Sau đây là một ví dụ.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-109">The following is an example.</span></span>  
  
    ```xml  
    <PropertyCondition Name="ControlType">ControlType.Pane</PropertyCondition>  
  
    ```  
  
     <span data-ttu-id="ffd2d-110">Điều kiện này chỉ định rằng `ControlType` nên là `"ControlType.Pane".`</span><span class="sxs-lookup"><span data-stu-id="ffd2d-110">This condition specifies that `ControlType` should be `"ControlType.Pane".`</span></span>  
  
-   <span data-ttu-id="ffd2d-111">`AndCondition`:</span><span class="sxs-lookup"><span data-stu-id="ffd2d-111">`AndCondition`:</span></span>  
  
    -   <span data-ttu-id="ffd2d-112">Điều này nhóm các điều kiện và kết quả thuộc tính trong TruePositive nếu tất cả điều kiện thuộc tính đều được thỏa mãn.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-112">This groups the property conditions and results in TruePositive if all the property conditions are satisfied.</span></span>  
  
    -   <span data-ttu-id="ffd2d-113">Tối thiểu hai điều kiện phải được cung cấp trong nhóm `AndCondition`.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-113">A minimum of two conditions must be given inside an `AndCondition` group.</span></span> <span data-ttu-id="ffd2d-114">Sau đây là một ví dụ.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-114">The following is an example.</span></span>  
  
        ```xml  
        <AndCondition Id="SearchCondition">  
        <PropertyCondition Name="Name">System and Security</PropertyCondition>  
        <PropertyCondition Name="ControlType">Hyperlink</PropertyCondition>  
        </AndCondition>  
  
        ```  
  
         <span data-ttu-id="ffd2d-115">Điều kiện này chỉ định rằng cả hai thuộc tính `ControlType` và `Name` đều cần được thỏa mãn.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-115">This condition specifies that both the `ControlType` and `Name` properties need to be satisfied.</span></span> <span data-ttu-id="ffd2d-116">`Name` và `Value` có thể được xác định từ chi tiết UISpy của kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-116">The `Name` and the `Value` can be determined from the UISpy details of the control.</span></span>  
  
-   <span data-ttu-id="ffd2d-117">`OrCondition`:</span><span class="sxs-lookup"><span data-stu-id="ffd2d-117">`OrCondition`:</span></span>  
  
    -   <span data-ttu-id="ffd2d-118">Điều này nhóm các điều kiện và kết quả thuộc tính trong `TruePositive` nếu bất kỳ một điều kiện thuộc tính nào được thỏa mãn.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-118">This groups the property conditions and results in `TruePositive` if any one of the property conditions is satisfied.</span></span>  
  
    -   <span data-ttu-id="ffd2d-119">Tối thiểu hai điều kiện phải được cung cấp trong nhóm `OrCondition`.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-119">A minimum of two conditions should be given inside the `OrCondition` group.</span></span> <span data-ttu-id="ffd2d-120">Sau đây là một ví dụ.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-120">The following is an example.</span></span>  
  
        ```xml  
        <OrCondition Id="SearchCondition">  
        <PropertyCondition Name="Name">System and Security</PropertyCondition>  
        <PropertyCondition Name="ControlType">Hyperlink</PropertyCondition>  
        </OrCondition>    
        ```  
  
         <span data-ttu-id="ffd2d-121">Điều kiện này chỉ định rằng thuộc tính `ControlType` hoặc `Name` cần được thỏa mãn.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-121">This condition specifies that either `ControlType` or `Name` property needs to be satisfied.</span></span> <span data-ttu-id="ffd2d-122">`Name` và `Value` có thể được xác định từ chi tiết UISpy của kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-122">The `Name` and the `Value` can be determined from the UISpy details of the control.</span></span>  
  
-   <span data-ttu-id="ffd2d-123">`NotCondition`:</span><span class="sxs-lookup"><span data-stu-id="ffd2d-123">`NotCondition`:</span></span>  
  
    -   <span data-ttu-id="ffd2d-124">Điều này nhóm các điều kiện và kết quả thuộc tính trong `TruePositive` nếu điều kiện thuộc tính không được thỏa mãn.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-124">This groups the property conditions and results in `TruePositive` if the property conditions are not satisfied.</span></span>  
  
    -   <span data-ttu-id="ffd2d-125">Chỉ một điều kiện có thể được cung cấp trong nhóm `NotCondition`.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-125">Only one condition can be given inside a `NotCondition` group.</span></span> <span data-ttu-id="ffd2d-126">Sau đây là một ví dụ.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-126">The following is an example.</span></span>  
  
        ```xml  
        <NotCondition Id="SearchCondition">  
        <PropertyCondition Name="Name">System and Security</PropertyCondition>  
        </NotCondition>  
  
        ```  
  
         <span data-ttu-id="ffd2d-127">Điều kiện này chỉ định nếu điều kiện thuộc tính `Name` không được thỏa mãn.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-127">This condition specifies if the `Name` property condition is not satisfied.</span></span> <span data-ttu-id="ffd2d-128">`Name` và `Value` có thể được xác định từ chi tiết UISpy của kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-128">The `Name` and the `Value` can be determined from the UISpy details of the control.</span></span>  
  
-   <span data-ttu-id="ffd2d-129">`NestedCondition`:</span><span class="sxs-lookup"><span data-stu-id="ffd2d-129">`NestedCondition`:</span></span>  
  
    -   <span data-ttu-id="ffd2d-130">Nhóm lồng nhau phải được chỉ định, chẳng hạn như `OrCondition` trong `AndCondition`.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-130">The nested grouping must be specified, such as an `OrCondition` in an `AndCondition`.</span></span> <span data-ttu-id="ffd2d-131">Điều kiện con cuối cùng nên là `PropertyCondition`.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-131">The final child condition should be a `PropertyCondition`.</span></span>  
  
    -   <span data-ttu-id="ffd2d-132">Bất kỳ thuộc tính thuộc loại sau đây đều có thể được bao gồm trong điều kiện:</span><span class="sxs-lookup"><span data-stu-id="ffd2d-132">Any property of following type can be included in the condition:</span></span>  
  
        -   `System.Boolean`  
  
        -   `System.String`  
  
        -   `System.Windows.Rect`  
  
        -   `System.Windows.Point`  
  
        -   `System.Windows.Automation.OrientationType`  
  
        -   `System.Windows.Automation.ControlType`  
  
### <a name="see-also"></a><span data-ttu-id="ffd2d-133">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ffd2d-133">See also</span></span>  
 <span data-ttu-id="ffd2d-134">[UIADDA](../unified-service-desk/uiadda.md) </span><span class="sxs-lookup"><span data-stu-id="ffd2d-134">[UIADDA](../unified-service-desk/uiadda.md) </span></span>  
 [<span data-ttu-id="ffd2d-135">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="ffd2d-135">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
