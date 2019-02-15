---
title: Events in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Events in Unified Service Desk are notifications that a hosted control can trigger to indicate to the application that something is occurring. Bạn có thể gán cuộc gọi hành động cho một sự kiện mà bạn muốn chạy khi sự kiện xảy ra và các cuộc gọi hành động sẽ được thực hiện theo thứ tự được xác định trong trường Thứ tự của định nghĩa sự kiện.
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
ms.assetid: dbb7d1c8-bbcf-42b2-a92d-96c82b285471
caps.latest.revision: 6
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: b2c4f76d3a66d4576585c3d1f979b8dff27af0e8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386720"
---
# <a name="events-in-unified-service-desk"></a>Events in Unified Service Desk
Sự kiện trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] là thông báo mà kiểm soát tổ chức có thể kích hoạt để cho ứng dụng biết rằng có điều gì đó đang xảy ra. Bạn có thể gán cuộc gọi hành động cho một sự kiện mà bạn muốn chạy khi sự kiện xảy ra và các cuộc gọi hành động sẽ được thực hiện theo thứ tự được xác định trong trường **Thứ tự** của định nghĩa sự kiện.  
  
 Sự kiện có thể có thông số, thông số này được trả về khi sự kiện xảy ra và có thể được sử dụng bởi một cuộc gọi hành động được gán cho các sự kiện như một tham số dữ liệu. Tham số sự kiện được sử dụng như tham số thay thế. Ví dụ, sự kiện **BrowserDocumentComplete** cho loại **Trang CRM** của kiểm soát tổ chức trả về URL của trang đã tải làm tham số sự kiện. Điều này có thể được sử dụng như tham số thay thế, ví dụ như [[url]] cho cuộc gọi hành động được gán cho sự kiện.  
  
 Bạn cũng có thể tạo sự kiện do người dùng xác định trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Create a user-defined event](../unified-service-desk/create-user-defined-event.md)  
  
### <a name="see-also"></a>Xem thêm  
 [Add action calls to an event](../unified-service-desk/add-action-calls-event.md)   
 [Cuộc gọi hành động](../unified-service-desk/action-calls.md)   
 [Core concepts for configuring Unified Service Desk](../unified-service-desk/core-concepts-for-configuring-unified-service-desk.md)
