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
# <a name="javadda-in-unified-service-desk"></a>JavaDDA in Unified Service Desk
The [!INCLUDE[pn_Java](../includes/pn-java.md)] data-driven adapter (JavaDDA) uses the [Java Access Bridge](http://www.oracle.com/technetwork/java/javase/tech/index-jsp-136191.html) to automate [!INCLUDE[pn_Java](../includes/pn-java.md)] applications. [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] supports Java Access Bridge 2.0.2. Bạn có thể sử dụng công cụ như [Java Monkey](https://docs.oracle.com/javase/accessbridge/2.0.2/javamonkey.htm) và [Java Ferret](https://docs.oracle.com/javase/accessbridge/2.0.2/javaferret.htm) để hiểu cấu trúc khả năng truy cập của ứng dụng. Để sử dụng DDA, bạn cần kiểm tra ứng dụng bằng một trong những công cụ này và xây dựng liên kết theo cách thủ công và hỗ trợ chúng cho DDA đang sử dụng chuỗi khởi tạo.  
  
 JavaDDA xác định ba loại kiểm soát:  `JAccControl`, `JAccSelector` và `JAccTree`. Mỗi thẻ kiểm soát phải có một thuộc tính tên chỉ định tên của bộ điều khiển được sử dụng trong tự động hóa hoạt động [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)].  
  
> [!NOTE]
> [!INCLUDE[pn_Java](../includes/pn-java.md)]Ứng dụng Abstract Window Toolkit (AWT) không được hỗ trợ đầy đủ trong [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)]. Bạn phải đặt cấu hình các ứng dụng AWT với WinDDA và chạy chúng như ứng dụng Win32 thông thường. WinDDA sử dụng Microsoft Active Accessibility (MSAA) để truy cập các điều khiển ứng dụng. Một số kiểm soát AWT có thể không tương thích đầy đủ với MSAA, do đó chúng có thể không hoạt động đúng cách. JavaDDA không được hỗ trợ cho [!INCLUDE[pn_WinSer2008](../includes/pn-winser2008.md)]. Để truy cập các kiểm soát AWT [!INCLUDE[pn_Java](../includes/pn-java.md)], bạn có thể sử dụng các công cụ như [Java Monkey](https://docs.oracle.com/javase/accessbridge/2.0.2/javamonkey.htm) và [Java Ferret](https://docs.oracle.com/javase/accessbridge/2.0.2/javaferret.htm).  
  
## <a name="javadda-tags"></a>Thẻ JavaDDA  
 Sau đây là các thẻ JavaDDA khác nhau:  
  
-   [Thẻ JAccControl](../unified-service-desk/jacc-control-tag.md)  
  
-   [Thẻ JAccSelector](../unified-service-desk/jacc-selector-tag.md)  
  
-   [Thẻ JAccTree](../unified-service-desk/jacc-tree-tag.md)  
  
-   [Thẻ Nút Đường dẫn Tìm kiếm](../unified-service-desk/search-path-node-tag.md)  
  
-   [Next Tag](../unified-service-desk/next-tag-javadda.md) [](../unified-service-desk/next-tag-javadda.md "Next Tag")  
  
-   [NextRole Tag](../unified-service-desk/nextrole-tag.md) [](../unified-service-desk/nextrole-tag.md "NextRole Tag")  
  
-   [Thẻ đường dẫn tìm kiếm FindWindow](../unified-service-desk/find-window-search-path-tag.md)  
  
-   [Sự kiện JavaDDA](../unified-service-desk/java-dda-events.md)  
  
### <a name="see-also"></a>Xem thêm  
 [Use Data Driven Adapters](../unified-service-desk/use-data-driven-adapters-ddas.md)   
 [WinDDA](../unified-service-desk/windda.md)   
 [WebDDA](../unified-service-desk/web-dda.md)   
 [UIADDA](../unified-service-desk/uiadda.md)
