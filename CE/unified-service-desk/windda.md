---
title: WinDDA in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn how to use Windows data-driven adapter (WinDDA) in Unified Service Desk.
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
ms.assetid: 2fe35fec-6805-4a3c-aeea-7c2192847a3a
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
ms.openlocfilehash: 8b5d339cfee15129f416aa54b751a33f5d364e75
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387738"
---
# <a name="windda"></a><span data-ttu-id="0d0c5-103">WinDDA</span><span class="sxs-lookup"><span data-stu-id="0d0c5-103">WinDDA</span></span>
<span data-ttu-id="0d0c5-104">Bộ chuyển đổi định hướng dữ liệu [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] (WinDDA) được sử dụng để tương tác với các ứng dụng dựa trên Windows.</span><span class="sxs-lookup"><span data-stu-id="0d0c5-104">[!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] data-driven adapter (WinDDA) is used to interact with Windows-based applications.</span></span> <span data-ttu-id="0d0c5-105">Công nghệ quan trọng được sử dụng trong DDA là Microsoft Active Accessibility (MSAA), với một số chức năng được bao gồm qua cuộc gọi chức năng Win32.</span><span class="sxs-lookup"><span data-stu-id="0d0c5-105">The key technology used in the DDA is Microsoft Active Accessibility (MSAA), with some functionality covered through Win32 function calls.</span></span> <span data-ttu-id="0d0c5-106">MSAA API cho phép bạn tự động hóa giao diện người dùng.</span><span class="sxs-lookup"><span data-stu-id="0d0c5-106">The MSAA API allows you to automate the user interface.</span></span> <span data-ttu-id="0d0c5-107">Một ứng dụng có thể sử dụng API này để làm cho giao diện dễ tiếp cận hơn cho người sử dụng với khả năng tiếp cận vấn đề.</span><span class="sxs-lookup"><span data-stu-id="0d0c5-107">An application can use this API to make its interface more accessible to users with accessibility issues.</span></span> <span data-ttu-id="0d0c5-108">Mặc dù việc sửa đổi giao diện người dùng (UI) làm cho giao diện dễ tiếp cận với người dùng hơn là mục đích chính của API, UI cũng có thể được sử dụng để tích hợp [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)].</span><span class="sxs-lookup"><span data-stu-id="0d0c5-108">Although modifying a user interface (UI) to make it more accessible to users is the primary intent of the API, it can also be used for [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] integration.</span></span> <span data-ttu-id="0d0c5-109">Windows tạo ra đối tượng proxy tiếp cận cho các kiểm soát Windows không cung cấp rõ ràng hỗ trợ MSAA của riêng họ.</span><span class="sxs-lookup"><span data-stu-id="0d0c5-109">Windows generates accessibility proxy objects for Windows controls that don’t explicitly provide their own MSAA support.</span></span> <span data-ttu-id="0d0c5-110">Việc sử dụng đối tượng proxy cung cấp phương án thay thế cho phương pháp tiếp cận phổ biến hơn của việc kiểm soát ứng dụng thông qua cuộc gọi Windows API.</span><span class="sxs-lookup"><span data-stu-id="0d0c5-110">The use of proxy objects provides an alternative to the more common approach of controlling an application through Windows API calls.</span></span> <span data-ttu-id="0d0c5-111">Nó cũng cho phép bạn kiểm soát bất kỳ loại ứng dụng (ngoài Win32) cho thấy nhiều giao diện người dùng thông qua MSAA.</span><span class="sxs-lookup"><span data-stu-id="0d0c5-111">It also allows you to control any application type (beyond Win32) that exposes its user interface through MSAA.</span></span>  
  
## <a name="windda-tags-and-events"></a><span data-ttu-id="0d0c5-112">Thẻ và sự kiện WinDDA</span><span class="sxs-lookup"><span data-stu-id="0d0c5-112">WinDDA tags and events</span></span>  
 <span data-ttu-id="0d0c5-113">WinDDA bao gồm các thẻ sau đây được sử dụng để xác định một điều khiển:</span><span class="sxs-lookup"><span data-stu-id="0d0c5-113">The WinDDA consists of the following tags that are used to define a control:</span></span>  
  
- [<span data-ttu-id="0d0c5-114">Thẻ AccControl</span><span class="sxs-lookup"><span data-stu-id="0d0c5-114">AccControl Tag</span></span>](../unified-service-desk/acccontrol-tag.md)  
  
- [<span data-ttu-id="0d0c5-115">Thẻ ACCSelector</span><span class="sxs-lookup"><span data-stu-id="0d0c5-115">ACCSelector Tag</span></span>](../unified-service-desk/acc-selector-tag.md)  
  
- [<span data-ttu-id="0d0c5-116">Thẻ Tiếp theo</span><span class="sxs-lookup"><span data-stu-id="0d0c5-116">Next Tag</span></span>](../unified-service-desk/next-tag-windda.md)  
  
- [<span data-ttu-id="0d0c5-117">Thẻ FindWindow</span><span class="sxs-lookup"><span data-stu-id="0d0c5-117">FindWindow Tag</span></span>](../unified-service-desk/find-window-tag.md)  
  
  <span data-ttu-id="0d0c5-118">Chủ đề sau đây cung cấp các thông tin về các sự kiện mà WinDDA hỗ trợ:</span><span class="sxs-lookup"><span data-stu-id="0d0c5-118">The following topic provides information about the events that the WinDDA supports:</span></span>  
  
- [<span data-ttu-id="0d0c5-119">Sự kiện WinDDA</span><span class="sxs-lookup"><span data-stu-id="0d0c5-119">WinDDA events</span></span>](../unified-service-desk/win-dda-events.md)  
  
### <a name="see-also"></a><span data-ttu-id="0d0c5-120">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="0d0c5-120">See also</span></span>  
 <span data-ttu-id="0d0c5-121">[Use Data Driven Adapters](../unified-service-desk/use-data-driven-adapters-ddas.md) </span><span class="sxs-lookup"><span data-stu-id="0d0c5-121">[Use Data Driven Adapters](../unified-service-desk/use-data-driven-adapters-ddas.md) </span></span>  
 <span data-ttu-id="0d0c5-122">[WebDDA](../unified-service-desk/web-dda.md) </span><span class="sxs-lookup"><span data-stu-id="0d0c5-122">[WebDDA](../unified-service-desk/web-dda.md) </span></span>  
 <span data-ttu-id="0d0c5-123">[UIADDA](../unified-service-desk/uiadda.md) </span><span class="sxs-lookup"><span data-stu-id="0d0c5-123">[UIADDA](../unified-service-desk/uiadda.md) </span></span>  
 [<span data-ttu-id="0d0c5-124">JavaDDA</span><span class="sxs-lookup"><span data-stu-id="0d0c5-124">JavaDDA</span></span>](../unified-service-desk/javadda.md)
