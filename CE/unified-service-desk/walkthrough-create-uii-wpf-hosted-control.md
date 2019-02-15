---
title: 'Walkthrough: Create a UII WPF Hosted Control | MicrosoftDocs'
description: Demonstrates how you can build a WPF-based User Interface Integration (UII) hosted control that interacts with Unified Service Desk and external applications (standalone and web).
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
ms.assetid: 4a6e9113-3956-448c-9953-ec7ee6f22d9e
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 7f65042a084c1c5caedb6345f5d659705e5dab9c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387850"
---
# <a name="walkthrough-create-a-uii-wpf-hosted-control-in-unified-service-desk"></a>Walkthrough: Create a UII WPF Hosted Control in Unified Service Desk
Cách này trình bày cách bạn có thể xây dựng kiểm soát tổ chức dựa trên [Windows Presentation Foundation (WPF)](https://msdn.microsoft.com/library/ms754130\(v=vs.110\).aspx) [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] tương tác với [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] và các ứng dụng bên ngoài (độc lập và web).  
  
 Trong cách này, bạn sẽ:  
  
- Create a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)][!INCLUDE[pn_wpf_acronym](../includes/pn-wpf-acronym.md)] hosted control, **Sample UII WPF Hosted Control**, which will display first name, last name, street address and ID of a contact when you search for contacts, and click a contact name to open it in a session in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Các giá trị này được hiển thị từ ngữ cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
- Change first name, last name, or street address values in an external application and web application hosted in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] from the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)][!INCLUDE[pn_wpf_acronym](../includes/pn-wpf-acronym.md)] hosted control that we create. The external and web applications were created in the following earlier walkthroughs: [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md).  
  
- Notify changes to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context to update the values there.  
  
<a name="Prereq"></a>   
## <a name="prerequisites"></a>Điều kiện tiên quyết  
  
- [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] 4.5.2  
  
- [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]ứng dụng khách. Điều này là cần thiết để thử nghiệm kiểm soát tổ chức.  
  
- [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)], [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]  
  
- [!INCLUDE[tn_nuget_package_manager](../includes/tn-nuget-package-manager.md)] for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)  
  
- **CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contain the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)][!INCLUDE[pn_wpf_acronym](../includes/pn-wpf-acronym.md)] hosted control project template. [Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].  
  
- You should have completed the [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md) to ensure that you have the external and web applications set up with the adapters to facilitate interaction with those applications.  
  
<a name="step1"></a>   
## <a name="step-1-create-a-uii-wpf-hosted-control-using-visual-studio"></a>Step 1: Create a UII WPF hosted control using Visual Studio  
  
<a name="Step1"></a>   
1. Start [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)], and create a new project.  
  
2. In the **New Project** dialog box:  
  
   1.  From the list of installed templates, expand **Visual C#**, and select **Dynamics 365 for Customer Engagement apps SDK Templates** > **Unified Service Desk** > **UII WPF Hosted Control**.  
  
   2.  Chỉ định tên và vị trí của dự án và chọn **OK** để tạo dự án mới.  
  
   ![Create a UII WPF hosted control](../unified-service-desk/media/usd-create-uii-wpf-hosted-control-1.png "Create a UII WPF hosted control")  
  
3. In **Solution Explorer**, right-click the **UiiWpfControl.xaml** file, and select **Open** to display the XAML designer.  
  
4. In the designer, add the following controls from the **Toolbox**:  
  
   |Loại kiểm soát|Tên|Text|  
   |------------------|----------|----------|  
   |Nhãn|lblFirstName|Tên|  
   |Nhãn|lblLastName|Họ|  
   |Nhãn|lblAddress|Địa chỉ Đường phố|  
   |Nhãn|lblID|ID|  
   |Hộp văn bản|txtFirstName||  
   |Hộp văn bản|txtLastName||  
   |Hộp văn bản|txtAddress||  
   |Hộp văn bản|txtID||  
   |Nút|btnUpdate|Update values in hosted apps|  
   |Nút|btnUpdateContext|Cập nhật ngữ cảnh|  
  
    This is how the controls should be laid out in the XAML designer.  
  
   ![Controls layout in the XAML designer](../unified-service-desk/media/usd-create-uii-wpf-hosted-control-2.png "Controls layout in the XAML designer")  
  
5. Double-click the **Update values in hosted apps** button (btnUpdate) to add the code for the `click` event for this button, and add the following code.  
  
   ```csharp  
   private void btnUpdate_Click(object sender, System.Windows.RoutedEventArgs e)  
   {  
      // This is how you fire an action to other hosted applications.   
      // The DoAction() code in the other application or application adapter   
      // will be called.  
      FireRequestAction(new RequestActionEventArgs("QsExternalApp", "UpdateFirstName", txtFirstName.Text)); // For the external application  
      FireRequestAction(new RequestActionEventArgs("QsExternalApp", "UpdateLastName", txtLastName.Text)); // For the external application  
      FireRequestAction(new RequestActionEventArgs("QsExternalApp", "UpdateAddress", txtAddress.Text)); // For the external application  
  
      FireRequestAction(new RequestActionEventArgs("QsWebApplication", "UpdateFirstName", txtFirstName.Text)); // For the external web application  
      FireRequestAction(new RequestActionEventArgs("QsWebApplication", "UpdateLastName", txtLastName.Text)); // For the external web application  
      FireRequestAction(new RequestActionEventArgs("QsWebApplication", "UpdateAddress", txtAddress.Text)); // For the external web application  
   }  
   ```  
  
6. Go to the XAML designer, and double-click the **Update context** button (btnUpdateContext) to add the code for the `click` event for this button. Add the following code.  
  
   ```csharp  
   private void btnContextChange_Click(object sender, System.Windows.RoutedEventArgs e)  
   {  
      // Get the current context and create a new context object from it.  
      string temp = Context.GetContext();  
      Context updatedContext = new Context(temp);  
  
      // Update the new context with the changed information.  
      updatedContext["firstname"] = txtFirstName.Text;  
      updatedContext["lastname"] = txtLastName.Text;  
      updatedContext["address1_line1"] = txtAddress.Text;  
  
      // Notify Unified Service Desk of this new context information.  
      FireChangeContext(new ContextEventArgs(updatedContext));  
  
      // Notify this UII hosted control about the change.  
      NotifyContextChange(updatedContext);  
   }  
   ```  
  
7. In the same file (UiiWpfControl.xaml.cs), update the override definition of the `NotifyContextChange` method to the following.  
  
   ```csharp  
   public override void NotifyContextChange(Context context)  
   {  
      // Populating text fields from context information.  
      txtFirstName.Text = context["firstname"];  
      txtLastName.Text = context["lastname"];  
      txtAddress.Text = context["address1_line1"];  
      txtID.Text = context["CustomerID"];  
  
      base.NotifyContextChange(context);  
   }  
   ```  
  
8. Save your project, and build it (**Build** > **Build Solution**). After the project builds successfully, an assembly (.dll file) is generated with the same name as your project name (in this case, UIIWPFHostedControl1.dll) in the /bin/debug folder of your project.  
  
9. Copy this file to your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application installation directory (typically C:\Program Files\Microsoft Dynamics CRM USD\USD). This file is required for testing, and eventually using this control from your client application.  
  
   > [!TIP]
   >  Note the name of the class that is used to build your [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control in the UiiWpfControl.xaml.cs file. Trong trường hợp này, đó là `UiiWpfControl`. You’ll need this information in the next step.  
  
<a name="step2"></a>   
## <a name="step-2-define-the-hosted-control-in-unified-service-desk"></a>Bước 2: Xác định kiểm soát tổ chức trong Unified Service Desk  
 Để lưu trữ [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] kiểm soát tổ chức WPF trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], bạn sẽ phải xác định và đặt cấu hình kiểm soát đó.  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk**.  
  
3. On the **Unified Service Desk** page, choose **Hosted Controls**.  
  
4. Trên trang **Kiểm soát Tổ chức**, chọn **Mới**.  
  
5. On the **New Hosted Control** page, specify the following values.  
  
   |Trường|Value|  
   |-----------|-----------|  
   |Tên|UIIWPFHostedControl|  
   |Tên Hiển thị|Sample UII WPF Hosted Control|  
   |USD Component Type|CCA Hosted Application|  
   |Ứng dụng được lưu trữ|Kiểm soát được lưu trữ|  
   |Ứng dụng toàn cầu|Được chọn|  
   |Nhóm hiển thị|Bảng điều khiển chính|  
   |Bộ điều hợp|Use No Adapter|  
   |URI cụm tổ hợp|UIIWPFHostedControl1|  
   |Loại cụm tổ hợp|UIIWPFHostedControl1.UiiWpfControl|  
  
   > [!NOTE]
   > **Assembly URI** is the name of your assembly and the **Assembly Type** is the name of your assembly followed by a dot (.) and then the class name in your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project. Trong ví dụ này, tên của cụm tổ hợp là `UIIWPFHostedControl1` và tên của lớp là `UiiWpfControl`, tên lớp mặc định khi bạn tạo kiểm soát tổ chức WPF [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)].  
  
   ![Define a new hosted control](../unified-service-desk/media/usd-new-hosted-control-uii-wpf.png "Define a new hosted control")  
  
6. Choose **Save** to create the hosted control.  
  
<a name="step3"></a>   
## <a name="step-3-define-uii-actions-for-the-external-application-and-web-application-hosted-controls-in-unified-service-desk"></a>Step 3: Define UII actions for the external application and web application hosted controls in Unified Service Desk  
 Bộ chuyển đổi cho các ứng dụng độc lập và web hiển thị ba hành động sau: `UpdateFirstName`, `UpdateLastName` và `UpdateAddress`. These adapters and the hosted controls for the external standalone and web applications were created in the earlier walkthroughs ([Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md)).  
  
 To update information in the external applications from within the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] WPF hosted control, you’ll have to define three [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions with the same name as defined earlier in the adapters for each of the external applications. In the earlier adapter walkthroughs ([Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application  Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md)), we defined the following two hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to display the external applications within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  `QsExternalApp` and `QsExternalWebApplication`. Trong bước này, chúng ta sẽ thêm ba hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] cho mỗi kiểm soát tổ chức.  
  
> [!IMPORTANT]
>  If you have already added the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions as part of step 3 in [Walkthrough: Create a UII Windows Forms Hosted Control](../unified-service-desk/walkthrough-create-uii-windows-forms-hosted-control.md), you don’t have to perform this step again. You can proceed to the next section for testing your hosted control.  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk**.  
  
3. On the **Unified Service Desk** page, choose **Hosted Controls**.  
  
4. Trên trang **Kiểm soát Tổ chức**, tìm kiếm `QSExternalApp` và mở để chỉnh sửa.  
  
5. Trên trang `QSExternalApp`, chọn mũi tên xuống bên cạnh tên kiểm soát tổ chức rồi chọn **Hành động UII**.  
  
6. Trên trang tiếp theo, chọn **Thêm Hành động UII Mới**.  
  
7. Trên trang **Hành động UII Mới**, nhập tên dưới dạng `UpdateFirstName` và chọn **Lưu & Đóng**. Thao tác này thêm hành động vào trang trước.  
  
8. Tương tự, thêm hai hành động sau:  `UpdateLastName` và `UpdateAddress`. Tất cả ba hành động này sẽ có sẵn cho kiểm soát tổ chức `QSExternalApp`.  
  
   ![Available UII actions for a hosted control](../unified-service-desk/media/usd-available-uii-actions-hosted-control.png "Available UII actions for a hosted control")  
  
9. Làm theo các bước 4 đến 8 để tạo ba hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] với cùng tên cho **QSExternalWebApp**.  
  
<a name="test"></a>   
## <a name="test-the-hosted-control"></a>Kiểm tra kiểm soát tổ chức  
 Before you test the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)][!INCLUDE[pn_wpf_acronym](../includes/pn-wpf-acronym.md)] hosted control, ensure that your sample web application is running so that it renders within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
1. Run [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.  
  
2. Trên lần đăng nhập thành công, bạn sẽ nhìn thấy ba kiểm soát tổ chức: **Kiểm soát Tổ chức WPF UII Mẫu**, **Ứng dụng Web Bên ngoài Mẫu** và **Ứng dụng Bên ngoài Mẫu**.  
  
   ![Sample UII WPF hosted control avaiilable](../unified-service-desk/media/usd-sample-hosted-controls-available-uii-wpf.png "Sample UII WPF hosted control avaiilable")  
  
3. Choose **Search**, and then choose **Contacts**. Choose any of the contacts to display the contact details in a session. Điều này cũng hiển thị tên, họ, địa chỉ đường phố và ID của hồ sơ liên hệ hiện được hiển thị trong tất cả ba kiểm soát mẫu:  
  
   ![Data displayed from USD context in the 3 controls](../unified-service-desk/media/usd-sample-controls-uii-wpf.png "Data displayed from USD context in the 3 controls")  
  
4. Thay đổi các giá trị trong **Kiểm soát Tổ chức WPF UII Mẫu** và bấm **Cập nhật các giá trị trong ứng dụng được lưu trữ** để cập nhật các giá trị trong hai ứng dụng bên ngoài khác.  
  
   ![Updated values in external apps](../unified-service-desk/media/usd-sample-controls-updated-values-uii-wpf.png "Updated values in external apps")  
  
5. Trong **Kiểm soát Tổ chức WPF UII Mẫu**, chọn **Cập nhật ngữ cảnh** để cập nhật thông tin ngữ cảnh trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
   ![Values updated in USD context](../unified-service-desk/media/usd-uii-wpf-values-updated-context.png "Values updated in USD context")  
  
### <a name="see-also"></a>Xem thêm  
 [Integrate with external applications and web applications](../unified-service-desk/integrate-external-applications-web-applications.md)   
 [Work with UII Hosted Controls](../unified-service-desk/use-uii-hosted-controls-unified-service-desk.md)   
 [Cách: Tạo một Kiểm soát Tổ chức Biểu mẫu Windows UII](../unified-service-desk/walkthrough-create-uii-windows-forms-hosted-control.md)   
 [Hành động UII](../unified-service-desk/uii-actions.md)
