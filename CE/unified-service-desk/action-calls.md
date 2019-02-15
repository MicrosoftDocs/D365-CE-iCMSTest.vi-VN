---
title: Action calls | MicrosoftDocs
description: Learn about actions that represents a call to a UII action associated with a hosted control. Action calls are used to pass parameters required to execute the underlying UII action in Unified Service Desk.
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
ms.assetid: 1f5a1817-28c8-4171-a83b-6941a57a5a6b
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
ms.openlocfilehash: 7f204b88552ae3aead0ede5ffbfac549d2ed97ce
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387699"
---
# <a name="action-calls"></a>Cuộc gọi hành động
Một cuộc gọi hành động đại diện cho một cuộc gọi đến một hành động UII được liên kết với kiểm soát tổ chức. Cuộc gọi hành động được sử dụng để vượt qua các tham số cần thiết để thực hiện các hành động UII cơ bản trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
 Một cuộc gọi hành động có thể được gắn liền với những điều sau trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] vì vậy chúng được thực hiện khi:  
  
- Phát sinh một sự kiện.  
  
- Nguyên tắc điều hướng cửa đã được xử lý.  
  
- Nút thanh công cụ được nhấp.  
  
- Mã lệnh tổng đài viên đang chạy hoặc câu trả lời được nhấp vào.  
  
  The action calls, and the sequence in which they are called, define the behavior of the configured system. Hành động cuộc gọi có thể được dùng như cuộc gọi chức năng riêng của nó, nơi các hành động UII là định nghĩa hoặc chữ ký chức năng.  
  
  You can also attach action calls to another action call to execute the attached action calls when the parent action call is executed. The action calls attached to an action call are called the sub-action calls.  
  
### <a name="see-also"></a>Xem thêm  
 [Create an action call for a UII action](../unified-service-desk/create-action-call-uii-action.md)   
 [Add action calls to an event](../unified-service-desk/add-action-calls-event.md)   
 [Hành động UII](../unified-service-desk/uii-actions.md)   
 [Manage hosted controls, actions, and events](../unified-service-desk/manage-hosted-controls-actions-events.md)
