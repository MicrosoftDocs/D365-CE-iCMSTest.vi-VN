---
title: 'Walkthrough: Create a UII Windows Forms Hosted Control | MicrosoftDocs'
description: Demonstrates how you can build a Windows Forms UII hosted control that interacts with Unified Service Desk and standalone or web external applications.
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
ms.assetid: a9fd1d9e-b04e-4ea0-b9c2-fda7bac4b7f9
caps.latest.revision: 7
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: d2145bccc14b57e04c6d96512c03fd356dfbb9e2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387538"
---
# <a name="walkthrough-create-a-uii-windows-forms-hosted-control-in-unified-service-desk"></a>Walkthrough: Create a UII Windows Forms Hosted Control in Unified Service Desk
Cách này trình bày cách bạn có thể xây dựng kiểm soát tổ chức [Biểu mẫu Windows](https://msdn.microsoft.com/library/ms229601\(v=vs.110\).aspx) [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] tương tác với [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] và ứng dụng web hoặc bên ngoài.  
  
 Trong cách này, bạn sẽ:  
  
- Tạo [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] kiểm soát tổ chức Biểu mẫu Windows, **Kiểm soát Tổ chức Biểu mẫu Windows UII Mẫu**, sẽ hiển thị tên, họ, địa chỉ đường phố và ID của người liên hệ khi bạn tìm kiếm liên hệ và bấm vào tên người liên hệ để mở trong một phiên trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. Các giá trị này được hiển thị từ ngữ cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
- Thay đổi các giá trị tên, họ hoặc địa chỉ đường phố trong ứng dụng bên ngoài và web được lưu trữ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] từ kiểm soát tổ chức Biểu mẫu Windows [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] mà chúng ta đã tạo. The external and web applications were created in earlier walkthroughs: [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md).  
  
- Thông báo các thay đổi đối với ngữ cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để cập nhật các giá trị tại đó.  
  
<a name="Prereq"></a>   
## <a name="prerequisites"></a>Điều kiện tiên quyết  
  
- [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] 4.5.2  
  
- [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application; required for testing the hosted control.  
  
- [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)], [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]  
  
- [!INCLUDE[tn_nuget_package_manager](../includes/tn-nuget-package-manager.md)] for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)  
  
- **CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the UII Windows Forms hosted control project template. [Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].  
  
- You should have completed [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md) to ensure that you have the external application and web application set up with the respective adapters to facilitate interaction with those applications.  
  
<a name="step1"></a>   
## <a name="step-1-create-a-uii-windows-forms-hosted-control-using-visual-studio"></a>Step 1: Create a UII Windows Forms hosted control using Visual Studio  
  
<a name="Step1"></a>   
1. Start [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)], and create a new project.  
  
2. In the **New Project** dialog box:  
  
   1.  From the list of installed templates, expand **Visual C#**, and select **Dynamics 365 for Customer Engagement apps SDK Templates** > **Unified Service Desk** > **UII Windows Forms Hosted Control**.  
  
   2.  Specify the name and location of the project, and click **OK** to create a new project.  
  
   ![Create a UII Windows Form hosted control](../unified-service-desk/media/usd-create-uii-windows-form-hosted-control-1.png "Create a UII Windows Form hosted control")  
  
3. Trong ngăn **Trình khám phá Giải pháp**, bấm chuột phải vào tệp **UiiWinformControl.cs** và chọn **Mở** để hiển thị trình thiết kế Biểu mẫu Windows.  
  
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
   |Nút|btnUpdate|Cập nhật các giá trị trong ứng dụng được lưu trữ|  
   |Nút|btnUpdateContext|Cập nhật ngữ cảnh|  
  
    Đây là cách các kiểm soát nên được đặt trong trình thiết kế.  
  
   ![Layout of the controls in your UII hosted control](../unified-service-desk/media/usd-ui-iwindows-form-hosted-control-design.png "Layout of the controls in your UII hosted control")  
  
5. Bấm đúp vào nút **Cập nhật các giá trị trong ứng dụng được lưu trữ** (`btnUpdate`) để thêm mã cho sự kiện `click` cho nút này và thêm mã sau.  
  
   ```csharp  
   private void btnUpdate_Click(object sender, EventArgs e)  
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
  
6. Đi đến chế độ xem thiết kế, bấm đúp vào nút **Cập nhật ngữ cảnh** (`btnUpdateContext`) để thêm mã cho sự kiện bấm chuột cho nút này. Thêm mã sau.  
  
   ```csharp  
   private void btnUpdateContext_Click(object sender, EventArgs e)  
   {  
      // Get the current context and create a new context object from it.  
      string temp = Context.GetContext();  
      Context updatedContext = new Context(temp);  
  
      // Update the new context with the changed information.  
      updatedContext["firstname"] = txtFirstName.Text;  
      updatedContext["lastname"] = txtLastName.Text;  
      updatedContext["address1_line1"] = txtAddress.Text;  
  
      // Notify Unified Service Desk of this new context information  
      FireChangeContext(new ContextEventArgs(updatedContext));  
  
      // Notify this UII hosted control about the change  
      NotifyContextChange(updatedContext);  
   }  
   ```  
  
7. In the same file (UiiWinformControl.cs), update the override definition of the `NotifyContextChange` method to the following:  
  
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
  
8. Save your project, and build it (**Build** > **Build Solution**). After the project builds successfully, an assembly (.dll file) is generated with the same name as your project name (in this case, UIIWindowsFormHostedConrol1.dll) in the /bin/debug folder of your project.  
  
9. Copy this file to your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application installation directory (typically C:\Program Files\Microsoft Dynamics CRM USD\USD). Cần có tệp này để thử nghiệm và cuối cùng là sử dụng kiểm soát này từ ứng dụng khách của bạn.  
  
   > [!TIP]
   >  Note the name of the class that is used to build your [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control in the UiiWinformControl.cs file. Trong trường hợp này, đó là UiiWinformControl. Bạn sẽ cần thông tin này trong bước tiếp theo.  
  
<a name="step2"></a>   
## <a name="step-2-define-the-hosted-control-in-unified-service-desk"></a>Bước 2: Xác định kiểm soát tổ chức trong Unified Service Desk  
 Để lưu trữ kiểm soát tổ chức Biểu mẫu Windows [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], bạn sẽ phải xác định và đặt cấu hình chúng.  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk**.  
  
3. On the **Unified Service Desk** page, click **Hosted Controls**.  
  
4. Trên trang **Kiểm soát Tổ chức**, bấm vào **Mới**.  
  
5. On the **New Hosted Control** page, specify the following values:  
  
   |Trường|Value|  
   |-----------|-----------|  
   |Tên|UIIWindowsFormHostedControl|  
   |Tên Hiển thị|Kiểm soát Tổ chức Biểu mẫu Windows UII Mẫu|  
   |USD Component Type|Ứng dụng được lưu trữ CCA|  
   |Ứng dụng được lưu trữ|Kiểm soát được lưu trữ|  
   |Ứng dụng toàn cầu|Được chọn|  
   |Nhóm hiển thị|Bảng điều khiển chính|  
   |Bộ điều hợp|Use No Adapter|  
   |URI cụm tổ hợp|UIIWindowsFormHostedControl1|  
   |Loại cụm tổ hợp|UIIWindowsFormHostedControl1.UiiWinformControl|  
  
   > [!NOTE]
   > **URI cụm tổ hợp** là tên của cụm tổ hợp của bạn và **Loại Cụm tổ hợp** là tên của cụm tổ hợp của bạn theo sau là dấu chấm (.) và sau đó là tên lớp trong dự án [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] của bạn. Trong ví dụ này, tên của cụm tổ hợp là `UIIWindowsFormHostedControl1` và tên của lớp là `UiiWinformControl`, là tên lớp mặc định khi bạn tạo kiểm soát tổ chức Biểu mẫu Windows [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)].  
  
   ![New hosted control in Unified Service Desk](../unified-service-desk/media/usd-new-hosted-control-uii-windows-form.png "New hosted control in Unified Service Desk")  
  
6. Click **Save** to create the hosted control.  
  
<a name="step3"></a>   
## <a name="step-3-define-uii-actions-for-the-external-application-and-web-application-hosted-controls-in-unified-service-desk"></a>Bước 3: Xác định hành động UII cho kiểm soát tổ chức ứng dụng bên ngoài và ứng dụng web trong Unified Service Desk  
 Bộ chuyển đổi cho các ứng dụng độc lập và web hiển thị ba hành động sau: `UpdateFirstName`, `UpdateLastName` và `UpdateAddress`. These adapters and the hosted controls for the external standalone and web applications were created in the earlier adapter walkthroughs ([Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md)).  
  
 Để cập nhật thông tin trong các ứng dụng bên ngoài từ trong [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] kiểm soát tổ chức Biểu mẫu Windows, bạn sẽ phải xác định ba hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] với cùng tên như được định nghĩa trước trong các bộ chuyển đổi cho mỗi ứng dụng bên ngoài. In the earlier adapter walkthroughs ([Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md)), you defined the following two hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to display the external applications within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]: `QsExternalApp` and `QsExternalWebApplication`. Trong bước này, bạn sẽ thêm ba hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] cho mỗi kiểm soát tổ chức.  
  
> [!IMPORTANT]
>  If you have already added the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions as part of step 3 in [Walkthrough: Create a UII WPF Hosted Control](../unified-service-desk/walkthrough-create-uii-wpf-hosted-control.md), you don’t have to perform this step again. Bạn có thể tiến hành phần tiếp theo để kiểm tra kiểm soát tổ chức của mình.  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk**.  
  
3. On the **Unified Service Desk** page, choose **Hosted Controls**.  
  
4. Trên trang **Kiểm soát Tổ chức**, tìm kiếm `QsExternalApp` và mở để chỉnh sửa.  
  
5. Trên trang **QsExternalApp**, bấm vào mũi tên xuống bên cạnh tên kiểm soát tổ chức, rồi bấm vào **Hành động UII**.  
  
6. Trên trang tiếp theo, bấm vào **thêm hành động UII mới**.  
  
7. Nhập tên là **UpdateFirstName** và bấm vào **Lưu & Đóng**. Thao tác này sẽ thêm hành động vào trang trước.  
  
8. Tương tự, thêm hai hành động sau: **UpdateLastName** và **UpdateAddress**. Tất cả ba hành động này sẽ có sẵn cho kiểm soát tổ chức `QsExternalApp`.  
  
   ![Available UII actions for a hosted control](../unified-service-desk/media/usd-available-uii-actions-hosted-control.png "Available UII actions for a hosted control")  
  
9. Làm theo các bước 4 đến 8 để tạo ba hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] với cùng tên cho kiểm soát tổ chức `QsExternalWebApp`.  
  
<a name="test"></a>   
## <a name="test-the-hosted-control"></a>Kiểm tra kiểm soát tổ chức  
 Trước khi bạn kiểm tra kiểm soát tổ chức Biểu mẫu Windows [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)], đảm bảo rằng ứng dụng web mẫu của bạn đang chạy sao cho ứng dụng hiển thị bên trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
1. Run the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.  
  
2. Trên lần đăng nhập an toàn, bạn sẽ nhìn thấy ba kiểm soát tổ chức: **Kiểm soát Tổ chức Biểu mẫu Windows UII Mẫu**, **Ứng dụng Web Bên ngoài Mẫu** và **Ứng dụng Bên ngoài Mẫu**.  
  
   ![Sample hosted controls available](../unified-service-desk/media/usd-sample-hosted-controls-available.png "Sample hosted controls available")  
  
3. Chọn **Tìm kiếm** rồi chọn **Người liên hệ**. Chọn bất kỳ người liên hệ nào để hiển thị chi tiết liên hệ trong một phiên. Điều này cũng hiển thị tên, họ, địa chỉ đường phố và ID của hồ sơ liên hệ hiện được hiển thị trong tất cả ba kiểm soát mẫu như được trình bày trong hình minh họa sau.  
  
   ![Sample controls in USD with contact information](../unified-service-desk/media/usd-3-samplecontrols-1.png "Sample controls in USD with contact information")  
  
4. Thay đổi các giá trị trong **Kiểm soát Tổ chức Biểu mẫu Windows UII Mẫu** và bấm vào **Cập nhật giá trị trong ứng dụng được lưu trữ** để cập nhật các giá trị trong hai ứng dụng bên ngoài khác.  
  
   ![Sample controls with updated values](../unified-service-desk/media/usd-3-sample-controls-updated-values.png "Sample controls with updated values")  
  
5. Trong **Kiểm soát Tổ chức Biểu mẫu Windows UII Mẫu**, bấm vào **Cập nhật ngữ cảnh** để cập nhật thông tin ngữ cảnh trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].  
  
   ![Values updated in the USD context](../unified-service-desk/media/usd-values-updated-context.png "Values updated in the USD context")  
  
### <a name="see-also"></a>Xem thêm  
 [Work with UII Hosted Controls](../unified-service-desk/use-uii-hosted-controls-unified-service-desk.md)   
 [Cách: Tạo Kiểm soát Tổ chức UII WPF](../unified-service-desk/walkthrough-create-uii-wpf-hosted-control.md)
