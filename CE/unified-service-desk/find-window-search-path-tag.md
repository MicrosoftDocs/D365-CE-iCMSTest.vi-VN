---
title: FindWindow search path tag in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Thẻ <FindWindow> chứa một danh sách các yếu tố phù hợp bị loại trừ theo thứ tự danh sách của chúng bên trong thẻ. Chủ đề này mô tả các yếu tố <FindWindow> với mã ví dụ.
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
ms.assetid: 5aeb435d-5206-4cda-aa9e-db69aaa2f515
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
ms.openlocfilehash: 335821fbf96a7e989e4879d3cc260e9a0dc367fe
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386295"
---
# <a name="findwindow-search-path-tag-in-unified-service-desk"></a><span data-ttu-id="64eb7-104">FindWindow search path tag in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="64eb7-104">FindWindow search path tag in Unified Service Desk</span></span>
<span data-ttu-id="64eb7-105">Thẻ `<FindWindow>` chứa một danh sách các yếu tố phù hợp bị loại trừ theo thứ tự danh sách của chúng bên trong thẻ.</span><span class="sxs-lookup"><span data-stu-id="64eb7-105">`<FindWindow>` tag contains a list of matching elements that are executed in the order of their listing within the tag.</span></span> <span data-ttu-id="64eb7-106">Chủ đề này mô tả các yếu tố `<FindWindow>` với mã ví dụ.</span><span class="sxs-lookup"><span data-stu-id="64eb7-106">This topic describes the `<FindWindow>` elements with example code.</span></span>  
  
<a name="elements"></a>   
## <a name="findwindow-elements"></a><span data-ttu-id="64eb7-107">\<FindWindow> elements</span><span class="sxs-lookup"><span data-stu-id="64eb7-107">\<FindWindow> elements</span></span>  
 <span data-ttu-id="64eb7-108">Đoạn mã sau đây hiển thị các yếu tố trong thẻ `<FindWindow>`</span><span class="sxs-lookup"><span data-stu-id="64eb7-108">The following code snippet shows the elements in a `<FindWindow>` tag</span></span>  
  
```vb  
# RELAX NG XML grammar for FindWindow   
# http://relaxng.org/compact-tutorial-20030326.html   
#   
Grammar  
{   
start = FindWindow FindWindow = element   
FindWindow  
{   
  element ControlId { attribute match { xsd:integer }?, text }*  
& element Caption { attribute match { xsd:integer }?, text }*  
& element CaptionStartsWith { same as Caption }*  
& element CaptionEndsWith { same as Caption }*  
& element CaptionContains { same as Caption }*  
& element Class { attribute match { xsd:integer }?, text }*  
& element ClassStartsWith { same as Class }*  
& element ClassEndsWith { same as Class }*  
& element ClassContains { same as Class }*  
& element Position { xsd:integer, xsd:integer } *  
& element Find { Caption & Class }*  
& element Desktop { empty }*  
& element Application { empty }*  
& element Owner { empty }*  
& element RelaxProcessIdRestriction { empty }*  
& element RelaxThreadIdRestriction { empty }*  
}  
}  
  
```  
  
 <span data-ttu-id="64eb7-109">Bảng sau mô tả các yếu tố `<FindWinow>`.</span><span class="sxs-lookup"><span data-stu-id="64eb7-109">The following table describes the `<FindWinow>` elements.</span></span>  
  
|<span data-ttu-id="64eb7-110">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="64eb7-110">Element</span></span>|<span data-ttu-id="64eb7-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="64eb7-111">Description</span></span>|  
|-------------|-----------------|  
|`ControlId`|<span data-ttu-id="64eb7-112">Cửa sổ với ID</span><span class="sxs-lookup"><span data-stu-id="64eb7-112">Window with ID</span></span>|  
|`Caption`|<span data-ttu-id="64eb7-113">Văn bản chú thích cửa sổ.</span><span class="sxs-lookup"><span data-stu-id="64eb7-113">Window caption text.</span></span>|  
|`CaptionStartsWith`|<span data-ttu-id="64eb7-114">Chú thích bắt đầu bằng văn bản</span><span class="sxs-lookup"><span data-stu-id="64eb7-114">Caption starts with text</span></span>|  
|`CaptionEndsWith`|<span data-ttu-id="64eb7-115">Chú thích kết thúc bằng văn bản.</span><span class="sxs-lookup"><span data-stu-id="64eb7-115">Caption ends with text.</span></span>|  
|`CaptionContains`|<span data-ttu-id="64eb7-116">Chú thích có chứa văn bản.</span><span class="sxs-lookup"><span data-stu-id="64eb7-116">Caption contains text.</span></span>|  
|`Class`|<span data-ttu-id="64eb7-117">Cửa sổ với tên lớp</span><span class="sxs-lookup"><span data-stu-id="64eb7-117">Window with class name</span></span>|  
|`ClassStartsWith`|<span data-ttu-id="64eb7-118">Tên lớp bắt đầu bằng văn bản.</span><span class="sxs-lookup"><span data-stu-id="64eb7-118">Class name starts with text.</span></span>|  
|`ClassEndsWith`|<span data-ttu-id="64eb7-119">Tên lớp kết thúc bằng văn bản.</span><span class="sxs-lookup"><span data-stu-id="64eb7-119">Class name ends with text.</span></span>|  
|`ClassContains`|<span data-ttu-id="64eb7-120">Lớp có chứa văn bản.</span><span class="sxs-lookup"><span data-stu-id="64eb7-120">Class contains text.</span></span>|  
|`Position`|<span data-ttu-id="64eb7-121">Tìm kiếm một cửa sổ ở một vị trí đã chỉ định.</span><span class="sxs-lookup"><span data-stu-id="64eb7-121">Search for a window at a specified position.</span></span> <span data-ttu-id="64eb7-122">Vị trí được định nghĩa là ở góc trên bên trái của cửa sổ như tọa độ (x, y).</span><span class="sxs-lookup"><span data-stu-id="64eb7-122">The position is defined as the upper-left corner of the window as (x,y) coordinates.</span></span> <span data-ttu-id="64eb7-123">The position is calculated either from the \<Application/> (default) or from the \<Desktop/>.</span><span class="sxs-lookup"><span data-stu-id="64eb7-123">The position is calculated either from the \<Application/> (default) or from the \<Desktop/>.</span></span> <span data-ttu-id="64eb7-124">If \<Desktop/> is used, it must be specified before the \<Position> element.</span><span class="sxs-lookup"><span data-stu-id="64eb7-124">If \<Desktop/> is used, it must be specified before the \<Position> element.</span></span>|  
|<span data-ttu-id="64eb7-125">Find</span><span class="sxs-lookup"><span data-stu-id="64eb7-125">Find</span></span>|<span data-ttu-id="64eb7-126">Tìm kiếm cửa sổ được chỉ định qua yếu tố `Class` hoặc `Caption`.</span><span class="sxs-lookup"><span data-stu-id="64eb7-126">Search for a window as specified via the `Class` or `Caption` element.</span></span> <span data-ttu-id="64eb7-127">Các yếu tố tương tự như `FindWindow` có thể được sử dụng tại đây (`Caption`,  `CaptionStartsWith`,  `CaptionEndsWith`,  `CaptionContains`,  `Class`,  `ClassStartsWith`,  `ClassEndsWith` hoặc `ClassContains`).</span><span class="sxs-lookup"><span data-stu-id="64eb7-127">The same elements as for `FindWindow` can be used here (`Caption`,  `CaptionStartsWith`,  `CaptionEndsWith`,  `CaptionContains`,  `Class`,  `ClassStartsWith`,  `ClassEndsWith`, or `ClassContains`).</span></span>|  
|`Desktop`|<span data-ttu-id="64eb7-128">Đặt điểm tìm cho máy tính để bàn</span><span class="sxs-lookup"><span data-stu-id="64eb7-128">Sets the search point to the desktop</span></span>|  
|`Application`|<span data-ttu-id="64eb7-129">Đặt điểm tìm cho cửa sổ ứng dụng cấp cao nhất.</span><span class="sxs-lookup"><span data-stu-id="64eb7-129">Sets the search point to the application's top-level window.</span></span>|  
|`Owner`|<span data-ttu-id="64eb7-130">Cửa sổ với chủ sở hữu được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="64eb7-130">Window with a specified owner.</span></span>|  
|`RelaxProcessIdRestriction`|<span data-ttu-id="64eb7-131">Bao gồm các cửa sổ với các ID quá trình khác nhau trong tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="64eb7-131">Includes windows with different process IDs in the search.</span></span> <span data-ttu-id="64eb7-132">Theo mặc định, tất cả cửa sổ thuộc về cùng ID quá trình.</span><span class="sxs-lookup"><span data-stu-id="64eb7-132">By default, all windows belong to the same process ID.</span></span>|  
|`RelaxThreadIdRestriction`|<span data-ttu-id="64eb7-133">Bao gồm các cửa sổ với các ID chuỗi chủ đề khác nhau trong quá trình tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="64eb7-133">Includes windows with different thread IDs in the search process.</span></span> <span data-ttu-id="64eb7-134">Theo mặc định, tất cả cửa sổ thuộc về cùng ID chuỗi chủ đề.</span><span class="sxs-lookup"><span data-stu-id="64eb7-134">By default, all windows belong to the same thread ID.</span></span>|  
  
<a name="samplecode"></a>   
## <a name="sample-code"></a><span data-ttu-id="64eb7-135">Mã mẫu</span><span class="sxs-lookup"><span data-stu-id="64eb7-135">Sample code</span></span>  
 <span data-ttu-id="64eb7-136">Tập hợp mẫu sau cho biết cách sử dụng các thuộc tính khác nhau.</span><span class="sxs-lookup"><span data-stu-id="64eb7-136">The following set of samples show the how the various attributes are used.</span></span>  
  
```xml  
The following sample searches for a window with the control ID 1003.  
<FindWindow>  
<ControlID>1003</ControlID>  
</FindWindow>  
  
The following sample searches for a window with the class name SunAWTFrame.  
<FindWindow>  
<Class>SunAWTFrame</Class>  
</FindWindow>  
  
The following sample searches for a window at desktop position x200 y400.   
<FindWindow>  
<Desktop/>  
<Position>200,400</Position>  
</FindWindow>  
  
The following sample searches for the second application with the caption CurrencyConv that is not within the same process as the DDA loaded application.   
  
<FindWindow>  
<RelaxProcessIdRestriction/>  
<Caption match="2">CurrencyConv</Caption>  
</FindWindow>  
  
```  
  
### <a name="see-also"></a><span data-ttu-id="64eb7-137">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="64eb7-137">See also</span></span>  
 <span data-ttu-id="64eb7-138">[JavaDDA](../unified-service-desk/javadda.md) </span><span class="sxs-lookup"><span data-stu-id="64eb7-138">[JavaDDA](../unified-service-desk/javadda.md) </span></span>  
 [<span data-ttu-id="64eb7-139">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="64eb7-139">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
