---
title: UII actions in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about UII actions in Unified Service Desk that define a specific operation that can be performed when called.
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
ms.assetid: 145b3e99-2423-441e-88ac-ec99b1364ed6
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
ms.openlocfilehash: 0c024104ad0552e323eae41e0576f5e40cf059e1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388151"
---
# <a name="uii-actions-in-unified-service-desk"></a>UII actions in Unified Service Desk
Hành động UII là một khái niệm kế thừa từ [!INCLUDE[pn_user_interface_integration](../includes/pn-user-interface-integration.md)] (UII). Hành động UII là cốt lõi của kiểm soát tổ chức và xác định một hoạt động cụ thể mà có thể được thực hiện khi được gọi. Hành động UII có thể được dùng như các phương pháp chung mà có thể được gọi từ thành phần bên ngoài và là chủ đề của cuộc gọi hành động trong [!INCLUDE[pn_unified_service_desk_for_crm](../includes/pn-unified-service-desk-for-crm.md)]. Kiểm soát tổ chức không thể tương tác với phần còn lại của các ứng dụng nếu không có hành động UII được xác định hoặc có sẵn cho kiểm soát tổ chức.  
  
 Với mỗi loại kiểm soát tổ chức được xác định trước trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], một tập hợp các hoạt động UII có sẵn. For information about predefined UII actions available for each hosted control type, see [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md). If you are developing a custom hosted control, it is not enough to just override the `DoAction` method in the code to handle a specific action for the hosted control. You must explicitly define the action in the **UII Actions** list for the custom hosted control in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, thereby enabling the user to call it using action calls. For more information about explicitly defining a UII action for a custom hosted control, see [Create custom Unified Service Desk hosted control](../unified-service-desk/walkthrough-create-custom-hosted-control-for-unified-service-desk.md).  
  
### <a name="see-also"></a>Xem thêm  
 [Thêm một hành động UII vào một điều khiển tổ chức](../unified-service-desk/add-uii-action-hosted-control.md)   
 [Cuộc gọi hành động](../unified-service-desk/action-calls.md)   
 [Create an action call for a UII action](../unified-service-desk/create-action-call-uii-action.md)   
 [Core concepts for configuring Unified Service Desk](../unified-service-desk/core-concepts-for-configuring-unified-service-desk.md)