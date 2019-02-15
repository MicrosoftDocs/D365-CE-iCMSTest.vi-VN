---
title: Manage access in Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn how to control user access to Unified Service Desk for Dynamics 365 for Customer Engagement apps by using configuration and security roles.
ms.custom:
- dyn365-USD, dyn365-admin
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
ms.assetid: 6246a780-eb72-4c37-b84a-9a78904ed631
caps.latest.revision: 5
author: kabala123
ms.author: kabala
manager: shujoshi
tags:
- MigrationHO
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: b1c592430deb42463c532e5e4a575c9a763e2bb3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382555"
---
# <a name="about-access-control"></a>About access control
[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration entities and the underlying [!INCLUDE[pn_user_inteface_integration_uii](../../includes/pn-user-interface-integration-uii.md)] entities are stored in [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps, and you can use the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] security model to govern access to both of these entities. [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] has a robust security model that combines role-based, record-level, and field-level security to define the overall security rights that users have. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Security concepts for Microsoft Dynamics CRM](/dynamics365/customer-engagement/admin/security-concepts)  
  
 [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]người dùng có thể được phân loại rộng rãi thành hai loại:  
  
- **Quản trị viên**: những người đặt cấu hình các [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] và thực thể UII để xác định một ứng dụng tổng đài viên.  
  
- **Tổng đài viên**: những người sử dụng các [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] ứng dụng khách để đọc cấu hình trong [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] và thực thể UII để thực hiện công việc hàng ngày của họ trong một trung tâm cuộc gọi.  
  
## <a name="using-unified-service-desk-security-roles"></a>Sử dụng vai trò bảo mật mới cho Unified Service Desk  
 Khi bạn triển khai [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] cho phiên bản [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], bốn vai trò bảo mật được tạo ra:  
  
- Vai trò **UIIAdministrator** và **UIIAgent** xác định quyền truy cập vào UII và yêu cầu thực thể [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].  
  
- Vai trò **Quản trị viên USD** và **USD đại lý** xác định quyền truy cập vào các [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] tổ chức, các thực thể UII tiềm ẩn, và yêu cầu [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] thực thể. Bạn phải gán một trong hai vai trò cho người dùng trong tổ chức của bạn tùy thuộc vào vai trò công việc của họ (người quản trị hoặc đại lý).  
  
  [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Implement security using custom security roles](../../unified-service-desk/admin/manage-access-using-unified-service-desk-security-roles.md)  
  
## <a name="using-unified-service-desk-configuration"></a>Sử dụng cấu hình ứng dụng Unified Service Desk  
 Một cách tiếp cận khác để lọc truy cập vào dữ liệu [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] là thông qua sử dụng cấu hình. Cấu hình là nhóm hợp lý của các thành phần khác nhau trong ứng dụng đại lý [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] chẳng hạn như cuộc gọi hành động, mã lệnh tổng đài viên, tìm kiếm thực thể, sự kiện, và kiểm soát tổ chức. Cấu hình có thể được gán cho người dùng để khi người dùng bắt đầu ứng dụng tổng đài viên [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], chỉ có các thành phần bao gồm trong cấu hình được hiển thị. Đây là một cách tuyệt vời để lọc điều mà bạn muốn được hiển thị cho các tổng đài viên của bạn mà không cần phải quản lý vai trò bảo mật của họ. Tuy nhiên, xin vui lòng lưu ý những điều sau đây:  
  
- A configuration can only be assigned to a user, and not to a team in [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  
  
- Một cấu hình chỉ lọc các thành phần khi bạn truy cập vào thông tin [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] thông qua ứng dụng khách. If you access [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../../includes/pn-microsoft-dynamics-crm-for-outlook.md)] directly, you can access data as per your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] security role.  
  
  [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Manage access using Unified Service Desk configuration](../../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)  
  
  
## <a name="see-also"></a>Xem thêm  
 [Quản lý quyền truy cập bằng cách sử dụng vai trò bảo mật của Unified Service Desk](../../unified-service-desk/admin/manage-access-using-unified-service-desk-security-roles.md)  
  
 [Quản lý quyền truy cập bằng cách sử dụng cấu hình của Unified Service Desk](../../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)  
