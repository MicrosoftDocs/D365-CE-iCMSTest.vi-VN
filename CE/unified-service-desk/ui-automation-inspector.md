---
title: UI Automation Inspector in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about UII Inspector to support the generation of bindings for the UIADDA.
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
ms.assetid: 8c3e2962-56df-427c-98bf-7fc4fb395749
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
ms.openlocfilehash: a51629e7b1d26b37b557f9634966ef29b8eba573
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388622"
---
# <a name="ui-automation-inspector-in-unified-service-desk"></a>UI Automation Inspector in Unified Service Desk
Trình kiểm tra [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] được mở rộng để hỗ trợ thế hệ liên kết cho UIADDA. Chủ đề này mô tả logic được sử dụng để xây dựng liên kết.  
  
## <a name="logic-to-build-the-binding"></a>Logic để xây dựng liên kết  
  
-   Nhận dạng Kiểm soát dựa trên các thuộc tính sau:  
  
    -   `AutomationId`  
  
    -   `Name`  
  
    -   `ClassName`  
  
    -   `IsEnabled`  
  
-   Chỉ các điều khoản nhóm `AndCondition` mới được sử dụng cho thế hệ, vì thuộc tính cụ thể được sử dụng cho thế hệ.  
  
-   Thuộc tính `MatchCount` sẽ được tạo ra dựa trên sự cần thiết phải liên kết kiểm soát.  
  
> [!NOTE]
>  Thuộc tính `AutomationId` và `Name` là chủ động trong một vài ứng dụng và trong một vài tình huống; trong các trường hợp này, cần xóa thuộc tính khỏi liên kết và cần cập nhật `MatchCount` theo cách thủ công để đặt liên kết.  
  
### <a name="see-also"></a>Xem thêm  
 [UIADDA](../unified-service-desk/uiadda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
