---
title: Next Tag (WinDDA) in Unified Service Desk for Dynamics 365 for Customer Engagement apps Customer Enagagement| MicrosoftDocs
description: The topic describes the attributes of the Next tag (winDDA).
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
ms.assetid: 4369bd08-3009-47cd-be60-20bed9df50fc
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
ms.openlocfilehash: e282769e56fe42f6b4a23ecd71d86d9e00d722dc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387103"
---
# <a name="next-tag-windda-in-unified-service-desk"></a><span data-ttu-id="0ccc8-103">Next Tag (WinDDA) in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="0ccc8-103">Next Tag (WinDDA) in Unified Service Desk</span></span>
<span data-ttu-id="0ccc8-104">Thẻ `<Next/>` có thể bao gồm thuộc tính `match` tùy chọn và thuộc tính `offset` tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-104">`<Next/>` tag can include an optional `match` attribute and an optional `offset` attribute.</span></span> <span data-ttu-id="0ccc8-105">Thuộc tính `match` có giá trị mặc định là `"1"` và thuộc tính bù có giá trị mặc định là `"0"`.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-105">The `match` attribute has a default value of `"1"`, and the offset attribute has a default value of `"0"`.</span></span> <span data-ttu-id="0ccc8-106">Mỗi yếu tố `<Next/>` truy xuất mức độ tiếp theo của hệ thống cấp bậc [IAccessible](https://msdn.microsoft.com/library/accessibility.iaccessible\(v=vs.110\).aspx) và quét để có kết quả phù hợp giữa văn bản bên trong và `Name` của mỗi nút `IAccessible`.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-106">Each `<Next/>` element retrieves the next level of the [IAccessible](https://msdn.microsoft.com/library/accessibility.iaccessible\(v=vs.110\).aspx) hierarchy and scans it for a match between the inner text and the `Name` of each `IAccessible` node.</span></span> <span data-ttu-id="0ccc8-107">Chủ đề này mô tả các thuộc tính của thẻ `Next`.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-107">This topic describes the attributes of the `Next` tag.</span></span>  
  
## <a name="attributes-of-next"></a><span data-ttu-id="0ccc8-108">Attributes of \<Next></span><span class="sxs-lookup"><span data-stu-id="0ccc8-108">Attributes of \<Next></span></span>  
  
- <span data-ttu-id="0ccc8-109">`Match` – Trả về thuộc tính phù hợp thứ nth.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-109">`Match` – Returns the nth matching attribute.</span></span>  
  
- <span data-ttu-id="0ccc8-110">`Offset` – Trả lại thuộc tính nth sau thuộc tính phù hợp.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-110">`Offset` – Returns the nth attribute after the matching attribute.</span></span>  
  
- <span data-ttu-id="0ccc8-111">`Culture` – Sử dụng thẻ `culture`.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-111">`Culture` – Uses the `culture` tag.</span></span>  
  
  <span data-ttu-id="0ccc8-112">The `match="2"` attribute specifies how many times a text match has to occur for the criteria to be satisfied.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-112">The `match="2"` attribute specifies how many times a text match has to occur for the criteria to be satisfied.</span></span> <span data-ttu-id="0ccc8-113">Khi đạt đến con số này, các thuộc tính `offset` có thể được sử dụng để chọn một nút liền kề `IAccessible` với các nút được kết hợp thành công.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-113">When this number is reached, the `offset` attribute can be used to select an `IAccessible` node adjacent to the node that was successfully matched.</span></span> <span data-ttu-id="0ccc8-114">Giá trị bù đắp được bao quanh, do đó không thể tham chiếu bên ngoài dãy `IAccessible` con.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-114">The offset value wraps around, so it is not possible to reference outside of the child `IAccessible` array.</span></span> <span data-ttu-id="0ccc8-115">Thẻ văn hóa cho phép bạn tìm kiếm các thuộc tính dành riêng cho ngôn ngữ để hiển thị trong ví dụ sau:</span><span class="sxs-lookup"><span data-stu-id="0ccc8-115">The culture tag allows you to search for language-specific attributes as shown in the following example:</span></span>  
  
```xml  
<AccControl name="closeButton">  
<Path>  
<Next culture="en-us">Close</Next>  
<Next culture="de-de">Beenden</Next>  
<Next culture="fr-fr">Fermer</Next>  
</Path>  
</AccControl>  
  
```  
  
 <span data-ttu-id="0ccc8-116">Mẫu sau tìm kiếm kiểm soát ở hai vị trí sau kiểm soát thứ tư với chú thích `Name`.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-116">The following sample searches for the control that is two positions after the fourth control with the caption `Name`.</span></span>  
  
```xml  
<AccControl name="NameBox">  
<Path>  
<Next match="4", offset="4">Name</Next>  
</Path>  
</AccControl>  
  
```  
  
### <a name="see-also"></a><span data-ttu-id="0ccc8-117">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="0ccc8-117">See also</span></span>  
 <span data-ttu-id="0ccc8-118">[Win DDA](../unified-service-desk/windda.md) </span><span class="sxs-lookup"><span data-stu-id="0ccc8-118">[Win DDA](../unified-service-desk/windda.md) </span></span>  
 [<span data-ttu-id="0ccc8-119">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="0ccc8-119">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
