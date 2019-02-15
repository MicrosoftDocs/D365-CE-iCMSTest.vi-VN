---
title: FindIEFrame in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The topic describes the attributes of <FindIEFrame> that searches for an application by its caption and selects a DOM of the window or a specific frame within a window.
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
ms.assetid: fc973cc7-d4af-4bdb-813a-4204ac46f939
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
ms.openlocfilehash: b5ac613ecf30dd0ecca8614f6683f6b887ca582b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387957"
---
# <a name="findieframe-in-unified-service-desk"></a><span data-ttu-id="aa0a5-103">FindIEFrame in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="aa0a5-103">FindIEFrame in Unified Service Desk</span></span>
<span data-ttu-id="aa0a5-104">Thẻ `<FindIEFrame>` tìm kiếm ứng dụng bằng chú thích của ứng dụng và chọn `DOM` của cửa sổ hoặc khung cụ thể bên trong cửa sổ.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-104">`<FindIEFrame>` tag searches for an application by its caption and selects a `DOM` of the window or a specific frame within a window.</span></span> <span data-ttu-id="aa0a5-105">Một ví dụ là một cửa sổ bật lên.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-105">An example is a pop-up window.</span></span> <span data-ttu-id="aa0a5-106">Thẻ này có thể khám phá cửa sổ bật lên bất kể nó có liên quan gì đến ứng dụng web được lưu trữ không.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-106">This tag can explore the pop-up window regardless of how it stands in relation to the hosted web application.</span></span> <span data-ttu-id="aa0a5-107">Chủ đề này mô tả các thuộc tính của `<FindIEFrame>`</span><span class="sxs-lookup"><span data-stu-id="aa0a5-107">This topic describes the attributes of `<FindIEFrame>`</span></span>  
  
## <a name="findieframe-syntax"></a><span data-ttu-id="aa0a5-108">\<FindIEFrame> syntax</span><span class="sxs-lookup"><span data-stu-id="aa0a5-108">\<FindIEFrame> syntax</span></span>  
 <span data-ttu-id="aa0a5-109">Đoạn mã sau hiển thị cách sử dụng `<FindIEFrame>`:</span><span class="sxs-lookup"><span data-stu-id="aa0a5-109">The following code snippet shows how `<FindIEFrame>` is used:</span></span>  
  
```xml  
<FindIEFrame> [matchtype="equals|startswith|endswith|contains"] [match="n"][relaxProcessIdRestriction="true|false"] >  
text to match against window caption  
</FindIEFrame>  
  
```  
  
## <a name="attributes-of-findieframe"></a><span data-ttu-id="aa0a5-110">Attributes of \<FindIEFrame></span><span class="sxs-lookup"><span data-stu-id="aa0a5-110">Attributes of \<FindIEFrame></span></span>  
 <span data-ttu-id="aa0a5-111">Bảng sau mô tả các thuộc tính tùy chọn của thẻ `<FindIEFrame>`.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-111">The following table describes the optional attributes of the `<FindIEFrame>` tag.</span></span>  
  
|<span data-ttu-id="aa0a5-112">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="aa0a5-112">Element</span></span>|<span data-ttu-id="aa0a5-113">Mô tả</span><span class="sxs-lookup"><span data-stu-id="aa0a5-113">Description</span></span>|  
|-------------|-----------------|  
|`matchtype`|<span data-ttu-id="aa0a5-114">Chỉ định cách kết hợp chú thích.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-114">Specifies how the caption should be matched.</span></span> <span data-ttu-id="aa0a5-115">Các giá trị có thể là `equals`, `startswith`, `endswith` hoặc `contains`.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-115">Possible values are `equals`, `startswith`, `endswith`, or `contains`.</span></span> <span data-ttu-id="aa0a5-116">Bất kỳ giá trị nào khác sẽ đặt một ngoại lệ.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-116">Any other value will throw an exception.</span></span>|  
|`match`|<span data-ttu-id="aa0a5-117">Chọn khung **thứ n** phù hợp với đặc điểm kỹ thuật.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-117">Selects the **nth** frame matching the specification.</span></span> <span data-ttu-id="aa0a5-118">Mặc định: **1**.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-118">Default: **1**.</span></span>|  
|`relaxProcessIdRestriction`|<span data-ttu-id="aa0a5-119">Tìm kiếm cửa sổ/khung phù hợp trong quá trình ứng dụng được lưu trữ (`False`) hoặc tìm kiếm qua tất cả quá trình (`True`).</span><span class="sxs-lookup"><span data-stu-id="aa0a5-119">Searches for a matching window/frame within the same process of the hosted application (`False`) or searches over all processes (`True`).</span></span>|  
  
 <span data-ttu-id="aa0a5-120">Mẫu mã sau đây hiển thị các liên kết cho kiểm soát có tên `PopupWindowText`.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-120">The following sample code shows the bindings for the control named `PopupWindowText`.</span></span> <span data-ttu-id="aa0a5-121">Kiểm soát trong văn bản là một cửa sổ bật lên `HTML`; trong trường hợp này, đó là cửa sổ bật lên trong **Ứng dụng Web Mẫu**.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-121">The control is the text in an `HTML` pop-up window; in this case, it is the pop-up window in the **Sample Web Application**.</span></span>  
  
```xml  
<HtmlElement name="PopupWindowText" type="HtmlElement">  
<FindIEFrame>http://uiiserver1/Microsoft.Cti.Samples.DemoWebApplication/popup1.htm - Windows Internet Explorer</FindIEFrame>  
<ElementMatchPath>/HTML/BODY/P/FONT</ElementMatchPath>  
</HtmlElement>  
  
```  
  
### <a name="see-also"></a><span data-ttu-id="aa0a5-122">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="aa0a5-122">See also</span></span>  
 <span data-ttu-id="aa0a5-123">[WebDDA](../unified-service-desk/web-dda.md) </span><span class="sxs-lookup"><span data-stu-id="aa0a5-123">[WebDDA](../unified-service-desk/web-dda.md) </span></span>  
 [<span data-ttu-id="aa0a5-124">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="aa0a5-124">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
