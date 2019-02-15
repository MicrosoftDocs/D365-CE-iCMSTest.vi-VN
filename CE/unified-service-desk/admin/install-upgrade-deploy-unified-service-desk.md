---
title: Install, deploy, and upgrade Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn how to install or upgrade Unified Service Desk for Dynamics 365 for Customer Engagement apps.
ms.custom:
- dyn365-USD, dyn365-admin
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
ms.assetid: e0fd70b6-73a4-4426-92d7-bb300457597e
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
ms.openlocfilehash: 103b8a0d4930405e07942459b9fe11d786f179b5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382441"
---
# <a name="install-deploy-and-upgrade-unified-service-desk"></a>Install, deploy, and upgrade Unified Service Desk
Before you can install and deploy [!INCLUDE[pn_unified_service_desk_for_crm](../../includes/pn-unified-service-desk-for-crm.md)], you must identify the [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps instance that you want to build and deploy the configuration on. While you can use a new [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] works best when the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] customization is mostly complete. [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] controls the call center agent’s view of [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] by manipulating windows, injecting [!INCLUDE[pn_JavaScript](../../includes/pn-javascript.md)], and so on. Nếu những thay đổi lớn xảy ra đối với môi trường [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] sau khi [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] được triển khai, nó có thể làm cho cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] của bạn không còn hoạt động theo yêu cầu. While the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration often comes later in a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] implementation, having [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] in mind when designing your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] environment is beneficial.  
  
 Cài đặt và triển khai [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] được thực hiện trong giai đoạn nơi ban đầu bạn thiết lập một môi trường phát triển để đặt cấu hình ứng dụng tổng đài viên bằng cách sử dụng một trong các ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mẫu làm cơ sở. Next, you test how your configurations appear and work using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application by connecting to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance where you configured [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. Next, you use the customized [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration on to a Production instance of [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], and the client application. The configuration includes the Customization Files package used to distribute to your agent’s computers any files and assemblies that are required.  
  
> [!IMPORTANT]
>  Bạn có thể cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] để tích hợp với các ứng dụng ngành nghề kinh doanh của bên thứ ba (LOB). However, before deploying an integrated solution (involving [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and LOB applications) in the production environment in your organization, you must thoroughly test your integrated solution to ensure that the performance results are aligned with your expectations. [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] might not function appropriately if integrated with LOB applications that demonstrate user interface (UI) blocking, memory leak issues, and slow response times.  
  
 Liệt kê dưới đây là trình tự mà chúng tôi khuyên bạn nên cài đặt và triển khai [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] trong tổ chức của bạn. Before installing [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], ensure that you meet the system requirements: [Unified Service Desk system requirements](../../unified-service-desk/admin/unified-service-desk-system-requirements.md).  
  
## <a name="step-1-initial-installation-and-deployment"></a>Bước 1: Cài đặt và triển khai đầu tiên  
 Xác định máy chủ [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] mà bạn muốn triển khai [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] và một máy tính phát triển sẽ được sử dụng cho triển khai gói [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] và sau đó kết nối với các gói bằng cách sử dụng ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].  
  
1. Cài đặt ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] trên máy tính phát triển. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Install the Unified Service Desk Client](../../unified-service-desk/admin/install-upgrade-unified-service-desk-client.md)  
  
2. Triển khai gói [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] cho phiên bản [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)]. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Deploy Unified Service Desk packages to Dynamics 365 for Customer Engagement server using Package Deployer](../../unified-service-desk/admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md)  
  
3. Run the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client, and connect to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance where you deployed the packages to verify that everything is working correctly. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Connect to Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)  
  
   **Thiết lập máy tính phát triển thêm**  
  
   To set up additional development computers for configuring your agent desktop applications using [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], install the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client on the computer. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Install Unified Service Desk Client](../../unified-service-desk/admin/install-upgrade-deploy-unified-service-desk.md)  
  
## <a name="step-2-configure-and-test-your-agent-application"></a>Bước 2: Đặt cấu hình và kiểm tra ứng dụng tổng đài viên của bạn  
 Use your development environment to configure your agent application by building on one of the available sample applications you deployed, and then test it by connecting to the customized package using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Use Unified Service Desk to configure your agent application](../../unified-service-desk/configure-agent-application-unified-service-desk.md)  
  
## <a name="step-3-deploy-the-customized-agent-application"></a>Bước 3: Triển khai ứng dụng đại lý tùy chỉnh  
 Sau khi bạn đã tùy chỉnh ứng dụng đại lý của bạn thông qua các cấu hình hoặc mã tùy chỉnh, bạn phải cài đặt ứng dụng khách hàng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]cùng với bất kỳ tập tin cần thiết cho các chức năng tùy chỉnh trên máy tính của đại lý của bạn. Consider creating a [!INCLUDE[pn_clickonce](../../includes/pn-clickonce.md)] application or an MSI package installer to bundle all the files together and deploy on the agent computers in your organization. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] see [MSDN: ClickOnce Security and Deployment](http://msdn.microsoft.com/library/t71a733d.aspx) or [MSDN: Windows Installer](http://msdn.microsoft.com/library/cc185688\(v=vs.85\).aspx)  
  
 Bạn cũng có thể muốn di chuyển cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] của bạn từ một bài kiểm tra/phát triển đến một môi trường sản xuất. Bạn có thể sử dụng [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)] mới để di chuyển dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] giữa phiên bản [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)]. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Migrate your Unified Service Desk configuration to another Dynamics 365 for Customer Engagement server](../../unified-service-desk/admin/migrate-unified-service-desk-configuration-dynamics-365-server.md)  
    
  
## <a name="see-also"></a>Xem thêm  
 [Yêu cầu hệ thống Unified Service Desk](../../unified-service-desk/admin/unified-service-desk-system-requirements.md)  
  
 [Cài đặt ứng dụng Unified Service Desk](../../unified-service-desk/admin/install-upgrade-unified-service-desk-client.md)  
  
 [Deploy sample Unified Service Desk applications to Dynamics 365 for Customer Engagement server using Package Deployer](../../unified-service-desk/admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md)  
  
 [Connect to Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)   
 
