---
title: Update Unified Service Desk for Dynamics 365 for Customer Engagement apps solution | MicrosoftDocs
description: Learn how to update Unified Service Desk for Dynamics 365 for Customer Engagement apps.
keywords: ''
ms.date: 08/23/2017
ms.service:
- dynamics-365-customerservice
ms.custom:
- dyn365-USD, dyn365-admin
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: d3773029-8b2f-4aa3-9317-abc309b01960
author: kabala123
ms.author: kabala
manager: shujoshi
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 136d722b61b02fb3d550c62610f63bf987dd1894
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382435"
---
# <a name="updating-the-solution"></a>Updating the solution
Read this topic only if you have an existing installation of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] from the previous release of [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps, and want to update to the [!INCLUDE[pn_crm_2016](../../includes/pn-crm-2016.md)] release.  
  
 Nếu bạn đang cài đặt [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] lần đầu tiên, bạn có thể bỏ qua chủ đề này.  
  
<a name="check"></a>   
## <a name="check-if-you-need-to-update-the-unified-service-desk-solution"></a>Check if you need to update the Unified Service Desk solution  
 Nếu bạn không chắc chắn cho dù bạn cần phải cập nhật cài đặt [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] của bạn, kiểm tra các phiên bản sau để chắc chắn.  
  
### <a name="check-the-unified-service-desk-solution-version"></a>Kiểm tra phiên bản giải pháp Unified Service Desk  
 In your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance, navigate to **[!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps** > **Settings** > **Solutions**. Nếu số phiên bản của các giải pháp phù hợp với những giải pháp trong bảng, bạn có phiên bản mới nhất của [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], và không cần phải Cập Nhật.  
  
|Tên Giải pháp|Phiên bản|  
|-------------------|-------------|  
|UiiForMicrosoftDynamicsCRM2011|4.0.0.xxx|  
|DynamicsUnifiedServiceDesk|4.0.0.xxx|
  
<a name="UpdateSolutions"></a>   
## <a name="update-unified-service-desk-solutions"></a>Cập nhật giải pháp Unified Service Desk  
 Before you update your [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] solutions, ensure that the version of your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] on-premises organization is [!INCLUDE[pn_crm_2016](../../includes/pn-crm-2016.md)], [!INCLUDE[pn_crm_2015_shortest](../../includes/pn-crm-2015-shortest.md)], or [!INCLUDE[pn_crm_2013_sp_shortest](../../includes/pn-crm-2013-sp-shortest.md)].  
  
1. [Download the Unified Service Desk package file](http://go.microsoft.com/fwlink/p/?LinkID=2007340) (CRM2016-8.x.x-USD-PackageDeployer.exe), and save it on your computer.  
  
2. Chạy các tập tin đã tải về để trích xuất nội dung vào một thư mục.  
  
3. Sau khi tệp được giải nén, nếu [!INCLUDE[pn_package_deployer_tool](../../includes/pn-package-deployer-tool.md)] bắt đầu tự động, hãy đóng lại.  
  
4. In the extracted folder, locate the following two solution files in the USDPackageDeployer\\*\<PackageName>* folder, where *\<PackageName>* is the name of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] package you currently have installed in your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance:  
  
   - UiiForMicrosoftDynamicsCRM_3_0_managed.zip  
  
   - DynamicsUnifiedServiceDesk_1_0_managed.zip 

   - UnifiedInterfaceDemoCustomization_1_0_managed.zip 
  
     Ví dụ, nếu bạn đã cài đặt gói cơ sở, bạn phải di chuyển vào thư mục USDPackageDeployer\BasePackage để tìm tập tin giải pháp cho việc Cập Nhật. Similarly, navigate to the USDPackageDeployer\CRM2013SP1Package folder if you have the [!INCLUDE[pn_crm_2013_sp_shortest](../../includes/pn-crm-2013-sp-shortest.md)] package, to the USDPackageDeployer\CRM2013SP1withProductUpdatesPackage folder if you have the [!INCLUDE[pn_crm_2013_sp_shortest](../../includes/pn-crm-2013-sp-shortest.md)] with Product Updates package, and USDPackageDeployer\ParatureKnowledgeManagementPackage folder if you have the Knowledge Management package.  
  
5. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  
  
6. Chuyển tới **Thiết đặt** > **Giải pháp**.   
  
7. Trên thanh công cụ **Hành động**, bấm **Nhập**.  
  
8. Browse to the UiiForMicrosoftDynamicsCRM_3_0_managed.zip file in the appropriate folder as explained in step 4, and select to import it to update the existing solution in your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.  
  
9. The next page will display a yellow bar saying **This solution package contains an update for a solution that is already installed**. Review the information about the solution, and click **Next**.  
  
10. On the next page, select the **Maintain customizations (recommended)** option and ensure that the **Enable any SDK message processing steps included in the solution** check box is selected. Bấm vào **tiếp theo**.  
  
     After the solution import completes successfully, the **UiiForMicrosoftDynamicsCRM** solution is updated.  
  
11. Repeat steps 7-10 for the DynamicsUnifiedServiceDesk_1_0_managed.zip and UnifiedInterfaceDemoCustomization_1_0_managed.zip file to update the **DynamicsUnifiedServiceDesk** and solution in your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance.  
  
     For detailed information about updating solutions in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], see [Import, update, and export solutions](/dynamics365/customer-engagement/customize/import-update-export-solutions).  
  
12. Trong [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], xác minh số phiên bản của giải pháp đã cập nhật với các giải pháp được liệt kê trong bảng trước đây để đảm bảo chúng là phiên bản mới nhất.  
  
13. Đóng phiên bản trình duyệt và đăng nhập một lần nữa vào [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] để xem các tính năng mới trong [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [What's new in Unified Service Desk for administrators](../../unified-service-desk/admin/whats-new-unified-service-desk-administrators.md).  
  
## <a name="see-also"></a>Xem thêm  
 [Connect to Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)   
 [Install and Deploy Unified Service Desk](../../unified-service-desk/admin/install-upgrade-deploy-unified-service-desk.md)   
