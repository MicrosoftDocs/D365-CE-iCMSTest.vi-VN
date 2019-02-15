---
title: Next Tag in Unified Service Desk for Dynamics 365 for Customer Engagement apps Customer Enagagement| MicrosoftDocs
description: The topic describes the attributes of <Next> tag. Bạn có thể sử dụng yếu tố <Next> để đặt con trỏ tìm kiếm vào yếu tố UI tiếp theo với chú thích phù hợp. Nếu bạn sử dụng <Next/>, tìm kiếm sẽ điều hướng đến nút tiếp theo bên trong cây.
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
ms.assetid: a8eefb0b-4ad3-4d98-aed2-0373187fd2e0
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
ms.openlocfilehash: 041b434b317068633d52ac9ed09ec9d6f5c4151d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386113"
---
# <a name="next-tag-in-unified-service-desk"></a><span data-ttu-id="9013d-105">Next Tag in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="9013d-105">Next Tag in Unified Service Desk</span></span>
<span data-ttu-id="9013d-106">Bạn có thể sử dụng yếu tố `<Next>` để đặt con trỏ tìm kiếm vào yếu tố UI tiếp theo với chú thích phù hợp.</span><span class="sxs-lookup"><span data-stu-id="9013d-106">You can use the `<Next>` element to set the search pointer to the next UI element with the matching caption.</span></span> <span data-ttu-id="9013d-107">Nếu bạn sử dụng `<Next/>`, tìm kiếm sẽ điều hướng đến nút tiếp theo bên trong cây.</span><span class="sxs-lookup"><span data-stu-id="9013d-107">If you use `<Next/>`, the search navigates to the next node within the tree.</span></span> <span data-ttu-id="9013d-108">The `<Next/>` tag navigates down the tree branches, not among siblings within one node of the tree.</span><span class="sxs-lookup"><span data-stu-id="9013d-108">The `<Next/>` tag navigates down the tree branches, not among siblings within one node of the tree.</span></span> <span data-ttu-id="9013d-109">Để điều hướng bên trong nút cây, hãy sử dụng thuộc tính `match` và `offset`.</span><span class="sxs-lookup"><span data-stu-id="9013d-109">To navigate within the tree node, use the `match` and `offset` attributes.</span></span> <span data-ttu-id="9013d-110">Chủ đề này mô tả các thuộc tính của thẻ `<Next>`.</span><span class="sxs-lookup"><span data-stu-id="9013d-110">This topic describes the attributes of `<Next>` tag.</span></span>  
  
## <a name="attributes-of-next-tag"></a><span data-ttu-id="9013d-111">Attributes of \<Next> tag</span><span class="sxs-lookup"><span data-stu-id="9013d-111">Attributes of \<Next> tag</span></span>  
 <span data-ttu-id="9013d-112">Bảng sau mô tả các thuộc tính của thẻ `<Next>`.</span><span class="sxs-lookup"><span data-stu-id="9013d-112">The following table describes the attributes of the `<Next>` tag.</span></span>  
  
|<span data-ttu-id="9013d-113">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="9013d-113">Attribute</span></span>|<span data-ttu-id="9013d-114">Mô tả</span><span class="sxs-lookup"><span data-stu-id="9013d-114">Description</span></span>|  
|---------------|-----------------|  
|`Match`|<span data-ttu-id="9013d-115">Yếu tố **thứ n**</span><span class="sxs-lookup"><span data-stu-id="9013d-115">**Nth** element</span></span>|  
|`Offset`|<span data-ttu-id="9013d-116">Yếu tố thứ **N** sau một yếu tố phù hợp.</span><span class="sxs-lookup"><span data-stu-id="9013d-116">**Nth** element after the one that matched.</span></span>|  
|`Culture`|<span data-ttu-id="9013d-117">Sử dụng văn hóa</span><span class="sxs-lookup"><span data-stu-id="9013d-117">Use culture</span></span>|  
  
 <span data-ttu-id="9013d-118">Liên kết mẫu sau tìm nút `Close` trong một ứng dụng cho ba nền văn hóa khác nhau: Anh, Đức và Pháp:</span><span class="sxs-lookup"><span data-stu-id="9013d-118">The following sample binding searches for the `Close` button in an application for three different cultures: English, German, and French:</span></span>  
  
```xml  
<Controls>  
<JAccControl name="CloseButton">  
<Path>  
<FindWindow>  
<Class>SunAWTFrame</Class>  
</FindWindow>  
<Next culture="en-us">Close</Next>  
<Next culture="de-de">Beenden</Next>  
<Next culture="fr-fr">Fermer</Next>  
</Path>  
</JAccControl>  
</Controls>  
  
```  
  
 <span data-ttu-id="9013d-119">Bằng cách sử dụng các thuộc tính `match` và `offset`, bạn có thể điều hướng cây khả năng tiếp cận cho các nút có cùng tên (sử dụng `match`) hoặc không có thông tin nhận dạng (bằng `offset`).</span><span class="sxs-lookup"><span data-stu-id="9013d-119">By using the attributes `match` and `offset`, you can navigate the accessibility tree for nodes with the same name (using `match`) or without an identifier (using `offset`).</span></span> <span data-ttu-id="9013d-120">Mẫu sau chọn mục nhập cây khả năng tiếp cận thứ hai sau mục nhập thứ tư với chú thích `Name`.</span><span class="sxs-lookup"><span data-stu-id="9013d-120">The following sample selects the second accessibility tree entry after the forth entry with the caption `Name`.</span></span>  
  
```xml  
<JAccControl name="TestButton">  
<Path>  
<Next match="4", offset="2" >Name</Next>  
</Path>  
</JAccControl>  
  
```  
  
> [!NOTE]
>  <span data-ttu-id="9013d-121">Các thẻ `<Next/>` và `<NextName/>` có cùng chức năng.</span><span class="sxs-lookup"><span data-stu-id="9013d-121">The `<Next/>` and `<NextName/>` tags have the same function.</span></span> <span data-ttu-id="9013d-122">Khi chỉ định liên kết của bạn, hãy sử dụng thẻ `<Next>` để chuyển tiếp tương thích.</span><span class="sxs-lookup"><span data-stu-id="9013d-122">When specifying your bindings, use the `<Next>` tag to be forward compatible.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="9013d-123">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9013d-123">See also</span></span>  
 <span data-ttu-id="9013d-124">[JavaDDA](../unified-service-desk/javadda.md) </span><span class="sxs-lookup"><span data-stu-id="9013d-124">[JavaDDA](../unified-service-desk/javadda.md) </span></span>  
 [<span data-ttu-id="9013d-125">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="9013d-125">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
