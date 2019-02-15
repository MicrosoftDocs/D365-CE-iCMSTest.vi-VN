---
title: UIA Extensibility in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about UIA extensibility in Unified Service Desk.
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
ms.assetid: 7a2c950b-36e6-48ef-8990-2725219255ed
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
ms.openlocfilehash: 4a308b370ddba641f3046018d1bb4446b66e0562
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385853"
---
# <a name="uia-extensibility-in-unified-service-desk"></a>UIA Extensibility in Unified Service Desk
Bạn có thể thêm đối số `data` vào từng phương pháp DDA khác nhau `OperationHandler` để cho phép khả năng mở rộng UIA. Bạn có thể sử dụng tham số này để mở rộng DDA khi cần. Theo mặc định, nếu tham số này là null, các phương pháp DDA khác nhau sẽ theo dõi hành vi mặc định. Bạn có thể đặt nội dung của tham số này cho một đối tượng. Chủ đề này mô tả cách mở rộng UIA bằng tham số `data`.  
  
 Đối với mỗi hoạt động sau, phương pháp `Execute` của hoạt động tương ứng sẽ xây dựng đối tượng dữ liệu để được chuyển tới phương pháp `OperationHandler` của DDA. Tham số `Data` được bao gồm trong các hoạt động sau:  
  
- `GetControlValue`: **"Desired Pattern to use/Desired Property name to retrieve"** can be passed to the data parameter to retrieve the specified property. The property can be any one from the [UIA property list](../unified-service-desk/uia-property-list.md).  `ControlProperty` – Chỉ định thuộc tính mà DDA nên truy xuất.  
  
- `SetControlValue`: **"Desired pattern Name" (Desired Pattern to use)** shall be passed to the data parameter to perform the pattern selection. The pattern can be any one from the [UIA Pattern List](../unified-service-desk/uia-pattern-list.md).  `ControlProperty` – Chỉ định thuộc tính mà DDA nên gán.  
  
- `ExecuteControlValue`: **"Desired pattern Name" (Desired Pattern to use)** shall be passed to the data parameter to perform the pattern execution. The pattern can be any one from the [UIA Pattern List](../unified-service-desk/uia-pattern-list.md) later in this section.  
  
- `RegisterActionForEvent`: **"For PropertyChangedEvent"** (data property) can be used to specify the property on which the event will be triggered. The property can be any one from the [UIA property list](../unified-service-desk/uia-property-list.md) later in this section.  
  
  Điều này được sử dụng để chuyển bất kỳ dữ liệu nào từ hoạt động của quy trình làm việc đến bộ chuyển đổi. Dữ liệu này có thể được DDA sử dụng hoặc bằng cách mở rộng DDA.  
  
### <a name="see-also"></a>Xem thêm  
 [UIADDA](../unified-service-desk/uiadda.md)   
 [Use Data Driven Adapters (DDAs)](../unified-service-desk/use-data-driven-adapters-ddas.md)
