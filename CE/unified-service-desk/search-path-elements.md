---
title: Search Path Elements in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about Search Path Elements in Unified Service Desk.
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
ms.assetid: 6b9e70b9-20a1-430c-9cf0-bb8ca7b2480d
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
ms.openlocfilehash: 6236241d78c26e8a82a21f14ab01c34888d29ff2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387819"
---
# <a name="search-path-elements-in-unified-service-desk"></a><span data-ttu-id="c943c-103">Search Path Elements in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="c943c-103">Search Path Elements in Unified Service Desk</span></span>
<span data-ttu-id="c943c-104">Ứng dụng web và các trang web có thể chứa khung.</span><span class="sxs-lookup"><span data-stu-id="c943c-104">Web applications and web pages can contain frames.</span></span> <span data-ttu-id="c943c-105">Các khung có thể có các kiểm soát được liên kết.</span><span class="sxs-lookup"><span data-stu-id="c943c-105">The frames can have associated controls.</span></span> <span data-ttu-id="c943c-106">Bạn cũng có thể đặt cấu hình kiểm soát bộ chuyển đổi định hướng dữ liệu (DDA) cho các kiểm soát dựa trên khung.</span><span class="sxs-lookup"><span data-stu-id="c943c-106">You can also configure data-driven adapter (DDA) controls for frame-based controls.</span></span> <span data-ttu-id="c943c-107">Ví dụ: bạn có thể cần truy cập các kiểm soát biểu mẫu `HTML` bên trong khung.</span><span class="sxs-lookup"><span data-stu-id="c943c-107">For example, you might need to access the `HTML` form controls inside a frame.</span></span> <span data-ttu-id="c943c-108">Để làm điều này, bạn sẽ tìm kiếm một khung cụ thể bên trong cửa sổ cho dữ liệu cụ thể.</span><span class="sxs-lookup"><span data-stu-id="c943c-108">To do this, you would search a specific frame within a window for specific data.</span></span> <span data-ttu-id="c943c-109">Bạn có thể bao gồm tìm kiếm đó trong chính WebDDA.</span><span class="sxs-lookup"><span data-stu-id="c943c-109">You can include that search in the WebDDA itself.</span></span>  
  
## <a name="search-path-elements"></a><span data-ttu-id="c943c-110">Tìm kiếm yếu tố đường dẫn</span><span class="sxs-lookup"><span data-stu-id="c943c-110">Search path elements</span></span>  
 <span data-ttu-id="c943c-111">WebDDA xác định ba yếu tố có thể được sử dụng trong đường dẫn tìm kiếm cho một kiểm soát nhất định:</span><span class="sxs-lookup"><span data-stu-id="c943c-111">The WebDDA defines three elements that can be used in the search path for a given control:</span></span>  
  
- [<span data-ttu-id="c943c-112">AttributeMatchPath</span><span class="sxs-lookup"><span data-stu-id="c943c-112">AttributeMatchPath</span></span>](../unified-service-desk/attribute-match-path.md)  
  
- [<span data-ttu-id="c943c-113">ElementMatchPath</span><span class="sxs-lookup"><span data-stu-id="c943c-113">ElementMatchPath</span></span>](../unified-service-desk/element-match-path.md)  
  
- [<span data-ttu-id="c943c-114">FindIEFrame</span><span class="sxs-lookup"><span data-stu-id="c943c-114">FindIEFrame</span></span>](../unified-service-desk/find-ie-frame.md)  
  
  <span data-ttu-id="c943c-115">Một đường dẫn tìm kiếm của kiểm soát có thể chứa nhiều yếu tố.</span><span class="sxs-lookup"><span data-stu-id="c943c-115">A control's search path can contain multiple elements.</span></span> <span data-ttu-id="c943c-116">Chúng sẽ được thực thi theo thứ tự được liệt kê trong đường dẫn tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="c943c-116">They will be executed in the order in that they are listed in the search path.</span></span> <span data-ttu-id="c943c-117">Ví dụ: mô tả kiểm soát sau trước tiên tìm một cửa sổ [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] được mô tả với yếu tố `<FindIEFrame/>` và sau đó sử dụng yếu tố `<ElementMatchPath/>` để xác định kiểm soát mong muốn trong cửa sổ [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] này.</span><span class="sxs-lookup"><span data-stu-id="c943c-117">For example, the following control description first looks for an [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] window described with the `<FindIEFrame/>` element, and then it uses the `<ElementMatchPath/>` element to identify the desired control within this [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] window.</span></span>  
  
```xml  
<HtmlElement name="Popup Text1" type="HtmlElement">  
<FindIEFrame matchtype="endswith">Popup - Windows Internet Explorer</FindIEFrame>  
<ElementMatchPath>/HTML/BODY/P/FONT</ElementMatchPath>  
</HtmlElement>  
  
```  
  
### <a name="see-also"></a><span data-ttu-id="c943c-118">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c943c-118">See also</span></span>  
 <span data-ttu-id="c943c-119">[WebDDA](../unified-service-desk/web-dda.md) </span><span class="sxs-lookup"><span data-stu-id="c943c-119">[WebDDA](../unified-service-desk/web-dda.md) </span></span>  
 [<span data-ttu-id="c943c-120">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="c943c-120">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
