---
title: Create a CTI Connector | MicrosoftDocs
description: Learn about the CTI Connector component in your custom CTI adapter contains the logic to connect to and communicate with an external CTI system. CTI Connector consists of the ICtiControl interface, which includes the CtiHostedControl class containing methods and events that will be called and listened to by the CTI Desktop Manager component.
ms.custom:
- dyn365-USD
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
ms.assetid: dc647143-8e14-4bb3-ad6a-844f6fc63b33
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: f5b325ee3ef1552b5d444913f1b8f39da5c97e93
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386034"
---
# <a name="create-a-cti-connector"></a>Create a CTI Connector
The [!INCLUDE[pn_cti_connector](../includes/pn-cti-connector.md)] component in your custom CTI adapter contains the logic to connect to and communicate with an external CTI system. [!INCLUDE[pn_cti_connector](../includes/pn-cti-connector.md)] consists of the [ICtiControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.icticontrol) interface, which includes the [CtiHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.controls.ctihostedcontrol) class containing methods and events that will be called and listened to by the [!INCLUDE[pn_cti_desktop_manager](../includes/pn-cti-desktop-manager.md)] component.  

 [!INCLUDE[pn_cti_connector](../includes/pn-cti-connector.md)] hỗ trợ hai mô hình tương tác với hệ thống CTI:  

- Mô hình đầu tiên là hệ thống bỏ phiếu dựa trên dịch vụ. Trong mô hình này, nhà phát triển xác định kết nối dịch vụ lên nguồn tương tác CTI ngược và các cuộc thăm dò là nguồn gốc cho cập nhật và sự kiện. Mô hình này được ưa thích cho nguồn CTI cung cấp quyền truy cập vào các sự kiện và hành động CTI qua dịch vụ web. Trong mô hình này, phải xem xét ở mô hình phân luồng phù hợp để hỗ trợ liên lạc không đồng bộ với dịch vụ web CTI ngược.  

- Mô hình thứ hai sử dụng đối tượng phiên bản hoặc tĩnh sử dụng hệ thống thông báo sự kiện hoặc gọi lại. Mô hình này được ưa thích cho nguồn CTI cung cấp API. Như mô hình bỏ phiếu, cần cân nhắc cung cấp hỗ trợ không đồng bộ qua luồng để ngăn tác động đến [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  

  Khung UII CTI chỉ hỗ trợ một phiên bản của thành phần [!INCLUDE[pn_cti_connector](../includes/pn-cti-connector.md)].  

<a name="Define"></a>   
## <a name="define-a-cti-connector"></a>Xác định Kết nối CTI  
 [!INCLUDE[pn_cti_connector](../includes/pn-cti-connector.md)] implements the [ICtiControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.icticontrol) interface. To define a [!INCLUDE[pn_cti_connector](../includes/pn-cti-connector.md)], use the CRM SDK [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] project template. [Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)]. 

> [!NOTE]
>  The template works if you have [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] 4.5.2 and [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)], [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]. Additionally, you must have [!INCLUDE[tn_nuget_package_manager](../includes/tn-nuget-package-manager.md)] for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d).  

 Mẫu [!INCLUDE[pn_cti_connector](../includes/pn-cti-connector.md)] cung cấp sự kiện và phương pháp được ghép sẵn giúp bạn xác định [!INCLUDE[pn_cti_connector](../includes/pn-cti-connector.md)].  

<a name="Step1"></a>   
1. Bắt đầu Visual Studio và tạo một dự án mới.  

2. Trong hộp thoại **Dự án mới**:  

   1.  From the list of installed templates, expand **Visual C#**, and select **CRM SDK Templates** > **Unified Service Desk** > **USD CTI Connector**.  

   2.  Chỉ định tên và vị trí của dự án và bấm vào **OK**.  

   ![Create a USD CTI Connector](../unified-service-desk/media/usd-cti-connector.png "Create a USD CTI Connector")  

3. In **Solution Explorer**, right-click the CtiConnector.cs file, and select **View Code** to display the code.  

4. Triển khai các phương pháp và sự kiện được yêu cầu. For sample code that demonstrates how to create a [!INCLUDE[pn_cti_connector](../includes/pn-cti-connector.md)], [download and install the UII SDK](http://go.microsoft.com/fwlink/p/?LinkId=395257), and then browse to the UII\SampleCode\UII\CCA\Source Code\Cti Root folder. For more information about the methods and events to implement for a [!INCLUDE[pn_cti_connector](../includes/pn-cti-connector.md)], see the [ICtiControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.icticontrol) interface.  

5. Save your project, and build it (**Build** > **Build Solution**). After the project builds successfully, an assembly (.dll file) is generated with the same names as your project (unless you changed it in the project properties) in the \bin\debug folder of your project.  

   > [!NOTE]
   >  Lưu ý tên của lớp được sử dụng để xây dựng kiểm soát CTI trong tệp `CtiConnector.cs`. Bạn sẽ cần thông tin này trong bước tiếp theo.  

6. Copy this file to your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application installation directory (typically C:\Program Files\Microsoft Dynamics CRM USD\USD). Cần có tệp này để kiểm tra và sử dụng [!INCLUDE[pn_cti_connector](../includes/pn-cti-connector.md)] từ ứng dụng khách [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] của bạn.  

<a name="Configure"></a>   
## <a name="configure-a-hosted-control-for-cti-connector-in-unified-service-desk"></a>Đặt cấu hình kiểm soát tổ chức cho Trình quản lý CTI trong Unified Service Desk  
 Sau khi bạn đã xây dựng kiểm soát [!INCLUDE[pn_cti_connector](../includes/pn-cti-connector.md)], bạn phải đặt cấu hình kiểm soát trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  

> [!NOTE]
>  Dự án [!INCLUDE[pn_cti_connector](../includes/pn-cti-connector.md)] cũng cho phép bạn xác định thành phần [!INCLUDE[pn_cti_desktop_manager](../includes/pn-cti-desktop-manager.md)] của bạn. Bạn phải tạo hai kiểm soát tổ chức riêng biệt, mỗi kiểm soát cho [!INCLUDE[pn_cti_connector](../includes/pn-cti-connector.md)] và [!INCLUDE[pn_cti_desktop_manager](../includes/pn-cti-desktop-manager.md)], trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] sau khi bạn đã thêm mã cho kiểm soát sau trong [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Create a CTI Desktop Manager](../unified-service-desk/create-cti-desktop-manager.md)  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement apps** > **Settings** > **Unified Service Desk**.  

3. Trên trang **Unified Service Desk**, chọn **Kiểm soát Tổ chức**.  

4. Trên trang **Kiểm soát Tổ chức**, chọn **Mới**.  

5. On the **New Hosted Control** page, specify the following values  


   |         Trường         |                                                                                                                                                                              Value                                                                                                                                                                               |
   |-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |         Tên          |                                                                                                                                                                           CTIConnector                                                                                                                                                                           |
   |  USD Component Type   |                                                                                                                                                                      Ứng dụng được lưu trữ CCA                                                                                                                                                                      |
   |  Ứng dụng được lưu trữ   |                                                                                                                                                                          Kiểm soát được lưu trữ                                                                                                                                                                          |
   | Application is Global |                                                                                                                                                                             Đã kiểm tra                                                                                                                                                                              |
   |     Nhóm hiển thị     |                                                                                                                                                                           Bảng điều khiển bị ẩn                                                                                                                                                                            |
   |        Bộ điều hợp        |                                                                                                                                                                          Không sử dụng bộ điều hợp                                                                                                                                                                          |
   |     URI cụm tổ hợp      |                                                                                                                                        This is the name of the assembly file (.dll) that you built in the previous step.                                                                                                                                         |
   |     Loại cụm tổ hợp     | This is the name of the assembly file (.dll) followed by a dot, and then the class name of your [!INCLUDE[pn_cti_connector](../includes/pn-cti-connector.md)]. Ví dụ: nếu tên tệp .dll của bạn là `MyCtiConnector` và tên của lớp của dự án CTI của bạn là `CtiConnector`, hãy nhập giá trị sau vào trường này:  `MyCtiConnector.CtiConnector`. |


6. Chọn **Lưu** để tạo kiểm soát tổ chức.  

### <a name="see-also"></a>Xem thêm  
 [Create a CTI Desktop Manager](../unified-service-desk/create-cti-desktop-manager.md)   
 [Create a CTI Control](../unified-service-desk/create-cti-control.md)   
 [UII Computer Telephony Integration (CTI) framework](../unified-service-desk/uii-computer-telephony-integration-cti-framework.md)   
 [Walkthrough: Use generic listener adapter for CTI events](../unified-service-desk/walkthrough-use-the-generic-listener-adapter-for-cti-event-routing.md)
