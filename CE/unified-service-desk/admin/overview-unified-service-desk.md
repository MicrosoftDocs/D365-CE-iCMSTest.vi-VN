---
title: Overview of Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Get started with Unified Service Desk for Dynamics 365 for Customer Engagement apps
ms.custom:
- dyn365-USD, dyn365-admin
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: hero-article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: bccc29e3-23a7-4d5a-b53f-432510e63c99
caps.latest.revision: 7
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
ms.openlocfilehash: 34bab7c964461f57a25f5119473d92c815e97886
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382355"
---
# <a name="what-is-unified-service-desk"></a>What is Unified Service Desk?
[!INCLUDE[pn_unified_service_desk_for_crm](../../includes/pn-unified-service-desk-for-crm.md)] Customer Engagement provides a configurable framework for quickly building applications for call centers so that agents can get a unified view of the customer data stored in [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps. Bạn có thể tổng hợp thông tin khách hàng từ khu vực khác nhau trong [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] vào một máy tính để bàn tích hợp cung cấp một cái nhìn 360° về sự tương tác khách hàng. Điều này cấp cho đại lý dịch vụ khách hàng của bạn quyền truy cập ngay lập tức vào thông tin quan trọng của doanh nghiệp để họ có thể nhanh chóng tham gia với khách hàng và giải quyết các thắc mắc và vấn đề.  
  
 [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], which is built using the [!INCLUDE[pn_user_inteface_integration_uii](../../includes/pn-user-interface-integration-uii.md)] framework, is designed as a series of adapters and modules that facilitate management of [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] UI elements (such as pages and dialogs), automatic loading of related records, agent scripting, a configurable toolbar, and so on. [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] can be configured and administered using [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../../includes/pn-microsoft-dynamics-crm-for-outlook.md)]. Using [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to configure agent applications doesn’t require you to write code for the most part, and therefore reduces the lead time to design an agent application as per your business requirements. Also, with the [!INCLUDE[pn_computer_telephony_integration_cti](../../includes/pn-computer-telephony-integration-cti.md)] framework of [!INCLUDE[pn_uii_acronym](../../includes/pn-uii-acronym.md)], organizations can build adapters to connect [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] with their existing [!INCLUDE[pn_cti_acronym](../../includes/pn-cti-acronym.md)] infrastructure to support customer communication in agent desktops over various channels such as chat, email, or telephone.  
  
 ![Video symbol](../../unified-service-desk/media/usd-video-thumbnail.png "Video symbol") [Video: Overview of Unified Service Desk (5:00)](http://go.microsoft.com/fwlink/p/?LinkId=506900)  
  
<a name="UII"></a>   
## <a name="what-is-user-interface-integration"></a>User Interface Integration là gì?  
 [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]thúc đẩy sức mạnh của nền tảng [!INCLUDE[pn_user_inteface_integration_uii](../../includes/pn-user-interface-integration-uii.md)] để giúp bạn nhanh chóng cấu hình ứng dụng tổng đài viên tùy chỉnh. The [!INCLUDE[pn_uii_acronym](../../includes/pn-uii-acronym.md)] framework lets you build and deploy composite agent applications that can provide unified access to customer information in [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps and external systems, and can aggregate different modes of customer interactions or channels. [!INCLUDE[pn_uii_acronym](../../includes/pn-uii-acronym.md)] provides a framework for non-intrusive integration of existing line-of-business (LOB) systems at the UI level. For more information about how you can use [!INCLUDE[pn_uii_acronym](../../includes/pn-uii-acronym.md)], see [Unified Service Desk and the UII framework](../../unified-service-desk/unified-service-desk-uii-framework.md).  
  
<a name="USD"></a>   
## <a name="what-makes-up-unified-service-desk"></a>Cấu tạo của Unified Service Desk?  
 [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]là một tập hợp các giải pháp và tệp dữ liệu có chứa thực thể cấu hình và thực thể cơ bản cho nền tảng [!INCLUDE[pn_uii_acronym](../../includes/pn-uii-acronym.md)]. Bạn đặt cấu hình tổ chức [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] để xác định trải nghiệm người dùng trong ứng dụng khách chẳng hạn như các kiểm soát khác nhau, bố cục, lưu lượng người dùng và v.v. Tất cả các thông tin cấu hình được lưu trữ trong thực thể [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] và bạn có thể bó nó cùng với các giải pháp và tệp dữ liệu vào "gói" xác định ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. Các gói sau đó có thể được triển khai đến bất kỳ phiên bản [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] và người dùng có thể kết nối với nó bằng cách sử dụng ứng dụng khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] để trải nghiệm giao diện và chức năng được xác định bởi các dữ liệu cấu hình của ứng dụng.  
  
 ![Basic Unified Service Desk topology diagram](../../unified-service-desk/media/usd-basic-topology.png "Basic Unified Service Desk topology diagram")  
  
 Tính năng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] được xác định bởi các tập tin hai giải pháp sau:  
  
- **Unified Service Desk động**: Tệp giải pháp có chứa thực thể [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] chính mà bạn đặt cấu hình để xác định trải nghiệm ứng dụng tổng đài viên.  
  
- **[!INCLUDE[pn_user_interface_integration](../../includes/pn-user-interface-integration.md)] for [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps**: This solution contains the underlying entities required by the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration entities.  
  
  [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] comes with four sample applications. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Sample Unified Service Desk applications](../../unified-service-desk/admin/sample-unified-service-desk-applications.md)  
  
  For information about the core [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] concepts, see [Core concepts for configuring Unified Service Desk](../../unified-service-desk/core-concepts-for-configuring-unified-service-desk.md).  
  

## <a name="see-also"></a>Xem thêm  
 [Thử thách của trung tâm cuộc gọi và cách trợ giúp có thể của Unified Service Desk?](../../unified-service-desk/admin/call-center-challenges-how-unified-service-desk-can-help.md)  
  
 [Ứng dụng Unified Service Desk mẫu](../../unified-service-desk/admin/sample-unified-service-desk-applications.md)  
