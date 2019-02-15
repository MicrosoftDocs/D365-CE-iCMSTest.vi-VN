---
title: JavaDDA in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The Java data-driven adapter (JavaDDA) uses the Java Access Bridge to automate Java applications. User Interface Integration (UII) supports Java Access Bridge 2.0.2.
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
ms.assetid: 1992cc1f-c212-486b-a457-aaf7bcf58b52
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
ms.openlocfilehash: dfcc3214f34927d471be9d81f3cadcb6c975a810
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385601"
---
# <a name="javadda-in-unified-service-desk"></a><span data-ttu-id="a4606-104">JavaDDA in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="a4606-104">JavaDDA in Unified Service Desk</span></span>
<span data-ttu-id="a4606-105">The [!INCLUDE[pn_Java](../includes/pn-java.md)] data-driven adapter (JavaDDA) uses the [Java Access Bridge](http://www.oracle.com/technetwork/java/javase/tech/index-jsp-136191.html) to automate [!INCLUDE[pn_Java](../includes/pn-java.md)] applications.</span><span class="sxs-lookup"><span data-stu-id="a4606-105">The [!INCLUDE[pn_Java](../includes/pn-java.md)] data-driven adapter (JavaDDA) uses the [Java Access Bridge](http://www.oracle.com/technetwork/java/javase/tech/index-jsp-136191.html) to automate [!INCLUDE[pn_Java](../includes/pn-java.md)] applications.</span></span> [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] <span data-ttu-id="a4606-106">supports Java Access Bridge 2.0.2.</span><span class="sxs-lookup"><span data-stu-id="a4606-106">supports Java Access Bridge 2.0.2.</span></span> <span data-ttu-id="a4606-107">Bạn có thể sử dụng công cụ như [Java Monkey](https://docs.oracle.com/javase/accessbridge/2.0.2/javamonkey.htm) và [Java Ferret](https://docs.oracle.com/javase/accessbridge/2.0.2/javaferret.htm) để hiểu cấu trúc khả năng truy cập của ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="a4606-107">You can use tools such as [Java Monkey](https://docs.oracle.com/javase/accessbridge/2.0.2/javamonkey.htm) and [Java Ferret](https://docs.oracle.com/javase/accessbridge/2.0.2/javaferret.htm) to understand the accessibility structure of the application.</span></span> <span data-ttu-id="a4606-108">Để sử dụng DDA, bạn cần kiểm tra ứng dụng bằng một trong những công cụ này và xây dựng liên kết theo cách thủ công và hỗ trợ chúng cho DDA đang sử dụng chuỗi khởi tạo.</span><span class="sxs-lookup"><span data-stu-id="a4606-108">To use the DDA, you need to inspect the application using either of these tools, and build the bindings manually and feed them to the DDA using initstring.</span></span>  
  
 <span data-ttu-id="a4606-109">JavaDDA xác định ba loại kiểm soát:  `JAccControl`, `JAccSelector` và `JAccTree`.</span><span class="sxs-lookup"><span data-stu-id="a4606-109">The JavaDDA defines three control types:  `JAccControl`, `JAccSelector`, and `JAccTree`.</span></span> <span data-ttu-id="a4606-110">Mỗi thẻ kiểm soát phải có một thuộc tính tên chỉ định tên của bộ điều khiển được sử dụng trong tự động hóa hoạt động [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)].</span><span class="sxs-lookup"><span data-stu-id="a4606-110">Each control tag must have a name attribute that specifies the name of the control used in [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)]automation activities.</span></span>  
  
> [!NOTE]
> [!INCLUDE[pn_Java](../includes/pn-java.md)]<span data-ttu-id="a4606-111">Ứng dụng Abstract Window Toolkit (AWT) không được hỗ trợ đầy đủ trong [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)].</span><span class="sxs-lookup"><span data-stu-id="a4606-111">Abstract Window Toolkit (AWT) applications are not fully supported in [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)].</span></span> <span data-ttu-id="a4606-112">Bạn phải đặt cấu hình các ứng dụng AWT với WinDDA và chạy chúng như ứng dụng Win32 thông thường.</span><span class="sxs-lookup"><span data-stu-id="a4606-112">You must configure the AWT applications with the WinDDA and run them as regular Win32 applications.</span></span> <span data-ttu-id="a4606-113">WinDDA sử dụng Microsoft Active Accessibility (MSAA) để truy cập các điều khiển ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="a4606-113">The WinDDA uses Microsoft Active Accessibility (MSAA) to access the applications controls.</span></span> <span data-ttu-id="a4606-114">Một số kiểm soát AWT có thể không tương thích đầy đủ với MSAA, do đó chúng có thể không hoạt động đúng cách.</span><span class="sxs-lookup"><span data-stu-id="a4606-114">Some AWT controls might not be fully compatible with MSAA, so they may not function properly.</span></span> <span data-ttu-id="a4606-115">JavaDDA không được hỗ trợ cho [!INCLUDE[pn_WinSer2008](../includes/pn-winser2008.md)].</span><span class="sxs-lookup"><span data-stu-id="a4606-115">The JavaDDA is not supported for [!INCLUDE[pn_WinSer2008](../includes/pn-winser2008.md)].</span></span> <span data-ttu-id="a4606-116">Để truy cập các kiểm soát AWT [!INCLUDE[pn_Java](../includes/pn-java.md)], bạn có thể sử dụng các công cụ như [Java Monkey](https://docs.oracle.com/javase/accessbridge/2.0.2/javamonkey.htm) và [Java Ferret](https://docs.oracle.com/javase/accessbridge/2.0.2/javaferret.htm).</span><span class="sxs-lookup"><span data-stu-id="a4606-116">To access [!INCLUDE[pn_Java](../includes/pn-java.md)] AWT controls, you can use tools such as [Java Monkey](https://docs.oracle.com/javase/accessbridge/2.0.2/javamonkey.htm) and [Java Ferret](https://docs.oracle.com/javase/accessbridge/2.0.2/javaferret.htm).</span></span>  
  
## <a name="javadda-tags"></a><span data-ttu-id="a4606-117">Thẻ JavaDDA</span><span class="sxs-lookup"><span data-stu-id="a4606-117">JavaDDA tags</span></span>  
 <span data-ttu-id="a4606-118">Sau đây là các thẻ JavaDDA khác nhau:</span><span class="sxs-lookup"><span data-stu-id="a4606-118">The following are the various JavaDDA tags:</span></span>  
  
-   [<span data-ttu-id="a4606-119">Thẻ JAccControl</span><span class="sxs-lookup"><span data-stu-id="a4606-119">JAccControl Tag</span></span>](../unified-service-desk/jacc-control-tag.md)  
  
-   [<span data-ttu-id="a4606-120">Thẻ JAccSelector</span><span class="sxs-lookup"><span data-stu-id="a4606-120">JAccSelector Tag</span></span>](../unified-service-desk/jacc-selector-tag.md)  
  
-   [<span data-ttu-id="a4606-121">Thẻ JAccTree</span><span class="sxs-lookup"><span data-stu-id="a4606-121">JAccTree Tag</span></span>](../unified-service-desk/jacc-tree-tag.md)  
  
-   [<span data-ttu-id="a4606-122">Thẻ Nút Đường dẫn Tìm kiếm</span><span class="sxs-lookup"><span data-stu-id="a4606-122">Search Path Node Tag</span></span>](../unified-service-desk/search-path-node-tag.md)  
  
-   <span data-ttu-id="a4606-123">[Next Tag](../unified-service-desk/next-tag-javadda.md) [](../unified-service-desk/next-tag-javadda.md "Next Tag")</span><span class="sxs-lookup"><span data-stu-id="a4606-123">[Next Tag](../unified-service-desk/next-tag-javadda.md) [](../unified-service-desk/next-tag-javadda.md "Next Tag")</span></span>  
  
-   <span data-ttu-id="a4606-124">[NextRole Tag](../unified-service-desk/nextrole-tag.md) [](../unified-service-desk/nextrole-tag.md "NextRole Tag")</span><span class="sxs-lookup"><span data-stu-id="a4606-124">[NextRole Tag](../unified-service-desk/nextrole-tag.md) [](../unified-service-desk/nextrole-tag.md "NextRole Tag")</span></span>  
  
-   [<span data-ttu-id="a4606-125">Thẻ đường dẫn tìm kiếm FindWindow</span><span class="sxs-lookup"><span data-stu-id="a4606-125">FindWindow search path tag</span></span>](../unified-service-desk/find-window-search-path-tag.md)  
  
-   [<span data-ttu-id="a4606-126">Sự kiện JavaDDA</span><span class="sxs-lookup"><span data-stu-id="a4606-126">JavaDDA Events</span></span>](../unified-service-desk/java-dda-events.md)  
  
### <a name="see-also"></a><span data-ttu-id="a4606-127">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a4606-127">See also</span></span>  
 <span data-ttu-id="a4606-128">[Use Data Driven Adapters](../unified-service-desk/use-data-driven-adapters-ddas.md) </span><span class="sxs-lookup"><span data-stu-id="a4606-128">[Use Data Driven Adapters](../unified-service-desk/use-data-driven-adapters-ddas.md) </span></span>  
 <span data-ttu-id="a4606-129">[WinDDA](../unified-service-desk/windda.md) </span><span class="sxs-lookup"><span data-stu-id="a4606-129">[WinDDA](../unified-service-desk/windda.md) </span></span>  
 <span data-ttu-id="a4606-130">[WebDDA](../unified-service-desk/web-dda.md) </span><span class="sxs-lookup"><span data-stu-id="a4606-130">[WebDDA](../unified-service-desk/web-dda.md) </span></span>  
 [<span data-ttu-id="a4606-131">UIADDA</span><span class="sxs-lookup"><span data-stu-id="a4606-131">UIADDA</span></span>](../unified-service-desk/uiadda.md)
