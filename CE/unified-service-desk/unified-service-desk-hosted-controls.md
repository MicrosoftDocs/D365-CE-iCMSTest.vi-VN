---
title: Unified Service Desk Hosted Controls | MicrosoftDocs
description: Learn about the basic concepts related to hosted controls in Unified Service Desk.
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
ms.assetid: 41ebb3f2-f9e1-40b0-bc5b-4af20b0c066b
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
ms.openlocfilehash: 068f813636b521a157a334ad99a7d9c77671baf2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387865"
---
# <a name="unified-service-desk-hosted-controls"></a>Kiểm soát Tổ chức Unified Service Desk
Khái niệm kiểm soát tổ chức là trung tâm với việc triển khai [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], và là yếu tố chính được sử dụng để xây dựng ứng dụng tác nhân sử dụng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. A hosted control in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] is a .NET component or a Dynamics 365 for Customer Engagement apps/external webpage that is hosted within an agent application.
  
<a name="PredefinednCustom"></a>   
## <a name="predefined-and-custom-unified-service-desk-hosted-controls"></a>Predefined and custom Unified Service Desk hosted controls  
 [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] provides you with various types of *predefined* hosted control depending on the component that you want to configure and display in your agent application. For example, a **CRM Page** type of hosted control is used to display a Dynamics 365 for Customer Engagement apps page in your agent application and a **Standard Web Application** type of hosted control is used for external web pages. Each hosted control type has a set of predefined events and actions associated with it. For more information, see [Events](../unified-service-desk/events.md) and [UII actions](../unified-service-desk/uii-actions.md). You can execute an action on a hosted control by creating an action call for the action. For more information, see [Action calls](../unified-service-desk/action-calls.md).  
  
 You can also create custom [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] hosted controls if none of the predefined hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] serve your purpose, and you desire some custom functionality. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Create custom Unified Service Desk hosted control](../unified-service-desk/walkthrough-create-custom-hosted-control-for-unified-service-desk.md)  
  
 For information about the various types of predefined hosted controls, and the events and UII actions associated with each type, see [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md).  
  
<a name="BaseClass"></a>   
## <a name="base-class-of-a-unified-service-desk-hosted-control"></a>Base class of a Unified Service Desk hosted control  
 All the predefined and custom hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] are objects that are derived from the [DynamicsBaseHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol) class. This class defines the methods and properties that are applicable to all the hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
 This is important for you to know because you can also create [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] hosted controls, which are derived from another class, and host them in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. For more information about the UII hosted controls, see [Use UII hosted controls with Unified Service Desk](../unified-service-desk/use-uii-hosted-controls-unified-service-desk.md).  
  
<a name="Global"></a>   
## <a name="global-and-session-based-unified-service-desk-hosted-controls"></a>Global and session-based Unified Service Desk hosted controls  
 From a lifecycle perspective, [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] has two types of [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] hosted controls: global and session-based. Kiểm soát tổ chức chung được bắt đầu khi các ứng dụng tác nhân và được phục hồi khi ứng dụng tác nhân đã chấm dứt. Kiểm soát tổ chức dựa trên phiên được bắt đầu khi phiên bắt đầu và thường được khôi phục ở cuối phiên.  
  
<a name="Dynamic"></a>   
## <a name="dynamic-unified-service-desk-hosted-controls"></a>Dynamic Unified Service Desk hosted controls  
 [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]cũng hỗ trợ kiểm soát tổ chức động cho phép một tác nhân bắt đầu hoặc đóng kiểm soát tổ chức theo yêu cầu, hoặc bằng cách sử dụng giao diện người dùng hoặc lập trình trong mã. Kiểm soát tổ chức động có thể là chung hoặc riêng. Kiểm soát tổ chức động chung được tải theo yêu cầu đầu tiên và bị ẩn sau đó và chúng có thể được yêu cầu tại bất kỳ thời điểm nào, chẳng hạn như trong một phiên chung, phiên bình thường hoặc quy trình làm việc. Kiểm soát tổ chức động chung chỉ có thể được tải sau khi phiên đã bắt đầu và mỗi phiên sử dụng một phiên bản ứng dụng khác nhau. Nếu kiểm soát tổ chức động là một phần của quy trình làm việc và chưa được bắt đầu khi quy trình làm việc bắt đầu, sau đó quy trình làm việc sẽ bắt đầu và đóng kiểm soát tổ chức khi quy trình làm việc hoàn tất.  
  
### <a name="see-also"></a>Xem thêm  
 [Hosted control types, actions, and events](../unified-service-desk/hosted-control-types-actions-events.md)   
 [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md)   
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)   
 [Học cách sử dụng Unified Service Desk](../unified-service-desk/learn-to-use-unified-service-desk.md)   
 [Use UII hosted controls with Unified Service Desk](../unified-service-desk/use-uii-hosted-controls-unified-service-desk.md)
