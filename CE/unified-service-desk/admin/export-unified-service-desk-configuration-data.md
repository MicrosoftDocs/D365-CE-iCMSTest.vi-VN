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
# <a name="export-unified-service-desk-configuration-data"></a><span data-ttu-id="540f7-103">Xuất dữ liệu cấu hình của Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="540f7-103">Export Unified Service Desk configuration data</span></span>
<span data-ttu-id="540f7-104">Bạn có thể xuất khẩu dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] của bạn từ hệ thống nguồn bằng cách sử dụng tệp giản đồ dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mặc định.</span><span class="sxs-lookup"><span data-stu-id="540f7-104">You can export your [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration data from your source system by using the default [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration data schema file.</span></span>  
  
1. <span data-ttu-id="540f7-105">Tải về [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)] và tệp giản đồ dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] (USDDefaultSchema.xml) mặc định.</span><span class="sxs-lookup"><span data-stu-id="540f7-105">Download the [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)] and the default [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration data schema file (USDDefaultSchema.xml).</span></span> <span data-ttu-id="540f7-106">The tool and the configuration data schema file are available in the [CRM SDK download package](http://go.microsoft.com/fwlink/?LinkID=627298).</span><span class="sxs-lookup"><span data-stu-id="540f7-106">The tool and the configuration data schema file are available in the [CRM SDK download package](http://go.microsoft.com/fwlink/?LinkID=627298).</span></span>  
  
   1. <span data-ttu-id="540f7-107">Download the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] apps package (.exe), and extract it to find the tool in the SDK\Tools\ConfigurationMigration folder.</span><span class="sxs-lookup"><span data-stu-id="540f7-107">Download the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] apps package (.exe), and extract it to find the tool in the SDK\Tools\ConfigurationMigration folder.</span></span>  
  
   2. <span data-ttu-id="540f7-108">Download the UII SDK package (.exe), and extract it to find the USDDefaultSchema.xml file in the UII\USD Developer Assets\USD Configuration Tool Schema folder.</span><span class="sxs-lookup"><span data-stu-id="540f7-108">Download the UII SDK package (.exe), and extract it to find the USDDefaultSchema.xml file in the UII\USD Developer Assets\USD Configuration Tool Schema folder.</span></span>  
  
2. <span data-ttu-id="540f7-109">Double-click the DataMigrationUtility.exe file in the SDK\Tools\ConfigurationMigration folder to run the [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)], and choose **Export data** in the main screen.</span><span class="sxs-lookup"><span data-stu-id="540f7-109">Double-click the DataMigrationUtility.exe file in the SDK\Tools\ConfigurationMigration folder to run the [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)], and choose **Export data** in the main screen.</span></span>  
  
3. <span data-ttu-id="540f7-110">Trên màn hình **Đăng nhập**, cung cấp chi tiết xác thực để kết nối với [!INCLUDE[pn_microsoftcrm_server](../../includes/pn-microsoftcrm-server.md)] của bạn từ nơi mà bạn muốn xuất dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="540f7-110">On the **Login** screen, provide authentication details to connect to your [!INCLUDE[pn_microsoftcrm_server](../../includes/pn-microsoftcrm-server.md)] from where you want to export data.</span></span> <span data-ttu-id="540f7-111">Nếu bạn có nhiều tổ chức trên máy chủ [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], và muốn chọn tổ chức từ nơi xuất dữ liệu, chọn hộp kiểm **Luôn hiển thị danh sách tổ chức có sẵn**.</span><span class="sxs-lookup"><span data-stu-id="540f7-111">If you have multiple organizations on the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] server, and want to select the organization from where to export the data, select the **Always display list of available orgs** check box.</span></span> <span data-ttu-id="540f7-112">Select **Login**.</span><span class="sxs-lookup"><span data-stu-id="540f7-112">Select **Login**.</span></span>  
  
4. <span data-ttu-id="540f7-113">Nếu bạn có nhiều tổ chức và muốn chọn tổ hộp kiểm **luôn hiển thị danh sách tổ chức có sẵn**, màn hình tiếp theo cho phép bạn chọn tổ chức bạn muốn kết nối.</span><span class="sxs-lookup"><span data-stu-id="540f7-113">If you have multiple organizations, and you selected the **Always display list of available orgs** check box, the next screen lets you choose the organization that you want to connect to.</span></span> <span data-ttu-id="540f7-114">Chọn một [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] tổ chức để kết nối.</span><span class="sxs-lookup"><span data-stu-id="540f7-114">Select a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] organization to connect to.</span></span>  
  
5. <span data-ttu-id="540f7-115">Trên màn hình kế tiếp, hãy chọn tệp giản đồ dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mặc định (USDDefaultSchema.xml) để sử dụng cho việc xuất dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="540f7-115">On the next screen, select the default [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration data schema file (USDDefaultSchema.xml) to be used for the data export.</span></span>  
  
6. <span data-ttu-id="540f7-116">Chỉ định tên và vị trí của tệp dữ liệu để được xuất.</span><span class="sxs-lookup"><span data-stu-id="540f7-116">Specify the name and location of the data file to be exported.</span></span>  
  
7. <span data-ttu-id="540f7-117">Choose **Export Data**.</span><span class="sxs-lookup"><span data-stu-id="540f7-117">Choose **Export Data**.</span></span> <span data-ttu-id="540f7-118">Màn hình hiển thị trạng thái quá trình xuất và vị trí của tệp đã xuất ở dưới cùng của màn hình sau khi đã xuất xong.</span><span class="sxs-lookup"><span data-stu-id="540f7-118">The screen displays the export progress status and the location of the exported file at the bottom of the screen once the export is complete.</span></span>  
  
8. <span data-ttu-id="540f7-119">Choose **Exit** to close the tool.</span><span class="sxs-lookup"><span data-stu-id="540f7-119">Choose **Exit** to close the tool.</span></span>  
  
## <a name="next-step"></a><span data-ttu-id="540f7-120">Bước tiếp theo</span><span class="sxs-lookup"><span data-stu-id="540f7-120">Next Step</span></span>  
 [<span data-ttu-id="540f7-121">Import Unified Service Desk configuration data</span><span class="sxs-lookup"><span data-stu-id="540f7-121">Import Unified Service Desk configuration data</span></span>](../../unified-service-desk/admin/import-unified-service-desk-configuration-data.md)  
  
## <a name="see-also"></a><span data-ttu-id="540f7-122">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="540f7-122">See also</span></span>  
 [<span data-ttu-id="540f7-123">Migrate your Unified Service Desk configuration to another Dynamics 365 for Customer Engagement server</span><span class="sxs-lookup"><span data-stu-id="540f7-123">Migrate your Unified Service Desk configuration to another Dynamics 365 for Customer Engagement server</span></span>](../../unified-service-desk/admin/migrate-unified-service-desk-configuration-dynamics-365-server.md)
