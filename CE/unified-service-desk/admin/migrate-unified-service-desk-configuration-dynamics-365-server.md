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
# <a name="migration-of-a-unified-service-desk-configuration"></a><span data-ttu-id="4b4fa-103">Migration of a Unified Service Desk configuration</span><span class="sxs-lookup"><span data-stu-id="4b4fa-103">Migration of a Unified Service Desk configuration</span></span> 
<span data-ttu-id="4b4fa-104">Sau khi bạn đã hoàn thành phát triển hoặc cấu hình ứng dụng tổng đài viên của bạn, bạn có thể muốn di chuyển dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mới nhất của bạn từ môi trường phát triển hoặc thử nghiệm của bạn tới môi trường sản xuất của bạn.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-104">After you have completed the development or configuration of your agent application, you might want to migrate your latest [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration data from your development or testing environment to your production environment.</span></span> <span data-ttu-id="4b4fa-105">Migrating your data involves exporting your existing configuration data from the source [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance, and then importing it into the target [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-105">Migrating your data involves exporting your existing configuration data from the source [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance, and then importing it into the target [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.</span></span>  
  
 <span data-ttu-id="4b4fa-106">To export your configuration data, you can use the [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)] and the default [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration data schema file (USDDefaultSchema.xml).</span><span class="sxs-lookup"><span data-stu-id="4b4fa-106">To export your configuration data, you can use the [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)] and the default [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration data schema file (USDDefaultSchema.xml).</span></span> <span data-ttu-id="4b4fa-107">The default schema file contains information about all the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] entities, relationships, and uniqueness definitions for each entity.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-107">The default schema file contains information about all the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] entities, relationships, and uniqueness definitions for each entity.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="4b4fa-108">[Export Unified Service Desk configuration data](../../unified-service-desk/admin/export-unified-service-desk-configuration-data.md)</span><span class="sxs-lookup"><span data-stu-id="4b4fa-108">[Export Unified Service Desk configuration data](../../unified-service-desk/admin/export-unified-service-desk-configuration-data.md)</span></span>  
  
 <span data-ttu-id="4b4fa-109">For more information about the [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)], see [Manage your configuration data](/dynamics365/customer-engagement/admin/manage-configuration-data).</span><span class="sxs-lookup"><span data-stu-id="4b4fa-109">For more information about the [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)], see [Manage your configuration data](/dynamics365/customer-engagement/admin/manage-configuration-data).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4b4fa-110">Tệp giản đồ dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mặc định không xuất thông tin người dùng từ hệ thống nguồn.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-110">The default [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration data schema file does not export user information from the source system.</span></span>  
> 
>  <span data-ttu-id="4b4fa-111">For records that include notes and attachments, including Customization Files (compressed folder), these items aren’t included in the record during the export.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-111">For records that include notes and attachments, including Customization Files (compressed folder), these items aren’t included in the record during the export.</span></span>  
  
 <span data-ttu-id="4b4fa-112">Để nhập dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] đã xuất vào phiên bản [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], bạn có thể thực hiện những cách sau:</span><span class="sxs-lookup"><span data-stu-id="4b4fa-112">To import the exported [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration data to a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance, you can do either of the following:</span></span>  
  
- <span data-ttu-id="4b4fa-113">**Sử dụng công cụ Configuration Migration**: các công cụ cũng cho phép bạn nhập dữ liệu cấu hình đã xuất.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-113">**Use the Configuration Migration tool**: The tool also enables you to import the exported configuration data.</span></span> <span data-ttu-id="4b4fa-114">Trước khi bạn làm điều đó mặc dù, bạn phải triển khai một trong gói [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mẫu để tạo ra các thực thể cơ bản trong phiên bản [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] đích.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-114">Before you do that though, you must deploy one of the sample [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] packages to create the underlying entities in the target [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="4b4fa-115">[Import configuration data using the Configuration Migration tool](../../unified-service-desk/admin/import-unified-service-desk-configuration-data.md#ConfigMigration)</span><span class="sxs-lookup"><span data-stu-id="4b4fa-115">[Import configuration data using the Configuration Migration tool](../../unified-service-desk/admin/import-unified-service-desk-configuration-data.md#ConfigMigration)</span></span>  
  
- <span data-ttu-id="4b4fa-116">**Use a custom package for Unified Service Desk**: Create a custom package for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to include the exported data along with the files in one of the sample [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] packages, and then deploy the custom package on the target [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance using the [!INCLUDE[pn_package_deployer_tool](../../includes/pn-package-deployer-tool.md)].</span><span class="sxs-lookup"><span data-stu-id="4b4fa-116">**Use a custom package for Unified Service Desk**: Create a custom package for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to include the exported data along with the files in one of the sample [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] packages, and then deploy the custom package on the target [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance using the [!INCLUDE[pn_package_deployer_tool](../../includes/pn-package-deployer-tool.md)].</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="4b4fa-117">[Import configuration data using a custom package for Unified Service Desk](../../unified-service-desk/admin/import-unified-service-desk-configuration-data.md#CustomPackage)</span><span class="sxs-lookup"><span data-stu-id="4b4fa-117">[Import configuration data using a custom package for Unified Service Desk](../../unified-service-desk/admin/import-unified-service-desk-configuration-data.md#CustomPackage)</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="4b4fa-118">[!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)] cung cấp hỗ trợ ghi nhật ký cho thông tin chi tiết về hồ sơ về:</span><span class="sxs-lookup"><span data-stu-id="4b4fa-118">The [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)] provides logging support to record detailed information about:</span></span>  
> 
> - <span data-ttu-id="4b4fa-119">Errors that can occur while signing in to the [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps instance using the tool.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-119">Errors that can occur while signing in to the [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps instance using the tool.</span></span>  
> - <span data-ttu-id="4b4fa-120">Activities performed by the tool during the schema definition and export and import of the configuration data.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-120">Activities performed by the tool during the schema definition and export and import of the configuration data.</span></span>  
> - <span data-ttu-id="4b4fa-121">Dữ liệu được nhập bằng cách sử dụng công cụ.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-121">Data that was imported using the tool.</span></span>  
> 
>   <span data-ttu-id="4b4fa-122">There are three log files generated by the tool that are available at the following location on the computer where you run the tool: c:\Users\\*\<UserName>* \AppData\Roaming\Microsoft\DataMigrationUtility\\*\<Version>*.[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)]</span><span class="sxs-lookup"><span data-stu-id="4b4fa-122">There are three log files generated by the tool that are available at the following location on the computer where you run the tool: c:\Users\\*\<UserName>* \AppData\Roaming\Microsoft\DataMigrationUtility\\*\<Version>*.[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)]</span></span> [<span data-ttu-id="4b4fa-123">Gỡ rối các vấn đề di chuyển dữ liệu cấu hình bằng cách sử dụng tệp nhật ký</span><span class="sxs-lookup"><span data-stu-id="4b4fa-123">Troubleshoot configuration data migration issues using log files</span></span>](/dynamics365/customer-engagement/admin/manage-configuration-data#Logfiles)  
  
  
## <a name="see-also"></a><span data-ttu-id="4b4fa-124">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="4b4fa-124">See also</span></span>  
 [<span data-ttu-id="4b4fa-125">Xuất dữ liệu cấu hình của Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="4b4fa-125">Export Unified Service Desk configuration data</span></span>](../../unified-service-desk/admin/export-unified-service-desk-configuration-data.md)  
  
 [<span data-ttu-id="4b4fa-126">Nhập dữ liệu cấu hình Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="4b4fa-126">Import Unified Service Desk configuration data</span></span>](../../unified-service-desk/admin/import-unified-service-desk-configuration-data.md)  
