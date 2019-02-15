---
title: Core concepts for configuring Unified Service Desk | MicrosoftDocs
descriptions: Unified Service Desk provides an object-oriented kind of configuration and development experience through its hosted control implementation where the hosted control is equivalent to the object in a typical object-oriented development, and is used throughout Unified Service Desk to provide its loose coupling of components.
ms.custom:
- dyn365-USD
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 3c35c1e5-47eb-40e6-ac3a-8359bef9afd3
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
ms.openlocfilehash: 2198d86d623606d202570a979f881a91197f69e8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388178"
---
# <a name="core-concepts-for-configuring-unified-service-desk"></a>Core concepts for configuring Unified Service Desk
[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] provides an object-oriented kind of configuration and development experience through its *hosted control implementation* where the hosted control is equivalent to the object in a typical object-oriented development, and is used throughout [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to provide its loose coupling of components. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Hosted Controls](../unified-service-desk/unified-service-desk-hosted-controls.md)  
  
 Sơ đồ dưới đây mô tả các khái niệm phát triển định hướng đối tượng và khái niệm tương đương của [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
 ![USD equivalents for object-oriented concepts](../unified-service-desk/media/crm-itpro-usd-oopsequivalent.png "USD equivalents for object-oriented concepts")  
  
 However, there are some important differences between [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] implementations and the typical object-oriented design:  
  
- **Tham số thay thế**, không giống như thuộc tính, được lưu trữ bên ngoài các đối tượng (kiểm soát tổ chức trong trường hợp của [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]) chính nó. This has a distinct advantage in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] that the properties persist longer than the life of the object, thereby allowing action calls to access the properties for use in parameters or logic long after the hosted control that exposed the parameter has been closed. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Replacement parameters](../unified-service-desk/replacement-parameters.md)  
  
- **[!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)]hành động** tương đương với tuyên bố phương pháp. The action must first be defined by the underlying object that implements the action, and then it can be declared in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps as a usable action. Action calls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] are essentially calls to these [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions and typically use replacement parameters as the parameters to the specific UII actions. Vì vậy, trong khi hành động UII đại diện cho tuyên bố hành động có thể được thực hiện, các cuộc gọi hành động đại diện cho các cuộc gọi thực tế để hành động. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [UII actions](../unified-service-desk/uii-actions.md), [Action calls](../unified-service-desk/action-calls.md)  
  
- **Events** in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] make one or more action calls, which internally call UII actions on other objects. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Events](../unified-service-desk/events.md)  
  
## <a name="reference"></a>Tham chiếu  
 [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md)  
    
  
## <a name="related-sections"></a>Các phần liên quan  
 [Learn to use Unified Service Desk](../unified-service-desk/learn-to-use-unified-service-desk.md)  
  
 [Get started with configuring your agent application](../unified-service-desk/get-started-configuring-agent-application.md)  
  
 [Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
