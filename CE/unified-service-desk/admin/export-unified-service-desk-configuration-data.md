---
title: Export Unified Service Desk for Dynamics 365 for Customer Engagement apps configuration data | MicrosoftDocs
description: Learn how to prepare a file for use with another instance using the Configuration Migration Tool and configuration data schema file.
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
ms.assetid: f3d3b348-ddf7-4174-af34-9583a9f2b7e6
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
ms.openlocfilehash: aa20c6ed48426ba3320955804b722e4e87e69419
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382415"
---
# <a name="export-unified-service-desk-configuration-data"></a>Xuất dữ liệu cấu hình của Unified Service Desk
Bạn có thể xuất khẩu dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] của bạn từ hệ thống nguồn bằng cách sử dụng tệp giản đồ dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mặc định.  
  
1. Tải về [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)] và tệp giản đồ dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] (USDDefaultSchema.xml) mặc định. The tool and the configuration data schema file are available in the [CRM SDK download package](http://go.microsoft.com/fwlink/?LinkID=627298).  
  
   1. Download the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] apps package (.exe), and extract it to find the tool in the SDK\Tools\ConfigurationMigration folder.  
  
   2. Download the UII SDK package (.exe), and extract it to find the USDDefaultSchema.xml file in the UII\USD Developer Assets\USD Configuration Tool Schema folder.  
  
2. Double-click the DataMigrationUtility.exe file in the SDK\Tools\ConfigurationMigration folder to run the [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)], and choose **Export data** in the main screen.  
  
3. Trên màn hình **Đăng nhập**, cung cấp chi tiết xác thực để kết nối với [!INCLUDE[pn_microsoftcrm_server](../../includes/pn-microsoftcrm-server.md)] của bạn từ nơi mà bạn muốn xuất dữ liệu. Nếu bạn có nhiều tổ chức trên máy chủ [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], và muốn chọn tổ chức từ nơi xuất dữ liệu, chọn hộp kiểm **Luôn hiển thị danh sách tổ chức có sẵn**. Select **Login**.  
  
4. Nếu bạn có nhiều tổ chức và muốn chọn tổ hộp kiểm **luôn hiển thị danh sách tổ chức có sẵn**, màn hình tiếp theo cho phép bạn chọn tổ chức bạn muốn kết nối. Chọn một [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] tổ chức để kết nối.  
  
5. Trên màn hình kế tiếp, hãy chọn tệp giản đồ dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mặc định (USDDefaultSchema.xml) để sử dụng cho việc xuất dữ liệu.  
  
6. Chỉ định tên và vị trí của tệp dữ liệu để được xuất.  
  
7. Choose **Export Data**. Màn hình hiển thị trạng thái quá trình xuất và vị trí của tệp đã xuất ở dưới cùng của màn hình sau khi đã xuất xong.  
  
8. Choose **Exit** to close the tool.  
  
## <a name="next-step"></a>Bước tiếp theo  
 [Import Unified Service Desk configuration data](../../unified-service-desk/admin/import-unified-service-desk-configuration-data.md)  
  
## <a name="see-also"></a>Xem thêm  
 [Migrate your Unified Service Desk configuration to another Dynamics 365 for Customer Engagement server](../../unified-service-desk/admin/migrate-unified-service-desk-configuration-dynamics-365-server.md)
