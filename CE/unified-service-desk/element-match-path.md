---
title: ElementMatchPath in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: '<ElementMatchPath> tag uses a sequence of HTML tags delimited by forward slashes. Chủ đề này mô tả cách hoạt động của <ElementMatchPath>. '
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
ms.assetid: 2db66e85-cba1-4a37-bfbf-2190966295af
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
ms.openlocfilehash: d349876f4451ef57f0bda0a0e6ac3d215a4579cc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385470"
---
# <a name="elementmatchpath-in-unified-service-desk"></a><span data-ttu-id="1f3c4-104">ElementMatchPath in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="1f3c4-104">ElementMatchPath in Unified Service Desk</span></span>
<span data-ttu-id="1f3c4-105">Thẻ `<ElementMatchPath>` sử dụng chuỗi các thẻ `HTML` được phân tách bởi gạch chéo.</span><span class="sxs-lookup"><span data-stu-id="1f3c4-105">`<ElementMatchPath>` tag uses a sequence of `HTML` tags delimited by forward slashes.</span></span> <span data-ttu-id="1f3c4-106">Chủ đề này mô tả cách hoạt động của `<ElementMatchPath>`.</span><span class="sxs-lookup"><span data-stu-id="1f3c4-106">This topic describes how `<ElementMatchPath>` works.</span></span>  
  
## <a name="elementmatchpath-syntax"></a><span data-ttu-id="1f3c4-107">\<ElementMatchPath> syntax</span><span class="sxs-lookup"><span data-stu-id="1f3c4-107">\<ElementMatchPath> syntax</span></span>  
 <span data-ttu-id="1f3c4-108">Đoạn mã sau hiển thị cách sử dụng `<ElementMatchPath>`:</span><span class="sxs-lookup"><span data-stu-id="1f3c4-108">The following code snippet shows how `<ElementMatchPath>` is used:</span></span>  
  
```xml  
<html >  
<head>  
    <title>Sample</title>  
</head>  
<body>  
    <form id="HAT form">  
        <p>HAT</p>  
        <p><input id="CB1" type="checkbox" />Customer Care Framework</p>  
    </form>  
</body>  
</html>  
  
```  
  
 <span data-ttu-id="1f3c4-109">Đường dẫn kết nối cho `checkbox` như sau:</span><span class="sxs-lookup"><span data-stu-id="1f3c4-109">The bindings path for `checkbox` is as follows:</span></span>  
  
```xml  
<ElementMatchPath>/html/body/form/p[1]/input</ElementMatchPath>  
  
```  
  
 <span data-ttu-id="1f3c4-110">Trình tự này theo dõi đường dẫn điều hướng từ gốc của `DOM` tới yếu tố mục tiêu, yếu tố cuối cùng trong danh sách.</span><span class="sxs-lookup"><span data-stu-id="1f3c4-110">This sequence traces a navigation path from the root of the `DOM` to the target element, the last element in the list.</span></span> <span data-ttu-id="1f3c4-111">Mỗi thẻ kế tiếp biểu thị con của thẻ cha mẹ trước.</span><span class="sxs-lookup"><span data-stu-id="1f3c4-111">Each successive tag represents the child of the previous parent tag.</span></span> <span data-ttu-id="1f3c4-112">Các thẻ `HTML` có thể có hạn định số, tùy chọn có dạng *[n]*, trong đó *n* là một số nguyên.</span><span class="sxs-lookup"><span data-stu-id="1f3c4-112">The `HTML` tags can have an optional, numerical qualifier that takes the form *[n]*, where *n* is an integer.</span></span> <span data-ttu-id="1f3c4-113">Hạn định `[0]` là mặt định khi không có giá trị nào được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="1f3c4-113">The qualifier `[0]` is the default when none is specified.</span></span> <span data-ttu-id="1f3c4-114">The qualifier *[1]* represents the second matching sibling at that `DOM` level, and so on.</span><span class="sxs-lookup"><span data-stu-id="1f3c4-114">The qualifier *[1]* represents the second matching sibling at that `DOM` level, and so on.</span></span> <span data-ttu-id="1f3c4-115">Hạn định đặc biệt `[-1]` biểu thị cho cặp phù hợp cuối cùng tại cấp độ `DOM` bất kể độ dài của danh sách.</span><span class="sxs-lookup"><span data-stu-id="1f3c4-115">The special qualifier `[-1]` represents the last matching sibling at that `DOM` level regardless of the length of the list.</span></span> <span data-ttu-id="1f3c4-116">Trong ví dụ trên, thẻ `<p>` thứ hai trong thẻ `<form>` được sử dụng làm gốc cho nút con tiếp theo trong cây `DOM`.</span><span class="sxs-lookup"><span data-stu-id="1f3c4-116">In the above example, the second `<p>` tag in the `<form>` tag is used as the root for the next child node in the `DOM` tree.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="1f3c4-117">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1f3c4-117">See also</span></span>  
 <span data-ttu-id="1f3c4-118">[WebDDA](../unified-service-desk/web-dda.md) </span><span class="sxs-lookup"><span data-stu-id="1f3c4-118">[WebDDA](../unified-service-desk/web-dda.md) </span></span>  
 [<span data-ttu-id="1f3c4-119">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="1f3c4-119">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
