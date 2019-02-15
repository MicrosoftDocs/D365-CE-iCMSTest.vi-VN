---
title: HyperLink in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
descrition: The <HyperLink> element does not define an element on the web application's user interface (UI), but it allows navigating to a specified URL. This element does not use the DOM tree to navigate. It only takes the <Url> tag to specify the target URL.
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
ms.assetid: 9fcb4f35-b9ef-412d-a62e-c4dc3f2e65cb
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
ms.openlocfilehash: 508a7475c29cef5a6d94c43e0470560341338a6e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387727"
---
# <a name="hyperlink-in-unified-service-desk"></a><span data-ttu-id="24f60-102">HyperLink in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="24f60-102">HyperLink in Unified Service Desk</span></span>
<span data-ttu-id="24f60-103">Yếu tố `<HyperLink>` không xác định một yếu tố trên giao diện người dùng (UI) của ứng dụng web nhưng yếu tố này cho phép điều hướng đến URL cụ thể.</span><span class="sxs-lookup"><span data-stu-id="24f60-103">The `<HyperLink>` element does not define an element on the web application's user interface (UI), but it allows navigating to a specified URL.</span></span> <span data-ttu-id="24f60-104">Yếu tố này không sử dụng cây `DOM` để điều hướng.</span><span class="sxs-lookup"><span data-stu-id="24f60-104">This element does not use the `DOM` tree to navigate.</span></span> <span data-ttu-id="24f60-105">Yếu tố này chỉ lấy thẻ `<Url>` để chỉ định URL mục tiêu, như được hiển thị trong ví dụ sau:</span><span class="sxs-lookup"><span data-stu-id="24f60-105">It only takes the `<Url>` tag to specify the target URL, as shown in the following example:</span></span>  
  
```xml  
<HyperLink name="control name">  
<Url>http://www.urlgoeshere.org</Url>  
</HyperLink>  
  
```  
  
### <a name="see-also"></a><span data-ttu-id="24f60-106">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="24f60-106">See also</span></span>  
 <span data-ttu-id="24f60-107">[WebDDA](../unified-service-desk/web-dda.md) </span><span class="sxs-lookup"><span data-stu-id="24f60-107">[WebDDA](../unified-service-desk/web-dda.md) </span></span>  
 [<span data-ttu-id="24f60-108">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="24f60-108">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
