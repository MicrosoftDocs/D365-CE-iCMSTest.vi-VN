---
title: Import Unified Service Desk for Dynamics 365 for Customer Engagement apps configuration data | MicrosoftDocs
description: Learn how configuration data can be imported in to a target Dynamics 365 for Customer Engagement apps instance.
ms.custom:
- dyn365-USD, dyn365-admin
ms.date: 10/29/2018
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
ms.assetid: 5fac5524-0f6b-4e8d-a43d-81626e33421a
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
ms.openlocfilehash: d2c28c8242b6dcf2ccaa786ee2df9a596b042a1e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382411"
---
# <a name="about-configuration-data"></a>About configuration data
You can import the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configuration data to the target [!INCLUDE[pn_microsoftcrm_server](../../includes/pn-microsoftcrm-server.md)] by using either of the following ways:  
  
- Sử dụng [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)]  
  
- Tạo một gói tùy chỉnh cho [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] có chứa dữ liệu cấu hình đã xuất  
  
  Trước khi bạn có thể nhập dữ liệu cấu hình cho hệ thống đích, hãy chắc chắn rằng bạn đã xuất [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] dữ liệu cấu hình từ hệ thống nguồn của bạn. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Export Unified Service Desk configuration data](../../unified-service-desk/admin/export-unified-service-desk-configuration-data.md)  
  
<a name="ConfigMigration"></a>   
## <a name="import-configuration-data-by-using-the-configuration-migration-tool"></a>Nhập dữ liệu cấu hình bằng cách sử dụng công cụ Configuration Migration  
  
1. Đảm bảo rằng phiên bản [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] nơi bạn đang di chuyển dữ liệu cấu hình đã triển khai gói [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] theo yêu cầu. Nếu không, triển khai gói [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mẫu. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Deploy sample Unified Service Desk applications to Dynamics 365 for Customer Engagement server using Package Deployer](../../unified-service-desk/admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md)  
  
2. Chạy [!INCLUDE[pn_configuration_migration_tool](../../includes/pn-configuration-migration-tool.md)], và bấm vào **nhập dữ liệu** trong màn hình chính. For information about downloading the tool, see step 1 in [Export Unified Service Desk configuration data](../../unified-service-desk/admin/export-unified-service-desk-configuration-data.md).  
  
3. Trên màn hình **Đăng nhập**, cung cấp chi tiết xác thực để kết nối với máy chủ [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] của bạn từ nơi mà bạn muốn xuất dữ liệu. Nếu bạn có nhiều tổ chức trên máy chủ [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], và muốn chọn tổ chức từ nơi xuất dữ liệu, chọn hộp kiểm **Luôn hiển thị danh sách tổ chức có sẵn**. Bấm vào **đăng nhập**.  
  
4. Nếu bạn có nhiều tổ chức và muốn chọn tổ hộp kiểm **luôn hiển thị danh sách tổ chức có sẵn**, màn hình tiếp theo cho phép bạn chọn tổ chức bạn muốn kết nối. Chọn một [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] tổ chức để kết nối.  
  
5. Màn hình kế tiếp sẽ nhắc bạn để cung cấp các tập tin dữ liệu (.zip) để nhập. Duyệt tìm tệp dữ liệu, chọn tệp, sau đó bấm vào **Nhập dữ liệu**.  
  
6. Màn hình kế tiếp sẽ hiển thị tình trạng nhập hồ sơ của bạn. Nhập dữ liệu được thực hiện trong nhiều lần chuyển cho lần nhập dữ liệu nền tảng đầu tiên trong khi xếp hàng đợi dữ liệu phụ thuộc, và sau đó nhập dữ liệu phụ thuộc trong lần chuyển tiếp theo để xử lý bất kỳ quan hệ phụ thuộc dữ liệu hoặc mối liên kết. Điều này đảm bảo nhập dữ liệu thông suốt và thống nhất.  
  
7. Bấm vào **Thoát** để đóng công cụ.  
  
<a name="CustomPackage"></a>   
## <a name="import-configuration-data-by-using-a-custom-package-for-unified-service-desk"></a>Nhập dữ liệu cấu hình bằng cách sử dụng một gói tùy chỉnh cho Unified Service Desk  
 Bạn có thể xây dựng một gói tùy chỉnh để bao gồm các dữ liệu cấu hình mà bạn đã xuất từ phiên bản hiện tại của [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] của bạn. Để tạo ra một gói tùy chỉnh để triển khai [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] dữ liệu cấu hình, bạn sẽ sử dụng tất cả các tệp hiện có trong một trong các gói [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mặc định và thay thế dữ liệu cấu hình tiêu chuẩn bằng dữ liệu cấu hình [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] của bạn mà bạn đã xuất. You can create a custom package for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] using the [!INCLUDE[pn_sdk](../../includes/pn-sdk.md)] template for [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)].  
  
### <a name="before-you-begin"></a>Trước khi bạn bắt đầu  
  
- [Download the Unified Service Desk package](http://go.microsoft.com/fwlink/?LinkID=854761) (self-extracting executable file), and double-click the file to extract the contents. Bạn sẽ sử dụng các tập tin dưới một trong các gói mặc định để tạo ứng dụng mẫu. In this example, you’ll use the files under the Base package (*\<ExtractedFolder>* \USDPackageDeployer\BasePackage).  
  
- Ensure that you know the prerequisites and how to create a custom package by using the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] SDK template for [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)]. For detailed information about using template to create a package, see [Create packages for the Dynamics 365 for Customer Engagement Package deployer](https://msdn.microsoft.com/library/dn688182.aspx).  
  
- [Download the CRM SDK package](http://go.microsoft.com/fwlink/?LinkID=627298) (.exe file), and extract it to locate the `PackageDeployer` folder under the *\<ExtractedFolder>* \SDK\Tools\ folder. Thư mục này chứa các cụm cần thiết để tạo dự án tùy chỉnh bằng cách sử dụng [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)].  
  
- Install the template (CRMSDKTemplates.vsix) from the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] SDK package that you extracted in the previous step. Tập tin có sẵn trong thư mục SDK\Mẫu.  
  
### <a name="how-to-create-a-custom-package"></a>Cách để tạo gói tùy chỉnh  
  
1. Start [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)], and create a new project by using the **Dynamics 365 for Customer Engagement apps Package** template.  
  
   ![New project for creating a custom package](../../unified-service-desk/media/crm-sdkv6-packagedeployer-01.png "New project for creating a custom package")  
  
2. Trong ngăn **Trình khám phá giải pháp**, mở rộng **Thư mục Gói**, và xóa tệp **ImportConfig.xml**.  
  
3. Thêm tất cả các giải pháp hiện có, nhập cấu hình, và các tệp khác ngoại trừ tập tin dữ liệu cấu hình mặc định từ một trong các gói [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mặc định vào dự án [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)]. Trong ví dụ này, chúng tôi sẽ sử dụng các gói phần mềm cơ sở. Add the following files from the *\<ExtractedFolder>* \USDPackageDeployer\BasePackage folder to **PkgFolder** in your [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)] solution:  
  
   -   DynamicsUnifiedServiceDesk_1_0_managed.zip  
  
   -   ImportConfig.xml  
  
   -   UII Option.csv  
  
   -   UiiforMicrosoftDynamicsCRM3_0_managed.zip  
  
   -   UIIOption.xml  
  
   -   UsdBaseCustomization_1_0_managed.zip  
  
4. Thêm tập tin dữ liệu cấu hình (.zip) mà bạn đã xuất trước đó từ phiên bản sẵn có của [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] của bạn.  
  
5. Với mỗi tập tin bạn đã thêm trong thư mục **Thư mục gói**, trong ngăn **thuộc tính**, đặt giá trị **sao chép vào thư mục đầu ra** thành **Luôn sao chép**. Điều này đảm bảo rằng các tập tin bạn đã thêm có sẵn trong các gói phần mềm được tạo ra.  
  
   ![Copy to output directory field](../../unified-service-desk/media/crm-itpro-usd-custompackage.PNG "Copy to output directory field")  
  
6. Nhấp đúp vào tệp **ImportConfig.xml** trong **Thư mục gói** để sửa. Cập Nhật giá trị của tham số `crmmigdataimportfile` để khớp tên của tập tin được xuất (.zip) mà bạn đã thêm ở bước 5.  
  
7. Nhấp đúp vào tệp **PackageTemplate.cs** để cập nhật tên gói và mô tả. For detailed information about this, see [Create packages for the Dynamics 365 for Customer Engagement Package deployer](https://msdn.microsoft.com/library/dn688182.aspx) in the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] SDK help.  
  
8. Save your project, and then build it (**Build** > **Build Solution**) to create the package. All the contents in the *\<Project>* \Bin\Debug folder are your package. Note that an assembly file (.dll) is created with the same name as your [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)] project name; this file contains the custom code that you created in the previous step.  
  
9. Copy the entire contents from your [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)] project debug folder (*\<Project>* \Bin\Debug) to the **PackageDeployer** folder, that is, at the same location as the **PackageDeployer.exe** file. Bạn sẽ được nhắc để thay thế một số tập tin; chấp nhận xác nhận để thay thế các tập tin trong thư mục [!INCLUDE[pn_package_deployer_tool](../../includes/pn-package-deployer-tool.md)].  
  
10. Sau khi sao chép tệp, chạy công cụ bằng cách bấm đúp vào tệp **PackageDeployer.exe**.  
  
11. Bạn sẽ được nhắc để xác định các thông tin đăng nhập của máy chủ [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] đích. Xác định các chi tiết và tiến hành.  
  
12. Trong màn hình lựa chọn gói, chọn gói tùy chỉnh của bạn để triển khai, và thực hiện theo các màn hình hướng dẫn triển khai các gói phần mềm.  
  
    [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Deploy sample Unified Service Desk applications to Dynamics 365 for Customer Engagement server using Package Deployer](../../unified-service-desk/admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md)  
  
## <a name="see-also"></a>Xem thêm  
 [Migrate your Unified Service Desk configuration to another Dynamics 365 for Customer Engagement server](../../unified-service-desk/admin/migrate-unified-service-desk-configuration-dynamics-365-server.md)   
 [Khắc phục sự cố Unified Service Desk](../../unified-service-desk/admin/troubleshoot-unified-service-desk.md)
