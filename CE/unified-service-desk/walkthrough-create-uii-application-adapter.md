---
title: 'Walkthrough: Create a UII Application Adapter in Unified Service Desk fopr Dynamics 365 for Customer Engagement| MicrosoftDocs'
description: Demonstrates how to host and interact with an external application in Unified Service Desk.
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
ms.assetid: f280285b-2284-40a8-a01d-ea24a65926c9
caps.latest.revision: 9
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: bd9292ad1011decbb1d808138ffd6498ca086aa6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388237"
---
# <a name="walkthrough-create-a-uii-application-adapter"></a>Walkthrough: Create a UII Application Adapter
You can create an application adapter if you want to integrate an external application with [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps provides a [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] template for creating an application adapter. Mẫu này cung cấp mã cơ bản như nhận xét để giúp bạn bắt đầu với việc tạo bộ chuyển đổi ứng dụng.  
  
 Trong cách này, bạn sẽ xây dựng một ứng dụng bên ngoài `QsExternalApp` và lưu trữ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Sau đó, bạn sẽ tạo và cấu hình bộ chuyển đổi ứng dụng được gọi là `ExternalApplicationAdapter` cho ứng dụng bên ngoài để tương tác với [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Ứng dụng bên ngoài có bốn nhãn: mỗi nhãn cho tên, họ, địa chỉ và ID của khách hàng và bốn hộp văn bản tương ứng để hiển thị các giá trị từ [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
## <a name="in-this-section"></a>In This Section  
 [Điều kiện tiên quyết](../unified-service-desk/walkthrough-create-uii-application-adapter.md#Prereq)  
  
 [Bước 1: Xây dựng ứng dụng bên ngoài mẫu](../unified-service-desk/walkthrough-create-uii-application-adapter.md#CreateExternalApp)  
  
 [Step 2: Configure the external application in Microsoft Dynamics 365 for Customer Engagement apps.](../unified-service-desk/walkthrough-create-uii-application-adapter.md#ConfigureExApp)  
  
 [Bước 3: Kiểm tra ứng dụng bên ngoài](../unified-service-desk/walkthrough-create-uii-application-adapter.md#TestExApp)  
  
 [Bước 4: Tạo bộ chuyển đổi ứng dụng](../unified-service-desk/walkthrough-create-uii-application-adapter.md#CreateAppAdapter)  
  
 [Step 5: Configure the application adapter in Microsoft Dynamics 365 for Customer Engagement apps](../unified-service-desk/walkthrough-create-uii-application-adapter.md#ConfigureAppAdapter)  
  
 [Bước 6: Thử nghiệm bộ chuyển đổi ứng dụng](../unified-service-desk/walkthrough-create-uii-application-adapter.md#TestAppAdapter)  
  
<a name="Prereq"></a>   
## <a name="prerequisites"></a>Điều kiện tiên quyết  
  
- [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] 4.5.2  
  
- [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application; required for testing the hosted control.  
  
- [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)], [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]  
  
- [!INCLUDE[tn_nuget_package_manager](../includes/tn-nuget-package-manager.md)] for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)  
  
- **CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the UII hosted control project template. [Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].  
  
<a name="CreateExternalApp"></a>   
## <a name="step-1-build-a-sample-external-application"></a>Bước 1: Xây dựng ứng dụng bên ngoài mẫu  
  
1. [Tải xuống gói UII SDK](http://go.microsoft.com/fwlink/p/?LinkId=519179).  
  
2. Double-click the package file to extract the contents.  
  
3. Navigate to the \<ExtractedFolder>\UII\SampleCode\UII\AIF\QsExternalApp folder, and open the Microsoft.Uii.QuickStarts.QsExternalApp.csproj file in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].  
  
4. Press F5 or choose **Debug** > **Start Debugging** to create a sample external application. The application (Microsoft.Uii.QuickStarts.QsExternalApp.exe) is created in the /bin/debug folder of the project.  
  
   ![Sample external app](../unified-service-desk/media/usd-sample-external-app.PNG "Sample external app")  
  
<a name="ConfigureExApp"></a>   
## <a name="step-2-configure-the-external-application-in-microsoft-dynamics-365-for-customer-engagement-apps"></a>Step 2: Configure the external application in Microsoft Dynamics 365 for Customer Engagement apps.  
 Trong bước này, bạn sẽ tạo kiểm soát tổ chức của loại **Ứng dụng Được lưu trữ Bên ngoài** để hiển thị ứng dụng biểu mẫu [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)].  
  
1. Đăng nhập vào **Microsoft Dynamics 365 for Customer Engagement**.  
  
2. Trên thanh điều hướng, bấm hoặc chạm vào **Microsoft Dynamics 365 for Customer Engagement**, rồi chọn **Thiết đặt**.  
  
3. Click or tap **Settings** > **Unified Service Desk** > **Hosted Controls**.  
  
4. Bấm vào **Mới**.  
  
5. On the **New Hosted Control** page, specify the following values:  
  
   |Trường|Value|  
   |-----------|-----------|  
   |Tên|QsExternalApp|  
   |Thành phần USD|CCA Hosted Application|  
   |Ứng dụng được lưu trữ|Ứng dụng được lưu trữ bên ngoài|  
   |Application is Global|Đã kiểm tra|  
   |Nhóm hiển thị|Bảng điều khiển chính|  
   |Bộ điều hợp|Use No Adapter|  
   |Application is Dynamic|Không|  
   |URI ứng dụng bên ngoài|Microsoft.Uii.QuickStarts.QsExternalApp.exe|  
  
   ![Application adapter configuration screen](../unified-service-desk/media/usd-external-app-config-1.PNG "Application adapter configuration screen")  
  
   ![Unified Service Desk external app hosting settings](../unified-service-desk/media/usd-externa-app-config-2.PNG "Unified Service Desk external app hosting settings")  
  
6. Bấm vào **Lưu**.  
  
<a name="TestExApp"></a>   
## <a name="step-3-test-the-external-application"></a>Bước 3: Kiểm tra ứng dụng bên ngoài  
  
1. Copy the application from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project output folder (\<ProjectFolder>\bin\debug) to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application directory. In this case, we will copy the Microsoft.Uii.QuickStarts.QsExternalApp.exefile to the C:\Program Files\Microsoft Dynamics CRM USD\USD directory.  
  
2. Run the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server.  
  
3. Trên lần đăng nhập thành công, bạn sẽ thấy nút **Ứng dụng Bên ngoài Mẫu** trên màn hình nền.  
  
4. Chọn **Ứng dụng Bên ngoài Mẫu** để xem ứng dụng bên ngoài được lưu trữ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
   ![Sample external app in Unified Service Desk](../unified-service-desk/media/usd-sample-external-app-1.PNG "Sample external app in Unified Service Desk")  
  
> [!NOTE]
>  Tại thời điểm này, các trường trống vì bạn chỉ lưu trữ ứng dụng trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Để điền các giá trị từ [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], bạn sẽ phải tạo bộ chuyển đổi ứng dụng như được mô tả trong bước tiếp theo.  
  
<a name="CreateAppAdapter"></a>   
## <a name="step-4-create-the-application-adapter"></a>Bước 4: Tạo bộ chuyển đổi ứng dụng  
  
1. Bắt đầu [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] và tạo một dự án mới.  
  
2. In the **New Project** dialog box:  
  
   1. From the list of installed templates, expand [!INCLUDE[pn_Visual_C#](../includes/pn-visual-csharp.md)], and select Dynamics 365 for Customer Engagement apps SDK Templates > **Unified Service Desk** > [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] Application Adapter  
  
   2. Specify the name and location of the project, and click **OK** to create a new project.  
  
   ![External application adapter in Visual Studio](../unified-service-desk/media/usd-external-app-adapter-vs.PNG "External application adapter in Visual Studio")  
  
3. Trong Trình khám phá Giải pháp, mở rộng phần Tham khảo để đảm bảo tất cả tham khảo cụm tổ hợp giải quyết chính xác.  
  
4. Open the AppAdapter.cs file and add the following lines of code to set the locations for each component on the page in the class definition.  
  
   ```csharp  
   // Set up your locations for each component on the page.  
           // If you wish, you could use Spy++ to get the actual names as well.  
           // First Name text box  
           int intFirstNameCoordX = 47;  
           int intFirstNameCoordY = 32;  
           // Last Name text box  
           int intLastNameCoordX = 223;  
           int intLastNameCoordY = 32;  
           // Address Text box  
           int intAddressCoordX = 47;  
           int intAddressCoordY = 81;  
           // Customer ID text box  
           int intIDCoordX = 47;  
           int intIDCoordY = 126;  
   ```  
  
5. Thêm mã sau đây vào định nghĩa `NotifyContextChange` để thông báo cho ứng dụng rằng ngữ cảnh đã thay đổi. For more information, see [Context)](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.hostedapplicationadapter.notifycontextchange\(microsoft.uii.csr.context\))  
  
   ```csharp  
   public override bool NotifyContextChange(Context context)  
           {  
               IntPtr ptr = MainWindowHandle;  
               // Find the control (first name) by position  
               IntPtr childHwnd = Win32API.FindWindowByPosition(ptr, new Point(intFirstNameCoordX, intFirstNameCoordY));  
               // Fill data out  
               Win32API.SetWindowTextAny(childHwnd, context["firstname"]);  
               // Find the control (last name) by position  
               childHwnd = Win32API.FindWindowByPosition(ptr, new Point(intLastNameCoordX, intLastNameCoordY));  
               // Fill out the data  
               Win32API.SetWindowTextAny(childHwnd, context["lastname"]);  
               childHwnd = Win32API.FindWindowByPosition(ptr, new Point(intAddressCoordX, intAddressCoordY));  
               Win32API.SetWindowTextAny(childHwnd, context["address1_line1"]);  
               childHwnd = Win32API.FindWindowByPosition(ptr, new Point(intIDCoordX, intIDCoordY));  
               Win32API.SetWindowTextAny(childHwnd, context["CustomerID"]);  
               // Hands control back over to the base class to notify next app of context change.  
               return base.NotifyContextChange(context);  
  
           }  
   ```  
  
6. Thêm mã sau vào định nghĩa thay thế của `DoAction` để cập nhật các trường biểu mẫu với các giá trị từ [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
   ```csharp  
   public override bool DoAction(Microsoft.Uii.Csr.Action action, RequestActionEventArgs args)  
           {  
               IntPtr ptr;  
               IntPtr childHwnd;  
               switch (args.Action)  
               {  
                   case "UpdateFirstName":  
                       // Get locations of what you want to update and handles  
                       ptr = MainWindowHandle;  
                       childHwnd = Win32API.FindWindowByPosition(ptr, new Point(intFirstNameCoordX, intFirstNameCoordY));  
                       // Populate data into fields  
                       Win32API.SetWindowTextAny(childHwnd, args.Data);  
                       break;  
                   case "UpdateLastName":  
                       // Get locations of what you want to update and handles  
                       ptr = MainWindowHandle;  
                       childHwnd = Win32API.FindWindowByPosition(ptr, new Point(intLastNameCoordX, intLastNameCoordY));  
                       // Populate data into fields  
                       Win32API.SetWindowTextAny(childHwnd, args.Data);  
                       break;  
               }  
               return base.DoAction(action, args);  
           }  
   ```  
  
7. Save your project, and build it (**Build** > **Build Solution**). After the project builds successfully, an assembly (ExternalApplicationAdapter.dll) is generated in the \bin\debug folder of your project folder. Bạn sẽ cần cụm tổ hợp này sau để kiểm tra và sử dụng bộ chuyển đổi ứng dụng của mình.  
  
<a name="ConfigureAppAdapter"></a>   
## <a name="step-4-configure-the-application-adapter-in-dynamics-365-for-customer-engagement"></a>Step 4: Configure the application adapter in Dynamics 365 for Customer Engagement  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement**, and then select **Settings**.  
  
3. Choose **Settings** > **Unified Service Desk** > **Hosted Controls**.  
  
4. Từ danh sách kiểm soát tổ chức, chọn kiểm soát tổ chức `QsExternalApp`.  
  
   ![Hosted control in Unified Service Desk](../unified-service-desk/media/usd-external-app-hosted-control.PNG "Hosted control in Unified Service Desk")  
  
5. Trong phần Cấu hình Bộ chuyển đổi, chỉ định các giá trị sau:  
  
   |||  
   |-|-|  
   |Trường|Value|  
   |Bộ điều hợp|Sử dụng bộ điều hợp|  
   |URI|`ExternalApplicationAdapter`|  
   |Loại|`ExternalApplicationAdapter.AppAdapter`|  
  
   ![External adapter configuration in Dynamics 365 for Customer Engagement apps](../unified-service-desk/media/usd-external-adapter-config.PNG "External adapter configuration in Dynamics 365 for Customer Engagement")  
  
   > [!NOTE]
   >  URI là tên của cụm tổ hợp của bạn và Loại là tên của cụm tổ hợp theo sau bởi dấu chấm (.) sau đó là tên lớp trong dự án [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] của bạn. Trong ví dụ này, tên của cụm tổ hợp là `ExternalApplicationAdapter` và tên của lớp là `AppAdapter`, chính là tên lớp mặc định khi bạn tạo bộ chuyển đổi ứng dụng.  
  
6. Bấm vào **Lưu** để lưu thay đổi của bạn.  
  
<a name="TestAppAdapter"></a>   
## <a name="step-5-test-the-application-adapter"></a>Bước 5: Thử nghiệm bộ chuyển đổi ứng dụng  
  
1. Copy the assembly that contains your application adapter definition from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project output folder (\<ProjectFolder>\bin\debug) to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application directory. In this case, we will copy the ExternalApplicationAdapter.dll file to the c:\Program Files\Microsoft Dynamics CRM USD\USD directory.  
  
2. Run [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server.  
  
3. Trên lần đăng nhập thành công, bạn sẽ nhìn thấy ứng dụng bên ngoài mẫu trên màn hình của mình.  
  
4. Choose **Search** and then choose **Contacts** and select a contact. Trong trường hợp này, chúng tôi sẽ chọn `Patrick Sands`.  
  
   ![Contacts list in Unified Service Desk](../unified-service-desk/media/usd-external-app-contacts-list.PNG "Contacts list in Unified Service Desk")  
  
5. Bấm vào **Ứng dụng Bên ngoài Mẫu** và bạn sẽ nhìn thấy tên, họ, địa chỉ và ID của khách hàng được điền vào.  
  
   ![Customer info in external application](../unified-service-desk/media/usd-external-app-customer-info.PNG "Customer info in external application")  
  
> [!NOTE]
>  Cách này cho bạn thấy cách hiển thị hoặc đọc dữ liệu từ [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] trong ứng dụng bên ngoài. To understand how to update the data in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] from the external application, see [Walkthrough: Create a UII Windows Forms Hosted Control](../unified-service-desk/walkthrough-create-uii-windows-forms-hosted-control.md)  
  
### <a name="see-also"></a>Xem thêm  
 [Use UII adapters to interact with external and web applications](../unified-service-desk/use-uii-adapters-interact-external-web-applications.md)
