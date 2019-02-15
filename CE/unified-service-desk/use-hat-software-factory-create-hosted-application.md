---
title: Use HAT Software Factory to create a hosted application in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn how to HAT Software Factory to create a hosted application in Unified Service Desk.
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
ms.assetid: 71395c77-168d-4047-9c70-e50b0e974025
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: b4e2fb9edb3225dde2dbe1d01c08e59c33e80265
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387573"
---
# <a name="use-hat-software-factory-to-create-a-hosted-application-in-unified-service-desk"></a>Use HAT Software Factory to create a hosted application in Unified Service Desk

Nhà máy Phần mềm [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)] cung cấp cho bạn các mẫu [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] để đặt cấu hình [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] được lưu trữ, web hoặc ứng dụng [!INCLUDE[pn_Java](../includes/pn-java.md)] và làm cho chúng sẵn có cho máy tính để bàn [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] (chẳng hạn như [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]). Để sử dụng Nhà máy Phần mềm [!INCLUDE[pn_hat](../includes/pn-hat.md)], trước tiên bạn phải cài đặt ứng dụng.  

<a name="Install"></a>   
## <a name="install-hat-software-factory"></a>Cài đặt Nhà máy Phần mềm HAT  

1. Ensure that you have [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] installed. HAT supports [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] 2015, [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] 2012, and [!INCLUDE[pn_Visual_Studio_2010_short](../includes/pn-visual-studio-2010-short.md)].  

2. [Tải xuống và giải nén gói UII SDK](http://go.microsoft.com/fwlink/p/?LinkId=395257). In the extracted folder, navigate to the UII\Templates folder to locate the HAT software plug-in for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)]: `Microsoft.Uii.Tools.Inspector.vsix`.  

3. Bấm đúp vào tệp `Microsoft.Uii.Tools.Inspector.vsix` để cài đặt plug-in phần mềm HAT cho [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].  

<a name="Create"></a>   
## <a name="create-a-hat-hosted-application-project"></a>Tạo một dự án ứng dụng được lưu trữ bởi HAT  
 Cài đặt Nhà máy Phần mềm HAT sẽ tạo các mẫu dự án mới trong [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] cho phép bạn tạo các ứng dụng được lưu trữ có thể sử dụng tự động hóa HAT.  

1. Bắt đầu [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] và tạo một dự án mới.  

2. Trong hộp thoại **Dự án Mới**, từ danh sách các mẫu đã cài đặt ở bên trái, mở rộng **Visual C#** và chọn:  

   1. **UII** > **External Application**:  Create a project with basic initialization string (Initstring.xml) file for an external application.  

   2. **UII** > **Web Application**:  Create a project with basic initialization string (Initstring.xml) for a web application.  

      Trong chủ đề này, bạn sẽ tạo một ứng dụng web.  

   ![HAT Bing search](../unified-service-desk/media/usd-hat-bing-search.PNG "HAT Bing search")  

3. Specify the name and location of the project, and click **OK**.  

4. Bạn được nhắc nhập URL cho ứng dụng web của mình. Type the URL, and then click **OK**.  

   ![Application properties for Bing](../unified-service-desk/media/usd-bing-url.PNG "Application properties for Bing")  

    This creates a web application project with an initialization string (Initstring.xml) that contains information about your web application URL, adapter info, and data bindings. Đây là thông tin cơ bản và sẽ cập nhật khi bạn đặt cấu hình ứng dụng được lưu trữ của mình với tự động hóa và liên kết.  

5. Tiếp theo, đặt cấu hình ứng dụng bằng cách sử dụng một trong các tùy chọn sau bằng cách bấm chuột phải vào tên dự án và chọn một tùy chọn từ menu phím tắt.  

   ![Use the shortcut menu to configure](../unified-service-desk/media/usd-create-hat-control-11.png "Use the shortcut menu to configure")  


   |             Tùy chọn             |                                                                                                                                                                             Mô tả                                                                                                                                                                             |
   |--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |          **Kiểm tra**           |                                                     Bắt đầu Kiểm tra UII để kiểm tra các kiểm soát ứng dụng. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Using UII inspector to create bindings](../unified-service-desk/use-uii-inspector-create-bindings-hosted-application.md)                                                      |
   | **Kiểm tra là Người dùng Khác**  |                                                                                                                                                          Bắt đầu Trình kiểm tra UII bằng các thông tin đăng nhập khác nhau.                                                                                                                                                           |
   | **Cấu hình  Ứng dụng** |                                                                             Cấu hình ứng dụng kiểm soát tổ chức. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configure the HAT application](../unified-service-desk/configure-hosted-application.md)                                                                              |
   |    **Cấu hình Hành động**    |                                                                Cấu hình một hành động cho ứng dụng HAT. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configuring an action for the HAT application](../unified-service-desk/configure-action-hosted-application.md)                                                                 |
   |           **Triển khai**           | Deploy the hosted control application configuration to the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Deploy and import an application configuration to or from a Dynamics 365 for Customer Engagement server](../unified-service-desk/deploy-hosted-application-unified-service-desk.md) |

   > [!NOTE]
   >  Khi sử dụng **Kiểm tra với tư cách một Người dùng khác** cho một ứng dụng dựa trên Windows với các quyền truy cập khác nhau, Trình kiểm tra UII đôi khi có thể không kiểm tra các kiểm soát. Trong những trường hợp này, hãy đảm bảo rằng [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] và ứng dụng đích chạy với cùng đặc quyền và bạn sử dụng tùy chọn **Kiểm tra** thay vì **Kiểm tra với tư cách Người dùng khác**. Tùy chọn này không khả dụng cho các ứng dụng web.  
   > 
   >  Trong khi kiểm tra ứng dụng với chức năng **Kiểm tra với tư cách Người dùng khác**, nếu ứng dụng sử dụng phương pháp lưu trữ `Set Parent`, liên kết ứng dụng có thể gặp lỗi. Trong khi sử dụng phương pháp `Set Parent`, bạn phải chọn `Use FindWindow` trong phần `Alternate Top-Level window` và chỉ định `Caption` và `Class` cho cửa sổ ứng dụng.  

6. Save your project, and build it (**Build** > **Build Solution**). After the project is built successfully, an assembly (Bing_Search.dll) is generated in the \bin\debug folder of your project folder. Cụm này sau đó sẽ được sử dụng khi triển khai ứng dụng.  

### <a name="see-also"></a>Xem thêm  
 [Using UII inspector to create bindings](../unified-service-desk/use-uii-inspector-create-bindings-hosted-application.md)   
 [Configure the hosted application](../unified-service-desk/configure-hosted-application.md)   
 [Configure an action for the hosted application](../unified-service-desk/configure-action-hosted-application.md)   
 [Deploy the hosted application to Unified Service Desk](../unified-service-desk/deploy-hosted-application-unified-service-desk.md)   
 [Import the hosted application from Unified Service Desk](../unified-service-desk/import-hosted-application-from-unified-service-desk.md)
