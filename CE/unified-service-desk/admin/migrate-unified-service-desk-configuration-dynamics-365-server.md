---
title: Migrate your Unified Service Desk for Dynamics 365 for Customer Engagement apps configuration to another Dynamics 365 for Customer Engagement apps instance | MicrosoftDocs
description: Learn how to move a Unified Service Desk for Dynamics 365 for Customer Engagement apps configuration to another instance.
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
ms.assetid: 49ebffe9-a55c-466a-a5ea-779510db2c4f
caps.latest.revision: 7
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 96c37f74f60840c2fa3193891afa24c56e30b9ac
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382398"
---
# <a name="migration-of-a-unified-service-desk-configuration"></a>Migration of a Unified Service Desk configuration 
Sau khi bạn đã hoàn thành phát triển hoặc cấu hình ứng dụng tổng đài viên của bạn, bạn có thể muốn di chuyển dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mới nhất của bạn từ môi trường phát triển hoặc thử nghiệm của bạn tới môi trường sản xuất của bạn. Migrating your data involves exporting your existing configuration data from the source [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance, and then importing it into the target [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.  
  
 To export your configuration data, you can use the [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)] and the default [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration data schema file (USDDefaultSchema.xml). The default schema file contains information about all the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] entities, relationships, and uniqueness definitions for each entity. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Export Unified Service Desk configuration data](../../unified-service-desk/admin/export-unified-service-desk-configuration-data.md)  
  
 For more information about the [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)], see [Manage your configuration data](/dynamics365/customer-engagement/admin/manage-configuration-data).  
  
> [!NOTE]
>  Tệp giản đồ dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mặc định không xuất thông tin người dùng từ hệ thống nguồn.  
> 
>  For records that include notes and attachments, including Customization Files (compressed folder), these items aren’t included in the record during the export.  
  
 Để nhập dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] đã xuất vào phiên bản [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], bạn có thể thực hiện những cách sau:  
  
- **Sử dụng công cụ Configuration Migration**: các công cụ cũng cho phép bạn nhập dữ liệu cấu hình đã xuất. Trước khi bạn làm điều đó mặc dù, bạn phải triển khai một trong gói [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mẫu để tạo ra các thực thể cơ bản trong phiên bản [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] đích. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Import configuration data using the Configuration Migration tool](../../unified-service-desk/admin/import-unified-service-desk-configuration-data.md#ConfigMigration)  
  
- **Use a custom package for Unified Service Desk**: Create a custom package for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to include the exported data along with the files in one of the sample [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] packages, and then deploy the custom package on the target [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance using the [!INCLUDE[pn_package_deployer_tool](../../includes/pn-package-deployer-tool.md)]. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Import configuration data using a custom package for Unified Service Desk](../../unified-service-desk/admin/import-unified-service-desk-configuration-data.md#CustomPackage)  
  
> [!IMPORTANT]
>  [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)] cung cấp hỗ trợ ghi nhật ký cho thông tin chi tiết về hồ sơ về:  
> 
> - Errors that can occur while signing in to the [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps instance using the tool.  
> - Activities performed by the tool during the schema definition and export and import of the configuration data.  
> - Dữ liệu được nhập bằng cách sử dụng công cụ.  
> 
>   There are three log files generated by the tool that are available at the following location on the computer where you run the tool: c:\Users\\*\<UserName>* \AppData\Roaming\Microsoft\DataMigrationUtility\\*\<Version>*.[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Gỡ rối các vấn đề di chuyển dữ liệu cấu hình bằng cách sử dụng tệp nhật ký](/dynamics365/customer-engagement/admin/manage-configuration-data#Logfiles)  
  
  
## <a name="see-also"></a>Xem thêm  
 [Xuất dữ liệu cấu hình của Unified Service Desk](../../unified-service-desk/admin/export-unified-service-desk-configuration-data.md)  
  
 [Nhập dữ liệu cấu hình Unified Service Desk](../../unified-service-desk/admin/import-unified-service-desk-configuration-data.md)  
