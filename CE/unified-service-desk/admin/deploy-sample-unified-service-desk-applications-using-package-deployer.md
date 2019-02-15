---
title: Deploy sample Unified Service Desk for Dynamics 365 for Customer Engagement applications using Package Deployer | MicrosoftDocs
description: Learn how to use Package Deployer to import a Unified Service desk sample application.
keywords: ''
ms.date: 08/17/2018
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
ms.assetid: fe906d8e-a06b-46e6-84c9-0c0710157b33
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
ms.openlocfilehash: ce18861585803fe8ceefcbc86204c4872c722d0d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382493"
---
# <a name="overview-of-package-deployer-and-the-sample-applications"></a>Overview of Package Deployer and the sample applications
[!INCLUDE[pn_unified_service_desk_for_crm](../../includes/pn-unified-service-desk-for-crm.md)] comes with  sample applications that you can use as the base for starting with your configuration of your agent application.  

 These sample applications are bundled as packages that need to be deployed on a [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps instance before you can start working. Sau khi triển khai, quá trình triển khai mà được thực hiện bằng cách sử dụng [!INCLUDE[pn_package_deployer_long](../../includes/pn-package-deployer-long.md)], các thực thể và tùy chỉnh mã cụ thể cho [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] trở thành có sẵn trong phiên bản [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].  

> [!IMPORTANT]
> - The sample applications are not supported for production use.  
>   - Only one [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] package can be deployed in a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance to avoid any loss or overlap of functionality. Nếu bạn muốn cài đặt một gói [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] khác, loại bỏ gói hiện tại và sau đó cài đặt các gói phần mềm khác. For information about removing an existing [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] package, see [Remove a sample Unified Service Desk package](../../unified-service-desk/admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md#Remove).  
>   - Before deploying a [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] package on a Production instance, ensure that you test the package on a pre-Production instance, preferably a mirror image of the Production instance. Also, be sure to back up the Production instance before deploying the package.  
>   - Bạn cũng có thể sử dụng [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] lệnh ghép ngắn cho [!INCLUDE[pn_package_deployer_short](../../includes/pn-package-deployer-short.md)] để triển khai gói. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Deploy packages using CRM Package Deployer and Windows PowerShell](/dynamics365/customer-engagement/admin/deploy-packages-using-package-deployer-windows-powershell)  


<a name="twodot1apps"></a>   
## <a name="unified-service-desk-sample-applications"></a>Unified Service Desk sample applications  
 [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] comes with these sample application packages.  


|                                                                          Ứng dụng mẫu                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    Mô tả                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                       [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] - Upgrade                                        | This sample application package will upgrade an existing [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] solution where:.<br /><br /> -   You want to upgrade an existing [!INCLUDE[pn_unified_service_desk_20](../../includes/pn-unified-service-desk-20.md)] solution without affecting the existing configuration data.<br />-   You want to install a new [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] solution that doesn't include a sample configuration in an environment where no [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] solution is currently installed. **Note:**  Because there are no sample configurations included with the Upgrade sample application, when you install this sample application in an environment that does not already have a [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] solution configured, you must  provide a configuration to make it useful. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Core concepts for configuring Unified Service Desk](../../unified-service-desk/core-concepts-for-configuring-unified-service-desk.md) |
|                                   [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] - New Environment                                    |                                                                                                                                                                                                                                                                 This sample application package can be used to help accelerate setting up the new development environment for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. Install this package in a [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps non-production organization that does not have an existing [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] solution configured or sample application installed. For more information about the scenarios supported in this sample application, see [Unified Service Desk New Environment sample package](../../unified-service-desk/admin/unified-service-desk-new-environment-package.md).                                                                                                                                                                                                                                                                  |
|                               [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] - Interactive Service Hub                                |                                                                                                                                Interactive Service Hub provides an intuitive interface to simplify the day-to-day job for customer support agents. Interactive Service Hub displays all the vital information related to customers in one place and lets customer support agents focus on things that require attention. Interactive Service Hub is available with [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] and [!INCLUDE[pn_crm_2016](../../includes/pn-crm-2016.md)] (on-premises) or later.      For more information about the scenarios supported in this sample application, see [Unified Service Desk Interactive Service Hub package](../../unified-service-desk/admin/unified-service-desk-interactive-service-hub-package.md ).<br /><br /> This sample application package contains the solutions and sample configuration data, which demonstrates how you can integrate Interactive Service Hub with [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].                                                                                                                                |
|                                      [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] - Web Client                                      |                                                                                                                                                                                                                                                                                                         The sample application package demonstrates customer service scenarios that can be delivered using [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and Microsoft Dynamics CRM 2013 or later. This sample helps administrators and system customizers understand the configurability of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. For more information about the scenarios supported in this sample application, see [Unified Service Desk 365 Web Client package](../../unified-service-desk/admin/unified-service-desk-dynamics-365-web-client-package.md).                                                                                                                                                                                                                                                                                                          |
|                                  [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] - Unified Interface                                   |                                                                                                                                                                                                                                                                                                                                                                        This sample package contains the core User Interface Integration (UII) and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] solutions. It helps you to integrate Unified Interface apps with [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] environment. For more information about the scenarios supported in this sample application, see [Unified Service Desk 365 Unified Interface package](../../unified-service-desk/admin/unified-service-desk-dynamics-365-unified-interface-package.md)<br><br> **Note:** The Unified Interface sample application is available for use from [!INCLUDE[pn-unified-service-desk-3-3](../../includes/pn-unified-service-desk-3-3.md)].                                                                                                                                                                                                                                                                                                                                                                         |
| [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] - [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] |                                                                                                          This sample package contains the core User Interface Integration (UII) and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] - [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] solutions. [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] analyzes the compliance of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] with best practice rules in certain categories. The [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] displays the results of analysis in the form of a report with severity levels, description of the parameter, and mitigation for the non-compliant rules.<br><br> **Note:** This package is available separately for [!INCLUDE [pn-unified-service-desk-3-2](../../includes/pn-unified-service-desk-3-2.md)] or lower versions until [!INCLUDE [pn-unified-service-desk-2-2](../../includes/pn-unified-service-desk-2-2.md)].                                                                                                          |

<a name="Deploy"></a>   
## <a name="deploy-a-sample-unified-service-desk-package-using-package-deployer"></a>Deploy a sample Unified Service Desk package using Package Deployer  

1. [Download](http://go.microsoft.com/fwlink/p/?LinkID=872261) the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] package file from the [!INCLUDE[pn_Microsoft_Download_Center](../../includes/pn-microsoft-download-center.md)], and save it on your computer.  

2. Chạy các tập tin đã tải về để trích xuất nội dung vào một thư mục.  

3. Sau khi các tập tin được trích xuất, [!INCLUDE[pn_package_deployer_tool](../../includes/pn-package-deployer-tool.md)] bắt đầu tự động. If it doesn’t, navigate to the \<*ExtractedFolder*>\USDPackageDeployer folder, and double-click the PackageDeployer.exe file to run the [!INCLUDE[pn_package_deployer_tool](../../includes/pn-package-deployer-tool.md)].  

4. Trong màn hình giới thiệu của [!INCLUDE[pn_package_deployer_tool](../../includes/pn-package-deployer-tool.md)], chọn **Tiếp tục**.  

5. In the **Connect to Microsoft Dynamics 365 for Customer Engagement apps** screen, provide authentication details to connect to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance where you want to deploy the package. Nếu bạn có nhiều tổ chức và muốn chọn tổ chức nơi bạn muốn triển khai gói [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], chọn hộp kiểm **Hiển thị danh sách tổ chức hiện có**. Chọn **Đăng nhập**.  

   ![Dynamics 365 for Customer Engagement apps authentication details sign-in](../../unified-service-desk/media/usd-package-deployer-1.PNG "Dynamics 365 for Customer Engagement apps authentication details sign-in")  

6. Nếu bạn có nhiều tổ chức và muốn chọn tổ chức bạn muốn kết nối trong bước trước, màn hình tiếp theo hiển thị danh sách tổ chức. Chọn một [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] tổ chức để kết nối và tiến hành.  

7. Xác thực thành công, màn hình kế tiếp sẽ hiển thị các gói có sẵn để triển khai. Đọc mô tả để xác định gói mà bạn muốn triển khai, chọn gói rồi chọn **Tiếp theo**.  

8. Màn hình kế tiếp sẽ hiển thị các thông tin chi tiết về gói đã chọn và những điều mà sẽ được cài đặt trên phiên bản [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] của bạn. Xem lại thông tin và chọn **Tiếp**.  

9. Màn hình **đã sẵn sàng để cài đặt** hiển thị các gói phần mềm được chọn để triển khai và tên của tổ chức [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] nơi nó sẽ được bố trí đến. Xem lại thông tin và chọn **Tiếp**.

   ![Package Ready](../../unified-service-desk/media/usd-package-deployer-2.png "Package Ready")

10. Màn hình kế tiếp sẽ hiển thị tình trạng xác nhận của các gói phần mềm được lựa chọn để được triển khai. Sau khi hoàn thành xác nhận thành công, chọn **Tiếp**. 

11. Trang tiếp theo Hiển thị tình trạng triển khai gói. You can choose the log link at the bottom-left corner of the screen to view the package deployment log file, PackageDeployer.log. For more information about logging, see [Troubleshoot package deployment issues using log files](../../unified-service-desk/admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md#Logfiles) later in this topic. Một thông báo xác nhận được hiển thị khi triển khai thành công gói. Bấm vào **tiếp theo**.  

    ![Package deployment status](../../unified-service-desk/media/usd-package-deployer-5.png "Package deployment status")  

12. Màn hình kế tiếp sẽ hiển thị tên và thông tin về các gói phần mềm mà bạn cần triển khai. Xem lại thông tin và chọn **Hoàn thành** để thoát khỏi [!INCLUDE[pn_package_deployer_tool](../../includes/pn-package-deployer-tool.md)].  

<a name="Remove"></a>   
## <a name="remove-a-sample-unified-service-desk-package"></a>Gỡ bỏ một gói Unified Service Desk mẫu  
 Khi bạn triển khai gói [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mẫu trong tổ chức [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], ba giải pháp quản lý sau được tạo ra:

- UiiforMicrosoftDynamicsCRM  

- DynamicsUnifiedServiceDesk  

- USD<em>\<PackageName></em>Customization, where *\<PackageName>* is the name of the package that you deployed.  

  Nếu bạn muốn triển khai gói [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] mẫu, bạn trước tiên phải loại bỏ ba giải pháp. Để thực hiện điều này:  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  

2. On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement apps**, and then choose **Settings**.  

3. Choose **Settings** > **Solutions**.  

4. Trên trang Giải pháp, chọn một trong các giải pháp bằng cách chọn giải pháp, rồi chọn **Xóa**. Bạn sẽ được nhắc để xác nhận gỡ bỏ cài đặt giải pháp quản lý. Chọn **OK** để tiếp tục.  

   > [!NOTE]
   >  You can’t remove the UiiforMicrosoftDynamicsCRM solution before you remove the DynamicsUnifiedServiceDesk solution because some of the components in the DynamicsUnifiedServiceDesk solution depend on the components in the UiiforMicrosoftDynamicsCRM solution.  

5. Sau khi giải pháp được xóa, lặp lại các bước cho hai giải pháp khác để xóa chúng.  

<a name="Logfiles"></a>   
## <a name="troubleshoot-package-deployment-issues-using-log-files"></a>Khắc phục sự cố các vấn đề triển khai gói bằng cách sử dụng tệp nhật ký  
 The [!INCLUDE[pn_package_deployer_tool](../../includes/pn-package-deployer-tool.md)] provides logging support to record detailed information about errors that can occur while signing in to the [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps instance using the tool and deploying packages. There are three log files generated by the tool that are available at the following location on the computer where you run the tool: c:\Users\\*\<UserName>* \AppData\Roaming\Microsoft\PackageDeployer\\*\<Version>*.  

- **Login_ErrorLog.log**: This provides information about the issues that occurred while signing in to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] apps instance using the tool. Nếu có bất kỳ vấn đề trong khi đăng nhập, một tin nhắn sẽ xuất hiện trên màn hình đăng nhập của công cụ này với một liên kết đến tập tin đăng nhập nói rằng một lỗi đã xảy ra trong khi thực hiện yêu cầu đăng nhập và người dùng có thể xem Nhật ký lỗi. Bạn có thể chọn liên kết trong thông báo để xem tệp nhật ký này. Tệp nhật ký được tạo ra lần đầu tiên gặp bất kỳ sự cố đăng nhập nào vào công cụ. Sau đó, tệp nhật ký ghi lại các thông tin về bất kỳ vấn đề đăng nhập.  

- **PackageDeployer.log**: This provides detailed information about each task performed in the tool during the deployment of the packages. Bạn có thể xem các tệp nhật ký từ công cụ bằng cách chọn liên kết **Xem tệp nhật ký** ở dưới cùng của màn hình.  

- **ComplexImportDetail.log**: This provides detailed information about the data imported in the last deployment using the tool. Each time you deploy a package using this tool, the existing details from the log file are moved to a file called CompelxImportDetail._old.log in the same directory, and the ComplexImportDetail.log file displays information about the latest import done using the tool.  

<a name="PostDeployment"></a>   
## <a name="post-deployment-step-for-the-package"></a>Post-deployment step for the package  
 If you have deployed the **Customer Service Hub** package, you must manually activate the following records in the **Service Management** area (**Settings** > **Service Management**) that are created by the package:  

|Thực thể|Hồ sơ phải được kích hoạt|  
|------------|-----------------------------|  
|Thỏa thuận cấp độ dịch vụ|-   Premium Customer SLA<br />-   Woodgrove Default SLA<br /><br /> Đặt **SLA mặc định Woodgrove** làm mặc định.|  
|Quyền được hưởng|-   Premium Entitlement<br />-   Standard Entitlement<br /><br /> Kích hoạt mỗi quyền lợi tại một thời điểm.|  
|Bộ quy tắc định tuyến|Quy tắc Định tuyến|  
|Quy tắc tạo trường hợp tự động|Email đến nguyên tắc trường hợp|  

 The **Customer Service Hub** package also creates sample queue, customer service schedule, and holiday schedule records.  


## <a name="see-also"></a>Xem thêm  
 [Deploy packages using Dynamics 365 for Customer Engagement Package deployer and Windows PowerShell](/dynamics365/customer-engagement/admin/deploy-packages-using-package-deployer-windows-powershell)   
 [Install and Deploy Unified Service Desk](../../unified-service-desk/admin/install-upgrade-deploy-unified-service-desk.md)   

