---
title: Hosted control types, actions, and events in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
ms.custom:
- dyn365-USD
ms.date: 04/24/2018
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
ms.assetid: 17eec4a8-03a4-467b-af3e-de99fcab4e22
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: b0018f27570d85c3bfed0432c5617fea14095048
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388474"
---
# <a name="hosted-control-types-actions-and-events-in-unified-service-desk"></a>Hosted control types, actions, and events in Unified Service Desk
Có rất nhiều loại kiểm soát tổ chức được xác định trước có sẵn trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để cho phép bạn xây dựng các loại kiểm soát khác nhau và trải nghiệm người dùng trong ứng dụng tổng đài viên của bạn. For example, to manage all the connections from your agent application to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, you create a hosted control of the **Connection Manager** type. To display data from a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps page, you create a hosted control of the **CRM Page** type.  
  
> [!NOTE]
>  Loại **Kiểm soát tổ chức ruy băng** chỉ sử dụng nội bộ. Bạn không phải sử dụng loại kiểm soát tổ chức trong ứng dụng tổng đài viên của bạn.  
  
## <a name="mandatory-hosted-control-types-in-an-agent-application"></a>Loại kiểm soát tổ chức bắt buộc trong ứng dụng tổng đài viên  
 The **Connection Manager** and **Global Manager** hosted control types are mandatory for a [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] agent application to work, and only a single instance of each of these hosted control types must exist in your agent application. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Connection Manager (Hosted Control)](../unified-service-desk/connection-manager-hosted-control.md) and [Global Manager (Hosted Control)](../unified-service-desk/global-manager-hosted-control.md)  
  
 The sample applications for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] come preconfigured with an instance of each of these two hosted control types. Nếu bạn vô hiệu hóa bất kỳ kiểm soát tổ chức nào trong ứng dụng, ứng dụng sẽ không hoạt động đúng cách. For more information about the four sample applications, see [Sample Unified Service Desk applications](admin/sample-unified-service-desk-applications.md).  
  
## <a name="predefined-uii-actions-and-events-for-hosted-controls"></a>Sự kiện và hành động UII xác định trước cho kiểm soát tổ chức:  
 Dựa trên loại kiểm soát tổ chức, một tập hợp các hành động UII được xác định trước và các sự kiện có sẵn trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Hành động UII là hành động cụ thể mà kiểm soát tổ chức có thể thực hiện. Sự kiện được nêu ra bởi kiểm soát tổ chức và bạn có thể thực hiện một hành động UII khi một sự kiện được đưa lên bằng cách tạo một cuộc gọi hành động UII, và kết hợp các cuộc gọi hành động đến một sự kiện. For information about the predefined actions and events available for each hosted control type, see [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md).  
  
 Bạn cũng có thể xem các hành động và sự kiện UII xác định trước cho kiểm soát tổ chức trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [View predefined actions and events for a hosted control](../unified-service-desk/view-predefined-actions-events-hosted-control.md)  
  
 [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] cung cấp trợ giúp về các hành động và sự kiện UII được xác định trước cho kiểm soát tổ chức trong trợ giúp được nhúng khi bạn xem hoặc làm việc với hành động hoặc sự kiện UII cho kiểm soát tổ chức. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [View embedded help for actions and events](../unified-service-desk/view-embedded-help-for-actions-and-events.md)  
  
> [!NOTE]
>  Hầu hết các kiểm soát tổ chức được xác định trước trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] có hành động được xác định trước được gọi là **mặc định**, mà gọi hành động trên kiểm soát tổ chức mà được đánh dấu là mặc định. Vì không có hành động được xác định trước cho bất kỳ kiểm soát tổ chức nào được đánh dấu là mặc định, gọi hành động **mặc định** trên bất kỳ kiểm soát tổ chức được xác định trước chỉ tải kiểm soát tổ chức tương ứng. Tuy nhiên, với kiểm soát tổ chức [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] tùy chỉnh, bạn có thể xác định một hành động và đặt nó làm mặc định để cho các hành động được gọi khi hành động **mặc định** được gọi trên kiểm soát tổ chức tùy chỉnh. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [USD Hosted Control (Hosted Control)](../unified-service-desk/usd-hosted-control-hosted-control.md)  
  
### <a name="see-also"></a>Xem thêm  
 [Kiểm soát Tổ chức](../unified-service-desk/unified-service-desk-hosted-controls.md)   
 [Hành động](../unified-service-desk/uii-actions.md)   
 [Sự kiện](../unified-service-desk/events.md)   
 [Get started with configuring your agent application](../unified-service-desk/get-started-configuring-agent-application.md)   
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)   
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)
