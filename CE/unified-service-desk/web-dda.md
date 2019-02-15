---
title: WebDDA in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about using Web data-driven adapter (WebDDA) in Unified Service Desk.
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
ms.assetid: 230e530d-921a-4d26-aa92-7947bfbbd83f
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
ms.openlocfilehash: 20b4c02ce6180aa50dae4f5fe129f7d239f4d694
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385706"
---
# <a name="webdda"></a><span data-ttu-id="35a1e-103">WebDDA</span><span class="sxs-lookup"><span data-stu-id="35a1e-103">WebDDA</span></span>
<span data-ttu-id="35a1e-104">Bộ chuyển đổi định hướng dữ liệu web (WebDDA) cung cấp quyền truy cập vào các ứng dụng dựa trên HTML.</span><span class="sxs-lookup"><span data-stu-id="35a1e-104">The Web data-driven adapter (WebDDA) provides access to HTML-based applications.</span></span> <span data-ttu-id="35a1e-105">Công nghệ quan trọng được sử dụng trong DDA này là Mô hình Đối tượng Tài liệu (DOM) của trình duyệt.</span><span class="sxs-lookup"><span data-stu-id="35a1e-105">The key technology used in this DDA is the Document Object Model (DOM) of the browser.</span></span> <span data-ttu-id="35a1e-106">Các liên kết được tạo ra theo cách tương tự với liên kết cho WinDDA, bằng cách xác định yếu tố then chốt và đường dẫn, trong trường hợp này là DOM, tới yếu tố.</span><span class="sxs-lookup"><span data-stu-id="35a1e-106">The bindings are created in a way similar to those for the WinDDA, by defining a key element and the path-through, in this case the DOM, to the element.</span></span>  
  
 <span data-ttu-id="35a1e-107">Yếu tố liên kết WebDDA khác nhau như sau:</span><span class="sxs-lookup"><span data-stu-id="35a1e-107">The various WebDDA binding elements are as follows:</span></span>  
  
-   [<span data-ttu-id="35a1e-108">AnchorElement</span><span class="sxs-lookup"><span data-stu-id="35a1e-108">AnchorElement</span></span>](../unified-service-desk/anchor-element.md)  
  
-   [<span data-ttu-id="35a1e-109">ButtonElement</span><span class="sxs-lookup"><span data-stu-id="35a1e-109">ButtonElement</span></span>](../unified-service-desk/button-element.md)  
  
-   [<span data-ttu-id="35a1e-110">InputElement</span><span class="sxs-lookup"><span data-stu-id="35a1e-110">InputElement</span></span>](../unified-service-desk/input-element.md)  
  
-   [<span data-ttu-id="35a1e-111">SelectElement</span><span class="sxs-lookup"><span data-stu-id="35a1e-111">SelectElement</span></span>](../unified-service-desk/select-element.md)  
  
-   [<span data-ttu-id="35a1e-112">TextAreaElement</span><span class="sxs-lookup"><span data-stu-id="35a1e-112">TextAreaElement</span></span>](../unified-service-desk/text-area-element.md)  
  
-   [<span data-ttu-id="35a1e-113">HtmlElement</span><span class="sxs-lookup"><span data-stu-id="35a1e-113">HtmlElement</span></span>](../unified-service-desk/html-element.md)  
  
-   [<span data-ttu-id="35a1e-114">Siêu liên kết</span><span class="sxs-lookup"><span data-stu-id="35a1e-114">HyperLink</span></span>](../unified-service-desk/hyperlink.md)  
  
-   [<span data-ttu-id="35a1e-115">Tìm kiếm Yếu tố Đường dẫn</span><span class="sxs-lookup"><span data-stu-id="35a1e-115">Search Path Elements</span></span>](../unified-service-desk/search-path-elements.md)  
  
-   [<span data-ttu-id="35a1e-116">AttributeMatchPath</span><span class="sxs-lookup"><span data-stu-id="35a1e-116">AttributeMatchPath</span></span>](../unified-service-desk/attribute-match-path.md)  
  
-   [<span data-ttu-id="35a1e-117">ElementMatchPath</span><span class="sxs-lookup"><span data-stu-id="35a1e-117">ElementMatchPath</span></span>](../unified-service-desk/element-match-path.md)  
  
-   [<span data-ttu-id="35a1e-118">FindIEFrame</span><span class="sxs-lookup"><span data-stu-id="35a1e-118">FindIEFrame</span></span>](../unified-service-desk/find-ie-frame.md)  
  
-   [<span data-ttu-id="35a1e-119">Sự kiện WebDDA</span><span class="sxs-lookup"><span data-stu-id="35a1e-119">WebDDA Events</span></span>](../unified-service-desk/web-dda-events.md)  
  
### <a name="see-also"></a><span data-ttu-id="35a1e-120">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="35a1e-120">See also</span></span>  
 <span data-ttu-id="35a1e-121">[Use Data Driven Adapters](../unified-service-desk/use-data-driven-adapters-ddas.md) </span><span class="sxs-lookup"><span data-stu-id="35a1e-121">[Use Data Driven Adapters](../unified-service-desk/use-data-driven-adapters-ddas.md) </span></span>  
 <span data-ttu-id="35a1e-122">[WinDDA](../unified-service-desk/windda.md) </span><span class="sxs-lookup"><span data-stu-id="35a1e-122">[WinDDA](../unified-service-desk/windda.md) </span></span>  
 <span data-ttu-id="35a1e-123">[UIADDA](../unified-service-desk/uiadda.md) </span><span class="sxs-lookup"><span data-stu-id="35a1e-123">[UIADDA](../unified-service-desk/uiadda.md) </span></span>  
 [<span data-ttu-id="35a1e-124">JavaDDA</span><span class="sxs-lookup"><span data-stu-id="35a1e-124">JavaDDA</span></span>](../unified-service-desk/javadda.md)
